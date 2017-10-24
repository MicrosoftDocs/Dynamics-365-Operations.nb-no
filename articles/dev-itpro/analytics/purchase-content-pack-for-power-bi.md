---
title: "Kjøps- og forbruksanalyse-innhold for Power BI"
description: "Dette emnet beskriver hva som er inkludert i Kjøps- og forbruksanalyse-innhold for Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdet, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: FrankDahl
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3e42746329b1194c0ce0e2fb5c476742259a5b43
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="8acfe-104">Kjøps- og forbruksanalyse-innhold for Power BI</span><span class="sxs-lookup"><span data-stu-id="8acfe-104">Purchase spend analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8acfe-105">Dette emnet beskriver hva som er inkludert i **Kjøps- og forbruksanalyse**-innhold for Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="8acfe-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="8acfe-106">Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.</span><span class="sxs-lookup"><span data-stu-id="8acfe-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="8acfe-107">Oversikt</span><span class="sxs-lookup"><span data-stu-id="8acfe-107">Overview</span></span>

<span data-ttu-id="8acfe-108">**Kjøps- og forbruksanalyse**-innhold for Power BI ble utformet for å hjelpe innkjøpsledere og ledere som er ansvarlige for budsjetter, med å holde øye med kjøpsutgifter.</span><span class="sxs-lookup"><span data-stu-id="8acfe-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="8acfe-109">Ledere kan analysere kjøpsutgifter på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="8acfe-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="8acfe-110">Kjøp hittil i år (etter leverandørgruppe og enkeltleverandører, innkjøpskategori og enkeltprodukter og leverandørplassering)</span><span class="sxs-lookup"><span data-stu-id="8acfe-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="8acfe-111">Årlig kjøpsendring (etter leverandørgruppe og innkjøpkategori)</span><span class="sxs-lookup"><span data-stu-id="8acfe-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="8acfe-112">Innholdet bruker kjøpstransaksjonsdata, og gir både en aggregert visning av kjøpstall for hele selskapet og en analyse av kjøpsutgifter etter leverandør og vare.</span><span class="sxs-lookup"><span data-stu-id="8acfe-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="8acfe-113">Rapportene uthever endringer i kjøpsutgifter over tid.</span><span class="sxs-lookup"><span data-stu-id="8acfe-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="8acfe-114">Derfor kan de brukes til å varsle ledere om positive og negative utgiftstrender for individuelle leverandører og produkter.</span><span class="sxs-lookup"><span data-stu-id="8acfe-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="8acfe-115">I tillegg viser diagrammer kjøpsutgifter for forskjellige innkjøpskategorier og leverandørgrupper.</span><span class="sxs-lookup"><span data-stu-id="8acfe-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="8acfe-116">Kategori- og distriktsledere kan derfor bruke diagrammene til å identifisere endringer i forbruksatferd.</span><span class="sxs-lookup"><span data-stu-id="8acfe-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="8acfe-117">Tilgang til Power BI-innhold</span><span class="sxs-lookup"><span data-stu-id="8acfe-117">Accessing the Power BI content</span></span>
<span data-ttu-id="8acfe-118">Hvis du bruker Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017), vil **Kjøps- og forbruksanalyse** for Power BI-innholdet vises på siden **Kjøps- og forbruksanalyse** (**Innkjøp og sourcing** > **Forespørsler og rapporter** > **Prestasjonsanalyse for kjøp** > **Kjøps- og forbruksanalyse**).</span><span class="sxs-lookup"><span data-stu-id="8acfe-118">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), the **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="8acfe-119">Mål som er inkludert i Power BI-innholdet</span><span class="sxs-lookup"><span data-stu-id="8acfe-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="8acfe-120">**Kjøps- og forbruksanalyse**-innhold for Power BI inneholder en rapport som består av et sett med mål.</span><span class="sxs-lookup"><span data-stu-id="8acfe-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="8acfe-121">Disse målene vises som diagrammer, fliser og tabeller.</span><span class="sxs-lookup"><span data-stu-id="8acfe-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="8acfe-122">Tabellen nedenfor gir en oversikt over effektene.</span><span class="sxs-lookup"><span data-stu-id="8acfe-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8acfe-123">Rapportside</span><span class="sxs-lookup"><span data-stu-id="8acfe-123">Report page</span></span></th>
<th><span data-ttu-id="8acfe-124">Diagrammer</span><span class="sxs-lookup"><span data-stu-id="8acfe-124">Charts</span></span></th>
<th><span data-ttu-id="8acfe-125">Fliser</span><span class="sxs-lookup"><span data-stu-id="8acfe-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8acfe-126">Kjøp etter leverandør</span><span class="sxs-lookup"><span data-stu-id="8acfe-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="8acfe-127">De 10 viktigste leverandørene etter kjøp (stablet liggende stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="8acfe-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="8acfe-128">Totalt innkjøp etter leverandørgruppe / land / navn (sektordiagram)</span><span class="sxs-lookup"><span data-stu-id="8acfe-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="8acfe-129">Innkjøp etter leverandørgruppe / land / navn (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="8acfe-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="8acfe-130">Gjennomsnittlig innkjøp etter leverandørgruppe / land / navn (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="8acfe-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8acfe-131">Totale innkjøp</span><span class="sxs-lookup"><span data-stu-id="8acfe-131">Total purchase</span></span></li>
<li><span data-ttu-id="8acfe-132">Årlig innkjøpsvekst</span><span class="sxs-lookup"><span data-stu-id="8acfe-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="8acfe-133">Totalt antall leverandører</span><span class="sxs-lookup"><span data-stu-id="8acfe-133">Total # vendors</span></span></li>
<li><span data-ttu-id="8acfe-134">Totalt antall aktive leverandører</span><span class="sxs-lookup"><span data-stu-id="8acfe-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8acfe-135">Kjøp etter produkt</span><span class="sxs-lookup"><span data-stu-id="8acfe-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="8acfe-136">Kjøp etter innkjøpskategori / produktnavn (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="8acfe-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="8acfe-137">Totalt innkjøp etter innkjøpskategori / produktnavn (sektordiagram)</span><span class="sxs-lookup"><span data-stu-id="8acfe-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="8acfe-138">De 10 viktigste produktene etter kjøp (stablet liggende stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="8acfe-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8acfe-139">Totalt antall produkter</span><span class="sxs-lookup"><span data-stu-id="8acfe-139">Total # of products</span></span></li>
<li><span data-ttu-id="8acfe-140">Totalt antall aktive produktprosentdeler av totalt antall produkter</span><span class="sxs-lookup"><span data-stu-id="8acfe-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="8acfe-141">Antall produkter som står for 80 % av innkjøp</span><span class="sxs-lookup"><span data-stu-id="8acfe-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8acfe-142">Innkjøp etter periode*</span><span class="sxs-lookup"><span data-stu-id="8acfe-142">Purchase by period*</span></span></td>
<td><ul>
<li><span data-ttu-id="8acfe-143">Innkjøp etter måned / dag (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="8acfe-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="8acfe-144">Kumulativ årlig kjøpsavvik (fossefallsdiagram)</span><span class="sxs-lookup"><span data-stu-id="8acfe-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="8acfe-145">Totalt årlig kjøpsvekst (stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="8acfe-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="8acfe-146">Innkjøpsutdrag (matrise)</span><span class="sxs-lookup"><span data-stu-id="8acfe-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8acfe-147">Årlig innkjøpsvekst</span><span class="sxs-lookup"><span data-stu-id="8acfe-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="8acfe-148">Årlig innkjøpsvekst i %</span><span class="sxs-lookup"><span data-stu-id="8acfe-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8acfe-149">Kjøp etter leverandørplassering</span><span class="sxs-lookup"><span data-stu-id="8acfe-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="8acfe-150">Kjøp etter by</span><span class="sxs-lookup"><span data-stu-id="8acfe-150">Purchase by city</span></span></li>
<li><span data-ttu-id="8acfe-151">Årlig innkjøpsvekst i %</span><span class="sxs-lookup"><span data-stu-id="8acfe-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="8acfe-152">Kjøp etter land</span><span class="sxs-lookup"><span data-stu-id="8acfe-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8acfe-153">Kjøps- og forbruksanalyse etter tid</span><span class="sxs-lookup"><span data-stu-id="8acfe-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="8acfe-154">Kjøp inneværende år etter måned / dag (linjediagram)</span><span class="sxs-lookup"><span data-stu-id="8acfe-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="8acfe-155">Kjøp inneværende or forrige år (linjediagram og stående stolpediagram)</span><span class="sxs-lookup"><span data-stu-id="8acfe-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8acfe-156">Kjøps- og forbruksanalyse etter leverandør</span><span class="sxs-lookup"><span data-stu-id="8acfe-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="8acfe-157">De 10 viktigste leverandørkjøpene i % av kjøp (trakt)</span><span class="sxs-lookup"><span data-stu-id="8acfe-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="8acfe-158">De 10 viktigste leverandørene med økte årlige kjøp</span><span class="sxs-lookup"><span data-stu-id="8acfe-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="8acfe-159">De 10 viktigste leverandørene med reduserte årlige kjøp</span><span class="sxs-lookup"><span data-stu-id="8acfe-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8acfe-160">\* Innkjøp i år og forrige år. og vekst etter innkjøpskategori</span><span class="sxs-lookup"><span data-stu-id="8acfe-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="8acfe-161">Utvide Power BI-innholdet</span><span class="sxs-lookup"><span data-stu-id="8acfe-161">Extending the Power BI content</span></span>
<span data-ttu-id="8acfe-162">Hvis du bruker innholdspakkene som er tilgjengelige i Microsoft Dynamics Lifecycle Services (LCS), kan du gi personer som ikke logger på Microsoft Dynamics 365, gode analyser.</span><span class="sxs-lookup"><span data-stu-id="8acfe-162">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="8acfe-163">Du kan endre disse innholdspakkene slik at de inneholder andre rapporter eller visuelle hjelpemidler, og deretter publisere innholdspakkene på Power BI.com-leieren for analyse.</span><span class="sxs-lookup"><span data-stu-id="8acfe-163">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="8acfe-164">Du kan finne **Kjøps- og forbruksanalyse**-innholdet for Power BI i det delte aktivabiblioteket i LCS.</span><span class="sxs-lookup"><span data-stu-id="8acfe-164">You can find the **Purchase spend analysis** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="8acfe-165">Hvis du vil ha mer informasjon om hvordan du laster ned innholdet og implementerer det i organisasjonen, kan du se [Power BI-innhold i LCS fra Microsoft og partnerne](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="8acfe-165">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="8acfe-166">Hvis du vil se en demo som viser hvordan du implementerer Power BI-innholdet, kan du se [Power BI-innhold fra Microsoft og partnerne i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).</span><span class="sxs-lookup"><span data-stu-id="8acfe-166">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

<span data-ttu-id="8acfe-167">Pass på at du laster ned **Kjøps- og forbruksanalyse**-innholdet som gjelder for versjonen av Dynamics 365 du bruker.</span><span class="sxs-lookup"><span data-stu-id="8acfe-167">Be sure to download the **Purchase spend analysis** content that applies to the version of Dynamics 365 that you're using.</span></span>

> [!NOTE]
> <span data-ttu-id="8acfe-168">Hvis du bruker oppdateringen for Microsoft Dynamics 365 for Operations versjon 1611, er KB 4011327 en forutsetning for dette Power BI-innholdet.</span><span class="sxs-lookup"><span data-stu-id="8acfe-168">If you're using Microsoft Dynamics 365 for Operations version 1611, KB 4011327 is a prerequisite for this Power BI content.</span></span> <span data-ttu-id="8acfe-169">Når du logger deg på LCS, har du tilgang til KB-artikkelen på https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span><span class="sxs-lookup"><span data-stu-id="8acfe-169">After you sign in to LCS, you can access the KB at https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="8acfe-170">Datamodell og enheter</span><span class="sxs-lookup"><span data-stu-id="8acfe-170">Data model and entities</span></span>
<span data-ttu-id="8acfe-171">Følgende data brukes til å fylle ut rapportsidene i **Kjøps- og forbruksanalyse**-innholdet for Power BI.</span><span class="sxs-lookup"><span data-stu-id="8acfe-171">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="8acfe-172">Disse dataene vises som aggregerte mål som er oppsamlet i enhetslageret.</span><span class="sxs-lookup"><span data-stu-id="8acfe-172">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="8acfe-173">Enhetslageret er en Microsoft SQL Server-database som er optimalisert for analyse.</span><span class="sxs-lookup"><span data-stu-id="8acfe-173">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="8acfe-174">Hvis du vil ha mer informasjon, se [Oversikt over Power BI-integrering med enhetslager](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="8acfe-174">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="8acfe-175">De aggregerte målingene i denne innholdspakken er delsett av aggregerte målinger som var tilgjengelige i innkjøpskuben i Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="8acfe-175">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="8acfe-176">For å plassere kubens aggregerte målinger i enhetslageret må du gjøre dem distribuerbare.</span><span class="sxs-lookup"><span data-stu-id="8acfe-176">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="8acfe-177">Hvis du vil ha mer informasjon, kan du se fremgangsmåten for hvordan du plasserer aggregerte målinger i enhetsbutikken i blogginnlegget [Oversikt over Power BI-integrering med enhetslager](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="8acfe-177">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="8acfe-178">De aggregerte nøkkelmålingene er tilgjengelige direkte fra fakturalinjeenheten, og brukes som grunnlag for innholdet.</span><span class="sxs-lookup"><span data-stu-id="8acfe-178">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="8acfe-179">Enhet</span><span class="sxs-lookup"><span data-stu-id="8acfe-179">Entity</span></span>        | <span data-ttu-id="8acfe-180">Aggregerte nøkkelmålinger</span><span class="sxs-lookup"><span data-stu-id="8acfe-180">Key aggregate measurements</span></span> | <span data-ttu-id="8acfe-181">Datakilde</span><span class="sxs-lookup"><span data-stu-id="8acfe-181">Data source</span></span>                                 | <span data-ttu-id="8acfe-182">Felt</span><span class="sxs-lookup"><span data-stu-id="8acfe-182">Field</span></span>              | <span data-ttu-id="8acfe-183">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="8acfe-183">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="8acfe-184">Fakturalinjer</span><span class="sxs-lookup"><span data-stu-id="8acfe-184">Invoice lines</span></span> | <span data-ttu-id="8acfe-185">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="8acfe-185">Purchase</span></span>                   | <span data-ttu-id="8acfe-186">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="8acfe-186">VendInvoiceTrans</span></span>                            | <span data-ttu-id="8acfe-187">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="8acfe-187">SUM(LineAmountMST)</span></span> | <span data-ttu-id="8acfe-188">Beløpet i regnskapsvaluta</span><span class="sxs-lookup"><span data-stu-id="8acfe-188">The amount in the accounting currency.</span></span> |

<span data-ttu-id="8acfe-189">Tabellen nedenfor viser viktige målinger som beregnes i innholdet fra fakturalinjeenheten.</span><span class="sxs-lookup"><span data-stu-id="8acfe-189">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="8acfe-190">Mål</span><span class="sxs-lookup"><span data-stu-id="8acfe-190">Measure</span></span>               | <span data-ttu-id="8acfe-191">Beregning</span><span class="sxs-lookup"><span data-stu-id="8acfe-191">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8acfe-192">Kjøp inneværende år</span><span class="sxs-lookup"><span data-stu-id="8acfe-192">Purchase current year</span></span> | <span data-ttu-id="8acfe-193">Kjøp inneværende år = SUM('Fakturalinjer'\[Kjøp\])</span><span class="sxs-lookup"><span data-stu-id="8acfe-193">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="8acfe-194">Kjøp forrige år</span><span class="sxs-lookup"><span data-stu-id="8acfe-194">Purchase last year</span></span>    | <span data-ttu-id="8acfe-195">Kjøp forrige år = CALCULATE(SUM('Fakturalinjer'\[Kjøp\]), SAMEPERIODLASTYEAR((Datoer\[Dato\]))</span><span class="sxs-lookup"><span data-stu-id="8acfe-195">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="8acfe-196">Årlig innkjøpsvekst</span><span class="sxs-lookup"><span data-stu-id="8acfe-196">YOY purchase growth</span></span>   | <span data-ttu-id="8acfe-197">Årlig kjøpsvekst = \[Kjøp inneværende år\] – \[Kjøp forrige år\]</span><span class="sxs-lookup"><span data-stu-id="8acfe-197">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="8acfe-198">Nøkkeldimensjonene nedenfor i innholdet brukes som filtre for å dele opp de aggregerte målingene, slik at du kan få flere detaljer og dypere analytisk innsikt.</span><span class="sxs-lookup"><span data-stu-id="8acfe-198">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="8acfe-199">Enhet</span><span class="sxs-lookup"><span data-stu-id="8acfe-199">Entity</span></span>                 | <span data-ttu-id="8acfe-200">Eksempler på attributter</span><span class="sxs-lookup"><span data-stu-id="8acfe-200">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="8acfe-201">Leverandører</span><span class="sxs-lookup"><span data-stu-id="8acfe-201">Vendors</span></span>                | <span data-ttu-id="8acfe-202">Leverandørgrupper, leverandørland eller områder, leverandørnavn</span><span class="sxs-lookup"><span data-stu-id="8acfe-202">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="8acfe-203">Produkter</span><span class="sxs-lookup"><span data-stu-id="8acfe-203">Products</span></span>               | <span data-ttu-id="8acfe-204">Produktnummer, produktnavn, navn på varegrupper</span><span class="sxs-lookup"><span data-stu-id="8acfe-204">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="8acfe-205">Innkjøpskategorier</span><span class="sxs-lookup"><span data-stu-id="8acfe-205">Procurement categories</span></span> | <span data-ttu-id="8acfe-206">Innkjøpskategori, navn på innkjøpskategori</span><span class="sxs-lookup"><span data-stu-id="8acfe-206">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="8acfe-207">Juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="8acfe-207">Legal entities</span></span>         | <span data-ttu-id="8acfe-208">Navn på juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="8acfe-208">Legal entity name</span></span>                                     |
| <span data-ttu-id="8acfe-209">Datoer</span><span class="sxs-lookup"><span data-stu-id="8acfe-209">Dates</span></span>                  | <span data-ttu-id="8acfe-210">Datoer, årsforskyvning</span><span class="sxs-lookup"><span data-stu-id="8acfe-210">Dates, Year offset</span></span>                                    |

<span data-ttu-id="8acfe-211">Som standard viser innholdspakkedataene for inneværende kalenderår.</span><span class="sxs-lookup"><span data-stu-id="8acfe-211">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="8acfe-212">Du kan imidlertid endre datofilteret i delen for rapportfiltre.</span><span class="sxs-lookup"><span data-stu-id="8acfe-212">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="8acfe-213">Du kan også endre firmafilteret.</span><span class="sxs-lookup"><span data-stu-id="8acfe-213">You can also change the company filter.</span></span>

