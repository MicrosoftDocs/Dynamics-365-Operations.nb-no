--- 
title: Definere en prosess for minimums-/maksimumsetterfylling
description: "Denne fremgangsmåten viser hvordan du definerer en ny etterfyllingprosess som bruker strategien for minimums-/maksimumsetterfylling."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 09a5bbe7601248fd2635fda4a0d87973a6e1ceba
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-a-min-max-replenishment-process"></a><span data-ttu-id="f373f-103">Definere en prosess for minimums-/maksimumsetterfylling</span><span class="sxs-lookup"><span data-stu-id="f373f-103">Set up a min-max replenishment process</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f373f-104">Denne fremgangsmåten viser hvordan du definerer en ny etterfyllingprosess som bruker strategien for minimums-/maksimumsetterfylling.</span><span class="sxs-lookup"><span data-stu-id="f373f-104">This procedure shows you how to set up a new replenishment process which uses the minimum/maximum replenishment strategy.</span></span> <span data-ttu-id="f373f-105">Når lagernivået synker til under minimumsnivået, opprettes det arbeid for å etterfylle lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="f373f-105">When inventory falls below the minimum level, work will be created to replenish the location.</span></span> <span data-ttu-id="f373f-106">Fremgangsmåten viser også hvordan du bruker faste plukklokasjoner for å tillate etterfylling selv om lagernivået synker til under minimumsnivået, og hvordan du aktiverer at etterfyllingsprosessen skal kjøres regelmessig ved hjelp av en satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="f373f-106">The procedure also shows how to use fixed picking locations to allow restocking even if inventory falls below the minimum level, and how to enable the replenishment process to run regularly using a batch job.</span></span> <span data-ttu-id="f373f-107">Disse oppgavene vil vanligvis utføres av en lagersjef.</span><span class="sxs-lookup"><span data-stu-id="f373f-107">These tasks would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="f373f-108">Du kan kjøre denne prosedyren i USMF-demodatafirmaet ved hjelp av eksempelverdiene i notatene, eller du kan kjøre den på dine egne data.</span><span class="sxs-lookup"><span data-stu-id="f373f-108">You can run this procedure in the USMF demo data company using the example values in the notes, or can run it on your own data.</span></span> <span data-ttu-id="f373f-109">Hvis du bruker dine egne data, må du kontrollere at du har et lager som er aktivert for lagerstyringsprosesser.</span><span class="sxs-lookup"><span data-stu-id="f373f-109">If you’re using your own data, make sure that you have a warehouse that’s enabled for Warehouse management processes.</span></span>


## <a name="create-a-fixed-picking-location"></a><span data-ttu-id="f373f-110">Opprette en fast plukklokasjon</span><span class="sxs-lookup"><span data-stu-id="f373f-110">Create a fixed picking location</span></span>
1. <span data-ttu-id="f373f-111">Gå til Lagerstyring > Oppsett > Lager > Faste lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="f373f-111">Go to Warehouse management > Setup > Warehouse > Fixed locations.</span></span>
    * <span data-ttu-id="f373f-112">Dette er en valgfri oppgave for minimums-/maksimumsetterfylling, men hvis du bruker fast plukklokasjon, gjør dette at lageret etterfylles selv om det faller under minimumsnivået, fordi systemet kan finne ut hvilke varer som må etterfylles, selv om det ikke er noen igjen.</span><span class="sxs-lookup"><span data-stu-id="f373f-112">This is an optional task for min-max replenishment, but if you use fixed picking location, this allows stock to be replenished even if it falls below the minimum level, because the system can determine which items need to be replenished, even if there aren't any left.</span></span>  
