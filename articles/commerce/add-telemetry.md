---
title: Legge til skript kode i områdes ID-er for å støtte telemetri
description: Dette emnet beskriver hvordan du kan legge til skriptkode på klientsiden på områdesidene dine for å støtte innsamling av telemetri på klientsiden.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 81c36685c1eccceb2f1854fe7c866186120c08a3
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154092"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="4d421-103">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="4d421-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4d421-104">Dette emnet beskriver hvordan du kan legge til skriptkode på klientsiden på områdesidene dine for å støtte innsamling av telemetri på klientsiden.</span><span class="sxs-lookup"><span data-stu-id="4d421-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="4d421-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="4d421-105">Overview</span></span>

<span data-ttu-id="4d421-106">Web Analytics er et viktig verktøy når du vil forstå hvordan kundene samhandler med området og tar avgjørelser som vil bidra til å optimalisere opplevelsen for maksimal konvertering.</span><span class="sxs-lookup"><span data-stu-id="4d421-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="4d421-107">Mange Web Analytics-pakker er tilgjengelige for å hjelpe deg med å oppnå disse målene, for eksempel Google Analytics, Clicky, Moz Analytics og KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="4d421-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="4d421-108">De fleste Web Analytics-pakker krever at du legger til skriptkode på klientsiden i **\<hode\>**-elementet på HTMLen for alle sidene på området.</span><span class="sxs-lookup"><span data-stu-id="4d421-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="4d421-109">Instruksjonene i dette emnet gjelder også for annen tilpasset funksjonalitet på klientsiden som Microsoft Dynamics 365 Commerce ikke tilbyr.</span><span class="sxs-lookup"><span data-stu-id="4d421-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a><span data-ttu-id="4d421-110">Opprette et gjenbrukbart sidefragment for skriptkoden</span><span class="sxs-lookup"><span data-stu-id="4d421-110">Create a reusable page fragment for your script code</span></span>

<span data-ttu-id="4d421-111">Ved hjelp av et sidefragment kan du bruke innebygd eller ekstern skriptkode på nytt på alle sidene på området, uansett hvilken mal de bruker.</span><span class="sxs-lookup"><span data-stu-id="4d421-111">A page fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a><span data-ttu-id="4d421-112">Opprette et gjenbrukbart sidefragment for den innebygde skriptkoden</span><span class="sxs-lookup"><span data-stu-id="4d421-112">Create a reusable page fragment for your inline script code</span></span>

<span data-ttu-id="4d421-113">Hvis du vil opprette et gjenbrukbart sidefragment for den innebygde skriptkoden i områdebygger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="4d421-113">To create a reusable page fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="4d421-114">Gå til **Sidefragmenter**, og velg **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="4d421-114">Go to **Page Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="4d421-115">I dialogboksen **Nytt sidefragment** velger du **Innebygd skript**.</span><span class="sxs-lookup"><span data-stu-id="4d421-115">In the **New Page Fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="4d421-116">Under **Navn på sidefragment** angir du et navn på fragmentet, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d421-116">Under **Page Fragment Name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="4d421-117">Under sidefragmentet du opprettet, velger du modulen **Standard innebygd skript**.</span><span class="sxs-lookup"><span data-stu-id="4d421-117">Under the page fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="4d421-118">I egenskapsruten til høyre, under **Innebygd skript**, angir du skriptet på klientsiden.</span><span class="sxs-lookup"><span data-stu-id="4d421-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="4d421-119">Deretter konfigurerer du andre alternativer etter behov.</span><span class="sxs-lookup"><span data-stu-id="4d421-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="4d421-120">Velg **Lagre**, og velg deretter **Fullfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="4d421-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="4d421-121">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="4d421-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a><span data-ttu-id="4d421-122">Opprette et gjenbrukbart sidefragment for den eksterne skriptkoden</span><span class="sxs-lookup"><span data-stu-id="4d421-122">Create a reusable page fragment for your external script code</span></span>

<span data-ttu-id="4d421-123">Hvis du vil opprette et gjenbrukbart sidefragment for den eksterne skriptkoden i områdebygger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="4d421-123">To create a reusable page fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="4d421-124">Gå til **Sidefragmenter**, og velg **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="4d421-124">Go to **Page Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="4d421-125">I dialogboksen **Nytt sidefragment** velger du **Eksternt skript**.</span><span class="sxs-lookup"><span data-stu-id="4d421-125">In the **New Page Fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="4d421-126">Under **Navn på sidefragment** angir du et navn på fragmentet, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d421-126">Under **Page Fragment Name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="4d421-127">Under sidefragmentet du opprettet, velger du modulen **Standard eksternt skript**.</span><span class="sxs-lookup"><span data-stu-id="4d421-127">Under the page fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="4d421-128">I egenskapsruten til høyre, under **Skriptkilde**, legger du til en ekstern eller relativ URL-adresse for den eksterne skriptkilden.</span><span class="sxs-lookup"><span data-stu-id="4d421-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="4d421-129">Deretter konfigurerer du andre alternativer etter behov.</span><span class="sxs-lookup"><span data-stu-id="4d421-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="4d421-130">Velg **Lagre**, og velg deretter **Fullfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="4d421-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="4d421-131">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="4d421-131">Select **Publish**.</span></span>

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="4d421-132">Legge til et sidefragment som inneholder skript kode, i en mal</span><span class="sxs-lookup"><span data-stu-id="4d421-132">Add a page fragment that includes script code to a template</span></span>

