---
title: Plasser til vegg – plasser til butikk
description: Dette emnet inneholder informasjon om funksjonen for Plasser til vegg – plasser til butikk. Med denne funksjonaliteten kan du håndtere scenarier der du må konsolidere et produkt i et oppsamlingsområde for forhåndspakker basert på konfigurerbare kriterier. Det bidrar til å redusere plukktiden fordi det tillater plukking til et enkelt målnummerskilt og kan bruke flere plasseringsposisjoner enn klyngeplukking.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3f2ae63758fcb6247c5e56433645d9252576c755
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996281"
---
# <a name="put-to-wall---put-to-store"></a><span data-ttu-id="3244c-105">Plasser til vegg – plasser til butikk</span><span class="sxs-lookup"><span data-stu-id="3244c-105">Put to wall - put to store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3244c-106">Funksjonen for *Plasser til vegg – plasser til butikk* kan håndtere scenarier der du må konsolidere et produkt i et oppsamlingsområde for forhåndspakker basert på konfigurerbare kriterier.</span><span class="sxs-lookup"><span data-stu-id="3244c-106">The *Put to wall - put to store* functionality lets you handle scenarios where you must consolidate a product to a prepack staging area, based on configurable criteria.</span></span> <span data-ttu-id="3244c-107">Fordi denne funksjonaliteten gjør det mulig å plukke til et enkelt målnummerskilt og bruke flere plasseringsstillinger enn klyngeplukking, vil firmaer som leverer til butikker eller behandler små varer, dra nytte av å redusere plukktiden.</span><span class="sxs-lookup"><span data-stu-id="3244c-107">Because this functionality allows for picking to a single target license plate and can use more put positions than cluster picking, companies that ship to stores or handle small items will benefit from decreased picking time.</span></span>

<span data-ttu-id="3244c-108">Arbeidsflyten for denne funksjonaliteten dirigerer plukket produkt til en sorteringslokasjon for distribusjon til forskjellige typer containere.</span><span class="sxs-lookup"><span data-stu-id="3244c-108">The workflow for this functionality directs picked product to a sorting location for distribution into various types of containers.</span></span> <span data-ttu-id="3244c-109">Vanligvis inneholder hver sorteringslokasjon flere sorteringsposisjoner.</span><span class="sxs-lookup"><span data-stu-id="3244c-109">Generally, each sorting location includes multiple sort positions.</span></span> <span data-ttu-id="3244c-110">Hver sorteringsposisjon tilordnes i henhold til kriteriene som er angitt av forretningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="3244c-110">Each sort position is assigned according to the criteria that are set by the business process.</span></span> <span data-ttu-id="3244c-111">Vanlige kriterier er det endelige målet, forsendelsen eller lasten.</span><span class="sxs-lookup"><span data-stu-id="3244c-111">Typical criteria are the final destination, shipment, or load.</span></span> <span data-ttu-id="3244c-112">Når et produkt mottas, distribueres det til hver sorteringsposisjon basert på antallet som er knyttet til ordren, målet, forsendelsen eller lasten.</span><span class="sxs-lookup"><span data-stu-id="3244c-112">After a product arrives, it's distributed to each sort position, based on the quantity that is associated with the order, destination, shipment, or load.</span></span> <span data-ttu-id="3244c-113">Når en container er full eller ferdig, flyttes den til en oppsamlingslokasjon eller en forsendelseslokasjon for videre behandling, avhengig av forretningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="3244c-113">When a container is full or complete, it's moved to a staging location or a shipping location for further handling, depending on the business process.</span></span>

<span data-ttu-id="3244c-114">Denne lagerfunksjonaliteten refereres også til med andre navn.</span><span class="sxs-lookup"><span data-stu-id="3244c-114">This warehousing functionality is also referred to by other names, such as put-to-light and break opens.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="3244c-115">Aktivere Utgående sortering-funksjonen</span><span class="sxs-lookup"><span data-stu-id="3244c-115">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="3244c-116">Før du kan bruke funksjonen for *Plasser til vegg – plasser til butikk*, må funksjonen *Utgående sortering* aktiveres på systemet.</span><span class="sxs-lookup"><span data-stu-id="3244c-116">Before you can use the *Put to wall - put to store* functionality, the *Outbound sorting* feature must be turned on in your system.</span></span> <span data-ttu-id="3244c-117">Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="3244c-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="3244c-118">Funksjonen vises på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="3244c-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="3244c-119">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="3244c-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="3244c-120">**Funksjonsnavn:** *Utgående sortering*</span><span class="sxs-lookup"><span data-stu-id="3244c-120">**Feature name:** *Outbound sorting*</span></span>

<span data-ttu-id="3244c-121">Funksjonen *Utgående sortering* kan brukes sammen med funksjonen *Organisasjonsomfattende bølgetrinnkode* hvis den er slått på.</span><span class="sxs-lookup"><span data-stu-id="3244c-121">The *Outbound sorting* feature can be used in conjunction with the *Organization wide wave step code* feature if it's turned on.</span></span> <span data-ttu-id="3244c-122">Du må også aktivere denne funksjonen hvis du vil bruke forhåndsdefinerte koder som er definert i bølgetrinnkoder.</span><span class="sxs-lookup"><span data-stu-id="3244c-122">You must also turn on this feature if you will use predefined codes that are set up in wave step codes.</span></span> <span data-ttu-id="3244c-123">I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="3244c-123">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="3244c-124">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="3244c-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="3244c-125">**Funksjonsnavn:** *Organisasjonsomfattende bølgetrinnkode*</span><span class="sxs-lookup"><span data-stu-id="3244c-125">**Feature name:** *Organization wide wave step code*</span></span>

## <a name="setup"></a><span data-ttu-id="3244c-126">Installasjon</span><span class="sxs-lookup"><span data-stu-id="3244c-126">Setup</span></span>

<span data-ttu-id="3244c-127">For denne demoen brukes standard Contoso-data og -lager *62*.</span><span class="sxs-lookup"><span data-stu-id="3244c-127">For this demo, standard Contoso data and warehouse *62* are used.</span></span> <span data-ttu-id="3244c-128">Noen tillegg som er nevnt senere, brukes også.</span><span class="sxs-lookup"><span data-stu-id="3244c-128">Some additions that are noted later are also used.</span></span>

### <a name="location-type"></a><span data-ttu-id="3244c-129">Plasseringstype</span><span class="sxs-lookup"><span data-stu-id="3244c-129">Location type</span></span>

1. <span data-ttu-id="3244c-130">Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonstyper**.</span><span class="sxs-lookup"><span data-stu-id="3244c-130">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="3244c-131">Velg **Ny** i handlingsruten for å opprette en lokasjonstype for sortering.</span><span class="sxs-lookup"><span data-stu-id="3244c-131">On the Action Pane, select **New** to create a location type for sorting.</span></span>
1. <span data-ttu-id="3244c-132">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3244c-132">Set the following values:</span></span>

    - <span data-ttu-id="3244c-133">**Lokasjonstype:** *SORTER*</span><span class="sxs-lookup"><span data-stu-id="3244c-133">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="3244c-134">**Beskrivelse:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="3244c-134">**Description:** *Sort*</span></span>

1. <span data-ttu-id="3244c-135">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3244c-135">Select **Save**.</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="3244c-136">Lagerstyringsparametere</span><span class="sxs-lookup"><span data-stu-id="3244c-136">Warehouse management parameters</span></span>

1. <span data-ttu-id="3244c-137">Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.</span><span class="sxs-lookup"><span data-stu-id="3244c-137">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="3244c-138">I fanen **Generelt** i hurtigfanen **Lokasjonstyper** setter du feltet for **sorteringslokasjonstype** til *SORTER*.</span><span class="sxs-lookup"><span data-stu-id="3244c-138">On the **General** tab, on the **Location types** FastTab, in the **Sorting location type** field, enter *SORT*.</span></span>
1. <span data-ttu-id="3244c-139">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3244c-139">Select **Save**.</span></span>

### <a name="location-profile"></a><span data-ttu-id="3244c-140">Lokasjonsprofil</span><span class="sxs-lookup"><span data-stu-id="3244c-140">Location profile</span></span>

1. <span data-ttu-id="3244c-141">Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="3244c-141">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="3244c-142">Velg **Ny** i handlingsruten for å opprette en lokasjonsprofil for sorteringslokasjon.</span><span class="sxs-lookup"><span data-stu-id="3244c-142">On the Action Pane, select **New** to create a location profile for the sorting location.</span></span>
1. <span data-ttu-id="3244c-143">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3244c-143">In the header, set the following values:</span></span>

    - <span data-ttu-id="3244c-144">**Lokasjonsprofil-ID:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="3244c-144">**Location profile ID:** *Sort*</span></span>
    - <span data-ttu-id="3244c-145">**Navn:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="3244c-145">**Name:** *Sort*</span></span>

1. <span data-ttu-id="3244c-146">Angi følgende verdier i **Generelt**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="3244c-146">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3244c-147">**Lokasjonsformat:** *PAKKE*</span><span class="sxs-lookup"><span data-stu-id="3244c-147">**Location format:** *PACK*</span></span>
    - <span data-ttu-id="3244c-148">**Lokasjonstype:** *SORTER*</span><span class="sxs-lookup"><span data-stu-id="3244c-148">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="3244c-149">**Bruk sporing av nummerskilt:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="3244c-149">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="3244c-150">**Tillat kombinerte varer:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="3244c-150">**Allow mixed items:** *Yes*</span></span>
    - <span data-ttu-id="3244c-151">Velg **Ja** i *Tillat kombinerte lagerstatuser*</span><span class="sxs-lookup"><span data-stu-id="3244c-151">**Allow mixed inventory statuses:** *Yes*</span></span>

