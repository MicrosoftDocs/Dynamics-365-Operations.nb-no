---
title: Definere arbeidsceller for lean manufacturing
description: En arbeidscelle er en bestemt type ressursgruppe som kan brukes i lean manufacturing-prosessaktiviteter.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, InventLocationIdLookup, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f1144bd9f99fef44210c2a01f71a39488354ccf
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576790"
---
# <a name="define-lean-manufacturing-work-cells"></a>Definere arbeidsceller for lean manufacturing

[!include [banner](../../includes/banner.md)]

En arbeidscelle er en bestemt type ressursgruppe som kan brukes i lean manufacturing-prosessaktiviteter. Arbeidsceller har innleverings- og utleveringssteder og en kapasitetsdefinisjon basert på en produksjonsflytmodell. Hvis du vil lære mer om de grunnleggende begrepene for arbeidsceller og kapasitetsberegninger for lean manufacturing, kan du se de tekniske dokumentene for Lean manufacturing. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne prosedyren


## <a name="create-a-work-cell"></a>Opprett en arbeidscelle. 
1. Gå til Organisasjonsstyring > Ressurser > Ressursgrupper.
2. Klikk på Ny.
3. Skriv inn en verdi i Ressursgruppe-feltet.
    * Arbeidscelle-ID-en er vanligvis en systematisk kode og må være unik for den juridiske enheten.  
4. Skriv inn en verdi i feltet Beskrivelse.
    * Beskrivelsen inneholder navnet på eller tittelen for arbeidscellen.  
5. Klikk på rullegardinknappen i Område-feltet for å åpne oppslaget.
    * En arbeidscelle finnes på ett bestemt område. Både inn- og utleveringslager og lokasjon må ligge på dette området.  
6. Klikk på koblingen i den valgte raden i listen.
7. Klikk på rullegardinknappen i feltet Produksjonsenhet for å åpne oppslaget.
8. Klikk på koblingen i den valgte raden i listen.
    * Velg en produksjonsenhet som denne arbeidscellen tilhører.  
9. Merk av for Arbeidscelle.
    * Hvis du vil bruke en ressursgruppe som en lean-arbeidscelle, må du merke av for Arbeidscelle.  Legg merke til at denne egenskapen ikke kan endres etter ressursgruppen er opprettet.  
10. Klikk på rullegardinknappen i feltet Innleveringslager for å åpne oppslaget.
11. Klikk på koblingen i den valgte raden i listen.
    * For regnskaps- og materialstyring fordeles vanligvis materialet som oppsamles i shop floor, til et bestemt virtuelt lager. Hvis du ønsker å etterfylle lokasjonene ved hjelp av lagerarbeid, må de imidlertid være en del av det mottakelige råvarelageret.  
12. Klikk på rullegardinknappen i feltet Innleveringssted for å åpne oppslaget.
13. Klikk på koblingen i den valgte raden i listen.
    * Legg merke til at for en prosessaktivitet kan Innleveringsstedet overskrives generelt eller for et bestemt produkt eller en bestemt produktvariant ved å definere plukkaktivitetene som feeder til prosessaktiviteten. Innleveringslokasjonene for en arbeidscelle kan ikke være nummerskiltkontrollert.  
14. Klikk på rullegardinknappen i feltet Utleveringslager for å åpne oppslaget.
15. Finn og velg ønsket post i listen.
    * I flere aktivitetsproduksjonsflyter eller -produksjonslinjer er dette ofte innleveringslageret for neste arbeidscelle eller salgs- eller transittlager som et produkt vanligvis overføres til etter produksjonsprosessen. Husk at under utforming av lean manufacturing-prosesser er transport vanligvis avfall, det samme er rapportering av transport.  
16. Klikk på koblingen i den valgte raden i listen.
17. Klikk på rullegardinknappen i feltet Utleveringssted for å åpne oppslaget.
    * I en produksjonsflyt med flere prosessaktiviteter er dette ofte Innleveringsstedet for den neste arbeidscellen.  
