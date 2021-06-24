---
title: Kostnadsoppføringer
description: Denne artikkelen inneholder informasjon om kostnadsoppføringer og når de opprettes. En kostnadsoppføring er en oppføring som registrerer antall og kostnad for en bestemt hendelse.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b258e111139f52f5ccf3ea3f385a1367576eacd
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188542"
---
# <a name="cost-entries"></a><span data-ttu-id="694c9-104">Kostnadsoppføringer</span><span class="sxs-lookup"><span data-stu-id="694c9-104">Cost entries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="694c9-105">Denne artikkelen inneholder informasjon om kostnadsoppføringer og når de opprettes.</span><span class="sxs-lookup"><span data-stu-id="694c9-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="694c9-106">En kostnadsoppføring er en oppføring som registrerer antall og kostnad for en bestemt hendelse.</span><span class="sxs-lookup"><span data-stu-id="694c9-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="694c9-107">Kostnadsoppføringer er aggregeringer av lagertransaksjoner som er registrert for aktive økonomiske lagerdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="694c9-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="694c9-108">Eksempler</span><span class="sxs-lookup"><span data-stu-id="694c9-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="694c9-109">Eksempel 1: Ingen kostnadsoppføringer opprettes</span><span class="sxs-lookup"><span data-stu-id="694c9-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="694c9-110">En overføringsjournalhendelse registreres.</span><span class="sxs-lookup"><span data-stu-id="694c9-110">A transfer journal event is registered.</span></span> <span data-ttu-id="694c9-111">Hendelsen overfører ett stykk av vare A fra lokasjon A til lokasjon B. Lokasjonslagerdimensjonen regnes ikke som en del av kostnadsobjektet.</span><span class="sxs-lookup"><span data-stu-id="694c9-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="694c9-112">Derfor oppretter hendelsen to lagertransaksjoner og ingen kostnadsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="694c9-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="694c9-113">Eksempel 2: Kostnadsoppføringer opprettes</span><span class="sxs-lookup"><span data-stu-id="694c9-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="694c9-114">En overføringsjournalhendelse registreres.</span><span class="sxs-lookup"><span data-stu-id="694c9-114">A transfer journal event is registered.</span></span> <span data-ttu-id="694c9-115">Hendelsen overfører ett stykk av vare A fra område 1 til område 2.</span><span class="sxs-lookup"><span data-stu-id="694c9-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="694c9-116">Områdelagerdimensjonen regnes som en del av kostnadsobjektet.</span><span class="sxs-lookup"><span data-stu-id="694c9-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="694c9-117">Derfor oppretter hendelsen to lagertransaksjoner og to kostnadsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="694c9-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="694c9-118">Eksempel 3: Én kostnadsoppføring opprettes</span><span class="sxs-lookup"><span data-stu-id="694c9-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="694c9-119">En produktkvitteringshendelse registreres for en bestilling.</span><span class="sxs-lookup"><span data-stu-id="694c9-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="694c9-120">Hendelsen registrerer 100 stykk av vare A med en enhetskostnad på NOK 100,00.</span><span class="sxs-lookup"><span data-stu-id="694c9-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="694c9-121">Siden vare A bruker et serienummer til å spore formålet med lagerstyring, opprettes et unikt serienummer for hver vare som mottas.</span><span class="sxs-lookup"><span data-stu-id="694c9-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="694c9-122">Derfor oppretter hendelsen 100 lagertransaksjoner og én kostnadsoppføring.</span><span class="sxs-lookup"><span data-stu-id="694c9-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="694c9-123">Kostnadsoppføringer-siden</span><span class="sxs-lookup"><span data-stu-id="694c9-123">Cost entries page</span></span>
<span data-ttu-id="694c9-124">Den nye **Kostnadsoppføringer**-siden lar deg vise og styre registrering av antall og kostnader.</span><span class="sxs-lookup"><span data-stu-id="694c9-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="694c9-125">Denne siden kompletterer sidene **Lagertransaksjon** og **Lagerutligning**.</span><span class="sxs-lookup"><span data-stu-id="694c9-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="694c9-126">Poster registreres i kronologisk rekkefølge for en hendelse.</span><span class="sxs-lookup"><span data-stu-id="694c9-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="694c9-127">Derfor kan du raskt finne og styre de akkumulerte kostnadene for en bestemt hendelse eller alle hendelsene som er knyttet til et dokument.</span><span class="sxs-lookup"><span data-stu-id="694c9-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="694c9-128">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="694c9-128">Here is an example:</span></span>

