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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3d3ff87a59632d58a7c34ef96f856b38f005651
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915769"
---
# <span data-ttu-id="22b40-103"><a name="CONCATENATE">CONCATENATE ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="22b40-103"><a name="CONCATENATE">CONCATENATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22b40-104">`CONCATENATE`-funksjonen returnerer alle de angitte tekststrengene som en *streng*-verdi etter at de er føyd sammen til én streng.</span><span class="sxs-lookup"><span data-stu-id="22b40-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="22b40-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="22b40-105">Syntax</span></span>

```
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="22b40-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="22b40-106">Arguments</span></span>

<span data-ttu-id="22b40-107">`text 1`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="22b40-107">`text 1`: *String*</span></span>

<span data-ttu-id="22b40-108">En referanse til en datakilde for *Streng*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="22b40-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="22b40-109">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="22b40-109">This argument is required.</span></span>

<span data-ttu-id="22b40-110">`text N`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="22b40-110">`text N`: *String*</span></span>

<span data-ttu-id="22b40-111">En referanse til en datakilde for *Streng*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="22b40-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="22b40-112">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="22b40-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="22b40-113">Returverdier</span><span class="sxs-lookup"><span data-stu-id="22b40-113">Return values</span></span>

<span data-ttu-id="22b40-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="22b40-114">*String*</span></span>

<span data-ttu-id="22b40-115">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="22b40-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="22b40-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="22b40-116">Example</span></span>

<span data-ttu-id="22b40-117">`CONCATENATE ("abc", "def")` returnerer **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="22b40-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="22b40-118">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="22b40-118">Usage notes</span></span>

<span data-ttu-id="22b40-119">Uttrykket `"abc" & "def"` returnerer også **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="22b40-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="22b40-120">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="22b40-120">Additional resources</span></span>

[<span data-ttu-id="22b40-121">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="22b40-121">Text functions</span></span>](er-functions-category-text.md)
