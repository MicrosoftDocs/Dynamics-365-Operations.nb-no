---
title: FA_SUM ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen FA_SUM
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
ms.openlocfilehash: 32eb07689598a3b6c852f272b480106670b88cd0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916988"
---
# <span data-ttu-id="bbe4e-103"><a name="FA_SUM">FA_SUM ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="bbe4e-103"><a name="FA_SUM">FA_SUM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bbe4e-104">`FA_SUM`-funksjonen returnerer en *Container (post)*-verdi som består av data for anleggsmiddelbeløpene for den angitte anleggsmiddelvaren, verdimodellkoden, rapporteringsåret og datoperioden.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe4e-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="bbe4e-105">Syntax</span></span>

```
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="bbe4e-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="bbe4e-106">Arguments</span></span>

<span data-ttu-id="bbe4e-107">`fixed asset code`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="bbe4e-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="bbe4e-108">En *streng*-verdi som representerer koden for en anleggsmiddelvare som saldoen beregnes for.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="bbe4e-109">`value model code`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="bbe4e-109">`value model code`: *String*</span></span>

<span data-ttu-id="bbe4e-110">En *streng*-verdi som representerer koden for en verdimodell som saldoen beregnes for.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="bbe4e-111">`start date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="bbe4e-111">`start date`: *Date*</span></span>

<span data-ttu-id="bbe4e-112">En *dato*-verdi som representerer startdatoen for en periode som anleggsmiddelbeløpene beregnes for.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="bbe4e-113">`end date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="bbe4e-113">`end date`: *Date*</span></span>

<span data-ttu-id="bbe4e-114">En *dato*-verdi som representerer sluttdatoen for en periode som anleggsmiddelbeløpene beregnes for.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="bbe4e-115">Returverdier</span><span class="sxs-lookup"><span data-stu-id="bbe4e-115">Return values</span></span>

<span data-ttu-id="bbe4e-116">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="bbe4e-116">*Container (record)*</span></span>

<span data-ttu-id="bbe4e-117">Den resulterende postvedien.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="bbe4e-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="bbe4e-118">Example</span></span>

<span data-ttu-id="bbe4e-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returnerer databeholderen for anleggsmiddel **COMP-000001** som er klargjort for den **gjeldende**-verdimodellen, og for en periode fra **Dato1** til **Dato2**.</span><span class="sxs-lookup"><span data-stu-id="bbe4e-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bbe4e-120">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="bbe4e-120">Additional resources</span></span>

[<span data-ttu-id="bbe4e-121">Andre funksjoner (spesifikke for forretningsområder)</span><span class="sxs-lookup"><span data-stu-id="bbe4e-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
