---
title: Planlagt direkteoverføring
description: Dette emnet beskriver avansert, planlagt direkteoverføring, hvor lagerantallet som kreves for en ordre, blir dirigert rett fra mottak eller oppretting til riktig utleveringsport eller oppstillingsområde. All gjenværende beholdning fra den inngående kilden dirigeres til den riktige lagringslokasjonen via den vanlige plasseringsprosessen.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 11e044e04e05c68af676bf97e6085e9975da5c1d
ms.sourcegitcommit: bef7bd2aac00d7eb837fd275d383b7a5c3f1c1ee
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/19/2021
ms.locfileid: "5911254"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="97559-104">Planlagt direkteoverføring</span><span class="sxs-lookup"><span data-stu-id="97559-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97559-105">Dette emnet beskriver avansert, planlagt direkteoverføring.</span><span class="sxs-lookup"><span data-stu-id="97559-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="97559-106">Planlagt direkteoverføring er en lagerprosess hvor lagerantallet som kreves for en ordre, blir dirigert rett fra mottak eller oppretting til riktig utleveringsport eller oppstillingsområde.</span><span class="sxs-lookup"><span data-stu-id="97559-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="97559-107">All gjenværende beholdning fra den inngående kilden dirigeres til den riktige lagringslokasjonen via den vanlige plasseringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="97559-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="97559-108">Direkteoverføring la arbeiderne hoppe over den inngående plasseringen og utgående plukking av lageret som allerede er merket for en utgående ordre.</span><span class="sxs-lookup"><span data-stu-id="97559-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="97559-109">Derfor reduseres antall ganger beholdningen berøres, der det er mulig.</span><span class="sxs-lookup"><span data-stu-id="97559-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="97559-110">Fordi det i tillegg er mindre samhandling med systemet, økes tids- og plassbesparelsene på lageret.</span><span class="sxs-lookup"><span data-stu-id="97559-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="97559-111">Før du kan kjøre direkteoverføring, må du konfigurere en ny direkteoverføringsmal der forsyningskilden og andre sett med krav for direkteoverføring er angitt.</span><span class="sxs-lookup"><span data-stu-id="97559-111">Before you can run cross-docking, you must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="97559-112">Når den utgående ordren opprettes, må linjen merkes mot en inngående ordre som inneholder den samme varen.</span><span class="sxs-lookup"><span data-stu-id="97559-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span> <span data-ttu-id="97559-113">Du kan velge direktivkodefeltet i malen for direkteoverføring, på samme måte som du oppretter etterfylling og bestillinger.</span><span class="sxs-lookup"><span data-stu-id="97559-113">You can select the directive code field on the cross-docking template, similar to the way you set up replenishment and purchase orders.</span></span>

<span data-ttu-id="97559-114">På tidspunktet for mottak av inngående ordre, identifiserer direkteoverføringsoppsettet automatisk behovet for direkteoverføring og oppretter bevegelsesarbeidet for det nødvendige antallet, basert på oppsettet til lokasjonsdirektivet.</span><span class="sxs-lookup"><span data-stu-id="97559-114">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="97559-115">Lagertransaksjoner avregistreres *ikke* når direkteoverføringsarbeid blir avbrutt, selv om innstillingen for denne funksjonen er aktivert i lagestyringsparametere.</span><span class="sxs-lookup"><span data-stu-id="97559-115">Inventory transactions are *not* unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="97559-116">Aktivere funksjonene for planlagt direkteoverføring</span><span class="sxs-lookup"><span data-stu-id="97559-116">Turn on the planned cross docking features</span></span>

