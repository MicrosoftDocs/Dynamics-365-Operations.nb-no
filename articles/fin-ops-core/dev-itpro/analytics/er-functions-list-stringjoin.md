---
title: STRINGJOIN ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen STRINGJOIN.
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
ms.openlocfilehash: 755e6481abb65dfecc8ddb6bceb032c8110095e2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568176"
---
# <a name="stringjoin-er-function"></a><span data-ttu-id="5ebd3-103">STRINGJOIN ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="5ebd3-103">STRINGJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ebd3-104">`STRINGJOIN`-funksjonen returnerer en *Streng*-verdi som består av sammenkoblede verdier for det angitte feltet fra den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="5ebd3-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="5ebd3-105">Verdiene kan skilles med det angitte skilletegnet.</span><span class="sxs-lookup"><span data-stu-id="5ebd3-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ebd3-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="5ebd3-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="5ebd3-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="5ebd3-107">Arguments</span></span>

<span data-ttu-id="5ebd3-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="5ebd3-108">`list`: *Record list*</span></span>

<span data-ttu-id="5ebd3-109">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="5ebd3-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="5ebd3-110">`field`: *Felt*</span><span class="sxs-lookup"><span data-stu-id="5ebd3-110">`field`: *Field*</span></span>

<span data-ttu-id="5ebd3-111">Den gyldige banen til et felt av *Streng*-datatypen i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="5ebd3-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="5ebd3-112">`delimiter`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="5ebd3-112">`delimiter`: *String*</span></span>

<span data-ttu-id="5ebd3-113">Et skilletegn som brukes til å skille delstrenger.</span><span class="sxs-lookup"><span data-stu-id="5ebd3-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="5ebd3-114">Returverdier</span><span class="sxs-lookup"><span data-stu-id="5ebd3-114">Return values</span></span>

<span data-ttu-id="5ebd3-115">*Streng*</span><span class="sxs-lookup"><span data-stu-id="5ebd3-115">*String*</span></span>

<span data-ttu-id="5ebd3-116">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="5ebd3-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="5ebd3-117">Eksempel</span><span class="sxs-lookup"><span data-stu-id="5ebd3-117">Example</span></span>

<span data-ttu-id="5ebd3-118">Hvis du angir `SPLIT("abc" , 1)` som datakilde **DS**, returnerer uttrykket `STRINGJOIN (DS, DS.Value, "-")` **"a-b-c"**.</span><span class="sxs-lookup"><span data-stu-id="5ebd3-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5ebd3-119">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5ebd3-119">Additional resources</span></span>

[<span data-ttu-id="5ebd3-120">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="5ebd3-120">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]