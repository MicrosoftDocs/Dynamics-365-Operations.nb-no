---
title: Lagersporing
description: Dette emnet inneholder informasjon om lagersporing. Med lagersporing kan du konsolidere behov etter vare og måleenhet fra ordrer som har statusen bestilt, reservert eller frigitt. Det hjelper lagerledere å planlegge plukklokasjoner før de frigir ordrer til lageret og oppretter plukkarbeid.
author: mirzaab
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0dd1f42b7bb337ccb65b7e4bdd9d307d074ae0d0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838160"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="89b95-105">Lagersporing</span><span class="sxs-lookup"><span data-stu-id="89b95-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89b95-106">Flere lagersporingsfunksjoner er tilgjengelig for å hjelpe lagerledere å planlegge plukklokasjoner før de frigir ordrer til lageret og oppretter plukkarbeid.</span><span class="sxs-lookup"><span data-stu-id="89b95-106">Several warehouse slotting features are available to help warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

<span data-ttu-id="89b95-107">Med *Lagersporing* kan du konsolidere behov etter vare og måleenhet fra ordrer som har statusen *bestilt*, *reservert* eller *frigitt*.</span><span class="sxs-lookup"><span data-stu-id="89b95-107">The *Warehouse slotting feature* lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="89b95-108">Det genererte behovet kan deretter brukes på lokasjoner som skal brukes til plukking, basert på antall, enhet, fysiske dimensjoner, faste lokasjoner og mer.</span><span class="sxs-lookup"><span data-stu-id="89b95-108">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="89b95-109">Etter at sporingsplanen er opprettet, kan etter fyllingsarbeid opprettes for å hente riktig lagermengde til hver lokasjon.</span><span class="sxs-lookup"><span data-stu-id="89b95-109">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="89b95-110">Med funksjonen *Lagersporing for overføringsordrer* kan lagerledere å etterfylle plukklokasjoner, basert på behov fra overføringsordrer som ennå ikke er frigitt til lageret.</span><span class="sxs-lookup"><span data-stu-id="89b95-110">The *Warehouse slotting for transfer orders* feature lets warehouse managers replenish picking locations, based on demand from transfer orders that aren't yet released to the warehouse.</span></span> <span data-ttu-id="89b95-111">Det sikrer at plukklokasjoner vil inkludere alle varene som kreves for overføringsordrene etter at de er frigitt til lager.</span><span class="sxs-lookup"><span data-stu-id="89b95-111">It ensures that picking locations will include all the items that are required for the transfer orders after they are released to warehouse.</span></span> <span data-ttu-id="89b95-112">Denne funksjonen krever at du også aktiverer funksjonen *Lagersporingsfunksjon*.</span><span class="sxs-lookup"><span data-stu-id="89b95-112">This feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span>

<span data-ttu-id="89b95-113">Funksjonen *Forbedringer av lagersporingsfordeling* legger til et alternativ for mallinjene som brukes av funksjonen *Lagersporing*.</span><span class="sxs-lookup"><span data-stu-id="89b95-113">The *Warehouse slotting allocation enhancements* feature adds an option for the template lines that are used by the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="89b95-114">Alternativet gjør det mulig for systemet å ta hensyn til den eksisterende lagerbeholdningen på en målplassering.</span><span class="sxs-lookup"><span data-stu-id="89b95-114">The option enables the system to consider existing on-hand inventory at a target location.</span></span> <span data-ttu-id="89b95-115">Derfor kan det genereres færre etterfyllinger for sporing.</span><span class="sxs-lookup"><span data-stu-id="89b95-115">Therefore, fewer replenishments might be generated for slotting.</span></span> <span data-ttu-id="89b95-116">Funksjonen *Forbedringer av lagersporingsfordeling* krever at du også aktiverer funksjonen *Lagersporing*.</span><span class="sxs-lookup"><span data-stu-id="89b95-116">The *Warehouse slotting allocation enhancements* feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="89b95-117">Den kan også brukes sammen med *Lagersporing for overføringsordrer*.</span><span class="sxs-lookup"><span data-stu-id="89b95-117">It can optionally be used together with the *Warehouse slotting for transfer orders* feature.</span></span>

## <a name="turn-on-the-warehouse-slotting-features"></a><span data-ttu-id="89b95-118">Aktivere lagersporingsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="89b95-118">Turn on the warehouse slotting features</span></span>

<span data-ttu-id="89b95-119">Før du kan bruke disse funksjonene, må de være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="89b95-119">Before you can use these features, they must be turned on in your system.</span></span> <span data-ttu-id="89b95-120">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere statusen for funksjonene og aktivere dem hvis nødvendig.</span><span class="sxs-lookup"><span data-stu-id="89b95-120">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="89b95-121">Aktiver følgende funksjoner etter behov:</span><span class="sxs-lookup"><span data-stu-id="89b95-121">Turn on the following features as required:</span></span>

- <span data-ttu-id="89b95-122">Lagersporingsfunksjon</span><span class="sxs-lookup"><span data-stu-id="89b95-122">Warehouse slotting feature</span></span>
- <span data-ttu-id="89b95-123">Lagersporing for overføringsordrer</span><span class="sxs-lookup"><span data-stu-id="89b95-123">Warehouse slotting for transfer orders</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="89b95-124">Funksjonen *Lagersporingsfunksjon* må være aktivert før denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="89b95-124">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

- <span data-ttu-id="89b95-125">Forbedringer i tildeling av lagersporing</span><span class="sxs-lookup"><span data-stu-id="89b95-125">Warehouse slotting allocation enhancements</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="89b95-126">Funksjonen *Lagersporingsfunksjon* må være aktivert før denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="89b95-126">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="89b95-127">Definere lagersporing</span><span class="sxs-lookup"><span data-stu-id="89b95-127">Set up warehouse slotting</span></span>

