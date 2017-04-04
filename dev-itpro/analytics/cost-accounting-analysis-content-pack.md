---
title: "Kostregnskapsanalyse strøm BI-innhold"
description: "Dette emnet beskriver hva som er inkludert i kostnadsregnskap analyse strømmen BI-innhold. Det forklarer hvordan du kan få tilgang til strøm BI-rapporter, og gir informasjon om datamodell og enheter som ble brukt til å bygge opp innholdet."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 50e7bd92ee693f59fd013226aee22bd1a54c81e2
ms.lasthandoff: 03/31/2017


---

# <a name="cost-accounting-analysis-power-bi-content"></a>Kostregnskapsanalyse strøm BI-innhold

Dette emnet beskriver hva som er inkludert i kostnadsregnskap analyse strømmen BI-innhold. Det forklarer hvordan du kan få tilgang til strøm BI-rapporter, og gir informasjon om datamodell og enheter som ble brukt til å bygge opp innholdet.

<a name="overview"></a>Oversikt
--------

Den **Kostregnskapsanalyse** Microsoft Power BI-innhold er ment for å kontrollere kostnader eller andre som er ansvarlig for å utføre kostnadskontroll i en organisasjon. Det inkluderer hovedmål, for eksempel kostnader, størrelsen og kostnadssats av faktiske kostnader, budsjettkostnader og fleksible budsjettkostnader. Den bruker transaksjonsdata fra kostnadsregnskap i Microsoft Dynamics 365 for operasjoner, og gir en samlet visning av kostnadene for hele organisasjonen i en rapporteringsvaluta. Ledere kan filtrere dataene ved kostnad objekter til å utføre kostnadskontroll for sine organisasjonsenheter, selv om organisasjonen kan ha flere juridiske enheter. Fordi det **Kostregnskapsanalyse** strømmen BI innhold høydepunkter avvik mellom budsjetterte kostnader og faktiske kostnader ledere kan bli varslet om positive og negative trender for sine operative enheter. Ledere kan drille ned kostnadene elementet hierarkier eller individuelle kostnadselementer få detaljert innsikt i hvordan kostnadsavvik har oppstått, og deretter utføre effektive tiltak. Den **Kostregnskapsanalyse** strømmen BI innhold La oss analysere kostnader regnskapsførere hvordan kostnadsflyten går gjennom objektene kostnaden for hele organisasjonen. Hvis du vil ha mer informasjon om kostnadsregnskapet, se [kostnadsregnskap hjemmeside](/dynamics365/operations/financials/cost-accounting/cost-accounting-home-page.md). Ved å definere sikkerhet tilgang på brukernivå i kostnadsregnskap og kombinere det med strøm BI på radnivå sikkerhet, kan du gi alle kostnader objektet eiere tilgang til den **Kostregnskapsanalyse** strømmen BI-innhold. Alle data i effektene blir deretter filtrert basert på tilgangsnivået som styres i kostnadsregnskap. Hvis du vil vite mer om sikkerhet tilgang på brukernivå og rad brukersikkerhet, kan du se [satt opp sikkerhet for kostnadsregnskap innhold for strøm BI](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Tilgang til strøm BI-innhold
Du kan finne den **Kostregnskapsanalyse** strømmen BI-innhold i delte aktiva biblioteket i Microsoft Dynamics Lifecycle tjenester (LCS). Hvis du vil ha mer informasjon om hvordan du laster ned innholdet, og koble den til din Dynamics 365 for operasjoner data, se [strømmen BI-innhold i LCS fra Microsoft og partnere på](power-bi-content-microsoft-partners.md). **Merk:** KB4011327 ** ** er en forutsetning for den **Kostregnskapsanalyse** strømmen BI-innhold.  Når du logger deg på levetidstjenester, kan du få tilgang til KB her: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mål som er inkludert i strøm BI-innhold
Innholdet inneholder et sett med rapportsider. Hver side består av et sett med mål som er visualized som tabeller, diagrammer og fliser. Tabellen nedenfor gir en oversikt over effekter i den **Kostregnskapsanalyse** strømmen BI-innhold.

| Rapportside                      | Diagram                                                                                                                         | Flis                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Kostnadskontroll etter regnskapsperiode    | Faktiske kostnader og budsjettkostnader ved kostnad elementet Hierarkinivå                                                                   | I forhold til faktiske kostnader, budsjettkostnader                    |
|                                  | Budsjett variansen av kostnader elementet Hierarkinivå                                                                               | Frekvens i forhold til faktiske kostnader budsjett kostnadssats          |
|                                  | Topp 10 Budsjettavvik i prosent av kostnader-elementet                                                                          | Faktisk størrelsen i forhold til budsjett magnitude          |
| Kostnadskontroll ved hittil i år     | Faktiske kostnader og budsjettkostnader etter kalenderåret periode                                                                           | I forhold til faktiske kostnader, budsjettkostnader                    |
|                                  | Varians for budsjett etter periode for kalenderåret                                                                                       | Frekvens i forhold til faktiske kostnader budsjett kostnadssats          |
|                                  | Topp 10 Budsjettavvik i prosent av kostnader-elementet                                                                          | Faktisk størrelsen i forhold til budsjett magnitude          |
| Kostnadssats av regnskapsåret.         | Faktisk kostnadssats ved kostnad virkemåte                                                                                             | Frekvens i forhold til faktiske kostnader budsjett kostnadssats          |
|                                  | Faktisk kostnadssats, budsjett kostnadsavvik rate, budsjettkostnader prosentsatsen og kostnadssats for budsjett ved kostnad elementet Hierarkinivå | Faktisk størrelsen i forhold til budsjett magnitude          |
|                                  | Budsjett variansen av kostnader elementet Hierarkinivå                                                                               |                                               |
|                                  | Topp 10 Budsjettavvik i prosent av kostnader-elementet                                                                          |                                               |
| Fleksibelt budsjett etter regnskapsperiode | Faktiske kostnader, budsjettkostnader og fleksible budsjettkostnader ved kostnad elementet Hierarkinivå                                             | Faktisk størrelsen i forhold til budsjett magnitude          |
|                                  | Varians for budsjett og fleksibelt budsjett variansen av kostnader elementet Hierarkinivå                                                  | Faktiske kostnader i forhold til fleksible budsjettkostnader           |
|                                  | Faktiske kostnader, budsjettkostnader og fleksible kostnader ved kostet virkemåten og kostet Hierarkinivå element                                  | Kostnadssatsen for faktiske kostnader hastighet i forhold til fleksibelt budsjett |
| Kostnadsoppgave etter regnskapsperiode  | Faktiske kostnader ved Hierarkinivå element for kostnader og kostnader dimensjon medlem objektnavn                                             |                                               |
|                                  | Faktiske kostnader ved kostnad objektet dimensjon-medlemsnavnet og -kostnader dimensjon medlem elementnavn                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Dynamics 365 for operasjoner data brukes til å fylle rapportsidene den **Kostregnskapsanalyse** strømmen BI-innhold. Disse dataene er representert som samlet mål mellomlagres i butikken enhet, som er en Microsoft SQL-database som er optimalisert for analyse. Hvis du vil ha mer informasjon, se [strømmen BI-oversikt over integrering med enheten butikken](power-bi-integration-entity-store.md). De følgende viktige samlet mål som skal brukes som grunnlag for innholdet.

| Enhet                  | Viktige samlet mål | Datakilde for Dynamics 365 for operasjoner | Felt     | beskrivelse                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| Oppføringer for kostnadsregnskap | Sum(Amount)               | CAMDATAAggregatedCostEntry                  | Beløp    | Beløpet i valutaen som Finans kostnadsregnskap |
| Statistiske oppføringer     | Sum(MAGNITUDE)            | CAMDATAAggregatedStatisctialEntry           | Størrelse |                                               |

Tabellen nedenfor viser hvordan de viktige samlet mål som skal brukes til å opprette flere beregnede mål i det innholdet dataset.

| Mål                                       | Hvordan målet skal beregnes                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Faktisk kostnad                                   | BEREGN (kostnadsregnskap-oppføringer\[mål\], 'Transaksjonen versjoner'\[ISSOURCEVERSIONBUDGET\_verdien\] = 0)            |
| Budsjettert kostnad                                   | BEREGN (kostnadsregnskap-oppføringer\[mål\], 'Transaksjonen versjoner'\[ISSOURCEVERSIONBUDGET\_verdien\] = 1)            |
| Budsjettert kostnad avvik                          | \[Budsjettere kostnader\] - \[faktisk kostnad\]                                                                                      |
| Budsjett avviksprosent                    | IF (\[budsjettkostnader\] = 0, blank(), \[Budsjettavvik\] / \[budsjettkostnader\])                                                |
| Faktisk størrelsen                              | BEREGN ('Statistisk oppføringer'\[FullMagnitude\], 'Transaksjonen versjoner'\[ISSOURCEVERSIONBUDGET\_verdien\] = 0)          |
| Magnitude budsjett                              | BEREGN (\[FullMagnitude\], 'Transaksjonen versjoner'\[ISSOURCEVERSIONBUDGET\_verdien\] = 1)                               |
| Statistisk Budsjettavvik                   | \[Budsjett magnitude\] - \[faktisk størrelsen\]                                                                            |
| Statistisk budsjett avviksprosent        | IF (\[budsjett magnitude\] = 0, blank(), \[statistisk Budsjettavvik\] / \[budsjett magnitude\])                          |
| Faktisk kostnadssats                              | IF (\[faktisk størrelsen\] = 0, BLANK(), \[faktisk kostnad\] / \[faktisk størrelsen\])                                          |
| Kostnadssats for budsjett                              | IF (\[budsjett magnitude\] = 0, BLANK(), \[budsjettkostnader\] / \[budsjett magnitude\])                                          |
| Budsjettert kostnad rate avvik                     | \[Kostnadssatsen for budsjettet\] - \[Faktisk kostnadssats\]                                                                            |
| Budsjettert kostnad avvik i prosent          | IF (\[budsjettkostnader\] = 0, blank(), \[budsjett kostnadsavvik-rate\] / \[budsjett kostnadssats\])                                 |
| Fast Budsjettkostnad                             | BEREGN (\[budsjettkostnader\], 'Accounting Poster kostnader'\[COSTBEHAVIOR\] = 1)                                              |
| Variabel Budsjettkostnad                          | BEREGN (\[budsjettkostnader\], 'Accounting Poster kostnader'\[COSTBEHAVIOR\] = 2)                                              |
| Fast fleksible budsjettkostnader                    | \[Fast Budsjettkostnad\]                                                                                                  |
| Variabel fleksible budsjettkostnader                 | IF (\[budsjett magnitude\] = 0, BLANK(), (\[variabel budsjettkostnader\] / \[budsjett magnitude\]) \*\[faktisk størrelsen\])       |
| Fleksible budsjettkostnader.                          | \[Faste kostnader for fleksibelt budsjett\] + \[variabel fleksible budsjettkostnader\]                                                     |
| Varians for fleksibelt budsjett                      | \[Fleksible budsjettkostnader\] - \[faktisk kostnad\]                                                                             |
| Fleksibelt budsjett avviksprosent           | IF (\[fleksible budsjettkostnader\] = 0, BLANK(), \[fleksibelt Budsjettavvik\] / \[fleksible budsjettkostnader\])                     |
| Fleksible budsjettkostnader rate                     | IF (\[faktisk størrelsen\] = 0, BLANK(), \[fleksible budsjettkostnader\] / \[faktisk størrelsen\])                                 |
| Fleksible budsjettkostnader rate avvik            | \[Kostnadssatsen for fleksibelt budsjett\] - \[Faktisk kostnadssats\]                                                                   |
| Prosentsatsen for fleksibelt budsjett kostnad avvik | IF (\[kostnadssatsen for fleksibelt budsjett\] = 0, BLANK(), \[fleksibelt budsjett kostnadsavvik-frekvens\] / \[kostnadssatsen for fleksibelt budsjett\]) |

Følgende viktige dimensjoner brukes som filtre kan skjære samlet målene for å oppnå større tetthet og gir dypere analytisk kunnskap.

| Enhet                             | Eksempler på attributtene                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Finans for kostnadsregnskap            | Kostnadsregnskapsfinans                                                                                               |
| Kostnadskontrollenheter                 | Navn på kostnadskontrollenhet                                                                                               |
| Kostnadselementdimensjoner            | Kostnad elementer dimension navn, kostnader dimensjon medlem elementnavnet, kostnader dimensjon medlem elementbeskrivelse          |
| Kostnadsobjektdimensjoner             | Kostobjekt dimensjonsnavn, kostnad objektet dimensjon medlemsnavn, kostnad objektet dimensjon medlem beskrivelse              |
| Statistiske dimensjoner             | Statistisk dimensjonsnavn, statistisk dimensjon medlemsnavn, statistisk dimensjon medlem beskrivelse              |
| Dimensjonshierarkier kostnads-objekt  | Koster hierarkiet i dimensjonen i objektnavn, koster objektet dimensjon hierarkinivå, kostnad-objekt dimensjonshierarkitreet    |
| Cost element dimensjonshierarkier | Koster hierarkiet i dimensjonen i elementnavnet, Cost element dimensjon hierarkinivå, kostnaden elementet dimensjonshierarkitreet |
| Statistisk dimensjonshierarkier  | Statistisk dimensjon hierarki-navnet, statistisk dimensjon hierarkinivå, statistiske dimensjonshierarkitreet    |
| Transaksjonsversjoner               | Navn på versjon                                                                                                         |
| Økonomiske kalendere                   | Kalenderen er Kalender-beskrivelse                                                                                       |
| Regnskapsår                       | Kalenderår                                                                                                        |
| Regnskapsperioder                     | Kalender-årsperiode                                                                                                 |

## <a name="additional-resources"></a>Tilleggsressurser
Her er noen nyttige koblinger som er knyttet til enheter og oppretting av Power BI-innhold:

-   [Dataenheter](..\data-entities\data-entities.md)
-   [Opprette innholdspakker for organisasjonen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering med Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Legge til Power BI-fliser i arbeidsområder](configure-power-bi-integration.md)
-   [Konfigurere sikkerhet for kostnadsregnskap innhold for strøm BI](setup-security-cost-accounting-content-pack.md)


