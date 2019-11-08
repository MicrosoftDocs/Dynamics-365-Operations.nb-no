---
title: Power BI-innholdet Analyse av innkjøp og forbruk
description: Dette emnet beskriver hva som er inkludert i Kjøps- og forbruksanalyse-innhold for Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdet, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdet.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d25bacc2ec1f8e13376b96e188b099a184f7f8c6
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569138"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="1f4b1-104">Power BI-innholdet Analyse av innkjøp og forbruk</span><span class="sxs-lookup"><span data-stu-id="1f4b1-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f4b1-105">Dette emnet beskriver hva som er inkludert i **Kjøps- og forbruksanalyse**-innhold for Power BI.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="1f4b1-106">Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="1f4b1-107">Oversikt</span><span class="sxs-lookup"><span data-stu-id="1f4b1-107">Overview</span></span>

<span data-ttu-id="1f4b1-108">**Kjøps- og forbruksanalyse**-innhold for Power BI ble utformet for å hjelpe innkjøpsledere og ledere som er ansvarlige for budsjetter, med å holde oversikt over kjøpsutgifter.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="1f4b1-109">Ledere kan analysere kjøpsutgifter på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="1f4b1-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="1f4b1-110">Kjøp hittil i år (etter leverandørgruppe og enkeltleverandører, innkjøpskategori og enkeltprodukter og leverandørplassering)</span><span class="sxs-lookup"><span data-stu-id="1f4b1-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="1f4b1-111">Årlig kjøpsendring (etter leverandørgruppe og innkjøpkategori)</span><span class="sxs-lookup"><span data-stu-id="1f4b1-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="1f4b1-112">Innholdet bruker kjøpstransaksjonsdata, og gir både en aggregert visning av kjøpstall for hele selskapet og en analyse av kjøpsutgifter etter leverandør og vare.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="1f4b1-113">Rapportene uthever endringer i kjøpsutgifter over tid.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="1f4b1-114">Derfor kan de brukes til å varsle ledere om positive og negative utgiftstrender for individuelle leverandører og produkter.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="1f4b1-115">I tillegg viser diagrammer kjøpsutgifter for forskjellige innkjøpskategorier og leverandørgrupper.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="1f4b1-116">Kategori- og distriktsledere kan derfor bruke diagrammene til å identifisere endringer i forbruksatferd.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="1f4b1-117">Tilgang til Power BI-innholdet</span><span class="sxs-lookup"><span data-stu-id="1f4b1-117">Accessing the Power BI content</span></span>
<span data-ttu-id="1f4b1-118">Power BI-innholdet **Analyse av innkjøp og forbruk** vises på **Analyse av innkjøp og forbruk**-siden (**Innkjøp og leverandører** \> **Forespørsler og rapporter** \> **Analyse av innkjøpsytelse** \> **Analyse av innkjøp og forbruk**).</span><span class="sxs-lookup"><span data-stu-id="1f4b1-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="1f4b1-119">Mål som er inkludert i Power BI-innholdet</span><span class="sxs-lookup"><span data-stu-id="1f4b1-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="1f4b1-120">**Kjøps- og forbruksanalyse**-innhold for Power BI inneholder en rapport som består av et sett med mål.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="1f4b1-121">Disse målene vises som diagrammer, fliser og tabeller.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-121">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="1f4b1-122">Delene nedenfor gir en oversikt over effektene.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-122">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="1f4b1-123">Rapportsiden Kjøp etter leverandør</span><span class="sxs-lookup"><span data-stu-id="1f4b1-123">Purchase by vendor report page</span></span>
<span data-ttu-id="1f4b1-124">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="1f4b1-124">**Charts**</span></span>
- <span data-ttu-id="1f4b1-125">De 10 viktigste leverandørene etter kjøp (stablet liggende stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="1f4b1-125">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="1f4b1-126">Totalt innkjøp etter leverandørgruppe / land / navn (sektordiagram)</span><span class="sxs-lookup"><span data-stu-id="1f4b1-126">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="1f4b1-127">Innkjøp etter leverandørgruppe / land / navn (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="1f4b1-127">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="1f4b1-128">Gjennomsnittlig innkjøp etter leverandørgruppe / land / navn (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="1f4b1-128">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="1f4b1-129">**Fliser**</span><span class="sxs-lookup"><span data-stu-id="1f4b1-129">**Tiles**</span></span>
- <span data-ttu-id="1f4b1-130">Totale innkjøp</span><span class="sxs-lookup"><span data-stu-id="1f4b1-130">Total purchase</span></span>
- <span data-ttu-id="1f4b1-131">Årlig innkjøpsvekst</span><span class="sxs-lookup"><span data-stu-id="1f4b1-131">YOY purchase growth</span></span>
- <span data-ttu-id="1f4b1-132">Totalt antall leverandører</span><span class="sxs-lookup"><span data-stu-id="1f4b1-132">Total # vendors</span></span>
- <span data-ttu-id="1f4b1-133">Totalt antall aktive leverandører</span><span class="sxs-lookup"><span data-stu-id="1f4b1-133">Total # of active vendors</span></span>

<span data-ttu-id="1f4b1-134">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="1f4b1-134">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="1f4b1-135">Rapportsiden Kjøp etter produkt</span><span class="sxs-lookup"><span data-stu-id="1f4b1-135">Purchase by product report page</span></span>

<span data-ttu-id="1f4b1-136">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="1f4b1-136">**Charts**</span></span>
- <span data-ttu-id="1f4b1-137">Kjøp etter innkjøpskategori / produktnavn (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="1f4b1-137">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="1f4b1-138">Totalt innkjøp etter innkjøpskategori / produktnavn (sektordiagram)</span><span class="sxs-lookup"><span data-stu-id="1f4b1-138">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="1f4b1-139">De 10 viktigste produktene etter kjøp (stablet liggende stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="1f4b1-139">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="1f4b1-140">**Fliser**</span><span class="sxs-lookup"><span data-stu-id="1f4b1-140">**Tiles**</span></span>
- <span data-ttu-id="1f4b1-141">Totalt antall produkter</span><span class="sxs-lookup"><span data-stu-id="1f4b1-141">Total # of products</span></span></li>
- <span data-ttu-id="1f4b1-142">Totalt antall aktive produktprosentdeler av totalt antall produkter</span><span class="sxs-lookup"><span data-stu-id="1f4b1-142">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="1f4b1-143">Antall produkter som står for 80 % av innkjøp</span><span class="sxs-lookup"><span data-stu-id="1f4b1-143">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="1f4b1-144">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="1f4b1-144">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="1f4b1-145">Rapportsiden Innkjøp etter periode</span><span class="sxs-lookup"><span data-stu-id="1f4b1-145">Purchase by period report page</span></span>
<span data-ttu-id="1f4b1-146">Denne siden viser innkjøp i år og forrige år, og vekst etter innkjøpskategori.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-146">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="1f4b1-147">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="1f4b1-147">**Charts**</span></span> 
- <span data-ttu-id="1f4b1-148">Innkjøp etter måned / dag (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="1f4b1-148">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="1f4b1-149">Kumulativ årlig kjøpsavvik (fossefallsdiagram)</span><span class="sxs-lookup"><span data-stu-id="1f4b1-149">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="1f4b1-150">Totalt årlig kjøpsvekst (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="1f4b1-150">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="1f4b1-151">Innkjøpsutdrag (matrise)</span><span class="sxs-lookup"><span data-stu-id="1f4b1-151">Procurement statement (matrix)</span></span>

<span data-ttu-id="1f4b1-152">**Fliser**</span><span class="sxs-lookup"><span data-stu-id="1f4b1-152">**Tiles**</span></span>
- <span data-ttu-id="1f4b1-153">Årlig innkjøpsvekst</span><span class="sxs-lookup"><span data-stu-id="1f4b1-153">YOY purchase growth</span></span>
- <span data-ttu-id="1f4b1-154">Årlig innkjøpsvekst i %</span><span class="sxs-lookup"><span data-stu-id="1f4b1-154">YOY purchase growth %</span></span>

<span data-ttu-id="1f4b1-155">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="1f4b1-155">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="1f4b1-156">Rapportsiden Kjøp etter leverandørplassering</span><span class="sxs-lookup"><span data-stu-id="1f4b1-156">Purchase by vendor location report page</span></span>

<span data-ttu-id="1f4b1-157">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="1f4b1-157">**Charts**</span></span>
- <span data-ttu-id="1f4b1-158">Kjøp etter by</span><span class="sxs-lookup"><span data-stu-id="1f4b1-158">Purchase by city</span></span>
- <span data-ttu-id="1f4b1-159">Årlig innkjøpsvekst i %</span><span class="sxs-lookup"><span data-stu-id="1f4b1-159">Purchase YOY growth %</span></span>
- <span data-ttu-id="1f4b1-160">Kjøp etter land</span><span class="sxs-lookup"><span data-stu-id="1f4b1-160">Purchase by country</span></span>

<span data-ttu-id="1f4b1-161">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="1f4b1-161">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="1f4b1-162">Rapportsiden Kjøps- og forbruksanalyse etter tid</span><span class="sxs-lookup"><span data-stu-id="1f4b1-162">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="1f4b1-163">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="1f4b1-163">**Charts**</span></span> 
- <span data-ttu-id="1f4b1-164">Kjøp inneværende år etter måned / dag (linjediagram)</span><span class="sxs-lookup"><span data-stu-id="1f4b1-164">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="1f4b1-165">Kjøp inneværende or forrige år (linjediagram og stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="1f4b1-165">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="1f4b1-166">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="1f4b1-166">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="1f4b1-167">Rapportsiden Kjøps- og forbruksanalyse etter leverandør</span><span class="sxs-lookup"><span data-stu-id="1f4b1-167">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="1f4b1-168">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="1f4b1-168">**Charts**</span></span> 
- <span data-ttu-id="1f4b1-169">De 10 viktigste leverandørkjøpene i % av kjøp (trakt)</span><span class="sxs-lookup"><span data-stu-id="1f4b1-169">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="1f4b1-170">De 10 viktigste leverandørene med økte årlige kjøp</span><span class="sxs-lookup"><span data-stu-id="1f4b1-170">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="1f4b1-171">De 10 viktigste leverandørene med reduserte årlige kjøp</span><span class="sxs-lookup"><span data-stu-id="1f4b1-171">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="1f4b1-172">**Eksempel** 
</span><span class="sxs-lookup"><span data-stu-id="1f4b1-172">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="1f4b1-173">Datamodell og enheter</span><span class="sxs-lookup"><span data-stu-id="1f4b1-173">Data model and entities</span></span>
<span data-ttu-id="1f4b1-174">Følgende data brukes til å fylle ut rapportsidene i **Kjøps- og forbruksanalyse**-innholdet for Power BI.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-174">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="1f4b1-175">Disse dataene vises som aggregerte mål som er oppsamlet i enhetslageret.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-175">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="1f4b1-176">Enhetslageret er en Microsoft SQL Server-database som er optimalisert for analyse.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-176">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="1f4b1-177">Hvis du vil ha mer informasjon, se [Oversikt over Power BI-integrering med enhetslager](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="1f4b1-177">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="1f4b1-178">De aggregerte målingene i denne innholdspakken er delsett av aggregerte målinger som var tilgjengelige i kjøpskuben i Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-178">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="1f4b1-179">For å plassere kubens aggregerte målinger i enhetslageret må du gjøre dem distribuerbare.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-179">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="1f4b1-180">Hvis du vil ha mer informasjon, kan du se fremgangsmåten for hvordan du plasserer aggregerte målinger i enhetsbutikken i [Oversikt over Power BI-integrering med enhetslager](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="1f4b1-180">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="1f4b1-181">De aggregerte nøkkelmålingene er tilgjengelige direkte fra fakturalinjeenheten, og brukes som grunnlag for innholdet.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-181">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="1f4b1-182">Enhet</span><span class="sxs-lookup"><span data-stu-id="1f4b1-182">Entity</span></span>        | <span data-ttu-id="1f4b1-183">Aggregerte nøkkelmålinger</span><span class="sxs-lookup"><span data-stu-id="1f4b1-183">Key aggregate measurements</span></span> | <span data-ttu-id="1f4b1-184">Datakilde</span><span class="sxs-lookup"><span data-stu-id="1f4b1-184">Data source</span></span>                                 | <span data-ttu-id="1f4b1-185">Felt</span><span class="sxs-lookup"><span data-stu-id="1f4b1-185">Field</span></span>              | <span data-ttu-id="1f4b1-186">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="1f4b1-186">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="1f4b1-187">Fakturalinjer</span><span class="sxs-lookup"><span data-stu-id="1f4b1-187">Invoice lines</span></span> | <span data-ttu-id="1f4b1-188">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="1f4b1-188">Purchase</span></span>                   | <span data-ttu-id="1f4b1-189">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="1f4b1-189">VendInvoiceTrans</span></span>                            | <span data-ttu-id="1f4b1-190">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="1f4b1-190">SUM(LineAmountMST)</span></span> | <span data-ttu-id="1f4b1-191">Beløpet i regnskapsvaluta</span><span class="sxs-lookup"><span data-stu-id="1f4b1-191">The amount in the accounting currency.</span></span> |

<span data-ttu-id="1f4b1-192">Tabellen nedenfor viser viktige målinger som beregnes i innholdet fra fakturalinjeenheten.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-192">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="1f4b1-193">Mål</span><span class="sxs-lookup"><span data-stu-id="1f4b1-193">Measure</span></span>               | <span data-ttu-id="1f4b1-194">Beregning</span><span class="sxs-lookup"><span data-stu-id="1f4b1-194">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f4b1-195">Kjøp inneværende år</span><span class="sxs-lookup"><span data-stu-id="1f4b1-195">Purchase current year</span></span> | <span data-ttu-id="1f4b1-196">Kjøp inneværende år = SUM('Fakturalinjer'\[Kjøp\])</span><span class="sxs-lookup"><span data-stu-id="1f4b1-196">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="1f4b1-197">Kjøp forrige år</span><span class="sxs-lookup"><span data-stu-id="1f4b1-197">Purchase last year</span></span>    | <span data-ttu-id="1f4b1-198">Kjøp forrige år = CALCULATE(SUM('Fakturalinjer'\[Kjøp\]), SAMEPERIODLASTYEAR((Datoer\[Dato\]))</span><span class="sxs-lookup"><span data-stu-id="1f4b1-198">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="1f4b1-199">Årlig innkjøpsvekst</span><span class="sxs-lookup"><span data-stu-id="1f4b1-199">YOY purchase growth</span></span>   | <span data-ttu-id="1f4b1-200">Årlig kjøpsvekst = \[Kjøp inneværende år\] – \[Kjøp forrige år\]</span><span class="sxs-lookup"><span data-stu-id="1f4b1-200">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="1f4b1-201">Nøkkeldimensjonene nedenfor i innholdet brukes som filtre for å dele opp de aggregerte målingene, slik at du kan få flere detaljer og dypere analytisk innsikt.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-201">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="1f4b1-202">Enhet</span><span class="sxs-lookup"><span data-stu-id="1f4b1-202">Entity</span></span>                 | <span data-ttu-id="1f4b1-203">Eksempler på attributter</span><span class="sxs-lookup"><span data-stu-id="1f4b1-203">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="1f4b1-204">Leverandører</span><span class="sxs-lookup"><span data-stu-id="1f4b1-204">Vendors</span></span>                | <span data-ttu-id="1f4b1-205">Leverandørgrupper, leverandørland eller områder, leverandørnavn</span><span class="sxs-lookup"><span data-stu-id="1f4b1-205">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="1f4b1-206">Produkter</span><span class="sxs-lookup"><span data-stu-id="1f4b1-206">Products</span></span>               | <span data-ttu-id="1f4b1-207">Produktnummer, produktnavn, navn på varegrupper</span><span class="sxs-lookup"><span data-stu-id="1f4b1-207">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="1f4b1-208">Innkjøpskategorier</span><span class="sxs-lookup"><span data-stu-id="1f4b1-208">Procurement categories</span></span> | <span data-ttu-id="1f4b1-209">Innkjøpskategori, navn på innkjøpskategori</span><span class="sxs-lookup"><span data-stu-id="1f4b1-209">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="1f4b1-210">Juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="1f4b1-210">Legal entities</span></span>         | <span data-ttu-id="1f4b1-211">Navn på juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="1f4b1-211">Legal entity name</span></span>                                     |
| <span data-ttu-id="1f4b1-212">Datoer</span><span class="sxs-lookup"><span data-stu-id="1f4b1-212">Dates</span></span>                  | <span data-ttu-id="1f4b1-213">Datoer, årsforskyvning</span><span class="sxs-lookup"><span data-stu-id="1f4b1-213">Dates, Year offset</span></span>                                    |

<span data-ttu-id="1f4b1-214">Som standard viser innholdspakkedataene for inneværende kalenderår.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="1f4b1-215">Du kan imidlertid endre datofilteret i delen for rapportfiltre.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="1f4b1-216">Du kan også endre firmafilteret.</span><span class="sxs-lookup"><span data-stu-id="1f4b1-216">You can also change the company filter.</span></span>
