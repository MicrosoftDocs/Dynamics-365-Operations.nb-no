--- 
title: Opprette en produksjonsflytversjon
description: "Denne prosedyren fokuserer på å opprette en ny produksjonsflytversjon."
author: cvocph
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 58b3c9cd265b97a814541315e4ba8378010eb2b2
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-production-flow-version"></a><span data-ttu-id="c78e4-103">Opprette en produksjonsflytversjon</span><span class="sxs-lookup"><span data-stu-id="c78e4-103">Create a production flow version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c78e4-104">Denne prosedyren fokuserer på å opprette en ny produksjonsflytversjon.</span><span class="sxs-lookup"><span data-stu-id="c78e4-104">This procedure focuses on creating a new production flow version.</span></span> <span data-ttu-id="c78e4-105">For denne prosedyren må produksjonsparameterne for lean manufacturing og måleenheter for klassen Tid defineres.</span><span class="sxs-lookup"><span data-stu-id="c78e4-105">For this procedure, the production parameters for lean manufacturing and the units of measurement for class time must be defined.</span></span> <span data-ttu-id="c78e4-106">Du må også definere en verdistrøm og en produksjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c78e4-106">You also need to define a value stream and a production group.</span></span> <span data-ttu-id="c78e4-107">Hvis du vil vite mer om produksjonsflyter og aktiviteter i lean manufacturing, kan du se i hvitebøkene om Lean manufacturing for Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="c78e4-107">To learn more about production flows and activities in lean manufacturing, see the white papers on Lean manufacturing for Microsoft Dynamics AX.</span></span> <span data-ttu-id="c78e4-108">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="c78e4-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="c78e4-109">Opprette en produksjonsflyt</span><span class="sxs-lookup"><span data-stu-id="c78e4-109">Create a production flow</span></span>
1. <span data-ttu-id="c78e4-110">Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.</span><span class="sxs-lookup"><span data-stu-id="c78e4-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="c78e4-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c78e4-111">Click New.</span></span>
3. <span data-ttu-id="c78e4-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="c78e4-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c78e4-113">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="c78e4-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c78e4-114">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="c78e4-114">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c78e4-115">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c78e4-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c78e4-116">Velg en driftsenhet av typen verdistrøm.</span><span class="sxs-lookup"><span data-stu-id="c78e4-116">Select an operating unit of type value stream.</span></span> <span data-ttu-id="c78e4-117">En verdistrøm er en driftsenhet som strekker seg over alle aktiviteter og flyter for verdistrømmen.</span><span class="sxs-lookup"><span data-stu-id="c78e4-117">A value stream is an operating unit that spans all activities and flows of the value stream.</span></span> <span data-ttu-id="c78e4-118">På dette stadiet er driftsenhetene begrenset til en juridisk enhet og har ingen ytterligere funksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="c78e4-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="c78e4-119">Klikk rullegardinknappen i feltet Produksjonsgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="c78e4-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="c78e4-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c78e4-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c78e4-121">Velg en produksjonsgruppe for produksjonsflyten.</span><span class="sxs-lookup"><span data-stu-id="c78e4-121">Select a production group for the production flow.</span></span> <span data-ttu-id="c78e4-122">Produksjonsgrupper gjør det mulig å definere materialer, arbeid og VIA-kontoer for en produksjonsprosess.</span><span class="sxs-lookup"><span data-stu-id="c78e4-122">Production groups allow the definition of material, labour, and WIP accounts for a production process.</span></span> <span data-ttu-id="c78e4-123">Hvis du vil knytte regnskapskonteksten til en produksjonsflyt, må du velge en produksjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c78e4-123">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="c78e4-124">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c78e4-124">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="c78e4-125">Opprette en produksjonsflytversjon</span><span class="sxs-lookup"><span data-stu-id="c78e4-125">Create a production flow version</span></span>
1. <span data-ttu-id="c78e4-126">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="c78e4-126">Click Add.</span></span>
2. <span data-ttu-id="c78e4-127">Angi dato og klokkeslett i feltet Utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="c78e4-127">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="c78e4-128">Om nødvendig kan du definere en utløpsdato for versjonen.</span><span class="sxs-lookup"><span data-stu-id="c78e4-128">If required, define an Expiration date for the version.</span></span> <span data-ttu-id="c78e4-129">Du kan oppdatere den når som helst, selv for aktive versjoner.</span><span class="sxs-lookup"><span data-stu-id="c78e4-129">You can update it at any given time, even for active versions.</span></span> <span data-ttu-id="c78e4-130">Du kan bruke den til å planlegge å fase ut en versjon.</span><span class="sxs-lookup"><span data-stu-id="c78e4-130">You can use it to plan to phase out a version.</span></span>  
3. <span data-ttu-id="c78e4-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c78e4-131">Click OK.</span></span>
4. <span data-ttu-id="c78e4-132">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c78e4-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="c78e4-133">Skriv inn en verdi i feltet Enhet.</span><span class="sxs-lookup"><span data-stu-id="c78e4-133">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="c78e4-134">ResolveChanges taktenheten.</span><span class="sxs-lookup"><span data-stu-id="c78e4-134">ResolveChanges the Takt unit.</span></span>
7. <span data-ttu-id="c78e4-135">Angi et nummer i feltet Gjennomsnittlig takttid.</span><span class="sxs-lookup"><span data-stu-id="c78e4-135">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="c78e4-136">Definer gjennomsnittlig takttid for versjonen.</span><span class="sxs-lookup"><span data-stu-id="c78e4-136">Define the Average takt time of the version.</span></span> <span data-ttu-id="c78e4-137">Definer en målrettet gjennomsnittlig takttid for taktkontrollen for produksjonsflytversjonen.</span><span class="sxs-lookup"><span data-stu-id="c78e4-137">For the takt control of the production flow version, define a targeted average takt time.</span></span> <span data-ttu-id="c78e4-138">Takten defineres som antall per tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="c78e4-138">The takt is defined as quantity per time period.</span></span> <span data-ttu-id="c78e4-139">I eksemplet er takttiden 0,2 timer per 10 stykker.</span><span class="sxs-lookup"><span data-stu-id="c78e4-139">In the example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="c78e4-140">For en arbeidstid på 8 timer tilsvarer dette en daglig produksjonskapasitet på 400 stykker.</span><span class="sxs-lookup"><span data-stu-id="c78e4-140">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="c78e4-141">I feltet Antall per syklus angir du et tall.</span><span class="sxs-lookup"><span data-stu-id="c78e4-141">In the Quantity per cycle field, enter a number.</span></span>
    * <span data-ttu-id="c78e4-142">Definer antall per syklus knyttet til den gjennomsnittlige takttiden.</span><span class="sxs-lookup"><span data-stu-id="c78e4-142">Define the quantity per cycle related to the Average takt time.</span></span>  
