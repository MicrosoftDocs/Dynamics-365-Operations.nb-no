--- 
title: " Opprette produktpakker for bestillinger"
description: "Denne prosedyren hjelper med å opprette en produktpakke og bruke den i en bestilling."
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d03deb17ca546c15e6c12733e52b19e250d10bfa
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="eeabe-103"> Opprette produktpakker for bestillinger</span><span class="sxs-lookup"><span data-stu-id="eeabe-103">Create product packages for purchase orders</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="eeabe-104">Denne prosedyren hjelper med å opprette en produktpakke og bruke den i en bestilling.</span><span class="sxs-lookup"><span data-stu-id="eeabe-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="eeabe-105">Bestillingen skal brukes til å opprette en ordre for et forhåndsdefinert sett med produkter.</span><span class="sxs-lookup"><span data-stu-id="eeabe-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="eeabe-106">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="eeabe-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="eeabe-107">Opprette en produktpakke</span><span class="sxs-lookup"><span data-stu-id="eeabe-107">Create a product package</span></span>
1. <span data-ttu-id="eeabe-108">Gå til Detaljhandel og handel > Lagerstyring > Etterfylling > Produktpakker.</span><span class="sxs-lookup"><span data-stu-id="eeabe-108">Go to Retail and commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="eeabe-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="eeabe-109">Click New.</span></span>
3. <span data-ttu-id="eeabe-110">Skriv inn en verdi i feltet Pakkenummer.</span><span class="sxs-lookup"><span data-stu-id="eeabe-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="eeabe-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="eeabe-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="eeabe-112">Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="eeabe-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="eeabe-113">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="eeabe-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="eeabe-114">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="eeabe-114">Click Add.</span></span>
8. <span data-ttu-id="eeabe-115">Skriv inn 0160 i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="eeabe-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="eeabe-116">Klikk rullegardinknappen i Størrelse-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="eeabe-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="eeabe-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="eeabe-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="eeabe-118">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="eeabe-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="eeabe-119">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="eeabe-119">Click Add.</span></span>
13. <span data-ttu-id="eeabe-120">Skriv inn 0160 i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="eeabe-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="eeabe-121">Klikk rullegardinknappen i feltet Variantnummer for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="eeabe-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="eeabe-122">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="eeabe-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="eeabe-123">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="eeabe-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="eeabe-124">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="eeabe-124">Click Add.</span></span>
18. <span data-ttu-id="eeabe-125">Skriv inn 0175 i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="eeabe-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="eeabe-126">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="eeabe-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="eeabe-127">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="eeabe-127">Click Save.</span></span>
21. <span data-ttu-id="eeabe-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="eeabe-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="eeabe-129">Legge til pakken i bestillingen</span><span class="sxs-lookup"><span data-stu-id="eeabe-129">Add package to purchase order</span></span>
1. <span data-ttu-id="eeabe-130">Gå til Leverandører > Bestillinger > Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="eeabe-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="eeabe-131">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="eeabe-131">Click New.</span></span>
3. <span data-ttu-id="eeabe-132">Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="eeabe-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="eeabe-133">Velg den samme leverandøren som produktpakken ble opprettet for tidligere, i listen, hvis du valgte en leverandør.</span><span class="sxs-lookup"><span data-stu-id="eeabe-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="eeabe-134">Aktiver/deaktiver utvidelsen av delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="eeabe-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="eeabe-135">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="eeabe-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="eeabe-136">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="eeabe-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="eeabe-137">Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="eeabe-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="eeabe-138">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="eeabe-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="eeabe-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="eeabe-139">Click OK.</span></span>
11. <span data-ttu-id="eeabe-140">Aktiver/deaktiver utvidelsen av delen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="eeabe-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="eeabe-141">Klikk kategorien Produktpakker.</span><span class="sxs-lookup"><span data-stu-id="eeabe-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="eeabe-142">Klikk Bestillingslinje.</span><span class="sxs-lookup"><span data-stu-id="eeabe-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="eeabe-143">Klikk Opprett linjer fra pakke.</span><span class="sxs-lookup"><span data-stu-id="eeabe-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="eeabe-144">Finn og velg produktpakken som ble opprettet i forrige trinn, i listen.</span><span class="sxs-lookup"><span data-stu-id="eeabe-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="eeabe-145">Angi et tall i Antall-feltet.</span><span class="sxs-lookup"><span data-stu-id="eeabe-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="eeabe-146">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="eeabe-146">Click Create.</span></span>
18. <span data-ttu-id="eeabe-147">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="eeabe-147">Click Save.</span></span>


