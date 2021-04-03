---
title: ER Konfigurere format for å utføre telling og summering (del 4 - Kjøre format)
description: Dette emnet beskriver hvordan du konfigurerer et elektronisk rapporteringsformat som teller og summerer basert på data fra tekstutdataene som allerede er generert. (Del 4)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ca8449581edc06016b6e387880aad91087b67f1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565423"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="2feba-104">ER Konfigurere format for å utføre telling og summering (del 4 - Kjøre format)</span><span class="sxs-lookup"><span data-stu-id="2feba-104">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2feba-105">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata.</span><span class="sxs-lookup"><span data-stu-id="2feba-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="2feba-106">Denne fremgangsmåten kan utføres i firmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="2feba-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="2feba-107">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Konfigurere format for å utføre telling og summering (del 3: Bruke beregninger for å lage utdata)".</span><span class="sxs-lookup"><span data-stu-id="2feba-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="2feba-108">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="2feba-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="2feba-109">Teste denne konfigurasjonen for generering av Intrastat-rapporter</span><span class="sxs-lookup"><span data-stu-id="2feba-109">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="2feba-110">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="2feba-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="2feba-111">Klikk på Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="2feba-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="2feba-112">Utvid Intrastat-modell i treet.</span><span class="sxs-lookup"><span data-stu-id="2feba-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="2feba-113">Utvid Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="2feba-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="2feba-114">Velg Intrastat-modell\Intrastat (DE)\Intrastat (DE) med telling og summering i treet.</span><span class="sxs-lookup"><span data-stu-id="2feba-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="2feba-115">Klikk på Konfigurasjoner i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2feba-115">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="2feba-116">Klikk på Brukerparametere.</span><span class="sxs-lookup"><span data-stu-id="2feba-116">Click User parameters.</span></span>
8. <span data-ttu-id="2feba-117">Velg Ja i feltet Kjøringsinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="2feba-117">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="2feba-118">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="2feba-118">Click OK.</span></span>
10. <span data-ttu-id="2feba-119">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="2feba-119">Click Edit.</span></span>
11. <span data-ttu-id="2feba-120">Velg Ja i feltet Kjøringsutkast.</span><span class="sxs-lookup"><span data-stu-id="2feba-120">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="2feba-121">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="2feba-121">Click Save.</span></span>
13. <span data-ttu-id="2feba-122">Gå til Avgift > Oppsett > Utenrikshandel > Utenrikshandelsparametere.</span><span class="sxs-lookup"><span data-stu-id="2feba-122">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="2feba-123">Utvid delen Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="2feba-123">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="2feba-124">Velg konfigurasjonen Intrastat (DE) med telling og summering.</span><span class="sxs-lookup"><span data-stu-id="2feba-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="2feba-125">Velg konfigurasjonen Intrastat (DE) med telling og summering.</span><span class="sxs-lookup"><span data-stu-id="2feba-125">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="2feba-126">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="2feba-126">Click Save.</span></span>
18. <span data-ttu-id="2feba-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2feba-127">Close the page.</span></span>
19. <span data-ttu-id="2feba-128">Gå til Avgift > Deklareringer > Utenrikshandel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="2feba-128">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="2feba-129">Klikk på Utlevering.</span><span class="sxs-lookup"><span data-stu-id="2feba-129">Click Output.</span></span>
21. <span data-ttu-id="2feba-130">Klikk på Rapport.</span><span class="sxs-lookup"><span data-stu-id="2feba-130">Click Report.</span></span>
    * <span data-ttu-id="2feba-131">Kjør prosessen for generering av Intrastat-rapport.</span><span class="sxs-lookup"><span data-stu-id="2feba-131">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="2feba-132">Angi datoen som 2000-01-01 i feltet Fra dato.</span><span class="sxs-lookup"><span data-stu-id="2feba-132">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="2feba-133">Definer start- og sluttdatoer for rapporteringsperioden som inkluderer eksisterende på skjematransaksjonene.</span><span class="sxs-lookup"><span data-stu-id="2feba-133">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="2feba-134">Angi datoen som 2022-12-31 i feltet Til dato.</span><span class="sxs-lookup"><span data-stu-id="2feba-134">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="2feba-135">Definer start- og sluttdatoer for rapporteringsperioden som inkluderer eksisterende på skjematransaksjonene.</span><span class="sxs-lookup"><span data-stu-id="2feba-135">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="2feba-136">Velg Ankomster i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="2feba-136">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="2feba-137">Velg Ja i feltet Generer fil.</span><span class="sxs-lookup"><span data-stu-id="2feba-137">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="2feba-138">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="2feba-138">Click OK.</span></span>
    * <span data-ttu-id="2feba-139">Se gjennom de opprettede utdataene med summeringslinjene på slutten.</span><span class="sxs-lookup"><span data-stu-id="2feba-139">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="2feba-140">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="2feba-140">Click New.</span></span>
