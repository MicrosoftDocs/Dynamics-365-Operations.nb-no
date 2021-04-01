---
title: Detaljer for arbeidslinje
description: Dette emnet inneholder informasjon om Arbeidslinjedetaljer-siden, som viser en omfattende liste som kan sorteres og filtreres, over de enkelte arbeidslinjene i systemet.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0cb182242a42443d5894b864523fc5f5fea9c5b1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245112"
---
# <a name="work-line-details"></a><span data-ttu-id="bf8fb-103">Detaljer for arbeidslinje</span><span class="sxs-lookup"><span data-stu-id="bf8fb-103">Work line details</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf8fb-104">**Arbeidslinjedetaljer**-siden viser en omfattende liste som kan sorteres og filtreres, over de enkelte arbeidslinjene i systemet.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-104">The **Work line details** page shows a comprehensive, sortable, and filterable list of the individual work lines in your system.</span></span> <span data-ttu-id="bf8fb-105">Den gir en fullstendig oversikt over arbeid som blir planlagt og utført i lageret.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-105">It provides a complete overview of work that is being planned and executed in the warehouse.</span></span> <span data-ttu-id="bf8fb-106">Du kan enkelt bytte mellom å vise alle arbeidslinjer og vise bare åpne arbeidslinjer.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-106">You can easily switch between viewing all work lines and viewing only open work lines.</span></span> <span data-ttu-id="bf8fb-107">Detaljer som gis for hver linje, er arbeidsstatus, varenummer, lokasjon, arbeidsantall, last-ID og forsendelses-ID.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-107">Details that are provided for each line include the work status, item number, location, work quantity, load ID, and shipment ID.</span></span>

## <a name="turn-on-the-work-line-details-feature"></a><span data-ttu-id="bf8fb-108">Aktivere funksjonen detaljer for arbeidslinje</span><span class="sxs-lookup"><span data-stu-id="bf8fb-108">Turn on the work line details feature</span></span>

<span data-ttu-id="bf8fb-109">Før du kan bruke denne funksjonen, må den være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="bf8fb-110">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-110">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="bf8fb-111">I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="bf8fb-111">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="bf8fb-112">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="bf8fb-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="bf8fb-113">**Funksjonsnavn:** *Arbeidslinjedetaljer*</span><span class="sxs-lookup"><span data-stu-id="bf8fb-113">**Feature name:** *Work line details*</span></span>

## <a name="open-and-use-the-work-line-details-page"></a><span data-ttu-id="bf8fb-114">Åpne og bruke Arbeidslinjedetaljer-siden</span><span class="sxs-lookup"><span data-stu-id="bf8fb-114">Open and use the Work line details page</span></span>

<span data-ttu-id="bf8fb-115">Hvis du vil vise en liste over arbeidslinjedetaljer, kan du gå til **Lagerstyring \> Arbeid \> Arbeidslinjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-115">To view the list of work line details, go to **Warehouse management \> Work \> Work line details**.</span></span> <span data-ttu-id="bf8fb-116">Herfra kan du utføre følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="bf8fb-116">From here, you can perform the following actions:</span></span>

