---
title: ER Konfigurere format for å utføre telling og summering (del 2 - Konfigurere beregninger)
description: Dette emnet beskriver hvordan du konfigurerer et elektronisk rapporteringsformat som teller og summerer basert på data fra tekstutdataene som allerede er generert. (Del 2)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6eb3d686e8f60de51001deffb4c2460c181a4ab
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565172"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="22553-104">ER Konfigurere format for å utføre telling og summering (del 2 - Konfigurere beregninger)</span><span class="sxs-lookup"><span data-stu-id="22553-104">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="22553-105">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata.</span><span class="sxs-lookup"><span data-stu-id="22553-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="22553-106">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="22553-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="22553-107">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Konfigurere format for å utføre telling og summering (del 1: Opprette format)".</span><span class="sxs-lookup"><span data-stu-id="22553-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="22553-108">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="22553-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="22553-109">Opprette en formatkonfigurasjon for å legge til tellings- og summeringsdetaljer</span><span class="sxs-lookup"><span data-stu-id="22553-109">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="22553-110">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="22553-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="22553-111">Klikk på Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="22553-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="22553-112">Utvid Intrastat-modell i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="22553-113">Velg Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-113">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="22553-114">Anta at du må tilpasse formatet fra Microsoft ved å legge til linjer med sammendragsdetaljer på slutten av Intrastat-rapporten.</span><span class="sxs-lookup"><span data-stu-id="22553-114">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="22553-115">Du må gjøre dette ved å avlede vår egen forekomst av Intrastat-konfigurasjonen fra Microsoft-forekomsten for å gjøre endringer.</span><span class="sxs-lookup"><span data-stu-id="22553-115">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="22553-116">Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="22553-116">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="22553-117">I Ny-feltet angir du Avled fra navnet: Intrastat (DE), Microsoft.</span><span class="sxs-lookup"><span data-stu-id="22553-117">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="22553-118">I Navn-feltet skriver du inn Intrastat (DE) med telling og summering.</span><span class="sxs-lookup"><span data-stu-id="22553-118">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="22553-119">Klikk på Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="22553-119">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="22553-120">Konfigurere denne rapporten for å utføre telling og summering basert på utdatadetaljene</span><span class="sxs-lookup"><span data-stu-id="22553-120">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="22553-121">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="22553-121">Click Designer.</span></span>
2. <span data-ttu-id="22553-122">Velg Ja i feltet Samle inn utdatadetaljer.</span><span class="sxs-lookup"><span data-stu-id="22553-122">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="22553-123">Dette flagget vil under kjøring aktivere prosessen for innsamling av utdatadetaljer for generering av Intrastat-filen.</span><span class="sxs-lookup"><span data-stu-id="22553-123">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="22553-124">Du må utføre telling for forskjellige Intrastat-retninger, så legg til en dedikert modellopplisting i datakildenes liste for denne formatkonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="22553-124">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="22553-125">Klikk på fanen Tilordning.</span><span class="sxs-lookup"><span data-stu-id="22553-125">Click the Mapping tab.</span></span>
4. <span data-ttu-id="22553-126">Klikk på Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="22553-126">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="22553-127">Velg Datamodell\Opplisting i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-127">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="22553-128">I Navn-feltet skriver du inn Retning-</span><span class="sxs-lookup"><span data-stu-id="22553-128">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="22553-129">Angi eller velg en verdi i Modellopplisting-feltet.</span><span class="sxs-lookup"><span data-stu-id="22553-129">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="22553-130">Velg verdien Retning.</span><span class="sxs-lookup"><span data-stu-id="22553-130">Select the value Direction.</span></span>  
8. <span data-ttu-id="22553-131">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="22553-131">Click OK.</span></span>
9. <span data-ttu-id="22553-132">Klikk på Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="22553-132">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="22553-133">Velg Funksjoner\Beregnet felt i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-133">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="22553-134">Skriv inn $BlockName i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="22553-134">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="22553-135">Klikk på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="22553-135">Click Edit formula.</span></span>
13. <span data-ttu-id="22553-136">Skriv inn block i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="22553-136">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="22553-137">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="22553-137">Click Save.</span></span>
15. <span data-ttu-id="22553-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="22553-138">Close the page.</span></span>
16. <span data-ttu-id="22553-139">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="22553-139">Click OK.</span></span>
17. <span data-ttu-id="22553-140">Klikk på Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="22553-140">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="22553-141">Velg Funksjoner\Beregnet felt i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-141">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="22553-142">Skriv inn $RecName i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="22553-142">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="22553-143">Klikk på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="22553-143">Click Edit formula.</span></span>
21. <span data-ttu-id="22553-144">Skriv inn record i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="22553-144">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="22553-145">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="22553-145">Click Save.</span></span>
23. <span data-ttu-id="22553-146">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="22553-146">Close the page.</span></span>
24. <span data-ttu-id="22553-147">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="22553-147">Click OK.</span></span>
25. <span data-ttu-id="22553-148">Klikk på Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="22553-148">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="22553-149">Velg Funksjoner\Beregnet felt i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-149">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="22553-150">Skriv inn $InvName i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="22553-150">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="22553-151">Klikk på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="22553-151">Click Edit formula.</span></span>
29. <span data-ttu-id="22553-152">Skriv inn InvoicedAmountEUR i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="22553-152">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="22553-153">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="22553-153">Click Save.</span></span>
31. <span data-ttu-id="22553-154">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="22553-154">Close the page.</span></span>
32. <span data-ttu-id="22553-155">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="22553-155">Click OK.</span></span>
33. <span data-ttu-id="22553-156">Velg Intrastat\Data i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-156">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="22553-157">Klikk Rediger-knappen for feltet Navn på innsamlet datanøkkel.</span><span class="sxs-lookup"><span data-stu-id="22553-157">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="22553-158">Klikk på Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="22553-158">Click Add data source.</span></span>
    * <span data-ttu-id="22553-159">$BlockName</span><span class="sxs-lookup"><span data-stu-id="22553-159">$BlockName</span></span>  
