--- 
title: "Kjøre formatet for å utføre telling og summering for elektronisk rapportering (ER)"
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 9f5520dc4e1eddc2fc52a05e5dc386b982d8f5ad
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="run-the-format-to-do-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="af8dd-103">Kjøre formatet for å utføre telling og summering for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="af8dd-103">Run the format to do counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af8dd-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata.</span><span class="sxs-lookup"><span data-stu-id="af8dd-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="af8dd-105">Denne fremgangsmåten kan utføres i firmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="af8dd-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="af8dd-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Konfigurere format for å utføre telling og summering (del 3: Bruke beregninger for å lage utdata)".</span><span class="sxs-lookup"><span data-stu-id="af8dd-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="af8dd-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="af8dd-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="af8dd-108">Teste denne konfigurasjonen for generering av Intrastat-rapporter</span><span class="sxs-lookup"><span data-stu-id="af8dd-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="af8dd-109">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="af8dd-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="af8dd-110">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="af8dd-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="af8dd-111">Utvid Intrastat-modell i treet.</span><span class="sxs-lookup"><span data-stu-id="af8dd-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="af8dd-112">Utvid Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="af8dd-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="af8dd-113">Velg Intrastat-modell\Intrastat (DE)\Intrastat (DE) med telling og summering i treet.</span><span class="sxs-lookup"><span data-stu-id="af8dd-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="af8dd-114">Klikk Konfigurasjoner i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="af8dd-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="af8dd-115">Klikk Brukerparametere.</span><span class="sxs-lookup"><span data-stu-id="af8dd-115">Click User parameters.</span></span>
8. <span data-ttu-id="af8dd-116">Velg Ja i feltet Kjøringsinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="af8dd-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="af8dd-117">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="af8dd-117">Click OK.</span></span>
10. <span data-ttu-id="af8dd-118">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="af8dd-118">Click Edit.</span></span>
11. <span data-ttu-id="af8dd-119">Velg Ja i feltet Kjøringsutkast.</span><span class="sxs-lookup"><span data-stu-id="af8dd-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="af8dd-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="af8dd-120">Click Save.</span></span>
13. <span data-ttu-id="af8dd-121">Gå til Avgift > Oppsett > Utenrikshandel > Utenrikshandelsparametere.</span><span class="sxs-lookup"><span data-stu-id="af8dd-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="af8dd-122">Utvid delen Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="af8dd-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="af8dd-123">Velg konfigurasjonen Intrastat (DE) med telling og summering.</span><span class="sxs-lookup"><span data-stu-id="af8dd-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="af8dd-124">Velg konfigurasjonen Intrastat (DE) med telling og summering.</span><span class="sxs-lookup"><span data-stu-id="af8dd-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="af8dd-125">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="af8dd-125">Click Save.</span></span>
18. <span data-ttu-id="af8dd-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="af8dd-126">Close the page.</span></span>
19. <span data-ttu-id="af8dd-127">Gå til Avgift > Deklareringer > Utenrikshandel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="af8dd-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="af8dd-128">Klikk Utlevering.</span><span class="sxs-lookup"><span data-stu-id="af8dd-128">Click Output.</span></span>
21. <span data-ttu-id="af8dd-129">Klikk Rapport.</span><span class="sxs-lookup"><span data-stu-id="af8dd-129">Click Report.</span></span>
    * <span data-ttu-id="af8dd-130">Kjør prosessen for generering av Intrastat-rapport.</span><span class="sxs-lookup"><span data-stu-id="af8dd-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="af8dd-131">Angi datoen som 2000-01-01 i feltet Fra dato.</span><span class="sxs-lookup"><span data-stu-id="af8dd-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="af8dd-132">Definer start- og sluttdatoer for rapporteringsperioden som inkluderer eksisterende på skjematransaksjonene.</span><span class="sxs-lookup"><span data-stu-id="af8dd-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="af8dd-133">Angi datoen som 2022-12-31 i feltet Til dato.</span><span class="sxs-lookup"><span data-stu-id="af8dd-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="af8dd-134">Definer start- og sluttdatoer for rapporteringsperioden som inkluderer eksisterende på skjematransaksjonene.</span><span class="sxs-lookup"><span data-stu-id="af8dd-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="af8dd-135">Velg Ankomster i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="af8dd-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="af8dd-136">Velg Ja i feltet Generer fil.</span><span class="sxs-lookup"><span data-stu-id="af8dd-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="af8dd-137">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="af8dd-137">Click OK.</span></span>
    * <span data-ttu-id="af8dd-138">Se gjennom de opprettede utdataene med summeringslinjene på slutten.</span><span class="sxs-lookup"><span data-stu-id="af8dd-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="af8dd-139">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="af8dd-139">Click New.</span></span>
