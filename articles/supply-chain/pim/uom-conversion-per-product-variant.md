---
title: Konvertering for måleenhet per produktvariant
description: Dette emnet forklarer hvordan konverteringer av måleenheter kan defineres for produktvarianter.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: c8181f0bda9b781a6c2b0feb0aba1beb51bfea65
ms.sourcegitcommit: af36eb17b36092a3101bbfc96486b25036676558
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/06/2020
ms.locfileid: "2935105"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="570b4-103">Konvertering for måleenhet per produktvariant</span><span class="sxs-lookup"><span data-stu-id="570b4-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="570b4-104">Dette emnet forklarer hvordan konverteringer av måleenheter kan defineres for produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="570b4-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="570b4-105">Det inneholder et eksempel på oppsettet.</span><span class="sxs-lookup"><span data-stu-id="570b4-105">It includes an example of the setup.</span></span>

<span data-ttu-id="570b4-106">Denne funksjonen gjør det mulig for firmaer å definere ulik enhetsomregning mellom variantene av samme produkt.</span><span class="sxs-lookup"><span data-stu-id="570b4-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="570b4-107">Eksemplet nedenfor brukes i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="570b4-107">The following example is used in this topic.</span></span> <span data-ttu-id="570b4-108">Et firma selger t-skjorter i størrelsene Liten, Middels, Stor og Ekstra stor.</span><span class="sxs-lookup"><span data-stu-id="570b4-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="570b4-109">T-skjorten er definert som et produkt, og de ulike størrelsene er definert som varianter av produktet.</span><span class="sxs-lookup"><span data-stu-id="570b4-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="570b4-110">T-skjortene pakkes i bokser, og det kan være fem t-skjorter i en boks, bortsett fra ekstra stor-størrelsen der det bare er plass til fire t-skjorter.</span><span class="sxs-lookup"><span data-stu-id="570b4-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="570b4-111">Firmaet ønsker å spore de ulike variantene av t-skjorter i enheten **Stykker**, men selger t-skjortene i enheten **Boks**.</span><span class="sxs-lookup"><span data-stu-id="570b4-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="570b4-112">Konverteringen mellom lagerenheten og salgsenheten er 1 boks = 5 stykker, med unntak av varianten ekstra stor, der konverteringen er 1 boks = 4 stykker.</span><span class="sxs-lookup"><span data-stu-id="570b4-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="570b4-113">Definere et produkt for enhetsomregning per variant</span><span class="sxs-lookup"><span data-stu-id="570b4-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="570b4-114">Produktvarianter kan bare opprettes for produkter av undertypen **Produkt**: **Produktstandard**.</span><span class="sxs-lookup"><span data-stu-id="570b4-114">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="570b4-115">Hvis du vil ha mer informasjon, kan du se [Opprette en produktstandard](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="570b4-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="570b4-116">Funksjonen er ikke aktivert for produkter som er angitt for Faktisk vekt-prosesser.</span><span class="sxs-lookup"><span data-stu-id="570b4-116">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="570b4-117">Når produktstandarden med frigitte produktvarianter er opprettet, kan enhetsomregninger per varianter defineres.</span><span class="sxs-lookup"><span data-stu-id="570b4-117">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="570b4-118">Du finner menyelementet for å åpne enhetskonverteringssiden i forbindelse med et produkt eller en produktvariant på følgende sider.</span><span class="sxs-lookup"><span data-stu-id="570b4-118">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="570b4-119">**Produktdetaljer**-siden</span><span class="sxs-lookup"><span data-stu-id="570b4-119">**Product details** page</span></span>
-   <span data-ttu-id="570b4-120">**Detaljer om frigitte produkter**-siden</span><span class="sxs-lookup"><span data-stu-id="570b4-120">**Released products details** page</span></span>
-   <span data-ttu-id="570b4-121">**Frigitte produktvarianter**-siden</span><span class="sxs-lookup"><span data-stu-id="570b4-121">**Released product variants** page</span></span>

<span data-ttu-id="570b4-122">Når du åpner **Enhetsomregning**-siden i konteksten av en produktstandard eller frigitt produktvariant, kan du velge om du vil definere enhetsomregning for produktet eller for en produktvariant.</span><span class="sxs-lookup"><span data-stu-id="570b4-122">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="570b4-123">Det gjør du ved å velge enten **Produktvariant** eller **Produkt** i **Opprett konvertering for**-feltet.</span><span class="sxs-lookup"><span data-stu-id="570b4-123">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="570b4-124">Produktvariant</span><span class="sxs-lookup"><span data-stu-id="570b4-124">Product variant</span></span>

<span data-ttu-id="570b4-125">Hvis du velger **Produktvariant**, kan du velge hvilken variant du vil definere enhetsomregning for i **Produktvariant**-feltet.</span><span class="sxs-lookup"><span data-stu-id="570b4-125">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="570b4-126">Produkt</span><span class="sxs-lookup"><span data-stu-id="570b4-126">Product</span></span>

<span data-ttu-id="570b4-127">Hvis du velger **Produkt**, kan du definere en enhetsomregning for produktstandarden.</span><span class="sxs-lookup"><span data-stu-id="570b4-127">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="570b4-128">Denne enhetsomregningen vil gjelde for alle produktvarianter uten definert enhetsomregning.</span><span class="sxs-lookup"><span data-stu-id="570b4-128">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="570b4-129">Eksempel</span><span class="sxs-lookup"><span data-stu-id="570b4-129">Example</span></span>

