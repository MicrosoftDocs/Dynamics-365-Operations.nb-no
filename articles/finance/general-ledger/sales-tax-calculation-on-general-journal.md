---
title: Mva-beregning på generelle journallinjer
description: Dette emnet beskriver hvordan merverdiavgift beregnes for ulike kontotyper (leverandør, kunde, finans og prosjekt) på generelle journallinjer.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 51d43c8e6d16201e1f8c392c13ead20287782dcc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446249"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a>Mva-beregning på generelle journallinjer
[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan merverdiavgift beregnes for ulike kontotyper (leverandør, kunde, finans og prosjekt) på generelle journallinjer.

Prosessen kan deles inn i tre trinn:

- Fastslå mva-retningen.

- Fastslår du mva-beløpet som skal lagres en midlertidig mva-tabell.

- Fastslå mva-beløpet og kontoen på bilaget.

## <a name="determine-the-sales-tax-direction"></a>Fastslå mva-retningen

Hvordan mva-retningen bestemmes avhenger av kontotypen i bilaget. Mva-retningen bestemmes av kombinasjonen av kontotypen og mva-koden. Avsnittene nedenfor beskriver mulighetene mer detaljert. 

### <a name="account-type-is-project"></a>Kontotype er Prosjekt

Hvis et bilag har journallinje der kontotypen er **Prosjekt**, vil alle journallinjene i bilaget bruke samme mva-retning. Illustrasjonen nedenfor viser regelen. Punktene nedenfor viser de mulige avgiftsretningene for prosjektkontoer.

•   Hvis mva-koden er use tax, er mva-retningen use tax.

•   Hvis mva-koden er avgiftsfritak, er mva-retningen avgiftsfritt kjøp.

•   Hvis mva-koden er Mva-transaksjoner innenfor EU, er mva-retningen Utgående merverdiavgift.

•   Hvis mva-koden er snudd avregning, er mva-retningen Utgående merverdiavgift.

I andre tilfeller er mva-retningen innkommende merverdiavgift.

Diagrammet nedenfor illustrerer regelen grafisk.

![Muligheter for avgiftsretning for prosjektkontoer](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a>Kontotype er Leverandør

Hvis et bilag har journallinje der kontotypen er **Leverandør**, vil alle journallinjene i bilaget bruke samme mva-retning. Punktene nedenfor viser de mulige avgiftsretningene for leverandørkontoer. 

•   Hvis mva-koden er use tax, er mva-retningen use tax.

•   Hvis mva-koden er avgiftsfritak, er mva-retningen avgiftsfritt kjøp.

•   Hvis mva-koden er Mva-transaksjoner innenfor EU, er mva-retningen Utgående merverdiavgift.

•   Hvis mva-koden er snudd avregning, er mva-retningen Utgående merverdiavgift.

I andre tilfeller er mva-retningen innkommende merverdiavgift.

Diagrammet nedenfor illustrerer regelen grafisk.

![Muligheter for avgiftsretning for leverandørkontoer](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a>Kontotype er Kunde

Hvis et bilag har journallinje der kontotypen er **Kunde**, vil alle journallinjene i bilaget bruke samme mva-retning. Punktene nedenfor viser de mulige avgiftsretningene for kundekontoer.

•   Hvis mva-koden er avgiftsfritak, er mva-retningen avgiftsfritt kjøp.

•   Hvis mva-koden er Mva-transaksjoner innenfor EU, er mva-retningen innkommende merverdiavgift.

•   Hvis mva-koden er snudd avregning, er mva-retningen innkommende merverdiavgift.

I andre tilfeller er mva-retningen Utgående merverdiavgift.

Diagrammet nedenfor illustrerer regelen grafisk.

![Muligheter for avgiftsretning for kundekontoer](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a>Kontotype er Finans

Illustrasjonen nedenfor viser regelen som gjelder når et bilag bare har journallinjer der kontotypen er **Finans**. Punktene nedenfor viser de mulige avgiftsretningene for finanskontoer.

•   Hvis mva-koden er use tax, er mva-retningen use tax.

•   Hvis mva-koden er avgiftsfritak, er mva-retningen avgiftsfritt kjøp.

Hvis journalbeløpet imidlertid er debet (positivt), er mva-retningen Innkommende merverdiavgift. Hvis journalbeløpet er kredit (negativt), er mva-retningen Utgående merverdiavgift.

Diagrammet nedenfor illustrerer regelen grafisk.

![Muligheter for avgiftsretning for finanskontoer](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a>Overstyre mva-retningen

Du kan overstyre mva-retningen når bilaget bare inneholder linjer der kontotypen er **Finans.**

Gå til **Økonomimodul \> Kontoplan \> Kontoer \> Hovedkontoer**, og velg hurtigfanen **Overstyringer for juridisk enhet**.

## <a name="determine-the-sales-tax-amount"></a>Fastslå mva-beløp

Denne delen beskriver hvordan fortegnet for mva-beløpet beregnes.

![Siden Mva-transaksjoner](media/sales-tax-amount-sign.jpg)

Tabellen nedenfor viser den generelle regelen for å fastslå fortegnet for mva-beløp i den midlertidige mva-tabellen.

| Journallinjebeløp | Mva-retning  | Fortegn for mva-beløp |
|---------------------|----------------------|-----------------------|
| Positiv            | Innkommende merverdiavgift | Positiv              |
| Positiv            | Utgående merverdiavgift    | Negativ              |
| Negativ            | Innkommende merverdiavgift | Negativ              |
| Negativ            | Utgående merverdiavgift    | Positiv              |

Det finnes en spesialregel for bilag som bare har **Prosjekt**- eller **Finans**-linjer når det velges en mva-gruppe eller en mva-gruppe for vare på **Finans**-linjen. Denne regelen styres ved hjelp av funksjonen Aktiver uavhengig beregning av merverdiavgift for generelle journaler. Når denne funksjonen er deaktivert, bruker avgiftsbeløpet **Finans**-linjen debet-/kreditretningen for **Prosjekt**-linjen. Når denne funksjonen er aktivert, bruker avgiftsbeløpet **Finans**-linjen sin egen debet-/kreditretning. Tabellene nedenfor viser regelen for hvert scenario. 

**Regel når funksjonen er aktivert**

| Journallinjebeløp for prosjekt | Mva-retning  | Fortegn for mva-beløp |
|--------------------------------|----------------------|-----------------------|
| Positiv                       | Innkommende merverdiavgift | Positiv              |
| Negativ                       | Innkommende merverdiavgift | Negativ              |

**Regel når funksjonen er deaktivert**

| Journallinjebeløp for finans  | Mva-retning  | Fortegn for mva-beløp |
|--------------------------------|----------------------|-----------------------|
| Positiv                       | Innkommende merverdiavgift | Positiv              |
| Negativ                       | Innkommende merverdiavgift | Negativ              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a>Fastslå mva-beløpet og kontoen på bilaget

Når du posterer merverdiavgift, hentes hovedkontoen fra profilen for finansposteringsgruppen. Når merverdiavgift er til innkommende, bruker systemet kontoen Innkommende merverdiavgift som er angitt i profilen. For merverdiavgift som er utgående bruker systemet kontoen Utgående merverdiavgift som er angitt i profilen.

Tabellen nedenfor viser den generelle regelen.

| Mva-retning  | Fortegn for mva-beløp | Mva-konto      | Beløp på bilag |
|----------------------|-----------------------|------------------------|-------------------|
| Innkommende merverdiavgift | Positiv              | Konto for innkommende merverdiavgift | Positive (debet)  |
| Innkommende merverdiavgift | Negativ              | Konto for innkommende merverdiavgift | Negativ (kredit)  |
| Utgående merverdiavgift    | Positiv              | Konto for utgående merverdiavgift    | Negativ (kredit)  |
| Utgående merverdiavgift    | Negativ              | Konto for utgående merverdiavgift    | Positive (debet)  |
