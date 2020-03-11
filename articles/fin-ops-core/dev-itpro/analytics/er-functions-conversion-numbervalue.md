---
title: NUMBERVALUE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NUMBERVALUE.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 6eeb66f4206eb39141a5b2573fcb9d15428ae52a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042667"
---
# <span data-ttu-id="01655-103"><a name="NUMBERVALUE">NUMBERVALUE ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="01655-103"><a name="NUMBERVALUE">NUMBERVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01655-104">`NUMBERVALUE`-funksjonen returnerer en *reell* verdi som er konvertert fra den angitte *streng*-verdien.</span><span class="sxs-lookup"><span data-stu-id="01655-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="01655-105">Under konverteringen vurderes de angitte skilletegnene for desimal- og siffergruppering.</span><span class="sxs-lookup"><span data-stu-id="01655-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="01655-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="01655-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="01655-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="01655-107">Arguments</span></span>

<span data-ttu-id="01655-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="01655-108">`text`: *String*</span></span>

<span data-ttu-id="01655-109">En tekstverdi som må konverteres til et *reelt* tall.</span><span class="sxs-lookup"><span data-stu-id="01655-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="01655-110">`decimal separator`: Streng</span><span class="sxs-lookup"><span data-stu-id="01655-110">`decimal separator`: String</span></span>

<span data-ttu-id="01655-111">Et desimalskilletegn.</span><span class="sxs-lookup"><span data-stu-id="01655-111">A decimal separator.</span></span> <span data-ttu-id="01655-112">Det brukes til å skille heltalls- og brøkdeler av et desimaltall.</span><span class="sxs-lookup"><span data-stu-id="01655-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="01655-113">`digit grouping separator`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="01655-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="01655-114">Et skilletegn for siffergruppering.</span><span class="sxs-lookup"><span data-stu-id="01655-114">A digit grouping separator.</span></span> <span data-ttu-id="01655-115">Det brukes som tusenskilletegn.</span><span class="sxs-lookup"><span data-stu-id="01655-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="01655-116">Returverdier</span><span class="sxs-lookup"><span data-stu-id="01655-116">Return values</span></span>

<span data-ttu-id="01655-117">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="01655-117">*Real*</span></span>

<span data-ttu-id="01655-118">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="01655-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="01655-119">Eksempel</span><span class="sxs-lookup"><span data-stu-id="01655-119">Example</span></span>

<span data-ttu-id="01655-120">`NUMBERVALUE( "1 234,56", ",", " ")` returnerer **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="01655-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01655-121">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="01655-121">Additional resources</span></span>

[<span data-ttu-id="01655-122">Typekonverteringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="01655-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
