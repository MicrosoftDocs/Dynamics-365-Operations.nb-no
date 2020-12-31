---
title: Legge til nye felt i en forretningsdokumentmal i Microsoft Excel
description: Dette emnet inneholder informasjon om hvordan du legger til nye felt i en forretningsdokumentmal i Microsoft Excel ved hjelp av funksjonen for administrasjon av forretningsdokumenter.
author: NickSelin
manager: AnnBe
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: fcfbcb021b192cef75d59b0db1796e994f3dc27d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681382"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a><span data-ttu-id="232b2-103">Legge til nye felt i en forretningsdokumentmal i Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="232b2-103">Add new fields to a business document template in Microsoft Excel</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="232b2-104">Du kan legge til nye felt i en mal som brukes til å generere forretningsdokumenter i Microsoft Excel-format.</span><span class="sxs-lookup"><span data-stu-id="232b2-104">You can add new fields to a template that is used to generate business documents in Microsoft Excel format.</span></span> <span data-ttu-id="232b2-105">Disse feltene kan legges til som plassholdere som brukes til å fylle genererte dokumenter med nødvendig informasjon fra programmet.</span><span class="sxs-lookup"><span data-stu-id="232b2-105">These fields can be added as placeholders that are used to fill generated documents with required information from the application.</span></span> <span data-ttu-id="232b2-106">For hvert felt du legger til, kan du også angi en binding til datakildene for å angi hvilke programdata som skal angis i feltet når malen brukes til å generere forretningsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="232b2-106">For every field that you add, you can also specify a binding to the data sources, to specify what application data will be entered in the field when the template is used to generate business documents.</span></span>

<span data-ttu-id="232b2-107">Hvis du vil vite mer om denne funksjonen, kan du fullføre eksemplet i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="232b2-107">To learn more about this feature, complete the example in this topic.</span></span> <span data-ttu-id="232b2-108">Dette eksemplet viser hvordan du oppdaterer en mal for å fylle ut feltene i skjemaer for fritekstfaktura som genereres.</span><span class="sxs-lookup"><span data-stu-id="232b2-108">This example shows how to update a template to fill in the fields in free text invoice forms that are generated.</span></span>

## <a name="configure-business-document-management-to-edit-templates"></a><span data-ttu-id="232b2-109">Konfigurere administrasjon av forretningsdokument til å redigere maler</span><span class="sxs-lookup"><span data-stu-id="232b2-109">Configure Business document management to edit templates</span></span>

<span data-ttu-id="232b2-110">Fordi Business Document Management (BDM) er bygd på toppen av rammeverket [Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md), må du konfigurere de nødvendige ER- og BDM-parameterne før du kan begynne å arbeide med BDM.</span><span class="sxs-lookup"><span data-stu-id="232b2-110">Because Business document management (BDM) is built on top of the [Electronic reporting (ER) overview](general-electronic-reporting.md) framework, you must configure the required ER and BDM parameters before you can start to work with BDM.</span></span>

1.  <span data-ttu-id="232b2-111">Logg deg på forekomsten av Microsoft Dynamics 365 Finance som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="232b2-111">Sign in to the instance of Microsoft Dynamics 365 Finance as the system administrator.</span></span>
2.  <span data-ttu-id="232b2-112">Fullfør følgende trinn i eksemplet i [Oversikt over administrasjon av forretningsdokument](er-business-document-management.md):</span><span class="sxs-lookup"><span data-stu-id="232b2-112">Complete the following steps of the example in the [Business document management overview](er-business-document-management.md) topic:</span></span>

    1.  <span data-ttu-id="232b2-113">Konfigurer ER-parametere.</span><span class="sxs-lookup"><span data-stu-id="232b2-113">Configure ER parameters.</span></span>
    2.  <span data-ttu-id="232b2-114">Slå på BDM.</span><span class="sxs-lookup"><span data-stu-id="232b2-114">Turn on BDM.</span></span>

