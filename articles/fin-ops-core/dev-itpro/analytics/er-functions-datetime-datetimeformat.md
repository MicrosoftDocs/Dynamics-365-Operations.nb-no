---
title: DATETIMEFORMAT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DATETIMEFORMAT.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 98919f40751a77465ae26acbd46af4396c588b13
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916413"
---
# <span data-ttu-id="1a207-103"><a name="DATETIMEFORMAT">DATETIMEFORMAT ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="1a207-103"><a name="DATETIMEFORMAT">DATETIMEFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a207-104">`DATETIMEFORMAT`-funksjonen returnerer en *Streng*-verdi som viser en gitt dato/klokkeslett-verdi som tekst i angitt format og i en valgfri angitt [kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="1a207-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="1a207-105">Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [egendefinert](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="1a207-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="1a207-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="1a207-106">Syntax 1</span></span>

```
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="1a207-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="1a207-107">Syntax 2</span></span>

```
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="1a207-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="1a207-108">Arguments</span></span>

<span data-ttu-id="1a207-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="1a207-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="1a207-110">En dato/klokkeslett-verdi som representerer dato og klokkeslett til-formatet.</span><span class="sxs-lookup"><span data-stu-id="1a207-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="1a207-111">`format`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="1a207-111">`format`: *String*</span></span>

<span data-ttu-id="1a207-112">Formatet til utdatastrengen.</span><span class="sxs-lookup"><span data-stu-id="1a207-112">The format of the output string.</span></span>

<span data-ttu-id="1a207-113">`culture`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="1a207-113">`culture`: *String*</span></span>

<span data-ttu-id="1a207-114">Kulturen som skal brukes til formatering.</span><span class="sxs-lookup"><span data-stu-id="1a207-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="1a207-115">Returverdier</span><span class="sxs-lookup"><span data-stu-id="1a207-115">Return values</span></span>

<span data-ttu-id="1a207-116">*Streng*</span><span class="sxs-lookup"><span data-stu-id="1a207-116">*String*</span></span>

<span data-ttu-id="1a207-117">Den resulterende strengverdien.</span><span class="sxs-lookup"><span data-stu-id="1a207-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1a207-118">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="1a207-118">Usage notes</span></span>

<span data-ttu-id="1a207-119">Når kulturen ikke er definert som et argument for den kalte funksjonen, defineres verdien for `culture` av kallkonteksten.</span><span class="sxs-lookup"><span data-stu-id="1a207-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="1a207-120">Hvis `DATETIMEFORMAT`-funksjonen for eksempel kalles ved hjelp av syntaks 1 i et ER-format for et **FIL**-element som er konfigurert til å bruke tysk kultur, vil konverteringen gjøres ved hjelp av tysk kultur.</span><span class="sxs-lookup"><span data-stu-id="1a207-120">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="1a207-121">Standardverdi for `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="1a207-121">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="1a207-122">Når `DATETIMEFORMAT`-funksjonen konverterer en gitt dato/klokkeslett-verdi, vurderes innstillingen for tidssone for programbrukeren som kjører ER-formatet som funksjonen kalles i konteksten til.</span><span class="sxs-lookup"><span data-stu-id="1a207-122">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="1a207-123">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="1a207-123">Example 1</span></span>

<span data-ttu-id="1a207-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returnerer gjeldende dato/klokkeslett-verdi for programserveren, 24. desember 2015, som **"24-12-2015"**, basert på det angitte egendefinerte formatet.</span><span class="sxs-lookup"><span data-stu-id="1a207-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="1a207-125">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="1a207-125">Example 2</span></span>

<span data-ttu-id="1a207-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returnerer gjeldende dato/klokkeslett-verdi for programøkt, 24. desember 2015, som **"24.12.2015"**, basert på den valgte tyske kulturen og det angitte formatet.</span><span class="sxs-lookup"><span data-stu-id="1a207-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="1a207-127">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="1a207-127">Example 3</span></span>

<span data-ttu-id="1a207-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returnerer strengverdien **2019-11-12T 08:00:00.0000000-08:00** når den kalles under en prosess som ble startet av en programbruker som har tidssoneverdien **(GMT-08:00) Stillehavskysten (USA og Canada)** i delen **Innstillinger for språk og land/område**.</span><span class="sxs-lookup"><span data-stu-id="1a207-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1a207-129">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="1a207-129">Additional resources</span></span>

[<span data-ttu-id="1a207-130">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="1a207-130">Date and time functions</span></span>](er-functions-category-datetime.md)
