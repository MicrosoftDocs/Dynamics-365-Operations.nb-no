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
ms.openlocfilehash: 21962952bb3bdd016831dc5e196af27c69ecc6db
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744077"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="d98a3-103">ISVALIDCHARACTERISO7064 ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="d98a3-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d98a3-104">`ISVALIDCHARACTERISO7064`-funksjonen returnerer den *boolske* verdien **SANN** hvis den angitte strengen representerer et gyldig internasjonalt bankkontonummer (IBAN).</span><span class="sxs-lookup"><span data-stu-id="d98a3-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="d98a3-105">Hvis ikke returneres den *boolske* verdien **USANN**.</span><span class="sxs-lookup"><span data-stu-id="d98a3-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d98a3-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="d98a3-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="d98a3-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="d98a3-107">Arguments</span></span>

<span data-ttu-id="d98a3-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="d98a3-108">`text`: *String*</span></span>

<span data-ttu-id="d98a3-109">En tekstverdi som representerer et IBAN-nummer.</span><span class="sxs-lookup"><span data-stu-id="d98a3-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="d98a3-110">Returverdier</span><span class="sxs-lookup"><span data-stu-id="d98a3-110">Return values</span></span>

<span data-ttu-id="d98a3-111">*Streng*</span><span class="sxs-lookup"><span data-stu-id="d98a3-111">*String*</span></span>

<span data-ttu-id="d98a3-112">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="d98a3-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d98a3-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d98a3-113">Example</span></span>

<span data-ttu-id="d98a3-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returnerer **SANN**.</span><span class="sxs-lookup"><span data-stu-id="d98a3-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="d98a3-115">`ISVALIDCHARACTERISO7064 ("AT61")` returnerer **USANN**.</span><span class="sxs-lookup"><span data-stu-id="d98a3-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d98a3-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d98a3-116">Additional resources</span></span>

[<span data-ttu-id="d98a3-117">Andre funksjoner (spesifikke for forretningsområder)</span><span class="sxs-lookup"><span data-stu-id="d98a3-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
