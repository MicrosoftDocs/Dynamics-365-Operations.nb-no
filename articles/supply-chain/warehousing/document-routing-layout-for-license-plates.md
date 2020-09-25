---
title: Dokumentrutingsoppsett for nummerskiltetiketter
description: Dette emnet beskriver hvordan du kan bruke formateringsmetoder til å skrive ut verdier på etiketter.
author: perlynne
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 9af077022ab0759534d2c1da5f39997712e6a354
ms.sourcegitcommit: 965fa733be068dc37f482d02ebbcd77f2c3d0a45
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/03/2020
ms.locfileid: "3763461"
---
# <a name="document-routing-layout-for-license-plate-labels"></a><span data-ttu-id="5e320-103">Dokumentrutingsoppsett for nummerskiltetiketter</span><span class="sxs-lookup"><span data-stu-id="5e320-103">Document routing layout for license plate labels</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e320-104">Dokumentrutingsoppsettet definerer oppsettet til nummerskiltetiketter og dataene som skrives ut på dem.</span><span class="sxs-lookup"><span data-stu-id="5e320-104">The document routing layout defines the layout of license plate labels, and the data that is printed on them.</span></span> <span data-ttu-id="5e320-105">Du konfigurerer utløsingspunkt for utskrift når du definerer menyelementer og arbeidsmaler for mobilenheter.</span><span class="sxs-lookup"><span data-stu-id="5e320-105">You configure the printing trigger points when you set up mobile device menu items and work templates.</span></span>

<span data-ttu-id="5e320-106">I et typisk scenario vil mottaksassistenter på lageret skrive ut nummerskiltetiketter umiddelbart etter at de har registrert innholdet på paller som ankommer mottaksområdet.</span><span class="sxs-lookup"><span data-stu-id="5e320-106">In a typical scenario, warehouse receiving clerks print license plate labels immediately after they record the contents of pallets that arrive in the receiving area.</span></span> <span data-ttu-id="5e320-107">De fysiske etikettene brukes på pallene.</span><span class="sxs-lookup"><span data-stu-id="5e320-107">The physical labels are applied to the pallets.</span></span> <span data-ttu-id="5e320-108">De kan deretter brukes til validering som en del av plasseringsprosessen som følger, og fremtidige utgående plukkoperasjoner.</span><span class="sxs-lookup"><span data-stu-id="5e320-108">They can then be used for validation as part of the put-away process that follows and future outbound picking operations.</span></span>

<span data-ttu-id="5e320-109">Du kan skrive ut svært komplekse etiketter, forutsatt at utskriftsenheten kan tolke teksten som sendes til den.</span><span class="sxs-lookup"><span data-stu-id="5e320-109">You can print highly complex labels, provided that the printing device can interpret the text that is sent to it.</span></span> <span data-ttu-id="5e320-110">Et ZPL-oppsett (Zebra Programming Language) som inneholder en strekkode, kan for eksempel ligne på følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="5e320-110">For example, a Zebra Programming Language (ZPL) layout that includes a bar code might resemble the following example.</span></span>

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

<span data-ttu-id="5e320-111">Som en del av etikettutskriftsprosessen vil teksten `$LicensePlateId$` i dette eksemplet erstattes med en dataverdi.</span><span class="sxs-lookup"><span data-stu-id="5e320-111">As part of the label printing process, the text `$LicensePlateId$` in this example will be replaced with a data value.</span></span>

<span data-ttu-id="5e320-112">Hvis du vil se hvilke verdier som blir skrevet ut, går du til **Lagerstyring \> Forespørsler og rapporter \> Nummerskiltetiketter**.</span><span class="sxs-lookup"><span data-stu-id="5e320-112">To see the values that will be printed, go to **Warehouse management \> Inquiries and reports \> License plate labels**.</span></span>

<span data-ttu-id="5e320-113">Flere generelt tilgjengelige verktøy for etikettgenerering kan hjelpe deg med å formatere teksten for etikettoppsettet.</span><span class="sxs-lookup"><span data-stu-id="5e320-113">Several widely available label generation tools can help you format the text for the label layout.</span></span> <span data-ttu-id="5e320-114">Mange av disse verktøyene støtter formatet `$FieldName$`.</span><span class="sxs-lookup"><span data-stu-id="5e320-114">Many of these tools support the `$FieldName$` format.</span></span> <span data-ttu-id="5e320-115">I tillegg bruker Microsoft Dynamics 365 Supply Chain Management en spesiell formateringslogikk som en del av felttilordningen for dokumentrutingsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="5e320-115">In addition, Microsoft Dynamics 365 Supply Chain Management uses special formatting logic as part of the field mapping for the document routing layout.</span></span>

## <a name="custom-number-formats"></a><span data-ttu-id="5e320-116">Egendefinerte tallformater</span><span class="sxs-lookup"><span data-stu-id="5e320-116">Custom number formats</span></span>

