---
title: CONCATENATE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen CONCATENATE.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 6e4800ce44d9da07818acec55c50224a9a000fe6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569611"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="44bef-103">CONCATENATE ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="44bef-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44bef-104">`CONCATENATE`-funksjonen returnerer alle de angitte tekststrengene som en *streng*-verdi etter at de er føyd sammen til én streng.</span><span class="sxs-lookup"><span data-stu-id="44bef-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="44bef-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="44bef-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="44bef-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="44bef-106">Arguments</span></span>

<span data-ttu-id="44bef-107">`text 1`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="44bef-107">`text 1`: *String*</span></span>

<span data-ttu-id="44bef-108">En referanse til en datakilde for *Streng*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="44bef-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="44bef-109">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="44bef-109">This argument is required.</span></span>

<span data-ttu-id="44bef-110">`text N`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="44bef-110">`text N`: *String*</span></span>

<span data-ttu-id="44bef-111">En referanse til en datakilde for *Streng*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="44bef-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="44bef-112">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="44bef-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="44bef-113">Returverdier</span><span class="sxs-lookup"><span data-stu-id="44bef-113">Return values</span></span>

<span data-ttu-id="44bef-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="44bef-114">*String*</span></span>

<span data-ttu-id="44bef-115">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="44bef-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="44bef-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="44bef-116">Example</span></span>

<span data-ttu-id="44bef-117">`CONCATENATE ("abc", "def")` returnerer **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="44bef-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="44bef-118">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="44bef-118">Usage notes</span></span>

<span data-ttu-id="44bef-119">Uttrykket `"abc" & "def"` returnerer også **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="44bef-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="44bef-120">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="44bef-120">Additional resources</span></span>

[<span data-ttu-id="44bef-121">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="44bef-121">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]