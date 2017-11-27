---
title: Delvis lokasjonssyklustelling
description: "Syklustellingsplaner styrer de faktiske telleoperasjonene. Du kan be om at bare bestemte produkter og produktvarianter telles, i stedet for all lagerbeholdning på et sted."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0e0f9d81f4d5943a89d8ac87776e05acb32cb8d9
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="partial-location-cycle-counting"></a><span data-ttu-id="e9afa-104">Delvis lokasjonssyklustelling</span><span class="sxs-lookup"><span data-stu-id="e9afa-104">Partial location cycle counting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e9afa-105">Syklustellingsplaner styrer de faktiske telleoperasjonene.</span><span class="sxs-lookup"><span data-stu-id="e9afa-105">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="e9afa-106">Du kan be om at bare bestemte produkter og produktvarianter telles, i stedet for all lagerbeholdning på et sted.</span><span class="sxs-lookup"><span data-stu-id="e9afa-106">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="e9afa-107">Ved å bruke syklustellingsplaner til å opprette opptellingsarbeid, kan du styre de faktiske opptellingsoperasjonene.</span><span class="sxs-lookup"><span data-stu-id="e9afa-107">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="e9afa-108">Du kan be om at bare bestemte produkter og produktvarianter telles, i stedet for all lagerbeholdning på et sted.</span><span class="sxs-lookup"><span data-stu-id="e9afa-108">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="e9afa-109">Ved å filtrere etter bestemte produkter kan lagersjefen redusere indirekte kostnader til gjennomgang, unngå konsolideringsfeil og spare tid.</span><span class="sxs-lookup"><span data-stu-id="e9afa-109">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="e9afa-110">Slik konfigurerer du delvis lokasjonssyklustelling</span><span class="sxs-lookup"><span data-stu-id="e9afa-110">How to configure partial location cycle counting</span></span>
<span data-ttu-id="e9afa-111">Når du bruker arbeidsprosessen for lageret for å telle operasjoner, opprettes et arbeidshode for hver lokasjon.</span><span class="sxs-lookup"><span data-stu-id="e9afa-111">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="e9afa-112">Når du definerer syklustellingsplanen, kan du bruke spørringen **Velg lokasjoner** for å begrense syklustellingsarbeidet som er opprettet.</span><span class="sxs-lookup"><span data-stu-id="e9afa-112">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="e9afa-113">Når du velger produkter for syklustellingsplanen, kan du velge både produkt- og produktetvariantspørringer for å begrense hva som telles.</span><span class="sxs-lookup"><span data-stu-id="e9afa-113">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="e9afa-114">Du kan tilknytte en **arbeidsmalen** til en syklustellingsplan for å definere hvordan syklustellingsarbeidet skal opprettes.</span><span class="sxs-lookup"><span data-stu-id="e9afa-114">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="e9afa-115">Arbeidsmalen for opptellingsoperasjoner refereres direkte fra syklustellingsplanen.</span><span class="sxs-lookup"><span data-stu-id="e9afa-115">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="e9afa-116">Når du definerer detaljer for arbeidsmalen, kan du bruke **arbeidslinjeskift**-alternativet for å angi om arbeidslinjene i opptellingn må grupperes etter varenummer eller produktvariantnummer.</span><span class="sxs-lookup"><span data-stu-id="e9afa-116">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="e9afa-117">Dette oppsettet er nødvendig hvis du vil telle lagerbeholdningen bare for bestemte produkter på et sted.</span><span class="sxs-lookup"><span data-stu-id="e9afa-117">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="e9afa-118">Linjene som opprettes for syklustellingsarbeidet, vil ha det informasjonsnivået du angir her, og den styrte opptellingsoperasjonen blir håndtert baser tpå dette nivået.</span><span class="sxs-lookup"><span data-stu-id="e9afa-118">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="e9afa-119">Hvis du knytter syklustellingsplaner til arbeidsmaler ved hjelp av alternativet **arbeidslinjeskift**, velges feltet **Delvis syklustelling** for syklustellingsarbeidet som er opprettet, og flere arbeidslinjer for syklustelling opprettes basert på arbeidsmalens definisjon.</span><span class="sxs-lookup"><span data-stu-id="e9afa-119">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="e9afa-120">Før delvis syklustellingsarbeid kan behandles, må du, som et minimum velge **Vis varenummer** for menyelementet mobilenhet som en del av oppsettet for syklustelling.</span><span class="sxs-lookup"><span data-stu-id="e9afa-120">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="e9afa-121">Lageroperatøren vil bli bedt om bare å registrere opptellingsinformasjon som er knyttet til opptellingslinjer (varenumre og produktdimensjoner).</span><span class="sxs-lookup"><span data-stu-id="e9afa-121">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="e9afa-122">Alle andre lagerbeholdninger vil bli ignorert for denne opptellingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="e9afa-122">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="e9afa-123">For den delvise syklustellingsprosessn blir ikke dato/klokkeslett for **Siste syklustelling** oppdatert for lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="e9afa-123">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="e9afa-124">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e9afa-124">Example</span></span>
<span data-ttu-id="e9afa-125">I dette eksemplet må bare varenummeret A0001 telles i lager 61.</span><span class="sxs-lookup"><span data-stu-id="e9afa-125">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="e9afa-126">Det opprettes en ny mal for syklustelling.</span><span class="sxs-lookup"><span data-stu-id="e9afa-126">A new work template for cycle counting is created.</span></span> <span data-ttu-id="e9afa-127">Alternativet **arbeidslinjeskift** brukes til å gruppere opptellingsarbeidslinjer etter varenummer.</span><span class="sxs-lookup"><span data-stu-id="e9afa-127">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="e9afa-128">Derfor får arbeidet som er opprettet for syklustelling, linjer per varenummer.</span><span class="sxs-lookup"><span data-stu-id="e9afa-128">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="e9afa-129">Du kan også gruppere linjene etter produktvariantnummer.</span><span class="sxs-lookup"><span data-stu-id="e9afa-129">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="e9afa-130">Det opprettes en ny plan for syklustelling som refererer til den nylig opprettede arbeidsmalen.</span><span class="sxs-lookup"><span data-stu-id="e9afa-130">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="e9afa-131">Syklustellingsplanen inkluderer alle lokasjoner på lager 61 (spørringen **Veg lokasjoner**) som rommer beholdningen for varenummer A0001.</span><span class="sxs-lookup"><span data-stu-id="e9afa-131">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="e9afa-132">Valg av bestemte produkter er definert i delen **Produktvalg for syklustellingsplan**.</span><span class="sxs-lookup"><span data-stu-id="e9afa-132">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="e9afa-133">Du kan velge produkter for planer for syklustelling ved å sette feltet **Tomme lokasjoner** til **Ekskluder tomme**.</span><span class="sxs-lookup"><span data-stu-id="e9afa-133">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.</span></span> <span data-ttu-id="e9afa-134">Når planen for syklustellingen behandles, opprettes det delvis syklustellingsarbeid for varenummer A0001.</span><span class="sxs-lookup"><span data-stu-id="e9afa-134">When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="e9afa-135">Den faktiske telleprosessen kan utføres ved hjelp av et menyelement for mobilenhet for veiledet syklustelling.</span><span class="sxs-lookup"><span data-stu-id="e9afa-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="see-also"></a><span data-ttu-id="e9afa-136">Se også</span><span class="sxs-lookup"><span data-stu-id="e9afa-136">See also</span></span>
--------

[<span data-ttu-id="e9afa-137">Syklustelling</span><span class="sxs-lookup"><span data-stu-id="e9afa-137">Cycle counting</span></span>](cycle-counting.md)


