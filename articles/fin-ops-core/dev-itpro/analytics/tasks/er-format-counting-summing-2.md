---
title: ER Konfigurere format for å utføre telling og summering (del 2 - Konfigurere beregninger)
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d785b321037645837dbcbaf28c8ede9b8e97b79
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550608"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="fa57c-103">ER Konfigurere format for å utføre telling og summering (del 2 - Konfigurere beregninger)</span><span class="sxs-lookup"><span data-stu-id="fa57c-103">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fa57c-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata.</span><span class="sxs-lookup"><span data-stu-id="fa57c-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="fa57c-105">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="fa57c-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="fa57c-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Konfigurere format for å utføre telling og summering (del 1: Opprette format)".</span><span class="sxs-lookup"><span data-stu-id="fa57c-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 1: Create format)” procedure.</span></span>

<span data-ttu-id="fa57c-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="fa57c-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="fa57c-108">Opprette en formatkonfigurasjon for å legge til tellings- og summeringsdetaljer</span><span class="sxs-lookup"><span data-stu-id="fa57c-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="fa57c-109">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="fa57c-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="fa57c-110">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="fa57c-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="fa57c-111">Utvid Intrastat-modell i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="fa57c-112">Velg Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="fa57c-113">Anta at du må tilpasse formatet fra Microsoft ved å legge til linjer med sammendragsdetaljer på slutten av Intrastat-rapporten.</span><span class="sxs-lookup"><span data-stu-id="fa57c-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="fa57c-114">Du må gjøre dette ved å avlede vår egen forekomst av Intrastat-konfigurasjonen fra Microsoft-forekomsten for å gjøre endringer.</span><span class="sxs-lookup"><span data-stu-id="fa57c-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="fa57c-115">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="fa57c-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="fa57c-116">I Ny-feltet angir du Avled fra navnet: Intrastat (DE), Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fa57c-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="fa57c-117">I Navn-feltet skriver du inn Intrastat (DE) med telling og summering.</span><span class="sxs-lookup"><span data-stu-id="fa57c-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="fa57c-118">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="fa57c-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="fa57c-119">Konfigurere denne rapporten for å utføre telling og summering basert på utdatadetaljene</span><span class="sxs-lookup"><span data-stu-id="fa57c-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="fa57c-120">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="fa57c-120">Click Designer.</span></span>
2. <span data-ttu-id="fa57c-121">Velg Ja i feltet Samle inn utdatadetaljer.</span><span class="sxs-lookup"><span data-stu-id="fa57c-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="fa57c-122">Dette flagget vil under kjøring aktivere prosessen for innsamling av utdatadetaljer for generering av Intrastat-filen.</span><span class="sxs-lookup"><span data-stu-id="fa57c-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="fa57c-123">Du må utføre telling for forskjellige Intrastat-retninger, så legg til en dedikert modellopplisting i datakildenes liste for denne formatkonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="fa57c-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources’ list of this format configuration.</span></span>  
3. <span data-ttu-id="fa57c-124">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="fa57c-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="fa57c-125">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="fa57c-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="fa57c-126">Velg Datamodell\Opplisting i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="fa57c-127">I Navn-feltet skriver du inn Retning-</span><span class="sxs-lookup"><span data-stu-id="fa57c-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="fa57c-128">Angi eller velg en verdi i Modellopplisting-feltet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="fa57c-129">Velg verdien Retning.</span><span class="sxs-lookup"><span data-stu-id="fa57c-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="fa57c-130">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="fa57c-130">Click OK.</span></span>
9. <span data-ttu-id="fa57c-131">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="fa57c-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="fa57c-132">Velg Funksjoner\Beregnet felt i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="fa57c-133">Skriv inn $BlockName i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="fa57c-134">Klikk Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="fa57c-134">Click Edit formula.</span></span>
13. <span data-ttu-id="fa57c-135">Skriv inn block i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="fa57c-136">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fa57c-136">Click Save.</span></span>
15. <span data-ttu-id="fa57c-137">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fa57c-137">Close the page.</span></span>
16. <span data-ttu-id="fa57c-138">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="fa57c-138">Click OK.</span></span>
17. <span data-ttu-id="fa57c-139">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="fa57c-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="fa57c-140">Velg Funksjoner\Beregnet felt i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="fa57c-141">Skriv inn $RecName i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="fa57c-142">Klikk Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="fa57c-142">Click Edit formula.</span></span>
21. <span data-ttu-id="fa57c-143">Skriv inn record i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="fa57c-144">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fa57c-144">Click Save.</span></span>
23. <span data-ttu-id="fa57c-145">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fa57c-145">Close the page.</span></span>
24. <span data-ttu-id="fa57c-146">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="fa57c-146">Click OK.</span></span>
25. <span data-ttu-id="fa57c-147">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="fa57c-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="fa57c-148">Velg Funksjoner\Beregnet felt i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="fa57c-149">Skriv inn $InvName i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="fa57c-150">Klikk Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="fa57c-150">Click Edit formula.</span></span>
29. <span data-ttu-id="fa57c-151">Skriv inn InvoicedAmountEUR i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="fa57c-152">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fa57c-152">Click Save.</span></span>
31. <span data-ttu-id="fa57c-153">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fa57c-153">Close the page.</span></span>
32. <span data-ttu-id="fa57c-154">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="fa57c-154">Click OK.</span></span>
33. <span data-ttu-id="fa57c-155">Velg Intrastat\Data i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="fa57c-156">Klikk Rediger-knappen for feltet Navn på innsamlet datanøkkel.</span><span class="sxs-lookup"><span data-stu-id="fa57c-156">Click Edit button for the ‘Collected data key name’ field</span></span>
35. <span data-ttu-id="fa57c-157">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="fa57c-157">Click Add data source.</span></span>
    * <span data-ttu-id="fa57c-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="fa57c-158">$BlockName</span></span>  
