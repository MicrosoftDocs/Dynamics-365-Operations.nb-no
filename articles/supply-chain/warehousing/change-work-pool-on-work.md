---
title: Endre arbeidspulje i arbeid
description: Dette emnet beskriver hvordan du kan bruke knappen for Endre arbeidspulje for arbeidselementer til å endre arbeidsutvalget for eksisterende arbeid.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 344918b77334f9aca11f799f8c031047ad229ee0
ms.sourcegitcommit: d25d0feb3f8a5a760eba50ba5f46e1db02737d25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677368"
---
# <a name="change-work-pool-on-work"></a><span data-ttu-id="6a2fc-103">Endre arbeidspulje i arbeid</span><span class="sxs-lookup"><span data-stu-id="6a2fc-103">Change work pool on work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a2fc-104">Du kan bruke arbeidspuljer for å organisere arbeidet i grupper.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-104">You can use work pools to organize work into groups.</span></span> <span data-ttu-id="6a2fc-105">Du kan for eksempel opprette en arbeidspulje for å klassifisere arbeid som skjer på en spesifikk lagerlokasjon.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-105">For example, you can create a work pool to classify work that occurs in a specific warehouse location.</span></span>

<span data-ttu-id="6a2fc-106">Funksjonen *Endre arbeidspulje i arbeid* legger til en knapp for **Endre arbeidsutvalg** i handlingsruten for arbeidselementer.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-106">The *Change work pool on work* feature adds a **Change work pool** button to the Action Pane for work items.</span></span> <span data-ttu-id="6a2fc-107">Derfor kan lagerledere enkelt endre arbeidsutvalget for eksisterende arbeid.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-107">Therefore, warehouse managers can easily change the work pool of existing work.</span></span> <span data-ttu-id="6a2fc-108">Med denne funksjonen kan ledere reagere raskt på endringer på shop floor på lageret, og det bidrar til å forbedre muligheten til å tilpasse seg endrede situasjoner og behovet for å overføre arbeid til andre arbeidsgrupper.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-108">This feature lets managers react quickly to changes on the warehouse shop floor, and it helps improve their ability to adapt to changing situations and the need to transfer work to another work pool.</span></span>

## <a name="turn-on-the-change-work-pool-on-work-feature"></a><span data-ttu-id="6a2fc-109">Aktivere funksjonen Endre arbeidspulje i arbeid</span><span class="sxs-lookup"><span data-stu-id="6a2fc-109">Turn on the Change work pool on work feature</span></span>

<span data-ttu-id="6a2fc-110">Før du begynner å definere eller bruke denne funksjonen må du kontrollere at den er tilgjengelig i systemet.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-110">Before you begin to set up or use this feature, you must make sure that it's available in your system.</span></span> <span data-ttu-id="6a2fc-111">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="6a2fc-112">I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="6a2fc-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="6a2fc-113">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="6a2fc-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="6a2fc-114">**Funksjonsnavn:** *Endre arbeidspulje i arbeid*</span><span class="sxs-lookup"><span data-stu-id="6a2fc-114">**Feature name:** *Change work pool on work*</span></span>

## <a name="set-up-the-change-work-pool-on-work-feature"></a><span data-ttu-id="6a2fc-115">Konfigurere funksjonen Endre arbeidspulje i arbeid</span><span class="sxs-lookup"><span data-stu-id="6a2fc-115">Set up the Change work pool on work feature</span></span>

<span data-ttu-id="6a2fc-116">Hvis du vil bruke denne funksjonen, må du ha noen arbeidsgrupper konfigurert.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-116">To use this feature, you must have some work pools set up.</span></span> <span data-ttu-id="6a2fc-117">Du kan også definere arbeidsmalene, slik at de automatisk tilordner et utvalg.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-117">You might also set up your work templates so that they automatically assign a pool.</span></span> <span data-ttu-id="6a2fc-118">Hvis du vil arbeide med eksempelscenarioet som er oppgitt senere i dette emnet, setter du opp systemet som beskrevet i denne delen.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-118">If you want to work through the example scenario that is provided later in this topic, set up your system as described in this section.</span></span>

### <a name="set-up-work-pools"></a><span data-ttu-id="6a2fc-119">Definere arbeidspuljer</span><span class="sxs-lookup"><span data-stu-id="6a2fc-119">Set up work pools</span></span>

<span data-ttu-id="6a2fc-120">I arbeidsutvalg kan du organisere arbeidselementer etter type.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-120">Work pools let you organize work items by type.</span></span> <span data-ttu-id="6a2fc-121">Hvis du vil arbeide med funksjonen *Endre arbeidspulje i arbeid*, må du ha minst to arbeidsgrupper tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-121">To work with the *Change work pool on work* feature, you must have at least two work pools available.</span></span> <span data-ttu-id="6a2fc-122">Følg denne fremgangsmåten for å vise og legge til arbeidspuljer.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-122">To view and add work pools, follow these steps.</span></span>

