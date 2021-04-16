---
title: DAYOFYEAR ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DAYOFYEAR.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 569e988db91ff992fb7db6e7fd6e8c6aa6a1a3e8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746921"
---
# <a name="dayofyear-er-function"></a><span data-ttu-id="cfb0c-103">DAYOFYEAR ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="cfb0c-103">DAYOFYEAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cfb0c-104">`DAYOFYEAR`-funksjonen returnerer en *Heltall*-verdi som representerer antall dager mellom 1. januar og den angitte datoen.</span><span class="sxs-lookup"><span data-stu-id="cfb0c-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfb0c-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="cfb0c-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="cfb0c-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="cfb0c-106">Arguments</span></span>

<span data-ttu-id="cfb0c-107">`date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="cfb0c-107">`date`: *Date*</span></span>

<span data-ttu-id="cfb0c-108">En datoverdi som representerer datoen som skal brukes for beregningen av antall dager.</span><span class="sxs-lookup"><span data-stu-id="cfb0c-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="cfb0c-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="cfb0c-109">Return values</span></span>

<span data-ttu-id="cfb0c-110">*Heltall*</span><span class="sxs-lookup"><span data-stu-id="cfb0c-110">*Integer*</span></span>

<span data-ttu-id="cfb0c-111">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="cfb0c-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="cfb0c-112">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="cfb0c-112">Example 1</span></span>

<span data-ttu-id="cfb0c-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returnerer **61**.</span><span class="sxs-lookup"><span data-stu-id="cfb0c-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="cfb0c-114">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="cfb0c-114">Example 2</span></span>

<span data-ttu-id="cfb0c-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returnerer **1**.</span><span class="sxs-lookup"><span data-stu-id="cfb0c-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cfb0c-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="cfb0c-116">Additional resources</span></span>

[<span data-ttu-id="cfb0c-117">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="cfb0c-117">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]