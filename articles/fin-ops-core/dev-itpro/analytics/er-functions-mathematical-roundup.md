---
title: ROUNDUP ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ROUNDUP.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d23a984bd59c4d2d37c407e3fcfed9c7017dcc7f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569341"
---
# <a name="roundup-er-function"></a><span data-ttu-id="b9453-103">ROUNDUP ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="b9453-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9453-104">`ROUNDUP`-funksjonen returnerer det angitte tallet som en *reell* verdi etter at det er rundet opp til angitt antall desimaler.</span><span class="sxs-lookup"><span data-stu-id="b9453-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9453-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="b9453-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="b9453-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="b9453-106">Arguments</span></span>

<span data-ttu-id="b9453-107">`number`: *Reell*</span><span class="sxs-lookup"><span data-stu-id="b9453-107">`number`: *Real*</span></span>

<span data-ttu-id="b9453-108">En numerisk verdi som må avrundes opp.</span><span class="sxs-lookup"><span data-stu-id="b9453-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="b9453-109">`decimals`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="b9453-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="b9453-110">En numerisk verdi som representerer antall desimaler.</span><span class="sxs-lookup"><span data-stu-id="b9453-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="b9453-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="b9453-111">Return values</span></span>

<span data-ttu-id="b9453-112">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="b9453-112">*Real*</span></span>

<span data-ttu-id="b9453-113">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="b9453-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b9453-114">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="b9453-114">Usage notes</span></span>

<span data-ttu-id="b9453-115">Denne funksjonen fungerer som [ROUND](er-functions-mathematical-round.md), men den avrunder alltid opp det angitte tallet (bort fra null).</span><span class="sxs-lookup"><span data-stu-id="b9453-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="b9453-116">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="b9453-116">Example 1</span></span>

<span data-ttu-id="b9453-117">`ROUNDUP (1200.763, 2)` avrunder opp til to desimalplasser og returnerer **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="b9453-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b9453-118">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="b9453-118">Example 2</span></span>

<span data-ttu-id="b9453-119">`ROUNDUP (1200.767, -3)` avrunder opp til nærmeste multiplum av 1 000, og returnerer **2000**.</span><span class="sxs-lookup"><span data-stu-id="b9453-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9453-120">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b9453-120">Additional resources</span></span>

[<span data-ttu-id="b9453-121">Matematiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="b9453-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]