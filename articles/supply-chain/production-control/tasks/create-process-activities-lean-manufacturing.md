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
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bd505446456791b26850d676722b6676b50dca4b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981212"
---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="d99dc-103">Opprette prosessaktiviteter for lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="d99dc-103">Create process activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d99dc-104">Opprett en prosessaktivitet for lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="d99dc-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="d99dc-105">Forutsetninger:</span><span class="sxs-lookup"><span data-stu-id="d99dc-105">Prerequisites:</span></span> 

1. <span data-ttu-id="d99dc-106">En produksjonsflyt og versjon som ikke er aktiv, må opprettes.</span><span class="sxs-lookup"><span data-stu-id="d99dc-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="d99dc-107">En arbeidscelle må opprettes.</span><span class="sxs-lookup"><span data-stu-id="d99dc-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="d99dc-108">Finne produksjonsflytversjonen</span><span class="sxs-lookup"><span data-stu-id="d99dc-108">Find the production flow version</span></span>
1. <span data-ttu-id="d99dc-109">Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.</span><span class="sxs-lookup"><span data-stu-id="d99dc-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="d99dc-110">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d99dc-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d99dc-111">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d99dc-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="d99dc-112">Opprette en ny aktivitet</span><span class="sxs-lookup"><span data-stu-id="d99dc-112">Create a new activity</span></span>
1. <span data-ttu-id="d99dc-113">Klikk på Aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="d99dc-113">Click Activities.</span></span>
    * <span data-ttu-id="d99dc-114">Kontroller at den valgte produksjonsflyten har en versjon i utkast, og velg den versjonen.</span><span class="sxs-lookup"><span data-stu-id="d99dc-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="d99dc-115">Klikk på Opprett ny planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="d99dc-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="d99dc-116">Klikk på Neste.</span><span class="sxs-lookup"><span data-stu-id="d99dc-116">Click Next.</span></span>
4. <span data-ttu-id="d99dc-117">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d99dc-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d99dc-118">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d99dc-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d99dc-119">Legg merke til at navnet må være unikt for en gitt produksjonsflyt for alle versjoner.</span><span class="sxs-lookup"><span data-stu-id="d99dc-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="d99dc-120">Angi et tall i feltet Prosessantall.</span><span class="sxs-lookup"><span data-stu-id="d99dc-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="d99dc-121">Vær oppmerksom på at uansett hvilket jobbantall som blir behandlet, er dette det minste antallet per jobb for å beregne kostnaden for arbeid.</span><span class="sxs-lookup"><span data-stu-id="d99dc-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="d99dc-122">Hvis jobbantall avviker fra dette antallet, vil arbeidskostnadsavvik opprettes.</span><span class="sxs-lookup"><span data-stu-id="d99dc-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="d99dc-123">Klikk på Neste.</span><span class="sxs-lookup"><span data-stu-id="d99dc-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="d99dc-124">Velge arbeidscellen</span><span class="sxs-lookup"><span data-stu-id="d99dc-124">Select the work cell</span></span>
1. <span data-ttu-id="d99dc-125">Klikk på rullegardinknappen i Arbeidscelle-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d99dc-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="d99dc-126">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d99dc-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="d99dc-127">Definere beholdningsoppdateringene</span><span class="sxs-lookup"><span data-stu-id="d99dc-127">Define the inventory updates</span></span>
1. <span data-ttu-id="d99dc-128">Merk av eller fjern merket i boksen Oppdater beholdningsmottak.</span><span class="sxs-lookup"><span data-stu-id="d99dc-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="d99dc-129">Hvis Oppdater beholdning = Nei, kan du definere aktiviteten for å motta et halvfabrikata (aktiviteten når ikke det neste nivået i stykklisten).</span><span class="sxs-lookup"><span data-stu-id="d99dc-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="d99dc-130">Du kan også velge å bruke halvfabrikata.</span><span class="sxs-lookup"><span data-stu-id="d99dc-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="d99dc-131">Definere plukkaktivitetene</span><span class="sxs-lookup"><span data-stu-id="d99dc-131">Define the picking activities</span></span>
1. <span data-ttu-id="d99dc-132">Klikk på Neste.</span><span class="sxs-lookup"><span data-stu-id="d99dc-132">Click Next.</span></span>
2. <span data-ttu-id="d99dc-133">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d99dc-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d99dc-134">En standard plukkaktivitet opprettes for innleveringsstedet for den valgte arbeidscellen.</span><span class="sxs-lookup"><span data-stu-id="d99dc-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="d99dc-135">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="d99dc-135">Click Add.</span></span>
    * <span data-ttu-id="d99dc-136">Du kan opprette flere plukkaktivitetene for bestemte produkter, som ikke er oppsamlet på innleveringsaktiviteten for arbeidscellen.</span><span class="sxs-lookup"><span data-stu-id="d99dc-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="d99dc-137">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d99dc-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d99dc-138">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="d99dc-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="d99dc-139">Klikk på rullegardinknappen i Lager-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d99dc-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d99dc-140">Med denne definisjonen plukkes alt materiale som forbrukes i aktiviteten fra standard innleveringslager og -lokasjon, med unntak av varen som er definert i den andre plukkaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="d99dc-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="d99dc-141">Denne varen plukkes fra et annet lager og en annen lokasjon.</span><span class="sxs-lookup"><span data-stu-id="d99dc-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="d99dc-142">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d99dc-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="d99dc-143">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d99dc-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d99dc-144">Merk av eller fjern merket i boksen Registrer svinn.</span><span class="sxs-lookup"><span data-stu-id="d99dc-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="d99dc-145">Klikk på Neste.</span><span class="sxs-lookup"><span data-stu-id="d99dc-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="d99dc-146">Definere aktivitetstidene</span><span class="sxs-lookup"><span data-stu-id="d99dc-146">Define the activity times</span></span>
