---
title: Nummerskiltposisjonering for lokasjon
description: Ved å plassering av nummerskiltlokasjon kan du se hvor et nummerskilt befinner seg på en lokasjon med flere paller, for eksempel en lokasjon som bruker pallestabling med dobbel dybde.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: e5fd7a9a9703f9ab6802def0aac096e29aa04f1a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831392"
---
# <a name="location-license-plate-positioning"></a><span data-ttu-id="a26de-103">Nummerskiltposisjonering for lokasjon</span><span class="sxs-lookup"><span data-stu-id="a26de-103">Location license plate positioning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a26de-104">Ved å plassering av nummerskiltlokasjon kan du se hvor et nummerskilt befinner seg på en lokasjon med flere paller, for eksempel en lokasjon som bruker pallestabling med dobbel dybde.</span><span class="sxs-lookup"><span data-stu-id="a26de-104">License plate location positioning lets you see where a license plate is located in a multi-pallet location, such as a location that uses double-deep pallet racking.</span></span>

<span data-ttu-id="a26de-105">Funksjonen legger til et sekvensnummer for hvert nummerskilt som settes inn i en lagerlokasjon.</span><span class="sxs-lookup"><span data-stu-id="a26de-105">The feature adds a sequence number to each license plate that is put into a storage location.</span></span> <span data-ttu-id="a26de-106">Dette sekvensnummeret brukes til å bestille nummerskilt i lagerlokasjonen.</span><span class="sxs-lookup"><span data-stu-id="a26de-106">This sequence number is used to order the license plates in the storage location.</span></span> <span data-ttu-id="a26de-107">Derfor støtter funksjonen intelligente scenarioer der kunder bruker et gravitasjonssporingssystem, og må kjenne til, for plukkfomål, hvilket nummerskilt som er vendt forover.</span><span class="sxs-lookup"><span data-stu-id="a26de-107">Therefore, the feature intelligently supports scenarios where customers are using a gravity racking system and must know, for picking purposes, which license plate is front-facing.</span></span>

<span data-ttu-id="a26de-108">Dette emnet inneholder et scenario som viser hvordan du definerer og bruker funksjonen.</span><span class="sxs-lookup"><span data-stu-id="a26de-108">This topic presents a scenario that shows how to set up and use the feature.</span></span>

## <a name="turn-on-the-location-license-plate-positioning-feature"></a><span data-ttu-id="a26de-109">Aktiver Nummerskiltplassering på lokasjon-funksjonen</span><span class="sxs-lookup"><span data-stu-id="a26de-109">Turn on the Location license plate positioning feature</span></span>

<span data-ttu-id="a26de-110">Før du kan bruke plassering av nummerskiltlokasjon, må funksjonen aktiveres i systemet.</span><span class="sxs-lookup"><span data-stu-id="a26de-110">Before you can use license plate location positioning, the feature must be turned on in your system.</span></span> <span data-ttu-id="a26de-111">Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="a26de-111">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="a26de-112">Funksjonen vises på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="a26de-112">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a26de-113">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="a26de-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a26de-114">**Funksjonsnavn:** *Nummerskiltplassering på lokasjon*</span><span class="sxs-lookup"><span data-stu-id="a26de-114">**Feature name:** *Location license plate positioning*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="a26de-115">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="a26de-115">Example scenario</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="a26de-116">Gjøre eksempeldata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="a26de-116">Make sample data available</span></span>

<span data-ttu-id="a26de-117">For å arbeide deg gjennom dette scenariet ved å bruke verdiene som foreslås her, må du arbeide på et system der standard eksempeldata er installert.</span><span class="sxs-lookup"><span data-stu-id="a26de-117">To work through this scenario by using the values that are suggested here, you must work on a system where sample data is installed.</span></span> <span data-ttu-id="a26de-118">Du må også velge den juridiske enheten **USMF** før du starter.</span><span class="sxs-lookup"><span data-stu-id="a26de-118">Additionally, you must select the **USMF** legal entity before you start.</span></span>

### <a name="set-up-the-feature-for-this-scenario"></a><span data-ttu-id="a26de-119">Konfigurer funksjonen for dette scenariet</span><span class="sxs-lookup"><span data-stu-id="a26de-119">Set up the feature for this scenario</span></span>

<span data-ttu-id="a26de-120">Fullfør fremgangsmåtene nedenfor for å konfigurere *Nummerskiltplassering på lokasjon*-funksjonen for scenariet som presenteres i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="a26de-120">Complete the following procedures to set up the *Location license plate positioning* feature for the scenario that is presented in this topic.</span></span>

#### <a name="location-profiles"></a><span data-ttu-id="a26de-121">Lokasjonsprofiler</span><span class="sxs-lookup"><span data-stu-id="a26de-121">Location profiles</span></span>

