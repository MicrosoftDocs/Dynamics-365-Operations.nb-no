---
title: Endre sorteringsrekkefølgen for varehandelsenheter
description: I dette emnet forklares begrepene som er relatert til å styre visningsrekkefølgen for ulike varehandelsrelaterte enheter i Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b983cb5c63db171c76d34375a93a2b9086185d3a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414651"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="8a3db-103">Endre sorteringsrekkefølgen for varehandelsenheter</span><span class="sxs-lookup"><span data-stu-id="8a3db-103">Change the sort order for merchandising entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8a3db-104">Forhandlere vurderer produktgjenkjenning som et primært verktøy for kundeinteraksjon på tvers av alle kanaler.</span><span class="sxs-lookup"><span data-stu-id="8a3db-104">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span> <span data-ttu-id="8a3db-105">Forskjellige funksjoner kan hjelpe kunder å oppdage produkter på en enkel måte.</span><span class="sxs-lookup"><span data-stu-id="8a3db-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="8a3db-106">De kan for eksempel bla gjennom kategorier, søke og filtrere.</span><span class="sxs-lookup"><span data-stu-id="8a3db-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="8a3db-107">I dette emnet forklares begrepene som er relatert til å styre visningsrekkefølgen for ulike varehandelsrelaterte enheter.</span><span class="sxs-lookup"><span data-stu-id="8a3db-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="8a3db-108">Det forklarer også hvordan du endrer sorteringsrekkefølgen.</span><span class="sxs-lookup"><span data-stu-id="8a3db-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="8a3db-109">Oversikt</span><span class="sxs-lookup"><span data-stu-id="8a3db-109">Overview</span></span>

<span data-ttu-id="8a3db-110">Støtten for sortering av ulike varehandelsrelaterte enheter er forbedret.</span><span class="sxs-lookup"><span data-stu-id="8a3db-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="8a3db-111">Denne støtten er nå bedre justert med eksisterende kundescenarier som tidligere krevde utvidelser fra implementeringspartnere.</span><span class="sxs-lookup"><span data-stu-id="8a3db-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="8a3db-112">I versjoner av Retail som er tidligere enn versjon 10.0.5, var sorteringsrekkefølgen for kategorier i navigasjonshierarkiet alfabetisk.</span><span class="sxs-lookup"><span data-stu-id="8a3db-112">In versions of Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="8a3db-113">Den nye egendefinerte funksjonen for sorteringsrekkefølge gjør at ledere kan konfigurere sorteringsrekkefølgen for ulike varehandelsrelaterte enheter på tvers av alle sluttbrukerklienter.</span><span class="sxs-lookup"><span data-stu-id="8a3db-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="8a3db-114">Disse klientene inkluderer hovedkontorer og telefonsentre.</span><span class="sxs-lookup"><span data-stu-id="8a3db-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a><span data-ttu-id="8a3db-115">Konfigurer visningsrekkefølgen for kategorier i produkthierarkiet</span><span class="sxs-lookup"><span data-stu-id="8a3db-115">Configure the display order for categories in the product hierarchy</span></span>

<span data-ttu-id="8a3db-116">Før du kan fullføre denne prosedyren, må du installere demodata i miljøet.</span><span class="sxs-lookup"><span data-stu-id="8a3db-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="8a3db-117">Gå til **Detaljhandel og handel \> Produkter og kategorier \> Handelsprodukthierarki**.</span><span class="sxs-lookup"><span data-stu-id="8a3db-117">Go to **Retail and Commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
2. <span data-ttu-id="8a3db-118">Klikk **Rediger kategorihierarki**.</span><span class="sxs-lookup"><span data-stu-id="8a3db-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="8a3db-119">Klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="8a3db-119">Click **Edit**.</span></span>
4. <span data-ttu-id="8a3db-120">Utvid **ALL \> Action Sports** i treet.</span><span class="sxs-lookup"><span data-stu-id="8a3db-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="8a3db-121">Utvid **ALL \> Team Sports** i treet.</span><span class="sxs-lookup"><span data-stu-id="8a3db-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="8a3db-122">Angi et tall i **Visningsrekkefølge**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8a3db-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="8a3db-123">(Nummeret kan være negativt.)</span><span class="sxs-lookup"><span data-stu-id="8a3db-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="8a3db-124">Gjenta trinn 4 til og med 6 for eventuelle tilleggskategorier du vil endre rekkefølgen på.</span><span class="sxs-lookup"><span data-stu-id="8a3db-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="8a3db-125">Visningsrekkefølgen for kanalnavigasjonshierarkiet vil gjenspeiles i hovedkontoret for handelsprodukthierarkiet og frigitte produkter etter kategori.</span><span class="sxs-lookup"><span data-stu-id="8a3db-125">The display order for the channel navigation hierarchy will be reflected in HQ for the commerce product hierarchy and released products by category.</span></span>

