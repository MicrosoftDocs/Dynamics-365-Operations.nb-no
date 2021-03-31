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
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65858838b0fbb245a9330fab4e3b65b36a9eb944
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219371"
---
# <a name="quality-management-overview"></a><span data-ttu-id="2b525-103">Oversikt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="2b525-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b525-104">Dette emnet beskriver hvordan du kan bruke kvalitetsstyring i Dynamics 365 Supply Chain Management for å forbedre produktkvalitet i forsyningskjeden.</span><span class="sxs-lookup"><span data-stu-id="2b525-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="2b525-105">Kvalitetsstyring kan hjelpe deg med å administrere behandlingstiden når du håndterer produkter med avvik, uavhengig av opprinnelsesstedet.</span><span class="sxs-lookup"><span data-stu-id="2b525-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="2b525-106">Fordi diagnosetyper er knyttet til rettelsesrapportering, kan Supply Chain Management planlegge oppgaver for å rette opp problemer og hindre at de skjer igjen.</span><span class="sxs-lookup"><span data-stu-id="2b525-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="2b525-107">I tillegg til funksjonalitet for håndtering av avvik inneholder kvalitetsstyring funksjonalitet for å spore problemer etter problemtype (selv interne problemer) og identifisere løsninger som kortsiktige eller langsiktige.</span><span class="sxs-lookup"><span data-stu-id="2b525-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="2b525-108">Statistikk om nøkkelytelsesindikator (KPI-er) gir innsikt i loggen for tidligere avviksproblemer og løsninger som ble brukt til å rette feilene.</span><span class="sxs-lookup"><span data-stu-id="2b525-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="2b525-109">Du kan bruke historiske data for å undersøke effektiviteten til tidligere kvalitetsmål og bestemme nødvendige tiltak som skal brukes i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="2b525-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="2b525-110">Når du definerer en kvalitetstilknytning, kan Supply Chain Management generere kvalitetsordrer for diverse forretningsprosesser, hendelser og betingelser.</span><span class="sxs-lookup"><span data-stu-id="2b525-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="2b525-111">Kvalitetstilknytningen kan dekke en bestemt vare, en bestemt varegruppe eller alle varer.</span><span class="sxs-lookup"><span data-stu-id="2b525-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="2b525-112">Eksempler på bruk av kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="2b525-112">Examples of the use of quality management</span></span>
<span data-ttu-id="2b525-113">Kvalitetsstyring er fleksibelt og kan implementeres på forskjellige måter for å oppfylle kravene til bestemte typer forsyningskjedeoperasjoner.</span><span class="sxs-lookup"><span data-stu-id="2b525-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="2b525-114">Følgende eksempel viser mulig bruk av disse funksjonene.</span><span class="sxs-lookup"><span data-stu-id="2b525-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="2b525-115">Start en prosess for kvalitetskontroll automatisk basert på forhåndsdefinerte kriterier (ved lagerregistrering av en bestilling fra en bestemt leverandør).</span><span class="sxs-lookup"><span data-stu-id="2b525-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="2b525-116">Blokker lageret under inspeksjon for å hindre bruk av ikke-godkjent lager (full blokkering av bestillingsantall).</span><span class="sxs-lookup"><span data-stu-id="2b525-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="2b525-117">Bruk vareprøver som en del av en kvalitetstilknytning for å definere hvor mye av det fysiske lageret som må kontrolleres.</span><span class="sxs-lookup"><span data-stu-id="2b525-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="2b525-118">Prøver kan være basert på faste antall, en prosentdel, eller et fullstendig nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="2b525-118">Sampling can be based on fixed quantities, a percentage, or full license plate.</span></span>

> [!NOTE]
> <span data-ttu-id="2b525-119">Funksjonen _Kvalitetsstyring for lagerprosesser_ utvider funksjonaliteten til kvalitetsstyring.</span><span class="sxs-lookup"><span data-stu-id="2b525-119">The _Quality management for warehouse processes_ feature extends the capabilities of quality management.</span></span> <span data-ttu-id="2b525-120">Hvis du bruker denne funksjonen, kan du se [Kvalitetsstyring for lagerprosesser](quality-management-for-warehouses-processes.md) for eksempler på hvordan kvalitetsstyring fungerer når den aktiveres.</span><span class="sxs-lookup"><span data-stu-id="2b525-120">If you are using this feature, then see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md) for examples of how quality management works when it's enabled.</span></span>

