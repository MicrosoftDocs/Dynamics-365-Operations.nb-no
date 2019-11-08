---
title: Oversikt over kvalitetsstyring
description: Dette emnet beskriver hvordan du kan bruke kvalitetsstyring i Dynamics 365 Supply Chain Management for å forbedre produktkvalitet i forsyningskjeden.
author: perlynne
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba38f9c43fed81768155a27dda88a4bfb4a7828e
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653562"
---
# <a name="quality-management-overview"></a><span data-ttu-id="cd563-103">Oversikt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="cd563-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd563-104">Dette emnet beskriver hvordan du kan bruke kvalitetsstyring i Dynamics 365 Supply Chain Management for å forbedre produktkvalitet i forsyningskjeden.</span><span class="sxs-lookup"><span data-stu-id="cd563-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="cd563-105">Kvalitetsstyring kan hjelpe deg med å administrere behandlingstiden når du håndterer produkter med avvik, uavhengig av opprinnelsespunktet.</span><span class="sxs-lookup"><span data-stu-id="cd563-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="cd563-106">Fordi diagnosetyper er knyttet til rettelsesrapportering, kan Supply Chain Management planlegge oppgaver for å rette opp problemer og hindre at de skjer igjen.</span><span class="sxs-lookup"><span data-stu-id="cd563-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="cd563-107">I tillegg til funksjonalitet for håndtering av avvik inneholder kvalitetsstyring funksjonalitet for å spore problemer etter problemtype (selv interne problemer) og identifisere løsninger som kortsiktige eller langsiktige.</span><span class="sxs-lookup"><span data-stu-id="cd563-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="cd563-108">Statistikk om nøkkelytelsesindikator (KPI-er) gir innsikt i loggen for tidligere avviksproblemer og løsninger som ble brukt til å rette feilene.</span><span class="sxs-lookup"><span data-stu-id="cd563-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="cd563-109">Du kan bruke historiske data for å undersøke effektiviteten til tidligere kvalitetsmål og bestemme nødvendige tiltak som skal brukes i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="cd563-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="cd563-110">Når du definerer en kvalitetstilknytning, kan Supply Chain Management generere kvalitetsordrer for diverse forretningsprosesser, hendelser og betingelser.</span><span class="sxs-lookup"><span data-stu-id="cd563-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="cd563-111">Kvalitetstilknytningen kan dekke en bestemt vare, en bestemt varegruppe eller alle varer.</span><span class="sxs-lookup"><span data-stu-id="cd563-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="cd563-112">Eksempler på bruk av kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="cd563-112">Examples of the use of quality management</span></span>
<span data-ttu-id="cd563-113">Kvalitetsstyring er fleksibelt og kan implementeres på forskjellige måter for å oppfylle kravene til bestemte typer forsyningskjedeoperasjoner.</span><span class="sxs-lookup"><span data-stu-id="cd563-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="cd563-114">Følgende eksempel viser mulig bruk av disse funksjonene.</span><span class="sxs-lookup"><span data-stu-id="cd563-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="cd563-115">Start en prosess for kvalitetskontroll automatisk basert på forhåndsdefinerte kriterier (ved lagerregistrering av en bestilling fra en bestemt leverandør).</span><span class="sxs-lookup"><span data-stu-id="cd563-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="cd563-116">Blokker lageret under inspeksjon for å hindre bruk av ikke-godkjent lager (full blokkering av bestillingsantall).</span><span class="sxs-lookup"><span data-stu-id="cd563-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="cd563-117">Bruk vareprøver som en del av en kvalitetstilknytning for å definere hvor mye av det fysiske lageret som må kontrolleres.</span><span class="sxs-lookup"><span data-stu-id="cd563-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="cd563-118">Prøver kan være basert på faste antall eller en prosentdel.</span><span class="sxs-lookup"><span data-stu-id="cd563-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="cd563-119">Opprette kvalitetsordrer for delvise mottak.</span><span class="sxs-lookup"><span data-stu-id="cd563-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="cd563-120">Hvis du vil opprette en kvalitetsordre som er basert på antallet som er fysisk mottatt med en ordre, må du velge den **Per oppdatert mengde** for den **Vareprøve** skjema.</span><span class="sxs-lookup"><span data-stu-id="cd563-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="cd563-121">Opprett testtyper med minimums-, maksimums-, og måltestverdier, og utfør kvalitative kontra kvantitative tester som har forhåndsdefinerte valideringsresultater.</span><span class="sxs-lookup"><span data-stu-id="cd563-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="cd563-122">Angi et akseptabelt kvalitetsnivå for å kontrollere kvalitetsmåltoleranser.</span><span class="sxs-lookup"><span data-stu-id="cd563-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="cd563-123">Angi ressursene som en inspeksjonsoperasjon krever, for eksempel et testområde og testinstrumenter.</span><span class="sxs-lookup"><span data-stu-id="cd563-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="cd563-124">Arbeide med kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="cd563-124">Working with quality associations</span></span>
<span data-ttu-id="cd563-125">Forretningsprosessen som bruker en kvalitetstilknytning, kan knyttes til ulike kildedokumenter, for eksempel bestillinger, salgsordrer eller produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="cd563-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="cd563-126">Hver kvalitetstilknytningspost definerer settet med tester, det akseptable kvalitetsnivået og samplingplanen som gjelder for kvalitetsordrene som genereres.</span><span class="sxs-lookup"><span data-stu-id="cd563-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="cd563-127">Du må definere en kvalitetstilknytningspost for hver variasjon i en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="cd563-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="cd563-128">Du kan for eksempel definere en kvalitetstilknytning som genererer en kvalitetsordre når et produkt for bestillingsmottak oppdateres.</span><span class="sxs-lookup"><span data-stu-id="cd563-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="cd563-129">Avhengig av oppsettet for utførelsesplanen kan selve utløsingsprosessen blokkeres når det finnes en åpen kvalitetsordre, eller de neste prosessene, for eksempel bestillingsfakturering, kan blokkeres.</span><span class="sxs-lookup"><span data-stu-id="cd563-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="cd563-130">**Merk:** Når det finnes åpne kvalitetsordrer, blokkeres lagerantall automatisk fra å bli utstedt.</span><span class="sxs-lookup"><span data-stu-id="cd563-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="cd563-131">Avhengig av **Full blokkering**-innstillingen på siden **Vareprøver** er antallet enten antallet på kvalitetsordren eller antallet på kildedokumentlinjen.</span><span class="sxs-lookup"><span data-stu-id="cd563-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="cd563-132">For en gitt forretningsprosess identifiserer kvalitetstilknytningspost hendelsen og betingelsene som en kvalitetsordre genereres for.</span><span class="sxs-lookup"><span data-stu-id="cd563-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="cd563-133">Betingelsene kan være spesifikke for et område eller en juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="cd563-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="cd563-134">En kvalitetsordre som omfatter destruktive tester, kan bare genereres når hvis det finnes lagerbeholdning for hendelsen.</span><span class="sxs-lookup"><span data-stu-id="cd563-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="cd563-135">De følgende eksemplene illustrerer hvordan en kvalitetstilknytningspost er definert for variasjonene innen ulike forretningsprosesser.</span><span class="sxs-lookup"><span data-stu-id="cd563-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="cd563-136">For hvert eksempel oppsummere følgende tabell hendelsene og betingelsene som er definert av en kvalitetstilknytningspost.</span><span class="sxs-lookup"><span data-stu-id="cd563-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="cd563-137">Referansetype</span><span class="sxs-lookup"><span data-stu-id="cd563-137">Reference type</span></span></th>
<th><span data-ttu-id="cd563-138">Hendelsestype</span><span class="sxs-lookup"><span data-stu-id="cd563-138">Event type</span></span></th>
<th><span data-ttu-id="cd563-139">Utførelse</span><span class="sxs-lookup"><span data-stu-id="cd563-139">Execution</span></span></th>
<th><span data-ttu-id="cd563-140">Hendelsesblokkering</span><span class="sxs-lookup"><span data-stu-id="cd563-140">Event blocking</span></span></th>
<th><span data-ttu-id="cd563-141">Dokumentreferanse</span><span class="sxs-lookup"><span data-stu-id="cd563-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="cd563-142">Beholdning</span><span class="sxs-lookup"><span data-stu-id="cd563-142">Inventory</span></span></td>
<td><span data-ttu-id="cd563-143">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="cd563-143">Not applicable</span></span></td>
<td><span data-ttu-id="cd563-144">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="cd563-144">Not applicable</span></span></td>
<td><span data-ttu-id="cd563-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="cd563-145">None</span></span></td>
<td><span data-ttu-id="cd563-146">Alle</span><span class="sxs-lookup"><span data-stu-id="cd563-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="cd563-147">Salg</span><span class="sxs-lookup"><span data-stu-id="cd563-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="cd563-148">Plukkingsprosess er planlagt</span><span class="sxs-lookup"><span data-stu-id="cd563-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="cd563-149">Før</span><span class="sxs-lookup"><span data-stu-id="cd563-149">Before</span></span></td>
<td><span data-ttu-id="cd563-150">Ingen</span><span class="sxs-lookup"><span data-stu-id="cd563-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="cd563-151">Bare Spesifikk ID, Gruppe eller Alle</span><span class="sxs-lookup"><span data-stu-id="cd563-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-152">Plukkingsprosess</span><span class="sxs-lookup"><span data-stu-id="cd563-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-153">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="cd563-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-154">Faktura</span><span class="sxs-lookup"><span data-stu-id="cd563-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cd563-155">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="cd563-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="cd563-156">Før</span><span class="sxs-lookup"><span data-stu-id="cd563-156">Before</span></span></td>
<td><span data-ttu-id="cd563-157">Ingen</span><span class="sxs-lookup"><span data-stu-id="cd563-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-158">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="cd563-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-159">Faktura</span><span class="sxs-lookup"><span data-stu-id="cd563-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="cd563-160">Kjøp</span><span class="sxs-lookup"><span data-stu-id="cd563-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="cd563-161">Kvitteringsliste</span><span class="sxs-lookup"><span data-stu-id="cd563-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="cd563-162">Før</span><span class="sxs-lookup"><span data-stu-id="cd563-162">Before</span></span></td>
<td><span data-ttu-id="cd563-163">Ingen</span><span class="sxs-lookup"><span data-stu-id="cd563-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-164">Kvitteringsliste</span><span class="sxs-lookup"><span data-stu-id="cd563-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-165">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="cd563-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-166">Faktura</span><span class="sxs-lookup"><span data-stu-id="cd563-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cd563-167">Etter</span><span class="sxs-lookup"><span data-stu-id="cd563-167">After</span></span></td>
<td><span data-ttu-id="cd563-168">Ingen</span><span class="sxs-lookup"><span data-stu-id="cd563-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-169">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="cd563-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-170">Faktura</span><span class="sxs-lookup"><span data-stu-id="cd563-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cd563-171">Registrering</span><span class="sxs-lookup"><span data-stu-id="cd563-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="cd563-172">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="cd563-172">Not applicable</span></span></td>
<td><span data-ttu-id="cd563-173">Ingen</span><span class="sxs-lookup"><span data-stu-id="cd563-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-174">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="cd563-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-175">Faktura</span><span class="sxs-lookup"><span data-stu-id="cd563-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="cd563-176">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="cd563-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="cd563-177">Før</span><span class="sxs-lookup"><span data-stu-id="cd563-177">Before</span></span></td>
<td><span data-ttu-id="cd563-178">Ingen</span><span class="sxs-lookup"><span data-stu-id="cd563-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-179">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="cd563-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-180">Faktura</span><span class="sxs-lookup"><span data-stu-id="cd563-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cd563-181">Etter</span><span class="sxs-lookup"><span data-stu-id="cd563-181">After</span></span></td>
<td><span data-ttu-id="cd563-182">Ingen</span><span class="sxs-lookup"><span data-stu-id="cd563-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-183">Faktura</span><span class="sxs-lookup"><span data-stu-id="cd563-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="cd563-184">Produksjon</span><span class="sxs-lookup"><span data-stu-id="cd563-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="cd563-185">Registrering</span><span class="sxs-lookup"><span data-stu-id="cd563-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="cd563-186">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="cd563-186">Not applicable</span></span></td>
<td><span data-ttu-id="cd563-187">Ingen</span><span class="sxs-lookup"><span data-stu-id="cd563-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="cd563-188">Alle</span><span class="sxs-lookup"><span data-stu-id="cd563-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-189">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="cd563-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-190">Slutt</span><span class="sxs-lookup"><span data-stu-id="cd563-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="cd563-191">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="cd563-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="cd563-192">Før</span><span class="sxs-lookup"><span data-stu-id="cd563-192">Before</span></span></td>
<td><span data-ttu-id="cd563-193">Ingen</span><span class="sxs-lookup"><span data-stu-id="cd563-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-194">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="cd563-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-195">Slutt</span><span class="sxs-lookup"><span data-stu-id="cd563-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cd563-196">Etter</span><span class="sxs-lookup"><span data-stu-id="cd563-196">After</span></span></td>
<td><span data-ttu-id="cd563-197">Ingen</span><span class="sxs-lookup"><span data-stu-id="cd563-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-198">Slutt</span><span class="sxs-lookup"><span data-stu-id="cd563-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="cd563-199">Karantene</span><span class="sxs-lookup"><span data-stu-id="cd563-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="cd563-200">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="cd563-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="cd563-201">Før</span><span class="sxs-lookup"><span data-stu-id="cd563-201">Before</span></span></td>
<td><span data-ttu-id="cd563-202">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="cd563-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-203">Slutt</span><span class="sxs-lookup"><span data-stu-id="cd563-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-204">Etter</span><span class="sxs-lookup"><span data-stu-id="cd563-204">After</span></span></td>
<td><span data-ttu-id="cd563-205">Slutt</span><span class="sxs-lookup"><span data-stu-id="cd563-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-206">Slutt</span><span class="sxs-lookup"><span data-stu-id="cd563-206">End</span></span></td>
<td><span data-ttu-id="cd563-207">Før</span><span class="sxs-lookup"><span data-stu-id="cd563-207">Before</span></span></td>
<td><span data-ttu-id="cd563-208">Slutt</span><span class="sxs-lookup"><span data-stu-id="cd563-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cd563-209">Ruteoperasjon</span><span class="sxs-lookup"><span data-stu-id="cd563-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="cd563-210">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="cd563-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="cd563-211">Før</span><span class="sxs-lookup"><span data-stu-id="cd563-211">Before</span></span></td>
<td><span data-ttu-id="cd563-212">Ingen</span><span class="sxs-lookup"><span data-stu-id="cd563-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="cd563-213">Bestemt ID, Gruppe eller Alle, og Ressursspesifikk, Gruppe eller Alle</span><span class="sxs-lookup"><span data-stu-id="cd563-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-214">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="cd563-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-215">Etter</span><span class="sxs-lookup"><span data-stu-id="cd563-215">After</span></span></td>
<td><span data-ttu-id="cd563-216">Ingen</span><span class="sxs-lookup"><span data-stu-id="cd563-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cd563-217">Koproduktproduksjon</span><span class="sxs-lookup"><span data-stu-id="cd563-217">Co-product production</span></span></td>
<td><span data-ttu-id="cd563-218">Registrering</span><span class="sxs-lookup"><span data-stu-id="cd563-218">Registration</span></span></td>
<td><span data-ttu-id="cd563-219">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="cd563-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cd563-220">Ingen</span><span class="sxs-lookup"><span data-stu-id="cd563-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="cd563-221">Alle</span><span class="sxs-lookup"><span data-stu-id="cd563-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cd563-222">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="cd563-222">Report as finished</span></span></td>
<td><span data-ttu-id="cd563-223">Før</span><span class="sxs-lookup"><span data-stu-id="cd563-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-224">Etter</span><span class="sxs-lookup"><span data-stu-id="cd563-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cd563-225">Tabellen nedenfor inneholder mer informasjon om hvordan kvalitetsordrer kan genereres for bestemte typer prosesser.</span><span class="sxs-lookup"><span data-stu-id="cd563-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="cd563-226">Type av prosess</span><span class="sxs-lookup"><span data-stu-id="cd563-226">Type of process</span></span></th>
<th><span data-ttu-id="cd563-227">Når kvalitetsordrer kan genereres automatisk</span><span class="sxs-lookup"><span data-stu-id="cd563-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="cd563-228">Når kvalitetsordrer kan genereres hvis destruktiv testing kreves</span><span class="sxs-lookup"><span data-stu-id="cd563-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="cd563-229">Betingelsesinformasjon</span><span class="sxs-lookup"><span data-stu-id="cd563-229">Condition information</span></span></th>
<th><span data-ttu-id="cd563-230">Informasjon om manuell generering</span><span class="sxs-lookup"><span data-stu-id="cd563-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="cd563-231">Bestilling</span><span class="sxs-lookup"><span data-stu-id="cd563-231">Purchase order</span></span></td>
<td><span data-ttu-id="cd563-232">Før eller etter en kvitteringsliste eller produktkvittering for materialet som mottas, posteres</span><span class="sxs-lookup"><span data-stu-id="cd563-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="cd563-233">Etter produktkvitteringen for materialet som mottas, er postert, fordi materialet må være tilgjengelig for destruktiv testing</span><span class="sxs-lookup"><span data-stu-id="cd563-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="cd563-234">Behovet for en kvalitetsordre kan reflektere et bestemt område, en vare, en leverandør eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="cd563-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="cd563-235">En manuelt generert kvalitetsordre som viser til en bestilling, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="cd563-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-236">Karanteneordre</span><span class="sxs-lookup"><span data-stu-id="cd563-236">Quarantine order</span></span></td>
<td><span data-ttu-id="cd563-237">Før eller etter karanteordren er rapportert som fullført eller avsluttet</span><span class="sxs-lookup"><span data-stu-id="cd563-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="cd563-238">Kvalitetsordrer som krever destruktive tester, kan ikke genereres.</span><span class="sxs-lookup"><span data-stu-id="cd563-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="cd563-239">Det forutsettes at karanteneordrefunksjonaliteten behandler disposisjonen av materialet som blir ødelagt.</span><span class="sxs-lookup"><span data-stu-id="cd563-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="cd563-240">Behovet for en kvalitetsordre kan reflektere et bestemt område, en vare, en leverandør eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="cd563-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="cd563-241">En manuelt generert kvalitetsordre som viser til en karanteneordre, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="cd563-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-242">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="cd563-242">Sales order</span></span></td>
<td><span data-ttu-id="cd563-243">Før en planlagt plukkeprosessen eller følgeseddeloppdatering for varene som leveres</span><span class="sxs-lookup"><span data-stu-id="cd563-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="cd563-244">I alle trinn</span><span class="sxs-lookup"><span data-stu-id="cd563-244">At any step</span></span></td>
<td><span data-ttu-id="cd563-245">Kravet til en kvalitetsordre kan reflektere et bestemt område, en vare, en kunde eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="cd563-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="cd563-246">En manuelt generert kvalitetsordre som viser til en salgsordre, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="cd563-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-247">Produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="cd563-247">Production order</span></span></td>
<td><span data-ttu-id="cd563-248">Før eller etter den ferdige kvaliteten for produksjonsordren er rapportert</span><span class="sxs-lookup"><span data-stu-id="cd563-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="cd563-249">Etter den ferdige kvaliteten for produksjonsordren er rapportert</span><span class="sxs-lookup"><span data-stu-id="cd563-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="cd563-250">Behovet for en kvalitetsordre kan reflektere et bestemt område eller en vare, eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="cd563-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="cd563-251">En manuelt generert kvalitetsordre som viser til en produksjonsordre, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="cd563-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-252">Produksjonsordre som har en ruteoperasjon</span><span class="sxs-lookup"><span data-stu-id="cd563-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="cd563-253">Før eller etter at rapporten for en operasjon er fullført</span><span class="sxs-lookup"><span data-stu-id="cd563-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="cd563-254">Etter at rapporteringen av produksjonen er fullført for den siste operasjonen</span><span class="sxs-lookup"><span data-stu-id="cd563-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="cd563-255">Behovet for en kvalitetsordre kan reflektere et bestemt område, en vare eller en operasjonsressurs eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="cd563-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="cd563-256">En manuelt generert kvalitetsordre som viser til en ruteoperasjon, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="cd563-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd563-257">Beholdning</span><span class="sxs-lookup"><span data-stu-id="cd563-257">Inventory</span></span></td>
<td><span data-ttu-id="cd563-258">En kvalitetsordre kan ikke genereres automatisk for en transaksjon innen en lagerjournal eller for overføringsordretransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="cd563-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="cd563-259">En kvalitetsordre må opprettes manuelt for en vares lagerantall.</span><span class="sxs-lookup"><span data-stu-id="cd563-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="cd563-260">Varens fysiske lagerbeholdning kreves.</span><span class="sxs-lookup"><span data-stu-id="cd563-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="cd563-261">Eksempler på automatisk generering av kvalitetsordre</span><span class="sxs-lookup"><span data-stu-id="cd563-261">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="cd563-262">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="cd563-262">Purchasing</span></span>

