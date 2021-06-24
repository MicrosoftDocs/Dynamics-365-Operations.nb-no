---
title: Vanlige spørsmål om evalueringsmiljø for Dynamics 365 Commerce
description: Dette emnet gir svar på vanlige spørsmål om evalueringsmiljøet for Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a0c6f82432a4786f23f12122f3806c3b96a05c8f
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193600"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a><span data-ttu-id="80ad3-103">Vanlige spørsmål om evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="80ad3-103">Dynamics 365 Commerce evaluation environment FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="80ad3-104">Dette emnet gir svar på vanlige spørsmål om evalueringsmiljøet for Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="80ad3-104">This topic provides answers to frequently asked questions about the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="80ad3-105">**Kan vi bruke Commerce-evalueringsmiljøet som en e-handel-butikkfasade for kunder som for tiden implementerer Retail?**</span><span class="sxs-lookup"><span data-stu-id="80ad3-105">**Can we use the Commerce evaluation environment as an e-Commerce storefront for customers that currently implement Retail?**</span></span>

<span data-ttu-id="80ad3-106">Nr.</span><span class="sxs-lookup"><span data-stu-id="80ad3-106">No.</span></span> <span data-ttu-id="80ad3-107">Evalueringsmiljøet for Commerce er bare for evaluering.</span><span class="sxs-lookup"><span data-stu-id="80ad3-107">The Commerce evaluation environment is only for evaluation.</span></span> <span data-ttu-id="80ad3-108">Hvis du trenger et miljø for en kunde som implementerer Retail, kan du kontakte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="80ad3-108">If you require an environment for a customer that implements Retail, contact Microsoft.</span></span>

<span data-ttu-id="80ad3-109">**Kan evalueringsmiljøet for Commerce brukes til å klargjøre e-handelsfunksjonene oppå et eksisterende program/miljø som implementerer Retail?**</span><span class="sxs-lookup"><span data-stu-id="80ad3-109">**Can the Commerce evaluation environment be used to provision the e-Commerce features on top of an existing application/environment that implements Retail?**</span></span>

<span data-ttu-id="80ad3-110">Nei (for det meste).</span><span class="sxs-lookup"><span data-stu-id="80ad3-110">No (mostly).</span></span> <span data-ttu-id="80ad3-111">Komponentene for Commerce-evaluering er bare tilgjengelige for miljøer som samsvarer med konfigurasjonene som er angitt i veiledningen for forhåndskrav og klargjøring.</span><span class="sxs-lookup"><span data-stu-id="80ad3-111">The Commerce evaluation components are available only to environments that match the configurations that are specified in the prerequisites and provisioning guide.</span></span> <span data-ttu-id="80ad3-112">I tillegg vil de nødvendige grunndemodataene ikke være tilgjengelige i miljøer som ble distribuert med en første versjon som er eldre enn 10.0.8.</span><span class="sxs-lookup"><span data-stu-id="80ad3-112">Additionally, the required base demo data won't be available in environments that were deployed with an initial release that is earlier than 10.0.8.</span></span> 

<span data-ttu-id="80ad3-113">**Hvilke kostnader er involvert i distribusjon av evalueringsmiljøet for Commerce på Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span><span class="sxs-lookup"><span data-stu-id="80ad3-113">**What costs are involved in deploying the Commerce evaluation environment on Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span></span>

