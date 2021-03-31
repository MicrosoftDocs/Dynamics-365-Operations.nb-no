---
title: Returkostpris og returparti-ID
description: Du vil kanskje at kostnadene for de returnerte produktene skal være lik kostnaden for produktene på tidspunktet da du solgte produktene til kunden. Du kan gjøre dette ved å bruke **Returparti-ID**.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnInventTransIdLookup, ReturnItemNumLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b420c0716823f587ea3f349a5d654ace23d84f41
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219275"
---
# <a name="return-cost-price-and-return-lot-id"></a><span data-ttu-id="a9f6f-104">Returkostpris og returparti-ID</span><span class="sxs-lookup"><span data-stu-id="a9f6f-104">Return cost price and return lot ID</span></span>        

[!include [banner](../includes/banner.md)]



<span data-ttu-id="a9f6f-105">Kostnaden for produkter som er returnert til lager, beregnes ved å bruke den gjeldende kostnaden av produkter.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-105">The cost of products that are returned to inventory is calculated by using the current cost of the products.</span></span> <span data-ttu-id="a9f6f-106">Du vil imidlertid kanskje at kostnadene for de returnerte produktene skal være lik kostnaden for produktene på tidspunktet da du solgte produktene til kunden.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-106">However, you might want the cost of the returned products to equal the cost of the products at the time when you sold the products to the customer.</span></span> <span data-ttu-id="a9f6f-107">Du kan gjøre dette ved å bruke feltet **Returparti-ID** på hurtigfanen **Linjedetaljer** i **Salgsordre**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-107">You can do this by using the **Return lot ID** field on the **Line details** FastTab in the **Sales order** form.</span></span>

<span data-ttu-id="a9f6f-108">Tenk deg for eksempel følgende scenario.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-108">For example, consider the following scenario.</span></span> <span data-ttu-id="a9f6f-109">Du fakturerer en kunde.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-109">You invoice a customer.</span></span> <span data-ttu-id="a9f6f-110">Deretter returnerer kunden de leverte produktene til deg.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-110">Then, the customer returns the delivered products to you.</span></span> <span data-ttu-id="a9f6f-111">Du kan returnere produkter til lager.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-111">You return the products to stock.</span></span> <span data-ttu-id="a9f6f-112">I dette tilfellet når du krediterer kunden for de returnerte produktene, beregnes kostnaden for disse produktene ved å bruke gjeldende kostnader av produkter.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-112">In this case, when you credit the customer for the returned products, the cost of those products is calculated by using the current cost of the products.</span></span> <span data-ttu-id="a9f6f-113">Men hvis du bruker **Returparti-ID**-feltet, beregnes kostnaden for de returnerte produktene ved å bruke kostnaden på fakturaen til det opprinnelige salget til kunden.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-113">However, if you use the **Return lot ID** field, the cost of the returned products is calculated by using the cost on the invoice of the original sale to the customer.</span></span>

<span data-ttu-id="a9f6f-114">Hvis du vil bruke en annen kostnad enn gjeldende kostnad for returer fra en kunde, kan du bruke en av følgende metoder.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-114">To use a cost other than the current cost for returns from a customer, use one of the following methods.</span></span>

## <a name="method-1-manually-enter-the-return-cost-price"></a><span data-ttu-id="a9f6f-115">Metode 1: Angi den returnerte kostprisen manuelt</span><span class="sxs-lookup"><span data-stu-id="a9f6f-115">Method 1: Manually enter the return cost price</span></span>

<span data-ttu-id="a9f6f-116">Som standard når du legger varer til en returordre blir varene returnert til lager med den gjeldende kostprisen.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-116">By default, when you add items to a return order, the items are returned to inventory at the current cost price.</span></span> <span data-ttu-id="a9f6f-117">Bruk følgende fremgangsmåte for å angi en annen returkostpris.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-117">To specify a different return cost price, follow these steps.</span></span>

