--- 
title: Opprette formatkonfigurasjoner for elektronisk rapportering
description: "De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en formatkonfigurasjon for elektronisk rapportering (ER)."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8c11f64fd899b8be4e6c3179913787eb2c32c6c6
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---
# <a name="create-electronic-reporting-er-format-configurations"></a><span data-ttu-id="f4dd9-103">Opprette formatkonfigurasjoner for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="f4dd9-103">Create Electronic reporting (ER) format configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4dd9-104">De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en formatkonfigurasjon for elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="f4dd9-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="f4dd9-105">Denne formatkonfigurasjonen definerer formatet for elektroniske dokumenter som skal brukes til behandling av betalinger.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="f4dd9-106">I dette eksemplet oppretter du en formatkonfigurasjon for eksempelfirmaet Litware, Inc. For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren Tilordne modell til valgte datakilder.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="f4dd9-107">Opprette en ny formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="f4dd9-107">Create a new format configuration</span></span>
1. <span data-ttu-id="f4dd9-108">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f4dd9-109">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="f4dd9-110">Velg Betalinger (forenklet model) i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="f4dd9-111">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="f4dd9-112">I feltet Ny angir du Format basert på datamodell PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="f4dd9-113">Skriv inn BACS (britisk fiktivt) i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="f4dd9-114">BACS (britisk fiktivt)</span><span class="sxs-lookup"><span data-stu-id="f4dd9-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="f4dd9-115">I Beskrivelse-feltet skriver du inn BACS-leverandørbetalingsformat (fiktivt Storbritannia).</span><span class="sxs-lookup"><span data-stu-id="f4dd9-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="f4dd9-116">BACS-leverandørbetalingsformat (fiktivt Storbritannia)</span><span class="sxs-lookup"><span data-stu-id="f4dd9-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="f4dd9-117">Den aktive konfigurasjonsleverandøren angis automatisk her.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="f4dd9-118">Denne leverandøren vil kunne vedlikeholde denne konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="f4dd9-119">Andre leverandører kan bruke denne konfigurasjonen, men kan ikke vedlikeholde den.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="f4dd9-120">Du kan definere et bestemt format for elektronisk dokument.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="f4dd9-121">La dette feltet stå tomt hvis du vil velge et format under kjøring.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="f4dd9-122">Angi eller velg en verdi i feltet Definisjon av datamodell.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="f4dd9-123">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-123">Click Create configuration.</span></span>
    * <span data-ttu-id="f4dd9-124">En ny konfigurasjon er opprettet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-124">A new configuration has been created.</span></span> <span data-ttu-id="f4dd9-125">Utkastversjonen kan brukes til å lagre utformingsformatet for behandling av elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="f4dd9-126">Designformat for elektronisk dokument</span><span class="sxs-lookup"><span data-stu-id="f4dd9-126">Design format of electronic document</span></span>
