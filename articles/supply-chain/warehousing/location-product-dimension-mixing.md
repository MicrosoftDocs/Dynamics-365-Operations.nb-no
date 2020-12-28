---
title: Kombinasjon av produktdimensjoner for lokasjon
description: Dette emnet inneholder informasjon om kombinasjon av produktdimensjoner for lokasjon. Denne lokasjonsprofilfunksjonaliteten bidrar til å forbedre lokasjonsstyringen når produktvarianter eller produkter som har dimensjoner, brukes, for eksempel i motebransjen. Den lar deg bestemme om konfigurasjoner, farger, stiler og størrelser kan blandes for en bestemt lokasjonsprofil, eller om bare én av disse dimensjonene eller en kombinasjon av dem kan legges til samme lokasjon.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 73519f3fe79d3d7d917d3044255f735640b8ccfd
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434731"
---
# <a name="location-product-dimension-mixing"></a><span data-ttu-id="d900d-105">Kombinasjon av produktdimensjoner for lokasjon</span><span class="sxs-lookup"><span data-stu-id="d900d-105">Location product dimension mixing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d900d-106">kombinasjon av produktdimensjoner for lokasjon er lokasjonsprofilfunksjonalitet som bidrar til å forbedre lokasjonsstyringen når produktvarianter eller produkter som har dimensjoner, brukes, for eksempel i motebransjen.</span><span class="sxs-lookup"><span data-stu-id="d900d-106">Location product dimension mixing is location profile functionality that helps improve location management when product variants or products that have dimensions are used, such as in the fashion industry.</span></span> <span data-ttu-id="d900d-107">Den lar deg bestemme om konfigurasjoner, farger, stiler og størrelser kan blandes for en bestemt lokasjonsprofil, eller om bare én av disse dimensjonene eller en kombinasjon av dem kan legges til samme lokasjon.</span><span class="sxs-lookup"><span data-stu-id="d900d-107">It lets you decide whether configurations, colors, styles, and sizes can be mixed for a specific location profile, or whether just one of these dimensions or a combination of them can be put to the same location.</span></span>

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a><span data-ttu-id="d900d-108">Slå på funksjonen for kombinasjon av produktdimensjoner for lokasjon</span><span class="sxs-lookup"><span data-stu-id="d900d-108">Turn on the Location product dimension mixing feature</span></span>

<span data-ttu-id="d900d-109">Før du kan bruke kombinasjon av produktdimensjoner for lokasjon, må funksjonen aktiveres i systemet.</span><span class="sxs-lookup"><span data-stu-id="d900d-109">Before you can use location product dimension mixing, the feature must be turned on in your system.</span></span> <span data-ttu-id="d900d-110">Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="d900d-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d900d-111">Funksjonen vises på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="d900d-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d900d-112">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="d900d-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d900d-113">**Funksjonsnavn:** *Kombinasjon av produktdimensjoner for lokasjon*</span><span class="sxs-lookup"><span data-stu-id="d900d-113">**Feature name:** *Location product dimension mixing*</span></span>

## <a name="setup"></a><span data-ttu-id="d900d-114">Installasjon</span><span class="sxs-lookup"><span data-stu-id="d900d-114">Setup</span></span>

<span data-ttu-id="d900d-115">Hver lokasjon på lageret må ha en tilknyttet lokasjonsprofil som beskriver egenskapene til lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="d900d-115">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location.</span></span> <span data-ttu-id="d900d-116">Alle lokasjoner som bruker samme lokasjonsprofil, vil derfor kunne tillate kombinasjon av produktdimensjoner etter at den er satt opp.</span><span class="sxs-lookup"><span data-stu-id="d900d-116">Therefore, all locations that use the same location profile will be able to allow product dimension mixing after it has been set up.</span></span>

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a><span data-ttu-id="d900d-117">Konfigurere lokasjonsprofiler for å tillate kombinasjon av produktdimensjoner</span><span class="sxs-lookup"><span data-stu-id="d900d-117">Configure location profiles to allow product dimension mixing</span></span>

1. <span data-ttu-id="d900d-118">Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="d900d-118">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="d900d-119">Velg **BULK** i listen over lokasjonsprofiler.</span><span class="sxs-lookup"><span data-stu-id="d900d-119">In the list of location profiles, select **BULK**.</span></span>
1. <span data-ttu-id="d900d-120">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="d900d-120">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="d900d-121">I **Generelt**-hurtigfanen setter du **Aktiver spesifikk kombinasjon av produktdimensjoner for lokasjon** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="d900d-121">On the **General** FastTab, set the **Enable location product dimension specific mixing** option to *Yes*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d900d-122">Du kan bare sette dette alternativet til *Ja* hvis **Tillat blandede varer** er satt til *Nei*.</span><span class="sxs-lookup"><span data-stu-id="d900d-122">You can set this option to *Yes* only if the **Allow mixed items** option is set to *No*.</span></span>

