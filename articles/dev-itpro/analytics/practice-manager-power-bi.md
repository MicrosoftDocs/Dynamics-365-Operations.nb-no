---
title: Praksisleder for Power BI-innhold
description: "Dette emnet beskriver hva som er inkludert i Praksisleder for Power BI-innhold. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdet, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: KimANelson
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ProjManagementWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 7b2c13573aca2ceb0eca36cf4aeee80d2f56ab8a
ms.contentlocale: nb-no
ms.lasthandoff: 08/13/2018

---

# <a name="practice-manager-power-bi-content"></a>Praksisleder for Power BI-innhold

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hva som er inkludert i **Praksisleder** for Microsoft Power BI-innhold. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="overview"></a>Oversikt

**Praksisleder** for Power BI-innhold ble opprettet for praksisledere og prosjektledere. Den gir hovedmål som er knyttet til prosjektene som organisasjonen arbeider på. Instrumentbordet gir en oversikt over prosjekter og relaterte kunder. Et filter på rapportnivå kan brukes til å rapportere for bestemte juridiske enheter. Dette Power BI-innholdet henter data fra aggregerte målinger av prosjektregnskapet.

**Praksisleder** for Power BI-innholdet inneholder fem rapportsider: en oversiktsside og fire sider som inneholder detaljer om prosjektkostnader, omsetning, behandling av opptjent verdi og timemål som er delt opp på tvers av forskjellige dimensjoner.

Alle beløp i innholdet vises i systemvalutaen. Du kan definere systemvalutaen på **Systemparametere**-siden.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innhold

Power BI-innholdet **Praksisleder** vises i **Prosjektstyring**-arbeidsområdet.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter som er inkludert i Power BI-innholdet

Tabellen nedenfor viser detaljer om mål som finnes på hver rapportside i **Praksisleder** for Power BI-innholdet.

| Rapportside       | Mål |
|-------------------|---------|
| Prosjektoversikt | <ul><li>Opprettede prosjekter</li><li>Estimerte prosjekter</li><li>Prosjekter som pågår</li><li>Faktisk inntekt etter kunde</li><li>Budsjettert bruttofortjeneste etter prosjekt</li><li>Oversikt over administrasjon av opptjent verdi</li></ul> |
| Kostnad              | <ul><li>Faktiske kostnader i forhold til budsjettkostnader etter måned</li><li>Faktiske kostnader i forhold til budsjettkostnader etter år</li><li>Faktiske kostnader i forhold til budsjettkostnader etter kategori</li><li>Faktisk kostnad etter transaksjonstype</li></ul> |
| Omsetning           | <ul><li>Faktisk inntekt etter måned</li><li>Faktisk omsetning etter postnummer</li><li>Faktisk inntekt i forhold til budsjettinntekt etter kategori</li><li>Faktisk inntekt etter kundebransje</li></ul> |
| EVM               | Ytelsesindeks for kostnad og tidsplan etter prosjekt |
| Timeantall             | <ul><li>Faktiske fakturerbare brukte timer i forhold til faktiske fakturerbare belastningstimer i forhold til timer i budsjett</li><li>Faktiske fakturerbare brukte timer i forhold til faktiske fakturerbare belastningstimer etter prosjekt</li><li>Faktiske fakturerbare brukte timer i forhold til faktiske fakturerbare belastningstimer etter ressurs</li><li>Forholdet mellom faktiske fakturerbare timer per prosjekt</li><li>Forholdet mellom faktiske fakturerbare timer per ressurs</li></ul> |

Diagrammer og fliser for alle disse rapportene kan filtreres og festes på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Du kan også bruke funksjonen for eksport av underliggende data til å eksportere de underliggende dataene som oppsummeres i en effekt.

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter

Følgende data brukes til å fylle ut rapportsidene i **Praksisleder**-innholdet for Power BI. Disse dataene vises som aggregerte mål som er oppsamlet i enhetslageret. Enhetslageret er en Microsoft SQL Server-database som er optimalisert for analyse. Hvis du vil ha mer informasjon, se [Oversikt over Power BI-integrering med enhetslager](power-bi-integration-entity-store.md).

Delene nedenfor forklarer de samlede målene som brukes i hver enhet.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Enhet: ProjectAccountingCube\_ActualHourUtilization
**Datakilde:** ProjEmplTrans

| Aggregerte nøkkelmålinger      | Felt                              | beskrivelse |
|--------------------------------|------------------------------------|-------------|
| Faktiske fakturerbare brukte timer | Sum(ActualUtilizationBillableRate) | Summen av faktiske fakturerbare brukte timer |
| Faktiske fakturerbare belastningstimer   | Sum(ActualBurdenBillableRate)      | Summen av faktisk belastning (rate) |