<span data-ttu-id="cd563-263">I innkjøp, hvis du du angir feltet **Hendelsestype** til **Produktkvittering** og feltet **Utførelse** til **Etter** på siden **Kvalitetstilknytninger**, får du følgende resultater:</span><span class="sxs-lookup"><span data-stu-id="cd563-263">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="cd563-264">Hvis alternativet **Per oppdatert mengde** er satt til **Ja**, genereres det en kvalitetsordre for hvert mottak mot bestillingen basert på det mottatte antallet og innstillingene i vareprøven.</span><span class="sxs-lookup"><span data-stu-id="cd563-264">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="cd563-265">Hver gang et antall mottas mot bestillingen, genereres nye kvalitetsordrer basert på det nylig mottatte antallet.</span><span class="sxs-lookup"><span data-stu-id="cd563-265">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="cd563-266">Hvis alternativet **Per oppdatert mengde** er satt til **Nei**, genereres det en kvalitetsordre for det første mottaket mot bestillingen basert på det mottatte antallet.</span><span class="sxs-lookup"><span data-stu-id="cd563-266">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="cd563-267">I tillegg blir én eller flere kvalitetsordrer opprettet på grunnlag av restantallet, avhengig av sporingsdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="cd563-267">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="cd563-268">Kvalitetsordrer genereres ikke for etterfølgende mottak mot bestillingen.</span><span class="sxs-lookup"><span data-stu-id="cd563-268">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="cd563-269">Kvalitetsspesifikasjon</span><span class="sxs-lookup"><span data-stu-id="cd563-269">Quality specification</span></span></th>
<th><span data-ttu-id="cd563-270">Per oppdatert mengde</span><span class="sxs-lookup"><span data-stu-id="cd563-270">Per updated quantity</span></span></th>
<th><span data-ttu-id="cd563-271">Per sporingsdimensjon</span><span class="sxs-lookup"><span data-stu-id="cd563-271">Per tracking dimension</span></span></th>
<th><span data-ttu-id="cd563-272">Resultat</span><span class="sxs-lookup"><span data-stu-id="cd563-272">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="cd563-273">Prosent: 10 %</span><span class="sxs-lookup"><span data-stu-id="cd563-273">Percentage: 10%</span></span></td>
<td><span data-ttu-id="cd563-274">Ja</span><span class="sxs-lookup"><span data-stu-id="cd563-274">Yes</span></span></td>
<td>
<p><span data-ttu-id="cd563-275">Partinummer: Nei</span><span class="sxs-lookup"><span data-stu-id="cd563-275">Batch number: No</span></span></p>
<p><span data-ttu-id="cd563-276">Serienummer: Nei</span><span class="sxs-lookup"><span data-stu-id="cd563-276">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="cd563-277">Ordreantall: 100</span><span class="sxs-lookup"><span data-stu-id="cd563-277">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="cd563-278">Rapporter som ferdig for 30</span><span class="sxs-lookup"><span data-stu-id="cd563-278">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="cd563-279">Kvalitetsordre #1 for 3 (10 % av 30)</span><span class="sxs-lookup"><span data-stu-id="cd563-279">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="cd563-280">Rapporter som ferdig for 70</span><span class="sxs-lookup"><span data-stu-id="cd563-280">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="cd563-281">Kvalitetsordre #2 for 7 (10 % av restordreantallet, som er lik 70 i dette tilfellet)</span><span class="sxs-lookup"><span data-stu-id="cd563-281">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="cd563-282">Fast antall: 1</span><span class="sxs-lookup"><span data-stu-id="cd563-282">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="cd563-283">Nei</span><span class="sxs-lookup"><span data-stu-id="cd563-283">No</span></span></td>
<td>
<p><span data-ttu-id="cd563-284">Partinummer: Nei</span><span class="sxs-lookup"><span data-stu-id="cd563-284">Batch number: No</span></span></p>
<p><span data-ttu-id="cd563-285">Serienummer: Nei</span><span class="sxs-lookup"><span data-stu-id="cd563-285">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="cd563-286">Ordreantall: 100</span><span class="sxs-lookup"><span data-stu-id="cd563-286">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="cd563-287">Rapporter som ferdig for 30</span><span class="sxs-lookup"><span data-stu-id="cd563-287">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="cd563-288">Kvalitetsordre #1 opprettes for 1 (for det første ferdigmeldte antallet, som har en fast verdi på 1).</span><span class="sxs-lookup"><span data-stu-id="cd563-288">Quality order #1 is created for 1 (for the first reported-as-finished quantity, which has a fixed value of 1).</span></span></li>
<li><span data-ttu-id="cd563-289">Det opprettes ingen flere kvalitetsordrer mot restantallet.</span><span class="sxs-lookup"><span data-stu-id="cd563-289">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="cd563-290">Rapporter som ferdig for 10</span><span class="sxs-lookup"><span data-stu-id="cd563-290">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="cd563-291">Ingen kvalitetsordrer er opprettet.</span><span class="sxs-lookup"><span data-stu-id="cd563-291">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="cd563-292">Rapporter som ferdig for 60</span><span class="sxs-lookup"><span data-stu-id="cd563-292">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="cd563-293">Ingen kvalitetsordrer er opprettet.</span><span class="sxs-lookup"><span data-stu-id="cd563-293">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="cd563-294">Fast antall: 1</span><span class="sxs-lookup"><span data-stu-id="cd563-294">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="cd563-295">Ja</span><span class="sxs-lookup"><span data-stu-id="cd563-295">Yes</span></span></td>
<td>
<p><span data-ttu-id="cd563-296">Partinummer: Ja</span><span class="sxs-lookup"><span data-stu-id="cd563-296">Batch number: Yes</span></span></p>
<p><span data-ttu-id="cd563-297">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="cd563-297">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="cd563-298">Ordreantall: 10</span><span class="sxs-lookup"><span data-stu-id="cd563-298">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="cd563-299">Rapporter som ferdig for 3</span><span class="sxs-lookup"><span data-stu-id="cd563-299">Report as finished for 3</span></span>
<ul>
<li><span data-ttu-id="cd563-300">Kvalitetsordre #1 for 1 av parti #b1, serie #s1</span><span class="sxs-lookup"><span data-stu-id="cd563-300">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="cd563-301">Kvalitetsordre #2 for 1 av parti #b2, serie #s2</span><span class="sxs-lookup"><span data-stu-id="cd563-301">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="cd563-302">Kvalitetsordre #3 for 1 av parti #b3, serie #s3</span><span class="sxs-lookup"><span data-stu-id="cd563-302">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="cd563-303">Rapporter som ferdig for 2</span><span class="sxs-lookup"><span data-stu-id="cd563-303">Report as finished for 2</span></span>
<ul>
<li><span data-ttu-id="cd563-304">Kvalitetsordre #4 for 1 av parti #b4, serie #s4</span><span class="sxs-lookup"><span data-stu-id="cd563-304">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="cd563-305">Kvalitetsordre #5 for 1 av parti #b5, serie #s5</span><span class="sxs-lookup"><span data-stu-id="cd563-305">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="cd563-306"><strong>Merk:</strong> Partiet kan brukes på nytt.</span><span class="sxs-lookup"><span data-stu-id="cd563-306"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="cd563-307">Fast antall: 2</span><span class="sxs-lookup"><span data-stu-id="cd563-307">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="cd563-308">Nei</span><span class="sxs-lookup"><span data-stu-id="cd563-308">No</span></span></td>
<td>
<p><span data-ttu-id="cd563-309">Partinummer: Ja</span><span class="sxs-lookup"><span data-stu-id="cd563-309">Batch number: Yes</span></span></p>
<p><span data-ttu-id="cd563-310">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="cd563-310">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="cd563-311">Ordreantall: 10</span><span class="sxs-lookup"><span data-stu-id="cd563-311">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="cd563-312">Rapporter som ferdig for 4</span><span class="sxs-lookup"><span data-stu-id="cd563-312">Report as finished for 4</span></span>
<ul>
<li><span data-ttu-id="cd563-313">Kvalitetsordre #1 for 1 av parti #b1, serie #s1.</span><span class="sxs-lookup"><span data-stu-id="cd563-313">Quality order #1 for 1 of batch #b1, serial #s1.</span></span></li>
<li><span data-ttu-id="cd563-314">Kvalitetsordre #2 for 1 av parti #b2, serie #s2.</span><span class="sxs-lookup"><span data-stu-id="cd563-314">Quality order #2 for 1 of batch #b2, serial #s2.</span></span></li>
<li><span data-ttu-id="cd563-315">Kvalitetsordre #3 for 1 av parti #b3, serie #s3.</span><span class="sxs-lookup"><span data-stu-id="cd563-315">Quality order #3 for 1 of batch #b3, serial #s3.</span></span></li>
<li><span data-ttu-id="cd563-316">Kvalitetsordre #4 for 1 av parti #b4, serie #s4.</span><span class="sxs-lookup"><span data-stu-id="cd563-316">Quality order #4 for 1 of batch #b4, serial #s4.</span></span></li>
<li><span data-ttu-id="cd563-317">Det opprettes ingen flere kvalitetsordrer mot restantallet.</span><span class="sxs-lookup"><span data-stu-id="cd563-317">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="cd563-318">Rapporter som ferdig for 6</span><span class="sxs-lookup"><span data-stu-id="cd563-318">Report as finished for 6</span></span>
<ul>
<li><span data-ttu-id="cd563-319">Ingen kvalitetsordrer er opprettet.</span><span class="sxs-lookup"><span data-stu-id="cd563-319">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="production"></a><span data-ttu-id="cd563-320">Produksjon</span><span class="sxs-lookup"><span data-stu-id="cd563-320">Production</span></span>

