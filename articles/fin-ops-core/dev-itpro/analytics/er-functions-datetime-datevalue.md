---
title: DATEVALUE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DATEVALUE.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 43e65055b0803ed330a19568f9565c3fae488ab2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682419"
---
# <a name="datevalue-er-function"></a><span data-ttu-id="526f9-103">DATEVALUE ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="526f9-103">DATEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="526f9-104">`DATEVALUE`-funksjonen returnerer en *dato*-verdi som konverteres fra en gitt tekstverdi i angitt format og i en valgfri angitt [kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) til en datoverdi.</span><span class="sxs-lookup"><span data-stu-id="526f9-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="526f9-105">Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [egendefinert](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="526f9-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="526f9-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="526f9-106">Syntax 1</span></span>

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="526f9-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="526f9-107">Syntax 2</span></span>

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="526f9-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="526f9-108">Arguments</span></span>

<span data-ttu-id="526f9-109">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="526f9-109">`text`: *String*</span></span>

<span data-ttu-id="526f9-110">Tekst som representerer verdien som skal formateres.</span><span class="sxs-lookup"><span data-stu-id="526f9-110">Text that represents the value to format.</span></span>

<span data-ttu-id="526f9-111">`format`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="526f9-111">`format`: *String*</span></span>

<span data-ttu-id="526f9-112">Formatet til den gitte teksten.</span><span class="sxs-lookup"><span data-stu-id="526f9-112">The format of the given text.</span></span>

<span data-ttu-id="526f9-113">`culture`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="526f9-113">`culture`: *String*</span></span>

<span data-ttu-id="526f9-114">Kulturen som brukes til formatering av den gitte teksten.</span><span class="sxs-lookup"><span data-stu-id="526f9-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="526f9-115">Returverdier</span><span class="sxs-lookup"><span data-stu-id="526f9-115">Return values</span></span>

<span data-ttu-id="526f9-116">*Dato*</span><span class="sxs-lookup"><span data-stu-id="526f9-116">*Date*</span></span>

<span data-ttu-id="526f9-117">Den resulterende datoverdien.</span><span class="sxs-lookup"><span data-stu-id="526f9-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="526f9-118">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="526f9-118">Usage notes</span></span>

<span data-ttu-id="526f9-119">Når kulturen ikke er definert som et argument for den kalte funksjonen, defineres verdien for `culture` av kallkonteksten.</span><span class="sxs-lookup"><span data-stu-id="526f9-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="526f9-120">Hvis `DATEVALUE`-funksjonen for eksempel kalles ved hjelp av syntaks 1 i et ER-format for et **FIL**-element som er konfigurert til å bruke tysk kultur, vil konverteringen gjøres ved hjelp av tysk kultur.</span><span class="sxs-lookup"><span data-stu-id="526f9-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="526f9-121">Standardverdi for `culture` er **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="526f9-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="526f9-122">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="526f9-122">Example 1</span></span>

<span data-ttu-id="526f9-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returnerer datoverdien **21. desember 2016**, basert på det spesifiserte egendefinerte formatet og standardprogrammets **EN-US**-kultur.</span><span class="sxs-lookup"><span data-stu-id="526f9-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="526f9-124">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="526f9-124">Example 2</span></span>

<span data-ttu-id="526f9-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returnerer datoverdien **21. januar 2016**, basert på angitt egendefinert format og kultur.</span><span class="sxs-lookup"><span data-stu-id="526f9-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="526f9-126">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` vil imidlertid iverksette et unntak for å informere brukeren om at den angitte strengen ikke gjenkjennes som en gyldig dato for den angitte kulturen.</span><span class="sxs-lookup"><span data-stu-id="526f9-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="526f9-127">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="526f9-127">Additional resources</span></span>

[<span data-ttu-id="526f9-128">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="526f9-128">Date and time functions</span></span>](er-functions-category-datetime.md)