<span data-ttu-id="570b4-130">Produktstandarden **t-skjorte** har fire frigitte produktvarianter: liten, middels, stor og ekstra stor.</span><span class="sxs-lookup"><span data-stu-id="570b4-130">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="570b4-131">T-skjortene er pakket i bokser, og det kan være fem t-skjorter i en boks, bortsett fra ekstra stor-størrelsen der det bare er plass til fire t-skjorter.</span><span class="sxs-lookup"><span data-stu-id="570b4-131">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="570b4-132">Først må du åpne **Enhetsomregning**-siden fra siden Frigi produktdetaljer for **t-skjorte.**</span><span class="sxs-lookup"><span data-stu-id="570b4-132">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="570b4-133">På **Enhetsomregning**-siden definerer du enhetsomregning for den frigitte produktvarianten ekstra stor.</span><span class="sxs-lookup"><span data-stu-id="570b4-133">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="570b4-134">**Felt**</span><span class="sxs-lookup"><span data-stu-id="570b4-134">**Field**</span></span>             | <span data-ttu-id="570b4-135">**Innstilling**</span><span class="sxs-lookup"><span data-stu-id="570b4-135">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="570b4-136">Opprett konvertering for</span><span class="sxs-lookup"><span data-stu-id="570b4-136">Create conversion for</span></span> | <span data-ttu-id="570b4-137">Produktvariant</span><span class="sxs-lookup"><span data-stu-id="570b4-137">Product variant</span></span>         |
| <span data-ttu-id="570b4-138">Produktvariant</span><span class="sxs-lookup"><span data-stu-id="570b4-138">Product variant</span></span>       | <span data-ttu-id="570b4-139">T-skjorte : : Ekstra stor : :</span><span class="sxs-lookup"><span data-stu-id="570b4-139">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="570b4-140">Fra enhet</span><span class="sxs-lookup"><span data-stu-id="570b4-140">From unit</span></span>             | <span data-ttu-id="570b4-141">Bokser</span><span class="sxs-lookup"><span data-stu-id="570b4-141">Boxes</span></span>                   |
| <span data-ttu-id="570b4-142">Omregningsfaktor</span><span class="sxs-lookup"><span data-stu-id="570b4-142">Factor</span></span>                | <span data-ttu-id="570b4-143">4</span><span class="sxs-lookup"><span data-stu-id="570b4-143">4</span></span>                       |
| <span data-ttu-id="570b4-144">Til enhet</span><span class="sxs-lookup"><span data-stu-id="570b4-144">To Unit</span></span>               | <span data-ttu-id="570b4-145">Stykker</span><span class="sxs-lookup"><span data-stu-id="570b4-145">Pieces</span></span>                  |

<span data-ttu-id="570b4-146">De frigitte produktvariantene liten, middels og stor har samme enhetsomregning mellom enheten Boks og Stykker, som betyr at du kan definere enhetsomregning for disse produktvariantene i produktstandarden.</span><span class="sxs-lookup"><span data-stu-id="570b4-146">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="570b4-147">**Felt**</span><span class="sxs-lookup"><span data-stu-id="570b4-147">**Field**</span></span>             | <span data-ttu-id="570b4-148">**Innstilling**</span><span class="sxs-lookup"><span data-stu-id="570b4-148">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="570b4-149">Opprett konvertering for</span><span class="sxs-lookup"><span data-stu-id="570b4-149">Create conversion for</span></span> | <span data-ttu-id="570b4-150">Produkt</span><span class="sxs-lookup"><span data-stu-id="570b4-150">Product</span></span>     |
| <span data-ttu-id="570b4-151">Produkt</span><span class="sxs-lookup"><span data-stu-id="570b4-151">Product</span></span>               | <span data-ttu-id="570b4-152">T-skjorte</span><span class="sxs-lookup"><span data-stu-id="570b4-152">T-Shirt</span></span>     |
| <span data-ttu-id="570b4-153">Fra enhet</span><span class="sxs-lookup"><span data-stu-id="570b4-153">From unit</span></span>             | <span data-ttu-id="570b4-154">Bokser</span><span class="sxs-lookup"><span data-stu-id="570b4-154">Boxes</span></span>       |
| <span data-ttu-id="570b4-155">Omregningsfaktor</span><span class="sxs-lookup"><span data-stu-id="570b4-155">Factor</span></span>                | <span data-ttu-id="570b4-156">5</span><span class="sxs-lookup"><span data-stu-id="570b4-156">5</span></span>           |
| <span data-ttu-id="570b4-157">Til enhet</span><span class="sxs-lookup"><span data-stu-id="570b4-157">To Unit</span></span>               | <span data-ttu-id="570b4-158">Stykker</span><span class="sxs-lookup"><span data-stu-id="570b4-158">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="570b4-159">Bruke Excel til å oppdatere enhetsomregningene</span><span class="sxs-lookup"><span data-stu-id="570b4-159">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="570b4-160">Hvis et produkt har mange produktvarianter med forskjellige enhetsomregninger, er det lurt å eksportere enhetskonverteringene fra **Enhetsomregning**-siden til et Excel-regneark, oppdatere konverteringene og deretter publisere dem tilbake til Supply Chain Mangement.</span><span class="sxs-lookup"><span data-stu-id="570b4-160">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Supply Chain Mangement.</span></span>

<span data-ttu-id="570b4-161">Alternativet for å eksportere til Excel og publisere endringene tilbake til Supply Chain Mangement, aktiveres fra **Åpne i Microsoft office**-menyelementet i handlingsruten på **Enhetsomregning**-siden.</span><span class="sxs-lookup"><span data-stu-id="570b4-161">The option to export to Excel and publish the edits back to Supply Chain Mangement is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