<span data-ttu-id="232b2-115">Du kan nå begynne å bruke BDM til å redigere maler for forretningsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="232b2-115">You can now start to use BDM to edit business document templates.</span></span>

## <a name="import-er-solutions-that-contain-a-template"></a><span data-ttu-id="232b2-116">Importere ER-løsninger som inneholder en mal</span><span class="sxs-lookup"><span data-stu-id="232b2-116">Import ER solutions that contain a template</span></span>

<span data-ttu-id="232b2-117">Eksemplet i denne fremgangsmåten bruker løsningen offisielt publisert for ER.</span><span class="sxs-lookup"><span data-stu-id="232b2-117">The example in this procedure uses the officially published ER solution.</span></span> <span data-ttu-id="232b2-118">Du må importere ER-konfigurasjonene av denne løsningen til den gjeldende forekomsten av Finance.</span><span class="sxs-lookup"><span data-stu-id="232b2-118">You must import the ER configurations of this solution into your current instance of Finance.</span></span>

<span data-ttu-id="232b2-119">ER-formatkonfigurasjonen **Fritekstfaktura (Excel)** for denne løsningen inneholder malen for forretningsdokumenter i Excel-format som kan redigeres ved hjelp av BDM.</span><span class="sxs-lookup"><span data-stu-id="232b2-119">The **Free text invoice (Excel)** ER format configuration of this solution contains the business document template in Excel format that can be edited by using BDM.</span></span> <span data-ttu-id="232b2-120">Importer den nyeste versjonen av denne ER-formatkonfigurasjonen fra Microsoft Dynamics Lifecycle Service (LCS).</span><span class="sxs-lookup"><span data-stu-id="232b2-120">Import the latest version of this ER format configuration from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="232b2-121">De tilsvarende tilordningskonfigurasjonene for ER-datamodell og ER-modell blir importert automatisk.</span><span class="sxs-lookup"><span data-stu-id="232b2-121">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

