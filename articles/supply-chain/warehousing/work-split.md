---
title: Oppdelt arbeid
description: Dette emnet gir informasjon om funksjonen for oppdelt arbeid. Med denne funksjonen kan du dele opp store arbeidsordrer i flere mindre arbeidsordrer som deretter kan tilordnes til flere lagerarbeidere. På denne måten kan det samme arbeidet plukkes samtidig av flere lagerarbeidere.
author: mirzaab
manager: tfehr
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e74b630e72d70829938f0f34efd624509b1ba7c3
ms.sourcegitcommit: 531be324bf706ca727d777720df899d6ddd3c2d7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/05/2020
ms.locfileid: "4434882"
---
# <a name="work-split"></a><span data-ttu-id="a5302-105">Oppdelt arbeid</span><span class="sxs-lookup"><span data-stu-id="a5302-105">Work split</span></span>

<span data-ttu-id="a5302-106">Med funksjonen for oppdelt arbeid kan du dele opp store arbeids-ID-er (det vil si arbeidsordrer som har flere linjer) i flere mindre arbeids-ID- som deretter kan tilordnes til flere lagerarbeidere.</span><span class="sxs-lookup"><span data-stu-id="a5302-106">Work split functionality lets you split large work IDs (that is, work orders that have several lines) into several smaller work IDs that you can then assign to multiple warehouse workers.</span></span> <span data-ttu-id="a5302-107">På denne måten kan det samme arbeidsopprettelsesnummeret plukkes samtidig av flere lagerarbeidere.</span><span class="sxs-lookup"><span data-stu-id="a5302-107">In this way, the same work creation number can be picked simultaneously by several warehouse workers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5302-108">Du kan bare dele opp arbeidsordrer som har statusen *Åpen* eller *Pågår*.</span><span class="sxs-lookup"><span data-stu-id="a5302-108">You can split only work orders that have a status of *Open* or *In-progress*.</span></span>

## <a name="turn-on-the-work-split-functionality"></a><span data-ttu-id="a5302-109">Aktivere funksjonen for oppdelt arbeid</span><span class="sxs-lookup"><span data-stu-id="a5302-109">Turn on the work split functionality</span></span>

<span data-ttu-id="a5302-110">Før du kan bruke funksjonen for oppdelt arbeid, må du aktivere funksjonen og den nødvendige funksjonen i systemet.</span><span class="sxs-lookup"><span data-stu-id="a5302-110">Before you can use the work split functionality, you must turn on the feature and its prerequisite feature in your system.</span></span> <span data-ttu-id="a5302-111">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonene og aktivere dem hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="a5302-111">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on as required.</span></span>

<span data-ttu-id="a5302-112">Først aktiverer du den nødvendige funksjonen *Organisasjonsomfattende arbeidsblokkering* hvis den ikke allerede er aktivert.</span><span class="sxs-lookup"><span data-stu-id="a5302-112">First, turn on the prerequisite *Organization-wide work blocking* feature if it isn't already turned on.</span></span> <span data-ttu-id="a5302-113">I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="a5302-113">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="a5302-114">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="a5302-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a5302-115">**Funksjonsnavn:** *Organisasjonsomfattende arbeidsblokkering*</span><span class="sxs-lookup"><span data-stu-id="a5302-115">**Feature name:** *Organization-wide work blocking*</span></span>

> [!NOTE]
> <span data-ttu-id="a5302-116">Når denne funksjonen er aktivert, blir dataoppgradering automatisk brukt etter at funksjonen er aktivert på tvers av alle juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="a5302-116">When this feature is activated, a data upgrade is automatically applied after the feature is turned on across all legal entities.</span></span>

<span data-ttu-id="a5302-117">Deretter aktiverer du *Oppdelt arbeid*-funksjonen, som er oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="a5302-117">Next, turn on the *Work split* feature, which is listed in the following way:</span></span>

- <span data-ttu-id="a5302-118">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="a5302-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a5302-119">**Funksjonsnavn:** *Oppdelt arbeid*</span><span class="sxs-lookup"><span data-stu-id="a5302-119">**Feature name:** *Work split*</span></span>

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a><span data-ttu-id="a5302-120">Forbedringer av sidene Arbeidsdetaljer og Alt arbeid</span><span class="sxs-lookup"><span data-stu-id="a5302-120">Enhancements to the Work details and All work pages</span></span>

