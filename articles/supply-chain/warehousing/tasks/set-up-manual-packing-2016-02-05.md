--- 
title: Definere manuell pakking (bare februar og mai 2016)
description: Pakkeprosessen lar deg validere og pakke produkter i containere.
author: BibiSp
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 31b689b6c31563f24892525eed5911af3a35bd51
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-manual-packing-february--may-2016-only"></a><span data-ttu-id="940f0-103">Definere manuell pakking (bare februar og mai 2016)</span><span class="sxs-lookup"><span data-stu-id="940f0-103">Set up manual packing (February & May 2016 only)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="940f0-104">Pakkeprosessen lar deg validere og pakke produkter i containere.</span><span class="sxs-lookup"><span data-stu-id="940f0-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="940f0-105">I denne prosessen plukker lagermedarbeidere varer fra lagerlokasjoner og flytter dem på en pakkestasjon der de kontrollerer vareantall og typer og tilordner dem til riktige containere.</span><span class="sxs-lookup"><span data-stu-id="940f0-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="940f0-106">Når en container er fullstendig pakket, kan de lukke den og flytte den til utleveringsportene, og produktene er klare til forsendelse.</span><span class="sxs-lookup"><span data-stu-id="940f0-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="940f0-107">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="940f0-107">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="940f0-108">Konfigurer lokasjonsprofiler</span><span class="sxs-lookup"><span data-stu-id="940f0-108">Set up location profiles</span></span>
1. <span data-ttu-id="940f0-109">Gå til Lagerstyring > Oppsett > Lager > Lokasjonsprofiler.</span><span class="sxs-lookup"><span data-stu-id="940f0-109">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="940f0-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="940f0-110">Click New.</span></span>
    * <span data-ttu-id="940f0-111">Lokasjonsprofilen brukes for emballasjestasjoner og inneholder informasjon og regler for en lokasjon.</span><span class="sxs-lookup"><span data-stu-id="940f0-111">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="940f0-112">Skriv inn en verdi i feltet Profil-ID for lokasjon.</span><span class="sxs-lookup"><span data-stu-id="940f0-112">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="940f0-113">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="940f0-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="940f0-114">Angi eller velg en verdi i feltet Lokasjonsformat.</span><span class="sxs-lookup"><span data-stu-id="940f0-114">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="940f0-115">Angi eller velg en verdi i feltet Lokasjonstype.</span><span class="sxs-lookup"><span data-stu-id="940f0-115">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="940f0-116">Velg Ja i feltet Tillat kombinerte varer.</span><span class="sxs-lookup"><span data-stu-id="940f0-116">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="940f0-117">Velg Ja i feltet Tillat kombinerte lagerstatuser.</span><span class="sxs-lookup"><span data-stu-id="940f0-117">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="940f0-118">Velg Ja i feltet Overstyr regler for partidager.</span><span class="sxs-lookup"><span data-stu-id="940f0-118">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="940f0-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="940f0-119">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="940f0-120">Definere lagerstyringsparametere</span><span class="sxs-lookup"><span data-stu-id="940f0-120">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="940f0-121">Gå til Lagerstyring > Oppsett > Lagerstyringsparametere.</span><span class="sxs-lookup"><span data-stu-id="940f0-121">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="940f0-122">Klikk kategorien Pakking.</span><span class="sxs-lookup"><span data-stu-id="940f0-122">Click the Packing tab.</span></span>
3. <span data-ttu-id="940f0-123">Angi eller velg en verdi i feltet Profil-ID for emballasjelokasjoner.</span><span class="sxs-lookup"><span data-stu-id="940f0-123">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="940f0-124">Merk lokasjonsprofilen som du vil bruke til pakking.</span><span class="sxs-lookup"><span data-stu-id="940f0-124">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="940f0-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="940f0-125">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="940f0-126">Definere containertyper</span><span class="sxs-lookup"><span data-stu-id="940f0-126">Set up container types</span></span>
1. <span data-ttu-id="940f0-127">Gå til Lagerstyring > Oppsett > Containere > Containertyper.</span><span class="sxs-lookup"><span data-stu-id="940f0-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="940f0-128">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="940f0-128">Click New.</span></span>
    * <span data-ttu-id="940f0-129">Du kan definere containertypene som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="940f0-129">You can define the types of containers to use.</span></span> <span data-ttu-id="940f0-130">Du kan angi de fysiske målene til containeren, inkludert taravekt, maksimumsvekt, maksimalt volum, lengde, bredde og vekt.</span><span class="sxs-lookup"><span data-stu-id="940f0-130">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="940f0-131">Attributtene er egendefinerte felt som lar deg legge til ekstra dimensjoner for containertypen.</span><span class="sxs-lookup"><span data-stu-id="940f0-131">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="940f0-132">Skriv inn en verdi i feltet Containertype.</span><span class="sxs-lookup"><span data-stu-id="940f0-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="940f0-133">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="940f0-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="940f0-134">Angi et tall i feltet Taravekt.</span><span class="sxs-lookup"><span data-stu-id="940f0-134">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="940f0-135">Angi et tall i feltet Maksimumsvekt.</span><span class="sxs-lookup"><span data-stu-id="940f0-135">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="940f0-136">Angi et tall i feltet Volum.</span><span class="sxs-lookup"><span data-stu-id="940f0-136">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="940f0-137">Angi et tall i feltet Lengde.</span><span class="sxs-lookup"><span data-stu-id="940f0-137">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="940f0-138">Angi et tall i feltet Bredde.</span><span class="sxs-lookup"><span data-stu-id="940f0-138">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="940f0-139">Angi et tall i feltet Høyde.</span><span class="sxs-lookup"><span data-stu-id="940f0-139">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="940f0-140">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="940f0-140">Click Save.</span></span>