<span data-ttu-id="a26de-122">Funksjonen må aktiveres i lokasjonsprofilen for hver lokasjon den skal brukes på.</span><span class="sxs-lookup"><span data-stu-id="a26de-122">The feature must be turned on in the location profile for every location where it will be used.</span></span>

1. <span data-ttu-id="a26de-123">Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="a26de-123">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="a26de-124">I listen over lokasjonsprofiler i venstre rute velger du **BULK-06**.</span><span class="sxs-lookup"><span data-stu-id="a26de-124">In the list of location profiles in the left pane, select **BULK-06**.</span></span>
1. <span data-ttu-id="a26de-125">På **Generelt**-hurtigfanen er det lagt til to nye alternativer av denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="a26de-125">On the **General** FastTab, two new options have been added by the feature.</span></span> <span data-ttu-id="a26de-126">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a26de-126">Set the following values:</span></span>

    - <span data-ttu-id="a26de-127">**Aktiver plassering av nummerskilt:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="a26de-127">**Enable license plate position:** *Yes*</span></span>

        <span data-ttu-id="a26de-128">Når dette alternativet er satt til *Ja*, opprettholdes nummerskiltplasseringen for nummerskilt på lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="a26de-128">When this option is set to *Yes*, the license plate position will be maintained for license plates in the location.</span></span>

    - <span data-ttu-id="a26de-129">**Vis LP-plassering for mobil enhet:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="a26de-129">**Display mobile device LP position:** *Yes*</span></span>

        <span data-ttu-id="a26de-130">Når dette alternativet er angitt til *Ja*, vises nummerskiltplasseringen for brukere av mobil enhet under justering og opptelling.</span><span class="sxs-lookup"><span data-stu-id="a26de-130">When this option is set to *Yes*, the license plate position will be shown to mobile device users during adjustment and counting.</span></span> <span data-ttu-id="a26de-131">Du kan endre innstillingen for dette alternativet bare når funksjonen er aktivert.</span><span class="sxs-lookup"><span data-stu-id="a26de-131">You can change the setting of this option only when the feature is turned on.</span></span>

1. <span data-ttu-id="a26de-132">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a26de-132">Select **Save**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="a26de-133">Lokasjonsdirektiver</span><span class="sxs-lookup"><span data-stu-id="a26de-133">Location directives</span></span>

1. <span data-ttu-id="a26de-134">Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.</span><span class="sxs-lookup"><span data-stu-id="a26de-134">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="a26de-135">I den venstre ruten kontrollerer du at **Arbeidsordretype**-feltet er satt til *Salgsordrer*.</span><span class="sxs-lookup"><span data-stu-id="a26de-135">In the left pane, make sure that the **Work order type** field is set to *Sales orders*.</span></span>
1. <span data-ttu-id="a26de-136">I listen over lokasjonsdirektiver velger du **61 SO plukkordre**.</span><span class="sxs-lookup"><span data-stu-id="a26de-136">In the list of location directives, select **61 SO Pick order**.</span></span>
1. <span data-ttu-id="a26de-137">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="a26de-137">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="a26de-138">På **Linjer**-hurtigfanen velger du linjen som har en verdi for **sekvensnummer** på *2*.</span><span class="sxs-lookup"><span data-stu-id="a26de-138">On the **Lines** FastTab, select the line that has a **Sequence number** value of *2*.</span></span>
1. <span data-ttu-id="a26de-139">På **Lokasjonsdirektivhandlinger**-hurtigfanen velger du linjen som har **Navn**-verdien *Plukk for mindre enn pall* (det skal være den eneste linjen), og endrer verdien for **sekvensnummer** til *2*.</span><span class="sxs-lookup"><span data-stu-id="a26de-139">On the **Location Directive Actions** FastTab, select the line that has a **Name** value of *Pick for less than pallet* (it should be the only line), and change its **Sequence number** value to *2*.</span></span>
1. <span data-ttu-id="a26de-140">Velg **Ny** ovenfor rutenettet for å legge til en linje for en ny handling for lokasjonsdirektiv.</span><span class="sxs-lookup"><span data-stu-id="a26de-140">Select **New** above the grid to add a line for a new location directive action.</span></span>
1. <span data-ttu-id="a26de-141">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a26de-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a26de-142">**Sekvensnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="a26de-142">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="a26de-143">**Navn:** *Plukkplassering 1*</span><span class="sxs-lookup"><span data-stu-id="a26de-143">**Name:** *Pick position 1*</span></span>

