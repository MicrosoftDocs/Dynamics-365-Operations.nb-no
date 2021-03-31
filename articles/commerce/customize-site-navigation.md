---
title: Tilpasse områdenavigering
description: Dette emnet beskriver hvordan du oppretter et tilpasset elektronisk navigasjonshierarki for å organisere produktene for weblesing på området i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cfd0a9559eb2b596adb822b228929e6855711bb4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222615"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="51d36-103">Tilpasse områdenavigering</span><span class="sxs-lookup"><span data-stu-id="51d36-103">Customize site navigation</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="51d36-104">Dette emnet beskriver hvordan du oppretter et tilpasset elektronisk navigasjonshierarki for å organisere produktene for weblesing på området i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="51d36-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="51d36-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="51d36-105">Overview</span></span>

<span data-ttu-id="51d36-106">Nettbutikkfasader lar vanligvis kunder oppdage og bla gjennom produkter ved å navigere gjennom produktkategorier.</span><span class="sxs-lookup"><span data-stu-id="51d36-106">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="51d36-107">Denne funksjonen finnes vanligvis ved hjelp av kategorier øverst på siden eller ved hjelp av et navigasjonsfelt på venstre side.</span><span class="sxs-lookup"><span data-stu-id="51d36-107">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="51d36-108">I Dynamics 365 Commerce kan du opprette og behandle hierarkistrukturen for kategorinavigasjonen og produktene som er inkludert i de ulike kategoriene.</span><span class="sxs-lookup"><span data-stu-id="51d36-108">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="51d36-109">Opprette et kanalnavigasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="51d36-109">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="51d36-110">Følg denne fremgangsmåten for å opprette et kanalnavigasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="51d36-110">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="51d36-111">Gå til **Detaljhandel og handel \> Produkter og kategorier \> Kategori- og produktadministrering**.</span><span class="sxs-lookup"><span data-stu-id="51d36-111">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="51d36-112">Velg **Kategorihierarkier**, og velg deretter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="51d36-112">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="51d36-113">Gi hierarkiet et navn.</span><span class="sxs-lookup"><span data-stu-id="51d36-113">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="51d36-114">Den øverste kategorien som du oppretter, er rotkategorinoden.</span><span class="sxs-lookup"><span data-stu-id="51d36-114">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="51d36-115">Den vises ikke på området.</span><span class="sxs-lookup"><span data-stu-id="51d36-115">It won't be shown on your site.</span></span> <span data-ttu-id="51d36-116">Hvis du vil opprette et kategorihierarki der en enkelt node på øverste nivå vises på området, oppretter og navngir du kategorien som et underordnet objekt av rotkategorien.</span><span class="sxs-lookup"><span data-stu-id="51d36-116">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="51d36-117">Velg **Ny kategorinode**, og gi kategorien et navn.</span><span class="sxs-lookup"><span data-stu-id="51d36-117">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="51d36-118">Fortsett å opprette likestilte og underordnede kategorier etter behov.</span><span class="sxs-lookup"><span data-stu-id="51d36-118">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="51d36-119">Du kan nå tilordne produkter til hver kategori du opprettet under kategorien på toppnivå.</span><span class="sxs-lookup"><span data-stu-id="51d36-119">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="51d36-120">Tilpasse rekkefølgen på kategorier</span><span class="sxs-lookup"><span data-stu-id="51d36-120">Customize the order of categories</span></span>

<span data-ttu-id="51d36-121">Som standard vises kategoriene du definerer, i alfabetisk rekkefølge på området.</span><span class="sxs-lookup"><span data-stu-id="51d36-121">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="51d36-122">Du kan imidlertid også tilpasse visningsrekkefølgen for kategorier.</span><span class="sxs-lookup"><span data-stu-id="51d36-122">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="51d36-123">Tilordne en kategorihierarkitype</span><span class="sxs-lookup"><span data-stu-id="51d36-123">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="51d36-124">Gå til **Detaljhandel og handel \> Produkter og kategorier \> Kategori- og produktadministrering**.</span><span class="sxs-lookup"><span data-stu-id="51d36-124">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="51d36-125">Velg **Kategorihierarkier**.</span><span class="sxs-lookup"><span data-stu-id="51d36-125">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="51d36-126">I handlingsruten, i kategorien **Kategorihierarki** i gruppen **Oppsett** velger du **Tilknytt hierarkitype**.</span><span class="sxs-lookup"><span data-stu-id="51d36-126">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="51d36-127">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="51d36-127">Select **New**.</span></span>
1. <span data-ttu-id="51d36-128">I feltet **Kategorihierarkitype** velger du **Kanalnavigasjonshierarki**.</span><span class="sxs-lookup"><span data-stu-id="51d36-128">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="51d36-129">I feltet **Kategorihierarki** velger du kanalnavigeringshierarkiet du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="51d36-129">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="51d36-130">Publisere nye eller oppdaterte navigasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="51d36-130">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="51d36-131">Følg denne fremgangsmåten for å gjøre navigasjonshierarkiet tilgjengelig for nettbutikkfasaden.</span><span class="sxs-lookup"><span data-stu-id="51d36-131">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="51d36-132">Gå til **Detaljhandel og handel \> Kanaloppsett \> Kanalkategorier og produktattributter**.</span><span class="sxs-lookup"><span data-stu-id="51d36-132">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="51d36-133">Velg nettbutikken i treet til venstre.</span><span class="sxs-lookup"><span data-stu-id="51d36-133">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="51d36-134">Velg **Publiser kanaloppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="51d36-134">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="51d36-135">Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="51d36-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="51d36-136">Finn og velg **Jobb 1040** i listen.</span><span class="sxs-lookup"><span data-stu-id="51d36-136">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="51d36-137">Velg **Kjør nå**.</span><span class="sxs-lookup"><span data-stu-id="51d36-137">Select **Run now**.</span></span>
1. <span data-ttu-id="51d36-138">Gjenta trinn 5 og 6 for jobbene 1070 og 1150.</span><span class="sxs-lookup"><span data-stu-id="51d36-138">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="51d36-139">Vise kategorier på området</span><span class="sxs-lookup"><span data-stu-id="51d36-139">Show categories on your site</span></span>

