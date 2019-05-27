---
title: Power BI-innholdet Kostnadsstyring
description: Dette emnet beskriver hva som er inkludert i Kostnadsbehandling-innhold for Power BI.
author: ShylaThompson
manager: AnnBe
ms.date: 03/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f67b1c901267bdf79c94e4f4c698c8731c515bb4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548656"
---
# <a name="cost-management-power-bi-content"></a>Power BI-innholdet Kostnadsstyring

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Oversikt

Microsoft Power BI-innholdet for **Kostnadsstyring** er ment for lagerregnskapsførere eller personer i organisasjonen som er ansvarlig for eller interessert i statusen til lageret eller varer i arbeid (VIA), eller som er ansvarlig for eller er interessert i å analysere avvik i standard kostpris.

> [!NOTE]
> Power BI-innholdet **Kostnadsbehandling** som er beskrevet i dette emnet, gjelder for Dynamics 365 for Finance and Operations 8.0.
> 
> Power BI-innholdspakken for **Kostnadsstyring**, tilgjengelig på AppSource-nettstedet, er foreldet. Hvis du vil ha mer informasjon om denne fjerningen, kan du se [Power BI-innholdspakker tilgjengelig på AppSource](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).

Power BI-innholdet gir et kategoriserte format som hjelper deg å overvåke ytelsen til beholdninger og visualisere hvordan kostnadene flyter gjennom dem. Du kan få innsikt, for eksempel omsetningshastighet, antall dager beholdningen er på lager, presisjon og ABC-klassifisering på det foretrukne aggregerte nivået (firma, vare, varegruppe eller område). Informasjonen som gjøres tilgjengelig, kan også brukes som et detaljert supplement til regnskapsoppgjøret.

Power BI-innholdet er bygd på aggregert **CostObjectStatementCacheMonthly**-måling, som har **CostObjectStatementCache**-tabellen som den primære datakilden. Denne tabellen håndteres av rammeverket for hurtigbuffer for datasett. Tabellen oppdateres hvert døgn som standard, men du kan endre oppdateringsfrekvensen eller aktivere manuelle oppdateringer i konfigurasjonen av datasettbufferen. Manuelle oppdateringer kan kjøres i enten **Kostnadsadministrasjon**-arbeidsområdet eller **Kostnadsanalyse**-arbeidsområdet.

Etter hver oppdatering av **CostObjectStatementCache**-tabellen, må den aggregerte **CostObjectStatementCacheMonthly**-målingen oppdateres før dataene i Power BI-effektene oppdateres.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innholdet

Power BI-innholdet for **Kostnadsadministrasjon** vises i **Kostnadsadministrasjon**- og **Kostnadsanalyse**-arbeidsområdet.

**Kostnadsadministrasjon**-arbeidsområdet inneholder følgende kategorier:

- **Oversikt** – denne kategorien viser programdata.
- **Status for lagerregnskap** – denne kategorien viser Power BI-innhold.
- **Status for produksjonsregnskap** – denne kategorien viser Power BI-innhold.

**Kostnadsanalyse**-arbeidsområdet inneholder følgende kategorier:

- **Oversikt** – denne kategorien viser programdata.
- **Analyse av lagerregnskap** – denne kategorien viser Power BI-innhold.
- **Analyse av produksjonsregnskap** – denne kategorien viser Power BI-innhold.
- **Standard kostavviksanalyse** – denne kategorien viser Power BI-innhold.

## <a name="report-pages-that-are-included-in-the-power-bi-content"></a>Rapporter som er inkludert i Power BI-innholdet

Power BI-innholdet **Kostnadsadministrasjon** omfatter et sett med rapportsider som består av et sett med mål. Disse målene vises som diagrammer, fliser og tabeller. 

Tabellene nedenfor gir en oversikt over visualiseringer i Power BI-innholdet **Kostnadsbehandling**.

### <a name="inventory-accounting-status"></a>Status for lagerregnskap

