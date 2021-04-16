---
title: Definere manuell pakking (februar 2016 og mai 2016)
description: Pakkeprosessen lar deg validere og pakke produkter i containere.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2843c42474fcd4afbbc2cd7753c0d06cfe467dbe
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810372"
---
# <a name="set-up-manual-packing-february-2016--may-2016"></a><span data-ttu-id="b1a26-103">Definere manuell pakking (februar 2016 og mai 2016)</span><span class="sxs-lookup"><span data-stu-id="b1a26-103">Set up manual packing (February 2016 & May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b1a26-104">Pakkeprosessen lar deg validere og pakke produkter i containere.</span><span class="sxs-lookup"><span data-stu-id="b1a26-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="b1a26-105">I denne prosessen plukker lagermedarbeidere varer fra lagerlokasjoner og flytter dem på en pakkestasjon der de kontrollerer vareantall og typer og tilordner dem til riktige containere.</span><span class="sxs-lookup"><span data-stu-id="b1a26-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="b1a26-106">Når en container er fullstendig pakket, kan de lukke den og flytte den til utleveringsportene, og produktene er klare til forsendelse.</span><span class="sxs-lookup"><span data-stu-id="b1a26-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="b1a26-107">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="b1a26-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="b1a26-108">Denne fremgangsmåten gjelder bare for februar 2016- og mai 2016-versjonen av Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="b1a26-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="b1a26-109">Konfigurer lokasjonsprofiler</span><span class="sxs-lookup"><span data-stu-id="b1a26-109">Set up location profiles</span></span>
1. <span data-ttu-id="b1a26-110">Gå til Lagerstyring > Oppsett > Lager > Lokasjonsprofiler.</span><span class="sxs-lookup"><span data-stu-id="b1a26-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="b1a26-111">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="b1a26-111">Click New.</span></span>
    * <span data-ttu-id="b1a26-112">Lokasjonsprofilen brukes for emballasjestasjoner og inneholder informasjon og regler for en lokasjon.</span><span class="sxs-lookup"><span data-stu-id="b1a26-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="b1a26-113">Skriv inn en verdi i feltet Profil-ID for lokasjon.</span><span class="sxs-lookup"><span data-stu-id="b1a26-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="b1a26-114">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="b1a26-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="b1a26-115">Angi eller velg en verdi i feltet Lokasjonsformat.</span><span class="sxs-lookup"><span data-stu-id="b1a26-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="b1a26-116">Angi eller velg en verdi i feltet Lokasjonstype.</span><span class="sxs-lookup"><span data-stu-id="b1a26-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="b1a26-117">Velg Ja i feltet Tillat kombinerte varer.</span><span class="sxs-lookup"><span data-stu-id="b1a26-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="b1a26-118">Velg Ja i feltet Tillat kombinerte lagerstatuser.</span><span class="sxs-lookup"><span data-stu-id="b1a26-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="b1a26-119">Velg Ja i feltet Overstyr regler for partidager.</span><span class="sxs-lookup"><span data-stu-id="b1a26-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="b1a26-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b1a26-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="b1a26-121">Definere lagerstyringsparametere</span><span class="sxs-lookup"><span data-stu-id="b1a26-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="b1a26-122">Gå til Lagerstyring > Oppsett > Lagerstyringsparametere.</span><span class="sxs-lookup"><span data-stu-id="b1a26-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="b1a26-123">Klikk på fanen Pakking.</span><span class="sxs-lookup"><span data-stu-id="b1a26-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="b1a26-124">Angi eller velg en verdi i feltet Profil-ID for emballasjelokasjoner.</span><span class="sxs-lookup"><span data-stu-id="b1a26-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="b1a26-125">Merk lokasjonsprofilen som du vil bruke til pakking.</span><span class="sxs-lookup"><span data-stu-id="b1a26-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="b1a26-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b1a26-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="b1a26-127">Definere containertyper</span><span class="sxs-lookup"><span data-stu-id="b1a26-127">Set up container types</span></span>
1. <span data-ttu-id="b1a26-128">Gå til Lagerstyring > Oppsett > Containere > Containertyper.</span><span class="sxs-lookup"><span data-stu-id="b1a26-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="b1a26-129">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="b1a26-129">Click New.</span></span>
    * <span data-ttu-id="b1a26-130">Du kan definere containertypene som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="b1a26-130">You can define the types of containers to use.</span></span> <span data-ttu-id="b1a26-131">Du kan angi de fysiske målene til containeren, inkludert taravekt, maksimumsvekt, maksimalt volum, lengde, bredde og vekt.</span><span class="sxs-lookup"><span data-stu-id="b1a26-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="b1a26-132">Attributtene er egendefinerte felt som lar deg legge til ekstra dimensjoner for containertypen.</span><span class="sxs-lookup"><span data-stu-id="b1a26-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="b1a26-133">Skriv inn en verdi i feltet Containertype.</span><span class="sxs-lookup"><span data-stu-id="b1a26-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="b1a26-134">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b1a26-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b1a26-135">Angi et tall i feltet Taravekt.</span><span class="sxs-lookup"><span data-stu-id="b1a26-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="b1a26-136">Angi et tall i feltet Maksimumsvekt.</span><span class="sxs-lookup"><span data-stu-id="b1a26-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="b1a26-137">Angi et tall i feltet Volum.</span><span class="sxs-lookup"><span data-stu-id="b1a26-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="b1a26-138">Angi et tall i feltet Lengde.</span><span class="sxs-lookup"><span data-stu-id="b1a26-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="b1a26-139">Angi et tall i feltet Bredde.</span><span class="sxs-lookup"><span data-stu-id="b1a26-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="b1a26-140">Angi et tall i feltet Høyde.</span><span class="sxs-lookup"><span data-stu-id="b1a26-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="b1a26-141">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="b1a26-141">Click Save.</span></span>
