--- 
title: Validere en produksjonsflyt og -versjon
description: "Denne fremgangsmåten viser hvordan du oppretter en ny produksjonsflyt og en første versjon for lean manufacturing."
author: ChristianRytt
manager: AnnBe
ms.date: 02/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 9087b0865dd7d22bcb9040631207f4fef2c82c06
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="validate-a-production-flow-and-version"></a><span data-ttu-id="13ccd-103">Validere en produksjonsflyt og -versjon</span><span class="sxs-lookup"><span data-stu-id="13ccd-103">Validate a production flow and version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="13ccd-104">Denne fremgangsmåten viser hvordan du oppretter en ny produksjonsflyt og en første versjon for lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="13ccd-104">This procedure shows how to create a new production flow and a first version for lean manufacturing.</span></span> <span data-ttu-id="13ccd-105">Forutsetninger: Produksjonsparameterne for lean manufacturing og enheter for klassen Tid må defineres.</span><span class="sxs-lookup"><span data-stu-id="13ccd-105">Prerequisites: The production parameters for Lean manufacturing and the units of measure for class time must be defined.</span></span> <span data-ttu-id="13ccd-106">Du må definere en verdistrøm og en produksjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="13ccd-106">You need to define a Value stream and a Production group.</span></span> <span data-ttu-id="13ccd-107">Se hvitebøkene for Lean manufacturing for å gjøre deg kjent med konseptene for produksjonsflyter og aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="13ccd-107">Refer to the white papers on Lean manufacturing to familiarize yourself with the concepts of production flows and activities.</span></span> <span data-ttu-id="13ccd-108">Denne fremgangsmåten refererer til den juridiske enheten USMF i demodataene.</span><span class="sxs-lookup"><span data-stu-id="13ccd-108">This procedure refers to the legal entity USMF in demo data.</span></span> <span data-ttu-id="13ccd-109">Forutsatt at den juridiske enheten er konfigurert for Lean manufacturing, kan imidlertid andre juridiske enheter brukes.</span><span class="sxs-lookup"><span data-stu-id="13ccd-109">However, assuming that the legal entity is configured for Lean manufacturing, other legal entities can be used.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="13ccd-110">Opprette en produksjonsflyt</span><span class="sxs-lookup"><span data-stu-id="13ccd-110">Create a production flow</span></span>
1. <span data-ttu-id="13ccd-111">Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.</span><span class="sxs-lookup"><span data-stu-id="13ccd-111">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="13ccd-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="13ccd-112">Click New.</span></span>
3. <span data-ttu-id="13ccd-113">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="13ccd-113">In the Name field, type a value.</span></span>
4. <span data-ttu-id="13ccd-114">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="13ccd-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="13ccd-115">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="13ccd-115">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="13ccd-116">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="13ccd-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="13ccd-117">En verdistrøm er en driftsenhet som strekker seg over alle aktiviteter og flyter for verdistrømmen.</span><span class="sxs-lookup"><span data-stu-id="13ccd-117">A value stream is an operating unit that spans over all activities and flows of the value stream.</span></span>   <span data-ttu-id="13ccd-118">På dette stadiet er driftsenhetene begrenset til en juridisk enhet og har ingen ytterligere funksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="13ccd-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="13ccd-119">Klikk rullegardinknappen i feltet Produksjonsgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="13ccd-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="13ccd-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="13ccd-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="13ccd-121">Produksjonsgrupper gjør det mulig å definere materialer, arbeid og VIA-kontoer for en produksjonsprosess.</span><span class="sxs-lookup"><span data-stu-id="13ccd-121">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="13ccd-122">Hvis du vil knytte regnskapskonteksten til en produksjonsflyt, må du velge en produksjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="13ccd-122">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="13ccd-123">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="13ccd-123">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="13ccd-124">Opprette en produksjonsflytversjon</span><span class="sxs-lookup"><span data-stu-id="13ccd-124">Create a production flow version</span></span>
1. <span data-ttu-id="13ccd-125">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="13ccd-125">Click Add.</span></span>
2. <span data-ttu-id="13ccd-126">Angi dato og klokkeslett i feltet Utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="13ccd-126">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="13ccd-127">Du kan oppdatere utløpsdatoen for versjonen på et gitt tidspunkt, selv for aktive versjoner.</span><span class="sxs-lookup"><span data-stu-id="13ccd-127">You can update the Expiration date of the version at any given time, even for active versions.</span></span> <span data-ttu-id="13ccd-128">Bruk utløpet for versjonen til å planlegge å fase ut en versjon.</span><span class="sxs-lookup"><span data-stu-id="13ccd-128">Use the expiration of the version to plan for a phase out of a version.</span></span>  
3. <span data-ttu-id="13ccd-129">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="13ccd-129">Click OK.</span></span>
4. <span data-ttu-id="13ccd-130">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="13ccd-130">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="13ccd-131">Skriv inn en verdi i feltet Enhet.</span><span class="sxs-lookup"><span data-stu-id="13ccd-131">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="13ccd-132">Velg taktenheten.</span><span class="sxs-lookup"><span data-stu-id="13ccd-132">Select the Takt unit.</span></span>
7. <span data-ttu-id="13ccd-133">Angi et nummer i feltet Gjennomsnittlig takttid.</span><span class="sxs-lookup"><span data-stu-id="13ccd-133">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="13ccd-134">Definer en målrettet gjennomsnittlig takttid for taktkontrollen for produksjonsflytversjonen.</span><span class="sxs-lookup"><span data-stu-id="13ccd-134">For the takt control of the production flow version, define a targeted average takt time.</span></span>   <span data-ttu-id="13ccd-135">Takten defineres som antall per tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="13ccd-135">The takt is defined as quantity  per time period.</span></span>  <span data-ttu-id="13ccd-136">I det gitte eksemplet er takttiden 0,2 timer per 10 stykker.</span><span class="sxs-lookup"><span data-stu-id="13ccd-136">In the given example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="13ccd-137">For en arbeidstid på 8 timer tilsvarer dette en daglig produksjonskapasitet på 400 stykker.</span><span class="sxs-lookup"><span data-stu-id="13ccd-137">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="13ccd-138">I feltet Antall per syklus angir du et tall.</span><span class="sxs-lookup"><span data-stu-id="13ccd-138">In the Quantity per cycle field, enter a number.</span></span>
9. <span data-ttu-id="13ccd-139">Vis eller skjul Versjonsdetaljer-delen.</span><span class="sxs-lookup"><span data-stu-id="13ccd-139">Expand or collapse the Version details section.</span></span>
10. <span data-ttu-id="13ccd-140">Angi et nummer i feltet Minste takttid.</span><span class="sxs-lookup"><span data-stu-id="13ccd-140">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="13ccd-141">Minste takttid må være mindre enn eller lik den gjennomsnittlige takttiden.</span><span class="sxs-lookup"><span data-stu-id="13ccd-141">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="13ccd-142">Angi et nummer i feltet Største takttid.</span><span class="sxs-lookup"><span data-stu-id="13ccd-142">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="13ccd-143">Største takttid må være større enn eller lik den gjennomsnittlige takttiden.</span><span class="sxs-lookup"><span data-stu-id="13ccd-143">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="13ccd-144">Angi et antall dager i perioden for faktisk syklustid</span><span class="sxs-lookup"><span data-stu-id="13ccd-144">Enter a number of days in the Period for actual cycle time</span></span>
    * <span data-ttu-id="13ccd-145">Perioden for faktisk syklustid er antall dager jobber aggregeres fra det faktiske minuttet bakover for å beregne den faktiske syklustiden.</span><span class="sxs-lookup"><span data-stu-id="13ccd-145">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="13ccd-146">Verdien kan endres når som helst, og brukes bare for beregning av de faktiske syklustider.</span><span class="sxs-lookup"><span data-stu-id="13ccd-146">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="13ccd-147">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="13ccd-147">Click Save.</span></span>