| Rapportside                               | Visualisering                                   |
|-------------------------------------------|-------------------------------------------------|
| Lageroversikt                        | Startsaldo                               |
|                                           | Netto endring                                      |
|                                           | Netto endring %                                    |
|                                           | Sluttsaldo                                  |
|                                           | Lagerpresisjon                              |
|                                           | Omløpshastighet på lager                        |
|                                           | Dags lagerbeholdning                          |
|                                           | Aktivt produkt i perioden                        |
|                                           | Aktive kostnadsobjekter i perioden                   |
|                                           | Saldo etter varegruppe                           |
|                                           | Saldo etter område                                 |
|                                           | Utdrag etter kategori                           |
|                                           | Netto endring etter kvartal                           |
| Lageroversikt etter område og varegruppe | Lagerpresisjon etter område                      |
|                                           | Omløpshastighet på lager etter område                |
|                                           | Beholdning – sluttsaldo etter område                |
|                                           | Lagerpresisjon etter varegruppe                |
|                                           | Omløpshastighet på lager etter varegruppe          |
|                                           | Beholdning – sluttsaldo etter område og varegruppe |
| Beholdningsoppgave                       | Beholdningsoppgave                             |
| Beholdningsoppgave etter område               | Beholdningsoppgave etter område                     |
| Beholdningsoppgave etter produkthierarki  | Beholdningsoppgave                             |
| Beholdningsoppgave etter produkthierarki  | Beholdningsoppgave etter område                     |

### <a name="manufacturing-accounting-status"></a>Status for produksjonsregnskap

| Rapportside                | Visualisering                       |
|----------------------------|-------------------------------------|
| VIA-oversikt HIÅ           | Startsaldo                   |
|                            | Netto endring                          |
|                            | Netto endring %                        |
|                            | Sluttsaldo                      |
|                            | Omsetningshastighet for VIA                  |
|                            | Dags VIA-beholdning                    |
|                            | Aktivt kostnadsobjekt i perioden        |
|                            | Nettoendring etter ressursgruppe        |
|                            | Saldo etter område                     |
|                            | Utdrag etter kategori               |
|                            | Netto endring etter kvartal               |
| VIA-oppgave              | Startsaldo                   |
|                            | Sluttsaldo                      |
|                            | VIA-oppgave etter kategori           |
| VIA-oppgave etter område      | Startsaldo                   |
|                            | Sluttsaldo                      |
|                            | VIA-oppgave etter kategori og område  |
| VIA-oppgave etter hierarki | Startsaldo                   |
|                            | Sluttsaldo                      |
|                            | VIA-oppgave etter kategorihierarki |

### <a name="inventory-accounting-analysis"></a>Analyse av lagerregnskap

| Rapportside        | Visualisering                                                                |
|--------------------|------------------------------------------------------------------------------|
| Beholdningsdetaljer  | De 10 viktigste ressursene etter sluttsaldo                                           |
|                    | De 10 viktigste ressursene etter nettoendringsøkning                                      |
|                    | De 10 viktigste ressursene etter nettoendringsreduksjon                                      |
|                    | De 10 viktigste ressursene etter omløpshastighet på lager                                 |
|                    | Ressurser etter lav omsetningshastighet på lager og sluttsaldo over terskel |
|                    | De 10 viktigste ressursene etter lav presisjon                                             |
| ABC-klassifisering | Beholdning – sluttsaldo                                                     |
|                    | Brukt materiale                                                            |
|                    | Solgt (vareforbruk)                                                                  |
| Lagertrender   | Beholdning – sluttsaldo                                                     |
|                    | Beholdning – nettoendring                                                         |
|                    | Omløpshastighet på lager                                                     |
|                    | Lagerpresisjon                                                           |

### <a name="manufacturing-accounting-analysis"></a>Analyse av produksjonsregnskap

| Rapportside | Visualisering      |
|-------------|--------------------|
| VIA-trender  | VIA-sluttsaldo |
|             | VIA-nettoendring     |
|             | Omsetningshastighet for VIA |

### <a name="std-cost-variance-analysis"></a>Standard kostavviksanalyse

| Rapportside                             | Visualisering                                        |
|-----------------------------------------|------------------------------------------------------|
| Avvik i kjøpspris (standardkostnad) HIÅ | Fremskaffet saldo                                     |
|                                         | Avvik i kjøpspris                              |
|                                         | Avviksgrad i kjøpspris                        |
|                                         | Avvik etter varegruppe                               |
|                                         | Avvik etter område                                     |
|                                         | Kjøpspris etter kvartal                            |
|                                         | Kjøpspris etter kvartal og varegruppe             |
|                                         | De 10 viktigste ressursene etter ugunstig kjøpsprisgrad |
|                                         | De 10 viktigste ressursene etter gunstig kjøpsprisgrad   |
| Produksjonsavvik (standardkostnad) HIÅ     | Produksjonskostnad                                    |
|                                         | Produksjonsavvik                                  |
|                                         | Produksjonsavviksgrad                            |
|                                         | Avvik etter varegruppe                               |
|                                         | Avvik etter område                                     |
|                                         | Produksjonsavvik etter kvartal                       |
|                                         | Produksjonsavvik etter kvartal og avvikstype     |
|                                         | De 10 viktigste ressursene etter ugunstig produksjonsavvik  |
|                                         | De 10 viktigste ressursene etter gunstig produksjonsavvik    |

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter

