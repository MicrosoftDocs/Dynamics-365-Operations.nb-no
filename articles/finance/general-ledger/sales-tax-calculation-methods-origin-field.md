---
title: Beregningsmåter av merverdiavgift i grunnlagsfeltet
description: Denne artikkelen beskriver alternativene i Opprinnelse-feltet på siden for mva-koder, og hvordan mva beregnes basert på det valgte alternativet for en mva-kode.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be935b80e06158d9634989ba03747f4a59247f8e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204936"
---
# <a name="sales-tax-calculation-methods-in-the-origin-field"></a>Beregningsmåter av merverdiavgift i grunnlagsfeltet

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver alternativene i Opprinnelse-feltet på siden for mva-koder, og hvordan mva beregnes basert på det valgte alternativet for en mva-kode.

For hver mva-kode du oppretter på siden Mva-koder, må du velge beregningsmåten som skal brukes for grunnlagsbeløpet for merverdiavgift i grunnlagsfeltet.

## <a name="percentage-of-net-amount"></a>Prosent av nettobeløp
Beregningsmåten Prosent av nettobeløp er standardverdien i grunnlagsfeltet. Merverdiavgiften beregnes som en prosent av innkjøps- eller salgsbeløpet, minus eventuell merverdiavgift.
### <a name="example"></a>Eksempel

Avgiftssatsen er 25 %. Fakturalinjen viser et antall på 10 varer til 1,00 krone hver, og kunden får 10 % linjerabatt. Nettobeløp: (10 x 1,00)-10% = 9,00 merverdiavgift: 9,00 x 25% = 2,25 totalbeløp: 9,00 + 2,25 = 11,25

## <a name="percentage-of-gross-amount"></a>Prosent av bruttobeløp
Hvis du velger metoden Prosent av bruttobeløp, beregnes merverdiavgift som en prosent av bruttosalgsbeløpet. Bruttobeløpet er nettolinjebeløpet pluss alle skatter og avgifter for linjen unntatt én avgift med opprinnelse = prosent av bruttobeløp.
### <a name="example"></a>Eksempel

Skattemyndighetene har innført spesielle avgifter på en vare. Avgiftsbeløpene legges til nettobeløpet før merverdiavgift beregnes. Gitt følgende mva-koder:
-   AVGIFT 1 = 10%, ved bruk av beregningsmåten prosent av nettobeløp
-   AVGIFT 2 = 20%, ved bruk av beregningsmåten prosent av nettobeløp
-   MERVERDIAVGIFT = 25%, ved bruk av beregningsmåten prosent av bruttobeløp

Hvis nettobeløpet er 10,00, er AVGIFT 1 1,00 (10,00 x 10%) og AVGIFT 2 = 2,00 (10,00 x 20%). Beløpene er som følger: bruttobeløp: nettobeløp + AVGIFT 1 beløp AVGIFT 2 beløp (10,00 + 1,00 + 2,00) = 13,00 MERVERDIAVGIFT = 13,00 x 25% = 3,25 Total AVGIFT og MERVERDIAVGIFT: 1,00 + 2,00 + 3,25 = 6,25 totalbeløp: 10,00 + 6,25 = 16,25

| **Obs!**                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bare én avgiftskode med opprinnelse = prosenten av bruttobeløpet kan brukes for en transaksjon. Hvis mer enn én eller slik avgiftskode bestemmes for en transaksjon, vises en feil om at merverdiavgift ikke kan beregnes. |


<a name="percentage-of-sales-tax"></a>Prosent av merverdiavgift
-----------------------

Når du velger prosent av merverdiavgift i grunnlagsfeltet, beregnes merverdiavgift som en prosent av merverdiavgiften som er valgt i feltet Merverdiavgift på merverdiavgift. Merverdiavgiften som er valgt i feltet Merverdiavgift på merverdiavgift, beregnes først. Den andre merverdiavgiften beregnes deretter basert på det første mva-beløpet.
### <a name="example"></a>Eksempel

Gitt følgende mva-koder:
-   AVGIFT 1 = 10%, ved bruk av beregningsmåten prosent av nettobeløp
-   AVGIFT 2 = 20%, ved bruk av metoden Prosent av merverdiavgift, med Avgift 1 i feltet Merverdiavgift på merverdiavgift
-   MERVERDIAVGIFT 1 = 25%, ved bruk av metoden prosent av bruttobeløp

Nettobeløp: 10,00 AVGIFT 1: 10,00 x 10% = 1,00 AVGIFT 2: 1,00 x 20% = 0,20 bruttobeløp: 10,00 + 1,00 + 0,20 = 11,20 MERVERDIAVGIFT: 11,20 x 25% = 2,80 total AVGIFT og MERVERDIAVGIFT: 1,00 + 0,20 + 2,80 = 4,00 totalbeløp: 10,00 + 4,00 = 14,00

| **Obs!**                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mva-beregninger med flere nivåer er ikke mulig. En avgift kan ikke beregnes basert på en avgift som allerede er beregnet basert på en annen avgift. Flere mva på mva-koder på enkeltnivå kan beregnes på en transaksjon. |

## <a name="amount-per-unit"></a>Beløp per enhet
Når du velger Beløp per enhet i grunnlagsfeltet, beregnes merverdiavgift som et fast beløp per enhet ganget med antallet på dokumentlinjen. En enhet må velges i Enhet-feltet. Beløpet per enhet angis på siden Verdier for merverdiavgiftskode.
### <a name="example"></a>Eksempel

