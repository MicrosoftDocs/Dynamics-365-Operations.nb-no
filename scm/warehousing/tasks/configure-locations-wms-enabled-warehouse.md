--- 
title: Konfigurere lokasjoner i et WMS-aktivert lager
description: Denne veiledningen viser deg hvordan du konfigurerer lokasjonsoppsettet for et nytt WMS-aktivert lager (et lager som bruker avanserte lagerstyringsprosesser).
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1082c86361180db84bb2b5c0b8158816f76a219e
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a><span data-ttu-id="964c8-103">Konfigurere lokasjoner i et WMS-aktivert lager</span><span class="sxs-lookup"><span data-stu-id="964c8-103">Configure locations in a WMS-enabled warehouse</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="964c8-104">Denne veiledningen viser deg hvordan du konfigurerer lokasjonsoppsettet for et nytt WMS-aktivert lager (et lager som bruker avanserte lagerstyringsprosesser).</span><span class="sxs-lookup"><span data-stu-id="964c8-104">This guide shows you how to configure the location setup for a new WMS-enabled warehouse (a warehouse that uses advanced warehouse management processes).</span></span> <span data-ttu-id="964c8-105">Prosessen gjøres vanligvis av en lagersjef.</span><span class="sxs-lookup"><span data-stu-id="964c8-105">The process is typically done by a warehouse manager.</span></span> <span data-ttu-id="964c8-106">Du kan kjøre denne veiledningen i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="964c8-106">You can run this guide in demo data company USMF or on your own data.</span></span> <span data-ttu-id="964c8-107">En forutsetning er at du har konfigurert minst ett område.</span><span class="sxs-lookup"><span data-stu-id="964c8-107">A precondition is that you have at least one site configured.</span></span>


## <a name="create-a-new-warehouse"></a><span data-ttu-id="964c8-108">Opprette et nytt lager</span><span class="sxs-lookup"><span data-stu-id="964c8-108">Create a new warehouse</span></span>
1. <span data-ttu-id="964c8-109">Gå til Lagre.</span><span class="sxs-lookup"><span data-stu-id="964c8-109">Go to Warehouses.</span></span>
2. <span data-ttu-id="964c8-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="964c8-110">Click New.</span></span>
3. <span data-ttu-id="964c8-111">Skriv inn en verdi i Lager-feltet.</span><span class="sxs-lookup"><span data-stu-id="964c8-111">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="964c8-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="964c8-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="964c8-113">Skriv inn en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="964c8-113">In the Site field, type a value.</span></span>
6. <span data-ttu-id="964c8-114">Vis eller skjul delen Lager.</span><span class="sxs-lookup"><span data-stu-id="964c8-114">Expand or collapse the Warehouse section.</span></span>
7. <span data-ttu-id="964c8-115">Angi alternativet Bruk lagerstyringsprosesser til Ja.</span><span class="sxs-lookup"><span data-stu-id="964c8-115">Set the Use warehouse management processes option to Yes.</span></span>
    * <span data-ttu-id="964c8-116">Denne innstillingen lar deg kjøre avanserte lagerprosesser som bruker lagerarbeid og mobilenheter.</span><span class="sxs-lookup"><span data-stu-id="964c8-116">This setting allows you to  run advanced warehousing processes using warehouse work and mobile devices.</span></span>  
8. <span data-ttu-id="964c8-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="964c8-117">Close the page.</span></span>

