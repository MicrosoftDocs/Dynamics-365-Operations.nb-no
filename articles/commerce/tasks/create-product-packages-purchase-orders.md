---
title: " Opprette produktpakker for bestillinger"
description: Denne prosedyren hjelper med å opprette en produktpakke og bruke den i en bestilling.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b0084c6b4acbf14e3afec552575d5be26114237
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141374"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="5a127-103"> Opprette produktpakker for bestillinger</span><span class="sxs-lookup"><span data-stu-id="5a127-103">Create product packages for purchase orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a127-104">Denne prosedyren hjelper med å opprette en produktpakke og bruke den i en bestilling.</span><span class="sxs-lookup"><span data-stu-id="5a127-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="5a127-105">Bestillingen skal brukes til å opprette en ordre for et forhåndsdefinert sett med produkter.</span><span class="sxs-lookup"><span data-stu-id="5a127-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="5a127-106">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="5a127-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="5a127-107">Opprette en produktpakke</span><span class="sxs-lookup"><span data-stu-id="5a127-107">Create a product package</span></span>
1. <span data-ttu-id="5a127-108">Gå til Detaljhandel og handel > Lagerstyring > Etterfylling > Produktpakker.</span><span class="sxs-lookup"><span data-stu-id="5a127-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="5a127-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5a127-109">Click New.</span></span>
3. <span data-ttu-id="5a127-110">Skriv inn en verdi i feltet Pakkenummer.</span><span class="sxs-lookup"><span data-stu-id="5a127-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="5a127-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="5a127-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5a127-112">Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5a127-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5a127-113">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5a127-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="5a127-114">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="5a127-114">Click Add.</span></span>
8. <span data-ttu-id="5a127-115">Skriv inn 0160 i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="5a127-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="5a127-116">Klikk rullegardinknappen i Størrelse-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5a127-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="5a127-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5a127-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="5a127-118">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="5a127-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="5a127-119">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="5a127-119">Click Add.</span></span>
13. <span data-ttu-id="5a127-120">Skriv inn 0160 i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="5a127-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="5a127-121">Klikk rullegardinknappen i feltet Variantnummer for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5a127-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="5a127-122">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5a127-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="5a127-123">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="5a127-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="5a127-124">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="5a127-124">Click Add.</span></span>
18. <span data-ttu-id="5a127-125">Skriv inn 0175 i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="5a127-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="5a127-126">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="5a127-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="5a127-127">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5a127-127">Click Save.</span></span>
21. <span data-ttu-id="5a127-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5a127-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="5a127-129">Legge til pakken i bestillingen</span><span class="sxs-lookup"><span data-stu-id="5a127-129">Add package to purchase order</span></span>
1. <span data-ttu-id="5a127-130">Gå til Leverandører > Bestillinger > Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="5a127-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="5a127-131">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5a127-131">Click New.</span></span>
3. <span data-ttu-id="5a127-132">Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5a127-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5a127-133">Velg den samme leverandøren som produktpakken ble opprettet for tidligere, i listen, hvis du valgte en leverandør.</span><span class="sxs-lookup"><span data-stu-id="5a127-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="5a127-134">Aktiver/deaktiver utvidelsen av delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="5a127-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="5a127-135">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5a127-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="5a127-136">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5a127-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="5a127-137">Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5a127-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="5a127-138">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5a127-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="5a127-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5a127-139">Click OK.</span></span>
11. <span data-ttu-id="5a127-140">Aktiver/deaktiver utvidelsen av delen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="5a127-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="5a127-141">Klikk kategorien Produktpakker.</span><span class="sxs-lookup"><span data-stu-id="5a127-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="5a127-142">Klikk Bestillingslinje.</span><span class="sxs-lookup"><span data-stu-id="5a127-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="5a127-143">Klikk Opprett linjer fra pakke.</span><span class="sxs-lookup"><span data-stu-id="5a127-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="5a127-144">Finn og velg produktpakken som ble opprettet i forrige trinn, i listen.</span><span class="sxs-lookup"><span data-stu-id="5a127-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="5a127-145">Angi et tall i Antall-feltet.</span><span class="sxs-lookup"><span data-stu-id="5a127-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="5a127-146">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="5a127-146">Click Create.</span></span>
18. <span data-ttu-id="5a127-147">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5a127-147">Click Save.</span></span>

