---
title: ISEMPTY ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ISEMPTY.
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
ms.openlocfilehash: 9c33e8b613bf5bf5bc17a42a7668d4cc4ee58e53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750442"
---
# <a name="isempty-er-function"></a><span data-ttu-id="4293f-103">ISEMPTY ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="4293f-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4293f-104">`ISEMPTY`-funksjonen returnerer den *boolske* verdien **SANN** hvis den angitte listen ikke inneholder noen poster.</span><span class="sxs-lookup"><span data-stu-id="4293f-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="4293f-105">Hvis ikke returneres den *boolske* verdien **USANN**.</span><span class="sxs-lookup"><span data-stu-id="4293f-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4293f-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="4293f-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="4293f-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="4293f-107">Arguments</span></span>

<span data-ttu-id="4293f-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="4293f-108">`list`: *Record list*</span></span>

<span data-ttu-id="4293f-109">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="4293f-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="4293f-110">Returverdier</span><span class="sxs-lookup"><span data-stu-id="4293f-110">Return values</span></span>

<span data-ttu-id="4293f-111">*Boolsk*</span><span class="sxs-lookup"><span data-stu-id="4293f-111">*Boolean*</span></span>

<span data-ttu-id="4293f-112">Den resulterende *boolske* verdien.</span><span class="sxs-lookup"><span data-stu-id="4293f-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="4293f-113">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="4293f-113">Example 1</span></span>

<span data-ttu-id="4293f-114">Hvis du angir datakilde **DS** av *Beregnet felt*-typen, og den inneholder uttrykket `SPLIT ("A|B|C", "|")`, genererer uttrykket `ISEMPTY(DS)` **USANN**.</span><span class="sxs-lookup"><span data-stu-id="4293f-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="4293f-115">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="4293f-115">Example 2</span></span>

<span data-ttu-id="4293f-116">Uttrykket `ISEMPTY (SPLIT ("",1))` returnerer **SANN**.</span><span class="sxs-lookup"><span data-stu-id="4293f-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4293f-117">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4293f-117">Additional resources</span></span>

[<span data-ttu-id="4293f-118">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="4293f-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]