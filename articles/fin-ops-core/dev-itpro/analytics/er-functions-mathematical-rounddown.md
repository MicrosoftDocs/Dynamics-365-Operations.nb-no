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
ms.openlocfilehash: 92150bb23e76f82907e0f3e8f0738b25801958bf
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041570"
---
# <span data-ttu-id="46dfc-103"><a name="ROUNDDOWN">ROUNDDOWN ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="46dfc-103"><a name="ROUNDDOWN">ROUNDDOWN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46dfc-104">`ROUNDDOWN`-funksjonen returnerer det angitte tallet som en *reell* verdi etter at det er rundet ned til angitt antall desimaler.</span><span class="sxs-lookup"><span data-stu-id="46dfc-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="46dfc-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="46dfc-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="46dfc-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="46dfc-106">Arguments</span></span>

<span data-ttu-id="46dfc-107">`number`: *Reell*</span><span class="sxs-lookup"><span data-stu-id="46dfc-107">`number`: *Real*</span></span>

<span data-ttu-id="46dfc-108">En numerisk verdi som må avrundes ned.</span><span class="sxs-lookup"><span data-stu-id="46dfc-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="46dfc-109">`decimals`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="46dfc-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="46dfc-110">En numerisk verdi som representerer antall desimaler.</span><span class="sxs-lookup"><span data-stu-id="46dfc-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="46dfc-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="46dfc-111">Return values</span></span>

<span data-ttu-id="46dfc-112">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="46dfc-112">*Real*</span></span>

<span data-ttu-id="46dfc-113">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="46dfc-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="46dfc-114">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="46dfc-114">Usage notes</span></span>

<span data-ttu-id="46dfc-115">Denne funksjonen fungerer som [ROUND](er-functions-mathematical-round.md), men den avrunder alltid ned det angitte tallet (mot null).</span><span class="sxs-lookup"><span data-stu-id="46dfc-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="46dfc-116">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="46dfc-116">Example 1</span></span>

<span data-ttu-id="46dfc-117">`ROUNDDOWN (1200.767, 2)` avrunder ned til to desimalplasser og returnerer **1200.76**.</span><span class="sxs-lookup"><span data-stu-id="46dfc-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="46dfc-118">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="46dfc-118">Example 2</span></span>

<span data-ttu-id="46dfc-119">`ROUNDDOWN (1700.767, -3)` avrunder ned til nærmeste multiplum av 1 000, og returnerer **1000**.</span><span class="sxs-lookup"><span data-stu-id="46dfc-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="46dfc-120">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="46dfc-120">Additional resources</span></span>

[<span data-ttu-id="46dfc-121">Matematiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="46dfc-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
