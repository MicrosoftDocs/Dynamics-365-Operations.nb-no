---
title: Reduksjonsdager – eksempel
description: Reduksjonsdager – eksempel.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90a2efff0add508ddb3d750bb3ca27ea35bf113a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836068"
---
# <a name="reduction-days-example"></a><span data-ttu-id="09bad-103">Reduksjonsdager – eksempel</span><span class="sxs-lookup"><span data-stu-id="09bad-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="09bad-104">Du har opprettet en abonnementstransaksjon for en kundes vedlikeholdsabonnement som beskrevet i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="09bad-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="09bad-105">Fra dato</span><span class="sxs-lookup"><span data-stu-id="09bad-105">From date</span></span></p></th>
<th><p><span data-ttu-id="09bad-106">Til dato</span><span class="sxs-lookup"><span data-stu-id="09bad-106">To date</span></span></p></th>
<th><p><span data-ttu-id="09bad-107">Abonnement</span><span class="sxs-lookup"><span data-stu-id="09bad-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="09bad-108">Abonnementstype</span><span class="sxs-lookup"><span data-stu-id="09bad-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="09bad-109">Project</span><span class="sxs-lookup"><span data-stu-id="09bad-109">Project</span></span></p></th>
<th><p><span data-ttu-id="09bad-110">Kategori</span><span class="sxs-lookup"><span data-stu-id="09bad-110">Category</span></span></p></th>
<th><p><span data-ttu-id="09bad-111">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="09bad-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="09bad-112">Salgspris</span><span class="sxs-lookup"><span data-stu-id="09bad-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09bad-113">01. mars 2011</span><span class="sxs-lookup"><span data-stu-id="09bad-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="09bad-114">31. mars 2011</span><span class="sxs-lookup"><span data-stu-id="09bad-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="09bad-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="09bad-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="09bad-116"><strong>Vanlig</strong></span><span class="sxs-lookup"><span data-stu-id="09bad-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="09bad-117">9013</span><span class="sxs-lookup"><span data-stu-id="09bad-117">9013</span></span></p></td>
<td><p><span data-ttu-id="09bad-118">SubCat2</span><span class="sxs-lookup"><span data-stu-id="09bad-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="09bad-119">EUR</span><span class="sxs-lookup"><span data-stu-id="09bad-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="09bad-120">200,00</span><span class="sxs-lookup"><span data-stu-id="09bad-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09bad-121">Kunden rapporterer at det ikke behov for service to dager (10. og 11. mars).</span><span class="sxs-lookup"><span data-stu-id="09bad-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="09bad-122">Dere avtaler å trekke fra disse to dagene på abonnementet.</span><span class="sxs-lookup"><span data-stu-id="09bad-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="09bad-123">Du oppretter en ny transaksjon av typen **Reduksjonsdager** som beskrevet i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="09bad-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="09bad-124">Fra dato</span><span class="sxs-lookup"><span data-stu-id="09bad-124">From date</span></span></p></th>
<th><p><span data-ttu-id="09bad-125">Til dato</span><span class="sxs-lookup"><span data-stu-id="09bad-125">To date</span></span></p></th>
<th><p><span data-ttu-id="09bad-126">Abonnement</span><span class="sxs-lookup"><span data-stu-id="09bad-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="09bad-127">Abonnementstype</span><span class="sxs-lookup"><span data-stu-id="09bad-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="09bad-128">Project</span><span class="sxs-lookup"><span data-stu-id="09bad-128">Project</span></span></p></th>
<th><p><span data-ttu-id="09bad-129">Kategori</span><span class="sxs-lookup"><span data-stu-id="09bad-129">Category</span></span></p></th>
<th><p><span data-ttu-id="09bad-130">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="09bad-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="09bad-131">Salgspris</span><span class="sxs-lookup"><span data-stu-id="09bad-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09bad-132">10. mars 2011</span><span class="sxs-lookup"><span data-stu-id="09bad-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="09bad-133">11. mars 2011</span><span class="sxs-lookup"><span data-stu-id="09bad-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="09bad-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="09bad-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="09bad-135"><strong>Reduksjonsdager</strong></span><span class="sxs-lookup"><span data-stu-id="09bad-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="09bad-136">9013</span><span class="sxs-lookup"><span data-stu-id="09bad-136">9013</span></span></p></td>
<td><p><span data-ttu-id="09bad-137">SubCat2</span><span class="sxs-lookup"><span data-stu-id="09bad-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="09bad-138">EUR</span><span class="sxs-lookup"><span data-stu-id="09bad-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="09bad-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="09bad-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09bad-140">Når transaksjonene for mars 2011 blir fakturert, blir salgsprisen på EUR 200 redusert med EUR 12,90.</span><span class="sxs-lookup"><span data-stu-id="09bad-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="09bad-141">Det fakturerbare beløpet for abonnementstransaksjonen er derfor EUR 187,10, og to transaksjoner faktureres for totalt EUR 187,10.</span><span class="sxs-lookup"><span data-stu-id="09bad-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="09bad-142">Se også</span><span class="sxs-lookup"><span data-stu-id="09bad-142">See also</span></span>

[<span data-ttu-id="09bad-143">Redusere dagene på abonnementsgebyr</span><span class="sxs-lookup"><span data-stu-id="09bad-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]