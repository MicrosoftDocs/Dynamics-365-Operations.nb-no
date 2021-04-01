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
ms.openlocfilehash: 67c44341b1c8633917f41fa82593ab66611ca1ea
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255427"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="81fa0-103">Livssyklus for partiordre fra oppretting til start</span><span class="sxs-lookup"><span data-stu-id="81fa0-103">Batch order lifecycle from create to start</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="81fa0-104">Denne prosedyren leder deg gjennom den første delen av livssyklusen til en partiordre.</span><span class="sxs-lookup"><span data-stu-id="81fa0-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="81fa0-105">Fra oppretting, kostnadsberegning og produksjonsjobbplanlegging til faktisk start av en partiordre.</span><span class="sxs-lookup"><span data-stu-id="81fa0-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="81fa0-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="81fa0-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="81fa0-107">Forutsetningene for å kjøre prosedyren med et annet datasett er et frigitt produkt med en aktiv formel- og ruteversjon.</span><span class="sxs-lookup"><span data-stu-id="81fa0-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="81fa0-108">Opprette en partiordre</span><span class="sxs-lookup"><span data-stu-id="81fa0-108">Create a batch order</span></span>
1. <span data-ttu-id="81fa0-109">Gå til Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="81fa0-109">Go to All production orders.</span></span>
2. <span data-ttu-id="81fa0-110">Klikk på Ny partiordre.</span><span class="sxs-lookup"><span data-stu-id="81fa0-110">Click New batch order.</span></span>
3. <span data-ttu-id="81fa0-111">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="81fa0-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="81fa0-112">Klikk på Opprett.</span><span class="sxs-lookup"><span data-stu-id="81fa0-112">Click Create.</span></span>
5. <span data-ttu-id="81fa0-113">Bruk hurtigfilteret til å filtrere på Produksjon-feltet med en verdi lik b.</span><span class="sxs-lookup"><span data-stu-id="81fa0-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="81fa0-114">Vise produksjonsformelen og forventede koprodukter</span><span class="sxs-lookup"><span data-stu-id="81fa0-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="81fa0-115">Klikk på Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="81fa0-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="81fa0-116">Klikk på Formel.</span><span class="sxs-lookup"><span data-stu-id="81fa0-116">Click Formula.</span></span>
3. <span data-ttu-id="81fa0-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="81fa0-117">Close the page.</span></span>
4. <span data-ttu-id="81fa0-118">Klikk på Koprodukter.</span><span class="sxs-lookup"><span data-stu-id="81fa0-118">Click Co-products.</span></span>
5. <span data-ttu-id="81fa0-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="81fa0-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="81fa0-120">Beregne partiordren</span><span class="sxs-lookup"><span data-stu-id="81fa0-120">Estimate the batch order</span></span>
1. <span data-ttu-id="81fa0-121">Klikk på Estimer.</span><span class="sxs-lookup"><span data-stu-id="81fa0-121">Click Estimate.</span></span>
2. <span data-ttu-id="81fa0-122">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="81fa0-122">Click OK.</span></span>
3. <span data-ttu-id="81fa0-123">Klikk på Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="81fa0-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="81fa0-124">Klikk på Vis beregningsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="81fa0-124">Click View calculation details.</span></span>
5. <span data-ttu-id="81fa0-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="81fa0-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="81fa0-126">Frigi partiordren</span><span class="sxs-lookup"><span data-stu-id="81fa0-126">Release the batch order</span></span>
1. <span data-ttu-id="81fa0-127">Klikk på Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="81fa0-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="81fa0-128">Klikk på Frigi.</span><span class="sxs-lookup"><span data-stu-id="81fa0-128">Click Release.</span></span>
3. <span data-ttu-id="81fa0-129">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="81fa0-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="81fa0-130">Planlegge produksjonsjobber</span><span class="sxs-lookup"><span data-stu-id="81fa0-130">Schedule production jobs</span></span>
1. <span data-ttu-id="81fa0-131">Klikk på Planlegg i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="81fa0-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="81fa0-132">Klikk på Planlegg jobber.</span><span class="sxs-lookup"><span data-stu-id="81fa0-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="81fa0-133">Velg Nei i Begrenset kapasitet-feltet.</span><span class="sxs-lookup"><span data-stu-id="81fa0-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="81fa0-134">Velg Nei i Begrenset materiale-feltet.</span><span class="sxs-lookup"><span data-stu-id="81fa0-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="81fa0-135">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="81fa0-135">Click OK.</span></span>
6. <span data-ttu-id="81fa0-136">Klikk på Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="81fa0-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="81fa0-137">Klikk på Alle jobber.</span><span class="sxs-lookup"><span data-stu-id="81fa0-137">Click All jobs.</span></span>
8. <span data-ttu-id="81fa0-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="81fa0-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="81fa0-139">Starte partiordren</span><span class="sxs-lookup"><span data-stu-id="81fa0-139">Start the batch order</span></span>
1. <span data-ttu-id="81fa0-140">Klikk på Start.</span><span class="sxs-lookup"><span data-stu-id="81fa0-140">Click Start.</span></span>
2. <span data-ttu-id="81fa0-141">Klikk på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="81fa0-141">Click the General tab.</span></span>
3. <span data-ttu-id="81fa0-142">Velg Nei i feltet Poster plukkliste nå.</span><span class="sxs-lookup"><span data-stu-id="81fa0-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="81fa0-143">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="81fa0-143">Click OK.</span></span>
5. <span data-ttu-id="81fa0-144">Klikk på Vis i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="81fa0-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="81fa0-145">Klikk på Plukkliste.</span><span class="sxs-lookup"><span data-stu-id="81fa0-145">Click Picking list.</span></span>
7. <span data-ttu-id="81fa0-146">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="81fa0-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="81fa0-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="81fa0-147">Close the page.</span></span>
9. <span data-ttu-id="81fa0-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="81fa0-148">Close the page.</span></span>
10. <span data-ttu-id="81fa0-149">Klikk på Rutekort.</span><span class="sxs-lookup"><span data-stu-id="81fa0-149">Click Route card.</span></span>
11. <span data-ttu-id="81fa0-150">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="81fa0-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="81fa0-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="81fa0-151">Close the page.</span></span>
13. <span data-ttu-id="81fa0-152">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="81fa0-152">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]