---
title: Rapportdefinisjoner i Utforming av finansrapport
description: "Denne artikkelen gir informasjon om rapportdefinisjoner. En rapportdefinisjon er en rapportkomponent (eller byggeblokk) som bruker en raddefinisjon, kolonnedefinisjon og valgfri rapporteringstredefinisjon for å opprette en rapport. En rapportdefinisjon inneholder også alternativer og innstillinger for å tilpasse en rapport."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 322f1cca32053224e1cd6dbaf29c098b983b5e1f
ms.contentlocale: nb-no
ms.lasthandoff: 08/13/2018

---

# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="6f9a9-105">Rapportdefinisjoner i Utforming av finansrapport</span><span class="sxs-lookup"><span data-stu-id="6f9a9-105">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f9a9-106">Denne artikkelen gir informasjon om rapportdefinisjoner.</span><span class="sxs-lookup"><span data-stu-id="6f9a9-106">This article provides information about report definitions.</span></span> <span data-ttu-id="6f9a9-107">En rapportdefinisjon er en rapportkomponent (eller byggeblokk) som bruker en raddefinisjon, kolonnedefinisjon og valgfri rapporteringstredefinisjon for å opprette en rapport.</span><span class="sxs-lookup"><span data-stu-id="6f9a9-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="6f9a9-108">En rapportdefinisjon inneholder også alternativer og innstillinger for å tilpasse en rapport.</span><span class="sxs-lookup"><span data-stu-id="6f9a9-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="6f9a9-109">En rapportdefinisjon er en rapportkomponent (eller byggeblokk) som bruker en raddefinisjon, kolonnedefinisjon og valgfri rapporteringstredefinisjon for å opprette en rapport.</span><span class="sxs-lookup"><span data-stu-id="6f9a9-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="6f9a9-110">En rapportdefinisjon inneholder også flere alternativer og innstillinger for å tilpasse en rapport.</span><span class="sxs-lookup"><span data-stu-id="6f9a9-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="6f9a9-111">Når du har definert raddefinisjoner og kolonnedefinisjoner, må du kombinere dem i en rapportdefinisjon.</span><span class="sxs-lookup"><span data-stu-id="6f9a9-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="6f9a9-112">Nå kan du også definere andre deler av definisjonene, for eksempel detaljnivået og rapportdatoen.</span><span class="sxs-lookup"><span data-stu-id="6f9a9-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="6f9a9-113">Du kan deretter lagre og generere en rapport.</span><span class="sxs-lookup"><span data-stu-id="6f9a9-113">You can then save and generate a report.</span></span> <span data-ttu-id="6f9a9-114">Finansrapportering tilbyr følgende detaljnivåer for rapportering:</span><span class="sxs-lookup"><span data-stu-id="6f9a9-114">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="6f9a9-115">Økonomisk</span><span class="sxs-lookup"><span data-stu-id="6f9a9-115">Financial</span></span>
- <span data-ttu-id="6f9a9-116">Økonomisk og konto</span><span class="sxs-lookup"><span data-stu-id="6f9a9-116">Financial and Account</span></span>
- <span data-ttu-id="6f9a9-117">Økonomisk, konto og transaksjon</span><span class="sxs-lookup"><span data-stu-id="6f9a9-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="6f9a9-118">Det kan imidlertid hende at transaksjonsdetaljer ikke er tilgjengelig i rapporter, avhengig av hvordan dataene er lagret i Microsoft Dynamics ERP-systemet.</span><span class="sxs-lookup"><span data-stu-id="6f9a9-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="6f9a9-119">Opprette en rapportdefinisjon</span><span class="sxs-lookup"><span data-stu-id="6f9a9-119">Create a report definition</span></span>
1. <span data-ttu-id="6f9a9-120">Gå til **Fil** -menyen i Rapportutforming og klikk **Ny**, og velg deretter **Rapportdefinisjon**.</span><span class="sxs-lookup"><span data-stu-id="6f9a9-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="6f9a9-121">Angi riktig informasjon i kategoriene **Rapport**, **Utdata og distribusjon**, **Topptekst og bunntekst** og **Innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="6f9a9-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="6f9a9-122">Innholdet i en rapportdefinisjon</span><span class="sxs-lookup"><span data-stu-id="6f9a9-122">Contents of a report definition</span></span>
<span data-ttu-id="6f9a9-123">Tabellen nedenfor beskriver kategoriene i en rapportdefinisjon og hvordan informasjonen brukes.</span><span class="sxs-lookup"><span data-stu-id="6f9a9-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6f9a9-124">Tabulator</span><span class="sxs-lookup"><span data-stu-id="6f9a9-124">Tab</span></span></th>
<th><span data-ttu-id="6f9a9-125">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6f9a9-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f9a9-126">Rapporter</span><span class="sxs-lookup"><span data-stu-id="6f9a9-126">Report</span></span></td>
<td><span data-ttu-id="6f9a9-127">Opprett en rapport, konfigurer en rapport eller endre en eksisterende rapport.</span><span class="sxs-lookup"><span data-stu-id="6f9a9-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f9a9-128">Utdata og distribusjon</span><span class="sxs-lookup"><span data-stu-id="6f9a9-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="6f9a9-129">Endre utdatatype og mål for rapporten.</span><span class="sxs-lookup"><span data-stu-id="6f9a9-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f9a9-130">Topptekst og bunntekst</span><span class="sxs-lookup"><span data-stu-id="6f9a9-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="6f9a9-131">Definer og formater topptekst og bunntekst for rapporten.</span><span class="sxs-lookup"><span data-stu-id="6f9a9-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="6f9a9-132">Du kan for eksempel legge til tekst eller bilder i toppteksten eller bunnteksten.</span><span class="sxs-lookup"><span data-stu-id="6f9a9-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="6f9a9-133">Finansrapportering støtter BMP-, JPG- og PNG-filer for bilder.</span><span class="sxs-lookup"><span data-stu-id="6f9a9-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="6f9a9-134">Du kan også legge til autotekstkoder for å sette inn tilleggsinformasjon, for eksempel et firmanavn, rapportnavn eller sidetall.</span><span class="sxs-lookup"><span data-stu-id="6f9a9-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f9a9-135">Innstillinger</span><span class="sxs-lookup"><span data-stu-id="6f9a9-135">Settings</span></span></td>
<td><span data-ttu-id="6f9a9-136">Angi innstillinger for rapportdefinisjon, for eksempel følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="6f9a9-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="6f9a9-137">Formatering og avrundingsbeløp</span><span class="sxs-lookup"><span data-stu-id="6f9a9-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="6f9a9-138">Formater detaljrapporter</span><span class="sxs-lookup"><span data-stu-id="6f9a9-138">Format detail reports</span></span></li>
<li><span data-ttu-id="6f9a9-139">Formater rapporteringtrær</span><span class="sxs-lookup"><span data-stu-id="6f9a9-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="6f9a9-140">Generer unntaksrapport</span><span class="sxs-lookup"><span data-stu-id="6f9a9-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="6f9a9-141">Angi valutaomregning</span><span class="sxs-lookup"><span data-stu-id="6f9a9-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="6f9a9-142">Delsum- og filterkontodetaljer</span><span class="sxs-lookup"><span data-stu-id="6f9a9-142">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="6f9a9-143">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6f9a9-143">Additional resources</span></span>

[<span data-ttu-id="6f9a9-144">Finansrapportering</span><span class="sxs-lookup"><span data-stu-id="6f9a9-144">Financial reporting</span></span>](financial-reporting-intro.md)

