---
title: Livssyklus for partiordre fra oppretting til start
description: Denne prosedyren leder deg gjennom den første delen av livssyklusen til en partiordre.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d3582791fa0564e17338593152e13644322cdb44
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147187"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="b4214-103">Livssyklus for partiordre fra oppretting til start</span><span class="sxs-lookup"><span data-stu-id="b4214-103">Batch order lifecycle from create to start</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b4214-104">Denne prosedyren leder deg gjennom den første delen av livssyklusen til en partiordre.</span><span class="sxs-lookup"><span data-stu-id="b4214-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="b4214-105">Fra oppretting, kostnadsberegning og produksjonsjobbplanlegging til faktisk start av en partiordre.</span><span class="sxs-lookup"><span data-stu-id="b4214-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="b4214-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="b4214-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="b4214-107">Forutsetningene for å kjøre prosedyren med et annet datasett er et frigitt produkt med en aktiv formel- og ruteversjon.</span><span class="sxs-lookup"><span data-stu-id="b4214-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="b4214-108">Opprette en partiordre</span><span class="sxs-lookup"><span data-stu-id="b4214-108">Create a batch order</span></span>
1. <span data-ttu-id="b4214-109">Gå til Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="b4214-109">Go to All production orders.</span></span>
2. <span data-ttu-id="b4214-110">Klikk Ny partiordre.</span><span class="sxs-lookup"><span data-stu-id="b4214-110">Click New batch order.</span></span>
3. <span data-ttu-id="b4214-111">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="b4214-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="b4214-112">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="b4214-112">Click Create.</span></span>
5. <span data-ttu-id="b4214-113">Bruk hurtigfilteret til å filtrere på Produksjon-feltet med en verdi lik b.</span><span class="sxs-lookup"><span data-stu-id="b4214-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="b4214-114">Vise produksjonsformelen og forventede koprodukter</span><span class="sxs-lookup"><span data-stu-id="b4214-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="b4214-115">Klikk Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b4214-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="b4214-116">Klikk Formel.</span><span class="sxs-lookup"><span data-stu-id="b4214-116">Click Formula.</span></span>
3. <span data-ttu-id="b4214-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b4214-117">Close the page.</span></span>
4. <span data-ttu-id="b4214-118">Klikk Koprodukter.</span><span class="sxs-lookup"><span data-stu-id="b4214-118">Click Co-products.</span></span>
5. <span data-ttu-id="b4214-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b4214-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="b4214-120">Beregne partiordren</span><span class="sxs-lookup"><span data-stu-id="b4214-120">Estimate the batch order</span></span>
1. <span data-ttu-id="b4214-121">Klikk Estimer.</span><span class="sxs-lookup"><span data-stu-id="b4214-121">Click Estimate.</span></span>
2. <span data-ttu-id="b4214-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b4214-122">Click OK.</span></span>
3. <span data-ttu-id="b4214-123">Klikk Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b4214-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="b4214-124">Klikk Vis beregningsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="b4214-124">Click View calculation details.</span></span>
5. <span data-ttu-id="b4214-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b4214-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="b4214-126">Frigi partiordren</span><span class="sxs-lookup"><span data-stu-id="b4214-126">Release the batch order</span></span>
1. <span data-ttu-id="b4214-127">Klikk Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b4214-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="b4214-128">Klikk Frigi.</span><span class="sxs-lookup"><span data-stu-id="b4214-128">Click Release.</span></span>
3. <span data-ttu-id="b4214-129">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b4214-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="b4214-130">Planlegge produksjonsjobber</span><span class="sxs-lookup"><span data-stu-id="b4214-130">Schedule production jobs</span></span>
1. <span data-ttu-id="b4214-131">Klikk Planlegg i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b4214-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="b4214-132">Klikk Planlegg jobber.</span><span class="sxs-lookup"><span data-stu-id="b4214-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="b4214-133">Velg Nei i Begrenset kapasitet-feltet.</span><span class="sxs-lookup"><span data-stu-id="b4214-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="b4214-134">Velg Nei i Begrenset materiale-feltet.</span><span class="sxs-lookup"><span data-stu-id="b4214-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="b4214-135">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b4214-135">Click OK.</span></span>
6. <span data-ttu-id="b4214-136">Klikk Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b4214-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="b4214-137">Klikk Alle jobber.</span><span class="sxs-lookup"><span data-stu-id="b4214-137">Click All jobs.</span></span>
8. <span data-ttu-id="b4214-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b4214-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="b4214-139">Starte partiordren</span><span class="sxs-lookup"><span data-stu-id="b4214-139">Start the batch order</span></span>
1. <span data-ttu-id="b4214-140">Klikk Start.</span><span class="sxs-lookup"><span data-stu-id="b4214-140">Click Start.</span></span>
2. <span data-ttu-id="b4214-141">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="b4214-141">Click the General tab.</span></span>
3. <span data-ttu-id="b4214-142">Velg Nei i feltet Poster plukkliste nå.</span><span class="sxs-lookup"><span data-stu-id="b4214-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="b4214-143">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b4214-143">Click OK.</span></span>
5. <span data-ttu-id="b4214-144">Klikk Vis i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b4214-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="b4214-145">Klikk Plukkliste.</span><span class="sxs-lookup"><span data-stu-id="b4214-145">Click Picking list.</span></span>
7. <span data-ttu-id="b4214-146">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b4214-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="b4214-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b4214-147">Close the page.</span></span>
9. <span data-ttu-id="b4214-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b4214-148">Close the page.</span></span>
10. <span data-ttu-id="b4214-149">Klikk Rutekort.</span><span class="sxs-lookup"><span data-stu-id="b4214-149">Click Route card.</span></span>
11. <span data-ttu-id="b4214-150">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b4214-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="b4214-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b4214-151">Close the page.</span></span>
13. <span data-ttu-id="b4214-152">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b4214-152">Close the page.</span></span>

