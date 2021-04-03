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
ms.openlocfilehash: 722b004e607cb2e6b7de292d92b67b18c2024696
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556272"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="b58b6-104">Planlagt direkteoverføring</span><span class="sxs-lookup"><span data-stu-id="b58b6-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b58b6-105">Dette emnet beskriver avansert, planlagt direkteoverføring.</span><span class="sxs-lookup"><span data-stu-id="b58b6-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="b58b6-106">Planlagt direkteoverføring er en lagerprosess hvor lagerantallet som kreves for en ordre, blir dirigert rett fra mottak eller oppretting til riktig utleveringsport eller oppstillingsområde.</span><span class="sxs-lookup"><span data-stu-id="b58b6-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="b58b6-107">All gjenværende beholdning fra den inngående kilden dirigeres til den riktige lagringslokasjonen via den vanlige plasseringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="b58b6-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="b58b6-108">Direkteoverføring la arbeiderne hoppe over den inngående plasseringen og utgående plukking av lageret som allerede er merket for en utgående ordre.</span><span class="sxs-lookup"><span data-stu-id="b58b6-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="b58b6-109">Derfor reduseres antall ganger beholdningen berøres, der det er mulig.</span><span class="sxs-lookup"><span data-stu-id="b58b6-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="b58b6-110">Fordi det i tillegg er mindre samhandling med systemet, økes tids- og plassbesparelsene på lageret.</span><span class="sxs-lookup"><span data-stu-id="b58b6-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="b58b6-111">Før direkteoverføring kan kjøres, må brukeren konfigurere en ny direkteoverføringsmal der forsyningskilden og andre sett med krav for direkteoverføring er angitt.</span><span class="sxs-lookup"><span data-stu-id="b58b6-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="b58b6-112">Når den utgående ordren opprettes, må linjen merkes mot en inngående ordre som inneholder den samme varen.</span><span class="sxs-lookup"><span data-stu-id="b58b6-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="b58b6-113">På tidspunktet for mottak av inngående ordre, identifiserer direkteoverføringsoppsettet automatisk behovet for direkteoverføring og oppretter bevegelsesarbeidet for det nødvendige antallet, basert på oppsettet til lokasjonsdirektivet.</span><span class="sxs-lookup"><span data-stu-id="b58b6-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="b58b6-114">Lagertransaksjoner avregistreres **ikke** når direkteoverføringsarbeid blir avbrutt, selv om innstillingen for denne funksjonen er aktivert i lagestyringsparametere.</span><span class="sxs-lookup"><span data-stu-id="b58b6-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="b58b6-115">Aktivere funksjonene for planlagt direkteoverføring</span><span class="sxs-lookup"><span data-stu-id="b58b6-115">Turn on the planned cross docking features</span></span>

