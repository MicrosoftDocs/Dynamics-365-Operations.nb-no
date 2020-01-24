---
title: Oversikt over Commerce-forhåndsvisningsmiljø
description: Dette emnet gir en oversikt over Microsoft Dynamics 365 Commerce-forhåndsvisningsmiljøet.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
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
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 901583afde4739be5313fa129ff0e52f11326881
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906076"
---
# <a name="commerce-preview-environment-overview"></a><span data-ttu-id="f0a86-103">Oversikt over Commerce-forhåndsvisningsmiljø</span><span class="sxs-lookup"><span data-stu-id="f0a86-103">Commerce preview environment overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f0a86-104">Dette emnet gir en oversikt over Microsoft Dynamics 365 Commerce-forhåndsvisningsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="f0a86-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="overview"></a><span data-ttu-id="f0a86-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="f0a86-105">Overview</span></span>

<span data-ttu-id="f0a86-106">Commerce-forhåndsvisningsmiljøet er et valgfritt ende-til-ende forhåndsvisningsmiljø for Dynamics 365 Commerce som gjør det mulig for potensielle kunder prøve ut Commerce-produktet før den generelle utgivelsen til offentligheten.</span><span class="sxs-lookup"><span data-stu-id="f0a86-106">The Commerce preview environment is an optional end-to-end preview environment of Dynamics 365 Commerce that lets potential customers try out the Commerce product before its general release to the public.</span></span>

<span data-ttu-id="f0a86-107">I tillegg til noen mindre begrensninger som ikke påvirker funksjonalitet, gir forhåndsvisningsmiljøet i Commerce den komplette Commerce-opplevelsen, og kan brukes av kunder og implementeringspartnere til å evaluere produktet, gi tilbakemelding og utføre tilpassings-/gapanalyse.</span><span class="sxs-lookup"><span data-stu-id="f0a86-107">Aside from some minor limitations that don't affect features or functionality, the Commerce preview environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-preview-environment"></a><span data-ttu-id="f0a86-108">Begrensninger i forhåndsvisningsmiljøet for Commerce</span><span class="sxs-lookup"><span data-stu-id="f0a86-108">Limitations of the Commerce preview environment</span></span>

<span data-ttu-id="f0a86-109">Selv om forhåndsvisningsmiljøet i Commerce inneholder det fullstendige settet med Commerce-funksjoner, er det noen mindre begrensninger:</span><span class="sxs-lookup"><span data-stu-id="f0a86-109">Although the Commerce preview environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="f0a86-110">Selv om selve Commerce-forhåndsvisningsmiljøet ikke har noen geografiske begrensninger, kan komponenter i miljøet, for eksempel Retail Cloud Scale Unit (RCSU) og e-handelsprogrammer, bare klargjøres i USA.</span><span class="sxs-lookup"><span data-stu-id="f0a86-110">Although the Commerce preview environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, can be provisioned only in the United States.</span></span>
- <span data-ttu-id="f0a86-111">Bruk av forhåndsvisningsmiljøet for Commerce har en 30-dagers tidsbegrensning fra datoen for klargjøring av e-handel.</span><span class="sxs-lookup"><span data-stu-id="f0a86-111">Use of the Commerce preview environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="f0a86-112">Forhåndsvisningsmiljøet for Commerce kan med hell distribueres og initialiseres bare i et miljø som bruker demonstrasjonstopologien, der alle komponentene i et miljø distribueres i én enkelt virtuell maskin (VM).</span><span class="sxs-lookup"><span data-stu-id="f0a86-112">The Commerce preview environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed in a single virtual machine (VM).</span></span> <span data-ttu-id="f0a86-113">Den største begrensningen for denne OneBox VM-topologien er antall samtidige brukere som gorhåndsvisningsmiljøet kan støtte.</span><span class="sxs-lookup"><span data-stu-id="f0a86-113">The main limitation of this OneBox VM topology is the number of concurrent users that the preview environment can support.</span></span>
- <span data-ttu-id="f0a86-114">Forhåndsvisningsmiljøet for Commerce kan bare evalueres til det generelle tilgjengeligheten (GA) for Commerce-produktet.</span><span class="sxs-lookup"><span data-stu-id="f0a86-114">The Commerce preview environment can be evaluated only until the general availability (GA) of the Commerce product.</span></span> <span data-ttu-id="f0a86-115">Nye demomiljøer vil være tilgjengelig etter GA.</span><span class="sxs-lookup"><span data-stu-id="f0a86-115">New demo environments will be available after GA.</span></span>

## <a name="get-started"></a><span data-ttu-id="f0a86-116">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="f0a86-116">Get started</span></span>

<span data-ttu-id="f0a86-117">Hvis du vil klargjøre forhåndsvisningsmiljøet for Commerce, kan du se [Klargjøre et Commerce-forhåndsvisningsmiljø](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="f0a86-117">To provision the Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0a86-118">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f0a86-118">Additional resources</span></span>

[<span data-ttu-id="f0a86-119">Klargjøre et Commerce-forhåndsvisningsmiljø</span><span class="sxs-lookup"><span data-stu-id="f0a86-119">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="f0a86-120">Konfigurere et Commerce-forhåndsvisningsmiljø</span><span class="sxs-lookup"><span data-stu-id="f0a86-120">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="f0a86-121">Konfigurere valgfrie funksjoner for et Commerce-forhåndsvisningsmiljø</span><span class="sxs-lookup"><span data-stu-id="f0a86-121">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="f0a86-122">Vanlige spørsmål for Commerce-forhåndsvisningsmiljø</span><span class="sxs-lookup"><span data-stu-id="f0a86-122">Commerce preview environment FAQ</span></span>](cpe-faq.md)
