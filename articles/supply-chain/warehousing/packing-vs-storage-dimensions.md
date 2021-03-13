---
title: Angi ulike dimensjoner for pakking og lagring
description: Dette emnet viser hvordan du angir hvilken prosess (pakking, lagring eller nestet pakking) hver angitte dimensjon skal brukes til.
author: mirzaab
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 004d9b4522335b481b640ef0fe35f4db66e3c9f5
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078294"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a><span data-ttu-id="299fe-103">Angi ulike dimensjoner for pakking og lagring</span><span class="sxs-lookup"><span data-stu-id="299fe-103">Set different dimensions for packing and storage</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="299fe-104">Noen varer pakkes eller lagres på en slik måte at du kanskje må spore fysiske dimensjoner ulikt for hver av flere forskjellige prosesser.</span><span class="sxs-lookup"><span data-stu-id="299fe-104">Some items are packed or stored in such a way that you may need to track physical dimensions differently for each of several different processes.</span></span> <span data-ttu-id="299fe-105">Med funksjonen *Dimensjoner for pakking av produkt* kan du definere én eller flere dimensjonstyper for hvert produkt.</span><span class="sxs-lookup"><span data-stu-id="299fe-105">The *Packaging product dimensions* feature lets you set up one or several types of dimensions for each product.</span></span> <span data-ttu-id="299fe-106">Hver dimensjonstype gir et sett med fysiske mål (vekt, bredde, dybde og høyde) og fastsetter prosessen der de fysiske målingsverdiene gjelder.</span><span class="sxs-lookup"><span data-stu-id="299fe-106">Each dimension type provides a set of physical measurements (weight, width, depth, and height), and establishes the process where those physical measurement values apply.</span></span> <span data-ttu-id="299fe-107">Når denne funksjonen er aktivert, støtter systemet følgende dimensjonstyper:</span><span class="sxs-lookup"><span data-stu-id="299fe-107">When this feature is enabled, your system will support the following types of dimensions:</span></span>

- <span data-ttu-id="299fe-108">*Lagring* - Lagringsdimensjoner brukes sammen med lokasjonsvolummål til å fastsette hvor mange eksemplarer av hver vare som kan lagres på forskjellige lagerlokasjoner.</span><span class="sxs-lookup"><span data-stu-id="299fe-108">*Storage* - Storage dimensions are used along with location volumetrics to determine how many of each item can be stored in various warehouse locations.</span></span>
- <span data-ttu-id="299fe-109">*Pakking* – Pakkingsdimensjoner brukes under containerbruk og den manuelle pakkeprosessen til å fastsette hvor mange eksemplarer av hver vare som får plass i forskjellige containertyper.</span><span class="sxs-lookup"><span data-stu-id="299fe-109">*Packing* - Packing dimensions are used during containerization and the manual packing process to determine how many of each item will fit in various container types.</span></span>
- <span data-ttu-id="299fe-110">*Nestet pakking* – Dimensjoner for nestet pakking brukes når pakkeprosessen inneholder flere nivåer.</span><span class="sxs-lookup"><span data-stu-id="299fe-110">*Nested packing* - Nested packing dimensions are used when the packing process contains multiple levels.</span></span>

<span data-ttu-id="299fe-111">*Lagring* sdimensjoner støttes selv om funksjonen *Dimensjoner for pakking av produkt* ikke er aktivert.</span><span class="sxs-lookup"><span data-stu-id="299fe-111">*Storage* dimensions are supported even when the *Packaging product dimensions* feature isn't enabled.</span></span> <span data-ttu-id="299fe-112">Du konfigurerer disse ved å bruke siden **Fysiske dimensjoner** i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="299fe-112">You set these up using the **Physical dimension** page in Supply Chain Management.</span></span> <span data-ttu-id="299fe-113">Disse dimensjonene brukes av alle prosesser der dimensjoner for pakking og nestet pakking ikke er angitt.</span><span class="sxs-lookup"><span data-stu-id="299fe-113">These dimensions are used by all processes where the packing and nested packing dimensions aren't specified.</span></span>