1. <span data-ttu-id="f4dd9-127">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-127">Click Designer.</span></span>
2. <span data-ttu-id="f4dd9-128">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="f4dd9-129">Velg Felles\Fil i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="f4dd9-130">I Navn-feltet skriver du inn Xml.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="f4dd9-131">XML</span><span class="sxs-lookup"><span data-stu-id="f4dd9-131">Xml</span></span>  
5. <span data-ttu-id="f4dd9-132">I Koding-feltet skriver du inn UTF-8.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="f4dd9-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="f4dd9-133">UTF-8</span></span>  
6. <span data-ttu-id="f4dd9-134">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-134">Click OK.</span></span>
7. <span data-ttu-id="f4dd9-135">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="f4dd9-136">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="f4dd9-137">I Navn-feltet skriver du inn Melding.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="f4dd9-138">Melding</span><span class="sxs-lookup"><span data-stu-id="f4dd9-138">Message</span></span>  
10. <span data-ttu-id="f4dd9-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-139">Click OK.</span></span>
11. <span data-ttu-id="f4dd9-140">Velg Xml\Melding i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="f4dd9-141">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-141">Click Add Element.</span></span>
13. <span data-ttu-id="f4dd9-142">I Navn-feltet skriver du inn ProcessingDate.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="f4dd9-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="f4dd9-143">ProcessingDate</span></span>  
14. <span data-ttu-id="f4dd9-144">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-144">Click OK.</span></span>
15. <span data-ttu-id="f4dd9-145">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-145">Click Add Element.</span></span>
16. <span data-ttu-id="f4dd9-146">I Navn-feltet skriver du inn MessageId.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="f4dd9-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="f4dd9-147">MessageId</span></span>  
17. <span data-ttu-id="f4dd9-148">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-148">Click OK.</span></span>
18. <span data-ttu-id="f4dd9-149">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-149">Click Add Element.</span></span>
19. <span data-ttu-id="f4dd9-150">Skriv inn Betalinger i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="f4dd9-151">Betalinger</span><span class="sxs-lookup"><span data-stu-id="f4dd9-151">Payments</span></span>  
20. <span data-ttu-id="f4dd9-152">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-152">Click OK.</span></span>
21. <span data-ttu-id="f4dd9-153">Velg Xml\Melding\Betalinger i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="f4dd9-154">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-154">Click Add Element.</span></span>
23. <span data-ttu-id="f4dd9-155">I Navn-feltet skriver du inn Element.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="f4dd9-156">Vare</span><span class="sxs-lookup"><span data-stu-id="f4dd9-156">Item</span></span>  
24. <span data-ttu-id="f4dd9-157">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-157">Click OK.</span></span>
25. <span data-ttu-id="f4dd9-158">Velg Xml\Melding\Betalinger\Vare i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="f4dd9-159">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="f4dd9-160">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="f4dd9-161">I Navn-feltet skriver du inn ID.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="f4dd9-162">ID</span><span class="sxs-lookup"><span data-stu-id="f4dd9-162">Id</span></span>  
29. <span data-ttu-id="f4dd9-163">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-163">Click OK.</span></span>
30. <span data-ttu-id="f4dd9-164">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="f4dd9-165">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="f4dd9-166">I Navn-feltet skriver du inn Leverandør.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="f4dd9-167">Leverandør</span><span class="sxs-lookup"><span data-stu-id="f4dd9-167">Vendor</span></span>  
33. <span data-ttu-id="f4dd9-168">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-168">Click OK.</span></span>
34. <span data-ttu-id="f4dd9-169">Velg Xml\Melding\Betalinger\Vare\Leverandør i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="f4dd9-170">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-170">Click Add Element.</span></span>
36. <span data-ttu-id="f4dd9-171">I Navn-feltet skriver du inn Navn.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="f4dd9-172">Navn</span><span class="sxs-lookup"><span data-stu-id="f4dd9-172">Name</span></span>  
37. <span data-ttu-id="f4dd9-173">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-173">Click OK.</span></span>
38. <span data-ttu-id="f4dd9-174">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-174">Click Add Element.</span></span>
39. <span data-ttu-id="f4dd9-175">I Navn-feltet skriver du inn Bank.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="f4dd9-176">Bank</span><span class="sxs-lookup"><span data-stu-id="f4dd9-176">Bank</span></span>  
40. <span data-ttu-id="f4dd9-177">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-177">Click OK.</span></span>
41. <span data-ttu-id="f4dd9-178">Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="f4dd9-179">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-179">Click Add Element.</span></span>
43. <span data-ttu-id="f4dd9-180">Skriv inn RoutingNumber i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="f4dd9-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="f4dd9-181">RoutingNumber</span></span>  
44. <span data-ttu-id="f4dd9-182">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-182">Click OK.</span></span>
45. <span data-ttu-id="f4dd9-183">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-183">Click Add Element.</span></span>
46. <span data-ttu-id="f4dd9-184">Skriv inn AccountNumber i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="f4dd9-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="f4dd9-185">AccountNumber</span></span>  
47. <span data-ttu-id="f4dd9-186">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-186">Click OK.</span></span>
48. <span data-ttu-id="f4dd9-187">Velg Xml\Melding\Betalinger\Vare\Leverandør i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="f4dd9-188">Klikk Kopier.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-188">Click Copy.</span></span>
50. <span data-ttu-id="f4dd9-189">Velg Xml\Melding\Betalinger\Vare i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="f4dd9-190">Klikk Lim inn.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-190">Click Paste.</span></span>
52. <span data-ttu-id="f4dd9-191">I Navn-feltet skriver du inn Betaler.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="f4dd9-192">Betaler</span><span class="sxs-lookup"><span data-stu-id="f4dd9-192">Payer</span></span>  
53. <span data-ttu-id="f4dd9-193">Velg Xml\Melding\Betalinger\Vare i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="f4dd9-194">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-194">Click Add Element.</span></span>
55. <span data-ttu-id="f4dd9-195">I Navn-feltet skriver du inn Valuta.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="f4dd9-196">Valuta</span><span class="sxs-lookup"><span data-stu-id="f4dd9-196">Currency</span></span>  
56. <span data-ttu-id="f4dd9-197">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-197">Click OK.</span></span>
57. <span data-ttu-id="f4dd9-198">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-198">Click Add Element.</span></span>
58. <span data-ttu-id="f4dd9-199">Skriv inn Beskrivelse i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="f4dd9-200">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f4dd9-200">Description</span></span>  
59. <span data-ttu-id="f4dd9-201">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-201">Click OK.</span></span>
60. <span data-ttu-id="f4dd9-202">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-202">Click Add Element.</span></span>
61. <span data-ttu-id="f4dd9-203">I Navn-feltet skriver du inn TransDate.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="f4dd9-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="f4dd9-204">TransDate</span></span>  
62. <span data-ttu-id="f4dd9-205">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-205">Click OK.</span></span>
63. <span data-ttu-id="f4dd9-206">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-206">Click Add Element.</span></span>
64. <span data-ttu-id="f4dd9-207">I Navn-feltet skriver du inn Beløp.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="f4dd9-208">Beløp</span><span class="sxs-lookup"><span data-stu-id="f4dd9-208">Amount</span></span>  
65. <span data-ttu-id="f4dd9-209">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="f4dd9-210">Klargjøre formatkomponenter for tilordning til datamodellelementer</span><span class="sxs-lookup"><span data-stu-id="f4dd9-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="f4dd9-211">Velg Xml\Melding\ProcessingDate i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="f4dd9-212">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="f4dd9-213">Velg Tekst\DateTime i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="f4dd9-214">Skriv inn åååå-MM-dd i Format-feltet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="f4dd9-215">åååå-MM-dd</span><span class="sxs-lookup"><span data-stu-id="f4dd9-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="f4dd9-216">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-216">Click OK.</span></span>
6. <span data-ttu-id="f4dd9-217">Velg Xml\Melding\Betalinger\Vare\TransDate i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="f4dd9-218">Klikk Legg til dato/klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="f4dd9-219">Skriv inn åååå-MM-dd i Format-feltet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="f4dd9-220">åååå-MM-dd</span><span class="sxs-lookup"><span data-stu-id="f4dd9-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="f4dd9-221">Velg Dato i feltet DateTime-type.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="f4dd9-222">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-222">Click OK.</span></span>
11. <span data-ttu-id="f4dd9-223">Velg Xml\Melding\MessageId i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="f4dd9-224">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="f4dd9-225">Velg Tekst\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="f4dd9-226">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-226">Click OK.</span></span>
15. <span data-ttu-id="f4dd9-227">Velg Xml\Melding\Betalinger\Vare\Leverandør\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="f4dd9-228">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-228">Click Add String.</span></span>
17. <span data-ttu-id="f4dd9-229">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-229">Click OK.</span></span>
18. <span data-ttu-id="f4dd9-230">Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank\RoutingNumber i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="f4dd9-231">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-231">Click Add String.</span></span>
20. <span data-ttu-id="f4dd9-232">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-232">Click OK.</span></span>
21. <span data-ttu-id="f4dd9-233">Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank\AccountNumber i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="f4dd9-234">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-234">Click Add String.</span></span>
23. <span data-ttu-id="f4dd9-235">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-235">Click OK.</span></span>
24. <span data-ttu-id="f4dd9-236">Velg Xml\Melding\Betalinger\Vare\Leverandør\Betaler\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="f4dd9-237">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-237">Click Add String.</span></span>
26. <span data-ttu-id="f4dd9-238">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-238">Click OK.</span></span>
27. <span data-ttu-id="f4dd9-239">Velg Xml\Melding\Betalinger\Vare\Betaler\Bank\RoutingNumber i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="f4dd9-240">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-240">Click Add String.</span></span>
29. <span data-ttu-id="f4dd9-241">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-241">Click OK.</span></span>
30. <span data-ttu-id="f4dd9-242">Velg Xml\Melding\Betalinger\Vare\Betaler\Bank\AccountNumber i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="f4dd9-243">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-243">Click Add String.</span></span>
32. <span data-ttu-id="f4dd9-244">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-244">Click OK.</span></span>
33. <span data-ttu-id="f4dd9-245">Velg Xml\Melding\Betalinger\Vare\Valuta i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="f4dd9-246">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-246">Click Add String.</span></span>
35. <span data-ttu-id="f4dd9-247">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-247">Click OK.</span></span>
36. <span data-ttu-id="f4dd9-248">Velg Xml\Melding\Betalinger\Vare\Leverandør\Beskrivelse i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="f4dd9-249">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-249">Click Add String.</span></span>
38. <span data-ttu-id="f4dd9-250">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-250">Click OK.</span></span>
39. <span data-ttu-id="f4dd9-251">Velg Xml\Melding\Betalinger\Vare\Beløp i treet.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="f4dd9-252">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-252">Click Add String.</span></span>
41. <span data-ttu-id="f4dd9-253">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-253">Click OK.</span></span>
42. <span data-ttu-id="f4dd9-254">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-254">Click Save.</span></span>
43. <span data-ttu-id="f4dd9-255">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-255">Close the page.</span></span>