1. <span data-ttu-id="a26de-144">Mens den nye linjen fremdeles er valgt, velger du **Rediger spørring** over rutenettet.</span><span class="sxs-lookup"><span data-stu-id="a26de-144">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="a26de-145">I redigeringsprogrammet for spørringer velger du **Sammenkoblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="a26de-145">In the query editor, select the **Joins** tab.</span></span>
1. <span data-ttu-id="a26de-146">Utvid **Lokasjoner**-tabellsammenkoblingen for å vise sammenkoblingen til **Lagerdimensjoner**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="a26de-146">Expand the **Locations** table join to show the join to the **Inventory dimensions** table.</span></span>
1. <span data-ttu-id="a26de-147">Utvid **Lagerdimensjoner**-tabellsammenkoblingen for å vise sammenkoblingen til **Lagerbeholdning**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="a26de-147">Expand the **Inventory dimensions** table join to show the join to the **On-hand inventory** table.</span></span>
1. <span data-ttu-id="a26de-148">Velg **Lagerdimensjoner** og velg deretter **Legg til tabellsammenkobling**.</span><span class="sxs-lookup"><span data-stu-id="a26de-148">Select **Inventory dimensions**, and then select **Add table join**.</span></span>
1. <span data-ttu-id="a26de-149">I listen over tabeller som vises i **Relasjon**-kolonnen, velger du **Nummerskilt (nummerskilt)**.</span><span class="sxs-lookup"><span data-stu-id="a26de-149">In the list of tables that appears, in the **Relation** column, select **License plate (License plate)**.</span></span> <span data-ttu-id="a26de-150">Velg deretter **Velg** for å legge til **Nummerskilt** i **Lagerdimensjoner**-tabellsammenkoblingen.</span><span class="sxs-lookup"><span data-stu-id="a26de-150">Then select **Select** to add **License plate** to the **Inventory dimensions** table join.</span></span>
1. <span data-ttu-id="a26de-151">Mens **Nummerskilt** fremdeles er valgt, velger du **Legg til tabellsammenkobling**.</span><span class="sxs-lookup"><span data-stu-id="a26de-151">While **License plate** is still selected, select **Add table join**.</span></span>
1. <span data-ttu-id="a26de-152">I listen over tabeller som vises i **Relasjon**-kolonnen, velger du **Nummerskiltplassering på lokasjon (nummerskilt)**.</span><span class="sxs-lookup"><span data-stu-id="a26de-152">In the list of tables that appears, in the **Relation** column, select **Location license plate positioning (License plate)**.</span></span> <span data-ttu-id="a26de-153">Velg deretter **Velg** for å legge til **Nummerskiltplassering på lokasjon** i **Lagerdimensjoner**-tabellsammekoblingen.</span><span class="sxs-lookup"><span data-stu-id="a26de-153">Then select **Select** to add **Location license plate positioning** to the **Inventory dimensions** table join.</span></span>

    <span data-ttu-id="a26de-154">![Tabellsammenkoblinger](media/LpTableJoin.png "Tabellsammenkoblinger")</span><span class="sxs-lookup"><span data-stu-id="a26de-154">![Table joins](media/LpTableJoin.png "Table joins")</span></span>

1. <span data-ttu-id="a26de-155">Velg **OK** for å bekrefte de oppdaterte, sammenkoblede tabellene og lukke redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="a26de-155">Select **OK** to confirm the updated joined tables and close the query editor.</span></span>
1. <span data-ttu-id="a26de-156">I hurtigfanen **Lokasjonsdirektivhandlinger** velger du **Rediger spørring** på nytt for å åpne dialogboksen for redigeringsprogram for spørring igjen.</span><span class="sxs-lookup"><span data-stu-id="a26de-156">On the **Location Directive Actions** FastTab, select **Edit query** again to reopen to the query editor.</span></span>
1. <span data-ttu-id="a26de-157">På **Område**-fanen velger du **Legg til** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="a26de-157">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="a26de-158">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a26de-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a26de-159">**Tabell:** *Nummerskiltplassering på lokasjon*</span><span class="sxs-lookup"><span data-stu-id="a26de-159">**Table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="a26de-160">**Avledet tabell:** *Nummerskiltplassering på lokasjon*</span><span class="sxs-lookup"><span data-stu-id="a26de-160">**Derived table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="a26de-161">**Felt:** *LP-plassering*</span><span class="sxs-lookup"><span data-stu-id="a26de-161">**Field:** *LP Position*</span></span>
    - <span data-ttu-id="a26de-162">**Kriterier:** *1*</span><span class="sxs-lookup"><span data-stu-id="a26de-162">**Criteria:** *1*</span></span>

    <span data-ttu-id="a26de-163">![Nytt område](media/LpPositionCriteria.png "Nytt område")</span><span class="sxs-lookup"><span data-stu-id="a26de-163">![New range](media/LpPositionCriteria.png "New range")</span></span>

1. <span data-ttu-id="a26de-164">Velg **OK** for å bekrefte endringene og lukke redigeringsprogrammet for spørring.</span><span class="sxs-lookup"><span data-stu-id="a26de-164">Select **OK** to confirm your changes and close the query editor.</span></span>

