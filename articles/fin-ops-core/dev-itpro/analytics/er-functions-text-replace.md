---
title: REPLACE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen REPLACE.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: d9c66f4c96f35e3ad5fc92e7925b5cd07c956aac
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916873"
---
# <span data-ttu-id="1c090-103"><a name="REPLACE">REPLACE ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="1c090-103"><a name="REPLACE">REPLACE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c090-104">`REPLACE`-funksjonen returnerer den angitte tekststrengen som en *streng*-verdi etter at hele eller deler av den er erstattet med en annen streng.</span><span class="sxs-lookup"><span data-stu-id="1c090-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c090-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="1c090-105">Syntax</span></span>

```
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="1c090-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="1c090-106">Arguments</span></span>

<span data-ttu-id="1c090-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="1c090-107">`text`: *String*</span></span>

<span data-ttu-id="1c090-108">Den gyldige banen til en datakilde av *Streng*-typen.</span><span class="sxs-lookup"><span data-stu-id="1c090-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="1c090-109">`pattern`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="1c090-109">`pattern`: *String*</span></span>

<span data-ttu-id="1c090-110">Hvis `regular expression flag`-argumentet er **USANN**, inneholder dette argumentet teksten som må erstattes.</span><span class="sxs-lookup"><span data-stu-id="1c090-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="1c090-111">Hvis `regular expression flag`-argumentet er **SANN**, inneholder dette argumentet et regulært uttrykk som definerer både et søkemønster og erstatningsteksten.</span><span class="sxs-lookup"><span data-stu-id="1c090-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="1c090-112">`replacement`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="1c090-112">`replacement`: *String*</span></span>

<span data-ttu-id="1c090-113">Hvis `regular expression flag`-argumentet er **USANN**, inneholder dette argumentet teksten som skal brukes som erstatning.</span><span class="sxs-lookup"><span data-stu-id="1c090-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="1c090-114">Hvis `regular expression flag`-argumentet er **SANN**, brukes ikke dette argumentet.</span><span class="sxs-lookup"><span data-stu-id="1c090-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="1c090-115">`regular expression flag`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="1c090-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="1c090-116">En *boolsk* verdi som angir om et regulært uttrykk brukes til å utføre erstatningen.</span><span class="sxs-lookup"><span data-stu-id="1c090-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="1c090-117">Returverdier</span><span class="sxs-lookup"><span data-stu-id="1c090-117">Return values</span></span>

<span data-ttu-id="1c090-118">*Streng*</span><span class="sxs-lookup"><span data-stu-id="1c090-118">*String*</span></span>

<span data-ttu-id="1c090-119">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="1c090-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1c090-120">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="1c090-120">Usage notes</span></span>

<span data-ttu-id="1c090-121">Hvis `regular expression flag`-argumentet er **SANN**, returnerer denne funksjonen den angitte strengen etter at den er endret ved å bruke det vanlige uttrykket som er angitt av `pattern`-argumentet.</span><span class="sxs-lookup"><span data-stu-id="1c090-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="1c090-122">Det vanlige uttrykket brukes til å søke etter tegn som skal erstattes.</span><span class="sxs-lookup"><span data-stu-id="1c090-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="1c090-123">Hvis argumentet `regular expression flag` er **USANN**, oppfører denne funksjonen seg som [TRANSLATE](er-functions-text-translate.md).</span><span class="sxs-lookup"><span data-stu-id="1c090-123">If the `regular expression flag` argument is **FALSE**, this function behaves like [TRANSLATE](er-functions-text-translate.md).</span></span> <span data-ttu-id="1c090-124">Tegnene som er angitt av `replacement`-argumentet, brukes til å erstatte tegnene som blir funnet.</span><span class="sxs-lookup"><span data-stu-id="1c090-124">The characters that are specified by the `replacement` argument are used to replace the characters that are found.</span></span> 

## <a name="example-1"></a><span data-ttu-id="1c090-125">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="1c090-125">Example 1</span></span>

<span data-ttu-id="1c090-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` bruker et vanlig uttrykk som fjerner alle ikke-numeriske symboler, og returnerer **"19234564971"**.</span><span class="sxs-lookup"><span data-stu-id="1c090-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="1c090-127">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="1c090-127">Example 2</span></span>

<span data-ttu-id="1c090-128">`REPLACE ("abcdef", "cd", "GH", false)` erstatter mønsteret **"cd"** med strengen **"GH"** og returnerer **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="1c090-128">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c090-129">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="1c090-129">Additional resources</span></span>

[<span data-ttu-id="1c090-130">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="1c090-130">Text functions</span></span>](er-functions-category-text.md)
