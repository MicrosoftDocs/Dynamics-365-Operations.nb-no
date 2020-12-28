---
title: Gruppestilling full
description: Dette emnet inneholder informasjon om funksjonen Gruppeposisjon full. Denne funksjonen gir et alternativ til mer rigid håndhevelse av arbeidsstoppregler når gruppueplukking brukes, ettersom det muliggjør en større margin med feil i de volumetriske begrensningene i beholdere eller transportkasser.
author: Mirzaab
manager: tfehr
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3610725815b35609ee98b69b367db2945bbf166a
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434768"
---
# <a name="cluster-position-full"></a><span data-ttu-id="a7f89-104">Gruppestilling full</span><span class="sxs-lookup"><span data-stu-id="a7f89-104">Cluster position full</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7f89-105">Funksjonen *Gruppeposisjon full* gir et alternativ til mer rigid håndhevelse av arbeidsstoppregler når gruppeplukking brukes, ettersom det muliggjør en større margin med feil i de volumetriske begrensningene i beholdere eller transportkasser.</span><span class="sxs-lookup"><span data-stu-id="a7f89-105">The *Cluster position full* feature offers an alternative to more rigid enforcement of work break rules when cluster picking is used, because it enables a larger margin of error in the volumetric constraints of containers or totes.</span></span> <span data-ttu-id="a7f89-106">I et vanlig scenario vil ikke alle varer i en arbeidsordre få plass i en valgt beholder.</span><span class="sxs-lookup"><span data-stu-id="a7f89-106">In a common scenario, not all items on a work order fit into a selected container.</span></span> <span data-ttu-id="a7f89-107">Lagerarbeidere som plukker i grupper, har få alternativer i dette scenarioet: de må enten endre til en større beholderstørrelse, eller samarbeide med sin overordnede for å finne en annen løsning.</span><span class="sxs-lookup"><span data-stu-id="a7f89-107">Warehouse workers who are cluster picking have few options in this scenario: they must either change to a larger container size or work with their supervisor to come up with a different solution.</span></span>

<span data-ttu-id="a7f89-108">Denne funksjonen gir mulighet til å kjøre knappen **Full** på en av arbeidsenhetene i en gruppe.</span><span class="sxs-lookup"><span data-stu-id="a7f89-108">This feature introduces the ability to run the **Full** button on one of the work units in a cluster.</span></span> <span data-ttu-id="a7f89-109">I eldre versjoner var dette alternativet bare tilgjengelig for vanlig ordreplukking, ikke for gruppeplukking.</span><span class="sxs-lookup"><span data-stu-id="a7f89-109">In older versions, this option was available only for regular order picking, not for cluster picking.</span></span> <span data-ttu-id="a7f89-110">Denne funksjonen er imidlertid forskjellig fra standardknappen **Full** ved at den avbryter det gjenstående arbeidet.</span><span class="sxs-lookup"><span data-stu-id="a7f89-110">However, this feature differs from the standard **Full** button in that it cancels the remaining work.</span></span> <span data-ttu-id="a7f89-111">Den foreslår ikke at brukeren legger til en ny hylle i den samme gruppen, og den oppretter ikke automatisk nytt arbeid.</span><span class="sxs-lookup"><span data-stu-id="a7f89-111">It doesn't suggest that the user add another bin to the same cluster, and it doesn't automatically create new work.</span></span>

## <a name="turn-on-the-cluster-position-full-feature"></a><span data-ttu-id="a7f89-112">Aktivere funksjonen Gruppeposisjon full</span><span class="sxs-lookup"><span data-stu-id="a7f89-112">Turn on the Cluster position full feature</span></span>

<span data-ttu-id="a7f89-113">Før du kan bruke denne funksjonen, må den være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="a7f89-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="a7f89-114">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den.</span><span class="sxs-lookup"><span data-stu-id="a7f89-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="a7f89-115">I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="a7f89-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a7f89-116">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="a7f89-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a7f89-117">**Funksjonsnavn:** *Gruppeposisjon full*</span><span class="sxs-lookup"><span data-stu-id="a7f89-117">**Feature name:** *Cluster position full*</span></span>

## <a name="setup"></a><span data-ttu-id="a7f89-118">Installasjon</span><span class="sxs-lookup"><span data-stu-id="a7f89-118">Setup</span></span>

<span data-ttu-id="a7f89-119">Denne delen inneholder retningslinjer, og et eksempel som viser hvordan du definerer og bruker funksjonen *Gruppeposisjon full*.</span><span class="sxs-lookup"><span data-stu-id="a7f89-119">This section provides guidelines, and an example that shows how to set up and use the *Cluster position full* feature.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="a7f89-120">Gjøre eksempeldata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="a7f89-120">Make sample data available</span></span>

