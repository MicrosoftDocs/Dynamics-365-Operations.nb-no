--- 
title: Registrere mottaket av varene i bestillingen
description: "Denne fremgangsmåten viser hvordan du registrerer mottak av varer direkte i en bestilling."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9b2300a593c9e153ee598fa72e29907c82f2b79e
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="73e25-103">Registrere mottaket av varene i bestillingen</span><span class="sxs-lookup"><span data-stu-id="73e25-103">Record the receipt of goods on the purchase order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73e25-104">Denne fremgangsmåten viser hvordan du registrerer mottak av varer direkte i en bestilling.</span><span class="sxs-lookup"><span data-stu-id="73e25-104">This procedure shows you how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="73e25-105">Det er også mulig å registrere produktmottak i lageret, og deretter registrere det senere på bestillingen.</span><span class="sxs-lookup"><span data-stu-id="73e25-105">It’s also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="73e25-106">Denne oppgaven gjøres vanligvis av en innkjøpsagent eller en leverandørkoordinator.</span><span class="sxs-lookup"><span data-stu-id="73e25-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="73e25-107">Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="73e25-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="73e25-108">Eksemplet inneholder fremgangsmåte for å opprette en enkel bestilling, slik at du kan spille av prosedyren som en oppgaveveiledning.</span><span class="sxs-lookup"><span data-stu-id="73e25-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="73e25-109">Hvis du bruker fremgangsmåten på dine egne data, begynner du med underoppgaven Registrere varemottak.</span><span class="sxs-lookup"><span data-stu-id="73e25-109">If you were using the procedure on your own data, you would start at the Record receipt of goods subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="73e25-110">Klargjøre en ny bestilling for mottak av varer</span><span class="sxs-lookup"><span data-stu-id="73e25-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="73e25-111">Gå til Innkjøp og leverandører > Bestillinger > Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="73e25-111">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="73e25-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="73e25-112">Click New.</span></span>
3. <span data-ttu-id="73e25-113">Angi US-101 i Leverandørkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="73e25-113">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="73e25-114">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="73e25-114">Click OK.</span></span>
5. <span data-ttu-id="73e25-115">Angi M0001 i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="73e25-115">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="73e25-116">Angi 5 i Antall-feltet.</span><span class="sxs-lookup"><span data-stu-id="73e25-116">In the Quantity field, enter 5.</span></span>
7. <span data-ttu-id="73e25-117">Klikk Kjøp i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="73e25-117">On the Action Pane, click Purchase.</span></span>
8. <span data-ttu-id="73e25-118">Klikk Bekreft.</span><span class="sxs-lookup"><span data-stu-id="73e25-118">Click Confirm.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="73e25-119">Registrere varemottak</span><span class="sxs-lookup"><span data-stu-id="73e25-119">Record receipt of goods</span></span>
1. <span data-ttu-id="73e25-120">Klikk Motta i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="73e25-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="73e25-121">Klikk Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="73e25-121">Click Product receipt.</span></span>
    * <span data-ttu-id="73e25-122">Antall-feltet lar deg velge forskjellige alternativer for antallet som du vil motta.</span><span class="sxs-lookup"><span data-stu-id="73e25-122">The Quantity field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="73e25-123">Hvis et antall for eksempel er registrert på lageret tidligere, kan du velge Registrert antall.</span><span class="sxs-lookup"><span data-stu-id="73e25-123">For example, if a quantity has previously been registered in the warehouse, you can select Registered quantity.</span></span>  <span data-ttu-id="73e25-124">I dette eksemplet bruker du verdien Bestilt antall.</span><span class="sxs-lookup"><span data-stu-id="73e25-124">For this example, use the value Ordered quantity.</span></span>   
3. <span data-ttu-id="73e25-125">Skriv inn en verdi i Produktkvittering-feltet.</span><span class="sxs-lookup"><span data-stu-id="73e25-125">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="73e25-126">Dette feltet brukes til å angi en referanse som skal brukes som bilag for produktkvitteringsjournalen.</span><span class="sxs-lookup"><span data-stu-id="73e25-126">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
4. <span data-ttu-id="73e25-127">Vis Linjer-delen.</span><span class="sxs-lookup"><span data-stu-id="73e25-127">Expand the Lines section.</span></span>
5. <span data-ttu-id="73e25-128">Sett verdien for Antall til 4.</span><span class="sxs-lookup"><span data-stu-id="73e25-128">Set Quantity to '4'.</span></span>
    * <span data-ttu-id="73e25-129">Her kan du fortsatt manuelt angi antallet som blir mottatt for hver linje i ordren.</span><span class="sxs-lookup"><span data-stu-id="73e25-129">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
6. <span data-ttu-id="73e25-130">Skjul Linjer-delen.</span><span class="sxs-lookup"><span data-stu-id="73e25-130">Collapse the Lines section.</span></span>
7. <span data-ttu-id="73e25-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="73e25-131">Click OK.</span></span>
    * <span data-ttu-id="73e25-132">Varene er nå registrert som mottatt i bestillingen, og en produktkvitteringsjournal er opprettet som dokument for å gjenspeile dette.</span><span class="sxs-lookup"><span data-stu-id="73e25-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="73e25-133">Du kan bruke handlingen Produktmottak for å vise journaler som er opprettet med bestillingen, og se hva som er mottatt og når.</span><span class="sxs-lookup"><span data-stu-id="73e25-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  