36. <span data-ttu-id="fa57c-159">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fa57c-159">Click Save.</span></span>
37. <span data-ttu-id="fa57c-160">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fa57c-160">Close the page.</span></span>
38. <span data-ttu-id="fa57c-161">Klikk Rediger-knappen for feltet Verdi for innsamlet datanøkkel.</span><span class="sxs-lookup"><span data-stu-id="fa57c-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="fa57c-162">Angi IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export") i Formel-feltet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="fa57c-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="fa57c-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="fa57c-164">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fa57c-164">Click Save.</span></span>
41. <span data-ttu-id="fa57c-165">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fa57c-165">Close the page.</span></span>
    * <span data-ttu-id="fa57c-166">Tell linjene i denne sekvensen.</span><span class="sxs-lookup"><span data-stu-id="fa57c-166">Count the lines of this sequence.</span></span> <span data-ttu-id="fa57c-167">Resultatene vil bli brukt med navnet "blokk" separat for forskjellige retninger.</span><span class="sxs-lookup"><span data-stu-id="fa57c-167">The results will be used with the name “block” separately for different directions.</span></span> <span data-ttu-id="fa57c-168">Verdien "Import" vil bli brukt for hvilke som helst Intrastat-transaksjoner for ankomster.</span><span class="sxs-lookup"><span data-stu-id="fa57c-168">Value “Import” will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="fa57c-169">Verdien "Eksport" vil bli brukt for hvilke som helst Intrastat-transaksjoner for utsendelser.</span><span class="sxs-lookup"><span data-stu-id="fa57c-169">The value “Export” will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="fa57c-170">Se på dette som et virtuelt Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="fa57c-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="fa57c-171">For hver transaksjon fylles det ut en rad der den første kolonnen"blokk" fylles ut med verdiene "Import" og "Eksport".</span><span class="sxs-lookup"><span data-stu-id="fa57c-171">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span>  
