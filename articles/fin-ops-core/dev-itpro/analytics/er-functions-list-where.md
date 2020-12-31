---
title: WHERE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen WHERE.
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
ms.openlocfilehash: 1cc47c5001cf456b1fc600b326f826ea3b8b43ee
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687056"
---
# <a name="where-er-function"></a><span data-ttu-id="f4b4b-103">WHERE ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="f4b4b-103">WHERE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4b4b-104">`WHERE`-funksjonen returnerer den angitte listen som en *postliste*-verdi etter at den er filtrert i henhold til den angitte betingelsen.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-104">The `WHERE` function returns the specified list as a *Record list* value after it has been filtered according to the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4b4b-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="f4b4b-105">Syntax</span></span>

```vb
WHERE (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="f4b4b-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="f4b4b-106">Arguments</span></span>

<span data-ttu-id="f4b4b-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="f4b4b-107">`list`: *Record list*</span></span>

<span data-ttu-id="f4b4b-108">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="f4b4b-109">`condition`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="f4b4b-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="f4b4b-110">Et gyldig betingelsesuttrykk som brukes til å filtrere poster i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="f4b4b-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="f4b4b-111">Return values</span></span>

<span data-ttu-id="f4b4b-112">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="f4b4b-112">*Record list*</span></span>

<span data-ttu-id="f4b4b-113">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f4b4b-114">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="f4b4b-114">Usage notes</span></span>

<span data-ttu-id="f4b4b-115">Denne funksjonen er ulik [FILTER](er-functions-list-filter.md)-funksjonen fordi den angitte betingelsen brukes på en ER-datakilde av typen *Postposte* som finnes i minnet.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-115">This function differs from the [FILTER](er-functions-list-filter.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="f4b4b-116">Hvis argumentene som er konfigurert for denne funksjonen (`list` og `condition`), tillater at denne forespørselen skal oversettes til det direkte SQL-kallet, utløses en varselmelding ved utformingstid.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-116">If the arguments that are configured for this function (`list` and `condition`) allow this request to be translated to the direct SQL call, a warning message is thrown at design time.</span></span> <span data-ttu-id="f4b4b-117">Denne meldingen informerer brukeren om at ytelsen kan forbedres hvis [FILTER](er-functions-list-filter.md)-funksjonen brukes i stedet for `WHERE`.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-117">This message informs the user that performance might be improved if the [FILTER](er-functions-list-filter.md) function is used instead of `WHERE`.</span></span>

## <a name="example-1"></a><span data-ttu-id="f4b4b-118">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="f4b4b-118">Example 1</span></span>

<span data-ttu-id="f4b4b-119">Hvis **Leverandør** er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, returnerer uttrykket `WHERE (Vendors, Vendors.VendGroup = "40")` en liste over bare leverandører som tilhører leverandørgruppe 40.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-119">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `WHERE (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="f4b4b-120">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="f4b4b-120">Example 2</span></span>

<span data-ttu-id="f4b4b-121">Hvis du angir datakilden **DS** for typen *Beregnet felt*, og den inneholder uttrykket `SPLIT ("A|B|C", "|")`, returnerer uttrykket `WHERE( DS, DS.Value = "B")` en liste med bare én post som inneholder teksten **"B"** i **Verdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f4b4b-121">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `WHERE( DS, DS.Value = "B")` returns a list of only one record that contains the text **"B"** in the **Value** field.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4b4b-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f4b4b-122">Additional resources</span></span>

[<span data-ttu-id="f4b4b-123">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="f4b4b-123">List functions</span></span>](er-functions-category-list.md)
