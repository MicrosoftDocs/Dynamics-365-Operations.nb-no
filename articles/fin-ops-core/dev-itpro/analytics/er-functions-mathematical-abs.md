---
title: ABS ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ABS
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
ms.openlocfilehash: 9b32c5e8a413be3583177f565e2d4909330ad1e0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917103"
---
# <span data-ttu-id="eebae-103"><a name="ABS">ABS ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="eebae-103"><a name="ABS">ABS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eebae-104">`ABS`-funksjonen returnerer den absolutte (modulus) verdien til det angitte nummeret som en *reell* verdi.</span><span class="sxs-lookup"><span data-stu-id="eebae-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="eebae-105">Altså returnes tallet uten fortegn.</span><span class="sxs-lookup"><span data-stu-id="eebae-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="eebae-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="eebae-106">Syntax</span></span>

```
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="eebae-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="eebae-107">Arguments</span></span>

<span data-ttu-id="eebae-108">`number`: *Reell*</span><span class="sxs-lookup"><span data-stu-id="eebae-108">`number`: *Real*</span></span>

<span data-ttu-id="eebae-109">En numerisk verdi du vil bruke modulus til.</span><span class="sxs-lookup"><span data-stu-id="eebae-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="eebae-110">Returverdier</span><span class="sxs-lookup"><span data-stu-id="eebae-110">Return values</span></span>

<span data-ttu-id="eebae-111">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="eebae-111">*Real*</span></span>

<span data-ttu-id="eebae-112">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="eebae-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="eebae-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="eebae-113">Example</span></span>

<span data-ttu-id="eebae-114">`ABS (-1)` returnerer **1**.</span><span class="sxs-lookup"><span data-stu-id="eebae-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eebae-115">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="eebae-115">Additional resources</span></span>

[<span data-ttu-id="eebae-116">Matematiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="eebae-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
