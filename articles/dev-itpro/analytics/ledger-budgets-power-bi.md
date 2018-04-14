---
title: Faktisk vs. budsjett Power BI-innhold
description: "Dette emnet beskriver Faktisk vs. budsjett-innholdet for Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdet, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a99af169bd1c447a15bc46a5adc89719dabc0718
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="358a4-104">Faktisk vs. budsjett Power BI-innhold</span><span class="sxs-lookup"><span data-stu-id="358a4-104">Actual vs budget Power BI content</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="358a4-105">Dette emnet beskriver **Faktisk vs. budsjett**-innholdet for Power BI.</span><span class="sxs-lookup"><span data-stu-id="358a4-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="358a4-106">Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.</span><span class="sxs-lookup"><span data-stu-id="358a4-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

## <a name="overview"></a><span data-ttu-id="358a4-107">Oversikt</span><span class="sxs-lookup"><span data-stu-id="358a4-107">Overview</span></span>

<span data-ttu-id="358a4-108">Den **Faktisk vs. budsjett** Power BI-innholdet ble opprettet for personer som har ansvar for overvåking av faktiske resultater mot budsjetterte resultater i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="358a4-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="358a4-109">**Faktisk vs. budsjett** Power BI-innhold gir oversikt over avvik i budsjettet.</span><span class="sxs-lookup"><span data-stu-id="358a4-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="358a4-110">Du kan analysere budsjettet for gjeldende år etter kontokategori, budsjettkode, hovedkontoe, beskrivelser av hovedkontoe eller regnskapsperiode for å få en bedre forståelse av eventuelle avvik.</span><span class="sxs-lookup"><span data-stu-id="358a4-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="358a4-111">Tilgang til Power BI-innhold</span><span class="sxs-lookup"><span data-stu-id="358a4-111">Accessing the Power BI content</span></span>
<span data-ttu-id="358a4-112">Rapporter fra Power BI-innholdet **Faktisk i forhold til budsjett** vises i **Finansbudsjetter og prognoser**- og **CFO**-arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="358a4-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="358a4-113">Rapporter som er inkludert i Power BI-innholdet</span><span class="sxs-lookup"><span data-stu-id="358a4-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="358a4-114">Tabellen nedenfor viser detaljer om mål som finnes på hver rapportside i **Faktisk vs. budsjett** Power BI-innholdet.</span><span class="sxs-lookup"><span data-stu-id="358a4-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>


|           <span data-ttu-id="358a4-115">Rapporter</span><span class="sxs-lookup"><span data-stu-id="358a4-115">Report</span></span>            |                                       <span data-ttu-id="358a4-116">Mål</span><span class="sxs-lookup"><span data-stu-id="358a4-116">Metrics</span></span>                                        |
|-----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="358a4-117">Utgifter – faktiske i forhold til budsjett</span><span class="sxs-lookup"><span data-stu-id="358a4-117">Expenses - Actual vs budget</span></span> |  <ul><li><span data-ttu-id="358a4-118">Totale utgifter i inneværende år</span><span class="sxs-lookup"><span data-stu-id="358a4-118">Total expenses this year</span></span></li><li><span data-ttu-id="358a4-119">Budsjetterte totale utgifter i inneværende år</span><span class="sxs-lookup"><span data-stu-id="358a4-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="358a4-120">Inntekt – faktisk i forhold til budsjett</span><span class="sxs-lookup"><span data-stu-id="358a4-120">Revenue - Actual vs budget</span></span>  |   <ul><li><span data-ttu-id="358a4-121">Totalomsetning i inneværende år</span><span class="sxs-lookup"><span data-stu-id="358a4-121">Total revenue this year</span></span></li><li><span data-ttu-id="358a4-122">Budsjettert totalomsetning i inneværende år</span><span class="sxs-lookup"><span data-stu-id="358a4-122">Budget total revenue this year</span></span></li><ul>    |
|           <span data-ttu-id="358a4-123">Utgift</span><span class="sxs-lookup"><span data-stu-id="358a4-123">Expense</span></span>           | <ul><li><span data-ttu-id="358a4-124">Totale utgifter i inneværende år</span><span class="sxs-lookup"><span data-stu-id="358a4-124">Total expenses this year</span></span></li><li><span data-ttu-id="358a4-125">Mål for utgifter basert på budsjett</span><span class="sxs-lookup"><span data-stu-id="358a4-125">Goal for expenses based on budget</span></span> </li><ul> |
|           <span data-ttu-id="358a4-126">Omsetning</span><span class="sxs-lookup"><span data-stu-id="358a4-126">Revenue</span></span>           |  <ul><li><span data-ttu-id="358a4-127">Totalomsetning i inneværende år</span><span class="sxs-lookup"><span data-stu-id="358a4-127">Total revenue this year</span></span></li><li><span data-ttu-id="358a4-128">Mål for inntekter basert på budsjett</span><span class="sxs-lookup"><span data-stu-id="358a4-128">Goal for revenue based on budget</span></span> </li><ul>  |
|         <span data-ttu-id="358a4-129">Nettoinntekt</span><span class="sxs-lookup"><span data-stu-id="358a4-129">Net income</span></span>          |  <ul><li><span data-ttu-id="358a4-130">Nettoinntekt i inneværende år</span><span class="sxs-lookup"><span data-stu-id="358a4-130">Net income this year</span></span></li><li><span data-ttu-id="358a4-131">Mål for nettoinntekt basert på budsjett</span><span class="sxs-lookup"><span data-stu-id="358a4-131">Goal for net income based on budget</span></span> </li><ul>  |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="358a4-132">Forstå datamodellen og enheter</span><span class="sxs-lookup"><span data-stu-id="358a4-132">Understanding the data model and entities</span></span>

