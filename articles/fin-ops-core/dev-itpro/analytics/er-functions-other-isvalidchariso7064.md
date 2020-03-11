---
title: ISVALIDCHARACTERISO7064 ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ISVALIDCHARACTERISO7064
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c858ad72db7afe63baca8288f312548c4fc37d5c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041406"
---
# <span data-ttu-id="eb997-103"><a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="eb997-103"><a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb997-104">`ISVALIDCHARACTERISO7064`-funksjonen returnerer den *boolske* verdien **SANN** hvis den angitte strengen representerer et gyldig internasjonalt bankkontonummer (IBAN).</span><span class="sxs-lookup"><span data-stu-id="eb997-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="eb997-105">Hvis ikke returneres den *boolske* verdien **USANN**.</span><span class="sxs-lookup"><span data-stu-id="eb997-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb997-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="eb997-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="eb997-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="eb997-107">Arguments</span></span>

<span data-ttu-id="eb997-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="eb997-108">`text`: *String*</span></span>

<span data-ttu-id="eb997-109">En tekstverdi som representerer et IBAN-nummer.</span><span class="sxs-lookup"><span data-stu-id="eb997-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="eb997-110">Returverdier</span><span class="sxs-lookup"><span data-stu-id="eb997-110">Return values</span></span>

<span data-ttu-id="eb997-111">*Streng*</span><span class="sxs-lookup"><span data-stu-id="eb997-111">*String*</span></span>

<span data-ttu-id="eb997-112">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="eb997-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="eb997-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="eb997-113">Example</span></span>

<span data-ttu-id="eb997-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returnerer **SANN**.</span><span class="sxs-lookup"><span data-stu-id="eb997-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="eb997-115">`ISVALIDCHARACTERISO7064 ("AT61")` returnerer **USANN**.</span><span class="sxs-lookup"><span data-stu-id="eb997-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb997-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="eb997-116">Additional resources</span></span>

[<span data-ttu-id="eb997-117">Andre funksjoner (spesifikke for forretningsområder)</span><span class="sxs-lookup"><span data-stu-id="eb997-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
