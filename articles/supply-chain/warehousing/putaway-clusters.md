---
title: Plasseringsgrupper
description: Plasseringsgrupper tilbyr en måte for å plukke flere nummerskilter samtidig og deretter ta dem med for plassering på forskjellige steder. De kan være veldig nyttige for detaljhandelsfirmaer, der nummerskilter vanligvis ikke er fulle paller med lager.
author: Mirzaab
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: b3a7d1b7109b83b26c8187a7f0d271f1c82f6d63
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840371"
---
# <a name="putaway-clusters"></a><span data-ttu-id="c4ad7-104">Plasseringsgrupper</span><span class="sxs-lookup"><span data-stu-id="c4ad7-104">Putaway clusters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4ad7-105">Plasseringsgrupper tilbyr en måte for å plukke flere nummerskilter samtidig og deretter ta dem med for plassering på forskjellige steder.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-105">Putaway clusters offer a way to pick multiple license plates at the same time and then take them for putaway in different locations.</span></span> <span data-ttu-id="c4ad7-106">Denne prosessen blir ofte referert til som en *melkerute*.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-106">This process is often referred to as a *milk run*.</span></span> <span data-ttu-id="c4ad7-107">Plasseringsgrupper kan være veldig nyttige for detaljhandelsfirmaer, der nummerskilter vanligvis ikke er fulle paller med lager.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-107">Putaway clusters can be very useful for retail businesses, where license plates typically aren't full pallets of inventory.</span></span> 

## <a name="turn-on-the-cluster-putaway-feature"></a><span data-ttu-id="c4ad7-108">Aktiver gruppeplasseringsfunksjonen</span><span class="sxs-lookup"><span data-stu-id="c4ad7-108">Turn on the cluster putaway feature</span></span>

<span data-ttu-id="c4ad7-109">Før du kan bruke denne funksjonen, må den være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="c4ad7-110">Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="c4ad7-111">Funksjonen vises på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c4ad7-112">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c4ad7-113">**Funksjonsnavn:** *Gruppeplasseringsfunksjon*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-113">**Feature name:** *Cluster putaway feature*</span></span>

## <a name="setup-for-the-example-scenario"></a><span data-ttu-id="c4ad7-114">Konfigurer for eksempelscenarioet</span><span class="sxs-lookup"><span data-stu-id="c4ad7-114">Setup for the example scenario</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="c4ad7-115">Gruppeprofiler</span><span class="sxs-lookup"><span data-stu-id="c4ad7-115">Cluster profiles</span></span>

<span data-ttu-id="c4ad7-116">Plasseringsgruppeprofilen avgjør hvor en vare skal plasseres, basert på lokasjonen som er tilordnet varen på mottakstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-116">The putaway cluster profile determines where an item will go, based on the location that is assigned to the item at the time of receipt.</span></span> <span data-ttu-id="c4ad7-117">Hvis det kreves forskjellige grupper, bør det opprettes andre plasseringsgrupper, én for hvert menyelement for mobilenhet.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-117">If different clusters are required, different putaway clusters should be created, one for each mobile device menu item.</span></span>

1. <span data-ttu-id="c4ad7-118">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Gruppeprofiler**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-118">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="c4ad7-119">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-119">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c4ad7-120">I **Hode**-visning angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-120">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="c4ad7-121">**ID for plasseringsgruppeprofil:** *Gruppeplassering*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-121">**Putaway cluster profile ID:** *Cluster putaway*</span></span>
    - <span data-ttu-id="c4ad7-122">**Navn på ID for plasseringsgruppeprofil:** *Gruppeplassering*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-122">**Putaway cluster profile ID Name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="c4ad7-123">**Gruppetype:** *Plassering*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-123">**Cluster type:** *Putaway*</span></span>
    - <span data-ttu-id="c4ad7-124">**Sekvensnummer:** Godta standardverdien.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-124">**Sequence number:** Accept the default value.</span></span>

