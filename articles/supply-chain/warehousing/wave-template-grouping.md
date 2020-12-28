---
title: Gruppering av bølgemal
description: Bølgemalgruppering gjør det mulig for systemet å bruke bølgemaloppsett til å fastslå, basert på kriterier du definerer, hvordan de skal dele frigitte linjer og tilordne dem til nye eller eksisterende bølger. Denne funksjonen kan være nyttig på lagre der bølger opprettes basert på bestemte kriterier, men der ledere foretrekker å opprette bølger automatisk i stedet for å bruke dem manuelt.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9cbc0b6655de740628bcf3709d250ac02238038b
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434818"
---
# <a name="wave-template-grouping"></a><span data-ttu-id="845c4-104">Gruppering av bølgemal</span><span class="sxs-lookup"><span data-stu-id="845c4-104">Wave template grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="845c4-105">Bølgemalgruppering gjør det mulig for systemet å bruke [bølgemaloppsett](tasks/configure-wave-processing.md) til å fastslå, basert på kriterier du definerer, hvordan de skal dele frigitte linjer og tilordne dem til nye eller eksisterende bølger.</span><span class="sxs-lookup"><span data-stu-id="845c4-105">Wave template grouping enables the system to use [wave template](tasks/configure-wave-processing.md) setups to determine, based on criteria that you define, how it should split released lines and assign them to new or existing waves.</span></span> <span data-ttu-id="845c4-106">Denne funksjonen kan være nyttig på lagre der bølger opprettes basert på bestemte kriterier, men der ledere foretrekker å opprette bølger automatisk i stedet for å bruke dem manuelt.</span><span class="sxs-lookup"><span data-stu-id="845c4-106">This feature can be useful in warehouses where waves are created based on specific criteria, but where managers prefer to create waves automatically instead of manually.</span></span> <span data-ttu-id="845c4-107">Det gjør det mulig for systemet å legge til alle nylig frigitte forsendelser i den første bølgen som blir funnet med samsvarende grupperingsfeltverdier.</span><span class="sxs-lookup"><span data-stu-id="845c4-107">It enables the system to add each newly released shipment to the first wave that it finds that has matching grouping field values.</span></span> <span data-ttu-id="845c4-108">Hvis det ikke blir funnet noen treff, oppretter systemet en ny bølge for den nye forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="845c4-108">If no match is found, the system creates a new wave for the new shipment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="845c4-109">Bølgemalgruppering støttes ikke for arbeidstypene *råvareplukking for produksjon* eller *Kanban-plukking*.</span><span class="sxs-lookup"><span data-stu-id="845c4-109">Wave template grouping isn't supported for the work types *production raw material picking* or *Kanban picking*.</span></span> <span data-ttu-id="845c4-110">Dette skyldes at bølgegruppering er basert på forsendelser, og at disse arbeidstypene ikke bruker forsendelser.</span><span class="sxs-lookup"><span data-stu-id="845c4-110">This is because wave grouping is based on shipments and these work types don't use shipments.</span></span>

## <a name="turn-on-the-wave-template-grouping-feature"></a><span data-ttu-id="845c4-111">Aktivere funksjonen Bølgemalgruppering</span><span class="sxs-lookup"><span data-stu-id="845c4-111">Turn on the Wave template grouping feature</span></span>

<span data-ttu-id="845c4-112">Før du kan bruke *Bølgemalgruppering*-funksjonen, må den aktiveres i systemet.</span><span class="sxs-lookup"><span data-stu-id="845c4-112">Before you can use the *Wave template grouping* feature, it must be turned on in your system.</span></span> <span data-ttu-id="845c4-113">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="845c4-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="845c4-114">I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="845c4-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="845c4-115">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="845c4-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="845c4-116">**Funksjonsnavn:** *Bølgemalgruppering*</span><span class="sxs-lookup"><span data-stu-id="845c4-116">**Feature name:** *Wave template grouping*</span></span>

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a><span data-ttu-id="845c4-117">Angi en bølgemal for å bruke bølgemalgruppering</span><span class="sxs-lookup"><span data-stu-id="845c4-117">Set a wave template to use wave template grouping</span></span>

<span data-ttu-id="845c4-118">Hvis du vil gjøre bølgemalgruppering tilgjengelig, følger du disse trinnene for å konfigurere [bølgemalen](tasks/configure-wave-processing.md).</span><span class="sxs-lookup"><span data-stu-id="845c4-118">To make wave template grouping available, follow these steps to set up your [wave template](tasks/configure-wave-processing.md).</span></span>

