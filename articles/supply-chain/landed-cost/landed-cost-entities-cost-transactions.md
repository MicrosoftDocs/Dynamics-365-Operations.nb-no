---
title: Kostnadstransaksjonsenheter
description: Denne artikkelen gir informasjon om kostnadstransaksjonsenheter, som gjør det mulig å dele verdien av en kostnad mellom innholdet i et kostnadsområde ved å velge en fordelingsmetode.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 3aabc1356eba27de797fa696dd928cb401d8501b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860819"
---
# <a name="cost-transaction-entities"></a>Kostnadstransaksjonsenheter

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

## <a name="apportionment"></a>Fordeling

Ved hjelp av Landingskostnad kan verdien av en kostnad deles mellom innholdet i et kostnadsområde (for eksempel fraktcontainere og så videre) ved at det velges en fordelingsmetode. Andelingsmetoden er angitt som en del av konfigurasjonen av automatiske kostnader som er basert på forretningsregler. Den trekkes gjennom som en del av kostnaden når en strek opprettes.

### <a name="configure-the-apportionment-mapping-for-use-with-data-entities"></a>Konfigurere vurderingstilordningen for bruk med dataenheter

Når en kostnad opprettes fra en ekstern kilde, for eksempel en spektør, kan ikke den eksterne kilden angi den foretrukne metoden for fordeling av kostnadsverdien. I fordelingstilordningen defineres standard fordelingsmetode for hver kostnadstypekode. Du får tilgang til tabellen for **Fordelingstilordning**-siden i Microsoft Dynamics 365 Supply Chain Management (**Landingskostnad \> Etterkalkuleringsoppsett \> Fordelingstildeling**).

Hvis en tilordningskombinasjon er definert, og en kostnad som samsvarer med kostnadstypekoden, opprettes ved å brukebruke en kostnadstransaksjonsentitet, brukes den tilordnede fordelingsmetoden i stedet for eventuell verdi som er angittenhetenityen.

Hvis det ikke finnes noen verdi i tilordningstabellen, men det er angitt en verdi for enheten, brukes den angitte verdien.

Hvis det ikke finnes noen verdi i tilordningstabellen eller posten som er sendt til enheten, vil opprettelsen mislykkes.

### <a name="apportionment-mapping-itmapportionmentmapping"></a>Fordelingstilordning (ITMApportionmentMapping)

Enheten for fordelingstilordning (`ITMApportionmentMapping`) oppretter tilordningsrelasjoner for fordeling og gjør det mulig for brukere å opprette eller oppdatere poster.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Fordelingsmetode | ITMApportionmentMapping.ApportionmentMethod | Int | Nei | Nei |
| Kosttypekode | ITMApportionmentMapping.ShipCostTypeId | Nvarchar(20) | **Ja** | Nei |

## <a name="voyage-costs-itmcosttransvoyageentity"></a>Reisekostnader (ITMCostTransVoyageEntity)

Reisekostnadsenheten (`ITMCostTransVoyageEntity`) oppretter reisekosttransaksjoner som blir brukt på dette nivået. Under importprosessen bruker systemet verdiene for **Kategori** og **Fordelingsmetode** som er inkludert i enheten, til å bestemme hvordan verdien av kostnaden skal fordeles på tvers av innholdet i reisen.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Fordelingsmetode | ITMCostTrans.ApportionmentMethod | Int | Nei | Nei |
| Kostnadsverdi | ITMCostTrans.CostValue | Numeric(32, 6) | Nei | Nei |
| Valuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nei | **Ja** |
| Linjenummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nei |
| Koblet kostnadstype | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nei | Nei |
| Minimumskostnad | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nei | Nei |
| Kategori | ITMCostTrans.ShipCostCategory | Int | Nei | Nei |
| Kosttypekode | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nei | Nei |
| Selskap | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nei | **Ja** |
| Sjøreise | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nei |
| Varens mva-gruppe | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nei | Nei |

## <a name="shipping-container-costs-itmcosttransshippingcontainerentity"></a>Forsendelsescontainerkostnader (ITMCostTransShippingContainerEntity)

Fraktcontainerkostnadsenheten (`ITMCostTransShippingContainerEntity`) oppretter forsendelsescontainerkostnader som brukes på containernivå for forsendelse. Under importprosessen bruker systemet verdiene for **Kategori** og **Fordelingsmetode** som er inkludert i enheten, til å bestemme hvordan verdien av kostnaden skal fordeles på tvers av innholdet i forsendelsescontaineren.

