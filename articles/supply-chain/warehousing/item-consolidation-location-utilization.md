---
title: Varekonsolidering – lokasjonsutnyttelse
description: Dette emnet gir informasjon om funksjonalitet som gjør det enkelt for lagerledere å vise og filtrere volumbruk av lokasjoner på tvers av lageret. Ledere kan velge lokasjoner og opprette lagerflyttingsarbeid direkte fra siden for varekonsolidering for å konsolidere varer og dermed gjøre bedre bruk av lagerplass.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6a328b20c1cfb2fc376ab4656c64cf585a5aa015
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017190"
---
# <a name="item-consolidation---location-utilization"></a><span data-ttu-id="6c9bf-104">Varekonsolidering – lokasjonsutnyttelse</span><span class="sxs-lookup"><span data-stu-id="6c9bf-104">Item consolidation - location utilization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c9bf-105">Dette emnet gir informasjon om funksjonalitet som gjør det enkelt for lagerledere å vise og filtrere volumbruk av lokasjoner på tvers av lageret.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-105">This topic provides information about functionality that makes it easy for warehouse managers to view and filter the volumetric utilization of locations across the warehouse.</span></span> <span data-ttu-id="6c9bf-106">Ledere kan velge lokasjoner og opprette lagerflyttingsarbeid direkte fra siden for **varekonsolidering** for å konsolidere varer og dermed gjøre bedre bruk av lagerplass.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-106">Managers can select locations and create inventory movement work directly from the **Item Consolidation** page to consolidate items and therefore make better use of warehouse space.</span></span>

## <a name="turn-on-the-features"></a><span data-ttu-id="6c9bf-107">Aktivere funksjonene</span><span class="sxs-lookup"><span data-stu-id="6c9bf-107">Turn on the features</span></span>

<span data-ttu-id="6c9bf-108">Før du kan bruke funksjonene som beskrives i dette emnet, må du aktivere dem i systemet.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-108">Before you can use the features that are described in this topic, you must turn them on in your system.</span></span> <span data-ttu-id="6c9bf-109">Administratorer kan bruke arbeidsområdet for [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere statusen for disse funksjonene og aktivere dem hvis nødvendig.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="6c9bf-110">Slå på begge disse funksjonene i den rekkefølgen de vises i.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-110">Turn on both the following features, in the order that they are listed in.</span></span> <span data-ttu-id="6c9bf-111">(Begge funksjonene gjelder for modulen for **Lagerstyring**.)</span><span class="sxs-lookup"><span data-stu-id="6c9bf-111">(Both features are for the **Warehouse management** module.)</span></span>

1. <span data-ttu-id="6c9bf-112">Status for lagerlokasjon</span><span class="sxs-lookup"><span data-stu-id="6c9bf-112">Warehouse location status</span></span>
2. <span data-ttu-id="6c9bf-113">Bruk av lokasjon for varekonsolidering</span><span class="sxs-lookup"><span data-stu-id="6c9bf-113">Item consolidation location utilization</span></span>

## <a name="warehouse-location-status"></a><span data-ttu-id="6c9bf-114">Status for lagerlokasjon</span><span class="sxs-lookup"><span data-stu-id="6c9bf-114">Warehouse location status</span></span>

<span data-ttu-id="6c9bf-115">Funksjonen *Status for lagerlokasjon* legger til fire nye felt på siden **Lokasjoner** for å spore tilleggsinformasjon om gjeldende status for lokasjonen:</span><span class="sxs-lookup"><span data-stu-id="6c9bf-115">The *Warehouse location status* feature adds four new fields to the **Locations** page to track additional information about the current state of the location:</span></span>

