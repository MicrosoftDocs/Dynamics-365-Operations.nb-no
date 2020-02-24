---
title: Vurderinger for søkemotoroptimalisering (SEO) for området
description: Dette emnet dekker søkemotoroptimaliseringshensyn (SEO) for området fra utvikling til produksjon.
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
ms.openlocfilehash: 7c7afed8e4620d5fe49ead47eb6c17d97d7492ad
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002814"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a><span data-ttu-id="6ad61-103">Vurderinger for søkemotoroptimalisering (SEO) for området</span><span class="sxs-lookup"><span data-stu-id="6ad61-103">Search engine optimization (SEO) considerations for your site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6ad61-104">Dette emnet dekker søkemotoroptimaliseringshensyn (SEO) for området fra utvikling til produksjon.</span><span class="sxs-lookup"><span data-stu-id="6ad61-104">This topic covers earch engine optimization (SEO) considerations for your site from development to production.</span></span>

## <a name="a-site-that-is-under-development"></a><span data-ttu-id="6ad61-105">Et område som er under utvikling</span><span class="sxs-lookup"><span data-stu-id="6ad61-105">A site that is under development</span></span>

<span data-ttu-id="6ad61-106">Mens et område er under utvikling, skal alle områdesidene ha metakodene **NOINDEX** og **NOFOLLOW**, slik at søkemotorene ikke indekserer sidene og lagrer utviklingsversjoner av området i hurtigbufferen.</span><span class="sxs-lookup"><span data-stu-id="6ad61-106">While a site is under development, all site pages should have the **NOINDEX** and **NOFOLLOW** meta tags, so that search engines don't index the pages and store development versions of your site in their cache.</span></span> <span data-ttu-id="6ad61-107">Hvis du vil gjøre denne konfigurasjonen, må du legge til standard metakodemoduler i områdesidemalen.</span><span class="sxs-lookup"><span data-stu-id="6ad61-107">To do this configuration, you must add the default meta tags module to the site page template.</span></span> <span data-ttu-id="6ad61-108">Standardegenskapene for metakoder vil da være tilgjengelige i delen om søkemotoregenskaper i sideredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="6ad61-108">The default meta tags properties will then be available in the SEO properties section in the page editor.</span></span> <span data-ttu-id="6ad61-109">Du kan bruke disse egenskapene til å administrere metakodene.</span><span class="sxs-lookup"><span data-stu-id="6ad61-109">You can use these properties to manage the meta tags.</span></span>

## <a name="soft-launch-of-a-site"></a><span data-ttu-id="6ad61-110">Myk lansering av et område</span><span class="sxs-lookup"><span data-stu-id="6ad61-110">Soft launch of a site</span></span>

<span data-ttu-id="6ad61-111">Under en "myk lansering" er et webområde gjort tilgjengelig for en begrenset målgruppe eller et begrenset marked før den fullstendige oppstarten skjer.</span><span class="sxs-lookup"><span data-stu-id="6ad61-111">During a "soft launch," a website is made available to a limited audience or market before the full launch occurs.</span></span> <span data-ttu-id="6ad61-112">Hvis du gjør en myk lansering av webområdet, bør du vurdere å la metakodene **NOINDEX** bli værende.</span><span class="sxs-lookup"><span data-stu-id="6ad61-112">If you do a soft launch of your website, you should consider leaving the **NOINDEX** meta tags in place.</span></span> <span data-ttu-id="6ad61-113">På denne måten bidrar du til å sikre at den myke oppstarten forblir begrenset til den begrensede målgruppen du vil nå.</span><span class="sxs-lookup"><span data-stu-id="6ad61-113">In this way, you help guarantee that the soft launch remains restricted to the limited audience that you want to reach.</span></span>

## <a name="a-site-that-is-in-production"></a><span data-ttu-id="6ad61-114">Et område som er i produksjon</span><span class="sxs-lookup"><span data-stu-id="6ad61-114">A site that is in production</span></span>

