---
title: Definere dekningsregler for varer
description: Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 02aa3b2b7924cdf6317225bfce23f182aa390b8c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565666"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="64eac-103">Definere dekningsregler for varer</span><span class="sxs-lookup"><span data-stu-id="64eac-103">Define coverage rules for items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="64eac-104">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="64eac-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="64eac-105">Denne prosedyren viser hvordan du oppretter dekningsregler og overstyrer dekningsinnstillinger for en bestemt vare.</span><span class="sxs-lookup"><span data-stu-id="64eac-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="64eac-106">Den viser også hvordan du kan angi standard lagerinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="64eac-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="64eac-107">Opprette en dekningsgruppe</span><span class="sxs-lookup"><span data-stu-id="64eac-107">Create a coverage group</span></span>
1. <span data-ttu-id="64eac-108">Gå til Dekningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="64eac-108">Go to Coverage groups.</span></span>
2. <span data-ttu-id="64eac-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="64eac-109">Click New.</span></span>
3. <span data-ttu-id="64eac-110">Skriv inn en verdi i Dekningsgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="64eac-110">In the Coverage group field, type a value.</span></span>
4. <span data-ttu-id="64eac-111">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="64eac-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="64eac-112">Skriv inn en verdi i feltet Kalender.</span><span class="sxs-lookup"><span data-stu-id="64eac-112">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="64eac-113">Velg kalenderen som hovedplanlegging bruker til å opprette forslag for etterfylling for varer i denne gruppen.</span><span class="sxs-lookup"><span data-stu-id="64eac-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="64eac-114">I Dekningskode-feltet velger du et alternativ.</span><span class="sxs-lookup"><span data-stu-id="64eac-114">In the Coverage code field, select an option.</span></span>
    * <span data-ttu-id="64eac-115">Velg Krav for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="64eac-115">Select Requirement for this procedure.</span></span>  
7. <span data-ttu-id="64eac-116">Angi 90 i feltet Dekningshorisont (dager).</span><span class="sxs-lookup"><span data-stu-id="64eac-116">In the Coverage time fence (days) field, enter '90'.</span></span>
    * <span data-ttu-id="64eac-117">For varer i denne gruppen oppretter hovedplanleggingen etterfyllingsforslag for opptil 90 dager i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="64eac-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="64eac-118">Angi 1 i Negative dager-feltet.</span><span class="sxs-lookup"><span data-stu-id="64eac-118">In the Negative days field, enter '1'.</span></span>
