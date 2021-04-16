---
title: Justere lagernivåer i lageret (grunnleggende lageraktiviteter)
description: Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en beholdningsjusteringsjournal for å justere lagernivåer for produkter i lageret.
author: MarkusFogelberg
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bba1df70cd23a29ddffad96a4a581154619dc74
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834151"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="6208d-103">Justere lagernivåer i lageret (grunnleggende lageraktiviteter)</span><span class="sxs-lookup"><span data-stu-id="6208d-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6208d-104">Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en beholdningsjusteringsjournal for å justere lagernivåer for produkter i lageret.</span><span class="sxs-lookup"><span data-stu-id="6208d-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="6208d-105">Du må ha en lagerjournalnavn definert for lagerjusteringer før du starter dette.</span><span class="sxs-lookup"><span data-stu-id="6208d-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="6208d-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="6208d-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="6208d-107">Disse oppgavene vil vanligvis utføres av en lageransatt.</span><span class="sxs-lookup"><span data-stu-id="6208d-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="6208d-108">Opprette en beholdningsjusteringsjournal</span><span class="sxs-lookup"><span data-stu-id="6208d-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="6208d-109">Gå til Lagerstyring > Journaloppføringer > Varer > Beholdningsjustering.</span><span class="sxs-lookup"><span data-stu-id="6208d-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="6208d-110">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="6208d-110">Click New.</span></span>
3. <span data-ttu-id="6208d-111">Klikk på rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6208d-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6208d-112">Klikk på journalnavnet for beholdningsjustering som du vil bruke, i listen.</span><span class="sxs-lookup"><span data-stu-id="6208d-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="6208d-113">Noen andre felt fylles ut basert på oppsettet av navnet på lagerjusteringsjournal som du velger.</span><span class="sxs-lookup"><span data-stu-id="6208d-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="6208d-114">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="6208d-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="6208d-115">Opprette journallinjer</span><span class="sxs-lookup"><span data-stu-id="6208d-115">Create journal lines</span></span>
1. <span data-ttu-id="6208d-116">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="6208d-116">Click New.</span></span>
2. <span data-ttu-id="6208d-117">Merk varenummerfeltet i listen.</span><span class="sxs-lookup"><span data-stu-id="6208d-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="6208d-118">Velg en vare i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="6208d-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="6208d-119">Hvis du bruker demonstrasjonsdataselskapet USMF, skriver du inn "D0001".</span><span class="sxs-lookup"><span data-stu-id="6208d-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="6208d-120">Klikk på rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6208d-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="6208d-121">Velg et område i listen.</span><span class="sxs-lookup"><span data-stu-id="6208d-121">In the list, select a site.</span></span>
6. <span data-ttu-id="6208d-122">Klikk på rullegardinknappen i Lager-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6208d-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="6208d-123">Velg et lager i listen.</span><span class="sxs-lookup"><span data-stu-id="6208d-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="6208d-124">Hvis du har valgt en vare med Lokasjon som en obligatorisk dimensjon, må du angi lokasjonen her.</span><span class="sxs-lookup"><span data-stu-id="6208d-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="6208d-125">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="6208d-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="6208d-126">Kostprisfeltet angir kostnaden per enhet for lagertilganger.</span><span class="sxs-lookup"><span data-stu-id="6208d-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="6208d-127">Hvis kostnaden ikke er angitt for varenummeret, eller hvis du vil endre den manuelt, gjør du det her.</span><span class="sxs-lookup"><span data-stu-id="6208d-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="6208d-128">Validere og postere beholdningsjusteringsjournalen</span><span class="sxs-lookup"><span data-stu-id="6208d-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="6208d-129">Klikk på Valider.</span><span class="sxs-lookup"><span data-stu-id="6208d-129">Click Validate.</span></span>
2. <span data-ttu-id="6208d-130">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="6208d-130">Click OK.</span></span>
3. <span data-ttu-id="6208d-131">Klikk på Poster.</span><span class="sxs-lookup"><span data-stu-id="6208d-131">Click Post.</span></span>
    * <span data-ttu-id="6208d-132">Når du posterer denne typen journal, blir det postert et lagermottak eller en lageravgang, lagernivå og lagerverdi endres og finanstransaksjoner blir generert.</span><span class="sxs-lookup"><span data-stu-id="6208d-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="6208d-133">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="6208d-133">Click OK.</span></span>
5. <span data-ttu-id="6208d-134">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="6208d-134">Close the form.</span></span>
6. <span data-ttu-id="6208d-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6208d-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]