1. <span data-ttu-id="c4ad7-125">Velg **Lagre** for å gjøre de obligatoriske feltene på **Generelt**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-125">Select **Save** to make the required fields on the **General** FastTab available.</span></span>
1. <span data-ttu-id="c4ad7-126">Angi følgende verdier i **Generelt**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-126">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c4ad7-127">**Tidspunkt for gruppetilordning:** *Ved mottak*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-127">**Cluster assignment timing:** *At receipt*</span></span>

        <span data-ttu-id="c4ad7-128">Dette feltet angir om plasseringsgruppen skal tilordnes umiddelbart når lageret mottas, eller om det skal sorteres senere.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-128">This field defines whether the putaway cluster should be assigned immediately when the inventory is received, or whether it should be sorted later.</span></span>

    - <span data-ttu-id="c4ad7-129">**Regel for gruppetilordning:** *Manuell*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-129">**Cluster assignment rule:** *Manual*</span></span>

        <span data-ttu-id="c4ad7-130">Dette feltet angir om gruppetilordningen skal fastslås automatisk av systemet eller manuelt av brukeren.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-130">This field defines whether the cluster assignment should be determined automatically by the system or manually by the user.</span></span>

    - <span data-ttu-id="c4ad7-131">**Direktivkoden:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-131">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="c4ad7-132">**Lokasjon for plasseringsgruppe:** *Mottak*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-132">**Putaway cluster locate:** *Receipt*</span></span>

        <span data-ttu-id="c4ad7-133">Følgende verdier er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-133">The following values are available:</span></span>

        - <span data-ttu-id="c4ad7-134">**Mottak** – En lokasjon ble funnet umiddelbart under mottak.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-134">**Receipt** – A location is found immediately during receipt.</span></span>
        - <span data-ttu-id="c4ad7-135">**Gruppelukking** – En lokasjon blir funnet når gruppen lukkes.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-135">**Cluster close** – A location is found when the cluster is closed.</span></span>
        - <span data-ttu-id="c4ad7-136">**Brukerrettet** – En lokasjon blir funnet når nummerskiltet plukkes fra gruppen for plassering.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-136">**User directed** – A location is found when the license plate is picked from the cluster for putaway.</span></span> <span data-ttu-id="c4ad7-137">I dette tilfellet blir det ikke angitt noen lokasjon når plasseringsarbeidet opprettes.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-137">In this case, no location is specified when the putaway work is created.</span></span> <span data-ttu-id="c4ad7-138">Under selve plasseringen må brukeren skanne nummerskiltet eller arbeids-ID-en for å starte plasseringstrinnet.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-138">During the putaway itself, the user must scan the license plate or work ID to initiate the put step.</span></span> <span data-ttu-id="c4ad7-139">Systemet finner deretter plasseringslokasjonen på nytt og gir brukeren beskjed om hvor det plukkede antallet skal plasseres.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-139">The system then finds the put location again and tells the user where to put the picked quantity.</span></span>

    - <span data-ttu-id="c4ad7-140">**Plasseringsgruppe per bruker:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-140">**Putaway cluster per user:** *No*</span></span>

        <span data-ttu-id="c4ad7-141">Dette feltet definerer om hver gruppe skal være unik per bruker når grupper tilordnes automatisk.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-141">This field defines whether each cluster should be unique per user when clusters are automatically assigned.</span></span> <span data-ttu-id="c4ad7-142">Det er bare tilgjengelig når **Regel for gruppetilordningsregel** er satt til *Automatisk*.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-142">It's available only when the **Cluster assignment rule** field is set to *Automatic*.</span></span>

    - <span data-ttu-id="c4ad7-143">**Enhetsbegrensning:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-143">**Unit restriction:** Leave this field blank.</span></span>

        <span data-ttu-id="c4ad7-144">Dette feltet definerer enheten som må mottas for at profilen skal være gyldig.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-144">This field defines the unit that must be received for the profile to be valid.</span></span> <span data-ttu-id="c4ad7-145">Hvis det er tomt, er alle enheter gyldige.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-145">If it's left blank, all units are valid.</span></span>

    - <span data-ttu-id="c4ad7-146">**Arbeidsenhetsskift:** *Individuelt*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-146">**Work unit break:** *Individual*</span></span>

        <span data-ttu-id="c4ad7-147">Dette feltet definerer om alle lagerbeholdningene skal konsolideres (ved å bruke gruppe-ID-en og nummerskiltet) på ett nummerskilt når en gruppe er lukket, og om den skal plasseres som et enkelt nummerskilt eller separat på nummerskiltene som ble mottatt.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-147">This field defines whether all inventory should be consolidated (by using the cluster ID and the license plate) onto one license plate when a cluster is closed, and whether it should be put away as a single license plate or separately on the license plates that were received.</span></span> <span data-ttu-id="c4ad7-148">Dette feltet er ikke tilgjengelig når feltet **Plasseringsgruppelokasjon** er satt til *Mottak*.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-148">This field is unavailable when the **Putaway cluster locate** field is set to *Receipt*.</span></span>

    - <span data-ttu-id="c4ad7-149">**Gruppe vedvarer som overordnet nummerskilt:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-149">**Cluster persists as Parent License Plate:** *No*</span></span>

        <span data-ttu-id="c4ad7-150">Hvis dette alternativet er angitt til *Ja*, når plasseringstrinnet er fullført, blir gruppe-ID-en et overordnet nummerskilt, og alle varene på gruppe-ID-en blir koblet til det overordnede nummerskiltet.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-150">If this option is set to *Yes*, when the put step is completed, the cluster ID will become a parent license plate, and all items on the cluster ID will be linked to that parent license plate.</span></span>

