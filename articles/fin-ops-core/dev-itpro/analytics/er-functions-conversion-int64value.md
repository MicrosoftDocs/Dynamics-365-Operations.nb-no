---
title: INT64VALUE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen INT64VALUE.
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
ms.openlocfilehash: 78b69b5280fb8c7ed99d73568097cd0c080a807a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744845"
---
# <a name="int64value-er-function"></a><span data-ttu-id="eb39d-103">INT64VALUE ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="eb39d-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb39d-104">`INT64VALUE`-funksjonen returnerer en *Int64*-verdi som representerer den angitte strengen.</span><span class="sxs-lookup"><span data-stu-id="eb39d-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="eb39d-105">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="eb39d-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="eb39d-106">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="eb39d-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="eb39d-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="eb39d-107">Arguments</span></span>

<span data-ttu-id="eb39d-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="eb39d-108">`text`: *String*</span></span>

<span data-ttu-id="eb39d-109">En tekstverdi som må konverteres til et *Int64*-tall.</span><span class="sxs-lookup"><span data-stu-id="eb39d-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="eb39d-110">`number`: *Reell* eller *Heltall*</span><span class="sxs-lookup"><span data-stu-id="eb39d-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="eb39d-111">En numerisk *Reell* eller *Heltall*-verdi som må konverteres til et *Int64*-tall.</span><span class="sxs-lookup"><span data-stu-id="eb39d-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="eb39d-112">Returverdier</span><span class="sxs-lookup"><span data-stu-id="eb39d-112">Return values</span></span>

<span data-ttu-id="eb39d-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="eb39d-113">*Int64*</span></span>

<span data-ttu-id="eb39d-114">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="eb39d-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="eb39d-115">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="eb39d-115">Usage notes</span></span>

<span data-ttu-id="eb39d-116">Desimaler avrundes.</span><span class="sxs-lookup"><span data-stu-id="eb39d-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="eb39d-117">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="eb39d-117">Example 1</span></span>

<span data-ttu-id="eb39d-118">`INT64VALUE ("22565422744")` returnerer *Int64*-verdien **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="eb39d-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="eb39d-119">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="eb39d-119">Example 2</span></span>

<span data-ttu-id="eb39d-120">`INT64VALUE ( VALUE("22565422744.77"))` returnerer *Int64*-verdien **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="eb39d-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb39d-121">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="eb39d-121">Additional resources</span></span>

[<span data-ttu-id="eb39d-122">Typekonverteringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="eb39d-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
