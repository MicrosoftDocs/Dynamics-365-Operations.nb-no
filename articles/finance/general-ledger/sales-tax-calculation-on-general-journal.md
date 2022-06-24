---
title: Mva-beregning på generelle journallinjer
description: Denne artikkelen beskriver hvordan merverdiavgift beregnes for ulike kontotyper (leverandør, kunde, finans og prosjekt) på generelle journallinjer.
author: EricWangChen
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: a73e145dd26e930c860e9ea31d7dab4f1593c2a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845294"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a>Mva-beregning på generelle journallinjer
[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan merverdiavgift beregnes for ulike kontotyper (leverandør, kunde, finans og prosjekt) på generelle journallinjer.

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

![Muligheter for avgiftsretning for prosjektkontoer.](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a>Kontotype er Leverandør

Hvis et bilag har journallinje der kontotypen er **Leverandør**, vil alle journallinjene i bilaget bruke samme mva-retning. Punktene nedenfor viser de mulige avgiftsretningene for leverandørkontoer. 

•   Hvis mva-koden er use tax, er mva-retningen use tax.

•   Hvis mva-koden er avgiftsfritak, er mva-retningen avgiftsfritt kjøp.

•   Hvis mva-koden er Mva-transaksjoner innenfor EU, er mva-retningen Utgående merverdiavgift.

•   Hvis mva-koden er snudd avregning, er mva-retningen Utgående merverdiavgift.

I andre tilfeller er mva-retningen innkommende merverdiavgift.

Diagrammet nedenfor illustrerer regelen grafisk.

![Muligheter for avgiftsretning for leverandørkontoer.](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a>Kontotype er Kunde

Hvis et bilag har en journallinje der kontotypen er **Kunde**, bruker alle journallinjene i bilaget samme mva-retning. 

Hvis mva-koden er avgiftsfritak, er mva-retningen Avgiftsfritt salg. I andre tilfeller er mva-retningen Utgående merverdiavgift.

### <a name="account-type-is-ledger"></a>Kontotype er Finans

Illustrasjonen nedenfor viser regelen som gjelder når et bilag bare har journallinjer der kontotypen er **Finans**. Punktene nedenfor viser de mulige avgiftsretningene for finanskontoer.

•   Hvis mva-koden er use tax, er mva-retningen use tax.

•   Hvis mva-koden er avgiftsfritak, er mva-retningen avgiftsfritt kjøp.

Hvis journalbeløpet imidlertid er debet (positivt), er mva-retningen Innkommende merverdiavgift. Hvis journalbeløpet er kredit (negativt), er mva-retningen Utgående merverdiavgift.

Diagrammet nedenfor illustrerer regelen grafisk.

![Muligheter for avgiftsretning for finanskontoer.](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a>Overstyre mva-retningen

Du kan overstyre mva-retningen når bilaget bare inneholder linjer der kontotypen er **Finans.**

Gå til **Økonomimodul \> Kontoplan \> Kontoer \> Hovedkontoer**, og velg hurtigfanen **Overstyringer for juridisk enhet**.

## <a name="determine-the-sales-tax-amount"></a>Fastslå mva-beløp

Denne delen beskriver hvordan fortegnet for mva-beløpet beregnes.

![Siden Mva-transaksjoner.](media/sales-tax-amount-sign.jpg)

Tabellen nedenfor viser den generelle regelen for å fastslå mva-retningen og fortegnet for mva-beløp i den midlertidige mva-tabellen.

| Journallinjebeløp | Mva-retning  | Fortegn for mva-beløp |
|---------------------|----------------------|-----------------------|
| Positiv            | Innkommende merverdiavgift | Positiv              |
| Positiv            | Utgående merverdiavgift    | Negativ              |
| Negativ            | Innkommende merverdiavgift | Negativ              |
| Negativ            | Utgående merverdiavgift    | Positiv              |

Det finnes en spesialregel for bilag som bare har **Prosjekt**- eller **Finans**-linjer når det velges en mva-gruppe eller en mva-gruppe for vare på **Finans**-linjen. Denne regelen styres ved hjelp av funksjonen **Aktiver uavhengig beregning av merverdiavgift for generelle journaler**. Når denne funksjonen er deaktivert, bruker avgiftsbeløpet **Finans**-linjen debet-/kreditretningen for **Prosjekt**-linjen. Når denne funksjonen er aktivert, bruker avgiftsbeløpet **Finans**-linjen sin egen debet-/kreditretning. Tabellene nedenfor viser regelen for hvert scenario. 

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
