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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16b55726fdb9ab15e74a9f752cac972b80a98de2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210991"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="4287e-103">Livssyklus for partiordre fra oppretting til start</span><span class="sxs-lookup"><span data-stu-id="4287e-103">Batch order lifecycle from create to start</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4287e-104">Denne prosedyren leder deg gjennom den første delen av livssyklusen til en partiordre.</span><span class="sxs-lookup"><span data-stu-id="4287e-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="4287e-105">Fra oppretting, kostnadsberegning og produksjonsjobbplanlegging til faktisk start av en partiordre.</span><span class="sxs-lookup"><span data-stu-id="4287e-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="4287e-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="4287e-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="4287e-107">Forutsetningene for å kjøre prosedyren med et annet datasett er et frigitt produkt med en aktiv formel- og ruteversjon.</span><span class="sxs-lookup"><span data-stu-id="4287e-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="4287e-108">Opprette en partiordre</span><span class="sxs-lookup"><span data-stu-id="4287e-108">Create a batch order</span></span>
1. <span data-ttu-id="4287e-109">Gå til Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="4287e-109">Go to All production orders.</span></span>
2. <span data-ttu-id="4287e-110">Klikk Ny partiordre.</span><span class="sxs-lookup"><span data-stu-id="4287e-110">Click New batch order.</span></span>
3. <span data-ttu-id="4287e-111">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="4287e-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="4287e-112">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="4287e-112">Click Create.</span></span>
5. <span data-ttu-id="4287e-113">Bruk hurtigfilteret til å filtrere på Produksjon-feltet med en verdi lik b.</span><span class="sxs-lookup"><span data-stu-id="4287e-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="4287e-114">Vise produksjonsformelen og forventede koprodukter</span><span class="sxs-lookup"><span data-stu-id="4287e-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="4287e-115">Klikk Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4287e-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="4287e-116">Klikk Formel.</span><span class="sxs-lookup"><span data-stu-id="4287e-116">Click Formula.</span></span>
3. <span data-ttu-id="4287e-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4287e-117">Close the page.</span></span>
4. <span data-ttu-id="4287e-118">Klikk Koprodukter.</span><span class="sxs-lookup"><span data-stu-id="4287e-118">Click Co-products.</span></span>
5. <span data-ttu-id="4287e-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4287e-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="4287e-120">Beregne partiordren</span><span class="sxs-lookup"><span data-stu-id="4287e-120">Estimate the batch order</span></span>
1. <span data-ttu-id="4287e-121">Klikk Estimer.</span><span class="sxs-lookup"><span data-stu-id="4287e-121">Click Estimate.</span></span>
2. <span data-ttu-id="4287e-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4287e-122">Click OK.</span></span>
3. <span data-ttu-id="4287e-123">Klikk Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4287e-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="4287e-124">Klikk Vis beregningsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="4287e-124">Click View calculation details.</span></span>
5. <span data-ttu-id="4287e-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4287e-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="4287e-126">Frigi partiordren</span><span class="sxs-lookup"><span data-stu-id="4287e-126">Release the batch order</span></span>
1. <span data-ttu-id="4287e-127">Klikk Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4287e-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="4287e-128">Klikk Frigi.</span><span class="sxs-lookup"><span data-stu-id="4287e-128">Click Release.</span></span>
3. <span data-ttu-id="4287e-129">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4287e-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="4287e-130">Planlegge produksjonsjobber</span><span class="sxs-lookup"><span data-stu-id="4287e-130">Schedule production jobs</span></span>
1. <span data-ttu-id="4287e-131">Klikk Planlegg i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4287e-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="4287e-132">Klikk Planlegg jobber.</span><span class="sxs-lookup"><span data-stu-id="4287e-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="4287e-133">Velg Nei i Begrenset kapasitet-feltet.</span><span class="sxs-lookup"><span data-stu-id="4287e-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="4287e-134">Velg Nei i Begrenset materiale-feltet.</span><span class="sxs-lookup"><span data-stu-id="4287e-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="4287e-135">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4287e-135">Click OK.</span></span>
6. <span data-ttu-id="4287e-136">Klikk Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4287e-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="4287e-137">Klikk Alle jobber.</span><span class="sxs-lookup"><span data-stu-id="4287e-137">Click All jobs.</span></span>
8. <span data-ttu-id="4287e-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4287e-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="4287e-139">Starte partiordren</span><span class="sxs-lookup"><span data-stu-id="4287e-139">Start the batch order</span></span>
1. <span data-ttu-id="4287e-140">Klikk Start.</span><span class="sxs-lookup"><span data-stu-id="4287e-140">Click Start.</span></span>
2. <span data-ttu-id="4287e-141">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="4287e-141">Click the General tab.</span></span>
3. <span data-ttu-id="4287e-142">Velg Nei i feltet Poster plukkliste nå.</span><span class="sxs-lookup"><span data-stu-id="4287e-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="4287e-143">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4287e-143">Click OK.</span></span>
5. <span data-ttu-id="4287e-144">Klikk Vis i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4287e-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="4287e-145">Klikk Plukkliste.</span><span class="sxs-lookup"><span data-stu-id="4287e-145">Click Picking list.</span></span>
7. <span data-ttu-id="4287e-146">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4287e-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="4287e-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4287e-147">Close the page.</span></span>
9. <span data-ttu-id="4287e-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4287e-148">Close the page.</span></span>
10. <span data-ttu-id="4287e-149">Klikk Rutekort.</span><span class="sxs-lookup"><span data-stu-id="4287e-149">Click Route card.</span></span>
11. <span data-ttu-id="4287e-150">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4287e-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="4287e-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4287e-151">Close the page.</span></span>
13. <span data-ttu-id="4287e-152">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4287e-152">Close the page.</span></span>

