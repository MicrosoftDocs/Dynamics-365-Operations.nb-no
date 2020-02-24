---
title: Lagre, forhåndsvise og publisere en side
description: Dette emnet beskriver hvordan du lagrer, forhåndsviser og publiserer en side i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 04200264fabca265484b5e66426810efe8028a50
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002825"
---
# <a name="save-preview-and-publish-a-page"></a><span data-ttu-id="61964-103">Lagre, forhåndsvise og publisere en side</span><span class="sxs-lookup"><span data-stu-id="61964-103">Save, preview, and publish a page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="61964-104">Dette emnet beskriver hvordan du lagrer, forhåndsviser og publiserer en side i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="61964-104">This topic describes how to save, preview, and publish a page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="save-a-page"></a><span data-ttu-id="61964-105">Lagre en side</span><span class="sxs-lookup"><span data-stu-id="61964-105">Save a page</span></span>

<span data-ttu-id="61964-106">Hvis du vil lagre en side, må du sjekke den ut til deg selv og åpne den i redigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="61964-106">To save a page, you must have it checked out to yourself and open in the page editor.</span></span> <span data-ttu-id="61964-107">Du bør lagre en side umiddelbart etter at du har endret den, for å bidra til å sikre at endringene lagres.</span><span class="sxs-lookup"><span data-stu-id="61964-107">You should save a page immediately after you modify it, to help guarantee that your changes are stored.</span></span>

<span data-ttu-id="61964-108">Når du lagrer en side, er endringene bare synlige for deg.</span><span class="sxs-lookup"><span data-stu-id="61964-108">When you save a page, the changes are visible only to you.</span></span> <span data-ttu-id="61964-109">Lagringsoperasjonen er primært ment å lagre endringer mens siden ennå ikke er klar til å sjekkes inn.</span><span class="sxs-lookup"><span data-stu-id="61964-109">The save operation is intended primarily to store changes while the page isn't yet ready to be checked in.</span></span> <span data-ttu-id="61964-110">Når du er ferdig med å endre siden, anbefaler vi at du sjekker den inn, slik at endringene blir synlige for andre.</span><span class="sxs-lookup"><span data-stu-id="61964-110">When you've finished modifying the page, we recommend that you check it in, so that the changes become visible to others.</span></span> <span data-ttu-id="61964-111">På dette tidspunktet kan siden også sjekkes ut av andre brukere som må endre den.</span><span class="sxs-lookup"><span data-stu-id="61964-111">At that point, the page can also be checked out by other users who must modify it.</span></span>

## <a name="preview-a-page"></a><span data-ttu-id="61964-112">Forhåndsvise en side</span><span class="sxs-lookup"><span data-stu-id="61964-112">Preview a page</span></span>

<span data-ttu-id="61964-113">Redigeringsverktøyet har to typer forhåndsvisningsfunksjoner: en WYSIWYG-forhåndsvisningsrute ("hva du ser, er hva du får") i sideredigeringsprogrammet og et eget forhåndsvisningsvindu.</span><span class="sxs-lookup"><span data-stu-id="61964-113">The authoring tool offers two kinds of preview features: a "what you see is what you get" (WYSIWYG) preview pane in the page editor and a separate preview window.</span></span>

<span data-ttu-id="61964-114">Når du bruker sideredigeringsprogrammet, vises det en WYSIWYG-forhåndsvisning i den midtre ruten.</span><span class="sxs-lookup"><span data-stu-id="61964-114">While you're using the page editor, a "what you see is what you get" (WYSIWYG) preview appears in the center pane.</span></span> <span data-ttu-id="61964-115">Denne forhåndsvisningen oppdateres automatisk hver gang du lagrer siden.</span><span class="sxs-lookup"><span data-stu-id="61964-115">This preview is automatically updated whenever you save the page.</span></span> <span data-ttu-id="61964-116">Du kan også oppdatere den manuelt ved å velge **Oppdater** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="61964-116">You can also manually update it by selecting **Refresh** on the command bar.</span></span> <span data-ttu-id="61964-117">WYSIWYG-forhåndsvisning gjengir siden på samme måte som områdets brukere vil se den, men redigeringshjelpere gjengis oppå den.</span><span class="sxs-lookup"><span data-stu-id="61964-117">The WYSIWYG preview renders the page just as the site's users will see it, but authoring helpers are rendered on top of it.</span></span>