12. <span data-ttu-id="b1a26-142">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b1a26-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="b1a26-143">Definere pakkeprofiler</span><span class="sxs-lookup"><span data-stu-id="b1a26-143">Set up packing profiles</span></span>
1. <span data-ttu-id="b1a26-144">Gå til Lagerstyring > Oppsett > Pakking > Pakkeprofiler.</span><span class="sxs-lookup"><span data-stu-id="b1a26-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="b1a26-145">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="b1a26-145">Click New.</span></span>
3. <span data-ttu-id="b1a26-146">Skriv inn en verdi i feltet Pakkeprofil-ID.</span><span class="sxs-lookup"><span data-stu-id="b1a26-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="b1a26-147">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b1a26-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b1a26-148">Angi eller velg en verdi i feltet Containerlukkingsprofil.</span><span class="sxs-lookup"><span data-stu-id="b1a26-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="b1a26-149">En ID for containerlukkingsprofil er valgfri, og er standard containerlukkingsprofil for denne emballasjeprofilen.</span><span class="sxs-lookup"><span data-stu-id="b1a26-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="b1a26-150">Velg et alternativ i feltet Modus for container-ID.</span><span class="sxs-lookup"><span data-stu-id="b1a26-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="b1a26-151">Dette alternativet avgjør om en container-ID genereres automatisk når det opprettes en container eller hvis en container-ID opprettes manuelt.</span><span class="sxs-lookup"><span data-stu-id="b1a26-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="b1a26-152">Angi eller velg en verdi i feltet Containertype.</span><span class="sxs-lookup"><span data-stu-id="b1a26-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="b1a26-153">Containertypen brukes som standard når det opprettes en ny container.</span><span class="sxs-lookup"><span data-stu-id="b1a26-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="b1a26-154">Merk av for Opprett container automatisk ved containerlukking.</span><span class="sxs-lookup"><span data-stu-id="b1a26-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="b1a26-155">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="b1a26-155">Click Save.</span></span>
10. <span data-ttu-id="b1a26-156">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b1a26-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="b1a26-157">Definere containerlukkingsprofiler</span><span class="sxs-lookup"><span data-stu-id="b1a26-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="b1a26-158">Gå til Lagerstyring > Oppsett > Containere > Containerlukkingsprofiler.</span><span class="sxs-lookup"><span data-stu-id="b1a26-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="b1a26-159">Containerlukkingsprofil definerer hva som skjer når en container lukkes.</span><span class="sxs-lookup"><span data-stu-id="b1a26-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="b1a26-160">Du kan definere flere containerlukkingsprofiler.</span><span class="sxs-lookup"><span data-stu-id="b1a26-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="b1a26-161">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="b1a26-161">Click New.</span></span>
3. <span data-ttu-id="b1a26-162">Angi en verdi i feltet Containerlukkingsprofil-ID.</span><span class="sxs-lookup"><span data-stu-id="b1a26-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="b1a26-163">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b1a26-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b1a26-164">Velg et alternativ i feltet Manifest den.</span><span class="sxs-lookup"><span data-stu-id="b1a26-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="b1a26-165">Angi om manifestering skal skje når du containere lukkes eller ved bekreftelse av forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="b1a26-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="b1a26-166">Legg merke til at manifestering krever transportstyring.</span><span class="sxs-lookup"><span data-stu-id="b1a26-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="b1a26-167">Manifestering må implementeres i transportmotorer for at det skal fungere.</span><span class="sxs-lookup"><span data-stu-id="b1a26-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="b1a26-168">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="b1a26-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="b1a26-169">Angi eller velg en verdi i feltet Standardlokasjon for endelig forsendelse.</span><span class="sxs-lookup"><span data-stu-id="b1a26-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="b1a26-170">Dette blir lokasjonen der produkter flyttes til når containere lukkes.</span><span class="sxs-lookup"><span data-stu-id="b1a26-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="b1a26-171">Denne lokasjonen må ha en lokasjonsprofil som er definert for lagerparametere.</span><span class="sxs-lookup"><span data-stu-id="b1a26-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="b1a26-172">Angi eller velg en verdi i feltet Vektenhet.</span><span class="sxs-lookup"><span data-stu-id="b1a26-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="b1a26-173">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="b1a26-173">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]