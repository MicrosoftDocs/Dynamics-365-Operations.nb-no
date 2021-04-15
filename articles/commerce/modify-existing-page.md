---
title: Endre en eksisterende områdeside
description: Dette emnet beskriver hvordan du endrer en eksisterende områdeside i Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b633965e45c16cb4e5991fab67783b867223f6ec
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803735"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="338bb-103">Endre en eksisterende områdeside</span><span class="sxs-lookup"><span data-stu-id="338bb-103">Modify an existing site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="338bb-104">Dette emnet beskriver hvordan du endrer en eksisterende områdeside i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="338bb-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="338bb-105">Når du må endre en side, er det første trinnet å åpne den i sideredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="338bb-105">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="338bb-106">Gå til området som inneholder siden, og finn siden du vil bruke, i listen over sider.</span><span class="sxs-lookup"><span data-stu-id="338bb-106">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="338bb-107">Hvis du ikke finner siden, kan du bruke redigeringsverktøyets omfattende søkefunksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="338bb-107">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="338bb-108">Skriv inn det nøyaktige sidenavnet, eller skriv inn de første bokstavene i objektet og deretter en stjerne (\*).</span><span class="sxs-lookup"><span data-stu-id="338bb-108">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="338bb-109">Det vises en filtrert liste over sider.</span><span class="sxs-lookup"><span data-stu-id="338bb-109">A filtered list of pages appears.</span></span> <span data-ttu-id="338bb-110">Du kan bruke denne listen til å finne siden du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="338bb-110">You can use this list to find the page that you want.</span></span> <span data-ttu-id="338bb-111">Når du har funnet riktig side, velger du sidenavnet for å åpne siden i sideredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="338bb-111">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="338bb-112">Hvis siden er synlig i sideinspeksjon, kan du velge **Rediger** og sjekke den ut siden før du åpner den i sideredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="338bb-112">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="338bb-113">På denne måten kan du sjekke ut flere sider samtidig.</span><span class="sxs-lookup"><span data-stu-id="338bb-113">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="338bb-114">Når siden er åpnet i redigeringsprogrammet for side, må du kontrollere at den er sjekket ut til deg.</span><span class="sxs-lookup"><span data-stu-id="338bb-114">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="338bb-115">Kommandolinjen i redigeringsverktøyet er dynamisk, kontekstavhengig og tilstandsfølsom.</span><span class="sxs-lookup"><span data-stu-id="338bb-115">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="338bb-116">Derfor vises bare handlingene du kan utføre på siden for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="338bb-116">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="338bb-117">Hvis siden for eksempel ikke er sjekket ut til deg, vises ikke knappene **Lagre** og **Fullfør redigering** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="338bb-117">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="338bb-118">Tilstanden for siden vises også på høyre side av vinduet.</span><span class="sxs-lookup"><span data-stu-id="338bb-118">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="338bb-119">Hvis siden ikke allerede er sjekket ut til deg, velger du **Rediger** kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="338bb-119">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="338bb-120">Kommandolinjen endres til å gjenspeile den nye statusen for siden.</span><span class="sxs-lookup"><span data-stu-id="338bb-120">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="338bb-121">Du får også et varsel som sier at siden ble sjekket ut til deg.</span><span class="sxs-lookup"><span data-stu-id="338bb-121">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="338bb-122">Det neste du gjør, er å utføre de faktiske endringene.</span><span class="sxs-lookup"><span data-stu-id="338bb-122">The next step is to make your actual changes.</span></span> <span data-ttu-id="338bb-123">Du vil ofte bruke sidedisposisjonstreet til venstre for å finne og velge modulen du vil endre, og deretter gjøre endringer i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="338bb-123">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="338bb-124">Endringen kan imidlertid noen ganger involvere å legge til eller fjerne modeller eller fragmenter.</span><span class="sxs-lookup"><span data-stu-id="338bb-124">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="338bb-125">Hvis du vil legge til et fragment eller en modul, bruker du sidedisposisjonstreet til å finne sporet der du vil legge til modulen eller fragmentet, og deretter velger du ellipseknappen (**...**) for sporet.</span><span class="sxs-lookup"><span data-stu-id="338bb-125">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="338bb-126">Det vises en meny som inneholder kommandoer for å legge til en modul eller et fragment.</span><span class="sxs-lookup"><span data-stu-id="338bb-126">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="338bb-127">Hvis du vil fjerne en modul eller et fragment, kan du finne og merke den/det i sidedisposisjonstreet, velge ellipseknappen og deretter velge kommandoen for å slette modulen eller fragmentet.</span><span class="sxs-lookup"><span data-stu-id="338bb-127">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="338bb-128">Du kan også vise og redigere egenskapene for en hvilken som helst modul i den visuelle sidebyggerforhåndsvisningen, ved å velge den direkte.</span><span class="sxs-lookup"><span data-stu-id="338bb-128">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="338bb-129">Når du er ferdig med å gjøre endringer og forhåndsvise effekten, bør du sjekke inn siden ved å velge **Fullfør redigering** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="338bb-129">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="338bb-130">Hvis du vil publisere endringene umiddelbart, velger du **Publiser** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="338bb-130">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="338bb-131">Den siste innsjekkede versjonen av siden du endret, publiseres og blir tilgjengelig for eksterne brukere som viser området ditt.</span><span class="sxs-lookup"><span data-stu-id="338bb-131">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="338bb-132">Eksempel: Endre videoen på startsiden</span><span class="sxs-lookup"><span data-stu-id="338bb-132">Example: Change the video on the home page</span></span>

