---
title: Avgift beregnes ikke eller avgiftsbeløpet er null
description: Dette emnet gir feilsøkingsinformasjon som kan hjelpe når avgiftsbeløpet er 0 (null) eller avgift ikke beregnes.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7237980f8d330a7b3f5c966d5bd3fff0eda8b21a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685863"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a>Avgift beregnes ikke eller avgiftsbeløpet er null

[!include [banner](../includes/banner.md)]

En transaksjon kan ha et linjebeløp som ikke er 0 (null), men enten beregnes ikke avgift eller beregnet avgiftsbeløp er 0. Hvis du vil feilsøke dette problemet, følger du trinnene i de følgende delene etter behov.

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a>Kontroller at avgiftskoder er riktig valgt av transaksjonen

Hvis transaksjonen ikke velger de riktige avgiftskodene, eller hvis den ikke velger noen avgiftskoder, blir det ikke beregnet avgifter på den. Følg disse trinnene for å kontrollere at avgiftskoder er riktig valgt av transaksjonen. 

1. I hurtigfanen **Linjedetaljer** i kategorien **Oppsett** i **Merverdiavgift**-delen kontrollerer du at riktig avgiftsgruppe er valgt i feltene **Varens mva-gruppe** og **Merverdiavgiftsgruppe**. Hvis riktig avgiftsgruppe ikke er valgt, velger du dem.

    [![Feltene Varens mva-gruppe og Merverdiavgiftsgruppe.](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)

2. Gå til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Mva-grupper**.
3. Velg den aktuelle mva-gruppen, og noter deg avgiftskoden i **Mva-kode**-feltet i the **Oppsett**-hurtigfanen.

    [![Siden Mva-grupper.](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)

4. Gå til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Vare, mva-grupper**.
5. Velg den riktige mva-gruppen for vare, og kontroller deretter at mva-koden i **Mva-kode**-feltet samsvarer med mva-koden i mva-gruppen i **Oppsett**-hurtigfanen.

    [![Siden Vare, mva-grupper.](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)

6. Hvis avgiftskodene ikke samsvarer, oppdaterer du mva-koden for én av gruppene.

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a>Kontroller at de valgte avgiftskodene ikke er fritatt, og at de har riktig mva-satsverdi.

Hvis avgiftskodene er fritatt, eller hvis mva-satsen er 0 (null), blir resultatet av avgiftsberegningen 0. Følg denne fremgangsmåten for å finne ut om de valgte avgiftskodene er fritatt, og kontrollere at riktig mva-sats brukes på dem.

1. Gå til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Mva-grupper**.
2. Velg den riktige mva-gruppen, og kontroller deretter at det ikke er merket av for **Avgiftsfri** i **Oppsett**-hurtigfanen. Hvis du har merket av for dette feltet, fjerner du merket.

    [![Avmerkingsboksen Avgiftsfri på Mva-grupper-siden.](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)

3. Gå til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Mva-koder**.
4. Velg den riktige mva-koden, og kontroller deretter at mva-satsverdien i **Verdi**-feltet ikke har verdien 0 (null). Hvis feltet er 0, må du oppdatere feltet slik at det settes til riktig avgiftssats.

    [![Verdi-felt på siden Verdier for merverdiavgiftskode.](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a>Bestem om null er riktig mva-beløp

I noen scenarier er et mva-beløp på 0 (null) riktig. Følg denne fremgangsmåten for å finne ut om 0 er det riktige avgiftsbeløpet for transaksjonen.

1. Gå til **Økonomimodul** \> **Finansoppsett** \> **Parametere for økonomimodul**.
2. Kontroller at **Total** er valgt i **Beregningsmetode**-feltet i kategorien **Merverdiavgift**.

    [![Beregningsmetode-felt på siden Parametere for økonomimodul.](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)

3. Gå til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Mva-koder**.
4. Velg den riktige mva-koden, velg **Beregning** \> **Grensegrunnlag**, og kontroller at grensegrunnlaget er satt til **Nettobeløp på fakturasaldo** eller **Fakturatotal inkl. andre mva-beløp**. Hvis du vil ha mer informasjon, kan du se [Fakturatotal inkl. andre mva-beløp](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).
5. Hvis de riktige verdiene er angitt i trinn 2 og 4, må du bestemme om totalbeløpet for transaksjonen er 0 (null). Hvis totalbeløpet er 0, er et mva-beløp på 0 det forventede resultatet. Fordi avgiftsberegningen er basert på det totale beløpet på fakturasaldoen, og dette beløpet ikke er linje etter linje, vil mva-beløpet på 0 bli tilordnet til hver linje etter avgiftsberegningen.

## <a name="determine-whether-customization-exists"></a>Fastslå om det finnes tilpasning

Hvis du har fullført trinnene i de forrige delene, men ikke har funnet problemet, må du avgjøre om det finnes tilpasning. Hvis det ikke finnes noen tilpasning, oppretter du en Microsoft-tjenesteforespørsel for mer støtte.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