12. <span data-ttu-id="940f0-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="940f0-141">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="940f0-142">Definere pakkeprofiler</span><span class="sxs-lookup"><span data-stu-id="940f0-142">Set up packing profiles</span></span>
1. <span data-ttu-id="940f0-143">Gå til Lagerstyring > Oppsett > Pakking > Pakkeprofiler.</span><span class="sxs-lookup"><span data-stu-id="940f0-143">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="940f0-144">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="940f0-144">Click New.</span></span>
3. <span data-ttu-id="940f0-145">Skriv inn en verdi i feltet Pakkeprofil-ID.</span><span class="sxs-lookup"><span data-stu-id="940f0-145">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="940f0-146">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="940f0-146">In the Description field, type a value.</span></span>
5. <span data-ttu-id="940f0-147">Angi eller velg en verdi i feltet Containerlukkingsprofil.</span><span class="sxs-lookup"><span data-stu-id="940f0-147">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="940f0-148">En ID for containerlukkingsprofil er valgfri, og er standard containerlukkingsprofil for denne emballasjeprofilen.</span><span class="sxs-lookup"><span data-stu-id="940f0-148">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="940f0-149">Velg et alternativ i feltet Modus for container-ID.</span><span class="sxs-lookup"><span data-stu-id="940f0-149">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="940f0-150">Dette alternativet avgjør om en container-ID genereres automatisk når det opprettes en container eller hvis en container-ID opprettes manuelt.</span><span class="sxs-lookup"><span data-stu-id="940f0-150">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="940f0-151">Angi eller velg en verdi i feltet Containertype.</span><span class="sxs-lookup"><span data-stu-id="940f0-151">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="940f0-152">Containertypen brukes som standard når det opprettes en ny container.</span><span class="sxs-lookup"><span data-stu-id="940f0-152">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="940f0-153">Merk av for Opprett container automatisk ved containerlukking.</span><span class="sxs-lookup"><span data-stu-id="940f0-153">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="940f0-154">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="940f0-154">Click Save.</span></span>
10. <span data-ttu-id="940f0-155">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="940f0-155">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="940f0-156">Definere containerlukkingsprofiler</span><span class="sxs-lookup"><span data-stu-id="940f0-156">Set up container closing profiles</span></span>
1. <span data-ttu-id="940f0-157">Gå til Lagerstyring > Oppsett > Containere > Containerlukkingsprofiler.</span><span class="sxs-lookup"><span data-stu-id="940f0-157">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="940f0-158">Containerlukkingsprofil definerer hva som skjer når en container lukkes.</span><span class="sxs-lookup"><span data-stu-id="940f0-158">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="940f0-159">Du kan definere flere containerlukkingsprofiler.</span><span class="sxs-lookup"><span data-stu-id="940f0-159">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="940f0-160">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="940f0-160">Click New.</span></span>
3. <span data-ttu-id="940f0-161">Angi en verdi i feltet Containerlukkingsprofil-ID.</span><span class="sxs-lookup"><span data-stu-id="940f0-161">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="940f0-162">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="940f0-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="940f0-163">Velg et alternativ i feltet Manifest den.</span><span class="sxs-lookup"><span data-stu-id="940f0-163">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="940f0-164">Angi om manifestering skal skje når du containere lukkes eller ved bekreftelse av forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="940f0-164">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="940f0-165">Legg merke til at manifestering krever transportstyring.</span><span class="sxs-lookup"><span data-stu-id="940f0-165">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="940f0-166">Manifestering må implementeres i transportmotorer for at det skal fungere.</span><span class="sxs-lookup"><span data-stu-id="940f0-166">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="940f0-167">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="940f0-167">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="940f0-168">Angi eller velg en verdi i feltet Standardlokasjon for endelig forsendelse.</span><span class="sxs-lookup"><span data-stu-id="940f0-168">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="940f0-169">Dette blir lokasjonen der produkter flyttes til når containere lukkes.</span><span class="sxs-lookup"><span data-stu-id="940f0-169">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="940f0-170">Denne lokasjonen må ha en lokasjonsprofil som er definert for lagerparametere.</span><span class="sxs-lookup"><span data-stu-id="940f0-170">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="940f0-171">Angi eller velg en verdi i feltet Vektenhet.</span><span class="sxs-lookup"><span data-stu-id="940f0-171">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="940f0-172">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="940f0-172">Click Save.</span></span>


