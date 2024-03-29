---
title: Støtte for dobbel valuta for avgift
description: Denne artikkelen beskriver hvordan du kan utvide funksjonen for dobbelt valutaregnskap i avgiftsdomenet og virkningen for avgiftsberegning og -postering
author: EricWang
ms.date: 12/11/2020
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
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 13d70d964a83c2efba090244d549bdb38ad25af2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909047"
---
# <a name="dual-currency-support-for-sales-tax"></a>Støtte for dobbel valuta for merverdiavgift
[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du kan utvide funksjonen for dobbelt valutaregnskap for merverdiavgift og virkningen for merverdiavgiftsberegning, -postering og -utligninger.

Funksjonen for dobbel valuta for Dynamics 365 Finance ble innført i versjon 8.1 (oktober 2018). Den endrer måten regnskapsoppføringer i rapporteringsvalutaen beregnes på.

I tidligere versjoner ble transaksjoner konvertert til rapporteringsvalutaen i følgende rekkefølge: 

- Totalen for transaksjonen ble beregnet i transaksjonsvalutaen > transaksjonsbeløpet ble konvertert til regnskapsvalutaen > regnskapsvalutabeløpet ble konvertert til rapporteringsvalutaen

Etter aktivering av funksjonen for dobbel valuta ble transaksjoner konvertert til rapporteringsvalutaen i følgende rekkefølge:

- Beløp i transaksjonsvaluta > Rapporteringsvalutabeløp

Hvis du vil ha mer informasjon om dobbel valuta, kan du se [Dobbel valuta](dual-currency.md).

Som en konsekvens av støtte for dobbel valuta er to nye funksjoner tilgjengelige i funksjonsstyringen: 

- Omregning av merverdiavgift (nytt i versjon 10.0.13)
- Angi finansdimensjoner i de realiserte resultatkontoene for valutajustering for mva-utligning (ny i versjon 10.0.17)

Støtte for dobbel valuta for merverdiavgift sikrer at avgifter beregnes nøyaktig i mva-valutaen, og at mva-utligningsperioden beregnes nøyaktig i både regnskapsvalutaen og rapporteringsvalutaen.

## <a name="sales-tax-conversion"></a>Mva-omregning

Parameteren **Omregning av merverdiavgift** gir to alternativer for å konvertere merverdiavgiftsbeløpet fra transaksjonsvalutaen til avgiftsvalutaen. 

- Regnskapsvaluta: Banen er "Beløp i transaksjonsvaluta > Beløp i regnskapsvaluta > Beløp i avgiftsvaluta". Valutakurstypen for regnskapsvalutaen (konfigurert i finansoppsett) blir brukt til valutaomregningen.
- Rapporteringsvaluta: Banen er "Beløp i transaksjonsvaluta > Beløp i rapporteringsvaluta > Beløp i avgiftsvaluta". Valutakurstypen for rapporteringsvalutaen (konfigurert i finansoppsett) blir brukt til valutaomregningen.

### <a name="example"></a>Eksempel

Et enkelt eksempel for å demonstrere denne funksjonaliteten er:

Valutaoppsett for finans og avgift

| Transaksjonsvaluta | Regnskapsvaluta | Rapporteringsvaluta | Avgiftsvaluta |
| -------------------- | ------------------- | ------------------ | ------------ |
| EUR                  | USD                 | GBP                | GBP          |

Valutakurs

| Fra valuta | Til valuta | Omregningsfaktor | Valutakurs |
| ------------- | ----------- | ------ | ------------- |
| EUR           | USD         | 1      | 1.11          |
| EUR           | GBP         | 1      | 0.83          |
| USD           | GBP         | 1      | 0.75          |

Beregning av avgiftsbeløp i ulike parameteralternativer

Avgiftsbeløp = 100 euro

| Omregningsparametere for merverdiavgift | Transaksjonsvaluta (EUR) | Regnskapsvaluta (USD) | Rapporteringsvaluta (GBP) | Avgiftsvaluta (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Regnskapsvaluta             | 100                        | 111                       | 83                       | **83.25**          |
| Rapporteringsvaluta              | 100                        | 111                       | 83                       | **83**             |

Denne parameteren kan konfigureres på grunnlag av samsvarsbehovet fra skattemyndighetene.


### <a name="upgrade-consideration"></a>Hensyn ved oppgradering

Denne funksjonen vil bare gjelde for nye transaksjoner. For mva-transaksjoner som allerede er lagret i TAXTRANS-tabellen, men ikke utlignet ennå, vil ikke systemet omberegne mva-beløpet i mva-valutaen fordi valutakursen ved tidspunktet for postering av avgift allerede mangler.

For å hindre foregående scenario anbefaler vi at du endrer denne parameterverdien i en ny (ren) mva-utligningsperiode som ikke inneholder noen ikke-utlignede mva-transaksjoner. Hvis du vil endre denne verdien midt i en mva-utligningsperiode, kan du kjøre programmet "Utlign og poster merverdiavgift" for gjeldende avgiftsutligningsperiode før du endrer denne parameterverdien.

Denne funksjonen legger til regnskapsoppføringer som avklarer gevinst og tap fra valutakurser. Oppføringene vil bli gjort i de realiserte valutajusteringsresultatkontoene når revaluering utføres under mva-utligningen. Hvis du vil ha mer informasjon, kan du se delen [Automatisk saldo for avgiftsutligning i rapporteringsvaluta](#tax-settlement-auto-balance-in-reporting-currency) senere i denne artikkelen.

> [!NOTE]
> Under utligningen tas informasjon for finansdimensjoner fra mva-kontoer, som er balansekontoer, og angis i resultatkontoer for valutajustering, som er resultatkontoer. Fordi det kan forekomme begrensninger på verdien til finansdimensjoner mellom balansekontoer og resultatregnskapskontoer, kan det oppstå en feil under utligningen og postering av merverdiavgiftsprosessen. Hvis du vil unngå å måtte endre kontostrukturer, kan du aktivere funksjonen "Fyll ut finansdimensjoner til de realiserte valutajusteringsresultatkontoene for utligning av merverdiavgift". Denne funksjonen tvinger avledingen av finansdimensjoner til valutajusteringsresultatkontoer. 

## <a name="track-reporting-currency-tax-amount"></a>Spore avgiftsbeløp i rapporteringsvaluta

Tre nye felt ble lagt til i mva-relaterte tabeller for å spore beløp i rapporteringsvalutaen. Disse feltene finnes i tabellene TAXUNCOMMITTED og TAXTRANS:

- TaxAmountRep: avgiftsbeløp i rapporteringsvaluta
- TaxBaseAmountRep: grunnlagsbeløp i rapporteringsvaluta
- TaxInCostPriceRep: ikke-fradragsberettiget beløp i rapporteringsvaluta

For avgift som bare er lagret i TAXUNCOMMITTED-tabellen, men som ennå ikke er postert, vil systemet omberegne mva-beløpet i rapporteringsvalutaen på tidspunktet for postering og lagring i TAXTRANS-tabellen.

Denne versjonen vil ikke inkludere endringer i rapporter og skjemaer som viser mva-beløpet i rapporteringsvalutaen. Endringer i rapporter og skjemaer blir levert i den fremtidige versjonen.



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a>Automatisk saldo for avgiftsutligning i rapporteringsvaluta

Hvis mva-utligningen ikke er balansert i rapporteringsvalutaen av en bestemt årsak, for eksempel når omregningsbanen for merverdiavgift er "regnskapsvaluta" eller endring av valutakursen i en enkelt avgiftsutligningsperiode, vil systemet automatisk generere regnskaps oppføringer for å justere avviket i finansoppsett.

Bruk det forrige eksemplet til å demonstrere denne funksjonen, og anta at dataene i TAXTRANS-tabellen på posteringstidspunktet er følgende.

| Omregningsparametere for merverdiavgift | Transaksjonsvaluta (EUR) | Regnskapsvaluta (USD) | Rapporteringsvaluta (GBP) | Avgiftsvaluta (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Regnskapsvaluta             | 100                        | 111                       | 83                       | **83.25**          |
| Rapporteringsvaluta              | 100                        | 111                       | 83                       | **83**             |

Når du kjører programmet for mva-utligning i løpet av månedsavslutningen, vil regnskapsposten være som følger.
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a>Scenario: merverdiavgiftsomregning = "Regnskapsvaluta"

| Hovedkonto           | Transaksjonsvaluta (GBP) | Regnskapsvaluta (USD) | Rapporteringsvaluta (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Utgående/innkommende merverdiavgift | -83,25                     | -111                      | -83,25                   |
| Avgiftsutligning         | 83.25                      | 111                       | 83.25                    |
| Realisert fortjeneste/tap     | 0                          | 0                         | -0,25                    |
| Utgående/innkommende merverdiavgift | 0                          | 0                         | 0.25                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a>Scenario: merverdiavgiftsomregning = "Rapporteringsvaluta"


| Hovedkonto           | Transaksjonsvaluta (GBP) | Regnskapsvaluta (USD) | Rapporteringsvaluta (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Utgående/innkommende merverdiavgift | -83                        | -110,67                   | -83                      |
| Avgiftsutligning         | 83                         | 110.67                    | 83                       |
| Realisert fortjeneste/tap     | 0                          | 0.33                      | 0                        |
| Utgående/innkommende merverdiavgift | 0                          | -0,33                     | 0                        |



Hvis du vil ha mer informasjon, kan du se følgende emner:

- [Dobbel valuta](dual-currency.md)
- [Oversikt over merverdiavgift](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
