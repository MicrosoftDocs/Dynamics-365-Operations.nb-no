--- 
title: Opprette en basislinjeprognose
description: "En produksjonsplanlegger kan opprette en basislinjeprognose ved å bruke tidsserie-prognosemodeller eller ved å kopiere det historiske behovet."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e6363ee48c0d13c79a6c623205dfa10f50d6070f
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-baseline-forecast"></a><span data-ttu-id="90a3f-103">Opprette en basislinjeprognose</span><span class="sxs-lookup"><span data-stu-id="90a3f-103">Create a baseline forecast</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="90a3f-104">En produksjonsplanlegger kan opprette en basislinjeprognose ved å bruke tidsserie-prognosemodeller eller ved å kopiere det historiske behovet.</span><span class="sxs-lookup"><span data-stu-id="90a3f-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="90a3f-105">Denne fremgangsmåten viser hvordan du kopierer det historiske behovet for å opprette en basislinjeprognose for alle produkter som bruker én varetildelingsnøkkel.</span><span class="sxs-lookup"><span data-stu-id="90a3f-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span> 


## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="90a3f-106">Definere en nøkkel for varefordeling</span><span class="sxs-lookup"><span data-stu-id="90a3f-106">Set up an item allocation key</span></span>
1. <span data-ttu-id="90a3f-107">Gå til Hovedplanlegging > Oppsett > Konserninterne planleggingsgrupper.</span><span class="sxs-lookup"><span data-stu-id="90a3f-107">Go to Master planning > Setup > Intercompany planning groups.</span></span>
2. <span data-ttu-id="90a3f-108">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="90a3f-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="90a3f-109">Du kan for eksempel filtrere på Navn-feltet med verdien 10.</span><span class="sxs-lookup"><span data-stu-id="90a3f-109">For example, filter on the Name field with a value of '10'.</span></span>
    * <span data-ttu-id="90a3f-110">Behovsprognose kjører på tvers av juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="90a3f-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="90a3f-111">Derfor må du definere alle selskapene som du vil generere prognoser for, i én konsernintern planleggingsgruppe.</span><span class="sxs-lookup"><span data-stu-id="90a3f-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="90a3f-112">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="90a3f-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="90a3f-113">Klikk Varefordelingsnøkler.</span><span class="sxs-lookup"><span data-stu-id="90a3f-113">Click Item allocation keys.</span></span>
    * <span data-ttu-id="90a3f-114">Velg alle varetildelingsnøklene du vil opprette prognoser for.</span><span class="sxs-lookup"><span data-stu-id="90a3f-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="90a3f-115">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="90a3f-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="90a3f-116">Velg D_Aloc varetildelingsnøkkelen.</span><span class="sxs-lookup"><span data-stu-id="90a3f-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="90a3f-117">Klikk >.</span><span class="sxs-lookup"><span data-stu-id="90a3f-117">Click >.</span></span>
