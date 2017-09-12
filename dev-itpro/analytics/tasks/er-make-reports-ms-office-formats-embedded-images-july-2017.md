--- 
title: Opprette rapporter i Microsoft Office-formater med innebygde bilder for elektronisk rapportering (ER) (del 1)
description: "De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan designe konfigurasjoner for elektronisk rapportering (ER) for å generere av elektroniske dokumenter i MS Office-formater (Excel og Word), som inneholder innebygde bilder."
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: bfc3d09017b864e6b2811cab9d7f4b05b048148b
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="make-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er--part-1"></a><span data-ttu-id="00918-103">Opprette rapporter i Microsoft Office-formater med innebygde bilder for elektronisk rapportering (ER) (del 1)</span><span class="sxs-lookup"><span data-stu-id="00918-103">Make reports in Microsoft Office formats with embedded images for electronic reporting (ER)  (Part 1)</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="00918-104">De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan designe konfigurasjoner for elektronisk rapportering (ER) for å generere av elektroniske dokumenter i MS Office-formater (Excel og Word), som inneholder innebygde bilder.</span><span class="sxs-lookup"><span data-stu-id="00918-104">The following steps explain how a user playing either ‘System administrator’ or ‘Electronic reporting developer’ role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="00918-105">I dette eksemplet skal du bruke opprettede ER-konfigurasjoner for eksempelfirmaet "Litware, Inc".</span><span class="sxs-lookup"><span data-stu-id="00918-105">In this example, you will use created ER configurations for sample company, ‘Litware, Inc.’.</span></span>  <span data-ttu-id="00918-106">For å fullføre disse trinnene, må du først fullføre trinnene i oppgaveveiledningen "ER lage rapporter i MS Office-formater med innebygde bilder (del 2: se gjennom konfigurasjoner)".</span><span class="sxs-lookup"><span data-stu-id="00918-106">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)” task guide.</span></span> <span data-ttu-id="00918-107">Denne fremgangsmåten kan utføres i USMF-firmaet.</span><span class="sxs-lookup"><span data-stu-id="00918-107">These steps can be performed in ‘USMF’ company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="00918-108">Kjøre format med tilordning av opprinnelig modell</span><span class="sxs-lookup"><span data-stu-id="00918-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="00918-109">Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="00918-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="00918-110">Bruk hurtigfilteret til å filtrere på Bankkonto-feltet med en verdi lik USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="00918-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="00918-111">Klikk Oppsett i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="00918-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="00918-112">Klikk Kontroller.</span><span class="sxs-lookup"><span data-stu-id="00918-112">Click Check.</span></span>
5. <span data-ttu-id="00918-113">Klikk Skriv ut test.</span><span class="sxs-lookup"><span data-stu-id="00918-113">Click Print test.</span></span>
    * <span data-ttu-id="00918-114">Kjør formatet for testformål.</span><span class="sxs-lookup"><span data-stu-id="00918-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="00918-115">Velg Ja i feltet Sjekkformat som kan forhandles.</span><span class="sxs-lookup"><span data-stu-id="00918-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="00918-116">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="00918-116">Click OK.</span></span>
    * <span data-ttu-id="00918-117">Se gjennom de opprettede utdataene.</span><span class="sxs-lookup"><span data-stu-id="00918-117">Review the created output.</span></span> <span data-ttu-id="00918-118">Legg merke til at firmalogoen skal vises i rapporten, i tillegg til autoriserte personens signatur.</span><span class="sxs-lookup"><span data-stu-id="00918-118">Note that the company logo is presented in the report as well as the authorized person’s signature.</span></span> <span data-ttu-id="00918-119">Signaturbilde av hentes fra feltet av typen "Beholder" for Sjekk oppsett posten som er tilknyttet den valgte bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="00918-119">The signature image is taken from the field of the ‘Container’ data type of the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="00918-120">Utvid Kopier-seksjonen.</span><span class="sxs-lookup"><span data-stu-id="00918-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="00918-121">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="00918-121">Click Edit.</span></span>
10. <span data-ttu-id="00918-122">Angi "Skriv ut vannmerke som Annuller" i feltet Vannmerker.</span><span class="sxs-lookup"><span data-stu-id="00918-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="00918-123">Endre innstillingen vannmerker oppsett til å vise vannmerketeksten i dokumentgenerering i et Excel-figur-element.</span><span class="sxs-lookup"><span data-stu-id="00918-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="00918-124">Klikk Skriv ut test.</span><span class="sxs-lookup"><span data-stu-id="00918-124">Click Print test.</span></span>
12. <span data-ttu-id="00918-125">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="00918-125">Click OK.</span></span>
    * <span data-ttu-id="00918-126">Se gjennom de opprettede utdataene.</span><span class="sxs-lookup"><span data-stu-id="00918-126">Review the created output.</span></span> <span data-ttu-id="00918-127">Legg merke til at vannmerket vises i rapporten er opprettet i henhold til alternativet merket område.</span><span class="sxs-lookup"><span data-stu-id="00918-127">Note that the watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="00918-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="00918-128">Close the page.</span></span>
