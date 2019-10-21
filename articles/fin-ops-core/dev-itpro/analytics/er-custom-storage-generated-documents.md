---
title: Angi et egendefinert lagringssted for genererte dokumenter
description: Dette emnet forklarer hvordan du utvider listen over lagringssteder for dokumenter som Elektronisk rapportering (ER)-formater genererer.
author: NickSelin
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: a1c41cd4440eaf70f720bfd64884e6ef4662f87a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181479"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a>Angi et egendefinert lagringssted for genererte dokumenter

[!include[banner](../includes/banner.md)]

API (Application programming interface) for Elektronisk rapportering-rammeverket (ER) lar deg utvide listen over lagringssteder for dokumenter som ER-formater genererer. Dette emnet inneholder en oversikt over de viktigste oppgavene du må fullføre for å legge til et egendefinert lagringssted.

## <a name="prerequisites"></a>Forutsetninger

Du må distribuere en topologi som støtter fortløpende bygging. (Hvis du vil ha mer informasjon, kan du se [Distribuere topologier som støtter sammenhengende automatisering av bygging og testing](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Du må ha tilgang til denne topologien for én av følgende roller:

- Utvikler av elektronisk rapportering
- Funksjonell konsulent for elektronisk rapportering
- Systemansvarlig

Du må også ha tilgang til utviklingsmiljøet for denne topologien.

## <a name="create-or-import-an-er-format-configuration"></a>Opprette eller importere en ER-formatkonfigurasjon

I gjeldende topologi [oppretter du et nytt ER-format](tasks/er-format-configuration-2016-11.md) for å generere dokumenter du har tenkt å legge til et egendefinert lagringssted for. Du kan også [importere et eksisterende ER-format til denne topologien](general-electronic-reporting-manage-configuration-lifecycle.md).

![Formatutformingsside](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> ER-formatet som du oppretter eller importerer, må inneholde minst ett av følgende formatelementer:
>
> - Fil
> - Mappe
> - Sammenslåing
> - Vedlegg

## <a name="create-a-new-document-type"></a>Opprette en ny dokumenttype

Hvis du vil angi hvordan dokumenter som et ER-format genererer, rutes, må du konfigurere [ER-mål](electronic-reporting-destinations.md). I hvert ER-mål som konfigureres til å lagre genererte dokumenter som filer, må du angi en dokumenttype for dokumentbehandlingsrammeverket. Ulike dokumenttyper kan brukes til å rute dokumenter som ulike ER-formater genererer.

1. Legg til en ny [dokumenttype](../../fin-and-ops/organization-administration/configure-document-management.md) for ER-formatet som du opprettet eller importerte tidligere. I illustrasjonen nedenfor er dokumenttypen **FileX**.
2. For å skille denne dokumenttypen fra andre dokumenttyper inkluderes et bestemt nøkkelord i navnet. I illustrasjonen nedenfor er navnet **(LOKAL) mappe**.
3. I **Klasse**-feltet angir du **Tilknytt fil**.
4. I **Gruppe**-feltet angir du **Fil**.

![Siden Dokumenttyper](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> Dokumenttypene er firmaspesifikke. Hvis du vil bruke et ER-format med et konfigurert mål i flere firmaer, må du konfigurere en egen dokumenttype i hvert firma.

## <a name="review-source-code"></a>Gå gjennom kildekode

Gå gjennom koden for **insertFile()**-metoden for **ERDocuManagement**-klasse. Legg merke til at **AttachingFile()**-hendelsen starter når den genererte filen er knyttet til en post.

```
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

**AttachingFile()**-hendelsen oppstår når følgende ER-mål behandles:

- **Arkiv** – Når dette målet brukes, opprettes en ny post for ER-formatet som kjøres, i ERFormatMappingRunJobTable-tabellen. **Arkivert**-feltet i denne oppføringen er satt til **Usann**. Hvis kjøringen av ER-formatet er vellykket, knyttes det genererte dokumentet til denne posten, og **AttachingFile()**-hendelsen oppstår. Dokumenttypen som velges i dette ER-målet, bestemmer lagringsstedet for den vedlagte filen (Microsoft Azure Storage eller en Microsoft SharePoint-mappe).
- **Jobbarkiv** – Når dette målet brukes, opprettes en ny post for ER-skjemaet som kjøres, i ERFormatMappingRunJobTable-tabellen. **Arkivert**-feltet i denne oppføringen er satt til **Sann**. Hvis kjøringen av ER-formatet er vellykket, knyttes det genererte dokumentet til denne posten, og **AttachingFile()**-hendelsen oppstår. Dokumenttypen som konfigureres i ER-parameterne, bestemmer lagringsstedet for den vedlagte filen (Azure Storage eller en Microsoft SharePoint-mappe).

![Siden Parametere for elektronisk rapportering](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a>Konfigurere et ER-mål

1. Konfigurer det arkiverte målet for et av de tidligere nevnte elementene (fil, mappe, sammenslåing eller vedlegg) for ER-formatet du opprettet eller importerte. For å få hjelp kan du se [ER Konfigurere mål](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).
2. Bruk dokumenttypen du la til tidligere for det konfigurerte målet. (For eksemplet i dette emnet er dokumenttypen **FileX**.)

![Dialogboksen Innstillinger for mål](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a>Endre kildekode

1. Legg til en ny klasse i Microsoft Visual Studio-prosjektet ditt, og skriv kode for å abonnere på **AttachingFile()**-hendelsen som ble nevnt tidligere. (Hvis du vil ha mer informasjon om utvidelsesmønsteret som brukes, se [Svare ved hjelp av EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) I den nye klassen kan du for eksempel skrive kode som utfører følgende handlinger:

    1. Lagre genererte filer i en mappe i det lokale filsystemet på serveren som kjører tjenesten Application Object Server (AOS).
    2. Lagre disse genererte filene bare når den nye dokumenttypen (for eksempel **FileX**-typen med nøkkelordet "(LOKAL)" i navnet) brukes når en fil knyttes til posten i ER-kjøringsjobbloggen.

    ```
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. Bygg prosjektet på nytt.

## <a name="run-the-er-format-that-you-created-or-imported"></a>Kjøre ER-formatet som du opprettet eller importerte

1. Kjør ER-formatet som du opprettet eller importerte.
2. Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Elektroniske rapporteringsjobber**. Finn posten som ble opprettet for denne kjøringsjobben, og som har den genererte filen tilknyttet.
3. Utforsk lokal **C:\\0**-mappen for å finne den samme genererte filen.

## <a name="additional-resources"></a>Tilleggsressurser

- [Mål for elektronisk rapportering](electronic-reporting-destinations.md)
- [Startside med utvidelsesmuligheter](../extensibility/extensibility-home-page.md)