1. <span data-ttu-id="d900d-123">I **Tillat kombinasjon av produktdimensjon**-hurtigfanen setter du **Størrelse** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="d900d-123">On the **Allowed product dimension mixing** FastTab, set the **Size** option to *Yes*.</span></span> <span data-ttu-id="d900d-124">I scenariet som beskrives i dette emnet, kan du bare foreta en blanding for produkter som har ulike **Størrelse**-dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="d900d-124">In the scenario that is described in this topic, mixing can be done only for products that have different **Size** dimensions.</span></span> <span data-ttu-id="d900d-125">Andre alternativer er også tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="d900d-125">However, other options are also available.</span></span>
1. <span data-ttu-id="d900d-126">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="d900d-126">Select **Save**.</span></span>

### <a name="create-a-new-product-master-and-product-variants"></a><span data-ttu-id="d900d-127">Opprett en ny produktstandard og produktvarianter</span><span class="sxs-lookup"><span data-stu-id="d900d-127">Create a new product master and product variants</span></span>

1. <span data-ttu-id="d900d-128">Gå til **Behandling av produktinformasjon \> Produkter \> Produktstandarder**.</span><span class="sxs-lookup"><span data-stu-id="d900d-128">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="d900d-129">I handlingsruten velger du **Ny** for å opprette en produktstandard.</span><span class="sxs-lookup"><span data-stu-id="d900d-129">On the Action Pane, select **New** to create a product master.</span></span>
1. <span data-ttu-id="d900d-130">Angi følgende verdier i dialogboksen **Nytt produkt**:</span><span class="sxs-lookup"><span data-stu-id="d900d-130">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d900d-131">**Produkttype:** *Vare*</span><span class="sxs-lookup"><span data-stu-id="d900d-131">**Product type:** *Item*</span></span>
    - <span data-ttu-id="d900d-132">**Produktundertype:** *Produktstandard*</span><span class="sxs-lookup"><span data-stu-id="d900d-132">**Product subtype:** *Product master*</span></span>
    - <span data-ttu-id="d900d-133">**Produktnummer:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="d900d-133">**Product number:** *B0001*</span></span>
    - <span data-ttu-id="d900d-134">**Produktnavn:** *B0001 Størrelse*</span><span class="sxs-lookup"><span data-stu-id="d900d-134">**Product name:** *B0001 Size*</span></span>
    - <span data-ttu-id="d900d-135">**Produktdimensjonsgruppe:** *Størrelse*</span><span class="sxs-lookup"><span data-stu-id="d900d-135">**Product dimension group:** *Size*</span></span>
    - <span data-ttu-id="d900d-136">**Konfigurasjonsteknologi:** *Forhåndsdefinert variant*</span><span class="sxs-lookup"><span data-stu-id="d900d-136">**Configuration technology:** *Predefined variant*</span></span>

1. <span data-ttu-id="d900d-137">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d900d-137">Select **OK**.</span></span>
1. <span data-ttu-id="d900d-138">På **Produktdetaljer**-siden på **Generelt**-hurtigfanen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d900d-138">On the **Product details** page, on the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d900d-139">**Generer varianter automatisk:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="d900d-139">**Generate variants automatically:** *Yes*</span></span>
    - <span data-ttu-id="d900d-140">**Størrelsesgruppe:** *CASUALDHIR*</span><span class="sxs-lookup"><span data-stu-id="d900d-140">**Size group:** *CASUALDHIR*</span></span>

1. <span data-ttu-id="d900d-141">Hvis du vil vise de forhåndsdefinerte variantene, velger du **Produktvarianter** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d900d-141">To view the predefined variants, on the Action Pane, select **Product variants**.</span></span>

    <span data-ttu-id="d900d-142">**Produktvarianter**-siden vises og viser en liste over varianter fra konfigurasjonen av størrelsesgruppen.</span><span class="sxs-lookup"><span data-stu-id="d900d-142">The **Product variants** page appears and shows a list of variants from the configuration of the size group.</span></span>