Feltene **Aggreger**, **Strekning** og **Koblet strekning** er spesifikke for poster der verdien **Kostnadsområde** er *Forsendelsescontainer*. Derfor finnes de ikke i dataenheter for andre kostnadsområder.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Mengde | ITMCostTrans.AggregatedCost | Int | Nei | Nei |
| Fordelingsmetode | ITMCostTrans.ApportionmentMethod | Int | Nei | Nei |
| Kostnadsverdi | ITMCostTrans.CostValue | Numeric(32, 6) | Nei | Nei |
| Valuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nei | **Ja** |
| Linjenummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nei |
| Koblet kostnadstype | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nei | Nei |
| Koblet strekning | ITMCostTrans.LinkLegId | Nvarchar(20) | Nei | Nei |
| Minimumskostnad | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nei | Nei |
| Fraktcontainer | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nei |
| Kategori | ITMCostTrans.ShipCostCategory | Int | Nei | Nei |
| Kosttypekode | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nei | Nei |
| Selskap | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nei | **Ja** |
| Sjøreise | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nei |
| Strekning | ITMCostTrans.ShipLegId | Nvarchar(20) | Nei | Nei |
| Varens mva-gruppe | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nei | Nei |

## <a name="folio-costs-itmcosttransfolioentity"></a>Foliokostnader (ITMCostTransFolioEntity)

Foliokostenheten (`ITMCostTransFolioEntity`) oppretter kostnadstransaksjonsposter som gjelder for folionivået. Under importprosessen bruker systemet verdiene for **Kategori** og **Fordelingsmetode** som er inkludert i enheten, til å bestemme hvordan verdien av kostnaden skal fordeles på tvers av innholdet i hver folio.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Fordelingsmetode | ITMCostTrans.ApportionmentMethod | Int | Nei | Nei |
| Kostnadsverdi | ITMCostTrans.CostValue | Numeric(32, 6) | Nei | Nei |
| Valuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nei | **Ja** |
| Linjenummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nei |
| Koblet kostnadstype | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nei | Nei |
| Minimumskostnad | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nei | Nei |
| Kategori | ITMCostTrans.ShipCostCategory | Int | Nei | Nei |
| Kosttypekode | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nei | Nei |
| Selskap | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nei | **Ja** |
| Folio | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nei |
| Varens mva-gruppe | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nei | Nei |

## <a name="purchase-order-costs-itmcosttranspurchaseentity"></a>Bestillingskostnader (ITMCostTransPurchaseEntity)

Innkjøpsordrekostnadsenheten (`ITMCostTransPurchaseEntity`) oppretter kostnadstransaksjoner som gjelder for innkjøperordrehodet. Under importprosessen bruker systemet verdiene for **Kategori** og **Fordelingsmetode** som er inkludert i enheten, til å bestemme hvordan verdien av kostnaden skal fordeles på tvers av innholdet i hver folio.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Fordelingsmetode | ITMCostTrans.ApportionmentMethod | Int | Nei | Nei |
| Kostnadsverdi | ITMCostTrans.CostValue | Numeric(32, 6) | Nei | Nei |
| Valuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nei | **Ja** |
| Linjenummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nei |
| Koblet kostnadstype | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nei | Nei |
| Minimumskostnad | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nei | Nei |
| Bestilling | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nei |
| Kategori | ITMCostTrans.ShipCostCategory | Int | Nei | Nei |
| Kosttypekode | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nei | Nei |
| Selskap | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nei | **Ja** |
| Varens mva-gruppe | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nei | Nei |

## <a name="item-costs-itmcosttransitementity"></a>Varekostnader (ITMCostTransItemEntity)

Varekostenheten (`ITMCostTransItemEntity`) oppretter kostnadstransaksjoner som gjelder for varenivået. Denne enheten er spesifikk for varer i bestillingslinjer. Verdien av kostnaden brukes i sin helhet for linjen.

Feltene for **Justeringsbeløp** og **Verdijustering** er spesifikke for kostnadsområdene på linjenivå. Derfor finnes de ikke i dataenheter for andre kostnadsområder.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Justeringsbeløp | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | Nei | Nei |
| Kostnadsverdi | ITMCostTrans.CostValue | Numeric(32, 6) | Nei | Nei |
| Valuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nei | **Ja** |
| Linjenummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nei |
| Koblet kostnadstype | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nei | Nei |
| Minimumskostnad | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nei | Nei |
| Bestilling | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nei |
| Bestillingslinjenummer | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nei |
| Kategori | ITMCostTrans.ShipCostCategory | Int | Nei | Nei |
| Kosttypekode | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nei | Nei |
| Selskap | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nei | **Ja** |
| Varens mva-gruppe | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nei | Nei |
| Verdijustering | ITMCostTrans.ValueAdjustmentMethod | Int | Nei | Nei |

