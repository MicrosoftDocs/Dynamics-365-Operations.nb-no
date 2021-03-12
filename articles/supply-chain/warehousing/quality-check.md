---
title: Kvalitetskontroll
description: Dette emnet inneholder informasjon om funksjonen Kvalitetskontroll. Denne funksjonen gjør det mulig for lagermedarbeidere å utføre stikkprøver for kvalitet når de mottar varer i mottakssonen.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 585ca933726cb932290f8abf8504aeb13848a0e5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996258"
---
# <a name="quality-check"></a><span data-ttu-id="d4167-104">Kvalitetskontroll</span><span class="sxs-lookup"><span data-stu-id="d4167-104">Quality check</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4167-105">Funksjonen *Kvalitetskontroll* gjør det mulig for lagermedarbeidere å utføre stikkprøver for kvalitet når de mottar varer i mottakssonen.</span><span class="sxs-lookup"><span data-stu-id="d4167-105">The *Quality check* feature lets warehouse workers do quick spot checks for quality while they receive items to the inbound dock area.</span></span> <span data-ttu-id="d4167-106">Disse stikkprøvene er nyttige når ansatte undersøker emballasje eller andre lett gjenkjennelige deler av en vare.</span><span class="sxs-lookup"><span data-stu-id="d4167-106">These spot checks are beneficial when workers inspect packaging or other easily recognizable parts of an item.</span></span> <span data-ttu-id="d4167-107">Funksjonen hjelper medarbeidere med å ta et raskt blikk på å se om noe er åpenbart feil eller skadet før de lagrer beholdningen på plasseringsstsedet.</span><span class="sxs-lookup"><span data-stu-id="d4167-107">The feature guides workers to take a quick look to see whether anything is obviously faulty or damaged before they stock the inventory in its putaway location.</span></span>

<span data-ttu-id="d4167-108">Denne funksjonen er et alternativ til standard kvalitetskontrollprosess.</span><span class="sxs-lookup"><span data-stu-id="d4167-108">This feature is an alternative to the standard quality check process.</span></span> <span data-ttu-id="d4167-109">Den gir større fleksibilitet og raskere behandling.</span><span class="sxs-lookup"><span data-stu-id="d4167-109">It offers more flexibility and faster processing.</span></span>

<span data-ttu-id="d4167-110">Når du bruker denne funksjonen, skjer ankomsten og kvalitetskontrollen på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="d4167-110">When you use this feature, the arrival and quality check occur in the following way:</span></span>

1. <span data-ttu-id="d4167-111">Når en forsendelse ankommer, registrerer en lagerarbeider ankomsten.</span><span class="sxs-lookup"><span data-stu-id="d4167-111">When a shipment arrives, a warehouse worker registers the arrival.</span></span> <span data-ttu-id="d4167-112">Arbeideren skanner også et nummerskilt for å registrere lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="d4167-112">The worker also scans a license plate to register the location.</span></span>
1. <span data-ttu-id="d4167-113">Arbeideren utfører en hurtig kvalitetskontroll og registrerer resultatet (bestått eller mislykket) for dette nummerskiltet.</span><span class="sxs-lookup"><span data-stu-id="d4167-113">The worker does a quick quality check and records the result (pass or fail) for that license plate.</span></span>
1. <span data-ttu-id="d4167-114">En av følgende handlinger inntreffer:</span><span class="sxs-lookup"><span data-stu-id="d4167-114">One of the following actions occurs:</span></span>

    - <span data-ttu-id="d4167-115">Hvis kvalitetskontrollen bestås, godtas nummerskiltet og rutes til en mottakslokasjon, som vanlig.</span><span class="sxs-lookup"><span data-stu-id="d4167-115">If the quality check is passed, the license plate is accepted and guided to a receiving location, as usual.</span></span>
    - <span data-ttu-id="d4167-116">Hvis kvalitetskontrollen mislykkes, avvises nummerskiltet og eksisterende plasseringsarbeid for det blir omadressert til en alternativ lokasjon for videre inspeksjon.</span><span class="sxs-lookup"><span data-stu-id="d4167-116">If the quality check is failed, the license plate is rejected, and existing putaway work for it is redirected to an alternate location for further inspection.</span></span> <span data-ttu-id="d4167-117">Det opprettes en ny kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="d4167-117">A new quality order is created.</span></span> <span data-ttu-id="d4167-118">Hvis du vil vise kvalitetsordren som ble opprettet fra den mislykkede kvalitetskontrollen, går du til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Kvalitetsordrer**.</span><span class="sxs-lookup"><span data-stu-id="d4167-118">To view the quality order that is created from the failed quality check, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="d4167-119">Denne prosessen kan også konfigureres slik at alle skannede nummerskilt sendes umiddelbart til kvalitetskontrollokasjonen.</span><span class="sxs-lookup"><span data-stu-id="d4167-119">This process can also be set up so that all scanned license plates are immediately diverted to the quality check location.</span></span>

## <a name="turn-on-the-quality-check-feature"></a><span data-ttu-id="d4167-120">Aktiver funksjonen Kvalitetskontroll</span><span class="sxs-lookup"><span data-stu-id="d4167-120">Turn on the Quality check feature</span></span>

<span data-ttu-id="d4167-121">Før du kan bruke funksjonen *Kvalitetskontroll*, må den være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="d4167-121">Before you can use the *Quality check* feature, it must be turned on in your system.</span></span> <span data-ttu-id="d4167-122">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="d4167-122">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d4167-123">I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="d4167-123">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d4167-124">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="d4167-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d4167-125">**Funksjonsnavn:** *Kvalitetskontroll*</span><span class="sxs-lookup"><span data-stu-id="d4167-125">**Feature name:** *Quality check*</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="d4167-126">Konfigurer funksjonen for eksempelscenarioet</span><span class="sxs-lookup"><span data-stu-id="d4167-126">Set up the feature for the example scenario</span></span>

<span data-ttu-id="d4167-127">Denne delen inneholder retningslinjer og et eksempel som viser hvordan du definerer funksjonen *Kvalitetskontroll* og klargjør eksempeldata foreksempel scenarioet som er oppgitt senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="d4167-127">This section provides guidelines and an example that shows how to set up the *Quality check* feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="d4167-128">Gjøre eksempeldata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="d4167-128">Make sample data available</span></span>