-   <span data-ttu-id="694c9-129">En produktkvitteringshendelse er registrert for vare A. 100 stykker mottas med en enhetskostnad på NOK 100,00.</span><span class="sxs-lookup"><span data-stu-id="694c9-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="694c9-130">Noen dager etter at fakturahendelsen er registrert, øker kostnadene til NOK 110,00.</span><span class="sxs-lookup"><span data-stu-id="694c9-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="694c9-131">Derfor er totalbeløpet NOK 11 000.</span><span class="sxs-lookup"><span data-stu-id="694c9-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="694c9-132">Det opprettes et andre bilag for å gjøre rede for differansen på NOK 1 000.</span><span class="sxs-lookup"><span data-stu-id="694c9-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="694c9-133">Noen dager senere registreres et tilleggsgebyr på NOK 150,00 på bestillingen for å dekke transportkostnadene.</span><span class="sxs-lookup"><span data-stu-id="694c9-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="694c9-134">Bilag</span><span class="sxs-lookup"><span data-stu-id="694c9-134">Voucher</span></span> | <span data-ttu-id="694c9-135">Dato</span><span class="sxs-lookup"><span data-stu-id="694c9-135">Date</span></span>       | <span data-ttu-id="694c9-136">Referanse</span><span class="sxs-lookup"><span data-stu-id="694c9-136">Reference</span></span>      | <span data-ttu-id="694c9-137">Tall</span><span class="sxs-lookup"><span data-stu-id="694c9-137">Number</span></span> | <span data-ttu-id="694c9-138">Parti-ID</span><span class="sxs-lookup"><span data-stu-id="694c9-138">Lot ID</span></span>  | <span data-ttu-id="694c9-139">Antall</span><span class="sxs-lookup"><span data-stu-id="694c9-139">Quantity</span></span> | <span data-ttu-id="694c9-140">Beløp</span><span class="sxs-lookup"><span data-stu-id="694c9-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="694c9-141">00001</span><span class="sxs-lookup"><span data-stu-id="694c9-141">00001</span></span>   | <span data-ttu-id="694c9-142">01.01.2015</span><span class="sxs-lookup"><span data-stu-id="694c9-142">01-01-2015</span></span> | <span data-ttu-id="694c9-143">Bestilling</span><span class="sxs-lookup"><span data-stu-id="694c9-143">Purchase order</span></span> | <span data-ttu-id="694c9-144">100001</span><span class="sxs-lookup"><span data-stu-id="694c9-144">100001</span></span> | <span data-ttu-id="694c9-145">0000101</span><span class="sxs-lookup"><span data-stu-id="694c9-145">0000101</span></span> | <span data-ttu-id="694c9-146">1 00,00</span><span class="sxs-lookup"><span data-stu-id="694c9-146">100.00</span></span>   | <span data-ttu-id="694c9-147">1000,00</span><span class="sxs-lookup"><span data-stu-id="694c9-147">1000.00</span></span> |
| <span data-ttu-id="694c9-148">00002</span><span class="sxs-lookup"><span data-stu-id="694c9-148">00002</span></span>   | <span data-ttu-id="694c9-149">20.01.2015</span><span class="sxs-lookup"><span data-stu-id="694c9-149">20-01-2015</span></span> | <span data-ttu-id="694c9-150">Bestilling</span><span class="sxs-lookup"><span data-stu-id="694c9-150">Purchase order</span></span> | <span data-ttu-id="694c9-151">100001</span><span class="sxs-lookup"><span data-stu-id="694c9-151">100001</span></span> | <span data-ttu-id="694c9-152">0000101</span><span class="sxs-lookup"><span data-stu-id="694c9-152">0000101</span></span> |          | <span data-ttu-id="694c9-153">100,00</span><span class="sxs-lookup"><span data-stu-id="694c9-153">100.00</span></span>  |
| <span data-ttu-id="694c9-154">00003</span><span class="sxs-lookup"><span data-stu-id="694c9-154">00003</span></span>   | <span data-ttu-id="694c9-155">31.01.2015</span><span class="sxs-lookup"><span data-stu-id="694c9-155">31-01-2015</span></span> | <span data-ttu-id="694c9-156">Justering</span><span class="sxs-lookup"><span data-stu-id="694c9-156">Adjustment</span></span>     | <span data-ttu-id="694c9-157">100001</span><span class="sxs-lookup"><span data-stu-id="694c9-157">100001</span></span> | <span data-ttu-id="694c9-158">0000101</span><span class="sxs-lookup"><span data-stu-id="694c9-158">0000101</span></span> |          | <span data-ttu-id="694c9-159">15,00</span><span class="sxs-lookup"><span data-stu-id="694c9-159">15.00</span></span>   |

<span data-ttu-id="694c9-160">**Kostnadsoppføringer**-siden aktiverer filtrering etter dokument-ID og dokumentdato.</span><span class="sxs-lookup"><span data-stu-id="694c9-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="694c9-161">Kostnadsoppføringer er bare tilgjengelige for [kostnadsobjekter](cost-object.md) eller frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="694c9-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="694c9-162">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="694c9-162">Additional resources</span></span>

[<span data-ttu-id="694c9-163">Kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="694c9-163">Cost objects</span></span>](cost-object.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]