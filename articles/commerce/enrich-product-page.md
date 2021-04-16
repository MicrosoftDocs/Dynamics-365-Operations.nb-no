---
title: Supplere en produktside
description: Dette emnet beskriver hvordan du supplerer en produktside i Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6c1a9474ed514426386b1d7b4a72b62129cdb8a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799056"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="7b93a-103">Supplere en produktside</span><span class="sxs-lookup"><span data-stu-id="7b93a-103">Enrich a product page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7b93a-104">Dette emnet beskriver hvordan du supplerer en produktside i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7b93a-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7b93a-105">Som standard bruker webområdet en generell side til å vise produktdata.</span><span class="sxs-lookup"><span data-stu-id="7b93a-105">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="7b93a-106">Denne siden inneholder grunnleggende informasjon om produktet og kontrollene som kreves for å selge den.</span><span class="sxs-lookup"><span data-stu-id="7b93a-106">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="7b93a-107">Du kan imidlertid supplere informasjonen som kommer fra Commerce Scale Unit, med tilleggsbilder eller -tekst for et bestemt produkt.</span><span class="sxs-lookup"><span data-stu-id="7b93a-107">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="7b93a-108">Denne prosessen kalles å supplere produktsiden.</span><span class="sxs-lookup"><span data-stu-id="7b93a-108">This process is known as enriching the product page.</span></span>

<span data-ttu-id="7b93a-109">I mange tilfeller vil du ha bruk for et bestemt tilleggsinnhold for produktene.</span><span class="sxs-lookup"><span data-stu-id="7b93a-109">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="7b93a-110">Når du går til **Detaljhandel og handel** i redigeringsverktøyet, vil du se en liste over produkter fra kanalen som er tilordnet området.</span><span class="sxs-lookup"><span data-stu-id="7b93a-110">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="7b93a-111">I denne listen viser kolonnen for **Supplert** om produktsiden for et produkt er supplert.</span><span class="sxs-lookup"><span data-stu-id="7b93a-111">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="7b93a-112">Hvis det vises et merke i kolonnen, finnes det en supplert produktside for produktet.</span><span class="sxs-lookup"><span data-stu-id="7b93a-112">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="7b93a-113">Hvis det ikke vises noen avmerking, brukes standard produktside og -innhold for produktet.</span><span class="sxs-lookup"><span data-stu-id="7b93a-113">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="7b93a-114">Du kan forhåndsvise både supplerte og ikke-supplerte produktsider ved å velge et produktnavn fra listen.</span><span class="sxs-lookup"><span data-stu-id="7b93a-114">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="7b93a-115">Supplere en produktside</span><span class="sxs-lookup"><span data-stu-id="7b93a-115">Enrich a product page</span></span>

<span data-ttu-id="7b93a-116">Følg denne fremgangsmåten for å supplere en produktside.</span><span class="sxs-lookup"><span data-stu-id="7b93a-116">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="7b93a-117">Under **Områder** velger du **Fabrikam** (eller navnet på området).</span><span class="sxs-lookup"><span data-stu-id="7b93a-117">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="7b93a-118">Velg **Produkter** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="7b93a-118">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="7b93a-119">Velg et hvilket som helst produkt som ikke har en supplert produktside.</span><span class="sxs-lookup"><span data-stu-id="7b93a-119">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="7b93a-120">Klikk på **Suppler produktside** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7b93a-120">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="7b93a-121">Velg **PDP-mal**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b93a-121">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="7b93a-122">Utvid **Hoved**-sporet i sidedisposisjonstreet til venstre.</span><span class="sxs-lookup"><span data-stu-id="7b93a-122">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="7b93a-123">Velg ellipseknappen (**...**) for **Hoved**-sporet, og velg deretter **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="7b93a-123">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="7b93a-124">Velg **Container 2**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b93a-124">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="7b93a-125">Velg ellipseknappen for **Container 2**, og velg deretter **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="7b93a-125">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="7b93a-126">Velg **Funksjon**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b93a-126">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="7b93a-127">I egenskapsruten til høyre, i feltet **Rik tekst**, angir du oppdatert beskrivelse for produktet.</span><span class="sxs-lookup"><span data-stu-id="7b93a-127">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="7b93a-128">I feltet **Overskrift** angir du overskriftstekst, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b93a-128">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="7b93a-129">Velg **Lagre**, og velg deretter **Fullfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="7b93a-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="7b93a-130">I feltet **Kommentarer** angir du **Supplerte et produkt**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b93a-130">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="7b93a-131">Velg **Forhåndsvisning** for å forhåndsvise den supplerte produktsiden.</span><span class="sxs-lookup"><span data-stu-id="7b93a-131">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="7b93a-132">Når du er ferdig, lukker du forhåndsvisningskategorien for å gå tilbake til redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="7b93a-132">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="7b93a-133">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="7b93a-133">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b93a-134">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="7b93a-134">Additional resources</span></span>

[<span data-ttu-id="7b93a-135">Endre en eksisterende områdeside</span><span class="sxs-lookup"><span data-stu-id="7b93a-135">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="7b93a-136">Legg til en ny områdeside</span><span class="sxs-lookup"><span data-stu-id="7b93a-136">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="7b93a-137">Velge sideoppsett</span><span class="sxs-lookup"><span data-stu-id="7b93a-137">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="7b93a-138">Behandle metadata for søkemotor</span><span class="sxs-lookup"><span data-stu-id="7b93a-138">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="7b93a-139">Lagre, forhåndsvise og publisere en side</span><span class="sxs-lookup"><span data-stu-id="7b93a-139">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="7b93a-140">Supplere en kategorimålside</span><span class="sxs-lookup"><span data-stu-id="7b93a-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="7b93a-141">Kontrollere tilgjengelighet for sideinnhold</span><span class="sxs-lookup"><span data-stu-id="7b93a-141">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="7b93a-142">Opprette dynamiske e-handelssider basert på URL-parametere</span><span class="sxs-lookup"><span data-stu-id="7b93a-142">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
