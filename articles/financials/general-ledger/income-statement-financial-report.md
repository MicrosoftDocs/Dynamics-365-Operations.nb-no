---
title: Finansrapport for resultatregnskap
description: "Denne artikkelen beskriver standardrapporten for inntektsregnskap. Den beskriver også byggeblokker som er knyttet til denne rapporten."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8ca90b949a1a2b5af4a0fd78ddf80d5add2565b9
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="income-statement-financial-report"></a><span data-ttu-id="4c8b0-104">Finansrapport for resultatregnskap</span><span class="sxs-lookup"><span data-stu-id="4c8b0-104">Income statement financial report</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4c8b0-105">Denne artikkelen beskriver standardrapporten for inntektsregnskap.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="4c8b0-106">Den beskriver også byggeblokker som er knyttet til denne rapporten.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="4c8b0-107">Standardrapport for resultatregnskap</span><span class="sxs-lookup"><span data-stu-id="4c8b0-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="4c8b0-108">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="4c8b0-108">Default report</span></span>             | <span data-ttu-id="4c8b0-109">Resultat</span><span class="sxs-lookup"><span data-stu-id="4c8b0-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c8b0-110">Resultatregnskap – Standard</span><span class="sxs-lookup"><span data-stu-id="4c8b0-110">Income Statement – Default</span></span> | <span data-ttu-id="4c8b0-111">Gir en oversikt over organisasjonens lønnsomhet for inneværende periode, og også for hittil i år.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="4c8b0-112">Byggeblokker</span><span class="sxs-lookup"><span data-stu-id="4c8b0-112">Building blocks</span></span>
<span data-ttu-id="4c8b0-113">Finansrapporten for resultatregnskapet bruker byggeblokkene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="4c8b0-114">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="4c8b0-114">Default report</span></span>             | <span data-ttu-id="4c8b0-115">Raddefinisjon</span><span class="sxs-lookup"><span data-stu-id="4c8b0-115">Row definition</span></span>                     | <span data-ttu-id="4c8b0-116">Kolonnedefinisjon</span><span class="sxs-lookup"><span data-stu-id="4c8b0-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="4c8b0-117">Resultatregnskap – Standard</span><span class="sxs-lookup"><span data-stu-id="4c8b0-117">Income Statement - Default</span></span> | <span data-ttu-id="4c8b0-118">Sammendrag for resultatregnskap – Standard</span><span class="sxs-lookup"><span data-stu-id="4c8b0-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="4c8b0-119">Periodisk og hittil i år – Standard</span><span class="sxs-lookup"><span data-stu-id="4c8b0-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="4c8b0-120">Raddefinisjon</span><span class="sxs-lookup"><span data-stu-id="4c8b0-120">Row definition</span></span>

<span data-ttu-id="4c8b0-121">Raddefinisjon, Sammendrag for resultatregnskap – Standard, inneholder en inndeling for hver del av et tradisjonelt resultatregnskap.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="4c8b0-122">Dimensjonen for hovedkontokategorien brukes til å opprette denne raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="4c8b0-123">Derfor kan alle generere rapporten uten å gjøre endringer.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="4c8b0-124">Kolonnedefinisjon</span><span class="sxs-lookup"><span data-stu-id="4c8b0-124">Column Definition</span></span>

<span data-ttu-id="4c8b0-125">Kolonnedefinisjonene inneholder ulike typer kolonner for å angi ulike nivåer av detaljer og økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="4c8b0-126">**Periodisk og hittil i år – Standard kolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="4c8b0-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="4c8b0-127">**DESC** – Beskrivelsen fra raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="4c8b0-128">**FD** – Økonomiske data for inneværende periode</span><span class="sxs-lookup"><span data-stu-id="4c8b0-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="4c8b0-129">**FD** – Økonomiske data hittil i år</span><span class="sxs-lookup"><span data-stu-id="4c8b0-129">**FD** – Financial data for the year to date</span></span>

 

<a name="see-also"></a><span data-ttu-id="4c8b0-130">Se også</span><span class="sxs-lookup"><span data-stu-id="4c8b0-130">See also</span></span>
--------

[<span data-ttu-id="4c8b0-131">Finansrapportering</span><span class="sxs-lookup"><span data-stu-id="4c8b0-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="4c8b0-132">Vise finansrapporter</span><span class="sxs-lookup"><span data-stu-id="4c8b0-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="4c8b0-133">Blogg for Dynamics-finansrapportering</span><span class="sxs-lookup"><span data-stu-id="4c8b0-133">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




