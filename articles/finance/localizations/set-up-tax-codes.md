---
title: Konfigurere avgiftskoder
description: Denne artikkelen forklarer hvordan du konfigurere avgiftkoder i avgiftsberegningstjenesten.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 1bc250716763ce9d8e25c8850c8a3676bf65fb0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862935"
---
# <a name="set-up-tax-codes"></a>Konfigurere avgiftskoder

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du konfigurere avgiftkoder i avgiftsberegningstjenesten. Det inkluderer oppsettet for et enkelt scenario for å få mva-koden til å fungere, og informasjon om avansert mva-kodefunksjonalitet for komplekse scenarier.

> [!IMPORTANT]
> Oppsettet av avgiftskoder i avgiftsberegningstjenesten er juridisk enhet–agnostisk. Du kan bare fullføre dette oppsettet i RCS (Regulatory Configuration Service) én gang. Avgiftskoder synkroniseres automatisk med Microsoft Dynamics 365 Finance når du aktiverer avgiftsberegningstjenesten for en valgt juridisk enhet i Finance.

## <a name="simple-setup"></a>Enkelt oppsett

Følg denne fremgangsmåten for å bruke en mva-kode i et enkelt scenario, for eksempel et scenario der det bare er én mva-sats.

1. Logg på [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Gå til **Arbeidsområder** \> **Globaliseringsfunksjoner** \> **Avgiftsberegning**.
3. Velg funksjonen og versjonen du vil sette opp, og velg **Rediger**.
4. Velg **Konfigurasjonsversjon** i kategorien **Generelt**.
5. På **Avgiftskoder**-fanen velger du **Legg til** og angir deretter avgiftskoden og en beskrivelse.
6. Velg **Beregningsopprinnelse**. En beregningsopprinnelse en en gruppe med metoder som defineres i avgiftskonfigurasjonsversjonen du valgte. I dette enkle scenariet velger du **Etter nettobeløp**.
7. Velg **Lagre**. Flere felter blir tilgjengelige, basert på beregningsopprinnelsen du valgte.
8. Velg **Legg til** en mva-sats for denne avgiftskoden i hurtigfanen **Satser**.
9. Velg **Lagre**.

## <a name="calculation-origin"></a>Beregningsopprinnelse

Beregningsopprinnelsen definerer hvordan avgiftsgrunnlagsbeløpet og avgiftsbeløpet skal beregnes. Det konfigureres ved hjelp av avgiftskonfigurasjon i arbeidsområdet **Elektronisk rapportering**. Følgende verdier er tilgjengelige i **Beregningsopprinnelse**-feltet:

- Etter nettobeløp
- Etter bruttobeløp
- Etter antall
- Etter margin
- Avgift på avgift

### <a name="by-net-amount"></a>Etter nettobeløp

Hvis du velger **Etter nettobeløp** i feltet **Beregningsopprinnelse** beregnes avgiftsbeløpet som en prosent av kjøps- eller salgsbeløpet, ekskludert andre mva-koder.

Mva-satsen er for eksempel 25 prosent, fakturalinjen viser et antall på 10 varer til 1,00 per stykk, og kunden får en 10 prosent linjerabatt. I dette tilfellet beregnes beløpene på følgende måte:

- **Nettobeløp:** (10 × 1,00) – 10 prosent = 9,00 
- **Merverdiavgift:** 9,00 × 25 percent = 2,25 
- **Totalt fakturabeløp:** = 9,00 + 2,25 = 11,25

### <a name="by-gross-amount"></a>Etter bruttobeløp

Hvis du velger **Etter bruttobeløp** i feltet **Beregningsopprinnelse**-feltet, beregnes merverdiavgift som en prosent av bruttosalgsbeløpet. Bruttobeløpet er injens nettobeløp pluss alle skatter og avgifter for linjen unntatt én avgift der **Beregningsopprinnelse**-feltet er satt til **Etter bruttobeløp**.

Skattemyndighetene har eksempelvis innført spesielle avgifter på en vare. Avgiftsbeløpene legges til nettobeløpet før avgift beregnes. Følgende avgiftskoder brukes:

- **Avgift 1** – Satsen er 10 prosent, og beregningsmetoden **Etter nettobeløp** brukes.
- **Avgift 2** – Satsen er 20 prosent, og beregningsmetoden **Etter nettobeløp** brukes.
- **Avgiftssats** – Satsen er 25 prosent, og beregningsmetoden **Etter nettobeløp** brukes.

Hvis nettobeløpet er 10,00, blir Avgift 1-beløpet 1,00 (10,00 × 10 prosent), og Avgift 2-beløpet er 2,00 (10,00 × 20 prosent). I dette tilfellet beregnes beløpene på følgende måte: 

- **Bruttobeløp:** Nettobeløp + Avgift 1-beløp + Avgift 2-beløp = 10,00 + 1,00 + 2,00 = 13,00 
- **Avgiftsbeløp:** 13,00 × 25 prosent = 3,25 
- **Totale avgifter:** 1,00 + 2,00 + 3,25 = 6,25 
- **Totalt fakturabeløp:** = 10,00 + 6,25 = 16,25

### <a name="by-quantity"></a>Etter antall

Hvis du velger **Etter antall** i feltet **Beregningsopprinnelse**, vil avgiftsbeløpet beregnes som et fast beløp per enhet og ganges med antallet som er angitt på dokumentlinjen. Beløpet per enhet er angitt i hurtigfanen **Satser**.

Mva-koden er for eksempel definert til 1,20 per enhet. På en salgsfakturalinje selges 25 enheter av en vare. I slike tilfeller beregnes avgiftsbeløpet til 25 × 1,20 = 30,00.

### <a name="by-margin"></a>Etter margin

Hvis du velger **Etter margin** i feltet **Beregningsopprinnelse**-feltet, beregnes merverdiavgift som en prosent av salgsmarginen. Salgsmarginen er salgsbeløpet minus kostnadsbeløpet. Denne beregningsmåten gjelder bare for salgstransaksjoner.

Mva-satsen er for eksempel 25 prosent, fakturalinjen viser et antall på 10 varer til 10,00 per stykk, og kostnad per vare er 6. I dette tilfellet beregnes beløpene på følgende måte:

- **Salgsmargin:** 10 × (10,00 – 6,00) = 40,00
- **Avgiftsbeløp:** 40,00 × 25 prosent = 10,00
- **Totalt fakturabeløp:** = 100,00 + 10,00 = 110,00

### <a name="tax-on-tax"></a>Avgift på avgift

Hvis du velger **Avgift på avgift** i **beregningsgrunnlag**-feltet, beregnes merverdiavgiften som en prosent av alle andre avgiftsbeløp på samme dokumentlinje.

Eksempelvis brukes følgende avgiftskoder:

- **Avgift 1** – Satsen er 10 prosent, og beregningsmetoden **Etter nettobeløp** brukes.
- **Avgift 2** – Satsen er 20 prosent, og beregningsmetoden **Etter nettobeløp** brukes.
- **Avgift på avgift** – Satsen er 25 prosent, og beregningsmetoden **Avgift på avgift** brukes.

I dette tilfellet beregnes beløpene på følgende måte:

- **Nettobeløp:** 10,00 
- **Avgift 1:** 10,00 × 10 prosent = 1,00 
- **Avgift 2:** 10,00 × 20 prosent = 2,00 
- **Avgift på avgift:** 3,00 × 25 prosent = 0,75
- **Total avgift:** 1,00 + 2,00 + 0,75 = 3,75 
- **Totalt fakturabeløp:** = 10,00 + 3,75 = 13,75

## <a name="advanced-functionality"></a>Avansert funksjonalitet

Denne delen beskriver avansert funksjonalitet for mva-kodeoppsettet for komplekse scenarier.

### <a name="tax-exemption"></a>Avgiftsfritak

Hvis du setter alternativet **Er Fritak** til **Ja** på hurtigfanen **Generelt**, overstyres mva-beløpet alltid til 0 (null), uansett faktisk avgiftssats.

Du kan settet feltet **Fritakskoder** for å angi årsaken til fritaket. 

Du kan aktivere hoveddataoppslag for feltet **Fritakskoder**. På den måten kan du velge blant de fritakskodeverdiene som er definert i Finance. Hvis du vil ha mer informasjon om hvordan du aktiverer hoveddataoppslag, kan du se [Aktiver hoveddataoppslag for mva-beregningskonfigurasjon](tax-service-set-up-environment-master-data-lookup.md).

Mva-satsen er for eksempel 25 prosent, og alternativet **Er Fritak** er satt til **Ja** i avgiftskoden. Fakturalinjen viser et antall på 10 varer til 1,00 kroner per stykk, og kunden får 10 prosent linjerabatt. I dette tilfellet beregnes beløpene på følgende måte:

- **Nettobeløp:** (10 × 1,00) – 10 prosent = 9,00 
- **Merverdiavgift:** 0,00 
- **Totalt fakturabeløp:** = 9,00 + 0,00 = 9,00

### <a name="use-tax"></a>Use tax

Hvis du setter alternativet **Er bruk avgift** til **Ja** på hurtigfanen **Generelt**, blir mva-beløpet postert til kontoen **Forfalt use tax** i stedet for kontoen for **Leverandørsammendrag**.

Mva-satsen er for eksempel 25 prosent, og alternativet **Er Bruk avgift** er satt til **Ja** i avgiftskoden. Fakturalinjen viser et antall på 10 varer til 1,00 kroner per stykk, og kunden får 10 prosent linjerabatt. I dette tilfellet beregnes beløpene på følgende måte:

- **Nettobeløp:** (10 × 1,00) – 10 prosent = 9,00 
- **Use tax:** 9,00 × 25 prosent = 2,25
- **Totalt fakturabeløp:** = 9,00 + 0,00 = 9,00

> [!IMPORTANT]
> Hvis både alternativet **Er Fritak** og **Er Bruk avgift** er satt til **Ja**, på en avgiftskode, gjenkjennes koden som avgiftsfri for salgstransaksjoner, og use tax for innkjøpstransaksjoner.

### <a name="reverse-charges"></a>Snudde avregninger

Hvis du setter **Er Snudd avregning**-alternativet til **Ja** i hurtigfanen **Generelt**, kan mva-satsen konfigureres som negativ. For et scenario for snudd avregning anbefaler vi at du definerer to avgiftskoder: én som har en positiv mva-sats, og en annen som har en negativ mva-sats. Begge avgiftskodene bør ha samme satsverdi, og alternativet **Er Snudd avregning** bør settes til **Ja** for avgiftskoden som har en negativ mva-sats. Hvis du vil ha mer informasjon om løsningen for snudd avregning i Finance, kan du se [Mekanisme for snudd avregning for MVA/GST-skjema](emea-reverse-charge.md).

For eksempel bestemmes det to avgiftskoder på én fakturalinje. Én mva-sats er 25 prosent. Den andre mva-satsen er -25 prosent, og alternativet **Er Snudd avregning** er satt til **Ja** i den andre avgiftskoden. Fakturalinjen viser et antall på 10 varer til 1,00 per stykk. I dette tilfellet beregnes beløpene på følgende måte:

- **Nettobeløp:** (10 × 1,00) = 10,00 
- **Avgiftskode 1:** 10,00 × 25 prosent = 2,50
- **Avgiftskode 2:** 10 × -25 prosent = -2,50
- **Totalt fakturabeløp:** 10,00 + 2,50 -2,50 = 10,00

### <a name="exclusion-from-base-amount-calculations"></a>Ekskluder fra grunnlagsbeløpsberegninger

Hvis du setter alternativet **Ekskluder fra grunnlagsbeløpsberegning** til **Ja** på hurtigfanen **Generelt**, utelates det beregnede mva-beløpet for mva-koden fra avgiftsgrunnlagsbeløpet for andre mva-kodeberegninger i pris inklusive-scenarioet.

Hvis du vil ha mer informasjon, kan du se [Beregn avgift på priser når Priser inkluderer mva. er aktivert](global-exclude-from-tax-base-amount-calculation.md).

### <a name="rates"></a>Satser

I hurtigfanen **Sats** kan du definere forskjellige mva-satser for ulike områder med avgiftsgrunnlagsbeløp. Når du skal beregne mva-beløpet, bruker mva-beregningstjenesten alltid satsen som samsvarer med avgiftsgrunnlagsbeløpet.

Mva-satser kan for eksempel konfigureres som vist i følgende tabell.

| Minimumsbeløp | Maksimumsbeløp | Sats   |
| -------------- | -------------- | ---------- |
| 0              | 1 000          | 10 prosent |
| 1 000          | 5 000          | 15 prosent |
| 5 000          | 10 000         | 20 prosent |
| 10 000         | 0              | 30 prosent |

I dette tilfellet beregnes avgiftsbeløp på følgende måte:

- Hvis avgiftsgrunnlagsbeløpet er 300,00, er mva-satsen 10 prosent, og avgiftsbeløpet er 300,00 × 10 prosent = 30,00.
- Hvis avgiftsgrunnlagsbeløpet er 3000,00, er mva-satsen 15 prosent, og avgiftsbeløpet er 3000,00 × 15 prosent = 450,00.
- Hvis avgiftsgrunnlagsbeløpet er 6000,00, er mva-satsen 20 prosent, og avgiftsbeløpet er 6000,00 × 10 prosent = 1200,00.
- Hvis avgiftsgrunnlagsbeløpet er 20 000, er mva-satsen 30 prosent, og avgiftsbeløpet er 20 000 × 30 prosent = 6000,00.

> [!NOTE]
> Hvis avgiftsgrunnlagsbeløpet kan samsvare med både maksimumsbeløpet på én linje og minimumsbeløpet på den andre linjen, vil grunnlaget bruke avgiftssatsen som samsvarer med minimumsgrunnlagsbeløpet. Hvis for eksempel avgiftsgrunnlagsbeløpet er 1000,00, er mva-satsen 15 prosent, og avgiftsbeløpet er 1000,00 × 15 prosent = 150,00.

### <a name="limits"></a>Grenser

I hurtigfanen **Grenser** kan du definere avgiftsgrenser for å overstyre det beregnede avgiftsbeløpet hvis mva-beløpet faller inn under minimums-/maksimumsområdet.

- Hvis det beregnede mva-beløpet er mer enn eller lik det maksimale avgiftsbeløpet som er konfigurert i hurtigfanen **Grenser**, vil det endelige mva-beløpet være lik maksimumsbeløpet for merverdiavgift.
- Hvis det beregnede avgiftsbeløpet er mindre enn minimumsavgiftsbeløpet som er konfigurert i **Grenser**-hurtigfanen, er det endelige avgiftsbeløpet 0 (null).

Mva-grensene konfigureres for eksempel på følgende måte:

- **Minimumsavgiftsbeløp:** 100 
- **Maksimumsavgiftsbeløp:** 1000

Hvis det beregnede mva-beløpet er 2000, er det endelige mva-beløpet 1000.

Hvis det beregnede mva-beløpet er 500, er det endelige mva-beløpet 500.

Hvis det beregnede mva-beløpet er 80, er det endelige mva-beløpet 0 (null).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
