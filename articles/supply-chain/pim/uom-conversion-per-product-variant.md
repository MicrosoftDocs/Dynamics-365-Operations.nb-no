---
title: Konvertering for måleenhet per produktvariant
description: Dette emnet forklarer hvordan konverteringer av måleenheter kan defineres for produktvarianter.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 36fc98c44625cce03945d76973de67021d53353e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844375"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="80877-103">Konvertering for måleenhet per produktvariant</span><span class="sxs-lookup"><span data-stu-id="80877-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

<span data-ttu-id="80877-104">Dette emnet forklarer hvordan konverteringer av måleenheter kan defineres for produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="80877-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="80877-105">Det inneholder et eksempel på oppsettet.</span><span class="sxs-lookup"><span data-stu-id="80877-105">It includes an example of the setup.</span></span>

<span data-ttu-id="80877-106">Denne funksjonen gjør det mulig for firmaer å definere ulik enhetsomregning mellom variantene av samme produkt.</span><span class="sxs-lookup"><span data-stu-id="80877-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="80877-107">Eksemplet nedenfor brukes i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="80877-107">The following example is used in this topic.</span></span> <span data-ttu-id="80877-108">Et firma selger t-skjorter i størrelsene Liten, Middels, Stor og Ekstra stor.</span><span class="sxs-lookup"><span data-stu-id="80877-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="80877-109">T-skjorten er definert som et produkt, og de ulike størrelsene er definert som varianter av produktet.</span><span class="sxs-lookup"><span data-stu-id="80877-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="80877-110">T-skjortene pakkes i bokser, og det kan være fem t-skjorter i en boks, bortsett fra ekstra stor-størrelsen der det bare er plass til fire t-skjorter.</span><span class="sxs-lookup"><span data-stu-id="80877-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="80877-111">Firmaet ønsker å spore de ulike variantene av t-skjorter i enheten **Stykker**, men selger t-skjortene i enheten **Boks**.</span><span class="sxs-lookup"><span data-stu-id="80877-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="80877-112">Konverteringen mellom lagerenheten og salgsenheten er 1 boks = 5 stykker, med unntak av varianten ekstra stor, der konverteringen er 1 boks = 4 stykker.</span><span class="sxs-lookup"><span data-stu-id="80877-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

## <a name="setup"></a><span data-ttu-id="80877-113">Installasjon</span><span class="sxs-lookup"><span data-stu-id="80877-113">Setup</span></span>