- <span data-ttu-id="6c9bf-116">**Varenummer** – varen som for øyeblikket er på lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-116">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="6c9bf-117">Hvis lokasjonen inneholder flere varer, er dette feltet tomt.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-117">If the location contains multiple items, this field will be blank.</span></span>
- <span data-ttu-id="6c9bf-118">**Dato og klokkeslett for siste aktivitet** – tidsstempelet for den siste lagertransaksjonen som ble utført mot lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-118">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="6c9bf-119">**Aldersdato** – datoen da beholdningen i lokasjonen ble hentet inn i lageret.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-119">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="6c9bf-120">Denne datoen beregnes basert på aldersdatoen til nummerskiltet.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-120">This date is calculated based on the license plate aging date.</span></span> <span data-ttu-id="6c9bf-121">Selv om datoen er nøyaktig for nummerskiltsporede lokasjoner, er det kanskje ikke nøyaktig for lokasjoner som ikke er nummerskiltsporet.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-121">Although this date is accurate for license plate–tracked locations, it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="6c9bf-122">**Lokasjonsstatus** – statusen til lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-122">**Location status** – The status of the location.</span></span> <span data-ttu-id="6c9bf-123">Fire verdier er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="6c9bf-123">Four values are available:</span></span>

    - <span data-ttu-id="6c9bf-124">**Ikke bestemt** – lokasjonsprofilen kan ikke spore status.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-124">**Undetermined** – The location profile doesn't track status.</span></span> <span data-ttu-id="6c9bf-125">Gjeldende status er derfor ukjent.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-125">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="6c9bf-126">**Tom** – Det er ikke lager på lokasjonen for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-126">**Empty** – No inventory is currently in the location.</span></span>
    - <span data-ttu-id="6c9bf-127">**Plukk** – Utgående transaksjoner er utført mot lokasjonen etter at det sist ble tømt.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-127">**Picking** – Outbound transactions have been performed against the location after it was last empty.</span></span>
    - <span data-ttu-id="6c9bf-128">**Lager** – Bare inngående transaksjoner er utført siden lokasjonen sist ble tømt.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-128">**Storage** – Only inbound transactions have been performed since the location was last empty.</span></span>

<span data-ttu-id="6c9bf-129">Med disse feltene kan lagerledere få en bedre oversikt over statusen for lagerlokasjonene.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-129">These fields let warehouse managers get a better overview of the status of the locations in the warehouse.</span></span> <span data-ttu-id="6c9bf-130">De tillater også mer avansert rapportering og filtrering.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-130">They also allow for more advanced reporting and filtering.</span></span>

## <a name="set-up-item-consolidation-and-location-utilization"></a><span data-ttu-id="6c9bf-131">Konfigurere varekonsolidering og lokasjonsutnyttelse</span><span class="sxs-lookup"><span data-stu-id="6c9bf-131">Set up item consolidation and location utilization</span></span>

<span data-ttu-id="6c9bf-132">Denne delen beskriver hvordan du kan klargjøre systemet til å bruke varekonsolidering og bruk av lokasjon.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-132">This section describes how to prepare your system to use item consolidation and location utilization.</span></span> <span data-ttu-id="6c9bf-133">Fremgangsmåtene bruker eksempelverdier fra standard demodata.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-133">The procedures use sample values from the standard demo data.</span></span> <span data-ttu-id="6c9bf-134">Hvis du planlegger å arbeide gjennom eksempelscenarioet som er oppgitt senere i dette emnet, velger du den juridiske enheten **USMF** (som inneholder standard demodata) og oppretter hver post som beskrives i denne delen.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-134">If you plan to work through the example scenario that is provided later in this topic, select the **USMF** legal entity (which contains the standard demo data), and create each record that is described in this section.</span></span> <span data-ttu-id="6c9bf-135">Hvis du ikke planlegger å arbeide gjennom eksempelscenarioet, kan verdiene som angis her, vurderes som eksempler på hvilke typer oppsett du må fullføre for å bruke funksjonene.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-135">If you don't plan to work through the example scenario, the values that are provided here can be considered examples of the types of setup that you must complete to use the features.</span></span>

### <a name="released-product"></a><span data-ttu-id="6c9bf-136">Frigitt produkt</span><span class="sxs-lookup"><span data-stu-id="6c9bf-136">Released product</span></span>

