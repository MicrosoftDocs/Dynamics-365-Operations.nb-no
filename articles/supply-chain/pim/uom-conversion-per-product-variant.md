---
title: Konvertering av måleenhet per produktvariant
description: Dette emnet forklarer hvordan du definerer måleenhetskonverteringer for produktvarianter. Det inneholder et eksempel på oppsettet.
author: johanhoffmann
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 71d35d47a703f0931ba3b4ab5df21c7199c7ea5b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434696"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="bb6d3-104">Konvertering av måleenhet per produktvariant</span><span class="sxs-lookup"><span data-stu-id="bb6d3-104">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb6d3-105">Dette emnet forklarer hvordan du konfigurerer måleenhetskonverteringer for ulike produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-105">This topic explains how to set up unit of measure conversions for various product variants.</span></span>

<span data-ttu-id="bb6d3-106">I stedet for å opprette flere individuelle produkter som må vedlikeholdes, kan du bruke produktvarianter til å opprette variasjoner av ett produkt.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-106">Instead of creating multiple individual products that must be maintained, you can use product variants to create variations of a single product.</span></span> <span data-ttu-id="bb6d3-107">En produktvariant kan for eksempel være en T-skjorte av en gitt størrelse og farge.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-107">For example, a product variant might be a T-shirt of a given size and color.</span></span>

<span data-ttu-id="bb6d3-108">Tidligere kunne enhetskonverteringer bare defineres for produktstandarden.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-108">Previously, unit conversions could be set up only on the product master.</span></span> <span data-ttu-id="bb6d3-109">Derfor har alle produktvarianter samme enhetskonverteringsregler.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-109">Therefore, all product variants had the same unit conversion rules.</span></span> <span data-ttu-id="bb6d3-110">Når funksjonen *Måleenhetskonverteringer for produktvarianter* er aktivert, kan du nå definere enhetskonverteringer mellom de forskjellige skjortenes størrelser og boksene som brukes for pakking, hvis T-skjorter blir solgt i bokser, og antall t-skjorter som kan pakkes i en boks, avhenger av størrelsen på t-skjorter.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-110">However, when the *Unit of measure conversions for product variants* feature is turned on, if your T-shirts are sold in boxes, and the number of T-shirts that can be packed in a box depends on the size of the T-shirts, you can now set up unit conversions between the different shirt sizes and the boxes that are used for packaging.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="bb6d3-111">Aktivere funksjonen i systemet</span><span class="sxs-lookup"><span data-stu-id="bb6d3-111">Turn on the feature in your system</span></span>

