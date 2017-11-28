---
title: Praksisleder for Power BI-innhold
description: "Dette emnet beskriver hva som er inkludert i Praksisleder for Power BI-innhold. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdet, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3462ef1bbde9a98ac6a7bc9a5c54e58ff98559c8
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="practice-manager-power-bi-content"></a>Praksisleder for Power BI-innhold

[!include[banner](../includes/banner.md)]

Dette emnet beskriver hva som er inkludert i **Praksisleder** for Microsoft Power BI-innhold. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="overview"></a>Oversikt

**Praksisleder** for Power BI-innhold ble opprettet for praksisledere og prosjektledere. Den gir hovedmål som er knyttet til prosjektene som organisasjonen arbeider på. Instrumentbordet gir en oversikt over prosjekter og relaterte kunder. Et filter på rapportnivå kan brukes til å rapportere for bestemte juridiske enheter. Dette Power BI-innholdet henter data fra aggregerte målinger av prosjektregnskapet.

**Praksisleder** for Power BI-innholdet inneholder fem rapportsider: en oversiktsside og fire sider som inneholder detaljer om prosjektkostnader, omsetning, behandling av opptjent verdi og timemål som er delt opp på tvers av forskjellige dimensjoner.

Alle beløp i innholdet vises i systemvalutaen. Du kan definere systemvalutaen på **Systemparametere**-siden.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innhold
Hvis du bruker Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017), vil **Praksisleder** for Power BI-innholdet vises i **Prosjektledelsens** arbeidsområde.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter som er inkludert i Power BI-innholdet

Tabellen nedenfor viser detaljer om mål som finnes på hver rapportside i **Praksisleder** for Power BI-innholdet.

| Rapportside       | Mål |
|-------------------|---------|
| Prosjektoversikt | <ul><li>Opprettede prosjekter</li><li>Estimerte prosjekter</li><li>Prosjekter som pågår</li><li>Antall prosjekter etter stadium</li><li>Antall prosjekter etter sted</li><li>Faktisk inntekt etter kunde</li><li>Budsjettert bruttofortjeneste etter prosjekt</li><li>Oversikt over administrasjon av opptjent verdi</li></ul> |
| Kostnad              | <ul><li>Faktiske kostnader i forhold til budsjettkostnader etter måned</li><li>Faktiske kostnader i forhold til budsjettkostnader etter år</li><li>Faktiske kostnader i forhold til budsjettkostnader etter kategori</li><li>Faktisk kostnad etter transaksjonstype</li></ul> |
| Omsetning           | <ul><li>Faktisk inntekt etter måned</li><li>Faktisk omsetning etter postnummer</li><li>Faktisk inntekt i forhold til budsjettinntekt etter kategori</li><li>Faktisk inntekt etter kundebransje</li></ul> |
| EVM               | Ytelsesindeks for kostnad og tidsplan etter prosjekt |
| Timeantall             | <ul><li>Faktiske fakturerbare brukte timer i forhold til faktiske fakturerbare belastningstimer i forhold til timer i budsjett</li><li>Faktiske fakturerbare brukte timer i forhold til faktiske fakturerbare belastningstimer etter prosjekt</li><li>Faktiske fakturerbare brukte timer i forhold til faktiske fakturerbare belastningstimer etter ressurs</li><li>Forholdet mellom faktiske fakturerbare timer per prosjekt</li><li>Forholdet mellom faktiske fakturerbare timer per ressurs</li></ul> |

Diagrammer og fliser for alle disse rapportene kan filtreres og festes på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Du kan også bruke funksjonen for eksport av underliggende data til å eksportere de underliggende dataene som oppsummeres i en effekt.

## <a name="extending-the-power-bi-content"></a>Utvide Power BI-innholdet
Hvis du bruker innholdspakkene som er tilgjengelige i Microsoft Dynamics Lifecycle Services (LCS), kan du gi personer som ikke logger på Microsoft Dynamics 365, gode analyser. Du kan endre disse innholdspakkene slik at de inneholder andre rapporter eller visuelle hjelpemidler, og deretter publisere dem på Power BI.com-leieren for analyse. 

