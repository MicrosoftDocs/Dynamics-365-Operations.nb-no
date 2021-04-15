---
title: Etterfylling av soneterskel
description: Sonebasert etterfylling bruker en minimum/maksimum (min./maks.) etterfyllingsstrategi, men evaluerer hele lagersoner i stedet for bare for enkeltlokasjoner. Derfor kan lagerledere raskere finne ut når det er behov for tilleggsbeholdning i en plukksone.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d0a97ed7b01a32e9276433713448a672f83f7d02
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814374"
---
# <a name="zone-threshold-replenishment"></a><span data-ttu-id="fc9ae-104">Etterfylling av soneterskel</span><span class="sxs-lookup"><span data-stu-id="fc9ae-104">Zone threshold replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc9ae-105">Sonebasert etterfylling bruker en minimum/maksimum (min./maks.) [etterfyllingsstrategi](replenishment.md), men evaluerer hele lagersoner i stedet for bare for enkeltlokasjoner.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-105">Zone-based replenishment uses a minimum/maximum (min/max) [replenishment](replenishment.md) strategy, but it evaluates whole warehouse zones instead of just individual locations.</span></span> <span data-ttu-id="fc9ae-106">Derfor kan lagerledere raskere finne ut når det er behov for tilleggsbeholdning i en plukksone.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-106">Therefore, warehouse managers can more quickly learn when additional inventory is required in a picking zone.</span></span>

<span data-ttu-id="fc9ae-107">Oppsettet for denne funksjonen ligner på oppsettet for lokasjonsbasert etterfylling.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-107">The setup for this feature resembles the setup for location-based replenishment.</span></span> <span data-ttu-id="fc9ae-108">Når du definerer en mal for min./maks. etterfylling, kan du imidlertid også angi om terskelen skal evalueres per lokasjon eller per sone.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-108">However, when you set up a template for min/max replenishment, you can also specify whether the threshold should be evaluated per location or per zone.</span></span> <span data-ttu-id="fc9ae-109">Hvis du definerer evaluering som er basert på soner, må du legge til bestemte soner i sonevalgspørringen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-109">If you set up evaluation that is based on zones, you must add specific zones to the zone selection query.</span></span>

<span data-ttu-id="fc9ae-110">Som lokasjonsbasert min./maks. etterfylling er sonebasert min./maks. etterfylling basert på oppsettet av en minimums beholdningsterskelen som utløser oppretting av etterfyllingsarbeid for utvalgte varer.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-110">Like location-based min/max replenishment, zone-based min/max replenishment is based the setup of a minimum inventory threshold that triggers the creation of replenishment work for selected items.</span></span> <span data-ttu-id="fc9ae-111">Dette etterfyllingsarbeidet øker beholdningen til den angitte maksimumsterskelen for sonen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-111">This replenishment work will increase inventory up to the specified maximum threshold for the zone.</span></span>

> [!NOTE]
> <span data-ttu-id="fc9ae-112">Prosesser for soneetterfylling for produktvarianter støttes ikke i den gjeldende versjonen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-112">Zone replenishment processes for product variants aren't supported in the current release.</span></span>


<span data-ttu-id="fc9ae-113">Til forskjell fra den lokasjonsbaserte min./maks. etterfyllingen må ikke sonebasert min./maks. etterfylling være faste lokasjoner for å vurdere om lokasjoner skal lagre en bestemt vare.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-113">Unlike location-based min/max replenishment, zone-based min/max replenishment doesn't require fixed locations to evaluate whether locations should store a specific item.</span></span> <span data-ttu-id="fc9ae-114">Derfor gjør sonebasert etterfylling det mulig å bruke min./maks. etterfylling, selv om du ikke har faste lokasjoner for hver vare eller varevariant på lageret.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-114">Therefore, zone-based replenishment lets you use min/max replenishment even if you don't have fixed locations for each item or item variant in the warehouse.</span></span> <span data-ttu-id="fc9ae-115">Når et antall i sonen faller under den angitte minimumsterskelen, opprettes etterfyllingsarbeid.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-115">When a quantity in the zone falls below the specified minimum threshold, replenishment work is created.</span></span> <span data-ttu-id="fc9ae-116">Lokasjonsdirektiver bestemmer hvilken lokasjon lageret skal plasseres i.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-116">Location directives will determine which specific location the inventory should be put into.</span></span>

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a><span data-ttu-id="fc9ae-117">Aktiver funksjonen for etterfylling av soneterskel</span><span class="sxs-lookup"><span data-stu-id="fc9ae-117">Turn on the Zone threshold replenishment feature</span></span>

<span data-ttu-id="fc9ae-118">Før du kan bruke *Etterfylling av soneterskel*-funksjonen, må den aktiveres i systemet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-118">Before you can use the *Zone threshold replenishment* feature, it must be turned on in your system.</span></span> <span data-ttu-id="fc9ae-119">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-119">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="fc9ae-120">I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="fc9ae-120">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="fc9ae-121">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="fc9ae-121">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="fc9ae-122">**Funksjonsnavn:** *Etterfylling av soneterskel*</span><span class="sxs-lookup"><span data-stu-id="fc9ae-122">**Feature name:** *Zone threshold replenishment*</span></span>

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a><span data-ttu-id="fc9ae-123">Konfigurere sonebasert etterfylling</span><span class="sxs-lookup"><span data-stu-id="fc9ae-123">Set up zone-based replenishment</span></span>

<span data-ttu-id="fc9ae-124">Hvis du vil konfigurere sonebasert etterfylling, må du konfigurere flere deler av systemet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-124">To set up zone-based replenishment, you must configure several parts of the system.</span></span> <span data-ttu-id="fc9ae-125">Denne delen introduserer de ulike innstillingene og gir informasjon om demonstrasjonsdataverdier du kan angi hvis du vil jobbe gjennom scenariet på slutten av dette emnet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-125">This section introduces the various settings and provides demo data values that you can enter if you want to work through the scenario at the end of this topic.</span></span>