![Egendefinert sortering av produkthierarki med negative verdier](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Egendefinert sortering av frigitte produkter etter kategori basert på produkthierarkiet](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="8a3db-128">Konfigurer visningsrekkefølgen for kategorier i kanalnavigasjonshierarkiet</span><span class="sxs-lookup"><span data-stu-id="8a3db-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="8a3db-129">Før du kan fullføre denne prosedyren, må du installere demodata i miljøet.</span><span class="sxs-lookup"><span data-stu-id="8a3db-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="8a3db-130">Gå til **Detaljhandel og handel \> Produkter og kategorier \> Navigasjonskategorier for kanal**.</span><span class="sxs-lookup"><span data-stu-id="8a3db-130">Go to **Retail and Commerce \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="8a3db-131">I listen velger du **navigasjonshierarkiet for klær**.</span><span class="sxs-lookup"><span data-stu-id="8a3db-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="8a3db-132">Klikk **Rediger kategorihierarki**.</span><span class="sxs-lookup"><span data-stu-id="8a3db-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="8a3db-133">Klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="8a3db-133">Click **Edit**.</span></span>
5. <span data-ttu-id="8a3db-134">Velg **Fashion \> Womenswear \> Womens Shoes** i treet.</span><span class="sxs-lookup"><span data-stu-id="8a3db-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="8a3db-135">Angi et tall i **Visningsrekkefølge**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8a3db-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="8a3db-136">Velg **Fashion \> Womenswear \> Tops** i treet.</span><span class="sxs-lookup"><span data-stu-id="8a3db-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="8a3db-137">På samme måte kan du definere sorteringsrekkefølgen for under kategoriene.</span><span class="sxs-lookup"><span data-stu-id="8a3db-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="8a3db-138">Velg **Fashion \> Menswear \> Casual Shirts** i treet.</span><span class="sxs-lookup"><span data-stu-id="8a3db-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="8a3db-139">Angi et tall i **Visningsrekkefølge**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8a3db-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="8a3db-140">Velg **Fashion \> Menswear \> Coats & Jackets** i treet.</span><span class="sxs-lookup"><span data-stu-id="8a3db-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="8a3db-141">Angi et tall i **Visningsrekkefølge**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8a3db-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="8a3db-142">Gjenta for eventuelle tilleggskategorier du vil endre rekkefølgen på.</span><span class="sxs-lookup"><span data-stu-id="8a3db-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="8a3db-143">Visningsrekkefølgen for kanalnavigasjonshierarkiet gjenspeiles i hovedkontor, katalog og kanaler.</span><span class="sxs-lookup"><span data-stu-id="8a3db-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and channels.</span></span>

![Egendefinert sortering av navigasjonshierarki for kanal](./media/ChannelNavCustomSorted.png)

![Egendefinert sortering av navigasjonshierarki for katalog basert på kanalnavigasjonshierarkiet](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![Salgssted med egendefinert sortering av kategorier](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="8a3db-147">Funksjonen for egendefinert sortering er deaktivert som standard.</span><span class="sxs-lookup"><span data-stu-id="8a3db-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="8a3db-148">Hvis du vil vite hvordan du aktiverer denne funksjonen og andre funksjoner, kan du se [Funksjonsbehandling](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="8a3db-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>
