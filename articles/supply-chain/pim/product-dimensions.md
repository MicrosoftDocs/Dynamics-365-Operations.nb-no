---
title: Produktdimensjoner
description: Det finnes fire produktdimensjoner – farge, konfigurasjon, størrelse og stil. Du kan kombinere produktdimensjoner i dimensjonsgrupper og tilordne dimensjonsgrupper til produktstandarder. Kombinasjonene av produktdimensjoner bestemmer hvordan produktvarianter defineres.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccb9d47bf6f081dbcc9590bddd4516cf7385ec23
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563580"
---
# <a name="product-dimensions"></a><span data-ttu-id="36f52-105">Produktdimensjoner</span><span class="sxs-lookup"><span data-stu-id="36f52-105">Product dimensions</span></span>

[!include [banner](../includes/banner.md)]

[!include [Retail name](../includes/retail-name.md)]

<span data-ttu-id="36f52-106">Det finnes fire produktdimensjoner – farge, konfigurasjon, størrelse og stil.</span><span class="sxs-lookup"><span data-stu-id="36f52-106">There are four product dimensions -  Color, Configuration, Size and Style.</span></span> <span data-ttu-id="36f52-107">Du kan kombinere produktdimensjoner i dimensjonsgrupper og tilordne dimensjonsgrupper til produktstandarder.</span><span class="sxs-lookup"><span data-stu-id="36f52-107">You combine product dimensions in dimension groups and assign dimension groups to product masters.</span></span> <span data-ttu-id="36f52-108">Kombinasjonene av produktdimensjoner bestemmer hvordan produktvarianter defineres.</span><span class="sxs-lookup"><span data-stu-id="36f52-108">The combinations of product dimensions determine how product variants are defined.</span></span>

<span data-ttu-id="36f52-109">Produktdimensjoner er egenskaper som brukes til å identifisere en produktvariant.</span><span class="sxs-lookup"><span data-stu-id="36f52-109">Product dimensions are characteristics that serve to identify a product variant.</span></span> <span data-ttu-id="36f52-110">Du kan bruke kombinasjoner av produktdimensjoner til å definere produktvariantene.</span><span class="sxs-lookup"><span data-stu-id="36f52-110">You can use combinations of product dimensions to define product variants.</span></span> <span data-ttu-id="36f52-111">Du må definere minst én produktdimensjon for en produktstandard for å opprette en produktvariant.</span><span class="sxs-lookup"><span data-stu-id="36f52-111">You must define at least one product dimension for a product master in order to create a product variant.</span></span>
<span data-ttu-id="36f52-112">Produktvarianter</span><span class="sxs-lookup"><span data-stu-id="36f52-112">Product variants</span></span>
----------------

<span data-ttu-id="36f52-113">Produktvarianter omtales også som varer.</span><span class="sxs-lookup"><span data-stu-id="36f52-113">Product variants are also referred to as items.</span></span> <span data-ttu-id="36f52-114">En vare er et materielt produkt, som ikke er det samme som en tjeneste.</span><span class="sxs-lookup"><span data-stu-id="36f52-114">An item is a tangible product, which is not the same as a service.</span></span> <span data-ttu-id="36f52-115">Det er også mulig å definere en produktstandard tjenestetypen.</span><span class="sxs-lookup"><span data-stu-id="36f52-115">It is also possible to define a product master with the Service type.</span></span> <span data-ttu-id="36f52-116">Når du bruker tjenestetypen, kan du angi produktvarianter som omfatter tjenester.</span><span class="sxs-lookup"><span data-stu-id="36f52-116">By using the Service type, you can specify product variants that include services.</span></span> <span data-ttu-id="36f52-117">Du kan for eksempel angi en produktstandard for konsulentarbeid og produktvarianter for arbeid som utføres av seniorkonsulenter og juniorkonsulenter.</span><span class="sxs-lookup"><span data-stu-id="36f52-117">For example, you can specify a product master for Consultancy work and product variants for work that is performed by senior consultants and junior consultants.</span></span>

## <a name="product-dimensions"></a><span data-ttu-id="36f52-118">Produktdimensjoner</span><span class="sxs-lookup"><span data-stu-id="36f52-118">Product dimensions</span></span>
<span data-ttu-id="36f52-119">Følgende produktdimensjoner er tilgjengelige: konfigurasjon, farge, størrelse og stil.</span><span class="sxs-lookup"><span data-stu-id="36f52-119">The following product dimensions are available: Configuration, Color, Size, and Style.</span></span> <span data-ttu-id="36f52-120">En produktvariant kan genereres basert på produktdimensjonsverdiene.</span><span class="sxs-lookup"><span data-stu-id="36f52-120">A product variant can be generated based on the product dimension values.</span></span>

