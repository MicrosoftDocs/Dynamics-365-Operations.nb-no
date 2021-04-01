---
title: Plukklinjegruppering
description: Dette emnet gir en oversikt over plukklinjegruppering.
author: Mirzaab
manager: tfehr
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ab8cdd7cad5420aca0de53e59220da9e230d411
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234639"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="edcde-103">Plukklinjegruppering</span><span class="sxs-lookup"><span data-stu-id="edcde-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="edcde-104">Plukklinjegruppering gjør at flere arbeidslinjer som har samme vare og lokasjon, kan kombineres til én plukking som presenteres for brukeren på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="edcde-104">Pick line grouping enables multiple work lines that have the same item and location to be combined into a single pick that is presented to the user on the mobile device.</span></span> <span data-ttu-id="edcde-105">Derfor kan lagermedarbeidere motta så effektive instruksjoner som mulig, men den nødvendige separasjonen av arbeidslinjer (for ulike beholdere, ordrer og så videre) kan fortsatt opprettholdes i systemet.</span><span class="sxs-lookup"><span data-stu-id="edcde-105">Therefore, warehouse workers can receive the most efficient instructions, but required work line separation (for different containers, orders, and so on) can still be maintained in the system.</span></span>

## <a name="turn-on-the-pick-line-grouping-feature"></a><span data-ttu-id="edcde-106">Aktivere funksjonen for plukklinjegruppering</span><span class="sxs-lookup"><span data-stu-id="edcde-106">Turn on the pick line grouping feature</span></span>

<span data-ttu-id="edcde-107">Før du kan bruke denne funksjonen, må den være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="edcde-107">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="edcde-108">Administratorer kan bruke arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere statusen for funksjonen og aktivere den om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="edcde-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="edcde-109">Funksjonen vises på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="edcde-109">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="edcde-110">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="edcde-110">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="edcde-111">**Funksjonsnavn:** *Plukklinjegruppering*</span><span class="sxs-lookup"><span data-stu-id="edcde-111">**Feature name:** *Pick line grouping*</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="edcde-112">Definere plukklinjegruppering</span><span class="sxs-lookup"><span data-stu-id="edcde-112">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="edcde-113">Opprette et menyelement for mobilenhet</span><span class="sxs-lookup"><span data-stu-id="edcde-113">Create a mobile device menu item</span></span>

1. <span data-ttu-id="edcde-114">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="edcde-114">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="edcde-115">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="edcde-115">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="edcde-116">I feltet **Menyelementnavn** angir du *Linjeplukking for salgsgruppe*.</span><span class="sxs-lookup"><span data-stu-id="edcde-116">In the **Menu item name** field, enter *Sales group line picking*.</span></span>
1. <span data-ttu-id="edcde-117">I **Tittel**-feltet angir du *Linjeplukking for salgsgruppe*.</span><span class="sxs-lookup"><span data-stu-id="edcde-117">In the **Title** field, enter *Sales group line picking*.</span></span> <span data-ttu-id="edcde-118">Denne tittelen vises på menyen på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="edcde-118">This title will be shown on the mobile device menu.</span></span>
1. <span data-ttu-id="edcde-119">Velg *Arbeid* i feltet **Modus**.</span><span class="sxs-lookup"><span data-stu-id="edcde-119">In the **Mode** field, select *Work*.</span></span>
1. <span data-ttu-id="edcde-120">Angi alternativet **Bruk eksisterende arbeid** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="edcde-120">Set the **Use existing work** option to *Yes*.</span></span>
1. <span data-ttu-id="edcde-121">Angi følgende verdier i **Generelt**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="edcde-121">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="edcde-122">Velg **Brukerstyrt** i feltet *Styrt av*.</span><span class="sxs-lookup"><span data-stu-id="edcde-122">In the **Directed by** field, select *User directed*.</span></span>
    - <span data-ttu-id="edcde-123">Sett alternativet **Generer nummerskilt** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="edcde-123">Set the **Generate license plate** option to *Yes*.</span></span>
    - <span data-ttu-id="edcde-124">Sett alternativet **Gruppeplukking** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="edcde-124">Set the **Group pick** option to *Yes*.</span></span>
    - <span data-ttu-id="edcde-125">Godta standardverdiene for de resterende alternativene.</span><span class="sxs-lookup"><span data-stu-id="edcde-125">Accept the default values for the remaining options.</span></span>

