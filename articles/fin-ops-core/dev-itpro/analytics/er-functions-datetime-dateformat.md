---
title: DATEFORMAT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DATEFORMAT.
author: NickSelin
ms.date: 01/04/2021
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
ms.openlocfilehash: 5a38f0016f69792e5beffa5d8224c70d6e5261c4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747041"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="411bd-103">DATEFORMAT ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="411bd-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="411bd-104">`DATEFORMAT`-funksjonen returnerer en *Streng*-verdi som viser en gitt datoverdi som tekst i angitt format og i en valgfri angitt [kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="411bd-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="411bd-105">Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [egendefinert](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="411bd-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="411bd-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="411bd-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="411bd-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="411bd-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="411bd-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="411bd-108">Arguments</span></span>

<span data-ttu-id="411bd-109">`date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="411bd-109">`date`: *Date*</span></span>

<span data-ttu-id="411bd-110">En datoverdi som representerer datoen som skal formateres.</span><span class="sxs-lookup"><span data-stu-id="411bd-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="411bd-111">`format`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="411bd-111">`format`: *String*</span></span>

<span data-ttu-id="411bd-112">Formatet til utdatastrengen.</span><span class="sxs-lookup"><span data-stu-id="411bd-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="411bd-113">Det skilles mellom små og store bokstaver i formatstrengen når du bruker et standardformat eller et egendefinert format.</span><span class="sxs-lookup"><span data-stu-id="411bd-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="411bd-114">Den [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) formatangivelsen «d» returnerer for eksempel datoen ved hjelp av det korte datomønsteret, mens den standard formatangivelsen «D» returnerer ved hjelp av mønsteret med lang dato.</span><span class="sxs-lookup"><span data-stu-id="411bd-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="411bd-115">Den [egendefinerte](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) formatangivelsen «M» returnerer måneden fra 1 til og med 12, mens den egendefinerte formatangivelsen «m» returnerer minuttet fra 0 til og med 59.</span><span class="sxs-lookup"><span data-stu-id="411bd-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="411bd-116">`culture`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="411bd-116">`culture`: *String*</span></span>

<span data-ttu-id="411bd-117">Kulturen som skal brukes til formatering.</span><span class="sxs-lookup"><span data-stu-id="411bd-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="411bd-118">Returverdier</span><span class="sxs-lookup"><span data-stu-id="411bd-118">Return values</span></span>

<span data-ttu-id="411bd-119">*Streng*</span><span class="sxs-lookup"><span data-stu-id="411bd-119">*String*</span></span>

<span data-ttu-id="411bd-120">Den resulterende strengverdien.</span><span class="sxs-lookup"><span data-stu-id="411bd-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="411bd-121">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="411bd-121">Usage notes</span></span>

<span data-ttu-id="411bd-122">Hvis kulturen ikke er definert som et argument for den kalte funksjonen, defineres verdien for `culture` av kallekonteksten.</span><span class="sxs-lookup"><span data-stu-id="411bd-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="411bd-123">Hvis `DATEFORMAT`-funksjonen for eksempel kalles ved hjelp av syntaks 1 i et ER-format for et **FIL**-element som er konfigurert til å bruke tysk kultur, vil konverteringen gjøres ved hjelp av tysk kultur.</span><span class="sxs-lookup"><span data-stu-id="411bd-123">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="411bd-124">Standardverdi for `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="411bd-124">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="411bd-125">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="411bd-125">Example 1</span></span>

<span data-ttu-id="411bd-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returnerer gjeldende dato for programserveren, 24. desember 2015, som strengen **"24-12-2015"**, basert på det angitte egendefinerte formatet.</span><span class="sxs-lookup"><span data-stu-id="411bd-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="411bd-127">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="411bd-127">Example 2</span></span>

<span data-ttu-id="411bd-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returnerer gjeldende programøktdato, 24. desember 2015, som strengen **"24-12-2015"**, basert på den valgte tyske kulturen og det angitte formatet.</span><span class="sxs-lookup"><span data-stu-id="411bd-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="411bd-129">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="411bd-129">Additional resources</span></span>

[<span data-ttu-id="411bd-130">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="411bd-130">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]