### <a name="release-products-to-the-usmf-company"></a><span data-ttu-id="d900d-143">Frigi produkter til USMF-firmaet</span><span class="sxs-lookup"><span data-stu-id="d900d-143">Release products to the USMF company</span></span>

1. <span data-ttu-id="d900d-144">I handlingsruten velger du **Frigi produkter**.</span><span class="sxs-lookup"><span data-stu-id="d900d-144">On the Action Pane, select **Release products**.</span></span>
1. <span data-ttu-id="d900d-145">På **Velg produkter som skal frigis**-siden bekrefter du at produktnummeret *B0001* er i listen, og deretter velger du **Neste**.</span><span class="sxs-lookup"><span data-stu-id="d900d-145">On the **Select products to release** page, confirm that product number *B0001* is in the list, and then select **Next**.</span></span>
1. <span data-ttu-id="d900d-146">Velg **Neste** for å bekrefte produktvariantene som skal frigis.</span><span class="sxs-lookup"><span data-stu-id="d900d-146">Select **Next** to confirm the product variants to release.</span></span>
1. <span data-ttu-id="d900d-147">Velg *USMF* på siden **Velg firmaer du vil frigi til**, og velg deretter **Neste** for å bekrefte valget.</span><span class="sxs-lookup"><span data-stu-id="d900d-147">On the **Select companies to release to** page, select *USMF*, and then select **Next** to confirm the selection.</span></span>
1. <span data-ttu-id="d900d-148">Velg **Fullfør** på **Bekreft merking**-siden for å fullføre frigivelsen.</span><span class="sxs-lookup"><span data-stu-id="d900d-148">On the **Confirm selection** page, select **Finish** to complete the release.</span></span>

    <span data-ttu-id="d900d-149">Du får en melding om at operasjonen er fullført.</span><span class="sxs-lookup"><span data-stu-id="d900d-149">You receive an "Operation completed" message.</span></span>

### <a name="update-a-released-product-in-the-usmf-company"></a><span data-ttu-id="d900d-150">Oppdatere et frigitt produkt i USMF firmaet</span><span class="sxs-lookup"><span data-stu-id="d900d-150">Update a released product in the USMF company</span></span>

1. <span data-ttu-id="d900d-151">Kontroller at du er logget på **USMF**-firmaet.</span><span class="sxs-lookup"><span data-stu-id="d900d-151">Make sure that you're signed in to the **USMF** company.</span></span>
1. <span data-ttu-id="d900d-152">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter** for å fullføre oppretting av frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="d900d-152">Go to **Product information management \> Products \> Released products** to finish creating the released product.</span></span>
1. <span data-ttu-id="d900d-153">Finn og velg varenummer *B0001* for å åpne **Detaljer om frigitt produkt**-siden.</span><span class="sxs-lookup"><span data-stu-id="d900d-153">Find and select item number *B0001* to open the **Released product details** page.</span></span>
1. <span data-ttu-id="d900d-154">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="d900d-154">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="d900d-155">I **Generelt**-hurtigfanen kontrollerer du at **Varemodellgruppe** er satt til *FIFO*.</span><span class="sxs-lookup"><span data-stu-id="d900d-155">On the **General** FastTab, make sure that the **Item model group** field is set to *FIFO*.</span></span>
1. <span data-ttu-id="d900d-156">I gruppen **Oppsett** i fanen **Produkt** i handlingsruten velger du **Dimensjonsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="d900d-156">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Dimension groups**.</span></span>
1. <span data-ttu-id="d900d-157">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d900d-157">Set the following values:</span></span>

    - <span data-ttu-id="d900d-158">**Lagringsdimensjonsgruppe:** *Bølge*</span><span class="sxs-lookup"><span data-stu-id="d900d-158">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="d900d-159">**Sporingsdimensjonsgruppe:** *Ingen*</span><span class="sxs-lookup"><span data-stu-id="d900d-159">**Tracking dimension group:** *None*</span></span>