9. <span data-ttu-id="c78e4-143">Aktiver/deaktiver utvidelsen av delen Versjonsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="c78e4-143">Toggle the expansion of the Version details section.</span></span>
10. <span data-ttu-id="c78e4-144">Angi et nummer i feltet Minste takttid.</span><span class="sxs-lookup"><span data-stu-id="c78e4-144">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="c78e4-145">Definer den minste takttiden.</span><span class="sxs-lookup"><span data-stu-id="c78e4-145">Define the minimum takt time.</span></span> <span data-ttu-id="c78e4-146">Minste takttid må være mindre enn eller lik den gjennomsnittlige takttiden.</span><span class="sxs-lookup"><span data-stu-id="c78e4-146">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="c78e4-147">Angi et nummer i feltet Største takttid.</span><span class="sxs-lookup"><span data-stu-id="c78e4-147">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="c78e4-148">Største takttid må være større enn eller lik den gjennomsnittlige takttiden.</span><span class="sxs-lookup"><span data-stu-id="c78e4-148">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="c78e4-149">Angi et tall i feltet Periode for faktisk syklustid (dager).</span><span class="sxs-lookup"><span data-stu-id="c78e4-149">In the Period for actual cycle time (days) field, enter a number.</span></span>
    * <span data-ttu-id="c78e4-150">Angi antall dager i perioden for faktisk syklustid.</span><span class="sxs-lookup"><span data-stu-id="c78e4-150">Enter the number of days in the Period for actual cycle time.</span></span> <span data-ttu-id="c78e4-151">Perioden for faktisk syklustid er antall dager jobber aggregeres fra det faktiske minuttet bakover for å beregne den faktiske syklustiden.</span><span class="sxs-lookup"><span data-stu-id="c78e4-151">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="c78e4-152">Verdien kan endres når som helst, og brukes bare for beregning av de faktiske syklustider.</span><span class="sxs-lookup"><span data-stu-id="c78e4-152">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="c78e4-153">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c78e4-153">Click Save.</span></span>


