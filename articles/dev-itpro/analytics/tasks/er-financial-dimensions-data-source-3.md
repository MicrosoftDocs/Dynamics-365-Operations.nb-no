--- 
title: "Utforme en rapport for å bruke finansdimensjoner som en datakilde for elektronisk rapportering (ER)"
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 178deb75bec9ee7c9c355b06850f7f771bac8704
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="design-a-report-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="a7dd3-103">Utforme en rapport for å bruke finansdimensjoner som en datakilde for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="a7dd3-103">Design a report to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a7dd3-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="a7dd3-105">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="a7dd3-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke finansdimensjoner som datakilde (del 2: Modelltilordning).</span><span class="sxs-lookup"><span data-stu-id="a7dd3-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="a7dd3-107">Utforme en rapport for å presentere finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="a7dd3-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="a7dd3-108">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a7dd3-109">Velg Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a7dd3-110">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="a7dd3-111">I feltet Ny angir du Format basert på datamodellen Eksempelmodell for finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="a7dd3-112">Bruk modellen som ble opprettet på forhånd som datakilde for den nye rapporten.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="a7dd3-113">Skriv inn Finansjournalrapport i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="a7dd3-114">Velg Oppføring i Definisjon av datamodell-feltet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="a7dd3-115">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-115">Click Create configuration.</span></span>
8. <span data-ttu-id="a7dd3-116">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-116">Click Designer.</span></span>
9. <span data-ttu-id="a7dd3-117">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="a7dd3-118">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="a7dd3-119">Skriv inn Rot i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="a7dd3-120">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-120">Click OK.</span></span>
13. <span data-ttu-id="a7dd3-121">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="a7dd3-122">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="a7dd3-123">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="a7dd3-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-124">Click OK.</span></span>
17. <span data-ttu-id="a7dd3-125">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="a7dd3-126">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="a7dd3-127">I Navn-feltet skriver du inn Journal.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="a7dd3-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-128">Click OK.</span></span>
21. <span data-ttu-id="a7dd3-129">Velg Rot: XML-element\Journal: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="a7dd3-130">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="a7dd3-131">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="a7dd3-132">Skriv inn Parti i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="a7dd3-133">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-133">Click OK.</span></span>
26. <span data-ttu-id="a7dd3-134">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="a7dd3-135">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="a7dd3-136">Skriv inn Transaksjon i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="a7dd3-137">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-137">Click OK.</span></span>
30. <span data-ttu-id="a7dd3-138">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="a7dd3-139">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="a7dd3-140">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="a7dd3-141">I Navn-feltet skriver du inn Bilag.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="a7dd3-142">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-142">Click OK.</span></span>
35. <span data-ttu-id="a7dd3-143">Klikk Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="a7dd3-144">Skriv inn Dato i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="a7dd3-145">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-145">Click OK.</span></span>
38. <span data-ttu-id="a7dd3-146">Klikk Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="a7dd3-147">I Navn-feltet skriver du inn Valuta.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="a7dd3-148">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-148">Click OK.</span></span>
41. <span data-ttu-id="a7dd3-149">Klikk Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="a7dd3-150">Skriv inn Dt i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="a7dd3-151">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-151">Click OK.</span></span>
44. <span data-ttu-id="a7dd3-152">Klikk Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="a7dd3-153">Skriv inn Kt i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="a7dd3-154">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-154">Click OK.</span></span>
47. <span data-ttu-id="a7dd3-155">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="a7dd3-156">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="a7dd3-157">Skriv inn Dimensjoner i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="a7dd3-158">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-158">Click OK.</span></span>
51. <span data-ttu-id="a7dd3-159">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="a7dd3-160">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="a7dd3-161">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="a7dd3-162">I Navn-feltet skriver du inn Kode.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="a7dd3-163">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-163">Click OK.</span></span>
56. <span data-ttu-id="a7dd3-164">Klikk Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="a7dd3-165">Skriv inn Verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="a7dd3-166">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-166">Click OK.</span></span>
59. <span data-ttu-id="a7dd3-167">Klikk Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="a7dd3-168">Skriv inn Beskr i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="a7dd3-169">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="a7dd3-170">Tilordne rapportelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="a7dd3-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="a7dd3-171">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="a7dd3-172">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a7dd3-173">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="a7dd3-174">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="a7dd3-175">Utvid modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="a7dd3-176">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element\Beskr: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="a7dd3-177">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Beskrivelse: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="a7dd3-178">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-178">Click Bind.</span></span>
9. <span data-ttu-id="a7dd3-179">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element\Verdi: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="a7dd3-180">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Kode: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="a7dd3-181">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-181">Click Bind.</span></span>
12. <span data-ttu-id="a7dd3-182">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element\Kode: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="a7dd3-183">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste\Navn: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="a7dd3-184">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-184">Click Bind.</span></span>
15. <span data-ttu-id="a7dd3-185">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dimensjonsdata: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="a7dd3-186">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dimensjoner: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="a7dd3-187">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-187">Click Bind.</span></span>
18. <span data-ttu-id="a7dd3-188">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Kt: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="a7dd3-189">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Kredit: Reell i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="a7dd3-190">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-190">Click Bind.</span></span>
21. <span data-ttu-id="a7dd3-191">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dt: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="a7dd3-192">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Debet: Reell i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="a7dd3-193">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-193">Click Bind.</span></span>
24. <span data-ttu-id="a7dd3-194">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Valuta: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="a7dd3-195">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Valuta: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="a7dd3-196">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-196">Click Bind.</span></span>
27. <span data-ttu-id="a7dd3-197">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Dato: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="a7dd3-198">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Dato: Dato i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="a7dd3-199">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-199">Click Bind.</span></span>
30. <span data-ttu-id="a7dd3-200">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element\Bilag: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="a7dd3-201">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste\Bilag: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="a7dd3-202">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-202">Click Bind.</span></span>
33. <span data-ttu-id="a7dd3-203">Velg Rot: XML-element\Journal: XML-element\Transaksjon: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="a7dd3-204">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Transaksjon: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="a7dd3-205">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-205">Click Bind.</span></span>
36. <span data-ttu-id="a7dd3-206">Velg Rot: XML-element\Journal: XML-element\Parti: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="a7dd3-207">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste\Parti: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="a7dd3-208">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-208">Click Bind.</span></span>
39. <span data-ttu-id="a7dd3-209">Velg Rot: XML-element\Journal: XML-element i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="a7dd3-210">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Journal: Postliste i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="a7dd3-211">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-211">Click Bind.</span></span>
42. <span data-ttu-id="a7dd3-212">Velg Rot: XML-element\Firma: XML-attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="a7dd3-213">Velg modell: Datamodellen Eksempelmodell for finansdimensjoner\Firma: Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="a7dd3-214">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-214">Click Bind.</span></span>
45. <span data-ttu-id="a7dd3-215">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-215">Click Save.</span></span>
46. <span data-ttu-id="a7dd3-216">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a7dd3-216">Close the page.</span></span>