1. <span data-ttu-id="845c4-119">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.</span><span class="sxs-lookup"><span data-stu-id="845c4-119">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="845c4-120">Velg bølgemalen du vil sette opp, i venstre rute.</span><span class="sxs-lookup"><span data-stu-id="845c4-120">In the left pane, select the wave template to set up.</span></span> <span data-ttu-id="845c4-121">Hvis du forbereder deg til å arbeide gjennom scenariet senere i dette emnet ved hjelp av demodata, velger du **62 Standardforsendelse**-malen.</span><span class="sxs-lookup"><span data-stu-id="845c4-121">If you're preparing to work through the scenario later in this topic by using demo data, select the **62 Shipping default** template.</span></span>
1. <span data-ttu-id="845c4-122">Velg **Rediger** for å legge siden inn i redigeringsmodus.</span><span class="sxs-lookup"><span data-stu-id="845c4-122">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="845c4-123">Angi følgende verdier i **Generelt**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="845c4-123">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="845c4-124">**Automatiser bølgeoppretting:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="845c4-124">**Automate wave creation:** *Yes*</span></span>
    - <span data-ttu-id="845c4-125">**Tilordne til åpne bølger:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="845c4-125">**Assign to open waves:** *Yes*</span></span>
    - <span data-ttu-id="845c4-126">**Behandle bølge ved frigivelse til lager:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="845c4-126">**Process wave at release to warehouse:** *No*</span></span>

1. <span data-ttu-id="845c4-127">I handlingsruten velger du **Rediger spørring** for å åpne dialogboksen for spørring.</span><span class="sxs-lookup"><span data-stu-id="845c4-127">On the Action Pane, select **Edit query** to open the query dialog box.</span></span>
1. <span data-ttu-id="845c4-128">I dialogboksen for spørring, på **Sortering**-fanen, går du gjennom sorteringskriteriene, og kontroller at det finnes en regel som inkluderer feltet som du vil bruke til å gruppere bølger.</span><span class="sxs-lookup"><span data-stu-id="845c4-128">In the query dialog box, on the **Sorting** tab, review the sorting criteria, and make sure that there is a rule that includes the field that you want to use to group your waves.</span></span>

    <span data-ttu-id="845c4-129">Hvis du forbereder deg til å arbeide gjennom scenariet ved hjelp av demodata, legger du til en rad som har følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="845c4-129">If you're preparing to work through the scenario by using demo data, add a row that has the following values:</span></span>

    - <span data-ttu-id="845c4-130">**Tabell:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="845c4-130">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="845c4-131">**Avledet tabell:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="845c4-131">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="845c4-132">**Felt:** *Transportørtjeneste*</span><span class="sxs-lookup"><span data-stu-id="845c4-132">**Field:** *Carrier service*</span></span>

        > [!NOTE]
        > <span data-ttu-id="845c4-133">Når du har valgt denne verdien, kan du få følgende melding: Feltet Transportørtjeneste er ikke et indeksfelt.</span><span class="sxs-lookup"><span data-stu-id="845c4-133">After you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="845c4-134">Vil du legge til sortering på dette?</span><span class="sxs-lookup"><span data-stu-id="845c4-134">Do you want to add sorting on this?"</span></span> <span data-ttu-id="845c4-135">Velg **Ja** for å legge til sortering.</span><span class="sxs-lookup"><span data-stu-id="845c4-135">Select **Yes** to add sorting.</span></span>

    - <span data-ttu-id="845c4-136">**Søkeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="845c4-136">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="845c4-137">Velg **OK** for å lagre endringene og lukke dialogboksen for spørring.</span><span class="sxs-lookup"><span data-stu-id="845c4-137">Select **OK** to save your changes and close the query dialog box.</span></span>
