---
title: ROUNDUP ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ROUNDUP.
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
ms.openlocfilehash: 84a62639b49db17fef1abcda75bc5ad7f08d1005
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917057"
---
# <span data-ttu-id="0c576-103"><a name="ROUNDUP">ROUNDUP ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="0c576-103"><a name="ROUNDUP">ROUNDUP ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c576-104">`ROUNDUP`-funksjonen returnerer det angitte tallet som en *reell* verdi etter at det er rundet opp til angitt antall desimaler.</span><span class="sxs-lookup"><span data-stu-id="0c576-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c576-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="0c576-105">Syntax</span></span>

```
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="0c576-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="0c576-106">Arguments</span></span>

<span data-ttu-id="0c576-107">`number`: *Reell*</span><span class="sxs-lookup"><span data-stu-id="0c576-107">`number`: *Real*</span></span>

<span data-ttu-id="0c576-108">En numerisk verdi som må avrundes opp.</span><span class="sxs-lookup"><span data-stu-id="0c576-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="0c576-109">`decimals`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="0c576-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="0c576-110">En numerisk verdi som representerer antall desimaler.</span><span class="sxs-lookup"><span data-stu-id="0c576-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="0c576-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="0c576-111">Return values</span></span>

<span data-ttu-id="0c576-112">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="0c576-112">*Real*</span></span>

<span data-ttu-id="0c576-113">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="0c576-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0c576-114">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="0c576-114">Usage notes</span></span>

<span data-ttu-id="0c576-115">Denne funksjonen fungerer som [ROUND](er-functions-mathematical-round.md), men den avrunder alltid opp det angitte tallet (bort fra null).</span><span class="sxs-lookup"><span data-stu-id="0c576-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="0c576-116">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="0c576-116">Example 1</span></span>

<span data-ttu-id="0c576-117">`ROUNDUP (1200.763, 2)` avrunder opp til to desimalplasser og returnerer **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="0c576-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0c576-118">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="0c576-118">Example 2</span></span>

<span data-ttu-id="0c576-119">`ROUNDUP (1200.767, -3)` avrunder opp til nærmeste multiplum av 1 000, og returnerer **2000**.</span><span class="sxs-lookup"><span data-stu-id="0c576-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c576-120">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0c576-120">Additional resources</span></span>

[<span data-ttu-id="0c576-121">Matematiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="0c576-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