2. <span data-ttu-id="f373f-113">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f373f-113">Click New.</span></span>
3. <span data-ttu-id="f373f-114">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="f373f-114">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="f373f-115">Hvis du bruker USMF, kan du velge vare 'A0001'.</span><span class="sxs-lookup"><span data-stu-id="f373f-115">If you’re using USMF, you can select item A0001.</span></span>  
4. <span data-ttu-id="f373f-116">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="f373f-116">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f373f-117">Hvis du bruker USMF, kan du velge område 2.</span><span class="sxs-lookup"><span data-stu-id="f373f-117">If you’re using USMF, you can select site 2.</span></span>  
5. <span data-ttu-id="f373f-118">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="f373f-118">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f373f-119">Hvis du bruker USMF, kan du velge lager 24.</span><span class="sxs-lookup"><span data-stu-id="f373f-119">If you’re using USMF, you can select warehouse 24.</span></span>  
6. <span data-ttu-id="f373f-120">Angi eller velg en verdi i feltet Lokasjon.</span><span class="sxs-lookup"><span data-stu-id="f373f-120">In the Location field, enter or select a value.</span></span>
    * <span data-ttu-id="f373f-121">Hvis du bruker USMF, kan du velge CP-003.</span><span class="sxs-lookup"><span data-stu-id="f373f-121">If you’re using USMF, you can select CP-003.</span></span>  
7. <span data-ttu-id="f373f-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f373f-122">Close the page.</span></span>

## <a name="create-a-replenishment-location-directive"></a><span data-ttu-id="f373f-123">Opprette et lokasjonsdirektiv for etterfylling</span><span class="sxs-lookup"><span data-stu-id="f373f-123">Create a replenishment location directive</span></span>
1. <span data-ttu-id="f373f-124">Gå til Lagerstyring > Oppsett > Lokasjonsdirektiver.</span><span class="sxs-lookup"><span data-stu-id="f373f-124">Go to Warehouse management > Setup > Location directives.</span></span>
    * <span data-ttu-id="f373f-125">Lokasjonsdirektiver brukes til å bestemme hvor varene skal plukkes fra i etterfyllingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="f373f-125">Location directives are used to determine where items should be picked from in the replenishment process.</span></span>  
2. <span data-ttu-id="f373f-126">Velg Etterfylling i feltet Arbeidsordretype.</span><span class="sxs-lookup"><span data-stu-id="f373f-126">In the Work order type field, select 'Replenishment'.</span></span>
3. <span data-ttu-id="f373f-127">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f373f-127">Click New.</span></span>
4. <span data-ttu-id="f373f-128">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f373f-128">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f373f-129">Velg Plukk i Arbeidstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="f373f-129">In the Work type field, select 'Pick'.</span></span>
6. <span data-ttu-id="f373f-130">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="f373f-130">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f373f-131">Hvis du bruker USMF, kan du velge område 2.</span><span class="sxs-lookup"><span data-stu-id="f373f-131">If you’re using USMF, you can select site 2.</span></span>  
7. <span data-ttu-id="f373f-132">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="f373f-132">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f373f-133">Hvis du bruker USMF, kan du velge lager 24.</span><span class="sxs-lookup"><span data-stu-id="f373f-133">If you’re using USMF, you can select warehouse 24.</span></span>  
8. <span data-ttu-id="f373f-134">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f373f-134">Click Save.</span></span>
9. <span data-ttu-id="f373f-135">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f373f-135">Click New.</span></span>
10. <span data-ttu-id="f373f-136">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f373f-136">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="f373f-137">Angi et tall i feltet Til-antall.</span><span class="sxs-lookup"><span data-stu-id="f373f-137">In the To quantity field, enter a number.</span></span>
    * <span data-ttu-id="f373f-138">Du kan for eksempel sette dette til 9999.</span><span class="sxs-lookup"><span data-stu-id="f373f-138">For example, you can set it to 9999.</span></span>  
12. <span data-ttu-id="f373f-139">Merk av for Tillat oppdeling.</span><span class="sxs-lookup"><span data-stu-id="f373f-139">Select the Allow split check box.</span></span>
    * <span data-ttu-id="f373f-140">Hvis du velger dette alternativet, tillater arbeidsopprettelsesprosessen at arbeidslinjeantall kan deles på tvers av flere lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="f373f-140">If you select this option, the work creation process will allow work line quantities to be split across multiple locations.</span></span>  