14. <span data-ttu-id="00918-129">Klikk Administrer betalinger i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="00918-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="00918-130">Klikk Kontroller.</span><span class="sxs-lookup"><span data-stu-id="00918-130">Click Checks.</span></span>
16. <span data-ttu-id="00918-131">Klikk Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="00918-131">Click Show filters.</span></span>
17. <span data-ttu-id="00918-132">Bruk følgende filtre: Angi en filterverdi på "381","385","389" i feltet "Sjekknummer" ved hjelp av filteroperatoren "er en av".</span><span class="sxs-lookup"><span data-stu-id="00918-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="00918-133">Merk alle rader i listen.</span><span class="sxs-lookup"><span data-stu-id="00918-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="00918-134">Klikk Skriv ut kopi av sjekk.</span><span class="sxs-lookup"><span data-stu-id="00918-134">Click Print check copy.</span></span>
    * <span data-ttu-id="00918-135">Kjør formatet for å skrive ut de valgte sjekkene.</span><span class="sxs-lookup"><span data-stu-id="00918-135">Run the format to re-print the selected cheques.</span></span>  
    * <span data-ttu-id="00918-136">Se gjennom de opprettede utdataene.</span><span class="sxs-lookup"><span data-stu-id="00918-136">Review the created output.</span></span> <span data-ttu-id="00918-137">Legg merke til at de valgte sjekkene er skrevet ut på nytt.</span><span class="sxs-lookup"><span data-stu-id="00918-137">Note that the selected cheques have been re-printed.</span></span> <span data-ttu-id="00918-138">Firmalogoen og etiketter skrives ikke etter at de vises i fortrykte skjemaet.</span><span class="sxs-lookup"><span data-stu-id="00918-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="00918-139">Endre tilordningen av den importerte datamodellen</span><span class="sxs-lookup"><span data-stu-id="00918-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="00918-140">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="00918-140">Close the page.</span></span>
2. <span data-ttu-id="00918-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="00918-141">Close the page.</span></span>
3. <span data-ttu-id="00918-142">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="00918-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="00918-143">Velg Modell for sjekker i treet.</span><span class="sxs-lookup"><span data-stu-id="00918-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="00918-144">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="00918-144">Click Designer.</span></span>
6. <span data-ttu-id="00918-145">Klikk Tilordne modell til datakilde.</span><span class="sxs-lookup"><span data-stu-id="00918-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="00918-146">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="00918-146">Click Designer.</span></span>
    * <span data-ttu-id="00918-147">Vi vil endre bindingen av-datamodellen signatur vare for å få signaturen bildet fra filen som er knyttet til posten sjekk oppsett som er tilknyttet den valgte bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="00918-147">We will change the binding of the data model’s signature item to get the signature image from the file that has been attached to the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="00918-148">Deaktiver Vis detaljer.</span><span class="sxs-lookup"><span data-stu-id="00918-148">Turn Show details off.</span></span>
9. <span data-ttu-id="00918-149">Utvid "oppsett" i treet.</span><span class="sxs-lookup"><span data-stu-id="00918-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="00918-150">Utvid "oppsett\signatur" i treet.</span><span class="sxs-lookup"><span data-stu-id="00918-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="00918-151">I treet velger du 'oppsett\signature\bilde = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span><span class="sxs-lookup"><span data-stu-id="00918-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="00918-152">Vis 'chequesaccount' i treet.</span><span class="sxs-lookup"><span data-stu-id="00918-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="00918-153">Utvid 'chequesaccount\<Relations' i treet.</span><span class="sxs-lookup"><span data-stu-id="00918-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="00918-154">Utvid 'chequesaccount\<RelationsBankChequeLayout' i treet.</span><span class="sxs-lookup"><span data-stu-id="00918-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="00918-155">Utvid 'chequesaccount\<RelationsBankChequeLayout\<Relations' i treet.</span><span class="sxs-lookup"><span data-stu-id="00918-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="00918-156">Utvid 'chequesaccount\<RelationsBankChequeLayout\<Relations\<Documents' i treet.</span><span class="sxs-lookup"><span data-stu-id="00918-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="00918-157">Velg 'chequesaccount\<RelationsBankChequeLayout\<Relations\<DocumentsgetFileContentAsContainer()' i treet.</span><span class="sxs-lookup"><span data-stu-id="00918-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="00918-158">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="00918-158">Click Bind.</span></span>
19. <span data-ttu-id="00918-159">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="00918-159">Click Save.</span></span>
20. <span data-ttu-id="00918-160">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="00918-160">Close the page.</span></span>
21. <span data-ttu-id="00918-161">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="00918-161">Close the page.</span></span>
22. <span data-ttu-id="00918-162">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="00918-162">Close the page.</span></span>
23. <span data-ttu-id="00918-163">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="00918-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="00918-164">Kjøre format ved hjelp av justert modelltilordning</span><span class="sxs-lookup"><span data-stu-id="00918-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="00918-165">Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="00918-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="00918-166">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="00918-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="00918-167">Du kan for eksempel filtrere på Bankkonto-feltet med verdien 'USMF OPER'.</span><span class="sxs-lookup"><span data-stu-id="00918-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="00918-168">Klikk Oppsett i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="00918-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="00918-169">Klikk Kontroller.</span><span class="sxs-lookup"><span data-stu-id="00918-169">Click Check.</span></span>
5. <span data-ttu-id="00918-170">Klikk Skriv ut test.</span><span class="sxs-lookup"><span data-stu-id="00918-170">Click Print test.</span></span>
6. <span data-ttu-id="00918-171">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="00918-171">Click OK.</span></span>
    * <span data-ttu-id="00918-172">Se gjennom de opprettede utdataene.</span><span class="sxs-lookup"><span data-stu-id="00918-172">Review the created output.</span></span> <span data-ttu-id="00918-173">Legg merke til at bildet fra dokumentbehandling vedlegget vises som signaturen for en autorisert person.</span><span class="sxs-lookup"><span data-stu-id="00918-173">Note that the image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="00918-174">Bruk Microsoft Word-dokument som en mal i det importerte formatet</span><span class="sxs-lookup"><span data-stu-id="00918-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="00918-175">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="00918-175">Close the page.</span></span>