-   <span data-ttu-id="2b525-121">Opprette kvalitetsordrer for delvise mottak.</span><span class="sxs-lookup"><span data-stu-id="2b525-121">Create quality orders for partial receipts.</span></span> <span data-ttu-id="2b525-122">Hvis du vil opprette en kvalitetsordre som er basert på antallet som er fysisk mottatt med en ordre, må du velge den **Per oppdatert mengde** for den **Vareprøve** skjema.</span><span class="sxs-lookup"><span data-stu-id="2b525-122">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="2b525-123">Opprett testtyper med minimums-, maksimums-, og måltestverdier, og utfør kvalitative kontra kvantitative tester som har forhåndsdefinerte valideringsresultater.</span><span class="sxs-lookup"><span data-stu-id="2b525-123">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="2b525-124">Angi et akseptabelt kvalitetsnivå for å kontrollere kvalitetsmåltoleranser.</span><span class="sxs-lookup"><span data-stu-id="2b525-124">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="2b525-125">Angi ressursene som en inspeksjonsoperasjon krever, for eksempel et testområde og testinstrumenter.</span><span class="sxs-lookup"><span data-stu-id="2b525-125">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="2b525-126">Arbeide med kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="2b525-126">Working with quality associations</span></span>
<span data-ttu-id="2b525-127">Forretningsprosessen som bruker en kvalitetstilknytning, kan knyttes til ulike kildedokumenter, for eksempel bestillinger, salgsordrer eller produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="2b525-127">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="2b525-128">Hver kvalitetstilknytningspost definerer settet med tester, det akseptable kvalitetsnivået og samplingplanen som gjelder for kvalitetsordrene som genereres.</span><span class="sxs-lookup"><span data-stu-id="2b525-128">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="2b525-129">Du må definere en kvalitetstilknytningspost for hver variasjon i en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="2b525-129">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="2b525-130">Du kan for eksempel definere en kvalitetstilknytning som genererer en kvalitetsordre når et produkt for bestillingsmottak oppdateres.</span><span class="sxs-lookup"><span data-stu-id="2b525-130">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="2b525-131">Avhengig av oppsettet for utførelsesplanen kan selve utløsingsprosessen blokkeres når det finnes en åpen kvalitetsordre, eller de neste prosessene, for eksempel bestillingsfakturering, kan blokkeres.</span><span class="sxs-lookup"><span data-stu-id="2b525-131">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="2b525-132">**Merk:** Når det finnes åpne kvalitetsordrer, blokkeres lagerantall automatisk fra å bli utstedt.</span><span class="sxs-lookup"><span data-stu-id="2b525-132">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="2b525-133">Avhengig av **Full blokkering**-innstillingen på siden **Vareprøver** er antallet enten antallet på kvalitetsordren eller antallet på kildedokumentlinjen.</span><span class="sxs-lookup"><span data-stu-id="2b525-133">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="2b525-134">For en gitt forretningsprosess identifiserer kvalitetstilknytningspost hendelsen og betingelsene som en kvalitetsordre genereres for.</span><span class="sxs-lookup"><span data-stu-id="2b525-134">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="2b525-135">Betingelsene kan være spesifikke for et område eller en juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="2b525-135">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="2b525-136">En kvalitetsordre som omfatter destruktive tester, kan bare genereres når hvis det finnes lagerbeholdning for hendelsen.</span><span class="sxs-lookup"><span data-stu-id="2b525-136">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="2b525-137">De følgende eksemplene illustrerer hvordan en kvalitetstilknytningspost er definert for variasjonene innen ulike forretningsprosesser.</span><span class="sxs-lookup"><span data-stu-id="2b525-137">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="2b525-138">For hvert eksempel oppsummere følgende tabell hendelsene og betingelsene som er definert av en kvalitetstilknytningspost.</span><span class="sxs-lookup"><span data-stu-id="2b525-138">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="2b525-139">Referansetype</span><span class="sxs-lookup"><span data-stu-id="2b525-139">Reference type</span></span></th>
<th><span data-ttu-id="2b525-140">Hendelsestype</span><span class="sxs-lookup"><span data-stu-id="2b525-140">Event type</span></span></th>
<th><span data-ttu-id="2b525-141">Utførelse</span><span class="sxs-lookup"><span data-stu-id="2b525-141">Execution</span></span></th>
<th><span data-ttu-id="2b525-142">Hendelsesblokkering</span><span class="sxs-lookup"><span data-stu-id="2b525-142">Event blocking</span></span></th>
<th><span data-ttu-id="2b525-143">Dokumentreferanse</span><span class="sxs-lookup"><span data-stu-id="2b525-143">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="2b525-144">Beholdning</span><span class="sxs-lookup"><span data-stu-id="2b525-144">Inventory</span></span></td>
<td><span data-ttu-id="2b525-145">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="2b525-145">Not applicable</span></span></td>
<td><span data-ttu-id="2b525-146">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="2b525-146">Not applicable</span></span></td>
<td><span data-ttu-id="2b525-147">Ingen</span><span class="sxs-lookup"><span data-stu-id="2b525-147">None</span></span></td>
<td><span data-ttu-id="2b525-148">Alle</span><span class="sxs-lookup"><span data-stu-id="2b525-148">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="2b525-149">Salg</span><span class="sxs-lookup"><span data-stu-id="2b525-149">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="2b525-150">Plukkingsprosess er planlagt</span><span class="sxs-lookup"><span data-stu-id="2b525-150">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="2b525-151">Før</span><span class="sxs-lookup"><span data-stu-id="2b525-151">Before</span></span></td>
<td><span data-ttu-id="2b525-152">Ingen</span><span class="sxs-lookup"><span data-stu-id="2b525-152">None</span></span></td>
<td rowspan="22"><span data-ttu-id="2b525-153">Bare Spesifikk ID, Gruppe eller Alle</span><span class="sxs-lookup"><span data-stu-id="2b525-153">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-154">Plukkingsprosess</span><span class="sxs-lookup"><span data-stu-id="2b525-154">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-155">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="2b525-155">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-156">Faktura</span><span class="sxs-lookup"><span data-stu-id="2b525-156">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2b525-157">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="2b525-157">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="2b525-158">Før</span><span class="sxs-lookup"><span data-stu-id="2b525-158">Before</span></span></td>
<td><span data-ttu-id="2b525-159">Ingen</span><span class="sxs-lookup"><span data-stu-id="2b525-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-160">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="2b525-160">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-161">Faktura</span><span class="sxs-lookup"><span data-stu-id="2b525-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="2b525-162">Kjøp</span><span class="sxs-lookup"><span data-stu-id="2b525-162">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="2b525-163">Kvitteringsliste</span><span class="sxs-lookup"><span data-stu-id="2b525-163">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="2b525-164">Før</span><span class="sxs-lookup"><span data-stu-id="2b525-164">Before</span></span></td>
<td><span data-ttu-id="2b525-165">Ingen</span><span class="sxs-lookup"><span data-stu-id="2b525-165">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-166">Kvitteringsliste</span><span class="sxs-lookup"><span data-stu-id="2b525-166">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-167">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="2b525-167">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-168">Faktura</span><span class="sxs-lookup"><span data-stu-id="2b525-168">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2b525-169">Etter</span><span class="sxs-lookup"><span data-stu-id="2b525-169">After</span></span></td>
<td><span data-ttu-id="2b525-170">Ingen</span><span class="sxs-lookup"><span data-stu-id="2b525-170">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-171">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="2b525-171">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-172">Faktura</span><span class="sxs-lookup"><span data-stu-id="2b525-172">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2b525-173">Registrering</span><span class="sxs-lookup"><span data-stu-id="2b525-173">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="2b525-174">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="2b525-174">Not applicable</span></span></td>
<td><span data-ttu-id="2b525-175">Ingen</span><span class="sxs-lookup"><span data-stu-id="2b525-175">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-176">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="2b525-176">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-177">Faktura</span><span class="sxs-lookup"><span data-stu-id="2b525-177">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="2b525-178">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="2b525-178">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="2b525-179">Før</span><span class="sxs-lookup"><span data-stu-id="2b525-179">Before</span></span></td>
<td><span data-ttu-id="2b525-180">Ingen</span><span class="sxs-lookup"><span data-stu-id="2b525-180">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-181">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="2b525-181">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-182">Faktura</span><span class="sxs-lookup"><span data-stu-id="2b525-182">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="2b525-183">Etter</span><span class="sxs-lookup"><span data-stu-id="2b525-183">After</span></span></td>
<td><span data-ttu-id="2b525-184">Ingen</span><span class="sxs-lookup"><span data-stu-id="2b525-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-185">Faktura</span><span class="sxs-lookup"><span data-stu-id="2b525-185">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="2b525-186">Produksjon</span><span class="sxs-lookup"><span data-stu-id="2b525-186">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="2b525-187">Registrering</span><span class="sxs-lookup"><span data-stu-id="2b525-187">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="2b525-188">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="2b525-188">Not applicable</span></span></td>
<td><span data-ttu-id="2b525-189">Ingen</span><span class="sxs-lookup"><span data-stu-id="2b525-189">None</span></span></td>
<td rowspan="12"><span data-ttu-id="2b525-190">Alle</span><span class="sxs-lookup"><span data-stu-id="2b525-190">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-191">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="2b525-191">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-192">Slutt</span><span class="sxs-lookup"><span data-stu-id="2b525-192">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="2b525-193">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="2b525-193">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="2b525-194">Før</span><span class="sxs-lookup"><span data-stu-id="2b525-194">Before</span></span></td>
<td><span data-ttu-id="2b525-195">Ingen</span><span class="sxs-lookup"><span data-stu-id="2b525-195">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-196">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="2b525-196">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-197">Slutt</span><span class="sxs-lookup"><span data-stu-id="2b525-197">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="2b525-198">Etter</span><span class="sxs-lookup"><span data-stu-id="2b525-198">After</span></span></td>
<td><span data-ttu-id="2b525-199">Ingen</span><span class="sxs-lookup"><span data-stu-id="2b525-199">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-200">Slutt</span><span class="sxs-lookup"><span data-stu-id="2b525-200">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="2b525-201">Karantene</span><span class="sxs-lookup"><span data-stu-id="2b525-201">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="2b525-202">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="2b525-202">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="2b525-203">Før</span><span class="sxs-lookup"><span data-stu-id="2b525-203">Before</span></span></td>
<td><span data-ttu-id="2b525-204">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="2b525-204">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-205">Slutt</span><span class="sxs-lookup"><span data-stu-id="2b525-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-206">Etter</span><span class="sxs-lookup"><span data-stu-id="2b525-206">After</span></span></td>
<td><span data-ttu-id="2b525-207">Slutt</span><span class="sxs-lookup"><span data-stu-id="2b525-207">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-208">Slutt</span><span class="sxs-lookup"><span data-stu-id="2b525-208">End</span></span></td>
<td><span data-ttu-id="2b525-209">Før</span><span class="sxs-lookup"><span data-stu-id="2b525-209">Before</span></span></td>
<td><span data-ttu-id="2b525-210">Slutt</span><span class="sxs-lookup"><span data-stu-id="2b525-210">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2b525-211">Ruteoperasjon</span><span class="sxs-lookup"><span data-stu-id="2b525-211">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="2b525-212">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="2b525-212">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="2b525-213">Før</span><span class="sxs-lookup"><span data-stu-id="2b525-213">Before</span></span></td>
<td><span data-ttu-id="2b525-214">Ingen</span><span class="sxs-lookup"><span data-stu-id="2b525-214">None</span></span></td>
<td rowspan="3"><span data-ttu-id="2b525-215">Bestemt ID, Gruppe eller Alle, og Ressursspesifikk, Gruppe eller Alle</span><span class="sxs-lookup"><span data-stu-id="2b525-215">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-216">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="2b525-216">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-217">Etter</span><span class="sxs-lookup"><span data-stu-id="2b525-217">After</span></span></td>
<td><span data-ttu-id="2b525-218">Ingen</span><span class="sxs-lookup"><span data-stu-id="2b525-218">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2b525-219">Koproduktproduksjon</span><span class="sxs-lookup"><span data-stu-id="2b525-219">Co-product production</span></span></td>
<td><span data-ttu-id="2b525-220">Registrering</span><span class="sxs-lookup"><span data-stu-id="2b525-220">Registration</span></span></td>
<td><span data-ttu-id="2b525-221">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="2b525-221">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2b525-222">Ingen</span><span class="sxs-lookup"><span data-stu-id="2b525-222">None</span></span></td>
<td rowspan="3"><span data-ttu-id="2b525-223">Alle</span><span class="sxs-lookup"><span data-stu-id="2b525-223">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="2b525-224">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="2b525-224">Report as finished</span></span></td>
<td><span data-ttu-id="2b525-225">Før</span><span class="sxs-lookup"><span data-stu-id="2b525-225">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-226">Etter</span><span class="sxs-lookup"><span data-stu-id="2b525-226">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2b525-227">Tabellen nedenfor inneholder mer informasjon om hvordan kvalitetsordrer kan genereres for bestemte typer prosesser.</span><span class="sxs-lookup"><span data-stu-id="2b525-227">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="2b525-228">Type av prosess</span><span class="sxs-lookup"><span data-stu-id="2b525-228">Type of process</span></span></th>
<th><span data-ttu-id="2b525-229">Når kvalitetsordrer kan genereres automatisk</span><span class="sxs-lookup"><span data-stu-id="2b525-229">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="2b525-230">Når kvalitetsordrer kan genereres hvis destruktiv testing kreves</span><span class="sxs-lookup"><span data-stu-id="2b525-230">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="2b525-231">Betingelsesinformasjon</span><span class="sxs-lookup"><span data-stu-id="2b525-231">Condition information</span></span></th>
<th><span data-ttu-id="2b525-232">Informasjon om manuell generering</span><span class="sxs-lookup"><span data-stu-id="2b525-232">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="2b525-233">Bestilling</span><span class="sxs-lookup"><span data-stu-id="2b525-233">Purchase order</span></span></td>
<td><span data-ttu-id="2b525-234">Før eller etter en kvitteringsliste eller produktkvittering for materialet som mottas, posteres</span><span class="sxs-lookup"><span data-stu-id="2b525-234">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="2b525-235">Etter produktkvitteringen for materialet som mottas, er postert, fordi materialet må være tilgjengelig for destruktiv testing</span><span class="sxs-lookup"><span data-stu-id="2b525-235">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="2b525-236">Behovet for en kvalitetsordre kan reflektere et bestemt område, en vare, en leverandør eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="2b525-236">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="2b525-237">En manuelt generert kvalitetsordre som viser til en bestilling, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="2b525-237">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-238">Karanteneordre</span><span class="sxs-lookup"><span data-stu-id="2b525-238">Quarantine order</span></span></td>
<td><span data-ttu-id="2b525-239">Før eller etter karanteordren er rapportert som fullført eller avsluttet</span><span class="sxs-lookup"><span data-stu-id="2b525-239">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="2b525-240">Kvalitetsordrer som krever destruktive tester, kan ikke genereres.</span><span class="sxs-lookup"><span data-stu-id="2b525-240">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="2b525-241">Det forutsettes at karanteneordrefunksjonaliteten behandler disposisjonen av materialet som blir ødelagt.</span><span class="sxs-lookup"><span data-stu-id="2b525-241">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="2b525-242">Behovet for en kvalitetsordre kan reflektere et bestemt område, en vare, en leverandør eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="2b525-242">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="2b525-243">En manuelt generert kvalitetsordre som viser til en karanteneordre, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="2b525-243">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-244">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="2b525-244">Sales order</span></span></td>
<td><span data-ttu-id="2b525-245">Før en planlagt plukkeprosessen eller følgeseddeloppdatering for varene som leveres</span><span class="sxs-lookup"><span data-stu-id="2b525-245">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="2b525-246">I alle trinn</span><span class="sxs-lookup"><span data-stu-id="2b525-246">At any step</span></span></td>
<td><span data-ttu-id="2b525-247">Kravet til en kvalitetsordre kan reflektere et bestemt område, en vare, en kunde eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="2b525-247">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="2b525-248">En manuelt generert kvalitetsordre som viser til en salgsordre, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="2b525-248">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-249">Produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="2b525-249">Production order</span></span></td>
<td><span data-ttu-id="2b525-250">Før eller etter den ferdige kvaliteten for produksjonsordren er rapportert</span><span class="sxs-lookup"><span data-stu-id="2b525-250">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="2b525-251">Etter den ferdige kvaliteten for produksjonsordren er rapportert</span><span class="sxs-lookup"><span data-stu-id="2b525-251">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="2b525-252">Behovet for en kvalitetsordre kan reflektere et bestemt område eller en vare, eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="2b525-252">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="2b525-253">En manuelt generert kvalitetsordre som viser til en produksjonsordre, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="2b525-253">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-254">Produksjonsordre som har en ruteoperasjon</span><span class="sxs-lookup"><span data-stu-id="2b525-254">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="2b525-255">Før eller etter at rapporten for en operasjon er fullført</span><span class="sxs-lookup"><span data-stu-id="2b525-255">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="2b525-256">Etter at rapporteringen av produksjonen er fullført for den siste operasjonen</span><span class="sxs-lookup"><span data-stu-id="2b525-256">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="2b525-257">Behovet for en kvalitetsordre kan reflektere et bestemt område, en vare eller en operasjonsressurs eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="2b525-257">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="2b525-258">En manuelt generert kvalitetsordre som viser til en ruteoperasjon, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="2b525-258">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2b525-259">Beholdning</span><span class="sxs-lookup"><span data-stu-id="2b525-259">Inventory</span></span></td>
<td><span data-ttu-id="2b525-260">En kvalitetsordre kan ikke genereres automatisk for en transaksjon innen en lagerjournal eller for overføringsordretransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="2b525-260">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="2b525-261">En kvalitetsordre må opprettes manuelt for en vares lagerantall.</span><span class="sxs-lookup"><span data-stu-id="2b525-261">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="2b525-262">Varens fysiske lagerbeholdning kreves.</span><span class="sxs-lookup"><span data-stu-id="2b525-262">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="2b525-263">Eksempler på automatisk generering av kvalitetsordre</span><span class="sxs-lookup"><span data-stu-id="2b525-263">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="2b525-264">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="2b525-264">Purchasing</span></span>

