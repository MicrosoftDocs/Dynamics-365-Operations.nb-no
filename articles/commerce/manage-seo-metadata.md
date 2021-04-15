---
title: Behandle metadata for søkemotor
description: Dette emnet beskriver hvordan du behandler metadata for søkemotoroptimalisering i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 1e03ef346df92a94b0a403f241d0f7d1f64fd210
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794217"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="aa551-103">Behandle metadata for søkemotor</span><span class="sxs-lookup"><span data-stu-id="aa551-103">Manage SEO metadata</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aa551-104">Dette emnet beskriver hvordan du behandler metadata for søkemotoroptimalisering i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="aa551-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="aa551-105">Søkemotormetadata for et område kan administreres ved hjelp av områdekart og sidemetadata.</span><span class="sxs-lookup"><span data-stu-id="aa551-105">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="aa551-106">Områdekart</span><span class="sxs-lookup"><span data-stu-id="aa551-106">Site maps</span></span>

<span data-ttu-id="aa551-107">Et områdekart er en maskinlesbar liste, i XML-format, på sidene på webområdet.</span><span class="sxs-lookup"><span data-stu-id="aa551-107">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="aa551-108">Den er ment å brukes av søkemotorer, slik at de kan gi bedre søkeresultater fra området ditt.</span><span class="sxs-lookup"><span data-stu-id="aa551-108">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="aa551-109">Områdekart kan tas inn manuelt ved hjelp av søkemotorer eller publiseres i en robots.txt-fil.</span><span class="sxs-lookup"><span data-stu-id="aa551-109">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="aa551-110">Dynamics 365 Commerce støtter automatisk generering av områdekart.</span><span class="sxs-lookup"><span data-stu-id="aa551-110">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="aa551-111">Områdekart oppdateres automatisk når sider publiseres og publisering fjernes.</span><span class="sxs-lookup"><span data-stu-id="aa551-111">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="aa551-112">Aktivere generering av områdekart</span><span class="sxs-lookup"><span data-stu-id="aa551-112">Turn on site map generation</span></span>

1. <span data-ttu-id="aa551-113">Logge på redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="aa551-113">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="aa551-114">Under **Områder** velger du **Fabrikam** (eller navnet på området).</span><span class="sxs-lookup"><span data-stu-id="aa551-114">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="aa551-115">Velg **Områdebehandling** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="aa551-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="aa551-116">Kontroller at **Områdekart aktivert** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="aa551-116">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="aa551-117">Sidemetadata</span><span class="sxs-lookup"><span data-stu-id="aa551-117">Page metadata</span></span>

<span data-ttu-id="aa551-118">Dynamics 365 Commerce lar deg administrere søkemotormetadata for enkeltsider.</span><span class="sxs-lookup"><span data-stu-id="aa551-118">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="aa551-119">Du kan vise og endre denne informasjonen i delen **Søkemotoregenskaper** i en sidecontainer.</span><span class="sxs-lookup"><span data-stu-id="aa551-119">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="aa551-120">Følgende søkemotormetadataegenskaper støttes:</span><span class="sxs-lookup"><span data-stu-id="aa551-120">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="aa551-121">Stillingstittel</span><span class="sxs-lookup"><span data-stu-id="aa551-121">Title</span></span>
- <span data-ttu-id="aa551-122">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="aa551-122">Description</span></span>
- <span data-ttu-id="aa551-123">Søkemotornøkkelord</span><span class="sxs-lookup"><span data-stu-id="aa551-123">SEO keywords</span></span>
- <span data-ttu-id="aa551-124">ARIA-etiketter</span><span class="sxs-lookup"><span data-stu-id="aa551-124">Aria labels</span></span>
- <span data-ttu-id="aa551-125">noindex</span><span class="sxs-lookup"><span data-stu-id="aa551-125">noindex</span></span>
- <span data-ttu-id="aa551-126">nofollow</span><span class="sxs-lookup"><span data-stu-id="aa551-126">nofollow</span></span>
- <span data-ttu-id="aa551-127">noarchive</span><span class="sxs-lookup"><span data-stu-id="aa551-127">noarchive</span></span>
- <span data-ttu-id="aa551-128">nocache</span><span class="sxs-lookup"><span data-stu-id="aa551-128">nocache</span></span>
- <span data-ttu-id="aa551-129">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="aa551-129">noOpenDirectoryProject</span></span>
- <span data-ttu-id="aa551-130">nosnippet</span><span class="sxs-lookup"><span data-stu-id="aa551-130">nosnippet</span></span>
- <span data-ttu-id="aa551-131">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="aa551-131">noImageIndex</span></span>
- <span data-ttu-id="aa551-132">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="aa551-132">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="aa551-133">Endre sidemetadata</span><span class="sxs-lookup"><span data-stu-id="aa551-133">Modify page metadata</span></span>

<span data-ttu-id="aa551-134">Hvis du vil endre sidemetadata, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="aa551-134">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="aa551-135">Under **Områder** velger du **Fabrikam** (eller navnet på området).</span><span class="sxs-lookup"><span data-stu-id="aa551-135">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="aa551-136">Velg **Sider** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="aa551-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="aa551-137">Velg startsiden for å åpne den i sideredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="aa551-137">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="aa551-138">På kommandolinjen velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="aa551-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="aa551-139">Velg **Standard metakoder** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="aa551-139">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="aa551-140">Hvis du vil legge til en ny metakode, velger du **Legg til**, og deretter angir du koden i feltet.</span><span class="sxs-lookup"><span data-stu-id="aa551-140">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="aa551-141">Hvis du vil fjerne en eksisterende metakode, velger du papirkurvsymbolet til høyre for den.</span><span class="sxs-lookup"><span data-stu-id="aa551-141">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="aa551-142">Velg **Lagre**, og velg deretter **Fullfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="aa551-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="aa551-143">I feltet **Kommentarer** angr du **Oppdaterte metakoder**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa551-143">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="aa551-144">Velg **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="aa551-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="aa551-145">Når du er ferdig, lukker du forhåndsvisningskategorien for å gå tilbake til redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="aa551-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="aa551-146">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="aa551-146">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aa551-147">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="aa551-147">Additional resources</span></span>

[<span data-ttu-id="aa551-148">Endre en eksisterende områdeside</span><span class="sxs-lookup"><span data-stu-id="aa551-148">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="aa551-149">Legg til en ny områdeside</span><span class="sxs-lookup"><span data-stu-id="aa551-149">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="aa551-150">Velge sideoppsett</span><span class="sxs-lookup"><span data-stu-id="aa551-150">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="aa551-151">Lagre, forhåndsvise og publisere en side</span><span class="sxs-lookup"><span data-stu-id="aa551-151">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="aa551-152">Supplere en produktside</span><span class="sxs-lookup"><span data-stu-id="aa551-152">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="aa551-153">Supplere en kategorimålside</span><span class="sxs-lookup"><span data-stu-id="aa551-153">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="aa551-154">Kontrollere tilgjengelighet for sideinnhold</span><span class="sxs-lookup"><span data-stu-id="aa551-154">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="aa551-155">Opprette dynamiske e-handelssider basert på URL-parametere</span><span class="sxs-lookup"><span data-stu-id="aa551-155">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
