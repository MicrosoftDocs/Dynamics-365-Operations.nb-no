---
title: Skjule Word-innholdskontroller i genererte rapporter
description: Dette emnet beskriver hvordan du konfigurerer et ER-format (Electronic reporting) til å generere rapporter som Microsoft Word-filer der innholdskontroller skjules.
author: NickSelin
manager: AnnBe
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 81ad25514154dd8982aa4f849f0b2bfeb85270f7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562124"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a><span data-ttu-id="6cc56-103">Skjule Word-innholdskontroller i genererte rapporter</span><span class="sxs-lookup"><span data-stu-id="6cc56-103">Suppress Word content controls in generated reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6cc56-104">Hvis du vil generere rapporter som Microsoft Word-dokumenter, må du utforme en mal for rapportene som et Word-dokument.</span><span class="sxs-lookup"><span data-stu-id="6cc56-104">To generate reports as Microsoft Word documents, you must design a template for the reports as a Word document.</span></span> <span data-ttu-id="6cc56-105">Denne malen må inneholde Word-innholdskontroller som plassholdere for data som fylles ut ved kjøretid.</span><span class="sxs-lookup"><span data-stu-id="6cc56-105">This template must contain Word content controls as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="6cc56-106">Hvis du vil bruke Word-dokumentet som opprettes som en mal for rapportene dine, kan du [konfigurere](er-design-configuration-word.md) en ny løsning for [Elektronisk rapportering (ER)](general-electronic-reporting.md)[løsning](er-quick-start1-new-solution.md).</span><span class="sxs-lookup"><span data-stu-id="6cc56-106">To use the Word document that is created as a template for your reports, you can [configure](er-design-configuration-word.md) a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="6cc56-107">Løsningen må inneholde en ER-[konfigurasjon](general-electronic-reporting.md#Configuration) som inneholder en komponent for ER-[format](general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="6cc56-107">The solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="6cc56-108">Dette ER-formatet må konfigureres til å bruke den utformede malen for rapportgenerering.</span><span class="sxs-lookup"><span data-stu-id="6cc56-108">This ER format must be configured to use the designed template for report generation.</span></span>

<span data-ttu-id="6cc56-109">I versjon 10.0.6 og senere av Dynamics 365 Finance kan du konfigurere formler i ER-formatet for å vise informasjon om enkelte Word-innholdskontroller i genererte dokumenter.</span><span class="sxs-lookup"><span data-stu-id="6cc56-109">In version 10.0.6 and later of Dynamics 365 Finance, you can configure formulas in your ER format to suppress some Word content controls in generated documents.</span></span>

<span data-ttu-id="6cc56-110">Trinnene nedenfor forklarer hvordan en bruker som er tilordnet til systemadministratoren eller den elektroniske rapporteringsfunksjonelle konsulentrollen, kan konfigurere et ER-format som genererer rapporter som Word-filer og viser noen av innholdskontrollene i de genererte rapportene som er konfigurert ved hjelp av en Word-mal.</span><span class="sxs-lookup"><span data-stu-id="6cc56-110">The following steps explain how a user who is assigned to the System administrator or Electronic reporting functional consultant role can configure an ER format that generates reports as Word files and suppresses some of the content controls in the generated reports that have been configured by using a Word template.</span></span>

<span data-ttu-id="6cc56-111">Denne fremgangsmåten kan gjennomføres i firmaet GBSI.</span><span class="sxs-lookup"><span data-stu-id="6cc56-111">These steps can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6cc56-112">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="6cc56-112">Prerequisites</span></span>

<span data-ttu-id="6cc56-113">For å fullføre disse trinnene, må du først fullføre trinnene i fløgende oppgaveveiledninger:</span><span class="sxs-lookup"><span data-stu-id="6cc56-113">To complete these steps, you must first complete the steps in the following task guides:</span></span>

- [<span data-ttu-id="6cc56-114">Utforme en konfigurasjon for generering av rapporter i OPENXML-format</span><span class="sxs-lookup"><span data-stu-id="6cc56-114">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="6cc56-115">Bruke ER-konfigurasjoner på nytt med Excel-maler for å generere rapporter i Word-format</span><span class="sxs-lookup"><span data-stu-id="6cc56-115">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)

<span data-ttu-id="6cc56-116">Når du fullfører trinnene i disse oppgavehåndbokene, klargjøres følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="6cc56-116">When you complete the steps of these task guides, the following items are prepared:</span></span>

- <span data-ttu-id="6cc56-117">Et ER-format kalt **Regnearkeksempelrapport** som konfigureres til å generere et dokument i Word-format</span><span class="sxs-lookup"><span data-stu-id="6cc56-117">A **Sample worksheet report** ER format that is configured to generate a document in Word format</span></span>
- <span data-ttu-id="6cc56-118">Et [utkast](general-electronic-reporting.md#component-versioning) til ER-formatet for **Regnearkeksempelrapport** som er merket som **Kjørbar**</span><span class="sxs-lookup"><span data-stu-id="6cc56-118">A [draft](general-electronic-reporting.md#component-versioning) version of the **Sample worksheet report** ER format that is marked as **Runnable**</span></span>
- <span data-ttu-id="6cc56-119">En **elektronisk** betalingsmåte som er konfigurert til å bruke ER-formatet for **Regnearkeksempelrapport** for leverandørbetalingsbehandling</span><span class="sxs-lookup"><span data-stu-id="6cc56-119">An **Electronic** method of payments that is configured to use the **Sample worksheet report** ER format for vendor payment processing</span></span>

<span data-ttu-id="6cc56-120">Du må også laste ned og lagre følgende mal for eksempelrapporten:</span><span class="sxs-lookup"><span data-stu-id="6cc56-120">You must also download and save the following template for the sample report:</span></span>

- [<span data-ttu-id="6cc56-121">Bundet mal 2 for betalingsrapport (SampleVendPaymDocReportBounded2.docx)</span><span class="sxs-lookup"><span data-stu-id="6cc56-121">Bounded Template 2 of Payment Report (SampleVendPaymDocReportBounded2.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a><span data-ttu-id="6cc56-122">Se gjennom den nedlastede Word-malen</span><span class="sxs-lookup"><span data-stu-id="6cc56-122">Review the downloaded Word template</span></span>

1. <span data-ttu-id="6cc56-123">Åpne malfilen **SampleVendPaymDocReportBounded2.docx** du lastet ned tidligere, i skrivebordsversjonen av Word.</span><span class="sxs-lookup"><span data-stu-id="6cc56-123">In the Word desktop application, open the **SampleVendPaymDocReportBounded2.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="6cc56-124">Kontroller at malfilen inneholder et sammendragsseksjon som viser totalt betalingsbeløp for hver valutakode som er oppfylt i de behandlede betalingene.</span><span class="sxs-lookup"><span data-stu-id="6cc56-124">Verify that the template file contains a summary section that shows the total payment amounts for every currency code that has been met in the processed payments.</span></span>

    - <span data-ttu-id="6cc56-125">Sammendragsdelen ligger i en separat tabell i Word-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6cc56-125">The summary section resides in a separate table of the Word document.</span></span>
    - <span data-ttu-id="6cc56-126">Den første raden i denne tabellen inneholder tabellkolonneoverskriftene som seksjonshode.</span><span class="sxs-lookup"><span data-stu-id="6cc56-126">The first row of this table holds the table columns headings as the section header.</span></span>
    - <span data-ttu-id="6cc56-127">Den andre raden i denne tabellen inneholder den gjentagende innholdskontrollen som deldetaljene.</span><span class="sxs-lookup"><span data-stu-id="6cc56-127">The second row of this table holds the repeating content control as the section details.</span></span>
    - <span data-ttu-id="6cc56-128">Denne innholdskontrollen er tilordnet til feltet **SummaryLines** i delen om tilpasset XML i **rapporten**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-128">This content control is mapped to the **SummaryLines** field of the **Report** custom XML part.</span></span>
    - <span data-ttu-id="6cc56-129">Basert på denne tilordningen er innholdskontrollen knyttet til elementet **SummaryLines** i det redigerbare ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="6cc56-129">Based on this mapping, the content control is associated with the **SummaryLines** element of the editable ER format.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6cc56-130">Den gjentagende innholdskontrollen merkes av nøkkelen **SummaryLines** som samsvarer med feltet for den egendefinerte XML-delen den er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="6cc56-130">The repeating content control is tagged by the **SummaryLines** key that matches the field of the custom XML part that it has been mapped to.</span></span>

    ![Oppsett for Word-mal](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="6cc56-132">Velg den eksisterende ER-rapportkonfigurasjonen</span><span class="sxs-lookup"><span data-stu-id="6cc56-132">Select the existing ER report configuration</span></span>

<span data-ttu-id="6cc56-133">I disse trinnene bruker du den eksisterende ER-konfigurasjonen du konfigurerte på nytt da du fullførte trinnene i de tidligere nevnte oppgaveveiledningene.</span><span class="sxs-lookup"><span data-stu-id="6cc56-133">For the following steps, you will reuse the existing ER configuration that you configured when you completed the steps in the previously mentioned task guides.</span></span>

1. <span data-ttu-id="6cc56-134">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-134">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6cc56-135">Velg **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-135">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="6cc56-136">På siden **Konfigurasjoner** utvider du **Betalingsmodell** i konfigurasjonstreet og velger **Regnearkeksempelrapport**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-136">On the **Configurations** page, in the configuration tree, expand **Payment model**, and select **Sample worksheet report**.</span></span>
4. <span data-ttu-id="6cc56-137">Velg **Utforming** for å redigere utkastversjonen av det valgte ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="6cc56-137">Select **Designer** to edit the draft version of the selected ER format.</span></span>

## <a name="replace-the-current-template-with-the-new-template"></a><span data-ttu-id="6cc56-138">Erstatt den gjeldende malen med den nye malen</span><span class="sxs-lookup"><span data-stu-id="6cc56-138">Replace the current template with the new template</span></span>

<span data-ttu-id="6cc56-139">For øyeblikket brukes filen SampleVendPaymDocReportBounded.docx som en mal for å generere utdataene i Word-format.</span><span class="sxs-lookup"><span data-stu-id="6cc56-139">Currently, the SampleVendPaymDocReportBounded.docx file is used as a template to generate the output in Word format.</span></span> <span data-ttu-id="6cc56-140">I fremgangsmåten nedenfor skal du erstatte denne Word-malen med den nye Word-malfilen, SampleVendPaymDocReportBounded2.docx, du lastet ned tidligere.</span><span class="sxs-lookup"><span data-stu-id="6cc56-140">In the following steps, you will replace this Word template with the new Word template, SampleVendPaymDocReportBounded2.docx, that you downloaded earlier.</span></span>

1. <span data-ttu-id="6cc56-141">På siden **Formatutforming** velger du **Vedlegg**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-141">On the **Format designer** page, select **Attachments**.</span></span>
2. <span data-ttu-id="6cc56-142">Velg **Slett** på siden **Vedlegg** for å fjerne den eksisterende malen.</span><span class="sxs-lookup"><span data-stu-id="6cc56-142">On the **Attachments** page, select **Delete** to remove the existing template.</span></span>
3. <span data-ttu-id="6cc56-143">Velg **Ja** for å bekrefte slettingen.</span><span class="sxs-lookup"><span data-stu-id="6cc56-143">Select **Yes** to confirm the deletion.</span></span>
4. <span data-ttu-id="6cc56-144">Velg **Ny** \> **Fil**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-144">Select **New** \> **File**.</span></span>
5. <span data-ttu-id="6cc56-145">Velg **Bla gjennom**, og bla til og velg filen **SampleVendPaymDocReportBounded2.docx** som du lastet ned tidligere.</span><span class="sxs-lookup"><span data-stu-id="6cc56-145">Select **Browse**, and browse to and select the **SampleVendPaymDocReportBounded2.docx** file that you downloaded earlier.</span></span>
6. <span data-ttu-id="6cc56-146">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-146">Select **OK**.</span></span>
7. <span data-ttu-id="6cc56-147">Lukk **Vedlegg**-siden.</span><span class="sxs-lookup"><span data-stu-id="6cc56-147">Close the **Attachments** page.</span></span>
8. <span data-ttu-id="6cc56-148">Angi eller velg filen **SampleVendPaymDocReportBounded2.docx** i feltet **Mal** på siden **Formatutforming**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-148">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReportBounded2.docx** file.</span></span>

## <a name="run-the-format-to-create-word-output"></a><span data-ttu-id="6cc56-149">Kjøre formatet for å opprette Word-utdata</span><span class="sxs-lookup"><span data-stu-id="6cc56-149">Run the format to create Word output</span></span>

1. <span data-ttu-id="6cc56-150">Gå til **Leverandører** \> **Betalinger** \> **Betalingsjournal**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-150">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="6cc56-151">Velg alle betalingene på i fanen **Liste** på siden **Leverandørbetalinger**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-151">On the **Vendor payments** page, on the **List** tab, select all the payments.</span></span>
3. <span data-ttu-id="6cc56-152">Velg **Betalingsstatus** \> **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-152">Select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="6cc56-153">Velg **Generer betalinger**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-153">Select **Generate payments**.</span></span>
5. <span data-ttu-id="6cc56-154">Velg **Elektronisk** i feltet **Betalingsmåte**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-154">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="6cc56-155">Velg **GBSI OPER** i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-155">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="6cc56-156">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-156">Select **OK**.</span></span>
8. <span data-ttu-id="6cc56-157">I dialogboksen **Parametere for elektronisk rapport** velger du **OK** og analyserer de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="6cc56-157">In the **Electronic report parameters** dialog box, select **OK**, and analyze the generated output.</span></span>

    ![Betalinger for behandling på Leverandørbetalinger-siden](./media/er-design-configuration-word-suppress-controls-image2.gif)

    <span data-ttu-id="6cc56-159">Resultatet vises i Word-format, og inneholder sammendragsdelen.</span><span class="sxs-lookup"><span data-stu-id="6cc56-159">The output is presented in Word format and contains the summary section.</span></span>

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a><span data-ttu-id="6cc56-160">Konfigurere det redigerbare formatet til å skrive ned sammendragsdelen</span><span class="sxs-lookup"><span data-stu-id="6cc56-160">Configure the editable format to suppress the summary section</span></span>

<span data-ttu-id="6cc56-161">Hvis du vil skrive inn sammendragsdelen i et generert dokument basert på forespørselen til en bruker som kjører dette ER-formatet, må du endre ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="6cc56-161">If you want to suppress the summary section in a generated document, based on the request of a user who runs this ER format, you must modify the editable ER format.</span></span>

1. <span data-ttu-id="6cc56-162">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering** og åpne utkastversjonen av ER-formatet for redigering.</span><span class="sxs-lookup"><span data-stu-id="6cc56-162">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**, and open the draft version of the ER format for editing.</span></span>
2. <span data-ttu-id="6cc56-163">Velg **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-163">Select **Reporting configurations**.</span></span> 
3. <span data-ttu-id="6cc56-164">Vis **Betalingsmodell** \> **Regnearkeksempelrapport** i konfigurasjonstreet på siden **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-164">On the **Configurations** page, in the configuration tree, expand **Payment model** \> **Sample worksheet report**.</span></span>
4. <span data-ttu-id="6cc56-165">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-165">Select **Designer**.</span></span>
5. <span data-ttu-id="6cc56-166">Vis **Word** og velg **SummaryLines** på siden **Formatutforming**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-166">On the **Format designer** page, expand **Word**, and select **SummaryLines**.</span></span>
6. <span data-ttu-id="6cc56-167">I fanen **Tilordning** legger du til en ny datakilde for å spørre brukeren i kjøretid om sammendragsdelen skal undersøkes:</span><span class="sxs-lookup"><span data-stu-id="6cc56-167">On the **Mapping** tab, add a new data source to ask the user, at runtime, whether the summary section should be suppressed:</span></span>

    1. <span data-ttu-id="6cc56-168">Velg **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-168">Select **Add root**.</span></span>
    2. <span data-ttu-id="6cc56-169">I dialogboksen **Legg til datakilde** velger du **Generelt\Inndataparameter for bruker** for å åpne dialogboksen **Datakildeegenskaper for Inndataparameter for bruker** .</span><span class="sxs-lookup"><span data-stu-id="6cc56-169">In the **Add data source** dialog box, select **General\User input parameter** to open the **'User input parameter' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="6cc56-170">Angi **uipSuppress** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-170">In the **Name** field, enter **uipSuppress**.</span></span>
    4. <span data-ttu-id="6cc56-171">Angi **Skjul sammendragsdel** i feltet **Etikett**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-171">In the **Label** field, enter **Suppress summary section**.</span></span>
    5. <span data-ttu-id="6cc56-172">I feltet **Navn på operasjonsdatatype** velger eller angir du **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-172">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="6cc56-173">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-173">Select **OK**.</span></span>

7. <span data-ttu-id="6cc56-174">Legg til en ny datakilde av programopplistingstypen **NoYes**:</span><span class="sxs-lookup"><span data-stu-id="6cc56-174">Add a new data source of the **NoYes** application enumeration type:</span></span>

    1. <span data-ttu-id="6cc56-175">Velg **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-175">Select **Add root**.</span></span>
    2. <span data-ttu-id="6cc56-176">I dialogboksen **Legg til datakilde** velger du **Dynamics 365 for Operations\Opplisting** for å åpne dialogboksen **Datakildeegenskaper for Opplisting**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-176">In the **Add data source** dialog box, select **Dynamics 365 for Operations\Enumeration** to open the **'Enumeration' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="6cc56-177">Angi **enumNoYes** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-177">In the **Name** field, enter **enumNoYes**.</span></span>
    4. <span data-ttu-id="6cc56-178">Angi **Skjul alternativer** i feltet **Etikett**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-178">In the **Label** field, enter **Suppress options**.</span></span>
    5. <span data-ttu-id="6cc56-179">I feltet **Navn på operasjonsdatatype** velger eller angir du **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-179">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="6cc56-180">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-180">Select **OK**.</span></span>

8. <span data-ttu-id="6cc56-181">For det valgte elementet for **SummaryLines**-format konfigurerer du formelen til å angi når Word-innholdskontrollen som er knyttet til det valgte formatelementet, skal skjules:</span><span class="sxs-lookup"><span data-stu-id="6cc56-181">For the selected **SummaryLines** format element, configure the formula to specify when the Word content control that is associated with the selected format element should be suppressed:</span></span>

    1. <span data-ttu-id="6cc56-182">Velg **Rediger** for å åpne siden **[Formelutforming](general-electronic-reporting-formula-designer.md)** i delen **Fjernet** i fanen **Tilordning**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-182">On the **Mapping** tab, in the **Removed** section, select **Edit** to open the **[Formula designer](general-electronic-reporting-formula-designer.md)** page.</span></span>
    2. <span data-ttu-id="6cc56-183">I feltet **Formel** angir du formelen `uipSuppress = enumNoYes.Yes`.</span><span class="sxs-lookup"><span data-stu-id="6cc56-183">In the **Formula** field, enter the formula `uipSuppress = enumNoYes.Yes`.</span></span>
    3. <span data-ttu-id="6cc56-184">Velg **Lagre**, og lukk siden **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-184">Select **Save**, and close the **Formula designer** page.</span></span>

        > [!NOTE]
        > <span data-ttu-id="6cc56-185">Denne formelen brukes på et generert dokument **etter at alle andre formatelementer er kjørt**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-185">This formula will be applied to a generated document **after all other format elements are run**.</span></span> <span data-ttu-id="6cc56-186">Hvis du vil bruke denne formelen, finnes det en Word-innholdskontroll som er merket som et formatelement som formelen er konfigurert for (**SummaryLines** i dette tilfellet), i et generert dokument.</span><span class="sxs-lookup"><span data-stu-id="6cc56-186">To apply this formula, a Word content control that is tagged as a format element that the formula is configured for (**SummaryLines** in this case) is found in a generated document.</span></span> <span data-ttu-id="6cc56-187">Denne innholdskontrollen fjernes deretter fullstendig, sammen med raden i Word-tabellen som inneholder den.</span><span class="sxs-lookup"><span data-stu-id="6cc56-187">That content control is then completely removed, together with the row in the Word table that holds it.</span></span> <span data-ttu-id="6cc56-188">Detaljraden i sammendragsdelen fjernes fra det genererte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6cc56-188">The details row of the summary section is removed from the generated document.</span></span>
        >
        > <span data-ttu-id="6cc56-189">På utformingstidsprogrammet kan du konfigurere formelen **Fjernet** for et formatelement, selv om ingen innholdskontroll i Word-malen du bruker, har en kode som samsvarer med navnet på et formatelement som egenskapen **Fjernet** er konfigurert for.</span><span class="sxs-lookup"><span data-stu-id="6cc56-189">At design time, you might configure the **Removed** formula for a format element, even though no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span> <span data-ttu-id="6cc56-190">Når du validerer formatet på utformingstidsprogrammet, får du en [advarsel](er-components-inspections.md#i14) om denne inkonsekvensen.</span><span class="sxs-lookup"><span data-stu-id="6cc56-190">When you validate the format at design time, you receive a [warning](er-components-inspections.md#i14) about this inconsistency.</span></span>
        >
        > <span data-ttu-id="6cc56-191">Ved kjøretid skjer det unntak hvis ingen innholdskontroll i Word-malen du bruker, har en kode som samsvarer med navnet på et formatelement som egenskapen **Fjernet** er konfigurert for.</span><span class="sxs-lookup"><span data-stu-id="6cc56-191">At runtime, an exception is thrown if no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span>

    4. <span data-ttu-id="6cc56-192">Sett alternativet **Med overordnet** til **Ja** i delen **Fjernet** i fanen **Tilordning**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-192">On the **Mapping** tab, in the **Removed** section, set the **With parent** option to **Yes**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="6cc56-193">Du må velge **Yes** for å fjerne hele Word-tabellen som det overordnede objektet i raden som inneholder detaljene for sammendragsdelen.</span><span class="sxs-lookup"><span data-stu-id="6cc56-193">You must set this option to **Yes** to remove the whole Word table as the parent object of the row that holds the summary section details.</span></span> <span data-ttu-id="6cc56-194">Hvis du setter dette alternativet til **Nei**, blir overskriftsraden for delen stående i det genererte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6cc56-194">If you set this option to **No**, the section header row remains in the generated document.</span></span>

9. <span data-ttu-id="6cc56-195">Velg **Lagre** for å lagre endringene i det redigerbare formatet.</span><span class="sxs-lookup"><span data-stu-id="6cc56-195">Select **Save** to save your changes to the editable format.</span></span>

    ![De genererte utdataene i Word-format](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a><span data-ttu-id="6cc56-197">Kjøre det endreded formatet for å opprette Word-utdata</span><span class="sxs-lookup"><span data-stu-id="6cc56-197">Run the modified format to create Word output</span></span>

1. <span data-ttu-id="6cc56-198">Gå til **Leverandører** \> **Betalinger** \> **Betalingsjournal**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-198">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="6cc56-199">Velg betalingsjournalen du opprettet, og velg deretter **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-199">Select the payment journal that you created, and then select **Lines**.</span></span>
3. <span data-ttu-id="6cc56-200">På sien **Leverandørbetalinger** merker du alle radene, og deretter velger du **Betalingsstatus** \> **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-200">On the **Vendor payments** page, select all the rows, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="6cc56-201">Velg **Generer betalinger**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-201">Select **Generate payments**.</span></span>
5. <span data-ttu-id="6cc56-202">Velg **Elektronisk** i feltet **Betalingsmåte**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-202">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="6cc56-203">Velg **GBSI OPER** i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-203">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="6cc56-204">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-204">Select **OK**.</span></span>
8. <span data-ttu-id="6cc56-205">Velg **Ja** feltet **Skjul sammendragsdel** i dialogboksen **Parametere for elektronisk rapport**.</span><span class="sxs-lookup"><span data-stu-id="6cc56-205">In the **Electronic report parameters** dialog box, in the **Suppress summary section** field, select **Yes**.</span></span>
9. <span data-ttu-id="6cc56-206">Velg **OK** og analyser de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="6cc56-206">Select **OK**, and analyze the generated output.</span></span>

    ![Genererte utdata i Word-format](./media/er-design-configuration-word-suppress-controls-image4.gif)

    <span data-ttu-id="6cc56-208">Legg merke til at utdataene ikke inneholder sammendragsdelen fordi det er skjedd en feil.</span><span class="sxs-lookup"><span data-stu-id="6cc56-208">Notice that the output doesn't contain the summary section, because it has been suppressed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6cc56-209">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6cc56-209">Additional resources</span></span>

- [<span data-ttu-id="6cc56-210">Utforme en konfigurasjon for generering av rapporter i OPENXML-format</span><span class="sxs-lookup"><span data-stu-id="6cc56-210">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="6cc56-211">Utforme en ny ER-konfigurasjon for å generere rapporter i Word-format</span><span class="sxs-lookup"><span data-stu-id="6cc56-211">Design a new ER configuration to generate reports in Word format</span></span>](er-design-configuration-word.md)
- [<span data-ttu-id="6cc56-212">Bruke ER-konfigurasjoner på nytt med Excel-maler for å generere rapporter i Word-format</span><span class="sxs-lookup"><span data-stu-id="6cc56-212">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="6cc56-213">Kontrollere den konfigurerte ER-komponenten for å forhindre kjøretidsproblemer</span><span class="sxs-lookup"><span data-stu-id="6cc56-213">Inspect the configured ER component to prevent runtime issues</span></span>](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]