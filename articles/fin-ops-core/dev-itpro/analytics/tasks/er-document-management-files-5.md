---
title: ER Bruke dokumentbehandlingsfiler i formatutdata (del 5 - Endre og kjøre format)
description: Dette emnet beskriver hvordan du konfigurerer et ER-format (Elektronisk rapportering) slik at det bruker dokumentbehandlingsfiler (vedlegg) i ER-utdata. (Del 5)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6062945dfea0eec02e5055e9ebe697189267e051
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564816"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="35219-104">ER Bruke dokumentbehandlingsfiler i formatutdata (del 5 - Endre og kjøre format)</span><span class="sxs-lookup"><span data-stu-id="35219-104">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="35219-105">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata.</span><span class="sxs-lookup"><span data-stu-id="35219-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="35219-106">Denne fremgangsmåten kan utføres i firmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="35219-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="35219-107">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke dokumentbehandlingsfiler i formatutdata (del 4: Kjøre format).</span><span class="sxs-lookup"><span data-stu-id="35219-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 4: Run format)" procedure.</span></span>

<span data-ttu-id="35219-108">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="35219-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="35219-109">Endre formatet for å fylle ut vedlegg til generering av meldinger i binærformat</span><span class="sxs-lookup"><span data-stu-id="35219-109">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="35219-110">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="35219-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="35219-111">Utvid Kundefakturamodell i treet.</span><span class="sxs-lookup"><span data-stu-id="35219-111">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="35219-112">Utvid Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.</span><span class="sxs-lookup"><span data-stu-id="35219-112">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="35219-113">Velg Kundefakturamodell\Kundefakturamodell (egendefinert)\Eksempelmelding for elektronisk faktura i treet.</span><span class="sxs-lookup"><span data-stu-id="35219-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="35219-114">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="35219-114">Click Designer.</span></span>
    * <span data-ttu-id="35219-115">Du skal fylle ut fakturameldingen i de genererte utdataene som en XML-fil ved hjelp av UNICODE-koding.</span><span class="sxs-lookup"><span data-stu-id="35219-115">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="35219-116">Klikk på Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="35219-116">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="35219-117">Velg Felles\Fil i treet.</span><span class="sxs-lookup"><span data-stu-id="35219-117">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="35219-118">I Navn-feltet skriver du inn XML-melding.</span><span class="sxs-lookup"><span data-stu-id="35219-118">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="35219-119">XML-melding</span><span class="sxs-lookup"><span data-stu-id="35219-119">Xml message</span></span>  
9. <span data-ttu-id="35219-120">I Koding-feltet skriver du inn UTF-8.</span><span class="sxs-lookup"><span data-stu-id="35219-120">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="35219-121">UTF-8</span><span class="sxs-lookup"><span data-stu-id="35219-121">UTF-8</span></span>  
10. <span data-ttu-id="35219-122">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="35219-122">Click OK.</span></span>
    * <span data-ttu-id="35219-123">Konfigurer de genererte utdataene som en zippet fil.</span><span class="sxs-lookup"><span data-stu-id="35219-123">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="35219-124">Klikk på Legg til rot for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="35219-124">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="35219-125">Velg Felles\Mappe i treet.</span><span class="sxs-lookup"><span data-stu-id="35219-125">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="35219-126">Skriv inn ZIP-utdata i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="35219-126">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="35219-127">ZIP-utdata</span><span class="sxs-lookup"><span data-stu-id="35219-127">Zip output</span></span>  
