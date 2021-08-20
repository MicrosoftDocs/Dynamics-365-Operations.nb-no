---
title: Generere rapporter i Office-formater som inneholder innebygde bilder
description: Dette emnet beskriver hvordan du utformer konfigurasjoner for elektronisk rapportering (ER) for å generere elektroniske dokumenter i Excel og Word som inneholder innebygde bilder.
author: NickSelin
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ec9f3013c1e365a3ca1a4c6cabe71a22e3e8b730eac38155ef023fe68107524
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735532"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a>Generere rapporter i Office-formater som inneholder innebygde bilder

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan designe konfigurasjoner for elektronisk rapportering (ER) for å generere elektroniske dokumenter i MS Office-formater (Excel og Word), som inneholder innebygde bilder.

I dette eksemplet skal du bruke opprettede ER-konfigurasjoner for eksempelfirmaet "Litware, Inc".  For å fullføre disse trinnene, må du først fullføre trinnene i oppgaveveiledningen "ER lage rapporter i MS Office-formater med innebygde bilder (del 2: se gjennom konfigurasjoner)". Denne fremgangsmåten kan utføres i USMF-firmaet.


## <a name="run-format-with-initial-model-mapping"></a>Kjøre format med tilordning av opprinnelig modell
1. Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.
2. Bruk hurtigfilteret til å filtrere på Bankkonto-feltet med en verdi lik USMF OPER.
3. Klikk på Oppsett i handlingsruten.
4. Klikk på Kontroller.
5. Klikk på Skriv ut test.
    * Kjør formatet for testformål.  
6. Velg Ja i feltet Sjekkformat som kan forhandles.
7. Klikk på OK.
    * Se gjennom de opprettede utdataene. Firmalogoen vises i rapporten, i tillegg til autoriserte personens signatur. Signaturbildet hentes fra feltet av typen "Beholder" for Sjekk oppsett-posten som er tilknyttet den valgte bankkontoen.  
8. Utvid Kopier-seksjonen.
9. Klikk på Rediger.
10. Angi "Skriv ut vannmerke som Annuller" i feltet Vannmerker.
    * Endre innstillingen vannmerker oppsett til å vise vannmerketeksten i dokumentgenerering i et Excel-figur-element.  
11. Klikk på Skriv ut test.
12. Klikk på OK.
    * Se gjennom de opprettede utdataene. Vannmerket vises i den opprettede rapporten i henhold til det valgte alternativet.  
13. Lukk siden.
14. Klikk på Administrer betalinger i handlingsruten.
15. Klikk på Kontroller.
16. Klikk på Vis filtre.
17. Bruk følgende filtre: Angi en filterverdi på "381","385","389" i feltet "Sjekknummer" ved hjelp av filteroperatoren "er en av".
18. Merk alle rader i listen.
19. Klikk på Skriv ut kopi av sjekk.
    * Kjør formatet for å skrive ut de valgte sjekkene på nytt.  
    * Se gjennom de opprettede utdataene. De valgte sjekkene er skrevet ut på nytt. Firmalogoen og etiketter skrives ikke etter at de vises i fortrykte skjemaet.  

## <a name="modify-the-mapping-of-the-imported-data-model"></a>Endre tilordningen av den importerte datamodellen
1. Lukk siden.
2. Lukk siden.
3. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
4. Velg Modell for sjekker i treet.
5. Klikk på Utforming.
6. Klikk på Tilordne modell til datakilde.
7. Klikk på Utforming.
    * Vi vil endre bindingen av datamodellens signaturelement for å få signaturbildet fra filen som er knyttet til posten Sjekk oppsett som er tilknyttet den valgte bankkontoen.  
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
18. Klikk på Bind.
19. Klikk på Lagre.
20. Lukk siden.
21. Lukk siden.
22. Lukk siden.
23. Lukk siden.

## <a name="run-format-using-the-adjusted-model-mapping"></a>Kjøre format ved hjelp av justert modelltilordning
1. Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.
2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Bankkonto-feltet med verdien 'USMF OPER'.
3. Klikk på Oppsett i handlingsruten.
4. Klikk på Kontroller.
5. Klikk på Skriv ut test.
6. Klikk på OK.
    * Se gjennom de opprettede utdataene. Bildet fra dokumentbehandlingsvedlegget vises som signaturen til en autorisert person.  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a>Bruk MS Word-dokument som en mal i det importerte formatet
1. Lukk siden.
2. Lukk siden.
3. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
4. Utvid Modell for sjekker i treet.
5. Velg 'Modell for sjekker\Utskriftsformat for sjekker' i treet.
6. Klikk på Utforming.
7. Klikk på Vedlegg.
8. Klikk på Slett.
9. Klikk på Ja.
10. Klikk på Ny.
11. Klikk på Fil.
    * Klikk Bla gjennom og velg den nedlastede på forhånd "Sjekk Word.docx-malfil.  
12. Lukk siden.
13. Angi eller velg en verdi i feltet Mal.
14. Klikk på Lagre.
15. Lukk siden.
16. Klikk på Rediger.
17. Velg Ja i feltet Kjøringsutkast.
18. Lukk siden.
19. Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.
20. Bruk hurtigfilteret til å filtrere på Bankkonto-feltet med en verdi lik USMF OPER.
21. Klikk på Kontroller.
22. Klikk på Skriv ut test.
23. Klikk på OK.
    * Se gjennom de opprettede utdataene. Utdataene er generert som et Word-dokument med innebygde bilder som presenterer firmalogoen, signaturen til en autorisert person og den valgte teksten til vannmerket.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]