<span data-ttu-id="61964-118">Når du er ferdig med å endre siden, kan det være lurt å forhåndsvise den for å se hva kundene vil se.</span><span class="sxs-lookup"><span data-stu-id="61964-118">When you've finished modifying the page, you might want to preview it to see what customers will see.</span></span> <span data-ttu-id="61964-119">Velg **Forhåndsvisning** på kommandolinjen for å forhåndsvise en side.</span><span class="sxs-lookup"><span data-stu-id="61964-119">To preview a page, select **Preview** on the command bar.</span></span> <span data-ttu-id="61964-120">Forhåndsvisningen vil vises i et eget leservindu.</span><span class="sxs-lookup"><span data-stu-id="61964-120">The preview will appear in a separate browser window.</span></span> <span data-ttu-id="61964-121">Siden i forhåndsvisningsvinduet vises på samme måte som områdets bruker vil se den.</span><span class="sxs-lookup"><span data-stu-id="61964-121">The page in the preview window is rendered just as the site's user will see it.</span></span> <span data-ttu-id="61964-122">Du kan endre størrelsen på vinduet for å kontrollere at svarmoduler gjengis riktig i alle visningsporter.</span><span class="sxs-lookup"><span data-stu-id="61964-122">You can resize the window to make sure that responsive modules are correctly rendered in all view ports.</span></span>

> [!NOTE]
> <span data-ttu-id="61964-123">Godkjenning og riktige tillatelser kreves for å forhåndsvise upublisert innhold.</span><span class="sxs-lookup"><span data-stu-id="61964-123">Authentication and correct permissions are required to preview unpublished content.</span></span> <span data-ttu-id="61964-124">Hvis du deler URL-adressen for forhåndsvisningen med noen, må vedkommende derfor ha de riktige tillatelsene for å få tilgang til innholdet.</span><span class="sxs-lookup"><span data-stu-id="61964-124">Therefore, if you share the URL of the preview with someone, that person must have the correct permissions to access the content.</span></span>

## <a name="publish-a-page"></a><span data-ttu-id="61964-125">Publisere en side</span><span class="sxs-lookup"><span data-stu-id="61964-125">Publish a page</span></span>

<span data-ttu-id="61964-126">Når siden er klar, er det neste trinnet å publisere den, slik at eksterne brukere kan vise innholdet.</span><span class="sxs-lookup"><span data-stu-id="61964-126">When your page is ready, the next step is to publish it, so that external users can view the content.</span></span> <span data-ttu-id="61964-127">Før du kan publisere en side må du sjekke den inn.</span><span class="sxs-lookup"><span data-stu-id="61964-127">Before you can publish a page, you must check it in.</span></span>

<span data-ttu-id="61964-128">Du kan publisere og oppheve publiseringen av sidene enten fra sideinspeksjonen eller sideredigeringen.</span><span class="sxs-lookup"><span data-stu-id="61964-128">You can publish and unpublish pages from either the page inspector or the page editor.</span></span> <span data-ttu-id="61964-129">Sideinspeksjonen viser en liste over sider og tillater masseoperasjoner.</span><span class="sxs-lookup"><span data-stu-id="61964-129">The page inspector shows a list of pages and allows for bulk operations.</span></span> <span data-ttu-id="61964-130">Sideredigeringsprogrammet kan brukes til å publisere eller oppheve publiseringen av bare den ene siden som er åpen i den.</span><span class="sxs-lookup"><span data-stu-id="61964-130">The page editor can be used to publish or unpublish only the single page that is open in it.</span></span>

<span data-ttu-id="61964-131">Hvis du vil publisere én eller flere sider fra sideinspeksjonen, merker du sidene, kontrollerer at de er sjekket inn, og deretter velger **Publiser** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="61964-131">To publish one or more pages from the page inspector, select the pages, make sure that they are checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="61964-132">Sidene publiseres, og du mottar en melding om operasjonen i redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="61964-132">The pages are published, and you receive a notification about the operation in the authoring tool.</span></span>

<span data-ttu-id="61964-133">Fremgangsmåten er lik for publisering av en enkelt side fra sideredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="61964-133">To publish a single page from the page editor, the procedure is similar.</span></span> <span data-ttu-id="61964-134">Mens siden er åpen i redigeringsprogrammet for side, må du kontrollere at den er sjekket inn og deretter velge **Publiser** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="61964-134">While the page is open in the page editor, make sure that it has been checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="61964-135">Siden publiseres, og du mottar en melding om operasjonen.</span><span class="sxs-lookup"><span data-stu-id="61964-135">The page is published, and you receive a notification about the operation.</span></span>