1. <span data-ttu-id="845c4-138">Velg **Bølgemalgruppering** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="845c4-138">On the Action Pane, select **Wave template grouping**.</span></span>
1. <span data-ttu-id="845c4-139">På **Bølgemalgruppering**-siden velger du **Grupper etter**-avmerkingsboksen for hver rad du vil bruke til å gruppere ordrelinjer i bølger, etter behov.</span><span class="sxs-lookup"><span data-stu-id="845c4-139">On the **Wave template grouping** page, select the **Group by** check box for each row that you want to use to group your order lines into waves, as required.</span></span> <span data-ttu-id="845c4-140">Hvis du er klar til å arbeide gjennom scenariet ved hjelp av demondata, merker du av **Grupper etter**-avmerkingsboksen for *Transportørtjeneste*-raden.</span><span class="sxs-lookup"><span data-stu-id="845c4-140">If you're preparing to work through the scenario by using demo data, select the **Group by** check box for the *Carrier service* row.</span></span>
1. <span data-ttu-id="845c4-141">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="845c4-141">Select **Save**.</span></span>
1. <span data-ttu-id="845c4-142">Lukk **Bølgemalgruppering**-siden.</span><span class="sxs-lookup"><span data-stu-id="845c4-142">Close the **Wave template grouping** page.</span></span>
1. <span data-ttu-id="845c4-143">Velg **Lagre** for å lagre malen.</span><span class="sxs-lookup"><span data-stu-id="845c4-143">Select **Save** to save your template.</span></span>

## <a name="scenario"></a><span data-ttu-id="845c4-144">Scenario</span><span class="sxs-lookup"><span data-stu-id="845c4-144">Scenario</span></span>

<span data-ttu-id="845c4-145">Denne delen inneholder et skript som du kan arbeide gjennom for å lære hva denne funksjonen gjør, og hvordan du arbeider med den.</span><span class="sxs-lookup"><span data-stu-id="845c4-145">This section provides a script that you can work through to learn what this feature does and how to work with it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="845c4-146">Gjøre eksempeldata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="845c4-146">Make sample data available</span></span>

<span data-ttu-id="845c4-147">For å arbeide deg gjennom dette scenariet ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert.</span><span class="sxs-lookup"><span data-stu-id="845c4-147">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="845c4-148">Du må også velge den juridiske enheten **USMF** før du begynner.</span><span class="sxs-lookup"><span data-stu-id="845c4-148">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="845c4-149">Du kan også bruke dette scenariet som en veiledning for å bruke funksjonen når du arbeider i et produksjonssystem.</span><span class="sxs-lookup"><span data-stu-id="845c4-149">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="845c4-150">I så fall må du imidlertid erstatte dine egne verdier, og det kan hende du mangler noen typer obligatoriske oppføringer som standard demonstrasjonsdata gir.</span><span class="sxs-lookup"><span data-stu-id="845c4-150">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-wave-template-grouping"></a><span data-ttu-id="845c4-151">Scenario: Bølgemalgruppering</span><span class="sxs-lookup"><span data-stu-id="845c4-151">Scenario: Wave template grouping</span></span>

<span data-ttu-id="845c4-152">Dette scenariet viser hvordan du bruker bølgemalgruppering til å opprette flere bølger automatisk basert på grupperingskriterier som er definert i en bølgemal.</span><span class="sxs-lookup"><span data-stu-id="845c4-152">This scenario shows how to use wave template grouping to automatically create multiple waves, based on grouping criteria that are defined in a wave template.</span></span> <span data-ttu-id="845c4-153">I dette scenariet er bølgemalen satt opp i systemet for å opprette én bølge per transportørtjeneste.</span><span class="sxs-lookup"><span data-stu-id="845c4-153">In this scenario, the wave template is set up in the system to create one wave per carrier service.</span></span>

