---
title: ROUND ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ROUND.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9384d5975e4a25d18ff741f87431daa4b0bbd7e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917080"
---
# <span data-ttu-id="de093-103"><a name="ROUND">ROUND ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="de093-103"><a name="ROUND">ROUND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de093-104">`ROUND`-funksjonen returnerer det angitte tallet som en *reell* verdi etter at det er avrundet til angitt antall desimaler.</span><span class="sxs-lookup"><span data-stu-id="de093-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="de093-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="de093-105">Syntax</span></span>

```
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="de093-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="de093-106">Arguments</span></span>

<span data-ttu-id="de093-107">`number`: *Reell*</span><span class="sxs-lookup"><span data-stu-id="de093-107">`number`: *Real*</span></span>

<span data-ttu-id="de093-108">En numerisk verdi som må avrundes.</span><span class="sxs-lookup"><span data-stu-id="de093-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="de093-109">`decimals`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="de093-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="de093-110">En numerisk verdi som representerer antall desimaler.</span><span class="sxs-lookup"><span data-stu-id="de093-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="de093-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="de093-111">Return values</span></span>

<span data-ttu-id="de093-112">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="de093-112">*Real*</span></span>

<span data-ttu-id="de093-113">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="de093-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="de093-114">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="de093-114">Usage notes</span></span>

<span data-ttu-id="de093-115">Hvis verdien for `decimals`-parameteren er større enn 0 (null), avrundes det angitte tallet til så mange desimalplasser.</span><span class="sxs-lookup"><span data-stu-id="de093-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="de093-116">Hvis verdien for `decimals`-parameteren er **0** (null), avrundes det angitte tallet til nærmeste heltall.</span><span class="sxs-lookup"><span data-stu-id="de093-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="de093-117">Hvis verdien for `decimals`-parameteren er mindre enn 0 (null), avrundes det angitte tallet til venstre for desimalpunktet.</span><span class="sxs-lookup"><span data-stu-id="de093-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="de093-118">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="de093-118">Example 1</span></span>

<span data-ttu-id="de093-119">`ROUND (1200.767, 2)` avrunder til to desimalplasser og returnerer **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="de093-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="de093-120">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="de093-120">Example 2</span></span>

<span data-ttu-id="de093-121">`ROUND (1200.767, -3)` avrunder til nærmeste multiplum av 1 000, og returnerer **1000**.</span><span class="sxs-lookup"><span data-stu-id="de093-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="de093-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="de093-122">Additional resources</span></span>

[<span data-ttu-id="de093-123">Matematiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="de093-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
