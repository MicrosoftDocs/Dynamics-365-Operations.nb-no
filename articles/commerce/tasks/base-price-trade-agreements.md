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
ms.openlocfilehash: 44dc059f7bfc3ba83a375c197ce67f1378a9bc9b
ms.sourcegitcommit: 74b10104338222a945684d841d60ab4b8e570168
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3899355"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="dfa89-103"> Basispris og forretningsavtaler</span><span class="sxs-lookup"><span data-stu-id="dfa89-103">Base price and trade agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dfa89-104">Denne prosedyren hjelper med å opprette kanalspesifikke salgsprisforretningsavtaler.</span><span class="sxs-lookup"><span data-stu-id="dfa89-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="dfa89-105">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="dfa89-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="dfa89-106">I **navigasjonsruten** går du til **Moduler > Retail og Commerce > Prissetting og rabattstyring > Prisgrupper > Alle prisgrupper**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-106">In the **Navigation pane**, go to **Modules > Retail and Commerce > Pricing and discounts management > Price groups > All price groups**.</span></span> <span data-ttu-id="dfa89-107">Prisgrupper er måten forretningsavtaler tilordnes til bestemte kanaler på.</span><span class="sxs-lookup"><span data-stu-id="dfa89-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="dfa89-108">Kanalspesifikke priser blir mulig ved å bruke prisgrupper for å tilordne forretningsavtaler til en kanal.</span><span class="sxs-lookup"><span data-stu-id="dfa89-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="dfa89-109">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-109">Click **New**.</span></span>
3. <span data-ttu-id="dfa89-110">Skriv inn en verdi i feltet **Prisgrupper**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-110">In the **Price groups** field, type a value.</span></span>
4. <span data-ttu-id="dfa89-111">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="dfa89-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="dfa89-112">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-112">Click **Save**.</span></span>
6. <span data-ttu-id="dfa89-113">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="dfa89-113">Close the page.</span></span>
7. <span data-ttu-id="dfa89-114">I **navigasjonsruten** går du til **Moduler > Retail og Commerce > Kanaler > Butikker > Alle butikker**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-114">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
8. <span data-ttu-id="dfa89-115">Velg New York i listen.</span><span class="sxs-lookup"><span data-stu-id="dfa89-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="dfa89-116">Klikk **Butikk** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dfa89-116">On the Action Pane, click **Store**.</span></span>
10. <span data-ttu-id="dfa89-117">Klikk **Prisgrupper**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-117">Click **Price groups**.</span></span>
11. <span data-ttu-id="dfa89-118">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-118">Click **New**.</span></span>
12. <span data-ttu-id="dfa89-119">Klikk rullegardinknappen i **Prisgrupper**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="dfa89-119">In the **Price groups** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="dfa89-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="dfa89-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="dfa89-121">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-121">Click **Save**.</span></span>
15. <span data-ttu-id="dfa89-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="dfa89-122">Close the page.</span></span>
16. <span data-ttu-id="dfa89-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="dfa89-123">Close the page.</span></span>
17. <span data-ttu-id="dfa89-124">I **navigasjonsruten** går du til **Moduler > Retail og Commerce > Produkter og kategorier > Frigitte produkter etter kategori**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-124">In the **Navigation pane**, go to **Modules > Retail and Commerce > Products and categories > Released products by category**.</span></span>
18. <span data-ttu-id="dfa89-125">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="dfa89-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="dfa89-126">Klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-126">Click **Edit**.</span></span>
20. <span data-ttu-id="dfa89-127">Utvid **Selg**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="dfa89-127">Expand the **Sell** fastTab.</span></span>
21. <span data-ttu-id="dfa89-128">Angi et tall i **Pris**-feltet</span><span class="sxs-lookup"><span data-stu-id="dfa89-128">In the **Price** field, enter a number.</span></span> <span data-ttu-id="dfa89-129">Denne prisen brukes hvis det ikke blir funnet en gjeldende forretningsavtale.</span><span class="sxs-lookup"><span data-stu-id="dfa89-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="dfa89-130">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-130">Click **Save**.</span></span>
23. <span data-ttu-id="dfa89-131">I **Handlingsrute** klikker du på **Selg**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-131">On the **Action Pane**, click **Sell**.</span></span>
24. <span data-ttu-id="dfa89-132">Klikk **Opprett forretningsavtaler**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-132">Click **Create trade agreements**.</span></span>
25. <span data-ttu-id="dfa89-133">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-133">Click **New**.</span></span>
26. <span data-ttu-id="dfa89-134">Klikk på rullegardinknappen i **Navn**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="dfa89-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="dfa89-135">Velg **Commerce** i listen.</span><span class="sxs-lookup"><span data-stu-id="dfa89-135">In the list, select **Commerce**.</span></span> <span data-ttu-id="dfa89-136">I demonstrasjonsdataene har journalnavnet **Commerce** standardrelasjonen **Pris (salg)**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-136">In the demo data, the **Commerce** journal name has the default relation of **Price (sales)**.</span></span> <span data-ttu-id="dfa89-137">Det betyr at alle nye linjer som opprettes, bruker salgsprisforretningsavtaler som standard.</span><span class="sxs-lookup"><span data-stu-id="dfa89-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="dfa89-138">Klikk på **Linjer** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-138">On the **Action pane**, click **Lines**.</span></span>
29. <span data-ttu-id="dfa89-139">Velg Gruppe i **Partskodetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="dfa89-139">In the **Party code type** field, select 'Group'.</span></span>
30. <span data-ttu-id="dfa89-140">Klikk på rullegardinknappen i **Kontovalg**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="dfa89-140">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="dfa89-141">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="dfa89-141">In the list, find and select the desired record.</span></span> <span data-ttu-id="dfa89-142">Dette fullfører koblingen fra kanal til prisgruppe til forretningsavtale.</span><span class="sxs-lookup"><span data-stu-id="dfa89-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="dfa89-143">Skriv inn en verdi i **Varerelasjon**-feltet.</span><span class="sxs-lookup"><span data-stu-id="dfa89-143">In the **Item relation** field, type a value.</span></span>
33. <span data-ttu-id="dfa89-144">Angi en verdi i feltet **Beløp i valuta**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-144">In the **Amount in currency** field, enter a number.</span></span>
34. <span data-ttu-id="dfa89-145">Merk av eller fjern merket for **Søk etter neste** i hurtigfanen **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-145">In the **Details** fastTab, check or uncheck the **Find next** checkbox.</span></span> <span data-ttu-id="dfa89-146">Når **Søk etter neste** settes til Ja, fortsetter prissettingsmotoren å søke etter gjeldende forretningsavtaler med en lavere salgspris.</span><span class="sxs-lookup"><span data-stu-id="dfa89-146">When **Find next** is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="dfa89-147">Når **Søk etter neste** settes til Nei, slutter motoren å søke og bruker forretningsavtalen.</span><span class="sxs-lookup"><span data-stu-id="dfa89-147">When **Find next** is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="dfa89-148">Klikk **Poster**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-148">Click **Post**.</span></span>
36. <span data-ttu-id="dfa89-149">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-149">Click **OK**.</span></span>
37. <span data-ttu-id="dfa89-150">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="dfa89-150">Close the page.</span></span>
38. <span data-ttu-id="dfa89-151">Klikk Selg i **handlingsruten.**</span><span class="sxs-lookup"><span data-stu-id="dfa89-151">On the **Action Pane**, click Sell.</span></span>
39. <span data-ttu-id="dfa89-152">Klikk **Salgspris**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-152">Click **Sales price**.</span></span>

