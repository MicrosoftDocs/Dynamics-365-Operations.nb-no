--- 
title: "Gå gjennom konfigurasjoner for å lage rapporter i Microsoft Office-formater med innebygde bilder"
description: "For å fullføre disse trinnene, må du først fullføre trinnene i oppgaveveiledningen \"ER lage rapporter i MS Office-formater med innebygde bilder (del 1: Definere parametere)\"."
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ca4749904607b458dbc0e81e451eb23cc465752e
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="review-configurations-to-make-reports-in-microsoft-office-formats-with-embedded-images"></a><span data-ttu-id="a9a98-103">Gå gjennom konfigurasjoner for å lage rapporter i Microsoft Office-formater med innebygde bilder</span><span class="sxs-lookup"><span data-stu-id="a9a98-103">Review configurations to make reports in Microsoft Office formats with embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a9a98-104">For å fullføre disse trinnene, må du først fullføre trinnene i oppgaveveiledningen "ER lage rapporter i MS Office-formater med innebygde bilder (del 1: Definere parametere)".</span><span class="sxs-lookup"><span data-stu-id="a9a98-104">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)” task guide.</span></span>

<span data-ttu-id="a9a98-105">Denne fremgangsmåten viser hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere elektroniske dokumenter som inneholder innebygde bilder i Microsoft Excel og Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="a9a98-105">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="a9a98-106">I dette eksemplet skal du gå gjennom ER-konfigurasjoner for eksempelfirmaet "Litware, Inc".</span><span class="sxs-lookup"><span data-stu-id="a9a98-106">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="a9a98-107">Denne fremgangsmåten er ment for brukere som har den systemansvarlige eller elektronisk rapportering utvikler-rolle tilordnet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="a9a98-108">Trinnene kan fullføres ved hjelp av USMF-datasett.</span><span class="sxs-lookup"><span data-stu-id="a9a98-108">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="a9a98-109">Gå gjennom den importerte datamodellen</span><span class="sxs-lookup"><span data-stu-id="a9a98-109">Review the imported data model</span></span>
1. <span data-ttu-id="a9a98-110">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="a9a98-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a9a98-111">Velg Modell for sjekker i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-111">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="a9a98-112">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="a9a98-112">Click Designer.</span></span>
    * <span data-ttu-id="a9a98-113">Denne modellen er utviklet for å representere sjekker for betaling med tanke på bedrifter og tilordning av denne modellen til programmets datakilder.</span><span class="sxs-lookup"><span data-stu-id="a9a98-113">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application’s data sources.</span></span> <span data-ttu-id="a9a98-114">Se gjennom denne modellen som operasjoner ER utformingen.</span><span class="sxs-lookup"><span data-stu-id="a9a98-114">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="a9a98-115">Legg merke til attributtene for modellelementene presenteres: strukturen, navn, beskrivelse, datatypen og så videre.</span><span class="sxs-lookup"><span data-stu-id="a9a98-115">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="a9a98-116">Utvid 'root' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-116">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="a9a98-117">Velg 'rot\sjekker' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-117">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="a9a98-118">Utvid 'rot\sjekker' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-118">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="a9a98-119">Utvid 'rot\sjekker\attributter' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-119">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="a9a98-120">Utvid 'rot\betaler' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-120">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="a9a98-121">Velg 'rot\istestrun' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-121">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="a9a98-122">Velg 'rot\oppsett' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-122">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="a9a98-123">I oppsettet av elementene i denne modellen representerer informasjon om utskrift sjekk skjemaoppsettet for den valgte bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="a9a98-123">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="a9a98-124">Det inneholder også to noder av typen beholder for lagring av bilder.</span><span class="sxs-lookup"><span data-stu-id="a9a98-124">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="a9a98-125">Utvid 'rot\oppsett' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-125">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="a9a98-126">Velg 'rot\oppsett\firmalogo' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-126">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="a9a98-127">Utvid 'rot\oppsett\firmalogo' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-127">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="a9a98-128">Velg 'rot\oppsett\firmalogo\bilde' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-128">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="a9a98-129">Velg 'rot\oppsett\firmalogo\isprinted' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-129">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="a9a98-130">Velg 'rot\oppsett\signatur' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-130">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="a9a98-131">Utvid 'rot\oppsett\signatur' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-131">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="a9a98-132">Velg 'rot\oppsett\signatur\bilde' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-132">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="a9a98-133">Velg 'rot\oppsett\signatur\isprinted' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-133">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="a9a98-134">Legg merke til at to bilde dataelementer er bundet til feltene i tabellene som inneholder bilder av firmalogoen og godkjente personens signatur i binært format.</span><span class="sxs-lookup"><span data-stu-id="a9a98-134">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person’s signature in binary format.</span></span>  