<span data-ttu-id="36f52-121">Produktdimensjonsverdier som størrelse, farge og stil kan opprettes på sidene **Størrelse**, **Farge** og **Stil**, som er tilgjengelige fra følgende steder: **Produktinformasjonsbehandling** &gt; **Oppsett** &gt; **Dimensjons- og variantgrupper** &gt; **Størrelser/farger/stiler**.</span><span class="sxs-lookup"><span data-stu-id="36f52-121">Product dimensions values such as Size, Color and Style can be created on the **Size**, **Color** and **Style** pages, which can be accessed from the following locations: **Product information management** &gt; **Setup** &gt; **Dimension and variant Groups** &gt; **Sizes/Colors/Styles**.</span></span> <span data-ttu-id="36f52-122">Produktdimensjonsverdier for konfigurasjonsdimensjonen opprettes vanligvis ved hjelp av produktkonfiguratoren eller den dimensjonsbaserte konfiguratoren.</span><span class="sxs-lookup"><span data-stu-id="36f52-122">Product dimension values for the Configuration dimension are typically created using either the Product configurator or the Dimension-based configurator.</span></span> <span data-ttu-id="36f52-123">Produktdimensjoner kan også opprettes og vedlikeholdes på **Produktdimensjoner**-siden, som er tilgjengelig fra følgende steder:</span><span class="sxs-lookup"><span data-stu-id="36f52-123">Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:</span></span>
-   <span data-ttu-id="36f52-124">Klikk på **Produktinformasjonsbehandling** &gt; **Produkter** &gt; **Produktstandarder**.</span><span class="sxs-lookup"><span data-stu-id="36f52-124">Click **Product information management** &gt; **Products** &gt; **Product masters**.</span></span> <span data-ttu-id="36f52-125">I **handlingsruten** klikker du på **Produktdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="36f52-125">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="36f52-126">Klikk på **Produktinformasjonsbehandling** &gt; **Produkter** &gt; **Alle produkter og produktstandarder**.</span><span class="sxs-lookup"><span data-stu-id="36f52-126">Click **Product information management** &gt; **Products** &gt; **All products and product masters**.</span></span> <span data-ttu-id="36f52-127">Velg en produktstandard.</span><span class="sxs-lookup"><span data-stu-id="36f52-127">Select a product master.</span></span> <span data-ttu-id="36f52-128">I **handlingsruten** klikker du på **Produktdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="36f52-128">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="36f52-129">Klikk på **Behandling av produktinformasjon** &gt; **Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="36f52-129">Click **Product information management** &gt; **Released products**.</span></span> <span data-ttu-id="36f52-130">Velg en produktstandard.</span><span class="sxs-lookup"><span data-stu-id="36f52-130">Select a product master.</span></span> <span data-ttu-id="36f52-131">I **handlingsruten** klikker du på **Produkt**.</span><span class="sxs-lookup"><span data-stu-id="36f52-131">On the **Action Pane**, click **Product**.</span></span> <span data-ttu-id="36f52-132">I gruppen **Produktstandard** klikker du **Produktdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="36f52-132">In the **Product master** group, click **Product dimensions**.</span></span>

<span data-ttu-id="36f52-133">Antallet varianter du kan opprette for en vare, er begrenset av antallet mulige kombinasjoner av produktdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="36f52-133">The number of variants that you can create for an item is limited by the number of possible product dimension combinations.</span></span>

| <span data-ttu-id="36f52-134">**Tips!**</span><span class="sxs-lookup"><span data-stu-id="36f52-134">**Tip**</span></span>                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36f52-135">Når du for eksempel bruker et produkt på en ordrelinje, velger du produktdimensjonene for å identifisere produktvarianten du vil arbeide med.</span><span class="sxs-lookup"><span data-stu-id="36f52-135">When you use a product on, for example, an order line, you select the product dimensions to identify the product variant that you want to work with.</span></span> |

