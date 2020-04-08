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
ms.openlocfilehash: 03fcc62236b14a8721a4cb611978e8672ae77ea3
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146934"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="ef641-103">Opprette en arbeidscelle for underleveranse for lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="ef641-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ef641-104">For å modellere underleveransearbeidet for lean manufacturing må du opprette en arbeidscelle som er knyttet til leverandøren som har arbeidet.</span><span class="sxs-lookup"><span data-stu-id="ef641-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="ef641-105">En arbeidscelle for underleveranse er knyttet til leverandøren via tilknytningen for en ressurs av typen leverandør.</span><span class="sxs-lookup"><span data-stu-id="ef641-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="ef641-106">Hvis du spiller dette opptaket i USMF-demofirmaet, kan du velge leverandørkonto ID 1002 og område 1.</span><span class="sxs-lookup"><span data-stu-id="ef641-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="ef641-107">Opprette en leverandørressurs</span><span class="sxs-lookup"><span data-stu-id="ef641-107">Create a vendor resource</span></span>
1. <span data-ttu-id="ef641-108">Gå til Ressurser.</span><span class="sxs-lookup"><span data-stu-id="ef641-108">Go to Resources.</span></span>
2. <span data-ttu-id="ef641-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ef641-109">Click New.</span></span>
3. <span data-ttu-id="ef641-110">Skriv inn en verdi i Ressurs-feltet.</span><span class="sxs-lookup"><span data-stu-id="ef641-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="ef641-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ef641-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ef641-112">Velg 'Leverandør' i Type-feltet.</span><span class="sxs-lookup"><span data-stu-id="ef641-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="ef641-113">Klikk rullegardinknappen i feltet Leverandør for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef641-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="ef641-114">Opprette ressursgruppen</span><span class="sxs-lookup"><span data-stu-id="ef641-114">Create the resource group</span></span>
1. <span data-ttu-id="ef641-115">Gå til Ressursgrupper.</span><span class="sxs-lookup"><span data-stu-id="ef641-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="ef641-116">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ef641-116">Click New.</span></span>
3. <span data-ttu-id="ef641-117">Skriv inn en verdi i Ressursgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="ef641-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="ef641-118">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ef641-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ef641-119">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef641-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ef641-120">Velg området som arbeidscellen skal tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="ef641-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="ef641-121">I teorien kan et område representere ett enkelt område som styres av en leverandør.</span><span class="sxs-lookup"><span data-stu-id="ef641-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="ef641-122">Imidlertid tildeles i de fleste tilfeller underleveranseressurser bare til området som bestiller arbeidet fra underleverandøren.</span><span class="sxs-lookup"><span data-stu-id="ef641-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="ef641-123">Legg merke til at inngående og utgående lagre fra arbeidsceller til underleverandører må være i samme område.</span><span class="sxs-lookup"><span data-stu-id="ef641-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="ef641-124">Skriv inn en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="ef641-124">In the Site field, type a value.</span></span>
7. <span data-ttu-id="ef641-125">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="ef641-125">@SysTaskRecorder:_RequestClose</span></span>
8. <span data-ttu-id="ef641-126">Merk av eller fjern merket i avmerkingsboksen Arbeidscelle.</span><span class="sxs-lookup"><span data-stu-id="ef641-126">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="ef641-127">Klikk rullegardinknappen i feltet Innleveringslager for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef641-127">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ef641-128">Velg lageret og lokasjonen som brukes til å klargjøre materialet for den leverandøradministrerte arbeidscellen.</span><span class="sxs-lookup"><span data-stu-id="ef641-128">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="ef641-129">Lager og lokasjon er utformet ved hjelp av et eget lager per leverandør og ett sted per arbeidscellen i mange tilfeller.</span><span class="sxs-lookup"><span data-stu-id="ef641-129">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="ef641-130">Klikk rullegardinknappen i feltet Innleveringssted for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef641-130">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="ef641-131">Klikk rullegardinknappen i feltet Utleveringslager for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef641-131">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ef641-132">Definer lager og lokasjonen der materialet posteres ved postering av aktiviteter i underleveranser for arbeidscellen.</span><span class="sxs-lookup"><span data-stu-id="ef641-132">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="ef641-133">Lager og lokasjon kan være på leverandørområdet for hvis leverandøren rapporterer kanban-jobbene.</span><span class="sxs-lookup"><span data-stu-id="ef641-133">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="ef641-134">Lager og lokasjon kan også være mottar plasseringen som er knyttet til det neste trinnet i produksjonsflyten.</span><span class="sxs-lookup"><span data-stu-id="ef641-134">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="ef641-135">Klikk rullegardinknappen i feltet Utleveringssted for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef641-135">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="ef641-136">Vis eller skjul delen Kalendere.</span><span class="sxs-lookup"><span data-stu-id="ef641-136">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="ef641-137">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ef641-137">Click Add.</span></span>
15. <span data-ttu-id="ef641-138">Klikk rullegardinknappen i Kalender-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef641-138">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ef641-139">Tilknytt arbeidstidskalenderen for arbeidscellen til ressursgruppen.</span><span class="sxs-lookup"><span data-stu-id="ef641-139">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="ef641-140">For kritiske ressurser anbefaler vi at du definerer bestemte kalendere som representerer nøyaktig arbeidstidene og tilknyttede kapasitet på webområdet arbeid cellen eller leverandør.</span><span class="sxs-lookup"><span data-stu-id="ef641-140">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="ef641-141">Vis eller skjul delen Ressurser.</span><span class="sxs-lookup"><span data-stu-id="ef641-141">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="ef641-142">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ef641-142">Click Add.</span></span>
    * <span data-ttu-id="ef641-143">En ressursgruppe for underleveranse må ha en tilknyttet ressurs av typen Leverandør, som kobler ressursgruppen til kundens leverandørkonto.</span><span class="sxs-lookup"><span data-stu-id="ef641-143">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="ef641-144">Klikk rullegardinknappen i feltet Ressurser for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef641-144">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ef641-145">Velg eller angi leverandørressursen som du opprettet i den forrige delaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="ef641-145">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="ef641-146">Vis eller skjul delen Arbeidscellekapasitet.</span><span class="sxs-lookup"><span data-stu-id="ef641-146">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="ef641-147">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ef641-147">Click Add.</span></span>
    * <span data-ttu-id="ef641-148">En arbeidscelle må ha en definert kapasitet.</span><span class="sxs-lookup"><span data-stu-id="ef641-148">A work cell must have a defined capacity.</span></span> <span data-ttu-id="ef641-149">I dette eksemplet oppretter vi en gjennomstrømningskapasitet på 100 enheter per standard arbeidsdag.</span><span class="sxs-lookup"><span data-stu-id="ef641-149">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="ef641-150">Klikk rullegardinknappen i feltet Produksjonsflytmodell for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef641-150">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="ef641-151">Velg et alternativ i Kapasitetsperiode-feltet.</span><span class="sxs-lookup"><span data-stu-id="ef641-151">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="ef641-152">Angi et nummer i feltet Gjennomsnittlig gjennomstrømningsantall.</span><span class="sxs-lookup"><span data-stu-id="ef641-152">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="ef641-153">Klikk rullegardinknappen i feltet Enhet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ef641-153">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="ef641-154">ResolveChanges enheten.</span><span class="sxs-lookup"><span data-stu-id="ef641-154">ResolveChanges the Unit.</span></span>