## <a name="define-a-location-format"></a><span data-ttu-id="964c8-118">Definere et lokasjonsformat</span><span class="sxs-lookup"><span data-stu-id="964c8-118">Define a location format</span></span>
1. <span data-ttu-id="964c8-119">Gå til Lokasjonsformater.</span><span class="sxs-lookup"><span data-stu-id="964c8-119">Go to Location formats.</span></span>
    * <span data-ttu-id="964c8-120">Lokasjonsformatene er et navngivningssystem som skal brukes til å opprette unike og konsekvente navn for de ulike lokasjonsboksposisjonene som brukes i et lager.</span><span class="sxs-lookup"><span data-stu-id="964c8-120">Location formats are a naming-system used to create unique and consistent names for the different location bin positions used within a warehouse.</span></span> <span data-ttu-id="964c8-121">Det kan være nyttig å bruke skilletegn som del av lokasjonsformatet for å gjøre det enklere å identifisere komponenter i lokasjonen for eksempel gangnummeret.</span><span class="sxs-lookup"><span data-stu-id="964c8-121">It can be useful to use separators as part of the location format to make it easier to identify components of the location such as the aisle number.</span></span> <span data-ttu-id="964c8-122">I dette eksemplet skal vi opprette et navn med fire komponenter.</span><span class="sxs-lookup"><span data-stu-id="964c8-122">In this example, we’ll create a name with four components.</span></span> <span data-ttu-id="964c8-123">Dette kan for eksempel være gang, reol, hylle og boks.</span><span class="sxs-lookup"><span data-stu-id="964c8-123">For example, these could be aisle, rack, shelf, and bin.</span></span>  
2. <span data-ttu-id="964c8-124">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="964c8-124">Click New.</span></span>
3. <span data-ttu-id="964c8-125">Skriv inn en verdi i feltet Lokasjonsformat.</span><span class="sxs-lookup"><span data-stu-id="964c8-125">In the Location format field, type a value.</span></span>
4. <span data-ttu-id="964c8-126">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="964c8-126">In the Name field, type a value.</span></span>
5. <span data-ttu-id="964c8-127">Skriv inn en verdi i Segmentbeskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="964c8-127">In the Segment description field, type a value.</span></span>
    * <span data-ttu-id="964c8-128">Dette beskriver hva den første delen av lokasjonsnavnet representerer.</span><span class="sxs-lookup"><span data-stu-id="964c8-128">This describes what the first component of the location name represents.</span></span> <span data-ttu-id="964c8-129">Det kan for eksempel være Gang.</span><span class="sxs-lookup"><span data-stu-id="964c8-129">For example, it could be Aisle.</span></span>  
6. <span data-ttu-id="964c8-130">Angi et tall i feltet Lengde.</span><span class="sxs-lookup"><span data-stu-id="964c8-130">In the Length field, enter a number.</span></span>
    * <span data-ttu-id="964c8-131">Dette bestemmer hvor mange tegn denne delen av lokasjonsnavnet må ha.</span><span class="sxs-lookup"><span data-stu-id="964c8-131">This determines how many characters this part of the location name must have.</span></span> <span data-ttu-id="964c8-132">Legg merke til at summen av alle komponenter i navnet, inkludert skilletegnene, ikke kan overskride 10 tegn.</span><span class="sxs-lookup"><span data-stu-id="964c8-132">Note that the total of all components in the name, including the separators, cannot exceed 10 characters.</span></span>  
7. <span data-ttu-id="964c8-133">Skriv inn en verdi i feltet Skilletegn.</span><span class="sxs-lookup"><span data-stu-id="964c8-133">In the Separator field, type a value.</span></span>
    * <span data-ttu-id="964c8-134">Dette bestemmer hvilket tegn eller symbol som brukes mellom første og andre komponent av navnet.</span><span class="sxs-lookup"><span data-stu-id="964c8-134">This determines which character or symbol is used between the first and second component of the name.</span></span>  
