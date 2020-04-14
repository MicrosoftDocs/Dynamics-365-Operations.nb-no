---
title: Endre modeller og tilordninger for å generere dokumenter med programdata
description: 'For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren "ER generere dokumenter med oppdatering av programdata (del 2: generere dokumenter)".'
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
ms.openlocfilehash: a4546de2c5c1773aadce0ec084ee7058ff2ae153
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141885"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a>Endre modeller og tilordninger for å generere dokumenter med programdata

[!include [banner](../../includes/banner.md)]

For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren "ER generere dokumenter med oppdatering av programdata (del 2: generere dokumenter)". 

Trinnene i denne fremgangsmåten forklarer hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere et elektronisk dokument og oppdatere programdata. I denne fremgangsmåten skal du endre ER-konfigurasjonene for å begynne med å bruke dem til å generere elektroniske dokumenter og oppdatere programdata. Denne fremgangsmåten er opprettet for brukere med rollen som systemansvarlig eller elektronisk rapportering utvikler. Disse trinnene kan fullføres ved hjelp av DEMF-datasettet.


## <a name="modify-data-model"></a>Endre datamodell
1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Velg 'Intrastat (modell)' i treet.
    * Du vil utvide hvordan du bruker datamodellen. I tillegg til å bruke den som datakilde for å generere Intrastat-rapporten, brukes datamodellen til å samle inn informasjon om Intrastat-rapportering av prosessen. Detaljene vil deretter brukes til å oppdatere applikasjonsdata.   
3. Klikk Utforming.
4. Klikk Ny for å åpne nedtrekksdialogen.
5. I feltet Ny node som en for angir du Modellrot.
6. Skriv inn "For oppdatering av programdata" i Navn-feltet.
    * For oppdatering av programdata  
7. Klikk Legg til.
8. Velg "For oppdatering av programdata" i treet.
    * Denne nye rotelementet legges til å angi dataflyten for å flytte data fra rapporten Intrastat (brukes som en datakilde) til applikasjonen tabellene (oppdatering målet). Roten for ulike varer må tilordnes automatisk for å hente data som er postert til det utgående dokumentet og henter data fra dokumentet som brukes til å oppdatere programdata.   
9. Klikk Ny for å åpne nedtrekksdialogen.
10. Skriv inn "Arkivhode" i Navn-feltet.
    * Arkivhode  
11. Velg Postliste i Varetype-feltet.
12. Klikk Legg til.
    * Siden du vil opprette en post for hver Intrastat-rapport som genereres, må du opprette en ny vare for den.  
13. Klikk Ny for å åpne nedtrekksdialogen.
14. Skriv inn Filnavn i Navn-feltet.
    * Filnavn  
15. Velg Streng i Varetype-feltet.
16. Klikk Legg til.
17. Klikk Ny for å åpne nedtrekksdialogen.
18. Skriv inn "Antall linjer" i Navn-feltet.
    * Antall linjer  
19. Velg "Heltall" i Varetype-feltet.
20. Klikk Legg til.
    * Legg til denne varen for å angi antallet Intrastat-transaksjoner som er rapportert under gjeldende rapporteringsprosessen.  
21. Klikk Ny for å åpne nedtrekksdialogen.
22. Skriv inn "Arkivlinjer" i Navn-feltet.
    * Arkivlinjer  
23. Velg Postliste i Varetype-feltet.
24. Klikk Legg til.
    * Legg til denne varen for å representere listen over Intrastat-transaksjoner som er rapportert under gjeldende rapporteringsprosessen.  
25. Klikk Ny for å åpne nedtrekksdialogen.
26. I Navn-feltet skriver du inn Beløp.
    * Beløp  
27. Velg Faktisk i Varetype-feltet.
28. Klikk Legg til.
29. Klikk Ny for å åpne nedtrekksdialogen.
30. Skriv inn "Artikkelpost-ID" i Navn-feltet.
    * Artikkelpost-ID  
31. Velg Int64 i Varetype-feltet.
32. Klikk Legg til.
33. Klikk Ny for å åpne nedtrekksdialogen.
34. I Navn-feltet skriver du inn Varenummer.
    * Varenummer  
35. Velg Streng i Varetype-feltet.
36. Klikk Legg til.
37. Klikk Lagre.
38. Lukk siden.

## <a name="modify-model-mapping"></a>Endre modelltilordning
1. Utvid 'Intrastat (modell)' i treet.
2. Velg 'Intrastat (modell)\Intrastat (tilordning)' i treet.
    * Endre den eksisterende modell tilordningen til å bruke den for oppdateringen av programdata og for å arkivere Intrastat-rapportering detaljer.  
3. Klikk Utforming.
4. Klikk Ny.
5. Skriv inn "Oppdater arkiv" i Navn-feltet.
    * Oppdater arkiv  
6. Velg "Til mål" i feltet Retning.
7. Klikk Lagre.
    * Denne nye tilordningen angir dataflyt for flytting av data (rapportere Intrastat-detaljer) fra datamodellen til programmet tabellene (oppdatering målet). Legg merke til at ulike modeller roten varer må brukes til å hente data fra programmet for rapporteringsprosessen og deretter bruke dataene fra datamodellen for oppdateringen av programdata.   
