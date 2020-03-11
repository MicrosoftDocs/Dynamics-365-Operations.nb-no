---
title: ADDDAYS ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ADDDAYS.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 08b9727fb34210fecff31826cc1f2b8da022156b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042464"
---
# <span data-ttu-id="85f0f-103"><a name="ADDDAYS">ADDDAYS ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="85f0f-103"><a name="ADDDAYS">ADDDAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85f0f-104">`ADDDAYS`-funksjonen returnerer en *DateTime*-verdi som er det angitte antallet dager før eller etter en angitt startdato.</span><span class="sxs-lookup"><span data-stu-id="85f0f-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="85f0f-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="85f0f-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="85f0f-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="85f0f-106">Arguments</span></span>

<span data-ttu-id="85f0f-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="85f0f-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="85f0f-108">En dato/klokkeslett-verdi som representerer startdatoen.</span><span class="sxs-lookup"><span data-stu-id="85f0f-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="85f0f-109">`days`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="85f0f-109">`days`: *Integer*</span></span>

<span data-ttu-id="85f0f-110">Antall dager før eller etter `datetime`.</span><span class="sxs-lookup"><span data-stu-id="85f0f-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="85f0f-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="85f0f-111">Return values</span></span>

<span data-ttu-id="85f0f-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="85f0f-112">*DateTime*</span></span>

<span data-ttu-id="85f0f-113">Den resulterende dato/klokkeslett-verdien.</span><span class="sxs-lookup"><span data-stu-id="85f0f-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="85f0f-114">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="85f0f-114">Usage notes</span></span>

<span data-ttu-id="85f0f-115">En positiv verdi for `days` gir en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="85f0f-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="85f0f-116">En negativ verdi gir en tidligere dato.</span><span class="sxs-lookup"><span data-stu-id="85f0f-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="85f0f-117">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="85f0f-117">Example 1</span></span>

<span data-ttu-id="85f0f-118">`ADDDAYS (NOW(), 7)` returnerer datoen og klokkeslettet sju dager i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="85f0f-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="85f0f-119">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="85f0f-119">Example 2</span></span>

<span data-ttu-id="85f0f-120">`ADDDAYS (NOW(), -3)` returnerer datoen og klokkeslettet tre dager tidligere.</span><span class="sxs-lookup"><span data-stu-id="85f0f-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="85f0f-121">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="85f0f-121">Additional resources</span></span>

[<span data-ttu-id="85f0f-122">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="85f0f-122">Date and time functions</span></span>](er-functions-category-datetime.md)