## <a name="example"></a><span data-ttu-id="36f52-136">Eksempel</span><span class="sxs-lookup"><span data-stu-id="36f52-136">Example</span></span>
<span data-ttu-id="36f52-137">Et firma selger dongeribukser.</span><span class="sxs-lookup"><span data-stu-id="36f52-137">A company sells denim jeans.</span></span> <span data-ttu-id="36f52-138">Varen dongeribukser bruker produktdimensjonene Farge og Størrelse.</span><span class="sxs-lookup"><span data-stu-id="36f52-138">The item, Jeans, uses the Color and Size product dimensions.</span></span> <span data-ttu-id="36f52-139">Dongeribuksene selges i tre forskjellige farger og seks forskjellige størrelser.</span><span class="sxs-lookup"><span data-stu-id="36f52-139">The jeans are sold in three different colors and six different sizes.</span></span> <span data-ttu-id="36f52-140">Farger: blå, svart, brun, Størrelser: XS, S, M, L, XL, XXL, ikke alle størrelser er tilgjengelige i alle tre fargene.</span><span class="sxs-lookup"><span data-stu-id="36f52-140">Colors: Blue, Black, Brown Sizes: XS, S, M, L, XL, XXL Not all sizes are available in all the three colors.</span></span> <span data-ttu-id="36f52-141">Hvis alle kombinasjonene hadde vært tilgjengelige, hadde det blitt opprettet 18 forskjellige typer dongeribukser.</span><span class="sxs-lookup"><span data-stu-id="36f52-141">If all combinations were available, it would create 18 different types of jeans.</span></span> <span data-ttu-id="36f52-142">I dette eksemplet produseres bare de følgende ni produktvariantkombinasjonene.</span><span class="sxs-lookup"><span data-stu-id="36f52-142">In this example, only the following nine product variant combinations are produced.</span></span>

| <span data-ttu-id="36f52-143">Farge</span><span class="sxs-lookup"><span data-stu-id="36f52-143">Color</span></span> | <span data-ttu-id="36f52-144">Størrelse</span><span class="sxs-lookup"><span data-stu-id="36f52-144">Size</span></span> |
|-------|------|
| <span data-ttu-id="36f52-145">Blå</span><span class="sxs-lookup"><span data-stu-id="36f52-145">Blue</span></span>  | <span data-ttu-id="36f52-146">XS</span><span class="sxs-lookup"><span data-stu-id="36f52-146">XS</span></span>   |
| <span data-ttu-id="36f52-147">Blå</span><span class="sxs-lookup"><span data-stu-id="36f52-147">Blue</span></span>  | <span data-ttu-id="36f52-148">L</span><span class="sxs-lookup"><span data-stu-id="36f52-148">S</span></span>    |
| <span data-ttu-id="36f52-149">Blå</span><span class="sxs-lookup"><span data-stu-id="36f52-149">Blue</span></span>  | <span data-ttu-id="36f52-150">M</span><span class="sxs-lookup"><span data-stu-id="36f52-150">M</span></span>    |
| <span data-ttu-id="36f52-151">Svart</span><span class="sxs-lookup"><span data-stu-id="36f52-151">Black</span></span> | <span data-ttu-id="36f52-152">M</span><span class="sxs-lookup"><span data-stu-id="36f52-152">M</span></span>    |
| <span data-ttu-id="36f52-153">Svart</span><span class="sxs-lookup"><span data-stu-id="36f52-153">Black</span></span> | <span data-ttu-id="36f52-154">L</span><span class="sxs-lookup"><span data-stu-id="36f52-154">L</span></span>    |
| <span data-ttu-id="36f52-155">Svart</span><span class="sxs-lookup"><span data-stu-id="36f52-155">Black</span></span> | <span data-ttu-id="36f52-156">XL</span><span class="sxs-lookup"><span data-stu-id="36f52-156">XL</span></span>   |
| <span data-ttu-id="36f52-157">Brun</span><span class="sxs-lookup"><span data-stu-id="36f52-157">Brown</span></span> | <span data-ttu-id="36f52-158">L</span><span class="sxs-lookup"><span data-stu-id="36f52-158">L</span></span>    |
| <span data-ttu-id="36f52-159">Brun</span><span class="sxs-lookup"><span data-stu-id="36f52-159">Brown</span></span> | <span data-ttu-id="36f52-160">XL</span><span class="sxs-lookup"><span data-stu-id="36f52-160">XL</span></span>   |
| <span data-ttu-id="36f52-161">Brun</span><span class="sxs-lookup"><span data-stu-id="36f52-161">Brown</span></span> | <span data-ttu-id="36f52-162">XXL</span><span class="sxs-lookup"><span data-stu-id="36f52-162">XXL</span></span>  |





