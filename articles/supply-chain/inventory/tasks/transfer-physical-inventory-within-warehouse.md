---
title: Overføre aktuell beholdning på lageret
description: Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for registrere flytting av en vare fra en lokasjon i et lager til en annen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79b3e91be8aeab10188b6d3925d44a9ec1106406
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554190"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="a86cd-103">Overføre aktuell beholdning på lageret</span><span class="sxs-lookup"><span data-stu-id="a86cd-103">Transfer physical inventory within the warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a86cd-104">Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for registrere flytting av en vare fra en lokasjon i et lager til en annen.</span><span class="sxs-lookup"><span data-stu-id="a86cd-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="a86cd-105">Du må ha en lagerjournalnavn definert for lageroverføringer før du starter dette.</span><span class="sxs-lookup"><span data-stu-id="a86cd-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="a86cd-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsdataselskapet USMF ved hjelp av eksempelverdiene som vises, eller du kan bruke dine egne data hvis du har produkter og lokasjoner definert.</span><span class="sxs-lookup"><span data-stu-id="a86cd-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="a86cd-107">Disse oppgavene vil vanligvis utføres av en lageransatt.</span><span class="sxs-lookup"><span data-stu-id="a86cd-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="a86cd-108">Opprette en beholdningsoverføringsjournal</span><span class="sxs-lookup"><span data-stu-id="a86cd-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="a86cd-109">Gå til Overføring.</span><span class="sxs-lookup"><span data-stu-id="a86cd-109">Go to Transfer.</span></span>
2. <span data-ttu-id="a86cd-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="a86cd-110">Click New.</span></span>
3. <span data-ttu-id="a86cd-111">Angi eller velg en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a86cd-111">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="a86cd-112">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a86cd-112">Click OK.</span></span>
    * <span data-ttu-id="a86cd-113">Det er muligheten til å angi Fra- og Til-dimensjoner for hver journallinje.</span><span class="sxs-lookup"><span data-stu-id="a86cd-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="a86cd-114">Disse er nødvendige for denne journaltypen.</span><span class="sxs-lookup"><span data-stu-id="a86cd-114">These are essential for this journal type.</span></span> <span data-ttu-id="a86cd-115">Du kan overføre varer til lokasjoner ved hjelp av andre regler.</span><span class="sxs-lookup"><span data-stu-id="a86cd-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="a86cd-116">I dette eksemplet skal vi overføre en vare innenfor samme lager, fra en nummerskiltkontrollert lokasjon til en lokasjon som ikke er nummerskiltkontrollert.</span><span class="sxs-lookup"><span data-stu-id="a86cd-116">In this example we’ll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="a86cd-117">Opprette journallinjer</span><span class="sxs-lookup"><span data-stu-id="a86cd-117">Create journal lines</span></span>
1. <span data-ttu-id="a86cd-118">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="a86cd-118">Click New.</span></span>
2. <span data-ttu-id="a86cd-119">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="a86cd-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="a86cd-120">Hvis du bruker USMF, kan du velge 'A0001'.</span><span class="sxs-lookup"><span data-stu-id="a86cd-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="a86cd-121">Angi eller velg en verdi i feltet Fra site.</span><span class="sxs-lookup"><span data-stu-id="a86cd-121">In the From site field, enter or select a value.</span></span>
    * <span data-ttu-id="a86cd-122">Hvis du bruker USMF, kan du velge 2.</span><span class="sxs-lookup"><span data-stu-id="a86cd-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="a86cd-123">Angi eller velg en verdi i feltet Til site.</span><span class="sxs-lookup"><span data-stu-id="a86cd-123">In the To site field, enter or select a value.</span></span>
    * <span data-ttu-id="a86cd-124">Hvis du bruker USMF, kan du velge 2.</span><span class="sxs-lookup"><span data-stu-id="a86cd-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="a86cd-125">Angi eller velg en verdi i feltet Fra lager.</span><span class="sxs-lookup"><span data-stu-id="a86cd-125">In the From warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a86cd-126">Hvis du bruker USMF, kan du velge 24.</span><span class="sxs-lookup"><span data-stu-id="a86cd-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="a86cd-127">Angi eller velg en verdi i feltet Til lager.</span><span class="sxs-lookup"><span data-stu-id="a86cd-127">In the To warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a86cd-128">Hvis du bruker USMF, kan du velge 24.</span><span class="sxs-lookup"><span data-stu-id="a86cd-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="a86cd-129">Angi eller velg en verdi i Fra lokasjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="a86cd-129">In the From location field, enter or select a value.</span></span>
    * <span data-ttu-id="a86cd-130">Hvis du bruker USMF, kan du velge FL-001.</span><span class="sxs-lookup"><span data-stu-id="a86cd-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="a86cd-131">Angi eller velg en verdi i Til lokasjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="a86cd-131">In the To location field, enter or select a value.</span></span>
    * <span data-ttu-id="a86cd-132">Hvis du bruker USMF, kan du velge BULK-001.</span><span class="sxs-lookup"><span data-stu-id="a86cd-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="a86cd-133">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="a86cd-133">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="a86cd-134">Klikk kategorien Lagerdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="a86cd-134">Click the Inventory dimensions tab.</span></span>
11. <span data-ttu-id="a86cd-135">Angi eller velg en verdi i feltet Nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="a86cd-135">In the License plate field, enter or select a value.</span></span>
    * <span data-ttu-id="a86cd-136">Hvis du bruker USMF, kan du velge 24.</span><span class="sxs-lookup"><span data-stu-id="a86cd-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="a86cd-137">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="a86cd-137">Click Save.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="a86cd-138">Postere beholdningsoverføringsjournalen</span><span class="sxs-lookup"><span data-stu-id="a86cd-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="a86cd-139">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="a86cd-139">Click Post.</span></span>
2. <span data-ttu-id="a86cd-140">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a86cd-140">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="a86cd-141">Vis lagertransaksjoner</span><span class="sxs-lookup"><span data-stu-id="a86cd-141">View inventory transactions</span></span>
1. <span data-ttu-id="a86cd-142">Klikk Lager.</span><span class="sxs-lookup"><span data-stu-id="a86cd-142">Click Inventory.</span></span>
2. <span data-ttu-id="a86cd-143">Klikk Transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="a86cd-143">Click Transactions.</span></span>
    * <span data-ttu-id="a86cd-144">Her kan du se transaksjonene som ble opprettet da du posterte journalen.</span><span class="sxs-lookup"><span data-stu-id="a86cd-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