1. <span data-ttu-id="c4ad7-151">På hurtigfanen **Gruppesortering** kan du definere kriterier for plasseringssortering.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-151">On the **Cluster sorting** FastTab, you can define putaway sorting criteria.</span></span> <span data-ttu-id="c4ad7-152">Velg **Ny** på verktøylinjen for å legge til en ny linje, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-152">Select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="c4ad7-153">**Sekvensnummer:** Godta standardverdien.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-153">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="c4ad7-154">**Feltnavn:** *WMSLocationId*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-154">**Field name:** *WMSLocationId*</span></span>

        <span data-ttu-id="c4ad7-155">Dette feltet definerer feltet som denne linjen skal bruke som sorteringskriterium på.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-155">This field defines the field that this line should use as a sorting criterion.</span></span>

    - <span data-ttu-id="c4ad7-156">**Sortering:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-156">**Sorting:** *Ascending*</span></span>

        <span data-ttu-id="c4ad7-157">Dette feltet angir om sorteringen skal utføres i stigende eller synkende rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-157">This field defines whether sorting should be done in ascending or descending order.</span></span>

1. <span data-ttu-id="c4ad7-158">På **Gryppearbeidsmal**-hurtigfanen velger du **Ny** på verktøylinjen for å legge til en linje, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-158">On the **Cluster work template** FastTab, select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="c4ad7-159">**Arbeidsordretype:** *Bestillinger*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-159">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="c4ad7-160">**Arbeidsmal:** *61 bestilling direkte*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-160">**Work template:** *61 PO Direct*</span></span>

1. <span data-ttu-id="c4ad7-161">Velg **Lagre** i handlingsruten , og velg deretter **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-161">On the Action Pane, select **Save**, and then select **Edit query**.</span></span>
1. <span data-ttu-id="c4ad7-162">I **Gruppeplassering**-dialogboksen, på **Område**-fanen, velger du **Legg til** for å legge til en ny linje i spørringen.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-162">In the **Cluster putaway** dialog box, on the **Range** tab, select **Add** to add a second line to the query.</span></span> <span data-ttu-id="c4ad7-163">Deretter oppdaterer du spørringslinjene som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-163">Then update the query lines as shown in the following table.</span></span>

    | <span data-ttu-id="c4ad7-164">Tabell</span><span class="sxs-lookup"><span data-stu-id="c4ad7-164">Table</span></span> | <span data-ttu-id="c4ad7-165">Avledet tabell</span><span class="sxs-lookup"><span data-stu-id="c4ad7-165">Derived table</span></span> | <span data-ttu-id="c4ad7-166">Felt</span><span class="sxs-lookup"><span data-stu-id="c4ad7-166">Field</span></span> | <span data-ttu-id="c4ad7-167">Vilkår</span><span class="sxs-lookup"><span data-stu-id="c4ad7-167">Criteria</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="c4ad7-168">Arbeid</span><span class="sxs-lookup"><span data-stu-id="c4ad7-168">Work</span></span> | <span data-ttu-id="c4ad7-169">Arbeid</span><span class="sxs-lookup"><span data-stu-id="c4ad7-169">Work</span></span> | <span data-ttu-id="c4ad7-170">Lager</span><span class="sxs-lookup"><span data-stu-id="c4ad7-170">Warehouse</span></span> | <span data-ttu-id="c4ad7-171">*61*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-171">*61*</span></span> |
    | <span data-ttu-id="c4ad7-172">Arbeid</span><span class="sxs-lookup"><span data-stu-id="c4ad7-172">Work</span></span> | <span data-ttu-id="c4ad7-173">Arbeid</span><span class="sxs-lookup"><span data-stu-id="c4ad7-173">Work</span></span> | <span data-ttu-id="c4ad7-174">Arbeids-ID</span><span class="sxs-lookup"><span data-stu-id="c4ad7-174">Work ID</span></span> | <span data-ttu-id="c4ad7-175">La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-175">Leave this field blank.</span></span> |

