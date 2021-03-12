---
title: Oversikt over evalueringsmiljø for Dynamics 365 Commerce
description: Dette emnet gir en oversikt over Microsoft Dynamics 365 Commerce-evalueringsmiljøet.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8e08c2f327771d7731b836840006d63b6ecb7dfc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000956"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="cf1f5-103">Oversikt over evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cf1f5-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cf1f5-104">Dette emnet gir en oversikt over Microsoft Dynamics 365 Commerce-evalueringsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="cf1f5-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="cf1f5-105">Commerce-evalueringsmiljøer er ikke generelt tilgjengelige, og gis til partnere og kunder på et per forespørsel-grunnlag.</span><span class="sxs-lookup"><span data-stu-id="cf1f5-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="cf1f5-106">Hvis du vil ha mer informasjon, ta kontakt med din Microsoft-partnerkontakten din.</span><span class="sxs-lookup"><span data-stu-id="cf1f5-106">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="cf1f5-107">Oversikt</span><span class="sxs-lookup"><span data-stu-id="cf1f5-107">Overview</span></span>

<span data-ttu-id="cf1f5-108">Commerce-evalueringssmiljøet er et valgfritt ende-til-ende-miljø for Dynamics 365 Commerce som gjør det mulig for partnere og potensielle kunder å prøve ut Commerce-produktet.</span><span class="sxs-lookup"><span data-stu-id="cf1f5-108">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="cf1f5-109">Evalueringsmiljøer er delvis forhåndskonfigurert til å redusere de nødvendige trinnene etter klargjøring.</span><span class="sxs-lookup"><span data-stu-id="cf1f5-109">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="cf1f5-110">I tillegg til noen mindre begrensninger som ikke påvirker funksjonalitet, gir Commerce-evalueringsmiljøet den komplette Commerce-opplevelsen, og kan brukes av kunder og implementeringspartnere til å evaluere produktet, gi tilbakemelding og utføre tilpassings-/gapanalyse.</span><span class="sxs-lookup"><span data-stu-id="cf1f5-110">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="cf1f5-111">Begrensninger i evalueringsmiljøet for Commerce</span><span class="sxs-lookup"><span data-stu-id="cf1f5-111">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="cf1f5-112">Selv om evalueringsmiljøet i Commerce inneholder det fullstendige settet med Commerce-funksjoner, er det noen mindre begrensninger:</span><span class="sxs-lookup"><span data-stu-id="cf1f5-112">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="cf1f5-113">Selv om selve Commerce-evalueringsmiljøet ikke har noen geografiske begrensninger, skal komponenter i miljøet, for eksempel Retail Cloud Scale Unit (RCSU) og e-handelsprogrammer, bare klargjøres i USA.</span><span class="sxs-lookup"><span data-stu-id="cf1f5-113">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="cf1f5-114">Bruk av evalueringsmiljøet for Commerce har en 30-dagers tidsbegrensning fra datoen for klargjøring av e-handel.</span><span class="sxs-lookup"><span data-stu-id="cf1f5-114">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="cf1f5-115">Evalueringsmiljøet for Commerce kan med hell distribueres og initialiseres bare i et miljø som bruker demonstrasjonstopologien, der alle komponentene i et miljø distribueres på én enkelt skybasert virtuell maskin (VM).</span><span class="sxs-lookup"><span data-stu-id="cf1f5-115">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="cf1f5-116">Den største begrensningen for denne topologien er antall samtidige brukere som miljøet kan støtte.</span><span class="sxs-lookup"><span data-stu-id="cf1f5-116">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="cf1f5-117">Kom i gang</span><span class="sxs-lookup"><span data-stu-id="cf1f5-117">Get started</span></span>

<span data-ttu-id="cf1f5-118">Hvis du vil klargjøre evalueringsmiljøet for Commerce, kan du se [Klargjøre et Commerce-evalueringsmiljø](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="cf1f5-118">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf1f5-119">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="cf1f5-119">Additional resources</span></span>

[<span data-ttu-id="cf1f5-120">Klargjøre et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cf1f5-120">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="cf1f5-121">Konfigurere et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="cf1f5-121">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="cf1f5-122">Konfigurere BOPIS i et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cf1f5-122">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="cf1f5-123">Konfigurere valgfrie funksjoner for et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cf1f5-123">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="cf1f5-124">Vanlige spørsmål om Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="cf1f5-124">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)
