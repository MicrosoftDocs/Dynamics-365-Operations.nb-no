--- 
title: Opprette en formatkonfigurasjon for elektronisk rapportering (ER)
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 04817d1f1851e43679995641e8b0ff99edaa83ad
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="f1456-103">Opprette en formatkonfigurasjon for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="f1456-103">Create a format configuration for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1456-104">De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en formatkonfigurasjon for elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="f1456-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="f1456-105">Denne formatkonfigurasjonen definerer formatet for elektroniske dokumenter som skal brukes til behandling av betalinger.</span><span class="sxs-lookup"><span data-stu-id="f1456-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="f1456-106">I dette eksemplet oppretter du en formatkonfigurasjon for eksempelfirmaet Litware, Inc. For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren Tilordne modell til valgte datakilder.</span><span class="sxs-lookup"><span data-stu-id="f1456-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="f1456-107">Opprette en ny formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="f1456-107">Create a new format configuration</span></span>
1. <span data-ttu-id="f1456-108">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="f1456-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f1456-109">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="f1456-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="f1456-110">Velg Betalinger (forenklet model) i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="f1456-111">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f1456-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="f1456-112">I feltet Ny angir du Format basert på datamodell PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="f1456-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="f1456-113">Skriv inn BACS (britisk fiktivt) i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f1456-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="f1456-114">BACS (britisk fiktivt)</span><span class="sxs-lookup"><span data-stu-id="f1456-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="f1456-115">I Beskrivelse-feltet skriver du inn BACS-leverandørbetalingsformat (fiktivt Storbritannia).</span><span class="sxs-lookup"><span data-stu-id="f1456-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="f1456-116">BACS-leverandørbetalingsformat (fiktivt Storbritannia)</span><span class="sxs-lookup"><span data-stu-id="f1456-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="f1456-117">Den aktive konfigurasjonsleverandøren angis automatisk her.</span><span class="sxs-lookup"><span data-stu-id="f1456-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="f1456-118">Denne leverandøren vil kunne vedlikeholde denne konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="f1456-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="f1456-119">Andre leverandører kan bruke denne konfigurasjonen, men kan ikke vedlikeholde den.</span><span class="sxs-lookup"><span data-stu-id="f1456-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="f1456-120">Du kan definere et bestemt format for elektronisk dokument.</span><span class="sxs-lookup"><span data-stu-id="f1456-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="f1456-121">La dette feltet stå tomt hvis du vil velge et format under kjøring.</span><span class="sxs-lookup"><span data-stu-id="f1456-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="f1456-122">Angi eller velg en verdi i feltet Definisjon av datamodell.</span><span class="sxs-lookup"><span data-stu-id="f1456-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="f1456-123">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="f1456-123">Click Create configuration.</span></span>
    * <span data-ttu-id="f1456-124">En ny konfigurasjon er opprettet.</span><span class="sxs-lookup"><span data-stu-id="f1456-124">A new configuration has been created.</span></span> <span data-ttu-id="f1456-125">Utkastversjonen kan brukes til å lagre utformingsformatet for behandling av elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="f1456-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="f1456-126">Designformat for elektronisk dokument</span><span class="sxs-lookup"><span data-stu-id="f1456-126">Design format of electronic document</span></span>
