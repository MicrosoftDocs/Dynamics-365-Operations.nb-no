---
title: Oversikt over kvalitetsstyring
description: Dette emnet beskriver hvordan du kan bruke kvalitetsstyring i Microsoft Dynamics 365 for Finance and Operations for å forbedre produktkvalitet i forsyningskjeden.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
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
ms.openlocfilehash: 1630d13437d7e930fdf32ed5fdc61fc62bc33817
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "338320"
---
# <a name="quality-management-overview"></a><span data-ttu-id="cec03-103">Oversikt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="cec03-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cec03-104">Dette emnet beskriver hvordan du kan bruke kvalitetsstyring i Microsoft Dynamics 365 for Finance and Operations for å forbedre produktkvalitet i forsyningskjeden.</span><span class="sxs-lookup"><span data-stu-id="cec03-104">This topic describes how you can use quality management in Microsoft Dynamics 365 for Finance and Operations to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="cec03-105">Kvalitetsstyring kan hjelpe deg med å administrere behandlingstiden når du håndterer produkter med avvik, uavhengig av opprinnelsespunktet.</span><span class="sxs-lookup"><span data-stu-id="cec03-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="cec03-106">Fordi diagnosetyper er knyttet til rettelsesrapportering, kan Microsoft Dynamics 365 for Finance and Operations planlegge oppgaver for å rette opp problemer og hindre at de skjer igjen.</span><span class="sxs-lookup"><span data-stu-id="cec03-106">Because diagnostic types are linked to correction reporting, Microsoft Dynamics 365 for Finance and Operations can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="cec03-107">I tillegg til funksjonalitet for håndtering av avvik inneholder kvalitetsstyring funksjonalitet for å spore problemer etter problemtype (selv interne problemer) og identifisere løsninger som kortsiktige eller langsiktige.</span><span class="sxs-lookup"><span data-stu-id="cec03-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="cec03-108">Statistikk om nøkkelytelsesindikator (KPI-er) gir innsikt i loggen for tidligere avviksproblemer og løsninger som ble brukt til å rette feilene.</span><span class="sxs-lookup"><span data-stu-id="cec03-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="cec03-109">Du kan bruke historiske data for å undersøke effektiviteten til tidligere kvalitetsmål og bestemme nødvendige tiltak som skal brukes i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="cec03-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="cec03-110">Når du definerer en kvalitetstilknytning, kan Finance and Operations generere kvalitetsordrer for diverse forretningsprosesser, hendelser og betingelser.</span><span class="sxs-lookup"><span data-stu-id="cec03-110">When you set up a quality association, Finance and Operations can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="cec03-111">Kvalitetstilknytningen kan dekke en bestemt vare, en bestemt varegruppe eller alle varer.</span><span class="sxs-lookup"><span data-stu-id="cec03-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="cec03-112">Eksempler på bruk av kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="cec03-112">Examples of the use of quality management</span></span>
<span data-ttu-id="cec03-113">Kvalitetsstyring er fleksibelt og kan implementeres på forskjellige måter for å oppfylle kravene til bestemte typer forsyningskjedeoperasjoner.</span><span class="sxs-lookup"><span data-stu-id="cec03-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="cec03-114">Følgende eksempel viser mulig bruk av disse funksjonene.</span><span class="sxs-lookup"><span data-stu-id="cec03-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="cec03-115">Start en prosess for kvalitetskontroll automatisk basert på forhåndsdefinerte kriterier (ved lagerregistrering av en bestilling fra en bestemt leverandør).</span><span class="sxs-lookup"><span data-stu-id="cec03-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="cec03-116">Blokker lageret under inspeksjon for å hindre bruk av ikke-godkjent lager (full blokkering av bestillingsantall).</span><span class="sxs-lookup"><span data-stu-id="cec03-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="cec03-117">Bruk vareprøver som en del av en kvalitetstilknytning for å definere hvor mye av det fysiske lageret som må kontrolleres.</span><span class="sxs-lookup"><span data-stu-id="cec03-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="cec03-118">Prøver kan være basert på faste antall eller en prosentdel.</span><span class="sxs-lookup"><span data-stu-id="cec03-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="cec03-119">Opprette kvalitetsordrer for delvise mottak.</span><span class="sxs-lookup"><span data-stu-id="cec03-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="cec03-120">Hvis du vil opprette en kvalitetsordre som er basert på antallet som er fysisk mottatt med en ordre, må du velge den **Per oppdatert mengde** for den **Vareprøve** skjema.</span><span class="sxs-lookup"><span data-stu-id="cec03-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="cec03-121">Opprett testtyper med minimums-, maksimums-, og måltestverdier, og utfør kvalitative kontra kvantitative tester som har forhåndsdefinerte valideringsresultater.</span><span class="sxs-lookup"><span data-stu-id="cec03-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="cec03-122">Angi et akseptabelt kvalitetsnivå for å kontrollere kvalitetsmåltoleranser.</span><span class="sxs-lookup"><span data-stu-id="cec03-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="cec03-123">Angi ressursene som en inspeksjonsoperasjon krever, for eksempel et testområde og testinstrumenter.</span><span class="sxs-lookup"><span data-stu-id="cec03-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="cec03-124">Arbeide med kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="cec03-124">Working with quality associations</span></span>
<span data-ttu-id="cec03-125">Forretningsprosessen som bruker en kvalitetstilknytning, kan knyttes til ulike kildedokumenter, for eksempel bestillinger, salgsordrer eller produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="cec03-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="cec03-126">Hver kvalitetstilknytningspost definerer settet med tester, det akseptable kvalitetsnivået og samplingplanen som gjelder for kvalitetsordrene som genereres.</span><span class="sxs-lookup"><span data-stu-id="cec03-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="cec03-127">Du må definere en kvalitetstilknytningspost for hver variasjon i en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="cec03-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="cec03-128">Du kan for eksempel definere en kvalitetstilknytning som genererer en kvalitetsordre når et produkt for bestillingsmottak oppdateres.</span><span class="sxs-lookup"><span data-stu-id="cec03-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="cec03-129">Avhengig av oppsettet for utførelsesplanen kan selve utløsingsprosessen blokkeres når det finnes en åpen kvalitetsordre, eller de neste prosessene, for eksempel bestillingsfakturering, kan blokkeres.</span><span class="sxs-lookup"><span data-stu-id="cec03-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="cec03-130">**Merk:** Når det finnes åpne kvalitetsordrer, blokkeres lagerantall automatisk fra å bli utstedt.</span><span class="sxs-lookup"><span data-stu-id="cec03-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="cec03-131">Avhengig av **Full blokkering**-innstillingen på siden **Vareprøver** er antallet enten antallet på kvalitetsordren eller antallet på kildedokumentlinjen.</span><span class="sxs-lookup"><span data-stu-id="cec03-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="cec03-132">For en gitt forretningsprosess identifiserer kvalitetstilknytningspost hendelsen og betingelsene som en kvalitetsordre genereres for.</span><span class="sxs-lookup"><span data-stu-id="cec03-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="cec03-133">Betingelsene kan være spesifikke for et område eller en juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="cec03-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="cec03-134">En kvalitetsordre som omfatter destruktive tester, kan bare genereres når hvis det finnes lagerbeholdning for hendelsen.</span><span class="sxs-lookup"><span data-stu-id="cec03-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="cec03-135">De følgende eksemplene illustrerer hvordan en kvalitetstilknytningspost er definert for variasjonene innen ulike forretningsprosesser.</span><span class="sxs-lookup"><span data-stu-id="cec03-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="cec03-136">For hvert eksempel oppsummere følgende tabell hendelsene og betingelsene som er definert av en kvalitetstilknytningspost.</span><span class="sxs-lookup"><span data-stu-id="cec03-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="cec03-137">Referansetype</span><span class="sxs-lookup"><span data-stu-id="cec03-137">Reference type</span></span></th>
<th><span data-ttu-id="cec03-138">Hendelsestype</span><span class="sxs-lookup"><span data-stu-id="cec03-138">Event type</span></span></th>
<th><span data-ttu-id="cec03-139">Utførelse</span><span class="sxs-lookup"><span data-stu-id="cec03-139">Execution</span></span></th>
<th><span data-ttu-id="cec03-140">Hendelsesblokkering</span><span class="sxs-lookup"><span data-stu-id="cec03-140">Event blocking</span></span></th>
<th><span data-ttu-id="cec03-141">Dokumentreferanse</span><span class="sxs-lookup"><span data-stu-id="cec03-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="cec03-142">Beholdning</span><span class="sxs-lookup"><span data-stu-id="cec03-142">Inventory</span></span></td>
<td><span data-ttu-id="cec03-143">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="cec03-143">Not applicable</span></span></td>
<td><span data-ttu-id="cec03-144">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="cec03-144">Not applicable</span></span></td>
<td><span data-ttu-id="cec03-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="cec03-145">None</span></span></td>
<td><span data-ttu-id="cec03-146">Alle</span><span class="sxs-lookup"><span data-stu-id="cec03-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="cec03-147">Salg</span><span class="sxs-lookup"><span data-stu-id="cec03-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="cec03-148">Plukkingsprosess er planlagt</span><span class="sxs-lookup"><span data-stu-id="cec03-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="cec03-149">Før</span><span class="sxs-lookup"><span data-stu-id="cec03-149">Before</span></span></td>
<td><span data-ttu-id="cec03-150">Ingen</span><span class="sxs-lookup"><span data-stu-id="cec03-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="cec03-151">Bare Spesifikk ID, Gruppe eller Alle</span><span class="sxs-lookup"><span data-stu-id="cec03-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-152">Plukkingsprosess</span><span class="sxs-lookup"><span data-stu-id="cec03-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-153">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="cec03-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-154">Faktura</span><span class="sxs-lookup"><span data-stu-id="cec03-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cec03-155">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="cec03-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="cec03-156">Før</span><span class="sxs-lookup"><span data-stu-id="cec03-156">Before</span></span></td>
<td><span data-ttu-id="cec03-157">Ingen</span><span class="sxs-lookup"><span data-stu-id="cec03-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-158">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="cec03-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-159">Faktura</span><span class="sxs-lookup"><span data-stu-id="cec03-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="cec03-160">Kjøp</span><span class="sxs-lookup"><span data-stu-id="cec03-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="cec03-161">Kvitteringsliste</span><span class="sxs-lookup"><span data-stu-id="cec03-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="cec03-162">Før</span><span class="sxs-lookup"><span data-stu-id="cec03-162">Before</span></span></td>
<td><span data-ttu-id="cec03-163">Ingen</span><span class="sxs-lookup"><span data-stu-id="cec03-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-164">Kvitteringsliste</span><span class="sxs-lookup"><span data-stu-id="cec03-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-165">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="cec03-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-166">Faktura</span><span class="sxs-lookup"><span data-stu-id="cec03-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cec03-167">Etter</span><span class="sxs-lookup"><span data-stu-id="cec03-167">After</span></span></td>
<td><span data-ttu-id="cec03-168">Ingen</span><span class="sxs-lookup"><span data-stu-id="cec03-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-169">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="cec03-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-170">Faktura</span><span class="sxs-lookup"><span data-stu-id="cec03-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cec03-171">Registrering</span><span class="sxs-lookup"><span data-stu-id="cec03-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="cec03-172">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="cec03-172">Not applicable</span></span></td>
<td><span data-ttu-id="cec03-173">Ingen</span><span class="sxs-lookup"><span data-stu-id="cec03-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-174">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="cec03-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-175">Faktura</span><span class="sxs-lookup"><span data-stu-id="cec03-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="cec03-176">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="cec03-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="cec03-177">Før</span><span class="sxs-lookup"><span data-stu-id="cec03-177">Before</span></span></td>
<td><span data-ttu-id="cec03-178">Ingen</span><span class="sxs-lookup"><span data-stu-id="cec03-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-179">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="cec03-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-180">Faktura</span><span class="sxs-lookup"><span data-stu-id="cec03-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cec03-181">Etter</span><span class="sxs-lookup"><span data-stu-id="cec03-181">After</span></span></td>
<td><span data-ttu-id="cec03-182">Ingen</span><span class="sxs-lookup"><span data-stu-id="cec03-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-183">Faktura</span><span class="sxs-lookup"><span data-stu-id="cec03-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="cec03-184">Produksjon</span><span class="sxs-lookup"><span data-stu-id="cec03-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="cec03-185">Registrering</span><span class="sxs-lookup"><span data-stu-id="cec03-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="cec03-186">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="cec03-186">Not applicable</span></span></td>
<td><span data-ttu-id="cec03-187">Ingen</span><span class="sxs-lookup"><span data-stu-id="cec03-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="cec03-188">Alle</span><span class="sxs-lookup"><span data-stu-id="cec03-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-189">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="cec03-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-190">Slutt</span><span class="sxs-lookup"><span data-stu-id="cec03-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="cec03-191">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="cec03-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="cec03-192">Før</span><span class="sxs-lookup"><span data-stu-id="cec03-192">Before</span></span></td>
<td><span data-ttu-id="cec03-193">Ingen</span><span class="sxs-lookup"><span data-stu-id="cec03-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-194">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="cec03-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-195">Slutt</span><span class="sxs-lookup"><span data-stu-id="cec03-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cec03-196">Etter</span><span class="sxs-lookup"><span data-stu-id="cec03-196">After</span></span></td>
<td><span data-ttu-id="cec03-197">Ingen</span><span class="sxs-lookup"><span data-stu-id="cec03-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-198">Slutt</span><span class="sxs-lookup"><span data-stu-id="cec03-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="cec03-199">Karantene</span><span class="sxs-lookup"><span data-stu-id="cec03-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="cec03-200">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="cec03-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="cec03-201">Før</span><span class="sxs-lookup"><span data-stu-id="cec03-201">Before</span></span></td>
<td><span data-ttu-id="cec03-202">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="cec03-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-203">Slutt</span><span class="sxs-lookup"><span data-stu-id="cec03-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-204">Etter</span><span class="sxs-lookup"><span data-stu-id="cec03-204">After</span></span></td>
<td><span data-ttu-id="cec03-205">Slutt</span><span class="sxs-lookup"><span data-stu-id="cec03-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-206">Slutt</span><span class="sxs-lookup"><span data-stu-id="cec03-206">End</span></span></td>
<td><span data-ttu-id="cec03-207">Før</span><span class="sxs-lookup"><span data-stu-id="cec03-207">Before</span></span></td>
<td><span data-ttu-id="cec03-208">Slutt</span><span class="sxs-lookup"><span data-stu-id="cec03-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cec03-209">Ruteoperasjon</span><span class="sxs-lookup"><span data-stu-id="cec03-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="cec03-210">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="cec03-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="cec03-211">Før</span><span class="sxs-lookup"><span data-stu-id="cec03-211">Before</span></span></td>
<td><span data-ttu-id="cec03-212">Ingen</span><span class="sxs-lookup"><span data-stu-id="cec03-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="cec03-213">Bestemt ID, Gruppe eller Alle, og Ressursspesifikk, Gruppe eller Alle</span><span class="sxs-lookup"><span data-stu-id="cec03-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-214">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="cec03-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-215">Etter</span><span class="sxs-lookup"><span data-stu-id="cec03-215">After</span></span></td>
<td><span data-ttu-id="cec03-216">Ingen</span><span class="sxs-lookup"><span data-stu-id="cec03-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cec03-217">Koproduktproduksjon</span><span class="sxs-lookup"><span data-stu-id="cec03-217">Co-product production</span></span></td>
<td><span data-ttu-id="cec03-218">Registrering</span><span class="sxs-lookup"><span data-stu-id="cec03-218">Registration</span></span></td>
<td><span data-ttu-id="cec03-219">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="cec03-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cec03-220">Ingen</span><span class="sxs-lookup"><span data-stu-id="cec03-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="cec03-221">Alle</span><span class="sxs-lookup"><span data-stu-id="cec03-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cec03-222">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="cec03-222">Report as finished</span></span></td>
<td><span data-ttu-id="cec03-223">Før</span><span class="sxs-lookup"><span data-stu-id="cec03-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-224">Etter</span><span class="sxs-lookup"><span data-stu-id="cec03-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cec03-225">Tabellen nedenfor inneholder mer informasjon om hvordan kvalitetsordrer kan genereres for bestemte typer prosesser.</span><span class="sxs-lookup"><span data-stu-id="cec03-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="cec03-226">Type av prosess</span><span class="sxs-lookup"><span data-stu-id="cec03-226">Type of process</span></span></th>
<th><span data-ttu-id="cec03-227">Når kvalitetsordrer kan genereres automatisk</span><span class="sxs-lookup"><span data-stu-id="cec03-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="cec03-228">Når kvalitetsordrer kan genereres hvis destruktiv testing kreves</span><span class="sxs-lookup"><span data-stu-id="cec03-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="cec03-229">Betingelsesinformasjon</span><span class="sxs-lookup"><span data-stu-id="cec03-229">Condition information</span></span></th>
<th><span data-ttu-id="cec03-230">Informasjon om manuell generering</span><span class="sxs-lookup"><span data-stu-id="cec03-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="cec03-231">Bestilling</span><span class="sxs-lookup"><span data-stu-id="cec03-231">Purchase order</span></span></td>
<td><span data-ttu-id="cec03-232">Før eller etter en kvitteringsliste eller produktkvittering for materialet som mottas, posteres</span><span class="sxs-lookup"><span data-stu-id="cec03-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="cec03-233">Etter produktkvitteringen for materialet som mottas, er postert, fordi materialet må være tilgjengelig for destruktiv testing</span><span class="sxs-lookup"><span data-stu-id="cec03-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="cec03-234">Behovet for en kvalitetsordre kan reflektere et bestemt område, en vare, en leverandør eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="cec03-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="cec03-235">En manuelt generert kvalitetsordre som viser til en bestilling, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="cec03-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-236">Karanteneordre</span><span class="sxs-lookup"><span data-stu-id="cec03-236">Quarantine order</span></span></td>
<td><span data-ttu-id="cec03-237">Før eller etter karanteordren er rapportert som fullført eller avsluttet</span><span class="sxs-lookup"><span data-stu-id="cec03-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="cec03-238">Kvalitetsordrer som krever destruktive tester, kan ikke genereres.</span><span class="sxs-lookup"><span data-stu-id="cec03-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="cec03-239">Det forutsettes at karanteneordrefunksjonaliteten behandler disposisjonen av materialet som blir ødelagt.</span><span class="sxs-lookup"><span data-stu-id="cec03-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="cec03-240">Behovet for en kvalitetsordre kan reflektere et bestemt område, en vare, en leverandør eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="cec03-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="cec03-241">En manuelt generert kvalitetsordre som viser til en karanteneordre, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="cec03-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-242">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="cec03-242">Sales order</span></span></td>
<td><span data-ttu-id="cec03-243">Før en planlagt plukkeprosessen eller følgeseddeloppdatering for varene som leveres</span><span class="sxs-lookup"><span data-stu-id="cec03-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="cec03-244">I alle trinn</span><span class="sxs-lookup"><span data-stu-id="cec03-244">At any step</span></span></td>
<td><span data-ttu-id="cec03-245">Kravet til en kvalitetsordre kan reflektere et bestemt område, en vare, en kunde eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="cec03-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="cec03-246">En manuelt generert kvalitetsordre som viser til en salgsordre, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="cec03-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-247">Produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="cec03-247">Production order</span></span></td>
<td><span data-ttu-id="cec03-248">Før eller etter den ferdige kvaliteten for produksjonsordren er rapportert</span><span class="sxs-lookup"><span data-stu-id="cec03-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="cec03-249">Etter den ferdige kvaliteten for produksjonsordren er rapportert</span><span class="sxs-lookup"><span data-stu-id="cec03-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="cec03-250">Behovet for en kvalitetsordre kan reflektere et bestemt område eller en vare, eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="cec03-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="cec03-251">En manuelt generert kvalitetsordre som viser til en produksjonsordre, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="cec03-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-252">Produksjonsordre som har en ruteoperasjon</span><span class="sxs-lookup"><span data-stu-id="cec03-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="cec03-253">Før eller etter at rapporten for en operasjon er fullført</span><span class="sxs-lookup"><span data-stu-id="cec03-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="cec03-254">Etter at rapporteringen av produksjonen er fullført for den siste operasjonen</span><span class="sxs-lookup"><span data-stu-id="cec03-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="cec03-255">Behovet for en kvalitetsordre kan reflektere et bestemt område, en vare eller en operasjonsressurs eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="cec03-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="cec03-256">En manuelt generert kvalitetsordre som viser til en ruteoperasjon, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="cec03-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec03-257">Beholdning</span><span class="sxs-lookup"><span data-stu-id="cec03-257">Inventory</span></span></td>
<td><span data-ttu-id="cec03-258">En kvalitetsordre kan ikke genereres automatisk for en transaksjon innen en lagerjournal eller for overføringsordretransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="cec03-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="cec03-259">En kvalitetsordre må opprettes manuelt for en vares lagerantall.</span><span class="sxs-lookup"><span data-stu-id="cec03-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="cec03-260">Varens fysiske lagerbeholdning kreves.</span><span class="sxs-lookup"><span data-stu-id="cec03-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="cec03-261">Kvalitetsstyringssider</span><span class="sxs-lookup"><span data-stu-id="cec03-261">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cec03-262">Side</span><span class="sxs-lookup"><span data-stu-id="cec03-262">Page</span></span></th>
<th><span data-ttu-id="cec03-263">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cec03-263">Description</span></span></th>
<th><span data-ttu-id="cec03-264">Eksempel</span><span class="sxs-lookup"><span data-stu-id="cec03-264">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cec03-265">Kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="cec03-265">Quality associations</span></span></td>
<td><span data-ttu-id="cec03-266">Se tidligere deler av denne artikkelen.</span><span class="sxs-lookup"><span data-stu-id="cec03-266">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="cec03-267">En kvalitetstilknytning definerer alle følgende opplysninger om en kvalitetsordre som er generert:</span><span class="sxs-lookup"><span data-stu-id="cec03-267">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="cec03-268">Transaksjonshendelsen</span><span class="sxs-lookup"><span data-stu-id="cec03-268">The transaction event</span></span></li>
<li><span data-ttu-id="cec03-269">Settet med tester som må utføres på elementene</span><span class="sxs-lookup"><span data-stu-id="cec03-269">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="cec03-270">Det akseptable kvalitetsnivået</span><span class="sxs-lookup"><span data-stu-id="cec03-270">The AQL</span></span></li>
<li><span data-ttu-id="cec03-271">Prøveplanen</span><span class="sxs-lookup"><span data-stu-id="cec03-271">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="cec03-272">Du må definere en kvalitetstilknytning for hver variasjon i en forretningsprosess som krever automatisk generering av kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="cec03-272">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="cec03-273">Eksempelvis kan en kvalitetsordre genereres i forretningsprosessen for bestillinger, karanteneordrer, salgsordrer og produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="cec03-273">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cec03-274">Tester</span><span class="sxs-lookup"><span data-stu-id="cec03-274">Tests</span></span></td>
<td><span data-ttu-id="cec03-275">Bruk denne siden til å definere og vise de individuelle testene som fastslår om produktene oppfyller kvalitetsspesifikasjoner.</span><span class="sxs-lookup"><span data-stu-id="cec03-275">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="cec03-276">Du kan tilordne én eller flere individuelle tester til en testgruppe.</span><span class="sxs-lookup"><span data-stu-id="cec03-276">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="cec03-277">I dette tilfellet må også angi testspesifikk informasjon, for eksempel de akseptable målingsverdiene.</span><span class="sxs-lookup"><span data-stu-id="cec03-277">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="cec03-278">Målingsverdiene brukes for kvantitative tester, og testvariablene brukes for kvalitative tester.</span><span class="sxs-lookup"><span data-stu-id="cec03-278">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="cec03-279">En kvantitativ test har testtypen <strong>Heltall</strong> eller <strong>Brøk</strong> og har også en angitt måleenhet.</span><span class="sxs-lookup"><span data-stu-id="cec03-279">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="cec03-280">Kvalitetsspesifikasjoner og testresultater uttrykkes som tall.</span><span class="sxs-lookup"><span data-stu-id="cec03-280">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="cec03-281">En kvalitativ test har testtypen <strong>Alternativ</strong>.</span><span class="sxs-lookup"><span data-stu-id="cec03-281">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="cec03-282">Kvalitative tester krever mer informasjon om testvariabelen som måles, og de tilhørende opplistede alternativene.</span><span class="sxs-lookup"><span data-stu-id="cec03-282">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="cec03-283">Kvalitetsspesifikasjoner og testresultater uttrykkes i henhold til et resultat.</span><span class="sxs-lookup"><span data-stu-id="cec03-283">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="cec03-284">Et produksjonsfirma utfører to tester på innkjøpt materiale: en kvantitativ test om materialkvalitet og en kvalitativ test om emballasjeskade.</span><span class="sxs-lookup"><span data-stu-id="cec03-284">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="cec03-285">Firmaet definerer tilleggsinformasjon om den kvalitative testen for å identifisere testvariabelen (skadet emballasje) og resultatene.</span><span class="sxs-lookup"><span data-stu-id="cec03-285">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="cec03-286">Firmaet bruker <strong>Testgrupper</strong>-siden til å tilordne de to testene til en testgruppe og angi testspesifikk informasjon.</span><span class="sxs-lookup"><span data-stu-id="cec03-286">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="cec03-287">Testgruppen tilordnes til en kvalitetsordre, slik at firmaet kan rapportere testresultater for de to testene.</span><span class="sxs-lookup"><span data-stu-id="cec03-287">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cec03-288">Testgrupper</span><span class="sxs-lookup"><span data-stu-id="cec03-288">Test groups</span></span></td>
<td><span data-ttu-id="cec03-289">Bruk denne siden til å definere, redigere og vise testgrupper og de individuelle testene som er tilordnet til en testgruppe.</span><span class="sxs-lookup"><span data-stu-id="cec03-289">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="cec03-290">Den øvre ruten viser testgrupper, og den nedre ruten viser testene som er tilordnet til en valgt testgruppe.</span><span class="sxs-lookup"><span data-stu-id="cec03-290">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="cec03-291">Du tilordner flere policyer til en testgruppe, for eksempel en prøveplan, et akseptabelt kvalitetsnivå og kravet til destruktiv testing.</span><span class="sxs-lookup"><span data-stu-id="cec03-291">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="cec03-292">Når du tilordner en individuell test til en testgruppe, definerer du tilleggsinformasjon, for eksempel sekvensen, dokumenter og gyldighetsdatoer.</span><span class="sxs-lookup"><span data-stu-id="cec03-292">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="cec03-293">For en kvantitativ test inkluderer informasjonen du definerer, også de akseptable målingsverdiene.</span><span class="sxs-lookup"><span data-stu-id="cec03-293">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="cec03-294">For en kvalitativ test inkluderer informasjonen testvariabelen og standardresultatet.</span><span class="sxs-lookup"><span data-stu-id="cec03-294">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="cec03-295">Testgruppen som er tilordnet en kvalitetsordre, definerer standardsettet med tester som må utføres for den bestemte varen.</span><span class="sxs-lookup"><span data-stu-id="cec03-295">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="cec03-296">Du kan imidlertid legge til, slette eller endre tester i kvalitetsordren.</span><span class="sxs-lookup"><span data-stu-id="cec03-296">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="cec03-297">Testresultater rapporteres for hver test på en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="cec03-297">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="cec03-298">Et produksjonsfirma definerer en testgruppe for hver variasjon av retningslinjene for kvalitet.</span><span class="sxs-lookup"><span data-stu-id="cec03-298">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="cec03-299">De ulike testgruppene gjenspeiler forskjeller i prøveplanene, settet med tester som må utføres sammen, det akseptable kvalitetsnivået og andre faktorer.</span><span class="sxs-lookup"><span data-stu-id="cec03-299">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="cec03-300">For kvantitative tester er det også forskjeller i de akseptable målingsverdiene.</span><span class="sxs-lookup"><span data-stu-id="cec03-300">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="cec03-301">Hvis du vil fremtvinge retningslinjene for kvalitet, tilordner firmaet en testgruppe til hver regel for automatisk generering av kvalitetsordrer på siden <strong>Kvalitetstilknytninger</strong>, og tilordner også en testgruppe til kvalitetsordrer som opprettes manuelt.</span><span class="sxs-lookup"><span data-stu-id="cec03-301">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cec03-302">Varekvalitetsgrupper</span><span class="sxs-lookup"><span data-stu-id="cec03-302">Item quality groups</span></span></td>
<td><span data-ttu-id="cec03-303">Bruk denne siden til å definere, redigere og vise varene som er tilordnet til en kvalitetsgruppe, eller kvalitetsgruppene som er tilordnet til en vare.</span><span class="sxs-lookup"><span data-stu-id="cec03-303">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="cec03-304">En kvalitetsgruppe representerer felles testkrav for varer.</span><span class="sxs-lookup"><span data-stu-id="cec03-304">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="cec03-305">Når du har definert testkravene på siden <strong>Testgrupper</strong>, kan du definere reglene for automatisk generering av kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="cec03-305">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="cec03-306">For å forenkle prosessen kan du ikke definerer reglene for individuelle varer.</span><span class="sxs-lookup"><span data-stu-id="cec03-306">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="cec03-307">I stedet definere du regler for en kvalitetsgruppe ved hjelp av siden <strong>Kvalitetstilknytninger</strong>.</span><span class="sxs-lookup"><span data-stu-id="cec03-307">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="cec03-308">Du kan også bruke siden <strong>Varekvalitetsgrupper</strong> for en valgt kvalitetsgruppe for å tilordne relevante varer til denne gruppen.</span><span class="sxs-lookup"><span data-stu-id="cec03-308">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="cec03-309">Du kan også bruke siden <strong>Varekvalitetsgrupper</strong> for en valgt vare for å tilordne relevante kvalitetsgrupper til varen.</span><span class="sxs-lookup"><span data-stu-id="cec03-309">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="cec03-310">Et produksjonsfirma kjøper inn ulike råmaterialer som har samme testkrav for innkommende inspeksjon.</span><span class="sxs-lookup"><span data-stu-id="cec03-310">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="cec03-311">Firmaet definerer en kvalitetsgruppe og tilordner deretter varenumrene som er tilknyttet råvarene til denne gruppen.</span><span class="sxs-lookup"><span data-stu-id="cec03-311">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="cec03-312">Senere kjøper selskapet en ny type råvarer som har samme testkrav.</span><span class="sxs-lookup"><span data-stu-id="cec03-312">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="cec03-313">I stedet for å opprette nye testkrav for det nye materialet, legger firmaet til varenummeret for det nye materialet i den eksisterende kvalitetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="cec03-313">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="cec03-314">Det samme produksjonsfirmaet produserer også varer med samme krav til produksjonstesting, og leverer varer med samme krav til utføring av tester før forsendelse.</span><span class="sxs-lookup"><span data-stu-id="cec03-314">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="cec03-315">Firmaet definerer to ekstra kvalitetsgrupper, og tilordner deretter de aktuelle varenumrene til hver gruppe.</span><span class="sxs-lookup"><span data-stu-id="cec03-315">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cec03-316">Testvariabler</span><span class="sxs-lookup"><span data-stu-id="cec03-316">Test variables</span></span></td>
<td><span data-ttu-id="cec03-317">Bruk denne siden til å definere og vise variablene som er tilknyttet en kvalitativ test.</span><span class="sxs-lookup"><span data-stu-id="cec03-317">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="cec03-318">For hver variabel kan du definere opplistede resultater som representerer de mulige alternativene.</span><span class="sxs-lookup"><span data-stu-id="cec03-318">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="cec03-319">Du definerer testene på siden <strong>Tester</strong>.</span><span class="sxs-lookup"><span data-stu-id="cec03-319">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="cec03-320">Du må sette testtypen for kvalitative tester til <strong>Alternativ</strong>.</span><span class="sxs-lookup"><span data-stu-id="cec03-320">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="cec03-321">Bruk siden <strong>Testgrupper</strong> til å tilordne en testvariabel til en enkelt test.</span><span class="sxs-lookup"><span data-stu-id="cec03-321">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="cec03-322">En produksjonsfirma som produserer kjeks, bruker en inspeksjonstest til det ferdige produktet.</span><span class="sxs-lookup"><span data-stu-id="cec03-322">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="cec03-323">Denne inspeksjonstesten har flere variabler.</span><span class="sxs-lookup"><span data-stu-id="cec03-323">This inspection test has several variables.</span></span> <span data-ttu-id="cec03-324">Én variabel er smak, og de mulige resultatene for denne variabelen er god og dårlig.</span><span class="sxs-lookup"><span data-stu-id="cec03-324">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="cec03-325">En annen variabel er farge, og de mulige resultatene er for mørk, for lys og riktig.</span><span class="sxs-lookup"><span data-stu-id="cec03-325">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cec03-326">Testvariabelresultater</span><span class="sxs-lookup"><span data-stu-id="cec03-326">Test variable outcomes</span></span></td>
<td><span data-ttu-id="cec03-327">Bruk denne siden til å definere, redigere og vise de mulige testresultatene for en testvariabel som er knyttet til en kvalitetstest.</span><span class="sxs-lookup"><span data-stu-id="cec03-327">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="cec03-328">For hvert resultat tilordner du statusen <strong>bestått</strong> eller <strong>mislykket</strong>.</span><span class="sxs-lookup"><span data-stu-id="cec03-328">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="cec03-329">Du må definere en variabel og resultatene for hver kvalitative test som defineres på siden <strong>Tester</strong>.</span><span class="sxs-lookup"><span data-stu-id="cec03-329">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="cec03-330">(For kvalitative tester er testtypen satt til <strong>Alternativ</strong> på <strong>Tester</strong>-siden.) Bruk <strong>Testgrupper</strong>-siden til å tilordne en testvariabel og standardresultatet til en enkelt kvalitetstest.</span><span class="sxs-lookup"><span data-stu-id="cec03-330">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="cec03-331">En produksjonsfirma som produserer kjeks, bruker en inspeksjonstest til det ferdige produktet.</span><span class="sxs-lookup"><span data-stu-id="cec03-331">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="cec03-332">Denne inspeksjonstesten har flere variabler.</span><span class="sxs-lookup"><span data-stu-id="cec03-332">This inspection test has of several variables.</span></span> <span data-ttu-id="cec03-333">Én variabel er smak, og de mulige resultatene for denne variabelen er god og dårlig.</span><span class="sxs-lookup"><span data-stu-id="cec03-333">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="cec03-334">En annen variabel er farge, og de mulige resultatene er for mørk, for lys og riktig.</span><span class="sxs-lookup"><span data-stu-id="cec03-334">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="cec03-335">Statusen <strong>bestått</strong> eller <strong>mislykket</strong> tilordnes hvert resultat.</span><span class="sxs-lookup"><span data-stu-id="cec03-335">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="cec03-336">Under inspeksjonstesten for hver variabel rapporterer inspektøren testresultatet ved å velge ett av resultatene.</span><span class="sxs-lookup"><span data-stu-id="cec03-336">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="cec03-337">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="cec03-337">Additional resources</span></span>
--------

[<span data-ttu-id="cec03-338">Kvalitetsstyringsprosesser</span><span class="sxs-lookup"><span data-stu-id="cec03-338">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="cec03-339">Aktivere behandling av avvik</span><span class="sxs-lookup"><span data-stu-id="cec03-339">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)
