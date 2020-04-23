---
title: REPLACE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen REPLACE.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 83d5095620a938f1ac4b8428fff9209fda7a7831
ms.sourcegitcommit: fb8ad8e2b142441a6530b364f3258bbcc0c724d2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201072"
---
# <a name=""></a><span data-ttu-id="2cc55-103"><a name="REPLACE">REPLACE ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="2cc55-103"><a name="REPLACE">REPLACE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2cc55-104">`REPLACE`-funksjonen returnerer den angitte tekststrengen som en *streng*-verdi etter at hele eller deler av den er erstattet med en annen streng.</span><span class="sxs-lookup"><span data-stu-id="2cc55-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cc55-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="2cc55-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="2cc55-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="2cc55-106">Arguments</span></span>

<span data-ttu-id="2cc55-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="2cc55-107">`text`: *String*</span></span>

<span data-ttu-id="2cc55-108">Den gyldige banen til en datakilde av *Streng*-typen.</span><span class="sxs-lookup"><span data-stu-id="2cc55-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="2cc55-109">`pattern`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="2cc55-109">`pattern`: *String*</span></span>

<span data-ttu-id="2cc55-110">Hvis `regular expression flag`-argumentet er **USANN**, inneholder dette argumentet teksten som må erstattes.</span><span class="sxs-lookup"><span data-stu-id="2cc55-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="2cc55-111">Hvis `regular expression flag`-argumentet er **SANN**, inneholder dette argumentet et regulært uttrykk som definerer både et søkemønster og erstatningsteksten.</span><span class="sxs-lookup"><span data-stu-id="2cc55-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="2cc55-112">`replacement`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="2cc55-112">`replacement`: *String*</span></span>

<span data-ttu-id="2cc55-113">Hvis `regular expression flag`-argumentet er **USANN**, inneholder dette argumentet teksten som skal brukes som erstatning.</span><span class="sxs-lookup"><span data-stu-id="2cc55-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="2cc55-114">Hvis `regular expression flag`-argumentet er **SANN**, brukes ikke dette argumentet.</span><span class="sxs-lookup"><span data-stu-id="2cc55-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="2cc55-115">`regular expression flag`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="2cc55-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="2cc55-116">En *boolsk* verdi som angir om et regulært uttrykk brukes til å utføre erstatningen.</span><span class="sxs-lookup"><span data-stu-id="2cc55-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="2cc55-117">Returverdier</span><span class="sxs-lookup"><span data-stu-id="2cc55-117">Return values</span></span>

<span data-ttu-id="2cc55-118">*Streng*</span><span class="sxs-lookup"><span data-stu-id="2cc55-118">*String*</span></span>

<span data-ttu-id="2cc55-119">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="2cc55-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2cc55-120">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="2cc55-120">Usage notes</span></span>

<span data-ttu-id="2cc55-121">Hvis `regular expression flag`-argumentet er **SANN**, returnerer denne funksjonen den angitte strengen etter at den er endret ved å bruke det vanlige uttrykket som er angitt av `pattern`-argumentet.</span><span class="sxs-lookup"><span data-stu-id="2cc55-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="2cc55-122">Det vanlige uttrykket brukes til å søke etter tegn som skal erstattes.</span><span class="sxs-lookup"><span data-stu-id="2cc55-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="2cc55-123">Hvis argumentet `regular expression flag` er **USANN**, returnerer denne funksjonen den angitte strengen etter settet med tegn som er definert i `pattern` er erstattet av tegnene i argumentet `replacement`.</span><span class="sxs-lookup"><span data-stu-id="2cc55-123">If the `regular expression flag` argument is **FALSE**, this function returns the specified string after the set of characters that are defined in the `pattern` argument have been replaced by characters of the `replacement` argument.</span></span> 

## <a name="example-1"></a><span data-ttu-id="2cc55-124">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="2cc55-124">Example 1</span></span>

<span data-ttu-id="2cc55-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` bruker et vanlig uttrykk som fjerner alle ikke-numeriske symboler, og returnerer **"19234564971"**.</span><span class="sxs-lookup"><span data-stu-id="2cc55-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="2cc55-126">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="2cc55-126">Example 2</span></span>

<span data-ttu-id="2cc55-127">`REPLACE ("abcdef", "cd", "GH", false)` erstatter mønsteret **"cd"** med strengen **"GH"** og returnerer **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="2cc55-127">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2cc55-128">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="2cc55-128">Additional resources</span></span>

[<span data-ttu-id="2cc55-129">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="2cc55-129">Text functions</span></span>](er-functions-category-text.md)
