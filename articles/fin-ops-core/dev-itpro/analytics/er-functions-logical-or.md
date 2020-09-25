---
title: OR ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen OR
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
ms.openlocfilehash: faf07c5d8b30cd3babe8a6a55ae7effe5ce457a0
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744629"
---
# <a name="or-er-function"></a><span data-ttu-id="bfaa6-103">OR ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="bfaa6-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bfaa6-104">`OR`-funksjonen returnerer en *boolsk* verdi av **USANN** hvis alle de angitte betingelsene er usanne.</span><span class="sxs-lookup"><span data-stu-id="bfaa6-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="bfaa6-105">Denne funksjonen returnerer en *boolsk* verdi av **SANN** hvis en angitt betingelse er sann.</span><span class="sxs-lookup"><span data-stu-id="bfaa6-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfaa6-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="bfaa6-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="bfaa6-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="bfaa6-107">Arguments</span></span>

<span data-ttu-id="bfaa6-108">`condition 1`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="bfaa6-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="bfaa6-109">Et gyldig betingelsesuttrykk som må testes.</span><span class="sxs-lookup"><span data-stu-id="bfaa6-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="bfaa6-110">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="bfaa6-110">This argument is required.</span></span>

<span data-ttu-id="bfaa6-111">`condition N`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="bfaa6-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="bfaa6-112">Et gyldig betingelsesuttrykk som må testes.</span><span class="sxs-lookup"><span data-stu-id="bfaa6-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="bfaa6-113">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="bfaa6-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="bfaa6-114">Returverdier</span><span class="sxs-lookup"><span data-stu-id="bfaa6-114">Return values</span></span>

<span data-ttu-id="bfaa6-115">*Boolsk*</span><span class="sxs-lookup"><span data-stu-id="bfaa6-115">*Boolean*</span></span>

<span data-ttu-id="bfaa6-116">Den resulterende *boolske* verdien.</span><span class="sxs-lookup"><span data-stu-id="bfaa6-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="bfaa6-117">Eksempel</span><span class="sxs-lookup"><span data-stu-id="bfaa6-117">Example</span></span>

<span data-ttu-id="bfaa6-118">`OR (1=2, "a"="a")` returnerer **SANN**.</span><span class="sxs-lookup"><span data-stu-id="bfaa6-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bfaa6-119">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="bfaa6-119">Additional resources</span></span>

[<span data-ttu-id="bfaa6-120">Logiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="bfaa6-120">Logical functions</span></span>](er-functions-category-logical.md)