1. <span data-ttu-id="6a2fc-123">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsutvalg**.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-123">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="6a2fc-124">Hvis du arbeider med demonstrasjonsdata fra **USMF**-firmaet og vil arbeide deg gjennom eksempelscenarioet senere i dette emnet, legger du til to arbeidsgrupper som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="6a2fc-124">If you're working with demo data from the **USMF** company and will work through the example scenario later in this topic, add two work pools that have the following settings:</span></span>

    - <span data-ttu-id="6a2fc-125">Arbeidspulje 1:</span><span class="sxs-lookup"><span data-stu-id="6a2fc-125">Work pool 1:</span></span>

        - <span data-ttu-id="6a2fc-126">**ID for arbeidsutvalg:** *WebShop*</span><span class="sxs-lookup"><span data-stu-id="6a2fc-126">**Work pool ID:** *Webshop*</span></span>
        - <span data-ttu-id="6a2fc-127">**Beskrivelse:** *WebShop*</span><span class="sxs-lookup"><span data-stu-id="6a2fc-127">**Description:** *Web Shop*</span></span>

    - <span data-ttu-id="6a2fc-128">Arbeidspulje 2:</span><span class="sxs-lookup"><span data-stu-id="6a2fc-128">Work pool 2:</span></span>

        - <span data-ttu-id="6a2fc-129">**ID for arbeidsutvalg:** *CallCenter*</span><span class="sxs-lookup"><span data-stu-id="6a2fc-129">**Work pool ID:** *CallCenter*</span></span>
        - <span data-ttu-id="6a2fc-130">**Beskrivelse:** *Telefonsenter*</span><span class="sxs-lookup"><span data-stu-id="6a2fc-130">**Description:** *Call Center*</span></span>

1. <span data-ttu-id="6a2fc-131">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-131">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="6a2fc-132">Konfigurer arbeidsmaler</span><span class="sxs-lookup"><span data-stu-id="6a2fc-132">Set up work templates</span></span>

<span data-ttu-id="6a2fc-133">For hver av arbeidsmalene kan du angi et standard arbeidsutvalg, i henhold til hva du trenger.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-133">For each of your work templates, you can set a default work pool, as you require.</span></span> <span data-ttu-id="6a2fc-134">For hver relevante mal tilordner du et arbeidsutvalg i kolonnen **ID for arbeidsutvalg**.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-134">For each relevant template, you assign a work pool in the **Work pool ID** column.</span></span> <span data-ttu-id="6a2fc-135">I dette tilfellet vil alle arbeidselementer som genereres ved hjelp av en gitt mal, automatisk arve det tilordnede arbeidsutvalget.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-135">In this case, all work items that are generated by using a given template automatically inherit the assigned work pool.</span></span> <span data-ttu-id="6a2fc-136">Hvis du arbeider med demonstrasjonsdata fra **USMF**-firmaet og vil arbeide deg gjennom eksempelscenarioet senere i dette emnet, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-136">If you're working with the demo data from the **USMF** company and will work through the example scenario later in this topic, follow these steps.</span></span>

1. <span data-ttu-id="6a2fc-137">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-137">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="6a2fc-138">I handlingsruten velger du **Rediger** for å legge siden inn i redigeringsmodus.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-138">On the Action Pane, select **Edit** to put the page into editing mode.</span></span>
1. <span data-ttu-id="6a2fc-139">Rediger malen ved å angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="6a2fc-139">Edit the template by setting the following values:</span></span>

    - <span data-ttu-id="6a2fc-140">**Arbeidsmal:** *62 Plukk til pakke*</span><span class="sxs-lookup"><span data-stu-id="6a2fc-140">**Work template:** *62 Pick to pack*</span></span>
    - <span data-ttu-id="6a2fc-141">**ID for arbeidsutvalg:** *WebShop*</span><span class="sxs-lookup"><span data-stu-id="6a2fc-141">**Work pool ID:** *Webshop*</span></span>

1. <span data-ttu-id="6a2fc-142">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-142">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="6a2fc-143">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="6a2fc-143">Example scenario</span></span>