8. <span data-ttu-id="964c8-135">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="964c8-135">Click New.</span></span>
9. <span data-ttu-id="964c8-136">Skriv inn en verdi i Segmentbeskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="964c8-136">In the Segment description field, type a value.</span></span>
10. <span data-ttu-id="964c8-137">Angi et tall i feltet Lengde.</span><span class="sxs-lookup"><span data-stu-id="964c8-137">In the Length field, enter a number.</span></span>
11. <span data-ttu-id="964c8-138">Skriv inn en verdi i feltet Skilletegn.</span><span class="sxs-lookup"><span data-stu-id="964c8-138">In the Separator field, type a value.</span></span>
12. <span data-ttu-id="964c8-139">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="964c8-139">Click New.</span></span>
13. <span data-ttu-id="964c8-140">Skriv inn en verdi i Segmentbeskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="964c8-140">In the Segment description field, type a value.</span></span>
14. <span data-ttu-id="964c8-141">Angi et tall i feltet Lengde.</span><span class="sxs-lookup"><span data-stu-id="964c8-141">In the Length field, enter a number.</span></span>
15. <span data-ttu-id="964c8-142">Skriv inn en verdi i feltet Skilletegn.</span><span class="sxs-lookup"><span data-stu-id="964c8-142">In the Separator field, type a value.</span></span>
16. <span data-ttu-id="964c8-143">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="964c8-143">Click New.</span></span>
17. <span data-ttu-id="964c8-144">Skriv inn en verdi i Segmentbeskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="964c8-144">In the Segment description field, type a value.</span></span>
18. <span data-ttu-id="964c8-145">Angi et tall i feltet Lengde.</span><span class="sxs-lookup"><span data-stu-id="964c8-145">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="964c8-146">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="964c8-146">Click Save.</span></span>
20. <span data-ttu-id="964c8-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="964c8-147">Close the page.</span></span>

## <a name="define-location-types"></a><span data-ttu-id="964c8-148">Definere lokasjonstyper</span><span class="sxs-lookup"><span data-stu-id="964c8-148">Define location types</span></span>
1. <span data-ttu-id="964c8-149">Gå til Lokasjonstyper.</span><span class="sxs-lookup"><span data-stu-id="964c8-149">Go to Location types.</span></span>
    * <span data-ttu-id="964c8-150">Lokasjonstyper kan brukes som filtreringsalternativer for å styre de ulike lagerstyringsprosessene.</span><span class="sxs-lookup"><span data-stu-id="964c8-150">Location types can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="964c8-151">Som et minimum må du opprette typer for oppsamling og endelig levering for å definere den utgående lagerstyringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="964c8-151">As a minimum, you need to create staging and final shipping location types in order to define the outbound warehouse management process.</span></span>  
2. <span data-ttu-id="964c8-152">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="964c8-152">Click New.</span></span>
3. <span data-ttu-id="964c8-153">Skriv inn en verdi i feltet Lokasjonstype.</span><span class="sxs-lookup"><span data-stu-id="964c8-153">In the Location type field, type a value.</span></span>
4. <span data-ttu-id="964c8-154">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="964c8-154">In the Description field, type a value.</span></span>
5. <span data-ttu-id="964c8-155">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="964c8-155">Close the page.</span></span>

## <a name="define-location-profile"></a><span data-ttu-id="964c8-156">Definere lokasjonsprofil</span><span class="sxs-lookup"><span data-stu-id="964c8-156">Define location profile</span></span>
1. <span data-ttu-id="964c8-157">Gå til Lokasjonsprofiler.</span><span class="sxs-lookup"><span data-stu-id="964c8-157">Go to Location profiles.</span></span>
    * <span data-ttu-id="964c8-158">Definisjonen av lokasjonsprofiler er svært viktig.</span><span class="sxs-lookup"><span data-stu-id="964c8-158">The definition of location profiles is very important.</span></span> <span data-ttu-id="964c8-159">Gruppert lokasjonskapasitet kan kontrolleres her, i tillegg til policyene som gjelder hva beholdning skal lagre, og hvordan den lagres.</span><span class="sxs-lookup"><span data-stu-id="964c8-159">Grouped locations capacity can be controlled here, as well as the policies related to what inventory gets stored, and how it is stored.</span></span> <span data-ttu-id="964c8-160">Lokasjonsprofiler kan brukes som filtreringsalternativer for å styre de ulike lagerstyringsprosessene.</span><span class="sxs-lookup"><span data-stu-id="964c8-160">Location profiles can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="964c8-161">Som et minimum må du opprette en brukerlokasjonsprofil for å aktivere lagerstyringsprosesser.</span><span class="sxs-lookup"><span data-stu-id="964c8-161">As a minimum, you must create a user location profile in order to enable the warehouse management processes.</span></span>  
