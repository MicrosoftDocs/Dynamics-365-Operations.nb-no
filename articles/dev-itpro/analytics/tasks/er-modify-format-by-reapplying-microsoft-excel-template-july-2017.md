---
title: Endre formater ved å bruke Excel-maler på nytt
description: For å fullføre trinnene i denne prosedyren må du først fullføre trinnene i prosedyren "ER Utforme en konfigurasjon for generering av rapporter i OPENXML-format".
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d5752caba9327475bb28c7bc6b0ee7e072f44f3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551167"
---
# <a name="modify-formats-by-reapplying-excel-templates"></a><span data-ttu-id="0680e-103">Endre formater ved å bruke Excel-maler på nytt</span><span class="sxs-lookup"><span data-stu-id="0680e-103">Modify formats by reapplying Excel templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0680e-104">For å fullføre trinnene i denne prosedyren må du først fullføre trinnene i prosedyren "ER Utforme en konfigurasjon for generering av rapporter i OPENXML-format".</span><span class="sxs-lookup"><span data-stu-id="0680e-104">To complete the steps in this procedure, you must first complete the procedure, ER - Design a configuration for generating reports in OPENXML format.</span></span>

<span data-ttu-id="0680e-105">Denne fremgangsmåten beskriver hvordan du endrer en elektronisk rapportering (ER)-formatkonfigurasjonen ved å utføre en Microsoft Excel-mal som er endret.</span><span class="sxs-lookup"><span data-stu-id="0680e-105">This procedure explains how to modify an Electronic reporting (ER) format configuration by reapplying a Microsoft Excel template that has been modified.</span></span> <span data-ttu-id="0680e-106">I denne prosedyren må du importere en endret Excel-mal til ER formatet konfigurasjonene som er opprettet for eksempel firmaer, Litware, Inc, og deretter generere elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="0680e-106">In this procedure, you will import a modified Excel template into ER format configurations that have been created for the sample company, Litware, Inc., and then generate electronic documents.</span></span> <span data-ttu-id="0680e-107">Denne fremgangsmåten er ment for brukere som har den systemansvarlige eller elektronisk rapportering utvikler-rolle.</span><span class="sxs-lookup"><span data-stu-id="0680e-107">This procedure is intended for users who have the system administrator or electronic reporting developer role.</span></span> <span data-ttu-id="0680e-108">Disse trinnene kan fullføres ved hjelp av GBSI-datasettet.</span><span class="sxs-lookup"><span data-stu-id="0680e-108">These steps can be completed by using the GBSI dataset.</span></span> <span data-ttu-id="0680e-109">Før du begynner, last ned og lagre filen, SampleVendPaymWsReport2.xlsx, som er oppført i Hjelpemnet. Modifiser elektronisk rapporteringsformat ved å gjenta en Excel-mal (modify-electronic-reporting-format-reapply-excel-template/).</span><span class="sxs-lookup"><span data-stu-id="0680e-109">Before you begin, download and save the file, SampleVendPaymWsReport2.xlsx, which is listed in the Help topic, Modify Electronic reporting format by reapplying an Excel template (modify-electronic-reporting-format-reapply-excel-template/).</span></span>

1. <span data-ttu-id="0680e-110">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="0680e-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="0680e-111">Kontroller at konfigurasjonsleverandøren for eksempelfirmaet "Litware, Inc." er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="0680e-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="0680e-112">Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="0680e-112">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  

## <a name="select-the-er-format"></a><span data-ttu-id="0680e-113">Velg ER-formatet</span><span class="sxs-lookup"><span data-stu-id="0680e-113">Select the ER format</span></span>
1. <span data-ttu-id="0680e-114">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="0680e-114">Click Reporting configurations.</span></span>
2. <span data-ttu-id="0680e-115">Utvid Betalingsmodell i treet.</span><span class="sxs-lookup"><span data-stu-id="0680e-115">In the tree, expand 'Payment model'.</span></span>
3. <span data-ttu-id="0680e-116">Velg Betalingsmodell\Regnearkeksempelrapport i treet.</span><span class="sxs-lookup"><span data-stu-id="0680e-116">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
4. <span data-ttu-id="0680e-117">Klikk Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="0680e-117">Click Attachments.</span></span>
    * <span data-ttu-id="0680e-118">Legg merke til at SampleVendPaymWsReport.xlsx Excel-filen blir brukt som en mal for betalingsbehandling for journalen.</span><span class="sxs-lookup"><span data-stu-id="0680e-118">Note that the SampleVendPaymWsReport.xlsx Excel file is currently used as a template for payment journal processing.</span></span>   
