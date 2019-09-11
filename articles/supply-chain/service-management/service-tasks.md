---
title: Oversikt over serviceoppgaver
description: Bruk serviceoppgaver til å beskrive oppgaven som skal fullføres under en serviceordre. Både teknikere og kunder kan se denne informasjonen.
author: ShylaThompson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd7e5293ef506c6d785b420824f2c2a2c96112f7
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865903"
---
# <a name="service-tasks-overview"></a><span data-ttu-id="917e3-104">Oversikt over serviceoppgaver</span><span class="sxs-lookup"><span data-stu-id="917e3-104">Service tasks overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="917e3-105">Bruk serviceoppgaver til å beskrive oppgaven som skal fullføres under en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="917e3-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="917e3-106">Både teknikere og kunder kan se denne informasjonen.</span><span class="sxs-lookup"><span data-stu-id="917e3-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="917e3-107">Du oppretter serviceoppgaver på **Serviceoppgaver**-siden, og du knytter serviceoppgaver til en bestemt serviceavtale eller serviceordre ved å opprette serviceoppgaverelasjoner.</span><span class="sxs-lookup"><span data-stu-id="917e3-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="917e3-108">Hver gang du oppretter en serviceoppgaverelasjon, kan du opprette følgende:</span><span class="sxs-lookup"><span data-stu-id="917e3-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="917e3-109">Interne merknader for oppgaven, for eksempel detaljerte tekniske forespørsler for oppgaven som teknikeren bør kjenne til.</span><span class="sxs-lookup"><span data-stu-id="917e3-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="917e3-110">Eksterne merknader som kunden kan se.</span><span class="sxs-lookup"><span data-stu-id="917e3-110">External notes that the customer can see.</span></span> <span data-ttu-id="917e3-111">Disse kan gi en mindre teknisk forklaring av oppgaven som utføres, i henhold til avtalen mellom kunden og servicefirmaet.</span><span class="sxs-lookup"><span data-stu-id="917e3-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="917e3-112">Når du har definert en serviceoppgaverelasjon mellom en serviceoppgave og en serviceordre eller serviceavtale, kan du angi denne serviceoppgaven når du oppretter serviceordrelinjer eller serviceavtalelinjer for den gjeldende serviceordren eller serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="917e3-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="917e3-113">Når du genererer serviceordrer fra en serviceavtale, kan du bruke serviceoppgavene som er tilordnet hver serviceavtalelinje, til å gruppere serviceordrelinjer i serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="917e3-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="917e3-114">Opprette en serviceoppgave</span><span class="sxs-lookup"><span data-stu-id="917e3-114">Create a service task</span></span>

1. <span data-ttu-id="917e3-115">Klikk **Servicestyring** \> **Oppsett** \> **Serviceoppgaver**.</span><span class="sxs-lookup"><span data-stu-id="917e3-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="917e3-116">Opprett en ny linje.</span><span class="sxs-lookup"><span data-stu-id="917e3-116">Create a new line.</span></span>
3. <span data-ttu-id="917e3-117">Angi service-ID og -beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="917e3-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="917e3-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="917e3-118">Example</span></span>

<span data-ttu-id="917e3-119">En tekniker må fullføre to jobber på en girkasse (serviceobjekt GB-1234) hos en kunde.</span><span class="sxs-lookup"><span data-stu-id="917e3-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="917e3-120">Det opprettes en serviceavtale for kunden, og flere transaksjoner knyttes til jobbene.</span><span class="sxs-lookup"><span data-stu-id="917e3-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="917e3-121">Serviceavtalen og serviceavtalelinjene for de to jobbene er som følger:</span><span class="sxs-lookup"><span data-stu-id="917e3-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="917e3-122">Serviceavtale</span><span class="sxs-lookup"><span data-stu-id="917e3-122">Service agreement</span></span>

