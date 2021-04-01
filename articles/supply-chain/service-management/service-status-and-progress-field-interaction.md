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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c66871d07bdfd949e29a704f53b3e5698d996c2d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254221"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="e0901-103">Servicestatus og fremdriftsfeltinteraksjon</span><span class="sxs-lookup"><span data-stu-id="e0901-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e0901-104">I **Serviceordrer**-skjemaet viser **Fremdrift**-feltet på serviceordrehodet statusen til hele serviceordren, og **Status** rapporterer statusen til individuelle serviceordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="e0901-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0901-105">Fremdrift</span><span class="sxs-lookup"><span data-stu-id="e0901-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="e0901-106">Status for linje 1</span><span class="sxs-lookup"><span data-stu-id="e0901-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="e0901-107">Status for linje 2</span><span class="sxs-lookup"><span data-stu-id="e0901-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="e0901-108">Status for linje 3</span><span class="sxs-lookup"><span data-stu-id="e0901-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0901-109"><strong>Pågår</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="e0901-110"><strong>Opprettet</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="e0901-111"><strong>Opprettet</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="e0901-112"><strong>Opprettet</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0901-113"><strong>Pågår</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="e0901-114"><strong>Avbrutt</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="e0901-115"><strong>Opprettet</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="e0901-116"><strong>Opprettet</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0901-117"><strong>Pågår</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="e0901-118"><strong>Opprettet</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="e0901-119"><strong>Avbrutt</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="e0901-120"><strong>Postert</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0901-121"><strong>Avbrutt</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="e0901-122"><strong>Avbrutt</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="e0901-123"><strong>Avbrutt</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="e0901-124"><strong>Avbrutt</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0901-125"><strong>Postert</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="e0901-126"><strong>Postert</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="e0901-127"><strong>Postert</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="e0901-128"><strong>Postert</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0901-129"><strong>Postert</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="e0901-130"><strong>Postert</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="e0901-131"><strong>Avbrutt</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="e0901-132"><strong>Avbrutt</strong></span><span class="sxs-lookup"><span data-stu-id="e0901-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e0901-133">Fremdriften til en serviceordre er i gang hvis alle linjer har statusen **Created**. Den er fremdeles i gang hvis noen har linjene har statusen **Annullert** eller **Postert**.</span><span class="sxs-lookup"><span data-stu-id="e0901-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="e0901-134">Hvis alle linjer i en serviceordre er merket som **Postert**, er fremdriften til statusordren **Postert** .</span><span class="sxs-lookup"><span data-stu-id="e0901-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="e0901-135">Hvis noen linjer er **Postert** og noen er **Annullert**, er fremdriften fremdeles **Postert**.</span><span class="sxs-lookup"><span data-stu-id="e0901-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]