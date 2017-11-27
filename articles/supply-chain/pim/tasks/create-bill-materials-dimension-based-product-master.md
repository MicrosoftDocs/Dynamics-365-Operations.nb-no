--- 
title: Opprette en stykkliste for en dimensjonsbasert produktstandard
description: "For denne prosedyren skal du har fullført de 4 forrige veiledningene i disse trinnene med åtte registreringer."
author: YuyuScheller
manager: AnnBe
ms.date: 11/03/2017
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
ms.sourcegitcommit: 8b5432addd1dd79a64dcbb751a59cf3084a63ab1
ms.openlocfilehash: 05837c2b21957133729074f614a6d3d7b7c08dad
ms.contentlocale: nb-no
ms.lasthandoff: 11/04/2017

---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="c66b5-103">Opprette en stykkliste for en dimensjonsbasert produktstandard</span><span class="sxs-lookup"><span data-stu-id="c66b5-103">Create a bill of materials for a dimension-based product master</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c66b5-104">For denne prosedyren skal du har fullført de 4 forrige veiledningene i disse trinnene med åtte registreringer.</span><span class="sxs-lookup"><span data-stu-id="c66b5-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="c66b5-105">De 4 første registreringene definerer dataene som kreves for å fullføre denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="c66b5-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="c66b5-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="c66b5-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c66b5-107">Denne oppgaven håndteres vanligvis av produktdesigneren.</span><span class="sxs-lookup"><span data-stu-id="c66b5-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="c66b5-108">Velg produkt</span><span class="sxs-lookup"><span data-stu-id="c66b5-108">Select the product</span></span>
1. <span data-ttu-id="c66b5-109">Klikk Vedlikehold av frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="c66b5-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="c66b5-110">Klikk Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="c66b5-110">Click Released products.</span></span>
3. <span data-ttu-id="c66b5-111">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c66b5-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c66b5-112">Finn den frigitte produktstandarden med dimensjonsbasert konfigurasjonsteknologi, som du opprettet i den første oppgaveveiledningen i disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="c66b5-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="c66b5-113">Klikk Utvikling i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c66b5-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="c66b5-114">Klikk Stykklisteversjon.</span><span class="sxs-lookup"><span data-stu-id="c66b5-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="c66b5-115">Opprette ny stykkliste og stykklisteversjon</span><span class="sxs-lookup"><span data-stu-id="c66b5-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="c66b5-116">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c66b5-116">Click New.</span></span>
2. <span data-ttu-id="c66b5-117">Klikk Stykkliste og stykklisteversjon.</span><span class="sxs-lookup"><span data-stu-id="c66b5-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="c66b5-118">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="c66b5-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="c66b5-119">Angi et område</span><span class="sxs-lookup"><span data-stu-id="c66b5-119">Setting a site</span></span>  
    * <span data-ttu-id="c66b5-120">Vi angir ikke et bestemt område for stykklisten i denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="c66b5-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="c66b5-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c66b5-121">Click OK.</span></span>
5. <span data-ttu-id="c66b5-122">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c66b5-122">Click New.</span></span>
    * <span data-ttu-id="c66b5-123">I denne fremgangsmåten skal vi legge til fire linjer i stykklisten.</span><span class="sxs-lookup"><span data-stu-id="c66b5-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="c66b5-124">To linjer representerer kabelalternativer og to linjer representerer kabinettalternativer.</span><span class="sxs-lookup"><span data-stu-id="c66b5-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="c66b5-125">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c66b5-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="c66b5-126">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="c66b5-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="c66b5-127">Velge varenummer A0001, HDMI 6' Kabler.</span><span class="sxs-lookup"><span data-stu-id="c66b5-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="c66b5-128">Angi eller velg en verdi i feltet Konfigurasjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c66b5-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="c66b5-129">Velg konfigurasjonsgruppen Kabel, som ble opprettet i veiledning 4 i disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="c66b5-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="c66b5-130">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c66b5-130">Click New.</span></span>
    * <span data-ttu-id="c66b5-131">Velge varenummer A0002, HDMI 12' Kabler.</span><span class="sxs-lookup"><span data-stu-id="c66b5-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="c66b5-132">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c66b5-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="c66b5-133">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="c66b5-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="c66b5-134">Angi eller velg en verdi i feltet Konfigurasjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c66b5-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="c66b5-135">Velg konfigurasjonsgruppen Kabel.</span><span class="sxs-lookup"><span data-stu-id="c66b5-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="c66b5-136">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c66b5-136">Click New.</span></span>
14. <span data-ttu-id="c66b5-137">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c66b5-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="c66b5-138">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="c66b5-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="c66b5-139">Velge varenummer D0002 Kabinett.</span><span class="sxs-lookup"><span data-stu-id="c66b5-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="c66b5-140">Angi eller velg en verdi i feltet Konfigurasjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c66b5-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="c66b5-141">Velg konfigurasjonsgruppen Kabinett for denne stykklistelinjen.</span><span class="sxs-lookup"><span data-stu-id="c66b5-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="c66b5-142">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c66b5-142">Click New.</span></span>
18. <span data-ttu-id="c66b5-143">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c66b5-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="c66b5-144">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="c66b5-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="c66b5-145">Velg varenummer M0007 StandardCabinet som siste stykklistelinje.</span><span class="sxs-lookup"><span data-stu-id="c66b5-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="c66b5-146">Angi eller velg en verdi i feltet Konfigurasjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c66b5-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="c66b5-147">Velg konfigurasjonsgruppen Kabinett for den siste stykklistelinjen.</span><span class="sxs-lookup"><span data-stu-id="c66b5-147">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="c66b5-148">Godkjenn og aktiver</span><span class="sxs-lookup"><span data-stu-id="c66b5-148">Approve and activate</span></span>
1. <span data-ttu-id="c66b5-149">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c66b5-149">Close the page.</span></span>
2. <span data-ttu-id="c66b5-150">Klikk Godkjenn.</span><span class="sxs-lookup"><span data-stu-id="c66b5-150">Click Approve.</span></span>
3. <span data-ttu-id="c66b5-151">Angi eller velg en verdi i feltet Godkjent av.</span><span class="sxs-lookup"><span data-stu-id="c66b5-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="c66b5-152">Velg Ja i Vil du også godkjenne stykklisten? .</span><span class="sxs-lookup"><span data-stu-id="c66b5-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="c66b5-153">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c66b5-153">Click OK.</span></span>
6. <span data-ttu-id="c66b5-154">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="c66b5-154">Click Activate.</span></span>