<span data-ttu-id="2b525-265">I innkjøp, hvis du du angir feltet **Hendelsestype** til **Produktkvittering** og feltet **Utførelse** til **Etter** på siden **Kvalitetstilknytninger**, får du følgende resultater:</span><span class="sxs-lookup"><span data-stu-id="2b525-265">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="2b525-266">Hvis alternativet **Per oppdatert mengde** er satt til **Ja**, genereres det en kvalitetsordre for hvert mottak mot bestillingen basert på det mottatte antallet og innstillingene i vareprøven.</span><span class="sxs-lookup"><span data-stu-id="2b525-266">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="2b525-267">Hver gang et antall mottas mot bestillingen, genereres nye kvalitetsordrer basert på det nylig mottatte antallet.</span><span class="sxs-lookup"><span data-stu-id="2b525-267">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="2b525-268">Hvis alternativet **Per oppdatert mengde** er satt til **Nei**, genereres det en kvalitetsordre for det første mottaket mot bestillingen basert på det mottatte antallet.</span><span class="sxs-lookup"><span data-stu-id="2b525-268">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="2b525-269">I tillegg blir én eller flere kvalitetsordrer opprettet på grunnlag av restantallet, avhengig av sporingsdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="2b525-269">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="2b525-270">Kvalitetsordrer genereres ikke for etterfølgende mottak mot bestillingen.</span><span class="sxs-lookup"><span data-stu-id="2b525-270">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="2b525-271">Produksjon</span><span class="sxs-lookup"><span data-stu-id="2b525-271">Production</span></span>

