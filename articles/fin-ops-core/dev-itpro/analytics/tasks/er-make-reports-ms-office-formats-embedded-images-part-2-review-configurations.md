---
title: Gå gjennom konfigurasjoner for å generere rapporter i Office-format som inneholder innebygde bilder
description: Dette emnet beskriver hvordan du utformer rapportkonfigurasjoner for å generere elektroniske dokumenter som inneholder innebygde bilder. (Del 1 – definere parametere).
author: NickSelin
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de815b363daa9135b50a2f5c9c4ac19e87b6b7ee
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751588"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="47cc7-104">Gå gjennom konfigurasjoner for å generere rapporter i Office-format som inneholder innebygde bilder</span><span class="sxs-lookup"><span data-stu-id="47cc7-104">Review configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="47cc7-105">For å fullføre disse trinnene, må du først fullføre trinnene i oppgaveveiledningen "ER lage rapporter i MS Office-formater med innebygde bilder (del 1: Definere parametere)".</span><span class="sxs-lookup"><span data-stu-id="47cc7-105">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)" task guide.</span></span>

<span data-ttu-id="47cc7-106">Denne fremgangsmåten viser hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere elektroniske dokumenter som inneholder innebygde bilder i Microsoft Excel og Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="47cc7-106">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="47cc7-107">I dette eksemplet skal du gå gjennom ER-konfigurasjoner for eksempelfirmaet "Litware, Inc".</span><span class="sxs-lookup"><span data-stu-id="47cc7-107">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="47cc7-108">Denne fremgangsmåten er ment for brukere som har den systemansvarlige eller elektronisk rapportering utvikler-rolle tilordnet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-108">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="47cc7-109">Trinnene kan fullføres ved hjelp av USMF-datasett.</span><span class="sxs-lookup"><span data-stu-id="47cc7-109">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="47cc7-110">Gå gjennom den importerte datamodellen</span><span class="sxs-lookup"><span data-stu-id="47cc7-110">Review the imported data model</span></span>
1. <span data-ttu-id="47cc7-111">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="47cc7-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="47cc7-112">Velg Modell for sjekker i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-112">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="47cc7-113">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="47cc7-113">Click Designer.</span></span>
    * <span data-ttu-id="47cc7-114">Denne modellen er utviklet for å representere sjekker for betaling med tanke på bedrifter og tilordning av denne modellen til programmets datakilder.</span><span class="sxs-lookup"><span data-stu-id="47cc7-114">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application's data sources.</span></span> <span data-ttu-id="47cc7-115">Se gjennom denne modellen som operasjoner ER utformingen.</span><span class="sxs-lookup"><span data-stu-id="47cc7-115">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="47cc7-116">Legg merke til attributtene for modellelementene presenteres: strukturen, navn, beskrivelse, datatypen og så videre.</span><span class="sxs-lookup"><span data-stu-id="47cc7-116">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="47cc7-117">Utvid 'root' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-117">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="47cc7-118">Velg 'rot\sjekker' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-118">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="47cc7-119">Utvid 'rot\sjekker' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-119">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="47cc7-120">Utvid 'rot\sjekker\attributter' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-120">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="47cc7-121">Utvid 'rot\betaler' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-121">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="47cc7-122">Velg 'rot\istestrun' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-122">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="47cc7-123">Velg 'rot\oppsett' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-123">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="47cc7-124">I oppsettet av elementene i denne modellen representerer informasjon om utskrift sjekk skjemaoppsettet for den valgte bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="47cc7-124">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="47cc7-125">Det inneholder også to noder av typen beholder for lagring av bilder.</span><span class="sxs-lookup"><span data-stu-id="47cc7-125">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="47cc7-126">Utvid 'rot\oppsett' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-126">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="47cc7-127">Velg 'rot\oppsett\firmalogo' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-127">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="47cc7-128">Utvid 'rot\oppsett\firmalogo' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-128">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="47cc7-129">Velg 'rot\oppsett\firmalogo\bilde' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-129">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="47cc7-130">Velg 'rot\oppsett\firmalogo\isprinted' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-130">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="47cc7-131">Velg 'rot\oppsett\signatur' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-131">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="47cc7-132">Utvid 'rot\oppsett\signatur' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-132">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="47cc7-133">Velg 'rot\oppsett\signatur\bilde' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-133">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="47cc7-134">Velg 'rot\oppsett\signatur\isprinted' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-134">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="47cc7-135">Legg merke til at to bilde dataelementer er bundet til feltene i tabellene som inneholder bilder av firmalogoen og godkjente personens signatur i binært format.</span><span class="sxs-lookup"><span data-stu-id="47cc7-135">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person's signature in binary format.</span></span>  
