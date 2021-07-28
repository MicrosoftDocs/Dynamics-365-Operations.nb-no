---
title: Rapport for mva-spesifikasjon etter finanstransaksjon
description: Dette emnet forklarer hvordan du bruker rapporten Mva-spesifikasjon etter finanstransaksjon til å vise og skrive ut informasjon om finanstransaksjoner som merverdiavgift beregnes for.
author: ericwang
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 447d319f5a96851f7eb3104b3330026d269e7dd1
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358815"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a>Rapport for mva-spesifikasjon etter finanstransaksjon
[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du bruker rapporten **Mva-spesifikasjon etter finanstransaksjon** til å vise og skrive ut informasjon om finanstransaksjoner som merverdiavgift beregnes for.

## <a name="tax-accounts-vs-non-tax-accounts"></a>Avgiftskontoer i forhold til ikke-avgiftskontoer

Rapporten **Mva-spesifikasjon etter finanstransaksjon** viser avgiftstransaksjoner for både avgiftskontoer og ikke-avgiftskontoer. Disse kontoene er kategorisert på følgende måte:

- **Avgiftskonto** – En konto anses å være avgiftskonto når en avgiftstransaksjon posteres, og hovedkontoen på **Merverdiavgift**-journallinjen er en avgiftskonto, for eksempel en utgående mva-konto eller en konto for innkommende merverdiavgift.
- **Ikke-avgiftskonto** – En konto anses å være ikke-avgiftskonto når en avgiftstransaksjon posteres, og hovedkontoen på den opprinnelige transaksjonen er en ikke-avgiftskonto, for eksempel en inntektskonto eller en utgiftskonto.

For avgiftskontoer viser kolonnene **0** (null) for kolonnene **Grunnlag**, **Innkommende merverdiavgift** og **Utgående merverdiavgift** . For ikke-avgiftskontoer viser disse kolonnene beløp.

## <a name="filtering-the-data-on-the-report"></a>Filtrere dataene i rapporten

Når du genererer rapporten, er følgende felt tilgjengelige. Du kan bruke disse feltene til å filtrere dataene som vises i rapporten.

| Felt                      | Beskrivelse |
|----------------------------|-------------|
| Dato                       | Bruk feltene i delene **Fra** og **Til** for å definere et datoområde for avgiftstransaksjonene. |
| Hovedkonto               | Bruk feltene i delene **Fra** og **Til** for å definere et datoområde for hovedkontoer. |
| Mva-kode             | Bruk feltene i delene **Fra** og **Til** for å definere et datoområde for mva-koder. |
| Gruppering                   | Velg om rapporten skal grupperes etter finanskonto eller mva-kode. |
| Delsum etter mva-kode | Sett dette alternativet til **Ja** for å vise delsummer etter mva-kode. |
| Bare summer                | Sett dette alternativet til **Ja** for å vise bare totaler. |
| Bare hovedkontoer         | Sett dette alternativet til **Ja** for å ta med bare hovedkontoer i rapporten. |

## <a name="showing-only-non-tax-accounts-on-the-report"></a>Vise bare ikke-avgiftskontoer i rapporten

Hvis du vil vise bare ikke-avgiftskontoer i rapporten, definerer du en filter betingelse, for eksempel en stjerne (\*), som vist i illustrasjonen nedenfor.

![Rapport som viser ikke-avgiftskontoer.](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]