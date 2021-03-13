---
title: Power BI-innholdet Kostnadsregnskapsanalyse
description: Dette emnet beskriver hva som er inkludert i Kostnadsregnskapsanalyse-innhold for Power BI.
author: AndersGirke
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1c9a4741c1b09b8e68a9fe95d6f4effa328615d5
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093392"
---
# <a name="cost-accounting-analysis-power-bi-content"></a>Power BI-innholdet Kostnadsregnskapsanalyse

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hva som er inkludert i Microsoft Power BI-innholdet **Kostnadsregnskapsanalyse**. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="overview"></a>Oversikt

Power BI-innholdet **Kostnadsregnskapsanalyse** er ment for kostnadskontrollører eller andre som er ansvarlig for å utføre kostnadskontroll i en organisasjon. Det inkluderer hovedmål, for eksempel kostnader, størrelse og kostnadssats etter faktiske kostnader, budsjettkostnader og fleksible budsjettkostnader. Det bruker transaksjonsdata fra modulen **Kostnadsregnskap** og gir en aggregert visning av kostnadene for hele organisasjonen i en rapporteringsvaluta. Ledere kan filtrere dataene etter kostnadsobjekter for å utføre kostnadskontroll for sine organisasjonsenheter, selv om organisasjonen kan ha flere juridiske enheter.

Siden innholdet **Kostnadsregnskapsanalyse** fremhever avvik mellom faktiske kostnader og budsjetterte kostnader, kan ledere bli varslet om positive og negative trender for sine driftsenheter. Ledere kan drille ned til kostnadselementhierarkiene eller individuelle kostnadselementer. På denne måten kan ledere få detaljert innsikt i hvordan kostnadsavvik har oppstått, og deretter iverksette effektive tiltak.

**Kostnadsregnskapsanalyse**-innholdet lar regnskapsførere analysere hvordan kostnaden flyter gjennom kostnadsobjektene for hele organisasjonen.

Hvis du vil ha mer informasjon om kostnadsregnskap, se [startside for kostnadsregnskap](../../../finance/cost-accounting/cost-accounting-home-page.md).

Ved å definere tilgangsnivåsikkerhet i kostnadsregnskap og kombinere det med radnivåsikkerhet i Power BI, kan du gi alle kostnadsobjekteiere tilgang til **Kostregnskapsanalyse**-innhold for Power BI. Alle data i visualiseringen blir deretter filtrert basert på tilgangsnivået som styres i kostnadsregnskap. Hvis du vil vite mer om tilgangsnivåsikkerhet og radnivåsikkerhet, kan du se [Definere sikkerhet for Power BI-innhold for analyse av kostnadsregnskap](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innholdet
Du kan finne **Kostnadsregnskapsanalyse**-innhold for Power BI i det delte aktivabiblioteket i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon om hvordan du laster ned innholdet og implementerer det i organisasjonen, kan du se [Power BI-innhold i LCS fra Microsoft og partnerne](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/).

Pass på at du laster ned innholdet **Kostnadsregnskapsanalyse** som gjelder for versjonen av Microsoft Dynamics 365 du bruker.

> [!NOTE]
> KB 4011327 er en forutsetning for dette Power BI-innholdet. Når du logger deg på LCS, har du tilgang til KB her på <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mål som er inkludert i Power BI-innholdet
Innholdet inneholder et sett med rapportsider. Hver side består av et sett med mål som er visualisert som diagrammer, fliser og tabeller. Tabellen nedenfor gir en oversikt over visualiseringene i Power BI-innholdet **Kostnadsregnskapsanalyse**.

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
Følgende data brukes til å fylle ut rapportsidene i Power BI-innholdet **Kostnadsregnskapsanalyse**. Disse dataene vises som aggregerte mål som er oppsamlet i enhetslageret. Enhetslageret er en Microsoft SQL Server-database som er optimalisert for analyse. Hvis du vil ha mer informasjon, se [Power BI-integrering med enhetslager](power-bi-integration-entity-store.md).

De aggregerte nøkkelmålingene som du finner nedenfor, brukes som grunnlag for innholdet.

| Enhet                  | Aggregerte nøkkelmålinger | Datakilde for Dynamics 365      | Felt     | Beskrivelse                                        |
|-------------------------|---------------------------|-----------------------------------|-----------|----------------------------------------------------|
| Kostnadsregnskapsoppføringer | SUM(beløp)               | CAMDATAAggregatedCostEntry        | Beløp    | Beløpet i valutaen for kostnadsregnskapsfinans. |
| Statistiske oppføringer     | SUM(størrelse)            | CAMDATAAggregatedStatisctialEntry | Størrelse |                                                    |

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