1. <span data-ttu-id="d99dc-147">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d99dc-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d99dc-148">Definisjonen av en kjøretid er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="d99dc-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="d99dc-149">Kjøretiden brukes til å beregne kostnad og produksjonstidene for kanban-jobber.</span><span class="sxs-lookup"><span data-stu-id="d99dc-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="d99dc-150">Kjøretider brukes ikke til å beregne kapasitetsbelastning og forbruk, som beregnes fra syklustid, som er avledet fra oppgaven for produksjonsflytversjonen.</span><span class="sxs-lookup"><span data-stu-id="d99dc-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="d99dc-151">Angi et tall i feltet Tid.</span><span class="sxs-lookup"><span data-stu-id="d99dc-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="d99dc-152">Skriv inn en verdi i feltet Enhet.</span><span class="sxs-lookup"><span data-stu-id="d99dc-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="d99dc-153">Velg tidsenheten.</span><span class="sxs-lookup"><span data-stu-id="d99dc-153">Select the Time unit.</span></span>
5. <span data-ttu-id="d99dc-154">Angi et tall i feltet Per antall.</span><span class="sxs-lookup"><span data-stu-id="d99dc-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="d99dc-155">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d99dc-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d99dc-156">Køtider er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="d99dc-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="d99dc-157">Angi et tall i feltet Tid.</span><span class="sxs-lookup"><span data-stu-id="d99dc-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="d99dc-158">Skriv inn en verdi i feltet Enhet.</span><span class="sxs-lookup"><span data-stu-id="d99dc-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="d99dc-159">Velg tidsenheten.</span><span class="sxs-lookup"><span data-stu-id="d99dc-159">Select the Time unit.</span></span>
10. <span data-ttu-id="d99dc-160">Angi et tall i feltet Per antall.</span><span class="sxs-lookup"><span data-stu-id="d99dc-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="d99dc-161">Klikk på Neste.</span><span class="sxs-lookup"><span data-stu-id="d99dc-161">Click Next.</span></span>
12. <span data-ttu-id="d99dc-162">Klikk på Finish.</span><span class="sxs-lookup"><span data-stu-id="d99dc-162">Click Finish.</span></span>
13. <span data-ttu-id="d99dc-163">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d99dc-163">Close the page.</span></span>

