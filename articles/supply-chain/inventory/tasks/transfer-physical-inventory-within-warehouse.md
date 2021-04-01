---
title: Overføre aktuell beholdning på lageret
description: Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for registrere flytting av en vare fra en lokasjon i et lager til en annen.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b745308aca2503b31d7d24d7cac693bb803fc6ab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244261"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="d0456-103">Overføre aktuell beholdning på lageret</span><span class="sxs-lookup"><span data-stu-id="d0456-103">Transfer physical inventory within the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d0456-104">Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for registrere flytting av en vare fra en lokasjon i et lager til en annen.</span><span class="sxs-lookup"><span data-stu-id="d0456-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="d0456-105">Du må ha en lagerjournalnavn definert for lageroverføringer før du starter dette.</span><span class="sxs-lookup"><span data-stu-id="d0456-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="d0456-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsdataselskapet USMF ved hjelp av eksempelverdiene som vises, eller du kan bruke dine egne data hvis du har produkter og lokasjoner definert.</span><span class="sxs-lookup"><span data-stu-id="d0456-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="d0456-107">Disse oppgavene vil vanligvis utføres av en lageransatt.</span><span class="sxs-lookup"><span data-stu-id="d0456-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="d0456-108">Opprette en beholdningsoverføringsjournal</span><span class="sxs-lookup"><span data-stu-id="d0456-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="d0456-109">I **navigasjonsruten** går du til **Beholdningsstyring > Journaloppføringer > Varer > Overføring**.</span><span class="sxs-lookup"><span data-stu-id="d0456-109">In the **Navigation pane**, go to **Inventory management > Journal entries > Items > Transfer**.</span></span>
2. <span data-ttu-id="d0456-110">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d0456-110">Click **New**.</span></span>
3. <span data-ttu-id="d0456-111">Angi eller velg en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d0456-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="d0456-112">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0456-112">Click **OK**.</span></span> <span data-ttu-id="d0456-113">Det er muligheten til å angi Fra- og Til-dimensjoner for hver journallinje.</span><span class="sxs-lookup"><span data-stu-id="d0456-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="d0456-114">Disse er nødvendige for denne journaltypen.</span><span class="sxs-lookup"><span data-stu-id="d0456-114">These are essential for this journal type.</span></span> <span data-ttu-id="d0456-115">Du kan overføre varer til lokasjoner ved hjelp av andre regler.</span><span class="sxs-lookup"><span data-stu-id="d0456-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="d0456-116">I dette eksemplet skal vi overføre en vare innenfor samme lager, fra en nummerskiltkontrollert lokasjon til en lokasjon som ikke er nummerskiltkontrollert.</span><span class="sxs-lookup"><span data-stu-id="d0456-116">In this example we'll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="d0456-117">Opprette journallinjer</span><span class="sxs-lookup"><span data-stu-id="d0456-117">Create journal lines</span></span>
1. <span data-ttu-id="d0456-118">Klikk på **Ny** i hurtigfanen **Journallinjer**.</span><span class="sxs-lookup"><span data-stu-id="d0456-118">Int the **Journal lines fastTab**, click **New**.</span></span>
2. <span data-ttu-id="d0456-119">Angi eller velg en verdi i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d0456-119">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="d0456-120">Hvis du bruker USMF, kan du velge 'A0001'.</span><span class="sxs-lookup"><span data-stu-id="d0456-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="d0456-121">Angi eller velg en verdi i feltet **Fra site**.</span><span class="sxs-lookup"><span data-stu-id="d0456-121">In the **From site** field, enter or select a value.</span></span> <span data-ttu-id="d0456-122">Hvis du bruker USMF, kan du velge 2.</span><span class="sxs-lookup"><span data-stu-id="d0456-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="d0456-123">Angi eller velg en verdi i feltet **Til site**.</span><span class="sxs-lookup"><span data-stu-id="d0456-123">In the **To site** field, enter or select a value.</span></span> <span data-ttu-id="d0456-124">Hvis du bruker USMF, kan du velge 2.</span><span class="sxs-lookup"><span data-stu-id="d0456-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="d0456-125">Angi eller velg en verdi i feltet **Fra lager**.</span><span class="sxs-lookup"><span data-stu-id="d0456-125">In the **From warehouse** field, enter or select a value.</span></span> <span data-ttu-id="d0456-126">Hvis du bruker USMF, kan du velge 24.</span><span class="sxs-lookup"><span data-stu-id="d0456-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="d0456-127">Angi eller velg en verdi i feltet **Til lager**.</span><span class="sxs-lookup"><span data-stu-id="d0456-127">In the **To warehouse** field, enter or select a value.</span></span> <span data-ttu-id="d0456-128">Hvis du bruker USMF, kan du velge 24.</span><span class="sxs-lookup"><span data-stu-id="d0456-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="d0456-129">Angi eller velg en verdi i **Fra lokasjon**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d0456-129">In the **From location** field, enter or select a value.</span></span> <span data-ttu-id="d0456-130">Hvis du bruker USMF, kan du velge FL-001.</span><span class="sxs-lookup"><span data-stu-id="d0456-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="d0456-131">Angi eller velg en verdi i **Til lokasjon**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d0456-131">In the **To location** field, enter or select a value.</span></span> <span data-ttu-id="d0456-132">Hvis du bruker USMF, kan du velge BULK-001.</span><span class="sxs-lookup"><span data-stu-id="d0456-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="d0456-133">Angi et tall i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d0456-133">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="d0456-134">Klikk på fanen **Lagerdimensjoner** i hurtigfanen **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="d0456-134">In the **Line details** fastTab, click the **Inventory dimensions** tab.</span></span>
11. <span data-ttu-id="d0456-135">Angi eller velg en verdi i **Nummerskilt**-feltet i **Fra lagerdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="d0456-135">In **From inventory dimensions**, in the **License plate** field, enter or select a value.</span></span> <span data-ttu-id="d0456-136">Hvis du bruker USMF, kan du velge 24.</span><span class="sxs-lookup"><span data-stu-id="d0456-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="d0456-137">Klikk på **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="d0456-137">Click **Save**.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="d0456-138">Postere beholdningsoverføringsjournalen</span><span class="sxs-lookup"><span data-stu-id="d0456-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="d0456-139">Klikk på **Poster** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="d0456-139">On the **Action Pane**, click **Post**.</span></span>
2. <span data-ttu-id="d0456-140">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0456-140">Click **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="d0456-141">Vis lagertransaksjoner</span><span class="sxs-lookup"><span data-stu-id="d0456-141">View inventory transactions</span></span>
1. <span data-ttu-id="d0456-142">Klikk på **Beholdning**.</span><span class="sxs-lookup"><span data-stu-id="d0456-142">Click **Inventory**.</span></span>
2. <span data-ttu-id="d0456-143">Klikk på **Transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="d0456-143">Click **Transactions**.</span></span> <span data-ttu-id="d0456-144">Her kan du se transaksjonene som ble opprettet da du posterte journalen.</span><span class="sxs-lookup"><span data-stu-id="d0456-144">Here you can see the transactions that were created when you posted your journal.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]