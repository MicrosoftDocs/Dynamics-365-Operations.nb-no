---
title: NOW ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NOW
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: c93aa2a0e3f6aa07ab9e843d3c5f11c5265e8c40
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746873"
---
# <a name="now-er-function"></a><span data-ttu-id="fa506-103">NOW ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="fa506-103">NOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa506-104">`NOW`-funksjonen returnerer en *DateTime*-verdi som representerer gjeldende dato og klokkeslett for programserveren.</span><span class="sxs-lookup"><span data-stu-id="fa506-104">The `NOW` function returns a *DateTime* value that represents the current application server date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa506-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="fa506-105">Syntax</span></span>

```vb
NOW ()
```

## <a name="return-values"></a><span data-ttu-id="fa506-106">Returverdier</span><span class="sxs-lookup"><span data-stu-id="fa506-106">Return values</span></span>

<span data-ttu-id="fa506-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="fa506-107">*DateTime*</span></span>

<span data-ttu-id="fa506-108">Den resulterende dato/klokkeslett-verdien.</span><span class="sxs-lookup"><span data-stu-id="fa506-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="fa506-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fa506-109">Example</span></span>

<span data-ttu-id="fa506-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returnerer gjeldende dato/klokkeslett-verdi for programserveren, 24. desember 2015, som **"24-12-2015"**, basert på det angitte egendefinerte formatet.</span><span class="sxs-lookup"><span data-stu-id="fa506-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fa506-111">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="fa506-111">Additional resources</span></span>

[<span data-ttu-id="fa506-112">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="fa506-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]