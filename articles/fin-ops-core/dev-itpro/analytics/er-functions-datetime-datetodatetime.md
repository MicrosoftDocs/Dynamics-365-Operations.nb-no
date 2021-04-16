---
title: DATETODATETIME ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DATETODATETIME.
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
ms.openlocfilehash: bb90c58544eeba804cd39542cc70fab3b840af80
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746969"
---
# <a name="datetodatetime-er-function"></a><span data-ttu-id="2834a-103">DATETODATETIME ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="2834a-103">DATETODATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2834a-104">`DATETODATETIME`-funksjonen returnerer en *DateTime*-verdi som konverteres fra en gitt datoverdi til en dato/klokkeslett-verdi i Coordinated Universal Time (Greenwich middeltid \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="2834a-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="2834a-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="2834a-105">Syntax</span></span>

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="2834a-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="2834a-106">Arguments</span></span>

<span data-ttu-id="2834a-107">`date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="2834a-107">`date`: *Date*</span></span>

<span data-ttu-id="2834a-108">En datoverdi som representerer datoen som skal konverteres.</span><span class="sxs-lookup"><span data-stu-id="2834a-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="2834a-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="2834a-109">Return values</span></span>

<span data-ttu-id="2834a-110">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="2834a-110">*DateTime*</span></span>

<span data-ttu-id="2834a-111">Den resulterende dato/klokkeslett-verdien.</span><span class="sxs-lookup"><span data-stu-id="2834a-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="2834a-112">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="2834a-112">Example 1</span></span>

<span data-ttu-id="2834a-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returnerer datoen for gjeldende Microsoft Dynamics 365 Finance-økt, 24. desember 2015, som **12/24/2015 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="2834a-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="2834a-114">I dette eksemplet er **CompInfo** en ER-datakilde av typen **Finance and Operations/tabell** og refererer til CompanyInfo-tabellen.</span><span class="sxs-lookup"><span data-stu-id="2834a-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="2834a-115">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="2834a-115">Example 2</span></span>

<span data-ttu-id="2834a-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returnerer dato/klokkeslett-verdien **11/12/2019 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="2834a-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2834a-117">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="2834a-117">Additional resources</span></span>

[<span data-ttu-id="2834a-118">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="2834a-118">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]