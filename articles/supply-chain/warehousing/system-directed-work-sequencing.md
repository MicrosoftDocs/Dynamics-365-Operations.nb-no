---
title: Systemstyrt arbeidssekvensiering
description: Dette emnet inneholder informasjon om systemstyrt arbeidssekvensering. Med denne funksjonaliteten kan du sortere og filtrere arbeidsordrene som systemet viser for brukere for kjøring. Det er nyttig i scenarier der det kreves tilleggskriterier for å styre lagerplukkprosessen.
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 86d396b069a354b8fa7e15793372a8293273d238
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434797"
---
# <a name="system-directed-work-sequencing"></a><span data-ttu-id="a13b2-105">Systemstyrt arbeidssekvensiering</span><span class="sxs-lookup"><span data-stu-id="a13b2-105">System-directed work sequencing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a13b2-106">Med systemstyrt arbeidssekvensering kan du sortere og filtrere arbeidsordrene som systemet viser for brukere for kjøring.</span><span class="sxs-lookup"><span data-stu-id="a13b2-106">System-directed work sequencing lets you sort and filter the work orders that the system presents to users for execution.</span></span> <span data-ttu-id="a13b2-107">Det er nyttig i scenarier der tilleggskriterier (for eksempel leveringstiden, plukksonen, lokasjonsprofilen eller en kombinasjon av ulike kriterier) er nødvendig for å drive lagerplukkprosessen.</span><span class="sxs-lookup"><span data-stu-id="a13b2-107">It's helpful in scenarios where additional criteria (such as the time of shipping, the picking zone, the location profile, or a combination of various criteria) are required to drive the warehouse picking process.</span></span>

<span data-ttu-id="a13b2-108">Denne funksjonaliteten utvider den gjeldende systemstyrte plukkfunksjonaliteten ved å legge til en omadressert spørringsrekkefølge, der brukere kan definere en sekvens og én eller flere spørringer som vil evaluere alle arbeidsordrene som opprettes.</span><span class="sxs-lookup"><span data-stu-id="a13b2-108">This functionality extends the current system-directed picking functionality by adding a system-directed query order, where users can set up a sequence and one or more queries that will evaluate all work orders that are created.</span></span> <span data-ttu-id="a13b2-109">Bare arbeidsordrer som oppfyller kriteriene som er angitt i oppsettet til menyelementet for den mobile enhetene, blir tatt opp og presentert.</span><span class="sxs-lookup"><span data-stu-id="a13b2-109">Only work orders that meet the criteria that are specified in the setup of the mobile device menu item will be captured and presented.</span></span>

<span data-ttu-id="a13b2-110">Denne funksjonaliteten gjør derfor at du kan optimalisere lagerplukkprosessene samtidig som den identifiserer arbeidsordrer som samsvarer med de angitte kriteriene, tilordner dem til det riktige menyelementet på den mobile enheten, og presenterer dem deretter til en arbeider, basert på et bestemt kompetansesett, et plukkutstyr eller et annet krav.</span><span class="sxs-lookup"><span data-stu-id="a13b2-110">Therefore, this functionality allows for further optimization of warehouse picking processes as it identifies work orders that match the specified criteria, assigns them to the correct mobile device menu item, and then presents them to a worker, based on a specific skill set, picking equipment, or other requirement.</span></span>

> [!NOTE]
> <span data-ttu-id="a13b2-111">Hvis det er behov for andre kriterier, må du bruke flere menyelementer for mobile enheter.</span><span class="sxs-lookup"><span data-stu-id="a13b2-111">If different criteria are needed, multiple mobile device menu items must be used.</span></span>

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a><span data-ttu-id="a13b2-112">Aktiver Systemstyrt arbeidssekvensering i hele organisasjonen-funksjonen</span><span class="sxs-lookup"><span data-stu-id="a13b2-112">Turn on the Organization-wide system directed work sequencing feature</span></span>

<span data-ttu-id="a13b2-113">Før du kan bruke systemstyrt arbeidssekvensering-funksjonen, må den aktiveres i systemet.</span><span class="sxs-lookup"><span data-stu-id="a13b2-113">Before you can use system-directed work sequencing, the feature must be turned on in your system.</span></span> <span data-ttu-id="a13b2-114">Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="a13b2-114">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="a13b2-115">Funksjonen vises på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="a13b2-115">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a13b2-116">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="a13b2-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a13b2-117">**Funksjonsnavn:** *Systemstyrt arbeidssekvensering i hele organisasjonen*</span><span class="sxs-lookup"><span data-stu-id="a13b2-117">**Feature name:** *Organization-wide system directed work sequencing*</span></span>

## <a name="setup"></a><span data-ttu-id="a13b2-118">Installasjon</span><span class="sxs-lookup"><span data-stu-id="a13b2-118">Setup</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="a13b2-119">Gjøre demodata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="a13b2-119">Make demo data available</span></span>

