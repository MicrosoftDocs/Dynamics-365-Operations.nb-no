---
title: Opprette et nytt produkt
description: Dette emnet beskriver hvordan du oppretter et nytt produkt i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 356bf91b2a946e7c0f5d5af9e2fe0b64342b856e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001973"
---
# <a name="create-a-new-product"></a><span data-ttu-id="49dfc-103">Opprette et nytt produkt</span><span class="sxs-lookup"><span data-stu-id="49dfc-103">Create a new product</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="49dfc-104">Dette emnet beskriver hvordan du oppretter et nytt produkt i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="49dfc-104">This topic describes how to create a new product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="49dfc-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="49dfc-105">Overview</span></span>

<span data-ttu-id="49dfc-106">Et produkt er først og fremst definert av produktnummer, navn og beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="49dfc-106">A product is primarily defined by a product number, name, and description.</span></span> <span data-ttu-id="49dfc-107">Andre data er imidlertid også nødvendig for å beskrive et produkt eller en tjeneste:</span><span class="sxs-lookup"><span data-stu-id="49dfc-107">However, other data is also required in order to describe a product or service:</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="49dfc-108">Opprette et nytt produkt</span><span class="sxs-lookup"><span data-stu-id="49dfc-108">Create a new product</span></span>

1. <span data-ttu-id="49dfc-109">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Produkter og kategorier \> Produkter etter kategori**.</span><span class="sxs-lookup"><span data-stu-id="49dfc-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Products by category**.</span></span>
1. <span data-ttu-id="49dfc-110">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="49dfc-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="49dfc-111">I **Produkttype**-rullegardinlisten velger du **Element** eller **Tjeneste**.</span><span class="sxs-lookup"><span data-stu-id="49dfc-111">In the **Product type** drop-down list, select either **Item** or **Service**.</span></span>
1. <span data-ttu-id="49dfc-112">I **Produktundertype**-rullegardinlisten velger du **Produkt** (hvis produktet ikke har noen varianter) eller **Produktstandard** (hvis produktet kommer til å ha varianter).</span><span class="sxs-lookup"><span data-stu-id="49dfc-112">In the **Product subtype** drop-down list, select either **Product** (if the product will have no variants) or **Product master** (if the product will have variants).</span></span>
1. <span data-ttu-id="49dfc-113">I **Produktnummer**-boksen angir du et produktnummer hvis det ikke allerede er forhåndsutfylt.</span><span class="sxs-lookup"><span data-stu-id="49dfc-113">In the **Product number** box, enter a product number if one is not already prepopulated.</span></span>
1. <span data-ttu-id="49dfc-114">I **Produktnavn**-boksen angir du et produktnavn.</span><span class="sxs-lookup"><span data-stu-id="49dfc-114">In the **Product name** box, enter a product name.</span></span>
1. <span data-ttu-id="49dfc-115">I **Søk etter navn**-boksen angir du et søkenavn.</span><span class="sxs-lookup"><span data-stu-id="49dfc-115">In the **Search name** box, enter a search name.</span></span>
1. <span data-ttu-id="49dfc-116">I **Handelskategori**-rullegardinlisten velger du en passende kategori.</span><span class="sxs-lookup"><span data-stu-id="49dfc-116">In the **Retail category** drop-down list, select an appropriate category.</span></span>
1. <span data-ttu-id="49dfc-117">Hvis produktet er et sett, velger du **Ja** for **Produktsett**.</span><span class="sxs-lookup"><span data-stu-id="49dfc-117">If the product is a kit, select **Yes** for **Product kit**.</span></span>
1. <span data-ttu-id="49dfc-118">Hvis produktundertypen er produktstandard, setter du **Produktdimensjonsgruppe** til å inkludere de støttede variantene.</span><span class="sxs-lookup"><span data-stu-id="49dfc-118">If the product subtype is product master, set the **Product dimension group** to include the supported variants.</span></span> <span data-ttu-id="49dfc-119">Alternativene inkluderer **Farge**, **Størrelse**, **Stil** og **Konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="49dfc-119">Options include **Color**, **Size**, **Style**, and **Configuration**.</span></span> <span data-ttu-id="49dfc-120">Det er mulig at du om nødvendig må opprette flere produktdimensjonsgrupper.</span><span class="sxs-lookup"><span data-stu-id="49dfc-120">You may need to create additional product dimension groups if needed.</span></span>
1. <span data-ttu-id="49dfc-121">I **Konfigurasjonsteknologi**-rullegardinlisten velger du et passende alternativ.</span><span class="sxs-lookup"><span data-stu-id="49dfc-121">In the **Configuration technology** drop-down list, select an appropriate option.</span></span>
1. <span data-ttu-id="49dfc-122">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="49dfc-122">Select **OK**.</span></span>

