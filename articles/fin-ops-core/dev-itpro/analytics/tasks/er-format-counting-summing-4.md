---
title: ER Konfigurere format for å utføre telling og summering (del 4 - Kjøre format)
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0a80e5b1a79c874ce0a8d24c85be71d0dc5c9c8
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550562"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="00f39-103">ER Konfigurere format for å utføre telling og summering (del 4 - Kjøre format)</span><span class="sxs-lookup"><span data-stu-id="00f39-103">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="00f39-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata.</span><span class="sxs-lookup"><span data-stu-id="00f39-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="00f39-105">Denne fremgangsmåten kan utføres i firmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="00f39-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="00f39-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Konfigurere format for å utføre telling og summering (del 3: Bruke beregninger for å lage utdata)".</span><span class="sxs-lookup"><span data-stu-id="00f39-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="00f39-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="00f39-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="00f39-108">Teste denne konfigurasjonen for generering av Intrastat-rapporter</span><span class="sxs-lookup"><span data-stu-id="00f39-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="00f39-109">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="00f39-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="00f39-110">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="00f39-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="00f39-111">Utvid Intrastat-modell i treet.</span><span class="sxs-lookup"><span data-stu-id="00f39-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="00f39-112">Utvid Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="00f39-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="00f39-113">Velg Intrastat-modell\Intrastat (DE)\Intrastat (DE) med telling og summering i treet.</span><span class="sxs-lookup"><span data-stu-id="00f39-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="00f39-114">Klikk Konfigurasjoner i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="00f39-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="00f39-115">Klikk Brukerparametere.</span><span class="sxs-lookup"><span data-stu-id="00f39-115">Click User parameters.</span></span>
8. <span data-ttu-id="00f39-116">Velg Ja i feltet Kjøringsinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="00f39-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="00f39-117">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="00f39-117">Click OK.</span></span>
10. <span data-ttu-id="00f39-118">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="00f39-118">Click Edit.</span></span>
11. <span data-ttu-id="00f39-119">Velg Ja i feltet Kjøringsutkast.</span><span class="sxs-lookup"><span data-stu-id="00f39-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="00f39-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="00f39-120">Click Save.</span></span>
13. <span data-ttu-id="00f39-121">Gå til Avgift > Oppsett > Utenrikshandel > Utenrikshandelsparametere.</span><span class="sxs-lookup"><span data-stu-id="00f39-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="00f39-122">Utvid delen Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="00f39-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="00f39-123">Velg konfigurasjonen Intrastat (DE) med telling og summering.</span><span class="sxs-lookup"><span data-stu-id="00f39-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="00f39-124">Velg konfigurasjonen Intrastat (DE) med telling og summering.</span><span class="sxs-lookup"><span data-stu-id="00f39-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="00f39-125">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="00f39-125">Click Save.</span></span>
18. <span data-ttu-id="00f39-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="00f39-126">Close the page.</span></span>
19. <span data-ttu-id="00f39-127">Gå til Avgift > Deklareringer > Utenrikshandel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="00f39-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="00f39-128">Klikk Utlevering.</span><span class="sxs-lookup"><span data-stu-id="00f39-128">Click Output.</span></span>
21. <span data-ttu-id="00f39-129">Klikk Rapport.</span><span class="sxs-lookup"><span data-stu-id="00f39-129">Click Report.</span></span>
    * <span data-ttu-id="00f39-130">Kjør prosessen for generering av Intrastat-rapport.</span><span class="sxs-lookup"><span data-stu-id="00f39-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="00f39-131">Angi datoen som 2000-01-01 i feltet Fra dato.</span><span class="sxs-lookup"><span data-stu-id="00f39-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="00f39-132">Definer start- og sluttdatoer for rapporteringsperioden som inkluderer eksisterende på skjematransaksjonene.</span><span class="sxs-lookup"><span data-stu-id="00f39-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="00f39-133">Angi datoen som 2022-12-31 i feltet Til dato.</span><span class="sxs-lookup"><span data-stu-id="00f39-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="00f39-134">Definer start- og sluttdatoer for rapporteringsperioden som inkluderer eksisterende på skjematransaksjonene.</span><span class="sxs-lookup"><span data-stu-id="00f39-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="00f39-135">Velg Ankomster i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="00f39-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="00f39-136">Velg Ja i feltet Generer fil.</span><span class="sxs-lookup"><span data-stu-id="00f39-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="00f39-137">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="00f39-137">Click OK.</span></span>
    * <span data-ttu-id="00f39-138">Se gjennom de opprettede utdataene med summeringslinjene på slutten.</span><span class="sxs-lookup"><span data-stu-id="00f39-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="00f39-139">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="00f39-139">Click New.</span></span>
