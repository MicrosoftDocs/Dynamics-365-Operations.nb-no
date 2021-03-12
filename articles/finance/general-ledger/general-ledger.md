---
title: Oversikt over Økonomimodul og Finansrapportering
description: Bruk økonomimodulen til å definere og styre finansposter for den juridiske enheten.
author: ShylaThompson
manager: AnnBe
ms.date: 08/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e6e09b5c800da639a8e02738a7fd58e7373cca2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975589"
---
# <a name="general-ledger-home-page"></a><span data-ttu-id="43132-103">Startside for økonomimodulen</span><span class="sxs-lookup"><span data-stu-id="43132-103">General ledger home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43132-104">Bruk økonomimodulen til å definere og styre finansposter for den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="43132-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="43132-105">Økonomimodulen er et register over debet- og kreditoppføringer.</span><span class="sxs-lookup"><span data-stu-id="43132-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="43132-106">Disse oppføringene klassifiseres ved hjelp av kontoene som vises i en kontoplan.</span><span class="sxs-lookup"><span data-stu-id="43132-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="43132-107">Planlegge kontoplanen</span><span class="sxs-lookup"><span data-stu-id="43132-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="43132-108">Hovedkontotyper</span><span class="sxs-lookup"><span data-stu-id="43132-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="43132-109">Du kan fordele, eller distribuere, pengebeløp til én eller flere kontoer eller kombinasjoner og konto og dimensjon basert på fordelingsregler.</span><span class="sxs-lookup"><span data-stu-id="43132-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="43132-110">Det finnes to typer tildelinger: fast og variabel.</span><span class="sxs-lookup"><span data-stu-id="43132-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="43132-111">Du kan også utligne transaksjoner mellom finanskontoer og revaluere valutabeløp.</span><span class="sxs-lookup"><span data-stu-id="43132-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="43132-112">På slutten av regnskapsåret må du generere avslutningstransaksjoner og klargjøre kontoene for neste regnskapsår.</span><span class="sxs-lookup"><span data-stu-id="43132-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="43132-113">Du kan bruke konsolideringsfunksjonaliteten til å kombinere de finansielle resultatene for flere juridiske enheter for datterselskap til resultater for én konsolidert organisasjon.</span><span class="sxs-lookup"><span data-stu-id="43132-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="43132-114">Datterselskapene kan finnes i den samme databasen eller i separate databaser.</span><span class="sxs-lookup"><span data-stu-id="43132-114">The subsidiaries can be in the same database or in separate databases.</span></span>

- [<span data-ttu-id="43132-115">Konsoliderings- og elimineringsoversikt</span><span class="sxs-lookup"><span data-stu-id="43132-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="43132-116">Kontosaldoer i økonomimodulen</span><span class="sxs-lookup"><span data-stu-id="43132-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="43132-117">Finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="43132-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="43132-118">[![Forretningsprosess](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="43132-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="43132-119">Merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="43132-119">Sales tax</span></span>
<span data-ttu-id="43132-120">Hvert firma samler og betaler avgifter til forskjellige skattemyndigheter.</span><span class="sxs-lookup"><span data-stu-id="43132-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="43132-121">Reglene og satsene varierer etter land/område, delstat, region og by.</span><span class="sxs-lookup"><span data-stu-id="43132-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="43132-122">Reglene må i tillegg oppdateres med jevne mellomrom når skattemyndighetene endrer kravene.</span><span class="sxs-lookup"><span data-stu-id="43132-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="43132-123">Mva-koder inneholder grunnleggende informasjon om hvordan du samler og betaler avgifter til myndighetene.</span><span class="sxs-lookup"><span data-stu-id="43132-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="43132-124">Når du definerer mva-koder, kan du definere beløpene eller prosentandelene som må samles inn.</span><span class="sxs-lookup"><span data-stu-id="43132-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="43132-125">Du definerer også de ulike metodene som brukes til å bruke disse beløpene eller prosentandelene på transaksjonsbeløpene.</span><span class="sxs-lookup"><span data-stu-id="43132-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="43132-126">Emnene i denne delen gir informasjon om hvordan du definerer mva-koder for metodene og satsene som kreves av skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="43132-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="43132-127">Oversikt over merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="43132-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="43132-128">Mva-satser basert på feltene grensegrunnlag og beregningsmetoder</span><span class="sxs-lookup"><span data-stu-id="43132-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="43132-129">Mva-betalinger og avrundingsregler</span><span class="sxs-lookup"><span data-stu-id="43132-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="43132-130">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="43132-130">Additional resources</span></span>

#### <a name="whats-new-and-in-development"></a><span data-ttu-id="43132-131">Hva er nytt og hva er under utvikling?</span><span class="sxs-lookup"><span data-stu-id="43132-131">What's new and in development</span></span>

<span data-ttu-id="43132-132">Gå til [Lanseringsplaner for Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2010158) for å se hvilke nye funksjoner som er planlagt.</span><span class="sxs-lookup"><span data-stu-id="43132-132">Go to the [Microsoft Dynamics 365 release plans](https://go.microsoft.com/fwlink/?linkid=2010158) to see what new features have been planned.</span></span> 

#### <a name="financial-reporting"></a><span data-ttu-id="43132-133">Finansrapportering</span><span class="sxs-lookup"><span data-stu-id="43132-133">Financial reporting</span></span>
<span data-ttu-id="43132-134">Gå til emnet [Oversikt over Financial reporting](../../fin-ops-core/dev-itpro/analytics/financial-reporting-intro.md) for informasjon om økonomiske rapporter.</span><span class="sxs-lookup"><span data-stu-id="43132-134">Go to the [Financial reporting overview](../../fin-ops-core/dev-itpro/analytics/financial-reporting-intro.md) topic for information about financial reports.</span></span>

#### <a name="blogs"></a><span data-ttu-id="43132-135">Blogger</span><span class="sxs-lookup"><span data-stu-id="43132-135">Blogs</span></span>

<span data-ttu-id="43132-136">Du kan finne meninger, nyheter og annen informasjon i bloggen for [Microsoft Dynamics 365](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) og bloggen for [Microsoft Dynamics 365 Finance and Operations - Financials](https://community.dynamics.com/365/financeandoperations/b/financials).</span><span class="sxs-lookup"><span data-stu-id="43132-136">You can find opinions, news, and other information on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) and the [Microsoft Dynamics 365 Finance and Operations - Financials blog](https://community.dynamics.com/365/financeandoperations/b/financials).</span></span>

<span data-ttu-id="43132-137">[Microsoft Dynamics Operations Partner Community-bloggen](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gir Microsoft Dynamics-partnere én ressurs der de kan finne ut mer om hva som er nytt og populært i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="43132-137">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in Dynamics 365.</span></span>

### <a name="videos"></a><span data-ttu-id="43132-138">Videoer</span><span class="sxs-lookup"><span data-stu-id="43132-138">Videos</span></span>

<span data-ttu-id="43132-139">Se instruksjonsvideoene som nå er tilgjengelige på [Microsoft Dynamics 365 YouTube-kanalen](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span><span class="sxs-lookup"><span data-stu-id="43132-139">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="43132-140">Fellesskapsblogger</span><span class="sxs-lookup"><span data-stu-id="43132-140">Community blogs</span></span>

- [<span data-ttu-id="43132-141">Hva du bør vite om finans i Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="43132-141">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)