<span data-ttu-id="6a2fc-144">Dette scenariet viser hvordan du kan endre strømmen av behandling for et eksisterende arbeidselement ved å endre arbeidsgruppen.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-144">This scenario shows how to change the stream of processing for an existing work item by changing its work pool.</span></span> <span data-ttu-id="6a2fc-145">Den bruker demonstrasjonsdata fra **USMF**-firmaet og innstillingene som ble foreslått tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-145">It uses demo data from the **USMF** company and the settings that were suggested earlier in this topic.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="6a2fc-146">Opprette en salgsordre og frigi den til lageret</span><span class="sxs-lookup"><span data-stu-id="6a2fc-146">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="6a2fc-147">Kontroller at det er nok lagerbeholdning for varene *A0001* og *A0002* på lager *62*.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-147">Confirm that there is enough on-hand inventory for items *A0001* and *A0002* in warehouse *62*.</span></span> <span data-ttu-id="6a2fc-148">Gå til **Lagerstyring \> Forespørsler og rapporter \> Beholdningsliste**, og rediger filtrene slik de vises her:</span><span class="sxs-lookup"><span data-stu-id="6a2fc-148">Go to **Inventory management \> Inquiries and reports \> On-hand list**, and edit the filters as shown here:</span></span>

    - <span data-ttu-id="6a2fc-149">**Lager**-verdien begynner med *62*.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-149">The **Warehouse** value begins with *62*.</span></span>
    - <span data-ttu-id="6a2fc-150">**Varenummer**-verdien er enten *A001* eller *A002*.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-150">The **Item number** value is either *A001* or *A002*.</span></span>

    <span data-ttu-id="6a2fc-151">Demonstrasjonsdata bør ha 10 som antall per stykk.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-151">Demo data should have a quantity of 10 each.</span></span>

    <span data-ttu-id="6a2fc-152">Deretter må du opprette en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-152">Next, you must create a sales order.</span></span>

1. <span data-ttu-id="6a2fc-153">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="6a2fc-154">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-154">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6a2fc-155">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="6a2fc-155">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="6a2fc-156">**Kundekonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="6a2fc-156">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="6a2fc-157">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="6a2fc-157">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="6a2fc-158">Velg **OK** for å opprette salgsorden og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-158">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="6a2fc-159">Den nye salgsordren åpnes.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-159">The new sales order is opened.</span></span> <span data-ttu-id="6a2fc-160">Den bør inneholde en ny, tom linje i rutenettet på **Salgsordrelinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-160">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="6a2fc-161">På denne linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="6a2fc-161">On this line, set the following values:</span></span>

    - <span data-ttu-id="6a2fc-162">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="6a2fc-162">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="6a2fc-163">**Antall:** *2*</span><span class="sxs-lookup"><span data-stu-id="6a2fc-163">**Quantity:** *2*</span></span>

1. <span data-ttu-id="6a2fc-164">Velg **Reservasjon** på **Beholdning**-menyen over rutenettet.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-164">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="6a2fc-165">På **Reservasjon**-siden, i handlingspanelet, velger du **Reserver parti** for å reservere lageret.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-165">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="6a2fc-166">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-166">Close the page.</span></span>
1. <span data-ttu-id="6a2fc-167">Velg **Legg til linje** på **Salgsordrelinjer**-hurtigfanen for å legge til en ny linje i salgsordren.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-167">On the **Sales order lines** FastTab, select **Add line** to add another line to your sales order.</span></span> <span data-ttu-id="6a2fc-168">På denne linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="6a2fc-168">On this line, set the following values:</span></span>

    - <span data-ttu-id="6a2fc-169">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="6a2fc-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="6a2fc-170">**Antall:** *2*</span><span class="sxs-lookup"><span data-stu-id="6a2fc-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="6a2fc-171">Velg **Reservasjon** på **Beholdning**-menyen over rutenettet.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-171">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="6a2fc-172">På **Reservasjon**-siden, i handlingspanelet, velger du **Reserver parti** for å reservere lageret.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-172">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="6a2fc-173">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-173">Close the page.</span></span>
1. <span data-ttu-id="6a2fc-174">Velg **Frigi til lager** i kategorien **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-174">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="6a2fc-175">Du mottar informasjonsmeldinger som viser bølge-ID og forsendelses-ID som er opprettet fra frigivelsen.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-175">You receive informational messages that show the wave ID and shipment ID that were created from the release.</span></span> <span data-ttu-id="6a2fc-176">Noter bølge-IDen.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-176">Make a note of the wave ID.</span></span>

### <a name="review-the-outbound-wave"></a><span data-ttu-id="6a2fc-177">Se gjennom den utgående bølgen</span><span class="sxs-lookup"><span data-stu-id="6a2fc-177">Review the outbound wave</span></span>

