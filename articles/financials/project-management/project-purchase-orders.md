---
title: Bestillinger for et prosjekt
description: "Denne artikkelen beskriver flere metoder du kan bruke til å opprette bestillinger for et prosjekt. Hvilken metode du bruker, er avhengig av formålet med bestillingen og når de innkjøpte varene forbrukes og belastes et prosjekt."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: dae65394a2180ccbf3317a41b635ba97034e541b
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="4b17d-104">Bestillinger for et prosjekt</span><span class="sxs-lookup"><span data-stu-id="4b17d-104">Purchase orders for a project</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4b17d-105">Denne artikkelen beskriver flere metoder du kan bruke til å opprette bestillinger for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="4b17d-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="4b17d-106">Hvilken metode du bruker, er avhengig av formålet med bestillingen og når de innkjøpte varene forbrukes og belastes et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="4b17d-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

<span data-ttu-id="4b17d-107">Du kan bruke flere metoder til å opprette bestillinger for et prosjekt i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4b17d-107">In Microsoft Dynamics 365 for Finance and Operations, you can use multiple methods to create purchase orders for a project.</span></span> <span data-ttu-id="4b17d-108">Hvilken metode du bruker, er avhengig av formålet med bestillingen, når de innkjøpte varene forbrukes, og når de innkjøpte varene skal belastes et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="4b17d-108">The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="4b17d-109">Metoder for å opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="4b17d-109">Methods for creating a purchase order</span></span>

<span data-ttu-id="4b17d-110">Du kan bruke én av følgende metoder til å opprette en bestilling i prosjektstyring og regnskap.</span><span class="sxs-lookup"><span data-stu-id="4b17d-110">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="4b17d-111">Formålet med bestillingen fastsetter når bestillingen skal forbrukes, og derfor når varene skal belastes et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="4b17d-111">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b17d-112">Metode</span><span class="sxs-lookup"><span data-stu-id="4b17d-112">Method</span></span></th>
<th><span data-ttu-id="4b17d-113">Formål</span><span class="sxs-lookup"><span data-stu-id="4b17d-113">Purpose</span></span></th>
<th><span data-ttu-id="4b17d-114">Forbruk av varer</span><span class="sxs-lookup"><span data-stu-id="4b17d-114">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4b17d-115">Opprett en bestilling direkte fra et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="4b17d-115">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="4b17d-116">Bruk denne metoden for å kjøpe varer fra en ekstern leverandør til forbruk på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="4b17d-116">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="4b17d-117">Du kan opprette bestillingen på to måter:</span><span class="sxs-lookup"><span data-stu-id="4b17d-117">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="4b17d-118">Fra selve prosjektet.</span><span class="sxs-lookup"><span data-stu-id="4b17d-118">From the project itself.</span></span> <span data-ttu-id="4b17d-119">I dette tilfellet er prosjekt allerede definert for bestillingen.</span><span class="sxs-lookup"><span data-stu-id="4b17d-119">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="4b17d-120">Ved å navigere til prosjektbestillingen.</span><span class="sxs-lookup"><span data-stu-id="4b17d-120">By navigating to the project purchase order.</span></span> <span data-ttu-id="4b17d-121">Du må velge både leverandøren og prosjektet som bestillingen skal opprettes for.</span><span class="sxs-lookup"><span data-stu-id="4b17d-121">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="4b17d-122">Varene forbrukes når leverandørfakturaen oppdateres.</span><span class="sxs-lookup"><span data-stu-id="4b17d-122">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b17d-123">Opprett en bestilling fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="4b17d-123">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="4b17d-124">Bruk denne metoden til å kjøpe varer når du oppretter en salgsordre fra et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="4b17d-124">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="4b17d-125">Varene forbrukes når salgsordren faktureres kunden.</span><span class="sxs-lookup"><span data-stu-id="4b17d-125">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b17d-126">Opprett en bestilling fra et varebehov.</span><span class="sxs-lookup"><span data-stu-id="4b17d-126">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="4b17d-127">Bruk denne metoden til å kjøpe varer når du oppretter et varebehov fra et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="4b17d-127">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="4b17d-128">Varene forbrukes når følgeseddelen for varebehov oppdateres.</span><span class="sxs-lookup"><span data-stu-id="4b17d-128">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="4b17d-129">Når du oppdaterer leverandørfakturaen eller følgeseddelen, blir du bedt om å oppdatere følgeseddelen for varebehovet.</span><span class="sxs-lookup"><span data-stu-id="4b17d-129">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="4b17d-130">Hvis du vil ha mer informasjon, se [Motta varer i bestilling fra varebehov](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="4b17d-130">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>