<span data-ttu-id="299fe-114">Du konfigurerer dimensjoner for *pakking* og *nestet pakking* ved å bruke siden **Fysiske produktdimensjoner**, som legges til når du aktiverer funksjonen *Dimensjoner for pakking av produkt*.</span><span class="sxs-lookup"><span data-stu-id="299fe-114">*Packing* and *nested packing* dimensions are set up using the **Physical product dimensions** page, which is added when you enable the *Packaging product dimensions* feature.</span></span>
<span data-ttu-id="299fe-115">Dette emnet inneholder et scenario som illustrerer hvordan du bruker denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="299fe-115">This topic provides a scenario that illustrates how to use this feature.</span></span>

## <a name="turn-on-the-packaging-product-dimensions-feature"></a><span data-ttu-id="299fe-116">Aktivere funksjonen for dimensjoner for pakking av produkt</span><span class="sxs-lookup"><span data-stu-id="299fe-116">Turn on the packaging product dimensions feature</span></span>

<span data-ttu-id="299fe-117">Før du kan bruke denne funksjonen, må den være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="299fe-117">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="299fe-118">Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="299fe-118">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="299fe-119">Funksjonen vises på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="299fe-119">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="299fe-120">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="299fe-120">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="299fe-121">**Funksjonsnavn:** *Dimensjoner for pakking av produkt*</span><span class="sxs-lookup"><span data-stu-id="299fe-121">**Feature name:** *Packaging product dimensions*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="299fe-122">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="299fe-122">Example scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="299fe-123">Definer scenariet</span><span class="sxs-lookup"><span data-stu-id="299fe-123">Set up the scenario</span></span>

<span data-ttu-id="299fe-124">Før du kan kjøre eksempelscenarioet, må du klargjøre systemet som beskrevet i denne delen.</span><span class="sxs-lookup"><span data-stu-id="299fe-124">Before you can run the example scenario, you must prepare your system as described in this section.</span></span>

#### <a name="enable-demo-data"></a><span data-ttu-id="299fe-125">Aktivere demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="299fe-125">Enable demo data</span></span>

