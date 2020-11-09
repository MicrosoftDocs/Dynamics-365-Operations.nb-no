---
title: Lagersporing
description: Dette emnet inneholder informasjon om lagersporing. Med lagersporing kan du konsolidere behov etter vare og måleenhet fra ordrer som har statusen bestilt, reservert eller frigitt. Det hjelper lagerledere å planlegge plukklokasjoner før de frigir ordrer til lageret og oppretter plukkarbeid.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ed9e6eae2ecc8de8d5eeef4699678e93dd74f193
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017420"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="22afb-105">Lagersporing</span><span class="sxs-lookup"><span data-stu-id="22afb-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22afb-106">Med lagersporing kan du konsolidere behov etter vare og måleenhet fra ordrer som har statusen *bestilt* , *reservert* eller *frigitt*.</span><span class="sxs-lookup"><span data-stu-id="22afb-106">Warehouse slotting lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered* , *Reserved* , or *Released*.</span></span> <span data-ttu-id="22afb-107">Det genererte behovet kan deretter brukes på lokasjoner som skal brukes til plukking, basert på antall, enhet, fysiske dimensjoner, faste lokasjoner og mer.</span><span class="sxs-lookup"><span data-stu-id="22afb-107">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="22afb-108">Etter at sporingsplanen er opprettet, kan etter fyllingsarbeid opprettes for å hente riktig lagermengde til hver lokasjon.</span><span class="sxs-lookup"><span data-stu-id="22afb-108">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="22afb-109">Denne funksjonen hjelper lagerledere å planlegge plukklokasjoner før de frigir ordrer til lageret og oppretter plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="22afb-109">This functionality helps warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

## <a name="turn-on-the-warehouse-slotting-feature"></a><span data-ttu-id="22afb-110">Aktivere lagersporingsfunksjonen</span><span class="sxs-lookup"><span data-stu-id="22afb-110">Turn on the warehouse slotting feature</span></span>

<span data-ttu-id="22afb-111">Før du kan bruke denne funksjonen, må den være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="22afb-111">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="22afb-112">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="22afb-112">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="22afb-113">I **Funksjonsadministrering** -arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="22afb-113">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="22afb-114">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="22afb-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="22afb-115">**Funksjonsnavn:** *Lagersporingsfunksjon*</span><span class="sxs-lookup"><span data-stu-id="22afb-115">**Feature name:** *Warehouse slotting feature*</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="22afb-116">Definere lagersporing</span><span class="sxs-lookup"><span data-stu-id="22afb-116">Set up warehouse slotting</span></span>

<span data-ttu-id="22afb-117">Hvis du vil bruke lagersporing, må du definere følgende elementer i systemet.</span><span class="sxs-lookup"><span data-stu-id="22afb-117">To use warehouse slotting, you must set up the following elements in your system.</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="22afb-118">Opprett måleenhetslag for sporing</span><span class="sxs-lookup"><span data-stu-id="22afb-118">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="22afb-119">Måleenhetslag gjør det mulig å gruppere flere måleenheter sammen for å sporing.</span><span class="sxs-lookup"><span data-stu-id="22afb-119">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="22afb-120">Hvis for eksempel bokser med flere størrelser plukkes fra samme boksplukkingsområde, kan ett lag opprettes for alle størrelsene.</span><span class="sxs-lookup"><span data-stu-id="22afb-120">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="22afb-121">**Det må opprettes en linje for hver måleenhet som skal være en del av laget.**</span><span class="sxs-lookup"><span data-stu-id="22afb-121">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="22afb-122">Gå til **Lagerstyring \> Oppsett \> Etterfylling \> Måleenhetslag for sporing**.</span><span class="sxs-lookup"><span data-stu-id="22afb-122">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="22afb-123">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="22afb-123">Select **New**.</span></span>
1. <span data-ttu-id="22afb-124">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="22afb-124">In the header, set the following values:</span></span>

    - <span data-ttu-id="22afb-125">**Måleenhetslag:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="22afb-125">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="22afb-126">**Beskrivelse:** *Hver bokspall*</span><span class="sxs-lookup"><span data-stu-id="22afb-126">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="22afb-127">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="22afb-127">Select **Save**.</span></span>