Mva-koden er definert som: USD 1,20 per enhet = boks på en salgsfakturalinje 25 bokser for en vare selges Mva-sats beregnes som 25 x 1,20 = 30,00

| **Obs!**                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hvis transaksjonen angis i en annen enhet enn enheten som er angitt i mva-koden, omregnes den automatisk basert på enhetsomregningene som er angitt på Enhetsomregninger-siden. |

###  <a name="amount-per-unit-additional-option"></a>Beløp per enhet, tilleggsalternativ

I kategorien Beregning kan du velge om et beløp per enhet beregnet mva beregnes før andre mva-koder og legges til nettobeløpet før andre mva-koder med opprinnelse = prosent av nettobeløp beregnes.

### <a name="examples"></a>Eksempler

Anta at vi beregner 2 avgiftskoder i en transaksjon:

-   AVGIFT: Opprinnelse = beløp per enhet og en merverdiavgift, verdien er satt til 5,00 per enhet = stk.
-   MERVERVIDAVGIFT: Opprinnelse = som vist i eksemplene nedenfor, settes verdien til 25%

Vi selger 1 stykk av en vare til en enhetspris på 10,00
#### <a name="example-1"></a>Eksempel 1

MERVERVIDAVGIFT: Opprinnelse = metoden prosent av bruttobeløp, alternativet Beregn før merverdiavgift har ingen innvirkning fordi MERVERVIDAVGIFT beregnes som en prosent av bruttobeløpet. AVGIFT: 1 x 5,00 = 5,00 bruttobeløp: 10,00 + 5,00 = 15,00 MERVERVIDAVGIFT: 15,00 x 25% = 3.75 total merverdiavgift: 5,00 + 3,75 = 8,75 totalbeløp: 10,00 + 8,75 = 18,75

#### <a name="example-2"></a>Eksempel 2

MERVERVIDAVGIFT: Opprinnelse = prosent av nettobeløp, alternativet Beregn før merverdiavgift er ikke valgt for avgiftsberegningen. Nettobeløp: 10,00 AVGIFT: 1 x 5,00 = 5,00 MERVERVIDAVGIFT: 10,00 x 25% = 2,50 Total merverdiavgift: 5,00 + 2,50 = 7,50 Totalbeløp: 10,00 + 7,50 = 17,50

#### <a name="example-3"></a>Eksempel 3

MERVERVIDAVGIFT = Opprinnelse = prosent av nettobeløp, alternativet Beregn før merverdiavgift er valgt for avgiftsberegningen. Nettobeløp: 10,00 AVGIFT: 1 x 5,00 = 5,00 MERVERVIDAVGIFT: (10,00 + 5,00) x 25% = 3,75 Total merverdiavgift: 5,00 + 3,75 = 8,75 Totalbeløp: 10,00 + 8,75 = 18,75

#### <a name="example-4"></a>Eksempel 4

Resultatet i eksempel 3 og 1 er det samme fordi det bare er én avgift. Anta at du har to avgifter, og bare én av dem er inkludert i nettobeløpet for mva-beregningen: AVGIFT 1: 5,00, med samme beløp per enhet-metode og alternativet Beregn før merverdiavgift er valgt AVGIFT 2: 2,50, med beløp per enhet-metoden og alternativet Beregn før merverdiavgift ikke er valgt Merverdiavgift : 25%, med metoden Prosent av nettobeløp Nettobeløp: 10,00 AVGIFT 1: 1 x 5,00 = 5,00 AVGIFT 2: 1 x 2,50 = 2,50 Nettobeløpet er mva-pliktig: 10,00 + 5,00 = 15,00 MERVERDIAVGIFT: 15,00 x 25% = 3.75 Total merverdiavgift, inkludert avgifter: 5,00 + 2,50 + 3,75 = 11,25 Totalbeløp: 10,00 + 11,25 = 21,25 MERVERDIAVGIFT på 25% beregnes for summen av nettobeløpet (10,00) + AVGIFT 1 (5,00) = 15,00. AVGIFT 2 legges til avgiftsbeløpet etter at merverdiavgiften er beregnet.

## <a name="calculated-percentage-of-net-amount"></a>Beregnet prosent av nettobeløp
Beregnet prosent av nettobeløp håndterer avgiftsberegning forskjellig, avhengig av innstillingen for parameteren Beløp inkludert merverdiavgift for bilaget eller journalen.
### <a name="example-1"></a>Eksempel 1

Dokumentet / journalen er satt til Beløp inkludert merverdiavgift = Ja Transaksjonslinjebeløp: 10,00 Avgiftssats: 25% Merverdiavgift: Transaksjonslinjebeløp x avgiftssats (10,00 x 25%) = 2,50 Avgiftsgrunnlagsbeløp (opprinnelig beløp): Transaksjonslinjebeløp - Merverdiavgift (10,00 2,50) = 7,50

### <a name="example-2"></a>Eksempel 2

Dokumentet / journalen er satt til Beløp inkludert merverdiavgift = Nei Transaksjonslinjebeløp: 10,00 Avgiftssats: 25% Merverdiavgift: (Transaksjonslinjebeløp x avgiftssats) / (100 - avgiftssats) (10,00 x 25%) / (100% - 25%) = 3,33 Avgiftsgrunnlagsbeløp (opprinnelig beløp): Transaksjonslinjebeløp = 10,00



<a name="additional-resources"></a>Tilleggsressurser
--------

[Mva-satser basert på feltene grensegrunnlag og beregningsmetoder](marginal-base-field.md)

[Hele beløp og alternativer for intervallberegning for mva-koder](whole-amount-interval-options-sales-tax-codes.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]