- <span data-ttu-id="bf8fb-117">Bruk **Filter**-feltet til å søke etter linjer som har en bestemt verdi for alle tilgjengelige parametere.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-117">Use the **Filter** field to search for lines that have a specific value for any available parameter.</span></span> <span data-ttu-id="bf8fb-118">(Tilgjengelige parametere inkluderer mange parametere som ikke vises som kolonner i rutenettet.)</span><span class="sxs-lookup"><span data-stu-id="bf8fb-118">(Available parameters include many parameters that aren't shown as columns in the grid.)</span></span>
- <span data-ttu-id="bf8fb-119">Bruk **Vis lukkede**-avmerkingsboksen til å vise eller skjule lukkede linjer.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-119">Use the **Show closed** check box to show or hide closed lines.</span></span>
- <span data-ttu-id="bf8fb-120">Velg **Vis dimensjoner** for å åpne **Dimensjonsvisning**-dialogboksen, der du kan velge å vise eller skjule forskjellige dimensjonskolonner i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-120">Select **Display dimensions** to open the **Dimensions display** dialog box, where you can choose to show or hide various dimension columns in the grid.</span></span>
- <span data-ttu-id="bf8fb-121">Velg en kolonneoverskrift for å åpne en meny der du kan velge å sortere eller filtrere listen etter verdier i den kolonnen.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-121">Select any column heading to open a menu where you can choose to sort or filter the list by values in that column.</span></span>
- <span data-ttu-id="bf8fb-122">Velg en arbeidslinje, og velg deretter **Endre lokasjon** for å åpne en dialogboks der du kan endre lokasjonen for arbeidslinjen.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-122">Select a work line, and then select **Change location** to open a dialog box where you can change the location for that work line.</span></span> <span data-ttu-id="bf8fb-123">Lokasjonen du angir, overstyrer oppsettet til lokasjonsdirektivet.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-123">The location that you specify will override the setup of the location directive.</span></span>
- <span data-ttu-id="bf8fb-124">Velg en arbeidslinje, og velg deretter **Avbryt arbeidslinje** for å åpne en dialogboks der du kan redusere antallet av den arbeidslinjen delvis eller helt.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-124">Select a work line, and then select **Cancel work line** to open a dialog box where you can partially or fully reduce the quantity of that work line.</span></span>
- <span data-ttu-id="bf8fb-125">Juster antall.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-125">Adjust quantities.</span></span>
- <span data-ttu-id="bf8fb-126">Vis transaksjonene bak en arbeidslinje.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-126">View the transactions behind any work line.</span></span>

## <a name="try-out-the-feature"></a><span data-ttu-id="bf8fb-127">Prøv ut funksjonen</span><span class="sxs-lookup"><span data-stu-id="bf8fb-127">Try out the feature</span></span>

<span data-ttu-id="bf8fb-128">Denne delen inneholder en tredjepartsdemo som viser hvordan du arbeider med arbeidslinjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-128">This section provides a three-part demo that shows how to work with work line details.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="bf8fb-129">Gjøre eksempeldata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="bf8fb-129">Make sample data available</span></span>

<span data-ttu-id="bf8fb-130">For å arbeide deg gjennom denne demonstrasjonen ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-130">To work through this demo by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="bf8fb-131">Du må også velge den juridiske enheten **USMF** før du begynner.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-131">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="bf8fb-132">Du kan også bruke denne demonstrasjonen som en veiledning når du arbeider i et produksjonssystem.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-132">You can also use this demo as guidance when you work on a production system.</span></span> <span data-ttu-id="bf8fb-133">Du må imidlertid erstatte dine egne verdier, og det kan hende du mangler noen typer obligatoriske oppføringer som standard demonstrasjonsdata gir.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-133">However, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a><span data-ttu-id="bf8fb-134">Kontroller at scenariooppsettet omfatter nok tilgjengelig beholdning</span><span class="sxs-lookup"><span data-stu-id="bf8fb-134">Verify that the scenario setup includes enough available inventory</span></span>

<span data-ttu-id="bf8fb-135">Hvis du arbeider med **USMF**-demonstrasjonsdata, må du først kontrollere at systemet er konfigurert slik at det finnes nok beholdning på hver relevante plukklokasjon.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-135">If you're working with the **USMF** demo data, you should first make sure that your system is set up so that enough inventory is available at each relevant pick location.</span></span> <span data-ttu-id="bf8fb-136">For denne demonstrasjonen er forventes det at du har følgende tilgjengelige beholdning:</span><span class="sxs-lookup"><span data-stu-id="bf8fb-136">For this demo, the expectation is that you have the following inventory available:</span></span>

