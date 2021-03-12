---
title: Planlagt direkteoverføring
description: Dette emnet beskriver avansert, planlagt direkteoverføring, hvor lagerantallet som kreves for en ordre, blir dirigert rett fra mottak eller oppretting til riktig utleveringsport eller oppstillingsområde. All gjenværende beholdning fra den inngående kilden dirigeres til den riktige lagringslokasjonen via den vanlige plasseringsprosessen.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: fb598b3ac7dd72e8c500f0c2eaf07462009c67f7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970312"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="d1f58-104">Planlagt direkteoverføring</span><span class="sxs-lookup"><span data-stu-id="d1f58-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1f58-105">Dette emnet beskriver avansert, planlagt direkteoverføring.</span><span class="sxs-lookup"><span data-stu-id="d1f58-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="d1f58-106">Planlagt direkteoverføring er en lagerprosess hvor lagerantallet som kreves for en ordre, blir dirigert rett fra mottak eller oppretting til riktig utleveringsport eller oppstillingsområde.</span><span class="sxs-lookup"><span data-stu-id="d1f58-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="d1f58-107">All gjenværende beholdning fra den inngående kilden dirigeres til den riktige lagringslokasjonen via den vanlige plasseringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="d1f58-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="d1f58-108">Direkteoverføring la arbeiderne hoppe over den inngående plasseringen og utgående plukking av lageret som allerede er merket for en utgående ordre.</span><span class="sxs-lookup"><span data-stu-id="d1f58-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="d1f58-109">Derfor reduseres antall ganger beholdningen berøres, der det er mulig.</span><span class="sxs-lookup"><span data-stu-id="d1f58-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="d1f58-110">Fordi det i tillegg er mindre samhandling med systemet, økes tids- og plassbesparelsene på lageret.</span><span class="sxs-lookup"><span data-stu-id="d1f58-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="d1f58-111">Før direkteoverføring kan kjøres, må brukeren konfigurere en ny direkteoverføringsmal der forsyningskilden og andre sett med krav for direkteoverføring er angitt.</span><span class="sxs-lookup"><span data-stu-id="d1f58-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="d1f58-112">Når den utgående ordren opprettes, må linjen merkes mot en inngående ordre som inneholder den samme varen.</span><span class="sxs-lookup"><span data-stu-id="d1f58-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="d1f58-113">På tidspunktet for mottak av inngående ordre, identifiserer direkteoverføringsoppsettet automatisk behovet for direkteoverføring og oppretter bevegelsesarbeidet for det nødvendige antallet, basert på oppsettet til lokasjonsdirektivet.</span><span class="sxs-lookup"><span data-stu-id="d1f58-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="d1f58-114">Lagertransaksjoner avregistreres **ikke** når direkteoverføringsarbeid blir avbrutt, selv om innstillingen for denne funksjonen er aktivert i lagestyringsparametere.</span><span class="sxs-lookup"><span data-stu-id="d1f58-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-feature"></a><span data-ttu-id="d1f58-115">Aktivere funksjonen for planlagt direkteoverføring</span><span class="sxs-lookup"><span data-stu-id="d1f58-115">Turn on the Planned cross docking feature</span></span>

<span data-ttu-id="d1f58-116">Før du kan bruke avansert, planlagt direkteoverføring, må funksjonen aktiveres i systemet.</span><span class="sxs-lookup"><span data-stu-id="d1f58-116">Before you can use advanced planned cross-docking, the feature must be turned on in your system.</span></span> <span data-ttu-id="d1f58-117">Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="d1f58-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d1f58-118">Funksjonen vises på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="d1f58-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d1f58-119">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="d1f58-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d1f58-120">**Funksjonsnavn:** *Planlagt direkteoverføring*</span><span class="sxs-lookup"><span data-stu-id="d1f58-120">**Feature name:** *Planned cross docking*</span></span>

## <a name="setup"></a><span data-ttu-id="d1f58-121">Installasjon</span><span class="sxs-lookup"><span data-stu-id="d1f58-121">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="d1f58-122">Generer lastposteringsmetoder på nytt</span><span class="sxs-lookup"><span data-stu-id="d1f58-122">Regenerate load posting methods</span></span>