1. <span data-ttu-id="f1456-127">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="f1456-127">Click Designer.</span></span>
2. <span data-ttu-id="f1456-128">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f1456-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="f1456-129">Velg Felles\Fil i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="f1456-130">I Navn-feltet skriver du inn Xml.</span><span class="sxs-lookup"><span data-stu-id="f1456-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="f1456-131">XML</span><span class="sxs-lookup"><span data-stu-id="f1456-131">Xml</span></span>  
5. <span data-ttu-id="f1456-132">I Koding-feltet skriver du inn UTF-8.</span><span class="sxs-lookup"><span data-stu-id="f1456-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="f1456-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="f1456-133">UTF-8</span></span>  
6. <span data-ttu-id="f1456-134">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-134">Click OK.</span></span>
7. <span data-ttu-id="f1456-135">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f1456-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="f1456-136">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="f1456-137">I Navn-feltet skriver du inn Melding.</span><span class="sxs-lookup"><span data-stu-id="f1456-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="f1456-138">Melding</span><span class="sxs-lookup"><span data-stu-id="f1456-138">Message</span></span>  
10. <span data-ttu-id="f1456-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-139">Click OK.</span></span>
11. <span data-ttu-id="f1456-140">Velg Xml\Melding i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="f1456-141">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f1456-141">Click Add Element.</span></span>
13. <span data-ttu-id="f1456-142">I Navn-feltet skriver du inn ProcessingDate.</span><span class="sxs-lookup"><span data-stu-id="f1456-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="f1456-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="f1456-143">ProcessingDate</span></span>  
14. <span data-ttu-id="f1456-144">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-144">Click OK.</span></span>
15. <span data-ttu-id="f1456-145">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f1456-145">Click Add Element.</span></span>
16. <span data-ttu-id="f1456-146">I Navn-feltet skriver du inn MessageId.</span><span class="sxs-lookup"><span data-stu-id="f1456-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="f1456-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="f1456-147">MessageId</span></span>  
17. <span data-ttu-id="f1456-148">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-148">Click OK.</span></span>
18. <span data-ttu-id="f1456-149">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f1456-149">Click Add Element.</span></span>
19. <span data-ttu-id="f1456-150">Skriv inn Betalinger i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f1456-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="f1456-151">Betalinger</span><span class="sxs-lookup"><span data-stu-id="f1456-151">Payments</span></span>  
20. <span data-ttu-id="f1456-152">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-152">Click OK.</span></span>
21. <span data-ttu-id="f1456-153">Velg Xml\Melding\Betalinger i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="f1456-154">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f1456-154">Click Add Element.</span></span>
23. <span data-ttu-id="f1456-155">I Navn-feltet skriver du inn Element.</span><span class="sxs-lookup"><span data-stu-id="f1456-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="f1456-156">Vare</span><span class="sxs-lookup"><span data-stu-id="f1456-156">Item</span></span>  
24. <span data-ttu-id="f1456-157">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-157">Click OK.</span></span>
25. <span data-ttu-id="f1456-158">Velg Xml\Melding\Betalinger\Vare i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="f1456-159">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f1456-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="f1456-160">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="f1456-161">I Navn-feltet skriver du inn ID.</span><span class="sxs-lookup"><span data-stu-id="f1456-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="f1456-162">ID</span><span class="sxs-lookup"><span data-stu-id="f1456-162">Id</span></span>  
29. <span data-ttu-id="f1456-163">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-163">Click OK.</span></span>
30. <span data-ttu-id="f1456-164">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f1456-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="f1456-165">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="f1456-166">I Navn-feltet skriver du inn Leverandør.</span><span class="sxs-lookup"><span data-stu-id="f1456-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="f1456-167">Leverandør</span><span class="sxs-lookup"><span data-stu-id="f1456-167">Vendor</span></span>  
33. <span data-ttu-id="f1456-168">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-168">Click OK.</span></span>
34. <span data-ttu-id="f1456-169">Velg Xml\Melding\Betalinger\Vare\Leverandør i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="f1456-170">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f1456-170">Click Add Element.</span></span>
36. <span data-ttu-id="f1456-171">I Navn-feltet skriver du inn Navn.</span><span class="sxs-lookup"><span data-stu-id="f1456-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="f1456-172">Navn</span><span class="sxs-lookup"><span data-stu-id="f1456-172">Name</span></span>  
37. <span data-ttu-id="f1456-173">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-173">Click OK.</span></span>
38. <span data-ttu-id="f1456-174">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f1456-174">Click Add Element.</span></span>
39. <span data-ttu-id="f1456-175">I Navn-feltet skriver du inn Bank.</span><span class="sxs-lookup"><span data-stu-id="f1456-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="f1456-176">Bank</span><span class="sxs-lookup"><span data-stu-id="f1456-176">Bank</span></span>  
40. <span data-ttu-id="f1456-177">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-177">Click OK.</span></span>
41. <span data-ttu-id="f1456-178">Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="f1456-179">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f1456-179">Click Add Element.</span></span>
43. <span data-ttu-id="f1456-180">Skriv inn RoutingNumber i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="f1456-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="f1456-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="f1456-181">RoutingNumber</span></span>  
44. <span data-ttu-id="f1456-182">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-182">Click OK.</span></span>
45. <span data-ttu-id="f1456-183">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f1456-183">Click Add Element.</span></span>
46. <span data-ttu-id="f1456-184">Skriv inn AccountNumber i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="f1456-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="f1456-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="f1456-185">AccountNumber</span></span>  
47. <span data-ttu-id="f1456-186">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-186">Click OK.</span></span>
48. <span data-ttu-id="f1456-187">Velg Xml\Melding\Betalinger\Vare\Leverandør i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="f1456-188">Klikk Kopier.</span><span class="sxs-lookup"><span data-stu-id="f1456-188">Click Copy.</span></span>
50. <span data-ttu-id="f1456-189">Velg Xml\Melding\Betalinger\Vare i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="f1456-190">Klikk Lim inn.</span><span class="sxs-lookup"><span data-stu-id="f1456-190">Click Paste.</span></span>
52. <span data-ttu-id="f1456-191">I Navn-feltet skriver du inn Betaler.</span><span class="sxs-lookup"><span data-stu-id="f1456-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="f1456-192">Betaler</span><span class="sxs-lookup"><span data-stu-id="f1456-192">Payer</span></span>  
53. <span data-ttu-id="f1456-193">Velg Xml\Melding\Betalinger\Vare i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="f1456-194">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f1456-194">Click Add Element.</span></span>
55. <span data-ttu-id="f1456-195">I Navn-feltet skriver du inn Valuta.</span><span class="sxs-lookup"><span data-stu-id="f1456-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="f1456-196">Valuta</span><span class="sxs-lookup"><span data-stu-id="f1456-196">Currency</span></span>  
56. <span data-ttu-id="f1456-197">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-197">Click OK.</span></span>
57. <span data-ttu-id="f1456-198">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f1456-198">Click Add Element.</span></span>
58. <span data-ttu-id="f1456-199">Skriv inn Beskrivelse i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f1456-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="f1456-200">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f1456-200">Description</span></span>  
59. <span data-ttu-id="f1456-201">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-201">Click OK.</span></span>
60. <span data-ttu-id="f1456-202">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f1456-202">Click Add Element.</span></span>
61. <span data-ttu-id="f1456-203">I Navn-feltet skriver du inn TransDate.</span><span class="sxs-lookup"><span data-stu-id="f1456-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="f1456-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="f1456-204">TransDate</span></span>  
62. <span data-ttu-id="f1456-205">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-205">Click OK.</span></span>
63. <span data-ttu-id="f1456-206">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="f1456-206">Click Add Element.</span></span>
64. <span data-ttu-id="f1456-207">I Navn-feltet skriver du inn Beløp.</span><span class="sxs-lookup"><span data-stu-id="f1456-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="f1456-208">Beløp</span><span class="sxs-lookup"><span data-stu-id="f1456-208">Amount</span></span>  
65. <span data-ttu-id="f1456-209">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="f1456-210">Klargjøre formatkomponenter for tilordning til datamodellelementer</span><span class="sxs-lookup"><span data-stu-id="f1456-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="f1456-211">Velg Xml\Melding\ProcessingDate i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="f1456-212">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f1456-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="f1456-213">Velg Tekst\DateTime i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="f1456-214">Skriv inn åååå-MM-dd i Format-feltet.</span><span class="sxs-lookup"><span data-stu-id="f1456-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="f1456-215">åååå-MM-dd</span><span class="sxs-lookup"><span data-stu-id="f1456-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="f1456-216">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-216">Click OK.</span></span>
6. <span data-ttu-id="f1456-217">Velg Xml\Melding\Betalinger\Vare\TransDate i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="f1456-218">Klikk Legg til dato/klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="f1456-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="f1456-219">Skriv inn åååå-MM-dd i Format-feltet.</span><span class="sxs-lookup"><span data-stu-id="f1456-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="f1456-220">åååå-MM-dd</span><span class="sxs-lookup"><span data-stu-id="f1456-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="f1456-221">Velg Dato i feltet DateTime-type.</span><span class="sxs-lookup"><span data-stu-id="f1456-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="f1456-222">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-222">Click OK.</span></span>
11. <span data-ttu-id="f1456-223">Velg Xml\Melding\MessageId i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="f1456-224">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f1456-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="f1456-225">Velg Tekst\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="f1456-226">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-226">Click OK.</span></span>
15. <span data-ttu-id="f1456-227">Velg Xml\Melding\Betalinger\Vare\Leverandør\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="f1456-228">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="f1456-228">Click Add String.</span></span>
17. <span data-ttu-id="f1456-229">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-229">Click OK.</span></span>
18. <span data-ttu-id="f1456-230">Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank\RoutingNumber i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="f1456-231">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="f1456-231">Click Add String.</span></span>
20. <span data-ttu-id="f1456-232">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-232">Click OK.</span></span>
21. <span data-ttu-id="f1456-233">Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank\AccountNumber i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="f1456-234">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="f1456-234">Click Add String.</span></span>
23. <span data-ttu-id="f1456-235">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-235">Click OK.</span></span>
24. <span data-ttu-id="f1456-236">Velg Xml\Melding\Betalinger\Vare\Leverandør\Betaler\Navn i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="f1456-237">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="f1456-237">Click Add String.</span></span>
26. <span data-ttu-id="f1456-238">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-238">Click OK.</span></span>
27. <span data-ttu-id="f1456-239">Velg Xml\Melding\Betalinger\Vare\Betaler\Bank\RoutingNumber i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="f1456-240">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="f1456-240">Click Add String.</span></span>
29. <span data-ttu-id="f1456-241">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-241">Click OK.</span></span>
30. <span data-ttu-id="f1456-242">Velg Xml\Melding\Betalinger\Vare\Betaler\Bank\AccountNumber i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="f1456-243">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="f1456-243">Click Add String.</span></span>
32. <span data-ttu-id="f1456-244">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-244">Click OK.</span></span>
33. <span data-ttu-id="f1456-245">Velg Xml\Melding\Betalinger\Vare\Valuta i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="f1456-246">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="f1456-246">Click Add String.</span></span>
35. <span data-ttu-id="f1456-247">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-247">Click OK.</span></span>
36. <span data-ttu-id="f1456-248">Velg Xml\Melding\Betalinger\Vare\Leverandør\Beskrivelse i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="f1456-249">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="f1456-249">Click Add String.</span></span>
38. <span data-ttu-id="f1456-250">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-250">Click OK.</span></span>
39. <span data-ttu-id="f1456-251">Velg Xml\Melding\Betalinger\Vare\Beløp i treet.</span><span class="sxs-lookup"><span data-stu-id="f1456-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="f1456-252">Klikk Legg til streng.</span><span class="sxs-lookup"><span data-stu-id="f1456-252">Click Add String.</span></span>
41. <span data-ttu-id="f1456-253">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1456-253">Click OK.</span></span>
42. <span data-ttu-id="f1456-254">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f1456-254">Click Save.</span></span>
43. <span data-ttu-id="f1456-255">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f1456-255">Close the page.</span></span>


