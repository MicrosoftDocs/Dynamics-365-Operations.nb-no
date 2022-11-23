---
title: Revaluering av valuta i et konsolideringsfirma
description: Denne artikkelen beskriver hvordan å revaluere valuta i et konsolideringsselskap.
author: aprilolson
ms.date: 10/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: twheeloc
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c05ef0d4d05d5113d3b858dafe49ee9c1c7211d9
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779669"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a>Revaluering av valuta i et konsolideringsfirma

[!include [banner](../includes/banner.md)]

Når du konsoliderer data fra én regnskapsvaluta til en annen, du må fortsatt kjøre valutarevaluering hvis det er endringer i valutakurser, slik at kontosaldoene revalueres på riktig måte. Når du konsoliderer de opprinnelig dataene, kan du bruke kategorien **Omveksling av valuta** for å velge de opprinnelige valutakursene for omveksling i løpet av konsolideringsprosessen. Når en ny valutakurs angis (for eksempel i neste måned), må du revaluere kontosaldoene. Urealisert fortjeneste og tap oppdateres deretter tilsvarende, basert på den nye valutakursen og datoen. Eksemplet nedenfor illustrerer regnskapsoppføringer som opprettes under prosessen.

## <a name="company-setup"></a>Firmaoppsett
-   **Kilde/driftsselskap (USMF)** – Amerikanske dollar (USD) brukes som regnskaps- og rapporteringsvaluta.
-   **Konsolidert firma (CON)** – Euro (EUR) brukes som regnskaps- og rapporteringsvaluta.
    -   **Realisert fortjeneste** – Finanskonto 801500
    -   **Realisert tap** – Finanskonto 801600
    -   **Urealisert fortjeneste** – Finanskonto 801600
    -   **Urealisert tap** – Finanskonto 801400

## <a name="original-transactions"></a>Opprinnelige transaksjoner
### <a name="cash-receipt-transactions-in-usmf"></a>Kontantmottakstransaksjoner i USMF

| Dato       | Finanskonto               | Valuta. | Beløp |
|------------|------------------------------|----------|--------|
| 11/10/2020 | 110110 – Kontant                | USD      | 500    |
| 11/10/2020 | 130100 – Kunder | USD      | -500   |

## <a name="exchange-rates"></a>Valutakurser

| Fra valuta | Til valuta | Startdato | Valutakurs |
|---------------|-------------|------------|---------------|
| EUR           | USD         | 1/10/2020  | 200           |
| EUR           | USD         | 1/11/2020  | 150           |
| EUR           | USD         | 1/12/2017  | 100           |

## <a name="perform-the-consolidation-for-october-2020"></a>Utfør konsolideringen for oktober 2020
### <a name="balances-in-the-consolidation-company"></a>Saldoer i konsolideringsfirmaet

| Finanskonto | Valuta. | Beløp | Beregning    |
|----------------|----------|--------|----------------|
| 110110         | EUR      | 250    | 500 USD × 50 %  |
| 130100         | EUR      | -250   | -500 USD × 50 % |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2020-through-november-30-2020"></a>Utfør valutarevaluering for kontoene fra 1. oktober 2020 til 30. november 2020
### <a name="balances-in-the-consolidation-company"></a>Saldoer i konsolideringsfirmaet

| Finanskonto | Valuta. | Beløp  | Beregning                        |
|----------------|----------|---------|------------------------------------|
| 110110         | EUR      | 333.33  | Opprinnelig beløp 500 × 66,6667 %  |
| 130100         | EUR      | -333,33 | Opprinnelig beløp -500 × 66,6667 % |
| 801400         | EUR      | 83.33   | 333,33 – 250                       |
| 801600         | EUR      | -83,33  | -333,33 – (-250)                   |

Du vil se tilleggstransaksjoner for rapporteringsvalutabeløpene.

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2020-through-december-31-2020"></a>Utfør valutarevaluering for kontoene fra 1. oktober 2020 til 31. desember 2020
### <a name="balances-in-the-consolidation-company"></a>Saldoer i konsolideringsfirmaet

| Finanskonto | Valuta. | Beløp  | Beregning                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         | EUR      | 500,00  | Opprinnelig beløp 500 × 1                           |
| 130100         | EUR      | -500,00 | Opprinnelig beløp -500 × 1                          |
| 801400         | EUR      | 250     | 500 – 333,33 = 166,67 166,67 + 83,33 = 250           |
| 801600         | EUR      | -250    | -500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