1. <span data-ttu-id="edcde-126">Følg denne fremgangsmåten for å konfigurere gyldige arbeidsklasser for menyelementet på mobilenheten:</span><span class="sxs-lookup"><span data-stu-id="edcde-126">Follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="edcde-127">Velg **Ny** i hurtigfanen **Arbeidsklasser**.</span><span class="sxs-lookup"><span data-stu-id="edcde-127">On the **Work classes** FastTab, elect **New**.</span></span>
    2. <span data-ttu-id="edcde-128">I feltet **Arbeidsklasse-ID** kan du velge *Salg* eller *Salgsordreplukking*, avhengig av lageret du skal bruke.</span><span class="sxs-lookup"><span data-stu-id="edcde-128">In the **Work class ID** field, you can select either *Sales* or *SO Pick*, depending on the warehouse that you will use.</span></span> <span data-ttu-id="edcde-129">I dette scenarioet velger du *Salgsordreplukking*.</span><span class="sxs-lookup"><span data-stu-id="edcde-129">For this scenario, select *SO Pick*.</span></span>

        <span data-ttu-id="edcde-130">Feltet **Arbeidsordretype** settes automatisk til *Salgsordrer*.</span><span class="sxs-lookup"><span data-stu-id="edcde-130">The **Work order type** field is automatically set to *Sales orders*.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="edcde-131">Definere en mobilenhetsmeny</span><span class="sxs-lookup"><span data-stu-id="edcde-131">Set up a mobile device menu</span></span>

<span data-ttu-id="edcde-132">Følg denne fremgangsmåten for å legge til menyelementet du nettopp opprettet, på **Utgående**-menyen.</span><span class="sxs-lookup"><span data-stu-id="edcde-132">Follow these steps to add the menu item that you just created to the **Outbound** menu.</span></span>

1. <span data-ttu-id="edcde-133">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="edcde-133">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="edcde-134">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="edcde-134">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="edcde-135">Listeruten viser alle eksisterende menyer på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="edcde-135">The list pane shows all existing mobile device menus.</span></span> <span data-ttu-id="edcde-136">Velg *Utgående* i listen.</span><span class="sxs-lookup"><span data-stu-id="edcde-136">Select *Outbound* in the list.</span></span>
1. <span data-ttu-id="edcde-137">I listen **Tilgjengelige menyer og menyelementer** finner og velger du menyelementet *Linjeplukking for salgsgruppe* du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="edcde-137">In the **Available menus and menu items** list, find and select the *Sales group line picking* menu item that you created.</span></span>
1. <span data-ttu-id="edcde-138">Velg høyre pil for å flytte menyelementet *Linjeplukking for salgsgruppe* til **Menystruktur**-listen.</span><span class="sxs-lookup"><span data-stu-id="edcde-138">Select the right arrow button to move the *Sales group line picking* menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="edcde-139">Bruk pil opp og pil ned til å flytte menyelementet til ønsket plassering i menystrukturen.</span><span class="sxs-lookup"><span data-stu-id="edcde-139">Use the up arrow and down arrow buttons to move the menu item into the desired position in the menu structure.</span></span>
1. <span data-ttu-id="edcde-140">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="edcde-140">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="edcde-141">Konfigurere en arbeidsmal</span><span class="sxs-lookup"><span data-stu-id="edcde-141">Set up a work template</span></span>

