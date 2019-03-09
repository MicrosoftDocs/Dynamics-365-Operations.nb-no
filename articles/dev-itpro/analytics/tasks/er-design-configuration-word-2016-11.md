---
title: Utforme ER-konfigurasjoner for å generere rapporter i Word-format
description: De følgende trinnene forklarer hvordan en bruker med rollen systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapporteringsformat til å generere rapporter som Microsoft Word-filer.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc47d44285af4c720d2f450d11fb1004ef461d0f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "362355"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a><span data-ttu-id="5e082-103">Utforme ER-konfigurasjoner for å generere rapporter i Word-format</span><span class="sxs-lookup"><span data-stu-id="5e082-103">Design ER configurations to generate reports in Word format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5e082-104">De følgende trinnene forklarer hvordan en bruker med rollen systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapporteringsformat (ER) til å generere rapporter som Microsoft Word-filer.</span><span class="sxs-lookup"><span data-stu-id="5e082-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="5e082-105">Denne fremgangsmåten kan utføres i firmaet GBSI.</span><span class="sxs-lookup"><span data-stu-id="5e082-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="5e082-106">For å fullføre disse trinnene må du først fullføre trinnene i oppgaveveiledningen "Opprette en ER-konfigurasjon for generering av rapporter i OPENXML-format".</span><span class="sxs-lookup"><span data-stu-id="5e082-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="5e082-107">På forhånd, må du også laste ned og lagre følgende maler lokalt, for eksempelrapporten:</span><span class="sxs-lookup"><span data-stu-id="5e082-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

- [<span data-ttu-id="5e082-108">Mal for betalingsrapport</span><span class="sxs-lookup"><span data-stu-id="5e082-108">Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="5e082-109">Bundet mal for betalingsrapport</span><span class="sxs-lookup"><span data-stu-id="5e082-109">Bounded Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)


<span data-ttu-id="5e082-110">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Microsoft Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="5e082-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="5e082-111">Velg den eksisterende ER-rapportkonfigurasjonen</span><span class="sxs-lookup"><span data-stu-id="5e082-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="5e082-112">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="5e082-112">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="5e082-113">Kontroller at konfigurasjonsleverandøren Litware, Inc</span><span class="sxs-lookup"><span data-stu-id="5e082-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="5e082-114">er merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="5e082-114">is selected as active.</span></span>  
2. <span data-ttu-id="5e082-115">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="5e082-115">Click Reporting configurations.</span></span>
    * <span data-ttu-id="5e082-116">Vi vil bruke den eksisterende ER-konfigurasjonen som er opprinnelig utformet for å generere rapportutdataene i OPENXML-formatet, på nytt.</span><span class="sxs-lookup"><span data-stu-id="5e082-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="5e082-117">Utvid Betalingsmodell i treet.</span><span class="sxs-lookup"><span data-stu-id="5e082-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="5e082-118">Velg Betalingsmodell\Regnearkeksempelrapport i treet.</span><span class="sxs-lookup"><span data-stu-id="5e082-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="5e082-119">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="5e082-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="5e082-120">Erstatt Excel-malen med Word-malen</span><span class="sxs-lookup"><span data-stu-id="5e082-120">Replace the Excel template with the Word template</span></span>
    * <span data-ttu-id="5e082-121">For øyeblikket brukes Excel-dokumentet som en mal til å generere utdataene i OPENXML-format.</span><span class="sxs-lookup"><span data-stu-id="5e082-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="5e082-122">Vi vil importere rapportens mal i Word-format.</span><span class="sxs-lookup"><span data-stu-id="5e082-122">We will import the report’s template in Word format.</span></span>  
1. <span data-ttu-id="5e082-123">Klikk Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="5e082-123">Click Attachments.</span></span>
    * <span data-ttu-id="5e082-124">Erstatt den eksisterende Excel-malen med Word-malen som du lastet ned tidligere, SampleVendPaymDocReport.docx.</span><span class="sxs-lookup"><span data-stu-id="5e082-124">Replace the existing Excel template with the Word template that you downloaded earlier, SampleVendPaymDocReport.docx.</span></span> <span data-ttu-id="5e082-125">Legg merke til at denne malen bare inneholder oppsettet for dokumentet vi vil generere som ER-utdata.</span><span class="sxs-lookup"><span data-stu-id="5e082-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="5e082-126">Klikk Slett.</span><span class="sxs-lookup"><span data-stu-id="5e082-126">Click Delete.</span></span>