<span data-ttu-id="51d36-140">Hvis du vil vise kategorihierarkiet i nettbutikkfasaden, må du legge til navigasjonsmenymodulen på riktig sted i en mal eller et fragment.</span><span class="sxs-lookup"><span data-stu-id="51d36-140">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="51d36-141">Navigasjonsmenymodulen vil deretter vise navigasjonshierarkiet, forutsatt at du har publisert navigasjonshierarkiet til kanalen som området er bundet til.</span><span class="sxs-lookup"><span data-stu-id="51d36-141">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="51d36-142">Navigasjonsmenymodulen som er inkludert i modulbiblioteket, gjør at brukere bare kan navigere til kategorier som ikke har underkategorier.</span><span class="sxs-lookup"><span data-stu-id="51d36-142">The navigation menu module that is included in the module library lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="51d36-143">Hvis kundene skal kunne navigere til kategorier som har underkategorier, må du tilpasse navigasjonsmenymodulen.</span><span class="sxs-lookup"><span data-stu-id="51d36-143">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="51d36-144">Legge til egendefinerte navigasjonsalternativer</span><span class="sxs-lookup"><span data-stu-id="51d36-144">Add custom navigation options</span></span>

<span data-ttu-id="51d36-145">Du kan legge til navigasjonsalternativer som ikke er en del av produktkategorihierarkiet, på navigasjonsmenyen.</span><span class="sxs-lookup"><span data-stu-id="51d36-145">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="51d36-146">På slutten av listen over produktkategorier kan du for eksempel legge til en **Kontakt oss**-vare som peker til en kontaktside som du har bygget for området.</span><span class="sxs-lookup"><span data-stu-id="51d36-146">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="51d36-147">Hvis du vil legge til egendefinerte navigasjonsalternativer i navigasjonsmenyen, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="51d36-147">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="51d36-148">I malen eller fragmentet som du vil tilpasse, velger du navigasjonsmenymodulen.</span><span class="sxs-lookup"><span data-stu-id="51d36-148">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="51d36-149">I egenskapsruten i kategorien **Data** velger **Legg til vare** for å opprette et nytt navigasjonselement for innholdsbehandlingssystem (CMS).</span><span class="sxs-lookup"><span data-stu-id="51d36-149">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="51d36-150">Angi koblingstekst og en URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="51d36-150">Enter link text and a URL.</span></span>
1. <span data-ttu-id="51d36-151">Gjenta trinn 2 og 3 for å legge til flere egendefinerte navigasjonsalternativer.</span><span class="sxs-lookup"><span data-stu-id="51d36-151">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="51d36-152">Når du er ferdig, velger du **Lagre** for å lagre malen eller fragmentet, og velg deretter **Fullfør redigering** for å sjekke den inn.</span><span class="sxs-lookup"><span data-stu-id="51d36-152">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51d36-153">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="51d36-153">Additional resources</span></span>

[<span data-ttu-id="51d36-154">Oversikt over maler og oppsett</span><span class="sxs-lookup"><span data-stu-id="51d36-154">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="51d36-155">Arbeide med maler</span><span class="sxs-lookup"><span data-stu-id="51d36-155">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="51d36-156">Arbeide med forhåndsinnstilte oppsett</span><span class="sxs-lookup"><span data-stu-id="51d36-156">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="51d36-157">Arbeide med fragmenter</span><span class="sxs-lookup"><span data-stu-id="51d36-157">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="51d36-158">Arbeide med moduler</span><span class="sxs-lookup"><span data-stu-id="51d36-158">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="51d36-159">Opprette en URL-adresse for side</span><span class="sxs-lookup"><span data-stu-id="51d36-159">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="51d36-160">Arbeide med publiseringsgrupper</span><span class="sxs-lookup"><span data-stu-id="51d36-160">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]