---
title: CN_GBT_ADDITIONALDIMENSIONID ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen CN_GBT_ADDITIONALDIMENSIONID ER
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38908c63c35465747505479bc983ada891f9e2bf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686816"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="99206-103">CN_GBT_ADDITIONALDIMENSIONID ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="99206-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99206-104">`CN_GBT_ADDITIONALDIMENSIONID`-funksjonen returnerer en *streng*-verdi som representerer en enkelt finansdimensjons-ID som er hentet fra den angitte strengen.</span><span class="sxs-lookup"><span data-stu-id="99206-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="99206-105">Den angitte strengen viser alle dimensjonene som en kommadelt liste over IDer.</span><span class="sxs-lookup"><span data-stu-id="99206-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="99206-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="99206-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="99206-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="99206-107">Arguments</span></span>

<span data-ttu-id="99206-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="99206-108">`text`: *String*</span></span>

<span data-ttu-id="99206-109">En *Streng*-verdi viser alle dimensjonene som en kommadelt liste over IDer.</span><span class="sxs-lookup"><span data-stu-id="99206-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="99206-110">`number`: Heltall</span><span class="sxs-lookup"><span data-stu-id="99206-110">`number`: Integer</span></span>

<span data-ttu-id="99206-111">En *Heltall*-verdi som definerer seriekoden for den forespurte dimensjonen i den angitte strengen.</span><span class="sxs-lookup"><span data-stu-id="99206-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="99206-112">Returverdier</span><span class="sxs-lookup"><span data-stu-id="99206-112">Return values</span></span>

<span data-ttu-id="99206-113">*Streng*</span><span class="sxs-lookup"><span data-stu-id="99206-113">*String*</span></span>

<span data-ttu-id="99206-114">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="99206-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="99206-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="99206-115">Example</span></span>

<span data-ttu-id="99206-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returnerer **"CC"**.</span><span class="sxs-lookup"><span data-stu-id="99206-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="99206-117">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="99206-117">Additional resources</span></span>

[<span data-ttu-id="99206-118">Andre funksjoner (spesifikke for forretningsområder)</span><span class="sxs-lookup"><span data-stu-id="99206-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
