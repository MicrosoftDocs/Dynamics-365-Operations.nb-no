---
title: ER Bruke finansdimensjoner som en datakilde (del 3 - Utforme rapporten)
description: Dette emnet beskriver hvordan du konfigurerer en ER-modell (Elektronisk rapportering) for å bruke finansdimensjoner som en datakilde for ER-rapporter. (Del 3)
author: NickSelin
manager: AnnBe
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
ms.openlocfilehash: a9594a12c28109d80c6ee07a9ee38f4923963dca
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565244"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="17e4b-104">ER Bruke finansdimensjoner som en datakilde (del 3 - Utforme rapporten)</span><span class="sxs-lookup"><span data-stu-id="17e4b-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17e4b-105">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="17e4b-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="17e4b-106">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="17e4b-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="17e4b-107">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke finansdimensjoner som datakilde (del 2: Modelltilordning).</span><span class="sxs-lookup"><span data-stu-id="17e4b-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="17e4b-108">Utforme en rapport for å presentere finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="17e4b-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="17e4b-109">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="17e4b-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="17e4b-110">Velg Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="17e4b-111">Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="17e4b-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="17e4b-112">I feltet Ny angir du Format basert på datamodellen Eksempelmodell for finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="17e4b-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="17e4b-113">Bruk modellen som ble opprettet på forhånd som datakilde for den nye rapporten.</span><span class="sxs-lookup"><span data-stu-id="17e4b-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="17e4b-114">Skriv inn Finansjournalrapport i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="17e4b-115">Velg Oppføring i Definisjon av datamodell-feltet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="17e4b-116">Klikk på Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="17e4b-116">Click Create configuration.</span></span>
8. <span data-ttu-id="17e4b-117">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="17e4b-117">Click Designer.</span></span>
9. <span data-ttu-id="17e4b-118">Klikk på Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="17e4b-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="17e4b-119">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="17e4b-120">Skriv inn Rot i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="17e4b-121">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="17e4b-121">Click OK.</span></span>
13. <span data-ttu-id="17e4b-122">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="17e4b-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="17e4b-123">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="17e4b-124">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="17e4b-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="17e4b-125">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="17e4b-125">Click OK.</span></span>
17. <span data-ttu-id="17e4b-126">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="17e4b-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="17e4b-127">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="17e4b-128">I Navn-feltet skriver du inn Journal.</span><span class="sxs-lookup"><span data-stu-id="17e4b-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="17e4b-129">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="17e4b-129">Click OK.</span></span>
21. <span data-ttu-id="17e4b-130">Velg Rot: XML-element\Journal: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="17e4b-131">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="17e4b-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="17e4b-132">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="17e4b-133">Skriv inn Parti i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="17e4b-134">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="17e4b-134">Click OK.</span></span>
26. <span data-ttu-id="17e4b-135">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="17e4b-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="17e4b-136">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="17e4b-137">Skriv inn Transaksjon i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="17e4b-138">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="17e4b-138">Click OK.</span></span>
30. <span data-ttu-id="17e4b-139">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="17e4b-140">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="17e4b-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="17e4b-141">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="17e4b-142">I Navn-feltet skriver du inn Bilag.</span><span class="sxs-lookup"><span data-stu-id="17e4b-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="17e4b-143">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="17e4b-143">Click OK.</span></span>
35. <span data-ttu-id="17e4b-144">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="17e4b-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="17e4b-145">Skriv inn Dato i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="17e4b-146">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="17e4b-146">Click OK.</span></span>
38. <span data-ttu-id="17e4b-147">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="17e4b-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="17e4b-148">I Navn-feltet skriver du inn Valuta.</span><span class="sxs-lookup"><span data-stu-id="17e4b-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="17e4b-149">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="17e4b-149">Click OK.</span></span>
41. <span data-ttu-id="17e4b-150">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="17e4b-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="17e4b-151">Skriv inn Dt i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="17e4b-152">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="17e4b-152">Click OK.</span></span>
44. <span data-ttu-id="17e4b-153">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="17e4b-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="17e4b-154">Skriv inn Kt i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="17e4b-155">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="17e4b-155">Click OK.</span></span>
47. <span data-ttu-id="17e4b-156">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="17e4b-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="17e4b-157">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="17e4b-158">Skriv inn Dimensjoner i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="17e4b-159">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="17e4b-159">Click OK.</span></span>
51. <span data-ttu-id="17e4b-160">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="17e4b-161">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="17e4b-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="17e4b-162">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="17e4b-163">I Navn-feltet skriver du inn Kode.</span><span class="sxs-lookup"><span data-stu-id="17e4b-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="17e4b-164">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="17e4b-164">Click OK.</span></span>
56. <span data-ttu-id="17e4b-165">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="17e4b-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="17e4b-166">Skriv inn Verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="17e4b-167">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="17e4b-167">Click OK.</span></span>
59. <span data-ttu-id="17e4b-168">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="17e4b-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="17e4b-169">Skriv inn Beskr i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="17e4b-170">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="17e4b-170">Click OK.</span></span>
<span data-ttu-id="17e4b-171">![Side med ER-operasjonsutforming](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="17e4b-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="17e4b-172">Tilordne rapportelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="17e4b-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="17e4b-173">Klikk på fanen Tilordning.</span><span class="sxs-lookup"><span data-stu-id="17e4b-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="17e4b-174">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="17e4b-175">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="17e4b-176">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="17e4b-177">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="17e4b-178">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element\Beskr: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="17e4b-179">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Beskrivelse: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="17e4b-180">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="17e4b-180">Click Bind.</span></span>
9. <span data-ttu-id="17e4b-181">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element\Verdi: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="17e4b-182">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Kode: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="17e4b-183">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="17e4b-183">Click Bind.</span></span>
12. <span data-ttu-id="17e4b-184">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element\Kode: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="17e4b-185">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Navn: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="17e4b-186">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="17e4b-186">Click Bind.</span></span>
15. <span data-ttu-id="17e4b-187">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="17e4b-188">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="17e4b-189">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="17e4b-189">Click Bind.</span></span>
18. <span data-ttu-id="17e4b-190">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Kt: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="17e4b-191">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Kredit: Reell i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="17e4b-192">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="17e4b-192">Click Bind.</span></span>
21. <span data-ttu-id="17e4b-193">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dt: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="17e4b-194">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Debet: Reell i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="17e4b-195">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="17e4b-195">Click Bind.</span></span>
24. <span data-ttu-id="17e4b-196">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Valuta: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="17e4b-197">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Valuta: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="17e4b-198">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="17e4b-198">Click Bind.</span></span>
27. <span data-ttu-id="17e4b-199">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dato: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="17e4b-200">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dato: Dato i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="17e4b-201">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="17e4b-201">Click Bind.</span></span>
30. <span data-ttu-id="17e4b-202">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Bilag: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="17e4b-203">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Bilag: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="17e4b-204">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="17e4b-204">Click Bind.</span></span>
33. <span data-ttu-id="17e4b-205">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="17e4b-206">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="17e4b-207">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="17e4b-207">Click Bind.</span></span>
36. <span data-ttu-id="17e4b-208">Velg Rot: XML-element\Journal: XML-element\Parti: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="17e4b-209">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Parti: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="17e4b-210">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="17e4b-210">Click Bind.</span></span>
39. <span data-ttu-id="17e4b-211">Velg Rot: XML-element\Journal: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="17e4b-212">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="17e4b-213">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="17e4b-213">Click Bind.</span></span>
42. <span data-ttu-id="17e4b-214">Velg Rot: XML-element\Firma: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="17e4b-215">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Firma: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="17e4b-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="17e4b-216">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="17e4b-216">Click Bind.</span></span>
45. <span data-ttu-id="17e4b-217">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="17e4b-217">Click Save.</span></span>
46. <span data-ttu-id="17e4b-218">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="17e4b-218">Close the page.</span></span>
<span data-ttu-id="17e4b-219">![Side med ER-operasjonsutforming](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="17e4b-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]