3. <span data-ttu-id="5e082-127">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="5e082-127">Click Yes.</span></span>
4. <span data-ttu-id="5e082-128">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5e082-128">Click New.</span></span>
5. <span data-ttu-id="5e082-129">Klikk Fil.</span><span class="sxs-lookup"><span data-stu-id="5e082-129">Click File.</span></span>
6. <span data-ttu-id="5e082-130">Klikk Bla gjennom.</span><span class="sxs-lookup"><span data-stu-id="5e082-130">Click Browse.</span></span> <span data-ttu-id="5e082-131">Gå til og velg SampleVendPaymDocReport.docx som du lastet ned tidligere.</span><span class="sxs-lookup"><span data-stu-id="5e082-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="5e082-132">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5e082-132">Click OK.</span></span>
    * <span data-ttu-id="5e082-133">Velg malen du lastet ned i den forrige fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="5e082-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="5e082-134">Angi eller velg en verdi i feltet Mal.</span><span class="sxs-lookup"><span data-stu-id="5e082-134">In the Template field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="5e082-135">Utvid Word-malen ved å legge til en egendefinert XML-del</span><span class="sxs-lookup"><span data-stu-id="5e082-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="5e082-136">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5e082-136">Click Save.</span></span>
    * <span data-ttu-id="5e082-137">I tillegg til å lagre konfigurasjonsendringer, oppdaterer Lagre-handlingen den vedlagte Word-malen.</span><span class="sxs-lookup"><span data-stu-id="5e082-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="5e082-138">Strukturen til det utformede formatet er overført til det vedlagte Word-dokumentet som en ny egendefinert XML-del med navnet "Rapport".</span><span class="sxs-lookup"><span data-stu-id="5e082-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="5e082-139">Legg merke til at den tilknyttede Word-malen ikke bare inneholder oppsettet for dokumentet vi vil generere som ER-utdata, den inneholder også strukturen til dataene som ER fyller ut i denne malen under kjøring.</span><span class="sxs-lookup"><span data-stu-id="5e082-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="5e082-140">Klikk Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="5e082-140">Click Attachments.</span></span>
    * <span data-ttu-id="5e082-141">Nå må du binde elementene i den egendefinerte XML-delen "Rapport" til deler på Word-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="5e082-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    * <span data-ttu-id="5e082-142">Hvis du har kjennskap til Word-dokumenter som kan utformes som skjemaer som inneholder innholdskontroller som er avgrenset med elementer av egendefinerte XML-deler – spill av alle trinnene i den neste delaktiviteten for å opprette et slikt dokument.</span><span class="sxs-lookup"><span data-stu-id="5e082-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="5e082-143">Hvis du vil ha mer informasjon, følg koblingen https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span><span class="sxs-lookup"><span data-stu-id="5e082-143">For more details, see this link https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span></span> <span data-ttu-id="5e082-144">Hvis ikke hopper du over alle trinnene i den neste delaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="5e082-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="5e082-145">Få Word med egendefinert XML-delen for å utføre databindinger</span><span class="sxs-lookup"><span data-stu-id="5e082-145">Get Word with custom XML part to do data bindings</span></span>
    * <span data-ttu-id="5e082-146">Åpne dette dokumentet i Word, og gjør følgende: – Åpne fanen Word-utvikler (tilpass båndet hvis det ikke er aktivert ennå).</span><span class="sxs-lookup"><span data-stu-id="5e082-146">Open this document in Word and do the following:  - Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>  <span data-ttu-id="5e082-147">- Velg ruten XML-tilordning.</span><span class="sxs-lookup"><span data-stu-id="5e082-147">- Select XML mapping pane.</span></span>  <span data-ttu-id="5e082-148">- Velg den egendefinerte XML-delen "Rapport" i oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5e082-148">- Select the ‘Report’ custom XML part in the lookup.</span></span>  <span data-ttu-id="5e082-149">- Utfør tilordning av elementene i den valgte egendefinerte XML-delen og innholdskontrollene for Word-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="5e082-149">- Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="5e082-150">- Lagre det oppdaterte Word-dokumentet på en lokal stasjon.</span><span class="sxs-lookup"><span data-stu-id="5e082-150">- Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="5e082-151">Last opp Word-malen med egendefinert XML-del bundet til innholdskontroller</span><span class="sxs-lookup"><span data-stu-id="5e082-151">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="5e082-152">Klikk Slett.</span><span class="sxs-lookup"><span data-stu-id="5e082-152">Click Delete.</span></span>