<span data-ttu-id="a13b2-120">For å arbeide deg gjennom dette scenariet ved å bruke verdiene som presenteres i dette emnet, må du arbeide på et system der standard demodata er installert.</span><span class="sxs-lookup"><span data-stu-id="a13b2-120">To work through the scenario by using the values that are presented in this topic, you must work on a system where the standard demo data is installed.</span></span> <span data-ttu-id="a13b2-121">Du må også velge den juridiske enheten **USMF**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-121">Additionally, you must select the **USMF** legal entity.</span></span> <span data-ttu-id="a13b2-122">Scenariene bruker lager *51* fra demodataene.</span><span class="sxs-lookup"><span data-stu-id="a13b2-122">The scenario uses warehouse *51* from the demo data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a13b2-123">Før du frigir ordrene til lageret, må du kontrollere at plukklokasjonene har nok beholdning for alle varene på ordrene.</span><span class="sxs-lookup"><span data-stu-id="a13b2-123">Before you release the orders to the warehouse, make sure that the pick locations have enough inventory for all the items on the orders.</span></span>
>
> <span data-ttu-id="a13b2-124">Standard USMF-data bør støtte dette scenariet.</span><span class="sxs-lookup"><span data-stu-id="a13b2-124">Default USMF data should support this scenario.</span></span> <span data-ttu-id="a13b2-125">Hvis du ikke bruker demodata, kan du se gjennom **Lokasjonsdirektiv**-innstillingen for å lære hvilke plukklokasjoner som skal brukes for plukking av salgsordre.</span><span class="sxs-lookup"><span data-stu-id="a13b2-125">If you aren't using demo data, review the **Location directive** setting to learn which picking locations are used for sales order picking.</span></span> <span data-ttu-id="a13b2-126">Hvis du må justere beholdninge, kan du opprette manuelle flyttinger, bruke etterfylling eller bruke en annen flyt.</span><span class="sxs-lookup"><span data-stu-id="a13b2-126">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span>

### <a name="set-up-a-mobile-device-menu-item"></a><span data-ttu-id="a13b2-127">Definere en mobilenhetsmenyelement</span><span class="sxs-lookup"><span data-stu-id="a13b2-127">Set up a mobile device menu item</span></span>

1. <span data-ttu-id="a13b2-128">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-128">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="a13b2-129">I listen over mobilenhetsmenyelementer velger du **Salgsplukking – system**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-129">In the list of mobile device menu items, select **Sales Picking – System**.</span></span> <span data-ttu-id="a13b2-130">Det nødvendige menyelementet bør allerede finnes.</span><span class="sxs-lookup"><span data-stu-id="a13b2-130">The required menu item should already exist.</span></span> 
1. <span data-ttu-id="a13b2-131">Bekreft følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="a13b2-131">Confirm the following settings:</span></span>

    - <span data-ttu-id="a13b2-132">På **Generelt**-hurtigfanen skal **Styrt av**-feltet angis til *Systemstyrt*.</span><span class="sxs-lookup"><span data-stu-id="a13b2-132">On the **General** FastTab, the **Directed by** field should be set to *System directed*.</span></span>
    - <span data-ttu-id="a13b2-133">**Arbeidsklasser**-hurtigfanen skal vise følgende innstillinger.</span><span class="sxs-lookup"><span data-stu-id="a13b2-133">The **Work classes** FastTab should show the following settings.</span></span>

        | <span data-ttu-id="a13b2-134">Arbeidsklasse-ID</span><span class="sxs-lookup"><span data-stu-id="a13b2-134">Work class ID</span></span> | <span data-ttu-id="a13b2-135">Arbeidsordretype</span><span class="sxs-lookup"><span data-stu-id="a13b2-135">Work order type</span></span> |
        |---|---|
        | <span data-ttu-id="a13b2-136">Salg</span><span class="sxs-lookup"><span data-stu-id="a13b2-136">Sales</span></span> | <span data-ttu-id="a13b2-137">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="a13b2-137">Sales orders</span></span> |
        | <span data-ttu-id="a13b2-138">Salgsordreplukking</span><span class="sxs-lookup"><span data-stu-id="a13b2-138">SO Pick</span></span> | <span data-ttu-id="a13b2-139">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="a13b2-139">Sales orders</span></span> |

1. <span data-ttu-id="a13b2-140">I handlingsruten velger du **Systemstyrte spørringer om arbeidssekvens**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-140">On the Action Pane, select **System directed work sequence queries**.</span></span>
1. <span data-ttu-id="a13b2-141">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-141">Select **Edit**.</span></span>
1. <span data-ttu-id="a13b2-142">Slett den eksisterende linjen, og bekreft deretter handlingen ved å velge **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-142">Delete the existing line, and then confirm the action by selecting **Yes**.</span></span>
1. <span data-ttu-id="a13b2-143">I handlingsruten velger du **Ny** for å opprette en linje.</span><span class="sxs-lookup"><span data-stu-id="a13b2-143">On the Action Pane, select **New** to create a line.</span></span>
1. <span data-ttu-id="a13b2-144">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a13b2-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a13b2-145">**Sekvensnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="a13b2-145">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="a13b2-146">**Beskrivelsesfelt:** *Arbeidsantall mindre enn 20 og synkende*</span><span class="sxs-lookup"><span data-stu-id="a13b2-146">**Description field:** *Work quantity less than 20 and Descending*</span></span>

1. <span data-ttu-id="a13b2-147">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-147">Select **Save**.</span></span>
1. <span data-ttu-id="a13b2-148">I handlingsruten velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-148">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="a13b2-149">På **Sammenkoblinger**-fanen utvides sammenkoblingshierarkiet for å vise **Arbeidslinjer**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="a13b2-149">On the **Joins** tab, expand the join hierarchy to show the **Work lines** table.</span></span>
1. <span data-ttu-id="a13b2-150">Velg **Arbeidslinjer**-tabellsammenkobling.</span><span class="sxs-lookup"><span data-stu-id="a13b2-150">Select the **Work lines** table join.</span></span>
1. <span data-ttu-id="a13b2-151">Velg **Legg til tabellsammenkobling**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-151">Select **Add table join**.</span></span>
1. <span data-ttu-id="a13b2-152">I listen som vises, finner du og velger raden med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="a13b2-152">In the list that appears, find and select the row that has the following settings:</span></span>

    - <span data-ttu-id="a13b2-153">**Sammenkoblingsmodus:** *n:1*</span><span class="sxs-lookup"><span data-stu-id="a13b2-153">**Join mode:** *n:1*</span></span>
    - <span data-ttu-id="a13b2-154">**Relasjon:** *Lokasjoner (lokasjon)*</span><span class="sxs-lookup"><span data-stu-id="a13b2-154">**Relation:** *Locations (Location)*</span></span>

