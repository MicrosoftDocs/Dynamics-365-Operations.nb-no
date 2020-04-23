---
title: Oversikt over kvalitetsstyring
description: Dette emnet beskriver hvordan du kan bruke kvalitetsstyring i Dynamics 365 Supply Chain Management for å forbedre produktkvalitet i forsyningskjeden.
author: perlynne
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b090450c6b39607f9661667f8063998bbe5ff52
ms.sourcegitcommit: c79062ba89498aa3fe3d86e478d9f32484f5f6dc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/03/2020
ms.locfileid: "3224915"
---
# <a name="quality-management-overview"></a><span data-ttu-id="d7116-103">Oversikt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="d7116-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7116-104">Dette emnet beskriver hvordan du kan bruke kvalitetsstyring i Dynamics 365 Supply Chain Management for å forbedre produktkvalitet i forsyningskjeden.</span><span class="sxs-lookup"><span data-stu-id="d7116-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="d7116-105">Kvalitetsstyring kan hjelpe deg med å administrere behandlingstiden når du håndterer produkter med avvik, uavhengig av opprinnelsespunktet.</span><span class="sxs-lookup"><span data-stu-id="d7116-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="d7116-106">Fordi diagnosetyper er knyttet til rettelsesrapportering, kan Supply Chain Management planlegge oppgaver for å rette opp problemer og hindre at de skjer igjen.</span><span class="sxs-lookup"><span data-stu-id="d7116-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="d7116-107">I tillegg til funksjonalitet for håndtering av avvik inneholder kvalitetsstyring funksjonalitet for å spore problemer etter problemtype (selv interne problemer) og identifisere løsninger som kortsiktige eller langsiktige.</span><span class="sxs-lookup"><span data-stu-id="d7116-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="d7116-108">Statistikk om nøkkelytelsesindikator (KPI-er) gir innsikt i loggen for tidligere avviksproblemer og løsninger som ble brukt til å rette feilene.</span><span class="sxs-lookup"><span data-stu-id="d7116-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="d7116-109">Du kan bruke historiske data for å undersøke effektiviteten til tidligere kvalitetsmål og bestemme nødvendige tiltak som skal brukes i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="d7116-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="d7116-110">Når du definerer en kvalitetstilknytning, kan Supply Chain Management generere kvalitetsordrer for diverse forretningsprosesser, hendelser og betingelser.</span><span class="sxs-lookup"><span data-stu-id="d7116-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="d7116-111">Kvalitetstilknytningen kan dekke en bestemt vare, en bestemt varegruppe eller alle varer.</span><span class="sxs-lookup"><span data-stu-id="d7116-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="d7116-112">Eksempler på bruk av kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="d7116-112">Examples of the use of quality management</span></span>
<span data-ttu-id="d7116-113">Kvalitetsstyring er fleksibelt og kan implementeres på forskjellige måter for å oppfylle kravene til bestemte typer forsyningskjedeoperasjoner.</span><span class="sxs-lookup"><span data-stu-id="d7116-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="d7116-114">Følgende eksempel viser mulig bruk av disse funksjonene.</span><span class="sxs-lookup"><span data-stu-id="d7116-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="d7116-115">Start en prosess for kvalitetskontroll automatisk basert på forhåndsdefinerte kriterier (ved lagerregistrering av en bestilling fra en bestemt leverandør).</span><span class="sxs-lookup"><span data-stu-id="d7116-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="d7116-116">Blokker lageret under inspeksjon for å hindre bruk av ikke-godkjent lager (full blokkering av bestillingsantall).</span><span class="sxs-lookup"><span data-stu-id="d7116-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="d7116-117">Bruk vareprøver som en del av en kvalitetstilknytning for å definere hvor mye av det fysiske lageret som må kontrolleres.</span><span class="sxs-lookup"><span data-stu-id="d7116-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="d7116-118">Prøver kan være basert på faste antall eller en prosentdel.</span><span class="sxs-lookup"><span data-stu-id="d7116-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="d7116-119">Opprette kvalitetsordrer for delvise mottak.</span><span class="sxs-lookup"><span data-stu-id="d7116-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="d7116-120">Hvis du vil opprette en kvalitetsordre som er basert på antallet som er fysisk mottatt med en ordre, må du velge den **Per oppdatert mengde** for den **Vareprøve** skjema.</span><span class="sxs-lookup"><span data-stu-id="d7116-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="d7116-121">Opprett testtyper med minimums-, maksimums-, og måltestverdier, og utfør kvalitative kontra kvantitative tester som har forhåndsdefinerte valideringsresultater.</span><span class="sxs-lookup"><span data-stu-id="d7116-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="d7116-122">Angi et akseptabelt kvalitetsnivå for å kontrollere kvalitetsmåltoleranser.</span><span class="sxs-lookup"><span data-stu-id="d7116-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="d7116-123">Angi ressursene som en inspeksjonsoperasjon krever, for eksempel et testområde og testinstrumenter.</span><span class="sxs-lookup"><span data-stu-id="d7116-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="d7116-124">Arbeide med kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="d7116-124">Working with quality associations</span></span>
<span data-ttu-id="d7116-125">Forretningsprosessen som bruker en kvalitetstilknytning, kan knyttes til ulike kildedokumenter, for eksempel bestillinger, salgsordrer eller produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="d7116-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="d7116-126">Hver kvalitetstilknytningspost definerer settet med tester, det akseptable kvalitetsnivået og samplingplanen som gjelder for kvalitetsordrene som genereres.</span><span class="sxs-lookup"><span data-stu-id="d7116-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="d7116-127">Du må definere en kvalitetstilknytningspost for hver variasjon i en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="d7116-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="d7116-128">Du kan for eksempel definere en kvalitetstilknytning som genererer en kvalitetsordre når et produkt for bestillingsmottak oppdateres.</span><span class="sxs-lookup"><span data-stu-id="d7116-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="d7116-129">Avhengig av oppsettet for utførelsesplanen kan selve utløsingsprosessen blokkeres når det finnes en åpen kvalitetsordre, eller de neste prosessene, for eksempel bestillingsfakturering, kan blokkeres.</span><span class="sxs-lookup"><span data-stu-id="d7116-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="d7116-130">**Merk:** Når det finnes åpne kvalitetsordrer, blokkeres lagerantall automatisk fra å bli utstedt.</span><span class="sxs-lookup"><span data-stu-id="d7116-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="d7116-131">Avhengig av **Full blokkering**-innstillingen på siden **Vareprøver** er antallet enten antallet på kvalitetsordren eller antallet på kildedokumentlinjen.</span><span class="sxs-lookup"><span data-stu-id="d7116-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="d7116-132">For en gitt forretningsprosess identifiserer kvalitetstilknytningspost hendelsen og betingelsene som en kvalitetsordre genereres for.</span><span class="sxs-lookup"><span data-stu-id="d7116-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="d7116-133">Betingelsene kan være spesifikke for et område eller en juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="d7116-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="d7116-134">En kvalitetsordre som omfatter destruktive tester, kan bare genereres når hvis det finnes lagerbeholdning for hendelsen.</span><span class="sxs-lookup"><span data-stu-id="d7116-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="d7116-135">De følgende eksemplene illustrerer hvordan en kvalitetstilknytningspost er definert for variasjonene innen ulike forretningsprosesser.</span><span class="sxs-lookup"><span data-stu-id="d7116-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="d7116-136">For hvert eksempel oppsummere følgende tabell hendelsene og betingelsene som er definert av en kvalitetstilknytningspost.</span><span class="sxs-lookup"><span data-stu-id="d7116-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="d7116-137">Referansetype</span><span class="sxs-lookup"><span data-stu-id="d7116-137">Reference type</span></span></th>
<th><span data-ttu-id="d7116-138">Hendelsestype</span><span class="sxs-lookup"><span data-stu-id="d7116-138">Event type</span></span></th>
<th><span data-ttu-id="d7116-139">Utførelse</span><span class="sxs-lookup"><span data-stu-id="d7116-139">Execution</span></span></th>
<th><span data-ttu-id="d7116-140">Hendelsesblokkering</span><span class="sxs-lookup"><span data-stu-id="d7116-140">Event blocking</span></span></th>
<th><span data-ttu-id="d7116-141">Dokumentreferanse</span><span class="sxs-lookup"><span data-stu-id="d7116-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="d7116-142">Beholdning</span><span class="sxs-lookup"><span data-stu-id="d7116-142">Inventory</span></span></td>
<td><span data-ttu-id="d7116-143">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="d7116-143">Not applicable</span></span></td>
<td><span data-ttu-id="d7116-144">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="d7116-144">Not applicable</span></span></td>
<td><span data-ttu-id="d7116-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7116-145">None</span></span></td>
<td><span data-ttu-id="d7116-146">Alle</span><span class="sxs-lookup"><span data-stu-id="d7116-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="d7116-147">Salg</span><span class="sxs-lookup"><span data-stu-id="d7116-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="d7116-148">Plukkingsprosess er planlagt</span><span class="sxs-lookup"><span data-stu-id="d7116-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="d7116-149">Før</span><span class="sxs-lookup"><span data-stu-id="d7116-149">Before</span></span></td>
<td><span data-ttu-id="d7116-150">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7116-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="d7116-151">Bare Spesifikk ID, Gruppe eller Alle</span><span class="sxs-lookup"><span data-stu-id="d7116-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-152">Plukkingsprosess</span><span class="sxs-lookup"><span data-stu-id="d7116-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-153">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="d7116-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-154">Faktura</span><span class="sxs-lookup"><span data-stu-id="d7116-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d7116-155">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="d7116-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="d7116-156">Før</span><span class="sxs-lookup"><span data-stu-id="d7116-156">Before</span></span></td>
<td><span data-ttu-id="d7116-157">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7116-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-158">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="d7116-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-159">Faktura</span><span class="sxs-lookup"><span data-stu-id="d7116-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="d7116-160">Kjøp</span><span class="sxs-lookup"><span data-stu-id="d7116-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="d7116-161">Kvitteringsliste</span><span class="sxs-lookup"><span data-stu-id="d7116-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="d7116-162">Før</span><span class="sxs-lookup"><span data-stu-id="d7116-162">Before</span></span></td>
<td><span data-ttu-id="d7116-163">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7116-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-164">Kvitteringsliste</span><span class="sxs-lookup"><span data-stu-id="d7116-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-165">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="d7116-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-166">Faktura</span><span class="sxs-lookup"><span data-stu-id="d7116-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d7116-167">Etter</span><span class="sxs-lookup"><span data-stu-id="d7116-167">After</span></span></td>
<td><span data-ttu-id="d7116-168">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7116-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-169">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="d7116-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-170">Faktura</span><span class="sxs-lookup"><span data-stu-id="d7116-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d7116-171">Registrering</span><span class="sxs-lookup"><span data-stu-id="d7116-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="d7116-172">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="d7116-172">Not applicable</span></span></td>
<td><span data-ttu-id="d7116-173">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7116-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-174">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="d7116-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-175">Faktura</span><span class="sxs-lookup"><span data-stu-id="d7116-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="d7116-176">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="d7116-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="d7116-177">Før</span><span class="sxs-lookup"><span data-stu-id="d7116-177">Before</span></span></td>
<td><span data-ttu-id="d7116-178">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7116-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-179">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="d7116-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-180">Faktura</span><span class="sxs-lookup"><span data-stu-id="d7116-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d7116-181">Etter</span><span class="sxs-lookup"><span data-stu-id="d7116-181">After</span></span></td>
<td><span data-ttu-id="d7116-182">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7116-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-183">Faktura</span><span class="sxs-lookup"><span data-stu-id="d7116-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="d7116-184">Produksjon</span><span class="sxs-lookup"><span data-stu-id="d7116-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="d7116-185">Registrering</span><span class="sxs-lookup"><span data-stu-id="d7116-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="d7116-186">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="d7116-186">Not applicable</span></span></td>
<td><span data-ttu-id="d7116-187">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7116-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="d7116-188">Alle</span><span class="sxs-lookup"><span data-stu-id="d7116-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-189">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="d7116-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-190">Slutt</span><span class="sxs-lookup"><span data-stu-id="d7116-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="d7116-191">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="d7116-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="d7116-192">Før</span><span class="sxs-lookup"><span data-stu-id="d7116-192">Before</span></span></td>
<td><span data-ttu-id="d7116-193">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7116-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-194">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="d7116-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-195">Slutt</span><span class="sxs-lookup"><span data-stu-id="d7116-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d7116-196">Etter</span><span class="sxs-lookup"><span data-stu-id="d7116-196">After</span></span></td>
<td><span data-ttu-id="d7116-197">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7116-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-198">Slutt</span><span class="sxs-lookup"><span data-stu-id="d7116-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="d7116-199">Karantene</span><span class="sxs-lookup"><span data-stu-id="d7116-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="d7116-200">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="d7116-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="d7116-201">Før</span><span class="sxs-lookup"><span data-stu-id="d7116-201">Before</span></span></td>
<td><span data-ttu-id="d7116-202">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="d7116-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-203">Slutt</span><span class="sxs-lookup"><span data-stu-id="d7116-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-204">Etter</span><span class="sxs-lookup"><span data-stu-id="d7116-204">After</span></span></td>
<td><span data-ttu-id="d7116-205">Slutt</span><span class="sxs-lookup"><span data-stu-id="d7116-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-206">Slutt</span><span class="sxs-lookup"><span data-stu-id="d7116-206">End</span></span></td>
<td><span data-ttu-id="d7116-207">Før</span><span class="sxs-lookup"><span data-stu-id="d7116-207">Before</span></span></td>
<td><span data-ttu-id="d7116-208">Slutt</span><span class="sxs-lookup"><span data-stu-id="d7116-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d7116-209">Ruteoperasjon</span><span class="sxs-lookup"><span data-stu-id="d7116-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="d7116-210">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="d7116-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="d7116-211">Før</span><span class="sxs-lookup"><span data-stu-id="d7116-211">Before</span></span></td>
<td><span data-ttu-id="d7116-212">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7116-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="d7116-213">Bestemt ID, Gruppe eller Alle, og Ressursspesifikk, Gruppe eller Alle</span><span class="sxs-lookup"><span data-stu-id="d7116-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-214">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="d7116-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-215">Etter</span><span class="sxs-lookup"><span data-stu-id="d7116-215">After</span></span></td>
<td><span data-ttu-id="d7116-216">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7116-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d7116-217">Koproduktproduksjon</span><span class="sxs-lookup"><span data-stu-id="d7116-217">Co-product production</span></span></td>
<td><span data-ttu-id="d7116-218">Registrering</span><span class="sxs-lookup"><span data-stu-id="d7116-218">Registration</span></span></td>
<td><span data-ttu-id="d7116-219">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="d7116-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d7116-220">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7116-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="d7116-221">Alle</span><span class="sxs-lookup"><span data-stu-id="d7116-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d7116-222">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="d7116-222">Report as finished</span></span></td>
<td><span data-ttu-id="d7116-223">Før</span><span class="sxs-lookup"><span data-stu-id="d7116-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-224">Etter</span><span class="sxs-lookup"><span data-stu-id="d7116-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d7116-225">Tabellen nedenfor inneholder mer informasjon om hvordan kvalitetsordrer kan genereres for bestemte typer prosesser.</span><span class="sxs-lookup"><span data-stu-id="d7116-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="d7116-226">Type av prosess</span><span class="sxs-lookup"><span data-stu-id="d7116-226">Type of process</span></span></th>
<th><span data-ttu-id="d7116-227">Når kvalitetsordrer kan genereres automatisk</span><span class="sxs-lookup"><span data-stu-id="d7116-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="d7116-228">Når kvalitetsordrer kan genereres hvis destruktiv testing kreves</span><span class="sxs-lookup"><span data-stu-id="d7116-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="d7116-229">Betingelsesinformasjon</span><span class="sxs-lookup"><span data-stu-id="d7116-229">Condition information</span></span></th>
<th><span data-ttu-id="d7116-230">Informasjon om manuell generering</span><span class="sxs-lookup"><span data-stu-id="d7116-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="d7116-231">Bestilling</span><span class="sxs-lookup"><span data-stu-id="d7116-231">Purchase order</span></span></td>
<td><span data-ttu-id="d7116-232">Før eller etter en kvitteringsliste eller produktkvittering for materialet som mottas, posteres</span><span class="sxs-lookup"><span data-stu-id="d7116-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="d7116-233">Etter produktkvitteringen for materialet som mottas, er postert, fordi materialet må være tilgjengelig for destruktiv testing</span><span class="sxs-lookup"><span data-stu-id="d7116-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="d7116-234">Behovet for en kvalitetsordre kan reflektere et bestemt område, en vare, en leverandør eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="d7116-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d7116-235">En manuelt generert kvalitetsordre som viser til en bestilling, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="d7116-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-236">Karanteneordre</span><span class="sxs-lookup"><span data-stu-id="d7116-236">Quarantine order</span></span></td>
<td><span data-ttu-id="d7116-237">Før eller etter karanteordren er rapportert som fullført eller avsluttet</span><span class="sxs-lookup"><span data-stu-id="d7116-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="d7116-238">Kvalitetsordrer som krever destruktive tester, kan ikke genereres.</span><span class="sxs-lookup"><span data-stu-id="d7116-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="d7116-239">Det forutsettes at karanteneordrefunksjonaliteten behandler disposisjonen av materialet som blir ødelagt.</span><span class="sxs-lookup"><span data-stu-id="d7116-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="d7116-240">Behovet for en kvalitetsordre kan reflektere et bestemt område, en vare, en leverandør eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="d7116-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d7116-241">En manuelt generert kvalitetsordre som viser til en karanteneordre, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="d7116-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-242">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="d7116-242">Sales order</span></span></td>
<td><span data-ttu-id="d7116-243">Før en planlagt plukkeprosessen eller følgeseddeloppdatering for varene som leveres</span><span class="sxs-lookup"><span data-stu-id="d7116-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="d7116-244">I alle trinn</span><span class="sxs-lookup"><span data-stu-id="d7116-244">At any step</span></span></td>
<td><span data-ttu-id="d7116-245">Kravet til en kvalitetsordre kan reflektere et bestemt område, en vare, en kunde eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="d7116-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d7116-246">En manuelt generert kvalitetsordre som viser til en salgsordre, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="d7116-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-247">Produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="d7116-247">Production order</span></span></td>
<td><span data-ttu-id="d7116-248">Før eller etter den ferdige kvaliteten for produksjonsordren er rapportert</span><span class="sxs-lookup"><span data-stu-id="d7116-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="d7116-249">Etter den ferdige kvaliteten for produksjonsordren er rapportert</span><span class="sxs-lookup"><span data-stu-id="d7116-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="d7116-250">Behovet for en kvalitetsordre kan reflektere et bestemt område eller en vare, eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="d7116-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d7116-251">En manuelt generert kvalitetsordre som viser til en produksjonsordre, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="d7116-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-252">Produksjonsordre som har en ruteoperasjon</span><span class="sxs-lookup"><span data-stu-id="d7116-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="d7116-253">Før eller etter at rapporten for en operasjon er fullført</span><span class="sxs-lookup"><span data-stu-id="d7116-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="d7116-254">Etter at rapporteringen av produksjonen er fullført for den siste operasjonen</span><span class="sxs-lookup"><span data-stu-id="d7116-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="d7116-255">Behovet for en kvalitetsordre kan reflektere et bestemt område, en vare eller en operasjonsressurs eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="d7116-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d7116-256">En manuelt generert kvalitetsordre som viser til en ruteoperasjon, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="d7116-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d7116-257">Beholdning</span><span class="sxs-lookup"><span data-stu-id="d7116-257">Inventory</span></span></td>
<td><span data-ttu-id="d7116-258">En kvalitetsordre kan ikke genereres automatisk for en transaksjon innen en lagerjournal eller for overføringsordretransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="d7116-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="d7116-259">En kvalitetsordre må opprettes manuelt for en vares lagerantall.</span><span class="sxs-lookup"><span data-stu-id="d7116-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="d7116-260">Varens fysiske lagerbeholdning kreves.</span><span class="sxs-lookup"><span data-stu-id="d7116-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="d7116-261">Eksempler på automatisk generering av kvalitetsordre</span><span class="sxs-lookup"><span data-stu-id="d7116-261">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="d7116-262">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="d7116-262">Purchasing</span></span>

<span data-ttu-id="d7116-263">I innkjøp, hvis du du angir feltet **Hendelsestype** til **Produktkvittering** og feltet **Utførelse** til **Etter** på siden **Kvalitetstilknytninger**, får du følgende resultater:</span><span class="sxs-lookup"><span data-stu-id="d7116-263">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="d7116-264">Hvis alternativet **Per oppdatert mengde** er satt til **Ja**, genereres det en kvalitetsordre for hvert mottak mot bestillingen basert på det mottatte antallet og innstillingene i vareprøven.</span><span class="sxs-lookup"><span data-stu-id="d7116-264">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="d7116-265">Hver gang et antall mottas mot bestillingen, genereres nye kvalitetsordrer basert på det nylig mottatte antallet.</span><span class="sxs-lookup"><span data-stu-id="d7116-265">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="d7116-266">Hvis alternativet **Per oppdatert mengde** er satt til **Nei**, genereres det en kvalitetsordre for det første mottaket mot bestillingen basert på det mottatte antallet.</span><span class="sxs-lookup"><span data-stu-id="d7116-266">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="d7116-267">I tillegg blir én eller flere kvalitetsordrer opprettet på grunnlag av restantallet, avhengig av sporingsdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="d7116-267">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="d7116-268">Kvalitetsordrer genereres ikke for etterfølgende mottak mot bestillingen.</span><span class="sxs-lookup"><span data-stu-id="d7116-268">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="d7116-269">Produksjon</span><span class="sxs-lookup"><span data-stu-id="d7116-269">Production</span></span>

