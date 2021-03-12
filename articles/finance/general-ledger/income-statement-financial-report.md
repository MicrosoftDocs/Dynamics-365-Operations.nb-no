---
title: Finansrapport for resultatregnskap
description: Denne artikkelen beskriver standardrapporten for inntektsregnskap. Den beskriver også byggeblokker som er knyttet til denne rapporten.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 146d4b9946c1b29105cff637fa9d8803db3d0c0f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988784"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="7b322-104">Finansrapport for resultatregnskap</span><span class="sxs-lookup"><span data-stu-id="7b322-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b322-105">Denne artikkelen beskriver standardrapporten for inntektsregnskap.</span><span class="sxs-lookup"><span data-stu-id="7b322-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="7b322-106">Den beskriver også byggeblokker som er knyttet til denne rapporten.</span><span class="sxs-lookup"><span data-stu-id="7b322-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="7b322-107">Standardrapport for resultatregnskap</span><span class="sxs-lookup"><span data-stu-id="7b322-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="7b322-108">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="7b322-108">Default report</span></span>             | <span data-ttu-id="7b322-109">Resultat</span><span class="sxs-lookup"><span data-stu-id="7b322-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b322-110">Resultatregnskap – Standard</span><span class="sxs-lookup"><span data-stu-id="7b322-110">Income Statement – Default</span></span> | <span data-ttu-id="7b322-111">Gir en oversikt over organisasjonens lønnsomhet for inneværende periode, og også for hittil i år.</span><span class="sxs-lookup"><span data-stu-id="7b322-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="7b322-112">Byggeblokker</span><span class="sxs-lookup"><span data-stu-id="7b322-112">Building blocks</span></span>
<span data-ttu-id="7b322-113">Finansrapporten for resultatregnskapet bruker byggeblokkene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="7b322-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="7b322-114">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="7b322-114">Default report</span></span>             | <span data-ttu-id="7b322-115">Raddefinisjon</span><span class="sxs-lookup"><span data-stu-id="7b322-115">Row definition</span></span>                     | <span data-ttu-id="7b322-116">Kolonnedefinisjon</span><span class="sxs-lookup"><span data-stu-id="7b322-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="7b322-117">Resultatregnskap – Standard</span><span class="sxs-lookup"><span data-stu-id="7b322-117">Income Statement - Default</span></span> | <span data-ttu-id="7b322-118">Sammendrag for resultatregnskap – Standard</span><span class="sxs-lookup"><span data-stu-id="7b322-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="7b322-119">Periodisk og hittil i år – Standard</span><span class="sxs-lookup"><span data-stu-id="7b322-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="7b322-120">Raddefinisjon</span><span class="sxs-lookup"><span data-stu-id="7b322-120">Row definition</span></span>

<span data-ttu-id="7b322-121">Raddefinisjon, Sammendrag for resultatregnskap – Standard, inneholder en inndeling for hver del av et tradisjonelt resultatregnskap.</span><span class="sxs-lookup"><span data-stu-id="7b322-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="7b322-122">Dimensjonen for hovedkontokategorien brukes til å opprette denne raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="7b322-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="7b322-123">Derfor kan alle generere rapporten uten å gjøre endringer.</span><span class="sxs-lookup"><span data-stu-id="7b322-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="7b322-124">Kolonnedefinisjon</span><span class="sxs-lookup"><span data-stu-id="7b322-124">Column Definition</span></span>

<span data-ttu-id="7b322-125">Kolonnedefinisjonene inneholder ulike typer kolonner for å angi ulike nivåer av detaljer og økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="7b322-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="7b322-126">**Periodisk og hittil i år – Standard kolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="7b322-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="7b322-127">**DESC** – Beskrivelsen fra raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="7b322-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="7b322-128">**FD** – Økonomiske data for inneværende periode</span><span class="sxs-lookup"><span data-stu-id="7b322-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="7b322-129">**FD** – Økonomiske data hittil i år</span><span class="sxs-lookup"><span data-stu-id="7b322-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="7b322-130">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="7b322-130">Additional resources</span></span>
--------

[<span data-ttu-id="7b322-131">Oversikt over finansrapportering</span><span class="sxs-lookup"><span data-stu-id="7b322-131">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="7b322-132">Vise finansrapporter</span><span class="sxs-lookup"><span data-stu-id="7b322-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="7b322-133">Blogg for Dynamics-finansrapportering</span><span class="sxs-lookup"><span data-stu-id="7b322-133">Dynamics Financial Reporting Blog</span></span>](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)