### <a name="set-up-directive-codes"></a><span data-ttu-id="fc9ae-126">Konfigurere direktivkoder</span><span class="sxs-lookup"><span data-stu-id="fc9ae-126">Set up directive codes</span></span>

<span data-ttu-id="fc9ae-127">Med [Direktivkoder](control-warehouse-location-directives.md) kan du være mer spesifikk når du definerer lokasjonsmalen som brukes i en arbeidsmal.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-127">[Directive codes](control-warehouse-location-directives.md) let you be more specific when you define the location template that is used in a work template.</span></span> <span data-ttu-id="fc9ae-128">Hver kode etablerer en felles verdi du kan referere til når du konfigurerer hver maltype.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-128">Each code establishes a common value that you can refer to when you configure each type of template.</span></span>

#### <a name="view-and-edit-directive-codes"></a><span data-ttu-id="fc9ae-129">Vise og redigere direktivkoder</span><span class="sxs-lookup"><span data-stu-id="fc9ae-129">View and edit directive codes</span></span>

<span data-ttu-id="fc9ae-130">Hvis du vil vise eller redigere direktivkoder, går du til **Lagerstyring \> Oppsett \> Direktivkoder**.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-130">To view or edit your directive codes, go to **Warehouse management \> Setup \> Directive codes**.</span></span>

#### <a name="prepare-demo-data-directive-codes"></a><span data-ttu-id="fc9ae-131">Forberede direktivkoder for demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="fc9ae-131">Prepare demo data directive codes</span></span>

<span data-ttu-id="fc9ae-132">Dette eksemplet viser hvordan du klargjør en direktivkode.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-132">This example shows how to prepare a directive code.</span></span> <span data-ttu-id="fc9ae-133">Hvis du planlegger å jobbe gjennom scenariet på slutten av dette emnet, bruker du demonstrasjonsdataverdiene som finnes her.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-133">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="fc9ae-134">Hvis ikke bruker du dine egne verdier.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-134">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="fc9ae-135">Velg den juridiske enheten **USMF** som skal brukes sammen med demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-135">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="fc9ae-136">Gå til **Lagerstyring \> Oppsett \> Direktivkoder**.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-136">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="fc9ae-137">I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="fc9ae-138">I den nye raden angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="fc9ae-138">In the new row, set the following values:</span></span>

    - <span data-ttu-id="fc9ae-139">**Direktivkode:** _Soneetterfyll._</span><span class="sxs-lookup"><span data-stu-id="fc9ae-139">**Directive code:** _Zone replen_</span></span>
    - <span data-ttu-id="fc9ae-140">**Beskrivelse av direktivet:** _Soneetterfylling_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-140">**Directive description:** _Zone replenishment_</span></span>

1. <span data-ttu-id="fc9ae-141">Velg **Lagre** for å lagre den nye koden.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-141">Select **Save** to save the new code.</span></span>

### <a name="set-up-replenishment-templates"></a><span data-ttu-id="fc9ae-142">Konfigurer etterfyllingsmaler</span><span class="sxs-lookup"><span data-stu-id="fc9ae-142">Set up replenishment templates</span></span>

<span data-ttu-id="fc9ae-143">Maler for etterfylling basert på [minimums- og maksimumsantall](tasks/set-up-min-max-replenishment-process.md) er den primære mekanismen for å opprettholde optimal nivåer på plukklokasjoner.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-143">[Min/max replenishment templates](tasks/set-up-min-max-replenishment-process.md) are the primary mechanism for maintaining optimal levels in picking locations.</span></span> <span data-ttu-id="fc9ae-144">I disse malene må du konfigurere reglene som skal brukes til å etterfylle beholdningen i lageret.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-144">In these templates, you must set up the rules that will be used to replenish inventory in the warehouse.</span></span> <span data-ttu-id="fc9ae-145">Etterfyllingen som malene kan brukes til, inkluderer sonebasert etterfylling.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-145">The replenishment that the templates can be used for includes zone-based replenishment.</span></span>

#### <a name="view-and-edit-replenishment-templates"></a><span data-ttu-id="fc9ae-146">Vise og redigere etterfyllingsmaler</span><span class="sxs-lookup"><span data-stu-id="fc9ae-146">View and edit replenishment templates</span></span>

<span data-ttu-id="fc9ae-147">En etterfyllingsmal er et sett med regler som bestemmer når og hvordan en lokasjon fylles.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-147">A replenishment template is a set of rules that control when and how a location is replenished.</span></span> <span data-ttu-id="fc9ae-148">Du velger en mal som skal styre når og hvordan etterfylling skal utføres.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-148">You select a template to control when and how replenishment is done.</span></span> <span data-ttu-id="fc9ae-149">Gå til **Lagerstyring \> Oppsett \> Etterfylling \> Etterfyllingsmaler** for å vise eller redigere etterfyllingsmalene.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-149">To view or edit your replenishment templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>

#### <a name="prepare-a-demo-data-replenishment-template"></a><span data-ttu-id="fc9ae-150">Klargjøre en etterfyllingsmal for demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="fc9ae-150">Prepare a demo data replenishment template</span></span>

