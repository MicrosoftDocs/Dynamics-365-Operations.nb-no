---
title: Områdevelgermodul
description: Dette emnet dekker områdevelgermodulen og beskriver hvordan du legger den til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.openlocfilehash: b4e5f715efcac7f883df99508d282db904be0d80
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665229"
---
# <a name="site-selector-module"></a><span data-ttu-id="f2e07-103">Områdevelgermodul</span><span class="sxs-lookup"><span data-stu-id="f2e07-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f2e07-104">Dette emnet dekker områdevelgermodulen og beskriver hvordan du legger den til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f2e07-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f2e07-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="f2e07-105">Overview</span></span>

<span data-ttu-id="f2e07-106">Når en bedrift har forskjellige områder på tvers av markeder, områder og nasjonale innstillinger, trenger områdebrukere en enkel måte å veksle mellom områder og velge foretrukket område for shopping.</span><span class="sxs-lookup"><span data-stu-id="f2e07-106">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="f2e07-107">For å få plass til dette scenarioet lar områdevelgermodulen brukere bla gjennom flere områder.</span><span class="sxs-lookup"><span data-stu-id="f2e07-107">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="f2e07-108">Områdevelgermodulen må være konfigurert med listen over områder (markeder, regioner eller nasjonale innstillinger) som områdebrukere kan bla gjennom.</span><span class="sxs-lookup"><span data-stu-id="f2e07-108">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="f2e07-109">Områdevelgermodulen er tilgjengelig i Dynamics 365 Commerce 10.0.14-versjonen.</span><span class="sxs-lookup"><span data-stu-id="f2e07-109">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="f2e07-110">Illustrasjonen nedenfor viser et eksempel på en områdevelgermodul som vises i hodet på en områdeside.</span><span class="sxs-lookup"><span data-stu-id="f2e07-110">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![Eksempel på en områdevelgermodul i toppteksten på en områdeside](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="f2e07-112">Egenskaper for områdevelgermodul</span><span class="sxs-lookup"><span data-stu-id="f2e07-112">Site selector module properties</span></span>

| <span data-ttu-id="f2e07-113">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="f2e07-113">Property name</span></span> | <span data-ttu-id="f2e07-114">Verdi</span><span class="sxs-lookup"><span data-stu-id="f2e07-114">Value</span></span>                 | <span data-ttu-id="f2e07-115">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f2e07-115">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="f2e07-116">Overskrift</span><span class="sxs-lookup"><span data-stu-id="f2e07-116">Heading</span></span>       | <span data-ttu-id="f2e07-117">Tekst</span><span class="sxs-lookup"><span data-stu-id="f2e07-117">Text</span></span>                  | <span data-ttu-id="f2e07-118">Overskriften for modulen.</span><span class="sxs-lookup"><span data-stu-id="f2e07-118">The heading for the module.</span></span> |
| <span data-ttu-id="f2e07-119">Områdealternativer</span><span class="sxs-lookup"><span data-stu-id="f2e07-119">Site options</span></span>  | <span data-ttu-id="f2e07-120">Navn, bilde, URL-adresse</span><span class="sxs-lookup"><span data-stu-id="f2e07-120">Name, Image, URL</span></span>      | <span data-ttu-id="f2e07-121">Denne egenskapen angir et navn, en kobling til startsiden for området, og et valgfritt bilde som skal vises for hvert område som er inkludert i modulen.</span><span class="sxs-lookup"><span data-stu-id="f2e07-121">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="f2e07-122">Bildet kan være et flagg, eller en presentasjon av et marked, en region eller et land.</span><span class="sxs-lookup"><span data-stu-id="f2e07-122">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="f2e07-123">Legge til en områdevelgermodul på en side</span><span class="sxs-lookup"><span data-stu-id="f2e07-123">Add a site selector module to a page</span></span>

<span data-ttu-id="f2e07-124">Områdevelgermodulen kan legges til i [topptekstmodulen](author-header-module.md) under områdevelgersporet.</span><span class="sxs-lookup"><span data-stu-id="f2e07-124">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="f2e07-125">Når den er lagt til, kan du definere moduloverskriften og områdealternativene.</span><span class="sxs-lookup"><span data-stu-id="f2e07-125">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2e07-126">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f2e07-126">Additional resources</span></span>

[<span data-ttu-id="f2e07-127">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="f2e07-127">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f2e07-128">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="f2e07-128">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f2e07-129">Søkebanemodul</span><span class="sxs-lookup"><span data-stu-id="f2e07-129">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="f2e07-130">Navigasjonsmenymodul</span><span class="sxs-lookup"><span data-stu-id="f2e07-130">Navigation menu module</span></span>](nav-menu-module.md)
