---
title: ORDERBY ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ORDERBY.
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
ms.openlocfilehash: 6ff280d66fd2c418984f2d7fd31a32609932e89c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745015"
---
# <a name="orderby-er-function"></a><span data-ttu-id="1504b-103">ORDERBY ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="1504b-103">ORDERBY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1504b-104">`ORDERBY`-funksjonen returnerer den angitte listen som en *postliste*-verdi etter at den er sortert i henhold til de angitte argumentene.</span><span class="sxs-lookup"><span data-stu-id="1504b-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="1504b-105">Disse argumentene kan defineres som uttrykk.</span><span class="sxs-lookup"><span data-stu-id="1504b-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="1504b-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="1504b-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="1504b-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="1504b-107">Arguments</span></span>

<span data-ttu-id="1504b-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="1504b-108">`list`: *Record list*</span></span>

<span data-ttu-id="1504b-109">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="1504b-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="1504b-110">`expression 1`: *Felt*</span><span class="sxs-lookup"><span data-stu-id="1504b-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="1504b-111">Den gyldige banen til et felt i datakilden som `list`-argumentet for den kalte funksjonen refererer til.</span><span class="sxs-lookup"><span data-stu-id="1504b-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="1504b-112">Det refererte feltet må være et felt av den primitive datatypen.</span><span class="sxs-lookup"><span data-stu-id="1504b-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="1504b-113">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="1504b-113">This argument is required.</span></span>

<span data-ttu-id="1504b-114">`expression N`: *Felt*</span><span class="sxs-lookup"><span data-stu-id="1504b-114">`expression N`: *Field*</span></span>

<span data-ttu-id="1504b-115">Den gyldige banen til et felt i datakilden som `list`-argumentet for den kalte funksjonen refererer til.</span><span class="sxs-lookup"><span data-stu-id="1504b-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="1504b-116">Det refererte feltet må være et felt av den primitive datatypen.</span><span class="sxs-lookup"><span data-stu-id="1504b-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="1504b-117">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="1504b-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="1504b-118">Returverdier</span><span class="sxs-lookup"><span data-stu-id="1504b-118">Return values</span></span>

<span data-ttu-id="1504b-119">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="1504b-119">*Record list*</span></span>

<span data-ttu-id="1504b-120">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="1504b-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="1504b-121">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="1504b-121">Example 1</span></span>

<span data-ttu-id="1504b-122">Hvis du angir datakilde **DS** av *Beregnet felt*-typen, og den inneholder uttrykket `SPLIT ("C|B|A", "|")`, genererer uttrykket `FIRST( ORDERBY( DS, DS. Value)).Value` tekstverdien **"A"**.</span><span class="sxs-lookup"><span data-stu-id="1504b-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="1504b-123">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="1504b-123">Example 2</span></span>

<span data-ttu-id="1504b-124">Hvis **Leverandør** er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, returnerer uttrykket `ORDERBY (Vendors, Vendors.'name()')` en liste over leverandører sortert etter navn i stigende rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="1504b-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1504b-125">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="1504b-125">Additional resources</span></span>

[<span data-ttu-id="1504b-126">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="1504b-126">List functions</span></span>](er-functions-category-list.md)
