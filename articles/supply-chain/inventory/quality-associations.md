---
title: Kvalitetstilknytninger
description: Dette emnet beskriver hvordan du kan bruke kvalitettilknytninger i Microsoft Dynamics 365 Supply Chain Management til å generere kvalitetsordrer automatisk som er knyttet til salgs-, innkjøps- og produksjonsprosessene.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f46f09dc9b67cfb04d0320a071c2c739266af58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956771"
---
# <a name="quality-associations"></a><span data-ttu-id="56b11-103">Kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="56b11-103">Quality associations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56b11-104">Dette emnet beskriver hvordan du kan bruke kvalitettilknytninger i Microsoft Dynamics 365 Supply Chain Management til å generere kvalitetsordrer automatisk som er knyttet til salgs-, innkjøps- og produksjonsprosessene.</span><span class="sxs-lookup"><span data-stu-id="56b11-104">This topic describes how you can use quality associations in Microsoft Dynamics 365 Supply Chain Management to automatically generate quality orders that are related to your sales, purchase, and production processes.</span></span>

<span data-ttu-id="56b11-105">En kvalitetstilknytning definerer alle følgende opplysninger om en kvalitetsordre som er generert:</span><span class="sxs-lookup"><span data-stu-id="56b11-105">A quality association defines all the following information for a quality order that is generated:</span></span>

- <span data-ttu-id="56b11-106">Transaksjonshendelsen</span><span class="sxs-lookup"><span data-stu-id="56b11-106">The transaction event</span></span>
- <span data-ttu-id="56b11-107">Settet med tester som må utføres på elementene</span><span class="sxs-lookup"><span data-stu-id="56b11-107">The set of tests that must be performed on the items</span></span>
- <span data-ttu-id="56b11-108">Akseptabelt kvalitetsnivå</span><span class="sxs-lookup"><span data-stu-id="56b11-108">The acceptable quality level (AQL)</span></span>
- <span data-ttu-id="56b11-109">Prøveplanen</span><span class="sxs-lookup"><span data-stu-id="56b11-109">The sampling plan</span></span>

<span data-ttu-id="56b11-110">Du må definere en kvalitetstilknytning for hver variasjon i en forretningsprosess som krever automatisk generering av kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="56b11-110">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="56b11-111">Eksempelvis kan en kvalitetsordre genereres i forretningsprosessen for bestillinger, karanteneordrer, salgsordrer og produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="56b11-111">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="56b11-112">Arbeide med kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="56b11-112">Working with quality associations</span></span>

<span data-ttu-id="56b11-113">Forretningsprosessen som bruker en kvalitetstilknytning, kan knyttes til ulike kildedokumenter, for eksempel bestillinger, salgsordrer eller produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="56b11-113">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="56b11-114">Hver kvalitetstilknytningspost definerer settet med tester, det akseptable kvalitetsnivået og samplingplanen som gjelder for kvalitetsordrene som genereres.</span><span class="sxs-lookup"><span data-stu-id="56b11-114">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="56b11-115">Du må definere en kvalitetstilknytningspost for hver variasjon i en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="56b11-115">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="56b11-116">Du kan for eksempel definere en kvalitetstilknytning som genererer en kvalitetsordre når et produkt for bestillingsmottak oppdateres.</span><span class="sxs-lookup"><span data-stu-id="56b11-116">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="56b11-117">Avhengig av oppsettet til utførelsesplanen kan selve utløsingsprosessen blokkeres mens det er en åpen kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="56b11-117">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order.</span></span> <span data-ttu-id="56b11-118">Etterfølgende prosesser, for eksempel fakturering av bestillinger, kan eventuelt blokkeres.</span><span class="sxs-lookup"><span data-stu-id="56b11-118">Alternatively, subsequent processes, such as purchase order invoicing, can be blocked.</span></span>

> [!NOTE]
> <span data-ttu-id="56b11-119">Når det finnes åpne kvalitetsordrer, blokkeres lagerantall automatisk fra å bli utstedt.</span><span class="sxs-lookup"><span data-stu-id="56b11-119">While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="56b11-120">Avhengig av innstillingen i **Full blokkering**-feltet på siden **Vareprøver** er antallet enten antallet på kvalitetsordren eller antallet på kildedokumentlinjen.</span><span class="sxs-lookup"><span data-stu-id="56b11-120">Depending on the setting of the **Full blocking** field on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span> <span data-ttu-id="56b11-121">Hvis du vil ha mer informasjon, kan du se [Vareprøve for kvalitetsstyring](quality-item-sampling.md).</span><span class="sxs-lookup"><span data-stu-id="56b11-121">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>

