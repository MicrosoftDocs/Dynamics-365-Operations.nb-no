---
title: Riktig lagersporingsinformasjon
description: Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for å korrigere lagersporingsinformasjon.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5155ada23fe4f559c79964e6bd10d86712009d1d
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145784"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="23ae3-103">Riktig lagersporingsinformasjon</span><span class="sxs-lookup"><span data-stu-id="23ae3-103">Correct inventory tracking information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23ae3-104">Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for å korrigere lagersporingsinformasjon.</span><span class="sxs-lookup"><span data-stu-id="23ae3-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="23ae3-105">I dette eksemplet vil vi oppdatere informasjonen for en partikontrollert vare ved å endre et feilregistrert parti til et annet parti.</span><span class="sxs-lookup"><span data-stu-id="23ae3-105">In this example, we'll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="23ae3-106">Du kan gå gjennom denne prosedyren i demonstrasjonsselskapet USPI eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="23ae3-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="23ae3-107">Hvis du bruker dine egne data, må du ha en vare som er partiaktivert, og den må ikke være lokasjonskontrollert.</span><span class="sxs-lookup"><span data-stu-id="23ae3-107">If you use your own data, you need to have an item that's batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="23ae3-108">Du må også ha et lagerjournalnavn definert for lageroverføringer.</span><span class="sxs-lookup"><span data-stu-id="23ae3-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="23ae3-109">Disse oppgavene vil vanligvis utføres av en lageransatt.</span><span class="sxs-lookup"><span data-stu-id="23ae3-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="23ae3-110">Opprette en beholdningsoverføringsjournal</span><span class="sxs-lookup"><span data-stu-id="23ae3-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="23ae3-111">Gå til Overføring.</span><span class="sxs-lookup"><span data-stu-id="23ae3-111">Go to Transfer.</span></span>
2. <span data-ttu-id="23ae3-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="23ae3-112">Click New.</span></span>
3. <span data-ttu-id="23ae3-113">Angi eller velg en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="23ae3-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="23ae3-114">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="23ae3-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="23ae3-115">Opprette journallinjer</span><span class="sxs-lookup"><span data-stu-id="23ae3-115">Create journal lines</span></span>
1. <span data-ttu-id="23ae3-116">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="23ae3-116">Click New.</span></span>
2. <span data-ttu-id="23ae3-117">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="23ae3-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="23ae3-118">Hvis du bruker USPI, velger du varen M5003.</span><span class="sxs-lookup"><span data-stu-id="23ae3-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="23ae3-119">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="23ae3-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="23ae3-120">Klikk kategorien Lagerdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="23ae3-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="23ae3-121">Angi eller velg en verdi i Partinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="23ae3-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="23ae3-122">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="23ae3-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="23ae3-123">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="23ae3-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="23ae3-124">Angi eller velg en verdi i Partinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="23ae3-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="23ae3-125">Poster journalen</span><span class="sxs-lookup"><span data-stu-id="23ae3-125">Post the journal</span></span>
1. <span data-ttu-id="23ae3-126">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="23ae3-126">Click Post.</span></span>
2. <span data-ttu-id="23ae3-127">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="23ae3-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="23ae3-128">Kontrollere sporingsinformasjon</span><span class="sxs-lookup"><span data-stu-id="23ae3-128">Check tracing information</span></span>
1. <span data-ttu-id="23ae3-129">Klikk Lager.</span><span class="sxs-lookup"><span data-stu-id="23ae3-129">Click Inventory.</span></span>
2. <span data-ttu-id="23ae3-130">Klikk Spor.</span><span class="sxs-lookup"><span data-stu-id="23ae3-130">Click Trace.</span></span>
3. <span data-ttu-id="23ae3-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="23ae3-131">Click OK.</span></span>
    * <span data-ttu-id="23ae3-132">Hvis du bruker denne sporingsinformasjonen, kan du spore tilbake til partiet du korrigerte lageret fra.</span><span class="sxs-lookup"><span data-stu-id="23ae3-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="23ae3-133">Du kan også bruke siden Varesporing for å se denne informasjonen.</span><span class="sxs-lookup"><span data-stu-id="23ae3-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="23ae3-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="23ae3-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="23ae3-135">Kontrollere lagertransaksjoner</span><span class="sxs-lookup"><span data-stu-id="23ae3-135">Check inventory transactions</span></span>
1. <span data-ttu-id="23ae3-136">Klikk Lager.</span><span class="sxs-lookup"><span data-stu-id="23ae3-136">Click Inventory.</span></span>
2. <span data-ttu-id="23ae3-137">Klikk Transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="23ae3-137">Click Transactions.</span></span>
    * <span data-ttu-id="23ae3-138">Her kan du se transaksjonene som ble opprettet da du posterte journalen.</span><span class="sxs-lookup"><span data-stu-id="23ae3-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

