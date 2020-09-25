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
ms.openlocfilehash: 12af71a024a76fca98fc2e876da9b59e5762cf07
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744557"
---
# <a name="round-er-function"></a><span data-ttu-id="ba657-103">ROUND ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="ba657-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba657-104">`ROUND`-funksjonen returnerer det angitte tallet som en *reell* verdi etter at det er avrundet til angitt antall desimaler.</span><span class="sxs-lookup"><span data-stu-id="ba657-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba657-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="ba657-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="ba657-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="ba657-106">Arguments</span></span>

<span data-ttu-id="ba657-107">`number`: *Reell*</span><span class="sxs-lookup"><span data-stu-id="ba657-107">`number`: *Real*</span></span>

<span data-ttu-id="ba657-108">En numerisk verdi som må avrundes.</span><span class="sxs-lookup"><span data-stu-id="ba657-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="ba657-109">`decimals`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="ba657-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="ba657-110">En numerisk verdi som representerer antall desimaler.</span><span class="sxs-lookup"><span data-stu-id="ba657-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="ba657-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="ba657-111">Return values</span></span>

<span data-ttu-id="ba657-112">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="ba657-112">*Real*</span></span>

<span data-ttu-id="ba657-113">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="ba657-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ba657-114">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="ba657-114">Usage notes</span></span>

<span data-ttu-id="ba657-115">Hvis verdien for `decimals`-parameteren er større enn 0 (null), avrundes det angitte tallet til så mange desimalplasser.</span><span class="sxs-lookup"><span data-stu-id="ba657-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="ba657-116">Hvis verdien for `decimals`-parameteren er **0** (null), avrundes det angitte tallet til nærmeste heltall.</span><span class="sxs-lookup"><span data-stu-id="ba657-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="ba657-117">Hvis verdien for `decimals`-parameteren er mindre enn 0 (null), avrundes det angitte tallet til venstre for desimalpunktet.</span><span class="sxs-lookup"><span data-stu-id="ba657-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="ba657-118">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="ba657-118">Example 1</span></span>

<span data-ttu-id="ba657-119">`ROUND (1200.767, 2)` avrunder til to desimalplasser og returnerer **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="ba657-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ba657-120">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="ba657-120">Example 2</span></span>

<span data-ttu-id="ba657-121">`ROUND (1200.767, -3)` avrunder til nærmeste multiplum av 1 000, og returnerer **1000**.</span><span class="sxs-lookup"><span data-stu-id="ba657-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ba657-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ba657-122">Additional resources</span></span>

[<span data-ttu-id="ba657-123">Matematiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="ba657-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
