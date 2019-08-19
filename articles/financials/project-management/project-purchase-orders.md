---
title: Bestillinger for et prosjekt
description: Denne artikkelen beskriver flere metoder du kan bruke til å opprette bestillinger for et prosjekt. Hvilken metode du bruker, er avhengig av formålet med bestillingen og når de innkjøpte varene forbrukes og belastes et prosjekt.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 971a4ea0abac43c160d8a6f46f385cbfc5134ffd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838877"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="6779f-104">Bestillinger for et prosjekt</span><span class="sxs-lookup"><span data-stu-id="6779f-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6779f-105">Denne artikkelen beskriver flere metoder du kan bruke til å opprette bestillinger for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="6779f-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="6779f-106">Hvilken metode du bruker, er avhengig av formålet med bestillingen og når de innkjøpte varene forbrukes og belastes et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="6779f-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

<span data-ttu-id="6779f-107">Du kan bruke flere metoder til å opprette bestillinger for et prosjekt i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6779f-107">In Microsoft Dynamics 365 for Finance and Operations, you can use multiple methods to create purchase orders for a project.</span></span> <span data-ttu-id="6779f-108">Hvilken metode du bruker, er avhengig av formålet med bestillingen, når de innkjøpte varene forbrukes, og når de innkjøpte varene skal belastes et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="6779f-108">The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="6779f-109">Metoder for å opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="6779f-109">Methods for creating a purchase order</span></span>

<span data-ttu-id="6779f-110">Du kan bruke én av følgende metoder til å opprette en bestilling i prosjektstyring og regnskap.</span><span class="sxs-lookup"><span data-stu-id="6779f-110">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="6779f-111">Formålet med bestillingen fastsetter når bestillingen skal forbrukes, og derfor når varene skal belastes et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="6779f-111">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6779f-112">Metode</span><span class="sxs-lookup"><span data-stu-id="6779f-112">Method</span></span></th>
<th><span data-ttu-id="6779f-113">Formål</span><span class="sxs-lookup"><span data-stu-id="6779f-113">Purpose</span></span></th>
<th><span data-ttu-id="6779f-114">Forbruk av varer</span><span class="sxs-lookup"><span data-stu-id="6779f-114">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6779f-115">Opprett en bestilling direkte fra et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="6779f-115">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="6779f-116">Bruk denne metoden for å kjøpe varer fra en ekstern leverandør til forbruk på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="6779f-116">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="6779f-117">Du kan opprette bestillingen på to måter:</span><span class="sxs-lookup"><span data-stu-id="6779f-117">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="6779f-118">Fra selve prosjektet.</span><span class="sxs-lookup"><span data-stu-id="6779f-118">From the project itself.</span></span> <span data-ttu-id="6779f-119">I dette tilfellet er prosjekt allerede definert for bestillingen.</span><span class="sxs-lookup"><span data-stu-id="6779f-119">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="6779f-120">Ved å navigere til prosjektbestillingen.</span><span class="sxs-lookup"><span data-stu-id="6779f-120">By navigating to the project purchase order.</span></span> <span data-ttu-id="6779f-121">Du må velge både leverandøren og prosjektet som bestillingen skal opprettes for.</span><span class="sxs-lookup"><span data-stu-id="6779f-121">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="6779f-122">Varene forbrukes når leverandørfakturaen oppdateres.</span><span class="sxs-lookup"><span data-stu-id="6779f-122">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6779f-123">Opprett en bestilling fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="6779f-123">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="6779f-124">Bruk denne metoden til å kjøpe varer når du oppretter en salgsordre fra et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="6779f-124">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="6779f-125">Varene forbrukes når salgsordren faktureres kunden.</span><span class="sxs-lookup"><span data-stu-id="6779f-125">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6779f-126">Opprett en bestilling fra et varebehov.</span><span class="sxs-lookup"><span data-stu-id="6779f-126">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="6779f-127">Bruk denne metoden til å kjøpe varer når du oppretter et varebehov fra et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="6779f-127">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="6779f-128">Varene forbrukes når følgeseddelen for varebehov oppdateres.</span><span class="sxs-lookup"><span data-stu-id="6779f-128">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="6779f-129">Når du oppdaterer leverandørfakturaen eller følgeseddelen, blir du bedt om å oppdatere følgeseddelen for varebehovet.</span><span class="sxs-lookup"><span data-stu-id="6779f-129">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="6779f-130">Hvis du vil ha mer informasjon, se [Motta varer i bestilling fra varebehov](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="6779f-130">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

