---
title: ROUND ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ROUND.
author: NickSelin
manager: kfend
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83fb5c04938e0aba1277f2d6017d4b66208a8858
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683262"
---
# <a name="round-er-function"></a><span data-ttu-id="b48de-103">ROUND ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="b48de-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b48de-104">`ROUND`-funksjonen returnerer det angitte tallet som en *reell* verdi etter at det er avrundet til angitt antall desimaler.</span><span class="sxs-lookup"><span data-stu-id="b48de-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="b48de-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="b48de-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="b48de-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="b48de-106">Arguments</span></span>

<span data-ttu-id="b48de-107">`number`: *Reell*</span><span class="sxs-lookup"><span data-stu-id="b48de-107">`number`: *Real*</span></span>

<span data-ttu-id="b48de-108">En numerisk verdi som må avrundes.</span><span class="sxs-lookup"><span data-stu-id="b48de-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="b48de-109">`decimals`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="b48de-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="b48de-110">En numerisk verdi som representerer antall desimaler.</span><span class="sxs-lookup"><span data-stu-id="b48de-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="b48de-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="b48de-111">Return values</span></span>

<span data-ttu-id="b48de-112">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="b48de-112">*Real*</span></span>

<span data-ttu-id="b48de-113">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="b48de-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b48de-114">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="b48de-114">Usage notes</span></span>

<span data-ttu-id="b48de-115">Hvis verdien for `decimals`-parameteren er større enn 0 (null), avrundes det angitte tallet til så mange desimalplasser.</span><span class="sxs-lookup"><span data-stu-id="b48de-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="b48de-116">Hvis verdien for `decimals`-parameteren er **0** (null), avrundes det angitte tallet til nærmeste jevne heltall.</span><span class="sxs-lookup"><span data-stu-id="b48de-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest even integer.</span></span>

<span data-ttu-id="b48de-117">Hvis verdien for `decimals`-parameteren er mindre enn 0 (null), avrundes det angitte tallet til venstre for desimalpunktet.</span><span class="sxs-lookup"><span data-stu-id="b48de-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="b48de-118">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="b48de-118">Example 1</span></span>

<span data-ttu-id="b48de-119">`ROUND (1200.767, 2)` avrunder til to desimalplasser og returnerer **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="b48de-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b48de-120">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="b48de-120">Example 2</span></span>

<span data-ttu-id="b48de-121">`ROUND (1200.767, -3)` avrunder til nærmeste multiplum av 1 000, og returnerer **1000**.</span><span class="sxs-lookup"><span data-stu-id="b48de-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="example-3"></a><span data-ttu-id="b48de-122">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="b48de-122">Example 3</span></span>

<span data-ttu-id="b48de-123">`ROUND (1200.5, 0)` avrunder til nærmeste jevne heltall og returnerer **1200**, mens `ROUND (1201.5, 0)` gjør det samme og returnerer **1202**.</span><span class="sxs-lookup"><span data-stu-id="b48de-123">`ROUND (1200.5, 0)` rounds to the nearest even integer and returns **1200**, while `ROUND (1201.5, 0)` does the same and returns **1202**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b48de-124">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b48de-124">Additional resources</span></span>

[<span data-ttu-id="b48de-125">Matematiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="b48de-125">Mathematical functions</span></span>](er-functions-category-mathematical.md)
