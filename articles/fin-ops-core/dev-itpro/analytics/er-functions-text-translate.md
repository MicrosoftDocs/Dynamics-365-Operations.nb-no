---
title: TRANSLATE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen TRANSLATE.
author: NickSelin
ms.date: 04/02/2020
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
ms.openlocfilehash: 7e4d6417757e27190ab7cabf2bf01243bb87b55c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746079"
---
# <a name="translate-er-function"></a><span data-ttu-id="206af-103">TRANSLATE ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="206af-103">TRANSLATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="206af-104">`TRANSLATE`-funksjonen returnerer en *Streng*-verdi som inneholder resultatet av tegnerstatningen av den angitte teksten i tegn i et annet angitt sett.</span><span class="sxs-lookup"><span data-stu-id="206af-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="206af-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="206af-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="206af-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="206af-106">Arguments</span></span>

<span data-ttu-id="206af-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="206af-107">`text`: *String*</span></span>

<span data-ttu-id="206af-108">Den gyldige banen til en datakilde av *Streng*-typen.</span><span class="sxs-lookup"><span data-stu-id="206af-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="206af-109">`pattern`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="206af-109">`pattern`: *String*</span></span>

<span data-ttu-id="206af-110">Teksten som må erstattes.</span><span class="sxs-lookup"><span data-stu-id="206af-110">The text that must be replaced.</span></span>

<span data-ttu-id="206af-111">`replacement`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="206af-111">`replacement`: *String*</span></span>

<span data-ttu-id="206af-112">Teksten som skal brukes som erstatning.</span><span class="sxs-lookup"><span data-stu-id="206af-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="206af-113">Returverdier</span><span class="sxs-lookup"><span data-stu-id="206af-113">Return values</span></span>

<span data-ttu-id="206af-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="206af-114">*String*</span></span>

<span data-ttu-id="206af-115">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="206af-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="206af-116">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="206af-116">Usage notes</span></span>

<span data-ttu-id="206af-117">`TRANSLATE`-funksjonen erstatter ett tegn om gangen.</span><span class="sxs-lookup"><span data-stu-id="206af-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="206af-118">Funksjonen erstatter det første tegnet i `text`-argumentet med det første tegnet i `pattern`-argumentet, og deretter det andre tegnet og følger den samme flyten til det er ferdig.</span><span class="sxs-lookup"><span data-stu-id="206af-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="206af-119">Når et tegn fra argumentene `text` og `pattern` er likt, erstattes det med et tegn fra `replacement`-argumentet som er plassert i samme posisjon som tegnet fra `pattern`-argumentet.</span><span class="sxs-lookup"><span data-stu-id="206af-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="206af-120">Hvis et tegn vises flere ganger i `pattern`-argumentet, brukes tilordningen av `replacement`-argumentet som tilsvarer den første forekomsten av dette tegnet.</span><span class="sxs-lookup"><span data-stu-id="206af-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="206af-121">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="206af-121">Example 1</span></span>

<span data-ttu-id="206af-122">`TRANSLATE ("abcdef", "cd", "GH")` erstatter tegnet **"c"** i den angitte teksten **"abcdef"** med tegnet **"G"** i `replacement`-teksten på grunn av følgende:</span><span class="sxs-lookup"><span data-stu-id="206af-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="206af-123">Tegnet **"c"** vises i `pattern`-teksten i første posisjon.</span><span class="sxs-lookup"><span data-stu-id="206af-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="206af-124">Den første posisjonen i `replacement`-teksten inneholder tegnet **"G"**.</span><span class="sxs-lookup"><span data-stu-id="206af-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="206af-125">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="206af-125">Example 2</span></span>

<span data-ttu-id="206af-126">`TRANSLATE ("abcdef", "ccd", "GH")` returnerer **"abGdef"**.</span><span class="sxs-lookup"><span data-stu-id="206af-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="206af-127">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="206af-127">Example 3</span></span>

<span data-ttu-id="206af-128">`TRANSLATE ("abccba", "abc", "123")` returnerer **"123321"**.</span><span class="sxs-lookup"><span data-stu-id="206af-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="206af-129">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="206af-129">Additional resources</span></span>

[<span data-ttu-id="206af-130">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="206af-130">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]