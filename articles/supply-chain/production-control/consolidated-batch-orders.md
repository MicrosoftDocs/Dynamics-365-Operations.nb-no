---
title: Konsoliderte partiordrer
description: Denne artikkelen beskriver begrepet konsoliderte partiordrer.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2098cb458821146f6d1bf029591493ac745626f1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966461"
---
# <a name="consolidated-batch-orders"></a><span data-ttu-id="f9ecf-103">Konsoliderte partiordrer</span><span class="sxs-lookup"><span data-stu-id="f9ecf-103">Consolidated batch orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9ecf-104">Denne artikkelen beskriver begrepet konsoliderte partiordrer.</span><span class="sxs-lookup"><span data-stu-id="f9ecf-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="f9ecf-105">En bulkvare som produseres anses som en overordnet vare, mens en pakket vare anses som en underordnet vare.</span><span class="sxs-lookup"><span data-stu-id="f9ecf-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="f9ecf-106">Forholdet mellom bulkvaren og den pakkede varen uttrykkes i en bulkvarekonvertering.</span><span class="sxs-lookup"><span data-stu-id="f9ecf-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="f9ecf-107">Denne bulkvarekonverteringen er definert i selve bulkvaren.</span><span class="sxs-lookup"><span data-stu-id="f9ecf-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="f9ecf-108">Pakkede varer kan pakkes i containere i én eller flere størrelser som anses som én enhet.</span><span class="sxs-lookup"><span data-stu-id="f9ecf-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="f9ecf-109">Ved å konsolidere ordrene, kan du vise alle de relaterte partiordrene for en bulkvare i én enkelt visning, slik at det blir enklere å fastslå gjenstående arbeid som må fullføres.</span><span class="sxs-lookup"><span data-stu-id="f9ecf-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="f9ecf-110">En konsolidert partiordre kan inneholde en hvilken som helst kombinasjon av følgende ordrer:</span><span class="sxs-lookup"><span data-stu-id="f9ecf-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="f9ecf-111">Én enkelt bulkordre og flere pakkede ordrer</span><span class="sxs-lookup"><span data-stu-id="f9ecf-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="f9ecf-112">Flere bulkordrer og flere pakkede ordrer</span><span class="sxs-lookup"><span data-stu-id="f9ecf-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="f9ecf-113">Flere bulkordrer og én enkelt pakket ordre</span><span class="sxs-lookup"><span data-stu-id="f9ecf-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="f9ecf-114">Bare pakkede ordrer</span><span class="sxs-lookup"><span data-stu-id="f9ecf-114">Only packed orders</span></span>