<span data-ttu-id="d1f58-123">Planlagt direkteoverføring er implementert som en lastposteringsmetode.</span><span class="sxs-lookup"><span data-stu-id="d1f58-123">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="d1f58-124">Når du har aktivert funksjonen, må du generere metodene på nytt.</span><span class="sxs-lookup"><span data-stu-id="d1f58-124">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="d1f58-125">Gå til **Lagerstyring \> Oppsett \> Lastposteringsmetoder**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-125">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="d1f58-126">Velg **Regenerer metoder** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d1f58-126">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="d1f58-127">Når regenereringen er fullført, skal det vises en metode som har **Metodenavn**-verdien *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="d1f58-127">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="d1f58-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d1f58-128">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="d1f58-129">Opprett en direkteoverføringsmal</span><span class="sxs-lookup"><span data-stu-id="d1f58-129">Create a cross-docking template</span></span>

1. <span data-ttu-id="d1f58-130">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Direkteoverføringsmaler**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-130">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="d1f58-131">I handlingsruten velger du **Ny** for å opprette en mal.</span><span class="sxs-lookup"><span data-stu-id="d1f58-131">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="d1f58-132">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d1f58-132">In the header, set the following values:</span></span>

    - <span data-ttu-id="d1f58-133">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="d1f58-133">**Sequence:** *1*</span></span>

        <span data-ttu-id="d1f58-134">Dette feltet definerer rekkefølgen malene skal evalueres i.</span><span class="sxs-lookup"><span data-stu-id="d1f58-134">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="d1f58-135">**ID for direkteoverføringsmal:** *51*</span><span class="sxs-lookup"><span data-stu-id="d1f58-135">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="d1f58-136">**Beskrivelse:** *Lager 51*</span><span class="sxs-lookup"><span data-stu-id="d1f58-136">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="d1f58-137">**Policy for behovsfrigivelse:** *Før forsyningsmottak*</span><span class="sxs-lookup"><span data-stu-id="d1f58-137">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="d1f58-138">**Lager:** *51*</span><span class="sxs-lookup"><span data-stu-id="d1f58-138">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d1f58-139">Oppsettet på **Planlegging**-hurtigfanen styrer hvordan malen fungerer.</span><span class="sxs-lookup"><span data-stu-id="d1f58-139">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="d1f58-140">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d1f58-140">Set the following values:</span></span>

    - <span data-ttu-id="d1f58-141">**Behovskrav:** *Ingen*</span><span class="sxs-lookup"><span data-stu-id="d1f58-141">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="d1f58-142">Dette feltet definerer kravene til behovslageret.</span><span class="sxs-lookup"><span data-stu-id="d1f58-142">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="d1f58-143">Hvis behovet må kobles til forsyningen før frigivelse, velger du *Merking*.</span><span class="sxs-lookup"><span data-stu-id="d1f58-143">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="d1f58-144">Hvis behovet må være ordrereservert mot forsyningen før frigivelse, velger *Ordrereservering*.</span><span class="sxs-lookup"><span data-stu-id="d1f58-144">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="d1f58-145">**Lokaliseringstype:** *Forsendelseslokasjoner*</span><span class="sxs-lookup"><span data-stu-id="d1f58-145">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="d1f58-146">Dette feltet definerer om direkteoverføringsarbeidet skal bruke oppsamling/lastlokasjoner fra forsendelsen, eller om det skal bruke lokasjonsdirektiver til å finne egne oppsamling/lastlokasjoner.</span><span class="sxs-lookup"><span data-stu-id="d1f58-146">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="d1f58-147">**Arbeidsmal:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="d1f58-147">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="d1f58-148">Dette feltet definerer arbeidsmalen som skal brukes når du oppretter direkteoverføringsarbeid.</span><span class="sxs-lookup"><span data-stu-id="d1f58-148">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="d1f58-149">**Ny validering ved forsyningsmottak:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="d1f58-149">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="d1f58-150">Dette alternativet angir om forsyningen skal valideres på nytt under mottak.</span><span class="sxs-lookup"><span data-stu-id="d1f58-150">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="d1f58-151">Hvis dette alternativet er satt til *Ja*, kontrolleres både vinduet maksimal tid og området for utløpsdager.</span><span class="sxs-lookup"><span data-stu-id="d1f58-151">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="d1f58-152">**Validerer tidsvindu:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="d1f58-152">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="d1f58-153">Dette alternativet angir om maksimalt tidsvindu skal evalueres når en forsyningskilde velges.</span><span class="sxs-lookup"><span data-stu-id="d1f58-153">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="d1f58-154">Hvis dette alternativet er satt til *Ja*, blir feltene som er relatert til maksimale og minimale tidsvinduer, tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="d1f58-154">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="d1f58-155">**Maksimalt tidsvindu:** *5*</span><span class="sxs-lookup"><span data-stu-id="d1f58-155">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="d1f58-156">Dette feltet definerer maksimal periode som er tillatt mellom forsyningsmottak og etterspørselsavreise.</span><span class="sxs-lookup"><span data-stu-id="d1f58-156">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="d1f58-157">**Enhet for maksimalt tidsvindu:** *Dager*</span><span class="sxs-lookup"><span data-stu-id="d1f58-157">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="d1f58-158">**Minimum tidsvindu** *0*</span><span class="sxs-lookup"><span data-stu-id="d1f58-158">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="d1f58-159">Dette feltet definerer minimum periode som er tillatt mellom forsyningsmottak og etterspørselsavreise.</span><span class="sxs-lookup"><span data-stu-id="d1f58-159">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="d1f58-160">**Enhet for minimum tidsvindu:** *Dager*</span><span class="sxs-lookup"><span data-stu-id="d1f58-160">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="d1f58-161">**Utløpsområde (dager):** *0*</span><span class="sxs-lookup"><span data-stu-id="d1f58-161">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="d1f58-162">*FEFO-kriterier:* Dette feltet definerer det maksimale antallet dager mellom utløpsdatoen til det første utløpte partiet som for øyeblikket er i lageret, og partiet som mottas.</span><span class="sxs-lookup"><span data-stu-id="d1f58-162">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="d1f58-163">I **Forsyningskilder**-hurtigfanen angir du hvilke typer forsyning som er gyldige for denne malen.</span><span class="sxs-lookup"><span data-stu-id="d1f58-163">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="d1f58-164">Velg **Ny**, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d1f58-164">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="d1f58-165">**Sekvensnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="d1f58-165">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d1f58-166">**Forsyningskilde:** *Bestilling*</span><span class="sxs-lookup"><span data-stu-id="d1f58-166">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="d1f58-167">Opprette en arbeidsklasse</span><span class="sxs-lookup"><span data-stu-id="d1f58-167">Create a work class</span></span>