<span data-ttu-id="5e320-117">Du kan tilpasse formateringen av numeriske feltverdier som skrives ut ved å bruke koder som har følgende format.</span><span class="sxs-lookup"><span data-stu-id="5e320-117">You can customize the formatting of numerical field values that are printed by using codes that have the following format.</span></span>

```dos
$FieldName:FormatString$
```

<span data-ttu-id="5e320-118">Her er en forklaring på dette formatet:</span><span class="sxs-lookup"><span data-stu-id="5e320-118">Here is an explanation of this format:</span></span>

- <span data-ttu-id="5e320-119">`FieldName` er navnet på datafeltet (for eksempel **Antall**).</span><span class="sxs-lookup"><span data-stu-id="5e320-119">`FieldName` is the name of the data field (such as **Qty**).</span></span>
- <span data-ttu-id="5e320-120">`FormatString` definerer hvordan dataene må skrives ut.</span><span class="sxs-lookup"><span data-stu-id="5e320-120">`FormatString` defines how the data must be printed.</span></span>

<span data-ttu-id="5e320-121">Eksemplene nedenfor viser hvordan du kan tilpasse feltet for arbeidsantall (**Antall**):</span><span class="sxs-lookup"><span data-stu-id="5e320-121">The following examples show how you can customize the work quantity (**Qty**) field:</span></span>

- <span data-ttu-id="5e320-122">Hvis du alltid vil vise fire sifre (ved å bruke nuller som plassholdere), bruker du `$Qty:0000$`.</span><span class="sxs-lookup"><span data-stu-id="5e320-122">To always show four digits (by using zeros as placeholders), use `$Qty:0000$`.</span></span> <span data-ttu-id="5e320-123">Hvis for eksempel antallet er 10, vil etiketten vise "0010".</span><span class="sxs-lookup"><span data-stu-id="5e320-123">For example, if the quantity is 10, the label will show "0010."</span></span>
- <span data-ttu-id="5e320-124">Hvis du alltid vil vise to desimaler, bruker du `$Qty:0.00$`.</span><span class="sxs-lookup"><span data-stu-id="5e320-124">To always show two decimal places, use `$Qty:0.00$`.</span></span> <span data-ttu-id="5e320-125">Hvis for eksempel antallet er 10, vil etiketten vise "10,00".</span><span class="sxs-lookup"><span data-stu-id="5e320-125">For example, if the quantity is 10, the label will show "10.00."</span></span>