42. <span data-ttu-id="fa57c-172">Utvid Intrastat\Data: Sekvens i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="fa57c-173">Velg Intrastat\Data: Sekvens\Ankomster? i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="fa57c-174">Klikk Rediger-knappen for feltet Navn på innsamlet datanøkkel.</span><span class="sxs-lookup"><span data-stu-id="fa57c-174">Click Edit button for the ‘Collected data key name’ field.</span></span>
    * <span data-ttu-id="fa57c-175">Tell linjene i denne sekvensen.</span><span class="sxs-lookup"><span data-stu-id="fa57c-175">Count the lines of this sequence.</span></span> <span data-ttu-id="fa57c-176">Resultatene blir lagret ved hjelp av navnet "post".</span><span class="sxs-lookup"><span data-stu-id="fa57c-176">The results will be memorized using the name “record”.</span></span>  
45. <span data-ttu-id="fa57c-177">Velg $RecName i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="fa57c-178">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="fa57c-178">Click Add data source.</span></span>
47. <span data-ttu-id="fa57c-179">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fa57c-179">Click Save.</span></span>
48. <span data-ttu-id="fa57c-180">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fa57c-180">Close the page.</span></span>
49. <span data-ttu-id="fa57c-181">Klikk Rediger-knappen for feltet Verdi for innsamlet datanøkkel.</span><span class="sxs-lookup"><span data-stu-id="fa57c-181">Click Edit button for the ‘Collected data key value’ field</span></span>
50. <span data-ttu-id="fa57c-182">I Formel-feltet skriver du inn Intrastat.CommodityRecord.CommodityCode.</span><span class="sxs-lookup"><span data-stu-id="fa57c-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="fa57c-183">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fa57c-183">Click Save.</span></span>
52. <span data-ttu-id="fa57c-184">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fa57c-184">Close the page.</span></span>
    * <span data-ttu-id="fa57c-185">Tell linjene i denne sekvensen.</span><span class="sxs-lookup"><span data-stu-id="fa57c-185">Count the lines of this sequence.</span></span> <span data-ttu-id="fa57c-186">Resultatene vil bli brukt med navnet "post" separat for forskjellige varekoder.</span><span class="sxs-lookup"><span data-stu-id="fa57c-186">The results will be used with the name “record” separately for different commodity codes.</span></span> <span data-ttu-id="fa57c-187">Se på dette som et virtuelt Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="fa57c-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="fa57c-188">For hver transaksjon fylles det ut en rad der den første kolonnen "blokk" fylles ut med verdiene "Import" og "Export" henholdsvis, og den andre blokken "post" med varekodeverdien</span><span class="sxs-lookup"><span data-stu-id="fa57c-188">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly and the second block “record” is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="fa57c-189">Velg Intrastat\Data: Sekvens\Fordelinger? i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="fa57c-190">Klikk Rediger-knappen for feltet Navn på innsamlet datanøkkel.</span><span class="sxs-lookup"><span data-stu-id="fa57c-190">Click Edit button for the ‘Collected data key name’ field</span></span>
