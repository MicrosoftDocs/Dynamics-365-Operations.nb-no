---
title: ROUNDDOWN ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ROUNDDOWN.
author: NickSelin
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
ms.openlocfilehash: 89fc134ec11a47506211ce68ec3aaf966d9a308b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744469"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="a62c6-103">ROUNDDOWN ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="a62c6-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a62c6-104">`ROUNDDOWN`-funksjonen returnerer det angitte tallet som en *reell* verdi etter at det er rundet ned til angitt antall desimaler.</span><span class="sxs-lookup"><span data-stu-id="a62c6-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="a62c6-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="a62c6-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="a62c6-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="a62c6-106">Arguments</span></span>

<span data-ttu-id="a62c6-107">`number`: *Reell*</span><span class="sxs-lookup"><span data-stu-id="a62c6-107">`number`: *Real*</span></span>

<span data-ttu-id="a62c6-108">En numerisk verdi som må avrundes ned.</span><span class="sxs-lookup"><span data-stu-id="a62c6-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="a62c6-109">`decimals`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="a62c6-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="a62c6-110">En numerisk verdi som representerer antall desimaler.</span><span class="sxs-lookup"><span data-stu-id="a62c6-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="a62c6-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="a62c6-111">Return values</span></span>

<span data-ttu-id="a62c6-112">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="a62c6-112">*Real*</span></span>

<span data-ttu-id="a62c6-113">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="a62c6-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a62c6-114">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="a62c6-114">Usage notes</span></span>

<span data-ttu-id="a62c6-115">Denne funksjonen fungerer som [ROUND](er-functions-mathematical-round.md), men den avrunder alltid ned det angitte tallet (mot null).</span><span class="sxs-lookup"><span data-stu-id="a62c6-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="a62c6-116">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="a62c6-116">Example 1</span></span>

<span data-ttu-id="a62c6-117">`ROUNDDOWN (1200.767, 2)` avrunder ned til to desimalplasser og returnerer **1200.76**.</span><span class="sxs-lookup"><span data-stu-id="a62c6-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="a62c6-118">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="a62c6-118">Example 2</span></span>

<span data-ttu-id="a62c6-119">`ROUNDDOWN (1700.767, -3)` avrunder ned til nærmeste multiplum av 1 000, og returnerer **1000**.</span><span class="sxs-lookup"><span data-stu-id="a62c6-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a62c6-120">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a62c6-120">Additional resources</span></span>

[<span data-ttu-id="a62c6-121">Matematiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="a62c6-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]