--- 
title: Opprette en Kanban-regel med fast antall for produksjon
description: "Denne prosedyren fokuserer på oppsettet som kreves for å opprette en Kanban-regel for fast produksjon for utløsing av transformasjonsaktiviteter, på en arbeidscelle, i et lean-miljø."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 555d79e8bacbae0287472e68701a04a3c1d635aa
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a><span data-ttu-id="1da6f-103">Opprette en Kanban-regel med fast antall for produksjon</span><span class="sxs-lookup"><span data-stu-id="1da6f-103">Create a fixed quantity kanban rule for manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1da6f-104">Denne prosedyren fokuserer på oppsettet som kreves for å opprette en Kanban-regel for fast produksjon for utløsing av transformasjonsaktiviteter, på en arbeidscelle, i et lean-miljø.</span><span class="sxs-lookup"><span data-stu-id="1da6f-104">This procedure focuses on the setup needed to create a fixed manufacturing kanban rule for triggering transforming activities, at a work cell, in a lean environment.</span></span> <span data-ttu-id="1da6f-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="1da6f-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="1da6f-106">Denne fremgangsmåten er ment for prosessingeniøren eller verdistrømlederen, når de klargjør produksjon av et nytt eller endret produkt.</span><span class="sxs-lookup"><span data-stu-id="1da6f-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="1da6f-107">Opprette ny Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="1da6f-107">Create new kanban rule</span></span>
1. <span data-ttu-id="1da6f-108">Gå til Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="1da6f-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="1da6f-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="1da6f-109">Click New.</span></span>
    * <span data-ttu-id="1da6f-110">Legg merke til at standardtype er Produksjon, og etterfyllingsstrategi er Fast.</span><span class="sxs-lookup"><span data-stu-id="1da6f-110">Notice that the default Type is Manufacturing and Replenishment strategy is Fixed.</span></span> <span data-ttu-id="1da6f-111">Du trenger ikke å endre disse parameterne.</span><span class="sxs-lookup"><span data-stu-id="1da6f-111">You do not have to change these parameters.</span></span>  
3. <span data-ttu-id="1da6f-112">Angi eller velg en verdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="1da6f-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="1da6f-113">Dette er aktiviteten som skal utføres for Kanbaner opprettet basert på denne kanban-regelen.</span><span class="sxs-lookup"><span data-stu-id="1da6f-113">This is the activity that will be performed for kanbans created based on this kanban rule.</span></span>  <span data-ttu-id="1da6f-114">Velg "SpeakerTestAndPackaging".</span><span class="sxs-lookup"><span data-stu-id="1da6f-114">Select 'SpeakerTestAndPackaging'.</span></span>  
4. <span data-ttu-id="1da6f-115">Vis delen Detaljer.</span><span class="sxs-lookup"><span data-stu-id="1da6f-115">Expand the Details section.</span></span>
5. <span data-ttu-id="1da6f-116">Angi eller velg en verdi i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="1da6f-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="1da6f-117">Velg L0050.</span><span class="sxs-lookup"><span data-stu-id="1da6f-117">Select L0050.</span></span>  
6. <span data-ttu-id="1da6f-118">I Måleenhet-feltet angir eller velger du en verdi.</span><span class="sxs-lookup"><span data-stu-id="1da6f-118">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="1da6f-119">Velg minutter.</span><span class="sxs-lookup"><span data-stu-id="1da6f-119">Select minutes.</span></span>  
7. <span data-ttu-id="1da6f-120">Angi et tall i feltet Leveringstid.</span><span class="sxs-lookup"><span data-stu-id="1da6f-120">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="1da6f-121">Angi 5.</span><span class="sxs-lookup"><span data-stu-id="1da6f-121">Enter 5.</span></span>  

## <a name="set-quantities"></a><span data-ttu-id="1da6f-122">Angi antall</span><span class="sxs-lookup"><span data-stu-id="1da6f-122">Set quantities</span></span>
1. <span data-ttu-id="1da6f-123">Utvid delen Antall.</span><span class="sxs-lookup"><span data-stu-id="1da6f-123">Expand the Quantities section.</span></span>
2. <span data-ttu-id="1da6f-124">Angi Standardantall som 10.</span><span class="sxs-lookup"><span data-stu-id="1da6f-124">Set Default quantity to '10'.</span></span>
    * <span data-ttu-id="1da6f-125">Dette er antallet som skal overføres til hver kanban.</span><span class="sxs-lookup"><span data-stu-id="1da6f-125">This is the quantity that will be transferred for each kanban.</span></span>  
3. <span data-ttu-id="1da6f-126">Merk av for Produktantallsavvik.</span><span class="sxs-lookup"><span data-stu-id="1da6f-126">Select the Product quantity variance check box.</span></span>
    * <span data-ttu-id="1da6f-127">Med dette kan valgte Kanbaner fullføres med et avvik fra standardantallet.</span><span class="sxs-lookup"><span data-stu-id="1da6f-127">With this, selected kanbans can be completed with a variance from the default quantity.</span></span>  <span data-ttu-id="1da6f-128">For å tillate Kanbaner å fullføres med et antall fra 8 til 12, setter du begge avvik til 2.</span><span class="sxs-lookup"><span data-stu-id="1da6f-128">To allow kanbans to be completed with a quantity from 8 to 12, set both variances to 2.</span></span>  
4. <span data-ttu-id="1da6f-129">Sett Avvik under til 2.</span><span class="sxs-lookup"><span data-stu-id="1da6f-129">Set Variance below to '2'.</span></span>
    * <span data-ttu-id="1da6f-130">Dette tillater fullføring ned til 10 - 2 = 8</span><span class="sxs-lookup"><span data-stu-id="1da6f-130">This will allow completing down to 10 - 2 = 8</span></span>  