<span data-ttu-id="89b95-128">Hvis du vil bruke lagersporing, må du definere følgende elementer i systemet:</span><span class="sxs-lookup"><span data-stu-id="89b95-128">To use warehouse slotting, you must set up the following elements in your system:</span></span>

- <span data-ttu-id="89b95-129">Måleenhetsnivåer for sporing</span><span class="sxs-lookup"><span data-stu-id="89b95-129">Slotting unit of measure tiers</span></span>
- <span data-ttu-id="89b95-130">Direktivkoder</span><span class="sxs-lookup"><span data-stu-id="89b95-130">Directive codes</span></span>
- <span data-ttu-id="89b95-131">Sporingsmaler</span><span class="sxs-lookup"><span data-stu-id="89b95-131">Slotting templates</span></span>
- <span data-ttu-id="89b95-132">Lokasjonsdirektiver</span><span class="sxs-lookup"><span data-stu-id="89b95-132">Location directives</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="89b95-133">Opprett måleenhetslag for sporing</span><span class="sxs-lookup"><span data-stu-id="89b95-133">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="89b95-134">Måleenhetslag gjør det mulig å gruppere flere måleenheter sammen for å sporing.</span><span class="sxs-lookup"><span data-stu-id="89b95-134">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="89b95-135">Hvis for eksempel bokser med flere størrelser plukkes fra samme boksplukkingsområde, kan ett lag opprettes for alle størrelsene.</span><span class="sxs-lookup"><span data-stu-id="89b95-135">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="89b95-136">**Det må opprettes en linje for hver måleenhet som skal være en del av laget.**</span><span class="sxs-lookup"><span data-stu-id="89b95-136">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="89b95-137">Gå til **Lagerstyring \> Oppsett \> Etterfylling \> Måleenhetslag for sporing**.</span><span class="sxs-lookup"><span data-stu-id="89b95-137">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="89b95-138">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="89b95-138">Select **New**.</span></span>
1. <span data-ttu-id="89b95-139">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="89b95-139">In the header, set the following values:</span></span>

    - <span data-ttu-id="89b95-140">**Måleenhetslag:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="89b95-140">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="89b95-141">**Beskrivelse:** *Hver bokspall*</span><span class="sxs-lookup"><span data-stu-id="89b95-141">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="89b95-142">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="89b95-142">Select **Save**.</span></span>
1. <span data-ttu-id="89b95-143">På **Måleenhet**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="89b95-143">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="89b95-144">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="89b95-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="89b95-145">**Enhet:** *Boks*</span><span class="sxs-lookup"><span data-stu-id="89b95-145">**Unit:** *Box*</span></span>
    - <span data-ttu-id="89b95-146">**Beskrivelse:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="89b95-146">**Description:** Leave this field blank.</span></span> <span data-ttu-id="89b95-147">Den fylles ut automatisk når du lagrer endringene.</span><span class="sxs-lookup"><span data-stu-id="89b95-147">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="89b95-148">**Enhetsklasse:** *Antall*</span><span class="sxs-lookup"><span data-stu-id="89b95-148">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="89b95-149">Velg **Ny** for å legge til en ny linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="89b95-149">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="89b95-150">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="89b95-150">On the new line, set the following values:</span></span>

    - <span data-ttu-id="89b95-151">**Enhet:** *ea*</span><span class="sxs-lookup"><span data-stu-id="89b95-151">**Unit:** *ea*</span></span>
    - <span data-ttu-id="89b95-152">**Beskrivelse:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="89b95-152">**Description:** Leave this field blank.</span></span> <span data-ttu-id="89b95-153">Den fylles ut automatisk når du lagrer endringene.</span><span class="sxs-lookup"><span data-stu-id="89b95-153">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="89b95-154">**Enhetsklasse:** *Antall*</span><span class="sxs-lookup"><span data-stu-id="89b95-154">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="89b95-155">Velg **Ny** for å legge til en tredje linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="89b95-155">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="89b95-156">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="89b95-156">On the new line, set the following values:</span></span>

    - <span data-ttu-id="89b95-157">**Enhet:** *PL*</span><span class="sxs-lookup"><span data-stu-id="89b95-157">**Unit:** *PL*</span></span>
    - <span data-ttu-id="89b95-158">**Beskrivelse:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="89b95-158">**Description:** Leave this field blank.</span></span> <span data-ttu-id="89b95-159">Den fylles ut automatisk når du lagrer endringene.</span><span class="sxs-lookup"><span data-stu-id="89b95-159">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="89b95-160">**Enhetsklasse:** *Antall*</span><span class="sxs-lookup"><span data-stu-id="89b95-160">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="89b95-161">Velg **Lagre** for å lagre laget.</span><span class="sxs-lookup"><span data-stu-id="89b95-161">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="89b95-162">Opprette en direktivkode for sporing</span><span class="sxs-lookup"><span data-stu-id="89b95-162">Create a directive code for slotting</span></span>

<span data-ttu-id="89b95-163">Du må velge direktivkoden som skal knyttes til en mal.</span><span class="sxs-lookup"><span data-stu-id="89b95-163">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="89b95-164">Gå til **Lagerstyring \> Oppsett \> Direktivkoder**.</span><span class="sxs-lookup"><span data-stu-id="89b95-164">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="89b95-165">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="89b95-165">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="89b95-166">I **Direktivkode**-feltet angir du *Sporing*.</span><span class="sxs-lookup"><span data-stu-id="89b95-166">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="89b95-167">I **Direktivbeskrivelse**-feltet angir du *Sporing*.</span><span class="sxs-lookup"><span data-stu-id="89b95-167">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="89b95-168">Definere sporingsmaler</span><span class="sxs-lookup"><span data-stu-id="89b95-168">Set up slotting templates</span></span>

