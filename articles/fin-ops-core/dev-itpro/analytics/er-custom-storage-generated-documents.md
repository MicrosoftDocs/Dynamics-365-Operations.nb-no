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
ms.openlocfilehash: f65118b6a7393ced9d80c30fad7540a7b27da6c7
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569090"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a><span data-ttu-id="bd34e-103">Angi et egendefinert lagringssted for genererte dokumenter</span><span class="sxs-lookup"><span data-stu-id="bd34e-103">Specify a custom storage location for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="bd34e-104">API (Application programming interface) for Elektronisk rapportering-rammeverket (ER) lar deg utvide listen over lagringssteder for dokumenter som ER-formater genererer.</span><span class="sxs-lookup"><span data-stu-id="bd34e-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="bd34e-105">Dette emnet inneholder en oversikt over de viktigste oppgavene du må fullføre for å legge til et egendefinert lagringssted.</span><span class="sxs-lookup"><span data-stu-id="bd34e-105">This topic includes an overview of the main tasks that you must complete to add a custom storage location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bd34e-106">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="bd34e-106">Prerequisites</span></span>

<span data-ttu-id="bd34e-107">Du må distribuere en topologi som støtter fortløpende bygging.</span><span class="sxs-lookup"><span data-stu-id="bd34e-107">You must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="bd34e-108">(Hvis du vil ha mer informasjon, kan du se [Distribuere topologier som støtter sammenhengende automatisering av bygging og testing](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Du må ha tilgang til denne topologien for én av følgende roller:</span><span class="sxs-lookup"><span data-stu-id="bd34e-108">(For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="bd34e-109">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="bd34e-109">Electronic reporting developer</span></span>
- <span data-ttu-id="bd34e-110">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="bd34e-110">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="bd34e-111">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="bd34e-111">System administrator</span></span>

<span data-ttu-id="bd34e-112">Du må også ha tilgang til utviklingsmiljøet for denne topologien.</span><span class="sxs-lookup"><span data-stu-id="bd34e-112">You must also have access to the development environment for this topology.</span></span>

## <a name="create-or-import-an-er-format-configuration"></a><span data-ttu-id="bd34e-113">Opprette eller importere en ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="bd34e-113">Create or import an ER format configuration</span></span>

<span data-ttu-id="bd34e-114">I gjeldende topologi [oppretter du et nytt ER-format](tasks/er-format-configuration-2016-11.md) for å generere dokumenter du har tenkt å legge til et egendefinert lagringssted for.</span><span class="sxs-lookup"><span data-stu-id="bd34e-114">In the current topology, [create a new ER format](tasks/er-format-configuration-2016-11.md) to generate documents that you plan to add a custom storage location for.</span></span> <span data-ttu-id="bd34e-115">Du kan også [importere et eksisterende ER-format til denne topologien](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="bd34e-115">Alternatively, [import an existing ER format into this topology](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![Formatutformingsside](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> <span data-ttu-id="bd34e-117">ER-formatet som du oppretter eller importerer, må inneholde minst ett av følgende formatelementer:</span><span class="sxs-lookup"><span data-stu-id="bd34e-117">The ER format that you create or import must contain at least one of the following format elements:</span></span>
>
> - <span data-ttu-id="bd34e-118">Fil</span><span class="sxs-lookup"><span data-stu-id="bd34e-118">File</span></span>
> - <span data-ttu-id="bd34e-119">Mappe</span><span class="sxs-lookup"><span data-stu-id="bd34e-119">Folder</span></span>
> - <span data-ttu-id="bd34e-120">Sammenslåing</span><span class="sxs-lookup"><span data-stu-id="bd34e-120">Merger</span></span>
> - <span data-ttu-id="bd34e-121">Vedlegg</span><span class="sxs-lookup"><span data-stu-id="bd34e-121">Attachment</span></span>

## <a name="create-a-new-document-type"></a><span data-ttu-id="bd34e-122">Opprette en ny dokumenttype</span><span class="sxs-lookup"><span data-stu-id="bd34e-122">Create a new document type</span></span>

<span data-ttu-id="bd34e-123">Hvis du vil angi hvordan dokumenter som et ER-format genererer, rutes, må du konfigurere [ER-mål](electronic-reporting-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="bd34e-123">To specify how documents that an ER format generates are routed, you must configure [ER destinations](electronic-reporting-destinations.md).</span></span> <span data-ttu-id="bd34e-124">I hvert ER-mål som konfigureres til å lagre genererte dokumenter som filer, må du angi en dokumenttype for dokumentbehandlingsrammeverket.</span><span class="sxs-lookup"><span data-stu-id="bd34e-124">In each ER destination that is configured to store generated documents as files, you must specify a document type of the Document management framework.</span></span> <span data-ttu-id="bd34e-125">Ulike dokumenttyper kan brukes til å rute dokumenter som ulike ER-formater genererer.</span><span class="sxs-lookup"><span data-stu-id="bd34e-125">Different document types can be used to route documents that different ER formats generate.</span></span>

1. <span data-ttu-id="bd34e-126">Legg til en ny [dokumenttype](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) for ER-formatet som du opprettet eller importerte tidligere.</span><span class="sxs-lookup"><span data-stu-id="bd34e-126">Add a new [document type](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) for the ER format that you created or imported earlier.</span></span> <span data-ttu-id="bd34e-127">I illustrasjonen nedenfor er dokumenttypen **FileX**.</span><span class="sxs-lookup"><span data-stu-id="bd34e-127">In the illustration that follows, the document type is **FileX**.</span></span>
2. <span data-ttu-id="bd34e-128">For å skille denne dokumenttypen fra andre dokumenttyper inkluderes et bestemt nøkkelord i navnet.</span><span class="sxs-lookup"><span data-stu-id="bd34e-128">To differentiate this document type from other document types, include a specific keyword in its name.</span></span> <span data-ttu-id="bd34e-129">I illustrasjonen nedenfor er navnet **(LOKAL) mappe**.</span><span class="sxs-lookup"><span data-stu-id="bd34e-129">For example, in the illustration that follows, the name is **(LOCAL) folder**.</span></span>
3. <span data-ttu-id="bd34e-130">I **Klasse**-feltet angir du **Tilknytt fil**.</span><span class="sxs-lookup"><span data-stu-id="bd34e-130">In the **Class** field, specify **Attach file**.</span></span>
4. <span data-ttu-id="bd34e-131">I **Gruppe**-feltet angir du **Fil**.</span><span class="sxs-lookup"><span data-stu-id="bd34e-131">In the **Group** field, specify **File**.</span></span>

![Siden Dokumenttyper](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> <span data-ttu-id="bd34e-133">Dokumenttypene er firmaspesifikke.</span><span class="sxs-lookup"><span data-stu-id="bd34e-133">Document types are company-specific.</span></span> <span data-ttu-id="bd34e-134">Hvis du vil bruke et ER-format med et konfigurert mål i flere firmaer, må du konfigurere en egen dokumenttype i hvert firma.</span><span class="sxs-lookup"><span data-stu-id="bd34e-134">To use an ER format with a configured destination in multiple companies, you must configure a separate document type in each company.</span></span>

## <a name="review-source-code"></a><span data-ttu-id="bd34e-135">Gå gjennom kildekode</span><span class="sxs-lookup"><span data-stu-id="bd34e-135">Review source code</span></span>

<span data-ttu-id="bd34e-136">Gå gjennom koden for **insertFile()**-metoden for **ERDocuManagement**-klasse.</span><span class="sxs-lookup"><span data-stu-id="bd34e-136">Review the code of the **insertFile()** method of the **ERDocuManagement** class.</span></span> <span data-ttu-id="bd34e-137">Legg merke til at **AttachingFile()**-hendelsen starter når den genererte filen er knyttet til en post.</span><span class="sxs-lookup"><span data-stu-id="bd34e-137">Notice that the **AttachingFile()** event is raised while the generated file is attached to a record.</span></span>

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

<span data-ttu-id="bd34e-138">**AttachingFile()**-hendelsen oppstår når følgende ER-mål behandles:</span><span class="sxs-lookup"><span data-stu-id="bd34e-138">The **AttachingFile()** event is raised when the following ER destinations are processed:</span></span>

- <span data-ttu-id="bd34e-139">**Arkiv** – Når dette målet brukes, opprettes en ny post for ER-formatet som kjøres, i ERFormatMappingRunJobTable-tabellen.</span><span class="sxs-lookup"><span data-stu-id="bd34e-139">**Archive** – When this destination is used, a new record for the ER format that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="bd34e-140">**Arkivert**-feltet i denne oppføringen er satt til **Usann**.</span><span class="sxs-lookup"><span data-stu-id="bd34e-140">The **Archived** field in this record is set to **False**.</span></span> <span data-ttu-id="bd34e-141">Hvis kjøringen av ER-formatet er vellykket, knyttes det genererte dokumentet til denne posten, og **AttachingFile()**-hendelsen oppstår.</span><span class="sxs-lookup"><span data-stu-id="bd34e-141">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="bd34e-142">Dokumenttypen som velges i dette ER-målet, bestemmer lagringsstedet for den vedlagte filen (Microsoft Azure Storage eller en Microsoft SharePoint-mappe).</span><span class="sxs-lookup"><span data-stu-id="bd34e-142">The document type that is selected in this ER destination determines the storage location for the attached file (Microsoft Azure Storage or a Microsoft SharePoint folder).</span></span>
- <span data-ttu-id="bd34e-143">**Jobbarkiv** – Når dette målet brukes, opprettes en ny post for ER-skjemaet som kjøres, i ERFormatMappingRunJobTable-tabellen.</span><span class="sxs-lookup"><span data-stu-id="bd34e-143">**Job archive** – When this destination is used, a new record for the ER form that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="bd34e-144">**Arkivert**-feltet i denne oppføringen er satt til **Sann**.</span><span class="sxs-lookup"><span data-stu-id="bd34e-144">The **Archived** field in this record is set to **True**.</span></span> <span data-ttu-id="bd34e-145">Hvis kjøringen av ER-formatet er vellykket, knyttes det genererte dokumentet til denne posten, og **AttachingFile()**-hendelsen oppstår.</span><span class="sxs-lookup"><span data-stu-id="bd34e-145">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="bd34e-146">Dokumenttypen som konfigureres i ER-parameterne, bestemmer lagringsstedet for den vedlagte filen (Azure Storage eller en Microsoft SharePoint-mappe).</span><span class="sxs-lookup"><span data-stu-id="bd34e-146">The document type that is configured in the ER parameters determines the storage location for the attached file (Azure Storage or a SharePoint folder).</span></span>

![Siden Parametere for elektronisk rapportering](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a><span data-ttu-id="bd34e-148">Konfigurere et ER-mål</span><span class="sxs-lookup"><span data-stu-id="bd34e-148">Configure an ER destination</span></span>

1. <span data-ttu-id="bd34e-149">Konfigurer det arkiverte målet for et av de tidligere nevnte elementene (fil, mappe, sammenslåing eller vedlegg) for ER-formatet du opprettet eller importerte.</span><span class="sxs-lookup"><span data-stu-id="bd34e-149">Configure the archived destination for one of the previously mentioned elements (file, folder, merger, or attachment) of the ER format that you created or imported.</span></span> <span data-ttu-id="bd34e-150">For å få hjelp kan du se [ER Konfigurere mål](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span><span class="sxs-lookup"><span data-stu-id="bd34e-150">For guidance, see [ER Configure destinations](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span></span>
2. <span data-ttu-id="bd34e-151">Bruk dokumenttypen du la til tidligere for det konfigurerte målet.</span><span class="sxs-lookup"><span data-stu-id="bd34e-151">Use the document type that you added earlier for the configured destination.</span></span> <span data-ttu-id="bd34e-152">(For eksemplet i dette emnet er dokumenttypen **FileX**.)</span><span class="sxs-lookup"><span data-stu-id="bd34e-152">(For the example in this topic, the document type is **FileX**.)</span></span>

![Dialogboksen Innstillinger for mål](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a><span data-ttu-id="bd34e-154">Endre kildekode</span><span class="sxs-lookup"><span data-stu-id="bd34e-154">Modify source code</span></span>

1. <span data-ttu-id="bd34e-155">Legg til en ny klasse i Microsoft Visual Studio-prosjektet ditt, og skriv kode for å abonnere på **AttachingFile()**-hendelsen som ble nevnt tidligere.</span><span class="sxs-lookup"><span data-stu-id="bd34e-155">Add a new class to your Microsoft Visual Studio project, and write code to subscribe to the **AttachingFile()** event that was mentioned earlier.</span></span> <span data-ttu-id="bd34e-156">(Hvis du vil ha mer informasjon om utvidelsesmønsteret som brukes, se [Svare ved hjelp av EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) I den nye klassen kan du for eksempel skrive kode som utfører følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="bd34e-156">(For more information about the extensibility pattern that is used, see [Respond by using EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) For example, in the new class, write code that performs the following actions:</span></span>

    1. <span data-ttu-id="bd34e-157">Lagre genererte filer i en mappe i det lokale filsystemet på serveren som kjører tjenesten Application Object Server (AOS).</span><span class="sxs-lookup"><span data-stu-id="bd34e-157">Store generated files in a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    2. <span data-ttu-id="bd34e-158">Lagre disse genererte filene bare når den nye dokumenttypen (for eksempel **FileX**-typen med nøkkelordet "(LOKAL)" i navnet) brukes når en fil knyttes til posten i ER-kjøringsjobbloggen.</span><span class="sxs-lookup"><span data-stu-id="bd34e-158">Store these generated files only when the new document type (for example, the **FileX** type that has the "(LOCAL)" keyword in its name) is used while a file is attached to the record in the ER execution job log.</span></span>

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

2. <span data-ttu-id="bd34e-159">Bygg prosjektet på nytt.</span><span class="sxs-lookup"><span data-stu-id="bd34e-159">Rebuild your project.</span></span>

## <a name="run-the-er-format-that-you-created-or-imported"></a><span data-ttu-id="bd34e-160">Kjøre ER-formatet som du opprettet eller importerte</span><span class="sxs-lookup"><span data-stu-id="bd34e-160">Run the ER format that you created or imported</span></span>

1. <span data-ttu-id="bd34e-161">Kjør ER-formatet som du opprettet eller importerte.</span><span class="sxs-lookup"><span data-stu-id="bd34e-161">Execute the ER format that you created or imported.</span></span>
2. <span data-ttu-id="bd34e-162">Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Elektroniske rapporteringsjobber**.</span><span class="sxs-lookup"><span data-stu-id="bd34e-162">Go to **Organization administration \> Electronic reporting \> Electronic reporting jobs**.</span></span> <span data-ttu-id="bd34e-163">Finn posten som ble opprettet for denne kjøringsjobben, og som har den genererte filen tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="bd34e-163">Find the record that was created for this execution job, and that has the generated file attached to it.</span></span>
3. <span data-ttu-id="bd34e-164">Utforsk lokal **C:\\0**-mappen for å finne den samme genererte filen.</span><span class="sxs-lookup"><span data-stu-id="bd34e-164">Explore the local **C:\\0** folder to find same generated file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bd34e-165">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="bd34e-165">Additional resources</span></span>

- [<span data-ttu-id="bd34e-166">Mål for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="bd34e-166">Electronic reporting destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="bd34e-167">Startside med utvidelsesmuligheter</span><span class="sxs-lookup"><span data-stu-id="bd34e-167">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)
