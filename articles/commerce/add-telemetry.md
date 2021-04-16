---
title: Legge til skript kode i områdes ID-er for å støtte telemetri
description: Dette emnet beskriver hvordan du kan legge til skriptkode på klientsiden på områdesidene dine for å støtte innsamling av telemetri på klientsiden.
author: bicyclingfool
ms.date: 09/29/2020
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
ms.openlocfilehash: fb1773ab10b23a586eb6a8286f145181818585b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797437"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="5eb31-103">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="5eb31-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5eb31-104">Dette emnet beskriver hvordan du kan legge til skriptkode på klientsiden på områdesidene dine for å støtte innsamling av telemetri på klientsiden.</span><span class="sxs-lookup"><span data-stu-id="5eb31-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

<span data-ttu-id="5eb31-105">Web Analytics er et viktig verktøy når du vil forstå hvordan kundene samhandler med området og tar avgjørelser som vil bidra til å optimalisere opplevelsen for maksimal konvertering.</span><span class="sxs-lookup"><span data-stu-id="5eb31-105">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="5eb31-106">Mange Web Analytics-pakker er tilgjengelige for å hjelpe deg med å oppnå disse målene, for eksempel Google Analytics, Clicky, Moz Analytics og KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="5eb31-106">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="5eb31-107">De fleste Web Analytics-pakker krever at du legger til skriptkode på klientsiden i **\<head\>**-elementet i HTML-koden for alle sidene på området.</span><span class="sxs-lookup"><span data-stu-id="5eb31-107">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="5eb31-108">Instruksjonene i dette emnet gjelder også for annen tilpasset funksjonalitet på klientsiden som Microsoft Dynamics 365 Commerce ikke tilbyr.</span><span class="sxs-lookup"><span data-stu-id="5eb31-108">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="5eb31-109">Opprette et gjenbrukbart fragment for skriptkoden</span><span class="sxs-lookup"><span data-stu-id="5eb31-109">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="5eb31-110">Ved hjelp av et fragment kan du bruke innebygd eller ekstern skriptkode på nytt på alle sidene på området, uansett hvilken mal de bruker.</span><span class="sxs-lookup"><span data-stu-id="5eb31-110">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="5eb31-111">Opprette et gjenbrukbart fragment for den innebygde skriptkoden</span><span class="sxs-lookup"><span data-stu-id="5eb31-111">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="5eb31-112">Hvis du vil opprette et gjenbrukbart fragment for den innebygde skriptkoden i områdebygger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="5eb31-112">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="5eb31-113">Gå til **Fragmenter**, og velg deretter **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-113">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="5eb31-114">I dialogboksen **Nytt fragment** velger du **Innebygd skript**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-114">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="5eb31-115">Under **Navn på fragment** angir du et navn på fragmentet, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-115">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="5eb31-116">Under fragmentet du opprettet, velger du modulen **Standard innebygd skript**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-116">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="5eb31-117">I egenskapsruten til høyre, under **Innebygd skript**, angir du skriptet på klientsiden.</span><span class="sxs-lookup"><span data-stu-id="5eb31-117">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="5eb31-118">Deretter konfigurerer du andre alternativer etter behov.</span><span class="sxs-lookup"><span data-stu-id="5eb31-118">Then configure other options as you require.</span></span>
1. <span data-ttu-id="5eb31-119">Velg **Lagre**, og velg deretter **Fullfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-119">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="5eb31-120">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-120">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="5eb31-121">Opprette et gjenbrukbart fragment for den eksterne skriptkoden</span><span class="sxs-lookup"><span data-stu-id="5eb31-121">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="5eb31-122">Hvis du vil opprette et gjenbrukbart fragment for den eksterne skriptkoden i områdebygger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="5eb31-122">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="5eb31-123">Gå til **Fragmenter**, og velg deretter **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-123">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="5eb31-124">I dialogboksen **Nytt fragment** velger du **Eksternt skript**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-124">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="5eb31-125">Under **Navn på fragment** angir du et navn på fragmentet, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-125">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="5eb31-126">Under fragmentet du opprettet, velger du modulen **Standard eksternt skript**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-126">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="5eb31-127">I egenskapsruten til høyre, under **Skriptkilde**, legger du til en ekstern eller relativ URL-adresse for den eksterne skriptkilden.</span><span class="sxs-lookup"><span data-stu-id="5eb31-127">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="5eb31-128">Deretter konfigurerer du andre alternativer etter behov.</span><span class="sxs-lookup"><span data-stu-id="5eb31-128">Then configure other options as you require.</span></span>
1. <span data-ttu-id="5eb31-129">Velg **Lagre**, og velg deretter **Fullfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="5eb31-130">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-130">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="5eb31-131">Hvis sikkerhetspolicy for innhold (CSP) er aktivert for området, må du kontrollere at alle eksterne URL-adresser er lagt til i CSP-direktivet **script-src** i Commerce-områdebygger.</span><span class="sxs-lookup"><span data-stu-id="5eb31-131">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="5eb31-132">Hvis du vil ha mer informasjon, se [Behandle policy for innholdssikkerhet (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="5eb31-132">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="5eb31-133">Legge til et fragment som inneholder skript kode, i en mal</span><span class="sxs-lookup"><span data-stu-id="5eb31-133">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="5eb31-134">Hvis du vil legge til et fragment som inneholder skriptkode, i en mal i områdebygger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="5eb31-134">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="5eb31-135">Gå til **Maler**, og åpne malen for sidene du vil legge til skriptkoden i.</span><span class="sxs-lookup"><span data-stu-id="5eb31-135">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="5eb31-136">I venstre rute utvider du malhierarkiet slik at det viser **HTML-hode**-sporet.</span><span class="sxs-lookup"><span data-stu-id="5eb31-136">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="5eb31-137">Velg ellipseknappen (**...**) for sporet **HTML-hode**, og velg deretter **Legg til fragment**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-137">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="5eb31-138">Velg fragmentet du opprettet for skriptkoden.</span><span class="sxs-lookup"><span data-stu-id="5eb31-138">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="5eb31-139">Velg **Lagre**, og velg deretter **Fullfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-139">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="5eb31-140">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-140">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="5eb31-141">Legge til et eksternt skript eller innebygd skript direkte i en mal</span><span class="sxs-lookup"><span data-stu-id="5eb31-141">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="5eb31-142">Hvis du vil sette inn et innebygd eller eksternt skript direkte i et sett med sider som styres av en enkelt mal, trenger du ikke å opprette et fragment først.</span><span class="sxs-lookup"><span data-stu-id="5eb31-142">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="5eb31-143">Legge til et innebygd skript direkte i en mal</span><span class="sxs-lookup"><span data-stu-id="5eb31-143">Add an inline script directly to a template</span></span>

