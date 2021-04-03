---
title: INTVALUE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen INTVALUE.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 64f43ad29d59ade1e124b6800734b003f6ca07df
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561476"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="cb4df-103">INTVALUE ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="cb4df-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb4df-104">`INTVALUE`-funksjonen returnerer en *Int*-verdi som representerer den angitte strengen.</span><span class="sxs-lookup"><span data-stu-id="cb4df-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="cb4df-105">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="cb4df-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="cb4df-106">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="cb4df-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="cb4df-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="cb4df-107">Arguments</span></span>

<span data-ttu-id="cb4df-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="cb4df-108">`text`: *String*</span></span>

<span data-ttu-id="cb4df-109">En tekstverdi som må konverteres til et *Int*-tall.</span><span class="sxs-lookup"><span data-stu-id="cb4df-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="cb4df-110">`number`: *Reell* eller *Heltall*</span><span class="sxs-lookup"><span data-stu-id="cb4df-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="cb4df-111">En numerisk *Reell* eller *Heltall*-verdi som må konverteres til et *Int*-tall.</span><span class="sxs-lookup"><span data-stu-id="cb4df-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="cb4df-112">Returverdier</span><span class="sxs-lookup"><span data-stu-id="cb4df-112">Return values</span></span>

<span data-ttu-id="cb4df-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="cb4df-113">*Int*</span></span>

<span data-ttu-id="cb4df-114">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="cb4df-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cb4df-115">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="cb4df-115">Usage notes</span></span>

<span data-ttu-id="cb4df-116">Desimaler avrundes.</span><span class="sxs-lookup"><span data-stu-id="cb4df-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="cb4df-117">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="cb4df-117">Example 1</span></span>

<span data-ttu-id="cb4df-118">`INTVALUE ("100.77")` returnerer *Int*-verdien **100**.</span><span class="sxs-lookup"><span data-stu-id="cb4df-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="cb4df-119">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="cb4df-119">Example 2</span></span>

<span data-ttu-id="cb4df-120">`INTVALUE (-100.77)` returnerer *Int*-verdien **-100**.</span><span class="sxs-lookup"><span data-stu-id="cb4df-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb4df-121">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="cb4df-121">Additional resources</span></span>

[<span data-ttu-id="cb4df-122">Typekonverteringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="cb4df-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]