<span data-ttu-id="845c4-154">Før du begynner, klargjør du bølgemalen som beskrevet i delen [Angi en bølgemal for å bruke bølgemalgruppering](#set-up-template) tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="845c4-154">Before you begin, prepare your wave template as described in the [Set a wave template to use wave template grouping](#set-up-template) section earlier in this topic.</span></span> <span data-ttu-id="845c4-155">Hvis du skal arbeide med demonstrasjonsdata for dette scenariet, må du passe på å bruke demodataverdiene som foreslås i denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="845c4-155">If you will be working with demo data for this scenario, be sure to use the demo data values that are suggested in that procedure.</span></span> <span data-ttu-id="845c4-156">Dette oppsettet vil gruppere bølger i henhold til transportørtjenesten som er angitt for hver salgsordre.</span><span class="sxs-lookup"><span data-stu-id="845c4-156">This setup will group your waves according to the carrier service that is set for each sales order.</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="845c4-157">Opprett salgsordre 1</span><span class="sxs-lookup"><span data-stu-id="845c4-157">Create sales order 1</span></span>

1. <span data-ttu-id="845c4-158">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="845c4-158">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="845c4-159">Velg **Ny** for å opprette en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="845c4-159">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="845c4-160">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="845c4-160">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="845c4-161">På **Kunde**-hurtigfanen angir du **Kundekonto**-feltet til *US-004*.</span><span class="sxs-lookup"><span data-stu-id="845c4-161">On the **Customer** FastTab, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="845c4-162">På hurtigfanen **Generelt** angir du **Lager**-feltet til *62*.</span><span class="sxs-lookup"><span data-stu-id="845c4-162">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="845c4-163">Velg **OK** for å opprette salgsorden og lukke **Opprett salgsordre**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="845c4-163">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="845c4-164">Den nye salgsordren åpnes i **Linjer**-visningen.</span><span class="sxs-lookup"><span data-stu-id="845c4-164">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="845c4-165">Noter deg salgsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="845c4-165">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="845c4-166">Bytt til **Topptekst**-visningen.</span><span class="sxs-lookup"><span data-stu-id="845c4-166">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="845c4-167">På **Levering**-hurtigfanen, i **Transport**-inndelingen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="845c4-167">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="845c4-168">**Transportør:** *Luftlast*</span><span class="sxs-lookup"><span data-stu-id="845c4-168">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="845c4-169">**Transportørtjeneste:** *Lufttransport*</span><span class="sxs-lookup"><span data-stu-id="845c4-169">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="845c4-170">Gå tilbake til **Linjer**-visningen.</span><span class="sxs-lookup"><span data-stu-id="845c4-170">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="845c4-171">I **Salgsordrelinjer**-inndelingen velger du **Legg til linje** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="845c4-171">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="845c4-172">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="845c4-172">On the new line, set the following values:</span></span>

    - <span data-ttu-id="845c4-173">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="845c4-173">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="845c4-174">**Antall:** *2*</span><span class="sxs-lookup"><span data-stu-id="845c4-174">**Quantity:** *2*</span></span>

1. <span data-ttu-id="845c4-175">Velg den nye ordrelinjen og deretter på **Beholdning**-menyen over rutenett, velger du **Reservasjon**.</span><span class="sxs-lookup"><span data-stu-id="845c4-175">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="845c4-176">På **Reservasjon**-siden, i handlingsruten, velger du **Reserver parti** for å reservere den valgte linjens fulle antall i lageret.</span><span class="sxs-lookup"><span data-stu-id="845c4-176">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="845c4-177">Lukk **Reservasjon**-siden for å gå tilbake til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="845c4-177">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="845c4-178">Velg **Frigi til lager** i gruppen **Handlinger** i kategorien **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="845c4-178">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="845c4-179">Du mottar en informasjonsmelding som viser forsendelse og bølge for denne ordren.</span><span class="sxs-lookup"><span data-stu-id="845c4-179">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="845c4-180">Skriv ned ID-nummeret for bølgen og forsendelses-ID-numre.</span><span class="sxs-lookup"><span data-stu-id="845c4-180">Make a note of the wave ID number and the shipment ID numbers.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a><span data-ttu-id="845c4-181">Vis bølgen som ble opprettet fra salgsordre 1</span><span class="sxs-lookup"><span data-stu-id="845c4-181">View the wave that was created from sales order 1</span></span>

1. <span data-ttu-id="845c4-182">Gå til **Lagerstyring \> Utgående bølger \> Forsendelsesbølger \> Alle bølger**.</span><span class="sxs-lookup"><span data-stu-id="845c4-182">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="845c4-183">Velg bølge-ID-en som ble opprettet fra salgsordren.</span><span class="sxs-lookup"><span data-stu-id="845c4-183">Select the wave ID that was created from the sales order.</span></span>
1. <span data-ttu-id="845c4-184">Velg bølge-ID-koblingen for å åpne siden for bølgedetaljer.</span><span class="sxs-lookup"><span data-stu-id="845c4-184">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="845c4-185">Legg merke til at forsendelsen er lagt til i **Bølgelinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="845c4-185">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="845c4-186">Opprett salgsordre 2</span><span class="sxs-lookup"><span data-stu-id="845c4-186">Create sales order 2</span></span>

1. <span data-ttu-id="845c4-187">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="845c4-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="845c4-188">Velg **Ny** for å opprette en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="845c4-188">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="845c4-189">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="845c4-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="845c4-190">På **Kunde**-hurtigfanen angir du **Kundekonto**-feltet til *US-005*.</span><span class="sxs-lookup"><span data-stu-id="845c4-190">On the **Customer** FastTab, set the **Customer account** field to *US-005*.</span></span>
    - <span data-ttu-id="845c4-191">På hurtigfanen **Generelt** angir du **Lager**-feltet til *62*.</span><span class="sxs-lookup"><span data-stu-id="845c4-191">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="845c4-192">Velg **OK** for å opprette salgsorden og lukke **Opprett salgsordre**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="845c4-192">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="845c4-193">Den nye salgsordren åpnes i **Linjer**-visningen.</span><span class="sxs-lookup"><span data-stu-id="845c4-193">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="845c4-194">Noter deg salgsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="845c4-194">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="845c4-195">Bytt til **Topptekst**-visningen.</span><span class="sxs-lookup"><span data-stu-id="845c4-195">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="845c4-196">På **Levering**-hurtigfanen, i **Transport**-inndelingen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="845c4-196">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="845c4-197">**Transportør:** *Blomsterflytting*</span><span class="sxs-lookup"><span data-stu-id="845c4-197">**Shipping carrier:** *Flower moving*</span></span>
    - <span data-ttu-id="845c4-198">**Transportørtjeneste:** *Std*</span><span class="sxs-lookup"><span data-stu-id="845c4-198">**Carrier service:** *Std*</span></span>

1. <span data-ttu-id="845c4-199">Gå tilbake til **Linjer**-visningen.</span><span class="sxs-lookup"><span data-stu-id="845c4-199">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="845c4-200">I **Salgsordrelinjer**-inndelingen velger du **Legg til linje** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="845c4-200">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="845c4-201">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="845c4-201">On the new line, set the following values:</span></span>

    - <span data-ttu-id="845c4-202">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="845c4-202">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="845c4-203">**Antall:** *1*</span><span class="sxs-lookup"><span data-stu-id="845c4-203">**Quantity:** *1*</span></span>

1. <span data-ttu-id="845c4-204">Velg den nye ordrelinjen og deretter på **Beholdning**-menyen over rutenett, velger du **Reservasjon**.</span><span class="sxs-lookup"><span data-stu-id="845c4-204">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="845c4-205">På **Reservasjon**-siden, i handlingsruten, velger du **Reserver parti** for å reservere den valgte linjens fulle antall i lageret.</span><span class="sxs-lookup"><span data-stu-id="845c4-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="845c4-206">Lukk **Reservasjon**-siden for å gå tilbake til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="845c4-206">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="845c4-207">Velg **Frigi til lager** i gruppen **Handlinger** i kategorien **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="845c4-207">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="845c4-208">Du mottar en informasjonsmelding som viser forsendelse og bølge for denne ordren.</span><span class="sxs-lookup"><span data-stu-id="845c4-208">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="845c4-209">Skriv ned ID-nummeret for bølgen og forsendelses-ID-numre.</span><span class="sxs-lookup"><span data-stu-id="845c4-209">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="845c4-210">Legg merke til at bølge-ID-en er forskjellig fra bølge-ID-en i den første salgsordren.</span><span class="sxs-lookup"><span data-stu-id="845c4-210">Notice that the wave ID differs from the wave ID of the first sales order.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a><span data-ttu-id="845c4-211">Vis bølgen som ble opprettet fra salgsordre 2</span><span class="sxs-lookup"><span data-stu-id="845c4-211">View the wave that was created from sales order 2</span></span>

1. <span data-ttu-id="845c4-212">Gå til **Lagerstyring \> Utgående bølger \> Forsendelsesbølger \> Alle bølger**.</span><span class="sxs-lookup"><span data-stu-id="845c4-212">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="845c4-213">Velg bølge-ID-en som ble opprettet fra den andre salgsordren.</span><span class="sxs-lookup"><span data-stu-id="845c4-213">Select the wave ID that was created from the second sales order.</span></span>
1. <span data-ttu-id="845c4-214">Velg bølge-ID-koblingen for å åpne siden for bølgedetaljer.</span><span class="sxs-lookup"><span data-stu-id="845c4-214">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="845c4-215">Legg merke til at forsendelsen er lagt til i **Bølgelinjer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="845c4-215">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

<span data-ttu-id="845c4-216">En ny bølge ble opprettet for denne forsendelsen, fordi den bruker en annen transportørtjeneste enn den første salgsordren.</span><span class="sxs-lookup"><span data-stu-id="845c4-216">A new wave was created for this shipment, because it uses a different carrier service than the first sales order.</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="845c4-217">Opprett salgsordre 3</span><span class="sxs-lookup"><span data-stu-id="845c4-217">Create sales order 3</span></span>

1. <span data-ttu-id="845c4-218">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="845c4-218">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="845c4-219">Velg **Ny** for å opprette en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="845c4-219">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="845c4-220">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="845c4-220">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="845c4-221">På **Kunde**-hurtigfanen angir du **Kundekonto**-feltet til *US-006*.</span><span class="sxs-lookup"><span data-stu-id="845c4-221">On the **Customer** FastTab, set the **Customer account** field to *US-006*.</span></span>
    - <span data-ttu-id="845c4-222">På hurtigfanen **Generelt** angir du **Lager**-feltet til *62*.</span><span class="sxs-lookup"><span data-stu-id="845c4-222">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="845c4-223">Velg **OK** for å opprette salgsorden og lukke **Opprett salgsordre**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="845c4-223">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="845c4-224">Den nye salgsordren åpnes i **Linjer**-visningen.</span><span class="sxs-lookup"><span data-stu-id="845c4-224">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="845c4-225">Noter deg salgsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="845c4-225">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="845c4-226">Bytt til **Topptekst**-visningen.</span><span class="sxs-lookup"><span data-stu-id="845c4-226">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="845c4-227">På **Levering**-hurtigfanen, i **Transport**-inndelingen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="845c4-227">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="845c4-228">**Transportør:** *Luftlast*</span><span class="sxs-lookup"><span data-stu-id="845c4-228">**Shipping carrier:** *Air Cargo*</span></span>
    - <span data-ttu-id="845c4-229">**Transportørtjeneste:** *Lufttransport*</span><span class="sxs-lookup"><span data-stu-id="845c4-229">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="845c4-230">Gå tilbake til **Linjer**-visningen.</span><span class="sxs-lookup"><span data-stu-id="845c4-230">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="845c4-231">I **Salgsordrelinjer**-inndelingen velger du **Legg til linje** for å legge til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="845c4-231">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="845c4-232">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="845c4-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="845c4-233">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="845c4-233">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="845c4-234">**Antall:** *1*</span><span class="sxs-lookup"><span data-stu-id="845c4-234">**Quantity:** *1*</span></span>

1. <span data-ttu-id="845c4-235">Velg den nye ordrelinjen og deretter på **Beholdning**-menyen over rutenett, velger du **Reservasjon**.</span><span class="sxs-lookup"><span data-stu-id="845c4-235">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="845c4-236">På **Reservasjon**-siden, i handlingsruten, velger du **Reserver parti** for å reservere den valgte linjens fulle antall i lageret.</span><span class="sxs-lookup"><span data-stu-id="845c4-236">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="845c4-237">Lukk **Reservasjon**-siden for å gå tilbake til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="845c4-237">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="845c4-238">Velg **Frigi til lager** i gruppen **Handlinger** i kategorien **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="845c4-238">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="845c4-239">Du mottar en informasjonsmelding som viser forsendelse og bølge for denne ordren.</span><span class="sxs-lookup"><span data-stu-id="845c4-239">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="845c4-240">Skriv ned ID-nummeret for bølgen og forsendelses-ID-numre.</span><span class="sxs-lookup"><span data-stu-id="845c4-240">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="845c4-241">Forsendelsen er tilordnet den eksisterende bølgen fra den første salgsordren.</span><span class="sxs-lookup"><span data-stu-id="845c4-241">The shipment has been assigned to the existing wave from the first sales order.</span></span>

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a><span data-ttu-id="845c4-242">Vis bølgen for salgsordrer 1 og 3</span><span class="sxs-lookup"><span data-stu-id="845c4-242">View the wave for sales orders 1 and 3</span></span>

1. <span data-ttu-id="845c4-243">Gå til **Lagerstyring \> Utgående bølger \> Forsendelsesbølger \> Alle bølger**.</span><span class="sxs-lookup"><span data-stu-id="845c4-243">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="845c4-244">Velg bølge-ID-en som ble opprettet fra den tredje salgsordren.</span><span class="sxs-lookup"><span data-stu-id="845c4-244">Select the wave ID that was created from the third sales order.</span></span>
1. <span data-ttu-id="845c4-245">Velg bølge-ID-koblingen for å åpne siden for bølgedetaljer.</span><span class="sxs-lookup"><span data-stu-id="845c4-245">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="845c4-246">Legg merke til at forsendelsen er lagt til på **Bølgelinjer**-hurtigfanen sammen med forsendelsen for den første salgsordren.</span><span class="sxs-lookup"><span data-stu-id="845c4-246">Notice that the shipment has been added to the **Wave lines** FastTab, together with the shipment for the first sales order.</span></span>
