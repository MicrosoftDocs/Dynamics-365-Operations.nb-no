---
title: Opprette en arbeidscelle for underleveranse for lean manufacturing
description: For å modellere underleveransearbeidet for lean manufacturing må du opprette en arbeidscelle som er knyttet til leverandøren som har arbeidet.
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58b725af456f1a5c7f158f01ffe48a2d8cdf056b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550543"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="963aa-103">Opprette en arbeidscelle for underleveranse for lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="963aa-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="963aa-104">For å modellere underleveransearbeidet for lean manufacturing må du opprette en arbeidscelle som er knyttet til leverandøren som har arbeidet.</span><span class="sxs-lookup"><span data-stu-id="963aa-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="963aa-105">En arbeidscelle for underleveranse er knyttet til leverandøren via tilknytningen for en ressurs av typen leverandør.</span><span class="sxs-lookup"><span data-stu-id="963aa-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="963aa-106">Hvis du spiller dette opptaket i USMF-demofirmaet, kan du velge leverandørkonto ID 1002 og område 1.</span><span class="sxs-lookup"><span data-stu-id="963aa-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="963aa-107">Opprette en leverandørressurs</span><span class="sxs-lookup"><span data-stu-id="963aa-107">Create a vendor resource</span></span>
1. <span data-ttu-id="963aa-108">Gå til Ressurser.</span><span class="sxs-lookup"><span data-stu-id="963aa-108">Go to Resources.</span></span>
2. <span data-ttu-id="963aa-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="963aa-109">Click New.</span></span>
3. <span data-ttu-id="963aa-110">Skriv inn en verdi i Ressurs-feltet.</span><span class="sxs-lookup"><span data-stu-id="963aa-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="963aa-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="963aa-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="963aa-112">Velg 'Leverandør' i Type-feltet.</span><span class="sxs-lookup"><span data-stu-id="963aa-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="963aa-113">Klikk rullegardinknappen i feltet Leverandør for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="963aa-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="963aa-114">Opprette ressursgruppen</span><span class="sxs-lookup"><span data-stu-id="963aa-114">Create the resource group</span></span>
1. <span data-ttu-id="963aa-115">Gå til Ressursgrupper.</span><span class="sxs-lookup"><span data-stu-id="963aa-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="963aa-116">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="963aa-116">Click New.</span></span>
3. <span data-ttu-id="963aa-117">Skriv inn en verdi i Ressursgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="963aa-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="963aa-118">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="963aa-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="963aa-119">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="963aa-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="963aa-120">Velg området som arbeidscellen skal tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="963aa-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="963aa-121">I teorien kan et område representere ett enkelt område som styres av en leverandør.</span><span class="sxs-lookup"><span data-stu-id="963aa-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="963aa-122">Imidlertid tildeles i de fleste tilfeller underleveranseressurser bare til området som bestiller arbeidet fra underleverandøren.</span><span class="sxs-lookup"><span data-stu-id="963aa-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="963aa-123">Legg merke til at inngående og utgående lagre fra arbeidsceller til underleverandører må være i samme område.</span><span class="sxs-lookup"><span data-stu-id="963aa-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="963aa-124">Skriv inn en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="963aa-124">In the Site field, type a value.</span></span>
7. <span data-ttu-id="963aa-125">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="963aa-125">@SysTaskRecorder:_RequestClose</span></span>
8. <span data-ttu-id="963aa-126">Merk av eller fjern merket i avmerkingsboksen Arbeidscelle.</span><span class="sxs-lookup"><span data-stu-id="963aa-126">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="963aa-127">Klikk rullegardinknappen i feltet Innleveringslager for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="963aa-127">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="963aa-128">Velg lageret og lokasjonen som brukes til å klargjøre materialet for den leverandøradministrerte arbeidscellen.</span><span class="sxs-lookup"><span data-stu-id="963aa-128">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="963aa-129">Lager og lokasjon er utformet ved hjelp av et eget lager per leverandør og ett sted per arbeidscellen i mange tilfeller.</span><span class="sxs-lookup"><span data-stu-id="963aa-129">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="963aa-130">Klikk rullegardinknappen i feltet Innleveringssted for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="963aa-130">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="963aa-131">Klikk rullegardinknappen i feltet Utleveringslager for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="963aa-131">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="963aa-132">Definer lager og lokasjonen der materialet posteres ved postering av aktiviteter i underleveranser for arbeidscellen.</span><span class="sxs-lookup"><span data-stu-id="963aa-132">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="963aa-133">Lager og lokasjon kan være på leverandørområdet for hvis leverandøren rapporterer kanban-jobbene.</span><span class="sxs-lookup"><span data-stu-id="963aa-133">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="963aa-134">Lager og lokasjon kan også være mottar plasseringen som er knyttet til det neste trinnet i produksjonsflyten.</span><span class="sxs-lookup"><span data-stu-id="963aa-134">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="963aa-135">Klikk rullegardinknappen i feltet Utleveringssted for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="963aa-135">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="963aa-136">Vis eller skjul delen Kalendere.</span><span class="sxs-lookup"><span data-stu-id="963aa-136">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="963aa-137">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="963aa-137">Click Add.</span></span>
15. <span data-ttu-id="963aa-138">Klikk rullegardinknappen i Kalender-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="963aa-138">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="963aa-139">Tilknytt arbeidstidskalenderen for arbeidscellen til ressursgruppen.</span><span class="sxs-lookup"><span data-stu-id="963aa-139">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="963aa-140">For kritiske ressurser anbefaler vi at du definerer bestemte kalendere som representerer nøyaktig arbeidstidene og tilknyttede kapasitet på webområdet arbeid cellen eller leverandør.</span><span class="sxs-lookup"><span data-stu-id="963aa-140">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="963aa-141">Vis eller skjul delen Ressurser.</span><span class="sxs-lookup"><span data-stu-id="963aa-141">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="963aa-142">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="963aa-142">Click Add.</span></span>
    * <span data-ttu-id="963aa-143">En ressursgruppe for underleveranse må ha en tilknyttet ressurs av typen Leverandør, som kobler ressursgruppen til kundens leverandørkonto.</span><span class="sxs-lookup"><span data-stu-id="963aa-143">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="963aa-144">Klikk rullegardinknappen i feltet Ressurser for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="963aa-144">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="963aa-145">Velg eller angi leverandørressursen som du opprettet i den forrige delaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="963aa-145">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="963aa-146">Vis eller skjul delen Arbeidscellekapasitet.</span><span class="sxs-lookup"><span data-stu-id="963aa-146">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="963aa-147">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="963aa-147">Click Add.</span></span>
    * <span data-ttu-id="963aa-148">En arbeidscelle må ha en definert kapasitet.</span><span class="sxs-lookup"><span data-stu-id="963aa-148">A work cell must have a defined capacity.</span></span> <span data-ttu-id="963aa-149">I dette eksemplet oppretter vi en gjennomstrømningskapasitet på 100 enheter per standard arbeidsdag.</span><span class="sxs-lookup"><span data-stu-id="963aa-149">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="963aa-150">Klikk rullegardinknappen i feltet Produksjonsflytmodell for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="963aa-150">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="963aa-151">Velg et alternativ i Kapasitetsperiode-feltet.</span><span class="sxs-lookup"><span data-stu-id="963aa-151">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="963aa-152">Angi et nummer i feltet Gjennomsnittlig gjennomstrømningsantall.</span><span class="sxs-lookup"><span data-stu-id="963aa-152">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="963aa-153">Klikk rullegardinknappen i feltet Enhet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="963aa-153">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="963aa-154">ResolveChanges enheten.</span><span class="sxs-lookup"><span data-stu-id="963aa-154">ResolveChanges the Unit.</span></span>