1. <span data-ttu-id="22afb-128">På **Måleenhet** -hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="22afb-128">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="22afb-129">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="22afb-129">On the new line, set the following values:</span></span>

    - <span data-ttu-id="22afb-130">**Enhet:** *Boks*</span><span class="sxs-lookup"><span data-stu-id="22afb-130">**Unit:** *Box*</span></span>
    - <span data-ttu-id="22afb-131">**Beskrivelse:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="22afb-131">**Description:** Leave this field blank.</span></span> <span data-ttu-id="22afb-132">Den fylles ut automatisk når du lagrer endringene.</span><span class="sxs-lookup"><span data-stu-id="22afb-132">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="22afb-133">**Enhetsklasse:** *Antall*</span><span class="sxs-lookup"><span data-stu-id="22afb-133">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="22afb-134">Velg **Ny** for å legge til en ny linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="22afb-134">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="22afb-135">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="22afb-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="22afb-136">**Enhet:** *ea*</span><span class="sxs-lookup"><span data-stu-id="22afb-136">**Unit:** *ea*</span></span>
    - <span data-ttu-id="22afb-137">**Beskrivelse:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="22afb-137">**Description:** Leave this field blank.</span></span> <span data-ttu-id="22afb-138">Den fylles ut automatisk når du lagrer endringene.</span><span class="sxs-lookup"><span data-stu-id="22afb-138">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="22afb-139">**Enhetsklasse:** *Antall*</span><span class="sxs-lookup"><span data-stu-id="22afb-139">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="22afb-140">Velg **Ny** for å legge til en tredje linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="22afb-140">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="22afb-141">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="22afb-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="22afb-142">**Enhet:** *PL*</span><span class="sxs-lookup"><span data-stu-id="22afb-142">**Unit:** *PL*</span></span>
    - <span data-ttu-id="22afb-143">**Beskrivelse:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="22afb-143">**Description:** Leave this field blank.</span></span> <span data-ttu-id="22afb-144">Den fylles ut automatisk når du lagrer endringene.</span><span class="sxs-lookup"><span data-stu-id="22afb-144">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="22afb-145">**Enhetsklasse:** *Antall*</span><span class="sxs-lookup"><span data-stu-id="22afb-145">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="22afb-146">Velg **Lagre** for å lagre laget.</span><span class="sxs-lookup"><span data-stu-id="22afb-146">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="22afb-147">Opprette en direktivkode for sporing</span><span class="sxs-lookup"><span data-stu-id="22afb-147">Create a directive code for slotting</span></span>

<span data-ttu-id="22afb-148">Du må velge direktivkoden som skal knyttes til en mal.</span><span class="sxs-lookup"><span data-stu-id="22afb-148">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="22afb-149">Gå til **Lagerstyring \> Oppsett \> Direktivkoder**.</span><span class="sxs-lookup"><span data-stu-id="22afb-149">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="22afb-150">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="22afb-150">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="22afb-151">I **Direktivkode** -feltet angir du *Sporing*.</span><span class="sxs-lookup"><span data-stu-id="22afb-151">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="22afb-152">I **Direktivbeskrivelse** -feltet angir du *Sporing*.</span><span class="sxs-lookup"><span data-stu-id="22afb-152">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="22afb-153">Definere sporingsmaler</span><span class="sxs-lookup"><span data-stu-id="22afb-153">Set up slotting templates</span></span>

<span data-ttu-id="22afb-154">Hver sporingsmal styrer hvordan beholdningen tilordnes lokasjoner for et bestemt lager.</span><span class="sxs-lookup"><span data-stu-id="22afb-154">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="22afb-155">Hver mal må inneholde en linje for hver sporingsspesifikasjon.</span><span class="sxs-lookup"><span data-stu-id="22afb-155">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="22afb-156">Bruk fremgangsmåtene i denne delen til å definere sporingsmaler.</span><span class="sxs-lookup"><span data-stu-id="22afb-156">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="22afb-157">Gå til **Lagerstyring \> Oppsett \> Etterfylling \> Sporingsmaler**.</span><span class="sxs-lookup"><span data-stu-id="22afb-157">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="22afb-158">Velg **Ny** for å opprette en mal.</span><span class="sxs-lookup"><span data-stu-id="22afb-158">Select **New** to create a template.</span></span>

<span data-ttu-id="22afb-159">Deretter må du definere maltoppteksten, sporingsspesifikasjoner og lokasjonsdirektiver som forklart nedenfor.</span><span class="sxs-lookup"><span data-stu-id="22afb-159">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span>

#### <a name="set-up-a-slotting-template-header"></a><span data-ttu-id="22afb-160">Angi en topptekst for sporingsmal</span><span class="sxs-lookup"><span data-stu-id="22afb-160">Set up a slotting template header</span></span>

