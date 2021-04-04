---
title: ROUNDDOWN ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ROUNDDOWN.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: f199d662eb31f184b6f978b3d251e64907254584
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567146"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="344b1-103">ROUNDDOWN ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="344b1-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="344b1-104">`ROUNDDOWN`-funksjonen returnerer det angitte tallet som en *reell* verdi etter at det er rundet ned til angitt antall desimaler.</span><span class="sxs-lookup"><span data-stu-id="344b1-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="344b1-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="344b1-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="344b1-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="344b1-106">Arguments</span></span>

<span data-ttu-id="344b1-107">`number`: *Reell*</span><span class="sxs-lookup"><span data-stu-id="344b1-107">`number`: *Real*</span></span>

<span data-ttu-id="344b1-108">En numerisk verdi som må avrundes ned.</span><span class="sxs-lookup"><span data-stu-id="344b1-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="344b1-109">`decimals`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="344b1-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="344b1-110">En numerisk verdi som representerer antall desimaler.</span><span class="sxs-lookup"><span data-stu-id="344b1-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="344b1-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="344b1-111">Return values</span></span>

<span data-ttu-id="344b1-112">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="344b1-112">*Real*</span></span>

<span data-ttu-id="344b1-113">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="344b1-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="344b1-114">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="344b1-114">Usage notes</span></span>

<span data-ttu-id="344b1-115">Denne funksjonen fungerer som [ROUND](er-functions-mathematical-round.md), men den avrunder alltid ned det angitte tallet (mot null).</span><span class="sxs-lookup"><span data-stu-id="344b1-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="344b1-116">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="344b1-116">Example 1</span></span>

<span data-ttu-id="344b1-117">`ROUNDDOWN (1200.767, 2)` avrunder ned til to desimalplasser og returnerer **1200.76**.</span><span class="sxs-lookup"><span data-stu-id="344b1-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="344b1-118">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="344b1-118">Example 2</span></span>

<span data-ttu-id="344b1-119">`ROUNDDOWN (1700.767, -3)` avrunder ned til nærmeste multiplum av 1 000, og returnerer **1000**.</span><span class="sxs-lookup"><span data-stu-id="344b1-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="344b1-120">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="344b1-120">Additional resources</span></span>

[<span data-ttu-id="344b1-121">Matematiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="344b1-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]