1. <span data-ttu-id="a13b2-155">Velg **Velg**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-155">Select **Select**.</span></span>

    <span data-ttu-id="a13b2-156">Lokasjoner legges til i tabellsammenkoblingen.</span><span class="sxs-lookup"><span data-stu-id="a13b2-156">Locations are added to the table join.</span></span>

1. <span data-ttu-id="a13b2-157">I **Sortering**-fanen velger du **Legg til** for å legge til en linje.</span><span class="sxs-lookup"><span data-stu-id="a13b2-157">On the **Sorting** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="a13b2-158">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a13b2-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a13b2-159">**Tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="a13b2-159">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="a13b2-160">**Avledet tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="a13b2-160">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="a13b2-161">**Felt:** *Arbeidsantall* (i meldingsboksen som vises, velger du **Ja** for å legge til sortering i dette feltet.)</span><span class="sxs-lookup"><span data-stu-id="a13b2-161">**Field:** *Work quantity* (In the message box that appears, select **Yes** to add sorting to this field.)</span></span>
    - <span data-ttu-id="a13b2-162">**Søkeretning:** *Synkende*</span><span class="sxs-lookup"><span data-stu-id="a13b2-162">**Search direction:** *Descending*</span></span>

1. <span data-ttu-id="a13b2-163">Velg **Område**-fanen.</span><span class="sxs-lookup"><span data-stu-id="a13b2-163">Select the **Range** tab.</span></span>

    <span data-ttu-id="a13b2-164">Hvis bare bestemte arbeidskriterier skal inkluderes i sekvensen, kan du angi dem i **Område**-fanen. I dette eksemplet vil du bare ta med arbeid der antallet er mindre enn 20 ea (den laveste måleenheten).</span><span class="sxs-lookup"><span data-stu-id="a13b2-164">If only specific work criteria should be included in the sequencing, you can specify them on the **Range** tab. In this example, you want to include only work where the quantity is less than 20 ea (the lowest unit of measure).</span></span>

    <span data-ttu-id="a13b2-165">Legg merke til at noen linjer allerede er inkludert.</span><span class="sxs-lookup"><span data-stu-id="a13b2-165">Notice that some lines are already included.</span></span> <span data-ttu-id="a13b2-166">Disse linjene bør ikke fjernes.</span><span class="sxs-lookup"><span data-stu-id="a13b2-166">Those lines should not be removed.</span></span>

1. <span data-ttu-id="a13b2-167">Velg **Legg til** for å legge til en linje.</span><span class="sxs-lookup"><span data-stu-id="a13b2-167">Select **Add** to add a line.</span></span>
1. <span data-ttu-id="a13b2-168">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a13b2-168">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a13b2-169">**Tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="a13b2-169">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="a13b2-170">**Avledet tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="a13b2-170">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="a13b2-171">**Felt:** *Beholdningsarbeidsantall*</span><span class="sxs-lookup"><span data-stu-id="a13b2-171">**Field:** *Inventory work quantity*</span></span>
    - <span data-ttu-id="a13b2-172">**Kriterier:** *\<20* (mindre enn 20)</span><span class="sxs-lookup"><span data-stu-id="a13b2-172">**Criteria:** *\<20* (less than 20)</span></span>

1. <span data-ttu-id="a13b2-173">Velg **Legg til** for å legge til en ny linje.</span><span class="sxs-lookup"><span data-stu-id="a13b2-173">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="a13b2-174">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a13b2-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a13b2-175">**Tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="a13b2-175">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="a13b2-176">**Avledet tabell:** *Arbeidslinjer*</span><span class="sxs-lookup"><span data-stu-id="a13b2-176">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="a13b2-177">**Felt:** *Arbeidstype*</span><span class="sxs-lookup"><span data-stu-id="a13b2-177">**Field:** *Work type*</span></span>
    - <span data-ttu-id="a13b2-178">**Kriterier:** *Plukk*</span><span class="sxs-lookup"><span data-stu-id="a13b2-178">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="a13b2-179">Velg **Legg til** for å legge til en ny linje.</span><span class="sxs-lookup"><span data-stu-id="a13b2-179">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="a13b2-180">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a13b2-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a13b2-181">**Tabell:** *Plasseringer*</span><span class="sxs-lookup"><span data-stu-id="a13b2-181">**Table:** *Locations*</span></span>
    - <span data-ttu-id="a13b2-182">**Avledet tabell:** *Lokasjoner*</span><span class="sxs-lookup"><span data-stu-id="a13b2-182">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="a13b2-183">**Felt:** *ID for lokasjonsprofil*</span><span class="sxs-lookup"><span data-stu-id="a13b2-183">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="a13b2-184">**Kriterier:** *!SCENE*</span><span class="sxs-lookup"><span data-stu-id="a13b2-184">**Criteria:** *!STAGE*</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="a13b2-185">Husk å ta med utropstegnet (*!*) foran *STAGE*.</span><span class="sxs-lookup"><span data-stu-id="a13b2-185">Be sure to include the exclamation point (*!*) in front of *STAGE*.</span></span>

1. <span data-ttu-id="a13b2-186">Velg **OK** for å lagre og lukke spørringen.</span><span class="sxs-lookup"><span data-stu-id="a13b2-186">Select **OK** to save and close the query.</span></span>
1. <span data-ttu-id="a13b2-187">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-187">Select **Save**.</span></span>
1. <span data-ttu-id="a13b2-188">Lukk siden for å gå tilbake til **Menyelementer på mobilenhet**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-188">Close the page to return to the **Mobile device menu items** page.</span></span>

