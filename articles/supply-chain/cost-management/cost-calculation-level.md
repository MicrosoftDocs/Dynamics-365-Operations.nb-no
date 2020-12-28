---
title: Kostnadsberegningsnivå
description: Dette emnet beskriver stykklistenivået som kalles Kostnadsberegningsnivå. Dette stykklistenivået utelukker produksjons- og partiordrer fra beregningene.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 52b77e794ee38add556ac01d62c973b38c48a548
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434319"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="87a56-104">Kostnadsberegningsnivå</span><span class="sxs-lookup"><span data-stu-id="87a56-104">Cost calculation level</span></span>

<span data-ttu-id="87a56-105">Stykklistenivået som heter **Kostnadsberegningsnivå**, ekskluderer produksjonsordre og partiordre fra beregningene.</span><span class="sxs-lookup"><span data-stu-id="87a56-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="87a56-106">Systemet bruker dette nivået når det kjører kostnadsberegninger i etterkalkuleringsversjoner.</span><span class="sxs-lookup"><span data-stu-id="87a56-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="87a56-107">I prosesser som omberegning og lagerlukking bruker systemet BOM-nivået **Stykklistenivå** i stedet.</span><span class="sxs-lookup"><span data-stu-id="87a56-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="87a56-108">Følgende enkle scenario viser forskjellene mellom stykklistenivåene for **Kostnadsberegningsnivå** og **Etterkalkuleringsnivå**.</span><span class="sxs-lookup"><span data-stu-id="87a56-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="87a56-109">Du har tre produkter: A, B og C. Produkt C er komponenten til produkt B, og produkt B er komponenten til produkt A.</span><span class="sxs-lookup"><span data-stu-id="87a56-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="87a56-110">**Etterkalkuleringsnivå** tilordner følgende stykklistenivåer:</span><span class="sxs-lookup"><span data-stu-id="87a56-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="87a56-111">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="87a56-111">**Product A:** 0</span></span>
    - <span data-ttu-id="87a56-112">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="87a56-112">**Product B:** 1</span></span>
    - <span data-ttu-id="87a56-113">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="87a56-113">**Product C:** 2</span></span>

- <span data-ttu-id="87a56-114">**Kostnadsberegningsnivå** tilordner følgende stykklistenivåer:</span><span class="sxs-lookup"><span data-stu-id="87a56-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="87a56-115">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="87a56-115">**Product A:** 0</span></span>
    - <span data-ttu-id="87a56-116">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="87a56-116">**Product B:** 1</span></span>
    - <span data-ttu-id="87a56-117">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="87a56-117">**Product C:** 2</span></span>

<span data-ttu-id="87a56-118">En produksjonsordre for produkt C opprettes deretter, og produkt A legges til i stykklisten for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="87a56-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="87a56-119">Når ordren er estimert, oppdateres stykklistenivåer på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="87a56-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="87a56-120">**Etterkalkuleringsnivå** tilordner følgende stykklistenivåer:</span><span class="sxs-lookup"><span data-stu-id="87a56-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="87a56-121">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="87a56-121">**Product B:** 1</span></span>
    - <span data-ttu-id="87a56-122">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="87a56-122">**Product C:** 2</span></span>
    - <span data-ttu-id="87a56-123">**Produkt A:** 3</span><span class="sxs-lookup"><span data-stu-id="87a56-123">**Product A:** 3</span></span>

- <span data-ttu-id="87a56-124">**Kostnadsberegningsnivå** tilordner følgende stykklistenivåer:</span><span class="sxs-lookup"><span data-stu-id="87a56-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="87a56-125">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="87a56-125">**Product A:** 0</span></span>
    - <span data-ttu-id="87a56-126">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="87a56-126">**Product B:** 1</span></span>
    - <span data-ttu-id="87a56-127">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="87a56-127">**Product C:** 2</span></span>

<span data-ttu-id="87a56-128">Denne virkemåten sikrer at endringer i stykklister for produksjonsordre ikke har innvirkning på etterfølgende kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="87a56-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
