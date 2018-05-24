---
title: Finansrapportering for Finance og Operations
description: "Finansrapportering for Dynamics 365 for Finance and Operations lar profesjonelle innen finans og forretninger opprette, vedlikeholde, distribuere og vise regnskapsoppgjør. Det beveger seg utover tradisjonelle rapporteringsbegrensninger for å gjøre det enklere for deg å effektivt utforme ulike typer rapporter."
author: aprilolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinanicalReportingSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 68813
ms.assetid: fe8b27e7-a40a-4689-ac6a-7f7401c387f5
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 54a3409e7bd0f1c704cf9f7dd1d860100ec83d7f
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="financial-reporting-for-finance-and-operations"></a><span data-ttu-id="0e4d7-104">Finansrapportering for Finance og Operations</span><span class="sxs-lookup"><span data-stu-id="0e4d7-104">Financial reporting for Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e4d7-105">Finansrapportering for Dynamics 365 for Finance and Operations lar profesjonelle innen finans og forretninger opprette, vedlikeholde, distribuere og vise regnskapsoppgjør.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-105">Financial reporting for Finance and Operations allows financial and business professionals to create, maintain, deploy, and view financial statements.</span></span> <span data-ttu-id="0e4d7-106">Det beveger seg utover tradisjonelle rapporteringsbegrensninger for å gjøre det enklere for deg å effektivt utforme ulike typer rapporter.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-106">It moves beyond traditional reporting constraints to help you efficiently design various types of reports.</span></span>

<span data-ttu-id="0e4d7-107">Finansrapportering inkluderer støtte for dimensjon.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-107">Financial reporting includes dimension support.</span></span> <span data-ttu-id="0e4d7-108">Derfor er kontosegmenter eller dimensjoner tilgjengelig umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-108">Therefore, account segments or dimensions are immediately available.</span></span> <span data-ttu-id="0e4d7-109">Ingen ekstra verktøy eller konfigurasjonstrinn er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-109">No additional tools or configuration steps are required.</span></span>

## <a name="financial-reporting-setup"></a><span data-ttu-id="0e4d7-110">Oppsett for finansrapportering</span><span class="sxs-lookup"><span data-stu-id="0e4d7-110">Financial reporting setup</span></span>
<span data-ttu-id="0e4d7-111">**Oppsett for finansrapportering**-siden inneholder en liste over alle finansdimensjonene i systemet.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-111">The **Financial reporting setup** page has a list of all financial dimensions in the system.</span></span> <span data-ttu-id="0e4d7-112">**Finans** > **Finansoppsett** > **Oppsett for finansrapportering**.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-112">**General ledger** > **Ledger setup** > **Financial reporting setup**.</span></span> 

<span data-ttu-id="0e4d7-113">**Oppsett for finansrapportering**-siden har to deler som fastsetter dataene du rapporterer i Finansrapportering:</span><span class="sxs-lookup"><span data-stu-id="0e4d7-113">The **Financial reporting setup** page has two sections that determine the data you report on in Financial reporting:</span></span>

<span data-ttu-id="0e4d7-114">• **Kategorien Dimensjon** - Siden forskjellige firmaer bruker ulike dimensjoner og kontostrukturer, er det ikke mulig å bestemme rekkefølgen som brukere vil vise alle finansdimensjoner i rapporter.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-114">•   **Dimensions tab** - Because different companies use different dimensions and account structures, there is no way to determine the order in which users want to view all financial dimensions on reports.</span></span> <span data-ttu-id="0e4d7-115">På denne siden kan du angi rekkefølgen du vil finansdimensjonene skal vises når du bygger og viser en rapport i Finansrapportering.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-115">This page allows you set the order in which you want financial dimensions to appear when you build and view a report in Financial reporting.</span></span>