1. <span data-ttu-id="d900d-160">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d900d-160">Select **OK**.</span></span>
1. <span data-ttu-id="d900d-161">I gruppen **Oppsett** i fanen **Produkt** i handlingsruten velger du **Reservasjonshierarki**.</span><span class="sxs-lookup"><span data-stu-id="d900d-161">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Reservation hierarchy**.</span></span>
1. <span data-ttu-id="d900d-162">Sett **Reservasjonshierarki**-feltet til *Standard*, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="d900d-162">Set the **Reservation hierarchy** field to *Default*, and then select **OK**.</span></span>
1. <span data-ttu-id="d900d-163">I delen **Administrasjon** i hurtigfanen **Generelt** ser du at valgene er oppdatert.</span><span class="sxs-lookup"><span data-stu-id="d900d-163">On the **General** FastTab, in the **Administration** section, notice that your selections have been updated.</span></span>
1. <span data-ttu-id="d900d-164">Angi *10* i **Pris**-feltet på hurtigfanen **Kjøp**.</span><span class="sxs-lookup"><span data-stu-id="d900d-164">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="d900d-165">På hurtigfanen **Styr kostnader** i feltet **Varegruppe** angir du *Lyd*.</span><span class="sxs-lookup"><span data-stu-id="d900d-165">On the **Manage costs** FastTab, in the **Item group** field, enter *Audio*.</span></span>
1. <span data-ttu-id="d900d-166">Angi *10* i **Pris**-feltet på hurtigfanen **Kjøp**.</span><span class="sxs-lookup"><span data-stu-id="d900d-166">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="d900d-167">På **LAger**-hurtigfanen angir du *ea* i **Sekvensgruppe-ID for enhet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d900d-167">On the **Warehouse** FastTab, in the **Unit sequence group ID** field, enter *ea*.</span></span>
1. <span data-ttu-id="d900d-168">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="d900d-168">Select **Save**.</span></span>

### <a name="create-a-location-directive"></a><span data-ttu-id="d900d-169">Opprette et lokasjonsdirektiv</span><span class="sxs-lookup"><span data-stu-id="d900d-169">Create a location directive</span></span>

1. <span data-ttu-id="d900d-170">Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.</span><span class="sxs-lookup"><span data-stu-id="d900d-170">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d900d-171">I den venstre ruten i **Arbeidsordretype**-feltet velger du *Bestillinger*.</span><span class="sxs-lookup"><span data-stu-id="d900d-171">In the left pane, in the **Work order type** field, select *Purchase orders*.</span></span>
1. <span data-ttu-id="d900d-172">I listen velger du lokasjonsdirektivet som har navnet *24 PO Direct*.</span><span class="sxs-lookup"><span data-stu-id="d900d-172">In the list, select the location directive that is named *24 PO Direct*.</span></span>
1. <span data-ttu-id="d900d-173">På hurtigfanen **Lokasjonsdirektivhandlinger** velger du **Ny** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="d900d-173">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d900d-174">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d900d-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d900d-175">**Sekvensnummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="d900d-175">**Sequence number:** *1*</span></span>

        <span data-ttu-id="d900d-176">Den nye linjen skal være foran den tidligere eksisterende linjen.</span><span class="sxs-lookup"><span data-stu-id="d900d-176">The new line should be in front of the previously existing line.</span></span> <span data-ttu-id="d900d-177">Hvis du vil gjøre endringen, bruker du knappene **Flytt opp** og **Flytt ned** på verktøylinjen, eller endrer den eksisterende linjens **Sekvensnummer**-verdi til *2*.</span><span class="sxs-lookup"><span data-stu-id="d900d-177">To make the change, use the **Move up** and **Move down** buttons on the toolbar, or change the existing line's **Sequence number** value to *2*.</span></span>

    - <span data-ttu-id="d900d-178">**Navn:** *Plasser i BULK-lokasjonsprofil*</span><span class="sxs-lookup"><span data-stu-id="d900d-178">**Name:** *Put to BULK Location profile*</span></span>
    - <span data-ttu-id="d900d-179">**Bruk av fast lokasjon:** *Faste og ikke-faste lokasjoner*</span><span class="sxs-lookup"><span data-stu-id="d900d-179">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>
    - <span data-ttu-id="d900d-180">**Tillat negativ beholdning:** *Fjern merket i denne avmerkingsboksen (= Nei)*</span><span class="sxs-lookup"><span data-stu-id="d900d-180">**Allow negative inventory:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="d900d-181">**Parti aktivert:** *Fjern merket i denne avmerkingsboksen (= Nei)*</span><span class="sxs-lookup"><span data-stu-id="d900d-181">**Batch enabled:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="d900d-182">**Strategi:** *Ingen*</span><span class="sxs-lookup"><span data-stu-id="d900d-182">**Strategy:** *None*</span></span>