1. <span data-ttu-id="3244c-152">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3244c-152">Select **Save**.</span></span>

### <a name="locations"></a><span data-ttu-id="3244c-153">Lokasjoner</span><span class="sxs-lookup"><span data-stu-id="3244c-153">Locations</span></span>

1. <span data-ttu-id="3244c-154">Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjoner**.</span><span class="sxs-lookup"><span data-stu-id="3244c-154">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="3244c-155">Fjern merket for **Generer kontrollsifre for lokasjon**.</span><span class="sxs-lookup"><span data-stu-id="3244c-155">Clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="3244c-156">Velg **Ny** i handlingsruten, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3244c-156">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="3244c-157">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="3244c-157">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="3244c-158">**Lokasjon:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="3244c-158">**Location:** *Sort*</span></span>
    - <span data-ttu-id="3244c-159">**Lokasjonsprofil-ID:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="3244c-159">**Location profile ID:** *Sort*</span></span>

1. <span data-ttu-id="3244c-160">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3244c-160">Select **Save**.</span></span>

### <a name="packing-profiles"></a><span data-ttu-id="3244c-161">Emballasjeprofil-ID</span><span class="sxs-lookup"><span data-stu-id="3244c-161">Packing profiles</span></span>

1. <span data-ttu-id="3244c-162">Gå til **Lagerstyring \> Oppsett \> Pakking \> Pakkeprofiler**.</span><span class="sxs-lookup"><span data-stu-id="3244c-162">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="3244c-163">Velg **Ny** i handlingsruten, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3244c-163">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="3244c-164">**Pakkeprofil-ID:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="3244c-164">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="3244c-165">**Beskrivelse:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="3244c-165">**Description:** *Sort*</span></span>
    - <span data-ttu-id="3244c-166">**Policy for containerpakking:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="3244c-166">**Container packing policy:** Leave this field blank.</span></span>
    - <span data-ttu-id="3244c-167">**Modus for container-ID:** *Automatisk*</span><span class="sxs-lookup"><span data-stu-id="3244c-167">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="3244c-168">**Containertype:** *PALL 48X48*</span><span class="sxs-lookup"><span data-stu-id="3244c-168">**Container type:** *PALLET 48X48*</span></span>
    - <span data-ttu-id="3244c-169">**Opprett container automatisk ved containerlukking:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="3244c-169">**Autocreate container at container close:** Leave this field blank.</span></span>

1. <span data-ttu-id="3244c-170">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3244c-170">Select **Save**.</span></span>

### <a name="wave-step-codes"></a><span data-ttu-id="3244c-171">Bølgetrinnkoder</span><span class="sxs-lookup"><span data-stu-id="3244c-171">Wave step codes</span></span>

<span data-ttu-id="3244c-172">Hvis du aktiverte *Organisasjonsomfattende bølgetrinnkode*, definerer du følgende kode.</span><span class="sxs-lookup"><span data-stu-id="3244c-172">If you turned on the *Organization wide wave step code* feature, set up the following code.</span></span>

1. <span data-ttu-id="3244c-173">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgetrinnkoder**.</span><span class="sxs-lookup"><span data-stu-id="3244c-173">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="3244c-174">Velg **Ny** i handlingsruten, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3244c-174">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="3244c-175">**Bølgetrinnkode:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="3244c-175">**Wave step code:** *Sort*</span></span>
    - <span data-ttu-id="3244c-176">**Bølgetrinnbeskrivelse:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="3244c-176">**Wave step description:** *Sort*</span></span>
    - <span data-ttu-id="3244c-177">**Bølgetrinntype:** *Sorter mal*</span><span class="sxs-lookup"><span data-stu-id="3244c-177">**Wave step type:** *Sort template*</span></span>

1. <span data-ttu-id="3244c-178">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3244c-178">Select **Save**.</span></span>

### <a name="outbound-sorting-template"></a><span data-ttu-id="3244c-179">Mal for utgående sortering</span><span class="sxs-lookup"><span data-stu-id="3244c-179">Outbound sorting template</span></span>

<span data-ttu-id="3244c-180">Sorteringsmalen styrer om sorteringsposisjoner opprettes, hvilke kriterier som brukes, og andre attributter for sorteringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="3244c-180">The sorting template controls whether sort positions are created, what criteria are used, and other attributes of the sorting process.</span></span>

1. <span data-ttu-id="3244c-181">Gå til **Lagerstyring \> Oppsett \> Pakking \> Utgående sorteringsmal**.</span><span class="sxs-lookup"><span data-stu-id="3244c-181">Go to **Warehouse management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="3244c-182">I handlingsruten velger du **Ny** for å opprette en sorteringsmal.</span><span class="sxs-lookup"><span data-stu-id="3244c-182">On the Action Pane, select **New** to create a sorting template.</span></span>
1. <span data-ttu-id="3244c-183">I toppteksten på den nye malen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3244c-183">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="3244c-184">**ID for utgående sorteringsmal:** *Bølgesortering*</span><span class="sxs-lookup"><span data-stu-id="3244c-184">**Outbound sorting template ID:** *Wave Sort*</span></span>
    - <span data-ttu-id="3244c-185">**Beskrivelse:** *Bølgesortering*</span><span class="sxs-lookup"><span data-stu-id="3244c-185">**Description:** *Wave sort*</span></span>
    - <span data-ttu-id="3244c-186">**Sorteringsmaltype:** *Bølgebehov*</span><span class="sxs-lookup"><span data-stu-id="3244c-186">**Sort template type:** *Wave demand*</span></span>

        <span data-ttu-id="3244c-187">Dette feltet definerer prosessen som sorteringsmalen brukes til.</span><span class="sxs-lookup"><span data-stu-id="3244c-187">This field defines the process that the sorting template is used for.</span></span> <span data-ttu-id="3244c-188">Følgende verdier er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="3244c-188">The following values are available:</span></span>

        - <span data-ttu-id="3244c-189">**Bølgebehov** – Sorteringsmalen brukes til prosessen *Plasser til vegg*.</span><span class="sxs-lookup"><span data-stu-id="3244c-189">**Wave demand** – The sorting template is used for the *Put to wall* process.</span></span> <span data-ttu-id="3244c-190">Denne maltypen brukes til å omgå pakkestasjonen og behandle lageret direkte utenfor bølgen.</span><span class="sxs-lookup"><span data-stu-id="3244c-190">This template type is used to bypass the pack station and process inventory directly out of the wave.</span></span> <span data-ttu-id="3244c-191">Du kan bare bruke denne typen hvis **sortering**-bølgeprosessmetoden er inkludert i bølgemalen.</span><span class="sxs-lookup"><span data-stu-id="3244c-191">You can use this type only if the **sorting** wave process method is included in the wave template.</span></span>
        - <span data-ttu-id="3244c-192">**Container** – Sorteringsmalen brukes til prosessen for *Pallbyggingen etter pakking*.</span><span class="sxs-lookup"><span data-stu-id="3244c-192">**Container** – The sorting template is used for the *Pallet building after packing* process.</span></span> <span data-ttu-id="3244c-193">Denne maltypen brukes til å behandle containere som er lukket på pakkestasjonen og må sorteres på paller.</span><span class="sxs-lookup"><span data-stu-id="3244c-193">This template type is used to process containers that are closed at the pack station and must be sorted onto pallets.</span></span>

    - <span data-ttu-id="3244c-194">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="3244c-194">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="3244c-195">**Lokasjon:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="3244c-195">**Location:** *Sort*</span></span>