<span data-ttu-id="d7116-270">I produksjon, hvis du du angir feltet **Hendelsestype** til **Ferdigmeld** og feltet **Utførelse** til **Etter** på siden **Kvalitetstilknytninger**, får du følgende resultater:</span><span class="sxs-lookup"><span data-stu-id="d7116-270">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="d7116-271">Hvis alternativet **Per oppdatert mengde** er satt til **Ja**, genereres det en kvalitetsordre for hver fullførte antall og innstillingene i vareprøven.</span><span class="sxs-lookup"><span data-stu-id="d7116-271">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="d7116-272">Hver gang et antall rapporteres som fullført mot produksjonsordren, genereres nye kvalitetsordrer basert på det nylig fullførte antallet.</span><span class="sxs-lookup"><span data-stu-id="d7116-272">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="d7116-273">Denne genereringslogikken er konsekvent med innkjøp.</span><span class="sxs-lookup"><span data-stu-id="d7116-273">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="d7116-274">Hvis alternativet **Per oppdatert mengde** er satt til **Nei**, genereres det en kvalitetsordre første gang antallet rapporteres som fullført, basert på det fullførte antallet.</span><span class="sxs-lookup"><span data-stu-id="d7116-274">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="d7116-275">I tillegg blir én eller flere kvalitetsordrer opprettet på grunnlag av restantallet, avhengig av sporingsdimensjonene for vareprøven.</span><span class="sxs-lookup"><span data-stu-id="d7116-275">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="d7116-276">Kvalitetsordrer genereres ikke for etterfølgende ferdigmeldte antall.</span><span class="sxs-lookup"><span data-stu-id="d7116-276">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="d7116-277">Kvalitetsspesifikasjon</span><span class="sxs-lookup"><span data-stu-id="d7116-277">Quality specification</span></span></th>
<th><span data-ttu-id="d7116-278">Per oppdatert mengde</span><span class="sxs-lookup"><span data-stu-id="d7116-278">Per updated quantity</span></span></th>
<th><span data-ttu-id="d7116-279">Per sporingsdimensjon</span><span class="sxs-lookup"><span data-stu-id="d7116-279">Per tracking dimension</span></span></th>
<th><span data-ttu-id="d7116-280">Resultat</span><span class="sxs-lookup"><span data-stu-id="d7116-280">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="d7116-281">Prosent: 10 %</span><span class="sxs-lookup"><span data-stu-id="d7116-281">Percentage: 10%</span></span></td>
<td><span data-ttu-id="d7116-282">Ja</span><span class="sxs-lookup"><span data-stu-id="d7116-282">Yes</span></span></td>
<td>
<p><span data-ttu-id="d7116-283">Partinummer: Nei</span><span class="sxs-lookup"><span data-stu-id="d7116-283">Batch number: No</span></span></p>
<p><span data-ttu-id="d7116-284">Serienummer: Nei</span><span class="sxs-lookup"><span data-stu-id="d7116-284">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="d7116-285">Ordreantall: 100</span><span class="sxs-lookup"><span data-stu-id="d7116-285">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="d7116-286">Rapporter som ferdig for 30</span><span class="sxs-lookup"><span data-stu-id="d7116-286">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="d7116-287">Kvalitetsordre #1 for 3 (10 % av 30)</span><span class="sxs-lookup"><span data-stu-id="d7116-287">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="d7116-288">Rapporter som ferdig for 70</span><span class="sxs-lookup"><span data-stu-id="d7116-288">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="d7116-289">Kvalitetsordre #2 for 7 (10 % av restordreantallet, som er lik 70 i dette tilfellet)</span><span class="sxs-lookup"><span data-stu-id="d7116-289">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="d7116-290">Fast antall: 1</span><span class="sxs-lookup"><span data-stu-id="d7116-290">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="d7116-291">Nei</span><span class="sxs-lookup"><span data-stu-id="d7116-291">No</span></span></td>
<td>
<p><span data-ttu-id="d7116-292">Partinummer: Nei</span><span class="sxs-lookup"><span data-stu-id="d7116-292">Batch number: No</span></span></p>
<p><span data-ttu-id="d7116-293">Serienummer: Nei</span><span class="sxs-lookup"><span data-stu-id="d7116-293">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="d7116-294">Ordreantall: 100</span><span class="sxs-lookup"><span data-stu-id="d7116-294">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="d7116-295">Rapporter som ferdig for 30</span><span class="sxs-lookup"><span data-stu-id="d7116-295">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="d7116-296">Kvalitetsordre #1 for 1 (for det første ferdigmeldte antallet, som har en fast verdi på 1)</span><span class="sxs-lookup"><span data-stu-id="d7116-296">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="d7116-297">Kvalitetsordre #2 for 1 (for det resterende antallet, som fremdeles har en fast verdi på 1)</span><span class="sxs-lookup"><span data-stu-id="d7116-297">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="d7116-298">Rapporter som ferdig for 10</span><span class="sxs-lookup"><span data-stu-id="d7116-298">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="d7116-299">Ingen kvalitetsordrer er opprettet.</span><span class="sxs-lookup"><span data-stu-id="d7116-299">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="d7116-300">Rapporter som ferdig for 60</span><span class="sxs-lookup"><span data-stu-id="d7116-300">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="d7116-301">Ingen kvalitetsordrer er opprettet.</span><span class="sxs-lookup"><span data-stu-id="d7116-301">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="d7116-302">Fast antall: 1</span><span class="sxs-lookup"><span data-stu-id="d7116-302">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="d7116-303">Ja</span><span class="sxs-lookup"><span data-stu-id="d7116-303">Yes</span></span></td>
<td>
<p><span data-ttu-id="d7116-304">Partinummer: Ja</span><span class="sxs-lookup"><span data-stu-id="d7116-304">Batch number: Yes</span></span></p>
<p><span data-ttu-id="d7116-305">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="d7116-305">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="d7116-306">Ordreantall: 10</span><span class="sxs-lookup"><span data-stu-id="d7116-306">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="d7116-307">Rapporter som ferdig for 3: 1 for #b1, #s1; 1 for #b2, #s2; og 1 for #b3, #s3</span><span class="sxs-lookup"><span data-stu-id="d7116-307">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="d7116-308">Kvalitetsordre #1 for 1 av parti #b1, serie #s1</span><span class="sxs-lookup"><span data-stu-id="d7116-308">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="d7116-309">Kvalitetsordre #2 for 1 av parti #b2, serie #s2</span><span class="sxs-lookup"><span data-stu-id="d7116-309">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="d7116-310">Kvalitetsordre #3 for 1 av parti #b3, serie #s3</span><span class="sxs-lookup"><span data-stu-id="d7116-310">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="d7116-311">Rapporter som ferdig for 2: 1 for #b4, #s4; og 1 for #b5, #s5</span><span class="sxs-lookup"><span data-stu-id="d7116-311">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="d7116-312">Kvalitetsordre #4 for 1 av parti #b4, serie #s4</span><span class="sxs-lookup"><span data-stu-id="d7116-312">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="d7116-313">Kvalitetsordre #5 for 1 av parti #b5, serie #s5</span><span class="sxs-lookup"><span data-stu-id="d7116-313">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="d7116-314"><strong>Merk:</strong> Partiet kan brukes på nytt.</span><span class="sxs-lookup"><span data-stu-id="d7116-314"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="d7116-315">Fast antall: 2</span><span class="sxs-lookup"><span data-stu-id="d7116-315">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="d7116-316">Nei</span><span class="sxs-lookup"><span data-stu-id="d7116-316">No</span></span></td>
<td>
<p><span data-ttu-id="d7116-317">Partinummer: Ja</span><span class="sxs-lookup"><span data-stu-id="d7116-317">Batch number: Yes</span></span></p>
<p><span data-ttu-id="d7116-318">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="d7116-318">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="d7116-319">Ordreantall: 10</span><span class="sxs-lookup"><span data-stu-id="d7116-319">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="d7116-320">Rapporter som ferdig for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; og 1 for #b4, #s4</span><span class="sxs-lookup"><span data-stu-id="d7116-320">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="d7116-321">Kvalitetsordre #1 for 1 av parti #b1, serie #s1</span><span class="sxs-lookup"><span data-stu-id="d7116-321">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="d7116-322">Kvalitetsordre #2 for 1 av parti #b2, serie #s2</span><span class="sxs-lookup"><span data-stu-id="d7116-322">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="d7116-323">Kvalitetsordre #3 for 1 av parti #b3, serie #s3</span><span class="sxs-lookup"><span data-stu-id="d7116-323">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="d7116-324">Kvalitetsordre #4 for 1 av parti #b4, serie #s4</span><span class="sxs-lookup"><span data-stu-id="d7116-324">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="d7116-325">Kvalitetsordre #5 for 2, uten referanse til et parti og et serienummer</span><span class="sxs-lookup"><span data-stu-id="d7116-325">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="d7116-326">Rapporter som ferdig for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; og 1 for #b10, #s10</span><span class="sxs-lookup"><span data-stu-id="d7116-326">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="d7116-327">Ingen kvalitetsordrer er opprettet.</span><span class="sxs-lookup"><span data-stu-id="d7116-327">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="d7116-328">Kvalitetsstyringssider</span><span class="sxs-lookup"><span data-stu-id="d7116-328">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7116-329">Side</span><span class="sxs-lookup"><span data-stu-id="d7116-329">Page</span></span></th>
<th><span data-ttu-id="d7116-330">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d7116-330">Description</span></span></th>
<th><span data-ttu-id="d7116-331">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d7116-331">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d7116-332">Kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="d7116-332">Quality associations</span></span></td>
<td><span data-ttu-id="d7116-333">Se tidligere deler av denne artikkelen.</span><span class="sxs-lookup"><span data-stu-id="d7116-333">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="d7116-334">En kvalitetstilknytning definerer alle følgende opplysninger om en kvalitetsordre som er generert:</span><span class="sxs-lookup"><span data-stu-id="d7116-334">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="d7116-335">Transaksjonshendelsen</span><span class="sxs-lookup"><span data-stu-id="d7116-335">The transaction event</span></span></li>
<li><span data-ttu-id="d7116-336">Settet med tester som må utføres på elementene</span><span class="sxs-lookup"><span data-stu-id="d7116-336">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="d7116-337">Det akseptable kvalitetsnivået</span><span class="sxs-lookup"><span data-stu-id="d7116-337">The AQL</span></span></li>
<li><span data-ttu-id="d7116-338">Prøveplanen</span><span class="sxs-lookup"><span data-stu-id="d7116-338">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="d7116-339">Du må definere en kvalitetstilknytning for hver variasjon i en forretningsprosess som krever automatisk generering av kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="d7116-339">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="d7116-340">Eksempelvis kan en kvalitetsordre genereres i forretningsprosessen for bestillinger, karanteneordrer, salgsordrer og produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="d7116-340">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7116-341">Tester</span><span class="sxs-lookup"><span data-stu-id="d7116-341">Tests</span></span></td>
<td><span data-ttu-id="d7116-342">Bruk denne siden til å definere og vise de individuelle testene som fastslår om produktene oppfyller kvalitetsspesifikasjoner.</span><span class="sxs-lookup"><span data-stu-id="d7116-342">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="d7116-343">Du kan tilordne én eller flere individuelle tester til en testgruppe.</span><span class="sxs-lookup"><span data-stu-id="d7116-343">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="d7116-344">I dette tilfellet må også angi testspesifikk informasjon, for eksempel de akseptable målingsverdiene.</span><span class="sxs-lookup"><span data-stu-id="d7116-344">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="d7116-345">Målingsverdiene brukes for kvantitative tester, og testvariablene brukes for kvalitative tester.</span><span class="sxs-lookup"><span data-stu-id="d7116-345">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="d7116-346">En kvantitativ test har testtypen <strong>Heltall</strong> eller <strong>Brøk</strong> og har også en angitt måleenhet.</span><span class="sxs-lookup"><span data-stu-id="d7116-346">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="d7116-347">Kvalitetsspesifikasjoner og testresultater uttrykkes som tall.</span><span class="sxs-lookup"><span data-stu-id="d7116-347">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="d7116-348">En kvalitativ test har testtypen <strong>Alternativ</strong>.</span><span class="sxs-lookup"><span data-stu-id="d7116-348">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="d7116-349">Kvalitative tester krever mer informasjon om testvariabelen som måles, og de tilhørende opplistede alternativene.</span><span class="sxs-lookup"><span data-stu-id="d7116-349">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="d7116-350">Kvalitetsspesifikasjoner og testresultater uttrykkes i henhold til et resultat.</span><span class="sxs-lookup"><span data-stu-id="d7116-350">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="d7116-351">Et produksjonsfirma utfører to tester på innkjøpt materiale: en kvantitativ test om materialkvalitet og en kvalitativ test om emballasjeskade.</span><span class="sxs-lookup"><span data-stu-id="d7116-351">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="d7116-352">Firmaet definerer tilleggsinformasjon om den kvalitative testen for å identifisere testvariabelen (skadet emballasje) og resultatene.</span><span class="sxs-lookup"><span data-stu-id="d7116-352">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="d7116-353">Firmaet bruker <strong>Testgrupper</strong>-siden til å tilordne de to testene til en testgruppe og angi testspesifikk informasjon.</span><span class="sxs-lookup"><span data-stu-id="d7116-353">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="d7116-354">Testgruppen tilordnes til en kvalitetsordre, slik at firmaet kan rapportere testresultater for de to testene.</span><span class="sxs-lookup"><span data-stu-id="d7116-354">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7116-355">Testgrupper</span><span class="sxs-lookup"><span data-stu-id="d7116-355">Test groups</span></span></td>
<td><span data-ttu-id="d7116-356">Bruk denne siden til å definere, redigere og vise testgrupper og de individuelle testene som er tilordnet til en testgruppe.</span><span class="sxs-lookup"><span data-stu-id="d7116-356">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="d7116-357">Den øvre ruten viser testgrupper, og den nedre ruten viser testene som er tilordnet til en valgt testgruppe.</span><span class="sxs-lookup"><span data-stu-id="d7116-357">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="d7116-358">Du tilordner flere policyer til en testgruppe, for eksempel en prøveplan, et akseptabelt kvalitetsnivå og kravet til destruktiv testing.</span><span class="sxs-lookup"><span data-stu-id="d7116-358">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="d7116-359">Når du tilordner en individuell test til en testgruppe, definerer du tilleggsinformasjon, for eksempel sekvensen, dokumenter og gyldighetsdatoer.</span><span class="sxs-lookup"><span data-stu-id="d7116-359">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="d7116-360">For en kvantitativ test inkluderer informasjonen du definerer, også de akseptable målingsverdiene.</span><span class="sxs-lookup"><span data-stu-id="d7116-360">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="d7116-361">For en kvalitativ test inkluderer informasjonen testvariabelen og standardresultatet.</span><span class="sxs-lookup"><span data-stu-id="d7116-361">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="d7116-362">Testgruppen som er tilordnet en kvalitetsordre, definerer standardsettet med tester som må utføres for den bestemte varen.</span><span class="sxs-lookup"><span data-stu-id="d7116-362">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="d7116-363">Du kan imidlertid legge til, slette eller endre tester i kvalitetsordren.</span><span class="sxs-lookup"><span data-stu-id="d7116-363">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="d7116-364">Testresultater rapporteres for hver test på en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="d7116-364">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="d7116-365">Et produksjonsfirma definerer en testgruppe for hver variasjon av retningslinjene for kvalitet.</span><span class="sxs-lookup"><span data-stu-id="d7116-365">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="d7116-366">De ulike testgruppene gjenspeiler forskjeller i prøveplanene, settet med tester som må utføres sammen, det akseptable kvalitetsnivået og andre faktorer.</span><span class="sxs-lookup"><span data-stu-id="d7116-366">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="d7116-367">For kvantitative tester er det også forskjeller i de akseptable målingsverdiene.</span><span class="sxs-lookup"><span data-stu-id="d7116-367">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="d7116-368">Hvis du vil fremtvinge retningslinjene for kvalitet, tilordner firmaet en testgruppe til hver regel for automatisk generering av kvalitetsordrer på siden <strong>Kvalitetstilknytninger</strong>, og tilordner også en testgruppe til kvalitetsordrer som opprettes manuelt.</span><span class="sxs-lookup"><span data-stu-id="d7116-368">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7116-369">Varekvalitetsgrupper</span><span class="sxs-lookup"><span data-stu-id="d7116-369">Item quality groups</span></span></td>
<td><span data-ttu-id="d7116-370">Bruk denne siden til å definere, redigere og vise varene som er tilordnet til en kvalitetsgruppe, eller kvalitetsgruppene som er tilordnet til en vare.</span><span class="sxs-lookup"><span data-stu-id="d7116-370">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="d7116-371">En kvalitetsgruppe representerer felles testkrav for varer.</span><span class="sxs-lookup"><span data-stu-id="d7116-371">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="d7116-372">Når du har definert testkravene på siden <strong>Testgrupper</strong>, kan du definere reglene for automatisk generering av kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="d7116-372">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="d7116-373">For å forenkle prosessen kan du ikke definerer reglene for individuelle varer.</span><span class="sxs-lookup"><span data-stu-id="d7116-373">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="d7116-374">I stedet definere du regler for en kvalitetsgruppe ved hjelp av siden <strong>Kvalitetstilknytninger</strong>.</span><span class="sxs-lookup"><span data-stu-id="d7116-374">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="d7116-375">Du kan også bruke siden <strong>Varekvalitetsgrupper</strong> for en valgt kvalitetsgruppe for å tilordne relevante varer til denne gruppen.</span><span class="sxs-lookup"><span data-stu-id="d7116-375">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="d7116-376">Du kan også bruke siden <strong>Varekvalitetsgrupper</strong> for en valgt vare for å tilordne relevante kvalitetsgrupper til varen.</span><span class="sxs-lookup"><span data-stu-id="d7116-376">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="d7116-377">Et produksjonsfirma kjøper inn ulike råmaterialer som har samme testkrav for innkommende inspeksjon.</span><span class="sxs-lookup"><span data-stu-id="d7116-377">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="d7116-378">Firmaet definerer en kvalitetsgruppe og tilordner deretter varenumrene som er tilknyttet råvarene til denne gruppen.</span><span class="sxs-lookup"><span data-stu-id="d7116-378">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="d7116-379">Senere kjøper selskapet en ny type råvarer som har samme testkrav.</span><span class="sxs-lookup"><span data-stu-id="d7116-379">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="d7116-380">I stedet for å opprette nye testkrav for det nye materialet, legger firmaet til varenummeret for det nye materialet i den eksisterende kvalitetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="d7116-380">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="d7116-381">Det samme produksjonsfirmaet produserer også varer med samme krav til produksjonstesting, og leverer varer med samme krav til utføring av tester før forsendelse.</span><span class="sxs-lookup"><span data-stu-id="d7116-381">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="d7116-382">Firmaet definerer to ekstra kvalitetsgrupper, og tilordner deretter de aktuelle varenumrene til hver gruppe.</span><span class="sxs-lookup"><span data-stu-id="d7116-382">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7116-383">Testvariabler</span><span class="sxs-lookup"><span data-stu-id="d7116-383">Test variables</span></span></td>
<td><span data-ttu-id="d7116-384">Bruk denne siden til å definere og vise variablene som er tilknyttet en kvalitativ test.</span><span class="sxs-lookup"><span data-stu-id="d7116-384">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="d7116-385">For hver variabel kan du definere opplistede resultater som representerer de mulige alternativene.</span><span class="sxs-lookup"><span data-stu-id="d7116-385">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="d7116-386">Du definerer testene på siden <strong>Tester</strong>.</span><span class="sxs-lookup"><span data-stu-id="d7116-386">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="d7116-387">Du må sette testtypen for kvalitative tester til <strong>Alternativ</strong>.</span><span class="sxs-lookup"><span data-stu-id="d7116-387">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="d7116-388">Bruk siden <strong>Testgrupper</strong> til å tilordne en testvariabel til en enkelt test.</span><span class="sxs-lookup"><span data-stu-id="d7116-388">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="d7116-389">En produksjonsfirma som produserer kjeks, bruker en inspeksjonstest til det ferdige produktet.</span><span class="sxs-lookup"><span data-stu-id="d7116-389">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="d7116-390">Denne inspeksjonstesten har flere variabler.</span><span class="sxs-lookup"><span data-stu-id="d7116-390">This inspection test has several variables.</span></span> <span data-ttu-id="d7116-391">Én variabel er smak, og de mulige resultatene for denne variabelen er god og dårlig.</span><span class="sxs-lookup"><span data-stu-id="d7116-391">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="d7116-392">En annen variabel er farge, og de mulige resultatene er for mørk, for lys og riktig.</span><span class="sxs-lookup"><span data-stu-id="d7116-392">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7116-393">Testvariabelresultater</span><span class="sxs-lookup"><span data-stu-id="d7116-393">Test variable outcomes</span></span></td>
<td><span data-ttu-id="d7116-394">Bruk denne siden til å definere, redigere og vise de mulige testresultatene for en testvariabel som er knyttet til en kvalitetstest.</span><span class="sxs-lookup"><span data-stu-id="d7116-394">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="d7116-395">For hvert resultat tilordner du statusen <strong>bestått</strong> eller <strong>mislykket</strong>.</span><span class="sxs-lookup"><span data-stu-id="d7116-395">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="d7116-396">Du må definere en variabel og resultatene for hver kvalitative test som defineres på siden <strong>Tester</strong>.</span><span class="sxs-lookup"><span data-stu-id="d7116-396">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="d7116-397">(For kvalitative tester er testtypen satt til <strong>Alternativ</strong> på <strong>Tester</strong>-siden.) Bruk <strong>Testgrupper</strong>-siden til å tilordne en testvariabel og standardresultatet til en enkelt kvalitetstest.</span><span class="sxs-lookup"><span data-stu-id="d7116-397">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="d7116-398">En produksjonsfirma som produserer kjeks, bruker en inspeksjonstest til det ferdige produktet.</span><span class="sxs-lookup"><span data-stu-id="d7116-398">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="d7116-399">Denne inspeksjonstesten har flere variabler.</span><span class="sxs-lookup"><span data-stu-id="d7116-399">This inspection test has of several variables.</span></span> <span data-ttu-id="d7116-400">Én variabel er smak, og de mulige resultatene for denne variabelen er god og dårlig.</span><span class="sxs-lookup"><span data-stu-id="d7116-400">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="d7116-401">En annen variabel er farge, og de mulige resultatene er for mørk, for lys og riktig.</span><span class="sxs-lookup"><span data-stu-id="d7116-401">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="d7116-402">Statusen <strong>bestått</strong> eller <strong>mislykket</strong> tilordnes hvert resultat.</span><span class="sxs-lookup"><span data-stu-id="d7116-402">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="d7116-403">Under inspeksjonstesten for hver variabel rapporterer inspektøren testresultatet ved å velge ett av resultatene.</span><span class="sxs-lookup"><span data-stu-id="d7116-403">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="d7116-404">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d7116-404">Additional resources</span></span>
--------

[<span data-ttu-id="d7116-405">Kvalitetsstyringsprosesser</span><span class="sxs-lookup"><span data-stu-id="d7116-405">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="d7116-406">Avviksstyring</span><span class="sxs-lookup"><span data-stu-id="d7116-406">Nonconformance management</span></span>](enable-nonconformance-management.md)
