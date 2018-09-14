--- 
title: Opprette en bestilling med en leveringsplan
description: "Denne fremgangsmåten viser hvordan du oppretter en leveringsplan for en bestilling."
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchDeliverySchedule, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 0a9b7b233339d41605e1b115bd14a18b706ef226
ms.contentlocale: nb-no
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a><span data-ttu-id="a127c-103">Opprette en bestilling med en leveringsplan</span><span class="sxs-lookup"><span data-stu-id="a127c-103">Create a purchase order with a delivery schedule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a127c-104">Denne fremgangsmåten viser hvordan du oppretter en leveringsplan for en bestilling.</span><span class="sxs-lookup"><span data-stu-id="a127c-104">This procedure demonstrates how to create a delivery schedule for a purchase order.</span></span> <span data-ttu-id="a127c-105">En leveringsplan brukes når et antall i en ordre eller en journal blir bedt om å bli levert i flere leveranser.</span><span class="sxs-lookup"><span data-stu-id="a127c-105">A delivery schedule is used when a quantity on an order or a journal is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="a127c-106">Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="a127c-106">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="a127c-107">Dette gjøres vanligvis av en innkjøpsagent.</span><span class="sxs-lookup"><span data-stu-id="a127c-107">This procedure would typically be done by a purchasing agent.</span></span>


## <a name="create-a-delivery-schedule"></a><span data-ttu-id="a127c-108">Opprette en leveringsplan</span><span class="sxs-lookup"><span data-stu-id="a127c-108">Create a delivery schedule</span></span>
1. <span data-ttu-id="a127c-109">Gå til Innkjøp og leverandører > Bestillinger > Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="a127c-109">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="a127c-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="a127c-110">Click New.</span></span>
3. <span data-ttu-id="a127c-111">Angi US-101 i Leverandørkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="a127c-111">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="a127c-112">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a127c-112">Click OK.</span></span>
5. <span data-ttu-id="a127c-113">Angi M0001 i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="a127c-113">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="a127c-114">Angi 10 i Antall-feltet.</span><span class="sxs-lookup"><span data-stu-id="a127c-114">In the Quantity field, enter 10.</span></span>
7. <span data-ttu-id="a127c-115">Klikk Bestillingslinje.</span><span class="sxs-lookup"><span data-stu-id="a127c-115">Click Purchase order line.</span></span>
8. <span data-ttu-id="a127c-116">Klikk Leveringsplan.</span><span class="sxs-lookup"><span data-stu-id="a127c-116">Click Delivery schedule.</span></span>
    * <span data-ttu-id="a127c-117">Siden Leveringsplan lar deg angi antall leveranser der det totale antallet på ordrelinjen skal leveres fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="a127c-117">The Delivery schedule page allows you to specify the number of shipments in which the total quantity of the order line will be delivered from the vendor.</span></span>  
    * <span data-ttu-id="a127c-118">Som standard kopieres det totale antallet og andre leveringsdetaljer for den opprinnelige innkjøpslinjen til den første leveringslinjen for planen.</span><span class="sxs-lookup"><span data-stu-id="a127c-118">By default, the system copies the total quantity and other delivery details of the original purchase line into the first delivery schedule line.</span></span> <span data-ttu-id="a127c-119">I dette eksemplet skal vi opprette en tidsplan for to forsendelser, der datoen for den andre forsendelsen er forskjøvet med en uke fra den første forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="a127c-119">In this example, we’ll create a schedule for two shipments, with the second shipment’s date offset by a week from the first shipment.</span></span>  
9. <span data-ttu-id="a127c-120">I Antall-feltet endrer du antallet til 4.</span><span class="sxs-lookup"><span data-stu-id="a127c-120">In the Quantity field, change the quantity to 4.</span></span>
10. <span data-ttu-id="a127c-121">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="a127c-121">Click New.</span></span>
11. <span data-ttu-id="a127c-122">Angi 6 som restantallet i Antall-feltet.</span><span class="sxs-lookup"><span data-stu-id="a127c-122">In the Quantity field, enter 6 as the remaining quantity.</span></span>
    * <span data-ttu-id="a127c-123">Velg en dato som er én uke etter datoen i den første leveringslinjen, i datofeltet for levering.</span><span class="sxs-lookup"><span data-stu-id="a127c-123">In the delivery date field, select a date that’s one week after the date on the first delivery line.</span></span>  
    * <span data-ttu-id="a127c-124">Du kan holde oversikt over det totale antallet som er tildelt til leveringsplanlinjene, ved å se på feltene Total og Gjenværende.</span><span class="sxs-lookup"><span data-stu-id="a127c-124">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="a127c-125">Når det gjenstående antallet er null, er det fullstendige antallet fra den opprinnelige linjen tildelt til tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="a127c-125">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>  
