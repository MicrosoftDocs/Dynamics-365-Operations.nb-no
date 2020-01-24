---
title: SESSIONNOW ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen SESSIONNOW.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 4dff6daa8fbd60ef1fc84d783e428d69477aac6d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916275"
---
# <span data-ttu-id="c592a-103"><a name="">SESSIONNOW ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="c592a-103"><a name="">SESSIONNOW ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c592a-104">`SESSIONNOW`-funksjonen returnerer en *DateTime*-verdi som representerer gjeldende dato og klokkeslett for programøkt.</span><span class="sxs-lookup"><span data-stu-id="c592a-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="c592a-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="c592a-105">Syntax</span></span>

```
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="c592a-106">Returverdier</span><span class="sxs-lookup"><span data-stu-id="c592a-106">Return values</span></span>

<span data-ttu-id="c592a-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="c592a-107">*DateTime*</span></span>

<span data-ttu-id="c592a-108">Den resulterende dato/klokkeslett-verdien.</span><span class="sxs-lookup"><span data-stu-id="c592a-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="c592a-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="c592a-109">Example</span></span>

<span data-ttu-id="c592a-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returnerer gjeldende dato/klokkeslett-verdi for programøkt, 24. desember 2015, som **"24.12.2015"**, basert på den valgte tyske kulturen og det angitte formatet.</span><span class="sxs-lookup"><span data-stu-id="c592a-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c592a-111">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c592a-111">Additional resources</span></span>

[<span data-ttu-id="c592a-112">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="c592a-112">Date and time functions</span></span>](er-functions-category-datetime.md)