2. <span data-ttu-id="964c8-162">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="964c8-162">Click New.</span></span>
3. <span data-ttu-id="964c8-163">Skriv inn en verdi i feltet Profil-ID for lokasjon.</span><span class="sxs-lookup"><span data-stu-id="964c8-163">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="964c8-164">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="964c8-164">In the Name field, type a value.</span></span>
5. <span data-ttu-id="964c8-165">Klikk rullegardinknappen i feltet Lokasjonsformat for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="964c8-165">In the Location format field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="964c8-166">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-166">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="964c8-167">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-167">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="964c8-168">Klikk rullegardinknappen i feltet Lokasjonstype for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="964c8-168">In the Location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="964c8-169">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-169">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="964c8-170">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-170">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="964c8-171">Merk av eller fjern merket i boksen Tillat kombinerte lagerstatuser.</span><span class="sxs-lookup"><span data-stu-id="964c8-171">Select or clear the Allow mixed  inventory statuses check box.</span></span>
    * <span data-ttu-id="964c8-172">Aktiver dette alternativet hvis du vil tillate blandede lagerstatusverdier i lokasjoner som skal grupperes etter denne lokasjonsprofilen.</span><span class="sxs-lookup"><span data-stu-id="964c8-172">Enable this option if you want to allow mixed inventory status values in the locations that are going to be grouped by this location profile.</span></span>  
12. <span data-ttu-id="964c8-173">Merk av eller fjern merket i boksen Overstyr regler for partidager.</span><span class="sxs-lookup"><span data-stu-id="964c8-173">Select or clear the Override rules for batch days check box.</span></span>
    * <span data-ttu-id="964c8-174">Aktiver dette alternativet for å overstyre regelen for hvor mange dager utløpsdatoene for beholdningsparti kan være forskjellig, for å tillate blanding av lagerpartier som ikke overholder denne regelen.</span><span class="sxs-lookup"><span data-stu-id="964c8-174">Enable this option to override the rule for how many days the inventory batch expiration dates can differ, to allow mixing of inventory batches that don’t obeying this rule.</span></span>  
13. <span data-ttu-id="964c8-175">Merk av eller fjern merket i boksen Tillat syklustelling.</span><span class="sxs-lookup"><span data-stu-id="964c8-175">Select or clear the Allow cycle counting check box.</span></span>
    * <span data-ttu-id="964c8-176">Aktiver dette alternativet hvis du vil tillate syklustellingbehandling i alle lokasjoner som skal grupperes etter denne lokasjonsprofilen.</span><span class="sxs-lookup"><span data-stu-id="964c8-176">Enable this option to allow cycle counting processing in all the locations that are going to be grouped by this location profile.</span></span>  
14. <span data-ttu-id="964c8-177">Vis eller skjul delen Dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="964c8-177">Expand or collapse the Dimensions section.</span></span>
    * <span data-ttu-id="964c8-178">Med kategorien Dimensjoner kan du definere parametere og metoder for å aktivere nøyaktige beregninger av belastningskapasitet i hver enkelt lokasjon.</span><span class="sxs-lookup"><span data-stu-id="964c8-178">The Dimensions tab allows you to define parameters and methods to enable precise calculations of the load capacity within each of the locations.</span></span>  
15. <span data-ttu-id="964c8-179">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="964c8-179">Close the page.</span></span>