36. <span data-ttu-id="22553-160">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="22553-160">Click Save.</span></span>
37. <span data-ttu-id="22553-161">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="22553-161">Close the page.</span></span>
38. <span data-ttu-id="22553-162">Klikk på Rediger-knappen for feltet Verdi for innsamlet datanøkkel.</span><span class="sxs-lookup"><span data-stu-id="22553-162">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="22553-163">Angi IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export") i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="22553-163">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="22553-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="22553-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="22553-165">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="22553-165">Click Save.</span></span>
41. <span data-ttu-id="22553-166">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="22553-166">Close the page.</span></span>
    * <span data-ttu-id="22553-167">Tell linjene i denne sekvensen.</span><span class="sxs-lookup"><span data-stu-id="22553-167">Count the lines of this sequence.</span></span> <span data-ttu-id="22553-168">Resultatene vil bli brukt med navnet "blokk" separat for forskjellige retninger.</span><span class="sxs-lookup"><span data-stu-id="22553-168">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="22553-169">Verdien "Import" vil bli brukt for hvilke som helst Intrastat-transaksjoner for ankomster.</span><span class="sxs-lookup"><span data-stu-id="22553-169">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="22553-170">Verdien "Eksport" vil bli brukt for hvilke som helst Intrastat-transaksjoner for utsendelser.</span><span class="sxs-lookup"><span data-stu-id="22553-170">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="22553-171">Se på dette som et virtuelt Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="22553-171">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="22553-172">For hver transaksjon fylles det ut en rad der den første kolonnen"blokk" fylles ut med verdiene "Import" og "Eksport".</span><span class="sxs-lookup"><span data-stu-id="22553-172">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="22553-173">Utvid Intrastat\Data: Sekvens i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-173">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="22553-174">Velg Intrastat\Data: Sekvens\Ankomster? i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-174">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="22553-175">Klikk Rediger-knappen for feltet Navn på innsamlet datanøkkel.</span><span class="sxs-lookup"><span data-stu-id="22553-175">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="22553-176">Tell linjene i denne sekvensen.</span><span class="sxs-lookup"><span data-stu-id="22553-176">Count the lines of this sequence.</span></span> <span data-ttu-id="22553-177">Resultatene blir lagret ved hjelp av navnet "post".</span><span class="sxs-lookup"><span data-stu-id="22553-177">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="22553-178">Velg $RecName i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-178">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="22553-179">Klikk på Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="22553-179">Click Add data source.</span></span>
47. <span data-ttu-id="22553-180">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="22553-180">Click Save.</span></span>
48. <span data-ttu-id="22553-181">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="22553-181">Close the page.</span></span>
49. <span data-ttu-id="22553-182">Klikk på Rediger-knappen for feltet Verdi for innsamlet datanøkkel.</span><span class="sxs-lookup"><span data-stu-id="22553-182">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="22553-183">I Formel-feltet skriver du inn Intrastat.CommodityRecord.CommodityCode.</span><span class="sxs-lookup"><span data-stu-id="22553-183">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="22553-184">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="22553-184">Click Save.</span></span>
52. <span data-ttu-id="22553-185">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="22553-185">Close the page.</span></span>
    * <span data-ttu-id="22553-186">Tell linjene i denne sekvensen.</span><span class="sxs-lookup"><span data-stu-id="22553-186">Count the lines of this sequence.</span></span> <span data-ttu-id="22553-187">Resultatene vil bli brukt med navnet "post" separat for forskjellige varekoder.</span><span class="sxs-lookup"><span data-stu-id="22553-187">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="22553-188">Se på dette som et virtuelt Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="22553-188">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="22553-189">For hver transaksjon fylles det ut en rad der den første kolonnen "blokk" fylles ut med verdiene "Import" og "Eksport" henholdsvis, og den andre blokken "post" med varekodeverdien.</span><span class="sxs-lookup"><span data-stu-id="22553-189">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="22553-190">Velg Intrastat\Data: Sekvens\Fordelinger? i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-190">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="22553-191">Klikk Rediger-knappen for feltet Navn på innsamlet datanøkkel.</span><span class="sxs-lookup"><span data-stu-id="22553-191">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="22553-192">Velg $RecName i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-192">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="22553-193">Klikk på Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="22553-193">Click Add data source.</span></span>