<span data-ttu-id="cd563-321">I produksjon, hvis du du angir feltet **Hendelsestype** til **Ferdigmeld** og feltet **Utførelse** til **Etter** på siden **Kvalitetstilknytninger**, får du følgende resultater:</span><span class="sxs-lookup"><span data-stu-id="cd563-321">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="cd563-322">Hvis alternativet **Per oppdatert mengde** er satt til **Ja**, genereres det en kvalitetsordre for hver fullførte antall og innstillingene i vareprøven.</span><span class="sxs-lookup"><span data-stu-id="cd563-322">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="cd563-323">Hver gang et antall rapporteres som fullført mot produksjonsordren, genereres nye kvalitetsordrer basert på det nylig fullførte antallet.</span><span class="sxs-lookup"><span data-stu-id="cd563-323">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="cd563-324">Denne genereringslogikken er konsekvent med innkjøp.</span><span class="sxs-lookup"><span data-stu-id="cd563-324">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="cd563-325">Hvis alternativet **Per oppdatert mengde** er satt til **Nei**, genereres det en kvalitetsordre første gang antallet rapporteres som fullført, basert på det fullførte antallet.</span><span class="sxs-lookup"><span data-stu-id="cd563-325">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="cd563-326">I tillegg blir én eller flere kvalitetsordrer opprettet på grunnlag av restantallet, avhengig av sporingsdimensjonene for vareprøven.</span><span class="sxs-lookup"><span data-stu-id="cd563-326">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="cd563-327">Kvalitetsordrer genereres ikke for etterfølgende ferdigmeldte antall.</span><span class="sxs-lookup"><span data-stu-id="cd563-327">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="cd563-328">Kvalitetsspesifikasjon</span><span class="sxs-lookup"><span data-stu-id="cd563-328">Quality specification</span></span></th>
<th><span data-ttu-id="cd563-329">Per oppdatert mengde</span><span class="sxs-lookup"><span data-stu-id="cd563-329">Per updated quantity</span></span></th>
<th><span data-ttu-id="cd563-330">Per sporingsdimensjon</span><span class="sxs-lookup"><span data-stu-id="cd563-330">Per tracking dimension</span></span></th>
<th><span data-ttu-id="cd563-331">Resultat</span><span class="sxs-lookup"><span data-stu-id="cd563-331">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="cd563-332">Prosent: 10 %</span><span class="sxs-lookup"><span data-stu-id="cd563-332">Percentage: 10%</span></span></td>
<td><span data-ttu-id="cd563-333">Ja</span><span class="sxs-lookup"><span data-stu-id="cd563-333">Yes</span></span></td>
<td>
<p><span data-ttu-id="cd563-334">Partinummer: Nei</span><span class="sxs-lookup"><span data-stu-id="cd563-334">Batch number: No</span></span></p>
<p><span data-ttu-id="cd563-335">Serienummer: Nei</span><span class="sxs-lookup"><span data-stu-id="cd563-335">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="cd563-336">Ordreantall: 100</span><span class="sxs-lookup"><span data-stu-id="cd563-336">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="cd563-337">Rapporter som ferdig for 30</span><span class="sxs-lookup"><span data-stu-id="cd563-337">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="cd563-338">Kvalitetsordre #1 for 3 (10 % av 30)</span><span class="sxs-lookup"><span data-stu-id="cd563-338">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="cd563-339">Rapporter som ferdig for 70</span><span class="sxs-lookup"><span data-stu-id="cd563-339">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="cd563-340">Kvalitetsordre #2 for 7 (10 % av restordreantallet, som er lik 70 i dette tilfellet)</span><span class="sxs-lookup"><span data-stu-id="cd563-340">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="cd563-341">Fast antall: 1</span><span class="sxs-lookup"><span data-stu-id="cd563-341">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="cd563-342">Nei</span><span class="sxs-lookup"><span data-stu-id="cd563-342">No</span></span></td>
<td>
<p><span data-ttu-id="cd563-343">Partinummer: Nei</span><span class="sxs-lookup"><span data-stu-id="cd563-343">Batch number: No</span></span></p>
<p><span data-ttu-id="cd563-344">Serienummer: Nei</span><span class="sxs-lookup"><span data-stu-id="cd563-344">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="cd563-345">Ordreantall: 100</span><span class="sxs-lookup"><span data-stu-id="cd563-345">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="cd563-346">Rapporter som ferdig for 30</span><span class="sxs-lookup"><span data-stu-id="cd563-346">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="cd563-347">Kvalitetsordre #1 for 1 (for det første ferdigmeldte antallet, som har en fast verdi på 1)</span><span class="sxs-lookup"><span data-stu-id="cd563-347">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="cd563-348">Kvalitetsordre #2 for 1 (for det resterende antallet, som fremdeles har en fast verdi på 1)</span><span class="sxs-lookup"><span data-stu-id="cd563-348">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="cd563-349">Rapporter som ferdig for 10</span><span class="sxs-lookup"><span data-stu-id="cd563-349">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="cd563-350">Ingen kvalitetsordrer er opprettet.</span><span class="sxs-lookup"><span data-stu-id="cd563-350">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="cd563-351">Rapporter som ferdig for 60</span><span class="sxs-lookup"><span data-stu-id="cd563-351">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="cd563-352">Ingen kvalitetsordrer er opprettet.</span><span class="sxs-lookup"><span data-stu-id="cd563-352">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="cd563-353">Fast antall: 1</span><span class="sxs-lookup"><span data-stu-id="cd563-353">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="cd563-354">Ja</span><span class="sxs-lookup"><span data-stu-id="cd563-354">Yes</span></span></td>
<td>
<p><span data-ttu-id="cd563-355">Partinummer: Ja</span><span class="sxs-lookup"><span data-stu-id="cd563-355">Batch number: Yes</span></span></p>
<p><span data-ttu-id="cd563-356">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="cd563-356">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="cd563-357">Ordreantall: 10</span><span class="sxs-lookup"><span data-stu-id="cd563-357">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="cd563-358">Rapporter som ferdig for 3: 1 for #b1, #s1; 1 for #b2, #s2; og 1 for #b3, #s3</span><span class="sxs-lookup"><span data-stu-id="cd563-358">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="cd563-359">Kvalitetsordre #1 for 1 av parti #b1, serie #s1</span><span class="sxs-lookup"><span data-stu-id="cd563-359">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="cd563-360">Kvalitetsordre #2 for 1 av parti #b2, serie #s2</span><span class="sxs-lookup"><span data-stu-id="cd563-360">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="cd563-361">Kvalitetsordre #3 for 1 av parti #b3, serie #s3</span><span class="sxs-lookup"><span data-stu-id="cd563-361">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="cd563-362">Rapporter som ferdig for 2: 1 for #b4, #s4; og 1 for #b5, #s5</span><span class="sxs-lookup"><span data-stu-id="cd563-362">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="cd563-363">Kvalitetsordre #4 for 1 av parti #b4, serie #s4</span><span class="sxs-lookup"><span data-stu-id="cd563-363">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="cd563-364">Kvalitetsordre #5 for 1 av parti #b5, serie #s5</span><span class="sxs-lookup"><span data-stu-id="cd563-364">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="cd563-365"><strong>Merk:</strong> Partiet kan brukes på nytt.</span><span class="sxs-lookup"><span data-stu-id="cd563-365"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="cd563-366">Fast antall: 2</span><span class="sxs-lookup"><span data-stu-id="cd563-366">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="cd563-367">Nei</span><span class="sxs-lookup"><span data-stu-id="cd563-367">No</span></span></td>
<td>
<p><span data-ttu-id="cd563-368">Partinummer: Ja</span><span class="sxs-lookup"><span data-stu-id="cd563-368">Batch number: Yes</span></span></p>
<p><span data-ttu-id="cd563-369">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="cd563-369">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="cd563-370">Ordreantall: 10</span><span class="sxs-lookup"><span data-stu-id="cd563-370">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="cd563-371">Rapporter som ferdig for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; og 1 for #b4, #s4</span><span class="sxs-lookup"><span data-stu-id="cd563-371">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="cd563-372">Kvalitetsordre #1 for 1 av parti #b1, serie #s1</span><span class="sxs-lookup"><span data-stu-id="cd563-372">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="cd563-373">Kvalitetsordre #2 for 1 av parti #b2, serie #s2</span><span class="sxs-lookup"><span data-stu-id="cd563-373">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="cd563-374">Kvalitetsordre #3 for 1 av parti #b3, serie #s3</span><span class="sxs-lookup"><span data-stu-id="cd563-374">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="cd563-375">Kvalitetsordre #4 for 1 av parti #b4, serie #s4</span><span class="sxs-lookup"><span data-stu-id="cd563-375">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="cd563-376">Kvalitetsordre #5 for 2, uten referanse til et parti og et serienummer</span><span class="sxs-lookup"><span data-stu-id="cd563-376">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="cd563-377">Rapporter som ferdig for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; og 1 for #b10, #s10</span><span class="sxs-lookup"><span data-stu-id="cd563-377">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="cd563-378">Ingen kvalitetsordrer er opprettet.</span><span class="sxs-lookup"><span data-stu-id="cd563-378">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="cd563-379">Kvalitetsstyringssider</span><span class="sxs-lookup"><span data-stu-id="cd563-379">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cd563-380">Side</span><span class="sxs-lookup"><span data-stu-id="cd563-380">Page</span></span></th>
<th><span data-ttu-id="cd563-381">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cd563-381">Description</span></span></th>
<th><span data-ttu-id="cd563-382">Eksempel</span><span class="sxs-lookup"><span data-stu-id="cd563-382">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cd563-383">Kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="cd563-383">Quality associations</span></span></td>
<td><span data-ttu-id="cd563-384">Se tidligere deler av denne artikkelen.</span><span class="sxs-lookup"><span data-stu-id="cd563-384">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="cd563-385">En kvalitetstilknytning definerer alle følgende opplysninger om en kvalitetsordre som er generert:</span><span class="sxs-lookup"><span data-stu-id="cd563-385">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="cd563-386">Transaksjonshendelsen</span><span class="sxs-lookup"><span data-stu-id="cd563-386">The transaction event</span></span></li>
<li><span data-ttu-id="cd563-387">Settet med tester som må utføres på elementene</span><span class="sxs-lookup"><span data-stu-id="cd563-387">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="cd563-388">Det akseptable kvalitetsnivået</span><span class="sxs-lookup"><span data-stu-id="cd563-388">The AQL</span></span></li>
<li><span data-ttu-id="cd563-389">Prøveplanen</span><span class="sxs-lookup"><span data-stu-id="cd563-389">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="cd563-390">Du må definere en kvalitetstilknytning for hver variasjon i en forretningsprosess som krever automatisk generering av kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="cd563-390">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="cd563-391">Eksempelvis kan en kvalitetsordre genereres i forretningsprosessen for bestillinger, karanteneordrer, salgsordrer og produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="cd563-391">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd563-392">Tester</span><span class="sxs-lookup"><span data-stu-id="cd563-392">Tests</span></span></td>
<td><span data-ttu-id="cd563-393">Bruk denne siden til å definere og vise de individuelle testene som fastslår om produktene oppfyller kvalitetsspesifikasjoner.</span><span class="sxs-lookup"><span data-stu-id="cd563-393">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="cd563-394">Du kan tilordne én eller flere individuelle tester til en testgruppe.</span><span class="sxs-lookup"><span data-stu-id="cd563-394">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="cd563-395">I dette tilfellet må også angi testspesifikk informasjon, for eksempel de akseptable målingsverdiene.</span><span class="sxs-lookup"><span data-stu-id="cd563-395">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="cd563-396">Målingsverdiene brukes for kvantitative tester, og testvariablene brukes for kvalitative tester.</span><span class="sxs-lookup"><span data-stu-id="cd563-396">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="cd563-397">En kvantitativ test har testtypen <strong>Heltall</strong> eller <strong>Brøk</strong> og har også en angitt måleenhet.</span><span class="sxs-lookup"><span data-stu-id="cd563-397">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="cd563-398">Kvalitetsspesifikasjoner og testresultater uttrykkes som tall.</span><span class="sxs-lookup"><span data-stu-id="cd563-398">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="cd563-399">En kvalitativ test har testtypen <strong>Alternativ</strong>.</span><span class="sxs-lookup"><span data-stu-id="cd563-399">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="cd563-400">Kvalitative tester krever mer informasjon om testvariabelen som måles, og de tilhørende opplistede alternativene.</span><span class="sxs-lookup"><span data-stu-id="cd563-400">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="cd563-401">Kvalitetsspesifikasjoner og testresultater uttrykkes i henhold til et resultat.</span><span class="sxs-lookup"><span data-stu-id="cd563-401">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="cd563-402">Et produksjonsfirma utfører to tester på innkjøpt materiale: en kvantitativ test om materialkvalitet og en kvalitativ test om emballasjeskade.</span><span class="sxs-lookup"><span data-stu-id="cd563-402">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="cd563-403">Firmaet definerer tilleggsinformasjon om den kvalitative testen for å identifisere testvariabelen (skadet emballasje) og resultatene.</span><span class="sxs-lookup"><span data-stu-id="cd563-403">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="cd563-404">Firmaet bruker <strong>Testgrupper</strong>-siden til å tilordne de to testene til en testgruppe og angi testspesifikk informasjon.</span><span class="sxs-lookup"><span data-stu-id="cd563-404">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="cd563-405">Testgruppen tilordnes til en kvalitetsordre, slik at firmaet kan rapportere testresultater for de to testene.</span><span class="sxs-lookup"><span data-stu-id="cd563-405">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd563-406">Testgrupper</span><span class="sxs-lookup"><span data-stu-id="cd563-406">Test groups</span></span></td>
<td><span data-ttu-id="cd563-407">Bruk denne siden til å definere, redigere og vise testgrupper og de individuelle testene som er tilordnet til en testgruppe.</span><span class="sxs-lookup"><span data-stu-id="cd563-407">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="cd563-408">Den øvre ruten viser testgrupper, og den nedre ruten viser testene som er tilordnet til en valgt testgruppe.</span><span class="sxs-lookup"><span data-stu-id="cd563-408">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="cd563-409">Du tilordner flere policyer til en testgruppe, for eksempel en prøveplan, et akseptabelt kvalitetsnivå og kravet til destruktiv testing.</span><span class="sxs-lookup"><span data-stu-id="cd563-409">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="cd563-410">Når du tilordner en individuell test til en testgruppe, definerer du tilleggsinformasjon, for eksempel sekvensen, dokumenter og gyldighetsdatoer.</span><span class="sxs-lookup"><span data-stu-id="cd563-410">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="cd563-411">For en kvantitativ test inkluderer informasjonen du definerer, også de akseptable målingsverdiene.</span><span class="sxs-lookup"><span data-stu-id="cd563-411">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="cd563-412">For en kvalitativ test inkluderer informasjonen testvariabelen og standardresultatet.</span><span class="sxs-lookup"><span data-stu-id="cd563-412">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="cd563-413">Testgruppen som er tilordnet en kvalitetsordre, definerer standardsettet med tester som må utføres for den bestemte varen.</span><span class="sxs-lookup"><span data-stu-id="cd563-413">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="cd563-414">Du kan imidlertid legge til, slette eller endre tester i kvalitetsordren.</span><span class="sxs-lookup"><span data-stu-id="cd563-414">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="cd563-415">Testresultater rapporteres for hver test på en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="cd563-415">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="cd563-416">Et produksjonsfirma definerer en testgruppe for hver variasjon av retningslinjene for kvalitet.</span><span class="sxs-lookup"><span data-stu-id="cd563-416">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="cd563-417">De ulike testgruppene gjenspeiler forskjeller i prøveplanene, settet med tester som må utføres sammen, det akseptable kvalitetsnivået og andre faktorer.</span><span class="sxs-lookup"><span data-stu-id="cd563-417">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="cd563-418">For kvantitative tester er det også forskjeller i de akseptable målingsverdiene.</span><span class="sxs-lookup"><span data-stu-id="cd563-418">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="cd563-419">Hvis du vil fremtvinge retningslinjene for kvalitet, tilordner firmaet en testgruppe til hver regel for automatisk generering av kvalitetsordrer på siden <strong>Kvalitetstilknytninger</strong>, og tilordner også en testgruppe til kvalitetsordrer som opprettes manuelt.</span><span class="sxs-lookup"><span data-stu-id="cd563-419">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd563-420">Varekvalitetsgrupper</span><span class="sxs-lookup"><span data-stu-id="cd563-420">Item quality groups</span></span></td>
<td><span data-ttu-id="cd563-421">Bruk denne siden til å definere, redigere og vise varene som er tilordnet til en kvalitetsgruppe, eller kvalitetsgruppene som er tilordnet til en vare.</span><span class="sxs-lookup"><span data-stu-id="cd563-421">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="cd563-422">En kvalitetsgruppe representerer felles testkrav for varer.</span><span class="sxs-lookup"><span data-stu-id="cd563-422">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="cd563-423">Når du har definert testkravene på siden <strong>Testgrupper</strong>, kan du definere reglene for automatisk generering av kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="cd563-423">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="cd563-424">For å forenkle prosessen kan du ikke definerer reglene for individuelle varer.</span><span class="sxs-lookup"><span data-stu-id="cd563-424">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="cd563-425">I stedet definere du regler for en kvalitetsgruppe ved hjelp av siden <strong>Kvalitetstilknytninger</strong>.</span><span class="sxs-lookup"><span data-stu-id="cd563-425">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="cd563-426">Du kan også bruke siden <strong>Varekvalitetsgrupper</strong> for en valgt kvalitetsgruppe for å tilordne relevante varer til denne gruppen.</span><span class="sxs-lookup"><span data-stu-id="cd563-426">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="cd563-427">Du kan også bruke siden <strong>Varekvalitetsgrupper</strong> for en valgt vare for å tilordne relevante kvalitetsgrupper til varen.</span><span class="sxs-lookup"><span data-stu-id="cd563-427">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="cd563-428">Et produksjonsfirma kjøper inn ulike råmaterialer som har samme testkrav for innkommende inspeksjon.</span><span class="sxs-lookup"><span data-stu-id="cd563-428">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="cd563-429">Firmaet definerer en kvalitetsgruppe og tilordner deretter varenumrene som er tilknyttet råvarene til denne gruppen.</span><span class="sxs-lookup"><span data-stu-id="cd563-429">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="cd563-430">Senere kjøper selskapet en ny type råvarer som har samme testkrav.</span><span class="sxs-lookup"><span data-stu-id="cd563-430">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="cd563-431">I stedet for å opprette nye testkrav for det nye materialet, legger firmaet til varenummeret for det nye materialet i den eksisterende kvalitetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="cd563-431">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="cd563-432">Det samme produksjonsfirmaet produserer også varer med samme krav til produksjonstesting, og leverer varer med samme krav til utføring av tester før forsendelse.</span><span class="sxs-lookup"><span data-stu-id="cd563-432">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="cd563-433">Firmaet definerer to ekstra kvalitetsgrupper, og tilordner deretter de aktuelle varenumrene til hver gruppe.</span><span class="sxs-lookup"><span data-stu-id="cd563-433">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd563-434">Testvariabler</span><span class="sxs-lookup"><span data-stu-id="cd563-434">Test variables</span></span></td>
<td><span data-ttu-id="cd563-435">Bruk denne siden til å definere og vise variablene som er tilknyttet en kvalitativ test.</span><span class="sxs-lookup"><span data-stu-id="cd563-435">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="cd563-436">For hver variabel kan du definere opplistede resultater som representerer de mulige alternativene.</span><span class="sxs-lookup"><span data-stu-id="cd563-436">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="cd563-437">Du definerer testene på siden <strong>Tester</strong>.</span><span class="sxs-lookup"><span data-stu-id="cd563-437">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="cd563-438">Du må sette testtypen for kvalitative tester til <strong>Alternativ</strong>.</span><span class="sxs-lookup"><span data-stu-id="cd563-438">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="cd563-439">Bruk siden <strong>Testgrupper</strong> til å tilordne en testvariabel til en enkelt test.</span><span class="sxs-lookup"><span data-stu-id="cd563-439">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="cd563-440">En produksjonsfirma som produserer kjeks, bruker en inspeksjonstest til det ferdige produktet.</span><span class="sxs-lookup"><span data-stu-id="cd563-440">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="cd563-441">Denne inspeksjonstesten har flere variabler.</span><span class="sxs-lookup"><span data-stu-id="cd563-441">This inspection test has several variables.</span></span> <span data-ttu-id="cd563-442">Én variabel er smak, og de mulige resultatene for denne variabelen er god og dårlig.</span><span class="sxs-lookup"><span data-stu-id="cd563-442">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="cd563-443">En annen variabel er farge, og de mulige resultatene er for mørk, for lys og riktig.</span><span class="sxs-lookup"><span data-stu-id="cd563-443">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd563-444">Testvariabelresultater</span><span class="sxs-lookup"><span data-stu-id="cd563-444">Test variable outcomes</span></span></td>
<td><span data-ttu-id="cd563-445">Bruk denne siden til å definere, redigere og vise de mulige testresultatene for en testvariabel som er knyttet til en kvalitetstest.</span><span class="sxs-lookup"><span data-stu-id="cd563-445">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="cd563-446">For hvert resultat tilordner du statusen <strong>bestått</strong> eller <strong>mislykket</strong>.</span><span class="sxs-lookup"><span data-stu-id="cd563-446">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="cd563-447">Du må definere en variabel og resultatene for hver kvalitative test som defineres på siden <strong>Tester</strong>.</span><span class="sxs-lookup"><span data-stu-id="cd563-447">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="cd563-448">(For kvalitative tester er testtypen satt til <strong>Alternativ</strong> på <strong>Tester</strong>-siden.) Bruk <strong>Testgrupper</strong>-siden til å tilordne en testvariabel og standardresultatet til en enkelt kvalitetstest.</span><span class="sxs-lookup"><span data-stu-id="cd563-448">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="cd563-449">En produksjonsfirma som produserer kjeks, bruker en inspeksjonstest til det ferdige produktet.</span><span class="sxs-lookup"><span data-stu-id="cd563-449">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="cd563-450">Denne inspeksjonstesten har flere variabler.</span><span class="sxs-lookup"><span data-stu-id="cd563-450">This inspection test has of several variables.</span></span> <span data-ttu-id="cd563-451">Én variabel er smak, og de mulige resultatene for denne variabelen er god og dårlig.</span><span class="sxs-lookup"><span data-stu-id="cd563-451">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="cd563-452">En annen variabel er farge, og de mulige resultatene er for mørk, for lys og riktig.</span><span class="sxs-lookup"><span data-stu-id="cd563-452">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="cd563-453">Statusen <strong>bestått</strong> eller <strong>mislykket</strong> tilordnes hvert resultat.</span><span class="sxs-lookup"><span data-stu-id="cd563-453">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="cd563-454">Under inspeksjonstesten for hver variabel rapporterer inspektøren testresultatet ved å velge ett av resultatene.</span><span class="sxs-lookup"><span data-stu-id="cd563-454">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="cd563-455">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="cd563-455">Additional resources</span></span>
--------

[<span data-ttu-id="cd563-456">Kvalitetsstyringsprosesser</span><span class="sxs-lookup"><span data-stu-id="cd563-456">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="cd563-457">Aktivere behandling av avvik</span><span class="sxs-lookup"><span data-stu-id="cd563-457">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)
