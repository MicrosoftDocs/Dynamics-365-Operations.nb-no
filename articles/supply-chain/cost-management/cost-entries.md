---
title: "Kostnadsoppføringer"
description: "Denne artikkelen inneholder informasjon om kostnadsoppføringer og når de opprettes. En kostnadsoppføring er en oppføring som registrerer antall og kostnad for en bestemt hendelse."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a61761a5c9d98befd67682e1790af5377b7a55e1
ms.openlocfilehash: 38fedcb2f482296b1c88dda98d34dd8b7debf555
ms.contentlocale: nb-no
ms.lasthandoff: 10/13/2017

---

# <a name="cost-entries"></a><span data-ttu-id="4564f-104">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="4564f-104">Cost entries</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4564f-105">Denne artikkelen inneholder informasjon om kostnadsoppføringer og når de opprettes.</span><span class="sxs-lookup"><span data-stu-id="4564f-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="4564f-106">En kostnadsoppføring er en oppføring som registrerer antall og kostnad for en bestemt hendelse.</span><span class="sxs-lookup"><span data-stu-id="4564f-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="4564f-107">Kostnadsoppføringer er aggregeringer av lagertransaksjoner som er registrert for aktive økonomiske lagerdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="4564f-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="4564f-108">Eksempler</span><span class="sxs-lookup"><span data-stu-id="4564f-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="4564f-109">Eksempel 1: Ingen kostnadsoppføringer opprettes</span><span class="sxs-lookup"><span data-stu-id="4564f-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="4564f-110">En overføringsjournalhendelse registreres.</span><span class="sxs-lookup"><span data-stu-id="4564f-110">A transfer journal event is registered.</span></span> <span data-ttu-id="4564f-111">Hendelsen overfører ett stykk av vare A fra lokasjon A til lokasjon B. Lokasjonslagerdimensjonen regnes ikke som en del av kostnadsobjektet.</span><span class="sxs-lookup"><span data-stu-id="4564f-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="4564f-112">Derfor oppretter hendelsen to lagertransaksjoner og ingen kostnadsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="4564f-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="4564f-113">Eksempel 2: Kostnadsoppføringer opprettes</span><span class="sxs-lookup"><span data-stu-id="4564f-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="4564f-114">En overføringsjournalhendelse registreres.</span><span class="sxs-lookup"><span data-stu-id="4564f-114">A transfer journal event is registered.</span></span> <span data-ttu-id="4564f-115">Hendelsen overfører ett stykk av vare A fra område 1 til område 2.</span><span class="sxs-lookup"><span data-stu-id="4564f-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="4564f-116">Områdelagerdimensjonen regnes som en del av kostnadsobjektet.</span><span class="sxs-lookup"><span data-stu-id="4564f-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="4564f-117">Derfor oppretter hendelsen to lagertransaksjoner og to kostnadsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="4564f-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="4564f-118">Eksempel 3: Én kostnadsoppføring opprettes</span><span class="sxs-lookup"><span data-stu-id="4564f-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="4564f-119">En produktkvitteringshendelse registreres for en bestilling.</span><span class="sxs-lookup"><span data-stu-id="4564f-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="4564f-120">Hendelsen registrerer 100 stykk av vare A med en enhetskostnad på NOK 100,00.</span><span class="sxs-lookup"><span data-stu-id="4564f-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="4564f-121">Siden vare A bruker et serienummer til å spore formålet med lagerstyring, opprettes et unikt serienummer for hver vare som mottas.</span><span class="sxs-lookup"><span data-stu-id="4564f-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="4564f-122">Derfor oppretter hendelsen 100 lagertransaksjoner og én kostnadsoppføring.</span><span class="sxs-lookup"><span data-stu-id="4564f-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="4564f-123">Kostnadsoppføringer-siden</span><span class="sxs-lookup"><span data-stu-id="4564f-123">Cost entries page</span></span>
<span data-ttu-id="4564f-124">Den nye **Kostnadsoppføringer**-siden lar deg vise og styre registrering av antall og kostnader.</span><span class="sxs-lookup"><span data-stu-id="4564f-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="4564f-125">Denne siden kompletterer sidene **Lagertransaksjon** og **Lagerutligning**.</span><span class="sxs-lookup"><span data-stu-id="4564f-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="4564f-126">Poster registreres i kronologisk rekkefølge for en hendelse.</span><span class="sxs-lookup"><span data-stu-id="4564f-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="4564f-127">Derfor kan du raskt finne og styre de akkumulerte kostnadene for en bestemt hendelse eller alle hendelsene som er knyttet til et dokument.</span><span class="sxs-lookup"><span data-stu-id="4564f-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="4564f-128">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="4564f-128">Here is an example:</span></span>