<span data-ttu-id="bb6d3-112">Hvis du ikke allerede ser denne funksjonen i systemet, kan du gå til [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funksjonen *Måleenhetskonverteringer for produktvarianter*.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-112">If you don't already see this feature in your system, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Unit of measure conversions for product variants* feature.</span></span>

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="bb6d3-113">Definere et produkt for enhetsomregning per variant</span><span class="sxs-lookup"><span data-stu-id="bb6d3-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="bb6d3-114">Produktvarianter kan opprettes bare for produkter som er produktstandarder.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-114">Product variants can be created only for products that are product masters.</span></span> <span data-ttu-id="bb6d3-115">Hvis du vil ha mer informasjon, kan du se [Opprette en produktstandard](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="bb6d3-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span> <span data-ttu-id="bb6d3-116">Funksjonen *Måleenhetskonverteringer for produktvarianter* er ikke tilgjengelig for produkter som er definert for faktisk vekt-prosesser.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-116">The *Unit of measure conversions for product variants* feature isn't available for products that are set up for catch-weight processes.</span></span>

<span data-ttu-id="bb6d3-117">Hvis du vil konfigurere en produktstandard til å støtte enhetskonvertering per variant, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-117">To configure a product master to support unit conversion per variant, follow these steps.</span></span>

1. <span data-ttu-id="bb6d3-118">Gå til **Behandling av produktinformasjon \> Produkter \> Produktstandarder**.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-118">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="bb6d3-119">Opprett eller åpne en produktstandard for å gå til siden **Produktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-119">Create or open a product master to go to its **Product details** page.</span></span>
1. <span data-ttu-id="bb6d3-120">Sett alternativet **Aktiver måleenhetskonverteringer** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-120">Set the **Enable unit of measure conversions** option to *Yes*.</span></span>
1. <span data-ttu-id="bb6d3-121">I gruppen **Oppsett** i kategorien **Produkt** i handlingsruten velger du **Enhetskonverteringer**.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-121">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Unit conversions**.</span></span>
1. <span data-ttu-id="bb6d3-122">Siden **Enhetskonverteringer** åpnes.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-122">The **Unit conversions** page opens.</span></span> <span data-ttu-id="bb6d3-123">Velg én av følgende kategorier:</span><span class="sxs-lookup"><span data-stu-id="bb6d3-123">Select one of the following tabs:</span></span>

    - <span data-ttu-id="bb6d3-124">**Klasseinterne konverteringer** – Velg denne kategorien for å konvertere mellom enheter som tilhører den samme enhetsklassen.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-124">**Intra-class conversions** – Select this tab to convert between units that belong to the same unit class.</span></span>
    - <span data-ttu-id="bb6d3-125">**Mellomklassekonverteringer** – Velg denne kategorien for å konvertere mellom enheter som tilhører ulike klasser.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-125">**Inter-class conversions** – Select this tab to convert between units that belong to different unit classes.</span></span>

1. <span data-ttu-id="bb6d3-126">Velg **Ny** for å legge til en ny enhetskonvertering.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-126">Select **New** to add a new unit conversion.</span></span>
1. <span data-ttu-id="bb6d3-127">Sett feltet **Opprett konvertering for** til én av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="bb6d3-127">Set the **Create conversion for** field to one of the following values:</span></span>

    - <span data-ttu-id="bb6d3-128">**Produkt** – Hvis du velger denne verdien, kan du definere en enhetskonvertering for produktstandarden.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-128">**Product** – If you select this value, you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="bb6d3-129">Denne enhetskonverteringen vil bli brukt som et tilbakefallsområde for alle produktvarianter som ingen enhetskonvertering er definert for.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-129">That unit conversion will be used as a fallback for all product variants that no unit conversion is defined for.</span></span>
    - <span data-ttu-id="bb6d3-130">**Produktvariant** – Hvis du velger denne verdien, kan du definere en enhetskonvertering for en bestemt produktvariant.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-130">**Product variant** – If you select this value, you can set up a unit conversion for a specific product variant.</span></span> <span data-ttu-id="bb6d3-131">Bruk feltet **Produktvariant** til å velge varianten.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-131">Use the **Product variant** field to select the variant.</span></span>

    ![![Legge til en ny enhetskonvertering](media/uom-new-conversion.png "Legge til en ny enhetskonvertering")](media/uom-new-conversion.png "Adding a new unit conversion")

1. <span data-ttu-id="bb6d3-133">Bruk de andre feltene som finnes, til å definere enhetskonverteringen.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-133">Use the other fields that are provided to set up your unit conversion.</span></span>
1. <span data-ttu-id="bb6d3-134">Velg **OK** for å lagre den nye enhetskonverteringen.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-134">Select **OK** to save the new unit conversion.</span></span>

> [!TIP]
> <span data-ttu-id="bb6d3-135">Du kan åpne siden **Enhetskonverteringer** for et produkt eller en produktvariant fra følgende sider:</span><span class="sxs-lookup"><span data-stu-id="bb6d3-135">You can open the **Unit conversions** page for a product or a product variant from any of the following pages:</span></span>
> 
> - <span data-ttu-id="bb6d3-136">Produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="bb6d3-136">Product details</span></span>
> - <span data-ttu-id="bb6d3-137">Detaljer om frigitt produkt</span><span class="sxs-lookup"><span data-stu-id="bb6d3-137">Released products details</span></span>
> - <span data-ttu-id="bb6d3-138">Frigitte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="bb6d3-138">Released product variants</span></span>

## <a name="example-scenario"></a><span data-ttu-id="bb6d3-139">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="bb6d3-139">Example scenario</span></span>

<span data-ttu-id="bb6d3-140">I dette  selger et firma T-skjerer i størrelsene Liten, Middels, Stor og Ekstra stor.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-140">In this scenario, a company sells T-shirts in sizes small, medium, large, and extra-large.</span></span> <span data-ttu-id="bb6d3-141">T-skjorten er definert som et produkt, og de ulike størrelsene er definert som varianter av det produktet.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-141">The T-shirt is defined as a product, and the different sizes are defined as variants of that product.</span></span> <span data-ttu-id="bb6d3-142">T-skjortene er pakket i bokser.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-142">The shirts are packed in boxes.</span></span> <span data-ttu-id="bb6d3-143">Når det gjelder størrelsene Liten, Middels og Stor, kan det være fem T-skjorter i hver boks.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-143">For sizes small, medium, and large, there can be five shirts in each box.</span></span> <span data-ttu-id="bb6d3-144">Hvis størrelsen er Ekstra stor, er det imidlertid bare plass til fire t-skjorter i hver boks.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-144">However, for size extra-large, there is space for only four shirts in each box.</span></span>

<span data-ttu-id="bb6d3-145">Firmaet ønsker å spore de ulike variantene av t-skjorter i enheten *Stykker*, men selger dem i *Boks*-enheter.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-145">The company wants to track the different variants in the *Pieces* unit, but it's selling them in the *Boxes* unit.</span></span> <span data-ttu-id="bb6d3-146">For størrelsene Liten, Middels og Stor, er konverteringen mellom lagerenheten og salgsenheten 1 boks = 5 stykker.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-146">For sizes small, medium, and large, the conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces.</span></span> <span data-ttu-id="bb6d3-147">Når størrelsen er Ekstra stor, er konverteringen 1 boks = 4 stykker.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-147">For size extra-large, the conversion is 1 Box = 4 Pieces.</span></span>

1. <span data-ttu-id="bb6d3-148">Fra siden **Detaljer om frigitt produkt** for produktet **T-skjorte** åpner du siden **Enhetskonverteringer**.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-148">From the **Released product details** page for the **T-Shirt** product, open the **Unit conversions** page.</span></span>
1. <span data-ttu-id="bb6d3-149">På siden **Enhetskonverteringer** definerer du følgende enhetskonvertering for den frigitte produktvarianten **Ekstra stor**.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-149">On the **Unit conversions** page, set up the following unit conversion for the **X-Large** released product variant.</span></span>

    | <span data-ttu-id="bb6d3-150">Felt</span><span class="sxs-lookup"><span data-stu-id="bb6d3-150">Field</span></span>                 | <span data-ttu-id="bb6d3-151">Innstilling</span><span class="sxs-lookup"><span data-stu-id="bb6d3-151">Setting</span></span>                 |
    |-----------------------|-------------------------|
    | <span data-ttu-id="bb6d3-152">Opprett konvertering for</span><span class="sxs-lookup"><span data-stu-id="bb6d3-152">Create conversion for</span></span> | <span data-ttu-id="bb6d3-153">Produktvariant</span><span class="sxs-lookup"><span data-stu-id="bb6d3-153">Product variant</span></span>         |
    | <span data-ttu-id="bb6d3-154">Produktvariant</span><span class="sxs-lookup"><span data-stu-id="bb6d3-154">Product variant</span></span>       | <span data-ttu-id="bb6d3-155">T-skjorte : : Ekstra stor : :</span><span class="sxs-lookup"><span data-stu-id="bb6d3-155">T-Shirt : : X-Large : :</span></span> |
    | <span data-ttu-id="bb6d3-156">Fra enhet</span><span class="sxs-lookup"><span data-stu-id="bb6d3-156">From unit</span></span>             | <span data-ttu-id="bb6d3-157">Bokser</span><span class="sxs-lookup"><span data-stu-id="bb6d3-157">Boxes</span></span>                   |
    | <span data-ttu-id="bb6d3-158">Faktor</span><span class="sxs-lookup"><span data-stu-id="bb6d3-158">Factor</span></span>                | <span data-ttu-id="bb6d3-159">4</span><span class="sxs-lookup"><span data-stu-id="bb6d3-159">4</span></span>                       |
    | <span data-ttu-id="bb6d3-160">Til enhet</span><span class="sxs-lookup"><span data-stu-id="bb6d3-160">To Unit</span></span>               | <span data-ttu-id="bb6d3-161">Stykker</span><span class="sxs-lookup"><span data-stu-id="bb6d3-161">Pieces</span></span>                  |

1. <span data-ttu-id="bb6d3-162">Ettersom produktvariantene **Liten**, **Middels** og **Stor** har samme enhetskonvertering mellom *Boks*- og *Stykker*-enhetene, kan du definere følgende enhetskonvertering for dem i produktstandarden.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-162">Because the **Small**, **Medium**, and **Large** product variants all have the same unit conversion between the *Box* and *Pieces* units, you can define the following unit conversion for them on the product master.</span></span>

    | <span data-ttu-id="bb6d3-163">Felt</span><span class="sxs-lookup"><span data-stu-id="bb6d3-163">Field</span></span>                 | <span data-ttu-id="bb6d3-164">Innstilling</span><span class="sxs-lookup"><span data-stu-id="bb6d3-164">Setting</span></span> |
    |-----------------------|---------|
    | <span data-ttu-id="bb6d3-165">Opprett konvertering for</span><span class="sxs-lookup"><span data-stu-id="bb6d3-165">Create conversion for</span></span> | <span data-ttu-id="bb6d3-166">Produkt</span><span class="sxs-lookup"><span data-stu-id="bb6d3-166">Product</span></span> |
    | <span data-ttu-id="bb6d3-167">Produkt</span><span class="sxs-lookup"><span data-stu-id="bb6d3-167">Product</span></span>               | <span data-ttu-id="bb6d3-168">T-skjorte</span><span class="sxs-lookup"><span data-stu-id="bb6d3-168">T-Shirt</span></span> |
    | <span data-ttu-id="bb6d3-169">Fra enhet</span><span class="sxs-lookup"><span data-stu-id="bb6d3-169">From unit</span></span>             | <span data-ttu-id="bb6d3-170">Bokser</span><span class="sxs-lookup"><span data-stu-id="bb6d3-170">Boxes</span></span>   |
    | <span data-ttu-id="bb6d3-171">Omregningsfaktor</span><span class="sxs-lookup"><span data-stu-id="bb6d3-171">Factor</span></span>                | <span data-ttu-id="bb6d3-172">5</span><span class="sxs-lookup"><span data-stu-id="bb6d3-172">5</span></span>       |
    | <span data-ttu-id="bb6d3-173">Til enhet</span><span class="sxs-lookup"><span data-stu-id="bb6d3-173">To Unit</span></span>               | <span data-ttu-id="bb6d3-174">Stykker</span><span class="sxs-lookup"><span data-stu-id="bb6d3-174">Pieces</span></span>  |

## <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="bb6d3-175">Bruke Excel til å oppdatere enhetsomregningene</span><span class="sxs-lookup"><span data-stu-id="bb6d3-175">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="bb6d3-176">Hvis et produkt har mange produktvarianter som har ulike enhetskonverteringer, kan det være lurt å eksportere enhetskonverteringene til en arbeidsbok i Microsoft Excel, oppdatere dem og deretter publisere dem tilbake til Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-176">If a product has many product variants that have different unit conversions, it's a good idea to export the unit conversions to a Microsoft Excel workbook, update them, and then publish them back to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="bb6d3-177">Hvis du vil eksportere enhetskonverteringer til Excel, velger du **Åpne i Microsoft Office** på siden **Enhetskonverteringer**.</span><span class="sxs-lookup"><span data-stu-id="bb6d3-177">To export unit conversions to Excel, on the **Unit conversions** page, on the Action Pane, select **Open in Microsoft Office**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb6d3-178">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="bb6d3-178">Additional resources</span></span>

[<span data-ttu-id="bb6d3-179">Administrere måleenhet</span><span class="sxs-lookup"><span data-stu-id="bb6d3-179">Manage unit of measure</span></span>](tasks/manage-unit-measure.md)
