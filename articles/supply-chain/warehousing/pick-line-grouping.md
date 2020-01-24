---
title: Plukklinjegruppering
description: Dette emnet gir en oversikt over plukklinjegruppering.
author: Mirzaab
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1b1d0135d450bc9be7b1303240a9ca70f95ae38e
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906274"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="aba49-103">Plukklinjegruppering</span><span class="sxs-lookup"><span data-stu-id="aba49-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aba49-104">I plukklinjegruppering kan flere arbeidslinjer som har samme vare og lokasjon, kombineres til én enkelt plukking som presenteres for brukeren på en mobilenhet.</span><span class="sxs-lookup"><span data-stu-id="aba49-104">In pick line grouping, multiple work lines that have the same item and location can be combined into a single pick that is presented to the user on a mobile device.</span></span> <span data-ttu-id="aba49-105">Derfor kan lagermedarbeidere motta de mest effektive instruksjonene som er mulige, men den nødvendige separasjon av arbeidslinjer i systemet opprettholdes også (for eksempel for ulike beholdere og ordrer).</span><span class="sxs-lookup"><span data-stu-id="aba49-105">Therefore, warehouse workers can receive the most efficient instructions that are possible, but the required separation of work lines in the system is also maintained (for example, for different containers and orders).</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="aba49-106">Definere plukklinjegruppering</span><span class="sxs-lookup"><span data-stu-id="aba49-106">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="aba49-107">Opprette et menyelement for mobilenhet</span><span class="sxs-lookup"><span data-stu-id="aba49-107">Create a mobile device menu item</span></span>

1. <span data-ttu-id="aba49-108">Gå til **Lagerstyrings \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**, og opprett et nytt menyelement som heter **Linjeplukking for salgsgruppe – brukerstyrt**.</span><span class="sxs-lookup"><span data-stu-id="aba49-108">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**, and create a new menu item that is named **Sales group line picking – User directed**.</span></span>
2. <span data-ttu-id="aba49-109">Angi følgende verdier under **Menyelementer på mobilenheten**:</span><span class="sxs-lookup"><span data-stu-id="aba49-109">Under **Mobile device menu items**, set the following values:</span></span>

    - <span data-ttu-id="aba49-110">I **Menyelementnavn**-feltet angir du **Salgsplukking - gruppelinje**.</span><span class="sxs-lookup"><span data-stu-id="aba49-110">In the **Menu item name** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="aba49-111">I **Tittel**-feltet angir du **Salgsplukking - gruppelinje**.</span><span class="sxs-lookup"><span data-stu-id="aba49-111">In the **Title** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="aba49-112">Velg **Arbeid** i feltet **Modus**.</span><span class="sxs-lookup"><span data-stu-id="aba49-112">In the **Mode** field, select **Work**.</span></span>
    - <span data-ttu-id="aba49-113">Angi alternativet **Bruk eksisterende arbeid** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="aba49-113">Set the **Use existing work** option to **Yes**.</span></span>

3. <span data-ttu-id="aba49-114">I hurtigfanen **Generelt** kan du angir følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="aba49-114">On the **General** FastTab, you can set the following values:</span></span>

    - <span data-ttu-id="aba49-115">Velg **Brukerstyrt** i feltet **Styrt av**.</span><span class="sxs-lookup"><span data-stu-id="aba49-115">In the **Directed by** field, select **User directed**.</span></span>
    - <span data-ttu-id="aba49-116">Sett alternativet **Generer nummerskilt** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="aba49-116">Set the **Generate license plate** option to **Yes**.</span></span>
    - <span data-ttu-id="aba49-117">Sett alternativet **Gruppeplukking** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="aba49-117">Set the **Group pick** option to **Yes**.</span></span>

4. <span data-ttu-id="aba49-118">I hurtigfanen **Arbeidsklasser** følger du denne fremgangsmåten for å konfigurere gyldige arbeidsklasser for menyelementet for mobilenheten:</span><span class="sxs-lookup"><span data-stu-id="aba49-118">On the **Work classes** FastTab, follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="aba49-119">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="aba49-119">Select **New**.</span></span>
    2. <span data-ttu-id="aba49-120">I feltet **Arbeidsklasse-ID** velger du **Salg** eller **Salgsordreplukking**, avhengig av lageret du skal bruke.</span><span class="sxs-lookup"><span data-stu-id="aba49-120">In the **Work class ID** field, select **Sales** or **SO Pick**, depending on the warehouse that you will use.</span></span>
    3. <span data-ttu-id="aba49-121">Velg **Salgsordrer** i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="aba49-121">In the **Work order type** field, select **Sales orders**.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="aba49-122">Definere en mobilenhetsmeny</span><span class="sxs-lookup"><span data-stu-id="aba49-122">Set up a mobile device menu</span></span>

