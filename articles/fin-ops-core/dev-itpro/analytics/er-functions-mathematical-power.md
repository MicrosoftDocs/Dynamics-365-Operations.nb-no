---
title: POWER ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen POWER.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 858f59cf0bc6387b09cbb6f0c59f58ba8107582c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683335"
---
# <a name="power-er-function"></a><span data-ttu-id="33244-103">POWER ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="33244-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33244-104">`POWER`-funksjonen returnerer en *reell* verdi som representerer resultatet av å heve det angitte positive tallet til den angitte potens.</span><span class="sxs-lookup"><span data-stu-id="33244-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="33244-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="33244-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="33244-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="33244-106">Arguments</span></span>

<span data-ttu-id="33244-107">`number`: *Reell* eller *Heltall*</span><span class="sxs-lookup"><span data-stu-id="33244-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="33244-108">En numerisk verdi som må heves til den angitte potens.</span><span class="sxs-lookup"><span data-stu-id="33244-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="33244-109">`power`: *Reell* eller *Heltall*</span><span class="sxs-lookup"><span data-stu-id="33244-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="33244-110">En numerisk verdi som representerer den bestemte potensen.</span><span class="sxs-lookup"><span data-stu-id="33244-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="33244-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="33244-111">Return values</span></span>

<span data-ttu-id="33244-112">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="33244-112">*Real*</span></span>

<span data-ttu-id="33244-113">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="33244-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="33244-114">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="33244-114">Example 1</span></span>

<span data-ttu-id="33244-115">`POWER (10, 2)` returnerer **100**.</span><span class="sxs-lookup"><span data-stu-id="33244-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="33244-116">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="33244-116">Example 2</span></span>

<span data-ttu-id="33244-117">`POWER (4, 0.5)` returnerer **2**.</span><span class="sxs-lookup"><span data-stu-id="33244-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33244-118">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="33244-118">Additional resources</span></span>

[<span data-ttu-id="33244-119">Matematiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="33244-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
