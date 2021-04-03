---
title: Importere filer i XML-format med valgfrie attributter
description: Dette emnet inneholder informasjon om utforming av ER-formater som angir XML-attributter for å analysere innkommende elektroniske dokumenter i XML-format.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 399f19197a729c11eaff94d708c837caef0d366d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562958"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a>Importere filer i XML-format med valgfrie attributter

[!include [banner](../includes/banner.md)]

Du kan utforme ER-formater (elektronisk rapportering) for å analysere innkommende elektroniske dokumenter i XML-format. Visse attributter i XML-elementer kan angis som valgfrie i et utformet ER-format. Dette gjør at du kan håndtere innkommende filer med og uten slike XML-attributter på riktig måte. Du kan deretter bruke innholdet fra disse filene til å oppdatere programdata.

Hvis du vil ha mer informasjon om denne funksjonen, fullfører du trinnene i emnet [(RCS) Importere filer i XML-format med valgfrie attributter](tasks/import-files-xml-format-optional-attributes.md), som er en del av forretningsprosessen 7.5.4.3 Acquire/Develop IT service/solution components (10677). Du kan laste ned denne oppgaveveiledningen og de tilknyttede eksempelfilene fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).


| Innholdsbeskrivelse       | Fil                                                         |
|---------------------------|--------------------------------------------------------------|
| Eksempelfil i XML-format | IncomingDocumentToLearnHowToHandleOptionalAttributes.xml     |
| Oppgaveveiledning                | RCS Import files in XML format with optional attributes.axtr |


Fremgangsmåten nedenfor forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan utforme en ER-formatkonfigurasjon for å importere filer i XML-format som inneholder valgfrie attributter. For å fullføre disse trinnene må du først fullføre trinnene i prosedyren [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md). Før du begynner, laster du ned filen IncomingDocumentToLearnHowToHandleOptionalAttributes.xml fra Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ) og lagrer den lokalt.

1. Gå til **Organisasjonsstyring** > **Arbeidsområder** > **Elektronisk rapportering**.
2. Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**. Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i emnet [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Klikk på **Rapporteringskonfigurasjoner**.

## <a name="create-a-new-data-model-configuration"></a>Opprett en ny datamodellkonfigurasjon
1. Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen.
2. Skriv inn «Modell for å importere XML-fil» i **Navn**-feltet.
3. Klikk **Opprett konfigurasjon**.
4. Klikk **Utforming**.
5. Klikk på **Ny** for å åpne nedtrekksdialogen.
6. Skriv inn «Rot» i **Navn**-feltet.
7. Klikk **Legg til**.
8. Klikk på **Ny** for å åpne nedtrekksdialogen.
9. Skriv inn «Liste» i **Navn**-feltet.
10.    Velg **Postliste** i **Varetype**-feltet.
11.    Klikk **Legg til**.
12.    Klikk på **Ny** for å åpne nedtrekksdialogen.
13.    I **Navn**-feltet skriver du inn «Kode».
14.    Velg **Streng** i **Varetype**-feltet.
15.    Klikk **Legg til**.
16.    Klikk **Lagre**.
17.    Lukk siden.
18.    Klikk på **Endre status**.
19.    Klikk på **Fullført**.
20.    Klikk **OK**.

## <a name="create-a-format-for-data-import"></a>Opprette et format for dataimport
1. Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen.
2. I **Ny**-feltet angir du «Format basert på datamodellen Modell for å importere XML-fil».
3. Skriv inn «Format for å importere XML-fil» i **Navn**-feltet. 
4. Velg **Ja** i feltet **Støtter dataimport**.
5. Klikk **Opprett konfigurasjon**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Utforme et format for å analysere innkommende fil i XML-format
1. Klikk **Utforming**.
2. Klikk på **Legg til rot** for å åpne nedtrekksdialogen.
3. Velg **XML\Element** i treet.
4. Skriv inn «rot» i **Navn**-feltet.
5. Klikk **OK**.
6. Klikk på **Legg til** for å åpne nedtrekksdialogen.
7. Velg **XML\Element** i treet.
8. I **Navn**-feltet skriver du inn «dokument».
9. Velg **Én mange** i feltet **Multiplisitet**.
10.    Klikk **OK**.
11.    Velg **rot\dokument** i treet.
12.    Klikk på **Legg til** for å åpne nedtrekksdialogen.
13.    Velg **XML\Attributt** i treet.
14.    I **Navn**-feltet skriver du inn «id».
15.    Klikk **OK**.
16.    Klikk **Lagre**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Utforme en formattilordning for å lagre analysert informasjon i datamodell
1.    Klikk på **Tilordne format til modell**.
2.    Klikk på **Ny**.
3.    Angi eller velg en verdi i feltet **Definisjon**.
4.    I **Navn**-feltet skriver du inn «Tilordning».
5.    Klikk **Lagre**.
6.    Klikk **Utforming**.
7.    Utvid **format** i treet.
8.    I treet utvider du **format\rot: XML-element(rot)**.
9.    I treet velger du **format\root: XML-element(rot)\dokument: XML-element 1..* (dokument)**.
10.    Klikk på **Bind**.
11.    I treet utvider du **format\rot: XML-element(rot)\dokument: XML-element 1..* (dokument)**.
12.    I treet velger du **format\root: XML-element(rot)\dokument: XML-element 1..* (dokument)\id**.
13.    I treet utvider du **Liste = format.rot.dokument**.
14.    I treet velger du **Liste = format.rot.dokument\Kode**.
15.    Klikk på **Bind**.
16.    Klikk **Lagre**.
17.    Lukk siden.

## <a name="run-format-mapping"></a>Kjøre formattilordning
1. Klikk på **Kjør**.
2. Klikk på **Bla gjennom**, og velg filen **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
3. Klikk **OK**.

> [!NOTE]
> Den valgte filen er ikke importert, siden formatutformingen forutsetter at et «id»-attributt finnes for «dokument»-elementet, men den importerte filen inneholder ikke noe slikt attributt.

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>Endre formatstrukturen for å håndtere XML-attributter som valgfrie
1. Lukk siden.
2. Utvid **rot\dokument** i treet.
3. Velg **rot\dokument\id** i treet.
4. Velg **Ja** i feltet **Tom streng for manglende attributt**.
5. Klikk **Lagre**.

## <a name="run-format-mapping-to-test-changes"></a>Kjøre formattilordning for å teste endringer
1. Klikk på **Tilordne format til modell**.
2. Klikk på **Kjør**.
3. Klikk på **Bla gjennom**, og velg filen **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
4. Klikk **OK**.
5. Se gjennom den genererte filen. Vær oppmerksom på at samme fil har blitt importert, siden formatutformingen nå regner «id»-attributtet for «dokument»-elementet for å være valgfritt.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]