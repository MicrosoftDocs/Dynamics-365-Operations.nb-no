--- 
title: "Opprette overføringsaktiviteter for lean manufacturing"
description: "Opprett en overføringsaktivitet for lean manufacturing."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e5f28b26cee2501f1294cd34a495ee925e6b1ba8
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="c5712-103">Opprette overføringsaktiviteter for lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="c5712-103">Create transfer activities for lean manufacturing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5712-104">Opprett en overføringsaktivitet for lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="c5712-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="c5712-105">Forutsetninger:</span><span class="sxs-lookup"><span data-stu-id="c5712-105">Prerequisites:</span></span> 

1. <span data-ttu-id="c5712-106">En produksjonsflyt og versjon som ikke er aktiv, må opprettes.</span><span class="sxs-lookup"><span data-stu-id="c5712-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="c5712-107">Fra- og Til- lager og -lokasjoner må opprettes.</span><span class="sxs-lookup"><span data-stu-id="c5712-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="c5712-108">Arbeidscellen som skal etterfylles eller som er etterfylt, kan eventuelt opprettes.</span><span class="sxs-lookup"><span data-stu-id="c5712-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="c5712-109">Finne produksjonsflytversjonen</span><span class="sxs-lookup"><span data-stu-id="c5712-109">Find the production flow version</span></span>
1. <span data-ttu-id="c5712-110">Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.</span><span class="sxs-lookup"><span data-stu-id="c5712-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="c5712-111">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="c5712-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c5712-112">Legg merke til at produksjonsflyten må ha en versjon i utkaststatus.</span><span class="sxs-lookup"><span data-stu-id="c5712-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="c5712-113">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c5712-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="c5712-114">Opprette en ny aktivitet</span><span class="sxs-lookup"><span data-stu-id="c5712-114">Create a new activity</span></span>
1. <span data-ttu-id="c5712-115">Klikk Aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="c5712-115">Click Activities.</span></span>
    * <span data-ttu-id="c5712-116">Kontroller at den valgte produksjonsflyten har en versjon i utkast, og velg den versjonen.</span><span class="sxs-lookup"><span data-stu-id="c5712-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="c5712-117">Klikk Opprett ny planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="c5712-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="c5712-118">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="c5712-118">Click Next.</span></span>
4. <span data-ttu-id="c5712-119">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="c5712-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c5712-120">Velg Overføring i Aktivitetstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="c5712-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="c5712-121">Angi et tall i feltet Prosessantall.</span><span class="sxs-lookup"><span data-stu-id="c5712-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="c5712-122">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="c5712-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="c5712-123">Velge arbeidscellene</span><span class="sxs-lookup"><span data-stu-id="c5712-123">Select the Work cells</span></span>
1. <span data-ttu-id="c5712-124">Klikk rullegardinknappen i feltet Etterfyller for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="c5712-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c5712-125">Når du skal bruke utleveringsstedet for arbeidscellen som fra-lokasjon i overføringsaktiviteten, velger du en arbeidscelle.</span><span class="sxs-lookup"><span data-stu-id="c5712-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="c5712-126">Det samme kan gjøres med den etterfylte arbeidscellen, som angir mållokasjonen for overføringsaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="c5712-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="c5712-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c5712-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="c5712-128">Definere beholdningsoppdateringene</span><span class="sxs-lookup"><span data-stu-id="c5712-128">Define the inventory updates</span></span>
1. <span data-ttu-id="c5712-129">Velg et alternativ i Produkttype-feltet.</span><span class="sxs-lookup"><span data-stu-id="c5712-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="c5712-130">Legg merke til at en overføring ikke endrer typen produkt.</span><span class="sxs-lookup"><span data-stu-id="c5712-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="c5712-131">Du kan overføre ferdige produkter eller halvfabrikata (overføring mellom to aktiviteter i en produksjonsflyt og eventuelt en kanban-flyt).</span><span class="sxs-lookup"><span data-stu-id="c5712-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="c5712-132">Når du overfører ferdige produkter, kan du velge om plukking eller mottak resulterer i en lagertransaksjon.</span><span class="sxs-lookup"><span data-stu-id="c5712-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="c5712-133">Definere overføringslokasjonene</span><span class="sxs-lookup"><span data-stu-id="c5712-133">Define the transfer locations</span></span>
1. <span data-ttu-id="c5712-134">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="c5712-134">Click Next.</span></span>
2. <span data-ttu-id="c5712-135">Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="c5712-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c5712-136">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="c5712-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="c5712-137">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c5712-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c5712-138">Klikk rullegardinknappen i Lokasjon-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="c5712-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c5712-139">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c5712-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="c5712-140">I Fraktet av-feltet velger du "Speditør".</span><span class="sxs-lookup"><span data-stu-id="c5712-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="c5712-141">Alternativene omfatter: Speditør - organisasjonen betjener forsendelseslageret, Mottaker - organisasjonen betjener mottakslageret, Transportør - en tredjepartsleverandør.</span><span class="sxs-lookup"><span data-stu-id="c5712-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="c5712-142">Hvis driftsorganisasjonen en leverandør, krever overføringsaktiviteten en utsettingsavtale.</span><span class="sxs-lookup"><span data-stu-id="c5712-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="c5712-143">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="c5712-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="c5712-144">Definere aktivitetstidene</span><span class="sxs-lookup"><span data-stu-id="c5712-144">Define the activity times</span></span>
1. <span data-ttu-id="c5712-145">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="c5712-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c5712-146">Definisjonen av en kjøretid er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="c5712-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="c5712-147">Kjøretiden brukes til å beregne kostnad og produksjonstidene for kanban-jobber.</span><span class="sxs-lookup"><span data-stu-id="c5712-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="c5712-148">Kjøretider brukes ikke til å beregne kapasitetsbelastning og forbruk, som beregnes fra syklustid, som er avledet fra oppgaven for produksjonsflytversjonen.</span><span class="sxs-lookup"><span data-stu-id="c5712-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="c5712-149">Angi et tall i feltet Tid.</span><span class="sxs-lookup"><span data-stu-id="c5712-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="c5712-150">Skriv inn en verdi i feltet Enhet.</span><span class="sxs-lookup"><span data-stu-id="c5712-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="c5712-151">Velg tidsenheten.</span><span class="sxs-lookup"><span data-stu-id="c5712-151">Select the Time unit.</span></span>
5. <span data-ttu-id="c5712-152">Angi et tall i feltet Per antall.</span><span class="sxs-lookup"><span data-stu-id="c5712-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="c5712-153">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="c5712-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c5712-154">Køtider er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="c5712-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="c5712-155">Angi et tall i feltet Tid.</span><span class="sxs-lookup"><span data-stu-id="c5712-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="c5712-156">Skriv inn en verdi i feltet Enhet.</span><span class="sxs-lookup"><span data-stu-id="c5712-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="c5712-157">Velg tidsenheten.</span><span class="sxs-lookup"><span data-stu-id="c5712-157">Select the Time unit.</span></span>
10. <span data-ttu-id="c5712-158">Angi et tall i feltet Per antall.</span><span class="sxs-lookup"><span data-stu-id="c5712-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="c5712-159">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="c5712-159">Click Next.</span></span>
12. <span data-ttu-id="c5712-160">Klikk Finish.</span><span class="sxs-lookup"><span data-stu-id="c5712-160">Click Finish.</span></span>
13. <span data-ttu-id="c5712-161">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c5712-161">Close the page.</span></span>


