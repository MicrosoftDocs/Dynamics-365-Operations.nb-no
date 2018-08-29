--- 
title: "Endre og kjøre formater for å bruke dokumentbehandlingsfiler i ER-utdata"
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 5effbecf98e633d07f9e5eb22d3df1a12967c1e4
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---
# <a name="modify-and-run-formats-to-use-document-management-files-in-er-output"></a><span data-ttu-id="0e8b2-103">Endre og kjøre formater for å bruke dokumentbehandlingsfiler i ER-utdata</span><span class="sxs-lookup"><span data-stu-id="0e8b2-103">Modify and run formats to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e8b2-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="0e8b2-105">Denne fremgangsmåten kan utføres i firmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="0e8b2-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke dokumentbehandlingsfiler i formatutdata (del 4: Kjøre format).</span><span class="sxs-lookup"><span data-stu-id="0e8b2-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4): Run format” procedure.</span></span>

<span data-ttu-id="0e8b2-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="0e8b2-108">Endre formatet for å fylle ut vedlegg til generering av meldinger i binærformat</span><span class="sxs-lookup"><span data-stu-id="0e8b2-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="0e8b2-109">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="0e8b2-110">Utvid Kundefakturamodell i treet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="0e8b2-111">Utvid Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="0e8b2-112">Velg Kundefakturamodell\Kundefakturamodell (egendefinert)\Eksempelmelding for elektronisk faktura i treet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="0e8b2-113">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-113">Click Designer.</span></span>
    * <span data-ttu-id="0e8b2-114">Du skal fylle ut fakturameldingen i de genererte utdataene som en XML-fil ved hjelp av UNICODE-koding.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="0e8b2-115">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="0e8b2-116">Velg Felles\Fil i treet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="0e8b2-117">I Navn-feltet skriver du inn XML-melding.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="0e8b2-118">XML-melding</span><span class="sxs-lookup"><span data-stu-id="0e8b2-118">Xml message</span></span>  
9. <span data-ttu-id="0e8b2-119">I Koding-feltet skriver du inn UTF-8.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="0e8b2-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="0e8b2-120">UTF-8</span></span>  
10. <span data-ttu-id="0e8b2-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-121">Click OK.</span></span>
    * <span data-ttu-id="0e8b2-122">Konfigurer de genererte utdataene som en zippet fil.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="0e8b2-123">Klikk Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="0e8b2-124">Velg Felles\Mappe i treet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="0e8b2-125">Skriv inn ZIP-utdata i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="0e8b2-126">ZIP-utdata</span><span class="sxs-lookup"><span data-stu-id="0e8b2-126">Zip output</span></span>  
14. <span data-ttu-id="0e8b2-127">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-127">Click OK.</span></span>
15. <span data-ttu-id="0e8b2-128">Velg ZIP-utdata i treet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="0e8b2-129">Legg til vedlegg i den zippede genereringsfilen som filer med opprinnelige navn og filtyper.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="0e8b2-130">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="0e8b2-131">Velg Felles\Fil i treet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="0e8b2-132">Skriv inn Tilknyttet fil i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="0e8b2-133">Tilknyttet fil</span><span class="sxs-lookup"><span data-stu-id="0e8b2-133">Attached file</span></span>  
19. <span data-ttu-id="0e8b2-134">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-134">Click OK.</span></span>
20. <span data-ttu-id="0e8b2-135">Velg ZIP-utdata\Tilknyttet fil i treet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="0e8b2-136">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="0e8b2-137">Velg Tekst\Base64 i treet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="0e8b2-138">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="0e8b2-139">Tilordne nye formatelementer til datamodell</span><span class="sxs-lookup"><span data-stu-id="0e8b2-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="0e8b2-140">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="0e8b2-141">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="0e8b2-142">Utvid modell\Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="0e8b2-143">Velg ZIP-utdata\Tilknyttet fil\Base64 i treet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="0e8b2-144">I treet velger du modell\Fakturavedlegg\Filinnhold.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="0e8b2-145">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-145">Click Bind.</span></span>
7. <span data-ttu-id="0e8b2-146">Velg ZIP-utdata\Tilknyttet fil i treet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="0e8b2-147">Klikk Rediger filnavn.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-147">Click Edit filename.</span></span>
9. <span data-ttu-id="0e8b2-148">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="0e8b2-149">Utvid modell\Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="0e8b2-150">Velg modell\Fakturavedlegg\Filnavn i treet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="0e8b2-151">Klikk Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-151">Click Add data source.</span></span>
13. <span data-ttu-id="0e8b2-152">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-152">Click Save.</span></span>
14. <span data-ttu-id="0e8b2-153">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-153">Close the page.</span></span>
15. <span data-ttu-id="0e8b2-154">Velg modell\Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="0e8b2-155">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-155">Click Bind.</span></span>
17. <span data-ttu-id="0e8b2-156">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-156">Click Save.</span></span>
18. <span data-ttu-id="0e8b2-157">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="0e8b2-158">Kjøre den utformede rapporten for den valgte fakturaen</span><span class="sxs-lookup"><span data-stu-id="0e8b2-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="0e8b2-159">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-159">Click Run.</span></span>
2. <span data-ttu-id="0e8b2-160">Utvid delen Poster som skal inkluderes ().</span><span class="sxs-lookup"><span data-stu-id="0e8b2-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="0e8b2-161">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-161">Click Filter.</span></span>
4. <span data-ttu-id="0e8b2-162">Merk raden for feltet Kundefakturajournal og Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="0e8b2-163">I kriteriefeltet Salgsordre skriver du inn ordrenummeret 000148.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="0e8b2-164">000148</span><span class="sxs-lookup"><span data-stu-id="0e8b2-164">000148</span></span>  
6. <span data-ttu-id="0e8b2-165">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-165">Click OK.</span></span>
7. <span data-ttu-id="0e8b2-166">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-166">Click OK.</span></span>
    * <span data-ttu-id="0e8b2-167">Se gjennom de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-167">Review the generated output.</span></span> <span data-ttu-id="0e8b2-168">Vær oppmerksom på at i tillegg til fakturameldingen i XML-format, er det opprettet en enkelt fil for hvert vedlegg.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-168">Note, in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="0e8b2-169">Vedleggsfilene fylles ut med de zippede utdataene i binærformat.</span><span class="sxs-lookup"><span data-stu-id="0e8b2-169">The attachment files are populated with the zipped output in binary format.</span></span>  