1. <span data-ttu-id="aba49-123">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="aba49-123">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span> 
1. <span data-ttu-id="aba49-124">Legg til menyelementet du nettopp opprettet, i ønsket meny.</span><span class="sxs-lookup"><span data-stu-id="aba49-124">Add the menu item that you just created to the desired menu.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="aba49-125">Konfigurere en arbeidsmal</span><span class="sxs-lookup"><span data-stu-id="aba49-125">Set up a work template</span></span>

1. <span data-ttu-id="aba49-126">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.</span><span class="sxs-lookup"><span data-stu-id="aba49-126">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="aba49-127">Finn arbeidsmalen som skal brukes med denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="aba49-127">Find the work template that should be used with this function.</span></span> <span data-ttu-id="aba49-128">I dette eksemplet kan du velge standard Contoso-arbeidsmal **51 Plukk til trinn**.</span><span class="sxs-lookup"><span data-stu-id="aba49-128">For this example, select the standard **51 Pick to stage** Contoso work template.</span></span>
1. <span data-ttu-id="aba49-129">Velg **Rediger spørring** på menyen.</span><span class="sxs-lookup"><span data-stu-id="aba49-129">On the menu, select **Edit query**.</span></span>
1. <span data-ttu-id="aba49-130">Velg **Legg til** i kategorien **Sortering**, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="aba49-130">On the **Sorting** tab, select **Add**, and then set the following values:</span></span>

    - <span data-ttu-id="aba49-131">I **Tabell**-feltet velger du **Midlertidige arbeidstransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="aba49-131">In the **Table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="aba49-132">I **Avledet tabell**-feltet velger du **Midlertidige arbeidstransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="aba49-132">In the **Derived table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="aba49-133">Velg **Varenummer** i feltet **Felt**.</span><span class="sxs-lookup"><span data-stu-id="aba49-133">In the **Field** field, select **Item number**.</span></span>
    - <span data-ttu-id="aba49-134">I feltet **Søkeretning** velger du **Stigende**.</span><span class="sxs-lookup"><span data-stu-id="aba49-134">In the **Search direction** field, select **Ascending**.</span></span>

> [!NOTE]
> <span data-ttu-id="aba49-135">For at grupperingsfunksjonaliteten for plukklinjen skal fungere, må arbeidslinjene sorteres etter vare-ID.</span><span class="sxs-lookup"><span data-stu-id="aba49-135">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="aba49-136">Hvis linjer som har de samme elementene, ikke er i rekkefølge etter hverandre, grupperes de ikke.</span><span class="sxs-lookup"><span data-stu-id="aba49-136">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="aba49-137">Eksempel</span><span class="sxs-lookup"><span data-stu-id="aba49-137">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="aba49-138">Opprett plukkarbeid</span><span class="sxs-lookup"><span data-stu-id="aba49-138">Create picking work</span></span>

