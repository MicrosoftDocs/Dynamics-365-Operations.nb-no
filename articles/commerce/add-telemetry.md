---
title: Legge til skript kode i områdes ID-er for å støtte telemetri
description: Dette emnet beskriver hvordan du kan legge til skriptkode på klientsiden på områdesidene dine for å støtte innsamling av telemetri på klientsiden.
author: bicyclingfool
manager: annbe
ms.date: 09/29/2020
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
ms.openlocfilehash: e15ba6a0d624bd97c25936aa6d3bfafb844b66c0
ms.sourcegitcommit: 7e8a9f92a2675bf5b620889678a2918f63f3e199
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2020
ms.locfileid: "3901502"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="912f1-103">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="912f1-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="912f1-104">Dette emnet beskriver hvordan du kan legge til skriptkode på klientsiden på områdesidene dine for å støtte innsamling av telemetri på klientsiden.</span><span class="sxs-lookup"><span data-stu-id="912f1-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="912f1-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="912f1-105">Overview</span></span>

<span data-ttu-id="912f1-106">Web Analytics er et viktig verktøy når du vil forstå hvordan kundene samhandler med området og tar avgjørelser som vil bidra til å optimalisere opplevelsen for maksimal konvertering.</span><span class="sxs-lookup"><span data-stu-id="912f1-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="912f1-107">Mange Web Analytics-pakker er tilgjengelige for å hjelpe deg med å oppnå disse målene, for eksempel Google Analytics, Clicky, Moz Analytics og KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="912f1-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="912f1-108">De fleste Web Analytics-pakker krever at du legger til skriptkode på klientsiden i **\<head\>** -elementet i HTML-koden for alle sidene på området.</span><span class="sxs-lookup"><span data-stu-id="912f1-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="912f1-109">Instruksjonene i dette emnet gjelder også for annen tilpasset funksjonalitet på klientsiden som Microsoft Dynamics 365 Commerce ikke tilbyr.</span><span class="sxs-lookup"><span data-stu-id="912f1-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="912f1-110">Opprette et gjenbrukbart fragment for skriptkoden</span><span class="sxs-lookup"><span data-stu-id="912f1-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="912f1-111">Ved hjelp av et fragment kan du bruke innebygd eller ekstern skriptkode på nytt på alle sidene på området, uansett hvilken mal de bruker.</span><span class="sxs-lookup"><span data-stu-id="912f1-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="912f1-112">Opprette et gjenbrukbart fragment for den innebygde skriptkoden</span><span class="sxs-lookup"><span data-stu-id="912f1-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="912f1-113">Hvis du vil opprette et gjenbrukbart fragment for den innebygde skriptkoden i områdebygger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="912f1-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="912f1-114">Gå til **Fragmenter** , og velg deretter **Nytt** .</span><span class="sxs-lookup"><span data-stu-id="912f1-114">Go to **Fragments** , and then select **New** .</span></span>
1. <span data-ttu-id="912f1-115">I dialogboksen **Nytt fragment** velger du **Innebygd skript** .</span><span class="sxs-lookup"><span data-stu-id="912f1-115">In the **New fragment** dialog box, select **Inline script** .</span></span>
1. <span data-ttu-id="912f1-116">Under **Navn på fragment** angir du et navn på fragmentet, og deretter velger du **OK** .</span><span class="sxs-lookup"><span data-stu-id="912f1-116">Under **Fragment name** , enter a name for the fragment, and then select **OK** .</span></span>
1. <span data-ttu-id="912f1-117">Under fragmentet du opprettet, velger du modulen **Standard innebygd skript** .</span><span class="sxs-lookup"><span data-stu-id="912f1-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="912f1-118">I egenskapsruten til høyre, under **Innebygd skript** , angir du skriptet på klientsiden.</span><span class="sxs-lookup"><span data-stu-id="912f1-118">In the property pane on the right, under **Inline script** , enter your client-side script.</span></span> <span data-ttu-id="912f1-119">Deretter konfigurerer du andre alternativer etter behov.</span><span class="sxs-lookup"><span data-stu-id="912f1-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="912f1-120">Velg **Lagre** , og velg deretter **Fullfør redigering** .</span><span class="sxs-lookup"><span data-stu-id="912f1-120">Select **Save** , and then select **Finish editing** .</span></span>
1. <span data-ttu-id="912f1-121">Velg **Publiser** .</span><span class="sxs-lookup"><span data-stu-id="912f1-121">Select **Publish** .</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="912f1-122">Opprette et gjenbrukbart fragment for den eksterne skriptkoden</span><span class="sxs-lookup"><span data-stu-id="912f1-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="912f1-123">Hvis du vil opprette et gjenbrukbart fragment for den eksterne skriptkoden i områdebygger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="912f1-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="912f1-124">Gå til **Fragmenter** , og velg deretter **Nytt** .</span><span class="sxs-lookup"><span data-stu-id="912f1-124">Go to **Fragments** , and then select **New** .</span></span>
1. <span data-ttu-id="912f1-125">I dialogboksen **Nytt fragment** velger du **Eksternt skript** .</span><span class="sxs-lookup"><span data-stu-id="912f1-125">In the **New fragment** dialog box, select **External script** .</span></span>
1. <span data-ttu-id="912f1-126">Under **Navn på fragment** angir du et navn på fragmentet, og deretter velger du **OK** .</span><span class="sxs-lookup"><span data-stu-id="912f1-126">Under **Fragment name** , enter a name for the fragment, and then select **OK** .</span></span>
1. <span data-ttu-id="912f1-127">Under fragmentet du opprettet, velger du modulen **Standard eksternt skript** .</span><span class="sxs-lookup"><span data-stu-id="912f1-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="912f1-128">I egenskapsruten til høyre, under **Skriptkilde** , legger du til en ekstern eller relativ URL-adresse for den eksterne skriptkilden.</span><span class="sxs-lookup"><span data-stu-id="912f1-128">In the property pane on the right, under **Script source** , add an external or relative URL for the external script source.</span></span> <span data-ttu-id="912f1-129">Deretter konfigurerer du andre alternativer etter behov.</span><span class="sxs-lookup"><span data-stu-id="912f1-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="912f1-130">Velg **Lagre** , og velg deretter **Fullfør redigering** .</span><span class="sxs-lookup"><span data-stu-id="912f1-130">Select **Save** , and then select **Finish editing** .</span></span>
1. <span data-ttu-id="912f1-131">Velg **Publiser** .</span><span class="sxs-lookup"><span data-stu-id="912f1-131">Select **Publish** .</span></span>

