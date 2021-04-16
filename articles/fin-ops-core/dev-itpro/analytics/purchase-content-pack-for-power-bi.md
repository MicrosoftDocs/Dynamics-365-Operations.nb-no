---
title: Power BI-innholdet Analyse av innkjøp og forbruk
description: Dette emnet beskriver hva som er inkludert i Kjøps- og forbruksanalyse-innhold for Power BI.
author: FrankDahl
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f9741b5f30f5e62b9e80000953113377fe016253
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749375"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="6924b-103">Power BI-innholdet Analyse av innkjøp og forbruk</span><span class="sxs-lookup"><span data-stu-id="6924b-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6924b-104">Dette emnet beskriver hva som er inkludert i Microsoft Power BI-innholdet for **Analyse av innkjøp og forbruk**.</span><span class="sxs-lookup"><span data-stu-id="6924b-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="6924b-105">Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.</span><span class="sxs-lookup"><span data-stu-id="6924b-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="6924b-106">Oversikt</span><span class="sxs-lookup"><span data-stu-id="6924b-106">Overview</span></span>

<span data-ttu-id="6924b-107">**Kjøps- og forbruksanalyse**-innhold for Power BI ble utformet for å hjelpe innkjøpsledere og ledere som er ansvarlige for budsjetter, med å holde oversikt over kjøpsutgifter.</span><span class="sxs-lookup"><span data-stu-id="6924b-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="6924b-108">Ledere kan analysere kjøpsutgifter på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="6924b-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="6924b-109">Kjøp hittil i år (etter leverandørgruppe og enkeltleverandører, innkjøpskategori og enkeltprodukter og leverandørplassering)</span><span class="sxs-lookup"><span data-stu-id="6924b-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="6924b-110">Årlig kjøpsendring (etter leverandørgruppe og innkjøpkategori)</span><span class="sxs-lookup"><span data-stu-id="6924b-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="6924b-111">Innholdet bruker kjøpstransaksjonsdata, og gir både en aggregert visning av kjøpstall for hele selskapet og en analyse av kjøpsutgifter etter leverandør og vare.</span><span class="sxs-lookup"><span data-stu-id="6924b-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="6924b-112">Rapportene uthever endringer i kjøpsutgifter over tid.</span><span class="sxs-lookup"><span data-stu-id="6924b-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="6924b-113">Derfor kan de brukes til å varsle ledere om positive og negative utgiftstrender for individuelle leverandører og produkter.</span><span class="sxs-lookup"><span data-stu-id="6924b-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="6924b-114">I tillegg viser diagrammer kjøpsutgifter for forskjellige innkjøpskategorier og leverandørgrupper.</span><span class="sxs-lookup"><span data-stu-id="6924b-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="6924b-115">Kategori- og distriktsledere kan derfor bruke diagrammene til å identifisere endringer i forbruksatferd.</span><span class="sxs-lookup"><span data-stu-id="6924b-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="6924b-116">Tilgang til Power BI-innholdet</span><span class="sxs-lookup"><span data-stu-id="6924b-116">Accessing the Power BI content</span></span>
<span data-ttu-id="6924b-117">Power BI-innholdet **Analyse av innkjøp og forbruk** vises på **Analyse av innkjøp og forbruk**-siden (**Innkjøp og leverandører** \> **Forespørsler og rapporter** \> **Analyse av innkjøpsytelse** \> **Analyse av innkjøp og forbruk**).</span><span class="sxs-lookup"><span data-stu-id="6924b-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="6924b-118">Mål som er inkludert i Power BI-innholdet</span><span class="sxs-lookup"><span data-stu-id="6924b-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="6924b-119">**Kjøps- og forbruksanalyse**-innhold for Power BI inneholder en rapport som består av et sett med mål.</span><span class="sxs-lookup"><span data-stu-id="6924b-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="6924b-120">Disse målene vises som diagrammer, fliser og tabeller.</span><span class="sxs-lookup"><span data-stu-id="6924b-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="6924b-121">Delene nedenfor gir en oversikt over effektene.</span><span class="sxs-lookup"><span data-stu-id="6924b-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="6924b-122">Rapportsiden Kjøp etter leverandør</span><span class="sxs-lookup"><span data-stu-id="6924b-122">Purchase by vendor report page</span></span>
<span data-ttu-id="6924b-123">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="6924b-123">**Charts**</span></span>
- <span data-ttu-id="6924b-124">De 10 viktigste leverandørene etter kjøp (stablet liggende stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="6924b-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="6924b-125">Totalt innkjøp etter leverandørgruppe / land / navn (sektordiagram)</span><span class="sxs-lookup"><span data-stu-id="6924b-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="6924b-126">Innkjøp etter leverandørgruppe / land / navn (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="6924b-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="6924b-127">Gjennomsnittlig innkjøp etter leverandørgruppe / land / navn (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="6924b-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="6924b-128">**Fliser**</span><span class="sxs-lookup"><span data-stu-id="6924b-128">**Tiles**</span></span>
- <span data-ttu-id="6924b-129">Totale innkjøp</span><span class="sxs-lookup"><span data-stu-id="6924b-129">Total purchase</span></span>
- <span data-ttu-id="6924b-130">Årlig innkjøpsvekst</span><span class="sxs-lookup"><span data-stu-id="6924b-130">YOY purchase growth</span></span>
- <span data-ttu-id="6924b-131">Totalt antall leverandører</span><span class="sxs-lookup"><span data-stu-id="6924b-131">Total # vendors</span></span>
- <span data-ttu-id="6924b-132">Totalt antall aktive leverandører</span><span class="sxs-lookup"><span data-stu-id="6924b-132">Total # of active vendors</span></span>

<span data-ttu-id="6924b-133">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="6924b-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="6924b-134">Rapportsiden Kjøp etter produkt</span><span class="sxs-lookup"><span data-stu-id="6924b-134">Purchase by product report page</span></span>

<span data-ttu-id="6924b-135">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="6924b-135">**Charts**</span></span>
- <span data-ttu-id="6924b-136">Kjøp etter innkjøpskategori / produktnavn (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="6924b-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="6924b-137">Totalt innkjøp etter innkjøpskategori / produktnavn (sektordiagram)</span><span class="sxs-lookup"><span data-stu-id="6924b-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="6924b-138">De 10 viktigste produktene etter kjøp (stablet liggende stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="6924b-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="6924b-139">**Fliser**</span><span class="sxs-lookup"><span data-stu-id="6924b-139">**Tiles**</span></span>
- <span data-ttu-id="6924b-140">Totalt antall produkter</span><span class="sxs-lookup"><span data-stu-id="6924b-140">Total # of products</span></span></li>
- <span data-ttu-id="6924b-141">Totalt antall aktive produktprosentdeler av totalt antall produkter</span><span class="sxs-lookup"><span data-stu-id="6924b-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="6924b-142">Antall produkter som står for 80 % av innkjøp</span><span class="sxs-lookup"><span data-stu-id="6924b-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="6924b-143">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="6924b-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="6924b-144">Rapportsiden Innkjøp etter periode</span><span class="sxs-lookup"><span data-stu-id="6924b-144">Purchase by period report page</span></span>
<span data-ttu-id="6924b-145">Denne siden viser innkjøp i år og forrige år, og vekst etter innkjøpskategori.</span><span class="sxs-lookup"><span data-stu-id="6924b-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="6924b-146">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="6924b-146">**Charts**</span></span> 
- <span data-ttu-id="6924b-147">Innkjøp etter måned / dag (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="6924b-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="6924b-148">Kumulativ årlig kjøpsavvik (fossefallsdiagram)</span><span class="sxs-lookup"><span data-stu-id="6924b-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="6924b-149">Totalt årlig kjøpsvekst (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="6924b-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="6924b-150">Innkjøpsutdrag (matrise)</span><span class="sxs-lookup"><span data-stu-id="6924b-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="6924b-151">**Fliser**</span><span class="sxs-lookup"><span data-stu-id="6924b-151">**Tiles**</span></span>
- <span data-ttu-id="6924b-152">Årlig innkjøpsvekst</span><span class="sxs-lookup"><span data-stu-id="6924b-152">YOY purchase growth</span></span>
- <span data-ttu-id="6924b-153">Årlig innkjøpsvekst i %</span><span class="sxs-lookup"><span data-stu-id="6924b-153">YOY purchase growth %</span></span>

<span data-ttu-id="6924b-154">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="6924b-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="6924b-155">Rapportsiden Kjøp etter leverandørplassering</span><span class="sxs-lookup"><span data-stu-id="6924b-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="6924b-156">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="6924b-156">**Charts**</span></span>
- <span data-ttu-id="6924b-157">Kjøp etter by</span><span class="sxs-lookup"><span data-stu-id="6924b-157">Purchase by city</span></span>
- <span data-ttu-id="6924b-158">Årlig innkjøpsvekst i %</span><span class="sxs-lookup"><span data-stu-id="6924b-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="6924b-159">Kjøp etter land</span><span class="sxs-lookup"><span data-stu-id="6924b-159">Purchase by country</span></span>

<span data-ttu-id="6924b-160">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="6924b-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="6924b-161">Rapportsiden Kjøps- og forbruksanalyse etter tid</span><span class="sxs-lookup"><span data-stu-id="6924b-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="6924b-162">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="6924b-162">**Charts**</span></span> 
- <span data-ttu-id="6924b-163">Kjøp inneværende år etter måned / dag (linjediagram)</span><span class="sxs-lookup"><span data-stu-id="6924b-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="6924b-164">Kjøp inneværende or forrige år (linjediagram og stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="6924b-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="6924b-165">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="6924b-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="6924b-166">Rapportsiden Kjøps- og forbruksanalyse etter leverandør</span><span class="sxs-lookup"><span data-stu-id="6924b-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="6924b-167">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="6924b-167">**Charts**</span></span> 
- <span data-ttu-id="6924b-168">De 10 viktigste leverandørkjøpene i % av kjøp (trakt)</span><span class="sxs-lookup"><span data-stu-id="6924b-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="6924b-169">De 10 viktigste leverandørene med økte årlige kjøp</span><span class="sxs-lookup"><span data-stu-id="6924b-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="6924b-170">De 10 viktigste leverandørene med reduserte årlige kjøp</span><span class="sxs-lookup"><span data-stu-id="6924b-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="6924b-171">**Eksempel** 
</span><span class="sxs-lookup"><span data-stu-id="6924b-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="6924b-172">Datamodell og enheter</span><span class="sxs-lookup"><span data-stu-id="6924b-172">Data model and entities</span></span>
<span data-ttu-id="6924b-173">Følgende data brukes til å fylle ut rapportsidene i **Kjøps- og forbruksanalyse**-innholdet for Power BI.</span><span class="sxs-lookup"><span data-stu-id="6924b-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="6924b-174">Disse dataene vises som aggregerte mål som er oppsamlet i enhetslageret.</span><span class="sxs-lookup"><span data-stu-id="6924b-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="6924b-175">Enhetslageret er en Microsoft SQL Server-database som er optimalisert for analyse.</span><span class="sxs-lookup"><span data-stu-id="6924b-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="6924b-176">Hvis du vil ha mer informasjon, se [Power BI-integrering med enhetslager](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="6924b-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="6924b-177">De aggregerte målingene i denne innholdspakken er delsett av aggregerte målinger som var tilgjengelige i kjøpskuben i Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="6924b-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="6924b-178">For å plassere kubens aggregerte målinger i enhetslageret må du gjøre dem distribuerbare.</span><span class="sxs-lookup"><span data-stu-id="6924b-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="6924b-179">Hvis du vil ha mer informasjon, kan du se fremgangsmåten for hvordan du plasserer aggregerte målinger i enhetsbutikken i  [Power BI-integrering med enhetslager](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="6924b-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="6924b-180">De aggregerte nøkkelmålingene er tilgjengelige direkte fra fakturalinjeenheten, og brukes som grunnlag for innholdet.</span><span class="sxs-lookup"><span data-stu-id="6924b-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="6924b-181">Enhet</span><span class="sxs-lookup"><span data-stu-id="6924b-181">Entity</span></span>        | <span data-ttu-id="6924b-182">Aggregerte nøkkelmålinger</span><span class="sxs-lookup"><span data-stu-id="6924b-182">Key aggregate measurements</span></span> | <span data-ttu-id="6924b-183">Datakilde</span><span class="sxs-lookup"><span data-stu-id="6924b-183">Data source</span></span>                                 | <span data-ttu-id="6924b-184">Felt</span><span class="sxs-lookup"><span data-stu-id="6924b-184">Field</span></span>              | <span data-ttu-id="6924b-185">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6924b-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="6924b-186">Fakturalinjer</span><span class="sxs-lookup"><span data-stu-id="6924b-186">Invoice lines</span></span> | <span data-ttu-id="6924b-187">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="6924b-187">Purchase</span></span>                   | <span data-ttu-id="6924b-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="6924b-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="6924b-189">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="6924b-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="6924b-190">Beløpet i regnskapsvaluta</span><span class="sxs-lookup"><span data-stu-id="6924b-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="6924b-191">Tabellen nedenfor viser viktige målinger som beregnes i innholdet fra fakturalinjeenheten.</span><span class="sxs-lookup"><span data-stu-id="6924b-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="6924b-192">Mål</span><span class="sxs-lookup"><span data-stu-id="6924b-192">Measure</span></span>               | <span data-ttu-id="6924b-193">Beregning</span><span class="sxs-lookup"><span data-stu-id="6924b-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6924b-194">Kjøp inneværende år</span><span class="sxs-lookup"><span data-stu-id="6924b-194">Purchase current year</span></span> | <span data-ttu-id="6924b-195">Kjøp inneværende år = SUM('Fakturalinjer'\[Kjøp\])</span><span class="sxs-lookup"><span data-stu-id="6924b-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="6924b-196">Kjøp forrige år</span><span class="sxs-lookup"><span data-stu-id="6924b-196">Purchase last year</span></span>    | <span data-ttu-id="6924b-197">Kjøp forrige år = CALCULATE(SUM('Fakturalinjer'\[Kjøp\]), SAMEPERIODLASTYEAR(Datoer\[Dato\]))</span><span class="sxs-lookup"><span data-stu-id="6924b-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="6924b-198">Årlig innkjøpsvekst</span><span class="sxs-lookup"><span data-stu-id="6924b-198">YOY purchase growth</span></span>   | <span data-ttu-id="6924b-199">Årlig kjøpsvekst = \[Kjøp inneværende år\] – \[Kjøp forrige år\]</span><span class="sxs-lookup"><span data-stu-id="6924b-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="6924b-200">Nøkkeldimensjonene nedenfor i innholdet brukes som filtre for å dele opp de aggregerte målingene, slik at du kan få flere detaljer og dypere analytisk innsikt.</span><span class="sxs-lookup"><span data-stu-id="6924b-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="6924b-201">Enhet</span><span class="sxs-lookup"><span data-stu-id="6924b-201">Entity</span></span>                 | <span data-ttu-id="6924b-202">Eksempler på attributter</span><span class="sxs-lookup"><span data-stu-id="6924b-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="6924b-203">Leverandører</span><span class="sxs-lookup"><span data-stu-id="6924b-203">Vendors</span></span>                | <span data-ttu-id="6924b-204">Leverandørgrupper, leverandørland eller områder, leverandørnavn</span><span class="sxs-lookup"><span data-stu-id="6924b-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="6924b-205">Produkter</span><span class="sxs-lookup"><span data-stu-id="6924b-205">Products</span></span>               | <span data-ttu-id="6924b-206">Produktnummer, produktnavn, navn på varegrupper</span><span class="sxs-lookup"><span data-stu-id="6924b-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="6924b-207">Innkjøpskategorier</span><span class="sxs-lookup"><span data-stu-id="6924b-207">Procurement categories</span></span> | <span data-ttu-id="6924b-208">Innkjøpskategori, navn på innkjøpskategori</span><span class="sxs-lookup"><span data-stu-id="6924b-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="6924b-209">Juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="6924b-209">Legal entities</span></span>         | <span data-ttu-id="6924b-210">Navn på juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="6924b-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="6924b-211">Datoer</span><span class="sxs-lookup"><span data-stu-id="6924b-211">Dates</span></span>                  | <span data-ttu-id="6924b-212">Datoer, årsforskyvning</span><span class="sxs-lookup"><span data-stu-id="6924b-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="6924b-213">Som standard viser innholdspakkedataene for inneværende kalenderår.</span><span class="sxs-lookup"><span data-stu-id="6924b-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="6924b-214">Du kan imidlertid endre datofilteret i delen for rapportfiltre.</span><span class="sxs-lookup"><span data-stu-id="6924b-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="6924b-215">Du kan også endre firmafilteret.</span><span class="sxs-lookup"><span data-stu-id="6924b-215">You can also change the company filter.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]