-   <span data-ttu-id="4564f-129">En produktkvitteringshendelse er registrert for vare A. 100 stykker mottas med en enhetskostnad på NOK 100,00.</span><span class="sxs-lookup"><span data-stu-id="4564f-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="4564f-130">Noen dager etter at fakturahendelsen er registrert, øker kostnadene til NOK 110,00.</span><span class="sxs-lookup"><span data-stu-id="4564f-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="4564f-131">Derfor er totalbeløpet NOK 11 000.</span><span class="sxs-lookup"><span data-stu-id="4564f-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="4564f-132">Det opprettes et andre bilag for å gjøre rede for differansen på NOK 1 000.</span><span class="sxs-lookup"><span data-stu-id="4564f-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="4564f-133">Noen dager senere registreres et tilleggsgebyr på NOK 150,00 på bestillingen for å dekke transportkostnadene.</span><span class="sxs-lookup"><span data-stu-id="4564f-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="4564f-134">Bilag</span><span class="sxs-lookup"><span data-stu-id="4564f-134">Voucher</span></span> | <span data-ttu-id="4564f-135">Dato</span><span class="sxs-lookup"><span data-stu-id="4564f-135">Date</span></span>       | <span data-ttu-id="4564f-136">Referanse</span><span class="sxs-lookup"><span data-stu-id="4564f-136">Reference</span></span>      | <span data-ttu-id="4564f-137">Tall</span><span class="sxs-lookup"><span data-stu-id="4564f-137">Number</span></span> | <span data-ttu-id="4564f-138">Parti-ID</span><span class="sxs-lookup"><span data-stu-id="4564f-138">Lot ID</span></span>  | <span data-ttu-id="4564f-139">Antall</span><span class="sxs-lookup"><span data-stu-id="4564f-139">Quantity</span></span> | <span data-ttu-id="4564f-140">Beløp</span><span class="sxs-lookup"><span data-stu-id="4564f-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="4564f-141">00001</span><span class="sxs-lookup"><span data-stu-id="4564f-141">00001</span></span>   | <span data-ttu-id="4564f-142">01.01.2015</span><span class="sxs-lookup"><span data-stu-id="4564f-142">01-01-2015</span></span> | <span data-ttu-id="4564f-143">Bestilling</span><span class="sxs-lookup"><span data-stu-id="4564f-143">Purchase order</span></span> | <span data-ttu-id="4564f-144">100001</span><span class="sxs-lookup"><span data-stu-id="4564f-144">100001</span></span> | <span data-ttu-id="4564f-145">0000101</span><span class="sxs-lookup"><span data-stu-id="4564f-145">0000101</span></span> | <span data-ttu-id="4564f-146">1 00,00</span><span class="sxs-lookup"><span data-stu-id="4564f-146">100.00</span></span>   | <span data-ttu-id="4564f-147">1000,00</span><span class="sxs-lookup"><span data-stu-id="4564f-147">1000.00</span></span> |
| <span data-ttu-id="4564f-148">00002</span><span class="sxs-lookup"><span data-stu-id="4564f-148">00002</span></span>   | <span data-ttu-id="4564f-149">20.01.2015</span><span class="sxs-lookup"><span data-stu-id="4564f-149">20-01-2015</span></span> | <span data-ttu-id="4564f-150">Bestilling</span><span class="sxs-lookup"><span data-stu-id="4564f-150">Purchase order</span></span> | <span data-ttu-id="4564f-151">100001</span><span class="sxs-lookup"><span data-stu-id="4564f-151">100001</span></span> | <span data-ttu-id="4564f-152">0000101</span><span class="sxs-lookup"><span data-stu-id="4564f-152">0000101</span></span> |          | <span data-ttu-id="4564f-153">100,00</span><span class="sxs-lookup"><span data-stu-id="4564f-153">100.00</span></span>  |
| <span data-ttu-id="4564f-154">00003</span><span class="sxs-lookup"><span data-stu-id="4564f-154">00003</span></span>   | <span data-ttu-id="4564f-155">31.01.2015</span><span class="sxs-lookup"><span data-stu-id="4564f-155">31-01-2015</span></span> | <span data-ttu-id="4564f-156">Justering</span><span class="sxs-lookup"><span data-stu-id="4564f-156">Adjustment</span></span>     | <span data-ttu-id="4564f-157">100001</span><span class="sxs-lookup"><span data-stu-id="4564f-157">100001</span></span> | <span data-ttu-id="4564f-158">0000101</span><span class="sxs-lookup"><span data-stu-id="4564f-158">0000101</span></span> |          | <span data-ttu-id="4564f-159">15,00</span><span class="sxs-lookup"><span data-stu-id="4564f-159">15.00</span></span>   |

<span data-ttu-id="4564f-160">**Kostnadsoppføringer**-siden aktiverer filtrering etter dokument-ID og dokumentdato.</span><span class="sxs-lookup"><span data-stu-id="4564f-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="4564f-161">Kostnadsoppføringer er bare tilgjengelige for [kostnadsobjekter](cost-object.md) eller frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="4564f-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

<a name="see-also"></a><span data-ttu-id="4564f-162">Se også</span><span class="sxs-lookup"><span data-stu-id="4564f-162">See also</span></span>
--------

[<span data-ttu-id="4564f-163">Kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="4564f-163">Cost objects</span></span>](cost-object.md)