### <a name="set-up-sample-data-for-this-scenario"></a><span data-ttu-id="a26de-165">Konfigurer eksempeldata for dette scenariet</span><span class="sxs-lookup"><span data-stu-id="a26de-165">Set up sample data for this scenario</span></span>

<span data-ttu-id="a26de-166">For dette scenariet må brukeren logge seg på lagermobilappen ved hjelp av en arbeider som er satt opp for lager *61* for å utføre arbeid.</span><span class="sxs-lookup"><span data-stu-id="a26de-166">For this scenario, the user must sign in to the warehousing mobile app by using a worker who is set up for warehouse *61* to perform work.</span></span> <span data-ttu-id="a26de-167">Brukeren må også fullføre transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="a26de-167">The user must also complete transactions.</span></span>

<span data-ttu-id="a26de-168">Siden *Nummerskiltplassering på lokasjon*-funksjonen legger til en ny identifikator for plassering av nummerskilt på en lokasjon, må du først opprette noen data for å støtte scenariet.</span><span class="sxs-lookup"><span data-stu-id="a26de-168">Because the *Location license plate positioning* feature adds a new identifier for license plate positions in a location, you must first create some data to support the scenario.</span></span>

#### <a name="spot-count-the-first-location"></a><span data-ttu-id="a26de-169">Spottelling på første lokasjon</span><span class="sxs-lookup"><span data-stu-id="a26de-169">Spot-count the first location</span></span>

1. <span data-ttu-id="a26de-170">Åpne lagermobilappen og logg på lager *61*.</span><span class="sxs-lookup"><span data-stu-id="a26de-170">Open the warehousing mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="a26de-171">Gå til **Beholdning \> Spottelling**.</span><span class="sxs-lookup"><span data-stu-id="a26de-171">Go to **Inventory \> Spot Counting**.</span></span>
1. <span data-ttu-id="a26de-172">På **Spottelling**-siden setter du **Lokasjon**-feltet til *01A01R1S1B*.</span><span class="sxs-lookup"><span data-stu-id="a26de-172">On the **Spot Counting** page, set the **Location** field to *01A01R1S1B*.</span></span>
1. <span data-ttu-id="a26de-173">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a26de-173">Select **OK**.</span></span>

    <span data-ttu-id="a26de-174">Siden viser lokasjonen du har angitt.</span><span class="sxs-lookup"><span data-stu-id="a26de-174">The page shows the location that you entered.</span></span> <span data-ttu-id="a26de-175">Den viser også følgende melding: Plassering fullført, legge til ny LP eller vare?"</span><span class="sxs-lookup"><span data-stu-id="a26de-175">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="a26de-176">Velg **Oppdater** for å legge til en telling på lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="a26de-176">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="a26de-177">På **Syklustelling: Legg til ny LP eller vare**-siden velger du **Vare**-feltet og angir deretter verdien *A0001*.</span><span class="sxs-lookup"><span data-stu-id="a26de-177">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0001*.</span></span>
1. <span data-ttu-id="a26de-178">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a26de-178">Select **OK**.</span></span>
1. <span data-ttu-id="a26de-179">På **Syklustelling: Legg til ny LP eller vare**-siden velger du **LP**-feltet, og deretter angir du verdien *LP1001* (eller et annet skiltnummer).</span><span class="sxs-lookup"><span data-stu-id="a26de-179">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1001* (or any other license plate number of your choice).</span></span>

    <span data-ttu-id="a26de-180">**Syklustelling: Legg til ny LP eller vare**-siden viser **Nummerskiltplassering 1**.</span><span class="sxs-lookup"><span data-stu-id="a26de-180">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="a26de-181">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a26de-181">Select **OK**.</span></span>

    <span data-ttu-id="a26de-182">Du må nå angi antallet for varen som telles på nummerskiltet.</span><span class="sxs-lookup"><span data-stu-id="a26de-182">You must now specify the quantity of the item that is counted on the license plate.</span></span>

1. <span data-ttu-id="a26de-183">Angi **Antall**-feltet til *10*.</span><span class="sxs-lookup"><span data-stu-id="a26de-183">Set the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="a26de-184">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a26de-184">Select **OK**.</span></span>

    <span data-ttu-id="a26de-185">Siden viser lokasjonen du har angitt.</span><span class="sxs-lookup"><span data-stu-id="a26de-185">The page shows the location that you entered.</span></span> <span data-ttu-id="a26de-186">Den viser også følgende melding: Plassering fullført, legge til ny LP eller vare?"</span><span class="sxs-lookup"><span data-stu-id="a26de-186">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="a26de-187">Velg **Oppdater** for å legge til en ny telling på lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="a26de-187">Select **Refresh** to add another count in the location.</span></span>
