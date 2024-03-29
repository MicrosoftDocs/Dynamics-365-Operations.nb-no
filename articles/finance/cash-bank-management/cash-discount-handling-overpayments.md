---
title: Kontantrabatter for overbetalinger
description: Denne artikkelen inneholder scenarier som viser hvordan en betaling skal håndteres når kunden tar en kontantrabatt, men også overbetaler.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 14171
ms.assetid: a94d0fd0-57ba-4054-93c8-519d01d50e19
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7c4e98481bc3607d3dce68a6b6cb0478524442f
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804162"
---
# <a name="cash-discounts-for-overpayments"></a>Kontantrabatter for overbetalinger

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder scenarier som viser hvordan en betaling skal håndteres når kunden tar en kontantrabatt, men også overbetaler. 

En faktura regnes som overbetalt når betalingsbeløpet er større enn fakturabeløpet minus kontantrabatten. Når du skal angi hvordan et kontantrabattavvik som du kan få, håndteres når en faktura er overbetalt, bruker du feltene **Håndtering av kontantrabatt** og **Maksimal over- eller underbetaling** på siden **Kundeparametere**. I eksemplet nedenfor har kunden overbetalt fakturaen med 0,50.

| Fakturatotal | Kontantrabatt tilgjengelig | Beløpet som skal betales, som inkluderer kontantrabatten | Beløpet kunden faktisk betaler |
|---------------|-------------------------|-----------------------------------------------------|-----------------------------------|
| 105,00        | 10,50                   | 94,50                                               | 95,00                             |

## <a name="cash-discount-administration--specific"></a>Håndtering av kontantrabatt = Presis
Når **Spesifikk** er valgt i feltet **Håndtering av kontantrabatt** på siden **Kontoer for automatiske transaksjoner**, blir hele kontantrabatten tatt. Overbetalingsbeløpet blir enten postert til en finanskonto for en kontantrabattdifferanse, eller blir igjen som en saldo på kundekontoen. Virkemåten avhenger av om hvor overbetalingsbeløpet er mellom 0,00 og beløpet som er angitt i feltet **Maksimal over- eller underbetaling**, eller om hvor overbetalingsbeløpet er større enn beløpet for **Maksimal over- eller underbetaling**.

### <a name="scenario-1"></a>Scenario 1

I dette scenarioet er overbetalingsbeløpet mellom 0,00 og maksimal over- eller underbetaling. En faktura for 105,00 registreres, og en kontantrabatt er tilgjengelig hvis fakturaen betales innen sju dager.

| Fakturatotal | Kontantrabatt tilgjengelig | Beløpet som skal betales, som inkluderer kontantrabatten |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Kunden sender en betaling for 95,00 innenfor kontantrabattperioden. Betalingen utlignes mot fakturaen for 105,00. Når fakturaen og betalingen utlignes, opprettes følgende transaksjoner for kunden i kundereskontro.

| Transaksjon   | Beløp | Saldo |
|---------------|--------|---------|
| Faktura       | 105,00 | 0,00    |
| Betaling       | -95,00 | 0,00    |
| Kontantrabatt | -10,50 | 0,00    |

Følgende regnskapsoppføringer genereres for betalingen og utligningen.

**Betaling**

| Konto             | Debetbeløp | Kreditbeløp |
|---------------------|--------------|---------------|
| Kontant                | 95,00        |               |
| Kundereskontro |              | 95,00         |

**Utligning**

| Konto                                                                                                          | Debetbeløp | Kreditbeløp |
|------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| Kontantrabatt (feltet **Hovedkonto for kunderabatter** på siden **Kontantrabatt**)                 | 10,50        |               |
| Kundereskontro                                                                                              |              | 10,50         |
| Kundekontantrabatt (feltet **Kundekontantrabatt** på siden **Konto for automatiske transaksjoner**) |              | 0.50          |
| Kundereskontro                                                                                              | 0.50         |               |

### <a name="scenario-2"></a>Scenario 2

I dette scenarioet overskrider overbetalingsbeløpet det maksimale over- eller underbetalingsbeløpet. En faktura for 105,00 registreres, og en kontantrabatt er tilgjengelig hvis fakturaen betales innen sju dager.

| Fakturatotal | Kontantrabatt tilgjengelig | Beløpet som skal betales, som inkluderer kontantrabatten |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Kunden sender en betaling for 95,00 innenfor kontantrabattperioden. Betalingen utlignes mot fakturaen for 105,00. Når fakturaen og betalingen utlignes, opprettes følgende transaksjoner for kunden i kundereskontro.

| Transaksjon   | Beløp | Saldo |
|---------------|--------|---------|
| Faktura       | 105,00 | 0,00    |
| Betaling       | -95,00 | -0,50   |
| Kontantrabatt | -10,50 | 0,00    |

Overbetalingsbeløpet på 0,50 blir igjen som en åpen saldo på betalingen, og kan utlignes mot en annen faktura. Følgende regnskapsoppføringer genereres for betalingen og utligningen. 

**Betaling**

| Konto             | Debetbeløp | Kreditbeløp |
|---------------------|--------------|---------------|
| Kontant                | 95,00        |               |
| Kundereskontro |              | 95,00         |

**Utligning**

| Konto                                                                                          | Debetbeløp | Kreditbeløp |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Kontantrabatt (feltet **Hovedkonto for kunderabatter** på siden **Kontantrabatt**) | 10,50        |               |
| Kundereskontro                                                                              |              | 10,50         |

## <a name="cash-discount-administration--unspecific"></a>Håndtering av kontantrabatt = Løs
Når **Løs** er valgt i feltet **Håndtering av kontantrabatt** på siden **Kontoer for automatiske transaksjoner**, reduseres kontantrabattbeløpet med overbetalingsbeløpet. Dette gjelder alltid, uansett om overbetalingsbeløpet er over eller under beløpet som er angitt i feltet **Maksimal over- eller underbetaling**.

### <a name="scenario-3"></a>Scenario 3

I dette scenarioet registreres en faktura for 105,00, og en kontantrabatt er tilgjengelig hvis fakturaen betales innen sju dager.

| Fakturatotal | Kontantrabatt tilgjengelig | Beløpet som skal betales, som inkluderer kontantrabatten |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Kunden sender en betaling for 95,00 innenfor kontantrabattdatoen. Betalingen utlignes mot fakturaen for 105,00. Når fakturaen og betalingen utlignes, opprettes følgende transaksjoner for kunden i kundereskontro.

| Transaksjon   | Beløp | Saldo |
|---------------|--------|---------|
| Faktura       | 105,00 | 0,00    |
| Betaling       | -95,00 | -0,00   |
| Kontantrabatt | -10,00 | 0,00    |

Kontantrabattbeløpet reduseres fra 10,50 til 10,00. Betalingen og fakturaen betraktes som utlignet. 

**Betaling**

| Konto             | Debetbeløp | Kreditbeløp |
|---------------------|--------------|---------------|
| Kontant                | 95,00        |               |
| Kundereskontro |              | 95,00         |

**Utligning**

| Konto                                                                                          | Debetbeløp | Kreditbeløp |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Kontantrabatt (feltet **Hovedkonto for kunderabatter** på siden **Kontantrabatt**) | 10,50        |               |
| Kundereskontro                                                                              |              | 10,50         |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
