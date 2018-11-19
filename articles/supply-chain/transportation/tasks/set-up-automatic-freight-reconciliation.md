--- 
title: Definere automatisk fraktavstemming
description: "Denne fremgangsmåten viser hvordan du setter opp data for automatisk fraktavstemming."
author: ShylaThompson
manager: AnnBe
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d990efd7c929b15d57d64e850bc3308349abb978
ms.openlocfilehash: b7772ad779495b36941a3dc86cc456d80a964467
ms.contentlocale: nb-no
ms.lasthandoff: 10/17/2018

---
# <a name="set-up-automatic-freight-reconciliation"></a><span data-ttu-id="37fd9-103">Definere automatisk fraktavstemming</span><span class="sxs-lookup"><span data-stu-id="37fd9-103">Set up automatic freight reconciliation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37fd9-104">Denne fremgangsmåten viser hvordan du setter opp data for automatisk fraktavstemming.</span><span class="sxs-lookup"><span data-stu-id="37fd9-104">This procedure shows how to set up data for automatic freight reconciliation.</span></span> <span data-ttu-id="37fd9-105">Dette gjøres vanligvis av en lagersjef.</span><span class="sxs-lookup"><span data-stu-id="37fd9-105">This is typically done by a warehouse manager.</span></span> <span data-ttu-id="37fd9-106">Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="37fd9-106">You can use this procedure in demo data company USMF.</span></span>


## <a name="set-up-the-freight-bill-type"></a><span data-ttu-id="37fd9-107">Definere fraktbrevtypen</span><span class="sxs-lookup"><span data-stu-id="37fd9-107">Set up the freight bill type</span></span>
1. <span data-ttu-id="37fd9-108">Gå til Transportstyring > Oppsett > Fraktavstemming > Fraktbrevtype.</span><span class="sxs-lookup"><span data-stu-id="37fd9-108">Go to Transportation management > Setup > Freight reconciliation > Freight bill type.</span></span>
    * <span data-ttu-id="37fd9-109">Fraktbrevtypen definerer hvordan fraktbrev og transportørfakturaer skal sammenlignes.</span><span class="sxs-lookup"><span data-stu-id="37fd9-109">The freight bill type defines how freight bills and carrier invoices  should be matched.</span></span>  
2. <span data-ttu-id="37fd9-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="37fd9-110">Click New.</span></span>
3. <span data-ttu-id="37fd9-111">Skriv inn en verdi i feltet Fraktbrevtype.</span><span class="sxs-lookup"><span data-stu-id="37fd9-111">In the Freight bill type field, type a value.</span></span>
4. <span data-ttu-id="37fd9-112">I Motormontering-feltet skriver du inn Microsoft.Dynamics.Ax.Tms.dll.</span><span class="sxs-lookup"><span data-stu-id="37fd9-112">In the Engine assembly field, type 'Microsoft.Dynamics.Ax.Tms.dll'.</span></span>
    * <span data-ttu-id="37fd9-113">Dette er standard kodebibliotek for samsvarsmotoren for transportstyring.</span><span class="sxs-lookup"><span data-stu-id="37fd9-113">This is the standard Transportation management matching engine code library.</span></span>  
5. <span data-ttu-id="37fd9-114">I Motorklasse-feltet skriver du inn Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer.</span><span class="sxs-lookup"><span data-stu-id="37fd9-114">In the Engine class field, type 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span></span>
    * <span data-ttu-id="37fd9-115">Dette er standard klasse for samsvarsmotoren for transportstyring.</span><span class="sxs-lookup"><span data-stu-id="37fd9-115">This is the standard Transportation management matching engine class.</span></span>  
6. <span data-ttu-id="37fd9-116">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="37fd9-116">Click New.</span></span>
7. <span data-ttu-id="37fd9-117">I Beskrivelse-feltet velger du verdien som skal samsvare på fraktbrevet og transportørfakturaen.</span><span class="sxs-lookup"><span data-stu-id="37fd9-117">In the Description field, choose the value that should match on the freight bill and the carrier invoice.</span></span>  
8. <span data-ttu-id="37fd9-118">I feltet Samsvar nødvendig velger du Ja.</span><span class="sxs-lookup"><span data-stu-id="37fd9-118">In the Match required field, select 'Yes'.</span></span>
    * <span data-ttu-id="37fd9-119">Hvis du setter dette feltet til Ja, betyr det at verdien som er valgt i Beskrivelse-feltet, må samsvare med både fraktbrevet og transportørfakturaen.</span><span class="sxs-lookup"><span data-stu-id="37fd9-119">If you set this field to Yes this means that the value selected in the Description field needs to match on both the freight bill and the carrier invoice.</span></span> <span data-ttu-id="37fd9-120">Hvis du setter det til Nei, kan feltet være tomt på én av disse.</span><span class="sxs-lookup"><span data-stu-id="37fd9-120">If you set it to No, the field can be blank on one of these.</span></span>  
9. <span data-ttu-id="37fd9-121">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="37fd9-121">Click Save.</span></span>

