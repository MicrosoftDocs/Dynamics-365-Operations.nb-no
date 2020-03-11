---
title: PADLEFT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen PADLEFT.
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
ms.openlocfilehash: d11e2d8b46614085156228ab1001d1f9340a05b0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040969"
---
# <span data-ttu-id="ff965-103"><a name="PADLEFT">PADLEFT ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="ff965-103"><a name="PADLEFT">PADLEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff965-104">`PADLEFT`-funksjonen returnerer en*Streng*-verdi med den angitte lengden der begynnelsen av den angitte strengen fylles ut med de angitte tegnene.</span><span class="sxs-lookup"><span data-stu-id="ff965-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff965-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="ff965-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="ff965-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="ff965-106">Arguments</span></span>

<span data-ttu-id="ff965-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ff965-107">`text`: *String*</span></span>

<span data-ttu-id="ff965-108">En *streng*-verdi som representerer den opprinnelige teksten.</span><span class="sxs-lookup"><span data-stu-id="ff965-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="ff965-109">`length`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="ff965-109">`length`: *Integer*</span></span>

<span data-ttu-id="ff965-110">En *Heltall*-verdi som representerer det endelige antallet tegn i den utfylte strengen.</span><span class="sxs-lookup"><span data-stu-id="ff965-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="ff965-111">`padding chars`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ff965-111">`padding chars`: *String*</span></span>

<span data-ttu-id="ff965-112">Tegnene som skal brukes til utfylling.</span><span class="sxs-lookup"><span data-stu-id="ff965-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="ff965-113">Returverdier</span><span class="sxs-lookup"><span data-stu-id="ff965-113">Return values</span></span>

<span data-ttu-id="ff965-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ff965-114">*String*</span></span>

<span data-ttu-id="ff965-115">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="ff965-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="ff965-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ff965-116">Example</span></span>

<span data-ttu-id="ff965-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returnerer tekststrengen **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span><span class="sxs-lookup"><span data-stu-id="ff965-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff965-118">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ff965-118">Additional resources</span></span>

[<span data-ttu-id="ff965-119">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="ff965-119">Text functions</span></span>](er-functions-category-text.md)