1. <span data-ttu-id="edcde-142">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.</span><span class="sxs-lookup"><span data-stu-id="edcde-142">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="edcde-143">Velg *Salgsordrer* i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="edcde-143">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="edcde-144">I rutenettet **Oversikt** finner og velger du arbeidsmalen som skal brukes med denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="edcde-144">In the **Overview** grid, find and select the work template that should be used with this function.</span></span> <span data-ttu-id="edcde-145">I dette scenarioet velger du malen *51 Plukk til trinn*.</span><span class="sxs-lookup"><span data-stu-id="edcde-145">For this scenario, select the *51 Pick to stage* template.</span></span>
1. <span data-ttu-id="edcde-146">I handlingsruten velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="edcde-146">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="edcde-147">I **Sortering**-fanen i dialogboksen for redigeringsprogram for spørring velger du **Legg til**, og deretter angir du følgende verdier for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="edcde-147">In the query editor dialog box, on the **Sorting** tab, select **Add**, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="edcde-148">I **Tabell**-kolonnen velger du *Midlertidige arbeidstransaksjoner*.</span><span class="sxs-lookup"><span data-stu-id="edcde-148">In the **Table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="edcde-149">I **Avledet tabell**-kolonnen velger du *Midlertidige arbeidstransaksjoner*.</span><span class="sxs-lookup"><span data-stu-id="edcde-149">In the **Derived table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="edcde-150">Velg *Varenummer* i **Felt**-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="edcde-150">In the **Field** column, select *Item number*.</span></span>
    - <span data-ttu-id="edcde-151">I kolonnen **Søkeretning** velger du *Stigende*.</span><span class="sxs-lookup"><span data-stu-id="edcde-151">In the **Search direction** column, select *Ascending*.</span></span>

1. <span data-ttu-id="edcde-152">Velg **OK** for å lukke dialogboksen og lagre valget ditt.</span><span class="sxs-lookup"><span data-stu-id="edcde-152">Select **OK** to close the dialog box and save your selection.</span></span>
1. <span data-ttu-id="edcde-153">Du får følgende melding: «Grupperingen blir tilbakeført – vil du fortsette?»</span><span class="sxs-lookup"><span data-stu-id="edcde-153">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="edcde-154">Klikk på **Ja** for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="edcde-154">Select **Yes** to continue.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="edcde-155">For at grupperingsfunksjonaliteten for plukklinjen skal fungere, må arbeidslinjene sorteres etter vare-ID.</span><span class="sxs-lookup"><span data-stu-id="edcde-155">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="edcde-156">Hvis linjer som har de samme elementene, ikke er i rekkefølge etter hverandre, grupperes de ikke.</span><span class="sxs-lookup"><span data-stu-id="edcde-156">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="edcde-157">Eksempel</span><span class="sxs-lookup"><span data-stu-id="edcde-157">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="edcde-158">Opprett plukkarbeid</span><span class="sxs-lookup"><span data-stu-id="edcde-158">Create picking work</span></span>

