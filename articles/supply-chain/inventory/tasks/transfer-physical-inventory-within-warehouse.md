---
title: "Overføre aktuell beholdning på lageret"
description: "Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for registrere flytting av en vare fra en lokasjon i et lager til en annen."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 9db5eb3ee1af57fa6c229fe2f7dfb80615f9fcff
ms.contentlocale: nb-no
ms.lasthandoff: 01/17/2018

---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="57828-103">Overføre aktuell beholdning på lageret</span><span class="sxs-lookup"><span data-stu-id="57828-103">Transfer physical inventory within the warehouse</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="57828-104">Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for registrere flytting av en vare fra en lokasjon i et lager til en annen.</span><span class="sxs-lookup"><span data-stu-id="57828-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="57828-105">Du må ha en lagerjournalnavn definert for lageroverføringer før du starter dette.</span><span class="sxs-lookup"><span data-stu-id="57828-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="57828-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsdataselskapet USMF ved hjelp av eksempelverdiene som vises, eller du kan bruke dine egne data hvis du har produkter og lokasjoner definert.</span><span class="sxs-lookup"><span data-stu-id="57828-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="57828-107">Disse oppgavene vil vanligvis utføres av en lageransatt.</span><span class="sxs-lookup"><span data-stu-id="57828-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="57828-108">Opprette en beholdningsoverføringsjournal</span><span class="sxs-lookup"><span data-stu-id="57828-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="57828-109">Gå til Overføring.</span><span class="sxs-lookup"><span data-stu-id="57828-109">Go to Transfer.</span></span>
2. <span data-ttu-id="57828-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="57828-110">Click New.</span></span>
3. <span data-ttu-id="57828-111">Angi eller velg en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="57828-111">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="57828-112">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="57828-112">Click OK.</span></span>
    * <span data-ttu-id="57828-113">Det er muligheten til å angi Fra- og Til-dimensjoner for hver journallinje.</span><span class="sxs-lookup"><span data-stu-id="57828-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="57828-114">Disse er nødvendige for denne journaltypen.</span><span class="sxs-lookup"><span data-stu-id="57828-114">These are essential for this journal type.</span></span> <span data-ttu-id="57828-115">Du kan overføre varer til lokasjoner ved hjelp av andre regler.</span><span class="sxs-lookup"><span data-stu-id="57828-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="57828-116">I dette eksemplet skal vi overføre en vare innenfor samme lager, fra en nummerskiltkontrollert lokasjon til en lokasjon som ikke er nummerskiltkontrollert.</span><span class="sxs-lookup"><span data-stu-id="57828-116">In this example we’ll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="57828-117">Opprette journallinjer</span><span class="sxs-lookup"><span data-stu-id="57828-117">Create journal lines</span></span>
1. <span data-ttu-id="57828-118">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="57828-118">Click New.</span></span>
2. <span data-ttu-id="57828-119">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="57828-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="57828-120">Hvis du bruker USMF, kan du velge 'A0001'.</span><span class="sxs-lookup"><span data-stu-id="57828-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="57828-121">Angi eller velg en verdi i feltet Fra site.</span><span class="sxs-lookup"><span data-stu-id="57828-121">In the From site field, enter or select a value.</span></span>
    * <span data-ttu-id="57828-122">Hvis du bruker USMF, kan du velge 2.</span><span class="sxs-lookup"><span data-stu-id="57828-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="57828-123">Angi eller velg en verdi i feltet Til site.</span><span class="sxs-lookup"><span data-stu-id="57828-123">In the To site field, enter or select a value.</span></span>
    * <span data-ttu-id="57828-124">Hvis du bruker USMF, kan du velge 2.</span><span class="sxs-lookup"><span data-stu-id="57828-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="57828-125">Angi eller velg en verdi i feltet Fra lager.</span><span class="sxs-lookup"><span data-stu-id="57828-125">In the From warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="57828-126">Hvis du bruker USMF, kan du velge 24.</span><span class="sxs-lookup"><span data-stu-id="57828-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="57828-127">Angi eller velg en verdi i feltet Til lager.</span><span class="sxs-lookup"><span data-stu-id="57828-127">In the To warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="57828-128">Hvis du bruker USMF, kan du velge 24.</span><span class="sxs-lookup"><span data-stu-id="57828-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="57828-129">Angi eller velg en verdi i Fra lokasjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="57828-129">In the From location field, enter or select a value.</span></span>
    * <span data-ttu-id="57828-130">Hvis du bruker USMF, kan du velge FL-001.</span><span class="sxs-lookup"><span data-stu-id="57828-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="57828-131">Angi eller velg en verdi i Til lokasjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="57828-131">In the To location field, enter or select a value.</span></span>
    * <span data-ttu-id="57828-132">Hvis du bruker USMF, kan du velge BULK-001.</span><span class="sxs-lookup"><span data-stu-id="57828-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="57828-133">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="57828-133">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="57828-134">Klikk kategorien Lagerdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="57828-134">Click the Inventory dimensions tab.</span></span>
11. <span data-ttu-id="57828-135">Angi eller velg en verdi i feltet Nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="57828-135">In the License plate field, enter or select a value.</span></span>
    * <span data-ttu-id="57828-136">Hvis du bruker USMF, kan du velge 24.</span><span class="sxs-lookup"><span data-stu-id="57828-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="57828-137">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="57828-137">Click Save.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="57828-138">Postere beholdningsoverføringsjournalen</span><span class="sxs-lookup"><span data-stu-id="57828-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="57828-139">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="57828-139">Click Post.</span></span>
2. <span data-ttu-id="57828-140">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="57828-140">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="57828-141">Vis lagertransaksjoner</span><span class="sxs-lookup"><span data-stu-id="57828-141">View inventory transactions</span></span>
1. <span data-ttu-id="57828-142">Klikk Lager.</span><span class="sxs-lookup"><span data-stu-id="57828-142">Click Inventory.</span></span>
2. <span data-ttu-id="57828-143">Klikk Transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="57828-143">Click Transactions.</span></span>
    * <span data-ttu-id="57828-144">Her kan du se transaksjonene som ble opprettet da du posterte journalen.</span><span class="sxs-lookup"><span data-stu-id="57828-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