<span data-ttu-id="fc9ae-151">Dette eksemplet viser hvordan du klargjør en etterfyllingsmal.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-151">This example shows how to prepare a replenishment template.</span></span> <span data-ttu-id="fc9ae-152">Hvis du planlegger å jobbe gjennom scenariet på slutten av dette emnet, bruker du demonstrasjonsdataverdiene som finnes her.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-152">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="fc9ae-153">Hvis ikke bruker du dine egne verdier.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-153">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="fc9ae-154">Velg den juridiske enheten **USMF** som skal brukes sammen med demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-154">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="fc9ae-155">Gå til **Lagerstyring \> Oppsett \> Etterfylling \> Etterfyllingsmaler**.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-155">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="fc9ae-156">Velg **Rediger** for å legge siden inn i redigeringsmodus.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-156">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="fc9ae-157">I handlingsruten velger du **Ny** for å legge til en rad i **Oversikt**-rutenettet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-157">On the Action Pane, select **New** to add a row to the **Overview** grid.</span></span>
1. <span data-ttu-id="fc9ae-158">I den nye raden angir du følgende verdier.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-158">In the new row, set the following values.</span></span> <span data-ttu-id="fc9ae-159">Godta standardverdiene for alle de andre feltene.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-159">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="fc9ae-160">**Etterfyllingsmal:** _Sone min./maks. etterfyll._</span><span class="sxs-lookup"><span data-stu-id="fc9ae-160">**Replenish template:** _Zone min/max replen_</span></span>
    - <span data-ttu-id="fc9ae-161">**Beskrivelse:** _Sone min./maks. etterfylling_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-161">**Description:** _Zone min/max replenishment_</span></span>
    - <span data-ttu-id="fc9ae-162">**Etterfyllingstype:** _Minimum eller maksimum_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-162">**Replenishment type:** _Minimum or maximum_</span></span>

1. <span data-ttu-id="fc9ae-163">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-163">Select **Save**.</span></span>
1. <span data-ttu-id="fc9ae-164">Mens den nye raden fortsatt er valgt i **Oversikt**-rutenettet, velger du **Ny** over **Detaljer for etterfyllingsmal**-rutenettet for å legge til en rad som er tilknyttet til *Sone min./maks. etterfyll.* som du akkurat har opprettet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-164">While the new row is still selected in the **Overview** grid, select **New** above the **Replenishment Template Details** grid to add a row that is associated with the *Zone Min/Max replen* replenishment template that you just created.</span></span>
1. <span data-ttu-id="fc9ae-165">I den nye raden angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="fc9ae-165">In the new row, set the following values:</span></span>

    - <span data-ttu-id="fc9ae-166">**Sekvensnummer:** Angi _1_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-166">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="fc9ae-167">**Beskrivelse:** Angi _Velg soneetterfylling_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-167">**Description:** Enter _Pick zone replenishment_.</span></span>
    - <span data-ttu-id="fc9ae-168">**Etterfyllingsenhet:** Velg _ea_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-168">**Replenishment unit:** Select _ea_.</span></span>
    - <span data-ttu-id="fc9ae-169">**Forespørselstype:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-169">**Request type:** Leave this field blank.</span></span>
    - <span data-ttu-id="fc9ae-170">**Direktivkode:** Dette feltet kobler etterfyllingsmalen til et lokasjonsdirektiv.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-170">**Directive code:** This field links the replenishment template with a location directive.</span></span> <span data-ttu-id="fc9ae-171">Velg demonstrasjonsdataenes direktivkode som du opprettet tidligere (_Soneetterfyll._).</span><span class="sxs-lookup"><span data-stu-id="fc9ae-171">Select the demo data directive code that you created earlier (_Zone replen_).</span></span>
    - <span data-ttu-id="fc9ae-172">**Arbeidsmal:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-172">**Work template:** Leave this field blank.</span></span>
    - <span data-ttu-id="fc9ae-173">**Minimumsantall:** I dette feltet angis antallet som skal utløse etterfylling.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-173">**Minimum quantity:** This field sets the quantity that replenishment will be triggered at.</span></span> <span data-ttu-id="fc9ae-174">Angi _50_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-174">Enter _50_.</span></span>
    - <span data-ttu-id="fc9ae-175">**Maksimumsantall:** I dette feltet angis maksimalt antall av en vare som kan finnes i en sone.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-175">**Maximum quantity:** This field sets the maximum quantity of an item that can be present in a zone.</span></span> <span data-ttu-id="fc9ae-176">Generert etterfyllingsarbeid øker beholdningen til dette antallet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-176">Generated replenishment work will increase inventory to this quantity.</span></span> <span data-ttu-id="fc9ae-177">Angi _150_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-177">Enter _150_.</span></span>
    - <span data-ttu-id="fc9ae-178">**Enhet:** I dette feltet angis enheten for minimums- og maksimumsverdiene.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-178">**Unit:** This field sets the unit for the minimum and maximum values.</span></span> <span data-ttu-id="fc9ae-179">Velg _ea_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-179">Select _ea_.</span></span>
    - <span data-ttu-id="fc9ae-180">**Behovsøkning:** Velg _Rund opp_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-180">**Demand increment:** Select _Round up_.</span></span>
    - <span data-ttu-id="fc9ae-181">**Etterfyll tomme faste lokasjoner:** Velg denne avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-181">**Replenish empty fixed locations:** Select this check box.</span></span>
    - <span data-ttu-id="fc9ae-182">**Etterfyll bare faste lokasjoner:** Fjern merket i denne boksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-182">**Replenish only fixed locations:** Clear this check box.</span></span>
    - <span data-ttu-id="fc9ae-183">**Modus for produktspørring:** Velg _Produktspørring_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-183">**Product query mode:** Select _Product query_.</span></span>
    - <span data-ttu-id="fc9ae-184">**Terskelomfang for etterfylling:** Dette feltet definerer om malen skal evalueres etter sone eller en bestemt lokasjon.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-184">**Replenishment threshold scope:** This field defines whether the template should evaluate by zone or by specific location.</span></span> <span data-ttu-id="fc9ae-185">Velg _Sone_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-185">Select _Zone_.</span></span>
    - <span data-ttu-id="fc9ae-186">**Lager:** Velg _61_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-186">**Warehouse:** Select _61_.</span></span>