<span data-ttu-id="aba49-139">Før du kan definere plukklinjegruppering, må du opprette noe kvalifisert utgående arbeid.</span><span class="sxs-lookup"><span data-stu-id="aba49-139">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="aba49-140">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="aba49-140">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="aba49-141">Velg **Ny** for å opprette en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="aba49-141">Select **New** to create a sales order.</span></span> 
3. <span data-ttu-id="aba49-142">Velg en kunde i **Kundekonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="aba49-142">In the **Customer account** field, select any customer.</span></span> 
4. <span data-ttu-id="aba49-143">På hurtigfanen **Generelt**, i **Lager**-feltet, velger du **51**.</span><span class="sxs-lookup"><span data-stu-id="aba49-143">On the **General** FastTab, in the **Warehouse** field, select **51**.</span></span> <span data-ttu-id="aba49-144">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="aba49-144">Then select **OK**.</span></span>
5. <span data-ttu-id="aba49-145">Legg til følgende seks linjer under **Salgsordrelinjer**:</span><span class="sxs-lookup"><span data-stu-id="aba49-145">Under **Sales order lines**, add the following six lines:</span></span>

    - <span data-ttu-id="aba49-146">**Linje 1:** I **Varenummer**-feltet velger du **M9200**.</span><span class="sxs-lookup"><span data-stu-id="aba49-146">**Line 1:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="aba49-147">I feltet **Antall** angi **3**.</span><span class="sxs-lookup"><span data-stu-id="aba49-147">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="aba49-148">**Linje 2:** I **Varenummer**-feltet velger du **M9201**.</span><span class="sxs-lookup"><span data-stu-id="aba49-148">**Line 2:** In the **Item number** field, select **M9201**.</span></span> <span data-ttu-id="aba49-149">I feltet **Antall** angi **3**.</span><span class="sxs-lookup"><span data-stu-id="aba49-149">In the **Quantity** field, enter **3**.</span></span> 
    - <span data-ttu-id="aba49-150">**Linje 3:** I **Varenummer**-feltet velger du **M9202**.</span><span class="sxs-lookup"><span data-stu-id="aba49-150">**Line 3:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="aba49-151">I feltet **Antall** angi **2**.</span><span class="sxs-lookup"><span data-stu-id="aba49-151">In the **Quantity** field, enter **2**.</span></span> 
    - <span data-ttu-id="aba49-152">**Linje 4:** I **Varenummer**-feltet velger du **M9200**.</span><span class="sxs-lookup"><span data-stu-id="aba49-152">**Line 4:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="aba49-153">I feltet **Antall** angi **1**.</span><span class="sxs-lookup"><span data-stu-id="aba49-153">In the **Quantity** field, enter **1**.</span></span> 
    - <span data-ttu-id="aba49-154">**Linje 5:** I **Varenummer**-feltet velger du **M9200**.</span><span class="sxs-lookup"><span data-stu-id="aba49-154">**Line 5:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="aba49-155">I feltet **Antall** angi **3**.</span><span class="sxs-lookup"><span data-stu-id="aba49-155">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="aba49-156">**Linje 6:** I **Varenummer**-feltet velger du **M9202**.</span><span class="sxs-lookup"><span data-stu-id="aba49-156">**Line 6:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="aba49-157">I feltet **Antall** angi **7**.</span><span class="sxs-lookup"><span data-stu-id="aba49-157">In the **Quantity** field, enter **7**.</span></span> 

    <span data-ttu-id="aba49-158">Her er et sammendrag av totalt antall for hver vare:</span><span class="sxs-lookup"><span data-stu-id="aba49-158">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="aba49-159">**Vare M9200:** 7 hver</span><span class="sxs-lookup"><span data-stu-id="aba49-159">**Item M9200:** 7 each</span></span>
    - <span data-ttu-id="aba49-160">**Vare M9201:** 3 hver</span><span class="sxs-lookup"><span data-stu-id="aba49-160">**Item M9201:** 3 each</span></span>
    - <span data-ttu-id="aba49-161">**Vare M9202:** 9 hver</span><span class="sxs-lookup"><span data-stu-id="aba49-161">**Item M9202:** 9 each</span></span>

6. <span data-ttu-id="aba49-162">Før du frigir ordrene til lageret, må du kontrollere at plukklokasjonene har nok beholdning for alle varene på alle ordrene.</span><span class="sxs-lookup"><span data-stu-id="aba49-162">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="aba49-163">Se gjennom **Lokasjonsdirektiv**-innstillingen for å bestemme hvilke plukklokasjoner som skal brukes for plukking av salgsordre.</span><span class="sxs-lookup"><span data-stu-id="aba49-163">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span>
7. <span data-ttu-id="aba49-164">Reserver beholdningen, og frigi den til lageret.</span><span class="sxs-lookup"><span data-stu-id="aba49-164">Reserve the inventory, and release it to the warehouse.</span></span> <span data-ttu-id="aba49-165">Det opprettes en arbeids-ID som har seks linjer.</span><span class="sxs-lookup"><span data-stu-id="aba49-165">A work ID that has six lines is created.</span></span> <span data-ttu-id="aba49-166">Linjene sorteres etter varenummer.</span><span class="sxs-lookup"><span data-stu-id="aba49-166">The lines are sorted by item number.</span></span>

