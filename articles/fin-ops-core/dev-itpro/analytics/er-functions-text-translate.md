---
title: TRANSLATE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen TRANSLATE.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 11954f3e48d8dc2257b3a0bc8768df47af3c5c0c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916712"
---
# <span data-ttu-id="bd7a9-103"><a name="TRANSLATE">TRANSLATE ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="bd7a9-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd7a9-104">`TRANSLATE`-funksjonen returnerer den angitte tekststrengen som en *streng*-verdi etter at hele eller deler av den er erstattet med en annen streng.</span><span class="sxs-lookup"><span data-stu-id="bd7a9-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd7a9-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="bd7a9-105">Syntax</span></span>

```
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="bd7a9-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="bd7a9-106">Arguments</span></span>

<span data-ttu-id="bd7a9-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="bd7a9-107">`text`: *String*</span></span>

<span data-ttu-id="bd7a9-108">Den gyldige banen til en datakilde av *Streng*-typen.</span><span class="sxs-lookup"><span data-stu-id="bd7a9-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="bd7a9-109">`pattern`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="bd7a9-109">`pattern`: *String*</span></span>

<span data-ttu-id="bd7a9-110">Teksten som må erstattes.</span><span class="sxs-lookup"><span data-stu-id="bd7a9-110">The text that must be replaced.</span></span>

<span data-ttu-id="bd7a9-111">`replacement`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="bd7a9-111">`replacement`: *String*</span></span>

<span data-ttu-id="bd7a9-112">Teksten som skal brukes som erstatning.</span><span class="sxs-lookup"><span data-stu-id="bd7a9-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="bd7a9-113">Returverdier</span><span class="sxs-lookup"><span data-stu-id="bd7a9-113">Return values</span></span>

<span data-ttu-id="bd7a9-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="bd7a9-114">*String*</span></span>

<span data-ttu-id="bd7a9-115">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="bd7a9-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="bd7a9-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="bd7a9-116">Example</span></span>

<span data-ttu-id="bd7a9-117">`TRANSLATE ("abcdef", "cd", "GH")` erstatter mønsteret **"cd"** med strengen **"GH"** og returnerer **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="bd7a9-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bd7a9-118">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="bd7a9-118">Additional resources</span></span>

[<span data-ttu-id="bd7a9-119">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="bd7a9-119">Text functions</span></span>](er-functions-category-text.md)
