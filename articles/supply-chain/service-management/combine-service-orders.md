---
title: Kombiner serviceordrer
description: Du kan kombinere serviceordrer.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7bd3ac8cf3c025b082b33247fcd020aebc010bc8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247724"
---
# <a name="combine-service-orders"></a><span data-ttu-id="de46c-103">Kombiner serviceordrer</span><span class="sxs-lookup"><span data-stu-id="de46c-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="de46c-104">Når du oppretter serviceordrelinjer automatisk i **Serviceavtaler**-skjemaet, kan du velge ett av følgende alternativer for å angi hvordan du vil gruppere dem:</span><span class="sxs-lookup"><span data-stu-id="de46c-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="de46c-105">**Etter serviceavtale**</span><span class="sxs-lookup"><span data-stu-id="de46c-105">**By service agreement**</span></span>

  - <span data-ttu-id="de46c-106">**Etter servicoppgave**</span><span class="sxs-lookup"><span data-stu-id="de46c-106">**By service task**</span></span>

  - <span data-ttu-id="de46c-107">**Etter ansatt**</span><span class="sxs-lookup"><span data-stu-id="de46c-107">**By employee**</span></span>

  - <span data-ttu-id="de46c-108">**Etter serviceobjekt**</span><span class="sxs-lookup"><span data-stu-id="de46c-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="de46c-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="de46c-109">Example</span></span>

<span data-ttu-id="de46c-110">Du kan opprette en serviceavtale med startdatoen 31. mars 2007.</span><span class="sxs-lookup"><span data-stu-id="de46c-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="de46c-111">I **Kombiner serviceordrer**-feltet angir du **Etter serviceobjekt**.</span><span class="sxs-lookup"><span data-stu-id="de46c-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="de46c-112">Deretter oppretter du følgende serviceavtalelinjer:</span><span class="sxs-lookup"><span data-stu-id="de46c-112">You then create the following service agreement lines:</span></span>

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
<th><p><span data-ttu-id="de46c-113">Avtalelinjenummer</span><span class="sxs-lookup"><span data-stu-id="de46c-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="de46c-114">transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="de46c-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="de46c-115">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="de46c-115">Description</span></span></p></th>
<th><p><span data-ttu-id="de46c-116">Intervall</span><span class="sxs-lookup"><span data-stu-id="de46c-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="de46c-117">Serviceobjekt</span><span class="sxs-lookup"><span data-stu-id="de46c-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="de46c-118">Startdato</span><span class="sxs-lookup"><span data-stu-id="de46c-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de46c-119">1</span><span class="sxs-lookup"><span data-stu-id="de46c-119">1</span></span></p></td>
<td><p><span data-ttu-id="de46c-120"><strong>Time</strong></span><span class="sxs-lookup"><span data-stu-id="de46c-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="de46c-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="de46c-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="de46c-122">Ukentlig</span><span class="sxs-lookup"><span data-stu-id="de46c-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="de46c-123">X-1</span><span class="sxs-lookup"><span data-stu-id="de46c-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="de46c-124">01.04.2007</span><span class="sxs-lookup"><span data-stu-id="de46c-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de46c-125">2</span><span class="sxs-lookup"><span data-stu-id="de46c-125">2</span></span></p></td>
<td><p><span data-ttu-id="de46c-126"><strong>Time</strong></span><span class="sxs-lookup"><span data-stu-id="de46c-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="de46c-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="de46c-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="de46c-128">Annenhver uke</span><span class="sxs-lookup"><span data-stu-id="de46c-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="de46c-129">X-2</span><span class="sxs-lookup"><span data-stu-id="de46c-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="de46c-130">01.04.2007</span><span class="sxs-lookup"><span data-stu-id="de46c-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de46c-131">3</span><span class="sxs-lookup"><span data-stu-id="de46c-131">3</span></span></p></td>
<td><p><span data-ttu-id="de46c-132"><strong>Time</strong></span><span class="sxs-lookup"><span data-stu-id="de46c-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="de46c-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="de46c-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="de46c-134">Ukentlig</span><span class="sxs-lookup"><span data-stu-id="de46c-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="de46c-135">X-2</span><span class="sxs-lookup"><span data-stu-id="de46c-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="de46c-136">01.04.2007</span><span class="sxs-lookup"><span data-stu-id="de46c-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="de46c-137">Du angir ikke tidsvinduer for noen av serviceavtalelinjene.</span><span class="sxs-lookup"><span data-stu-id="de46c-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="de46c-138">Dermed flyttes ikke serviceordrelinjene fra den beregnede datoen de faller på.</span><span class="sxs-lookup"><span data-stu-id="de46c-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="de46c-139">Deretter genererer du serviceordrelinjer fra skjemaet **Opprett serviceordrer** fra 01.04.07 til 30.04.07.</span><span class="sxs-lookup"><span data-stu-id="de46c-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="de46c-140">Totalt sett opprettes det ti serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="de46c-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="de46c-141">Fordi du valgte kombinasjonsinnstillingen **Etter serviceobjekt**, får alle serviceordrer som opprettes, bare serviceordrelinjer med ett bestemt serviceobjekt.</span><span class="sxs-lookup"><span data-stu-id="de46c-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="de46c-142">Serviceordrelinjer som genereres fra serviceavtalen og har samme servicedato og samme objekt, kombineres på samme serviceordre.</span><span class="sxs-lookup"><span data-stu-id="de46c-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="de46c-143">I dette eksemplet har kalenderen som er angitt i skjemaet <STRONG>Servicestyringsparametere</STRONG>, ingen lukkede dager.</span><span class="sxs-lookup"><span data-stu-id="de46c-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="de46c-144">Serviceordrelinjene blir gruppert ytterligere i serviceordrer i henhold til eventuelle tidsvinduer som du angir i serviceavtalelinjene.</span><span class="sxs-lookup"><span data-stu-id="de46c-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="de46c-145">Se også</span><span class="sxs-lookup"><span data-stu-id="de46c-145">See also</span></span>

[<span data-ttu-id="de46c-146">Opprette serviceordrer automatisk</span><span class="sxs-lookup"><span data-stu-id="de46c-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]