---
title: ROUNDDOWN ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ROUNDDOWN.
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
ms.openlocfilehash: 7ac559983609d4fdb80c9ac70d84031e4a231889
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744533"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="804c4-103">ROUNDDOWN ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="804c4-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="804c4-104">`ROUNDDOWN`-funksjonen returnerer det angitte tallet som en *reell* verdi etter at det er rundet ned til angitt antall desimaler.</span><span class="sxs-lookup"><span data-stu-id="804c4-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="804c4-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="804c4-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="804c4-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="804c4-106">Arguments</span></span>

<span data-ttu-id="804c4-107">`number`: *Reell*</span><span class="sxs-lookup"><span data-stu-id="804c4-107">`number`: *Real*</span></span>

<span data-ttu-id="804c4-108">En numerisk verdi som må avrundes ned.</span><span class="sxs-lookup"><span data-stu-id="804c4-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="804c4-109">`decimals`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="804c4-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="804c4-110">En numerisk verdi som representerer antall desimaler.</span><span class="sxs-lookup"><span data-stu-id="804c4-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="804c4-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="804c4-111">Return values</span></span>

<span data-ttu-id="804c4-112">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="804c4-112">*Real*</span></span>

<span data-ttu-id="804c4-113">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="804c4-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="804c4-114">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="804c4-114">Usage notes</span></span>

<span data-ttu-id="804c4-115">Denne funksjonen fungerer som [ROUND](er-functions-mathematical-round.md), men den avrunder alltid ned det angitte tallet (mot null).</span><span class="sxs-lookup"><span data-stu-id="804c4-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="804c4-116">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="804c4-116">Example 1</span></span>

<span data-ttu-id="804c4-117">`ROUNDDOWN (1200.767, 2)` avrunder ned til to desimalplasser og returnerer **1200.76**.</span><span class="sxs-lookup"><span data-stu-id="804c4-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="804c4-118">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="804c4-118">Example 2</span></span>

<span data-ttu-id="804c4-119">`ROUNDDOWN (1700.767, -3)` avrunder ned til nærmeste multiplum av 1 000, og returnerer **1000**.</span><span class="sxs-lookup"><span data-stu-id="804c4-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="804c4-120">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="804c4-120">Additional resources</span></span>

[<span data-ttu-id="804c4-121">Matematiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="804c4-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