1. <span data-ttu-id="6a2fc-178">Gå til **Lagerstyring \> Utgående bølger \> Forsendelsesbølger \> Alle bølger**.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-178">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="6a2fc-179">I rutenettet søker du etter bølge-IDen som ble opprettet fra frigivelsen av salgsordren.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-179">In the grid, search for the wave ID that was created from the release of the sales order.</span></span>
1. <span data-ttu-id="6a2fc-180">Velg bølge-ID for å vise detaljene.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-180">Select the wave ID to view the details.</span></span>
1. <span data-ttu-id="6a2fc-181">I hurtigfanen **Bølgelinjer** kontrollerer du at det vises en forsendelses-ID for salgsordren.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-181">On the **Wave lines** FastTab, make sure that a shipment ID is shown for the sales order.</span></span>

    > [!TIP]
    > <span data-ttu-id="6a2fc-182">Hvis alternativet **Behandle bølge ved frigivelse til lager** er satt til *Nei* i oppsettet for forsendelsesbølgemalen, må du behandle bølgen manuelt ved å velge **Prosess** fra **Bølge**-kategorien i handlingsruten for å opprette arbeid.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-182">If the **Process wave at release to warehouse** option is set to *No* in the setup for the shipping wave template, you must manually process the wave by selecting **Process** from the **Wave** tab on the Action Pane to create work.</span></span>

1. <span data-ttu-id="6a2fc-183">Kontroller at bølgen er behandlet.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-183">Make sure that the wave has been processed.</span></span> <span data-ttu-id="6a2fc-184">Denne behandlingen oppretter det nødvendige arbeidet.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-184">This processing creates the required work.</span></span>

### <a name="view-work-details-and-change-the-work-pool"></a><span data-ttu-id="6a2fc-185">Vise arbeidsdetaljer og endre arbeidsutvalget</span><span class="sxs-lookup"><span data-stu-id="6a2fc-185">View work details and change the work pool</span></span>

<span data-ttu-id="6a2fc-186">Du kan bruke **Arbeidsdetaljer**-siden til å vise arbeidet som ble opprettet, og til å administrere arbeidsutvalget.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-186">You can use the **Work details** page to view the work that was created and to manage the work pool.</span></span>

1. <span data-ttu-id="6a2fc-187">Gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-187">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="6a2fc-188">Velg raden for arbeidet som nettopp ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-188">Select the row for the work that was just created.</span></span> <span data-ttu-id="6a2fc-189">**Ordrenummer**-kolonnen vil vise salgsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-189">The **Order number** column will show the sales order number.</span></span>

    <span data-ttu-id="6a2fc-190">Feltet **ID for arbeidsutvalg** blir satt til IDen for arbeidsutvalget som ble definert i arbeidsmalen.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-190">The **Work pool ID** field will be set to the work pool ID that was set up in the work template.</span></span>

    > [!TIP]
    > <span data-ttu-id="6a2fc-191">Hvis du ikke ser feltet **ID for arbeidsutvalg**, legger du til kolonnen i rutenettet og oppdaterer deretter siden.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-191">If you don't see the **Work pool ID** field, add the column to the grid, and then refresh the page.</span></span>

1. <span data-ttu-id="6a2fc-192">Hvis du vil endre arbeidsutvalget som er knyttet til arbeids-IDen, går du til handlingsruten i kategorien **Arbeid** og velger **Endre ID for arbeidsutvalg**.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-192">To change the work pool that is associated with the work ID, on the Action Pane, on the **Work** tab, select **Change Work pool ID**.</span></span>
1. <span data-ttu-id="6a2fc-193">I dialogboksen **Endre arbeidsutvalg**, i hurtigkategorien **Parametere** i feltet **ID for arbeidsutvalg**, velger du *CallCenter*.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-193">In the **Change work pool** dialog box, on the **Parameters** FastTab, in the **Work pool ID** field, select *CallCenter*.</span></span>
1. <span data-ttu-id="6a2fc-194">Velg **OK** for å bruke endringen.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-194">Select **OK** to apply your change.</span></span>
1. <span data-ttu-id="6a2fc-195">Merk at verdien for feltet **ID for arbeidsutvalg** nå er endret til *CallCenter*.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-195">Notice that the value of the **Work pool ID** field has now been changed to *CallCenter*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a2fc-196">Når dialogboksen **Endre arbeidsutvalg** vises, kan det hende at feltet **ID for arbeidsutvalg** er tomt som standard.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-196">When the **Change work pool** dialog box appears, the **Work pool ID** field might be blank by default.</span></span> <span data-ttu-id="6a2fc-197">Hvis feltet er tomt når du velger **OK** for å bruke endringer, fjerner du arbeidsutvalget helt fra arbeidet.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-197">If the field is blank when you select **OK** to apply changes, you will remove the work pool completely from the work.</span></span>
>
> <span data-ttu-id="6a2fc-198">I tillegg til å bytte arbeidsutvalg kan du bruke denne fremgangsmåten til å legge til et arbeidsutvalg i alle arbeidselementer som ikke har et, eller til å fjerne et arbeidsutvalg fra alle arbeidselementer som har et.</span><span class="sxs-lookup"><span data-stu-id="6a2fc-198">In addition to switching work pools, you can use this procedure to add a work pool to any work item that doesn't have one, or to remove a work pool from any work item that does have one.</span></span>