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
ms.openlocfilehash: 0b04ee246d4c28e934407ccb92d792692cc4347d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301656"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="c2446-104">Importere historiske data for behovsprognoser</span><span class="sxs-lookup"><span data-stu-id="c2446-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2446-105">For å garantere nøyaktigheten til behovsprognoser må du ha så mange historiske behovsdata som du kan få per vare eller varetildelingsnøkkel.</span><span class="sxs-lookup"><span data-stu-id="c2446-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="c2446-106">Hvis de historiske behovsdataene ikke allerede er importert, bruker du dataenheten **Historisk eksternt behov** (ReqDemPlanHistoricalExternalDemandEntity) i Dynamics 365 Supply Chain Management til å importere de.</span><span class="sxs-lookup"><span data-stu-id="c2446-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="c2446-107">I arbeidsområdet **Databehandling** kan du se en oversikt over alle feltene i enheten.</span><span class="sxs-lookup"><span data-stu-id="c2446-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="c2446-108">Åpne arbeidsområdet **Databehandling**.</span><span class="sxs-lookup"><span data-stu-id="c2446-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="c2446-109">Velg flisen **Dataenheter**.</span><span class="sxs-lookup"><span data-stu-id="c2446-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="c2446-110">Søk i enhetslisten etter **Historisk eksternt behov**.</span><span class="sxs-lookup"><span data-stu-id="c2446-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="c2446-111">Velg **Målfelt**.</span><span class="sxs-lookup"><span data-stu-id="c2446-111">Select **Target fields**.</span></span> <span data-ttu-id="c2446-112">Feltene nedenfor er obligatoriske: område (**DeliveringSiteId**), dato (**DemandDate**), antall (**DemandQuantity**), og enten varenummer (**ItemNumber**) eller varefordelingsnøkkel (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="c2446-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="c2446-113">Hvis du vil bruke dataenheten, må du ha en Microsoft Excel-fil eller CSV-fil (kommadelte verdier) som inneholder de historiske behovsdataene.</span><span class="sxs-lookup"><span data-stu-id="c2446-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="c2446-114">Følgende eksempel viser hvordan du importerer data fra en CSV-fil.</span><span class="sxs-lookup"><span data-stu-id="c2446-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="c2446-115">Hvis du vil ha mer informasjon om hvordan du importerer data, inkludert hvordan du rydder opp data etter import, kan du se [Oversikt over dataimport- og -eksportjobber](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) og de beslektede emnene.</span><span class="sxs-lookup"><span data-stu-id="c2446-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

<span data-ttu-id="c2446-116">Se også [Generer en statistisk basislinjeprognose](generate-statistical-baseline-forecast.md).</span><span class="sxs-lookup"><span data-stu-id="c2446-116">See also [Generate a statistical baseline forecast](generate-statistical-baseline-forecast.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]