> [!NOTE]
> <span data-ttu-id="a13b2-189">Dette oppsettet definerer kriteriene som vil bli brukt til å mate det berettigede arbeidet til menyelementet på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="a13b2-189">This setup defines the criteria that will be used to feed eligible work to the mobile device menu item.</span></span> <span data-ttu-id="a13b2-190">Hvis du legger til flere kriterielinjer i spørringen, vil systemet bruke spørringslinjen som har laveste sekvensnummer først.</span><span class="sxs-lookup"><span data-stu-id="a13b2-190">If you add more criteria lines to the query, the system will use the query line that has lowest sequence number first.</span></span> <span data-ttu-id="a13b2-191">Med andre ord vil alt kvalifisert arbeid for sekvensnummer 1 bli presentert for brukeren først, og deretter alt arbeid for sekvensnummer 2.</span><span class="sxs-lookup"><span data-stu-id="a13b2-191">In other words, all eligible work for sequence number 1 will be presented to the user first, and then all work for sequence number 2.</span></span> <span data-ttu-id="a13b2-192">Hvis et bestemt område og en sortering må brukes sammen, bør derfor de angis i den samme systemstyrte arbeidssekvensspørringen.</span><span class="sxs-lookup"><span data-stu-id="a13b2-192">Therefore, if a specific range and sorting must be used together, they should be specified in the same system-directed work sequence query.</span></span>
>
> <span data-ttu-id="a13b2-193">Dette oppsettet vil fange opp alt arbeid som har minst én linje der antallet er mindre enn 20 ea.</span><span class="sxs-lookup"><span data-stu-id="a13b2-193">This setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="a13b2-194">Hvis arbeidet har en linje der antallet er nøyaktig 20 eller mer enn 20 ea, vil det derfor være gyldig, forutsatt at det også har minst én linje der antallet er mindre enn 20 ea.</span><span class="sxs-lookup"><span data-stu-id="a13b2-194">Therefore, if the work has a line where the quantity is exactly 20 ea or more than 20 ea, it will be valid, provided that it also has at least one line where the quantity is less than 20 ea.</span></span>

### <a name="location-directives"></a><span data-ttu-id="a13b2-195">Lokasjonsdirektiver</span><span class="sxs-lookup"><span data-stu-id="a13b2-195">Location directives</span></span>

<span data-ttu-id="a13b2-196">Hvis du bruker standard Contoso-data, trenger ikke spørringen for handlingen for lokasjonsdirektiv endringer.</span><span class="sxs-lookup"><span data-stu-id="a13b2-196">If you're using default Contoso data, the query for the location directive action won't require changes.</span></span> <span data-ttu-id="a13b2-197">Hvis du imidlertid vil være sikker på at lokasjonsdirektivene vil hente varene på salgsordrene når du bruker funksjonen i et ikke-Contoso-miljø, oppretter du et nytt lokasjonsdirektiv.</span><span class="sxs-lookup"><span data-stu-id="a13b2-197">However, to make sure that the location directives will capture the items on the sales orders when you apply the feature in a non-Contoso environment, create a new location directive.</span></span> <span data-ttu-id="a13b2-198">Følg denne fremgangsmåten for å kontrollere innstillingene i demomiljøet.</span><span class="sxs-lookup"><span data-stu-id="a13b2-198">To verify the settings in the demo environment, follow these steps.</span></span>

1. <span data-ttu-id="a13b2-199">Gå til **Lagerstyring** \> **Oppsett** \> **Lokasjonsdirektiver**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-199">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
1. <span data-ttu-id="a13b2-200">Velg *Salgsordrer* i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-200">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="a13b2-201">Velg lokasjonsdirektivet som heter *51 Plukk*.</span><span class="sxs-lookup"><span data-stu-id="a13b2-201">Select the location directive that is named *51 Pick*.</span></span>
1. <span data-ttu-id="a13b2-202">På **Handlinger for lokasjonsdirektiv**-hurtigfanen velger du linjen for **Plukk**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="a13b2-202">On the **Location Directive Actions** FastTab, select the line for the **Pick** action.</span></span>
1. <span data-ttu-id="a13b2-203">Velg **Rediger spørring** over rutenettet.</span><span class="sxs-lookup"><span data-stu-id="a13b2-203">Select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="a13b2-204">Gå gjennom **Område**-spørringen.</span><span class="sxs-lookup"><span data-stu-id="a13b2-204">Review the **Range** query.</span></span>

    1. <span data-ttu-id="a13b2-205">Finn linjen der **Felt**-feltet er satt til *Lokasjon*.</span><span class="sxs-lookup"><span data-stu-id="a13b2-205">Find the line where the **Field** field is set to *Location*.</span></span>
    2. <span data-ttu-id="a13b2-206">Kontroller at **Kriterier**-feltet er tomt (det vil si at det ikke er noen begrensninger).</span><span class="sxs-lookup"><span data-stu-id="a13b2-206">Make sure that the **Criteria** field is blank (that is, there are no restrictions).</span></span>

## <a name="scenario"></a><span data-ttu-id="a13b2-207">Scenario</span><span class="sxs-lookup"><span data-stu-id="a13b2-207">Scenario</span></span>

### <a name="create-sales-order-picking-work"></a><span data-ttu-id="a13b2-208">Opprette et plukkarbeid for salgsordre</span><span class="sxs-lookup"><span data-stu-id="a13b2-208">Create sales order picking work</span></span>

