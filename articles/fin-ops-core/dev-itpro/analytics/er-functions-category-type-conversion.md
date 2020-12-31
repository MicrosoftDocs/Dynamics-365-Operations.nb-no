---
title: Liste over ER-funksjoner i typekonverteringskategorien
description: Dette emnet inneholder informasjon om konverteringsfunksjonene som støttes i elektronisk rapportering (ER).
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d160c02403bf067ed523fbd634e65c622b522b97
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686081"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="14c24-103">Liste over ER-funksjoner i typekonverteringskategorien</span><span class="sxs-lookup"><span data-stu-id="14c24-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14c24-104">Konverteringsfunksjoner for elektronisk rapportering (ER)-type kan brukes til å konvertere verdier mellom typer.</span><span class="sxs-lookup"><span data-stu-id="14c24-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="14c24-105">Dette emnet inneholder et sammendrag av disse funksjonene.</span><span class="sxs-lookup"><span data-stu-id="14c24-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="14c24-106">Typekonverteringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="14c24-106">Type conversion functions</span></span>

| <span data-ttu-id="14c24-107">Funksjon</span><span class="sxs-lookup"><span data-stu-id="14c24-107">Function</span></span> | <span data-ttu-id="14c24-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="14c24-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="14c24-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="14c24-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="14c24-110">Denne funksjonen returnerer en *Int64*-verdi som representerer den angitte strengen.</span><span class="sxs-lookup"><span data-stu-id="14c24-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="14c24-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="14c24-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="14c24-112">Denne funksjonen returnerer en *Int*-verdi som representerer den angitte strengen.</span><span class="sxs-lookup"><span data-stu-id="14c24-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="14c24-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="14c24-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="14c24-114">Denne funksjonen returnerer en *reell* verdi som er konvertert fra den angitte *streng*-verdien.</span><span class="sxs-lookup"><span data-stu-id="14c24-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="14c24-115">Under konverteringen vurderes de angitte skilletegnene for desimal- og siffergruppering.</span><span class="sxs-lookup"><span data-stu-id="14c24-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="14c24-116">Verdi</span><span class="sxs-lookup"><span data-stu-id="14c24-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="14c24-117">Denne funksjonen returnerer en *reell* verdi som er konvertert fra den angitte *streng*-verdien.</span><span class="sxs-lookup"><span data-stu-id="14c24-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="14c24-118">Typekonverteringsfunksjoner i kategorien Dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="14c24-118">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="14c24-119">Tabellen nedenfor beskriver funksjonene for typekonvertering i kategorien [dato og klokkeslett](er-functions-category-datetime.md).</span><span class="sxs-lookup"><span data-stu-id="14c24-119">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="14c24-120">Funksjon</span><span class="sxs-lookup"><span data-stu-id="14c24-120">Function</span></span> | <span data-ttu-id="14c24-121">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="14c24-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="14c24-122">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="14c24-122">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="14c24-123">Denne funksjonen returnerer en *DateTime*-verdi som konverteres fra en gitt *streng*-verdi i angitt format og i en valgfri angitt kultur til en dato/klokkeslett-verdi.</span><span class="sxs-lookup"><span data-stu-id="14c24-123">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="14c24-124">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="14c24-124">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="14c24-125">Denne funksjonen returnerer en *DateTime*-verdi som konverteres fra en gitt *dato*-verdi til en dato/klokkeslett-verdi i Coordinated Universal Time (Greenwich middeltid \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="14c24-125">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="14c24-126">DateValue</span><span class="sxs-lookup"><span data-stu-id="14c24-126">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="14c24-127">Denne funksjonen returnerer en *dato*-verdi som konverteres fra en gitt *streng*-verdi i angitt format og i en valgfri angitt kultur til en datoverdi.</span><span class="sxs-lookup"><span data-stu-id="14c24-127">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="14c24-128">Typekonverteringsfunksjoner i listekategorien</span><span class="sxs-lookup"><span data-stu-id="14c24-128">Type conversion functions in the list category</span></span>