<span data-ttu-id="338bb-133">Følgende eksempel viser hvordan du endrer startsiden ved å endre videoen som vises i videospillermodulen.</span><span class="sxs-lookup"><span data-stu-id="338bb-133">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="338bb-134">Under **Områder** velger du **Fabrikam** (eller navnet på området).</span><span class="sxs-lookup"><span data-stu-id="338bb-134">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="338bb-135">Velg **Sider** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="338bb-135">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="338bb-136">Finn og velg startsside for å åpne den i sideredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="338bb-136">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="338bb-137">På kommandolinjen velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="338bb-137">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="338bb-138">Velg **Hoved**-spor i sideoppsettet.</span><span class="sxs-lookup"><span data-stu-id="338bb-138">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="338bb-139">Utvid alle moduler for flytende containere under **Hoved**-sporet.</span><span class="sxs-lookup"><span data-stu-id="338bb-139">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="338bb-140">Finn og velg videospillermodulen.</span><span class="sxs-lookup"><span data-stu-id="338bb-140">Find and select the video player module.</span></span>
1. <span data-ttu-id="338bb-141">I egenskapsruten til høyre velger du **video**-egenskapen.</span><span class="sxs-lookup"><span data-stu-id="338bb-141">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="338bb-142">Aktivavelgeren vises.</span><span class="sxs-lookup"><span data-stu-id="338bb-142">The asset picker appears.</span></span>
1. <span data-ttu-id="338bb-143">I aktivavelgeren velger du et tilgjengelig videoaktiva, eller velg **Last opp nytt aktiva** for å laste opp et nytt videoaktiva.</span><span class="sxs-lookup"><span data-stu-id="338bb-143">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="338bb-144">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="338bb-144">Select **OK**.</span></span>
1. <span data-ttu-id="338bb-145">Velg **Lagre**, og velg deretter **Fullfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="338bb-145">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="338bb-146">I feltet **Kommentarer** angir du **Endre videown**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="338bb-146">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="338bb-147">Velg **Forhåndsvisning** for å forhåndsvise den oppdaterte siden.</span><span class="sxs-lookup"><span data-stu-id="338bb-147">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="338bb-148">Når du er ferdig, lukker du forhåndsvisningskategorien for å gå tilbake til redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="338bb-148">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="338bb-149">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="338bb-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="338bb-150">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="338bb-150">Additional resources</span></span>

[<span data-ttu-id="338bb-151">Legg til en ny områdeside</span><span class="sxs-lookup"><span data-stu-id="338bb-151">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="338bb-152">Velge sideoppsett</span><span class="sxs-lookup"><span data-stu-id="338bb-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="338bb-153">Behandle metadata for søkemotor</span><span class="sxs-lookup"><span data-stu-id="338bb-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="338bb-154">Lagre, forhåndsvise og publisere en side</span><span class="sxs-lookup"><span data-stu-id="338bb-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="338bb-155">Supplere en produktside</span><span class="sxs-lookup"><span data-stu-id="338bb-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="338bb-156">Supplere en kategorimålside</span><span class="sxs-lookup"><span data-stu-id="338bb-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="338bb-157">Kontrollere tilgjengelighet for sideinnhold</span><span class="sxs-lookup"><span data-stu-id="338bb-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="338bb-158">Opprette dynamiske e-handelssider basert på URL-parametere</span><span class="sxs-lookup"><span data-stu-id="338bb-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