<span data-ttu-id="a13b2-209">Før systemstyrt plukking kjøres, bør noe utgående arbeid opprettes.</span><span class="sxs-lookup"><span data-stu-id="a13b2-209">Before system-directed picking is run, some outbound work should be created.</span></span> <span data-ttu-id="a13b2-210">I dette scenariet skal du opprette fire salgsordrer som er basert på den angitte systemstyrte arbeidssekvensspørringer.</span><span class="sxs-lookup"><span data-stu-id="a13b2-210">For this scenario, you will create four sales orders that are based on the specified system-directed work sequence queries.</span></span>

<span data-ttu-id="a13b2-211">Du vil reservere beholdningsantall for hver salgsordre.</span><span class="sxs-lookup"><span data-stu-id="a13b2-211">You will reserve inventory quantities for each sales order.</span></span> <span data-ttu-id="a13b2-212">Derfor kan ikke reservert beholdning trekkes tilbake fra lageret for andre ordrer hvis ikke lagerreserveringen, eller deler av lagerreserveringen, avbrytes.</span><span class="sxs-lookup"><span data-stu-id="a13b2-212">Therefore, reserved inventory can't be withdrawn from the warehouse for other orders unless the inventory reservation, or part of the inventory reservation, is canceled.</span></span>

<span data-ttu-id="a13b2-213">Du vil deretter frigi hver salgsordre til beholdning for å opprette det utgående arbeidet.</span><span class="sxs-lookup"><span data-stu-id="a13b2-213">You will then release each sales order to the warehouse to create the outbound work.</span></span>

#### <a name="sales-order-1"></a><span data-ttu-id="a13b2-214">Salgsordre 1</span><span class="sxs-lookup"><span data-stu-id="a13b2-214">Sales order 1</span></span>

1. <span data-ttu-id="a13b2-215">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-215">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a13b2-216">I handlingsruten velger du **Ny** for å opprette salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="a13b2-216">On the Action Pane, select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="a13b2-217">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a13b2-217">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a13b2-218">I **Kunde**-delen angir du **Kundekonto**-feltet til *US-004*.</span><span class="sxs-lookup"><span data-stu-id="a13b2-218">In the **Customer** section, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="a13b2-219">I **Generelt**-delen angir du **Lager**-feltet til *51*.</span><span class="sxs-lookup"><span data-stu-id="a13b2-219">In the **General** section, set the **Warehouse** field to *51*.</span></span>

1. <span data-ttu-id="a13b2-220">Velg **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a13b2-220">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="a13b2-221">Noter deg salgsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="a13b2-221">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="a13b2-222">Legg til en linje i den nye salgsordren, og angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a13b2-222">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="a13b2-223">**Varenummer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="a13b2-223">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="a13b2-224">**Antall:** *20*</span><span class="sxs-lookup"><span data-stu-id="a13b2-224">**Quantity:** *20*</span></span>

1. <span data-ttu-id="a13b2-225">Velg **Reservasjon** på **Beholdning**-menyen over rutenettet.</span><span class="sxs-lookup"><span data-stu-id="a13b2-225">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="a13b2-226">På **Reservasjon**-siden velger du **Reserver parti** for å reservere beholdningen.</span><span class="sxs-lookup"><span data-stu-id="a13b2-226">On the **Reservation** page, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="a13b2-227">Lukk **Reservasjon**-siden.</span><span class="sxs-lookup"><span data-stu-id="a13b2-227">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="a13b2-228">I handlingsruten på **Lager**-fanen, velger du **Frigi til lager** for å opprette arbeidet for lageret.</span><span class="sxs-lookup"><span data-stu-id="a13b2-228">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse** to create work for the warehouse.</span></span>

    <span data-ttu-id="a13b2-229">Du mottar informasjonsmeldinger som viser bølge-ID og forsendelses-ID-er som er opprettet for salgsordren.</span><span class="sxs-lookup"><span data-stu-id="a13b2-229">You receive informational messages that show the wave ID and shipment IDs that were created for the sales order.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="a13b2-230">Salgsordre 2</span><span class="sxs-lookup"><span data-stu-id="a13b2-230">Sales order 2</span></span>

1. <span data-ttu-id="a13b2-231">I handlingsruten velger du **Ny** for å opprette salgsordre 2.</span><span class="sxs-lookup"><span data-stu-id="a13b2-231">On the Action Pane, select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="a13b2-232">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a13b2-232">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a13b2-233">**Kundekonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="a13b2-233">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="a13b2-234">**Lager:** *51*</span><span class="sxs-lookup"><span data-stu-id="a13b2-234">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="a13b2-235">Velg **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a13b2-235">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="a13b2-236">Noter deg salgsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="a13b2-236">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="a13b2-237">Legg til en linje i den nye salgsordren, og angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a13b2-237">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="a13b2-238">**Varenummer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="a13b2-238">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="a13b2-239">**Antall:** *5*</span><span class="sxs-lookup"><span data-stu-id="a13b2-239">**Quantity:** *5*</span></span>

1. <span data-ttu-id="a13b2-240">Velg **Legg til linje** for å legge til en ny linje, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a13b2-240">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="a13b2-241">**Varenummer:** *M9201*</span><span class="sxs-lookup"><span data-stu-id="a13b2-241">**Item number:** *M9201*</span></span>
    - <span data-ttu-id="a13b2-242">**Antall:** *1*</span><span class="sxs-lookup"><span data-stu-id="a13b2-242">**Quantity:** *1*</span></span>

1. <span data-ttu-id="a13b2-243">Reserver beholdning for begge linjer.</span><span class="sxs-lookup"><span data-stu-id="a13b2-243">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="a13b2-244">Frigi ordren til beholdning.</span><span class="sxs-lookup"><span data-stu-id="a13b2-244">Release the order to the warehouse.</span></span>

#### <a name="sales-order-3"></a><span data-ttu-id="a13b2-245">Salgsordre 3</span><span class="sxs-lookup"><span data-stu-id="a13b2-245">Sales order 3</span></span>

