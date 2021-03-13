---
title: Søkeresultatmodul
description: Dette emnet dekker søkeresultatmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3761be29955458099d01f2271057884fc1fd6f28
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097184"
---
# <a name="search-results-module"></a><span data-ttu-id="fead4-103">Søkeresultatmodul</span><span class="sxs-lookup"><span data-stu-id="fead4-103">Search results module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="fead4-104">Dette emnet dekker søkeresultatmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fead4-104">This topic covers search results modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fead4-105">Modulen for søkeresultater returnerer produktsøkeresultater og en liste over gjeldende presiseringer for produktene.</span><span class="sxs-lookup"><span data-stu-id="fead4-105">The search results module returns product search results and a list of applicable refiners for the products.</span></span> <span data-ttu-id="fead4-106">Søkeresultatmoduler på Dynamics 365 Commerce-områder kan brukes til å gjengi sider for følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="fead4-106">Search results modules on Dynamics 365 Commerce sites can be used to render pages for the following scenarios:</span></span>

- <span data-ttu-id="fead4-107">Søkeresultater som startes ved hjelp av et brukersøk</span><span class="sxs-lookup"><span data-stu-id="fead4-107">Search results that are initiated by a user search</span></span>
- <span data-ttu-id="fead4-108">Søkeresultater som viser et bestemt sett med produkter, for eksempel "Kjøp lignende utseende"</span><span class="sxs-lookup"><span data-stu-id="fead4-108">Search results that show a specific set of products, such as "Shop similar looks"</span></span>
- <span data-ttu-id="fead4-109">Liste over produkter som tilhører en kategori</span><span class="sxs-lookup"><span data-stu-id="fead4-109">Lists of products that belong to a category</span></span>

