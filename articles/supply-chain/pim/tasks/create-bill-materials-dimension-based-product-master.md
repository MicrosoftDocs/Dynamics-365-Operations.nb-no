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
ms.openlocfilehash: 13053dd87242963586678b46c64493feb3383c4c
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920711"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="59542-103">Opprette en stykkliste for en dimensjonsbasert produktstandard</span><span class="sxs-lookup"><span data-stu-id="59542-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="59542-104">For denne prosedyren skal du har fullført de 4 forrige veiledningene i disse trinnene med åtte registreringer.</span><span class="sxs-lookup"><span data-stu-id="59542-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="59542-105">De 4 første registreringene definerer dataene som kreves for å fullføre denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="59542-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="59542-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="59542-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="59542-107">Denne oppgaven håndteres vanligvis av produktdesigneren.</span><span class="sxs-lookup"><span data-stu-id="59542-107">This task is typically handled by the product designer.</span></span>

## <a name="select-the-product"></a><span data-ttu-id="59542-108">Velg produkt</span><span class="sxs-lookup"><span data-stu-id="59542-108">Select the product</span></span>

1. <span data-ttu-id="59542-109">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="59542-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="59542-110">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="59542-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="59542-111">Finn den frigitte produktstandarden med dimensjonsbasert konfigurasjonsteknologi, som du opprettet i den første oppgaveveiledningen i disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="59542-111">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
1. <span data-ttu-id="59542-112">Velg **Utvikle** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="59542-112">On the Action Pane, select **Engineer**.</span></span>
1. <span data-ttu-id="59542-113">Velg **BOM-versjoner**.</span><span class="sxs-lookup"><span data-stu-id="59542-113">Select **BOM versions**.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="59542-114">Opprette ny stykkliste og stykklisteversjon</span><span class="sxs-lookup"><span data-stu-id="59542-114">Create new BOM and BOM version</span></span>

1. <span data-ttu-id="59542-115">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="59542-115">Select **New**.</span></span>
1. <span data-ttu-id="59542-116">Velg **Stykkliste og stykklisteversjon**.</span><span class="sxs-lookup"><span data-stu-id="59542-116">Select **BOM and BOM version**.</span></span>
1. <span data-ttu-id="59542-117">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="59542-117">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="59542-118">Angi et område</span><span class="sxs-lookup"><span data-stu-id="59542-118">Setting a site</span></span>  
    * <span data-ttu-id="59542-119">Vi angir ikke et bestemt område for stykklisten i denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="59542-119">In this procedure we don't set a specific site for the BOM.</span></span>  
1. <span data-ttu-id="59542-120">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="59542-120">Select **OK**.</span></span>
1. <span data-ttu-id="59542-121">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="59542-121">Select **New**.</span></span>
    * <span data-ttu-id="59542-122">I denne fremgangsmåten skal vi legge til fire linjer i stykklisten.</span><span class="sxs-lookup"><span data-stu-id="59542-122">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="59542-123">To linjer representerer kabelalternativer og to linjer representerer kabinettalternativer.</span><span class="sxs-lookup"><span data-stu-id="59542-123">Two lines represent cable options and two lines represent cabinet options.</span></span>  
1. <span data-ttu-id="59542-124">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="59542-124">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="59542-125">Angi eller velg en verdi i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="59542-125">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="59542-126">Velge varenummer A0001, HDMI 6' Kabler.</span><span class="sxs-lookup"><span data-stu-id="59542-126">Select item number A0001, HDMI 6' Cables.</span></span>  
1. <span data-ttu-id="59542-127">Angi eller velg en verdi i feltet **Konfigurasjonsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="59542-127">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="59542-128">Velg konfigurasjonsgruppen Kabel, som ble opprettet i veiledning 4 i disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="59542-128">Select the cable configuration group created in guide 4 in this sequence.</span></span>  
1. <span data-ttu-id="59542-129">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="59542-129">Select **New**.</span></span>
    * <span data-ttu-id="59542-130">Velge varenummer A0002, HDMI 12' Kabler.</span><span class="sxs-lookup"><span data-stu-id="59542-130">Select item number A0002, HDMI 12' Cables.</span></span>  
1. <span data-ttu-id="59542-131">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="59542-131">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="59542-132">Angi eller velg en verdi i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="59542-132">In the **Item number** field, enter or select a value.</span></span>
1. <span data-ttu-id="59542-133">Angi eller velg en verdi i feltet **Konfigurasjonsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="59542-133">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="59542-134">Velg konfigurasjonsgruppen Kabel på nytt.</span><span class="sxs-lookup"><span data-stu-id="59542-134">Select the cable configuration group again.</span></span>  
1. <span data-ttu-id="59542-135">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="59542-135">Select **New**.</span></span>
1. <span data-ttu-id="59542-136">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="59542-136">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="59542-137">Angi eller velg en verdi i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="59542-137">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="59542-138">Velge varenummer D0002 Kabinett.</span><span class="sxs-lookup"><span data-stu-id="59542-138">Select item number D0002 Cabinet.</span></span>  
1. <span data-ttu-id="59542-139">Angi eller velg en verdi i feltet **Konfigurasjonsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="59542-139">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="59542-140">Velg konfigurasjonsgruppen Kabinett for denne stykklistelinjen.</span><span class="sxs-lookup"><span data-stu-id="59542-140">Select the cabinet configuration group for this BOM line.</span></span>  
1. <span data-ttu-id="59542-141">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="59542-141">Select **New**.</span></span>
1. <span data-ttu-id="59542-142">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="59542-142">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="59542-143">Angi eller velg en verdi i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="59542-143">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="59542-144">Velg varenummer M0007 StandardCabinet som siste stykklistelinje.</span><span class="sxs-lookup"><span data-stu-id="59542-144">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
1. <span data-ttu-id="59542-145">Angi eller velg en verdi i feltet **Konfigurasjonsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="59542-145">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="59542-146">Velg konfigurasjonsgruppen Kabinett for den siste stykklistelinjen.</span><span class="sxs-lookup"><span data-stu-id="59542-146">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="59542-147">Godkjenn og aktiver</span><span class="sxs-lookup"><span data-stu-id="59542-147">Approve and activate</span></span>

1. <span data-ttu-id="59542-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="59542-148">Close the page.</span></span>
1. <span data-ttu-id="59542-149">Velg **Godkjenn**.</span><span class="sxs-lookup"><span data-stu-id="59542-149">Select **Approve**.</span></span>
1. <span data-ttu-id="59542-150">Angi eller velg en verdi i feltet **Godkjent av**.</span><span class="sxs-lookup"><span data-stu-id="59542-150">In the **Approved by** field, enter or select a value.</span></span>
1. <span data-ttu-id="59542-151">Velg *Ja* i feltet **Vil du også godkjenne stykklisten?**.</span><span class="sxs-lookup"><span data-stu-id="59542-151">Select *Yes* in the **Do you also want to approve the bill of materials?** field.</span></span>
1. <span data-ttu-id="59542-152">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="59542-152">Select **OK**.</span></span>
1. <span data-ttu-id="59542-153">Velg **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="59542-153">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]