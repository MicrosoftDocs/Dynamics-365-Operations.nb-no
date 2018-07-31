---
title: "Hjemmeside for Økonomimodul og Finansrapportering"
description: "Bruk økonomimodulen til å definere og styre finansposter for den juridiske enheten."
author: twheeloc
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 03bab1d03be71c0e23a6ea93f542d6a52a212a1f
ms.openlocfilehash: 9ee3f73cd11b38ed2237ea3fe08db18000e55f07
ms.contentlocale: nb-no
ms.lasthandoff: 06/25/2018

---

# <a name="general-ledger"></a><span data-ttu-id="7f4ee-103">Økonomimodul</span><span class="sxs-lookup"><span data-stu-id="7f4ee-103">General ledger</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f4ee-104">Bruk økonomimodulen til å definere og styre finansposter for den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="7f4ee-105">Økonomimodulen er et register over debet- og kreditoppføringer.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="7f4ee-106">Disse oppføringene klassifiseres ved hjelp av kontoene som vises i en kontoplan.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="7f4ee-107">Planlegge kontoplanen</span><span class="sxs-lookup"><span data-stu-id="7f4ee-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="7f4ee-108">Hovedkontotyper</span><span class="sxs-lookup"><span data-stu-id="7f4ee-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="7f4ee-109">Du kan fordele, eller distribuere, pengebeløp til én eller flere kontoer eller kombinasjoner og konto og dimensjon basert på fordelingsregler.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="7f4ee-110">Det finnes to typer tildelinger: fast og variabel.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="7f4ee-111">Du kan også utligne transaksjoner mellom finanskontoer og revaluere valutabeløp.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="7f4ee-112">På slutten av regnskapsåret må du generere avslutningstransaksjoner og klargjøre kontoene for neste regnskapsår.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="7f4ee-113">Du kan bruke konsolideringsfunksjonaliteten til å kombinere de finansielle resultatene for flere juridiske enheter for datterselskap til resultater for én konsolidert organisasjon.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="7f4ee-114">Datterselskapene kan finnes i den samme Microsoft Dynamics 365 for Finance and Operations-databasen eller i separate databaser.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

- [<span data-ttu-id="7f4ee-115">Konsoliderings- og elimineringsoversikt</span><span class="sxs-lookup"><span data-stu-id="7f4ee-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="7f4ee-116">Kontosaldoer i økonomimodulen</span><span class="sxs-lookup"><span data-stu-id="7f4ee-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="7f4ee-117">Finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="7f4ee-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="7f4ee-118">[![Forretningsprosess](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="7f4ee-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="7f4ee-119">Merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="7f4ee-119">Sales tax</span></span>
<span data-ttu-id="7f4ee-120">Hvert firma samler og betaler avgifter til forskjellige skattemyndigheter.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="7f4ee-121">Reglene og satsene varierer etter land/område, delstat, region og by.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="7f4ee-122">Reglene må i tillegg oppdateres med jevne mellomrom når skattemyndighetene endrer kravene.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="7f4ee-123">Mva-koder inneholder grunnleggende informasjon om hvordan du samler og betaler avgifter til myndighetene.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="7f4ee-124">Når du definerer mva-koder, kan du definere beløpene eller prosentandelene som må samles inn.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="7f4ee-125">Du definerer også de ulike metodene som brukes til å bruke disse beløpene eller prosentandelene på transaksjonsbeløpene.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="7f4ee-126">Emnene i denne delen gir informasjon om hvordan du definerer mva-koder for metodene og satsene som kreves av skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="7f4ee-127">Oversikt over merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="7f4ee-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="7f4ee-128">Mva-satser basert på feltene grensegrunnlag og beregningsmetoder</span><span class="sxs-lookup"><span data-stu-id="7f4ee-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="7f4ee-129">Mva-betalinger og avrundingsregler</span><span class="sxs-lookup"><span data-stu-id="7f4ee-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="7f4ee-130">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="7f4ee-130">Additional resources</span></span>

### <a name="whats-new"></a><span data-ttu-id="7f4ee-131">Nyheter</span><span class="sxs-lookup"><span data-stu-id="7f4ee-131">What's new</span></span>

<span data-ttu-id="7f4ee-132">Gå til den [Produktmerknader](https://docs.microsoft.com/en-us/business-applications-release-notes/) for å se hvilke nye funksjoner som er lansert.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-132">Go to the [Release notes](https://docs.microsoft.com/en-us/business-applications-release-notes/) to see what new features have been released.</span></span> 

### <a name="videos"></a><span data-ttu-id="7f4ee-133">Videoer</span><span class="sxs-lookup"><span data-stu-id="7f4ee-133">Videos</span></span>

<span data-ttu-id="7f4ee-134">Se instruksjonsvideoene som nå er tilgjengelige på [Microsoft Dynamics 365 YouTube-kanalen](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span><span class="sxs-lookup"><span data-stu-id="7f4ee-134">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

### <a name="blogs"></a><span data-ttu-id="7f4ee-135">Blogger</span><span class="sxs-lookup"><span data-stu-id="7f4ee-135">Blogs</span></span>

<span data-ttu-id="7f4ee-136">Du kan finne meninger, nyheter og annen informasjon om Leverandører og andre løsninger i [Microsoft Dynamics 365-bloggen](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span><span class="sxs-lookup"><span data-stu-id="7f4ee-136">You can find opinions, news, and other information about Accounts payable and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span></span>

<span data-ttu-id="7f4ee-137">Det er mange innlegg om General Ledger på [Microsoft Dynamics AX-teamets produktblogg](https://blogs.msdn.microsoft.com/dax/)</span><span class="sxs-lookup"><span data-stu-id="7f4ee-137">There are many posts about General ledger on the [Microsoft Dynamics AX product team blog](https://blogs.msdn.microsoft.com/dax/).</span></span> <span data-ttu-id="7f4ee-138">Selv om noen av disse innleggene ble skrevet for den forrige versjonen av General Ledger, gjelder de samme konseptene, og prosedyrene er også like i den gjeldende versjonen.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-138">Although some of these posts were written for the previous version of General ledger, the same concepts still apply, and the procedures are also similar in the current version.</span></span>

<span data-ttu-id="7f4ee-139">[Microsoft Dynamics Operations Partner Community-bloggen](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gir Microsoft Dynamics-partnere én ressurs der de kan finne ut mer om hva som er nytt og populært i MBS Operations.</span><span class="sxs-lookup"><span data-stu-id="7f4ee-139">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="7f4ee-140">Fellesskapsblogger</span><span class="sxs-lookup"><span data-stu-id="7f4ee-140">Community blogs</span></span>

- [<span data-ttu-id="7f4ee-141">Hva du bør vite om finans i Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7f4ee-141">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)


