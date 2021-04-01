---
title: Opprette leveringsplan
description: Denne fremgangsmåten viser hvordan du oppretter en leveringsplan for en salgsordre.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ddbc59a35b5e6d466a495885e992a00f42f9994
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250912"
---
# <a name="create-delivery-schedule"></a><span data-ttu-id="666ca-103">Opprette leveringsplan</span><span class="sxs-lookup"><span data-stu-id="666ca-103">Create delivery schedule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="666ca-104">Denne fremgangsmåten viser hvordan du oppretter en leveringsplan for en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="666ca-104">This procedure demonstrates how to create a delivery schedule for a sales order.</span></span> <span data-ttu-id="666ca-105">En leveringsplan brukes når et antall i en ordre eller et tilbud blir bedt om å bli levert i flere leveranser.</span><span class="sxs-lookup"><span data-stu-id="666ca-105">A delivery schedule is used when a quantity on an order or a quotation is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="666ca-106">Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="666ca-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-delivery-schedule"></a><span data-ttu-id="666ca-107">Opprette leveringsplan</span><span class="sxs-lookup"><span data-stu-id="666ca-107">Create delivery schedule</span></span>
1. <span data-ttu-id="666ca-108">Gå til Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="666ca-108">Go to All sales orders.</span></span>
2. <span data-ttu-id="666ca-109">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="666ca-109">Click New.</span></span>
3. <span data-ttu-id="666ca-110">Angi eller velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="666ca-110">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="666ca-111">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="666ca-111">Click OK.</span></span>
5. <span data-ttu-id="666ca-112">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="666ca-112">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="666ca-113">Angi et nummer i feltet Antall som er større enn 1.</span><span class="sxs-lookup"><span data-stu-id="666ca-113">In the Quantity field, enter a number that is bigger than 1.</span></span>
7. <span data-ttu-id="666ca-114">Klikk på Salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="666ca-114">Click Sales order line.</span></span>
8. <span data-ttu-id="666ca-115">Klikk på Leveringsplan.</span><span class="sxs-lookup"><span data-stu-id="666ca-115">Click Delivery schedule.</span></span>
    * <span data-ttu-id="666ca-116">Siden Leveringsplan er stedet der du kan angi antall leveranser der det totale antallet på ordrelinjen skal leveres til kunden.</span><span class="sxs-lookup"><span data-stu-id="666ca-116">The Delivery schedule page is the place where you can specify the number of shipments in which the total quantity of the order line will be delivered to the customer.</span></span>    
    * <span data-ttu-id="666ca-117">Som standard kopieres det totale antallet og andre leveringsdetaljer for den opprinnelige salgsordrelinjen til den første leveringslinjen for planen.</span><span class="sxs-lookup"><span data-stu-id="666ca-117">By default, the system copies the total quantity and other delivery details of the original sales line into the first delivery schedule line.</span></span> <span data-ttu-id="666ca-118">I dette eksemplet skal vi opprette en tidsplan for to forsendelser, der datoen for den andre forsendelsen er forskjøvet med en uke fra den første.</span><span class="sxs-lookup"><span data-stu-id="666ca-118">In this example, we'll create a schedule for two shipments, with the second shipment's date offset by a week from the first one.</span></span>  
9. <span data-ttu-id="666ca-119">Angi et tall som er en del av det totale antallet, i Antall-feltet.</span><span class="sxs-lookup"><span data-stu-id="666ca-119">In the Quantity field, enter a number that is part of the total quantity.</span></span>
10. <span data-ttu-id="666ca-120">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="666ca-120">Click New.</span></span>
11. <span data-ttu-id="666ca-121">Angi restantallet i Antall-feltet.</span><span class="sxs-lookup"><span data-stu-id="666ca-121">In the Quantity field, enter the remaining quantity.</span></span>
12. <span data-ttu-id="666ca-122">Angi en dato som er én uke fremover fra datoen for den første leveringslinjen, i feltet Ønsket forsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="666ca-122">In the Requested ship date field, enter a date a date that is one week ahead from the date of the first delivery line.</span></span>
    * <span data-ttu-id="666ca-123">De to alternativene i hurtigfanen Gebyrkonvertering styrer hvordan du vil at tilleggene skal fordeles over leveringsplanlinjene, når de er tilordnet til den opprinnelige ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="666ca-123">The two options on the Charges conversion FastTab control how you want the charges to be distributed across the delivery schedule lines, once they've been assigned to the original order line.</span></span> <span data-ttu-id="666ca-124">Hvis du velger Kopier bruttobeløp, kopieres det samme beløpet til hver linje.</span><span class="sxs-lookup"><span data-stu-id="666ca-124">If you select Copy gross amounts, the same charge amount is copied to each line.</span></span> <span data-ttu-id="666ca-125">Alternativet Tildel til leveringslinjer deler tillegget likt på tvers av leveringslinjene.</span><span class="sxs-lookup"><span data-stu-id="666ca-125">The Allocate to delivery lines option divides the charge equally across the delivery lines.</span></span>  
    * <span data-ttu-id="666ca-126">Bare faste gebyrer kan deles, mens variable kostnader fortsatt blir kopiert til linjene.</span><span class="sxs-lookup"><span data-stu-id="666ca-126">Only fixed charges can be divided, whereas variable charges will still be copied to the lines.</span></span>  
