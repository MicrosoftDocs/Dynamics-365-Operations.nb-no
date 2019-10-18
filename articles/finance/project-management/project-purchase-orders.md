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
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174564"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="94567-104">Bestillinger for et prosjekt</span><span class="sxs-lookup"><span data-stu-id="94567-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94567-105">Denne artikkelen beskriver flere metoder du kan bruke til å opprette bestillinger for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="94567-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="94567-106">Hvilken metode du bruker, er avhengig av formålet med bestillingen og når de innkjøpte varene forbrukes og belastes et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="94567-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="94567-107">Metoder for å opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="94567-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="94567-108">Du kan bruke én av følgende metoder til å opprette en bestilling i prosjektstyring og regnskap.</span><span class="sxs-lookup"><span data-stu-id="94567-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="94567-109">Formålet med bestillingen fastsetter når bestillingen skal forbrukes, og derfor når varene skal belastes et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="94567-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="94567-110">Metode</span><span class="sxs-lookup"><span data-stu-id="94567-110">Method</span></span></th>
<th><span data-ttu-id="94567-111">Formål</span><span class="sxs-lookup"><span data-stu-id="94567-111">Purpose</span></span></th>
<th><span data-ttu-id="94567-112">Forbruk av varer</span><span class="sxs-lookup"><span data-stu-id="94567-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="94567-113">Opprett en bestilling direkte fra et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="94567-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="94567-114">Bruk denne metoden for å kjøpe varer fra en ekstern leverandør til forbruk på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="94567-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="94567-115">Du kan opprette bestillingen på to måter:</span><span class="sxs-lookup"><span data-stu-id="94567-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="94567-116">Fra selve prosjektet.</span><span class="sxs-lookup"><span data-stu-id="94567-116">From the project itself.</span></span> <span data-ttu-id="94567-117">I dette tilfellet er prosjekt allerede definert for bestillingen.</span><span class="sxs-lookup"><span data-stu-id="94567-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="94567-118">Ved å navigere til prosjektbestillingen.</span><span class="sxs-lookup"><span data-stu-id="94567-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="94567-119">Du må velge både leverandøren og prosjektet som bestillingen skal opprettes for.</span><span class="sxs-lookup"><span data-stu-id="94567-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="94567-120">Varene forbrukes når leverandørfakturaen oppdateres.</span><span class="sxs-lookup"><span data-stu-id="94567-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94567-121">Opprett en bestilling fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="94567-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="94567-122">Bruk denne metoden til å kjøpe varer når du oppretter en salgsordre fra et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="94567-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="94567-123">Varene forbrukes når salgsordren faktureres kunden.</span><span class="sxs-lookup"><span data-stu-id="94567-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="94567-124">Opprett en bestilling fra et varebehov.</span><span class="sxs-lookup"><span data-stu-id="94567-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="94567-125">Bruk denne metoden til å kjøpe varer når du oppretter et varebehov fra et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="94567-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="94567-126">Varene forbrukes når følgeseddelen for varebehov oppdateres.</span><span class="sxs-lookup"><span data-stu-id="94567-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="94567-127">Når du oppdaterer leverandørfakturaen eller følgeseddelen, blir du bedt om å oppdatere følgeseddelen for varebehovet.</span><span class="sxs-lookup"><span data-stu-id="94567-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="94567-128">Hvis du vil ha mer informasjon, se [Motta varer i bestilling fra varebehov](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="94567-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