<span data-ttu-id="0e4d7-116">• **Kategorien Attributter** er der du kan velge om du vil ha muligheten til å bruke **Leverandører** og **Kunder** som attributter for filtrering og rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-116">•   **Attributes tab** is where you can select whether you want the ability to use **Vendors** and **Customers** as attributes for filtering and report design.</span></span> <span data-ttu-id="0e4d7-117">Rapportering av leverandør og kunde vil bare være nyttig hvis du ikke angir flere leverandører eller kunder i ett bilag ved postering av transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-117">Reporting on Vendor and Customer will only be valuable if you do not enter multiple vendors or customers in a single voucher when posting transactions.</span></span> <span data-ttu-id="0e4d7-118">Hvis du velger leverandør og/eller kunde, legges det til ekstra tid i integreringen.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-118">Choosing Vendor and/or Customer will add additional time to the integration.</span></span>



## <a name="financial-reporting-components"></a><span data-ttu-id="0e4d7-119">Komponenter for finansrapportering</span><span class="sxs-lookup"><span data-stu-id="0e4d7-119">Financial reporting components</span></span>
<span data-ttu-id="0e4d7-120">Finansrapporteringskomponentene nedenfor gjør det enkelt å opprette, vise og planlegge rapporter.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-120">The following components of financial reporting make it easy to create, view, and schedule reports.</span></span>

| <span data-ttu-id="0e4d7-121">Komponent</span><span class="sxs-lookup"><span data-stu-id="0e4d7-121">Component</span></span>        | <span data-ttu-id="0e4d7-122">Funksjoner</span><span class="sxs-lookup"><span data-stu-id="0e4d7-122">Functions</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="0e4d7-123">Tilleggsinformasjon</span><span class="sxs-lookup"><span data-stu-id="0e4d7-123">Additional information</span></span>                                                                          |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e4d7-124">Rapportutforming</span><span class="sxs-lookup"><span data-stu-id="0e4d7-124">Report Designer</span></span>  | <span data-ttu-id="0e4d7-125">Opprett rapportbyggeblokker som kan kombineres for å definere og generere en rapport.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-125">Create report building blocks that can be combined to define and generate a report.</span></span> <span data-ttu-id="0e4d7-126">Rapportveiviseren veileder mindre erfarne brukere gjennom utformingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-126">The report wizard guides less experienced users through the design process.</span></span> <span data-ttu-id="0e4d7-127">Avanserte brukere kan opprette nye rapportbyggeblokker eller endre eksisterende byggeblokker for å oppfylle sine behov.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-127">Advanced users can create new report building blocks or modify existing building blocks to meet their requirements.</span></span> |                                                                                                 |
| <span data-ttu-id="0e4d7-128">Rapporttidsplaner</span><span class="sxs-lookup"><span data-stu-id="0e4d7-128">Report schedules</span></span> | <span data-ttu-id="0e4d7-129">Planlegge én enkelt rapport eller en gruppe rapporter, slik at de blir generert med jevne mellomrom.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-129">Schedule a single report or a group of reports so that it is generated on a regular basis.</span></span>                                                                                                                                                                                          | [<span data-ttu-id="0e4d7-130">Generere en finansrapport</span><span class="sxs-lookup"><span data-stu-id="0e4d7-130">Generate a financial report</span></span>](generate-financial-report.md) |

