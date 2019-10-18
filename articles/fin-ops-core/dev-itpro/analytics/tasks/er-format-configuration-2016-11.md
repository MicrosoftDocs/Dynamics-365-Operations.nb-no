---
title: ER Opprette en formatkonfigurasjon (november 2016)
description: Dette emnet beskriver hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en formatkonfigurasjon for elektronisk rapportering (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1fd41b1724eb2e0405c0e7a7e0ff0aea4a945e0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184951"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="067e3-103">ER Opprette en formatkonfigurasjon (november 2016)</span><span class="sxs-lookup"><span data-stu-id="067e3-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="067e3-104">Dette emnet beskriver hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en formatkonfigurasjon for elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="067e3-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="067e3-105">Denne formatkonfigurasjonen definerer formatet for elektroniske dokumenter som skal brukes til behandling av betalinger.</span><span class="sxs-lookup"><span data-stu-id="067e3-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="067e3-106">I dette eksemplet oppretter du en formatkonfigurasjon for eksempelfirmaet Litware, Inc. For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren Tilordne modell til valgte datakilder.</span><span class="sxs-lookup"><span data-stu-id="067e3-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="067e3-107">Opprette en ny formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="067e3-107">Create a new format configuration</span></span>
1. <span data-ttu-id="067e3-108">Gå til **Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="067e3-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="067e3-109">Klikk på **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="067e3-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="067e3-110">Velg **Betalinger (forenklet model)** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="067e3-111">Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="067e3-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="067e3-112">Hvis du ikke ser **Opprett konfigurasjon**, må du aktivere utformingsmodus på siden **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="067e3-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="067e3-113">I **Ny**-feltet angir du **Format basert på datamodell PaymentModel**.</span><span class="sxs-lookup"><span data-stu-id="067e3-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="067e3-114">Skriv inn **BACS (britisk fiktivt)** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="067e3-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="067e3-115">I **Beskrivelse**-feltet skriver du inn **BACS-leverandørbetalingsformat (fiktivt Storbritannia)**.</span><span class="sxs-lookup"><span data-stu-id="067e3-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="067e3-116">Den aktive konfigurasjonsleverandøren angis automatisk her.</span><span class="sxs-lookup"><span data-stu-id="067e3-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="067e3-117">Denne leverandøren vil kunne vedlikeholde denne konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="067e3-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="067e3-118">Andre leverandører kan bruke denne konfigurasjonen, men kan ikke vedlikeholde den.</span><span class="sxs-lookup"><span data-stu-id="067e3-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="067e3-119">Du kan definere et bestemt format for elektronisk dokument.</span><span class="sxs-lookup"><span data-stu-id="067e3-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="067e3-120">La dette feltet stå tomt hvis du vil velge et format under kjøring.</span><span class="sxs-lookup"><span data-stu-id="067e3-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="067e3-121">Angi eller velg en verdi i feltet **Definisjon av datamodell**.</span><span class="sxs-lookup"><span data-stu-id="067e3-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="067e3-122">Klikk **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="067e3-122">Click **Create configuration**.</span></span> <span data-ttu-id="067e3-123">En ny konfigurasjon er opprettet.</span><span class="sxs-lookup"><span data-stu-id="067e3-123">A new configuration has been created.</span></span> <span data-ttu-id="067e3-124">Utkastversjonen kan brukes til å lagre utformingsformatet for behandling av elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="067e3-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="067e3-125">Utforme formatet på et elektronisk dokument</span><span class="sxs-lookup"><span data-stu-id="067e3-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="067e3-126">Klikk **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="067e3-126">Click **Designer**.</span></span>
2. <span data-ttu-id="067e3-127">Klikk på **Legg til rot** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="067e3-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="067e3-128">Velg **Felles\Fil** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="067e3-129">I **Navn**-feltet skriver du inn **Xml**.</span><span class="sxs-lookup"><span data-stu-id="067e3-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="067e3-130">I **Koding**-feltet skriver du inn **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="067e3-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="067e3-131">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-131">Click **OK**.</span></span>
7. <span data-ttu-id="067e3-132">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="067e3-132">Click **Add**.</span></span>
8. <span data-ttu-id="067e3-133">Velg **XML\Element** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="067e3-134">I **Navn**-feltet skriver du inn **Melding**.</span><span class="sxs-lookup"><span data-stu-id="067e3-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="067e3-135">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-135">Click **OK**.</span></span>
11. <span data-ttu-id="067e3-136">Velg **Xml\Melding** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="067e3-137">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="067e3-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="067e3-138">I **Navn**-feltet skriver du inn **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="067e3-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="067e3-139">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-139">Click **OK**.</span></span>
15. <span data-ttu-id="067e3-140">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="067e3-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="067e3-141">I Navn-feltet skriver du inn **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="067e3-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="067e3-142">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-142">Click **OK**.</span></span>
18. <span data-ttu-id="067e3-143">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="067e3-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="067e3-144">Skriv inn **Betalinger** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="067e3-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="067e3-145">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-145">Click **OK**.</span></span>
21. <span data-ttu-id="067e3-146">Velg **Xml\Melding\Betalinger** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="067e3-147">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="067e3-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="067e3-148">I **Navn**-feltet skriver du inn **Vare**.</span><span class="sxs-lookup"><span data-stu-id="067e3-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="067e3-149">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-149">Click **OK**.</span></span>
25. <span data-ttu-id="067e3-150">Velg **Xml\Melding\Betalinger\Vare** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="067e3-151">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="067e3-151">Click **Add**.</span></span>
27. <span data-ttu-id="067e3-152">Velg **XML\Attributt** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="067e3-153">I Navn-feltet skriver du inn **ID**.</span><span class="sxs-lookup"><span data-stu-id="067e3-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="067e3-154">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-154">Click **OK**.</span></span>
30. <span data-ttu-id="067e3-155">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="067e3-155">Click **Add**.</span></span>
31. <span data-ttu-id="067e3-156">Velg **XML\Element** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="067e3-157">I Navn-feltet skriver du inn **Leverandør**.</span><span class="sxs-lookup"><span data-stu-id="067e3-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="067e3-158">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-158">Click **OK**.</span></span>
34. <span data-ttu-id="067e3-159">Velg **Xml\Melding\Betalinger\Vare\Leverandør** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="067e3-160">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="067e3-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="067e3-161">I Navn-feltet skriver du inn **Navn**.</span><span class="sxs-lookup"><span data-stu-id="067e3-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="067e3-162">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-162">Click **OK**.</span></span>
38. <span data-ttu-id="067e3-163">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="067e3-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="067e3-164">I **Navn**-feltet skriver du inn **Bank**.</span><span class="sxs-lookup"><span data-stu-id="067e3-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="067e3-165">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-165">Click **OK**.</span></span>
41. <span data-ttu-id="067e3-166">Velg **Xml\Melding\Betalinger\Vare\Leverandør\Bank** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="067e3-167">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="067e3-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="067e3-168">Skriv inn **RoutingNumber** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="067e3-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="067e3-169">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-169">Click **OK**.</span></span>
45. <span data-ttu-id="067e3-170">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="067e3-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="067e3-171">Skriv inn **AccountNumber** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="067e3-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="067e3-172">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-172">Click **OK**.</span></span>
48. <span data-ttu-id="067e3-173">Velg **Xml\Melding\Betalinger\Vare\Leverandør** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="067e3-174">Klikk **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="067e3-174">Click **Copy**.</span></span>
50. <span data-ttu-id="067e3-175">Velg **Xml\Melding\Betalinger\Vare** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="067e3-176">Klikk på **Lim inn**.</span><span class="sxs-lookup"><span data-stu-id="067e3-176">Click **Paste**.</span></span>
52. <span data-ttu-id="067e3-177">I **Navn**-feltet skriver du inn **Betaler**.</span><span class="sxs-lookup"><span data-stu-id="067e3-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="067e3-178">Velg **Xml\Melding\Betalinger\Vare** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="067e3-179">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="067e3-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="067e3-180">I **Navn**-feltet skriver du inn **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="067e3-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="067e3-181">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-181">Click **OK**.</span></span>
57. <span data-ttu-id="067e3-182">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="067e3-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="067e3-183">Skriv inn **Beskrivelse** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="067e3-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="067e3-184">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-184">Click **OK**.</span></span>
60. <span data-ttu-id="067e3-185">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="067e3-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="067e3-186">I Navn-feltet skriver du inn **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="067e3-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="067e3-187">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-187">Click **OK**.</span></span>
63. <span data-ttu-id="067e3-188">Klikk på **Legg til element**.</span><span class="sxs-lookup"><span data-stu-id="067e3-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="067e3-189">I Navn-feltet skriver du inn **Beløp**.</span><span class="sxs-lookup"><span data-stu-id="067e3-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="067e3-190">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="067e3-191">Klargjøre formatkomponenter for tilordning til datamodellelementer</span><span class="sxs-lookup"><span data-stu-id="067e3-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="067e3-192">Velg **Xml\Melding\ProcessingDate** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="067e3-193">Klikk på **Legg til** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="067e3-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="067e3-194">Velg **Tekst\DateTime** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="067e3-195">Skriv inn **åååå-MM-dd** i **Format**-feltet.</span><span class="sxs-lookup"><span data-stu-id="067e3-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="067e3-196">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-196">Click **OK**.</span></span>
6. <span data-ttu-id="067e3-197">Velg **Xml\Melding\Betalinger\Vare\TransDate** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="067e3-198">Klikk på **Legg til dato/klokkeslett**.</span><span class="sxs-lookup"><span data-stu-id="067e3-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="067e3-199">Skriv inn **åååå-MM-dd** i **Format**-feltet.</span><span class="sxs-lookup"><span data-stu-id="067e3-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="067e3-200">Velg **Dato** i feltet **Dato/klokkeslett**-type.</span><span class="sxs-lookup"><span data-stu-id="067e3-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="067e3-201">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-201">Click **OK**.</span></span>
11. <span data-ttu-id="067e3-202">Velg **Xml\Melding\MessageId** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="067e3-203">Klikk på **Legg til** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="067e3-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="067e3-204">Velg **Tekst\Streng** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="067e3-205">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-205">Click **OK**.</span></span>
15. <span data-ttu-id="067e3-206">Velg **Xml\Melding\Betalinger\Vare\Leverandør\Navn** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="067e3-207">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="067e3-207">Click **Add String**.</span></span>
17. <span data-ttu-id="067e3-208">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-208">Click **OK**.</span></span>
18. <span data-ttu-id="067e3-209">Velg **Xml\Melding\Betalinger\Vare\Leverandør\Bank\RoutingNumber** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="067e3-210">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="067e3-210">Click **Add String**.</span></span>
20. <span data-ttu-id="067e3-211">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-211">Click **OK**.</span></span>
21. <span data-ttu-id="067e3-212">Velg **Xml\Melding\Betalinger\Vare\Leverandør\Bank\AccountNumber** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="067e3-213">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="067e3-213">Click **Add String**.</span></span>
23. <span data-ttu-id="067e3-214">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-214">Click **OK**.</span></span>
24. <span data-ttu-id="067e3-215">Velg **Xml\Melding\Betalinger\Vare\Betaler\Navn** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="067e3-216">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="067e3-216">Click **Add String**.</span></span>
26. <span data-ttu-id="067e3-217">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-217">Click **OK**.</span></span>
27. <span data-ttu-id="067e3-218">Velg **Xml\Melding\Betalinger\Vare\Betaler\Bank\RoutingNumber** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="067e3-219">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="067e3-219">Click **Add String**.</span></span>
29. <span data-ttu-id="067e3-220">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-220">Click **OK**.</span></span>
30. <span data-ttu-id="067e3-221">Velg **Xml\Melding\Betalinger\Vare\Betaler\Bank\AccountNumber** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="067e3-222">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="067e3-222">Click **Add String**.</span></span>
32. <span data-ttu-id="067e3-223">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-223">Click **OK**.</span></span>
33. <span data-ttu-id="067e3-224">Velg **Xml\Melding\Betalinger\Vare\Valuta** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="067e3-225">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="067e3-225">Click **Add String**.</span></span>
35. <span data-ttu-id="067e3-226">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-226">Click **OK**.</span></span>
36. <span data-ttu-id="067e3-227">Velg **Xml\Melding\Betalinger\Vare\Beskrivelse** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="067e3-228">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="067e3-228">Click **Add String**.</span></span>
38. <span data-ttu-id="067e3-229">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-229">Click **OK**.</span></span>
39. <span data-ttu-id="067e3-230">Velg **Xml\Melding\Betalinger\Vare\Beløp** i treet.</span><span class="sxs-lookup"><span data-stu-id="067e3-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="067e3-231">Klikk på **Legg til streng**.</span><span class="sxs-lookup"><span data-stu-id="067e3-231">Click **Add String**.</span></span>
41. <span data-ttu-id="067e3-232">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="067e3-232">Click **OK**.</span></span>
42. <span data-ttu-id="067e3-233">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="067e3-233">Click **Save**.</span></span>
43. <span data-ttu-id="067e3-234">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="067e3-234">Close the page.</span></span>