1. <span data-ttu-id="d1f58-168">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsklasser**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-168">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="d1f58-169">I handlingsruten velger du **Ny** for å opprette en arbeidsklasse.</span><span class="sxs-lookup"><span data-stu-id="d1f58-169">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="d1f58-170">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d1f58-170">Set the following values:</span></span>

    - <span data-ttu-id="d1f58-171">**Arbeidsklasse-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d1f58-171">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="d1f58-172">**Beskrivelse:** *Direkteoverføring*</span><span class="sxs-lookup"><span data-stu-id="d1f58-172">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="d1f58-173">**Arbeidsordretype:** *Direkteoverføring*</span><span class="sxs-lookup"><span data-stu-id="d1f58-173">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="d1f58-174">Opprette en arbeidsmal</span><span class="sxs-lookup"><span data-stu-id="d1f58-174">Create a work template</span></span>

1. <span data-ttu-id="d1f58-175">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-175">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="d1f58-176">Angi *Direkteoverføring* i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-176">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="d1f58-177">I handlingsruten velger du **Ny** for å legge til en linje i **Oversikt**-fanen.</span><span class="sxs-lookup"><span data-stu-id="d1f58-177">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="d1f58-178">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d1f58-178">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d1f58-179">**Sekvensnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="d1f58-179">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d1f58-180">**Arbeidsmal:** *51 Direkteoverføring*</span><span class="sxs-lookup"><span data-stu-id="d1f58-180">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="d1f58-181">**Arbeidsmalbeskrivelse:** *51 Direkteoverføring*</span><span class="sxs-lookup"><span data-stu-id="d1f58-181">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="d1f58-182">Velg **Lagre** for å gjøre **Arbeidsmaldetaljer**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="d1f58-182">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="d1f58-183">På **Arbeidsmaldetaljer**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="d1f58-183">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d1f58-184">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d1f58-184">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d1f58-185">**Arbeidstype:** *Plukk*</span><span class="sxs-lookup"><span data-stu-id="d1f58-185">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="d1f58-186">**Arbeidsklasse-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d1f58-186">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="d1f58-187">Velg **Ny** for å legge til en ny linje, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d1f58-187">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="d1f58-188">**Arbeidstype:** *Plasser*</span><span class="sxs-lookup"><span data-stu-id="d1f58-188">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d1f58-189">**Arbeidsklasse-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d1f58-189">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="d1f58-190">Velg **Lagre**, og Bekreft at det er merket av for **Gyldig** for *51 Direkteoverføring*-malen.</span><span class="sxs-lookup"><span data-stu-id="d1f58-190">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="d1f58-191">Arbeidsklasse-ID-en for *Plukk*- og *Plasser*-arbeidstypene må være like.</span><span class="sxs-lookup"><span data-stu-id="d1f58-191">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="d1f58-192">Opprette lokasjonsdirektiver</span><span class="sxs-lookup"><span data-stu-id="d1f58-192">Create location directives</span></span>

