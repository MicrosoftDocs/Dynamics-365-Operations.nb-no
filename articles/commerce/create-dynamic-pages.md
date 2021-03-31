---
title: Opprette dynamiske e-handelssider basert på URL-parametere
description: Dette emnet beskriver hvordan du konfigurerer en e-handelside i Microsoft Dynamics 365 Commerce som kan ha dynamisk innhold basert på URL-parametere.
author: StuHarg
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8d6b4756fc81dc99786da251d5d9a575a71ccc49
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208021"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a><span data-ttu-id="dcaff-103">Opprette dynamiske e-handelssider basert på URL-parametere</span><span class="sxs-lookup"><span data-stu-id="dcaff-103">Create dynamic e-commerce pages based on URL parameters</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="dcaff-104">Dette emnet beskriver hvordan du konfigurerer en e-handelside i Microsoft Dynamics 365 Commerce som kan ha dynamisk innhold basert på URL-parametere.</span><span class="sxs-lookup"><span data-stu-id="dcaff-104">This topic describes how to set up a Microsoft Dynamics 365 Commerce e-commerce page that can serve dynamic content, based on URL parameters.</span></span>

<span data-ttu-id="dcaff-105">En e-handelsside kan konfigureres til å ha forskjellig innhold, basert på et segment i URL-banen.</span><span class="sxs-lookup"><span data-stu-id="dcaff-105">An e-commerce page can be configured to serve different content, based on a segment in the URL path.</span></span> <span data-ttu-id="dcaff-106">Derfor kalles siden en dynamisk side.</span><span class="sxs-lookup"><span data-stu-id="dcaff-106">Therefore, the page is known as a dynamic page.</span></span> <span data-ttu-id="dcaff-107">Segmentet brukes som en parameter for å hente sideinnholdet.</span><span class="sxs-lookup"><span data-stu-id="dcaff-107">The segment is used as a parameter to retrieve the page content.</span></span> <span data-ttu-id="dcaff-108">Det vil for eksempel opprettes en side med navnet **blogg\_fremviser** som knyttes til URL-adressen `https://fabrikam.com/blog`.</span><span class="sxs-lookup"><span data-stu-id="dcaff-108">For example, a page that is named **blog\_viewer** is created and associated with the URL `https://fabrikam.com/blog`.</span></span> <span data-ttu-id="dcaff-109">Denne siden kan deretter brukes til å vise forskjellig innhold, basert på det siste segmentet i URL-banen.</span><span class="sxs-lookup"><span data-stu-id="dcaff-109">This page can then be used to show different content, based on the last segment in the URL path.</span></span> <span data-ttu-id="dcaff-110">Eksempelvis er det siste segmentet i URL-adressen `https://fabrikam.com/blog/article-1` **artikkel-1**.</span><span class="sxs-lookup"><span data-stu-id="dcaff-110">For example, the last segment in the URL `https://fabrikam.com/blog/article-1` is **article-1**.</span></span>

<span data-ttu-id="dcaff-111">Separate egendefinerte sider som overstyrer den dynamiske siden, kan også knyttes til segmenter i URL-banen.</span><span class="sxs-lookup"><span data-stu-id="dcaff-111">Separate custom pages that override the dynamic page can also be associated with segments in the URL path.</span></span> <span data-ttu-id="dcaff-112">Det vil for eksempel opprettes en side med navnet **blogg\_sammendrag** som knyttes til URL-adressen `https://fabrikam.com/blog/about-this-blog`.</span><span class="sxs-lookup"><span data-stu-id="dcaff-112">For example, a page that is named **blog\_summary** is created and associated with the URL `https://fabrikam.com/blog/about-this-blog`.</span></span> <span data-ttu-id="dcaff-113">Når denne URL-adressen forespørres, returneres **blogg\_sammendrag**-siden som er knyttet til paramenteren **/about-this-blog** i stedet for siden **blogg\_fremviser**.</span><span class="sxs-lookup"><span data-stu-id="dcaff-113">When this URL is requested, the **blog\_summary** page that is associated with the **/about-this-blog** parameter is returned instead of the **blog\_viewer** page.</span></span>

