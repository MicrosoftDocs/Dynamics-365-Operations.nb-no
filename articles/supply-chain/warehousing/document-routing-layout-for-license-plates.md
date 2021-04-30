---
title: Dokumentrutingsoppsett for nummerskiltetiketter
description: Dette emnet beskriver hvordan du kan bruke formateringsmetoder til å skrive ut verdier på etiketter.
author: perlynne
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 6b5bf6815f225dcca8f9e89e2c85942ce8a2ccd7
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907993"
---
# <a name="document-routing-layout-for-license-plate-labels"></a><span data-ttu-id="1f1d0-103">Dokumentrutingsoppsett for nummerskiltetiketter</span><span class="sxs-lookup"><span data-stu-id="1f1d0-103">Document routing layout for license plate labels</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1f1d0-104">Dokumentrutingsoppsettet definerer oppsettet til nummerskiltetiketter og dataene som skrives ut på dem.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-104">The document routing layout defines the layout of license plate labels, and the data that is printed on them.</span></span> <span data-ttu-id="1f1d0-105">Du konfigurerer utløsingspunkt for utskrift når du definerer menyelementer og arbeidsmaler for mobilenheter.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-105">You configure the printing trigger points when you set up mobile device menu items and work templates.</span></span>

<span data-ttu-id="1f1d0-106">I et typisk scenario vil mottaksassistenter på lageret skrive ut nummerskiltetiketter umiddelbart etter at de har registrert innholdet på paller som ankommer mottaksområdet.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-106">In a typical scenario, warehouse receiving clerks print license plate labels immediately after they record the contents of pallets that arrive in the receiving area.</span></span> <span data-ttu-id="1f1d0-107">De fysiske etikettene brukes på pallene.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-107">The physical labels are applied to the pallets.</span></span> <span data-ttu-id="1f1d0-108">De kan deretter brukes til validering som en del av plasseringsprosessen som følger, og fremtidige utgående plukkoperasjoner.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-108">They can then be used for validation as part of the put-away process that follows and future outbound picking operations.</span></span>

<span data-ttu-id="1f1d0-109">Du kan skrive ut svært komplekse etiketter, forutsatt at utskriftsenheten kan tolke teksten som sendes til den.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-109">You can print highly complex labels, provided that the printing device can interpret the text that is sent to it.</span></span> <span data-ttu-id="1f1d0-110">Et ZPL-oppsett (Zebra Programming Language) som inneholder en strekkode, kan for eksempel ligne på følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-110">For example, a Zebra Programming Language (ZPL) layout that includes a bar code might resemble the following example.</span></span>

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

<span data-ttu-id="1f1d0-111">Som en del av etikettutskriftsprosessen vil teksten `$LicensePlateId$` i dette eksemplet erstattes med en dataverdi.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-111">As part of the label printing process, the text `$LicensePlateId$` in this example will be replaced with a data value.</span></span>

<span data-ttu-id="1f1d0-112">Hvis du vil se hvilke verdier som blir skrevet ut, går du til **Lagerstyring \> Forespørsler og rapporter \> Nummerskiltetiketter**.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-112">To see the values that will be printed, go to **Warehouse management \> Inquiries and reports \> License plate labels**.</span></span>

<span data-ttu-id="1f1d0-113">Flere generelt tilgjengelige verktøy for etikettgenerering kan hjelpe deg med å formatere teksten for etikettoppsettet.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-113">Several widely available label generation tools can help you format the text for the label layout.</span></span> <span data-ttu-id="1f1d0-114">Mange av disse verktøyene støtter formatet `$FieldName$`.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-114">Many of these tools support the `$FieldName$` format.</span></span> <span data-ttu-id="1f1d0-115">I tillegg bruker Microsoft Dynamics 365 Supply Chain Management en spesiell formateringslogikk som en del av felttilordningen for dokumentrutingsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-115">In addition, Microsoft Dynamics 365 Supply Chain Management uses special formatting logic as part of the field mapping for the document routing layout.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="1f1d0-116">Aktivere denne funksjonen for systemet</span><span class="sxs-lookup"><span data-stu-id="1f1d0-116">Turn on this feature for your system</span></span>