1. <span data-ttu-id="a26de-188">På **Syklustelling: Legg til ny LP eller vare**-siden velger du **Vare**-feltet og angir deretter verdien *A0002*.</span><span class="sxs-lookup"><span data-stu-id="a26de-188">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="a26de-189">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a26de-189">Select **OK**.</span></span>
1. <span data-ttu-id="a26de-190">På **Syklustelling: Legg til ny LP eller vare**-siden velger du **LP**-feltet, og deretter angir du verdien *LP1002* (eller eventuelle andre skiltnumre du velger, forutsatt at det er forskjellig fra skiltnummeret du angav tidligere).</span><span class="sxs-lookup"><span data-stu-id="a26de-190">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1002* (or any other license plate number of your choice, provided that it differs from the license plate number that you specified earlier).</span></span>
1. <span data-ttu-id="a26de-191">Endre nummerskiltplasseringen ved å sette feltet **LP-plassering** til *2*.</span><span class="sxs-lookup"><span data-stu-id="a26de-191">Change the license plate position by setting the **LP Position** field to *2*.</span></span>
1. <span data-ttu-id="a26de-192">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a26de-192">Select **OK**.</span></span>
1. <span data-ttu-id="a26de-193">Angi antallet av varen som telles, på nummerskiltet ved å sette **Antall**-feltet til *10*.</span><span class="sxs-lookup"><span data-stu-id="a26de-193">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="a26de-194">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a26de-194">Select **OK**.</span></span>

    <span data-ttu-id="a26de-195">Siden viser lokasjonen du har angitt.</span><span class="sxs-lookup"><span data-stu-id="a26de-195">The page shows the location that you entered.</span></span> <span data-ttu-id="a26de-196">Den viser også følgende melding: Plassering fullført, legge til ny LP eller vare?"</span><span class="sxs-lookup"><span data-stu-id="a26de-196">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="a26de-197">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a26de-197">Select **OK**.</span></span>

<span data-ttu-id="a26de-198">Arbeidet er nå fullført.</span><span class="sxs-lookup"><span data-stu-id="a26de-198">Work is now completed.</span></span>

#### <a name="spot-count-the-second-location"></a><span data-ttu-id="a26de-199">Spottelling på andre lokasjon</span><span class="sxs-lookup"><span data-stu-id="a26de-199">Spot-count the second location</span></span>

1. <span data-ttu-id="a26de-200">På **Spottelling**-siden setter du **Lokasjon**-feltet til *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="a26de-200">On the **Spot Counting** page, set the **Location** field to *01A01R1S2B*.</span></span>
1. <span data-ttu-id="a26de-201">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a26de-201">Select **OK**.</span></span>

    <span data-ttu-id="a26de-202">Siden viser lokasjonen du har angitt.</span><span class="sxs-lookup"><span data-stu-id="a26de-202">The page shows the location that you entered.</span></span> <span data-ttu-id="a26de-203">Den viser også følgende melding: Plassering fullført, legge til ny LP eller vare?"</span><span class="sxs-lookup"><span data-stu-id="a26de-203">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="a26de-204">Velg **Oppdater** for å legge til en telling på lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="a26de-204">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="a26de-205">På **Syklustelling: Legg til ny LP eller vare**-siden velger du **Vare**-feltet og angir deretter verdien *A0002*.</span><span class="sxs-lookup"><span data-stu-id="a26de-205">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="a26de-206">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a26de-206">Select **OK**.</span></span>
1. <span data-ttu-id="a26de-207">På **Syklustelling: Legg til ny LP eller vare**-siden velger du **LP**-feltet, og deretter angir du verdien *LP1003* (eller eventuelle andre skiltnumre du velger, forutsatt at det er forskjellig fra begge skiltnumrene du angav i den forrige prosedyren).</span><span class="sxs-lookup"><span data-stu-id="a26de-207">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1003* (or any other license plate number of your choice, provided that it differs from the both the license plate numbers that you specified in the previous procedure).</span></span>

    <span data-ttu-id="a26de-208">**Syklustelling: Legg til ny LP eller vare**-siden viser **Nummerskiltplassering 1**.</span><span class="sxs-lookup"><span data-stu-id="a26de-208">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="a26de-209">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a26de-209">Select **OK**.</span></span>
1. <span data-ttu-id="a26de-210">Angi antallet av varen som telles, på nummerskiltet ved å sette **Antall**-feltet til *10*.</span><span class="sxs-lookup"><span data-stu-id="a26de-210">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="a26de-211">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a26de-211">Select **OK**.</span></span>

    <span data-ttu-id="a26de-212">Siden viser lokasjonen du har angitt.</span><span class="sxs-lookup"><span data-stu-id="a26de-212">The page shows the location that you entered.</span></span> <span data-ttu-id="a26de-213">Den viser også følgende melding: Plassering fullført, legge til ny LP eller vare?"</span><span class="sxs-lookup"><span data-stu-id="a26de-213">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="a26de-214">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a26de-214">Select **OK**.</span></span>