## <a name="transfer-line-costs-itmcosttranstransferlineentity"></a>Overføringslinjekostnader (ITMCostTransTransferLineEntity)

Enheten for overføringslinjekostnad (`ITMCostTransTransferLineEntity`) oppretter kostnadstransaksjoner som gjelder for overføringsordrelinjenivået. Verdien av disse kostnadene brukes i sin helhet for overføringsordrelinjen.

Feltene for **Justeringsbeløp** og **Verdijustering** er spesifikke for kostnadsområdene på linjenivå. Derfor finnes de ikke i dataenheter for andre kostnadsområder.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Justeringsbeløp | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | Nei | Nei |
| Kostnadsverdi | ITMCostTrans.CostValue | Numeric(32, 6) | Nei | Nei |
| Valuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nei | **Ja** |
| Linjenummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nei |
| Koblet kostnadstype | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nei | Nei |
| Minimumskostnad | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nei | Nei |
| Kategori | ITMCostTrans.ShipCostCategory | Int | Nei | Nei |
| Kosttypekode | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nei | Nei |
| Selskap | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nei | **Ja** |
| Overføringsordre | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nei |
| Nummer på overføringsordrelinje | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nei |
| Varens mva-gruppe | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nei | Nei |
| Verdijustering | ITMCostTrans.ValueAdjustmentMethod | Int | Nei | Nei |

### <a name="transaction-table"></a>Transaksjonstabell

En kostnadstransaksjonspost knyttes til et kostnadsområde ved tilordning av et transaksjonstabellnummer (`TransTableId`). Når det kreves bestemte tabellidentifikasjonsnumre, blir enhetene delt basert på disse verdiene, slik at det finnes en enhet for hvert kostnadsområde.

Verdien for transaksjonstabellen (`TransTableId`) er implisitt ved valg av kostnadstransaksjonsenheten.

### <a name="calculated-fields"></a>Beregnede felt

Følgende felt er ikke tilgjengelige for innlegging eller oppdatering når en kostnadstransaksjonsenhet brukes, fordi disse feltene bare angis når det er utført bestemte handlinger i forhold til poster som skal utføres:

- **Estimert kostnad** – Dette feltet angis når det posteres en faktura for bestillingen eller overføringen mottas.
- **Estimert kostnadvaluta** – Dette feltet angis når det posteres en faktura for reisen (bestilling) eller en overføring er mottatt.
- **Faktisk kostnad** – Dette feltet angis når en leverandørfaktura posteres. Den er knyttet til kostnaden.

### <a name="find-auto-costs"></a>Finn automatiske kostnader

En **Finn automatiske kostnader**-knapp som er tilgjengelig for hvert kostnadsområde (lagring, forsendelsescontainer og så videre) gir en metode for å oppdatere kostnadstransaksjonene for dette kostnadsområdet fra informasjonen i konfigurasjonstabellene. Når du velger knappen for et kostnadsområde, fjerner systemet eksisterende kostnader for dette kostnadsområdet, og oppretter nye poster basert på den gjeldende konfigurasjonen av tabellene for automatisk kostnadsoppsett.

Kostnadstransaksjonsposter som opprettes ved hjelp av en dataenhet, flagges som importert. Disse postene slettes ikke når du velger **Søk etter automatiske kostnader**, fordi de ikke blir opprettet på nytt fra tabellene for oppsett av automatiske kostnader. En kostnadstransaksjonspost som er flagget som importert, kan imidlertid fremdeles slettes.

### <a name="linked-fields"></a>Koblede felt

Hver kostnadstransaksjon kan knyttes til en annen post i det samme kostnadsområdet. Denne tilknytningen etableres via feltet **Koblede kostnadstype**. Det gjør at en kostnadsverdi kan beregnes som en prosentandel av en annen kostnad.

Feltet **Tilknyttet kosttype** kan bare valideres hvis posten det refereres til, behandles først, eller hvis den allerede finnes i tabellen. De samme kravene gjelder for **Koblet strekning**-feltet som bare brukes for kostnader i kostnadsområdet for forsendelsescontainer.