<span data-ttu-id="5eb31-144">Hvis du vil legge til et innebygd skript direkte i en mal i områdebygger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="5eb31-144">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="5eb31-145">Gå til **Maler**, og åpne malen for sidene du vil legge til skriptkoden i.</span><span class="sxs-lookup"><span data-stu-id="5eb31-145">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="5eb31-146">I venstre rute utvider du malhierarkiet slik at det viser **HTML-hode**-sporet.</span><span class="sxs-lookup"><span data-stu-id="5eb31-146">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="5eb31-147">Velg ellipseknappen (**...**) for **HTML-hode**-sporet, og velg deretter **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-147">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5eb31-148">I dialogboksen **Legg til modul** velger du **Innebygd skript**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-148">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="5eb31-149">I egenskapsruten til høyre, under **Innebygd skript**, angir du skriptet på klientsiden.</span><span class="sxs-lookup"><span data-stu-id="5eb31-149">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="5eb31-150">Deretter konfigurerer du andre alternativer etter behov.</span><span class="sxs-lookup"><span data-stu-id="5eb31-150">Then configure other options as you require.</span></span>
1. <span data-ttu-id="5eb31-151">Velg **Lagre**, og velg deretter **Fullfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-151">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="5eb31-152">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-152">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="5eb31-153">Legge til et eksternt skript direkte i en mal</span><span class="sxs-lookup"><span data-stu-id="5eb31-153">Add an external script directly to a template</span></span>

<span data-ttu-id="5eb31-154">Hvis du vil legge til et eksternt skript direkte i en mal i områdebygger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="5eb31-154">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="5eb31-155">Gå til **Maler**, og åpne malen for sidene du vil legge til skriptkoden i.</span><span class="sxs-lookup"><span data-stu-id="5eb31-155">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="5eb31-156">I venstre rute utvider du malhierarkiet slik at det viser **HTML-hode**-sporet.</span><span class="sxs-lookup"><span data-stu-id="5eb31-156">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="5eb31-157">Velg ellipseknappen (**...**) for **HTML-hode**-sporet, og velg deretter **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-157">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5eb31-158">I dialogboksen **Legg til modul** velger du **Eksternt skript**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-158">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="5eb31-159">I egenskapsruten til høyre, under **Skriptkilde**, legger du til en ekstern eller relativ URL-adresse for den eksterne skriptkilden.</span><span class="sxs-lookup"><span data-stu-id="5eb31-159">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="5eb31-160">Deretter konfigurerer du andre alternativer etter behov.</span><span class="sxs-lookup"><span data-stu-id="5eb31-160">Then configure other options as you require.</span></span>
1. <span data-ttu-id="5eb31-161">Velg **Lagre**, og velg deretter **Fullfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-161">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="5eb31-162">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="5eb31-162">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5eb31-163">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5eb31-163">Additional resources</span></span>

[<span data-ttu-id="5eb31-164">Legge til en logo</span><span class="sxs-lookup"><span data-stu-id="5eb31-164">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="5eb31-165">Velge et områdetema</span><span class="sxs-lookup"><span data-stu-id="5eb31-165">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="5eb31-166">Arbeide med CSS-overstyringsfiler</span><span class="sxs-lookup"><span data-stu-id="5eb31-166">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="5eb31-167">Legge til et favorittikon</span><span class="sxs-lookup"><span data-stu-id="5eb31-167">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="5eb31-168">Legge til en velkomstmelding</span><span class="sxs-lookup"><span data-stu-id="5eb31-168">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="5eb31-169">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="5eb31-169">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="5eb31-170">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="5eb31-170">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
