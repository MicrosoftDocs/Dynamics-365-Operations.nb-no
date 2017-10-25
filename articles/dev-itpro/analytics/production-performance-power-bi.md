---
title: Produksjonsytelse for Power BI-innhold
description: "Dette emnet beskriver hva som er inkludert i Produksjonsytelse-innhold for Power BI. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: b49cfe39732a450e4723419c50d8bcc3d64b7ec9
ms.openlocfilehash: f0551a9b58b58f6bdac433b88f44919428c14426
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="production-performance-power-bi-content"></a>Produksjonsytelse for Power BI-innhold

[!include[banner](../includes/banner.md)]

Dette emnet beskriver hva som er inkludert i **Produksjonsytelse**-innhold for Microsoft Power BI. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="overview"></a>Oversikt

**Produksjonsytelse**-innholdet for Power BI er ment for produksjonsledere eller personer i organisasjonen som er ansvarlig for produksjonskontroll.

Med de inkluderte rapportene kan du bruke Power BI til å overvåke ytelsen til produksjonsoperasjoner med hensyn til rask utføring, kvalitet og kostnad. Rapportene bruker transaksjonsdata fra produksjonsordrer og partiordrer, og gir både en aggregert visning av bedriftsomfattende produksjonsmål og en analyse av mål etter produkt og ressurs.

Power BI-innholdet uthever organisasjonens evne til å fullføre produksjonen til planlagt tid og i sin helhet. Fremtidig ytelse vises basert på produksjonsplanene. Omfattende rapporter gir detaljert innsikt i produktmangler som er forårsaket av produksjon, og også feilsatsene for ressurser og operasjoner.

Dette Power BI-innholdet lar deg også analysere produksjonsavvik. Produksjonsavvik beregnes som differansen mellom estimerte kostnader og faktiske kostnader. Produksjonsavvik beregnes når produksjonsordrer eller partiordrer når **avsluttet** status.

