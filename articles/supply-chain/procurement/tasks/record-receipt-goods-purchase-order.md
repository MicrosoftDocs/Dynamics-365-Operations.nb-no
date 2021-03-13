---
title: Registrere mottaket av varene i bestillingen
description: Dette emnet forklarer hvordan du registrerer mottak av varer direkte i en bestilling.
author: RichardLuan
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d016df08850c75858c50b7f9a97b11b566d26cb0
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022664"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="6f571-103">Registrere mottaket av varene i bestillingen</span><span class="sxs-lookup"><span data-stu-id="6f571-103">Record the receipt of goods on the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f571-104">Dette emnet forklarer hvordan du registrerer mottak av varer direkte i en bestilling.</span><span class="sxs-lookup"><span data-stu-id="6f571-104">This topic explains how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="6f571-105">Det er også mulig å registrere produktmottak i lageret, og deretter registrere det senere på bestillingen.</span><span class="sxs-lookup"><span data-stu-id="6f571-105">It's also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="6f571-106">Denne oppgaven gjøres vanligvis av en innkjøpsagent eller en leverandørkoordinator.</span><span class="sxs-lookup"><span data-stu-id="6f571-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="6f571-107">Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="6f571-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="6f571-108">Eksemplet inneholder fremgangsmåte for å opprette en enkel bestilling, slik at du kan spille av prosedyren som en oppgaveveiledning.</span><span class="sxs-lookup"><span data-stu-id="6f571-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="6f571-109">Hvis du bruker fremgangsmåten på dine egne data, begynner du med underoppgaven **Registrere varemottak**.</span><span class="sxs-lookup"><span data-stu-id="6f571-109">If you were using the procedure on your own data, you would start at the **Record receipt of goods** subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="6f571-110">Klargjøre en ny bestilling for mottak av varer</span><span class="sxs-lookup"><span data-stu-id="6f571-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="6f571-111">Gå til **Navigasjonsrute > Moduler > Innkjøp og leverandører > Bestillinger > Alle bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="6f571-111">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="6f571-112">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6f571-112">Select **New**.</span></span>
3. <span data-ttu-id="6f571-113">Angi `US-101` i **Leverandørkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6f571-113">In the **Vendor account** field, enter `US-101`.</span></span>
4. <span data-ttu-id="6f571-114">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f571-114">Select **OK**.</span></span>
5. <span data-ttu-id="6f571-115">Angi `M0001` i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="6f571-115">In the **Item number** field, enter `M0001`.</span></span>
6. <span data-ttu-id="6f571-116">I **Antall**-feltet angir du `5`.</span><span class="sxs-lookup"><span data-stu-id="6f571-116">In the **Quantity** field, enter `5`.</span></span>
7. <span data-ttu-id="6f571-117">Klikk på **Innkjøp** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6f571-117">On the Action Pane, select **Purchase**.</span></span>
8. <span data-ttu-id="6f571-118">Velg **Bekreft**.</span><span class="sxs-lookup"><span data-stu-id="6f571-118">Select **Confirm**.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="6f571-119">Registrere varemottak</span><span class="sxs-lookup"><span data-stu-id="6f571-119">Record receipt of goods</span></span>
1. <span data-ttu-id="6f571-120">Klikk på **Mottak** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6f571-120">On the Action Pane, select **Receive**.</span></span>
2. <span data-ttu-id="6f571-121">Velg **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="6f571-121">Select **Product receipt**.</span></span> <span data-ttu-id="6f571-122">**Antall**-feltet lar deg velge forskjellige alternativer for antallet som du vil motta.</span><span class="sxs-lookup"><span data-stu-id="6f571-122">The **Quantity** field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="6f571-123">Hvis et antall for eksempel er registrert på lageret tidligere, kan du velge **Registrert antall**.</span><span class="sxs-lookup"><span data-stu-id="6f571-123">For example, if a quantity has previously been registered in the warehouse, you can select **Registered quantity**.</span></span> <span data-ttu-id="6f571-124">I dette eksemplet bruker du verdien **Bestilt antall**.</span><span class="sxs-lookup"><span data-stu-id="6f571-124">For this example, use the value **Ordered quantity**.</span></span>
3. <span data-ttu-id="6f571-125">Utvid seksjonen **Oversikt**.</span><span class="sxs-lookup"><span data-stu-id="6f571-125">Expand the **Overview** section.</span></span>
4. <span data-ttu-id="6f571-126">Skriv inn en verdi i **Produktkvittering**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6f571-126">In the **Product receipt** field, type any value.</span></span> <span data-ttu-id="6f571-127">Dette feltet brukes til å angi en referanse som skal brukes som bilag for produktkvitteringsjournalen.</span><span class="sxs-lookup"><span data-stu-id="6f571-127">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
5. <span data-ttu-id="6f571-128">Vis **Linjer**-delen.</span><span class="sxs-lookup"><span data-stu-id="6f571-128">Expand the **Lines** section.</span></span>
6. <span data-ttu-id="6f571-129">Sett verdien for **Antall** til 4.</span><span class="sxs-lookup"><span data-stu-id="6f571-129">Set **Quantity** to '4'.</span></span> <span data-ttu-id="6f571-130">Her kan du fortsatt manuelt angi antallet som blir mottatt for hver linje i ordren.</span><span class="sxs-lookup"><span data-stu-id="6f571-130">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
7. <span data-ttu-id="6f571-131">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f571-131">Select **OK**.</span></span> <span data-ttu-id="6f571-132">Varene er nå registrert som mottatt i bestillingen, og en produktkvitteringsjournal er opprettet som dokument for å gjenspeile dette.</span><span class="sxs-lookup"><span data-stu-id="6f571-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="6f571-133">Du kan bruke handlingen Produktmottak for å vise journaler som er opprettet med bestillingen, og se hva som er mottatt og når.</span><span class="sxs-lookup"><span data-stu-id="6f571-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  

