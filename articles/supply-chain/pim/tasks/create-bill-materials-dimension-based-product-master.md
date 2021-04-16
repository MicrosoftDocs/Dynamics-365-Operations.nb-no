---
title: Opprette en stykkliste for en dimensjonsbasert produktstandard
description: For denne prosedyren skal du har fullført de 4 forrige veiledningene i disse trinnene med åtte registreringer.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0db1c35779a468d9a86d18eb6c849d40bc8c03a3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820088"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="f2f65-103">Opprette en stykkliste for en dimensjonsbasert produktstandard</span><span class="sxs-lookup"><span data-stu-id="f2f65-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2f65-104">For denne prosedyren skal du har fullført de 4 forrige veiledningene i disse trinnene med åtte registreringer.</span><span class="sxs-lookup"><span data-stu-id="f2f65-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="f2f65-105">De 4 første registreringene definerer dataene som kreves for å fullføre denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="f2f65-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="f2f65-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="f2f65-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f2f65-107">Denne oppgaven håndteres vanligvis av produktdesigneren.</span><span class="sxs-lookup"><span data-stu-id="f2f65-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="f2f65-108">Velg produkt</span><span class="sxs-lookup"><span data-stu-id="f2f65-108">Select the product</span></span>
1. <span data-ttu-id="f2f65-109">Klikk på Vedlikehold av frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="f2f65-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="f2f65-110">Klikk på Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="f2f65-110">Click Released products.</span></span>
3. <span data-ttu-id="f2f65-111">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f2f65-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f2f65-112">Finn den frigitte produktstandarden med dimensjonsbasert konfigurasjonsteknologi, som du opprettet i den første oppgaveveiledningen i disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="f2f65-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="f2f65-113">Klikk på Utvikling i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f2f65-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="f2f65-114">Klikk på Stykklisteversjon.</span><span class="sxs-lookup"><span data-stu-id="f2f65-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="f2f65-115">Opprette ny stykkliste og stykklisteversjon</span><span class="sxs-lookup"><span data-stu-id="f2f65-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="f2f65-116">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="f2f65-116">Click New.</span></span>
2. <span data-ttu-id="f2f65-117">Klikk på Stykkliste og stykklisteversjon.</span><span class="sxs-lookup"><span data-stu-id="f2f65-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="f2f65-118">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f2f65-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f2f65-119">Angi et område</span><span class="sxs-lookup"><span data-stu-id="f2f65-119">Setting a site</span></span>  
    * <span data-ttu-id="f2f65-120">Vi angir ikke et bestemt område for stykklisten i denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="f2f65-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="f2f65-121">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="f2f65-121">Click OK.</span></span>
5. <span data-ttu-id="f2f65-122">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="f2f65-122">Click New.</span></span>
    * <span data-ttu-id="f2f65-123">I denne fremgangsmåten skal vi legge til fire linjer i stykklisten.</span><span class="sxs-lookup"><span data-stu-id="f2f65-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="f2f65-124">To linjer representerer kabelalternativer og to linjer representerer kabinettalternativer.</span><span class="sxs-lookup"><span data-stu-id="f2f65-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="f2f65-125">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f2f65-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="f2f65-126">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="f2f65-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="f2f65-127">Velge varenummer A0001, HDMI 6' Kabler.</span><span class="sxs-lookup"><span data-stu-id="f2f65-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="f2f65-128">Angi eller velg en verdi i feltet Konfigurasjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f2f65-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="f2f65-129">Velg konfigurasjonsgruppen Kabel, som ble opprettet i veiledning 4 i disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="f2f65-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="f2f65-130">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="f2f65-130">Click New.</span></span>
    * <span data-ttu-id="f2f65-131">Velge varenummer A0002, HDMI 12' Kabler.</span><span class="sxs-lookup"><span data-stu-id="f2f65-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="f2f65-132">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f2f65-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="f2f65-133">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="f2f65-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="f2f65-134">Angi eller velg en verdi i feltet Konfigurasjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f2f65-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="f2f65-135">Velg konfigurasjonsgruppen Kabel.</span><span class="sxs-lookup"><span data-stu-id="f2f65-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="f2f65-136">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="f2f65-136">Click New.</span></span>
14. <span data-ttu-id="f2f65-137">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f2f65-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="f2f65-138">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="f2f65-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="f2f65-139">Velge varenummer D0002 Kabinett.</span><span class="sxs-lookup"><span data-stu-id="f2f65-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="f2f65-140">Angi eller velg en verdi i feltet Konfigurasjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f2f65-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="f2f65-141">Velg konfigurasjonsgruppen Kabinett for denne stykklistelinjen.</span><span class="sxs-lookup"><span data-stu-id="f2f65-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="f2f65-142">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="f2f65-142">Click New.</span></span>
18. <span data-ttu-id="f2f65-143">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f2f65-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="f2f65-144">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="f2f65-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="f2f65-145">Velg varenummer M0007 StandardCabinet som siste stykklistelinje.</span><span class="sxs-lookup"><span data-stu-id="f2f65-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="f2f65-146">Angi eller velg en verdi i feltet Konfigurasjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f2f65-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="f2f65-147">Velg konfigurasjonsgruppen Kabinett for den siste stykklistelinjen.</span><span class="sxs-lookup"><span data-stu-id="f2f65-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="f2f65-148">Godkjenn og aktiver</span><span class="sxs-lookup"><span data-stu-id="f2f65-148">Approve and activate</span></span>
1. <span data-ttu-id="f2f65-149">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f2f65-149">Close the page.</span></span>
2. <span data-ttu-id="f2f65-150">Klikk på Godkjenn.</span><span class="sxs-lookup"><span data-stu-id="f2f65-150">Click Approve.</span></span>
3. <span data-ttu-id="f2f65-151">Angi eller velg en verdi i feltet Godkjent av.</span><span class="sxs-lookup"><span data-stu-id="f2f65-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="f2f65-152">Velg Ja i Vil du også godkjenne stykklisten? .</span><span class="sxs-lookup"><span data-stu-id="f2f65-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="f2f65-153">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="f2f65-153">Click OK.</span></span>
6. <span data-ttu-id="f2f65-154">Klikk på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="f2f65-154">Click Activate.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]