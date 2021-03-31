---
title: Riktig lagersporingsinformasjon
description: Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for å korrigere lagersporingsinformasjon.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 76e73f10df5bb520b6d0d787eda08053a5e33c81
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223416"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="d9445-103">Riktig lagersporingsinformasjon</span><span class="sxs-lookup"><span data-stu-id="d9445-103">Correct inventory tracking information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d9445-104">Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for å korrigere lagersporingsinformasjon.</span><span class="sxs-lookup"><span data-stu-id="d9445-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="d9445-105">I dette eksemplet vil vi oppdatere informasjonen for en partikontrollert vare ved å endre et feilregistrert parti til et annet parti.</span><span class="sxs-lookup"><span data-stu-id="d9445-105">In this example, we'll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="d9445-106">Du kan gå gjennom denne prosedyren i demonstrasjonsselskapet USPI eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="d9445-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="d9445-107">Hvis du bruker dine egne data, må du ha en vare som er partiaktivert, og den må ikke være lokasjonskontrollert.</span><span class="sxs-lookup"><span data-stu-id="d9445-107">If you use your own data, you need to have an item that's batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="d9445-108">Du må også ha et lagerjournalnavn definert for lageroverføringer.</span><span class="sxs-lookup"><span data-stu-id="d9445-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="d9445-109">Disse oppgavene vil vanligvis utføres av en lageransatt.</span><span class="sxs-lookup"><span data-stu-id="d9445-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="d9445-110">Opprette en beholdningsoverføringsjournal</span><span class="sxs-lookup"><span data-stu-id="d9445-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="d9445-111">Gå til Overføring.</span><span class="sxs-lookup"><span data-stu-id="d9445-111">Go to Transfer.</span></span>
2. <span data-ttu-id="d9445-112">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="d9445-112">Click New.</span></span>
3. <span data-ttu-id="d9445-113">Angi eller velg en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d9445-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="d9445-114">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="d9445-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="d9445-115">Opprette journallinjer</span><span class="sxs-lookup"><span data-stu-id="d9445-115">Create journal lines</span></span>
1. <span data-ttu-id="d9445-116">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="d9445-116">Click New.</span></span>
2. <span data-ttu-id="d9445-117">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="d9445-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="d9445-118">Hvis du bruker USPI, velger du varen M5003.</span><span class="sxs-lookup"><span data-stu-id="d9445-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="d9445-119">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="d9445-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="d9445-120">Klikk på fanen Lagerdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="d9445-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="d9445-121">Angi eller velg en verdi i Partinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="d9445-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="d9445-122">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="d9445-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="d9445-123">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="d9445-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="d9445-124">Angi eller velg en verdi i Partinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="d9445-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="d9445-125">Poster journalen</span><span class="sxs-lookup"><span data-stu-id="d9445-125">Post the journal</span></span>
1. <span data-ttu-id="d9445-126">Klikk på Poster.</span><span class="sxs-lookup"><span data-stu-id="d9445-126">Click Post.</span></span>
2. <span data-ttu-id="d9445-127">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="d9445-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="d9445-128">Kontrollere sporingsinformasjon</span><span class="sxs-lookup"><span data-stu-id="d9445-128">Check tracing information</span></span>
1. <span data-ttu-id="d9445-129">Klikk på Lager.</span><span class="sxs-lookup"><span data-stu-id="d9445-129">Click Inventory.</span></span>
2. <span data-ttu-id="d9445-130">Klikk på Spor.</span><span class="sxs-lookup"><span data-stu-id="d9445-130">Click Trace.</span></span>
3. <span data-ttu-id="d9445-131">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="d9445-131">Click OK.</span></span>
    * <span data-ttu-id="d9445-132">Hvis du bruker denne sporingsinformasjonen, kan du spore tilbake til partiet du korrigerte lageret fra.</span><span class="sxs-lookup"><span data-stu-id="d9445-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="d9445-133">Du kan også bruke siden Varesporing for å se denne informasjonen.</span><span class="sxs-lookup"><span data-stu-id="d9445-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="d9445-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d9445-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="d9445-135">Kontrollere lagertransaksjoner</span><span class="sxs-lookup"><span data-stu-id="d9445-135">Check inventory transactions</span></span>
1. <span data-ttu-id="d9445-136">Klikk på Lager.</span><span class="sxs-lookup"><span data-stu-id="d9445-136">Click Inventory.</span></span>
2. <span data-ttu-id="d9445-137">Klikk på Transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="d9445-137">Click Transactions.</span></span>
    * <span data-ttu-id="d9445-138">Her kan du se transaksjonene som ble opprettet da du posterte journalen.</span><span class="sxs-lookup"><span data-stu-id="d9445-138">Here you can see the transactions that were created when you posted your journal.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]