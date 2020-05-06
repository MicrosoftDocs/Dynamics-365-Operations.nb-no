---
title: Supplere en kategorimålside
description: Dette emnet dekker supplering av kategorisider i Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
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
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ca31ec7d2eee7d2b0c863506338341a870ff07ee
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269849"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="a9573-103">Supplere en kategorimålside</span><span class="sxs-lookup"><span data-stu-id="a9573-103">Enrich a category landing page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a9573-104">Dette emnet dekker supplering av kategorisider i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a9573-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a9573-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="a9573-105">Overview</span></span>

<span data-ttu-id="a9573-106">Commerce leverer en standard kategorimålside som brukes når kategoridata vises.</span><span class="sxs-lookup"><span data-stu-id="a9573-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="a9573-107">En standard kategoriside inneholder nødvendige elementer, for eksempel presiseringer, kategoriserte produktplasseringer, sorteringsalternativer, et valgsammendrag og sidenummereringskontroller.</span><span class="sxs-lookup"><span data-stu-id="a9573-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="a9573-108">I stedet for å bruke standard kategoriside kan det imidlertid være lurt å bruke en "supplert" kategorimålside med mer innhold og mer spesifikke elementer.</span><span class="sxs-lookup"><span data-stu-id="a9573-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="a9573-109">Et typisk supplement kan involvere å legge til kategorispesifikt markedsføringsinnhold på kategorisiden.</span><span class="sxs-lookup"><span data-stu-id="a9573-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="a9573-110">Dette innholdet kan inkludere produktplassering på tvers av kategorier for kryssalgsformål, redigeringslister, bilder, videoer og annen tekst.</span><span class="sxs-lookup"><span data-stu-id="a9573-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="a9573-111">Du kan enten endre standard kategoriside eller definere en annen kategoriside for en bestemt kategori.</span><span class="sxs-lookup"><span data-stu-id="a9573-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Supplere kategorimålside](./media/CategoryLandingPages.png)

<span data-ttu-id="a9573-113">I Commerce-områdebyggeren inneholder siden **Produkter** en liste over kategorier fra kanalen som er tilordnet området.</span><span class="sxs-lookup"><span data-stu-id="a9573-113">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="a9573-114">Hvis statusen **Supplert** er valgt for en kategoriside, er denne kategorisiden supplert.</span><span class="sxs-lookup"><span data-stu-id="a9573-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="a9573-115">Hvis ikke brukes standard kategoriside og -innhold for kategorien.</span><span class="sxs-lookup"><span data-stu-id="a9573-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="a9573-116">Du kan forhåndsvise både de supplerte og de ikke-supplerte produktsidene for en kategori ved å velge kategorinavnet.</span><span class="sxs-lookup"><span data-stu-id="a9573-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="a9573-117">Gjør følgende for å gjøre en kategoriside rikere:</span><span class="sxs-lookup"><span data-stu-id="a9573-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="a9573-118">På **Produkter**-siden velger du navnet på kategorien som du vil supplere kategorisiden for.</span><span class="sxs-lookup"><span data-stu-id="a9573-118">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="a9573-119">Standard kategoriside for den valgte kategorien åpnes i redigeringsprogrammet for sider.</span><span class="sxs-lookup"><span data-stu-id="a9573-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="a9573-120">Velg **Suppler kategoriside**.</span><span class="sxs-lookup"><span data-stu-id="a9573-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="a9573-121">Velg en mal for den berikede kategorisiden.</span><span class="sxs-lookup"><span data-stu-id="a9573-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="a9573-122">Hvis du bare gjør små endringer, kan du velge standard kategoriside.</span><span class="sxs-lookup"><span data-stu-id="a9573-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="a9573-123">Du kan også velge en bestemt kategorisidemal.</span><span class="sxs-lookup"><span data-stu-id="a9573-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="a9573-124">Når du velger en mal, åpnes redigeringsprogrammet for side, og den valgte malen brukes til å opprette en ny kategoriside for den valgte kategorien.</span><span class="sxs-lookup"><span data-stu-id="a9573-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="a9573-125">Siden sjekkes ut til deg, og du kan nå utføre endringene.</span><span class="sxs-lookup"><span data-stu-id="a9573-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="a9573-126">Moduler som bruker kategorispesifikasjonsdata, bruker dataene fra den valgte kategorien.</span><span class="sxs-lookup"><span data-stu-id="a9573-126">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="a9573-127">Innstillingene for malen du velger, avgjør hvilke endringer du kan utføre.</span><span class="sxs-lookup"><span data-stu-id="a9573-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a9573-128">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a9573-128">Additional resources</span></span>

[<span data-ttu-id="a9573-129">Endre en eksisterende områdeside</span><span class="sxs-lookup"><span data-stu-id="a9573-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="a9573-130">Legg til en ny områdeside</span><span class="sxs-lookup"><span data-stu-id="a9573-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="a9573-131">Velge sideoppsett</span><span class="sxs-lookup"><span data-stu-id="a9573-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="a9573-132">Behandle metadata for søkemotor</span><span class="sxs-lookup"><span data-stu-id="a9573-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="a9573-133">Lagre, forhåndsvise og publisere en side</span><span class="sxs-lookup"><span data-stu-id="a9573-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="a9573-134">Supplere en produktside</span><span class="sxs-lookup"><span data-stu-id="a9573-134">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="a9573-135">Kontrollere tilgjengelighet for sideinnhold</span><span class="sxs-lookup"><span data-stu-id="a9573-135">Verify page content accessibility</span></span>](verify-accessibility.md)
