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
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 296b3fb03b20dee5b6024c182df7feb3ce280913
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964676"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="fa508-103"> Opprette produktpakker for bestillinger</span><span class="sxs-lookup"><span data-stu-id="fa508-103">Create product packages for purchase orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa508-104">Denne prosedyren hjelper med å opprette en produktpakke og bruke den i en bestilling.</span><span class="sxs-lookup"><span data-stu-id="fa508-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="fa508-105">Bestillingen skal brukes til å opprette en ordre for et forhåndsdefinert sett med produkter.</span><span class="sxs-lookup"><span data-stu-id="fa508-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="fa508-106">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="fa508-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="fa508-107">Opprette en produktpakke</span><span class="sxs-lookup"><span data-stu-id="fa508-107">Create a product package</span></span>
1. <span data-ttu-id="fa508-108">Gå til Detaljhandel og handel > Lagerstyring > Etterfylling > Produktpakker.</span><span class="sxs-lookup"><span data-stu-id="fa508-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="fa508-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="fa508-109">Click New.</span></span>
3. <span data-ttu-id="fa508-110">Skriv inn en verdi i feltet Pakkenummer.</span><span class="sxs-lookup"><span data-stu-id="fa508-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="fa508-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="fa508-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fa508-112">Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fa508-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="fa508-113">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fa508-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="fa508-114">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="fa508-114">Click Add.</span></span>
8. <span data-ttu-id="fa508-115">Skriv inn 0160 i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="fa508-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="fa508-116">Klikk rullegardinknappen i Størrelse-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fa508-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="fa508-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fa508-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="fa508-118">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="fa508-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="fa508-119">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="fa508-119">Click Add.</span></span>
13. <span data-ttu-id="fa508-120">Skriv inn 0160 i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="fa508-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="fa508-121">Klikk rullegardinknappen i feltet Variantnummer for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fa508-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="fa508-122">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fa508-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="fa508-123">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="fa508-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="fa508-124">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="fa508-124">Click Add.</span></span>
18. <span data-ttu-id="fa508-125">Skriv inn 0175 i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="fa508-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="fa508-126">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="fa508-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="fa508-127">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fa508-127">Click Save.</span></span>
21. <span data-ttu-id="fa508-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fa508-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="fa508-129">Legge til pakken i bestillingen</span><span class="sxs-lookup"><span data-stu-id="fa508-129">Add package to purchase order</span></span>
1. <span data-ttu-id="fa508-130">Gå til Leverandører > Bestillinger > Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="fa508-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="fa508-131">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="fa508-131">Click New.</span></span>
3. <span data-ttu-id="fa508-132">Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fa508-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="fa508-133">Velg den samme leverandøren som produktpakken ble opprettet for tidligere, i listen, hvis du valgte en leverandør.</span><span class="sxs-lookup"><span data-stu-id="fa508-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="fa508-134">Aktiver/deaktiver utvidelsen av delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="fa508-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="fa508-135">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fa508-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="fa508-136">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fa508-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="fa508-137">Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fa508-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="fa508-138">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fa508-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="fa508-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="fa508-139">Click OK.</span></span>
11. <span data-ttu-id="fa508-140">Aktiver/deaktiver utvidelsen av delen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="fa508-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="fa508-141">Klikk kategorien Produktpakker.</span><span class="sxs-lookup"><span data-stu-id="fa508-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="fa508-142">Klikk Bestillingslinje.</span><span class="sxs-lookup"><span data-stu-id="fa508-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="fa508-143">Klikk Opprett linjer fra pakke.</span><span class="sxs-lookup"><span data-stu-id="fa508-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="fa508-144">Finn og velg produktpakken som ble opprettet i forrige trinn, i listen.</span><span class="sxs-lookup"><span data-stu-id="fa508-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="fa508-145">Angi et tall i Antall-feltet.</span><span class="sxs-lookup"><span data-stu-id="fa508-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="fa508-146">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="fa508-146">Click Create.</span></span>
18. <span data-ttu-id="fa508-147">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fa508-147">Click Save.</span></span>

