---
title: DATEFORMAT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DATEFORMAT.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 1fa6bdef2168112aeb17e0edb9f9a6d1b3bd45c0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684939"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="6c92f-103">DATEFORMAT ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="6c92f-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c92f-104">`DATEFORMAT`-funksjonen returnerer en *Streng*-verdi som viser en gitt datoverdi som tekst i angitt format og i en valgfri angitt [kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="6c92f-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="6c92f-105">Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [egendefinert](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="6c92f-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="6c92f-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="6c92f-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="6c92f-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="6c92f-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="6c92f-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="6c92f-108">Arguments</span></span>

<span data-ttu-id="6c92f-109">`date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="6c92f-109">`date`: *Date*</span></span>

<span data-ttu-id="6c92f-110">En datoverdi som representerer datoen som skal formateres.</span><span class="sxs-lookup"><span data-stu-id="6c92f-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="6c92f-111">`format`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="6c92f-111">`format`: *String*</span></span>

<span data-ttu-id="6c92f-112">Formatet til utdatastrengen.</span><span class="sxs-lookup"><span data-stu-id="6c92f-112">The format of the output string.</span></span>

<span data-ttu-id="6c92f-113">`culture`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="6c92f-113">`culture`: *String*</span></span>

<span data-ttu-id="6c92f-114">Kulturen som skal brukes til formatering.</span><span class="sxs-lookup"><span data-stu-id="6c92f-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="6c92f-115">Returverdier</span><span class="sxs-lookup"><span data-stu-id="6c92f-115">Return values</span></span>

<span data-ttu-id="6c92f-116">*Streng*</span><span class="sxs-lookup"><span data-stu-id="6c92f-116">*String*</span></span>

<span data-ttu-id="6c92f-117">Den resulterende strengverdien.</span><span class="sxs-lookup"><span data-stu-id="6c92f-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6c92f-118">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="6c92f-118">Usage notes</span></span>

<span data-ttu-id="6c92f-119">Når kulturen ikke er definert som et argument for den kalte funksjonen, defineres verdien for `culture` av kallkonteksten.</span><span class="sxs-lookup"><span data-stu-id="6c92f-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="6c92f-120">Hvis `DATEFORMAT`-funksjonen for eksempel kalles ved hjelp av syntaks 1 i et ER-format for et **FIL**-element som er konfigurert til å bruke tysk kultur, vil konverteringen gjøres ved hjelp av tysk kultur.</span><span class="sxs-lookup"><span data-stu-id="6c92f-120">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="6c92f-121">Standardverdi for `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="6c92f-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="6c92f-122">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="6c92f-122">Example 1</span></span>

<span data-ttu-id="6c92f-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returnerer gjeldende dato for programserveren, 24. desember 2015, som strengen **"24-12-2015"**, basert på det angitte egendefinerte formatet.</span><span class="sxs-lookup"><span data-stu-id="6c92f-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="6c92f-124">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="6c92f-124">Example 2</span></span>

<span data-ttu-id="6c92f-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returnerer gjeldende programøktdato, 24. desember 2015, som strengen  **"24-12-2015"**, basert på den valgte tyske kulturen og det angitte formatet.</span><span class="sxs-lookup"><span data-stu-id="6c92f-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string  **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c92f-126">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6c92f-126">Additional resources</span></span>

[<span data-ttu-id="6c92f-127">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="6c92f-127">Date and time functions</span></span>](er-functions-category-datetime.md)
