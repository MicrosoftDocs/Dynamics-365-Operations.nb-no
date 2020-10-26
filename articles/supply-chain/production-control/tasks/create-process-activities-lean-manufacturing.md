---
title: Opprette prosessaktiviteter for lean manufacturing
description: Opprett en prosessaktivitet for lean manufacturing.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup, PlanActivityDetails, KanbanJobPickingListPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3cb096eb25fa449b521c370bcb1677e38e399658
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983404"
---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="4f305-103">Opprette prosessaktiviteter for lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="4f305-103">Create process activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4f305-104">Opprett en prosessaktivitet for lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="4f305-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="4f305-105">Forutsetninger:</span><span class="sxs-lookup"><span data-stu-id="4f305-105">Prerequisites:</span></span> 

1. <span data-ttu-id="4f305-106">En produksjonsflyt og versjon som ikke er aktiv, må opprettes.</span><span class="sxs-lookup"><span data-stu-id="4f305-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="4f305-107">En arbeidscelle må opprettes.</span><span class="sxs-lookup"><span data-stu-id="4f305-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="4f305-108">Finne produksjonsflytversjonen</span><span class="sxs-lookup"><span data-stu-id="4f305-108">Find the production flow version</span></span>
1. <span data-ttu-id="4f305-109">Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.</span><span class="sxs-lookup"><span data-stu-id="4f305-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="4f305-110">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4f305-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="4f305-111">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4f305-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="4f305-112">Opprette en ny aktivitet</span><span class="sxs-lookup"><span data-stu-id="4f305-112">Create a new activity</span></span>
1. <span data-ttu-id="4f305-113">Klikk Aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="4f305-113">Click Activities.</span></span>
    * <span data-ttu-id="4f305-114">Kontroller at den valgte produksjonsflyten har en versjon i utkast, og velg den versjonen.</span><span class="sxs-lookup"><span data-stu-id="4f305-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="4f305-115">Klikk Opprett ny planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="4f305-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="4f305-116">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="4f305-116">Click Next.</span></span>
4. <span data-ttu-id="4f305-117">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4f305-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="4f305-118">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4f305-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="4f305-119">Legg merke til at navnet må være unikt for en gitt produksjonsflyt for alle versjoner.</span><span class="sxs-lookup"><span data-stu-id="4f305-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="4f305-120">Angi et tall i feltet Prosessantall.</span><span class="sxs-lookup"><span data-stu-id="4f305-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="4f305-121">Vær oppmerksom på at uansett hvilket jobbantall som blir behandlet, er dette det minste antallet per jobb for å beregne kostnaden for arbeid.</span><span class="sxs-lookup"><span data-stu-id="4f305-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="4f305-122">Hvis jobbantall avviker fra dette antallet, vil arbeidskostnadsavvik opprettes.</span><span class="sxs-lookup"><span data-stu-id="4f305-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="4f305-123">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="4f305-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="4f305-124">Velge arbeidscellen</span><span class="sxs-lookup"><span data-stu-id="4f305-124">Select the work cell</span></span>
1. <span data-ttu-id="4f305-125">Klikk rullegardinknappen i Arbeidscelle-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4f305-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="4f305-126">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4f305-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="4f305-127">Definere beholdningsoppdateringene</span><span class="sxs-lookup"><span data-stu-id="4f305-127">Define the inventory updates</span></span>
1. <span data-ttu-id="4f305-128">Merk av eller fjern merket i boksen Oppdater beholdningsmottak.</span><span class="sxs-lookup"><span data-stu-id="4f305-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="4f305-129">Hvis Oppdater beholdning = Nei, kan du definere aktiviteten for å motta et halvfabrikata (aktiviteten når ikke det neste nivået i stykklisten).</span><span class="sxs-lookup"><span data-stu-id="4f305-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="4f305-130">Du kan også velge å bruke halvfabrikata.</span><span class="sxs-lookup"><span data-stu-id="4f305-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="4f305-131">Definere plukkaktivitetene</span><span class="sxs-lookup"><span data-stu-id="4f305-131">Define the picking activities</span></span>
1. <span data-ttu-id="4f305-132">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="4f305-132">Click Next.</span></span>
2. <span data-ttu-id="4f305-133">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4f305-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4f305-134">En standard plukkaktivitet opprettes for innleveringsstedet for den valgte arbeidscellen.</span><span class="sxs-lookup"><span data-stu-id="4f305-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="4f305-135">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4f305-135">Click Add.</span></span>
    * <span data-ttu-id="4f305-136">Du kan opprette flere plukkaktivitetene for bestemte produkter, som ikke er oppsamlet på innleveringsaktiviteten for arbeidscellen.</span><span class="sxs-lookup"><span data-stu-id="4f305-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="4f305-137">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4f305-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="4f305-138">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="4f305-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="4f305-139">Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4f305-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4f305-140">Med denne definisjonen plukkes alt materiale som forbrukes i aktiviteten fra standard innleveringslager og -lokasjon, med unntak av varen som er definert i den andre plukkaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="4f305-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="4f305-141">Denne varen plukkes fra et annet lager og en annen lokasjon.</span><span class="sxs-lookup"><span data-stu-id="4f305-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="4f305-142">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4f305-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="4f305-143">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4f305-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="4f305-144">Merk av eller fjern merket i boksen Registrer svinn.</span><span class="sxs-lookup"><span data-stu-id="4f305-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="4f305-145">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="4f305-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="4f305-146">Definere aktivitetstidene</span><span class="sxs-lookup"><span data-stu-id="4f305-146">Define the activity times</span></span>
1. <span data-ttu-id="4f305-147">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4f305-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4f305-148">Definisjonen av en kjøretid er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="4f305-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="4f305-149">Kjøretiden brukes til å beregne kostnad og produksjonstidene for kanban-jobber.</span><span class="sxs-lookup"><span data-stu-id="4f305-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="4f305-150">Kjøretider brukes ikke til å beregne kapasitetsbelastning og forbruk, som beregnes fra syklustid, som er avledet fra oppgaven for produksjonsflytversjonen.</span><span class="sxs-lookup"><span data-stu-id="4f305-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="4f305-151">Angi et tall i feltet Tid.</span><span class="sxs-lookup"><span data-stu-id="4f305-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="4f305-152">Skriv inn en verdi i feltet Enhet.</span><span class="sxs-lookup"><span data-stu-id="4f305-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="4f305-153">Velg tidsenheten.</span><span class="sxs-lookup"><span data-stu-id="4f305-153">Select the Time unit.</span></span>
5. <span data-ttu-id="4f305-154">Angi et tall i feltet Per antall.</span><span class="sxs-lookup"><span data-stu-id="4f305-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="4f305-155">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4f305-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4f305-156">Køtider er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="4f305-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="4f305-157">Angi et tall i feltet Tid.</span><span class="sxs-lookup"><span data-stu-id="4f305-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="4f305-158">Skriv inn en verdi i feltet Enhet.</span><span class="sxs-lookup"><span data-stu-id="4f305-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="4f305-159">Velg tidsenheten.</span><span class="sxs-lookup"><span data-stu-id="4f305-159">Select the Time unit.</span></span>
10. <span data-ttu-id="4f305-160">Angi et tall i feltet Per antall.</span><span class="sxs-lookup"><span data-stu-id="4f305-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="4f305-161">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="4f305-161">Click Next.</span></span>
12. <span data-ttu-id="4f305-162">Klikk Finish.</span><span class="sxs-lookup"><span data-stu-id="4f305-162">Click Finish.</span></span>
13. <span data-ttu-id="4f305-163">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4f305-163">Close the page.</span></span>