<span data-ttu-id="2b525-272">I produksjon, hvis du du angir feltet **Hendelsestype** til **Ferdigmeld** og feltet **Utførelse** til **Etter** på siden **Kvalitetstilknytninger**, får du følgende resultater:</span><span class="sxs-lookup"><span data-stu-id="2b525-272">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="2b525-273">Hvis alternativet **Per oppdatert mengde** er satt til **Ja**, genereres det en kvalitetsordre for hver fullførte antall og innstillingene i vareprøven.</span><span class="sxs-lookup"><span data-stu-id="2b525-273">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="2b525-274">Hver gang et antall rapporteres som fullført mot produksjonsordren, genereres nye kvalitetsordrer basert på det nylig fullførte antallet.</span><span class="sxs-lookup"><span data-stu-id="2b525-274">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="2b525-275">Denne genereringslogikken er konsekvent med innkjøp.</span><span class="sxs-lookup"><span data-stu-id="2b525-275">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="2b525-276">Hvis alternativet **Per oppdatert mengde** er satt til **Nei**, genereres det en kvalitetsordre første gang antallet rapporteres som fullført, basert på det fullførte antallet.</span><span class="sxs-lookup"><span data-stu-id="2b525-276">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="2b525-277">I tillegg blir én eller flere kvalitetsordrer opprettet på grunnlag av restantallet, avhengig av sporingsdimensjonene for vareprøven.</span><span class="sxs-lookup"><span data-stu-id="2b525-277">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="2b525-278">Kvalitetsordrer genereres ikke for etterfølgende ferdigmeldte antall.</span><span class="sxs-lookup"><span data-stu-id="2b525-278">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="2b525-279">Kvalitetsspesifikasjon</span><span class="sxs-lookup"><span data-stu-id="2b525-279">Quality specification</span></span></th>
<th><span data-ttu-id="2b525-280">Per oppdatert mengde</span><span class="sxs-lookup"><span data-stu-id="2b525-280">Per updated quantity</span></span></th>
<th><span data-ttu-id="2b525-281">Per sporingsdimensjon</span><span class="sxs-lookup"><span data-stu-id="2b525-281">Per tracking dimension</span></span></th>
<th><span data-ttu-id="2b525-282">Resultat</span><span class="sxs-lookup"><span data-stu-id="2b525-282">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="2b525-283">Prosent: 10 %</span><span class="sxs-lookup"><span data-stu-id="2b525-283">Percentage: 10%</span></span></td>
<td><span data-ttu-id="2b525-284">Ja</span><span class="sxs-lookup"><span data-stu-id="2b525-284">Yes</span></span></td>
<td>
<p><span data-ttu-id="2b525-285">Partinummer: Nei</span><span class="sxs-lookup"><span data-stu-id="2b525-285">Batch number: No</span></span></p>
<p><span data-ttu-id="2b525-286">Serienummer: Nei</span><span class="sxs-lookup"><span data-stu-id="2b525-286">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="2b525-287">Ordreantall: 100</span><span class="sxs-lookup"><span data-stu-id="2b525-287">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="2b525-288">Rapporter som ferdig for 30</span><span class="sxs-lookup"><span data-stu-id="2b525-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="2b525-289">Kvalitetsordre #1 for 3 (10 % av 30)</span><span class="sxs-lookup"><span data-stu-id="2b525-289">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="2b525-290">Rapporter som ferdig for 70</span><span class="sxs-lookup"><span data-stu-id="2b525-290">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="2b525-291">Kvalitetsordre #2 for 7 (10 % av restordreantallet, som er lik 70 i dette tilfellet)</span><span class="sxs-lookup"><span data-stu-id="2b525-291">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="2b525-292">Fast antall: 1</span><span class="sxs-lookup"><span data-stu-id="2b525-292">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="2b525-293">Nei</span><span class="sxs-lookup"><span data-stu-id="2b525-293">No</span></span></td>
<td>
<p><span data-ttu-id="2b525-294">Partinummer: Nei</span><span class="sxs-lookup"><span data-stu-id="2b525-294">Batch number: No</span></span></p>
<p><span data-ttu-id="2b525-295">Serienummer: Nei</span><span class="sxs-lookup"><span data-stu-id="2b525-295">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="2b525-296">Ordreantall: 100</span><span class="sxs-lookup"><span data-stu-id="2b525-296">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="2b525-297">Rapporter som ferdig for 30</span><span class="sxs-lookup"><span data-stu-id="2b525-297">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="2b525-298">Kvalitetsordre #1 for 1 (for det første ferdigmeldte antallet, som har en fast verdi på 1)</span><span class="sxs-lookup"><span data-stu-id="2b525-298">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="2b525-299">Kvalitetsordre #2 for 1 (for det resterende antallet, som fremdeles har en fast verdi på 1)</span><span class="sxs-lookup"><span data-stu-id="2b525-299">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="2b525-300">Rapporter som ferdig for 10</span><span class="sxs-lookup"><span data-stu-id="2b525-300">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="2b525-301">Ingen kvalitetsordrer er opprettet.</span><span class="sxs-lookup"><span data-stu-id="2b525-301">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="2b525-302">Rapporter som ferdig for 60</span><span class="sxs-lookup"><span data-stu-id="2b525-302">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="2b525-303">Ingen kvalitetsordrer er opprettet.</span><span class="sxs-lookup"><span data-stu-id="2b525-303">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="2b525-304">Fast antall: 1</span><span class="sxs-lookup"><span data-stu-id="2b525-304">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="2b525-305">Ja</span><span class="sxs-lookup"><span data-stu-id="2b525-305">Yes</span></span></td>
<td>
<p><span data-ttu-id="2b525-306">Partinummer: Ja</span><span class="sxs-lookup"><span data-stu-id="2b525-306">Batch number: Yes</span></span></p>
<p><span data-ttu-id="2b525-307">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="2b525-307">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="2b525-308">Ordreantall: 10</span><span class="sxs-lookup"><span data-stu-id="2b525-308">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="2b525-309">Rapporter som ferdig for 3: 1 for #b1, #s1; 1 for #b2, #s2; og 1 for #b3, #s3</span><span class="sxs-lookup"><span data-stu-id="2b525-309">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="2b525-310">Kvalitetsordre #1 for 1 av parti #b1, serie #s1</span><span class="sxs-lookup"><span data-stu-id="2b525-310">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="2b525-311">Kvalitetsordre #2 for 1 av parti #b2, serie #s2</span><span class="sxs-lookup"><span data-stu-id="2b525-311">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="2b525-312">Kvalitetsordre #3 for 1 av parti #b3, serie #s3</span><span class="sxs-lookup"><span data-stu-id="2b525-312">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="2b525-313">Rapporter som ferdig for 2: 1 for #b4, #s4; og 1 for #b5, #s5</span><span class="sxs-lookup"><span data-stu-id="2b525-313">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="2b525-314">Kvalitetsordre #4 for 1 av parti #b4, serie #s4</span><span class="sxs-lookup"><span data-stu-id="2b525-314">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="2b525-315">Kvalitetsordre #5 for 1 av parti #b5, serie #s5</span><span class="sxs-lookup"><span data-stu-id="2b525-315">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="2b525-316"><strong>Merk:</strong> Partiet kan brukes på nytt.</span><span class="sxs-lookup"><span data-stu-id="2b525-316"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="2b525-317">Fast antall: 2</span><span class="sxs-lookup"><span data-stu-id="2b525-317">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="2b525-318">Nei</span><span class="sxs-lookup"><span data-stu-id="2b525-318">No</span></span></td>
<td>
<p><span data-ttu-id="2b525-319">Partinummer: Ja</span><span class="sxs-lookup"><span data-stu-id="2b525-319">Batch number: Yes</span></span></p>
<p><span data-ttu-id="2b525-320">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="2b525-320">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="2b525-321">Ordreantall: 10</span><span class="sxs-lookup"><span data-stu-id="2b525-321">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="2b525-322">Rapporter som ferdig for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; og 1 for #b4, #s4</span><span class="sxs-lookup"><span data-stu-id="2b525-322">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="2b525-323">Kvalitetsordre #1 for 1 av parti #b1, serie #s1</span><span class="sxs-lookup"><span data-stu-id="2b525-323">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="2b525-324">Kvalitetsordre #2 for 1 av parti #b2, serie #s2</span><span class="sxs-lookup"><span data-stu-id="2b525-324">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="2b525-325">Kvalitetsordre #3 for 1 av parti #b3, serie #s3</span><span class="sxs-lookup"><span data-stu-id="2b525-325">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="2b525-326">Kvalitetsordre #4 for 1 av parti #b4, serie #s4</span><span class="sxs-lookup"><span data-stu-id="2b525-326">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="2b525-327">Kvalitetsordre #5 for 2, uten referanse til et parti og et serienummer</span><span class="sxs-lookup"><span data-stu-id="2b525-327">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="2b525-328">Rapporter som ferdig for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; og 1 for #b10, #s10</span><span class="sxs-lookup"><span data-stu-id="2b525-328">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="2b525-329">Ingen kvalitetsordrer er opprettet.</span><span class="sxs-lookup"><span data-stu-id="2b525-329">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="2b525-330">Funksjonen *Kvalitetsstyring for lagerprosesser* legger til funksjoner for kvalitetsordrebehandling for produksjon med **hendelsestype** satt til *Ferdigmeld* og **utførelse** satt til *Etter*, og for innkjøp med **hendelsestype** satt til *Registrering*.</span><span class="sxs-lookup"><span data-stu-id="2b525-330">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production with **Event type** set to *Report as finished* and **Execution** set to *After*, and for purchases with **Event type** set to *Registration*.</span></span> <span data-ttu-id="2b525-331">For mer informasjon, se [Kvalitetsstyring for lagerprosesser](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="2b525-331">For details, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