## <a name="enable-warehouse-management-parameters"></a><span data-ttu-id="964c8-180">Aktivere parametere for lagerstyring</span><span class="sxs-lookup"><span data-stu-id="964c8-180">Enable warehouse management parameters</span></span>
1. <span data-ttu-id="964c8-181">Gå til Lagerstyringsparametere.</span><span class="sxs-lookup"><span data-stu-id="964c8-181">Go to Warehouse management parameters.</span></span>
    * <span data-ttu-id="964c8-182">Hvis du skal kunne behandle lagerarbeid, må du angi parametere for brukerlokasjonsprofilen, oppsamlingslokasjonstypen og den endelige leveringslokasjonstypen. Så snart den utgående prosessen slutter ved den endelige forsendelseslokasjonstypen som du definerer, oppdateres de relaterte utgående transaksjonene til Plukket.</span><span class="sxs-lookup"><span data-stu-id="964c8-182">To be able to process warehouse work, you need to set parameters for the user location profile the staging location type, and the final shipping location type  As soon as the outbound process ends at the final shipping location type that you define, the related outbound transactions will be updated to ‘Picked’.</span></span>  
2. <span data-ttu-id="964c8-183">Vis eller skjul delen Lokasjonsprofiler.</span><span class="sxs-lookup"><span data-stu-id="964c8-183">Expand or collapse the Location profiles section.</span></span>
3. <span data-ttu-id="964c8-184">Klikk rullegardinknappen i feltet Brukerlokasjon for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="964c8-184">In the User location field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="964c8-185">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="964c8-186">Vis eller skjul delen Lokasjonstyper.</span><span class="sxs-lookup"><span data-stu-id="964c8-186">Expand or collapse the Location types section.</span></span>
6. <span data-ttu-id="964c8-187">Klikk rullegardinknappen i feltet Oppsamlingslokasjonstype for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="964c8-187">In the Staging location type field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="964c8-188">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-188">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="964c8-189">Klikk rullegardinknappen i feltet Endelig leveringslokasjonstype for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="964c8-189">In the Final shipping location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="964c8-190">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-190">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="964c8-191">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="964c8-191">Close the page.</span></span>

## <a name="define-warehouse-zone-groups"></a><span data-ttu-id="964c8-192">Definere lagersonegrupper</span><span class="sxs-lookup"><span data-stu-id="964c8-192">Define warehouse zone groups</span></span>
1. <span data-ttu-id="964c8-193">Gå til Lagersonegrupper.</span><span class="sxs-lookup"><span data-stu-id="964c8-193">Go to Warehouse zone groups.</span></span>
    * <span data-ttu-id="964c8-194">Lagersoner kan brukes som filtre for alternativer for å styre de ulike lagerstyringsprosessene.</span><span class="sxs-lookup"><span data-stu-id="964c8-194">Warehouse zones can be used as filters for options to control the different warehouse management processes.</span></span> <span data-ttu-id="964c8-195">Du må opprette en sonegruppe før du kan definere en sone.</span><span class="sxs-lookup"><span data-stu-id="964c8-195">You need to create a zone group before you can define a zone.</span></span>  
2. <span data-ttu-id="964c8-196">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="964c8-196">Click New.</span></span>
3. <span data-ttu-id="964c8-197">Skriv inn en verdi i feltet ID for sonegruppe.</span><span class="sxs-lookup"><span data-stu-id="964c8-197">In the Zone group ID field, type a value.</span></span>
4. <span data-ttu-id="964c8-198">Skriv inn en verdi i feltet Navn på sonegruppe.</span><span class="sxs-lookup"><span data-stu-id="964c8-198">In the Zone group name field, type a value.</span></span>
5. <span data-ttu-id="964c8-199">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="964c8-199">Close the page.</span></span>

