---
title: UPPER ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen UPPER.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3e594138ef8e28f1b3aaf333026fa8f9e55cca0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688347"
---
# <a name="upper-er-function"></a><span data-ttu-id="59b34-103">UPPER ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="59b34-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59b34-104">`UPPER`-funksjonen returnerer den angitte tekststrengen som en *Streng*-verdi etter at den er konvertert til store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="59b34-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="59b34-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="59b34-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="59b34-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="59b34-106">Arguments</span></span>

<span data-ttu-id="59b34-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="59b34-107">`text`: *String*</span></span>

<span data-ttu-id="59b34-108">Den gyldige banen til en datakilde av *Streng*-typen.</span><span class="sxs-lookup"><span data-stu-id="59b34-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="59b34-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="59b34-109">Return values</span></span>

<span data-ttu-id="59b34-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="59b34-110">*String*</span></span>

<span data-ttu-id="59b34-111">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="59b34-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="59b34-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="59b34-112">Example</span></span>

<span data-ttu-id="59b34-113">`UPPER ("Sample")` returnerer **"SAMPLE"**.</span><span class="sxs-lookup"><span data-stu-id="59b34-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59b34-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="59b34-114">Additional resources</span></span>

[<span data-ttu-id="59b34-115">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="59b34-115">Text functions</span></span>](er-functions-category-text.md)