9. <span data-ttu-id="64eac-119">Angi 1 i Positive dager-feltet.</span><span class="sxs-lookup"><span data-stu-id="64eac-119">In the Positive days field, enter '1'.</span></span>
10. <span data-ttu-id="64eac-120">Vis eller skjul delen Annet.</span><span class="sxs-lookup"><span data-stu-id="64eac-120">Expand or collapse the Other section.</span></span>
11. <span data-ttu-id="64eac-121">Angi 1 i feltet Påslag dager lagt til i behovsdato.</span><span class="sxs-lookup"><span data-stu-id="64eac-121">In the Receipt margin added to requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="64eac-122">Hvis for eksempel mottaksmarginen er satt til 1 dag, og en bestillingslinje blir planlagt for mottak den 15. mai, beregner hovedplanleggingen den justerte mottaksdatoen som 16. mai.</span><span class="sxs-lookup"><span data-stu-id="64eac-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="64eac-123">Angi 1 i feltet Sikkerhetsdager trukket fra behovsdato.</span><span class="sxs-lookup"><span data-stu-id="64eac-123">In the Issue margin deducted from requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="64eac-124">Hvis for eksempel mottaksmarginen er satt til 1 dag, og en bestillingslinje blir planlagt for mottak den 15. mai, beregner hovedplanleggingen den justerte mottaksdatoen som 14. mai.</span><span class="sxs-lookup"><span data-stu-id="64eac-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="64eac-125">Angi 1 i feltet Respittid, gjenbestilling lagt til vareleveringstiden.</span><span class="sxs-lookup"><span data-stu-id="64eac-125">In the Reorder margin added to item lead time field, enter '1'.</span></span>
14. <span data-ttu-id="64eac-126">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="64eac-126">Click Save.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="64eac-127">Opprett et nytt produkt</span><span class="sxs-lookup"><span data-stu-id="64eac-127">Create a new product</span></span>
1. <span data-ttu-id="64eac-128">Gå til Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="64eac-128">Go to Released products.</span></span>
2. <span data-ttu-id="64eac-129">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="64eac-129">Click New.</span></span>
3. <span data-ttu-id="64eac-130">Skriv inn en verdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="64eac-130">In the Product number field, type a value.</span></span>
4. <span data-ttu-id="64eac-131">Skriv inn en verdi i feltet Produktnavn.</span><span class="sxs-lookup"><span data-stu-id="64eac-131">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="64eac-132">Klikk rullegardinknappen i feltet Varemodellgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="64eac-132">In the Item model group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="64eac-133">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="64eac-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="64eac-134">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="64eac-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="64eac-135">Klikk rullegardinknappen i feltet Varegruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="64eac-135">In the Item group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="64eac-136">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="64eac-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="64eac-137">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="64eac-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="64eac-138">Klikk rullegardinknappen i Lagringsdimensjonsgruppe-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="64eac-138">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="64eac-139">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="64eac-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="64eac-140">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="64eac-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="64eac-141">Klikk rullegardinknappen i Sporingsdimensjonsgruppe-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="64eac-141">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="64eac-142">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="64eac-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="64eac-143">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="64eac-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="64eac-144">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="64eac-144">Click OK.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="64eac-145">Konfigurere standard ordreinnstillinger</span><span class="sxs-lookup"><span data-stu-id="64eac-145">Setup default order settings</span></span>
1. <span data-ttu-id="64eac-146">Klikk Plan i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="64eac-146">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="64eac-147">Klikk Standard ordreinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="64eac-147">Click Default order settings.</span></span>
3. <span data-ttu-id="64eac-148">Skriv inn området som brukes som standard ved opprettelse av bestillinger, i feltet Innkjøpssite.</span><span class="sxs-lookup"><span data-stu-id="64eac-148">In the Purchase site field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="64eac-149">Skriv inn området der varen lagres, i feltet Lagersite.</span><span class="sxs-lookup"><span data-stu-id="64eac-149">In the Inventory site field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="64eac-150">Vis eller skjul delen Beholdning.</span><span class="sxs-lookup"><span data-stu-id="64eac-150">Expand or collapse the Inventory section.</span></span>
6. <span data-ttu-id="64eac-151">Angi Flere til 10.</span><span class="sxs-lookup"><span data-stu-id="64eac-151">Set Multiple to '10'.</span></span>
7. <span data-ttu-id="64eac-152">Angi Min.</span><span class="sxs-lookup"><span data-stu-id="64eac-152">Set Min.</span></span> <span data-ttu-id="64eac-153">ordreantall til 10.</span><span class="sxs-lookup"><span data-stu-id="64eac-153">order quantity to '10'.</span></span>
8. <span data-ttu-id="64eac-154">Angi Maks.</span><span class="sxs-lookup"><span data-stu-id="64eac-154">Set Max.</span></span> <span data-ttu-id="64eac-155">ordreantall til 100.</span><span class="sxs-lookup"><span data-stu-id="64eac-155">order quantity to '100'.</span></span>
9. <span data-ttu-id="64eac-156">Angi Standard ordreantall til 10.</span><span class="sxs-lookup"><span data-stu-id="64eac-156">Set Standard order quantity to '10'.</span></span>
10. <span data-ttu-id="64eac-157">Angi et tall i feltet Leveringstid for innkjøp.</span><span class="sxs-lookup"><span data-stu-id="64eac-157">In the Purchase lead time field, enter a number.</span></span>
11. <span data-ttu-id="64eac-158">Merk av eller fjern merket i avmerkingsboksen Virkedager.</span><span class="sxs-lookup"><span data-stu-id="64eac-158">Select or clear the Working days check box.</span></span>
12. <span data-ttu-id="64eac-159">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="64eac-159">Click Save.</span></span>
13. <span data-ttu-id="64eac-160">Velg Bestilling i feltet Standard ordretype.</span><span class="sxs-lookup"><span data-stu-id="64eac-160">In the Default order type field select 'Purchase order'.</span></span>
14. <span data-ttu-id="64eac-161">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="64eac-161">Click Save.</span></span>
15. <span data-ttu-id="64eac-162">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="64eac-162">Close the page.</span></span>
    * <span data-ttu-id="64eac-163">Lukk siden Standard ordreinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="64eac-163">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="64eac-164">Legge til en vare i en dekningsgruppe</span><span class="sxs-lookup"><span data-stu-id="64eac-164">Add an item to a coverage group</span></span>
