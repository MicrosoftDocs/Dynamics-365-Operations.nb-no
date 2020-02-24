---
title: Legg til en ny områdeside
description: Dette emnet beskriver hvordan du legger til en ny områdeside i Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 68461f1f0be46f979a67e1806e03c02200cf61db
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001352"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="ade39-103">Legg til en ny områdeside</span><span class="sxs-lookup"><span data-stu-id="ade39-103">Add a new site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ade39-104">Dette emnet beskriver hvordan du legger til en ny områdeside i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ade39-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ade39-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="ade39-105">Overview</span></span>

<span data-ttu-id="ade39-106">Når du har opprettet maler og fragmenter for området, er neste trinn å begynne å opprette sider som bruker dem.</span><span class="sxs-lookup"><span data-stu-id="ade39-106">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="ade39-107">For å komme i gang må du velge en mal eller et oppsett, et sidenavn og en side-URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="ade39-107">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="ade39-108">Mal eller oppsett</span><span class="sxs-lookup"><span data-stu-id="ade39-108">Template or layout</span></span>

<span data-ttu-id="ade39-109">Du kan enten bruke en mal eller et oppsett for den nye siden.</span><span class="sxs-lookup"><span data-stu-id="ade39-109">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="ade39-110">For mer informasjon, se [Oversikt over maler og oppsett](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ade39-110">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="ade39-111">Sidenavn</span><span class="sxs-lookup"><span data-stu-id="ade39-111">Page name</span></span>

<span data-ttu-id="ade39-112">Sidenavnet må være unikt for siden.</span><span class="sxs-lookup"><span data-stu-id="ade39-112">The page name must be unique to your page.</span></span> <span data-ttu-id="ade39-113">Det bør være beskrivende, slik at du enkelt kan finne det, og andre personer vet hva siden er ment for.</span><span class="sxs-lookup"><span data-stu-id="ade39-113">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="ade39-114">Velg sidenavnet nøye, fordi det ikke kan endres senere.</span><span class="sxs-lookup"><span data-stu-id="ade39-114">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="ade39-115">URL-adresse for side</span><span class="sxs-lookup"><span data-stu-id="ade39-115">Page URL</span></span>

<span data-ttu-id="ade39-116">Du kan velge å angi en URL-adresse til den nye siden.</span><span class="sxs-lookup"><span data-stu-id="ade39-116">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="ade39-117">Når du oppretter en side, kan du angi en streng som skal brukes til å opprette en fullstendig URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="ade39-117">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="ade39-118">Denne strengen kalles en relativ URL-adresse eller en URL-plassholder.</span><span class="sxs-lookup"><span data-stu-id="ade39-118">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="ade39-119">En fullstendig URL-adresse genereres deretter på grunnlag av URL-plassholderen, og den nye siden tilordnes.</span><span class="sxs-lookup"><span data-stu-id="ade39-119">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="ade39-120">Du kan endre URL-plassholderen senere, før du publiserer siden.</span><span class="sxs-lookup"><span data-stu-id="ade39-120">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="ade39-121">Hvis du vil ha mer informasjon, kan du se [Opprette en URL-adresse for side](create-page-URL.md).</span><span class="sxs-lookup"><span data-stu-id="ade39-121">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="ade39-122">Dynamics 365 Commerce kobler fra URL-adresser og innhold.</span><span class="sxs-lookup"><span data-stu-id="ade39-122">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="ade39-123">Du kan med andre ord opprette en side som ikke er tilknyttet en URL-adresse, og det kan opprettes en URL-adresse som ikke er tilknyttet en side.</span><span class="sxs-lookup"><span data-stu-id="ade39-123">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="ade39-124">Innholdsbytting kan derfor utføres for en URL-adresse og krever ikke nedetid, og omadresseringer er enklere å administrere.</span><span class="sxs-lookup"><span data-stu-id="ade39-124">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="ade39-125">Legge til en ny side</span><span class="sxs-lookup"><span data-stu-id="ade39-125">Add a new page</span></span>

<span data-ttu-id="ade39-126">Følg denne fremgangsmåten for å legge til en ny områdeside på området.</span><span class="sxs-lookup"><span data-stu-id="ade39-126">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="ade39-127">Under **Områder** velger du **Fabrikam** (eller navnet på området).</span><span class="sxs-lookup"><span data-stu-id="ade39-127">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="ade39-128">Velg **Ny side**.</span><span class="sxs-lookup"><span data-stu-id="ade39-128">Select **New Page**.</span></span>
1. <span data-ttu-id="ade39-129">I dialogboksen **Ny side** velger du malen og deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="ade39-129">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="ade39-130">I feltet **Sidenavn** angir du et sidenavn (for eksempel **Min nye side**).</span><span class="sxs-lookup"><span data-stu-id="ade39-130">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="ade39-131">I feltet **URL** angir du en streng (URL-plassholder) for å fullføre URL-adressen (for eksempel **minnyeside**).</span><span class="sxs-lookup"><span data-stu-id="ade39-131">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="ade39-132">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ade39-132">Select **OK**.</span></span> <span data-ttu-id="ade39-133">Redigeringsprogrammet for side vises.</span><span class="sxs-lookup"><span data-stu-id="ade39-133">The page editor appears.</span></span> <span data-ttu-id="ade39-134">Legg merke til at det automatisk blir lagt til et topptekst og en bunntekst på siden basert på malen du har valgt.</span><span class="sxs-lookup"><span data-stu-id="ade39-134">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="ade39-135">På sideoppsettet velger du sporet for **Hoved**, velger ellipseknappen (**...**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="ade39-135">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="ade39-136">Velg **Container**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="ade39-136">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="ade39-137">Velg **Flytende container**, velg ellipseknappen, og velg deretter **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="ade39-137">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ade39-138">Velg **Innholdsrik blokk**, og velg dereter **OK**.</span><span class="sxs-lookup"><span data-stu-id="ade39-138">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="ade39-139">Velg **Innholdsrik blokk**, velg ellipseknappen, og velg deretter **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="ade39-139">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ade39-140">Velg **Innholdsrikt blokkelement**, og velg dereter **OK**.</span><span class="sxs-lookup"><span data-stu-id="ade39-140">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="ade39-141">I avsnittsruten til høyre velger du **Avsnitt**, og deretter, i feltet, angir du **Min testtekst**.</span><span class="sxs-lookup"><span data-stu-id="ade39-141">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="ade39-142">Velg **Lagre**, og velg deretter **Sjekk inn**.</span><span class="sxs-lookup"><span data-stu-id="ade39-142">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="ade39-143">I feltet **Kommentarer** angr du **La til nye side**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="ade39-143">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="ade39-144">Velg **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="ade39-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="ade39-145">Når du er ferdig, lukker du forhåndsvisningskategorien for å gå tilbake til redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="ade39-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="ade39-146">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="ade39-146">Select **Publish**.</span></span>
1. <span data-ttu-id="ade39-147">I navigasjonsbanen (søkebaner) velger du **Fabrikam** (eller navnet på området).</span><span class="sxs-lookup"><span data-stu-id="ade39-147">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="ade39-148">Velg **URL-adresser**i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="ade39-148">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="ade39-149">Finn og velg URL-adresse (**minnyeside**) i listen.</span><span class="sxs-lookup"><span data-stu-id="ade39-149">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="ade39-150">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="ade39-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ade39-151">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ade39-151">Additional resources</span></span>

[<span data-ttu-id="ade39-152">Endre en eksisterende områdeside</span><span class="sxs-lookup"><span data-stu-id="ade39-152">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="ade39-153">Velge sideoppsett</span><span class="sxs-lookup"><span data-stu-id="ade39-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="ade39-154">Behandle metadata for søkemotor</span><span class="sxs-lookup"><span data-stu-id="ade39-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="ade39-155">Lagre, forhåndsvise og publisere en side</span><span class="sxs-lookup"><span data-stu-id="ade39-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="ade39-156">Supplere en produktside</span><span class="sxs-lookup"><span data-stu-id="ade39-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="ade39-157">Supplere en kategorimålside</span><span class="sxs-lookup"><span data-stu-id="ade39-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="ade39-158">Kontrollere tilgjengelighet for sideinnhold</span><span class="sxs-lookup"><span data-stu-id="ade39-158">Verify page content accessibility</span></span>](verify-accessibility.md)
