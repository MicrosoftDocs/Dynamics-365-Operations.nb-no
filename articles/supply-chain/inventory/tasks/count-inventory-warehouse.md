---
title: Lageropptelling på et lager
description: Dette emnet beskriver prosessen med å opprette og postere en lageropptellingsjournal for å telle en bestemt vare på en lokasjon i lageret.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34013783bab79d80f1dac9a7806042608635e617
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204177"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="125e1-103">Lageropptelling på et lager</span><span class="sxs-lookup"><span data-stu-id="125e1-103">Count inventory in a warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="125e1-104">Dette emnet beskriver prosessen med å opprette og postere en lageropptellingsjournal for å telle en bestemt vare på en lokasjon i lageret.</span><span class="sxs-lookup"><span data-stu-id="125e1-104">This topic describes the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="125e1-105">Fremgangsmåten gjelder for "grunnleggende lageraktiviteter"-funksjoner, tilgjengelige i lagerstyringsmodulen, ikke for lagerstyringsfunksjonaliteten som er tilgjengelig i lagerstyringsmodulen.</span><span class="sxs-lookup"><span data-stu-id="125e1-105">The procedure applies to "basic warehousing" functionality, available in the Inventory management module, not to the warehousing functionality that's available in the Warehouse management module.</span></span> <span data-ttu-id="125e1-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="125e1-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="125e1-107">Hvis du bruker dine egne data, må du kontrollere at du har produkter og lokasjoner definert, og at du har opprettet et beholdningsjournalnavn for opptellingsjournaler.</span><span class="sxs-lookup"><span data-stu-id="125e1-107">If you're using your own data, make sure that you have products and locations set up, and that you've created an inventory journal name for counting journals.</span></span> <span data-ttu-id="125e1-108">Beholdningsopptelling utføres vanligvis av en lageransatt.</span><span class="sxs-lookup"><span data-stu-id="125e1-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="125e1-109">Opprette en lageropptellingsjournal</span><span class="sxs-lookup"><span data-stu-id="125e1-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="125e1-110">Gå til **Navigasjonsrute > Moduler > Lagerstyring > Loggoppføringer > Vareopptelling > Opptelling**.</span><span class="sxs-lookup"><span data-stu-id="125e1-110">Go to **Navigation pane > Modules > Inventory management > Journal entries > Item counting > Counting**.</span></span>
2. <span data-ttu-id="125e1-111">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="125e1-111">Select **New**.</span></span>
3. <span data-ttu-id="125e1-112">I **Navn**-feltet velger du navnet på lageropptellingsjournalen du vil bruke, fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="125e1-112">In the **Name** field, select the inventory counting journal name you want to use from the drop-down list.</span></span> <span data-ttu-id="125e1-113">Noen andre felt fylles ut basert på oppsettet av standardnavn for lageropptellingsjournal som du velger.</span><span class="sxs-lookup"><span data-stu-id="125e1-113">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
4. <span data-ttu-id="125e1-114">Klikk rullegardinknappen i feltet **Arbeider** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="125e1-114">In the **Worker** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="125e1-115">**Velg** arbeideren du vil bruke, i listen.</span><span class="sxs-lookup"><span data-stu-id="125e1-115">In the list, **Select** the worker you want to use.</span></span>
6. <span data-ttu-id="125e1-116">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="125e1-116">Select **OK**.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="125e1-117">Opprette journallinjer</span><span class="sxs-lookup"><span data-stu-id="125e1-117">Create journal lines</span></span>
1. <span data-ttu-id="125e1-118">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="125e1-118">Select **New**.</span></span>
2. <span data-ttu-id="125e1-119">Velg det ønskede oppslaget fra rullegardinlisten i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="125e1-119">In the **Item number** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="125e1-120">Hvis du bruker demonstrasjonsdataselskapet USMF, velger du **A0001**.</span><span class="sxs-lookup"><span data-stu-id="125e1-120">If you are using demo data company USMF, select **A0001**.</span></span>  
3. <span data-ttu-id="125e1-121">Velg det ønskede oppslaget fra rullegardinlisten i **Område**-feltet.</span><span class="sxs-lookup"><span data-stu-id="125e1-121">In the **Site** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="125e1-122">Hvis du bruker demonstrasjonsdataselskapet USMF, velger du område **2**.</span><span class="sxs-lookup"><span data-stu-id="125e1-122">If you are using demo data company USMF, select site **2**.</span></span>
4. <span data-ttu-id="125e1-123">Velg det ønskede oppslaget fra rullegardinlisten i **Lager**-feltet.</span><span class="sxs-lookup"><span data-stu-id="125e1-123">In the **Warehouse** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="125e1-124">Hvis du bruker demonstrasjonsdataselskapet USMF, velger du lager **24**.</span><span class="sxs-lookup"><span data-stu-id="125e1-124">If you are using demo data company USMF, select warehouse **24**.</span></span>  
5. <span data-ttu-id="125e1-125">Velg det ønskede oppslaget fra rullegardinlisten i **Sted**-feltet.</span><span class="sxs-lookup"><span data-stu-id="125e1-125">In the **Location** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="125e1-126">Hvis du bruker demonstrasjonsdataselskapet USMF, velger du lokasjon **BULK-001**.</span><span class="sxs-lookup"><span data-stu-id="125e1-126">If you are using demo data company USMF, select location **BULK-001**.</span></span>  
6. <span data-ttu-id="125e1-127">Angi et tall i feltet Opptelt.</span><span class="sxs-lookup"><span data-stu-id="125e1-127">In the Counted field, enter a number.</span></span> <span data-ttu-id="125e1-128">Hvis du angir et opptelt nummer som er forskjellig fra nummeret som vises i feltet **Beholdning**, oppdateres feltet **Antall** for å vise avviket.</span><span class="sxs-lookup"><span data-stu-id="125e1-128">If you enter a counted number that's different to the number shown in the **On-hand** field, the **Quantity** field is updated to show the discrepancy.</span></span>  
7. <span data-ttu-id="125e1-129">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="125e1-129">Select **Save**.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="125e1-130">Postere lageropptellingsjournalen</span><span class="sxs-lookup"><span data-stu-id="125e1-130">Post the inventory counting journal</span></span>
1. <span data-ttu-id="125e1-131">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="125e1-131">Select **Post**.</span></span> <span data-ttu-id="125e1-132">Når du posterer en lageropptellingsjournal, og hvis det opptelte beløpet er forskjellig fra beløpet som rapporteres i feltet **Beholdning**, blir det postert et lagermottak eller en lageravgang, lagernivå og lagerverdi endres og finanstransaksjoner blir generert.</span><span class="sxs-lookup"><span data-stu-id="125e1-132">When you post an inventory counting journal, if the counted amount differs from amount that's reported in the **On-hand** field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>
2. <span data-ttu-id="125e1-133">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="125e1-133">Select **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="125e1-134">Vis lagertransaksjoner</span><span class="sxs-lookup"><span data-stu-id="125e1-134">View inventory transactions</span></span>
1. <span data-ttu-id="125e1-135">Velg **Lager**.</span><span class="sxs-lookup"><span data-stu-id="125e1-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="125e1-136">Velg **Transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="125e1-136">Select **Transactions**.</span></span> <span data-ttu-id="125e1-137">Her kan du se relaterte transaksjoner som opprettes når du posterer lageropptellingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="125e1-137">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

