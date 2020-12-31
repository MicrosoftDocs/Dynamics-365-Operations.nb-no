---
title: MID ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen MID
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d8a7d2e9beb0fc8724d26de0acaf1d61e3834c6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680296"
---
# <a name="mid-er-function"></a><span data-ttu-id="344a2-103">MID ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="344a2-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="344a2-104">`MID`-funksjonen returnerer en *streng*-verdi som viser det angitte antallet tegn fra den angitte strengen, og begynner fra den angitte posisjonen.</span><span class="sxs-lookup"><span data-stu-id="344a2-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="344a2-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="344a2-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="344a2-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="344a2-106">Arguments</span></span>

<span data-ttu-id="344a2-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="344a2-107">`text`: *String*</span></span>

<span data-ttu-id="344a2-108">En *streng*-verdi som angir teksten det skal returneres tegn fra.</span><span class="sxs-lookup"><span data-stu-id="344a2-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="344a2-109">`starting position`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="344a2-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="344a2-110">En *Heltall*-verdi som angir plasseringen til det første tegnet som må returneres fra den angitte teksten.</span><span class="sxs-lookup"><span data-stu-id="344a2-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="344a2-111">`number of characters`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="344a2-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="344a2-112">En *Heltall*-verdi som angir antall tegn som må returneres, som begynner fra den angitte startposisjonen.</span><span class="sxs-lookup"><span data-stu-id="344a2-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="344a2-113">Returverdier</span><span class="sxs-lookup"><span data-stu-id="344a2-113">Return values</span></span>

<span data-ttu-id="344a2-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="344a2-114">*String*</span></span>

<span data-ttu-id="344a2-115">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="344a2-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="344a2-116">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="344a2-116">Usage notes</span></span>

<span data-ttu-id="344a2-117">Hvis verdien for `starting position`-argumentet er mindre enn 0 (null), telles tegnene som returneres, fra den første plasseringen i den angitte strengen.</span><span class="sxs-lookup"><span data-stu-id="344a2-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="344a2-118">Hvis verdien for `starting position`-argumentet overskrider lengden på den angitte strengen, returneres en tom streng.</span><span class="sxs-lookup"><span data-stu-id="344a2-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="344a2-119">Eksempel</span><span class="sxs-lookup"><span data-stu-id="344a2-119">Example</span></span>

<span data-ttu-id="344a2-120">`MID ("Sample", 2, 3)` returnerer **"amp"**.</span><span class="sxs-lookup"><span data-stu-id="344a2-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="344a2-121">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="344a2-121">Additional resources</span></span>

[<span data-ttu-id="344a2-122">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="344a2-122">Text functions</span></span>](er-functions-category-text.md)
