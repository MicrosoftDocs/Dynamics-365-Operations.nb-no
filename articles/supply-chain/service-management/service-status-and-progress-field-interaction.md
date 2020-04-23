---
title: Servicestatus og fremdriftsfeltinteraksjon
description: I Serviceordrer-skjemaet viser Fremdrift-feltet på serviceordrehodet statusen til hele serviceordren, og Status rapporterer statusen til individuelle serviceordrelinjer.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd70d00f7ce531b225362065dfd9f1f5c1adc754
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207330"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="68383-103">Servicestatus og fremdriftsfeltinteraksjon</span><span class="sxs-lookup"><span data-stu-id="68383-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="68383-104">I **Serviceordrer**-skjemaet viser **Fremdrift**-feltet på serviceordrehodet statusen til hele serviceordren, og **Status** rapporterer statusen til individuelle serviceordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="68383-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="68383-105">Fremdrift</span><span class="sxs-lookup"><span data-stu-id="68383-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="68383-106">Status for linje 1</span><span class="sxs-lookup"><span data-stu-id="68383-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="68383-107">Status for linje 2</span><span class="sxs-lookup"><span data-stu-id="68383-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="68383-108">Status for linje 3</span><span class="sxs-lookup"><span data-stu-id="68383-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="68383-109"><strong>Pågår</strong></span><span class="sxs-lookup"><span data-stu-id="68383-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="68383-110"><strong>Opprettet</strong></span><span class="sxs-lookup"><span data-stu-id="68383-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="68383-111"><strong>Opprettet</strong></span><span class="sxs-lookup"><span data-stu-id="68383-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="68383-112"><strong>Opprettet</strong></span><span class="sxs-lookup"><span data-stu-id="68383-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68383-113"><strong>Pågår</strong></span><span class="sxs-lookup"><span data-stu-id="68383-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="68383-114"><strong>Avbrutt</strong></span><span class="sxs-lookup"><span data-stu-id="68383-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="68383-115"><strong>Opprettet</strong></span><span class="sxs-lookup"><span data-stu-id="68383-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="68383-116"><strong>Opprettet</strong></span><span class="sxs-lookup"><span data-stu-id="68383-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68383-117"><strong>Pågår</strong></span><span class="sxs-lookup"><span data-stu-id="68383-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="68383-118"><strong>Opprettet</strong></span><span class="sxs-lookup"><span data-stu-id="68383-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="68383-119"><strong>Avbrutt</strong></span><span class="sxs-lookup"><span data-stu-id="68383-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="68383-120"><strong>Postert</strong></span><span class="sxs-lookup"><span data-stu-id="68383-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68383-121"><strong>Avbrutt</strong></span><span class="sxs-lookup"><span data-stu-id="68383-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="68383-122"><strong>Avbrutt</strong></span><span class="sxs-lookup"><span data-stu-id="68383-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="68383-123"><strong>Avbrutt</strong></span><span class="sxs-lookup"><span data-stu-id="68383-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="68383-124"><strong>Avbrutt</strong></span><span class="sxs-lookup"><span data-stu-id="68383-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68383-125"><strong>Postert</strong></span><span class="sxs-lookup"><span data-stu-id="68383-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="68383-126"><strong>Postert</strong></span><span class="sxs-lookup"><span data-stu-id="68383-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="68383-127"><strong>Postert</strong></span><span class="sxs-lookup"><span data-stu-id="68383-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="68383-128"><strong>Postert</strong></span><span class="sxs-lookup"><span data-stu-id="68383-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68383-129"><strong>Postert</strong></span><span class="sxs-lookup"><span data-stu-id="68383-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="68383-130"><strong>Postert</strong></span><span class="sxs-lookup"><span data-stu-id="68383-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="68383-131"><strong>Avbrutt</strong></span><span class="sxs-lookup"><span data-stu-id="68383-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="68383-132"><strong>Avbrutt</strong></span><span class="sxs-lookup"><span data-stu-id="68383-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="68383-133">Fremdriften til en serviceordre er i gang hvis alle linjer har statusen **Created**. Den er fremdeles i gang hvis noen har linjene har statusen **Annullert** eller **Postert**.</span><span class="sxs-lookup"><span data-stu-id="68383-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="68383-134">Hvis alle linjer i en serviceordre er merket som **Postert**, er fremdriften til statusordren **Postert** .</span><span class="sxs-lookup"><span data-stu-id="68383-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="68383-135">Hvis noen linjer er **Postert** og noen er **Annullert**, er fremdriften fremdeles **Postert**.</span><span class="sxs-lookup"><span data-stu-id="68383-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  