<span data-ttu-id="56b11-122">For en gitt forretningsprosess identifiserer kvalitetstilknytningspost hendelsen og betingelsene som en kvalitetsordre genereres for.</span><span class="sxs-lookup"><span data-stu-id="56b11-122">For a given business process, the quality association record identifies the event and conditions that a quality order is generated for.</span></span> <span data-ttu-id="56b11-123">Betingelsene kan være spesifikke for et område eller en juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="56b11-123">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="56b11-124">En kvalitetsordre som omfatter destruktive tester, kan bare genereres når hvis det finnes lagerbeholdning for hendelsen.</span><span class="sxs-lookup"><span data-stu-id="56b11-124">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="56b11-125">Hvis du vil arbeide med kvalitetstilknytninger, kan du gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Kvalitetstilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="56b11-125">To work with quality associations, go to **Inventory management \> Setup \> Quality control \> Quality associations**.</span></span> <span data-ttu-id="56b11-126">De følgende eksemplene illustrerer hvordan en kvalitetstilknytningspost er definert for variasjonene innen ulike forretningsprosesser.</span><span class="sxs-lookup"><span data-stu-id="56b11-126">The following examples show how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="56b11-127">For hvert eksempel oppsummere følgende tabell hendelsene og betingelsene som er definert av en kvalitetstilknytningspost.</span><span class="sxs-lookup"><span data-stu-id="56b11-127">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="56b11-128">Referansetype</span><span class="sxs-lookup"><span data-stu-id="56b11-128">Reference type</span></span></th>
<th><span data-ttu-id="56b11-129">Hendelsestype</span><span class="sxs-lookup"><span data-stu-id="56b11-129">Event type</span></span></th>
<th><span data-ttu-id="56b11-130">Utførelse</span><span class="sxs-lookup"><span data-stu-id="56b11-130">Execution</span></span></th>
<th><span data-ttu-id="56b11-131">Hendelsesblokkering</span><span class="sxs-lookup"><span data-stu-id="56b11-131">Event blocking</span></span></th>
<th><span data-ttu-id="56b11-132">Dokumentreferanse</span><span class="sxs-lookup"><span data-stu-id="56b11-132">Document reference</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="56b11-133">Beholdning</span><span class="sxs-lookup"><span data-stu-id="56b11-133">Inventory</span></span></td>
<td><span data-ttu-id="56b11-134">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="56b11-134">Not applicable</span></span></td>
<td><span data-ttu-id="56b11-135">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="56b11-135">Not applicable</span></span></td>
<td><span data-ttu-id="56b11-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="56b11-136">None</span></span></td>
<td><span data-ttu-id="56b11-137">Alle</span><span class="sxs-lookup"><span data-stu-id="56b11-137">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="56b11-138">Salg</span><span class="sxs-lookup"><span data-stu-id="56b11-138">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="56b11-139">Plukkingsprosess er planlagt</span><span class="sxs-lookup"><span data-stu-id="56b11-139">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="56b11-140">Før</span><span class="sxs-lookup"><span data-stu-id="56b11-140">Before</span></span></td>
<td><span data-ttu-id="56b11-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="56b11-141">None</span></span></td>
<td rowspan="22"><span data-ttu-id="56b11-142">Bare Spesifikk ID, Gruppe eller Alle</span><span class="sxs-lookup"><span data-stu-id="56b11-142">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-143">Plukkingsprosess</span><span class="sxs-lookup"><span data-stu-id="56b11-143">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-144">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="56b11-144">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-145">Faktura</span><span class="sxs-lookup"><span data-stu-id="56b11-145">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="56b11-146">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="56b11-146">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="56b11-147">Før</span><span class="sxs-lookup"><span data-stu-id="56b11-147">Before</span></span></td>
<td><span data-ttu-id="56b11-148">Ingen</span><span class="sxs-lookup"><span data-stu-id="56b11-148">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-149">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="56b11-149">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-150">Faktura</span><span class="sxs-lookup"><span data-stu-id="56b11-150">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="56b11-151">Kjøp</span><span class="sxs-lookup"><span data-stu-id="56b11-151">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="56b11-152">Kvitteringsliste</span><span class="sxs-lookup"><span data-stu-id="56b11-152">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="56b11-153">Før</span><span class="sxs-lookup"><span data-stu-id="56b11-153">Before</span></span></td>
<td><span data-ttu-id="56b11-154">Ingen</span><span class="sxs-lookup"><span data-stu-id="56b11-154">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-155">Kvitteringsliste</span><span class="sxs-lookup"><span data-stu-id="56b11-155">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-156">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="56b11-156">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-157">Faktura</span><span class="sxs-lookup"><span data-stu-id="56b11-157">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="56b11-158">Etter</span><span class="sxs-lookup"><span data-stu-id="56b11-158">After</span></span></td>
<td><span data-ttu-id="56b11-159">Ingen</span><span class="sxs-lookup"><span data-stu-id="56b11-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-160">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="56b11-160">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-161">Faktura</span><span class="sxs-lookup"><span data-stu-id="56b11-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="56b11-162">Registrering</span><span class="sxs-lookup"><span data-stu-id="56b11-162">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="56b11-163">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="56b11-163">Not applicable</span></span></td>
<td><span data-ttu-id="56b11-164">Ingen</span><span class="sxs-lookup"><span data-stu-id="56b11-164">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-165">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="56b11-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-166">Faktura</span><span class="sxs-lookup"><span data-stu-id="56b11-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="56b11-167">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="56b11-167">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="56b11-168">Før</span><span class="sxs-lookup"><span data-stu-id="56b11-168">Before</span></span></td>
<td><span data-ttu-id="56b11-169">Ingen</span><span class="sxs-lookup"><span data-stu-id="56b11-169">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-170">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="56b11-170">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-171">Faktura</span><span class="sxs-lookup"><span data-stu-id="56b11-171">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="56b11-172">Etter</span><span class="sxs-lookup"><span data-stu-id="56b11-172">After</span></span></td>
<td><span data-ttu-id="56b11-173">Ingen</span><span class="sxs-lookup"><span data-stu-id="56b11-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-174">Faktura</span><span class="sxs-lookup"><span data-stu-id="56b11-174">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="56b11-175">Produksjon</span><span class="sxs-lookup"><span data-stu-id="56b11-175">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="56b11-176">Registrering</span><span class="sxs-lookup"><span data-stu-id="56b11-176">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="56b11-177">Gjelder ikke her</span><span class="sxs-lookup"><span data-stu-id="56b11-177">Not applicable</span></span></td>
<td><span data-ttu-id="56b11-178">Ingen</span><span class="sxs-lookup"><span data-stu-id="56b11-178">None</span></span></td>
<td rowspan="12"><span data-ttu-id="56b11-179">Alle</span><span class="sxs-lookup"><span data-stu-id="56b11-179">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-180">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="56b11-180">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-181">Slutt</span><span class="sxs-lookup"><span data-stu-id="56b11-181">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="56b11-182">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="56b11-182">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="56b11-183">Før</span><span class="sxs-lookup"><span data-stu-id="56b11-183">Before</span></span></td>
<td><span data-ttu-id="56b11-184">Ingen</span><span class="sxs-lookup"><span data-stu-id="56b11-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-185">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="56b11-185">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-186">Slutt</span><span class="sxs-lookup"><span data-stu-id="56b11-186">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="56b11-187">Etter</span><span class="sxs-lookup"><span data-stu-id="56b11-187">After</span></span></td>
<td><span data-ttu-id="56b11-188">Ingen</span><span class="sxs-lookup"><span data-stu-id="56b11-188">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-189">Slutt</span><span class="sxs-lookup"><span data-stu-id="56b11-189">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="56b11-190">Karantene</span><span class="sxs-lookup"><span data-stu-id="56b11-190">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="56b11-191">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="56b11-191">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="56b11-192">Før</span><span class="sxs-lookup"><span data-stu-id="56b11-192">Before</span></span></td>
<td><span data-ttu-id="56b11-193">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="56b11-193">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-194">Slutt</span><span class="sxs-lookup"><span data-stu-id="56b11-194">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-195">Etter</span><span class="sxs-lookup"><span data-stu-id="56b11-195">After</span></span></td>
<td><span data-ttu-id="56b11-196">Slutt</span><span class="sxs-lookup"><span data-stu-id="56b11-196">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-197">Slutt</span><span class="sxs-lookup"><span data-stu-id="56b11-197">End</span></span></td>
<td><span data-ttu-id="56b11-198">Før</span><span class="sxs-lookup"><span data-stu-id="56b11-198">Before</span></span></td>
<td><span data-ttu-id="56b11-199">Slutt</span><span class="sxs-lookup"><span data-stu-id="56b11-199">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="56b11-200">Ruteoperasjon</span><span class="sxs-lookup"><span data-stu-id="56b11-200">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="56b11-201">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="56b11-201">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="56b11-202">Før</span><span class="sxs-lookup"><span data-stu-id="56b11-202">Before</span></span></td>
<td><span data-ttu-id="56b11-203">None</span><span class="sxs-lookup"><span data-stu-id="56b11-203">None</span></span></td>
<td rowspan="3"><span data-ttu-id="56b11-204">Bestemt ID, Gruppe eller Alle, og Ressursspesifikk, Gruppe eller Alle</span><span class="sxs-lookup"><span data-stu-id="56b11-204">Specific ID, Group, or All, and specific Resource, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-205">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="56b11-205">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-206">Etter</span><span class="sxs-lookup"><span data-stu-id="56b11-206">After</span></span></td>
<td><span data-ttu-id="56b11-207">None</span><span class="sxs-lookup"><span data-stu-id="56b11-207">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="56b11-208">Koproduktproduksjon</span><span class="sxs-lookup"><span data-stu-id="56b11-208">Co-product production</span></span></td>
<td><span data-ttu-id="56b11-209">Registrering</span><span class="sxs-lookup"><span data-stu-id="56b11-209">Registration</span></span></td>
<td><span data-ttu-id="56b11-210">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="56b11-210">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="56b11-211">None</span><span class="sxs-lookup"><span data-stu-id="56b11-211">None</span></span></td>
<td rowspan="3"><span data-ttu-id="56b11-212">Alle</span><span class="sxs-lookup"><span data-stu-id="56b11-212">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="56b11-213">Ferdigmeld</span><span class="sxs-lookup"><span data-stu-id="56b11-213">Report as finished</span></span></td>
<td><span data-ttu-id="56b11-214">Før</span><span class="sxs-lookup"><span data-stu-id="56b11-214">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-215">Etter</span><span class="sxs-lookup"><span data-stu-id="56b11-215">After</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="56b11-216">Funksjonen *Kvalitetsstyring for lagerprosesser* legger til funksjoner for kvalitetsordrebehandling for produksjon med feltet **Hendelsestype** satt til *Ferdigmeld* og **Utførelse** satt til *Etter*, og for innkjøp med **Hendelsestype** satt til *Registrering*.</span><span class="sxs-lookup"><span data-stu-id="56b11-216">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production where the **Event type** field is set to *Report as finished* and the **Execution** field is set to *After*, and for purchases where the **Event type** field is set to *Registration*.</span></span> <span data-ttu-id="56b11-217">For mer informasjon, se [Kvalitetsstyring for lagerprosesser](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="56b11-217">For more information, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