1. <span data-ttu-id="a13b2-246">I handlingsruten velger du **Ny** for å opprette salgsordre 3.</span><span class="sxs-lookup"><span data-stu-id="a13b2-246">On the Action Pane, select **New** to create sales order 3.</span></span>
1. <span data-ttu-id="a13b2-247">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a13b2-247">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a13b2-248">**Kundekonto:** *US-009*</span><span class="sxs-lookup"><span data-stu-id="a13b2-248">**Customer account:** *US-009*</span></span>
    - <span data-ttu-id="a13b2-249">**Lager:** *51*</span><span class="sxs-lookup"><span data-stu-id="a13b2-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="a13b2-250">Velg **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a13b2-250">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="a13b2-251">Noter deg salgsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="a13b2-251">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="a13b2-252">Legg til en linje i den nye salgsordren, og angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a13b2-252">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="a13b2-253">**Varenummer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="a13b2-253">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="a13b2-254">**Antall:** *7*</span><span class="sxs-lookup"><span data-stu-id="a13b2-254">**Quantity:** *7*</span></span>

1. <span data-ttu-id="a13b2-255">Velg **Legg til linje** for å legge til en ny linje, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a13b2-255">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="a13b2-256">**Varenummer:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="a13b2-256">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="a13b2-257">**Antall:** *8*</span><span class="sxs-lookup"><span data-stu-id="a13b2-257">**Quantity:** *8*</span></span>

1. <span data-ttu-id="a13b2-258">Reserver beholdning for begge linjer.</span><span class="sxs-lookup"><span data-stu-id="a13b2-258">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="a13b2-259">Frigi ordren til beholdning.</span><span class="sxs-lookup"><span data-stu-id="a13b2-259">Release the order to the warehouse.</span></span>

#### <a name="sales-order-4"></a><span data-ttu-id="a13b2-260">Salgsordre 4</span><span class="sxs-lookup"><span data-stu-id="a13b2-260">Sales order 4</span></span>

1. <span data-ttu-id="a13b2-261">I handlingsruten velger du **Ny** for å opprette salgsordre 4.</span><span class="sxs-lookup"><span data-stu-id="a13b2-261">On the Action Pane, select **New** to create sales order 4.</span></span>
1. <span data-ttu-id="a13b2-262">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a13b2-262">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a13b2-263">**Kundekonto:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="a13b2-263">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="a13b2-264">**Lager:** *51*</span><span class="sxs-lookup"><span data-stu-id="a13b2-264">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="a13b2-265">Velg **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a13b2-265">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="a13b2-266">Noter deg salgsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="a13b2-266">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="a13b2-267">Legg til en linje i den nye salgsordren, og angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a13b2-267">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="a13b2-268">**Varenummer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="a13b2-268">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="a13b2-269">**Antall:** *25*</span><span class="sxs-lookup"><span data-stu-id="a13b2-269">**Quantity:** *25*</span></span>

1. <span data-ttu-id="a13b2-270">Velg **Legg til linje** for å legge til en ny linje, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a13b2-270">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="a13b2-271">**Varenummer:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="a13b2-271">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="a13b2-272">**Antall:** *10*</span><span class="sxs-lookup"><span data-stu-id="a13b2-272">**Quantity:** *10*</span></span>

1. <span data-ttu-id="a13b2-273">Reserver beholdning for begge linjer.</span><span class="sxs-lookup"><span data-stu-id="a13b2-273">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="a13b2-274">Frigi ordren til beholdning.</span><span class="sxs-lookup"><span data-stu-id="a13b2-274">Release the order to the warehouse.</span></span>

### <a name="get-work-ids-for-the-work-that-was-created"></a><span data-ttu-id="a13b2-275">Hent arbeids-ID-er for arbeidet som ble opprettet</span><span class="sxs-lookup"><span data-stu-id="a13b2-275">Get work IDs for the work that was created</span></span>

1. <span data-ttu-id="a13b2-276">Gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-276">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="a13b2-277">Filtrere på **Lager**-feltet slik at bare arbeid på lager *51* vises.</span><span class="sxs-lookup"><span data-stu-id="a13b2-277">Filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="a13b2-278">Fire arbeids-ID-er skal ha blitt opprettet.</span><span class="sxs-lookup"><span data-stu-id="a13b2-278">Four work IDs should have been created.</span></span> <span data-ttu-id="a13b2-279">Skriv ned arbeids-ID-en for hver salgsordre.</span><span class="sxs-lookup"><span data-stu-id="a13b2-279">Make a note of the work ID for each sales order.</span></span>

    | <span data-ttu-id="a13b2-280">Salgsordre-ID</span><span class="sxs-lookup"><span data-stu-id="a13b2-280">Sales order ID</span></span> | <span data-ttu-id="a13b2-281">Arbeids-ID</span><span class="sxs-lookup"><span data-stu-id="a13b2-281">Work ID</span></span> | <span data-ttu-id="a13b2-282">Arbeidsmengde</span><span class="sxs-lookup"><span data-stu-id="a13b2-282">Work quantity</span></span> |
    |---|---|---|
    | <span data-ttu-id="a13b2-283">Salgsordre 1</span><span class="sxs-lookup"><span data-stu-id="a13b2-283">Sales Order 1</span></span> | <span data-ttu-id="a13b2-284">Arbeids-ID 1</span><span class="sxs-lookup"><span data-stu-id="a13b2-284">Work ID 1</span></span> | <span data-ttu-id="a13b2-285">20 ea</span><span class="sxs-lookup"><span data-stu-id="a13b2-285">20 ea</span></span> |
    | <span data-ttu-id="a13b2-286">Salgsordre 2</span><span class="sxs-lookup"><span data-stu-id="a13b2-286">Sales Order 2</span></span> | <span data-ttu-id="a13b2-287">Arbeids-ID 2</span><span class="sxs-lookup"><span data-stu-id="a13b2-287">Work ID 2</span></span> | <span data-ttu-id="a13b2-288">6 ea (sum av begge linjer)</span><span class="sxs-lookup"><span data-stu-id="a13b2-288">6 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="a13b2-289">Salgsordre 3</span><span class="sxs-lookup"><span data-stu-id="a13b2-289">Sales Order 3</span></span> | <span data-ttu-id="a13b2-290">Arbeids-ID 3</span><span class="sxs-lookup"><span data-stu-id="a13b2-290">Work ID 3</span></span> | <span data-ttu-id="a13b2-291">15 ea (sum av begge linjer)</span><span class="sxs-lookup"><span data-stu-id="a13b2-291">15 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="a13b2-292">Salgsordre 4</span><span class="sxs-lookup"><span data-stu-id="a13b2-292">Sales Order 4</span></span> | <span data-ttu-id="a13b2-293">Arbeids-ID 4</span><span class="sxs-lookup"><span data-stu-id="a13b2-293">Work ID 4</span></span> | <span data-ttu-id="a13b2-294">35 ea (sum av begge linjer)</span><span class="sxs-lookup"><span data-stu-id="a13b2-294">35 ea (sum of both lines)</span></span> |

