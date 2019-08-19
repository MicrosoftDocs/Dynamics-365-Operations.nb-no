---
title: Aktivere utskrift av nummerskiltetikett
description: Denne fremgangsmåten tillater automatisk utskrift av en SSCC-etikett (Serial Shipping Container Code) etter at den siste varen er plukket fra lageret i en arbeidsprosess for salgsplukk.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed74806e5e037570f3ed7f59725eed494c829d34
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847279"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="9bdfc-103">Aktivere utskrift av nummerskiltetikett</span><span class="sxs-lookup"><span data-stu-id="9bdfc-103">Enable license plate label printing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9bdfc-104">Denne fremgangsmåten tillater automatisk utskrift av en SSCC-etikett (Serial Shipping Container Code) etter at den siste varen er plukket fra lageret i en arbeidsprosess for salgsplukk.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="9bdfc-105">Du kan kjøre denne prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="9bdfc-106">Hvis du skal kjøre det på dine egne data, må du ha en nummerserie som er definert for nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="9bdfc-107">Du må definere en etikettskriver før du begynner.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="9bdfc-108">Gå til Organisasjonsstyring > Oppsett > Nettverksskrivere.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="9bdfc-109">I handlingsruten velger du Alternativer, og deretter klikker du Last ned installasjonsprogram for dokumentrutingsagent.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="9bdfc-110">Kjør installasjonsprogrammet og kontroller at du har en fungerende skriver satt til Aktiv før du fortsetter med prosedyren.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="9bdfc-111">Angi GS1-firmaprefikset</span><span class="sxs-lookup"><span data-stu-id="9bdfc-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="9bdfc-112">Gå til Lagerstyring > Oppsett > Lagerstyringsparametere.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="9bdfc-113">I feltet GS1-firmaprefiks angir du det 7-sifrede GS1-firmanummeret.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="9bdfc-114">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-114">Click Save.</span></span>
4. <span data-ttu-id="9bdfc-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="9bdfc-116">Konfigurasjon av nummerserien for SSCC-skiltnummeret</span><span class="sxs-lookup"><span data-stu-id="9bdfc-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="9bdfc-117">Gå til Organisasjonsadministrasjon > Nummerserier > Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="9bdfc-118">Velg et alternativ i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="9bdfc-119">Velg et alternativ i Referanse-feltet.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="9bdfc-120">Skriv inn en verdi i feltet Firma.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="9bdfc-121">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="9bdfc-122">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="9bdfc-123">Utvid seksjonen Segmenter.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="9bdfc-124">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-124">Click Edit.</span></span>
9. <span data-ttu-id="9bdfc-125">Merk den første raden i tabellen Segmenter</span><span class="sxs-lookup"><span data-stu-id="9bdfc-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="9bdfc-126">Klikk Fjern.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-126">Click Remove.</span></span>
11. <span data-ttu-id="9bdfc-127">Klikk Fjern.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-127">Click Remove.</span></span>
12. <span data-ttu-id="9bdfc-128">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-128">Click Save.</span></span>
13. <span data-ttu-id="9bdfc-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="9bdfc-130">Opprett dokumentruteoppsettet</span><span class="sxs-lookup"><span data-stu-id="9bdfc-130">Create the document route layout</span></span>
1. <span data-ttu-id="9bdfc-131">Gå til Lagerstyring > Oppsett > Dokumentruting > Dokumentrutingsoppsett.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="9bdfc-132">Aktiver SSCC-oppsettet.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="9bdfc-133">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-133">Click New.</span></span>
3. <span data-ttu-id="9bdfc-134">Skriv inn en verdi i feltet Oppset-ID.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="9bdfc-135">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9bdfc-136">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="9bdfc-137">Klikk Sett inn i slutten av teksten.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="9bdfc-138">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-138">Click Save.</span></span>
8. <span data-ttu-id="9bdfc-139">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="9bdfc-140">Konfigurer dokumentrutingen</span><span class="sxs-lookup"><span data-stu-id="9bdfc-140">Set up the document routing</span></span>
1. <span data-ttu-id="9bdfc-141">Gå til Lagerstyring > Oppsett > Dokumentruting > Dokumentruting.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="9bdfc-142">Velg et alternativ i feltet Arbeidsordretype.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="9bdfc-143">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-143">Click New.</span></span>
4. <span data-ttu-id="9bdfc-144">Skriv inn en verdi i Lager-feltet.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="9bdfc-145">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="9bdfc-146">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-146">Click New.</span></span>
7. <span data-ttu-id="9bdfc-147">Angi eller velg en verdi i feltet Oppsett-ID.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="9bdfc-148">I Navn-feltet angir du navnet på skriveren du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="9bdfc-149">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-149">Click Save.</span></span>
10. <span data-ttu-id="9bdfc-150">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="9bdfc-151">Opprett mobilenhetsmeny</span><span class="sxs-lookup"><span data-stu-id="9bdfc-151">Create mobile device menu</span></span>
1. <span data-ttu-id="9bdfc-152">Gå til Lagerstyring > Oppsett > Mobilenhet > Menyelementer på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="9bdfc-153">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-153">Click New.</span></span>
3. <span data-ttu-id="9bdfc-154">Skriv inn en verdi i feltet Menyelementnavn.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="9bdfc-155">Skriv inn en verdi i Tittel-feltet.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="9bdfc-156">Velg et alternativ i Modus -feltet.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="9bdfc-157">Velg Ja i feltet Bruk eksisterende arbeid.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="9bdfc-158">Velg Ja i Generer nummerskilt-feltet.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="9bdfc-159">Utvid Arbeidsklasser-delen.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="9bdfc-160">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-160">Click New.</span></span>
10. <span data-ttu-id="9bdfc-161">Skriv inn en verdi i feltet Arbeidsklasse-ID.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="9bdfc-162">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-162">Click Save.</span></span>
12. <span data-ttu-id="9bdfc-163">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-163">Close the page.</span></span>
13. <span data-ttu-id="9bdfc-164">Gå til Lagerstyring > Oppsett > Mobilenhet > Meny på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="9bdfc-165">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="9bdfc-166">I treet velger du menyelementet du har opprettet før.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="9bdfc-167">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="9bdfc-167">Click Edit.</span></span>
17. <span data-ttu-id="9bdfc-168">Klikk pilen for å legge til menyelementet i menyen.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="9bdfc-169">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-169">Click Save.</span></span>
19. <span data-ttu-id="9bdfc-170">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="9bdfc-171">Oppdater en arbeidsmal</span><span class="sxs-lookup"><span data-stu-id="9bdfc-171">Update a work template</span></span>
1. <span data-ttu-id="9bdfc-172">Gå til Lagerstyring > Oppsett > Arbeid > Arbeidsmaler.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="9bdfc-173">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9bdfc-174">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-174">Click Edit.</span></span>
4. <span data-ttu-id="9bdfc-175">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-175">Click New.</span></span>
5. <span data-ttu-id="9bdfc-176">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="9bdfc-177">Velg Skriv ut i Arbeidstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="9bdfc-178">Angi eller velg en verdi i feltet Arbeidsklasse-ID.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="9bdfc-179">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9bdfc-180">Klikk Flytt opp.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-180">Click Move up.</span></span>
10. <span data-ttu-id="9bdfc-181">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-181">Click Save.</span></span>
11. <span data-ttu-id="9bdfc-182">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9bdfc-182">Close the page.</span></span>

