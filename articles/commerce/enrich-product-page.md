---
title: Supplere en produktside
description: Dette emnet beskriver hvordan du supplerer en produktside i Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9c0f329d21cdda5c36a39a8c602d5925b720f52
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945749"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="e635f-103">Supplere en produktside</span><span class="sxs-lookup"><span data-stu-id="e635f-103">Enrich a product page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e635f-104">Dette emnet beskriver hvordan du supplerer en produktside i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e635f-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e635f-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="e635f-105">Overview</span></span>

<span data-ttu-id="e635f-106">Som standard bruker webområdet en generell side til å vise produktdata.</span><span class="sxs-lookup"><span data-stu-id="e635f-106">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="e635f-107">Denne siden inneholder grunnleggende informasjon om produktet og kontrollene som kreves for å selge den.</span><span class="sxs-lookup"><span data-stu-id="e635f-107">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="e635f-108">Du kan imidlertid supplere informasjonen som kommer fra Retail Server, med tilleggsbilder eller -tekst for et bestemt produkt.</span><span class="sxs-lookup"><span data-stu-id="e635f-108">However, you can supplement the information that comes from the Retail Server with additional images or text for a specific product.</span></span> <span data-ttu-id="e635f-109">Denne prosessen kalles å supplere produktsiden.</span><span class="sxs-lookup"><span data-stu-id="e635f-109">This process is known as enriching the product page.</span></span>

<span data-ttu-id="e635f-110">I mange tilfeller vil du ha bruk for et bestemt tilleggsinnhold for produktene.</span><span class="sxs-lookup"><span data-stu-id="e635f-110">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="e635f-111">Når du går til **Retail** i redigeringsverktøyet, vil du se en liste over produkter fra kanalen som er tilordnet området.</span><span class="sxs-lookup"><span data-stu-id="e635f-111">When you go to **Retail** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="e635f-112">I denne listen viser kolonnen for **Supplert** om produktsiden for et produkt er supplert.</span><span class="sxs-lookup"><span data-stu-id="e635f-112">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="e635f-113">Hvis det vises et merke i kolonnen, finnes det en supplert produktside for produktet.</span><span class="sxs-lookup"><span data-stu-id="e635f-113">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="e635f-114">Hvis det ikke vises noen avmerking, brukes standard produktside og -innhold for produktet.</span><span class="sxs-lookup"><span data-stu-id="e635f-114">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="e635f-115">Du kan forhåndsvise både supplerte og ikke-supplerte produktsider ved å velge et produktnavn fra listen.</span><span class="sxs-lookup"><span data-stu-id="e635f-115">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="e635f-116">Supplere en produktside</span><span class="sxs-lookup"><span data-stu-id="e635f-116">Enrich a product page</span></span>

<span data-ttu-id="e635f-117">Følg denne fremgangsmåten for å supplere en produktside.</span><span class="sxs-lookup"><span data-stu-id="e635f-117">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="e635f-118">Under **Områder** velger du **Fabrikam** (eller navnet på området).</span><span class="sxs-lookup"><span data-stu-id="e635f-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="e635f-119">Velg **Produkter**i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="e635f-119">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="e635f-120">Velg et hvilket som helst produkt som ikke har en supplert produktside.</span><span class="sxs-lookup"><span data-stu-id="e635f-120">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="e635f-121">Klikk på **Suppler produktside** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e635f-121">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="e635f-122">Velg **PDP-mal**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e635f-122">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="e635f-123">Utvid **Hoved**-sporet i sidedisposisjonstreet til venstre.</span><span class="sxs-lookup"><span data-stu-id="e635f-123">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="e635f-124">Velg ellipseknappen (**...**) for **Hoved**-sporet, og velg deretter **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="e635f-124">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="e635f-125">Velg **Container 2**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e635f-125">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="e635f-126">Velg ellipseknappen for **Container 2**, og velg deretter **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="e635f-126">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="e635f-127">Velg **Funksjon**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e635f-127">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="e635f-128">I egenskapsruten til høyre, i feltet **Rik tekst**, angir du oppdatert beskrivelse for produktet.</span><span class="sxs-lookup"><span data-stu-id="e635f-128">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="e635f-129">I feltet **Overskrift** angir du overskriftstekst, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="e635f-129">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="e635f-130">Velg **Lagre**, og velg deretter **Sjekk inn**.</span><span class="sxs-lookup"><span data-stu-id="e635f-130">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="e635f-131">I feltet **Kommentarer** angir du **Supplerte et produkt**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="e635f-131">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="e635f-132">Velg **Forhåndsvisning** for å forhåndsvise den supplerte produktsiden.</span><span class="sxs-lookup"><span data-stu-id="e635f-132">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="e635f-133">Når du er ferdig, lukker du forhåndsvisningskategorien for å gå tilbake til redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="e635f-133">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="e635f-134">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="e635f-134">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e635f-135">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e635f-135">Additional resources</span></span>

[<span data-ttu-id="e635f-136">Endre en eksisterende områdeside</span><span class="sxs-lookup"><span data-stu-id="e635f-136">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="e635f-137">Legg til en ny områdeside</span><span class="sxs-lookup"><span data-stu-id="e635f-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="e635f-138">Velge sideoppsett</span><span class="sxs-lookup"><span data-stu-id="e635f-138">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="e635f-139">Behandle metadata for søkemotor</span><span class="sxs-lookup"><span data-stu-id="e635f-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="e635f-140">Lagre, forhåndsvise og publisere en side</span><span class="sxs-lookup"><span data-stu-id="e635f-140">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="e635f-141">Supplere en kategorimålside</span><span class="sxs-lookup"><span data-stu-id="e635f-141">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="e635f-142">Kontrollere tilgjengelighet for sideinnhold</span><span class="sxs-lookup"><span data-stu-id="e635f-142">Verify page content accessibility</span></span>](verify-accessibility.md)