- <span data-ttu-id="bf8fb-137">**Vare M9200:** 45 ea.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-137">**Item M9200:** 45 ea.</span></span> <span data-ttu-id="bf8fb-138">(eller mer)</span><span class="sxs-lookup"><span data-stu-id="bf8fb-138">(or more)</span></span>
- <span data-ttu-id="bf8fb-139">**Vare M9202:** 10 ea.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-139">**Item M9202:** 10 ea.</span></span> <span data-ttu-id="bf8fb-140">(eller mer)</span><span class="sxs-lookup"><span data-stu-id="bf8fb-140">(or more)</span></span>

<span data-ttu-id="bf8fb-141">Følg denne fremgangsmåten for å kontrollere at det er nok beholdning tilgjengelig, og for å gjøre eventuelle nødvendige justeringer.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-141">Follow these steps to verify that enough inventory is available and to make any adjustments that are required.</span></span>

1. <span data-ttu-id="bf8fb-142">Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**, og finn ut hvilke plukklokasjoner som skal brukes ved plukking av salgsordrer på lager 51.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-142">Go to **Warehouse management \> Setup \> Location directives**, and determine which picking locations are used for sales order picking at warehouse 51.</span></span> <span data-ttu-id="bf8fb-143">(Hvis du vil ha mer informasjon, kan du se [Kontrollere lagerarbeid ved hjelp av arbeidsmaler og lokasjonsdirektiver](control-warehouse-location-directives.md).)</span><span class="sxs-lookup"><span data-stu-id="bf8fb-143">(For more information, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md).)</span></span>
1. <span data-ttu-id="bf8fb-144">Kontroller beholdningsnivåene ved relevante lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-144">Check the inventory levels at the relevant locations.</span></span>
1. <span data-ttu-id="bf8fb-145">Juster beholdningen etter behov.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-145">Adjust inventory as required.</span></span> <span data-ttu-id="bf8fb-146">Du kan opprette manuelle flyttinger, bruke etterfylling eller bruke en annen flyt til å justere beholdningen.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-146">You can create manual movements, use replenishment, or apply any other flow to adjust the inventory.</span></span>

### <a name="part-1-create-picking-work"></a><span data-ttu-id="bf8fb-147">Del 1: Opprett plukkarbeid</span><span class="sxs-lookup"><span data-stu-id="bf8fb-147">Part 1: Create picking work</span></span>

<span data-ttu-id="bf8fb-148">Før du begynner å opprette arbeid, må du kontrollere at lageret er konfigurert til å svare på arbeidsforespørsler på forventet måte.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-148">Before you start to create work, make sure that your warehouse is set up to respond to work requests in the expected manner.</span></span>

<span data-ttu-id="bf8fb-149">Følg denne fremgangsmåten for å opprette plukkearbeid.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-149">Follow these steps to create some picking work.</span></span>

1. <span data-ttu-id="bf8fb-150">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-150">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="bf8fb-151">Velg **Ny** for å åpne **Opprett salgsordre**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-151">Select **New** to open the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="bf8fb-152">I **Opprett salgsordre**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="bf8fb-152">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="bf8fb-153">På **Kunde**-hurtigfanen angir du **Kundekonto**-feltet til _US-001_.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-153">On the **Customer** FastTab, set the **Customer account** field to _US-001_.</span></span>
    - <span data-ttu-id="bf8fb-154">På hurtigfanen **Generelt** angir du **Lager**-feltet til _51_.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-154">On the **General** FastTab, set the **Warehouse** field to _51_.</span></span>