1. <span data-ttu-id="d1f58-193">Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-193">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d1f58-194">I den venstre ruten setter du **Arbeidsordretype**-feltet til *Direkteoverføring*.</span><span class="sxs-lookup"><span data-stu-id="d1f58-194">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="d1f58-195">Velg **Ny** i handlingsruten, og angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d1f58-195">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="d1f58-196">**Sekvensnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="d1f58-196">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d1f58-197">**Navn:** *51 Direkteoverføringsplass*</span><span class="sxs-lookup"><span data-stu-id="d1f58-197">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="d1f58-198">**Arbeidstype:** *Plasser*</span><span class="sxs-lookup"><span data-stu-id="d1f58-198">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d1f58-199">**Område:** *5*</span><span class="sxs-lookup"><span data-stu-id="d1f58-199">**Site:** *5*</span></span>
    - <span data-ttu-id="d1f58-200">**Lager:** *51*</span><span class="sxs-lookup"><span data-stu-id="d1f58-200">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d1f58-201">Velg **Lagre** for å gjøre **Linjer**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="d1f58-201">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="d1f58-202">På **Linjer**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="d1f58-202">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d1f58-203">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d1f58-203">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d1f58-204">**Fra-antall:** *1*</span><span class="sxs-lookup"><span data-stu-id="d1f58-204">**From quantity:** *1*</span></span>
    - <span data-ttu-id="d1f58-205">**Til-antall:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="d1f58-205">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="d1f58-206">Velg **Lagre** for å gjøre **Lokasjonsdirektivhandlinger**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="d1f58-206">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="d1f58-207">På hurtigfanen **Lokasjonsdirektivhandlinger** velger du **Ny** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="d1f58-207">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d1f58-208">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d1f58-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d1f58-209">**Navn:** *Rampedør*</span><span class="sxs-lookup"><span data-stu-id="d1f58-209">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="d1f58-210">**Bruk av fast lokasjon:** *Faste og ikke-faste lokasjoner*</span><span class="sxs-lookup"><span data-stu-id="d1f58-210">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="d1f58-211">Velg **Lagre** for å gjøre **Rediger spørring**-knappen på **Lokasjonsdirektivhandlinger**-verktøylinjen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="d1f58-211">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="d1f58-212">Velg **Rediger spørring** for å åpne redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="d1f58-212">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="d1f58-213">I **Område**-fanen kontrollerer du at følgende to linjer er konfigurert:</span><span class="sxs-lookup"><span data-stu-id="d1f58-213">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="d1f58-214">Linje 1:</span><span class="sxs-lookup"><span data-stu-id="d1f58-214">Line 1:</span></span>

        - <span data-ttu-id="d1f58-215">**Tabell:** *Plasseringer*</span><span class="sxs-lookup"><span data-stu-id="d1f58-215">**Table:** *Locations*</span></span>
        - <span data-ttu-id="d1f58-216">**Avledet tabell:** *Lokasjoner*</span><span class="sxs-lookup"><span data-stu-id="d1f58-216">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="d1f58-217">**Felt:** *Lager*</span><span class="sxs-lookup"><span data-stu-id="d1f58-217">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="d1f58-218">**Kriterier:** *51*</span><span class="sxs-lookup"><span data-stu-id="d1f58-218">**Criteria:** *51*</span></span>

    - <span data-ttu-id="d1f58-219">Linje 2:</span><span class="sxs-lookup"><span data-stu-id="d1f58-219">Line 2:</span></span>

        - <span data-ttu-id="d1f58-220">**Tabell:** *Plasseringer*</span><span class="sxs-lookup"><span data-stu-id="d1f58-220">**Table:** *Locations*</span></span>
        - <span data-ttu-id="d1f58-221">**Avledet tabell:** *Lokasjoner*</span><span class="sxs-lookup"><span data-stu-id="d1f58-221">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="d1f58-222">**Felt:** *Lokasjon*</span><span class="sxs-lookup"><span data-stu-id="d1f58-222">**Field:** *Location*</span></span>
        - <span data-ttu-id="d1f58-223">**Kriterier:** *Rampedør*</span><span class="sxs-lookup"><span data-stu-id="d1f58-223">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="d1f58-224">Velg **OK** for å lukke redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="d1f58-224">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="d1f58-225">Opprette et menyelement for mobilenhet</span><span class="sxs-lookup"><span data-stu-id="d1f58-225">Create a mobile device menu item</span></span>