| <span data-ttu-id="917e3-123">Project</span><span class="sxs-lookup"><span data-stu-id="917e3-123">Project</span></span> | <span data-ttu-id="917e3-124">Serviceavtale</span><span class="sxs-lookup"><span data-stu-id="917e3-124">Service agreement</span></span> | <span data-ttu-id="917e3-125">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="917e3-125">Description</span></span>                                  | <span data-ttu-id="917e3-126">Gruppere</span><span class="sxs-lookup"><span data-stu-id="917e3-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="917e3-127">9012</span><span class="sxs-lookup"><span data-stu-id="917e3-127">9012</span></span>    | <span data-ttu-id="917e3-128">000008\_001</span><span class="sxs-lookup"><span data-stu-id="917e3-128">000008\_001</span></span>       | <span data-ttu-id="917e3-129">Inspeksjon og rutineerstatning – GB-1234</span><span class="sxs-lookup"><span data-stu-id="917e3-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="917e3-130">Bonus</span><span class="sxs-lookup"><span data-stu-id="917e3-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="917e3-131">Serviceavtalelinjer</span><span class="sxs-lookup"><span data-stu-id="917e3-131">Service agreement lines</span></span>

| <span data-ttu-id="917e3-132">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="917e3-132">Description</span></span>             | <span data-ttu-id="917e3-133">transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="917e3-133">Transaction type</span></span> | <span data-ttu-id="917e3-134">Serviceobjekt</span><span class="sxs-lookup"><span data-stu-id="917e3-134">Service object</span></span> | <span data-ttu-id="917e3-135">Serviceoppgave</span><span class="sxs-lookup"><span data-stu-id="917e3-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="917e3-136">Inspeksjon og rengjøring</span><span class="sxs-lookup"><span data-stu-id="917e3-136">Inspection and cleaning</span></span> | <span data-ttu-id="917e3-137">Time</span><span class="sxs-lookup"><span data-stu-id="917e3-137">Hour</span></span>             | <span data-ttu-id="917e3-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="917e3-138">GB-1234</span></span>        | <span data-ttu-id="917e3-139">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="917e3-139">I/C - GB1234</span></span> |
| <span data-ttu-id="917e3-140">Reise</span><span class="sxs-lookup"><span data-stu-id="917e3-140">Travel</span></span>                  | <span data-ttu-id="917e3-141">Expense</span><span class="sxs-lookup"><span data-stu-id="917e3-141">Expense</span></span>          | <span data-ttu-id="917e3-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="917e3-142">GB-1234</span></span>        | <span data-ttu-id="917e3-143">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="917e3-143">I/C - GB1234</span></span> |
| <span data-ttu-id="917e3-144">Materialer</span><span class="sxs-lookup"><span data-stu-id="917e3-144">Materials</span></span>               | <span data-ttu-id="917e3-145">Element</span><span class="sxs-lookup"><span data-stu-id="917e3-145">Item</span></span>             | <span data-ttu-id="917e3-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="917e3-146">GB-1234</span></span>        | <span data-ttu-id="917e3-147">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="917e3-147">I/C - GB1234</span></span> |
| <span data-ttu-id="917e3-148">Rutineerstatning</span><span class="sxs-lookup"><span data-stu-id="917e3-148">Routine replacement</span></span>     | <span data-ttu-id="917e3-149">Time</span><span class="sxs-lookup"><span data-stu-id="917e3-149">Hour</span></span>             | <span data-ttu-id="917e3-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="917e3-150">GB-1234</span></span>        | <span data-ttu-id="917e3-151">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="917e3-151">RR - GB1234</span></span>  |
| <span data-ttu-id="917e3-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="917e3-152">GR-1</span></span>                    | <span data-ttu-id="917e3-153">Element</span><span class="sxs-lookup"><span data-stu-id="917e3-153">Item</span></span>             | <span data-ttu-id="917e3-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="917e3-154">GB-1234</span></span>        | <span data-ttu-id="917e3-155">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="917e3-155">RR - GB1234</span></span>  |
| <span data-ttu-id="917e3-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="917e3-156">GR-5</span></span>                    | <span data-ttu-id="917e3-157">Element</span><span class="sxs-lookup"><span data-stu-id="917e3-157">Item</span></span>             | <span data-ttu-id="917e3-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="917e3-158">GB-1234</span></span>        | <span data-ttu-id="917e3-159">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="917e3-159">RR - GB1234</span></span>  |

