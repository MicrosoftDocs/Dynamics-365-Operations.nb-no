---
title: Definere en prosess for minimums-/maksimumsetterfylling
description: Denne fremgangsmåten viser hvordan du definerer en ny etterfyllingprosess som bruker strategien for minimums-/maksimumsetterfylling.
author: perlynne
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, InventItemIdLookupSimple, WMSLocationIdLookup, WHSLocDirTable, InventLocationIdLookup, SysQueryForm, WHSWorkTemplateTable, WHSReplenishmentTemplates, UnitOfMeasureLookup, SysQueryTableLookUp, SysQueryFieldLookUp, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ef3c33125850662cfb0dfba6e6349ce32ceda0af
ms.sourcegitcommit: 62d66f98d4bbf916e19184506b90055bb68d219f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/28/2019
ms.locfileid: "1924453"
---
# <a name="set-up-a-min-max-replenishment-process"></a>Definere en prosess for minimums-/maksimumsetterfylling

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du definerer en ny etterfyllingprosess som bruker strategien for minimums-/maksimumsetterfylling. Når lagernivået synker til under minimumsnivået, opprettes det arbeid for å etterfylle lokasjonen. Fremgangsmåten viser også hvordan du bruker faste plukklokasjoner for å tillate etterfylling selv om lagernivået synker til under minimumsnivået, og hvordan du aktiverer at etterfyllingsprosessen skal kjøres regelmessig ved hjelp av en satsvis jobb. Disse oppgavene vil vanligvis utføres av en lagersjef. Du kan kjøre denne prosedyren i USMF-demodatafirmaet ved hjelp av eksempelverdiene i notatene, eller du kan kjøre den på dine egne data. Hvis du bruker dine egne data, må du kontrollere at du har et lager som er aktivert for lagerstyringsprosesser.


## <a name="create-a-fixed-picking-location"></a>Opprette en fast plukklokasjon
1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Lager > Faste lokasjoner**. Dette er en valgfri oppgave for minimums-/maksimumsetterfylling, men hvis du bruker fast plukklokasjon, gjør dette at lageret etterfylles selv om det faller under minimumsnivået, fordi systemet kan finne ut hvilke varer som må etterfylles, selv om det ikke er noen igjen.
2. Klikk på **Ny**.
3. Angi eller velg en verdi i **Varenummer**-feltet. Hvis du bruker USMF, kan du velge vare 'A0001'.  
4. Angi eller velg en verdi i **Område**-feltet. Hvis du bruker USMF, kan du velge område 2.  
5. Angi eller velg en verdi i feltet **Lager**. Hvis du bruker USMF, kan du velge lager 24.  
6. Angi eller velg en verdi i feltet **Lokasjon**. Hvis du bruker USMF, kan du velge CP-003.  
7. Lukk siden.

## <a name="create-a-replenishment-location-directive"></a>Opprette et lokasjonsdirektiv for etterfylling
1. Gå til **Lagerstyring > Oppsett > Lokasjonsdirektiver**. Lokasjonsdirektiver brukes til å bestemme hvor varene skal plukkes fra i etterfyllingsprosessen.
2. Velg Etterfylling i feltet **Arbeidsordretype**.
3. Klikk **Ny** i **handlingsruten**.
4. Skriv inn en verdi i **Navn**-feltet.
5. Velg Plukk i **Arbeidstype**-feltet.
6. Angi eller velg en verdi i **Område**-feltet. Hvis du bruker USMF, kan du velge område 2.  
7. Angi eller velg en verdi i feltet **Lager**. Hvis du bruker USMF, kan du velge lager 24.  
8. Klikk **Lagre**.
9. Klikk på **Ny**i **Linjer**-delen.
10. Merk den valgte raden i listen.
11. Angi et tall i feltet **Til-antall**. Du kan for eksempel sette dette til 9999.  
12. Merk av for **Tillat oppdeling**. Hvis du velger dette alternativet, tillater arbeidsopprettelsesprosessen at arbeidslinjeantall kan deles på tvers av flere lokasjoner.  
13. Klikk **Lagre**.
14. Klikk på **Ny** i **Lokasjonsdirektivhandlinger**-delen.
15. Merk den valgte raden i listen.
16. Skriv inn en verdi i **Navn**-feltet.
17. Klikk **Lagre**.
18. Klikk på **Rediger spørring** i **handlingsruten**. Du kan redigere denne spørringen for å legge til begrensninger der lageret kan velges fra i etterfyllingsprosessen. Det kan for eksempel være at lageret bare skal brukes fra partiområdet i lageret.
19. Klikk **OK**.
20. Lukk siden.

