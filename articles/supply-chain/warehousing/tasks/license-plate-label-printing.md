---
title: Aktivere utskrift av nummerskiltetikett
description: Dette emnet viser hvordan du aktiverer automatisk utskrift av en SSCC-etikett (Serial Shipping Container Code) etter at den siste varen er plukket fra lageret i en arbeidsprosess for salgsplukk.
author: perlynne
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 43dc913e84fa53179855d7ab8dbbf4d179e2cc63
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383050"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="ab91d-103">Aktivere utskrift av nummerskiltetikett</span><span class="sxs-lookup"><span data-stu-id="ab91d-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ab91d-104">Dette emnet viser hvordan du aktiverer automatisk utskrift av en SSCC-etikett (Serial Shipping Container Code) etter at den siste varen er plukket fra lageret i en arbeidsprosess for salgsplukk.</span><span class="sxs-lookup"><span data-stu-id="ab91d-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="ab91d-105">Du kan kjøre denne prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="ab91d-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="ab91d-106">Hvis du skal kjøre det på dine egne data, må du ha en nummerserie som er definert for nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="ab91d-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="ab91d-107">Du må definere en etikettskriver før du begynner.</span><span class="sxs-lookup"><span data-stu-id="ab91d-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="ab91d-108">Gå til Organisasjonsstyring > Oppsett > Nettverksskrivere.</span><span class="sxs-lookup"><span data-stu-id="ab91d-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="ab91d-109">I handlingsruten velger du Alternativer, og deretter klikker du Last ned installasjonsprogram for dokumentrutingsagent.</span><span class="sxs-lookup"><span data-stu-id="ab91d-109">On the Action Pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="ab91d-110">Kjør installasjonsprogrammet og kontroller at du har en fungerende skriver satt til Aktiv før du fortsetter med prosedyren.</span><span class="sxs-lookup"><span data-stu-id="ab91d-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="ab91d-111">Angi GS1-firmaprefikset</span><span class="sxs-lookup"><span data-stu-id="ab91d-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="ab91d-112">Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Lagerstyringsparametere**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="ab91d-113">I feltet **GS1-firmaprefiks** angir du det 7-sifrede GS1-firmanummeret.</span><span class="sxs-lookup"><span data-stu-id="ab91d-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="ab91d-114">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-114">Select **Save**.</span></span>
4. <span data-ttu-id="ab91d-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ab91d-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="ab91d-116">Konfigurasjon av nummerserien for SSCC-skiltnummeret</span><span class="sxs-lookup"><span data-stu-id="ab91d-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="ab91d-117">Gå til **Navigasjonsrute > Moduler > Organisasjonsadministrasjon > Nummerserier > Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="ab91d-118">Velg et alternativ i **Område**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ab91d-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="ab91d-119">Velg et alternativ i **Referanse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ab91d-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="ab91d-120">Skriv inn en verdi i feltet **Firma.**</span><span class="sxs-lookup"><span data-stu-id="ab91d-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="ab91d-121">Utvid seksjonen **Segmenter**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="ab91d-122">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-122">Select **Edit**.</span></span>
7. <span data-ttu-id="ab91d-123">Merk den første raden i tabellen **Segmenter**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="ab91d-124">Velg **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-124">Select **Remove**.</span></span>
9. <span data-ttu-id="ab91d-125">Velg **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-125">Select **Remove**.</span></span>
10. <span data-ttu-id="ab91d-126">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-126">Select **Save**.</span></span>
11. <span data-ttu-id="ab91d-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ab91d-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="ab91d-128">Opprett dokumentruteoppsettet</span><span class="sxs-lookup"><span data-stu-id="ab91d-128">Create the document route layout</span></span>
1. <span data-ttu-id="ab91d-129">Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Dokumentruting > Dokumentrutingsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="ab91d-130">Aktiver SSCC-oppsettet.</span><span class="sxs-lookup"><span data-stu-id="ab91d-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="ab91d-131">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-131">Select **New**.</span></span>
3. <span data-ttu-id="ab91d-132">Skriv inn en verdi i feltet **Oppsett-ID**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="ab91d-133">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ab91d-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="ab91d-134">Velg **Sett inn i slutten av teksten**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="ab91d-135">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-135">Select **Save**.</span></span>
7. <span data-ttu-id="ab91d-136">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ab91d-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="ab91d-137">Konfigurer dokumentrutingen</span><span class="sxs-lookup"><span data-stu-id="ab91d-137">Set up the document routing</span></span>
1. <span data-ttu-id="ab91d-138">Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Dokumentruting > Dokumentruting**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="ab91d-139">Velg et alternativ i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="ab91d-140">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-140">Select **New**.</span></span>
4. <span data-ttu-id="ab91d-141">Skriv inn en verdi i **Lager**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ab91d-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="ab91d-142">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ab91d-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="ab91d-143">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-143">Select **New**.</span></span>
7. <span data-ttu-id="ab91d-144">Angi eller velg en verdi i feltet **Oppsett-ID**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="ab91d-145">I **Navn**-feltet angir du navnet på skriveren du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="ab91d-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="ab91d-146">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-146">Select **Save**.</span></span>
10. <span data-ttu-id="ab91d-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ab91d-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="ab91d-148">Opprett mobilenhetsmeny</span><span class="sxs-lookup"><span data-stu-id="ab91d-148">Create mobile device menu</span></span>
1. <span data-ttu-id="ab91d-149">Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Mobilenhet > Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="ab91d-150">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-150">Select **New**.</span></span>
3. <span data-ttu-id="ab91d-151">Skriv inn en verdi i feltet **Menyelementnavn**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="ab91d-152">Skriv inn en verdi i **Tittel**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ab91d-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="ab91d-153">Velg et alternativ i **Modus**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ab91d-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="ab91d-154">Velg **Ja** i feltet **Bruk eksisterende arbeid**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="ab91d-155">Velg **Ja** i **Generer nummerskilt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ab91d-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="ab91d-156">Utvid **Arbeidsklasser**-delen.</span><span class="sxs-lookup"><span data-stu-id="ab91d-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="ab91d-157">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-157">Select **New**.</span></span>
10. <span data-ttu-id="ab91d-158">Skriv inn en verdi i feltet **Arbeidsklasse-ID**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="ab91d-159">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-159">Select **Save**.</span></span>
12. <span data-ttu-id="ab91d-160">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ab91d-160">Close the page.</span></span>
13. <span data-ttu-id="ab91d-161">Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Mobilenhet > Meny på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="ab91d-162">Velg menyelementet du opprettet tidligere, i treet.</span><span class="sxs-lookup"><span data-stu-id="ab91d-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="ab91d-163">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-163">Select **Edit**.</span></span>
16. <span data-ttu-id="ab91d-164">Velg pilen for å legge til menyelementet i menyen.</span><span class="sxs-lookup"><span data-stu-id="ab91d-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="ab91d-165">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-165">Select **Save**.</span></span>
18. <span data-ttu-id="ab91d-166">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ab91d-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="ab91d-167">Oppdater en arbeidsmal</span><span class="sxs-lookup"><span data-stu-id="ab91d-167">Update a work template</span></span>
1. <span data-ttu-id="ab91d-168">Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Arbeid > Arbeidsmaler**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="ab91d-169">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-169">Select **Edit**.</span></span>
3. <span data-ttu-id="ab91d-170">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-170">Select **New**.</span></span>
4. <span data-ttu-id="ab91d-171">Velg **Skriv ut** i **Arbeidstype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ab91d-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="ab91d-172">Angi eller velg en verdi i feltet **Arbeidsklasse-ID**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="ab91d-173">Velg **Flytt opp**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-173">Select **Move up**.</span></span>
7. <span data-ttu-id="ab91d-174">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ab91d-174">Select **Save**.</span></span>
8. <span data-ttu-id="ab91d-175">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ab91d-175">Close the page.</span></span>

