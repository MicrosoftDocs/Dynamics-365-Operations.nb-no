---
title: INDEX ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen INDEX.
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
ms.openlocfilehash: 88be8f8bdc82bf3eab5c99e72046c794d8fac361
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566931"
---
# <a name="index-er-function"></a><span data-ttu-id="153ba-103">INDEX ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="153ba-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="153ba-104">`INDEX`-funksjonen returnerer en *Container (post)*-verdi som er valgt ved hjelp av den angitte numeriske indeksen i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="153ba-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="153ba-105">Det oppstår et unntak hvis indeksen er utenfor området til postene i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="153ba-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="153ba-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="153ba-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="153ba-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="153ba-107">Arguments</span></span>

<span data-ttu-id="153ba-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="153ba-108">`list`: *Record list*</span></span>

<span data-ttu-id="153ba-109">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="153ba-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="153ba-110">`index`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="153ba-110">`index`: *Integer*</span></span>

<span data-ttu-id="153ba-111">En numerisk indeks som angir plasseringen til den ønskede posten i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="153ba-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="153ba-112">Returverdier</span><span class="sxs-lookup"><span data-stu-id="153ba-112">Return values</span></span>

<span data-ttu-id="153ba-113">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="153ba-113">*Container (record)*</span></span>

<span data-ttu-id="153ba-114">Den resulterende postvedien.</span><span class="sxs-lookup"><span data-stu-id="153ba-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="153ba-115">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="153ba-115">Example 1</span></span>

<span data-ttu-id="153ba-116">Hvis du angir datakilden **DS** for typen *Beregnet felt*, og den inneholder uttrykket `SPLIT ("A|B|C", "|")`, returnerer uttrykket `DS.Value` tekstverdien **B** for den andre posten i denne postlisten.</span><span class="sxs-lookup"><span data-stu-id="153ba-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="153ba-117">Uttrykket `INDEX (SPLIT ("A|B|C", "|"), 2).Value` returnerer også tekstverdien **"B"**.</span><span class="sxs-lookup"><span data-stu-id="153ba-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="153ba-118">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="153ba-118">Example 2</span></span>

<span data-ttu-id="153ba-119">Hvis du angir datakilde **DS** av *Beregnet felt*-typen, og den inneholder uttrykket `SPLIT ("A|B|C", "|")`, genererer uttrykket `INDEX (SPLIT ("A|B|C", "|"), 4).Value` et unntak under kjøring.</span><span class="sxs-lookup"><span data-stu-id="153ba-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="153ba-120">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="153ba-120">Additional resources</span></span>

[<span data-ttu-id="153ba-121">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="153ba-121">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]