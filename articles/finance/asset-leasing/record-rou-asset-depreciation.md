---
title: Postere avskrivning for bruksrettseiendel (forhåndsversjon)
description: Denne artikkelen forklarer hvordan du oppretter journaloppføringen for nedbetalingen som kreves for leieavtaler som er oppført i balansen til en organisasjon.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseAssetSchedule
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 93e521cf409af4c01d625f27bdd7a7564e471bd9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903283"
---
# <a name="record-right-of-use-asset-depreciation-preview"></a>Postere avskrivning for bruksrettseiendel (forhåndsversjon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


For leieavtaler som er oppført i balansen til en organisasjon, nedbetales bruksrettseiendelen på månedlig basis. Denne artikkelen forklarer hvordan du oppretter journaloppføringen for nedbetalingen. Nedbetalingen debiterer utgiftsfinanskontoen og kreditere den akkumulerte avskrivningsfinanskontoen basert på oppsettet av posteringsprofilen og leietypen. Disse oppføringene kan opprettes for hver leieavtale, eller de kan opprettes for flere leieavtaler ved å bruke funksjonen for satsvis journal.

## <a name="asset-depreciation-schedule"></a>Avskrivningsplan for aktiva

1. Velg en leieavtale på siden **Leiesammendrag**. Deretter velger du **Tablåer \> Avskrivningsplan for aktiva** for å åpne siden **Avskrivningsplan for aktiva**.

    Journaloppføring for avskrivningskostnad for bruksrettseiendel er basert på beløpet i kolonnen **Avskrivningsutgift**. Hvis du vil ha et eksempel på retningslinjene for regnskapsstandardsamsvar, kan du se [Beregning av nedbetalingsutgift for bruksrettseiendel for finansiell leie](#calculation-of-rou-asset-amortization-expense-for-finance-leases) senere i denne artikkelen.
    
2. Velg avskrivningsperioden, og velg deretter **Opprett Journal**. Du får en melding som angir at journalen som skal brukes til å registrere avskrivning, er opprettet.
3. Velg **Journaler \> Journaler for aktivaleie** for å åpne siden **Journaler for aktivaleie**, der du kan se journaloppføringen for avskrivningsutgift som ble opprettet.

   Systemet låser bestemte økonomiske felt fra å bli redigert for å forhindre avvik mellom transaksjonene og planene. Noen av feltene som er låst, inkluderer: **Konto**, **Beløp**, **Finansdimensjoner**, **Valuta** og **Transaksjonstype**. I tillegg kan du ikke legge til eller slette journaloppføringslinjer i noen journaloppføringer for anleggsmiddelleasing, fordi dette kan føre til avvik mellom planene og transaksjonene.

4. Velg journaloppføringen, og velg deretter **Poster** for å registrere avskrivningsoppføringen til økonomimodulen.

## <a name="calculation-of-rou-asset-amortization-expense-for-operating-leases"></a>Beregning av nedbetalingsutgift for bruksrettseiendel for gjeldende leie

Avskrivningsutgiftene for gjeldende leie beregnes som forskjellen mellom den månedlige lineære leieutgiften og den månedlige renteutgiften på leieforpliktelsen, i henhold til Accounting Standards Codification-emne 842 (ASC 842), som er standard i Generally Accepted Accounting Principles i USA (US GAAP). Leieavtalen for lineær avskrivning beregnes som summen av alle leiebetalinger delt på leieavtalen i måneder. (Summen av leiebetalinger omfatter alle forskuddsbetalinger, opprinnelig direkte kostnad, avviklingskostnader og leieinsentiver.) Følgende tabell viser et eksempel på nedbetalingskostnader for gjeldende leie.

### <a name="example-of-rou-asset-amortization-expense-for-operating-leases"></a>Eksempel på nedbetalingsutgift for bruksrettseiendel for gjeldende leie

| Felt                                          | Verdi       |
|------------------------------------------------|-------------|
| Betalingsbeløp                                 | 1 000       |
| Betalingsfrekvens                              | Månedlig     |
| Leietermin (måneder)                            | 24          |
| Totalt antall leiebetalinger                           | 24,000      |
| Trinnvis lånerente                     | 5 %          |
| Annuitetstype                                   | Annuitetsforfall |
| Sammensetningsintervall                           | Månedlig     |
| Nåværende verdi av fremtidige minimum leiebetalinger | 22,888.87   |

Som tidligere nevnt beregnes den lineære leieutgiften som summen av alle betalinger delt på leieavtalen. Systemet beregner automatisk den månedlige renteutgiften i tidsplanen for gjeldsnedbetaling. Renteutgiften beregnes ved hjelp av metoden for effektiv rentesats. Systemet vil bruke lineær leiekostnad til å trekke fra renteutgiften for hver måned. Verdien brukes til å redusere bruksrettseiendelen.

| Måned | Lineære leiekostnad | Renteutgift                        | Beregning av nedbetalingskostnad for bruksrettseiendel |
|-------|--------------------------|-----------------------------------------|-----------------------------------------------|
| 1     | (24.000 ÷ 24) = 1.000,00 | (22.888,87 – 1000) × (5 % ÷ 12) = 91,20 | 1000 – 91,20 = 908,80                        |
| 2     | (24.000 ÷ 24) = 1.000,00 | (21.980,08 – 1000) × (5 % ÷ 12) = 87,42 | 1000 – 87,42 = 912,58                        |
| 3     | (24.000 ÷ 24) = 1.000,00 | (21.067,49 – 1000) × (5 % ÷ 12) = 83,62 | 1000 – 83,62 = 916,39                        |

> [!NOTE]
> I henhold til ASC 842 klassifiseres avskrivningen av bruksrettseiendelen for gjeldende leie som en leieutgift i resultat regnskapet. For synlighet beskriver aktivaleie posten som avskrivning av bruksrettseiendelen. Debetposten bør imidlertid tilordnes til en utgiftskonto for gjeldende leie, og kreditposten bør tilordnes direkte til bruksrettseiendelen for den gjeldende leien. Men i leieparameterne kan du angi at kreditposter skal opprettes til en akkumulert avskrivningskonto for bruksrettseiendeler.

Hvis leien klassifiseres som gjeldende leie, beregnes den månedlige avskrivningen etter verdiforringelse ved hjelp av lineær avskrivning.

## <a name="calculation-of-rou-asset-amortization-expense-for-finance-leases"></a>Beregning av nedbetalingsutgift for bruksrettseiendel for finansiell leie

For leieavtaler som har en finansklassifisering, beregner systemet nedbetalingen av bruksrettseiendelen på lineær basis. Derfor vil avskrivningsutgiften være den samme for hver måned.

I samsvar med International Financial Reporting Standard 16 (IFRS 16) og ASC 842 vil aktivaet bli nedbetalt i løpet av leieperioden eller aktivaets levetid, avhengig av hva som er kortest. Hvis parameteren **Overføring av eierskap** er aktivert for leieavtalen, vil leieavtalen automatisk bli avskrevet i løpet av aktivaets levetid.

### <a name="example-of-rou-asset-amortization-expense-for-finance-leases"></a>Eksempel på nedbetalingsutgift for bruksrettseiendel for finansiell leie

| Felt                                | Verdi                                   |
|--------------------------------------|-----------------------------------------|
| Startsaldo for bruksrettseiendel | 22,889.87                               |
| Leietermin (måneder)                  | 24                                      |
| Aktivalevetid (måneder)           | 36                                      |
| Måned                                | Nedbetalingsutgift for bruksrettseiendel |
| 1                                    | 22.889,87 ÷ 24 = 953,74                 |
| 2                                    | 22.889,87 ÷ 24 = 953,74                 |
| 3                                    | 22.889,87 ÷ 24 = 953,74                 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