|          <span data-ttu-id="358a4-133">Enhet</span><span class="sxs-lookup"><span data-stu-id="358a4-133">Entity</span></span>           |                                     <span data-ttu-id="358a4-134">Innhold</span><span class="sxs-lookup"><span data-stu-id="358a4-134">Contents</span></span>                                     |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="358a4-135">Aktiviteter i øknomimodulen</span><span class="sxs-lookup"><span data-stu-id="358a4-135">General Ledger Activities</span></span> |                    <span data-ttu-id="358a4-136">Transaksjonsbeløp for økonomimodulen</span><span class="sxs-lookup"><span data-stu-id="358a4-136">Transaction amounts for the general ledger</span></span>                    |
|     <span data-ttu-id="358a4-137">Budsjettaktiviteter</span><span class="sxs-lookup"><span data-stu-id="358a4-137">Budget Activities</span></span>     |                   <span data-ttu-id="358a4-138">Transaksjonsbeløp for budsjettregisteret</span><span class="sxs-lookup"><span data-stu-id="358a4-138">Transaction amounts for the budget register</span></span>                    |
|       <span data-ttu-id="358a4-139">Hovedkontoer</span><span class="sxs-lookup"><span data-stu-id="358a4-139">Main Accounts</span></span>       |                        <span data-ttu-id="358a4-140">Hovedkontoer rapporter kan filtreres etter</span><span class="sxs-lookup"><span data-stu-id="358a4-140">Main accounts to filter reports by</span></span>                        |
|     <span data-ttu-id="358a4-141">Regnskapskalendere</span><span class="sxs-lookup"><span data-stu-id="358a4-141">Fiscal Calendars</span></span>      |                      <span data-ttu-id="358a4-142">Regnskapskalendere rapporter kan filtreres etter</span><span class="sxs-lookup"><span data-stu-id="358a4-142">Fiscal calendars to filter reports by</span></span>                       |
|          <span data-ttu-id="358a4-143">Finanskontoer</span><span class="sxs-lookup"><span data-stu-id="358a4-143">Ledgers</span></span>          |       <span data-ttu-id="358a4-144">Finanskontoer som kan brukes til å filtrere rapporten til den gjeldende finanskontoen</span><span class="sxs-lookup"><span data-stu-id="358a4-144">Ledgers that can be used to filter the report to the current ledger</span></span>        |
|       <span data-ttu-id="358a4-145">Budsjettkoder</span><span class="sxs-lookup"><span data-stu-id="358a4-145">Budget Codes</span></span>        |                        <span data-ttu-id="358a4-146">Budsjettkoder rapporter kan filtreres etter</span><span class="sxs-lookup"><span data-stu-id="358a4-146">Budget codes to filter reports by</span></span>                         |
|      <span data-ttu-id="358a4-147">Juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="358a4-147">Legal Entities</span></span>       | <span data-ttu-id="358a4-148">Juridiske enheter som kan brukes til å filtrere rapporten til den gjeldende juridiske enheten</span><span class="sxs-lookup"><span data-stu-id="358a4-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |


