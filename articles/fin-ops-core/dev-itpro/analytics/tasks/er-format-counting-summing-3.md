---
title: ER Konfigurere format for å utføre telling og summering (del 3 - Bruke beregninger for å lage utdataene)
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7bbef7048488056f50ec8967a9af53d468666856
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550769"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="6c210-103">ER Konfigurere format for å utføre telling og summering (del 3 - Bruke beregninger for å lage utdataene)</span><span class="sxs-lookup"><span data-stu-id="6c210-103">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6c210-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata.</span><span class="sxs-lookup"><span data-stu-id="6c210-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="6c210-105">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="6c210-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="6c210-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Konfigurere format for å utføre telling og summering (del 2: Konfigurere beregninger)".</span><span class="sxs-lookup"><span data-stu-id="6c210-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="6c210-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="6c210-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="6c210-108">Konfigurere denne rapporten for å bruke tellings- og summeringsinformasjon</span><span class="sxs-lookup"><span data-stu-id="6c210-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="6c210-109">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="6c210-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="6c210-110">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="6c210-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="6c210-111">Utvid Intrastat-modell i treet.</span><span class="sxs-lookup"><span data-stu-id="6c210-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="6c210-112">Utvid Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="6c210-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="6c210-113">Velg Intrastat-modell\Intrastat (DE)\Intrastat (DE) med telling og summering i treet.</span><span class="sxs-lookup"><span data-stu-id="6c210-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="6c210-114">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="6c210-114">Click Designer.</span></span>
7. <span data-ttu-id="6c210-115">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="6c210-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="6c210-116">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="6c210-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="6c210-117">Legg til en ny datakilde for å hente listen over lagrede blokker.</span><span class="sxs-lookup"><span data-stu-id="6c210-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="6c210-118">Velg Funksjoner\Beregnet felt i treet.</span><span class="sxs-lookup"><span data-stu-id="6c210-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="6c210-119">Skriv inn $BlocksList i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="6c210-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="6c210-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="6c210-120">$BlocksList</span></span>  
11. <span data-ttu-id="6c210-121">Klikk Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="6c210-121">Click Edit formula.</span></span>
12. <span data-ttu-id="6c210-122">I treet velger du Datainnsamlingsfunksjoner\COLLECTEDLIST.</span><span class="sxs-lookup"><span data-stu-id="6c210-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="6c210-123">Klikk Legg til funksjon.</span><span class="sxs-lookup"><span data-stu-id="6c210-123">Click Add function.</span></span>
14. <span data-ttu-id="6c210-124">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="6c210-124">Click Add data source.</span></span>
15. <span data-ttu-id="6c210-125">Skriv inn "COLLECTEDLIST('$BlockName', " i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="6c210-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="6c210-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="6c210-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="6c210-127">Skriv inn COLLECTEDLIST('$BlockName', "\*") i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="6c210-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="6c210-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="6c210-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="6c210-129">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6c210-129">Click Save.</span></span>
    * <span data-ttu-id="6c210-130">Mønsteret "\*" betyr at alle blokker vil bli inkludert i listen for denne posten.</span><span class="sxs-lookup"><span data-stu-id="6c210-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="6c210-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6c210-131">Close the page.</span></span>