1. <span data-ttu-id="d900d-183">Mens den nye linjen fremdeles er valgt, velger du **Rediger spørring** over rutenettet.</span><span class="sxs-lookup"><span data-stu-id="d900d-183">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="d900d-184">I spørringsdialogboksen, på **Område**-fanen, velger du **Legg til** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="d900d-184">In the query dialog box, on the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="d900d-185">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d900d-185">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d900d-186">**Tabell:** *Plasseringer*</span><span class="sxs-lookup"><span data-stu-id="d900d-186">**Table:** *Locations*</span></span>
    - <span data-ttu-id="d900d-187">**Avledet tabell:** *Lokasjoner*</span><span class="sxs-lookup"><span data-stu-id="d900d-187">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="d900d-188">**Felt:** *ID for lokasjonsprofil*</span><span class="sxs-lookup"><span data-stu-id="d900d-188">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="d900d-189">**Vilkår:** *BULK*</span><span class="sxs-lookup"><span data-stu-id="d900d-189">**Criteria:** *BULK*</span></span>

1. <span data-ttu-id="d900d-190">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d900d-190">Select **OK**.</span></span>
1. <span data-ttu-id="d900d-191">Velg **Lagre** i handlingsruten på **Lokasjonsdirektiver**-siden.</span><span class="sxs-lookup"><span data-stu-id="d900d-191">On the **Location directives** page, on the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="d900d-192">På **Lokasjonsdirektivhandlinger**-hurtigfanen **Strategi**-feltet, hvis du bruker lokasjonsstrategien *Konsolidering*, overstyres oppsettet på **Tillatt kombinasjon av produktdimensjon**-hurtigfanen på **Lokasjonsprofiler**, og varene vil bli plassert på samme lokasjon, selv om denne virkemåten ikke er tillatt i oppsettet.</span><span class="sxs-lookup"><span data-stu-id="d900d-192">On the **Location Directive Actions** FastTab **Strategy** field, if you use the *Consolidate* location strategy, the setup of the **Allowed product dimension mixing** FastTab on the **Location profiles** will be overridden, and items will be put to the same location even if this behavior isn't allowed by the setup.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="d900d-193">Opprette et menyelement for mobilenhet</span><span class="sxs-lookup"><span data-stu-id="d900d-193">Create a mobile device menu item</span></span>

1. <span data-ttu-id="d900d-194">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="d900d-194">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="d900d-195">Velg **Ny** i handlingsruten for å opprette et menyelement som skal brukes til sortering.</span><span class="sxs-lookup"><span data-stu-id="d900d-195">On the Action Pane, select **New** to create a menu item to use for sorting.</span></span>
1. <span data-ttu-id="d900d-196">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d900d-196">In the header, set the following values:</span></span>

    - <span data-ttu-id="d900d-197">**Menyelementnavn:** *PO-linjemottak*</span><span class="sxs-lookup"><span data-stu-id="d900d-197">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="d900d-198">**Tittel:** *PO-linjemottak*</span><span class="sxs-lookup"><span data-stu-id="d900d-198">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="d900d-199">**Modus:** *Arbeid*</span><span class="sxs-lookup"><span data-stu-id="d900d-199">**Mode:** *Work*</span></span>
    - <span data-ttu-id="d900d-200">**Bruke eksisterende arbeid:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="d900d-200">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="d900d-201">Angi følgende verdier i **Generelt**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="d900d-201">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d900d-202">**Arbeidsopprettingsprosess:** *Bestillingslinjemottak og -plassering*</span><span class="sxs-lookup"><span data-stu-id="d900d-202">**Work creation process:** *Purchase order line receiving and putaway*</span></span>
    - <span data-ttu-id="d900d-203">**Generer nummerskilt:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="d900d-203">**Generate license plate:** *Yes*</span></span>

1. <span data-ttu-id="d900d-204">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="d900d-204">Select **Save**.</span></span>

### <a name="configure-the-mobile-device-menu"></a><span data-ttu-id="d900d-205">Konfigurere mobilenhetsmenyen</span><span class="sxs-lookup"><span data-stu-id="d900d-205">Configure the mobile device menu</span></span>

1. <span data-ttu-id="d900d-206">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="d900d-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="d900d-207">Velg **Inngående** i listen over menyer.</span><span class="sxs-lookup"><span data-stu-id="d900d-207">In the list of menus, select **Inbound**.</span></span>
1. <span data-ttu-id="d900d-208">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="d900d-208">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="d900d-209">I **Tilgjengelige menyer og menyelementer**-listen finner og velger du **PO-linjemottak**-menyelementet.</span><span class="sxs-lookup"><span data-stu-id="d900d-209">In the **Available Menus And Menu Items** list, find and select the **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="d900d-210">Velg høyre pil for å flytte **PO-linjemottak**-menyelementet til **Menystruktur**-listen.</span><span class="sxs-lookup"><span data-stu-id="d900d-210">Select the right arrow button to move the **PO line receiving** menu item to the **Menu Structure** list.</span></span> <span data-ttu-id="d900d-211">På denne måten legger du til det nye menyelementet på den valgte menyen.</span><span class="sxs-lookup"><span data-stu-id="d900d-211">In this way, you add your new menu item to the selected menu.</span></span>
1. <span data-ttu-id="d900d-212">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="d900d-212">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="d900d-213">Scenario</span><span class="sxs-lookup"><span data-stu-id="d900d-213">Scenario</span></span>

