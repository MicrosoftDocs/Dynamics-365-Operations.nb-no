--- 
title: "Utforme ER-konfigurasjoner for å generere rapporter i Word-format"
description: "De følgende trinnene forklarer hvordan en bruker med rollen systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapporteringsformat til å generere rapporter som Microsoft Word-filer."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: dc47d44285af4c720d2f450d11fb1004ef461d0f
ms.contentlocale: nb-no
ms.lasthandoff: 10/16/2018

---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a>Utforme ER-konfigurasjoner for å generere rapporter i Word-format

[!include [task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker med rollen systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å generere rapporter som Microsoft-filer. Denne fremgangsmåten kan utføres i firmaet GBSI.

For å fullføre disse trinnene må du først fullføre trinnene i oppgaveveiledningen "Opprette en ER-konfigurasjon for generering av rapporter i OPENXML-format". På forhånd, må du også laste ned og lagre følgende maler lokalt, for eksempelrapporten:

- [Mal for betalingsrapport](https://go.microsoft.com/fwlink/?linkid=862266)
- [Bundet mal for betalingsrapport](https://go.microsoft.com/fwlink/?linkid=862266)


Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Microsoft Dynamics 365 for Operations, versjon 1611.


## <a name="select-the-existing-er-report-configuration"></a>Velg den eksisterende ER-rapportkonfigurasjonen
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
    * Kontroller at konfigurasjonsleverandøren Litware, Inc er merket som aktiv.  
2. Klikk Rapporteringskonfigurasjoner.
    * Vi vil bruke den eksisterende ER-konfigurasjonen som er opprinnelig utformet for å generere rapportutdataene i OPENXML-formatet, på nytt.  
3. Utvid Betalingsmodell i treet.
4. Velg Betalingsmodell\Regnearkeksempelrapport i treet.
5. Klikk Utforming.

## <a name="replace-the-excel-template-with-the-word-template"></a>Erstatt Excel-malen med Word-malen
    * For øyeblikket brukes Excel-dokumentet som en mal til å generere utdataene i OPENXML-format. Vi vil importere rapportens mal i Word-format.  
1. Klikk Vedlegg.
    * Erstatt den eksisterende Excel-malen med Word-malen som du lastet ned tidligere, SampleVendPaymDocReport.docx. Legg merke til at denne malen bare inneholder oppsettet for dokumentet vi vil generere som ER-utdata.  
2. Klikk Slett.
3. Klikk Ja.
4. Klikk Ny.
5. Klikk Fil.
6. Klikk Bla gjennom. Gå til og velg SampleVendPaymDocReport.docx som du lastet ned tidligere. Klikk OK.
    * Velg malen du lastet ned i den forrige fremgangsmåten.  
7. Angi eller velg en verdi i feltet Mal.

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>Utvid Word-malen ved å legge til en egendefinert XML-del
1. Klikk Lagre.
    * I tillegg til å lagre konfigurasjonsendringer, oppdaterer Lagre-handlingen den vedlagte Word-malen. Strukturen til det utformede formatet er overført til det vedlagte Word-dokumentet som en ny egendefinert XML-del med navnet "Rapport". Legg merke til at den tilknyttede Word-malen ikke bare inneholder oppsettet for dokumentet vi vil generere som ER-utdata, den inneholder også strukturen til dataene som ER fyller ut i denne malen under kjøring.  
2. Klikk Vedlegg.
    * Nå må du binde elementene i den egendefinerte XML-delen "Rapport" til deler på Word-dokumentet.  
    * Hvis du har kjennskap til Word-dokumenter som kan utformes som skjemaer som inneholder innholdskontroller som er avgrenset med elementer av egendefinerte XML-deler – spill av alle trinnene i den neste delaktiviteten for å opprette et slikt dokument. Hvis du vil ha mer informasjon, følg koblingen https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US. Hvis ikke hopper du over alle trinnene i den neste delaktiviteten.  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>Få Word med egendefinert XML-delen for å utføre databindinger
    * Åpne dette dokumentet i Word, og gjør følgende: – Åpne fanen Word-utvikler (tilpass båndet hvis det ikke er aktivert ennå).  - Velg ruten XML-tilordning.  - Velg den egendefinerte XML-delen "Rapport" i oppslaget.  - Utfør tilordning av elementene i den valgte egendefinerte XML-delen og innholdskontrollene for Word-dokumentet.  - Lagre det oppdaterte Word-dokumentet på en lokal stasjon.  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>Last opp Word-malen med egendefinert XML-del bundet til innholdskontroller
1. Klikk Slett.
2. Klikk Ja.
    * Legg til ny mal. Hvis du har fullført trinnene i den forrige delaktiviteten, velger du Word-dokumentet du opprettet og lagret lokalt. Ellers velger du Microsoft Word-malen SampleVendPaymDocReportBounded.docx som du lastet ned tidligere.  
3. Klikk Ny.
4. Klikk Fil.
5. Klikk Bla gjennom. Gå til og velg SampleVendPaymDocReportBounded.docx som du lastet ned tidligere. Klikk OK.
6. I Mal-feltet velger du dokumentet du lastet ned i den forrige fremgangsmåten.
7. Klikk Lagre.
8. Lukk siden.

## <a name="execute-the-format-to-create-word-output"></a>Kjør formatet for å opprette Word-utdata
1. Klikk Konfigurasjoner i handlingsruten.
2. Klikk Brukerparametere.
3. Velg Ja i feltet Kjøringsinnstillinger.
4. Klikk OK.
5. Klikk Rediger.
6. Velg Ja i feltet Kjøringsutkast.
7. Klikk Lagre.
8. Lukk siden.
9. Lukk siden.
10. Gå til Leverandører > Betalinger > Betalingsjournal.
11. Klikk Linjer.
12. Merk eller fjern merking for alle rader i listen.
13. Klikk Betalingsstatus.
14. Velg Ingen.
15. Klikk Generer betalinger.
16. Klikk OK.
17. Klikk OK.
    * Analyser de genererte utdataene. Legg merke til at de opprettede utdataene vises i Word-format og inneholder detaljer for de behandlede betalingene.  


