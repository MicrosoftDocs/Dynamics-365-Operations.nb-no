--- 
title: Motta varer i bestilling fra varebehov
description: "Denne fremgangsmåten viser hvordan du mottar varer på en bestilling fra et varebehov."
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0fa70da5e06d1bc82fb9d2419bb0a7c8dd0da467
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="3809b-103">Motta varer i bestilling fra varebehov</span><span class="sxs-lookup"><span data-stu-id="3809b-103">Receive items on purchase order from item requirement</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3809b-104">Denne fremgangsmåten viser hvordan du mottar varer på en bestilling fra et varebehov.</span><span class="sxs-lookup"><span data-stu-id="3809b-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="3809b-105">Når du bruker et varebehov i stedet for en varetransaksjon, kan du planlegge levering like før varen faktisk brukes, opprette en bestilling, inkludere varen i rammeverket for forretningsavtalen, og inkludere varebehovet i produksjonsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="3809b-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="3809b-106">Denne oppgaven bruker USSI-datasettet.</span><span class="sxs-lookup"><span data-stu-id="3809b-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="3809b-107">Gå til Prosjektstyring og regnskap > Prosjekter > Alle prosjekter.</span><span class="sxs-lookup"><span data-stu-id="3809b-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="3809b-108">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3809b-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="3809b-109">Klikk Plan i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3809b-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="3809b-110">Klikk Varebehov.</span><span class="sxs-lookup"><span data-stu-id="3809b-110">Click Item requirements.</span></span>
5. <span data-ttu-id="3809b-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3809b-111">Click New.</span></span>
6. <span data-ttu-id="3809b-112">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3809b-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="3809b-113">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="3809b-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="3809b-114">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="3809b-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="3809b-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3809b-115">Click Save.</span></span>
10. <span data-ttu-id="3809b-116">Klikk Administrer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3809b-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="3809b-117">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="3809b-117">Click Functions.</span></span>
12. <span data-ttu-id="3809b-118">Klikk Opprett bestilling.</span><span class="sxs-lookup"><span data-stu-id="3809b-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="3809b-119">Merk av for Ta med.</span><span class="sxs-lookup"><span data-stu-id="3809b-119">Select the Include check box.</span></span>
14. <span data-ttu-id="3809b-120">Angi eller velg en verdi i Leverandørkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="3809b-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="3809b-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3809b-121">Click OK.</span></span>
16. <span data-ttu-id="3809b-122">Gå til Leverandører > Bestillinger > Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="3809b-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="3809b-123">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3809b-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="3809b-124">Klikk Kjøp i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3809b-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="3809b-125">Klikk Bekreft.</span><span class="sxs-lookup"><span data-stu-id="3809b-125">Click Confirm.</span></span>
20. <span data-ttu-id="3809b-126">Klikk Motta i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3809b-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="3809b-127">Klikk Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="3809b-127">Click Product receipt.</span></span>
22. <span data-ttu-id="3809b-128">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3809b-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="3809b-129">Skriv inn en verdi i feltet Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="3809b-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="3809b-130">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3809b-130">Click OK.</span></span>


