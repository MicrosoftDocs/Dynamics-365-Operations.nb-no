---
title: Administrere ER-modelltilordning i separate ER-konfigurasjoner
description: Dette emnet beskriver hvordan du administrerer ER-modelltilordninger (Elektronisk rapportering) i separate ER-konfigurasjoner.
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf4896bec7aa68cc6616756ef07c4db95e20a5cf7ebde3102f482cd5abad1420
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776054"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a>Administrere ER-modelltilordning i separate ER-konfigurasjoner

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet til rollen systemansvarlig eller utvikler av elektronisk rapportering, kan administrere modelltilordninger for elektronisk rapportering (ER) i separate ER-konfigurasjoner. I denne oppgaveveiledningen skal du opprette nødvendige ER-konfigurasjoner for eksempelfirmaet, Litware, Inc. For å fullføre denne oppgaveveiledningen, må du først fullføre trinnene i oppgaveveiledningen, "Opprette en konfigurasjonsleverandør og merke den som aktiv." 

Fordi ER konfigurasjoner deles mellom firmaer, kan du fullføre oppgaveveiledningen ved hjelp av datasettet firmaet velger. Funksjonaliteten for denne oppgaveveiledningen er tilgjengelig hvis du har installert én av følgende hurtigreparasjoner: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for Dynamics AX 7.0-versjonen eller https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for Dynamics 365 for Operations-versjonen.

1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
    * Kontroller at konfigurasjonsleverandøren for eksempelfirmaET "Litware, Inc." er tilgjengelig og merket som aktiv. Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i oppgaveveilednignen "Opprette en konfigurasjonsleverandør og merke den som aktiv".   

## <a name="add-a-new-er-model-configuration"></a>Legg til en ny ER-konfigurasjon
1. Klikk på Rapporteringskonfigurasjoner.
    * Legg til en ny modellkonfigurasjon. Navnet må være unikt i konfigurasjonstreet.  
2. Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.
3. Skriv inn Eksempeldatamodell i Navn-feltet.
    * Eksempel på datamodell  
4. Klikk på Opprett konfigurasjon.
5. Klikk på Utforming.
6. Klikk på Ny for å åpne nedtrekksdialogen.
7. Skriv inn Rot i Navn-feltet.
    * Rot  
8. Klikk på Legg til.
9. Klikk på Ny for å åpne nedtrekksdialogen.
10. I Navn-feltet skriver du inn Firma.
    * Firma  
11. Klikk på Legg til.
12. I Beskrivelse-feltet angir du teksten, beskrivelsen av den juridiske enheten eller firmaet der brukeren logget under kjøring. 
    * Beskrivelse av den juridiske enheten eller firmaet der brukeren logget under kjøring.  
13. Klikk på Rotreferanse.
14. Klikk på OK.
15. Klikk på Lagre.
16. Lukk siden.
17. Klikk på Endre status.
18. Klikk på Fullført.
19. Klikk på OK.

## <a name="add-a-new-er-model-mapping-configuration"></a>Legg til en ny ER-modelltilordningskonfigurasjon
1. Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.
2. I feltet Ny angir du Modeltilordning basert på datamodellen Eksempeldatamodell.
3. Skriv inn Eksempeltilordning i Navn-feltet.
    * Eksempeltilordning  
4. Klikk på Opprett konfigurasjon.
5. Utvid seksjonen Forutsetninger.
    * Gruppen Forutsetninger for implementasjoner er lagt til automatisk. Gruppen inneholder den nødvendige komponenten som refererer til den overordnede data konfigurasjonen og merkes som implementering. Dette betyr at denne modelltilordningskonfigurasjonen for eksempeltilordning betraktes som implementering av datamodellen Eksempeldatamodell. Derfor tvinger denne komponenten ER å laste ned modelltilordningskonfigurasjon for eksempeltilordning fra et ER-repositorium når modellkonfigurasjonen for eksempeldatamodellen lastes ned.   
6. Klikk på Utforming.
    * Den opprettede modelltilordningskonfigurasjonen inneholder en ny, tom tilordning med samme navn som den opprettet konfigurasjonen. Når en valgt overordnet modellkonfigurasjon inneholder modelltilordninger, vil de bli kopiert til en ny modelltilordningskonfigurasjon.   
7. Klikk på Utforming.
8. Velg Dynamics 365 for Operations\Tabell i treet.
9. Klikk på Legg til rot.
10. I Navn-feltet skriver du inn Firma.
    * Firma  
11. Skriv inn CompanyInfo i Tabell-feltet.
    * CompanyInfo  
