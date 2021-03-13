---
title: ER Bruke dokumentbehandlingsfiler i formatutdata (del 3 – Opprette format)
description: Dette emnet beskriver hvordan du konfigurerer et elektronisk rapporteringsformat slik at det bruker dokumentbehandlingsfiler i ER-utdata. (Del 3)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 432cf4c41a7a223ab07b02edf6da7eac9965cff0
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092622"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="31789-104">ER Bruke dokumentbehandlingsfiler i formatutdata (del 3 – Opprette format)</span><span class="sxs-lookup"><span data-stu-id="31789-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31789-105">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata.</span><span class="sxs-lookup"><span data-stu-id="31789-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="31789-106">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="31789-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="31789-107">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke dokumentbehandlingsfiler i formatutdata (del 2: Utvide datamodell).</span><span class="sxs-lookup"><span data-stu-id="31789-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="31789-108">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="31789-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="31789-109">Opprette et format for å behandle fakturaer</span><span class="sxs-lookup"><span data-stu-id="31789-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="31789-110">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="31789-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="31789-111">Klikk på Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="31789-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="31789-112">Utvid Kundefakturamodell i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="31789-113">Velg Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="31789-114">Du vil opprette et format for å generere elektroniske meldinger med informasjon om filer som er knyttet til en salgsordre som er relatert til en faktura for elektronisk behandling.</span><span class="sxs-lookup"><span data-stu-id="31789-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="31789-115">Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="31789-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="31789-116">I feltet Ny angir du Format basert på datamodellen Kundefakturamodell (egendefinert).</span><span class="sxs-lookup"><span data-stu-id="31789-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="31789-117">I Navn-feltet skriver du inn Eksempelmelding for elektronisk faktura.</span><span class="sxs-lookup"><span data-stu-id="31789-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="31789-118">Eksempelmelding for elektronisk faktura</span><span class="sxs-lookup"><span data-stu-id="31789-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="31789-119">Angi eller velg en verdi i feltet Definisjon av datamodell.</span><span class="sxs-lookup"><span data-stu-id="31789-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="31789-120">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="31789-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="31789-121">Klikk på Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="31789-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="31789-122">Utforme et format for å fylle ut vedlegg til generering av en melding i MIME-format</span><span class="sxs-lookup"><span data-stu-id="31789-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="31789-123">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="31789-123">Click Designer.</span></span>
2. <span data-ttu-id="31789-124">Klikk på Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="31789-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="31789-125">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="31789-126">I Navn-feltet skriver du inn Faktura.</span><span class="sxs-lookup"><span data-stu-id="31789-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="31789-127">Faktura</span><span class="sxs-lookup"><span data-stu-id="31789-127">Invoice</span></span>  
5. <span data-ttu-id="31789-128">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="31789-128">Click OK.</span></span>
6. <span data-ttu-id="31789-129">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="31789-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="31789-130">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="31789-131">Skriv inn Salgsordre i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="31789-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="31789-132">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="31789-132">SalesOrder</span></span>  
9. <span data-ttu-id="31789-133">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="31789-133">Click OK.</span></span>
10. <span data-ttu-id="31789-134">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="31789-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="31789-135">Skriv inn Fakturanummer i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="31789-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="31789-136">Fakturanummer</span><span class="sxs-lookup"><span data-stu-id="31789-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="31789-137">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="31789-137">Click OK.</span></span>
13. <span data-ttu-id="31789-138">Klikk på Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="31789-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="31789-139">Skriv inn Fakturabeløp i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="31789-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="31789-140">Fakturabeløp</span><span class="sxs-lookup"><span data-stu-id="31789-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="31789-141">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="31789-141">Click OK.</span></span>
16. <span data-ttu-id="31789-142">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="31789-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="31789-143">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="31789-144">I Navn-feltet skriver du inn Vedlagte dokumenter.</span><span class="sxs-lookup"><span data-stu-id="31789-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="31789-145">Vedlagte dokumenter</span><span class="sxs-lookup"><span data-stu-id="31789-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="31789-146">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="31789-146">Click OK.</span></span>
20. <span data-ttu-id="31789-147">Velg Faktura\Vedlagte dokumenter i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="31789-148">Klikk på Legg til element.</span><span class="sxs-lookup"><span data-stu-id="31789-148">Click Add Element.</span></span>
22. <span data-ttu-id="31789-149">I Navn-feltet skriver du inn Dokument.</span><span class="sxs-lookup"><span data-stu-id="31789-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="31789-150">Dokument</span><span class="sxs-lookup"><span data-stu-id="31789-150">Document</span></span>  
23. <span data-ttu-id="31789-151">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="31789-151">Click OK.</span></span>
24. <span data-ttu-id="31789-152">Velg Faktura\Vedlagte dokumenter\Dokument i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="31789-153">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="31789-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="31789-154">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="31789-155">Skriv inn Filnavn i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="31789-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="31789-156">Filnavn</span><span class="sxs-lookup"><span data-stu-id="31789-156">FileName</span></span>  
28. <span data-ttu-id="31789-157">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="31789-157">Click OK.</span></span>
29. <span data-ttu-id="31789-158">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="31789-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="31789-159">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="31789-160">Skriv inn Filinnhold i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="31789-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="31789-161">Filinnhold</span><span class="sxs-lookup"><span data-stu-id="31789-161">FileContent</span></span>  
32. <span data-ttu-id="31789-162">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="31789-162">Click OK.</span></span>
33. <span data-ttu-id="31789-163">Velg Faktura\Vedlagte dokumenter\Dokument\Filinnhold i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="31789-164">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="31789-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="31789-165">Velg Tekst\Base64 i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="31789-166">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="31789-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="31789-167">Tilordne formatelementer til datamodell som datakilde</span><span class="sxs-lookup"><span data-stu-id="31789-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="31789-168">Velg Faktura\Salgsordre i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="31789-169">Klikk på fanen Tilordning.</span><span class="sxs-lookup"><span data-stu-id="31789-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="31789-170">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="31789-171">Velg modell\Salgsordrenummer(SalesId) i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="31789-172">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="31789-172">Click Bind.</span></span>
6. <span data-ttu-id="31789-173">Velg Faktura\Fakturanummer i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="31789-174">Utvid modell\Grunnlagsfaktura(InvoiceBase) i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="31789-175">Velg modell\Grunnlagsfaktura(InvoiceBase)\Fakturanummer(Id) i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="31789-176">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="31789-176">Click Bind.</span></span>
10. <span data-ttu-id="31789-177">Velg Faktura\Fakturabeløp i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="31789-178">Velg modell\Grunnlagsfaktura(InvoiceBase)\Fakturabeløp(Amount) i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="31789-179">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="31789-179">Click Bind.</span></span>
13. <span data-ttu-id="31789-180">Utvid modell\Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="31789-181">I treet velger du modell\Fakturavedlegg\Filinnhold.</span><span class="sxs-lookup"><span data-stu-id="31789-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="31789-182">Velg Faktura\Vedlagte dokumenter\Dokument\Filinnhold\Base64 i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="31789-183">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="31789-183">Click Bind.</span></span>
17. <span data-ttu-id="31789-184">Velg modell\Fakturavedlegg\Filnavn i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="31789-185">Velg Faktura\Vedlagte dokumenter\Dokument\Filnavn i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="31789-186">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="31789-186">Click Bind.</span></span>
20. <span data-ttu-id="31789-187">Velg modell\Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="31789-188">Velg Faktura\Vedlagte dokumenter\Dokument i treet.</span><span class="sxs-lookup"><span data-stu-id="31789-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="31789-189">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="31789-189">Click Bind.</span></span>
23. <span data-ttu-id="31789-190">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="31789-190">Click Save.</span></span>
24. <span data-ttu-id="31789-191">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="31789-191">Close the page.</span></span>

