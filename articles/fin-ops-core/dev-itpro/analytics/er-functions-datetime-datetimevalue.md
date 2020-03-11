---
title: DATETIMEVALUE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DATETIMEVALUE.
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
ms.openlocfilehash: 29d81599563dec2827fa8a82c86b74cb9e34eea2
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070696"
---
# <span data-ttu-id="8b326-103"><a name="DATETIMEVALUE">DATETIMEVALUE ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="8b326-103"><a name="DATETIMEVALUE">DATETIMEVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b326-104">`DATETIMEVALUE`-funksjonen returnerer en *DateTime*-verdi som konverteres fra en gitt tekstverdi i angitt format og i en valgfri angitt [kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) til en dato/klokkeslett-verdi.</span><span class="sxs-lookup"><span data-stu-id="8b326-104">The `DATETIMEVALUE` function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date/time value.</span></span> <span data-ttu-id="8b326-105">Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [egendefinert](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="8b326-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="8b326-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="8b326-106">Syntax 1</span></span>

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="8b326-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="8b326-107">Syntax 2</span></span>

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="8b326-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="8b326-108">Arguments</span></span>

<span data-ttu-id="8b326-109">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="8b326-109">`text`: *String*</span></span>

<span data-ttu-id="8b326-110">Tekst som representerer verdien som skal formateres.</span><span class="sxs-lookup"><span data-stu-id="8b326-110">Text that represents the value to format.</span></span>

<span data-ttu-id="8b326-111">`format`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="8b326-111">`format`: *String*</span></span>

<span data-ttu-id="8b326-112">Formatet til den gitte teksten.</span><span class="sxs-lookup"><span data-stu-id="8b326-112">The format of the given text.</span></span>

<span data-ttu-id="8b326-113">`culture`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="8b326-113">`culture`: *String*</span></span>

<span data-ttu-id="8b326-114">Kulturen som brukes til formatering av den gitte teksten.</span><span class="sxs-lookup"><span data-stu-id="8b326-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="8b326-115">Returverdier</span><span class="sxs-lookup"><span data-stu-id="8b326-115">Return values</span></span>

<span data-ttu-id="8b326-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="8b326-116">*DateTime*</span></span>

<span data-ttu-id="8b326-117">Den resulterende dato/klokkeslett-verdien.</span><span class="sxs-lookup"><span data-stu-id="8b326-117">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8b326-118">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="8b326-118">Usage notes</span></span>

<span data-ttu-id="8b326-119">Når kulturen ikke er definert som et argument for den kalte funksjonen, defineres verdien for `culture` av kallkonteksten.</span><span class="sxs-lookup"><span data-stu-id="8b326-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="8b326-120">Hvis `DATETIMEVALUE`-funksjonen for eksempel kalles ved hjelp av syntaks 1 i et ER-format for et **FIL**-element som er konfigurert til å bruke tysk kultur, vil konverteringen gjøres ved hjelp av tysk kultur.</span><span class="sxs-lookup"><span data-stu-id="8b326-120">For example, if the `DATETIMEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="8b326-121">Standardverdi for `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="8b326-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="8b326-122">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="8b326-122">Example 1</span></span>

<span data-ttu-id="8b326-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returnerer **2:55:00 AM den 21. desember 2016**, basert på det spesifiserte egendefinerte formatet og standardprogrammets **EN-US**-kultur.</span><span class="sxs-lookup"><span data-stu-id="8b326-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="8b326-124">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="8b326-124">Example 2</span></span>

<span data-ttu-id="8b326-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returnerer **2:55:00 AM den 21. desember 2016**, basert på spesifisert egendefinert format og kultur.</span><span class="sxs-lookup"><span data-stu-id="8b326-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="8b326-126">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` vil imidlertid iverksette et unntak for å informere brukeren om at den angitte strengen ikke gjenkjennes som en gyldig dato/klokkeslett-verdi for den angitte kulturen.</span><span class="sxs-lookup"><span data-stu-id="8b326-126">However, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date/time value for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8b326-127">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8b326-127">Additional resources</span></span>

[<span data-ttu-id="8b326-128">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="8b326-128">Date and time functions</span></span>](er-functions-category-datetime.md)