28. <span data-ttu-id="af8dd-140">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="af8dd-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="af8dd-141">Velg Fordelinger i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="af8dd-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="af8dd-142">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="af8dd-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="af8dd-143">Angi eller velg en verdi i feltet Artikkel.</span><span class="sxs-lookup"><span data-stu-id="af8dd-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="af8dd-144">Sett vekt til 10.</span><span class="sxs-lookup"><span data-stu-id="af8dd-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="af8dd-145">Sett fakturabeløp til 10 000.</span><span class="sxs-lookup"><span data-stu-id="af8dd-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="af8dd-146">Sett statistisk beløp til 10 000.</span><span class="sxs-lookup"><span data-stu-id="af8dd-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="af8dd-147">Klikk Utlevering.</span><span class="sxs-lookup"><span data-stu-id="af8dd-147">Click Output.</span></span>
36. <span data-ttu-id="af8dd-148">Klikk Rapport.</span><span class="sxs-lookup"><span data-stu-id="af8dd-148">Click Report.</span></span>
37. <span data-ttu-id="af8dd-149">Velg Fordelinger i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="af8dd-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="af8dd-150">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="af8dd-150">Click OK.</span></span>
    * <span data-ttu-id="af8dd-151">Se gjennom de opprettede utdataene med summeringslinjene på slutten.</span><span class="sxs-lookup"><span data-stu-id="af8dd-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="af8dd-152">Vær oppmerksom på at det har blitt endret sammenlignet med første kjøring.</span><span class="sxs-lookup"><span data-stu-id="af8dd-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="af8dd-153">Kjøre denne konfigurasjonen i feilsøkingsmodus for å gå gjennom innsamlede tellings- og summeringsdata</span><span class="sxs-lookup"><span data-stu-id="af8dd-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="af8dd-154">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="af8dd-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="af8dd-155">Utvid Intrastat-modell i treet.</span><span class="sxs-lookup"><span data-stu-id="af8dd-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="af8dd-156">Utvid Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="af8dd-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="af8dd-157">Velg Intrastat-modell\Intrastat (DE)\Intrastat (DE) med telling og summering i treet.</span><span class="sxs-lookup"><span data-stu-id="af8dd-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="af8dd-158">Klikk Konfigurasjoner i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="af8dd-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="af8dd-159">Klikk Brukerparametere.</span><span class="sxs-lookup"><span data-stu-id="af8dd-159">Click User parameters.</span></span>
7. <span data-ttu-id="af8dd-160">Velg Ja i feltet Kjør i feilsøkingsmodus.</span><span class="sxs-lookup"><span data-stu-id="af8dd-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="af8dd-161">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="af8dd-161">Click OK.</span></span>
9. <span data-ttu-id="af8dd-162">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="af8dd-162">Close the page.</span></span>
10. <span data-ttu-id="af8dd-163">Gå til Avgift > Deklareringer > Utenrikshandel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="af8dd-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="af8dd-164">Klikk Utlevering.</span><span class="sxs-lookup"><span data-stu-id="af8dd-164">Click Output.</span></span>
12. <span data-ttu-id="af8dd-165">Klikk Rapport.</span><span class="sxs-lookup"><span data-stu-id="af8dd-165">Click Report.</span></span>
13. <span data-ttu-id="af8dd-166">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="af8dd-166">Click OK.</span></span>
14. <span data-ttu-id="af8dd-167">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="af8dd-167">Close the page.</span></span>
15. <span data-ttu-id="af8dd-168">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="af8dd-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="af8dd-169">Utvid Intrastat-modell i treet.</span><span class="sxs-lookup"><span data-stu-id="af8dd-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="af8dd-170">Utvid Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="af8dd-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="af8dd-171">Velg Intrastat-modell\Intrastat (DE)\Intrastat (DE) med telling og summering i treet.</span><span class="sxs-lookup"><span data-stu-id="af8dd-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="af8dd-172">Klikk Feilsøkingslogger.</span><span class="sxs-lookup"><span data-stu-id="af8dd-172">Click Debug logs.</span></span>
    * <span data-ttu-id="af8dd-173">Vær oppmerksom på at det er opprettet en feilsøkingsloggpost for kjøringen av den valgte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="af8dd-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="af8dd-174">Klikk Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="af8dd-174">Click Attach.</span></span>
21. <span data-ttu-id="af8dd-175">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="af8dd-175">Click Open.</span></span>
    * <span data-ttu-id="af8dd-176">Se gjennom den opprettede XML-filen som inneholder tellings- og summeringsdetaljer som ble samlet inn under kjøringen av den valgte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="af8dd-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  