2. <span data-ttu-id="00918-176">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="00918-176">Close the page.</span></span>
3. <span data-ttu-id="00918-177">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="00918-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="00918-178">Utvid Modell for sjekker i treet.</span><span class="sxs-lookup"><span data-stu-id="00918-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="00918-179">Velg 'Modell for sjekker\Utskriftsformat for sjekker' i treet.</span><span class="sxs-lookup"><span data-stu-id="00918-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="00918-180">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="00918-180">Click Designer.</span></span>
7. <span data-ttu-id="00918-181">Klikk Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="00918-181">Click Attachments.</span></span>
8. <span data-ttu-id="00918-182">Klikk Slett.</span><span class="sxs-lookup"><span data-stu-id="00918-182">Click Delete.</span></span>
9. <span data-ttu-id="00918-183">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="00918-183">Click Yes.</span></span>
10. <span data-ttu-id="00918-184">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="00918-184">Click New.</span></span>
11. <span data-ttu-id="00918-185">Klikk Fil.</span><span class="sxs-lookup"><span data-stu-id="00918-185">Click File.</span></span>
    * <span data-ttu-id="00918-186">Klikk Bla gjennom og velg den nedlastede på forhånd "sjekk Word.docx-malfil.</span><span class="sxs-lookup"><span data-stu-id="00918-186">Click Browse and select the downloaded in advance ‘Cheque template Word.docx’ file.</span></span>  
12. <span data-ttu-id="00918-187">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="00918-187">Close the page.</span></span>
13. <span data-ttu-id="00918-188">Angi eller velg en verdi i feltet Mal.</span><span class="sxs-lookup"><span data-stu-id="00918-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="00918-189">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="00918-189">Click Save.</span></span>
15. <span data-ttu-id="00918-190">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="00918-190">Close the page.</span></span>
16. <span data-ttu-id="00918-191">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="00918-191">Click Edit.</span></span>
17. <span data-ttu-id="00918-192">Velg Ja i feltet Kjøringsutkast.</span><span class="sxs-lookup"><span data-stu-id="00918-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="00918-193">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="00918-193">Close the page.</span></span>
19. <span data-ttu-id="00918-194">Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="00918-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="00918-195">Bruk hurtigfilteret til å filtrere på Bankkonto-feltet med en verdi lik USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="00918-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="00918-196">Klikk Kontroller.</span><span class="sxs-lookup"><span data-stu-id="00918-196">Click Check.</span></span>
22. <span data-ttu-id="00918-197">Klikk Skriv ut test.</span><span class="sxs-lookup"><span data-stu-id="00918-197">Click Print test.</span></span>
23. <span data-ttu-id="00918-198">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="00918-198">Click OK.</span></span>
    * <span data-ttu-id="00918-199">Se gjennom de opprettede utdataene.</span><span class="sxs-lookup"><span data-stu-id="00918-199">Review the created output.</span></span> <span data-ttu-id="00918-200">Legg merke til at utdataene er generert som et Microsoft Word-dokument med innebygde bilder presenterer firmalogoen, signaturen til en autorisert person og den merkede teksten til vannmerket.</span><span class="sxs-lookup"><span data-stu-id="00918-200">Note that the output has been generated as a MS Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  