### <a name="run-the-mobile-device-flow"></a><span data-ttu-id="aba49-167">Kjør flyten for mobilenhet</span><span class="sxs-lookup"><span data-stu-id="aba49-167">Run the mobile device flow</span></span>

1. <span data-ttu-id="aba49-168">På mobilenheten velger du menyen som inneholder det nye menyelementet for mobilenhet.</span><span class="sxs-lookup"><span data-stu-id="aba49-168">On the mobile device, select the menu that includes the new mobile device menu item.</span></span>
1. <span data-ttu-id="aba49-169">Velg menyelementet **Salgsplukking – gruppelinje**, og start plukkingen.</span><span class="sxs-lookup"><span data-stu-id="aba49-169">Select the **Sales Pick – Group line** menu item, and initiate the pick.</span></span>

    <span data-ttu-id="aba49-170">Når du har valgt menyen og angitt arbeids-ID, ser du plukktrinnet der alle plukklinjene for vare M9200 er gruppert.</span><span class="sxs-lookup"><span data-stu-id="aba49-170">After you select the menu and enter the work ID, you see the pick step where all pick lines for item M9200 are grouped.</span></span> <span data-ttu-id="aba49-171">Du får en instruksjon om å plukke 7 hver av vare M9200.</span><span class="sxs-lookup"><span data-stu-id="aba49-171">You receive an instruction to pick 7 each of item M9200.</span></span>

1. <span data-ttu-id="aba49-172">Bekreft plukktrinnet.</span><span class="sxs-lookup"><span data-stu-id="aba49-172">Confirm the pick step.</span></span> 
1. <span data-ttu-id="aba49-173">Gå til klientskjermen for arbeidet som pågår, og legg merke til at alle tre plukklinjer for vare M9200 ble lukket samtidig.</span><span class="sxs-lookup"><span data-stu-id="aba49-173">Go to the client screen of the work in process, and notice that all three pick lines for item M9200 were closed simultaneously.</span></span>

    <span data-ttu-id="aba49-174">Arbeidslinje 4 presenteres.</span><span class="sxs-lookup"><span data-stu-id="aba49-174">Work line 4 is presented.</span></span>

1. <span data-ttu-id="aba49-175">Bekreft plukktrinnet.</span><span class="sxs-lookup"><span data-stu-id="aba49-175">Confirm the pick step.</span></span>

    <span data-ttu-id="aba49-176">Det siste plukktrinnet på mobilenheten samler de to siste plukklinjene fra arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="aba49-176">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>

1. <span data-ttu-id="aba49-177">Fullfør plukktrinnet for 9 hver av vare M9202.</span><span class="sxs-lookup"><span data-stu-id="aba49-177">Complete the pick step for 9 each of item M9202.</span></span>
1. <span data-ttu-id="aba49-178">Bekreft plasseringstrinnet og eventuelle ekstra plukkings-/plasseringspar for å fullføre arbeidet.</span><span class="sxs-lookup"><span data-stu-id="aba49-178">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!NOTE]
> - <span data-ttu-id="aba49-179">Arbeidslinjer kan bare grupperes hvis de er i rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="aba49-179">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="aba49-180">Følgende funksjonalitet støttes ikke:</span><span class="sxs-lookup"><span data-stu-id="aba49-180">The following functionality isn't supported:</span></span>
>
>    - <span data-ttu-id="aba49-181">Faktisk vekt-varer.</span><span class="sxs-lookup"><span data-stu-id="aba49-181">Catch-weight items.</span></span> <span data-ttu-id="aba49-182">Hvis det er noen faktisk vekt-varer på arbeidet, får du en feilmelding før du begynner å plukke.</span><span class="sxs-lookup"><span data-stu-id="aba49-182">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>    - <span data-ttu-id="aba49-183">Stykkplukking.</span><span class="sxs-lookup"><span data-stu-id="aba49-183">Piece picking.</span></span>
>    - <span data-ttu-id="aba49-184">Arbeidslinjer som har uferdig etterfyllingsarbeid.</span><span class="sxs-lookup"><span data-stu-id="aba49-184">Work lines that have unfinished replenishment work.</span></span>
>    - <span data-ttu-id="aba49-185">Overplukking.</span><span class="sxs-lookup"><span data-stu-id="aba49-185">Over-picking.</span></span>
