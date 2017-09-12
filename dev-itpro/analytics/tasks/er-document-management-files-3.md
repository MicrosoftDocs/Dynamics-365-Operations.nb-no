--- 
title: "Opprette format for å bruke dokumentbehandlingsfiler i formatutdata for elektronisk rapportering (ER)"
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5548839c4d394d45cfb39da50ca78dab4b4e08e4
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="0e6bf-103">Opprette format for å bruke dokumentbehandlingsfiler i formatutdata for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="0e6bf-103">Create format to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e6bf-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="0e6bf-105">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="0e6bf-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke dokumentbehandlingsfiler i formatutdata (del 2: Utvide datamodell).</span><span class="sxs-lookup"><span data-stu-id="0e6bf-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="0e6bf-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="0e6bf-108">Opprette et format for å behandle fakturaer</span><span class="sxs-lookup"><span data-stu-id="0e6bf-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="0e6bf-109">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="0e6bf-110">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="0e6bf-111">Utvid Kundefakturamodell i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="0e6bf-112">Velg Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="0e6bf-113">Du vil opprette et format for å generere elektroniske meldinger med informasjon om filer som er knyttet til en salgsordre som er relatert til en faktura for elektronisk behandling.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="0e6bf-114">Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="0e6bf-115">I feltet Ny angir du Format basert på datamodellen Kundefakturamodell (egendefinert).</span><span class="sxs-lookup"><span data-stu-id="0e6bf-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="0e6bf-116">I Navn-feltet skriver du inn Eksempelmelding for elektronisk faktura.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="0e6bf-117">Eksempelmelding for elektronisk faktura</span><span class="sxs-lookup"><span data-stu-id="0e6bf-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="0e6bf-118">Angi eller velg en verdi i feltet Definisjon av datamodell.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="0e6bf-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="0e6bf-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="0e6bf-120">Klikk Opprett konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="0e6bf-121">Utforme et format for å fylle ut vedlegg til generering av en melding i MIME-format</span><span class="sxs-lookup"><span data-stu-id="0e6bf-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="0e6bf-122">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-122">Click Designer.</span></span>
2. <span data-ttu-id="0e6bf-123">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="0e6bf-124">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="0e6bf-125">I Navn-feltet skriver du inn Faktura.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="0e6bf-126">Faktura</span><span class="sxs-lookup"><span data-stu-id="0e6bf-126">Invoice</span></span>  
5. <span data-ttu-id="0e6bf-127">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-127">Click OK.</span></span>
6. <span data-ttu-id="0e6bf-128">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="0e6bf-129">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="0e6bf-130">Skriv inn Salgsordre i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="0e6bf-131">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="0e6bf-131">SalesOrder</span></span>  
9. <span data-ttu-id="0e6bf-132">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-132">Click OK.</span></span>
10. <span data-ttu-id="0e6bf-133">Klikk Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="0e6bf-134">Skriv inn Fakturanummer i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="0e6bf-135">Fakturanummer</span><span class="sxs-lookup"><span data-stu-id="0e6bf-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="0e6bf-136">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-136">Click OK.</span></span>
13. <span data-ttu-id="0e6bf-137">Klikk Legg til attributt.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="0e6bf-138">Skriv inn Fakturabeløp i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="0e6bf-139">Fakturabeløp</span><span class="sxs-lookup"><span data-stu-id="0e6bf-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="0e6bf-140">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-140">Click OK.</span></span>
16. <span data-ttu-id="0e6bf-141">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="0e6bf-142">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="0e6bf-143">I Navn-feltet skriver du inn Vedlagte dokumenter.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="0e6bf-144">Vedlagte dokumenter</span><span class="sxs-lookup"><span data-stu-id="0e6bf-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="0e6bf-145">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-145">Click OK.</span></span>
20. <span data-ttu-id="0e6bf-146">Velg Faktura\Vedlagte dokumenter i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="0e6bf-147">Klikk Legg til element.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-147">Click Add Element.</span></span>
22. <span data-ttu-id="0e6bf-148">I Navn-feltet skriver du inn Dokument.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="0e6bf-149">Dokument</span><span class="sxs-lookup"><span data-stu-id="0e6bf-149">Document</span></span>  
23. <span data-ttu-id="0e6bf-150">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-150">Click OK.</span></span>
24. <span data-ttu-id="0e6bf-151">Velg Faktura\Vedlagte dokumenter\Dokument i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="0e6bf-152">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="0e6bf-153">Velg XML\Attributt i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="0e6bf-154">Skriv inn Filnavn i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="0e6bf-155">Filnavn</span><span class="sxs-lookup"><span data-stu-id="0e6bf-155">FileName</span></span>  
28. <span data-ttu-id="0e6bf-156">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-156">Click OK.</span></span>
29. <span data-ttu-id="0e6bf-157">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="0e6bf-158">Velg XML\Element i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="0e6bf-159">Skriv inn Filinnhold i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="0e6bf-160">Filinnhold</span><span class="sxs-lookup"><span data-stu-id="0e6bf-160">FileContent</span></span>  
32. <span data-ttu-id="0e6bf-161">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-161">Click OK.</span></span>
33. <span data-ttu-id="0e6bf-162">Velg Faktura\Vedlagte dokumenter\Dokument\Filinnhold i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="0e6bf-163">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="0e6bf-164">Velg Tekst\Base64 i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="0e6bf-165">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="0e6bf-166">Tilordne formatelementer til datamodell som datakilde</span><span class="sxs-lookup"><span data-stu-id="0e6bf-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="0e6bf-167">Velg Faktura\Salgsordre i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="0e6bf-168">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="0e6bf-169">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="0e6bf-170">Velg modell\Salgsordrenummer(SalesId) i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="0e6bf-171">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-171">Click Bind.</span></span>
6. <span data-ttu-id="0e6bf-172">Velg Faktura\Fakturanummer i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="0e6bf-173">Utvid modell\Grunnlagsfaktura(InvoiceBase) i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="0e6bf-174">Velg modell\Grunnlagsfaktura(InvoiceBase)\Fakturanummer(Id) i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="0e6bf-175">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-175">Click Bind.</span></span>
10. <span data-ttu-id="0e6bf-176">Velg Faktura\Fakturabeløp i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="0e6bf-177">Velg modell\Grunnlagsfaktura(InvoiceBase)\Fakturabeløp(Amount) i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="0e6bf-178">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-178">Click Bind.</span></span>
13. <span data-ttu-id="0e6bf-179">Utvid modell\Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="0e6bf-180">I treet velger du modell\Fakturavedlegg\Filinnhold.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="0e6bf-181">Velg Faktura\Vedlagte dokumenter\Dokument\Filinnhold\Base64 i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="0e6bf-182">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-182">Click Bind.</span></span>
17. <span data-ttu-id="0e6bf-183">Velg modell\Fakturavedlegg\Filnavn i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="0e6bf-184">Velg Faktura\Vedlagte dokumenter\Dokument\Filnavn i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="0e6bf-185">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-185">Click Bind.</span></span>
20. <span data-ttu-id="0e6bf-186">Velg modell\Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="0e6bf-187">Velg Faktura\Vedlagte dokumenter\Dokument i treet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="0e6bf-188">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-188">Click Bind.</span></span>
23. <span data-ttu-id="0e6bf-189">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-189">Click Save.</span></span>
24. <span data-ttu-id="0e6bf-190">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-190">Close the page.</span></span>


