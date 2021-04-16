---
title: 'Definere delvis prosess for syklustelling for lokasjon '
description: Når du bruker Bla antall planer du oppretter opptelling, kan du lede faktiske opptellingsdatoen operasjonene ved å be om at bare bestemte produkter og produktvarianter telles i stedet for alle lager på lokasjonen.
author: ShylaThompson
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fcda301934c6ccc06f17ed8ae13c52754336d2ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830912"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="f9172-103">Definere delvis prosess for syklustelling for lokasjon </span><span class="sxs-lookup"><span data-stu-id="f9172-103">Define partial location cycle counting process</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f9172-104">Når du bruker Bla antall planer du oppretter opptelling, kan du lede faktiske opptellingsdatoen operasjonene ved å be om at bare bestemte produkter og produktvarianter telles i stedet for alle lager på lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="f9172-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="f9172-105">Ved å filtrere etter bestemte produkter kan lagersjefen redusere indirekte kostnader til gjennomgang, unngå konsolideringsfeil og spare tid.</span><span class="sxs-lookup"><span data-stu-id="f9172-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="f9172-106">Vanligvis utfører en lagersjef konfigurasjonsoppgavene.</span><span class="sxs-lookup"><span data-stu-id="f9172-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="f9172-107">Du kan gå gjennom denne fremgangsmåten i USMF-demonstrasjonsdataselskapet eller i dine egne data.</span><span class="sxs-lookup"><span data-stu-id="f9172-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="f9172-108">Opprette en mal for syklustellingsarbeid</span><span class="sxs-lookup"><span data-stu-id="f9172-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="f9172-109">Gå til Lagerstyring > Oppsett > Arbeid > Arbeidsmaler.</span><span class="sxs-lookup"><span data-stu-id="f9172-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="f9172-110">Velg "Syklustelling" i feltet Arbeidsordretype.</span><span class="sxs-lookup"><span data-stu-id="f9172-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="f9172-111">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="f9172-111">Click New.</span></span>
4. <span data-ttu-id="f9172-112">Angi et nummer i Sekvensnummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="f9172-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="f9172-113">Sorteringsrekkefølgen er fra det laveste tallet til det høyeste tallet.</span><span class="sxs-lookup"><span data-stu-id="f9172-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="f9172-114">Verdien må være over 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f9172-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="f9172-115">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f9172-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="f9172-116">Angi en verdi i feltet Arbeidsmal.</span><span class="sxs-lookup"><span data-stu-id="f9172-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="f9172-117">Skriv inn en verdi i feltet Beskrivelse av arbeidsmal.</span><span class="sxs-lookup"><span data-stu-id="f9172-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="f9172-118">Angi eller velg en verdi i feltet ID for arbeidsutvalg.</span><span class="sxs-lookup"><span data-stu-id="f9172-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="f9172-119">Angi et tall i Arbiesdprioritet-feltet.</span><span class="sxs-lookup"><span data-stu-id="f9172-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="f9172-120">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="f9172-120">Click Save.</span></span>
11. <span data-ttu-id="f9172-121">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="f9172-121">Click New.</span></span>
12. <span data-ttu-id="f9172-122">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f9172-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="f9172-123">Velg Opptelling i Arbeidstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="f9172-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="f9172-124">Angi eller velg en verdi i feltet Arbeidsklasse-ID.</span><span class="sxs-lookup"><span data-stu-id="f9172-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="f9172-125">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="f9172-125">Click Save.</span></span>
16. <span data-ttu-id="f9172-126">Klikk på Arbeidslinjeinndelinger.</span><span class="sxs-lookup"><span data-stu-id="f9172-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="f9172-127">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="f9172-127">Click New.</span></span>
18. <span data-ttu-id="f9172-128">Angi et nummer i Sekvensnummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="f9172-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="f9172-129">Sorteringsrekkefølgen er fra det laveste tallet til det høyeste tallet.</span><span class="sxs-lookup"><span data-stu-id="f9172-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="f9172-130">Verdien må være over 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f9172-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="f9172-131">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="f9172-131">Click Save.</span></span>
20. <span data-ttu-id="f9172-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f9172-132">Close the page.</span></span>
21. <span data-ttu-id="f9172-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f9172-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="f9172-134">Opprette en syklustellingplan</span><span class="sxs-lookup"><span data-stu-id="f9172-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="f9172-135">Gå til Lagerstyring > Oppsett > Syklustelling > Planer for syklustelling.</span><span class="sxs-lookup"><span data-stu-id="f9172-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="f9172-136">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="f9172-136">Click New.</span></span>
3. <span data-ttu-id="f9172-137">Skriv inn en verdi i feltet ID for syklustellingsplan.</span><span class="sxs-lookup"><span data-stu-id="f9172-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="f9172-138">Skriv inn en verdi i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="f9172-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f9172-139">Angi et tall i feltet Største antall syklustellinger.</span><span class="sxs-lookup"><span data-stu-id="f9172-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="f9172-140">Angi eller velg en verdi i feltet Arbeidsmal.</span><span class="sxs-lookup"><span data-stu-id="f9172-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="f9172-141">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="f9172-141">Click New.</span></span>
8. <span data-ttu-id="f9172-142">Angi et nummer i Sekvensnummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="f9172-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="f9172-143">Sorteringsrekkefølgen er fra det laveste tallet til det høyeste tallet.</span><span class="sxs-lookup"><span data-stu-id="f9172-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="f9172-144">Verdien må være over 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f9172-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="f9172-145">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f9172-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="f9172-146">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="f9172-146">Click Save.</span></span>
11. <span data-ttu-id="f9172-147">Klikk på Definer produktspørring.</span><span class="sxs-lookup"><span data-stu-id="f9172-147">Click Define product query.</span></span>
12. <span data-ttu-id="f9172-148">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f9172-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="f9172-149">Angi eller velg en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="f9172-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="f9172-150">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="f9172-150">Click OK.</span></span>
15. <span data-ttu-id="f9172-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f9172-151">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]