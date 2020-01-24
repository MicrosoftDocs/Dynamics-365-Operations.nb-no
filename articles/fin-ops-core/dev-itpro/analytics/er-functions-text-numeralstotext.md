---
title: NUMERALSTOTEXT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NUMERALSTOTEXT.
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
ms.openlocfilehash: 459123a66dae7a3d87a22b042e1be6585959ac15
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915631"
---
# <span data-ttu-id="44a3c-103"><a name="NUMERALSTOTEXT">NUMERALSTOTEXT ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="44a3c-103"><a name="NUMERALSTOTEXT">NUMERALSTOTEXT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44a3c-104">`NUMERALSTOTEXT`-funksjonen returnerer det angitte tallet som en *Streng*-verdi etter at det er skrevet ut (det vil si konvertert til tekststrenger) på det angitte språket.</span><span class="sxs-lookup"><span data-stu-id="44a3c-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="44a3c-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="44a3c-105">Syntax</span></span>

```
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="44a3c-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="44a3c-106">Arguments</span></span>

<span data-ttu-id="44a3c-107">`number`: *Heltall* eller *Reell*</span><span class="sxs-lookup"><span data-stu-id="44a3c-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="44a3c-108">En numerisk verdi som angir nummeret som må staves.</span><span class="sxs-lookup"><span data-stu-id="44a3c-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="44a3c-109">`language`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="44a3c-109">`language`: *String*</span></span>

<span data-ttu-id="44a3c-110">En *streng*-verdi som representerer språkkoden.</span><span class="sxs-lookup"><span data-stu-id="44a3c-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="44a3c-111">`currency`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="44a3c-111">`currency`: *String*</span></span>

<span data-ttu-id="44a3c-112">En *streng*-verdi som representerer valutakoden.</span><span class="sxs-lookup"><span data-stu-id="44a3c-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="44a3c-113">`print currency name flag`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="44a3c-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="44a3c-114">En *boolsk* verdi som angir om et valutanavn må legges til den stavede teksten.</span><span class="sxs-lookup"><span data-stu-id="44a3c-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="44a3c-115">`decimal points`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="44a3c-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="44a3c-116">En *Heltall*-verdi som angir antall desimaler som den stavede teksten skal ha.</span><span class="sxs-lookup"><span data-stu-id="44a3c-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="44a3c-117">Returverdier</span><span class="sxs-lookup"><span data-stu-id="44a3c-117">Return values</span></span>

<span data-ttu-id="44a3c-118">*Streng*</span><span class="sxs-lookup"><span data-stu-id="44a3c-118">*String*</span></span>

<span data-ttu-id="44a3c-119">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="44a3c-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="44a3c-120">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="44a3c-120">Usage notes</span></span>

<span data-ttu-id="44a3c-121">Språkkoden er valgfri.</span><span class="sxs-lookup"><span data-stu-id="44a3c-121">The language code is optional.</span></span> <span data-ttu-id="44a3c-122">Hvis den er definert som en tom streng, brukes språkkoden for kjørekontekst.</span><span class="sxs-lookup"><span data-stu-id="44a3c-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="44a3c-123">Standard språkkode er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="44a3c-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="44a3c-124">Språkkoden for konteksten som kjører, er definert i en **Mappe** eller **Fil**-element i formatet elektronisk rapportering (ER) som kjører.</span><span class="sxs-lookup"><span data-stu-id="44a3c-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="44a3c-125">Valutakoden er valgfri.</span><span class="sxs-lookup"><span data-stu-id="44a3c-125">The currency code is optional.</span></span> <span data-ttu-id="44a3c-126">Hvis den er definert som en tom streng, brukes firmakoden for kjørekontekst.</span><span class="sxs-lookup"><span data-stu-id="44a3c-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="44a3c-127">Argumentene `print currency name flag` og `decimal points` analyseres bare for følgende språkkoder: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** og **RU**.</span><span class="sxs-lookup"><span data-stu-id="44a3c-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="44a3c-128">I tillegg analyseres `print currency name flag`-argumentet bare for firmaer der land- eller områdekonteksten støtter navn for valutanedgang.</span><span class="sxs-lookup"><span data-stu-id="44a3c-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="44a3c-129">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="44a3c-129">Example 1</span></span>

<span data-ttu-id="44a3c-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returnerer **"1234 og 56"**.</span><span class="sxs-lookup"><span data-stu-id="44a3c-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="44a3c-131">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="44a3c-131">Example 2</span></span>

<span data-ttu-id="44a3c-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returnerer **"Sto dwadzieścia"**.</span><span class="sxs-lookup"><span data-stu-id="44a3c-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="44a3c-133">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="44a3c-133">Example 3</span></span>

<span data-ttu-id="44a3c-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returnerer **"Сто двадцать евро 21 евроцент"**.</span><span class="sxs-lookup"><span data-stu-id="44a3c-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="44a3c-135">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="44a3c-135">Additional resources</span></span>

[<span data-ttu-id="44a3c-136">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="44a3c-136">Text functions</span></span>](er-functions-category-text.md)