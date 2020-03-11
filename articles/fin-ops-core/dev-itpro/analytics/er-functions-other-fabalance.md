---
title: FA_BALANCE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen FA_BALANCE.
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
ms.openlocfilehash: 76a087157ae53e2c571654ade7383d7bd7a005c3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041452"
---
# <span data-ttu-id="cf5de-103"><a name="FA_BALANCE">FA_BALANCE ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="cf5de-103"><a name="FA_BALANCE">FA_BALANCE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf5de-104">`FA_BALANCE`-funksjonen returnerer en *Container (post)*-verdi som består av data for anleggsmiddelsaldoen for den angitte anleggsmiddelvaren, verdimodellkoden, rapporteringsåret og rapporteringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="cf5de-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf5de-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="cf5de-105">Syntax</span></span>

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="cf5de-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="cf5de-106">Arguments</span></span>

<span data-ttu-id="cf5de-107">`fixed asset code`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="cf5de-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="cf5de-108">En *streng*-verdi som representerer koden for en anleggsmiddelvare som saldoen beregnes for.</span><span class="sxs-lookup"><span data-stu-id="cf5de-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="cf5de-109">`value model code`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="cf5de-109">`value model code`: *String*</span></span>

<span data-ttu-id="cf5de-110">En *streng*-verdi som representerer koden for en verdimodell som saldoen beregnes for.</span><span class="sxs-lookup"><span data-stu-id="cf5de-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="cf5de-111">`reporting year`: *Opplistingsverdi*</span><span class="sxs-lookup"><span data-stu-id="cf5de-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="cf5de-112">En opplistingsverdi for **AssetYear**-programmet som definerer en periode for saldoberegningen.</span><span class="sxs-lookup"><span data-stu-id="cf5de-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="cf5de-113">`reporting date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="cf5de-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="cf5de-114">En *dato*-verdi som definerer en dato for saldoberegningen.</span><span class="sxs-lookup"><span data-stu-id="cf5de-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="cf5de-115">Returverdier</span><span class="sxs-lookup"><span data-stu-id="cf5de-115">Return values</span></span>

<span data-ttu-id="cf5de-116">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="cf5de-116">*Container (record)*</span></span>

<span data-ttu-id="cf5de-117">Den resulterende postvedien.</span><span class="sxs-lookup"><span data-stu-id="cf5de-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="cf5de-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="cf5de-118">Example</span></span>

<span data-ttu-id="cf5de-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returnerer den klargjorte databeholderen for saldoer for anleggsmidlet **COMP-000001** som har verdimodellen **Gjeldende** på den gjeldende datoen for programøkten.</span><span class="sxs-lookup"><span data-stu-id="cf5de-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf5de-120">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="cf5de-120">Additional resources</span></span>

[<span data-ttu-id="cf5de-121">Andre funksjoner (spesifikke for forretningsområder)</span><span class="sxs-lookup"><span data-stu-id="cf5de-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
