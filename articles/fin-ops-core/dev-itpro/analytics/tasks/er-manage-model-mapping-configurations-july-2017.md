---
title: Administrere ER-modelltilordning i separate ER-konfigurasjoner
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet til rollen systemansvarlig eller utvikler av elektronisk rapportering, kan administrere modelltilordninger for elektronisk rapportering (ER) i separate ER-konfigurasjoner.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8ff3b419caafec626497c65ea18ca24ca95cb5d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143059"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a>Administrere ER-modelltilordning i separate ER-konfigurasjoner

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet til rollen systemansvarlig eller utvikler av elektronisk rapportering, kan administrere modelltilordninger for elektronisk rapportering (ER) i separate ER-konfigurasjoner. I denne oppgaveveiledningen skal du opprette nødvendige ER-konfigurasjoner for eksempelfirmaet, Litware, Inc. For å fullføre denne oppgaveveiledningen, må du først fullføre trinnene i oppgaveveiledningen, "Opprette en konfigurasjonsleverandør og merke den som aktiv." 

Fordi ER konfigurasjoner deles mellom firmaer, kan du fullføre oppgaveveiledningen ved hjelp av datasettet firmaet velger. Funksjonaliteten for denne oppgaveveiledningen er tilgjengelig hvis du har installert én av følgende hurtigreparasjoner: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for Dynamics AX 7.0-versjonen eller https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for Dynamics 365 for Operations-versjonen.

1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
    * Kontroller at konfigurasjonsleverandøren for eksempelfirmaET "Litware, Inc." er tilgjengelig og merket som aktiv. Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i oppgaveveilednignen "Opprette en konfigurasjonsleverandør og merke den som aktiv".   

## <a name="add-a-new-er-model-configuration"></a>Legg til en ny ER-konfigurasjon
1. Klikk Rapporteringskonfigurasjoner.
    * Legg til en ny modellkonfigurasjon. Navnet må være unikt i konfigurasjonstreet.  
2. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
3. Skriv inn Eksempeldatamodell i Navn-feltet.
    * Eksempel på datamodell  
4. Klikk Opprett konfigurasjon.
5. Klikk Utforming.
6. Klikk Ny for å åpne nedtrekksdialogen.
7. Skriv inn Rot i Navn-feltet.
    * Rot  
8. Klikk Legg til.
9. Klikk Ny for å åpne nedtrekksdialogen.
10. I Navn-feltet skriver du inn Firma.
    * Firma  
11. Klikk Legg til.
12. I Beskrivelse-feltet angir du teksten, beskrivelsen av den juridiske enheten eller firmaet der brukeren logget under kjøring. 
    * Beskrivelse av den juridiske enheten eller firmaet der brukeren logget under kjøring.  
13. Klikk Rotreferanse.
14. Klikk OK.
15. Klikk Lagre.
16. Lukk siden.
17. Klikk Endre status.
18. Klikk Fullført.
19. Klikk OK.

## <a name="add-a-new-er-model-mapping-configuration"></a>Legg til en ny ER-modelltilordningskonfigurasjon
1. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
2. I feltet Ny angir du Modeltilordning basert på datamodellen Eksempeldatamodell.
3. Skriv inn Eksempeltilordning i Navn-feltet.
    * Eksempeltilordning  
4. Klikk Opprett konfigurasjon.
5. Utvid seksjonen Forutsetninger.
    * Legg merke til at gruppen Forutsetninger for implementasjoner er lagt til automatisk. Gruppen inneholder den nødvendige komponenten som refererer til den overordnede data konfigurasjonen og merkes som implementering. Dette betyr at implementeringen av datamodellen, datamodellen for eksempel er lagt til konfigurasjon for tilordning av dette eksemplet tilordning. Derfor tvinger denne komponenten ER å laste ned konfigurasjonen for tilordning, eksempel på tilordning fra en database ER når konfigurasjonen av modellen, prøve datamodellen, lastes ned.   
6. Klikk Utforming.
    * Merk at konfigurasjonen for opprettede tilordningen inneholder en ny, tom tilordning med samme navn som opprettet konfigurasjonen. Vær oppmerksom på at når en konfigurasjon for valgte overordnede inneholder tilordninger av verdimodellen, vil de bli kopiert til en ny konfigurasjon for tilordning.   
7. Klikk Utforming.
8. Velg Dynamics 365 for Operations\Tabell i treet.
9. Klikk Legg til rot.
10. I Navn-feltet skriver du inn Firma.
    * Firma  
11. Skriv inn CompanyInfo i Tabell-feltet.
    * CompanyInfo  
