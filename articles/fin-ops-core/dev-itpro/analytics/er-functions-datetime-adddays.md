---
title: ADDDAYS ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ADDDAYS.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 85ad6508c0d16796efbf1ad81e25d74365de8f30
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570778"
---
# <a name="adddays-er-function"></a><span data-ttu-id="a87cb-103">ADDDAYS ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="a87cb-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a87cb-104">`ADDDAYS`-funksjonen returnerer en *DateTime*-verdi som er det angitte antallet dager før eller etter en angitt startdato.</span><span class="sxs-lookup"><span data-stu-id="a87cb-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="a87cb-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="a87cb-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="a87cb-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="a87cb-106">Arguments</span></span>

<span data-ttu-id="a87cb-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="a87cb-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="a87cb-108">En dato/klokkeslett-verdi som representerer startdatoen.</span><span class="sxs-lookup"><span data-stu-id="a87cb-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="a87cb-109">`days`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="a87cb-109">`days`: *Integer*</span></span>

<span data-ttu-id="a87cb-110">Antall dager før eller etter `datetime`.</span><span class="sxs-lookup"><span data-stu-id="a87cb-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="a87cb-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="a87cb-111">Return values</span></span>

<span data-ttu-id="a87cb-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="a87cb-112">*DateTime*</span></span>

<span data-ttu-id="a87cb-113">Den resulterende dato/klokkeslett-verdien.</span><span class="sxs-lookup"><span data-stu-id="a87cb-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a87cb-114">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="a87cb-114">Usage notes</span></span>

<span data-ttu-id="a87cb-115">En positiv verdi for `days` gir en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="a87cb-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="a87cb-116">En negativ verdi gir en tidligere dato.</span><span class="sxs-lookup"><span data-stu-id="a87cb-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="a87cb-117">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="a87cb-117">Example 1</span></span>

<span data-ttu-id="a87cb-118">`ADDDAYS (NOW(), 7)` returnerer datoen og klokkeslettet sju dager i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="a87cb-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="a87cb-119">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="a87cb-119">Example 2</span></span>

<span data-ttu-id="a87cb-120">`ADDDAYS (NOW(), -3)` returnerer datoen og klokkeslettet tre dager tidligere.</span><span class="sxs-lookup"><span data-stu-id="a87cb-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a87cb-121">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a87cb-121">Additional resources</span></span>

[<span data-ttu-id="a87cb-122">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="a87cb-122">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]