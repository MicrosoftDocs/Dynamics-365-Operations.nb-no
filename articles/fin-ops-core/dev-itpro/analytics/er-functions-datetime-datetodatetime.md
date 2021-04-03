---
title: DATETODATETIME ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DATETODATETIME.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: d30fdc9c7b6f277b8712b733cabdb0552db2a748
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563588"
---
# <a name="datetodatetime-er-function"></a><span data-ttu-id="f7db2-103">DATETODATETIME ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="f7db2-103">DATETODATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7db2-104">`DATETODATETIME`-funksjonen returnerer en *DateTime*-verdi som konverteres fra en gitt datoverdi til en dato/klokkeslett-verdi i Coordinated Universal Time (Greenwich middeltid \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="f7db2-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="f7db2-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="f7db2-105">Syntax</span></span>

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="f7db2-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="f7db2-106">Arguments</span></span>

<span data-ttu-id="f7db2-107">`date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="f7db2-107">`date`: *Date*</span></span>

<span data-ttu-id="f7db2-108">En datoverdi som representerer datoen som skal konverteres.</span><span class="sxs-lookup"><span data-stu-id="f7db2-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="f7db2-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="f7db2-109">Return values</span></span>

<span data-ttu-id="f7db2-110">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="f7db2-110">*DateTime*</span></span>

<span data-ttu-id="f7db2-111">Den resulterende dato/klokkeslett-verdien.</span><span class="sxs-lookup"><span data-stu-id="f7db2-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="f7db2-112">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="f7db2-112">Example 1</span></span>

<span data-ttu-id="f7db2-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returnerer datoen for gjeldende Microsoft Dynamics 365 Finance-økt, 24. desember 2015, som **12/24/2015 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="f7db2-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="f7db2-114">I dette eksemplet er **CompInfo** en ER-datakilde av typen **Finance and Operations/tabell** og refererer til CompanyInfo-tabellen.</span><span class="sxs-lookup"><span data-stu-id="f7db2-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="f7db2-115">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="f7db2-115">Example 2</span></span>

<span data-ttu-id="f7db2-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returnerer dato/klokkeslett-verdien **11/12/2019 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="f7db2-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7db2-117">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f7db2-117">Additional resources</span></span>

[<span data-ttu-id="f7db2-118">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="f7db2-118">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]