---
title: Rapport for mva-spesifikasjon etter finanstransaksjon
description: Dette emnet forklarer hvordan du bruker rapporten Mva-spesifikasjon etter finanstransaksjon til å vise og skrive ut informasjon om finanstransaksjoner som merverdiavgift beregnes for.
author: ericwang
manager: Ann Beebe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 1c36d9f8fb81a0a7e7a6de3db48cebdcf9d13b2d
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/14/2019
ms.locfileid: "2591200"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a><span data-ttu-id="d0ebe-103">Rapport for mva-spesifikasjon etter finanstransaksjon</span><span class="sxs-lookup"><span data-stu-id="d0ebe-103">Sales tax specification by ledger transaction report</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0ebe-104">Dette emnet forklarer hvordan du bruker rapporten **Mva-spesifikasjon etter finanstransaksjon** til å vise og skrive ut informasjon om finanstransaksjoner som merverdiavgift beregnes for.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-104">This topic explains how to use the **Sales tax specification by ledger transaction** report to view and print information about ledger transactions that sales tax is calculated for.</span></span>

## <a name="tax-accounts-vs-non-tax-accounts"></a><span data-ttu-id="d0ebe-105">Avgiftskontoer i forhold til ikke-avgiftskontoer</span><span class="sxs-lookup"><span data-stu-id="d0ebe-105">Tax accounts vs. non-tax accounts</span></span>

<span data-ttu-id="d0ebe-106">Rapporten **Mva-spesifikasjon etter finanstransaksjon** viser avgiftstransaksjoner for både avgiftskontoer og ikke-avgiftskontoer.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-106">The **Sales tax specification by ledger transaction** report shows tax transactions for both tax accounts and non-tax accounts.</span></span> <span data-ttu-id="d0ebe-107">Disse kontoene er kategorisert på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="d0ebe-107">These accounts are categorized in the following way:</span></span>

- <span data-ttu-id="d0ebe-108">**Avgiftskonto** – En konto anses å være avgiftskonto når en avgiftstransaksjon posteres, og hovedkontoen på **Merverdiavgift**-journallinjen er en avgiftskonto, for eksempel en utgående mva-konto eller en konto for innkommende merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-108">**Tax account** – An account is considered a tax account when a tax transaction is posted, and the main account on the **Sales Tax** journal line is a tax account, such as a sales tax payable account or a sales tax receivable account.</span></span>
- <span data-ttu-id="d0ebe-109">**Ikke-avgiftskonto** – En konto anses å være ikke-avgiftskonto når en avgiftstransaksjon posteres, og hovedkontoen på den opprinnelige transaksjonen er en ikke-avgiftskonto, for eksempel en inntektskonto eller en utgiftskonto.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-109">**Non-tax account** – An account is considered a non-tax account when a tax transaction is posted, and the main account on the original transaction is a non-tax account, such as a revenue account or an expense account.</span></span>

<span data-ttu-id="d0ebe-110">For avgiftskontoer viser kolonnene **0** (null) for kolonnene **Grunnlag**, **Innkommende merverdiavgift** og **Utgående merverdiavgift** .</span><span class="sxs-lookup"><span data-stu-id="d0ebe-110">For tax accounts, the **Origin**, **Sales tax receivable**, and **Sales tax payable** columns on the report show **0** (zero).</span></span> <span data-ttu-id="d0ebe-111">For ikke-avgiftskontoer viser disse kolonnene beløp.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-111">For non-tax accounts, those columns show amounts.</span></span>

## <a name="filtering-the-data-on-the-report"></a><span data-ttu-id="d0ebe-112">Filtrere dataene i rapporten</span><span class="sxs-lookup"><span data-stu-id="d0ebe-112">Filtering the data on the report</span></span>