19. <span data-ttu-id="6c210-132">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="6c210-132">Click OK.</span></span>
20. <span data-ttu-id="6c210-133">Klikk Formater-kategorien.</span><span class="sxs-lookup"><span data-stu-id="6c210-133">Click the Format tab.</span></span>
21. <span data-ttu-id="6c210-134">Velg Intrastat\Data i treet.</span><span class="sxs-lookup"><span data-stu-id="6c210-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="6c210-135">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="6c210-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="6c210-136">Velg Tekst\Sekvens i treet.</span><span class="sxs-lookup"><span data-stu-id="6c210-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="6c210-137">Skriv inn Totalsummer etter blokker i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="6c210-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="6c210-138">Totalsummer etter blokker</span><span class="sxs-lookup"><span data-stu-id="6c210-138">Totals by blocks</span></span>  
25. <span data-ttu-id="6c210-139">Velg Ny linje - Windows (CR LF) i Spesialtegn-feltet.</span><span class="sxs-lookup"><span data-stu-id="6c210-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="6c210-140">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="6c210-140">Click OK.</span></span>
27. <span data-ttu-id="6c210-141">Velg Intrastat\Data\Totalsummer etter blokker i treet.</span><span class="sxs-lookup"><span data-stu-id="6c210-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="6c210-142">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="6c210-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="6c210-143">Velg Tekst\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="6c210-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="6c210-144">I Navn-feltet skriver du inn Blokkode.</span><span class="sxs-lookup"><span data-stu-id="6c210-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="6c210-145">Blokkode</span><span class="sxs-lookup"><span data-stu-id="6c210-145">Block code</span></span>  
31. <span data-ttu-id="6c210-146">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="6c210-146">Click OK.</span></span>
32. <span data-ttu-id="6c210-147">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="6c210-147">Click Add String.</span></span>
33. <span data-ttu-id="6c210-148">Skriv inn Linjetelling i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="6c210-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="6c210-149">Linjetelling</span><span class="sxs-lookup"><span data-stu-id="6c210-149">Lines counting</span></span>  
34. <span data-ttu-id="6c210-150">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="6c210-150">Click OK.</span></span>
35. <span data-ttu-id="6c210-151">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="6c210-151">Click Add String.</span></span>
36. <span data-ttu-id="6c210-152">I Navn-feltet skriver du inn Totalbeløp.</span><span class="sxs-lookup"><span data-stu-id="6c210-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="6c210-153">Totalbeløp</span><span class="sxs-lookup"><span data-stu-id="6c210-153">Total amount</span></span>  
37. <span data-ttu-id="6c210-154">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="6c210-154">Click OK.</span></span>
38. <span data-ttu-id="6c210-155">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="6c210-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="6c210-156">Velg $BlocksList i treet.</span><span class="sxs-lookup"><span data-stu-id="6c210-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="6c210-157">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="6c210-157">Click Bind.</span></span>
    * <span data-ttu-id="6c210-158">Opprett en summeringslinje for hver lagret blokk.</span><span class="sxs-lookup"><span data-stu-id="6c210-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="6c210-159">Klikk Formater-kategorien.</span><span class="sxs-lookup"><span data-stu-id="6c210-159">Click the Format tab.</span></span>