Du kan finne **Praksisleder**-innholdet for Power BI i det delte aktivabiblioteket i LCS. Hvis du vil ha mer informasjon om hvordan du laster ned innholdet og implementerer det i organisasjonen, kan du se [Power BI-innhold i LCS fra Microsoft og partnerne](power-bi-content-microsoft-partners.md). Hvis du vil se en demo som viser hvordan du implementerer Power BI-innholdet, kan du se [Power BI-innhold fra Microsoft og partnerne i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

Pass på at du laster ned **Praksisleder**-innholdet som gjelder for versjonen av Dynamics 365 du bruker.

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter

Følgende data brukes til å fylle ut rapportsidene i **Praksisleder**-innholdet for Power BI. Disse dataene vises som aggregerte mål som er oppsamlet i enhetslageret. Enhetslageret er en Microsoft SQL Server-database som er optimalisert for analyse. Hvis du vil ha mer informasjon, se [Oversikt over Power BI-integrering med enhetslager](power-bi-integration-entity-store.md).

Delene nedenfor forklarer de samlede målene som brukes i hver enhet.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Enhet: ProjectAccountingCube_ActualHourUtilization
**Datakilde:** ProjEmplTrans

| Aggregerte nøkkelmålinger      | Felt                              | beskrivelse | 
|--------------------------------|------------------------------------|-------------|
| Faktiske fakturerbare brukte timer | Sum(ActualUtilizationBillableRate) | Summen av faktiske fakturerbare brukte timer |
| Faktiske fakturerbare belastningstimer   | Sum(ActualBurdenBillableRate)      | Summen av faktisk belastning (rate) |

### <a name="entity-projectaccountingcubeactuals"></a>Enhet: ProjectAccountingCube_Actuals
**Datakilde:** ProjTransPosting

| Aggregerte nøkkelmålinger | Felt              | beskrivelse | 
|---------------------------|--------------------|-------------|
| Faktisk omsetning            | Sum(ActualRevenue) | Summen av postert inntekt for alle transaksjoner |   
| Faktisk kostnad               | Sum(ActualCost)    | Summen av bokførte kostnader for alle transaksjonstyper |

### <a name="entity-projectaccountingcubecustomer"></a>Enhet: ProjectAccountingCube_Customer
**Datakilde:** CustTable

| Aggregerte nøkkelmålinger | Felt                                            | beskrivelse | 
|---------------------------|--------------------------------------------------|-------------|
| Antall prosjekter        | COUNTA(ProjectAccountingCube_Projects[PROJECTS]) | Antall tilgjengelige prosjekter |


### <a name="entity-projectaccountingcubeforecasts"></a>Enhet: ProjectAccountingCube_Forecasts
**Datakilde:** ProjTransBudget

| Aggregerte nøkkelmålinger | Felt                  | beskrivelse | 
|---------------------------|------------------------|-------------|
| Budsjettert kostnad               | Sum(BudgetCost)        | Summen av estimerte kostnader for alle transaksjonstyper |
| Budsjettert omsetning            | Sum(BudgetRevenue)     | Summen av antatt påløpt/fakturert omsetning  |
| Budsjettert bruttofortjeneste       | Sum(BudgetGrossMargin) | Forskjellen mellom summen av total prognoseomsetning og summen av total prognosekostnad |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Enhet: ProjectAccountingCube_ProjectPlanCostsView
**Datakilde:** Prosjekt

| Aggregerte nøkkelmålinger | Felt                    | beskrivelse | 
|---------------------------|--------------------------|-------------|
| Planlagt kostnad              | Sum(SumOfTotalCostPrice) | Total kostpris i estimater for alle prosjekttransaksjonstypene med planlagte oppgaver |

### <a name="entity-projectaccountingcubeprojects"></a>Enhet: ProjectAccountingCube_Projects
**Datakilde:** Prosjekt

| Aggregerte nøkkelmålinger    | Felt | beskrivelse | 
|------------------------------|-------|-------------|
| Indeks for kostnadsytelse       | ProjectAccountingCube_Projects[Opptjent verdi] / ProjectAccountingCube_Projects [totale faktiske kostnader for fullførte oppgaver] | Beregning av total opptjent verdi delt på total faktisk kostnad |
| Planlegg ytelse – indeks   | ProjectAccountingCube_Projects[Opptjent verdi] / ProjectAccountingCube_Projects[totale planlagte kostnader for fullførte oppgaver] | Beregning av total opptjent verdi delt på total planlagt kostnad |
| Prosent av arbeid fullført | Prosent av arbeid fullført = ProjectAccountingCube_Projects [totale faktiske kostnader for fullførte oppgaver] / (ProjectAccountingCube_Projects [totale faktiske kostnader for fullførte oppgaver] + ProjectAccountingCube_Projects [totale planlagte kostnader for prosjektet] - ProjectAccountingCube_Projects [totale planlagte kostnader for fullførte oppgaver]) | Total prosentandel av fullført arbeid basert på total faktisk kostnad for fullført oppgave og planlagte kostnader for prosjektet |
| Forholdet mellom faktiske fakturerbare timer   | ProjectAccountingCube_Projects [totale faktiske fakturerbare brukte prosjekttimer] / (ProjectAccountingCube_Projects [totale faktiske fakturerbare brukte prosjekttimer] + ProjectAccountingCube_Projects [totale faktiske fakturerbare belastningstimer for prosjekt]) | Totalt antall faktiske fakturerbare timer basert på brukte timer og belastningstimer |
| Opptjent verdi                 | ProjectAccountingCube_Projects[totale planlagte kostnader for prosjektet] * ProjectAccountingCube_Projects[Prosent av arbeid fullført ] | Totale planlagte kostnader multiplisert med prosent av arbeid fullført |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Enhet: ProjectAccountingCube_TotalEstimatedCosts 
**Datakilde:** ProjTable

| Aggregerte nøkkelmålinger       | Felt               | beskrivelse | 
|---------------------------------|---------------------|-------------|
| Planlagt kostnad for fullført aktivitet | Sum(TotalCostPrice) | Total kostpris i estimater for alle prosjekttransaksjonstypene med fullførte oppgaver |