## <a name="create-a-replenishment-work-template"></a>Opprette en arbeidsmal for etterfylling
1. Gå til **Lagerstyring > Oppsett > Arbeid > Arbeidsmaler**. Arbeidsmalen brukes for å veilede systemet for hvordan arbeidet for minimums-/maksimumsetterfylling skal opprettes. Som et minimum må det være en arbeidsmallinje for plukking og plassering. Arbeidsmalen vil si at den er ugyldig til all nødvendig informasjon er fylt ut. 
2. Velg Etterfylling i feltet **Arbeidsordretype**.
3. Klikk **Ny** i **handlingsruten**.
4. Angi en verdi i feltet **Arbeidsmal**.
5. Klikk **Lagre**.
6. Klikk på **Ny** i **Arbeidsmaldetaljer**-delen:
7. Velg Plukk i **Arbeidstype**-feltet.
8. Angi eller velg en verdi i feltet **Arbeidsklasse-ID**. Dette bør være en arbeidsklasse relatert til etterfylling. Hvis du bruker USMF, velger du Etterfylle.  
9. Klikk på **Ny** i **Arbeidsmaldetaljer**-delen:
10. Merk den valgte raden i listen.
11. Velg Plasser i **Arbeidstype**-feltet.
12. Angi eller velg en verdi i feltet **Arbeidsklasse-ID**.
13. Klikk **Lagre**.
14. Lukk siden.

## <a name="create-a-new-replenishment-template"></a>Opprette en ny etterfyllingsmal
1. Gå til **Lagerstyring > Oppsett > Etterfylling > Etterfyllingsmaler**. Etterfyllingsmalen brukes til å definere varer og antall og lokasjonen som skal etterfylles.
2. Klikk **Ny** i **handlingsruten**.
3. Angi en verdi i feltet **Etterfyllingsmal**. Gi malen et navn for å angi at den er for minimums-/maksimumsetterfylling.  
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Merk av for **Tillat at bølgebehov kan bruke ureserverte antall**. Hvis du velger dette alternativet, gir det mulighet for etterfylling for bølgebehov antallene som er relatert til minimums-/maksimumsetterfylling. Dette kan for eksempel være nyttig hvis arbeidet for minimums-/maksimumsetterfylling ikke behandles umiddelbart, slik at du unngår oppretting av unødvendige arbeid for behovsetterfylling.
6. Klikk på **Ny** i **Detaljer for etterfyllingsmal**-delen:
7. Angi et nummer i **Sekvensnummer**-feltet.
8. Skriv inn en verdi i **Beskrivelse**-feltet.
9. Merk den valgte raden i listen.
10. Angi eller velg en verdi i feltet **Etterfyllingsenhet**. Velg for eksempel stk. Denne innstillingen er obligatorisk. Den lar deg angi en annen målenhet for etterfyllingsarbeid sammenlignet med enheten som er angitt for de minste og største lagernivåene i denne malen.
11. Angi eller velg en verdi i feltet **Arbeidsmal**. Velg arbeidsmalen du opprettet tidligere.  
12. Angi et tall i feltet **Minimumsantall**. Velg det minste antallet som skal utløse etterfyllingen. Sett det for eksempel til 50. Det er mulig å la det være satt til null hvis du etterfyller en fast plassering og alternativet **Etterfyll tomme faste lokasjoner** er satt til Ja. Vi anbefaler også at du velger alternativet **Etterfyll bare faste lokasjoner** med hensyn til ytelsen.
13. Angi et tall i feltet **Maksimumsantall**. Sett det for eksempel til 100.  
14. Angi eller velg en verdi i **Enhet**-feltet. Tilordne enheten for minimums- og maksimumsantall. Sett det for eksempel til stk.  
15. Merk av for **Etterfyll tomme faste lokasjoner**. Velg dette alternativet for å etterfylle faste lokasjoner når de er tomme. Du kan eventuelt bare lokasjonene der det er et antall på lager som skal etterfylles.
16. Merk av for **Etterfyll bare faste lokasjoner**.
17. Klikk på **Velg produkter**. Dette er stedet der du kan definere hvilke produkter som skal etterfylles. Hvis det er merket av for alternativet Faste plukklokasjoner, må du også definere lokasjonene i denne spørringen. Variantspesifikke og produktspesifikke spørringer er tilgjengelige.
18. Velg raden **Varer**.
19. Skriv inn en verdi i **Kriterier**-feltet. Velg varene som skal etterfylles på de faste lokasjonene. Skriv for eksempel inn A* for å velge alle varenumre som begynner med A.
20. Klikk **Legg til**. Legg til enhetslokasjonen (med mindre den allerede finnes) for å kunne begrense etterfyllingsarbeidet til de faste plukklokasjonene innenfor et bestemt område i lageret.
21. Merk den valgte raden i listen.
22. Sett **Tabell**-feltet til Lokasjoner.
23. Velg lokasjonsprofil-ID i feltet **Felt**.
24. Angi eller velg en verdi i **Kriterier**-feltet.
25. Klikk **OK**.
26. Lukk siden.

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a>Angi at etterfyllingsprosessen skal kjøres som en satsvis jobb
1. Gå til **Lagerstyring > Etterfylling > Etterfyllinger**. Siden Etterfyllinger lar deg definere etterfylling som skal kjøres som en satsvis jobb, eller å kreve at den startes manuelt.
2. Klikk **Filter**.
3. Merk den valgte raden i listen.
4. Angi eller velg en verdi i **Kriterier**-feltet.
5. Klikk **OK**.
6. Vis delen **Kjør i bakgrunnen**.
7. Sett alternativet **Satsvis behandling** til Ja.
8. Klikk på **Regelmessighet**.
9. Velg alternativet **Ingen sluttdato**.
10. Angi **Mønster for regelmessighet** Velg for eksempel Dager.  
11. Klikk **OK**.
12. Klikk **OK**.