20. <span data-ttu-id="a9a98-135">Utvid 'rot\oppsett\vannmerke' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-135">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="a9a98-136">Klikk Tilordne modell til datakilde.</span><span class="sxs-lookup"><span data-stu-id="a9a98-136">Click Map model to datasource.</span></span>
22. <span data-ttu-id="a9a98-137">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="a9a98-137">Click Designer.</span></span>
23. <span data-ttu-id="a9a98-138">Utvid 'chequesselected' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-138">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="a9a98-139">Utvid "oppsett" i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-139">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="a9a98-140">Utvid 'oppsett\firmalogo' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-140">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="a9a98-141">Utvid "oppsett\signatur" i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-141">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="a9a98-142">Utvid 'oppsett\vannmerke' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-142">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="a9a98-143">Aktiver Vis detaljer.</span><span class="sxs-lookup"><span data-stu-id="a9a98-143">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="a9a98-144">Legg merke til at modellelementet sjekker data er bundet til tabellen for TmpChequePrintout som under kjøringen inneholder poster for sjekker som brukeren har valgt for utskrift.</span><span class="sxs-lookup"><span data-stu-id="a9a98-144">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="a9a98-145">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a9a98-145">Close the page.</span></span>
30. <span data-ttu-id="a9a98-146">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a9a98-146">Close the page.</span></span>
31. <span data-ttu-id="a9a98-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a9a98-147">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="a9a98-148">Gå gjennom det importerte formatet</span><span class="sxs-lookup"><span data-stu-id="a9a98-148">Review the imported format</span></span>
1. <span data-ttu-id="a9a98-149">Utvid Modell for sjekker i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-149">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="a9a98-150">Velg 'Modell for sjekker\Utskriftsformat for sjekker' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-150">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="a9a98-151">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="a9a98-151">Click Designer.</span></span>
4. <span data-ttu-id="a9a98-152">Klikk Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="a9a98-152">Click Attachments.</span></span>
5. <span data-ttu-id="a9a98-153">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="a9a98-153">Click Open.</span></span>
    * <span data-ttu-id="a9a98-154">Åpne den vedlagte rapportmalen i Excel.</span><span class="sxs-lookup"><span data-stu-id="a9a98-154">Open the attached report’s template in Excel.</span></span>  
    * <span data-ttu-id="a9a98-155">Se gjennom vedlagte rapportens Excel-malen som skal brukes til å skrive ut sjekker.</span><span class="sxs-lookup"><span data-stu-id="a9a98-155">Review the attached report’s Excel template that will be used to print cheques.</span></span> <span data-ttu-id="a9a98-156">Malen inneholder to sjekker per side, og er utformet for å skrive ut sjekker til det fortrykte skjemaet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-156">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="a9a98-157">Legg merke til at to tomme bilder bygges.</span><span class="sxs-lookup"><span data-stu-id="a9a98-157">Note that two blank images are embedded.</span></span> <span data-ttu-id="a9a98-158">Disse tomme bildene er for firmalogoen og signaturen til personen som godkjenner en betaling.</span><span class="sxs-lookup"><span data-stu-id="a9a98-158">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="a9a98-159">Kontroller at bildene kalles CompLogo og SignatureImage, henholdsvis i Excel.</span><span class="sxs-lookup"><span data-stu-id="a9a98-159">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="a9a98-160">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a9a98-160">Close the page.</span></span>
7. <span data-ttu-id="a9a98-161">Utvid 'Report' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-161">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="a9a98-162">Utvid 'Rapport\ChequeLines' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-162">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="a9a98-163">Velg 'Rapport\ChequeLines\CompLogo' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-163">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="a9a98-164">Aktiver Vis detaljer.</span><span class="sxs-lookup"><span data-stu-id="a9a98-164">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="a9a98-165">Legg merke til at formatet "CompLogo" celleobjekt representerer Excel varen som skal brukes til å fylle ut bildet for bedriftslogo i rapporten.</span><span class="sxs-lookup"><span data-stu-id="a9a98-165">Note that the ‘CompLogo’ format’s cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="a9a98-166">Dette formatet elementet bundet bilde data modellelement som inneholder et bilde for bedriftslogo i binært format under kjøringen.</span><span class="sxs-lookup"><span data-stu-id="a9a98-166">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="a9a98-167">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="a9a98-167">Click the Mapping tab.</span></span>
12. <span data-ttu-id="a9a98-168">Klikk på Redigering aktivert.</span><span class="sxs-lookup"><span data-stu-id="a9a98-168">Click Edit enabled.</span></span>
    * <span data-ttu-id="a9a98-169">Vær oppmerksom på at du kan gjøre celleobjekt formatet "CompLogo" slik at den ikke lenger er aktivert.</span><span class="sxs-lookup"><span data-stu-id="a9a98-169">Note that you can make the ‘CompLogo’ format’s cell element so that it’s no longer enabled.</span></span> <span data-ttu-id="a9a98-170">I dette tilfellet skjuler det tilknyttede elementet for Excel-bildet en firmalogo i den genererte rapporten.</span><span class="sxs-lookup"><span data-stu-id="a9a98-170">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="a9a98-171">Hvis aktivert uttrykket returnerer SANN, og den definerte bindingen gir ikke noe bilde, viser det tilknyttede elementet for Excel-bilde et bilde som er lagret i Excel-malen.</span><span class="sxs-lookup"><span data-stu-id="a9a98-171">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="a9a98-172">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a9a98-172">Close the page.</span></span>
14. <span data-ttu-id="a9a98-173">Utvid 'labels: Container' i treet.</span><span class="sxs-lookup"><span data-stu-id="a9a98-173">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="a9a98-174">Enkelte etiketter vises i skjemaet forhåndstrykt sjekk inkluderes i rapporten når den opprettes for testformål.</span><span class="sxs-lookup"><span data-stu-id="a9a98-174">Some labels that are presented in the preprinted cheque form will be included in the report when it’s created for testing purposes.</span></span> <span data-ttu-id="a9a98-175">Imidlertid skrives disse ikke ut ved utskrift av reell, fordi det fortrykte skjemaet inneholder allerede dem.</span><span class="sxs-lookup"><span data-stu-id="a9a98-175">However, those labels won’t be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="a9a98-176">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a9a98-176">Close the page.</span></span>


