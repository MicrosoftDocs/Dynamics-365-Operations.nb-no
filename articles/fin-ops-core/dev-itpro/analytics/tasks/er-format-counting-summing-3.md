---
title: ER Konfigurere format for å utføre telling og summering (del 3 - Bruke beregninger for å lage utdataene)
description: Dette emnet beskriver hvordan du konfigurerer et elektronisk rapporteringsformat som teller og summerer basert på data fra tekstutdataene som allerede er generert. (Del 3)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7073539ed4c1d9d5acbb0ca84b43538d87fc8b4b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749003"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="5c1ec-104">ER Konfigurere format for å utføre telling og summering (del 3 - Bruke beregninger for å lage utdataene)</span><span class="sxs-lookup"><span data-stu-id="5c1ec-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5c1ec-105">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="5c1ec-106">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="5c1ec-107">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Konfigurere format for å utføre telling og summering (del 2: Konfigurere beregninger)".</span><span class="sxs-lookup"><span data-stu-id="5c1ec-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="5c1ec-108">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="5c1ec-109">Konfigurere denne rapporten for å bruke tellings- og summeringsinformasjon</span><span class="sxs-lookup"><span data-stu-id="5c1ec-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="5c1ec-110">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="5c1ec-111">Klikk på Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="5c1ec-112">Utvid Intrastat-modell i treet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="5c1ec-113">Utvid Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="5c1ec-114">Velg Intrastat-modell\Intrastat (DE)\Intrastat (DE) med telling og summering i treet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="5c1ec-115">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-115">Click Designer.</span></span>
7. <span data-ttu-id="5c1ec-116">Klikk på fanen Tilordning.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="5c1ec-117">Klikk på Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="5c1ec-118">Legg til en ny datakilde for å hente listen over lagrede blokker.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="5c1ec-119">Velg Funksjoner\Beregnet felt i treet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="5c1ec-120">Skriv inn $BlocksList i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="5c1ec-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="5c1ec-121">$BlocksList</span></span>  
11. <span data-ttu-id="5c1ec-122">Klikk på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-122">Click Edit formula.</span></span>
12. <span data-ttu-id="5c1ec-123">I treet velger du Datainnsamlingsfunksjoner\COLLECTEDLIST.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="5c1ec-124">Klikk på Legg til funksjon.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-124">Click Add function.</span></span>
14. <span data-ttu-id="5c1ec-125">Klikk på Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-125">Click Add data source.</span></span>
15. <span data-ttu-id="5c1ec-126">Skriv inn "COLLECTEDLIST('$BlockName', " i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="5c1ec-127">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="5c1ec-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="5c1ec-128">Skriv inn COLLECTEDLIST('$BlockName', "\*") i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="5c1ec-129">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="5c1ec-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="5c1ec-130">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-130">Click Save.</span></span>
    * <span data-ttu-id="5c1ec-131">Mønsteret "\*" betyr at alle blokker vil bli inkludert i listen for denne posten.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="5c1ec-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-132">Close the page.</span></span>
19. <span data-ttu-id="5c1ec-133">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-133">Click OK.</span></span>
20. <span data-ttu-id="5c1ec-134">Klikk på Formater-fanen.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-134">Click the Format tab.</span></span>
21. <span data-ttu-id="5c1ec-135">Velg Intrastat\Data i treet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="5c1ec-136">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="5c1ec-137">Velg Tekst\Sekvens i treet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="5c1ec-138">Skriv inn Totalsummer etter blokker i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="5c1ec-139">Totalsummer etter blokker</span><span class="sxs-lookup"><span data-stu-id="5c1ec-139">Totals by blocks</span></span>  
25. <span data-ttu-id="5c1ec-140">Velg Ny linje - Windows (CR LF) i Spesialtegn-feltet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="5c1ec-141">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-141">Click OK.</span></span>
27. <span data-ttu-id="5c1ec-142">Velg Intrastat\Data\Totalsummer etter blokker i treet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="5c1ec-143">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="5c1ec-144">Velg Tekst\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="5c1ec-145">I Navn-feltet skriver du inn Blokkode.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="5c1ec-146">Blokkode</span><span class="sxs-lookup"><span data-stu-id="5c1ec-146">Block code</span></span>  
31. <span data-ttu-id="5c1ec-147">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-147">Click OK.</span></span>
32. <span data-ttu-id="5c1ec-148">Klikk på Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-148">Click Add String.</span></span>
33. <span data-ttu-id="5c1ec-149">Skriv inn Linjetelling i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="5c1ec-150">Linjetelling</span><span class="sxs-lookup"><span data-stu-id="5c1ec-150">Lines counting</span></span>  
34. <span data-ttu-id="5c1ec-151">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-151">Click OK.</span></span>
35. <span data-ttu-id="5c1ec-152">Klikk på Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-152">Click Add String.</span></span>
36. <span data-ttu-id="5c1ec-153">I Navn-feltet skriver du inn Totalbeløp.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="5c1ec-154">Totalbeløp</span><span class="sxs-lookup"><span data-stu-id="5c1ec-154">Total amount</span></span>  
37. <span data-ttu-id="5c1ec-155">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-155">Click OK.</span></span>
38. <span data-ttu-id="5c1ec-156">Klikk på fanen Tilordning.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="5c1ec-157">Velg $BlocksList i treet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="5c1ec-158">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-158">Click Bind.</span></span>
    * <span data-ttu-id="5c1ec-159">Opprett en summeringslinje for hver lagret blokk.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="5c1ec-160">Klikk på Formater-fanen.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-160">Click the Format tab.</span></span>
