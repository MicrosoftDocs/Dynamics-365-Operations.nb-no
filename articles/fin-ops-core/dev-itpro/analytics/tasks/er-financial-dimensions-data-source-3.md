---
title: ER Bruke finansdimensjoner som en datakilde (del 3 - Utforme rapporten)
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cef61787e50561eaac4fd52741ab5f90d9c4171d
ms.sourcegitcommit: d9125c20b21459076e4fd92fd9ebfe2e53a0431b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406503"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="11700-103">ER Bruke finansdimensjoner som en datakilde (del 3 - Utforme rapporten)</span><span class="sxs-lookup"><span data-stu-id="11700-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11700-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="11700-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="11700-105">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="11700-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="11700-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke finansdimensjoner som datakilde (del 2: Modelltilordning).</span><span class="sxs-lookup"><span data-stu-id="11700-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="11700-107">Utforme en rapport for å presentere finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="11700-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="11700-108">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="11700-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="11700-109">Velg Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="11700-110">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="11700-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="11700-111">I feltet Ny angir du Format basert på datamodellen Eksempelmodell for finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="11700-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="11700-112">Bruk modellen som ble opprettet på forhånd som datakilde for den nye rapporten.</span><span class="sxs-lookup"><span data-stu-id="11700-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="11700-113">Skriv inn Finansjournalrapport i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="11700-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="11700-114">Velg Oppføring i Definisjon av datamodell-feltet.</span><span class="sxs-lookup"><span data-stu-id="11700-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="11700-115">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="11700-115">Click Create configuration.</span></span>
8. <span data-ttu-id="11700-116">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="11700-116">Click Designer.</span></span>
9. <span data-ttu-id="11700-117">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="11700-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="11700-118">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="11700-119">Skriv inn Rot i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="11700-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="11700-120">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="11700-120">Click OK.</span></span>
13. <span data-ttu-id="11700-121">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="11700-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="11700-122">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="11700-123">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="11700-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="11700-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="11700-124">Click OK.</span></span>
17. <span data-ttu-id="11700-125">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="11700-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="11700-126">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="11700-127">I Navn-feltet skriver du inn Journal.</span><span class="sxs-lookup"><span data-stu-id="11700-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="11700-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="11700-128">Click OK.</span></span>
21. <span data-ttu-id="11700-129">Velg Rot: XML-element\Journal: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="11700-130">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="11700-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="11700-131">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="11700-132">Skriv inn Parti i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="11700-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="11700-133">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="11700-133">Click OK.</span></span>
26. <span data-ttu-id="11700-134">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="11700-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="11700-135">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="11700-136">Skriv inn Transaksjon i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="11700-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="11700-137">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="11700-137">Click OK.</span></span>
30. <span data-ttu-id="11700-138">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="11700-139">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="11700-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="11700-140">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="11700-141">I Navn-feltet skriver du inn Bilag.</span><span class="sxs-lookup"><span data-stu-id="11700-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="11700-142">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="11700-142">Click OK.</span></span>
35. <span data-ttu-id="11700-143">Klikk Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="11700-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="11700-144">Skriv inn Dato i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="11700-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="11700-145">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="11700-145">Click OK.</span></span>
38. <span data-ttu-id="11700-146">Klikk Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="11700-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="11700-147">I Navn-feltet skriver du inn Valuta.</span><span class="sxs-lookup"><span data-stu-id="11700-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="11700-148">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="11700-148">Click OK.</span></span>
41. <span data-ttu-id="11700-149">Klikk Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="11700-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="11700-150">Skriv inn Dt i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="11700-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="11700-151">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="11700-151">Click OK.</span></span>
44. <span data-ttu-id="11700-152">Klikk Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="11700-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="11700-153">Skriv inn Kt i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="11700-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="11700-154">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="11700-154">Click OK.</span></span>
47. <span data-ttu-id="11700-155">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="11700-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="11700-156">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="11700-157">Skriv inn Dimensjoner i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="11700-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="11700-158">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="11700-158">Click OK.</span></span>
51. <span data-ttu-id="11700-159">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="11700-160">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="11700-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="11700-161">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="11700-162">I Navn-feltet skriver du inn Kode.</span><span class="sxs-lookup"><span data-stu-id="11700-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="11700-163">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="11700-163">Click OK.</span></span>
56. <span data-ttu-id="11700-164">Klikk Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="11700-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="11700-165">Skriv inn Verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="11700-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="11700-166">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="11700-166">Click OK.</span></span>
59. <span data-ttu-id="11700-167">Klikk Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="11700-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="11700-168">Skriv inn Beskr i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="11700-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="11700-169">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="11700-169">Click OK.</span></span>
<span data-ttu-id="11700-170">![Side med ER-operasjonsutforming](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="11700-170">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="11700-171">Tilordne rapportelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="11700-171">Map report elements to data sources</span></span>
1. <span data-ttu-id="11700-172">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="11700-172">Click the Mapping tab.</span></span>
2. <span data-ttu-id="11700-173">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-173">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="11700-174">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="11700-175">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="11700-176">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="11700-177">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element\Beskr: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-177">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="11700-178">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Beskrivelse: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="11700-179">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="11700-179">Click Bind.</span></span>
9. <span data-ttu-id="11700-180">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element\Verdi: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-180">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="11700-181">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Kode: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="11700-182">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="11700-182">Click Bind.</span></span>
12. <span data-ttu-id="11700-183">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element\Kode: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-183">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="11700-184">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Navn: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="11700-185">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="11700-185">Click Bind.</span></span>
15. <span data-ttu-id="11700-186">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-186">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="11700-187">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-187">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="11700-188">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="11700-188">Click Bind.</span></span>
18. <span data-ttu-id="11700-189">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Kt: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-189">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="11700-190">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Kredit: Reell i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="11700-191">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="11700-191">Click Bind.</span></span>
21. <span data-ttu-id="11700-192">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dt: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-192">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="11700-193">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Debet: Reell i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="11700-194">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="11700-194">Click Bind.</span></span>
24. <span data-ttu-id="11700-195">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Valuta: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-195">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="11700-196">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Valuta: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="11700-197">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="11700-197">Click Bind.</span></span>
27. <span data-ttu-id="11700-198">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dato: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-198">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="11700-199">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dato: Dato i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="11700-200">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="11700-200">Click Bind.</span></span>
30. <span data-ttu-id="11700-201">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Bilag: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-201">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="11700-202">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Bilag: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="11700-203">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="11700-203">Click Bind.</span></span>
33. <span data-ttu-id="11700-204">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-204">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="11700-205">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="11700-206">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="11700-206">Click Bind.</span></span>
36. <span data-ttu-id="11700-207">Velg Rot: XML-element\Journal: XML-element\Parti: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-207">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="11700-208">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Parti: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-208">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="11700-209">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="11700-209">Click Bind.</span></span>
39. <span data-ttu-id="11700-210">Velg Rot: XML-element\Journal: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-210">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="11700-211">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-211">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="11700-212">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="11700-212">Click Bind.</span></span>
42. <span data-ttu-id="11700-213">Velg Rot: XML-element\Firma: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-213">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="11700-214">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Firma: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="11700-214">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="11700-215">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="11700-215">Click Bind.</span></span>
45. <span data-ttu-id="11700-216">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="11700-216">Click Save.</span></span>
46. <span data-ttu-id="11700-217">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="11700-217">Close the page.</span></span>
<span data-ttu-id="11700-218">![Side med ER-operasjonsutforming](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="11700-218">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

