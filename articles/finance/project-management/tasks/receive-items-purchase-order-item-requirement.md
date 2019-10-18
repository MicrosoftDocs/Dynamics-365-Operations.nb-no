---
title: Motta varer i bestilling fra varebehov
description: Dette emnet forklarer hvordan du mottar varer på en bestilling fra et varebehov.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7afdae65c5ae7e3196c6b9f142dd87aec39b5ea3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174426"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="c86e4-103">Motta varer i bestilling fra varebehov</span><span class="sxs-lookup"><span data-stu-id="c86e4-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c86e4-104">Dette emnet forklarer hvordan du mottar varer på en bestilling fra et varebehov.</span><span class="sxs-lookup"><span data-stu-id="c86e4-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="c86e4-105">Når du bruker et varebehov i stedet for en varetransaksjon, kan du planlegge levering like før varen faktisk brukes, opprette en bestilling, inkludere varen i rammeverket for forretningsavtalen, og inkludere varebehovet i produksjonsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="c86e4-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="c86e4-106">Denne oppgaven bruker USSI-datasettet.</span><span class="sxs-lookup"><span data-stu-id="c86e4-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="c86e4-107">Gå til **Moduler > Prosjektstyring og regnskap > Prosjekter > Alle prosjekter** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="c86e4-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="c86e4-108">Velg koblingen i den ønskede raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c86e4-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="c86e4-109">Velg **Plan** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c86e4-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="c86e4-110">Velg **Varebehov**.</span><span class="sxs-lookup"><span data-stu-id="c86e4-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="c86e4-111">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c86e4-111">Select **New**.</span></span>
6. <span data-ttu-id="c86e4-112">Angi eller velg en verdi i feltet **Varenummer** i den nye raden.</span><span class="sxs-lookup"><span data-stu-id="c86e4-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="c86e4-113">Angi et tall i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c86e4-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="c86e4-114">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c86e4-114">Select **Save**.</span></span>
9. <span data-ttu-id="c86e4-115">Velg **Administrer** på handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c86e4-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="c86e4-116">Velg **Funksjoner**.</span><span class="sxs-lookup"><span data-stu-id="c86e4-116">Select **Functions**.</span></span>
11. <span data-ttu-id="c86e4-117">Velg **Opprett bestilling**.</span><span class="sxs-lookup"><span data-stu-id="c86e4-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="c86e4-118">Merk av for **Inkluder alt**.</span><span class="sxs-lookup"><span data-stu-id="c86e4-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="c86e4-119">Angi eller velg en verdi i **Leverandørkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c86e4-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="c86e4-120">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c86e4-120">Select **OK**.</span></span>
15. <span data-ttu-id="c86e4-121">I navigasjonsruten går du til **Moduler > Leverandører > Bestillinger > Alle bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="c86e4-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="c86e4-122">Velg koblingen i den ønskede raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c86e4-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="c86e4-123">Klikk **Innkjøp** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c86e4-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="c86e4-124">Velg **Bekreft**.</span><span class="sxs-lookup"><span data-stu-id="c86e4-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="c86e4-125">Klikk på **Mottak** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c86e4-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="c86e4-126">Velg **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="c86e4-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="c86e4-127">Skriv inn en verdi i feltet **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="c86e4-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="c86e4-128">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c86e4-128">Select **OK**.</span></span>

