---
title: CONCATENATE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen CONCATENATE.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 903429994ae5618b597aa0ab0991e9f6783a96ed
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687944"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="b4341-103">CONCATENATE ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="b4341-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4341-104">`CONCATENATE`-funksjonen returnerer alle de angitte tekststrengene som en *streng*-verdi etter at de er føyd sammen til én streng.</span><span class="sxs-lookup"><span data-stu-id="b4341-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4341-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="b4341-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="b4341-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="b4341-106">Arguments</span></span>

<span data-ttu-id="b4341-107">`text 1`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="b4341-107">`text 1`: *String*</span></span>

<span data-ttu-id="b4341-108">En referanse til en datakilde for *Streng*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="b4341-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="b4341-109">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="b4341-109">This argument is required.</span></span>

<span data-ttu-id="b4341-110">`text N`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="b4341-110">`text N`: *String*</span></span>

<span data-ttu-id="b4341-111">En referanse til en datakilde for *Streng*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="b4341-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="b4341-112">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="b4341-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="b4341-113">Returverdier</span><span class="sxs-lookup"><span data-stu-id="b4341-113">Return values</span></span>

<span data-ttu-id="b4341-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="b4341-114">*String*</span></span>

<span data-ttu-id="b4341-115">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="b4341-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b4341-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="b4341-116">Example</span></span>

<span data-ttu-id="b4341-117">`CONCATENATE ("abc", "def")` returnerer **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="b4341-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b4341-118">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="b4341-118">Usage notes</span></span>

<span data-ttu-id="b4341-119">Uttrykket `"abc" & "def"` returnerer også **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="b4341-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4341-120">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b4341-120">Additional resources</span></span>

[<span data-ttu-id="b4341-121">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="b4341-121">Text functions</span></span>](er-functions-category-text.md)