1. <span data-ttu-id="d1f58-226">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-226">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="d1f58-227">I listen over menyelementer i venstre rute velger du **Kjøpsplassering**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-227">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="d1f58-228">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-228">Select **Edit**.</span></span>
1. <span data-ttu-id="d1f58-229">På **Arbeidsklasser**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="d1f58-229">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d1f58-230">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d1f58-230">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d1f58-231">**Arbeidsklasse-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d1f58-231">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="d1f58-232">**Arbeidsordretype:** *Direkteoverføring*</span><span class="sxs-lookup"><span data-stu-id="d1f58-232">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="d1f58-233">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-233">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="d1f58-234">Scenario</span><span class="sxs-lookup"><span data-stu-id="d1f58-234">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="d1f58-235">Opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="d1f58-235">Create a purchase order</span></span>

<span data-ttu-id="d1f58-236">Følg disse trinnene for å opprette en bestilling som en forsyningskilde.</span><span class="sxs-lookup"><span data-stu-id="d1f58-236">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="d1f58-237">Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-237">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="d1f58-238">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d1f58-238">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d1f58-239">I **Opprett bestilling**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d1f58-239">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d1f58-240">**Leverandørkonto:** *104*</span><span class="sxs-lookup"><span data-stu-id="d1f58-240">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="d1f58-241">**Lager:** *51*</span><span class="sxs-lookup"><span data-stu-id="d1f58-241">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d1f58-242">Velg **OK** og noter deg ordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="d1f58-242">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="d1f58-243">Det legges til en ny linje i rutenettet på **Bestillingslinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="d1f58-243">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="d1f58-244">På denne linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d1f58-244">On this line, set the following values:</span></span>

    - <span data-ttu-id="d1f58-245">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d1f58-245">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d1f58-246">**Antall:** *5*</span><span class="sxs-lookup"><span data-stu-id="d1f58-246">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="d1f58-247">Opprette en salgsordre</span><span class="sxs-lookup"><span data-stu-id="d1f58-247">Create a sales order</span></span>

<span data-ttu-id="d1f58-248">Følg disse trinnene for å opprette en salgsordre som en behovskilde.</span><span class="sxs-lookup"><span data-stu-id="d1f58-248">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="d1f58-249">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-249">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d1f58-250">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d1f58-250">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d1f58-251">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d1f58-251">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d1f58-252">**Kundekonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="d1f58-252">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="d1f58-253">**Lager:** *51*</span><span class="sxs-lookup"><span data-stu-id="d1f58-253">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d1f58-254">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-254">Select **OK**.</span></span>
1. <span data-ttu-id="d1f58-255">Det legges til en ny linje i rutenettet på **Salgsordrelinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="d1f58-255">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d1f58-256">På denne linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d1f58-256">On this line, set the following values:</span></span>

    - <span data-ttu-id="d1f58-257">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d1f58-257">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d1f58-258">**Antall:** *3*</span><span class="sxs-lookup"><span data-stu-id="d1f58-258">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="d1f58-259">Opprett planlagt direkteoverføring</span><span class="sxs-lookup"><span data-stu-id="d1f58-259">Create planned cross-docking</span></span>