14. <span data-ttu-id="35219-128">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="35219-128">Click OK.</span></span>
15. <span data-ttu-id="35219-129">Velg ZIP-utdata i treet.</span><span class="sxs-lookup"><span data-stu-id="35219-129">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="35219-130">Legg til vedlegg i den zippede genereringsfilen som filer med opprinnelige navn og filtyper.</span><span class="sxs-lookup"><span data-stu-id="35219-130">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="35219-131">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="35219-131">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="35219-132">Velg Felles\Fil i treet.</span><span class="sxs-lookup"><span data-stu-id="35219-132">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="35219-133">Skriv inn Tilknyttet fil i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="35219-133">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="35219-134">Tilknyttet fil</span><span class="sxs-lookup"><span data-stu-id="35219-134">Attached file</span></span>  
19. <span data-ttu-id="35219-135">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="35219-135">Click OK.</span></span>
20. <span data-ttu-id="35219-136">Velg ZIP-utdata\Tilknyttet fil i treet.</span><span class="sxs-lookup"><span data-stu-id="35219-136">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="35219-137">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="35219-137">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="35219-138">Velg Tekst\Base64 i treet.</span><span class="sxs-lookup"><span data-stu-id="35219-138">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="35219-139">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="35219-139">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="35219-140">Tilordne nye formatelementer til datamodell</span><span class="sxs-lookup"><span data-stu-id="35219-140">Map new format elements to data model</span></span>
1. <span data-ttu-id="35219-141">Klikk på fanen Tilordning.</span><span class="sxs-lookup"><span data-stu-id="35219-141">Click the Mapping tab.</span></span>
2. <span data-ttu-id="35219-142">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="35219-142">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="35219-143">Utvid modell\Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="35219-143">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="35219-144">Velg ZIP-utdata\Tilknyttet fil\Base64 i treet.</span><span class="sxs-lookup"><span data-stu-id="35219-144">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="35219-145">I treet velger du modell\Fakturavedlegg\Filinnhold.</span><span class="sxs-lookup"><span data-stu-id="35219-145">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="35219-146">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="35219-146">Click Bind.</span></span>
7. <span data-ttu-id="35219-147">Velg ZIP-utdata\Tilknyttet fil i treet.</span><span class="sxs-lookup"><span data-stu-id="35219-147">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="35219-148">Klikk på Rediger filnavn.</span><span class="sxs-lookup"><span data-stu-id="35219-148">Click Edit filename.</span></span>
9. <span data-ttu-id="35219-149">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="35219-149">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="35219-150">Utvid modell\Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="35219-150">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="35219-151">Velg modell\Fakturavedlegg\Filnavn i treet.</span><span class="sxs-lookup"><span data-stu-id="35219-151">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="35219-152">Klikk på Legg til datakilde.</span><span class="sxs-lookup"><span data-stu-id="35219-152">Click Add data source.</span></span>
13. <span data-ttu-id="35219-153">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="35219-153">Click Save.</span></span>
14. <span data-ttu-id="35219-154">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="35219-154">Close the page.</span></span>
15. <span data-ttu-id="35219-155">Velg modell\Fakturavedlegg i treet.</span><span class="sxs-lookup"><span data-stu-id="35219-155">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="35219-156">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="35219-156">Click Bind.</span></span>
17. <span data-ttu-id="35219-157">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="35219-157">Click Save.</span></span>
18. <span data-ttu-id="35219-158">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="35219-158">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="35219-159">Kjøre den utformede rapporten for den valgte fakturaen</span><span class="sxs-lookup"><span data-stu-id="35219-159">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="35219-160">Klikk på Kjør.</span><span class="sxs-lookup"><span data-stu-id="35219-160">Click Run.</span></span>
2. <span data-ttu-id="35219-161">Utvid delen Poster som skal inkluderes ().</span><span class="sxs-lookup"><span data-stu-id="35219-161">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="35219-162">Klikk på Filter.</span><span class="sxs-lookup"><span data-stu-id="35219-162">Click Filter.</span></span>
4. <span data-ttu-id="35219-163">Merk raden for feltet Kundefakturajournal og Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="35219-163">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="35219-164">I kriteriefeltet Salgsordre skriver du inn ordrenummeret 000148.</span><span class="sxs-lookup"><span data-stu-id="35219-164">In the Criteria field, In the criteria "Sales order" field, type the order number 000148.</span></span>
    * <span data-ttu-id="35219-165">000148</span><span class="sxs-lookup"><span data-stu-id="35219-165">000148</span></span>  
6. <span data-ttu-id="35219-166">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="35219-166">Click OK.</span></span>
7. <span data-ttu-id="35219-167">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="35219-167">Click OK.</span></span>
    * <span data-ttu-id="35219-168">Se gjennom de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="35219-168">Review the generated output.</span></span> <span data-ttu-id="35219-169">Vær oppmerksom på at i tillegg til fakturameldingen i XML-format, er det opprettet en enkelt fil for hvert vedlegg.</span><span class="sxs-lookup"><span data-stu-id="35219-169">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="35219-170">Vedleggsfilene fylles ut med de zippede utdataene i binærformat.</span><span class="sxs-lookup"><span data-stu-id="35219-170">The attachment files are populated with the zipped output in binary format.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]