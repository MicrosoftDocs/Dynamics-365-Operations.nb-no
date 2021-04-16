---
title: Tilpasse områdenavigering
description: Dette emnet beskriver hvordan du oppretter et tilpasset elektronisk navigasjonshierarki for å organisere produktene for weblesing på området i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5bc50243ac3845adc60bfc173fc532fb28f3cdf6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799355"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="955c9-103">Tilpasse områdenavigering</span><span class="sxs-lookup"><span data-stu-id="955c9-103">Customize site navigation</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="955c9-104">Dette emnet beskriver hvordan du oppretter et tilpasset elektronisk navigasjonshierarki for å organisere produktene for weblesing på området i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="955c9-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="955c9-105">Nettbutikkfasader lar vanligvis kunder oppdage og bla gjennom produkter ved å navigere gjennom produktkategorier.</span><span class="sxs-lookup"><span data-stu-id="955c9-105">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="955c9-106">Denne funksjonen finnes vanligvis ved hjelp av kategorier øverst på siden eller ved hjelp av et navigasjonsfelt på venstre side.</span><span class="sxs-lookup"><span data-stu-id="955c9-106">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="955c9-107">I Dynamics 365 Commerce kan du opprette og behandle hierarkistrukturen for kategorinavigasjonen og produktene som er inkludert i de ulike kategoriene.</span><span class="sxs-lookup"><span data-stu-id="955c9-107">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="955c9-108">Opprette et kanalnavigasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="955c9-108">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="955c9-109">Følg denne fremgangsmåten for å opprette et kanalnavigasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="955c9-109">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="955c9-110">Gå til **Detaljhandel og handel \> Produkter og kategorier \> Kategori- og produktadministrering**.</span><span class="sxs-lookup"><span data-stu-id="955c9-110">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="955c9-111">Velg **Kategorihierarkier**, og velg deretter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="955c9-111">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="955c9-112">Gi hierarkiet et navn.</span><span class="sxs-lookup"><span data-stu-id="955c9-112">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="955c9-113">Den øverste kategorien som du oppretter, er rotkategorinoden.</span><span class="sxs-lookup"><span data-stu-id="955c9-113">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="955c9-114">Den vises ikke på området.</span><span class="sxs-lookup"><span data-stu-id="955c9-114">It won't be shown on your site.</span></span> <span data-ttu-id="955c9-115">Hvis du vil opprette et kategorihierarki der en enkelt node på øverste nivå vises på området, oppretter og navngir du kategorien som et underordnet objekt av rotkategorien.</span><span class="sxs-lookup"><span data-stu-id="955c9-115">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="955c9-116">Velg **Ny kategorinode**, og gi kategorien et navn.</span><span class="sxs-lookup"><span data-stu-id="955c9-116">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="955c9-117">Fortsett å opprette likestilte og underordnede kategorier etter behov.</span><span class="sxs-lookup"><span data-stu-id="955c9-117">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="955c9-118">Du kan nå tilordne produkter til hver kategori du opprettet under kategorien på toppnivå.</span><span class="sxs-lookup"><span data-stu-id="955c9-118">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="955c9-119">Tilpasse rekkefølgen på kategorier</span><span class="sxs-lookup"><span data-stu-id="955c9-119">Customize the order of categories</span></span>

<span data-ttu-id="955c9-120">Som standard vises kategoriene du definerer, i alfabetisk rekkefølge på området.</span><span class="sxs-lookup"><span data-stu-id="955c9-120">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="955c9-121">Du kan imidlertid også tilpasse visningsrekkefølgen for kategorier.</span><span class="sxs-lookup"><span data-stu-id="955c9-121">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="955c9-122">Tilordne en kategorihierarkitype</span><span class="sxs-lookup"><span data-stu-id="955c9-122">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="955c9-123">Gå til **Detaljhandel og handel \> Produkter og kategorier \> Kategori- og produktadministrering**.</span><span class="sxs-lookup"><span data-stu-id="955c9-123">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="955c9-124">Velg **Kategorihierarkier**.</span><span class="sxs-lookup"><span data-stu-id="955c9-124">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="955c9-125">I handlingsruten, i kategorien **Kategorihierarki** i gruppen **Oppsett** velger du **Tilknytt hierarkitype**.</span><span class="sxs-lookup"><span data-stu-id="955c9-125">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="955c9-126">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="955c9-126">Select **New**.</span></span>
1. <span data-ttu-id="955c9-127">I feltet **Kategorihierarkitype** velger du **Kanalnavigasjonshierarki**.</span><span class="sxs-lookup"><span data-stu-id="955c9-127">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="955c9-128">I feltet **Kategorihierarki** velger du kanalnavigeringshierarkiet du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="955c9-128">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="955c9-129">Publisere nye eller oppdaterte navigasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="955c9-129">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="955c9-130">Følg denne fremgangsmåten for å gjøre navigasjonshierarkiet tilgjengelig for nettbutikkfasaden.</span><span class="sxs-lookup"><span data-stu-id="955c9-130">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="955c9-131">Gå til **Detaljhandel og handel \> Kanaloppsett \> Kanalkategorier og produktattributter**.</span><span class="sxs-lookup"><span data-stu-id="955c9-131">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="955c9-132">Velg nettbutikken i treet til venstre.</span><span class="sxs-lookup"><span data-stu-id="955c9-132">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="955c9-133">Velg **Publiser kanaloppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="955c9-133">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="955c9-134">Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="955c9-134">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="955c9-135">Finn og velg **Jobb 1040** i listen.</span><span class="sxs-lookup"><span data-stu-id="955c9-135">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="955c9-136">Velg **Kjør nå**.</span><span class="sxs-lookup"><span data-stu-id="955c9-136">Select **Run now**.</span></span>
1. <span data-ttu-id="955c9-137">Gjenta trinn 5 og 6 for jobbene 1070 og 1150.</span><span class="sxs-lookup"><span data-stu-id="955c9-137">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="955c9-138">Vise kategorier på området</span><span class="sxs-lookup"><span data-stu-id="955c9-138">Show categories on your site</span></span>