1. <span data-ttu-id="22afb-161">Angi følgende verdier i toppteksten for malen:</span><span class="sxs-lookup"><span data-stu-id="22afb-161">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="22afb-162">**Sporingsmal:** _61_</span><span class="sxs-lookup"><span data-stu-id="22afb-162">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="22afb-163">**Beskrivelse:** _61_</span><span class="sxs-lookup"><span data-stu-id="22afb-163">**Description:** _61_</span></span>
    - <span data-ttu-id="22afb-164">**Behovstype:** *Salgsordre*</span><span class="sxs-lookup"><span data-stu-id="22afb-164">**Demand type:** *Sales order*</span></span>

        <span data-ttu-id="22afb-165">Fortiden er *Salgsordre* den eneste behovstypen som støttes.</span><span class="sxs-lookup"><span data-stu-id="22afb-165">Currently, *Sales order* is the only demand type that is supported.</span></span>

    - <span data-ttu-id="22afb-166">**Behovsstrategi:** _Bestilt_</span><span class="sxs-lookup"><span data-stu-id="22afb-166">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="22afb-167">Følgende verdier er tilgjengelige i dette feltet:</span><span class="sxs-lookup"><span data-stu-id="22afb-167">The following values are available in this field:</span></span>

        - <span data-ttu-id="22afb-168">**Bestilt** – hele det bestilte antallet på salgsordren skal vurderes som behov.</span><span class="sxs-lookup"><span data-stu-id="22afb-168">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="22afb-169">**Reservert** – bare antallet for salgsordrelinjen som er reservert (fysisk og bestilt), skal vurderes som behov.</span><span class="sxs-lookup"><span data-stu-id="22afb-169">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>

    - <span data-ttu-id="22afb-170">**Lager:** _61_</span><span class="sxs-lookup"><span data-stu-id="22afb-170">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="22afb-171">**Tillat at bølgebehov bruker ikke-reservert antall:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="22afb-171">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="22afb-172">Du kan også angi en spørring for å begrense omfanget av behovet som evalueres.</span><span class="sxs-lookup"><span data-stu-id="22afb-172">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="22afb-173">Definer sporingsspesifikasjoner for hver mal</span><span class="sxs-lookup"><span data-stu-id="22afb-173">Set up slotting specifications for each template</span></span>

