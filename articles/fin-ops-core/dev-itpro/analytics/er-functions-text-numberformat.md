---
title: NUMBERFORMAT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NUMBERFORMAT.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 4a383b3f7c0ca7c4e5afc609cc8a7b1b07021b02
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890389"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="4ec8a-103">NUMBERFORMAT ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="4ec8a-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ec8a-104">`NUMBERFORMAT`-funksjonen returnerer en *Streng*-verdi som viser det angitte tallet i angitt format og i en valgfri angitt [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="4ec8a-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="4ec8a-105">Hvis du vil ha informasjon om hvilke formater som støttes, kan du se [standard](/dotnet/standard/base-types/standard-numeric-format-strings) og [egendefinert](/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="4ec8a-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-numeric-format-strings) and [custom](/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="4ec8a-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="4ec8a-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="4ec8a-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="4ec8a-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="4ec8a-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="4ec8a-108">Arguments</span></span>

<span data-ttu-id="4ec8a-109">`number`: *Heltall* eller *Reell*</span><span class="sxs-lookup"><span data-stu-id="4ec8a-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="4ec8a-110">En numerisk verdi som angir nummeret som må formateres.</span><span class="sxs-lookup"><span data-stu-id="4ec8a-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="4ec8a-111">`format` : *Streng*</span><span class="sxs-lookup"><span data-stu-id="4ec8a-111">`format` : *String*</span></span>

<span data-ttu-id="4ec8a-112">En *streng*-verdi som representerer formatet.</span><span class="sxs-lookup"><span data-stu-id="4ec8a-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="4ec8a-113">`culture`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="4ec8a-113">`culture`: *String*</span></span>

<span data-ttu-id="4ec8a-114">En *streng*-verdi som representerer kulturen som skal brukes til formatering.</span><span class="sxs-lookup"><span data-stu-id="4ec8a-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="4ec8a-115">Returverdier</span><span class="sxs-lookup"><span data-stu-id="4ec8a-115">Return values</span></span>

<span data-ttu-id="4ec8a-116">*Streng*</span><span class="sxs-lookup"><span data-stu-id="4ec8a-116">*String*</span></span>

<span data-ttu-id="4ec8a-117">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="4ec8a-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4ec8a-118">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="4ec8a-118">Usage notes</span></span>

<span data-ttu-id="4ec8a-119">Hvis kulturen ikke er definert som et argument for den kalte funksjonen, vil konteksten som denne funksjonen kjøres i, bestemme kulturen som brukes til å formatere tall.</span><span class="sxs-lookup"><span data-stu-id="4ec8a-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="4ec8a-120">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="4ec8a-120">Example 1</span></span>

<span data-ttu-id="4ec8a-121">For **EN-US**-kulturen returnerer `NUMBERFORMAT (0.45, "p")` **"45.00 %"**, og `NUMBERFORMAT (10.45, "#")` returnerer **"10"**.</span><span class="sxs-lookup"><span data-stu-id="4ec8a-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="4ec8a-122">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="4ec8a-122">Example 2</span></span>

<span data-ttu-id="4ec8a-123">`NUMBERFORMAT (10/3, "F2", "de")` returnerer **3,33**, mens `NUMBERFORMAT (10/3, "F2", "en-us")` returnerer **3.33**.</span><span class="sxs-lookup"><span data-stu-id="4ec8a-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ec8a-124">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4ec8a-124">Additional resources</span></span>

[<span data-ttu-id="4ec8a-125">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="4ec8a-125">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]