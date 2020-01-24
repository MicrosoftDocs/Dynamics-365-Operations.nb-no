---
title: INTVALUE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen INTVALUE.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 2b279de39cf91c3919145735518034fc60cd3341
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917724"
---
# <span data-ttu-id="0ea6b-103"><a name="INTVALUE">INTVALUE ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="0ea6b-103"><a name="INTVALUE">INTVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ea6b-104">`INTVALUE`-funksjonen returnerer en *Int*-verdi som representerer den angitte strengen.</span><span class="sxs-lookup"><span data-stu-id="0ea6b-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="0ea6b-105">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="0ea6b-105">Syntax 1</span></span>

```
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="0ea6b-106">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="0ea6b-106">Syntax 2</span></span>

```
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="0ea6b-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="0ea6b-107">Arguments</span></span>

<span data-ttu-id="0ea6b-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="0ea6b-108">`text`: *String*</span></span>

<span data-ttu-id="0ea6b-109">En tekstverdi som må konverteres til et *Int*-tall.</span><span class="sxs-lookup"><span data-stu-id="0ea6b-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="0ea6b-110">`number`: *Reell* eller *Heltall*</span><span class="sxs-lookup"><span data-stu-id="0ea6b-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="0ea6b-111">En numerisk *Reell* eller *Heltall*-verdi som må konverteres til et *Int*-tall.</span><span class="sxs-lookup"><span data-stu-id="0ea6b-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="0ea6b-112">Returverdier</span><span class="sxs-lookup"><span data-stu-id="0ea6b-112">Return values</span></span>

<span data-ttu-id="0ea6b-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="0ea6b-113">*Int*</span></span>

<span data-ttu-id="0ea6b-114">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="0ea6b-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0ea6b-115">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="0ea6b-115">Usage notes</span></span>

<span data-ttu-id="0ea6b-116">Desimaler avrundes.</span><span class="sxs-lookup"><span data-stu-id="0ea6b-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="0ea6b-117">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="0ea6b-117">Example 1</span></span>

<span data-ttu-id="0ea6b-118">`INTVALUE ("100.77")` returnerer *Int*-verdien **100**.</span><span class="sxs-lookup"><span data-stu-id="0ea6b-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0ea6b-119">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="0ea6b-119">Example 2</span></span>

<span data-ttu-id="0ea6b-120">`INTVALUE (-100.77)` returnerer *Int*-verdien **-100**.</span><span class="sxs-lookup"><span data-stu-id="0ea6b-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ea6b-121">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0ea6b-121">Additional resources</span></span>

[<span data-ttu-id="0ea6b-122">Typekonverteringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="0ea6b-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
