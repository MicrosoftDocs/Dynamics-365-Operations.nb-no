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
ms.openlocfilehash: 13346c4810d6c93d4ef47ce525831332562c7f51
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743405"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="ab686-103">NUMBERVALUE ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="ab686-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab686-104">`NUMBERVALUE`-funksjonen returnerer en *reell* verdi som er konvertert fra den angitte *streng*-verdien.</span><span class="sxs-lookup"><span data-stu-id="ab686-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="ab686-105">Under konverteringen vurderes de angitte skilletegnene for desimal- og siffergruppering.</span><span class="sxs-lookup"><span data-stu-id="ab686-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab686-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="ab686-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="ab686-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="ab686-107">Arguments</span></span>

<span data-ttu-id="ab686-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ab686-108">`text`: *String*</span></span>

<span data-ttu-id="ab686-109">En tekstverdi som må konverteres til et *reelt* tall.</span><span class="sxs-lookup"><span data-stu-id="ab686-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="ab686-110">`decimal separator`: Streng</span><span class="sxs-lookup"><span data-stu-id="ab686-110">`decimal separator`: String</span></span>

<span data-ttu-id="ab686-111">Et desimalskilletegn.</span><span class="sxs-lookup"><span data-stu-id="ab686-111">A decimal separator.</span></span> <span data-ttu-id="ab686-112">Det brukes til å skille heltalls- og brøkdeler av et desimaltall.</span><span class="sxs-lookup"><span data-stu-id="ab686-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="ab686-113">`digit grouping separator`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ab686-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="ab686-114">Et skilletegn for siffergruppering.</span><span class="sxs-lookup"><span data-stu-id="ab686-114">A digit grouping separator.</span></span> <span data-ttu-id="ab686-115">Det brukes som tusenskilletegn.</span><span class="sxs-lookup"><span data-stu-id="ab686-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="ab686-116">Returverdier</span><span class="sxs-lookup"><span data-stu-id="ab686-116">Return values</span></span>

<span data-ttu-id="ab686-117">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="ab686-117">*Real*</span></span>

<span data-ttu-id="ab686-118">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="ab686-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="ab686-119">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ab686-119">Example</span></span>

<span data-ttu-id="ab686-120">`NUMBERVALUE( "1 234,56", ",", " ")` returnerer **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="ab686-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ab686-121">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ab686-121">Additional resources</span></span>

[<span data-ttu-id="ab686-122">Typekonverteringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="ab686-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
