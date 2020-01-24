---
title: Liste over ER-funksjoner i kategorien Dato og klokkeslett
description: Dette emnet inneholder informasjon om dato- og klokkeslettfunksjoner som støttes i elektronisk rapportering (ER).
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
ms.openlocfilehash: fa8e725ac6bd7d280dc0269a70e3f7abf1ad4d43
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916574"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a><span data-ttu-id="ac8b1-103">Liste over ER-funksjoner i kategorien Dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="ac8b1-103">List of ER functions in the Date and time category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac8b1-104">Dato- og klokkeslettfunksjoner for elektronisk rapportering (ER) kan brukes til å trekke ut informasjon fra dato- og klokkeslettverdier, og til å utføre operasjoner på dem.</span><span class="sxs-lookup"><span data-stu-id="ac8b1-104">Electronic reporting (ER) date and time functions can be used to extract information from date and time values, and to perform operations on them.</span></span> <span data-ttu-id="ac8b1-105">Dette emnet inneholder et sammendrag av disse funksjonene.</span><span class="sxs-lookup"><span data-stu-id="ac8b1-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="ac8b1-106">Liste over funksjoner som støttes</span><span class="sxs-lookup"><span data-stu-id="ac8b1-106">List of supported functions</span></span>

| <span data-ttu-id="ac8b1-107">Funksjon</span><span class="sxs-lookup"><span data-stu-id="ac8b1-107">Function</span></span> | <span data-ttu-id="ac8b1-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ac8b1-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ac8b1-109">AddDays</span><span class="sxs-lookup"><span data-stu-id="ac8b1-109">AddDays</span></span>](er-functions-datetime-adddays.md) | <span data-ttu-id="ac8b1-110">Denne funksjonen returnerer en *Datetime*-verdi som er det angitte antallet dager før eller etter en angitt startdato.</span><span class="sxs-lookup"><span data-stu-id="ac8b1-110">This function returns a *DateTime* value that is the specified number of days before or after a specified start date.</span></span> |
| [<span data-ttu-id="ac8b1-111">DateFormat</span><span class="sxs-lookup"><span data-stu-id="ac8b1-111">DateFormat</span></span>](er-functions-datetime-dateformat.md) | <span data-ttu-id="ac8b1-112">Denne funksjonen returnerer en *streng*-verdi som viser en gitt datoverdi som tekst i angitt format og i en valgfri angitt kultur.</span><span class="sxs-lookup"><span data-stu-id="ac8b1-112">This function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="ac8b1-113">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="ac8b1-113">DateTimeFormat</span></span>](er-functions-datetime-datetimeformat.md) | <span data-ttu-id="ac8b1-114">Denne funksjonen returnerer en *streng*-verdi som viser en gitt dato/klokkeslett-verdi som tekst i angitt format og i en valgfri angitt kultur.</span><span class="sxs-lookup"><span data-stu-id="ac8b1-114">This function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="ac8b1-115">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="ac8b1-115">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md) | <span data-ttu-id="ac8b1-116">Denne funksjonen returnerer en *DateTime*-verdi som konverteres fra en gitt tekstverdi i angitt format og i en valgfri angitt kultur til en dato/klokkeslett-verdi.</span><span class="sxs-lookup"><span data-stu-id="ac8b1-116">This function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="ac8b1-117">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="ac8b1-117">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="ac8b1-118">Denne funksjonen returnerer en *Datetime*-verdi som konverteres fra en gitt datoverdi til en dato/klokkeslett-verdi i Coordinated Universal Time (Greenwich middeltid \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="ac8b1-118">This function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="ac8b1-119">DateValue</span><span class="sxs-lookup"><span data-stu-id="ac8b1-119">DateValue</span></span>](er-functions-datetime-datevalue.md) | <span data-ttu-id="ac8b1-120">Denne funksjonen returnerer en *Date*-verdi som konverteres fra en gitt tekstverdi i angitt format og i en valgfri angitt kultur til en dato/klokkeslett-verdi.</span><span class="sxs-lookup"><span data-stu-id="ac8b1-120">This function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified culture to a date value.</span></span> |
| [<span data-ttu-id="ac8b1-121">DayOfYear</span><span class="sxs-lookup"><span data-stu-id="ac8b1-121">DayOfYear</span></span>](er-functions-datetime-dayofyear.md) | <span data-ttu-id="ac8b1-122">Denne funksjonen returnerer en *Heltall*-verdi som representerer antall dager mellom 1. januar og den angitte datoen.</span><span class="sxs-lookup"><span data-stu-id="ac8b1-122">This function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span> |
| [<span data-ttu-id="ac8b1-123">Dager</span><span class="sxs-lookup"><span data-stu-id="ac8b1-123">Days</span></span>](er-functions-datetime-days.md) | <span data-ttu-id="ac8b1-124">Denne funksjonen returnerer en *Heltall*-verdi som representerer antall dager mellom en angitt dato og en annen angitt dato.</span><span class="sxs-lookup"><span data-stu-id="ac8b1-124">This function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span> |
| [<span data-ttu-id="ac8b1-125">Now</span><span class="sxs-lookup"><span data-stu-id="ac8b1-125">Now</span></span>](er-functions-datetime-now.md) | <span data-ttu-id="ac8b1-126">Denne funksjonen returnerer en *Datetime*-verdi som representerer gjeldende dato og klokkeslett for programserveren.</span><span class="sxs-lookup"><span data-stu-id="ac8b1-126">This function returns a *DateTime* value that represents the current application server date and time.</span></span> |
| [<span data-ttu-id="ac8b1-127">NullDate</span><span class="sxs-lookup"><span data-stu-id="ac8b1-127">NullDate</span></span>](er-functions-datetime-nulldate.md) | <span data-ttu-id="ac8b1-128">Denne funksjonen returnerer en *dato*-verdi som representerer **null**-datoen (1. januar 1900).</span><span class="sxs-lookup"><span data-stu-id="ac8b1-128">This function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span> |
| [<span data-ttu-id="ac8b1-129">NullDateTime</span><span class="sxs-lookup"><span data-stu-id="ac8b1-129">NullDateTime</span></span>](er-functions-datetime-nulldatetime.md) | <span data-ttu-id="ac8b1-130">Denne funksjonen returnerer en *DateTime*-verdi som representerer **null** dato/klokkeslett-verdien (1. januar 1900) i Coordinated Universal Time.</span><span class="sxs-lookup"><span data-stu-id="ac8b1-130">This function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time.</span></span> |
| [<span data-ttu-id="ac8b1-131">SessionNow</span><span class="sxs-lookup"><span data-stu-id="ac8b1-131">SessionNow</span></span>](er-functions-datetime-sessionnow.md) | <span data-ttu-id="ac8b1-132">Denne funksjonen returnerer en *Datetime*-verdi som representerer gjeldende dato og klokkeslett for programøkt.</span><span class="sxs-lookup"><span data-stu-id="ac8b1-132">This function returns a *DateTime* value that represents the current application session date and time.</span></span> |
| [<span data-ttu-id="ac8b1-133">SessionToday</span><span class="sxs-lookup"><span data-stu-id="ac8b1-133">SessionToday</span></span>](er-functions-datetime-sessiontoday.md) | <span data-ttu-id="ac8b1-134">Denne funksjonen returnerer en *dato*-verdi som representerer gjeldende dato for programøkt.</span><span class="sxs-lookup"><span data-stu-id="ac8b1-134">This function returns a *Date* value that represents the current application session date.</span></span> |
| [<span data-ttu-id="ac8b1-135">I dag</span><span class="sxs-lookup"><span data-stu-id="ac8b1-135">Today</span></span>](er-functions-datetime-today.md) | <span data-ttu-id="ac8b1-136">Denne funksjonen returnerer en *dato*-verdi som representerer gjeldende dato for programserveren.</span><span class="sxs-lookup"><span data-stu-id="ac8b1-136">This function returns a *Date* value that represents the current application server date.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="ac8b1-137">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ac8b1-137">Additional resources</span></span>

[<span data-ttu-id="ac8b1-138">Oversikt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="ac8b1-138">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="ac8b1-139">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="ac8b1-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="ac8b1-140">Formelspråk i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="ac8b1-140">Electronic reporting formula language</span></span>](er-formula-language.md)
