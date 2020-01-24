---
title: Behandle metadata for søkemotor
description: Dette emnet beskriver hvordan du behandler metadata for søkemotoroptimalisering i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 3ea06713af69659c205686a971393892fa584072
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945726"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="d8172-103">Behandle metadata for søkemotor</span><span class="sxs-lookup"><span data-stu-id="d8172-103">Manage SEO metadata</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="d8172-104">Dette emnet beskriver hvordan du behandler metadata for søkemotoroptimalisering i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d8172-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d8172-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="d8172-105">Overview</span></span>

<span data-ttu-id="d8172-106">Søkemotormetadata for et område kan administreres ved hjelp av områdekart og sidemetadata.</span><span class="sxs-lookup"><span data-stu-id="d8172-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="d8172-107">Områdekart</span><span class="sxs-lookup"><span data-stu-id="d8172-107">Site maps</span></span>

<span data-ttu-id="d8172-108">Et områdekart er en maskinlesbar liste, i XML-format, på sidene på webområdet.</span><span class="sxs-lookup"><span data-stu-id="d8172-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="d8172-109">Den er ment å brukes av søkemotorer, slik at de kan gi bedre søkeresultater fra området ditt.</span><span class="sxs-lookup"><span data-stu-id="d8172-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="d8172-110">Områdekart kan tas inn manuelt ved hjelp av søkemotorer eller publiseres i en robots.txt-fil.</span><span class="sxs-lookup"><span data-stu-id="d8172-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="d8172-111">Dynamics 365 Commerce støtter automatisk generering av områdekart.</span><span class="sxs-lookup"><span data-stu-id="d8172-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="d8172-112">Områdekart oppdateres automatisk når sider publiseres og publisering fjernes.</span><span class="sxs-lookup"><span data-stu-id="d8172-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="d8172-113">Aktivere generering av områdekart</span><span class="sxs-lookup"><span data-stu-id="d8172-113">Turn on site map generation</span></span>

1. <span data-ttu-id="d8172-114">Logge på redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="d8172-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="d8172-115">Under **Områder** velger du **Fabrikam** (eller navnet på området).</span><span class="sxs-lookup"><span data-stu-id="d8172-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="d8172-116">Velg **Områdebehandling** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="d8172-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="d8172-117">Kontroller at **Områdekart aktivert** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="d8172-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="d8172-118">Sidemetadata</span><span class="sxs-lookup"><span data-stu-id="d8172-118">Page metadata</span></span>

<span data-ttu-id="d8172-119">Dynamics 365 Commerce lar deg administrere søkemotormetadata for enkeltsider.</span><span class="sxs-lookup"><span data-stu-id="d8172-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="d8172-120">Du kan vise og endre denne informasjonen i delen **Søkemotoregenskaper** i en sidecontainer.</span><span class="sxs-lookup"><span data-stu-id="d8172-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="d8172-121">Følgende søkemotormetadataegenskaper støttes:</span><span class="sxs-lookup"><span data-stu-id="d8172-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="d8172-122">Stillingstittel</span><span class="sxs-lookup"><span data-stu-id="d8172-122">Title</span></span>
- <span data-ttu-id="d8172-123">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d8172-123">Description</span></span>
- <span data-ttu-id="d8172-124">Søkemotornøkkelord</span><span class="sxs-lookup"><span data-stu-id="d8172-124">SEO keywords</span></span>
- <span data-ttu-id="d8172-125">ARIA-etiketter</span><span class="sxs-lookup"><span data-stu-id="d8172-125">Aria labels</span></span>
- <span data-ttu-id="d8172-126">noindex</span><span class="sxs-lookup"><span data-stu-id="d8172-126">noindex</span></span>
- <span data-ttu-id="d8172-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="d8172-127">nofollow</span></span>
- <span data-ttu-id="d8172-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="d8172-128">noarchive</span></span>
- <span data-ttu-id="d8172-129">nocache</span><span class="sxs-lookup"><span data-stu-id="d8172-129">nocache</span></span>
- <span data-ttu-id="d8172-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="d8172-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="d8172-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="d8172-131">nosnippet</span></span>
- <span data-ttu-id="d8172-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="d8172-132">noImageIndex</span></span>
- <span data-ttu-id="d8172-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="d8172-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="d8172-134">Endre sidemetadata</span><span class="sxs-lookup"><span data-stu-id="d8172-134">Modify page metadata</span></span>

<span data-ttu-id="d8172-135">Hvis du vil endre sidemetadata, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="d8172-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="d8172-136">Under **Områder** velger du **Fabrikam** (eller navnet på området).</span><span class="sxs-lookup"><span data-stu-id="d8172-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="d8172-137">Velg **Sider**i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="d8172-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="d8172-138">Velg startsiden for å åpne den i sideredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="d8172-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="d8172-139">Velg **Sjekk ut** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d8172-139">On the Action Pane, select **Check Out**.</span></span>
1. <span data-ttu-id="d8172-140">Velg **Standard metakoder** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="d8172-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="d8172-141">Hvis du vil legge til en ny metakode, velger du **Legg til**, og deretter angir du koden i feltet.</span><span class="sxs-lookup"><span data-stu-id="d8172-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span>

    <span data-ttu-id="d8172-142">Hvis du vil fjerne en eksisterende metakode, velger du papirkurvsymbolet til høyre for den.</span><span class="sxs-lookup"><span data-stu-id="d8172-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>

1. <span data-ttu-id="d8172-143">Velg **Lagre**, og velg deretter **Sjekk inn**.</span><span class="sxs-lookup"><span data-stu-id="d8172-143">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="d8172-144">I feltet **Kommentarer** angr du **Oppdaterte metakoder**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="d8172-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="d8172-145">Velg **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="d8172-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="d8172-146">Når du er ferdig, lukker du forhåndsvisningskategorien for å gå tilbake til redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="d8172-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="d8172-147">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="d8172-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d8172-148">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d8172-148">Additional resources</span></span>

[<span data-ttu-id="d8172-149">Endre en eksisterende områdeside</span><span class="sxs-lookup"><span data-stu-id="d8172-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="d8172-150">Legg til en ny områdeside</span><span class="sxs-lookup"><span data-stu-id="d8172-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="d8172-151">Velge sideoppsett</span><span class="sxs-lookup"><span data-stu-id="d8172-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="d8172-152">Lagre, forhåndsvise og publisere en side</span><span class="sxs-lookup"><span data-stu-id="d8172-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="d8172-153">Supplere en produktside</span><span class="sxs-lookup"><span data-stu-id="d8172-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="d8172-154">Supplere en kategorimålside</span><span class="sxs-lookup"><span data-stu-id="d8172-154">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="d8172-155">Kontrollere tilgjengelighet for sideinnhold</span><span class="sxs-lookup"><span data-stu-id="d8172-155">Verify page content accessibility</span></span>](verify-accessibility.md)