<span data-ttu-id="22afb-174">For hver mal du oppretter, følger du disse trinnene for å legge til en linje for hver sporingsspesifikasjon.</span><span class="sxs-lookup"><span data-stu-id="22afb-174">For each template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="22afb-175">På **Sporingsmaldetaljer** -hurtigfanen velger du **Ny** for å opprette en mallinje.</span><span class="sxs-lookup"><span data-stu-id="22afb-175">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="22afb-176">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="22afb-176">On the new line, set the following values:</span></span>

    - <span data-ttu-id="22afb-177">**Sekvens:** _1_</span><span class="sxs-lookup"><span data-stu-id="22afb-177">**Sequence:** _1_</span></span>
    - <span data-ttu-id="22afb-178">**Beskrivelse:** _Fast lokasjon_</span><span class="sxs-lookup"><span data-stu-id="22afb-178">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="22afb-179">**Minimumsantall:** _1_</span><span class="sxs-lookup"><span data-stu-id="22afb-179">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="22afb-180">Dette feltet definerer minimumsantall for behov som er nødvendig for linjen.</span><span class="sxs-lookup"><span data-stu-id="22afb-180">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="22afb-181">**Maksimalt antall:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="22afb-181">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="22afb-182">Dette feltet definerer maksimumsantall for behov som er gyldig for linjen.</span><span class="sxs-lookup"><span data-stu-id="22afb-182">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="22afb-183">**Enhet:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="22afb-183">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="22afb-184">Dette feltet definerer måleenheten som minimums- og maksimumsantallet viser til.</span><span class="sxs-lookup"><span data-stu-id="22afb-184">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="22afb-185">**Måleenhetslag:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="22afb-185">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="22afb-186">Dette feltet definerer måleenheten for behov som er gyldig for linjen.</span><span class="sxs-lookup"><span data-stu-id="22afb-186">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="22afb-187">(Hvis du vil ha mer informasjon, kan du se delen [Opprett måleenhetslag for sporing](#unit-tiers) tidligere i dette emnet.)</span><span class="sxs-lookup"><span data-stu-id="22afb-187">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="22afb-188">**Tilordne sporkriterier:** _Vurder antall_</span><span class="sxs-lookup"><span data-stu-id="22afb-188">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="22afb-189">Følgende verdier er tilgjengelige i dette feltet:</span><span class="sxs-lookup"><span data-stu-id="22afb-189">The following values are available in this field:</span></span>

        - <span data-ttu-id="22afb-190">**Anta tom** – dette systemet bør anta at alle lokasjonene i plukkområdet er tomme og bør ikke kontrollere disse lokasjonene for beholdning.</span><span class="sxs-lookup"><span data-stu-id="22afb-190">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="22afb-191">**Vurder antall** – systemet bør kontrollere lokasjonene i plukkområdet for beholdning og bør hoppe over eventuelle lokasjoner som ikke er tomme.</span><span class="sxs-lookup"><span data-stu-id="22afb-191">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>

    - <span data-ttu-id="22afb-192">**Direktivkode:** _Sporing_</span><span class="sxs-lookup"><span data-stu-id="22afb-192">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="22afb-193">Dette feltet definerer lokasjonsdirektivet som brukes til å finne plukklokasjonen for etterfyllingsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="22afb-193">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="22afb-194">**Overflytlokasjon:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="22afb-194">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="22afb-195">Dette feltet definerer den lokasjonen som det er satt inn hvis det ikke finnes en lokasjon for antallet når linjen behandles.</span><span class="sxs-lookup"><span data-stu-id="22afb-195">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="22afb-196">**Tillat la være:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="22afb-196">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="22afb-197">Hvis dette alternativet er satt til *Ja* , hvis et behov ikke kan spores, opprettes det bevegelsesarbeid for å få beholdning ut av lokasjoner der det er beholdning, men der ingenting var ble sporet.</span><span class="sxs-lookup"><span data-stu-id="22afb-197">When this option is set to *Yes* , if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="22afb-198">Malen kjøres deretter på nytt.</span><span class="sxs-lookup"><span data-stu-id="22afb-198">The template is then run again.</span></span> <span data-ttu-id="22afb-199">Denne gangen ignorerer beholdningen på lokasjonene.</span><span class="sxs-lookup"><span data-stu-id="22afb-199">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="22afb-200">Denne funksjonaliteten fungerer best når **Tilordne sporkriterier** er satt til _Vurder antall_.</span><span class="sxs-lookup"><span data-stu-id="22afb-200">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="22afb-201">**Fast lokasjonsbruk:** _Bare faste lokasjoner for produktet_</span><span class="sxs-lookup"><span data-stu-id="22afb-201">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="22afb-202">Følgende verdier er tilgjengelige i dette feltet:</span><span class="sxs-lookup"><span data-stu-id="22afb-202">The following values are available in this field:</span></span>

        - <span data-ttu-id="22afb-203">**Faste og ikke-faste lokasjoner** – systemet bør ikke begrenses til å bruke bare faste lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="22afb-203">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="22afb-204">**Bare faste lokasjoner for produktet** – systemet skal bare spore til lokasjoner som er faste lokasjoner for produktet.</span><span class="sxs-lookup"><span data-stu-id="22afb-204">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="22afb-205">**Bare faste lokasjoner for produktvarianten** – systemet skal bare spore til lokasjoner som er faste lokasjoner for produktvarianten.</span><span class="sxs-lookup"><span data-stu-id="22afb-205">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

1. <span data-ttu-id="22afb-206">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="22afb-206">Select **Save**.</span></span>
1. <span data-ttu-id="22afb-207">Velg **Ny** for å opprett en ny mallinje.</span><span class="sxs-lookup"><span data-stu-id="22afb-207">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="22afb-208">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="22afb-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="22afb-209">**Sekvens:** _2_</span><span class="sxs-lookup"><span data-stu-id="22afb-209">**Sequence:** _2_</span></span>
    - <span data-ttu-id="22afb-210">**Beskrivelse:** _Annet_</span><span class="sxs-lookup"><span data-stu-id="22afb-210">**Description:** _Other_</span></span>
    - <span data-ttu-id="22afb-211">**Minimumsantall:** _1_</span><span class="sxs-lookup"><span data-stu-id="22afb-211">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="22afb-212">**Maksimumsantall:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="22afb-212">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="22afb-213">**Enhet:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="22afb-213">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="22afb-214">**Måleenhetslag:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="22afb-214">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="22afb-215">**Tilordne sporkriterier:** _Vurder antall_</span><span class="sxs-lookup"><span data-stu-id="22afb-215">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="22afb-216">**Direktivkode:** _Sporing_</span><span class="sxs-lookup"><span data-stu-id="22afb-216">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="22afb-217">**Overflytlokasjon:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="22afb-217">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="22afb-218">**Tillat la være:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="22afb-218">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="22afb-219">**Bruk faste lokasjoner:** _Faste og ikke-faste lokasjoner_</span><span class="sxs-lookup"><span data-stu-id="22afb-219">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="22afb-220">I spørringen for den andre linjen vil du nå angi kriteriene som brukes til å bestemme hvilke lokasjoner behovet etter linjen kan spores til.</span><span class="sxs-lookup"><span data-stu-id="22afb-220">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="22afb-221">Velg linjen der **Sekvens** -feltet er satt til *2*.</span><span class="sxs-lookup"><span data-stu-id="22afb-221">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="22afb-222">Velg **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="22afb-222">Select **Edit query**.</span></span>
1. <span data-ttu-id="22afb-223">På **Område** -fanen velger du **Legg til** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="22afb-223">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="22afb-224">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="22afb-224">On the new line, set the following values:</span></span>

    - <span data-ttu-id="22afb-225">**Tabell:** *Plasseringer*</span><span class="sxs-lookup"><span data-stu-id="22afb-225">**Table:** *Locations*</span></span>
    - <span data-ttu-id="22afb-226">**Avledet tabell:** *Lokasjoner*</span><span class="sxs-lookup"><span data-stu-id="22afb-226">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="22afb-227">**Felt:** *ID for lokasjonsprofil*</span><span class="sxs-lookup"><span data-stu-id="22afb-227">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="22afb-228">**Kriterier:** *Plukk-06* (Velg dobbelt plusstegn \[**++**\] i feltet for å utvide listen, og velg deretter *Plukk-06* - *Plukkområde 6*.)</span><span class="sxs-lookup"><span data-stu-id="22afb-228">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="22afb-229">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="22afb-229">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="22afb-230">Konfigurer lokasjonsdirektiver</span><span class="sxs-lookup"><span data-stu-id="22afb-230">Set up location directives</span></span>

<span data-ttu-id="22afb-231">Minst ett lokasjonsdirektiv må være satt opp for å støtte sporingsplukkinger.</span><span class="sxs-lookup"><span data-stu-id="22afb-231">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="22afb-232">Bruk fremgangsmåtene i denne delen til å definere et nytt *lokasjonsdirektiv for etterfylling* for sporingsplukkinger.</span><span class="sxs-lookup"><span data-stu-id="22afb-232">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="22afb-233">Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.</span><span class="sxs-lookup"><span data-stu-id="22afb-233">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="22afb-234">I den venstre ruten i **Arbeidsordretype** -feltet velger du *Etterfylling*.</span><span class="sxs-lookup"><span data-stu-id="22afb-234">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="22afb-235">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="22afb-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="22afb-236">I toppteksten for det nye lokasjonsdirektivet angir *61 Sporingsplukk* i **Navn** -feltet.</span><span class="sxs-lookup"><span data-stu-id="22afb-236">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="22afb-237">Konfigurer Lokasjonsdirektiv-hurtigfanen</span><span class="sxs-lookup"><span data-stu-id="22afb-237">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="22afb-238">Angi følgende verdier i **Lokasjonsdirektiver** -hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="22afb-238">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="22afb-239">Godta standardverdiene for alle de andre feltene.</span><span class="sxs-lookup"><span data-stu-id="22afb-239">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="22afb-240">**Arbeidstype:** _Plukk_</span><span class="sxs-lookup"><span data-stu-id="22afb-240">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="22afb-241">**Område:** _6_</span><span class="sxs-lookup"><span data-stu-id="22afb-241">**Site:** _6_</span></span>
    - <span data-ttu-id="22afb-242">**Lager:** _61_</span><span class="sxs-lookup"><span data-stu-id="22afb-242">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="22afb-243">**Direktivkode:** _Sporing_</span><span class="sxs-lookup"><span data-stu-id="22afb-243">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="22afb-244">Velg **Lagre** for å gjøre **Linjer** -hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="22afb-244">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="22afb-245">Konfigurere Linjer-hurtigfanen</span><span class="sxs-lookup"><span data-stu-id="22afb-245">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="22afb-246">På hurtigfanen **Linjer** velger du **Ny** for å opprette en linje.</span><span class="sxs-lookup"><span data-stu-id="22afb-246">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="22afb-247">På den nye linjen angir du følgende verdier.</span><span class="sxs-lookup"><span data-stu-id="22afb-247">On the new line, set the following values.</span></span> <span data-ttu-id="22afb-248">Godta standardverdiene for alle de andre feltene.</span><span class="sxs-lookup"><span data-stu-id="22afb-248">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="22afb-249">**Fra-antall:** _0_</span><span class="sxs-lookup"><span data-stu-id="22afb-249">**From quantity:** _0_</span></span>
    - <span data-ttu-id="22afb-250">**Til antall:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="22afb-250">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="22afb-251">Velg **Lagre** for å gjøre **Lokasjonsdirektivhandlinger** -hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="22afb-251">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="22afb-252">Konfigurer Handlinger for lokasjonsdirektiv-hurtigfanen</span><span class="sxs-lookup"><span data-stu-id="22afb-252">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="22afb-253">På hurtigfanen **Handlinger for lokasjonsdirektiv** velger du **Ny** for å opprette en linje.</span><span class="sxs-lookup"><span data-stu-id="22afb-253">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="22afb-254">På den nye linjen angir du følgende verdier.</span><span class="sxs-lookup"><span data-stu-id="22afb-254">On the new line, set the following values.</span></span> <span data-ttu-id="22afb-255">Godta standardverdiene for alle de andre feltene.</span><span class="sxs-lookup"><span data-stu-id="22afb-255">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="22afb-256">**Navn:** _Bulk_</span><span class="sxs-lookup"><span data-stu-id="22afb-256">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="22afb-257">**Strategi:** _Ingen_</span><span class="sxs-lookup"><span data-stu-id="22afb-257">**Strategy:** _None_</span></span>

1. <span data-ttu-id="22afb-258">Velg **Lagre** for å aktivere **Rediger spørring** -knappen.</span><span class="sxs-lookup"><span data-stu-id="22afb-258">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="22afb-259">Rediger spørringen</span><span class="sxs-lookup"><span data-stu-id="22afb-259">Edit the query</span></span>

1. <span data-ttu-id="22afb-260">I **Handlinger for lokasjonsdirektiv** -hurtigfanen velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="22afb-260">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="22afb-261">På **Område** -fanen velger du **Legg til** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="22afb-261">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="22afb-262">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="22afb-262">On the new line, set the following values:</span></span>

    - <span data-ttu-id="22afb-263">**Tabell:** *Plasseringer*</span><span class="sxs-lookup"><span data-stu-id="22afb-263">**Table:** *Locations*</span></span>
    - <span data-ttu-id="22afb-264">**Avledet tabell:** *Lokasjoner*</span><span class="sxs-lookup"><span data-stu-id="22afb-264">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="22afb-265">**Felt:** *Sone-ID*</span><span class="sxs-lookup"><span data-stu-id="22afb-265">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="22afb-266">**Kriterier:** *Bulk* (Velg dobbelt plusstegn \[**++**\] i feltet for å utvide listen, og velg deretter *Bulk*.)</span><span class="sxs-lookup"><span data-stu-id="22afb-266">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="22afb-267">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="22afb-267">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="22afb-268">Scenario</span><span class="sxs-lookup"><span data-stu-id="22afb-268">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="22afb-269">Definer scenariet</span><span class="sxs-lookup"><span data-stu-id="22afb-269">Set up the scenario</span></span>

<span data-ttu-id="22afb-270">I dette scenariet bruker du de innebygde eksempeldataene, og oppretter postene som er beskrevet i denne delen.</span><span class="sxs-lookup"><span data-stu-id="22afb-270">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="22afb-271">Bruke USMF-eksempeldataene</span><span class="sxs-lookup"><span data-stu-id="22afb-271">Use the USMF sample data</span></span>

<span data-ttu-id="22afb-272">For å arbeide deg gjennom dette scenariet ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert.</span><span class="sxs-lookup"><span data-stu-id="22afb-272">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="22afb-273">Du må også velge den juridiske enheten **USMF** før du begynner.</span><span class="sxs-lookup"><span data-stu-id="22afb-273">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="22afb-274">Opprette behov</span><span class="sxs-lookup"><span data-stu-id="22afb-274">Create demand</span></span>

<span data-ttu-id="22afb-275">Følg denne fremgangsmåten for å opprette behovet du vil bruke sporing på.</span><span class="sxs-lookup"><span data-stu-id="22afb-275">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="22afb-276">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="22afb-276">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="22afb-277">Velg **Ny** for å opprette en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="22afb-277">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="22afb-278">I **Opprett salgsordre** -dialogboksen, i **Kundekonto** -feltet, velger du _US-007_.</span><span class="sxs-lookup"><span data-stu-id="22afb-278">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="22afb-279">I **Lager** -feltet velger du _61_.</span><span class="sxs-lookup"><span data-stu-id="22afb-279">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="22afb-280">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="22afb-280">Select **OK**.</span></span>
1. <span data-ttu-id="22afb-281">Den nye salgsordren åpnes.</span><span class="sxs-lookup"><span data-stu-id="22afb-281">The new sales order is opened.</span></span> <span data-ttu-id="22afb-282">Det inneholder en tom linje på **Salgsordrelinjer** -hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="22afb-282">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="22afb-283">På denne linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="22afb-283">On this line, set the following values:</span></span>

    - <span data-ttu-id="22afb-284">**Vare:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="22afb-284">**Item:** _L0101_</span></span>
    - <span data-ttu-id="22afb-285">**Antall:** _20_</span><span class="sxs-lookup"><span data-stu-id="22afb-285">**Quantity:** _20_</span></span>

1. <span data-ttu-id="22afb-286">Velg **Legg til linje** for å legge til en ny linje, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="22afb-286">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="22afb-287">**Vare:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="22afb-287">**Item:** _T0100_</span></span>
    - <span data-ttu-id="22afb-288">**Antall:** _8_</span><span class="sxs-lookup"><span data-stu-id="22afb-288">**Quantity:** _8_</span></span>

1. <span data-ttu-id="22afb-289">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="22afb-289">Select **Save**.</span></span>
1. <span data-ttu-id="22afb-290">Velg **Ny** for å opprette en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="22afb-290">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="22afb-291">I **Opprett salgsordre** -dialogboksen, i **Kundekonto** -feltet, velger du _US-008_.</span><span class="sxs-lookup"><span data-stu-id="22afb-291">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="22afb-292">I **Lager** -feltet velger du _61_.</span><span class="sxs-lookup"><span data-stu-id="22afb-292">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="22afb-293">Den nye salgsordren åpnes.</span><span class="sxs-lookup"><span data-stu-id="22afb-293">The new sales order is opened.</span></span> <span data-ttu-id="22afb-294">Det inneholder en tom linje på **Salgsordrelinjer** -hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="22afb-294">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="22afb-295">På denne linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="22afb-295">On this line, set the following values:</span></span>

    - <span data-ttu-id="22afb-296">**Vare:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="22afb-296">**Item:** _T0100_</span></span>
    - <span data-ttu-id="22afb-297">**Antall:** _1_</span><span class="sxs-lookup"><span data-stu-id="22afb-297">**Quantity:** _1_</span></span>

1. <span data-ttu-id="22afb-298">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="22afb-298">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="22afb-299">Gå gjennom et vanlig sporingsscenario</span><span class="sxs-lookup"><span data-stu-id="22afb-299">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="22afb-300">Når alle forutsetningselementene er på plass, som beskrevet i den forrige delen, er du klar til å prøve ut funksjonen ved å jobbe gjennom hver øvelse i denne delen.</span><span class="sxs-lookup"><span data-stu-id="22afb-300">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="22afb-301">Generer behov</span><span class="sxs-lookup"><span data-stu-id="22afb-301">Generate demand</span></span>

1. <span data-ttu-id="22afb-302">Gå til **Lagerstyring \> Oppsett \> Etterfylling \> Sporingsmaler** , og velg sporingsmalen du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="22afb-302">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates** , and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="22afb-303">Velg **Generelt behov** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="22afb-303">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="22afb-304">Denne kommandoen evaluerer alle behov som er i systemet, og som samsvarer med sporingsmalspørringen.</span><span class="sxs-lookup"><span data-stu-id="22afb-304">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="22afb-305">Det totale behovet på tvers av alle ordrer konsolideres deretter på én linje per antall/måleenhet.</span><span class="sxs-lookup"><span data-stu-id="22afb-305">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="22afb-306">En informasjonsmelding vises når prosessen er fullført.</span><span class="sxs-lookup"><span data-stu-id="22afb-306">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="22afb-307">Sporingsbehov</span><span class="sxs-lookup"><span data-stu-id="22afb-307">Slotting demand</span></span>

<span data-ttu-id="22afb-308">*Sporingsbehovet* viser resultatene av behovsgenerering, basert på oppsettet til sporingsmalen.</span><span class="sxs-lookup"><span data-stu-id="22afb-308">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="22afb-309">I handlingsruten velger **Sporingsbehov** for å vise resultatene fra **Generelt behov** -kommandoen.</span><span class="sxs-lookup"><span data-stu-id="22afb-309">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="22afb-310">Linjene i sporingsbehov kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="22afb-310">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="22afb-311">Du kan slette en linje, legge til en ny linje eller redigere linjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="22afb-311">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="22afb-312">Du kan redigere behovet manuelt, eller du kan importere den fra et eksternt system ved hjelp av dataadministrasjon.</span><span class="sxs-lookup"><span data-stu-id="22afb-312">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="22afb-313">Det som er oppgitt i sporingsbehov, vil bli brukt i neste trinn, uansett hvor den kom fra.</span><span class="sxs-lookup"><span data-stu-id="22afb-313">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="22afb-314">Finn behov</span><span class="sxs-lookup"><span data-stu-id="22afb-314">Locate demand</span></span>

<span data-ttu-id="22afb-315">Etter at behov er generert, må du bruke **Finn behov** -kommandoen til å generere *sporingsplanen*.</span><span class="sxs-lookup"><span data-stu-id="22afb-315">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="22afb-316">Velg **Finn behov** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="22afb-316">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="22afb-317">Sporingsprosessen kjører.</span><span class="sxs-lookup"><span data-stu-id="22afb-317">The slotting process runs.</span></span> <span data-ttu-id="22afb-318">En informasjonsmelding vises når prosessen er fullført.</span><span class="sxs-lookup"><span data-stu-id="22afb-318">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="22afb-319">Sporingsplan</span><span class="sxs-lookup"><span data-stu-id="22afb-319">Slotting plan</span></span>

<span data-ttu-id="22afb-320">Sporingsplanen viser lokasjonen som hver vare/antall ble tilordnet til, om overflyt ble brukt, om det ble opprettet en arbeidslinje og mallinjen som ble brukt.</span><span class="sxs-lookup"><span data-stu-id="22afb-320">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="22afb-321">**Alle etterspørsler som ikke kunne spores, er uthevet i rødt.**</span><span class="sxs-lookup"><span data-stu-id="22afb-321">**Any demand that could not be slotted is highlighted in red.**</span></span>

- <span data-ttu-id="22afb-322">I handlingsruten velger **Sporingsplan** for å vise resultatene.</span><span class="sxs-lookup"><span data-stu-id="22afb-322">On the Action Pane, select **Slotting plan** to view the results.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="22afb-323">Opprett etterfylling</span><span class="sxs-lookup"><span data-stu-id="22afb-323">Create replenishment</span></span>

<span data-ttu-id="22afb-324">Etter at sporingsplanen er opprettet, må du opprette *Etterfyllingsarbeid* , basert på planen.</span><span class="sxs-lookup"><span data-stu-id="22afb-324">After the slotting plan has been created, you must create *replenishment work* , based on the plan.</span></span>

- <span data-ttu-id="22afb-325">Velg **Kjør etterfylling** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="22afb-325">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="22afb-326">En informasjonsmelding vises når prosessen er fullført.</span><span class="sxs-lookup"><span data-stu-id="22afb-326">An informational message appears when the process is completed.</span></span> <span data-ttu-id="22afb-327">Denne meldingen angir antallet hoder som ble opprettet for build-ID-en for arbeid.</span><span class="sxs-lookup"><span data-stu-id="22afb-327">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="22afb-328">Lokasjonsdirektiver som vil bli brukt, identifiseres basert på direktivkoden som er angitt på hver mallinje.</span><span class="sxs-lookup"><span data-stu-id="22afb-328">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="22afb-329">Tips!</span><span class="sxs-lookup"><span data-stu-id="22afb-329">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="22afb-330">Definere automatisk sporing</span><span class="sxs-lookup"><span data-stu-id="22afb-330">Set up automatic slotting</span></span>

<span data-ttu-id="22afb-331">Når alle nødvendige elementer er på plass, kan du konfigurere sporing til å kjøre automatisk ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="22afb-331">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="22afb-332">Gå til **Lagerstyring \> Etterfylling \> Kjør sporing**.</span><span class="sxs-lookup"><span data-stu-id="22afb-332">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="22afb-333">Angi sporingstrinn som skal kjøres.</span><span class="sxs-lookup"><span data-stu-id="22afb-333">Specify the slotting steps to run.</span></span> <span data-ttu-id="22afb-334">Velg ett eller flere av følgende sporingstrinn:</span><span class="sxs-lookup"><span data-stu-id="22afb-334">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="22afb-335">Generer behov</span><span class="sxs-lookup"><span data-stu-id="22afb-335">Generate demand</span></span>
    - <span data-ttu-id="22afb-336">Finn behov</span><span class="sxs-lookup"><span data-stu-id="22afb-336">Locate demand</span></span>
    - <span data-ttu-id="22afb-337">Opprett etterfyllingsarbeid</span><span class="sxs-lookup"><span data-stu-id="22afb-337">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="22afb-338">Sporingstrinnene er progressive.</span><span class="sxs-lookup"><span data-stu-id="22afb-338">The slotting steps are progressive.</span></span> <span data-ttu-id="22afb-339">Hvis du vil velge *Finn behov* , må du først velge *Generer behov*.</span><span class="sxs-lookup"><span data-stu-id="22afb-339">If you want to select *Locate demand* , you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="22afb-340">Angi hvilken sporingsmal som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="22afb-340">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="22afb-341">Angi at regelmessigheten skal kjøres automatisk hvis du vil.</span><span class="sxs-lookup"><span data-stu-id="22afb-341">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="22afb-342">For øvelsene i scenarioet må du **ikke** sette opp automatisk sporing.</span><span class="sxs-lookup"><span data-stu-id="22afb-342">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