5. <span data-ttu-id="0680e-119">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="0680e-119">Click Open.</span></span>
    * <span data-ttu-id="0680e-120">Klikk Åpne for å utforske oppsettet for Excel-malen.</span><span class="sxs-lookup"><span data-stu-id="0680e-120">Click Open to explore the layout of the Excel template.</span></span>  
    * <span data-ttu-id="0680e-121">Gå gjennom malen.</span><span class="sxs-lookup"><span data-stu-id="0680e-121">Review the template.</span></span> <span data-ttu-id="0680e-122">Legg merke til at den for øyeblikket inneholder følgende detaljer for hver betalingslinje: leverandørens kontonummer, leverandørnavn, bank, rutingdnummer, kontonummer, debet, kredit og valuta.</span><span class="sxs-lookup"><span data-stu-id="0680e-122">Note that it currently includes the following details for each payment line: vendor account number, vendor name, bank, routing number, account number, debit, credit, and currency.</span></span> <span data-ttu-id="0680e-123">I dette eksemplet ønsker vi å utvide listen ved å legge til detaljer om betaling.</span><span class="sxs-lookup"><span data-stu-id="0680e-123">For this example, we want to extend this list by adding details about the payment date.</span></span>   
6. <span data-ttu-id="0680e-124">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0680e-124">Close the page.</span></span>

## <a name="reapply-a-new-excel-template-to-er-format"></a><span data-ttu-id="0680e-125">Bruk en ny Excel-mal på ER-formatet på nytt</span><span class="sxs-lookup"><span data-stu-id="0680e-125">Reapply a new Excel template to ER format</span></span>
1. <span data-ttu-id="0680e-126">Klikk Utforming.</span><span class="sxs-lookup"><span data-stu-id="0680e-126">Click Designer.</span></span>
    * <span data-ttu-id="0680e-127">Åpne utkastversjonen av det valgte ER formatet for redigering.</span><span class="sxs-lookup"><span data-stu-id="0680e-127">Open the draft version of the selected ER format for editing.</span></span>  
2. <span data-ttu-id="0680e-128">Klikk Import i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="0680e-128">On the Action Pane, click Import.</span></span>
3. <span data-ttu-id="0680e-129">Klikk Oppdater fra Excel.</span><span class="sxs-lookup"><span data-stu-id="0680e-129">Click Update from Excel.</span></span>
    * <span data-ttu-id="0680e-130">Klikk "Oppdater mal", og velg deretter filen SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="0680e-130">Click ‘Update template’, and then select the file, SampleVendPaymWsReport2.xlsx.</span></span>  
    * <span data-ttu-id="0680e-131">Klikk Oppdater mal, og bla gjennom for å få den nedlastede tidligere SampleVendPaymWsReport2.xlsx-filen.</span><span class="sxs-lookup"><span data-stu-id="0680e-131">Click Update template and browse to get the downloaded earlier SampleVendPaymWsReport2.xlsx file.</span></span>  
4. <span data-ttu-id="0680e-132">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0680e-132">Click OK.</span></span>
    * <span data-ttu-id="0680e-133">SampleVendPaymWsReport2.xlsx malen brukes.</span><span class="sxs-lookup"><span data-stu-id="0680e-133">The SampleVendPaymWsReport2.xlsx template is applied.</span></span> <span data-ttu-id="0680e-134">Strukturen i Er-formatet synkroniseres med innholdet i malen, der elementene blir lagt til ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="0680e-134">The structure of the ER format is synchronized with the content of the template, whose elements are added to the ER format.</span></span> <span data-ttu-id="0680e-135">Alle elementer i ER-formatet som ikke er inkludert i malen, blir fjernet fra formatdefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="0680e-135">Any existing elements in the ER format that aren’t included in the template are removed from the format definition.</span></span>  
5. <span data-ttu-id="0680e-136">Velg 'Excel' i treet.</span><span class="sxs-lookup"><span data-stu-id="0680e-136">In the tree, select 'Excel'.</span></span>
    * <span data-ttu-id="0680e-137">Legg merke til at Mal-feltet nå inneholder en referanse til den nye malen.</span><span class="sxs-lookup"><span data-stu-id="0680e-137">Note that the Template field now contains a reference to the new template.</span></span>   
6. <span data-ttu-id="0680e-138">Klikk Vedlegg.</span><span class="sxs-lookup"><span data-stu-id="0680e-138">Click Attachments.</span></span>
7. <span data-ttu-id="0680e-139">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="0680e-139">Click Open.</span></span>
    * <span data-ttu-id="0680e-140">Klikk Åpne for å utforske oppsettet for den modifiserte Excel-malen.</span><span class="sxs-lookup"><span data-stu-id="0680e-140">Click Open to explore the layout of the modified Excel template.</span></span>  
    * <span data-ttu-id="0680e-141">Gå gjennom malen.</span><span class="sxs-lookup"><span data-stu-id="0680e-141">Review the template.</span></span> <span data-ttu-id="0680e-142">Legg merke til at teksten nå inneholder en linje for betalingsdato.</span><span class="sxs-lookup"><span data-stu-id="0680e-142">Note that it now contains a line for the payment date.</span></span>   