<span data-ttu-id="955c9-139">Hvis du vil vise kategorihierarkiet i nettbutikkfasaden, må du legge til navigasjonsmenymodulen på riktig sted i en mal eller et fragment.</span><span class="sxs-lookup"><span data-stu-id="955c9-139">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="955c9-140">Navigasjonsmenymodulen vil deretter vise navigasjonshierarkiet, forutsatt at du har publisert navigasjonshierarkiet til kanalen som området er bundet til.</span><span class="sxs-lookup"><span data-stu-id="955c9-140">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="955c9-141">Navigasjonsmenymodulen som er inkludert i modulbiblioteket, gjør at brukere bare kan navigere til kategorier som ikke har underkategorier.</span><span class="sxs-lookup"><span data-stu-id="955c9-141">The navigation menu module that is included in the module library lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="955c9-142">Hvis kundene skal kunne navigere til kategorier som har underkategorier, må du tilpasse navigasjonsmenymodulen.</span><span class="sxs-lookup"><span data-stu-id="955c9-142">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="955c9-143">Legge til egendefinerte navigasjonsalternativer</span><span class="sxs-lookup"><span data-stu-id="955c9-143">Add custom navigation options</span></span>

<span data-ttu-id="955c9-144">Du kan legge til navigasjonsalternativer som ikke er en del av produktkategorihierarkiet, på navigasjonsmenyen.</span><span class="sxs-lookup"><span data-stu-id="955c9-144">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="955c9-145">På slutten av listen over produktkategorier kan du for eksempel legge til en **Kontakt oss**-vare som peker til en kontaktside som du har bygget for området.</span><span class="sxs-lookup"><span data-stu-id="955c9-145">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="955c9-146">Hvis du vil legge til egendefinerte navigasjonsalternativer i navigasjonsmenyen, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="955c9-146">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="955c9-147">I malen eller fragmentet som du vil tilpasse, velger du navigasjonsmenymodulen.</span><span class="sxs-lookup"><span data-stu-id="955c9-147">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="955c9-148">I egenskapsruten i kategorien **Data** velger **Legg til vare** for å opprette et nytt navigasjonselement for innholdsbehandlingssystem (CMS).</span><span class="sxs-lookup"><span data-stu-id="955c9-148">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="955c9-149">Angi koblingstekst og en URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="955c9-149">Enter link text and a URL.</span></span>
1. <span data-ttu-id="955c9-150">Gjenta trinn 2 og 3 for å legge til flere egendefinerte navigasjonsalternativer.</span><span class="sxs-lookup"><span data-stu-id="955c9-150">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="955c9-151">Når du er ferdig, velger du **Lagre** for å lagre malen eller fragmentet, og velg deretter **Fullfør redigering** for å sjekke den inn.</span><span class="sxs-lookup"><span data-stu-id="955c9-151">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="955c9-152">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="955c9-152">Additional resources</span></span>

[<span data-ttu-id="955c9-153">Oversikt over maler og oppsett</span><span class="sxs-lookup"><span data-stu-id="955c9-153">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="955c9-154">Arbeide med maler</span><span class="sxs-lookup"><span data-stu-id="955c9-154">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="955c9-155">Arbeide med forhåndsinnstilte oppsett</span><span class="sxs-lookup"><span data-stu-id="955c9-155">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="955c9-156">Arbeide med fragmenter</span><span class="sxs-lookup"><span data-stu-id="955c9-156">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="955c9-157">Arbeide med moduler</span><span class="sxs-lookup"><span data-stu-id="955c9-157">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="955c9-158">Opprette en URL-adresse for side</span><span class="sxs-lookup"><span data-stu-id="955c9-158">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="955c9-159">Arbeide med publiseringsgrupper</span><span class="sxs-lookup"><span data-stu-id="955c9-159">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