1. <span data-ttu-id="3244c-196">Angi følgende verdier i **Generelt**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="3244c-196">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3244c-197">**Sorteringsbekreftelse:** *Posisjonsskanning*</span><span class="sxs-lookup"><span data-stu-id="3244c-197">**Sort verification:** *Position scan*</span></span>

        <span data-ttu-id="3244c-198">Dette feltet definerer bekreftelsen som kreves ved sortering.</span><span class="sxs-lookup"><span data-stu-id="3244c-198">This field defines the verification that is required during sorting.</span></span> <span data-ttu-id="3244c-199">Følgende verdier er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="3244c-199">The following values are available:</span></span>

        - <span data-ttu-id="3244c-200">None</span><span class="sxs-lookup"><span data-stu-id="3244c-200">None</span></span>
        - <span data-ttu-id="3244c-201">Nummerskiltskanning</span><span class="sxs-lookup"><span data-stu-id="3244c-201">License plate scan</span></span>
        - <span data-ttu-id="3244c-202">Posisjonsskanning</span><span class="sxs-lookup"><span data-stu-id="3244c-202">Position scan</span></span>

    - <span data-ttu-id="3244c-203">**Opprett arbeid ved posisjonslukking:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="3244c-203">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="3244c-204">Hvis dette valget settes til *Ja* når posisjonen er lukket, opprettes arbeid for å flytte lageret til den endelige leveringslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="3244c-204">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="3244c-205">Hvis det settes til *Nei*, plukkes lageret umiddelbart til ordren når posisjonen lukkes.</span><span class="sxs-lookup"><span data-stu-id="3244c-205">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="3244c-206">**Stillingstilordning:** *Manuell*</span><span class="sxs-lookup"><span data-stu-id="3244c-206">**Position assignment:** *Manual*</span></span>

        <span data-ttu-id="3244c-207">Dette feltet definerer typen stillingstilordning.</span><span class="sxs-lookup"><span data-stu-id="3244c-207">This field defines the type of position assignment.</span></span> <span data-ttu-id="3244c-208">Følgende verdier er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="3244c-208">The following values are available:</span></span>

        - <span data-ttu-id="3244c-209">**Manuell** – Brukeren må alltid angi hvilken posisjon lageret skal sorteres til.</span><span class="sxs-lookup"><span data-stu-id="3244c-209">**Manual** – The user must always indicate which position the inventory should be sorted to.</span></span>
        - <span data-ttu-id="3244c-210">**Automatisk** – Systemet sender automatisk lageret til en posisjon når det er mulig, basert på inndelingene i sorteringsmalen.</span><span class="sxs-lookup"><span data-stu-id="3244c-210">**Automatic** – The system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

    - <span data-ttu-id="3244c-211">**Tilordne kriterier for sorteringsposisjon:** *Bruk bare tom plassering*</span><span class="sxs-lookup"><span data-stu-id="3244c-211">**Assign sort position criteria:** *Only use empty position*</span></span>

        <span data-ttu-id="3244c-212">Dette feltet styrer om lageret som allerede finnes på sorteringsposisjoner, skal tas hensyn til når en posisjon tilordnes for behovet.</span><span class="sxs-lookup"><span data-stu-id="3244c-212">This field controls whether inventory that is already present on sort positions is taken into account when a position is assigned for the demand.</span></span> <span data-ttu-id="3244c-213">Følgende verdier er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="3244c-213">The following values are available:</span></span>

        - <span data-ttu-id="3244c-214">**Bruk bare tom plassering** – Stillinger som allerede har tilknyttet lager, vil bli tatt med i betraktningen</span><span class="sxs-lookup"><span data-stu-id="3244c-214">**Only use empty position** – Positions that already have inventory associated with them will be taken into account</span></span>
        - <span data-ttu-id="3244c-215">**Anta tom plassering** – Et lager som allerede finnes på plasseringen, ignoreres under tilordningen.</span><span class="sxs-lookup"><span data-stu-id="3244c-215">**Assume position empty** – Any inventory that is already on the position will be disregarded during assignment.</span></span> <span data-ttu-id="3244c-216">Alle tilgjengelige plasseringer vil bli brukt.</span><span class="sxs-lookup"><span data-stu-id="3244c-216">All available positions will be used.</span></span>

    - <span data-ttu-id="3244c-217">**Bølgetrinnkode:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="3244c-217">**Wave step code:** *Sort*</span></span>

        <span data-ttu-id="3244c-218">Hvis funksjonen *Organisasjonsomfattende bølgetrinnkode* er aktivert, må *Sorter*-bølgetrinnkoden også konfigureres i bølgetrinnkodene.</span><span class="sxs-lookup"><span data-stu-id="3244c-218">If the *Organization wide wave step code* feature is turned on, the *Sort* wave step code must also be set up in wave step codes.</span></span>

    - <span data-ttu-id="3244c-219">**Automatisk lukking av sorteringsposisjon:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="3244c-219">**Auto close sort position:** *Yes*</span></span>

        <span data-ttu-id="3244c-220">Hvis dette alternativet er satt til *Ja*, vil sorteringsposisjonen automatisk lukkes når alt arbeid som kommer til posisjonen, er fullført.</span><span class="sxs-lookup"><span data-stu-id="3244c-220">If this option is set to *Yes*, the sort position will automatically be closed when all work that comes to the position has been completed.</span></span>

    - <span data-ttu-id="3244c-221">**Antall sorteringsposisjoner:** *3*</span><span class="sxs-lookup"><span data-stu-id="3244c-221">**Number of sort positions:** *3*</span></span>

        <span data-ttu-id="3244c-222">Dette feltet angir maksimalt antall sorteringsposisjoner som systemet vil opprette.</span><span class="sxs-lookup"><span data-stu-id="3244c-222">This field defines the maximum number of sort positions that the system will create.</span></span>

    - <span data-ttu-id="3244c-223">**Prefiks for sorteringsposisjon:** *SP-*</span><span class="sxs-lookup"><span data-stu-id="3244c-223">**Sort position prefix:** *SP-*</span></span>

        <span data-ttu-id="3244c-224">Dette feltet definerer prefikset som systemet tilordner før posisjonsnummeret.</span><span class="sxs-lookup"><span data-stu-id="3244c-224">This field defines the prefix that the system assigns before the position number.</span></span>

    - <span data-ttu-id="3244c-225">**Automatisk pakking av sorteringsposisjon:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="3244c-225">**Auto pack sort position:** *Yes*</span></span>

        <span data-ttu-id="3244c-226">Hvis dette alternativet er satt til *Ja*, vil lageret på sorteringsposisjonen pakkes i en container når posisjonen lukkes.</span><span class="sxs-lookup"><span data-stu-id="3244c-226">If this option is set to *Yes*, the inventory on the sort position will be packed into a container when the position is closed.</span></span>

    - <span data-ttu-id="3244c-227">**Pakkeprofil-ID:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="3244c-227">**Packing profile ID:** *Sort*</span></span>

        <span data-ttu-id="3244c-228">Dette feltet definerer pakkeprofilen som vil bli brukt når sorteringsposisjonen pakkes i en container.</span><span class="sxs-lookup"><span data-stu-id="3244c-228">This field defines the packing profile that will be used when the sort position is packed into a container.</span></span>

1. <span data-ttu-id="3244c-229">Velg **Rediger spørring** i handlingsruten for å angi kriteriene som brukes for denne sorteringsmalen.</span><span class="sxs-lookup"><span data-stu-id="3244c-229">On the Action Pane, select **Edit query** to specify the criteria that are used for this sorting template.</span></span>
1. <span data-ttu-id="3244c-230">I spørringsdialogboksen i fanen **Sortering** velger du **Ny** for å legge til en linje, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3244c-230">In the query dialog box, on the **Sorting** tab, select **New** to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="3244c-231">**Tabell:** *Lastdetaljer*</span><span class="sxs-lookup"><span data-stu-id="3244c-231">**Table:** *Load details*</span></span>
    - <span data-ttu-id="3244c-232">**Avledet tabell:** *Lastdetaljer*</span><span class="sxs-lookup"><span data-stu-id="3244c-232">**Derived table:** *Load details*</span></span>
    - <span data-ttu-id="3244c-233">**Felt:** *Leverings-ID*</span><span class="sxs-lookup"><span data-stu-id="3244c-233">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="3244c-234">**Søkeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="3244c-234">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="3244c-235">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3244c-235">Select **OK**.</span></span>
1. <span data-ttu-id="3244c-236">Du kan få følgende melding: "Gruppering vil bli tilbakestilt, vil du fortsette?"</span><span class="sxs-lookup"><span data-stu-id="3244c-236">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="3244c-237">Velg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3244c-237">Select **Yes**.</span></span>

    <span data-ttu-id="3244c-238">Knappen for **Inndelinger for utgående sortereringmal** i handlingsruten blir tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="3244c-238">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="3244c-239">Velg alternativet for **Inndelinger for utgående sortereringmal** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3244c-239">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="3244c-240">Merk av for **Grupper etter-feltet** for å gruppere etter forsendelses-ID.</span><span class="sxs-lookup"><span data-stu-id="3244c-240">Select the **Group by field** check box to group by shipment ID.</span></span>

    <span data-ttu-id="3244c-241">Denne innstillingen vil opprette én sorteringsposisjon per forsendelse som er en container i bølgen.</span><span class="sxs-lookup"><span data-stu-id="3244c-241">This setting will create one sort position per shipment that is a container in the wave.</span></span>

1. <span data-ttu-id="3244c-242">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3244c-242">Select **OK**.</span></span>

### <a name="wave-process-methods"></a><span data-ttu-id="3244c-243">Bølgebehandlingsmetoder</span><span class="sxs-lookup"><span data-stu-id="3244c-243">Wave process methods</span></span>

1. <span data-ttu-id="3244c-244">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgebehandlingsmetoder**.</span><span class="sxs-lookup"><span data-stu-id="3244c-244">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="3244c-245">Velg **Regenerer metoder** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3244c-245">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="3244c-246">**Sortering**-metoden legges til i listen over tilgjengelige metoder, og bølgemaltypen *Forsendelse* velges for den.</span><span class="sxs-lookup"><span data-stu-id="3244c-246">The **sorting** method is added to the list of available methods, and the *Shipping* wave template type is selected for it.</span></span>

### <a name="wave-templates"></a><span data-ttu-id="3244c-247">Bølgemaler</span><span class="sxs-lookup"><span data-stu-id="3244c-247">Wave templates</span></span>

<span data-ttu-id="3244c-248">Rediger bølgemalen som brukes for bølgebehovsortering.</span><span class="sxs-lookup"><span data-stu-id="3244c-248">Edit the wave template that is used for wave demand sorting.</span></span>

1. <span data-ttu-id="3244c-249">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.</span><span class="sxs-lookup"><span data-stu-id="3244c-249">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="3244c-250">I feltet *Bølgemaltype* velger du **Forsendelse**.</span><span class="sxs-lookup"><span data-stu-id="3244c-250">In the **Wave template type** field, select *Shipping*.</span></span>
1. <span data-ttu-id="3244c-251">Velg den eksisterende malen **62 Standardforsendelse**.</span><span class="sxs-lookup"><span data-stu-id="3244c-251">Select the existing **62 Shipping default** template.</span></span>
1. <span data-ttu-id="3244c-252">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="3244c-252">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="3244c-253">Gjør følgende endringer i hurtigfanen **Generelt**:</span><span class="sxs-lookup"><span data-stu-id="3244c-253">On the **General** FastTab, make the following changes:</span></span>

    - <span data-ttu-id="3244c-254">Sett alternativet **Behandle bølge ved frigivelse til lager** til *Nei*.</span><span class="sxs-lookup"><span data-stu-id="3244c-254">Set the **Process wave at release to warehouse** option to *No*.</span></span>
    - <span data-ttu-id="3244c-255">Sett alternativet **Tilordne til åpne bølger** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="3244c-255">Set the **Assign to open waves** option to *Yes*.</span></span>

