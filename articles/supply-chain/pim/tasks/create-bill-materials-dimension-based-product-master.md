---
title: Opprette en stykkliste for en dimensjonsbasert produktstandard
description: For denne prosedyren skal du har fullført de 4 forrige veiledningene i disse trinnene med åtte registreringer.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 677aacb72d1c3f33bed8bb6c9cd32e5dbca677cc
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844927"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="539f6-103">Opprette en stykkliste for en dimensjonsbasert produktstandard</span><span class="sxs-lookup"><span data-stu-id="539f6-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="539f6-104">For denne prosedyren skal du har fullført de 4 forrige veiledningene i disse trinnene med åtte registreringer.</span><span class="sxs-lookup"><span data-stu-id="539f6-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="539f6-105">De 4 første registreringene definerer dataene som kreves for å fullføre denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="539f6-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="539f6-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="539f6-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="539f6-107">Denne oppgaven håndteres vanligvis av produktdesigneren.</span><span class="sxs-lookup"><span data-stu-id="539f6-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="539f6-108">Velg produkt</span><span class="sxs-lookup"><span data-stu-id="539f6-108">Select the product</span></span>
1. <span data-ttu-id="539f6-109">Klikk Vedlikehold av frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="539f6-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="539f6-110">Klikk Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="539f6-110">Click Released products.</span></span>
3. <span data-ttu-id="539f6-111">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="539f6-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="539f6-112">Finn den frigitte produktstandarden med dimensjonsbasert konfigurasjonsteknologi, som du opprettet i den første oppgaveveiledningen i disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="539f6-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="539f6-113">Klikk Utvikling i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="539f6-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="539f6-114">Klikk Stykklisteversjon.</span><span class="sxs-lookup"><span data-stu-id="539f6-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="539f6-115">Opprette ny stykkliste og stykklisteversjon</span><span class="sxs-lookup"><span data-stu-id="539f6-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="539f6-116">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="539f6-116">Click New.</span></span>
2. <span data-ttu-id="539f6-117">Klikk Stykkliste og stykklisteversjon.</span><span class="sxs-lookup"><span data-stu-id="539f6-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="539f6-118">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="539f6-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="539f6-119">Angi et område</span><span class="sxs-lookup"><span data-stu-id="539f6-119">Setting a site</span></span>  
    * <span data-ttu-id="539f6-120">Vi angir ikke et bestemt område for stykklisten i denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="539f6-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="539f6-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="539f6-121">Click OK.</span></span>
5. <span data-ttu-id="539f6-122">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="539f6-122">Click New.</span></span>
    * <span data-ttu-id="539f6-123">I denne fremgangsmåten skal vi legge til fire linjer i stykklisten.</span><span class="sxs-lookup"><span data-stu-id="539f6-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="539f6-124">To linjer representerer kabelalternativer og to linjer representerer kabinettalternativer.</span><span class="sxs-lookup"><span data-stu-id="539f6-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="539f6-125">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="539f6-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="539f6-126">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="539f6-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="539f6-127">Velge varenummer A0001, HDMI 6' Kabler.</span><span class="sxs-lookup"><span data-stu-id="539f6-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="539f6-128">Angi eller velg en verdi i feltet Konfigurasjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="539f6-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="539f6-129">Velg konfigurasjonsgruppen Kabel, som ble opprettet i veiledning 4 i disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="539f6-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="539f6-130">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="539f6-130">Click New.</span></span>
    * <span data-ttu-id="539f6-131">Velge varenummer A0002, HDMI 12' Kabler.</span><span class="sxs-lookup"><span data-stu-id="539f6-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="539f6-132">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="539f6-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="539f6-133">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="539f6-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="539f6-134">Angi eller velg en verdi i feltet Konfigurasjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="539f6-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="539f6-135">Velg konfigurasjonsgruppen Kabel.</span><span class="sxs-lookup"><span data-stu-id="539f6-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="539f6-136">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="539f6-136">Click New.</span></span>
14. <span data-ttu-id="539f6-137">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="539f6-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="539f6-138">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="539f6-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="539f6-139">Velge varenummer D0002 Kabinett.</span><span class="sxs-lookup"><span data-stu-id="539f6-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="539f6-140">Angi eller velg en verdi i feltet Konfigurasjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="539f6-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="539f6-141">Velg konfigurasjonsgruppen Kabinett for denne stykklistelinjen.</span><span class="sxs-lookup"><span data-stu-id="539f6-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="539f6-142">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="539f6-142">Click New.</span></span>
18. <span data-ttu-id="539f6-143">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="539f6-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="539f6-144">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="539f6-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="539f6-145">Velg varenummer M0007 StandardCabinet som siste stykklistelinje.</span><span class="sxs-lookup"><span data-stu-id="539f6-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="539f6-146">Angi eller velg en verdi i feltet Konfigurasjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="539f6-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="539f6-147">Velg konfigurasjonsgruppen Kabinett for den siste stykklistelinjen.</span><span class="sxs-lookup"><span data-stu-id="539f6-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="539f6-148">Godkjenn og aktiver</span><span class="sxs-lookup"><span data-stu-id="539f6-148">Approve and activate</span></span>
1. <span data-ttu-id="539f6-149">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="539f6-149">Close the page.</span></span>
2. <span data-ttu-id="539f6-150">Klikk Godkjenn.</span><span class="sxs-lookup"><span data-stu-id="539f6-150">Click Approve.</span></span>
3. <span data-ttu-id="539f6-151">Angi eller velg en verdi i feltet Godkjent av.</span><span class="sxs-lookup"><span data-stu-id="539f6-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="539f6-152">Velg Ja i Vil du også godkjenne stykklisten? .</span><span class="sxs-lookup"><span data-stu-id="539f6-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="539f6-153">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="539f6-153">Click OK.</span></span>
6. <span data-ttu-id="539f6-154">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="539f6-154">Click Activate.</span></span>