20. <span data-ttu-id="47cc7-136">Utvid 'rot\oppsett\vannmerke' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-136">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="47cc7-137">Klikk på Tilordne modell til datakilde.</span><span class="sxs-lookup"><span data-stu-id="47cc7-137">Click Map model to datasource.</span></span>
22. <span data-ttu-id="47cc7-138">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="47cc7-138">Click Designer.</span></span>
23. <span data-ttu-id="47cc7-139">Utvid 'chequesselected' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-139">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="47cc7-140">Utvid "oppsett" i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-140">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="47cc7-141">Utvid 'oppsett\firmalogo' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-141">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="47cc7-142">Utvid "oppsett\signatur" i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-142">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="47cc7-143">Utvid 'oppsett\vannmerke' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-143">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="47cc7-144">Aktiver Vis detaljer.</span><span class="sxs-lookup"><span data-stu-id="47cc7-144">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="47cc7-145">Legg merke til at modellelementet sjekker data er bundet til tabellen for TmpChequePrintout som under kjøringen inneholder poster for sjekker som brukeren har valgt for utskrift.</span><span class="sxs-lookup"><span data-stu-id="47cc7-145">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="47cc7-146">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="47cc7-146">Close the page.</span></span>
30. <span data-ttu-id="47cc7-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="47cc7-147">Close the page.</span></span>
31. <span data-ttu-id="47cc7-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="47cc7-148">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="47cc7-149">Gå gjennom det importerte formatet</span><span class="sxs-lookup"><span data-stu-id="47cc7-149">Review the imported format</span></span>
1. <span data-ttu-id="47cc7-150">Utvid Modell for sjekker i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-150">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="47cc7-151">Velg 'Modell for sjekker\Utskriftsformat for sjekker' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-151">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="47cc7-152">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="47cc7-152">Click Designer.</span></span>
4. <span data-ttu-id="47cc7-153">Klikk på Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="47cc7-153">Click Attachments.</span></span>
5. <span data-ttu-id="47cc7-154">Klikk på Åpne.</span><span class="sxs-lookup"><span data-stu-id="47cc7-154">Click Open.</span></span>
    * <span data-ttu-id="47cc7-155">Åpne den vedlagte rapportmalen i Excel.</span><span class="sxs-lookup"><span data-stu-id="47cc7-155">Open the attached report's template in Excel.</span></span>  
    * <span data-ttu-id="47cc7-156">Se gjennom vedlagte rapportens Excel-malen som skal brukes til å skrive ut sjekker.</span><span class="sxs-lookup"><span data-stu-id="47cc7-156">Review the attached report's Excel template that will be used to print cheques.</span></span> <span data-ttu-id="47cc7-157">Malen inneholder to sjekker per side, og er utformet for å skrive ut sjekker til det fortrykte skjemaet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-157">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="47cc7-158">Legg merke til at to tomme bilder bygges.</span><span class="sxs-lookup"><span data-stu-id="47cc7-158">Note that two blank images are embedded.</span></span> <span data-ttu-id="47cc7-159">Disse tomme bildene er for firmalogoen og signaturen til personen som godkjenner en betaling.</span><span class="sxs-lookup"><span data-stu-id="47cc7-159">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="47cc7-160">Kontroller at bildene kalles CompLogo og SignatureImage, henholdsvis i Excel.</span><span class="sxs-lookup"><span data-stu-id="47cc7-160">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="47cc7-161">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="47cc7-161">Close the page.</span></span>
7. <span data-ttu-id="47cc7-162">Utvid 'Report' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-162">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="47cc7-163">Utvid 'Rapport\ChequeLines' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-163">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="47cc7-164">Velg 'Rapport\ChequeLines\CompLogo' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-164">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="47cc7-165">Aktiver Vis detaljer.</span><span class="sxs-lookup"><span data-stu-id="47cc7-165">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="47cc7-166">Legg merke til at formatet "CompLogo" celleobjekt representerer Excel varen som skal brukes til å fylle ut bildet for bedriftslogo i rapporten.</span><span class="sxs-lookup"><span data-stu-id="47cc7-166">Note that the 'CompLogo' format's cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="47cc7-167">Dette formatet elementet bundet bilde data modellelement som inneholder et bilde for bedriftslogo i binært format under kjøringen.</span><span class="sxs-lookup"><span data-stu-id="47cc7-167">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="47cc7-168">Klikk på fanen Tilordning.</span><span class="sxs-lookup"><span data-stu-id="47cc7-168">Click the Mapping tab.</span></span>
12. <span data-ttu-id="47cc7-169">Klikk på Redigering aktivert.</span><span class="sxs-lookup"><span data-stu-id="47cc7-169">Click Edit enabled.</span></span>
    * <span data-ttu-id="47cc7-170">Vær oppmerksom på at du kan gjøre celleobjekt formatet "CompLogo" slik at den ikke lenger er aktivert.</span><span class="sxs-lookup"><span data-stu-id="47cc7-170">Note that you can make the 'CompLogo' format's cell element so that it's no longer enabled.</span></span> <span data-ttu-id="47cc7-171">I dette tilfellet skjuler det tilknyttede elementet for Excel-bildet en firmalogo i den genererte rapporten.</span><span class="sxs-lookup"><span data-stu-id="47cc7-171">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="47cc7-172">Hvis aktivert uttrykket returnerer SANN, og den definerte bindingen gir ikke noe bilde, viser det tilknyttede elementet for Excel-bilde et bilde som er lagret i Excel-malen.</span><span class="sxs-lookup"><span data-stu-id="47cc7-172">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="47cc7-173">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="47cc7-173">Close the page.</span></span>
14. <span data-ttu-id="47cc7-174">Utvid 'labels: Container' i treet.</span><span class="sxs-lookup"><span data-stu-id="47cc7-174">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="47cc7-175">Enkelte etiketter vises i skjemaet forhåndstrykt sjekk inkluderes i rapporten når den opprettes for testformål.</span><span class="sxs-lookup"><span data-stu-id="47cc7-175">Some labels that are presented in the preprinted cheque form will be included in the report when it's created for testing purposes.</span></span> <span data-ttu-id="47cc7-176">Imidlertid skrives disse ikke ut ved reell utskrift, fordi det forhåndstrykte skjemaet allerede inneholder dem.</span><span class="sxs-lookup"><span data-stu-id="47cc7-176">However, those labels won't be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="47cc7-177">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="47cc7-177">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]