1. <span data-ttu-id="bf8fb-155">Velg **OK** for å opprette salgsorden og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-155">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="bf8fb-156">Den nye salgsordren åpnes.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-156">Your new sales order is opened.</span></span> <span data-ttu-id="bf8fb-157">Den inneholder en ny, tom rad i **Salgsordrelinjer**-rutenettet.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-157">It includes a new, empty row in the **Sales order lines** grid.</span></span> <span data-ttu-id="bf8fb-158">Angi følgende verdier for denne ordrelinjen:</span><span class="sxs-lookup"><span data-stu-id="bf8fb-158">On this order line, set the following values:</span></span>

    - <span data-ttu-id="bf8fb-159">**Varenummer:** _M9200_</span><span class="sxs-lookup"><span data-stu-id="bf8fb-159">**Item number:** _M9200_</span></span>
    - <span data-ttu-id="bf8fb-160">**Antall:** _20_</span><span class="sxs-lookup"><span data-stu-id="bf8fb-160">**Quantity:** _20_</span></span>
    - <span data-ttu-id="bf8fb-161">**Enhet:** _ea_</span><span class="sxs-lookup"><span data-stu-id="bf8fb-161">**Unit:** _ea_</span></span>

1. <span data-ttu-id="bf8fb-162">Velg den nye ordrelinjen og deretter på **Beholdning**-menyen velger du **Reservasjon** for å åpne **Reservasjon**-siden.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-162">Select the new order line, and then, on the **Inventory** menu, select **Reservation** to open the **Reservation** page.</span></span>
1. <span data-ttu-id="bf8fb-163">På **Reservasjon**-siden velger du **Reserver parti** for å reservere den valgte linjens fulle antall i lageret.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-163">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="bf8fb-164">Lukk **Reservasjon**-siden for å gå tilbake til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-164">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="bf8fb-165">Velg **Frigi til lager** i fanen **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-165">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span> <span data-ttu-id="bf8fb-166">Systemet oppretter en forsendelse, legger den til en ny last, og oppretter det nødvendige arbeidet.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-166">The system creates a shipment, adds it to a new load, and creates the required work.</span></span>
1. <span data-ttu-id="bf8fb-167">Opprett en ny salgsordre for samme kundekonto og lager som du brukte for den første ordren.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-167">Create a second sales order for the same customer account and warehouse that you used for the first order.</span></span> <span data-ttu-id="bf8fb-168">Legg til følgende to ordrelinjer i denne ordren:</span><span class="sxs-lookup"><span data-stu-id="bf8fb-168">Add the following two order lines to this order:</span></span>

    - <span data-ttu-id="bf8fb-169">**Linje 1:** Angi **Varenummer**-feltet til _M9200_, **Antall**-feltet til _25_ og **Enhet**-feltet til _ea_.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-169">**Line 1:** Set the **Item number** field to _M9200_, the **Quantity** field to _25_, and the **Unit** field to _ea_.</span></span>
    - <span data-ttu-id="bf8fb-170">**Linje 2:** Angi **Varenummer**-feltet til _M9202_, **Antall**-feltet til _10_ og **Enhet**-feltet til _ea_.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-170">**Line 2:** Set the **Item number** field to _M9202_, the **Quantity** field to _10_, and the **Unit** field to _ea_.</span></span>

1. <span data-ttu-id="bf8fb-171">Gjenta trinn 6 til og med 8 for å reservere beholdningen for hver ordrelinje (én om gangen), og gjenta deretter trinn 9 for å frigi ordren til lageret.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-171">Repeat steps 6 through 8 to reserve the inventory for each order line (one at a time), and then repeat step 9 to release the order to the warehouse.</span></span>

### <a name="part-2-change-the-location-for-a-work-line"></a><span data-ttu-id="bf8fb-172">Del 2: Endre lokasjonen for en arbeidslinje</span><span class="sxs-lookup"><span data-stu-id="bf8fb-172">Part 2: Change the location for a work line</span></span>

