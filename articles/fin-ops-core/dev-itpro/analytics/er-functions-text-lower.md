---
title: LOWER ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen LOWER.
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: e684883d4262e4c3cd8a84d0a1c6f1d685bb650b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746297"
---
# <a name="lower-er-function"></a><span data-ttu-id="a004a-103">LOWER ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="a004a-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a004a-104">`LOWER`-funksjonen returnerer den angitte tekststrengen som en *Streng*-verdi etter at den er konvertert til små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="a004a-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="a004a-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="a004a-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="a004a-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="a004a-106">Arguments</span></span>

<span data-ttu-id="a004a-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="a004a-107">`text`: *String*</span></span>

<span data-ttu-id="a004a-108">En *streng*-verdi som angir teksten.</span><span class="sxs-lookup"><span data-stu-id="a004a-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="a004a-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="a004a-109">Return values</span></span>

<span data-ttu-id="a004a-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="a004a-110">*String*</span></span>

<span data-ttu-id="a004a-111">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="a004a-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="a004a-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a004a-112">Example</span></span>

<span data-ttu-id="a004a-113">`LOWER ("Sample")` returnerer **"sample"**.</span><span class="sxs-lookup"><span data-stu-id="a004a-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a004a-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a004a-114">Additional resources</span></span>

[<span data-ttu-id="a004a-115">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="a004a-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]