<span data-ttu-id="4d421-133">Hvis du vil legge til et sidefragment som inneholder skriptkode, i en mal i områdebygger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="4d421-133">To add a page fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="4d421-134">Gå til **Maler**, og åpne malen for sidene du vil legge til skriptkoden i.</span><span class="sxs-lookup"><span data-stu-id="4d421-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="4d421-135">I venstre rute utvider du malhierarkiet slik at det viser **HTML-hode**-sporet.</span><span class="sxs-lookup"><span data-stu-id="4d421-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="4d421-136">Velg ellipseknappen (**...**) for **HTML-hode**-sporet, og velg deretter **Legg til sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="4d421-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="4d421-137">Velg fragmentet du opprettet for skriptkoden.</span><span class="sxs-lookup"><span data-stu-id="4d421-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="4d421-138">Velg **Lagre**, og velg deretter **Fullfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="4d421-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="4d421-139">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="4d421-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="4d421-140">Legge til et eksternt skript eller innebygd skript direkte i en mal</span><span class="sxs-lookup"><span data-stu-id="4d421-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="4d421-141">Hvis du vil sette inn et innebygd eller eksternt skript direkte i et sett med sider som styres av en enkelt mal, trenger du ikke å opprette et sidefragment først.</span><span class="sxs-lookup"><span data-stu-id="4d421-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a page fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="4d421-142">Legge til et innebygd skript direkte i en mal</span><span class="sxs-lookup"><span data-stu-id="4d421-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="4d421-143">Hvis du vil legge til et innebygd skript direkte i en mal i områdebygger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="4d421-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="4d421-144">Gå til **Maler**, og åpne malen for sidene du vil legge til skriptkoden i.</span><span class="sxs-lookup"><span data-stu-id="4d421-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="4d421-145">I venstre rute utvider du malhierarkiet slik at det viser **HTML-hode**-sporet.</span><span class="sxs-lookup"><span data-stu-id="4d421-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="4d421-146">Velg ellipseknappen (**...**) for **HTML-hode**-sporet, og velg deretter **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="4d421-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4d421-147">I dialogboksen **Legg til modul** velger du **Innebygd skript**.</span><span class="sxs-lookup"><span data-stu-id="4d421-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="4d421-148">I egenskapsruten til høyre, under **Innebygd skript**, angir du skriptet på klientsiden.</span><span class="sxs-lookup"><span data-stu-id="4d421-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="4d421-149">Deretter konfigurerer du andre alternativer etter behov.</span><span class="sxs-lookup"><span data-stu-id="4d421-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="4d421-150">Velg **Lagre**, og velg deretter **Fullfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="4d421-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="4d421-151">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="4d421-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="4d421-152">Legge til et eksternt skript direkte i en mal</span><span class="sxs-lookup"><span data-stu-id="4d421-152">Add an external script directly to a template</span></span>

<span data-ttu-id="4d421-153">Hvis du vil legge til et eksternt skript direkte i en mal i områdebygger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="4d421-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="4d421-154">Gå til **Maler**, og åpne malen for sidene du vil legge til skriptkoden i.</span><span class="sxs-lookup"><span data-stu-id="4d421-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="4d421-155">I venstre rute utvider du malhierarkiet slik at det viser **HTML-hode**-sporet.</span><span class="sxs-lookup"><span data-stu-id="4d421-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="4d421-156">Velg ellipseknappen (**...**) for **HTML-hode**-sporet, og velg deretter **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="4d421-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4d421-157">I dialogboksen **Legg til modul** velger du **Eksternt skript**.</span><span class="sxs-lookup"><span data-stu-id="4d421-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="4d421-158">I egenskapsruten til høyre, under **Skriptkilde**, legger du til en ekstern eller relativ URL-adresse for den eksterne skriptkilden.</span><span class="sxs-lookup"><span data-stu-id="4d421-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="4d421-159">Deretter konfigurerer du andre alternativer etter behov.</span><span class="sxs-lookup"><span data-stu-id="4d421-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="4d421-160">Velg **Lagre**, og velg deretter **Fullfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="4d421-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="4d421-161">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="4d421-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d421-162">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4d421-162">Additional resources</span></span>

[<span data-ttu-id="4d421-163">Legge til en logo</span><span class="sxs-lookup"><span data-stu-id="4d421-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="4d421-164">Velge et områdetema</span><span class="sxs-lookup"><span data-stu-id="4d421-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="4d421-165">Arbeide med CSS-overstyringsfiler</span><span class="sxs-lookup"><span data-stu-id="4d421-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="4d421-166">Legge til et favorittikon</span><span class="sxs-lookup"><span data-stu-id="4d421-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="4d421-167">Legge til en velkomstmelding</span><span class="sxs-lookup"><span data-stu-id="4d421-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="4d421-168">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="4d421-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="4d421-169">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="4d421-169">Add languages to your site</span></span>](add-languages-to-site.md)
