---
title: LOWER ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen LOWER.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 12577e571c8e87db79395895e2a22e66ee7df32c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745687"
---
# <a name="lower-er-function"></a><span data-ttu-id="e8852-103">LOWER ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="e8852-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8852-104">`LOWER`-funksjonen returnerer den angitte tekststrengen som en *Streng*-verdi etter at den er konvertert til små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="e8852-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8852-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="e8852-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="e8852-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="e8852-106">Arguments</span></span>

<span data-ttu-id="e8852-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="e8852-107">`text`: *String*</span></span>

<span data-ttu-id="e8852-108">En *streng*-verdi som angir teksten.</span><span class="sxs-lookup"><span data-stu-id="e8852-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="e8852-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="e8852-109">Return values</span></span>

<span data-ttu-id="e8852-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="e8852-110">*String*</span></span>

<span data-ttu-id="e8852-111">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="e8852-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="e8852-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e8852-112">Example</span></span>

<span data-ttu-id="e8852-113">`LOWER ("Sample")` returnerer **"sample"**.</span><span class="sxs-lookup"><span data-stu-id="e8852-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8852-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e8852-114">Additional resources</span></span>

[<span data-ttu-id="e8852-115">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="e8852-115">Text functions</span></span>](er-functions-category-text.md)
