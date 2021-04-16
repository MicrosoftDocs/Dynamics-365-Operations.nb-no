---
title: Utgående sortering
description: Dette emnet inneholder informasjon om utgående sortering. Denne funksjonaliteten gjør det enklere å håndtere små containere og hjelper lagerarbeidere å planlegge og organisere pallkapasitet på lastebilen.
author: Mirzaab
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3c576209a86f776ac424f7fb9f2b606bea774a67
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828400"
---
# <a name="outbound-sorting"></a><span data-ttu-id="dd421-104">Utgående sortering</span><span class="sxs-lookup"><span data-stu-id="dd421-104">Outbound sorting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd421-105">Denne funksjonaliteten gjør det enklere å håndtere små containere og hjelper lagerarbeidere å planlegge og organisere pallkapasitet på lastebilen.</span><span class="sxs-lookup"><span data-stu-id="dd421-105">This functionality makes it easier to handle small containers and helps warehouse workers better plan and organize pallet capacity in the truck.</span></span> <span data-ttu-id="dd421-106">Når du bruker utgående sortering, kan du sortere pakkede containere til riktig pall etter at de har vært på en pakkestasjon.</span><span class="sxs-lookup"><span data-stu-id="dd421-106">When you use outbound sorting, you can sort packed containers to the correct pallet after they have been at a packing station.</span></span> <span data-ttu-id="dd421-107">Du kan også bygge et emballasjehierarki.</span><span class="sxs-lookup"><span data-stu-id="dd421-107">You can also build a packing hierarchy.</span></span>

<span data-ttu-id="dd421-108">Med denne funksjonaliteten kan du bygge paller fra containere som er pakket gjennom pakkefunksjonaliteten.</span><span class="sxs-lookup"><span data-stu-id="dd421-108">This functionality lets you build pallets from containers that are packed through the packing functionality.</span></span> <span data-ttu-id="dd421-109">Containeren sendes ikke til den endelige forsendelseslokasjonen, fordi den er i den opprinnelige pakkeflyten.</span><span class="sxs-lookup"><span data-stu-id="dd421-109">The container isn't sent to the final shipping location as it is in the original packing flow.</span></span> <span data-ttu-id="dd421-110">I stedet kan arbeidere lukke containeren og flytte den til en sorteringstypeplassering.</span><span class="sxs-lookup"><span data-stu-id="dd421-110">Instead, workers can close the container and move it to a sort type location.</span></span> <span data-ttu-id="dd421-111">De kan deretter sortere containere til plasseringer, der hver har et nummerskilt (LP).</span><span class="sxs-lookup"><span data-stu-id="dd421-111">They can then sort containers to positions, each of which has a license plate (LP).</span></span> <span data-ttu-id="dd421-112">Når containerne er sortert, kan det opprettes arbeid for å sende hele nummerskiltet til endelig forsendelsessone eller endelige stadielokasjoner basert på lokasjonsdirektiver eller dine egne behov.</span><span class="sxs-lookup"><span data-stu-id="dd421-112">After the containers have been sorted, work can be created to send the whole LP to the final shipping dock or stage locations, based on location directives or your own requirements.</span></span> <span data-ttu-id="dd421-113">I tillegg kan handlingen med å lukke sorteringsposisjonen umiddelbart flytte lageret til den endelige forsendelseslokasjonen og plukke den til ordren.</span><span class="sxs-lookup"><span data-stu-id="dd421-113">Additionally, the action of closing of the sort position can immediately move the inventory to the final shipping location and pick it to the order.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="dd421-114">Aktivere Utgående sortering-funksjonen</span><span class="sxs-lookup"><span data-stu-id="dd421-114">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="dd421-115">Før du kan bruke funksjonen må den være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="dd421-115">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="dd421-116">Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="dd421-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="dd421-117">Funksjonen vises på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="dd421-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="dd421-118">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="dd421-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="dd421-119">**Funksjonsnavn:** *Utgående sortering*</span><span class="sxs-lookup"><span data-stu-id="dd421-119">**Feature name:** *Outbound sorting*</span></span>

## <a name="setup"></a><span data-ttu-id="dd421-120">Installasjon</span><span class="sxs-lookup"><span data-stu-id="dd421-120">Setup</span></span>

<span data-ttu-id="dd421-121">I dette scenariet må du bruke standard **USMF**-demodata og lager *62*.</span><span class="sxs-lookup"><span data-stu-id="dd421-121">For this scenario, you must use standard **USMF** demo data and warehouse *62*.</span></span> <span data-ttu-id="dd421-122">Du må også fullføre oppsettet som er beskrevet i følgende underdeler.</span><span class="sxs-lookup"><span data-stu-id="dd421-122">You must also complete the setup that is described in the following subsections.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="dd421-123">Definere en bølgemal</span><span class="sxs-lookup"><span data-stu-id="dd421-123">Set up a wave template</span></span>

<span data-ttu-id="dd421-124">Dette oppsettet behandler automatisk bølgen og oppretter arbeid når en linje frigis til lageret.</span><span class="sxs-lookup"><span data-stu-id="dd421-124">This setup automatically processes the wave and creates work when a line is released to the warehouse.</span></span>

1. <span data-ttu-id="dd421-125">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.</span><span class="sxs-lookup"><span data-stu-id="dd421-125">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="dd421-126">I mallisten velger du **Lager 62**.</span><span class="sxs-lookup"><span data-stu-id="dd421-126">In the template list, select **Warehouse 62**.</span></span>
1. <span data-ttu-id="dd421-127">I hurtigfanen **Generelt** kontrollerer du at alternativet **Behandle bølge ved frigivelse til lager** er satt til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="dd421-127">On the **General** FastTab, make sure that the **Process wave at release to warehouse** option is set to *Yes*.</span></span>

### <a name="set-up-a-worker"></a><span data-ttu-id="dd421-128">Angi en arbeider</span><span class="sxs-lookup"><span data-stu-id="dd421-128">Set up a worker</span></span>

<span data-ttu-id="dd421-129">Pakkestasjonen regnes som en lokasjon.</span><span class="sxs-lookup"><span data-stu-id="dd421-129">The packing station is considered a location.</span></span> <span data-ttu-id="dd421-130">Lagerarbeidere som logger på pakkestasjonen, ser og fungerer bare på forsendelser og containere som er planlagt ved denne bestemte pakkelokasjonen.</span><span class="sxs-lookup"><span data-stu-id="dd421-130">Warehouse workers who sign in at the packing station see and work on only shipments and containers that are planned at that specific packing location.</span></span> <span data-ttu-id="dd421-131">En bruker som logger på Microsoft Dynamics 365, må konfigureres som en arbeider i Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="dd421-131">A user who signs in to Microsoft Dynamics 365 must be set up as a worker in Warehouse management.</span></span> <span data-ttu-id="dd421-132">Hvis brukerens navn ikke vises i listen over arbeidsbrukere, kan du bruke følgende fremgangsmåte for å legge det til.</span><span class="sxs-lookup"><span data-stu-id="dd421-132">If the user's name doesn't appear in the list of work users, use the following procedure to add it.</span></span>

> [!NOTE]
> <span data-ttu-id="dd421-133">Disse trinnene forutsetter at brukeren allerede finnes i systemet og er knyttet til som en ansatt eller arbeider i **Human Resources**-modulen.</span><span class="sxs-lookup"><span data-stu-id="dd421-133">These steps assume that the user already exists in the system and has been associated as an employee or worker in the **Human Resources** module.</span></span>

1. <span data-ttu-id="dd421-134">Gå til **Lagerstyring \> Oppsett \> Arbeider**.</span><span class="sxs-lookup"><span data-stu-id="dd421-134">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="dd421-135">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="dd421-135">Select **New**.</span></span>
1. <span data-ttu-id="dd421-136">I **Arbeider**-feltet velger du målbrukeren i listen over ansatte.</span><span class="sxs-lookup"><span data-stu-id="dd421-136">In the **Worker** field, select the target user in the list of employees.</span></span>
1. <span data-ttu-id="dd421-137">Velg **Velg**.</span><span class="sxs-lookup"><span data-stu-id="dd421-137">Select **Select**.</span></span>
1. <span data-ttu-id="dd421-138">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dd421-138">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="dd421-139">I hurtigfanen **Brukere** velger du **Ny** for å opprette en konto for en mobilenhet, og angi følgende verdier for den:</span><span class="sxs-lookup"><span data-stu-id="dd421-139">On the **Users** FastTab, select **New** to create a mobile device account, and set the following values for it:</span></span>

    - <span data-ttu-id="dd421-140">**Bruker-ID:** Angi en unik ID.</span><span class="sxs-lookup"><span data-stu-id="dd421-140">**User ID:** Enter a unique ID.</span></span>
    - <span data-ttu-id="dd421-141">**Brukernavn:** Angi et navn på ID-en.</span><span class="sxs-lookup"><span data-stu-id="dd421-141">**User name:** Enter a name for the ID.</span></span>
    - <span data-ttu-id="dd421-142">**Standardlager:** *62*</span><span class="sxs-lookup"><span data-stu-id="dd421-142">**Default warehouse:** *62*</span></span>
    - <span data-ttu-id="dd421-143">**Menynavn:** *Hoved*</span><span class="sxs-lookup"><span data-stu-id="dd421-143">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="dd421-144">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dd421-144">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="dd421-145">Dialogboksen **Angi passord** vises, der du kan opprette et enkelt passord som brukeren kan bruke til å logge på mobilappen.</span><span class="sxs-lookup"><span data-stu-id="dd421-145">The **Set password** dialog box appears, where you can create a simple password that the user can use to sign in to the mobile app.</span></span> <span data-ttu-id="dd421-146">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="dd421-146">Set the following values:</span></span>

    - <span data-ttu-id="dd421-147">**Passord:** Angi et enkelt passord.</span><span class="sxs-lookup"><span data-stu-id="dd421-147">**Password:** Enter a simple password.</span></span>
    - <span data-ttu-id="dd421-148">**Bekreft passord:** Skriv inn det samme passordet på nytt.</span><span class="sxs-lookup"><span data-stu-id="dd421-148">**Confirm password:** Enter the same password again.</span></span>

1. <span data-ttu-id="dd421-149">Velg **Angi passord**.</span><span class="sxs-lookup"><span data-stu-id="dd421-149">Select **Set password**.</span></span>

    <span data-ttu-id="dd421-150">Et varsel i Handlingssenteret informerer deg om at passordet er angitt for brukeren du opprettet.</span><span class="sxs-lookup"><span data-stu-id="dd421-150">A notification in the Action Center informs you that the password has been set for the user that you created.</span></span>

### <a name="create-a-location-type"></a><span data-ttu-id="dd421-151">Opprette en lokasjonstype</span><span class="sxs-lookup"><span data-stu-id="dd421-151">Create a location type</span></span>

1. <span data-ttu-id="dd421-152">Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonstyper**.</span><span class="sxs-lookup"><span data-stu-id="dd421-152">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="dd421-153">I handlingsruten velger du **Ny** for å opprette en lokasjonstype, og deretter angir du følgende verdier for den:</span><span class="sxs-lookup"><span data-stu-id="dd421-153">On the Action Pane, select **New** to create a location type, and set the following values for it:</span></span>

    - <span data-ttu-id="dd421-154">**Plasseringstype:** *SORTER*</span><span class="sxs-lookup"><span data-stu-id="dd421-154">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="dd421-155">**Beskrivelse:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="dd421-155">**Description:** *Sort*</span></span>