## <a name="define-warehouse-zones"></a><span data-ttu-id="964c8-200">Definere lagersoner</span><span class="sxs-lookup"><span data-stu-id="964c8-200">Define Warehouse zones</span></span>
1. <span data-ttu-id="964c8-201">Gå til Soner.</span><span class="sxs-lookup"><span data-stu-id="964c8-201">Go to Zones.</span></span>
2. <span data-ttu-id="964c8-202">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="964c8-202">Click New.</span></span>
3. <span data-ttu-id="964c8-203">Skriv inn en verdi i feltet Sone-ID.</span><span class="sxs-lookup"><span data-stu-id="964c8-203">In the Zone ID field, type a value.</span></span>
4. <span data-ttu-id="964c8-204">Skriv inn en verdi i feltet Sonenavn.</span><span class="sxs-lookup"><span data-stu-id="964c8-204">In the Zone name field, type a value.</span></span>
5. <span data-ttu-id="964c8-205">Klikk rullegardinknappen i feltet ID for sonegruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="964c8-205">In the Zone group ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="964c8-206">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="964c8-207">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-207">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="964c8-208">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="964c8-208">Close the page.</span></span>

## <a name="create-locations-using-the-location-setup-wizard"></a><span data-ttu-id="964c8-209">Opprette lokasjoner ved hjelp av veiviseren for lokasjonsoppsett</span><span class="sxs-lookup"><span data-stu-id="964c8-209">Create locations using the Location setup wizard</span></span>
1. <span data-ttu-id="964c8-210">Gå til Veiviser for lokasjonsoppsett.</span><span class="sxs-lookup"><span data-stu-id="964c8-210">Go to Location setup wizard.</span></span>
2. <span data-ttu-id="964c8-211">Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="964c8-211">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="964c8-212">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-212">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="964c8-213">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-213">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="964c8-214">Klikk rullegardinknappen i feltet Sone-ID for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="964c8-214">In the Zone ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="964c8-215">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-215">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="964c8-216">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-216">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="964c8-217">Klikk rullegardinknappen i feltet Profil-ID for lokasjon for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="964c8-217">In the Location profile ID field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="964c8-218">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-218">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="964c8-219">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-219">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="964c8-220">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-220">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="964c8-221">Angi et tall i feltet Fra-nummer.</span><span class="sxs-lookup"><span data-stu-id="964c8-221">In the From number field, enter a number.</span></span>
    * <span data-ttu-id="964c8-222">Feltene Fra-nummer og Til-nummer definerer hvor mange lokasjoner som skal opprettes.</span><span class="sxs-lookup"><span data-stu-id="964c8-222">The From number and To number fields define how many locations will be created.</span></span> <span data-ttu-id="964c8-223">Hvis du for eksempel angir Fra-nummer 1 og Til-nummer 3 for alle fire linjer i lokasjonsformatet, opprettes 81 lokasjoner (3x3x3x3).</span><span class="sxs-lookup"><span data-stu-id="964c8-223">For example, if you set From number to 1 and To number to 3 for all four lines in the location format, 81 locations will be created (3x3x3x3).</span></span>  
13. <span data-ttu-id="964c8-224">Angi et tall i feltet Til-nummer.</span><span class="sxs-lookup"><span data-stu-id="964c8-224">In the To number field, enter a number.</span></span>
14. <span data-ttu-id="964c8-225">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-225">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="964c8-226">Angi et tall i feltet Fra-nummer.</span><span class="sxs-lookup"><span data-stu-id="964c8-226">In the From number field, enter a number.</span></span>
16. <span data-ttu-id="964c8-227">Angi et tall i feltet Til-nummer.</span><span class="sxs-lookup"><span data-stu-id="964c8-227">In the To number field, enter a number.</span></span>
17. <span data-ttu-id="964c8-228">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-228">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="964c8-229">Angi et tall i feltet Fra-nummer.</span><span class="sxs-lookup"><span data-stu-id="964c8-229">In the From number field, enter a number.</span></span>
19. <span data-ttu-id="964c8-230">Angi et tall i feltet Til-nummer.</span><span class="sxs-lookup"><span data-stu-id="964c8-230">In the To number field, enter a number.</span></span>
20. <span data-ttu-id="964c8-231">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-231">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="964c8-232">Angi et tall i feltet Fra-nummer.</span><span class="sxs-lookup"><span data-stu-id="964c8-232">In the From number field, enter a number.</span></span>
22. <span data-ttu-id="964c8-233">Angi et tall i feltet Til-nummer.</span><span class="sxs-lookup"><span data-stu-id="964c8-233">In the To number field, enter a number.</span></span>
23. <span data-ttu-id="964c8-234">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="964c8-234">Click Create.</span></span>