<span data-ttu-id="fead4-110">Hvis du vil ha mer informasjon om kategori- og søkeresultatsider, kan du se [Oversikt over standard kategorimålside og søkeresultatside](category-search-page-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fead4-110">For more information about category and search results pages, see [Default category landing page and search results page overview](category-search-page-overview.md).</span></span>

<span data-ttu-id="fead4-111">Følgende illustrasjon viser et eksempel på en søkeresultatside for en kategori på Fabrikam-området.</span><span class="sxs-lookup"><span data-stu-id="fead4-111">The following illustration shows an example of a search results page for a category on the Fabrikam site.</span></span>

![Eksempel på en søkeresultatside på Fabrikam-området](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a><span data-ttu-id="fead4-113">Egenskaper for søkeresultatmodul</span><span class="sxs-lookup"><span data-stu-id="fead4-113">Search results module properties</span></span>

<span data-ttu-id="fead4-114">I tabellen nedenfor finner du en oversikt over egenskaper for søkeresultatmoduler sammen med verdier og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="fead4-114">The following table lists the properties of search result modules, together with their values and descriptions.</span></span>

| <span data-ttu-id="fead4-115">Egenskap</span><span class="sxs-lookup"><span data-stu-id="fead4-115">Property</span></span> | <span data-ttu-id="fead4-116">Verdier</span><span class="sxs-lookup"><span data-stu-id="fead4-116">Values</span></span> | <span data-ttu-id="fead4-117">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fead4-117">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="fead4-118">Varer per side</span><span class="sxs-lookup"><span data-stu-id="fead4-118">Items per page</span></span> | <span data-ttu-id="fead4-119">Heltall</span><span class="sxs-lookup"><span data-stu-id="fead4-119">Integer</span></span> | <span data-ttu-id="fead4-120">Antallet elementer som skal vises på hver side.</span><span class="sxs-lookup"><span data-stu-id="fead4-120">The number of items that should be shown on each page.</span></span> |
| <span data-ttu-id="fead4-121">Tillat tilbake på PDP</span><span class="sxs-lookup"><span data-stu-id="fead4-121">Allow back on PDP</span></span> | <span data-ttu-id="fead4-122">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="fead4-122">**True** or **False**</span></span> | <span data-ttu-id="fead4-123">Hvis denne egenskapen settes til **Sann**, vil brødsmulenavigasjonen på produktdetaljsiden (PDP) som åpnes, vise koblingen "Tilbake til resultater" når en bruker velger et produkt på søkeresultatsiden.</span><span class="sxs-lookup"><span data-stu-id="fead4-123">If this property is set to **True**, when a user selects a product on the search results page, the breadcrumb navigation on the product details page (PDP) that is opened will show a "Back to results" link.</span></span> |
| <span data-ttu-id="fead4-124">Utvid presiseringer</span><span class="sxs-lookup"><span data-stu-id="fead4-124">Expand Refiners</span></span> | <span data-ttu-id="fead4-125">**Alle**, **1**, **2**, **3** eller **4**</span><span class="sxs-lookup"><span data-stu-id="fead4-125">**All**, **1**, **2**, **3**, or **4**</span></span> | <span data-ttu-id="fead4-126">Antallet toppresiseringer som skal utvides når en side lastes inn.</span><span class="sxs-lookup"><span data-stu-id="fead4-126">The number of top refiners that should be expanded when a page is loaded.</span></span> <span data-ttu-id="fead4-127">Hvis for eksempel denne egenskapen er satt til **3**, utvides de første tre presiseringene på siden.</span><span class="sxs-lookup"><span data-stu-id="fead4-127">For example, if this property is set to **3**, the first three refiners on the page will be expanded.</span></span> |
| <span data-ttu-id="fead4-128">Skjul visning av kategorihierarki</span><span class="sxs-lookup"><span data-stu-id="fead4-128">Hide category hierarchy display</span></span> | <span data-ttu-id="fead4-129">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="fead4-129">**True** or **False**</span></span> | <span data-ttu-id="fead4-130">Hvis denne egenskapen er satt til **Sann**, vil kategorihierarkivisningen på siden være skjult.</span><span class="sxs-lookup"><span data-stu-id="fead4-130">If this property is set to **True**, the category hierarchy display on the page will be hidden.</span></span> <span data-ttu-id="fead4-131">Denne egenskapen bør settes til **Sann** hvis du bruker [brødsmulemodulen](add-breadcrumb.md) for å vise kategorihierarkiet.</span><span class="sxs-lookup"><span data-stu-id="fead4-131">This property should be set to **True** if you're using the [breadcrumb module](add-breadcrumb.md) to show the category hierarchy.</span></span>|
| <span data-ttu-id="fead4-132">Inkluder produktattributter i søkeresultater</span><span class="sxs-lookup"><span data-stu-id="fead4-132">Include product attributes in search results</span></span> | <span data-ttu-id="fead4-133">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="fead4-133">**True** or **False**</span></span> | <span data-ttu-id="fead4-134">Hvis denne egenskapen er satt til **Sann**, blir attributter returnert for produktene i søkeresultatene.</span><span class="sxs-lookup"><span data-stu-id="fead4-134">If this property is set to **True**, attributes will be returned for the products in the search results.</span></span> <span data-ttu-id="fead4-135">Selv om disse attributtene kan vises på et Commerce-område, kreves det en utvidelse.</span><span class="sxs-lookup"><span data-stu-id="fead4-135">Although these attributes can be shown on a Commerce site, an extension is required.</span></span>|
| <span data-ttu-id="fead4-136">Vis tilknytningspriser</span><span class="sxs-lookup"><span data-stu-id="fead4-136">Show affiliation prices</span></span> | <span data-ttu-id="fead4-137">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="fead4-137">**True** or **False**</span></span> | <span data-ttu-id="fead4-138">Hvis denne egenskapen er satt til **Sann**, vises tilknytningspriser for produkter i søkeresultatene når en pålogget bruker blar gjennom siden.</span><span class="sxs-lookup"><span data-stu-id="fead4-138">If this property is set to **True**, affiliation prices for products will be shown in the search results when a signed-in user browses the page.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="fead4-139">I Dynamics 365 Commerce 10.0.16-versjonen og senere kan konfigurasjonen **Vis tilknytningspriser** brukes til å vise tilknytningspriser på siden.</span><span class="sxs-lookup"><span data-stu-id="fead4-139">In the Dynamics 365 Commerce 10.0.16 release and later, the **Show affiliation prices** configuration can be used to show affiliation prices on the page.</span></span>

## <a name="supported-modules"></a><span data-ttu-id="fead4-140">Støttede moduler</span><span class="sxs-lookup"><span data-stu-id="fead4-140">Supported modules</span></span>

<span data-ttu-id="fead4-141">Søkeresultatmodulen støtter [hurtigvisningsmodulen](quick-view-module.md), som gjør det mulig for brukere å vise produktinformasjon og legge til varer i handlekurven fra søkeresultatsiden.</span><span class="sxs-lookup"><span data-stu-id="fead4-141">The search results module supports the [quick view module](quick-view-module.md), which lets users view product information and add items to the cart from the search results page.</span></span>

## <a name="add-a-search-results-module-to-a-category-page"></a><span data-ttu-id="fead4-142">Legge til en søkeresultatmodul på en kategoriside</span><span class="sxs-lookup"><span data-stu-id="fead4-142">Add a search results module to a category page</span></span>

<span data-ttu-id="fead4-143">For å legge til en søkeresultatmodul på en kategoriside, følg disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="fead4-143">To add a search results module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="fead4-144">Gå til **Maler**, og velg **Ny** for å opprette en ny mal.</span><span class="sxs-lookup"><span data-stu-id="fead4-144">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="fead4-145">I dialogboksen **Ny mal** angir du navnet på **Søkeresultater**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="fead4-145">In the **New template** dialog box, enter the name **Search results**, and then select **OK**.</span></span>
1. <span data-ttu-id="fead4-146">I **Tekst**-sporet velger du ellipsen (…), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="fead4-146">In the **Body** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fead4-147">I dialogboksen **Legg til modul** velger du **Standardside**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="fead4-147">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fead4-148">I **Hoved**-sporet på **Standardside**-modulen velger du ellipseknappen (...), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="fead4-148">In the **Main** slot of the **Default Page** module, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fead4-149">I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="fead4-149">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fead4-150">I **Beholder**-sporet velger du ellipsen (…), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="fead4-150">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fead4-151">I dialogboksen **Legg til modul** velger du **Brødsmule**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="fead4-151">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fead4-152">Skriv inn verdien **1** for **Minimum antall forekomster** i egenskapsruten **Brødsmule**.</span><span class="sxs-lookup"><span data-stu-id="fead4-152">In the **Breadcrumb** properties pane, enter the value **1** for **Min Occurs**.</span></span>
1. <span data-ttu-id="fead4-153">I **Beholder**-sporet velger du ellipsen (…), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="fead4-153">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fead4-154">I dialogboksen **Legg til modul** velger du **Søkeresultater**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="fead4-154">In the **Add Module** dialog box, select the **Search results** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fead4-155">I ruten for egenskaper i **Søkeresultater** angir du verdien **1** for **Minimum antall forekomster**, og deretter angir du andre nødvendige egenskaper for søkeresultatmodulen.</span><span class="sxs-lookup"><span data-stu-id="fead4-155">In the **Search results** properties pane, enter the value **1** for **Min Occurs**, and then set any other required properties for the search results module.</span></span> <span data-ttu-id="fead4-156">Ved å angi disse egenskapene i malen, sikrer du at alle tilpasninger til en bestemt kategoriside automatisk inneholder disse innstillingene.</span><span class="sxs-lookup"><span data-stu-id="fead4-156">By setting these properties in the template, you ensure that any customizations to a specific category page will automatically include these settings.</span></span>
1. <span data-ttu-id="fead4-157">Velg **Fullfør redigering**, og velg deretter **Publiser** for å publisere malen.</span><span class="sxs-lookup"><span data-stu-id="fead4-157">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>
1. <span data-ttu-id="fead4-158">Gå til **Sider**, og velg **Ny** for å opprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="fead4-158">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="fead4-159">I dialogboksen **Velg en mal** velger du malen **Søkeresultater** som du opprettet, angir **Kategoriside** for **Sidenavn**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="fead4-159">In the **Choose a template** dialog box, select the **Search results** template that you created, enter **Category page** for **Page name**, and then select **OK**.</span></span> <span data-ttu-id="fead4-160">Siden alle verdiene er angitt i malen, er siden klar til å publiseres.</span><span class="sxs-lookup"><span data-stu-id="fead4-160">Because all the values are set in the template, the page is ready to be published.</span></span>
1. <span data-ttu-id="fead4-161">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="fead4-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fead4-162">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="fead4-162">Additional resources</span></span>

[<span data-ttu-id="fead4-163">Oversikt over standard kategorimålside og søkeresultatside</span><span class="sxs-lookup"><span data-stu-id="fead4-163">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="fead4-164">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="fead4-164">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fead4-165">Hurtigvisningsmodul</span><span class="sxs-lookup"><span data-stu-id="fead4-165">Quick view module</span></span>](quick-view-module.md)
