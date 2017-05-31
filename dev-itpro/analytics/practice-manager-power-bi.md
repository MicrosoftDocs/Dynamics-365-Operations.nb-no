---
title: Praksisleder for Power BI-innhold
description: "Dette emnet beskriver hva som er inkludert i Praksisleder for Power BI-innhold. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdspakken, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdspakken."
author: knelson
manager: AnnBe
ms.date: 04/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer/IT Pro
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.dyn365.intro: 2017/04/27
ms.dyn365.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0f2a1a9df8e5036c60b74b8a710e606b0b1e312a
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="practice-manager-power-bi-content"></a>Praksisleder for Power BI-innhold

[!include[banner](../includes/banner.md)]


Dette emnet beskriver hva som er inkludert i **Praksisleder** for Microsoft Power BI-innhold. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="overview"></a>Oversikt

**Praksisleder** for Power BI-innhold ble opprettet for praksisledere og prosjektledere. Den gir hovedmål som er knyttet til prosjektene som organisasjonen arbeider på. Instrumentbordet gir en oversikt over prosjekter og relaterte kunder. Et filter på rapportnivå kan brukes til å rapportere for bestemte juridiske enheter. Power BI-innholdet henter data fra aggregerte målinger for prosjektregnskap for Microsoft Dynamics 365 for Operations.

**Praksisleder** for Power BI-innholdet inneholder fem rapportsider: en oversiktsside og fire sider som inneholder detaljer om prosjektkostnader, omsetning, behandling av opptjent verdi og timemål som er delt opp på tvers av forskjellige dimensjoner.

Alle beløp i innholdet vises i systemvalutaen. Du kan definere systemvalutaen på **Systemparametere**-siden.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innhold

Du kan finne **Praksisleder** for Power BI-innhold for Power BI i det delte aktivabiblioteket i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon om hvordan du laster ned innholdspakken og kobler den til Dynamics 365 for Operations-data, kan du se [Power BI-innhold i LCS fra Microsoft og partnere](power-bi-content-microsoft-partners.md).

