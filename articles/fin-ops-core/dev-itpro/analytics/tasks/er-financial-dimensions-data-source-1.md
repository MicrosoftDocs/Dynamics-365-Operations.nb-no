---
title: ER Bruke finansdimensjoner som en datakilde (del 1 - Utforme datamodell)
description: Dette emnet beskriver hvordan du konfigurerer en ER-modell (Elektronisk rapportering) for å bruke finansdimensjoner som en datakilde for ER-rapporter. (Del 1)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5ecae444d80698c03ac050b49894daa1b090f74
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570198"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="9addc-104">ER Bruke finansdimensjoner som en datakilde (del 1 - Utforme datamodell)</span><span class="sxs-lookup"><span data-stu-id="9addc-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9addc-105">De følgende trinnene forklarer hvordan en systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="9addc-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="9addc-106">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="9addc-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="9addc-107">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="9addc-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="9addc-108">Opprette en ny datamodell</span><span class="sxs-lookup"><span data-stu-id="9addc-108">Create a new data model</span></span>
1. <span data-ttu-id="9addc-109">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="9addc-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="9addc-110">Forsikre deg om at leverandøren Litware, Inc</span><span class="sxs-lookup"><span data-stu-id="9addc-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="9addc-111">er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="9addc-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="9addc-112">Klikk på Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="9addc-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="9addc-113">Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9addc-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="9addc-114">Skriv inn Eksempelmodell for finansdimensjoner i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9addc-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="9addc-115">Klikk på Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="9addc-115">Click Create configuration.</span></span>
6. <span data-ttu-id="9addc-116">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="9addc-116">Click Designer.</span></span>
7. <span data-ttu-id="9addc-117">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9addc-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="9addc-118">I Navn-feltet skriver du inn Oppføring.</span><span class="sxs-lookup"><span data-stu-id="9addc-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="9addc-119">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="9addc-119">Click Add.</span></span>
10. <span data-ttu-id="9addc-120">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9addc-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="9addc-121">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="9addc-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="9addc-122">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="9addc-122">Click Add.</span></span>
    * <span data-ttu-id="9addc-123">Vi vil legge til en ny postliste i modellen vår.</span><span class="sxs-lookup"><span data-stu-id="9addc-123">We will add to our model a new record list.</span></span> <span data-ttu-id="9addc-124">Denne listen vil vise (for ER-rapporter som bruker denne modellen som datakilde) innstillingene for valgte finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="9addc-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="9addc-125">Hver finansdimensjon vil bli presentert i denne listen som en post med aktuelle felt som representerer dimensjonens innstilling.</span><span class="sxs-lookup"><span data-stu-id="9addc-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="9addc-126">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9addc-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="9addc-127">Skriv inn Dimensjonsinnstilling i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9addc-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="9addc-128">Velg Postliste i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="9addc-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="9addc-129">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="9addc-129">Click Add.</span></span>
17. <span data-ttu-id="9addc-130">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9addc-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="9addc-131">I Navn-feltet skriver du inn Kode.</span><span class="sxs-lookup"><span data-stu-id="9addc-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="9addc-132">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="9addc-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="9addc-133">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="9addc-133">Click Add.</span></span>
21. <span data-ttu-id="9addc-134">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9addc-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="9addc-135">I Navn-feltet skriver du inn Navn.</span><span class="sxs-lookup"><span data-stu-id="9addc-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="9addc-136">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="9addc-136">Click Add.</span></span>
24. <span data-ttu-id="9addc-137">Velg Oppføring i treet.</span><span class="sxs-lookup"><span data-stu-id="9addc-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="9addc-138">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9addc-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="9addc-139">I Navn-feltet skriver du inn Journal.</span><span class="sxs-lookup"><span data-stu-id="9addc-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="9addc-140">Velg Postliste i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="9addc-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="9addc-141">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="9addc-141">Click Add.</span></span>
29. <span data-ttu-id="9addc-142">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9addc-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="9addc-143">Skriv inn Parti i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9addc-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="9addc-144">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="9addc-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="9addc-145">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="9addc-145">Click Add.</span></span>
33. <span data-ttu-id="9addc-146">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9addc-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="9addc-147">Skriv inn Transaksjon i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9addc-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="9addc-148">Velg Postliste i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="9addc-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="9addc-149">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="9addc-149">Click Add.</span></span>
37. <span data-ttu-id="9addc-150">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9addc-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="9addc-151">Skriv inn Dato i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9addc-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="9addc-152">Velg Dato i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="9addc-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="9addc-153">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="9addc-153">Click Add.</span></span>
41. <span data-ttu-id="9addc-154">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9addc-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="9addc-155">I Navn-feltet skriver du inn Debet.</span><span class="sxs-lookup"><span data-stu-id="9addc-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="9addc-156">Velg Faktisk i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="9addc-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="9addc-157">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="9addc-157">Click Add.</span></span>
45. <span data-ttu-id="9addc-158">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9addc-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="9addc-159">I Navn-feltet skriver du inn Kredit.</span><span class="sxs-lookup"><span data-stu-id="9addc-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="9addc-160">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="9addc-160">Click Add.</span></span>
48. <span data-ttu-id="9addc-161">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9addc-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="9addc-162">I Navn-feltet skriver du inn Valuta.</span><span class="sxs-lookup"><span data-stu-id="9addc-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="9addc-163">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="9addc-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="9addc-164">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="9addc-164">Click Add.</span></span>
52. <span data-ttu-id="9addc-165">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9addc-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="9addc-166">I Navn-feltet skriver du inn Bilag.</span><span class="sxs-lookup"><span data-stu-id="9addc-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="9addc-167">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="9addc-167">Click Add.</span></span>
55. <span data-ttu-id="9addc-168">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9addc-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="9addc-169">Skriv inn Dimensjonsdata i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9addc-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="9addc-170">Velg Postliste i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="9addc-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="9addc-171">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="9addc-171">Click Add.</span></span>
    * <span data-ttu-id="9addc-172">Vi la til en ny postliste i modellen vår.</span><span class="sxs-lookup"><span data-stu-id="9addc-172">We added to our model a new record list.</span></span> <span data-ttu-id="9addc-173">Denne listen vil vise (for ER-rapporter som bruker denne modellen som datakilde) verdiene for valgte finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="9addc-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="9addc-174">Hver finansdimensjon vil bli presentert i denne listen som en post med aktuelle felt som representerer dimensjonens verdier.</span><span class="sxs-lookup"><span data-stu-id="9addc-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="9addc-175">Dimensjonsnavn blir også presentert i denne posten som et felt som skal brukes, om nødvendig, for utvalgsformål.</span><span class="sxs-lookup"><span data-stu-id="9addc-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="9addc-176">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9addc-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="9addc-177">I Navn-feltet skriver du inn Kode.</span><span class="sxs-lookup"><span data-stu-id="9addc-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="9addc-178">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="9addc-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="9addc-179">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="9addc-179">Click Add.</span></span>
63. <span data-ttu-id="9addc-180">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9addc-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="9addc-181">Skriv inn Beskrivelse i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9addc-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="9addc-182">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="9addc-182">Click Add.</span></span>
66. <span data-ttu-id="9addc-183">Klikk på Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="9addc-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="9addc-184">I Navn-feltet skriver du inn Navn.</span><span class="sxs-lookup"><span data-stu-id="9addc-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="9addc-185">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="9addc-185">Click Add.</span></span>
69. <span data-ttu-id="9addc-186">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="9addc-186">Click Save.</span></span>
70. <span data-ttu-id="9addc-187">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9addc-187">Close the page.</span></span>

![Siden ER-datamodellutforming](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]