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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df693d745d1fe74b4500dd3fda0cc0c4be21142d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917034"
---
# <span data-ttu-id="5b3a7-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="5b3a7-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b3a7-104">`CN_GBT_ADDITIONALDIMENSIONID`-funksjonen returnerer en *streng*-verdi som representerer en enkelt finansdimensjons-ID som er hentet fra den angitte strengen.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="5b3a7-105">Den angitte strengen viser alle dimensjonene som en kommadelt liste over IDer.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b3a7-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="5b3a7-106">Syntax</span></span>

```
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="5b3a7-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="5b3a7-107">Arguments</span></span>

<span data-ttu-id="5b3a7-108">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="5b3a7-108">`text`: *String*</span></span>

<span data-ttu-id="5b3a7-109">En *Streng*-verdi viser alle dimensjonene som en kommadelt liste over IDer.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="5b3a7-110">`number`: Heltall</span><span class="sxs-lookup"><span data-stu-id="5b3a7-110">`number`: Integer</span></span>

<span data-ttu-id="5b3a7-111">En *Heltall*-verdi som definerer seriekoden for den forespurte dimensjonen i den angitte strengen.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="5b3a7-112">Returverdier</span><span class="sxs-lookup"><span data-stu-id="5b3a7-112">Return values</span></span>

<span data-ttu-id="5b3a7-113">*Streng*</span><span class="sxs-lookup"><span data-stu-id="5b3a7-113">*String*</span></span>

<span data-ttu-id="5b3a7-114">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="5b3a7-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="5b3a7-115">Example</span></span>

<span data-ttu-id="5b3a7-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returnerer **"CC"**.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5b3a7-117">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5b3a7-117">Additional resources</span></span>

[<span data-ttu-id="5b3a7-118">Andre funksjoner (spesifikke for forretningsområder)</span><span class="sxs-lookup"><span data-stu-id="5b3a7-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
