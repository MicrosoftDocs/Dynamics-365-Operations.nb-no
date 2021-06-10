---
title: INDEX ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen INDEX.
author: NickSelin
ms.date: 05/20/2021
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
ms.openlocfilehash: 5a0fdb8958670efe8e2a37cee183bf836fa6c7e8
ms.sourcegitcommit: 047b0503868cc7d7b21868e24405d76af35db747
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087757"
---
# <a name="index-er-function"></a><span data-ttu-id="2551c-103">INDEX ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="2551c-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2551c-104">`INDEX`-funksjonen returnerer en *Container (post)*-verdi som er valgt ved hjelp av den angitte numeriske indeksen i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="2551c-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="2551c-105">Det oppstår et unntak hvis indeksen er utenfor området til postene i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="2551c-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="2551c-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="2551c-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="2551c-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="2551c-107">Arguments</span></span>

<span data-ttu-id="2551c-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="2551c-108">`list`: *Record list*</span></span>

<span data-ttu-id="2551c-109">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="2551c-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="2551c-110">`index`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="2551c-110">`index`: *Integer*</span></span>

<span data-ttu-id="2551c-111">En numerisk indeks som angir plasseringen til den ønskede posten i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="2551c-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

> [!NOTE]
> <span data-ttu-id="2551c-112">Fordi enbasert nummerering brukes for denne funksjonen, kan du angi verdien **1** for å returnere den første posten i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="2551c-112">Because one-based numbering is used for this function, specify the value **1** to return the first record of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="2551c-113">Returverdier</span><span class="sxs-lookup"><span data-stu-id="2551c-113">Return values</span></span>

<span data-ttu-id="2551c-114">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="2551c-114">*Container (record)*</span></span>

<span data-ttu-id="2551c-115">Den resulterende postvedien.</span><span class="sxs-lookup"><span data-stu-id="2551c-115">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="2551c-116">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="2551c-116">Example 1</span></span>

<span data-ttu-id="2551c-117">Hvis du angir datakilden **DS** for typen *Beregnet felt*, og den inneholder uttrykket `SPLIT ("A|B|C", "|")`, returnerer uttrykket `DS.Value` tekstverdien **B** for den andre posten i denne postlisten.</span><span class="sxs-lookup"><span data-stu-id="2551c-117">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="2551c-118">Uttrykket `INDEX (SPLIT ("A|B|C", "|"), 2).Value` returnerer også tekstverdien **"B"**.</span><span class="sxs-lookup"><span data-stu-id="2551c-118">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="2551c-119">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="2551c-119">Example 2</span></span>

<span data-ttu-id="2551c-120">Hvis du angir datakilde **DS** av *Beregnet felt*-typen, og den inneholder uttrykket `SPLIT ("A|B|C", "|")`, genererer uttrykket `INDEX (SPLIT ("A|B|C", "|"), 4).Value` et unntak under kjøring.</span><span class="sxs-lookup"><span data-stu-id="2551c-120">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2551c-121">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="2551c-121">Additional resources</span></span>

[<span data-ttu-id="2551c-122">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="2551c-122">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