1. <span data-ttu-id="3244c-256">I hurtigfanen **Metoder** angir du metoden **Sortering**:</span><span class="sxs-lookup"><span data-stu-id="3244c-256">On the **Methods** FastTab, set up the **sorting** method:</span></span>

    1. <span data-ttu-id="3244c-257">I rutenettet **Gjenværende metoder** velger du **Sortering**.</span><span class="sxs-lookup"><span data-stu-id="3244c-257">In the **Remaining Methods** grid, select **sorting**.</span></span>
    2. <span data-ttu-id="3244c-258">Velg høyre pil for å flytte **sortering** til **Valgte metoder**-rutenettet.</span><span class="sxs-lookup"><span data-stu-id="3244c-258">Select the right arrow button to move **sorting** to the **Selected Methods** grid.</span></span>
    3. <span data-ttu-id="3244c-259">I rutenettet **Valgte metoder** velger du **Sortering**.</span><span class="sxs-lookup"><span data-stu-id="3244c-259">In the **Selected Methods** grid, select **sorting**.</span></span>
    4. <span data-ttu-id="3244c-260">Angi feltet **Bølgetrinnkode** til *Sorter*.</span><span class="sxs-lookup"><span data-stu-id="3244c-260">Set the **Wave step code** field to *Sort*.</span></span>

1. <span data-ttu-id="3244c-261">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3244c-261">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="3244c-262">Menyelementer på mobilenheten</span><span class="sxs-lookup"><span data-stu-id="3244c-262">Mobile device menu items</span></span>

1. <span data-ttu-id="3244c-263">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="3244c-263">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="3244c-264">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3244c-264">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3244c-265">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3244c-265">In the header, set the following values:</span></span>

    - <span data-ttu-id="3244c-266">**Menyelementnavn:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="3244c-266">**Menu item name:** *Sort*</span></span>
    - <span data-ttu-id="3244c-267">**Tittel:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="3244c-267">**Title:** *Sort*</span></span>
    - <span data-ttu-id="3244c-268">**Modus:** *Indirekte*</span><span class="sxs-lookup"><span data-stu-id="3244c-268">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="3244c-269">**Bruke eksisterende arbeid:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="3244c-269">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="3244c-270">Angi følgende verdier i **Generelt**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="3244c-270">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3244c-271">**Aktivitetskode:** *Utgående sortering*</span><span class="sxs-lookup"><span data-stu-id="3244c-271">**Activity code:** *Outbound sorting*</span></span>
    - <span data-ttu-id="3244c-272">**Bruk prosessveiledning:** *Ja* (standardverdi)</span><span class="sxs-lookup"><span data-stu-id="3244c-272">**Use process guide:** *Yes* (default value)</span></span>
    - <span data-ttu-id="3244c-273">**ID for utgående sorteringsmal:** *Bølgesortering*</span><span class="sxs-lookup"><span data-stu-id="3244c-273">**Outbound sorting template ID:** *Wave Sort*</span></span>

1. <span data-ttu-id="3244c-274">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3244c-274">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="3244c-275">Meny på mobilenheten</span><span class="sxs-lookup"><span data-stu-id="3244c-275">Mobile device menu</span></span>

1. <span data-ttu-id="3244c-276">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="3244c-276">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="3244c-277">Velg **Utgående** i listen over menyer.</span><span class="sxs-lookup"><span data-stu-id="3244c-277">In the list of menus, select **Outbound**.</span></span>
1. <span data-ttu-id="3244c-278">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="3244c-278">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="3244c-279">I rutenettet **Tilgjengelige menyer og menyelementer** finner og velger du **Sorter**-menyelementet du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="3244c-279">In the **Available Menus And Menu Items** grid, find and select the **Sort** menu item that you just created.</span></span>
1. <span data-ttu-id="3244c-280">Velg høyre pil-knappen for å flytte **Sorter** til rutenettet **Menystruktur**.</span><span class="sxs-lookup"><span data-stu-id="3244c-280">Select the right arrow button to move **Sort** to the **Menu Structure** grid.</span></span> <span data-ttu-id="3244c-281">På denne måten legger du til menyelementet på menyen **Utgående**.</span><span class="sxs-lookup"><span data-stu-id="3244c-281">In this way, you add the menu item to the **Outbound** menu.</span></span>
1. <span data-ttu-id="3244c-282">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3244c-282">Select **Save**.</span></span>

### <a name="location-directives"></a><span data-ttu-id="3244c-283">Lokasjonsdirektiver</span><span class="sxs-lookup"><span data-stu-id="3244c-283">Location directives</span></span>

<span data-ttu-id="3244c-284">Du må opprette lokasjonsdirektiver for å veilede arbeidet som opprettes etter at sorteringen er fullført.</span><span class="sxs-lookup"><span data-stu-id="3244c-284">You must create location directives to guide the work that is created after the sorting is completed.</span></span>

1. <span data-ttu-id="3244c-285">Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.</span><span class="sxs-lookup"><span data-stu-id="3244c-285">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="3244c-286">Velg *Sortert lagerplukking* i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="3244c-286">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="3244c-287">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3244c-287">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3244c-288">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3244c-288">In the header, set the following values:</span></span>

    - <span data-ttu-id="3244c-289">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="3244c-289">**Sequence:** *1*</span></span>
    - <span data-ttu-id="3244c-290">**Navn:** *Sett til rampedør*</span><span class="sxs-lookup"><span data-stu-id="3244c-290">**Name:** *Put to Baydoor*</span></span>

1. <span data-ttu-id="3244c-291">Angi følgende verdier i **Lokasjonsdirektiver**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="3244c-291">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3244c-292">**Arbeidstype:** *Plasser*</span><span class="sxs-lookup"><span data-stu-id="3244c-292">**Work type:** *Put*</span></span>
    - <span data-ttu-id="3244c-293">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="3244c-293">**Site:** *6*</span></span>
    - <span data-ttu-id="3244c-294">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="3244c-294">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="3244c-295">**Direktivkoden:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="3244c-295">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="3244c-296">**Flere SKUer:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="3244c-296">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="3244c-297">Velg **Lagre** for å gjøre **Linjer**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="3244c-297">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="3244c-298">På hurtigfanen **Linjer** velger du **Ny**, og angi deretter følgende verdier.</span><span class="sxs-lookup"><span data-stu-id="3244c-298">On the **Lines** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="3244c-299">Godta standardverdiene for alle de andre feltene.</span><span class="sxs-lookup"><span data-stu-id="3244c-299">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="3244c-300">**Sekvensnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="3244c-300">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="3244c-301">**Fra-antall:** *0*</span><span class="sxs-lookup"><span data-stu-id="3244c-301">**From quantity:** *0*</span></span>
    - <span data-ttu-id="3244c-302">**Til-antall:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="3244c-302">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="3244c-303">Velg **Lagre** for å gjøre **Lokasjonsdirektivhandlinger**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="3244c-303">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="3244c-304">På hurtigfanen **Handlinger for lokasjonsdirektiv** velger du **Ny**, og angi deretter følgende verdier.</span><span class="sxs-lookup"><span data-stu-id="3244c-304">On the **Location Directive Actions** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="3244c-305">Godta standardverdiene for alle de andre feltene.</span><span class="sxs-lookup"><span data-stu-id="3244c-305">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="3244c-306">**Sekvensnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="3244c-306">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="3244c-307">**Navn:** *Rampedør*</span><span class="sxs-lookup"><span data-stu-id="3244c-307">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="3244c-308">Velg **Lagre** for å gjøre **Rediger spørring**-knappen på **Lokasjonsdirektivhandlinger**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="3244c-308">Select **Save** to make the **Edit query** button on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="3244c-309">I **Handlinger for lokasjonsdirektiv**-hurtigfanen velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="3244c-309">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="3244c-310">I dialogboksen for spørring, i fanen **Område**, finner du raden der feltet **Felt** er satt til *Lokasjon*.</span><span class="sxs-lookup"><span data-stu-id="3244c-310">In the query dialog box, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="3244c-311">Sett **Vilkår**-feltet for denne raden til *Rampedør*.</span><span class="sxs-lookup"><span data-stu-id="3244c-311">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="3244c-312">Velg **OK** for å bekrefte redigeringen.</span><span class="sxs-lookup"><span data-stu-id="3244c-312">Select **OK** to confirm the edit.</span></span>

### <a name="work-classes"></a><span data-ttu-id="3244c-313">Arbeidsklasser</span><span class="sxs-lookup"><span data-stu-id="3244c-313">Work classes</span></span>

1. <span data-ttu-id="3244c-314">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsklasser**.</span><span class="sxs-lookup"><span data-stu-id="3244c-314">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="3244c-315">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3244c-315">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3244c-316">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3244c-316">In the header, set the following values:</span></span>

    - <span data-ttu-id="3244c-317">**Arbeidsklasse-ID:** *Sortering*</span><span class="sxs-lookup"><span data-stu-id="3244c-317">**Work class ID:** *Sorting*</span></span>
    - <span data-ttu-id="3244c-318">**Beskrivelse:** *Sortering*</span><span class="sxs-lookup"><span data-stu-id="3244c-318">**Description:** *Sorting*</span></span>
    - <span data-ttu-id="3244c-319">**Arbeidsordretype:** *Sortert lagerplukking*</span><span class="sxs-lookup"><span data-stu-id="3244c-319">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="3244c-320">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3244c-320">Select **Save**.</span></span>

### <a name="work-templates"></a><span data-ttu-id="3244c-321">Arbeidsmaler</span><span class="sxs-lookup"><span data-stu-id="3244c-321">Work templates</span></span>

