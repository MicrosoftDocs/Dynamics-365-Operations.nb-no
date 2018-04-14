---
title: Konsoliderte partiordrer
description: Denne artikkelen beskriver begrepet konsoliderte partiordrer.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 4c6be66eef6434f9ecca82903cc1e16b4bc290fe
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="consolidated-batch-orders"></a><span data-ttu-id="bf3e9-103">Konsoliderte partiordrer</span><span class="sxs-lookup"><span data-stu-id="bf3e9-103">Consolidated batch orders</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="bf3e9-104">Denne artikkelen beskriver begrepet konsoliderte partiordrer.</span><span class="sxs-lookup"><span data-stu-id="bf3e9-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="bf3e9-105">En bulkvare som produseres anses som en overordnet vare, mens en pakket vare anses som en underordnet vare.</span><span class="sxs-lookup"><span data-stu-id="bf3e9-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="bf3e9-106">Forholdet mellom bulkvaren og den pakkede varen uttrykkes i en bulkvarekonvertering.</span><span class="sxs-lookup"><span data-stu-id="bf3e9-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="bf3e9-107">Denne bulkvarekonverteringen er definert i selve bulkvaren.</span><span class="sxs-lookup"><span data-stu-id="bf3e9-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="bf3e9-108">Pakkede varer kan pakkes i containere i én eller flere størrelser som anses som én enhet.</span><span class="sxs-lookup"><span data-stu-id="bf3e9-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="bf3e9-109">Ved å konsolidere ordrene, kan du vise alle de relaterte partiordrene for en bulkvare i én enkelt visning, slik at det blir enklere å fastslå gjenstående arbeid som må fullføres.</span><span class="sxs-lookup"><span data-stu-id="bf3e9-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="bf3e9-110">En konsolidert partiordre kan inneholde en hvilken som helst kombinasjon av følgende ordrer:</span><span class="sxs-lookup"><span data-stu-id="bf3e9-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="bf3e9-111">Én enkelt bulkordre og flere pakkede ordrer</span><span class="sxs-lookup"><span data-stu-id="bf3e9-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="bf3e9-112">Flere bulkordrer og flere pakkede ordrer</span><span class="sxs-lookup"><span data-stu-id="bf3e9-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="bf3e9-113">Flere bulkordrer og én enkelt pakket ordre</span><span class="sxs-lookup"><span data-stu-id="bf3e9-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="bf3e9-114">Bare pakkede ordrer</span><span class="sxs-lookup"><span data-stu-id="bf3e9-114">Only packed orders</span></span>





