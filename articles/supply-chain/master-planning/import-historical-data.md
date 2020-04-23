---
title: Importere historiske data for behovsprognoser
description: For å få nøyaktige behovsprognoser, trenger du historiske behovsdata per vare eller varetildelingsnøkkel. Dette emnet forklarer hvordan du bruker dataenheter til å importere historiske behovsdata fra alle systemer, slik at du har en lengre logg over behovsprognosedata.
author: roxanadiaconu
manager: tfehr
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97e84b478b8fd65313d8c3be5c9a50756d8b4924
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213852"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="01b4f-104">Importere historiske data for behovsprognoser</span><span class="sxs-lookup"><span data-stu-id="01b4f-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01b4f-105">For å garantere nøyaktigheten til behovsprognoser må du ha så mange historiske behovsdata som du kan få per vare eller varetildelingsnøkkel.</span><span class="sxs-lookup"><span data-stu-id="01b4f-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="01b4f-106">Hvis de historiske behovsdataene ikke allerede er importert, bruker du dataenheten **Historisk eksternt behov** (ReqDemPlanHistoricalExternalDemandEntity) i Dynamics 365 Supply Chain Management til å importere de.</span><span class="sxs-lookup"><span data-stu-id="01b4f-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="01b4f-107">I arbeidsområdet **Databehandling** kan du se en oversikt over alle feltene i enheten.</span><span class="sxs-lookup"><span data-stu-id="01b4f-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="01b4f-108">Åpne arbeidsområdet **Databehandling**.</span><span class="sxs-lookup"><span data-stu-id="01b4f-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="01b4f-109">Klikk flisen **Dataenheter**.</span><span class="sxs-lookup"><span data-stu-id="01b4f-109">Click the **Data entities** tile.</span></span>
3. <span data-ttu-id="01b4f-110">Søk i enhetslisten etter **Historisk eksternt behov**.</span><span class="sxs-lookup"><span data-stu-id="01b4f-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="01b4f-111">Klikk **Målfelt**.</span><span class="sxs-lookup"><span data-stu-id="01b4f-111">Click **Target fields**.</span></span> <span data-ttu-id="01b4f-112">Feltene nedenfor er obligatoriske: område (**DeliveringSiteId**), dato (**DemandDate**), antall (**DemandQuantity**), og enten varenummer (**ItemNumber**) eller varefordelingsnøkkel (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="01b4f-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="01b4f-113">Hvis du vil bruke dataenheten, må du ha en Microsoft Excel-fil eller CSV-fil (kommadelte verdier) som inneholder de historiske behovsdataene.</span><span class="sxs-lookup"><span data-stu-id="01b4f-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="01b4f-114">Følgende eksempel viser hvordan du importerer data fra en CSV-fil.</span><span class="sxs-lookup"><span data-stu-id="01b4f-114">The following example shows how to import the data from a CSV file.</span></span>

## <a name="example"></a><span data-ttu-id="01b4f-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="01b4f-115">Example</span></span>

<span data-ttu-id="01b4f-116">Du kan bruke følgende fil som et eksempel.</span><span class="sxs-lookup"><span data-stu-id="01b4f-116">You can use the following file as an example.</span></span> <span data-ttu-id="01b4f-117">Last ned [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span><span class="sxs-lookup"><span data-stu-id="01b4f-117">Download the [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span></span> <span data-ttu-id="01b4f-118">Denne filen inneholder historiske behovsdata for vare D0001.</span><span class="sxs-lookup"><span data-stu-id="01b4f-118">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="01b4f-119">Den inneholder bare følgende obligatoriske felter: område, antall og behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="01b4f-119">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="01b4f-120">Velg firmaet du vil importere de historiske behovsdataene til.</span><span class="sxs-lookup"><span data-stu-id="01b4f-120">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="01b4f-121">Åpne arbeidsområdet **Databehandling**.</span><span class="sxs-lookup"><span data-stu-id="01b4f-121">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="01b4f-122">Klikk flisen **Importer**.</span><span class="sxs-lookup"><span data-stu-id="01b4f-122">Click the **Import** tile.</span></span>
4. <span data-ttu-id="01b4f-123">Angi et navn for importprosjektet, for eksempel **Importer historiske behovsdata for vare D0001**.</span><span class="sxs-lookup"><span data-stu-id="01b4f-123">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="01b4f-124">I feltet **Kildedataformat** velger du filformatet for filen du importerer.</span><span class="sxs-lookup"><span data-stu-id="01b4f-124">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="01b4f-125">Hvis du vil importere filen HistoricalDemandData i dette eksemplet, velger du **CSV**.</span><span class="sxs-lookup"><span data-stu-id="01b4f-125">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="01b4f-126">I feltet **Enhetsnavn** velger du **Historisk eksternt behov**.</span><span class="sxs-lookup"><span data-stu-id="01b4f-126">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="01b4f-127">Lagre filen på datamaskinen, og last den deretter opp.</span><span class="sxs-lookup"><span data-stu-id="01b4f-127">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="01b4f-128">Klikk **Importer**.</span><span class="sxs-lookup"><span data-stu-id="01b4f-128">Click **Import**.</span></span>
9. <span data-ttu-id="01b4f-129">Siden **Utførelsessammendrag** åpnes automatisk.</span><span class="sxs-lookup"><span data-stu-id="01b4f-129">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="01b4f-130">Kontroller de importerte dataene på siden.</span><span class="sxs-lookup"><span data-stu-id="01b4f-130">Verify the imported data on the page.</span></span>

<span data-ttu-id="01b4f-131">Når du har importert de historiske behovsdataene, kan du generere en behovsprognose.</span><span class="sxs-lookup"><span data-stu-id="01b4f-131">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01b4f-132">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="01b4f-132">Additional resources</span></span>

[<span data-ttu-id="01b4f-133">Generere en statistisk basislinjeprognose</span><span class="sxs-lookup"><span data-stu-id="01b4f-133">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)