<span data-ttu-id="56b11-218">Tabellen nedenfor inneholder mer informasjon om hvordan kvalitetsordrer kan genereres for bestemte typer prosesser.</span><span class="sxs-lookup"><span data-stu-id="56b11-218">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>

<div class="tableSection">
<table>
<thead>
<tr>
<th><span data-ttu-id="56b11-219">Type av prosess</span><span class="sxs-lookup"><span data-stu-id="56b11-219">Type of process</span></span></th>
<th><span data-ttu-id="56b11-220">Når kvalitetsordrer kan genereres automatisk</span><span class="sxs-lookup"><span data-stu-id="56b11-220">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="56b11-221">Når kvalitetsordrer kan genereres hvis destruktiv testing kreves</span><span class="sxs-lookup"><span data-stu-id="56b11-221">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="56b11-222">Betingelsesinformasjon</span><span class="sxs-lookup"><span data-stu-id="56b11-222">Condition information</span></span></th>
<th><span data-ttu-id="56b11-223">Informasjon om manuell generering</span><span class="sxs-lookup"><span data-stu-id="56b11-223">Manual generation information</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="56b11-224">Bestilling</span><span class="sxs-lookup"><span data-stu-id="56b11-224">Purchase order</span></span></td>
<td><span data-ttu-id="56b11-225">Før eller etter en kvitteringsliste eller produktkvittering for materialet som mottas, posteres</span><span class="sxs-lookup"><span data-stu-id="56b11-225">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="56b11-226">Etter produktkvitteringen for materialet som mottas, er postert, fordi materialet må være tilgjengelig for destruktiv testing</span><span class="sxs-lookup"><span data-stu-id="56b11-226">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="56b11-227">Behovet for en kvalitetsordre kan reflektere et bestemt område, en vare, en leverandør eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="56b11-227">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="56b11-228">En manuelt generert kvalitetsordre som viser til en bestilling, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="56b11-228">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-229">Karanteneordre</span><span class="sxs-lookup"><span data-stu-id="56b11-229">Quarantine order</span></span></td>
<td><span data-ttu-id="56b11-230">Før eller etter karanteordren er rapportert som fullført eller avsluttet</span><span class="sxs-lookup"><span data-stu-id="56b11-230">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="56b11-231">Kvalitetsordrer som krever destruktive tester, kan ikke genereres.</span><span class="sxs-lookup"><span data-stu-id="56b11-231">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="56b11-232">Det forutsettes at karanteneordrefunksjonaliteten behandler disposisjonen av materialet som blir ødelagt.</span><span class="sxs-lookup"><span data-stu-id="56b11-232">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="56b11-233">Behovet for en kvalitetsordre kan reflektere et bestemt område, en vare, en leverandør eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="56b11-233">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="56b11-234">En manuelt generert kvalitetsordre som viser til en karanteneordre, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="56b11-234">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-235">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="56b11-235">Sales order</span></span></td>
<td><span data-ttu-id="56b11-236">Før en planlagt plukkeprosessen eller følgeseddeloppdatering for varene som leveres</span><span class="sxs-lookup"><span data-stu-id="56b11-236">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="56b11-237">I alle trinn</span><span class="sxs-lookup"><span data-stu-id="56b11-237">At any step</span></span></td>
<td><span data-ttu-id="56b11-238">Kravet til en kvalitetsordre kan reflektere et bestemt område, en vare, en kunde eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="56b11-238">The requirement for a quality order can reflect a specific site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="56b11-239">En manuelt generert kvalitetsordre som viser til en salgsordre, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="56b11-239">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-240">Produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="56b11-240">Production order</span></span></td>
<td><span data-ttu-id="56b11-241">Før eller etter den ferdige kvaliteten for produksjonsordren er rapportert</span><span class="sxs-lookup"><span data-stu-id="56b11-241">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="56b11-242">Etter den ferdige kvaliteten for produksjonsordren er rapportert</span><span class="sxs-lookup"><span data-stu-id="56b11-242">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="56b11-243">Behovet for en kvalitetsordre kan reflektere et bestemt område eller vare, eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="56b11-243">The requirement for a quality order can reflect a specific site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="56b11-244">En manuelt generert kvalitetsordre som viser til en produksjonsordre, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="56b11-244">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-245">Produksjonsordre som har en ruteoperasjon</span><span class="sxs-lookup"><span data-stu-id="56b11-245">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="56b11-246">Før eller etter at rapporten for en operasjon er fullført</span><span class="sxs-lookup"><span data-stu-id="56b11-246">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="56b11-247">Etter at rapporteringen av produksjonen er fullført for den siste operasjonen</span><span class="sxs-lookup"><span data-stu-id="56b11-247">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="56b11-248">Behovet for en kvalitetsordre kan reflektere et bestemt område, en vare eller en operasjonsressurs eller en kombinasjon av disse betingelsene.</span><span class="sxs-lookup"><span data-stu-id="56b11-248">The requirement for a quality order can reflect a specific site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="56b11-249">En manuelt generert kvalitetsordre som viser til en ruteoperasjon, kan benytte informasjon i en kvalitetstilknytningspost, for eksempel testprøveplanen.</span><span class="sxs-lookup"><span data-stu-id="56b11-249">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="56b11-250">Lager</span><span class="sxs-lookup"><span data-stu-id="56b11-250">Inventory</span></span></td>
<td><span data-ttu-id="56b11-251">En kvalitetsordre kan ikke genereres automatisk for en transaksjon innen en lagerjournal eller for overføringsordretransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="56b11-251">A quality order can't be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="56b11-252">En kvalitetsordre må opprettes manuelt for en vares lagerantall.</span><span class="sxs-lookup"><span data-stu-id="56b11-252">A quality order must be manually created for an item's inventory quantity.</span></span> <span data-ttu-id="56b11-253">Varens fysiske lagerbeholdning kreves.</span><span class="sxs-lookup"><span data-stu-id="56b11-253">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a><span data-ttu-id="56b11-254">Eksempler på automatisk generering av kvalitetsordrer</span><span class="sxs-lookup"><span data-stu-id="56b11-254">Examples of automatic generation of quality orders</span></span>