## <a name="create-locations-manually"></a><span data-ttu-id="964c8-235">Opprette lokasjoner manuelt</span><span class="sxs-lookup"><span data-stu-id="964c8-235">Create locations manually</span></span>
1. <span data-ttu-id="964c8-236">Gå til Lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="964c8-236">Go to Locations.</span></span>
    * <span data-ttu-id="964c8-237">Manuell opprettelse av lokasjoner i et lager kan gjøres enkelt.</span><span class="sxs-lookup"><span data-stu-id="964c8-237">Manually creation of locations within a warehouse can easily be done.</span></span> <span data-ttu-id="964c8-238">Lokasjonens navn og lokasjonsprofil-IDen er obligatoriske verdier.</span><span class="sxs-lookup"><span data-stu-id="964c8-238">The location name and the Location profile ID are mandatory values.</span></span>  
2. <span data-ttu-id="964c8-239">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="964c8-239">Click New.</span></span>
3. <span data-ttu-id="964c8-240">Skriv inn en verdi i Lager-feltet.</span><span class="sxs-lookup"><span data-stu-id="964c8-240">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="964c8-241">Skriv inn en verdi i feltet Lokasjon.</span><span class="sxs-lookup"><span data-stu-id="964c8-241">In the Location field, type a value.</span></span>
    * <span data-ttu-id="964c8-242">Vær oppmerksom på at du oppretter en ny lokasjon her, så du må skrive inn et nytt unikt navn, i stedet for å velge et eksisterende.</span><span class="sxs-lookup"><span data-stu-id="964c8-242">Note that you're creating a new location here, so you need to type a new unique name, rather than selecting an existing one.</span></span>  
5. <span data-ttu-id="964c8-243">Skriv inn en verdi i feltet Profil-ID for lokasjon.</span><span class="sxs-lookup"><span data-stu-id="964c8-243">In the Location profile ID field, type a value.</span></span>
6. <span data-ttu-id="964c8-244">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="964c8-244">Close the page.</span></span>

## <a name="define-pack-size-categories"></a><span data-ttu-id="964c8-245">Definere kategorier for pakkestørrelse</span><span class="sxs-lookup"><span data-stu-id="964c8-245">Define Pack size categories</span></span>
1. <span data-ttu-id="964c8-246">Gå til Kategorier for pakkestørrelse.</span><span class="sxs-lookup"><span data-stu-id="964c8-246">Go to Pack size categories.</span></span>
    * <span data-ttu-id="964c8-247">Kategorier for pakkestørrelse kan brukes til å gruppere varer med lignende fysiske pakkestørrelser.</span><span class="sxs-lookup"><span data-stu-id="964c8-247">Pack size categories can be used to group items that have similar physical packing sizes.</span></span> <span data-ttu-id="964c8-248">I dette eksemplet brukes pakkestørrelseskategorien til å styre kapasiteten ved plukklokasjoner i en bestemt sone i lageret.</span><span class="sxs-lookup"><span data-stu-id="964c8-248">In this example the pack size category will be used to control the capacity at the picking locations within a specific zone of the warehouse.</span></span> <span data-ttu-id="964c8-249">Vær oppmerksom på at pakkestørrelseskategori-ID må være tilordnet til frigitt produkt-enhet for å kunne brukes som en del av behandling av lagringsgrenser.</span><span class="sxs-lookup"><span data-stu-id="964c8-249">Please note that the pack size category ID must be assigned to the released product entity in order to be used as part of the stocking limits processing.</span></span>  