1. <span data-ttu-id="3244c-322">Gå til **Lagerstyring \> Arbeid \> Arbeidsmaler**.</span><span class="sxs-lookup"><span data-stu-id="3244c-322">Go to **Warehouse management \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="3244c-323">Velg *Salgsordrer* i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="3244c-323">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="3244c-324">Velg **62 Plukk til pakke**-arbeidsmalen i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="3244c-324">In the grid, select the **62 Pick to pack** work template.</span></span>
1. <span data-ttu-id="3244c-325">Velg **Arbeidshodeskift** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3244c-325">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="3244c-326">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="3244c-326">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="3244c-327">I linjen der **Feltnavn**-feltet er satt til *Forsendelses-ID*, fjerner du merket i avmerkings boksen **Grupper etter dette feltet** .</span><span class="sxs-lookup"><span data-stu-id="3244c-327">On the line where the **Field name** field is set to *Shipment ID*, clear the **Group by this field** check box.</span></span>
1. <span data-ttu-id="3244c-328">Velg **Lagre**, og lukk deretter dialogboksen **Arbeidshodeskift**.</span><span class="sxs-lookup"><span data-stu-id="3244c-328">Select **Save**, and then close the **Work header breaks** dialog box.</span></span>
1. <span data-ttu-id="3244c-329">Velg *Sortert lagerplukking* i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="3244c-329">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="3244c-330">Velg **Ny** for å opprette en arbeidsmal.</span><span class="sxs-lookup"><span data-stu-id="3244c-330">Select **New** to create a work template.</span></span>
1. <span data-ttu-id="3244c-331">Angi følgende verdier i delen **Oversikt**.</span><span class="sxs-lookup"><span data-stu-id="3244c-331">In the **Overview** section, set the following values.</span></span> <span data-ttu-id="3244c-332">Godta standardverdiene for alle de andre feltene.</span><span class="sxs-lookup"><span data-stu-id="3244c-332">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="3244c-333">**Arbeidsmal:** *Sortert plukking*</span><span class="sxs-lookup"><span data-stu-id="3244c-333">**Work template:** *Sorted picking*</span></span>
    - <span data-ttu-id="3244c-334">**Beskrivelse av arbeidsmal:** *Sortert plukking*</span><span class="sxs-lookup"><span data-stu-id="3244c-334">**Work template description:** *Sorted picking*</span></span>

1. <span data-ttu-id="3244c-335">Velg **Lagre** for å gjøre **Arbeidsmaldetaljer**-delen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="3244c-335">Select **Save** to make the **Work Template Details** section available.</span></span>
1. <span data-ttu-id="3244c-336">I delen **Arbeidsmaldetaljer** oppretter du to linjer.</span><span class="sxs-lookup"><span data-stu-id="3244c-336">In the **Work Template Details** section, you will create two lines.</span></span> <span data-ttu-id="3244c-337">Velg **Ny**, og angi deretter følgende verdier for linje 1:</span><span class="sxs-lookup"><span data-stu-id="3244c-337">Select **New**, and then set the following values for line 1:</span></span>

    - <span data-ttu-id="3244c-338">**Arbeidstype:** *Plukk*</span><span class="sxs-lookup"><span data-stu-id="3244c-338">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="3244c-339">**Obligatorisk:** Valgt (= *Ja*)</span><span class="sxs-lookup"><span data-stu-id="3244c-339">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="3244c-340">**Arbeidsklasse-ID:** *Sortering*</span><span class="sxs-lookup"><span data-stu-id="3244c-340">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="3244c-341">Velg **Ny** på nytt, og angi deretter følgende verdier for linje 2:</span><span class="sxs-lookup"><span data-stu-id="3244c-341">Select **New** again, and then set the following values for line 2:</span></span>

    - <span data-ttu-id="3244c-342">**Arbeidstype:** *Plasser*</span><span class="sxs-lookup"><span data-stu-id="3244c-342">**Work type:** *Put*</span></span>
    - <span data-ttu-id="3244c-343">**Obligatorisk:** Valgt (= *Ja*)</span><span class="sxs-lookup"><span data-stu-id="3244c-343">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="3244c-344">**Arbeidsklasse-ID:** *Sortering*</span><span class="sxs-lookup"><span data-stu-id="3244c-344">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="3244c-345">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3244c-345">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="3244c-346">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="3244c-346">Example scenario</span></span>

<span data-ttu-id="3244c-347">Dette scenariet simulerer en situasjon der lageret lagrer små varer på lokasjoner og må pakke dem i bokser før de leveres, og der pakkestasjonsfunksjonaliteten ikke passer.</span><span class="sxs-lookup"><span data-stu-id="3244c-347">This scenario simulates a situation where the warehouse stores small items in locations and must pack them into boxes before they are shipped, and where packing station functionality isn't really suitable.</span></span> <span data-ttu-id="3244c-348">Arbeidere plukker bestillinger for flere kunder og forskjellige adresser samtidig for å øke plukkehastigheten.</span><span class="sxs-lookup"><span data-stu-id="3244c-348">Workers pick orders for multiple customers and different addresses at the same time to increase the picking speed.</span></span> <span data-ttu-id="3244c-349">Når plukkingen er fullført, kommer arbeidere til sorteringslokasjonen, der de plukkede varene kan sorteres til riktig boks basert på nødvendige kriterier.</span><span class="sxs-lookup"><span data-stu-id="3244c-349">After picking has been completed, the workers arrive at the sorting location, where the picked items can be sorted to the correct box, based on required criteria.</span></span> <span data-ttu-id="3244c-350">I dette eksemplet vil forsendelses-IDen bli brukt til å fastslå den riktige boksen, fordi hver forsendelse har en annen adresse.</span><span class="sxs-lookup"><span data-stu-id="3244c-350">In this example, the shipment ID will be used to determine the correct box, because each shipment has a different address.</span></span> <span data-ttu-id="3244c-351">Etter at alle varer fra lasten er pakket og sortert etter forsendelse, flyttes boksene til oppsamlingsområdet, og til slutt lastes de på en lastebil.</span><span class="sxs-lookup"><span data-stu-id="3244c-351">After all items from the load are packed and sorted by shipment, the boxes will be moved to the staging area and eventually loaded onto a truck.</span></span>

<span data-ttu-id="3244c-352">Før du starter scenariet må du kontrollere at alle standard lagerfunksjoner er definert riktig for lageret.</span><span class="sxs-lookup"><span data-stu-id="3244c-352">Before you start the scenario, make sure that all standard warehouse functionality is set up correctly for your warehouse.</span></span> <span data-ttu-id="3244c-353">Standard Contoso-lager *62* brukes til dette formålet.</span><span class="sxs-lookup"><span data-stu-id="3244c-353">Standard Contoso warehouse *62* is used for this purpose.</span></span> <span data-ttu-id="3244c-354">Standardkonfigurasjoner er ikke endret, bortsett fra det som er beskrevet i oppsettet.</span><span class="sxs-lookup"><span data-stu-id="3244c-354">Standard configurations haven't been changed, besides what is described in the setup.</span></span>

### <a name="create-demand"></a><span data-ttu-id="3244c-355">Opprette behov</span><span class="sxs-lookup"><span data-stu-id="3244c-355">Create demand</span></span>

<span data-ttu-id="3244c-356">Før funksjonaliteten kan demonstreres, må du opprette behov.</span><span class="sxs-lookup"><span data-stu-id="3244c-356">Before the functionality can be demonstrated, you must create some demand.</span></span> <span data-ttu-id="3244c-357">I dette scenariet skal du opprette tre salgsordrer for at tre ulike kunder skal simulere forskjellige leveringsadresser.</span><span class="sxs-lookup"><span data-stu-id="3244c-357">For this scenario, you will create three sales orders for three different customers to simulate different delivery addresses.</span></span> <span data-ttu-id="3244c-358">På denne måten skal du opprette tre separate forsendelser.</span><span class="sxs-lookup"><span data-stu-id="3244c-358">In this way, you will create three separate shipments.</span></span>

<span data-ttu-id="3244c-359">Før du oppretter salgsordrer og forsendelser må du kontrollere at plukklokasjonene har nok lager for alle varene på ordrene.</span><span class="sxs-lookup"><span data-stu-id="3244c-359">Before you create sales orders and shipments, make sure that the pick locations have enough inventory for all the items on the orders.</span></span> <span data-ttu-id="3244c-360">Se gjennom lokasjonsdirektivinnstillingene for å bekrefte plukklokasjonene som skal brukes for plukking av salgsordre.</span><span class="sxs-lookup"><span data-stu-id="3244c-360">Review the location directive settings to confirm the picking locations that are used for sales order picking.</span></span> <span data-ttu-id="3244c-361">Hvis du må justere beholdninge, kan du opprette manuelle flyttinger, bruke etterfylling eller bruke en annen flyt.</span><span class="sxs-lookup"><span data-stu-id="3244c-361">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span> <span data-ttu-id="3244c-362">Reserver deretter lageret.</span><span class="sxs-lookup"><span data-stu-id="3244c-362">Then reserve the inventory.</span></span>

1. <span data-ttu-id="3244c-363">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="3244c-363">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="3244c-364">Velg **Ny** for å opprette en ny salgsordre for ordre 1.</span><span class="sxs-lookup"><span data-stu-id="3244c-364">Select **New** to create a sales order for order 1.</span></span>
1. <span data-ttu-id="3244c-365">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3244c-365">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3244c-366">**Kunde:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="3244c-366">**Customer:** *US-001*</span></span>
    - <span data-ttu-id="3244c-367">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="3244c-367">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="3244c-368">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3244c-368">Select **OK**.</span></span>
1. <span data-ttu-id="3244c-369">Det legges til en ny linje i rutenettet på **Salgsordrelinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="3244c-369">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="3244c-370">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3244c-370">Set the following values:</span></span>

    - <span data-ttu-id="3244c-371">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="3244c-371">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="3244c-372">**Antall:** *5*</span><span class="sxs-lookup"><span data-stu-id="3244c-372">**Quantity:** *5*</span></span>