42. <span data-ttu-id="6c210-160">Velg Intrastat\Data\Totalsummer etter blokker\Blokkode i treet.</span><span class="sxs-lookup"><span data-stu-id="6c210-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="6c210-161">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="6c210-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="6c210-162">Klikk Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="6c210-162">Click Edit formula.</span></span>
45. <span data-ttu-id="6c210-163">Skriv inn '"Block id: " & ' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="6c210-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="6c210-164">"Block id: " &</span><span class="sxs-lookup"><span data-stu-id="6c210-164">"Block id: " &</span></span>  
46. <span data-ttu-id="6c210-165">Utvid $BlocksList i treet.</span><span class="sxs-lookup"><span data-stu-id="6c210-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="6c210-166">Velg $BlocksList\Verdi i treet.</span><span class="sxs-lookup"><span data-stu-id="6c210-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="6c210-167">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="6c210-167">Click Add data source.</span></span>
49. <span data-ttu-id="6c210-168">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6c210-168">Click Save.</span></span>
50. <span data-ttu-id="6c210-169">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6c210-169">Close the page.</span></span>
51. <span data-ttu-id="6c210-170">Klikk Formater-kategorien.</span><span class="sxs-lookup"><span data-stu-id="6c210-170">Click the Format tab.</span></span>
52. <span data-ttu-id="6c210-171">Velg Intrastat\Data\Totalsummer etter blokker\Linjetelling i treet.</span><span class="sxs-lookup"><span data-stu-id="6c210-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="6c210-172">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="6c210-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="6c210-173">Klikk Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="6c210-173">Click Edit formula.</span></span>
    * <span data-ttu-id="6c210-174">Opprett utdata for antallet linjer for hver blokk som er presentert i denne rapporten.</span><span class="sxs-lookup"><span data-stu-id="6c210-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="6c210-175">Skriv inn '"Antall linjer i denne blokken: " & ' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="6c210-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="6c210-176">"Antall linjer i denne blokken: " &</span><span class="sxs-lookup"><span data-stu-id="6c210-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="6c210-177">Skriv inn '"Antall linjer i denne blokken: " & TEXT('. i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="6c210-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="6c210-178">"Antall linjer i denne blokken: " & TEXT( </span><span class="sxs-lookup"><span data-stu-id="6c210-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="6c210-179">I treet velger du Datainnsamlingsfunksjoner\COUNTIFS.</span><span class="sxs-lookup"><span data-stu-id="6c210-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="6c210-180">Klikk Legg til funksjon.</span><span class="sxs-lookup"><span data-stu-id="6c210-180">Click Add function.</span></span>
59. <span data-ttu-id="6c210-181">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="6c210-181">Click Add data source.</span></span>
60. <span data-ttu-id="6c210-182">Skriv inn '"Antall linjer i denne blokken: " & TEXT(COUNTIFS('$BlockName',' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="6c210-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="6c210-183">"Antall linjer i denne blokken: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="6c210-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="6c210-184">Utvid $BlocksList i treet.</span><span class="sxs-lookup"><span data-stu-id="6c210-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="6c210-185">Velg $BlocksList\Verdi i treet.</span><span class="sxs-lookup"><span data-stu-id="6c210-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="6c210-186">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="6c210-186">Click Add data source.</span></span>
64. <span data-ttu-id="6c210-187">Skriv inn '"Antall linjer i denne blokken: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, ' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="6c210-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="6c210-188">"Antall linjer i denne blokken: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="6c210-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="6c210-189">Velg $RecName i treet.</span><span class="sxs-lookup"><span data-stu-id="6c210-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="6c210-190">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="6c210-190">Click Add data source.</span></span>
67. <span data-ttu-id="6c210-191">Skriv inn '"Antall linjer i denne blokken: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="6c210-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="6c210-192">"Antall linjer i denne blokken: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="6c210-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="6c210-193">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6c210-193">Click Save.</span></span>
69. <span data-ttu-id="6c210-194">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6c210-194">Close the page.</span></span>
70. <span data-ttu-id="6c210-195">Klikk Formater-kategorien.</span><span class="sxs-lookup"><span data-stu-id="6c210-195">Click the Format tab.</span></span>
71. <span data-ttu-id="6c210-196">Velg Intrastat\Data\Totalsummer etter blokker\Totalbeløp i treet.</span><span class="sxs-lookup"><span data-stu-id="6c210-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="6c210-197">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="6c210-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="6c210-198">Klikk Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="6c210-198">Click Edit formula.</span></span>
    * <span data-ttu-id="6c210-199">Opprett utdata som skal være summen av det fakturerte beløpet for hver blokk presentert i denne rapporten.</span><span class="sxs-lookup"><span data-stu-id="6c210-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="6c210-200">Skriv inn '"Sum av fakturert beløp: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="6c210-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="6c210-201">"Sum av fakturert beløp: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="6c210-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="6c210-202">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6c210-202">Click Save.</span></span>
76. <span data-ttu-id="6c210-203">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6c210-203">Close the page.</span></span>
77. <span data-ttu-id="6c210-204">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6c210-204">Click Save.</span></span>
78. <span data-ttu-id="6c210-205">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6c210-205">Close the page.</span></span>

