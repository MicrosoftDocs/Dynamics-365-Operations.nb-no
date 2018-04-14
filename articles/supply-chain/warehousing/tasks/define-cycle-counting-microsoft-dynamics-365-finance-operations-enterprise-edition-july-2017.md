--- 
title: 'Definere syklustelling '
description: "Syklustelling er en lagerprosess som du kan bruke til å overvåke varer i lagerbeholdning."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5a95f63efe3d78dc371cacdc09734490a601b1b8
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="define-cycle-counting"></a><span data-ttu-id="57b82-103">Definere syklustelling </span><span class="sxs-lookup"><span data-stu-id="57b82-103">Define cycle counting</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="57b82-104">Syklustelling er en lagerprosess som du kan bruke til å overvåke varer i lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="57b82-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="57b82-105">Denne oppgaveregistreringen viser hvordan du gjør følgende: definere standard opptellingsarbeidsprioritet, aktivere et menyelement for mobil enhet for å behandle både plukkings- og opptellingsoperasjoner, aktivere en utløser for opptellingsterskel når en lokasjon blir tom og aktivere en syklustellingsplan for en bestemt vare i et bestemt lager.</span><span class="sxs-lookup"><span data-stu-id="57b82-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="57b82-106">Disse oppgavene utføres vanligvis av en lagersjef.</span><span class="sxs-lookup"><span data-stu-id="57b82-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="57b82-107">Du kan gå gjennom denne fremgangsmåten i USMF-demonstrasjonsdataselskapet eller i dine egne data.</span><span class="sxs-lookup"><span data-stu-id="57b82-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="57b82-108">Angi prioritet for opptellingsarbeid</span><span class="sxs-lookup"><span data-stu-id="57b82-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="57b82-109">Gå til Lagerstyring > Oppsett > Lagerstyringsparametere.</span><span class="sxs-lookup"><span data-stu-id="57b82-109">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="57b82-110">Klikk kategorien for Syklustelling.</span><span class="sxs-lookup"><span data-stu-id="57b82-110">Click the Cycle counting tab.</span></span>
3. <span data-ttu-id="57b82-111">Angi et nummer i feltet Standardprioritet for arbeid for syklustelling.</span><span class="sxs-lookup"><span data-stu-id="57b82-111">In the Default cycle count work priority field, enter a number.</span></span>
    * <span data-ttu-id="57b82-112">Dette trinnet endrer prioriteten til syklustellingsarbeidet, sammenlignet med andre typer varer i lageret.</span><span class="sxs-lookup"><span data-stu-id="57b82-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="57b82-113">Ved å skrive inn et tall som er lavere enn tallet for andre typer arbeid, kan du øke prioriteten for syklustellingsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="57b82-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="57b82-114">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="57b82-114">Click Save.</span></span>
