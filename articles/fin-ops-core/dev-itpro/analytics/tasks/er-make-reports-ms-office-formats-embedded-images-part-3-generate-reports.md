---
title: Generere rapporter i Office-formater som inneholder innebygde bilder
description: De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan designe konfigurasjoner for elektronisk rapportering (ER) for å generere elektroniske dokumenter i MS Office-formater (Excel og Word), som inneholder innebygde bilder.
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78dcdbd83dc717104d437662f7f451c9ecb714cf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684385"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="37754-103">Generere rapporter i Office-formater som inneholder innebygde bilder</span><span class="sxs-lookup"><span data-stu-id="37754-103">Generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="37754-104">De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan designe konfigurasjoner for elektronisk rapportering (ER) for å generere elektroniske dokumenter i MS Office-formater (Excel og Word), som inneholder innebygde bilder.</span><span class="sxs-lookup"><span data-stu-id="37754-104">The following steps explain how a user playing either 'System administrator' or 'Electronic reporting developer' role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="37754-105">I dette eksemplet skal du bruke opprettede ER-konfigurasjoner for eksempelfirmaet "Litware, Inc".</span><span class="sxs-lookup"><span data-stu-id="37754-105">In this example, you will use created ER configurations for sample company, 'Litware, Inc.'.</span></span>  <span data-ttu-id="37754-106">For å fullføre disse trinnene, må du først fullføre trinnene i oppgaveveiledningen "ER lage rapporter i MS Office-formater med innebygde bilder (del 2: se gjennom konfigurasjoner)".</span><span class="sxs-lookup"><span data-stu-id="37754-106">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)" task guide.</span></span> <span data-ttu-id="37754-107">Denne fremgangsmåten kan utføres i USMF-firmaet.</span><span class="sxs-lookup"><span data-stu-id="37754-107">These steps can be performed in 'USMF' company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="37754-108">Kjøre format med tilordning av opprinnelig modell</span><span class="sxs-lookup"><span data-stu-id="37754-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="37754-109">Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="37754-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="37754-110">Bruk hurtigfilteret til å filtrere på Bankkonto-feltet med en verdi lik USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="37754-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="37754-111">Klikk Oppsett i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="37754-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="37754-112">Klikk Kontroller.</span><span class="sxs-lookup"><span data-stu-id="37754-112">Click Check.</span></span>
5. <span data-ttu-id="37754-113">Klikk Skriv ut test.</span><span class="sxs-lookup"><span data-stu-id="37754-113">Click Print test.</span></span>
    * <span data-ttu-id="37754-114">Kjør formatet for testformål.</span><span class="sxs-lookup"><span data-stu-id="37754-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="37754-115">Velg Ja i feltet Sjekkformat som kan forhandles.</span><span class="sxs-lookup"><span data-stu-id="37754-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="37754-116">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="37754-116">Click OK.</span></span>
    * <span data-ttu-id="37754-117">Se gjennom de opprettede utdataene.</span><span class="sxs-lookup"><span data-stu-id="37754-117">Review the created output.</span></span> <span data-ttu-id="37754-118">Firmalogoen vises i rapporten, i tillegg til autoriserte personens signatur.</span><span class="sxs-lookup"><span data-stu-id="37754-118">The company logo is presented in the report as well as the authorized person's signature.</span></span> <span data-ttu-id="37754-119">Signaturbildet hentes fra feltet av typen "Beholder" for Sjekk oppsett-posten som er tilknyttet den valgte bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="37754-119">The signature image is taken from the field of the 'Container' data type of the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="37754-120">Utvid Kopier-seksjonen.</span><span class="sxs-lookup"><span data-stu-id="37754-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="37754-121">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="37754-121">Click Edit.</span></span>
10. <span data-ttu-id="37754-122">Angi "Skriv ut vannmerke som Annuller" i feltet Vannmerker.</span><span class="sxs-lookup"><span data-stu-id="37754-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="37754-123">Endre innstillingen vannmerker oppsett til å vise vannmerketeksten i dokumentgenerering i et Excel-figur-element.</span><span class="sxs-lookup"><span data-stu-id="37754-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="37754-124">Klikk Skriv ut test.</span><span class="sxs-lookup"><span data-stu-id="37754-124">Click Print test.</span></span>
12. <span data-ttu-id="37754-125">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="37754-125">Click OK.</span></span>
    * <span data-ttu-id="37754-126">Se gjennom de opprettede utdataene.</span><span class="sxs-lookup"><span data-stu-id="37754-126">Review the created output.</span></span> <span data-ttu-id="37754-127">Vannmerket vises i den opprettede rapporten i henhold til det valgte alternativet.</span><span class="sxs-lookup"><span data-stu-id="37754-127">The watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="37754-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="37754-128">Close the page.</span></span>