1. <span data-ttu-id="c4ad7-176">Velg **OK** for å lagre spørringen og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-176">Select **OK** to save the query and close the dialog box.</span></span>
1. <span data-ttu-id="c4ad7-177">Velg **Lagre** i handlingsruten og lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-177">On the Action Pane, select **Save**, and close the page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c4ad7-178">Felter i gruppeprofilen som vises nedtonet når **Generer gruppe-ID** er satt til *Ja*, er ikke tilgjengelige og vil ikke bli tatt med når denne funksjonen brukes.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-178">Fields in the cluster profile that appear dimmed when **Generate cluster ID** is set to *Yes* are unavailable and won't be considered when this feature is used.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="c4ad7-179">Menyelementer på mobilenheten</span><span class="sxs-lookup"><span data-stu-id="c4ad7-179">Mobile device menu items</span></span>

<span data-ttu-id="c4ad7-180">To nye menyelementer for mobilenheter er tilgjengelige for denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-180">Two new mobile device menu items are available for this feature.</span></span> <span data-ttu-id="c4ad7-181">Menyelementet **Motta og sorter gruppe** brukes til å sortere det mottatte lageret til en plasseringsgruppe ved mottak.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-181">The **Receive and sort cluster** menu item is used to sort the received inventory into a putaway cluster upon receipt.</span></span> <span data-ttu-id="c4ad7-182">Menyelementet **Gruppeplassering** brukes til å plassere gruppen etter at den er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-182">The **Cluster putaway** menu item is used to put the cluster away after it has been assigned.</span></span>

#### <a name="receive-and-sort-cluster"></a><span data-ttu-id="c4ad7-183">Motta og sorter gruppe</span><span class="sxs-lookup"><span data-stu-id="c4ad7-183">Receive and sort cluster</span></span>

<span data-ttu-id="c4ad7-184">Opprett et nytt menyelement for mobilenhet for mottak av lager og sortering i en gruppe.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-184">Create a new mobile device menu item for receiving inventory and sorting into a cluster.</span></span> <span data-ttu-id="c4ad7-185">Dette menyelementet vil opprette innkommende arbeid etter at lager er mottatt, som angir at mottaksmenyelementet vil bli brukt for plasseringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-185">This menu item will create inbound work after inventory is received, which indicates that the receiving menu item will be used for putaway clusters.</span></span>

> [!NOTE]
> <span data-ttu-id="c4ad7-186">Menyelementet **Motta og sorter gruppe** kan brukes med følgende mottaksmenyelementer:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-186">The **Receive and sort cluster** menu item can be used with the following receiving menu items:</span></span>
>
> - <span data-ttu-id="c4ad7-187">Mottak av bestillingslinje</span><span class="sxs-lookup"><span data-stu-id="c4ad7-187">Purchase order line receiving</span></span>
> - <span data-ttu-id="c4ad7-188">Mottak av bestillingsvare</span><span class="sxs-lookup"><span data-stu-id="c4ad7-188">Purchase order item receiving</span></span>
> - <span data-ttu-id="c4ad7-189">Mottak av lastvare</span><span class="sxs-lookup"><span data-stu-id="c4ad7-189">Load item receiving</span></span>

1. <span data-ttu-id="c4ad7-190">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-190">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="c4ad7-191">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-191">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c4ad7-192">I **Hode**-visning angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-192">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="c4ad7-193">**Menyelementnavn:** *Motta og sortere gruppe*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-193">**Menu item name:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="c4ad7-194">**Tittel:** *Motta og sorter gruppe*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-194">**Title:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="c4ad7-195">**Modus:** *Arbeid*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-195">**Mode:** *Work*</span></span>
    - <span data-ttu-id="c4ad7-196">**Bruke eksisterende arbeid:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-196">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="c4ad7-197">Angi følgende verdier i **Generelt**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-197">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c4ad7-198">**Arbeidsopprettingsprosess:** *Mottak av bestillingsvarer*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-198">**Work creation process:** *Purchase order item receiving*</span></span>
    - <span data-ttu-id="c4ad7-199">**Generer nummerskilt:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-199">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="c4ad7-200">**Tilordne plasseringsgruppe:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-200">**Assign putaway cluster:** *Yes*</span></span>

        > [!NOTE]
        > <span data-ttu-id="c4ad7-201">Alternativet **Tilordne plasseringsgruppe** er bare tilgjengelig for ettrinnsaktiviteten *Arbeidsopprettingsprosess* for mottak.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-201">The **Assign putaway cluster** option is available only for the one-step *Work creation process* activity for receiving.</span></span>

    <span data-ttu-id="c4ad7-202">Godta standardverdiene for de resterende feltene.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-202">Accept the default values for the remaining fields.</span></span>