<span data-ttu-id="a26de-215">Arbeidet er nå fullført.</span><span class="sxs-lookup"><span data-stu-id="a26de-215">Work is now completed.</span></span>

#### <a name="work-details"></a><span data-ttu-id="a26de-216">Arbeidsdetaljer</span><span class="sxs-lookup"><span data-stu-id="a26de-216">Work details</span></span>

> [!NOTE]
> <span data-ttu-id="a26de-217">Spottellinger fra den mobile appen syklustellingsarbeid i Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a26de-217">Spot counts from the mobile app create cycle counting work in Microsoft Dynamics 365.</span></span> <span data-ttu-id="a26de-218">Arbeidet krever at tellingene godtas før de posteres til beholdningen.</span><span class="sxs-lookup"><span data-stu-id="a26de-218">The work requires that the counts be accepted before they are posted to inventory.</span></span>

1. <span data-ttu-id="a26de-219">Logg på Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a26de-219">Sign in to Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="a26de-220">Gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="a26de-220">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="a26de-221">I **Oversikt**-fanen kan du se etter linjene som har følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a26de-221">On the **Overview** tab, look for the lines that have the following values:</span></span>

    - <span data-ttu-id="a26de-222">**Arbeidsordretype:** *Syklustelling*</span><span class="sxs-lookup"><span data-stu-id="a26de-222">**Work order type:** *Cycle counting*</span></span>
    - <span data-ttu-id="a26de-223">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="a26de-223">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="a26de-224">**Arbeidsstatus:** *Venter på gjennomgang*</span><span class="sxs-lookup"><span data-stu-id="a26de-224">**Work status:** *Pending review*</span></span>

    <span data-ttu-id="a26de-225">To arbeids-ID-er skal ha blitt opprettet for disse linjene.</span><span class="sxs-lookup"><span data-stu-id="a26de-225">Two work IDs should have been created for these lines.</span></span> <span data-ttu-id="a26de-226">Tellingene for begge disse arbeids-ID-ene må godtas.</span><span class="sxs-lookup"><span data-stu-id="a26de-226">The counts for both these work IDs must be accepted.</span></span>

1. <span data-ttu-id="a26de-227">I rutenettet velger du den første arbeids-ID-en for *Syklustelling*-arbeidsordretypen.</span><span class="sxs-lookup"><span data-stu-id="a26de-227">In the grid, select the first work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="a26de-228">Velg **Syklustelling** i gruppen **Arbeid** i fanen **Arbeid** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a26de-228">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="a26de-229">To linjer vises, én for hver vare og hvert nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="a26de-229">Two lines are shown, one for each item and license plate.</span></span> <span data-ttu-id="a26de-230">Verdiene i feltene **Opptalt antall**, **Lokasjon**, **Nummerskilt** og **Vare** må være i samsvar med opptellingsoppføringene du opprettet på den mobile enheten.</span><span class="sxs-lookup"><span data-stu-id="a26de-230">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span> <span data-ttu-id="a26de-231">Hvis noen av disse feltene ikke er synlige, velger du **Vis dimensjoner** i handlingsruten for å legge dem til i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="a26de-231">If any of these fields aren't visible, select **Display dimensions** on the Action Pane to add them to the grid.</span></span>

1. <span data-ttu-id="a26de-232">Velg begge linjene.</span><span class="sxs-lookup"><span data-stu-id="a26de-232">Select both lines.</span></span>
1. <span data-ttu-id="a26de-233">Klikk på **Godta telling** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a26de-233">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="a26de-234">Du får meldingen Postering – journal.</span><span class="sxs-lookup"><span data-stu-id="a26de-234">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="a26de-235">Velg **Meldingsdetaljer** for å vise det posterte journalnummeret.</span><span class="sxs-lookup"><span data-stu-id="a26de-235">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="a26de-236">Lukk meldingsdetaljene.</span><span class="sxs-lookup"><span data-stu-id="a26de-236">Close the message details.</span></span>
1. <span data-ttu-id="a26de-237">Oppdater **Arbeid**-siden.</span><span class="sxs-lookup"><span data-stu-id="a26de-237">Refresh the **Work** page.</span></span>

    <span data-ttu-id="a26de-238">Den første arbeids-ID-en er lukket og vises ikke lenger.</span><span class="sxs-lookup"><span data-stu-id="a26de-238">The first work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="a26de-239">Hvis du vil vise lukket arbeid, merker du av for **Vis lukket** over rutenettet.</span><span class="sxs-lookup"><span data-stu-id="a26de-239">To view closed work, select the **Show closed** check box above the grid.</span></span>

    <span data-ttu-id="a26de-240">Du vil nå godta arbeidet for nummerskiltet i *01A01R1S2B*-lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="a26de-240">You will now accept the work for the license plate in the *01A01R1S2B* location.</span></span>

