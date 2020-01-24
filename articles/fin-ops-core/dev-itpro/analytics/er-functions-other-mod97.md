---
title: MOD_97 ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen MOD_97
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
ms.openlocfilehash: 23e63f6b7999399fd5365c616613cbc603774d53
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916942"
---
# <span data-ttu-id="7e28d-103"><a name="MOD_97">MOD_97 ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="7e28d-103"><a name="MOD_97">MOD_97 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e28d-104">`MOD_97`-funksjonen returnerer en *streng*-verdi som representerer en kreditorreferanse som et MOD97-uttrykk, basert på sifrene i det angitte fakturanummeret.</span><span class="sxs-lookup"><span data-stu-id="7e28d-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e28d-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="7e28d-105">Syntax</span></span>

```
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="7e28d-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="7e28d-106">Arguments</span></span>

<span data-ttu-id="7e28d-107">`invoice number digits`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="7e28d-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="7e28d-108">En tekstverdi som representerer sifrene i et fakturanummer.</span><span class="sxs-lookup"><span data-stu-id="7e28d-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="7e28d-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="7e28d-109">Return values</span></span>

<span data-ttu-id="7e28d-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="7e28d-110">*String*</span></span>

<span data-ttu-id="7e28d-111">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="7e28d-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="7e28d-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="7e28d-112">Example</span></span>

<span data-ttu-id="7e28d-113">`MOD_97 ("VEND-200002")` returnerer **"20000285"**.</span><span class="sxs-lookup"><span data-stu-id="7e28d-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7e28d-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="7e28d-114">Additional resources</span></span>

[<span data-ttu-id="7e28d-115">Andre funksjoner (spesifikke for forretningsområder)</span><span class="sxs-lookup"><span data-stu-id="7e28d-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