### <a name="purchasing"></a><span data-ttu-id="56b11-255">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="56b11-255">Purchasing</span></span>

<span data-ttu-id="56b11-256">I innkjøp, hvis du du angir feltet **Hendelsestype** til *Produktkvittering* og feltet **Utførelse** til *Etter* på siden **Kvalitetstilknytninger**, får du følgende resultater:</span><span class="sxs-lookup"><span data-stu-id="56b11-256">In purchasing, if you set the **Event type** field to *Product receipt* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="56b11-257">Hvis alternativet **Per oppdatert mengde** er satt til *Ja*, genereres det en kvalitetsordre for hvert mottak mot bestillingen basert på det mottatte antallet og innstillingene i vareprøven.</span><span class="sxs-lookup"><span data-stu-id="56b11-257">If the **Per updated quantity** option is set to *Yes*, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="56b11-258">Hver gang et antall mottas mot bestillingen, genereres nye kvalitetsordrer basert på det nylig mottatte antallet.</span><span class="sxs-lookup"><span data-stu-id="56b11-258">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="56b11-259">Hvis alternativet **Per oppdatert mengde** er satt til *Nei*, genereres det en kvalitetsordre for det første mottaket mot bestillingen basert på det mottatte antallet.</span><span class="sxs-lookup"><span data-stu-id="56b11-259">If the **Per updated quantity** option is set to *No*, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="56b11-260">I tillegg blir én eller flere kvalitetsordrer opprettet på grunnlag av restantallet, avhengig av sporingsdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="56b11-260">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="56b11-261">Kvalitetsordrer genereres ikke for etterfølgende mottak mot bestillingen.</span><span class="sxs-lookup"><span data-stu-id="56b11-261">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="56b11-262">Produksjon</span><span class="sxs-lookup"><span data-stu-id="56b11-262">Production</span></span>