18. Finn og velg ønsket post i listen.
19. Klikk på koblingen i den valgte raden i listen.
20. Vis eller skjul delen Operasjon.
    * En kjøretidskategori må angis for å aktivere kostnadsberegning og behandling av lean kanban-jobber.  
21. Klikk på rullegardinknappen i feltet Kjøretidskategori for å åpne oppslaget.
22. Finn og velg ønsket post i listen.
    * Kjøretidskostnadskategorien brukes i standard kostnadsberegning og backflush-etterkalkulering.  
23. Klikk på koblingen i den valgte raden i listen.
24. Vis eller skjul delen Kalendere.
25. Klikk på Legg til.
26. Klikk på rullegardinknappen i Kalender-feltet for å åpne oppslaget.
27. Finn og velg ønsket post i listen.
    * Arbeidscellene i et område bruker vanligvis samme arbeidstidskalender. Hvis arbeidsceller kan ha individuelle arbeidstider, må du kanskje opprette en bestemt arbeidstidskalender for arbeidscellen. Legg merke til at kalenderen skal ha en standard arbeidstid definert når den brukes for en lean arbeidscelle, fordi kapasitetsdefinisjonen vanligvis er knyttet til standard arbeidstid for en arbeidsdag.  
28. Klikk på koblingen i den valgte raden i listen.
29. Vis eller skjul delen Arbeidscellekapasitet.
30. Klikk på Legg til.
31. Klikk på rullegardinknappen i feltet Produksjonsflytmodell for å åpne oppslaget.
32. Finn og velg ønsket post i listen.
    * Denne prosedyren krever gjennomstrømming av typen produksjonsflytmodell for å vise definisjonen av produksjonskapasitet.  
33. Klikk på koblingen i den valgte raden i listen.
34. Velg et alternativ i Kapasitetsperiode-feltet.
    * Alternativene omfatter: Standard arbeidsdag - kapasiteten uttrykkes av lengden på standard arbeidsdagen i arbeidstidskalenderen for arbeidscellen. For hver dag bestemmes faktisk arbeidstid fra kalenderen og den gyldige tilgjengelige kapasiteten beregnes basert på den.   Uke - tillater en ukentlig kapasitet. Det gjøres ingen justering av faktisk arbeidstid.   Måned - tillater en månedlig kapasitet. Det gjøres ingen justering av faktisk kapasitet.   Vanligvis brukes standard arbeidsdag for daglig perioder og ukentlig kapasitet brukes for ukentlige kapasitetsperioder.  
35. Angi et nummer i feltet Gjennomsnittlig gjennomstrømningsantall.
    * Legg merke til at en lean-operasjon aldri defineres for den maksimale kapasiteten som er mulig i et ideelt miljø. I stedet bør alltid kapasiteten defineres for operasjoner som kjører under vanlige forhold.  
36. Klikk på rullegardinknappen i feltet Enhet for å åpne oppslaget.
37. Klikk på koblingen i den valgte raden i listen.
38. ResolveChanges enheten.

## <a name="add-a-financial-dimension"></a>Legge til en finansdimensjon
1. Vis eller skjul delen Finansdimensjoner.
    * Legg merke til at finansdimensjoner som er definert for produksjonsflyten overstyrer finansdimensjonen for en gitt arbeidscelle.    Finansdimensjonene som kan velges, avhenger av konfigurasjonen av finansdimensjonene for systemet. Følgende trinn tilsvarer demodatasettet i firma USMF. Når du bruker andre data, er det ikke sikkert at trinnene gjelder.  
2. Klikk på rullegardinknappen i feltet CostCenter for å åpne oppslaget.
3. Finn og velg ønsket post i listen.
    * Dimensjonene som skal velges for lean-arbeidsceller, avhenger av implementeringen av finansdimensjoner i regnskapsmodellen for en bestemt juridisk enhet.  
4. Klikk på koblingen i den valgte raden i listen.
5. Klikk på rullegardinknappen i feltet ItemGroup for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
7. Klikk på koblingen i den valgte raden i listen.

## <a name="save"></a>Lagre
1. Klikk på Lagre.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]