<span data-ttu-id="89b95-169">Hver sporingsmal styrer hvordan beholdningen tilordnes lokasjoner for et bestemt lager.</span><span class="sxs-lookup"><span data-stu-id="89b95-169">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="89b95-170">Hver mal må inneholde en linje for hver sporingsspesifikasjon.</span><span class="sxs-lookup"><span data-stu-id="89b95-170">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="89b95-171">Bruk fremgangsmåtene i denne delen til å definere sporingsmaler.</span><span class="sxs-lookup"><span data-stu-id="89b95-171">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="89b95-172">Gå til **Lagerstyring \> Oppsett \> Etterfylling \> Sporingsmaler**.</span><span class="sxs-lookup"><span data-stu-id="89b95-172">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="89b95-173">Velg **Ny** for å opprette en mal.</span><span class="sxs-lookup"><span data-stu-id="89b95-173">Select **New** to create a template.</span></span>

<span data-ttu-id="89b95-174">Deretter må du definere maltoppteksten, sporingsspesifikasjoner og lokasjonsdirektiver som forklart nedenfor.</span><span class="sxs-lookup"><span data-stu-id="89b95-174">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span> <span data-ttu-id="89b95-175">Oppsettet for sporing for overføringsordrer ligner oppsettet for sporing for salgsordrer, men **Behovstype**-feltet angir *Overføringsordrer* i stedet for *Salgsordre*.</span><span class="sxs-lookup"><span data-stu-id="89b95-175">The setup for slotting for transfer orders resembles the setup for slotting for sales orders, but the **Demand type** field is set *Transfer orders* instead of *Sales order*.</span></span>

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a><span data-ttu-id="89b95-176">Definere hodet for en sporingsmal for salgsordre</span><span class="sxs-lookup"><span data-stu-id="89b95-176">Set up the header for a sales order slotting template</span></span>

1. <span data-ttu-id="89b95-177">Angi følgende verdier i toppteksten for malen:</span><span class="sxs-lookup"><span data-stu-id="89b95-177">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="89b95-178">**Sporingsmal:** _61_</span><span class="sxs-lookup"><span data-stu-id="89b95-178">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="89b95-179">**Beskrivelse:** _61_</span><span class="sxs-lookup"><span data-stu-id="89b95-179">**Description:** _61_</span></span>
    - <span data-ttu-id="89b95-180">**Behovstype:** *Salgsordre*</span><span class="sxs-lookup"><span data-stu-id="89b95-180">**Demand type:** *Sales order*</span></span>

        > [!NOTE]
        > <span data-ttu-id="89b95-181">For øyeblikket er *Salgsordrer* og *Overføringsordrer* de eneste behovstypene som støttes.</span><span class="sxs-lookup"><span data-stu-id="89b95-181">Currently, *Sales orders* and *Transfer orders* are the only demand types that are supported.</span></span> <span data-ttu-id="89b95-182">Du kan bare velge *Overføringsordrer* hvis funksjonen *Lagersporing for overføringsordrer* er aktivert.</span><span class="sxs-lookup"><span data-stu-id="89b95-182">You can select *Transfer orders* only if the *Warehouse Slotting for transfer orders* feature is turned on.</span></span>

    - <span data-ttu-id="89b95-183">**Behovsstrategi:** _Bestilt_</span><span class="sxs-lookup"><span data-stu-id="89b95-183">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="89b95-184">Følgende verdier er tilgjengelige i dette feltet:</span><span class="sxs-lookup"><span data-stu-id="89b95-184">The following values are available in this field:</span></span>

        - <span data-ttu-id="89b95-185">**Bestilt** – hele det bestilte antallet på salgsordren skal vurderes som behov.</span><span class="sxs-lookup"><span data-stu-id="89b95-185">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="89b95-186">**Reservert** – bare antallet for salgsordrelinjen som er reservert (fysisk og bestilt), skal vurderes som behov.</span><span class="sxs-lookup"><span data-stu-id="89b95-186">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>
        - <span data-ttu-id="89b95-187">**Frigitt** – Det frigitte antallet skal vurderes som behov.</span><span class="sxs-lookup"><span data-stu-id="89b95-187">**Released** – The released quantity should be considered demand.</span></span>

    - <span data-ttu-id="89b95-188">**Lager:** _61_</span><span class="sxs-lookup"><span data-stu-id="89b95-188">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="89b95-189">**Tillat at bølgebehov bruker ikke-reservert antall:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="89b95-189">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="89b95-190">Du kan også angi en spørring for å begrense omfanget av behovet som evalueres.</span><span class="sxs-lookup"><span data-stu-id="89b95-190">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="89b95-191">Definer sporingsspesifikasjoner for hver mal</span><span class="sxs-lookup"><span data-stu-id="89b95-191">Set up slotting specifications for each template</span></span>

