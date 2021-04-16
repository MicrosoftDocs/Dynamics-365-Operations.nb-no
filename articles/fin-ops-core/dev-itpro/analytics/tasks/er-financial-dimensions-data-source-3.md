---
title: ER Bruke finansdimensjoner som en datakilde (del 3 - Utforme rapporten)
description: Dette emnet beskriver hvordan du konfigurerer en ER-modell (Elektronisk rapportering) for å bruke finansdimensjoner som en datakilde for ER-rapporter. (Del 3)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a3b9a8b5775d2001f3384480e2f9593f2dfa8b1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752418"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="25fd2-104">ER Bruke finansdimensjoner som en datakilde (del 3 - Utforme rapporten)</span><span class="sxs-lookup"><span data-stu-id="25fd2-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25fd2-105">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="25fd2-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="25fd2-106">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="25fd2-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="25fd2-107">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke finansdimensjoner som datakilde (del 2: Modelltilordning).</span><span class="sxs-lookup"><span data-stu-id="25fd2-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="25fd2-108">Utforme en rapport for å presentere finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="25fd2-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="25fd2-109">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="25fd2-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="25fd2-110">Velg Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="25fd2-111">Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="25fd2-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="25fd2-112">I feltet Ny angir du Format basert på datamodellen Eksempelmodell for finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="25fd2-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="25fd2-113">Bruk modellen som ble opprettet på forhånd som datakilde for den nye rapporten.</span><span class="sxs-lookup"><span data-stu-id="25fd2-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="25fd2-114">Skriv inn Finansjournalrapport i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="25fd2-115">Velg Oppføring i Definisjon av datamodell-feltet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="25fd2-116">Klikk på Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="25fd2-116">Click Create configuration.</span></span>
8. <span data-ttu-id="25fd2-117">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="25fd2-117">Click Designer.</span></span>
9. <span data-ttu-id="25fd2-118">Klikk på Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="25fd2-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="25fd2-119">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="25fd2-120">Skriv inn Rot i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="25fd2-121">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="25fd2-121">Click OK.</span></span>
13. <span data-ttu-id="25fd2-122">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="25fd2-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="25fd2-123">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="25fd2-124">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="25fd2-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="25fd2-125">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="25fd2-125">Click OK.</span></span>
17. <span data-ttu-id="25fd2-126">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="25fd2-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="25fd2-127">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="25fd2-128">I Navn-feltet skriver du inn Journal.</span><span class="sxs-lookup"><span data-stu-id="25fd2-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="25fd2-129">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="25fd2-129">Click OK.</span></span>
21. <span data-ttu-id="25fd2-130">Velg Rot: XML-element\Journal: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="25fd2-131">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="25fd2-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="25fd2-132">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="25fd2-133">Skriv inn Parti i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="25fd2-134">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="25fd2-134">Click OK.</span></span>
26. <span data-ttu-id="25fd2-135">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="25fd2-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="25fd2-136">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="25fd2-137">Skriv inn Transaksjon i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="25fd2-138">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="25fd2-138">Click OK.</span></span>
30. <span data-ttu-id="25fd2-139">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="25fd2-140">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="25fd2-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="25fd2-141">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="25fd2-142">I Navn-feltet skriver du inn Bilag.</span><span class="sxs-lookup"><span data-stu-id="25fd2-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="25fd2-143">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="25fd2-143">Click OK.</span></span>
35. <span data-ttu-id="25fd2-144">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="25fd2-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="25fd2-145">Skriv inn Dato i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="25fd2-146">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="25fd2-146">Click OK.</span></span>
38. <span data-ttu-id="25fd2-147">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="25fd2-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="25fd2-148">I Navn-feltet skriver du inn Valuta.</span><span class="sxs-lookup"><span data-stu-id="25fd2-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="25fd2-149">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="25fd2-149">Click OK.</span></span>
41. <span data-ttu-id="25fd2-150">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="25fd2-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="25fd2-151">Skriv inn Dt i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="25fd2-152">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="25fd2-152">Click OK.</span></span>
44. <span data-ttu-id="25fd2-153">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="25fd2-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="25fd2-154">Skriv inn Kt i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="25fd2-155">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="25fd2-155">Click OK.</span></span>
47. <span data-ttu-id="25fd2-156">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="25fd2-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="25fd2-157">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="25fd2-158">Skriv inn Dimensjoner i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="25fd2-159">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="25fd2-159">Click OK.</span></span>
51. <span data-ttu-id="25fd2-160">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="25fd2-161">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="25fd2-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="25fd2-162">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="25fd2-163">I Navn-feltet skriver du inn Kode.</span><span class="sxs-lookup"><span data-stu-id="25fd2-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="25fd2-164">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="25fd2-164">Click OK.</span></span>
56. <span data-ttu-id="25fd2-165">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="25fd2-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="25fd2-166">Skriv inn Verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="25fd2-167">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="25fd2-167">Click OK.</span></span>
59. <span data-ttu-id="25fd2-168">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="25fd2-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="25fd2-169">Skriv inn Beskr i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="25fd2-170">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="25fd2-170">Click OK.</span></span>
<span data-ttu-id="25fd2-171">![Side med ER-operasjonsutforming](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="25fd2-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="25fd2-172">Tilordne rapportelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="25fd2-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="25fd2-173">Klikk på fanen Tilordning.</span><span class="sxs-lookup"><span data-stu-id="25fd2-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="25fd2-174">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="25fd2-175">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="25fd2-176">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="25fd2-177">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="25fd2-178">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element\Beskr: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="25fd2-179">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Beskrivelse: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="25fd2-180">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="25fd2-180">Click Bind.</span></span>
9. <span data-ttu-id="25fd2-181">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element\Verdi: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="25fd2-182">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Kode: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="25fd2-183">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="25fd2-183">Click Bind.</span></span>
12. <span data-ttu-id="25fd2-184">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element\Kode: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="25fd2-185">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Navn: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="25fd2-186">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="25fd2-186">Click Bind.</span></span>
15. <span data-ttu-id="25fd2-187">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="25fd2-188">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="25fd2-189">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="25fd2-189">Click Bind.</span></span>
18. <span data-ttu-id="25fd2-190">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Kt: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="25fd2-191">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Kredit: Reell i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="25fd2-192">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="25fd2-192">Click Bind.</span></span>
21. <span data-ttu-id="25fd2-193">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dt: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="25fd2-194">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Debet: Reell i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="25fd2-195">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="25fd2-195">Click Bind.</span></span>
24. <span data-ttu-id="25fd2-196">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Valuta: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="25fd2-197">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Valuta: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="25fd2-198">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="25fd2-198">Click Bind.</span></span>
27. <span data-ttu-id="25fd2-199">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dato: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="25fd2-200">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dato: Dato i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="25fd2-201">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="25fd2-201">Click Bind.</span></span>
30. <span data-ttu-id="25fd2-202">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Bilag: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="25fd2-203">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Bilag: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="25fd2-204">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="25fd2-204">Click Bind.</span></span>
33. <span data-ttu-id="25fd2-205">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="25fd2-206">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="25fd2-207">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="25fd2-207">Click Bind.</span></span>
36. <span data-ttu-id="25fd2-208">Velg Rot: XML-element\Journal: XML-element\Parti: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="25fd2-209">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Parti: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="25fd2-210">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="25fd2-210">Click Bind.</span></span>
39. <span data-ttu-id="25fd2-211">Velg Rot: XML-element\Journal: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="25fd2-212">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="25fd2-213">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="25fd2-213">Click Bind.</span></span>
42. <span data-ttu-id="25fd2-214">Velg Rot: XML-element\Firma: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="25fd2-215">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Firma: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="25fd2-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="25fd2-216">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="25fd2-216">Click Bind.</span></span>
45. <span data-ttu-id="25fd2-217">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="25fd2-217">Click Save.</span></span>
46. <span data-ttu-id="25fd2-218">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="25fd2-218">Close the page.</span></span>
<span data-ttu-id="25fd2-219">![Side med ER-operasjonsutforming](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="25fd2-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]