1. <span data-ttu-id="dd421-156">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dd421-156">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="dd421-157">Definere lagerstyringsparametere</span><span class="sxs-lookup"><span data-stu-id="dd421-157">Set up Warehouse management parameters</span></span>

1. <span data-ttu-id="dd421-158">Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.</span><span class="sxs-lookup"><span data-stu-id="dd421-158">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="dd421-159">I fanen **Generelt** i hurtigfanen **Lokasjonstyper** angir du feltet for **sorteringslokasjonstype** til *SORTER*.</span><span class="sxs-lookup"><span data-stu-id="dd421-159">On the **General** tab, on the **Location types** FastTab, set the **Sorting location type** field to *SORT*.</span></span>
1. <span data-ttu-id="dd421-160">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dd421-160">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-location-profile"></a><span data-ttu-id="dd421-161">Konfigurere en lokasjonsprofil</span><span class="sxs-lookup"><span data-stu-id="dd421-161">Set up a location profile</span></span>

1. <span data-ttu-id="dd421-162">Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="dd421-162">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="dd421-163">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dd421-163">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dd421-164">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="dd421-164">In the header, set the following values:</span></span>

    - <span data-ttu-id="dd421-165">**Lokasjonsprofil-ID:** *Sortering*</span><span class="sxs-lookup"><span data-stu-id="dd421-165">**Location profile ID:** *Sorting*</span></span>
    - <span data-ttu-id="dd421-166">**Navn:** *Sortering*</span><span class="sxs-lookup"><span data-stu-id="dd421-166">**Name:** *Sorting*</span></span>

