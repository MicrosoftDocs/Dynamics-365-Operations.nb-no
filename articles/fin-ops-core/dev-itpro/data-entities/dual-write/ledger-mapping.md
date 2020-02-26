---
title: Integrert finans
description: Dette emnet beskriver integreringen av finansdata mellom Finance and Operations og andre Dynamics 365-programmer ved bruk av Common Data Service.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6bf1c554f56c1424da9fde98f67f80a6b7c95461
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019939"
---
# <a name="integrated-ledger"></a>Integrert finans

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

I et forretningsprogram definerer finansdata kjerneoppsettet for hvordan et firma gjør forretninger. Finansdata beskriver for eksempel regnskapsåret firmaet følger, transaksjonsvalutaene og kontoene det bruker. Dette emnet beskriver integreringen av disse finansielle dataene.

## <a name="templates"></a>Maler

Finansdata inkluderer en samling enhetstilordninger for viktige finansområder som fungerer sammen under datasamhandling, som vist i følgende tabell.

Finance and Operations-apper      | Andre Dynamics 365-apper
---------------------------------|---------------------------------
Valutaer                       | transactioncurrencies
FiscalCalendar                   | msdyn\_fiscalcalendars
FiscalCalendarYear               | msdyn\_fiscalcalendaryears
ExchRateType                     | msdyn\_exchangeratetypes
ExchangeRateCurrencyPair         | msdyn\_currencyexchangeratepairs
FiscalPeriodEntity               | msdyn\_fiscalcalendarperiods
MainAccountCategory              | msdyn\_mainaccountcategory
MainAccount                      | msdyn\_mainaccounts
Finans                           | msdyn\_ledgers
ExchangeRates                    | msdyn\_currencyexchangerates
FinancialCalendarPeriod          | msdyn\_fiscalcalendarperiods
DimensionAttributeEntity         | msdyn\_dimensionattributes.md
DimensionIntegrationFormatEntity | msdyn\_financialdimensionformats.md
LedgerChartOfAccounts            | msdyn\_chartofaccounts.md


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




