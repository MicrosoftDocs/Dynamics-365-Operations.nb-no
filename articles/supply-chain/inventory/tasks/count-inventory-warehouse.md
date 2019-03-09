---
title: Lageropptelling på et lager
description: Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageropptellingsjournal for å telle en bestemt vare på en lokasjon i lageret.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c0bbfe8f86d27f81b0d577ed89dfa34ebcf3f18
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "353477"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="6f187-103">Lageropptelling på et lager</span><span class="sxs-lookup"><span data-stu-id="6f187-103">Count inventory in a warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6f187-104">Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageropptellingsjournal for å telle en bestemt vare på en lokasjon i lageret.</span><span class="sxs-lookup"><span data-stu-id="6f187-104">This procedure walks you through the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="6f187-105">Fremgangsmåten gjelder for "grunnleggende lageraktiviteter"-funksjoner, tilgjengelige i lagerstyringsmodulen, ikke for lagerstyringsfunksjonaliteten som er tilgjengelig i lagerstyringsmodulen.</span><span class="sxs-lookup"><span data-stu-id="6f187-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="6f187-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="6f187-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="6f187-107">Hvis du bruker dine egne data, må du kontrollere at du har produkter og lokasjoner definert, og at du har opprettet et beholdningsjournalnavn for opptellingsjournaler.</span><span class="sxs-lookup"><span data-stu-id="6f187-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="6f187-108">Beholdningsopptelling utføres vanligvis av en lageransatt.</span><span class="sxs-lookup"><span data-stu-id="6f187-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="6f187-109">Opprette en lageropptellingsjournal</span><span class="sxs-lookup"><span data-stu-id="6f187-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="6f187-110">Gå til Lagerstyring > Loggoppføringer > Vareopptelling > Opptelling.</span><span class="sxs-lookup"><span data-stu-id="6f187-110">Go to Inventory management > Journal entries > Item counting > Counting.</span></span>
2. <span data-ttu-id="6f187-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6f187-111">Click New.</span></span>
3. <span data-ttu-id="6f187-112">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6f187-112">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6f187-113">Klikk journalnavnet for beholdningsopptelling som du vil bruke, i listen</span><span class="sxs-lookup"><span data-stu-id="6f187-113">In the list, click on the inventory counting journal name you want to use</span></span>
    * <span data-ttu-id="6f187-114">Noen andre felt fylles ut basert på oppsettet av standardnavn for lageropptellingsjournal som du velger.</span><span class="sxs-lookup"><span data-stu-id="6f187-114">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
5. <span data-ttu-id="6f187-115">Klikk rullegardinknappen i feltet Arbeider for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6f187-115">In the Worker field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="6f187-116">Velg arbeideren du vil bruke, i listen.</span><span class="sxs-lookup"><span data-stu-id="6f187-116">In the list, select the worker you want to use.</span></span>
7. <span data-ttu-id="6f187-117">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="6f187-117">Click Select.</span></span>
8. <span data-ttu-id="6f187-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="6f187-118">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="6f187-119">Opprette journallinjer</span><span class="sxs-lookup"><span data-stu-id="6f187-119">Create journal lines</span></span>
1. <span data-ttu-id="6f187-120">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6f187-120">Click New.</span></span>
2. <span data-ttu-id="6f187-121">Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6f187-121">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="6f187-122">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="6f187-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6f187-123">Hvis du bruker demonstrasjonsdataselskapet USMF, velger du "A0001".</span><span class="sxs-lookup"><span data-stu-id="6f187-123">If you are using demo data company USMF, select 'A0001'.</span></span>  
4. <span data-ttu-id="6f187-124">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6f187-124">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="6f187-125">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="6f187-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6f187-126">Hvis du bruker demonstrasjonsdataselskapet USMF, velger du område 2.</span><span class="sxs-lookup"><span data-stu-id="6f187-126">If you are using demo data company USMF, select site '2'.</span></span>  
6. <span data-ttu-id="6f187-127">Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6f187-127">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="6f187-128">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="6f187-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6f187-129">Hvis du bruker demonstrasjonsdataselskapet USMF, velger du lager 24.</span><span class="sxs-lookup"><span data-stu-id="6f187-129">If you are using demo data company USMF, select warehouse '24'.</span></span>  
8. <span data-ttu-id="6f187-130">Klikk rullegardinknappen i Lokasjon-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6f187-130">In the Location field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="6f187-131">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="6f187-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6f187-132">Hvis du bruker demonstrasjonsdataselskapet USMF, velger du lokasjon BULK-001.</span><span class="sxs-lookup"><span data-stu-id="6f187-132">If you are using demo data company USMF, select location 'BULK-001'</span></span>  
10. <span data-ttu-id="6f187-133">Angi et tall i feltet Opptelt.</span><span class="sxs-lookup"><span data-stu-id="6f187-133">In the Counted field, enter a number.</span></span>
    * <span data-ttu-id="6f187-134">Hvis du angir et opptelt nummer som er forskjellig fra nummeret som vises i feltet Beholdning, oppdateres feltet Antall for å vise avviket.</span><span class="sxs-lookup"><span data-stu-id="6f187-134">If you enter a counted number that’s different to the number shown in the On-hand field, the Quantity field is updated to show the discrepancy.</span></span>  
11. <span data-ttu-id="6f187-135">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6f187-135">Click Save.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="6f187-136">Postere lageropptellingsjournalen</span><span class="sxs-lookup"><span data-stu-id="6f187-136">Post the inventory counting journal</span></span>
1. <span data-ttu-id="6f187-137">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="6f187-137">Click Post.</span></span>
    * <span data-ttu-id="6f187-138">Når du posterer en lageropptellingsjournal, og hvis det opptelte beløpet er forskjellig fra beløpet som rapporteres i feltet Beholdning, blir det postert et lagermottak eller en lageravgang, lagernivå og lagerverdi endres og finanstransaksjoner blir generert.</span><span class="sxs-lookup"><span data-stu-id="6f187-138">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the On-hand field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
2. <span data-ttu-id="6f187-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="6f187-139">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="6f187-140">Vis lagertransaksjoner</span><span class="sxs-lookup"><span data-stu-id="6f187-140">View inventory transactions</span></span>
1. <span data-ttu-id="6f187-141">Klikk Lager.</span><span class="sxs-lookup"><span data-stu-id="6f187-141">Click Inventory.</span></span>
2. <span data-ttu-id="6f187-142">Klikk Transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="6f187-142">Click Transactions.</span></span>
    * <span data-ttu-id="6f187-143">Her kan du se relaterte transaksjoner som opprettes når du posterer lageropptellingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="6f187-143">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

