---
title: DATETIMEFORMAT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DATETIMEFORMAT.
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
ms.openlocfilehash: 8044f81ee59af4a11bfab38525afdac5a46acd2c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891263"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="d548d-103">DATETIMEFORMAT ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="d548d-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d548d-104">`DATETIMEFORMAT`-funksjonen returnerer en *Streng*-verdi som viser en gitt dato/klokkeslett-verdi som tekst i angitt format og i en valgfri angitt [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="d548d-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="d548d-105">Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [egendefinert](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="d548d-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="d548d-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="d548d-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="d548d-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="d548d-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="d548d-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="d548d-108">Arguments</span></span>

<span data-ttu-id="d548d-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="d548d-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="d548d-110">En dato/klokkeslett-verdi som representerer dato og klokkeslett til-formatet.</span><span class="sxs-lookup"><span data-stu-id="d548d-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="d548d-111">`format`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="d548d-111">`format`: *String*</span></span>

<span data-ttu-id="d548d-112">Formatet til utdatastrengen.</span><span class="sxs-lookup"><span data-stu-id="d548d-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="d548d-113">Det skilles mellom små og store bokstaver i formatstrengen når du bruker et standardformat eller et egendefinert format.</span><span class="sxs-lookup"><span data-stu-id="d548d-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="d548d-114">Den [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) formatangivelsen «d» returnerer for eksempel datoen ved hjelp av det korte datomønsteret, mens den standard formatangivelsen «D» returnerer ved hjelp av mønsteret med lang dato.</span><span class="sxs-lookup"><span data-stu-id="d548d-114">For example, the [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="d548d-115">Den [egendefinerte](/dotnet/standard/base-types/custom-date-and-time-format-strings) formatangivelsen «M» returnerer måneden fra 1 til og med 12, mens den egendefinerte formatangivelsen «m» returnerer minuttet fra 0 til og med 59.</span><span class="sxs-lookup"><span data-stu-id="d548d-115">Additionally, the [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="d548d-116">`culture`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="d548d-116">`culture`: *String*</span></span>

<span data-ttu-id="d548d-117">Kulturen som skal brukes til formatering.</span><span class="sxs-lookup"><span data-stu-id="d548d-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="d548d-118">Returverdier</span><span class="sxs-lookup"><span data-stu-id="d548d-118">Return values</span></span>

<span data-ttu-id="d548d-119">*Streng*</span><span class="sxs-lookup"><span data-stu-id="d548d-119">*String*</span></span>

<span data-ttu-id="d548d-120">Den resulterende strengverdien.</span><span class="sxs-lookup"><span data-stu-id="d548d-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d548d-121">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="d548d-121">Usage notes</span></span>

<span data-ttu-id="d548d-122">Hvis kulturen ikke er definert som et argument for den kalte funksjonen, defineres verdien for `culture` av kallekonteksten.</span><span class="sxs-lookup"><span data-stu-id="d548d-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="d548d-123">Hvis `DATETIMEFORMAT`-funksjonen for eksempel kalles ved hjelp av syntaks 1 i et ER-format for et **FIL**-element som er konfigurert til å bruke tysk kultur, vil konverteringen gjøres ved hjelp av tysk kultur.</span><span class="sxs-lookup"><span data-stu-id="d548d-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="d548d-124">Standardverdi for `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="d548d-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="d548d-125">Når `DATETIMEFORMAT`-funksjonen konverterer en gitt dato/klokkeslett-verdi, vurderes innstillingen for tidssone for programbrukeren som kjører ER-formatet som funksjonen kalles i konteksten til.</span><span class="sxs-lookup"><span data-stu-id="d548d-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="d548d-126">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="d548d-126">Example 1</span></span>

<span data-ttu-id="d548d-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returnerer gjeldende dato/klokkeslett-verdi for programserveren, 24. desember 2015, som **"24-12-2015"**, basert på det angitte egendefinerte formatet.</span><span class="sxs-lookup"><span data-stu-id="d548d-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="d548d-128">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="d548d-128">Example 2</span></span>

<span data-ttu-id="d548d-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returnerer gjeldende dato/klokkeslett-verdi for programøkt, 24. desember 2015, som **"24.12.2015"**, basert på den valgte tyske kulturen og det angitte formatet.</span><span class="sxs-lookup"><span data-stu-id="d548d-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="d548d-130">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="d548d-130">Example 3</span></span>

<span data-ttu-id="d548d-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returnerer strengverdien **2019-11-12T 08:00:00.0000000-08:00** når funksjonen kalles under en prosess som ble startet av en programbruker som har tidssoneverdien **(GMT-08:00) Stillehavskysten (USA og Canada)** i delen **Innstillinger for språk og land/område**.</span><span class="sxs-lookup"><span data-stu-id="d548d-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d548d-132">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d548d-132">Additional resources</span></span>

[<span data-ttu-id="d548d-133">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="d548d-133">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]