2. <span data-ttu-id="5e082-153">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="5e082-153">Click Yes.</span></span>
    * <span data-ttu-id="5e082-154">Legg til ny mal.</span><span class="sxs-lookup"><span data-stu-id="5e082-154">Add a new template.</span></span> <span data-ttu-id="5e082-155">Hvis du har fullført trinnene i den forrige delaktiviteten, velger du Word-dokumentet du opprettet og lagret lokalt.</span><span class="sxs-lookup"><span data-stu-id="5e082-155">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="5e082-156">Ellers velger du Microsoft Word-malen SampleVendPaymDocReportBounded.docx som du lastet ned tidligere.</span><span class="sxs-lookup"><span data-stu-id="5e082-156">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="5e082-157">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5e082-157">Click New.</span></span>
4. <span data-ttu-id="5e082-158">Klikk Fil.</span><span class="sxs-lookup"><span data-stu-id="5e082-158">Click File.</span></span>
5. <span data-ttu-id="5e082-159">Klikk Bla gjennom.</span><span class="sxs-lookup"><span data-stu-id="5e082-159">Click Browse.</span></span> <span data-ttu-id="5e082-160">Gå til og velg SampleVendPaymDocReportBounded.docx som du lastet ned tidligere.</span><span class="sxs-lookup"><span data-stu-id="5e082-160">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="5e082-161">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5e082-161">Click OK.</span></span>
6. <span data-ttu-id="5e082-162">I Mal-feltet velger du dokumentet du lastet ned i den forrige fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="5e082-162">In the Template field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="5e082-163">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5e082-163">Click Save.</span></span>
8. <span data-ttu-id="5e082-164">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5e082-164">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="5e082-165">Kjør formatet for å opprette Word-utdata</span><span class="sxs-lookup"><span data-stu-id="5e082-165">Execute the format to create Word output</span></span>
1. <span data-ttu-id="5e082-166">Klikk Konfigurasjoner i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5e082-166">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="5e082-167">Klikk Brukerparametere.</span><span class="sxs-lookup"><span data-stu-id="5e082-167">Click User parameters.</span></span>
3. <span data-ttu-id="5e082-168">Velg Ja i feltet Kjøringsinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="5e082-168">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="5e082-169">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5e082-169">Click OK.</span></span>
5. <span data-ttu-id="5e082-170">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="5e082-170">Click Edit.</span></span>
6. <span data-ttu-id="5e082-171">Velg Ja i feltet Kjøringsutkast.</span><span class="sxs-lookup"><span data-stu-id="5e082-171">Select Yes in the Run Draft field.</span></span>
7. <span data-ttu-id="5e082-172">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5e082-172">Click Save.</span></span>
8. <span data-ttu-id="5e082-173">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5e082-173">Close the page.</span></span>
9. <span data-ttu-id="5e082-174">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5e082-174">Close the page.</span></span>
10. <span data-ttu-id="5e082-175">Gå til Leverandører > Betalinger > Betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="5e082-175">Go to Accounts payable > Payments > Payment journal.</span></span>
11. <span data-ttu-id="5e082-176">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="5e082-176">Click Lines.</span></span>
12. <span data-ttu-id="5e082-177">Merk eller fjern merking for alle rader i listen.</span><span class="sxs-lookup"><span data-stu-id="5e082-177">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="5e082-178">Klikk Betalingsstatus.</span><span class="sxs-lookup"><span data-stu-id="5e082-178">Click Payment status.</span></span>
14. <span data-ttu-id="5e082-179">Velg Ingen.</span><span class="sxs-lookup"><span data-stu-id="5e082-179">Click None.</span></span>
15. <span data-ttu-id="5e082-180">Klikk Generer betalinger.</span><span class="sxs-lookup"><span data-stu-id="5e082-180">Click Generate payments.</span></span>
16. <span data-ttu-id="5e082-181">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5e082-181">Click OK.</span></span>
17. <span data-ttu-id="5e082-182">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5e082-182">Click OK.</span></span>
    * <span data-ttu-id="5e082-183">Analyser de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="5e082-183">Analyze the generated output.</span></span> <span data-ttu-id="5e082-184">Legg merke til at de opprettede utdataene vises i Word-format og inneholder detaljer for de behandlede betalingene.</span><span class="sxs-lookup"><span data-stu-id="5e082-184">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  

