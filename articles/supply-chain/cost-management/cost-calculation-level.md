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
ms.openlocfilehash: 1cfbbb6aadbd24a0352776285f6c60ff10f59549
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251032"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="6a8cf-104">Kostnadsberegningsnivå</span><span class="sxs-lookup"><span data-stu-id="6a8cf-104">Cost calculation level</span></span>

<span data-ttu-id="6a8cf-105">Stykklistenivået som heter **Kostnadsberegningsnivå**, ekskluderer produksjonsordre og partiordre fra beregningene.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="6a8cf-106">Systemet bruker dette nivået når det kjører kostnadsberegninger i etterkalkuleringsversjoner.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="6a8cf-107">I prosesser som omberegning og lagerlukking bruker systemet BOM-nivået **Stykklistenivå** i stedet.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="6a8cf-108">Følgende enkle scenario viser forskjellene mellom stykklistenivåene for **Kostnadsberegningsnivå** og **Etterkalkuleringsnivå**.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="6a8cf-109">Du har tre produkter: A, B og C. Produkt C er komponenten til produkt B, og produkt B er komponenten til produkt A.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="6a8cf-110">**Etterkalkuleringsnivå** tilordner følgende stykklistenivåer:</span><span class="sxs-lookup"><span data-stu-id="6a8cf-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="6a8cf-111">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="6a8cf-111">**Product A:** 0</span></span>
    - <span data-ttu-id="6a8cf-112">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="6a8cf-112">**Product B:** 1</span></span>
    - <span data-ttu-id="6a8cf-113">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="6a8cf-113">**Product C:** 2</span></span>

- <span data-ttu-id="6a8cf-114">**Kostnadsberegningsnivå** tilordner følgende stykklistenivåer:</span><span class="sxs-lookup"><span data-stu-id="6a8cf-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="6a8cf-115">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="6a8cf-115">**Product A:** 0</span></span>
    - <span data-ttu-id="6a8cf-116">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="6a8cf-116">**Product B:** 1</span></span>
    - <span data-ttu-id="6a8cf-117">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="6a8cf-117">**Product C:** 2</span></span>

<span data-ttu-id="6a8cf-118">En produksjonsordre for produkt C opprettes deretter, og produkt A legges til i stykklisten for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="6a8cf-119">Når ordren er estimert, oppdateres stykklistenivåer på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="6a8cf-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="6a8cf-120">**Etterkalkuleringsnivå** tilordner følgende stykklistenivåer:</span><span class="sxs-lookup"><span data-stu-id="6a8cf-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="6a8cf-121">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="6a8cf-121">**Product B:** 1</span></span>
    - <span data-ttu-id="6a8cf-122">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="6a8cf-122">**Product C:** 2</span></span>
    - <span data-ttu-id="6a8cf-123">**Produkt A:** 3</span><span class="sxs-lookup"><span data-stu-id="6a8cf-123">**Product A:** 3</span></span>

- <span data-ttu-id="6a8cf-124">**Kostnadsberegningsnivå** tilordner følgende stykklistenivåer:</span><span class="sxs-lookup"><span data-stu-id="6a8cf-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="6a8cf-125">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="6a8cf-125">**Product A:** 0</span></span>
    - <span data-ttu-id="6a8cf-126">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="6a8cf-126">**Product B:** 1</span></span>
    - <span data-ttu-id="6a8cf-127">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="6a8cf-127">**Product C:** 2</span></span>

<span data-ttu-id="6a8cf-128">Denne virkemåten sikrer at endringer i stykklister for produksjonsordre ikke har innvirkning på etterfølgende kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="6a8cf-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]