<span data-ttu-id="6ad61-115">Når et område er i produksjon, bør du kontrollere at alle områdesidene er riktig kodet.</span><span class="sxs-lookup"><span data-stu-id="6ad61-115">When a site is in production, you should make sure that all site pages are correctly tagged.</span></span> <span data-ttu-id="6ad61-116">Microsoft Dynamics 365 Commerce bruker informasjonen som er angitt for en side, til å gjengi all søkemotorinformasjon på den aktuelle siden.</span><span class="sxs-lookup"><span data-stu-id="6ad61-116">Microsoft Dynamics 365 Commerce uses the information that is entered for a page to render all the SEO information on that page.</span></span> <span data-ttu-id="6ad61-117">Følgende moduler inneholder denne funksjonaliteten: kategorisidesammendrag, listesidesammendrag og produktsidesammendrag.</span><span class="sxs-lookup"><span data-stu-id="6ad61-117">The following modules provide this functionality: category page summary, list page summary, and product page summary.</span></span>

<span data-ttu-id="6ad61-118">For å optimalisere søkemotorindeksering bruker gjengivelsesrammeverket både opplysningene fra søkemotoregenskapene som er konfigurert i Dynamics 365 Commerce, og modulspesifikk informasjon.</span><span class="sxs-lookup"><span data-stu-id="6ad61-118">To optimize search engine indexing, the rendering framework uses both information from the SEO properties that are configured in Dynamics 365 Commerce and module-specific information.</span></span> <span data-ttu-id="6ad61-119">For et område som er i produksjon, bør du kontrollere at robots.txt-filen tillater indeksering av hele området, og at det inneholder koblinger til det publiserte områdekartdokumentet.</span><span class="sxs-lookup"><span data-stu-id="6ad61-119">For a site that is in production, you should make sure that the robots.txt file allows for indexing of your whole site, and that it contains links to your published site map document.</span></span> <span data-ttu-id="6ad61-120">Du bør slå på funksjonen for generering av områdekart på **Områdeinnstillinger \> Områdekart aktivert**.</span><span class="sxs-lookup"><span data-stu-id="6ad61-120">You should turn on the site map generation functionality at **Site Settings \> Site maps enabled**.</span></span>

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a><span data-ttu-id="6ad61-121">Innstillinger for sidesøkemotor for intern forhåndsvisning, begrenset målgruppe og alle målgrupper</span><span class="sxs-lookup"><span data-stu-id="6ad61-121">Page SEO settings for internal preview, limited audiences, and all audiences</span></span>

<span data-ttu-id="6ad61-122">Fordi Dynamics 365 Commerce støtter WYSIWYG-forhåndsvisning (det du ser, er det du får), kan forfattere klargjøre sideinnholdet uten å bekymre seg om at informasjonen blir synlig for besøkende på webområdet.</span><span class="sxs-lookup"><span data-stu-id="6ad61-122">Because Dynamics 365 Commerce supports "what you see is what you get" (WYSIWYG) authenticated previews, authors can prepare their page content without having to worry that the information will become visible to site visitors.</span></span> <span data-ttu-id="6ad61-123">Hvis en side må publiseres, men eksponeringen må begrenses, skal den ha metakoden **NOINDEX**, slik at den ikke vil bli indeksert av søkemotorer.</span><span class="sxs-lookup"><span data-stu-id="6ad61-123">If a page must be published, but its exposure must be limited, it should have the **NOINDEX** meta tag, so that it won't be indexed by search engines.</span></span> <span data-ttu-id="6ad61-124">Når siden er klar for alle målgrupper, bør alle de grunnleggende søkemotormetadataene være til stede for å maksimere effektiviteten av søkmotorindeksering.</span><span class="sxs-lookup"><span data-stu-id="6ad61-124">Then, when the page is ready for all audiences, all the basic SEO metadata should be present, to maximize the efficiency of search engine indexing.</span></span> <span data-ttu-id="6ad61-125">I tillegg bør metakoden **NOLIMIT** fjernes.</span><span class="sxs-lookup"><span data-stu-id="6ad61-125">Additionally, the **NOLIMIT** meta tag should be removed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ad61-126">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6ad61-126">Additional resources</span></span>

[<span data-ttu-id="6ad61-127">Behandle brukere og roller for e-handel</span><span class="sxs-lookup"><span data-stu-id="6ad61-127">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="6ad61-128">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="6ad61-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="6ad61-129">Behandle policy for innholdssikkerhet (CSP)</span><span class="sxs-lookup"><span data-stu-id="6ad61-129">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
