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
ms.openlocfilehash: 75df802b75454baeea75a8ceb32d5d045a77a3a0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916551"
---
# <span data-ttu-id="71485-103"><a name="INT64VALUE">INT64VALUE ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="71485-103"><a name="INT64VALUE">INT64VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71485-104">`INT64VALUE`-funksjonen returnerer en *Int64*-verdi som representerer den angitte strengen.</span><span class="sxs-lookup"><span data-stu-id="71485-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="71485-105">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="71485-105">Syntax 1</span></span>

```
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="71485-106">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="71485-106">Syntax 2</span></span>

```
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="71485-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="71485-107">Arguments</span></span>

<span data-ttu-id="71485-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="71485-108">`text`: *String*</span></span>

<span data-ttu-id="71485-109">En tekstverdi som må konverteres til et *Int64*-tall.</span><span class="sxs-lookup"><span data-stu-id="71485-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="71485-110">`number`: *Reell* eller *Heltall*</span><span class="sxs-lookup"><span data-stu-id="71485-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="71485-111">En numerisk *Reell* eller *Heltall*-verdi som må konverteres til et *Int64*-tall.</span><span class="sxs-lookup"><span data-stu-id="71485-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="71485-112">Returverdier</span><span class="sxs-lookup"><span data-stu-id="71485-112">Return values</span></span>

<span data-ttu-id="71485-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="71485-113">*Int64*</span></span>

<span data-ttu-id="71485-114">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="71485-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="71485-115">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="71485-115">Usage notes</span></span>

<span data-ttu-id="71485-116">Desimaler avrundes.</span><span class="sxs-lookup"><span data-stu-id="71485-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="71485-117">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="71485-117">Example 1</span></span>

<span data-ttu-id="71485-118">`INT64VALUE ("22565422744")` returnerer *Int64*-verdien **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="71485-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="71485-119">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="71485-119">Example 2</span></span>

<span data-ttu-id="71485-120">`INT64VALUE ( VALUE("22565422744.77"))` returnerer *Int64*-verdien **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="71485-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71485-121">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="71485-121">Additional resources</span></span>

[<span data-ttu-id="71485-122">Typekonverteringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="71485-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
