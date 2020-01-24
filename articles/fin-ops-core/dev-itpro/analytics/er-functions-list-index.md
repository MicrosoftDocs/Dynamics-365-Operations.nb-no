---
title: INDEX ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen INDEX.
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
ms.openlocfilehash: a7fe2cbb5421da3c6dd1d044316b276836c5e5c1
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917310"
---
# <span data-ttu-id="b6bcf-103"><a name="INDEX">INDEX ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="b6bcf-103"><a name="INDEX">INDEX ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6bcf-104">`INDEX`-funksjonen returnerer en *Container (post)*-verdi som er valgt ved hjelp av den angitte numeriske indeksen i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="b6bcf-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="b6bcf-105">Det oppstår et unntak hvis indeksen er utenfor området til postene i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="b6bcf-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6bcf-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="b6bcf-106">Syntax</span></span>

```
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="b6bcf-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="b6bcf-107">Arguments</span></span>

<span data-ttu-id="b6bcf-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="b6bcf-108">`list`: *Record list*</span></span>

<span data-ttu-id="b6bcf-109">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="b6bcf-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="b6bcf-110">`index`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="b6bcf-110">`index`: *Integer*</span></span>

<span data-ttu-id="b6bcf-111">En numerisk indeks som angir plasseringen til den ønskede posten i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="b6bcf-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="b6bcf-112">Returverdier</span><span class="sxs-lookup"><span data-stu-id="b6bcf-112">Return values</span></span>

<span data-ttu-id="b6bcf-113">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="b6bcf-113">*Container (record)*</span></span>

<span data-ttu-id="b6bcf-114">Den resulterende postvedien.</span><span class="sxs-lookup"><span data-stu-id="b6bcf-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="b6bcf-115">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="b6bcf-115">Example 1</span></span>

<span data-ttu-id="b6bcf-116">Hvis du angir datakilden **DS** for typen *Beregnet felt*, og den inneholder uttrykket `SPLIT ("A|B|C", "|")`, returnerer uttrykket `DS.Value` tekstverdien **B** for den andre posten i denne postlisten.</span><span class="sxs-lookup"><span data-stu-id="b6bcf-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="b6bcf-117">Uttrykket `INDEX (SPLIT ("A|B|C", "|"), 2).Value` returnerer også tekstverdien **"B"**.</span><span class="sxs-lookup"><span data-stu-id="b6bcf-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b6bcf-118">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="b6bcf-118">Example 2</span></span>

<span data-ttu-id="b6bcf-119">Hvis du angir datakilde **DS** av *Beregnet felt*-typen, og den inneholder uttrykket `SPLIT ("A|B|C", "|")`, genererer uttrykket `INDEX (SPLIT ("A|B|C", "|"), 4).Value` et unntak under kjøring.</span><span class="sxs-lookup"><span data-stu-id="b6bcf-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6bcf-120">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b6bcf-120">Additional resources</span></span>

[<span data-ttu-id="b6bcf-121">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="b6bcf-121">List functions</span></span>](er-functions-category-list.md)