28. <span data-ttu-id="2feba-141">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2feba-141">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="2feba-142">Velg Fordelinger i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="2feba-142">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="2feba-143">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="2feba-143">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="2feba-144">Angi eller velg en verdi i feltet Artikkel.</span><span class="sxs-lookup"><span data-stu-id="2feba-144">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="2feba-145">Sett vekt til 10.</span><span class="sxs-lookup"><span data-stu-id="2feba-145">Set Weight to '10'.</span></span>
33. <span data-ttu-id="2feba-146">Sett fakturabeløp til 10 000.</span><span class="sxs-lookup"><span data-stu-id="2feba-146">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="2feba-147">Sett statistisk beløp til 10 000.</span><span class="sxs-lookup"><span data-stu-id="2feba-147">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="2feba-148">Klikk på Utlevering.</span><span class="sxs-lookup"><span data-stu-id="2feba-148">Click Output.</span></span>
36. <span data-ttu-id="2feba-149">Klikk på Rapport.</span><span class="sxs-lookup"><span data-stu-id="2feba-149">Click Report.</span></span>
37. <span data-ttu-id="2feba-150">Velg Fordelinger i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="2feba-150">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="2feba-151">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="2feba-151">Click OK.</span></span>
    * <span data-ttu-id="2feba-152">Se gjennom de opprettede utdataene med summeringslinjene på slutten.</span><span class="sxs-lookup"><span data-stu-id="2feba-152">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="2feba-153">Vær oppmerksom på at det har blitt endret sammenlignet med første kjøring.</span><span class="sxs-lookup"><span data-stu-id="2feba-153">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="2feba-154">Kjøre denne konfigurasjonen i feilsøkingsmodus for å gå gjennom innsamlede tellings- og summeringsdata</span><span class="sxs-lookup"><span data-stu-id="2feba-154">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="2feba-155">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="2feba-155">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="2feba-156">Utvid Intrastat-modell i treet.</span><span class="sxs-lookup"><span data-stu-id="2feba-156">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="2feba-157">Utvid Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="2feba-157">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="2feba-158">Velg Intrastat-modell\Intrastat (DE)\Intrastat (DE) med telling og summering i treet.</span><span class="sxs-lookup"><span data-stu-id="2feba-158">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="2feba-159">Klikk på Konfigurasjoner i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2feba-159">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="2feba-160">Klikk på Brukerparametere.</span><span class="sxs-lookup"><span data-stu-id="2feba-160">Click User parameters.</span></span>
7. <span data-ttu-id="2feba-161">Velg Ja i feltet Kjør i feilsøkingsmodus.</span><span class="sxs-lookup"><span data-stu-id="2feba-161">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="2feba-162">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="2feba-162">Click OK.</span></span>
9. <span data-ttu-id="2feba-163">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2feba-163">Close the page.</span></span>
10. <span data-ttu-id="2feba-164">Gå til Avgift > Deklareringer > Utenrikshandel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="2feba-164">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="2feba-165">Klikk på Utlevering.</span><span class="sxs-lookup"><span data-stu-id="2feba-165">Click Output.</span></span>
12. <span data-ttu-id="2feba-166">Klikk på Rapport.</span><span class="sxs-lookup"><span data-stu-id="2feba-166">Click Report.</span></span>
13. <span data-ttu-id="2feba-167">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="2feba-167">Click OK.</span></span>
14. <span data-ttu-id="2feba-168">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2feba-168">Close the page.</span></span>
15. <span data-ttu-id="2feba-169">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="2feba-169">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="2feba-170">Utvid Intrastat-modell i treet.</span><span class="sxs-lookup"><span data-stu-id="2feba-170">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="2feba-171">Utvid Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="2feba-171">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="2feba-172">Velg Intrastat-modell\Intrastat (DE)\Intrastat (DE) med telling og summering i treet.</span><span class="sxs-lookup"><span data-stu-id="2feba-172">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="2feba-173">Klikk på Feilsøkingslogger.</span><span class="sxs-lookup"><span data-stu-id="2feba-173">Click Debug logs.</span></span>
    * <span data-ttu-id="2feba-174">Vær oppmerksom på at det er opprettet en feilsøkingsloggpost for kjøringen av den valgte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="2feba-174">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="2feba-175">Klikk på Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="2feba-175">Click Attach.</span></span>
21. <span data-ttu-id="2feba-176">Klikk på Åpne.</span><span class="sxs-lookup"><span data-stu-id="2feba-176">Click Open.</span></span>
    * <span data-ttu-id="2feba-177">Se gjennom den opprettede XML-filen som inneholder tellings- og summeringsdetaljer som ble samlet inn under kjøringen av den valgte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="2feba-177">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]