14. <span data-ttu-id="37754-129">Klikk Administrer betalinger i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="37754-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="37754-130">Klikk Kontroller.</span><span class="sxs-lookup"><span data-stu-id="37754-130">Click Checks.</span></span>
16. <span data-ttu-id="37754-131">Klikk Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="37754-131">Click Show filters.</span></span>
17. <span data-ttu-id="37754-132">Bruk følgende filtre: Angi en filterverdi på "381","385","389" i feltet "Sjekknummer" ved hjelp av filteroperatoren "er en av".</span><span class="sxs-lookup"><span data-stu-id="37754-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="37754-133">Merk alle rader i listen.</span><span class="sxs-lookup"><span data-stu-id="37754-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="37754-134">Klikk Skriv ut kopi av sjekk.</span><span class="sxs-lookup"><span data-stu-id="37754-134">Click Print check copy.</span></span>
    * <span data-ttu-id="37754-135">Kjør formatet for å skrive ut de valgte sjekkene på nytt.</span><span class="sxs-lookup"><span data-stu-id="37754-135">Run the format to reprint the selected cheques.</span></span>  
    * <span data-ttu-id="37754-136">Se gjennom de opprettede utdataene.</span><span class="sxs-lookup"><span data-stu-id="37754-136">Review the created output.</span></span> <span data-ttu-id="37754-137">De valgte sjekkene er skrevet ut på nytt.</span><span class="sxs-lookup"><span data-stu-id="37754-137">The selected cheques have been reprinted.</span></span> <span data-ttu-id="37754-138">Firmalogoen og etiketter skrives ikke etter at de vises i fortrykte skjemaet.</span><span class="sxs-lookup"><span data-stu-id="37754-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="37754-139">Endre tilordningen av den importerte datamodellen</span><span class="sxs-lookup"><span data-stu-id="37754-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="37754-140">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="37754-140">Close the page.</span></span>
2. <span data-ttu-id="37754-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="37754-141">Close the page.</span></span>
3. <span data-ttu-id="37754-142">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="37754-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="37754-143">Velg Modell for sjekker i treet.</span><span class="sxs-lookup"><span data-stu-id="37754-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="37754-144">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="37754-144">Click Designer.</span></span>
6. <span data-ttu-id="37754-145">Klikk Tilordne modell til datakilde.</span><span class="sxs-lookup"><span data-stu-id="37754-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="37754-146">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="37754-146">Click Designer.</span></span>
    * <span data-ttu-id="37754-147">Vi vil endre bindingen av datamodellens signaturelement for å få signaturbildet fra filen som er knyttet til posten Sjekk oppsett som er tilknyttet den valgte bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="37754-147">We will change the binding of the data model's signature item to get the signature image from the file that has been attached to the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="37754-148">Deaktiver Vis detaljer.</span><span class="sxs-lookup"><span data-stu-id="37754-148">Turn off Show details.</span></span>
9. <span data-ttu-id="37754-149">Utvid "oppsett" i treet.</span><span class="sxs-lookup"><span data-stu-id="37754-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="37754-150">Utvid "oppsett\signatur" i treet.</span><span class="sxs-lookup"><span data-stu-id="37754-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="37754-151">I treet velger du 'oppsett\signature\bilde = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span><span class="sxs-lookup"><span data-stu-id="37754-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="37754-152">Vis 'chequesaccount' i treet.</span><span class="sxs-lookup"><span data-stu-id="37754-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="37754-153">Utvid 'chequesaccount\<Relations' i treet.</span><span class="sxs-lookup"><span data-stu-id="37754-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="37754-154">Utvid 'chequesaccount\<RelationsBankChequeLayout' i treet.</span><span class="sxs-lookup"><span data-stu-id="37754-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="37754-155">Utvid 'chequesaccount\<RelationsBankChequeLayout\<Relations' i treet.</span><span class="sxs-lookup"><span data-stu-id="37754-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="37754-156">Utvid 'chequesaccount\<RelationsBankChequeLayout\<Relations\<Documents' i treet.</span><span class="sxs-lookup"><span data-stu-id="37754-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="37754-157">Velg 'chequesaccount\<RelationsBankChequeLayout\<Relations\<DocumentsgetFileContentAsContainer()' i treet.</span><span class="sxs-lookup"><span data-stu-id="37754-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="37754-158">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="37754-158">Click Bind.</span></span>
19. <span data-ttu-id="37754-159">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="37754-159">Click Save.</span></span>
20. <span data-ttu-id="37754-160">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="37754-160">Close the page.</span></span>
21. <span data-ttu-id="37754-161">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="37754-161">Close the page.</span></span>
22. <span data-ttu-id="37754-162">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="37754-162">Close the page.</span></span>
23. <span data-ttu-id="37754-163">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="37754-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="37754-164">Kjøre format ved hjelp av justert modelltilordning</span><span class="sxs-lookup"><span data-stu-id="37754-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="37754-165">Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="37754-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="37754-166">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="37754-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="37754-167">Du kan for eksempel filtrere på Bankkonto-feltet med verdien 'USMF OPER'.</span><span class="sxs-lookup"><span data-stu-id="37754-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="37754-168">Klikk Oppsett i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="37754-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="37754-169">Klikk Kontroller.</span><span class="sxs-lookup"><span data-stu-id="37754-169">Click Check.</span></span>
5. <span data-ttu-id="37754-170">Klikk Skriv ut test.</span><span class="sxs-lookup"><span data-stu-id="37754-170">Click Print test.</span></span>
6. <span data-ttu-id="37754-171">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="37754-171">Click OK.</span></span>
    * <span data-ttu-id="37754-172">Se gjennom de opprettede utdataene.</span><span class="sxs-lookup"><span data-stu-id="37754-172">Review the created output.</span></span> <span data-ttu-id="37754-173">Bildet fra dokumentbehandlingsvedlegget vises som signaturen til en autorisert person.</span><span class="sxs-lookup"><span data-stu-id="37754-173">The image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="37754-174">Bruk MS Word-dokument som en mal i det importerte formatet</span><span class="sxs-lookup"><span data-stu-id="37754-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="37754-175">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="37754-175">Close the page.</span></span>
