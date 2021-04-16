---
title: Rapportdefinisjoner i Utforming av finansrapport
description: Denne artikkelen gir informasjon om rapportdefinisjoner.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 52322453328814b06bacefb4829bb10bf9953186
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755450"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="72e37-103">Rapportdefinisjoner i Utforming av finansrapport</span><span class="sxs-lookup"><span data-stu-id="72e37-103">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72e37-104">Denne artikkelen gir informasjon om rapportdefinisjoner.</span><span class="sxs-lookup"><span data-stu-id="72e37-104">This article provides information about report definitions.</span></span> <span data-ttu-id="72e37-105">En rapportdefinisjon er en rapportkomponent (eller byggeblokk) som bruker en raddefinisjon, kolonnedefinisjon og valgfri rapporteringstredefinisjon for å opprette en rapport.</span><span class="sxs-lookup"><span data-stu-id="72e37-105">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="72e37-106">En rapportdefinisjon inneholder også alternativer og innstillinger for å tilpasse en rapport.</span><span class="sxs-lookup"><span data-stu-id="72e37-106">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="72e37-107">En rapportdefinisjon er en rapportkomponent (eller byggeblokk) som bruker en raddefinisjon, kolonnedefinisjon og valgfri rapporteringstredefinisjon for å opprette en rapport.</span><span class="sxs-lookup"><span data-stu-id="72e37-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="72e37-108">En rapportdefinisjon inneholder også flere alternativer og innstillinger for å tilpasse en rapport.</span><span class="sxs-lookup"><span data-stu-id="72e37-108">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="72e37-109">Når du har definert raddefinisjoner og kolonnedefinisjoner, må du kombinere dem i en rapportdefinisjon.</span><span class="sxs-lookup"><span data-stu-id="72e37-109">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="72e37-110">Nå kan du også definere andre deler av definisjonene, for eksempel detaljnivået og rapportdatoen.</span><span class="sxs-lookup"><span data-stu-id="72e37-110">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="72e37-111">Du kan deretter lagre og generere en rapport.</span><span class="sxs-lookup"><span data-stu-id="72e37-111">You can then save and generate a report.</span></span> <span data-ttu-id="72e37-112">Finansrapportering tilbyr følgende detaljnivåer for rapportering:</span><span class="sxs-lookup"><span data-stu-id="72e37-112">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="72e37-113">Økonomisk</span><span class="sxs-lookup"><span data-stu-id="72e37-113">Financial</span></span>
- <span data-ttu-id="72e37-114">Økonomisk og konto</span><span class="sxs-lookup"><span data-stu-id="72e37-114">Financial and Account</span></span>
- <span data-ttu-id="72e37-115">Økonomisk, konto og transaksjon</span><span class="sxs-lookup"><span data-stu-id="72e37-115">Financial, Account, and Transaction</span></span>

<span data-ttu-id="72e37-116">Alt etter hvordan data er lagret i Microsoft Dynamics ERP-systemet, kan det hende at transaksjonsdetaljer ikke er tilgjengelige i rapporter.</span><span class="sxs-lookup"><span data-stu-id="72e37-116">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="72e37-117">Opprette en rapportdefinisjon</span><span class="sxs-lookup"><span data-stu-id="72e37-117">Create a report definition</span></span>
1. <span data-ttu-id="72e37-118">Gå til **Fil** -menyen i Rapportutforming og klikk **Ny**, og velg deretter **Rapportdefinisjon**.</span><span class="sxs-lookup"><span data-stu-id="72e37-118">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="72e37-119">Angi riktig informasjon i fanene **Rapport**, **Utdata og distribusjon**, **Topptekst og bunntekst** og **Innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="72e37-119">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="72e37-120">Innholdet i en rapportdefinisjon</span><span class="sxs-lookup"><span data-stu-id="72e37-120">Contents of a report definition</span></span>
<span data-ttu-id="72e37-121">Tabellen nedenfor beskriver fanene i en rapportdefinisjon og hvordan informasjonen brukes.</span><span class="sxs-lookup"><span data-stu-id="72e37-121">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="72e37-122">Tabulator</span><span class="sxs-lookup"><span data-stu-id="72e37-122">Tab</span></span></th>
<th><span data-ttu-id="72e37-123">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="72e37-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72e37-124">Rapporter</span><span class="sxs-lookup"><span data-stu-id="72e37-124">Report</span></span></td>
<td><span data-ttu-id="72e37-125">Opprett en rapport, konfigurer en rapport eller endre en eksisterende rapport.</span><span class="sxs-lookup"><span data-stu-id="72e37-125">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e37-126">Utdata og distribusjon</span><span class="sxs-lookup"><span data-stu-id="72e37-126">Output and Distribution</span></span></td>
<td><span data-ttu-id="72e37-127">Endre utdatatype og mål for rapporten.</span><span class="sxs-lookup"><span data-stu-id="72e37-127">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e37-128">Topptekst og bunntekst</span><span class="sxs-lookup"><span data-stu-id="72e37-128">Headers and Footers</span></span></td>
<td><span data-ttu-id="72e37-129">Definer og formater topptekst og bunntekst for rapporten.</span><span class="sxs-lookup"><span data-stu-id="72e37-129">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="72e37-130">Du kan for eksempel legge til tekst eller bilder i toppteksten eller bunnteksten.</span><span class="sxs-lookup"><span data-stu-id="72e37-130">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="72e37-131">Finansrapportering støtter BMP-, JPG- og PNG-filer for bilder.</span><span class="sxs-lookup"><span data-stu-id="72e37-131">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="72e37-132">Du kan også legge til autotekstkoder for å sette inn tilleggsinformasjon, for eksempel et firmanavn, rapportnavn eller sidetall.</span><span class="sxs-lookup"><span data-stu-id="72e37-132">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72e37-133">Innstillinger</span><span class="sxs-lookup"><span data-stu-id="72e37-133">Settings</span></span></td>
<td><span data-ttu-id="72e37-134">Angi innstillinger for rapportdefinisjon, for eksempel følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="72e37-134">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="72e37-135">Formatering og avrundingsbeløp</span><span class="sxs-lookup"><span data-stu-id="72e37-135">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="72e37-136">Formater detaljrapporter</span><span class="sxs-lookup"><span data-stu-id="72e37-136">Format detail reports</span></span></li>
<li><span data-ttu-id="72e37-137">Formater rapporteringtrær</span><span class="sxs-lookup"><span data-stu-id="72e37-137">Format reporting trees</span></span></li>
<li><span data-ttu-id="72e37-138">Generer unntaksrapport</span><span class="sxs-lookup"><span data-stu-id="72e37-138">Generate an exception report</span></span></li>
<li><span data-ttu-id="72e37-139">Angi valutaomregning</span><span class="sxs-lookup"><span data-stu-id="72e37-139">Specify currency conversion</span></span></li>
<li><span data-ttu-id="72e37-140">Delsum- og filterkontodetaljer</span><span class="sxs-lookup"><span data-stu-id="72e37-140">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="72e37-141">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="72e37-141">Additional resources</span></span>

[<span data-ttu-id="72e37-142">Finansrapportering</span><span class="sxs-lookup"><span data-stu-id="72e37-142">Financial reporting</span></span>](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]