1. <span data-ttu-id="3244c-373">Velg **Legg til linje** for å legge til en ny linje, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3244c-373">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="3244c-374">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="3244c-374">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="3244c-375">**Antall:** *10*</span><span class="sxs-lookup"><span data-stu-id="3244c-375">**Quantity:** *10*</span></span>

1. <span data-ttu-id="3244c-376">Gjenta følgende trinn for hver salgslinje i ordren for å reservere lager for den:</span><span class="sxs-lookup"><span data-stu-id="3244c-376">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="3244c-377">På **Salgsordrelinjer**-fanen, på **Beholdning**-menyen, velger du **Reservasjon**.</span><span class="sxs-lookup"><span data-stu-id="3244c-377">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="3244c-378">På **Reservasjon**-siden velger du **Reserver parti**, og deretter lukker du siden.</span><span class="sxs-lookup"><span data-stu-id="3244c-378">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="3244c-379">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3244c-379">Select **Save**.</span></span>

1. <span data-ttu-id="3244c-380">Velg **Ny** for å opprette en ny salgsordre for ordre 2.</span><span class="sxs-lookup"><span data-stu-id="3244c-380">Select **New** to create a sales order for order 2.</span></span>
1. <span data-ttu-id="3244c-381">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3244c-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3244c-382">**Kunde:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="3244c-382">**Customer:** *US-004*</span></span>
    - <span data-ttu-id="3244c-383">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="3244c-383">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="3244c-384">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3244c-384">Select **OK**.</span></span>
1. <span data-ttu-id="3244c-385">Det legges til en ny linje i rutenettet på **Salgsordrelinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="3244c-385">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="3244c-386">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3244c-386">Set the following values:</span></span>

    - <span data-ttu-id="3244c-387">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="3244c-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="3244c-388">**Antall:** *7*</span><span class="sxs-lookup"><span data-stu-id="3244c-388">**Quantity:** *7*</span></span>

1. <span data-ttu-id="3244c-389">Velg **Legg til linje** for å legge til en ny linje, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3244c-389">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="3244c-390">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="3244c-390">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="3244c-391">**Antall:** *3*</span><span class="sxs-lookup"><span data-stu-id="3244c-391">**Quantity:** *3*</span></span>

1. <span data-ttu-id="3244c-392">Gjenta følgende trinn for hver salgslinje i ordren for å reservere lager for den:</span><span class="sxs-lookup"><span data-stu-id="3244c-392">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="3244c-393">På **Salgsordrelinjer**-fanen, på **Beholdning**-menyen, velger du **Reservasjon**.</span><span class="sxs-lookup"><span data-stu-id="3244c-393">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="3244c-394">På **Reservasjon**-siden velger du **Reserver parti**, og deretter lukker du siden.</span><span class="sxs-lookup"><span data-stu-id="3244c-394">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="3244c-395">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3244c-395">Select **Save**.</span></span>

1. <span data-ttu-id="3244c-396">Velg **Ny** for å opprette en ny salgsordre for ordre 3.</span><span class="sxs-lookup"><span data-stu-id="3244c-396">Select **New** to create a sales order for order 3.</span></span>
1. <span data-ttu-id="3244c-397">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3244c-397">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3244c-398">**Kunde:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="3244c-398">**Customer:** *US-007*</span></span>
    - <span data-ttu-id="3244c-399">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="3244c-399">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="3244c-400">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3244c-400">Select **OK**.</span></span>
1. <span data-ttu-id="3244c-401">Det legges til en ny linje i rutenettet på **Salgsordrelinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="3244c-401">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="3244c-402">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="3244c-402">Set the following values:</span></span>

    - <span data-ttu-id="3244c-403">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="3244c-403">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="3244c-404">**Antall:** *8*</span><span class="sxs-lookup"><span data-stu-id="3244c-404">**Quantity:** *8*</span></span>

1. <span data-ttu-id="3244c-405">Følg disse trinnene for reservere lager for salgslinjen:</span><span class="sxs-lookup"><span data-stu-id="3244c-405">Follow these steps to reserve inventory for the sales line:</span></span>

    1. <span data-ttu-id="3244c-406">På **Salgsordrelinjer**-fanen, på **Beholdning**-menyen, velger du **Reservasjon**.</span><span class="sxs-lookup"><span data-stu-id="3244c-406">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="3244c-407">På **Reservasjon**-siden velger du **Reserver parti**, og deretter lukker du siden.</span><span class="sxs-lookup"><span data-stu-id="3244c-407">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="3244c-408">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3244c-408">Select **Save**.</span></span>

<span data-ttu-id="3244c-409">Fullfør følgende fremgangsmåte for å frigi hver salgsordre til lageret.</span><span class="sxs-lookup"><span data-stu-id="3244c-409">Complete the following procedure to release each sales order to the warehouse.</span></span> <span data-ttu-id="3244c-410">Det opprettes tre forskjellige forsendelser.</span><span class="sxs-lookup"><span data-stu-id="3244c-410">Three different shipments will be created.</span></span> <span data-ttu-id="3244c-411">Deretter legger du til alle de tre leveringer i én ny bølge.</span><span class="sxs-lookup"><span data-stu-id="3244c-411">You will then add all three shipments to one new wave.</span></span>

1. <span data-ttu-id="3244c-412">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="3244c-412">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="3244c-413">I rutenettet velger du første salgsordre du opprettet.</span><span class="sxs-lookup"><span data-stu-id="3244c-413">In the grid, select the first sales order that you created.</span></span>
1. <span data-ttu-id="3244c-414">Velg **Frigi til lager** i fanen **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3244c-414">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="3244c-415">Du mottar en informasjonsmelding som viser bølge-ID og forsendelses-ID som er opprettet.</span><span class="sxs-lookup"><span data-stu-id="3244c-415">You receive an informational message that shows the wave ID and shipment ID that were created.</span></span>

1. <span data-ttu-id="3244c-416">Gjenta de forrige trinnene for å frigi salgsordre 2 og 3 til lageret.</span><span class="sxs-lookup"><span data-stu-id="3244c-416">Repeat the previous steps to release sales orders 2 and 3 to the warehouse.</span></span> <span data-ttu-id="3244c-417">Legg merke til at informasjonsmeldingen du mottar, angir at det er lagt til en forsendelse til bølgen som ble opprettet da du frigav salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="3244c-417">Notice that the informational message that you receive indicates that a shipment has been added to the wave that was created when you released sales order 1.</span></span>
1. <span data-ttu-id="3244c-418">Gå til **Lagerstyring \> Utgående bølger \> Forsendelsesbølger \> Alle bølger**.</span><span class="sxs-lookup"><span data-stu-id="3244c-418">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="3244c-419">Velg bølge-IDen som ble opprettet fra frigivelsen av salgsordrene for å åpne **Bølger**-siden.</span><span class="sxs-lookup"><span data-stu-id="3244c-419">Select the wave ID that was created from the release of the sales orders to open the **Waves** page.</span></span> <span data-ttu-id="3244c-420">Denne siden viser bølgeinformasjon.</span><span class="sxs-lookup"><span data-stu-id="3244c-420">This page shows the wave details.</span></span> <span data-ttu-id="3244c-421">Hurtigfanen **Bølgelinjer** viser forsendelsene som ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="3244c-421">The **Wave lines** FastTab shows the shipments that were created.</span></span>

    <span data-ttu-id="3244c-422">Du må nå opprette arbeid for å hente varer fra plukklokasjonene til sorteringslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="3244c-422">You must now create work to bring items from the picking locations to the sorting location.</span></span>

1. <span data-ttu-id="3244c-423">Klikk på **Prosess** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3244c-423">On the Action Pane, select **Process**.</span></span>

    <span data-ttu-id="3244c-424">Under bølgebehandling vil sorteringsmetoden bruke sorteringsmalen til å tilordne lageret for å sortere posisjoner.</span><span class="sxs-lookup"><span data-stu-id="3244c-424">During wave processing, the sorting method will use the sorting template to assign the inventory to sort positions.</span></span> <span data-ttu-id="3244c-425">Når bølgebehandling er fullført, mottar du en informasjonsmeling som angir at bølgen er postert og arbeidet er opprettet.</span><span class="sxs-lookup"><span data-stu-id="3244c-425">When wave processing is completed, you receive an informational message that states that the wave has been posted and work has been created.</span></span>

1. <span data-ttu-id="3244c-426">I handlingsruten i fanen **Bølge** i gruppen **Relatert informasjon** velger du **Arbeid** for å vise arbeidet som ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="3244c-426">On the Action Pane, on the **Wave** tab, in the **Related information** group, select **Work** to view the work that was created.</span></span> <span data-ttu-id="3244c-427">Noter arbeids-ID-en.</span><span class="sxs-lookup"><span data-stu-id="3244c-427">Make a note of the work ID.</span></span>
1. <span data-ttu-id="3244c-428">Gå til **Lagerstyring \> Pakking og containerbruk \> Posisjonstilordninger for utgående sortering**.</span><span class="sxs-lookup"><span data-stu-id="3244c-428">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="3244c-429">I den venstre kolonnen kan du vise den utgående sorteringsposisjonen som ble opprettet for hver forsendelse.</span><span class="sxs-lookup"><span data-stu-id="3244c-429">In the left column, you can view the outbound sorting position that was created for each shipment.</span></span>
1. <span data-ttu-id="3244c-430">I hurtigfanen **Kriterier for sorteringsposisjon** kan du vise forsendelses-ID for posisjonen.</span><span class="sxs-lookup"><span data-stu-id="3244c-430">On the **Sort position criteria** FastTab, you can view the shipment ID for that position.</span></span>