**Produksjonsytelse** for Power BI-innhold inneholder data som kommer fra produksjonsordrer og partiordrer. Rapportene inneholder ikke data som er knyttet til kanban-produksjoner.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innhold
Hvis du bruker Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017), vil **Produksjonsytelse** for Power BI-innholdet vises på siden **Produksjonsytelse** (**Produksjonskontroll** > **Forespørsler og rapporter** > **Analyse av produksjonsytelse** > **Produksjonsytelse**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mål som er inkludert i Power BI-innholdet

**Produksjonsytelse** for Power BI-innhold omfatter et sett med rapportsider. Hver side består av et sett med mål som er visualisert som diagrammer, fliser og tabeller.

Tabellen nedenfor gir en oversikt over effektene som er inkludert.

| Rapportside                                | Diagrammer                                               | Fliser |
|--------------------------------------------|------------------------------------------------------|-------|
| Produksjonsytelse                     | <ul><li>Antall produksjoner etter dato</li><li>Antall produksjoner etter produkt og varegruppe</li><li>Antall planlagte produksjoner etter dato</li><li>10 dårligste produkter etter til planlagt tid og i sin helhet</li></ul> | <ul><li>Totalt antall ordrer</li><li>Prosent til planlagt tid og i sin helhet</li><li>Ufullstendig %</li><li>For tidlig %</li><li>For sent %</li></ul> |
| Mangler etter produkt                         | <ul><li>Antall defekte (spm) etter dato</li><li>Antall defekte (spm) etter produkt og varegruppe</li><li>Antall produsert etter dato</li><li>Topp 10 produkter etter effektiv sats</li></ul> | <ul><li>Antall defekte (spm)</li><li>Defekt antall</li><li>Totalt antall</li></ul> |
| Manglertrend etter produkt                   | Antall defekte (spm) etter antall produsert | Antall defekte (spm) |
| Defekte etter ressurs                        | <ul><li>Antall defekte (spm) etter dato</li><li>Antall defekte (spm) etter ressurs og sted</li><li>Antall defekte (spm) etter operasjon</li><li>Topp 10 ressurser etter antall defekte</li></ul> | Defekt antall |
| Manglertrend etter ressurs                  | Antall defekte (spm) etter antall behandlet | |
| Produksjonsprisavvik for etterkalkulering av jobbordre | <ul><li>Produksjonsavvik etter dato og kostgruppetype</li><li>Produksjonsavvik etter sted og kostgruppetype</li><li>Topp 10 produkter med ugunstige produksjonsavvik</li><li>Topp 10 ugunstige produksjonsavvik etter ressurs</li></ul> | <ul><li>Realisert kostnad</li><li>Produksjonsavvik</li><li>Produksjonsavvik %</li></ul> |

## <a name="extending-the-power-bi-content"></a>Utvide Power BI-innholdet
Hvis du bruker innholdspakkene som er tilgjengelige i Microsoft Dynamics Lifecycle Services (LCS), kan du gi personer som ikke logger på Microsoft Dynamics 365, gode analyser. Du kan endre disse innholdspakkene slik at de inneholder andre rapporter eller visuelle hjelpemidler, og deretter publisere innholdspakkene på Power BI.com-leieren for analyse.

Du kan finne **Produksjonsytelse**-innholdet for Power BI i det delte aktivabiblioteket i LCS. Hvis du vil ha mer informasjon om hvordan du laster ned innholdet og implementerer det i organisasjonen, kan du se [Power BI-innhold i LCS fra Microsoft og partnerne](power-bi-content-microsoft-partners.md). Hvis du vil se en demo som viser hvordan du implementerer Power BI-innholdet, kan du se [Power BI-innhold fra Microsoft og partnerne i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

Pass på at du laster ned **Produksjonsytelse**-innholdet som gjelder for versjonen av Dynamics 365 du bruker.

> [!NOTE]
> Hvis du bruker oppdateringen for Microsoft Dynamics 365 for Operations versjon 1611, er KB 4011327 en forutsetning for dette Power BI-innholdet. Når du logger deg på LCS, har du tilgang til KB-artikkelen på https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter

Følgende data brukes for rapportsidene i **Produksjonsytelse**-innholdet for Power BI. Disse dataene vises som aggregerte mål som er oppsamlet i enhetslageret. Enhetslageret er en Microsoft SQL Server-database som er optimalisert for analyse. Hvis du vil vite mer om enhetslageret, kan du se [Power BI-integrering med enhetslager](power-bi-integration-entity-store.md).

Tabellen nedenfor viser nøkkelmålingene som brukes som grunnlag for Power BI-innholdet.

| Enhet                   | Aggregerte nøkkelmålinger  | Datakilde for Finance and Operations | Felt              |
|--------------------------|-----------------------------|----------------------------------------|--------------------|
| CostCalculation          | CostAmount                  | ProdCalcTransExpanded                  | CostAmount         |
| CostCalculation          | CostMarkup                  | ProdCalcTransExpanded                  | CostMarkup         |
| CostCalculation          | ActualCostAmount            | ProdCalcTransExpanded                  | RealCostAmount     |
| CostCalculation          | RealCostAdjustment          | ProdCalcTransExpanded                  | RealCostAdjustment |
| RouteTransactions        | ErrorQuantity               | ProdRouteTransExpanded                 | QtyError           |
| RouteTransactions        | GoodQuantity                | ProdRouteTransExpanded                 | QtyGood            |
| ProductionOrder          | DaysDelayed                 | ProdTableExpanded                      | DaysDelayed        |
| ProductionOrder          | LeadTime                    | ProdTableExpanded                      | LeadTime           |
| ProductionOrder          | PlannedLeadTime             | ProdTableExpanded                      | PlannedLeadTime    |
| ProductionOrder          | ProductionOrderCount        | ProdTableExpanded                      |                    |
| CoproductCostCalculation | CoproductCostAmount         | PmfCoByProdCalcTransExpanded           | CostAmount         |
| CoproductCostCalculation | CoproductCostMarkup         | PmfCoByProdCalcTransExpanded           | CostMarkup         |
| CoproductCostCalculation | CoproductRealCostAdjustment | PmfCoByProdCalcTransExpanded           | RealCostAdjustment |
| CoproductCostCalculation | CoproductActualCostAmount   | PmfCoByProdCalcTransExpanded           | RealCostAmount     |

Tabellen nedenfor viser hvordan de aggregerte nøkkelmålingene brukes til å opprette flere beregnede målinger i datasettet for innholdet.

| Mål                  | Slik beregnes målet |
|--------------------------|-------------------------------|
| Produksjonsavvik, %   | SUM('Produksjonsavvik'[produksjonsavvik]) / SUM('Produksjonsavvik'[estimert kostnad]) |
| Alle planlagte ordrer       | COUNTROWS('Planlagt produksjonsordre') |
| For tidlig                    | COUNTROWS(FILTER('Planlagt produksjonsordre', 'Planlagt produksjonsordre'[Planlagt sluttdato] \< 'Planlagt produksjonsordre'[Behovsdato])) |
| For sent                     | COUNTROWS(FILTER('Planlagt produksjonsordre', 'Planlagt produksjonsordre'[Planlagt sluttdato] \> 'Planlagt produksjonsordre'[Behovsdato])) |
| Til planlagt tid                  | COUNTROWS(FILTER('Planlagt produksjonsordre', 'Planlagt produksjonsordre'[Planlagt sluttdato] = 'Planlagt produksjonsordre'[Behovsdato])) |
| Til planlagt tid                | IF ( 'Planlagt produksjonsordre'[til planlagt tid] \<\> 0, 'Planlagt produksjonsordre'[til planlagt tid], IF ('Planlagt produksjonsordre'[Alle planlagte ordrer] \<\> 0, 0, BLANK()) ) / 'Planlagt produksjonsordre'[Alle planlagte ordrer] |
| Fullført                | COUNTROWS(FILTER('Produksjonsordre', 'Produksjonsordre'[Er RAF'ed] = TRUE)) |
| Antall defekte (spm)     | IF( 'Produksjonsordre'[Totalt antall] = 0, BLANK(), (SUM('Produksjonsordre'[Defekt antall]) / 'Produksjonsordre'[Totalt antall]) \* 1000000) |
| Forsinket produksjon  | 'Produksjonsordre' [For sent \#] / 'Produksjonsordre'[Fullført] |
| For tidlig og i sin helhet          | COUNTROWS(FILTER('Produksjonsordre', 'Produksjonsordre'[Er i sin helhet] = TRUE && 'Produksjonsordre'[Er for tidlig] = TRUE)) |
| For tidlig \#                 | COUNTROWS(FILTER('Produksjonsordre', 'Produksjonsordre'[Er for tidlig] = TRUE)) |
| For tidlig %                  | IFERROR( IF('Produksjonsordre'[For tidlig \#] \<\> 0, 'Produksjonsordre'[For tidlig \#], IF('Produksjonsordre'[Totalt antall ordrer] = 0, BLANK(), 0)) / 'Produksjonsordre'[Totalt antall ordrer], BLANK()) |
| Ufullstendig               | COUNTROWS(FILTER('Produksjonsordre', 'Produksjonsordre'[Er i sin helhet] = FALSE && 'Produksjonsordre'[Er RAF'ed] = TRUE)) |
| Ufullstendig %             | IFERROR( IF('Produksjonsordre'[Ufullstendig] \<\> 0, 'Produksjonsordre'[Ufullstendig], IF('Produksjonsordre'[Totalt antall ordrer] = 0, BLANK(), 0)) / 'Produksjonsordre'[Totalt antall ordrer], BLANK()) |
| Er forsinket               | 'Produksjonsordre'[Er RAF'ed] = TRUE && 'Produksjonsordre'[Forsinket verdi] = 1 |
| Er tidlig                 | 'Produksjonsordre'[Er RAF'ed] = TRUE && 'Produksjonsordre'[Antall dager forsinket] \< 0 |
| Er i sin helhet               | 'Produksjonsordre'[Antall korrekte] \>= 'Produksjonsordre'[Planlagt antall] |
| Er RAF'ed                | 'Produksjonsordre'[Produksjonsstatusverdi] = 5 \|\| 'Produksjonsordre'[Produksjonsstatusverdi] = 7 |
| For sent og i sin helhet           | COUNTROWS(FILTER('Produksjonsordre', 'Produksjonsordre'[Er i sin helhet] = TRUE && 'Produksjonsordre'[Er forsinket] = TRUE)) |
| For sent \#                  | COUNTROWS(FILTER('Produksjonsordre', 'Produksjonsordre'[Er forsinket] = TRUE)) |
| For sent %                   | IFERROR( IF('Produksjonsordre'[For sent \#] \<\> 0, 'Produksjonsordre'[For sent \#], IF('Produksjonsordre'[Totalt antall ordrer] = 0, BLANK(), 0)) / 'Produksjonsordre'[Totalt antall ordrer], BLANK()) |
| Til planlagt tid og i sin helhet        | COUNTROWS(FILTER('Produksjonsordre', 'Produksjonsordre'[Er i sin helhet] = TRUE && 'Produksjonsordre'[Er forsinket] = FALSE && 'Produksjonsordre'[Er for tidlig] = FALSE)) |
| Prosent til planlagt tid og i sin helhet      | IFERROR( IF('Produksjonsordre'[Til planlagt tid og i sin helhet] \<\> 0, 'Produksjonsordre'[Til planlagt tid og i sin helhet], IF('Produksjonsordre'[Fullført] = 0, BLANK(), 0)) / 'Produksjonsordre'[Fullført], BLANK()) |
| Totalt antall ordrer             | COUNTROWS('Produksjonsordre') |
| Totalt antall           | SUM('Produksjonsordre'[Antall korrekte]) + SUM('Produksjonsordre'[Defekt antall]) |
| Antall defekte (spm)        | IF( 'Rutetransaksjoner'[Behandlet antall] = 0, BLANK(), (SUM('Rutetransaksjoner'[Defekt antall]) / 'Rutetransaksjoner'[Behandlet antall]) \* 1000000) |
| Antall defekte kombinert (spm) | IF( 'Rutetransaksjoner'[Totalt antall kombinert] = 0, BLANK(), (SUM('Rutetransaksjoner'[Defekt antall]) / 'Rutetransaksjoner'[Totalt antall kombinert]) \* 1000000) |
| Behandlet antall       | SUM('Rutetransaksjoner'[Antall korrekte]) + SUM('Rutetransaksjoner'[Defekt antall]) |
| Totalt antall kombinert     | SUM('Produksjonsordre'[Antall korrekte]) + SUM('Rutetransaksjoner'[Defekt antall]) |

Tabellen nedenfor viser nøkkeldimensjonene som brukes som filtre for å dele opp de aggregerte målingene, slik at du kan få flere detaljer og dypere analytisk innsikt.

| Enhet                    | Eksempler på attributter                                        |
|---------------------------|---------------------------------------------------------------|
| Rapportert som ferdigmeldt dato | Fullført dato (Ferdigmeld), måned og årsforskyvning                 |
| Avsluttet dato                | Avsluttet måned forskyvning og måned                                  |
| Behovsdato          | Behovsdato måned forskyvning og behovsdato            |
| Rutetransaksjonsdato    | Rutetransaksjonsmåned forskyvning og dato                       |
| Siter                     | Område-ID, områdenavn, delstat og by                          |
| Enheter                  | ID og navn                                                   |
| Ressurser                 | Ressurs-ID, ressursnavn, ressurstype og ressursgruppe |
| Produkter                  | Produktnummer, produktnavn, vare-ID og varegruppe         |

## <a name="additional-resources"></a>Tilleggsressurser

Her er noen nyttige koblinger som er knyttet til enheter og oppretting av Power BI-innhold:

- [Dataenheter](../data-entities/data-entities.md)
- [Opprette innholdspakker for organisasjonen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [Datamodellering med Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [Legge til Power BI-fliser i arbeidsområder](configure-power-bi-integration.md)