57. <span data-ttu-id="22553-194">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="22553-194">Click Save.</span></span>
58. <span data-ttu-id="22553-195">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="22553-195">Close the page.</span></span>
59. <span data-ttu-id="22553-196">Klikk på Rediger-knappen for feltet Verdi for innsamlet datanøkkel.</span><span class="sxs-lookup"><span data-stu-id="22553-196">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="22553-197">I Formel-feltet skriver du inn Intrastat.CommodityRecord.CommodityCode.</span><span class="sxs-lookup"><span data-stu-id="22553-197">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="22553-198">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="22553-198">Click Save.</span></span>
62. <span data-ttu-id="22553-199">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="22553-199">Close the page.</span></span>
63. <span data-ttu-id="22553-200">Utvid Intrastat\Data: Sekvens\Fordelinger: Sekvens? i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="22553-201">Utvid Intrastat\Data: Sekvens\Fordelinger: Sekvens?\Post = Intrastat.CommodityRecord i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-201">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="22553-202">Klikk på Formater-fanen.</span><span class="sxs-lookup"><span data-stu-id="22553-202">Click the Format tab.</span></span>
66. <span data-ttu-id="22553-203">Velg Intrastat\Data\Fordelinger\Post\Fakturabeløp EUR i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-203">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="22553-204">Klikk på fanen Tilordning.</span><span class="sxs-lookup"><span data-stu-id="22553-204">Click the Mapping tab.</span></span>
68. <span data-ttu-id="22553-205">Klikk Rediger-knappen for feltet Navn på innsamlet datanøkkel.</span><span class="sxs-lookup"><span data-stu-id="22553-205">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="22553-206">Velg $InvName i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-206">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="22553-207">Klikk på Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="22553-207">Click Add data source.</span></span>
71. <span data-ttu-id="22553-208">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="22553-208">Click Save.</span></span>
72. <span data-ttu-id="22553-209">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="22553-209">Close the page.</span></span>
    * <span data-ttu-id="22553-210">Summer de fakturerte beløpsverdiene for linjer i denne sekvensen.</span><span class="sxs-lookup"><span data-stu-id="22553-210">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="22553-211">Resultatene vil bli brukt med navnet "InvoicedAmountEUR" separat for forskjellige Intrastat-retninger og varekoder.</span><span class="sxs-lookup"><span data-stu-id="22553-211">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="22553-212">Se på dette som en virtuell opprettelse i Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="22553-212">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="22553-213">For hver transaksjon fylles det ut en rad der den første kolonnen"blokk" fylles ut med verdiene "Import" og "Eksport".</span><span class="sxs-lookup"><span data-stu-id="22553-213">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="22553-214">Den andre blokken "post" fylles ut med varekodeverdien og den tredje kolonnen "InvoicedAmountEUR" fylles ut med fakturabeløpsverdien.</span><span class="sxs-lookup"><span data-stu-id="22553-214">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="22553-215">Utvid Intrastat\Data\Ankomster? i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-215">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="22553-216">Utvid Intrastat\Data\Ankomster?\Post = Intrastat.CommodityRecord i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-216">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="22553-217">Klikk på Formater-fanen.</span><span class="sxs-lookup"><span data-stu-id="22553-217">Click the Format tab.</span></span>
76. <span data-ttu-id="22553-218">Velg Intrastat\Data\Ankomster\Post\Fakturabeløp EUR i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-218">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="22553-219">Klikk på fanen Tilordning.</span><span class="sxs-lookup"><span data-stu-id="22553-219">Click the Mapping tab.</span></span>
78. <span data-ttu-id="22553-220">Klikk Rediger-knappen for feltet Navn på innsamlet datanøkkel.</span><span class="sxs-lookup"><span data-stu-id="22553-220">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="22553-221">Velg $InvName i treet.</span><span class="sxs-lookup"><span data-stu-id="22553-221">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="22553-222">Klikk på Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="22553-222">Click Add data source.</span></span>
81. <span data-ttu-id="22553-223">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="22553-223">Click Save.</span></span>
82. <span data-ttu-id="22553-224">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="22553-224">Close the page.</span></span>
83. <span data-ttu-id="22553-225">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="22553-225">Click Save.</span></span>
84. <span data-ttu-id="22553-226">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="22553-226">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]