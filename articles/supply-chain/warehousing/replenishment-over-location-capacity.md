---
title: Etterfylling over lokasjonskapasitet
description: Dette emnet inneholder informasjon om funksjonen Etterfylling over lokasjonskapasitet. Denne funksjonen aktiverer alt etterfyllingsarbeid som vil være nødvendig å opprette for dagen, og administrerer tilgjengelighet for etterfyllingsarbeidet for å sikre at plukklokasjonen ikke går ut av beholdning eller går over kapasitet.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 309df56671bf258e1669ae6d5393de01e2b500f0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823245"
---
# <a name="replenishment-over-location-capacity"></a><span data-ttu-id="887f4-104">Etterfylling over lokasjonskapasitet</span><span class="sxs-lookup"><span data-stu-id="887f4-104">Replenishment over location capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="887f4-105">Noen lagre med nøy volum eller plassbegrensning må levere mer antall av en vare på en dag enn det er plass til i plukklokasjonen.</span><span class="sxs-lookup"><span data-stu-id="887f4-105">Some high-volume or space-constrained warehouses must ship more quantity of an item in a day than will fit in the picking location.</span></span> <span data-ttu-id="887f4-106">Funksjonen *v* aktiverer alt etterfyllingsarbeid som vil være nødvendig å opprette for dagen, og administrerer tilgjengelighet for etterfyllingsarbeidet for å sikre at plukklokasjonen ikke går ut av beholdning eller går over kapasitet..</span><span class="sxs-lookup"><span data-stu-id="887f4-106">The *Replenishment over location capacity* feature enables all replenishment work that will be required for the day to be created and manages availability of that replenishment work to ensure that the picking location neither runs out of inventory nor goes above capacity.</span></span>

<span data-ttu-id="887f4-107">Funksjonen gjør det mulig å opprette mer etterfyllingsarbeid enn det er plass til i en lokasjon, og det forventes at etterfyllingsarbeid ikke fullføres når lokasjonen er full.</span><span class="sxs-lookup"><span data-stu-id="887f4-107">The feature enables more replenishment work to be created than will fit in a location, and it blocks replenishment work from being completed when the location is full.</span></span> <span data-ttu-id="887f4-108">Når beholdningen plukkstedet faller under en konfigurerbar terskel, gjøres mer etterfyllingsarbeid tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="887f4-108">As inventory in the picking location drops below a configurable threshold, more replenishment work is made available.</span></span>

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a><span data-ttu-id="887f4-109">Aktivere funksjonen Etterfylling over lokasjonskapasitet</span><span class="sxs-lookup"><span data-stu-id="887f4-109">Turn on the Replenishment over location capacity feature</span></span>

<span data-ttu-id="887f4-110">For å gjøre denne funksjonen tilgjengelig aktiverer du følgende funksjoner i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i denne rekkefølgen):</span><span class="sxs-lookup"><span data-stu-id="887f4-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in this order):</span></span>

1. <span data-ttu-id="887f4-111">Organisasjonsomfattende arbeidsblokkering</span><span class="sxs-lookup"><span data-stu-id="887f4-111">Organization-wide work blocking</span></span>
1. <span data-ttu-id="887f4-112">Etterfylling over lokasjonskapasitet</span><span class="sxs-lookup"><span data-stu-id="887f4-112">Replenishment over location capacity</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="887f4-113">Konfigurer funksjonen for eksempelscenarioet</span><span class="sxs-lookup"><span data-stu-id="887f4-113">Set up the feature for the example scenario</span></span>

<span data-ttu-id="887f4-114">Denne delen inneholder retningslinjer og et eksempel som viser hvordan du definerer denne funksjonen og klargjør eksempeldata foreksempel scenarioet som er oppgitt senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="887f4-114">This section provides guidelines and an example that shows how to set up this feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="enable-sample-data"></a><span data-ttu-id="887f4-115">Aktivere eksempeldata</span><span class="sxs-lookup"><span data-stu-id="887f4-115">Enable sample data</span></span>

