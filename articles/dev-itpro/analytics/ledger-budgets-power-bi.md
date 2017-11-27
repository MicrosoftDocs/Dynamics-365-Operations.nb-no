---
title: Faktisk vs. budsjett Power BI-innhold
description: "Dette emnet beskriver Faktisk vs. budsjett-innholdet for Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdet, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: ryansandness
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f09af96fb1c76d8737d2c535f1a46565a18deca0
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="57874-104">Faktisk vs. budsjett Power BI-innhold</span><span class="sxs-lookup"><span data-stu-id="57874-104">Actual vs budget Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="57874-105">Dette emnet beskriver **Faktisk vs. budsjett**-innholdet for Power BI.</span><span class="sxs-lookup"><span data-stu-id="57874-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="57874-106">Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.</span><span class="sxs-lookup"><span data-stu-id="57874-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

# <a name="overview"></a><span data-ttu-id="57874-107">Oversikt</span><span class="sxs-lookup"><span data-stu-id="57874-107">Overview</span></span>

<span data-ttu-id="57874-108">Den **Faktisk vs. budsjett** Power BI-innholdet ble opprettet for personer som har ansvar for overvåking av faktiske resultater mot budsjetterte resultater i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="57874-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="57874-109">**Faktisk vs. budsjett** Power BI-innhold gir oversikt over avvik i budsjettet.</span><span class="sxs-lookup"><span data-stu-id="57874-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="57874-110">Du kan analysere budsjettet for gjeldende år etter kontokategori, budsjettkode, hovedkontoe, beskrivelser av hovedkontoe eller regnskapsperiode for å få en bedre forståelse av eventuelle avvik.</span><span class="sxs-lookup"><span data-stu-id="57874-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

# <a name="accessing-the-power-bi-content"></a><span data-ttu-id="57874-111">Tilgang til Power BI-innhold</span><span class="sxs-lookup"><span data-stu-id="57874-111">Accessing the Power BI content</span></span>
<span data-ttu-id="57874-112">Hvis du bruker Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017), vil rapporter fra **Faktisk vs. budsjett** Power Bi-innholdet vises i arbeidsområdene **Hovedbok for budsjett og prognoser** og **Finanssjef**.</span><span class="sxs-lookup"><span data-stu-id="57874-112">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

