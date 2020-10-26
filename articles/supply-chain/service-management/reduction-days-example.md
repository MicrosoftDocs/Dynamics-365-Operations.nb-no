---
title: Reduksjonsdager – eksempel
description: Reduksjonsdager – eksempel.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87c46cd7ee7410e1c7cb88868cd19f5075482f8c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975662"
---
# <a name="reduction-days-example"></a><span data-ttu-id="a09de-103">Reduksjonsdager – eksempel</span><span class="sxs-lookup"><span data-stu-id="a09de-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a09de-104">Du har opprettet en abonnementstransaksjon for en kundes vedlikeholdsabonnement som beskrevet i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="a09de-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="a09de-105">Fra dato</span><span class="sxs-lookup"><span data-stu-id="a09de-105">From date</span></span></p></th>
<th><p><span data-ttu-id="a09de-106">Til dato</span><span class="sxs-lookup"><span data-stu-id="a09de-106">To date</span></span></p></th>
<th><p><span data-ttu-id="a09de-107">Abonnement</span><span class="sxs-lookup"><span data-stu-id="a09de-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="a09de-108">Abonnementstype</span><span class="sxs-lookup"><span data-stu-id="a09de-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="a09de-109">Project</span><span class="sxs-lookup"><span data-stu-id="a09de-109">Project</span></span></p></th>
<th><p><span data-ttu-id="a09de-110">Kategori</span><span class="sxs-lookup"><span data-stu-id="a09de-110">Category</span></span></p></th>
<th><p><span data-ttu-id="a09de-111">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="a09de-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="a09de-112">Salgspris</span><span class="sxs-lookup"><span data-stu-id="a09de-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a09de-113">01. mars 2011</span><span class="sxs-lookup"><span data-stu-id="a09de-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="a09de-114">31. mars 2011</span><span class="sxs-lookup"><span data-stu-id="a09de-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="a09de-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="a09de-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="a09de-116"><strong>Vanlig</strong></span><span class="sxs-lookup"><span data-stu-id="a09de-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="a09de-117">9013</span><span class="sxs-lookup"><span data-stu-id="a09de-117">9013</span></span></p></td>
<td><p><span data-ttu-id="a09de-118">SubCat2</span><span class="sxs-lookup"><span data-stu-id="a09de-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="a09de-119">EUR</span><span class="sxs-lookup"><span data-stu-id="a09de-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="a09de-120">200,00</span><span class="sxs-lookup"><span data-stu-id="a09de-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a09de-121">Kunden rapporterer at det ikke behov for service to dager (10. og 11. mars).</span><span class="sxs-lookup"><span data-stu-id="a09de-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="a09de-122">Dere avtaler å trekke fra disse to dagene på abonnementet.</span><span class="sxs-lookup"><span data-stu-id="a09de-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="a09de-123">Du oppretter en ny transaksjon av typen **Reduksjonsdager** som beskrevet i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="a09de-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="a09de-124">Fra dato</span><span class="sxs-lookup"><span data-stu-id="a09de-124">From date</span></span></p></th>
<th><p><span data-ttu-id="a09de-125">Til dato</span><span class="sxs-lookup"><span data-stu-id="a09de-125">To date</span></span></p></th>
<th><p><span data-ttu-id="a09de-126">Abonnement</span><span class="sxs-lookup"><span data-stu-id="a09de-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="a09de-127">Abonnementstype</span><span class="sxs-lookup"><span data-stu-id="a09de-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="a09de-128">Project</span><span class="sxs-lookup"><span data-stu-id="a09de-128">Project</span></span></p></th>
<th><p><span data-ttu-id="a09de-129">Kategori</span><span class="sxs-lookup"><span data-stu-id="a09de-129">Category</span></span></p></th>
<th><p><span data-ttu-id="a09de-130">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="a09de-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="a09de-131">Salgspris</span><span class="sxs-lookup"><span data-stu-id="a09de-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a09de-132">10. mars 2011</span><span class="sxs-lookup"><span data-stu-id="a09de-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="a09de-133">11. mars 2011</span><span class="sxs-lookup"><span data-stu-id="a09de-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="a09de-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="a09de-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="a09de-135"><strong>Reduksjonsdager</strong></span><span class="sxs-lookup"><span data-stu-id="a09de-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="a09de-136">9013</span><span class="sxs-lookup"><span data-stu-id="a09de-136">9013</span></span></p></td>
<td><p><span data-ttu-id="a09de-137">SubCat2</span><span class="sxs-lookup"><span data-stu-id="a09de-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="a09de-138">EUR</span><span class="sxs-lookup"><span data-stu-id="a09de-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="a09de-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="a09de-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a09de-140">Når transaksjonene for mars 2011 blir fakturert, blir salgsprisen på EUR 200 redusert med EUR 12,90.</span><span class="sxs-lookup"><span data-stu-id="a09de-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="a09de-141">Det fakturerbare beløpet for abonnementstransaksjonen er derfor EUR 187,10, og to transaksjoner faktureres for totalt EUR 187,10.</span><span class="sxs-lookup"><span data-stu-id="a09de-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="a09de-142">Se også</span><span class="sxs-lookup"><span data-stu-id="a09de-142">See also</span></span>

[<span data-ttu-id="a09de-143">Redusere dagene på abonnementsgebyr</span><span class="sxs-lookup"><span data-stu-id="a09de-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