2. <span data-ttu-id="964c8-250">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="964c8-250">Click New.</span></span>
3. <span data-ttu-id="964c8-251">Skriv inn en verdi i feltet ID for kategori for pakkestørrelse.</span><span class="sxs-lookup"><span data-stu-id="964c8-251">In the Pack size category ID field, type a value.</span></span>
4. <span data-ttu-id="964c8-252">Skriv inn en verdi i feltet Navn på kategori for pakkestørrelse.</span><span class="sxs-lookup"><span data-stu-id="964c8-252">In the Pack size category name field, type a value.</span></span>
5. <span data-ttu-id="964c8-253">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="964c8-253">Close the page.</span></span>

## <a name="define-location-stocking-limits"></a><span data-ttu-id="964c8-254">Definere lagringsgrenser for lokasjon</span><span class="sxs-lookup"><span data-stu-id="964c8-254">Define location stocking limits</span></span>
1. <span data-ttu-id="964c8-255">Gå til Lokasjon – lagringsgrenser.</span><span class="sxs-lookup"><span data-stu-id="964c8-255">Go to Location stocking limits.</span></span>
    * <span data-ttu-id="964c8-256">Lokasjon – lagringsgrenser hjelper med å være sikker på at arbeidet ikke er opprettet for å be om at lageret skal plasseres på en lokasjon som ikke har den fysiske kapasiteten til å føre beholdningen.</span><span class="sxs-lookup"><span data-stu-id="964c8-256">Location stocking limits help to make sure that work isn't created to request that inventory to be put in a location that doesn't have the physical capacity to carry the inventory.</span></span>  
2. <span data-ttu-id="964c8-257">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="964c8-257">Click New.</span></span>
3. <span data-ttu-id="964c8-258">Skriv inn en verdi i Lager-feltet.</span><span class="sxs-lookup"><span data-stu-id="964c8-258">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="964c8-259">Skriv inn en verdi i feltet Profil-ID for lokasjon.</span><span class="sxs-lookup"><span data-stu-id="964c8-259">In the Location profile ID field, type a value.</span></span>
5. <span data-ttu-id="964c8-260">Skriv inn en verdi i feltet ID for kategori for pakkestørrelse.</span><span class="sxs-lookup"><span data-stu-id="964c8-260">In the Pack size category ID field, type a value.</span></span>
6. <span data-ttu-id="964c8-261">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="964c8-261">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="964c8-262">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="964c8-262">Click Save.</span></span>
8. <span data-ttu-id="964c8-263">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="964c8-263">Close the page.</span></span>

## <a name="define-fixed-picking-locations"></a><span data-ttu-id="964c8-264">Definere faste plukklokasjoner</span><span class="sxs-lookup"><span data-stu-id="964c8-264">Define fixed picking locations</span></span>
1. <span data-ttu-id="964c8-265">Gå til Faste lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="964c8-265">Go to Fixed locations.</span></span>
    * <span data-ttu-id="964c8-266">Du kan definere hvilke lokasjoner som skal brukes per produkt eller produktvariant.</span><span class="sxs-lookup"><span data-stu-id="964c8-266">You can define the locations to be used per product or per product variant.</span></span> <span data-ttu-id="964c8-267">Det er mulig å opprette flere faste lokasjoner for det samme produktet innenfor samme lager.</span><span class="sxs-lookup"><span data-stu-id="964c8-267">It is possible to create multiple fixed locations for the same product within the same warehouse.</span></span>  
2. <span data-ttu-id="964c8-268">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="964c8-268">Click New.</span></span>
3. <span data-ttu-id="964c8-269">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="964c8-269">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="964c8-270">Skriv inn en verdi i Lager-feltet.</span><span class="sxs-lookup"><span data-stu-id="964c8-270">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="964c8-271">Klikk rullegardinknappen i Lokasjon-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="964c8-271">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="964c8-272">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="964c8-272">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="964c8-273">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="964c8-273">Close the page.</span></span>