13. <span data-ttu-id="f373f-141">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f373f-141">Click Save.</span></span>
14. <span data-ttu-id="f373f-142">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f373f-142">Click New.</span></span>
15. <span data-ttu-id="f373f-143">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f373f-143">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="f373f-144">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f373f-144">In the Name field, type a value.</span></span>
17. <span data-ttu-id="f373f-145">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f373f-145">Click Save.</span></span>
18. <span data-ttu-id="f373f-146">Klikk Rediger spørring.</span><span class="sxs-lookup"><span data-stu-id="f373f-146">Click Edit query.</span></span>
    * <span data-ttu-id="f373f-147">Du kan redigere denne spørringen for å legge til begrensninger der lageret kan velges fra i etterfyllingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="f373f-147">You can edit this query to add restrictions where inventory can be selected from in the replenishment process.</span></span> <span data-ttu-id="f373f-148">Det kan for eksempel være at lageret bare skal brukes fra partiområdet i lageret.</span><span class="sxs-lookup"><span data-stu-id="f373f-148">For example, it could be that inventory should only be used from the Bulk area of the warehouse.</span></span>  
19. <span data-ttu-id="f373f-149">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f373f-149">Click OK.</span></span>
20. <span data-ttu-id="f373f-150">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f373f-150">Close the page.</span></span>

## <a name="create-a-replenishment-work-template"></a><span data-ttu-id="f373f-151">Opprette en arbeidsmal for etterfylling</span><span class="sxs-lookup"><span data-stu-id="f373f-151">Create a replenishment work template</span></span>
1. <span data-ttu-id="f373f-152">Gå til Lagerstyring > Oppsett > Arbeid > Arbeidsmaler.</span><span class="sxs-lookup"><span data-stu-id="f373f-152">Go to Warehouse management > Setup > Work > Work templates.</span></span>
    * <span data-ttu-id="f373f-153">Arbeidsmalen brukes for å veilede systemet for hvordan arbeidet for minimums-/maksimumsetterfylling skal opprettes.</span><span class="sxs-lookup"><span data-stu-id="f373f-153">The work template is use to guide the system as to how the min/max replenishment work must be created.</span></span> <span data-ttu-id="f373f-154">Som et minimum må det være en arbeidsmallinje for plukking og plassering.</span><span class="sxs-lookup"><span data-stu-id="f373f-154">As a minimum, there must be a work template line for a pick and a put.</span></span> <span data-ttu-id="f373f-155">Arbeidsmalen vil si at den er ugyldig til all nødvendig informasjon er fylt ut.</span><span class="sxs-lookup"><span data-stu-id="f373f-155">The work template will say that it’s Invalid until all the necessary information has been filled in.</span></span>  
2. <span data-ttu-id="f373f-156">Velg Etterfylling i feltet Arbeidsordretype.</span><span class="sxs-lookup"><span data-stu-id="f373f-156">In the Work order type field, select 'Replenishment'.</span></span>
3. <span data-ttu-id="f373f-157">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f373f-157">Click New.</span></span>
4. <span data-ttu-id="f373f-158">Angi en verdi i feltet Arbeidsmal.</span><span class="sxs-lookup"><span data-stu-id="f373f-158">In the Work template field, type a value.</span></span>
5. <span data-ttu-id="f373f-159">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f373f-159">Click Save.</span></span>
6. <span data-ttu-id="f373f-160">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f373f-160">Click New.</span></span>
7. <span data-ttu-id="f373f-161">Velg Plukk i Arbeidstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="f373f-161">In the Work type field, select 'Pick'.</span></span>
8. <span data-ttu-id="f373f-162">Angi eller velg en verdi i feltet Arbeidsklasse-ID.</span><span class="sxs-lookup"><span data-stu-id="f373f-162">In the Work class ID field, enter or select a value.</span></span>
    * <span data-ttu-id="f373f-163">Dette bør være en arbeidsklasse relatert til etterfylling.</span><span class="sxs-lookup"><span data-stu-id="f373f-163">This should be a work class related to replenishment.</span></span> <span data-ttu-id="f373f-164">Hvis du bruker USMF, velger du Etterfylle.</span><span class="sxs-lookup"><span data-stu-id="f373f-164">If you’re using USMF, select Replenish.</span></span>  
9. <span data-ttu-id="f373f-165">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f373f-165">Click New.</span></span>
10. <span data-ttu-id="f373f-166">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f373f-166">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="f373f-167">Velg Plasser i Arbeidstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="f373f-167">In the Work type field, select 'Put'.</span></span>
12. <span data-ttu-id="f373f-168">Angi eller velg en verdi i feltet Arbeidsklasse-ID.</span><span class="sxs-lookup"><span data-stu-id="f373f-168">In the Work class ID field, enter or select a value.</span></span>
13. <span data-ttu-id="f373f-169">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f373f-169">Click Save.</span></span>
14. <span data-ttu-id="f373f-170">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f373f-170">Close the page.</span></span>