<span data-ttu-id="b58b6-116">Hvis systemet ikke allerede inneholder funksjonene som er beskrevet i dette emnet, kan du gå til [Funksjonsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere følgende funksjoner i følgende rekkefølge:</span><span class="sxs-lookup"><span data-stu-id="b58b6-116">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="b58b6-117">*Planlagt direkteoverføring*</span><span class="sxs-lookup"><span data-stu-id="b58b6-117">*Planned cross docking*</span></span>
2. <span data-ttu-id="b58b6-118">*Kryssoverføringsmaler med lokasjonsdirektiver*</span><span class="sxs-lookup"><span data-stu-id="b58b6-118">*Cross docking templates with location directives*</span></span>

## <a name="setup"></a><span data-ttu-id="b58b6-119">Installasjon</span><span class="sxs-lookup"><span data-stu-id="b58b6-119">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="b58b6-120">Generer lastposteringsmetoder på nytt</span><span class="sxs-lookup"><span data-stu-id="b58b6-120">Regenerate load posting methods</span></span>

<span data-ttu-id="b58b6-121">Planlagt direkteoverføring er implementert som en lastposteringsmetode.</span><span class="sxs-lookup"><span data-stu-id="b58b6-121">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="b58b6-122">Når du har aktivert funksjonen, må du generere metodene på nytt.</span><span class="sxs-lookup"><span data-stu-id="b58b6-122">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="b58b6-123">Gå til **Lagerstyring \> Oppsett \> Lastposteringsmetoder**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-123">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="b58b6-124">Velg **Regenerer metoder** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b58b6-124">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="b58b6-125">Når regenereringen er fullført, skal det vises en metode som har **Metodenavn**-verdien *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="b58b6-125">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="b58b6-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b58b6-126">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="b58b6-127">Opprett en direkteoverføringsmal</span><span class="sxs-lookup"><span data-stu-id="b58b6-127">Create a cross-docking template</span></span>

1. <span data-ttu-id="b58b6-128">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Direkteoverføringsmaler**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-128">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="b58b6-129">I handlingsruten velger du **Ny** for å opprette en mal.</span><span class="sxs-lookup"><span data-stu-id="b58b6-129">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="b58b6-130">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="b58b6-130">In the header, set the following values:</span></span>

    - <span data-ttu-id="b58b6-131">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="b58b6-131">**Sequence:** *1*</span></span>

        <span data-ttu-id="b58b6-132">Dette feltet definerer rekkefølgen malene skal evalueres i.</span><span class="sxs-lookup"><span data-stu-id="b58b6-132">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="b58b6-133">**ID for direkteoverføringsmal:** *51*</span><span class="sxs-lookup"><span data-stu-id="b58b6-133">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="b58b6-134">**Beskrivelse:** *Lager 51*</span><span class="sxs-lookup"><span data-stu-id="b58b6-134">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="b58b6-135">**Policy for behovsfrigivelse:** *Før forsyningsmottak*</span><span class="sxs-lookup"><span data-stu-id="b58b6-135">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="b58b6-136">**Lager:** *51*</span><span class="sxs-lookup"><span data-stu-id="b58b6-136">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b58b6-137">Oppsettet på **Planlegging**-hurtigfanen styrer hvordan malen fungerer.</span><span class="sxs-lookup"><span data-stu-id="b58b6-137">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="b58b6-138">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="b58b6-138">Set the following values:</span></span>

    - <span data-ttu-id="b58b6-139">**Behovskrav:** *Ingen*</span><span class="sxs-lookup"><span data-stu-id="b58b6-139">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="b58b6-140">Dette feltet definerer kravene til behovslageret.</span><span class="sxs-lookup"><span data-stu-id="b58b6-140">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="b58b6-141">Hvis behovet må kobles til forsyningen før frigivelse, velger du *Merking*.</span><span class="sxs-lookup"><span data-stu-id="b58b6-141">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="b58b6-142">Hvis behovet må være ordrereservert mot forsyningen før frigivelse, velger *Ordrereservering*.</span><span class="sxs-lookup"><span data-stu-id="b58b6-142">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="b58b6-143">**Lokaliseringstype:** *Forsendelseslokasjoner*</span><span class="sxs-lookup"><span data-stu-id="b58b6-143">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="b58b6-144">Dette feltet definerer om direkteoverføringsarbeidet skal bruke oppsamling/lastlokasjoner fra forsendelsen, eller om det skal bruke lokasjonsdirektiver til å finne egne oppsamling/lastlokasjoner.</span><span class="sxs-lookup"><span data-stu-id="b58b6-144">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="b58b6-145">**Arbeidsmal:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="b58b6-145">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="b58b6-146">Dette feltet definerer arbeidsmalen som skal brukes når du oppretter direkteoverføringsarbeid.</span><span class="sxs-lookup"><span data-stu-id="b58b6-146">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="b58b6-147">**Ny validering ved forsyningsmottak:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="b58b6-147">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="b58b6-148">Dette alternativet angir om forsyningen skal valideres på nytt under mottak.</span><span class="sxs-lookup"><span data-stu-id="b58b6-148">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="b58b6-149">Hvis dette alternativet er satt til *Ja*, kontrolleres både vinduet maksimal tid og området for utløpsdager.</span><span class="sxs-lookup"><span data-stu-id="b58b6-149">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="b58b6-150">**Direktivkode** La dette feltet stå tomt</span><span class="sxs-lookup"><span data-stu-id="b58b6-150">**Directive code** Leave this field blank</span></span>

        <span data-ttu-id="b58b6-151">Ved hjelp av dette alternativet kan systemet bruke lokasjonsdirektiver til å bidra til å finne den beste lokasjonen å flytte lageret for direkteoverføring til.</span><span class="sxs-lookup"><span data-stu-id="b58b6-151">This option enables the system to use location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="b58b6-152">Du kan definere alternativet ved å tilordne en direktivkode til hver relevante direkteoverføringsmal.</span><span class="sxs-lookup"><span data-stu-id="b58b6-152">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="b58b6-153">Hver direktivkode identifiserer et unikt lokasjonsdirektiv.</span><span class="sxs-lookup"><span data-stu-id="b58b6-153">Each directive code identifies a unique location directive.</span></span>

    - <span data-ttu-id="b58b6-154">**Validerer tidsvindu:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="b58b6-154">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="b58b6-155">Dette alternativet angir om maksimalt tidsvindu skal evalueres når en forsyningskilde velges.</span><span class="sxs-lookup"><span data-stu-id="b58b6-155">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="b58b6-156">Hvis dette alternativet er satt til *Ja*, blir feltene som er relatert til maksimale og minimale tidsvinduer, tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="b58b6-156">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="b58b6-157">**Maksimalt tidsvindu:** *5*</span><span class="sxs-lookup"><span data-stu-id="b58b6-157">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="b58b6-158">Dette feltet definerer maksimal periode som er tillatt mellom forsyningsmottak og etterspørselsavreise.</span><span class="sxs-lookup"><span data-stu-id="b58b6-158">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="b58b6-159">**Enhet for maksimalt tidsvindu:** *Dager*</span><span class="sxs-lookup"><span data-stu-id="b58b6-159">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="b58b6-160">**Minimum tidsvindu** *0*</span><span class="sxs-lookup"><span data-stu-id="b58b6-160">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="b58b6-161">Dette feltet definerer minimum periode som er tillatt mellom forsyningsmottak og etterspørselsavreise.</span><span class="sxs-lookup"><span data-stu-id="b58b6-161">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="b58b6-162">**Enhet for minimum tidsvindu:** *Dager*</span><span class="sxs-lookup"><span data-stu-id="b58b6-162">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="b58b6-163">**Utløpsområde (dager):** *0*</span><span class="sxs-lookup"><span data-stu-id="b58b6-163">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="b58b6-164">*FEFO-kriterier:* Dette feltet definerer det maksimale antallet dager mellom utløpsdatoen til det første utløpte partiet som for øyeblikket er i lageret, og partiet som mottas.</span><span class="sxs-lookup"><span data-stu-id="b58b6-164">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="b58b6-165">I **Forsyningskilder**-hurtigfanen angir du hvilke typer forsyning som er gyldige for denne malen.</span><span class="sxs-lookup"><span data-stu-id="b58b6-165">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="b58b6-166">Velg **Ny**, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="b58b6-166">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="b58b6-167">**Sekvensnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="b58b6-167">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="b58b6-168">**Forsyningskilde:** *Bestilling*</span><span class="sxs-lookup"><span data-stu-id="b58b6-168">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="b58b6-169">Opprette en arbeidsklasse</span><span class="sxs-lookup"><span data-stu-id="b58b6-169">Create a work class</span></span>

1. <span data-ttu-id="b58b6-170">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsklasser**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-170">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="b58b6-171">I handlingsruten velger du **Ny** for å opprette en arbeidsklasse.</span><span class="sxs-lookup"><span data-stu-id="b58b6-171">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="b58b6-172">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="b58b6-172">Set the following values:</span></span>

    - <span data-ttu-id="b58b6-173">**Arbeidsklasse-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b58b6-173">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="b58b6-174">**Beskrivelse:** *Direkteoverføring*</span><span class="sxs-lookup"><span data-stu-id="b58b6-174">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="b58b6-175">**Arbeidsordretype:** *Direkteoverføring*</span><span class="sxs-lookup"><span data-stu-id="b58b6-175">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="b58b6-176">Opprette en arbeidsmal</span><span class="sxs-lookup"><span data-stu-id="b58b6-176">Create a work template</span></span>

1. <span data-ttu-id="b58b6-177">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-177">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="b58b6-178">Angi *Direkteoverføring* i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-178">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="b58b6-179">I handlingsruten velger du **Ny** for å legge til en linje i **Oversikt**-fanen.</span><span class="sxs-lookup"><span data-stu-id="b58b6-179">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="b58b6-180">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="b58b6-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b58b6-181">**Sekvensnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="b58b6-181">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="b58b6-182">**Arbeidsmal:** *51 Direkteoverføring*</span><span class="sxs-lookup"><span data-stu-id="b58b6-182">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="b58b6-183">**Arbeidsmalbeskrivelse:** *51 Direkteoverføring*</span><span class="sxs-lookup"><span data-stu-id="b58b6-183">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="b58b6-184">Velg **Lagre** for å gjøre **Arbeidsmaldetaljer**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="b58b6-184">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="b58b6-185">På **Arbeidsmaldetaljer**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="b58b6-185">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b58b6-186">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="b58b6-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b58b6-187">**Arbeidstype:** *Plukk*</span><span class="sxs-lookup"><span data-stu-id="b58b6-187">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="b58b6-188">**Arbeidsklasse-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b58b6-188">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="b58b6-189">Velg **Ny** for å legge til en ny linje, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="b58b6-189">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="b58b6-190">**Arbeidstype:** *Plasser*</span><span class="sxs-lookup"><span data-stu-id="b58b6-190">**Work type:** *Put*</span></span>
    - <span data-ttu-id="b58b6-191">**Arbeidsklasse-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b58b6-191">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="b58b6-192">Velg **Lagre**, og Bekreft at det er merket av for **Gyldig** for *51 Direkteoverføring*-malen.</span><span class="sxs-lookup"><span data-stu-id="b58b6-192">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="b58b6-193">Arbeidsklasse-ID-en for *Plukk*- og *Plasser*-arbeidstypene må være like.</span><span class="sxs-lookup"><span data-stu-id="b58b6-193">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="b58b6-194">Opprette lokasjonsdirektiver</span><span class="sxs-lookup"><span data-stu-id="b58b6-194">Create location directives</span></span>

1. <span data-ttu-id="b58b6-195">Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-195">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b58b6-196">I den venstre ruten setter du **Arbeidsordretype**-feltet til *Direkteoverføring*.</span><span class="sxs-lookup"><span data-stu-id="b58b6-196">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="b58b6-197">Velg **Ny** i handlingsruten, og angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="b58b6-197">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="b58b6-198">**Sekvensnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="b58b6-198">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="b58b6-199">**Navn:** *51 Direkteoverføringsplass*</span><span class="sxs-lookup"><span data-stu-id="b58b6-199">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="b58b6-200">**Arbeidstype:** *Plasser*</span><span class="sxs-lookup"><span data-stu-id="b58b6-200">**Work type:** *Put*</span></span>
    - <span data-ttu-id="b58b6-201">**Område:** *5*</span><span class="sxs-lookup"><span data-stu-id="b58b6-201">**Site:** *5*</span></span>
    - <span data-ttu-id="b58b6-202">**Lager:** *51*</span><span class="sxs-lookup"><span data-stu-id="b58b6-202">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b58b6-203">Velg **Lagre** for å gjøre **Linjer**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="b58b6-203">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="b58b6-204">På **Linjer**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="b58b6-204">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b58b6-205">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="b58b6-205">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b58b6-206">**Fra-antall:** *1*</span><span class="sxs-lookup"><span data-stu-id="b58b6-206">**From quantity:** *1*</span></span>
    - <span data-ttu-id="b58b6-207">**Til-antall:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="b58b6-207">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="b58b6-208">Velg **Lagre** for å gjøre **Lokasjonsdirektivhandlinger**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="b58b6-208">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="b58b6-209">På hurtigfanen **Lokasjonsdirektivhandlinger** velger du **Ny** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="b58b6-209">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b58b6-210">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="b58b6-210">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b58b6-211">**Navn:** *Rampedør*</span><span class="sxs-lookup"><span data-stu-id="b58b6-211">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="b58b6-212">**Bruk av fast lokasjon:** *Faste og ikke-faste lokasjoner*</span><span class="sxs-lookup"><span data-stu-id="b58b6-212">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="b58b6-213">Velg **Lagre** for å gjøre **Rediger spørring**-knappen på **Lokasjonsdirektivhandlinger**-verktøylinjen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="b58b6-213">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="b58b6-214">Velg **Rediger spørring** for å åpne redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="b58b6-214">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="b58b6-215">I **Område**-fanen kontrollerer du at følgende to linjer er konfigurert:</span><span class="sxs-lookup"><span data-stu-id="b58b6-215">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="b58b6-216">Linje 1:</span><span class="sxs-lookup"><span data-stu-id="b58b6-216">Line 1:</span></span>

        - <span data-ttu-id="b58b6-217">**Tabell:** *Plasseringer*</span><span class="sxs-lookup"><span data-stu-id="b58b6-217">**Table:** *Locations*</span></span>
        - <span data-ttu-id="b58b6-218">**Avledet tabell:** *Lokasjoner*</span><span class="sxs-lookup"><span data-stu-id="b58b6-218">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="b58b6-219">**Felt:** *Lager*</span><span class="sxs-lookup"><span data-stu-id="b58b6-219">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="b58b6-220">**Kriterier:** *51*</span><span class="sxs-lookup"><span data-stu-id="b58b6-220">**Criteria:** *51*</span></span>

    - <span data-ttu-id="b58b6-221">Linje 2:</span><span class="sxs-lookup"><span data-stu-id="b58b6-221">Line 2:</span></span>

        - <span data-ttu-id="b58b6-222">**Tabell:** *Plasseringer*</span><span class="sxs-lookup"><span data-stu-id="b58b6-222">**Table:** *Locations*</span></span>
        - <span data-ttu-id="b58b6-223">**Avledet tabell:** *Lokasjoner*</span><span class="sxs-lookup"><span data-stu-id="b58b6-223">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="b58b6-224">**Felt:** *Lokasjon*</span><span class="sxs-lookup"><span data-stu-id="b58b6-224">**Field:** *Location*</span></span>
        - <span data-ttu-id="b58b6-225">**Kriterier:** *Rampedør*</span><span class="sxs-lookup"><span data-stu-id="b58b6-225">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="b58b6-226">Velg **OK** for å lukke redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="b58b6-226">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="b58b6-227">Opprette et menyelement for mobilenhet</span><span class="sxs-lookup"><span data-stu-id="b58b6-227">Create a mobile device menu item</span></span>

1. <span data-ttu-id="b58b6-228">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-228">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="b58b6-229">I listen over menyelementer i venstre rute velger du **Kjøpsplassering**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-229">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="b58b6-230">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-230">Select **Edit**.</span></span>
1. <span data-ttu-id="b58b6-231">På **Arbeidsklasser**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="b58b6-231">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b58b6-232">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="b58b6-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b58b6-233">**Arbeidsklasse-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b58b6-233">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="b58b6-234">**Arbeidsordretype:** *Direkteoverføring*</span><span class="sxs-lookup"><span data-stu-id="b58b6-234">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="b58b6-235">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-235">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="b58b6-236">Scenario</span><span class="sxs-lookup"><span data-stu-id="b58b6-236">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="b58b6-237">Opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="b58b6-237">Create a purchase order</span></span>

<span data-ttu-id="b58b6-238">Følg disse trinnene for å opprette en bestilling som en forsyningskilde.</span><span class="sxs-lookup"><span data-stu-id="b58b6-238">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="b58b6-239">Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-239">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="b58b6-240">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b58b6-240">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b58b6-241">I **Opprett bestilling**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="b58b6-241">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b58b6-242">**Leverandørkonto:** *104*</span><span class="sxs-lookup"><span data-stu-id="b58b6-242">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="b58b6-243">**Lager:** *51*</span><span class="sxs-lookup"><span data-stu-id="b58b6-243">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b58b6-244">Velg **OK** og noter deg ordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="b58b6-244">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="b58b6-245">Det legges til en ny linje i rutenettet på **Bestillingslinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="b58b6-245">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="b58b6-246">På denne linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="b58b6-246">On this line, set the following values:</span></span>

    - <span data-ttu-id="b58b6-247">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b58b6-247">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="b58b6-248">**Antall:** *5*</span><span class="sxs-lookup"><span data-stu-id="b58b6-248">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="b58b6-249">Opprette en salgsordre</span><span class="sxs-lookup"><span data-stu-id="b58b6-249">Create a sales order</span></span>

<span data-ttu-id="b58b6-250">Følg disse trinnene for å opprette en salgsordre som en behovskilde.</span><span class="sxs-lookup"><span data-stu-id="b58b6-250">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="b58b6-251">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-251">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b58b6-252">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b58b6-252">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b58b6-253">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="b58b6-253">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b58b6-254">**Kundekonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="b58b6-254">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="b58b6-255">**Lager:** *51*</span><span class="sxs-lookup"><span data-stu-id="b58b6-255">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b58b6-256">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-256">Select **OK**.</span></span>
1. <span data-ttu-id="b58b6-257">Det legges til en ny linje i rutenettet på **Salgsordrelinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="b58b6-257">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b58b6-258">På denne linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="b58b6-258">On this line, set the following values:</span></span>

    - <span data-ttu-id="b58b6-259">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b58b6-259">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="b58b6-260">**Antall:** *3*</span><span class="sxs-lookup"><span data-stu-id="b58b6-260">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="b58b6-261">Opprett planlagt direkteoverføring</span><span class="sxs-lookup"><span data-stu-id="b58b6-261">Create planned cross-docking</span></span>

<span data-ttu-id="b58b6-262">Følg disse trinnene for å opprette den planlagte direkteoverføringen fra salgsordren.</span><span class="sxs-lookup"><span data-stu-id="b58b6-262">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="b58b6-263">På **Salgsordredetaljer**-siden for salgsordren du nettopp opprettet, velger du **Frigi til lager** i handlingsruten på **Lager**-fanen i **Handlinger**-gruppen.</span><span class="sxs-lookup"><span data-stu-id="b58b6-263">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="b58b6-264">Frigi til lager-handling oppretter en forsendelse og lastlinje for salgsordrelinjen, og prøver å tildele beholdning.</span><span class="sxs-lookup"><span data-stu-id="b58b6-264">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="b58b6-265">Du får en informasjonsmelding.</span><span class="sxs-lookup"><span data-stu-id="b58b6-265">You receive an informational message.</span></span> <span data-ttu-id="b58b6-266">Du får også følgende advarsel: Ikke no arbeid ble opprettet for bølge XXXX.</span><span class="sxs-lookup"><span data-stu-id="b58b6-266">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="b58b6-267">Se loggen over oppretting av arbeid for detaljer.</span><span class="sxs-lookup"><span data-stu-id="b58b6-267">See the work creation history log for details."</span></span> <span data-ttu-id="b58b6-268">Denne virkemåten forventes fordi det ikke er noe beholdning i lageret.</span><span class="sxs-lookup"><span data-stu-id="b58b6-268">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="b58b6-269">På **Salgsordrelinjer**-fanen, på **Lager**-menyen, velger du **Forsendelsesdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-269">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="b58b6-270">**Forsendelsesdetaljer**-siden vises og viser forsendelsen som ble opprettet for salgsordren.</span><span class="sxs-lookup"><span data-stu-id="b58b6-270">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="b58b6-271">I **Lastlinjer**-hurtigfanen legger du merke til at feltet **Planlagt direkteoverføringsantall** er satt til *3*.</span><span class="sxs-lookup"><span data-stu-id="b58b6-271">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="b58b6-272">Fordi det ikke var noe beholdning tilgjengelig på lageret, men en gyldig forsyningskilde vil bli mottatt i tidsvinduet som er definert i direkteoverføringsmalen, ble direkteoverføringsantallet opprettet.</span><span class="sxs-lookup"><span data-stu-id="b58b6-272">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="b58b6-273">I **Lastlinjer**-hurtigfanen velger du **Planlagt direkteoverføring** for å vise detaljene for direkteoverføringen som ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="b58b6-273">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="b58b6-274">Behandle direkteoverføringen</span><span class="sxs-lookup"><span data-stu-id="b58b6-274">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="b58b6-275">Bestilling mottatt på lagermobilappen</span><span class="sxs-lookup"><span data-stu-id="b58b6-275">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="b58b6-276">Systemet vil motta antallet på 5 fra bestillingen til mottakslokasjonen og opprette to arbeidsdeler.</span><span class="sxs-lookup"><span data-stu-id="b58b6-276">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="b58b6-277">Den første arbeids-ID-en som opprettes, har **Arbeidsordretype**-verdien *Direkteoverføring* og er koblet til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="b58b6-277">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="b58b6-278">Den har et antall på 3 og dirigeres til den endelige forsendelseslokasjonen, slik at den kan sendes umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="b58b6-278">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="b58b6-279">Den andre arbeids-ID-en som opprettes, har **Arbeidsordretype**-verdien *Bestillinger* og er koblet til bestillingen.</span><span class="sxs-lookup"><span data-stu-id="b58b6-279">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="b58b6-280">Den har gjenstående antall på 2 som ikke ble direkteoverført, og som sendes til plassering for lageret.</span><span class="sxs-lookup"><span data-stu-id="b58b6-280">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="b58b6-281">Logg på mobilenheten som en bruker i lageret *51*.</span><span class="sxs-lookup"><span data-stu-id="b58b6-281">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="b58b6-282">Gå til **Inngående \> Kjøpsmottak**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-282">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="b58b6-283">I **PONum**-feltet angir du bestillingsnummeret.</span><span class="sxs-lookup"><span data-stu-id="b58b6-283">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="b58b6-284">I feltet **Antall** angi *5*.</span><span class="sxs-lookup"><span data-stu-id="b58b6-284">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="b58b6-285">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-285">Select **OK**.</span></span>
1. <span data-ttu-id="b58b6-286">På neste side angir du **Vare**-feltet til *A0001*.</span><span class="sxs-lookup"><span data-stu-id="b58b6-286">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="b58b6-287">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-287">Select **OK**.</span></span>
1. <span data-ttu-id="b58b6-288">På neste side kontrollerer du verdiene for **PONum**, **Vare** og **Antall** ved å velge **OK**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-288">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="b58b6-289">Du mottar en Arbeid fullført-melding.</span><span class="sxs-lookup"><span data-stu-id="b58b6-289">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="b58b6-290">Velg **Avbryt** for å avslutte.</span><span class="sxs-lookup"><span data-stu-id="b58b6-290">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="b58b6-291">Plassering til direkteoverføring og bulk</span><span class="sxs-lookup"><span data-stu-id="b58b6-291">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="b58b6-292">For øyeblikket har begge arbeids-ID-ene samme målnummerskilt.</span><span class="sxs-lookup"><span data-stu-id="b58b6-292">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="b58b6-293">Hvis du vil fullføre de neste trinnene, må du hente arbeids-ID-en og målnummerskilt-ID-en.</span><span class="sxs-lookup"><span data-stu-id="b58b6-293">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="b58b6-294">Du kan få denne informasjonen fra arbeidsdetaljene for bestillingslinjen og salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="b58b6-294">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="b58b6-295">Du kan også gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer** og filtrere arbeid der **Lager**-verdien er *51*.</span><span class="sxs-lookup"><span data-stu-id="b58b6-295">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="b58b6-296">Gå til **Inngående \> Kjøpsplassering** på den mobile enheten, og angi målnummerskiltet fra arbeidet.</span><span class="sxs-lookup"><span data-stu-id="b58b6-296">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="b58b6-297">I **ID**-feltet angir du målnummerskilt-ID-en fra arbeidsdetaljene.</span><span class="sxs-lookup"><span data-stu-id="b58b6-297">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="b58b6-298">Direkteoverføringsplukking-siden viser plukklokasjonen (*RECV*), målnummerskiltet (*nummerskilt*), vare (*A0001*) og antall (*3*).</span><span class="sxs-lookup"><span data-stu-id="b58b6-298">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="b58b6-299">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-299">Select **OK**.</span></span>
1. <span data-ttu-id="b58b6-300">I feltet **mål-LP** angir du et målnummerskilt for nummerskilt-ID-en som skal plasseres (direkteoverføres) til forsendelsesstedet.</span><span class="sxs-lookup"><span data-stu-id="b58b6-300">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="b58b6-301">Du kan velge en hvilken som helst nummerskilt-ID.</span><span class="sxs-lookup"><span data-stu-id="b58b6-301">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="b58b6-302">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-302">Select **OK**.</span></span>
1. <span data-ttu-id="b58b6-303">På den neste siden angir du nummerskilt-ID-en i **ID**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b58b6-303">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="b58b6-304">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-304">Select **OK**.</span></span>
1. <span data-ttu-id="b58b6-305">Bekreft arbeidet for plukking av det gjenstående antallet på 2, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-305">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="b58b6-306">På den neste siden velger du **Fullført** for å avslutte plukkprosessen og begynne plasseringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="b58b6-306">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="b58b6-307">Mobilappen presenterer lokasjonen og nummerskiltet som varen skal plasseres i.</span><span class="sxs-lookup"><span data-stu-id="b58b6-307">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="b58b6-308">Bekreft masselagringen **Plasser** ved å velge **OK**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-308">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="b58b6-309">Bekreft direkteoverføringen **Plasser** på neste side ved å velge **OK**.</span><span class="sxs-lookup"><span data-stu-id="b58b6-309">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="b58b6-310">Du mottar en Arbeid fullført-melding.</span><span class="sxs-lookup"><span data-stu-id="b58b6-310">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="b58b6-311">Velg **Avbryt** for å avslutte.</span><span class="sxs-lookup"><span data-stu-id="b58b6-311">Select **Cancel** to exit.</span></span>

<span data-ttu-id="b58b6-312">Illustrasjonen nedenfor viser hvordan det fullførte direkteoverføringsarbeidet kan vises i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b58b6-312">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="b58b6-313">![Direkteoverføringsarbeid fullført](media/PlannedCrossDockingWork.png "Direkteoverføringsarbeid fullført")</span><span class="sxs-lookup"><span data-stu-id="b58b6-313">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]