<span data-ttu-id="3244c-431">Én arbeids-ID er opprettet for å hente lager fra plukklokasjonene til sorteringslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="3244c-431">One work ID has been created to bring inventory from the picking locations to the sorting location.</span></span> <span data-ttu-id="3244c-432">For å fullføre arbeidet trenger du arbeids-IDen som ble opprettet under bølgebehandlingen.</span><span class="sxs-lookup"><span data-stu-id="3244c-432">To complete the work, you will need the work ID that was created during wave processing.</span></span>

### <a name="sales-order-picking-to-the-sorting-location"></a><span data-ttu-id="3244c-433">Salgsordreplukking til sorteringslokasjonen</span><span class="sxs-lookup"><span data-stu-id="3244c-433">Sales order picking to the sorting location</span></span>

1. <span data-ttu-id="3244c-434">Logg på mobilappen som en arbeider i lageret *62*.</span><span class="sxs-lookup"><span data-stu-id="3244c-434">Sign in to the mobile app as a worker in warehouse *62*.</span></span>
1. <span data-ttu-id="3244c-435">I hovedmenyen velger du **Utgående**.</span><span class="sxs-lookup"><span data-stu-id="3244c-435">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="3244c-436">I **Utgående**-menyen velger du **Salgsplukking**.</span><span class="sxs-lookup"><span data-stu-id="3244c-436">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="3244c-437">Velg **ID**-feltet, og angi deretter arbeids-IDen fra bølgebehandlingen.</span><span class="sxs-lookup"><span data-stu-id="3244c-437">Select the **ID** field, and then enter the work ID from the wave processing.</span></span>
1. <span data-ttu-id="3244c-438">Bekreft oppføringen.</span><span class="sxs-lookup"><span data-stu-id="3244c-438">Confirm your entry.</span></span>

    <span data-ttu-id="3244c-439">Deretter blir du bedt om å angi et målnummerskilt (LP).</span><span class="sxs-lookup"><span data-stu-id="3244c-439">Next, you're prompted to enter a target license plate (LP).</span></span> <span data-ttu-id="3244c-440">Legg merke til at linje 1 fra salgsordre 1 må plukkes og legges til målnummerskiltet.</span><span class="sxs-lookup"><span data-stu-id="3244c-440">Notice that line 1 from sales order 1 is what must be picked and added to the target license plate.</span></span> <span data-ttu-id="3244c-441">Varenummeret, antallet, varebeskrivelsen og plukklokasjonen vises.</span><span class="sxs-lookup"><span data-stu-id="3244c-441">The item number, quantity, item description, and pick location are shown.</span></span>

1. <span data-ttu-id="3244c-442">I feltet for **målnummerskilt** angir du målnummerskilt.</span><span class="sxs-lookup"><span data-stu-id="3244c-442">In the **Target LP** field, enter a license plate number.</span></span>

    <span data-ttu-id="3244c-443">Du vil plukke alle linjer som ble opprettet fra den behandlede bølgen, til samme mållisensplate.</span><span class="sxs-lookup"><span data-stu-id="3244c-443">You will pick all lines that were created from the processed wave onto the same target license plate.</span></span>

1. <span data-ttu-id="3244c-444">Bekreft oppføringen.</span><span class="sxs-lookup"><span data-stu-id="3244c-444">Confirm your entry.</span></span>

    <span data-ttu-id="3244c-445">Mobilappen presenterer nå en serie med **Plukk**-sider som peker deg til plukklokasjonen og til varen og antallet som må plukkes.</span><span class="sxs-lookup"><span data-stu-id="3244c-445">The mobile app now presents a series of **Pick** pages that point you to the picking location, and to the item and quantity that must be picked.</span></span> <span data-ttu-id="3244c-446">Når den plukkede varen er lagt til i nummerskiltet, bekrefter du plukkarbeidet.</span><span class="sxs-lookup"><span data-stu-id="3244c-446">After the picked item is added to the license plate, you will confirm the pick work.</span></span> <span data-ttu-id="3244c-447">Den siste siden vil være arbeidet med å sette de plukkede varene inn i sorteringslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="3244c-447">The last page will be the work to put the picked items into the sorting location.</span></span>

1. <span data-ttu-id="3244c-448">Bekreft det første plukkarbeidet.</span><span class="sxs-lookup"><span data-stu-id="3244c-448">Confirm the first pick work.</span></span>
1. <span data-ttu-id="3244c-449">Det neste plukkarbeidet vises.</span><span class="sxs-lookup"><span data-stu-id="3244c-449">The next pick work is shown.</span></span> <span data-ttu-id="3244c-450">Bekreft plukket.</span><span class="sxs-lookup"><span data-stu-id="3244c-450">Confirm the pick.</span></span>
1. <span data-ttu-id="3244c-451">Fortsett med å bekrefte det gjenstående plukkarbeidet.</span><span class="sxs-lookup"><span data-stu-id="3244c-451">Continue to confirm the remaining pick work.</span></span>
1. <span data-ttu-id="3244c-452">Det siste trinnet er å fullføre plasseringsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="3244c-452">The last step is to complete the put work.</span></span> <span data-ttu-id="3244c-453">Bekreft plasseringen til sorteringslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="3244c-453">Confirm the put-away to the sorting location.</span></span>

    <span data-ttu-id="3244c-454">Du mottar en Arbeid fullført-melding.</span><span class="sxs-lookup"><span data-stu-id="3244c-454">You receive a "Work completed" message.</span></span>

1. <span data-ttu-id="3244c-455">Avslutt **Salgsplukking** på mobilappen.</span><span class="sxs-lookup"><span data-stu-id="3244c-455">Exit **Sales Picking** on the mobile app.</span></span>

### <a name="sortingput-to-wall"></a><span data-ttu-id="3244c-456">Sortering/plassering til vegg</span><span class="sxs-lookup"><span data-stu-id="3244c-456">Sorting/put-to-wall</span></span>

<span data-ttu-id="3244c-457">Nå som alt lager er plassert til sorteringslokasjonen, må den sorteres til den riktige sorteringsposisjonen.</span><span class="sxs-lookup"><span data-stu-id="3244c-457">Now that all inventory has been put to the sorting location, it must be sorted to the correct sort position.</span></span>

1. <span data-ttu-id="3244c-458">Logge på mobilappen.</span><span class="sxs-lookup"><span data-stu-id="3244c-458">Sign in to the mobile app.</span></span>
1. <span data-ttu-id="3244c-459">I hovedmenyen velger du **Utgående**.</span><span class="sxs-lookup"><span data-stu-id="3244c-459">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="3244c-460">På menyen **Utgående** velger du **Sortering** for å starte sorteringen av varene.</span><span class="sxs-lookup"><span data-stu-id="3244c-460">On the **Outbound** menu, select **Sort** to start to sort the items.</span></span>
1. <span data-ttu-id="3244c-461">I **LP/CON**-feltet angir du mållisensplaten for det plukkede salgsordrearbeidet.</span><span class="sxs-lookup"><span data-stu-id="3244c-461">In the **LP/CON** field, enter the target license plate of the picked sales order work.</span></span>
1. <span data-ttu-id="3244c-462">Bekreft oppføringen.</span><span class="sxs-lookup"><span data-stu-id="3244c-462">Confirm your entry.</span></span>
1. <span data-ttu-id="3244c-463">Angi varenummeret som skal sorteres først.</span><span class="sxs-lookup"><span data-stu-id="3244c-463">Enter the item number to sort first.</span></span>
1. <span data-ttu-id="3244c-464">Systemet bestemmer den første sorteringsposisjonen som skal vises.</span><span class="sxs-lookup"><span data-stu-id="3244c-464">The system determines the first sort position that should be shown.</span></span> <span data-ttu-id="3244c-465">Bekreft sorteringsposisjonen.</span><span class="sxs-lookup"><span data-stu-id="3244c-465">Confirm the sort position.</span></span>
1. <span data-ttu-id="3244c-466">Du blir bedt om å tilordne en lisensplate til sorteringsposisjonen.</span><span class="sxs-lookup"><span data-stu-id="3244c-466">You're prompted to assign a license plate to the sort position.</span></span> <span data-ttu-id="3244c-467">Velg **LP**-feltet, angi et lisensplatenummer, og bekreft deretter oppføringen.</span><span class="sxs-lookup"><span data-stu-id="3244c-467">Select the **LP** field, enter a license plate number, and then confirm your entry.</span></span>

    <span data-ttu-id="3244c-468">Siden sorteringsposisjonen er knyttet til forsendelses-IDen, skal du sortere de plukkede varene til et nummerskilt som er spesifikt for den utgående forsendelsen og salgsordren.</span><span class="sxs-lookup"><span data-stu-id="3244c-468">Because the sort position is related to the shipment ID, you will sort the picked items into a license plate that is specific to the outbound shipment and sales order.</span></span>

    <span data-ttu-id="3244c-469">Den neste siden viser vare-IDen, antallet, sorteringsposisjons-IDen og "fra"- (plukk) og "til"-nummerskilt-IDene (sortering).</span><span class="sxs-lookup"><span data-stu-id="3244c-469">The next page shows the item ID, quantity, sort position ID, and the "from" (picking) and "to" (sorting) license plate IDs.</span></span> <span data-ttu-id="3244c-470">Informasjonen på denne siden instruerer deg om å sortere den angitte varen og mengdene fra plukkingens nummerskilt til sorteringsnummerskiltet.</span><span class="sxs-lookup"><span data-stu-id="3244c-470">The information on this page instructs you to sort the specified item and quantities from the picking license plate into the sorting license plate.</span></span>