## <a name="create-a-new-replenishment-template"></a><span data-ttu-id="f373f-171">Opprette en ny etterfyllingsmal</span><span class="sxs-lookup"><span data-stu-id="f373f-171">Create a new replenishment template</span></span>
1. <span data-ttu-id="f373f-172">Gå til Lagerstyring > Oppsett > Etterfylling > Etterfyllingsmaler.</span><span class="sxs-lookup"><span data-stu-id="f373f-172">Go to Warehouse management > Setup > Replenishment > Replenishment templates.</span></span>
    * <span data-ttu-id="f373f-173">Etterfyllingsmalen brukes til å definere varer og antall og lokasjonen som skal etterfylles.</span><span class="sxs-lookup"><span data-stu-id="f373f-173">The replenishment template is used to define the items and quantities, and the location to replenish.</span></span>  
2. <span data-ttu-id="f373f-174">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f373f-174">Click New.</span></span>
3. <span data-ttu-id="f373f-175">Angi en verdi i feltet Etterfyll.</span><span class="sxs-lookup"><span data-stu-id="f373f-175">In the Replenish template field, type a value.</span></span>
    * <span data-ttu-id="f373f-176">Gi malen et navn for å angi at den er for minimums-/maksimumsetterfylling.</span><span class="sxs-lookup"><span data-stu-id="f373f-176">Give the template a name to indicate that it’s for min/max replenishment.</span></span>  
4. <span data-ttu-id="f373f-177">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f373f-177">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f373f-178">Merk av for Tillat at bølgebehov kan bruke ureserverte antall.</span><span class="sxs-lookup"><span data-stu-id="f373f-178">Select the Allow wave demand to use unreserved quantities check box.</span></span>
    * <span data-ttu-id="f373f-179">Hvis du velger dette alternativet, gir det mulighet for etterfylling for bølgebehov antallene som er relatert til minimums-/maksimumsetterfylling.</span><span class="sxs-lookup"><span data-stu-id="f373f-179">If you select this option, it enables wave demand replenishment to consume quantities that are related to min/max replenishment.</span></span> <span data-ttu-id="f373f-180">Dette kan for eksempel være nyttig hvis arbeidet for minimums-/maksimumsetterfylling ikke behandles umiddelbart, slik at du unngår oppretting av unødvendige arbeid for behovsetterfylling.</span><span class="sxs-lookup"><span data-stu-id="f373f-180">For example, this might be useful if the min/max replenishment work isn’t processed immediately, to avoid unnecessary demand replenishment work from being created.</span></span>  
6. <span data-ttu-id="f373f-181">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f373f-181">Click New.</span></span>
7. <span data-ttu-id="f373f-182">Angi et nummer i Sekvensnummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="f373f-182">In the Sequence number field, enter a number.</span></span>
8. <span data-ttu-id="f373f-183">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f373f-183">In the Description field, type a value.</span></span>
9. <span data-ttu-id="f373f-184">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f373f-184">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="f373f-185">Angi eller velg en verdi i feltet Etterfylling.</span><span class="sxs-lookup"><span data-stu-id="f373f-185">In the Replenishment unit field, enter or select a value.</span></span>
    * <span data-ttu-id="f373f-186">Velg for eksempel stk.</span><span class="sxs-lookup"><span data-stu-id="f373f-186">For example, select pcs.</span></span> <span data-ttu-id="f373f-187">Denne innstillingen er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f373f-187">This setting is mandatory.</span></span> <span data-ttu-id="f373f-188">Den lar deg angi en annen målenhet for etterfyllingsarbeid sammenlignet med enheten som er angitt for de minste og største lagernivåene i denne malen.</span><span class="sxs-lookup"><span data-stu-id="f373f-188">It allows you to specify a different unit of measurement for replenishment work compared to the unit specified for the minimum and maximum stock levels in this template.</span></span>  
11. <span data-ttu-id="f373f-189">Angi eller velg en verdi i feltet Arbeidsmal.</span><span class="sxs-lookup"><span data-stu-id="f373f-189">In the Work template field, enter or select a value.</span></span>
    * <span data-ttu-id="f373f-190">Velg arbeidsmalen du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="f373f-190">Choose the work template that you created earlier.</span></span>  