<span data-ttu-id="edcde-159">Før du kan definere plukklinjegruppering, må du opprette noe kvalifisert utgående arbeid.</span><span class="sxs-lookup"><span data-stu-id="edcde-159">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="edcde-160">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="edcde-160">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="edcde-161">Velg **Ny** for å opprette en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="edcde-161">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="edcde-162">Velg *US-004* i **Kundekonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="edcde-162">In the **Customer account** field, select *US-004*.</span></span>
1. <span data-ttu-id="edcde-163">På hurtigfanen **Generelt**, i **Lager**-feltet, velger du *51*.</span><span class="sxs-lookup"><span data-stu-id="edcde-163">On the **General** FastTab, in the **Warehouse** field, select *51*.</span></span>
1. <span data-ttu-id="edcde-164">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="edcde-164">Select **OK**.</span></span>
1. <span data-ttu-id="edcde-165">Legg til følgende seks linjer i hurtigfanen **Salgsordrelinjer**:</span><span class="sxs-lookup"><span data-stu-id="edcde-165">On the **Sales order lines** FastTab, add the following six lines:</span></span>

    - <span data-ttu-id="edcde-166">**Linje 1:** I **Varenummer**-feltet velger du *M9200*.</span><span class="sxs-lookup"><span data-stu-id="edcde-166">**Line 1:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="edcde-167">I feltet **Antall** angi *3*.</span><span class="sxs-lookup"><span data-stu-id="edcde-167">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="edcde-168">**Linje 2:** I **Varenummer**-feltet velger du *M9201*.</span><span class="sxs-lookup"><span data-stu-id="edcde-168">**Line 2:** In the **Item number** field, select *M9201*.</span></span> <span data-ttu-id="edcde-169">I feltet **Antall** angi *3*.</span><span class="sxs-lookup"><span data-stu-id="edcde-169">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="edcde-170">**Linje 3:** I **Varenummer**-feltet velger du *M9202*.</span><span class="sxs-lookup"><span data-stu-id="edcde-170">**Line 3:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="edcde-171">I feltet **Antall** angi *2*.</span><span class="sxs-lookup"><span data-stu-id="edcde-171">In the **Quantity** field, enter *2*.</span></span>
    - <span data-ttu-id="edcde-172">**Linje 4:** I **Varenummer**-feltet velger du *M9200*.</span><span class="sxs-lookup"><span data-stu-id="edcde-172">**Line 4:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="edcde-173">I feltet **Antall** angi *1*.</span><span class="sxs-lookup"><span data-stu-id="edcde-173">In the **Quantity** field, enter *1*.</span></span>
    - <span data-ttu-id="edcde-174">**Linje 5:** I **Varenummer**-feltet velger du *M9200*.</span><span class="sxs-lookup"><span data-stu-id="edcde-174">**Line 5:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="edcde-175">I feltet **Antall** angi *3*.</span><span class="sxs-lookup"><span data-stu-id="edcde-175">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="edcde-176">**Linje 6:** I **Varenummer**-feltet velger du *M9202*.</span><span class="sxs-lookup"><span data-stu-id="edcde-176">**Line 6:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="edcde-177">I feltet **Antall** angi *7*.</span><span class="sxs-lookup"><span data-stu-id="edcde-177">In the **Quantity** field, enter *7*.</span></span>

    <span data-ttu-id="edcde-178">Her er et sammendrag av totalt antall for hver vare:</span><span class="sxs-lookup"><span data-stu-id="edcde-178">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="edcde-179">**Vare M9200:** *7* hver</span><span class="sxs-lookup"><span data-stu-id="edcde-179">**Item M9200:** *7* each</span></span>
    - <span data-ttu-id="edcde-180">**Vare M9201:** *3* hver</span><span class="sxs-lookup"><span data-stu-id="edcde-180">**Item M9201:** *3* each</span></span>
    - <span data-ttu-id="edcde-181">**Vare M9202:** *9* hver</span><span class="sxs-lookup"><span data-stu-id="edcde-181">**Item M9202:** *9* each</span></span>

1. <span data-ttu-id="edcde-182">Før du frigir ordrene til lageret, må du kontrollere at plukklokasjonene har nok beholdning for alle varene på alle ordrene.</span><span class="sxs-lookup"><span data-stu-id="edcde-182">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="edcde-183">Se gjennom **Lokasjonsdirektiv**-innstillingen for å bestemme hvilke plukklokasjoner som skal brukes for plukking av salgsordre.</span><span class="sxs-lookup"><span data-stu-id="edcde-183">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span> <span data-ttu-id="edcde-184">Hvis du bruker demonstrasjonsdatamiljøet Contoso for lager *51*, bekrefter du at det finnes tilgjengelig beholdning.</span><span class="sxs-lookup"><span data-stu-id="edcde-184">If you're using the Contoso demo data environment for warehouse *51*, confirm that there is available inventory.</span></span>

    <span data-ttu-id="edcde-185">Du må nå reservere beholdningen for hver linje.</span><span class="sxs-lookup"><span data-stu-id="edcde-185">You must now reserve the inventory for each line.</span></span>