1. <span data-ttu-id="a26de-241">I rutenettet velger du den andre arbeids-ID-en for *Syklustelling*-arbeidsordretypen på **Oversikt**-fanen.</span><span class="sxs-lookup"><span data-stu-id="a26de-241">On the **Overview** tab, select the second work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="a26de-242">Velg **Syklustelling** i gruppen **Arbeid** i fanen **Arbeid** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a26de-242">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="a26de-243">Det vises en linje for varen og nummerskiltet.</span><span class="sxs-lookup"><span data-stu-id="a26de-243">One line is shown, for the item and license plate.</span></span> <span data-ttu-id="a26de-244">Verdiene i feltene **Opptalt antall**, **Lokasjon**, **Nummerskilt** og **Vare** må være i samsvar med opptellingsoppføringene du opprettet på den mobile enheten.</span><span class="sxs-lookup"><span data-stu-id="a26de-244">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span>

1. <span data-ttu-id="a26de-245">Velg linjen.</span><span class="sxs-lookup"><span data-stu-id="a26de-245">Select the line.</span></span>
1. <span data-ttu-id="a26de-246">Klikk på **Godta telling** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a26de-246">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="a26de-247">Du får meldingen Postering – journal.</span><span class="sxs-lookup"><span data-stu-id="a26de-247">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="a26de-248">Velg **Meldingsdetaljer** for å vise det posterte journalnummeret.</span><span class="sxs-lookup"><span data-stu-id="a26de-248">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="a26de-249">Lukk meldingsdetaljene.</span><span class="sxs-lookup"><span data-stu-id="a26de-249">Close the message details.</span></span>
1. <span data-ttu-id="a26de-250">Oppdater **Arbeid**-siden.</span><span class="sxs-lookup"><span data-stu-id="a26de-250">Refresh the **Work** page.</span></span>

    <span data-ttu-id="a26de-251">Den andre arbeids-ID-en er lukket og vises ikke lenger.</span><span class="sxs-lookup"><span data-stu-id="a26de-251">The second work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="a26de-252">Hvis du vil vise lukket arbeid, merker du av for **Vis lukket** over rutenettet.</span><span class="sxs-lookup"><span data-stu-id="a26de-252">To view closed work, select the **Show closed** check box above the grid.</span></span>

#### <a name="on-hand-by-location"></a><span data-ttu-id="a26de-253">Beholdning etter lokasjon</span><span class="sxs-lookup"><span data-stu-id="a26de-253">On-hand by location</span></span>

1. <span data-ttu-id="a26de-254">Gå til **Lagerstyring \> Forespørsler og rapporter \> Beholdning etter lokasjon**.</span><span class="sxs-lookup"><span data-stu-id="a26de-254">Go to **Warehouse management \> Inquiries and reports \> On-hand by location**.</span></span>
1. <span data-ttu-id="a26de-255">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a26de-255">Set the following values:</span></span>

    - <span data-ttu-id="a26de-256">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="a26de-256">**Site:** *6*</span></span>
    - <span data-ttu-id="a26de-257">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="a26de-257">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="a26de-258">**Oppdater på tvers av lokasjoner:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="a26de-258">**Refresh across locations:** *Yes*</span></span>

1. <span data-ttu-id="a26de-259">Merk at lokasjonen *01A01R1S1B* har to nummerskilt:</span><span class="sxs-lookup"><span data-stu-id="a26de-259">Notice that location *01A01R1S1B* has two license plates:</span></span>

    - <span data-ttu-id="a26de-260">**A0001**, der **LP-posisjon**-feltet er satt til *1*</span><span class="sxs-lookup"><span data-stu-id="a26de-260">**A0001**, where the **LP Position** field is set to *1*</span></span>
    - <span data-ttu-id="a26de-261">**A0002**, der **LP-posisjon**-feltet er satt til *2*</span><span class="sxs-lookup"><span data-stu-id="a26de-261">**A0002**, where the **LP Position** field is set to *2*</span></span>

1. <span data-ttu-id="a26de-262">Merk at lokasjonen *01A01R1S2B* har ett nummerskilt:</span><span class="sxs-lookup"><span data-stu-id="a26de-262">Notice that location *01A01R1S2B* has one license plate:</span></span>

    - <span data-ttu-id="a26de-263">**A0002**, der **LP-posisjon**-feltet er satt til *1*</span><span class="sxs-lookup"><span data-stu-id="a26de-263">**A0002**, where the **LP Position** field is set to *1*</span></span>

### <a name="sales-order-scenario"></a><span data-ttu-id="a26de-264">Salgsordrescenario</span><span class="sxs-lookup"><span data-stu-id="a26de-264">Sales order scenario</span></span>

