---
title: FA_BALANCE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen FA_BALANCE.
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
ms.openlocfilehash: 37c440a5c626016ebdb75703a2be63c9a1a2b560
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567598"
---
# <a name="fa_balance-er-function"></a><span data-ttu-id="9d786-103">FA_BALANCE ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="9d786-103">FA_BALANCE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d786-104">`FA_BALANCE`-funksjonen returnerer en *Container (post)*-verdi som består av data for anleggsmiddelsaldoen for den angitte anleggsmiddelvaren, verdimodellkoden, rapporteringsåret og rapporteringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="9d786-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d786-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="9d786-105">Syntax</span></span>

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="9d786-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="9d786-106">Arguments</span></span>

<span data-ttu-id="9d786-107">`fixed asset code`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="9d786-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="9d786-108">En *streng*-verdi som representerer koden for en anleggsmiddelvare som saldoen beregnes for.</span><span class="sxs-lookup"><span data-stu-id="9d786-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="9d786-109">`value model code`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="9d786-109">`value model code`: *String*</span></span>

<span data-ttu-id="9d786-110">En *streng*-verdi som representerer koden for en verdimodell som saldoen beregnes for.</span><span class="sxs-lookup"><span data-stu-id="9d786-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="9d786-111">`reporting year`: *Opplistingsverdi*</span><span class="sxs-lookup"><span data-stu-id="9d786-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="9d786-112">En opplistingsverdi for **AssetYear**-programmet som definerer en periode for saldoberegningen.</span><span class="sxs-lookup"><span data-stu-id="9d786-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="9d786-113">`reporting date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="9d786-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="9d786-114">En *dato*-verdi som definerer en dato for saldoberegningen.</span><span class="sxs-lookup"><span data-stu-id="9d786-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="9d786-115">Returverdier</span><span class="sxs-lookup"><span data-stu-id="9d786-115">Return values</span></span>

<span data-ttu-id="9d786-116">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="9d786-116">*Container (record)*</span></span>

<span data-ttu-id="9d786-117">Den resulterende postvedien.</span><span class="sxs-lookup"><span data-stu-id="9d786-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="9d786-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="9d786-118">Example</span></span>

<span data-ttu-id="9d786-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returnerer den klargjorte databeholderen for saldoer for anleggsmidlet **COMP-000001** som har verdimodellen **Gjeldende** på den gjeldende datoen for programøkten.</span><span class="sxs-lookup"><span data-stu-id="9d786-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9d786-120">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="9d786-120">Additional resources</span></span>

[<span data-ttu-id="9d786-121">Andre funksjoner (spesifikke for forretningsområder)</span><span class="sxs-lookup"><span data-stu-id="9d786-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]