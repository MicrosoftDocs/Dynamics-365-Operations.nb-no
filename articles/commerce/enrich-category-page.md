---
title: Supplere en kategorimålside
description: Dette emnet dekker supplering av kategorisider i Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5e18439fc0e91619cade33b83b87be0d5c4d1040
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799017"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="b4086-103">Supplere en kategorimålside</span><span class="sxs-lookup"><span data-stu-id="b4086-103">Enrich a category landing page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b4086-104">Dette emnet dekker supplering av kategorisider i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b4086-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b4086-105">Commerce leverer en standard kategorimålside som brukes når kategoridata vises.</span><span class="sxs-lookup"><span data-stu-id="b4086-105">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="b4086-106">En standard kategoriside inneholder nødvendige elementer, for eksempel presiseringer, kategoriserte produktplasseringer, sorteringsalternativer, et valgsammendrag og sidenummereringskontroller.</span><span class="sxs-lookup"><span data-stu-id="b4086-106">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="b4086-107">I stedet for å bruke standard kategoriside kan det imidlertid være lurt å bruke en "supplert" kategorimålside med mer innhold og mer spesifikke elementer.</span><span class="sxs-lookup"><span data-stu-id="b4086-107">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="b4086-108">Et typisk supplement kan involvere å legge til kategorispesifikt markedsføringsinnhold på kategorisiden.</span><span class="sxs-lookup"><span data-stu-id="b4086-108">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="b4086-109">Dette innholdet kan inkludere produktplassering på tvers av kategorier for kryssalgsformål, redigeringslister, bilder, videoer og annen tekst.</span><span class="sxs-lookup"><span data-stu-id="b4086-109">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="b4086-110">Du kan enten endre standard kategoriside eller definere en annen kategoriside for en bestemt kategori.</span><span class="sxs-lookup"><span data-stu-id="b4086-110">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Supplere kategorimålside](./media/CategoryLandingPages.png)

<span data-ttu-id="b4086-112">I Commerce-områdebyggeren inneholder siden **Produkter** en liste over kategorier fra kanalen som er tilordnet området.</span><span class="sxs-lookup"><span data-stu-id="b4086-112">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="b4086-113">Hvis statusen **Supplert** er valgt for en kategoriside, er denne kategorisiden supplert.</span><span class="sxs-lookup"><span data-stu-id="b4086-113">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="b4086-114">Hvis ikke brukes standard kategoriside og -innhold for kategorien.</span><span class="sxs-lookup"><span data-stu-id="b4086-114">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="b4086-115">Du kan forhåndsvise både de supplerte og de ikke-supplerte produktsidene for en kategori ved å velge kategorinavnet.</span><span class="sxs-lookup"><span data-stu-id="b4086-115">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="b4086-116">Gjør følgende for å gjøre en kategoriside rikere:</span><span class="sxs-lookup"><span data-stu-id="b4086-116">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="b4086-117">På **Produkter**-siden velger du navnet på kategorien som du vil supplere kategorisiden for.</span><span class="sxs-lookup"><span data-stu-id="b4086-117">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="b4086-118">Standard kategoriside for den valgte kategorien åpnes i redigeringsprogrammet for sider.</span><span class="sxs-lookup"><span data-stu-id="b4086-118">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="b4086-119">Velg **Suppler kategoriside**.</span><span class="sxs-lookup"><span data-stu-id="b4086-119">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="b4086-120">Velg en mal for den berikede kategorisiden.</span><span class="sxs-lookup"><span data-stu-id="b4086-120">Select a template for the enriched category page.</span></span> <span data-ttu-id="b4086-121">Hvis du bare gjør små endringer, kan du velge standard kategoriside.</span><span class="sxs-lookup"><span data-stu-id="b4086-121">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="b4086-122">Du kan også velge en bestemt kategorisidemal.</span><span class="sxs-lookup"><span data-stu-id="b4086-122">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="b4086-123">Når du velger en mal, åpnes redigeringsprogrammet for side, og den valgte malen brukes til å opprette en ny kategoriside for den valgte kategorien.</span><span class="sxs-lookup"><span data-stu-id="b4086-123">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="b4086-124">Siden sjekkes ut til deg, og du kan nå utføre endringene.</span><span class="sxs-lookup"><span data-stu-id="b4086-124">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="b4086-125">Moduler som bruker kategorispesifikasjonsdata, bruker dataene fra den valgte kategorien.</span><span class="sxs-lookup"><span data-stu-id="b4086-125">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="b4086-126">Innstillingene for malen du velger, avgjør hvilke endringer du kan utføre.</span><span class="sxs-lookup"><span data-stu-id="b4086-126">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4086-127">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b4086-127">Additional resources</span></span>

[<span data-ttu-id="b4086-128">Endre en eksisterende områdeside</span><span class="sxs-lookup"><span data-stu-id="b4086-128">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="b4086-129">Legg til en ny områdeside</span><span class="sxs-lookup"><span data-stu-id="b4086-129">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="b4086-130">Velge sideoppsett</span><span class="sxs-lookup"><span data-stu-id="b4086-130">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="b4086-131">Behandle metadata for søkemotor</span><span class="sxs-lookup"><span data-stu-id="b4086-131">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="b4086-132">Lagre, forhåndsvise og publisere en side</span><span class="sxs-lookup"><span data-stu-id="b4086-132">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="b4086-133">Supplere en produktside</span><span class="sxs-lookup"><span data-stu-id="b4086-133">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="b4086-134">Kontrollere tilgjengelighet for sideinnhold</span><span class="sxs-lookup"><span data-stu-id="b4086-134">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="b4086-135">Opprette dynamiske e-handelssider basert på URL-parametere</span><span class="sxs-lookup"><span data-stu-id="b4086-135">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
