---
title: ER Bruke dokumentbehandlingsfiler i formatutdata (del 3 – Opprette format)
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapporteringsformat til å bruke dokumentbehandlingsfiler i ER-utdata.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4324ed62c56abea6d90d83d950429b6ddf7a84b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142039"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="efc8b-103">ER Bruke dokumentbehandlingsfiler i formatutdata (del 3 – Opprette format)</span><span class="sxs-lookup"><span data-stu-id="efc8b-103">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="efc8b-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata.</span><span class="sxs-lookup"><span data-stu-id="efc8b-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="efc8b-105">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="efc8b-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="efc8b-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke dokumentbehandlingsfiler i formatutdata (del 2: Utvide datamodell).</span><span class="sxs-lookup"><span data-stu-id="efc8b-106">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="efc8b-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="efc8b-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="efc8b-108">Opprette et format for å behandle fakturaer</span><span class="sxs-lookup"><span data-stu-id="efc8b-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="efc8b-109">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="efc8b-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="efc8b-110">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="efc8b-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="efc8b-111">Utvid Kundefakturamodell i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="efc8b-112">Velg Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="efc8b-113">Du vil opprette et format for å generere elektroniske meldinger med informasjon om filer som er knyttet til en salgsordre som er relatert til en faktura for elektronisk behandling.</span><span class="sxs-lookup"><span data-stu-id="efc8b-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="efc8b-114">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="efc8b-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="efc8b-115">I feltet Ny angir du Format basert på datamodellen Kundefakturamodell (egendefinert).</span><span class="sxs-lookup"><span data-stu-id="efc8b-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="efc8b-116">I Navn-feltet skriver du inn Eksempelmelding for elektronisk faktura.</span><span class="sxs-lookup"><span data-stu-id="efc8b-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="efc8b-117">Eksempelmelding for elektronisk faktura</span><span class="sxs-lookup"><span data-stu-id="efc8b-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="efc8b-118">Angi eller velg en verdi i feltet Definisjon av datamodell.</span><span class="sxs-lookup"><span data-stu-id="efc8b-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="efc8b-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="efc8b-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="efc8b-120">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="efc8b-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="efc8b-121">Utforme et format for å fylle ut vedlegg til generering av en melding i MIME-format</span><span class="sxs-lookup"><span data-stu-id="efc8b-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="efc8b-122">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="efc8b-122">Click Designer.</span></span>
2. <span data-ttu-id="efc8b-123">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="efc8b-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="efc8b-124">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="efc8b-125">I Navn-feltet skriver du inn Faktura.</span><span class="sxs-lookup"><span data-stu-id="efc8b-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="efc8b-126">Faktura</span><span class="sxs-lookup"><span data-stu-id="efc8b-126">Invoice</span></span>  
5. <span data-ttu-id="efc8b-127">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="efc8b-127">Click OK.</span></span>
6. <span data-ttu-id="efc8b-128">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="efc8b-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="efc8b-129">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="efc8b-130">Skriv inn Salgsordre i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="efc8b-131">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="efc8b-131">SalesOrder</span></span>  
9. <span data-ttu-id="efc8b-132">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="efc8b-132">Click OK.</span></span>
10. <span data-ttu-id="efc8b-133">Klikk Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="efc8b-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="efc8b-134">Skriv inn Fakturanummer i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="efc8b-135">Fakturanummer</span><span class="sxs-lookup"><span data-stu-id="efc8b-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="efc8b-136">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="efc8b-136">Click OK.</span></span>
13. <span data-ttu-id="efc8b-137">Klikk Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="efc8b-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="efc8b-138">Skriv inn Fakturabeløp i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="efc8b-139">Fakturabeløp</span><span class="sxs-lookup"><span data-stu-id="efc8b-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="efc8b-140">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="efc8b-140">Click OK.</span></span>
16. <span data-ttu-id="efc8b-141">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="efc8b-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="efc8b-142">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="efc8b-143">I Navn-feltet skriver du inn Vedlagte dokumenter.</span><span class="sxs-lookup"><span data-stu-id="efc8b-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="efc8b-144">Vedlagte dokumenter</span><span class="sxs-lookup"><span data-stu-id="efc8b-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="efc8b-145">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="efc8b-145">Click OK.</span></span>
20. <span data-ttu-id="efc8b-146">Velg Faktura\Vedlagte dokumenter i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="efc8b-147">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="efc8b-147">Click Add Element.</span></span>
22. <span data-ttu-id="efc8b-148">I Navn-feltet skriver du inn Dokument.</span><span class="sxs-lookup"><span data-stu-id="efc8b-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="efc8b-149">Dokument</span><span class="sxs-lookup"><span data-stu-id="efc8b-149">Document</span></span>  
23. <span data-ttu-id="efc8b-150">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="efc8b-150">Click OK.</span></span>
24. <span data-ttu-id="efc8b-151">Velg Faktura\Vedlagte dokumenter\Dokument i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="efc8b-152">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="efc8b-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="efc8b-153">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="efc8b-154">Skriv inn Filnavn i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="efc8b-155">Filnavn</span><span class="sxs-lookup"><span data-stu-id="efc8b-155">FileName</span></span>  
28. <span data-ttu-id="efc8b-156">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="efc8b-156">Click OK.</span></span>
29. <span data-ttu-id="efc8b-157">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="efc8b-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="efc8b-158">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="efc8b-159">Skriv inn Filinnhold i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="efc8b-160">Filinnhold</span><span class="sxs-lookup"><span data-stu-id="efc8b-160">FileContent</span></span>  
32. <span data-ttu-id="efc8b-161">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="efc8b-161">Click OK.</span></span>
33. <span data-ttu-id="efc8b-162">Velg Faktura\Vedlagte dokumenter\Dokument\Filinnhold i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="efc8b-163">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="efc8b-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="efc8b-164">Velg Tekst\Base64 i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="efc8b-165">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="efc8b-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="efc8b-166">Tilordne formatelementer til datamodell som datakilde</span><span class="sxs-lookup"><span data-stu-id="efc8b-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="efc8b-167">Velg Faktura\Salgsordre i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="efc8b-168">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="efc8b-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="efc8b-169">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="efc8b-170">Velg modell\Salgsordrenummer(SalesId) i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="efc8b-171">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="efc8b-171">Click Bind.</span></span>
6. <span data-ttu-id="efc8b-172">Velg Faktura\Fakturanummer i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="efc8b-173">Utvid modell\Grunnlagsfaktura(InvoiceBase) i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="efc8b-174">Velg modell\Grunnlagsfaktura(InvoiceBase)\Fakturanummer(Id) i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="efc8b-175">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="efc8b-175">Click Bind.</span></span>
10. <span data-ttu-id="efc8b-176">Velg Faktura\Fakturabeløp i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="efc8b-177">Velg modell\Grunnlagsfaktura(InvoiceBase)\Fakturabeløp(Amount) i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="efc8b-178">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="efc8b-178">Click Bind.</span></span>
13. <span data-ttu-id="efc8b-179">Utvid modell\Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="efc8b-180">I treet velger du modell\Fakturavedlegg\Filinnhold.</span><span class="sxs-lookup"><span data-stu-id="efc8b-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="efc8b-181">Velg Faktura\Vedlagte dokumenter\Dokument\Filinnhold\Base64 i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="efc8b-182">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="efc8b-182">Click Bind.</span></span>
17. <span data-ttu-id="efc8b-183">Velg modell\Fakturavedlegg\Filnavn i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="efc8b-184">Velg Faktura\Vedlagte dokumenter\Dokument\Filnavn i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="efc8b-185">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="efc8b-185">Click Bind.</span></span>
20. <span data-ttu-id="efc8b-186">Velg modell\Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="efc8b-187">Velg Faktura\Vedlagte dokumenter\Dokument i treet.</span><span class="sxs-lookup"><span data-stu-id="efc8b-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="efc8b-188">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="efc8b-188">Click Bind.</span></span>
23. <span data-ttu-id="efc8b-189">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="efc8b-189">Click Save.</span></span>
24. <span data-ttu-id="efc8b-190">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="efc8b-190">Close the page.</span></span>