1. <span data-ttu-id="c4ad7-203">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-203">On the Action Pane, select **Save**.</span></span>

#### <a name="cluster-putaway"></a><span data-ttu-id="c4ad7-204">Gruppeplassering</span><span class="sxs-lookup"><span data-stu-id="c4ad7-204">Cluster putaway</span></span>

<span data-ttu-id="c4ad7-205">Opprett et nytt menyelement for mobilenhet for å plassere vekk gruppen etter at den er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-205">Create a new mobile device menu item for putting the cluster away after it has been assigned.</span></span>

1. <span data-ttu-id="c4ad7-206">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="c4ad7-207">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-207">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c4ad7-208">I **Hode**-visning angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-208">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="c4ad7-209">**Menyelementnavn:** *Gruppeplassering*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-209">**Menu item name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="c4ad7-210">**Tittel:** *Gruppeplassering*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-210">**Title:** *Cluster putaway*</span></span>
    - <span data-ttu-id="c4ad7-211">**Modus:** *Arbeid*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-211">**Mode:** *Work*</span></span>
    - <span data-ttu-id="c4ad7-212">**Bruke eksisterende arbeid:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-212">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="c4ad7-213">På **Generelt**-hurtigfanen settes **Styrt av**-feltet til *Gruppeplassering*.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-213">On the **General** FastTab, set the **Directed by** field to *Cluster putaway*.</span></span> <span data-ttu-id="c4ad7-214">Godta standardverdiene for de resterende feltene.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-214">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="c4ad7-215">Definer gyldig arbeidsklasse for menyelementet for denne mobilenheten på hurtigfanen **Arbeidsklasser**:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-215">On the **Work classes** FastTab, set up the valid work class for this mobile device menu item:</span></span>

    - <span data-ttu-id="c4ad7-216">**Arbeidsklasse-ID:** *Kjøp*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-216">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="c4ad7-217">**Arbeidsordretype:** *Bestillinger*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-217">**Work order type:** *Purchase orders*</span></span>

1. <span data-ttu-id="c4ad7-218">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-218">On the Action Pane, select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="c4ad7-219">Meny på mobilenheten</span><span class="sxs-lookup"><span data-stu-id="c4ad7-219">Mobile device menu</span></span>

<span data-ttu-id="c4ad7-220">Legg til menyelementene du nettopp opprettet, på innkommende menyen i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-220">Add the menu items that you just created to the inbound menu of the mobile app.</span></span>

1. <span data-ttu-id="c4ad7-221">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-221">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="c4ad7-222">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-222">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="c4ad7-223">Velg **Inngående** i menylisten.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-223">In the menu list, select **Inbound**.</span></span>
1. <span data-ttu-id="c4ad7-224">I **Tilgjengelige menyer og menyelementer**-listen finner og velger du **Motta og sorter gruppe**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-224">In the **Available menus and menu items** list, find and select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="c4ad7-225">Velg høyre pil for å flytte det valgte menyelementet til **Menystruktur**-listen.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-225">Select the right arrow button to move the selected menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="c4ad7-226">Bruk pil opp eller pil ned hvis du vil flytte menyelementet til ønsket plassering på menyen.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-226">Use the up arrow or down arrow button to move the menu item into the desired position in the menu.</span></span>
1. <span data-ttu-id="c4ad7-227">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-227">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="c4ad7-228">Gjenta trinn 4 til og med 7 for å legge til de gjenværende menyelementene:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-228">Repeat steps 4 through 7 to add the remaining menu items:</span></span>

    - <span data-ttu-id="c4ad7-229">Tilordne gruppe</span><span class="sxs-lookup"><span data-stu-id="c4ad7-229">Assign cluster</span></span>
    - <span data-ttu-id="c4ad7-230">Gruppeplassering</span><span class="sxs-lookup"><span data-stu-id="c4ad7-230">Cluster putaway</span></span>

