---
title: Brukergrensesnitt i Microsoft Office-stil i Forretningsdokumentbehandling
description: Dette emnet forklarer hvordan du bruker det nye brukergrensesnittet i funksjonen for administrasjon av forretningsdokument i ER-rammeverket (elektronisk rapportering).
author: v-anamir
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6c5081f71a18dfac83b7aea950395436b42f50e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881042"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a><span data-ttu-id="457c8-103">Brukergrensesnitt i Microsoft Office-stil i Forretningsdokumentbehandling</span><span class="sxs-lookup"><span data-stu-id="457c8-103">Microsoft Office-style user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="457c8-104">Med forretningsdokumentadministrering kan forretningsbrukere redigere forretningsdokumentmaler ved å bruke en Microsoft 365-tjeneste eller den aktuelle Microsoft Office-skrivebordsapplikasjonen.</span><span class="sxs-lookup"><span data-stu-id="457c8-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="457c8-105">Redigeringer kan inneholde utformingsendringer eller nye distribusjoner, eller brukere kan legge til plassholdere for å inkludere ytterligere data uten å måtte endre kildekoden.</span><span class="sxs-lookup"><span data-stu-id="457c8-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="457c8-106">Hvis du vil ha mer informasjon om hvordan du arbeider med administrering av forretningsdokumenter, kan du se [Oversikt over administrering av forretningsdokumenter](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="457c8-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="457c8-107">Det nye brukergrensesnittet (UI) er tydeligere og mer behagelig å bruke.</span><span class="sxs-lookup"><span data-stu-id="457c8-107">The new user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="457c8-108">**Forretningsdokument**-området viser bare malene som er tilgjengelige for gjeldende leverandør.</span><span class="sxs-lookup"><span data-stu-id="457c8-108">The **Business document** area shows only the templates that are available for the current provider.</span></span> <span data-ttu-id="457c8-109">I det forrige grensesnittet oppførte kategorien **Mal** alle malene som var tilgjengelige for alle leverandører.</span><span class="sxs-lookup"><span data-stu-id="457c8-109">In the previous UI, the **Template** tab listed all the templates that were available for any providers.</span></span> <span data-ttu-id="457c8-110">Den viste også alle malene som var opprettet og redigert av alle brukere som hadde samme rolle.</span><span class="sxs-lookup"><span data-stu-id="457c8-110">It also showed all the templates that were created and edited by any user who had the same role.</span></span>

<span data-ttu-id="457c8-111">Du kan bruke **Nytt dokument**-knappen til å opprette og redigere en mal i en formatkonfigurasjon for elektronisk rapportering (ER) som leveres av en annen leverandør.</span><span class="sxs-lookup"><span data-stu-id="457c8-111">You can use the **New document** button to create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="457c8-112">I eksemplet i dette emnet er leverandøren Microsoft.</span><span class="sxs-lookup"><span data-stu-id="457c8-112">In the example in this topic, the provider is Microsoft.</span></span> <span data-ttu-id="457c8-113">Du kan også opprette en mal ved å laste opp din egen mal i Excel-format.</span><span class="sxs-lookup"><span data-stu-id="457c8-113">Alternatively, you can create a template by uploading your own template in Excel format.</span></span>


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