Data fra Microsoft Dynamics 365 for Finance and Operations brukes til å fylle ut rapportsidene i Power BI-innholdet **Kostnadsstyring**. Disse dataene representeres som aggregerte målinger som mellomlagres i enhetsbutikken, som er en Microsoft SQL Server-database som er optimalisert for analyse. Hvis du vil ha mer informasjon, se [Power BI-integrering med enhetslager](power-bi-integration-entity-store.md).

De aggregerte nøkkelmålingene for følgende objekter brukes som grunnlag for Power BI-innholdet.

| Objekt                          | Aggregerte nøkkelmålinger | Datakilde for Finance and Operations | Felt               |
|---------------------------------|----------------------------|----------------------------------------|---------------------|
| CostObjectStatementCacheMonthly | Beløp                     | CostObjectStatementCache               | Beløp              |
| CostObjectStatementCacheMonthly | Antall                   | CostObjectStatementCache               | Antall                 |
| CostInventoryAccountingKPIGoal  | AnnualInventoryTurn        | CostInventoryAccountingKPIGoal         | AnnualInventoryTurn |
| CostInventoryAccountingKPIGoal  | InventoryAccuracy          | CostInventoryAccountingKPIGoal         | InventoryAccuracy   |

Tabellen nedenfor viser de beregnede nøkkelmålingene i Power BI-innholdet.

| Mål                            | Beregning |
|------------------------------------|-------------|
| Startsaldo                  | Startsaldo = \[sluttsaldo\]-\[nettoendring\] |
| Startsaldoantall             | Startsaldoantall = \[sluttsaldoantall\]-\[nettoendringsantall\] |
| Sluttsaldo                     | Sluttsaldo = (CALCULATE(SUM(\[Amount\]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\])))) |
| Sluttsaldoantall                | Sluttsaldoantall = CALCULATE(SUM(\[QTY\]), FILTER(ALL(FiscalCalendar),FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\]))) |
| Netto endring                         | Nettoendring = SUM(\[AMOUNT\]) |
| Nettoendringsantall                    | Nettoendringsantall = SUM(\[QTY\]) |
| Omløpshastighet på lager etter beløp | Omløpshastighet på lager etter beløp = if(OR(\[Beholdning – gjennomsnittlig saldo\] \<= 0, \[Solgt lagerbeholdning eller forbrukte avganger\] \>= 0), 0, ABS(\[Solgt lagerbeholdning eller forbrukte avganger\])/\[Beholdning – gjennomsnittlig saldo\]) |
| Beholdning – gjennomsnittlig saldo          | Beholdning – gjennomsnittlig saldo = ((\[sluttsaldo\] + \[startsaldo\]) / 2) |
| Dags lagerbeholdning             | Dags lagerbeholdning = 365 / CostObjectStatementEntries\[Omløpshastighet på lager etter beløp\] |
| Lagerpresisjon                 | Lagerpresisjon etter beløp = IF(\[sluttsaldo\] \<= 0, IF(OR(\[beholdning – opptelt beløp\] \<\> 0, \[sluttsaldo\] \< 0), 0, 1), MAX(0, (\[sluttsaldo\] - ABS(\[beholdning – opptelt beløp\]))/\[sluttsaldo\])) |

Nøkkeldimensjonene nedenfor brukes som filtre for å dele opp de aggregerte målingene, slik at du kan få flere detaljer og dypere analytisk innsikt.


| Enhet                                                  | Eksempler på attributter                          |
|---------------------------------------------------------|-------------------------------------------------|
| Produkter                                                | Produktnummer, produktnavn, enhet, varegrupper |
| Kategorihierarkier (tilordnet rollen Kostnadsstyring) | Kategorihierarki, kategorinivå              |
| Juridiske enheter                                          | Navn på juridiske enheter                              |
| Økonomiske kalendere                                        | Regnskapskalender, år, kvartal, periode, måned   |
| Nettsted                                                    | ID, navn, adresse, delstat og land               |
