---
title: "Cost management strøm BI innhold"
description: "Dette emnet beskriver hva som er inkludert i Cost management strømmen BI-innhold. Det forklarer hvordan du kan få tilgang til strøm BI-rapporter, og gir informasjon om en datamodell og enheter som brukes til å bygge opp innholdet."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: e4de011e6eeac58643b828b65e24b874d981d5e7
ms.lasthandoff: 03/31/2017


---

# <a name="cost-management-power-bi-content"></a>Cost management strøm BI innhold

Dette emnet beskriver hva som er inkludert i Cost management strømmen BI-innhold. Det forklarer hvordan du kan få tilgang til strøm BI-rapporter, og gir informasjon om en datamodell og enheter som brukes til å bygge opp innholdet.

# <a name="overview"></a>Oversikt

Den **Cost management** Microsoft Power BI-innholdet er ment for lager regnskapsførere, revisorer eller personer i organisasjonen som er ansvarlig for lageret. Den **Cost management** strømmen BI-innhold gir leder innsikt i beholdning og beholdning av varer i arbeid (via), og hvordan kostnadsflyten går gjennom dem etter kategori over tid. Informasjonen kan også brukes som et detaljert supplement til regnskapsoppgjøret.

## <a name="key-measures"></a>Viktige mål

+ Startsaldo
+ Sluttsaldo
+ Netto endring
+ Netto endring i %
+ Aldersfordeling

## <a name="key-performance-indicators"></a>Nøkkelytelsesindikatorer
+ Beholdningsomsetning
+ Lagerpresisjon