1. <span data-ttu-id="6c9bf-137">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-137">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="6c9bf-138">I feltet **Varenummer** velger du *M9201* , og deretter åpner du detaljsiden.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-138">In the **Item number** field, select *M9201* , and open the details page.</span></span>
1. <span data-ttu-id="6c9bf-139">I handlingsruten i kategorien **Administrer lager** i gruppen **Lager** velger du **Fysiske dimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-139">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="6c9bf-140">På **Fysiske dimensjoner** -siden i handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-140">On the **Physical dimension** page, on the Action Pane, select **New**.</span></span>

    <span data-ttu-id="6c9bf-141">Det blir lagt til en ny linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-141">A new line is added to the grid.</span></span> <span data-ttu-id="6c9bf-142">**Varenummer** -feltet er forhåndsdefinert.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-142">The **Item number** field is preset.</span></span>

1. <span data-ttu-id="6c9bf-143">I **Enhet** -feltet velger du *ea*.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-143">In the **Unit** field, select *ea*.</span></span> <span data-ttu-id="6c9bf-144">De gjenværende feltene på linjen angis automatisk.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-144">The remaining fields on the line are automatically set.</span></span>
1. <span data-ttu-id="6c9bf-145">Velg **Lagre** , og lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-145">Select **Save** , and close the page.</span></span>

### <a name="location-profile"></a><span data-ttu-id="6c9bf-146">Lokasjonsprofil</span><span class="sxs-lookup"><span data-stu-id="6c9bf-146">Location profile</span></span>

1. <span data-ttu-id="6c9bf-147">Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-147">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="6c9bf-148">Velg **ETASJE-05** i listen over lokasjonsprofiler.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-148">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="6c9bf-149">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-149">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="6c9bf-150">I hurtigfanen **Generelt** kontrollerer du at begge alternativene nedenfor er satt til *Ja* :</span><span class="sxs-lookup"><span data-stu-id="6c9bf-150">On the **General** FastTab, make sure that both the following options are set to *Yes* :</span></span>

    - <span data-ttu-id="6c9bf-151">Aktiver vare i lokasjonen</span><span class="sxs-lookup"><span data-stu-id="6c9bf-151">Enable item in location</span></span>
    - <span data-ttu-id="6c9bf-152">Aktiver lokasjonsstatus</span><span class="sxs-lookup"><span data-stu-id="6c9bf-152">Enable location status</span></span>

1. <span data-ttu-id="6c9bf-153">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-153">Select **Save**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="6c9bf-154">Hvis alternativene **Aktiver vare på lokasjon** og **Aktiver lokasjonsstatus** allerede er satt til *Ja* , går du videre til instruksjonene for å definere hurtigfanen **Dimensjoner** i trinn 10.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-154">If the **Enable item in location** and **Enable location status** options were already set to *Yes* , skip ahead to the instructions for setting up the **Dimensions** FastTab in step 10.</span></span> <span data-ttu-id="6c9bf-155">Hvis alternativene ikke allerede er satt til *Ja* , må du kjøre en konsekvenskontroll for modulen **Lagerstyring** etter at du har angitt dem manuelt.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-155">If the options weren't already set to *Yes* , you must run a consistency check for the **Warehouse management** module after you manually set them.</span></span> <span data-ttu-id="6c9bf-156">I dette tilfellet går du videre til neste trinn.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-156">In this case, continue to the next step.</span></span>

1. <span data-ttu-id="6c9bf-157">Hvis du vil kjøre en konsekvenskontroll, går du til **Systemadministrasjon \> Periodiske oppgaver \> Database \> Konsekvenskontroll**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-157">To run the consistency check, go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="6c9bf-158">Angi følgende verdier i dialogboksen **Konsekvenskontroll** :</span><span class="sxs-lookup"><span data-stu-id="6c9bf-158">In the **Consistency check** dialog box, set the following values:</span></span>

    - <span data-ttu-id="6c9bf-159">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-159">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="6c9bf-160">**Kontroller/løs:** *Kontroller*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-160">**Check/Fix:** *Check*</span></span>
    - <span data-ttu-id="6c9bf-161">**Fra dato** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-161">**From date:** Leave this field blank.</span></span>
    - <span data-ttu-id="6c9bf-162">**Konsekvenskontroll av lagerlokasjonsstatus:** Merk av for dette alternativet.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-162">**Warehouse location status consistency check:** Select this check box.</span></span>

