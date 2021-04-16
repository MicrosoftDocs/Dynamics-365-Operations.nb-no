---
title: DATETIMEVALUE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DATETIMEVALUE.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: cec8f16e683c7eb808fc353830f2baa5c46e31d1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747017"
---
# <a name="datetimevalue-er-function"></a><span data-ttu-id="07069-103">DATETIMEVALUE ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="07069-103">DATETIMEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07069-104">`DATETIMEVALUE`-funksjonen returnerer en *DateTime*-verdi som konverteres fra en gitt tekstverdi i angitt format og i en valgfri angitt [kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) til en dato/klokkeslett-verdi.</span><span class="sxs-lookup"><span data-stu-id="07069-104">The `DATETIMEVALUE` function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date/time value.</span></span> <span data-ttu-id="07069-105">Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [egendefinert](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="07069-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="07069-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="07069-106">Syntax 1</span></span>

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="07069-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="07069-107">Syntax 2</span></span>

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="07069-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="07069-108">Arguments</span></span>

<span data-ttu-id="07069-109">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="07069-109">`text`: *String*</span></span>

<span data-ttu-id="07069-110">Tekst som representerer verdien som skal formateres.</span><span class="sxs-lookup"><span data-stu-id="07069-110">Text that represents the value to format.</span></span>

<span data-ttu-id="07069-111">`format`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="07069-111">`format`: *String*</span></span>

<span data-ttu-id="07069-112">Formatet til den gitte teksten.</span><span class="sxs-lookup"><span data-stu-id="07069-112">The format of the given text.</span></span>

<span data-ttu-id="07069-113">`culture`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="07069-113">`culture`: *String*</span></span>

<span data-ttu-id="07069-114">Kulturen som brukes til formatering av den gitte teksten.</span><span class="sxs-lookup"><span data-stu-id="07069-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="07069-115">Returverdier</span><span class="sxs-lookup"><span data-stu-id="07069-115">Return values</span></span>

<span data-ttu-id="07069-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="07069-116">*DateTime*</span></span>

<span data-ttu-id="07069-117">Den resulterende dato/klokkeslett-verdien.</span><span class="sxs-lookup"><span data-stu-id="07069-117">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="07069-118">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="07069-118">Usage notes</span></span>

<span data-ttu-id="07069-119">Når kulturen ikke er definert som et argument for den kalte funksjonen, defineres verdien for `culture` av kallkonteksten.</span><span class="sxs-lookup"><span data-stu-id="07069-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="07069-120">Hvis `DATETIMEVALUE`-funksjonen for eksempel kalles ved hjelp av syntaks 1 i et ER-format for et **FIL**-element som er konfigurert til å bruke tysk kultur, vil konverteringen gjøres ved hjelp av tysk kultur.</span><span class="sxs-lookup"><span data-stu-id="07069-120">For example, if the `DATETIMEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="07069-121">Standardverdi for `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="07069-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="07069-122">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="07069-122">Example 1</span></span>

<span data-ttu-id="07069-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returnerer **2:55:00 AM den 21. desember 2016**, basert på det spesifiserte egendefinerte formatet og standardprogrammets **EN-US**-kultur.</span><span class="sxs-lookup"><span data-stu-id="07069-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="07069-124">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="07069-124">Example 2</span></span>

<span data-ttu-id="07069-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returnerer **2:55:00 AM den 21. desember 2016**, basert på spesifisert egendefinert format og kultur.</span><span class="sxs-lookup"><span data-stu-id="07069-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="07069-126">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` vil imidlertid iverksette et unntak for å informere brukeren om at den angitte strengen ikke gjenkjennes som en gyldig dato/klokkeslett-verdi for den angitte kulturen.</span><span class="sxs-lookup"><span data-stu-id="07069-126">However, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date/time value for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="07069-127">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="07069-127">Additional resources</span></span>

[<span data-ttu-id="07069-128">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="07069-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]