<span data-ttu-id="49dfc-123">Følgende bilde viser et eksempelprodukt som legges til.</span><span class="sxs-lookup"><span data-stu-id="49dfc-123">The following image shows an example product being added.</span></span>

![Opprette et produkt](media/create-new-product.png)

<span data-ttu-id="49dfc-125">Når et produkt er lagt til, kan ekstra data angis for det, for eksempel **Produktbeskrivelse**, **Variantgrupper**, **Dimensjonsgrupper**, **Produktattributter** og **Relaterte produkter**.</span><span class="sxs-lookup"><span data-stu-id="49dfc-125">Once a product is added, additional data can be set for it, such as **Product description**, **Variant groups**, **Dimension groups**, **Product attributes**, and **Related products**.</span></span>

<span data-ttu-id="49dfc-126">Det følgende bildet viser flere detaljer for produktet.</span><span class="sxs-lookup"><span data-stu-id="49dfc-126">The following image shows a product's additional details.</span></span>

![Produktdetaljer](media/create-new-product-2.png)

### <a name="create-product-variants"></a><span data-ttu-id="49dfc-128">Opprett produktvarianter</span><span class="sxs-lookup"><span data-stu-id="49dfc-128">Create product variants</span></span>

<span data-ttu-id="49dfc-129">Hvis produktundertypen er **Produktstandard**, må spesifikke varianter opprettes.</span><span class="sxs-lookup"><span data-stu-id="49dfc-129">If the product subtype is **Product master**, specific variants will need to be created.</span></span> 

<span data-ttu-id="49dfc-130">Hvis du vil opprette produktvarianter, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="49dfc-130">To create product variants, follow these steps.</span></span>

1. <span data-ttu-id="49dfc-131">I handlingsruten velger du **Produktvarianter**.</span><span class="sxs-lookup"><span data-stu-id="49dfc-131">On the action pane, select **Product variants**.</span></span>
1. <span data-ttu-id="49dfc-132">Hvis variantgrupper er valgt i handlingsruten, velger du \**Variantforslag*.</span><span class="sxs-lookup"><span data-stu-id="49dfc-132">If variant groups have been selected on the action pane, select \**Variant suggestions*.</span></span>
1. <span data-ttu-id="49dfc-133">Velg variantene du vil støtte for produktet.</span><span class="sxs-lookup"><span data-stu-id="49dfc-133">Select the variants you would like to support for the product.</span></span>
1. <span data-ttu-id="49dfc-134">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="49dfc-134">Select **Create**.</span></span>

## <a name="release-a-product"></a><span data-ttu-id="49dfc-135">Frigi et produkt</span><span class="sxs-lookup"><span data-stu-id="49dfc-135">Release a product</span></span>

<span data-ttu-id="49dfc-136">Hvis du vil selge et produkt, må det først frigis til en juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="49dfc-136">To sell a product it must first be released to a legal entity.</span></span>