5. <span data-ttu-id="57b82-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="57b82-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="57b82-116">Aktivere mobilenheten</span><span class="sxs-lookup"><span data-stu-id="57b82-116">Enable the mobile device</span></span>
1. <span data-ttu-id="57b82-117">Gå til Lagerstyring > Oppsett > Mobilenhet > Menyelementer på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="57b82-117">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="57b82-118">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="57b82-118">Click New.</span></span>
3. <span data-ttu-id="57b82-119">Skriv inn en verdi i feltet Menyelementnavn.</span><span class="sxs-lookup"><span data-stu-id="57b82-119">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="57b82-120">Skriv inn en verdi i Tittel-feltet.</span><span class="sxs-lookup"><span data-stu-id="57b82-120">In the Title field, type a value.</span></span>
5. <span data-ttu-id="57b82-121">Velg Arbeid i feltet Modus.</span><span class="sxs-lookup"><span data-stu-id="57b82-121">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="57b82-122">Angi alternativet Bruk eksisterende arbeid til Ja.</span><span class="sxs-lookup"><span data-stu-id="57b82-122">Set the Use existing work option to Yes.</span></span>
    * <span data-ttu-id="57b82-123">Når du setter dette alternativet til Ja, vil systemet se etter eksisterende arbeid når menyelementet for mobilenhet brukes.</span><span class="sxs-lookup"><span data-stu-id="57b82-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="57b82-124">Velg Systemstyrt i feltet Styrt av.</span><span class="sxs-lookup"><span data-stu-id="57b82-124">In the Directed by field, select 'System directed'.</span></span>
    * <span data-ttu-id="57b82-125">Når "Systemrettet" er valgt, kommer lagermedarbeideren til å åpne arbeid som er i definerte arbeidsklasser.</span><span class="sxs-lookup"><span data-stu-id="57b82-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="57b82-126">(Vi vil opprette disse arbeidsklassene etterpå.)</span><span class="sxs-lookup"><span data-stu-id="57b82-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="57b82-127">Vis eller skjul delen Arbeidsklasser.</span><span class="sxs-lookup"><span data-stu-id="57b82-127">Expand or collapse the Work classes section.</span></span>
    * <span data-ttu-id="57b82-128">Nå skal vi opprette to klasser for arbeid som skal brukes med dette menyelementet for mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="57b82-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="57b82-129">Når menyelementet brukes, spørres det etter disse arbeidsklassene, og arbeidet med høyest prioritet blir vist for brukeren.</span><span class="sxs-lookup"><span data-stu-id="57b82-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="57b82-130">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="57b82-130">Click New.</span></span>