<span data-ttu-id="d0ebe-113">Når du genererer rapporten, er følgende felt tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-113">When you generate the report, the following default fields are available.</span></span> <span data-ttu-id="d0ebe-114">Du kan bruke disse feltene til å filtrere dataene som vises i rapporten.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-114">You can use these fields to filter the data that is shown on the report.</span></span>

| <span data-ttu-id="d0ebe-115">Felt</span><span class="sxs-lookup"><span data-stu-id="d0ebe-115">Field</span></span>                      | <span data-ttu-id="d0ebe-116">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d0ebe-116">Description</span></span> |
|----------------------------|-------------|
| <span data-ttu-id="d0ebe-117">Dato</span><span class="sxs-lookup"><span data-stu-id="d0ebe-117">Date</span></span>                       | <span data-ttu-id="d0ebe-118">Bruk feltene i delene **Fra** og **Til** for å definere et datoområde for avgiftstransaksjonene.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-118">Use the fields in the **From** and **To** sections to define a date range for the tax transactions.</span></span> |
| <span data-ttu-id="d0ebe-119">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="d0ebe-119">Main account</span></span>               | <span data-ttu-id="d0ebe-120">Bruk feltene i delene **Fra** og **Til** for å definere et datoområde for hovedkontoer.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-120">Use the fields in the **From** and **To** sections to define a range of main accounts.</span></span> |
| <span data-ttu-id="d0ebe-121">Mva-kode</span><span class="sxs-lookup"><span data-stu-id="d0ebe-121">Sales tax code</span></span>             | <span data-ttu-id="d0ebe-122">Bruk feltene i delene **Fra** og **Til** for å definere et datoområde for mva-koder.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-122">Use the fields in the **From** and **To** sections to define a range of sales tax codes.</span></span> |
| <span data-ttu-id="d0ebe-123">Gruppering</span><span class="sxs-lookup"><span data-stu-id="d0ebe-123">Grouping</span></span>                   | <span data-ttu-id="d0ebe-124">Velg om rapporten skal grupperes etter finanskonto eller mva-kode.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-124">Select whether the report should be grouped by ledger account or sales tax code.</span></span> |
| <span data-ttu-id="d0ebe-125">Delsum etter mva-kode</span><span class="sxs-lookup"><span data-stu-id="d0ebe-125">Subtotal by sales tax code</span></span> | <span data-ttu-id="d0ebe-126">Sett dette alternativet til **Ja** for å vise delsummer etter mva-kode.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-126">Set this option to **Yes** to show subtotals by sales tax code.</span></span> |
| <span data-ttu-id="d0ebe-127">Bare summer</span><span class="sxs-lookup"><span data-stu-id="d0ebe-127">Totals only</span></span>                | <span data-ttu-id="d0ebe-128">Sett dette alternativet til **Ja** for å vise bare totaler.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-128">Set this option to **Yes** to show only totals.</span></span> |
| <span data-ttu-id="d0ebe-129">Bare hovedkontoer</span><span class="sxs-lookup"><span data-stu-id="d0ebe-129">Main accounts only</span></span>         | <span data-ttu-id="d0ebe-130">Sett dette alternativet til **Ja** for å ta med bare hovedkontoer i rapporten.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-130">Set this option to **Yes** to include only main accounts on the report.</span></span> |

## <a name="showing-only-non-tax-accounts-on-the-report"></a><span data-ttu-id="d0ebe-131">Vise bare ikke-avgiftskontoer i rapporten</span><span class="sxs-lookup"><span data-stu-id="d0ebe-131">Showing only non-tax accounts on the report</span></span>

<span data-ttu-id="d0ebe-132">Hvis du vil vise bare ikke-avgiftskontoer i rapporten, definerer du en filter betingelse, for eksempel en stjerne (\*), som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-132">To show only non-tax accounts on the report, set up a filter condition, such as an asterisk (\*), as shown in the following illustration.</span></span>

![Rapport som viser ikke-avgiftskontoer](media/taxspecperledgertrans.png)