5. <span data-ttu-id="1da6f-131">Sett Avvik over til 2.</span><span class="sxs-lookup"><span data-stu-id="1da6f-131">Set Variance above to '2'.</span></span>
    * <span data-ttu-id="1da6f-132">Dette tillater fullføring opp til 10 + 2 = 12</span><span class="sxs-lookup"><span data-stu-id="1da6f-132">This will allow completing up to 10 + 2 = 12</span></span>  
6. <span data-ttu-id="1da6f-133">Angi et nummer i feltet Fast Kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="1da6f-133">In the Fixed kanban quantity field, enter a number.</span></span>
    * <span data-ttu-id="1da6f-134">Dette er antall Kanbaner som skal være aktive.</span><span class="sxs-lookup"><span data-stu-id="1da6f-134">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="1da6f-135">I dette tilfellet 5 Kanbaner som hver behandler 10.</span><span class="sxs-lookup"><span data-stu-id="1da6f-135">In this case, 5 kanbans processing 10 each.</span></span>  
7. <span data-ttu-id="1da6f-136">Angi 2 i feltet Nedre varslingsgrense.</span><span class="sxs-lookup"><span data-stu-id="1da6f-136">In the Alert boundary minimum field, enter '2'.</span></span>
    * <span data-ttu-id="1da6f-137">Brukes til å holde oversikt over minimumsbeløpet for alle Kanbaner som skal være på målet.</span><span class="sxs-lookup"><span data-stu-id="1da6f-137">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="1da6f-138">Dette brukes for eksempel brukes i oversikten over kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="1da6f-138">For example, this is used on the kanban quantity overview.</span></span>  
8. <span data-ttu-id="1da6f-139">Angi 4 i feltet Øvre varslingsgrense.</span><span class="sxs-lookup"><span data-stu-id="1da6f-139">In the Alert boundary maximum field, enter '4'.</span></span>
    * <span data-ttu-id="1da6f-140">Brukes til å holde oversikt over maksimumsbeløpet for alle Kanbaner som skal være på målet.</span><span class="sxs-lookup"><span data-stu-id="1da6f-140">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="1da6f-141">Dette brukes for eksempel brukes i oversikten over kanban-antall.</span><span class="sxs-lookup"><span data-stu-id="1da6f-141">For example, this is used on the kanban quantity overview.</span></span>  
9. <span data-ttu-id="1da6f-142">Angi 1 feltet Antall for automatisk planlegging.</span><span class="sxs-lookup"><span data-stu-id="1da6f-142">In the Automatic planning quantity field, enter '1'.</span></span>
    * <span data-ttu-id="1da6f-143">Hvis du setter dette til 1, betyr det at hver kanban planlegges på nytt automatisk.</span><span class="sxs-lookup"><span data-stu-id="1da6f-143">Setting this to 1 means that every kanban will be automatically planned.</span></span>   <span data-ttu-id="1da6f-144">Hvis vi angir 3, vil ikke Kanbanene planlegges før 3 tomme Kanbaner er klar til planlegging.</span><span class="sxs-lookup"><span data-stu-id="1da6f-144">If we entered 3, the kanbans would not be planned until 3 empty kanbans are ready for planning.</span></span> <span data-ttu-id="1da6f-145">Dette er nyttig for å gruppere arbeidet og unngå for mange oppsett.</span><span class="sxs-lookup"><span data-stu-id="1da6f-145">This is useful for grouping work and avoiding too much setup.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="1da6f-146">Opprette Kanbaner</span><span class="sxs-lookup"><span data-stu-id="1da6f-146">Create Kanbans</span></span>
1. <span data-ttu-id="1da6f-147">Vis delen Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="1da6f-147">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="1da6f-148">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="1da6f-148">Click Save.</span></span>
    * <span data-ttu-id="1da6f-149">Kanban-regelen må lagres før du kan opprette Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="1da6f-149">The kanban rule needs to be saved before kanbans can be created.</span></span>  
3. <span data-ttu-id="1da6f-150">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="1da6f-150">Click Add.</span></span>
    * <span data-ttu-id="1da6f-151">Legg merke til at det ikke finnes noen aktive Kanbaner, og på grunn av dette er det foreslåtte "antallet nye Kanbaner" 5.</span><span class="sxs-lookup"><span data-stu-id="1da6f-151">Note that there are no active kanbans, due to this the suggested 'Number of new kanbans' are 5.</span></span> <span data-ttu-id="1da6f-152">Dette er lik "Fast Kanban-antall".</span><span class="sxs-lookup"><span data-stu-id="1da6f-152">This is equal to the 'Fixed kanban quantity'.</span></span>  
4. <span data-ttu-id="1da6f-153">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="1da6f-153">Click Create.</span></span>
    * <span data-ttu-id="1da6f-154">Dette vil opprette 5 Kanbaner.</span><span class="sxs-lookup"><span data-stu-id="1da6f-154">This will create 5 kanbans.</span></span>  
    * <span data-ttu-id="1da6f-155">Legg merke til at 5 Kanbaner, hver for 10, ble opprettet for denne kanban-regel for produksjon.</span><span class="sxs-lookup"><span data-stu-id="1da6f-155">Note that 5 kanbans, for 10 each, was created for this manufacturing kanban rule.</span></span> <span data-ttu-id="1da6f-156">Dette er det siste trinnet i prosedyren.</span><span class="sxs-lookup"><span data-stu-id="1da6f-156">This is the last step in this procedure.</span></span>  