12. <span data-ttu-id="a127c-126">Vis Gebyrkonvertering-delen.</span><span class="sxs-lookup"><span data-stu-id="a127c-126">Expand the Charges conversion section.</span></span>
    * <span data-ttu-id="a127c-127">Alternativene her lar deg kontrollere hvor du vil at gebyrer skal fordeles over leveringsplanlinjene.</span><span class="sxs-lookup"><span data-stu-id="a127c-127">The options here allow you to control how you want charges to be distributed across the delivery schedule lines.</span></span> <span data-ttu-id="a127c-128">Hvis du velger Kopier bruttobeløp, kopieres gebyrbeløpet på den opprinnelige ordrelinjen til hver leveringslinje.</span><span class="sxs-lookup"><span data-stu-id="a127c-128">If you select Copy gross amounts, the charge amount on the original order line is copied to each delivery line.</span></span> <span data-ttu-id="a127c-129">Alternativet Tildel til leveringslinjer deler opprinnelige linjegebyr i henhold til antallet på hver leveringslinje.</span><span class="sxs-lookup"><span data-stu-id="a127c-129">The Allocate to delivery lines option divides the original line charge according to the quantity on each delivery line.</span></span>  
13. <span data-ttu-id="a127c-130">Skjul Gebyrkonvertering-delen.</span><span class="sxs-lookup"><span data-stu-id="a127c-130">Collapse the Charges conversion section.</span></span>
14. <span data-ttu-id="a127c-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a127c-131">Click OK.</span></span>
    * <span data-ttu-id="a127c-132">Leveringsplanen er nå brukt på ordren.</span><span class="sxs-lookup"><span data-stu-id="a127c-132">The delivery schedule has now been applied to the order.</span></span>  
    * <span data-ttu-id="a127c-133">Den opprinnelige ordrelinjen, kalt en kommersiell linje, er konvertert til en ordrelinje med flere leveringer.</span><span class="sxs-lookup"><span data-stu-id="a127c-133">The original order line, now referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="a127c-134">Den er merket med et eget ikon og fungerer som et hode for leveringslinjene.</span><span class="sxs-lookup"><span data-stu-id="a127c-134">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
15. <span data-ttu-id="a127c-135">Velg den andre ordrelinjen, som er den første av de to leveringslinjene.</span><span class="sxs-lookup"><span data-stu-id="a127c-135">Select the second order line, which is the first of the two delivery lines.</span></span>
    * <span data-ttu-id="a127c-136">De to nye linjene, referert til som leveringslinjer, utgjør en leveringsplan.</span><span class="sxs-lookup"><span data-stu-id="a127c-136">The two new lines, referred to as Delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="a127c-137">Ordren behandles mot disse linjene og ikke den opprinnelige linjen.</span><span class="sxs-lookup"><span data-stu-id="a127c-137">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="a127c-138">Hvis dokumenter, for eksempel bekreftelser, produktkvitteringsjournaler eller fakturaer, skrives ut, vises bare leveringslinjene.</span><span class="sxs-lookup"><span data-stu-id="a127c-138">If documents such as confirmations, product receipt journals, or invoices are printed, only the delivery lines are shown.</span></span>  

## <a name="change-the-delivery-schedule"></a><span data-ttu-id="a127c-139">Endre leveringsplanen</span><span class="sxs-lookup"><span data-stu-id="a127c-139">Change the delivery schedule</span></span>
    * <span data-ttu-id="a127c-140">Du kan endre antallet på leveringslinjer.</span><span class="sxs-lookup"><span data-stu-id="a127c-140">You can change the quantity on delivery lines.</span></span> <span data-ttu-id="a127c-141">Hvis du gjør dette, oppdateres den kommersielle linjen automatisk til det totale antallet i leveringslinjene.</span><span class="sxs-lookup"><span data-stu-id="a127c-141">If you do this, the commercial line is automatically updated to the total quantity in the delivery lines.</span></span>  
