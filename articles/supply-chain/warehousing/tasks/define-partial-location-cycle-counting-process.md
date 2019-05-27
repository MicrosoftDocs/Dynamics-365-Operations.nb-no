---
title: 'Definere delvis prosess for syklustelling for lokasjon '
description: Når du bruker Bla antall planer du oppretter opptelling, kan du lede faktiske opptellingsdatoen operasjonene ved å be om at bare bestemte produkter og produktvarianter telles i stedet for alle lager på lokasjonen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3aafb42cea1664b0629f57fe4492736601902cc1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568264"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="383f4-103">Definere delvis prosess for syklustelling for lokasjon </span><span class="sxs-lookup"><span data-stu-id="383f4-103">Define partial location cycle counting process</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="383f4-104">Når du bruker Bla antall planer du oppretter opptelling, kan du lede faktiske opptellingsdatoen operasjonene ved å be om at bare bestemte produkter og produktvarianter telles i stedet for alle lager på lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="383f4-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="383f4-105">Ved å filtrere etter bestemte produkter kan lagersjefen redusere indirekte kostnader til gjennomgang, unngå konsolideringsfeil og spare tid.</span><span class="sxs-lookup"><span data-stu-id="383f4-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="383f4-106">Vanligvis utfører en lagersjef konfigurasjonsoppgavene.</span><span class="sxs-lookup"><span data-stu-id="383f4-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="383f4-107">Du kan gå gjennom denne fremgangsmåten i USMF-demonstrasjonsdataselskapet eller i dine egne data.</span><span class="sxs-lookup"><span data-stu-id="383f4-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="383f4-108">Opprette en mal for syklustellingsarbeid</span><span class="sxs-lookup"><span data-stu-id="383f4-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="383f4-109">Gå til Lagerstyring > Oppsett > Arbeid > Arbeidsmaler.</span><span class="sxs-lookup"><span data-stu-id="383f4-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="383f4-110">Velg "Syklustelling" i feltet Arbeidsordretype.</span><span class="sxs-lookup"><span data-stu-id="383f4-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="383f4-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="383f4-111">Click New.</span></span>
4. <span data-ttu-id="383f4-112">Angi et nummer i Sekvensnummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="383f4-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="383f4-113">Sorteringsrekkefølgen er fra det laveste tallet til det høyeste tallet.</span><span class="sxs-lookup"><span data-stu-id="383f4-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="383f4-114">Verdien må være over 0 (null).</span><span class="sxs-lookup"><span data-stu-id="383f4-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="383f4-115">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="383f4-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="383f4-116">Angi en verdi i feltet Arbeidsmal.</span><span class="sxs-lookup"><span data-stu-id="383f4-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="383f4-117">Skriv inn en verdi i feltet Beskrivelse av arbeidsmal.</span><span class="sxs-lookup"><span data-stu-id="383f4-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="383f4-118">Angi eller velg en verdi i feltet ID for arbeidsutvalg.</span><span class="sxs-lookup"><span data-stu-id="383f4-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="383f4-119">Angi et tall i Arbiesdprioritet-feltet.</span><span class="sxs-lookup"><span data-stu-id="383f4-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="383f4-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="383f4-120">Click Save.</span></span>
11. <span data-ttu-id="383f4-121">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="383f4-121">Click New.</span></span>
12. <span data-ttu-id="383f4-122">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="383f4-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="383f4-123">Velg Opptelling i Arbeidstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="383f4-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="383f4-124">Angi eller velg en verdi i feltet Arbeidsklasse-ID.</span><span class="sxs-lookup"><span data-stu-id="383f4-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="383f4-125">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="383f4-125">Click Save.</span></span>
16. <span data-ttu-id="383f4-126">Klikk Arbeidslinjeinndelinger.</span><span class="sxs-lookup"><span data-stu-id="383f4-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="383f4-127">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="383f4-127">Click New.</span></span>
18. <span data-ttu-id="383f4-128">Angi et nummer i Sekvensnummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="383f4-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="383f4-129">Sorteringsrekkefølgen er fra det laveste tallet til det høyeste tallet.</span><span class="sxs-lookup"><span data-stu-id="383f4-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="383f4-130">Verdien må være over 0 (null).</span><span class="sxs-lookup"><span data-stu-id="383f4-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="383f4-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="383f4-131">Click Save.</span></span>
20. <span data-ttu-id="383f4-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="383f4-132">Close the page.</span></span>
21. <span data-ttu-id="383f4-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="383f4-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="383f4-134">Opprette en syklustellingplan</span><span class="sxs-lookup"><span data-stu-id="383f4-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="383f4-135">Gå til Lagerstyring > Oppsett > Syklustelling > Planer for syklustelling.</span><span class="sxs-lookup"><span data-stu-id="383f4-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="383f4-136">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="383f4-136">Click New.</span></span>
3. <span data-ttu-id="383f4-137">Skriv inn en verdi i feltet ID for syklustellingsplan.</span><span class="sxs-lookup"><span data-stu-id="383f4-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="383f4-138">Skriv inn en verdi i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="383f4-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="383f4-139">Angi et tall i feltet Største antall syklustellinger.</span><span class="sxs-lookup"><span data-stu-id="383f4-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="383f4-140">Angi eller velg en verdi i feltet Arbeidsmal.</span><span class="sxs-lookup"><span data-stu-id="383f4-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="383f4-141">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="383f4-141">Click New.</span></span>
8. <span data-ttu-id="383f4-142">Angi et nummer i Sekvensnummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="383f4-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="383f4-143">Sorteringsrekkefølgen er fra det laveste tallet til det høyeste tallet.</span><span class="sxs-lookup"><span data-stu-id="383f4-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="383f4-144">Verdien må være over 0 (null).</span><span class="sxs-lookup"><span data-stu-id="383f4-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="383f4-145">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="383f4-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="383f4-146">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="383f4-146">Click Save.</span></span>
11. <span data-ttu-id="383f4-147">Klikk Definer produktspørring.</span><span class="sxs-lookup"><span data-stu-id="383f4-147">Click Define product query.</span></span>
12. <span data-ttu-id="383f4-148">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="383f4-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="383f4-149">Angi eller velg en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="383f4-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="383f4-150">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="383f4-150">Click OK.</span></span>
15. <span data-ttu-id="383f4-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="383f4-151">Close the page.</span></span>

