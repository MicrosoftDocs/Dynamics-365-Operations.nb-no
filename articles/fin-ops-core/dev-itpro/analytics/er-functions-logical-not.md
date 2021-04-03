---
title: NOT ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NOT
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 9b55b3d8930ece7e2f2925579821ca88749801f7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565886"
---
# <a name="not-er-function"></a><span data-ttu-id="c2db7-103">NOT ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="c2db7-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2db7-104">`NOT`-funksjonen returnerer den omvendte logiske verdien til den angitte betingelsen som en *boolsk* verdi.</span><span class="sxs-lookup"><span data-stu-id="c2db7-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2db7-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="c2db7-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="c2db7-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="c2db7-106">Arguments</span></span>

<span data-ttu-id="c2db7-107">`condition`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="c2db7-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="c2db7-108">Et gyldig betingelsesuttrykk som må tilbakeføres.</span><span class="sxs-lookup"><span data-stu-id="c2db7-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="c2db7-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="c2db7-109">Return values</span></span>

<span data-ttu-id="c2db7-110">*Boolsk*</span><span class="sxs-lookup"><span data-stu-id="c2db7-110">*Boolean*</span></span>

<span data-ttu-id="c2db7-111">Den resulterende *boolske* verdien.</span><span class="sxs-lookup"><span data-stu-id="c2db7-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="c2db7-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="c2db7-112">Example</span></span>

<span data-ttu-id="c2db7-113">`NOT (TRUE)` returnerer **USANN**.</span><span class="sxs-lookup"><span data-stu-id="c2db7-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2db7-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c2db7-114">Additional resources</span></span>

[<span data-ttu-id="c2db7-115">Logiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="c2db7-115">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]