<span data-ttu-id="d4167-129">For å arbeide deg gjennom dette [eksempelscenarioet](#example-scenario) ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert.</span><span class="sxs-lookup"><span data-stu-id="d4167-129">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="d4167-130">Du må også velge den juridiske enheten **USMF** før du begynner.</span><span class="sxs-lookup"><span data-stu-id="d4167-130">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="quality-check-template"></a><a name="quality-template"></a><span data-ttu-id="d4167-131">Mal for kvalitetskontroll</span><span class="sxs-lookup"><span data-stu-id="d4167-131">Quality check template</span></span>

<span data-ttu-id="d4167-132">Kvalitetskontrollmalen definerer reglene for å utføre stikkprøver for kvalitet på det tidspunktet du mottar.</span><span class="sxs-lookup"><span data-stu-id="d4167-132">The quality check template defines the rules for doing quick spot checks for quality at the time of receiving.</span></span>

1. <span data-ttu-id="d4167-133">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Kvalitetskontrollmal**.</span><span class="sxs-lookup"><span data-stu-id="d4167-133">Go to **Warehouse management \> Setup \> Work \> Quality check template**.</span></span>
1. <span data-ttu-id="d4167-134">Velg **Ny** for å legge til en mal i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="d4167-134">Select **New** to add a template to the grid.</span></span>
1. <span data-ttu-id="d4167-135">Angi følgende verdier for å definere den nye malen:</span><span class="sxs-lookup"><span data-stu-id="d4167-135">Set the following values to define the new template:</span></span>

    - <span data-ttu-id="d4167-136">**Navn på kvalitetskontrollmal:** *Dock-kontroll*</span><span class="sxs-lookup"><span data-stu-id="d4167-136">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="d4167-137">Angi et navn som identifiserer policyene som brukes for denne malen.</span><span class="sxs-lookup"><span data-stu-id="d4167-137">Enter a name that identifies the policies applied for this template.</span></span>

    - <span data-ttu-id="d4167-138">**Godkjenningspolicy:** *Spør bruker*</span><span class="sxs-lookup"><span data-stu-id="d4167-138">**Acceptance policy:** *Prompt user*</span></span>

        <span data-ttu-id="d4167-139">Angi om brukere skal bli bedt om å godta eller avvise kvaliteten på beholdningen mens de behandler arbeidet, eller om kvaliteten skal avvises automatisk.</span><span class="sxs-lookup"><span data-stu-id="d4167-139">Specify whether users should be prompted to accept or reject the quality of the inventory while they process the work, or whether the quality should automatically be rejected.</span></span> <span data-ttu-id="d4167-140">De tilgjengelige alternativene er *Avvis automatisk* og *Spør bruker*.</span><span class="sxs-lookup"><span data-stu-id="d4167-140">The available options are *Auto reject* and *Prompt user*.</span></span>

    - <span data-ttu-id="d4167-141">**Policy for kvalitetsbehandling:** *Opprett kvalitetsordre*</span><span class="sxs-lookup"><span data-stu-id="d4167-141">**Quality processing policy:** *Create quality order*</span></span>

        <span data-ttu-id="d4167-142">Velg policyen som skal brukes når kvaliteten på beholdningen avvises.</span><span class="sxs-lookup"><span data-stu-id="d4167-142">Select the policy that should be used when the quality of the inventory is rejected.</span></span> <span data-ttu-id="d4167-143">Følgende alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="d4167-143">The following options are available:</span></span>

        - <span data-ttu-id="d4167-144">*Opprett bare arbeid* – Opprett bare arbeid for å gjøre beholdningsbevegelser enklere.</span><span class="sxs-lookup"><span data-stu-id="d4167-144">*Create work only* – Just create work to facilitate inventory movement.</span></span>
        - <span data-ttu-id="d4167-145">*Opprett kvalitetsordre* – Opprett en kvalitets ordre for å forenkle kvalitetstester.</span><span class="sxs-lookup"><span data-stu-id="d4167-145">*Create quality order* – Create a quality order to facilitate quality tests.</span></span>

    - <span data-ttu-id="d4167-146">**Testgruppe:** *Omslutning*</span><span class="sxs-lookup"><span data-stu-id="d4167-146">**Test group:** *Enclosure*</span></span>

        <span data-ttu-id="d4167-147">Angi testgruppen som skal brukes i kvalitetsordren som opprettes.</span><span class="sxs-lookup"><span data-stu-id="d4167-147">Specify the test group that should be used in the quality order that is created.</span></span> <span data-ttu-id="d4167-148">Testgrupper blir definert i **Lagerstyring**-modulen.</span><span class="sxs-lookup"><span data-stu-id="d4167-148">Test groups are set up in the **Inventory management** module.</span></span>

        <span data-ttu-id="d4167-149">La alternativet **Destruktiv tekst** være slått av for testgruppen.</span><span class="sxs-lookup"><span data-stu-id="d4167-149">Leave the **Destructive text** option turned off for the test group.</span></span> <span data-ttu-id="d4167-150">Dette alternativet definerer om prøven skal ødelegges som del av testene i testgruppen.</span><span class="sxs-lookup"><span data-stu-id="d4167-150">This option defines whether the sample will be destroyed as part of the tests in the test group.</span></span> <span data-ttu-id="d4167-151">Når en destruktiv test brukes, genererer system en beholdningstransaksjon der en kvalitetsordre opprettes for en vare.</span><span class="sxs-lookup"><span data-stu-id="d4167-151">If a destructive test is used, the system generates an inventory transaction when a quality order is created for an item.</span></span> <span data-ttu-id="d4167-152">Den nye lagertransaksjonen forutsier lagerreduksjonen for testantallet.</span><span class="sxs-lookup"><span data-stu-id="d4167-152">The new inventory transaction predicts the inventory reduction for the test quantity.</span></span> <span data-ttu-id="d4167-153">Beholdningsreduksjonen skjer når kvalitetsordren er fullført gjennom valideringstrinnet.</span><span class="sxs-lookup"><span data-stu-id="d4167-153">The inventory reduction occurs when the quality order is completed through the validation step.</span></span> <span data-ttu-id="d4167-154">Lagertransaksjonen identifiseres som en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="d4167-154">The inventory transaction is identified as a quality order.</span></span>

### <a name="work-class--quality-check"></a><a name="work-class"></a><span data-ttu-id="d4167-155">Arbeidsklasse – kvalitetskontroll</span><span class="sxs-lookup"><span data-stu-id="d4167-155">Work class – Quality check</span></span>

<span data-ttu-id="d4167-156">Arbeidsklasser brukes til å styre og/eller begrense typen arbeidsordrelinjer som lagermedarbeidere kan behandle på en mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="d4167-156">Work classes are used to direct and/or limit the type of work order lines that warehouse workers can process on a mobile device.</span></span>

1. <span data-ttu-id="d4167-157">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsklasser**.</span><span class="sxs-lookup"><span data-stu-id="d4167-157">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="d4167-158">Velg **Ny** for å opprette en arbeidsklasse.</span><span class="sxs-lookup"><span data-stu-id="d4167-158">Select **New** to create a work class.</span></span>
1. <span data-ttu-id="d4167-159">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d4167-159">In the header, set the following values:</span></span>

    - <span data-ttu-id="d4167-160">**Arbeidsklasse-ID:** *Kvalitetskontroll*</span><span class="sxs-lookup"><span data-stu-id="d4167-160">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="d4167-161">Angi et navn som identifiserer arbeidsklassen.</span><span class="sxs-lookup"><span data-stu-id="d4167-161">Enter a name that identifies the work class.</span></span>

    - <span data-ttu-id="d4167-162">**Beskrivelse:** *Kvalitetskontroll*</span><span class="sxs-lookup"><span data-stu-id="d4167-162">**Description:** *QC Check*</span></span>

        <span data-ttu-id="d4167-163">Angi en kort beskrivelse som angir hva arbeidsklassen brukes for.</span><span class="sxs-lookup"><span data-stu-id="d4167-163">Enter a short description that indicates what the work class is used for.</span></span>

    - <span data-ttu-id="d4167-164">**Arbeidsordretype:** *Kvalitetskontroll*</span><span class="sxs-lookup"><span data-stu-id="d4167-164">**Work order type:** *Quality in quality check*</span></span>

        <span data-ttu-id="d4167-165">Velg typen arbeidsordre som opprettes av arbeidsklassen.</span><span class="sxs-lookup"><span data-stu-id="d4167-165">Select the type of work order that is created by the work class.</span></span> <span data-ttu-id="d4167-166">Når du definerer arbeid for kvalitetskontroll, velger du alltid *Kvalitet i kvalitetskontroll*.</span><span class="sxs-lookup"><span data-stu-id="d4167-166">When you set up quality control work, always select *Quality in quality check*.</span></span>

1. <span data-ttu-id="d4167-167">På hurtigfanen **Gyldige plasseringslokasjonstyper** lar du feltet **Lokasjonstype** være tomt.</span><span class="sxs-lookup"><span data-stu-id="d4167-167">On the **Valid put location types** FastTab, leave the **Location type** field blank.</span></span>

    <span data-ttu-id="d4167-168">Hvis du velger en lokasjonstype, begrenser du lokasjonene der varer kan legges etter at de er plukket.</span><span class="sxs-lookup"><span data-stu-id="d4167-168">If you select a location type, you limit the locations where items can be put after they are picked.</span></span> <span data-ttu-id="d4167-169">Dette feltet brukes når et lokasjonsdirektiv forsøker å løse lokasjonen, eller når en lagermedarbeider angir lokasjonen for menyelementet for mobilenheten manuelt.</span><span class="sxs-lookup"><span data-stu-id="d4167-169">This field is used when a location directive tries to resolve the location, or when a warehouse worker manually specifies the location for the mobile device menu item.</span></span>

<span data-ttu-id="d4167-170">Hvis du vil ha mer informasjon om arbeidsklasser og hvordan du oppretter dem, kan du se [Opprette en arbeidsklasse](tasks/create-work-class.md).</span><span class="sxs-lookup"><span data-stu-id="d4167-170">For more information about work classes and how to create them, see [Create a work class](tasks/create-work-class.md).</span></span>

### <a name="work-template"></a><span data-ttu-id="d4167-171">Arbeidsmal</span><span class="sxs-lookup"><span data-stu-id="d4167-171">Work template</span></span>

<span data-ttu-id="d4167-172">Med arbeidsmaler kan du definere arbeidsoperasjoner som må utføres på lageret.</span><span class="sxs-lookup"><span data-stu-id="d4167-172">Work templates let you define the work operations that must be performed in the warehouse.</span></span> <span data-ttu-id="d4167-173">Vanligvis består lageroperasjoner av to handlinger: en lagerarbeider plukker opp beholdning på en lokasjon og plasserer den plukkede beholdningen på en annen lokasjon.</span><span class="sxs-lookup"><span data-stu-id="d4167-173">Typically, warehouse work operations consist of a pair of actions: a warehouse worker picks on-hand inventory up in one location and then puts the picked inventory down in another location.</span></span> <span data-ttu-id="d4167-174">En arbeidsmal for kvalitetskontroll definerer arbeidsoperasjonene for å utføre kvalitetskontroller.</span><span class="sxs-lookup"><span data-stu-id="d4167-174">A work template for quality control defines the work operations for doing quality checks.</span></span>

#### <a name="purchase-orders"></a><span data-ttu-id="d4167-175">Bestillinger</span><span class="sxs-lookup"><span data-stu-id="d4167-175">Purchase orders</span></span>

1. <span data-ttu-id="d4167-176">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.</span><span class="sxs-lookup"><span data-stu-id="d4167-176">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="d4167-177">I hodet setter du *Arbeidsordretype*-feltet til **Bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="d4167-177">In the header, set the **Work order type** field to *Purchase orders*.</span></span>
1. <span data-ttu-id="d4167-178">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="d4167-178">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="d4167-179">Velg en arbeidsmal som skal inneholde et kvalitetskontrolltrinn.</span><span class="sxs-lookup"><span data-stu-id="d4167-179">Select a work template that should include a quality check step.</span></span> <span data-ttu-id="d4167-180">I **Oversikt**-delen i **Arbeidsmal**-feltet velger du *51 bestillingsmottak*.</span><span class="sxs-lookup"><span data-stu-id="d4167-180">In the **Overview** section, in the **Work template** field, select *51 PO Receipt*.</span></span>
1. <span data-ttu-id="d4167-181">I delen **Arbeidsmaldetaljer** ser du at rutenettet har to eksisterende linjer: én for *plukking* og én for *plassering*.</span><span class="sxs-lookup"><span data-stu-id="d4167-181">In the **Work template details** section, notice that the grid has two existing lines: one for *Pick* and one for *Put*.</span></span>
1. <span data-ttu-id="d4167-182">i delen **Arbeidsmaldetaljer** velger du **Ny** for å legge til en rad for kvalitetskontroll i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="d4167-182">In the **Work template details** section, select **New** to add a row for quality control to the grid.</span></span> <span data-ttu-id="d4167-183">Legg merke til at **Linjenummer**-feltet for den nye linjen er satt til *3*.</span><span class="sxs-lookup"><span data-stu-id="d4167-183">Notice that the **Line number** field for the new line is set to *3*.</span></span>
1. <span data-ttu-id="d4167-184">På den nye linjen angir du følgende verdier.</span><span class="sxs-lookup"><span data-stu-id="d4167-184">On the new line, set the following values.</span></span> <span data-ttu-id="d4167-185">Godta standardverdiene for de resterende feltene.</span><span class="sxs-lookup"><span data-stu-id="d4167-185">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="d4167-186">**Arbeidstype:** *Kvalitetskontroll*</span><span class="sxs-lookup"><span data-stu-id="d4167-186">**Work type:** *Quality check*</span></span>
    - <span data-ttu-id="d4167-187">**Arbeidsklasse-ID:** *Kjøp*</span><span class="sxs-lookup"><span data-stu-id="d4167-187">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="d4167-188">**Navn på kvalitetskontrollmal:** *Dock-kontroll*</span><span class="sxs-lookup"><span data-stu-id="d4167-188">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="d4167-189">Velg den unike IDen for arbeidsklassen.</span><span class="sxs-lookup"><span data-stu-id="d4167-189">Select the unique ID for the work class.</span></span> <span data-ttu-id="d4167-190">Du bruker denne verdien til å konfigurere menyelementene på den mobile enheten og typene arbeid som disse menyelementene kan behandle.</span><span class="sxs-lookup"><span data-stu-id="d4167-190">You use this value to configure the menu items on the mobile device and the types of work that those menu items can process.</span></span>

1. <span data-ttu-id="d4167-191">I handlingsruten velger du **Lagre** for å lagre arbeidet så langt.</span><span class="sxs-lookup"><span data-stu-id="d4167-191">On the Action Pane, select **Save** to save your work so far.</span></span>

    <span data-ttu-id="d4167-192">Du mottar en informasjonsmelding som sier "Ugyldig – kvalitetskontroll må komme direkte etter en plukking".</span><span class="sxs-lookup"><span data-stu-id="d4167-192">You receive an informational message that states, "Invalid - Quality check must come directly after a pick."</span></span> <span data-ttu-id="d4167-193">Derfor må du endre **Linjenummer**-verdien for linjen du nettopp la til.</span><span class="sxs-lookup"><span data-stu-id="d4167-193">Therefore, you must change the **Line number** value for the line that you just added.</span></span>

1. <span data-ttu-id="d4167-194">Følg disse trinnene for å endre **Linjenummer**-verdien for den nye linjen:</span><span class="sxs-lookup"><span data-stu-id="d4167-194">Follow these steps to change the **Line number** value for the new line:</span></span>

    1. <span data-ttu-id="d4167-195">I delen **Arbeidsmaldetaljer** velger du linjen hvor **Arbeidstype**-feltet er satt til *Kvalitetskontroll*.</span><span class="sxs-lookup"><span data-stu-id="d4167-195">In the **Work template details** section, select the line where the **Work type** field is set to *Quality check*.</span></span>
    2. <span data-ttu-id="d4167-196">Velg knappen **Flytt opp** eller **Flytt ned** for å flytte *Kvalitetskontroll*-linjen slik at den er etter *Plukl*-linjen.</span><span class="sxs-lookup"><span data-stu-id="d4167-196">Select the **Move up** or **Move down** button to move the *Quality check* line so that it's after the *Pick* line.</span></span>

1. <span data-ttu-id="d4167-197">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d4167-197">On the Action Pane, select **Save**.</span></span>

#### <a name="quality-in-quality-check"></a><span data-ttu-id="d4167-198">Kvalitet i kvalitetskontroll</span><span class="sxs-lookup"><span data-stu-id="d4167-198">Quality in quality check</span></span>

<span data-ttu-id="d4167-199">Deretter oppretter du en arbeidsmal for kvalitetskontrollen.</span><span class="sxs-lookup"><span data-stu-id="d4167-199">Next, create a work template for the quality check.</span></span>

1. <span data-ttu-id="d4167-200">I hodet på **Arbeidsmaler**-siden endrer du verdien på **Arbeidsordretype**-feltet til *Kvalitetskontroll*.</span><span class="sxs-lookup"><span data-stu-id="d4167-200">In the header of the **Work templates** page, change the value of the **Work order type** field to *Quality in quality check*.</span></span>
1. <span data-ttu-id="d4167-201">I handlingsruten velger du **Ny** for å legge til en rad i rutenettet i **Oversikt**-delen.</span><span class="sxs-lookup"><span data-stu-id="d4167-201">On the Action Pane, select **New** to add a row to the grid in the **Overview** section.</span></span>
1. <span data-ttu-id="d4167-202">I den nye raden angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d4167-202">In the new row, set the following values:</span></span>

    - <span data-ttu-id="d4167-203">**Arbeidsmal:** *51 kvalitetskontroll*</span><span class="sxs-lookup"><span data-stu-id="d4167-203">**Work template:** *51 Quality Check*</span></span>

        <span data-ttu-id="d4167-204">Angi et navn for malen.</span><span class="sxs-lookup"><span data-stu-id="d4167-204">Enter a name for the template.</span></span>

    - <span data-ttu-id="d4167-205">**Beskrivelse av arbeidsmal:** *51 kvalitetskontroll*</span><span class="sxs-lookup"><span data-stu-id="d4167-205">**Work template description:** *51 Quality Check*</span></span>

1. <span data-ttu-id="d4167-206">I handlingsruten velger du **Lagre** for å gjøre **Arbeidsmaldetaljer**-delen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="d4167-206">On the Action Pane, select **Save** to make the **Work template details** section available.</span></span>
1. <span data-ttu-id="d4167-207">Mens den nye malen fortsatt er valgt i **Oversikt**-delen, velger du **Ny** i delen **Arbeidsmaldetaljer** for å legge til en rad i rutenettet der.</span><span class="sxs-lookup"><span data-stu-id="d4167-207">While the new template is still selected in the **Overview** section, select **New** in the **Work template details** section to add a row to the grid there.</span></span>
1. <span data-ttu-id="d4167-208">I den nye raden angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d4167-208">In the new row, set the following values:</span></span>

    - <span data-ttu-id="d4167-209">**Arbeidstype:** *Plukk*</span><span class="sxs-lookup"><span data-stu-id="d4167-209">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="d4167-210">**Arbeidsklasse-ID:** *Kvalitetskontroll*</span><span class="sxs-lookup"><span data-stu-id="d4167-210">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="d4167-211">Velg navnet på [arbeidsklassen](#work-class) som du opprettet tidligere for kvalitetskontrollarbeid.</span><span class="sxs-lookup"><span data-stu-id="d4167-211">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="d4167-212">I delen **Arbeidsmaldetaljer** velger du **Ny** igjen for å legge til en annen rad.</span><span class="sxs-lookup"><span data-stu-id="d4167-212">In the **Work template details** section, select **New** again to add another row.</span></span>
1. <span data-ttu-id="d4167-213">I den nye raden angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d4167-213">In the new row, set the following values:</span></span>

    - <span data-ttu-id="d4167-214">**Arbeidstype:** *Plasser*</span><span class="sxs-lookup"><span data-stu-id="d4167-214">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d4167-215">**Arbeidsklasse-ID:** *Kvalitetskontroll*</span><span class="sxs-lookup"><span data-stu-id="d4167-215">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="d4167-216">Velg navnet på [arbeidsklassen](#work-class) som du opprettet tidligere for kvalitetskontrollarbeid.</span><span class="sxs-lookup"><span data-stu-id="d4167-216">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="d4167-217">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d4167-217">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="d4167-218">Hvis du vil ha mer informasjon om arbeidsmaler, kan du se [Kontrollere lagerarbeid ved hjelp av arbeidsmaler og lokasjonsdirektiver](control-warehouse-location-directives.md).</span><span class="sxs-lookup"><span data-stu-id="d4167-218">For more information about work templates, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md)</span></span>

### <a name="location-directive--quality-failures"></a><span data-ttu-id="d4167-219">Lokasjonsdirektiv – kvalitetsfeil</span><span class="sxs-lookup"><span data-stu-id="d4167-219">Location directive – Quality failures</span></span>

<span data-ttu-id="d4167-220">Lokasjonsdirektiver er regler som bidrar til å identifisere plukke- og plasseringslokasjoner for lagerbevegelse.</span><span class="sxs-lookup"><span data-stu-id="d4167-220">Location directives are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="d4167-221">I en salgsordretransaksjon bestemmer for eksempel et lokasjonsdirektiv hvor varene blir plukket og hvor de plukkede varene skal plasseres.</span><span class="sxs-lookup"><span data-stu-id="d4167-221">For example, in a sales order transaction, a location directive determines where the items will be picked and where the picked items will be put.</span></span> <span data-ttu-id="d4167-222">Du må konfigurere en lokasjonsdirektivregel for å definere hvordan mislykkede kvalitetskontroller skal behandles.</span><span class="sxs-lookup"><span data-stu-id="d4167-222">You must configure a location directive rule to define how failed quality checks will be handled.</span></span>

1. <span data-ttu-id="d4167-223">Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.</span><span class="sxs-lookup"><span data-stu-id="d4167-223">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d4167-224">I den venstre ruten angir du **Arbeidsordretype**-feltet til *Bestillinger* for å arbeide med lokasjonsdirektiver av denne typen.</span><span class="sxs-lookup"><span data-stu-id="d4167-224">In the left pane, set the **Work order type** field to *Purchase orders* to work with location directives of that type.</span></span>
1. <span data-ttu-id="d4167-225">Velg **Ny** i handlingsruten for å opprette et lokasjonsdirektiv for kvalitetskontroller.</span><span class="sxs-lookup"><span data-stu-id="d4167-225">On the Action Pane, select **New** to create a location directive for quality checks.</span></span>
1. <span data-ttu-id="d4167-226">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d4167-226">In the header, set the following values:</span></span>

    - <span data-ttu-id="d4167-227">**Sekvensnummer:** Godta standardverdien.</span><span class="sxs-lookup"><span data-stu-id="d4167-227">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="d4167-228">**Navn:** *51 til kvalitet*</span><span class="sxs-lookup"><span data-stu-id="d4167-228">**Name:** *51 To Quality*</span></span>

1. <span data-ttu-id="d4167-229">Angi følgende verdier i **Lokasjonsdirektiver**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="d4167-229">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="d4167-230">Godta standardverdiene for de resterende feltene.</span><span class="sxs-lookup"><span data-stu-id="d4167-230">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="d4167-231">**Arbeidstype:** *Plasser*</span><span class="sxs-lookup"><span data-stu-id="d4167-231">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d4167-232">**Område:** *5*</span><span class="sxs-lookup"><span data-stu-id="d4167-232">**Site:** *5*</span></span>
    - <span data-ttu-id="d4167-233">**Lager:** *51*</span><span class="sxs-lookup"><span data-stu-id="d4167-233">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d4167-234">I handlingsruten velger du **Lagre** for å lagre direktivet og gjøre hurtigfanen **Linjer** tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="d4167-234">On the Action Pane select **Save** to save your directive and make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="d4167-235">På **Linjer**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="d4167-235">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d4167-236">På den nye linjen angir du følgende verdier.</span><span class="sxs-lookup"><span data-stu-id="d4167-236">On the new line, set the following values.</span></span> <span data-ttu-id="d4167-237">Godta standardverdiene for de resterende feltene.</span><span class="sxs-lookup"><span data-stu-id="d4167-237">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="d4167-238">**Fra-antall:** *1*</span><span class="sxs-lookup"><span data-stu-id="d4167-238">**From quantity:** *1*</span></span>
    - <span data-ttu-id="d4167-239">**Til-antall:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="d4167-239">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="d4167-240">I handlingsruten velger du **Lagre** for å lagre den nye linjen og gjøre hurtigfanen **Handlinger for lokasjonsdirektiv** tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="d4167-240">On the Action Pane, select **Save** to save the new line and make the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="d4167-241">Mens den nye linjen fremdeles er valgt på hurtigfanen **Linjer**, velger du **Ny** på hurtigfanen **Handlinger for lokasjonsdirektiv** for å legge til en rad i rutenettet der, slik at du kan definere en handling for linjen.</span><span class="sxs-lookup"><span data-stu-id="d4167-241">While the new line is still selected on the **Lines** FastTab, select **New** on the **Location directive actions** FastTab to add a row to the grid there, so that you can set up an action for the line.</span></span>
1. <span data-ttu-id="d4167-242">I den nye raden setter du **Navn**-feltet til *Kvalitet*.</span><span class="sxs-lookup"><span data-stu-id="d4167-242">In the new row, set the **Name** field to *Quality*.</span></span> <span data-ttu-id="d4167-243">Godta standardverdiene for de resterende feltene.</span><span class="sxs-lookup"><span data-stu-id="d4167-243">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="d4167-244">I handligsruten velger du **Lagre** for å gjøre **Rediger spørring**-knappen på **Lokasjonsdirektivhandlinger**-hurtigfanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="d4167-244">On the Action Pane, select **Save** to make the **Edit query** button on the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="d4167-245">Når linjen du nettopp la til, fremdeles er valgt i hurtigfanen **Handlinger for lokasjonsdirektiv**, velger du **Rediger spørring** for å åpne en dialogboks der du kan redigere spørringen for handlingen.</span><span class="sxs-lookup"><span data-stu-id="d4167-245">While the line that you just added is still selected on the **Location directive actions** FastTab, select **Edit query** to open a dialog box where you can edit the query for the action.</span></span>
1. <span data-ttu-id="d4167-246">På **Område**-fanen velger du **Legg til** for å legge til en rad i spørringen.</span><span class="sxs-lookup"><span data-stu-id="d4167-246">On the **Range** tab, select **Add** to add a row to the query.</span></span>
1. <span data-ttu-id="d4167-247">I den nye raden angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d4167-247">In the new row, set the following values:</span></span>

    - <span data-ttu-id="d4167-248">**Tabell:** *Plasseringer*</span><span class="sxs-lookup"><span data-stu-id="d4167-248">**Table:** *Locations*</span></span>
    - <span data-ttu-id="d4167-249">**Avledet tabell:** *Lokasjoner*</span><span class="sxs-lookup"><span data-stu-id="d4167-249">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="d4167-250">**Felt:** *Lokasjon*</span><span class="sxs-lookup"><span data-stu-id="d4167-250">**Field:** *Location*</span></span>
    - <span data-ttu-id="d4167-251">**Vilkår:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="d4167-251">**Criteria:** *QMS*</span></span>

    <span data-ttu-id="d4167-252">*QMS*-lokasjonen er en lagerlokasjon for kvalitet.</span><span class="sxs-lookup"><span data-stu-id="d4167-252">The *QMS* location is a warehouse location for quality.</span></span>

1. <span data-ttu-id="d4167-253">Velg **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="d4167-253">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="d4167-254">Du må nå endre rekkefølgen til lokasjonsdirektivene for bestilling for lager *51*.</span><span class="sxs-lookup"><span data-stu-id="d4167-254">You must now change the sequence of purchase order location directives for warehouse *51*.</span></span> <span data-ttu-id="d4167-255">Lagre det nye lokasjonsdirektivet *51 til kvalitet*, oppdater siden og velg lokasjonsdirektivet i listen.</span><span class="sxs-lookup"><span data-stu-id="d4167-255">Save the new *51 To Quality* location directive, refresh the page, and select the location directive in the list.</span></span> <span data-ttu-id="d4167-256">Deretter bruker du knappene **Flytt opp** og **Flytt ned** i handlingsruten til å plassere lokasjonsdirektivet for lager *51* i følgende rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="d4167-256">Then use the **Move up** and **Move down** buttons on the Action Pane to put the location directive for warehouse *51* in the following order.</span></span> <span data-ttu-id="d4167-257">(Før du velger **Flytt opp** eller **Flytt ned**, må du velge et lokasjonsdirektiv i listen.)</span><span class="sxs-lookup"><span data-stu-id="d4167-257">(Before you select **Move up** or **Move down**, you must select a location directive in the list.)</span></span>

    1. <span data-ttu-id="d4167-258">51 til kvalitet</span><span class="sxs-lookup"><span data-stu-id="d4167-258">51 To Quality</span></span>
    2. <span data-ttu-id="d4167-259">51 bestilling direkte</span><span class="sxs-lookup"><span data-stu-id="d4167-259">51 PO Direct</span></span>
    3. <span data-ttu-id="d4167-260">51 QMS</span><span class="sxs-lookup"><span data-stu-id="d4167-260">51 QMS</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="d4167-261">Menyelementer på mobilenheten</span><span class="sxs-lookup"><span data-stu-id="d4167-261">Mobile device menu items</span></span>

<span data-ttu-id="d4167-262">Konfigurer et menyelement slik at mobilenheter kan utføre **Kvalitetskontroll**-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="d4167-262">Configure a menu item so that mobile devices can perform the **Quality Check** function.</span></span>

#### <a name="purchase-putaway"></a><span data-ttu-id="d4167-263">Kjøpsplassering</span><span class="sxs-lookup"><span data-stu-id="d4167-263">Purchase putaway</span></span>

1. <span data-ttu-id="d4167-264">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="d4167-264">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="d4167-265">Velg menyelementet **Kjøpsplassering** i listen.</span><span class="sxs-lookup"><span data-stu-id="d4167-265">In the list, select the **Purchase put-away** menu item.</span></span>
1. <span data-ttu-id="d4167-266">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="d4167-266">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="d4167-267">I **Arbeidsklasser**-delenvelger du **Ny** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="d4167-267">In the **Work classes** section, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="d4167-268">I den nye raden angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d4167-268">In the new row, set the following values:</span></span>

    - <span data-ttu-id="d4167-269">**Arbeidsklasse-ID:** *Kvalitetskontroll*</span><span class="sxs-lookup"><span data-stu-id="d4167-269">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="d4167-270">Angi navnet på [arbeidsklassen](#work-class) som du opprettet tidligere for kvalitetskontrollarbeid.</span><span class="sxs-lookup"><span data-stu-id="d4167-270">Enter the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

    - <span data-ttu-id="d4167-271">**Arbeidsordretype:** *Kvalitetskontroll*</span><span class="sxs-lookup"><span data-stu-id="d4167-271">**Work order type:** *Quality in quality check*</span></span>

1. <span data-ttu-id="d4167-272">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d4167-272">On the Action Pane, select **Save**.</span></span>

#### <a name="purchase-order-line-receiving"></a><span data-ttu-id="d4167-273">Mottak av bestillingslinje</span><span class="sxs-lookup"><span data-stu-id="d4167-273">Purchase order line receiving</span></span>

1. <span data-ttu-id="d4167-274">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="d4167-274">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="d4167-275">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d4167-275">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d4167-276">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d4167-276">In the header, set the following values:</span></span>

    - <span data-ttu-id="d4167-277">**Menyelementnavn:** *PO-linjemottak*</span><span class="sxs-lookup"><span data-stu-id="d4167-277">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="d4167-278">**Tittel:** *PO-linjemottak*</span><span class="sxs-lookup"><span data-stu-id="d4167-278">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="d4167-279">**Modus:** *Arbeid*</span><span class="sxs-lookup"><span data-stu-id="d4167-279">**Mode:** *Work*</span></span>
    - <span data-ttu-id="d4167-280">**Bruke eksisterende arbeid:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="d4167-280">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="d4167-281">Angi følgende verdier i **Generelt**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="d4167-281">On the **General** FastTab, set the following values.</span></span> <span data-ttu-id="d4167-282">Godta standardverdiene for de resterende feltene.</span><span class="sxs-lookup"><span data-stu-id="d4167-282">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="d4167-283">**Arbeidsopprettingsprosess:** *Bestillingslinjemottak og -plassering*</span><span class="sxs-lookup"><span data-stu-id="d4167-283">**Work creation process:** *Purchase order line receiving and put away*</span></span>
    - <span data-ttu-id="d4167-284">**Generer nummerskilt:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="d4167-284">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="d4167-285">**Arbeidsmal:** *51 bestillingsmottak*</span><span class="sxs-lookup"><span data-stu-id="d4167-285">**Work template:** *51 PO Receipt*</span></span>

1. <span data-ttu-id="d4167-286">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d4167-286">On the Action Pane, select **Save**.</span></span>

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="d4167-287">Legge til menyelementet på en meny for mobilenhet</span><span class="sxs-lookup"><span data-stu-id="d4167-287">Add the menu item to a mobile device menu</span></span>

1. <span data-ttu-id="d4167-288">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="d4167-288">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="d4167-289">Velg **Innkommende**-,'menyen i den venstre ruten.</span><span class="sxs-lookup"><span data-stu-id="d4167-289">In the left pane, select the **Inbound** menu.</span></span>
1. <span data-ttu-id="d4167-290">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="d4167-290">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="d4167-291">I kolonnen **Tilgjengelige menyer og menyelementer** velger du det nye menyelementet **PO-linjemottak**.</span><span class="sxs-lookup"><span data-stu-id="d4167-291">In the **Available menus and menu items** column, select the new **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="d4167-292">Velg høyre pil-knappen for å flytte **PO-linjemottak** til kolonnen **Menystruktur**.</span><span class="sxs-lookup"><span data-stu-id="d4167-292">Select the right arrow button to move **PO line receiving** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="d4167-293">I kolonnen **Menystruktur** velger du **PO-linjemottak**, og deretter velger du pil opp eller pil ned for å flytte menyelementet til ønsket plassering på menyen på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="d4167-293">In the **Menu structure** column, select **PO line receiving**, and then select the up arrow or down arrow button to move the menu item to the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="d4167-294">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d4167-294">On the Action Pane, select **Save**.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="d4167-295">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="d4167-295">Example scenario</span></span>

<span data-ttu-id="d4167-296">Etter at du har gjort alle de tidligere beskrevne eksempeldataene tilgjengelige og konfigurert dem, kan du arbeide deg gjennom dette scenariet for å prøve ut *Kvalitetskontroll*-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="d4167-296">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Quality check* feature.</span></span> <span data-ttu-id="d4167-297">Verdiene som vises i dette scenariet, antar at du arbeider med standard demonstrasjonsdata, at du har valgt den juridiske enheten **USMF**, og at du klargjorde eksempelpostene som er beskrevet tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="d4167-297">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="d4167-298">Dette scenariet fungerer også som et eksempel som viser hvordan funksjonen kan brukes i et produksjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="d4167-298">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="d4167-299">Opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="d4167-299">Create a purchase order</span></span>

1. <span data-ttu-id="d4167-300">Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="d4167-300">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="d4167-301">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d4167-301">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d4167-302">I **Opprett bestilling**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d4167-302">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d4167-303">**Leverandørkonto:** *104*</span><span class="sxs-lookup"><span data-stu-id="d4167-303">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="d4167-304">**Lager:** *51*</span><span class="sxs-lookup"><span data-stu-id="d4167-304">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d4167-305">Velg **OK** for å lukke dialogboksen og opprette den nye bestillingen.</span><span class="sxs-lookup"><span data-stu-id="d4167-305">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="d4167-306">På hurtigfanen **Bestillingslinjer** inneholder rutenettet en ny, tom linje.</span><span class="sxs-lookup"><span data-stu-id="d4167-306">On the **Purchase order lines** FastTab, the grid contains a new, blank line.</span></span> <span data-ttu-id="d4167-307">På denne linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d4167-307">On this line, set the following values:</span></span>

    - <span data-ttu-id="d4167-308">**Varenummer:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="d4167-308">**Item number:** *M9203*</span></span>
    - <span data-ttu-id="d4167-309">**Antall:** *3*</span><span class="sxs-lookup"><span data-stu-id="d4167-309">**Quantity:** *3*</span></span>
    - <span data-ttu-id="d4167-310">**Enhet:** *PL*</span><span class="sxs-lookup"><span data-stu-id="d4167-310">**Unit:** *PL*</span></span>

1. <span data-ttu-id="d4167-311">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d4167-311">On the Action Pane, select **Save**.</span></span>

### <a name="process-quality-check-receiving"></a><span data-ttu-id="d4167-312">Behandle kvalitetskontrollmottak</span><span class="sxs-lookup"><span data-stu-id="d4167-312">Process quality check receiving</span></span>

<span data-ttu-id="d4167-313">Når bestillingen er opprettet, kan den mottas ved hjelp av menyelementet **PO-linjemottak** og funksjonaliteten i *Kvalitetskontroll*-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="d4167-313">After the purchase order has been created, it can be received by using the **PO line receiving** menu item and the functionality of the *Quality check* feature.</span></span>

#### <a name="receive-pallet-1"></a><span data-ttu-id="d4167-314">Motta pall 1</span><span class="sxs-lookup"><span data-stu-id="d4167-314">Receive pallet 1</span></span>

1. <span data-ttu-id="d4167-315">Logg på lagerappen som en bruker for lageret *51*.</span><span class="sxs-lookup"><span data-stu-id="d4167-315">Sign in to the warehouse app as a user for warehouse *51*.</span></span> <span data-ttu-id="d4167-316">(Angi *51* som bruker-ID og *1* som passord.)</span><span class="sxs-lookup"><span data-stu-id="d4167-316">(Enter *51* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="d4167-317">Gå til **Innkommende \> PO-linjemottak**.</span><span class="sxs-lookup"><span data-stu-id="d4167-317">Go to **Inbound \> PO line receiving**.</span></span>
1. <span data-ttu-id="d4167-318">I **PONUM**-feltet angir du bestillingsnummeret.</span><span class="sxs-lookup"><span data-stu-id="d4167-318">In the **PONUM** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="d4167-319">Bekreft bestillingsnummeret.</span><span class="sxs-lookup"><span data-stu-id="d4167-319">Confirm the purchase order number.</span></span>
1. <span data-ttu-id="d4167-320">I **LINENUM**-feltet angir du nummeret på bestillingslinjen som mottas.</span><span class="sxs-lookup"><span data-stu-id="d4167-320">In the **LINENUM** field, enter the number of the purchase order line that is being received.</span></span> <span data-ttu-id="d4167-321">Fordi ordren bare har én linje i dette scenariet, vil du angi *1* i **LINENUM**-feltet for hvert mottakstrinn.</span><span class="sxs-lookup"><span data-stu-id="d4167-321">Because the order has only one line in this scenario, you will enter *1* in the **LINENUM** field for each receiving step.</span></span>
1. <span data-ttu-id="d4167-322">Bekreft linjenummeret.</span><span class="sxs-lookup"><span data-stu-id="d4167-322">Confirm the line number.</span></span>
1. <span data-ttu-id="d4167-323">I **QTY**-feltet angir du antallet som skal mottas.</span><span class="sxs-lookup"><span data-stu-id="d4167-323">In the **QTY** field, enter the quantity to receive.</span></span> <span data-ttu-id="d4167-324">Fordi bestillingen er for tre paller (*PL*) i dette scenariet, og det er tremottaks trinn, angir du *1* i **QTY**-feltet for hvert mottakstrinn.</span><span class="sxs-lookup"><span data-stu-id="d4167-324">Because the purchase order is for three pallets (*PL*) in this scenario, and there are three receiving steps, you will enter *1* in the **QTY** field for each receiving step.</span></span>
1. <span data-ttu-id="d4167-325">Bekreft antallet.</span><span class="sxs-lookup"><span data-stu-id="d4167-325">Confirm the quantity.</span></span>

    <span data-ttu-id="d4167-326">Siden **Kvalitetskontroll** som vises, har ingen oppføringsfelt.</span><span class="sxs-lookup"><span data-stu-id="d4167-326">The **Quality check** page that appears has no entry fields.</span></span> <span data-ttu-id="d4167-327">Den har bare bekreftelsesknappen (hakemerke) nederst og menyknappen (**≡**) øverst.</span><span class="sxs-lookup"><span data-stu-id="d4167-327">It has only the confirmation (check mark) button at the bottom and the Menu button (**≡**) at the top.</span></span> <span data-ttu-id="d4167-328">(Meny-knappen kalles noen ganger for hamburgeren eller hamburgerknappen.) Hvis du vil ekspedere kvalitetskontrollprosessen, må brukere bare bekrefte siden **Kvalitetskontroll** når pallen består kvalitetskontrollen.</span><span class="sxs-lookup"><span data-stu-id="d4167-328">(The Menu button is sometimes referred to as the hamburger or the hamburger button.) To expedite the quality check process, when the pallet passes the quality check, the user just confirms the **Quality check** page.</span></span>

    <span data-ttu-id="d4167-329">![Siden Kvalitetskontroll](media/quality-check.png "Siden Kvalitetskontroll")</span><span class="sxs-lookup"><span data-stu-id="d4167-329">![Quality check page](media/quality-check.png "Quality check page")</span></span>

1. <span data-ttu-id="d4167-330">Velg bekreftelsesknappen for å bestå kvalitetskontrollen for pall 1 fra linje 1.</span><span class="sxs-lookup"><span data-stu-id="d4167-330">Select the confirmation button to pass the quality check for pallet 1 from line 1.</span></span>

    <span data-ttu-id="d4167-331">Siden **Bestillinger: Plasser** som vises, viser detaljer om plasseringsarbeidet:</span><span class="sxs-lookup"><span data-stu-id="d4167-331">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="d4167-332">**LOC:** Plasseringen som systemet har fastslått</span><span class="sxs-lookup"><span data-stu-id="d4167-332">**LOC:** The system determined location</span></span>

        <span data-ttu-id="d4167-333">Denne lokasjonen er den tilordnede plasseringslokasjonen for bestillingsmottak.</span><span class="sxs-lookup"><span data-stu-id="d4167-333">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="d4167-334">**LP:** Den systemgenererte nummerskilt-ID-en</span><span class="sxs-lookup"><span data-stu-id="d4167-334">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="d4167-335">**Vare:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="d4167-335">**Item:** *M9203*</span></span>
    - <span data-ttu-id="d4167-336">**Ant.:** *1 PL: 100 per stk*</span><span class="sxs-lookup"><span data-stu-id="d4167-336">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="d4167-337">Varebeskrivelsen vises også.</span><span class="sxs-lookup"><span data-stu-id="d4167-337">The item description is also shown.</span></span>

1. <span data-ttu-id="d4167-338">Bekreft plasseringsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="d4167-338">Confirm the putaway work.</span></span>

    <span data-ttu-id="d4167-339">På **Oppgave**-siden for bestillingslinjemottak vises meldingen "Arbeid fullført".</span><span class="sxs-lookup"><span data-stu-id="d4167-339">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="d4167-340">**LINENUM**-feltet er tilgjengelig, slik at du kan begynne å motta den neste pallen.</span><span class="sxs-lookup"><span data-stu-id="d4167-340">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

#### <a name="receive-pallet-2"></a><span data-ttu-id="d4167-341">Motta pall 2</span><span class="sxs-lookup"><span data-stu-id="d4167-341">Receive pallet 2</span></span>

<span data-ttu-id="d4167-342">For dette scenariet vil pall 2 bli avvist.</span><span class="sxs-lookup"><span data-stu-id="d4167-342">For this scenario, pallet 2 will be rejected.</span></span>

1. <span data-ttu-id="d4167-343">I **LINENUM**-feltet angir du *1* og bekrefter linjenummeret.</span><span class="sxs-lookup"><span data-stu-id="d4167-343">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="d4167-344">**QTY**-feltet er nå tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="d4167-344">The **QTY** field is now available.</span></span> <span data-ttu-id="d4167-345">Angi *1*, og bekreft antallet.</span><span class="sxs-lookup"><span data-stu-id="d4167-345">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="d4167-346">Siden **Kvalitetskontroll** vises.</span><span class="sxs-lookup"><span data-stu-id="d4167-346">The **Quality check** page appears.</span></span> <span data-ttu-id="d4167-347">For dette mottaket vil pallen bli avvist for kvalitet, og den vil plasseres i *QMS*-kvalitetslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="d4167-347">For this receipt, the pallet will be rejected for quality, and it will be put into the *QMS* quality location.</span></span>

1. <span data-ttu-id="d4167-348">Velg menyknappen (**≡**) øverst på siden, og velg deretter **Avvis** på menyen.</span><span class="sxs-lookup"><span data-stu-id="d4167-348">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Reject**.</span></span>
1. <span data-ttu-id="d4167-349">På **Oppgave**-siden som vises, angir du **QMS** som *Plassering*-lokasjon å sende pallen til for videre inspeksjon.</span><span class="sxs-lookup"><span data-stu-id="d4167-349">On the **Task** page that appears, enter **QMS** as the *Put* location to send the pallet to for further inspection.</span></span>

    <span data-ttu-id="d4167-350">Siden **Kvalitet i kvalitetskontroll: Plasser** som vises, viser detaljer om plasseringsarbeidet:</span><span class="sxs-lookup"><span data-stu-id="d4167-350">The **Quality in quality check: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="d4167-351">**LOC:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="d4167-351">**LOC:** *QMS*</span></span>

        <span data-ttu-id="d4167-352">Denne lokasjonen er den tilordnede plasseringslokasjonen for mottak med avvist kvalitet.</span><span class="sxs-lookup"><span data-stu-id="d4167-352">This location is the designated putaway location for rejected quality receiving.</span></span>

    - <span data-ttu-id="d4167-353">**LP:** Den systemgenererte nummerskilt-ID-en</span><span class="sxs-lookup"><span data-stu-id="d4167-353">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="d4167-354">**Vare:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="d4167-354">**Item:** *M9203*</span></span>
    - <span data-ttu-id="d4167-355">**Ant.:** *1 PL: 100 per stk*</span><span class="sxs-lookup"><span data-stu-id="d4167-355">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="d4167-356">Varebeskrivelsen vises også.</span><span class="sxs-lookup"><span data-stu-id="d4167-356">The item description is also shown.</span></span>

1. <span data-ttu-id="d4167-357">Bekreft plasseringsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="d4167-357">Confirm the putaway work.</span></span>

    <span data-ttu-id="d4167-358">På **Oppgave**-siden for bestillingslinjemottak vises meldingen "Arbeid fullført".</span><span class="sxs-lookup"><span data-stu-id="d4167-358">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="d4167-359">**LINENUM**-feltet er tilgjengelig, slik at du kan begynne å motta den neste pallen.</span><span class="sxs-lookup"><span data-stu-id="d4167-359">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

<span data-ttu-id="d4167-360">Du har nå fullført kvalitetskontrollen og opprettet en kvalitetsordre for den avviste pallen.</span><span class="sxs-lookup"><span data-stu-id="d4167-360">You've now completed the quality check and created a quality order for the rejected pallet.</span></span> <span data-ttu-id="d4167-361">Hvis du vil vise ordren som ble opprettet, går du til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Kvalitetsordrer**.</span><span class="sxs-lookup"><span data-stu-id="d4167-361">To view the order that was created, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="d4167-362">Testing av kvalitetsordre kan nå behandles.</span><span class="sxs-lookup"><span data-stu-id="d4167-362">Quality order testing can now be processed.</span></span> <span data-ttu-id="d4167-363">Kvalitetstesting dekkes ikke i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="d4167-363">Quality testing isn't covered in this topic.</span></span>

<span data-ttu-id="d4167-364">Hvis du vil ha mer informasjon om kvalitetsbehandling, kan du se [Oversikt over kvalitetsbehandling](../inventory/enable-quality-management.md).</span><span class="sxs-lookup"><span data-stu-id="d4167-364">For more information about quality management, see [Quality management overview](../inventory/enable-quality-management.md)</span></span>

#### <a name="receive-pallet-3"></a><span data-ttu-id="d4167-365">Motta pall 3</span><span class="sxs-lookup"><span data-stu-id="d4167-365">Receive pallet 3</span></span>

<span data-ttu-id="d4167-366">For dette scenariet vil pall 3 bli godtatt.</span><span class="sxs-lookup"><span data-stu-id="d4167-366">For this scenario, pallet 3 will be accepted.</span></span>

1. <span data-ttu-id="d4167-367">I **LINENUM**-feltet angir du *1* og bekrefter linjenummeret.</span><span class="sxs-lookup"><span data-stu-id="d4167-367">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="d4167-368">**QTY**-feltet er nå tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="d4167-368">The **QTY** field is now available.</span></span> <span data-ttu-id="d4167-369">Angi *1*, og bekreft antallet.</span><span class="sxs-lookup"><span data-stu-id="d4167-369">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="d4167-370">Siden **Kvalitetskontroll** vises.</span><span class="sxs-lookup"><span data-stu-id="d4167-370">The **Quality check** page appears.</span></span> <span data-ttu-id="d4167-371">For dette mottaket vil pallen bli godtatt for kvalitet, og den vil plasseres i en samlet plasseringslokasjon.</span><span class="sxs-lookup"><span data-stu-id="d4167-371">For this receipt, the pallet will be accepted for quality, and it will be put into a bulk putaway location.</span></span>

1. <span data-ttu-id="d4167-372">Velg bekreftelsesknappen for å bestå kvalitetskontrollen.</span><span class="sxs-lookup"><span data-stu-id="d4167-372">Select the confirmation button to pass the quality check.</span></span>

    <span data-ttu-id="d4167-373">Siden **Bestillinger: Plasser** som vises, viser detaljer om plasseringsarbeidet:</span><span class="sxs-lookup"><span data-stu-id="d4167-373">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="d4167-374">**LOC:** Plasseringen som systemet har fastslått</span><span class="sxs-lookup"><span data-stu-id="d4167-374">**LOC:** The system determined location</span></span>

        <span data-ttu-id="d4167-375">Denne lokasjonen er den tilordnede plasseringslokasjonen for bestillingsmottak.</span><span class="sxs-lookup"><span data-stu-id="d4167-375">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="d4167-376">**LP:** Den systemgenererte nummerskilt-ID-en</span><span class="sxs-lookup"><span data-stu-id="d4167-376">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="d4167-377">**Vare:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="d4167-377">**Item:** *M9203*</span></span>
    - <span data-ttu-id="d4167-378">**Ant.:** *1 PL: 100 per stk*</span><span class="sxs-lookup"><span data-stu-id="d4167-378">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="d4167-379">Varebeskrivelsen vises også.</span><span class="sxs-lookup"><span data-stu-id="d4167-379">The item description is also shown.</span></span>

1. <span data-ttu-id="d4167-380">Bekreft plasseringsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="d4167-380">Confirm the putaway work.</span></span>

    <span data-ttu-id="d4167-381">På **Oppgave**-siden for bestillingslinjemottak vises meldingen "Arbeid fullført".</span><span class="sxs-lookup"><span data-stu-id="d4167-381">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="d4167-382">**LINENUM**-feltet er tilgjengelig, slik at du kan begynne å motta den neste pallen.</span><span class="sxs-lookup"><span data-stu-id="d4167-382">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

1. <span data-ttu-id="d4167-383">Velg menyknappen (**≡**) øverst på siden, og velg deretter **Avbryt** for å gå tilbake til menyen.</span><span class="sxs-lookup"><span data-stu-id="d4167-383">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Cancel** to return to the menu.</span></span>

<span data-ttu-id="d4167-384">Du kan nå lukke mobilappen.</span><span class="sxs-lookup"><span data-stu-id="d4167-384">You can now close the mobile app.</span></span>