<span data-ttu-id="1f1d0-117">Hvis systemet ikke allerede inneholder funksjonene som er beskrevet i dette emnet, kan du gå til [Funksjonsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funksjonen *Forbedrede oppsett for nummerskiltetikett*.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Enhanced license plate label layouts* feature.</span></span>

## <a name="custom-number-formats"></a><span data-ttu-id="1f1d0-118">Egendefinerte tallformater</span><span class="sxs-lookup"><span data-stu-id="1f1d0-118">Custom number formats</span></span>

<span data-ttu-id="1f1d0-119">Du kan tilpasse formateringen av numeriske feltverdier som skrives ut ved å bruke koder som har følgende format.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-119">You can customize the formatting of numerical field values that are printed by using codes that have the following format.</span></span>

```dos
$FieldName:FormatString$
```

<span data-ttu-id="1f1d0-120">Her er en forklaring på dette formatet:</span><span class="sxs-lookup"><span data-stu-id="1f1d0-120">Here is an explanation of this format:</span></span>

- <span data-ttu-id="1f1d0-121">`FieldName` er navnet på datafeltet (for eksempel **Antall**).</span><span class="sxs-lookup"><span data-stu-id="1f1d0-121">`FieldName` is the name of the data field (such as **Qty**).</span></span>
- <span data-ttu-id="1f1d0-122">`FormatString` definerer hvordan dataene må skrives ut.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-122">`FormatString` defines how the data must be printed.</span></span>

<span data-ttu-id="1f1d0-123">Eksemplene nedenfor viser hvordan du kan tilpasse feltet for arbeidsantall (**Antall**):</span><span class="sxs-lookup"><span data-stu-id="1f1d0-123">The following examples show how you can customize the work quantity (**Qty**) field:</span></span>

- <span data-ttu-id="1f1d0-124">Hvis du alltid vil vise fire sifre (ved å bruke nuller som plassholdere), bruker du `$Qty:0000$`.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-124">To always show four digits (by using zeros as placeholders), use `$Qty:0000$`.</span></span> <span data-ttu-id="1f1d0-125">Hvis for eksempel antallet er 10, vil etiketten vise "0010".</span><span class="sxs-lookup"><span data-stu-id="1f1d0-125">For example, if the quantity is 10, the label will show "0010."</span></span>
- <span data-ttu-id="1f1d0-126">Hvis du alltid vil vise to desimaler, bruker du `$Qty:0.00$`.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-126">To always show two decimal places, use `$Qty:0.00$`.</span></span> <span data-ttu-id="1f1d0-127">Hvis for eksempel antallet er 10, vil etiketten vise "10,00".</span><span class="sxs-lookup"><span data-stu-id="1f1d0-127">For example, if the quantity is 10, the label will show "10.00."</span></span>

<span data-ttu-id="1f1d0-128">Hvis du vil ha en fullstendig liste over de tilgjengelige tallformatstrengene, kan du se [Egendefinerte tallformatstrenger](/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="1f1d0-128">For a complete list of the available number format strings, see [Custom numeric format strings](/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="custom-string-formats"></a><span data-ttu-id="1f1d0-129">Egendefinerte strengformater</span><span class="sxs-lookup"><span data-stu-id="1f1d0-129">Custom string formats</span></span>

<span data-ttu-id="1f1d0-130">Du kan fjerne de første tegnene i en streng ved å bruke følgende felt og formatkode.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-130">You can remove the first characters of a string by using the following field and format code.</span></span>

```dos
$FieldName:#..$
```

<span data-ttu-id="1f1d0-131">Her angir `#` hvor mange tegn det skal hoppes over.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-131">Here, `#` specifies the number of characters to skip.</span></span> <span data-ttu-id="1f1d0-132">Hvis du for eksempel vil skrive ut et SSCC-skiltnummer (Serial Shipping Container Code) som ikke inkluderer de to første tegnene, bruker du `$LicensePlateId:2..$`.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-132">For example, to print a Serial Shipping Container Code (SSCC) license plate number that doesn't include the first two characters, use `$LicensePlateId:2..$`.</span></span> <span data-ttu-id="1f1d0-133">I dette tilfellet vil skiltnummeret 0011111111111222221 skrives ut som 11111111111222221.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-133">In this case, the license plate number 0011111111111222221 will be printed as "11111111111222221."</span></span>

## <a name="custom-datetime-formats"></a><span data-ttu-id="1f1d0-134">Egen definerte dato- og klokkeslettformater</span><span class="sxs-lookup"><span data-stu-id="1f1d0-134">Custom date/time formats</span></span>

<span data-ttu-id="1f1d0-135">Følgende eksempel viser hvordan du kan styre formatet som brukes til å skrive ut datoer.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-135">The following example shows how you can control the format that is used to print dates.</span></span>

```dos
$PrintedDate:dd-MM-yyyy$
```

<span data-ttu-id="1f1d0-136">I dette eksemplet vil datoen 30. april 2020 skrives ut som "30-04-2020".</span><span class="sxs-lookup"><span data-stu-id="1f1d0-136">In this example, the date April 30, 2020, will be printed as "30-04-2020."</span></span>

<span data-ttu-id="1f1d0-137">Hvis du vil ha en fullstendig liste over de tilgjengelige dato- og klokkeslettformatene, kan du se [Egendefinerte formatstrenger for dato/klokkeslett](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="1f1d0-137">For a complete list of the available date/time formats, see [Custom date and time format strings](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="print-individual-lines-from-multiline-data"></a><span data-ttu-id="1f1d0-138">Skrive ut enkeltlinjer fra flerlinjedata</span><span class="sxs-lookup"><span data-stu-id="1f1d0-138">Print individual lines from multiline data</span></span>

<span data-ttu-id="1f1d0-139">Hvis et datafelt inneholder flere linjer (det vil si linjer som er atskilt med linjeskift), kan du skrive ut en enkelt linje ved hjelp av følgende format.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-139">If a data field contains multiple lines (that is, lines that are separated by line breaks), you can print an individual line by using the following format.</span></span>

```dos
$FieldName[#]$
```

<span data-ttu-id="1f1d0-140">Her er `#` linjenummeret du vil skrive ut.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-140">Here, `#` is the line number that you want to print.</span></span> <span data-ttu-id="1f1d0-141">(Bruk 1 for den første linjen.)</span><span class="sxs-lookup"><span data-stu-id="1f1d0-141">(Use 1 for the first line.)</span></span>

<span data-ttu-id="1f1d0-142">Systemet har for eksempel et `AdditionalAddress`-felt som lagrer følgende adresse med flere linjer:</span><span class="sxs-lookup"><span data-stu-id="1f1d0-142">For example, your system has an `AdditionalAddress` field that stores the following multiline address:</span></span>

<span data-ttu-id="1f1d0-143">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-143">Contoso Inc.</span></span>  
<span data-ttu-id="1f1d0-144">123 Gatenavn</span><span class="sxs-lookup"><span data-stu-id="1f1d0-144">123 Street Name</span></span>  
<span data-ttu-id="1f1d0-145">By, Stat</span><span class="sxs-lookup"><span data-stu-id="1f1d0-145">Some City, Some State</span></span>

<span data-ttu-id="1f1d0-146">Du kan skrive ut denne adressen, én linje om gangen, ved hjelp av følgende koder.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-146">You can print this address, one line at a time, by using the following codes.</span></span>

| <span data-ttu-id="1f1d0-147">Kode</span><span class="sxs-lookup"><span data-stu-id="1f1d0-147">Code</span></span> | <span data-ttu-id="1f1d0-148">Tekst som skrives ut</span><span class="sxs-lookup"><span data-stu-id="1f1d0-148">Text that is printed</span></span> |
|---|---|
| `$AdditionalAddress[1]$` | <span data-ttu-id="1f1d0-149">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-149">Contoso Inc.</span></span> |
| `$AdditionalAddress[2]$` | <span data-ttu-id="1f1d0-150">123 Gatenavn</span><span class="sxs-lookup"><span data-stu-id="1f1d0-150">123 Street Name</span></span> |
| `$AdditionalAddress[3]$` | <span data-ttu-id="1f1d0-151">By, Stat</span><span class="sxs-lookup"><span data-stu-id="1f1d0-151">Some City, Some State</span></span> |

## <a name="print-and-format-from-a-display-method"></a><span data-ttu-id="1f1d0-152">Skrive ut og formatere fra en visningsmetode</span><span class="sxs-lookup"><span data-stu-id="1f1d0-152">Print and format from a display method</span></span>

<span data-ttu-id="1f1d0-153">Du kan skrive ut fra en visningsmetode ved å bruke følgende format.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-153">You can print from a display method by using the following format.</span></span>

```dos
$DisplayMethod()$
```

<span data-ttu-id="1f1d0-154">Du kan kombinere dette formatet med andre typer som ble beskrevet tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-154">You can combine this format with other types that were described earlier in this topic.</span></span> <span data-ttu-id="1f1d0-155">Du kan for eksempel ha en visningsmetode kalt `DisplayListOfItemsNumbers()`, og du kan skrive ut det første varenummeret for denne metoden.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-155">For example, you have a display method that is named `DisplayListOfItemsNumbers()`, and you want to print the first item number of this method.</span></span> <span data-ttu-id="1f1d0-156">I dette tilfellet kan du bruke følgende kode.</span><span class="sxs-lookup"><span data-stu-id="1f1d0-156">In this case, you can use the following code.</span></span>

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a><span data-ttu-id="1f1d0-157">Mer informasjon om hvordan du skriver ut etiketter</span><span class="sxs-lookup"><span data-stu-id="1f1d0-157">More information about how to print labels</span></span>

<span data-ttu-id="1f1d0-158">Hvis du vil ha mer informasjon om hvordan du definerer og skriver ut etiketter, kan du se [Aktivere utskrift av nummerskiltetikett](tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="1f1d0-158">For more information about how to set up and print labels, see [Enable license plate label printing](tasks/license-plate-label-printing.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]