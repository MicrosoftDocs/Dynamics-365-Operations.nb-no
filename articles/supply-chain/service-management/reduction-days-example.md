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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df528bf7e95ee7ea74a792894b5e1c2f50c57730
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234759"
---
# <a name="reduction-days-example"></a><span data-ttu-id="75b89-103">Reduksjonsdager – eksempel</span><span class="sxs-lookup"><span data-stu-id="75b89-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="75b89-104">Du har opprettet en abonnementstransaksjon for en kundes vedlikeholdsabonnement som beskrevet i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="75b89-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="75b89-105">Fra dato</span><span class="sxs-lookup"><span data-stu-id="75b89-105">From date</span></span></p></th>
<th><p><span data-ttu-id="75b89-106">Til dato</span><span class="sxs-lookup"><span data-stu-id="75b89-106">To date</span></span></p></th>
<th><p><span data-ttu-id="75b89-107">Abonnement</span><span class="sxs-lookup"><span data-stu-id="75b89-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="75b89-108">Abonnementstype</span><span class="sxs-lookup"><span data-stu-id="75b89-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="75b89-109">Project</span><span class="sxs-lookup"><span data-stu-id="75b89-109">Project</span></span></p></th>
<th><p><span data-ttu-id="75b89-110">Kategori</span><span class="sxs-lookup"><span data-stu-id="75b89-110">Category</span></span></p></th>
<th><p><span data-ttu-id="75b89-111">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="75b89-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="75b89-112">Salgspris</span><span class="sxs-lookup"><span data-stu-id="75b89-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75b89-113">01. mars 2011</span><span class="sxs-lookup"><span data-stu-id="75b89-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="75b89-114">31. mars 2011</span><span class="sxs-lookup"><span data-stu-id="75b89-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="75b89-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="75b89-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="75b89-116"><strong>Vanlig</strong></span><span class="sxs-lookup"><span data-stu-id="75b89-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="75b89-117">9013</span><span class="sxs-lookup"><span data-stu-id="75b89-117">9013</span></span></p></td>
<td><p><span data-ttu-id="75b89-118">SubCat2</span><span class="sxs-lookup"><span data-stu-id="75b89-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="75b89-119">EUR</span><span class="sxs-lookup"><span data-stu-id="75b89-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="75b89-120">200,00</span><span class="sxs-lookup"><span data-stu-id="75b89-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="75b89-121">Kunden rapporterer at det ikke behov for service to dager (10. og 11. mars).</span><span class="sxs-lookup"><span data-stu-id="75b89-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="75b89-122">Dere avtaler å trekke fra disse to dagene på abonnementet.</span><span class="sxs-lookup"><span data-stu-id="75b89-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="75b89-123">Du oppretter en ny transaksjon av typen **Reduksjonsdager** som beskrevet i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="75b89-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="75b89-124">Fra dato</span><span class="sxs-lookup"><span data-stu-id="75b89-124">From date</span></span></p></th>
<th><p><span data-ttu-id="75b89-125">Til dato</span><span class="sxs-lookup"><span data-stu-id="75b89-125">To date</span></span></p></th>
<th><p><span data-ttu-id="75b89-126">Abonnement</span><span class="sxs-lookup"><span data-stu-id="75b89-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="75b89-127">Abonnementstype</span><span class="sxs-lookup"><span data-stu-id="75b89-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="75b89-128">Project</span><span class="sxs-lookup"><span data-stu-id="75b89-128">Project</span></span></p></th>
<th><p><span data-ttu-id="75b89-129">Kategori</span><span class="sxs-lookup"><span data-stu-id="75b89-129">Category</span></span></p></th>
<th><p><span data-ttu-id="75b89-130">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="75b89-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="75b89-131">Salgspris</span><span class="sxs-lookup"><span data-stu-id="75b89-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75b89-132">10. mars 2011</span><span class="sxs-lookup"><span data-stu-id="75b89-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="75b89-133">11. mars 2011</span><span class="sxs-lookup"><span data-stu-id="75b89-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="75b89-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="75b89-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="75b89-135"><strong>Reduksjonsdager</strong></span><span class="sxs-lookup"><span data-stu-id="75b89-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="75b89-136">9013</span><span class="sxs-lookup"><span data-stu-id="75b89-136">9013</span></span></p></td>
<td><p><span data-ttu-id="75b89-137">SubCat2</span><span class="sxs-lookup"><span data-stu-id="75b89-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="75b89-138">EUR</span><span class="sxs-lookup"><span data-stu-id="75b89-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="75b89-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="75b89-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="75b89-140">Når transaksjonene for mars 2011 blir fakturert, blir salgsprisen på EUR 200 redusert med EUR 12,90.</span><span class="sxs-lookup"><span data-stu-id="75b89-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="75b89-141">Det fakturerbare beløpet for abonnementstransaksjonen er derfor EUR 187,10, og to transaksjoner faktureres for totalt EUR 187,10.</span><span class="sxs-lookup"><span data-stu-id="75b89-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="75b89-142">Se også</span><span class="sxs-lookup"><span data-stu-id="75b89-142">See also</span></span>

[<span data-ttu-id="75b89-143">Redusere dagene på abonnementsgebyr</span><span class="sxs-lookup"><span data-stu-id="75b89-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]