<span data-ttu-id="97559-117">Hvis systemet ikke allerede inneholder funksjonene som er beskrevet i dette emnet, kan du gå til [Funksjonsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere følgende funksjoner i følgende rekkefølge:</span><span class="sxs-lookup"><span data-stu-id="97559-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="97559-118">*Planlagt direkteoverføring*</span><span class="sxs-lookup"><span data-stu-id="97559-118">*Planned cross docking*</span></span>
1. <span data-ttu-id="97559-119">*Kryssoverføringsmaler med lokasjonsdirektiver*</span><span class="sxs-lookup"><span data-stu-id="97559-119">*Cross docking templates with location directives*</span></span>
    > [!NOTE]
    > <span data-ttu-id="97559-120">Ved hjelp av denne funksjonen kan **Direktivkode**-feltet angis i malen for direkteoverføring, på samme måte som du oppretter etterfyllingsmaler.</span><span class="sxs-lookup"><span data-stu-id="97559-120">This feature enables the **Directive code** field to be specified on the cross-docking template, similar to the way you set up replenishment templates.</span></span> <span data-ttu-id="97559-121">Hvis du aktiverer denne funksjonen, kan du legge til en direktivkode på arbeidsmallinjene for direkteoverføring for den endelige *Plasser*-linjen.</span><span class="sxs-lookup"><span data-stu-id="97559-121">Enabling this feature prevents you from adding a directive code on the cross-docking work template lines for the final *Put* line.</span></span> <span data-ttu-id="97559-122">Dette sikrer at den endelige plasseringslokasjonen kan bestemmes under oppretting av arbeidsprosesser før du vurderer arbeidsmaler.</span><span class="sxs-lookup"><span data-stu-id="97559-122">This ensures that the final put location can be determined during work creation before considering work templates.</span></span>

## <a name="setup"></a><span data-ttu-id="97559-123">Installasjon</span><span class="sxs-lookup"><span data-stu-id="97559-123">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="97559-124">Generer lastposteringsmetoder på nytt</span><span class="sxs-lookup"><span data-stu-id="97559-124">Regenerate load posting methods</span></span>

<span data-ttu-id="97559-125">Planlagt direkteoverføring er implementert som en lastposteringsmetode.</span><span class="sxs-lookup"><span data-stu-id="97559-125">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="97559-126">Når du har aktivert funksjonen, må du generere metodene på nytt.</span><span class="sxs-lookup"><span data-stu-id="97559-126">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="97559-127">Gå til **Lagerstyring \> Oppsett \> Lastposteringsmetoder**.</span><span class="sxs-lookup"><span data-stu-id="97559-127">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="97559-128">Velg **Regenerer metoder** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="97559-128">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="97559-129">Når regenereringen er fullført, skal det vises en metode som har **Metodenavn**-verdien *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="97559-129">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="97559-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="97559-130">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="97559-131">Opprett en direkteoverføringsmal</span><span class="sxs-lookup"><span data-stu-id="97559-131">Create a cross-docking template</span></span>

1. <span data-ttu-id="97559-132">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Direkteoverføringsmaler**.</span><span class="sxs-lookup"><span data-stu-id="97559-132">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="97559-133">I handlingsruten velger du **Ny** for å opprette en mal.</span><span class="sxs-lookup"><span data-stu-id="97559-133">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="97559-134">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="97559-134">In the header, set the following values:</span></span>

    - <span data-ttu-id="97559-135">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="97559-135">**Sequence:** *1*</span></span>

        <span data-ttu-id="97559-136">Dette feltet definerer rekkefølgen malene skal evalueres i.</span><span class="sxs-lookup"><span data-stu-id="97559-136">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="97559-137">**ID for direkteoverføringsmal:** *51*</span><span class="sxs-lookup"><span data-stu-id="97559-137">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="97559-138">**Beskrivelse:** *Lager 51*</span><span class="sxs-lookup"><span data-stu-id="97559-138">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="97559-139">**Policy for behovsfrigivelse:** *Før forsyningsmottak*</span><span class="sxs-lookup"><span data-stu-id="97559-139">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="97559-140">**Lager:** *51*</span><span class="sxs-lookup"><span data-stu-id="97559-140">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="97559-141">Oppsettet på **Planlegging**-hurtigfanen styrer hvordan malen fungerer.</span><span class="sxs-lookup"><span data-stu-id="97559-141">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="97559-142">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="97559-142">Set the following values:</span></span>

    - <span data-ttu-id="97559-143">**Behovskrav:** *Ingen*</span><span class="sxs-lookup"><span data-stu-id="97559-143">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="97559-144">Dette feltet definerer kravene til behovslageret.</span><span class="sxs-lookup"><span data-stu-id="97559-144">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="97559-145">Hvis behovet må kobles til forsyningen før frigivelse, velger du *Merking*.</span><span class="sxs-lookup"><span data-stu-id="97559-145">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="97559-146">Hvis behovet må være ordrereservert mot forsyningen før frigivelse, velger *Ordrereservering*.</span><span class="sxs-lookup"><span data-stu-id="97559-146">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="97559-147">**Lokaliseringstype:** *Forsendelseslokasjoner*</span><span class="sxs-lookup"><span data-stu-id="97559-147">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="97559-148">Dette feltet definerer om direkteoverføringsarbeidet skal bruke oppsamling/lastlokasjoner fra forsendelsen, eller om det skal bruke lokasjonsdirektiver til å finne egne oppsamling/lastlokasjoner.</span><span class="sxs-lookup"><span data-stu-id="97559-148">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="97559-149">**Arbeidsmal:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="97559-149">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="97559-150">Dette feltet definerer arbeidsmalen som skal brukes når du oppretter direkteoverføringsarbeid.</span><span class="sxs-lookup"><span data-stu-id="97559-150">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="97559-151">**Ny validering ved forsyningsmottak:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="97559-151">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="97559-152">Dette alternativet angir om forsyningen skal valideres på nytt under mottak.</span><span class="sxs-lookup"><span data-stu-id="97559-152">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="97559-153">Hvis dette alternativet er satt til *Ja*, kontrolleres både vinduet maksimal tid og området for utløpsdager.</span><span class="sxs-lookup"><span data-stu-id="97559-153">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="97559-154">**Direktivkode:** La dette feltet stå tomt</span><span class="sxs-lookup"><span data-stu-id="97559-154">**Directive code:** Leave this field blank</span></span>

        <span data-ttu-id="97559-155">Dette alternativet aktiveres av funksjonen *Kryssoverføringsmaler med lokasjonsdirektiver*.</span><span class="sxs-lookup"><span data-stu-id="97559-155">This option is enabled by the *Cross docking templates with location directives* feature.</span></span> <span data-ttu-id="97559-156">Systemet bruker lokasjonsdirektiver til å bidra til å finne den beste lokasjonen å flytte lageret for direkteoverføring til.</span><span class="sxs-lookup"><span data-stu-id="97559-156">The system uses location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="97559-157">Du kan definere alternativet ved å tilordne en direktivkode til hver relevante direkteoverføringsmal.</span><span class="sxs-lookup"><span data-stu-id="97559-157">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="97559-158">Hvis en direktivkode er angitt, søker systemet etter lokasjonsdirektiver per direktivkode når arbeid må genereres.</span><span class="sxs-lookup"><span data-stu-id="97559-158">If a directive code is set, the system will search location directives by directive code when work is generated.</span></span> <span data-ttu-id="97559-159">På denne måten kan du begrense lokasjonsdirektiver som brukes for en bestemt direkteoverføringsmal.</span><span class="sxs-lookup"><span data-stu-id="97559-159">In this way, you can limit location directives that are used for a particular cross-docking template.</span></span>

    - <span data-ttu-id="97559-160">**Validerer tidsvindu:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="97559-160">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="97559-161">Dette alternativet angir om maksimalt tidsvindu skal evalueres når en forsyningskilde velges.</span><span class="sxs-lookup"><span data-stu-id="97559-161">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="97559-162">Hvis dette alternativet er satt til *Ja*, blir feltene som er relatert til maksimale og minimale tidsvinduer, tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="97559-162">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="97559-163">**Maksimalt tidsvindu:** *5*</span><span class="sxs-lookup"><span data-stu-id="97559-163">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="97559-164">Dette feltet definerer maksimal periode som er tillatt mellom forsyningsmottak og etterspørselsavreise.</span><span class="sxs-lookup"><span data-stu-id="97559-164">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="97559-165">**Enhet for maksimalt tidsvindu:** *Dager*</span><span class="sxs-lookup"><span data-stu-id="97559-165">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="97559-166">**Minimum tidsvindu** *0*</span><span class="sxs-lookup"><span data-stu-id="97559-166">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="97559-167">Dette feltet definerer minimum periode som er tillatt mellom forsyningsmottak og etterspørselsavreise.</span><span class="sxs-lookup"><span data-stu-id="97559-167">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="97559-168">**Enhet for minimum tidsvindu:** *Dager*</span><span class="sxs-lookup"><span data-stu-id="97559-168">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="97559-169">**Utløpsområde (dager):** *0*</span><span class="sxs-lookup"><span data-stu-id="97559-169">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="97559-170">*FEFO-kriterier:* Dette feltet definerer det maksimale antallet dager mellom utløpsdatoen til det første utløpte partiet som for øyeblikket er i lageret, og partiet som mottas.</span><span class="sxs-lookup"><span data-stu-id="97559-170">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="97559-171">I **Forsyningskilder**-hurtigfanen angir du hvilke typer forsyning som er gyldige for denne malen.</span><span class="sxs-lookup"><span data-stu-id="97559-171">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="97559-172">Velg **Ny**, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="97559-172">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="97559-173">**Sekvensnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="97559-173">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="97559-174">**Forsyningskilde:** *Bestilling*</span><span class="sxs-lookup"><span data-stu-id="97559-174">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="97559-175">Opprette en arbeidsklasse</span><span class="sxs-lookup"><span data-stu-id="97559-175">Create a work class</span></span>

1. <span data-ttu-id="97559-176">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsklasser**.</span><span class="sxs-lookup"><span data-stu-id="97559-176">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="97559-177">I handlingsruten velger du **Ny** for å opprette en arbeidsklasse.</span><span class="sxs-lookup"><span data-stu-id="97559-177">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="97559-178">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="97559-178">Set the following values:</span></span>

    - <span data-ttu-id="97559-179">**Arbeidsklasse-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="97559-179">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="97559-180">**Beskrivelse:** *Direkteoverføring*</span><span class="sxs-lookup"><span data-stu-id="97559-180">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="97559-181">**Arbeidsordretype:** *Direkteoverføring*</span><span class="sxs-lookup"><span data-stu-id="97559-181">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="97559-182">Opprette en arbeidsmal</span><span class="sxs-lookup"><span data-stu-id="97559-182">Create a work template</span></span>

1. <span data-ttu-id="97559-183">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.</span><span class="sxs-lookup"><span data-stu-id="97559-183">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="97559-184">Angi *Direkteoverføring* i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="97559-184">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="97559-185">I handlingsruten velger du **Ny** for å legge til en linje i **Oversikt**-fanen.</span><span class="sxs-lookup"><span data-stu-id="97559-185">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="97559-186">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="97559-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="97559-187">**Sekvensnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="97559-187">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="97559-188">**Arbeidsmal:** *51 Direkteoverføring*</span><span class="sxs-lookup"><span data-stu-id="97559-188">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="97559-189">**Arbeidsmalbeskrivelse:** *51 Direkteoverføring*</span><span class="sxs-lookup"><span data-stu-id="97559-189">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="97559-190">Velg **Lagre** for å gjøre **Arbeidsmaldetaljer**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="97559-190">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="97559-191">På **Arbeidsmaldetaljer**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="97559-191">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="97559-192">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="97559-192">On the new line, set the following values:</span></span>

    - <span data-ttu-id="97559-193">**Arbeidstype:** *Plukk*</span><span class="sxs-lookup"><span data-stu-id="97559-193">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="97559-194">**Arbeidsklasse-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="97559-194">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="97559-195">Velg **Ny** for å legge til en ny linje, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="97559-195">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="97559-196">**Arbeidstype:** *Plasser*</span><span class="sxs-lookup"><span data-stu-id="97559-196">**Work type:** *Put*</span></span>
    - <span data-ttu-id="97559-197">**Arbeidsklasse-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="97559-197">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="97559-198">Velg **Lagre**, og Bekreft at det er merket av for **Gyldig** for *51 Direkteoverføring*-malen.</span><span class="sxs-lookup"><span data-stu-id="97559-198">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="97559-199">Arbeidsklasse-ID-en for *Plukk*- og *Plasser*-arbeidstypene må være like.</span><span class="sxs-lookup"><span data-stu-id="97559-199">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="97559-200">Opprette lokasjonsdirektiver</span><span class="sxs-lookup"><span data-stu-id="97559-200">Create location directives</span></span>

1. <span data-ttu-id="97559-201">Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.</span><span class="sxs-lookup"><span data-stu-id="97559-201">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="97559-202">I den venstre ruten setter du **Arbeidsordretype**-feltet til *Direkteoverføring*.</span><span class="sxs-lookup"><span data-stu-id="97559-202">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="97559-203">Velg **Ny** i handlingsruten, og angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="97559-203">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="97559-204">**Sekvensnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="97559-204">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="97559-205">**Navn:** *51 Direkteoverføringsplass*</span><span class="sxs-lookup"><span data-stu-id="97559-205">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="97559-206">**Arbeidstype:** *Plasser*</span><span class="sxs-lookup"><span data-stu-id="97559-206">**Work type:** *Put*</span></span>
    - <span data-ttu-id="97559-207">**Område:** *5*</span><span class="sxs-lookup"><span data-stu-id="97559-207">**Site:** *5*</span></span>
    - <span data-ttu-id="97559-208">**Lager:** *51*</span><span class="sxs-lookup"><span data-stu-id="97559-208">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="97559-209">Velg **Lagre** for å gjøre **Linjer**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="97559-209">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="97559-210">På **Linjer**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="97559-210">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="97559-211">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="97559-211">On the new line, set the following values:</span></span>

    - <span data-ttu-id="97559-212">**Fra-antall:** *1*</span><span class="sxs-lookup"><span data-stu-id="97559-212">**From quantity:** *1*</span></span>
    - <span data-ttu-id="97559-213">**Til-antall:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="97559-213">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="97559-214">Velg **Lagre** for å gjøre **Lokasjonsdirektivhandlinger**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="97559-214">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="97559-215">På hurtigfanen **Lokasjonsdirektivhandlinger** velger du **Ny** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="97559-215">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="97559-216">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="97559-216">On the new line, set the following values:</span></span>

    - <span data-ttu-id="97559-217">**Navn:** *Rampedør*</span><span class="sxs-lookup"><span data-stu-id="97559-217">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="97559-218">**Bruk av fast lokasjon:** *Faste og ikke-faste lokasjoner*</span><span class="sxs-lookup"><span data-stu-id="97559-218">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="97559-219">Velg **Lagre** for å gjøre **Rediger spørring**-knappen på **Lokasjonsdirektivhandlinger**-verktøylinjen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="97559-219">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="97559-220">Velg **Rediger spørring** for å åpne redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="97559-220">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="97559-221">I **Område**-fanen kontrollerer du at følgende to linjer er konfigurert:</span><span class="sxs-lookup"><span data-stu-id="97559-221">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="97559-222">Linje 1:</span><span class="sxs-lookup"><span data-stu-id="97559-222">Line 1:</span></span>

        - <span data-ttu-id="97559-223">**Tabell:** *Plasseringer*</span><span class="sxs-lookup"><span data-stu-id="97559-223">**Table:** *Locations*</span></span>
        - <span data-ttu-id="97559-224">**Avledet tabell:** *Lokasjoner*</span><span class="sxs-lookup"><span data-stu-id="97559-224">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="97559-225">**Felt:** *Lager*</span><span class="sxs-lookup"><span data-stu-id="97559-225">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="97559-226">**Kriterier:** *51*</span><span class="sxs-lookup"><span data-stu-id="97559-226">**Criteria:** *51*</span></span>

    - <span data-ttu-id="97559-227">Linje 2:</span><span class="sxs-lookup"><span data-stu-id="97559-227">Line 2:</span></span>

        - <span data-ttu-id="97559-228">**Tabell:** *Plasseringer*</span><span class="sxs-lookup"><span data-stu-id="97559-228">**Table:** *Locations*</span></span>
        - <span data-ttu-id="97559-229">**Avledet tabell:** *Lokasjoner*</span><span class="sxs-lookup"><span data-stu-id="97559-229">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="97559-230">**Felt:** *Lokasjon*</span><span class="sxs-lookup"><span data-stu-id="97559-230">**Field:** *Location*</span></span>
        - <span data-ttu-id="97559-231">**Kriterier:** *Rampedør*</span><span class="sxs-lookup"><span data-stu-id="97559-231">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="97559-232">Velg **OK** for å lukke redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="97559-232">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="97559-233">Opprette et menyelement for mobilenhet</span><span class="sxs-lookup"><span data-stu-id="97559-233">Create a mobile device menu item</span></span>

1. <span data-ttu-id="97559-234">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="97559-234">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="97559-235">I listen over menyelementer i venstre rute velger du **Kjøpsplassering**.</span><span class="sxs-lookup"><span data-stu-id="97559-235">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="97559-236">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="97559-236">Select **Edit**.</span></span>
1. <span data-ttu-id="97559-237">På **Arbeidsklasser**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="97559-237">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="97559-238">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="97559-238">On the new line, set the following values:</span></span>

    - <span data-ttu-id="97559-239">**Arbeidsklasse-ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="97559-239">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="97559-240">**Arbeidsordretype:** *Direkteoverføring*</span><span class="sxs-lookup"><span data-stu-id="97559-240">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="97559-241">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="97559-241">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="97559-242">Scenario</span><span class="sxs-lookup"><span data-stu-id="97559-242">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="97559-243">Opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="97559-243">Create a purchase order</span></span>

<span data-ttu-id="97559-244">Følg disse trinnene for å opprette en bestilling som en forsyningskilde.</span><span class="sxs-lookup"><span data-stu-id="97559-244">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="97559-245">Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="97559-245">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="97559-246">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="97559-246">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="97559-247">I **Opprett bestilling**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="97559-247">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="97559-248">**Leverandørkonto:** *104*</span><span class="sxs-lookup"><span data-stu-id="97559-248">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="97559-249">**Lager:** *51*</span><span class="sxs-lookup"><span data-stu-id="97559-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="97559-250">Velg **OK** og noter deg ordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="97559-250">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="97559-251">Det legges til en ny linje i rutenettet på **Bestillingslinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="97559-251">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="97559-252">På denne linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="97559-252">On this line, set the following values:</span></span>

    - <span data-ttu-id="97559-253">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="97559-253">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="97559-254">**Antall:** *5*</span><span class="sxs-lookup"><span data-stu-id="97559-254">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="97559-255">Opprette en salgsordre</span><span class="sxs-lookup"><span data-stu-id="97559-255">Create a sales order</span></span>

<span data-ttu-id="97559-256">Følg disse trinnene for å opprette en salgsordre som en behovskilde.</span><span class="sxs-lookup"><span data-stu-id="97559-256">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="97559-257">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="97559-257">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="97559-258">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="97559-258">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="97559-259">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="97559-259">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="97559-260">**Kundekonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="97559-260">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="97559-261">**Lager:** *51*</span><span class="sxs-lookup"><span data-stu-id="97559-261">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="97559-262">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97559-262">Select **OK**.</span></span>
1. <span data-ttu-id="97559-263">Det legges til en ny linje i rutenettet på **Salgsordrelinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="97559-263">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="97559-264">På denne linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="97559-264">On this line, set the following values:</span></span>

    - <span data-ttu-id="97559-265">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="97559-265">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="97559-266">**Antall:** *3*</span><span class="sxs-lookup"><span data-stu-id="97559-266">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="97559-267">Opprett planlagt direkteoverføring</span><span class="sxs-lookup"><span data-stu-id="97559-267">Create planned cross-docking</span></span>

<span data-ttu-id="97559-268">Følg disse trinnene for å opprette den planlagte direkteoverføringen fra salgsordren.</span><span class="sxs-lookup"><span data-stu-id="97559-268">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="97559-269">På **Salgsordredetaljer**-siden for salgsordren du nettopp opprettet, velger du **Frigi til lager** i handlingsruten på **Lager**-fanen i **Handlinger**-gruppen.</span><span class="sxs-lookup"><span data-stu-id="97559-269">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="97559-270">Frigi til lager-handling oppretter en forsendelse og lastlinje for salgsordrelinjen, og prøver å tildele beholdning.</span><span class="sxs-lookup"><span data-stu-id="97559-270">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="97559-271">Du får en informasjonsmelding.</span><span class="sxs-lookup"><span data-stu-id="97559-271">You receive an informational message.</span></span> <span data-ttu-id="97559-272">Du får også følgende advarsel: Ikke no arbeid ble opprettet for bølge XXXX.</span><span class="sxs-lookup"><span data-stu-id="97559-272">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="97559-273">Se loggen over oppretting av arbeid for detaljer.</span><span class="sxs-lookup"><span data-stu-id="97559-273">See the work creation history log for details."</span></span> <span data-ttu-id="97559-274">Denne virkemåten forventes fordi det ikke er noe beholdning i lageret.</span><span class="sxs-lookup"><span data-stu-id="97559-274">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="97559-275">På **Salgsordrelinjer**-fanen, på **Lager**-menyen, velger du **Forsendelsesdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="97559-275">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="97559-276">**Forsendelsesdetaljer**-siden vises og viser forsendelsen som ble opprettet for salgsordren.</span><span class="sxs-lookup"><span data-stu-id="97559-276">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="97559-277">I **Lastlinjer**-hurtigfanen legger du merke til at feltet **Planlagt direkteoverføringsantall** er satt til *3*.</span><span class="sxs-lookup"><span data-stu-id="97559-277">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="97559-278">Fordi det ikke var noe beholdning tilgjengelig på lageret, men en gyldig forsyningskilde vil bli mottatt i tidsvinduet som er definert i direkteoverføringsmalen, ble direkteoverføringsantallet opprettet.</span><span class="sxs-lookup"><span data-stu-id="97559-278">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="97559-279">I **Lastlinjer**-hurtigfanen velger du **Planlagt direkteoverføring** for å vise detaljene for direkteoverføringen som ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="97559-279">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="97559-280">Behandle direkteoverføringen</span><span class="sxs-lookup"><span data-stu-id="97559-280">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="97559-281">Bestilling mottatt på lagermobilappen</span><span class="sxs-lookup"><span data-stu-id="97559-281">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="97559-282">Systemet vil motta antallet på 5 fra bestillingen til mottakslokasjonen og opprette to arbeidsdeler.</span><span class="sxs-lookup"><span data-stu-id="97559-282">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="97559-283">Den første arbeids-ID-en som opprettes, har **Arbeidsordretype**-verdien *Direkteoverføring* og er koblet til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="97559-283">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="97559-284">Den har et antall på 3 og dirigeres til den endelige forsendelseslokasjonen, slik at den kan sendes umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="97559-284">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="97559-285">Den andre arbeids-ID-en som opprettes, har **Arbeidsordretype**-verdien *Bestillinger* og er koblet til bestillingen.</span><span class="sxs-lookup"><span data-stu-id="97559-285">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="97559-286">Den har gjenstående antall på 2 som ikke ble direkteoverført, og som sendes til plassering for lageret.</span><span class="sxs-lookup"><span data-stu-id="97559-286">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="97559-287">Logg på mobilenheten som en bruker i lageret *51*.</span><span class="sxs-lookup"><span data-stu-id="97559-287">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="97559-288">Gå til **Inngående \> Kjøpsmottak**.</span><span class="sxs-lookup"><span data-stu-id="97559-288">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="97559-289">I **PONum**-feltet angir du bestillingsnummeret.</span><span class="sxs-lookup"><span data-stu-id="97559-289">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="97559-290">I feltet **Antall** angi *5*.</span><span class="sxs-lookup"><span data-stu-id="97559-290">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="97559-291">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97559-291">Select **OK**.</span></span>
1. <span data-ttu-id="97559-292">På neste side angir du **Vare**-feltet til *A0001*.</span><span class="sxs-lookup"><span data-stu-id="97559-292">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="97559-293">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97559-293">Select **OK**.</span></span>
1. <span data-ttu-id="97559-294">På neste side kontrollerer du verdiene for **PONum**, **Vare** og **Antall** ved å velge **OK**.</span><span class="sxs-lookup"><span data-stu-id="97559-294">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="97559-295">Du mottar en Arbeid fullført-melding.</span><span class="sxs-lookup"><span data-stu-id="97559-295">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="97559-296">Velg **Avbryt** for å avslutte.</span><span class="sxs-lookup"><span data-stu-id="97559-296">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="97559-297">Plassering til direkteoverføring og bulk</span><span class="sxs-lookup"><span data-stu-id="97559-297">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="97559-298">For øyeblikket har begge arbeids-ID-ene samme målnummerskilt.</span><span class="sxs-lookup"><span data-stu-id="97559-298">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="97559-299">Hvis du vil fullføre de neste trinnene, må du hente arbeids-ID-en og målnummerskilt-ID-en.</span><span class="sxs-lookup"><span data-stu-id="97559-299">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="97559-300">Du kan få denne informasjonen fra arbeidsdetaljene for bestillingslinjen og salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="97559-300">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="97559-301">Du kan også gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer** og filtrere arbeid der **Lager**-verdien er *51*.</span><span class="sxs-lookup"><span data-stu-id="97559-301">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="97559-302">Gå til **Inngående \> Kjøpsplassering** på den mobile enheten, og angi målnummerskiltet fra arbeidet.</span><span class="sxs-lookup"><span data-stu-id="97559-302">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="97559-303">I **ID**-feltet angir du målnummerskilt-ID-en fra arbeidsdetaljene.</span><span class="sxs-lookup"><span data-stu-id="97559-303">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="97559-304">Direkteoverføringsplukking-siden viser plukklokasjonen (*RECV*), målnummerskiltet (*nummerskilt*), vare (*A0001*) og antall (*3*).</span><span class="sxs-lookup"><span data-stu-id="97559-304">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="97559-305">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97559-305">Select **OK**.</span></span>
1. <span data-ttu-id="97559-306">I feltet **mål-LP** angir du et målnummerskilt for nummerskilt-ID-en som skal plasseres (direkteoverføres) til forsendelsesstedet.</span><span class="sxs-lookup"><span data-stu-id="97559-306">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="97559-307">Du kan velge en hvilken som helst nummerskilt-ID.</span><span class="sxs-lookup"><span data-stu-id="97559-307">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="97559-308">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97559-308">Select **OK**.</span></span>
1. <span data-ttu-id="97559-309">På den neste siden angir du nummerskilt-ID-en i **ID**-feltet.</span><span class="sxs-lookup"><span data-stu-id="97559-309">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="97559-310">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97559-310">Select **OK**.</span></span>
1. <span data-ttu-id="97559-311">Bekreft arbeidet for plukking av det gjenstående antallet på 2, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="97559-311">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="97559-312">På den neste siden velger du **Fullført** for å avslutte plukkprosessen og begynne plasseringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="97559-312">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="97559-313">Mobilappen presenterer lokasjonen og nummerskiltet som varen skal plasseres i.</span><span class="sxs-lookup"><span data-stu-id="97559-313">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="97559-314">Bekreft masselagringen **Plasser** ved å velge **OK**.</span><span class="sxs-lookup"><span data-stu-id="97559-314">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="97559-315">Bekreft direkteoverføringen **Plasser** på neste side ved å velge **OK**.</span><span class="sxs-lookup"><span data-stu-id="97559-315">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="97559-316">Du mottar en Arbeid fullført-melding.</span><span class="sxs-lookup"><span data-stu-id="97559-316">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="97559-317">Velg **Avbryt** for å avslutte.</span><span class="sxs-lookup"><span data-stu-id="97559-317">Select **Cancel** to exit.</span></span>

<span data-ttu-id="97559-318">Illustrasjonen nedenfor viser hvordan det fullførte direkteoverføringsarbeidet kan vises i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="97559-318">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="97559-319">![Direkteoverføringsarbeid fullført](media/PlannedCrossDockingWork.png "Direkteoverføringsarbeid fullført")</span><span class="sxs-lookup"><span data-stu-id="97559-319">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]