1. <span data-ttu-id="fc9ae-187">Velg **Velg produkter** over **Detaljer for etterfyllingsmal**-rutenettet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-187">Select **Select products** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="fc9ae-188">I **Produktspørring**-dialogboksen, på **Område**-fanen, velger du **Legg til** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-188">In the **Product query** dialog box, on the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="fc9ae-189">I den nye raden angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="fc9ae-189">In the new row, set the following values:</span></span>

    - <span data-ttu-id="fc9ae-190">**Tabell:** _Varer_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-190">**Table:** _Items_</span></span>
    - <span data-ttu-id="fc9ae-191">**Avledet tabell:** _Varer_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-191">**Derived table:** _Items_</span></span>
    - <span data-ttu-id="fc9ae-192">**Felt:** _Varenummer_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-192">**Field:** _Item number_</span></span>
    - <span data-ttu-id="fc9ae-193">**Vilkår:** _A0001_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-193">**Criteria:** _A0001_</span></span>

1. <span data-ttu-id="fc9ae-194">Velg **OK** for å lagre spørringen og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-194">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="fc9ae-195">Velg **Velg sone som skal etterfylles** over **Detaljer for etterfyllingsmal**-rutenettet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-195">Select **Select zones to replenish** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="fc9ae-196">I **Sonespørring**-dialogboksen, på **Område**-fanen, legger du til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-196">In the **Zone query** dialog box, on the **Range** tab, add a row to the grid.</span></span>
1. <span data-ttu-id="fc9ae-197">I den nye raden angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="fc9ae-197">In the new row, set the following values:</span></span>

    - <span data-ttu-id="fc9ae-198">**Tabell:** _Lagersone_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-198">**Table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="fc9ae-199">**Avledet tabell:** _Lagersone_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-199">**Derived table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="fc9ae-200">**Felt:** _Sone-ID_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-200">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="fc9ae-201">**Vilkår:** _ETASJE_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-201">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="fc9ae-202">Velg **OK** for å lagre spørringen og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-202">Select **OK** to save your query and close the dialog box.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="fc9ae-203">Konfigurer lokasjonsdirektiver</span><span class="sxs-lookup"><span data-stu-id="fc9ae-203">Set up location directives</span></span>

<span data-ttu-id="fc9ae-204">Til forskjell fra lokasjonsbasert min./maks. etterfylling krever sonebasert min./maks. etterfylling at du definerer både plukklokasjonsdirektiver og legger til lokasjonsdirektiver, fordi systemet evaluerer hele sonen i stedet for bare plukklokasjon for utgående arbeid.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-204">Unlike location-based min/max replenishment, zone-based min/max replenishment requires that you set up both pick location directives and put location directives, because the system evaluates the whole zone instead of just the pick location for outbound work.</span></span>

#### <a name="view-and-edit-location-directives"></a><span data-ttu-id="fc9ae-205">Vise og redigere lokasjonsdirektiver</span><span class="sxs-lookup"><span data-stu-id="fc9ae-205">View and edit location directives</span></span>

<span data-ttu-id="fc9ae-206">Hvis du vil vise eller redigere lokasjonsdirektiver, går du til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-206">To view or edit your location directives, go to **Warehouse management \> Setup \> Location directives**.</span></span>

<span data-ttu-id="fc9ae-207">Se neste del for eksempler som viser hvordan du kan bruke innstillingene til å opprette de påkrevde plukklokasjonsdirektivene og legge til lokasjonsdirektiver.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-207">For examples that show how to use the settings to create the required pick location directives and put location directives, see the next section.</span></span>

#### <a name="prepare-demo-data-location-directives"></a><span data-ttu-id="fc9ae-208">Forberede lokasjonsdirektiver for demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="fc9ae-208">Prepare demo data location directives</span></span>

<span data-ttu-id="fc9ae-209">Hvis du vil forberede demonstrasjonsdata slik at de kan brukes i scenariet på slutten av dette emnet, må du opprette to lokasjonsdirektiver: ett for plukking og ett for plassering.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-209">To prepare demo data so that it can be used in the scenario at the end of this topic, you must create two location directives: one for pick and one for put.</span></span>

##### <a name="create-a-replenishment-pick-directive"></a><span data-ttu-id="fc9ae-210">Opprette et plukkdirektiv for etterfylling</span><span class="sxs-lookup"><span data-stu-id="fc9ae-210">Create a replenishment pick directive</span></span>