12. <span data-ttu-id="f373f-191">Angi et tall i feltet Minimumsantall.</span><span class="sxs-lookup"><span data-stu-id="f373f-191">In the Minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="f373f-192">Velg det minste antallet som skal utløse etterfyllingen.</span><span class="sxs-lookup"><span data-stu-id="f373f-192">Select the minimum quantity that should trigger the replenishment.</span></span> <span data-ttu-id="f373f-193">Sett det for eksempel til 50.</span><span class="sxs-lookup"><span data-stu-id="f373f-193">For example, set this to 50.</span></span> <span data-ttu-id="f373f-194">Det er mulig å la det være satt til null hvis du etterfyller en fast plassering og alternativet Etterfyll tomme faste lokasjoner er satt til Ja.</span><span class="sxs-lookup"><span data-stu-id="f373f-194">It is possible to leave this set to zero, if you’re replenishing a fixed location and the Replenish empty fixed locations option is set to Yes.</span></span> <span data-ttu-id="f373f-195">Vi anbefaler også at du velger alternativet Etterfyll tomme faste lokasjoner med hensyn til ytelsen.</span><span class="sxs-lookup"><span data-stu-id="f373f-195">We also recommend that you select the Replenish only fixed locations option for performance reasons.</span></span>  
13. <span data-ttu-id="f373f-196">Angi et tall i feltet Maksimumsantall.</span><span class="sxs-lookup"><span data-stu-id="f373f-196">In the Maximum quantity field, enter a number.</span></span>
    * <span data-ttu-id="f373f-197">Sett det for eksempel til 100.</span><span class="sxs-lookup"><span data-stu-id="f373f-197">For example, set this to 100.</span></span>  
14. <span data-ttu-id="f373f-198">Angi eller velg en verdi i Enhet-feltet.</span><span class="sxs-lookup"><span data-stu-id="f373f-198">In the Unit field, enter or select a value.</span></span>
    * <span data-ttu-id="f373f-199">Tilordne enheten for minimums- og maksimumsantall.</span><span class="sxs-lookup"><span data-stu-id="f373f-199">Assign the unit for the minimum and maximum quantities.</span></span> <span data-ttu-id="f373f-200">Sett det for eksempel til stk.</span><span class="sxs-lookup"><span data-stu-id="f373f-200">For example, set this to pcs.</span></span>  
15. <span data-ttu-id="f373f-201">Merk av for Etterfyll tomme faste lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="f373f-201">Select the Replenish empty fixed locations check box.</span></span>
    * <span data-ttu-id="f373f-202">Velg dette alternativet for å etterfylle faste lokasjoner når de er tomme.</span><span class="sxs-lookup"><span data-stu-id="f373f-202">Select this check box to replenish fixed locations when they are empty.</span></span> <span data-ttu-id="f373f-203">Du kan eventuelt bare lokasjonene der det er et antall på lager som skal etterfylles.</span><span class="sxs-lookup"><span data-stu-id="f373f-203">Otherwise, only the locations where there is a quantity on hand will be replenished.</span></span>  
16. <span data-ttu-id="f373f-204">Merk av for Etterfyll bare faste lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="f373f-204">Select the Replenish only fixed locations check box.</span></span>
17. <span data-ttu-id="f373f-205">Klikk Velg produkter.</span><span class="sxs-lookup"><span data-stu-id="f373f-205">Click Select products.</span></span>
    * <span data-ttu-id="f373f-206">Dette er stedet der du kan definere hvilke produkter som skal etterfylles.</span><span class="sxs-lookup"><span data-stu-id="f373f-206">This is the place to define which products should be replenished.</span></span> <span data-ttu-id="f373f-207">Hvis det er merket av for alternativet Faste plukklokasjoner, må du også definere lokasjonene i denne spørringen.</span><span class="sxs-lookup"><span data-stu-id="f373f-207">If the Fixed picking locations option is selected, you also need to define the locations in this query.</span></span> <span data-ttu-id="f373f-208">Variantspesifikke og produktspesifikke spørringer er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="f373f-208">Variant-specific queries are available as well product-specific queries.</span></span>  
