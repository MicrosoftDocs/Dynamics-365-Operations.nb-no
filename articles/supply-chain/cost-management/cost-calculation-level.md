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
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 42088d8c005cf3fc04e768f1b8e8c8ca0b8c6993
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967738"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="3b551-104">Kostnadsberegningsnivå</span><span class="sxs-lookup"><span data-stu-id="3b551-104">Cost calculation level</span></span>

<span data-ttu-id="3b551-105">Stykklistenivået som heter **Kostnadsberegningsnivå**, ekskluderer produksjonsordre og partiordre fra beregningene.</span><span class="sxs-lookup"><span data-stu-id="3b551-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="3b551-106">Systemet bruker dette nivået når det kjører kostnadsberegninger i etterkalkuleringsversjoner.</span><span class="sxs-lookup"><span data-stu-id="3b551-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="3b551-107">I prosesser som omberegning og lagerlukking bruker systemet BOM-nivået **Stykklistenivå** i stedet.</span><span class="sxs-lookup"><span data-stu-id="3b551-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="3b551-108">Følgende enkle scenario viser forskjellene mellom stykklistenivåene for **Kostnadsberegningsnivå** og **Etterkalkuleringsnivå**.</span><span class="sxs-lookup"><span data-stu-id="3b551-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="3b551-109">Du har tre produkter: A, B og C. Produkt C er komponenten til produkt B, og produkt B er komponenten til produkt A.</span><span class="sxs-lookup"><span data-stu-id="3b551-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="3b551-110">**Etterkalkuleringsnivå** tilordner følgende stykklistenivåer:</span><span class="sxs-lookup"><span data-stu-id="3b551-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="3b551-111">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="3b551-111">**Product A:** 0</span></span>
    - <span data-ttu-id="3b551-112">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="3b551-112">**Product B:** 1</span></span>
    - <span data-ttu-id="3b551-113">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="3b551-113">**Product C:** 2</span></span>

- <span data-ttu-id="3b551-114">**Kostnadsberegningsnivå** tilordner følgende stykklistenivåer:</span><span class="sxs-lookup"><span data-stu-id="3b551-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="3b551-115">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="3b551-115">**Product A:** 0</span></span>
    - <span data-ttu-id="3b551-116">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="3b551-116">**Product B:** 1</span></span>
    - <span data-ttu-id="3b551-117">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="3b551-117">**Product C:** 2</span></span>

<span data-ttu-id="3b551-118">En produksjonsordre for produkt C opprettes deretter, og produkt A legges til i stykklisten for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="3b551-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="3b551-119">Når ordren er estimert, oppdateres stykklistenivåer på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="3b551-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="3b551-120">**Etterkalkuleringsnivå** tilordner følgende stykklistenivåer:</span><span class="sxs-lookup"><span data-stu-id="3b551-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="3b551-121">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="3b551-121">**Product B:** 1</span></span>
    - <span data-ttu-id="3b551-122">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="3b551-122">**Product C:** 2</span></span>
    - <span data-ttu-id="3b551-123">**Produkt A:** 3</span><span class="sxs-lookup"><span data-stu-id="3b551-123">**Product A:** 3</span></span>

- <span data-ttu-id="3b551-124">**Kostnadsberegningsnivå** tilordner følgende stykklistenivåer:</span><span class="sxs-lookup"><span data-stu-id="3b551-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="3b551-125">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="3b551-125">**Product A:** 0</span></span>
    - <span data-ttu-id="3b551-126">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="3b551-126">**Product B:** 1</span></span>
    - <span data-ttu-id="3b551-127">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="3b551-127">**Product C:** 2</span></span>

<span data-ttu-id="3b551-128">Denne virkemåten sikrer at endringer i stykklister for produksjonsordre ikke har innvirkning på etterfølgende kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="3b551-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