2. <span data-ttu-id="37754-176">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="37754-176">Close the page.</span></span>
3. <span data-ttu-id="37754-177">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="37754-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="37754-178">Utvid Modell for sjekker i treet.</span><span class="sxs-lookup"><span data-stu-id="37754-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="37754-179">Velg 'Modell for sjekker\Utskriftsformat for sjekker' i treet.</span><span class="sxs-lookup"><span data-stu-id="37754-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="37754-180">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="37754-180">Click Designer.</span></span>
7. <span data-ttu-id="37754-181">Klikk Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="37754-181">Click Attachments.</span></span>
8. <span data-ttu-id="37754-182">Klikk Slett.</span><span class="sxs-lookup"><span data-stu-id="37754-182">Click Delete.</span></span>
9. <span data-ttu-id="37754-183">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="37754-183">Click Yes.</span></span>
10. <span data-ttu-id="37754-184">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="37754-184">Click New.</span></span>
11. <span data-ttu-id="37754-185">Klikk Fil.</span><span class="sxs-lookup"><span data-stu-id="37754-185">Click File.</span></span>
    * <span data-ttu-id="37754-186">Klikk Bla gjennom og velg den nedlastede på forhånd "Sjekk Word.docx-malfil.</span><span class="sxs-lookup"><span data-stu-id="37754-186">Click Browse and select the downloaded in advance 'Cheque template Word.docx' file.</span></span>  
12. <span data-ttu-id="37754-187">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="37754-187">Close the page.</span></span>
13. <span data-ttu-id="37754-188">Angi eller velg en verdi i feltet Mal.</span><span class="sxs-lookup"><span data-stu-id="37754-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="37754-189">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="37754-189">Click Save.</span></span>
15. <span data-ttu-id="37754-190">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="37754-190">Close the page.</span></span>
16. <span data-ttu-id="37754-191">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="37754-191">Click Edit.</span></span>
17. <span data-ttu-id="37754-192">Velg Ja i feltet Kjøringsutkast.</span><span class="sxs-lookup"><span data-stu-id="37754-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="37754-193">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="37754-193">Close the page.</span></span>
19. <span data-ttu-id="37754-194">Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="37754-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="37754-195">Bruk hurtigfilteret til å filtrere på Bankkonto-feltet med en verdi lik USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="37754-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="37754-196">Klikk Kontroller.</span><span class="sxs-lookup"><span data-stu-id="37754-196">Click Check.</span></span>
22. <span data-ttu-id="37754-197">Klikk Skriv ut test.</span><span class="sxs-lookup"><span data-stu-id="37754-197">Click Print test.</span></span>
23. <span data-ttu-id="37754-198">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="37754-198">Click OK.</span></span>
    * <span data-ttu-id="37754-199">Se gjennom de opprettede utdataene.</span><span class="sxs-lookup"><span data-stu-id="37754-199">Review the created output.</span></span> <span data-ttu-id="37754-200">Utdataene er generert som et Word-dokument med innebygde bilder som presenterer firmalogoen, signaturen til en autorisert person og den valgte teksten til vannmerket.</span><span class="sxs-lookup"><span data-stu-id="37754-200">The output has been generated as a Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  