13. <span data-ttu-id="666ca-127">Flytt markøren bort fra den andre leveringslinjen for å oppdatere siden.</span><span class="sxs-lookup"><span data-stu-id="666ca-127">Move the cursor away from the second delivery line to update the page.</span></span>
    * <span data-ttu-id="666ca-128">Du kan holde oversikt over det totale antallet som er tildelt til leveringsplanlinjene, ved å se på feltene Total og Gjenværende.</span><span class="sxs-lookup"><span data-stu-id="666ca-128">You can keep track of the total quantity that's allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="666ca-129">Når det gjenstående antallet er null, er det fullstendige antallet fra den opprinnelige linjen tildelt til tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="666ca-129">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>   
14. <span data-ttu-id="666ca-130">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="666ca-130">Click OK.</span></span>
    * <span data-ttu-id="666ca-131">Leveringsplanen er nå kopiert til ordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="666ca-131">The delivery schedule has now been copied to the order lines.</span></span>   
    * <span data-ttu-id="666ca-132">Den opprinnelige ordrelinjen, kalt en kommersiell linje, er konvertert til en ordrelinje med flere leveringer.</span><span class="sxs-lookup"><span data-stu-id="666ca-132">The original order line, referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="666ca-133">Den er merket med et eget ikon og fungerer som et hode for leveringslinjene.</span><span class="sxs-lookup"><span data-stu-id="666ca-133">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
    * <span data-ttu-id="666ca-134">De to nye linjene, referert til som leveringslinjer, utgjør en leveringsplan.</span><span class="sxs-lookup"><span data-stu-id="666ca-134">The two new lines, referred to as delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="666ca-135">Ordren behandles mot disse linjene og ikke den opprinnelige linjen.</span><span class="sxs-lookup"><span data-stu-id="666ca-135">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="666ca-136">Hvis dokumenter, for eksempel plukklister, følgesedler eller fakturaer, skrives ut, vises bare leveringslinjene.</span><span class="sxs-lookup"><span data-stu-id="666ca-136">If documents such as confirmation slips, picking lists, packing slips, or invoices are printed, only the delivery lines are shown.</span></span>   
    * <span data-ttu-id="666ca-137">Leveringslinjene kan ha andre leveringsdatoer, antall, leveringsmåter og lagerdimensjoner, for eksempel område og lager.</span><span class="sxs-lookup"><span data-stu-id="666ca-137">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span> <span data-ttu-id="666ca-138">Produktdimensjonene må imidlertid alltid samsvare med dem på den kommersielle linjen, og kan ikke endres.</span><span class="sxs-lookup"><span data-stu-id="666ca-138">However, the product dimensions must always match the ones on the commercial line and can't be changed.</span></span>  
15. <span data-ttu-id="666ca-139">Angi et nummer i feltet Antall som er større enn det gjeldende nummeret.</span><span class="sxs-lookup"><span data-stu-id="666ca-139">In the Quantity field, enter a number that's bigger than the current one.</span></span>
16. <span data-ttu-id="666ca-140">Velg den kommersielle linjen for å se effekten av omberegningen av antall.</span><span class="sxs-lookup"><span data-stu-id="666ca-140">Select the commercial line to see the effect of the quantity recalculation.</span></span>
17. <span data-ttu-id="666ca-141">Klikk på Plukk og pakk i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="666ca-141">On the Action Pane, click Pick and pack.</span></span>
18. <span data-ttu-id="666ca-142">Klikk på Poster følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="666ca-142">Click Post packing slip.</span></span>
19. <span data-ttu-id="666ca-143">Utvid seksjonen Parametere.</span><span class="sxs-lookup"><span data-stu-id="666ca-143">Expand the Parameters section.</span></span>
20. <span data-ttu-id="666ca-144">Velg Alle i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="666ca-144">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="666ca-145">Legg merke til at følgeseddelen opprettes for de to leveringsplanlinjene og ikke den opprinnelige ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="666ca-145">Note that the packing slip will be created for the two delivery schedule lines and not the original order line.</span></span>  
21. <span data-ttu-id="666ca-146">Velg Ja i feltet Skriv ut pakkseddel.</span><span class="sxs-lookup"><span data-stu-id="666ca-146">Select Yes in the Print packing slip field.</span></span>
22. <span data-ttu-id="666ca-147">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="666ca-147">Click OK.</span></span>
23. <span data-ttu-id="666ca-148">Klikk på Ja.</span><span class="sxs-lookup"><span data-stu-id="666ca-148">Click Yes.</span></span>
24. <span data-ttu-id="666ca-149">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="666ca-149">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]