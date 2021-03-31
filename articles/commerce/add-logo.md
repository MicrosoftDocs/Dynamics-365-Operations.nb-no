---
title: Legge til en logo
description: Dette emnet beskriver hvordan du legger til en logo på området ditt i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 143c1ab33547119ceab0a4fba165669bc8b22bf4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207585"
---
# <a name="add-a-logo"></a><span data-ttu-id="7944f-103">Legge til en logo</span><span class="sxs-lookup"><span data-stu-id="7944f-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7944f-104">Dette emnet beskriver hvordan du legger til en logo på området ditt i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7944f-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7944f-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="7944f-105">Overview</span></span>

<span data-ttu-id="7944f-106">Noe av det første du gjør når du bygger området, er å legge til selskapet eller merkelogoen i overskriften til området.</span><span class="sxs-lookup"><span data-stu-id="7944f-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="7944f-107">Det elektroniske modulbiblioteket for Dynamics 365 Commerce gir en modul som gjør denne oppgaven lett.</span><span class="sxs-lookup"><span data-stu-id="7944f-107">The Dynamics 365 Commerce online module library provides a module that makes this task easy.</span></span>

<span data-ttu-id="7944f-108">Du kan legge til en logo direkte i en mal, et oppsett eller en side.</span><span class="sxs-lookup"><span data-stu-id="7944f-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="7944f-109">På denne måten kan du enkelt endre logoen som vises på bestemte sider eller i grupper med sider.</span><span class="sxs-lookup"><span data-stu-id="7944f-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="7944f-110">Dette emnet dekker imidlertid det hyppigste scenarioet, der du legger til logoen din i et topptekstfragment som kan brukes på nytt på tvers av alle sidene på området.</span><span class="sxs-lookup"><span data-stu-id="7944f-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7944f-111">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="7944f-111">Prerequisites</span></span>

<span data-ttu-id="7944f-112">Før du kan legge til en logo på alle sidene på området, må du fullføre disse oppgavene.</span><span class="sxs-lookup"><span data-stu-id="7944f-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="7944f-113">Last opp logoen til mediebiblioteket.</span><span class="sxs-lookup"><span data-stu-id="7944f-113">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="7944f-114">Lag et topptekstfragment.</span><span class="sxs-lookup"><span data-stu-id="7944f-114">Create a header fragment.</span></span> <span data-ttu-id="7944f-115">Hvis du vil ha mer informasjon om hvordan du oppretter og bruker fragmenter, se [Arbeide med fragmenter](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="7944f-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="7944f-116">Inkluder topptekstfragmentet i malen som sidene på området bruker for alternativene for oppsett og modul.</span><span class="sxs-lookup"><span data-stu-id="7944f-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="7944f-117">Hvis du vil ha mer informasjon om maler, kan du se [Arbeide med maler](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="7944f-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="7944f-118">Legge til en logo i et topptekstfragment</span><span class="sxs-lookup"><span data-stu-id="7944f-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="7944f-119">Følg denne fremgangsmåten for å legge til en logo i topptekstfragmentet for området.</span><span class="sxs-lookup"><span data-stu-id="7944f-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="7944f-120">Velg **Fragmenter** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="7944f-120">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="7944f-121">Velg topptekstfragmentet du opprettet, og velg deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="7944f-121">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="7944f-122">Utvid hodemodulen.</span><span class="sxs-lookup"><span data-stu-id="7944f-122">Expand the header module.</span></span>
1. <span data-ttu-id="7944f-123">I egenskapsruten for hodemodulen angir du et bilde og en kobling for logoen.</span><span class="sxs-lookup"><span data-stu-id="7944f-123">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="7944f-124">Lagre topptekstfragmentet, fullfør redigeringen av det, og publiser det.</span><span class="sxs-lookup"><span data-stu-id="7944f-124">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="7944f-125">Når du har publisert det oppdaterte topptekstfragmentet, vil alle områdesidene som bruker malen som inneholder topptekstfragmentet, vise logoen.</span><span class="sxs-lookup"><span data-stu-id="7944f-125">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7944f-126">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="7944f-126">Additional resources</span></span>

[<span data-ttu-id="7944f-127">Velge et områdetema</span><span class="sxs-lookup"><span data-stu-id="7944f-127">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="7944f-128">Arbeide med CSS-overstyringsfiler</span><span class="sxs-lookup"><span data-stu-id="7944f-128">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="7944f-129">Legge til et favorittikon</span><span class="sxs-lookup"><span data-stu-id="7944f-129">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="7944f-130">Legge til en velkomstmelding</span><span class="sxs-lookup"><span data-stu-id="7944f-130">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="7944f-131">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="7944f-131">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="7944f-132">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="7944f-132">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="7944f-133">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="7944f-133">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]