1. <span data-ttu-id="dd421-167">Angi følgende verdier i **Generelt**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="dd421-167">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="dd421-168">**Lokasjonsformat:** *ASRB* (Aisle-Rack-Shelf-Bin)</span><span class="sxs-lookup"><span data-stu-id="dd421-168">**Location format:** *ASRB* (Aisle-Rack-Shelf-Bin)</span></span>
    - <span data-ttu-id="dd421-169">**Plasseringstype:** *SORTER*</span><span class="sxs-lookup"><span data-stu-id="dd421-169">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="dd421-170">**Bruk sporing av nummerskilt:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="dd421-170">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="dd421-171">**Tillat kombinerte varer:** *Ja* (når du setter dette alternativet til *Ja*, settes alternativet **Tillat kombinerte lagerpartier** automatisk til *Ja*, og dette kan ikke endres uavhengig av hverandre.)</span><span class="sxs-lookup"><span data-stu-id="dd421-171">**Allow mixed items:** *Yes* (When you set this option to *Yes*, the **Allow mixed inventory batches** option is automatically set to *Yes* and can't be changed independently.)</span></span>

1. <span data-ttu-id="dd421-172">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dd421-172">Select **Save**.</span></span>

### <a name="set-up-a-location"></a><span data-ttu-id="dd421-173">Konfigurere en lokasjon</span><span class="sxs-lookup"><span data-stu-id="dd421-173">Set up a location</span></span>

1. <span data-ttu-id="dd421-174">Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjoner**.</span><span class="sxs-lookup"><span data-stu-id="dd421-174">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="dd421-175">Fjern merket for **Generer kontrollsifre for lokasjon** i hodet.</span><span class="sxs-lookup"><span data-stu-id="dd421-175">In the header, clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="dd421-176">I handlingsruten velger du **Ny** for å opprette en lokasjon, og deretter angir du følgende verdier for den:</span><span class="sxs-lookup"><span data-stu-id="dd421-176">On the Action Pane, select **New** to create a location, and set the following values for it:</span></span>

    - <span data-ttu-id="dd421-177">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="dd421-177">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="dd421-178">**Lokasjon:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="dd421-178">**Location:** *SORT*</span></span>
    - <span data-ttu-id="dd421-179">**Lokasjonsprofil-ID:** *SORTERING*</span><span class="sxs-lookup"><span data-stu-id="dd421-179">**Location profile ID:** *SORTING*</span></span>

1. <span data-ttu-id="dd421-180">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dd421-180">Select **Save**.</span></span>

### <a name="set-up-an-outbound-sorting-template"></a><span data-ttu-id="dd421-181">Definere en utgående sorteringsmal</span><span class="sxs-lookup"><span data-stu-id="dd421-181">Set up an outbound sorting template</span></span>

<span data-ttu-id="dd421-182">Den utgående sorteringsmalen bestemmer om arbeidet skal opprettes fra sorteringslokasjonen, og om sortering skal utføres manuelt eller automatisk.</span><span class="sxs-lookup"><span data-stu-id="dd421-182">The outbound sorting template determines whether work is created out of the sort location, and whether sorting is done manually or automatically.</span></span>

<span data-ttu-id="dd421-183">I dette scenariet skal du opprette en utgående sorteringsmal for å bygge paller etter pakkstasjonen.</span><span class="sxs-lookup"><span data-stu-id="dd421-183">For this scenario, you will create an outbound sorting template to build pallets after the packing station.</span></span>

1. <span data-ttu-id="dd421-184">Gå til **Lagerstyring \> Oppsett \> Pakking \> Utgående sorteringsmal**.</span><span class="sxs-lookup"><span data-stu-id="dd421-184">Go to **Warehouse Management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="dd421-185">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dd421-185">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dd421-186">I toppteksten på den nye malen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="dd421-186">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="dd421-187">**ID for utgående sorteringsmal:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="dd421-187">**Outbound sorting template ID:** *AutoWork*</span></span>
    - <span data-ttu-id="dd421-188">**Beskrivelse:** *Opprettelse av automatisk arbeid*</span><span class="sxs-lookup"><span data-stu-id="dd421-188">**Description:** *Auto Work Creation*</span></span>
    - <span data-ttu-id="dd421-189">**Type utgående sorteringsmal:** *Container*</span><span class="sxs-lookup"><span data-stu-id="dd421-189">**Outbound sorting template type:** *Container*</span></span>
    - <span data-ttu-id="dd421-190">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="dd421-190">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="dd421-191">**Lokasjon:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="dd421-191">**Location:** *SORT*</span></span>

1. <span data-ttu-id="dd421-192">Angi følgende verdier i **Generelt**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="dd421-192">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="dd421-193">**Sorteringsbekreftelse:** *Posisjonsskanning*</span><span class="sxs-lookup"><span data-stu-id="dd421-193">**Sort verification:** *Position scan*</span></span>
    - <span data-ttu-id="dd421-194">**Opprett arbeid ved posisjonslukking:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="dd421-194">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="dd421-195">Hvis dette valget settes til *Ja* når posisjonen er lukket, opprettes arbeid for å flytte lageret til den endelige leveringslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="dd421-195">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="dd421-196">Hvis det settes til *Nei*, plukkes lageret umiddelbart til ordren når posisjonen lukkes.</span><span class="sxs-lookup"><span data-stu-id="dd421-196">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="dd421-197">**Stillingstilordning:** *Automatisk*</span><span class="sxs-lookup"><span data-stu-id="dd421-197">**Position assignment:** *Automatic*</span></span>

        <span data-ttu-id="dd421-198">Hvis dette feltet settes til *Manuell*, må brukeren alltid angi hvilken posisjon lageret skal sorteres til.</span><span class="sxs-lookup"><span data-stu-id="dd421-198">If this field is set to *Manual*, the user must always indicate which position the inventory should be sorted to.</span></span> <span data-ttu-id="dd421-199">Hvis det er satt til *Automatisk*, vil systemet automatisk sende lageret til en posisjon automatisk når det er mulig, basert på inndelingene i sorteringsmalen.</span><span class="sxs-lookup"><span data-stu-id="dd421-199">If it's set to *Automatic*, the system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

1. <span data-ttu-id="dd421-200">Velg **Lagre** for å gjøre **Rediger spørring**-knappen på handlingsruten tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="dd421-200">Select **Save** to make the **Edit query** button on the Action Pane available.</span></span>
1. <span data-ttu-id="dd421-201">I handlingsruten velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="dd421-201">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="dd421-202">I redigeringsprogrammet i fanen **Sortering** legger du til en linje med følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="dd421-202">In the query editor, on the **Sorting** tab, add a line that has the following values:</span></span>

    - <span data-ttu-id="dd421-203">**Tabell:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="dd421-203">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="dd421-204">**Avledet tabell:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="dd421-204">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="dd421-205">**Felt:** *Transportørtjeneste*</span><span class="sxs-lookup"><span data-stu-id="dd421-205">**Field:** *Carrier service*</span></span>

        <span data-ttu-id="dd421-206">Når du har valgt denne verdien, kan du få følgende melding: Feltet Transportørtjeneste er ikke et indeksfelt.</span><span class="sxs-lookup"><span data-stu-id="dd421-206">When you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="dd421-207">Vil du legge til sortering på dette?</span><span class="sxs-lookup"><span data-stu-id="dd421-207">Do you want to add sorting on this?"</span></span> <span data-ttu-id="dd421-208">Velg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="dd421-208">Select **Yes**.</span></span>

    - <span data-ttu-id="dd421-209">**Søkeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="dd421-209">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="dd421-210">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-210">Select **OK**.</span></span>
1. <span data-ttu-id="dd421-211">Du kan få følgende melding: "Gruppering vil bli tilbakestilt, vil du fortsette?"</span><span class="sxs-lookup"><span data-stu-id="dd421-211">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="dd421-212">Velg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="dd421-212">Select **Yes**.</span></span>

    <span data-ttu-id="dd421-213">Knappen for **Inndelinger for utgående sortereringmal** i handlingsruten blir tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="dd421-213">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="dd421-214">Velg alternativet for **Inndelinger for utgående sortereringmal** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dd421-214">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="dd421-215">I **Sorteringskriterier for utgående**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="dd421-215">In the **Outbound sorting criteria** dialog box, set the following values:</span></span>

    - <span data-ttu-id="dd421-216">**Referansetabellnavn:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="dd421-216">**Reference table name:** *Shipments*</span></span>
    - <span data-ttu-id="dd421-217">**Referansefeltnavn:** *Transportørtjeneste*</span><span class="sxs-lookup"><span data-stu-id="dd421-217">**Reference field name:** *Carrier service*</span></span>
    - <span data-ttu-id="dd421-218">**Grupper etter-feltet:** Merk av i denne avmerkingsboksen for å gruppere forsendelser etter transportørservice.</span><span class="sxs-lookup"><span data-stu-id="dd421-218">**Group by field:** Select this check box to group shipments by carrier service.</span></span>

1. <span data-ttu-id="dd421-219">Velg **OK** for å lagre innstillingene og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="dd421-219">Select **OK** to save your settings and close the dialog box.</span></span>

### <a name="set-up-container-packing-policies"></a><span data-ttu-id="dd421-220">Definere policyer for containerpakking</span><span class="sxs-lookup"><span data-stu-id="dd421-220">Set up container packing policies</span></span>

1. <span data-ttu-id="dd421-221">Gå til **Lagerstyring \> Oppsett \> Containere \> Policyer for containerpakking**.</span><span class="sxs-lookup"><span data-stu-id="dd421-221">Go to **Warehouse management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="dd421-222">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dd421-222">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dd421-223">I toppteksten på den nye policyen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="dd421-223">In the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="dd421-224">**Policy for containerpakking:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="dd421-224">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="dd421-225">**Beskrivelse:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="dd421-225">**Description:** *Sort*</span></span>

1. <span data-ttu-id="dd421-226">Angi følgende verdier i **Oversikt**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="dd421-226">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="dd421-227">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="dd421-227">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="dd421-228">**Standardlokasjon for sortering:** *SORTER*</span><span class="sxs-lookup"><span data-stu-id="dd421-228">**Default location for sorting:** *SORT*</span></span>
    - <span data-ttu-id="dd421-229">**Vekt/enhet:** *kg*</span><span class="sxs-lookup"><span data-stu-id="dd421-229">**Weight unit:** *kg*</span></span>
    - <span data-ttu-id="dd421-230">**Policy for containerlukking:** *Automatisk frigivelse*</span><span class="sxs-lookup"><span data-stu-id="dd421-230">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="dd421-231">**Policy for containerfrigivelse:** *Tilordne container til utgående sorteringsposisjon*</span><span class="sxs-lookup"><span data-stu-id="dd421-231">**Container release policy:** *Assign container to outbound sorting position*</span></span>

1. <span data-ttu-id="dd421-232">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dd421-232">Select **Save**.</span></span>

### <a name="set-up-packing-profiles"></a><span data-ttu-id="dd421-233">Definere pakkeprofiler</span><span class="sxs-lookup"><span data-stu-id="dd421-233">Set up packing profiles</span></span>

<span data-ttu-id="dd421-234">Opprett en ny pakkeprofil som skal brukes sammen med sorteringsfunksjonen.</span><span class="sxs-lookup"><span data-stu-id="dd421-234">Create a new packing profile that will be used together with the sorting functionality.</span></span>

1. <span data-ttu-id="dd421-235">Gå til **Lagerstyring \> Oppsett \> Pakking \> Pakkeprofiler**.</span><span class="sxs-lookup"><span data-stu-id="dd421-235">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="dd421-236">I handlingsruten velger du **Ny** for å opprette en linje, og deretter angir du følgende verdier for den:</span><span class="sxs-lookup"><span data-stu-id="dd421-236">On the Action Pane, select **New** to create a line, and set the following values for it:</span></span>

    - <span data-ttu-id="dd421-237">**Pakkeprofil-ID:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="dd421-237">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="dd421-238">**Beskrivelse:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="dd421-238">**Description:** *Sort*</span></span>
    - <span data-ttu-id="dd421-239">**Policy for containerpakking:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="dd421-239">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="dd421-240">**Modus for container-ID:** *Automatisk*</span><span class="sxs-lookup"><span data-stu-id="dd421-240">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="dd421-241">**Containertype:** *Boks-Stor*</span><span class="sxs-lookup"><span data-stu-id="dd421-241">**Container type:** *Box-Large*</span></span>
    - <span data-ttu-id="dd421-242">**Opprett container automatisk ved containerlukking:** Fjernet (= *Nei*)</span><span class="sxs-lookup"><span data-stu-id="dd421-242">**Auto create container at container close:** Cleared (= *No*)</span></span>

1. <span data-ttu-id="dd421-243">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dd421-243">Select **Save**.</span></span>

### <a name="set-up-work-classes"></a><span data-ttu-id="dd421-244">Konfigurere arbeidsklasser</span><span class="sxs-lookup"><span data-stu-id="dd421-244">Set up work classes</span></span>

<span data-ttu-id="dd421-245">Definer en arbeidsklasse som skal brukes sammen med sortering.</span><span class="sxs-lookup"><span data-stu-id="dd421-245">Set up a work class that will be used together with sorting.</span></span>

1. <span data-ttu-id="dd421-246">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsklasser**.</span><span class="sxs-lookup"><span data-stu-id="dd421-246">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="dd421-247">I handlingsruten velger du **Ny** for å opprette en arbeidsklasse for sortering, og deretter angir du følgende verdier for den:</span><span class="sxs-lookup"><span data-stu-id="dd421-247">On the Action Pane, select **New** to create a work class for sorting, and set the following values for it:</span></span>

    - <span data-ttu-id="dd421-248">**Arbeidsklasse-ID:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="dd421-248">**Work class ID:** *Sort*</span></span>
    - <span data-ttu-id="dd421-249">**Beskrivelse:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="dd421-249">**Description:** *Sort*</span></span>
    - <span data-ttu-id="dd421-250">**Arbeidsordretype:** *Sortert lagerplukking*</span><span class="sxs-lookup"><span data-stu-id="dd421-250">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="dd421-251">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dd421-251">Select **Save**.</span></span>

### <a name="set-up-mobile-device-menu-items"></a><span data-ttu-id="dd421-252">Definere en mobilenhetsmenyelementer</span><span class="sxs-lookup"><span data-stu-id="dd421-252">Set up mobile device menu items</span></span>

#### <a name="set-up-a-new-pallet-menu-item"></a><span data-ttu-id="dd421-253">Definere et nytt pallemenyelement</span><span class="sxs-lookup"><span data-stu-id="dd421-253">Set up a new pallet menu item</span></span>

<span data-ttu-id="dd421-254">Opprett et menyelement for mobilenhet for å bygge paller under sortering.</span><span class="sxs-lookup"><span data-stu-id="dd421-254">Create a mobile device menu item to build pallets during sorting.</span></span>

1. <span data-ttu-id="dd421-255">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="dd421-255">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="dd421-256">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dd421-256">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dd421-257">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="dd421-257">In the header, set the following values:</span></span>

    - <span data-ttu-id="dd421-258">**Navn på menyelement:** *Palleversjon*</span><span class="sxs-lookup"><span data-stu-id="dd421-258">**Menu item name:** *Pallet build*</span></span>
    - <span data-ttu-id="dd421-259">**Tittel:** *Palleversjon*</span><span class="sxs-lookup"><span data-stu-id="dd421-259">**Title:** *Pallet build*</span></span>
    - <span data-ttu-id="dd421-260">**Modus:** *Indirekte*</span><span class="sxs-lookup"><span data-stu-id="dd421-260">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="dd421-261">**Bruke eksisterende arbeid:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="dd421-261">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="dd421-262">Angi følgende verdier i **Generelt**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="dd421-262">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="dd421-263">**Aktivitetskode:** *Utgående sortering*</span><span class="sxs-lookup"><span data-stu-id="dd421-263">**Activity code:** *Outbound sorting*</span></span>

        <span data-ttu-id="dd421-264">Når dette feltet er satt til *Utgående sortering*, vises feltet **ID for utgående sorteringsmal**.</span><span class="sxs-lookup"><span data-stu-id="dd421-264">When this field is set to *Outbound sorting*, the **Outbound sorting template ID** field is shown.</span></span>

    - <span data-ttu-id="dd421-265">**Bruk prosessveiledning:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="dd421-265">**Use process guide:** *Yes*</span></span>

        <span data-ttu-id="dd421-266">Når feltet **Aktivitetskode** er satt til *Utgående sortering*, settes dette alternativet automatisk til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="dd421-266">When the **Activity code** field is set to *Outbound sorting*, this option is automatically set to *Yes*.</span></span>

    - <span data-ttu-id="dd421-267">**ID for utgående sorteringsmal:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="dd421-267">**Outbound sorting template ID:** *AutoWork*</span></span>

1. <span data-ttu-id="dd421-268">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dd421-268">Select **Save**.</span></span>

#### <a name="set-up-a-new-loading-menu-item"></a><span data-ttu-id="dd421-269">Definere et nytt lastemenyelement</span><span class="sxs-lookup"><span data-stu-id="dd421-269">Set up a new loading menu item</span></span>

<span data-ttu-id="dd421-270">Deretter oppretter du et menyelement som lar brukere flytte de sorterte lagervarene til forsendelseslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="dd421-270">Next, create a menu item that lets users move the sorted inventory items to the shipping location.</span></span>

1. <span data-ttu-id="dd421-271">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="dd421-271">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="dd421-272">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dd421-272">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dd421-273">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="dd421-273">In the header, set the following values:</span></span>

    - <span data-ttu-id="dd421-274">**Navn på menyelement:** *Last fra sortering*</span><span class="sxs-lookup"><span data-stu-id="dd421-274">**Menu item name:** *Load from Sorting*</span></span>
    - <span data-ttu-id="dd421-275">**Tittel:** *Last fra sortering*</span><span class="sxs-lookup"><span data-stu-id="dd421-275">**Title:** *Load from Sorting*</span></span>
    - <span data-ttu-id="dd421-276">**Modus:** *Arbeid*</span><span class="sxs-lookup"><span data-stu-id="dd421-276">**Mode:** *Work*</span></span>
    - <span data-ttu-id="dd421-277">**Bruke eksisterende arbeid:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="dd421-277">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="dd421-278">På **Generelt**-hurtigfanen settes **Styrt av**-feltet til *Brukerstyrt*.</span><span class="sxs-lookup"><span data-stu-id="dd421-278">On the **General** FastTab, set the **Directed by** field to *User directed*.</span></span>
1. <span data-ttu-id="dd421-279">På hurtigfanen **Arbeidsklasser** velger du **Ny**, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="dd421-279">On the **Work classes** FastTab, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="dd421-280">**Arbeidsklasse-ID:** *SORTER*</span><span class="sxs-lookup"><span data-stu-id="dd421-280">**Work class ID:** *SORT*</span></span>
    - <span data-ttu-id="dd421-281">**Arbeidsordretype:** *Sortert lagerplukking*</span><span class="sxs-lookup"><span data-stu-id="dd421-281">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="dd421-282">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dd421-282">Select **Save**.</span></span>

### <a name="set-up-the-mobile-device-menu"></a><span data-ttu-id="dd421-283">Definere mobilenhetsmeny</span><span class="sxs-lookup"><span data-stu-id="dd421-283">Set up the mobile device menu</span></span>

<span data-ttu-id="dd421-284">Du må nå legge til de nye menyelementene på mobilenhetsmenyen.</span><span class="sxs-lookup"><span data-stu-id="dd421-284">You must now add the new menu items to the mobile device menu.</span></span>

1. <span data-ttu-id="dd421-285">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="dd421-285">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="dd421-286">Velg **Utgående**-menyen.</span><span class="sxs-lookup"><span data-stu-id="dd421-286">Select the **Outbound** menu.</span></span>
1. <span data-ttu-id="dd421-287">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="dd421-287">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="dd421-288">I kolonnen **Tilgjengelige menyer og menyelementer** finner og velger du **Palleversjon**.</span><span class="sxs-lookup"><span data-stu-id="dd421-288">In the **Available menus and menu items** column, find and select **Pallet build**.</span></span>
1. <span data-ttu-id="dd421-289">Velg høyre pil-knappen for å flytte **Palleversjon** til kolonnen **Menystruktur**.</span><span class="sxs-lookup"><span data-stu-id="dd421-289">Select the right arrow button to move **Pallet build** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="dd421-290">Bruk pil opp og pil ned for å plassere menyelementet **Palleversjon** i ønsket posisjon på mobilenhetmenyen.</span><span class="sxs-lookup"><span data-stu-id="dd421-290">Use the up arrow and down arrow buttons to put the **Pallet build** menu item in the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="dd421-291">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dd421-291">Select **Save**.</span></span>
1. <span data-ttu-id="dd421-292">Gjenta denne fremgangsmåten for å legge til menyen **Last fra sortering** på **Utgående**-menyen.</span><span class="sxs-lookup"><span data-stu-id="dd421-292">Repeat this procedure to add the **Load from Sorting** menu item to the **Outbound** menu.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="dd421-293">Konfigurer lokasjonsdirektiver</span><span class="sxs-lookup"><span data-stu-id="dd421-293">Set up location directives</span></span>

<span data-ttu-id="dd421-294">*Lokasjonsdirektiver* er regler som bidrar til å identifisere plukke- og plasseringslokasjoner for lagerbevegelse.</span><span class="sxs-lookup"><span data-stu-id="dd421-294">*Location directives* are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="dd421-295">Du må nå opprette en regel for å behandle sorteringsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="dd421-295">You must now create a rule to manage the sorting work.</span></span>

#### <a name="set-up-a-single-sku-directive"></a><span data-ttu-id="dd421-296">Definere et enkelt-SKU-direktiv</span><span class="sxs-lookup"><span data-stu-id="dd421-296">Set up a single-SKU directive</span></span>

1. <span data-ttu-id="dd421-297">Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.</span><span class="sxs-lookup"><span data-stu-id="dd421-297">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="dd421-298">I venstre rute endrer du verdien på feltet **Arbeidsordretype** til *Sortert lagerplukking*.</span><span class="sxs-lookup"><span data-stu-id="dd421-298">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="dd421-299">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dd421-299">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dd421-300">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="dd421-300">In the header, set the following values:</span></span>

    - <span data-ttu-id="dd421-301">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="dd421-301">**Sequence:** *1*</span></span>
    - <span data-ttu-id="dd421-302">**Navn:** *Rampedør*</span><span class="sxs-lookup"><span data-stu-id="dd421-302">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="dd421-303">Angi følgende verdier i **Lokasjonsdirektiver**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="dd421-303">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="dd421-304">**Arbeidstype:** *Plasser*</span><span class="sxs-lookup"><span data-stu-id="dd421-304">**Work type:** *Put*</span></span>
    - <span data-ttu-id="dd421-305">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="dd421-305">**Site:** *6*</span></span>
    - <span data-ttu-id="dd421-306">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="dd421-306">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="dd421-307">**Flere SKUer:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="dd421-307">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="dd421-308">Velg **Lagre** for å gjøre verktøylinjen på **Linjer**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="dd421-308">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="dd421-309">På hurtigfanen **Linjer** velger du **Ny**, og angi deretter følgende verdier på den nye linjen:</span><span class="sxs-lookup"><span data-stu-id="dd421-309">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="dd421-310">Godta standardverdiene for alle de andre feltene.</span><span class="sxs-lookup"><span data-stu-id="dd421-310">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="dd421-311">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="dd421-311">**Sequence:** *1*</span></span>
    - <span data-ttu-id="dd421-312">**Fra:** *0*</span><span class="sxs-lookup"><span data-stu-id="dd421-312">**From:** *0*</span></span>
    - <span data-ttu-id="dd421-313">**Til:** *1,000,000*</span><span class="sxs-lookup"><span data-stu-id="dd421-313">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="dd421-314">Velg **Lagre** for å gjøre verktøylinjen på **Handlinger for lokasjonsdirektiv**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="dd421-314">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="dd421-315">På hurtigfanen **Handlinger for lokasjonsdirektiv** velger du **Ny**, og angi deretter følgende verdier på den nye linjen:</span><span class="sxs-lookup"><span data-stu-id="dd421-315">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="dd421-316">Godta standardverdiene for alle de andre feltene.</span><span class="sxs-lookup"><span data-stu-id="dd421-316">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="dd421-317">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="dd421-317">**Sequence:** *1*</span></span>
    - <span data-ttu-id="dd421-318">**Navn:** *Rampedør*</span><span class="sxs-lookup"><span data-stu-id="dd421-318">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="dd421-319">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dd421-319">Select **Save**.</span></span>
1. <span data-ttu-id="dd421-320">I **Handlinger for lokasjonsdirektiv**-hurtigfanen velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="dd421-320">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="dd421-321">I redigeringsprogrammet for spørring, i fanen **Område**, finner du raden der feltet **Felt** er satt til *Lokasjon*.</span><span class="sxs-lookup"><span data-stu-id="dd421-321">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="dd421-322">Sett **Vilkår**-feltet for denne raden til *Rampedør*.</span><span class="sxs-lookup"><span data-stu-id="dd421-322">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="dd421-323">Velg **OK** for å lagre innstillingene og lukke redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="dd421-323">Select **OK** to save your settings and close the query editor.</span></span>

#### <a name="set-up-a-multiple-sku-directive"></a><span data-ttu-id="dd421-324">Definere et flere-SKU-direktiv</span><span class="sxs-lookup"><span data-stu-id="dd421-324">Set up a multiple-SKU directive</span></span>

1. <span data-ttu-id="dd421-325">Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.</span><span class="sxs-lookup"><span data-stu-id="dd421-325">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="dd421-326">I venstre rute endrer du verdien på feltet **Arbeidsordretype** til *Sortert lagerplukking*.</span><span class="sxs-lookup"><span data-stu-id="dd421-326">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="dd421-327">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dd421-327">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dd421-328">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="dd421-328">In the header, set the following values:</span></span>

    - <span data-ttu-id="dd421-329">**Sekvens:** *2*</span><span class="sxs-lookup"><span data-stu-id="dd421-329">**Sequence:** *2*</span></span>
    - <span data-ttu-id="dd421-330">**Navn:** *Rampedør, flere*</span><span class="sxs-lookup"><span data-stu-id="dd421-330">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="dd421-331">Angi følgende verdier i **Lokasjonsdirektiver**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="dd421-331">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="dd421-332">**Arbeidstype:** *Plasser*</span><span class="sxs-lookup"><span data-stu-id="dd421-332">**Work type:** *Put*</span></span>
    - <span data-ttu-id="dd421-333">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="dd421-333">**Site:** *6*</span></span>
    - <span data-ttu-id="dd421-334">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="dd421-334">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="dd421-335">**Flere SKUer:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="dd421-335">**Multiple SKU:** *Yes*</span></span>

1. <span data-ttu-id="dd421-336">Velg **Lagre** for å gjøre verktøylinjen på **Linjer**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="dd421-336">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="dd421-337">På hurtigfanen **Linjer** velger du **Ny**, og angi deretter følgende verdier på den nye linjen:</span><span class="sxs-lookup"><span data-stu-id="dd421-337">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="dd421-338">Godta standardverdiene for alle de andre feltene.</span><span class="sxs-lookup"><span data-stu-id="dd421-338">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="dd421-339">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="dd421-339">**Sequence:** *1*</span></span>
    - <span data-ttu-id="dd421-340">**Fra:** *0*</span><span class="sxs-lookup"><span data-stu-id="dd421-340">**From:** *0*</span></span>
    - <span data-ttu-id="dd421-341">**Til:** *1,000,000*</span><span class="sxs-lookup"><span data-stu-id="dd421-341">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="dd421-342">Velg **Lagre** for å gjøre verktøylinjen på **Handlinger for lokasjonsdirektiv**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="dd421-342">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="dd421-343">På hurtigfanen **Handlinger for lokasjonsdirektiv** velger du **Ny**, og angi deretter følgende verdier på den nye linjen:</span><span class="sxs-lookup"><span data-stu-id="dd421-343">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="dd421-344">Godta standardverdiene for alle de andre feltene.</span><span class="sxs-lookup"><span data-stu-id="dd421-344">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="dd421-345">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="dd421-345">**Sequence:** *1*</span></span>
    - <span data-ttu-id="dd421-346">**Navn:** *Rampedør, flere*</span><span class="sxs-lookup"><span data-stu-id="dd421-346">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="dd421-347">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dd421-347">Select **Save**.</span></span>
1. <span data-ttu-id="dd421-348">I **Handlinger for lokasjonsdirektiv**-hurtigfanen velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="dd421-348">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="dd421-349">I redigeringsprogrammet for spørring, i fanen **Område**, finner du raden der feltet **Felt** er satt til *Lokasjon*.</span><span class="sxs-lookup"><span data-stu-id="dd421-349">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="dd421-350">Sett **Vilkår**-feltet for denne raden til *Rampedør*.</span><span class="sxs-lookup"><span data-stu-id="dd421-350">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="dd421-351">Velg **OK** for å lagre innstillingene og lukke redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="dd421-351">Select **OK** to save your settings and close the query editor.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="dd421-352">Konfigurer arbeidsmaler</span><span class="sxs-lookup"><span data-stu-id="dd421-352">Set up work templates</span></span>

1. <span data-ttu-id="dd421-353">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.</span><span class="sxs-lookup"><span data-stu-id="dd421-353">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="dd421-354">Endre verdien på feltet **Arbeidsordretype** til *Sortert lagerplukking*.</span><span class="sxs-lookup"><span data-stu-id="dd421-354">Change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="dd421-355">I handlingsruten velger du **Ny** for å opprette en arbeidsmal.</span><span class="sxs-lookup"><span data-stu-id="dd421-355">On the Action Pane, select **New** to create a work template.</span></span>
1. <span data-ttu-id="dd421-356">Angi følgende verdier i fanen **Oversikt**:</span><span class="sxs-lookup"><span data-stu-id="dd421-356">On the **Overview** tab, set the following values:</span></span>

    - <span data-ttu-id="dd421-357">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="dd421-357">**Sequence:** *1*</span></span>
    - <span data-ttu-id="dd421-358">**Arbeidsmal:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="dd421-358">**Work template:** *Sort*</span></span>
    - <span data-ttu-id="dd421-359">**Beskrivelse av arbeidsmal:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="dd421-359">**Work template description:** *Sort*</span></span>

1. <span data-ttu-id="dd421-360">Velg **Lagre** for å gjøre **Arbeidsmaldetaljer**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="dd421-360">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="dd421-361">På **Arbeidsmaldetaljer**-hurtigfanen velger du **Ny** for å legge til en linje, og angi deretter følgende verdier for den:</span><span class="sxs-lookup"><span data-stu-id="dd421-361">On the **Work Template Details** FastTab, select **New** to add a line, and then set the following values for it:</span></span>

    - <span data-ttu-id="dd421-362">**Arbeidstype:** *Plukk*</span><span class="sxs-lookup"><span data-stu-id="dd421-362">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="dd421-363">**Arbeidsklasse-ID:** *SORTER*</span><span class="sxs-lookup"><span data-stu-id="dd421-363">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="dd421-364">Velg **Ny** på nytt for å legge til en ny linje, og angi deretter følgende verdier for den:</span><span class="sxs-lookup"><span data-stu-id="dd421-364">Select **New** again to add a second line, and then set the following values for it:</span></span>

    - <span data-ttu-id="dd421-365">**Arbeidstype:** *Plasser*</span><span class="sxs-lookup"><span data-stu-id="dd421-365">**Work type:** *Put*</span></span>
    - <span data-ttu-id="dd421-366">**Arbeidsklasse-ID:** *SORTER*</span><span class="sxs-lookup"><span data-stu-id="dd421-366">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="dd421-367">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dd421-367">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="dd421-368">Scenario</span><span class="sxs-lookup"><span data-stu-id="dd421-368">Scenario</span></span>

<span data-ttu-id="dd421-369">Dette scenariet simulerer en situasjon der pakkede containere automatisk skal sorteres til forskjellige posisjoner (paller) etter pakkestasjonen, avhengig av transportørtjenesten.</span><span class="sxs-lookup"><span data-stu-id="dd421-369">This scenario simulates a situation where packed containers should automatically be sorted to different positions (pallets) after the packing station, depending on the shipping carrier service.</span></span> <span data-ttu-id="dd421-370">Etter at alle varer fra lasten er pakket og sortert etter adresse, flyttes pallene til rampedøren.</span><span class="sxs-lookup"><span data-stu-id="dd421-370">After all items from the load are packed and sorted by address, the pallets will be moved to the bay door.</span></span>

### <a name="create-sales-orders-and-picking-work"></a><span data-ttu-id="dd421-371">Opprette salgsordrer og plukkarbeid</span><span class="sxs-lookup"><span data-stu-id="dd421-371">Create sales orders and picking work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="dd421-372">Opprett salgsordre 1</span><span class="sxs-lookup"><span data-stu-id="dd421-372">Create sales order 1</span></span>

1. <span data-ttu-id="dd421-373">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="dd421-373">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="dd421-374">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dd421-374">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dd421-375">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="dd421-375">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="dd421-376">**Kundekonto:** *US-005*</span><span class="sxs-lookup"><span data-stu-id="dd421-376">**Customer account:** *US-005*</span></span>
    - <span data-ttu-id="dd421-377">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="dd421-377">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="dd421-378">Velg **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="dd421-378">Select **OK** to close the dialog box.</span></span>

    <span data-ttu-id="dd421-379">Den nye salgsordren åpnes.</span><span class="sxs-lookup"><span data-stu-id="dd421-379">The new sales order is opened.</span></span>

1. <span data-ttu-id="dd421-380">Bytt til **Topptekst**-visningen.</span><span class="sxs-lookup"><span data-stu-id="dd421-380">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="dd421-381">På **Levering**-hurtigfanen, i **Transport**-inndelingen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="dd421-381">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="dd421-382">**Transportør:** *Luftlast*</span><span class="sxs-lookup"><span data-stu-id="dd421-382">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="dd421-383">**Transportørtjeneste:** *Lufttransport*</span><span class="sxs-lookup"><span data-stu-id="dd421-383">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="dd421-384">Gå til **Linjer**-visningen.</span><span class="sxs-lookup"><span data-stu-id="dd421-384">Switch to the **Lines** view.</span></span>
1. <span data-ttu-id="dd421-385">Hvis en ny, tom linje ikke automatisk legges til i rutenettet i **Salgsordrelinjer**-hurtigfanen, velger du **Legg til linje** for å legge til en linje.</span><span class="sxs-lookup"><span data-stu-id="dd421-385">If a new, empty line isn't automatically added to the grid on the **Sales order lines** FastTab, select **Add line** to add one.</span></span>
1. <span data-ttu-id="dd421-386">Angi følgende verdier på den nye ordrelinjen:</span><span class="sxs-lookup"><span data-stu-id="dd421-386">On the new order line, set the following values:</span></span>

    - <span data-ttu-id="dd421-387">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="dd421-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="dd421-388">**Antall:** *2*</span><span class="sxs-lookup"><span data-stu-id="dd421-388">**Quantity:** *2*</span></span>

1. <span data-ttu-id="dd421-389">Mens den nye ordrelinjen fremdeles er valgt på hurtigfanen **Salgsordrelinjer**, velger du **Reservasjon** på menyen **Lager**.</span><span class="sxs-lookup"><span data-stu-id="dd421-389">While the new order line is still selected on the **Sales order lines** FastTab, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="dd421-390">På **Reservasjon**-siden velger du **Reserver parti** for å reservere det fulle antallet på den valgte linjen i lageret.</span><span class="sxs-lookup"><span data-stu-id="dd421-390">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="dd421-391">Lukk **Reservasjon**-siden for å gå tilbake til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="dd421-391">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="dd421-392">Velg **Frigi til lager** i gruppen **Handlinger** i fanen **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dd421-392">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="dd421-393">Du mottar en informasjonsmelding som viser forsendelse og bølge for denne ordren.</span><span class="sxs-lookup"><span data-stu-id="dd421-393">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="dd421-394">Skriv ned nummeret på bølge-ID og forsendelses-ID.</span><span class="sxs-lookup"><span data-stu-id="dd421-394">Make a note of the wave ID and shipment ID numbers.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="dd421-395">Salgsordre 2</span><span class="sxs-lookup"><span data-stu-id="dd421-395">Sales order 2</span></span>

1. <span data-ttu-id="dd421-396">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="dd421-396">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="dd421-397">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dd421-397">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dd421-398">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="dd421-398">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="dd421-399">**Kundekonto:** *US-006*</span><span class="sxs-lookup"><span data-stu-id="dd421-399">**Customer account:** *US-006*</span></span>
    - <span data-ttu-id="dd421-400">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="dd421-400">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="dd421-401">Velg **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="dd421-401">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="dd421-402">Den nye salgsordren åpnes.</span><span class="sxs-lookup"><span data-stu-id="dd421-402">The new sales order is opened.</span></span> <span data-ttu-id="dd421-403">Den bør inneholde en ny, tom linje i rutenettet på **Salgsordrelinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="dd421-403">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="dd421-404">Angi følgende verdier på denne ordrelinjen:</span><span class="sxs-lookup"><span data-stu-id="dd421-404">Set the following values on this order line:</span></span>

    - <span data-ttu-id="dd421-405">**Vare:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="dd421-405">**Item:** *A0001*</span></span>
    - <span data-ttu-id="dd421-406">**Antall:** *1*</span><span class="sxs-lookup"><span data-stu-id="dd421-406">**Quantity:** *1*</span></span>

1. <span data-ttu-id="dd421-407">På hurtigfanen **Linjedetaljer**, i fanen **Levering** setter du feltet **Leveringsmåte** til *Flowe-STD*.</span><span class="sxs-lookup"><span data-stu-id="dd421-407">On the **Line details** FastTab, on the **Delivery** tab, set the **Mode of delivery** field to *Flowe-STD*.</span></span>
1. <span data-ttu-id="dd421-408">På hurtigfanen **Salgsordrelinjer** velger du **Legg til linje**, og angi deretter følgende verdier på den andre ordrelinjen:</span><span class="sxs-lookup"><span data-stu-id="dd421-408">On the **Sales order lines** FastTab, select **Add line**, and then set the following values on the second order line:</span></span>

    - <span data-ttu-id="dd421-409">**Vare:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="dd421-409">**Item:** *A0002*</span></span>
    - <span data-ttu-id="dd421-410">**Antall:** *1*</span><span class="sxs-lookup"><span data-stu-id="dd421-410">**Quantity:** *1*</span></span>

1. <span data-ttu-id="dd421-411">På hurtigfanen **Linjedetaljer**, i fanen **Levering**, endrer du verdien i feltet **Leveringsmåte** til *Air C-Air*.</span><span class="sxs-lookup"><span data-stu-id="dd421-411">On the **Line details** FastTab, on the **Delivery** tab, change the value of the **Mode of delivery** field to *Air C-Air*.</span></span>
1. <span data-ttu-id="dd421-412">I hurtigfanen **Salgsordrelinjer** velger du den første ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="dd421-412">On the **Sales order lines** FastTab, select the first order line.</span></span> <span data-ttu-id="dd421-413">Velg deretter **Reservasjon** på **Lager**-menyen over rutenettet.</span><span class="sxs-lookup"><span data-stu-id="dd421-413">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="dd421-414">På **Reservasjon**-siden velger du **Reserver parti** for å reservere det fulle antallet på den valgte linjen i lageret.</span><span class="sxs-lookup"><span data-stu-id="dd421-414">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="dd421-415">Lukk **Reservasjon**-siden for å gå tilbake til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="dd421-415">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="dd421-416">I hurtigfanen **Salgsordrelinjer** velger du den andre ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="dd421-416">On the **Sales order lines** FastTab, select the second order line.</span></span> <span data-ttu-id="dd421-417">Velg deretter **Reservasjon** på **Lager**-menyen over rutenettet.</span><span class="sxs-lookup"><span data-stu-id="dd421-417">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="dd421-418">På **Reservasjon**-siden velger du **Reserver parti** for å reservere det fulle antallet på den valgte linjen i lageret.</span><span class="sxs-lookup"><span data-stu-id="dd421-418">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="dd421-419">Lukk **Reservasjon**-siden for å gå tilbake til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="dd421-419">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="dd421-420">Velg **Frigi til lager** i gruppen **Handlinger** i fanen **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dd421-420">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="dd421-421">Du mottar en informasjonsmelding som viser forsendelse og bølge for denne ordren.</span><span class="sxs-lookup"><span data-stu-id="dd421-421">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="dd421-422">Merk at to bølge-ID-numre og to forsendelses-ID-numre er opprettet, én for hver leveringsmåte for salgsordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="dd421-422">Notice that two wave ID numbers and two shipment ID numbers have been created, one for each mode of delivery for the sales order lines.</span></span>

#### <a name="get-the-work-ids-from-the-work-details"></a><span data-ttu-id="dd421-423">Hente arbeids-IDene fra arbeidsdetaljene</span><span class="sxs-lookup"><span data-stu-id="dd421-423">Get the work IDs from the work details</span></span>

1. <span data-ttu-id="dd421-424">Gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="dd421-424">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="dd421-425">Siden viser arbeids-IDene som er opprettet fra salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="dd421-425">The page shows the work IDs that have been created from sales orders.</span></span> <span data-ttu-id="dd421-426">Bruk bølge-IDene og forsendelses-IDene fra salgsordrene som du opprettet, for å finne arbeids-IDen for hver bølge og forsendelse.</span><span class="sxs-lookup"><span data-stu-id="dd421-426">Use the wave IDs and shipment IDs from the sales orders that you created to find the work ID for each wave and shipment.</span></span> <span data-ttu-id="dd421-427">Noter deg arbeids-IDene, fordi du trenger dem i de neste trinnene.</span><span class="sxs-lookup"><span data-stu-id="dd421-427">Make a note of those work IDs, because you will need them in the next steps.</span></span> <span data-ttu-id="dd421-428">Legg merke til at to arbeids-IDer er opprettet for den andre salgsordren.</span><span class="sxs-lookup"><span data-stu-id="dd421-428">Notice that two work IDs were created for the second sales order.</span></span> <span data-ttu-id="dd421-429">Hvis ulike varer er plukket fra forskjellige lokasjoner, genereres separate arbeids-IDer.</span><span class="sxs-lookup"><span data-stu-id="dd421-429">If different items are picked from different locations, separate word IDs are generated.</span></span>

### <a name="pick-items-for-the-sales-orders"></a><span data-ttu-id="dd421-430">Plukke varer for salgsordrene</span><span class="sxs-lookup"><span data-stu-id="dd421-430">Pick items for the sales orders</span></span>

<span data-ttu-id="dd421-431">Fullfør det opprettede arbeidet ved å bruke den mobile enheten til å flytte elementene til pakkestasjonen.</span><span class="sxs-lookup"><span data-stu-id="dd421-431">Complete the created work by using the mobile device to move the items to the pack station.</span></span>

1. <span data-ttu-id="dd421-432">På den mobile enheten logger du på lager *62* ved hjelp av bruker-IDen du opprettet for dette scenariet (eller bruker-IDen for en eksisterende demodatabruker).</span><span class="sxs-lookup"><span data-stu-id="dd421-432">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="dd421-433">I hovedmenyen velger du **Utgående**.</span><span class="sxs-lookup"><span data-stu-id="dd421-433">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="dd421-434">I **Utgående**-menyen velger du **Salgsplukking**.</span><span class="sxs-lookup"><span data-stu-id="dd421-434">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="dd421-435">I **ID**-feltet angir du arbeids-IDen som ble opprettet for salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="dd421-435">In the **ID** field, enter the work ID that was created for sales order 1.</span></span>
1. <span data-ttu-id="dd421-436">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-436">Select **OK**.</span></span>
1. <span data-ttu-id="dd421-437">På siden **Salgsordrer - Plukk** angir du et målnummerskilt som ble opprettet for salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="dd421-437">On the **Sales orders - Pick** page, enter a target LP that was created for sales order 1.</span></span> <span data-ttu-id="dd421-438">Legg merke til at plukklokasjon (*bulk-001*), vare (*A0001*) og antall (*2 stk*) vises.</span><span class="sxs-lookup"><span data-stu-id="dd421-438">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*2 pcs*) are shown.</span></span>
1. <span data-ttu-id="dd421-439">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-439">Select **OK**.</span></span>
1. <span data-ttu-id="dd421-440">Se gjennom informasjonen på siden **Salgsordrer - Plasser**.</span><span class="sxs-lookup"><span data-stu-id="dd421-440">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="dd421-441">**Loc**-feltet bør angi at de plukkede varene skal overføres til *Pakke*-lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="dd421-441">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="dd421-442">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-442">Select **OK**.</span></span>

    <span data-ttu-id="dd421-443">På siden **Skann en arbeids-ID/nummerskilt-ID** får du meldingen "Arbeid fullført"-melding, som viser at arbeids-IDen fra salgsordre 1 er fullført.</span><span class="sxs-lookup"><span data-stu-id="dd421-443">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message, which indicates that the work ID from sales order 1 has been completed.</span></span>

    <span data-ttu-id="dd421-444">Du skal nå plukke salgsordre 2.</span><span class="sxs-lookup"><span data-stu-id="dd421-444">You will now pick sales order 2.</span></span>