42. <span data-ttu-id="5c1ec-161">Velg Intrastat\Data\Totalsummer etter blokker\Blokkode i treet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="5c1ec-162">Klikk på fanen Tilordning.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="5c1ec-163">Klikk på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-163">Click Edit formula.</span></span>
45. <span data-ttu-id="5c1ec-164">Skriv inn '"Block id: " & ' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="5c1ec-165">"Block id: " &</span><span class="sxs-lookup"><span data-stu-id="5c1ec-165">"Block id: " &</span></span>  
46. <span data-ttu-id="5c1ec-166">Utvid $BlocksList i treet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="5c1ec-167">Velg $BlocksList\Verdi i treet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="5c1ec-168">Klikk på Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-168">Click Add data source.</span></span>
49. <span data-ttu-id="5c1ec-169">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-169">Click Save.</span></span>
50. <span data-ttu-id="5c1ec-170">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-170">Close the page.</span></span>
51. <span data-ttu-id="5c1ec-171">Klikk på Formater-fanen.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-171">Click the Format tab.</span></span>
52. <span data-ttu-id="5c1ec-172">Velg Intrastat\Data\Totalsummer etter blokker\Linjetelling i treet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="5c1ec-173">Klikk på fanen Tilordning.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="5c1ec-174">Klikk på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-174">Click Edit formula.</span></span>
    * <span data-ttu-id="5c1ec-175">Opprett utdata for antallet linjer for hver blokk som er presentert i denne rapporten.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="5c1ec-176">Skriv inn '"Antall linjer i denne blokken: " & ' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="5c1ec-177">"Antall linjer i denne blokken: " &</span><span class="sxs-lookup"><span data-stu-id="5c1ec-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="5c1ec-178">Skriv inn '"Antall linjer i denne blokken: " & TEXT('. i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="5c1ec-179">"Antall linjer i denne blokken: " & TEXT( </span><span class="sxs-lookup"><span data-stu-id="5c1ec-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="5c1ec-180">I treet velger du Datainnsamlingsfunksjoner\COUNTIFS.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="5c1ec-181">Klikk på Legg til funksjon.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-181">Click Add function.</span></span>
59. <span data-ttu-id="5c1ec-182">Klikk på Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-182">Click Add data source.</span></span>
60. <span data-ttu-id="5c1ec-183">Skriv inn '"Antall linjer i denne blokken: " & TEXT(COUNTIFS('$BlockName',' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="5c1ec-184">"Antall linjer i denne blokken: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="5c1ec-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="5c1ec-185">Utvid $BlocksList i treet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="5c1ec-186">Velg $BlocksList\Verdi i treet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="5c1ec-187">Klikk på Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-187">Click Add data source.</span></span>
64. <span data-ttu-id="5c1ec-188">Skriv inn '"Antall linjer i denne blokken: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, ' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="5c1ec-189">"Antall linjer i denne blokken: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="5c1ec-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="5c1ec-190">Velg $RecName i treet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="5c1ec-191">Klikk på Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-191">Click Add data source.</span></span>
67. <span data-ttu-id="5c1ec-192">Skriv inn '"Antall linjer i denne blokken: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="5c1ec-193">"Antall linjer i denne blokken: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="5c1ec-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="5c1ec-194">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-194">Click Save.</span></span>
69. <span data-ttu-id="5c1ec-195">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-195">Close the page.</span></span>
70. <span data-ttu-id="5c1ec-196">Klikk på Formater-fanen.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-196">Click the Format tab.</span></span>
71. <span data-ttu-id="5c1ec-197">Velg Intrastat\Data\Totalsummer etter blokker\Totalbeløp i treet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="5c1ec-198">Klikk på fanen Tilordning.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="5c1ec-199">Klikk på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-199">Click Edit formula.</span></span>
    * <span data-ttu-id="5c1ec-200">Opprett utdata som skal være summen av det fakturerte beløpet for hver blokk presentert i denne rapporten.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="5c1ec-201">Skriv inn '"Sum av fakturert beløp: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))' i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="5c1ec-202">"Sum av fakturert beløp: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="5c1ec-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="5c1ec-203">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-203">Click Save.</span></span>
76. <span data-ttu-id="5c1ec-204">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-204">Close the page.</span></span>
77. <span data-ttu-id="5c1ec-205">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-205">Click Save.</span></span>
78. <span data-ttu-id="5c1ec-206">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5c1ec-206">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]