1. <span data-ttu-id="6c9bf-163">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-163">Select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="6c9bf-164">Når konsekvenskontrollen er utført, mottar du en varsling.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-164">When the consistency check is completed, you receive a notification.</span></span> <span data-ttu-id="6c9bf-165">Åpne [handlingssenteret](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) for å vise meldingen.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-165">Open the [Action Center](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) to view the message.</span></span> <span data-ttu-id="6c9bf-166">Velg **Meldingsdetaljer** for å vise detaljene.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-166">Select **Message details** to view the details.</span></span>
    >
    > <span data-ttu-id="6c9bf-167">Hvis meldingen for konsekvenskontrollen viser statusen "Feil lokasjonsstatusinformasjon for lokasjonen XXXX i lageret XX", må du kjøre konsekvenskontrollen på nytt.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-167">If the message for the consistency check states, "Incorrect location status information found for location XXXX in warehouse XX," you must run the consistency check again.</span></span> <span data-ttu-id="6c9bf-168">Denne gangen setter du feltet **Kontroller/korriger** til *Rett feil*.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-168">This time, set the **Check/Fix** field to *Fix error*.</span></span> <span data-ttu-id="6c9bf-169">Vis meldingene for å være sikker på at ingen feil ble funnet.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-169">View the messages to make sure that no errors were found.</span></span>

1. <span data-ttu-id="6c9bf-170">Du må nå fullføre konfigurasjonen av lokasjonsprofilen.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-170">You must now finish setting up the location profile.</span></span> <span data-ttu-id="6c9bf-171">Gå tilbake til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsprofiler** , velg lokasjonsprofil **ETASJE-05** , og velg deretter **Rediger** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-171">Go back to **Warehouse management \> Setup \> Warehouse \> Location profiles** , select location profile **FLOOR-05** , and then, on the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="6c9bf-172">Angi følgende verdier i **Dimensjoner** -hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="6c9bf-172">On the **Dimensions** FastTab, set the following values:</span></span>

    - <span data-ttu-id="6c9bf-173">**Volumutnyttelsesprosent:** *100*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-173">**Volume utilization percentage:** *100*</span></span>
    - <span data-ttu-id="6c9bf-174">**Volumetrisk metode som brukes for lagerlokasjon:** *Bruk lokasjonsvolum*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-174">**Volumetric method used for inventory location:** *Use location volume*</span></span>
    - <span data-ttu-id="6c9bf-175">**Faktisk lokasjonshøyde:** *10*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-175">**Actual location height:** *10*</span></span>
    - <span data-ttu-id="6c9bf-176">**Faktisk lokasjonsbredde:** *10*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-176">**Actual location width:** *10*</span></span>
    - <span data-ttu-id="6c9bf-177">**Faktisk dybde for lokasjon:** *10*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-177">**Actual location depth:** *10*</span></span>
    - <span data-ttu-id="6c9bf-178">**Maksimumsvekt:** *100*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-178">**Maximum weight:** *100*</span></span>

1. <span data-ttu-id="6c9bf-179">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-179">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="6c9bf-180">Menyelementer på mobilenheten</span><span class="sxs-lookup"><span data-stu-id="6c9bf-180">Mobile device menu items</span></span>

