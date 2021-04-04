---
title: AND ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen AND
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
ms.openlocfilehash: 068b9a3b2cf2e5bffe895bc4e8a7cbb2d8025ad7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560091"
---
# <a name="and-er-function"></a><span data-ttu-id="2b01d-103">AND ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="2b01d-103">AND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b01d-104">`AND`-funksjonen returnerer en *boolsk* verdi av **SANN** hvis alle de angitte betingelsene er sanne.</span><span class="sxs-lookup"><span data-stu-id="2b01d-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="2b01d-105">Hvis ikke returneres den *boolske* verdien **USANN**.</span><span class="sxs-lookup"><span data-stu-id="2b01d-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b01d-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="2b01d-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="2b01d-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="2b01d-107">Arguments</span></span>

<span data-ttu-id="2b01d-108">`condition 1`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="2b01d-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="2b01d-109">Et gyldig betingelsesuttrykk som må testes.</span><span class="sxs-lookup"><span data-stu-id="2b01d-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="2b01d-110">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="2b01d-110">This argument is required.</span></span>

<span data-ttu-id="2b01d-111">`condition N`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="2b01d-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="2b01d-112">Et gyldig betingelsesuttrykk som må testes.</span><span class="sxs-lookup"><span data-stu-id="2b01d-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="2b01d-113">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="2b01d-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="2b01d-114">Returverdier</span><span class="sxs-lookup"><span data-stu-id="2b01d-114">Return values</span></span>

<span data-ttu-id="2b01d-115">*Boolsk*</span><span class="sxs-lookup"><span data-stu-id="2b01d-115">*Boolean*</span></span>

<span data-ttu-id="2b01d-116">Den resulterende *boolske* verdien.</span><span class="sxs-lookup"><span data-stu-id="2b01d-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2b01d-117">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="2b01d-117">Usage notes</span></span>

<span data-ttu-id="2b01d-118">I argumentene til logiske funksjoner kan du bruke datakildereferanser, tall- og tekstverdier, boolske verdier, sammenligningsoperatorer og andre funksjoner for elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="2b01d-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="2b01d-119">Alle argumentene må imidlertid evalueres til en *boolsk* verdi som er **SANN** eller **USANN**.</span><span class="sxs-lookup"><span data-stu-id="2b01d-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="2b01d-120">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b01d-120">Example</span></span>

<span data-ttu-id="2b01d-121">`AND (1=1, "a"="a")` returnerer **SANN**.</span><span class="sxs-lookup"><span data-stu-id="2b01d-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="2b01d-122">`AND (1=2, "a"="a")` returnerer **USANN**.</span><span class="sxs-lookup"><span data-stu-id="2b01d-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2b01d-123">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="2b01d-123">Additional resources</span></span>

[<span data-ttu-id="2b01d-124">Logiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="2b01d-124">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]