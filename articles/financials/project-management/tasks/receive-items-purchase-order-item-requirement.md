---
title: Motta varer i bestilling fra varebehov
description: Denne fremgangsmåten viser hvordan du mottar varer på en bestilling fra et varebehov.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26572a49426719fba520338a5eccd7e0af78890e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572379"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="513e6-103">Motta varer i bestilling fra varebehov</span><span class="sxs-lookup"><span data-stu-id="513e6-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="513e6-104">Denne fremgangsmåten viser hvordan du mottar varer på en bestilling fra et varebehov.</span><span class="sxs-lookup"><span data-stu-id="513e6-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="513e6-105">Når du bruker et varebehov i stedet for en varetransaksjon, kan du planlegge levering like før varen faktisk brukes, opprette en bestilling, inkludere varen i rammeverket for forretningsavtalen, og inkludere varebehovet i produksjonsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="513e6-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="513e6-106">Denne oppgaven bruker USSI-datasettet.</span><span class="sxs-lookup"><span data-stu-id="513e6-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="513e6-107">Gå til Prosjektstyring og regnskap > Prosjekter > Alle prosjekter.</span><span class="sxs-lookup"><span data-stu-id="513e6-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="513e6-108">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="513e6-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="513e6-109">Klikk Plan i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="513e6-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="513e6-110">Klikk Varebehov.</span><span class="sxs-lookup"><span data-stu-id="513e6-110">Click Item requirements.</span></span>
5. <span data-ttu-id="513e6-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="513e6-111">Click New.</span></span>
6. <span data-ttu-id="513e6-112">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="513e6-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="513e6-113">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="513e6-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="513e6-114">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="513e6-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="513e6-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="513e6-115">Click Save.</span></span>
10. <span data-ttu-id="513e6-116">Klikk Administrer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="513e6-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="513e6-117">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="513e6-117">Click Functions.</span></span>
12. <span data-ttu-id="513e6-118">Klikk Opprett bestilling.</span><span class="sxs-lookup"><span data-stu-id="513e6-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="513e6-119">Merk av for Ta med.</span><span class="sxs-lookup"><span data-stu-id="513e6-119">Select the Include check box.</span></span>
14. <span data-ttu-id="513e6-120">Angi eller velg en verdi i Leverandørkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="513e6-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="513e6-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="513e6-121">Click OK.</span></span>
16. <span data-ttu-id="513e6-122">Gå til Leverandører > Bestillinger > Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="513e6-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="513e6-123">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="513e6-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="513e6-124">Klikk Kjøp i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="513e6-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="513e6-125">Klikk Bekreft.</span><span class="sxs-lookup"><span data-stu-id="513e6-125">Click Confirm.</span></span>
20. <span data-ttu-id="513e6-126">Klikk Motta i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="513e6-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="513e6-127">Klikk Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="513e6-127">Click Product receipt.</span></span>
22. <span data-ttu-id="513e6-128">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="513e6-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="513e6-129">Skriv inn en verdi i feltet Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="513e6-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="513e6-130">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="513e6-130">Click OK.</span></span>