# <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="57874-113">Rapporter som er inkludert i Power BI-innholdet</span><span class="sxs-lookup"><span data-stu-id="57874-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="57874-114">Tabellen nedenfor viser detaljer om mål som finnes på hver rapportside i **Faktisk vs. budsjett** Power BI-innholdet.</span><span class="sxs-lookup"><span data-stu-id="57874-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="57874-115">Rapporter</span><span class="sxs-lookup"><span data-stu-id="57874-115">Report</span></span>                      | <span data-ttu-id="57874-116">Mål</span><span class="sxs-lookup"><span data-stu-id="57874-116">Metrics</span></span> |
|-----------------------------|---------|
| <span data-ttu-id="57874-117">Utgifter – faktiske i forhold til budsjett</span><span class="sxs-lookup"><span data-stu-id="57874-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="57874-118">Totale utgifter i inneværende år</span><span class="sxs-lookup"><span data-stu-id="57874-118">Total expenses this year</span></span></li><li><span data-ttu-id="57874-119">Budsjetterte totale utgifter i inneværende år</span><span class="sxs-lookup"><span data-stu-id="57874-119">Budget total expenses this year</span></span></li></ul> |
| <span data-ttu-id="57874-120">Inntekt – faktisk i forhold til budsjett</span><span class="sxs-lookup"><span data-stu-id="57874-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="57874-121">Totalomsetning i inneværende år</span><span class="sxs-lookup"><span data-stu-id="57874-121">Total revenue this year</span></span></li><li><span data-ttu-id="57874-122">Budsjettert totalomsetning i inneværende år</span><span class="sxs-lookup"><span data-stu-id="57874-122">Budget total revenue this year</span></span></li><ul> |
| <span data-ttu-id="57874-123">Utgift</span><span class="sxs-lookup"><span data-stu-id="57874-123">Expense</span></span>                     | <ul><li><span data-ttu-id="57874-124">Totale utgifter i inneværende år</span><span class="sxs-lookup"><span data-stu-id="57874-124">Total expenses this year</span></span></li><li><span data-ttu-id="57874-125">Mål for utgifter basert på budsjett</span><span class="sxs-lookup"><span data-stu-id="57874-125">Goal for expenses based on budget</span></span> </li><ul> |
| <span data-ttu-id="57874-126">Omsetning</span><span class="sxs-lookup"><span data-stu-id="57874-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="57874-127">Totalomsetning i inneværende år</span><span class="sxs-lookup"><span data-stu-id="57874-127">Total revenue this year</span></span></li><li><span data-ttu-id="57874-128">Mål for inntekter basert på budsjett</span><span class="sxs-lookup"><span data-stu-id="57874-128">Goal for revenue based on budget</span></span> </li><ul> |
| <span data-ttu-id="57874-129">Nettoinntekt</span><span class="sxs-lookup"><span data-stu-id="57874-129">Net income</span></span>                  | <ul><li><span data-ttu-id="57874-130">Nettoinntekt i inneværende år</span><span class="sxs-lookup"><span data-stu-id="57874-130">Net income this year</span></span></li><li><span data-ttu-id="57874-131">Mål for nettoinntekt basert på budsjett</span><span class="sxs-lookup"><span data-stu-id="57874-131">Goal for net income based on budget</span></span> </li><ul> |

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="57874-132">Utvide Power BI-innholdet</span><span class="sxs-lookup"><span data-stu-id="57874-132">Extending the Power BI content</span></span>
<span data-ttu-id="57874-133">Hvis du bruker innholdspakkene som er tilgjengelige i Microsoft Dynamics Lifecycle Services (LCS), kan du gi personer som ikke logger på Microsoft Dynamics 365, gode analyser.</span><span class="sxs-lookup"><span data-stu-id="57874-133">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="57874-134">Du kan endre disse innholdspakkene slik at de inneholder andre rapporter eller visuelle hjelpemidler, og deretter publisere innholdspakkene på Power BI.com-leieren for analyse.</span><span class="sxs-lookup"><span data-stu-id="57874-134">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="57874-135">Du kan finne **Faktisk vs. budsjett**-innholdet for Power BI i det delte aktivabiblioteket i LCS.</span><span class="sxs-lookup"><span data-stu-id="57874-135">You can find the **Actual vs budget** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="57874-136">Hvis du vil ha mer informasjon om hvordan du laster ned innholdet og implementerer det i organisasjonen, kan du se [Power BI-innhold i LCS fra Microsoft og partnerne](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="57874-136">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="57874-137">Hvis du vil se en demo som viser hvordan du implementerer Power BI-innholdet, kan du se [Power BI-innhold fra Microsoft og partnerne i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).</span><span class="sxs-lookup"><span data-stu-id="57874-137">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

# <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="57874-138">Forstå datamodellen og enheter</span><span class="sxs-lookup"><span data-stu-id="57874-138">Understanding the data model and entities</span></span>

| <span data-ttu-id="57874-139">Enhet</span><span class="sxs-lookup"><span data-stu-id="57874-139">Entity</span></span>                    | <span data-ttu-id="57874-140">Innhold</span><span class="sxs-lookup"><span data-stu-id="57874-140">Contents</span></span> |
|---------------------------|----------|
| <span data-ttu-id="57874-141">Aktiviteter i øknomimodulen</span><span class="sxs-lookup"><span data-stu-id="57874-141">General Ledger Activities</span></span> | <span data-ttu-id="57874-142">Transaksjonsbeløp for økonomimodulen</span><span class="sxs-lookup"><span data-stu-id="57874-142">Transaction amounts for the general ledger</span></span> |
| <span data-ttu-id="57874-143">Budsjettaktiviteter</span><span class="sxs-lookup"><span data-stu-id="57874-143">Budget Activities</span></span>         | <span data-ttu-id="57874-144">Transaksjonsbeløp for budsjettregisteret</span><span class="sxs-lookup"><span data-stu-id="57874-144">Transaction amounts for the budget register</span></span> |
| <span data-ttu-id="57874-145">Hovedkontoer</span><span class="sxs-lookup"><span data-stu-id="57874-145">Main Accounts</span></span>             | <span data-ttu-id="57874-146">Hovedkontoer rapporter kan filtreres etter</span><span class="sxs-lookup"><span data-stu-id="57874-146">Main accounts to filter reports by</span></span> |
| <span data-ttu-id="57874-147">Regnskapskalendere</span><span class="sxs-lookup"><span data-stu-id="57874-147">Fiscal Calendars</span></span>          | <span data-ttu-id="57874-148">Regnskapskalendere rapporter kan filtreres etter</span><span class="sxs-lookup"><span data-stu-id="57874-148">Fiscal calendars to filter reports by</span></span> |
| <span data-ttu-id="57874-149">Finanskontoer</span><span class="sxs-lookup"><span data-stu-id="57874-149">Ledgers</span></span>                   | <span data-ttu-id="57874-150">Finanskontoer som kan brukes til å filtrere rapporten til den gjeldende finanskontoen</span><span class="sxs-lookup"><span data-stu-id="57874-150">Ledgers that can be used to filter the report to the current ledger</span></span> |
| <span data-ttu-id="57874-151">Budsjettkoder</span><span class="sxs-lookup"><span data-stu-id="57874-151">Budget Codes</span></span>              | <span data-ttu-id="57874-152">Budsjettkoder rapporter kan filtreres etter</span><span class="sxs-lookup"><span data-stu-id="57874-152">Budget codes to filter reports by</span></span> |
| <span data-ttu-id="57874-153">Juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="57874-153">Legal Entities</span></span>            | <span data-ttu-id="57874-154">Juridiske enheter som kan brukes til å filtrere rapporten til den gjeldende juridiske enheten</span><span class="sxs-lookup"><span data-stu-id="57874-154">Legal entities that can be used to filter the report to the current legal entity</span></span> |

