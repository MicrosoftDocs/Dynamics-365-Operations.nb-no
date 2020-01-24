---
title: SESSIONTODAY ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen SESSIONTODAY.
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
ms.openlocfilehash: bcfb36d6e3fb8475546f7cfb420c4aca848ac896
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917471"
---
# <span data-ttu-id="b5788-103"><a name="SESSIONTODAY">SESSIONTODAY ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="b5788-103"><a name="SESSIONTODAY">SESSIONTODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5788-104">`SESSIONTODAY`-funksjonen returnerer en *dato*-verdi som representerer gjeldende dato for programøkt.</span><span class="sxs-lookup"><span data-stu-id="b5788-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5788-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="b5788-105">Syntax</span></span>

```
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="b5788-106">Returverdier</span><span class="sxs-lookup"><span data-stu-id="b5788-106">Return values</span></span>

<span data-ttu-id="b5788-107">*Dato*</span><span class="sxs-lookup"><span data-stu-id="b5788-107">*Date*</span></span>

<span data-ttu-id="b5788-108">Den resulterende datoverdien.</span><span class="sxs-lookup"><span data-stu-id="b5788-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="b5788-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="b5788-109">Example</span></span>

<span data-ttu-id="b5788-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returnerer gjeldende programøktdato, 24. desember 2015, som strengen **"24-12-2015"**, basert på den valgte tyske kulturen og det angitte formatet.</span><span class="sxs-lookup"><span data-stu-id="b5788-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5788-111">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b5788-111">Additional resources</span></span>

[<span data-ttu-id="b5788-112">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="b5788-112">Date and time functions</span></span>](er-functions-category-datetime.md)
