---
title: Hjemmeside for Økonomimodul og Finansrapportering
description: Bruk økonomimodulen til å definere og styre finansposter for den juridiske enheten.
author: ShylaThompson
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b6683107f4b2dbe36af78749612ce950ea19582
ms.sourcegitcommit: afab5269613d1d1dfd79cd39370b747dee13d3fc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/19/2019
ms.locfileid: "403243"
---
# <a name="general-ledger"></a><span data-ttu-id="edf58-103">Økonomimodul</span><span class="sxs-lookup"><span data-stu-id="edf58-103">General ledger</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="edf58-104">Bruk økonomimodulen til å definere og styre finansposter for den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="edf58-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="edf58-105">Økonomimodulen er et register over debet- og kreditoppføringer.</span><span class="sxs-lookup"><span data-stu-id="edf58-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="edf58-106">Disse oppføringene klassifiseres ved hjelp av kontoene som vises i en kontoplan.</span><span class="sxs-lookup"><span data-stu-id="edf58-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="edf58-107">Planlegge kontoplanen</span><span class="sxs-lookup"><span data-stu-id="edf58-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="edf58-108">Hovedkontotyper</span><span class="sxs-lookup"><span data-stu-id="edf58-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="edf58-109">Du kan fordele, eller distribuere, pengebeløp til én eller flere kontoer eller kombinasjoner og konto og dimensjon basert på fordelingsregler.</span><span class="sxs-lookup"><span data-stu-id="edf58-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="edf58-110">Det finnes to typer tildelinger: fast og variabel.</span><span class="sxs-lookup"><span data-stu-id="edf58-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="edf58-111">Du kan også utligne transaksjoner mellom finanskontoer og revaluere valutabeløp.</span><span class="sxs-lookup"><span data-stu-id="edf58-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="edf58-112">På slutten av regnskapsåret må du generere avslutningstransaksjoner og klargjøre kontoene for neste regnskapsår.</span><span class="sxs-lookup"><span data-stu-id="edf58-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="edf58-113">Du kan bruke konsolideringsfunksjonaliteten til å kombinere de finansielle resultatene for flere juridiske enheter for datterselskap til resultater for én konsolidert organisasjon.</span><span class="sxs-lookup"><span data-stu-id="edf58-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="edf58-114">Datterselskapene kan finnes i den samme Microsoft Dynamics 365 for Finance and Operations-databasen eller i separate databaser.</span><span class="sxs-lookup"><span data-stu-id="edf58-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

- [<span data-ttu-id="edf58-115">Konsoliderings- og elimineringsoversikt</span><span class="sxs-lookup"><span data-stu-id="edf58-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="edf58-116">Kontosaldoer i økonomimodulen</span><span class="sxs-lookup"><span data-stu-id="edf58-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="edf58-117">Finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="edf58-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="edf58-118">[![Forretningsprosess](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="edf58-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="edf58-119">Merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="edf58-119">Sales tax</span></span>
<span data-ttu-id="edf58-120">Hvert firma samler og betaler avgifter til forskjellige skattemyndigheter.</span><span class="sxs-lookup"><span data-stu-id="edf58-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="edf58-121">Reglene og satsene varierer etter land/område, delstat, region og by.</span><span class="sxs-lookup"><span data-stu-id="edf58-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="edf58-122">Reglene må i tillegg oppdateres med jevne mellomrom når skattemyndighetene endrer kravene.</span><span class="sxs-lookup"><span data-stu-id="edf58-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="edf58-123">Mva-koder inneholder grunnleggende informasjon om hvordan du samler og betaler avgifter til myndighetene.</span><span class="sxs-lookup"><span data-stu-id="edf58-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="edf58-124">Når du definerer mva-koder, kan du definere beløpene eller prosentandelene som må samles inn.</span><span class="sxs-lookup"><span data-stu-id="edf58-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="edf58-125">Du definerer også de ulike metodene som brukes til å bruke disse beløpene eller prosentandelene på transaksjonsbeløpene.</span><span class="sxs-lookup"><span data-stu-id="edf58-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="edf58-126">Emnene i denne delen gir informasjon om hvordan du definerer mva-koder for metodene og satsene som kreves av skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="edf58-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="edf58-127">Oversikt over merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="edf58-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="edf58-128">Mva-satser basert på feltene grensegrunnlag og beregningsmetoder</span><span class="sxs-lookup"><span data-stu-id="edf58-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="edf58-129">Mva-betalinger og avrundingsregler</span><span class="sxs-lookup"><span data-stu-id="edf58-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="edf58-130">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="edf58-130">Additional resources</span></span>

#### <a name="whats-new-and-in-development"></a><span data-ttu-id="edf58-131">Hva er nytt og hva er under utvikling?</span><span class="sxs-lookup"><span data-stu-id="edf58-131">What's new and in development</span></span>

<span data-ttu-id="edf58-132">Gå til [Produktmerknader for Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2010158) for å se hvilke nye funksjoner som er planlagt.</span><span class="sxs-lookup"><span data-stu-id="edf58-132">Go to the [Microsoft Dynamics 365 Release Notes](https://go.microsoft.com/fwlink/?linkid=2010158) to see what new features have been planned.</span></span> 

#### <a name="blogs"></a><span data-ttu-id="edf58-133">Blogger</span><span class="sxs-lookup"><span data-stu-id="edf58-133">Blogs</span></span>

<span data-ttu-id="edf58-134">Du kan finne meninger, nyheter og annen informasjon i [Microsoft Dynamics 365-bloggen](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) og [Microsoft Dynamics 365 Finance and Operations – Financials-bloggen](https://community.dynamics.com/365/financeandoperations/b/financials).</span><span class="sxs-lookup"><span data-stu-id="edf58-134">You can find opinions, news, and other information on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) and the [Microsoft Dynamics 365 Finance and Operations - Financials blog](https://community.dynamics.com/365/financeandoperations/b/financials).</span></span>

<span data-ttu-id="edf58-135">[Microsoft Dynamics Operations Partner Community-bloggen](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gir Microsoft Dynamics-partnere én ressurs der de kan finne ut mer om hva som er nytt og populært i MBS Operations.</span><span class="sxs-lookup"><span data-stu-id="edf58-135">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

### <a name="videos"></a><span data-ttu-id="edf58-136">Videoer</span><span class="sxs-lookup"><span data-stu-id="edf58-136">Videos</span></span>

<span data-ttu-id="edf58-137">Se instruksjonsvideoene som nå er tilgjengelige på [Microsoft Dynamics 365 YouTube-kanalen](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span><span class="sxs-lookup"><span data-stu-id="edf58-137">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="edf58-138">Fellesskapsblogger</span><span class="sxs-lookup"><span data-stu-id="edf58-138">Community blogs</span></span>

- [<span data-ttu-id="edf58-139">Hva du bør vite om finans i Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="edf58-139">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)