## <a name="example-scenario"></a><span data-ttu-id="c4ad7-231">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="c4ad7-231">Example scenario</span></span>

<span data-ttu-id="c4ad7-232">Dette scenarioet simulerer behandling av plasseringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-232">This scenario simulates putaway cluster processing.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="c4ad7-233">Opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="c4ad7-233">Create a purchase order</span></span>

1. <span data-ttu-id="c4ad7-234">Gå til **Leverandører \> Bestillinger \> Alle bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-234">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="c4ad7-235">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c4ad7-236">I **Opprett bestilling**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-236">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="c4ad7-237">**Leverandørkonto:** *1001*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-237">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="c4ad7-238">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-238">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="c4ad7-239">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-239">Select **OK**.</span></span>

    <span data-ttu-id="c4ad7-240">Siden **Alle bestillinger** vises.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-240">The **All purchase orders** page appears.</span></span>

1. <span data-ttu-id="c4ad7-241">På **Alle bestillinger**-siden i hurtigfanen **Bestillingslinjer** bruker du **Legg til linje**- knappen til å legge til følgende linjer:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-241">On the **All purchase orders** page, on the **Purchase order lines** FastTab, use the **Add line** button to add the following lines:</span></span>

    - <span data-ttu-id="c4ad7-242">Bestillingslinje 1:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-242">Purchase order line 1:</span></span>

        - <span data-ttu-id="c4ad7-243">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-243">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="c4ad7-244">**Antall:** *10*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-244">**Quantity:** *10*</span></span>

    - <span data-ttu-id="c4ad7-245">Bestillingslinje 2:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-245">Purchase order line 2:</span></span>

        - <span data-ttu-id="c4ad7-246">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-246">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="c4ad7-247">**Antall:** *20*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-247">**Quantity:** *20*</span></span>

    - <span data-ttu-id="c4ad7-248">Bestillingslinje 3:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-248">Purchase order line 3:</span></span>

        - <span data-ttu-id="c4ad7-249">**Varenummer:** *M9215*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-249">**Item number:** *M9215*</span></span>
        - <span data-ttu-id="c4ad7-250">**Antall:** *30*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-250">**Quantity:** *30*</span></span>

1. <span data-ttu-id="c4ad7-251">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-251">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="c4ad7-252">Noter deg bestillingsnummeret.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-252">Make a note of the purchase order number.</span></span>

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a><span data-ttu-id="c4ad7-253">Motta lager og plasser det fra mobilenheten</span><span class="sxs-lookup"><span data-stu-id="c4ad7-253">Receive inventory and put it away from the mobile device</span></span>

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a><span data-ttu-id="c4ad7-254">Motta og sorter lageret i en gruppe</span><span class="sxs-lookup"><span data-stu-id="c4ad7-254">Receive and sort the inventory into a cluster</span></span>

1. <span data-ttu-id="c4ad7-255">Logg på mobilappen Lagerstyring som en bruker som er konfigurert for lager *61*.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-255">Sign in to the Warehouse Management mobile app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="c4ad7-256">I hovedmenyen velger du **Innkommende**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-256">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="c4ad7-257">Velg **Motta og sorter gruppe** på **Innkommende**-menyen.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-257">On the **Inbound** menu, select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="c4ad7-258">I **Ponum**-feltet angir du bestillingsnummeret.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-258">In the **Ponum** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="c4ad7-259">Velg **OK** (hakesymbolknappen).</span><span class="sxs-lookup"><span data-stu-id="c4ad7-259">Select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="c4ad7-260">Velg **Vare**-feltet, angi varenummeret *A0001* og velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-260">Select the **Item** field, enter item number *A0001*, and then select **OK**.</span></span>
1. <span data-ttu-id="c4ad7-261">Velg **Antall**-feltet, angi *10* ved å bruke talltastaturet, og velg deretter hakesymbolknappen.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-261">Select the **Qty** field, enter *10* by using the number pad, and then select the check mark button.</span></span>
1. <span data-ttu-id="c4ad7-262">På oppgavesiden **Antall** velger du **OK** (hakesymbolknappen) for å bekrefte antallet du har angitt.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-262">On the **Qty** task page, select **OK** (the check mark button) to confirm the quantity that you entered.</span></span>
1. <span data-ttu-id="c4ad7-263">Velg **OK** på oppgavesiden **Vare** for å bekrefte at varen *A0001* ble angitt.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-263">On the **Item** task page, select **OK** to confirm that item *A0001* was entered.</span></span>
1. <span data-ttu-id="c4ad7-264">Velg **Gruppe-ID**-feltet, og angi en verdi for å tilordne en ID for gruppen du oppretter.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-264">Select the **Cluster ID** field, and enter a value to assign an ID for the cluster that you're creating.</span></span>

    <span data-ttu-id="c4ad7-265">ID-en du angir her, vil bli brukt når de to gjenværende varene i bestillingen mottas.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-265">The ID that you enter here will be used when the two remaining items on the purchase order are received.</span></span>

