---
title: Kostnadsbehandling-innhold for Power BI
description: Dette emnet beskriver hva som er inkludert i Kostnadsbehandling-innhold for Power BI.
author: YuyuScheller
manager: AnnBe
ms.date: 02/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b167d7577823bbc88d8e64952333110f9a652b64
ms.openlocfilehash: 1f552e1ee0286326e3a2a8bb6a7bfb84df53b45d
ms.contentlocale: nb-no
ms.lasthandoff: 02/02/2018

---

# <a name="cost-management-power-bi-content"></a>Kostnadsbehandling-innhold for Power BI

[!include[banner](../includes/banner.md)]

> [Merknad] Denne innholdspakken er avskrevet slik det står i [Power BI-innholdspakker som er publisert på PowerBI.com](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features#power-bi-content-packs-published-to-powerbicom).


Dette emnet beskriver hva som er inkludert i Kostnadsbehandling-innhold for Power BI. 

**Kostnadsbehandling-innhold** for Microsoft Power BI er ment for lager regnskapsførere, revisorer eller personer i organisasjonen som er ansvarlig for lageret. **Kostnadsbehandling-innhold** for Power BI gir ledere innsikt i beholdning og VIA-lager, og hvordan kostnadsflyten går gjennom dem etter kategori over tid. Informasjonen kan også brukes som et detaljert supplement til regnskapsoppgjøret.

## <a name="key-measures"></a>Nøkkelmål

+ Startsaldo
+ Sluttsaldo
+ Netto endring
+ Nettoendring i %
+ Aldersfordeling

## <a name="key-performance-indicators"></a>Nøkkelytelsesindikatorer
+ Beholdningsomsetning
+ Lagerpresisjon

Den primære datakilden for CostAggregatedCostStatementEntryEntity er CostStatementCache-tabellen. Denne tabellen håndteres av rammeverket for hurtigbuffer for datasett. Tabellen oppdateres hvert døgn som standard, men du kan aktivere manuelle oppdateringer i databufferkonfigurasjonen. Deretter kan du gjøre en manuell oppdatering i arbeidsområdet **Kostnadsstyring** eller **Kostnadsanalyse**. Når oppdateringen av CostStatementCache er kjørt, må du oppdatere OData-koblingen på Power BI.com for å se de oppdaterte dataene på området. Avviksmålene (innkjøp, produksjon) målene i dette Power BI-innholdet gjelder bare for varer som evalueres av lagermodellen med standard kostpris. Produksjonsavvik beregnes som differansen mellom aktive kostnader og faktiske kostnader. Produksjonsavvik beregnes når produksjonsordren har statusen **Avsluttet**. Hvis du vil ha mer informasjon om produksjonsavvikstyper og hvordan hver type beregnes, se [Om å analysere avvik for en fullført produksjonsordre](https://technet.microsoft.com/en-us/library/gg242850.aspx).


## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mål som er inkludert i Power BI-innholdet
Innholdet inneholder et sett med rapportsider. Hver side består av et sett med mål som er visualisert som diagrammer, fliser og tabeller. Tabellen nedenfor gir en oversikt over visualiseringer i Power BI-innholdet **Kostnadsbehandling**.

| Rapportside | Diagrammer | Titler |
|---|---|---|
|Samlet lagerbeholdning (standard etter gjeldende periode) |Presisjon |Lagermål:<br>Beholdning – sluttsaldo<br>Beholdning – nettoendring<br>Beholdning – nettoendring i %<br>|
| |Beholdningsomsetning | |
| |Beholdning – sluttsaldo etter ressursgruppe | |
| |Beholdning – nettoendring etter kategorinavn nivå 1 og kategorinavn nivå 2| |
| |Kjøpsavvik etter ressursgruppe og kategorinavn på nivå 3 | |
|Beholdning etter område (standard etter gjeldende periode) |Beholdning – sluttsaldo etter områdenavn og ressursgruppe | |
| |Beholdningsomsetning etter områdenavn og ressursgruppe | |
| |Beholdning – sluttsaldo etter sted og ressursgruppe | |
|Beholdning etter ressursgruppe (standard etter gjeldende periode) |Lagermål | |
| |Lagerpresisjon etter beløp etter ressursgruppe | |
| |Beholdningsomsetning etter beløp etter ressursgruppe | |
|Lager YOY (standard gjeldende år i forhold til fjoråret) |Lagermål | |
| |Lager-KPI-er:<br>Beholdningsomsetning<br>Lagerpresisjon | |
| |Beholdning – sluttsaldo etter år og ressursgruppe | |
| |Kjøpsavvik etter år og kategorinavn på nivå 3 | |
|Aldersfordeling for lager (standard etter inneværende år) |Aldersfordeling for lager etter kvartal og ressursgruppe | |
| |Aldersfordeling for lager etter kvartal og områdenavn | |
|Samlet VIA (standard etter gjeldende periode) |VIA-nettoendring etter kategorinavn nivå 1 og kategorinavn nivå 2 |Arbeid som pågår (VIA)-mål:<br>VIA-sluttsaldo<br>VIA-nettoendring<br>VIA-nettoendring i %<br> |
| |Produksjonsavvik etter ressursgruppe og kategorinavn på nivå 3 | |
| |VIA-nettoendring etter ressursgruppe | |
|VIA etter område (standard etter gjeldende periode) |Arbeid som pågår (VIA)-mål | |
| |VIA-nettoendring etter områdenavn og kategorinavn nivå 2 | |
| |Produksjonsavvik etter områdenavn og kategorinavn på nivå 3 | |

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Finance and Operations-data brukes til å fylle ut rapportsider i Power BI-innholdet **Kostnadsstyring**. Disse dataene representeres som aggregerte målinger som mellomlagres i enhetsbutikken, som er en Microsoft SQL-database som er optimalisert for analyse. Hvis du vil ha mer informasjon, se [Oversikt over Power BI-integrering med enhetslager](power-bi-integration-entity-store.md). De aggregerte nøkkelmålingene som du finner nedenfor, brukes som grunnlag for innholdet.

| Enhet            | Aggregerte nøkkelmålinger | Datakilde for Finance and Operations | Felt             | beskrivelse                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Oppgaveoppføringer | Netto endring                | CostAggregatedCostStatementEntryEntity      | sum(\[Beløp\])   | Beløp i regnskapsvalutaen |
| Oppgaveoppføringer | Endring i nettoantall       | CostAggregatedCostStatementEntryEntity      | sum(\[Antall\]) |                                   |

Tabellen nedenfor viser hvordan de aggregerte nøkkelmålingene brukes til å opprette flere beregnede målinger i datasettet for innholdet.

| Mål                                 | Slik beregnes målet                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Startsaldo                       | \[Sluttsaldo\]-\[Nettoendring\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Startsaldoantall              | \[Sluttsaldoantall\]-\[Endring i nettoantall\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Sluttsaldo                          | CALCULATE(SUM(\[Beløp\]), FILTER(ALLEXCEPT('Økonomiske kalendere', 'Økonomiske kalendere'\[LedgerRecId\], 'enheter'\[ID\], 'enheter'\[Navn\], 'Finanskontoer'\[Valuta\], 'Finanskontoer'\[Beskrivelse\], 'Finanskontoer'\[Navn\]), 'Økonomiske kalendere'\[Dato\] &lt;= MAX('Økonomiske kalendere'\[Dato\])))                                                                                                                                                                                           |
| Sluttsaldoantall                 | CALCULATE(SUM(\[Antall\]), FILTER(ALLEXCEPT('Økonomiske kalendere', 'Økonomiske kalendere'\[LedgerRecId\], 'enheter'\[ID\], 'enheter'\[Navn\], 'Finanskontoer'\[Valuta\], 'Finanskontoer'\[Beskrivelse\], 'Finanskontoer'\[Navn\]), 'Økonomiske kalendere'\[Dato\] &lt;= MAX('Økonomiske kalendere'\[Dato\])))                                                                                                                                                                                         |
| Startsaldo for beholdning             | CALCULATE(\[Startsaldo\], 'Oppgaveoppføringer'\[Setningstype\] = "Beholdning")                                                                                                                                                                                                                                                                                                                                                                                      |
| Beholdning – sluttsaldo                | CALCULATE(\[Sluttsaldo\], 'Oppgaveoppføringer'\[Setningstype\] = "Beholdning")                                                                                                                                                                                                                                                                                                                                                                                         |
| Beholdning – nettoendring                    | CALCULATE(\[Nettoendring\], 'Oppgaveoppføringer'\[Setningstype\] = "Beholdning")                                                                                                                                                                                                                                                                                                                                                                                             |
| Beholdning – endring i nettoantall           | CALCULATE(\[Endring i nettoantall\], 'Oppgaveoppføringer'\[Setningstype\] = "Beholdning")                                                                                                                                                                                                                                                                                                                                                                                    |
| Beholdning – nettoendring i %                  | IF(\[Beholdning – sluttsaldo\] = 0, 0, \[Beholdning – nettoendring\] / \[Beholdning – sluttsaldo\])                                                                                                                                                                                                                                                                                                                                                                           |
| Beholdningsomsetning etter beløp                | if(OR(\[Beholdning – gjennomsnittlig saldo\] &lt;= 0, \[Beholdning – solgte eller forbrukte avganger\] &gt;= 0), 0, ABS(\[Beholdning – solgte eller forbrukte avganger\])/\[Beholdning – gjennomsnittlig saldo\])                                                                                                                                                                                                                                                                                                  |
| Beholdning – gjennomsnittlig saldo               | (\[Beholdning – sluttsaldo\] + \[Beholdning – startsaldo\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Beholdning – solgte eller forbrukte avganger       | \[Solgt lagerbeholdning\] + \[Beholdning – solgte eller forbrukte avganger\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Beholdning – solgte eller forbrukte avganger        | CALCULATE(\[Beholdning – nettoendring\], 'Oppgaveoppføringer'\[Kategorinavn - nivå 2\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Solgt lagerbeholdning                          | CALCULATE(\[Beholdning – nettoendring\], 'Oppgaveoppføringer'\[Kategorinavn - nivå 2\_\] = "Solgt")                                                                                                                                                                                                                                                                                                                                                                             |
| Lagerpresisjon etter beløp            | IF(\[Beholdning – sluttsaldo\] &lt;= 0, IF(OR(\[Beholdning – opptelt beløp\] &lt;&gt; 0, \[Beholdning – sluttsaldo\] &lt; 0), 0, 1), MAX(0, (\[Beholdning – sluttsaldo\] - ABS(\[Beholdning –\]))/\[Beholdning – sluttsaldo\]))                                                                                                                                                                                                                              |
| Beholdning – opptelt beløp                | CALCULATE(\[Beholdning – nettoendring\], 'Oppgaveoppføringer'\[Kategorinavn - nivå 3\_\] = "Opptelling")                                                                                                                                                                                                                                                                                                                                                                         |
| Aldersfordeling for lager                         | if(ISBLANK(max('Økonomiske kalendere'\[Dato\])), tom(), MAX(0, MIN(\[Aldersfordeling for lager – antall mottak\], \[Aldersfordeling for lager – sluttsaldoantall\] - \[Aldersfordeling for lager – antall mottak i fremtiden\]))) \* \[Beholdning – gj.sn. enhetskostnad\]                                                                                                                                                                                                                                |
| Aldersfordeling for lager – antall mottak       | IF(\[minDate\] = \[minDateAllSelected\], CALCULATE(\[Beholdning – endring i nettoantall\], 'Oppgaveoppføringer'\[Antall\] &gt; 0, FILTER(ALLEXCEPT('Økonomiske kalendere', 'Økonomiske kalendere'\[LedgerRecId\], 'enheter'\[ID\], 'enheter'\[Navn\], 'Finanskontoer'\[Valuta\], 'Finanskontoer'\[Beskrivelse\], 'Finanskontoer'\[Navn\]), 'Økonomiske kalendere'\[Dato\] &lt;= MAX('Økonomiske kalendere'\[Dato\]))), CALCULATE(\[Beholdning – endring i nettoantall\], 'Oppgaveoppføringer'\[Antall\] &gt; 0)) |
| Aldersfordeling for lager – sluttsaldoantall | \[Aldersfordeling for lager – sluttsaldoantall\] + CALCULATE(\[Beholdning – endring i nettoantall\], FILTER(ALLEXCEPT('Økonomiske kalendere', 'Økonomiske kalendere'\[LedgerRecId\], 'enheter'\[ID\], 'enheter'\[Navn\], 'Finanskontoer'\[Valuta\], 'Finanskontoer'\[Beskrivelse\], 'Finanskontoer'\[Navn\]), 'Økonomiske kalendere'\[Dato\] &gt; max('Økonomiske kalendere'\[Dato\]) ))                                                                                                                                 |
| Aldersfordeling for lager – mottak i fremtiden  | CALCULATE(\[Beholdning – nettoendring\], 'Oppgaveoppføringer'\[Beløp\] &gt; 0, FILTER(ALLEXCEPT('Økonomiske kalendere', 'Økonomiske kalendere'\[LedgerRecId\], 'enheter'\[ID\], 'enheter'\[Navn\], 'Finanskontoer'\[Valuta\], 'Finanskontoer'\[Beskrivelse\], 'Finanskontoer'\[Navn\]), 'Økonomiske kalendere'\[Dato\] &gt; MAX('Økonomiske kalendere'\[Dato\])))                                                                                                                                             |
| Beholdning – gj.sn. enhetskostnad                 | CALCULATE(\[Beholdning – sluttsaldo\] / \[Aldersfordeling for lager – sluttsaldoantall\],ALLEXCEPT('Økonomiske kalendere', 'Økonomiske kalendere'\[LedgerRecId\], 'enheter'\[ID\], 'enheter'\[Navn\], 'Finanskontoer'\[Valuta\], 'Finanskontoer'\[Beskrivelse\], 'Finanskontoer'\[Navn\]))                                                                                                                                                                                                                 |
| Kjøpsavvik                      | CALCULATE(SUM(\[Beløp\]), 'Oppgaveoppføringer'\[Kategorinavn - nivå 2\_\] = "Fremskaffet", 'Oppgaveoppføringer'\[Setningstype\] = "Avvik")                                                                                                                                                                                                                                                                                                                              |
| VIA-startsaldo                   | CALCULATE(\[Startsaldo\], 'Oppgaveoppføringer'\[Setningstype\] = "VIA")                                                                                                                                                                                                                                                                                                                                                                                            |
| VIA-sluttsaldo                      | CALCULATE(\[Sluttsaldo\], 'Oppgaveoppføringer'\[Setningstype\] = "VIA")                                                                                                                                                                                                                                                                                                                                                                                               |
| VIA-nettoendring                          | CALCULATE(\[Nettoendring\], 'Oppgaveoppføringer'\[Setningstype\] = "VIA")                                                                                                                                                                                                                                                                                                                                                                                                   |
| VIA-nettoendring i %                        | IF(\[VIA-sluttsaldo\] = 0, 0, \[VIA-nettoendring\] / \[VIA-sluttsaldo\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Produksjonsavvik                    | CALCULATE(SUM(\[Beløp\]), 'Oppgaveoppføringer'\[Kategorinavn - nivå 2\_\] = "ManufacturedCost", 'Oppgaveoppføringer'\[Setningstype\] = "Avvik")                                                                                                                                                                                                                                                                                                                      |
| Kategorinavn - nivå 1                 | switch(\[Kategorinavn - nivå 1\_\], "Ingen", "Ingen", "NetSourcing", "Netto leverandører", "NetUsage", "Nettobruk", "NetConversionCost", "Nettokonverteringskostnad", "NetCostOfGoodsManufactured", "Nettokostnad for produserte varer", "BeginningBalance", "Startsaldo")                                                                                                                                                                                                         |
| Kategorinavn - nivå 2                 | switch(\[Kategorinavn - nivå 2\_\], "Ingen", "Ingen", "Fremskaffet", "Fremskaffet", "Avhendet", "Avhendet", "Overført", "Overført", "Solgt", "Solgt", "ConsumedMaterialsCost", "Brukt materialkostnad", "ConsumedManufacturingCost", "Brukt produksjonskostnad", "ConsumedOutsourcingCost", "Brukt utsettingskostnad", "ConsumedIndirectCost", "Brukt indirekte kostnad", "ManufacturedCost", "Produksjonskostnad", "Avvik", "Avvik")                            |
| Kategorinavn - nivå 3                 | switch(\[Kategorinavn - nivå 3\_\], "Ingen", "Ingen", "Opptelling", "Ingen", "ProductionPriceVariance", "Produksjonspris", "QuantityVariance", "Antall", "SubstitutionVariance", "Erstatning", "ScrapVariance", "Svinn", "LotSizeVariance", "Partistørrelse", "RevaluationVariance", "Revaluering", "PurchasePriceVariance", "Innkjøpspris", "CostChangeVariance", "Kostendring", "RoundingVariance", "Avrundingsavvik")                                                   |

Nøkkeldimensjonene nedenfor brukes som filtre for å dele opp de aggregerte målingene for å oppnå flere detaljer og dypere analytisk innsikt.

| Enhet           | Eksempler på attributter                       |
|------------------|----------------------------------------------|
| Enheter         | ID, navn                                     |
| Økonomiske kalendere | Kalender, måned, periode, kvartal, år       |
| KPI-mål        | Mål for lagerpresisjon, mål for beholdningsomsetning |
| Finanskontoer          | Valuta, navn, beskrivelse                  |
| Siter            | ID, navn, land, poststed                      |