<span data-ttu-id="a7f89-121">For å arbeide deg gjennom dette [eksempelscenarioet](#example-scenario) ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert.</span><span class="sxs-lookup"><span data-stu-id="a7f89-121">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="a7f89-122">Du må også velge den juridiske enheten **USMF** før du begynner.</span><span class="sxs-lookup"><span data-stu-id="a7f89-122">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="a7f89-123">Du kan også bruke dette eksempelscenarioet som en veiledning for å bruke denne funksjonen i et produksjonssystem.</span><span class="sxs-lookup"><span data-stu-id="a7f89-123">You can also use the example scenario as guidance for working with this feature on a production system.</span></span> <span data-ttu-id="a7f89-124">I så fall må du imidlertid bytte dine egne verdier for innstillingene som beskrives her.</span><span class="sxs-lookup"><span data-stu-id="a7f89-124">However, in that case, you must substitute your own values for the settings that are described here.</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="a7f89-125">Gruppeprofiler</span><span class="sxs-lookup"><span data-stu-id="a7f89-125">Cluster profiles</span></span>

<span data-ttu-id="a7f89-126">Du må angi om gruppe-ID-er skal genereres automatisk, hvor mange stillinger som brukes, når sektorgrupper brytes og hvordan plukkarbeidet blir sekvensiert og verifisert.</span><span class="sxs-lookup"><span data-stu-id="a7f89-126">You must specify whether cluster IDs are automatically generated, how many positions are used, when clusters are broken, and how the picking work is sequenced and verified.</span></span>

1. <span data-ttu-id="a7f89-127">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Gruppeprofiler**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-127">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="a7f89-128">I listeruten velger du posten **Opprett gruppe**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-128">In the list pane, select the **Create Cluster** record.</span></span>
1. <span data-ttu-id="a7f89-129">Bekreft følgende verdier i hurtigkategorin **Generelt**:</span><span class="sxs-lookup"><span data-stu-id="a7f89-129">On the **General** FastTab, verify the following values:</span></span>

    - <span data-ttu-id="a7f89-130">**Generer gruppe-ID:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="a7f89-130">**Generate cluster ID:** *Yes*</span></span>
    - <span data-ttu-id="a7f89-131">**Aktiver stillinger:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="a7f89-131">**Activate positions:** *Yes*</span></span>
    - <span data-ttu-id="a7f89-132">**Antall stillinger:** *2*</span><span class="sxs-lookup"><span data-stu-id="a7f89-132">**Number of positions:** *2*</span></span>
    - <span data-ttu-id="a7f89-133">**Stillingsnavn:** *Numerisk*</span><span class="sxs-lookup"><span data-stu-id="a7f89-133">**Position name:** *Numeric*</span></span>
    - <span data-ttu-id="a7f89-134">**Bryt opp gruppe ved:** *Plasser*</span><span class="sxs-lookup"><span data-stu-id="a7f89-134">**Break cluster at:** *Put*</span></span>
    - <span data-ttu-id="a7f89-135">**Type sorteringsbekreftelse:** *Posisjonsskanning*</span><span class="sxs-lookup"><span data-stu-id="a7f89-135">**Sort verification type:** *Position scan*</span></span>

1. <span data-ttu-id="a7f89-136">I hurtigkategorin **Gruppesortering**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-136">In the **Cluster sorting** FastTab.</span></span> <span data-ttu-id="a7f89-137">Rutenettet bør være tomt (det vil si at det ikke inneholder linjer).</span><span class="sxs-lookup"><span data-stu-id="a7f89-137">The grid should be blank (that is, it should contain no lines).</span></span>

### <a name="work-templates"></a><span data-ttu-id="a7f89-138">Arbeidsmaler</span><span class="sxs-lookup"><span data-stu-id="a7f89-138">Work templates</span></span>

<span data-ttu-id="a7f89-139">Du må definere hvordan plukkarbeidet for gruppeplukking opprettes.</span><span class="sxs-lookup"><span data-stu-id="a7f89-139">You must define how the picking work for cluster picking is created.</span></span>

1. <span data-ttu-id="a7f89-140">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-140">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="a7f89-141">Øverst på siden setter du feltet **Arbeidsordretype** til *Salgsordrer*.</span><span class="sxs-lookup"><span data-stu-id="a7f89-141">At the top of the page, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="a7f89-142">Kontroller at følgende arbeidsmaler fra demonstrasjonsdataene er oppført.</span><span class="sxs-lookup"><span data-stu-id="a7f89-142">Make sure that the following work templates from the demo data are listed.</span></span> <span data-ttu-id="a7f89-143">Hvis de ikke er tilgjengelige, kan du ikke fullføre scenarioet.</span><span class="sxs-lookup"><span data-stu-id="a7f89-143">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="a7f89-144">61 SO Stadium</span><span class="sxs-lookup"><span data-stu-id="a7f89-144">61 SO Stage</span></span>
    - <span data-ttu-id="a7f89-145">61 SO Gruppeplukking</span><span class="sxs-lookup"><span data-stu-id="a7f89-145">61 SO Cluster pick</span></span>

### <a name="location-directives"></a><span data-ttu-id="a7f89-146">Lokasjonsdirektiver</span><span class="sxs-lookup"><span data-stu-id="a7f89-146">Location directives</span></span>

<span data-ttu-id="a7f89-147">Du må angi hvor varene skal plukkes fra og hvor de blir plassert.</span><span class="sxs-lookup"><span data-stu-id="a7f89-147">You must specify where items are picked from and where they are put.</span></span>

1. <span data-ttu-id="a7f89-148">Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-148">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="a7f89-149">I listetoppteksten setter du feltet *Arbeidsordretype* til **Salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-149">In the list header, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="a7f89-150">Kontroller at følgende salgsordredirektivene fra demonstrasjonsdataene er oppført.</span><span class="sxs-lookup"><span data-stu-id="a7f89-150">Make sure that the following sales order directives from the demo data are listed.</span></span> <span data-ttu-id="a7f89-151">Hvis de ikke er tilgjengelige, kan du ikke fullføre scenarioet.</span><span class="sxs-lookup"><span data-stu-id="a7f89-151">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="a7f89-152">61 Gruppeplukking</span><span class="sxs-lookup"><span data-stu-id="a7f89-152">61 Cluster pick</span></span>
    - <span data-ttu-id="a7f89-153">61 SO Plukkordre</span><span class="sxs-lookup"><span data-stu-id="a7f89-153">61 SO Pick order</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="a7f89-154">Menyelementer på mobilenheten</span><span class="sxs-lookup"><span data-stu-id="a7f89-154">Mobile device menu items</span></span>

<span data-ttu-id="a7f89-155">Du må konfigurere et menyelement for mobilenhet til å bruke eksisterende arbeid styres av gruppeplukking.</span><span class="sxs-lookup"><span data-stu-id="a7f89-155">You must configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="a7f89-156">I menyelementet for mobilenhet for gruppeplukking må parameteren **Tillat arbeidsoppdeling** være aktivert, og arbeidsklassen *Salgsordreplukking* må legges til.</span><span class="sxs-lookup"><span data-stu-id="a7f89-156">In the mobile device menu item for cluster picking, the **Allow splitting of work** parameter must be turned on, and the *SO Pick* work class must be added.</span></span>

1. <span data-ttu-id="a7f89-157">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-157">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="a7f89-158">I listeruten velger du posten **Oppretting av gruppeplukking**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-158">In the list pane, select the **Cluster Pick Create** record.</span></span>
1. <span data-ttu-id="a7f89-159">Velg **Rediger** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a7f89-159">Select **Edit** in the Action pane.</span></span>
1. <span data-ttu-id="a7f89-160">Angi følgende verdier i **Generelt**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="a7f89-160">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="a7f89-161">**Styrt av:** *Gruppeplukking*</span><span class="sxs-lookup"><span data-stu-id="a7f89-161">**Directed by:** *Cluster picking*</span></span>
    - <span data-ttu-id="a7f89-162">**Generer nummerskilt:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="a7f89-162">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="a7f89-163">**Tillat arbeidsoppdeling:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="a7f89-163">**Allow splitting of work:** *Yes*</span></span>
    - <span data-ttu-id="a7f89-164">**ID for gruppeprofil:** *Opprett gruppe*</span><span class="sxs-lookup"><span data-stu-id="a7f89-164">**Cluster profile ID:** *Create Cluster*</span></span>

    <span data-ttu-id="a7f89-165">Godta standardverdiene for alle de andre feltene.</span><span class="sxs-lookup"><span data-stu-id="a7f89-165">Accept the default values for all other fields.</span></span>

1. <span data-ttu-id="a7f89-166">I hurtigkategorin **Arbeidsklasser** legger du til følgende to linjer etter behov:</span><span class="sxs-lookup"><span data-stu-id="a7f89-166">On the **Work classes** FastTab, add the following two lines, as required:</span></span>

    - <span data-ttu-id="a7f89-167">Linje 1 (finnes vanligvis i demodata):</span><span class="sxs-lookup"><span data-stu-id="a7f89-167">Line 1 (usually present in demo data):</span></span>

        - <span data-ttu-id="a7f89-168">**Arbeidsklasse-ID:** *Salg*</span><span class="sxs-lookup"><span data-stu-id="a7f89-168">**Work class ID:** *Sales*</span></span> 
        - <span data-ttu-id="a7f89-169">**Arbeidsordretype:** *Salgsordrer*</span><span class="sxs-lookup"><span data-stu-id="a7f89-169">**Work order type:** *Sales orders*</span></span>

    - <span data-ttu-id="a7f89-170">Linje 2 (finnes sannsynligvis ikke i demodata):</span><span class="sxs-lookup"><span data-stu-id="a7f89-170">Line 2 (probably not present in demo data):</span></span>

        - <span data-ttu-id="a7f89-171">**Arbeidsklasse-ID:** *Salgsordreplukking*</span><span class="sxs-lookup"><span data-stu-id="a7f89-171">**Work class ID:** *SO Pick*</span></span>
        - <span data-ttu-id="a7f89-172">**Arbeidsordretype:** *Salgsordrer*</span><span class="sxs-lookup"><span data-stu-id="a7f89-172">**Work order type:** *Sales orders*</span></span>

1. <span data-ttu-id="a7f89-173">Gå til **Arbeidsbekreftelsesoppsett** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a7f89-173">Go to **Work confirmation setup** in the Action pane.</span></span>
1. <span data-ttu-id="a7f89-174">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-174">Select **Edit**.</span></span>
1. <span data-ttu-id="a7f89-175">Angi følgende verdier på linjen i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="a7f89-175">Enter the following values on the line in grid.</span></span>
    - <span data-ttu-id="a7f89-176">**Arbeidstype** - *Plukking*</span><span class="sxs-lookup"><span data-stu-id="a7f89-176">**Work type** - *Pick*</span></span>
    - <span data-ttu-id="a7f89-177">**Produktbekreftelse** - *Merk av i avmerkingsboksen*</span><span class="sxs-lookup"><span data-stu-id="a7f89-177">**Product confirmation** - *Select the check box*</span></span>

1. <span data-ttu-id="a7f89-178">Velg **Lagre** i handlingsruten og lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a7f89-178">Select **Save** in the Action pane and close the page.</span></span>

## <a name="create-picking-work"></a><span data-ttu-id="a7f89-179">Opprett plukkarbeid</span><span class="sxs-lookup"><span data-stu-id="a7f89-179">Create picking work</span></span>

<span data-ttu-id="a7f89-180">Før du kan starte gruppeplukking, må du opprette noe utgående arbeid.</span><span class="sxs-lookup"><span data-stu-id="a7f89-180">Before you can start cluster picking, you must create some outbound work.</span></span> <span data-ttu-id="a7f89-181">Gruppeprofilen du opprettet tidligere, angir to gruppestillinger.</span><span class="sxs-lookup"><span data-stu-id="a7f89-181">The cluster profile that you created earlier specifies two cluster positions.</span></span> <span data-ttu-id="a7f89-182">Det må derfor opprettes minst to arbeids-ID-er for plukking av salgsordre.</span><span class="sxs-lookup"><span data-stu-id="a7f89-182">Therefore, at least two work IDs must be created for sales order picking.</span></span> <span data-ttu-id="a7f89-183">I dette scenarioet vil det oppstå transaksjoner i lager *61*, og de vil bruke varene *L0101* og *T0100*.</span><span class="sxs-lookup"><span data-stu-id="a7f89-183">For this scenario, transactions will occur in warehouse *61*, and they will use items *L0101* and *T0100*.</span></span> <span data-ttu-id="a7f89-184">Demonstrasjonsdataene bør ha tilstrekkelig lagerbeholdning av disse varene.</span><span class="sxs-lookup"><span data-stu-id="a7f89-184">The demo data should have enough on-hand inventory of these items.</span></span> <span data-ttu-id="a7f89-185">Kontroller at du har tilstrekkelig beholdning til å fullføre transaksjonene.</span><span class="sxs-lookup"><span data-stu-id="a7f89-185">Make sure that you have enough inventory to complete the transactions.</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="a7f89-186">Opprett salgsordre 1</span><span class="sxs-lookup"><span data-stu-id="a7f89-186">Create sales order 1</span></span>

1. <span data-ttu-id="a7f89-187">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-187">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a7f89-188">Velg **Ny** for å opprette salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="a7f89-188">Select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="a7f89-189">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a7f89-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a7f89-190">**Kundekonto:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="a7f89-190">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="a7f89-191">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="a7f89-191">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="a7f89-192">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-192">Select **OK**.</span></span>
1. <span data-ttu-id="a7f89-193">Den nye salgsordren åpnes.</span><span class="sxs-lookup"><span data-stu-id="a7f89-193">The new sales order is opened.</span></span> <span data-ttu-id="a7f89-194">På hurtigfanen **Salgsordrelinjer** legger du til en linje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="a7f89-194">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="a7f89-195">**Varenummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="a7f89-195">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="a7f89-196">**Antall:** *5*</span><span class="sxs-lookup"><span data-stu-id="a7f89-196">**Quantity:** *5*</span></span>

1. <span data-ttu-id="a7f89-197">På hurtigkategorin **Linjedetaljer** i kategorien **Levering** setter du verdien for feltet **Bekreftet forsendelsesdato** til dagens dato.</span><span class="sxs-lookup"><span data-stu-id="a7f89-197">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="a7f89-198">I hurtigkategorien **Salgsordrelinjer** legger du til ytterligere en linje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="a7f89-198">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="a7f89-199">**Varenummer:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="a7f89-199">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="a7f89-200">**Antall:** *20*</span><span class="sxs-lookup"><span data-stu-id="a7f89-200">**Quantity:** *20*</span></span>

1. <span data-ttu-id="a7f89-201">På hurtigkategorin **Linjedetaljer** i kategorien **Levering** setter du verdien for feltet **Bekreftet forsendelsesdato** til dagens dato.</span><span class="sxs-lookup"><span data-stu-id="a7f89-201">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="a7f89-202">For hver linje du legger til, kan du følge denne fremgangsmåten for å reservere lager:</span><span class="sxs-lookup"><span data-stu-id="a7f89-202">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="a7f89-203">Velg linjen som skal reserveres.</span><span class="sxs-lookup"><span data-stu-id="a7f89-203">Select the line to reserve.</span></span>
    2. <span data-ttu-id="a7f89-204">På hurtigfanen **Salgsordrelinjer** velger du **Beholdning \> Reservasjon**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-204">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="a7f89-205">På **Reservasjon**-siden, i handlingspanelet, velger du **Reserver parti** for å reservere lageret.</span><span class="sxs-lookup"><span data-stu-id="a7f89-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="a7f89-206">Lukk **Reservasjon**-siden.</span><span class="sxs-lookup"><span data-stu-id="a7f89-206">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="a7f89-207">Velg **Frigi til lager** i kategorien **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a7f89-207">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="a7f89-208">Når frigivelsen er fullført, mottar du informasjonsmeldinger som viser bølge- og last-ID-er som ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="a7f89-208">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="a7f89-209">Opprett salgsordre 2</span><span class="sxs-lookup"><span data-stu-id="a7f89-209">Create sales order 2</span></span>

1. <span data-ttu-id="a7f89-210">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-210">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a7f89-211">Velg **Ny** for å opprette salgsordre 2.</span><span class="sxs-lookup"><span data-stu-id="a7f89-211">Select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="a7f89-212">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a7f89-212">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a7f89-213">**Kundekonto:** *US-011*</span><span class="sxs-lookup"><span data-stu-id="a7f89-213">**Customer account:** *US-011*</span></span>
    - <span data-ttu-id="a7f89-214">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="a7f89-214">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="a7f89-215">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-215">Select **OK**.</span></span>
1. <span data-ttu-id="a7f89-216">Den nye salgsordren åpnes.</span><span class="sxs-lookup"><span data-stu-id="a7f89-216">The new sales order is opened.</span></span> <span data-ttu-id="a7f89-217">På hurtigfanen **Salgsordrelinjer** legger du til en linje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="a7f89-217">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="a7f89-218">**Varenummer:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="a7f89-218">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="a7f89-219">**Antall:** *20*</span><span class="sxs-lookup"><span data-stu-id="a7f89-219">**Quantity:** *20*</span></span>

1. <span data-ttu-id="a7f89-220">På hurtigkategorin **Linjedetaljer** i kategorien **Levering** setter du verdien for feltet **Bekreftet forsendelsesdato** til dagens dato.</span><span class="sxs-lookup"><span data-stu-id="a7f89-220">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="a7f89-221">I hurtigkategorien **Salgsordrelinjer** legger du til ytterligere en linje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="a7f89-221">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="a7f89-222">**Varenummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="a7f89-222">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="a7f89-223">**Antall:** *2*</span><span class="sxs-lookup"><span data-stu-id="a7f89-223">**Quantity:** *2*</span></span>

1. <span data-ttu-id="a7f89-224">På hurtigkategorin **Linjedetaljer** i kategorien **Levering** setter du verdien for feltet **Bekreftet forsendelsesdato** til dagens dato.</span><span class="sxs-lookup"><span data-stu-id="a7f89-224">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="a7f89-225">For hver linje du legger til, kan du følge denne fremgangsmåten for å reservere lager:</span><span class="sxs-lookup"><span data-stu-id="a7f89-225">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="a7f89-226">Velg linjen som skal reserveres.</span><span class="sxs-lookup"><span data-stu-id="a7f89-226">Select the line to reserve.</span></span>
    2. <span data-ttu-id="a7f89-227">På hurtigfanen **Salgsordrelinjer** velger du **Beholdning \> Reservasjon**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-227">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="a7f89-228">På **Reservasjon**-siden, i handlingspanelet, velger du **Reserver parti** for å reservere lageret.</span><span class="sxs-lookup"><span data-stu-id="a7f89-228">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="a7f89-229">Lukk **Reservasjon**-siden.</span><span class="sxs-lookup"><span data-stu-id="a7f89-229">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="a7f89-230">Velg **Frigi til lager** i kategorien **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a7f89-230">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="a7f89-231">Når frigivelsen er fullført, mottar du informasjonsmeldinger som viser bølge- og last-ID-er som ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="a7f89-231">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="get-work-ids-and-license-plate-numbers"></a><span data-ttu-id="a7f89-232">Hent arbeids-ID-er og nummerskilt</span><span class="sxs-lookup"><span data-stu-id="a7f89-232">Get work IDs and license plate numbers</span></span>

<span data-ttu-id="a7f89-233">To arbeids-ID-er bør være opprettet, og hver av dem har to plukklinjer.</span><span class="sxs-lookup"><span data-stu-id="a7f89-233">Two work IDs should have been created, each of which has two pick lines.</span></span> <span data-ttu-id="a7f89-234">Følg denne fremgangsmåten for å finne arbeids-ID-ene og nummerskilttilordningene.</span><span class="sxs-lookup"><span data-stu-id="a7f89-234">Follow these steps to find the work IDs and license plate assignments.</span></span>

1. <span data-ttu-id="a7f89-235">Gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-235">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="a7f89-236">I rutenettet **Oversikt** søker du i kolonnen **Ordrenummer** etter de to salgsordrene du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="a7f89-236">In the **Overview** grid, search the **Order number** column for the two sales orders that you just created.</span></span> <span data-ttu-id="a7f89-237">For hver salgsordre noterer du den tilsvarende arbeids-ID-en.</span><span class="sxs-lookup"><span data-stu-id="a7f89-237">For each sales order, make a note of the corresponding work ID.</span></span>
1. <span data-ttu-id="a7f89-238">Velg raden for hver salgsordre for å vise relatert informasjon i rutenettet **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-238">Select the row for each sales order to show related information in the **Lines** grid.</span></span> <span data-ttu-id="a7f89-239">Noter deg hvor hver vare blir plukket fra.</span><span class="sxs-lookup"><span data-stu-id="a7f89-239">Make a note of the location that each item will be picked from.</span></span>
1. <span data-ttu-id="a7f89-240">Gå til **Lagerstyring \> Forespørsler og rapporter \> Beholdningsliste**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-240">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="a7f89-241">I handlingsruten velger du **Dimensjoner** for å åpne dialogboksen **Dimensjonsvisning**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-241">On the Action Pane, select **Dimensions** to open the **Dimension display** dialog box.</span></span>
1. <span data-ttu-id="a7f89-242">Kontroller at det er merket av for **Nummerskilt**, **Lager** og **Varenummer**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-242">Make sure that the **License plate**, **Warehouse**, and **Item number** check boxes are selected, and then select **OK**.</span></span>
1. <span data-ttu-id="a7f89-243">Angi følgende filtre i ruten **Filter**:</span><span class="sxs-lookup"><span data-stu-id="a7f89-243">In the **Filter** pane, set the following filters:</span></span>

    - <span data-ttu-id="a7f89-244">**Varenummer** – **er enten** – *L0101* eller *T100*</span><span class="sxs-lookup"><span data-stu-id="a7f89-244">**Item number** – **is one of** – *L0101* and *T100*</span></span>
    - <span data-ttu-id="a7f89-245">**Lager** – **starter med** – *61*</span><span class="sxs-lookup"><span data-stu-id="a7f89-245">**Warehouse** – **begins with** – *61*</span></span>

1. <span data-ttu-id="a7f89-246">Noter deg verdiene for **Nummerskilt** som vises.</span><span class="sxs-lookup"><span data-stu-id="a7f89-246">Make a note of the **License plate** values that are shown.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="a7f89-247">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="a7f89-247">Example scenario</span></span>

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a><span data-ttu-id="a7f89-248">Flytutføring for mobilenhet – behandling av arbeidsbekreftelse for produktet</span><span class="sxs-lookup"><span data-stu-id="a7f89-248">Mobile device flow execution – Work confirmation setup for the product</span></span>

1. <span data-ttu-id="a7f89-249">Logg på lagerappen som en bruker på lageret *61*.</span><span class="sxs-lookup"><span data-stu-id="a7f89-249">Sign in to the warehouse app as a user in warehouse *61*.</span></span>
1. <span data-ttu-id="a7f89-250">Gå til **Utgående \> Oppretting av gruppeplukking**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-250">Go to **Outbound \> Cluster pick create**.</span></span>

    <span data-ttu-id="a7f89-251">Siden **OPPGAVE: Tilordne arbeid til gruppe** vises.</span><span class="sxs-lookup"><span data-stu-id="a7f89-251">The **TASK: Assign work to Cluster** page appears.</span></span>

1. <span data-ttu-id="a7f89-252">Angi arbeids-ID-en for salgsordre 1 for å tilordne den til gruppeposisjon 1.</span><span class="sxs-lookup"><span data-stu-id="a7f89-252">Enter the work ID for sales order 1 to assign it to cluster position 1.</span></span>
1. <span data-ttu-id="a7f89-253">Velg **OK** (hakesymbol).</span><span class="sxs-lookup"><span data-stu-id="a7f89-253">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a7f89-254">Angi arbeids-ID-en for salgsordre 2 for å tilordne den til gruppeposisjon 2.</span><span class="sxs-lookup"><span data-stu-id="a7f89-254">Enter the work ID for sales order 2 to assign it to cluster position 2.</span></span>
1. <span data-ttu-id="a7f89-255">Velg **OK** (hakesymbol).</span><span class="sxs-lookup"><span data-stu-id="a7f89-255">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="a7f89-256">Siden **OPPGAVE: Oppretting av gruppeplukking: Plukk** vises med *Vare L0101 2 PL*.</span><span class="sxs-lookup"><span data-stu-id="a7f89-256">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item L0101 2 PL*.</span></span>

<span data-ttu-id="a7f89-257">Ettersom gruppeprofilen setter antall posisjoner til 2, vil systemet automatisk omdirigere deg til den første konsolideringplukkingen: to paller (PL) av varen *L0101*.</span><span class="sxs-lookup"><span data-stu-id="a7f89-257">Because the cluster profile set the number of positions to 2, the system automatically directs you to the first consolidate pick: two pallets (PL) of item *L0101*.</span></span>

<span data-ttu-id="a7f89-258">Når som helst i trinnene nedenfor kan du velge kategorien **Detaljer** for å vise mer informasjon om oppgaven, for eksempel plukklokasjon.</span><span class="sxs-lookup"><span data-stu-id="a7f89-258">At any time during the following steps, you can select the **Details** tab to view additional information about the task, such as the picking location.</span></span>

1. <span data-ttu-id="a7f89-259">Sett verdien i feltet **VARE** til *L0101*.</span><span class="sxs-lookup"><span data-stu-id="a7f89-259">Set the **ITEM** field to *L0101*.</span></span> <span data-ttu-id="a7f89-260">Dette bekrefter varenummeret, som er nødvendig for dette menyelementet (du konfigurerte dette tidligere ved å velge **Arbeidsbekreftelsesoppsett** på siden **Menyelement for mobilenhet** da du opprettet dette menyelementet).</span><span class="sxs-lookup"><span data-stu-id="a7f89-260">This confirms the item number, which is required for this menu item (you configured this earlier by selecting **Work confirmation setup**  from the **Mobile device menu item** page when you created this menu item).</span></span>
1. <span data-ttu-id="a7f89-261">Angi nummerskiltet som er knyttet til varen på lokasjonen som blir plukket.</span><span class="sxs-lookup"><span data-stu-id="a7f89-261">Enter the license plate number that is associated with the item in the location that is being picked.</span></span> <span data-ttu-id="a7f89-262">Du skal plukke to paller.</span><span class="sxs-lookup"><span data-stu-id="a7f89-262">You will pick two pallets.</span></span>
1. <span data-ttu-id="a7f89-263">Sett verdien i feltet **LP** til *LP\_PLUKK\_01*.</span><span class="sxs-lookup"><span data-stu-id="a7f89-263">Set the **LP** field to *LP\_PICK\_01*.</span></span>
1. <span data-ttu-id="a7f89-264">Velg **OK** (hakesymbol).</span><span class="sxs-lookup"><span data-stu-id="a7f89-264">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="a7f89-265">Siden **OPPGAVE: Sortere: Oppretting av gruppeplukking** vises.</span><span class="sxs-lookup"><span data-stu-id="a7f89-265">The **TASK: Sort: Cluster Pick Create** page appears.</span></span> <span data-ttu-id="a7f89-266">Her skal du sortere de to plukkede pallene til en plukkposisjon.</span><span class="sxs-lookup"><span data-stu-id="a7f89-266">Here, you will sort the two picked pallets into a pick position.</span></span> <span data-ttu-id="a7f89-267">Denne posisjonen kan være en transportkasse eller en beholder som brukes til å skille den plukkede beholdningen etter salgsordre.</span><span class="sxs-lookup"><span data-stu-id="a7f89-267">This position might be a tote or container that is used to separate the picked inventory by sales order.</span></span>

1. <span data-ttu-id="a7f89-268">Vis detaljene som vises for varen (*L0101*) og antallet (*20* EA) som skal sorteres i posisjon 1 (for salgsordre 1).</span><span class="sxs-lookup"><span data-stu-id="a7f89-268">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="a7f89-269">Sett feltet **POSISJONSNAVN** til *1*.</span><span class="sxs-lookup"><span data-stu-id="a7f89-269">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="a7f89-270">Velg **OK** (hakesymbol).</span><span class="sxs-lookup"><span data-stu-id="a7f89-270">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a7f89-271">Vis detaljene som vises for varen (*L0101*) og antallet (*20* EA) som skal sorteres i posisjon 2 (for salgsordre 2).</span><span class="sxs-lookup"><span data-stu-id="a7f89-271">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="a7f89-272">Sett feltet **POSISJONSNAVN** til *2*.</span><span class="sxs-lookup"><span data-stu-id="a7f89-272">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="a7f89-273">Velg **OK** (hakesymbol).</span><span class="sxs-lookup"><span data-stu-id="a7f89-273">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="a7f89-274">Siden **OPPGAVE: Oppretting av gruppeplukking: Plukk** vises med *Vare T0100 7 EA*.</span><span class="sxs-lookup"><span data-stu-id="a7f89-274">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item T0100 7 ea*.</span></span>

<span data-ttu-id="a7f89-275">I dette scenarioet kan ikke posisjon 1 godta hele antallet varer som må plukkes for å oppfylle salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="a7f89-275">In this scenario, position 1 can't accept the full quantity of items that must be picked to fulfill sales order 1.</span></span> <span data-ttu-id="a7f89-276">En posisjon må merkes som full.</span><span class="sxs-lookup"><span data-stu-id="a7f89-276">A position must be marked as full.</span></span> <span data-ttu-id="a7f89-277">I dette scenarioet skal du utføre en delvis plukking av den andre varen.</span><span class="sxs-lookup"><span data-stu-id="a7f89-277">In this scenario, you will do a partial pick of the second item.</span></span> <span data-ttu-id="a7f89-278">Den andre varen plukkes delvis for posisjon 1, og nytt arbeid blir opprettet for å plukke det gjenstående antallet for å oppfylle ordren.</span><span class="sxs-lookup"><span data-stu-id="a7f89-278">The second item will be partially picked for position 1, and new work will be created to pick the remaining quantity to fulfill the order.</span></span>

1. <span data-ttu-id="a7f89-279">Velg menyknappen (noen ganger kalt hamburger eller hamburgerknappen), og velg deretter **Posisjon full**.</span><span class="sxs-lookup"><span data-stu-id="a7f89-279">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Position full**.</span></span>
1. <span data-ttu-id="a7f89-280">Identifiser posisjonen som er full og velg *1*.</span><span class="sxs-lookup"><span data-stu-id="a7f89-280">Identify the position that is full, and select *1*.</span></span>
1. <span data-ttu-id="a7f89-281">Velg **OK** (hakesymbol).</span><span class="sxs-lookup"><span data-stu-id="a7f89-281">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a7f89-282">Angi plukkantallet som fremdeles kan plukkes i posisjon 1.</span><span class="sxs-lookup"><span data-stu-id="a7f89-282">Enter the pick quantity that can still be picked into position 1.</span></span> <span data-ttu-id="a7f89-283">Systemet kan bestemme hvilket varenummer som skal plukkes.</span><span class="sxs-lookup"><span data-stu-id="a7f89-283">The system can determine which item number is being picked.</span></span>
1. <span data-ttu-id="a7f89-284">Angi *2*.</span><span class="sxs-lookup"><span data-stu-id="a7f89-284">Enter *2*.</span></span>
1. <span data-ttu-id="a7f89-285">Velg **OK** (hakesymbol).</span><span class="sxs-lookup"><span data-stu-id="a7f89-285">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a7f89-286">Bekreft at varenummeret skal fullføre plukkingen av den gjenværende varen i posisjon 2.</span><span class="sxs-lookup"><span data-stu-id="a7f89-286">Confirm the item number to complete the pick of the remaining item into position 2.</span></span>
1. <span data-ttu-id="a7f89-287">Sett verdien i feltet **VARE** til *T0100*.</span><span class="sxs-lookup"><span data-stu-id="a7f89-287">Set the **ITEM** field to *T0100*.</span></span>
1. <span data-ttu-id="a7f89-288">Velg **OK** (hakesymbol).</span><span class="sxs-lookup"><span data-stu-id="a7f89-288">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a7f89-289">Angi nummerskiltet som varen blir plukket fra, ved å sette feltet **LP** til *LPREPL04*.</span><span class="sxs-lookup"><span data-stu-id="a7f89-289">Enter the license plate that the item is being picked from by setting the **LP** field to *LPREPL04*.</span></span>
1. <span data-ttu-id="a7f89-290">Velg **OK** (hakesymbol).</span><span class="sxs-lookup"><span data-stu-id="a7f89-290">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a7f89-291">Vis detaljene som vises for varen (*T0100*) og antallet (*2* EA) som skal sorteres i posisjon 2 (for salgsordre 2).</span><span class="sxs-lookup"><span data-stu-id="a7f89-291">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="a7f89-292">Sett feltet **POSISJONSNAVN** til *2*.</span><span class="sxs-lookup"><span data-stu-id="a7f89-292">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="a7f89-293">Velg **OK** (hakesymbol).</span><span class="sxs-lookup"><span data-stu-id="a7f89-293">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a7f89-294">Vis detaljene som vises for varen (*T0100*) og antallet (*2* EA) som skal sorteres i posisjon 1 (for salgsordre 1).</span><span class="sxs-lookup"><span data-stu-id="a7f89-294">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="a7f89-295">Sett feltet **POSISJONSNAVN** til *1*.</span><span class="sxs-lookup"><span data-stu-id="a7f89-295">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="a7f89-296">Velg **OK** (hakesymbol).</span><span class="sxs-lookup"><span data-stu-id="a7f89-296">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="a7f89-297">Siden **OPPGAVE: Oppretting av gruppeplukking: Plassere** vises.</span><span class="sxs-lookup"><span data-stu-id="a7f89-297">The **TASK: Cluster Pick Create: Put** page appears.</span></span>

<span data-ttu-id="a7f89-298">I dette scenarioet er gruppeplukkingen fullført, og brukeren blir omdirigert til å plassere plukkede varer fra posisjon 1 og 2 på oppsamlingslokasjon *STAGE01*.</span><span class="sxs-lookup"><span data-stu-id="a7f89-298">In this scenario, the cluster pick has been completed, and the user is directed to put away the picked items from position 1 and position 2 into staging location *STAGE01*.</span></span>

1. <span data-ttu-id="a7f89-299">Gå gjennom informasjonen på siden.</span><span class="sxs-lookup"><span data-stu-id="a7f89-299">Review the information on the page.</span></span> <span data-ttu-id="a7f89-300">Det viser at et totalt antall på *44* vil bli lagt til på oppsamlingslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="a7f89-300">It shows that a total quantity of *44* will be put to the staging location.</span></span>
1. <span data-ttu-id="a7f89-301">Velg **OK** (hakesymbol).</span><span class="sxs-lookup"><span data-stu-id="a7f89-301">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="a7f89-302">Du mottar meldingen Gruppe fullført.</span><span class="sxs-lookup"><span data-stu-id="a7f89-302">You receive a "Cluster Completed" message.</span></span>

<span data-ttu-id="a7f89-303">Du kan nå bruke menyelementet **Salgsplukking** til å plukke restantallet.</span><span class="sxs-lookup"><span data-stu-id="a7f89-303">You can now use the **Sales Picking** menu item to pick the remaining quantity.</span></span> <span data-ttu-id="a7f89-304">Du kan deretter bruke menyelementet **Salgslasting** til å flytte varene fra lokasjonsplasseringen til lasterampen.</span><span class="sxs-lookup"><span data-stu-id="a7f89-304">You can then use the **Sales loading** menu item to move the items from the staging location to the loading dock.</span></span>
