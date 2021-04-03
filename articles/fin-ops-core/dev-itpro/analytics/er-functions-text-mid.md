---
title: MID ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen MID
author: NickSelin
manager: kfend
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
ms.openlocfilehash: e0520bc54465f00d36e88787933b291847dee852
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562739"
---
# <a name="mid-er-function"></a><span data-ttu-id="d19d3-103">MID ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="d19d3-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d19d3-104">`MID`-funksjonen returnerer en *streng*-verdi som viser det angitte antallet tegn fra den angitte strengen, og begynner fra den angitte posisjonen.</span><span class="sxs-lookup"><span data-stu-id="d19d3-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="d19d3-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="d19d3-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="d19d3-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="d19d3-106">Arguments</span></span>

<span data-ttu-id="d19d3-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="d19d3-107">`text`: *String*</span></span>

<span data-ttu-id="d19d3-108">En *streng*-verdi som angir teksten det skal returneres tegn fra.</span><span class="sxs-lookup"><span data-stu-id="d19d3-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="d19d3-109">`starting position`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="d19d3-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="d19d3-110">En *Heltall*-verdi som angir plasseringen til det første tegnet som må returneres fra den angitte teksten.</span><span class="sxs-lookup"><span data-stu-id="d19d3-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="d19d3-111">`number of characters`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="d19d3-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="d19d3-112">En *Heltall*-verdi som angir antall tegn som må returneres, som begynner fra den angitte startposisjonen.</span><span class="sxs-lookup"><span data-stu-id="d19d3-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="d19d3-113">Returverdier</span><span class="sxs-lookup"><span data-stu-id="d19d3-113">Return values</span></span>

<span data-ttu-id="d19d3-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="d19d3-114">*String*</span></span>

<span data-ttu-id="d19d3-115">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="d19d3-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d19d3-116">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="d19d3-116">Usage notes</span></span>

<span data-ttu-id="d19d3-117">Hvis verdien for `starting position`-argumentet er mindre enn 0 (null), telles tegnene som returneres, fra den første plasseringen i den angitte strengen.</span><span class="sxs-lookup"><span data-stu-id="d19d3-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="d19d3-118">Hvis verdien for `starting position`-argumentet overskrider lengden på den angitte strengen, returneres en tom streng.</span><span class="sxs-lookup"><span data-stu-id="d19d3-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="d19d3-119">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d19d3-119">Example</span></span>

<span data-ttu-id="d19d3-120">`MID ("Sample", 2, 3)` returnerer **"amp"**.</span><span class="sxs-lookup"><span data-stu-id="d19d3-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d19d3-121">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d19d3-121">Additional resources</span></span>

[<span data-ttu-id="d19d3-122">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="d19d3-122">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]