<span data-ttu-id="a13b2-295">Før du kjører flyten på den mobile enheten, må du kontrollere at bare arbeidet du nettopp opprettet, er i *Åpen*-status for lager *51* og *Salgsordre*-arbeidsordretypen.</span><span class="sxs-lookup"><span data-stu-id="a13b2-295">Before you run the flow on the mobile device, make sure that only the work that you just created is in *Open* status for warehouse *51* and the *Sales order* work order type.</span></span> <span data-ttu-id="a13b2-296">Ellers kan resultatene av testen variere, fordi den systemstyrte plukkingen vil inkludere alt kvalifisert arbeid.</span><span class="sxs-lookup"><span data-stu-id="a13b2-296">Otherwise, the results of the test might vary, because the system-direct picking will include all eligible work.</span></span>

1. <span data-ttu-id="a13b2-297">Gå til **Lagerstyring \> Arbeid \> Utgående \> Åpnet salgsarbeid**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-297">Go to **Warehouse management \> Work \> Outbound \> Open sales work**.</span></span>
1. <span data-ttu-id="a13b2-298">Filtrere på **Lager**-feltet slik at bare arbeid på lager *51* vises i **Åpent salgsarbeid**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-298">In the **Open sales work** grid, filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="a13b2-299">Bekreft at bare de fire arbeids-ID-ene som du opprettet tidligere, vises.</span><span class="sxs-lookup"><span data-stu-id="a13b2-299">Confirm that only the four work IDs that you created earlier are shown.</span></span>
1. <span data-ttu-id="a13b2-300">Lukk **Arbeid**-siden.</span><span class="sxs-lookup"><span data-stu-id="a13b2-300">Close the **Work** page.</span></span>

### <a name="mobile-device-flow-execution"></a><span data-ttu-id="a13b2-301">Kjøring for mobilenhetflyt</span><span class="sxs-lookup"><span data-stu-id="a13b2-301">Mobile device flow execution</span></span>

<span data-ttu-id="a13b2-302">På grunnlag av oppsettet vil systemet mate bruker arbeidet som er sortert etter det høyeste arbeidslinjeantallet, til det laveste.</span><span class="sxs-lookup"><span data-stu-id="a13b2-302">Based on the setup, the system will feed the user work that is sorted from the highest work line quantity to the lowest.</span></span> <span data-ttu-id="a13b2-303">Antall på hver linje vil være mindre enn 20 ea.</span><span class="sxs-lookup"><span data-stu-id="a13b2-303">The quantity on every line will be less than 20 ea.</span></span>

<span data-ttu-id="a13b2-304">Husk at dette oppsettet vil fange opp alt arbeid som har minst én linje der antallet er mindre enn 20 ea.</span><span class="sxs-lookup"><span data-stu-id="a13b2-304">Remember that this setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="a13b2-305">Hvis arbeidet har en annen linje der antallet er nøyaktig 20 ea eller mer enn 20 ea, vil det også være gyldig.</span><span class="sxs-lookup"><span data-stu-id="a13b2-305">Therefore, if the work has another line where the quantity is exactly 20 ea or more than 20 ea, it will also be valid.</span></span>

#### <a name="mobile-app"></a><span data-ttu-id="a13b2-306">Mobilapp</span><span class="sxs-lookup"><span data-stu-id="a13b2-306">Mobile app</span></span>

1. <span data-ttu-id="a13b2-307">Logg på lagerappen som en bruker i lageret *51*.</span><span class="sxs-lookup"><span data-stu-id="a13b2-307">Sign in to the warehousing app as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="a13b2-308">Gå til **Utgående \> Salgsplukking – system**.</span><span class="sxs-lookup"><span data-stu-id="a13b2-308">Go to **Outbound \> Sales Picking - System**.</span></span>

    <span data-ttu-id="a13b2-309">Plukktrinnet for arbeids-ID *4* presenteres.</span><span class="sxs-lookup"><span data-stu-id="a13b2-309">The pick step for work ID *4* is presented.</span></span> <span data-ttu-id="a13b2-310">Denne arbeids-ID-en vises først på grunn av oppsettet til den systemstyrte spørringsrekkefølgen, der du angav at arbeidet skal utføres i rekkefølge basert på synkende arbeidslinjeantall.</span><span class="sxs-lookup"><span data-stu-id="a13b2-310">This work ID is presented first because of the setup of the system-directed query order, where you specified that work should be sequenced based on descending work line quantity.</span></span>

