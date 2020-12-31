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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c7156b9990397822a6bea9ed8b3df8f65490572
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683287"
---
# <a name="abs-er-function"></a><span data-ttu-id="9e682-103">ABS ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="9e682-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e682-104">`ABS`-funksjonen returnerer den absolutte (modulus) verdien til det angitte nummeret som en *reell* verdi.</span><span class="sxs-lookup"><span data-stu-id="9e682-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="9e682-105">Altså returnes tallet uten fortegn.</span><span class="sxs-lookup"><span data-stu-id="9e682-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e682-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="9e682-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="9e682-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="9e682-107">Arguments</span></span>

<span data-ttu-id="9e682-108">`number`: *Reell*</span><span class="sxs-lookup"><span data-stu-id="9e682-108">`number`: *Real*</span></span>

<span data-ttu-id="9e682-109">En numerisk verdi du vil bruke modulus til.</span><span class="sxs-lookup"><span data-stu-id="9e682-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="9e682-110">Returverdier</span><span class="sxs-lookup"><span data-stu-id="9e682-110">Return values</span></span>

<span data-ttu-id="9e682-111">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="9e682-111">*Real*</span></span>

<span data-ttu-id="9e682-112">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="9e682-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="9e682-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="9e682-113">Example</span></span>

<span data-ttu-id="9e682-114">`ABS (-1)` returnerer **1**.</span><span class="sxs-lookup"><span data-stu-id="9e682-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9e682-115">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="9e682-115">Additional resources</span></span>

[<span data-ttu-id="9e682-116">Matematiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="9e682-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