<span data-ttu-id="917e3-160">Serviceavtalelinjene for de to jobbene har to serviceoppgaver tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="917e3-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="917e3-161">Serviceoppgavene bestemmer hvilke transaksjoner som tilhører hver jobb.</span><span class="sxs-lookup"><span data-stu-id="917e3-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="917e3-162">I det første tilfellet identifiserer serviceoppgaven I/C - GB1234 alle serviceavtalelinjene i forbindelse med inspeksjonen og rengjøringen av objekt GB-1234.</span><span class="sxs-lookup"><span data-stu-id="917e3-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="917e3-163">I det andre tilfellet, identifiserer serviceoppgave RR - GB1234 alle serviceavtalelinjene i forbindelse med å fullføre en rutineerstatningsjobb.</span><span class="sxs-lookup"><span data-stu-id="917e3-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="917e3-164">Serviceoppgaverelasjonene som kobler serviceoppgavene til den bestemte avtalen, er som følger:</span><span class="sxs-lookup"><span data-stu-id="917e3-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="917e3-165">Serviceoppgaver</span><span class="sxs-lookup"><span data-stu-id="917e3-165">Service tasks</span></span>

| <span data-ttu-id="917e3-166">Serviceoppgave</span><span class="sxs-lookup"><span data-stu-id="917e3-166">Service task</span></span> | <span data-ttu-id="917e3-167">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="917e3-167">Description</span></span>                             | <span data-ttu-id="917e3-168">Intern merknad</span><span class="sxs-lookup"><span data-stu-id="917e3-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="917e3-169">Ekstern merknad</span><span class="sxs-lookup"><span data-stu-id="917e3-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="917e3-170">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="917e3-170">I/C - GB1234</span></span> | <span data-ttu-id="917e3-171">Inspeksjon av girkasse GB-1234</span><span class="sxs-lookup"><span data-stu-id="917e3-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="917e3-172">Visuell og mekanisk inspeksjon og rengjøring av girkasse GB-1234.</span><span class="sxs-lookup"><span data-stu-id="917e3-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="917e3-173">Rutineinspeksjon av girkasse</span><span class="sxs-lookup"><span data-stu-id="917e3-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="917e3-174">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="917e3-174">RR - GB1234</span></span>  | <span data-ttu-id="917e3-175">Rutineerstatning av deler i GB-1234</span><span class="sxs-lookup"><span data-stu-id="917e3-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="917e3-176">Rutineserviceerstatning av GR-1- og GR-5-komponenter (for girkasser som er produsert før 2002, erstatt også GR-2-komponenten)</span><span class="sxs-lookup"><span data-stu-id="917e3-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="917e3-177">Rutineerstatning av deler</span><span class="sxs-lookup"><span data-stu-id="917e3-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="917e3-178">Gruppeserviceordrer</span><span class="sxs-lookup"><span data-stu-id="917e3-178">Group service orders</span></span>

<span data-ttu-id="917e3-179">Når du oppretter serviceordrer automatisk, kan du bruke serviceoppgaver som et grupperingskriterium.</span><span class="sxs-lookup"><span data-stu-id="917e3-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="917e3-180">Hvis du vil gruppere serviceordrer etter serviceoppgaver, kan du på serviceavtalen definere at serviceordrer som er basert på serviceavtalen, skal grupperes etter serviceoppgave-ID-en som de første grupperingskriteriene.</span><span class="sxs-lookup"><span data-stu-id="917e3-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="917e3-181">**Gruppere etter serviceoppgave**</span><span class="sxs-lookup"><span data-stu-id="917e3-181">**Group by service task**</span></span>

1. <span data-ttu-id="917e3-182">Klikk **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**.</span><span class="sxs-lookup"><span data-stu-id="917e3-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="917e3-183">I kategorien **Oppsett** velger du **Etter serviceoppgave** i **Kombiner serviceordrer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="917e3-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>


