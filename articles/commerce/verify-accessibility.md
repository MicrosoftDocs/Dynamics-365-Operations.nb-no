---
title: Kontrollere tilgjengelighet for sideinnhold
description: Dette emnet beskriver hvordan du kontrollerer tilgjengeligheten for sideinnhold i Microsoft Dynamics 365 Commerce.
author: josaw1
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 186044fc7a360f227cecffb39bad0e225245dd4d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210977"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="91776-103">Kontrollere tilgjengelighet for sideinnhold</span><span class="sxs-lookup"><span data-stu-id="91776-103">Verify page content accessibility</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="91776-104">Dette emnet beskriver hvordan du kontrollerer tilgjengeligheten for sideinnhold i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="91776-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="91776-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="91776-105">Overview</span></span>

<span data-ttu-id="91776-106">Når du er ferdig med å endre en side, bør du sørge for at innholdet er tilgjengelig for alle på Internett.</span><span class="sxs-lookup"><span data-stu-id="91776-106">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="91776-107">I redigeringsverktøyene for handel kan du enkelt kontrollere tilgjengeligheten til sideinnholdet ved hjelp av den integrerte [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="91776-107">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="91776-108">Denne tjenesten verifiserer sideinnholdet ditt mot de seneste retningslinjene for [tilgjengelighet i World Wide Web Consortium (W3C)](https://www.w3.org/standards/webdesign/accessibility).</span><span class="sxs-lookup"><span data-stu-id="91776-108">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="91776-109">[Microsoft Accessibility Insights](https://accessibilityinsights.io/)-integreringen må være aktivert på leier- eller områdenivået før du kan bruke den.</span><span class="sxs-lookup"><span data-stu-id="91776-109">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="91776-110">Aktivere Microsoft Accessibility Insights for alle områdene i leieren</span><span class="sxs-lookup"><span data-stu-id="91776-110">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="91776-111">Følg denne fremgangsmåten for å aktivere [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-integrasjon for alle Commerce-områder i leieren.</span><span class="sxs-lookup"><span data-stu-id="91776-111">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="91776-112">For å få tilgang til leierinnstillinger må du være logget på Commerce som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="91776-112">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="91776-113">Logg på Commerce som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="91776-113">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="91776-114">I den venstre navigasjonsruten velger **Leierinnstillinger** (ved siden av tannhjulsymbolet) for å utvide den.</span><span class="sxs-lookup"><span data-stu-id="91776-114">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="91776-115">Velg **Funksjoner** under **Leierinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="91776-115">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="91776-116">Sett alternativet **Tilgjengelighetskontroll** til **På**.</span><span class="sxs-lookup"><span data-stu-id="91776-116">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="91776-117">Aktivere Microsoft Accessibility Insights for et enkelt område</span><span class="sxs-lookup"><span data-stu-id="91776-117">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="91776-118">Følg denne fremgangsmåten for å aktivere [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-integrasjon for et enkelt Commerce-område.</span><span class="sxs-lookup"><span data-stu-id="91776-118">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="91776-119">Under **Områder** velger du **Fabrikam** (eller navnet på området).</span><span class="sxs-lookup"><span data-stu-id="91776-119">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="91776-120">Velg **Områdeinnstillinger** i navigasjonsruten til venstre for å utvide den.</span><span class="sxs-lookup"><span data-stu-id="91776-120">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="91776-121">Velg **Funksjoner** under **Områdeinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="91776-121">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="91776-122">Sett alternativet **Tilgjengelighetskontroll** til **På**.</span><span class="sxs-lookup"><span data-stu-id="91776-122">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="91776-123">Kontrollere tilgjengeligheten til innholdet på startsiden</span><span class="sxs-lookup"><span data-stu-id="91776-123">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="91776-124">Hvis du vil bruke den integrerte [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-tjenesten til å skanne og kontrollere innholdet på startsiden i Commerce, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="91776-124">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="91776-125">Under **Områder** velger du **Fabrikam** (eller navnet på området).</span><span class="sxs-lookup"><span data-stu-id="91776-125">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="91776-126">Velg **Sider** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="91776-126">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="91776-127">Finn og velg startsside for å åpne den i sideredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="91776-127">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="91776-128">På kommandolinjen velger du **Kontroller tilgjengelighet**.</span><span class="sxs-lookup"><span data-stu-id="91776-128">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="91776-129">Siden **Kontroller tilgjengelighet** vises.</span><span class="sxs-lookup"><span data-stu-id="91776-129">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="91776-130">Når skanningen er fullført, kan du se gjennom innholdet i rapporten.</span><span class="sxs-lookup"><span data-stu-id="91776-130">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="91776-131">Hvis noen av kontrollene mislyktes, velger du hvert mislykket kontrollelement for å utvide det slik at du kan vise flere detaljer.</span><span class="sxs-lookup"><span data-stu-id="91776-131">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="91776-132">Hvis du vil lukke rapporten etter at du er ferdig med å se gjennom den, blar du til bunnan av siden **Kontroller tilgjengelighet** og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="91776-132">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91776-133">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="91776-133">Additional resources</span></span>

[<span data-ttu-id="91776-134">Endre en eksisterende områdeside</span><span class="sxs-lookup"><span data-stu-id="91776-134">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="91776-135">Legg til en ny områdeside</span><span class="sxs-lookup"><span data-stu-id="91776-135">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="91776-136">Velge sideoppsett</span><span class="sxs-lookup"><span data-stu-id="91776-136">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="91776-137">Behandle metadata for søkemotor</span><span class="sxs-lookup"><span data-stu-id="91776-137">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="91776-138">Lagre, forhåndsvise og publisere en side</span><span class="sxs-lookup"><span data-stu-id="91776-138">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="91776-139">Supplere en produktside</span><span class="sxs-lookup"><span data-stu-id="91776-139">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="91776-140">Supplere en kategorimålside</span><span class="sxs-lookup"><span data-stu-id="91776-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="91776-141">Opprette dynamiske e-handelssider basert på URL-parametere</span><span class="sxs-lookup"><span data-stu-id="91776-141">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]