<span data-ttu-id="d900d-214">Dette demonstrasjonsscenarioet viser hvordan to ulike produktvarianter kan plasseres på samme lokasjon når lokasjonsprofilen ikke tillater blandede varer, men *Kombinasjon av produktdimensjoner for lokasjon*-funksjonen er aktivert.</span><span class="sxs-lookup"><span data-stu-id="d900d-214">This demo scenario shows how two different product variants can be put to the same location when the location profile doesn't allow for mixed items, but the *Location product dimension mixing* feature is enabled.</span></span> <span data-ttu-id="d900d-215">I dette tilfellet skal du bruke **Størrelse**-varianten som kriterium.</span><span class="sxs-lookup"><span data-stu-id="d900d-215">In this case, you will use the **Size** variant as the criterion.</span></span>

<span data-ttu-id="d900d-216">Før du begynner, må du kontrollere at det finnes tomme lokasjoner på lager *24* som bruker *BULK*-lokasjonsprofilen.</span><span class="sxs-lookup"><span data-stu-id="d900d-216">Before you begin, make sure that there are empty locations in warehouse *24* that use the *BULK* location profile.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="d900d-217">Opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="d900d-217">Create a purchase order</span></span>

<span data-ttu-id="d900d-218">Du oppretter en bestilling som har tre linjer: to linjer for samme produktnummer, men forskjellige **Størrelse**-varianter, og en tredje linje for et annet produkt som ikke har noen varianter.</span><span class="sxs-lookup"><span data-stu-id="d900d-218">You will create a purchase order that has three lines: two lines for the same product number but different **Size** variants, and a third line for a different product that has no variants.</span></span>

1. <span data-ttu-id="d900d-219">Gå til **Leverandører \> Bestillinger \> Alle bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="d900d-219">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="d900d-220">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d900d-220">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d900d-221">I **Opprett bestilling**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d900d-221">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d900d-222">**Leverandørkonto:** *1001*</span><span class="sxs-lookup"><span data-stu-id="d900d-222">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="d900d-223">**Lager:** *24*</span><span class="sxs-lookup"><span data-stu-id="d900d-223">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="d900d-224">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d900d-224">Select **OK**.</span></span>
1. <span data-ttu-id="d900d-225">Bestillingen opprettes, og det legges til en ny linje på **Bestillingslinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="d900d-225">The purchase order is created, and a new line is added on the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="d900d-226">Noter deg bestillingsnummeret.</span><span class="sxs-lookup"><span data-stu-id="d900d-226">Make a note of the purchase order number.</span></span>
1. <span data-ttu-id="d900d-227">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d900d-227">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d900d-228">**Varenummer:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="d900d-228">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="d900d-229">**Størrelse** *L*</span><span class="sxs-lookup"><span data-stu-id="d900d-229">**Size** *L*</span></span>
    - <span data-ttu-id="d900d-230">**Antall:** *2*</span><span class="sxs-lookup"><span data-stu-id="d900d-230">**Quantity:** *2*</span></span>

1. <span data-ttu-id="d900d-231">Velg **Legg til linje** over rutenettet for å legge til en ny bestillingslinje, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d900d-231">Select **Add line** above the grid to add a second purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="d900d-232">**Varenummer:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="d900d-232">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="d900d-233">**Størrelse** *XL*</span><span class="sxs-lookup"><span data-stu-id="d900d-233">**Size** *XL*</span></span>
    - <span data-ttu-id="d900d-234">**Antall:** *2*</span><span class="sxs-lookup"><span data-stu-id="d900d-234">**Quantity:** *2*</span></span>

1. <span data-ttu-id="d900d-235">Velg **Legg til linje** for å legge til en tredje bestillingslinje, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d900d-235">Select **Add line** to add a third purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="d900d-236">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d900d-236">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d900d-237">**Antall:** *1*</span><span class="sxs-lookup"><span data-stu-id="d900d-237">**Quantity:** *1*</span></span>