1. <span data-ttu-id="3244c-471">Bekreft sorteringsposisjonen.</span><span class="sxs-lookup"><span data-stu-id="3244c-471">Confirm the sort position.</span></span>
1. <span data-ttu-id="3244c-472">Sorter varene i den første sorteringsposisjonen.</span><span class="sxs-lookup"><span data-stu-id="3244c-472">Sort the items in the first sort position.</span></span> <span data-ttu-id="3244c-473">Når du er ferdig, sender systemet deg til den neste sorteringsposisjonen.</span><span class="sxs-lookup"><span data-stu-id="3244c-473">When you've finished, the system directs you to the next sort position.</span></span>
1. <span data-ttu-id="3244c-474">Gjenta denne prosessen for alle valgte linjer i arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="3244c-474">Repeat this process for all picked lines on the work order.</span></span> <span data-ttu-id="3244c-475">Du bør også bruke denne prosessen når det er flere plukklinjer med samme varenummer.</span><span class="sxs-lookup"><span data-stu-id="3244c-475">You should also use this process when there are multiple pick lines that have the same item number.</span></span>

    <span data-ttu-id="3244c-476">Når du gjentar denne prosessen for alle varer, evaluerer systemet kriteriene fra det neste skannede element (arbeidslinje) og bestemmer hvilken sorteringsposisjon den skal legges til.</span><span class="sxs-lookup"><span data-stu-id="3244c-476">As you repeat this process for all items, the system evaluates the criteria from the next scanned item (work line) and determines which sorting position it should be put to.</span></span> <span data-ttu-id="3244c-477">Du blir automatisk dirigert til å plassere varen til riktig sorteringsposisjon.</span><span class="sxs-lookup"><span data-stu-id="3244c-477">You're automatically directed to put the item to the correct sort position.</span></span> <span data-ttu-id="3244c-478">Avhengig av bekreftelsesoppsettet blir du også dirigert til å bekrefte denne handlingen ved å angi posisjonsnummeret eller nummerskilt-ID-en.</span><span class="sxs-lookup"><span data-stu-id="3244c-478">Depending on the confirmation setup, you're also directed to confirm this action by entering the position number or license plate ID.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3244c-479">Hvis automatisk sortering er aktivert, er ikke manuell overstyring tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="3244c-479">If automatic sorting is turned on, manual override isn't available.</span></span>

1. <span data-ttu-id="3244c-480">Når du er ferdig, åpner du siden **Posisjonstilordninger for utgående sortering** i Microsoft Dynamics 365 Supply Chain Management for å se gjennom statusen for posisjonene.</span><span class="sxs-lookup"><span data-stu-id="3244c-480">When you've finished, in Microsoft Dynamics 365 Supply Chain Management, open the **Outbound sorting position assignments** page to review the status of the positions.</span></span>

    - <span data-ttu-id="3244c-481">Hvis stillingene er lukket automatisk, velger du **Vis lukket** for å vise de lukkede posisjonene.</span><span class="sxs-lookup"><span data-stu-id="3244c-481">If positions are closed automatically, select **Show closed** to show the closed positions.</span></span>
    - <span data-ttu-id="3244c-482">Legg merke til at sorteringsposisjonstransaksjoner vises.</span><span class="sxs-lookup"><span data-stu-id="3244c-482">Notice that sort position transactions are shown.</span></span> <span data-ttu-id="3244c-483">Varen og antallet som ble behandlet via posisjonen, vises.</span><span class="sxs-lookup"><span data-stu-id="3244c-483">The item and quantity that were processed through the position are shown.</span></span>

    <span data-ttu-id="3244c-484">Når du definerer den utgående sorteringsmalen, setter du alternativet **Sorteringsposisjonen automatisk lukking** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="3244c-484">When you set up the outbound sorting template, you set the **Auto close sort position** option to *Yes*.</span></span> <span data-ttu-id="3244c-485">Derfor lukkes stillingen automatisk etter at det siste forventede lageret blir lagt til den.</span><span class="sxs-lookup"><span data-stu-id="3244c-485">Therefore, the position is automatically closed after the last expected inventory is put to it.</span></span> <span data-ttu-id="3244c-486">Sorteringsposisjonene er i **Lukket**-status, og arbeidet er opprettet for å flytte det sorterte lageret til *Rampedør*-lokasjon.</span><span class="sxs-lookup"><span data-stu-id="3244c-486">The sort positions are in **Closed** status, and work has been created to move the sorted inventory to *Baydoor* location.</span></span>

1. <span data-ttu-id="3244c-487">Fullfør det sorterte lagerplukkingsarbeidet for å flytte lageret til forsendelsesstedet.</span><span class="sxs-lookup"><span data-stu-id="3244c-487">Complete the sorted inventory picking work to move the inventory to the shipping location.</span></span> <span data-ttu-id="3244c-488">Når lageret er klart, bekrefter du sending.</span><span class="sxs-lookup"><span data-stu-id="3244c-488">When the inventory is ready, ship-confirm it.</span></span>

> [!NOTE]
> <span data-ttu-id="3244c-489">For sortert lagerplukkingsarbeid skal behandles på rett måte, må et mobilenhetsmenyelement med arbeidsklasse-ID der feltet **Arbeidsordretype** er satt til *Sortert lagerplukking*, brukes til flyttings- og innlastingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="3244c-489">For sorted inventory picking work to be processed correctly, a mobile device menu item that has a work class ID where the **Work order type** field is set to *Sorted inventory picking* should be used for the movement and loading process.</span></span>

### <a name="manually-close-a-position-optional"></a><span data-ttu-id="3244c-490">Lukke en stilling manuelt (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="3244c-490">Manually close a position (optional)</span></span>

<span data-ttu-id="3244c-491">Hvis sorteringsposisjoner skal lukkes manuelt, må alternativet **Sorteringsposisjonen automatisk lukking** for den utgående sorteringsmalen settes til *Nei*, og det må gjøres en lukking før lageret kan flyttes til rampedøren.</span><span class="sxs-lookup"><span data-stu-id="3244c-491">If sort positions should be closed manually, the **Auto close sort position** option for the outbound sorting template must be set to *No*, and closing must be done before inventory can be moved to the bay door area.</span></span> <span data-ttu-id="3244c-492">Stillinger kan lukkes på forskjellige måter:</span><span class="sxs-lookup"><span data-stu-id="3244c-492">Positions can be closed in various ways:</span></span>

- <span data-ttu-id="3244c-493">Via lagerappen:</span><span class="sxs-lookup"><span data-stu-id="3244c-493">Via the warehouse app:</span></span>

    - <span data-ttu-id="3244c-494">Brukeren kan skanne én av varene som allerede finnes på posisjonen, og deretter velge **Lukk** for å lukke posisjonen.</span><span class="sxs-lookup"><span data-stu-id="3244c-494">The user can scan one of the items that are already on the position and then select **Close** to close the position.</span></span>
    - <span data-ttu-id="3244c-495">Hvis brukeren skanner en container som allerede er sortert container, vises det en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="3244c-495">If the user scans a container that has already been sorted container, an error message is shown.</span></span> <span data-ttu-id="3244c-496">Brukeren kan imidlertid fremdeles fortsette å lukke posisjonen.</span><span class="sxs-lookup"><span data-stu-id="3244c-496">However, the user can still continue to close the position.</span></span>

- <span data-ttu-id="3244c-497">Fra Microsoft Dynamics 365 Supply Chain Management siden **Posisjonstilordninger for utgående sortering**:</span><span class="sxs-lookup"><span data-stu-id="3244c-497">From the Microsoft Dynamics 365 Supply Chain Management **Outbound sorting position assignments** page:</span></span>

    - <span data-ttu-id="3244c-498">Brukeren kan velge den utgående sorteringsposisjonsposten og deretter velge **Lukk posisjon** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3244c-498">The user can select the outbound sorting position record and then select **Close position** on the Action Pane.</span></span>

## <a name="tips"></a><span data-ttu-id="3244c-499">Tips!</span><span class="sxs-lookup"><span data-stu-id="3244c-499">Tips</span></span>

- <span data-ttu-id="3244c-500">Varer kan ikke flyttes mellom posisjoner etter at de er tilordnet til en posisjon.</span><span class="sxs-lookup"><span data-stu-id="3244c-500">Items can't be moved between positions after they have been assigned to one.</span></span> <span data-ttu-id="3244c-501">Systemet evaluerer hvor mange av hver vare som skal gå til en bestemt posisjon.</span><span class="sxs-lookup"><span data-stu-id="3244c-501">The system evaluates how many of each item should go to a specific position.</span></span>
- <span data-ttu-id="3244c-502">Sorteringsmal kan konfigureres til å opprette containere automatisk når posisjoner er lukket.</span><span class="sxs-lookup"><span data-stu-id="3244c-502">Sorts template can be configured to automatically create containers when positions are closed.</span></span> <span data-ttu-id="3244c-503">Denne fremgangsmåten vil opprette en standard container-ID-struktur som er basert på den angitte pakkeprofilen.</span><span class="sxs-lookup"><span data-stu-id="3244c-503">This approach will create standard container ID structure that is based on the specified packing profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3244c-504">Etter at bevegelsesarbeidet er opprettet fra sorteringslokasjonen, må du ikke avbryte arbeidet.</span><span class="sxs-lookup"><span data-stu-id="3244c-504">After movement work has been created from the sorting location, you must not cancel the work.</span></span> <span data-ttu-id="3244c-505">Hvis ikke blir posisjonen og containerne i den slettet fra systemet og vil ikke være tilgjengelig for videre behandling.</span><span class="sxs-lookup"><span data-stu-id="3244c-505">Otherwise, the position and the containers in it will be deleted from the system and unavailable for further processing.</span></span> <span data-ttu-id="3244c-506">Beholdningen blir også fjernet.</span><span class="sxs-lookup"><span data-stu-id="3244c-506">The inventory will also be removed.</span></span>
