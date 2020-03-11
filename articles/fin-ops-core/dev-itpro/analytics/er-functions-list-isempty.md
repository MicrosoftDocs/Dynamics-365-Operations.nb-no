---
title: ISEMPTY ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ISEMPTY.
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
ms.openlocfilehash: 6adca3c95c10e7d4b3287561925a9d9fe8a74121
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042050"
---
# <span data-ttu-id="cc30f-103"><a name="ISEMPTY">ISEMPTY ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="cc30f-103"><a name="ISEMPTY">ISEMPTY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc30f-104">`ISEMPTY`-funksjonen returnerer den *boolske* verdien **SANN** hvis den angitte listen ikke inneholder noen poster.</span><span class="sxs-lookup"><span data-stu-id="cc30f-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="cc30f-105">Hvis ikke returneres den *boolske* verdien **USANN**.</span><span class="sxs-lookup"><span data-stu-id="cc30f-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc30f-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="cc30f-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="cc30f-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="cc30f-107">Arguments</span></span>

<span data-ttu-id="cc30f-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="cc30f-108">`list`: *Record list*</span></span>

<span data-ttu-id="cc30f-109">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="cc30f-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="cc30f-110">Returverdier</span><span class="sxs-lookup"><span data-stu-id="cc30f-110">Return values</span></span>

<span data-ttu-id="cc30f-111">*Boolsk*</span><span class="sxs-lookup"><span data-stu-id="cc30f-111">*Boolean*</span></span>

<span data-ttu-id="cc30f-112">Den resulterende *boolske* verdien.</span><span class="sxs-lookup"><span data-stu-id="cc30f-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="cc30f-113">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="cc30f-113">Example 1</span></span>

<span data-ttu-id="cc30f-114">Hvis du angir datakilde **DS** av *Beregnet felt*-typen, og den inneholder uttrykket `SPLIT ("A|B|C", "|")`, genererer uttrykket `ISEMPTY(DS)` **USANN**.</span><span class="sxs-lookup"><span data-stu-id="cc30f-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="cc30f-115">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="cc30f-115">Example 2</span></span>

<span data-ttu-id="cc30f-116">Uttrykket `ISEMPTY (SPLIT ("",1))` returnerer **SANN**.</span><span class="sxs-lookup"><span data-stu-id="cc30f-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc30f-117">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="cc30f-117">Additional resources</span></span>

[<span data-ttu-id="cc30f-118">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="cc30f-118">List functions</span></span>](er-functions-category-list.md)