<span data-ttu-id="d900d-238">1. Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="d900d-238">1.Select **Save**.</span></span>

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a><span data-ttu-id="d900d-239">Motta bestillingslinjer i lagerappen</span><span class="sxs-lookup"><span data-stu-id="d900d-239">Receive purchase order lines in the warehouse app</span></span>

1. <span data-ttu-id="d900d-240">Logg på lagerappen som en bruker som er aktivert for lager *24*.</span><span class="sxs-lookup"><span data-stu-id="d900d-240">Sign in to the warehouse app as a user who is enabled for warehouse *24*.</span></span>
1. <span data-ttu-id="d900d-241">Velg **Inngående**-menyen.</span><span class="sxs-lookup"><span data-stu-id="d900d-241">Select the **Inbound** menu.</span></span>
1. <span data-ttu-id="d900d-242">Velg **PO-linjemottak**.</span><span class="sxs-lookup"><span data-stu-id="d900d-242">Select **PO Line receiving**.</span></span>
1. <span data-ttu-id="d900d-243">Velg **PONUM**-feltet, og angi bestillingsnummeret.</span><span class="sxs-lookup"><span data-stu-id="d900d-243">Select the **PONUM** field, and then enter the purchase order number.</span></span>
1. <span data-ttu-id="d900d-244">Bekreft oppføringen ved å velge Bekreft-knappen (✔) nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="d900d-244">Confirm your entry by selecting the confirm button ( ✔ ) at the bottom of the page.</span></span>
1. <span data-ttu-id="d900d-245">Angi linjenummeret fra bestillingen som mottas.</span><span class="sxs-lookup"><span data-stu-id="d900d-245">Enter the line number from the purchase order that is being received.</span></span> <span data-ttu-id="d900d-246">Velg **LINENUM**-feltet, og bruk deretter talltastaturet til å angi *1*.</span><span class="sxs-lookup"><span data-stu-id="d900d-246">Select the **LINENUM** field, and then use the number pad to enter *1*.</span></span>
1. <span data-ttu-id="d900d-247">Bekreft oppføringen.</span><span class="sxs-lookup"><span data-stu-id="d900d-247">Confirm your entry.</span></span>
1. <span data-ttu-id="d900d-248">Angi antallet som skal mottas.</span><span class="sxs-lookup"><span data-stu-id="d900d-248">Enter the quantity to receive.</span></span> <span data-ttu-id="d900d-249">Velg plusstegn (**+**) to ganger for å øke verdien i **Antall**-feltet til *2*.</span><span class="sxs-lookup"><span data-stu-id="d900d-249">Select the plus sign (**+**) button two times to increase the value in the **Qty** field to *2*.</span></span>
1. <span data-ttu-id="d900d-250">Registrer oppføringen ved å velge knappen (✔) nederst på siden, og bekreft deretter oppføringen ved å velge knappen (✔) på nytt.</span><span class="sxs-lookup"><span data-stu-id="d900d-250">Register your entry by selecting the button ( ✔ ) at the bottom of the page, and then confirm your entry by selecting the button ( ✔ ) again.</span></span>
1. <span data-ttu-id="d900d-251">Vis informasjonen i **Bestillinger: Plasser**-siden.</span><span class="sxs-lookup"><span data-stu-id="d900d-251">View the information on the **Purchase orders: Put** page.</span></span> <span data-ttu-id="d900d-252">Denne siden viser arbeidet som er opprettet for plasseringen (Arbeid 1).</span><span class="sxs-lookup"><span data-stu-id="d900d-252">This page shows the work that has been created for the put-away (Work 1).</span></span>

    <span data-ttu-id="d900d-253">Lokasjonen der den mottatte varen vil plasseres, nummerskiltet, varen, størrelsen og antallet i den **PO-linjemottak**-oppgaven som du nettopp har fullført, vises.</span><span class="sxs-lookup"><span data-stu-id="d900d-253">The location where the received item will be put away, the license plate, the item, the size, and the quantity of the **PO Line receiving** task that you just completed are shown.</span></span>

