---
title: Importere historiske data for behovsprognoser
description: For å få nøyaktige behovsprognoser, trenger du historiske behovsdata per vare eller varetildelingsnøkkel. Dette emnet forklarer hvordan du bruker dataenheter til å importere historiske behovsdata fra alle systemer, slik at du har en lengre logg over behovsprognosedata.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9bb3c178a698bdcd46e7c596247360ba9233b398
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816490"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="205c4-104">Importere historiske data for behovsprognoser</span><span class="sxs-lookup"><span data-stu-id="205c4-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="205c4-105">For å garantere nøyaktigheten til behovsprognoser må du ha så mange historiske behovsdata som du kan få per vare eller varetildelingsnøkkel.</span><span class="sxs-lookup"><span data-stu-id="205c4-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="205c4-106">Hvis de historiske behovsdataene ikke allerede er importert, bruker du dataenheten **Historisk eksternt behov** (ReqDemPlanHistoricalExternalDemandEntity) i Dynamics 365 Supply Chain Management til å importere de.</span><span class="sxs-lookup"><span data-stu-id="205c4-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="205c4-107">I arbeidsområdet **Databehandling** kan du se en oversikt over alle feltene i enheten.</span><span class="sxs-lookup"><span data-stu-id="205c4-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="205c4-108">Åpne arbeidsområdet **Databehandling**.</span><span class="sxs-lookup"><span data-stu-id="205c4-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="205c4-109">Velg flisen **Dataenheter**.</span><span class="sxs-lookup"><span data-stu-id="205c4-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="205c4-110">Søk i enhetslisten etter **Historisk eksternt behov**.</span><span class="sxs-lookup"><span data-stu-id="205c4-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="205c4-111">Velg **Målfelt**.</span><span class="sxs-lookup"><span data-stu-id="205c4-111">Select **Target fields**.</span></span> <span data-ttu-id="205c4-112">Feltene nedenfor er obligatoriske: område (**DeliveringSiteId**), dato (**DemandDate**), antall (**DemandQuantity**), og enten varenummer (**ItemNumber**) eller varefordelingsnøkkel (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="205c4-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="205c4-113">Hvis du vil bruke dataenheten, må du ha en Microsoft Excel-fil eller CSV-fil (kommadelte verdier) som inneholder de historiske behovsdataene.</span><span class="sxs-lookup"><span data-stu-id="205c4-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="205c4-114">Følgende eksempel viser hvordan du importerer data fra en CSV-fil.</span><span class="sxs-lookup"><span data-stu-id="205c4-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="205c4-115">Hvis du vil ha mer informasjon om hvordan du importerer data, inkludert hvordan du rydder opp data etter import, kan du se [Oversikt over dataimport- og -eksportjobber](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) og de beslektede emnene.</span><span class="sxs-lookup"><span data-stu-id="205c4-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

## <a name="example"></a><span data-ttu-id="205c4-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="205c4-116">Example</span></span>

<span data-ttu-id="205c4-117">Du kan bruke følgende fil som et eksempel.</span><span class="sxs-lookup"><span data-stu-id="205c4-117">You can use the following file as an example.</span></span> <span data-ttu-id="205c4-118">Last ned [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/).</span><span class="sxs-lookup"><span data-stu-id="205c4-118">Download the [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/).</span></span> <span data-ttu-id="205c4-119">Denne filen inneholder historiske behovsdata for vare D0001.</span><span class="sxs-lookup"><span data-stu-id="205c4-119">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="205c4-120">Den inneholder bare følgende obligatoriske felter: område, antall og behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="205c4-120">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="205c4-121">Velg firmaet du vil importere de historiske behovsdataene til.</span><span class="sxs-lookup"><span data-stu-id="205c4-121">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="205c4-122">Åpne arbeidsområdet **Databehandling**.</span><span class="sxs-lookup"><span data-stu-id="205c4-122">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="205c4-123">Velg **Import**-flisen.</span><span class="sxs-lookup"><span data-stu-id="205c4-123">Select the **Import** tile.</span></span>
4. <span data-ttu-id="205c4-124">Angi et navn for importprosjektet, for eksempel **Importer historiske behovsdata for vare D0001**.</span><span class="sxs-lookup"><span data-stu-id="205c4-124">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="205c4-125">I feltet **Kildedataformat** velger du filformatet for filen du importerer.</span><span class="sxs-lookup"><span data-stu-id="205c4-125">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="205c4-126">Hvis du vil importere filen HistoricalDemandData i dette eksemplet, velger du **CSV**.</span><span class="sxs-lookup"><span data-stu-id="205c4-126">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="205c4-127">I feltet **Enhetsnavn** velger du **Historisk eksternt behov**.</span><span class="sxs-lookup"><span data-stu-id="205c4-127">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="205c4-128">Lagre filen på datamaskinen, og last den deretter opp.</span><span class="sxs-lookup"><span data-stu-id="205c4-128">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="205c4-129">Velg **Import**.</span><span class="sxs-lookup"><span data-stu-id="205c4-129">Select **Import**.</span></span>
9. <span data-ttu-id="205c4-130">Siden **Utførelsessammendrag** åpnes automatisk.</span><span class="sxs-lookup"><span data-stu-id="205c4-130">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="205c4-131">Kontroller de importerte dataene på siden.</span><span class="sxs-lookup"><span data-stu-id="205c4-131">Verify the imported data on the page.</span></span>

<span data-ttu-id="205c4-132">Når du har importert de historiske behovsdataene, kan du generere en behovsprognose.</span><span class="sxs-lookup"><span data-stu-id="205c4-132">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="205c4-133">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="205c4-133">Additional resources</span></span>

[<span data-ttu-id="205c4-134">Generere en statistisk basislinjeprognose</span><span class="sxs-lookup"><span data-stu-id="205c4-134">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)  
[<span data-ttu-id="205c4-135">Oversikt over dataimport- og -eksportjobber</span><span class="sxs-lookup"><span data-stu-id="205c4-135">Data import and export jobs overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]