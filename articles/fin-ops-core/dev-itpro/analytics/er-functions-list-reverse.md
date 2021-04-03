---
title: REVERSE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen REVERSE.
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
ms.openlocfilehash: f76582bc8b752fe0322bee8917d8649ed1c024ba
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567372"
---
# <a name="reverse-er-function"></a><span data-ttu-id="f4c7d-103">REVERSE ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="f4c7d-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4c7d-104">`REVERSE`-funksjonen returnerer den angitte listen som en *postliste*-verdi i reversert sorteringsrekkefølge.</span><span class="sxs-lookup"><span data-stu-id="f4c7d-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4c7d-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="f4c7d-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="f4c7d-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="f4c7d-106">Arguments</span></span>

<span data-ttu-id="f4c7d-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="f4c7d-107">`list`: *Record list*</span></span>

<span data-ttu-id="f4c7d-108">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="f4c7d-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f4c7d-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="f4c7d-109">Return values</span></span>

<span data-ttu-id="f4c7d-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="f4c7d-110">*Record list*</span></span>

<span data-ttu-id="f4c7d-111">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="f4c7d-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="f4c7d-112">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="f4c7d-112">Example 1</span></span>

<span data-ttu-id="f4c7d-113">Hvis du angir datakilde **DS** av *Beregnet felt*-typen, og den inneholder uttrykket `SPLIT ("C|B|A", "|")`, genererer uttrykket `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` tekstverdien **"C"**.</span><span class="sxs-lookup"><span data-stu-id="f4c7d-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f4c7d-114">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="f4c7d-114">Example 2</span></span>

<span data-ttu-id="f4c7d-115">Hvis **Leverandør** er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, returnerer uttrykket `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` en liste over leverandører sortert etter navn i synkende rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="f4c7d-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4c7d-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f4c7d-116">Additional resources</span></span>

[<span data-ttu-id="f4c7d-117">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="f4c7d-117">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]