10. <span data-ttu-id="57b82-131">Velg en verdi i feltet Arbeidsklasse-ID.</span><span class="sxs-lookup"><span data-stu-id="57b82-131">In the Work class ID field, select a value.</span></span>
11. <span data-ttu-id="57b82-132">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="57b82-132">Click New.</span></span>
12. <span data-ttu-id="57b82-133">Velg en verdi i feltet Arbeidsklasse-ID.</span><span class="sxs-lookup"><span data-stu-id="57b82-133">In the Work class ID field, select a value.</span></span>
13. <span data-ttu-id="57b82-134">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="57b82-134">Click Save.</span></span>
14. <span data-ttu-id="57b82-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="57b82-135">Close the page.</span></span>
15. <span data-ttu-id="57b82-136">Gå til Lagerstyring > Oppsett > Mobilenhet > Meny på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="57b82-136">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
16. <span data-ttu-id="57b82-137">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="57b82-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="57b82-138">Velg menyelementet du har nettopp opprettet, i treet.</span><span class="sxs-lookup"><span data-stu-id="57b82-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="57b82-139">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="57b82-139">Click Edit.</span></span>
19. <span data-ttu-id="57b82-140">Klikk pilen for å legge til menyelementet i menyen.</span><span class="sxs-lookup"><span data-stu-id="57b82-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="57b82-141">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="57b82-141">Click Save.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="57b82-142">Opprette en opptellingsterskel</span><span class="sxs-lookup"><span data-stu-id="57b82-142">Create a counting threshold</span></span>
1. <span data-ttu-id="57b82-143">Gå til Lagerstyring > Oppsett > Syklustelling > Terskler for syklustelling.</span><span class="sxs-lookup"><span data-stu-id="57b82-143">Go to Warehouse management > Setup > Cycle counting > Cycle count thresholds.</span></span>
2. <span data-ttu-id="57b82-144">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="57b82-144">Click New.</span></span>
3. <span data-ttu-id="57b82-145">Skriv inn en verdi i feltet ID for syklustellingsterskel.</span><span class="sxs-lookup"><span data-stu-id="57b82-145">In the Cycle counting threshold ID field, type a value.</span></span>
4. <span data-ttu-id="57b82-146">Angi alternativet Behandle syklustelling umiddelbart som Ja.</span><span class="sxs-lookup"><span data-stu-id="57b82-146">Set the Process cycle counting immediately option to Yes.</span></span>
5. <span data-ttu-id="57b82-147">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="57b82-147">In the Description field, type a value.</span></span>
6. <span data-ttu-id="57b82-148">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="57b82-148">Click Save.</span></span>
7. <span data-ttu-id="57b82-149">Klikk Velg lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="57b82-149">Click Select locations.</span></span>
8. <span data-ttu-id="57b82-150">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="57b82-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="57b82-151">Velg en verdi i feltet Vilkår.</span><span class="sxs-lookup"><span data-stu-id="57b82-151">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="57b82-152">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="57b82-152">Click OK.</span></span>
11. <span data-ttu-id="57b82-153">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="57b82-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="57b82-154">Opprette en plan for syklustelling</span><span class="sxs-lookup"><span data-stu-id="57b82-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="57b82-155">Gå til Lagerstyring > Oppsett > Syklustelling > Planer for syklustelling.</span><span class="sxs-lookup"><span data-stu-id="57b82-155">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="57b82-156">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="57b82-156">Click New.</span></span>
3. <span data-ttu-id="57b82-157">Skriv inn en verdi i feltet ID for syklustellingsplan.</span><span class="sxs-lookup"><span data-stu-id="57b82-157">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="57b82-158">Skriv inn en verdi i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="57b82-158">In the Description field, type a value.</span></span>
5. <span data-ttu-id="57b82-159">Angi et tall i feltet Største antall syklustellinger.</span><span class="sxs-lookup"><span data-stu-id="57b82-159">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="57b82-160">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="57b82-160">Click Save.</span></span>
7. <span data-ttu-id="57b82-161">Klikk Velg lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="57b82-161">Click Select locations.</span></span>
8. <span data-ttu-id="57b82-162">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="57b82-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="57b82-163">Velg en verdi i feltet Vilkår.</span><span class="sxs-lookup"><span data-stu-id="57b82-163">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="57b82-164">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="57b82-164">Click OK.</span></span>
11. <span data-ttu-id="57b82-165">Angi et tall i feltet Dager mellom syklustellinger.</span><span class="sxs-lookup"><span data-stu-id="57b82-165">In the Days between cycle counting field, enter a number.</span></span>
    * <span data-ttu-id="57b82-166">Hvis for eksempel feltet Dager mellom syklustellinger er angitt til 5, opprettes syklustellingsarbeidet hver femte dag.</span><span class="sxs-lookup"><span data-stu-id="57b82-166">For example, if the Days between cycle counting field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="57b82-167">Hvis syklustellingsarbeid imidlertid behandles på dag tre, opprettes neste syklustellingsarbeid fem dager etter den siste syklustellingen ble behandlet, på dag 8.</span><span class="sxs-lookup"><span data-stu-id="57b82-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="57b82-168">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="57b82-168">Click Save.</span></span>
13. <span data-ttu-id="57b82-169">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="57b82-169">Click New.</span></span>
14. <span data-ttu-id="57b82-170">Angi et nummer i Sekvensnummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="57b82-170">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="57b82-171">Sorteringen er fra det laveste tallet til det høyeste tallet.</span><span class="sxs-lookup"><span data-stu-id="57b82-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="57b82-172">Verdien må være over 0 (null).</span><span class="sxs-lookup"><span data-stu-id="57b82-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="57b82-173">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="57b82-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="57b82-174">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="57b82-174">In the Description field, type a value.</span></span>
17. <span data-ttu-id="57b82-175">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="57b82-175">Click Save.</span></span>
18. <span data-ttu-id="57b82-176">Klikk Definer produktspørring.</span><span class="sxs-lookup"><span data-stu-id="57b82-176">Click Define product query.</span></span>
19. <span data-ttu-id="57b82-177">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="57b82-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="57b82-178">Angi eller velg en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="57b82-178">In the Criteria field, enter or select a value.</span></span>
21. <span data-ttu-id="57b82-179">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="57b82-179">Click OK.</span></span>
22. <span data-ttu-id="57b82-180">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="57b82-180">Close the page.</span></span>


