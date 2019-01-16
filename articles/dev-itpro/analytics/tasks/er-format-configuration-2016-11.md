--- 
title: ER Opprette en formatkonfigurasjon (november 2016)
description: "De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en formatkonfigurasjon for elektronisk rapportering (ER)."
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 13469aad7fdcefb3a1706eec0527f29968e007eb
ms.openlocfilehash: 10511fe5b936135471b522fc7152a54686a3be87
ms.contentlocale: nb-no
ms.lasthandoff: 12/18/2018

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="8c3e4-103">ER Opprette en formatkonfigurasjon (november 2016)</span><span class="sxs-lookup"><span data-stu-id="8c3e4-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8c3e4-104">De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en formatkonfigurasjon for elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="8c3e4-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="8c3e4-105">Denne formatkonfigurasjonen definerer formatet for elektroniske dokumenter som skal brukes til behandling av betalinger.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="8c3e4-106">I dette eksemplet oppretter du en formatkonfigurasjon for eksempelfirmaet Litware, Inc. For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren Tilordne modell til valgte datakilder.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="8c3e4-107">Opprette en ny formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="8c3e4-107">Create a new format configuration</span></span>
1. <span data-ttu-id="8c3e4-108">Gå til **Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="8c3e4-109">Klikk på **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="8c3e4-110">Velg **Betalinger (forenklet model)** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="8c3e4-111">Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-111">Click **Create configuration** to open the drop dialog.</span></span>
 > [!NOTE]
 > <span data-ttu-id="8c3e4-112">Hvis du ikke ser **Opprett konfigurasjon**, må du aktivere utformingsmodus på siden **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
5. <span data-ttu-id="8c3e4-113">I **Ny**-feltet angir du **Format basert på datamodell PaymentModel**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="8c3e4-114">Skriv inn **BACS (britisk fiktivt)** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="8c3e4-115">I **Beskrivelse**-feltet skriver du inn **BACS-leverandørbetalingsformat (fiktivt Storbritannia)**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="8c3e4-116">Den aktive konfigurasjonsleverandøren angis automatisk her.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="8c3e4-117">Denne leverandøren vil kunne vedlikeholde denne konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="8c3e4-118">Andre leverandører kan bruke denne konfigurasjonen, men kan ikke vedlikeholde den.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="8c3e4-119">Du kan definere et bestemt format for elektronisk dokument.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="8c3e4-120">La dette feltet stå tomt hvis du vil velge et format under kjøring.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="8c3e4-121">Angi eller velg en verdi i feltet **Definisjon av datamodell**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="8c3e4-122">Klikk **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-122">Click **Create configuration**.</span></span> <span data-ttu-id="8c3e4-123">En ny konfigurasjon er opprettet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-123">A new configuration has been created.</span></span> <span data-ttu-id="8c3e4-124">Utkastversjonen kan brukes til å lagre utformingsformatet for behandling av elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  
 > [!NOTE]
 > <span data-ttu-id="8c3e4-125">Hvis du ikke ser **Opprett konfigurasjon**, må du aktivere utformingsmodus på siden **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-125">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span>


## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="8c3e4-126">Utforme formatet på et elektronisk dokument</span><span class="sxs-lookup"><span data-stu-id="8c3e4-126">Design the format of an electronic document</span></span>
1. <span data-ttu-id="8c3e4-127">Klikk **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-127">Click **Designer**.</span></span>
2. <span data-ttu-id="8c3e4-128">Klikk på **Legg til rot** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-128">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="8c3e4-129">Velg **Felles\Fil** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-129">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="8c3e4-130">I **Navn**-feltet skriver du inn **Xml**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-130">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="8c3e4-131">I **Koding**-feltet skriver du inn **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-131">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="8c3e4-132">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-132">Click **OK**.</span></span>
7. <span data-ttu-id="8c3e4-133">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-133">Click **Add**.</span></span>
8. <span data-ttu-id="8c3e4-134">Velg **XML\Element** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-134">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="8c3e4-135">I **Navn**-feltet skriver du inn **Melding**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-135">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="8c3e4-136">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-136">Click **OK**.</span></span>
11. <span data-ttu-id="8c3e4-137">Velg **Xml\Melding** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-137">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="8c3e4-138">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-138">Click **Add Element**.</span></span>
13. <span data-ttu-id="8c3e4-139">I **Navn**-feltet skriver du inn **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-139">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="8c3e4-140">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-140">Click **OK**.</span></span>
15. <span data-ttu-id="8c3e4-141">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-141">Click **Add Element**.</span></span>
16. <span data-ttu-id="8c3e4-142">I Navn-feltet skriver du inn **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-142">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="8c3e4-143">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-143">Click **OK**.</span></span>
18. <span data-ttu-id="8c3e4-144">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-144">Click **Add Element**.</span></span>
19. <span data-ttu-id="8c3e4-145">Skriv inn **Betalinger** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-145">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="8c3e4-146">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-146">Click **OK**.</span></span>
21. <span data-ttu-id="8c3e4-147">Velg **Xml\Melding\Betalinger** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-147">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="8c3e4-148">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-148">Click **Add Element**.</span></span>
23. <span data-ttu-id="8c3e4-149">I **Navn**-feltet skriver du inn **Vare**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-149">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="8c3e4-150">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-150">Click **OK**.</span></span>
25. <span data-ttu-id="8c3e4-151">Velg **Xml\Melding\Betalinger\Vare** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-151">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="8c3e4-152">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-152">Click **Add**.</span></span>
27. <span data-ttu-id="8c3e4-153">Velg **XML\Attributt** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-153">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="8c3e4-154">I Navn-feltet skriver du inn **ID**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-154">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="8c3e4-155">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-155">Click **OK**.</span></span>
30. <span data-ttu-id="8c3e4-156">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-156">Click **Add**.</span></span>
31. <span data-ttu-id="8c3e4-157">Velg **XML\Element** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-157">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="8c3e4-158">I Navn-feltet skriver du inn **Leverandør**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-158">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="8c3e4-159">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-159">Click **OK**.</span></span>
34. <span data-ttu-id="8c3e4-160">Velg **Xml\Melding\Betalinger\Vare\Leverandør** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-160">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="8c3e4-161">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-161">Click **Add Element**.</span></span>
36. <span data-ttu-id="8c3e4-162">I Navn-feltet skriver du inn **Navn**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-162">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="8c3e4-163">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-163">Click **OK**.</span></span>
38. <span data-ttu-id="8c3e4-164">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-164">Click **Add Element**.</span></span>
39. <span data-ttu-id="8c3e4-165">I **Navn**-feltet skriver du inn **Bank**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-165">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="8c3e4-166">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-166">Click **OK**.</span></span>
41. <span data-ttu-id="8c3e4-167">Velg **Xml\Melding\Betalinger\Vare\Leverandør\Bank** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-167">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="8c3e4-168">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-168">Click **Add Element**.</span></span>
43. <span data-ttu-id="8c3e4-169">Skriv inn **RoutingNumber** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-169">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="8c3e4-170">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-170">Click **OK**.</span></span>
45. <span data-ttu-id="8c3e4-171">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-171">Click **Add Element**.</span></span>
46. <span data-ttu-id="8c3e4-172">Skriv inn **AccountNumber** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-172">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="8c3e4-173">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-173">Click **OK**.</span></span>
48. <span data-ttu-id="8c3e4-174">Velg **Xml\Melding\Betalinger\Vare\Leverandør** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-174">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="8c3e4-175">Klikk **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-175">Click **Copy**.</span></span>
50. <span data-ttu-id="8c3e4-176">Velg **Xml\Melding\Betalinger\Vare** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-176">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="8c3e4-177">Klikk på **Lim inn**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-177">Click **Paste**.</span></span>
52. <span data-ttu-id="8c3e4-178">I **Navn**-feltet skriver du inn **Betaler**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-178">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="8c3e4-179">Velg **Xml\Melding\Betalinger\Vare** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-179">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="8c3e4-180">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-180">Click **Add Element**.</span></span>
55. <span data-ttu-id="8c3e4-181">I **Navn**-feltet skriver du inn **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-181">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="8c3e4-182">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-182">Click **OK**.</span></span>
57. <span data-ttu-id="8c3e4-183">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-183">Click **Add Element**.</span></span>
58. <span data-ttu-id="8c3e4-184">Skriv inn **Beskrivelse** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-184">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="8c3e4-185">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-185">Click **OK**.</span></span>
60. <span data-ttu-id="8c3e4-186">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-186">Click **Add Element**.</span></span>
61. <span data-ttu-id="8c3e4-187">I Navn-feltet skriver du inn **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-187">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="8c3e4-188">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-188">Click **OK**.</span></span>
63. <span data-ttu-id="8c3e4-189">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-189">Click **Add Element**.</span></span>
64. <span data-ttu-id="8c3e4-190">I Navn-feltet skriver du inn **Beløp**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-190">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="8c3e4-191">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-191">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="8c3e4-192">Klargjøre formatkomponenter for tilordning til datamodellelementer</span><span class="sxs-lookup"><span data-stu-id="8c3e4-192">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="8c3e4-193">Velg **Xml\Melding\ProcessingDate** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-193">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="8c3e4-194">Klikk på **Legg til** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-194">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="8c3e4-195">Velg **Tekst\DateTime** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-195">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="8c3e4-196">Skriv inn **åååå-MM-dd** i **Format**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-196">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="8c3e4-197">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-197">Click **OK**.</span></span>
6. <span data-ttu-id="8c3e4-198">Velg **Xml\Melding\Betalinger\Vare\TransDate** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-198">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="8c3e4-199">Klikk på **Legg til dato/klokkeslett**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-199">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="8c3e4-200">Skriv inn **åååå-MM-dd** i **Format**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-200">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="8c3e4-201">Velg **Dato** i feltet **Dato/klokkeslett**-type.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-201">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="8c3e4-202">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-202">Click **OK**.</span></span>
11. <span data-ttu-id="8c3e4-203">Velg **Xml\Melding\MessageId** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-203">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="8c3e4-204">Klikk på **Legg til** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-204">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="8c3e4-205">Velg **Tekst\Streng** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-205">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="8c3e4-206">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-206">Click **OK**.</span></span>
15. <span data-ttu-id="8c3e4-207">Velg **Xml\Melding\Betalinger\Vare\Leverandør\Navn** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-207">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="8c3e4-208">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-208">Click **Add String**.</span></span>
17. <span data-ttu-id="8c3e4-209">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-209">Click **OK**.</span></span>
18. <span data-ttu-id="8c3e4-210">Velg **Xml\Melding\Betalinger\Vare\Leverandør\Bank\RoutingNumber** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-210">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="8c3e4-211">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-211">Click **Add String**.</span></span>
20. <span data-ttu-id="8c3e4-212">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-212">Click **OK**.</span></span>
21. <span data-ttu-id="8c3e4-213">Velg **Xml\Melding\Betalinger\Vare\Leverandør\Bank\AccountNumber** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-213">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="8c3e4-214">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-214">Click **Add String**.</span></span>
23. <span data-ttu-id="8c3e4-215">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-215">Click **OK**.</span></span>
24. <span data-ttu-id="8c3e4-216">Velg **Xml\Melding\Betalinger\Vare\Betaler\Navn** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-216">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="8c3e4-217">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-217">Click **Add String**.</span></span>
26. <span data-ttu-id="8c3e4-218">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-218">Click **OK**.</span></span>
27. <span data-ttu-id="8c3e4-219">Velg **Xml\Melding\Betalinger\Vare\Betaler\Bank\RoutingNumber** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-219">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="8c3e4-220">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-220">Click **Add String**.</span></span>
29. <span data-ttu-id="8c3e4-221">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-221">Click **OK**.</span></span>
30. <span data-ttu-id="8c3e4-222">Velg **Xml\Melding\Betalinger\Vare\Betaler\Bank\AccountNumber** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-222">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="8c3e4-223">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-223">Click **Add String**.</span></span>
32. <span data-ttu-id="8c3e4-224">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-224">Click **OK**.</span></span>
33. <span data-ttu-id="8c3e4-225">Velg **Xml\Melding\Betalinger\Vare\Valuta** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-225">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="8c3e4-226">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-226">Click **Add String**.</span></span>
35. <span data-ttu-id="8c3e4-227">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-227">Click **OK**.</span></span>
36. <span data-ttu-id="8c3e4-228">Velg **Xml\Melding\Betalinger\Vare\Beskrivelse** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-228">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="8c3e4-229">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-229">Click **Add String**.</span></span>
38. <span data-ttu-id="8c3e4-230">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-230">Click **OK**.</span></span>
39. <span data-ttu-id="8c3e4-231">Velg **Xml\Melding\Betalinger\Vare\Beløp** i treet.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-231">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="8c3e4-232">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-232">Click **Add String**.</span></span>
41. <span data-ttu-id="8c3e4-233">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-233">Click **OK**.</span></span>
42. <span data-ttu-id="8c3e4-234">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-234">Click **Save**.</span></span>
43. <span data-ttu-id="8c3e4-235">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8c3e4-235">Close the page.</span></span>


