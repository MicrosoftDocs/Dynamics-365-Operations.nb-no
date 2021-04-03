---
title: Power BI-innholdet Faktisk vs. budsjett
description: Dette emnet beskriver Faktisk vs. budsjett-innholdet for Power BI. Det forklarer hvordan du får tilgang til rapportene og gir informasjon om datamodellen.
author: panolte
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: f3e2f62b666559ba9a356e4948c2033da9cc95d5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568579"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="7e5b3-104">Power BI-innholdet Faktisk vs. budsjett</span><span class="sxs-lookup"><span data-stu-id="7e5b3-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e5b3-105">Dette emnet beskriver Microsoft Power BI-innholdet i **Faktisk i forhold til budsjett**.</span><span class="sxs-lookup"><span data-stu-id="7e5b3-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="7e5b3-106">Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.</span><span class="sxs-lookup"><span data-stu-id="7e5b3-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="7e5b3-107">Oversikt</span><span class="sxs-lookup"><span data-stu-id="7e5b3-107">Overview</span></span>

<span data-ttu-id="7e5b3-108">Power BI-innholdet **Faktisk vs. budsjett** ble opprettet for personer som har ansvar for overvåking av faktiske resultater mot budsjetterte resultater i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="7e5b3-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="7e5b3-109">Power BI-innholdet **Faktisk vs. budsjett** gir oversikt over avvik i budsjettet.</span><span class="sxs-lookup"><span data-stu-id="7e5b3-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="7e5b3-110">Du kan analysere budsjettet for gjeldende år etter kontokategori, budsjettkode, hovedkontoe, beskrivelser av hovedkontoe eller regnskapsperiode for å få en bedre forståelse av eventuelle avvik.</span><span class="sxs-lookup"><span data-stu-id="7e5b3-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="7e5b3-111">Tilgang til Power BI-innholdet</span><span class="sxs-lookup"><span data-stu-id="7e5b3-111">Accessing the Power BI content</span></span>
<span data-ttu-id="7e5b3-112">Rapporter fra Power BI-innholdet **Faktisk i forhold til budsjett** vises i **Finansbudsjetter og prognoser**- og **CFO**-arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="7e5b3-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="7e5b3-113">Rapporter som er inkludert i Power BI-innholdet</span><span class="sxs-lookup"><span data-stu-id="7e5b3-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="7e5b3-114">Tabellen nedenfor viser detaljer om mål som finnes på hver rapportside i Power BI-innholdet **Faktisk vs. budsjett**.</span><span class="sxs-lookup"><span data-stu-id="7e5b3-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="7e5b3-115">Rapporter</span><span class="sxs-lookup"><span data-stu-id="7e5b3-115">Report</span></span>                      | <span data-ttu-id="7e5b3-116">Mål</span><span class="sxs-lookup"><span data-stu-id="7e5b3-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7e5b3-117">Utgifter – faktiske i forhold til budsjett</span><span class="sxs-lookup"><span data-stu-id="7e5b3-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="7e5b3-118">Totale utgifter i inneværende år</span><span class="sxs-lookup"><span data-stu-id="7e5b3-118">Total expenses this year</span></span></li><li><span data-ttu-id="7e5b3-119">Budsjetterte totale utgifter i inneværende år</span><span class="sxs-lookup"><span data-stu-id="7e5b3-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="7e5b3-120">Inntekt – faktisk i forhold til budsjett</span><span class="sxs-lookup"><span data-stu-id="7e5b3-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="7e5b3-121">Totalomsetning i inneværende år</span><span class="sxs-lookup"><span data-stu-id="7e5b3-121">Total revenue this year</span></span></li><li><span data-ttu-id="7e5b3-122">Budsjettert totalomsetning i inneværende år</span><span class="sxs-lookup"><span data-stu-id="7e5b3-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="7e5b3-123">Utgift</span><span class="sxs-lookup"><span data-stu-id="7e5b3-123">Expense</span></span>                     | <ul><li><span data-ttu-id="7e5b3-124">Totale utgifter i inneværende år</span><span class="sxs-lookup"><span data-stu-id="7e5b3-124">Total expenses this year</span></span></li><li><span data-ttu-id="7e5b3-125">Mål for utgifter basert på budsjett</span><span class="sxs-lookup"><span data-stu-id="7e5b3-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="7e5b3-126">Omsetning</span><span class="sxs-lookup"><span data-stu-id="7e5b3-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="7e5b3-127">Totalomsetning i inneværende år</span><span class="sxs-lookup"><span data-stu-id="7e5b3-127">Total revenue this year</span></span></li><li><span data-ttu-id="7e5b3-128">Mål for inntekter basert på budsjett</span><span class="sxs-lookup"><span data-stu-id="7e5b3-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="7e5b3-129">Nettoinntekt</span><span class="sxs-lookup"><span data-stu-id="7e5b3-129">Net income</span></span>                  | <ul><li><span data-ttu-id="7e5b3-130">Nettoinntekt i inneværende år</span><span class="sxs-lookup"><span data-stu-id="7e5b3-130">Net income this year</span></span></li><li><span data-ttu-id="7e5b3-131">Mål for nettoinntekt basert på budsjett</span><span class="sxs-lookup"><span data-stu-id="7e5b3-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="7e5b3-132">Forstå datamodellen og enheter</span><span class="sxs-lookup"><span data-stu-id="7e5b3-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="7e5b3-133">Enhet</span><span class="sxs-lookup"><span data-stu-id="7e5b3-133">Entity</span></span>                    | <span data-ttu-id="7e5b3-134">Innhold</span><span class="sxs-lookup"><span data-stu-id="7e5b3-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7e5b3-135">Aktiviteter i øknomimodulen</span><span class="sxs-lookup"><span data-stu-id="7e5b3-135">General Ledger Activities</span></span> | <span data-ttu-id="7e5b3-136">Transaksjonsbeløp for økonomimodulen</span><span class="sxs-lookup"><span data-stu-id="7e5b3-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="7e5b3-137">Budsjettaktiviteter</span><span class="sxs-lookup"><span data-stu-id="7e5b3-137">Budget Activities</span></span>         | <span data-ttu-id="7e5b3-138">Transaksjonsbeløp for budsjettregisteret</span><span class="sxs-lookup"><span data-stu-id="7e5b3-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="7e5b3-139">Hovedkontoer</span><span class="sxs-lookup"><span data-stu-id="7e5b3-139">Main Accounts</span></span>             | <span data-ttu-id="7e5b3-140">Hovedkontoer rapporter kan filtreres etter</span><span class="sxs-lookup"><span data-stu-id="7e5b3-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="7e5b3-141">Regnskapskalendere</span><span class="sxs-lookup"><span data-stu-id="7e5b3-141">Fiscal Calendars</span></span>          | <span data-ttu-id="7e5b3-142">Regnskapskalendere rapporter kan filtreres etter</span><span class="sxs-lookup"><span data-stu-id="7e5b3-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="7e5b3-143">Finanskontoer</span><span class="sxs-lookup"><span data-stu-id="7e5b3-143">Ledgers</span></span>                   | <span data-ttu-id="7e5b3-144">Finanskontoer som kan brukes til å filtrere rapporten til den gjeldende finanskontoen</span><span class="sxs-lookup"><span data-stu-id="7e5b3-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="7e5b3-145">Budsjettkoder</span><span class="sxs-lookup"><span data-stu-id="7e5b3-145">Budget Codes</span></span>              | <span data-ttu-id="7e5b3-146">Budsjettkoder rapporter kan filtreres etter</span><span class="sxs-lookup"><span data-stu-id="7e5b3-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="7e5b3-147">Juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="7e5b3-147">Legal Entities</span></span>            | <span data-ttu-id="7e5b3-148">Juridiske enheter som kan brukes til å filtrere rapporten til den gjeldende juridiske enheten</span><span class="sxs-lookup"><span data-stu-id="7e5b3-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]