Hvis du vil se en demo som viser hvordan du implementerer Power BI-innholdet, kan du se [Power BI-innhold fra Microsoft og partnerne i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter som er inkludert i Power BI-innholdet

Tabellen nedenfor viser detaljer om mål som finnes på hver rapportside i **Praksisleder** for Power BI-innholdet.

| Rapportside                                          | Mål               |
|------------------------------------------------------|-----------------------------------------------|
| Instrumentbord  | Opprettede prosjekter<br>Estimerte prosjekter<br>Prosjekter som pågår<br>Antall prosjekter etter stadium<br>Antall prosjekter etter sted<br>Faktisk inntekt etter kunde<br>Budsjettert bruttofortjeneste etter prosjekt<br>Oversikt over administrasjon av opptjent verdi |
| Kostnad                                                 | Faktiske kostnader i forhold til budsjettkostnader etter måned<br>Faktiske kostnader i forhold til budsjettkostnader etter år<br>Faktiske kostnader i forhold til budsjettkostnader etter kategori<br>Faktisk kostnad etter transaksjonstype       |
| Omsetning                                              | Faktisk inntekt etter måned<br>Faktisk omsetning etter postnummer<br>Faktisk inntekt i forhold til budsjettinntekt etter kategori<br>Faktisk inntekt etter kundebransje        |
| EVM                                                  | Ytelsesindeks for kostnad og tidsplan etter prosjekt                 |
| Timeantall                                                | Faktiske fakturerbare brukte timer i forhold til faktiske fakturerbare belastningstimer i forhold til timer i budsjett<br>Faktiske fakturerbare brukte timer i forhold til faktiske fakturerbare belastningstimer etter prosjekt<br>Faktiske fakturerbare brukte timer i forhold til faktiske fakturerbare belastningstimer etter ressurs<br>Forholdet mellom faktiske fakturerbare timer per prosjekt<br>Forholdet mellom faktiske fakturerbare timer per ressurs |

Diagrammer og fliser for alle disse rapportene kan filtreres og festes på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Du kan også bruke funksjonen for eksport av underliggende data til å eksportere de underliggende dataene som oppsummeres i en effekt.

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter

Dynamics 365 for Operations-data brukes til å fylle ut rapportsider i **Praksisleder** for Power BI-innhold. Disse dataene representeres som aggregerte målinger som mellomlagres i enhetsbutikken, som er en Microsoft SQL-database som er optimalisert for analyse. Hvis du vil ha mer informasjon, se [Oversikt over Power BI-integrering med enhetslager](power-bi-integration-entity-store.md).

Delene nedenfor forklarer de samlede målene som brukes i hver enhet.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Enhet: ProjectAccountingCube_ActualHourUtilization
**Datakilde**: ProjEmplTrans

| Aggregerte nøkkelmålinger                | Felt                                | beskrivelse                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualBillableUtilizedHours              | Sum(ActualUtilizationBillableRate)   | Summen av faktiske fakturerbare brukte timer |
| ActualBillableBurdenHours                | Sum(ActualBurdenBillableRate)        | Summen av faktisk belastning (rate)             |

### <a name="entity-projectaccountingcubeactuals"></a>Enhet: ProjectAccountingCube_Actuals
**Datakilde**: ProjTransPosting

| Aggregerte nøkkelmålinger                | Felt                                | beskrivelse                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualRevenue                            |     Sum(ActualRevenue)               |  Summen av postert inntekt for alle transaksjoner |   
| ActualCost   |                             Sum(ActualCost)           |    Summen av bokførte kostnader for alle transaksjonstyper    |

### <a name="entity-projectaccountingcubecustomer"></a>Enhet: ProjectAccountingCube_Customer
**Datakilde**: CustTable

| Aggregerte nøkkelmålinger                | Felt                                | beskrivelse                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    Antall prosjekter        |   COUNTA(ProjectAccountingCube_Projects[PROJECTS])       |         Antall tilgjengelige prosjekter    |


### <a name="entity-projectaccountingcubeforecasts"></a>Enhet: ProjectAccountingCube_Forecasts
**Datakilde**: ProjTransBudget

| Aggregerte nøkkelmålinger                | Felt                                | beskrivelse                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    BudgetCost    |       Sum(BudgetCost)  |       Summen av estimerte kostnader for alle transaksjonstyper     |
|     BudgetRevenue    |         Sum(BudgetRevenue)    |    Summen av antatt påløpt/fakturert omsetning         |
|BudgetGrossMargin | Sum(BudgetGrossMargin) |Forskjellen mellom summen av total prognoseomsetning og summen av total prognosekostnad

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Enhet: ProjectAccountingCube_ProjectPlanCostsView
**Datakilde**: Prosjekt

| Aggregerte nøkkelmålinger                | Felt                                | beskrivelse                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|      PlannedCost      |        Sum(SumOfTotalCostPrice)   | Total kostpris i estimater for alle prosjekttransaksjonstypene med planlagte oppgaver |

### <a name="entity-projectaccountingcubeprojects"></a>Enhet: ProjectAccountingCube_Projects
**Datakilde**: Prosjekt

| Aggregerte nøkkelmålinger                | Felt                                | beskrivelse                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|   Indeks for kostnadsytelse  |ProjectAccountingCube_Projects[Opptjent verdi] / ProjectAccountingCube_Projects [totale faktiske kostnader for fullførte oppgaver] |     Beregning av total opptjent verdi delt på total faktisk kostnad|
|  Planlegg ytelse – indeks |ProjectAccountingCube_Projects[Opptjent verdi] / ProjectAccountingCube_Projects[totale planlagte kostnader for fullførte oppgaver]|Beregning av total opptjent verdi delt på total planlagt kostnad |
|Prosent av arbeid fullført |Prosent av arbeid fullført = ProjectAccountingCube_Projects [totale faktiske kostnader for fullførte oppgaver] / (ProjectAccountingCube_Projects [totale faktiske kostnader for fullførte oppgaver] + ProjectAccountingCube_Projects [totale planlagte kostnader for prosjektet] - ProjectAccountingCube_Projects [totale planlagte kostnader for fullførte oppgaver])|Total prosentandel av fullført arbeid basert på total faktisk kostnad for fullført oppgave og planlagte kostnader for prosjektet|
|Forholdet mellom faktiske fakturerbare timer per prosjekt|ProjectAccountingCube_Projects [totale faktiske fakturerbare brukte prosjekttimer] / (ProjectAccountingCube_Projects [totale faktiske fakturerbare brukte prosjekttimer] + ProjectAccountingCube_Projects [totale faktiske fakturerbare belastningstimer for prosjekt])|Totalt antall faktiske fakturerbare timer basert på brukte + belastning|
|Opptjent verdi|ProjectAccountingCube_Projects[totale planlagte kostnader for prosjektet] * ProjectAccountingCube_Projects[Prosent av arbeid fullført ]|Totale planlagte kostnader multiplisert med prosent av arbeid fullført|

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Enhet: ProjectAccountingCube_TotalEstimatedCosts 
**Datakilde**: ProjTable

| Aggregerte nøkkelmålinger                | Felt                                | beskrivelse                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| CompletedActivityPlannedCost  |  Sum(TotalCostPrice)  |   Total kostpris i estimater for alle prosjekttransaksjonstypene med fullførte oppgaver|

## <a name="additional-resources"></a>Tilleggsressurser

Her er noen nyttige koblinger som er knyttet til enheter og oppretting av Power BI-innhold:

- [Dataenheter](/dynamics365/operations/dev-itpro/data-entities/data-entities)
- [Opprette innholdspakker for organisasjonen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [Datamodellering med Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [Konfigurer Power BI-integrering for arbeidsområder](configure-power-bi-integration.md)