1. <span data-ttu-id="6c9bf-181">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-181">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="6c9bf-182">Velg **Ny** i handlingsruten for å opprette et menyelement for sortering.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-182">On the Action Pane, select **New** to create a menu item for sorting.</span></span>
1. <span data-ttu-id="6c9bf-183">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="6c9bf-183">In the header, set the following values:</span></span>

    - <span data-ttu-id="6c9bf-184">**Menyelementnavn:** *Juster i*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-184">**Menu item name:** *Adjust In*</span></span>
    - <span data-ttu-id="6c9bf-185">**Tittel:** *Juster inn*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-185">**Title:** *Adjust In*</span></span>
    - <span data-ttu-id="6c9bf-186">**Modus:** *Arbeid*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-186">**Mode:** *Work*</span></span>
    - <span data-ttu-id="6c9bf-187">**Bruke eksisterende arbeid:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-187">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="6c9bf-188">Angi følgende verdier i **Generelt** -hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="6c9bf-188">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="6c9bf-189">**Arbeidsopprettelsesprosess:** *Justering inn*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-189">**Work creation process:** *Adjustment in*</span></span>
    - <span data-ttu-id="6c9bf-190">**Lagerjusteringstyper:** *Juster inn*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-190">**Inventory adjustment types:** *Adjust in*</span></span>

1. <span data-ttu-id="6c9bf-191">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-191">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="6c9bf-192">Meny på mobilenheten</span><span class="sxs-lookup"><span data-stu-id="6c9bf-192">Mobile device menu</span></span>

1. <span data-ttu-id="6c9bf-193">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-193">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="6c9bf-194">Velg **Lager** i listen over menyer.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-194">In the list of menus, select **Inventory**.</span></span>
1. <span data-ttu-id="6c9bf-195">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-195">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="6c9bf-196">I **Tilgjengelige menyer og menyelementer** -listen finner og velger du **Juster inn** -menyelementet.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-196">In the **Available Menus And Menu Items** list, find and select the **Adjust In** menu item.</span></span>
1. <span data-ttu-id="6c9bf-197">Velg høyre pil-knappen for å flytte **Juster inn** til listen **Menystruktur**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-197">Select the right arrow button to move **Adjust In** to the **Menu Structure** list.</span></span> <span data-ttu-id="6c9bf-198">På denne måten legger du til det nye menyelementet på den valgte menyen.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-198">In this way, you add the new menu item to the selected menu.</span></span>
1. <span data-ttu-id="6c9bf-199">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-199">Select **Save**.</span></span>

### <a name="movement-types"></a><span data-ttu-id="6c9bf-200">Bevegelsestyper</span><span class="sxs-lookup"><span data-stu-id="6c9bf-200">Movement types</span></span>

1. <span data-ttu-id="6c9bf-201">Gå til **Lagerstyring \> Oppsett \> Lager \> Varetilgangstyper**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-201">Go to **Warehouse management \> Setup \> Inventory \> Movement types**.</span></span>
1. <span data-ttu-id="6c9bf-202">Velg **Ny** i handlingsruten, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="6c9bf-202">On the Action Pane, select **New** , and then set the following values:</span></span>

    - <span data-ttu-id="6c9bf-203">**Bevegelsestypekode:** *KONSOLIDER*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-203">**Movement type code:** *CONSOLIDATE*</span></span>
    - <span data-ttu-id="6c9bf-204">**Beskrivelse:** *Konsolider lokasjoner*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-204">**Description:** *Consolidate locations*</span></span>
    - <span data-ttu-id="6c9bf-205">**Arbeidsklasse-ID:** *InvMov*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-205">**Work class ID:** *InvMov*</span></span>

1. <span data-ttu-id="6c9bf-206">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-206">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="6c9bf-207">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="6c9bf-207">Example scenario</span></span>

<span data-ttu-id="6c9bf-208">Følgende scenario bruker lagerappen på en mobilenhet for å lage en *justering inn* på to steder i lageret.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-208">The following scenario uses the warehouse app on a mobile device to make an inventory *adjustment in* to two locations in the warehouse.</span></span>

### <a name="add-inventory-to-locations"></a><span data-ttu-id="6c9bf-209">Legge til lager på lokasjoner</span><span class="sxs-lookup"><span data-stu-id="6c9bf-209">Add inventory to locations</span></span>

1. <span data-ttu-id="6c9bf-210">Logg på mobilenheten som en bruker som er aktivert for lager *51*.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-210">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="6c9bf-211">Gå til **Lager \> Juster inn**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-211">Go to **Inventory \> Adjust In**.</span></span>

    <span data-ttu-id="6c9bf-212">Du skal nå angi den første lokasjonsjusteringen.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-212">You will now enter the first location adjustment.</span></span>

