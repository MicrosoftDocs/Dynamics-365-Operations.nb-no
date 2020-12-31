---
title: STRINGJOIN ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen STRINGJOIN.
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
ms.openlocfilehash: 586dbcb98d237325188f4b0384580613ab7a9347
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683747"
---
# <a name="stringjoin-er-function"></a><span data-ttu-id="09a4d-103">STRINGJOIN ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="09a4d-103">STRINGJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09a4d-104">`STRINGJOIN`-funksjonen returnerer en *Streng*-verdi som består av sammenkoblede verdier for det angitte feltet fra den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="09a4d-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="09a4d-105">Verdiene kan skilles med det angitte skilletegnet.</span><span class="sxs-lookup"><span data-stu-id="09a4d-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="09a4d-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="09a4d-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="09a4d-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="09a4d-107">Arguments</span></span>

<span data-ttu-id="09a4d-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="09a4d-108">`list`: *Record list*</span></span>

<span data-ttu-id="09a4d-109">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="09a4d-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="09a4d-110">`field`: *Felt*</span><span class="sxs-lookup"><span data-stu-id="09a4d-110">`field`: *Field*</span></span>

<span data-ttu-id="09a4d-111">Den gyldige banen til et felt av *Streng*-datatypen i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="09a4d-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="09a4d-112">`delimiter`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="09a4d-112">`delimiter`: *String*</span></span>

<span data-ttu-id="09a4d-113">Et skilletegn som brukes til å skille delstrenger.</span><span class="sxs-lookup"><span data-stu-id="09a4d-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="09a4d-114">Returverdier</span><span class="sxs-lookup"><span data-stu-id="09a4d-114">Return values</span></span>

<span data-ttu-id="09a4d-115">*Streng*</span><span class="sxs-lookup"><span data-stu-id="09a4d-115">*String*</span></span>

<span data-ttu-id="09a4d-116">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="09a4d-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="09a4d-117">Eksempel</span><span class="sxs-lookup"><span data-stu-id="09a4d-117">Example</span></span>

<span data-ttu-id="09a4d-118">Hvis du angir `SPLIT("abc" , 1)` som datakilde **DS**, returnerer uttrykket `STRINGJOIN (DS, DS.Value, "-")` **"a-b-c"**.</span><span class="sxs-lookup"><span data-stu-id="09a4d-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="09a4d-119">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="09a4d-119">Additional resources</span></span>

[<span data-ttu-id="09a4d-120">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="09a4d-120">List functions</span></span>](er-functions-category-list.md)