### <a name="entity-projectaccountingcubeactuals"></a>Enhet: ProjectAccountingCube\_Actuals
**Datakilde:** ProjTransPosting

| Aggregerte nøkkelmålinger | Felt              | beskrivelse |
|---------------------------|--------------------|-------------|
| Faktisk omsetning            | Sum(ActualRevenue) | Summen av postert inntekt for alle transaksjoner |
| Faktisk kostnad               | Sum(ActualCost)    | Summen av bokførte kostnader for alle transaksjonstyper |

### <a name="entity-projectaccountingcubecustomer"></a>Enhet: ProjectAccountingCube\_Customer
**Datakilde:** CustTable

| Aggregerte nøkkelmålinger | Felt                                             | beskrivelse |
|---------------------------|---------------------------------------------------|-------------|
| Antall prosjekter        | COUNTA(ProjectAccountingCube\_Projects\[PROSJEKTER\]) | Antall tilgjengelige prosjekter |

### <a name="entity-projectaccountingcubeforecasts"></a>Enhet: ProjectAccountingCube\_Forecasts
**Datakilde:** ProjTransBudget

| Aggregerte nøkkelmålinger | Felt                  | beskrivelse |
|---------------------------|------------------------|-------------|
| Budsjettert kostnad               | Sum(BudgetCost)        | Summen av estimerte kostnader for alle transaksjonstyper |
| Budsjettert omsetning            | Sum(BudgetRevenue)     | Summen av antatt påløpt/fakturert omsetning |
| Budsjettert bruttofortjeneste       | Sum(BudgetGrossMargin) | Forskjellen mellom summen av total prognoseomsetning og summen av total prognosekostnad |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Enhet: ProjectAccountingCube\_ProjectPlanCostsView
**Datakilde:** Prosjekt

| Aggregerte nøkkelmålinger | Felt                    | beskrivelse |
|---------------------------|--------------------------|-------------|
| Planlagt kostnad              | Sum(SumOfTotalCostPrice) | Total kostpris i estimater for alle prosjekttransaksjonstypene med planlagte oppgaver |

### <a name="entity-projectaccountingcubeprojects"></a>Enhet: ProjectAccountingCube\_Projects
**Datakilde:** Prosjekt

| Aggregerte nøkkelmålinger    | Felt | beskrivelse |
|------------------------------|-------|-------------|
| Indeks for kostnadsytelse       | ProjectAccountingCube\_Projects\[Opptjent verdi\] ÷ ProjectAccountingCube\_Projects\[Totale faktiske kostnader for fullførte oppgaver\] | Beregning av total opptjent verdi delt på total faktisk kostnad |
| Planlegg ytelse – indeks   | ProjectAccountingCube\_Projects\[Opptjent verdi\] ÷ ProjectAccountingCube\_Projects\[Totale planlagte kostnader for fullførte oppgaver\] | Beregning av total opptjent verdi delt på total planlagt kostnad |
| Prosent av arbeid fullført | Prosent av arbeid fullført = ProjectAccountingCube\_Projects\[Totale faktiske kostnader for fullførte oppgaver\] ÷ (ProjectAccountingCube\_Projects\[Totale faktiske kostnader for fullførte oppgaver\] + ProjectAccountingCube\_Projects\[Totale planlagte kostnader for prosjektet\] – ProjectAccountingCube\_Projects\[Totale planlagte kostnader for fullførte oppgaver\]) | Total prosentandel av fullført arbeid basert på total faktisk kostnad for fullført oppgave og planlagte kostnader for prosjektet |
| Forholdet mellom faktiske fakturerbare timer   | ProjectAccountingCube\_Projects\[Totale faktiske fakturerbare brukte prosjekttimer\] ÷ (ProjectAccountingCube\_Projects\[Totale faktiske fakturerbare brukte prosjekttimer\] + ProjectAccountingCube\_Projects\[Totale faktiske fakturerbare belastningstimer for prosjekt\]) | Totalt antall faktiske fakturerbare timer basert på brukte timer og belastningstimer |
| Opptjent verdi                 | ProjectAccountingCube\_Projects\[Totale planlagte kostnader for prosjektet\] × ProjectAccountingCube\_Projects\[Prosent av arbeid fullført\] | Totale planlagte kostnader multiplisert med prosent av arbeid fullført |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Enhet: ProjectAccountingCube\_TotalEstimatedCosts 
**Datakilde:** ProjTable

| Aggregerte nøkkelmålinger       | Felt               | beskrivelse |
|---------------------------------|---------------------|-------------|
| Planlagt kostnad for fullført aktivitet | Sum(TotalCostPrice) | Total kostpris i estimater for alle prosjekttransaksjonstypene med fullførte oppgaver |

