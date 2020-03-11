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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a518f255a4488c5ed6e007b1787e678fd88aff36
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041728"
---
# <span data-ttu-id="7f090-103"><a name="NOT">NOT ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="7f090-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f090-104">`NOT`-funksjonen returnerer den omvendte logiske verdien til den angitte betingelsen som en *boolsk* verdi.</span><span class="sxs-lookup"><span data-stu-id="7f090-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f090-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="7f090-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="7f090-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="7f090-106">Arguments</span></span>

<span data-ttu-id="7f090-107">`condition`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="7f090-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="7f090-108">Et gyldig betingelsesuttrykk som må tilbakeføres.</span><span class="sxs-lookup"><span data-stu-id="7f090-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="7f090-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="7f090-109">Return values</span></span>

<span data-ttu-id="7f090-110">*Boolsk*</span><span class="sxs-lookup"><span data-stu-id="7f090-110">*Boolean*</span></span>

<span data-ttu-id="7f090-111">Den resulterende *boolske* verdien.</span><span class="sxs-lookup"><span data-stu-id="7f090-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="7f090-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="7f090-112">Example</span></span>

<span data-ttu-id="7f090-113">`NOT (TRUE)` returnerer **USANN**.</span><span class="sxs-lookup"><span data-stu-id="7f090-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f090-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="7f090-114">Additional resources</span></span>

[<span data-ttu-id="7f090-115">Logiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="7f090-115">Logical functions</span></span>](er-functions-category-logical.md)
