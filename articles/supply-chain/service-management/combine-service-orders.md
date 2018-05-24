---
title: Kombiner serviceordrer
description: Du kan kombinere serviceordrer.
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8bc28d03d36d184e4bf41de2c50dac15e6d7813c
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="combine-service-orders"></a><span data-ttu-id="db168-103">Kombiner serviceordrer</span><span class="sxs-lookup"><span data-stu-id="db168-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="db168-104">Når du oppretter serviceordrelinjer automatisk i **Serviceavtaler**-skjemaet, kan du velge ett av følgende alternativer for å angi hvordan du vil gruppere dem:</span><span class="sxs-lookup"><span data-stu-id="db168-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="db168-105">**Etter serviceavtale**</span><span class="sxs-lookup"><span data-stu-id="db168-105">**By service agreement**</span></span>

  - <span data-ttu-id="db168-106">**Etter servicoppgave**</span><span class="sxs-lookup"><span data-stu-id="db168-106">**By service task**</span></span>

  - <span data-ttu-id="db168-107">**Etter ansatt**</span><span class="sxs-lookup"><span data-stu-id="db168-107">**By employee**</span></span>

  - <span data-ttu-id="db168-108">**Etter serviceobjekt**</span><span class="sxs-lookup"><span data-stu-id="db168-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="db168-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="db168-109">Example</span></span>

<span data-ttu-id="db168-110">Du kan opprette en serviceavtale med startdatoen 31. mars 2007.</span><span class="sxs-lookup"><span data-stu-id="db168-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="db168-111">I **Kombiner serviceordrer**-feltet angir du **Etter serviceobjekt**.</span><span class="sxs-lookup"><span data-stu-id="db168-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="db168-112">Deretter oppretter du følgende serviceavtalelinjer:</span><span class="sxs-lookup"><span data-stu-id="db168-112">You then create the following service agreement lines:</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="db168-113">Avtalelinjenummer</span><span class="sxs-lookup"><span data-stu-id="db168-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="db168-114">transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="db168-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="db168-115">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="db168-115">Description</span></span></p></th>
<th><p><span data-ttu-id="db168-116">Intervall</span><span class="sxs-lookup"><span data-stu-id="db168-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="db168-117">Serviceobjekt</span><span class="sxs-lookup"><span data-stu-id="db168-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="db168-118">Startdato</span><span class="sxs-lookup"><span data-stu-id="db168-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db168-119">1</span><span class="sxs-lookup"><span data-stu-id="db168-119">1</span></span></p></td>
<td><p><span data-ttu-id="db168-120"><strong>Time</strong></span><span class="sxs-lookup"><span data-stu-id="db168-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="db168-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="db168-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="db168-122">Ukentlig</span><span class="sxs-lookup"><span data-stu-id="db168-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="db168-123">X-1</span><span class="sxs-lookup"><span data-stu-id="db168-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="db168-124">01.04.2007</span><span class="sxs-lookup"><span data-stu-id="db168-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db168-125">2</span><span class="sxs-lookup"><span data-stu-id="db168-125">2</span></span></p></td>
<td><p><span data-ttu-id="db168-126"><strong>Time</strong></span><span class="sxs-lookup"><span data-stu-id="db168-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="db168-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="db168-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="db168-128">Annenhver uke</span><span class="sxs-lookup"><span data-stu-id="db168-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="db168-129">X-2</span><span class="sxs-lookup"><span data-stu-id="db168-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="db168-130">01.04.2007</span><span class="sxs-lookup"><span data-stu-id="db168-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db168-131">3</span><span class="sxs-lookup"><span data-stu-id="db168-131">3</span></span></p></td>
<td><p><span data-ttu-id="db168-132"><strong>Time</strong></span><span class="sxs-lookup"><span data-stu-id="db168-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="db168-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="db168-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="db168-134">Ukentlig</span><span class="sxs-lookup"><span data-stu-id="db168-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="db168-135">X-2</span><span class="sxs-lookup"><span data-stu-id="db168-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="db168-136">01.04.2007</span><span class="sxs-lookup"><span data-stu-id="db168-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="db168-137">Du angir ikke tidsvinduer for noen av serviceavtalelinjene.</span><span class="sxs-lookup"><span data-stu-id="db168-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="db168-138">Dermed flyttes ikke serviceordrelinjene fra den beregnede datoen de faller på.</span><span class="sxs-lookup"><span data-stu-id="db168-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="db168-139">Deretter genererer du serviceordrelinjer fra skjemaet **Opprett serviceordrer** fra 01.04.07 til 30.04.07.</span><span class="sxs-lookup"><span data-stu-id="db168-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="db168-140">Totalt sett opprettes det ti serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="db168-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="db168-141">Fordi du valgte kombinasjonsinnstillingen **Etter serviceobjekt**, får alle serviceordrer som opprettes, bare serviceordrelinjer med ett bestemt serviceobjekt.</span><span class="sxs-lookup"><span data-stu-id="db168-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="db168-142">Serviceordrelinjer som genereres fra serviceavtalen og har samme servicedato og samme objekt, kombineres på samme serviceordre.</span><span class="sxs-lookup"><span data-stu-id="db168-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="db168-143">I dette eksemplet har kalenderen som er angitt i skjemaet <STRONG>Servicestyringsparametere</STRONG>, ingen lukkede dager.</span><span class="sxs-lookup"><span data-stu-id="db168-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="db168-144">Serviceordrelinjene blir gruppert ytterligere i serviceordrer i henhold til eventuelle tidsvinduer som du angir i serviceavtalelinjene.</span><span class="sxs-lookup"><span data-stu-id="db168-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="db168-145">Se også</span><span class="sxs-lookup"><span data-stu-id="db168-145">See also</span></span>

[<span data-ttu-id="db168-146">Opprette serviceordrer automatisk</span><span class="sxs-lookup"><span data-stu-id="db168-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  