Den primære datakilden for CostAggregatedCostStatementEntryEntity er CostStatementCache-tabellen. Denne tabellen håndteres av rammeverket for datasett-hurtigbuffer. Tabellen oppdateres hvert døgn som standard, men du kan aktivere manuelle oppdateringer i hurtigbufferen Datakonfigurasjon. Deretter kan du gjøre en manuell oppdatering i den **Cost management** eller **koster analysis** arbeidsområde. Når oppdateringen av CostStatementCache er kjørt, må du oppdatere OData-tilkobling på strøm BI.com til å se de oppdaterte dataene på området. Avvik (innkjøp, produksjon) målene i dette innholdet strømmen BI gjelder bare for varer som er vurdering av innholdslistemetoden som Standard kostpris. Produksjonsavvik beregnes som differansen mellom aktive kostnader og faktiske kostnader. Produksjonsavvik beregnes når produksjonsordren har statusen **avsluttet**. Hvis du vil ha mer informasjon om produksjonen varians-typene og hvordan hver type beregnes, se [om å analysere avvik for en fullført produksjonsordre](https://technet.microsoft.com/en-us/library/gg242850.aspx).

## <a name="accessing-the-power-bi-content"></a>Tilgang til strøm BI-innhold
Den **Cost management** strømmen BI-innhold er tilgjengelig fra PowerBI.com. Hvis du vil ha mer informasjon om hvordan du kobler og laste inn dine Microsoft Dynamics-365 for operasjoner data, se [Access strømmen BI-innhold fra PowerBI.com](power-bi-home-page.md).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mål som er inkludert i strøm BI-innhold
Innholdet inneholder et sett med rapportsider. Hver side består av et sett med mål som er visualized som tabeller, diagrammer og fliser. Tabellen nedenfor gir en oversikt over effekter i den **Cost management** strømmen BI-innhold.

| Rapportside | Diagrammer | Titler |
|---|---|---|
|Samlet lagerbeholdning (standard etter gjeldende periode) |Presisjon |Lager mål:<br>Lager, sluttsaldo<br>Lager bevegelse<br>Lager bevegelse %<br>|
| |Beholdningsomsetning | |
| |Lager sluttsaldo etter ressursgruppe | |
| |Lager bevegelse av kategori navn-nivå 1 og nivå 2 navn| |
| |Kjøpsavvik etter ressursgruppe og navn på nivå 3 | |
|Lager per område (standard etter gjeldende periode) |Lager sluttsaldo ved områdenavn og ressursgruppe | |
| |Lager slå av områdenavnet og ressursgruppe | |
| |Lager sluttsaldo av group by- og ressursinformasjon | |
|Lager per ressursgruppen (standard etter gjeldende periode) |Lager mål | |
| |Lager nøyaktigheten av beløpet av ressursgruppe | |
| |Lager slå av beløpet av ressursgruppe | |
|Lager YOY (standard gjeldende år i forhold til fjoråret) |Lager mål | |
| |Lager KPIer:<br>Beholdningsomsetning<br>Lagerpresisjon | |
| |Lager sluttsaldo etter år og ressurs | |
| |Kjøpsavvik etter år og kategori navn på nivå 3 | |
|Lager aldersfordeling (standard av inneværende år) |Lager aldersfordelt etter kvartal og ressurs | |
| |Lager aldersfordelt etter kvartal og området navn | |
|VIA generelle (standard etter gjeldende periode) |Endre netto RIA ved kategori navn-nivå 1 og nivå 2 navn |Varer i arbeid via måler:<br>Sluttsaldo for via<br>RIA-bevegelse<br>VIA bevegelse %<br> |
| |Produksjonsprisavvik etter ressursgruppe og navn på nivå 3 | |
| |VIA bevegelse av ressursgruppe | |
|VIA etter område (standard etter gjeldende periode) |Varer i arbeid via mål | |
| |Endre netto RIA ved områdenavnet og navn på nivå 2 | |
| |Produksjonsprisavvik etter områdenavnet og navn på nivå 3 | |

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Dynamics 365 for operasjoner data brukes til å fylle rapportsidene i den **Cost management** strømmen BI-innhold. Disse dataene er representert som samlet mål mellomlagres i butikken enhet, som er en Microsoft SQL-database som er optimalisert for analyse. Hvis du vil ha mer informasjon, se [strømmen BI-oversikt over integrering med enheten butikken](power-bi-integration-entity-store.md). De følgende viktige samlet mål som skal brukes som grunnlag for innholdet.

| Enhet            | Viktige samlet mål | Datakilde for Dynamics 365 for operasjoner | Felt             | beskrivelse                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Oppføringer i setningen | Netto endring                | CostAggregatedCostStatementEntryEntity      | Sum (\[beløpet\])   | Beløpet i regnskapsvalutaen |
| Oppføringer i setningen | Netto endring-antall       | CostAggregatedCostStatementEntryEntity      | Sum (\[antallet\]) |                                   |

Tabellen nedenfor viser hvordan de viktige samlet mål som skal brukes til å opprette flere beregnede mål i det innholdet dataset.

| Mål                                 | Hvordan målet skal beregnes                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Startsaldo                       | \[Sluttsaldo\]-\[bevegelse\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Begynnelsen Saldoantall              | \[Saldo Sluttantall\]-\[bevegelse antall\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Sluttsaldo                          | BEREGN (SUMMER (\[beløpet\]), FILTER (ALLEXCEPT ('Regnskapskalendere', 'Regnskapskalendere'\[LedgerRecId\], "enheter"\[ID\], "enheter"\[navnet\], 'Finans'\[valuta\], 'Finans'\[beskrivelse\], 'Finans'\[navn\]), 'Regnskapskalendere'\[dato\]&lt;= Maks ('Regnskapskalendere'\[dato\])))                                                                                                                                                                                           |
| Avslutter Saldoantall                 | BEREGN (SUMMER (\[antallet\]), FILTER (ALLEXCEPT ('Regnskapskalendere', 'Regnskapskalendere'\[LedgerRecId\], "enheter"\[ID\], "enheter"\[navnet\], 'Finans'\[valuta\], 'Finans'\[beskrivelse\], 'Finans'\[navn\]), 'Regnskapskalendere'\[dato\]&lt;= Maks ('Regnskapskalendere'\[dato\])))                                                                                                                                                                                         |
| Lager startsaldo             | BEREGN (\[startsaldo\], 'Utdragsposter'\[setningstypen\] = "Lager")                                                                                                                                                                                                                                                                                                                                                                                      |
| Lager, sluttsaldo                | BEREGN (\[sluttsaldo\], 'Utdragsposter'\[setningstypen\] = "Lager")                                                                                                                                                                                                                                                                                                                                                                                         |
| Lager bevegelse                    | BEREGN (\[bevegelse\], 'Utdragsposter'\[setningstypen\] = "Lager")                                                                                                                                                                                                                                                                                                                                                                                             |
| Lagerantallet bevegelse           | BEREGN (\[bevegelse antallet\], 'Utdragsposter'\[setningstypen\] = "Lager")                                                                                                                                                                                                                                                                                                                                                                                    |
| Lager bevegelse %                  | IF (\[lager sluttsaldoen\] = 0, 0, \[lager bevegelse\] / \[lager sluttsaldoen\])                                                                                                                                                                                                                                                                                                                                                                           |
| Lager slå av beløp                | Hvis (eller (\[lager gjennomsnittlig Saldo\]&lt;= 0, \[lager solgt eller forbrukt problemer\]&gt;= 0), 0, ABS (\[lager solgt eller forbrukt problemer\]) /\[lager gjennomsnittlig Saldo\])                                                                                                                                                                                                                                                                                                  |
| Gjennomsnittlig lagerbalansen               | (\[Lager sluttsaldoen\] + \[lager startsaldo\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Lager solgt eller forbrukt problemer       | \[Lager solgte\] + \[lager forbrukt materialkostnaden\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Lager brukt materialkostnaden        | BEREGN (\[lager bevegelse\], 'Utdragsposter'\[kategorinavn - nivå 2\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Solgt lagerbeholdning                          | BEREGN (\[lager bevegelse\], 'Utdragsposter'\[kategorinavn - nivå 2\_\] = "Sold")                                                                                                                                                                                                                                                                                                                                                                             |
| Lager nøyaktigheten av beløp            | IF (\[lager sluttsaldoen\]&lt;= 0, hvis (eller (\[lager opptelt beløp\]&lt;&gt; 0, \[lager sluttsaldoen\]&lt; 0), 0, 1), Maks (0, (\[lager sluttsaldoen\] -ABS (\[lager opptelt beløp\])) /\[lager sluttsaldoen\]))                                                                                                                                                                                                                              |
| Lager opptelt beløp                | BEREGN (\[lager bevegelse\], 'Utdragsposter'\[kategorinavn - nivå 3\_\] = "Opptelling")                                                                                                                                                                                                                                                                                                                                                                         |
| Aldersfordeling for lager                         | Hvis (ERTOM (maks ('Regnskapskalendere'\[dato\])), blank(), MAX (0, MIN (\[lager aldersfordeling mottak antallet\], \[lager aldersfordeling siste balanse antallet\] - \[lager aldersfordeling mottak antallet i fremtiden\]))) \*\[lager avg enhetskost\]                                                                                                                                                                                                                                |
| Lager aldersfordeling antallet for mottak       | Hvis (\[minDate\] = \[minDateAllSelected\], BEREGN (\[lager bevegelse antallet\], setning-oppføringer\[antallet\]&gt; 0, FILTER (ALLEXCEPT ('Regnskapskalendere', 'Regnskapskalendere'\[LedgerRecId\], "enheter"\[ID\], "enheter"\[navnet\], 'Finans'\[valuta\], 'Finans'\[beskrivelse\], 'Finans'\[navn\]), 'Regnskapskalendere'\[dato\]&lt;= Maks ('Regnskapskalendere'\[dato\]))), BEREGN (\[lager bevegelse antallet\], setning-oppføringer\[antallet\]&gt; 0)) |
| Lager aldersfordelt saldo Sluttantall | \[Lager slutter saldo antallet\] + BEREGNING (\[lager bevegelse antallet\], FILTER (ALLEXCEPT ('Regnskapskalendere', 'Regnskapskalendere'\[LedgerRecId\], "enheter"\[ID\], "enheter"\[navnet\], 'Finans'\[valuta\], 'Finans'\[beskrivelse\], 'Finans'\[navn\]), 'Regnskapskalendere'\[dato\]&gt; Maks ('Regnskapskalendere'\[dato\])))                                                                                                                                 |
| Aldersfordeling på lagertilganger i fremtiden  | BEREGN (\[lager bevegelse\], 'Utdragsposter'\[beløpet\]&gt; 0, FILTER (ALLEXCEPT ('Regnskapskalendere', 'Regnskapskalendere'\[LedgerRecId\], "enheter"\[ID\], "enheter"\[navnet\], 'Finans'\[valuta\], 'Finans'\[beskrivelse\], 'Finans'\[navn\]), 'Regnskapskalendere'\[dato\]&gt; MAX ('Regnskapskalendere'\[dato\])))                                                                                                                                             |
| Lager avg enhetskost                 | BEREGN (\[lager sluttsaldoen\] / \[lager siste balanse antallet\], ALLEXCEPT ('Regnskapskalendere', 'Regnskapskalendere'\[LedgerRecId\], "enheter"\[ID\], "enheter"\[navnet\], 'Finans'\[valuta\], 'Finans'\[beskrivelse\], 'Finans'\[navn\]))                                                                                                                                                                                                                 |
| Kjøpsavvik                      | BEREGN (SUMMER (\[beløpet\]), 'Utdragsposter'\[kategorinavn - nivå 2\_\] = "Procured", 'Utdragsposter'\[setningstypen\] = "Avvik")                                                                                                                                                                                                                                                                                                                              |
| VIA startsaldo                   | BEREGN (\[startsaldo\], 'Utdragsposter'\[setningstypen\] = "Via")                                                                                                                                                                                                                                                                                                                                                                                            |
| Sluttsaldo for via                      | BEREGN (\[sluttsaldo\], 'Utdragsposter'\[setningstypen\] = "Via")                                                                                                                                                                                                                                                                                                                                                                                               |
| RIA-bevegelse                          | BEREGN (\[bevegelse\], 'Utdragsposter'\[setningstypen\] = "Via")                                                                                                                                                                                                                                                                                                                                                                                                   |
| VIA bevegelse %                        | IF (\[via sluttsaldo\] = 0, 0, \[via bevegelsen\] / \[via sluttsaldo\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Produksjonsavvik                    | BEREGN (SUMMER (\[beløpet\]), 'Utdragsposter'\[kategorinavn - nivå 2\_\] = "ManufacturedCost", 'Utdragsposter'\[setningstypen\] = "Avvik")                                                                                                                                                                                                                                                                                                                      |
| Kategorinavn - nivå 1                 | Bytte (\[kategorinavn - nivå 1\_\], "None", "None", "NetSourcing", "Net leverandører", "NetUsage", "Net Bruk", "NetConversionCost", "Net konvertering kostnader", "NetCostOfGoodsManufactured", "Net kostnader for produserte varer", "BeginningBalance", "Startsaldo")                                                                                                                                                                                                         |
| Kategorinavn - nivå 2                 | Bytte (\[kategorinavn - nivå 2\_\], "None", "None", "Procured", "Procured", "Disposed", "Disposed", "Overført", "Overført", "Solgt", "Solgt", "ConsumedMaterialsCost", "Brukt materialkostnad", "ConsumedManufacturingCost", "Brukt produksjonskostnaden", "ConsumedOutsourcingCost", "Forbrukt kostnad outsourcing", "ConsumedIndirectCost", "Forbrukt indirekte kostnad", "ManufacturedCost", "Produsert kostnad", "Avvik", "Avvik")                            |
| Kategorinavn - nivå 3                 | Bytte (\[kategorinavn - nivå 3\_\], "None", "None", "Teller", "None", "ProductionPriceVariance", "produksjonspris", "QuantityVariance", "Antall", "SubstitutionVariance", "Substitution", "ScrapVariance", "Kladd", "LotSizeVariance", "Partistørrelsen", "RevaluationVariance", "Omvurdering", "PurchasePriceVariance", "Innkjøpspris", "CostChangeVariance", "Kostprisendringen", "RoundingVariance", "Avrundingsavvik")                                                   |

Følgende viktige dimensjoner brukes som filtre kan skjære samlet målene for å oppnå større tetthet og gir dypere analytisk kunnskap.

| Enhet           | Eksempler på attributtene                       |
|------------------|----------------------------------------------|
| Enheter         | ID, navn                                     |
| Økonomiske kalendere | Kalenderen måneden, perioden, kvartal, år       |
| KPI-mål        | Lager nøyaktige mål, lager slå målet |
| Finanskontoer          | Valuta, navn, beskrivelse                  |
| Siter            | ID, navn, land og by                      |

## <a name="additional-resources"></a>Tilleggsressurser
Her er noen nyttige koblinger som er knyttet til enheter og oppretting av Power BI-innhold:

-   [Dataenheter](..\data-entities\data-entities.md)
-   [Opprette innholdspakker for organisasjonen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering med Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Legge til Power BI-fliser i arbeidsområder](configure-power-bi-integration.md)