55. <span data-ttu-id="fa57c-191">Velg $RecName i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="fa57c-192">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="fa57c-192">Click Add data source.</span></span>
57. <span data-ttu-id="fa57c-193">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fa57c-193">Click Save.</span></span>
58. <span data-ttu-id="fa57c-194">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fa57c-194">Close the page.</span></span>
59. <span data-ttu-id="fa57c-195">Klikk Rediger-knappen for feltet Verdi for innsamlet datanøkkel.</span><span class="sxs-lookup"><span data-stu-id="fa57c-195">Click the Edit button for the ‘Collected data key value’ field.</span></span>
60. <span data-ttu-id="fa57c-196">I Formel-feltet skriver du inn Intrastat.CommodityRecord.CommodityCode.</span><span class="sxs-lookup"><span data-stu-id="fa57c-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="fa57c-197">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fa57c-197">Click Save.</span></span>
62. <span data-ttu-id="fa57c-198">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fa57c-198">Close the page.</span></span>
63. <span data-ttu-id="fa57c-199">Utvid Intrastat\Data: Sekvens\Fordelinger: Sekvens? i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="fa57c-200">Utvid Intrastat\Data: Sekvens\Fordelinger: Sekvens?\Post = Intrastat.CommodityRecord i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="fa57c-201">Klikk Formater-kategorien.</span><span class="sxs-lookup"><span data-stu-id="fa57c-201">Click the Format tab.</span></span>
66. <span data-ttu-id="fa57c-202">Velg Intrastat\Data\Fordelinger\Post\Fakturabeløp EUR i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="fa57c-203">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="fa57c-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="fa57c-204">Klikk Rediger-knappen for feltet Navn på innsamlet datanøkkel.</span><span class="sxs-lookup"><span data-stu-id="fa57c-204">Click the Edit button for the ‘Collected data key name’ field.</span></span>
69. <span data-ttu-id="fa57c-205">Velg $InvName i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="fa57c-206">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="fa57c-206">Click Add data source.</span></span>
71. <span data-ttu-id="fa57c-207">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fa57c-207">Click Save.</span></span>
72. <span data-ttu-id="fa57c-208">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fa57c-208">Close the page.</span></span>
    * <span data-ttu-id="fa57c-209">Summer de fakturerte beløpsverdiene for linjer i denne sekvensen.</span><span class="sxs-lookup"><span data-stu-id="fa57c-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="fa57c-210">Resultatene vil bli brukt med navnet "InvoicedAmountEUR" separat for forskjellige Intrastat-retninger og varekoder.</span><span class="sxs-lookup"><span data-stu-id="fa57c-210">The results will be used with the name “InvoicedAmountEUR” separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="fa57c-211">Se på dette som en virtuell opprettelse i Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="fa57c-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="fa57c-212">For hver transaksjon fylles det ut en rad der den første kolonnen"blokk" fylles ut med verdiene "Import" og "Eksport".</span><span class="sxs-lookup"><span data-stu-id="fa57c-212">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span> <span data-ttu-id="fa57c-213">Den andre blokken "post" fylles ut med varekodeverdien og den tredje kolonnen "InvoicedAmountEUR" fylles ut med fakturabeløpsverdien.</span><span class="sxs-lookup"><span data-stu-id="fa57c-213">The second block “record” is filled with the commodity code value, and the third column “InvoicedAmountEUR” is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="fa57c-214">Utvid Intrastat\Data\Ankomster? i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="fa57c-215">Utvid Intrastat\Data\Ankomster?\Post = Intrastat.CommodityRecord i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="fa57c-216">Klikk Formater-kategorien.</span><span class="sxs-lookup"><span data-stu-id="fa57c-216">Click the Format tab.</span></span>
76. <span data-ttu-id="fa57c-217">Velg Intrastat\Data\Ankomster\Post\Fakturabeløp EUR i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="fa57c-218">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="fa57c-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="fa57c-219">Klikk Rediger-knappen for feltet Navn på innsamlet datanøkkel.</span><span class="sxs-lookup"><span data-stu-id="fa57c-219">Click the Edit button for the ‘Collected data key name’ field.</span></span>
79. <span data-ttu-id="fa57c-220">Velg $InvName i treet.</span><span class="sxs-lookup"><span data-stu-id="fa57c-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="fa57c-221">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="fa57c-221">Click Add data source.</span></span>
81. <span data-ttu-id="fa57c-222">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fa57c-222">Click Save.</span></span>
82. <span data-ttu-id="fa57c-223">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fa57c-223">Close the page.</span></span>
83. <span data-ttu-id="fa57c-224">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fa57c-224">Click Save.</span></span>
84. <span data-ttu-id="fa57c-225">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fa57c-225">Close the page.</span></span>

