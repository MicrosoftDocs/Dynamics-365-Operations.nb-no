---
title: Riktig lagersporingsinformasjon
description: "Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for å korrigere lagersporingsinformasjon."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: e28d10646f01604098de8cedc30c8c7a7c89866b
ms.contentlocale: nb-no
ms.lasthandoff: 09/12/2017

---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="e7810-103">Riktig lagersporingsinformasjon</span><span class="sxs-lookup"><span data-stu-id="e7810-103">Correct inventory tracking information</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e7810-104">Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for å korrigere lagersporingsinformasjon.</span><span class="sxs-lookup"><span data-stu-id="e7810-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="e7810-105">I dette eksemplet vil vi oppdatere informasjonen for en partikontrollert vare ved å endre et feilregistrert parti til et annet parti.</span><span class="sxs-lookup"><span data-stu-id="e7810-105">In this example, we’ll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="e7810-106">Du kan gå gjennom denne prosedyren i demonstrasjonsselskapet USPI eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="e7810-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="e7810-107">Hvis du bruker dine egne data, må du ha en vare som er partiaktivert, og den må ikke være lokasjonskontrollert.</span><span class="sxs-lookup"><span data-stu-id="e7810-107">If you use your own data, you need to have an item that’s batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="e7810-108">Du må også ha et lagerjournalnavn definert for lageroverføringer.</span><span class="sxs-lookup"><span data-stu-id="e7810-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="e7810-109">Disse oppgavene vil vanligvis utføres av en lageransatt.</span><span class="sxs-lookup"><span data-stu-id="e7810-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="e7810-110">Opprette en beholdningsoverføringsjournal</span><span class="sxs-lookup"><span data-stu-id="e7810-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="e7810-111">Gå til Overføring.</span><span class="sxs-lookup"><span data-stu-id="e7810-111">Go to Transfer.</span></span>
2. <span data-ttu-id="e7810-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="e7810-112">Click New.</span></span>
3. <span data-ttu-id="e7810-113">Angi eller velg en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="e7810-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="e7810-114">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="e7810-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="e7810-115">Opprette journallinjer</span><span class="sxs-lookup"><span data-stu-id="e7810-115">Create journal lines</span></span>
1. <span data-ttu-id="e7810-116">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="e7810-116">Click New.</span></span>
2. <span data-ttu-id="e7810-117">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="e7810-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="e7810-118">Hvis du bruker USPI, velger du varen M5003.</span><span class="sxs-lookup"><span data-stu-id="e7810-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="e7810-119">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="e7810-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="e7810-120">Klikk kategorien Lagerdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="e7810-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="e7810-121">Angi eller velg en verdi i Partinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="e7810-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="e7810-122">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="e7810-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="e7810-123">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="e7810-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="e7810-124">Angi eller velg en verdi i Partinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="e7810-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="e7810-125">Poster journalen</span><span class="sxs-lookup"><span data-stu-id="e7810-125">Post the journal</span></span>
1. <span data-ttu-id="e7810-126">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="e7810-126">Click Post.</span></span>
2. <span data-ttu-id="e7810-127">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="e7810-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="e7810-128">Kontrollere sporingsinformasjon</span><span class="sxs-lookup"><span data-stu-id="e7810-128">Check tracing information</span></span>
1. <span data-ttu-id="e7810-129">Klikk Lager.</span><span class="sxs-lookup"><span data-stu-id="e7810-129">Click Inventory.</span></span>
2. <span data-ttu-id="e7810-130">Klikk Spor.</span><span class="sxs-lookup"><span data-stu-id="e7810-130">Click Trace.</span></span>
3. <span data-ttu-id="e7810-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="e7810-131">Click OK.</span></span>
    * <span data-ttu-id="e7810-132">Hvis du bruker denne sporingsinformasjonen, kan du spore tilbake til partiet du korrigerte lageret fra.</span><span class="sxs-lookup"><span data-stu-id="e7810-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="e7810-133">Du kan også bruke siden Varesporing for å se denne informasjonen.</span><span class="sxs-lookup"><span data-stu-id="e7810-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="e7810-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e7810-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="e7810-135">Kontrollere lagertransaksjoner</span><span class="sxs-lookup"><span data-stu-id="e7810-135">Check inventory transactions</span></span>
1. <span data-ttu-id="e7810-136">Klikk Lager.</span><span class="sxs-lookup"><span data-stu-id="e7810-136">Click Inventory.</span></span>
2. <span data-ttu-id="e7810-137">Klikk Transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="e7810-137">Click Transactions.</span></span>
    * <span data-ttu-id="e7810-138">Her kan du se transaksjonene som ble opprettet da du posterte journalen.</span><span class="sxs-lookup"><span data-stu-id="e7810-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