1. <span data-ttu-id="fc9ae-211">Velg den juridiske enheten **USMF** som skal brukes sammen med demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-211">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="fc9ae-212">Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-212">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="fc9ae-213">I den venstre ruten setter du **Arbeidsordretype**-feltet til _Etterfylling_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-213">In the left pane, set the **Work order type** field to _Replenishment_.</span></span>
1. <span data-ttu-id="fc9ae-214">I handlingsruten velger du **Ny** for å opprette et nytt direktiv.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-214">On the Action Pane, select **New** to create a new directive.</span></span>
1. <span data-ttu-id="fc9ae-215">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="fc9ae-215">Set the following values:</span></span>

    - <span data-ttu-id="fc9ae-216">**Sekvensnummer:** Godta standardverdien.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-216">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="fc9ae-217">**Navn:** Angi _Soneplukking_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-217">**Name:** Enter _Zone pick_.</span></span>
    - <span data-ttu-id="fc9ae-218">**Arbeidstype:** Velg _Plukk_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-218">**Work type:** Select _Pick_.</span></span>
    - <span data-ttu-id="fc9ae-219">**Område:** Velg _6_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-219">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="fc9ae-220">**Lager:** Velg _61_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-220">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="fc9ae-221">**Direktivkoden:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-221">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="fc9ae-222">**Fler SKU:** Angi dette alternativet til _Nei_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-222">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="fc9ae-223">Velg **Lagre** for å opprette et direktiv med innstillingene du har konfigurert så langt.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-223">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="fc9ae-224">På **Linjer**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-224">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="fc9ae-225">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="fc9ae-225">On the new line, set the following values:</span></span>

    - <span data-ttu-id="fc9ae-226">**Sekvensnummer:** Angi _1_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-226">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="fc9ae-227">**Fra-antall:** Angi _0_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-227">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="fc9ae-228">**Til-antall:** Angi _10000000_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-228">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="fc9ae-229">**Enhet:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-229">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="fc9ae-230">**Finn antall:** Velg _Ingen_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-230">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="fc9ae-231">**Begrens etter enhet:** Fjern merket i denne avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-231">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="fc9ae-232">**Rund opp til enhet:** Fjern merket i denne avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-232">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="fc9ae-233">**Finn emballasjeantall:** Fjern merket i denne avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-233">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="fc9ae-234">**Tillat oppdeling:** Merk av denne avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-234">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="fc9ae-235">Velg **Lagre** for å lagre den nye linjen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-235">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="fc9ae-236">Mens den nye linjen fremdeles er valgt i **Linjer**-rutenettet velger du **Ny** på **Handlinger for lokasjonsdirektiv**-hurtigfanen for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-236">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="fc9ae-237">I den nye raden angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="fc9ae-237">In the new row, set the following values:</span></span>

    - <span data-ttu-id="fc9ae-238">**Sekvensnummer:** Angi _1_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-238">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="fc9ae-239">**Navn:** Angi _Plukk fra parti_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-239">**Name:** Enter _Pick from bulk_.</span></span>
    - <span data-ttu-id="fc9ae-240">**Fast lokasjonsbruk:** Velg _Faste og ikke-faste lokasjoner_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-240">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="fc9ae-241">**Tillat negativ beholdning:** Fjern merket i denne avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-241">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="fc9ae-242">**Parti aktivert:** Fjern merket i denne avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-242">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="fc9ae-243">**Strategi:** Velg _Ingen_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-243">**Strategy:** Select _None_.</span></span>

1. <span data-ttu-id="fc9ae-244">Velg **Lagre** for å lagre den nye handlingen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-244">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="fc9ae-245">Mens den nye handlingen fremdeles er valgt, velger du **Rediger spørring** over **Handlinger for lokasjonsdirektiv**-rutenettet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-245">While your new action still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="fc9ae-246">En spørringsdialogboks vises der du kan velge lokasjonene du vil etterfylle fra.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-246">A query dialog box appears, where you can select the locations to replenish from.</span></span> <span data-ttu-id="fc9ae-247">På **Område**-fanen velger du **Legg til** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-247">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="fc9ae-248">I den nye raden angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="fc9ae-248">In the new row, set the following values:</span></span>

    - <span data-ttu-id="fc9ae-249">**Tabell:** _Plasseringer_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-249">**Table:** _Locations_</span></span>
    - <span data-ttu-id="fc9ae-250">**Avledet tabell:** _Lokasjoner_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-250">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="fc9ae-251">**Felt:** _Sone-ID_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-251">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="fc9ae-252">**Vilkår:** _BULK_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-252">**Criteria:** _BULK_</span></span>

1. <span data-ttu-id="fc9ae-253">Velg **OK** for å lagre spørringen og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-253">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="fc9ae-254">Velg **Lagre** for å lagre lokasjonsdirektivet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-254">Select **Save** to save your location directive.</span></span>

##### <a name="create-a-replenishment-put-directive"></a><span data-ttu-id="fc9ae-255">Opprette et plasseringsdirektiv for etterfylling</span><span class="sxs-lookup"><span data-stu-id="fc9ae-255">Create a replenishment put directive</span></span>

1. <span data-ttu-id="fc9ae-256">I ruten til venstre på **Lokasjonsdirektiver**-siden kontrollerer du at **Arbeidsordretype**-feltet fremdeles er angitt til _Etterfylling_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-256">On the **Location directives** page, in the left pane, make sure that the **Work order type** field is still set to _Replenishment_.</span></span>
1. <span data-ttu-id="fc9ae-257">I handlingsruten velger du **Ny** for å opprette et nytt direktiv.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-257">On the Action Pane, select **New** to create another new directive.</span></span>
1. <span data-ttu-id="fc9ae-258">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="fc9ae-258">Set the following values:</span></span>

    - <span data-ttu-id="fc9ae-259">**Sekvensnummer:** Godta standardverdien.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-259">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="fc9ae-260">**Navn:** Angi _Soneplassering_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-260">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="fc9ae-261">**Arbeidsordretype:** Velg _Plasser_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-261">**Work order type:** Select _Put_.</span></span>
    - <span data-ttu-id="fc9ae-262">**Område:** Velg _6_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-262">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="fc9ae-263">**Lager:** Velg _61_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-263">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="fc9ae-264">**Direktivkode:** Velg _Soneetterfyll._ for å koble dette lokasjonsdirektivet med etterfyllingsmalen du opprettet tidligere, ved hjelp av koden du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-264">**Directive code:** Select _Zone replen_ to link this location directive with the replenishment template that you created earlier by using the code that you created earlier.</span></span>
    - <span data-ttu-id="fc9ae-265">**Fler SKU:** Angi dette alternativet til _Nei_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-265">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="fc9ae-266">Velg **Lagre** for å opprette et direktiv med innstillingene du har konfigurert så langt.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-266">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="fc9ae-267">På **Linjer**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-267">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="fc9ae-268">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="fc9ae-268">On the new line, set the following values:</span></span>

    - <span data-ttu-id="fc9ae-269">**Sekvensnummer:** Angi _1_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-269">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="fc9ae-270">**Fra-antall:** Angi _0_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-270">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="fc9ae-271">**Til-antall:** Angi _10000000_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-271">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="fc9ae-272">**Enhet:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-272">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="fc9ae-273">**Finn antall:** Velg _Ingen_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-273">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="fc9ae-274">**Begrens etter enhet:** Fjern merket i denne avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-274">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="fc9ae-275">**Rund opp til enhet:** Fjern merket i denne avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-275">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="fc9ae-276">**Finn emballasjeantall:** Fjern merket i denne avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-276">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="fc9ae-277">**Tillat oppdeling:** Merk av denne avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-277">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="fc9ae-278">Velg **Lagre** for å lagre den nye linjen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-278">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="fc9ae-279">Mens den nye linjen fremdeles er valgt i **Linjer**-rutenettet velger du **Ny** på **Handlinger for lokasjonsdirektiv**-hurtigfanen for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-279">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="fc9ae-280">I den nye raden angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="fc9ae-280">In the new row, set the following values:</span></span>

    - <span data-ttu-id="fc9ae-281">**Sekvensnummer:** Angi _1_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-281">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="fc9ae-282">**Navn:** Angi _Soneplassering_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-282">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="fc9ae-283">**Fast lokasjonsbruk:** Velg _Faste og ikke-faste lokasjoner_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-283">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="fc9ae-284">**Tillat negativ beholdning:** Fjern merket i denne avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-284">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="fc9ae-285">**Parti aktivert:** Fjern merket i denne avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-285">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="fc9ae-286">**Strategi:** Velg _Konsolider_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-286">**Strategy:** Select _Consolidate_.</span></span>

