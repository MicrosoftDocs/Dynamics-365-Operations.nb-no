---
title: " Basispris og forretningsavtaler"
description: Denne prosedyren hjelper med å opprette kanalspesifikke salgsprisforretningsavtaler.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7576c4218118724562ff739ff9805a06b7ba22d5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023556"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="29b01-103"> Basispris og forretningsavtaler</span><span class="sxs-lookup"><span data-stu-id="29b01-103">Base price and trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="29b01-104">Denne prosedyren hjelper med å opprette kanalspesifikke salgsprisforretningsavtaler.</span><span class="sxs-lookup"><span data-stu-id="29b01-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="29b01-105">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="29b01-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="29b01-106">I **navigasjonsruten** går du til **Moduler > Retail og Commerce > Prissetting og rabattstyring > Prisgrupper > Alle prisgrupper**.</span><span class="sxs-lookup"><span data-stu-id="29b01-106">In the **Navigation pane**, go to **Modules > Retail and Commerce > Pricing and discounts management > Price groups > All price groups**.</span></span> <span data-ttu-id="29b01-107">Prisgrupper er måten forretningsavtaler tilordnes til bestemte kanaler på.</span><span class="sxs-lookup"><span data-stu-id="29b01-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="29b01-108">Kanalspesifikke priser blir mulig ved å bruke prisgrupper for å tilordne forretningsavtaler til en kanal.</span><span class="sxs-lookup"><span data-stu-id="29b01-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="29b01-109">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="29b01-109">Click **New**.</span></span>
3. <span data-ttu-id="29b01-110">Skriv inn en verdi i feltet **Prisgrupper**.</span><span class="sxs-lookup"><span data-stu-id="29b01-110">In the **Price groups** field, type a value.</span></span>
4. <span data-ttu-id="29b01-111">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="29b01-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="29b01-112">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="29b01-112">Click **Save**.</span></span>
6. <span data-ttu-id="29b01-113">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="29b01-113">Close the page.</span></span>
7. <span data-ttu-id="29b01-114">I **navigasjonsruten** går du til **Moduler > Retail og Commerce > Kanaler > Butikker > Alle butikker**.</span><span class="sxs-lookup"><span data-stu-id="29b01-114">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
8. <span data-ttu-id="29b01-115">Velg New York i listen.</span><span class="sxs-lookup"><span data-stu-id="29b01-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="29b01-116">Klikk **Butikk** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="29b01-116">On the Action Pane, click **Store**.</span></span>
10. <span data-ttu-id="29b01-117">Klikk **Prisgrupper**.</span><span class="sxs-lookup"><span data-stu-id="29b01-117">Click **Price groups**.</span></span>
11. <span data-ttu-id="29b01-118">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="29b01-118">Click **New**.</span></span>
12. <span data-ttu-id="29b01-119">Klikk rullegardinknappen i **Prisgrupper**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="29b01-119">In the **Price groups** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="29b01-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="29b01-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="29b01-121">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="29b01-121">Click **Save**.</span></span>
15. <span data-ttu-id="29b01-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="29b01-122">Close the page.</span></span>
16. <span data-ttu-id="29b01-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="29b01-123">Close the page.</span></span>
17. <span data-ttu-id="29b01-124">I **navigasjonsruten** går du til **Moduler > Retail og Commerce > Produkter og kategorier > Frigitte produkter etter kategori**.</span><span class="sxs-lookup"><span data-stu-id="29b01-124">In the **Navigation pane**, go to **Modules > Retail and Commerce > Products and categories > Released products by category**.</span></span>
18. <span data-ttu-id="29b01-125">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="29b01-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="29b01-126">Klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="29b01-126">Click **Edit**.</span></span>
20. <span data-ttu-id="29b01-127">Utvid **Selg**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="29b01-127">Expand the **Sell** fastTab.</span></span>
21. <span data-ttu-id="29b01-128">Angi et tall i **Pris**-feltet</span><span class="sxs-lookup"><span data-stu-id="29b01-128">In the **Price** field, enter a number.</span></span> <span data-ttu-id="29b01-129">Denne prisen brukes hvis det ikke blir funnet en gjeldende forretningsavtale.</span><span class="sxs-lookup"><span data-stu-id="29b01-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="29b01-130">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="29b01-130">Click **Save**.</span></span>
23. <span data-ttu-id="29b01-131">I **Handlingsrute** klikker du på **Selg**.</span><span class="sxs-lookup"><span data-stu-id="29b01-131">On the **Action Pane**, click **Sell**.</span></span>
24. <span data-ttu-id="29b01-132">Klikk **Opprett forretningsavtaler**.</span><span class="sxs-lookup"><span data-stu-id="29b01-132">Click **Create trade agreements**.</span></span>
25. <span data-ttu-id="29b01-133">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="29b01-133">Click **New**.</span></span>
26. <span data-ttu-id="29b01-134">Klikk på rullegardinknappen i **Navn**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="29b01-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="29b01-135">Velg **Commerce** i listen.</span><span class="sxs-lookup"><span data-stu-id="29b01-135">In the list, select **Commerce**.</span></span> <span data-ttu-id="29b01-136">I demonstrasjonsdataene har journalnavnet **Commerce** standardrelasjonen **Pris (salg)**.</span><span class="sxs-lookup"><span data-stu-id="29b01-136">In the demo data, the **Commerce** journal name has the default relation of **Price (sales)**.</span></span> <span data-ttu-id="29b01-137">Det betyr at alle nye linjer som opprettes, bruker salgsprisforretningsavtaler som standard.</span><span class="sxs-lookup"><span data-stu-id="29b01-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="29b01-138">Klikk på **Linjer** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="29b01-138">On the **Action pane**, click **Lines**.</span></span>
29. <span data-ttu-id="29b01-139">Velg Gruppe i **Kontokode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="29b01-139">In the **Account code** field, select 'Group'.</span></span>
30. <span data-ttu-id="29b01-140">Klikk på rullegardinknappen i **Kontovalg**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="29b01-140">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="29b01-141">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="29b01-141">In the list, find and select the desired record.</span></span> <span data-ttu-id="29b01-142">Dette fullfører koblingen fra kanal til prisgruppe til forretningsavtale.</span><span class="sxs-lookup"><span data-stu-id="29b01-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="29b01-143">Skriv inn en verdi i **Varerelasjon**-feltet.</span><span class="sxs-lookup"><span data-stu-id="29b01-143">In the **Item relation** field, type a value.</span></span>
33. <span data-ttu-id="29b01-144">Angi en verdi i feltet **Beløp i valuta**.</span><span class="sxs-lookup"><span data-stu-id="29b01-144">In the **Amount in currency** field, enter a number.</span></span>
34. <span data-ttu-id="29b01-145">Merk av eller fjern merket for **Søk etter neste** i hurtigfanen **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="29b01-145">In the **Details** fastTab, check or uncheck the **Find next** checkbox.</span></span> <span data-ttu-id="29b01-146">Når **Søk etter neste** settes til Ja, fortsetter prissettingsmotoren å søke etter gjeldende forretningsavtaler med en lavere salgspris.</span><span class="sxs-lookup"><span data-stu-id="29b01-146">When **Find next** is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="29b01-147">Når **Søk etter neste** settes til Nei, slutter motoren å søke og bruker forretningsavtalen.</span><span class="sxs-lookup"><span data-stu-id="29b01-147">When **Find next** is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="29b01-148">Klikk **Poster**.</span><span class="sxs-lookup"><span data-stu-id="29b01-148">Click **Post**.</span></span>
36. <span data-ttu-id="29b01-149">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="29b01-149">Click **OK**.</span></span>
37. <span data-ttu-id="29b01-150">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="29b01-150">Close the page.</span></span>
38. <span data-ttu-id="29b01-151">Klikk Selg i **handlingsruten.**</span><span class="sxs-lookup"><span data-stu-id="29b01-151">On the **Action Pane**, click Sell.</span></span>
39. <span data-ttu-id="29b01-152">Klikk **Salgspris**.</span><span class="sxs-lookup"><span data-stu-id="29b01-152">Click **Sales price**.</span></span>

