--- 
title: Aktivere utskrift av nummerskiltetikett
description: "Denne fremgangsmåten tillater automatisk utskrift av en SSCC-etikett (Serial Shipping Container Code) etter at den siste varen er plukket fra lageret i en arbeidsprosess for salgsplukk."
author: perlynne
manager: AnnBe
ms.date: 11/03/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6d186bf7e4aee8cfa97adbd90b9090085e842f9b
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="25717-103">Aktivere utskrift av nummerskiltetikett</span><span class="sxs-lookup"><span data-stu-id="25717-103">Enable license plate label printing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25717-104">Denne fremgangsmåten tillater automatisk utskrift av en SSCC-etikett (Serial Shipping Container Code) etter at den siste varen er plukket fra lageret i en arbeidsprosess for salgsplukk.</span><span class="sxs-lookup"><span data-stu-id="25717-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="25717-105">Du kan kjøre denne prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="25717-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="25717-106">Hvis du skal kjøre det på dine egne data, må du ha en nummerserie som er definert for nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="25717-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="25717-107">Du må definere en etikettskriver før du begynner.</span><span class="sxs-lookup"><span data-stu-id="25717-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="25717-108">Gå til Organisasjonsstyring > Oppsett > Nettverksskrivere.</span><span class="sxs-lookup"><span data-stu-id="25717-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="25717-109">I handlingsruten velger du Alternativer, og deretter klikker du Last ned installasjonsprogram for dokumentrutingsagent.</span><span class="sxs-lookup"><span data-stu-id="25717-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="25717-110">Kjør installasjonsprogrammet og kontroller at du har en fungerende skriver satt til Aktiv før du fortsetter med prosedyren.</span><span class="sxs-lookup"><span data-stu-id="25717-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="25717-111">Angi GS1-firmaprefikset</span><span class="sxs-lookup"><span data-stu-id="25717-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="25717-112">Gå til Lagerstyring > Oppsett > Lagerstyringsparametere.</span><span class="sxs-lookup"><span data-stu-id="25717-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="25717-113">I feltet GS1-firmaprefiks angir du det 7-sifrede GS1-firmanummeret.</span><span class="sxs-lookup"><span data-stu-id="25717-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="25717-114">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="25717-114">Click Save.</span></span>
4. <span data-ttu-id="25717-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="25717-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="25717-116">Konfigurasjon av nummerserien for SSCC-skiltnummeret</span><span class="sxs-lookup"><span data-stu-id="25717-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="25717-117">Gå til Organisasjonsadministrasjon > Nummerserier > Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="25717-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="25717-118">Velg et alternativ i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="25717-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="25717-119">Velg et alternativ i Referanse-feltet.</span><span class="sxs-lookup"><span data-stu-id="25717-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="25717-120">Skriv inn en verdi i feltet Firma.</span><span class="sxs-lookup"><span data-stu-id="25717-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="25717-121">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="25717-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="25717-122">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="25717-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="25717-123">Utvid seksjonen Segmenter.</span><span class="sxs-lookup"><span data-stu-id="25717-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="25717-124">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="25717-124">Click Edit.</span></span>
9. <span data-ttu-id="25717-125">Merk den første raden i tabellen Segmenter</span><span class="sxs-lookup"><span data-stu-id="25717-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="25717-126">Klikk Fjern.</span><span class="sxs-lookup"><span data-stu-id="25717-126">Click Remove.</span></span>
11. <span data-ttu-id="25717-127">Klikk Fjern.</span><span class="sxs-lookup"><span data-stu-id="25717-127">Click Remove.</span></span>
12. <span data-ttu-id="25717-128">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="25717-128">Click Save.</span></span>
13. <span data-ttu-id="25717-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="25717-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="25717-130">Opprett dokumentruteoppsettet</span><span class="sxs-lookup"><span data-stu-id="25717-130">Create the document route layout</span></span>
1. <span data-ttu-id="25717-131">Gå til Lagerstyring > Oppsett > Dokumentruting > Dokumentrutingsoppsett.</span><span class="sxs-lookup"><span data-stu-id="25717-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="25717-132">Aktiver SSCC-oppsettet.</span><span class="sxs-lookup"><span data-stu-id="25717-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="25717-133">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="25717-133">Click New.</span></span>
3. <span data-ttu-id="25717-134">Skriv inn en verdi i feltet Oppset-ID.</span><span class="sxs-lookup"><span data-stu-id="25717-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="25717-135">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="25717-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="25717-136">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="25717-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="25717-137">Klikk Sett inn i slutten av teksten.</span><span class="sxs-lookup"><span data-stu-id="25717-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="25717-138">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="25717-138">Click Save.</span></span>
8. <span data-ttu-id="25717-139">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="25717-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="25717-140">Konfigurer dokumentrutingen</span><span class="sxs-lookup"><span data-stu-id="25717-140">Set up the document routing</span></span>
1. <span data-ttu-id="25717-141">Gå til Lagerstyring > Oppsett > Dokumentruting > Dokumentruting.</span><span class="sxs-lookup"><span data-stu-id="25717-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="25717-142">Velg et alternativ i feltet Arbeidsordretype.</span><span class="sxs-lookup"><span data-stu-id="25717-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="25717-143">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="25717-143">Click New.</span></span>
4. <span data-ttu-id="25717-144">Skriv inn en verdi i Lager-feltet.</span><span class="sxs-lookup"><span data-stu-id="25717-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="25717-145">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="25717-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="25717-146">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="25717-146">Click New.</span></span>
7. <span data-ttu-id="25717-147">Angi eller velg en verdi i feltet Oppsett-ID.</span><span class="sxs-lookup"><span data-stu-id="25717-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="25717-148">I Navn-feltet angir du navnet på skriveren du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="25717-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="25717-149">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="25717-149">Click Save.</span></span>
10. <span data-ttu-id="25717-150">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="25717-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="25717-151">Opprett mobilenhetsmeny</span><span class="sxs-lookup"><span data-stu-id="25717-151">Create mobile device menu</span></span>
1. <span data-ttu-id="25717-152">Gå til Lagerstyring > Oppsett > Mobilenhet > Menyelementer på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="25717-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="25717-153">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="25717-153">Click New.</span></span>
3. <span data-ttu-id="25717-154">Skriv inn en verdi i feltet Menyelementnavn.</span><span class="sxs-lookup"><span data-stu-id="25717-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="25717-155">Skriv inn en verdi i Tittel-feltet.</span><span class="sxs-lookup"><span data-stu-id="25717-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="25717-156">Velg et alternativ i Modus -feltet.</span><span class="sxs-lookup"><span data-stu-id="25717-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="25717-157">Velg Ja i feltet Bruk eksisterende arbeid.</span><span class="sxs-lookup"><span data-stu-id="25717-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="25717-158">Velg Ja i Generer nummerskilt-feltet.</span><span class="sxs-lookup"><span data-stu-id="25717-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="25717-159">Utvid Arbeidsklasser-delen.</span><span class="sxs-lookup"><span data-stu-id="25717-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="25717-160">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="25717-160">Click New.</span></span>
10. <span data-ttu-id="25717-161">Skriv inn en verdi i feltet Arbeidsklasse-ID.</span><span class="sxs-lookup"><span data-stu-id="25717-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="25717-162">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="25717-162">Click Save.</span></span>
12. <span data-ttu-id="25717-163">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="25717-163">Close the page.</span></span>
13. <span data-ttu-id="25717-164">Gå til Lagerstyring > Oppsett > Mobilenhet > Meny på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="25717-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="25717-165">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="25717-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="25717-166">I treet velger du menyelementet du har opprettet før.</span><span class="sxs-lookup"><span data-stu-id="25717-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="25717-167">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="25717-167">Click Edit.</span></span>
17. <span data-ttu-id="25717-168">Klikk pilen for å legge til menyelementet i menyen.</span><span class="sxs-lookup"><span data-stu-id="25717-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="25717-169">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="25717-169">Click Save.</span></span>
19. <span data-ttu-id="25717-170">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="25717-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="25717-171">Oppdater en arbeidsmal</span><span class="sxs-lookup"><span data-stu-id="25717-171">Update a work template</span></span>
1. <span data-ttu-id="25717-172">Gå til Lagerstyring > Oppsett > Arbeid > Arbeidsmaler.</span><span class="sxs-lookup"><span data-stu-id="25717-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="25717-173">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="25717-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="25717-174">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="25717-174">Click Edit.</span></span>
4. <span data-ttu-id="25717-175">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="25717-175">Click New.</span></span>
5. <span data-ttu-id="25717-176">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="25717-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="25717-177">Velg Skriv ut i Arbeidstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="25717-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="25717-178">Angi eller velg en verdi i feltet Arbeidsklasse-ID.</span><span class="sxs-lookup"><span data-stu-id="25717-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="25717-179">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="25717-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="25717-180">Klikk Flytt opp.</span><span class="sxs-lookup"><span data-stu-id="25717-180">Click Move up.</span></span>
10. <span data-ttu-id="25717-181">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="25717-181">Click Save.</span></span>
11. <span data-ttu-id="25717-182">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="25717-182">Close the page.</span></span>


