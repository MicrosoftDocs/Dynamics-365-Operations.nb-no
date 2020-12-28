---
title: Iframe-modul
description: Dette emnet dekker iFrame-modulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 4afd8f60938c99d1981be1625ef28f91d9e4bb4c
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665402"
---
# <a name="iframe-module"></a><span data-ttu-id="c5f66-103">Iframe-modul</span><span class="sxs-lookup"><span data-stu-id="c5f66-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c5f66-104">Dette emnet dekker iFrame-modulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c5f66-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c5f66-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="c5f66-105">Overview</span></span>

<span data-ttu-id="c5f66-106">En iFrame-modul gir en iFrame (innebygd ramme) som er vert for eksternt innhold på et område.</span><span class="sxs-lookup"><span data-stu-id="c5f66-106">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="c5f66-107">Den kan for eksempel brukes til å være vert for en YouTube-video eller PDF-filvisning på en områdeside.</span><span class="sxs-lookup"><span data-stu-id="c5f66-107">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="c5f66-108">En iFrame-modul krever en mål-URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="c5f66-108">An iframe module requires a target URL.</span></span> <span data-ttu-id="c5f66-109">Deretter er den vert for innholdet på målsiden i et HTML **iFrame**-element.</span><span class="sxs-lookup"><span data-stu-id="c5f66-109">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="c5f66-110">Eksterne URL-adresser må være på tillatelseslisten i henhold til områdets sikkerhetspolicy for innhold (CSP).</span><span class="sxs-lookup"><span data-stu-id="c5f66-110">External URLs must be on the allow list per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="c5f66-111">For iFrame-innhold bør URL-adresser tillates ved å bruke direktivet **frame-ancestor**.</span><span class="sxs-lookup"><span data-stu-id="c5f66-111">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="c5f66-112">Hvis du vil ha mer informasjon, se [Behandle policy for innholdssikkerhet (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="c5f66-112">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

> [!NOTE]
> <span data-ttu-id="c5f66-113">iFrame-modulen er tilgjengelig i Dynamics 365 Commerce 10.0.13-versjonen.</span><span class="sxs-lookup"><span data-stu-id="c5f66-113">The iframe module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="c5f66-114">Det følgende bildet viser eksempler på iFrame-moduler som viser eksterne videoer på områdesider.</span><span class="sxs-lookup"><span data-stu-id="c5f66-114">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![Eksempel på iFrame-moduler som viser eksterne videoer](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="c5f66-116">Egenskaper for iFrame-modul</span><span class="sxs-lookup"><span data-stu-id="c5f66-116">Iframe module properties</span></span>

| <span data-ttu-id="c5f66-117">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="c5f66-117">Property name</span></span>             | <span data-ttu-id="c5f66-118">Verdi</span><span class="sxs-lookup"><span data-stu-id="c5f66-118">Value</span></span>                 | <span data-ttu-id="c5f66-119">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c5f66-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="c5f66-120">Overskrift</span><span class="sxs-lookup"><span data-stu-id="c5f66-120">Heading</span></span> | <span data-ttu-id="c5f66-121">Tekst</span><span class="sxs-lookup"><span data-stu-id="c5f66-121">Text</span></span> | <span data-ttu-id="c5f66-122">Overskriften for modulen.</span><span class="sxs-lookup"><span data-stu-id="c5f66-122">The heading for the module.</span></span> |
| <span data-ttu-id="c5f66-123">Mål-URL-adresse</span><span class="sxs-lookup"><span data-stu-id="c5f66-123">Target URL</span></span> | <span data-ttu-id="c5f66-124">URL</span><span class="sxs-lookup"><span data-stu-id="c5f66-124">URL</span></span> | <span data-ttu-id="c5f66-125">URL-adressen som vertsmodulen ligger i.</span><span class="sxs-lookup"><span data-stu-id="c5f66-125">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="c5f66-126">Høyde</span><span class="sxs-lookup"><span data-stu-id="c5f66-126">Height</span></span> | <span data-ttu-id="c5f66-127">Tall eller prosent</span><span class="sxs-lookup"><span data-stu-id="c5f66-127">Number or percentage</span></span> | <span data-ttu-id="c5f66-128">Høyden på modulen, i piksler eller som en prosent.</span><span class="sxs-lookup"><span data-stu-id="c5f66-128">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="c5f66-129">Verdien **100** vil for eksempel bli behandlet som antall piksler, og verdien **100 %** vil bli behandlet som en prosent.</span><span class="sxs-lookup"><span data-stu-id="c5f66-129">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="c5f66-130">Aria-etikett</span><span class="sxs-lookup"><span data-stu-id="c5f66-130">Aria label</span></span> | <span data-ttu-id="c5f66-131">Tekst</span><span class="sxs-lookup"><span data-stu-id="c5f66-131">Text</span></span> | <span data-ttu-id="c5f66-132">En ARIA-etikett (Accessible Rich Internet Applications) kan defineres for tilgjengelighetsformål.</span><span class="sxs-lookup"><span data-stu-id="c5f66-132">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="c5f66-133">Legg til en iFrame-modul på en side</span><span class="sxs-lookup"><span data-stu-id="c5f66-133">Add an iframe module to a page</span></span>

<span data-ttu-id="c5f66-134">Følg denne fremgangsmåten for å legge til en iFrame-modul på en side for å vise en ekstern video.</span><span class="sxs-lookup"><span data-stu-id="c5f66-134">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="c5f66-135">Gå til **Maler**, og velg **Ny** for å opprette en ny mal.</span><span class="sxs-lookup"><span data-stu-id="c5f66-135">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="c5f66-136">I dialogboksen **Ny mal**, under **Malnavn**, angir du **Markedsføringsmal**, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5f66-136">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="c5f66-137">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="c5f66-137">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="c5f66-138">Gå til **Sider**, og velg **Ny** for å opprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="c5f66-138">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="c5f66-139">I **Velg en mal**-dialogboksen velger du malen **Markedsføringsmal**.</span><span class="sxs-lookup"><span data-stu-id="c5f66-139">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="c5f66-140">Under **Sidenavn** angir du **Markedsføringsside**, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5f66-140">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="c5f66-141">På **Hoved**-sporet på den nye siden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="c5f66-141">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c5f66-142">I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5f66-142">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c5f66-143">I modulens egenskaperrute setter du **Bredde**-verdien til **Fyll container**.</span><span class="sxs-lookup"><span data-stu-id="c5f66-143">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="c5f66-144">I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="c5f66-144">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c5f66-145">I dialogboksen **Legg til modul** velger du **iFrame**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5f66-145">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c5f66-146">I modulens egenskapsrute angir du verdien for **Mål-URL-adresse** til en ekstern URL-adresse for en video.</span><span class="sxs-lookup"><span data-stu-id="c5f66-146">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="c5f66-147">Angi andre egenskaper, for eksempel **Overskrift** og **Høyde** etter behov.</span><span class="sxs-lookup"><span data-stu-id="c5f66-147">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="c5f66-148">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="c5f66-148">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="c5f66-149">Gå til markedsføringssiden på området.</span><span class="sxs-lookup"><span data-stu-id="c5f66-149">Go to the marketing page on your site.</span></span> <span data-ttu-id="c5f66-150">Du skal se at videoen gjengis i iFrame-modulen.</span><span class="sxs-lookup"><span data-stu-id="c5f66-150">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="c5f66-151">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c5f66-151">Additional resources</span></span>

[<span data-ttu-id="c5f66-152">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="c5f66-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c5f66-153">Behandle policy for innholdssikkerhet (CSP)</span><span class="sxs-lookup"><span data-stu-id="c5f66-153">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