<span data-ttu-id="a5302-121">Funksjonen *Oppdelt arbeid* legger til følgende to knapper i fanen **Arbeid** i handlingsruten på sidene **Arbeidsdetaljer** og **Alt arbeid**:</span><span class="sxs-lookup"><span data-stu-id="a5302-121">The *Work split* feature adds the following two buttons to the **Work** tab on the Action Pane of the **Work details** and **All work** pages:</span></span>

- <span data-ttu-id="a5302-122">**Del arbeid** – Del opp gjeldende arbeids-ID i flere mindre arbeids-ID-er som kan behandles av individuelle arbeidere.</span><span class="sxs-lookup"><span data-stu-id="a5302-122">**Split work** – Split the current work ID into multiple smaller work IDs that can be processed by separate workers.</span></span>
- <span data-ttu-id="a5302-123">**Avbryt arbeidsoppdelingsøkt** – Avbryt arbeidsoppdelingsøkten, og gjør arbeidet tilgjengelig for behandling.</span><span class="sxs-lookup"><span data-stu-id="a5302-123">**Cancel work split session** – Cancel the work split session, and make the work available for processing.</span></span>

<span data-ttu-id="a5302-124">![Knappene Del opp Arbeid og Avbryt arbeidsoppdelingsøkt](media/Work_split_buttons.png "Knappene Del opp Arbeid og Avbryt arbeidsoppdelingsøkt")</span><span class="sxs-lookup"><span data-stu-id="a5302-124">![Split work and Cancel work split session buttons](media/Work_split_buttons.png "Split work and Cancel work split session buttons")</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5302-125">Knappen **Del arbeid** er ikke tilgjengelig hvis noen av følgende betingelser er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="a5302-125">The **Split work** button won't be available if any of the following conditions are met:</span></span>
>
> - <span data-ttu-id="a5302-126">Arbeidsstatusen er noe annet enn *Åpen* eller *Pågår*.</span><span class="sxs-lookup"><span data-stu-id="a5302-126">The work status is something other than *Open* or *In progress*.</span></span>
> - <span data-ttu-id="a5302-127">En container-ID er knyttet til arbeids-ID-en.</span><span class="sxs-lookup"><span data-stu-id="a5302-127">A container ID is associated with the work ID.</span></span> <span data-ttu-id="a5302-128">(En container kan ikke deles systematisk, fordi den krever fysiske handlinger.)</span><span class="sxs-lookup"><span data-stu-id="a5302-128">(A container can't be systematically split, because it requires physical actions.)</span></span>
> - <span data-ttu-id="a5302-129">Arbeidet er knyttet til en gruppe.</span><span class="sxs-lookup"><span data-stu-id="a5302-129">The work is associated with a cluster.</span></span>
> - <span data-ttu-id="a5302-130">Arbeidsordretypen er noe annet enn en av følgende typer:</span><span class="sxs-lookup"><span data-stu-id="a5302-130">The work order type is something other than one of the following types:</span></span>
>
>    - <span data-ttu-id="a5302-131">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="a5302-131">Sales orders</span></span>
>    - <span data-ttu-id="a5302-132">Råvareplukking</span><span class="sxs-lookup"><span data-stu-id="a5302-132">Raw material picking</span></span>
>    - <span data-ttu-id="a5302-133">Utstedelse for overføring</span><span class="sxs-lookup"><span data-stu-id="a5302-133">Transfer issue</span></span>
>
> - <span data-ttu-id="a5302-134">Arbeidet deles for øyeblikket av en annen bruker.</span><span class="sxs-lookup"><span data-stu-id="a5302-134">The work is currently being split by another user.</span></span> <span data-ttu-id="a5302-135">Hvis du prøver å åpne delingssiden for arbeid som allerede deles av en annen bruker, får du følgende feilmelding: Arbeidet med ID \#\#\#\# deles for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="a5302-135">If you try to open the splitting page for work that is already being split by another user, you receive the following error message: "The work with ID \#\#\#\# is currently being split.</span></span> <span data-ttu-id="a5302-136">Prøv på nytt om noen minutter.</span><span class="sxs-lookup"><span data-stu-id="a5302-136">Retry in a few minutes.</span></span> <span data-ttu-id="a5302-137">Hvis du fortsatt får denne meldingen, kontakter du en overordnet.</span><span class="sxs-lookup"><span data-stu-id="a5302-137">If you continue to receive this message, contact a supervisor."</span></span>

<span data-ttu-id="a5302-138">En ny arbeidsblokkeringsårsak, *Del arbeid*, angir når arbeids-ID-en er i ferd med å deles opp.</span><span class="sxs-lookup"><span data-stu-id="a5302-138">A new work blocking reason, *Split work*, indicates when the work ID is in the process of being split.</span></span> <span data-ttu-id="a5302-139">Det vises både på siden **Del arbeid** og i lagerappen hvis en bruker prøver å kjøre arbeidet.</span><span class="sxs-lookup"><span data-stu-id="a5302-139">It's shown both on the **Split work** page and in the warehouse app if a user tries to run the work.</span></span> <span data-ttu-id="a5302-140">Når det brukes blokkeringsårsaker, endres navnet på det **Blokkert bølge**-feltet fra arbeids-ID-en til **Blokkert**.</span><span class="sxs-lookup"><span data-stu-id="a5302-140">When blocking reasons are used, the name of the **Blocked wave** field from the work ID is changed to **Blocked**.</span></span>

## <a name="initiate-a-work-split"></a><span data-ttu-id="a5302-141">Starte en arbeidsoppdeling</span><span class="sxs-lookup"><span data-stu-id="a5302-141">Initiate a work split</span></span>

<span data-ttu-id="a5302-142">Funksjonen legger til en ny **Del arbeid**-side som gjør det mulig for brukere å dele arbeidslinjer fra arbeids-ID-en.</span><span class="sxs-lookup"><span data-stu-id="a5302-142">The feature adds a new **Split work** page that lets users split work lines from the work ID.</span></span> <span data-ttu-id="a5302-143">Når siden åpnes for første gang, viser den linjer som har arbeidsstatusen *Åpen* og som kan deles.</span><span class="sxs-lookup"><span data-stu-id="a5302-143">When the page is first opened, it shows lines that have a work status of *Open* and that are available to be split.</span></span> <span data-ttu-id="a5302-144">I handlingsruten velger **Del arbeid** for å behandle det valgte arbeidet.</span><span class="sxs-lookup"><span data-stu-id="a5302-144">On the Action Pane, select **Split work** to process the selected work.</span></span>

<span data-ttu-id="a5302-145">Følg denne fremgangsmåten for å dele arbeid.</span><span class="sxs-lookup"><span data-stu-id="a5302-145">To split work, follow these steps.</span></span>

1. <span data-ttu-id="a5302-146">Åpne en av følgende sider:</span><span class="sxs-lookup"><span data-stu-id="a5302-146">Open one of the following work pages:</span></span>

    - <span data-ttu-id="a5302-147">**Arbeidsdetaljer** (**Lagerstyring \> Arbeid \> Arbeidsdetaljer**)</span><span class="sxs-lookup"><span data-stu-id="a5302-147">**Work details** (**Warehouse management \> Work \> Work details**)</span></span>
    - <span data-ttu-id="a5302-148">**Alt arbeid** (**Lagerstyring \> Arbeid \> Alt arbeid**)</span><span class="sxs-lookup"><span data-stu-id="a5302-148">**All work** (**Warehouse management \> Work \> All work**)</span></span>

1. <span data-ttu-id="a5302-149">Velg en arbeids-ID som skal deles, i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="a5302-149">In the grid, select a work ID to split.</span></span> <span data-ttu-id="a5302-150">Feltet **Arbeidsordretype** må være satt til en av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a5302-150">The **Work order type** field must be set to one of the following values:</span></span>

    - <span data-ttu-id="a5302-151">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="a5302-151">Sales orders</span></span>
    - <span data-ttu-id="a5302-152">Råvareplukking</span><span class="sxs-lookup"><span data-stu-id="a5302-152">Raw material picking</span></span>
    - <span data-ttu-id="a5302-153">Utstedelse for overføring</span><span class="sxs-lookup"><span data-stu-id="a5302-153">Transfer issue</span></span>

1. <span data-ttu-id="a5302-154">Velg **Del arbeid** i gruppen **Arbeid** i fanen **Arbeid** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a5302-154">On the Action Pane, on the **Work** tab, in the **Work** group, select **Split work**.</span></span>

    <span data-ttu-id="a5302-155">Siden **Del arbeid** vises og viser arbeidslinjene som er åpne og som kan deles.</span><span class="sxs-lookup"><span data-stu-id="a5302-155">The **Split work** page appears and shows the work lines that are open and available to be split.</span></span> <span data-ttu-id="a5302-156">Som standard vises bare tilgjengelige arbeidslinjer.</span><span class="sxs-lookup"><span data-stu-id="a5302-156">By default, only available work lines are shown.</span></span> <span data-ttu-id="a5302-157">Hvis du vil vise alle linjene for arbeids-ID-en (for eksempel linjer med arbeidstypen *Plasser*), merker du av for **Vis alle linjer** over rutenettet.</span><span class="sxs-lookup"><span data-stu-id="a5302-157">To view all lines for the work ID (for example, lines that have a work type of *Put*), select the **Show all lines** check box above the grid.</span></span>

    <span data-ttu-id="a5302-158">Følgende melding vises: Brukere kan ikke behandle linjer for arbeidet før du er ferdig med oppdelingen og lukker denne siden.</span><span class="sxs-lookup"><span data-stu-id="a5302-158">The following message is shown: "Users can't process lines of the work until you finish splitting and close this page."</span></span>

    <span data-ttu-id="a5302-159">Feltet **Arbeidsblokkeringsårsak** for gjeldende arbeid vil bli satt til *Delt arbeid*, og arbeidet blir blokkert.</span><span class="sxs-lookup"><span data-stu-id="a5302-159">The **Work blocking reason** field for the current work will be set to *Split work*, and the work will be blocked.</span></span>

    <span data-ttu-id="a5302-160">![Blokkeringsårsak](media/Blocking_reason.png "Blokkeringsårsak")</span><span class="sxs-lookup"><span data-stu-id="a5302-160">![Blocking reason](media/Blocking_reason.png "Blocking reason")</span></span>

1. <span data-ttu-id="a5302-161">Velg linjene som skal fjernes fra den gjeldende arbeids-ID-en, og legg til en ny arbeids-ID.</span><span class="sxs-lookup"><span data-stu-id="a5302-161">Select the lines to remove from the current work ID and add to a new work ID.</span></span> <span data-ttu-id="a5302-162">Følgende hendelser skjer:</span><span class="sxs-lookup"><span data-stu-id="a5302-162">The following events occur:</span></span>

    - <span data-ttu-id="a5302-163">Når du deler arbeidet, annulleres de valgte linjene eller linjene fra den opprinnelige arbeids-ID-en og kopieres til en ny arbeids-ID.</span><span class="sxs-lookup"><span data-stu-id="a5302-163">When you split the work, the selected line or lines from the original work ID are canceled and then copied to a new work ID.</span></span>
    - <span data-ttu-id="a5302-164">Den eksisterende arbeidsmalstrukturen og lokasjonen til plasseringen (og også fremtidige plukk/plasser-par) beholdes.</span><span class="sxs-lookup"><span data-stu-id="a5302-164">The existing work template structure and the location of the put (and also future pick/put pairs) are preserved.</span></span> <span data-ttu-id="a5302-165">Verdiene for følgende arbeids-ID-felter kopieres fra det opprinnelige arbeidet til det nye arbeidet:</span><span class="sxs-lookup"><span data-stu-id="a5302-165">Values for the following work ID fields are copied from the original work to the new work:</span></span>

        - <span data-ttu-id="a5302-166">Last-ID</span><span class="sxs-lookup"><span data-stu-id="a5302-166">Load ID</span></span>
        - <span data-ttu-id="a5302-167">Forsendelses-ID</span><span class="sxs-lookup"><span data-stu-id="a5302-167">Shipment ID</span></span>
        - <span data-ttu-id="a5302-168">Arbeidsordretype</span><span class="sxs-lookup"><span data-stu-id="a5302-168">Work order type</span></span>
        - <span data-ttu-id="a5302-169">Ordrenummer</span><span class="sxs-lookup"><span data-stu-id="a5302-169">Order number</span></span>
        - <span data-ttu-id="a5302-170">Site</span><span class="sxs-lookup"><span data-stu-id="a5302-170">Site</span></span>
        - <span data-ttu-id="a5302-171">Lager</span><span class="sxs-lookup"><span data-stu-id="a5302-171">Warehouse</span></span>
        - <span data-ttu-id="a5302-172">Arbeidsprioritet</span><span class="sxs-lookup"><span data-stu-id="a5302-172">Work priority</span></span>
        - <span data-ttu-id="a5302-173">ID for arbeidsutvalg</span><span class="sxs-lookup"><span data-stu-id="a5302-173">Work pool ID</span></span>
        - <span data-ttu-id="a5302-174">Bølge-ID</span><span class="sxs-lookup"><span data-stu-id="a5302-174">Wave ID</span></span>
        - <span data-ttu-id="a5302-175">Arbeidsopprettingsnummer</span><span class="sxs-lookup"><span data-stu-id="a5302-175">Work creation number</span></span>

    - <span data-ttu-id="a5302-176">Følgende felter kopieres ikke til den nye arbeids-ID-en:</span><span class="sxs-lookup"><span data-stu-id="a5302-176">The following fields aren't copied to the new work ID:</span></span>

        - <span data-ttu-id="a5302-177">**Arbeids-ID** – En ny arbeids-ID genereres fra den riktige nummerserien.</span><span class="sxs-lookup"><span data-stu-id="a5302-177">**Work ID** – A new work ID is generated from the appropriate number sequence.</span></span>
        - <span data-ttu-id="a5302-178">**Arbeidsstatus** – Dette feltet er satt til *Åpen*.</span><span class="sxs-lookup"><span data-stu-id="a5302-178">**Work status** – This field is set to *Open*.</span></span>
        - <span data-ttu-id="a5302-179">**Låst av** – Dette feltet er opprinnelig satt til tomt.</span><span class="sxs-lookup"><span data-stu-id="a5302-179">**Locked by** – This field is initially set to blank.</span></span>
        - <span data-ttu-id="a5302-180">**ID for målnummerskilt** – Dette feltet blir stående tomt.</span><span class="sxs-lookup"><span data-stu-id="a5302-180">**Target license plate ID** – This field is left blank.</span></span>
        - <span data-ttu-id="a5302-181">**Opprettingsdato og -klokkeslett** – Dette feltet blir satt til gjeldende dato og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="a5302-181">**Created date and time** – This field is set to the current date and time.</span></span>
        - <span data-ttu-id="a5302-182">**Blokkert bølge / låst** – Dette feltet omberegnes for den opprinnelige arbeids-ID-en og den nye arbeids-ID-en.</span><span class="sxs-lookup"><span data-stu-id="a5302-182">**Blocked wave/frozen** – This field is recomputed for the original work ID and the new work ID.</span></span>

1. <span data-ttu-id="a5302-183">Velg **Del arbeid** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a5302-183">On the Action Pane, select **Split work**.</span></span>

<span data-ttu-id="a5302-184">Mens arbeidet deles, vises følgende melding: Behandler operasjon – del arbeid.</span><span class="sxs-lookup"><span data-stu-id="a5302-184">While the work is being split, the following message is shown: "Processing operation - Split work".</span></span> <span data-ttu-id="a5302-185">Når denne meldingen er synlig, kan du avbryte operasjonen ved å velge **Avbryt** i meldingsboksen.</span><span class="sxs-lookup"><span data-stu-id="a5302-185">While this message is visible, you can cancel the operation by selecting **Cancel** in the message box.</span></span>

<span data-ttu-id="a5302-186">Hvis avmerkingsboksen **Vis alle linjer** ikke vises, vil ikke linjen som ble oppdelt og avbrutt, lenger vises i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="a5302-186">If the **Show all lines** check box is cleared, the line that was split off and canceled will no longer appear in the grid.</span></span> <span data-ttu-id="a5302-187">Hvis avmerkingsboksen er valgt, skal du se at verdien i **Arbeidsstatus**-feltet for den linjen er endret til *Avbrutt*.</span><span class="sxs-lookup"><span data-stu-id="a5302-187">If the check box is selected, you should see that the value of the **Work status** field for that line has changed to *Canceled*.</span></span>

<span data-ttu-id="a5302-188">Følgende varsel vises for å angi at den nye arbeids-ID-en er opprettet: Arbeid \#\#\#\#e r opprettet ved deling av opprinnelig arbeid \#\#\#\#.</span><span class="sxs-lookup"><span data-stu-id="a5302-188">The following notification is shown to indicate that the new work ID has been created: "Work \#\#\#\# has been created by splitting off from original work \#\#\#\#."</span></span>

<span data-ttu-id="a5302-189">Andre arbeidslinjer fra den opprinnelige arbeids-ID-en (for eksempel *Plasser*-linjer) blir justert som påkrevd for å gjenspeile arbeidslinjene som er avbrutt.</span><span class="sxs-lookup"><span data-stu-id="a5302-189">Other work lines from the original work ID (such as *Put* lines) will be adjusted as required to reflect the lines of work that have been canceled.</span></span> <span data-ttu-id="a5302-190">Hvis for eksempel den opprinnelige arbeids-ID-en hadde en *Plasser*-linje for et antall på 15, og *Plukk*-linjer som har et totalt antall på 10, ble avbrutt, vil det nye *plasseringsantallet* på den opprinnelige Arbeids-ID-en nå være 5.</span><span class="sxs-lookup"><span data-stu-id="a5302-190">For example, if the original work ID had a *Put* line for a quantity of 15, and *Pick* lines that have a total quantity of 10 were canceled, the new *Put* quantity on the original work ID will now be 5.</span></span>

<span data-ttu-id="a5302-191">Det nye arbeidet vil ikke umiddelbart være tilordnet til noen brukere.</span><span class="sxs-lookup"><span data-stu-id="a5302-191">The new work won't immediately be assigned to any user.</span></span> <span data-ttu-id="a5302-192">Du kan imidlertid tilordne det til en bruker nå, hvis det er nødvendig, ved å bruke standardfunksjonaliteten på siden **Arbeidsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="a5302-192">However, you can assign it to a user now, as required, by using the standard functionality of the **Work details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5302-193">Du kan bare dele arbeids-ID-er som inneholder to eller flere tilgjengelige arbeidslinjer.</span><span class="sxs-lookup"><span data-stu-id="a5302-193">You can split only work IDs that contain two or more available work lines.</span></span> <span data-ttu-id="a5302-194">Hvis du velger **Del arbeid** når det bare er én arbeidslinje, vil du få følgende feilmelding: Minst én arbeidslinje må forbli på innledende arbeid.</span><span class="sxs-lookup"><span data-stu-id="a5302-194">If you select **Split work** when there is only one work line, you will receive the following error message: "At least one work line must remain on initial work."</span></span> <span data-ttu-id="a5302-195">I dette tilfellet vil ingen oppdeling skje.</span><span class="sxs-lookup"><span data-stu-id="a5302-195">In this case, no splitting will occur.</span></span>

## <a name="finish-a-work-split"></a><span data-ttu-id="a5302-196">Fullfør en arbeidsoppdeling</span><span class="sxs-lookup"><span data-stu-id="a5302-196">Finish a work split</span></span>

<span data-ttu-id="a5302-197">Hvis du vil fullføre deling av arbeidet, må du fjerne blokkeringsårsaken *Del arbeid*.</span><span class="sxs-lookup"><span data-stu-id="a5302-197">To finish splitting work, the *Split work* blocking reason must be removed.</span></span> <span data-ttu-id="a5302-198">Det er to måter å fullføre dette trinnet på:</span><span class="sxs-lookup"><span data-stu-id="a5302-198">There are two ways to complete this step:</span></span>

- <span data-ttu-id="a5302-199">Brukeren som deler arbeidet, lukker siden **Del arbeid** ved å velge **Lukk**-knappen (**X**) øverst til høyre.</span><span class="sxs-lookup"><span data-stu-id="a5302-199">The user who is splitting the work closes the **Split work** page by selecting the **Close** button (**X**) in the upper-right corner.</span></span> <span data-ttu-id="a5302-200">Når siden er lukket, fjernes blokkeringsårsaken *Del arbeid*.</span><span class="sxs-lookup"><span data-stu-id="a5302-200">When the page is closed, the *Split Work* blocking reason will be removed.</span></span> <span data-ttu-id="a5302-201">*Blokkert*-statusen for dette arbeidet blir omberegnet, og hvis det ikke er noen gjenstående blokkeringsårsaker for dette arbeidet, oppheves blokkeringen av arbeidet.</span><span class="sxs-lookup"><span data-stu-id="a5302-201">The *Blocked* state of this work will be recomputed and, if there are no remaining blocking reasons for this work, the work will be unblocked.</span></span>
- <span data-ttu-id="a5302-202">Alle brukere som åpner arbeids-ID-en og velger knappen **Avbryt arbeidsoppdelingsøkt** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a5302-202">Any user opens the work ID and selects the **Cancel work split session** button on the Action Pane.</span></span> <span data-ttu-id="a5302-203">Blokkeringsårsaken *Del arbeid* blir fjernet, og *Blokkert*-statusen for dette arbeidet blir omberegnet, akkurat som når siden **Del arbeid** lukkes.</span><span class="sxs-lookup"><span data-stu-id="a5302-203">The *Split work* blocking reason will be removed, and the *Blocked* state of this work will be recomputed, just as when the **Split work** page is closed.</span></span>

<span data-ttu-id="a5302-204">Når blokkeringsårsaken *Delt arbeid* er fjernet, kan arbeidet kjøres på mobilenheten, forutsatt at statusen **Blokkert** er satt til *Nei* på arbeids-ID-en.</span><span class="sxs-lookup"><span data-stu-id="a5302-204">After the *Split work* blocking reason is removed, the work can be run on the mobile device, provided that the **Blocked** state is set to *No* on the work ID.</span></span>

## <a name="user-blocking-on-the-warehouse-app"></a><span data-ttu-id="a5302-205">Brukerblokkering i lagerappen</span><span class="sxs-lookup"><span data-stu-id="a5302-205">User blocking on the warehouse app</span></span>

<span data-ttu-id="a5302-206">Hvis du prøver å bruke lagerappen til å kjøre plukkarbeid mot en arbeids-ID som deles, får du følgende feilmelding: Arbeidet med ID \#\#\#\# deles for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="a5302-206">If you try to use the warehouse app to run picking work against a work ID that is being split, you will receive the following error message: "The work with ID \#\#\#\# is currently being split."</span></span> <span data-ttu-id="a5302-207">Hvis du får denne meldingen, velger du **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="a5302-207">If you receive this message, select **Cancel**.</span></span> <span data-ttu-id="a5302-208">Deretter kan du fortsette å behandle annet arbeid.</span><span class="sxs-lookup"><span data-stu-id="a5302-208">You can then continue to process other work.</span></span>

## <a name="other-blocked-operations"></a><span data-ttu-id="a5302-209">Andre blokkerte operasjoner</span><span class="sxs-lookup"><span data-stu-id="a5302-209">Other blocked operations</span></span>

<span data-ttu-id="a5302-210">Alle operasjoner som endrer arbeidslinjer, arbeidslagertransaksjoner eller etterfyllingskoblinger som er relatert til arbeid som deles, vil mislykkes, og følgende feilmelding vises: Arbeidet med ID \#\#\#\# deles nå.</span><span class="sxs-lookup"><span data-stu-id="a5302-210">Any operations that modify work lines, work inventory transactions, or replenishment links that are related to work that is being split will fail, and the following error message will be shown: "The work with ID \#\#\#\# is currently being split."</span></span>
