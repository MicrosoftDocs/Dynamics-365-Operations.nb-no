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
ms.openlocfilehash: c5c3e4c8bd918fa1154d2c111970d2f6d0e90e08
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743645"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="93a0e-103">INTVALUE ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="93a0e-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93a0e-104">`INTVALUE`-funksjonen returnerer en *Int*-verdi som representerer den angitte strengen.</span><span class="sxs-lookup"><span data-stu-id="93a0e-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="93a0e-105">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="93a0e-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="93a0e-106">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="93a0e-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="93a0e-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="93a0e-107">Arguments</span></span>

<span data-ttu-id="93a0e-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="93a0e-108">`text`: *String*</span></span>

<span data-ttu-id="93a0e-109">En tekstverdi som må konverteres til et *Int*-tall.</span><span class="sxs-lookup"><span data-stu-id="93a0e-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="93a0e-110">`number`: *Reell* eller *Heltall*</span><span class="sxs-lookup"><span data-stu-id="93a0e-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="93a0e-111">En numerisk *Reell* eller *Heltall*-verdi som må konverteres til et *Int*-tall.</span><span class="sxs-lookup"><span data-stu-id="93a0e-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="93a0e-112">Returverdier</span><span class="sxs-lookup"><span data-stu-id="93a0e-112">Return values</span></span>

<span data-ttu-id="93a0e-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="93a0e-113">*Int*</span></span>

<span data-ttu-id="93a0e-114">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="93a0e-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="93a0e-115">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="93a0e-115">Usage notes</span></span>

<span data-ttu-id="93a0e-116">Desimaler avrundes.</span><span class="sxs-lookup"><span data-stu-id="93a0e-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="93a0e-117">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="93a0e-117">Example 1</span></span>

<span data-ttu-id="93a0e-118">`INTVALUE ("100.77")` returnerer *Int*-verdien **100**.</span><span class="sxs-lookup"><span data-stu-id="93a0e-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="93a0e-119">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="93a0e-119">Example 2</span></span>

<span data-ttu-id="93a0e-120">`INTVALUE (-100.77)` returnerer *Int*-verdien **-100**.</span><span class="sxs-lookup"><span data-stu-id="93a0e-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="93a0e-121">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="93a0e-121">Additional resources</span></span>

[<span data-ttu-id="93a0e-122">Typekonverteringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="93a0e-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