## <a name="set-up-the-freight-bill-type-assignment"></a><span data-ttu-id="37fd9-122">Definere tilordningen av fraktbrevtype</span><span class="sxs-lookup"><span data-stu-id="37fd9-122">Set up the freight bill type assignment</span></span>
1. <span data-ttu-id="37fd9-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="37fd9-123">Close the page.</span></span>
2. <span data-ttu-id="37fd9-124">Gå til Transportstyring > Oppsett > Fraktavstemming > Tilordninger av fraktbrevtype.</span><span class="sxs-lookup"><span data-stu-id="37fd9-124">Go to Transportation management > Setup > Freight reconciliation > Freight bill type assignments.</span></span>
    * <span data-ttu-id="37fd9-125">Fraktbrevtypetilordningen brukes til å angi hvilken fraktbrevtype som skal brukes for en bestemt transportør.</span><span class="sxs-lookup"><span data-stu-id="37fd9-125">The freight bill type assignment is used to specify which freight bill type is used for a particular carrier.</span></span>   
3. <span data-ttu-id="37fd9-126">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="37fd9-126">Click New.</span></span>
4. <span data-ttu-id="37fd9-127">Angi eller velg en verdi i feltet Modus.</span><span class="sxs-lookup"><span data-stu-id="37fd9-127">In the Mode field, enter or select a value.</span></span>
5. <span data-ttu-id="37fd9-128">Angi eller velg en verdi i feltet Transportør.</span><span class="sxs-lookup"><span data-stu-id="37fd9-128">In the Shipping carrier field, enter or select a value.</span></span>
6. <span data-ttu-id="37fd9-129">I Fraktbrevtype-feltet velger du fraktbrevtypen du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="37fd9-129">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
7. <span data-ttu-id="37fd9-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="37fd9-130">Close the page.</span></span>

## <a name="set-up-the-audit-master"></a><span data-ttu-id="37fd9-131">Konfigurere revisjonsstandarden</span><span class="sxs-lookup"><span data-stu-id="37fd9-131">Set up the audit master</span></span>
1. <span data-ttu-id="37fd9-132">Gå til Transportstyring > Oppsett > Fraktavstemming > Revisjonsstandard.</span><span class="sxs-lookup"><span data-stu-id="37fd9-132">Go to Transportation management > Setup > Freight reconciliation > Audit master.</span></span>
    * <span data-ttu-id="37fd9-133">Revisjonsstandarden definerer toleransegrensene for automatisk fraktavstemming.</span><span class="sxs-lookup"><span data-stu-id="37fd9-133">The audit master defines the tolerance limits for automatic freight reconciliation.</span></span> <span data-ttu-id="37fd9-134">Den angir hvor stor forskjell det kan være mellom pengebeløpet på fraktbrevet og transportørfakturaen og likevel tillate avstemming.</span><span class="sxs-lookup"><span data-stu-id="37fd9-134">It specifies by how much the monetary amounts on the freight bill and the carrier invoice can differ and still allow reconciliation to occur.</span></span> <span data-ttu-id="37fd9-135">Den definerer også hvordan avvik skal håndteres.</span><span class="sxs-lookup"><span data-stu-id="37fd9-135">It also defines how to handle discrepancies.</span></span>  
2. <span data-ttu-id="37fd9-136">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="37fd9-136">Click New.</span></span>
3. <span data-ttu-id="37fd9-137">Angi en verdi i feltet Revisjonsstandard-ID.</span><span class="sxs-lookup"><span data-stu-id="37fd9-137">In the Audit master ID field, type a value.</span></span>
4. <span data-ttu-id="37fd9-138">Velg samme transportør som du gjorde tidligere, i feltet Transportør.</span><span class="sxs-lookup"><span data-stu-id="37fd9-138">In the Shipping carrier  field, select the same shipping carrier as you did earlier.</span></span>
5. <span data-ttu-id="37fd9-139">I Fraktbrevtype-feltet velger du fraktbrevtypen du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="37fd9-139">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
6. <span data-ttu-id="37fd9-140">Utvid delen Toleranse.</span><span class="sxs-lookup"><span data-stu-id="37fd9-140">Expand the Tolerance section.</span></span>
7. <span data-ttu-id="37fd9-141">Angi et tall i feltet Minste toleransenivå.</span><span class="sxs-lookup"><span data-stu-id="37fd9-141">In the Minimum tolerance level field, enter a number.</span></span>
8. <span data-ttu-id="37fd9-142">Angi et tall i feltet Største toleransenivå.</span><span class="sxs-lookup"><span data-stu-id="37fd9-142">In the Maximum tolerance level field, enter a number.</span></span>
9. <span data-ttu-id="37fd9-143">Utvid delen Resultat.</span><span class="sxs-lookup"><span data-stu-id="37fd9-143">Expand the Result section.</span></span>
10. <span data-ttu-id="37fd9-144">Angi eller velg en verdi i feltet Årsakskode for overbetaling.</span><span class="sxs-lookup"><span data-stu-id="37fd9-144">In the Overpayment reason code field, enter or select a value.</span></span>
    * <span data-ttu-id="37fd9-145">Hvis pengebeløpene er forskjellige på fraktbrevet og transportørfakturaen, angir årsakskodene for over- og underbetaling kontoene som forskjellen skal registreres på, så lenge differansen er innenfor toleransenivåene.</span><span class="sxs-lookup"><span data-stu-id="37fd9-145">If the monetary amounts differ on the freight bill and the carrier invoice, the overpayment and underpayment reason codes specify the accounts that the difference should be registered on, as long as the difference is within the tolerance levels.</span></span>  
11. <span data-ttu-id="37fd9-146">Angi eller velg en verdi i feltet Årsakskode for underbetaling.</span><span class="sxs-lookup"><span data-stu-id="37fd9-146">In the Underpayment reason code field, enter or select a value.</span></span>
12. <span data-ttu-id="37fd9-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="37fd9-147">Close the page.</span></span>