1. <span data-ttu-id="edcde-186">I hurtigfanen **Salgsordrelinjer** velger du en av linjene som må reserveres.</span><span class="sxs-lookup"><span data-stu-id="edcde-186">On the **Sales order lines** FastTab, select one of the lines that must be reserved.</span></span>
1. <span data-ttu-id="edcde-187">Velg **Reservasjon** på **Beholdning**-menyen over rutenettet.</span><span class="sxs-lookup"><span data-stu-id="edcde-187">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="edcde-188">I handlingsruten på **Reservasjon**-siden velger du **Reserver parti** for å gjøre reservasjonen gjeldende.</span><span class="sxs-lookup"><span data-stu-id="edcde-188">On the **Reservation** page, on the Action Pane, select **Reserve lot** to apply the reservation.</span></span> <span data-ttu-id="edcde-189">Lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="edcde-189">Then close the page.</span></span>
1. <span data-ttu-id="edcde-190">Gjenta trinn 8 til og med 10 for de gjenstående linjene som må reserveres.</span><span class="sxs-lookup"><span data-stu-id="edcde-190">Repeat steps 8 through 10 for the remaining lines that must be reserved.</span></span>

    <span data-ttu-id="edcde-191">Du må nå frigi salgsordren til lageret.</span><span class="sxs-lookup"><span data-stu-id="edcde-191">You must now release the sales order to the warehouse.</span></span>

1. <span data-ttu-id="edcde-192">Velg **Frigi til lager** i fanen **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="edcde-192">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="edcde-193">Du får en melding om at det er opprettet en forsendelse og en bølge, og at bølgen er sendt for å bli kjørt i en bunke.</span><span class="sxs-lookup"><span data-stu-id="edcde-193">You receive a message that states that a shipment and a wave have been created, and that the wave has been submitted to run in a batch.</span></span>

    <span data-ttu-id="edcde-194">Når bølgen og alle nedstrøms jobber er fullført, opprettes en arbeids-ID for arbeid som har seks linjer.</span><span class="sxs-lookup"><span data-stu-id="edcde-194">When the wave and all downstream jobs have been completed, a work ID is created for work that has six lines.</span></span> <span data-ttu-id="edcde-195">Linjene sorteres etter varenummer.</span><span class="sxs-lookup"><span data-stu-id="edcde-195">The lines are sorted by item number.</span></span>

1. <span data-ttu-id="edcde-196">Gå til **Lagerstyring \> Arbeid \> Alt arbeid** for å vise arbeidet som ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="edcde-196">Go to **Warehouse management \> Work \> All work** to view the work that was created.</span></span> <span data-ttu-id="edcde-197">Noter verdien for **Arbeids-ID**, fordi du kommer til å få behov for den i neste fremgangsmåte.</span><span class="sxs-lookup"><span data-stu-id="edcde-197">Make a note of the **Work ID** value, because you will need it in the next procedure.</span></span>

### <a name="initiate-picking-from-the-mobile-device"></a><span data-ttu-id="edcde-198">Starte plukking fra mobilenheten</span><span class="sxs-lookup"><span data-stu-id="edcde-198">Initiate picking from the mobile device</span></span>

1. <span data-ttu-id="edcde-199">Logg på mobilenheten som en bruker som er aktivert for lager *51*.</span><span class="sxs-lookup"><span data-stu-id="edcde-199">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="edcde-200">På mobilenheten velger du menyen som inneholder det nye menyelementet for mobilenhet.</span><span class="sxs-lookup"><span data-stu-id="edcde-200">On the mobile device, select the menu that includes the new mobile device menu item.</span></span> <span data-ttu-id="edcde-201">I dette scenarioet velger du **Utgående**.</span><span class="sxs-lookup"><span data-stu-id="edcde-201">For this scenario, select **Outbound**.</span></span>
1. <span data-ttu-id="edcde-202">Velg menyelementet **Linjeplukking for salgsgruppe** for å starte plukkingen.</span><span class="sxs-lookup"><span data-stu-id="edcde-202">Select the **Sales group line picking** menu item to initiate the pick.</span></span>
1. <span data-ttu-id="edcde-203">Angi **Arbeids-ID**-verdien du noterte i forrige fremgangsmåte.</span><span class="sxs-lookup"><span data-stu-id="edcde-203">Enter the **Work ID** value that you made a note of in the previous procedure.</span></span>

    <span data-ttu-id="edcde-204">Du skal se et plukktrinn der alle plukklinjer for varen *M9200* er gruppert, og du skal få en instruks om å plukke *7* hver av varen *M9200*.</span><span class="sxs-lookup"><span data-stu-id="edcde-204">You should see a pick step where all pick lines for item *M9200* are grouped, and you should receive an instruction to pick *7* each of item *M9200*.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="edcde-205">På mobilenheten er plukkarbeidet for de tre plukkarbeidslinjene samlet i ett plukktrinn for brukeren.</span><span class="sxs-lookup"><span data-stu-id="edcde-205">On the mobile device, the pick work for the three pick work lines has been aggregated into one picking step for the user.</span></span>

