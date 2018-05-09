---
title: "Kjøps- og forbruksanalyse-innhold for Power BI"
description: "Dette emnet beskriver hva som er inkludert i Kjøps- og forbruksanalyse-innhold for Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdet, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ab9fe6d0abc996af15ec4ace84e18d3db64f4e08
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="45bb8-104">Kjøps- og forbruksanalyse-innhold for Power BI</span><span class="sxs-lookup"><span data-stu-id="45bb8-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45bb8-105">Dette emnet beskriver hva som er inkludert i **Kjøps- og forbruksanalyse**-innhold for Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="45bb8-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="45bb8-106">Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.</span><span class="sxs-lookup"><span data-stu-id="45bb8-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="45bb8-107">Oversikt</span><span class="sxs-lookup"><span data-stu-id="45bb8-107">Overview</span></span>

<span data-ttu-id="45bb8-108">**Kjøps- og forbruksanalyse**-innhold for Power BI ble utformet for å hjelpe innkjøpsledere og ledere som er ansvarlige for budsjetter, med å holde øye med kjøpsutgifter.</span><span class="sxs-lookup"><span data-stu-id="45bb8-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="45bb8-109">Ledere kan analysere kjøpsutgifter på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="45bb8-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="45bb8-110">Kjøp hittil i år (etter leverandørgruppe og enkeltleverandører, innkjøpskategori og enkeltprodukter og leverandørplassering)</span><span class="sxs-lookup"><span data-stu-id="45bb8-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="45bb8-111">Årlig kjøpsendring (etter leverandørgruppe og innkjøpkategori)</span><span class="sxs-lookup"><span data-stu-id="45bb8-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="45bb8-112">Innholdet bruker kjøpstransaksjonsdata, og gir både en aggregert visning av kjøpstall for hele selskapet og en analyse av kjøpsutgifter etter leverandør og vare.</span><span class="sxs-lookup"><span data-stu-id="45bb8-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="45bb8-113">Rapportene uthever endringer i kjøpsutgifter over tid.</span><span class="sxs-lookup"><span data-stu-id="45bb8-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="45bb8-114">Derfor kan de brukes til å varsle ledere om positive og negative utgiftstrender for individuelle leverandører og produkter.</span><span class="sxs-lookup"><span data-stu-id="45bb8-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="45bb8-115">I tillegg viser diagrammer kjøpsutgifter for forskjellige innkjøpskategorier og leverandørgrupper.</span><span class="sxs-lookup"><span data-stu-id="45bb8-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="45bb8-116">Kategori- og distriktsledere kan derfor bruke diagrammene til å identifisere endringer i forbruksatferd.</span><span class="sxs-lookup"><span data-stu-id="45bb8-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="45bb8-117">Tilgang til Power BI-innhold</span><span class="sxs-lookup"><span data-stu-id="45bb8-117">Accessing the Power BI content</span></span>
<span data-ttu-id="45bb8-118">Power BI-innholdet **Analyse av innkjøp og forbruk** vises på **Analyse av innkjøp og forbruk**-siden (**Innkjøp og leverandører** > **Forespørsler og rapporter** > **Analyse av innkjøpsytelse** > **Analyse av innkjøp og forbruk**).</span><span class="sxs-lookup"><span data-stu-id="45bb8-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="45bb8-119">Mål som er inkludert i Power BI-innholdet</span><span class="sxs-lookup"><span data-stu-id="45bb8-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="45bb8-120">**Kjøps- og forbruksanalyse**-innhold for Power BI inneholder en rapport som består av et sett med mål.</span><span class="sxs-lookup"><span data-stu-id="45bb8-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="45bb8-121">Disse målene vises som diagrammer, fliser og tabeller.</span><span class="sxs-lookup"><span data-stu-id="45bb8-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="45bb8-122">Tabellen nedenfor gir en oversikt over effektene.</span><span class="sxs-lookup"><span data-stu-id="45bb8-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45bb8-123">Rapportside</span><span class="sxs-lookup"><span data-stu-id="45bb8-123">Report page</span></span></th>
<th><span data-ttu-id="45bb8-124">Diagrammer</span><span class="sxs-lookup"><span data-stu-id="45bb8-124">Charts</span></span></th>
<th><span data-ttu-id="45bb8-125">Fliser</span><span class="sxs-lookup"><span data-stu-id="45bb8-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="45bb8-126">Kjøp etter leverandør</span><span class="sxs-lookup"><span data-stu-id="45bb8-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="45bb8-127">De 10 viktigste leverandørene etter kjøp (stablet liggende stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="45bb8-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="45bb8-128">Totalt innkjøp etter leverandørgruppe / land / navn (sektordiagram)</span><span class="sxs-lookup"><span data-stu-id="45bb8-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="45bb8-129">Innkjøp etter leverandørgruppe / land / navn (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="45bb8-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="45bb8-130">Gjennomsnittlig innkjøp etter leverandørgruppe / land / navn (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="45bb8-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="45bb8-131">Totale innkjøp</span><span class="sxs-lookup"><span data-stu-id="45bb8-131">Total purchase</span></span></li>
<li><span data-ttu-id="45bb8-132">Årlig innkjøpsvekst</span><span class="sxs-lookup"><span data-stu-id="45bb8-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="45bb8-133">Totalt antall leverandører</span><span class="sxs-lookup"><span data-stu-id="45bb8-133">Total # vendors</span></span></li>
<li><span data-ttu-id="45bb8-134">Totalt antall aktive leverandører</span><span class="sxs-lookup"><span data-stu-id="45bb8-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45bb8-135">Kjøp etter produkt</span><span class="sxs-lookup"><span data-stu-id="45bb8-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="45bb8-136">Kjøp etter innkjøpskategori / produktnavn (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="45bb8-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="45bb8-137">Totalt innkjøp etter innkjøpskategori / produktnavn (sektordiagram)</span><span class="sxs-lookup"><span data-stu-id="45bb8-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="45bb8-138">De 10 viktigste produktene etter kjøp (stablet liggende stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="45bb8-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="45bb8-139">Totalt antall produkter</span><span class="sxs-lookup"><span data-stu-id="45bb8-139">Total # of products</span></span></li>
<li><span data-ttu-id="45bb8-140">Totalt antall aktive produktprosentdeler av totalt antall produkter</span><span class="sxs-lookup"><span data-stu-id="45bb8-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="45bb8-141">Antall produkter som står for 80 % av innkjøp</span><span class="sxs-lookup"><span data-stu-id="45bb8-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45bb8-142">Innkjøp etter periode\*</span><span class="sxs-lookup"><span data-stu-id="45bb8-142">Purchase by period\*</span></span></td>
<td><ul>
<li><span data-ttu-id="45bb8-143">Innkjøp etter måned / dag (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="45bb8-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="45bb8-144">Kumulativ årlig kjøpsavvik (fossefallsdiagram)</span><span class="sxs-lookup"><span data-stu-id="45bb8-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="45bb8-145">Totalt årlig kjøpsvekst (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="45bb8-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="45bb8-146">Innkjøpsutdrag (matrise)</span><span class="sxs-lookup"><span data-stu-id="45bb8-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="45bb8-147">Årlig innkjøpsvekst</span><span class="sxs-lookup"><span data-stu-id="45bb8-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="45bb8-148">Årlig innkjøpsvekst i %</span><span class="sxs-lookup"><span data-stu-id="45bb8-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45bb8-149">Kjøp etter leverandørplassering</span><span class="sxs-lookup"><span data-stu-id="45bb8-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="45bb8-150">Kjøp etter by</span><span class="sxs-lookup"><span data-stu-id="45bb8-150">Purchase by city</span></span></li>
<li><span data-ttu-id="45bb8-151">Årlig innkjøpsvekst i %</span><span class="sxs-lookup"><span data-stu-id="45bb8-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="45bb8-152">Kjøp etter land</span><span class="sxs-lookup"><span data-stu-id="45bb8-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45bb8-153">Kjøps- og forbruksanalyse etter tid</span><span class="sxs-lookup"><span data-stu-id="45bb8-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="45bb8-154">Kjøp inneværende år etter måned / dag (linjediagram)</span><span class="sxs-lookup"><span data-stu-id="45bb8-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="45bb8-155">Kjøp inneværende or forrige år (linjediagram og stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="45bb8-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45bb8-156">Kjøps- og forbruksanalyse etter leverandør</span><span class="sxs-lookup"><span data-stu-id="45bb8-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="45bb8-157">De 10 viktigste leverandørkjøpene i % av kjøp (trakt)</span><span class="sxs-lookup"><span data-stu-id="45bb8-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="45bb8-158">De 10 viktigste leverandørene med økte årlige kjøp</span><span class="sxs-lookup"><span data-stu-id="45bb8-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="45bb8-159">De 10 viktigste leverandørene med reduserte årlige kjøp</span><span class="sxs-lookup"><span data-stu-id="45bb8-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="45bb8-160">\* Innkjøp i år og forrige år. og vekst etter innkjøpskategori</span><span class="sxs-lookup"><span data-stu-id="45bb8-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="45bb8-161">Datamodell og enheter</span><span class="sxs-lookup"><span data-stu-id="45bb8-161">Data model and entities</span></span>
<span data-ttu-id="45bb8-162">Følgende data brukes til å fylle ut rapportsidene i **Kjøps- og forbruksanalyse**-innholdet for Power BI.</span><span class="sxs-lookup"><span data-stu-id="45bb8-162">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="45bb8-163">Disse dataene vises som aggregerte mål som er oppsamlet i enhetslageret.</span><span class="sxs-lookup"><span data-stu-id="45bb8-163">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="45bb8-164">Enhetslageret er en Microsoft SQL Server-database som er optimalisert for analyse.</span><span class="sxs-lookup"><span data-stu-id="45bb8-164">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="45bb8-165">Hvis du vil ha mer informasjon, se [Oversikt over Power BI-integrering med enhetslager](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="45bb8-165">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="45bb8-166">De aggregerte målingene i denne innholdspakken er delsett av aggregerte målinger som var tilgjengelige i innkjøpskuben i Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="45bb8-166">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="45bb8-167">For å plassere kubens aggregerte målinger i enhetslageret må du gjøre dem distribuerbare.</span><span class="sxs-lookup"><span data-stu-id="45bb8-167">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="45bb8-168">Hvis du vil ha mer informasjon, kan du se fremgangsmåten for hvordan du plasserer aggregerte målinger i enhetsbutikken i blogginnlegget [Oversikt over Power BI-integrering med enhetslager](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="45bb8-168">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="45bb8-169">De aggregerte nøkkelmålingene er tilgjengelige direkte fra fakturalinjeenheten, og brukes som grunnlag for innholdet.</span><span class="sxs-lookup"><span data-stu-id="45bb8-169">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="45bb8-170">Enhet</span><span class="sxs-lookup"><span data-stu-id="45bb8-170">Entity</span></span>        | <span data-ttu-id="45bb8-171">Aggregerte nøkkelmålinger</span><span class="sxs-lookup"><span data-stu-id="45bb8-171">Key aggregate measurements</span></span> | <span data-ttu-id="45bb8-172">Datakilde</span><span class="sxs-lookup"><span data-stu-id="45bb8-172">Data source</span></span>                                 | <span data-ttu-id="45bb8-173">Felt</span><span class="sxs-lookup"><span data-stu-id="45bb8-173">Field</span></span>              | <span data-ttu-id="45bb8-174">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="45bb8-174">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="45bb8-175">Fakturalinjer</span><span class="sxs-lookup"><span data-stu-id="45bb8-175">Invoice lines</span></span> | <span data-ttu-id="45bb8-176">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="45bb8-176">Purchase</span></span>                   | <span data-ttu-id="45bb8-177">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="45bb8-177">VendInvoiceTrans</span></span>                            | <span data-ttu-id="45bb8-178">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="45bb8-178">SUM(LineAmountMST)</span></span> | <span data-ttu-id="45bb8-179">Beløpet i regnskapsvaluta</span><span class="sxs-lookup"><span data-stu-id="45bb8-179">The amount in the accounting currency.</span></span> |

<span data-ttu-id="45bb8-180">Tabellen nedenfor viser viktige målinger som beregnes i innholdet fra fakturalinjeenheten.</span><span class="sxs-lookup"><span data-stu-id="45bb8-180">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="45bb8-181">Mål</span><span class="sxs-lookup"><span data-stu-id="45bb8-181">Measure</span></span>               | <span data-ttu-id="45bb8-182">Beregning</span><span class="sxs-lookup"><span data-stu-id="45bb8-182">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45bb8-183">Kjøp inneværende år</span><span class="sxs-lookup"><span data-stu-id="45bb8-183">Purchase current year</span></span> | <span data-ttu-id="45bb8-184">Kjøp inneværende år = SUM('Fakturalinjer'\[Kjøp\])</span><span class="sxs-lookup"><span data-stu-id="45bb8-184">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="45bb8-185">Kjøp forrige år</span><span class="sxs-lookup"><span data-stu-id="45bb8-185">Purchase last year</span></span>    | <span data-ttu-id="45bb8-186">Kjøp forrige år = CALCULATE(SUM('Fakturalinjer'\[Kjøp\]), SAMEPERIODLASTYEAR((Datoer\[Dato\]))</span><span class="sxs-lookup"><span data-stu-id="45bb8-186">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="45bb8-187">Årlig innkjøpsvekst</span><span class="sxs-lookup"><span data-stu-id="45bb8-187">YOY purchase growth</span></span>   | <span data-ttu-id="45bb8-188">Årlig kjøpsvekst = \[Kjøp inneværende år\] – \[Kjøp forrige år\]</span><span class="sxs-lookup"><span data-stu-id="45bb8-188">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="45bb8-189">Nøkkeldimensjonene nedenfor i innholdet brukes som filtre for å dele opp de aggregerte målingene, slik at du kan få flere detaljer og dypere analytisk innsikt.</span><span class="sxs-lookup"><span data-stu-id="45bb8-189">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="45bb8-190">Enhet</span><span class="sxs-lookup"><span data-stu-id="45bb8-190">Entity</span></span>                 | <span data-ttu-id="45bb8-191">Eksempler på attributter</span><span class="sxs-lookup"><span data-stu-id="45bb8-191">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="45bb8-192">Leverandører</span><span class="sxs-lookup"><span data-stu-id="45bb8-192">Vendors</span></span>                | <span data-ttu-id="45bb8-193">Leverandørgrupper, leverandørland eller områder, leverandørnavn</span><span class="sxs-lookup"><span data-stu-id="45bb8-193">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="45bb8-194">Produkter</span><span class="sxs-lookup"><span data-stu-id="45bb8-194">Products</span></span>               | <span data-ttu-id="45bb8-195">Produktnummer, produktnavn, navn på varegrupper</span><span class="sxs-lookup"><span data-stu-id="45bb8-195">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="45bb8-196">Innkjøpskategorier</span><span class="sxs-lookup"><span data-stu-id="45bb8-196">Procurement categories</span></span> | <span data-ttu-id="45bb8-197">Innkjøpskategori, navn på innkjøpskategori</span><span class="sxs-lookup"><span data-stu-id="45bb8-197">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="45bb8-198">Juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="45bb8-198">Legal entities</span></span>         | <span data-ttu-id="45bb8-199">Navn på juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="45bb8-199">Legal entity name</span></span>                                     |
| <span data-ttu-id="45bb8-200">Datoer</span><span class="sxs-lookup"><span data-stu-id="45bb8-200">Dates</span></span>                  | <span data-ttu-id="45bb8-201">Datoer, årsforskyvning</span><span class="sxs-lookup"><span data-stu-id="45bb8-201">Dates, Year offset</span></span>                                    |

<span data-ttu-id="45bb8-202">Som standard viser innholdspakkedataene for inneværende kalenderår.</span><span class="sxs-lookup"><span data-stu-id="45bb8-202">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="45bb8-203">Du kan imidlertid endre datofilteret i delen for rapportfiltre.</span><span class="sxs-lookup"><span data-stu-id="45bb8-203">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="45bb8-204">Du kan også endre firmafilteret.</span><span class="sxs-lookup"><span data-stu-id="45bb8-204">You can also change the company filter.</span></span>

