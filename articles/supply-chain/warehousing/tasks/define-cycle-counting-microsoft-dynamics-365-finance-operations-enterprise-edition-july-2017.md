---
title: 'Definere syklustelling '
description: Syklustelling er en lagerprosess som du kan bruke til å overvåke varer i lagerbeholdning.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountThreshold, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSParameters, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0b94bcc1c33889f336541f3dd8ba4782fac0261
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238996"
---
# <a name="define-cycle-counting"></a><span data-ttu-id="b9087-103">Definere syklustelling </span><span class="sxs-lookup"><span data-stu-id="b9087-103">Define cycle counting</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b9087-104">Syklustelling er en lagerprosess som du kan bruke til å overvåke varer i lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="b9087-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="b9087-105">Denne oppgaveregistreringen viser hvordan du gjør følgende: definere standard opptellingsarbeidsprioritet, aktivere et menyelement for mobil enhet for å behandle både plukkings- og opptellingsoperasjoner, aktivere en utløser for opptellingsterskel når en lokasjon blir tom og aktivere en syklustellingsplan for en bestemt vare i et bestemt lager.</span><span class="sxs-lookup"><span data-stu-id="b9087-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="b9087-106">Disse oppgavene utføres vanligvis av en lagersjef.</span><span class="sxs-lookup"><span data-stu-id="b9087-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="b9087-107">Du kan gå gjennom denne fremgangsmåten i USMF-demonstrasjonsdataselskapet eller i dine egne data.</span><span class="sxs-lookup"><span data-stu-id="b9087-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="b9087-108">Angi prioritet for opptellingsarbeid</span><span class="sxs-lookup"><span data-stu-id="b9087-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="b9087-109">I **navigasjonsruten** går du til **Moduler > Lagerstyring > Oppsett > Lagerstyringsparametere**.</span><span class="sxs-lookup"><span data-stu-id="b9087-109">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="b9087-110">Klikk på fanen **Syklustelling**.</span><span class="sxs-lookup"><span data-stu-id="b9087-110">Click the **Cycle counting** tab.</span></span>
3. <span data-ttu-id="b9087-111">Angi et nummer i feltet **Standardprioritet for arbeid for syklustelling**.</span><span class="sxs-lookup"><span data-stu-id="b9087-111">In the **Default cycle count work priority** field, enter a number.</span></span> <span data-ttu-id="b9087-112">Dette trinnet endrer prioriteten til syklustellingsarbeidet, sammenlignet med andre typer varer i lageret.</span><span class="sxs-lookup"><span data-stu-id="b9087-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="b9087-113">Ved å skrive inn et tall som er lavere enn tallet for andre typer arbeid, kan du øke prioriteten for syklustellingsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="b9087-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="b9087-114">Klikk på **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b9087-114">Click **Save**.</span></span>
5. <span data-ttu-id="b9087-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b9087-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="b9087-116">Aktivere mobilenheten</span><span class="sxs-lookup"><span data-stu-id="b9087-116">Enable the mobile device</span></span>
1. <span data-ttu-id="b9087-117">I **navigasjonsruten** går du til **Moduler > Lagerstyring > Oppsett > Mobilenhet >Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="b9087-117">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="b9087-118">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b9087-118">Click **New**.</span></span>
3. <span data-ttu-id="b9087-119">Skriv inn en verdi i feltet **Menyelementnavn**.</span><span class="sxs-lookup"><span data-stu-id="b9087-119">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="b9087-120">Skriv inn en verdi i **Tittel**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b9087-120">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="b9087-121">Velg Arbeid i feltet **Modus**.</span><span class="sxs-lookup"><span data-stu-id="b9087-121">In the **Mode** field, select 'Work'.</span></span>
6. <span data-ttu-id="b9087-122">Angi alternativet **Bruk eksisterende arbeid** til Ja.</span><span class="sxs-lookup"><span data-stu-id="b9087-122">Set the **Use existing work** option to Yes.</span></span> <span data-ttu-id="b9087-123">Når du setter dette alternativet til Ja, vil systemet se etter eksisterende arbeid når menyelementet for mobilenhet brukes.</span><span class="sxs-lookup"><span data-stu-id="b9087-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="b9087-124">Velg Systemstyrt i feltet **Styrt av**.</span><span class="sxs-lookup"><span data-stu-id="b9087-124">In the **Directed by** field, select 'System directed'.</span></span> <span data-ttu-id="b9087-125">Når "Systemrettet" er valgt, kommer lagermedarbeideren til å åpne arbeid som er i definerte arbeidsklasser.</span><span class="sxs-lookup"><span data-stu-id="b9087-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="b9087-126">(Vi vil opprette disse arbeidsklassene etterpå.)</span><span class="sxs-lookup"><span data-stu-id="b9087-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="b9087-127">Utvid **Arbeidsklasser**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="b9087-127">Expand the **Work classes** fastTab.</span></span> <span data-ttu-id="b9087-128">Nå skal vi opprette to klasser for arbeid som skal brukes med dette menyelementet for mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="b9087-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="b9087-129">Når menyelementet brukes, spørres det etter disse arbeidsklassene, og arbeidet med høyest prioritet blir vist for brukeren.</span><span class="sxs-lookup"><span data-stu-id="b9087-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="b9087-130">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b9087-130">Click **New**.</span></span>
10. <span data-ttu-id="b9087-131">Velg en verdi i feltet **Arbeidsklasse-ID**.</span><span class="sxs-lookup"><span data-stu-id="b9087-131">In the **Work class ID** field, select a value.</span></span>
11. <span data-ttu-id="b9087-132">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b9087-132">Click **New**.</span></span>
12. <span data-ttu-id="b9087-133">Velg en verdi i feltet **Arbeidsklasse-ID**.</span><span class="sxs-lookup"><span data-stu-id="b9087-133">In the **Work class ID** field, select a value.</span></span>
13. <span data-ttu-id="b9087-134">Klikk på **Lagre** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="b9087-134">In the **Action Pane**, click **Save**.</span></span>
14. <span data-ttu-id="b9087-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b9087-135">Close the page.</span></span>
15. <span data-ttu-id="b9087-136">I **navigasjonsruten** går du til **Moduler > Lagerstyring > Oppsett > Mobilenhet > Meny på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="b9087-136">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
16. <span data-ttu-id="b9087-137">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b9087-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="b9087-138">Velg menyelementet du har nettopp opprettet, i treet.</span><span class="sxs-lookup"><span data-stu-id="b9087-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="b9087-139">Klikk på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="b9087-139">Click **Edit**.</span></span>
19. <span data-ttu-id="b9087-140">Klikk på pilen for å legge til menyelementet i menyen.</span><span class="sxs-lookup"><span data-stu-id="b9087-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="b9087-141">Klikk på **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b9087-141">Click **Save**.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="b9087-142">Opprette en opptellingsterskel</span><span class="sxs-lookup"><span data-stu-id="b9087-142">Create a counting threshold</span></span>
1. <span data-ttu-id="b9087-143">I **navigasjonsruten** går du til **Moduler > Lagerstyring > Oppsett > Syklustelling > Terskler for syklustelling**.</span><span class="sxs-lookup"><span data-stu-id="b9087-143">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count thresholds**.</span></span>
2. <span data-ttu-id="b9087-144">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b9087-144">Click **New**.</span></span>
3. <span data-ttu-id="b9087-145">Skriv inn en verdi i feltet **ID for syklustellingsterskel**.</span><span class="sxs-lookup"><span data-stu-id="b9087-145">In the **Cycle counting threshold ID** field, type a value.</span></span>
4. <span data-ttu-id="b9087-146">Angi alternativet **Behandle syklustelling umiddelbart** til Ja.</span><span class="sxs-lookup"><span data-stu-id="b9087-146">Set the **Process cycle counting immediately** option to Yes.</span></span>
5. <span data-ttu-id="b9087-147">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b9087-147">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="b9087-148">Klikk på **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b9087-148">Click **Save**.</span></span>
7. <span data-ttu-id="b9087-149">Klikk på **Velg lokasjoner**.</span><span class="sxs-lookup"><span data-stu-id="b9087-149">Click **Select locations**.</span></span>
8. <span data-ttu-id="b9087-150">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b9087-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="b9087-151">Velg en verdi i **Kriterier**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b9087-151">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="b9087-152">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9087-152">Click **OK**.</span></span>
11. <span data-ttu-id="b9087-153">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b9087-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="b9087-154">Opprette en plan for syklustelling</span><span class="sxs-lookup"><span data-stu-id="b9087-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="b9087-155">I **navigasjonsruten** går du til **Moduler > Lagerstyring > Oppsett > Syklustelling > Planer for syklustelling**.</span><span class="sxs-lookup"><span data-stu-id="b9087-155">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count plans**.</span></span>
2. <span data-ttu-id="b9087-156">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b9087-156">Click **New**.</span></span>
3. <span data-ttu-id="b9087-157">Skriv inn en verdi i feltet **ID for syklustellingsplan**.</span><span class="sxs-lookup"><span data-stu-id="b9087-157">In the **Cycle counting plan ID** field, type a value.</span></span>
4. <span data-ttu-id="b9087-158">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b9087-158">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="b9087-159">Angi et tall i feltet **Største antall syklustellinger**.</span><span class="sxs-lookup"><span data-stu-id="b9087-159">In the **Maximum number of cycle counts** field, enter a number.</span></span>
6. <span data-ttu-id="b9087-160">Klikk på **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b9087-160">Click **Save**.</span></span>
7. <span data-ttu-id="b9087-161">Klikk på **Velg lokasjoner**.</span><span class="sxs-lookup"><span data-stu-id="b9087-161">Click **Select locations**.</span></span>
8. <span data-ttu-id="b9087-162">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b9087-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="b9087-163">Velg en verdi i **Kriterier**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b9087-163">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="b9087-164">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9087-164">Click **OK**.</span></span>
11. <span data-ttu-id="b9087-165">Angi et tall i feltet **Dager mellom syklustellinger**.</span><span class="sxs-lookup"><span data-stu-id="b9087-165">In the **Days between cycle counting** field, enter a number.</span></span> <span data-ttu-id="b9087-166">Hvis for eksempel feltet **Dager mellom syklustellinger** er angitt til 5, opprettes syklustellingsarbeidet hver femte dag.</span><span class="sxs-lookup"><span data-stu-id="b9087-166">For example, if the **Days between cycle counting** field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="b9087-167">Hvis syklustellingsarbeid imidlertid behandles på dag tre, opprettes neste syklustellingsarbeid fem dager etter den siste syklustellingen ble behandlet, på dag 8.</span><span class="sxs-lookup"><span data-stu-id="b9087-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="b9087-168">Klikk på **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b9087-168">Click **Save**.</span></span>
13. <span data-ttu-id="b9087-169">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b9087-169">Click **New**.</span></span>
14. <span data-ttu-id="b9087-170">Angi et nummer i **Sekvensnummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b9087-170">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="b9087-171">Sorteringen er fra det laveste tallet til det høyeste tallet.</span><span class="sxs-lookup"><span data-stu-id="b9087-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="b9087-172">Verdien må være over 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b9087-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="b9087-173">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b9087-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="b9087-174">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b9087-174">In the **Description** field, type a value.</span></span>
17. <span data-ttu-id="b9087-175">Klikk på **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b9087-175">Click **Save**.</span></span>
18. <span data-ttu-id="b9087-176">Klikk på **Definer produktspørring**.</span><span class="sxs-lookup"><span data-stu-id="b9087-176">Click **Define product** query.</span></span>
19. <span data-ttu-id="b9087-177">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b9087-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="b9087-178">Angi eller velg en verdi i **Kriterier**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b9087-178">In the **Criteria** field, enter or select a value.</span></span>
21. <span data-ttu-id="b9087-179">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9087-179">Click **OK**.</span></span>
22. <span data-ttu-id="b9087-180">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b9087-180">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]