<span data-ttu-id="80ad3-114">Et tradisjonelt Dynamics 365 Finance/Dynamics 365 Supply Chain Management-/Dynamics 365 Commerce-hovedkvarterdemomiljø (virtuell maskin\[VM\]) vil være vert for Azure-abonnementet.</span><span class="sxs-lookup"><span data-stu-id="80ad3-114">A traditional Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce headquarters demo environment (virtual machine \[VM\]) will be hosted in your Azure subscription.</span></span> <span data-ttu-id="80ad3-115">Du kan bruke [Azure prising-kalkulatoren](https://azure.microsoft.com/pricing/calculator/) til å estimere denne kostnaden.</span><span class="sxs-lookup"><span data-stu-id="80ad3-115">You can use the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/) to estimate this cost.</span></span>

<span data-ttu-id="80ad3-116">Andre komponenter som for eksempel Commerce Scale Unit, Commerce-områdebygger og ditt e-handelsområde vil være tilgjengelig som en tjeneste (SaaS) og være vertsbasert hos Microsoft.</span><span class="sxs-lookup"><span data-stu-id="80ad3-116">Other components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site will be available as software as a service (SaaS) and hosted by Microsoft.</span></span>

<span data-ttu-id="80ad3-117">**Hvilke Azure-områder støttes for øyeblikket for evalueringsmiljøet i Commerce?**</span><span class="sxs-lookup"><span data-stu-id="80ad3-117">**Which Azure geographies are currently supported for the Commerce evaluation environment?**</span></span>

<span data-ttu-id="80ad3-118">Evalueringsmiljøet for Commerce kan bare distribueres i Nord-Amerika-området.</span><span class="sxs-lookup"><span data-stu-id="80ad3-118">The Commerce evaluation environment can be deployed only in the North America geography.</span></span>

<span data-ttu-id="80ad3-119">**Finnes det en nedlastbar virtuell harddisk (VHD) som har det komplette alternativet for OneBox virtuell maskin (VM)?**</span><span class="sxs-lookup"><span data-stu-id="80ad3-119">**Is there a downloadable virtual hard disk (VHD) that has the complete OneBox virtual machine (VM) option?**</span></span>

<span data-ttu-id="80ad3-120">Dynamics 365 Commerce og Commerce Scale Unit er fullstendig programvare som en tjeneste (SaaS) og må være skybasert.</span><span class="sxs-lookup"><span data-stu-id="80ad3-120">Dynamics 365 Commerce and Commerce Scale Unit are completely software as a service (SaaS) and must be cloud-hosted.</span></span>

<span data-ttu-id="80ad3-121">**Hvor lenge kan evalueringsmiljøet for Commerce brukes?**</span><span class="sxs-lookup"><span data-stu-id="80ad3-121">**How long can the Commerce evaluation environment be used?**</span></span>

<span data-ttu-id="80ad3-122">Commerce-evalueringsmiljøet har en 30-dagers tidsgrense fra datoen SaaS-komponenter som for eksempel Commerce Scale Unit, Commerce-områdebygger og ditt e-handelsområde klargjøres.</span><span class="sxs-lookup"><span data-stu-id="80ad3-122">The Commerce evaluation environment has a 30-day time limit from the date when SaaS components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site are provisioned.</span></span>

<span data-ttu-id="80ad3-123">**Kan jeg forlenge tidsbegrensningen for evalueringsmiljøet i Commerce?**</span><span class="sxs-lookup"><span data-stu-id="80ad3-123">**Can I extend the time limit for my Commerce evaluation environment?**</span></span>

<span data-ttu-id="80ad3-124">Utvidelsen av tidsgrensen er et unntak fra normen og vurderes for hvert tilfelle.</span><span class="sxs-lookup"><span data-stu-id="80ad3-124">Extension of the time limit is an exception to the norm and is considered on a case-by-case basis.</span></span> <span data-ttu-id="80ad3-125">Du må kontakte din Microsoft-partnerkontakten for hjelp.</span><span class="sxs-lookup"><span data-stu-id="80ad3-125">You should reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="80ad3-126">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="80ad3-126">Additional resources</span></span>

[<span data-ttu-id="80ad3-127">Oversikt over Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="80ad3-127">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="80ad3-128">Klargjøre et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="80ad3-128">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="80ad3-129">Konfigurere et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="80ad3-129">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="80ad3-130">Konfigurere BOPIS i et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="80ad3-130">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="80ad3-131">Konfigurere valgfrie funksjoner for et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="80ad3-131">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]