<span data-ttu-id="299fe-126">For å kunne arbeide deg gjennom dette scenariet ved å bruke de angitte demonstrasjonspostene og -verdiene som er angitt her, må du være på et system der standard [demonstrasjonsdata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert.</span><span class="sxs-lookup"><span data-stu-id="299fe-126">To work through this scenario using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="299fe-127">Du må også velge den juridiske enheten *USMF* før du begynner.</span><span class="sxs-lookup"><span data-stu-id="299fe-127">Additionally, you must select the *USMF* legal entity before you begin.</span></span>

#### <a name="add-a-new-physical-dimension-to-a-product"></a><span data-ttu-id="299fe-128">Legge en ny fysisk dimensjon til et produkt</span><span class="sxs-lookup"><span data-stu-id="299fe-128">Add a new physical dimension to a product</span></span>

<span data-ttu-id="299fe-129">Legg til en ny fysisk dimensjon for et produkt ved å gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="299fe-129">Add a new physical dimension for a product by doing the following:</span></span>

1. <span data-ttu-id="299fe-130">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="299fe-130">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="299fe-131">Velg produktet med **Varenummer** *A0001*.</span><span class="sxs-lookup"><span data-stu-id="299fe-131">Select the product with **Item number** *A0001*.</span></span>
1. <span data-ttu-id="299fe-132">I handlingsruten i åpner du fanen **Administrer lager**, og i gruppen **Lager** velger du **Fysiske produktdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="299fe-132">On the Action Pane, open the **Manage inventory** tab and, from the **Warehouse** group, select **Physical product dimensions**.</span></span>
1. <span data-ttu-id="299fe-133">Siden **Fysiske produktdimensjoner** åpnes.</span><span class="sxs-lookup"><span data-stu-id="299fe-133">The **Physical product dimensions** page opens.</span></span> <span data-ttu-id="299fe-134">Velg **Ny** i handlingsruten for å legge til en ny dimensjon i rutenettet med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="299fe-134">On the Action Pane, select **New** to add a new dimension to the grid with the following settings:</span></span>
    - <span data-ttu-id="299fe-135">**Fysisk dimensjonstype** – *Pakking*</span><span class="sxs-lookup"><span data-stu-id="299fe-135">**Physical dimension type** - *Packing*</span></span>
    - <span data-ttu-id="299fe-136">**Fysisk enhet** – *stk.*</span><span class="sxs-lookup"><span data-stu-id="299fe-136">**Physical unit** - *pcs*</span></span>
    - <span data-ttu-id="299fe-137">**Vekt** – *4*</span><span class="sxs-lookup"><span data-stu-id="299fe-137">**Weight** - *4*</span></span>
    - <span data-ttu-id="299fe-138">**Vektenhet** – *kg*</span><span class="sxs-lookup"><span data-stu-id="299fe-138">**Weight unit** - *kg*</span></span>
    - <span data-ttu-id="299fe-139">**Dybde** – *3*</span><span class="sxs-lookup"><span data-stu-id="299fe-139">**Depth** - *3*</span></span>
    - <span data-ttu-id="299fe-140">**Høyde** – *4*</span><span class="sxs-lookup"><span data-stu-id="299fe-140">**Height** - *4*</span></span>
    - <span data-ttu-id="299fe-141">**Bredde** – *3*</span><span class="sxs-lookup"><span data-stu-id="299fe-141">**Width** - *3*</span></span>
    - <span data-ttu-id="299fe-142">**Lengde** – *cm*</span><span class="sxs-lookup"><span data-stu-id="299fe-142">**Length** - *cm*</span></span>
    - <span data-ttu-id="299fe-143">**Volumenhet** – *cm3*</span><span class="sxs-lookup"><span data-stu-id="299fe-143">**Volume unit** - *cm3*</span></span>

<span data-ttu-id="299fe-144">**Volum**-feltet beregnes automatisk basert på innstillingene for **Dybde**, **Høyde** og **Bredde**.</span><span class="sxs-lookup"><span data-stu-id="299fe-144">The **Volume** field is automatically calculated based on your **Depth**, **Height**, and **Width** settings.</span></span>

#### <a name="create-a-new-container-type"></a><span data-ttu-id="299fe-145">Opprett en ny containertype</span><span class="sxs-lookup"><span data-stu-id="299fe-145">Create a new container type</span></span>

<span data-ttu-id="299fe-146">Gå til **Lagerstyring \> Oppsett \> Containere \> Containertyper**, og opprett en ny post med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="299fe-146">Go to **Warehouse management \> Setup \> Containers \> Container types** and create a new record with the following settings:</span></span>

- <span data-ttu-id="299fe-147">**Containertypekode** – *Kort eske*</span><span class="sxs-lookup"><span data-stu-id="299fe-147">**Container type code** - *Short Box*</span></span>
- <span data-ttu-id="299fe-148">**Beskrivelse** – *Kort eske*</span><span class="sxs-lookup"><span data-stu-id="299fe-148">**Description** - *Short Box*</span></span>
- <span data-ttu-id="299fe-149">**Maksimal nettovekt** – *50*</span><span class="sxs-lookup"><span data-stu-id="299fe-149">**Maximum net weight** - *50*</span></span>
- <span data-ttu-id="299fe-150">**Volum** – *144*</span><span class="sxs-lookup"><span data-stu-id="299fe-150">**Volume** - *144*</span></span>
- <span data-ttu-id="299fe-151">**Lengde** – *6*</span><span class="sxs-lookup"><span data-stu-id="299fe-151">**Length** - *6*</span></span>
- <span data-ttu-id="299fe-152">**Bredde** – *6*</span><span class="sxs-lookup"><span data-stu-id="299fe-152">**Width** - *6*</span></span>
- <span data-ttu-id="299fe-153">**Høyde** – *4*</span><span class="sxs-lookup"><span data-stu-id="299fe-153">**Height** - *4*</span></span>

#### <a name="create-a-container-group"></a><span data-ttu-id="299fe-154">Opprette en containergruppe</span><span class="sxs-lookup"><span data-stu-id="299fe-154">Create a container group</span></span>

<span data-ttu-id="299fe-155">Gå til **Lagerstyring \> Oppsett \> Containere \> Containergrupper**, og opprett en ny post med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="299fe-155">Go to **Warehouse management \> Setup \> Containers \> Container groups** and create a new record with the following settings:</span></span>

- <span data-ttu-id="299fe-156">**Containergruppe-ID** – *Kort eske*</span><span class="sxs-lookup"><span data-stu-id="299fe-156">**Container group ID** - *Short Box*</span></span>
- <span data-ttu-id="299fe-157">**Beskrivelse** – *Kort eske*</span><span class="sxs-lookup"><span data-stu-id="299fe-157">**Description** - *Short Box*</span></span>

<span data-ttu-id="299fe-158">Legg til en ny linje i **Detaljer**-delen.</span><span class="sxs-lookup"><span data-stu-id="299fe-158">Add a new line to the **Details** section.</span></span> <span data-ttu-id="299fe-159">Sett **Containertype** til *Kort eske*.</span><span class="sxs-lookup"><span data-stu-id="299fe-159">Set the **Container type** to *Short Box*.</span></span>

#### <a name="set-up-a-container-build-template"></a><span data-ttu-id="299fe-160">Definere en mal for containerversjon</span><span class="sxs-lookup"><span data-stu-id="299fe-160">Set up a container build template</span></span>

<span data-ttu-id="299fe-161">Gå til **Lagerstyring \> Oppsett \> Containere \> Maler for containerversjoner** og velg **Esker**.</span><span class="sxs-lookup"><span data-stu-id="299fe-161">Go to **Warehouse management \> Setup \> Containers \> Container build templates** and select **Boxes**.</span></span> <span data-ttu-id="299fe-162">Endre **Containergruppe-ID** til *Kort eske*.</span><span class="sxs-lookup"><span data-stu-id="299fe-162">Change the **Container group ID** to *Short Box*.</span></span>

### <a name="run-the-scenario"></a><span data-ttu-id="299fe-163">Kjøre scenarioet</span><span class="sxs-lookup"><span data-stu-id="299fe-163">Run the scenario</span></span>

<span data-ttu-id="299fe-164">Når du har klargjort systemet som beskrevet i den forrige delen, er du klar til å kjøre scenarioet som beskrevet i neste del.</span><span class="sxs-lookup"><span data-stu-id="299fe-164">After you have prepared your system as described in the previous section, you are ready to run the scenario as described in the next section.</span></span>

#### <a name="create-a-sales-order-and-create-a-shipment"></a><span data-ttu-id="299fe-165">Opprette en salgsordre og en forsendelse</span><span class="sxs-lookup"><span data-stu-id="299fe-165">Create a sales order and create a shipment</span></span>

<span data-ttu-id="299fe-166">I denne prosessen skal du opprette en forsendelse basert på dimensjoner for vare *pakking* der høyden er mindre enn 3.</span><span class="sxs-lookup"><span data-stu-id="299fe-166">In this process you will create a shipment based on the item *packing* dimensions, for which the height is less than 3.</span></span>

1. <span data-ttu-id="299fe-167">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="299fe-167">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="299fe-168">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="299fe-168">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="299fe-169">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="299fe-169">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="299fe-170">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="299fe-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="299fe-171">**Lager:** *63*</span><span class="sxs-lookup"><span data-stu-id="299fe-171">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="299fe-172">Velg **OK** for å opprette salgsorden og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="299fe-172">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="299fe-173">Den nye salgsordren åpnes.</span><span class="sxs-lookup"><span data-stu-id="299fe-173">The new sales order is opened.</span></span> <span data-ttu-id="299fe-174">Den bør inneholde en ny, tom linje i rutenettet på **Salgsordrelinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="299fe-174">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="299fe-175">På denne linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="299fe-175">On this line, set the following values:</span></span>

    - <span data-ttu-id="299fe-176">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="299fe-176">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="299fe-177">**Antall:** *5*</span><span class="sxs-lookup"><span data-stu-id="299fe-177">**Quantity:** *5*</span></span>

1. <span data-ttu-id="299fe-178">På hurtigfanen **Salgsordrelinjer** velger du **Beholdning \> Reservasjon**.</span><span class="sxs-lookup"><span data-stu-id="299fe-178">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="299fe-179">På **Reservasjon**-siden, i handlingspanelet, velger du **Reserver parti** for å reservere lageret.</span><span class="sxs-lookup"><span data-stu-id="299fe-179">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="299fe-180">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="299fe-180">Close the page.</span></span>
1. <span data-ttu-id="299fe-181">I handlingsruten åpner du **Lager**-fanen og velger **Frigi til lager** for å opprette arbeidet for lageret.</span><span class="sxs-lookup"><span data-stu-id="299fe-181">On the Action Pane, open the **Warehouse** tab and select **Release to warehouse** to create work for the warehouse.</span></span>
1. <span data-ttu-id="299fe-182">I hurtigfanen **Salgsordrelinje** velger du **Lager \> Forsendelsesdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="299fe-182">On the **Sales order lines** FastTab, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="299fe-183">I handlingsruten åpner du **Transport**-fanen og velger **Vis containere**.</span><span class="sxs-lookup"><span data-stu-id="299fe-183">On the Action Pane, open the **Transportation** tab and select **View containers**.</span></span> <span data-ttu-id="299fe-184">Bekreft at varen ble containerbrukt i de to *Kort eske*-containerne.</span><span class="sxs-lookup"><span data-stu-id="299fe-184">Confirm that the item was containerized into the two *Short Box* containers.</span></span>

#### <a name="place-an-item-into-storage"></a><span data-ttu-id="299fe-185">Plassere en vare på lager</span><span class="sxs-lookup"><span data-stu-id="299fe-185">Place an item into storage</span></span>

1. <span data-ttu-id="299fe-186">Åpne mobilenheten, logg deg på lager 63, og gå til **Lager \> Juster inn**.</span><span class="sxs-lookup"><span data-stu-id="299fe-186">Open the mobile device, sign in to warehouse 63 and go to **Inventory \> Adjust In**.</span></span>
1. <span data-ttu-id="299fe-187">Angi **Lok.** = *SHORT-01*.</span><span class="sxs-lookup"><span data-stu-id="299fe-187">Enter **Loc** = *SHORT-01*.</span></span> <span data-ttu-id="299fe-188">Lag et nytt nummerskilt med **Vare** = *A0001* og **Antall** = *1 stk.*</span><span class="sxs-lookup"><span data-stu-id="299fe-188">Make a new license plate with **Item** = *A0001* and **Quantity** = *1 pcs*.</span></span>
1. <span data-ttu-id="299fe-189">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="299fe-189">Select **OK**.</span></span> <span data-ttu-id="299fe-190">Du får en feilmelding om at lokasjonen SHORT-01 mislyktes fordi vare A0001 ikke passer i lokasjonens angitte dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="299fe-190">You will receive the error "Location SHORT-01 failed because item A0001 does not fit in location's specified dimensions."</span></span> <span data-ttu-id="299fe-191">Dette skjer fordi dimensjoner av typen *Lagring* for produktet er større enn dimensjonene som er angitt i lokasjonsprofilen.</span><span class="sxs-lookup"><span data-stu-id="299fe-191">This is because the *Storage* type dimensions of the product are larger than the dimensions specified on the location profile.</span></span>
