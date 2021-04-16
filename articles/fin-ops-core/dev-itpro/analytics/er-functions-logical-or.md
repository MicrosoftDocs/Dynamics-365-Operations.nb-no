---
title: OR ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen OR
author: NickSelin
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
ms.openlocfilehash: 9763cdbabfbaba1af433c1fd753b03982ecb550d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751735"
---
# <a name="or-er-function"></a><span data-ttu-id="a35a1-103">OR ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="a35a1-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a35a1-104">`OR`-funksjonen returnerer en *boolsk* verdi av **USANN** hvis alle de angitte betingelsene er usanne.</span><span class="sxs-lookup"><span data-stu-id="a35a1-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="a35a1-105">Denne funksjonen returnerer en *boolsk* verdi av **SANN** hvis en angitt betingelse er sann.</span><span class="sxs-lookup"><span data-stu-id="a35a1-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a35a1-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="a35a1-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="a35a1-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="a35a1-107">Arguments</span></span>

<span data-ttu-id="a35a1-108">`condition 1`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="a35a1-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="a35a1-109">Et gyldig betingelsesuttrykk som må testes.</span><span class="sxs-lookup"><span data-stu-id="a35a1-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="a35a1-110">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="a35a1-110">This argument is required.</span></span>

<span data-ttu-id="a35a1-111">`condition N`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="a35a1-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="a35a1-112">Et gyldig betingelsesuttrykk som må testes.</span><span class="sxs-lookup"><span data-stu-id="a35a1-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="a35a1-113">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="a35a1-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="a35a1-114">Returverdier</span><span class="sxs-lookup"><span data-stu-id="a35a1-114">Return values</span></span>

<span data-ttu-id="a35a1-115">*Boolsk*</span><span class="sxs-lookup"><span data-stu-id="a35a1-115">*Boolean*</span></span>

<span data-ttu-id="a35a1-116">Den resulterende *boolske* verdien.</span><span class="sxs-lookup"><span data-stu-id="a35a1-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="a35a1-117">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a35a1-117">Example</span></span>

<span data-ttu-id="a35a1-118">`OR (1=2, "a"="a")` returnerer **SANN**.</span><span class="sxs-lookup"><span data-stu-id="a35a1-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a35a1-119">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a35a1-119">Additional resources</span></span>

[<span data-ttu-id="a35a1-120">Logiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="a35a1-120">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]