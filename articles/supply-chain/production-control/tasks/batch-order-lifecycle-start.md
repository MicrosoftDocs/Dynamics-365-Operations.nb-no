---
title: Livssyklus for partiordre fra oppretting til start
description: Denne prosedyren leder deg gjennom den første delen av livssyklusen til en partiordre.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5fd04587c95ba8a48750f96302a11aeaf82308d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981412"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="82907-103">Livssyklus for partiordre fra oppretting til start</span><span class="sxs-lookup"><span data-stu-id="82907-103">Batch order lifecycle from create to start</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="82907-104">Denne prosedyren leder deg gjennom den første delen av livssyklusen til en partiordre.</span><span class="sxs-lookup"><span data-stu-id="82907-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="82907-105">Fra oppretting, kostnadsberegning og produksjonsjobbplanlegging til faktisk start av en partiordre.</span><span class="sxs-lookup"><span data-stu-id="82907-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="82907-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="82907-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="82907-107">Forutsetningene for å kjøre prosedyren med et annet datasett er et frigitt produkt med en aktiv formel- og ruteversjon.</span><span class="sxs-lookup"><span data-stu-id="82907-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="82907-108">Opprette en partiordre</span><span class="sxs-lookup"><span data-stu-id="82907-108">Create a batch order</span></span>
1. <span data-ttu-id="82907-109">Gå til Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="82907-109">Go to All production orders.</span></span>
2. <span data-ttu-id="82907-110">Klikk på Ny partiordre.</span><span class="sxs-lookup"><span data-stu-id="82907-110">Click New batch order.</span></span>
3. <span data-ttu-id="82907-111">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="82907-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="82907-112">Klikk på Opprett.</span><span class="sxs-lookup"><span data-stu-id="82907-112">Click Create.</span></span>
5. <span data-ttu-id="82907-113">Bruk hurtigfilteret til å filtrere på Produksjon-feltet med en verdi lik b.</span><span class="sxs-lookup"><span data-stu-id="82907-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="82907-114">Vise produksjonsformelen og forventede koprodukter</span><span class="sxs-lookup"><span data-stu-id="82907-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="82907-115">Klikk på Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="82907-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="82907-116">Klikk på Formel.</span><span class="sxs-lookup"><span data-stu-id="82907-116">Click Formula.</span></span>
3. <span data-ttu-id="82907-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="82907-117">Close the page.</span></span>
4. <span data-ttu-id="82907-118">Klikk på Koprodukter.</span><span class="sxs-lookup"><span data-stu-id="82907-118">Click Co-products.</span></span>
5. <span data-ttu-id="82907-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="82907-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="82907-120">Beregne partiordren</span><span class="sxs-lookup"><span data-stu-id="82907-120">Estimate the batch order</span></span>
1. <span data-ttu-id="82907-121">Klikk på Estimer.</span><span class="sxs-lookup"><span data-stu-id="82907-121">Click Estimate.</span></span>
2. <span data-ttu-id="82907-122">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="82907-122">Click OK.</span></span>
3. <span data-ttu-id="82907-123">Klikk på Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="82907-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="82907-124">Klikk på Vis beregningsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="82907-124">Click View calculation details.</span></span>
5. <span data-ttu-id="82907-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="82907-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="82907-126">Frigi partiordren</span><span class="sxs-lookup"><span data-stu-id="82907-126">Release the batch order</span></span>
1. <span data-ttu-id="82907-127">Klikk på Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="82907-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="82907-128">Klikk på Frigi.</span><span class="sxs-lookup"><span data-stu-id="82907-128">Click Release.</span></span>
3. <span data-ttu-id="82907-129">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="82907-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="82907-130">Planlegge produksjonsjobber</span><span class="sxs-lookup"><span data-stu-id="82907-130">Schedule production jobs</span></span>
1. <span data-ttu-id="82907-131">Klikk på Planlegg i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="82907-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="82907-132">Klikk på Planlegg jobber.</span><span class="sxs-lookup"><span data-stu-id="82907-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="82907-133">Velg Nei i Begrenset kapasitet-feltet.</span><span class="sxs-lookup"><span data-stu-id="82907-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="82907-134">Velg Nei i Begrenset materiale-feltet.</span><span class="sxs-lookup"><span data-stu-id="82907-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="82907-135">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="82907-135">Click OK.</span></span>
6. <span data-ttu-id="82907-136">Klikk på Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="82907-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="82907-137">Klikk på Alle jobber.</span><span class="sxs-lookup"><span data-stu-id="82907-137">Click All jobs.</span></span>
8. <span data-ttu-id="82907-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="82907-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="82907-139">Starte partiordren</span><span class="sxs-lookup"><span data-stu-id="82907-139">Start the batch order</span></span>
1. <span data-ttu-id="82907-140">Klikk på Start.</span><span class="sxs-lookup"><span data-stu-id="82907-140">Click Start.</span></span>
2. <span data-ttu-id="82907-141">Klikk på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="82907-141">Click the General tab.</span></span>
3. <span data-ttu-id="82907-142">Velg Nei i feltet Poster plukkliste nå.</span><span class="sxs-lookup"><span data-stu-id="82907-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="82907-143">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="82907-143">Click OK.</span></span>
5. <span data-ttu-id="82907-144">Klikk på Vis i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="82907-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="82907-145">Klikk på Plukkliste.</span><span class="sxs-lookup"><span data-stu-id="82907-145">Click Picking list.</span></span>
7. <span data-ttu-id="82907-146">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="82907-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="82907-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="82907-147">Close the page.</span></span>
9. <span data-ttu-id="82907-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="82907-148">Close the page.</span></span>
10. <span data-ttu-id="82907-149">Klikk på Rutekort.</span><span class="sxs-lookup"><span data-stu-id="82907-149">Click Route card.</span></span>
11. <span data-ttu-id="82907-150">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="82907-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="82907-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="82907-151">Close the page.</span></span>
13. <span data-ttu-id="82907-152">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="82907-152">Close the page.</span></span>