<span data-ttu-id="887f4-116">For å arbeide deg gjennom dette [eksempelscenarioet](#example-scenario) ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert.</span><span class="sxs-lookup"><span data-stu-id="887f4-116">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="887f4-117">Du må også velge den juridiske enheten **USMF** før du begynner.</span><span class="sxs-lookup"><span data-stu-id="887f4-117">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="location-profile"></a><span data-ttu-id="887f4-118">Lokasjonsprofil</span><span class="sxs-lookup"><span data-stu-id="887f4-118">Location profile</span></span>

<span data-ttu-id="887f4-119">Aktiver funksjonaliteten for Etterfylling over kapasitet på lokasjonsprofilen.</span><span class="sxs-lookup"><span data-stu-id="887f4-119">Enable the replenish over capacity functionality on the location profile.</span></span>

1. <span data-ttu-id="887f4-120">Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="887f4-120">Go to **Warehouse management \> Setup \> Warehouse \> Locations profiles**.</span></span>
1. <span data-ttu-id="887f4-121">Velg **PLUK-06** i venstre rute.</span><span class="sxs-lookup"><span data-stu-id="887f4-121">In the left pane, select **PICK-06**.</span></span>
1. <span data-ttu-id="887f4-122">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="887f4-122">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="887f4-123">Angi følgende verdier på **Etterfylling**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="887f4-123">On the **Replenishment** FastTab, set the following values:</span></span>

    - <span data-ttu-id="887f4-124">**Overskrid lokasjonskapasitet:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="887f4-124">**Exceed Location Capacity:** *Yes*</span></span>

        <span data-ttu-id="887f4-125">Når dette er aktivert, er det tillatt for etterfyllingsarbeid å overskride maksimumskapasiteten til lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="887f4-125">When enabled, the maximum capacity of the location will be allowed to be exceeded by replenishment work.</span></span> <span data-ttu-id="887f4-126">Dette gjør det også mulig med andre felt på hurtigfanen **Etterfylling**.</span><span class="sxs-lookup"><span data-stu-id="887f4-126">This also enables other fields on the **Replenishment** FastTab.</span></span>

    - <span data-ttu-id="887f4-127">**Terskeltype for arbeidstilgjengelighet:** *Antall*</span><span class="sxs-lookup"><span data-stu-id="887f4-127">**Work availability threshold type:** *Quantity*</span></span>

        <span data-ttu-id="887f4-128">Dette feltet definerer metoden som brukes til å fastslå når mer arbeid skal frigis.</span><span class="sxs-lookup"><span data-stu-id="887f4-128">This field defines the method that is used to determine when more work should be released.</span></span> <span data-ttu-id="887f4-129">Du kan frigi etter antall eller prosent:</span><span class="sxs-lookup"><span data-stu-id="887f4-129">You can release by either quantity or a percentage:</span></span>

        - <span data-ttu-id="887f4-130">*Prosent* – Velg dette alternativet for å bruke prosentkapasitet som er basert på beholdningsgrenser eller volummål.</span><span class="sxs-lookup"><span data-stu-id="887f4-130">*Percent* – Select this option to use percentage capacity that is based on stocking limits or volumetrics.</span></span> <span data-ttu-id="887f4-131">Hvis du velger dette alternativet, aktiveres feltet **Overflytprosent**, og de to antallsrelaterte feltene, **Overflytantall** og **Overflytenhet**, deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="887f4-131">Selecting this option enables the **Overflow percentage** field, and disables the two quantity related fields,  **Overflow quantity** and **Overflow unit**.</span></span>

            <span data-ttu-id="887f4-132">Du kan bruke dette alternativet hvis plukklokasjonene bruker volummål.</span><span class="sxs-lookup"><span data-stu-id="887f4-132">You can use this option if the picking locations use volumetrics.</span></span>

            <span data-ttu-id="887f4-133">Hvis det er merket av for dette alternativet, setter du feltet **Overflytprosent** til prosenten der mer etterfyllingsarbeid blir gjort tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="887f4-133">If this option is selected, set the **Overflow percentage** field to the percentage at which more replenishment work will be made available.</span></span>

        - <span data-ttu-id="887f4-134">*Antall* – Velg dette alternativet for å bruke en bestemt antallsverdi.</span><span class="sxs-lookup"><span data-stu-id="887f4-134">*Quantity* – Select this option to use a specific quantity value.</span></span> <span data-ttu-id="887f4-135">Hvis du velger dette alternativet, deaktiveres feltet **Overflytprosent**, og de feltene **Overflytantall** og **Overflytenhet** aktiveres.</span><span class="sxs-lookup"><span data-stu-id="887f4-135">Selecting this option disables the **Overflow percentage** field and enables **Overflow quantity** and **Overflow unit** fields.</span></span>

            <span data-ttu-id="887f4-136">Bruk dette alternativet når du ikke bruker volummål for lokasjoner som etterfylles, eller når du har konsekvente mengder der du vil at mer beholdning skal hentes til lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="887f4-136">Use this option when you aren't using volumetrics for the locations that are being replenished, or when you have consistent quantities at which you want more inventory to be brought to the location.</span></span>

           <span data-ttu-id="887f4-137">Hvis dette alternativet er valgt, angir du feltene **Overflytantall** og **Overflytenhet** til antallet og enheten der mer etterfyllings arbeid skal gjøres tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="887f4-137">If this option is selected, set the **Overflow quantity** and **Overflow unit** fields to the quantity and unit at which more replenishment work will be made available.</span></span>

    - <span data-ttu-id="887f4-138">**Overflytantall:** *0,65*</span><span class="sxs-lookup"><span data-stu-id="887f4-138">**Overflow quantity:** *0.65*</span></span>

        <span data-ttu-id="887f4-139">Dette feltet definerer antallet lokasjonen overflyter i.</span><span class="sxs-lookup"><span data-stu-id="887f4-139">This field defines the quantity at which the location overflows.</span></span>

        <span data-ttu-id="887f4-140">Arbeid er tilgjengelig så lenge summen av beholdningsantall i lokasjonen og arbeidsmengde er under denne verdien.</span><span class="sxs-lookup"><span data-stu-id="887f4-140">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this value.</span></span> <span data-ttu-id="887f4-141">Etterfyllingsantall over denne verdien blir blokkert, og blokkeringen må oppheves manuelt.</span><span class="sxs-lookup"><span data-stu-id="887f4-141">Any replenishment work above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="887f4-142">Lokasjonsbeholdningsgrenser vurderes når arbeidsantallet beregnes.</span><span class="sxs-lookup"><span data-stu-id="887f4-142">Location stocking limits are considered when the work quantity is calculated.</span></span>

    - <span data-ttu-id="887f4-143">**Overflytenhet:** *PL*</span><span class="sxs-lookup"><span data-stu-id="887f4-143">**Overflow unit:** *PL*</span></span>

        <span data-ttu-id="887f4-144">Dette feltet definerer enheten som er knyttet til overflytantallet.</span><span class="sxs-lookup"><span data-stu-id="887f4-144">This field defines the unit that is associated with the overflow quantity.</span></span>

        <span data-ttu-id="887f4-145">I dette tilfellet vil mer etterfyllingsarbeid gjøres tilgjengelig når lokasjonen går ned til 0,65 paller (PL).</span><span class="sxs-lookup"><span data-stu-id="887f4-145">In this case, more replenishment work will be made available when the location gets down to 0.65 pallet (PL).</span></span>

    - <span data-ttu-id="887f4-146">**Overflytprosent**</span><span class="sxs-lookup"><span data-stu-id="887f4-146">**Overflow percentage**</span></span>

        <span data-ttu-id="887f4-147">Dette feltet definerer prosenten der lokasjonen overflyter.</span><span class="sxs-lookup"><span data-stu-id="887f4-147">This field defines the percentage at which the location overflows.</span></span>

        <span data-ttu-id="887f4-148">Arbeid er tilgjengelig så lenge summen av beholdningsantall i lokasjonen og arbeidsmengde er under denne prosentverdien.</span><span class="sxs-lookup"><span data-stu-id="887f4-148">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this percentage.</span></span> <span data-ttu-id="887f4-149">Prosent for etterfyllingsantall over denne verdien blir blokkert, og blokkeringen må oppheves manuelt.</span><span class="sxs-lookup"><span data-stu-id="887f4-149">Any replenishment work quantity percentage above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="887f4-150">Lokasjonsbeholdningsgrenser vurderes når arbeidsantallsprosenten beregnes.</span><span class="sxs-lookup"><span data-stu-id="887f4-150">Location stocking limits are considered when the work quantity percentage is calculated.</span></span> <span data-ttu-id="887f4-151">Hvis det ikke er definert noen lagergrenser for lokasjoner, beregnes arbeidsmengdeprosenten etter volum hvis volumbegrensninger er definert for lokasjonsprofilen.</span><span class="sxs-lookup"><span data-stu-id="887f4-151">If no location stocking limits are defined, the work quantity percentage is calculated by volume if volume constraints are defined for the location profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="887f4-152">Hvis du bruker demonstrasjonsdataene for den juridiske enheten **USMF** og tidligere har aktivert funksjonen *Nummerskiltposisjonering for lokasjon*, må du deaktivere innstillingen **Aktiver nummerskiltposisjonering** for lokasjonsprofilen **BULK-06** for å fullføre trinnene for mobil i eksempelscenarioet.</span><span class="sxs-lookup"><span data-stu-id="887f4-152">If you're using the demo data for the **USMF** legal entity and previously turned on the *Location license plate positioning* feature, you must turn off the **Enable license plate positioning** setting for the **BULK-06** location profile to complete the mobile steps in the example scenario.</span></span>

### <a name="wave-step-code"></a><span data-ttu-id="887f4-153">Bølgetrinnkode</span><span class="sxs-lookup"><span data-stu-id="887f4-153">Wave step code</span></span>

> [!NOTE]
> <span data-ttu-id="887f4-154">Hvis du vil definere en bølgetrinnskode som beskrevet her, kan det være at du først må bruke [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktivere funksjonen *Organisasjonsomfattende bølgetrinnkode*.</span><span class="sxs-lookup"><span data-stu-id="887f4-154">To set up a wave step code as described here, you might first have to use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named *Organization wide wave step code*.</span></span>

1. <span data-ttu-id="887f4-155">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgetrinnkoder**.</span><span class="sxs-lookup"><span data-stu-id="887f4-155">Go to **Warehouse Management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="887f4-156">Velg **Ny**, og angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="887f4-156">Select **New**, and set the following values:</span></span>

    - <span data-ttu-id="887f4-157">**Bølgetrinnkode:** *Etterfyll*</span><span class="sxs-lookup"><span data-stu-id="887f4-157">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="887f4-158">**Bølgetrinnbeskrivelse:** *Etterfylling*</span><span class="sxs-lookup"><span data-stu-id="887f4-158">**Wave step description:** *Replenishment*</span></span>
    - <span data-ttu-id="887f4-159">**Bølgetrinntype:** *Etterfylling*</span><span class="sxs-lookup"><span data-stu-id="887f4-159">**Wave step type:** *Replenishment*</span></span>

1. <span data-ttu-id="887f4-160">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="887f4-160">Select **Save**.</span></span>

### <a name="replenishment-template"></a><span data-ttu-id="887f4-161">Etterfyllingsmal</span><span class="sxs-lookup"><span data-stu-id="887f4-161">Replenishment template</span></span>

<span data-ttu-id="887f4-162">Etterfyllingsmaler er et sett med regler som bestemmer når og hvordan en lokasjon fylles.</span><span class="sxs-lookup"><span data-stu-id="887f4-162">Replenishment templates are a set of rules that control when and how a location is replenished.</span></span>

1. <span data-ttu-id="887f4-163">Gå til **Lagerstyring \> Oppsett \> Etterfylling \> Etterfyllingsmaler**.</span><span class="sxs-lookup"><span data-stu-id="887f4-163">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="887f4-164">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="887f4-164">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="887f4-165">I **Oversikt**-delen velger du linjen der feltet **Etterfyllingsmal** er satt til *Behovsbasert etterfylling*.</span><span class="sxs-lookup"><span data-stu-id="887f4-165">In the **Overview** section, select the line where the **Replenish template** field is set to *Demand replenish*.</span></span>
1. <span data-ttu-id="887f4-166">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="887f4-166">Set the following values:</span></span>

    - <span data-ttu-id="887f4-167">**Bølgetrinnkode:** *Etterfyll*</span><span class="sxs-lookup"><span data-stu-id="887f4-167">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="887f4-168">**Tillat at bølgebehov bruker ikke-reservert antall:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="887f4-168">**Allow wave demand to use unreserved quantities:** *Yes*</span></span>

1. <span data-ttu-id="887f4-169">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="887f4-169">Select **Save**.</span></span>

### <a name="wave-template"></a><span data-ttu-id="887f4-170">Bølgemal</span><span class="sxs-lookup"><span data-stu-id="887f4-170">Wave template</span></span>

1. <span data-ttu-id="887f4-171">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.</span><span class="sxs-lookup"><span data-stu-id="887f4-171">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="887f4-172">I den venstre ruten setter du **Bølgemaltype**-feltet til *Forsendelse*.</span><span class="sxs-lookup"><span data-stu-id="887f4-172">In the left pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="887f4-173">Velg malen **61 Forsendelse** fra listen.</span><span class="sxs-lookup"><span data-stu-id="887f4-173">Select template **61 Shipping** in the list.</span></span>
1. <span data-ttu-id="887f4-174">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="887f4-174">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="887f4-175">I hurtigfanen **Generelt** setter du alternativet **Automatiser frigivelse av etterfyllingsarbeid** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="887f4-175">On the **General** FastTab, set the **Automate replenishment work release** option to *Yes*.</span></span>

    <span data-ttu-id="887f4-176">Sett dette alternativet til *Ja* for å opprette behovsbasert etterfyllingarbeid og frigi det automatisk.</span><span class="sxs-lookup"><span data-stu-id="887f4-176">Set this option to *Yes* to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="887f4-177">Du må legge til etterfyllingsbølgemetoden i bølgemalen og opprette en mal for etterfylling av typen **Bølgebehov**.</span><span class="sxs-lookup"><span data-stu-id="887f4-177">You must add the replenishment wave method to the wave template and create a replenishment template of the **Wave demand** type.</span></span> <span data-ttu-id="887f4-178">Angi en mal for etterfylling på siden **Etterfyllingsmaler**.</span><span class="sxs-lookup"><span data-stu-id="887f4-178">Set up a replenishment template on the **Replenishment templates** page.</span></span> <span data-ttu-id="887f4-179">Hvis du vil definere en etterfyllingsmal, må du legge til etterfyllingsmetoden i bølgemalen.</span><span class="sxs-lookup"><span data-stu-id="887f4-179">To set up a replenishment template, you must add the replenish method to the wave template.</span></span>

1. <span data-ttu-id="887f4-180">På hurtigfanen **Metoder**, i kolonnen **Valgte metoder**, finner du følgende linje:</span><span class="sxs-lookup"><span data-stu-id="887f4-180">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="887f4-181">**Metodenavn:** *etterfylle*</span><span class="sxs-lookup"><span data-stu-id="887f4-181">**Method name:** *replenish*</span></span>
    - <span data-ttu-id="887f4-182">**Navn:** *Etterfylling*</span><span class="sxs-lookup"><span data-stu-id="887f4-182">**Name:** *Replenishment*</span></span>

1. <span data-ttu-id="887f4-183">Sett feltet **Bølgetrinnkode** for denne linjen til *Etterfyll*.</span><span class="sxs-lookup"><span data-stu-id="887f4-183">Set the **Wave step code** field for this line to *Replen*.</span></span>
1. <span data-ttu-id="887f4-184">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="887f4-184">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="887f4-185">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="887f4-185">Example scenario</span></span>

<span data-ttu-id="887f4-186">Etter at du har gjort alle de tidligere beskrevne eksempeldataene tilgjengelige og konfigurert dem, kan du arbeide deg gjennom dette scenariet for å prøve ut funksjonen *Etterfylling over lokasjonskapasitet*.</span><span class="sxs-lookup"><span data-stu-id="887f4-186">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Replenishment over location capacity* feature.</span></span> <span data-ttu-id="887f4-187">Verdiene som vises i dette scenariet, antar at du arbeider med standard demonstrasjonsdata, at du har valgt den juridiske enheten **USMF**, og at du klargjorde eksempelpostene som er beskrevet tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="887f4-187">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="887f4-188">Dette scenariet fungerer også som et eksempel som viser hvordan funksjonen kan brukes i et produksjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="887f4-188">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-replenishment-work"></a><span data-ttu-id="887f4-189">Opprett etterfyllingsarbeid</span><span class="sxs-lookup"><span data-stu-id="887f4-189">Create replenishment work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="887f4-190">Opprett salgsordre 1</span><span class="sxs-lookup"><span data-stu-id="887f4-190">Create sales order 1</span></span>

1. <span data-ttu-id="887f4-191">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="887f4-191">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="887f4-192">I handlingsruten velger du **Ny** for å åpne en dialogboks for oppretting av en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="887f4-192">On the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="887f4-193">Angi følgende verdier i dialogboksen:</span><span class="sxs-lookup"><span data-stu-id="887f4-193">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="887f4-194">**Kundekonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="887f4-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="887f4-195">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="887f4-195">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="887f4-196">Velg **OK** for å opprette salgsorden og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="887f4-196">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="887f4-197">Den nye salgsordren åpnes.</span><span class="sxs-lookup"><span data-stu-id="887f4-197">The new sales order is opened.</span></span> <span data-ttu-id="887f4-198">Det inneholder en ny, tom linje på **Salgsordrelinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="887f4-198">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="887f4-199">På denne linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="887f4-199">On this line, set the following values:</span></span>

    - <span data-ttu-id="887f4-200">**Varenummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="887f4-200">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="887f4-201">**Antall:** *40*</span><span class="sxs-lookup"><span data-stu-id="887f4-201">**Quantity:** *40*</span></span>

1. <span data-ttu-id="887f4-202">På hurtigfanen **Salgsordrelinjer** velger du **Beholdning \> Reservasjon**.</span><span class="sxs-lookup"><span data-stu-id="887f4-202">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="887f4-203">På **Reservasjon**-siden velger du **Reserver parti**.</span><span class="sxs-lookup"><span data-stu-id="887f4-203">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="887f4-204">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="887f4-204">Close the page.</span></span>
1. <span data-ttu-id="887f4-205">Velg **Frigi til lager** i fanen **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="887f4-205">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="887f4-206">Du mottar informasjonsmeldinger som viser bølge-ID og forsendelses-ID som er opprettet.</span><span class="sxs-lookup"><span data-stu-id="887f4-206">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="887f4-207">Det opprettes også en etterfyllingsbølge.</span><span class="sxs-lookup"><span data-stu-id="887f4-207">A replenishment wave is also created.</span></span>

    <span data-ttu-id="887f4-208">Du får også en advarsel som sier: "Blokkeringen av arbeids-ID XXXX kan ikke oppheves, fordi den ikke har fullført etterfyllingsarbeid."</span><span class="sxs-lookup"><span data-stu-id="887f4-208">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="887f4-209">Opprett salgsordre 2</span><span class="sxs-lookup"><span data-stu-id="887f4-209">Create sales order 2</span></span>

1. <span data-ttu-id="887f4-210">I handlingsruten på siden **Alle salgsordrer** velger du **Ny** for å åpne en dialogboks for oppretting av en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="887f4-210">On the **All sales orders**, page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="887f4-211">Angi følgende verdi i dialogboksen:</span><span class="sxs-lookup"><span data-stu-id="887f4-211">In the dialog box, set the following value:</span></span>

    - <span data-ttu-id="887f4-212">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="887f4-212">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="887f4-213">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="887f4-213">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="887f4-214">Velg **OK** for å opprette salgsorden og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="887f4-214">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="887f4-215">Den nye salgsordren åpnes.</span><span class="sxs-lookup"><span data-stu-id="887f4-215">The new sales order is opened.</span></span> <span data-ttu-id="887f4-216">Det inneholder en ny, tom linje på **Salgsordrelinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="887f4-216">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="887f4-217">På denne linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="887f4-217">On this line, set the following values:</span></span>

    - <span data-ttu-id="887f4-218">**Varenummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="887f4-218">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="887f4-219">**Antall:** *60*</span><span class="sxs-lookup"><span data-stu-id="887f4-219">**Quantity:** *60*</span></span>

1. <span data-ttu-id="887f4-220">På hurtigfanen **Salgsordrelinjer** velger du **Beholdning \> Reservasjon**.</span><span class="sxs-lookup"><span data-stu-id="887f4-220">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="887f4-221">På **Reservasjon**-siden velger du **Reserver parti**.</span><span class="sxs-lookup"><span data-stu-id="887f4-221">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="887f4-222">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="887f4-222">Close the page.</span></span>
1. <span data-ttu-id="887f4-223">Velg **Frigi til lager** i fanen **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="887f4-223">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="887f4-224">Du mottar informasjonsmeldinger som viser bølge-ID og forsendelses-ID som er opprettet.</span><span class="sxs-lookup"><span data-stu-id="887f4-224">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="887f4-225">Det opprettes også en etterfyllingsbølge.</span><span class="sxs-lookup"><span data-stu-id="887f4-225">A replenishment wave is also created.</span></span>

    <span data-ttu-id="887f4-226">Du får også en advarsel som sier: "Blokkeringen av arbeids-ID XXXX kan ikke oppheves, fordi den ikke har fullført etterfyllingsarbeid."</span><span class="sxs-lookup"><span data-stu-id="887f4-226">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="887f4-227">Opprett salgsordre 3</span><span class="sxs-lookup"><span data-stu-id="887f4-227">Create sales order 3</span></span>

1. <span data-ttu-id="887f4-228">I handlingsruten på siden **Alle salgsordrer** velger du **Ny** for å åpne en dialogboks for oppretting av en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="887f4-228">On the **All sales orders** page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="887f4-229">Angi følgende verdier i dialogboksen:</span><span class="sxs-lookup"><span data-stu-id="887f4-229">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="887f4-230">**Kundekonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="887f4-230">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="887f4-231">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="887f4-231">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="887f4-232">Velg **OK** for å opprette salgsorden og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="887f4-232">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="887f4-233">Den nye salgsordren åpnes.</span><span class="sxs-lookup"><span data-stu-id="887f4-233">The new sales order is opened.</span></span> <span data-ttu-id="887f4-234">Det inneholder en ny, tom linje på **Salgsordrelinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="887f4-234">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="887f4-235">På denne linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="887f4-235">On this line, set the following values:</span></span>

    - <span data-ttu-id="887f4-236">**Varenummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="887f4-236">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="887f4-237">**Antall:** *30*</span><span class="sxs-lookup"><span data-stu-id="887f4-237">**Quantity:** *30*</span></span>

1. <span data-ttu-id="887f4-238">På hurtigfanen **Salgsordrelinjer** velger du **Beholdning \> Reservasjon**.</span><span class="sxs-lookup"><span data-stu-id="887f4-238">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="887f4-239">På **Reservasjon**-siden velger du **Reserver parti**.</span><span class="sxs-lookup"><span data-stu-id="887f4-239">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="887f4-240">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="887f4-240">Close the page.</span></span>
1. <span data-ttu-id="887f4-241">Velg **Frigi til lager** i fanen **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="887f4-241">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="887f4-242">Du mottar informasjonsmeldinger som viser bølge-ID og forsendelses-ID som er opprettet.</span><span class="sxs-lookup"><span data-stu-id="887f4-242">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="887f4-243">Det opprettes også en etterfyllingsbølge.</span><span class="sxs-lookup"><span data-stu-id="887f4-243">A replenishment wave is also created.</span></span>

    <span data-ttu-id="887f4-244">Du får også en advarsel som sier: "Blokkeringen av arbeids-ID XXXX kan ikke oppheves, fordi den ikke har fullført etterfyllingsarbeid."</span><span class="sxs-lookup"><span data-stu-id="887f4-244">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="view-work-details"></a><span data-ttu-id="887f4-245">Vis arbeidsdetaljer</span><span class="sxs-lookup"><span data-stu-id="887f4-245">View work details</span></span>

1. <span data-ttu-id="887f4-246">Gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="887f4-246">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="887f4-247">I **Oversikt**-delen filtrerer du **Lager**-kolonnen for lager *61*.</span><span class="sxs-lookup"><span data-stu-id="887f4-247">In the **Overview** section, filter the **Warehouse** column for warehouse *61*.</span></span>
1. <span data-ttu-id="887f4-248">Du skal se at sju arbeids-ID-er ble opprettet for de tre etterspørselssalgsordrene.</span><span class="sxs-lookup"><span data-stu-id="887f4-248">You should see that seven work IDs were created for the three demand sales orders.</span></span>

    - <span data-ttu-id="887f4-249">Tre av de sju arbeids-ID-ene har **Arbeidsordretype**-verdien *Etterfylling*, og fire har **Arbeidsordretype**-verdien *Salgsordrer*.</span><span class="sxs-lookup"><span data-stu-id="887f4-249">Three of the seven work IDs have a **Work order type** value of *Replenishment*, and four have a **Work order type** value of *Sales orders*.</span></span>
    - <span data-ttu-id="887f4-250">Alle de tre arbeids-ID-ene som har **Arbeidsordretype**-verdien *Etterfylling*, har de samme *Plukk*- og *Plassering*-stedene i **Linjer**-delen:</span><span class="sxs-lookup"><span data-stu-id="887f4-250">All three work IDs that have a **Work order type** value of *Replenishment* have the same *Pick* and *Put* locations in the **Lines** section:</span></span>

        - <span data-ttu-id="887f4-251">**Plukk:** *02A01R5S1B*</span><span class="sxs-lookup"><span data-stu-id="887f4-251">**Pick:** *02A01R5S1B*</span></span>
        - <span data-ttu-id="887f4-252">**Plassering:** *06A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="887f4-252">**Put:** *06A01R2S1B*</span></span>

    - <span data-ttu-id="887f4-253">Det ble opprettet to arbeids-ID-er for salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="887f4-253">Two work IDs were created for sales order 1.</span></span>

1. <span data-ttu-id="887f4-254">Skriv ned arbeids-ID-ene for salgsordrene.</span><span class="sxs-lookup"><span data-stu-id="887f4-254">Make a note of the work IDs for the sales orders.</span></span>

<span data-ttu-id="887f4-255">Avhengig av beholdningsantallene kan arbeidsantallene som opprettes, variere noe.</span><span class="sxs-lookup"><span data-stu-id="887f4-255">Depending on your on-hand quantities, the work quantities that are created might vary slightly.</span></span> <span data-ttu-id="887f4-256">Generelt sett bør imidlertid arbeidshodene som opprettes, samsvare med dette scenarioeksemplet.</span><span class="sxs-lookup"><span data-stu-id="887f4-256">However, overall, the work headers that are created should match this scenario example.</span></span>

#### <a name="on-hand-inventory-license-plate-id"></a><span data-ttu-id="887f4-257">Nummerskilt-ID for lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="887f4-257">On-hand inventory license plate ID</span></span>

<span data-ttu-id="887f4-258">Senere i dette scenariet skal du bruke mobilappen Lagerstyring (eller en emulator), der du må identifisere nummerskiltet for å fullføre plukke- og etterfyllingsscenariene.</span><span class="sxs-lookup"><span data-stu-id="887f4-258">Later in this scenario, you will use the Warehouse Management mobile app (or an emulator), where you must identify the license plate to complete the picking and replenishment scenarios.</span></span>

<span data-ttu-id="887f4-259">Følg denne fremgangsmåten for å finne ID-ene til nummerskiltene som du vil trenge senere.</span><span class="sxs-lookup"><span data-stu-id="887f4-259">To find the license plate IDs that you will need later, follow these steps.</span></span>

1. <span data-ttu-id="887f4-260">Gå til **Lagerstyring \> Forespørsler og rapporter \> Beholdningsliste**.</span><span class="sxs-lookup"><span data-stu-id="887f4-260">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="887f4-261">Velg **Vis filtre**-knappen for å åpne filterruten.</span><span class="sxs-lookup"><span data-stu-id="887f4-261">Select the **Show filters** button to open the filter pane.</span></span>
1. <span data-ttu-id="887f4-262">Angi følgende filtreringskriterier for å hente nummerskiltene for scenariet.</span><span class="sxs-lookup"><span data-stu-id="887f4-262">Enter the following filtering criteria to get the license plates for the scenario.</span></span> <span data-ttu-id="887f4-263">Bruk filteret *begynner med*.</span><span class="sxs-lookup"><span data-stu-id="887f4-263">Use the *begins with* filter.</span></span>

    - <span data-ttu-id="887f4-264">**Varenummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="887f4-264">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="887f4-265">**Lager:** *61*</span><span class="sxs-lookup"><span data-stu-id="887f4-265">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="887f4-266">Velg **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="887f4-266">Select **Apply**.</span></span>
1. <span data-ttu-id="887f4-267">Klikk på **Dimensjoner** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="887f4-267">On the Action Pane, select **Dimensions**.</span></span>
1. <span data-ttu-id="887f4-268">I dialogboksen **Dimensjonsvisning**, i delen **Lagringsdimensjoner**, velger du alle verdiene.</span><span class="sxs-lookup"><span data-stu-id="887f4-268">In the **Dimensions display** dialog box, in the **Storage Dimensions** section, select all the values.</span></span>
1. <span data-ttu-id="887f4-269">I **Transaksjoner**-delen velger du **Varenummer** og **Antall \<\> 0**.</span><span class="sxs-lookup"><span data-stu-id="887f4-269">In the **Transactions** section, select **Item number** and **Quantity \<\> 0**.</span></span>
1. <span data-ttu-id="887f4-270">Når du er ferdig, velger du **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="887f4-270">When you've finished, select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="887f4-271">Rutenettet **Beholdning** viser skiltnumrene for varen *T0100* i hver lokasjon.</span><span class="sxs-lookup"><span data-stu-id="887f4-271">The **On-hand** grid shows the license plate numbers for item *T0100* in each location.</span></span> <span data-ttu-id="887f4-272">Noter deg hvilket nummerskilt som finnes på hver lokasjon, fordi du vil ha behov for denne informasjonen senere.</span><span class="sxs-lookup"><span data-stu-id="887f4-272">Make a note of the license plate that is in each location, because you will need this information later.</span></span>
1. <span data-ttu-id="887f4-273">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="887f4-273">Close the page.</span></span>

### <a name="process-steps"></a><span data-ttu-id="887f4-274">Prosesstrinn</span><span class="sxs-lookup"><span data-stu-id="887f4-274">Process steps</span></span>

<span data-ttu-id="887f4-275">Du vil utføre etterfylling av lagerlokasjon for de to første arbeids-ID-ene.</span><span class="sxs-lookup"><span data-stu-id="887f4-275">You will perform the warehouse location replenishment for the first two work IDs.</span></span> <span data-ttu-id="887f4-276">Arbeid på det tredje etterfyllingsarbeidet vil være blokkert til lagernivået på plukklokasjonen faller under terskelen.</span><span class="sxs-lookup"><span data-stu-id="887f4-276">Work on the third replenishment work will be blocked until the inventory level in the picking location falls below the threshold.</span></span>

#### <a name="replenishment"></a><span data-ttu-id="887f4-277">Etterfylling</span><span class="sxs-lookup"><span data-stu-id="887f4-277">Replenishment</span></span>

1. <span data-ttu-id="887f4-278">Logg på mobilappen Lagerstyring som en bruker som er aktivert i lager *61*.</span><span class="sxs-lookup"><span data-stu-id="887f4-278">Sign in to the Warehouse Management mobile app as a user in warehouse *61*.</span></span> <span data-ttu-id="887f4-279">(Angi *61* som bruker-ID og *1* som passord.)</span><span class="sxs-lookup"><span data-stu-id="887f4-279">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="887f4-280">Gå til **Beholdning \> Etterfylling**.</span><span class="sxs-lookup"><span data-stu-id="887f4-280">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="887f4-281">Du blir bedt om å fullføre det første etterfyllingsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="887f4-281">You're prompted to complete the first replenishment work.</span></span> <span data-ttu-id="887f4-282">Varenummeret, antallet og lokasjonen det skal plukkes fra, vises.</span><span class="sxs-lookup"><span data-stu-id="887f4-282">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="887f4-283">I **LP**-feltet angir du skiltnummeret for varen i lokasjonen som vises.</span><span class="sxs-lookup"><span data-stu-id="887f4-283">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="887f4-284">Velg **OK**-knappen (hakesymbolet).</span><span class="sxs-lookup"><span data-stu-id="887f4-284">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="887f4-285">Systemet genererer et målskiltnummer for det nye nummerskiltet for den plukkede varen.</span><span class="sxs-lookup"><span data-stu-id="887f4-285">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="887f4-286">Velg **OK** for å bekrefte verdien.</span><span class="sxs-lookup"><span data-stu-id="887f4-286">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="887f4-287">Plasseringsarbeid vises som instruerer brukeren om å plassere målnummerskiltet på etterfyllingslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="887f4-287">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="887f4-288">*Plassering*-lokasjonen skal være **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="887f4-288">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="887f4-289">Bekreft plasseringsdetaljene, og velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="887f4-289">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="887f4-290">Du får en melding om arbeidet er fullført, og detaljene for neste etterfyllingsplukkoppgave vises: varenummeret, antallet og lokasjonen det skal plukkes fra.</span><span class="sxs-lookup"><span data-stu-id="887f4-290">You receive a "Work Completed" message, and the details of the next replenishment pick task are shown: the item number, quantity, and location to pick from.</span></span> <span data-ttu-id="887f4-291">Plukklokasjonen vil være den samme som den første etterfyllingslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="887f4-291">The picking location will be the same as the first replenishment location.</span></span> <span data-ttu-id="887f4-292">Derfor vil nummerskiltet ha samme nummerskilt-ID som ble brukt for den første etterfyllingsarbeidsoppgaven.</span><span class="sxs-lookup"><span data-stu-id="887f4-292">Therefore, the license plate will have the same license plate ID that was used for the first replenishment work task.</span></span>

1. <span data-ttu-id="887f4-293">Gjenta de foregående trinnene for å fullføre etterfyllingsarbeidet for den andre arbeidsoppgaven.</span><span class="sxs-lookup"><span data-stu-id="887f4-293">Repeat the preceding steps to complete the replenishment work for the second work task.</span></span> <span data-ttu-id="887f4-294">Antallet og målnummerskiltet vil være forskjellig fra antallet og målnummerskiltet i den første arbeidsoppgaven.</span><span class="sxs-lookup"><span data-stu-id="887f4-294">The quantity and target license plate will differ from the quantity and target license plate for the first work task.</span></span>

<span data-ttu-id="887f4-295">Når det andre etter fyllingsarbeidet er fullført, vises en melding om at arbeidet er fullført.</span><span class="sxs-lookup"><span data-stu-id="887f4-295">After the second replenishment work is completed, you receive a "Work Completed" message.</span></span> <span data-ttu-id="887f4-296">Mobilenheten informerer også om at det ikke er noe tilgjengelig arbeid, selv om det gjenstår noe etterfyllingsarbeid.</span><span class="sxs-lookup"><span data-stu-id="887f4-296">The mobile device also informs you that there is no work available, even though some replenishment work remains.</span></span> <span data-ttu-id="887f4-297">Dette skjer fordi etterfyllingsarbeidet har tilgjengelighetsstatusen *På vent*, og er derfor merket som **Blokkert**.</span><span class="sxs-lookup"><span data-stu-id="887f4-297">This behavior occurs because the replenishment work has an availability status of *Held* and is therefore marked as **Blocked**.</span></span>

<span data-ttu-id="887f4-298">Statusen *På vent* ble utløst fordi lokasjonsprofilen for plukkelokasjonen som arbeidet tilordnes til, har en **Overflytantall**-verdi på *0,65 PL*.</span><span class="sxs-lookup"><span data-stu-id="887f4-298">The *Held* status was triggered because the location profile for the picking location that the work is being assigned to has an **Overflow quantity** value of *0.65 PL*.</span></span> <span data-ttu-id="887f4-299">De to forrige etterfyllingsarbeidsoppgavene har fylt lokasjonen nesten til overflytgrensen for varen *T0100*.</span><span class="sxs-lookup"><span data-stu-id="887f4-299">The two previous replenishment work tasks filled the location almost to its overflow limit for item *T0100*.</span></span> <span data-ttu-id="887f4-300">(Enhetskonverteringen for varen er *1 PL = 100 stk*.) Derfor vil gjenstående etterfyllingsarbeid føre til at lokasjonen overskrider overflytgrensen.</span><span class="sxs-lookup"><span data-stu-id="887f4-300">(The unit conversion for the item is *1 PL = 100 ea*.) Therefore, the remaining replenishment work would cause the location to exceed its overflow limit.</span></span>

<span data-ttu-id="887f4-301">Før nok beholdning er plukket fra lokasjonen for å få den under terskelen for arbeidsfrigivelse på menyen på mobilenheten, vil dette etterfyllingsarbeidet forbli blokkert.</span><span class="sxs-lookup"><span data-stu-id="887f4-301">Until enough inventory is picked from the location to bring it below the work release threshold on the mobile device menu item, this replenishment work will remain blocked.</span></span>

#### <a name="sales-order-pick"></a><span data-ttu-id="887f4-302">Salgsordreplukking</span><span class="sxs-lookup"><span data-stu-id="887f4-302">Sales order pick</span></span>

<span data-ttu-id="887f4-303">Før den gjenstående etterfyllingsarbeidsoppgaven kan fullføres, må plukklokasjonen tømmes til et nivå der blokkeringen for det gjenstående etterfyllingsarbeidet kan oppheves.</span><span class="sxs-lookup"><span data-stu-id="887f4-303">Before the remaining replenishment work task can be completed, the picking location must be depleted of inventory to a level where the remaining replenishment work can be unblocked.</span></span> <span data-ttu-id="887f4-304">Med andre ord kan ikke summen av lagerbeholdningen på lokasjonen og etterfyllingsantallet overskride verdien for **Overflytantall**.</span><span class="sxs-lookup"><span data-stu-id="887f4-304">In other words, the sum of the quantity of on-hand inventory in the location and the replenishment quantity can't exceed the **Overflow quantity** value.</span></span> <span data-ttu-id="887f4-305">Når denne summen er mindre enn overløpsantallet, blir blokkeringen av det gjenstående etterfyllingsarbeidet opphevet.</span><span class="sxs-lookup"><span data-stu-id="887f4-305">When this sum is less than the overflow quantity, the remaining replenishment work will be unblocked.</span></span>

1. <span data-ttu-id="887f4-306">Logg på mobilappen Lagerstyring som en bruker som er aktivert i lager *61*.</span><span class="sxs-lookup"><span data-stu-id="887f4-306">Sign in to the Warehouse Management mobile app as a user in warehouse *61*.</span></span> <span data-ttu-id="887f4-307">(Angi *61* som bruker-ID og *1* som passord.)</span><span class="sxs-lookup"><span data-stu-id="887f4-307">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="887f4-308">Gå til **Utgående \> Salgsplukking**.</span><span class="sxs-lookup"><span data-stu-id="887f4-308">Go to **Outbound \> Sales Picking**.</span></span>
1. <span data-ttu-id="887f4-309">Angi den første arbeids-ID-en for salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="887f4-309">Enter the first work ID for sales order 1.</span></span>

    <span data-ttu-id="887f4-310">Du kan se arbeids-ID-ene for salgsordrer som du har tatt notat av tidligere, på siden **Arbeidsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="887f4-310">Refer to the work IDs for sales orders that you made a note of earlier, on the **Work details** page.</span></span> <span data-ttu-id="887f4-311">Arbeids-ID-en du angir her, vil generere plukkarbeid for et antall på 10 stk. fra to separate lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="887f4-311">The work ID that you enter here will generate pick work for a quantity of 10 ea from two separate locations.</span></span>

1. <span data-ttu-id="887f4-312">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="887f4-312">Select **OK**.</span></span>

    <span data-ttu-id="887f4-313">Oppgavesiden **Salgsordrer: Plukk** viser varenummeret, antallet og lokasjonen du skal plukke fra, for den første lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="887f4-313">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the first location.</span></span>

1. <span data-ttu-id="887f4-314">I **LP**-feltet angir du skiltnummeret for varen i lokasjonen som vises.</span><span class="sxs-lookup"><span data-stu-id="887f4-314">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="887f4-315">Velg **OK**-knappen (hakesymbolet).</span><span class="sxs-lookup"><span data-stu-id="887f4-315">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="887f4-316">Oppgavesiden **Salgsordrer: Plukk** viser varenummeret, antallet og lokasjonen du skal plukke fra, for den neste lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="887f4-316">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the next location.</span></span>

1. <span data-ttu-id="887f4-317">I **LP**-feltet angir du skiltnummeret for varen i lokasjonen som vises.</span><span class="sxs-lookup"><span data-stu-id="887f4-317">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="887f4-318">Velg **OK**-knappen (hakesymbolet).</span><span class="sxs-lookup"><span data-stu-id="887f4-318">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="887f4-319">Siden **Salgsordrer: Plasser** instruerer deg om å plassere begge de fullførte plukkarbeidene i den utgående oppsamlingslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="887f4-319">The **Sales orders: Put** page instructs you to put away both the completed picking works to the outbound staging location.</span></span>

1. <span data-ttu-id="887f4-320">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="887f4-320">Select **OK**.</span></span>

    <span data-ttu-id="887f4-321">Du mottar en Arbeid fullført-melding.</span><span class="sxs-lookup"><span data-stu-id="887f4-321">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="887f4-322">Angi den andre arbeids-ID-en for salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="887f4-322">Enter the second work ID for sales order 1.</span></span>

    <span data-ttu-id="887f4-323">Det er bare én plukkoppgave for denne arbeids-ID-en.</span><span class="sxs-lookup"><span data-stu-id="887f4-323">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="887f4-324">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="887f4-324">Select **OK**.</span></span>

    <span data-ttu-id="887f4-325">Oppgavesiden **Salgsordrer: Plukk** viser varenummeret, antallet og lokasjonen du skal plukke fra.</span><span class="sxs-lookup"><span data-stu-id="887f4-325">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="887f4-326">I **LP**-feltet angir du skiltnummeret for varen i lokasjonen som vises.</span><span class="sxs-lookup"><span data-stu-id="887f4-326">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="887f4-327">Nummerskiltet du angir, vil være et av de systemgenererte nummerskiltene fra etterfyllingsarbeidsoppgavene.</span><span class="sxs-lookup"><span data-stu-id="887f4-327">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="887f4-328">For å være sikker på at du registrerer riktig nummerskilt-ID, må du kontrollere beholdningen på siden **Beholdningsliste** for varen, lokasjonen og antallet.</span><span class="sxs-lookup"><span data-stu-id="887f4-328">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="887f4-329">Velg **OK**-knappen (hakesymbolet).</span><span class="sxs-lookup"><span data-stu-id="887f4-329">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="887f4-330">Bekreft instruksjonene for plasseringsoppgaven til plasseringen for utgående oppsamling.</span><span class="sxs-lookup"><span data-stu-id="887f4-330">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="887f4-331">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="887f4-331">Select **OK**.</span></span>

    <span data-ttu-id="887f4-332">Du mottar en Arbeid fullført-melding.</span><span class="sxs-lookup"><span data-stu-id="887f4-332">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="887f4-333">Salgsordre 2 er sperret for plukking fordi etterfyllingsoppgaven den er koblet til, ikke er fullført.</span><span class="sxs-lookup"><span data-stu-id="887f4-333">Sales order 2 is blocked from picking because the replenishment task that it's linked to isn't completed.</span></span> <span data-ttu-id="887f4-334">For øyeblikket er det fremdeles et antall på 30 stk. i plukklokasjonen, og etterfyllingsantallet for salgsordre 2 er 60 stk.</span><span class="sxs-lookup"><span data-stu-id="887f4-334">Currently, there is still a quantity of 30 ea in the picking location, and the replenishment quantity for sales order 2 is 60 ea.</span></span> <span data-ttu-id="887f4-335">Summen av lagerbeholdningen og etterfyllingsbeholdningen (90 stk.) overskrider overflytantallet på 0,65 PL (eller 65 stk.).</span><span class="sxs-lookup"><span data-stu-id="887f4-335">The sum of the on-hand inventory and the replenishment inventory (90 ea) exceeds the overflow quantity of 0.65 PL (or 65 ea).</span></span> <span data-ttu-id="887f4-336">Før etterfyllingsarbeidet kan fullføres, må salgsordre 3 plukkes.</span><span class="sxs-lookup"><span data-stu-id="887f4-336">Before the replenishment work can be completed, sales order 3 must be picked.</span></span>

1. <span data-ttu-id="887f4-337">Angi den arbeids-ID-en for salgsordre 3.</span><span class="sxs-lookup"><span data-stu-id="887f4-337">Enter the work ID for sales order 3.</span></span>

    <span data-ttu-id="887f4-338">Det er bare én plukkoppgave for denne arbeids-ID-en.</span><span class="sxs-lookup"><span data-stu-id="887f4-338">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="887f4-339">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="887f4-339">Select **OK**.</span></span>

    <span data-ttu-id="887f4-340">Oppgavesiden **Salgsordrer: Plukk** viser varenummeret, antallet og lokasjonen du skal plukke fra.</span><span class="sxs-lookup"><span data-stu-id="887f4-340">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="887f4-341">I **LP**-feltet angir du skiltnummeret for varen i lokasjonen som vises.</span><span class="sxs-lookup"><span data-stu-id="887f4-341">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="887f4-342">Nummerskiltet du angir, vil være et av de systemgenererte nummerskiltene fra etterfyllingsarbeidsoppgavene.</span><span class="sxs-lookup"><span data-stu-id="887f4-342">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="887f4-343">For å være sikker på at du registrerer riktig nummerskilt-ID, må du kontrollere beholdningen på siden **Beholdningsliste** for varen, lokasjonen og antallet.</span><span class="sxs-lookup"><span data-stu-id="887f4-343">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="887f4-344">Velg **OK**-knappen (hakesymbolet).</span><span class="sxs-lookup"><span data-stu-id="887f4-344">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="887f4-345">Bekreft instruksjonene for plasseringsoppgaven til plasseringen for utgående oppsamling.</span><span class="sxs-lookup"><span data-stu-id="887f4-345">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="887f4-346">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="887f4-346">Select **OK**.</span></span>

    <span data-ttu-id="887f4-347">Du mottar en Arbeid fullført-melding.</span><span class="sxs-lookup"><span data-stu-id="887f4-347">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="887f4-348">Så snart summen av beholdningsantallet i plukklokasjonen og etterfyllingsantallet er under terskelen, vil du kunne behandle gjenstående etterfyllingsarbeid.</span><span class="sxs-lookup"><span data-stu-id="887f4-348">As soon as the sum of the on-hand quantity in the picking location and the replenishment quantity is below the threshold, you will be able to process the remaining replenishment work.</span></span>

<span data-ttu-id="887f4-349">Gå tilbake til siden **Arbeidsdetaljer**, og legg merke til at tilgjengeligheten for etterfyllingsarbeidet for den siste delen av etterfyllingen (for salgsordre 2) er *Åpen*, fordi det nå er nok plass på lokasjonen til å godta etterfyllingen.</span><span class="sxs-lookup"><span data-stu-id="887f4-349">Return to the **Work details** page, and notice that the replenishment work availability for the final piece of replenishment (for sales order 2) is *Open*, because there is now enough space in the location to accept the replenishment.</span></span>

<span data-ttu-id="887f4-350">Nå kan du behandle dette etterfyllingsarbeidet via mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="887f4-350">You can now process this replenishment work via the mobile device.</span></span>

1. <span data-ttu-id="887f4-351">Gå til **Beholdning \> Etterfylling**.</span><span class="sxs-lookup"><span data-stu-id="887f4-351">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="887f4-352">Du blir bedt om å fullføre det resterende etterfyllingsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="887f4-352">You're prompted to complete the remaining replenishment work.</span></span> <span data-ttu-id="887f4-353">Varenummeret, antallet og lokasjonen det skal plukkes fra, vises.</span><span class="sxs-lookup"><span data-stu-id="887f4-353">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="887f4-354">I **LP**-feltet angir du skiltnummeret for varen i lokasjonen som vises.</span><span class="sxs-lookup"><span data-stu-id="887f4-354">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="887f4-355">Velg **OK**-knappen (hakesymbolet).</span><span class="sxs-lookup"><span data-stu-id="887f4-355">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="887f4-356">Systemet genererer et målskiltnummer for det nye nummerskiltet for den plukkede varen.</span><span class="sxs-lookup"><span data-stu-id="887f4-356">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="887f4-357">Velg **OK** for å bekrefte verdien.</span><span class="sxs-lookup"><span data-stu-id="887f4-357">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="887f4-358">Plasseringsarbeid vises som instruerer brukeren om å plassere målnummerskiltet på etterfyllingslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="887f4-358">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="887f4-359">*Plassering*-lokasjonen skal være **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="887f4-359">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="887f4-360">Bekreft plasseringsdetaljene, og velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="887f4-360">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="887f4-361">Du får meldingene om fullført arbeid og ikke noe arbeid tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="887f4-361">You receive "Work Completed" and "No Work Available" messages.</span></span>

<span data-ttu-id="887f4-362">Nå kan du plukke salgsordre 2.</span><span class="sxs-lookup"><span data-stu-id="887f4-362">You can now pick sales order 2.</span></span> <span data-ttu-id="887f4-363">Blokkeringen for den ble fjernet da etter fyllingsarbeidet som er koblet til salgsordren, ble fullført.</span><span class="sxs-lookup"><span data-stu-id="887f4-363">It became unblocked when the replenishment work that is linked to the sales order was completed.</span></span>

1. <span data-ttu-id="887f4-364">Angi arbeids-ID-en for salgsordre 2.</span><span class="sxs-lookup"><span data-stu-id="887f4-364">Enter the work ID for sales order 2.</span></span>

    <span data-ttu-id="887f4-365">Det er bare én plukkoppgave for denne arbeids-ID-en.</span><span class="sxs-lookup"><span data-stu-id="887f4-365">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="887f4-366">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="887f4-366">Select **OK**.</span></span>

    <span data-ttu-id="887f4-367">Oppgavesiden **Salgsordrer: Plukk** viser varenummeret, antallet og lokasjonen du skal plukke fra.</span><span class="sxs-lookup"><span data-stu-id="887f4-367">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="887f4-368">I **LP**-feltet angir du skiltnummeret for varen i lokasjonen som vises.</span><span class="sxs-lookup"><span data-stu-id="887f4-368">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="887f4-369">Nummerskiltet du angir, vil være det systemgenererte nummerskiltet fra etterfyllingsarbeidsoppgaven.</span><span class="sxs-lookup"><span data-stu-id="887f4-369">The license plate that you specify will be the system-generated license plate from the replenishment work task.</span></span> <span data-ttu-id="887f4-370">For å være sikker på at du registrerer riktig nummerskilt-ID, må du kontrollere beholdningen på siden **Beholdningsliste** for varen, lokasjonen og antallet.</span><span class="sxs-lookup"><span data-stu-id="887f4-370">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="887f4-371">Velg **OK**-knappen (hakesymbolet).</span><span class="sxs-lookup"><span data-stu-id="887f4-371">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="887f4-372">Bekreft instruksjonene for plasseringsoppgaven til plasseringen for utgående oppsamling.</span><span class="sxs-lookup"><span data-stu-id="887f4-372">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="887f4-373">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="887f4-373">Select **OK**.</span></span>

    <span data-ttu-id="887f4-374">Du mottar en Arbeid fullført-melding.</span><span class="sxs-lookup"><span data-stu-id="887f4-374">You receive a "Work Completed" message.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="887f4-375">Merknader og tips</span><span class="sxs-lookup"><span data-stu-id="887f4-375">Notes and tips</span></span>

- <span data-ttu-id="887f4-376">Denne funksjonaliteten fungerer med alle typer etterfylling: bølgebehov, min/maks, lastbehov og sporing.</span><span class="sxs-lookup"><span data-stu-id="887f4-376">This functionality works with all types of replenishment: wave demand, min/max, load demand, and slotting.</span></span>
- <span data-ttu-id="887f4-377">Du kan manuelt overstyre tilgjengeligheten av etterfyllingsarbeid for hvert arbeidshode fra siden **Arbeidsdetaljer** hvis du vil.</span><span class="sxs-lookup"><span data-stu-id="887f4-377">You can manually override the replenishment work availability for each work header from the **Work details** page if you want.</span></span>
- <span data-ttu-id="887f4-378">Når systemet angir tilgjengeligheten for etterfyllingsarbeid, vurderes all beholdning som allerede finnes på lokasjonen før noe som helst arbeid fullføres.</span><span class="sxs-lookup"><span data-stu-id="887f4-378">When the system sets the replenishment work availability, it considers any inventory that is already in the location before any work is completed</span></span>
- <span data-ttu-id="887f4-379">Hver del av salgsordrearbeid er koblet til et bestemt etterfyllingsarbeid.</span><span class="sxs-lookup"><span data-stu-id="887f4-379">Each piece of sales order work is linked to a specific replenishment work.</span></span> <span data-ttu-id="887f4-380">Det finnes ingen tilsvarende funksjonalitet for tilgjengelighet av salgsarbeid.</span><span class="sxs-lookup"><span data-stu-id="887f4-380">There is no corresponding sales work availability functionality.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]