1. <span data-ttu-id="c4ad7-266">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-266">Select **OK**.</span></span>

    <span data-ttu-id="c4ad7-267">Oppgavesiden **Ponum** vises og viser meldingen Arbeid fullført.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-267">The **Ponum** task page appears and shows a "Work completed" message.</span></span>

    <span data-ttu-id="c4ad7-268">Vare *A0001* er nå mottatt på *RECV*-lokasjonen og tilordnet gruppe-ID-en du angav i trinn 10.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-268">Item *A0001* has now been received into the *RECV* location and assigned to the cluster ID that you entered in step 10.</span></span>

1. <span data-ttu-id="c4ad7-269">Gjenta trinn 4 til og med 11 for å motta de gjenstående to varene fra bestillingen, og tilordne dem til gruppe-ID-en:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-269">Repeat steps 4 through 11 to receive the remaining two items from the purchase order and assign them to the cluster ID:</span></span>

    - <span data-ttu-id="c4ad7-270">Et antall på *20* for vare *A0002*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-270">A quantity of *20* for item *A0002*</span></span>
    - <span data-ttu-id="c4ad7-271">Et antall på *30* for vare *M9215*</span><span class="sxs-lookup"><span data-stu-id="c4ad7-271">A quantity of *30* for item *M9215*</span></span>

#### <a name="close-the-cluster"></a><span data-ttu-id="c4ad7-272">Lukk gruppen</span><span class="sxs-lookup"><span data-stu-id="c4ad7-272">Close the cluster</span></span>

<span data-ttu-id="c4ad7-273">Før varene i gruppen kan plasseres, må gruppen lukkes.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-273">Before the items in the cluster can be put away, the cluster must be closed.</span></span>