<span data-ttu-id="5e320-126">Hvis du vil ha en fullstendig liste over de tilgjengelige tallformatstrengene, kan du se [Egendefinerte tallformatstrenger](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="5e320-126">For a complete list of the available number format strings, see [Custom numeric format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="custom-string-formats"></a><span data-ttu-id="5e320-127">Egendefinerte strengformater</span><span class="sxs-lookup"><span data-stu-id="5e320-127">Custom string formats</span></span>

<span data-ttu-id="5e320-128">Du kan fjerne de første tegnene i en streng ved å bruke følgende felt og formatkode.</span><span class="sxs-lookup"><span data-stu-id="5e320-128">You can remove the first characters of a string by using the following field and format code.</span></span>

```dos
$FieldName:#..$
```

<span data-ttu-id="5e320-129">Her angir `#` hvor mange tegn det skal hoppes over.</span><span class="sxs-lookup"><span data-stu-id="5e320-129">Here, `#` specifies the number of characters to skip.</span></span> <span data-ttu-id="5e320-130">Hvis du for eksempel vil skrive ut et SSCC-skiltnummer (Serial Shipping Container Code) som ikke inkluderer de to første tegnene, bruker du `$LicensePlateId:2..$`.</span><span class="sxs-lookup"><span data-stu-id="5e320-130">For example, to print a Serial Shipping Container Code (SSCC) license plate number that doesn't include the first two characters, use `$LicensePlateId:2..$`.</span></span> <span data-ttu-id="5e320-131">I dette tilfellet vil skiltnummeret 0011111111111222221 skrives ut som 11111111111222221.</span><span class="sxs-lookup"><span data-stu-id="5e320-131">In this case, the license plate number 0011111111111222221 will be printed as "11111111111222221."</span></span>

## <a name="custom-datetime-formats"></a><span data-ttu-id="5e320-132">Egen definerte dato- og klokkeslettformater</span><span class="sxs-lookup"><span data-stu-id="5e320-132">Custom date/time formats</span></span>

<span data-ttu-id="5e320-133">Følgende eksempel viser hvordan du kan styre formatet som brukes til å skrive ut datoer.</span><span class="sxs-lookup"><span data-stu-id="5e320-133">The following example shows how you can control the format that is used to print dates.</span></span>

```dos
$PrintedDate:dd-MM-yyyy$
```

<span data-ttu-id="5e320-134">I dette eksemplet vil datoen 30. april 2020 skrives ut som "30-04-2020".</span><span class="sxs-lookup"><span data-stu-id="5e320-134">In this example, the date April 30, 2020, will be printed as "30-04-2020."</span></span>

<span data-ttu-id="5e320-135">Hvis du vil ha en fullstendig liste over de tilgjengelige dato- og klokkeslettformatene, kan du se [Egendefinerte formatstrenger for dato/klokkeslett](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="5e320-135">For a complete list of the available date/time formats, see [Custom date and time format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="print-individual-lines-from-multiline-data"></a><span data-ttu-id="5e320-136">Skrive ut enkeltlinjer fra flerlinjedata</span><span class="sxs-lookup"><span data-stu-id="5e320-136">Print individual lines from multiline data</span></span>

<span data-ttu-id="5e320-137">Hvis et datafelt inneholder flere linjer (det vil si linjer som er atskilt med linjeskift), kan du skrive ut en enkelt linje ved hjelp av følgende format.</span><span class="sxs-lookup"><span data-stu-id="5e320-137">If a data field contains multiple lines (that is, lines that are separated by line breaks), you can print an individual line by using the following format.</span></span>

```dos
$FieldName[#]$
```

<span data-ttu-id="5e320-138">Her er `#` linjenummeret du vil skrive ut.</span><span class="sxs-lookup"><span data-stu-id="5e320-138">Here, `#` is the line number that you want to print.</span></span> <span data-ttu-id="5e320-139">(Bruk 1 for den første linjen.)</span><span class="sxs-lookup"><span data-stu-id="5e320-139">(Use 1 for the first line.)</span></span>

<span data-ttu-id="5e320-140">Systemet har for eksempel et `AdditionalAddress`-felt som lagrer følgende adresse med flere linjer:</span><span class="sxs-lookup"><span data-stu-id="5e320-140">For example, your system has an `AdditionalAddress` field that stores the following multiline address:</span></span>

<span data-ttu-id="5e320-141">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="5e320-141">Contoso Inc.</span></span>  
<span data-ttu-id="5e320-142">123 Gatenavn</span><span class="sxs-lookup"><span data-stu-id="5e320-142">123 Street Name</span></span>  
<span data-ttu-id="5e320-143">By, Stat</span><span class="sxs-lookup"><span data-stu-id="5e320-143">Some City, Some State</span></span>

<span data-ttu-id="5e320-144">Du kan skrive ut denne adressen, én linje om gangen, ved hjelp av følgende koder.</span><span class="sxs-lookup"><span data-stu-id="5e320-144">You can print this address, one line at a time, by using the following codes.</span></span>

| <span data-ttu-id="5e320-145">Kode</span><span class="sxs-lookup"><span data-stu-id="5e320-145">Code</span></span> | <span data-ttu-id="5e320-146">Tekst som skrives ut</span><span class="sxs-lookup"><span data-stu-id="5e320-146">Text that is printed</span></span> |
|---|---|
| `$AdditionalAddress[1]$` | <span data-ttu-id="5e320-147">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="5e320-147">Contoso Inc.</span></span> |
| `$AdditionalAddress[2]$` | <span data-ttu-id="5e320-148">123 Gatenavn</span><span class="sxs-lookup"><span data-stu-id="5e320-148">123 Street Name</span></span> |
| `$AdditionalAddress[3]$` | <span data-ttu-id="5e320-149">By, Stat</span><span class="sxs-lookup"><span data-stu-id="5e320-149">Some City, Some State</span></span> |

## <a name="print-and-format-from-a-display-method"></a><span data-ttu-id="5e320-150">Skrive ut og formatere fra en visningsmetode</span><span class="sxs-lookup"><span data-stu-id="5e320-150">Print and format from a display method</span></span>

<span data-ttu-id="5e320-151">Du kan skrive ut fra en visningsmetode ved å bruke følgende format.</span><span class="sxs-lookup"><span data-stu-id="5e320-151">You can print from a display method by using the following format.</span></span>

```dos
$DisplayMethod()$
```

<span data-ttu-id="5e320-152">Du kan kombinere dette formatet med andre typer som ble beskrevet tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="5e320-152">You can combine this format with other types that were described earlier in this topic.</span></span> <span data-ttu-id="5e320-153">Du kan for eksempel ha en visningsmetode kalt `DisplayListOfItemsNumbers()`, og du kan skrive ut det første varenummeret for denne metoden.</span><span class="sxs-lookup"><span data-stu-id="5e320-153">For example, you have a display method that is named `DisplayListOfItemsNumbers()`, and you want to print the first item number of this method.</span></span> <span data-ttu-id="5e320-154">I dette tilfellet kan du bruke følgende kode.</span><span class="sxs-lookup"><span data-stu-id="5e320-154">In this case, you can use the following code.</span></span>

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a><span data-ttu-id="5e320-155">Mer informasjon om hvordan du skriver ut etiketter</span><span class="sxs-lookup"><span data-stu-id="5e320-155">More information about how to print labels</span></span>

<span data-ttu-id="5e320-156">Hvis du vil ha mer informasjon om hvordan du definerer og skriver ut etiketter, kan du se [Aktivere utskrift av nummerskiltetikett](tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="5e320-156">For more information about how to set up and print labels, see [Enable license plate label printing](tasks/license-plate-label-printing.md).</span></span>