## <a name="quality-management-pages"></a><span data-ttu-id="2b525-332">Kvalitetsstyringssider</span><span class="sxs-lookup"><span data-stu-id="2b525-332">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2b525-333">Side</span><span class="sxs-lookup"><span data-stu-id="2b525-333">Page</span></span></th>
<th><span data-ttu-id="2b525-334">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="2b525-334">Description</span></span></th>
<th><span data-ttu-id="2b525-335">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b525-335">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2b525-336">Kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="2b525-336">Quality associations</span></span></td>
<td><span data-ttu-id="2b525-337">Se tidligere deler av denne artikkelen.</span><span class="sxs-lookup"><span data-stu-id="2b525-337">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="2b525-338">En kvalitetstilknytning definerer alle følgende opplysninger om en kvalitetsordre som er generert:</span><span class="sxs-lookup"><span data-stu-id="2b525-338">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="2b525-339">Transaksjonshendelsen</span><span class="sxs-lookup"><span data-stu-id="2b525-339">The transaction event</span></span></li>
<li><span data-ttu-id="2b525-340">Settet med tester som må utføres på elementene</span><span class="sxs-lookup"><span data-stu-id="2b525-340">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="2b525-341">Det akseptable kvalitetsnivået</span><span class="sxs-lookup"><span data-stu-id="2b525-341">The AQL</span></span></li>
<li><span data-ttu-id="2b525-342">Prøveplanen</span><span class="sxs-lookup"><span data-stu-id="2b525-342">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="2b525-343">Du må definere en kvalitetstilknytning for hver variasjon i en forretningsprosess som krever automatisk generering av kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="2b525-343">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="2b525-344">Eksempelvis kan en kvalitetsordre genereres i forretningsprosessen for bestillinger, karanteneordrer, salgsordrer og produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="2b525-344">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b525-345">Tester</span><span class="sxs-lookup"><span data-stu-id="2b525-345">Tests</span></span></td>
<td><span data-ttu-id="2b525-346">Bruk denne siden til å definere og vise de individuelle testene som fastslår om produktene oppfyller kvalitetsspesifikasjoner.</span><span class="sxs-lookup"><span data-stu-id="2b525-346">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="2b525-347">Du kan tilordne én eller flere individuelle tester til en testgruppe.</span><span class="sxs-lookup"><span data-stu-id="2b525-347">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="2b525-348">I dette tilfellet må også angi testspesifikk informasjon, for eksempel de akseptable målingsverdiene.</span><span class="sxs-lookup"><span data-stu-id="2b525-348">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="2b525-349">Målingsverdiene brukes for kvantitative tester, og testvariablene brukes for kvalitative tester.</span><span class="sxs-lookup"><span data-stu-id="2b525-349">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="2b525-350">En kvantitativ test har testtypen <strong>Heltall</strong> eller <strong>Brøk</strong> og har også en angitt måleenhet.</span><span class="sxs-lookup"><span data-stu-id="2b525-350">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="2b525-351">Kvalitetsspesifikasjoner og testresultater uttrykkes som tall.</span><span class="sxs-lookup"><span data-stu-id="2b525-351">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="2b525-352">En kvalitativ test har testtypen <strong>Alternativ</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b525-352">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="2b525-353">Kvalitative tester krever mer informasjon om testvariabelen som måles, og de tilhørende opplistede alternativene.</span><span class="sxs-lookup"><span data-stu-id="2b525-353">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="2b525-354">Kvalitetsspesifikasjoner og testresultater uttrykkes i henhold til et resultat.</span><span class="sxs-lookup"><span data-stu-id="2b525-354">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="2b525-355">Et produksjonsfirma utfører to tester på innkjøpt materiale: en kvantitativ test om materialkvalitet og en kvalitativ test om emballasjeskade.</span><span class="sxs-lookup"><span data-stu-id="2b525-355">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="2b525-356">Firmaet definerer tilleggsinformasjon om den kvalitative testen for å identifisere testvariabelen (skadet emballasje) og resultatene.</span><span class="sxs-lookup"><span data-stu-id="2b525-356">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="2b525-357">Firmaet bruker <strong>Testgrupper</strong>-siden til å tilordne de to testene til en testgruppe og angi testspesifikk informasjon.</span><span class="sxs-lookup"><span data-stu-id="2b525-357">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="2b525-358">Testgruppen tilordnes til en kvalitetsordre, slik at firmaet kan rapportere testresultater for de to testene.</span><span class="sxs-lookup"><span data-stu-id="2b525-358">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b525-359">Testgrupper</span><span class="sxs-lookup"><span data-stu-id="2b525-359">Test groups</span></span></td>
<td><span data-ttu-id="2b525-360">Bruk denne siden til å definere, redigere og vise testgrupper og de individuelle testene som er tilordnet til en testgruppe.</span><span class="sxs-lookup"><span data-stu-id="2b525-360">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="2b525-361">Den øvre ruten viser testgrupper, og den nedre ruten viser testene som er tilordnet til en valgt testgruppe.</span><span class="sxs-lookup"><span data-stu-id="2b525-361">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="2b525-362">Du tilordner flere policyer til en testgruppe, for eksempel en prøveplan, et akseptabelt kvalitetsnivå og kravet til destruktiv testing.</span><span class="sxs-lookup"><span data-stu-id="2b525-362">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="2b525-363">Når du tilordner en individuell test til en testgruppe, definerer du tilleggsinformasjon, for eksempel sekvensen, dokumenter og gyldighetsdatoer.</span><span class="sxs-lookup"><span data-stu-id="2b525-363">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="2b525-364">For en kvantitativ test inkluderer informasjonen du definerer, også de akseptable målingsverdiene.</span><span class="sxs-lookup"><span data-stu-id="2b525-364">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="2b525-365">For en kvalitativ test inkluderer informasjonen testvariabelen og standardresultatet.</span><span class="sxs-lookup"><span data-stu-id="2b525-365">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="2b525-366">Testgruppen som er tilordnet en kvalitetsordre, definerer standardsettet med tester som må utføres for den bestemte varen.</span><span class="sxs-lookup"><span data-stu-id="2b525-366">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="2b525-367">Du kan imidlertid legge til, slette eller endre tester i kvalitetsordren.</span><span class="sxs-lookup"><span data-stu-id="2b525-367">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="2b525-368">Testresultater rapporteres for hver test på en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="2b525-368">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="2b525-369">Et produksjonsfirma definerer en testgruppe for hver variasjon av retningslinjene for kvalitet.</span><span class="sxs-lookup"><span data-stu-id="2b525-369">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="2b525-370">De ulike testgruppene gjenspeiler forskjeller i prøveplanene, settet med tester som må utføres sammen, det akseptable kvalitetsnivået og andre faktorer.</span><span class="sxs-lookup"><span data-stu-id="2b525-370">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="2b525-371">For kvantitative tester er det også forskjeller i de akseptable målingsverdiene.</span><span class="sxs-lookup"><span data-stu-id="2b525-371">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="2b525-372">Hvis du vil fremtvinge retningslinjene for kvalitet, tilordner firmaet en testgruppe til hver regel for automatisk generering av kvalitetsordrer på siden <strong>Kvalitetstilknytninger</strong>, og tilordner også en testgruppe til kvalitetsordrer som opprettes manuelt.</span><span class="sxs-lookup"><span data-stu-id="2b525-372">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b525-373">Varekvalitetsgrupper</span><span class="sxs-lookup"><span data-stu-id="2b525-373">Item quality groups</span></span></td>
<td><span data-ttu-id="2b525-374">Bruk denne siden til å definere, redigere og vise varene som er tilordnet til en kvalitetsgruppe, eller kvalitetsgruppene som er tilordnet til en vare.</span><span class="sxs-lookup"><span data-stu-id="2b525-374">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="2b525-375">En kvalitetsgruppe representerer felles testkrav for varer.</span><span class="sxs-lookup"><span data-stu-id="2b525-375">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="2b525-376">Når du har definert testkravene på siden <strong>Testgrupper</strong>, kan du definere reglene for automatisk generering av kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="2b525-376">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="2b525-377">For å forenkle prosessen kan du ikke definerer reglene for individuelle varer.</span><span class="sxs-lookup"><span data-stu-id="2b525-377">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="2b525-378">I stedet definere du regler for en kvalitetsgruppe ved hjelp av siden <strong>Kvalitetstilknytninger</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b525-378">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="2b525-379">Du kan også bruke siden <strong>Varekvalitetsgrupper</strong> for en valgt kvalitetsgruppe for å tilordne relevante varer til denne gruppen.</span><span class="sxs-lookup"><span data-stu-id="2b525-379">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="2b525-380">Du kan også bruke siden <strong>Varekvalitetsgrupper</strong> for en valgt vare for å tilordne relevante kvalitetsgrupper til varen.</span><span class="sxs-lookup"><span data-stu-id="2b525-380">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="2b525-381">Et produksjonsfirma kjøper inn ulike råmaterialer som har samme testkrav for innkommende inspeksjon.</span><span class="sxs-lookup"><span data-stu-id="2b525-381">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="2b525-382">Firmaet definerer en kvalitetsgruppe og tilordner deretter varenumrene som er tilknyttet råvarene til denne gruppen.</span><span class="sxs-lookup"><span data-stu-id="2b525-382">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="2b525-383">Senere kjøper selskapet en ny type råvarer som har samme testkrav.</span><span class="sxs-lookup"><span data-stu-id="2b525-383">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="2b525-384">I stedet for å opprette nye testkrav for det nye materialet, legger firmaet til varenummeret for det nye materialet i den eksisterende kvalitetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="2b525-384">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="2b525-385">Det samme produksjonsfirmaet produserer også varer med samme krav til produksjonstesting, og leverer varer med samme krav til utføring av tester før forsendelse.</span><span class="sxs-lookup"><span data-stu-id="2b525-385">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="2b525-386">Firmaet definerer to ekstra kvalitetsgrupper, og tilordner deretter de aktuelle varenumrene til hver gruppe.</span><span class="sxs-lookup"><span data-stu-id="2b525-386">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b525-387">Testvariabler</span><span class="sxs-lookup"><span data-stu-id="2b525-387">Test variables</span></span></td>
<td><span data-ttu-id="2b525-388">Bruk denne siden til å definere og vise variablene som er tilknyttet en kvalitativ test.</span><span class="sxs-lookup"><span data-stu-id="2b525-388">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="2b525-389">For hver variabel kan du definere opplistede resultater som representerer de mulige alternativene.</span><span class="sxs-lookup"><span data-stu-id="2b525-389">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="2b525-390">Du definerer testene på siden <strong>Tester</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b525-390">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="2b525-391">Du må sette testtypen for kvalitative tester til <strong>Alternativ</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b525-391">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="2b525-392">Bruk siden <strong>Testgrupper</strong> til å tilordne en testvariabel til en enkelt test.</span><span class="sxs-lookup"><span data-stu-id="2b525-392">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="2b525-393">En produksjonsfirma som produserer kjeks, bruker en inspeksjonstest til det ferdige produktet.</span><span class="sxs-lookup"><span data-stu-id="2b525-393">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="2b525-394">Denne inspeksjonstesten har flere variabler.</span><span class="sxs-lookup"><span data-stu-id="2b525-394">This inspection test has several variables.</span></span> <span data-ttu-id="2b525-395">Én variabel er smak, og de mulige resultatene for denne variabelen er god og dårlig.</span><span class="sxs-lookup"><span data-stu-id="2b525-395">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="2b525-396">En annen variabel er farge, og de mulige resultatene er for mørk, for lys og riktig.</span><span class="sxs-lookup"><span data-stu-id="2b525-396">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b525-397">Testvariabelresultater</span><span class="sxs-lookup"><span data-stu-id="2b525-397">Test variable outcomes</span></span></td>
<td><span data-ttu-id="2b525-398">Bruk denne siden til å definere, redigere og vise de mulige testresultatene for en testvariabel som er knyttet til en kvalitetstest.</span><span class="sxs-lookup"><span data-stu-id="2b525-398">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="2b525-399">For hvert resultat tilordner du statusen <strong>bestått</strong> eller <strong>mislykket</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b525-399">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="2b525-400">Du må definere en variabel og resultatene for hver kvalitative test som defineres på siden <strong>Tester</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b525-400">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="2b525-401">(For kvalitative tester er testtypen satt til <strong>Alternativ</strong> på <strong>Tester</strong>-siden.) Bruk <strong>Testgrupper</strong>-siden til å tilordne en testvariabel og standardresultatet til en enkelt kvalitetstest.</span><span class="sxs-lookup"><span data-stu-id="2b525-401">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="2b525-402">En produksjonsfirma som produserer kjeks, bruker en inspeksjonstest til det ferdige produktet.</span><span class="sxs-lookup"><span data-stu-id="2b525-402">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="2b525-403">Denne inspeksjonstesten har flere variabler.</span><span class="sxs-lookup"><span data-stu-id="2b525-403">This inspection test has of several variables.</span></span> <span data-ttu-id="2b525-404">Én variabel er smak, og de mulige resultatene for denne variabelen er god og dårlig.</span><span class="sxs-lookup"><span data-stu-id="2b525-404">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="2b525-405">En annen variabel er farge, og de mulige resultatene er for mørk, for lys og riktig.</span><span class="sxs-lookup"><span data-stu-id="2b525-405">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="2b525-406">Statusen <strong>bestått</strong> eller <strong>mislykket</strong> tilordnes hvert resultat.</span><span class="sxs-lookup"><span data-stu-id="2b525-406">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="2b525-407">Under inspeksjonstesten for hver variabel rapporterer inspektøren testresultatet ved å velge ett av resultatene.</span><span class="sxs-lookup"><span data-stu-id="2b525-407">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="2b525-408">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="2b525-408">Additional resources</span></span>
--------

[<span data-ttu-id="2b525-409">Kvalitetsstyringsprosesser</span><span class="sxs-lookup"><span data-stu-id="2b525-409">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="2b525-410">Avviksstyring</span><span class="sxs-lookup"><span data-stu-id="2b525-410">Nonconformance management</span></span>](enable-nonconformance-management.md)

[<span data-ttu-id="2b525-411">Kvalitetsstyring for lagerprosesser</span><span class="sxs-lookup"><span data-stu-id="2b525-411">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]