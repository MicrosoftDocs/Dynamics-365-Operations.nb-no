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
ms.openlocfilehash: 2aa3d5e34e6dcd9b5d4a3fe3f21d7e3285adbcad
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745423"
---
# <a name="sessiontoday-er-function"></a><span data-ttu-id="991f2-103">SESSIONTODAY ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="991f2-103">SESSIONTODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="991f2-104">`SESSIONTODAY`-funksjonen returnerer en *dato*-verdi som representerer gjeldende dato for programøkt.</span><span class="sxs-lookup"><span data-stu-id="991f2-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="991f2-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="991f2-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="991f2-106">Returverdier</span><span class="sxs-lookup"><span data-stu-id="991f2-106">Return values</span></span>

<span data-ttu-id="991f2-107">*Dato*</span><span class="sxs-lookup"><span data-stu-id="991f2-107">*Date*</span></span>

<span data-ttu-id="991f2-108">Den resulterende datoverdien.</span><span class="sxs-lookup"><span data-stu-id="991f2-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="991f2-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="991f2-109">Example</span></span>

<span data-ttu-id="991f2-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returnerer gjeldende programøktdato, 24. desember 2015, som strengen **"24-12-2015"**, basert på den valgte tyske kulturen og det angitte formatet.</span><span class="sxs-lookup"><span data-stu-id="991f2-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="991f2-111">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="991f2-111">Additional resources</span></span>

[<span data-ttu-id="991f2-112">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="991f2-112">Date and time functions</span></span>](er-functions-category-datetime.md)
