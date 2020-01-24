---
title: TRIM ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen TRIM
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 2673b0167f7602a6d6eaa79be639905028e99822
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915539"
---
# <span data-ttu-id="3dcab-103"><a name="TRIM">TRIM ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="3dcab-103"><a name="TRIM">TRIM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3dcab-104">`TRIM`-funksjonen returnerer den angitte tekststrengen som en *streng*-verdi etter at innledende og etterfølgende mellomrom er avkortet, og når flere mellomrom mellom ord er fjernet.</span><span class="sxs-lookup"><span data-stu-id="3dcab-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dcab-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="3dcab-105">Syntax</span></span>

```
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="3dcab-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="3dcab-106">Arguments</span></span>

<span data-ttu-id="3dcab-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="3dcab-107">`text`: *String*</span></span>

<span data-ttu-id="3dcab-108">Den gyldige banen til en datakilde av *Streng*-typen.</span><span class="sxs-lookup"><span data-stu-id="3dcab-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="3dcab-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="3dcab-109">Return values</span></span>

<span data-ttu-id="3dcab-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="3dcab-110">*String*</span></span>

<span data-ttu-id="3dcab-111">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="3dcab-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="3dcab-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="3dcab-112">Example</span></span>

<span data-ttu-id="3dcab-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returnerer **"Eksempeltekst"**.</span><span class="sxs-lookup"><span data-stu-id="3dcab-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3dcab-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="3dcab-114">Additional resources</span></span>

[<span data-ttu-id="3dcab-115">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="3dcab-115">Text functions</span></span>](er-functions-category-text.md)
