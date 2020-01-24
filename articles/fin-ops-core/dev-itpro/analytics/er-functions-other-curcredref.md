---
title: CURCREDREF ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen CURCREDREF.
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
ms.openlocfilehash: 5633541b1c7e25a0cfb837c4679691506806421b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917011"
---
# <span data-ttu-id="d38d6-103"><a name="CURCREDREF">CURCREDREF ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="d38d6-103"><a name="CURCREDREF">CURCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d38d6-104">`CURCREDREF`-funksjonen returnerer en *streng*-verdi som representerer en kreditorreferanse, basert på sifrene i det angitte fakturanummeret.</span><span class="sxs-lookup"><span data-stu-id="d38d6-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="d38d6-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="d38d6-105">Syntax</span></span>

```
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="d38d6-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="d38d6-106">Arguments</span></span>

<span data-ttu-id="d38d6-107">`invoice number digits`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="d38d6-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="d38d6-108">En tekstverdi som representerer sifrene i et fakturanummer.</span><span class="sxs-lookup"><span data-stu-id="d38d6-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="d38d6-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="d38d6-109">Return values</span></span>

<span data-ttu-id="d38d6-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="d38d6-110">*String*</span></span>

<span data-ttu-id="d38d6-111">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="d38d6-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d38d6-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d38d6-112">Example</span></span>

<span data-ttu-id="d38d6-113">`CURCredRef ("VEND-200002")` returnerer **"2200002"**.</span><span class="sxs-lookup"><span data-stu-id="d38d6-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d38d6-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d38d6-114">Additional resources</span></span>

[<span data-ttu-id="d38d6-115">Andre funksjoner (spesifikke for forretningsområder)</span><span class="sxs-lookup"><span data-stu-id="d38d6-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