1. <span data-ttu-id="dd421-445">I **ID**-feltet angir du arbeids-IDen som ble opprettet for salgsordre 2, der linje 1 har vare *A0001*.</span><span class="sxs-lookup"><span data-stu-id="dd421-445">In the **ID** field, enter the work ID that was created for sales order 2, where line 1 has item *A0001*.</span></span>
1. <span data-ttu-id="dd421-446">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-446">Select **OK**.</span></span>
1. <span data-ttu-id="dd421-447">Angi et målnummerskilt på siden **Salgsordrer - Plukk**.</span><span class="sxs-lookup"><span data-stu-id="dd421-447">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="dd421-448">Legg merke til at plukklokasjon (*bulk-001*), vare (*A0001*) og antall (*1 stk*) vises.</span><span class="sxs-lookup"><span data-stu-id="dd421-448">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="dd421-449">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-449">Select **OK**.</span></span>
1. <span data-ttu-id="dd421-450">Se gjennom informasjonen på siden **Salgsordrer - Plasser**.</span><span class="sxs-lookup"><span data-stu-id="dd421-450">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="dd421-451">**Loc**-feltet bør angi at de plukkede varene skal overføres til *Pakke*-lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="dd421-451">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="dd421-452">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-452">Select **OK**.</span></span>

    <span data-ttu-id="dd421-453">På siden **Skann en arbeids-ID/nummerskilt-ID** mottar du en "Arbeid fullført"-meldingen.</span><span class="sxs-lookup"><span data-stu-id="dd421-453">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="dd421-454">Denne meldingen angir at arbeids-IDen fra linje 1 i salgsordre 2 er fullført.</span><span class="sxs-lookup"><span data-stu-id="dd421-454">This message indicates that the work ID from line 1 of sales order 2 has been completed.</span></span>