<span data-ttu-id="56b11-263">I produksjon, hvis du du angir feltet **Hendelsestype** til *Ferdigmeld* og feltet **Utførelse** til *Etter* på siden **Kvalitetstilknytninger**, får du følgende resultater:</span><span class="sxs-lookup"><span data-stu-id="56b11-263">In production, if you set the **Event type** field to *Report as finished* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="56b11-264">Hvis alternativet **Per oppdatert mengde** er satt til *Ja*, genereres det en kvalitetsordre for hver fullførte antall og innstillingene i vareprøven.</span><span class="sxs-lookup"><span data-stu-id="56b11-264">If the **Per updated quantity** option is set to *Yes*, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="56b11-265">Hver gang et antall rapporteres som fullført mot produksjonsordren, genereres nye kvalitetsordrer basert på det nylig fullførte antallet.</span><span class="sxs-lookup"><span data-stu-id="56b11-265">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on the newly finished quantity.</span></span> <span data-ttu-id="56b11-266">Denne genereringslogikken er konsekvent med innkjøp.</span><span class="sxs-lookup"><span data-stu-id="56b11-266">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="56b11-267">Hvis alternativet **Per oppdatert mengde** er satt til *Nei*, genereres det en kvalitetsordre første gang antallet rapporteres som fullført, basert på det fullførte antallet.</span><span class="sxs-lookup"><span data-stu-id="56b11-267">If the **Per updated quantity** option is set to *No*, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="56b11-268">I tillegg blir én eller flere kvalitetsordrer opprettet på grunnlag av restantallet, avhengig av sporingsdimensjonene for vareprøven.</span><span class="sxs-lookup"><span data-stu-id="56b11-268">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="56b11-269">Kvalitetsordrer genereres ikke for etterfølgende ferdigmeldte antall.</span><span class="sxs-lookup"><span data-stu-id="56b11-269">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="56b11-270">Kvalitetsspesifikasjon</span><span class="sxs-lookup"><span data-stu-id="56b11-270">Quality specification</span></span></th>
<th><span data-ttu-id="56b11-271">Per oppdatert mengde</span><span class="sxs-lookup"><span data-stu-id="56b11-271">Per updated quantity</span></span></th>
<th><span data-ttu-id="56b11-272">Per sporingsdimensjon</span><span class="sxs-lookup"><span data-stu-id="56b11-272">Per tracking dimension</span></span></th>
<th><span data-ttu-id="56b11-273">Resultat</span><span class="sxs-lookup"><span data-stu-id="56b11-273">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="56b11-274">Prosent: 10 %</span><span class="sxs-lookup"><span data-stu-id="56b11-274">Percentage: 10%</span></span></td>
<td><span data-ttu-id="56b11-275">Ja</span><span class="sxs-lookup"><span data-stu-id="56b11-275">Yes</span></span></td>
<td>
<p><span data-ttu-id="56b11-276">Partinummer: Nei</span><span class="sxs-lookup"><span data-stu-id="56b11-276">Batch number: No</span></span></p>
<p><span data-ttu-id="56b11-277">Serienummer: Nei</span><span class="sxs-lookup"><span data-stu-id="56b11-277">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="56b11-278">Ordreantall: 100</span><span class="sxs-lookup"><span data-stu-id="56b11-278">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="56b11-279">Rapporter som ferdig for 30</span><span class="sxs-lookup"><span data-stu-id="56b11-279">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="56b11-280">Kvalitetsordre 1 for 3 (10 % av 30)</span><span class="sxs-lookup"><span data-stu-id="56b11-280">Quality order 1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="56b11-281">Rapporter som ferdig for 70</span><span class="sxs-lookup"><span data-stu-id="56b11-281">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="56b11-282">Kvalitetsordre 2 for 7 (10 % av restordreantallet, som er 70 i dette tilfellet)</span><span class="sxs-lookup"><span data-stu-id="56b11-282">Quality order 2 for 7 (10% of the remaining order quantity, which is 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="56b11-283">Fast antall: 1</span><span class="sxs-lookup"><span data-stu-id="56b11-283">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="56b11-284">Ingen</span><span class="sxs-lookup"><span data-stu-id="56b11-284">No</span></span></td>
<td>
<p><span data-ttu-id="56b11-285">Partinummer: Nei</span><span class="sxs-lookup"><span data-stu-id="56b11-285">Batch number: No</span></span></p>
<p><span data-ttu-id="56b11-286">Serienummer: Nei</span><span class="sxs-lookup"><span data-stu-id="56b11-286">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="56b11-287">Ordreantall: 100</span><span class="sxs-lookup"><span data-stu-id="56b11-287">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="56b11-288">Rapporter som ferdig for 30</span><span class="sxs-lookup"><span data-stu-id="56b11-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="56b11-289">Kvalitetsordre 1 for 1 (for det første ferdigmeldte antallet, som har en fast verdi på 1)</span><span class="sxs-lookup"><span data-stu-id="56b11-289">Quality order 1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="56b11-290">Kvalitetsordre 2 for 1 (for det resterende antallet, som fremdeles har en fast verdi på 1)</span><span class="sxs-lookup"><span data-stu-id="56b11-290">Quality order 2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="56b11-291">Rapporter som ferdig for 10</span><span class="sxs-lookup"><span data-stu-id="56b11-291">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="56b11-292">Ingen kvalitetsordrer er opprettet.</span><span class="sxs-lookup"><span data-stu-id="56b11-292">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="56b11-293">Rapporter som ferdig for 60</span><span class="sxs-lookup"><span data-stu-id="56b11-293">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="56b11-294">Ingen kvalitetsordrer er opprettet.</span><span class="sxs-lookup"><span data-stu-id="56b11-294">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="56b11-295">Fast antall: 1</span><span class="sxs-lookup"><span data-stu-id="56b11-295">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="56b11-296">Ja</span><span class="sxs-lookup"><span data-stu-id="56b11-296">Yes</span></span></td>
<td>
<p><span data-ttu-id="56b11-297">Partinummer: Ja</span><span class="sxs-lookup"><span data-stu-id="56b11-297">Batch number: Yes</span></span></p>
<p><span data-ttu-id="56b11-298">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="56b11-298">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="56b11-299">Ordreantall: 10</span><span class="sxs-lookup"><span data-stu-id="56b11-299">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="56b11-300">Ferdigmeld for 3: 1 for partinummer b1, serienummer s1. 1 for partinummer b2, serienummer s2. og 1 for partinummer b3, serienummer s3</span><span class="sxs-lookup"><span data-stu-id="56b11-300">Report as finished for 3: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; and 1 for batch number b3, serial number s3</span></span>
<ul>
<li><span data-ttu-id="56b11-301">Kvalitetsordre 1 for 1 av partinummer b1, serienummer s1</span><span class="sxs-lookup"><span data-stu-id="56b11-301">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="56b11-302">Kvalitetsordre 2 for 1 av partinummer b2, serienummer s2</span><span class="sxs-lookup"><span data-stu-id="56b11-302">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="56b11-303">Kvalitetsordre 3 for 1 av partinummer b3, serienummer s3</span><span class="sxs-lookup"><span data-stu-id="56b11-303">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="56b11-304">Ferdigmeld for 2: 1 for partinummer b4, serienummer 4; og 1 for partinummer b5, serienummer s5</span><span class="sxs-lookup"><span data-stu-id="56b11-304">Report as finished for 2: 1 for batch number b4, serial number s4; and 1 for batch number b5, serial number s5</span></span>
<ul>
<li><span data-ttu-id="56b11-305">Kvalitetsordre 4 for 1 av partinummer b4, serienummer s4</span><span class="sxs-lookup"><span data-stu-id="56b11-305">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
<li><span data-ttu-id="56b11-306">Kvalitetsordre 5 for 1 av partinummer b5, serienummer s5</span><span class="sxs-lookup"><span data-stu-id="56b11-306">Quality order 5 for 1 of batch number b5, serial number s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="56b11-307"><strong>Merk:</strong> Partiet kan brukes på nytt.</span><span class="sxs-lookup"><span data-stu-id="56b11-307"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="56b11-308">Fast antall: 2</span><span class="sxs-lookup"><span data-stu-id="56b11-308">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="56b11-309">Ingen</span><span class="sxs-lookup"><span data-stu-id="56b11-309">No</span></span></td>
<td>
<p><span data-ttu-id="56b11-310">Partinummer: Ja</span><span class="sxs-lookup"><span data-stu-id="56b11-310">Batch number: Yes</span></span></p>
<p><span data-ttu-id="56b11-311">Serienummer: Ja</span><span class="sxs-lookup"><span data-stu-id="56b11-311">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="56b11-312">Ordreantall: 10</span><span class="sxs-lookup"><span data-stu-id="56b11-312">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="56b11-313">Ferdigmeld for 4: 1 for partinummer b1, serienummer s1. 1 for partinummer b2, serienummer s2. 1 for partinummer b3, serienummer s3 og 1 for partinummer b4, serienummer s4</span><span class="sxs-lookup"><span data-stu-id="56b11-313">Report as finished for 4: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; 1 for batch number b3, serial number s3; and 1 for batch number b4, serial number s4</span></span>
<ul>
<li><span data-ttu-id="56b11-314">Kvalitetsordre 1 for 1 av partinummer b1, serienummer s1</span><span class="sxs-lookup"><span data-stu-id="56b11-314">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="56b11-315">Kvalitetsordre 2 for 1 av partinummer b2, serienummer s2</span><span class="sxs-lookup"><span data-stu-id="56b11-315">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="56b11-316">Kvalitetsordre 3 for 1 av partinummer b3, serienummer s3</span><span class="sxs-lookup"><span data-stu-id="56b11-316">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
<li><span data-ttu-id="56b11-317">Kvalitetsordre 4 for 1 av partinummer b4, serienummer s4</span><span class="sxs-lookup"><span data-stu-id="56b11-317">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="56b11-318">Kvalitetsordre 5 for 2, uten referanse til et partinummer og et serienummer</span><span class="sxs-lookup"><span data-stu-id="56b11-318">Quality order 5 for 2, without a reference to a batch number and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="56b11-319">Ferdigmeld for 6: 1 for partinummer b5, serienummer s5. 1 for partinummer b6, serienummer s6. 1 for partinummer b7, serienummer s7. 1 for partinummer b8, serienummer s8. 1 for partinummer b9, serienummer s9 og 1 for partinummer b10, serienummer s10</span><span class="sxs-lookup"><span data-stu-id="56b11-319">Report as finished for 6: 1 for batch number b5, serial number s5; 1 for batch number b6, serial number s6; 1 for batch number b7, serial number s7; 1 for batch number b8, serial number s8; 1 for batch number b9, serial number s9; and 1 for batch number b10, serial number s10</span></span>
<ul>
<li><span data-ttu-id="56b11-320">Ingen kvalitetsordrer er opprettet.</span><span class="sxs-lookup"><span data-stu-id="56b11-320">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="56b11-321">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="56b11-321">Additional resources</span></span>

- [<span data-ttu-id="56b11-322">Kvalitetsstyringsprosesser</span><span class="sxs-lookup"><span data-stu-id="56b11-322">Quality management processes</span></span>](quality-management-processes.md)
- [<span data-ttu-id="56b11-323">Aktivere kvalitets- og avviksstyring</span><span class="sxs-lookup"><span data-stu-id="56b11-323">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="56b11-324">Kvalitetsstyring for lagerprosesser</span><span class="sxs-lookup"><span data-stu-id="56b11-324">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