1. <span data-ttu-id="edcde-206">Bekreft plukktrinnet.</span><span class="sxs-lookup"><span data-stu-id="edcde-206">Confirm the pick step.</span></span>
1. <span data-ttu-id="edcde-207">Gå til arbeidssiden for arbeids-ID-en, og legg merke til at alle tre plukklinjer for varen *M9200* ble lukket samtidig.</span><span class="sxs-lookup"><span data-stu-id="edcde-207">Go to the work page for the work ID, and notice that all three pick lines for item *M9200* were closed simultaneously.</span></span>
1. <span data-ttu-id="edcde-208">Gå tilbake til mobilenheten, og fortsett å plukke.</span><span class="sxs-lookup"><span data-stu-id="edcde-208">Go back to the mobile device, and continue to pick.</span></span> <span data-ttu-id="edcde-209">Arbeidslinje 4 for vare *M9201* skal vises.</span><span class="sxs-lookup"><span data-stu-id="edcde-209">Work line 4 for item *M9201* should be presented.</span></span> <span data-ttu-id="edcde-210">Siden det bare var én arbeidslinje i ordren, er det ingenting å samle.</span><span class="sxs-lookup"><span data-stu-id="edcde-210">Because there was only one work line on the order, there is nothing to aggregate.</span></span>
1. <span data-ttu-id="edcde-211">Bekreft plukktrinnet.</span><span class="sxs-lookup"><span data-stu-id="edcde-211">Confirm the pick step.</span></span>
1. <span data-ttu-id="edcde-212">Det siste plukktrinnet på mobilenheten samler de to siste plukklinjene fra arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="edcde-212">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>
1. <span data-ttu-id="edcde-213">Fullfør plukktrinnet for *9* hver av varen *M9202*.</span><span class="sxs-lookup"><span data-stu-id="edcde-213">Complete the pick step for *9* each of item *M9202*.</span></span>
1. <span data-ttu-id="edcde-214">Bekreft plasseringstrinnet og eventuelle ekstra plukkings-/plasseringspar for å fullføre arbeidet.</span><span class="sxs-lookup"><span data-stu-id="edcde-214">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!IMPORTANT]
>
> - <span data-ttu-id="edcde-215">Arbeidslinjer kan bare grupperes hvis de er i rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="edcde-215">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="edcde-216">Følgende funksjonalitet støttes ikke:</span><span class="sxs-lookup"><span data-stu-id="edcde-216">The following functionality isn't supported:</span></span>
>
>   - <span data-ttu-id="edcde-217">Faktisk vekt-varer</span><span class="sxs-lookup"><span data-stu-id="edcde-217">Catch-weight items</span></span>
>
>    <span data-ttu-id="edcde-218">Hvis det er noen faktisk vekt-varer på arbeidet, får du en feilmelding før du begynner å plukke.</span><span class="sxs-lookup"><span data-stu-id="edcde-218">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>
>   - <span data-ttu-id="edcde-219">Stykkplukking</span><span class="sxs-lookup"><span data-stu-id="edcde-219">Piece picking</span></span>
>   - <span data-ttu-id="edcde-220">Arbeidslinjer som har uferdig etterfyllingsarbeid</span><span class="sxs-lookup"><span data-stu-id="edcde-220">Work lines that have unfinished replenishment work</span></span>
>   - <span data-ttu-id="edcde-221">Overplukking</span><span class="sxs-lookup"><span data-stu-id="edcde-221">Over-picking</span></span>
>   - <span data-ttu-id="edcde-222">Ny tildeling av vare for plukking med mangler</span><span class="sxs-lookup"><span data-stu-id="edcde-222">Short picking with item reallocation</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]