1. <span data-ttu-id="a127c-142">I Antall-feltet i den første leveringslinjen, endrer du antallet fra 4 til 5.</span><span class="sxs-lookup"><span data-stu-id="a127c-142">In the Quantity field of the first delivery line, change the quantity from 4 to 5.</span></span>
2. <span data-ttu-id="a127c-143">Velg den første bestillingslinjen (den kommersielle linjen).</span><span class="sxs-lookup"><span data-stu-id="a127c-143">Select the first order line (the commercial line).</span></span>
    * <span data-ttu-id="a127c-144">Antallet på den kommersielle linjen er endret til 11.</span><span class="sxs-lookup"><span data-stu-id="a127c-144">The quantity on the commercial line has been changed to 11.</span></span>  

## <a name="process-product-receipt-using-delivery-schedules"></a><span data-ttu-id="a127c-145">Behandle produktkvitteringer ved hjelp av leveringsplaner</span><span class="sxs-lookup"><span data-stu-id="a127c-145">Process product receipt using delivery schedules</span></span>
    * <span data-ttu-id="a127c-146">Bestillingen må bekreftes før produktmottak kan behandles.</span><span class="sxs-lookup"><span data-stu-id="a127c-146">The purchase order must be confirmed before product receipt can be processed.</span></span> <span data-ttu-id="a127c-147">I dette eksemplet registreres mottaket direkte på bestillingen.</span><span class="sxs-lookup"><span data-stu-id="a127c-147">In this example, receipt is recorded directly on the purchase order.</span></span> <span data-ttu-id="a127c-148">Mottaket kan også ha blitt registrert når varene ble mottatt i lageret.</span><span class="sxs-lookup"><span data-stu-id="a127c-148">Receipt could also have been recorded when the goods arrived in the warehouse.</span></span>  
1. <span data-ttu-id="a127c-149">Klikk Kjøp i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a127c-149">On the Action Pane, click Purchase.</span></span>
2. <span data-ttu-id="a127c-150">Klikk Bekreft.</span><span class="sxs-lookup"><span data-stu-id="a127c-150">Click Confirm.</span></span>
3. <span data-ttu-id="a127c-151">Klikk Motta i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a127c-151">On the Action Pane, click Receive.</span></span>
4. <span data-ttu-id="a127c-152">Klikk Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="a127c-152">Click Product receipt.</span></span>
5. <span data-ttu-id="a127c-153">Skriv inn en verdi i Produktkvittering-feltet.</span><span class="sxs-lookup"><span data-stu-id="a127c-153">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="a127c-154">Dette feltet brukes til å angi en referanse som skal brukes som bilag for produktkvitteringsjournalen.</span><span class="sxs-lookup"><span data-stu-id="a127c-154">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
    * <span data-ttu-id="a127c-155">I Antall-feltet velger du Bestilt antall.</span><span class="sxs-lookup"><span data-stu-id="a127c-155">In the Quantity field, select ‘Ordered quantity’.</span></span> <span data-ttu-id="a127c-156">Dette alternativet betyr at det mottaket behandles for antallet som ordrelinjene ble opprettet med.</span><span class="sxs-lookup"><span data-stu-id="a127c-156">This option means that receipt will process for the quantity that the order lines were created with.</span></span>  
    * <span data-ttu-id="a127c-157">Kontroller at feltet Skriv ut produktkvittering er satt til Nei.</span><span class="sxs-lookup"><span data-stu-id="a127c-157">Make sure that the Print product receipt field is set to No.</span></span> <span data-ttu-id="a127c-158">Utskrift er ikke nødvendig i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="a127c-158">Printing isn’t needed in this example.</span></span>  
6. <span data-ttu-id="a127c-159">Vis Linjer-delen.</span><span class="sxs-lookup"><span data-stu-id="a127c-159">Expand the Lines section.</span></span>
    * <span data-ttu-id="a127c-160">Legg merke til hvordan produktkvitteringen opprettes for de to leveringslinjene og ikke for den opprinnelige ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="a127c-160">Notice how the product receipt is created for the two delivery lines and not the original order line.</span></span> <span data-ttu-id="a127c-161">Hvis du har registrert mottak i lageret, vil det være registrert på leveringsplanlinjene.</span><span class="sxs-lookup"><span data-stu-id="a127c-161">If receipt had been recorded in the warehouse, it would also have been recorded on the delivery schedule lines.</span></span>  
7. <span data-ttu-id="a127c-162">Skjul Linjer-delen.</span><span class="sxs-lookup"><span data-stu-id="a127c-162">Collapse the Lines section.</span></span>
8. <span data-ttu-id="a127c-163">Klikk OK for å postere kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="a127c-163">Click OK to post the receipt.</span></span>