## <a name="features"></a><span data-ttu-id="0e4d7-131">Funksjoner</span><span class="sxs-lookup"><span data-stu-id="0e4d7-131">Features</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0e4d7-132">Funksjon</span><span class="sxs-lookup"><span data-stu-id="0e4d7-132">Feature</span></span></th>
<th><span data-ttu-id="0e4d7-133">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0e4d7-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0e4d7-134">Fleksibel rapportutforming</span><span class="sxs-lookup"><span data-stu-id="0e4d7-134">Report design flexibility</span></span></td>
<td><span data-ttu-id="0e4d7-135">Rapportutforming inneholder følgende rapporteringsalternativer når du utformer en rapport:</span><span class="sxs-lookup"><span data-stu-id="0e4d7-135">Report Designer provides the following reporting options when you design a report:</span></span>
<ul>
<li><span data-ttu-id="0e4d7-136">Lagre dimensjonskombinasjoner og gjenbruke dimensjoner for flere rapporter.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-136">Save dimension combinations, and reuse the dimensions for multiple reports.</span></span></li>
<li><span data-ttu-id="0e4d7-137">Styre hvordan dimensjonsbeskrivelser er formatert og vises.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-137">Control how dimension descriptions are formatted and displayed.</span></span></li>
<li><span data-ttu-id="0e4d7-138">Identifiser kontoer eller dimensjoner som er utelatt fra rapportbyggeblokker.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-138">Identify accounts or dimensions that have been omitted from report building blocks.</span></span></li>
<li><span data-ttu-id="0e4d7-139">Formatere overskrifter rullende prognoser.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-139">Format headers for rolling forecasts.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e4d7-140">Finansrapportsamarbeid</span><span class="sxs-lookup"><span data-stu-id="0e4d7-140">Financial report collaboration</span></span></td>
<td><span data-ttu-id="0e4d7-141">Følgende funksjoner lar deg administrere generering og distribusjon av rapporter:</span><span class="sxs-lookup"><span data-stu-id="0e4d7-141">The following features help you manage the generation and distribution of reports:</span></span>
<ul>
<li><span data-ttu-id="0e4d7-142">Planlegge rapporter slik at de automatisk å genereres daglig, ukentlig, månedlig eller årlig.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-142">Schedule reports so that they are automatically generated on a daily, weekly, monthly, or annual basis.</span></span></li>
<li><span data-ttu-id="0e4d7-143">Eksportere til det skrivebeskyttede XPS-formatet, som gir bedre dokumentsikkerhet ved hjelp av digitale signaturer.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-143">Export to the read-only XPS format, which provides better document security through digital signatures.</span></span></li>
<li><span data-ttu-id="0e4d7-144">Eksportere til et Microsoft Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-144">Export to a Microsoft Excel worksheet.</span></span></li>
<li><span data-ttu-id="0e4d7-145">Hvis du vil dele rapporter, kan du opprette e-postmeldinger som inneholder koblinger til rapportene.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-145">To share reports, you can create email messages that contain links to the reports.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e4d7-146">Vise interaktiv rapport</span><span class="sxs-lookup"><span data-stu-id="0e4d7-146">Interactive report viewing</span></span></td>
<td><span data-ttu-id="0e4d7-147">Interaktive funksjoner lar deg utføre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="0e4d7-147">Interactive features let you perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="0e4d7-148">Endre rapportdatoen for rapporten som du viser.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-148">Change the report date for the report that you&#39;re viewing.</span></span></li>
<li><span data-ttu-id="0e4d7-149">Endre valutaen for rapporten som du viser.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-149">Change the currency of the report that you&#39;re viewing.</span></span></li>
<li><span data-ttu-id="0e4d7-150">Vis rapporten i et sammendrag eller en detaljert visning.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-150">View the report in either a summary view or a detailed view.</span></span></li>
<li><span data-ttu-id="0e4d7-151">Legg til dimensjonsfiltre for å begrense rapportinnholdet til en bestemt dimensjon eller en kombinasjon av dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-151">Add dimension filters to limit the report content to a specific dimension or combination of dimensions.</span></span></li>
<li><span data-ttu-id="0e4d7-152">Legg til attributtfiltre for å begrense rapportinnholdet til et bestemt attributt en kombinasjon av attributter.</span><span class="sxs-lookup"><span data-stu-id="0e4d7-152">Add attribute filters to limit the report content to a specific attribute or combination of attributes.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="0e4d7-153">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0e4d7-153">Additional resources</span></span>
[<span data-ttu-id="0e4d7-154">Generere en finansrapport</span><span class="sxs-lookup"><span data-stu-id="0e4d7-154">Generate a financial report</span></span>](generate-financial-report.md)