1. <span data-ttu-id="6c9bf-213">I **Justering inn** -oppgave velger du lokasjonen du vil utføre lagerjusteringen for.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-213">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="6c9bf-214">Velg **LP-001** i *LOC* -feltet.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-214">In the **LOC** field, select *LP-001*.</span></span>
1. <span data-ttu-id="6c9bf-215">Bekreft lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-215">Confirm the location.</span></span>
1. <span data-ttu-id="6c9bf-216">Opprett en nummerskilt-ID for varen som skal legges til i lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-216">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="6c9bf-217">I feltet **Nummerskilt** angir du *LP00101*.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-217">In the **LP** field, enter *LP00101*.</span></span>
1. <span data-ttu-id="6c9bf-218">Bekreft nummerskiltet.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-218">Confirm the license plate.</span></span>
1. <span data-ttu-id="6c9bf-219">Angi varen som skal legges til i nummerskiltet.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-219">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="6c9bf-220">Angi *M9201* i feltet **ITEM**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-220">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="6c9bf-221">Bekreft varen.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-221">Confirm the item.</span></span>
1. <span data-ttu-id="6c9bf-222">Angi antallet av varen som skal legges til.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-222">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="6c9bf-223">I feltet **QTY** angir du *10*.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-223">In the **QTY** field, enter *10*.</span></span>
1. <span data-ttu-id="6c9bf-224">Bekreft antallet.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-224">Confirm the quantity.</span></span>

    <span data-ttu-id="6c9bf-225">Du mottar en Arbeid fullført-melding.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-225">You receive a "Work Completed" message.</span></span> <span data-ttu-id="6c9bf-226">Du skal nå angi den andre lokasjonsjusteringen.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-226">You will now enter the second location adjustment.</span></span>

1. <span data-ttu-id="6c9bf-227">I **Justering inn** -oppgave velger du lokasjonen du vil utføre lagerjusteringen for.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-227">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="6c9bf-228">Velg **LP-002** i *LOC* -feltet.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-228">In the **LOC** field, select *LP-002*.</span></span>
1. <span data-ttu-id="6c9bf-229">Bekreft lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-229">Confirm the location.</span></span>
1. <span data-ttu-id="6c9bf-230">Opprett en nummerskilt-ID for varen som skal legges til i lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-230">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="6c9bf-231">I feltet **Nummerskilt** angir du *LP00201*.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-231">In the **LP** field, enter *LP00201*.</span></span>
1. <span data-ttu-id="6c9bf-232">Bekreft nummerskiltet.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-232">Confirm the license plate.</span></span>
1. <span data-ttu-id="6c9bf-233">Angi varen som skal legges til i nummerskiltet.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-233">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="6c9bf-234">Angi *M9201* i feltet **ITEM**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-234">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="6c9bf-235">Bekreft varen.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-235">Confirm the item.</span></span>
1. <span data-ttu-id="6c9bf-236">Angi antallet av varen som skal legges til.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-236">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="6c9bf-237">I feltet **QTY** angir du *15*.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-237">In the **QTY** field, enter *15*.</span></span>
1. <span data-ttu-id="6c9bf-238">Bekreft antallet.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-238">Confirm the quantity.</span></span>

    <span data-ttu-id="6c9bf-239">Du mottar en Arbeid fullført-melding.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-239">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="6c9bf-240">Velg menyknappen (noen ganger kalt hamburger eller hamburgerknappen), og velg deretter **Avbryt** for å avslutte **Justering inn** -oppgaven.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-240">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit the **Adjustment in** task.</span></span>

### <a name="consolidate-locations"></a><span data-ttu-id="6c9bf-241">Konsolidere lokasjoner</span><span class="sxs-lookup"><span data-stu-id="6c9bf-241">Consolidate locations</span></span>