8. Klikk Utforming.
9. Velg 'Datamodell\Datamodell' i treet.
    * Legg til den obligatoriske datakilden. Dette er datamodellen som inneholder detaljer om de rapporterte Intrastat-transaksjonene som må være arkivert.  
10. Klikk Legg til rot.
11. I Navn-feltet skriver du inn "modell".
    * modell  
12. I feltet Definisjon, angir eller velger du verdien "For oppdatering av programdata".
    * For oppdatering av programdata  
13. Klikk OK.
14. Utvid noden 'model' i treet.
15. Velg Funksjoner\Beregnet felt i treet.
16. Velg 'modell\Arkivhode' i treet.
17. Klikk Legg til.
    * Hvis du vil nummerere rapporterte Intrastat-transaksjoner for arkivering, må den riktige datakilden legges til.  
18. Skriv inn "Opplistede linjer" i Navn-feltet.
    * Opplistede linjer  
19. Klikk Rediger formel.
20. Velg 'List\ENUMERATE' i treet.
21. Klikk Legg til funksjon.
22. Utvid noden 'model' i treet.
23. Utvide 'modell\Arkivhode' i treet.
24. Velg 'modell\Arkivhode\Arkivlinjer'.
25. Klikk Legg til datakilde.
26. I Formel-feltet angir du 'ENUMERATE(model.'Archive header'.'Archive lines')'.
    * ENUMERATE(model.'Arkivhode'.'Arkivlinjer')  
27. Klikk Lagre.
28. Lukk siden.
29. Klikk OK.
30. Klikk Legg til mål.
    * Legg til programtabeller som nødvendige mål som krever oppdateringer for å arkivere detaljene i rapporterte Intrastat-transaksjoner.  
31. I Navn-feltet skriver du inn "Arkiv".
    * Arkiver  
32. Skriv inn "IntrastatArchiveGeneral" i Tabellnavn-feltet.
    * IntrastatArchiveGeneral  
    * Behold posthandlingen "Sett inn" slik at du kan legge til poster i løpet av den detaljerte arkiveringen av hver Intrastat-rapportering prosessen.  
33. Velg Ja i feltet Postinfologg.
    * Velg Ja hvis du vil ha informasjon om problemer med oppdateringen av programdata.  
34. Velg Ja i feltet Hopp over validering av posthandling.
    * Velg Ja hvis du vil skjule valideringsfeil om det tomme feltet "ID for Intrastat-arkiv". Dette vil bli gjort når poster legges til, basert på sekvens nummerserie innstillingene som er konfigurert for denne tabellen i parameterskjemaet Utenrikshandel.  
35. Klikk OK.
    * Bind elementene for de tillagte datakildene (filtrerte modell basert på valgte rotelementet) med elementer fra det nye målet.  
36. Utvid "Arkiv" i treet.
37. Utvid "Arkiv\<Relasjoner" i treet.
38. Utvid "Arkiv\<Relasjoner\IntrastatArchiveDetail" i treet.
39. I treet velger du "Arkiv\<Relasjoner\Intrastat\ArchiveDetail\Amount(AmountMST)".
40. Utvid 'modell\Arkivhode\Opplistede linjer' i treet.
41. Utvid 'modell\Arkivhode\Opplistede linjer\Verdi' i treet.
42. Velg 'modell\Arkivhode\Opplistede linjer\Verdi\Beløp' i treet.
43. Klikk Bind.
44. Velg 'arkiv\<Relasjoner\IntrastatArchiveDetail\Commodity(IntrastatCommodity)' i treet.
45. Velg 'modell\Arkivhode\Opplistede linjer\Verdi\Artikkelpost-ID' i treet.
46. Klikk Bind.
47. I treet velger du "Arkiv\<Relasjoner\IntrastatArchiveDetail\Item number(ItemId)".
48. Velg 'modell\Arkivhode\Opplistede linjer\Verdi\Varenummer' i treet.
49. Klikk Bind.
50. I treet velger du "Arkiv\<Relasjoner\IntrastatArchiveDetail\Line number(LineNumber)".
51. Velg 'modell\Arkivhode\Opplistede linjer\Nummer' i treet.
52. Klikk Bind.
53. Velg "Arkiv\<Relasjoner\Intrastat\ArchiveDetail" i treet.
54. Velg 'modell\Arkivhode\Opplistede linjer' i treet.
55. Klikk Bind.
56. Velg 'Arkiv\Filnavn(FileName)' i treet.
57. Velg 'modell\Arkivhode\Filnavn' i treet.
58. Klikk Bind.
59. Velg 'Arkiv\Antall linjer(NumberOfLines)' i treet.
60. Velg 'modell\Arkivhode\Antall linjer' i treet.
61. Klikk Bind.
62. Velg 'Arkiv' i treet.
63. Velg 'modell\Arkivhode' i treet.
64. Klikk Bind.
65. Klikk Lagre.
66. Lukk siden.
67. Lukk siden.

