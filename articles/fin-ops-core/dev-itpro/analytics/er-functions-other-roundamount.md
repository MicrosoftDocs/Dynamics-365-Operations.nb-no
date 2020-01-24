---
title: ROUNDAMOUNT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ROUNDAMOUNT.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c68933352da1f9c7dc5dad76e8635981f8a89fce
ms.sourcegitcommit: 9291e6dc0de076a16684980e528c5aa98845bb34
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2918985"
---
# <span data-ttu-id="243b6-103"><a name="ROUNDAMOUNT">ROUNDAMOUNT ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="243b6-103"><a name="ROUNDAMOUNT">ROUNDAMOUNT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="243b6-104">`ROUNDAMOUNT`-funksjonen returnerer en *reell* verdi som resultatet av avrunding av det angitte beløpet til nærmeste multiplum av et annet nummer i henhold til den angitte avrundingsregelen.</span><span class="sxs-lookup"><span data-stu-id="243b6-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="243b6-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="243b6-105">Syntax</span></span>

```
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="243b6-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="243b6-106">Arguments</span></span>

<span data-ttu-id="243b6-107">`number`: *Int* eller *Real*</span><span class="sxs-lookup"><span data-stu-id="243b6-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="243b6-108">En numerisk verdi som må avrundes.</span><span class="sxs-lookup"><span data-stu-id="243b6-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="243b6-109">`decimals`: *Int* eller *Real*</span><span class="sxs-lookup"><span data-stu-id="243b6-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="243b6-110">Tallet som verdien for `number`-parameteren må avrundes til et multiplum av.</span><span class="sxs-lookup"><span data-stu-id="243b6-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="243b6-111">`round rule`: *Opplistingsverdi*</span><span class="sxs-lookup"><span data-stu-id="243b6-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="243b6-112">En opplistingsverdi for **RoundOffType**-opplistingen som definerer avrundingsregelen.</span><span class="sxs-lookup"><span data-stu-id="243b6-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="243b6-113">Denne opplistingen har følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="243b6-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="243b6-114">Normal (ordinær)</span><span class="sxs-lookup"><span data-stu-id="243b6-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="243b6-115">Nedover (RoundDown)</span><span class="sxs-lookup"><span data-stu-id="243b6-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="243b6-116">Avrundingsmetode (RoundUp)</span><span class="sxs-lookup"><span data-stu-id="243b6-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="243b6-117">Returverdier</span><span class="sxs-lookup"><span data-stu-id="243b6-117">Return values</span></span>

<span data-ttu-id="243b6-118">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="243b6-118">*Real*</span></span>

<span data-ttu-id="243b6-119">Den resulterende numeriske verdien er et multiplum av verdien som er angitt av `decimals`-parameteren, og er nærmest verdien som er angitt av `number`-parameteren.</span><span class="sxs-lookup"><span data-stu-id="243b6-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="243b6-120">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="243b6-120">Usage notes</span></span>

<span data-ttu-id="243b6-121">Når `number`-parameteren er null, returnerer denne funksjonen alltid null.</span><span class="sxs-lookup"><span data-stu-id="243b6-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="243b6-122">Når `decimals`-parameteren er null, runder denne funksjonen av til standard avrundingsverdi.</span><span class="sxs-lookup"><span data-stu-id="243b6-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="243b6-123">Når `round rule`-parameteren er satt til **RoundOffType.Ordinary**, er standard avrundingsverdi **0,01**.</span><span class="sxs-lookup"><span data-stu-id="243b6-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="243b6-124">Hvis ikke er standard avrundingsverdi **1,0**.</span><span class="sxs-lookup"><span data-stu-id="243b6-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="243b6-125">Når `round rule`-parameteren er satt til **RoundOffType.Ordinary**, runder denne funksjonen av til det nærmeste avrundingsbeløpet.</span><span class="sxs-lookup"><span data-stu-id="243b6-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="243b6-126">Når `round rule`-parameteren er satt til **RoundOffType.RoundDown**, runder denne funksjonen av mot null til nærmeste avrundingsbeløpet.</span><span class="sxs-lookup"><span data-stu-id="243b6-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="243b6-127">Når `round rule`-parameteren er satt til **RoundOffType.RoundUp**, runder denne funksjonen bort fra null til nærmeste avrundingsbeløpet.</span><span class="sxs-lookup"><span data-stu-id="243b6-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="243b6-128">Når `round rule`-parameteren er satt til **RoundOffType.Ordinary**, oppfører denne funksjonen seg som [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel-funksjonen og [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X + +-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="243b6-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="243b6-129">Kommentarer</span><span class="sxs-lookup"><span data-stu-id="243b6-129">Remarks</span></span>

<span data-ttu-id="243b6-130">Hvis du vil avrunde en numerisk verdi til et angitt antall desimaler, bruker du [ROUND](er-functions-mathematical-round.md)-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="243b6-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="243b6-131">Eksempel</span><span class="sxs-lookup"><span data-stu-id="243b6-131">Example</span></span>

<span data-ttu-id="243b6-132">Hvis **model.RoundOff**-parameteren er satt til **RoundOffType.Ordinary**, returnerer `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35.</span><span class="sxs-lookup"><span data-stu-id="243b6-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="243b6-133">Hvis **model.RoundOff**-parameteren er satt til **RoundOffType.RoundDown**, returnerer `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35.</span><span class="sxs-lookup"><span data-stu-id="243b6-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="243b6-134">Hvis **model.RoundOff**-parameteren er satt til **RoundOffType.RoundUp**, returnerer `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 8,4.</span><span class="sxs-lookup"><span data-stu-id="243b6-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="243b6-135">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="243b6-135">Additional resources</span></span>

[<span data-ttu-id="243b6-136">Andre funksjoner (spesifikke for forretningsområder)</span><span class="sxs-lookup"><span data-stu-id="243b6-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="243b6-137">Matematiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="243b6-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)