<span data-ttu-id="d1f58-260">Følg disse trinnene for å opprette den planlagte direkteoverføringen fra salgsordren.</span><span class="sxs-lookup"><span data-stu-id="d1f58-260">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="d1f58-261">På **Salgsordredetaljer**-siden for salgsordren du nettopp opprettet, velger du **Frigi til lager** i handlingsruten på **Lager**-fanen i **Handlinger**-gruppen.</span><span class="sxs-lookup"><span data-stu-id="d1f58-261">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="d1f58-262">Frigi til lager-handling oppretter en forsendelse og lastlinje for salgsordrelinjen, og prøver å tildele beholdning.</span><span class="sxs-lookup"><span data-stu-id="d1f58-262">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="d1f58-263">Du får en informasjonsmelding.</span><span class="sxs-lookup"><span data-stu-id="d1f58-263">You receive an informational message.</span></span> <span data-ttu-id="d1f58-264">Du får også følgende advarsel: Ikke no arbeid ble opprettet for bølge XXXX.</span><span class="sxs-lookup"><span data-stu-id="d1f58-264">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="d1f58-265">Se loggen over oppretting av arbeid for detaljer.</span><span class="sxs-lookup"><span data-stu-id="d1f58-265">See the work creation history log for details."</span></span> <span data-ttu-id="d1f58-266">Denne virkemåten forventes fordi det ikke er noe beholdning i lageret.</span><span class="sxs-lookup"><span data-stu-id="d1f58-266">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="d1f58-267">På **Salgsordrelinjer**-fanen, på **Lager**-menyen, velger du **Forsendelsesdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-267">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="d1f58-268">**Forsendelsesdetaljer**-siden vises og viser forsendelsen som ble opprettet for salgsordren.</span><span class="sxs-lookup"><span data-stu-id="d1f58-268">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="d1f58-269">I **Lastlinjer**-hurtigfanen legger du merke til at feltet **Planlagt direkteoverføringsantall** er satt til *3*.</span><span class="sxs-lookup"><span data-stu-id="d1f58-269">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="d1f58-270">Fordi det ikke var noe beholdning tilgjengelig på lageret, men en gyldig forsyningskilde vil bli mottatt i tidsvinduet som er definert i direkteoverføringsmalen, ble direkteoverføringsantallet opprettet.</span><span class="sxs-lookup"><span data-stu-id="d1f58-270">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="d1f58-271">I **Lastlinjer**-hurtigfanen velger du **Planlagt direkteoverføring** for å vise detaljene for direkteoverføringen som ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="d1f58-271">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="d1f58-272">Behandle direkteoverføringen</span><span class="sxs-lookup"><span data-stu-id="d1f58-272">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="d1f58-273">Bestilling mottatt på lagermobilappen</span><span class="sxs-lookup"><span data-stu-id="d1f58-273">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="d1f58-274">Systemet vil motta antallet på 5 fra bestillingen til mottakslokasjonen og opprette to arbeidsdeler.</span><span class="sxs-lookup"><span data-stu-id="d1f58-274">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="d1f58-275">Den første arbeids-ID-en som opprettes, har **Arbeidsordretype**-verdien *Direkteoverføring* og er koblet til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="d1f58-275">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="d1f58-276">Den har et antall på 3 og dirigeres til den endelige forsendelseslokasjonen, slik at den kan sendes umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="d1f58-276">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="d1f58-277">Den andre arbeids-ID-en som opprettes, har **Arbeidsordretype**-verdien *Bestillinger* og er koblet til bestillingen.</span><span class="sxs-lookup"><span data-stu-id="d1f58-277">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="d1f58-278">Den har gjenstående antall på 2 som ikke ble direkteoverført, og som sendes til plassering for lageret.</span><span class="sxs-lookup"><span data-stu-id="d1f58-278">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="d1f58-279">Logg på mobilenheten som en bruker i lageret *51*.</span><span class="sxs-lookup"><span data-stu-id="d1f58-279">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="d1f58-280">Gå til **Inngående \> Kjøpsmottak**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-280">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="d1f58-281">I **PONum**-feltet angir du bestillingsnummeret.</span><span class="sxs-lookup"><span data-stu-id="d1f58-281">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="d1f58-282">I feltet **Antall** angi *5*.</span><span class="sxs-lookup"><span data-stu-id="d1f58-282">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="d1f58-283">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-283">Select **OK**.</span></span>
1. <span data-ttu-id="d1f58-284">På neste side angir du **Vare**-feltet til *A0001*.</span><span class="sxs-lookup"><span data-stu-id="d1f58-284">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="d1f58-285">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-285">Select **OK**.</span></span>
1. <span data-ttu-id="d1f58-286">På neste side kontrollerer du verdiene for **PONum**, **Vare** og **Antall** ved å velge **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-286">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="d1f58-287">Du mottar en Arbeid fullført-melding.</span><span class="sxs-lookup"><span data-stu-id="d1f58-287">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="d1f58-288">Velg **Avbryt** for å avslutte.</span><span class="sxs-lookup"><span data-stu-id="d1f58-288">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="d1f58-289">Plassering til direkteoverføring og bulk</span><span class="sxs-lookup"><span data-stu-id="d1f58-289">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="d1f58-290">For øyeblikket har begge arbeids-ID-ene samme målnummerskilt.</span><span class="sxs-lookup"><span data-stu-id="d1f58-290">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="d1f58-291">Hvis du vil fullføre de neste trinnene, må du hente arbeids-ID-en og målnummerskilt-ID-en.</span><span class="sxs-lookup"><span data-stu-id="d1f58-291">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="d1f58-292">Du kan få denne informasjonen fra arbeidsdetaljene for bestillingslinjen og salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="d1f58-292">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="d1f58-293">Du kan også gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer** og filtrere arbeid der **Lager**-verdien er *51*.</span><span class="sxs-lookup"><span data-stu-id="d1f58-293">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="d1f58-294">Gå til **Inngående \> Kjøpsplassering** på den mobile enheten, og angi målnummerskiltet fra arbeidet.</span><span class="sxs-lookup"><span data-stu-id="d1f58-294">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="d1f58-295">I **ID**-feltet angir du målnummerskilt-ID-en fra arbeidsdetaljene.</span><span class="sxs-lookup"><span data-stu-id="d1f58-295">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="d1f58-296">Direkteoverføringsplukking-siden viser plukklokasjonen (*RECV*), målnummerskiltet (*nummerskilt*), vare (*A0001*) og antall (*3*).</span><span class="sxs-lookup"><span data-stu-id="d1f58-296">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="d1f58-297">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-297">Select **OK**.</span></span>
1. <span data-ttu-id="d1f58-298">I feltet **mål-LP** angir du et målnummerskilt for nummerskilt-ID-en som skal plasseres (direkteoverføres) til forsendelsesstedet.</span><span class="sxs-lookup"><span data-stu-id="d1f58-298">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="d1f58-299">Du kan velge en hvilken som helst nummerskilt-ID.</span><span class="sxs-lookup"><span data-stu-id="d1f58-299">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="d1f58-300">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-300">Select **OK**.</span></span>
1. <span data-ttu-id="d1f58-301">På den neste siden angir du nummerskilt-ID-en i **ID**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d1f58-301">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="d1f58-302">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-302">Select **OK**.</span></span>
1. <span data-ttu-id="d1f58-303">Bekreft arbeidet for plukking av det gjenstående antallet på 2, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-303">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="d1f58-304">På den neste siden velger du **Fullført** for å avslutte plukkprosessen og begynne plasseringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="d1f58-304">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="d1f58-305">Mobilappen presenterer lokasjonen og nummerskiltet som varen skal plasseres i.</span><span class="sxs-lookup"><span data-stu-id="d1f58-305">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="d1f58-306">Bekreft masselagringen **Plasser** ved å velge **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-306">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="d1f58-307">Bekreft direkteoverføringen **Plasser** på neste side ved å velge **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1f58-307">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="d1f58-308">Du mottar en Arbeid fullført-melding.</span><span class="sxs-lookup"><span data-stu-id="d1f58-308">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="d1f58-309">Velg **Avbryt** for å avslutte.</span><span class="sxs-lookup"><span data-stu-id="d1f58-309">Select **Cancel** to exit.</span></span>

<span data-ttu-id="d1f58-310">Illustrasjonen nedenfor viser hvordan det fullførte direkteoverføringsarbeidet kan vises i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d1f58-310">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="d1f58-311">![Direkteoverføringsarbeid fullført](media/PlannedCrossDockingWork.png "Direkteoverføringsarbeid fullført")</span><span class="sxs-lookup"><span data-stu-id="d1f58-311">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>