1. <span data-ttu-id="dd421-455">I **ID**-feltet angir du arbeids-IDen som ble opprettet for salgsordre 2, der linje 2 har vare *A0002*.</span><span class="sxs-lookup"><span data-stu-id="dd421-455">In the **ID** field, enter the work ID that was created for sales order 2, where line 2 has item *A0002*.</span></span>
1. <span data-ttu-id="dd421-456">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-456">Select **OK**.</span></span>
1. <span data-ttu-id="dd421-457">Angi et målnummerskilt på siden **Salgsordrer - Plukk**.</span><span class="sxs-lookup"><span data-stu-id="dd421-457">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="dd421-458">Legg merke til at plukklokasjon (*bulk-002*), vare (*A0001*) og antall (*1 stk*) vises.</span><span class="sxs-lookup"><span data-stu-id="dd421-458">Notice that the picking location (*bulk-002*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="dd421-459">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-459">Select **OK**.</span></span>
1. <span data-ttu-id="dd421-460">Se gjennom informasjonen på siden **Salgsordrer - Plasser**.</span><span class="sxs-lookup"><span data-stu-id="dd421-460">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="dd421-461">**Loc**-feltet bør angi at de plukkede varene skal overføres til *Pakke*-lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="dd421-461">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="dd421-462">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-462">Select **OK**.</span></span>

    <span data-ttu-id="dd421-463">På siden **Skann en arbeids-ID/nummerskilt-ID** mottar du en "Arbeid fullført"-meldingen.</span><span class="sxs-lookup"><span data-stu-id="dd421-463">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="dd421-464">Denne meldingen angir at arbeids-IDen fra linje 2 i salgsordre 2 er fullført.</span><span class="sxs-lookup"><span data-stu-id="dd421-464">This message indicates that the work ID from line 2 of sales order 2 has been completed.</span></span>

### <a name="pack-sales-orders-into-containers"></a><span data-ttu-id="dd421-465">Pakkesalgsordrer i containere</span><span class="sxs-lookup"><span data-stu-id="dd421-465">Pack sales orders into containers</span></span>

#### <a name="pack-sales-order-1-into-containers"></a><span data-ttu-id="dd421-466">Pakkesalgsordre 1 i containere</span><span class="sxs-lookup"><span data-stu-id="dd421-466">Pack sales order 1 into containers</span></span>

1. <span data-ttu-id="dd421-467">Gå til **Lagerstyring \> Pakking og containerbruk \> Pakke**.</span><span class="sxs-lookup"><span data-stu-id="dd421-467">Go to **Warehouse management \> Packing and containerization \> Pack**.</span></span>

    <span data-ttu-id="dd421-468">Dialogboksen **Velg pakkstasjon** vises.</span><span class="sxs-lookup"><span data-stu-id="dd421-468">The **Select packing station** dialog box appears.</span></span> <span data-ttu-id="dd421-469">Som standard bør feltet **Arbeider** settes til navnet på arbeideren du konfigurerte tidligere.</span><span class="sxs-lookup"><span data-stu-id="dd421-469">By default, the **Worker** field should be set to the name of the worker that you set up earlier.</span></span>

1. <span data-ttu-id="dd421-470">Angi følgende verdier for å vise og arbeide med forsendelser og containere som er planlagt på den bestemte pakkelokasjonen:</span><span class="sxs-lookup"><span data-stu-id="dd421-470">Set the following values to view and work on shipments and containers that are planned at the specific packing location:</span></span>

    - <span data-ttu-id="dd421-471">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="dd421-471">**Site:** *6*</span></span>
    - <span data-ttu-id="dd421-472">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="dd421-472">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="dd421-473">**Plassering:** *Pakke*</span><span class="sxs-lookup"><span data-stu-id="dd421-473">**Location:** *Pack*</span></span>
    - <span data-ttu-id="dd421-474">**Pakkeprofil-ID:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="dd421-474">**Packing profile ID:** *Sort*</span></span>

1. <span data-ttu-id="dd421-475">Velg **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="dd421-475">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="dd421-476">På siden **Pakke** i feltet **Lisensplate eller forsendelse** angir du målnummerskiltet for salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="dd421-476">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for sales order 1.</span></span> <span data-ttu-id="dd421-477">Deretter velger du **Tab**- eller **Enter**-tasten på tastaturet for å gå ut av feltet.</span><span class="sxs-lookup"><span data-stu-id="dd421-477">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="dd421-478">I handlingsruten velger du **Ny container**.</span><span class="sxs-lookup"><span data-stu-id="dd421-478">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="dd421-479">Godta alle standardinnstillingene, og velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-479">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="dd421-480">Noter container-IDen.</span><span class="sxs-lookup"><span data-stu-id="dd421-480">Make a note of the container ID.</span></span>
1. <span data-ttu-id="dd421-481">Angi følgende verdier på **Varepakking**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="dd421-481">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="dd421-482">**Antall:** *1*</span><span class="sxs-lookup"><span data-stu-id="dd421-482">**Quantity:** *1*</span></span>
    - <span data-ttu-id="dd421-483">**Identifikator:** Vare *A0001*</span><span class="sxs-lookup"><span data-stu-id="dd421-483">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="dd421-484">I handlingsruten velger du **Lukk container**.</span><span class="sxs-lookup"><span data-stu-id="dd421-484">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="dd421-485">I dialogboksen **Lukk container** velger du **Hent systemvekt** for å få systemet til å oppdatere **Bruttovekt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="dd421-485">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="dd421-486">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-486">Select **OK**.</span></span> <span data-ttu-id="dd421-487">Containeren flyttes til *SORTER*-plasseringen og er klar til sortering.</span><span class="sxs-lookup"><span data-stu-id="dd421-487">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="dd421-488">Opprett en andre container for å legge til den andre varen fra målnummerskiltet for salgsordre 1 i en ny container.</span><span class="sxs-lookup"><span data-stu-id="dd421-488">Create a second container to add the second item from the LP for sales order 1 to a new container.</span></span>
1. <span data-ttu-id="dd421-489">I handlingsruten velger du **Ny container**.</span><span class="sxs-lookup"><span data-stu-id="dd421-489">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="dd421-490">Godta alle standardinnstillingene, og velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-490">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="dd421-491">Noter container-IDen.</span><span class="sxs-lookup"><span data-stu-id="dd421-491">Make a note of the container ID.</span></span>
1. <span data-ttu-id="dd421-492">Angi følgende verdier på **Varepakking**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="dd421-492">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="dd421-493">**Antall:** *1*</span><span class="sxs-lookup"><span data-stu-id="dd421-493">**Quantity:** *1*</span></span>
    - <span data-ttu-id="dd421-494">**Identifikator:** Vare *A0001*</span><span class="sxs-lookup"><span data-stu-id="dd421-494">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="dd421-495">I handlingsruten velger du **Lukk container**.</span><span class="sxs-lookup"><span data-stu-id="dd421-495">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="dd421-496">I dialogboksen **Lukk container** velger du **Hent systemvekt** for å få systemet til å oppdatere **Bruttovekt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="dd421-496">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="dd421-497">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-497">Select **OK**.</span></span> <span data-ttu-id="dd421-498">Containeren flyttes til *SORTER*-plasseringen og er klar til sortering.</span><span class="sxs-lookup"><span data-stu-id="dd421-498">The container is moved to the *SORT* location and is ready for sorting.</span></span>

#### <a name="pack-sales-order-2-into-containers"></a><span data-ttu-id="dd421-499">Pakkesalgsordre 2 i containere</span><span class="sxs-lookup"><span data-stu-id="dd421-499">Pack sales order 2 into containers</span></span>

1. <span data-ttu-id="dd421-500">På siden **Pakke** i feltet **Lisensplate eller forsendelse** angir du målnummerskiltet for linje 1 for salgsordre 2.</span><span class="sxs-lookup"><span data-stu-id="dd421-500">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for line 1 of sales order 2.</span></span> <span data-ttu-id="dd421-501">Deretter velger du **Tab**- eller **Enter**-tasten på tastaturet for å gå ut av feltet.</span><span class="sxs-lookup"><span data-stu-id="dd421-501">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="dd421-502">I handlingsruten velger du **Ny container**.</span><span class="sxs-lookup"><span data-stu-id="dd421-502">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="dd421-503">Godta alle standardinnstillingene, og velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-503">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="dd421-504">Noter container-IDen.</span><span class="sxs-lookup"><span data-stu-id="dd421-504">Make a note of the container ID.</span></span>
1. <span data-ttu-id="dd421-505">Angi følgende verdier på **Varepakking**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="dd421-505">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="dd421-506">**Antall:** *1*</span><span class="sxs-lookup"><span data-stu-id="dd421-506">**Quantity:** *1*</span></span>
    - <span data-ttu-id="dd421-507">**Identifikator:** Vare *A0001*</span><span class="sxs-lookup"><span data-stu-id="dd421-507">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="dd421-508">I handlingsruten velger du **Lukk container**.</span><span class="sxs-lookup"><span data-stu-id="dd421-508">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="dd421-509">I dialogboksen **Lukk container** velger du **Hent systemvekt** for å få systemet til å oppdatere **Bruttovekt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="dd421-509">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="dd421-510">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-510">Select **OK**.</span></span> <span data-ttu-id="dd421-511">Containeren flyttes til *SORTER*-plasseringen og er klar til sortering.</span><span class="sxs-lookup"><span data-stu-id="dd421-511">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="dd421-512">I feltet **Lisensplate eller forsendelse** angir du målnummerskiltet for linje 2 for salgsordre 2.</span><span class="sxs-lookup"><span data-stu-id="dd421-512">In the **License plate or shipment** field, enter the target LP for line 2 of the sales order 2.</span></span> <span data-ttu-id="dd421-513">Deretter velger du **Tab**- eller **Enter**-tasten på tastaturet for å gå ut av feltet.</span><span class="sxs-lookup"><span data-stu-id="dd421-513">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="dd421-514">I handlingsruten velger du **Ny container**.</span><span class="sxs-lookup"><span data-stu-id="dd421-514">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="dd421-515">Godta alle standardinnstillingene, og velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-515">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="dd421-516">Noter container-IDen.</span><span class="sxs-lookup"><span data-stu-id="dd421-516">Make a note of the container ID.</span></span>
1. <span data-ttu-id="dd421-517">Angi følgende verdier på **Varepakking**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="dd421-517">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="dd421-518">**Antall:** *1*</span><span class="sxs-lookup"><span data-stu-id="dd421-518">**Quantity:** *1*</span></span>
    - <span data-ttu-id="dd421-519">**Identifikator-felt:** Vare *A0002*</span><span class="sxs-lookup"><span data-stu-id="dd421-519">**Identifier field:** Item *A0002*</span></span>

1. <span data-ttu-id="dd421-520">I handlingsruten velger du **Lukk container**.</span><span class="sxs-lookup"><span data-stu-id="dd421-520">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="dd421-521">I dialogboksen **Lukk container** velger du **Hent systemvekt** for å få systemet til å oppdatere **Bruttovekt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="dd421-521">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="dd421-522">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-522">Select **OK**.</span></span> <span data-ttu-id="dd421-523">Containeren flyttes til *SORTER*-plasseringen og er klar til sortering.</span><span class="sxs-lookup"><span data-stu-id="dd421-523">The container is moved to the *SORT* location and is ready for sorting.</span></span>

<span data-ttu-id="dd421-524">Hvis du vil vise containerdetaljene, går du til **Lagerstyring \> Pakking og containerbruk \> Containere** og søker etter container-IDene som ble opprettet under pakking.</span><span class="sxs-lookup"><span data-stu-id="dd421-524">To view the container details, go to **Warehouse management \> Packing and containerization \> Containers**, and search for the container IDs that were created during packing.</span></span>

### <a name="sort-the-containers"></a><span data-ttu-id="dd421-525">Sortere containerne</span><span class="sxs-lookup"><span data-stu-id="dd421-525">Sort the containers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd421-526">Når du får tilgang til **Palleversjon** i menyelementet på mobilappen for å utføre utgående sortering, vil du se en knapp som er merket som **Full**.</span><span class="sxs-lookup"><span data-stu-id="dd421-526">When you access the **Pallet build** menu item on the mobile app to do outbound sorting, you will see a button that is labeled **Full**.</span></span> <span data-ttu-id="dd421-527">*Ikke bruk **Full**-knappen til å sortere eller lukke posisjonen.*</span><span class="sxs-lookup"><span data-stu-id="dd421-527">*Don't use the **Full** button to sort or close the position.*</span></span>
>
> <span data-ttu-id="dd421-528">**Full**-knappen er angitt som standard og kan ikke deaktiveres eller fjernes fra siden.</span><span class="sxs-lookup"><span data-stu-id="dd421-528">The **Full** button is provided by default and can't be disabled or removed from the page.</span></span> <span data-ttu-id="dd421-529">Den brukes ikke for funksjonen *Utgående sortering*.</span><span class="sxs-lookup"><span data-stu-id="dd421-529">It isn't used for the *Outbound sorting* feature.</span></span>

#### <a name="sort-the-first-container"></a><span data-ttu-id="dd421-530">Sortere den første containeren</span><span class="sxs-lookup"><span data-stu-id="dd421-530">Sort the first container</span></span>

1. <span data-ttu-id="dd421-531">På den mobile enheten logger du på lager *62* ved hjelp av bruker-IDen du opprettet for dette scenariet (eller bruker-IDen for en eksisterende demodatabruker).</span><span class="sxs-lookup"><span data-stu-id="dd421-531">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="dd421-532">I hovedmenyen velger du **Utgående**.</span><span class="sxs-lookup"><span data-stu-id="dd421-532">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="dd421-533">I **Utgående**-menyen velger du **Palleversjon**.</span><span class="sxs-lookup"><span data-stu-id="dd421-533">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="dd421-534">I **LP/Con**-feltet angir du den første container-IDen som er tilknyttet salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="dd421-534">In the **LP/Con** field, enter the first container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="dd421-535">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-535">Select **OK**.</span></span>
1. <span data-ttu-id="dd421-536">Fordi det ikke finnes noen sorteringsposisjoner, må du angi en.</span><span class="sxs-lookup"><span data-stu-id="dd421-536">Because no sort positions currently exist, you must specify one.</span></span> <span data-ttu-id="dd421-537">I **Sporteringsposisjon-ID**-feltet angir du *SP01*.</span><span class="sxs-lookup"><span data-stu-id="dd421-537">In the **Sort position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="dd421-538">Fordi ingen nummerskilt er knyttet til sorteringsposisjon *SP01*, må du angi et.</span><span class="sxs-lookup"><span data-stu-id="dd421-538">Because no LP is currently associated with sort position *SP01*, you must specify one.</span></span> <span data-ttu-id="dd421-539">I feltet **Nummerskilt** angir du *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="dd421-539">In the **LP** field, enter *PLP01*.</span></span>
1. <span data-ttu-id="dd421-540">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-540">Select **OK**.</span></span>
1. <span data-ttu-id="dd421-541">Siden validering av sorteringsposisjon er slått på, må du angi ID for sorteringsposisjon på nytt.</span><span class="sxs-lookup"><span data-stu-id="dd421-541">Because sort position validation is turned on, you must enter the sort position ID again.</span></span> <span data-ttu-id="dd421-542">I **Sporteringsposisjon-ID**-feltet angir du *SP01*.</span><span class="sxs-lookup"><span data-stu-id="dd421-542">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="dd421-543">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-543">Select **OK**.</span></span>

    <span data-ttu-id="dd421-544">Du mottar en Arbeid fullført-melding.</span><span class="sxs-lookup"><span data-stu-id="dd421-544">You receive a "Work completed" message.</span></span>

> [!TIP]
> <span data-ttu-id="dd421-545">Hvis du vil vise sorteringsposisjonen og nummerskiltet i den, går du til **Lagerstyring \> Pakking og containerbruk \> Posisjonstilordninger for utgående sortering**.</span><span class="sxs-lookup"><span data-stu-id="dd421-545">To view the sort position and the LP in it, go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
>
> <span data-ttu-id="dd421-546">Siden **Posisjonstilordninger for utgående sortering** viser alle sorteringsposisjonene som for øyeblikket er aktive.</span><span class="sxs-lookup"><span data-stu-id="dd421-546">The **Outbound sorting position assignments** page shows all the sort positions that are currently active.</span></span> <span data-ttu-id="dd421-547">Feltet **Transaksjoner for sorteringsposisjon** viser nummerskiltet som er knyttet til hver sorteringsplassering, og containerne som finnes i sorteringsposisjonen.</span><span class="sxs-lookup"><span data-stu-id="dd421-547">The **Sort position transactions** field shows the LP that is associated with each sort position, and the containers that are in the sort position.</span></span> <span data-ttu-id="dd421-548">Legg merke til at det allerede finnes én sorteringsposisjon, og at hurtigfanen **Kriterier for sorteringsposisjon** viser et vilkår for **Forsendelse – Transportørtjeneste - Fly**.</span><span class="sxs-lookup"><span data-stu-id="dd421-548">Notice that one sort position currently exists, and that the **Sort position criteria** FastTab shows a criterion of **Shipment – Carrier service - Air**.</span></span>

#### <a name="sort-the-remaining-containers"></a><span data-ttu-id="dd421-549">Sortere de resterende containerne</span><span class="sxs-lookup"><span data-stu-id="dd421-549">Sort the remaining containers</span></span>

1. <span data-ttu-id="dd421-550">På den mobile enheten logger du på lager *62* ved hjelp av bruker-IDen du opprettet for dette scenariet (eller bruker-IDen for en eksisterende demodatabruker).</span><span class="sxs-lookup"><span data-stu-id="dd421-550">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="dd421-551">I hovedmenyen velger du **Utgående**.</span><span class="sxs-lookup"><span data-stu-id="dd421-551">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="dd421-552">I **Utgående**-menyen velger du **Palleversjon**.</span><span class="sxs-lookup"><span data-stu-id="dd421-552">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="dd421-553">I **LP/Con**-feltet angir du den andre container-IDen som er tilknyttet salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="dd421-553">In the **LP/Con** field, enter the second container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="dd421-554">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-554">Select **OK**.</span></span> <span data-ttu-id="dd421-555">Siden sorteringsmalen er satt opp til å sortere automatisk, og det allerede finnes en sorteringsposisjon som har samsvarende vilkår, blir du automatisk dirigert til riktig sorteringsposisjon.</span><span class="sxs-lookup"><span data-stu-id="dd421-555">Because the sorting template is set up to sort automatically, and a sort position that has matching criteria already exists, you're automatically directed to the correct sort position.</span></span>
1. <span data-ttu-id="dd421-556">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-556">Select **OK**.</span></span>
1. <span data-ttu-id="dd421-557">Bekreft sorteringsposisjons-IDen for å angi at lageret er på riktig sted.</span><span class="sxs-lookup"><span data-stu-id="dd421-557">Confirm the sort position ID to indicate that the inventory is in the correct place.</span></span> <span data-ttu-id="dd421-558">I **Sporteringsposisjon-ID**-feltet angir du *SP01*.</span><span class="sxs-lookup"><span data-stu-id="dd421-558">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="dd421-559">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-559">Select **OK**.</span></span>

    <span data-ttu-id="dd421-560">Arbeid er fullført på den andre containeren fra salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="dd421-560">Work is completed on the second container from sales order 1.</span></span> <span data-ttu-id="dd421-561">Du skal nå sortere de gjenstående containerne fra salgsordre 2.</span><span class="sxs-lookup"><span data-stu-id="dd421-561">You will now sort the remaining containers from sales order 2.</span></span>

1. <span data-ttu-id="dd421-562">I **LP/Con**-feltet angir du container-IDen til containeren fra salgsordre 2 som inneholder vare *A0001*.</span><span class="sxs-lookup"><span data-stu-id="dd421-562">In the **LP/Con** field, enter the container ID of the container from sales order 2 that holds item *A0001*.</span></span> <span data-ttu-id="dd421-563">Fordi transportørtjenesten er forskjellig, blir du bedt om å angi en ny sorteringsposisjon og tilordne et nummerskilt til denne posisjonen.</span><span class="sxs-lookup"><span data-stu-id="dd421-563">Because the carrier service differs, you're prompted to enter a new sort position and assign an LP to that position.</span></span> <span data-ttu-id="dd421-564">Bruk sorteringsposisjon *SP02* og nummerskilt *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="dd421-564">Use sort position *SP02* and LP *PLP02*.</span></span>
1. <span data-ttu-id="dd421-565">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-565">Select **OK**.</span></span>
1. <span data-ttu-id="dd421-566">Bekreft sorteringsposisjonen ved å angi *SP02* i feltet **Sporteringsposisjon**.</span><span class="sxs-lookup"><span data-stu-id="dd421-566">Confirm the sort position by entering *SP02* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="dd421-567">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-567">Select **OK**.</span></span>

    <span data-ttu-id="dd421-568">Arbeidet er fullført på containeren.</span><span class="sxs-lookup"><span data-stu-id="dd421-568">Work is completed on the container.</span></span>

1. <span data-ttu-id="dd421-569">I **LP/Con**-feltet angir du container-IDen til den gjenværende containeren fra salgsordre 2 som inneholder vare *A0002*.</span><span class="sxs-lookup"><span data-stu-id="dd421-569">In the **LP/Con** field, enter the container ID for the remaining container from sales order 2 that holds item *A0002*.</span></span> <span data-ttu-id="dd421-570">Fordi transportørtjenesten er den samme som transportørtjenesten for salgsordre 1, viser systemet den eksisterende sorteringsposisjonen som har samsvarende kriterier.</span><span class="sxs-lookup"><span data-stu-id="dd421-570">Because the carrier service is the same as the carrier service for sales order 1, the system shows the existing sort position that has matching criteria.</span></span>
1. <span data-ttu-id="dd421-571">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-571">Select **OK**.</span></span>
1. <span data-ttu-id="dd421-572">Bekreft sorteringsposisjonen ved å angi *SP01* i feltet **Sporteringsposisjon**.</span><span class="sxs-lookup"><span data-stu-id="dd421-572">Confirm the sort position by entering *SP01* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="dd421-573">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-573">Select **OK**.</span></span>

    <span data-ttu-id="dd421-574">Arbeidet er fullført på containeren.</span><span class="sxs-lookup"><span data-stu-id="dd421-574">Work is completed on the container.</span></span>

### <a name="close-the-outbound-sorting-positions"></a><span data-ttu-id="dd421-575">Lukke den utgående sorteringsposisjonen</span><span class="sxs-lookup"><span data-stu-id="dd421-575">Close the outbound sorting positions</span></span>

<span data-ttu-id="dd421-576">Når hele lageret er sortert, må posisjonen lukkes før arbeidet kan opprettes.</span><span class="sxs-lookup"><span data-stu-id="dd421-576">When all inventory has been sorted, the position must be closed before work can be created.</span></span> <span data-ttu-id="dd421-577">Sortert lagerplukkingsarbeid vil bli opprettet for å ta lageret til rampedøren.</span><span class="sxs-lookup"><span data-stu-id="dd421-577">Sorted inventory picking work will be created to take the inventory to the bay door.</span></span>

#### <a name="close-a-position-from-the-mobile-device"></a><span data-ttu-id="dd421-578">Lukke en posisjon fra den mobile enheten</span><span class="sxs-lookup"><span data-stu-id="dd421-578">Close a position from the mobile device</span></span>

1. <span data-ttu-id="dd421-579">På den mobile enheten logger du på lager *62* ved hjelp av bruker-IDen du opprettet for dette scenariet (eller bruker-IDen for en eksisterende demodatabruker).</span><span class="sxs-lookup"><span data-stu-id="dd421-579">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="dd421-580">I hovedmenyen velger du **Utgående**.</span><span class="sxs-lookup"><span data-stu-id="dd421-580">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="dd421-581">I **Utgående**-menyen velger du **Palleversjon**.</span><span class="sxs-lookup"><span data-stu-id="dd421-581">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="dd421-582">I **LP/con**-feltet angir du en container-ID som ble sortert for å sortere posisjonen *SP01*.</span><span class="sxs-lookup"><span data-stu-id="dd421-582">In the **LP/Con** field, enter a container ID that was sorted to sort position *SP01*.</span></span>
1. <span data-ttu-id="dd421-583">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-583">Select **OK**.</span></span>
1. <span data-ttu-id="dd421-584">Du får følgende melding: "Containeren er allerede sortert til posisjon SP01.</span><span class="sxs-lookup"><span data-stu-id="dd421-584">You receive the following message: "The container is already sorted to position SP01.</span></span> <span data-ttu-id="dd421-585">Vil du lukke posisjonen?"</span><span class="sxs-lookup"><span data-stu-id="dd421-585">Close the position?"</span></span> <span data-ttu-id="dd421-586">Velg **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="dd421-586">Select **Close**.</span></span>

    <span data-ttu-id="dd421-587">Arbeidet er fullført.</span><span class="sxs-lookup"><span data-stu-id="dd421-587">Work is completed.</span></span>

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a><span data-ttu-id="dd421-588">Lukke en posisjon fra utgående sorteringsposisjonstilordninger</span><span class="sxs-lookup"><span data-stu-id="dd421-588">Close a position from outbound sorting position assignments</span></span>

1. <span data-ttu-id="dd421-589">Gå til **Lagerstyring \> Pakking og containerbruk \> Posisjonstilordninger for utgående sortering**.</span><span class="sxs-lookup"><span data-stu-id="dd421-589">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="dd421-590">I venstre kolonne velger du **SP02**.</span><span class="sxs-lookup"><span data-stu-id="dd421-590">In the left column, select **SP02**.</span></span> <span data-ttu-id="dd421-591">Denne utgående sorteringsposisjonsraden er den du vil lukke.</span><span class="sxs-lookup"><span data-stu-id="dd421-591">This outbound sorting position row is the one that you will close.</span></span>
1. <span data-ttu-id="dd421-592">I handlingsruten velger du **Lukk posisjon**.</span><span class="sxs-lookup"><span data-stu-id="dd421-592">On the Action Pane, select **Close position**.</span></span> <span data-ttu-id="dd421-593">Sorteringsposisjons posten er lukket og vises ikke lenger.</span><span class="sxs-lookup"><span data-stu-id="dd421-593">The sorting position record is closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="dd421-594">Hvis du vil vise alle poster med lukkede posisjoner, merker du av for **Vis lukket**.</span><span class="sxs-lookup"><span data-stu-id="dd421-594">To show all closed position records, select the **Show closed** check box.</span></span>

### <a name="sorted-inventory-picking"></a><span data-ttu-id="dd421-595">Sortert lagerhenting</span><span class="sxs-lookup"><span data-stu-id="dd421-595">Sorted inventory picking</span></span>

<span data-ttu-id="dd421-596">Du må fylle ut det sorterte lagerplukkingsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="dd421-596">You must complete the sorted inventory picking work.</span></span> <span data-ttu-id="dd421-597">Når det er fullført, blir lageret plukket lageret til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="dd421-597">When it's completed, the inventory will be picked to the sales order.</span></span> <span data-ttu-id="dd421-598">På dette tidspunktet gjelder alle andre lagerprosesser.</span><span class="sxs-lookup"><span data-stu-id="dd421-598">At that point, all other warehouse processes apply.</span></span>

1. <span data-ttu-id="dd421-599">På den mobile enheten logger du på lager *62* ved hjelp av bruker-IDen du opprettet for dette scenariet (eller bruker-IDen for en eksisterende demodatabruker).</span><span class="sxs-lookup"><span data-stu-id="dd421-599">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="dd421-600">I hovedmenyen velger du **Utgående**.</span><span class="sxs-lookup"><span data-stu-id="dd421-600">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="dd421-601">På menyen **Utgående** velger du **Last fra sortering**.</span><span class="sxs-lookup"><span data-stu-id="dd421-601">On the **Outbound** menu, select **Load from Sorting**.</span></span>
1. <span data-ttu-id="dd421-602">Angi mål-IDen for nummerskilt fra den første sorteringsposisjonen, *SP01*.</span><span class="sxs-lookup"><span data-stu-id="dd421-602">Enter the target LP ID from the first sort position, *SP01*.</span></span> <span data-ttu-id="dd421-603">Angi **ID**-feltet til *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="dd421-603">Set the **ID** field to *PLP01*.</span></span>
1. <span data-ttu-id="dd421-604">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-604">Select **OK**.</span></span>
1. <span data-ttu-id="dd421-605">Siden **Sortert lagerplukking: Plukk** viser plukkarbeidet som må utføres.</span><span class="sxs-lookup"><span data-stu-id="dd421-605">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="dd421-606">Plukk fra *SORTER*-lokasjonen og målnummerskiltet *PLP01*, som har flere varer og et antall på *3*.</span><span class="sxs-lookup"><span data-stu-id="dd421-606">Pick from the *SORT* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="dd421-607">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-607">Select **OK**.</span></span>
1. <span data-ttu-id="dd421-608">Siden **Sortert lagerplukking: Plasser** viser plasseringsarbeidet som må utføres.</span><span class="sxs-lookup"><span data-stu-id="dd421-608">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="dd421-609">Plasser til *Rampedør*-lokasjonen og målnummerskilt *PLP01*, som har flere varer og et antall på *3*.</span><span class="sxs-lookup"><span data-stu-id="dd421-609">Put to the *Baydoor* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="dd421-610">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-610">Select **OK**.</span></span>

    <span data-ttu-id="dd421-611">Arbeidet er fullført.</span><span class="sxs-lookup"><span data-stu-id="dd421-611">Work is completed.</span></span>

1. <span data-ttu-id="dd421-612">Angi målnummerskilt-ID-en fra den andre sorteringsposisjonen, *SP02*.</span><span class="sxs-lookup"><span data-stu-id="dd421-612">Enter the target license plate ID from the second sort position, *SP02*.</span></span> <span data-ttu-id="dd421-613">Angi **ID**-feltet til *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="dd421-613">Set the **ID** field to *PLP02*.</span></span>
1. <span data-ttu-id="dd421-614">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-614">Select **OK**.</span></span>
1. <span data-ttu-id="dd421-615">Siden **Sortert lagerplukking: Plukk** viser plukkarbeidet som må utføres.</span><span class="sxs-lookup"><span data-stu-id="dd421-615">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="dd421-616">Plukk fra *SORTER*-lokasjonen og målnummerskiltet *PLP02*, som har flere varer og et antall på *1*.</span><span class="sxs-lookup"><span data-stu-id="dd421-616">Pick from the *SORT* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="dd421-617">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-617">Select **OK**.</span></span>
1. <span data-ttu-id="dd421-618">Siden **Sortert lagerplukking: Plasser** viser plasseringsarbeidet som må utføres.</span><span class="sxs-lookup"><span data-stu-id="dd421-618">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="dd421-619">Plasser til *Rampedør*-lokasjonen og målnummerskilt *PLP02*, som har flere varer og et antall på *1*.</span><span class="sxs-lookup"><span data-stu-id="dd421-619">Put to the *Baydoor* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="dd421-620">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd421-620">Select **OK**.</span></span>

    <span data-ttu-id="dd421-621">Arbeidet er fullført.</span><span class="sxs-lookup"><span data-stu-id="dd421-621">Work is completed.</span></span>

<span data-ttu-id="dd421-622">På dette tidspunktet og fremover gjelder alle andre lagerprosesser.</span><span class="sxs-lookup"><span data-stu-id="dd421-622">From this point forward, all other warehouse processes apply.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]