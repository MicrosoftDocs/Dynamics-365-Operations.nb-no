---
title: LEN ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen LEN
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
ms.openlocfilehash: e51e181de53cd185679110e99b9f89695bacdf92
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744269"
---
# <a name="len-er-function"></a><span data-ttu-id="8dd6a-103">LEN ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="8dd6a-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8dd6a-104">`LEN`-funksjonen returnerer antall tegn i den angitte strengen som en *Heltall*-verdi.</span><span class="sxs-lookup"><span data-stu-id="8dd6a-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dd6a-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="8dd6a-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="8dd6a-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="8dd6a-106">Arguments</span></span>

<span data-ttu-id="8dd6a-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="8dd6a-107">`text`: *String*</span></span>

<span data-ttu-id="8dd6a-108">En *streng*-verdi som angir teksten.</span><span class="sxs-lookup"><span data-stu-id="8dd6a-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="8dd6a-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="8dd6a-109">Return values</span></span>

<span data-ttu-id="8dd6a-110">*Heltall*</span><span class="sxs-lookup"><span data-stu-id="8dd6a-110">*Integer*</span></span>

<span data-ttu-id="8dd6a-111">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="8dd6a-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="8dd6a-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="8dd6a-112">Example</span></span>

<span data-ttu-id="8dd6a-113">`LEN ("Sample")` returnerer **6**.</span><span class="sxs-lookup"><span data-stu-id="8dd6a-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8dd6a-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8dd6a-114">Additional resources</span></span>

[<span data-ttu-id="8dd6a-115">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="8dd6a-115">Text functions</span></span>](er-functions-category-text.md)
