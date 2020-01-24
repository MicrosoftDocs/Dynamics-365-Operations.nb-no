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
ms.openlocfilehash: 81a596f5206b23001feea553adcdf6c904572775
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917126"
---
# <span data-ttu-id="4fd4c-103"><a name="OR">OR ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="4fd4c-103"><a name="OR">OR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fd4c-104">`OR`-funksjonen returnerer en *boolsk* verdi av **USANN** hvis alle de angitte betingelsene er usanne.</span><span class="sxs-lookup"><span data-stu-id="4fd4c-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="4fd4c-105">Denne funksjonen returnerer en *boolsk* verdi av **SANN** hvis en angitt betingelse er sann.</span><span class="sxs-lookup"><span data-stu-id="4fd4c-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fd4c-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="4fd4c-106">Syntax</span></span>

```
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="4fd4c-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="4fd4c-107">Arguments</span></span>

<span data-ttu-id="4fd4c-108">`condition 1`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="4fd4c-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="4fd4c-109">Et gyldig betingelsesuttrykk som må testes.</span><span class="sxs-lookup"><span data-stu-id="4fd4c-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="4fd4c-110">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="4fd4c-110">This argument is required.</span></span>

<span data-ttu-id="4fd4c-111">`condition N`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="4fd4c-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="4fd4c-112">Et gyldig betingelsesuttrykk som må testes.</span><span class="sxs-lookup"><span data-stu-id="4fd4c-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="4fd4c-113">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="4fd4c-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="4fd4c-114">Returverdier</span><span class="sxs-lookup"><span data-stu-id="4fd4c-114">Return values</span></span>

<span data-ttu-id="4fd4c-115">*Boolsk*</span><span class="sxs-lookup"><span data-stu-id="4fd4c-115">*Boolean*</span></span>

<span data-ttu-id="4fd4c-116">Den resulterende *boolske* verdien.</span><span class="sxs-lookup"><span data-stu-id="4fd4c-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="4fd4c-117">Eksempel</span><span class="sxs-lookup"><span data-stu-id="4fd4c-117">Example</span></span>

<span data-ttu-id="4fd4c-118">`OR (1=2, "a"="a")` returnerer **SANN**.</span><span class="sxs-lookup"><span data-stu-id="4fd4c-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4fd4c-119">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4fd4c-119">Additional resources</span></span>

[<span data-ttu-id="4fd4c-120">Logiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="4fd4c-120">Logical functions</span></span>](er-functions-category-logical.md)