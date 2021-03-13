---
title: ER Bruke finansdimensjoner som en datakilde (del 3 - Utforme rapporten)
description: Dette emnet beskriver hvordan du konfigurerer en ER-modell (Elektronisk rapportering) for å bruke finansdimensjoner som en datakilde for ER-rapporter. (Del 3)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0d6da96850e04d5e975b3febbfae2737c8a86af
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092306"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="a1492-104">ER Bruke finansdimensjoner som en datakilde (del 3 - Utforme rapporten)</span><span class="sxs-lookup"><span data-stu-id="a1492-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a1492-105">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="a1492-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="a1492-106">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="a1492-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="a1492-107">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke finansdimensjoner som datakilde (del 2: Modelltilordning).</span><span class="sxs-lookup"><span data-stu-id="a1492-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="a1492-108">Utforme en rapport for å presentere finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="a1492-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="a1492-109">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="a1492-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a1492-110">Velg Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a1492-111">Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a1492-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="a1492-112">I feltet Ny angir du Format basert på datamodellen Eksempelmodell for finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="a1492-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="a1492-113">Bruk modellen som ble opprettet på forhånd som datakilde for den nye rapporten.</span><span class="sxs-lookup"><span data-stu-id="a1492-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="a1492-114">Skriv inn Finansjournalrapport i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1492-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="a1492-115">Velg Oppføring i Definisjon av datamodell-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1492-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="a1492-116">Klikk på Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="a1492-116">Click Create configuration.</span></span>
8. <span data-ttu-id="a1492-117">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="a1492-117">Click Designer.</span></span>
9. <span data-ttu-id="a1492-118">Klikk på Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a1492-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="a1492-119">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="a1492-120">Skriv inn Rot i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1492-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="a1492-121">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="a1492-121">Click OK.</span></span>
13. <span data-ttu-id="a1492-122">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a1492-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="a1492-123">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="a1492-124">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="a1492-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="a1492-125">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="a1492-125">Click OK.</span></span>
17. <span data-ttu-id="a1492-126">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a1492-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="a1492-127">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="a1492-128">I Navn-feltet skriver du inn Journal.</span><span class="sxs-lookup"><span data-stu-id="a1492-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="a1492-129">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="a1492-129">Click OK.</span></span>
21. <span data-ttu-id="a1492-130">Velg Rot: XML-element\Journal: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="a1492-131">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a1492-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="a1492-132">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="a1492-133">Skriv inn Parti i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1492-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="a1492-134">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="a1492-134">Click OK.</span></span>
26. <span data-ttu-id="a1492-135">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a1492-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="a1492-136">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="a1492-137">Skriv inn Transaksjon i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1492-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="a1492-138">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="a1492-138">Click OK.</span></span>
30. <span data-ttu-id="a1492-139">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="a1492-140">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a1492-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="a1492-141">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="a1492-142">I Navn-feltet skriver du inn Bilag.</span><span class="sxs-lookup"><span data-stu-id="a1492-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="a1492-143">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="a1492-143">Click OK.</span></span>
35. <span data-ttu-id="a1492-144">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="a1492-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="a1492-145">Skriv inn Dato i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1492-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="a1492-146">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="a1492-146">Click OK.</span></span>
38. <span data-ttu-id="a1492-147">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="a1492-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="a1492-148">I Navn-feltet skriver du inn Valuta.</span><span class="sxs-lookup"><span data-stu-id="a1492-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="a1492-149">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="a1492-149">Click OK.</span></span>
41. <span data-ttu-id="a1492-150">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="a1492-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="a1492-151">Skriv inn Dt i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1492-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="a1492-152">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="a1492-152">Click OK.</span></span>
44. <span data-ttu-id="a1492-153">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="a1492-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="a1492-154">Skriv inn Kt i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1492-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="a1492-155">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="a1492-155">Click OK.</span></span>
47. <span data-ttu-id="a1492-156">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a1492-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="a1492-157">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="a1492-158">Skriv inn Dimensjoner i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1492-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="a1492-159">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="a1492-159">Click OK.</span></span>
51. <span data-ttu-id="a1492-160">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="a1492-161">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a1492-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="a1492-162">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="a1492-163">I Navn-feltet skriver du inn Kode.</span><span class="sxs-lookup"><span data-stu-id="a1492-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="a1492-164">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="a1492-164">Click OK.</span></span>
56. <span data-ttu-id="a1492-165">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="a1492-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="a1492-166">Skriv inn Verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1492-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="a1492-167">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="a1492-167">Click OK.</span></span>
59. <span data-ttu-id="a1492-168">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="a1492-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="a1492-169">Skriv inn Beskr i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a1492-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="a1492-170">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="a1492-170">Click OK.</span></span>
<span data-ttu-id="a1492-171">![Side med ER-operasjonsutforming](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="a1492-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="a1492-172">Tilordne rapportelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="a1492-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="a1492-173">Klikk på fanen Tilordning.</span><span class="sxs-lookup"><span data-stu-id="a1492-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="a1492-174">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a1492-175">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="a1492-176">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="a1492-177">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="a1492-178">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element\Beskr: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="a1492-179">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Beskrivelse: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="a1492-180">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="a1492-180">Click Bind.</span></span>
9. <span data-ttu-id="a1492-181">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element\Verdi: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="a1492-182">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Kode: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="a1492-183">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="a1492-183">Click Bind.</span></span>
12. <span data-ttu-id="a1492-184">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element\Kode: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="a1492-185">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Navn: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="a1492-186">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="a1492-186">Click Bind.</span></span>
15. <span data-ttu-id="a1492-187">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="a1492-188">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="a1492-189">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="a1492-189">Click Bind.</span></span>
18. <span data-ttu-id="a1492-190">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Kt: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="a1492-191">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Kredit: Reell i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="a1492-192">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="a1492-192">Click Bind.</span></span>
21. <span data-ttu-id="a1492-193">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dt: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="a1492-194">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Debet: Reell i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="a1492-195">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="a1492-195">Click Bind.</span></span>
24. <span data-ttu-id="a1492-196">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Valuta: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="a1492-197">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Valuta: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="a1492-198">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="a1492-198">Click Bind.</span></span>
27. <span data-ttu-id="a1492-199">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dato: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="a1492-200">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dato: Dato i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="a1492-201">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="a1492-201">Click Bind.</span></span>
30. <span data-ttu-id="a1492-202">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Bilag: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="a1492-203">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Bilag: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="a1492-204">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="a1492-204">Click Bind.</span></span>
33. <span data-ttu-id="a1492-205">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="a1492-206">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="a1492-207">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="a1492-207">Click Bind.</span></span>
36. <span data-ttu-id="a1492-208">Velg Rot: XML-element\Journal: XML-element\Parti: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="a1492-209">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Parti: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="a1492-210">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="a1492-210">Click Bind.</span></span>
39. <span data-ttu-id="a1492-211">Velg Rot: XML-element\Journal: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="a1492-212">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="a1492-213">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="a1492-213">Click Bind.</span></span>
42. <span data-ttu-id="a1492-214">Velg Rot: XML-element\Firma: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="a1492-215">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Firma: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="a1492-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="a1492-216">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="a1492-216">Click Bind.</span></span>
45. <span data-ttu-id="a1492-217">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="a1492-217">Click Save.</span></span>
46. <span data-ttu-id="a1492-218">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a1492-218">Close the page.</span></span>
<span data-ttu-id="a1492-219">![Side med ER-operasjonsutforming](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="a1492-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