1.  <span data-ttu-id="a9f6f-118">Klikk på **Salg og markedsføring** \> **Vanlig** \> **Returordrer** \> **Alle returordrer**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-118">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="a9f6f-119">I **handlingsturen** i **Ny**-gruppen klikker du **Returordre**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-119">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="a9f6f-120">I skjemaet **Opprett returordre**, velg en kundekonto og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-120">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="a9f6f-121">I skjemaet **Returordre - autorisasjonsreturnr.: %1, %2**, velg en vare, og angi et negativt antall i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-121">In the **Return order - RMA number: %1, %2** form, select an item, and then enter a negative quantity in the **Quantity** field.</span></span>

5.  <span data-ttu-id="a9f6f-122">Klikk på hurtigfanen **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-122">Click the **Line details** FastTab.</span></span>

6.  <span data-ttu-id="a9f6f-123">Gå til fanen **Generelt**, og angi en verdi i feltet **Returkostpris**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-123">On the **General** tab, enter a value in the **Return cost price** field.</span></span> <span data-ttu-id="a9f6f-124">Denne verdien brukes når varene er returnert til lager.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-124">This value is used when the goods are returned to inventory.</span></span> <span data-ttu-id="a9f6f-125">Hvis du ikke angir en verdi, brukes den gjeldende kostprisen når varene er returnert til lager.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-125">If you do not enter a value, the current cost price is used when the goods are returned to inventory.</span></span>

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a><span data-ttu-id="a9f6f-126">Metode 2: Automatisk generere kostprisen, basert på kundefakturalinjen</span><span class="sxs-lookup"><span data-stu-id="a9f6f-126">Method 2: Automatically generate the cost price based on the customer invoice line</span></span>

<span data-ttu-id="a9f6f-127">Dette er den foretrukne metoden for å opprette returlinjer.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-127">This is the preferred method to use to create return lines.</span></span> <span data-ttu-id="a9f6f-128">Hvis du vil bruke kostnaden for produktene samtidig som da du solgte produktene til kunden, oppretter du en returordre og angir en salgslinje som skal returneres.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-128">To use the cost of the products at the time when you sold the products to the customer, create a return order and specify a sales line to return.</span></span>

1.  <span data-ttu-id="a9f6f-129">Klikk på **Salg og markedsføring** \> **Vanlig** \> **Returordrer** \> **Alle returordrer**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-129">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="a9f6f-130">I **handlingsturen** i **Ny**-gruppen klikker du **Returordre**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-130">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="a9f6f-131">I skjemaet **Opprett returordre**, velg en kundekonto og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-131">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="a9f6f-132">I skjemaet **Returordre - autorisasjonsreturnr.: %1, %2**, i **Handlingsrute**, klikk **Søk etter salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-132">In the **Return order - RMA number: %1, %2** form, on the **Action Pane**, click **Find sales order**.</span></span>

5.  <span data-ttu-id="a9f6f-133">I skjemaet **Søk etter salgsordre** velger du fakturalinjen som skal returneres, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-133">In the **Find sales order** form, select the invoice line to return, and then click **OK**.</span></span>
    
    <span data-ttu-id="a9f6f-134">På hurtigfanen **Linjedetaljer** på fanen **Generelt** viser feltet **Returparti-ID** verdien fra den opprinnelige salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-134">On the **Line details** FastTab, on the **General** tab, the **Return lot ID** field displays the value from the original sales line.</span></span> <span data-ttu-id="a9f6f-135">I tillegg viser feltet **Returkostpris** kostverdien fra den opprinnelige salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-135">Additionally, the **Return cost price** field displays the cost value from the original sales line.</span></span>

## <a name="cost-calculation-example"></a><span data-ttu-id="a9f6f-136">Eksempel på kostnadsberegning</span><span class="sxs-lookup"><span data-stu-id="a9f6f-136">Cost calculation example</span></span>