<span data-ttu-id="80877-114">Du kan konfigurere parameterne for å bruke funksjonen for produkter som er aktivert for **Alle prosesser** eller bare for produkt som er aktivert for **Lagerprosesser** ved hjelp av **Aktiver måleenhetskonverteringer**-alternativet på **Produktinformasjonsparametere**-siden.</span><span class="sxs-lookup"><span data-stu-id="80877-114">You can configure the parameters for using the feature for products enabled for **All processes** or only for product enabled for the **Warehouse processes** by using the **Enable unit of measure conversations** option on the **Product information parameters** page.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="80877-115">Definere et produkt for enhetsomregning per variant</span><span class="sxs-lookup"><span data-stu-id="80877-115">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="80877-116">Produktvarianter kan bare opprettes for produkter av undertypen **Produkt**: **Produktstandard**.</span><span class="sxs-lookup"><span data-stu-id="80877-116">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="80877-117">Hvis du vil ha mer informasjon, kan du se [Opprette en produktstandard](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="80877-117">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="80877-118">Funksjonen er ikke aktivert for produkter som er angitt for Faktisk vekt-prosesser.</span><span class="sxs-lookup"><span data-stu-id="80877-118">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="80877-119">Under opprettingen av en produktstandard aktiverer du konvertering for måleenhet ved hjelp av **Aktiver måleenhetskonverteringer**-alternativet på **Produktdetaljer**-siden.</span><span class="sxs-lookup"><span data-stu-id="80877-119">During the creation of a product master enable unit of measure conversion by using the **Enable unit of measure conversions** option on the **Product details** page.</span></span>

<span data-ttu-id="80877-120">Når produktstandarden med frigitte produktvarianter er opprettet, kan enhetsomregninger per varianter defineres.</span><span class="sxs-lookup"><span data-stu-id="80877-120">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="80877-121">Du finner menyelementet for å åpne enhetskonverteringssiden i forbindelse med et produkt eller en produktvariant på følgende sider.</span><span class="sxs-lookup"><span data-stu-id="80877-121">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="80877-122">**Produktdetaljer**-siden</span><span class="sxs-lookup"><span data-stu-id="80877-122">**Product details** page</span></span>
-   <span data-ttu-id="80877-123">**Detaljer om frigitte produkter**-siden</span><span class="sxs-lookup"><span data-stu-id="80877-123">**Released products details** page</span></span>
-   <span data-ttu-id="80877-124">**Frigitte produktvarianter**-siden</span><span class="sxs-lookup"><span data-stu-id="80877-124">**Released product variants** page</span></span>

<span data-ttu-id="80877-125">Når du åpner **Enhetsomregning**-siden i konteksten av en produktstandard eller frigitt produktvariant, kan du velge om du vil definere enhetsomregning for produktet eller for en produktvariant.</span><span class="sxs-lookup"><span data-stu-id="80877-125">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="80877-126">Det gjør du ved å velge enten **Produktvariant** eller **Produkt** i **Opprett konvertering for**-feltet.</span><span class="sxs-lookup"><span data-stu-id="80877-126">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="80877-127">Produktvariant</span><span class="sxs-lookup"><span data-stu-id="80877-127">Product variant</span></span>

<span data-ttu-id="80877-128">Hvis du velger **Produktvariant**, kan du velge hvilken variant du vil definere enhetsomregning for i **Produktvariant**-feltet.</span><span class="sxs-lookup"><span data-stu-id="80877-128">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="80877-129">Produkt</span><span class="sxs-lookup"><span data-stu-id="80877-129">Product</span></span>

<span data-ttu-id="80877-130">Hvis du velger **Produkt**, kan du definere en enhetsomregning for produktstandarden.</span><span class="sxs-lookup"><span data-stu-id="80877-130">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="80877-131">Denne enhetsomregningen vil gjelde for alle produktvarianter uten definert enhetsomregning.</span><span class="sxs-lookup"><span data-stu-id="80877-131">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="80877-132">Eksempel</span><span class="sxs-lookup"><span data-stu-id="80877-132">Example</span></span>

<span data-ttu-id="80877-133">Produktstandarden **t-skjorte** har fire frigitte produktvarianter: liten, middels, stor og ekstra stor.</span><span class="sxs-lookup"><span data-stu-id="80877-133">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="80877-134">T-skjortene er pakket i bokser, og det kan være fem t-skjorter i en boks, bortsett fra ekstra stor-størrelsen der det bare er plass til fire t-skjorter.</span><span class="sxs-lookup"><span data-stu-id="80877-134">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="80877-135">Først må du åpne **Enhetsomregning**-siden fra siden Frigi produktdetaljer for **t-skjorte.**</span><span class="sxs-lookup"><span data-stu-id="80877-135">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="80877-136">På **Enhetsomregning**-siden definerer du enhetsomregning for den frigitte produktvarianten ekstra stor.</span><span class="sxs-lookup"><span data-stu-id="80877-136">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="80877-137">**Felt**</span><span class="sxs-lookup"><span data-stu-id="80877-137">**Field**</span></span>             | <span data-ttu-id="80877-138">**Innstilling**</span><span class="sxs-lookup"><span data-stu-id="80877-138">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="80877-139">Opprett konvertering for</span><span class="sxs-lookup"><span data-stu-id="80877-139">Create conversion for</span></span> | <span data-ttu-id="80877-140">Produktvariant</span><span class="sxs-lookup"><span data-stu-id="80877-140">Product variant</span></span>         |
| <span data-ttu-id="80877-141">Produktvariant</span><span class="sxs-lookup"><span data-stu-id="80877-141">Product variant</span></span>       | <span data-ttu-id="80877-142">T-skjorte : : Ekstra stor : :</span><span class="sxs-lookup"><span data-stu-id="80877-142">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="80877-143">Fra enhet</span><span class="sxs-lookup"><span data-stu-id="80877-143">From unit</span></span>             | <span data-ttu-id="80877-144">Bokser</span><span class="sxs-lookup"><span data-stu-id="80877-144">Boxes</span></span>                   |
| <span data-ttu-id="80877-145">Omregningsfaktor</span><span class="sxs-lookup"><span data-stu-id="80877-145">Factor</span></span>                | <span data-ttu-id="80877-146">4</span><span class="sxs-lookup"><span data-stu-id="80877-146">4</span></span>                       |
| <span data-ttu-id="80877-147">Til enhet</span><span class="sxs-lookup"><span data-stu-id="80877-147">To Unit</span></span>               | <span data-ttu-id="80877-148">Stykker</span><span class="sxs-lookup"><span data-stu-id="80877-148">Pieces</span></span>                  |

<span data-ttu-id="80877-149">De frigitte produktvariantene liten, middels og stor har samme enhetsomregning mellom enheten Boks og Stykker, som betyr at du kan definere enhetsomregning for disse produktvariantene i produktstandarden.</span><span class="sxs-lookup"><span data-stu-id="80877-149">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="80877-150">**Felt**</span><span class="sxs-lookup"><span data-stu-id="80877-150">**Field**</span></span>             | <span data-ttu-id="80877-151">**Innstilling**</span><span class="sxs-lookup"><span data-stu-id="80877-151">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="80877-152">Opprett konvertering for</span><span class="sxs-lookup"><span data-stu-id="80877-152">Create conversion for</span></span> | <span data-ttu-id="80877-153">Produkt</span><span class="sxs-lookup"><span data-stu-id="80877-153">Product</span></span>     |
| <span data-ttu-id="80877-154">Produkt</span><span class="sxs-lookup"><span data-stu-id="80877-154">Product</span></span>               | <span data-ttu-id="80877-155">T-skjorte</span><span class="sxs-lookup"><span data-stu-id="80877-155">T-Shirt</span></span>     |
| <span data-ttu-id="80877-156">Fra enhet</span><span class="sxs-lookup"><span data-stu-id="80877-156">From unit</span></span>             | <span data-ttu-id="80877-157">Bokser</span><span class="sxs-lookup"><span data-stu-id="80877-157">Boxes</span></span>       |
| <span data-ttu-id="80877-158">Omregningsfaktor</span><span class="sxs-lookup"><span data-stu-id="80877-158">Factor</span></span>                | <span data-ttu-id="80877-159">5</span><span class="sxs-lookup"><span data-stu-id="80877-159">5</span></span>           |
| <span data-ttu-id="80877-160">Til enhet</span><span class="sxs-lookup"><span data-stu-id="80877-160">To Unit</span></span>               | <span data-ttu-id="80877-161">Stykker</span><span class="sxs-lookup"><span data-stu-id="80877-161">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="80877-162">Bruke Excel til å oppdatere enhetsomregningene</span><span class="sxs-lookup"><span data-stu-id="80877-162">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="80877-163">Hvis et produkt har mange produktvarianter med forskjellige enhetsomregninger, er det lurt å eksportere enhetskonverteringene fra **Enhetsomregning**-siden til et Excel-regneark, oppdatere konverteringene og deretter publisere dem tilbake til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="80877-163">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Finance and Operations.</span></span>

<span data-ttu-id="80877-164">Alternativet for å eksportere til Excel og publisere endringene tilbake til Finance and Operations, aktiveres fra **Åpne i Microsoft office**-menyelementet i handlingsruten på **Enhetsomregning**-siden.</span><span class="sxs-lookup"><span data-stu-id="80877-164">The option to export to Excel and publish the edits back to Finance and Operations is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