1. <span data-ttu-id="6c9bf-242">Gå til **Lagerstyring \> Periodiske oppgaver \> Varekonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-242">Go to **Warehouse management \> Periodic tasks \> Item consolidation**.</span></span>
1. <span data-ttu-id="6c9bf-243">I hodet velger du lageret det skal utfører konsolidering for.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-243">In the header, select a warehouse to do the consolidation for.</span></span> <span data-ttu-id="6c9bf-244">I **Lager** -feltet angir du *51*.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-244">In the **Warehouse** field, enter *51*.</span></span>

    <span data-ttu-id="6c9bf-245">Det vises en post for hver lokasjon der vare *M9201* ble justert.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-245">A record is shown for each location where item *M9201* was adjusted.</span></span> <span data-ttu-id="6c9bf-246">Kolonnen **Utnyttelsesprosent** viser volumbruk for hver lokasjon.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-246">The **Utilization percentage** column shows the volumetric utilization of each location.</span></span>

1. <span data-ttu-id="6c9bf-247">Hvis du vil konsolidere lageret, velger du alle lokasjonene som må konsolideres, og deretter velger du **Konsolider lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-247">To consolidate inventory, select all the locations that must be consolidated, and then, on the Action Pane, select **Consolidate Inventory**.</span></span>
1. <span data-ttu-id="6c9bf-248">I dialogboksen **Konsolider lager** angir du lokasjonen og bevegelsestypen som skal brukes til å opprette arbeidet for lagerflytting.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-248">In the **Consolidate inventory** dialog box, specify the location and movement type that should be used to create the work for inventory movement.</span></span> <span data-ttu-id="6c9bf-249">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="6c9bf-249">Set the following values:</span></span>

    - <span data-ttu-id="6c9bf-250">**Lokasjon:** *LP-001*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-250">**Location:** *LP-001*</span></span>
    - <span data-ttu-id="6c9bf-251">**Bevegelsestypekode:** *KONSOLIDER*</span><span class="sxs-lookup"><span data-stu-id="6c9bf-251">**Movement type code:** *CONSOLIDATE*</span></span>

1. <span data-ttu-id="6c9bf-252">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-252">Select **OK**.</span></span>
1. <span data-ttu-id="6c9bf-253">Du mottar en informasjonsmelding som viser bevegelsesarbeidet som ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-253">You receive an informational message that shows the movement work that was created.</span></span> <span data-ttu-id="6c9bf-254">Noter bevegelsesarbeids-IDen.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-254">Make a note of the movement work ID.</span></span>

### <a name="view-movement-work"></a><span data-ttu-id="6c9bf-255">Vise bevegelsesarbeid</span><span class="sxs-lookup"><span data-stu-id="6c9bf-255">View movement work</span></span>

1. <span data-ttu-id="6c9bf-256">Gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-256">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="6c9bf-257">Vis arbeidet som ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-257">View the work that was created.</span></span> <span data-ttu-id="6c9bf-258">Bruk IDen for bevegelsesarbeid fra lagerkonsolideringen for å filtrere eller søke i arbeidsrutenettet.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-258">Use the movement work ID from the inventory consolidation to filter or search the work grid.</span></span>

    <span data-ttu-id="6c9bf-259">I dette scenariet ble det brukt en eksisterende lokasjon som hadde lager, som lagerkonsolideringslokasjon.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-259">In this scenario, an existing location that had inventory was used as the inventory consolidation location.</span></span> <span data-ttu-id="6c9bf-260">Derfor ble det bare opprettet én arbeids-ID.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-260">Therefore, only one work ID was created.</span></span>

    > [!NOTE]
   > <span data-ttu-id="6c9bf-261">Systemet oppretter én arbeids-ID for hver flytting som må fullføres.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-261">The system creates one work ID for each move that must be completed.</span></span> <span data-ttu-id="6c9bf-262">Hvis du angir en lokasjon som allerede inneholder lager, opprettes bare én arbeids-ID.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-262">If you specify a location that already contains inventory, only one work ID is created.</span></span> <span data-ttu-id="6c9bf-263">Hvis du angir en ny lokasjon, opprettes det to arbeids-IDer.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-263">If you specify a new location, two work IDs are created.</span></span>
