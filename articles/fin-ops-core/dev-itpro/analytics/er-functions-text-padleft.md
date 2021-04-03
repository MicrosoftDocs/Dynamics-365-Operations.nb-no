---
title: PADLEFT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen PADLEFT.
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
ms.openlocfilehash: 86957808ca30db87e6f8202c2024d9929969fc3d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562691"
---
# <a name="padleft-er-function"></a><span data-ttu-id="b5d88-103">PADLEFT ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="b5d88-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5d88-104">`PADLEFT`-funksjonen returnerer en *Streng*-verdi med den angitte lengden der begynnelsen av den angitte strengen fylles ut med de angitte tegnene.</span><span class="sxs-lookup"><span data-stu-id="b5d88-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d88-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="b5d88-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="b5d88-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="b5d88-106">Arguments</span></span>

<span data-ttu-id="b5d88-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="b5d88-107">`text`: *String*</span></span>

<span data-ttu-id="b5d88-108">En *streng*-verdi som representerer den opprinnelige teksten.</span><span class="sxs-lookup"><span data-stu-id="b5d88-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="b5d88-109">`length`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="b5d88-109">`length`: *Integer*</span></span>

<span data-ttu-id="b5d88-110">En *Heltall*-verdi som representerer det endelige antallet tegn i den utfylte strengen.</span><span class="sxs-lookup"><span data-stu-id="b5d88-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="b5d88-111">`padding chars`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="b5d88-111">`padding chars`: *String*</span></span>

<span data-ttu-id="b5d88-112">Tegnene som skal brukes til utfylling.</span><span class="sxs-lookup"><span data-stu-id="b5d88-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="b5d88-113">Returverdier</span><span class="sxs-lookup"><span data-stu-id="b5d88-113">Return values</span></span>

<span data-ttu-id="b5d88-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="b5d88-114">*String*</span></span>

<span data-ttu-id="b5d88-115">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="b5d88-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b5d88-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="b5d88-116">Example</span></span>

<span data-ttu-id="b5d88-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returnerer tekststrengen **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span><span class="sxs-lookup"><span data-stu-id="b5d88-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5d88-118">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b5d88-118">Additional resources</span></span>

[<span data-ttu-id="b5d88-119">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="b5d88-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]