1. <span data-ttu-id="fc9ae-287">Velg **Lagre** for å lagre den nye handlingen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-287">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="fc9ae-288">Mens den nye handlingen fremdeles er valgt, velger du **Rediger spørring** over **Handlinger for lokasjonsdirektiv**-rutenettet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-288">While your new action is still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="fc9ae-289">En spørringsdialogboks vises der du kan velge sonene du vil etterfylle.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-289">A query dialog box appears, where you can select the zone to replenish to.</span></span> <span data-ttu-id="fc9ae-290">Denne sonen skal være den samme sonen som er angitt i etterfyllingsmalen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-290">This zone should be the same zone that is specified in the replenishment template.</span></span> <span data-ttu-id="fc9ae-291">På **Område**-fanen velger du **Legg til** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-291">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="fc9ae-292">I den nye raden angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="fc9ae-292">In the new row, set the following values:</span></span>

    - <span data-ttu-id="fc9ae-293">**Tabell:** _Plasseringer_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-293">**Table:** _Locations_</span></span>
    - <span data-ttu-id="fc9ae-294">**Avledet tabell:** _Lokasjoner_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-294">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="fc9ae-295">**Felt:** _Sone-ID_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-295">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="fc9ae-296">**Vilkår:** _ETASJE_</span><span class="sxs-lookup"><span data-stu-id="fc9ae-296">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="fc9ae-297">Velg **OK** for å lagre spørringen og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-297">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="fc9ae-298">Velg **Lagre** for å lagre lokasjonsdirektivet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-298">Select **Save** to save your location directive.</span></span>

## <a name="scenario"></a><span data-ttu-id="fc9ae-299">Scenario</span><span class="sxs-lookup"><span data-stu-id="fc9ae-299">Scenario</span></span>

<span data-ttu-id="fc9ae-300">Denne delen inneholder et eksempelscenario som viser hvordan du arbeider med funksjonen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-300">This section provides a sample scenario that shows how to work with the feature.</span></span>

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a><span data-ttu-id="fc9ae-301">Klargjøre eksempeldataene som kreves for eksempelscenarioet</span><span class="sxs-lookup"><span data-stu-id="fc9ae-301">Prepare the sample data that is required for the sample scenario</span></span>

<span data-ttu-id="fc9ae-302">Før du begynner å jobbe gjennom scenariet, må du aktivere eksempeldata og konfigurere funksjonen som beskrevet i denne delen og i de forrige delene i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-302">Before you start to work through the scenario, you must activate sample data and set up the feature as described in this section and in the previous sections of this topic.</span></span>

#### <a name="use-the-usmf-legal-entity"></a><span data-ttu-id="fc9ae-303">Bruk den juridiske enheten USMF</span><span class="sxs-lookup"><span data-stu-id="fc9ae-303">Use the USMF legal entity</span></span>

<span data-ttu-id="fc9ae-304">For å arbeide deg gjennom dette scenariet ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-304">To work through the scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="fc9ae-305">Du må også velge den juridiske enheten **USMF** før du begynner.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-305">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="prepare-additional-sample-data"></a><span data-ttu-id="fc9ae-306">Klargjøre flere eksempeldata</span><span class="sxs-lookup"><span data-stu-id="fc9ae-306">Prepare additional sample data</span></span>

