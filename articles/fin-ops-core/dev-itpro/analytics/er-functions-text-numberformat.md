---
title: NUMBERFORMAT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NUMBERFORMAT.
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
ms.openlocfilehash: 8a431414044846bf4e79e6b9f0e5b27281ea8f46
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744413"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="89b89-103">NUMBERFORMAT ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="89b89-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89b89-104">`NUMBERFORMAT`-funksjonen returnerer en *Streng*-verdi som viser det angitte tallet i angitt format og i en valgfri angitt [kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="89b89-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="89b89-105">Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) og [egendefinert](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="89b89-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="89b89-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="89b89-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="89b89-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="89b89-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="89b89-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="89b89-108">Arguments</span></span>

<span data-ttu-id="89b89-109">`number`: *Heltall* eller *Reell*</span><span class="sxs-lookup"><span data-stu-id="89b89-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="89b89-110">En numerisk verdi som angir nummeret som må formateres.</span><span class="sxs-lookup"><span data-stu-id="89b89-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="89b89-111">`format` : *Streng*</span><span class="sxs-lookup"><span data-stu-id="89b89-111">`format` : *String*</span></span>

<span data-ttu-id="89b89-112">En *streng*-verdi som representerer formatet.</span><span class="sxs-lookup"><span data-stu-id="89b89-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="89b89-113">`culture`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="89b89-113">`culture`: *String*</span></span>

<span data-ttu-id="89b89-114">En *streng*-verdi som representerer kulturen som skal brukes til formatering.</span><span class="sxs-lookup"><span data-stu-id="89b89-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="89b89-115">Returverdier</span><span class="sxs-lookup"><span data-stu-id="89b89-115">Return values</span></span>

<span data-ttu-id="89b89-116">*Streng*</span><span class="sxs-lookup"><span data-stu-id="89b89-116">*String*</span></span>

<span data-ttu-id="89b89-117">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="89b89-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="89b89-118">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="89b89-118">Usage notes</span></span>

<span data-ttu-id="89b89-119">Hvis kulturen ikke er definert som et argument for den kalte funksjonen, vil konteksten som denne funksjonen kjøres i, bestemme kulturen som brukes til å formatere tall.</span><span class="sxs-lookup"><span data-stu-id="89b89-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="89b89-120">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="89b89-120">Example 1</span></span>

<span data-ttu-id="89b89-121">For **EN-US**-kulturen returnerer `NUMBERFORMAT (0.45, "p")` **"45.00 %"**, og `NUMBERFORMAT (10.45, "#")` returnerer **"10"**.</span><span class="sxs-lookup"><span data-stu-id="89b89-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="89b89-122">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="89b89-122">Example 2</span></span>

<span data-ttu-id="89b89-123">`NUMBERFORMAT (10/3, "F2", "de")` returnerer **3,33**, mens `NUMBERFORMAT (10/3, "F2", "en-us")` returnerer **3.33**.</span><span class="sxs-lookup"><span data-stu-id="89b89-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="89b89-124">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="89b89-124">Additional resources</span></span>

[<span data-ttu-id="89b89-125">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="89b89-125">Text functions</span></span>](er-functions-category-text.md)