> [!NOTE]
> <span data-ttu-id="912f1-132">Hvis sikkerhetspolicy for innhold (CSP) er aktivert for området, må du kontrollere at alle eksterne URL-adresser er lagt til i CSP-direktivet **script-src** i Commerce-områdebygger.</span><span class="sxs-lookup"><span data-stu-id="912f1-132">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="912f1-133">Hvis du vil ha mer informasjon, se [Behandle policy for innholdssikkerhet (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="912f1-133">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="912f1-134">Legge til et fragment som inneholder skript kode, i en mal</span><span class="sxs-lookup"><span data-stu-id="912f1-134">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="912f1-135">Hvis du vil legge til et fragment som inneholder skriptkode, i en mal i områdebygger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="912f1-135">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="912f1-136">Gå til **Maler** , og åpne malen for sidene du vil legge til skriptkoden i.</span><span class="sxs-lookup"><span data-stu-id="912f1-136">Go to **Templates** , and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="912f1-137">I venstre rute utvider du malhierarkiet slik at det viser **HTML-hode** -sporet.</span><span class="sxs-lookup"><span data-stu-id="912f1-137">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="912f1-138">Velg ellipseknappen ( **...** ) for sporet **HTML-hode** , og velg deretter **Legg til fragment** .</span><span class="sxs-lookup"><span data-stu-id="912f1-138">In the **HTML Head** slot, select the ellipsis button ( **...** ), and then select **Add fragment** .</span></span>
1. <span data-ttu-id="912f1-139">Velg fragmentet du opprettet for skriptkoden.</span><span class="sxs-lookup"><span data-stu-id="912f1-139">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="912f1-140">Velg **Lagre** , og velg deretter **Fullfør redigering** .</span><span class="sxs-lookup"><span data-stu-id="912f1-140">Select **Save** , and then select **Finish editing** .</span></span>
1. <span data-ttu-id="912f1-141">Velg **Publiser** .</span><span class="sxs-lookup"><span data-stu-id="912f1-141">Select **Publish** .</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="912f1-142">Legge til et eksternt skript eller innebygd skript direkte i en mal</span><span class="sxs-lookup"><span data-stu-id="912f1-142">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="912f1-143">Hvis du vil sette inn et innebygd eller eksternt skript direkte i et sett med sider som styres av en enkelt mal, trenger du ikke å opprette et fragment først.</span><span class="sxs-lookup"><span data-stu-id="912f1-143">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="912f1-144">Legge til et innebygd skript direkte i en mal</span><span class="sxs-lookup"><span data-stu-id="912f1-144">Add an inline script directly to a template</span></span>

<span data-ttu-id="912f1-145">Hvis du vil legge til et innebygd skript direkte i en mal i områdebygger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="912f1-145">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="912f1-146">Gå til **Maler** , og åpne malen for sidene du vil legge til skriptkoden i.</span><span class="sxs-lookup"><span data-stu-id="912f1-146">Go to **Templates** , and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="912f1-147">I venstre rute utvider du malhierarkiet slik at det viser **HTML-hode** -sporet.</span><span class="sxs-lookup"><span data-stu-id="912f1-147">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="912f1-148">Velg ellipseknappen ( **...** ) for **HTML-hode** -sporet, og velg deretter **Legg til modul** .</span><span class="sxs-lookup"><span data-stu-id="912f1-148">In the **HTML Head** slot, select the ellipsis button ( **...** ), and then select **Add Module** .</span></span>
1. <span data-ttu-id="912f1-149">I dialogboksen **Legg til modul** velger du **Innebygd skript** .</span><span class="sxs-lookup"><span data-stu-id="912f1-149">In the **Add Module** dialog box, select **Inline script** .</span></span>
1. <span data-ttu-id="912f1-150">I egenskapsruten til høyre, under **Innebygd skript** , angir du skriptet på klientsiden.</span><span class="sxs-lookup"><span data-stu-id="912f1-150">In the property pane on the right, under **Inline script** , enter your client-side script.</span></span> <span data-ttu-id="912f1-151">Deretter konfigurerer du andre alternativer etter behov.</span><span class="sxs-lookup"><span data-stu-id="912f1-151">Then configure other options as you require.</span></span>
1. <span data-ttu-id="912f1-152">Velg **Lagre** , og velg deretter **Fullfør redigering** .</span><span class="sxs-lookup"><span data-stu-id="912f1-152">Select **Save** , and then select **Finish editing** .</span></span>
1. <span data-ttu-id="912f1-153">Velg **Publiser** .</span><span class="sxs-lookup"><span data-stu-id="912f1-153">Select **Publish** .</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="912f1-154">Legge til et eksternt skript direkte i en mal</span><span class="sxs-lookup"><span data-stu-id="912f1-154">Add an external script directly to a template</span></span>

<span data-ttu-id="912f1-155">Hvis du vil legge til et eksternt skript direkte i en mal i områdebygger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="912f1-155">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="912f1-156">Gå til **Maler** , og åpne malen for sidene du vil legge til skriptkoden i.</span><span class="sxs-lookup"><span data-stu-id="912f1-156">Go to **Templates** , and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="912f1-157">I venstre rute utvider du malhierarkiet slik at det viser **HTML-hode** -sporet.</span><span class="sxs-lookup"><span data-stu-id="912f1-157">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="912f1-158">Velg ellipseknappen ( **...** ) for **HTML-hode** -sporet, og velg deretter **Legg til modul** .</span><span class="sxs-lookup"><span data-stu-id="912f1-158">In the **HTML Head** slot, select the ellipsis button ( **...** ), and then select **Add Module** .</span></span>
1. <span data-ttu-id="912f1-159">I dialogboksen **Legg til modul** velger du **Eksternt skript** .</span><span class="sxs-lookup"><span data-stu-id="912f1-159">In the **Add Module** dialog box, select **External script** .</span></span>
1. <span data-ttu-id="912f1-160">I egenskapsruten til høyre, under **Skriptkilde** , legger du til en ekstern eller relativ URL-adresse for den eksterne skriptkilden.</span><span class="sxs-lookup"><span data-stu-id="912f1-160">In the property pane on the right, under **Script source** , add an external or relative URL for the external script source.</span></span> <span data-ttu-id="912f1-161">Deretter konfigurerer du andre alternativer etter behov.</span><span class="sxs-lookup"><span data-stu-id="912f1-161">Then configure other options as you require.</span></span>
1. <span data-ttu-id="912f1-162">Velg **Lagre** , og velg deretter **Fullfør redigering** .</span><span class="sxs-lookup"><span data-stu-id="912f1-162">Select **Save** , and then select **Finish editing** .</span></span>
1. <span data-ttu-id="912f1-163">Velg **Publiser** .</span><span class="sxs-lookup"><span data-stu-id="912f1-163">Select **Publish** .</span></span>

## <a name="additional-resources"></a><span data-ttu-id="912f1-164">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="912f1-164">Additional resources</span></span>

[<span data-ttu-id="912f1-165">Legge til en logo</span><span class="sxs-lookup"><span data-stu-id="912f1-165">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="912f1-166">Velge et områdetema</span><span class="sxs-lookup"><span data-stu-id="912f1-166">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="912f1-167">Arbeide med CSS-overstyringsfiler</span><span class="sxs-lookup"><span data-stu-id="912f1-167">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="912f1-168">Legge til et favorittikon</span><span class="sxs-lookup"><span data-stu-id="912f1-168">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="912f1-169">Legge til en velkomstmelding</span><span class="sxs-lookup"><span data-stu-id="912f1-169">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="912f1-170">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="912f1-170">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="912f1-171">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="912f1-171">Add languages to your site</span></span>](add-languages-to-site.md)