<span data-ttu-id="457c8-114">Videoen om hvordan du [oppretter et nytt forretningsdokument ved å bruke Forretningsdokumentbehandling](https://youtu.be/gAIYl-mM_pw) (vist ovenfor) er inkludert i [Finance and Operations-spillelisten](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), som er tilgjengelig på YouTube.</span><span class="sxs-lookup"><span data-stu-id="457c8-114">The [Create a new business document using Business document management](https://youtu.be/gAIYl-mM_pw) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="457c8-115">Gjøre det nye dokumentbrukergrensesnittet i forretningsdokumentadministrering tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="457c8-115">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="457c8-116">Hvis du vil begynne å bruke det nye dokumentbrukergrensesnittet i forretningsdokumentadministrering, må du aktivere **Office-lignende brukergrensesnittopplevelse for forretningsdokumentadministrering**-funksjonen i **Funksjonsadministrering**-arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="457c8-116">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="457c8-117">Følg disse trinnene for å aktivere denne funksjonen for alle juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="457c8-117">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="457c8-118">I **Funksjonsadministrering**-arbeidsområdet, i **Alle**-fanen velger du **Office-lignende brukergrensesnittopplevelse for forretningsdokumentadministrering**-funksjonen i listen.</span><span class="sxs-lookup"><span data-stu-id="457c8-118">In the **Feature management** workspace, on the **All** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="457c8-119">Velg **Aktiver nå** for å aktivere den valgte funksjonen.</span><span class="sxs-lookup"><span data-stu-id="457c8-119">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="457c8-120">Oppdater siden for å få tilgang til den nye funksjonen.</span><span class="sxs-lookup"><span data-stu-id="457c8-120">Refresh the page to access the new feature.</span></span>

## <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="457c8-121">Redigere maler som eies av andre leverandører</span><span class="sxs-lookup"><span data-stu-id="457c8-121">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="457c8-122">I **Forretningsdokumentadministrering**-arbeidsområdet velger du **Nytt dokument**.</span><span class="sxs-lookup"><span data-stu-id="457c8-122">In the **Business document management** workspace, select **New document**.</span></span>

    ![Arbeidsområdet Administrasjon av forretningsdokument](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="457c8-124">På **Velg**-fanen velger du dokumentet som skal brukes som mal, og velger deretter **Opprett dokument**.</span><span class="sxs-lookup"><span data-stu-id="457c8-124">On the **Select** tab, select the document to use as a template, and then select **Create document**.</span></span>

    ![Forretningsdokumenter-dialogboksen](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="457c8-126">I den nye dialogboksen, i **Tittel**-feltet endrer du tittelen etter behov.</span><span class="sxs-lookup"><span data-stu-id="457c8-126">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="457c8-127">Tittelteksten brukes til å navngi den nye ER-formatkonfigurasjonen som opprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="457c8-127">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="457c8-128">Utkastversjonen av denne konfigurasjonen (**Kopi av FTI-kunderapport (GER)**) vil inneholde den redigerte malen og vil bli brukt til å kjøre dette ER-formatet for den gjeldende brukeren.</span><span class="sxs-lookup"><span data-stu-id="457c8-128">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="457c8-129">Den opprinnelige malen fra den grunnleggende ER-formatkonfigurasjonen vil bli brukt til å kjøre dette ER-formatet for alle andre brukere.</span><span class="sxs-lookup"><span data-stu-id="457c8-129">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="457c8-130">I **Navn** -feltet endrer du navnet på den første revisjonen av den redigerbare malen som skal opprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="457c8-130">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="457c8-131">I **Kommentar**-feltet oppdater du merknadene for revisjonen av den redigerbare malen som opprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="457c8-131">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="457c8-132">Velg **OK** for å bekrefte starten på redigeringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="457c8-132">Select **OK** to confirm the start of the editing process.</span></span>

    ![Dokumentopprettelse-dialogboksen](./media/BDM_overview_new_template3.png)

<span data-ttu-id="457c8-134">**Nytt dokument**-knappen brukes til å opprette og redigere en mal i en ER-formatkonfigurasjon som leveres av en annen leverandør.</span><span class="sxs-lookup"><span data-stu-id="457c8-134">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="457c8-135">I dette eksemplet er leverandøren Microsoft.</span><span class="sxs-lookup"><span data-stu-id="457c8-135">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="457c8-136">Når du velger **Nytt dokument**, kan du vise alle malene som eies av gjeldende leverandør og andre leverandører.</span><span class="sxs-lookup"><span data-stu-id="457c8-136">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="457c8-137">Når du har valgt malen, åpnes den for redigering.</span><span class="sxs-lookup"><span data-stu-id="457c8-137">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="457c8-138">Den redigerte malen blir deretter lagret i en ny ER-formatkonfigurasjon som genereres automatisk.</span><span class="sxs-lookup"><span data-stu-id="457c8-138">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a><span data-ttu-id="457c8-139">Last opp en mal som bruker et eksisterende Excel-format</span><span class="sxs-lookup"><span data-stu-id="457c8-139">Upload a template that uses an existing Excel format</span></span>
<span data-ttu-id="457c8-140">Følg denne fremgangsmåten for å oppgi nødvendig informasjon før du laster opp en mal.</span><span class="sxs-lookup"><span data-stu-id="457c8-140">Follow these steps to provide required information before you upload a template.</span></span>

1. <span data-ttu-id="457c8-141">I **Forretningsdokumentadministrering**-arbeidsområdet velger du **Nytt dokument**.</span><span class="sxs-lookup"><span data-stu-id="457c8-141">In the **Business document management** workspace, select **New document**.</span></span>

    ![Arbeidsområdet Administrasjon av forretningsdokument](./media/BDM_overview_new_template1.png)
    
2. <span data-ttu-id="457c8-143">Gå til siden **Opprett en ny mal**, **Last opp**-fanen og deretter **Mal**-fanen, og velg **Bla gjennom** for å søke etter og velge Excel-filen du vil bruke som en mal.</span><span class="sxs-lookup"><span data-stu-id="457c8-143">On the **Create a new template** page, on the **Upload** tab, on the **Template** tab, select **Browse** to find and select the Excel file that you want to use as a template.</span></span> <span data-ttu-id="457c8-144">I **Mal**-delen er feltene **Tittel** og **Beskrivelse** fylt ut automatisk.</span><span class="sxs-lookup"><span data-stu-id="457c8-144">In the **Template** section, the **Title** and **Description** fields are automatically filled in.</span></span> <span data-ttu-id="457c8-145">De angir navnet på og beskrivelsen av den nye ER-formatkonfigurasjonen som opprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="457c8-145">They specify the name and description of the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="457c8-146">Du kan redigere disse feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="457c8-146">You can edit these fields as you require.</span></span>
3. <span data-ttu-id="457c8-147">I **Dokumenttype**-delen i **Navn**-feltet angir du typen forretningsdokument.</span><span class="sxs-lookup"><span data-stu-id="457c8-147">In the **Document Type** section, in the **Name** field, specify the type of business document.</span></span> <span data-ttu-id="457c8-148">Denne verdien brukes til å søke i den riktige datakilden (det vil si ER-modellkonfigurasjonen).</span><span class="sxs-lookup"><span data-stu-id="457c8-148">This value will be used to search the correct data source (that is, the ER model configuration).</span></span>

    ![Mal-fanen](./media/BDM_overview_new_UI_import_21.jpg)

4. <span data-ttu-id="457c8-150">På **Datakilde**-fanen, på hurtigfanen **Filter**, velger du **Bruk filter**.</span><span class="sxs-lookup"><span data-stu-id="457c8-150">On the **Data source** tab, on the **Filter** FastTab, select **Apply filter**.</span></span> <span data-ttu-id="457c8-151">I **Datakilde**-delen fylles **Navn**-feltet ut automatisk, men du kan også velge en verdi manuelt.</span><span class="sxs-lookup"><span data-stu-id="457c8-151">In the **Data source** section, the **Name** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="457c8-152">Du kan bruke filteret til å søke etter riktig datakildenavn etter navn, beskrivelse, kode for land/område og forretningsdokumenttype.</span><span class="sxs-lookup"><span data-stu-id="457c8-152">You can use the filter to search for the appropriate data source name by name, description, country/region code, and business document type.</span></span>

    ![Datakilde-fanen](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > <span data-ttu-id="457c8-154">**Filter**-hurtigfanen brukes til å søke i den riktige datakilden (det vil si ER-modellkonfigurasjonen).</span><span class="sxs-lookup"><span data-stu-id="457c8-154">The **Filter** FastTab is used to search the correct data source (that is, the ER model configuration).</span></span> <span data-ttu-id="457c8-155">Du kan redigere alle filterfelt for å finne den mest relevante datakilden for dokumentet du laster opp.</span><span class="sxs-lookup"><span data-stu-id="457c8-155">You can edit all filter fields to find the most appropriate data source for the document that you're uploading.</span></span>
    > 
    > <span data-ttu-id="457c8-156">Betingelsene på **Filter**-hurtigkategorien brukes som **ELLER**-betingelser.</span><span class="sxs-lookup"><span data-stu-id="457c8-156">The conditions on the **Filter** FastTab are used as **OR** conditions.</span></span>
    
5. <span data-ttu-id="457c8-157">Velg **Registrer automatisk** i **Tilordning**-fanen.</span><span class="sxs-lookup"><span data-stu-id="457c8-157">On the **Mapping** tab, select **Auto detect**.</span></span> <span data-ttu-id="457c8-158">**Rotdefinisjon**-feltet fylles ut automatisk, men du kan også velge en verdi manuelt.</span><span class="sxs-lookup"><span data-stu-id="457c8-158">The **Root definition** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="457c8-159">Denne fanen viser slutttilordningen for elementene fra malen og modellen.</span><span class="sxs-lookup"><span data-stu-id="457c8-159">This tab shows the end mapping for the elements from the template and the model.</span></span>

    ![Tilordning-fanen](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > <span data-ttu-id="457c8-161">Tilordningen i **Malstruktur**-delen bruker hele samsvaret mellom etikettene eller beskrivelsene i datakilden på brukerens språk, og i cellenavnet i malen.</span><span class="sxs-lookup"><span data-stu-id="457c8-161">The mapping in the **Template structure** section uses the full match of the labels or descriptions in the data source in the user's language, and in the cell name in the template.</span></span>

6. <span data-ttu-id="457c8-162">Velg **Opprett dokument** for å bekrefte at du vil opprette en mal og starte redigeringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="457c8-162">Select **Create document** to confirm that you want to create a template and start the editing process.</span></span>

<span data-ttu-id="457c8-163">Hvis du vil ha mer informasjon, kan du se [Oversikt over forretningsdokumentadministrering](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="457c8-163">For more information, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="457c8-164">Hvis det ikke finnes leverandør i Elektronisk rapportering, kan du opprette en.</span><span class="sxs-lookup"><span data-stu-id="457c8-164">If there isn't a provider in Electronic reporting, you can create one.</span></span> <span data-ttu-id="457c8-165">Hvis det ikke finnes en aktiv leverandør, kan du velge å aktivere en.</span><span class="sxs-lookup"><span data-stu-id="457c8-165">If there's no active provider, you can select to activate one.</span></span>

- <span data-ttu-id="457c8-166">Hvis du vil opprette en leverandør, endrer du navnet på leverandøren i **Navn**-feltet, oppdaterer Internett-adressen til den nye leverandøren i feltet **Internett-adresse** og velger **OK** for å bekrefte.</span><span class="sxs-lookup"><span data-stu-id="457c8-166">To create a provider, change the name of the provider in the **Name** field, update the internet address of the new provider in the **Internet address** field, and select **OK** to confirm.</span></span>

    ![Opprette ny leverandør i BDM](./media/bdm_create_provider.png)
    
- <span data-ttu-id="457c8-168">Hvis du vil aktivere eksisterende leverandør, velger du navnet på leverandøren i **Konfigurasjonsleverandør**-feltet, og velger **OK** for å angi leverandøren som aktiv.</span><span class="sxs-lookup"><span data-stu-id="457c8-168">To activate existing provider, choose the name of the provider in the **Configuration provider** field, and select **OK** to set provider as active.</span></span>

    ![Aktivere leverandør i BDM](./media/bdm_choose_provider.png)

> [!NOTE]
> <span data-ttu-id="457c8-170">Hver BDM-mal refererer til leverandøren som forfatteren av konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="457c8-170">Each BDM template refers to the provider as the author of the configuration.</span></span> <span data-ttu-id="457c8-171">Dette er årsaken til hvorfor en aktiv leverandør er nødvendig for malen.</span><span class="sxs-lookup"><span data-stu-id="457c8-171">This is why an active provider is required for the template.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
