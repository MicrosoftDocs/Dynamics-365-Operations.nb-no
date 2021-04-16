---
title: ER Opprette en formatkonfigurasjon (november 2016)
description: Dette emnet forklarer hvordan du oppretter en formatkonfigurasjon for elektronisk rapportering (ER).
author: NickSelin
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46686b9e4f6197f565a324a9d03cbb695b6a933b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749075"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="e540f-103">ER Opprette en formatkonfigurasjon (november 2016)</span><span class="sxs-lookup"><span data-stu-id="e540f-103">ER Create a format configuration (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e540f-104">Dette emnet beskriver hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en formatkonfigurasjon for elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="e540f-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="e540f-105">Denne formatkonfigurasjonen definerer formatet for elektroniske dokumenter som skal brukes til behandling av betalinger.</span><span class="sxs-lookup"><span data-stu-id="e540f-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="e540f-106">I dette eksemplet oppretter du en formatkonfigurasjon for eksempelfirmaet Litware, Inc. For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren Tilordne modell til valgte datakilder.</span><span class="sxs-lookup"><span data-stu-id="e540f-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Map model to selected datasources" procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="e540f-107">Opprette en ny formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="e540f-107">Create a new format configuration</span></span>
1. <span data-ttu-id="e540f-108">Gå til **Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="e540f-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="e540f-109">Klikk på **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="e540f-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="e540f-110">Velg **Betalinger (forenklet model)** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="e540f-111">Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="e540f-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="e540f-112">Hvis du ikke ser **Opprett konfigurasjon**, må du aktivere utformingsmodus på siden **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="e540f-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="e540f-113">I **Ny**-feltet angir du **Format basert på datamodell PaymentModel**.</span><span class="sxs-lookup"><span data-stu-id="e540f-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="e540f-114">Skriv inn **BACS (britisk fiktivt)** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e540f-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="e540f-115">I **Beskrivelse**-feltet skriver du inn **BACS-leverandørbetalingsformat (fiktivt Storbritannia)**.</span><span class="sxs-lookup"><span data-stu-id="e540f-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="e540f-116">Den aktive konfigurasjonsleverandøren angis automatisk her.</span><span class="sxs-lookup"><span data-stu-id="e540f-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="e540f-117">Denne leverandøren vil kunne vedlikeholde denne konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="e540f-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="e540f-118">Andre leverandører kan bruke denne konfigurasjonen, men kan ikke vedlikeholde den.</span><span class="sxs-lookup"><span data-stu-id="e540f-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="e540f-119">Du kan definere et bestemt format for elektronisk dokument.</span><span class="sxs-lookup"><span data-stu-id="e540f-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="e540f-120">La dette feltet stå tomt hvis du vil velge et format under kjøring.</span><span class="sxs-lookup"><span data-stu-id="e540f-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="e540f-121">Angi eller velg en verdi i feltet **Definisjon av datamodell**.</span><span class="sxs-lookup"><span data-stu-id="e540f-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="e540f-122">Klikk på **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="e540f-122">Click **Create configuration**.</span></span> <span data-ttu-id="e540f-123">En ny konfigurasjon er opprettet.</span><span class="sxs-lookup"><span data-stu-id="e540f-123">A new configuration has been created.</span></span> <span data-ttu-id="e540f-124">Utkastversjonen kan brukes til å lagre utformingsformatet for behandling av elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="e540f-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="e540f-125">Utforme formatet på et elektronisk dokument</span><span class="sxs-lookup"><span data-stu-id="e540f-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="e540f-126">Klikk på **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="e540f-126">Click **Designer**.</span></span>
2. <span data-ttu-id="e540f-127">Klikk på **Legg til rot** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="e540f-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="e540f-128">Velg **Felles\Fil** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="e540f-129">I **Navn**-feltet skriver du inn **Xml**.</span><span class="sxs-lookup"><span data-stu-id="e540f-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="e540f-130">I **Koding**-feltet skriver du inn **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="e540f-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="e540f-131">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-131">Click **OK**.</span></span>
7. <span data-ttu-id="e540f-132">Klikk på **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="e540f-132">Click **Add**.</span></span>
8. <span data-ttu-id="e540f-133">Velg **XML\Element** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="e540f-134">I **Navn**-feltet skriver du inn **Melding**.</span><span class="sxs-lookup"><span data-stu-id="e540f-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="e540f-135">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-135">Click **OK**.</span></span>
11. <span data-ttu-id="e540f-136">Velg **Xml\Melding** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="e540f-137">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="e540f-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="e540f-138">I **Navn**-feltet skriver du inn **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="e540f-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="e540f-139">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-139">Click **OK**.</span></span>
15. <span data-ttu-id="e540f-140">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="e540f-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="e540f-141">I Navn-feltet skriver du inn **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="e540f-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="e540f-142">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-142">Click **OK**.</span></span>
18. <span data-ttu-id="e540f-143">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="e540f-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="e540f-144">Skriv inn **Betalinger** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e540f-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="e540f-145">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-145">Click **OK**.</span></span>
21. <span data-ttu-id="e540f-146">Velg **Xml\Melding\Betalinger** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="e540f-147">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="e540f-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="e540f-148">I **Navn**-feltet skriver du inn **Vare**.</span><span class="sxs-lookup"><span data-stu-id="e540f-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="e540f-149">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-149">Click **OK**.</span></span>
25. <span data-ttu-id="e540f-150">Velg **Xml\Melding\Betalinger\Vare** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="e540f-151">Klikk på **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="e540f-151">Click **Add**.</span></span>
27. <span data-ttu-id="e540f-152">Velg **XML\Attributt** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="e540f-153">I Navn-feltet skriver du inn **ID**.</span><span class="sxs-lookup"><span data-stu-id="e540f-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="e540f-154">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-154">Click **OK**.</span></span>
30. <span data-ttu-id="e540f-155">Klikk på **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="e540f-155">Click **Add**.</span></span>
31. <span data-ttu-id="e540f-156">Velg **XML\Element** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="e540f-157">I Navn-feltet skriver du inn **Leverandør**.</span><span class="sxs-lookup"><span data-stu-id="e540f-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="e540f-158">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-158">Click **OK**.</span></span>
34. <span data-ttu-id="e540f-159">Velg **Xml\Melding\Betalinger\Vare\Leverandør** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="e540f-160">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="e540f-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="e540f-161">I Navn-feltet skriver du inn **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e540f-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="e540f-162">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-162">Click **OK**.</span></span>
38. <span data-ttu-id="e540f-163">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="e540f-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="e540f-164">I **Navn**-feltet skriver du inn **Bank**.</span><span class="sxs-lookup"><span data-stu-id="e540f-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="e540f-165">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-165">Click **OK**.</span></span>
41. <span data-ttu-id="e540f-166">Velg **Xml\Melding\Betalinger\Vare\Leverandør\Bank** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="e540f-167">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="e540f-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="e540f-168">Skriv inn **RoutingNumber** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e540f-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="e540f-169">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-169">Click **OK**.</span></span>
45. <span data-ttu-id="e540f-170">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="e540f-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="e540f-171">Skriv inn **AccountNumber** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e540f-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="e540f-172">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-172">Click **OK**.</span></span>
48. <span data-ttu-id="e540f-173">Velg **Xml\Melding\Betalinger\Vare\Leverandør** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="e540f-174">Klikk på **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="e540f-174">Click **Copy**.</span></span>
50. <span data-ttu-id="e540f-175">Velg **Xml\Melding\Betalinger\Vare** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="e540f-176">Klikk på **Lim inn**.</span><span class="sxs-lookup"><span data-stu-id="e540f-176">Click **Paste**.</span></span>
52. <span data-ttu-id="e540f-177">I **Navn**-feltet skriver du inn **Betaler**.</span><span class="sxs-lookup"><span data-stu-id="e540f-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="e540f-178">Velg **Xml\Melding\Betalinger\Vare** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="e540f-179">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="e540f-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="e540f-180">I **Navn**-feltet skriver du inn **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="e540f-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="e540f-181">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-181">Click **OK**.</span></span>
57. <span data-ttu-id="e540f-182">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="e540f-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="e540f-183">Skriv inn **Beskrivelse** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e540f-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="e540f-184">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-184">Click **OK**.</span></span>
60. <span data-ttu-id="e540f-185">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="e540f-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="e540f-186">I Navn-feltet skriver du inn **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="e540f-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="e540f-187">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-187">Click **OK**.</span></span>
63. <span data-ttu-id="e540f-188">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="e540f-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="e540f-189">I Navn-feltet skriver du inn **Beløp**.</span><span class="sxs-lookup"><span data-stu-id="e540f-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="e540f-190">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="e540f-191">Klargjøre formatkomponenter for tilordning til datamodellelementer</span><span class="sxs-lookup"><span data-stu-id="e540f-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="e540f-192">Velg **Xml\Melding\ProcessingDate** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="e540f-193">Klikk på **Legg til** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="e540f-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="e540f-194">Velg **Tekst\DateTime** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="e540f-195">Skriv inn **åååå-MM-dd** i **Format**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e540f-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="e540f-196">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-196">Click **OK**.</span></span>
6. <span data-ttu-id="e540f-197">Velg **Xml\Melding\Betalinger\Vare\TransDate** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="e540f-198">Klikk på **Legg til dato/klokkeslett**.</span><span class="sxs-lookup"><span data-stu-id="e540f-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="e540f-199">Skriv inn **åååå-MM-dd** i **Format**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e540f-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="e540f-200">Velg **Dato** i feltet **Dato/klokkeslett**-type.</span><span class="sxs-lookup"><span data-stu-id="e540f-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="e540f-201">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-201">Click **OK**.</span></span>
11. <span data-ttu-id="e540f-202">Velg **Xml\Melding\MessageId** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="e540f-203">Klikk på **Legg til** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="e540f-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="e540f-204">Velg **Tekst\Streng** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="e540f-205">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-205">Click **OK**.</span></span>
15. <span data-ttu-id="e540f-206">Velg **Xml\Melding\Betalinger\Vare\Leverandør\Navn** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="e540f-207">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="e540f-207">Click **Add String**.</span></span>
17. <span data-ttu-id="e540f-208">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-208">Click **OK**.</span></span>
18. <span data-ttu-id="e540f-209">Velg **Xml\Melding\Betalinger\Vare\Leverandør\Bank\RoutingNumber** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="e540f-210">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="e540f-210">Click **Add String**.</span></span>
20. <span data-ttu-id="e540f-211">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-211">Click **OK**.</span></span>
21. <span data-ttu-id="e540f-212">Velg **Xml\Melding\Betalinger\Vare\Leverandør\Bank\AccountNumber** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="e540f-213">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="e540f-213">Click **Add String**.</span></span>
23. <span data-ttu-id="e540f-214">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-214">Click **OK**.</span></span>
24. <span data-ttu-id="e540f-215">Velg **Xml\Melding\Betalinger\Vare\Betaler\Navn** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="e540f-216">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="e540f-216">Click **Add String**.</span></span>
26. <span data-ttu-id="e540f-217">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-217">Click **OK**.</span></span>
27. <span data-ttu-id="e540f-218">Velg **Xml\Melding\Betalinger\Vare\Betaler\Bank\RoutingNumber** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="e540f-219">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="e540f-219">Click **Add String**.</span></span>
29. <span data-ttu-id="e540f-220">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-220">Click **OK**.</span></span>
30. <span data-ttu-id="e540f-221">Velg **Xml\Melding\Betalinger\Vare\Betaler\Bank\AccountNumber** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="e540f-222">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="e540f-222">Click **Add String**.</span></span>
32. <span data-ttu-id="e540f-223">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-223">Click **OK**.</span></span>
33. <span data-ttu-id="e540f-224">Velg **Xml\Melding\Betalinger\Vare\Valuta** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="e540f-225">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="e540f-225">Click **Add String**.</span></span>
35. <span data-ttu-id="e540f-226">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-226">Click **OK**.</span></span>
36. <span data-ttu-id="e540f-227">Velg **Xml\Melding\Betalinger\Vare\Beskrivelse** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="e540f-228">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="e540f-228">Click **Add String**.</span></span>
38. <span data-ttu-id="e540f-229">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-229">Click **OK**.</span></span>
39. <span data-ttu-id="e540f-230">Velg **Xml\Melding\Betalinger\Vare\Beløp** i treet.</span><span class="sxs-lookup"><span data-stu-id="e540f-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="e540f-231">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="e540f-231">Click **Add String**.</span></span>
41. <span data-ttu-id="e540f-232">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e540f-232">Click **OK**.</span></span>
42. <span data-ttu-id="e540f-233">Klikk på **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e540f-233">Click **Save**.</span></span>
43. <span data-ttu-id="e540f-234">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e540f-234">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]