<span data-ttu-id="a9f6f-137">Når du bruker feltet **Returparti-ID** i en returordrelinje for å angi den returnerte kostprisen, brukes kostnaden på returordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-137">When you use the **Return lot ID** field on a return order line to specify the return cost price, the cost on the return order line is used.</span></span> <span data-ttu-id="a9f6f-138">Hvis du kjører funksjonen for lagerlukking eller omberegning, justeres kostnaden på den opprinnelige salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-138">If you run the inventory close or recalculation functionality, the cost is adjusted on the original sales line.</span></span> <span data-ttu-id="a9f6f-139">Kostnaden på returordrelinjen justeres automatisk for å gjenspeile den samme kostnaden per stykk.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-139">The cost on the return order line is automatically adjusted to reflect the same cost per piece.</span></span>

1.  <span data-ttu-id="a9f6f-140">Opprett og frigi et produkt som heter Test.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-140">Create and release a product that is named Test.</span></span> <span data-ttu-id="a9f6f-141">I skjemaet **Detaljer om frigitt produkt** angir du følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="a9f6f-141">In the **Released product details** form, specify the following information:</span></span>
    
    1.  <span data-ttu-id="a9f6f-142">På hurtigfanen **Styr kostnader** i feltet **Varegruppe** velger du **Deler**-gruppen.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-142">On the **Manage costs** FastTab, in the **Item group** field, select the **Parts** group.</span></span>
    
    2.  <span data-ttu-id="a9f6f-143">På hurtigfanen **Generelt** i feltet **Varemodellgruppe** velger du **DEF**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-143">On the **General** FastTab, in the **Item model group** field, select **DEF**.</span></span>
    
    3.  <span data-ttu-id="a9f6f-144">På hurtigfanen **Kjøp** i **Pris**-feltet skriver du inn 10,00 som kostprisen for varen.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-144">On the **Purchase** FastTab, in the **Price** field, type 10.00 as the cost price of the item.</span></span>
    
    4.  <span data-ttu-id="a9f6f-145">I **handlingsruten** klikker du på **Dimensjonsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-145">On the **Action Pane**, click **Dimension groups**.</span></span> <span data-ttu-id="a9f6f-146">I feltet **Lagringsdimensjonsgruppe** velger du **Bare område og lager**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-146">In the **Storage dimension group** field, select **Site and Warehouse only**.</span></span> <span data-ttu-id="a9f6f-147">I feltet **Sporingsdimensjonsgruppe** velger du **Ingen aktive sporingsdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-147">In the **Tracking dimension group** field, select **No active tracking dimensions**.</span></span>

2.  <span data-ttu-id="a9f6f-148">Opprett en bestilling for 10 stykker av varen Test til 6,00 per enhet, og poster deretter en faktura for bestillingen.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-148">Create a purchase order for 10 pieces of the Test item at 6.00 per piece, and then post an invoice for the purchase order.</span></span>
    
    <span data-ttu-id="a9f6f-149">Opprett en ny bestilling for 10 stykker av varen Test til 8,00 per enhet, og poster deretter en faktura for bestillingen.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-149">Create a second purchase order for 10 pieces of the Test item at 8.00 per piece, and then post an invoice for the purchase order.</span></span>

3.  <span data-ttu-id="a9f6f-150">Poster en faktura for en salgsordre for å selge fem stykker av varen Test.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-150">Post an invoice for a sales order to sell five pieces of the Test item.</span></span>
    
    <span data-ttu-id="a9f6f-151">I dette tilfellet beregnes salgsordrelinjen til 35,00 (5 enheter \* 7,00 i gjennomsnittlig kostnad per enhet).</span><span class="sxs-lookup"><span data-stu-id="a9f6f-151">In this case, the sales order line is costed at 35.00 (5 pieces \* 7.00 average cost per piece).</span></span>

4.  <span data-ttu-id="a9f6f-152">Opprett en returordre for kunden.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-152">Create a return order for the customer.</span></span> <span data-ttu-id="a9f6f-153">I skjemaet **Søk etter salgsordre** velger du fakturalinjen, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-153">In the **Find sales order** form, select the invoice line, and then click **OK**.</span></span>

