---
title: Vanlige kilder til produksjonsavvik
description: Denne artikkelen beskriver forskjellige vanlige kilder til hver type produksjonsavvik.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 50f8cd7904e1d32175edd321fbd6533e985fb324
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---

# <a name="common-sources-of-production-variances"></a><span data-ttu-id="2d512-103">Vanlige kilder til produksjonsavvik</span><span class="sxs-lookup"><span data-stu-id="2d512-103">Common sources of production variances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d512-104">Denne artikkelen beskriver forskjellige vanlige kilder til hver type produksjonsavvik.</span><span class="sxs-lookup"><span data-stu-id="2d512-104">This article explains various typical sources of each type of production variance.</span></span> 

<span data-ttu-id="2d512-105">Her er noen vanlige kilder til et **partistørrelsesavvik**:</span><span class="sxs-lookup"><span data-stu-id="2d512-105">Here are some typical sources of a **lot size** variance:</span></span>

-   <span data-ttu-id="2d512-106">Det korrekte antallet for en produksjonsordre avviker fra det beregnede antallet som brukes i standard kostnadsberegning.</span><span class="sxs-lookup"><span data-stu-id="2d512-106">The good quantity for a production order differs from the calculation quantity that is used in the standard cost calculation.</span></span> <span data-ttu-id="2d512-107">Antallet gir grunnlaget for nedbetaling av konstante kostnader.</span><span class="sxs-lookup"><span data-stu-id="2d512-107">The quantity provides the basis for amortizing constant costs.</span></span>
-   <span data-ttu-id="2d512-108">Verdien av konstante kostnader på produksjonsordren avviker fra de konstante kostnadene som er brukt i standard kostnadsberegning.</span><span class="sxs-lookup"><span data-stu-id="2d512-108">The value of constant costs on the production order differs from the constant costs that are used in the standard cost calculation.</span></span> <span data-ttu-id="2d512-109">De konstante kostnadene på produksjonsordren kan være forskjellige av flere årsaker.</span><span class="sxs-lookup"><span data-stu-id="2d512-109">The constant costs on the production order can differ for several reasons.</span></span> <span data-ttu-id="2d512-110">De konstante kostnadene kan for eksempel gjenspeile følgende faktorer:</span><span class="sxs-lookup"><span data-stu-id="2d512-110">For example, the constant costs might reflect the following factors:</span></span>
    -   <span data-ttu-id="2d512-111">Manuelle endringer i produksjonsstykklisten stykklisten eller ruten</span><span class="sxs-lookup"><span data-stu-id="2d512-111">Manual changes to the production bill of materials (BOM) or route</span></span>
    -   <span data-ttu-id="2d512-112">Valget av en annen stykklisteversjon eller ruteversjon når du oppretter produksjonsordren</span><span class="sxs-lookup"><span data-stu-id="2d512-112">The selection of a different BOM version or route version when you create the production order</span></span>
    -   <span data-ttu-id="2d512-113">Planlagte tekniske endringer med den stykklisteversjonen eller ruteversjonen som er tilordnet varen</span><span class="sxs-lookup"><span data-stu-id="2d512-113">Planned engineering changes to the BOM version or route version that is assigned to the item</span></span>

<span data-ttu-id="2d512-114">Her er noen vanlige kilder til et avvik i **produksjonspris**:</span><span class="sxs-lookup"><span data-stu-id="2d512-114">Here are some typical sources of a **production price** variance:</span></span>

-   <span data-ttu-id="2d512-115">Kostnadskategorien (og kostkategoripris) for det rapporterte forbruket av en ruteoperasjon avviker fra den kostnadskategorien som er brukt i standard kostnadsberegning.</span><span class="sxs-lookup"><span data-stu-id="2d512-115">The cost category (and cost category price) for the reported consumption of a routing operation differs from the cost category that is used in standard cost calculation.</span></span>
-   <span data-ttu-id="2d512-116">Den aktive kostnaden for kostkategoriprisen avviker fra den kostkategoriprisen som er brukt i standard kostnadsberegning.</span><span class="sxs-lookup"><span data-stu-id="2d512-116">The active cost for the cost category price differs from the cost category price that is used in standard cost calculation.</span></span>

<span data-ttu-id="2d512-117">Her er noen vanlige kilder til et avvik i **produksjonsantall**:</span><span class="sxs-lookup"><span data-stu-id="2d512-117">Here are some typical sources of a **production quantity** variance:</span></span>

-   <span data-ttu-id="2d512-118">Du overproduserer eller underproduserer komponentmateriale.</span><span class="sxs-lookup"><span data-stu-id="2d512-118">You over-issue or under-issue a material component.</span></span>
-   <span data-ttu-id="2d512-119">Du overrapporterer ruteoperasjon eller underrapporterer en ruteoperasjon.</span><span class="sxs-lookup"><span data-stu-id="2d512-119">You over-report or under-report the time for a routing operation.</span></span>
-   <span data-ttu-id="2d512-120">Du overmottar over eller undermottar det korrekte antallet for den overordnede varen, relativt til ordreantallet.</span><span class="sxs-lookup"><span data-stu-id="2d512-120">You over-receive or under-receive the good quantity of the parent item, relative to the order quantity.</span></span> <span data-ttu-id="2d512-121">Du kan imidlertid utstede komponenter og rapportere operasjoner fullstendig, basert på ordreantallet for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="2d512-121">However, you issue components and report operations completely, based on the order quantity for the production order.</span></span>

<span data-ttu-id="2d512-122">Her er noen vanlige kilder til et avvik i **produksjonserstatning**:</span><span class="sxs-lookup"><span data-stu-id="2d512-122">Here are some typical sources of a **production substitution** variance:</span></span>

-   <span data-ttu-id="2d512-123">Du utsteder et komponentmateriale som ikke er i produksjonsstykklisten.</span><span class="sxs-lookup"><span data-stu-id="2d512-123">You issue a material component that isn't on the production BOM.</span></span>
-   <span data-ttu-id="2d512-124">Du legger manuelt til en komponent til produksjonsstykklisten og rapporterer denne komponenten som forbruk.</span><span class="sxs-lookup"><span data-stu-id="2d512-124">You manually add a component to the production BOM and report that component as consumed.</span></span>
-   <span data-ttu-id="2d512-125">Du rapporterer en vare som forbrukt, men uten å legge den til manuelt i produksjonsstykklisten.</span><span class="sxs-lookup"><span data-stu-id="2d512-125">You report an item as consumed but don't manually add it to the production BOM.</span></span>
-   <span data-ttu-id="2d512-126">Du legger manuelt til en operasjon til produksjonsruten og rapporterer operasjonen som forbrukt.</span><span class="sxs-lookup"><span data-stu-id="2d512-126">You manually add an operation to the production route and report that operation as consumed.</span></span>
-   <span data-ttu-id="2d512-127">Når du oppretter produksjonsordren, velger du en stykklisteversjon som avviker fra stykklisteversjonen den som ble brukt i standard kostnadsberegning.</span><span class="sxs-lookup"><span data-stu-id="2d512-127">When you create the production order, you select a BOM version that differs from the BOM version that is used in the standard cost calculation.</span></span>
-   <span data-ttu-id="2d512-128">Når du oppretter produksjonsordren, velger du ruteversjonen som avviker fra ruteversjonen som ble brukt i standard kostnadsberegning.</span><span class="sxs-lookup"><span data-stu-id="2d512-128">When you create the production order, you select a route version that differs from the route version that is used in the standard cost calculation.</span></span>





