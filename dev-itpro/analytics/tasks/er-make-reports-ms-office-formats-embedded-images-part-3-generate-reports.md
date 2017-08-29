--- 
title: Generere rapporter i Microsoft Office-formater med innebygde bilder for elektronisk rapportering (ER)
description: "De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan designe konfigurasjoner for elektronisk rapportering (ER) for å generere av elektroniske dokumenter i MS Office-formater (Excel og Word), som inneholder innebygde bilder."
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4576d89923926971ab3ca30dc702baedf05f602a
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="generate-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er"></a>Generere rapporter i Microsoft Office-formater med innebygde bilder for elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan designe konfigurasjoner for elektronisk rapportering (ER) for å generere av elektroniske dokumenter i MS Office-formater (Excel og Word), som inneholder innebygde bilder.

I dette eksemplet skal du bruke opprettede ER-konfigurasjoner for eksempelfirmaet "Litware, Inc".  For å fullføre disse trinnene, må du først fullføre trinnene i oppgaveveiledningen "ER lage rapporter i MS Office-formater med innebygde bilder (del 2: se gjennom konfigurasjoner)". Denne fremgangsmåten kan utføres i USMF-firmaet.


## <a name="run-format-with-initial-model-mapping"></a>Kjøre format med tilordning av opprinnelig modell
1. Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.
2. Bruk hurtigfilteret til å filtrere på Bankkonto-feltet med en verdi lik USMF OPER.
3. Klikk Oppsett i handlingsruten.
4. Klikk Kontroller.
5. Klikk Skriv ut test.
    * Kjør formatet for testformål.  
6. Velg Ja i feltet Sjekkformat som kan forhandles.
7. Klikk OK.
    * Se gjennom de opprettede utdataene. Legg merke til at firmalogoen skal vises i rapporten, i tillegg til autoriserte personens signatur. Signaturbilde av hentes fra feltet av typen "Beholder" for Sjekk oppsett posten som er tilknyttet den valgte bankkontoen.  
8. Utvid Kopier-seksjonen.
9. Klikk Rediger.
10. Angi "Skriv ut vannmerke som Annuller" i feltet Vannmerker.
    * Endre innstillingen vannmerker oppsett til å vise vannmerketeksten i dokumentgenerering i et Excel-figur-element.  
11. Klikk Skriv ut test.
12. Klikk OK.
    * Se gjennom de opprettede utdataene. Legg merke til at vannmerket vises i rapporten er opprettet i henhold til alternativet merket område.  
13. Lukk siden.
14. Klikk Administrer betalinger i handlingsruten.
15. Klikk Kontroller.
16. Klikk Vis filtre.
17. Bruk følgende filtre: Angi en filterverdi på "381","385","389" i feltet "Sjekknummer" ved hjelp av filteroperatoren "er en av".
18. Merk alle rader i listen.
19. Klikk Skriv ut kopi av sjekk.
    * Kjør formatet for å skrive ut de valgte sjekkene.  
    * Se gjennom de opprettede utdataene. Legg merke til at de valgte sjekkene er skrevet ut på nytt. Firmalogoen og etiketter skrives ikke etter at de vises i fortrykte skjemaet.  

## <a name="modify-the-mapping-of-the-imported-data-model"></a>Endre tilordningen av den importerte datamodellen
1. Lukk siden.
2. Lukk siden.
3. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
4. Velg Modell for sjekker i treet.
5. Klikk Utforming.
6. Klikk Tilordne modell til datakilde.
7. Klikk Utforming.
    * Vi vil endre bindingen av-datamodellen signatur vare for å få signaturen bildet fra filen som er knyttet til posten sjekk oppsett som er tilknyttet den valgte bankkontoen.  
8. Deaktiver Vis detaljer.
9. Utvid "oppsett" i treet.
10. Utvid "oppsett\signatur" i treet.
11. I treet velger du 'oppsett\signature\bilde = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.
12. Vis 'chequesaccount' i treet.
13. Utvid 'chequesaccount\<Relations' i treet.
14. Utvid 'chequesaccount\<RelationsBankChequeLayout' i treet.
15. Utvid 'chequesaccount\<RelationsBankChequeLayout\<Relations' i treet.
16. Utvid 'chequesaccount\<RelationsBankChequeLayout\<Relations\<Documents' i treet.
17. Velg 'chequesaccount\<RelationsBankChequeLayout\<Relations\<DocumentsgetFileContentAsContainer()' i treet.
18. Klikk Bind.
19. Klikk Lagre.
20. Lukk siden.
21. Lukk siden.
22. Lukk siden.
23. Lukk siden.

## <a name="run-format-using-the-adjusted-model-mapping"></a>Kjøre format ved hjelp av justert modelltilordning
1. Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.
2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Bankkonto-feltet med verdien 'USMF OPER'.
3. Klikk Oppsett i handlingsruten.
4. Klikk Kontroller.
5. Klikk Skriv ut test.
6. Klikk OK.
    * Se gjennom de opprettede utdataene. Legg merke til at bildet fra dokumentbehandling vedlegget vises som signaturen for en autorisert person.  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a>Bruk Microsoft Word-dokument som en mal i det importerte formatet
1. Lukk siden.
2. Lukk siden.
3. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
4. Utvid Modell for sjekker i treet.
5. Velg 'Modell for sjekker\Utskriftsformat for sjekker' i treet.
6. Klikk Utforming.
7. Klikk Vedlegg.
8. Klikk Slett.
9. Klikk Ja.
10. Klikk Ny.
11. Klikk Fil.
    * Klikk Bla gjennom og velg den nedlastede på forhånd "sjekk Word.docx-malfil.  
12. Lukk siden.
13. Angi eller velg en verdi i feltet Mal.
14. Klikk Lagre.
15. Lukk siden.
16. Klikk Rediger.
17. Velg Ja i feltet Kjøringsutkast.
18. Lukk siden.
19. Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.
20. Bruk hurtigfilteret til å filtrere på Bankkonto-feltet med en verdi lik USMF OPER.
21. Klikk Kontroller.
22. Klikk Skriv ut test.
23. Klikk OK.
    * Se gjennom de opprettede utdataene. Legg merke til at utdataene er generert som et Microsoft Word-dokument med innebygde bilder presenterer firmalogoen, signaturen til en autorisert person og den merkede teksten til vannmerket.  