5.  <span data-ttu-id="a9f6f-154">I skjemaet **Returordre - autorisasjonsreturnr.: %1, %2** må du kontrollere at en returordre blir generert for å returnere varen Test.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-154">In the **Return order - RMA number: %1, %2** form, verify that a return order is generated to return the Test item.</span></span> <span data-ttu-id="a9f6f-155">Antall for returordren er satt til -5,00.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-155">The quantity of the return order is set to -5.00.</span></span>
    
    <span data-ttu-id="a9f6f-156">Feltet **Returparti-ID** viser en parti-ID.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-156">The **Return lot ID** field displays a lot ID.</span></span> <span data-ttu-id="a9f6f-157">Denne parti-ID-en hentes fra den opprinnelige salgsordren til varen som ble solgt til kunden.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-157">This lot ID is taken from the original sales order of the item that was sold to the customer.</span></span> <span data-ttu-id="a9f6f-158">Feltet **Returkostpris** viser kostprisen fra den opprinnelige salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-158">The **Return cost price** field displays the cost price from the original sales line.</span></span>

6.  <span data-ttu-id="a9f6f-159">Registrer mottaket av de returnerte varene.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-159">Register the receipt of the returned items.</span></span>

7.  <span data-ttu-id="a9f6f-160">Poster en følgeseddel for de returnerte varene.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-160">Post a packing slip for the returned items.</span></span>

8.  <span data-ttu-id="a9f6f-161">Poster en faktura for returordren.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-161">Post an invoice for the return order.</span></span> <span data-ttu-id="a9f6f-162">På listesiden **Alle salgsordrer** velger du en salgsordre der **Returordre** er ordretypen.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-162">On the **All sales orders** list page, select a sales order for which **Returned order** is the order type.</span></span>

9.  <span data-ttu-id="a9f6f-163">Åpne skjemaet **Lagertransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-163">Open the **Inventory transactions** form.</span></span> <span data-ttu-id="a9f6f-164">Kontroller at returen er kalkulert til 7,00 per enhet ved hjelp av verdien i feltet **Returkostpris**, for en total på 35,00 i **Kostnadsbeløp**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-164">Verify that the return is costed at 7.00 per piece by using the value in the **Return cost price** field, for a total of 35.00 in the **Cost amount** field.</span></span> <span data-ttu-id="a9f6f-165">Du kan åpne skjemaet **Lagertransaksjoner** fra skjemaet **Returordre - autorisasjonsreturnr.: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-165">You can open the **Inventory transactions** form from the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="a9f6f-166">I **Linjer**-rutenettet klikker du **Beholdning** \> **Transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-166">In the **Lines** grid, click **Inventory** \> **Transactions**.</span></span>

10. <span data-ttu-id="a9f6f-167">I lagerstyring kan du bruke skjemaet **Lukking og justering** til å kjøre prosedyren **3. Lukk**.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-167">In Inventory and warehouse management, use the **Closing and adjustment** form to run the **3. Close** procedure.</span></span>
    
    <span data-ttu-id="a9f6f-168">Denne handlingen justerer kostnaden på den opprinnelige salgslinjen som ble kalkulert til -35,00 (5 enheter \* 7,00) til -30,00 (5 enheter \* 6,00).</span><span class="sxs-lookup"><span data-stu-id="a9f6f-168">This action adjusts the cost on the original sales line that was costed at -35.00 (5 pieces \* 7.00) to -30.00 (5 pieces \* 6.00).</span></span> <span data-ttu-id="a9f6f-169">Dette er fordi lagermodellgruppen bruker først inn, først ut (FIFO), og 6,00 per enhet er FIFO-kostnaden fra den første bestillingen.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-169">This is because the inventory model group uses First in, First out (FIFO), and 6.00 per piece is the FIFO cost from the first purchase order.</span></span> <span data-ttu-id="a9f6f-170">I tillegg justerer handlingen kostnaden på retursalgslinjen, slik at den samsvarer med kostnaden per enhet i den opprinnelige salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-170">Additionally, the action adjusts the cost on the return sales line to match the cost per piece on the original sales line.</span></span> <span data-ttu-id="a9f6f-171">Derfor justeres kostnaden for returlinjen fra 35,00 til 30,00.</span><span class="sxs-lookup"><span data-stu-id="a9f6f-171">Therefore, the cost of the return line is adjusted from 35.00 to 30.00.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]