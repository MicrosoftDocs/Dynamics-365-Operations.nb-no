---
title: Definere dekningsregler for varer
description: Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11d92185bdbcf7aa1a668b6d2aa311805e42293c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3974986"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="25695-103">Definere dekningsregler for varer</span><span class="sxs-lookup"><span data-stu-id="25695-103">Define coverage rules for items</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25695-104">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="25695-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="25695-105">Denne prosedyren viser hvordan du oppretter dekningsregler og overstyrer dekningsinnstillinger for en bestemt vare.</span><span class="sxs-lookup"><span data-stu-id="25695-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="25695-106">Den viser også hvordan du kan angi standard lagerinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="25695-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="25695-107">Opprette en dekningsgruppe</span><span class="sxs-lookup"><span data-stu-id="25695-107">Create a coverage group</span></span>
1. <span data-ttu-id="25695-108">Gå til **Navigasjonsrute > Moduler > Hovedplanlegging > Oppsett > Dekningsgrupper** .</span><span class="sxs-lookup"><span data-stu-id="25695-108">Go to **Navigation pane > Modules > Master planning > Setup > Coverage groups** .</span></span>
2. <span data-ttu-id="25695-109">Klikk på **Ny** .</span><span class="sxs-lookup"><span data-stu-id="25695-109">Click **New** .</span></span>
3. <span data-ttu-id="25695-110">Skriv inn en verdi i **Dekningsgruppe** -feltet.</span><span class="sxs-lookup"><span data-stu-id="25695-110">In the **Coverage group** field, type a value.</span></span>
4. <span data-ttu-id="25695-111">Skriv inn en verdi i **Navn** -feltet.</span><span class="sxs-lookup"><span data-stu-id="25695-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="25695-112">Skriv inn en verdi i feltet **Kalender** .</span><span class="sxs-lookup"><span data-stu-id="25695-112">In the **Calendar** field, type a value.</span></span> <span data-ttu-id="25695-113">Velg kalenderen som hovedplanlegging bruker til å opprette forslag for etterfylling for varer i denne gruppen.</span><span class="sxs-lookup"><span data-stu-id="25695-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="25695-114">I **Dekningskode** -feltet velger du et alternativ.</span><span class="sxs-lookup"><span data-stu-id="25695-114">In the **Coverage code** field, select an option.</span></span> <span data-ttu-id="25695-115">Velg "Krav" for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="25695-115">Select 'Requirement' for this procedure.</span></span>  
7. <span data-ttu-id="25695-116">Angi 90 i feltet **Dekningshorisont (dager)** .</span><span class="sxs-lookup"><span data-stu-id="25695-116">In the **Coverage time fence (days) field** , enter '90'.</span></span> <span data-ttu-id="25695-117">For varer i denne gruppen oppretter hovedplanleggingen etterfyllingsforslag for opptil 90 dager i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="25695-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="25695-118">Angi 1 i **Negative dager** -feltet.</span><span class="sxs-lookup"><span data-stu-id="25695-118">In the **Negative days** field, enter '1'.</span></span>
9. <span data-ttu-id="25695-119">Angi 1 i **Positive dager** -feltet.</span><span class="sxs-lookup"><span data-stu-id="25695-119">In the **Positive days** field, enter '1'.</span></span>
10. <span data-ttu-id="25695-120">Vis eller skjul delen **Annet** .</span><span class="sxs-lookup"><span data-stu-id="25695-120">Expand or collapse the **Other** section.</span></span>
11. <span data-ttu-id="25695-121">Under delen **Sikkerhetsmarginer i dager** i feltet **RPåslag dager lagt til i behovsdato** angir du 1.</span><span class="sxs-lookup"><span data-stu-id="25695-121">Under the **Safety margins in days** section, in the **Receipt margin added to requirement date** field, enter '1'.</span></span> <span data-ttu-id="25695-122">Hvis for eksempel mottaksmarginen er satt til 1 dag, og en bestillingslinje blir planlagt for mottak den 15. mai, beregner hovedplanleggingen den justerte mottaksdatoen som 16. mai.</span><span class="sxs-lookup"><span data-stu-id="25695-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="25695-123">Angi 1 i feltet **Sikkerhetsdager trukket fra behovsdato** .</span><span class="sxs-lookup"><span data-stu-id="25695-123">In the **Issue margin deducted from requirement date** field, enter '1'.</span></span> <span data-ttu-id="25695-124">Hvis for eksempel mottaksmarginen er satt til 1 dag, og en bestillingslinje blir planlagt for mottak den 15. mai, beregner hovedplanleggingen den justerte mottaksdatoen som 14. mai.</span><span class="sxs-lookup"><span data-stu-id="25695-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="25695-125">Angi 1 i feltet **Respittid, gjenbestilling lagt til vareleveringstiden** .</span><span class="sxs-lookup"><span data-stu-id="25695-125">In the **Reorder margin added to item lead time** field, enter '1'.</span></span>
14. <span data-ttu-id="25695-126">Klikk **Lagre** .</span><span class="sxs-lookup"><span data-stu-id="25695-126">Click **Save** .</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="25695-127">Opprette et nytt produkt</span><span class="sxs-lookup"><span data-stu-id="25695-127">Create a new product</span></span>
1. <span data-ttu-id="25695-128">Gå til **Navigasjonsrute > Moduler > Behandling av produktinformasjon > Produkter > Frigitte produkter** .</span><span class="sxs-lookup"><span data-stu-id="25695-128">Go to **Navigation pane > Modules > Product information management > Products > Released products** .</span></span>
2. <span data-ttu-id="25695-129">Klikk på **Ny** .</span><span class="sxs-lookup"><span data-stu-id="25695-129">Click **New** .</span></span>
3. <span data-ttu-id="25695-130">Skriv inn en verdi i feltet **Produktnummer** .</span><span class="sxs-lookup"><span data-stu-id="25695-130">In the **Product number** field, type a value.</span></span>
4. <span data-ttu-id="25695-131">Skriv inn en verdi i feltet **Produktnavn** .</span><span class="sxs-lookup"><span data-stu-id="25695-131">In the **Product name** field, type a value.</span></span>
5. <span data-ttu-id="25695-132">Klikk rullegardinknappen i feltet **Varemodellgruppe** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="25695-132">In the **Item model group** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="25695-133">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="25695-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="25695-134">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="25695-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="25695-135">Klikk rullegardinknappen i feltet **Varegruppe** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="25695-135">In the **Item group** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="25695-136">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="25695-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="25695-137">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="25695-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="25695-138">Klikk rullegardinknappen i **Lagringsdimensjonsgruppe** -feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="25695-138">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="25695-139">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="25695-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="25695-140">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="25695-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="25695-141">Klikk rullegardinknappen i **Sporingsdimensjonsgruppe** -feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="25695-141">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="25695-142">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="25695-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="25695-143">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="25695-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="25695-144">Klikk **OK** .</span><span class="sxs-lookup"><span data-stu-id="25695-144">Click **OK** .</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="25695-145">Konfigurere standard ordreinnstillinger</span><span class="sxs-lookup"><span data-stu-id="25695-145">Setup default order settings</span></span>
1. <span data-ttu-id="25695-146">Klikk **Plan** i **handlingsruten** .</span><span class="sxs-lookup"><span data-stu-id="25695-146">On the **Action Pane** , click **Plan** .</span></span>
2. <span data-ttu-id="25695-147">Under **Ordreinnstillinger** klikker du **Standard ordreinnstillinger** .</span><span class="sxs-lookup"><span data-stu-id="25695-147">Under **Order settings** , click **Default order settings** .</span></span>
3. <span data-ttu-id="25695-148">Under **Bestilling** , i feltet **Standardområde** skriver du inn området som brukes som standard når bestillinger opprettes.</span><span class="sxs-lookup"><span data-stu-id="25695-148">Under **Purchase order** , in the **Default site** field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="25695-149">Skriv inn området der varen lagres, i feltet **Standardlager** .</span><span class="sxs-lookup"><span data-stu-id="25695-149">In the **Default warehouse** field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="25695-150">Vis eller skjul delen **Beholdning** .</span><span class="sxs-lookup"><span data-stu-id="25695-150">Expand or collapse the **Inventory** section.</span></span>
6. <span data-ttu-id="25695-151">I feltet **Multippel** skriver du inn 10.</span><span class="sxs-lookup"><span data-stu-id="25695-151">In the **Multiple** field, type '10'.</span></span>
7. <span data-ttu-id="25695-152">I feltet **Minimumsordre** skriver du inn 10.</span><span class="sxs-lookup"><span data-stu-id="25695-152">In the **Min. order quantity** field, type '10'.</span></span>
8. <span data-ttu-id="25695-153">I feltet **Maks. ordreantall** skriver du inn 100.</span><span class="sxs-lookup"><span data-stu-id="25695-153">In the **Max. order quantity** field, type '100'.</span></span>
9. <span data-ttu-id="25695-154">I feltet **Standard ordreantall** skriver du inn 10.</span><span class="sxs-lookup"><span data-stu-id="25695-154">In the **Standard order quantity** , type '10'.</span></span>
10. <span data-ttu-id="25695-155">Angi et tall i feltet **Leveringstid for innkjøp** .</span><span class="sxs-lookup"><span data-stu-id="25695-155">In the **Purchase lead time** field, enter a number.</span></span>
11. <span data-ttu-id="25695-156">Merk av eller fjern merket i avmerkingsboksen **Virkedager** .</span><span class="sxs-lookup"><span data-stu-id="25695-156">Select or clear the **Working days** check box.</span></span>
12. <span data-ttu-id="25695-157">Klikk **Lagre** .</span><span class="sxs-lookup"><span data-stu-id="25695-157">Click **Save** .</span></span>
13. <span data-ttu-id="25695-158">Velg Bestilling i feltet **Standard ordretype** .</span><span class="sxs-lookup"><span data-stu-id="25695-158">In the **Default order type** field select 'Purchase order'.</span></span>
14. <span data-ttu-id="25695-159">Klikk **Lagre** .</span><span class="sxs-lookup"><span data-stu-id="25695-159">Click **Save** .</span></span>
15. <span data-ttu-id="25695-160">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="25695-160">Close the page.</span></span> <span data-ttu-id="25695-161">Lukk siden Standard ordreinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="25695-161">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="25695-162">Legge til en vare i en dekningsgruppe</span><span class="sxs-lookup"><span data-stu-id="25695-162">Add an item to a coverage group</span></span>
1. <span data-ttu-id="25695-163">Vis eller skjul delen **Plan** .</span><span class="sxs-lookup"><span data-stu-id="25695-163">Expand or collapse the **Plan** section.</span></span>
2. <span data-ttu-id="25695-164">Klikk rullegardinknappen i **Dekningsgruppe** -feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="25695-164">In the **Coverage group** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="25695-165">I listen finner du **dekningsgruppen** du har opprettet.</span><span class="sxs-lookup"><span data-stu-id="25695-165">In the list, find the **Coverage group** you have created.</span></span>
4. <span data-ttu-id="25695-166">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="25695-166">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="25695-167">Opprette varedekningsregler</span><span class="sxs-lookup"><span data-stu-id="25695-167">Create item coverage rules</span></span>
1. <span data-ttu-id="25695-168">Klikk **Plan** i **handlingsruten** .</span><span class="sxs-lookup"><span data-stu-id="25695-168">On the **Action Pane** , click **Plan** .</span></span>
2. <span data-ttu-id="25695-169">Under **Dekning** klikker du **Varedekning** .</span><span class="sxs-lookup"><span data-stu-id="25695-169">Under **Coverage** , click **Item coverage** .</span></span>
3. <span data-ttu-id="25695-170">Klikk på **Ny** .</span><span class="sxs-lookup"><span data-stu-id="25695-170">Click **New** .</span></span>
4. <span data-ttu-id="25695-171">Klikk kategorien **Generelt** .</span><span class="sxs-lookup"><span data-stu-id="25695-171">Click the **General** tab.</span></span>
5. <span data-ttu-id="25695-172">Merk av i boksen i overskriften til **Overstyr dekningsgruppeinnstillinger** .</span><span class="sxs-lookup"><span data-stu-id="25695-172">Check the box on the header of **Override coverage group** settings.</span></span>
6. <span data-ttu-id="25695-173">Angi 60 i feltet **Dekningshorisont (dager)** .</span><span class="sxs-lookup"><span data-stu-id="25695-173">In the **Coverage time fence (days)** field, enter '60'.</span></span> <span data-ttu-id="25695-174">Selv om varene i dekningsgruppen Krav er planlagt 90 dager frem i tid, blir elementet planlagt 60 dager frem i tid.</span><span class="sxs-lookup"><span data-stu-id="25695-174">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="25695-175">Angi 2 i **Negative dager** -feltet.</span><span class="sxs-lookup"><span data-stu-id="25695-175">In the **Negative days** field, enter '2'.</span></span>
8. <span data-ttu-id="25695-176">Angi 2 i **Positive dager** -feltet.</span><span class="sxs-lookup"><span data-stu-id="25695-176">In the **Positive days** field, enter '2'.</span></span>
9. <span data-ttu-id="25695-177">Klikk kategorien **Leveringstid** .</span><span class="sxs-lookup"><span data-stu-id="25695-177">Click the **Lead time** tab.</span></span>
10. <span data-ttu-id="25695-178">Merk av i boksen i overskriften for **Innkjøp** .</span><span class="sxs-lookup"><span data-stu-id="25695-178">Check the box on the header of **Purchase** .</span></span>
11. <span data-ttu-id="25695-179">Angi 5 i feltet **Innkjøpstid** .</span><span class="sxs-lookup"><span data-stu-id="25695-179">In the **Purchase time** field, enter '5'.</span></span>
12. <span data-ttu-id="25695-180">Klikk **Lagre** .</span><span class="sxs-lookup"><span data-stu-id="25695-180">Click **Save** .</span></span>