8. <span data-ttu-id="0680e-143">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0680e-143">Close the page.</span></span>
9. <span data-ttu-id="0680e-144">Utvid 'Excel' i treet.</span><span class="sxs-lookup"><span data-stu-id="0680e-144">In the tree, expand 'Excel'.</span></span>
10. <span data-ttu-id="0680e-145">Vis Excel\PaymLines i treet.</span><span class="sxs-lookup"><span data-stu-id="0680e-145">In the tree, expand 'Excel\PaymLines'.</span></span>
11. <span data-ttu-id="0680e-146">Velg 'Excel\PaymLines\PaymDate' i treet.</span><span class="sxs-lookup"><span data-stu-id="0680e-146">In the tree, select 'Excel\PaymLines\PaymDate'.</span></span>
    * <span data-ttu-id="0680e-147">Legg merke til at ER-formatet nå inneholder ett element til.</span><span class="sxs-lookup"><span data-stu-id="0680e-147">Note that the ER format now contains one more item.</span></span> <span data-ttu-id="0680e-148">En celle, PaymDate, er lagt til Excel-malen.</span><span class="sxs-lookup"><span data-stu-id="0680e-148">A cell, PaymDate, has been added to the Excel template.</span></span>  
12. <span data-ttu-id="0680e-149">Klikk kategorien Tilordning.</span><span class="sxs-lookup"><span data-stu-id="0680e-149">Click the Mapping tab.</span></span>
13. <span data-ttu-id="0680e-150">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="0680e-150">In the tree, expand 'model'.</span></span>
14. <span data-ttu-id="0680e-151">Utvid modell\Betalinger i treet.</span><span class="sxs-lookup"><span data-stu-id="0680e-151">In the tree, expand 'model\Payments'.</span></span>
15. <span data-ttu-id="0680e-152">I treet velger du modell\Betalinger\Transaksjonsdato(TransactionDate).</span><span class="sxs-lookup"><span data-stu-id="0680e-152">In the tree, select 'model\Payments\Transaction date(TransactionDate)'.</span></span>
16. <span data-ttu-id="0680e-153">Klikk Bind.</span><span class="sxs-lookup"><span data-stu-id="0680e-153">Click Bind.</span></span>
    * <span data-ttu-id="0680e-154">Angi hvilke data som legges til den nye cellen under kjøring.</span><span class="sxs-lookup"><span data-stu-id="0680e-154">Specify what data is added to the new cell at runtime.</span></span>  
17. <span data-ttu-id="0680e-155">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="0680e-155">Click Save.</span></span>
18. <span data-ttu-id="0680e-156">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0680e-156">Close the page.</span></span>

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a><span data-ttu-id="0680e-157">Aktiver den endrede utkastversjonen av ER-formatet for bruk i journalen for betalingsbehandling</span><span class="sxs-lookup"><span data-stu-id="0680e-157">Enable the modified draft version of the ER format for use in payment journal processing</span></span>
1. <span data-ttu-id="0680e-158">Klikk Konfigurasjoner i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="0680e-158">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="0680e-159">Klikk Brukerparametere.</span><span class="sxs-lookup"><span data-stu-id="0680e-159">Click User parameters.</span></span>
3. <span data-ttu-id="0680e-160">Velg Ja i feltet Kjøringsinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="0680e-160">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="0680e-161">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="0680e-161">Click OK.</span></span>
5. <span data-ttu-id="0680e-162">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="0680e-162">Click Edit.</span></span>
6. <span data-ttu-id="0680e-163">Velg Ja i feltet Kjøringsutkast.</span><span class="sxs-lookup"><span data-stu-id="0680e-163">Select Yes in the Run Draft field.</span></span>

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a><span data-ttu-id="0680e-164">Bruk den endrede utkastversjonen av ER-formatet i journalen for betalingsbehandling</span><span class="sxs-lookup"><span data-stu-id="0680e-164">Use the modified draft version of the ER format for payment journal processing</span></span>
    * <span data-ttu-id="0680e-165">Gå gjennom det opprettede regnearket, inkludert nye detaljer over betalingslinjer – betalingsdato.</span><span class="sxs-lookup"><span data-stu-id="0680e-165">Review the created worksheet, including new detail of payment lines – payment date.</span></span>  