<span data-ttu-id="89b95-192">For hver salgsordremal du oppretter, følger du disse trinnene for å legge til en linje for hver sporingsspesifikasjon.</span><span class="sxs-lookup"><span data-stu-id="89b95-192">For each sales order template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="89b95-193">På **Sporingsmaldetaljer**-hurtigfanen velger du **Ny** for å opprette en mallinje.</span><span class="sxs-lookup"><span data-stu-id="89b95-193">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="89b95-194">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="89b95-194">On the new line, set the following values:</span></span>

    - <span data-ttu-id="89b95-195">**Sekvens:** _1_</span><span class="sxs-lookup"><span data-stu-id="89b95-195">**Sequence:** _1_</span></span>
    - <span data-ttu-id="89b95-196">**Beskrivelse:** _Fast lokasjon_</span><span class="sxs-lookup"><span data-stu-id="89b95-196">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="89b95-197">**Minimumsantall:** _1_</span><span class="sxs-lookup"><span data-stu-id="89b95-197">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="89b95-198">Dette feltet definerer minimumsantall for behov som er nødvendig for linjen.</span><span class="sxs-lookup"><span data-stu-id="89b95-198">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="89b95-199">**Maksimalt antall:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="89b95-199">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="89b95-200">Dette feltet definerer maksimumsantall for behov som er gyldig for linjen.</span><span class="sxs-lookup"><span data-stu-id="89b95-200">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="89b95-201">**Enhet:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="89b95-201">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="89b95-202">Dette feltet definerer måleenheten som minimums- og maksimumsantallet viser til.</span><span class="sxs-lookup"><span data-stu-id="89b95-202">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="89b95-203">**Måleenhetslag:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="89b95-203">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="89b95-204">Dette feltet definerer måleenheten for behov som er gyldig for linjen.</span><span class="sxs-lookup"><span data-stu-id="89b95-204">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="89b95-205">(Hvis du vil ha mer informasjon, kan du se delen [Opprett måleenhetslag for sporing](#unit-tiers) tidligere i dette emnet.)</span><span class="sxs-lookup"><span data-stu-id="89b95-205">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="89b95-206">**Tilordne sporkriterier:** _Vurder antall_</span><span class="sxs-lookup"><span data-stu-id="89b95-206">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="89b95-207">Følgende verdier er tilgjengelige i dette feltet:</span><span class="sxs-lookup"><span data-stu-id="89b95-207">The following values are available in this field:</span></span>

        - <span data-ttu-id="89b95-208">**Anta tom** – dette systemet bør anta at alle lokasjonene i plukkområdet er tomme og bør ikke kontrollere disse lokasjonene for beholdning.</span><span class="sxs-lookup"><span data-stu-id="89b95-208">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="89b95-209">**Vurder antall** – systemet bør kontrollere lokasjonene i plukkområdet for beholdning og bør hoppe over eventuelle lokasjoner som ikke er tomme.</span><span class="sxs-lookup"><span data-stu-id="89b95-209">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>
        - <span data-ttu-id="89b95-210">**Vurder beholdning** – Systemet bør kontrollere om en mållokasjon inneholder ikke-reserverte antall for varen på behovslinjen.</span><span class="sxs-lookup"><span data-stu-id="89b95-210">**Consider on-hand** – The system should check whether any target location contains unreserved quantities for the item on the demand line.</span></span> <span data-ttu-id="89b95-211">Hvis antallet er stort nok til å oppfylle minst én enhet for behovs injen, reduseres den genererte sporingsplanposten med det tilgjengelige antallet.</span><span class="sxs-lookup"><span data-stu-id="89b95-211">If the quantity is large enough to satisfy at least one unit of the demand line, the generated slotting plan record is reduced by the available amount.</span></span> <span data-ttu-id="89b95-212">Hvis for eksempel behovet er 10 esker, og én eske er på lager, vil behovet som finnes, være ni esker.</span><span class="sxs-lookup"><span data-stu-id="89b95-212">For example, if the demand is 10 cases, and one case is on hand, the located demand will be nine cases.</span></span> <span data-ttu-id="89b95-213">Hvis behovet er 10 esker, og én eske er på lager, vil behovet som finnes, være 10 esker.</span><span class="sxs-lookup"><span data-stu-id="89b95-213">If the demand is 10 cases, and one each is on hand, the located demand will be 10 cases.</span></span> <span data-ttu-id="89b95-214">Denne verdien er bare tilgjengelig når funksjonen *Forbedringer i tildeling av lagersporing* er aktivert.</span><span class="sxs-lookup"><span data-stu-id="89b95-214">This value is available only when the *Warehouse slotting allocation enhancements* feature is turned on.</span></span>

    - <span data-ttu-id="89b95-215">**Direktivkode:** _Sporing_</span><span class="sxs-lookup"><span data-stu-id="89b95-215">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="89b95-216">Dette feltet definerer lokasjonsdirektivet som brukes til å finne plukklokasjonen for etterfyllingsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="89b95-216">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="89b95-217">**Overflytlokasjon:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="89b95-217">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="89b95-218">Dette feltet definerer den lokasjonen som det er satt inn hvis det ikke finnes en lokasjon for antallet når linjen behandles.</span><span class="sxs-lookup"><span data-stu-id="89b95-218">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="89b95-219">**Tillat la være:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="89b95-219">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="89b95-220">Hvis dette alternativet er satt til *Ja*, hvis et behov ikke kan spores, opprettes det bevegelsesarbeid for å få beholdning ut av lokasjoner der det er beholdning, men der ingenting var ble sporet.</span><span class="sxs-lookup"><span data-stu-id="89b95-220">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="89b95-221">Malen kjøres deretter på nytt.</span><span class="sxs-lookup"><span data-stu-id="89b95-221">The template is then run again.</span></span> <span data-ttu-id="89b95-222">Denne gangen ignorerer beholdningen på lokasjonene.</span><span class="sxs-lookup"><span data-stu-id="89b95-222">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="89b95-223">Denne funksjonaliteten fungerer best når **Tilordne sporkriterier** er satt til _Vurder antall_.</span><span class="sxs-lookup"><span data-stu-id="89b95-223">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="89b95-224">**Fast lokasjonsbruk:** _Bare faste lokasjoner for produktet_</span><span class="sxs-lookup"><span data-stu-id="89b95-224">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="89b95-225">Følgende verdier er tilgjengelige i dette feltet:</span><span class="sxs-lookup"><span data-stu-id="89b95-225">The following values are available in this field:</span></span>

        - <span data-ttu-id="89b95-226">**Faste og ikke-faste lokasjoner** – systemet bør ikke begrenses til å bruke bare faste lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="89b95-226">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="89b95-227">**Bare faste lokasjoner for produktet** – systemet skal bare spore til lokasjoner som er faste lokasjoner for produktet.</span><span class="sxs-lookup"><span data-stu-id="89b95-227">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="89b95-228">**Bare faste lokasjoner for produktvarianten** – systemet skal bare spore til lokasjoner som er faste lokasjoner for produktvarianten.</span><span class="sxs-lookup"><span data-stu-id="89b95-228">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

> [!NOTE]
> <span data-ttu-id="89b95-229">Hvis sporingsmalen inneholder minst én linje der feltet **Tilordne sporkriterier** er satt til å *Vurder beholdning*, vil ikke Tillat-vinduer være tillatt for noen linjer i malen.</span><span class="sxs-lookup"><span data-stu-id="89b95-229">If the slotting template contains at least one line where the **Assign slot criteria** field is set to *Consider on-hand*, let-ups are no longer allowed for any line in the template.</span></span>

1. <span data-ttu-id="89b95-230">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="89b95-230">Select **Save**.</span></span>
1. <span data-ttu-id="89b95-231">Velg **Ny** for å opprett en ny mallinje.</span><span class="sxs-lookup"><span data-stu-id="89b95-231">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="89b95-232">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="89b95-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="89b95-233">**Sekvens:** _2_</span><span class="sxs-lookup"><span data-stu-id="89b95-233">**Sequence:** _2_</span></span>
    - <span data-ttu-id="89b95-234">**Beskrivelse:** _Annet_</span><span class="sxs-lookup"><span data-stu-id="89b95-234">**Description:** _Other_</span></span>
    - <span data-ttu-id="89b95-235">**Minimumsantall:** _1_</span><span class="sxs-lookup"><span data-stu-id="89b95-235">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="89b95-236">**Maksimumsantall:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="89b95-236">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="89b95-237">**Enhet:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="89b95-237">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="89b95-238">**Måleenhetslag:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="89b95-238">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="89b95-239">**Tilordne sporkriterier:** _Vurder antall_</span><span class="sxs-lookup"><span data-stu-id="89b95-239">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="89b95-240">**Direktivkode:** _Sporing_</span><span class="sxs-lookup"><span data-stu-id="89b95-240">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="89b95-241">**Overflytlokasjon:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="89b95-241">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="89b95-242">**Tillat la være:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="89b95-242">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="89b95-243">**Bruk faste lokasjoner:** _Faste og ikke-faste lokasjoner_</span><span class="sxs-lookup"><span data-stu-id="89b95-243">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="89b95-244">I spørringen for den andre linjen vil du nå angi kriteriene som brukes til å bestemme hvilke lokasjoner behovet etter linjen kan spores til.</span><span class="sxs-lookup"><span data-stu-id="89b95-244">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="89b95-245">Velg linjen der **Sekvens**-feltet er satt til *2*.</span><span class="sxs-lookup"><span data-stu-id="89b95-245">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="89b95-246">Velg **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="89b95-246">Select **Edit query**.</span></span>
1. <span data-ttu-id="89b95-247">På **Område**-fanen velger du **Legg til** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="89b95-247">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="89b95-248">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="89b95-248">On the new line, set the following values:</span></span>

    - <span data-ttu-id="89b95-249">**Tabell:** *Plasseringer*</span><span class="sxs-lookup"><span data-stu-id="89b95-249">**Table:** *Locations*</span></span>
    - <span data-ttu-id="89b95-250">**Avledet tabell:** *Lokasjoner*</span><span class="sxs-lookup"><span data-stu-id="89b95-250">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="89b95-251">**Felt:** *ID for lokasjonsprofil*</span><span class="sxs-lookup"><span data-stu-id="89b95-251">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="89b95-252">**Kriterier:** *Plukk-06* (Velg dobbelt plusstegn \[**++**\] i feltet for å utvide listen, og velg deretter *Plukk-06* - *Plukkområde 6*.)</span><span class="sxs-lookup"><span data-stu-id="89b95-252">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="89b95-253">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="89b95-253">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="89b95-254">Konfigurer lokasjonsdirektiver</span><span class="sxs-lookup"><span data-stu-id="89b95-254">Set up location directives</span></span>

<span data-ttu-id="89b95-255">Minst ett lokasjonsdirektiv må være satt opp for å støtte sporingsplukkinger.</span><span class="sxs-lookup"><span data-stu-id="89b95-255">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="89b95-256">Bruk fremgangsmåtene i denne delen til å definere et nytt *lokasjonsdirektiv for etterfylling* for sporingsplukkinger.</span><span class="sxs-lookup"><span data-stu-id="89b95-256">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="89b95-257">Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.</span><span class="sxs-lookup"><span data-stu-id="89b95-257">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="89b95-258">I den venstre ruten i **Arbeidsordretype**-feltet velger du *Etterfylling*.</span><span class="sxs-lookup"><span data-stu-id="89b95-258">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="89b95-259">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="89b95-259">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="89b95-260">I toppteksten for det nye lokasjonsdirektivet angir *61 Sporingsplukk* i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="89b95-260">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>
1. <span data-ttu-id="89b95-261">I feltet **Sekvensnummer** godtar du standardverdien.</span><span class="sxs-lookup"><span data-stu-id="89b95-261">In the **Sequence number** field, accept the default value.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="89b95-262">Konfigurer Lokasjonsdirektiv-hurtigfanen</span><span class="sxs-lookup"><span data-stu-id="89b95-262">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="89b95-263">Angi følgende verdier i **Lokasjonsdirektiver**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="89b95-263">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="89b95-264">Godta standardverdiene for alle de andre feltene.</span><span class="sxs-lookup"><span data-stu-id="89b95-264">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="89b95-265">**Arbeidstype:** _Plukk_</span><span class="sxs-lookup"><span data-stu-id="89b95-265">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="89b95-266">**Område:** _6_</span><span class="sxs-lookup"><span data-stu-id="89b95-266">**Site:** _6_</span></span>
    - <span data-ttu-id="89b95-267">**Lager:** _61_</span><span class="sxs-lookup"><span data-stu-id="89b95-267">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="89b95-268">**Direktivkode:** _Sporing_</span><span class="sxs-lookup"><span data-stu-id="89b95-268">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="89b95-269">Velg **Lagre** for å gjøre **Linjer**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="89b95-269">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="89b95-270">Konfigurere Linjer-hurtigfanen</span><span class="sxs-lookup"><span data-stu-id="89b95-270">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="89b95-271">På hurtigfanen **Linjer** velger du **Ny** for å opprette en linje.</span><span class="sxs-lookup"><span data-stu-id="89b95-271">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="89b95-272">På den nye linjen angir du følgende verdier.</span><span class="sxs-lookup"><span data-stu-id="89b95-272">On the new line, set the following values.</span></span>

    - <span data-ttu-id="89b95-273">**Fra-antall:** _0_</span><span class="sxs-lookup"><span data-stu-id="89b95-273">**From quantity:** _0_</span></span>
    - <span data-ttu-id="89b95-274">**Til antall:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="89b95-274">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="89b95-275">Godta standardverdiene for de resterende feltene.</span><span class="sxs-lookup"><span data-stu-id="89b95-275">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="89b95-276">Velg **Lagre** for å gjøre **Lokasjonsdirektivhandlinger**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="89b95-276">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="89b95-277">Konfigurer Handlinger for lokasjonsdirektiv-hurtigfanen</span><span class="sxs-lookup"><span data-stu-id="89b95-277">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="89b95-278">På hurtigfanen **Handlinger for lokasjonsdirektiv** velger du **Ny** for å opprette en linje.</span><span class="sxs-lookup"><span data-stu-id="89b95-278">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="89b95-279">På den nye linjen angir du følgende verdier.</span><span class="sxs-lookup"><span data-stu-id="89b95-279">On the new line, set the following values.</span></span> <span data-ttu-id="89b95-280">Godta standardverdiene for alle de andre feltene.</span><span class="sxs-lookup"><span data-stu-id="89b95-280">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="89b95-281">**Sekvensnummer:** Godta standardverdien.</span><span class="sxs-lookup"><span data-stu-id="89b95-281">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="89b95-282">**Navn:** _Bulk_</span><span class="sxs-lookup"><span data-stu-id="89b95-282">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="89b95-283">**Strategi:** _Ingen_</span><span class="sxs-lookup"><span data-stu-id="89b95-283">**Strategy:** _None_</span></span>

1. <span data-ttu-id="89b95-284">Godta standardverdiene for de resterende feltene.</span><span class="sxs-lookup"><span data-stu-id="89b95-284">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="89b95-285">Velg **Lagre** for å aktivere **Rediger spørring**-knappen.</span><span class="sxs-lookup"><span data-stu-id="89b95-285">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="89b95-286">Rediger spørringen</span><span class="sxs-lookup"><span data-stu-id="89b95-286">Edit the query</span></span>

1. <span data-ttu-id="89b95-287">I **Handlinger for lokasjonsdirektiv**-hurtigfanen velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="89b95-287">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="89b95-288">På **Område**-fanen velger du **Legg til** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="89b95-288">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="89b95-289">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="89b95-289">On the new line, set the following values:</span></span>

    - <span data-ttu-id="89b95-290">**Tabell:** *Plasseringer*</span><span class="sxs-lookup"><span data-stu-id="89b95-290">**Table:** *Locations*</span></span>
    - <span data-ttu-id="89b95-291">**Avledet tabell:** *Lokasjoner*</span><span class="sxs-lookup"><span data-stu-id="89b95-291">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="89b95-292">**Felt:** *Sone-ID*</span><span class="sxs-lookup"><span data-stu-id="89b95-292">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="89b95-293">**Kriterier:** *Bulk* (Velg dobbelt plusstegn \[**++**\] i feltet for å utvide listen, og velg deretter *Bulk*.)</span><span class="sxs-lookup"><span data-stu-id="89b95-293">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="89b95-294">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="89b95-294">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="89b95-295">Scenario</span><span class="sxs-lookup"><span data-stu-id="89b95-295">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="89b95-296">Definer scenariet</span><span class="sxs-lookup"><span data-stu-id="89b95-296">Set up the scenario</span></span>

<span data-ttu-id="89b95-297">I dette scenariet bruker du de innebygde eksempeldataene, og oppretter postene som er beskrevet i denne delen.</span><span class="sxs-lookup"><span data-stu-id="89b95-297">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="89b95-298">Bruke USMF-eksempeldataene</span><span class="sxs-lookup"><span data-stu-id="89b95-298">Use the USMF sample data</span></span>

<span data-ttu-id="89b95-299">For å arbeide deg gjennom dette scenariet ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert.</span><span class="sxs-lookup"><span data-stu-id="89b95-299">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="89b95-300">Du må også velge den juridiske enheten **USMF** før du begynner.</span><span class="sxs-lookup"><span data-stu-id="89b95-300">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="89b95-301">Opprette behov</span><span class="sxs-lookup"><span data-stu-id="89b95-301">Create demand</span></span>

<span data-ttu-id="89b95-302">Følg denne fremgangsmåten for å opprette behovet du vil bruke sporing på.</span><span class="sxs-lookup"><span data-stu-id="89b95-302">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="89b95-303">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="89b95-303">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="89b95-304">Velg **Ny** for å opprette en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="89b95-304">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="89b95-305">I **Opprett salgsordre**-dialogboksen, i **Kundekonto**-feltet, velger du _US-007_.</span><span class="sxs-lookup"><span data-stu-id="89b95-305">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="89b95-306">I **Lager**-feltet velger du _61_.</span><span class="sxs-lookup"><span data-stu-id="89b95-306">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="89b95-307">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="89b95-307">Select **OK**.</span></span>
1. <span data-ttu-id="89b95-308">Den nye salgsordren åpnes.</span><span class="sxs-lookup"><span data-stu-id="89b95-308">The new sales order is opened.</span></span> <span data-ttu-id="89b95-309">Det inneholder en tom linje på **Salgsordrelinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="89b95-309">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="89b95-310">På denne linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="89b95-310">On this line, set the following values:</span></span>

    - <span data-ttu-id="89b95-311">**Vare:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="89b95-311">**Item:** _L0101_</span></span>
    - <span data-ttu-id="89b95-312">**Antall:** _20_</span><span class="sxs-lookup"><span data-stu-id="89b95-312">**Quantity:** _20_</span></span>

1. <span data-ttu-id="89b95-313">Velg **Legg til linje** for å legge til en ny linje, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="89b95-313">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="89b95-314">**Vare:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="89b95-314">**Item:** _T0100_</span></span>
    - <span data-ttu-id="89b95-315">**Antall:** _8_</span><span class="sxs-lookup"><span data-stu-id="89b95-315">**Quantity:** _8_</span></span>

1. <span data-ttu-id="89b95-316">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="89b95-316">Select **Save**.</span></span>
1. <span data-ttu-id="89b95-317">Velg **Ny** for å opprette en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="89b95-317">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="89b95-318">I **Opprett salgsordre**-dialogboksen, i **Kundekonto**-feltet, velger du _US-008_.</span><span class="sxs-lookup"><span data-stu-id="89b95-318">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="89b95-319">I **Lager**-feltet velger du _61_.</span><span class="sxs-lookup"><span data-stu-id="89b95-319">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="89b95-320">Den nye salgsordren åpnes.</span><span class="sxs-lookup"><span data-stu-id="89b95-320">The new sales order is opened.</span></span> <span data-ttu-id="89b95-321">Det inneholder en tom linje på **Salgsordrelinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="89b95-321">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="89b95-322">På denne linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="89b95-322">On this line, set the following values:</span></span>

    - <span data-ttu-id="89b95-323">**Vare:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="89b95-323">**Item:** _T0100_</span></span>
    - <span data-ttu-id="89b95-324">**Antall:** _1_</span><span class="sxs-lookup"><span data-stu-id="89b95-324">**Quantity:** _1_</span></span>

1. <span data-ttu-id="89b95-325">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="89b95-325">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="89b95-326">Gå gjennom et vanlig sporingsscenario</span><span class="sxs-lookup"><span data-stu-id="89b95-326">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="89b95-327">Når alle forutsetningselementene er på plass, som beskrevet i den forrige delen, er du klar til å prøve ut funksjonen ved å jobbe gjennom hver øvelse i denne delen.</span><span class="sxs-lookup"><span data-stu-id="89b95-327">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="89b95-328">Generer behov</span><span class="sxs-lookup"><span data-stu-id="89b95-328">Generate demand</span></span>

1. <span data-ttu-id="89b95-329">Gå til **Lagerstyring \> Oppsett \> Etterfylling \> Sporingsmaler**, og velg sporingsmalen du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="89b95-329">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="89b95-330">Velg **Generelt behov** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="89b95-330">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="89b95-331">Denne kommandoen evaluerer alle behov som er i systemet, og som samsvarer med sporingsmalspørringen.</span><span class="sxs-lookup"><span data-stu-id="89b95-331">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="89b95-332">Det totale behovet på tvers av alle ordrer konsolideres deretter på én linje per antall/måleenhet.</span><span class="sxs-lookup"><span data-stu-id="89b95-332">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="89b95-333">En informasjonsmelding vises når prosessen er fullført.</span><span class="sxs-lookup"><span data-stu-id="89b95-333">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="89b95-334">Sporingsbehov</span><span class="sxs-lookup"><span data-stu-id="89b95-334">Slotting demand</span></span>

<span data-ttu-id="89b95-335">*Sporingsbehovet* viser resultatene av behovsgenerering, basert på oppsettet til sporingsmalen.</span><span class="sxs-lookup"><span data-stu-id="89b95-335">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="89b95-336">I handlingsruten velger **Sporingsbehov** for å vise resultatene fra **Generelt behov**-kommandoen.</span><span class="sxs-lookup"><span data-stu-id="89b95-336">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="89b95-337">Linjene i sporingsbehov kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="89b95-337">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="89b95-338">Du kan slette en linje, legge til en ny linje eller redigere linjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="89b95-338">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="89b95-339">Du kan redigere behovet manuelt, eller du kan importere den fra et eksternt system ved hjelp av dataadministrasjon.</span><span class="sxs-lookup"><span data-stu-id="89b95-339">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="89b95-340">Det som er oppgitt i sporingsbehov, vil bli brukt i neste trinn, uansett hvor den kom fra.</span><span class="sxs-lookup"><span data-stu-id="89b95-340">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="89b95-341">Finn behov</span><span class="sxs-lookup"><span data-stu-id="89b95-341">Locate demand</span></span>

<span data-ttu-id="89b95-342">Etter at behov er generert, må du bruke **Finn behov**-kommandoen til å generere *sporingsplanen*.</span><span class="sxs-lookup"><span data-stu-id="89b95-342">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="89b95-343">Velg **Finn behov** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="89b95-343">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="89b95-344">Sporingsprosessen kjører.</span><span class="sxs-lookup"><span data-stu-id="89b95-344">The slotting process runs.</span></span> <span data-ttu-id="89b95-345">En informasjonsmelding vises når prosessen er fullført.</span><span class="sxs-lookup"><span data-stu-id="89b95-345">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="89b95-346">Sporingsplan</span><span class="sxs-lookup"><span data-stu-id="89b95-346">Slotting plan</span></span>

<span data-ttu-id="89b95-347">Sporingsplanen viser lokasjonen som hver vare/antall ble tilordnet til, om overflyt ble brukt, om det ble opprettet en arbeidslinje og mallinjen som ble brukt.</span><span class="sxs-lookup"><span data-stu-id="89b95-347">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="89b95-348">*Alle etterspørsler som ikke kunne spores, er uthevet i rødt.*</span><span class="sxs-lookup"><span data-stu-id="89b95-348">*Any demand that could not be slotted is highlighted in red.*</span></span>

- <span data-ttu-id="89b95-349">I handlingsruten velger **Sporingsplan** for å vise resultatene.</span><span class="sxs-lookup"><span data-stu-id="89b95-349">On the Action Pane, select **Slotting plan** to view the results.</span></span>

> [!NOTE]
> - <span data-ttu-id="89b95-350">Prosessene **Generer behov**, **Finn behov** og **Kjør etterfylling** er nå i en sandkasse.</span><span class="sxs-lookup"><span data-stu-id="89b95-350">The **Generate demand**, **Locate demand**, and **Run replenishment** processes are now run in a sandbox.</span></span> <span data-ttu-id="89b95-351">(Disse prosessene er tilgjengelige fra handlingsruten på siden **Sporingsmaler**.)</span><span class="sxs-lookup"><span data-stu-id="89b95-351">(These processes are available from the Action Pane on the **Slotting templates** page.)</span></span>
> - <span data-ttu-id="89b95-352">Prosessene **Generer behov**, **Finn behov** og **Kjør etterfylling** for å sikre at de ikke kan utløses samtidig.</span><span class="sxs-lookup"><span data-stu-id="89b95-352">The **Generate demand**, **Locate demand**, and **Run replenishment** processes have a lock to ensure that they can't be triggered at the same time.</span></span> <span data-ttu-id="89b95-353">Ellers kan dataene som brukes, bli slettes.</span><span class="sxs-lookup"><span data-stu-id="89b95-353">Otherwise, the data that is used could be deleted.</span></span>
> - <span data-ttu-id="89b95-354">Prosessene **Generer behov** og **Finn behov** viser en advarsel hvis kjøringen ikke genererte poster, eller hvis postene mangler informasjon.</span><span class="sxs-lookup"><span data-stu-id="89b95-354">The **Generate demand** and **Locate demand** processes show a warning if the run didn't generate records, or if the records are missing information.</span></span>
> - <span data-ttu-id="89b95-355">Når du velger **Sporingsplan**, har ikke siden knappene **Ny**, **Rediger** eller **Slett** i handlingsruten, fordi datakilden ikke kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="89b95-355">When you select **Slotting plan**, the page doesn't have **New**, **Edit**, or **Delete** buttons on the Action Pane, because the data source can't be edited.</span></span>
> - <span data-ttu-id="89b95-356">Når du velger **Kjør etterfylling**, validerer systemet den valgte spormalen og prosessene.</span><span class="sxs-lookup"><span data-stu-id="89b95-356">When you select **Run replenishment**, the system validates the selected slot template and processes.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="89b95-357">Opprett etterfylling</span><span class="sxs-lookup"><span data-stu-id="89b95-357">Create replenishment</span></span>

<span data-ttu-id="89b95-358">Etter at sporingsplanen er opprettet, må du opprette *Etterfyllingsarbeid*, basert på planen.</span><span class="sxs-lookup"><span data-stu-id="89b95-358">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="89b95-359">Velg **Kjør etterfylling** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="89b95-359">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="89b95-360">En informasjonsmelding vises når prosessen er fullført.</span><span class="sxs-lookup"><span data-stu-id="89b95-360">An informational message appears when the process is completed.</span></span> <span data-ttu-id="89b95-361">Denne meldingen angir antallet hoder som ble opprettet for build-ID-en for arbeid.</span><span class="sxs-lookup"><span data-stu-id="89b95-361">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="89b95-362">Lokasjonsdirektiver som vil bli brukt, identifiseres basert på direktivkoden som er angitt på hver mallinje.</span><span class="sxs-lookup"><span data-stu-id="89b95-362">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="89b95-363">Tips!</span><span class="sxs-lookup"><span data-stu-id="89b95-363">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="89b95-364">Definere automatisk sporing</span><span class="sxs-lookup"><span data-stu-id="89b95-364">Set up automatic slotting</span></span>

<span data-ttu-id="89b95-365">Når alle nødvendige elementer er på plass, kan du konfigurere sporing til å kjøre automatisk ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="89b95-365">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="89b95-366">Gå til **Lagerstyring \> Etterfylling \> Kjør sporing**.</span><span class="sxs-lookup"><span data-stu-id="89b95-366">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="89b95-367">Angi sporingstrinn som skal kjøres.</span><span class="sxs-lookup"><span data-stu-id="89b95-367">Specify the slotting steps to run.</span></span> <span data-ttu-id="89b95-368">Velg ett eller flere av følgende sporingstrinn:</span><span class="sxs-lookup"><span data-stu-id="89b95-368">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="89b95-369">Generer behov</span><span class="sxs-lookup"><span data-stu-id="89b95-369">Generate demand</span></span>
    - <span data-ttu-id="89b95-370">Finn behov</span><span class="sxs-lookup"><span data-stu-id="89b95-370">Locate demand</span></span>
    - <span data-ttu-id="89b95-371">Opprett etterfyllingsarbeid</span><span class="sxs-lookup"><span data-stu-id="89b95-371">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="89b95-372">Sporingstrinnene er progressive.</span><span class="sxs-lookup"><span data-stu-id="89b95-372">The slotting steps are progressive.</span></span> <span data-ttu-id="89b95-373">Hvis du vil velge *Finn behov*, må du først velge *Generer behov*.</span><span class="sxs-lookup"><span data-stu-id="89b95-373">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="89b95-374">Angi hvilken sporingsmal som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="89b95-374">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="89b95-375">Angi at regelmessigheten skal kjøres automatisk hvis du vil.</span><span class="sxs-lookup"><span data-stu-id="89b95-375">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="89b95-376">For øvelsene i scenarioet må du **ikke** sette opp automatisk sporing.</span><span class="sxs-lookup"><span data-stu-id="89b95-376">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]