---
title: Aktivere utskrift av nummerskiltetikett
description: Dette emnet viser hvordan du aktiverer automatisk utskrift av en SSCC-etikett (Serial Shipping Container Code) etter at den siste varen er plukket fra lageret i en arbeidsprosess for salgsplukk.
author: perlynne
manager: AnnBe
ms.date: 07/19/2019
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
ms.openlocfilehash: ed4fa28039c9320998f6524c9c9edb0a0301b7b0
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866832"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="1e593-103">Aktivere utskrift av nummerskiltetikett</span><span class="sxs-lookup"><span data-stu-id="1e593-103">Enable license plate label printing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1e593-104">Dette emnet viser hvordan du aktiverer automatisk utskrift av en SSCC-etikett (Serial Shipping Container Code) etter at den siste varen er plukket fra lageret i en arbeidsprosess for salgsplukk.</span><span class="sxs-lookup"><span data-stu-id="1e593-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="1e593-105">Du kan kjøre denne prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="1e593-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="1e593-106">Hvis du skal kjøre det på dine egne data, må du ha en nummerserie som er definert for nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="1e593-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="1e593-107">Du må definere en etikettskriver før du begynner.</span><span class="sxs-lookup"><span data-stu-id="1e593-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="1e593-108">Gå til Organisasjonsstyring > Oppsett > Nettverksskrivere.</span><span class="sxs-lookup"><span data-stu-id="1e593-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="1e593-109">I handlingsruten velger du Alternativer, og deretter klikker du Last ned installasjonsprogram for dokumentrutingsagent.</span><span class="sxs-lookup"><span data-stu-id="1e593-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="1e593-110">Kjør installasjonsprogrammet og kontroller at du har en fungerende skriver satt til Aktiv før du fortsetter med prosedyren.</span><span class="sxs-lookup"><span data-stu-id="1e593-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="1e593-111">Angi GS1-firmaprefikset</span><span class="sxs-lookup"><span data-stu-id="1e593-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="1e593-112">Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Lagerstyringsparametere**.</span><span class="sxs-lookup"><span data-stu-id="1e593-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="1e593-113">I feltet **GS1-firmaprefiks** angir du det 7-sifrede GS1-firmanummeret.</span><span class="sxs-lookup"><span data-stu-id="1e593-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="1e593-114">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="1e593-114">Select **Save**.</span></span>
4. <span data-ttu-id="1e593-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1e593-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="1e593-116">Konfigurasjon av nummerserien for SSCC-skiltnummeret</span><span class="sxs-lookup"><span data-stu-id="1e593-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="1e593-117">Gå til **Navigasjonsrute > Moduler > Organisasjonsadministrasjon > Nummerserier > Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="1e593-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="1e593-118">Velg et alternativ i **Område**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1e593-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="1e593-119">Velg et alternativ i **Referanse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1e593-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="1e593-120">Skriv inn en verdi i feltet **Firma.**</span><span class="sxs-lookup"><span data-stu-id="1e593-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="1e593-121">Utvid seksjonen **Segmenter**.</span><span class="sxs-lookup"><span data-stu-id="1e593-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="1e593-122">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="1e593-122">Select **Edit**.</span></span>
7. <span data-ttu-id="1e593-123">Merk den første raden i tabellen **Segmenter**.</span><span class="sxs-lookup"><span data-stu-id="1e593-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="1e593-124">Velg **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="1e593-124">Select **Remove**.</span></span>
9. <span data-ttu-id="1e593-125">Velg **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="1e593-125">Select **Remove**.</span></span>
10. <span data-ttu-id="1e593-126">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="1e593-126">Select **Save**.</span></span>
11. <span data-ttu-id="1e593-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1e593-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="1e593-128">Opprett dokumentruteoppsettet</span><span class="sxs-lookup"><span data-stu-id="1e593-128">Create the document route layout</span></span>
1. <span data-ttu-id="1e593-129">Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Dokumentruting > Dokumentrutingsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="1e593-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="1e593-130">Aktiver SSCC-oppsettet.</span><span class="sxs-lookup"><span data-stu-id="1e593-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="1e593-131">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1e593-131">Select **New**.</span></span>
3. <span data-ttu-id="1e593-132">Skriv inn en verdi i feltet **Oppsett-ID**.</span><span class="sxs-lookup"><span data-stu-id="1e593-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="1e593-133">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1e593-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="1e593-134">Velg **Sett inn i slutten av teksten**.</span><span class="sxs-lookup"><span data-stu-id="1e593-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="1e593-135">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="1e593-135">Select **Save**.</span></span>
7. <span data-ttu-id="1e593-136">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1e593-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="1e593-137">Konfigurer dokumentrutingen</span><span class="sxs-lookup"><span data-stu-id="1e593-137">Set up the document routing</span></span>
1. <span data-ttu-id="1e593-138">Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Dokumentruting > Dokumentruting**.</span><span class="sxs-lookup"><span data-stu-id="1e593-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="1e593-139">Velg et alternativ i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="1e593-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="1e593-140">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1e593-140">Select **New**.</span></span>
4. <span data-ttu-id="1e593-141">Skriv inn en verdi i **Lager**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1e593-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="1e593-142">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1e593-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="1e593-143">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1e593-143">Select **New**.</span></span>
7. <span data-ttu-id="1e593-144">Angi eller velg en verdi i feltet **Oppsett-ID**.</span><span class="sxs-lookup"><span data-stu-id="1e593-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="1e593-145">I **Navn**-feltet angir du navnet på skriveren du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="1e593-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="1e593-146">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="1e593-146">Select **Save**.</span></span>
10. <span data-ttu-id="1e593-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1e593-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="1e593-148">Opprett mobilenhetsmeny</span><span class="sxs-lookup"><span data-stu-id="1e593-148">Create mobile device menu</span></span>
1. <span data-ttu-id="1e593-149">Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Mobilenhet > Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="1e593-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="1e593-150">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1e593-150">Select **New**.</span></span>
3. <span data-ttu-id="1e593-151">Skriv inn en verdi i feltet **Menyelementnavn**.</span><span class="sxs-lookup"><span data-stu-id="1e593-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="1e593-152">Skriv inn en verdi i **Tittel**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1e593-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="1e593-153">Velg et alternativ i **Modus**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1e593-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="1e593-154">Velg **Ja** i feltet **Bruk eksisterende arbeid**.</span><span class="sxs-lookup"><span data-stu-id="1e593-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="1e593-155">Velg **Ja** i **Generer nummerskilt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1e593-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="1e593-156">Utvid **Arbeidsklasser**-delen.</span><span class="sxs-lookup"><span data-stu-id="1e593-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="1e593-157">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1e593-157">Select **New**.</span></span>
10. <span data-ttu-id="1e593-158">Skriv inn en verdi i feltet **Arbeidsklasse-ID**.</span><span class="sxs-lookup"><span data-stu-id="1e593-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="1e593-159">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="1e593-159">Select **Save**.</span></span>
12. <span data-ttu-id="1e593-160">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1e593-160">Close the page.</span></span>
13. <span data-ttu-id="1e593-161">Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Mobilenhet > Meny på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="1e593-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="1e593-162">Velg menyelementet du opprettet tidligere, i treet.</span><span class="sxs-lookup"><span data-stu-id="1e593-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="1e593-163">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="1e593-163">Select **Edit**.</span></span>
16. <span data-ttu-id="1e593-164">Velg pilen for å legge til menyelementet i menyen.</span><span class="sxs-lookup"><span data-stu-id="1e593-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="1e593-165">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="1e593-165">Select **Save**.</span></span>
18. <span data-ttu-id="1e593-166">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1e593-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="1e593-167">Oppdater en arbeidsmal</span><span class="sxs-lookup"><span data-stu-id="1e593-167">Update a work template</span></span>
1. <span data-ttu-id="1e593-168">Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Arbeid > Arbeidsmaler**.</span><span class="sxs-lookup"><span data-stu-id="1e593-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="1e593-169">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="1e593-169">Select **Edit**.</span></span>
3. <span data-ttu-id="1e593-170">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1e593-170">Select **New**.</span></span>
4. <span data-ttu-id="1e593-171">Velg **Skriv ut** i **Arbeidstype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1e593-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="1e593-172">Angi eller velg en verdi i feltet **Arbeidsklasse-ID**.</span><span class="sxs-lookup"><span data-stu-id="1e593-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="1e593-173">Velg **Flytt opp**.</span><span class="sxs-lookup"><span data-stu-id="1e593-173">Select **Move up**.</span></span>
7. <span data-ttu-id="1e593-174">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="1e593-174">Select **Save**.</span></span>
8. <span data-ttu-id="1e593-175">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1e593-175">Close the page.</span></span>

