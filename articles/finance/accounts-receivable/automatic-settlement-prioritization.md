---
title: Automatisk utligning og prioritering
description: Dette emnet beskriver hvordan transaksjonene utlignes hvis du velger automatisk utligning på parametersiden Kunder. Det forklarer også hvordan automatisk utligning kan brukes sammen med betalingsprioritet.
author: ShivamPandey-msft
ms.date: 01/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: kfend
ms.custom: 14531
ms.assetid: e7837cf6-ec69-44b4-8d47-eba38d5c7b1f
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47ccdb49b4d5c43b4f9cb9a967bd30376474e4c1
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712265"
---
# <a name="automatic-settlement-and-prioritization"></a>Automatisk utligning og prioritering

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan transaksjonene utlignes hvis du velger automatisk utligning på parametersiden Kunder. Det forklarer også hvordan automatisk utligning kan brukes sammen med betalingsprioritet.

Du har to alternativer når du utligner betalinger med fakturaer og andre transaksjoner. Du kan manuelt velge hvilke transaksjoner som skal utlignes, eller systemet kan velge transaksjonene automatisk ved hjelp av funksjonen for automatisk utligning. Du kan også tilpasse hvordan automatiske utligninger behandles ved hjelp av alternativet **Prioriter utligning**. Alle disse alternativene er en del av parameterne for utligning som er definert på **Kundeparametere**-siden. Måten transaksjoner utlignes på automatisk, kan variere, avhengig av hvilken metode du bruker for automatisk utligning. De følgende metodene er tilgjengelige:

-   Brukerdefinert utligningsprioritet
-   Standard automatisk utligning

Delene nedenfor beskriver hvordan transaksjonene utlignes for hver metode.

## <a name="example-transactions"></a>Eksempeltransaksjoner
Eksemplene på utligninger senere i denne artikkelen, er basert på følgende transaksjoner. Alle transaksjonene er for kunde 2050.

| Transaksjon   | Dato        | Beløp | Betingelser for kontantrabatt | Kontantrabattdato | Kommentarer                                                                                                                                                                                      |
|---------------|-------------|--------|---------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Faktura 1     | 15. august   | 100,00 | 2%14, netto 30        | 29. august          |                                                                                                                                                                                               |
| Faktura 2     | 1. september | 250,00 | 2%14, netto 30        | 15. september       |                                                                                                                                                                                               |
| Faktura 3     | 15. oktober  | 500,00 | 2 % 14/netto 30        | 29. oktober         |                                                                                                                                                                                               |
| Rentenota | 15. oktober  | 7,00   |                     |                    | Denne rentenotaen er for faktura 1 og faktura 2. Beløpet beregnes som 2 prosent rente på beløp som er 30 eller flere dager over fristen. Eksempel: 0,02 × (100,00 + 250,00) = 7,00. |

## <a name="user-defined-settlement-priority"></a>Brukerdefinert utligningsprioritet
Hvis du setter **Bruk prioritet for automatiske utligninger** til **Ja** på **Kundeparametere**-siden, brukes utligningsprioriteten som du definerer på **Utligningsprioritet**-siden når transaksjoner er valgt for automatisk utligning. Følgende utligningsprioritet er definert i dette eksemplet:

1.  transaksjonstype
    -   Betalingsgebyrer
    -   Purringer
    -   Rentenotaer
    -   Fakturaer

2.  Transaksjonsdato, stigende
3.  Bilag

Hvis du posterer en betaling på 700,00 25. oktober, utlignes betalingen til transaksjonene i følgende rekkefølge.

| Bilag       | Dato       | Faktura | Beløp i transaksjonsvaluta | Beløp som skal utlignes | Saldo | Valuta |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Rentenota | 15/10/2015 |         | 7,00                           | 7,00             | 0,00    | USD      |
| Faktura 1     | 15/8/2015  | 10001   | 100,00                         | 100,00           | 0,00    | USD      |
| Faktura 2     | 1/9/2015   | 10002   | 250,00                         | 250,00           | 0,00    | USD      |
| Faktura 3     | 15/10/2015 |         | 500,00                         | 343.00           | 157.00  | USD      |

## <a name="default-automatic-settlement"></a>Standard automatisk utligning
Hvis det ikke finnes noen brukerdefinert utligningsprioritet, velges transaksjoner for utligning automatisk basert på forfallsdatoen. Transaksjoner som er utlignet, må ha samme valuta som transaksjonen som de er utlignet mot. Hvis du posterer en betaling på 700,00 25. oktober, blir følgende transaksjoner valgt for utligning.

| Bilag       | Dato       | Faktura | Beløp i transaksjonsvaluta | Beløp som skal utlignes | Saldo | Valuta |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Faktura 1     | 15/8/2015  | 10001   | 100,00                         | 100,00           | 0,00    | USD      |
| Faktura 2     | 1/9/2015   | 10002   | 250,00                         | 250,00           | 0,00    | USD      |
| Faktura 3     | 15/10/2015 |         | 500.00                         | 350.00           | 150.00  | USD      |
| Rentenota | 15/10/2015 |         | 7.00                           | 0.00             | 7.00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
