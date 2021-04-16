---
title: Livssyklus for partiordre fra oppretting til start
description: Denne prosedyren leder deg gjennom den første delen av livssyklusen til en partiordre.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d9ed44c9e05ea815e78ae041234ad61f76d89d8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825044"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="1b481-103">Livssyklus for partiordre fra oppretting til start</span><span class="sxs-lookup"><span data-stu-id="1b481-103">Batch order lifecycle from create to start</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1b481-104">Denne prosedyren leder deg gjennom den første delen av livssyklusen til en partiordre.</span><span class="sxs-lookup"><span data-stu-id="1b481-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="1b481-105">Fra oppretting, kostnadsberegning og produksjonsjobbplanlegging til faktisk start av en partiordre.</span><span class="sxs-lookup"><span data-stu-id="1b481-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="1b481-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="1b481-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="1b481-107">Forutsetningene for å kjøre prosedyren med et annet datasett er et frigitt produkt med en aktiv formel- og ruteversjon.</span><span class="sxs-lookup"><span data-stu-id="1b481-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="1b481-108">Opprette en partiordre</span><span class="sxs-lookup"><span data-stu-id="1b481-108">Create a batch order</span></span>
1. <span data-ttu-id="1b481-109">Gå til Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="1b481-109">Go to All production orders.</span></span>
2. <span data-ttu-id="1b481-110">Klikk på Ny partiordre.</span><span class="sxs-lookup"><span data-stu-id="1b481-110">Click New batch order.</span></span>
3. <span data-ttu-id="1b481-111">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="1b481-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="1b481-112">Klikk på Opprett.</span><span class="sxs-lookup"><span data-stu-id="1b481-112">Click Create.</span></span>
5. <span data-ttu-id="1b481-113">Bruk hurtigfilteret til å filtrere på Produksjon-feltet med en verdi lik b.</span><span class="sxs-lookup"><span data-stu-id="1b481-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="1b481-114">Vise produksjonsformelen og forventede koprodukter</span><span class="sxs-lookup"><span data-stu-id="1b481-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="1b481-115">Klikk på Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="1b481-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="1b481-116">Klikk på Formel.</span><span class="sxs-lookup"><span data-stu-id="1b481-116">Click Formula.</span></span>
3. <span data-ttu-id="1b481-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1b481-117">Close the page.</span></span>
4. <span data-ttu-id="1b481-118">Klikk på Koprodukter.</span><span class="sxs-lookup"><span data-stu-id="1b481-118">Click Co-products.</span></span>
5. <span data-ttu-id="1b481-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1b481-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="1b481-120">Beregne partiordren</span><span class="sxs-lookup"><span data-stu-id="1b481-120">Estimate the batch order</span></span>
1. <span data-ttu-id="1b481-121">Klikk på Estimer.</span><span class="sxs-lookup"><span data-stu-id="1b481-121">Click Estimate.</span></span>
2. <span data-ttu-id="1b481-122">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="1b481-122">Click OK.</span></span>
3. <span data-ttu-id="1b481-123">Klikk på Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="1b481-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="1b481-124">Klikk på Vis beregningsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="1b481-124">Click View calculation details.</span></span>
5. <span data-ttu-id="1b481-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1b481-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="1b481-126">Frigi partiordren</span><span class="sxs-lookup"><span data-stu-id="1b481-126">Release the batch order</span></span>
1. <span data-ttu-id="1b481-127">Klikk på Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="1b481-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="1b481-128">Klikk på Frigi.</span><span class="sxs-lookup"><span data-stu-id="1b481-128">Click Release.</span></span>
3. <span data-ttu-id="1b481-129">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="1b481-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="1b481-130">Planlegge produksjonsjobber</span><span class="sxs-lookup"><span data-stu-id="1b481-130">Schedule production jobs</span></span>
1. <span data-ttu-id="1b481-131">Klikk på Planlegg i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="1b481-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="1b481-132">Klikk på Planlegg jobber.</span><span class="sxs-lookup"><span data-stu-id="1b481-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="1b481-133">Velg Nei i Begrenset kapasitet-feltet.</span><span class="sxs-lookup"><span data-stu-id="1b481-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="1b481-134">Velg Nei i Begrenset materiale-feltet.</span><span class="sxs-lookup"><span data-stu-id="1b481-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="1b481-135">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="1b481-135">Click OK.</span></span>
6. <span data-ttu-id="1b481-136">Klikk på Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="1b481-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="1b481-137">Klikk på Alle jobber.</span><span class="sxs-lookup"><span data-stu-id="1b481-137">Click All jobs.</span></span>
8. <span data-ttu-id="1b481-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1b481-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="1b481-139">Starte partiordren</span><span class="sxs-lookup"><span data-stu-id="1b481-139">Start the batch order</span></span>
1. <span data-ttu-id="1b481-140">Klikk på Start.</span><span class="sxs-lookup"><span data-stu-id="1b481-140">Click Start.</span></span>
2. <span data-ttu-id="1b481-141">Klikk på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="1b481-141">Click the General tab.</span></span>
3. <span data-ttu-id="1b481-142">Velg Nei i feltet Poster plukkliste nå.</span><span class="sxs-lookup"><span data-stu-id="1b481-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="1b481-143">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="1b481-143">Click OK.</span></span>
5. <span data-ttu-id="1b481-144">Klikk på Vis i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="1b481-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="1b481-145">Klikk på Plukkliste.</span><span class="sxs-lookup"><span data-stu-id="1b481-145">Click Picking list.</span></span>
7. <span data-ttu-id="1b481-146">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="1b481-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="1b481-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1b481-147">Close the page.</span></span>
9. <span data-ttu-id="1b481-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1b481-148">Close the page.</span></span>
10. <span data-ttu-id="1b481-149">Klikk på Rutekort.</span><span class="sxs-lookup"><span data-stu-id="1b481-149">Click Route card.</span></span>
11. <span data-ttu-id="1b481-150">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="1b481-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="1b481-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1b481-151">Close the page.</span></span>
13. <span data-ttu-id="1b481-152">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1b481-152">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]