28. <span data-ttu-id="00f39-140">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="00f39-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="00f39-141">Velg Fordelinger i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="00f39-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="00f39-142">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="00f39-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="00f39-143">Angi eller velg en verdi i feltet Artikkel.</span><span class="sxs-lookup"><span data-stu-id="00f39-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="00f39-144">Sett vekt til 10.</span><span class="sxs-lookup"><span data-stu-id="00f39-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="00f39-145">Sett fakturabeløp til 10 000.</span><span class="sxs-lookup"><span data-stu-id="00f39-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="00f39-146">Sett statistisk beløp til 10 000.</span><span class="sxs-lookup"><span data-stu-id="00f39-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="00f39-147">Klikk Utlevering.</span><span class="sxs-lookup"><span data-stu-id="00f39-147">Click Output.</span></span>
36. <span data-ttu-id="00f39-148">Klikk Rapport.</span><span class="sxs-lookup"><span data-stu-id="00f39-148">Click Report.</span></span>
37. <span data-ttu-id="00f39-149">Velg Fordelinger i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="00f39-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="00f39-150">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="00f39-150">Click OK.</span></span>
    * <span data-ttu-id="00f39-151">Se gjennom de opprettede utdataene med summeringslinjene på slutten.</span><span class="sxs-lookup"><span data-stu-id="00f39-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="00f39-152">Vær oppmerksom på at det har blitt endret sammenlignet med første kjøring.</span><span class="sxs-lookup"><span data-stu-id="00f39-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="00f39-153">Kjøre denne konfigurasjonen i feilsøkingsmodus for å gå gjennom innsamlede tellings- og summeringsdata</span><span class="sxs-lookup"><span data-stu-id="00f39-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="00f39-154">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="00f39-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="00f39-155">Utvid Intrastat-modell i treet.</span><span class="sxs-lookup"><span data-stu-id="00f39-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="00f39-156">Utvid Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="00f39-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="00f39-157">Velg Intrastat-modell\Intrastat (DE)\Intrastat (DE) med telling og summering i treet.</span><span class="sxs-lookup"><span data-stu-id="00f39-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="00f39-158">Klikk Konfigurasjoner i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="00f39-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="00f39-159">Klikk Brukerparametere.</span><span class="sxs-lookup"><span data-stu-id="00f39-159">Click User parameters.</span></span>
7. <span data-ttu-id="00f39-160">Velg Ja i feltet Kjør i feilsøkingsmodus.</span><span class="sxs-lookup"><span data-stu-id="00f39-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="00f39-161">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="00f39-161">Click OK.</span></span>
9. <span data-ttu-id="00f39-162">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="00f39-162">Close the page.</span></span>
10. <span data-ttu-id="00f39-163">Gå til Avgift > Deklareringer > Utenrikshandel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="00f39-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="00f39-164">Klikk Utlevering.</span><span class="sxs-lookup"><span data-stu-id="00f39-164">Click Output.</span></span>
12. <span data-ttu-id="00f39-165">Klikk Rapport.</span><span class="sxs-lookup"><span data-stu-id="00f39-165">Click Report.</span></span>
13. <span data-ttu-id="00f39-166">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="00f39-166">Click OK.</span></span>
14. <span data-ttu-id="00f39-167">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="00f39-167">Close the page.</span></span>
15. <span data-ttu-id="00f39-168">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="00f39-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="00f39-169">Utvid Intrastat-modell i treet.</span><span class="sxs-lookup"><span data-stu-id="00f39-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="00f39-170">Utvid Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="00f39-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="00f39-171">Velg Intrastat-modell\Intrastat (DE)\Intrastat (DE) med telling og summering i treet.</span><span class="sxs-lookup"><span data-stu-id="00f39-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="00f39-172">Klikk Feilsøkingslogger.</span><span class="sxs-lookup"><span data-stu-id="00f39-172">Click Debug logs.</span></span>
    * <span data-ttu-id="00f39-173">Vær oppmerksom på at det er opprettet en feilsøkingsloggpost for kjøringen av den valgte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="00f39-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="00f39-174">Klikk Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="00f39-174">Click Attach.</span></span>
21. <span data-ttu-id="00f39-175">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="00f39-175">Click Open.</span></span>
    * <span data-ttu-id="00f39-176">Se gjennom den opprettede XML-filen som inneholder tellings- og summeringsdetaljer som ble samlet inn under kjøringen av den valgte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="00f39-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