1. <span data-ttu-id="d900d-254">Bekreft plasseringsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="d900d-254">Confirm the put-away work.</span></span>
1. <span data-ttu-id="d900d-255">Gjenta trinnene 4 til og med 11 for bestillingslinje 2.</span><span class="sxs-lookup"><span data-stu-id="d900d-255">Repeat the steps 4 through 11 for the purchase order line 2.</span></span> <span data-ttu-id="d900d-256">I trinn 8 angir du imidlertid et antall på *1*.</span><span class="sxs-lookup"><span data-stu-id="d900d-256">However, in step 8, specify a quantity of *1*.</span></span>

    <span data-ttu-id="d900d-257">Det opprettes nytt plasseringsarbeid (Arbeid 2) for samme lokasjon som Arbeid 1.</span><span class="sxs-lookup"><span data-stu-id="d900d-257">New put-away work (Work 2) is created for the same location as Work 1.</span></span>

1. <span data-ttu-id="d900d-258">Gjenta trinnene 4 til og med 11 igjen for bestillingslinje 2.</span><span class="sxs-lookup"><span data-stu-id="d900d-258">Repeat the steps 4 through 11 again for purchase order line 2.</span></span> <span data-ttu-id="d900d-259">I trinn 8 angir du gjenværende antall på *1*.</span><span class="sxs-lookup"><span data-stu-id="d900d-259">In step 8, specify the remaining quantity of *1*.</span></span>

    <span data-ttu-id="d900d-260">Det opprettes nytt plasseringsarbeid (Arbeid 3) for samme lokasjon som Arbeid 1 og Arbeid 2.</span><span class="sxs-lookup"><span data-stu-id="d900d-260">New put-away work (Work 3) is created for the same location as Work 1 and Work 2.</span></span> <span data-ttu-id="d900d-261">Dette skjer fordi *Konsolidering*-lokasjonsdirektivstrategien brukes, og **Tillatt kombinasjon av produktdimensjon**-hurtigfanen på *Bulk*-**lokasjonsprofiler**-oppsettet gjør at **Størrelse**-varianten kan blandes på en lokasjon.</span><span class="sxs-lookup"><span data-stu-id="d900d-261">This behavior occurs because the *Consolidate* location directive strategy is used, and the **Allowed product dimension mixing** FastTab on the *Bulk* **Location profiles** setup allows the **Size** variant to be mixed on a location.</span></span>

1. <span data-ttu-id="d900d-262">Gjenta trinnene 4 til og med 11 for bestillingslinje 3.</span><span class="sxs-lookup"><span data-stu-id="d900d-262">Repeat the steps 4 through 11 for purchase order line 3.</span></span> <span data-ttu-id="d900d-263">I trinn 8 angir du et antall på *1* for varenummer *A0001*.</span><span class="sxs-lookup"><span data-stu-id="d900d-263">In step 8, specify a quantity of *1* for item number *A0001*.</span></span>

    <span data-ttu-id="d900d-264">Nytt plasseringsarbeid (Arbeid 4) opprettes for en annen lokasjon enn lokasjonen som brukes for bestillingslinje 1 og 2.</span><span class="sxs-lookup"><span data-stu-id="d900d-264">New put-away work (Work 4) is created for a different location than the location that is used for purchase order lines 1 and 2.</span></span> <span data-ttu-id="d900d-265">Dette problemet oppstår fordi lokasjonsprofilen ikke tillater blandede produkter, men den tillater blandede dimensjoner av samme produktstandard.</span><span class="sxs-lookup"><span data-stu-id="d900d-265">This behavior occurs because the location profile doesn't allow for mixed products, but it does allow for mixed dimensions of the same product master.</span></span>

1. <span data-ttu-id="d900d-266">Velg menyknappen øverst på siden (noen ganger kalt hamburger eller hamburgerknappen), og velg deretter **Avbryt** for å avslutte **PO-linjemottak**.</span><span class="sxs-lookup"><span data-stu-id="d900d-266">Select the Menu button at the top of the page (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit **PO Line receiving**.</span></span>

> [!TIP]
> <span data-ttu-id="d900d-267">Du kan gjenta dette scenariet, men denne gangen angir **Størrelse** - *Nei* under **Tillat kombinasjon av produktdimensjon**-hurtigfanen på *BULK*-**lokasjonsprofiler**, slik at ingen av produktdimensjoner kan blandes.</span><span class="sxs-lookup"><span data-stu-id="d900d-267">You can repeat this scenario, but this time, set **Size** - *No* under the **Allow product dimension mixing** FastTab on the *BULK* **Location profiles**, so that none of the product dimensions can be mixed.</span></span> <span data-ttu-id="d900d-268">I dette tilfellet vil hver produktvariant bli satt til en ny lokasjon når du mottar bestillingen.</span><span class="sxs-lookup"><span data-stu-id="d900d-268">In this case, when you receive the purchase order, each product variant will be put to a new location.</span></span>