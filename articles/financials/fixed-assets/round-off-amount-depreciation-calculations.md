---
title: "Avrundingsbeløp for avskrivningsberegninger"
description: "Denne artikkelen omhandler feltet Avrundingsavskrivning som finnes på Tablåoppsett-sidene."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0ad57b076542c38d3c29dba4caacf830de6f7200
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="dcd90-103">Avrundingsbeløp for avskrivningsberegninger</span><span class="sxs-lookup"><span data-stu-id="dcd90-103">Round-off amount for depreciation calculations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="dcd90-104">Denne artikkelen omhandler feltet Avrundingsavskrivning som finnes på Tablåoppsett-sidene.</span><span class="sxs-lookup"><span data-stu-id="dcd90-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="dcd90-105">Avrundingsbeløp for avskrivning angis for hvert tablå.</span><span class="sxs-lookup"><span data-stu-id="dcd90-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="dcd90-106">Avrundingsbeløp for avskrivning brukes i avskrivningsprofilen for anleggsmiddel som viser fremtidig avskrivning og verdi for anleggsmiddelet, også i avskrivningsforslag.</span><span class="sxs-lookup"><span data-stu-id="dcd90-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="dcd90-107">Angi det laveste avskrivningsbeløpet som er tillatt for tablået.</span><span class="sxs-lookup"><span data-stu-id="dcd90-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="dcd90-108">Uavhengig av avrundingen som er angitt, blir avskrivningsbeløpet i den siste avskrivningsperioden ikke avrundet.</span><span class="sxs-lookup"><span data-stu-id="dcd90-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="dcd90-109">På slutten av siste avskrivningsperiode må verdien av anleggsmiddelet være 0 (null) eller skrapverdien, hvis skrapverdi brukes.</span><span class="sxs-lookup"><span data-stu-id="dcd90-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="dcd90-110">Eksempel</span><span class="sxs-lookup"><span data-stu-id="dcd90-110">Example</span></span>

<span data-ttu-id="dcd90-111">Avskrivning uten avrunding beregnes som 2 444,44.</span><span class="sxs-lookup"><span data-stu-id="dcd90-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="dcd90-112">Som følgende tabell viser varierer beløpene som foreslås, avhengig av hvordan avrunding er satt opp.</span><span class="sxs-lookup"><span data-stu-id="dcd90-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="dcd90-113">Avrundingsmetode</span><span class="sxs-lookup"><span data-stu-id="dcd90-113">Rounding method</span></span> | <span data-ttu-id="dcd90-114">Avskrivningsbeløp</span><span class="sxs-lookup"><span data-stu-id="dcd90-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="dcd90-115">Avrunding 0,1</span><span class="sxs-lookup"><span data-stu-id="dcd90-115">Rounding 0.1</span></span>    | <span data-ttu-id="dcd90-116">2 444,40</span><span class="sxs-lookup"><span data-stu-id="dcd90-116">2,444.40</span></span>            |
| <span data-ttu-id="dcd90-117">Avrunding 1,00</span><span class="sxs-lookup"><span data-stu-id="dcd90-117">Rounding 1.00</span></span>   | <span data-ttu-id="dcd90-118">2 444,00</span><span class="sxs-lookup"><span data-stu-id="dcd90-118">2,444.00</span></span>            |
| <span data-ttu-id="dcd90-119">Avrunding 10,00</span><span class="sxs-lookup"><span data-stu-id="dcd90-119">Rounding 10.00</span></span>  | <span data-ttu-id="dcd90-120">2 440,00</span><span class="sxs-lookup"><span data-stu-id="dcd90-120">2,440.00</span></span>            |
| <span data-ttu-id="dcd90-121">Avrunding 100,00</span><span class="sxs-lookup"><span data-stu-id="dcd90-121">Rounding 100.00</span></span> | <span data-ttu-id="dcd90-122">2 400,00</span><span class="sxs-lookup"><span data-stu-id="dcd90-122">2,400.00</span></span>            |