1. <span data-ttu-id="a13b2-311">Fullfør ønsket plukking og plasser for å lukke arbeids-ID-en.</span><span class="sxs-lookup"><span data-stu-id="a13b2-311">Complete the required pick and put to close the work ID.</span></span>

    <span data-ttu-id="a13b2-312">Deretter presenteres arbeids-ID *3*.</span><span class="sxs-lookup"><span data-stu-id="a13b2-312">Next, work ID *3* is presented.</span></span> <span data-ttu-id="a13b2-313">En av arbeidslinjene er neste i sekvensen, basert på arbeidslinjeantallet.</span><span class="sxs-lookup"><span data-stu-id="a13b2-313">One of its work lines is next in the sequence, based on the work line quantity.</span></span>

1. <span data-ttu-id="a13b2-314">Fullfør plukking og plasser for å lukke arbeids-ID-en.</span><span class="sxs-lookup"><span data-stu-id="a13b2-314">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="a13b2-315">Deretter presenteres arbeids-ID *2*.</span><span class="sxs-lookup"><span data-stu-id="a13b2-315">Next, work ID *2* is presented.</span></span> <span data-ttu-id="a13b2-316">Dette arbeidets plukklinje er neste i sekvensen.</span><span class="sxs-lookup"><span data-stu-id="a13b2-316">This work's pick line is next in the sequence.</span></span>

1. <span data-ttu-id="a13b2-317">Fullfør plukking og plasser for å lukke arbeids-ID-en.</span><span class="sxs-lookup"><span data-stu-id="a13b2-317">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="a13b2-318">Det skal ikke presenteres noe mer arbeid for deg.</span><span class="sxs-lookup"><span data-stu-id="a13b2-318">No further work should be presented to you.</span></span> <span data-ttu-id="a13b2-319">Arbeids-ID *1* er ikke kvalifisert for dette menyelementet på mobilenheter, fordi spørringen angir at arbeidshoder bare skal regnes med hvis antallet på arbeidslinjene er mindre enn 20 ea.</span><span class="sxs-lookup"><span data-stu-id="a13b2-319">Work ID *1* isn't eligible for this mobile device menu item, because the query specifies that work headers are considered only if the quantity on the work lines is less than 20 ea.</span></span>

## <a name="tips"></a><span data-ttu-id="a13b2-320">Tips!</span><span class="sxs-lookup"><span data-stu-id="a13b2-320">Tips</span></span>

<span data-ttu-id="a13b2-321">De systemstyrte arbeidssekvensspørringene er *inklusive*.</span><span class="sxs-lookup"><span data-stu-id="a13b2-321">The system-directed work sequence queries are *inclusive*.</span></span> <span data-ttu-id="a13b2-322">Det er viktig at du husker dette faktumet for noen oppsett.</span><span class="sxs-lookup"><span data-stu-id="a13b2-322">It's important that you remember this fact for some setups.</span></span> <span data-ttu-id="a13b2-323">Du vil for eksempel at et bestemt menyelement skal behandle bare arbeid der arbeidsenheten er *ea*, og du angir denne begrensningen i **Område**-fanen i spørringen.</span><span class="sxs-lookup"><span data-stu-id="a13b2-323">For example, you want a specific menu item to process only work where the work unit is *ea*, and you specify that restriction on the **Range** tab of the query.</span></span> <span data-ttu-id="a13b2-324">I dette tilfellet vil alt arbeid der minst én arbeidslinje har arbeidsenheten som angis til *ea*, bli matet til arbeideren.</span><span class="sxs-lookup"><span data-stu-id="a13b2-324">In this case, all work where at least one work line has the work unit set to *ea* will be fed to the worker.</span></span> <span data-ttu-id="a13b2-325">Derfor kan dette arbeidet også omfatte arbeid der arbeidslinjer har en annen arbeidsenhet enn *ea* (for eksempel *boks* eller *pall*).</span><span class="sxs-lookup"><span data-stu-id="a13b2-325">Therefore, this work might also include work where work lines have a work unit other than *ea* (such as *box* or *pallet*).</span></span> <span data-ttu-id="a13b2-326">Spørringen vil bare ekskludere arbeidslinjer der arbeidslinjen er satt til *ea*.</span><span class="sxs-lookup"><span data-stu-id="a13b2-326">The query will exclude only work where no work line has the work unit set to *ea*.</span></span>

<span data-ttu-id="a13b2-327">I eksemplet fra dette scenariet ble derfor arbeids-ID *4* også hentet av spørringen.</span><span class="sxs-lookup"><span data-stu-id="a13b2-327">Therefore, in the example from this scenario, work ID *4* was also captured by the query.</span></span> <span data-ttu-id="a13b2-328">Når den ble opprettet, ble to linjer lagt til: én for 25 ea og en annen for 10 ea.</span><span class="sxs-lookup"><span data-stu-id="a13b2-328">When it was created, two lines were added: one for 25 ea and another for 10 ea.</span></span> <span data-ttu-id="a13b2-329">Arbeidet ble fortsatt presentert for brukeren fordi minst én arbeidslinje har et antall på mindre enn 20 ea.</span><span class="sxs-lookup"><span data-stu-id="a13b2-329">The work was still presented to the user, because at least one work line has a quantity of less than 20 ea.</span></span>

<span data-ttu-id="a13b2-330">Avhengig av scenariet kan du forhindre denne virkemåten ved å bruke arbeidspauser.</span><span class="sxs-lookup"><span data-stu-id="a13b2-330">Depending on the scenario, you can prevent this behavior by using work breaks.</span></span>
