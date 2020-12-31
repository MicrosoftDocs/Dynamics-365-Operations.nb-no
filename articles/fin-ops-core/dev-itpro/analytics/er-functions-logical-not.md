---
title: NOT ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NOT
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
ms.openlocfilehash: 2308ab4d222863312441b3f17559ac4d3afbfb29
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686960"
---
# <a name="not-er-function"></a><span data-ttu-id="da524-103">NOT ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="da524-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da524-104">`NOT`-funksjonen returnerer den omvendte logiske verdien til den angitte betingelsen som en *boolsk* verdi.</span><span class="sxs-lookup"><span data-stu-id="da524-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="da524-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="da524-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="da524-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="da524-106">Arguments</span></span>

<span data-ttu-id="da524-107">`condition`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="da524-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="da524-108">Et gyldig betingelsesuttrykk som må tilbakeføres.</span><span class="sxs-lookup"><span data-stu-id="da524-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="da524-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="da524-109">Return values</span></span>

<span data-ttu-id="da524-110">*Boolsk*</span><span class="sxs-lookup"><span data-stu-id="da524-110">*Boolean*</span></span>

<span data-ttu-id="da524-111">Den resulterende *boolske* verdien.</span><span class="sxs-lookup"><span data-stu-id="da524-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="da524-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="da524-112">Example</span></span>

<span data-ttu-id="da524-113">`NOT (TRUE)` returnerer **USANN**.</span><span class="sxs-lookup"><span data-stu-id="da524-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da524-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="da524-114">Additional resources</span></span>

[<span data-ttu-id="da524-115">Logiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="da524-115">Logical functions</span></span>](er-functions-category-logical.md)