<span data-ttu-id="a26de-265">Nå når funksjonen *Nummerskiltplassering på lokasjon* er konfigurert, og beholdningen er klargjort, må du opprette en salgsordre for å generere plukking av arbeid som vil styre lagerarbeideren for å plukke vare *A0002* fra lagerlokasjonen der pall-ID-en er i posisjon *1*.</span><span class="sxs-lookup"><span data-stu-id="a26de-265">Now that the *Location license plate positioning* feature has been set up, and the inventory has been staged, you must create a sales order to generate picking work that will direct the warehouse worker to pick item *A0002* from the inventory location where the pallet ID is in position *1*.</span></span>

1. <span data-ttu-id="a26de-266">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a26de-266">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a26de-267">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a26de-267">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a26de-268">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a26de-268">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a26de-269">**Kundekonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="a26de-269">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="a26de-270">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="a26de-270">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="a26de-271">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a26de-271">Select **OK**.</span></span>
1. <span data-ttu-id="a26de-272">Det legges til en ny linje i rutenettet på **Salgsordrelinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="a26de-272">A new line is added to the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="a26de-273">På denne nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="a26de-273">On this new line, set the following values:</span></span>

    - <span data-ttu-id="a26de-274">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="a26de-274">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="a26de-275">**Antall:** *1*</span><span class="sxs-lookup"><span data-stu-id="a26de-275">**Quantity:** *1*</span></span>

1. <span data-ttu-id="a26de-276">Velg **Reservasjon** på **Beholdning**-menyen over rutenettet.</span><span class="sxs-lookup"><span data-stu-id="a26de-276">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="a26de-277">På **Reservasjon**-siden, i handlingspanelet, velger du **Reserver parti** for å reservere beholdning for ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="a26de-277">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve inventory for the order line.</span></span>
1. <span data-ttu-id="a26de-278">Lukk **Reservasjon**-siden.</span><span class="sxs-lookup"><span data-stu-id="a26de-278">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="a26de-279">Velg **Frigi til lager** i gruppen **Handlinger** i fanen **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a26de-279">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="a26de-280">Du mottar en informasjonsmelding som viser bølge-ID og forsendelses-ID-er som er opprettet for ordren.</span><span class="sxs-lookup"><span data-stu-id="a26de-280">You receive an informational message that indicates the wave ID and shipment ID that were created for the order.</span></span>

1. <span data-ttu-id="a26de-281">I **Salgsordrelinjer**-hurtigfanen, på **Lager**-menyen over rutenettet, velger du **Arbeidsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="a26de-281">On the **Sales order lines** FastTab, on the **Warehouse** menu above the grid, select **Work details**.</span></span>
1. <span data-ttu-id="a26de-282">**Arbeid**-siden vises og viser arbeidet som ble opprettet for salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="a26de-282">The **Work** page appears and shows the work that was created for the sales line.</span></span> <span data-ttu-id="a26de-283">Noter deg arbeids-ID-en som vises.</span><span class="sxs-lookup"><span data-stu-id="a26de-283">Make a note of the work ID that is shown.</span></span>

### <a name="sales-picking-scenario"></a><span data-ttu-id="a26de-284">Salgsplukkscenario</span><span class="sxs-lookup"><span data-stu-id="a26de-284">Sales picking scenario</span></span>

1. <span data-ttu-id="a26de-285">Åpne mobilappen og logg på lager *61*.</span><span class="sxs-lookup"><span data-stu-id="a26de-285">Open the mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="a26de-286">Gå til **Utgående \> Salgsplukking**.</span><span class="sxs-lookup"><span data-stu-id="a26de-286">Go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="a26de-287">På **Skann en arbeids-ID/nummerskilt-ID**-siden velger du **ID**-feltet og angir deretter arbeids-ID-en fra salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="a26de-287">On the **Scan a work ID / license plate ID** page, select the **ID** field, and then enter the work ID from the sales line.</span></span>
1. <span data-ttu-id="a26de-288">Legg merke til at plukkarbeidet leder deg til å plukke vare *A0002* fra lokasjon *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="a26de-288">Notice that the picking work directs you to pick item *A0002* from location *01A01R1S2B*.</span></span> <span data-ttu-id="a26de-289">Du får denne instruksjonen fordi vare *A0002* er på et nummerskilt som er på plassering *1* på den lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="a26de-289">You receive this instruction because item *A0002* is on a license plate that is in position *1* in that location.</span></span>

    <span data-ttu-id="a26de-290">![Plassering 1-lokasjon](media/LocationLicensePlatePositioning.png "Plassering 1-lokasjon")</span><span class="sxs-lookup"><span data-stu-id="a26de-290">![Position 1 location](media/LocationLicensePlatePositioning.png "Position 1 location")</span></span>

1. <span data-ttu-id="a26de-291">Angi nummerskilt-ID-en du opprettet for lokasjonen, og følg deretter instruksjonene for å velge salgsordren.</span><span class="sxs-lookup"><span data-stu-id="a26de-291">Enter the license plate ID that you created for the location, and then follow the prompts to pick the sales order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]