1. <span data-ttu-id="49dfc-137">Fra produktsiden velger du **Frigi produkter**.</span><span class="sxs-lookup"><span data-stu-id="49dfc-137">From the product page, select **Release products**.</span></span>

    ![Frigi produkt](media/create-new-product-3.png)

1. <span data-ttu-id="49dfc-139">Velg produktet som skal frigis, og velg deretter **Neste**.</span><span class="sxs-lookup"><span data-stu-id="49dfc-139">Select the product to release, and then select **Next**.</span></span>

    ![Velg produktet som skal frigis](media/create-new-product-4.png)

1. <span data-ttu-id="49dfc-141">Velg produktvariantsettet som skal frigis, og velg deretter **Neste**.</span><span class="sxs-lookup"><span data-stu-id="49dfc-141">Select the set of product variants to release, and then select **Next**.</span></span>

    ![Velg variantene som skal frigis](media/create-new-product-5.png)

1. <span data-ttu-id="49dfc-143">Velg den juridiske enheten, og velg deretter **Neste**.</span><span class="sxs-lookup"><span data-stu-id="49dfc-143">Select the legal entity, and then select **Next**.</span></span>

    ![Velg juridisk enhet](media/create-new-product-6.png)

1. <span data-ttu-id="49dfc-145">Velg **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="49dfc-145">Select **Finish**.</span></span>

    ![Avslutte produktfrigivelse](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a><span data-ttu-id="49dfc-147">Konfigurer et frigitt produkt</span><span class="sxs-lookup"><span data-stu-id="49dfc-147">Configure a released product</span></span>

<span data-ttu-id="49dfc-148">Når et produkt er frigitt, vil det kreve ytterligere konfigurasjon som omfatter tilføying av en pris for produktet.</span><span class="sxs-lookup"><span data-stu-id="49dfc-148">Once a product is released, it will then require further configuration that includes adding a price to the product.</span></span>

1. <span data-ttu-id="49dfc-149">I navigasjonsruten går du til **Moduler \> Handel og detaljhandel \> Produkter og kategorier \> Frigitte produkter etter kategori**.</span><span class="sxs-lookup"><span data-stu-id="49dfc-149">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="49dfc-150">Velg produktkategorinoden for produktet som ble frigitt, og velg deretter produktet fra produktlisten.</span><span class="sxs-lookup"><span data-stu-id="49dfc-150">Select the product category node for the product that was released, and then select the product from the product list.</span></span>
1. <span data-ttu-id="49dfc-151">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="49dfc-151">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="49dfc-152">I **Kjøp**-delen konfigurerer du eventuelle påkrevde egenskaper, inkludert **Enhet**, **Pris** og **Antall**.</span><span class="sxs-lookup"><span data-stu-id="49dfc-152">In the **Purchase** section, configure any required properties including **Unit**, **Price**,  and **Quantity**.</span></span>
1. <span data-ttu-id="49dfc-153">I handlingsruten velger du **Valider** for å sikre at det ikke rapporteres noen feil for manglende felt.</span><span class="sxs-lookup"><span data-stu-id="49dfc-153">On the action pane, select **Validate** to ensure that no errors are reported for missing fields.</span></span>
1. <span data-ttu-id="49dfc-154">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="49dfc-154">On the action pane, select **Save**.</span></span>

<span data-ttu-id="49dfc-155">Bildet nedenfor viser en eksempelkonfigurasjon for et frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="49dfc-155">The following image shows an example configuration for a released product.</span></span>

![Konfigurere et frigitt produkt](media/create-new-product-8.png)

## <a name="additional-resources"></a><span data-ttu-id="49dfc-157">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="49dfc-157">Additional resources</span></span>

[<span data-ttu-id="49dfc-158">Opprett juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="49dfc-158">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="49dfc-159">Opprette en variantgruppe</span><span class="sxs-lookup"><span data-stu-id="49dfc-159">Create a variant group</span></span>](create-variant-group.md) 