1. <span data-ttu-id="64eac-165">Vis eller skjul delen Plan.</span><span class="sxs-lookup"><span data-stu-id="64eac-165">Expand or collapse the Plan section.</span></span>
2. <span data-ttu-id="64eac-166">Klikk rullegardinknappen i Dekningsgruppe-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="64eac-166">In the Coverage group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="64eac-167">I listen finner du dekningsgruppen du har opprettet.</span><span class="sxs-lookup"><span data-stu-id="64eac-167">In the list, find the Coverage group you have created.</span></span>
4. <span data-ttu-id="64eac-168">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="64eac-168">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="64eac-169">Opprette varedekningsregler</span><span class="sxs-lookup"><span data-stu-id="64eac-169">Create item coverage rules</span></span>
1. <span data-ttu-id="64eac-170">Klikk Plan i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="64eac-170">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="64eac-171">Klikk Varedekning.</span><span class="sxs-lookup"><span data-stu-id="64eac-171">Click Item coverage.</span></span>
3. <span data-ttu-id="64eac-172">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="64eac-172">Click New.</span></span>
4. <span data-ttu-id="64eac-173">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="64eac-173">Click the General tab.</span></span>
5. <span data-ttu-id="64eac-174">Merk av i boksen i overskriften til Overstyr dekningsgruppeinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="64eac-174">Check the box on the header of Override coverage group settings.</span></span>
6. <span data-ttu-id="64eac-175">Angi 60 i feltet Dekningshorisont (dager).</span><span class="sxs-lookup"><span data-stu-id="64eac-175">In the Coverage time fence (days) field, enter '60'.</span></span>
    * <span data-ttu-id="64eac-176">Selv om varene i dekningsgruppen Krav er planlagt 90 dager frem i tid, blir elementet planlagt 60 dager frem i tid.</span><span class="sxs-lookup"><span data-stu-id="64eac-176">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="64eac-177">Angi 2 i Negative dager-feltet.</span><span class="sxs-lookup"><span data-stu-id="64eac-177">In the Negative days field, enter '2'.</span></span>
8. <span data-ttu-id="64eac-178">Angi 2 i Positive dager-feltet.</span><span class="sxs-lookup"><span data-stu-id="64eac-178">In the Positive days field, enter '2'.</span></span>
9. <span data-ttu-id="64eac-179">Klikk kategorien Leveringstid.</span><span class="sxs-lookup"><span data-stu-id="64eac-179">Click the Lead time tab.</span></span>
10. <span data-ttu-id="64eac-180">Merk av i boksen i overskriften for Innkjøp.</span><span class="sxs-lookup"><span data-stu-id="64eac-180">Check the box on the header of Purchase.</span></span>
11. <span data-ttu-id="64eac-181">Angi 5 i feltet Innkjøpstid.</span><span class="sxs-lookup"><span data-stu-id="64eac-181">In the Purchase time field, enter '5'.</span></span>
12. <span data-ttu-id="64eac-182">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="64eac-182">Click Save.</span></span>