7. <span data-ttu-id="90a3f-118">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="90a3f-118">Close the page.</span></span>
8. <span data-ttu-id="90a3f-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="90a3f-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-paramters"></a><span data-ttu-id="90a3f-120">Definere parameterne for behovsprognose</span><span class="sxs-lookup"><span data-stu-id="90a3f-120">Set up the demand forecasting paramters</span></span>
1. <span data-ttu-id="90a3f-121">Gå til Hovedplanlegging > Oppsett > Behovsprognose > Parametere for behovsprognose.</span><span class="sxs-lookup"><span data-stu-id="90a3f-121">Go to Master planning > Setup > Demand forecasting > Demand forecasting parameters.</span></span>
2. <span data-ttu-id="90a3f-122">Utvid delen Prognosealgoritmeparametere.</span><span class="sxs-lookup"><span data-stu-id="90a3f-122">Expand the Forecast algorithm parameters section.</span></span>
3. <span data-ttu-id="90a3f-123">Velg Kopier over historisk behov i feltet Strategi for prognosegenerering.</span><span class="sxs-lookup"><span data-stu-id="90a3f-123">In the Forecast generation strategy field, select 'Copy over historical demand'.</span></span>
4. <span data-ttu-id="90a3f-124">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="90a3f-124">Click Save.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="90a3f-125">Opprette en basislinjeprognose</span><span class="sxs-lookup"><span data-stu-id="90a3f-125">Create a baseline forecast</span></span>
1. <span data-ttu-id="90a3f-126">Gå til Hovedplanlegging > Prognose > Behovsprognose > Generer statistisk basislinjeprognose.</span><span class="sxs-lookup"><span data-stu-id="90a3f-126">Go to Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast.</span></span>
2. <span data-ttu-id="90a3f-127">Angi en dato i Fra dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="90a3f-127">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="90a3f-128">Angi denne datoen hvis du har salgsordrer fra og med 1. januar 2015.</span><span class="sxs-lookup"><span data-stu-id="90a3f-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="90a3f-129">Hvis ikke kan du angi den tidligste datoen for salgsordrene.</span><span class="sxs-lookup"><span data-stu-id="90a3f-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="90a3f-130">Angi en dato i Til dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="90a3f-130">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="90a3f-131">Angi den siste datoen i salgsordrene, for eksempel 2015-03-31.</span><span class="sxs-lookup"><span data-stu-id="90a3f-131">Enter the last date of your sales orders, for example '2015-03-31'.</span></span>  
4. <span data-ttu-id="90a3f-132">Angi en dato i Fra dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="90a3f-132">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="90a3f-133">Angi 2015-04-01.</span><span class="sxs-lookup"><span data-stu-id="90a3f-133">Enter '2015-04-01'.</span></span> <span data-ttu-id="90a3f-134">Denne datoen beregnes automatisk som startdatoen for den neste prognoseperioden.</span><span class="sxs-lookup"><span data-stu-id="90a3f-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="90a3f-135">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="90a3f-135">Expand the Records to include section.</span></span>
6. <span data-ttu-id="90a3f-136">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="90a3f-136">Click Filter.</span></span>
7. <span data-ttu-id="90a3f-137">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="90a3f-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="90a3f-138">Merk raden der feltet = Konsernintern planleggingsgruppe.</span><span class="sxs-lookup"><span data-stu-id="90a3f-138">Mark the row where Field = Intercompany planning group.</span></span>  
8. <span data-ttu-id="90a3f-139">Skriv inn en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="90a3f-139">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="90a3f-140">Skriv inn den konserninterne planleggingsgruppen, for eksempel 10, som du brukte i den første oppgaven.</span><span class="sxs-lookup"><span data-stu-id="90a3f-140">Type the intercompany planning group, for example, 10, that you used in the first task.</span></span>  
9. <span data-ttu-id="90a3f-141">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="90a3f-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="90a3f-142">Merk raden der feltet = Varetildelingsnøkkel.</span><span class="sxs-lookup"><span data-stu-id="90a3f-142">Select the row where Field = Item allocation key.</span></span>  
10. <span data-ttu-id="90a3f-143">Skriv inn en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="90a3f-143">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="90a3f-144">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="90a3f-144">Click OK.</span></span>
12. <span data-ttu-id="90a3f-145">Utvid seksjonen Avanserte parametere.</span><span class="sxs-lookup"><span data-stu-id="90a3f-145">Expand the Advanced parameters section.</span></span>
13. <span data-ttu-id="90a3f-146">Velg Måned i Prognoseperiode-feltet.</span><span class="sxs-lookup"><span data-stu-id="90a3f-146">In the Forecast bucket field, select 'Month'.</span></span>
14. <span data-ttu-id="90a3f-147">Angi 3 i Prognosehorisont-feltet.</span><span class="sxs-lookup"><span data-stu-id="90a3f-147">In the Forecast horizon field, enter '3'.</span></span>
15. <span data-ttu-id="90a3f-148">Angi 1 i feltet Låsningshorisont.</span><span class="sxs-lookup"><span data-stu-id="90a3f-148">In the Freeze time fence field, enter '1'.</span></span>
16. <span data-ttu-id="90a3f-149">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="90a3f-149">Click OK.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="90a3f-150">Visualisere behovsprognosen</span><span class="sxs-lookup"><span data-stu-id="90a3f-150">Visualize the demand forecast</span></span>
1. <span data-ttu-id="90a3f-151">Gå til Hovedplanlegging > Prognose > Behovsprognose > Justert behovsprognose.</span><span class="sxs-lookup"><span data-stu-id="90a3f-151">Go to Master planning > Forecasting > Demand forecasting > Adjusted demand forecast.</span></span>
2. <span data-ttu-id="90a3f-152">Velg cellen i rad 1, kolonne 2 i tabellen for aggregert visning.</span><span class="sxs-lookup"><span data-stu-id="90a3f-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="90a3f-153">Dette er den andre måneden du har opprettet prognose.</span><span class="sxs-lookup"><span data-stu-id="90a3f-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="90a3f-154">Sett QtyCell til "400".</span><span class="sxs-lookup"><span data-stu-id="90a3f-154">Set QtyCell to '400'.</span></span>
    * <span data-ttu-id="90a3f-155">I cellen angir du et annet nummer enn prognoseverdien, for eksempel 400.</span><span class="sxs-lookup"><span data-stu-id="90a3f-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="90a3f-156">Du har gjort en manuell justering av prognosen.</span><span class="sxs-lookup"><span data-stu-id="90a3f-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="90a3f-157">Legg merke til den grafiske indikasjonen i neste trinn.</span><span class="sxs-lookup"><span data-stu-id="90a3f-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="90a3f-158">Klikk Prognoselinjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="90a3f-158">Click Forecast line details.</span></span>
    * <span data-ttu-id="90a3f-159">På denne siden kan du se presisjonsverdier, historisk behov og prognose.</span><span class="sxs-lookup"><span data-stu-id="90a3f-159">In this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="90a3f-160">Du kan også endre prognosen.</span><span class="sxs-lookup"><span data-stu-id="90a3f-160">You can make changes to the forecast as well.</span></span>  


