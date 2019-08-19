---
title: Registrere mottaket av varene i bestillingen
description: Dette emnet forklarer hvordan du registrerer mottak av varer direkte i en bestilling.
author: FrankDahl
manager: AnnBe
ms.date: 07/09/19
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e81bb3fe95326636c28885d4decad69f841e3db
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844015"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="330fb-103">Registrere mottaket av varene i bestillingen</span><span class="sxs-lookup"><span data-stu-id="330fb-103">Record the receipt of goods on the purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="330fb-104">Dette emnet forklarer hvordan du registrerer mottak av varer direkte i en bestilling.</span><span class="sxs-lookup"><span data-stu-id="330fb-104">This topic explains how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="330fb-105">Det er også mulig å registrere produktmottak i lageret, og deretter registrere det senere på bestillingen.</span><span class="sxs-lookup"><span data-stu-id="330fb-105">It’s also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="330fb-106">Denne oppgaven gjøres vanligvis av en innkjøpsagent eller en leverandørkoordinator.</span><span class="sxs-lookup"><span data-stu-id="330fb-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="330fb-107">Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="330fb-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="330fb-108">Eksemplet inneholder fremgangsmåte for å opprette en enkel bestilling, slik at du kan spille av prosedyren som en oppgaveveiledning.</span><span class="sxs-lookup"><span data-stu-id="330fb-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="330fb-109">Hvis du bruker fremgangsmåten på dine egne data, begynner du med underoppgaven **Registrere varemottak**.</span><span class="sxs-lookup"><span data-stu-id="330fb-109">If you were using the procedure on your own data, you would start at the **Record receipt of goods** subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="330fb-110">Klargjøre en ny bestilling for mottak av varer</span><span class="sxs-lookup"><span data-stu-id="330fb-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="330fb-111">Gå til **Navigasjonsrute > Moduler > Innkjøp og leverandører > Bestillinger > Alle bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="330fb-111">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="330fb-112">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="330fb-112">Select **New**.</span></span>
3. <span data-ttu-id="330fb-113">Angi `US-101` i **Leverandørkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="330fb-113">In the **Vendor account** field, enter `US-101`.</span></span>
4. <span data-ttu-id="330fb-114">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="330fb-114">Select **OK**.</span></span>
5. <span data-ttu-id="330fb-115">Angi `M0001` i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="330fb-115">In the **Item number** field, enter `M0001`.</span></span>
6. <span data-ttu-id="330fb-116">I **Antall**-feltet angir du `5`.</span><span class="sxs-lookup"><span data-stu-id="330fb-116">In the **Quantity** field, enter `5`.</span></span>
7. <span data-ttu-id="330fb-117">Klikk **Innkjøp** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="330fb-117">On the Action Pane, select **Purchase**.</span></span>
8. <span data-ttu-id="330fb-118">Velg **Bekreft**.</span><span class="sxs-lookup"><span data-stu-id="330fb-118">Select **Confirm**.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="330fb-119">Registrere varemottak</span><span class="sxs-lookup"><span data-stu-id="330fb-119">Record receipt of goods</span></span>
1. <span data-ttu-id="330fb-120">Klikk på **Mottak** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="330fb-120">On the Action Pane, select **Receive**.</span></span>
2. <span data-ttu-id="330fb-121">Velg **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="330fb-121">Select **Product receipt**.</span></span> <span data-ttu-id="330fb-122">**Antall**-feltet lar deg velge forskjellige alternativer for antallet som du vil motta.</span><span class="sxs-lookup"><span data-stu-id="330fb-122">The **Quantity** field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="330fb-123">Hvis et antall for eksempel er registrert på lageret tidligere, kan du velge **Registrert antall**.</span><span class="sxs-lookup"><span data-stu-id="330fb-123">For example, if a quantity has previously been registered in the warehouse, you can select **Registered quantity**.</span></span> <span data-ttu-id="330fb-124">I dette eksemplet bruker du verdien **Bestilt antall**.</span><span class="sxs-lookup"><span data-stu-id="330fb-124">For this example, use the value **Ordered quantity**.</span></span>
3. <span data-ttu-id="330fb-125">Utvid seksjonen **Oversikt**.</span><span class="sxs-lookup"><span data-stu-id="330fb-125">Expand the **Overview** section.</span></span>
4. <span data-ttu-id="330fb-126">Skriv inn en verdi i **Produktkvittering**-feltet.</span><span class="sxs-lookup"><span data-stu-id="330fb-126">In the **Product receipt** field, type any value.</span></span> <span data-ttu-id="330fb-127">Dette feltet brukes til å angi en referanse som skal brukes som bilag for produktkvitteringsjournalen.</span><span class="sxs-lookup"><span data-stu-id="330fb-127">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
5. <span data-ttu-id="330fb-128">Vis **Linjer**-delen.</span><span class="sxs-lookup"><span data-stu-id="330fb-128">Expand the **Lines** section.</span></span>
6. <span data-ttu-id="330fb-129">Sett verdien for **Antall** til 4.</span><span class="sxs-lookup"><span data-stu-id="330fb-129">Set **Quantity** to '4'.</span></span> <span data-ttu-id="330fb-130">Her kan du fortsatt manuelt angi antallet som blir mottatt for hver linje i ordren.</span><span class="sxs-lookup"><span data-stu-id="330fb-130">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
7. <span data-ttu-id="330fb-131">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="330fb-131">Select **OK**.</span></span> <span data-ttu-id="330fb-132">Varene er nå registrert som mottatt i bestillingen, og en produktkvitteringsjournal er opprettet som dokument for å gjenspeile dette.</span><span class="sxs-lookup"><span data-stu-id="330fb-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="330fb-133">Du kan bruke handlingen Produktmottak for å vise journaler som er opprettet med bestillingen, og se hva som er mottatt og når.</span><span class="sxs-lookup"><span data-stu-id="330fb-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  

