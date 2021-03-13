---
title: Bruke ER-konfigurasjoner på nytt med Excel-maler for å generere rapporter i Word-format
description: Dette emnet beskriver hvordan rapportformater som ble utformet for å generere rapporter som Excel-arbeidsbøker, kan konfigureres slik at de genererer rapporter som Word-dokumenter.
author: NickSelin
manager: AnnBe
ms.date: 01/11/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 769913fd0344eb276b3b1bd055255272ca5dfffd
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092722"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a><span data-ttu-id="dbe5b-103">Bruke ER-konfigurasjoner på nytt med Excel-maler for å generere rapporter i Word-format</span><span class="sxs-lookup"><span data-stu-id="dbe5b-103">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dbe5b-104">Hvis du vil generere rapporter som Microsoft Word-dokumenter, kan du [konfigurere](../er-design-configuration-word.md) et nytt [format](../general-electronic-reporting.md#FormatComponentOutbound) for [ER (Elektronisk rapportering)](../general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="dbe5b-104">To generate reports as Microsoft Word documents, you can [configure](../er-design-configuration-word.md) a new [Electronic reporting (ER)](../general-electronic-reporting.md) [format](../general-electronic-reporting.md#FormatComponentOutbound).</span></span> <span data-ttu-id="dbe5b-105">Du kan også bruke et ER-format på nytt som opprinnelig ble utformet for å generere rapporter som Excel-arbeidsbøker.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-105">Alternatively, you can reuse an ER format that was originally designed to generate reports as Excel workbooks.</span></span> <span data-ttu-id="dbe5b-106">I så fall må du erstatte Excel-malen med en Word-mal.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-106">In this case, you must replace the Excel template with a Word template.</span></span>

<span data-ttu-id="dbe5b-107">Fremgangsmåtene nedenfor viser hvordan en bruker med rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan konfigurere et ER-format slik at det genererer rapporter som Word-filer, ved å bruke et ER-format på nytt som ble utformet for å generere rapporter som Excel-filer.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-107">The following procedures show how a user in either the System administrator role or the Electronic reporting developer role can configure an ER format to generate reports as Word files by reusing an ER format that was designed to generate reports as Excel files.</span></span>

<span data-ttu-id="dbe5b-108">Disse fremgangsmåtene kan fullføres i firmaet GBSI.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-108">These procedures can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dbe5b-109">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="dbe5b-109">Prerequisites</span></span>

<span data-ttu-id="dbe5b-110">For å kunne fullføre disse fremgangsmåtene må du først følge trinnene i oppgaveveiledningen [Utforme en konfigurasjon for generering av rapporter i OPENXML-format](er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="dbe5b-110">To complete these procedures, you must first follow the steps in the [Design a configuration for generating reports in OPENXML format](er-design-reports-openxml-2016-11.md) task guide.</span></span>

<span data-ttu-id="dbe5b-111">Du må også laste ned og lagre følgende maler lokalt for eksempelrapporten:</span><span class="sxs-lookup"><span data-stu-id="dbe5b-111">You must also download and locally save the following templates for the sample report:</span></span>

- [<span data-ttu-id="dbe5b-112">Mal for betalingsrapport (SampleVendPaymDocReport.docx)</span><span class="sxs-lookup"><span data-stu-id="dbe5b-112">Template of Payment Report (SampleVendPaymDocReport.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="dbe5b-113">Bundet mal for betalingsrapport (SampleVendPaymDocReportBounded.docx)</span><span class="sxs-lookup"><span data-stu-id="dbe5b-113">Bounded Template of Payment Report (SampleVendPaymDocReportBounded.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

<span data-ttu-id="dbe5b-114">Disse fremgangsmåtene er for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611 (november 2016).</span><span class="sxs-lookup"><span data-stu-id="dbe5b-114">These procedures are for a feature that was added in Dynamics 365 for Operations version 1611 (November 2016).</span></span>

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="dbe5b-115">Velg den eksisterende ER-rapportkonfigurasjonen</span><span class="sxs-lookup"><span data-stu-id="dbe5b-115">Select the existing ER report configuration</span></span>

1. <span data-ttu-id="dbe5b-116">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering** i Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-116">In Dynamics 365 Finance, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="dbe5b-117">Kontroller at konfigurasjonsleverandøren **Litware, Inc.** er merket som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-117">Make sure that the **Litware, Inc.** configuration provider is selected as **Active**.</span></span> <span data-ttu-id="dbe5b-118">Hvis den ikke er det, følger du trinnene i opprett oppgaveveiledningen [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="dbe5b-118">If it isn't, follow the steps in the [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) task guide.</span></span>
3. <span data-ttu-id="dbe5b-119">Velg **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-119">Select **Reporting configurations**.</span></span> <span data-ttu-id="dbe5b-120">Du skal bruke den eksisterende ER-konfigurasjonen som opprinnelig ble utformet for å generere rapportutdataene i OPENXML-formatet, på nytt.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-120">You will reuse the existing ER configuration that was designed to generate the report output in OPENXML format.</span></span>
4. <span data-ttu-id="dbe5b-121">I konfigurasjonstreet i venstre rute på **Konfigurasjoner**-siden utvider du **Betalingsmodell** og velger **Regnearkeksempelrapport**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-121">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and select **Sample worksheet report**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dbe5b-122">Utkastversjonen av det valgte ER-formatet kan redigeres i hurtigfanen **Versjoner**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-122">The draft version of the selected ER format can be edited on the **Versions** FastTab.</span></span>

5. <span data-ttu-id="dbe5b-123">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-123">Select **Designer**.</span></span>
6. <span data-ttu-id="dbe5b-124">Merk at tittelen på rotformatelementet på **Formatutforming**-siden angir at en Excel-mal for øyeblikket er i bruk.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-124">On the **Format designer** page, notice that the title of the root format element indicates that an Excel template is currently used.</span></span>

![Velge den eksisterende konfigurasjonen](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a><span data-ttu-id="dbe5b-126">Se gjennom den nedlastede Word-malen</span><span class="sxs-lookup"><span data-stu-id="dbe5b-126">Review the downloaded Word template</span></span>

1. <span data-ttu-id="dbe5b-127">Åpne malfilen **SampleVendPaymDocReport.docx** du lastet ned tidligere, i skrivebordsversjonen av Word.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-127">In the Word desktop application, open the **SampleVendPaymDocReport.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="dbe5b-128">Kontroller at malen bare inneholder oppsettet for dokumentet du vil generere som ER-utdata.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-128">Verify that the template contains only the layout of the document that you want to generate as ER output.</span></span>

![Oppsettet i Word-malen i skrivebordsprogrammet](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a><span data-ttu-id="dbe5b-130">Erstatte Excel-malen med Word-malen og legge til en egendefinert XML-del</span><span class="sxs-lookup"><span data-stu-id="dbe5b-130">Replace the Excel template with the Word template and add a custom XML part</span></span>

<span data-ttu-id="dbe5b-131">For øyeblikket brukes Excel-dokumentet som en mal til å generere utdataene i OPENXML-format.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-131">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="dbe5b-132">Du skal erstatte denne malen med Word-malfilen SampleVendPaymDocReport.docx du lastet ned tidligere.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-132">You will replace this template with the SampleVendPaymDocReport.docx Word template file that you downloaded earlier.</span></span> <span data-ttu-id="dbe5b-133">Du skal også utvide Word-malen ved å legge til en egendefinert XML-del.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-133">You will also extend the Word template by adding a custom XML part.</span></span>

1. <span data-ttu-id="dbe5b-134">Velg **Vedlegg** i **Format**-fanen på **Formatutforming**-siden i Finance.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-134">In Finance, on the **Format designer** page, on the **Format** tab, select **Attachments**.</span></span>
2. <span data-ttu-id="dbe5b-135">Velg **Slett** på **Vedlegg**-siden for å fjerne den eksisterende Excel-malen.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-135">On the **Attachments** page, select **Delete** to remove the existing Excel template.</span></span> <span data-ttu-id="dbe5b-136">Velg **Ja** for å bekrefte endringen.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-136">Select **Yes** to confirm the change.</span></span>
3. <span data-ttu-id="dbe5b-137">Velg **Ny** \> **Fil**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-137">Select **New** \> **File**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dbe5b-138">Du må velge en dokumenttype som er [konfigurert](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) i ER-parameterne, for å kunne lagre maler for ER-formater.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-138">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

4. <span data-ttu-id="dbe5b-139">Velg **Bla gjennom**, og bla deretter til og velg filen **SampleVendPaymDocReport.docx** som du lastet ned tidligere.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-139">Select **Browse**, and then browse to and select the **SampleVendPaymDocReport.docx** file that you downloaded earlier.</span></span>
5. <span data-ttu-id="dbe5b-140">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-140">Select **OK**.</span></span>
6. <span data-ttu-id="dbe5b-141">Lukk **Vedlegg**-siden.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-141">Close the **Attachments** page.</span></span>
7. <span data-ttu-id="dbe5b-142">Angi eller velg filen **SampleVendPaymDocReport.docx** i **Mal**-feltet på **Formatutforming**-siden for å bruke denne Word-malen i stedet for Excel-malen som ble brukt tidligere.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-142">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReport.docx** file to use that Word template instead of the Excel template that was previously used.</span></span>
8. <span data-ttu-id="dbe5b-143">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-143">Select **Save**.</span></span>

    <span data-ttu-id="dbe5b-144">I tillegg til å lagre konfigurasjonsendringer, oppdaterer **Lagre**-handlingen den vedlagte Word-malen.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-144">In addition to storing configuration changes, the **Save** action updates the attached Word template.</span></span> <span data-ttu-id="dbe5b-145">Den hierarkiske strukturen til det utformede formatet føyes til det vedlagte Word-dokumentet som en ny, egendefinert XML-del med navnet **Rapport**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-145">The hierarchical structure of the designed format is added to the attached Word document as a new custom XML part that is named **Report**.</span></span> <span data-ttu-id="dbe5b-146">Den vedlagte Word-malen inneholder oppsettet for dokumentet som blir generert som ER-utdata, og strukturen til dataene som ER registrerer i denne malen under kjøring.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-146">The attached Word template contains the layout of the document that will be generated as ER output and the structure of data that ER will enter in that template at runtime.</span></span>

9. <span data-ttu-id="dbe5b-147">Merk at tittelen på rotformatelementet angir at en Word-mal for øyeblikket er i bruk.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-147">Notice that the title of the root format element indicates that a Word template is currently used.</span></span>

    ![Erstatte Excel-malen med Word-malen og legge til en egendefinert XML-del](../media/er-design-configuration-word-2016-11-image03.gif)

10. <span data-ttu-id="dbe5b-149">Velg **Vedlegg** i fanen **Format**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-149">On the **Format** tab, select **Attachments**.</span></span>

<span data-ttu-id="dbe5b-150">Du kan nå tilordne elementene i den egendefinerte XML-delen **Rapport** til innholdskontrollene for Word-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-150">You can now map the elements of the **Report** custom XML part to the content controls of the Word document.</span></span>

<span data-ttu-id="dbe5b-151">Hvis du har erfaring med utforming av Word-dokumenter som skjemaer som inneholder [innholdskontroller](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) som er tilordnet til elementer med [egendefinerte XML-deler](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), fullfører du alle trinnene i den neste fremgangsmåten for å opprette dokumentet.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-151">If you're familiar with the process of designing Word documents as forms that contain [content controls](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) that are mapped to elements of [custom XML parts](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), complete all steps in the next procedure to create the document.</span></span> <span data-ttu-id="dbe5b-152">Hvis du vil ha mer informasjon, kan du se [Opprette skjemaer som brukere fullfører eller skriver ut i Word](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span><span class="sxs-lookup"><span data-stu-id="dbe5b-152">For more information, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span></span> <span data-ttu-id="dbe5b-153">Ellers hopper du over neste fremgangsmåte.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-153">Otherwise, skip the next procedure.</span></span>

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a><span data-ttu-id="dbe5b-154">Hente et Word-dokument som har en egendefinert XML-del, og foreta datatilordning</span><span class="sxs-lookup"><span data-stu-id="dbe5b-154">Get a Word document that has a custom XML part and do data mapping</span></span>

1. <span data-ttu-id="dbe5b-155">Velg **Åpne** på **Vedlegg**-siden i Finance for å laste ned den valgte malen fra Finance og lagre den lokalt som et Word-dokument.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-155">In Finance, on the **Attachments** page, select **Open** to download the selected template from Finance and store it locally as a Word document.</span></span>
3. <span data-ttu-id="dbe5b-156">Åpne dokumentet du nettopp lastet ned, i skrivebordsversjonen av Word.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-156">In the Word desktop application, open the document that you just downloaded.</span></span>
4. <span data-ttu-id="dbe5b-157">I **Utvikler**-fanen velger du ruten **XML-tilordning**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-157">On the **Developer** tab, select **XML Mapping Pane**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dbe5b-158">Hvis **Utvikler**-fanen ikke vises på båndet, kan du tilpasse båndet for å legge den til.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-158">If the **Developer** tab doesn't appear on the ribbon, customize the ribbon to add it.</span></span>

5. <span data-ttu-id="dbe5b-159">Velg den egendefinerte XML-delen **Rapport** i feltet **Egendefinert XML-del** i ruten **XML-tilordning**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-159">In the **XML Mapping** pane, in the **Custom XML Part** field, select the **Report** custom XML part.</span></span>
6. <span data-ttu-id="dbe5b-160">Tilordne elementene i den valgte egendefinerte XML-delen **Rapport** og innholdskontrollene for Word-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-160">Map the elements of the selected **Report** custom XML part and the content controls of the Word document.</span></span>
7. <span data-ttu-id="dbe5b-161">Lagre det oppdaterte Word-dokumentet lokalt som **SampleVendPaymDocReportBounded.docx**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-161">Save the updated Word document locally as **SampleVendPaymDocReportBounded.docx**.</span></span>

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="dbe5b-162">Gå gjennom Word-malen der den egendefinerte XML-delen er tilordnet til innholdskontroller</span><span class="sxs-lookup"><span data-stu-id="dbe5b-162">Review the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="dbe5b-163">Åpne malfilen **SampleVendPaymDocReportBounded.docx** i skrivebordsversjonen av Word.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-163">In the Word desktop application, open the **SampleVendPaymDocReportBounded.docx** template file.</span></span>
2. <span data-ttu-id="dbe5b-164">Kontroller at malen inneholder oppsettet for dokumentet du vil generere som ER-utdata.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-164">Verify that the template contains the layout of the document that you want to generate as ER output.</span></span> <span data-ttu-id="dbe5b-165">Innholdskontrollene som brukes som plassholdere for data som ER skal registrere i denne malen ved kjøretid, er basert på tilordningene som er konfigurert mellom elementer i den egendefinerte XML-delen **Rapport** og innholdskontrollene i Word-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-165">The content controls that are used as placeholders for data that ER will enter in this template at runtime are based on the mappings that are configured between elements of the **Report** custom XML part and the content controls of the Word document.</span></span>

![Forhåndsvisning av Word-mal i skrivebordsprogrammet](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="dbe5b-167">Laste opp Word-malen der den egendefinerte XML-delen er tilordnet til innholdskontroller</span><span class="sxs-lookup"><span data-stu-id="dbe5b-167">Upload the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="dbe5b-168">Velg **Slett** på **Vedlegg**-siden i Finance for å fjerne Word-malen som ikke har noen tilordninger mellom elementer i den egendefinerte XML-delen **Rapport** og innholdskontrollene.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-168">In Finance, on the **Attachments** page, select **Delete** to remove the Word template that has no mappings between elements of the **Report** custom XML part and content controls.</span></span> <span data-ttu-id="dbe5b-169">Velg **Ja** for å bekrefte endringen.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-169">Select **Yes** to confirm the change.</span></span>
2. <span data-ttu-id="dbe5b-170">Velg **Ny** \> **Fil** for å legge til en ny malfil som inneholder tilordninger mellom elementer i den egendefinerte XML-delen **Rapport** og innholdskontrollene.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-170">Select **New** \> **File** to add a new template file that contains mappings between elements of the **Report** custom XML part and content controls.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dbe5b-171">Du må velge en dokumenttype som er [konfigurert](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) i ER-parameterne, for å kunne lagre maler for ER-formater.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-171">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

3. <span data-ttu-id="dbe5b-172">Velg **Bla gjennom**, og bla deretter til og velg filen **SampleVendPaymDocReportBounded.docx** du lastet ned eller klargjorde ved å fullføre fremgangsmåten i delen [Hente et Word-dokument som har en egendefinert XML-del, og foreta datatilordning](#get-word-doc).</span><span class="sxs-lookup"><span data-stu-id="dbe5b-172">Select **Browse**, and then browse to and select the **SampleVendPaymDocReportBounded.docx** file that you downloaded or prepared by completing the procedure in the [Get a Word that has a custom XML part to do data mapping](#get-word-doc) section.</span></span>
4. <span data-ttu-id="dbe5b-173">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-173">Select **OK**.</span></span>
5. <span data-ttu-id="dbe5b-174">Lukk **Vedlegg**-siden.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-174">Close the **Attachments** page.</span></span>
6. <span data-ttu-id="dbe5b-175">Velg dokumentet du nettopp lastet ned, i **Mal**-feltet på **Formatutforming**-siden.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-175">On the **Format designer** page, in the **Template** field, select the document that you just downloaded.</span></span>
7. <span data-ttu-id="dbe5b-176">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-176">Select **Save**.</span></span>
8. <span data-ttu-id="dbe5b-177">Lukk **Formatutforming**-siden.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-177">Close the **Format designer** page.</span></span>

## <a name="mark-the-configured-format-as-runnable"></a><span data-ttu-id="dbe5b-178">Merke det konfigurerte formatet som kjørbart</span><span class="sxs-lookup"><span data-stu-id="dbe5b-178">Mark the configured format as runnable</span></span>

<span data-ttu-id="dbe5b-179">For å kunne kjøre utkastversjonen av det redigerbare formatet må du gjøre den [kjørbar](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span><span class="sxs-lookup"><span data-stu-id="dbe5b-179">To run the draft version of the editable format, you must make it [runnable](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span></span>

1. <span data-ttu-id="dbe5b-180">Velg **Brukerparametere** i gruppen **Avanserte innstillinger** i **Konfigurasjoner**-fanen i handlingsruten på **Konfigurasjoner**-siden i Finance.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-180">In Finance, on the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
2. <span data-ttu-id="dbe5b-181">I dialogboksen **Brukerparametere** setter du **Kjøringsinnstillinger** til **Ja**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-181">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
3. <span data-ttu-id="dbe5b-182">Velg **Rediger** for å gjøre gjeldende side redigerbar, hvis nødvendig.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-182">Select **Edit** to make the current page editable, as required.</span></span>
4. <span data-ttu-id="dbe5b-183">Angi **Ja** for alternativet **Kjør utkast** for den valgte konfigurasjonen **Regnearkeksempelrapport**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-183">For the currently selected **Sample worksheet report** configuration, set the **Run Draft** option to **Yes**.</span></span>
5. <span data-ttu-id="dbe5b-184">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-184">Select **Save**.</span></span>

## <a name="run-the-format-to-create-output-in-word-format"></a><span data-ttu-id="dbe5b-185">Kjøre formatet for å opprette utdata i Word-format</span><span class="sxs-lookup"><span data-stu-id="dbe5b-185">Run the format to create output in Word format</span></span>

1. <span data-ttu-id="dbe5b-186">Gå til **Leverandører** \> **Betalinger** \> **Betalingsjournal** i Finance.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-186">In Finance, go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="dbe5b-187">Velg **Linjer** i en betalingsjournal du angav tidligere.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-187">In a payment journal that you entered earlier, select **Lines**.</span></span>
3. <span data-ttu-id="dbe5b-188">På **Leverandørbetalinger**-siden merker du alle radene i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-188">On the **Vendor payments** page, select all rows in the grid.</span></span>
4. <span data-ttu-id="dbe5b-189">Velg **Betalingsstatus** \> **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-189">Select **Payment status** \> **None**.</span></span>

    ![Betalinger for behandling på Leverandørbetalinger-siden](../media/er-design-configuration-word-2016-11-image05.png)

5. <span data-ttu-id="dbe5b-191">Velg **Generer betalinger** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-191">On the Action Pane, select **Generate payments**.</span></span>
6. <span data-ttu-id="dbe5b-192">Følg denne fremgangsmåten i dialogboksen som vises:</span><span class="sxs-lookup"><span data-stu-id="dbe5b-192">In the dialog box that appears, follow these steps:</span></span>

    1. <span data-ttu-id="dbe5b-193">Velg **Elektronisk** i feltet **Betalingsmåte**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-193">In the **Method of payment** field, select **Electronic**.</span></span>
    2. <span data-ttu-id="dbe5b-194">Velg **GBSI OPER** i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-194">In the **Bank account** field, select **GBSI OPER**.</span></span>
    3. <span data-ttu-id="dbe5b-195">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-195">Select **OK**.</span></span>

7. <span data-ttu-id="dbe5b-196">I dialogboksen **Parametere for elektronisk rapport** velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-196">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="dbe5b-197">De genererte utdataene vises i Word-format og inneholder detaljene for de behandlede betalingene.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-197">The generated output is presented in Word format and contains the details of the processed payments.</span></span> <span data-ttu-id="dbe5b-198">Analyser de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="dbe5b-198">Analyze the generated output.</span></span>

    ![Genererte utdata i Word-format](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a><span data-ttu-id="dbe5b-200">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="dbe5b-200">Additional resources</span></span>

- [<span data-ttu-id="dbe5b-201">Utforme en ny ER-konfigurasjon for å generere rapporter i Word-format</span><span class="sxs-lookup"><span data-stu-id="dbe5b-201">Design a new ER configuration to generate reports in Word format</span></span>](../er-design-configuration-word.md)
- [<span data-ttu-id="dbe5b-202">Bygge inn bilder og figurer i dokumenter du genererer ved hjelp av ER</span><span class="sxs-lookup"><span data-stu-id="dbe5b-202">Embed images and shapes in documents that you generate by using ER</span></span>](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)
