---
title: Reduksjonsdager – eksempel
description: Reduksjonsdager – eksempel.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46b38579e8a6246476d0893e1a047ad434f6d399
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "334111"
---
# <a name="reduction-days-example"></a><span data-ttu-id="a4155-103">Reduksjonsdager – eksempel</span><span class="sxs-lookup"><span data-stu-id="a4155-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a4155-104">Du har opprettet en abonnementstransaksjon for en kundes vedlikeholdsabonnement som beskrevet i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="a4155-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a4155-105">Fra dato</span><span class="sxs-lookup"><span data-stu-id="a4155-105">From date</span></span></p></th>
<th><p><span data-ttu-id="a4155-106">Til dato</span><span class="sxs-lookup"><span data-stu-id="a4155-106">To date</span></span></p></th>
<th><p><span data-ttu-id="a4155-107">Abonnement</span><span class="sxs-lookup"><span data-stu-id="a4155-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="a4155-108">Abonnementstype</span><span class="sxs-lookup"><span data-stu-id="a4155-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="a4155-109">Project</span><span class="sxs-lookup"><span data-stu-id="a4155-109">Project</span></span></p></th>
<th><p><span data-ttu-id="a4155-110">Kategori</span><span class="sxs-lookup"><span data-stu-id="a4155-110">Category</span></span></p></th>
<th><p><span data-ttu-id="a4155-111">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="a4155-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="a4155-112">Salgspris</span><span class="sxs-lookup"><span data-stu-id="a4155-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4155-113">01. mars 2011</span><span class="sxs-lookup"><span data-stu-id="a4155-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="a4155-114">31. mars 2011</span><span class="sxs-lookup"><span data-stu-id="a4155-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="a4155-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="a4155-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="a4155-116"><strong>Vanlig</strong></span><span class="sxs-lookup"><span data-stu-id="a4155-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="a4155-117">9013</span><span class="sxs-lookup"><span data-stu-id="a4155-117">9013</span></span></p></td>
<td><p><span data-ttu-id="a4155-118">SubCat2</span><span class="sxs-lookup"><span data-stu-id="a4155-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="a4155-119">EUR</span><span class="sxs-lookup"><span data-stu-id="a4155-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="a4155-120">200,00</span><span class="sxs-lookup"><span data-stu-id="a4155-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a4155-121">Kunden rapporterer at det ikke behov for service to dager (10. og 11. mars).</span><span class="sxs-lookup"><span data-stu-id="a4155-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="a4155-122">Dere avtaler å trekke fra disse to dagene på abonnementet.</span><span class="sxs-lookup"><span data-stu-id="a4155-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="a4155-123">Du oppretter en ny transaksjon av typen **Reduksjonsdager** som beskrevet i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="a4155-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a4155-124">Fra dato</span><span class="sxs-lookup"><span data-stu-id="a4155-124">From date</span></span></p></th>
<th><p><span data-ttu-id="a4155-125">Til dato</span><span class="sxs-lookup"><span data-stu-id="a4155-125">To date</span></span></p></th>
<th><p><span data-ttu-id="a4155-126">Abonnement</span><span class="sxs-lookup"><span data-stu-id="a4155-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="a4155-127">Abonnementstype</span><span class="sxs-lookup"><span data-stu-id="a4155-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="a4155-128">Project</span><span class="sxs-lookup"><span data-stu-id="a4155-128">Project</span></span></p></th>
<th><p><span data-ttu-id="a4155-129">Kategori</span><span class="sxs-lookup"><span data-stu-id="a4155-129">Category</span></span></p></th>
<th><p><span data-ttu-id="a4155-130">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="a4155-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="a4155-131">Salgspris</span><span class="sxs-lookup"><span data-stu-id="a4155-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4155-132">10. mars 2011</span><span class="sxs-lookup"><span data-stu-id="a4155-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="a4155-133">11. mars 2011</span><span class="sxs-lookup"><span data-stu-id="a4155-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="a4155-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="a4155-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="a4155-135"><strong>Reduksjonsdager</strong></span><span class="sxs-lookup"><span data-stu-id="a4155-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="a4155-136">9013</span><span class="sxs-lookup"><span data-stu-id="a4155-136">9013</span></span></p></td>
<td><p><span data-ttu-id="a4155-137">SubCat2</span><span class="sxs-lookup"><span data-stu-id="a4155-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="a4155-138">EUR</span><span class="sxs-lookup"><span data-stu-id="a4155-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="a4155-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="a4155-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a4155-140">Når transaksjonene for mars 2011 blir fakturert, blir salgsprisen på EUR 200 redusert med EUR 12,90.</span><span class="sxs-lookup"><span data-stu-id="a4155-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="a4155-141">Det fakturerbare beløpet for abonnementstransaksjonen er derfor EUR 187,10, og to transaksjoner faktureres for totalt EUR 187,10.</span><span class="sxs-lookup"><span data-stu-id="a4155-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4155-142">Se også</span><span class="sxs-lookup"><span data-stu-id="a4155-142">See also</span></span>

[<span data-ttu-id="a4155-143">Redusere dagene på abonnementsgebyr</span><span class="sxs-lookup"><span data-stu-id="a4155-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