<span data-ttu-id="232b2-122">Hvis du vil ha mer informasjon om å importere ER-konfigurasjoner, kan du se [Administrere livssyklus til konfigurasjoner for elektronisk rapportering (ER)](general-electronic-reporting-manage-configuration-lifecycle.md)</span><span class="sxs-lookup"><span data-stu-id="232b2-122">For more information about how to import ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![Siden Delt LCS-aktivabibliotek](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a><span data-ttu-id="232b2-124">Rediger malen for ER-løsning</span><span class="sxs-lookup"><span data-stu-id="232b2-124">Edit the ER solution template</span></span>

1.  <span data-ttu-id="232b2-125">Logg på som en bruker med tilgang til arbeidsområdet for **administrasjon av forretningsdokument**.</span><span class="sxs-lookup"><span data-stu-id="232b2-125">Sign in as a user who has access to the **Business document management** workspace.</span></span>
2.  <span data-ttu-id="232b2-126">Åpne arbeidsområdet for **administrasjon av forretningsdokument**.</span><span class="sxs-lookup"><span data-stu-id="232b2-126">Open the **Business document management** workspace.</span></span>

    ![Arbeidsområdet Administrasjon av forretningsdokument](./media/BDM-AddFldExcel-Workspace.png)

3.  <span data-ttu-id="232b2-128">I rutenettet velger du malen **Fritekstfaktura (Excel)**.</span><span class="sxs-lookup"><span data-stu-id="232b2-128">In the grid, select the **Free text invoice (Excel)** template.</span></span>
4.  <span data-ttu-id="232b2-129">Velg **Ny mal** i den høyre ruten for å opprette en ny mal som er basert på den valgte malen.</span><span class="sxs-lookup"><span data-stu-id="232b2-129">In the right pane, select **New template** to create a new template that is based on the selected template.</span></span>
5.  <span data-ttu-id="232b2-130">I **Tittel**-feltet angir du **Fritekstfaktura (Excel) Contoso** som tittel for den nye malen.</span><span class="sxs-lookup"><span data-stu-id="232b2-130">In the **Title** field, enter **Free text invoice (Excel) Contoso** as the title of the new template.</span></span>
6.  <span data-ttu-id="232b2-131">Velg **OK** for å bekrefte starten på redigeringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="232b2-131">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="232b2-132">Siden for BDM-malredigering vises.</span><span class="sxs-lookup"><span data-stu-id="232b2-132">The BDM template editor page appears.</span></span> <span data-ttu-id="232b2-133">Du kan bruke Microsoft 365 til å redigere den valgte malen på nettet i den innebygde kontrollen.</span><span class="sxs-lookup"><span data-stu-id="232b2-133">You can use Microsoft 365 to edit the selected template online in the embedded control.</span></span>

![Siden for BDM-malredigering](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a><span data-ttu-id="232b2-135">Legg til etiketten for et nytt felt i malen</span><span class="sxs-lookup"><span data-stu-id="232b2-135">Add the label for a new field to the template</span></span>

1.  <span data-ttu-id="232b2-136">Merk av for **Overskrifter og støttelinjer** for den redigerbare Excel-malen i **Vis**-kategorien i Excel-båndet på siden for BDM-malredigering.</span><span class="sxs-lookup"><span data-stu-id="232b2-136">On the BDM template editor page, on the Excel ribbon, on the **View** tab, select the **Headings and Gridlines** check boxes for the editable Excel template.</span></span>

    ![Avmerkingsbokser for overskrifter og støttelinjer merket av](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  <span data-ttu-id="232b2-138">Merk cellene **E8:F8**.</span><span class="sxs-lookup"><span data-stu-id="232b2-138">Select cells **E8:F8**.</span></span>
3.  <span data-ttu-id="232b2-139">På Excel-båndet i kategorien **Hjem** velger du **Slå sammen og sentrer** for å slå samme de merkede cellene i en ny sammenslått **E8:F8**-celle.</span><span class="sxs-lookup"><span data-stu-id="232b2-139">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **E8:F8** cell.</span></span>
4.  <span data-ttu-id="232b2-140">I den sammenslåtte cellen **E8:F8** skriver du **URL-adresse**.</span><span class="sxs-lookup"><span data-stu-id="232b2-140">In the merged cell **E8:F8**, enter **URL**.</span></span>
5.  <span data-ttu-id="232b2-141">Merk sammenslått celle **E7:F7**, velg **Kopier format**, og velg deretter sammenslått celle **E8:F8** for å formatere den på samme måte som den sammenslåtte cellen **E7:F7**.</span><span class="sxs-lookup"><span data-stu-id="232b2-141">Select merged cell **E7:F7**, select **Format painter**, and then select merged cell **E8:F8** to format it in the same way as merged cell **E7:F7**.</span></span>

    ![Ny feltetikett lagt til i malen](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a><span data-ttu-id="232b2-143">Formatere malen for å reservere plass for et nytt felt</span><span class="sxs-lookup"><span data-stu-id="232b2-143">Format the template to reserve space for a new field</span></span>

1.  <span data-ttu-id="232b2-144">Velg sammenslått celle **GG8:H8** siden for BDM-malredigering.</span><span class="sxs-lookup"><span data-stu-id="232b2-144">On the BDM template editor page, select merged cell **G8:H8**.</span></span>
2.  <span data-ttu-id="232b2-145">På Excel-båndet i kategorien **Hjem** velger du **Slå sammen og sentrer** for å slå samme de merkede cellene i en ny sammenslått **G8:H8**-celle.</span><span class="sxs-lookup"><span data-stu-id="232b2-145">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **G8:H8** cell.</span></span>
3.  <span data-ttu-id="232b2-146">Merk sammenslått celle **G7:H7**, velg **Kopier format**, og velg deretter sammenslått celle **G8:H8** for å formatere den på samme måte som den sammenslåtte cellen **G7:H7**.</span><span class="sxs-lookup"><span data-stu-id="232b2-146">Select merged cell **G7:H7**, select **Format painter**, and then select merged cell **G8:H8** to format it in the same way as merged cell **G7:H7**.</span></span>

    ![Reservert plass for det nye feltet](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  <span data-ttu-id="232b2-148">I **Navn**-boksen velger du **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="232b2-148">In the **Name** box field, select **CompanyInfo**.</span></span>

    <span data-ttu-id="232b2-149">**CompanyInfo**-området for gjeldende Excel-mal inneholder alle feltene som brukes til å fylle hodet i en generert rapport med detaljene i det gjeldende firmaet som selgerpart.</span><span class="sxs-lookup"><span data-stu-id="232b2-149">The **CompanyInfo** range of the current Excel template holds all the fields that are used to fill the header of a generated report with the details of the current company as a seller party.</span></span>

    ![CompanyInfo-område valgt](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a><span data-ttu-id="232b2-151">Legg til et nytt felt i malen</span><span class="sxs-lookup"><span data-stu-id="232b2-151">Add a new field to the template</span></span>

1.  <span data-ttu-id="232b2-152">Velg **Vis format** i handlingruten på siden **BDM-malredigering**.</span><span class="sxs-lookup"><span data-stu-id="232b2-152">On the **BDM template editor** page, on the Action Pane, select **Show format**.</span></span>
2.  <span data-ttu-id="232b2-153">Velg **Legg til** i **Malstruktur**-ruten.</span><span class="sxs-lookup"><span data-stu-id="232b2-153">In the **Template structure** pane, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="232b2-154">Du må justere delen av malen du vil bruke som et nytt felt.</span><span class="sxs-lookup"><span data-stu-id="232b2-154">You must adjust the section of the template that you want to use as a new field.</span></span> <span data-ttu-id="232b2-155">Du har allerede gjort denne justeringen ved å formatere sammenslått celle **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="232b2-155">You already made this adjustment by formatting merged cell **G8:H8**.</span></span>

    ![Legge til et nytt felt i malen](./media/BDM-AddFldExcel-AddCell.png)

3.  <span data-ttu-id="232b2-157">Velg **Excel\celle** for å legge til et nytt felt som en celle i malen.</span><span class="sxs-lookup"><span data-stu-id="232b2-157">Select **Excel\Cell** to add a new field as a cell in the template.</span></span>

    <span data-ttu-id="232b2-158">Du kan velge **Excel\Område** hvis du vil legge til et nytt område i malen.</span><span class="sxs-lookup"><span data-stu-id="232b2-158">You can select **Excel\Range** if you want to add a new range to the template.</span></span> <span data-ttu-id="232b2-159">Området som skrives inn, kan inneholde flere celler.</span><span class="sxs-lookup"><span data-stu-id="232b2-159">The range that is entered can contain multiple cells.</span></span> <span data-ttu-id="232b2-160">Du kan legge til disse cellene senere.</span><span class="sxs-lookup"><span data-stu-id="232b2-160">You can add these cells later.</span></span>
    
    <span data-ttu-id="232b2-161">Legg merke til at **CompanyInfo**-malkomponenten automatisk blir valgt i **Malstruktur**-ruten, fordi den er den mest egnede overordnede komponenten i den gjeldende malstrukturen for feltet du legger til.</span><span class="sxs-lookup"><span data-stu-id="232b2-161">Notice that the **CompanyInfo** template component, is automatically selected in the **Template structure** pane, because it's the most suitable parent component in the current template structure for the field that you're adding.</span></span>
    
4.  <span data-ttu-id="232b2-162">I feltet **Excel-område** angir du **CompanyURL_Value**.</span><span class="sxs-lookup"><span data-stu-id="232b2-162">In the **Excel range** field, enter **CompanyURL_Value**.</span></span>
5.  <span data-ttu-id="232b2-163">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="232b2-163">Select **OK**.</span></span>

    ![CompanyURL_Value-felt lagt til i malstrukturen](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  <span data-ttu-id="232b2-165">I **Malstruktur**-ruten velger du ellipseknappen (...), og velger deretter **Vis bindinger**.</span><span class="sxs-lookup"><span data-stu-id="232b2-165">In the **Template structure** pane, select the ellipsis button (...), and then select **Show bindings**.</span></span>

    ![Vis bindinger valgt](./media/BDM-AddFldExcel-ShowBindings.png)

    <span data-ttu-id="232b2-167">**Malstruktur**-ruten viser nå datakildene som er tilgjengelige i det underliggende ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="232b2-167">The **Template structure** pane now shows the data sources that are available in the underlying ER format.</span></span>

7.  <span data-ttu-id="232b2-168">Velg **CompanyInfo_Value** som feltet du vil binde til en datakilde av det underliggende ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="232b2-168">Select **CompanyInfo_Value** as the field that you plan to bind to a data source of the underlying ER format.</span></span>
8.  <span data-ttu-id="232b2-169">I delen **Datakilder** i ruten **Malstruktur** utvider du **Modell \> InvoiceBase \> CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="232b2-169">In the **Data sources** section of the **Template structure** pane, expand **Model \> InvoiceBase \> CompanyInfo**.</span></span>
9.  <span data-ttu-id="232b2-170">Under **CompanyInfo** velger du **WebsiteURI**-elementet.</span><span class="sxs-lookup"><span data-stu-id="232b2-170">Under **CompanyInfo**, select the **WebsiteURI** item.</span></span>

    ![WebsiteURI-element valgt](./media/BDM-AddFldExcel-BindURL.png)

10. <span data-ttu-id="232b2-172">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="232b2-172">Select **Bind**.</span></span>
11. <span data-ttu-id="232b2-173">I ruten **Malstruktur** velger du **Lagre**, og lukker deretter siden for BDM-malredigering.</span><span class="sxs-lookup"><span data-stu-id="232b2-173">In the **Template structure** pane, select **Save**, and then close the BDM template editor page.</span></span>

<span data-ttu-id="232b2-174">I arbeidsområdet **Administrasjon av forretningsdokument** viser **Mal**-kategorien i ruten til høyre den oppdaterte malen.</span><span class="sxs-lookup"><span data-stu-id="232b2-174">In the **Business document management** workspace, the **Template** tab in the right pane shows the updated template.</span></span> <span data-ttu-id="232b2-175">I rutenettet legger du merke til at **Status**-feltet for den redigerte malen har blitt endret til **Utkast** og **Revisjon**-feltet er ikke lenger tomt.</span><span class="sxs-lookup"><span data-stu-id="232b2-175">In the grid, notice that the **Status** field for the edited template has been changed to **Draft**, and the **Revision** field is no longer blank.</span></span> <span data-ttu-id="232b2-176">Dette betyr at prosessen for redigering av denne malen er startet.</span><span class="sxs-lookup"><span data-stu-id="232b2-176">These changes indicate that the process of editing this template has been started.</span></span>

![Redigert mal i arbeidsområdet for administrasjon av forretningsdokument](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a><span data-ttu-id="232b2-178">Se gjennom firmainnstillinger</span><span class="sxs-lookup"><span data-stu-id="232b2-178">Review company settings</span></span>

1.  <span data-ttu-id="232b2-179">Gå til **Organisasjonsstyring \> Organisasjoner \> Juridiske enheter**.</span><span class="sxs-lookup"><span data-stu-id="232b2-179">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>
2.  <span data-ttu-id="232b2-180">Kontroller at URL-adressen for firma er angitt i hurtigfanen **Kontaktinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="232b2-180">On the **Contact information** FastTab, verify that the company URL is entered.</span></span>

![Firma-URL angitt på juridisk enhet-siden](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a><span data-ttu-id="232b2-182">Generere forretningsdokumenter for å teste den oppdaterte malen</span><span class="sxs-lookup"><span data-stu-id="232b2-182">Generate business documents to test the updated template</span></span>

1.  <span data-ttu-id="232b2-183">Endre firmaet til **USMF** i programmet, og gå til **Kunder \> Fakturaer \> Alle fritekstfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="232b2-183">In the application, change the company to **USMF**, and go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2.  <span data-ttu-id="232b2-184">Velg **FTI-00000002**-fakturaen, og velg deretter **Utskriftsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="232b2-184">Select invoice **FTI-00000002**, and then select **Print management**.</span></span>
3.  <span data-ttu-id="232b2-185">I venstre rute utvider du **Modul - kunder \> Dokumenter \> Fritekstfaktura**.</span><span class="sxs-lookup"><span data-stu-id="232b2-185">In the left pane, expand **Module - accounts receivable \> Documents \> Free text invoice**.</span></span>
4.  <span data-ttu-id="232b2-186">Under **Fritekstfaktura** velger du **Opprinnelig dokument** for å angi omfanget av fakturaer for behandling.</span><span class="sxs-lookup"><span data-stu-id="232b2-186">Under **Free text invoice**, select the **Original document** level to specify the scope of invoices for processing.</span></span>
5.  <span data-ttu-id="232b2-187">I feltet **Rapportformat** i ruten til høyre velger du malen **Fritekstfaktura (Excel) Contoso** for det angitte dokumentnivået.</span><span class="sxs-lookup"><span data-stu-id="232b2-187">In the right pane, in the **Report format** field, select the **Free text invoice (Excel) Contoso** template for the specified document level.</span></span>

    ![Fritekstfaktura (Excel) Contoso-mal valgt](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  <span data-ttu-id="232b2-189">Trykk på **ESC** for å lukke den gjeldende siden.</span><span class="sxs-lookup"><span data-stu-id="232b2-189">Press **Esc** to close the current page.</span></span>
7.  <span data-ttu-id="232b2-190">Velg **Skriv ut \> Valgt**.</span><span class="sxs-lookup"><span data-stu-id="232b2-190">Select **Print \> Selected**.</span></span>
8.  <span data-ttu-id="232b2-191">Last ned det genererte dokumentet, og åpne det i Excel.</span><span class="sxs-lookup"><span data-stu-id="232b2-191">Download the generated document, and open it in Excel.</span></span>

    ![Fritekstfaktura i Excel](./media/BDM-AddFldExcel-PreviewReport.png)

<span data-ttu-id="232b2-193">Den endrede malen brukes til å generere rapporten fritekstfaktura for den valgte varen.</span><span class="sxs-lookup"><span data-stu-id="232b2-193">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="232b2-194">Hvis du vil analysere hvordan denne rapporten påvirkes av endringene du gjør for malen, kan du kjøre denne rapporten i én programøkt rett etter at du endret malen i en annen programøkt.</span><span class="sxs-lookup"><span data-stu-id="232b2-194">To analyze how this report is affected by changes that you make to the template, run the report in one application session immediately after you change the template in another application session.</span></span>

## <a name="related-links"></a><span data-ttu-id="232b2-195">Relaterte koblinger</span><span class="sxs-lookup"><span data-stu-id="232b2-195">Related links</span></span>

[<span data-ttu-id="232b2-196">Oversikt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="232b2-196">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="232b2-197">Oversikt over administrasjon av forretningsdokument</span><span class="sxs-lookup"><span data-stu-id="232b2-197">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="232b2-198">Utforme en konfigurasjon for generering av rapporter i OPENXML-format</span><span class="sxs-lookup"><span data-stu-id="232b2-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks/er-design-reports-openxml-2016-11.md)