12. Klikk OK.
13. Utvid 'Company' i treet.
14. Utvid 'Company\find()' i treet.
15. Velg 'Company\find()\Name' i treet.
16. Klikk Bind.
17. Klikk Lagre.
18. Lukk siden.
19. Lukk siden.
20. Klikk Konfigurasjoner i handlingsruten.
21. Klikk Brukerparametere.
22. Velg Ja i feltet Kjøringsinnstillinger.
23. Klikk OK.
24. Klikk Rediger.
25. Velg Ja i feltet Kjøringsutkast.

## <a name="add-a-new-er-format-configuration"></a>Legg til en ny ER-formatkonfigurasjon
1. Velg 'Sample data model' i treet.
2. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
3. I feltet Ny angir du Format basert på datamodellen Eksempeldatamodell.
4. Skriv inn Eksempelformat i Navn-feltet.
    * Eksempelformat  
5. Klikk Opprett konfigurasjon.
6. Klikk Utforming.
7. Klikk Legg til rot for å åpne nedtrekksdialogen.
8. Velg Tekst\Streng i treet.
9. Klikk OK.
10. Klikk kategorien Tilordning.
11. Utvid noden 'model' i treet.
12. Velg 'model\Company' i treet.
13. Klikk Bind.
14. Klikk Lagre.
15. Lukk siden.
    * Kjør utkastversjonen av formatet som er opprettet for testformål.  
16. Klikk Kjør.
    * Klikk Kjør på hurtigfanen Versjoner.  
17. Klikk OK.
    * Gå gjennom utdataene som inneholder navnet på firmaet der brukeren som kjører denne formatkonfigurasjonen er logget på. Legg merke til at den opprettede tilordningen konfigurasjonen brukes av denne formatkonfigurasjonen fordi bare én tilgjengelig konfigurasjon som inneholder tilordninger av nødvendige modellen.   

## <a name="add-alternative-er-model-mapping-configuration"></a>Legg til en alternativ ER-modelltilordningskonfigurasjon
1. Velg 'Sample data model' i treet.
2. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
3. I feltet Ny angir du Modeltilordning basert på datamodellen Eksempeldatamodell.
4. Skriv inn Eksempel på tilordning (alternativ) i Navn-feltet.
    * Eksempel på tilordning (alternativ)  
5. Klikk Opprett konfigurasjon.
6. Klikk Utforming.
7. Klikk Utforming.
8. Velg Dynamics 365 for Operations\Tabell i treet.
9. Klikk Legg til rot.
10. I Navn-feltet skriver du inn Firma.
    * Firma  
11. Skriv inn CompanyInfo i Tabell-feltet.
    * CompanyInfo  
12. Klikk OK.
13. Klikk Rediger.
14. I treet velger du Streng\CONCATENATE.
15. Klikk Legg til funksjon.
16. Utvid 'Company' i treet.
17. Utvid 'Company\find()' i treet.
18. Velg 'Company\find()\Name' i treet.
19. Klikk Legg til datakilde.
20. Skriv inn en verdi i feltet Formel.
    * CONCATENATE(Company.'find()'.Name, ";",  
21. Velg 'Company\find()\Company(DataArea)' i treet.
22. Klikk Legg til datakilde.
23. Skriv inn en verdi i feltet Formel.
    * CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)  
24. Klikk Lagre.
25. Lukk siden.
26. Klikk Lagre.
27. Lukk siden.
28. Lukk siden.
29. Velg Ja i feltet Kjøringsutkast.

## <a name="use-an-existing-er-model-mapping-configuration"></a>Bruk en eksisterende ER-modelltilordningskonfigurasjon
1. Velg 'Sample data model\Sample format' i treet.
2. Klikk Kjør.
    * Vær oppmerksom på at den valgte utkastversjonen av formatkonfigurasjonen ER ikke kan utføres fordi det er mer enn én konfigurasjon for tilordning for den udefinerte datamodellen som er valgt som datakilden for det kjørende ER-formatet.   
    * Nå vil du definere tilordning av alternativ konfigurasjon som fra hvilken modell tilordningene brukes som datakilder ER formateringen.   
3. Velg 'Sample data model\Sample mapping (alternative)' i treet.
4. Velg Ja i feltet Standard for modelltilordning.
5. Velg 'Sample data model\Sample format' i treet.
6. Klikk Kjør.
7. Klikk OK.
    * Legg merke til at den standard tilordning konfigurasjonen brukes av denne formatkonfigurasjonen for generering av det elektroniske dokumentet (opprettet utdataene inneholder firmakoden).  