<span data-ttu-id="61964-136">Når du publiserer en side, publiseres bare sideinnholdet.</span><span class="sxs-lookup"><span data-stu-id="61964-136">When you publish a page, just the page content is published.</span></span> <span data-ttu-id="61964-137">Du og andre brukere kan gå til siden og vise den bare etter at en URL-adresse er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="61964-137">You and other users can go to the page and view it only after a URL is associated with it.</span></span> <span data-ttu-id="61964-138">Nettadressen må publiseres separat.</span><span class="sxs-lookup"><span data-stu-id="61964-138">The URL must be published separately.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="61964-139">Før du kan publisere en side må alle bilder eller fragmenter som siden refererer til, allerede være publisert.</span><span class="sxs-lookup"><span data-stu-id="61964-139">Before you can publish a page, any images or fragments that the page references must already be published.</span></span>

## <a name="save-preview-and-publish-a-home-page"></a><span data-ttu-id="61964-140">Lagre, forhåndsvise og publisere en startside</span><span class="sxs-lookup"><span data-stu-id="61964-140">Save, preview, and publish a home page</span></span>

<span data-ttu-id="61964-141">Følg denne fremgangsmåten for å lagre, forhåndsvise og publisere en startside.</span><span class="sxs-lookup"><span data-stu-id="61964-141">To save, preview, and publish a home page, follow these steps.</span></span>

1. <span data-ttu-id="61964-142">Under **Områder** velger du **Fabrikam** (eller navnet på området).</span><span class="sxs-lookup"><span data-stu-id="61964-142">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="61964-143">Velg **Sider**i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="61964-143">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="61964-144">Finn og velg startsside for å åpne den i sideredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="61964-144">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="61964-145">Velg **Sjekk ut**.</span><span class="sxs-lookup"><span data-stu-id="61964-145">Select **Check Out**.</span></span>
1. <span data-ttu-id="61964-146">Endre siden slik du vil ha den.</span><span class="sxs-lookup"><span data-stu-id="61964-146">Modify the page as you require.</span></span>
1. <span data-ttu-id="61964-147">Velg **Lagre**, og velg deretter **Sjekk inn**.</span><span class="sxs-lookup"><span data-stu-id="61964-147">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="61964-148">Skriv inn en merknad om endringene du har gjort, i feltet **Kommentar**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="61964-148">In the **Comments** field, enter a note about the changes that you made, and then select **OK**.</span></span>
1. <span data-ttu-id="61964-149">Velg **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="61964-149">Select **Preview** to preview your page.</span></span> <span data-ttu-id="61964-150">Når du er ferdig, lukker du forhåndsvisningskategorien for å gå tilbake til redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="61964-150">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="61964-151">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="61964-151">Select **Publish**.</span></span>

## <a name="publish-a-url"></a><span data-ttu-id="61964-152">Publisere en URL-adresse</span><span class="sxs-lookup"><span data-stu-id="61964-152">Publish a URL</span></span>

<span data-ttu-id="61964-153">Hvis du vil publisere en URL-adresse, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="61964-153">To publish a URL, follow these steps.</span></span>

1. <span data-ttu-id="61964-154">Under **Områder** velger du **Fabrikam** (eller navnet på området).</span><span class="sxs-lookup"><span data-stu-id="61964-154">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="61964-155">Velg **URL-adresser**i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="61964-155">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="61964-156">Finn og velg URL-adressen du vil publisere.</span><span class="sxs-lookup"><span data-stu-id="61964-156">Find and select the URL to publish.</span></span>
1. <span data-ttu-id="61964-157">På kommandolinjen velger du **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="61964-157">On the command bar, select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61964-158">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="61964-158">Additional resources</span></span>

[<span data-ttu-id="61964-159">Endre en eksisterende områdeside</span><span class="sxs-lookup"><span data-stu-id="61964-159">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="61964-160">Legg til en ny områdeside</span><span class="sxs-lookup"><span data-stu-id="61964-160">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="61964-161">Velge sideoppsett</span><span class="sxs-lookup"><span data-stu-id="61964-161">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="61964-162">Behandle metadata for søkemotor</span><span class="sxs-lookup"><span data-stu-id="61964-162">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="61964-163">Supplere en produktside</span><span class="sxs-lookup"><span data-stu-id="61964-163">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="61964-164">Supplere en kategorimålside</span><span class="sxs-lookup"><span data-stu-id="61964-164">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="61964-165">Kontrollere tilgjengelighet for sideinnhold</span><span class="sxs-lookup"><span data-stu-id="61964-165">Verify page content accessibility</span></span>](verify-accessibility.md)