> [!NOTE]
> <span data-ttu-id="dcaff-114">Funksjonaliteten for mottak, henting og visning av dynamisk sideinnhold implementeres ved hjelp av en egendefinert modul.</span><span class="sxs-lookup"><span data-stu-id="dcaff-114">The functionality for hosting, retrieving, and showing dynamic page content is implemented by using a custom module.</span></span> <span data-ttu-id="dcaff-115">Hvis du vil ha mer informasjon, kan du se [Utvidelsesmulighet for Internett-kanal](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="dcaff-115">For more information, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="set-up-a-dynamic-e-commerce-page"></a><span data-ttu-id="dcaff-116">Definere en dynamisk e-handelsside</span><span class="sxs-lookup"><span data-stu-id="dcaff-116">Set up a dynamic e-commerce page</span></span>

<span data-ttu-id="dcaff-117">Hvis du vil definere en dynamisk e-handelside, må du opprette den dynamiske siden, opprette basis-URLen og konfigurere ruten til den dynamiske siden.</span><span class="sxs-lookup"><span data-stu-id="dcaff-117">To set up a dynamic e-commerce page, you must create the dynamic page, create the base URL, and configure the route to the dynamic page.</span></span>

### <a name="create-the-page-that-will-serve-dynamic-content"></a><span data-ttu-id="dcaff-118">Opprette en side som inneholder dynamisk innhold</span><span class="sxs-lookup"><span data-stu-id="dcaff-118">Create the page that will serve dynamic content</span></span>

<span data-ttu-id="dcaff-119">Følg trinnene i [Legg til en ny områdeside](add-new-page.md) for å opprette en side som inneholder dynamisk innhold.</span><span class="sxs-lookup"><span data-stu-id="dcaff-119">To create a page that will serve dynamic content, follow the steps in [Add a new site page](add-new-page.md).</span></span> <span data-ttu-id="dcaff-120">Siden du oppretter, krever implementering av en modul som bruker det siste segmentet i URL-banen til å hente innhold fra en ekstern datakilde.</span><span class="sxs-lookup"><span data-stu-id="dcaff-120">The page that you create will require implementation of a module that uses the last segment in the URL path to retrieve content from an external data source.</span></span> <span data-ttu-id="dcaff-121">Hvis du vil ha mer informasjon om utvikling av egendefinerte moduler, kan du se [Utvidelsesmulighet for Internett-kanal](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="dcaff-121">For more information about custom module development, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

### <a name="create-the-base-url-for-the-dynamic-page"></a><span data-ttu-id="dcaff-122">Opprette basis-URLen for den dynamiske siden</span><span class="sxs-lookup"><span data-stu-id="dcaff-122">Create the base URL for the dynamic page</span></span>

<span data-ttu-id="dcaff-123">Følg denne fremgangsmåten for å opprette basis-URLen for den dynamiske siden i Commerce-områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="dcaff-123">To create the base URL for the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="dcaff-124">Gå til **URL-adresser**, og velg **Ny \> Ny URL-adresse**.</span><span class="sxs-lookup"><span data-stu-id="dcaff-124">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="dcaff-125">Velg **Intern side** i dialogboksen **Opprett ny URL-adresse**.</span><span class="sxs-lookup"><span data-stu-id="dcaff-125">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="dcaff-126">Under **URL-bane** angir du banen som skal fungere som roten for den dynamiske siden (i dette eksemplet **/blogg**).</span><span class="sxs-lookup"><span data-stu-id="dcaff-126">Under **URL path**, enter the path that will serve as the root for the dynamic page (in this example, **/blog**).</span></span> <span data-ttu-id="dcaff-127">Velg deretter **Neste**.</span><span class="sxs-lookup"><span data-stu-id="dcaff-127">Then select **Next**.</span></span>
1. <span data-ttu-id="dcaff-128">I dialogboksen **Velg en side** velger du siden du opprettet som dynamisk side, og deretter velger du **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dcaff-128">In the **Select a page** dialog box, select the page that you created to serve as the dynamic page, and then select **Save**.</span></span>
1. <span data-ttu-id="dcaff-129">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="dcaff-129">Select **Publish**.</span></span>

### <a name="configure-the-route-to-the-dynamic-page"></a><span data-ttu-id="dcaff-130">Konfigurere ruten til den dynamiske siden</span><span class="sxs-lookup"><span data-stu-id="dcaff-130">Configure the route to the dynamic page</span></span>

<span data-ttu-id="dcaff-131">Følg denne fremgangsmåten for å konfigurere ruten til den dynamiske siden i Commerce-områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="dcaff-131">To configure the route to the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="dcaff-132">Gå til **Områdeinnstillinger \> Tillegg**.</span><span class="sxs-lookup"><span data-stu-id="dcaff-132">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="dcaff-133">Under **Parameteriserte URL-baner** velger du **Legg til**, og deretter legger du inn URL-banen du skrev inn da du opprettet URL-adressen (i dette eksemplet **/blogg**).</span><span class="sxs-lookup"><span data-stu-id="dcaff-133">Under **Parameterized URL paths**, select **Add**, and then enter the URL path that you entered when you created the URL (in this example, **/blog**).</span></span>
1. <span data-ttu-id="dcaff-134">Velg **Lagre og publiser**.</span><span class="sxs-lookup"><span data-stu-id="dcaff-134">Select **Save and publish**.</span></span>

<span data-ttu-id="dcaff-135">Når ruten er konfigurert, vil alle forespørsler til den parameteriserte URL-banen returnere siden som er knyttet til denne URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="dcaff-135">After the route is configured, all requests to the parameterized URL path will return the page that is associated with that URL.</span></span> <span data-ttu-id="dcaff-136">Hvis det finnes forespørsler som inneholder et ekstra segment, returneres den tilknyttede siden, og innholdet på siden hentes ved å bruke segmentet som en parameter.</span><span class="sxs-lookup"><span data-stu-id="dcaff-136">If any requests contain an additional segment, the associated page will be returned, and the page content will be retrieved by using the segment as a parameter.</span></span> <span data-ttu-id="dcaff-137">Eksempelvis vil `https://fabrikam.com/blog/article-1` returnere siden **blogg\_sammendrag**, og sideinnholdet hentes ved hjelp av parameteren **/artikkel-1**.</span><span class="sxs-lookup"><span data-stu-id="dcaff-137">For example, `https://fabrikam.com/blog/article-1` will return the **blog\_summary** page, and the page content will be retrieved by using the **/article-1** parameter.</span></span>

## <a name="override-a-parameterized-url-with-a-custom-page"></a><span data-ttu-id="dcaff-138">Overstyre en parameterisert URL-adresse med en egendefinert side</span><span class="sxs-lookup"><span data-stu-id="dcaff-138">Override a parameterized URL with a custom page</span></span>

<span data-ttu-id="dcaff-139">Følg denne fremgangsmåten for å overstyre en parameterisert URL-adresse med en egendefinert side i Commerce-områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="dcaff-139">To override a parameterized URL with a custom page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="dcaff-140">Gå til **URL-adresser**, og velg **Ny \> Ny URL-adresse**.</span><span class="sxs-lookup"><span data-stu-id="dcaff-140">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="dcaff-141">Velg **Intern side** i dialogboksen **Opprett ny URL-adresse**.</span><span class="sxs-lookup"><span data-stu-id="dcaff-141">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="dcaff-142">Under **URL-bane** angir du banen som inkluderer segmentet som skal overstyres (i dette eksemplet **/blogg/about-this-blog**).</span><span class="sxs-lookup"><span data-stu-id="dcaff-142">Under **URL path**, enter the path that includes the segment to override (in this example, **/blog/about-this-blog**).</span></span> <span data-ttu-id="dcaff-143">Velg deretter **Neste**.</span><span class="sxs-lookup"><span data-stu-id="dcaff-143">Then select **Next**.</span></span>
1. <span data-ttu-id="dcaff-144">Velg den egendefinerte siden, og velg deretter **Lagre** i dialogboksen **Velg en side**.</span><span class="sxs-lookup"><span data-stu-id="dcaff-144">In the **Select a page** dialog box, select the custom page, and then select **Save**.</span></span>
1. <span data-ttu-id="dcaff-145">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="dcaff-145">Select **Publish**.</span></span>
1. <span data-ttu-id="dcaff-146">Hvis den egendefinerte siden ennå ikke er publisert, kan du gå til **Sider**, velge den egendefinerte siden og deretter velge **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="dcaff-146">If the custom page hasn't yet been published, go to **Pages**, select the custom page, and then select **Publish**.</span></span>

<span data-ttu-id="dcaff-147">Når den egendefinerte siden er publisert, blir den vist i stedet for den dynamiske siden som har parameterisert innhold.</span><span class="sxs-lookup"><span data-stu-id="dcaff-147">After the custom page is published, it will be served instead of the dynamic page that has parameterized content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dcaff-148">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="dcaff-148">Additional resources</span></span>

[<span data-ttu-id="dcaff-149">Endre en eksisterende områdeside</span><span class="sxs-lookup"><span data-stu-id="dcaff-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="dcaff-150">Legg til en ny områdeside</span><span class="sxs-lookup"><span data-stu-id="dcaff-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="dcaff-151">Velge sideoppsett</span><span class="sxs-lookup"><span data-stu-id="dcaff-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="dcaff-152">Behandle metadata for søkemotor</span><span class="sxs-lookup"><span data-stu-id="dcaff-152">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="dcaff-153">Lagre, forhåndsvise og publisere en side</span><span class="sxs-lookup"><span data-stu-id="dcaff-153">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="dcaff-154">Supplere en produktside</span><span class="sxs-lookup"><span data-stu-id="dcaff-154">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="dcaff-155">Supplere en kategorimålside</span><span class="sxs-lookup"><span data-stu-id="dcaff-155">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="dcaff-156">Kontrollere tilgjengelighet for sideinnhold</span><span class="sxs-lookup"><span data-stu-id="dcaff-156">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="dcaff-157">Utvidelsesmulighet for Internett-kanal</span><span class="sxs-lookup"><span data-stu-id="dcaff-157">Online channel extensibility</span></span>](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]