18. <span data-ttu-id="f373f-209">Velg raden Varer.</span><span class="sxs-lookup"><span data-stu-id="f373f-209">Select the Items row.</span></span>
19. <span data-ttu-id="f373f-210">Skriv inn en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="f373f-210">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="f373f-211">Velg varene som skal etterfylles på de faste lokasjonene.</span><span class="sxs-lookup"><span data-stu-id="f373f-211">Select the items that should be replenished at the fixed locations.</span></span> <span data-ttu-id="f373f-212">Skriv for eksempel inn A\* for å velge alle varenumre som begynner med A.</span><span class="sxs-lookup"><span data-stu-id="f373f-212">For example, type A\* to select all item numbers beginning with A.</span></span>  
20. <span data-ttu-id="f373f-213">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="f373f-213">Click Add.</span></span>
    * <span data-ttu-id="f373f-214">Legg til enhetslokasjonen (med mindre den allerede finnes) for å kunne begrense etterfyllingsarbeidet til de faste plukklokasjonene innenfor et bestemt område i lageret.</span><span class="sxs-lookup"><span data-stu-id="f373f-214">Add the Location entity (unless it already exists) to be able to restrict the replenishment work to the fixed picking locations within a specific area of the warehouse.</span></span>  
21. <span data-ttu-id="f373f-215">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f373f-215">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="f373f-216">Sett Tabell-feltet til Lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="f373f-216">Set the Table field to Locations.</span></span>
23. <span data-ttu-id="f373f-217">Velg lokasjonsprofil-ID i feltet Felt.</span><span class="sxs-lookup"><span data-stu-id="f373f-217">In the Field field, select Location profile ID.</span></span>
24. <span data-ttu-id="f373f-218">Angi eller velg en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="f373f-218">In the Criteria field, enter or select a value.</span></span>
25. <span data-ttu-id="f373f-219">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f373f-219">Click OK.</span></span>
26. <span data-ttu-id="f373f-220">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f373f-220">Close the page.</span></span>

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a><span data-ttu-id="f373f-221">Angi at etterfyllingsprosessen skal kjøres som en satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="f373f-221">Set the replenishment process to run as a batch job</span></span>
1. <span data-ttu-id="f373f-222">Gå til Lagerstyring > Etterfylling > Etterfyllinger.</span><span class="sxs-lookup"><span data-stu-id="f373f-222">Go to Warehouse management > Replenishment > Replenishments.</span></span>
    * <span data-ttu-id="f373f-223">Siden Etterfyllinger lar deg definere etterfylling som skal kjøres som en satsvis jobb, eller å kreve at den startes manuelt.</span><span class="sxs-lookup"><span data-stu-id="f373f-223">The Replenishments page allows you to set up replenishment to run as a batch job, or to require that it’s started manually.</span></span>  
2. <span data-ttu-id="f373f-224">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="f373f-224">Click Filter.</span></span>
3. <span data-ttu-id="f373f-225">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f373f-225">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f373f-226">Angi eller velg en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="f373f-226">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="f373f-227">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f373f-227">Click OK.</span></span>
6. <span data-ttu-id="f373f-228">Utvid Kjør i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="f373f-228">Expand the Run in the background section.</span></span>
7. <span data-ttu-id="f373f-229">Sett alternativet Satsvis behandling til Ja.</span><span class="sxs-lookup"><span data-stu-id="f373f-229">Set the Batch processing option to Yes.</span></span>
8. <span data-ttu-id="f373f-230">Klikk Regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="f373f-230">Click Recurrence.</span></span>
9. <span data-ttu-id="f373f-231">Velg Ingen sluttdato.</span><span class="sxs-lookup"><span data-stu-id="f373f-231">Select the No end date option.</span></span>
10. <span data-ttu-id="f373f-232">Sett mønsteret for regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="f373f-232">Set the Recurrence pattern.</span></span>
    * <span data-ttu-id="f373f-233">Velg for eksempel Dager.</span><span class="sxs-lookup"><span data-stu-id="f373f-233">For example, select Days.</span></span>  
11. <span data-ttu-id="f373f-234">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f373f-234">Click OK.</span></span>
12. <span data-ttu-id="f373f-235">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f373f-235">Click OK.</span></span>


