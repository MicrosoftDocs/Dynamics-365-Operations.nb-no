---
title: Kostnadsregnskapsanalyse-innhold for Power BI
description: "Dette emnet beskriver hva som er inkludert i Kostnadsregnskapsanalyse-innhold for Power BI. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5ce75a6145bde4a8c33ed785c7d2a60a52416676
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="cost-accounting-analysis-power-bi-content"></a>Kostnadsregnskapsanalyse-innhold for Power BI

[!include[banner](../includes/banner.md)]


Dette emnet beskriver hva som er inkludert i Kostnadsregnskapsanalyse-innhold for Power BI. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

<a name="overview"></a>Oversikt
--------

**Kostregnskapsanalyse-innhold** for Microsoft Power BI er ment for kostnadskontrollører eller andre som er ansvarlig for å utføre kostnadskontroll i en organisasjon. Det inkluderer hovedmål, for eksempel kostnader, størrelse og kostnadssats etter faktiske kostnader, budsjettkostnader og fleksible budsjettkostnader. Det bruker transaksjonsdata fra kostnadsregnskap i Microsoft Dynamics 365 for Operations, og gir en samlet visning av kostnadene for hele organisasjonen i en rapporteringsvaluta. Ledere kan filtrere dataene etter kostnadsobjekter for å utføre kostnadskontroll for sine organisasjonsenheter, selv om organisasjonen kan ha flere juridiske enheter. Fordi **Kostregnskapsanalyse-innhold** for Power BI fremhever avvik mellom faktiske kostnader og budsjetterte kostnader, kan ledere bli varslet om positive og negative trender for sine driftsenheter. Ledere kan drille ned til kostnadselementhierarkier eller individuelle kostnadselementer for å få detaljert innsikt i hvordan kostnadsavvik har oppstått, og deretter utføre effektive tiltak. **Kostregnskapsanalyse-innhold** for Power BI lar regnskapsførere analysere hvordan kostnadsflyten går gjennom kostnadsobjektene for hele organisasjonen. Hvis du vil ha mer informasjon om kostnadsregnskap, se [startside for kostnadsregnskap](/dynamics365/operations/financials/cost-accounting/cost-accounting-home-page). Ved å definere tilgangsnivåsikkerhet i kostnadsregnskap og kombinere det med radnivåsikkerhet i Power BI, kan du gi alle kostnadsobjekteiere tilgang til **Kostregnskapsanalyse-innhold** for Power BI. Alle data i effektene blir deretter filtrert basert på tilgangsnivået som styres i kostnadsregnskap. Hvis du vil vite mer om tilgangsnivåsikkerhet og radnivåsikkerhet, kan du se [Konfigurere sikkerhet for Kostnadsregnskaps-innhold for Power BI](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innhold
Du kan finne **Kostnadsregnskapsanalyse-innhold** for Power BI i det delte aktivabiblioteket i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon om hvordan du laster ned innholdet og kobler det til Dynamics 365 for Operations-data, kan du se [Power BI-innhold i LCS fra Microsoft og partnere](power-bi-content-microsoft-partners.md). 

> MERK - **KB 4011327** er en forutsetning for dette Power BI-innholdet. Når du logger deg på Lifecycle Services, kan du få tilgang til KB her: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mål som er inkludert i Power BI-innholdet
Innholdet inneholder et sett med rapportsider. Hver side består av et sett med mål som er visualisert som diagrammer, fliser og tabeller. Tabellen nedenfor gir en oversikt over effekter i **Kostnadsregnskapsanalyse-innhold** for Power BI.

| Rapportside                      | Diagram                                                                                                                         | Flis                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Kostnadskontroll etter regnskapsperiode    | Faktiske kostnader og budsjettkostnader etter hierarkinivå for kostnadselement                                                                   | Faktisk kostnad i forhold til budsjettkostnad                    |
|                                  | Budsjettavvik etter hierarkinivå for kostnadselement                                                                               | Faktisk kostnadssats i forhold til kostnadssats for budsjett          |
|                                  | Topp 10 budsjettavvik i prosent etter kostnadselement                                                                          | Faktisk størrelse i forhold til budsjettstørrelse          |
| Kostnadskontroll etter hittil i år     | Faktiske kostnader og budsjettkostnader etter kalenderårperiode                                                                           | Faktisk kostnad i forhold til budsjettkostnad                    |
|                                  | Budsjettavvik etter kalenderårperiode                                                                                       | Faktisk kostnadssats i forhold til kostnadssats for budsjett          |
|                                  | Topp 10 budsjettavvik i prosent etter kostnadselement                                                                          | Faktisk størrelse i forhold til budsjettstørrelse          |
| Kostnadssats etter regnskapsår         | Faktisk kostnadssats etter kostnadsatferd                                                                                             | Faktisk kostnadssats i forhold til kostnadssats for budsjett          |
|                                  | Faktisk kostnadssats, budsjettkostnadsavvik, sats, kostnadssats for budsjett i prosent og kostnadssats for budsjett etter hierarkinivå for kostnadselement | Faktisk størrelse i forhold til budsjettstørrelse          |
|                                  | Budsjettavvik etter hierarkinivå for kostnadselement                                                                               |                                               |
|                                  | Topp 10 budsjettavvik i prosent etter kostnadselement                                                                          |                                               |
| Fleksibelt budsjett etter regnskapsperiode | Faktiske kostnader, budsjettkostnader og fleksible budsjettkostnader etter hierarkinivå for kostnadselement                                             | Faktisk størrelse i forhold til budsjettstørrelse          |
|                                  | Budsjettavvik og fleksibelt budsjettavvik etter hierarkinivå for kostnadselement                                                  | Faktisk kostnad i forhold til fleksibel budsjettkostnad           |
|                                  | Faktiske kostnader, budsjettkostnader og fleksible kostnader etter kostnadsatferd og hierarkinivå for kostnadselement                                  | Faktisk kostnadssats i forhold til kostnadssats for fleksibelt budsjett |
| Kostnadsoppgave etter regnskapsperiode  | Faktiske kostnader etter hierarkinivå for kostnadselement og navn på medlem av dimensjon for kostnadsobjekt                                             |                                               |
|                                  | Faktiske kostnader etter navn på medlem av dimensjon for kostnadsobjekt og navn på medlem av dimensjon for kostnadselement                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Dynamics 365 for Operations-data brukes til å fylle ut rapportsider i **Kostnadsregnskapsanalyse-innhold** for Power BI. Disse dataene representeres som aggregerte målinger som mellomlagres i enhetsbutikken, som er en Microsoft SQL-database som er optimalisert for analyse. Hvis du vil ha mer informasjon, se [Oversikt over Power BI-integrering med enhetslager](power-bi-integration-entity-store.md). De aggregerte nøkkelmålingene som du finner nedenfor, brukes som grunnlag for innholdet.

| Enhet                  | Aggregerte nøkkelmålinger | Datakilde for Dynamics 365 for Operations | Felt     | beskrivelse                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| Kostnadsregnskapsoppføringer | SUM(beløp)               | CAMDATAAggregatedCostEntry                  | Beløp    | Beløp i valuta for kostnadsregnskapsfinans |
| Statistiske oppføringer     | SUM(størrelse)            | CAMDATAAggregatedStatisctialEntry           | Størrelse |                                               |

Tabellen nedenfor viser hvordan de aggregerte nøkkelmålingene brukes til å opprette flere beregnede målinger i datasettet for innholdet.

| Mål                                       | Slik beregnes målet                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Faktisk kostnad                                   | CALCULATE('kostnadsregnskapsoppføringer'\[Mål\], 'Transaksjonsversjoner'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)            |
| Budsjettert kostnad                                   | CALCULATE('kostnadsregnskapsoppføringer'\[Mål\], 'Transaksjonsversjoner'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)            |
| Budsjettkostnadsavvik                          | \[Budsjettkostnad\] - \[Faktisk kostnad\]                                                                                      |
| Budsjettavviksprosent                    | IF (\[Budsjettkostnad\] = 0, tom(), \[Budsjettavvik\] / \[Budsjettkostnad\])                                                |
| Faktisk størrelse                              | CALCULATE('Statistiske oppføringer'\[FullMagnitude\], 'Transaction versions'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)          |
| Budsjettstørrelse                              | CALCULATE(\[FullMagnitude\], 'Transaksjonsversjoner'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)                               |
| Statistisk budsjettavvik                   | \[Budsjettstørrelse\] - \[Faktisk størrelse\]                                                                            |
| Statistisk budsjettavviksprosent        | IF(\[Budsjettstørrelse\] = 0, tom(), \[Statistisk budsjettavvik\] / \[Budsjettstørrelse\])                          |
| Faktisk kostnadssats                              | IF (\[Faktisk størrelse\] = 0, BLANK(), \[Faktisk kostnad\] / \[Faktisk størrelse\])                                          |
| Kostnadssats for budsjett                              | IF(\[Budsjettstørrelse\] = 0, BLANK(), \[Budsjettkostnad\] / \[Budsjettstørrelse\])                                          |
| Kostnadssats for budsjett, avvik                     | \[Faktisk kostnadssats\] - \[Faktisk kostnadssats\]                                                                            |
| Kostnadssats for budsjett, prosent          | IF (\[Budsjettkostnad\] = 0, tom(), \[Kostnadssats for budsjett, avvik\] / \[Kostnadssats for budsjett\])                                 |
| Fast budsjettkostnad                             | CALCULATE(\[Budsjettkostnad\], 'Kostnadsregnskapsoppføringer'\[COSTBEHAVIOR\] = 1)                                              |
| Variabel budsjettkostnad                          | CALCULATE(\[Budsjettkostnad\], 'Kostnadsregnskapsoppføringer'\[COSTBEHAVIOR\] = 2)                                              |
| Fast fleksibel budsjettkostnad                    | \[Fast budsjettkostnad\]                                                                                                  |
| Variabel fleksibel budsjettkostnad                 | IF(\[Budsjettstørrelse\] = 0, BLANK(), (\[Variabel budsjettkostnad\] / \[Budsjettstørrelse\]) \* \[Faktisk størrelse\])       |
| Fleksibel budsjettkostnad                          | \[Fast fleksibel budsjettkostnad\] + \[Variabel fleksibel budsjettkostnad\]                                                     |
| Fleksibelt budsjettavvik                      | \[Fleksibel budsjettkostnad\] - \[Faktisk kostnad\]                                                                             |
| Fleksibel budsjettavviksprosent           | IF(\[Fleksibel budsjettkostnad\] = 0, BLANK(), \[Fleksibelt budsjettavvik\] / \[Fleksibel budsjettkostnad\])                     |
| Kostnadssats for fleksibelt budsjett                     | IF (\[Faktisk størrelse\] = 0, BLANK(), \[Fleksibel budsjettkostnad\] / \[Faktisk størrelse\])                                 |
| Kostnadssats for fleksibelt budsjett, avvik            | \[Kostnadssats for fleksibelt budsjett\] - \[Faktisk kostnadssats\]                                                                   |
| Kostnadssats for fleksibelt budsjett, avviksprosent | IF(\[Kostnadssats for fleksibelt budsjett\] = 0, BLANK(), \[Kostnadssats for fleksibelt budsjett, avvik\] / \[Kostnadssats for fleksibelt budsjett\]) |

Nøkkeldimensjonene nedenfor brukes som filtre for å dele opp de aggregerte målingene for å oppnå flere detaljer og dypere analytisk innsikt.

| Enhet                             | Eksempler på attributter                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Finans for kostnadsregnskap            | Kostnadsregnskapsfinans                                                                                               |
| Kostnadskontrollenheter                 | Navn på kostnadskontrollenhet                                                                                               |
| Kostnadselementdimensjoner            | Navn på kostnadselementdimensjon, navn på medlem av dimensjon for kostnadselement, beskrivelse av medlem av dimensjon for kostnadselement          |
| Kostnadsobjektdimensjoner             | Navn på kostnadsobjektdimensjon, navn på medlem av dimensjon for kostnadsobjekt, beskrivelse av medlem av dimensjon for kostnadsobjekt              |
| Statistiske dimensjoner             | Navn på statistisk dimensjon, Navn på medlem av statistisk dimensjon, beskrivelse av medlem av statistisk dimensjon              |
| Hierarkier for kostnadsobjektdimensjon  | Hierarkinavn for kostnadsobjektdimensjon, hierarkinivå for kostnadsobjektdimensjon, hierarkitre for kostnadsobjektdimensjon    |
| Dimensjonshierarkier for kostnadselement | Hierarkinavn for kostnadselementdimensjon, hierarkinivå for kostnadselementdimensjon, hierarkitre for kostnadselementdimensjon |
| Hierarkier for statistisk dimensjon  | Dimensjonshierarkinavn for statistikk, dimensjonshierarkinivå for statistikk, dimensjonshierarkitre for statistikk    |
| Transaksjonsversjoner               | Navn på versjon                                                                                                         |
| Økonomiske kalendere                   | Kalender, kalenderbeskrivelse                                                                                       |
| Regnskapsår                       | Kalenderår                                                                                                        |
| Regnskapsperioder                     | Kalenderårperiode                                                                                                 |

## <a name="additional-resources"></a>Tilleggsressurser
Her er noen nyttige koblinger som er knyttet til enheter og oppretting av Power BI-innhold:

-   [Dataenheter](..\data-entities\data-entities.md)
-   [Opprette innholdspakker for organisasjonen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering med Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Legge til Power BI-fliser i arbeidsområder](configure-power-bi-integration.md)
-   [Konfigurere sikkerhet for Kostnadsregnskaps-innhold for Power BI](setup-security-cost-accounting-content-pack.md)