1. <span data-ttu-id="bf8fb-173">Gå til **Lagerstyring \> Arbeid \> Arbeidslinjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-173">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="bf8fb-174">Finn og velg en av arbeidslinjene du opprettet for denne demonstrasjonen.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-174">Find and select one of the work lines that you created for this demo.</span></span>
1. <span data-ttu-id="bf8fb-175">Velg **Endre lokasjon** for å åpne **Velg ny lokasjon**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-175">Select **Change location** to open the **Select new location** dialog box.</span></span>
1. <span data-ttu-id="bf8fb-176">I **Velg ny lokasjon**-dialogboksen i **Lokasjon**-feltet velger du en ny lokasjon for arbeidslinjen.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-176">In the **Select new location** dialog box, in the **Location** field, select a new location for the work line.</span></span>
1. <span data-ttu-id="bf8fb-177">Velg **OK** for ta i bruk endringen og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-177">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf8fb-178">Du kan bare sende lokasjonsendringer hvis den nye lokasjonen har nok tilgjengelig beholdning (for en plukking), eller hvis den består lokasjonstypevalidering (for en plassering).</span><span class="sxs-lookup"><span data-stu-id="bf8fb-178">You can submit location changes only if the new location has enough inventory available (for a pick), or if it passes location-type validation (for a put).</span></span>

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a><span data-ttu-id="bf8fb-179">Del 3: Endre antallet i en arbeidslinje eller avbryt en arbeidslinje</span><span class="sxs-lookup"><span data-stu-id="bf8fb-179">Part 3: Change the quantity of a work line or cancel a work line</span></span>

1. <span data-ttu-id="bf8fb-180">Gå til **Lagerstyring \> Arbeid \> Arbeidslinjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-180">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="bf8fb-181">Finn og velg en av arbeidslinjene du opprettet for denne demonstrasjonen.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-181">Find and select one of the work lines that you created for this demo.</span></span> <span data-ttu-id="bf8fb-182">Vær oppmerksom på at du bare kan avbryte eller endre antall for arbeidslinjer der arbeidstypen er _plukk_.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-182">Note that you can cancel or change quantities only for work lines where the work type is _pick_.</span></span>
1. <span data-ttu-id="bf8fb-183">Velg **Avbryt arbeidslinje** for å åpne **Antall som skal avbrytes**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-183">Select **Cancel work line** to open the **Quantity to cancel** dialog box.</span></span>
1. <span data-ttu-id="bf8fb-184">I **Antall som skal avbrytes**-dialogboksen endrer du verdien i **Antall**-feltet for å angi antallet som skal *trekkes fra* antallet som for øyeblikket er angitt for linjen.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-184">In the **Quantity to cancel** dialog box, change the value in the **Quantity** field to specify the quantity that should be *subtracted from* the quantity that is currently specified for the line.</span></span> <span data-ttu-id="bf8fb-185">Som standard viser **Antall**-feltet hele antallet.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-185">By default, the **Quantity** field shows the full quantity.</span></span>

    - <span data-ttu-id="bf8fb-186">Hvis du avbryter hele antallet, endres **Arbeidsstatus**-verdien til _Avbrutt_, men **Arbeidsantall**-feltet vil fremdeles vise den opprinnelige verdien.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-186">If you cancel the full quantity, the **Work status** value will be changed to _Canceled_, but the **Work quantity** field will still show the original value.</span></span>
    - <span data-ttu-id="bf8fb-187">Hvis du bare deler av antallet, oppdateres **Arbeidsantall**-feltet for å vise den nye verdien, men **Arbeidsstatus**-verdien endres ikke.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-187">If you cancel just part of the quantity, the **Work quantity** field will be updated to show the new value, but the **Work status** value won't change.</span></span>

1. <span data-ttu-id="bf8fb-188">Velg **OK** for ta i bruk endringen og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-188">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf8fb-189">Hvis du avbryter bare en del av antallet for en arbeidslinje, må du også fjerne det foreldede antallet fra lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-189">If you cancel just part of the quantity for a work line, you must also remove the obsolete quantity from the load line.</span></span> <span data-ttu-id="bf8fb-190">Hvis ikke, med mindre underlevering er konfigurert riktig, kan ikke belastningslinjen leveringsbekreftes.</span><span class="sxs-lookup"><span data-stu-id="bf8fb-190">Otherwise, unless under-delivery is set up correctly, the load line can't be ship-confirmed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]