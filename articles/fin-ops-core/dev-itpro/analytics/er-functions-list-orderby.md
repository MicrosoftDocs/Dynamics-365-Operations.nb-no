---
title: ORDERBY ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ORDERBY.
author: NickSelin
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
ms.openlocfilehash: 51da7f3766f5af901c8be6668bc2511cd8e2f9e9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753198"
---
# <a name="orderby-er-function"></a><span data-ttu-id="9a48a-103">ORDERBY ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="9a48a-103">ORDERBY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a48a-104">`ORDERBY`-funksjonen returnerer den angitte listen som en *postliste*-verdi etter at den er sortert i henhold til de angitte argumentene.</span><span class="sxs-lookup"><span data-stu-id="9a48a-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="9a48a-105">Disse argumentene kan defineres som uttrykk.</span><span class="sxs-lookup"><span data-stu-id="9a48a-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a48a-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="9a48a-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="9a48a-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="9a48a-107">Arguments</span></span>

<span data-ttu-id="9a48a-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="9a48a-108">`list`: *Record list*</span></span>

<span data-ttu-id="9a48a-109">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="9a48a-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="9a48a-110">`expression 1`: *Felt*</span><span class="sxs-lookup"><span data-stu-id="9a48a-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="9a48a-111">Den gyldige banen til et felt i datakilden som `list`-argumentet for den kalte funksjonen refererer til.</span><span class="sxs-lookup"><span data-stu-id="9a48a-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="9a48a-112">Det refererte feltet må være et felt av den primitive datatypen.</span><span class="sxs-lookup"><span data-stu-id="9a48a-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="9a48a-113">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="9a48a-113">This argument is required.</span></span>

<span data-ttu-id="9a48a-114">`expression N`: *Felt*</span><span class="sxs-lookup"><span data-stu-id="9a48a-114">`expression N`: *Field*</span></span>

<span data-ttu-id="9a48a-115">Den gyldige banen til et felt i datakilden som `list`-argumentet for den kalte funksjonen refererer til.</span><span class="sxs-lookup"><span data-stu-id="9a48a-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="9a48a-116">Det refererte feltet må være et felt av den primitive datatypen.</span><span class="sxs-lookup"><span data-stu-id="9a48a-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="9a48a-117">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="9a48a-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="9a48a-118">Returverdier</span><span class="sxs-lookup"><span data-stu-id="9a48a-118">Return values</span></span>

<span data-ttu-id="9a48a-119">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="9a48a-119">*Record list*</span></span>

<span data-ttu-id="9a48a-120">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="9a48a-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="9a48a-121">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="9a48a-121">Example 1</span></span>

<span data-ttu-id="9a48a-122">Hvis du angir datakilde **DS** av *Beregnet felt*-typen, og den inneholder uttrykket `SPLIT ("C|B|A", "|")`, genererer uttrykket `FIRST( ORDERBY( DS, DS. Value)).Value` tekstverdien **"A"**.</span><span class="sxs-lookup"><span data-stu-id="9a48a-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="9a48a-123">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="9a48a-123">Example 2</span></span>

<span data-ttu-id="9a48a-124">Hvis **Leverandør** er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, returnerer uttrykket `ORDERBY (Vendors, Vendors.'name()')` en liste over leverandører sortert etter navn i stigende rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="9a48a-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9a48a-125">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="9a48a-125">Additional resources</span></span>

[<span data-ttu-id="9a48a-126">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="9a48a-126">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]