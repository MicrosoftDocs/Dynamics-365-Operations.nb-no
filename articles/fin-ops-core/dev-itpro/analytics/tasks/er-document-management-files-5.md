---
title: ER Bruke dokumentbehandlingsfiler i formatutdata (del 5 - Endre og kjøre format)
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1a52a7dd3b31c0189577422a79d47b318aae4a05
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142014"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="a9d65-103">ER Bruke dokumentbehandlingsfiler i formatutdata (del 5 - Endre og kjøre format)</span><span class="sxs-lookup"><span data-stu-id="a9d65-103">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a9d65-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata.</span><span class="sxs-lookup"><span data-stu-id="a9d65-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="a9d65-105">Denne fremgangsmåten kan utføres i firmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="a9d65-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="a9d65-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke dokumentbehandlingsfiler i formatutdata (del 4: Kjøre format).</span><span class="sxs-lookup"><span data-stu-id="a9d65-106">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 4: Run format)" procedure.</span></span>

<span data-ttu-id="a9d65-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="a9d65-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="a9d65-108">Endre formatet for å fylle ut vedlegg til generering av meldinger i binærformat</span><span class="sxs-lookup"><span data-stu-id="a9d65-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="a9d65-109">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="a9d65-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a9d65-110">Utvid Kundefakturamodell i treet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="a9d65-111">Utvid Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="a9d65-112">Velg Kundefakturamodell\Kundefakturamodell (egendefinert)\Eksempelmelding for elektronisk faktura i treet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="a9d65-113">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="a9d65-113">Click Designer.</span></span>
    * <span data-ttu-id="a9d65-114">Du skal fylle ut fakturameldingen i de genererte utdataene som en XML-fil ved hjelp av UNICODE-koding.</span><span class="sxs-lookup"><span data-stu-id="a9d65-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="a9d65-115">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a9d65-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="a9d65-116">Velg Felles\Fil i treet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="a9d65-117">I Navn-feltet skriver du inn XML-melding.</span><span class="sxs-lookup"><span data-stu-id="a9d65-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="a9d65-118">XML-melding</span><span class="sxs-lookup"><span data-stu-id="a9d65-118">Xml message</span></span>  
9. <span data-ttu-id="a9d65-119">I Koding-feltet skriver du inn UTF-8.</span><span class="sxs-lookup"><span data-stu-id="a9d65-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="a9d65-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="a9d65-120">UTF-8</span></span>  
10. <span data-ttu-id="a9d65-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a9d65-121">Click OK.</span></span>
    * <span data-ttu-id="a9d65-122">Konfigurer de genererte utdataene som en zippet fil.</span><span class="sxs-lookup"><span data-stu-id="a9d65-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="a9d65-123">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a9d65-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="a9d65-124">Velg Felles\Mappe i treet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="a9d65-125">Skriv inn ZIP-utdata i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="a9d65-126">ZIP-utdata</span><span class="sxs-lookup"><span data-stu-id="a9d65-126">Zip output</span></span>  
14. <span data-ttu-id="a9d65-127">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a9d65-127">Click OK.</span></span>
15. <span data-ttu-id="a9d65-128">Velg ZIP-utdata i treet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="a9d65-129">Legg til vedlegg i den zippede genereringsfilen som filer med opprinnelige navn og filtyper.</span><span class="sxs-lookup"><span data-stu-id="a9d65-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="a9d65-130">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a9d65-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="a9d65-131">Velg Felles\Fil i treet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="a9d65-132">Skriv inn Tilknyttet fil i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="a9d65-133">Tilknyttet fil</span><span class="sxs-lookup"><span data-stu-id="a9d65-133">Attached file</span></span>  
19. <span data-ttu-id="a9d65-134">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a9d65-134">Click OK.</span></span>
20. <span data-ttu-id="a9d65-135">Velg ZIP-utdata\Tilknyttet fil i treet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="a9d65-136">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a9d65-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="a9d65-137">Velg Tekst\Base64 i treet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="a9d65-138">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a9d65-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="a9d65-139">Tilordne nye formatelementer til datamodell</span><span class="sxs-lookup"><span data-stu-id="a9d65-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="a9d65-140">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="a9d65-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="a9d65-141">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="a9d65-142">Utvid modell\Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="a9d65-143">Velg ZIP-utdata\Tilknyttet fil\Base64 i treet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="a9d65-144">I treet velger du modell\Fakturavedlegg\Filinnhold.</span><span class="sxs-lookup"><span data-stu-id="a9d65-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="a9d65-145">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="a9d65-145">Click Bind.</span></span>
7. <span data-ttu-id="a9d65-146">Velg ZIP-utdata\Tilknyttet fil i treet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="a9d65-147">Klikk Rediger filnavn.</span><span class="sxs-lookup"><span data-stu-id="a9d65-147">Click Edit filename.</span></span>
9. <span data-ttu-id="a9d65-148">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="a9d65-149">Utvid modell\Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="a9d65-150">Velg modell\Fakturavedlegg\Filnavn i treet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="a9d65-151">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="a9d65-151">Click Add data source.</span></span>
13. <span data-ttu-id="a9d65-152">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="a9d65-152">Click Save.</span></span>
14. <span data-ttu-id="a9d65-153">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a9d65-153">Close the page.</span></span>
15. <span data-ttu-id="a9d65-154">Velg modell\Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="a9d65-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="a9d65-155">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="a9d65-155">Click Bind.</span></span>
17. <span data-ttu-id="a9d65-156">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="a9d65-156">Click Save.</span></span>
18. <span data-ttu-id="a9d65-157">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a9d65-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="a9d65-158">Kjøre den utformede rapporten for den valgte fakturaen</span><span class="sxs-lookup"><span data-stu-id="a9d65-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="a9d65-159">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="a9d65-159">Click Run.</span></span>
2. <span data-ttu-id="a9d65-160">Utvid delen Poster som skal inkluderes ().</span><span class="sxs-lookup"><span data-stu-id="a9d65-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="a9d65-161">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="a9d65-161">Click Filter.</span></span>
4. <span data-ttu-id="a9d65-162">Merk raden for feltet Kundefakturajournal og Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="a9d65-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="a9d65-163">I kriteriefeltet Salgsordre skriver du inn ordrenummeret 000148.</span><span class="sxs-lookup"><span data-stu-id="a9d65-163">In the Criteria field, In the criteria "Sales order" field, type the order number 000148.</span></span>
    * <span data-ttu-id="a9d65-164">000148</span><span class="sxs-lookup"><span data-stu-id="a9d65-164">000148</span></span>  
6. <span data-ttu-id="a9d65-165">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a9d65-165">Click OK.</span></span>
7. <span data-ttu-id="a9d65-166">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a9d65-166">Click OK.</span></span>
    * <span data-ttu-id="a9d65-167">Se gjennom de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="a9d65-167">Review the generated output.</span></span> <span data-ttu-id="a9d65-168">Vær oppmerksom på at i tillegg til fakturameldingen i XML-format, er det opprettet en enkelt fil for hvert vedlegg.</span><span class="sxs-lookup"><span data-stu-id="a9d65-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="a9d65-169">Vedleggsfilene fylles ut med de zippede utdataene i binærformat.</span><span class="sxs-lookup"><span data-stu-id="a9d65-169">The attachment files are populated with the zipped output in binary format.</span></span>  