1. <span data-ttu-id="c4ad7-274">I Supply Chain Management går du til **Lagerstyring \> Arbeid \> Utgående \> Arbeidsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-274">In Supply Chain Management, go to **Warehouse management \> Work \> Outbound \> Work clusters**.</span></span>
1. <span data-ttu-id="c4ad7-275">I delen **Arbeidsgruppe** på siden **Arbeidsgrupper** søker du i **Gruppe-ID**-feltet etter gruppe-ID-en du angav tidligere.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-275">On the **Work clusters** page, in the **Work cluster** section, search the **Cluster ID** field for the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="c4ad7-276">Hvis gruppen ikke vises, kan den allerede være lukket.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-276">If the cluster isn't shown, it might already have been closed.</span></span> <span data-ttu-id="c4ad7-277">Hvis du vil finne ut om gruppen ble lukket, merker du av for **Vis lukket arbeid** og søker etter gruppe-ID-en du angav tidligere.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-277">To determine whether the cluster was closed, select the **Show closed work** check box, and search for the cluster ID that you entered earlier.</span></span> <span data-ttu-id="c4ad7-278">Følg deretter ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="c4ad7-278">Then follow one of these steps:</span></span>

    - <span data-ttu-id="c4ad7-279">Hvis gruppen er lukket, hopper du over resten av fremgangsmåten for å gå videre til neste fremgangsmåte, [Plasser gruppen](#put-the-cluster-away).</span><span class="sxs-lookup"><span data-stu-id="c4ad7-279">If the cluster has been closed, skip the remaining steps of this procedure, and move on to the next procedure, [Put the cluster away](#put-the-cluster-away).</span></span>
    - <span data-ttu-id="c4ad7-280">Hvis gruppen ikke er lukket, følger du resten av denne fremgangsmåten for å lukke gruppen manuelt.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-280">If the cluster hasn't been closed, follow the remaining steps of this procedure to manually close the cluster.</span></span> <span data-ttu-id="c4ad7-281">Gå deretter videre til neste fremgangsmåte.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-281">Then move on to the next procedure.</span></span>

1. <span data-ttu-id="c4ad7-282">Velg gruppe-ID-en du angav tidligere, i delen **Arbeidsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-282">In the **Work cluster** section, select the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="c4ad7-283">I handlingsruten velger du **Lukk gruppe**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-283">On the Action Pane, select **Close cluster**.</span></span>

    <span data-ttu-id="c4ad7-284">Når gruppen er lukket, vises den ikke lenger i delen **Arbeidsgruppe** (med mindre det er merket av for **Vis lukket arbeid**).</span><span class="sxs-lookup"><span data-stu-id="c4ad7-284">After the cluster has been closed, it's no longer shown in the **Work cluster** section (unless the **Show closed work** check box is selected).</span></span>

#### <a name="put-the-cluster-away"></a><span data-ttu-id="c4ad7-285">Plasser gruppen</span><span class="sxs-lookup"><span data-stu-id="c4ad7-285">Put the cluster away</span></span>

1. <span data-ttu-id="c4ad7-286">Logg på mobilappen Lagerstyring som en bruker som er konfigurert for lager *61*.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-286">Sign in to the Warehouse Management mobile app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="c4ad7-287">I hovedmenyen velger du **Innkommende**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-287">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="c4ad7-288">I menyen **Innkommende** velger du **Gruppeplassering**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-288">On the **Inbound** menu, select **Cluster putaway**.</span></span>
1. <span data-ttu-id="c4ad7-289">Velg **Gruppe-ID**, og angi gruppe-ID-en du angav tidligere for den lukkede gruppen.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-289">Select **Cluster ID**, and enter the cluster ID that you entered earlier for the closed cluster.</span></span>
1. <span data-ttu-id="c4ad7-290">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-290">Select **OK**.</span></span>

    <span data-ttu-id="c4ad7-291">Siden **Gruppeplassering: plukk** vises.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-291">The **Cluster putaway: Pick** page appears.</span></span> <span data-ttu-id="c4ad7-292">Den viser gruppe-ID-en, plukklokasjonen, varene (verdien *Flere* vises) og det totale antallet i gruppen som må plukkes.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-292">It shows the cluster ID, the picking location, the items (the value *Multiple* will be shown), and the total quantity in the cluster that must be picked.</span></span>

1. <span data-ttu-id="c4ad7-293">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-293">Select **OK**.</span></span>

    <span data-ttu-id="c4ad7-294">Siden **Gruppeplassering: plasser** vises.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-294">The **Cluster putaway: Put** page appears.</span></span> <span data-ttu-id="c4ad7-295">**Plasser**-instruksjonene identifiserer gruppe-ID-en, plasseringslokasjonen, varene, det totale antallet og nummerskilt-ID-ene for varene som er mottatt i gruppen.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-295">The **Put** instructions identify the cluster ID, the put location, the items, the total quantity, and the license plate IDs for the items that have been received on the cluster.</span></span>

    <span data-ttu-id="c4ad7-296">Du har standardalternativer for å overstyre eller overføre dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-296">You have the standard options to override or pass this step.</span></span>

    <span data-ttu-id="c4ad7-297">![Gruppeplassering: plasser-side](media/Cluster_putaway-Put.png "Gruppeplassering: plasser-side")</span><span class="sxs-lookup"><span data-stu-id="c4ad7-297">![Cluster putaway: Put page](media/Cluster_putaway-Put.png "Cluster putaway: Put page")</span></span>

1. <span data-ttu-id="c4ad7-298">Velg **OK** for å bekrefte plasseringen av gruppen.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-298">Select **OK** to confirm the putaway of the cluster.</span></span>

    <span data-ttu-id="c4ad7-299">Meldingen Gruppe fullført vises.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-299">A "Cluster completed" message is shown.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="c4ad7-300">Merknader og tips</span><span class="sxs-lookup"><span data-stu-id="c4ad7-300">Notes and tips</span></span>

<span data-ttu-id="c4ad7-301">For tilfeller der gruppe-ID-en blir det overordnede nummerskiltet for en nestet pall, gis plasseringsposisjonen automatisk når gruppe-ID-en skannes.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-301">For cases where the cluster ID becomes the parent license plate for a nested pallet, the put position is automatically given when the cluster ID is scanned.</span></span> <span data-ttu-id="c4ad7-302">Det må ikke skannes flere nummerskilter, selv om det er angitt manuell generering av nummerskilter.</span><span class="sxs-lookup"><span data-stu-id="c4ad7-302">No further license plate must be scanned, even if license plate generation is set to manual.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]