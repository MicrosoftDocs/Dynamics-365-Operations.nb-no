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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 7f5435a97776b817a4b99887cbab8283de25b692
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4014864"
---
# <a name="integrated-ledger"></a><span data-ttu-id="c0d7a-103">Integrert finans</span><span class="sxs-lookup"><span data-stu-id="c0d7a-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="c0d7a-104">I et forretningsprogram definerer finansdata kjerneoppsettet for hvordan et firma gjør forretninger.</span><span class="sxs-lookup"><span data-stu-id="c0d7a-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="c0d7a-105">Finansdata beskriver for eksempel regnskapsåret firmaet følger, transaksjonsvalutaene og kontoene det bruker.</span><span class="sxs-lookup"><span data-stu-id="c0d7a-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="c0d7a-106">Dette emnet beskriver integreringen av disse finansielle dataene.</span><span class="sxs-lookup"><span data-stu-id="c0d7a-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="c0d7a-107">Maler</span><span class="sxs-lookup"><span data-stu-id="c0d7a-107">Templates</span></span>

<span data-ttu-id="c0d7a-108">Finansdata inkluderer en samling enhetstilordninger for viktige finansområder som fungerer sammen under datasamhandling, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="c0d7a-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="c0d7a-109">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="c0d7a-109">Finance and Operations apps</span></span>      | <span data-ttu-id="c0d7a-110">Modelldrevet app i Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c0d7a-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="c0d7a-111">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c0d7a-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="c0d7a-112">Valutaer</span><span class="sxs-lookup"><span data-stu-id="c0d7a-112">Currencies</span></span>                       | <span data-ttu-id="c0d7a-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="c0d7a-113">transactioncurrencies</span></span>            |
<span data-ttu-id="c0d7a-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="c0d7a-114">FiscalCalendar</span></span>                   | <span data-ttu-id="c0d7a-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="c0d7a-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="c0d7a-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="c0d7a-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="c0d7a-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="c0d7a-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="c0d7a-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="c0d7a-118">ExchRateType</span></span>                     | <span data-ttu-id="c0d7a-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="c0d7a-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="c0d7a-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="c0d7a-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="c0d7a-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="c0d7a-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="c0d7a-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="c0d7a-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="c0d7a-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="c0d7a-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="c0d7a-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="c0d7a-124">MainAccountCategory</span></span>              | <span data-ttu-id="c0d7a-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="c0d7a-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="c0d7a-126">MainAccount</span><span class="sxs-lookup"><span data-stu-id="c0d7a-126">MainAccount</span></span>                      | <span data-ttu-id="c0d7a-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="c0d7a-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="c0d7a-128">Finans</span><span class="sxs-lookup"><span data-stu-id="c0d7a-128">Ledger</span></span>                           | <span data-ttu-id="c0d7a-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="c0d7a-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="c0d7a-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="c0d7a-130">ExchangeRates</span></span>                    | <span data-ttu-id="c0d7a-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="c0d7a-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="c0d7a-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="c0d7a-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="c0d7a-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="c0d7a-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="c0d7a-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="c0d7a-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="c0d7a-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="c0d7a-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="c0d7a-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="c0d7a-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="c0d7a-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="c0d7a-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="c0d7a-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="c0d7a-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="c0d7a-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="c0d7a-139">msdyn\_chartofaccounts</span></span>        |


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




