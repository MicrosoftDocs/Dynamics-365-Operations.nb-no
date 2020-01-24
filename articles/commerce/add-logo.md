---
title: Legge til en logo
description: Dette emnet beskriver hvordan du legger til en logo på området ditt i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914630"
---
# <a name="add-a-logo"></a><span data-ttu-id="0ace2-103">Legge til en logo</span><span class="sxs-lookup"><span data-stu-id="0ace2-103">Add a logo</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="0ace2-104">Dette emnet beskriver hvordan du legger til en logo på området ditt i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0ace2-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0ace2-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="0ace2-105">Overview</span></span>

<span data-ttu-id="0ace2-106">Noe av det første du gjør når du bygger området, er å legge til selskapet eller merkelogoen i overskriften til området.</span><span class="sxs-lookup"><span data-stu-id="0ace2-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="0ace2-107">Den elektroniske startpakken for Dynamics 365 Commerce gir en modul som gjør denne oppgaven lett.</span><span class="sxs-lookup"><span data-stu-id="0ace2-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="0ace2-108">Du kan legge til en logo direkte i en mal, et oppsett eller en side.</span><span class="sxs-lookup"><span data-stu-id="0ace2-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="0ace2-109">På denne måten kan du enkelt endre logoen som vises på bestemte sider eller i grupper med sider.</span><span class="sxs-lookup"><span data-stu-id="0ace2-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="0ace2-110">Dette emnet dekker imidlertid det hyppigste scenarioet, der du legger til logoen din i et topptekstfragment som kan brukes på nytt på tvers av alle sidene på området.</span><span class="sxs-lookup"><span data-stu-id="0ace2-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0ace2-111">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="0ace2-111">Prerequisites</span></span>

<span data-ttu-id="0ace2-112">Før du kan legge til en logo på alle sidene på området, må du fullføre disse oppgavene.</span><span class="sxs-lookup"><span data-stu-id="0ace2-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="0ace2-113">Last opp logoen din til den digitale innholdsbehandleren, som du kan få tilgang til fra **Aktiva**-siden.</span><span class="sxs-lookup"><span data-stu-id="0ace2-113">Upload your logo to the digital assets manager, which you can access from the **Assets** page.</span></span>
1. <span data-ttu-id="0ace2-114">Lag et topptekstfragment.</span><span class="sxs-lookup"><span data-stu-id="0ace2-114">Create a header fragment.</span></span> <span data-ttu-id="0ace2-115">Hvis du vil ha mer informasjon om hvordan du oppretter og bruker fragmenter, se [Arbeide med fragmenter](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="0ace2-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="0ace2-116">Inkluder topptekstfragmentet i malen som sidene på området bruker for alternativene for oppsett og modul.</span><span class="sxs-lookup"><span data-stu-id="0ace2-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="0ace2-117">Hvis du vil ha mer informasjon om maler, kan du se [Arbeide med maler](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="0ace2-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="0ace2-118">Legge til en logo i et topptekstfragment</span><span class="sxs-lookup"><span data-stu-id="0ace2-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="0ace2-119">Følg denne fremgangsmåten for å legge til en logo i topptekstfragmentet for området.</span><span class="sxs-lookup"><span data-stu-id="0ace2-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="0ace2-120">Velg **Fragmenter** i navigasjonsruten til venstre, og velg deretter topptekstfragmentet du har opprettet.</span><span class="sxs-lookup"><span data-stu-id="0ace2-120">In the navigation pane on the left, select **Fragments**, and then select the header fragment that you created.</span></span>
2. <span data-ttu-id="0ace2-121">Velg **Sjekk ut**.</span><span class="sxs-lookup"><span data-stu-id="0ace2-121">Select **Check out**.</span></span>
3. <span data-ttu-id="0ace2-122">Utvid **Topptekst**-sporet og **Logo**-sporet.</span><span class="sxs-lookup"><span data-stu-id="0ace2-122">Expand the **Header** slot and the **Logo** slot.</span></span>
4. <span data-ttu-id="0ace2-123">Velg ellipseknappen (**...**) for **Logo**-sporet, og velg deretter **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="0ace2-123">Select the ellipsis button (**...**) for the **Logo** slot, and then select **Add module**.</span></span>
5. <span data-ttu-id="0ace2-124">Velg logomodulen.</span><span class="sxs-lookup"><span data-stu-id="0ace2-124">Select the logo module.</span></span>
6. <span data-ttu-id="0ace2-125">I egenskapsruten til høyre konfigurerer du logomodulen slik at den viser logoen din.</span><span class="sxs-lookup"><span data-stu-id="0ace2-125">In the properties pane on the right, configure the logo module so that it shows your logo.</span></span>
7. <span data-ttu-id="0ace2-126">Lagre topptekstfragmentet, sjekk det inn, og publiser det.</span><span class="sxs-lookup"><span data-stu-id="0ace2-126">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="0ace2-127">Når du har publisert det oppdaterte topptekstfragmentet, vil alle områdesidene som bruker malen som inneholder topptekstfragmentet, vise logoen.</span><span class="sxs-lookup"><span data-stu-id="0ace2-127">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ace2-128">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0ace2-128">Additional resources</span></span>

[<span data-ttu-id="0ace2-129">Velge et områdetema</span><span class="sxs-lookup"><span data-stu-id="0ace2-129">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="0ace2-130">Arbeide med CSS-overstyringsfiler</span><span class="sxs-lookup"><span data-stu-id="0ace2-130">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="0ace2-131">Legge til et favorittikon</span><span class="sxs-lookup"><span data-stu-id="0ace2-131">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="0ace2-132">Legge til en velkomstmelding</span><span class="sxs-lookup"><span data-stu-id="0ace2-132">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="0ace2-133">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="0ace2-133">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="0ace2-134">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="0ace2-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="0ace2-135">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="0ace2-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