<span data-ttu-id="fc9ae-307">Når du har valgt den juridiske enheten **USMF**, legger du til de ekstra eksempeldataene som kreves, som beskrevet under [Konfigurere sonebasert etterfylling](#setup) tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-307">After you've selected the **USMF** legal entity, add the additional sample data that is required, as described in the [Set up zone-based replenishment](#setup) section earlier in this topic.</span></span>

#### <a name="check-your-on-hand-inventory"></a><span data-ttu-id="fc9ae-308">Kontrollere lagerbeholdningen</span><span class="sxs-lookup"><span data-stu-id="fc9ae-308">Check your on-hand inventory</span></span>

<span data-ttu-id="fc9ae-309">Følg denne fremgangsmåten for å kontrollere at systemet inneholder nok beholdning til å støtte eksempelscenariet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-309">Follow these steps to make sure that your system includes enough inventory to support the sample scenario.</span></span>

1. <span data-ttu-id="fc9ae-310">Kontroller at det er lagerbeholdning for vare *A0001* på to forskjellige lokasjoner i plukksonen (*ETASJE*) som er angitt i etterfyllingsmalen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-310">Make sure that there is on-hand inventory for item *A0001* at two different locations in the pick zone (*FLOOR*) that is specified in the replenishment template.</span></span> <span data-ttu-id="fc9ae-311">Den totale beholdningen må imidlertid være mindre enn det påkrevde minimumsantallet (*50*) som er angitt i etterfyllingsmalen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-311">However, the total inventory should be less than the required minimum quantity (*50*) that is specified on the replenishment template.</span></span> <span data-ttu-id="fc9ae-312">På denne måten kan du simulere hvordan beregningen skal skje for hele sonen i stedet for bare for én enkel lokasjon.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-312">In this way, you can simulate how the calculation occurs for the whole zone instead of just for a single location.</span></span> <span data-ttu-id="fc9ae-313">**Bruk noen av lagerprosessene til å justere beholdningen etter behov.**</span><span class="sxs-lookup"><span data-stu-id="fc9ae-313">**Use any of the warehouse processes to adjust inventory as required.**</span></span>
1. <span data-ttu-id="fc9ae-314">Kontroller at det er nok beholdning for vare *A0001* til en partilokasjon som er angitt i lokasjonsdirektivet for soneplukking, der etterfyllingsarbeidet skal plukke varene fra sone-ID *PARTI*.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-314">Make sure that there is enough inventory for item *A0001* at a bulk location that is specified in the zone pick location directive where the replenishment work should pick the items from zone ID *BULK*.</span></span> <span data-ttu-id="fc9ae-315">Den totale beholdningen må være mer enn det påkrevde maksimumsantallet (*150*) som er angitt i etterfyllingsmalen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-315">The total inventory must be more than the required maximum quantity (*150*) that is specified in the replenishment template.</span></span>
1. <span data-ttu-id="fc9ae-316">Valgfritt, men anbefalt: Følg denne fremgangsmåten for å opprette en justeringsjournal for beholdning:</span><span class="sxs-lookup"><span data-stu-id="fc9ae-316">Optional but recommended: Follow these steps to create an inventory adjustment journal:</span></span>

    1. <span data-ttu-id="fc9ae-317">Gå til **Lagerstyring \> Journaloppføringer \> Varer \> Beholdningsjustering**.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-317">Go to **Inventory management \> Journal entries \> Items \> Inventory adjustment**.</span></span>
    1. <span data-ttu-id="fc9ae-318">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-318">Select **New**.</span></span>
    1. <span data-ttu-id="fc9ae-319">I dialogboksen **Opprett beholdningsjournal** velger du *61* i **Lager**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-319">In the **Create inventory journal** dialog box, in the **Warehouse** field, select *61*.</span></span>
    1. <span data-ttu-id="fc9ae-320">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-320">Select **OK**.</span></span>
    1. <span data-ttu-id="fc9ae-321">På **Journallinjer**-hurtigfanen bruker du **Ny**-knappen til å legge til tre linjer i rutenettet og angir følgende verdier.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-321">On the **Journal lines** FastTab, use the **New** button to add three lines to the grid, and set the following values.</span></span> <span data-ttu-id="fc9ae-322">Når du er ferdig med å konfigurere hver linje, velger du **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-322">After you've finished setting up each line, select **Save**.</span></span>

        - <span data-ttu-id="fc9ae-323">**Linje 1:**</span><span class="sxs-lookup"><span data-stu-id="fc9ae-323">**Line 1:**</span></span>

            - <span data-ttu-id="fc9ae-324">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="fc9ae-324">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="fc9ae-325">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="fc9ae-325">**Site:** *6*</span></span>
            - <span data-ttu-id="fc9ae-326">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="fc9ae-326">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="fc9ae-327">**Lokasjon:** *02A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="fc9ae-327">**Location:** *02A01R1S1B*</span></span>
            - <span data-ttu-id="fc9ae-328">**Nummerskilt:** Velg et eksisterende nummerskilt i listen, eller opprett et nytt nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-328">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="fc9ae-329">**Antall:** *1000*</span><span class="sxs-lookup"><span data-stu-id="fc9ae-329">**Quantity:** *1000*</span></span>

        - <span data-ttu-id="fc9ae-330">**Linje 2:**</span><span class="sxs-lookup"><span data-stu-id="fc9ae-330">**Line 2:**</span></span>

            - <span data-ttu-id="fc9ae-331">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="fc9ae-331">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="fc9ae-332">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="fc9ae-332">**Site:** *6*</span></span>
            - <span data-ttu-id="fc9ae-333">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="fc9ae-333">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="fc9ae-334">**Lokasjon:** *07A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="fc9ae-334">**Location:** *07A01R2S1B*</span></span>
            - <span data-ttu-id="fc9ae-335">**Nummerskilt:** Velg et eksisterende nummerskilt i listen, eller opprett et nytt nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-335">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="fc9ae-336">**Antall:** *15*</span><span class="sxs-lookup"><span data-stu-id="fc9ae-336">**Quantity:** *15*</span></span>

        - <span data-ttu-id="fc9ae-337">**Linje 3:**</span><span class="sxs-lookup"><span data-stu-id="fc9ae-337">**Line 3:**</span></span>

            - <span data-ttu-id="fc9ae-338">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="fc9ae-338">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="fc9ae-339">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="fc9ae-339">**Site:** *6*</span></span>
            - <span data-ttu-id="fc9ae-340">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="fc9ae-340">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="fc9ae-341">**Lokasjon:** *07A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="fc9ae-341">**Location:** *07A01R1S1B*</span></span>
            - <span data-ttu-id="fc9ae-342">**Nummerskilt:** Velg et eksisterende nummerskilt i listen, eller opprett et nytt nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-342">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="fc9ae-343">**Antall:** *10*</span><span class="sxs-lookup"><span data-stu-id="fc9ae-343">**Quantity:** *10*</span></span>

    1. <span data-ttu-id="fc9ae-344">Velg **Valider** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-344">On the Action Pane, select **Validate**.</span></span> <span data-ttu-id="fc9ae-345">Løs eventuelle feil som blir funnet før du går videre til neste trinn.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-345">Address any errors that are found before you move on to the next step.</span></span>
    1. <span data-ttu-id="fc9ae-346">Velg **Bokfør** i handlingsruten for å postere beholdningen til lageret.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-346">On the Action Pane, select **Post** to post the inventory to the warehouse.</span></span>

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a><span data-ttu-id="fc9ae-347">Eksempelscenario: Kjør sonebasert min./maks. etterfylling</span><span class="sxs-lookup"><span data-stu-id="fc9ae-347">Sample scenario: Run zone-based min/max replenishment</span></span>

<span data-ttu-id="fc9ae-348">Etter at alle de nødvendige eksempeldataene er på plass, kan du utløse etterfylling ved å følge denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-348">After all the prerequisite sample data is in place, you can trigger replenishment by following these steps.</span></span>

1. <span data-ttu-id="fc9ae-349">Gå til **Lagerstyring \> Etterfylling \> Etterfyllinger**.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-349">Go to **Warehouse management \> Replenishment \> Replenishments**.</span></span>
1. <span data-ttu-id="fc9ae-350">På hurtigfanen **Poster som skal inkluderes** i **Etterfylling**-dialogboksen velger du **Filter**.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-350">In the **Replenishment** dialog box, on the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="fc9ae-351">I **Forespørsel**-dialogboksen på **Område**-fanen redigerer du standard tabellrad på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="fc9ae-351">In the **Inquiry** dialog box, on the **Range** tab, edit the default table row in the following way:</span></span>

    - <span data-ttu-id="fc9ae-352">**Tabell:** Velg _Etterfyllingsmaler_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-352">**Table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="fc9ae-353">**Avledet tabell:** Velg _Etterfyllingsmaler_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-353">**Derived table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="fc9ae-354">**Felt:** Velg _Etterfyllingsmal_.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-354">**Field:** Select _Replenishment template_.</span></span>
    - <span data-ttu-id="fc9ae-355">**Vilkår:** Velg _Sone min./maks. etterfyll._.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-355">**Criteria:** Select _Zone min/max replen_.</span></span> <span data-ttu-id="fc9ae-356">Denne etterfyllingsmalen er etterfyllingsmalen du opprettet mens du forberedt demonstrasjonsdataene for dette scenariet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-356">This replenishment template is the replenishment template that you created while you were preparing the demo data for this scenario.</span></span>

1. <span data-ttu-id="fc9ae-357">Velg **OK** for å lagre spørringen og gå til bake til **Etterfylling**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-357">Select **OK** to save the query and go back to the **Replenishment** dialog box.</span></span>
1. <span data-ttu-id="fc9ae-358">Velg **OK** for å kjøre etterfyllingsmalen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-358">Select **OK** to run the replenishment template.</span></span>

<span data-ttu-id="fc9ae-359">Etterfyllingsarbeid opprettes nå for å plukkebeholdning fra *PARTI*-sonen og etterfyll den med *ETASJE*-sonen.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-359">Replenishment work is now created to pick inventory from the *BULK* zone and replenish it to the *FLOOR* zone.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="fc9ae-360">Merknader og tips</span><span class="sxs-lookup"><span data-stu-id="fc9ae-360">Notes and tips</span></span>

<span data-ttu-id="fc9ae-361">Her er noen få merknader og tips om hvordan du arbeider med funksjonen:</span><span class="sxs-lookup"><span data-stu-id="fc9ae-361">Here are a few notes and tips for working with the feature:</span></span>

- <span data-ttu-id="fc9ae-362">Hvis du vil definere etterfyllingsarbeid som går til ønsket sone, kan du koble linjene for etterfyllingsmaler og lokasjonsdirektiver på en av følgende måter:</span><span class="sxs-lookup"><span data-stu-id="fc9ae-362">To set up replenishment work that goes to the desired zone, you can link the replenishment template lines and location directives in either of the following ways:</span></span>

    - <span data-ttu-id="fc9ae-363">Rediger lokasjonsdirektivets hovedspørring og filtrer de valgte linjene for etterfyllingsmal.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-363">Edit the location directive header query, and filter the selected replenishment template lines.</span></span>
    - <span data-ttu-id="fc9ae-364">Bruk en direktivkode på linjen for etterfyllingsmalen, og samsvar den til lokasjonsdirektivet for plassering.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-364">Use a directive code on the replenishment template line, and match it to the put location directive.</span></span>

- <span data-ttu-id="fc9ae-365">Hvis du bruker dynamiske lokasjoner, vil etterfyllingsarbeid bli opprettet enten for den første tilgjengelige lokasjonen eller for en lokasjon som allerede inneholder beholdningen, hvis handlingen for lokasjonsdirektivet er definert til å bruke **Konsolidering**-strategien.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-365">If you're using dynamic locations, replenishment work will be created either for the first available location or for a location that already contains inventory, if the location directive action is set up to use the **Consolidate** strategy.</span></span>
- <span data-ttu-id="fc9ae-366">Hvis du bruker faste lokasjoner i stedet for soner, bør du bruke [standard min./maks. etterfylling](tasks/set-up-min-max-replenishment-process.md).</span><span class="sxs-lookup"><span data-stu-id="fc9ae-366">If you're using fixed locations instead of zones, you should use [standard min/max replenishment](tasks/set-up-min-max-replenishment-process.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]