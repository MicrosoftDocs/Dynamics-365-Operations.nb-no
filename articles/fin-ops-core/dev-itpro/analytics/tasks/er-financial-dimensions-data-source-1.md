---
title: ER Bruke finansdimensjoner som en datakilde (del 1 - Utforme datamodell)
description: De følgende trinnene forklarer hvordan en systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca295d651838f34106c9b91a53efc1f4faad4e4a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182491"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1-design-data-model"></a><span data-ttu-id="bd792-103">ER Bruke finansdimensjoner som en datakilde (del 1: Utforme datamodell)</span><span class="sxs-lookup"><span data-stu-id="bd792-103">ER Use financial dimensions as a data source (Part 1: Design data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bd792-104">De følgende trinnene forklarer hvordan en systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="bd792-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="bd792-105">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="bd792-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="bd792-106">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="bd792-106">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="bd792-107">Opprette en ny datamodell</span><span class="sxs-lookup"><span data-stu-id="bd792-107">Create a new data model</span></span>
1. <span data-ttu-id="bd792-108">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="bd792-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="bd792-109">Forsikre deg om at leverandøren Litware, Inc</span><span class="sxs-lookup"><span data-stu-id="bd792-109">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="bd792-110">er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="bd792-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="bd792-111">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="bd792-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="bd792-112">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="bd792-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="bd792-113">Skriv inn Eksempelmodell for finansdimensjoner i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd792-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="bd792-114">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="bd792-114">Click Create configuration.</span></span>
6. <span data-ttu-id="bd792-115">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="bd792-115">Click Designer.</span></span>
7. <span data-ttu-id="bd792-116">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="bd792-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="bd792-117">I Navn-feltet skriver du inn Oppføring.</span><span class="sxs-lookup"><span data-stu-id="bd792-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="bd792-118">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd792-118">Click Add.</span></span>
10. <span data-ttu-id="bd792-119">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="bd792-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="bd792-120">I Navn-feltet skriver du inn Firma.</span><span class="sxs-lookup"><span data-stu-id="bd792-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="bd792-121">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd792-121">Click Add.</span></span>
    * <span data-ttu-id="bd792-122">Vi vil legge til en ny postliste i modellen vår.</span><span class="sxs-lookup"><span data-stu-id="bd792-122">We will add to our model a new record list.</span></span> <span data-ttu-id="bd792-123">Denne listen vil vise (for ER-rapporter som bruker denne modellen som datakilde) innstillingene for valgte finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="bd792-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="bd792-124">Hver finansdimensjon vil bli presentert i denne listen som en post med aktuelle felt som representerer dimensjonens innstilling.</span><span class="sxs-lookup"><span data-stu-id="bd792-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s setting.</span></span>  
13. <span data-ttu-id="bd792-125">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="bd792-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="bd792-126">Skriv inn Dimensjonsinnstilling i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd792-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="bd792-127">Velg Postliste i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd792-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="bd792-128">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd792-128">Click Add.</span></span>
17. <span data-ttu-id="bd792-129">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="bd792-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="bd792-130">I Navn-feltet skriver du inn Kode.</span><span class="sxs-lookup"><span data-stu-id="bd792-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="bd792-131">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd792-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="bd792-132">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd792-132">Click Add.</span></span>
21. <span data-ttu-id="bd792-133">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="bd792-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="bd792-134">I Navn-feltet skriver du inn Navn.</span><span class="sxs-lookup"><span data-stu-id="bd792-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="bd792-135">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd792-135">Click Add.</span></span>
24. <span data-ttu-id="bd792-136">Velg Oppføring i treet.</span><span class="sxs-lookup"><span data-stu-id="bd792-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="bd792-137">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="bd792-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="bd792-138">I Navn-feltet skriver du inn Journal.</span><span class="sxs-lookup"><span data-stu-id="bd792-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="bd792-139">Velg Postliste i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd792-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="bd792-140">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd792-140">Click Add.</span></span>
29. <span data-ttu-id="bd792-141">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="bd792-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="bd792-142">Skriv inn Parti i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd792-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="bd792-143">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd792-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="bd792-144">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd792-144">Click Add.</span></span>
33. <span data-ttu-id="bd792-145">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="bd792-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="bd792-146">Skriv inn Transaksjon i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd792-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="bd792-147">Velg Postliste i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd792-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="bd792-148">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd792-148">Click Add.</span></span>
37. <span data-ttu-id="bd792-149">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="bd792-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="bd792-150">Skriv inn Dato i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd792-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="bd792-151">Velg Dato i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd792-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="bd792-152">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd792-152">Click Add.</span></span>
41. <span data-ttu-id="bd792-153">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="bd792-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="bd792-154">I Navn-feltet skriver du inn Debet.</span><span class="sxs-lookup"><span data-stu-id="bd792-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="bd792-155">Velg Faktisk i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd792-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="bd792-156">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd792-156">Click Add.</span></span>
45. <span data-ttu-id="bd792-157">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="bd792-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="bd792-158">I Navn-feltet skriver du inn Kredit.</span><span class="sxs-lookup"><span data-stu-id="bd792-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="bd792-159">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd792-159">Click Add.</span></span>
48. <span data-ttu-id="bd792-160">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="bd792-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="bd792-161">I Navn-feltet skriver du inn Valuta.</span><span class="sxs-lookup"><span data-stu-id="bd792-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="bd792-162">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd792-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="bd792-163">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd792-163">Click Add.</span></span>
52. <span data-ttu-id="bd792-164">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="bd792-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="bd792-165">I Navn-feltet skriver du inn Bilag.</span><span class="sxs-lookup"><span data-stu-id="bd792-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="bd792-166">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd792-166">Click Add.</span></span>
55. <span data-ttu-id="bd792-167">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="bd792-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="bd792-168">Skriv inn Dimensjonsdata i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd792-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="bd792-169">Velg Postliste i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd792-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="bd792-170">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd792-170">Click Add.</span></span>
    * <span data-ttu-id="bd792-171">Vi la til en ny postliste i modellen vår.</span><span class="sxs-lookup"><span data-stu-id="bd792-171">We added to our model a new record list.</span></span> <span data-ttu-id="bd792-172">Denne listen vil vise (for ER-rapporter som bruker denne modellen som datakilde) verdiene for valgte finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="bd792-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="bd792-173">Hver finansdimensjon vil bli presentert i denne listen som en post med aktuelle felt som representerer dimensjonens verdier.</span><span class="sxs-lookup"><span data-stu-id="bd792-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s values.</span></span> <span data-ttu-id="bd792-174">Dimensjonsnavn blir også presentert i denne posten som et felt som skal brukes, om nødvendig, for utvalgsformål.</span><span class="sxs-lookup"><span data-stu-id="bd792-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="bd792-175">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="bd792-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="bd792-176">I Navn-feltet skriver du inn Kode.</span><span class="sxs-lookup"><span data-stu-id="bd792-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="bd792-177">Velg Streng i Varetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd792-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="bd792-178">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd792-178">Click Add.</span></span>
63. <span data-ttu-id="bd792-179">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="bd792-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="bd792-180">Skriv inn Beskrivelse i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="bd792-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="bd792-181">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd792-181">Click Add.</span></span>
66. <span data-ttu-id="bd792-182">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="bd792-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="bd792-183">I Navn-feltet skriver du inn Navn.</span><span class="sxs-lookup"><span data-stu-id="bd792-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="bd792-184">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bd792-184">Click Add.</span></span>
69. <span data-ttu-id="bd792-185">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="bd792-185">Click Save.</span></span>
70. <span data-ttu-id="bd792-186">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="bd792-186">Close the page.</span></span>