<span data-ttu-id="14c24-129">Tabellen nedenfor beskriver funksjonene for typekonvertering i [listekategorien](er-functions-category-list.md).</span><span class="sxs-lookup"><span data-stu-id="14c24-129">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="14c24-130">Funksjon</span><span class="sxs-lookup"><span data-stu-id="14c24-130">Function</span></span> | <span data-ttu-id="14c24-131">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="14c24-131">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="14c24-132">Liste</span><span class="sxs-lookup"><span data-stu-id="14c24-132">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="14c24-133">Denne funksjonen returnerer en *Postliste*-verdi som en ny liste som er opprettet fra de angitte argumentene for typen *Container (post)*.</span><span class="sxs-lookup"><span data-stu-id="14c24-133">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="14c24-134">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="14c24-134">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="14c24-135">Denne funksjonen returnerer en *postliste*-verdi som opprettes basert på strukturen til et gitt argument for typen *Opplisting* eller *Container (post)*.</span><span class="sxs-lookup"><span data-stu-id="14c24-135">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="14c24-136">Del</span><span class="sxs-lookup"><span data-stu-id="14c24-136">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="14c24-137">Denne funksjonen deler den angitte *Streng*-verdien inn i delstrenger og returnerer resultatet som en ny *Postliste*-verdi.</span><span class="sxs-lookup"><span data-stu-id="14c24-137">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="14c24-138">StringJoin</span><span class="sxs-lookup"><span data-stu-id="14c24-138">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="14c24-139">Denne funksjonen returnerer en *Streng*-verdi som består av sammenkoblede verdier for det angitte feltet fra den angitte *Postliste*-verdien.</span><span class="sxs-lookup"><span data-stu-id="14c24-139">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="14c24-140">Verdiene kan skilles med det angitte skilletegnet.</span><span class="sxs-lookup"><span data-stu-id="14c24-140">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="14c24-141">Typekonverteringsfunksjoner i tekstkategorien</span><span class="sxs-lookup"><span data-stu-id="14c24-141">Type conversion functions in the text category</span></span>

<span data-ttu-id="14c24-142">Tabellen nedenfor beskriver funksjonene for typekonvertering i [tekstkategorien](er-functions-category-text.md).</span><span class="sxs-lookup"><span data-stu-id="14c24-142">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="14c24-143">Funksjon</span><span class="sxs-lookup"><span data-stu-id="14c24-143">Function</span></span> | <span data-ttu-id="14c24-144">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="14c24-144">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="14c24-145">Char</span><span class="sxs-lookup"><span data-stu-id="14c24-145">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="14c24-146">Denne funksjonen returnerer en *streng*-verdi som representerer et enkelt tegn som det angitte Unicode-nummeret refererer til.</span><span class="sxs-lookup"><span data-stu-id="14c24-146">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="14c24-147">GuidValue</span><span class="sxs-lookup"><span data-stu-id="14c24-147">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="14c24-148">Denne funksjonen konverterer de angitte inndataene for *Streng*-datatypen til et dataelement av *GUID*-typen.</span><span class="sxs-lookup"><span data-stu-id="14c24-148">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="14c24-149">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="14c24-149">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="14c24-150">Denne funksjonen returnerer en *streng*-verdi som representerer det angitte tallet i angitt format og i en valgfri angitt kultur.</span><span class="sxs-lookup"><span data-stu-id="14c24-150">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="14c24-151">QrCode</span><span class="sxs-lookup"><span data-stu-id="14c24-151">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="14c24-152">Denne funksjonen returnerer en *Container*-verdi som presenterer et QR-kodebilde for den angitte strengen i binært format.</span><span class="sxs-lookup"><span data-stu-id="14c24-152">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="14c24-153">Tekst</span><span class="sxs-lookup"><span data-stu-id="14c24-153">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="14c24-154">Denne funksjonen returnerer en *Streng*-verdi som representerer det angitte tallet etter at det er konvertert til en tekststreng som formateres i henhold til de nasjonale innstillingene for serveren for gjeldende forekomst av programmet.</span><span class="sxs-lookup"><span data-stu-id="14c24-154">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="14c24-155">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="14c24-155">Additional resources</span></span>

[<span data-ttu-id="14c24-156">Oversikt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="14c24-156">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="14c24-157">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="14c24-157">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="14c24-158">Formelspråk i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="14c24-158">Electronic reporting formula language</span></span>](er-formula-language.md)