12. Klikk på OK.
13. Utvid 'Company' i treet.
14. Utvid 'Company\find()' i treet.
15. Velg 'Company\find()\Name' i treet.
16. Klikk på Bind.
17. Klikk på Lagre.
18. Lukk siden.
19. Lukk siden.
20. Klikk på Konfigurasjoner i handlingsruten.
21. Klikk på Brukerparametere.
22. Velg Ja i feltet Kjøringsinnstillinger.
23. Klikk på OK.
24. Klikk på Rediger.
25. Velg Ja i feltet Kjøringsutkast.

## <a name="add-a-new-er-format-configuration"></a>Legg til en ny ER-formatkonfigurasjon
1. Velg 'Sample data model' i treet.
2. Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.
3. I feltet Ny angir du Format basert på datamodellen Eksempeldatamodell.
4. Skriv inn Eksempelformat i Navn-feltet.
    * Eksempelformat  
5. Klikk på Opprett konfigurasjon.
6. Klikk på Utforming.
7. Klikk på Legg til rot for å åpne nedtrekksdialogen.
8. Velg Tekst\Streng i treet.
9. Klikk på OK.
10. Klikk på fanen Tilordning.
11. Utvid noden 'model' i treet.
12. Velg 'model\Company' i treet.
13. Klikk på Bind.
14. Klikk på Lagre.
15. Lukk siden.
    * Kjør utkastversjonen av formatet som er opprettet for testformål.  
16. Klikk på Kjør.
    * Klikk Kjør på hurtigfanen Versjoner.  
17. Klikk på OK.
    * Gå gjennom utdataene som inneholder navnet på firmaet der brukeren som kjører denne formatkonfigurasjonen er logget på. Den opprettede modelltilordningskonfigurasjonen brukes av denne formatkonfigurasjonen fordi det bare er én tilgjengelig konfigurasjon som inneholder nødvendige modelltilordninger.   

## <a name="add-alternative-er-model-mapping-configuration"></a>Legg til alternativ ER-modelltilordningskonfigurasjon
1. Velg 'Sample data model' i treet.
2. Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.
3. I feltet Ny angir du Modeltilordning basert på datamodellen Eksempeldatamodell.
4. Skriv inn Eksempel på tilordning (alternativ) i Navn-feltet.
    * Eksempel på tilordning (alternativ)  
5. Klikk på Opprett konfigurasjon.
6. Klikk på Utforming.
7. Klikk på Utforming.
8. Velg Dynamics 365 for Operations\Tabell i treet.
9. Klikk på Legg til rot.
10. I Navn-feltet skriver du inn Firma.
    * Firma  
11. Skriv inn CompanyInfo i Tabell-feltet.
    * CompanyInfo  
12. Klikk på OK.
13. Klikk på Rediger.
14. I treet velger du Streng\CONCATENATE.
15. Klikk på Legg til funksjon.
16. Utvid 'Company' i treet.
17. Utvid 'Company\find()' i treet.
18. Velg 'Company\find()\Name' i treet.
19. Klikk på Legg til datakilde.
20. Skriv inn en verdi i feltet Formel.
    * CONCATENATE(Company.'find()'.Name, ";",  
21. Velg 'Company\find()\Company(DataArea)' i treet.
22. Klikk på Legg til datakilde.
23. Skriv inn en verdi i feltet Formel.
    * CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)  
24. Klikk på Lagre.
25. Lukk siden.
26. Klikk på Lagre.
27. Lukk siden.
28. Lukk siden.
29. Velg Ja i feltet Kjøringsutkast.

## <a name="use-an-existing-er-model-mapping-configuration"></a>Bruk en eksisterende ER-modelltilordningskonfigurasjon
1. Velg 'Sample data model\Sample format' i treet.
2. Klikk på Kjør.
    * Den valgte utkastversjonen av ER-formatkonfigurasjonen ikke kan utføres, fordi det er mer enn én tilgjengelig modelltilordningskonfigurasjon for den udefinerte datamodellen som er valgt som datakilden for det kjørende ER-formatet.   
    * Nå skal du definere den alternative modelltilordningskonfigurasjonen som den som modelltilordningene skal brukes fra som datakilder for det kjørende ER-formatet.   
3. Velg 'Sample data model\Sample mapping (alternative)' i treet.
4. Velg Ja i feltet Standard for modelltilordning.
5. Velg 'Sample data model\Sample format' i treet.
6. Klikk på Kjør.
7. Klikk på OK.
    * Standard modelltilordningskonfigurasjon brukes av denne formatkonfigurasjonen for generering av det elektroniske dokumentet (opprettede utdata inneholder firmakoden).  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]