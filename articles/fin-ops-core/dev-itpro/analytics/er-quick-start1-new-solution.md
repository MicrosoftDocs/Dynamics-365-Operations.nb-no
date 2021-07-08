---
title: Utforme en ny ER-løsning for å skrive ut en egendefinert rapport
description: Dette emnet forklarer hvordan du utformer en ER-løsning (elektronisk rapportering) for å skrive ut en egendefinert rapport.
author: NickSelin
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90e5381c2d30753e3ad82a38d7361b411f1d7a87
ms.sourcegitcommit: 3673eeca1ada0f3e4ec277176515a946706f8a41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304399"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a><span data-ttu-id="3752d-103">Utforme en ny ER-løsning for å skrive ut en egendefinert rapport</span><span class="sxs-lookup"><span data-stu-id="3752d-103">Design a new ER solution to print a custom report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3752d-104">De følgende trinnene forklarer hvordan en bruker en rolle som systemansvarlig, utvikler av elektronisk rapportering eller funksjonskonsulent for elektronisk rapportering kan konfigurere parametere for ER-rammeverket, utforme nødvendige ER-konfigurasjoner for en ny ER-løsning for å få tilgang til dataene i et bestemt forretningsdomene og generere en egendefinert rapport i Microsoft Office-format.</span><span class="sxs-lookup"><span data-stu-id="3752d-104">The following steps explain how a user in the System Administrator, Electronic Reporting Developer, or Electronic Reporting Functional Consultant role can configure parameters of the ER framework, design the required ER configurations of a new ER solution to access the data of a particular business domain, and generate a custom report in Microsoft Office format.</span></span> <span data-ttu-id="3752d-105">Denne fremgangsmåten kan gjennomføres i firmaet **USMF**.</span><span class="sxs-lookup"><span data-stu-id="3752d-105">These steps can be completed in the **USMF** company.</span></span>

- [<span data-ttu-id="3752d-106">Konfigurere ER-rammeverket</span><span class="sxs-lookup"><span data-stu-id="3752d-106">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="3752d-107">Konfigurere ER-parametere</span><span class="sxs-lookup"><span data-stu-id="3752d-107">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="3752d-108">Aktivere en ER-konfigurasjonsleverandør</span><span class="sxs-lookup"><span data-stu-id="3752d-108">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="3752d-109">Se gjennom listen over ER-konfigurasjonsleverandører</span><span class="sxs-lookup"><span data-stu-id="3752d-109">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="3752d-110">Legg til en ny ER-konfigurasjonsleverandør</span><span class="sxs-lookup"><span data-stu-id="3752d-110">Add a new ER configuration provider</span></span>](#AddProvider)
        - [<span data-ttu-id="3752d-111">Aktivere en ER-konfigurasjonsleverandør</span><span class="sxs-lookup"><span data-stu-id="3752d-111">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="3752d-112">Utforme en domenespesifikk datamodell</span><span class="sxs-lookup"><span data-stu-id="3752d-112">Design a domain-specific data model</span></span>](#DesignModel)

    - [<span data-ttu-id="3752d-113">Importere en ny datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3752d-113">Import a new data model configuration</span></span>](#ImportDataModel)
    - [<span data-ttu-id="3752d-114">Opprett en ny datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3752d-114">Create a new data model configuration</span></span>](#DesignDataModel)

        - [<span data-ttu-id="3752d-115">Gi navn til datamodellen</span><span class="sxs-lookup"><span data-stu-id="3752d-115">Name the data model</span></span>](#NameDataModel)
        - [<span data-ttu-id="3752d-116">Legge til datamodellfelt</span><span class="sxs-lookup"><span data-stu-id="3752d-116">Add data model fields</span></span>](#FieldsEntry)
        - [<span data-ttu-id="3752d-117">Fullføre utformingen av datamodellen</span><span class="sxs-lookup"><span data-stu-id="3752d-117">Complete the design of the data model</span></span>](#CompleteDataModel)

- [<span data-ttu-id="3752d-118">Utforme en modelltilordning for den konfigurerte datamodellen</span><span class="sxs-lookup"><span data-stu-id="3752d-118">Design a model mapping for the configured data model</span></span>](#DesignMapping)

    - [<span data-ttu-id="3752d-119">Importere en ny modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3752d-119">Import a new model mapping configuration</span></span>](#ImportModelMapping)
    - [<span data-ttu-id="3752d-120">Opprette en ny modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3752d-120">Create a new model mapping configuration</span></span>](#CreateModelMapping)

        - [<span data-ttu-id="3752d-121">Utforme en ny modelltilordningskomponent</span><span class="sxs-lookup"><span data-stu-id="3752d-121">Design a new model mapping component</span></span>](#DesignMappingComponent)
        - [<span data-ttu-id="3752d-122">Legge til datakilder for å få tilgang til apptabeller</span><span class="sxs-lookup"><span data-stu-id="3752d-122">Add data sources to access application tables</span></span>](#AddMmDataSource1)
        - [<span data-ttu-id="3752d-123">Legge til datakilder for å få tilgang til appopplistinger</span><span class="sxs-lookup"><span data-stu-id="3752d-123">Add data sources to access application enumerations</span></span>](#AddMmDataSource2)
        - [<span data-ttu-id="3752d-124">Legge til ER-etiketter for å generere en rapport på et angitt språk</span><span class="sxs-lookup"><span data-stu-id="3752d-124">Add ER labels to generate a report in a specified language</span></span>](#AddMmLabels)
        - [<span data-ttu-id="3752d-125">Legge til en datakilde for å transformere resultatene av å sammenligne opplistingsverdier med en tekstverdi</span><span class="sxs-lookup"><span data-stu-id="3752d-125">Add a data source to transform the results of comparing enumeration values to a text value</span></span>](#AddMmDataSource3)
        - [<span data-ttu-id="3752d-126">Binde datakilder til datamodellfelt</span><span class="sxs-lookup"><span data-stu-id="3752d-126">Bind data sources to data model fields</span></span>](#AddMmBindings1)
        - [<span data-ttu-id="3752d-127">Fullføre utformingen av modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="3752d-127">Complete the design of the model mapping</span></span>](#CompleteModelMapping)

- [<span data-ttu-id="3752d-128">Utforme en mal for en egendefinert rapport</span><span class="sxs-lookup"><span data-stu-id="3752d-128">Design a template for a custom report</span></span>](#DesignReportTemplate)
- [<span data-ttu-id="3752d-129">Utforme et format</span><span class="sxs-lookup"><span data-stu-id="3752d-129">Design a format</span></span>](#DesignFormat)

    - [<span data-ttu-id="3752d-130">Importere en konstruert formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3752d-130">Import a designed format configuration</span></span>](#FormatImport)
    - [<span data-ttu-id="3752d-131">Opprette en ny formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3752d-131">Create a new format configuration</span></span>](#FormatCreate)

        - [<span data-ttu-id="3752d-132">Importere en rapportmal</span><span class="sxs-lookup"><span data-stu-id="3752d-132">Import a report template</span></span>](#ImportReportTemplate)
        - [<span data-ttu-id="3752d-133">Konfigurere et format</span><span class="sxs-lookup"><span data-stu-id="3752d-133">Configure a format</span></span>](#ConfigureFormat)
        - [<span data-ttu-id="3752d-134">Definere databinding for en rapporttittel</span><span class="sxs-lookup"><span data-stu-id="3752d-134">Define the data binding for a report title</span></span>](#DefineFormatBindings)
        - [<span data-ttu-id="3752d-135">Gå gjennom modelldatakilden</span><span class="sxs-lookup"><span data-stu-id="3752d-135">Review the model data source</span></span>](#ReviewModelDataSource)
        - [<span data-ttu-id="3752d-136">Binde formatelementer til datakildefelt</span><span class="sxs-lookup"><span data-stu-id="3752d-136">Bind format elements to data source fields</span></span>](#BindFormatElements)

    - [<span data-ttu-id="3752d-137">Kjøre et designet format fra ER</span><span class="sxs-lookup"><span data-stu-id="3752d-137">Run a designed format from ER</span></span>](#RunFormatFromER)

- [<span data-ttu-id="3752d-138">Justere et designet format</span><span class="sxs-lookup"><span data-stu-id="3752d-138">Tune a designed format</span></span>](#TuneFormat)

    - [<span data-ttu-id="3752d-139">Endre et format for å endre navnet på et generert dokument</span><span class="sxs-lookup"><span data-stu-id="3752d-139">Modify a format to change the name of a generated document</span></span>](#ModifyToChangeName)
    - [<span data-ttu-id="3752d-140">Endre et format for å endre rekkefølgen på spørsmål</span><span class="sxs-lookup"><span data-stu-id="3752d-140">Modify a format to change the order of questions</span></span>](#ModifyToOrder)
    - [<span data-ttu-id="3752d-141">Kjøre et endret format fra ER</span><span class="sxs-lookup"><span data-stu-id="3752d-141">Run a modified format from ER</span></span>](#RunFormatFromER2)
    - [<span data-ttu-id="3752d-142">Fullføre formatutformingen</span><span class="sxs-lookup"><span data-stu-id="3752d-142">Complete the format design</span></span>](#CompleteFormat)

- [<span data-ttu-id="3752d-143">Utarbeide appartefakter for å kalle den utformede rapporten</span><span class="sxs-lookup"><span data-stu-id="3752d-143">Develop application artefacts to call the designed report</span></span>](#DevelopCustomCode)

    - [<span data-ttu-id="3752d-144">Endre kildekode</span><span class="sxs-lookup"><span data-stu-id="3752d-144">Modify source code</span></span>](#ModifySourceCode)

        - [<span data-ttu-id="3752d-145">Legge til en datakontraktklasse</span><span class="sxs-lookup"><span data-stu-id="3752d-145">Add a data contract class</span></span>](#DataContractClass)
        - [<span data-ttu-id="3752d-146">Legge til en grensesnittbyggerklasse</span><span class="sxs-lookup"><span data-stu-id="3752d-146">Add a UI builder class</span></span>](#UIBuilderClass)
        - [<span data-ttu-id="3752d-147">Legge til en dataleverandørklasse</span><span class="sxs-lookup"><span data-stu-id="3752d-147">Add a data provider class</span></span>](#DataProviderClass)
        - [<span data-ttu-id="3752d-148">Legge til en etikettfil</span><span class="sxs-lookup"><span data-stu-id="3752d-148">Add a labels file</span></span>](#LabelsFile)
        - [<span data-ttu-id="3752d-149">Legge til en rapporttjenesteklasse</span><span class="sxs-lookup"><span data-stu-id="3752d-149">Add a report service class</span></span>](#ServiceClass)
        - [<span data-ttu-id="3752d-150">Legge til en rapportkontrollerklasse</span><span class="sxs-lookup"><span data-stu-id="3752d-150">Add a report controller class</span></span>](#ControllerClass)
        - [<span data-ttu-id="3752d-151">Legge til et menyelement</span><span class="sxs-lookup"><span data-stu-id="3752d-151">Add a menu item</span></span>](#MenuItem)
        - [<span data-ttu-id="3752d-152">Legge til et menyelement i en meny</span><span class="sxs-lookup"><span data-stu-id="3752d-152">Add a menu item to a menu</span></span>](#Menu)
        - [<span data-ttu-id="3752d-153">Bygge et Visual Studio-prosjekt</span><span class="sxs-lookup"><span data-stu-id="3752d-153">Build a Visual Studio project</span></span>](#BuildVSProject)

    - [<span data-ttu-id="3752d-154">Kjøre et format fra appen</span><span class="sxs-lookup"><span data-stu-id="3752d-154">Run a format from the application</span></span>](#RunFormatFromApp)

- [<span data-ttu-id="3752d-155">Justere en utviklet ER-løsning</span><span class="sxs-lookup"><span data-stu-id="3752d-155">Tune a designed ER solution</span></span>](#TuneSolution)

    - [<span data-ttu-id="3752d-156">Endre en modelltilordning</span><span class="sxs-lookup"><span data-stu-id="3752d-156">Modify a model mapping</span></span>](#ModifyModelMapping)

        - [<span data-ttu-id="3752d-157">Legge til datakilder for å få tilgang til et datakontraktobjekt</span><span class="sxs-lookup"><span data-stu-id="3752d-157">Add data sources to access a data contract object</span></span>](#AddDataSource1)
        - [<span data-ttu-id="3752d-158">Legge til en datakilde for å få tilgang til ER-formattilordningsposter</span><span class="sxs-lookup"><span data-stu-id="3752d-158">Add a data source to access ER format mapping records</span></span>](#AddDataSource2)
        - [<span data-ttu-id="3752d-159">Legge til en datakilde for å få tilgang til en formattilordningspost for et kjørende ER-format</span><span class="sxs-lookup"><span data-stu-id="3752d-159">Add a data source to access a format mapping record of a running ER format</span></span>](#AddDataSource3)
        - [<span data-ttu-id="3752d-160">Angi navnet på det kjørende ER-formatet i datamodellen</span><span class="sxs-lookup"><span data-stu-id="3752d-160">Enter the name of the running ER format in the data model</span></span>](#AddBinding)
        - [<span data-ttu-id="3752d-161">Fullføre utformingen av modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="3752d-161">Complete the design of the model mapping</span></span>](#CompleteModelMapping2)

    - [<span data-ttu-id="3752d-162">Endre et format</span><span class="sxs-lookup"><span data-stu-id="3752d-162">Modify a format</span></span>](#ModifyFormat)

        - [<span data-ttu-id="3752d-163">Legge til et nytt formatelement</span><span class="sxs-lookup"><span data-stu-id="3752d-163">Add a new format element</span></span>](#AddFormatElement)
        - [<span data-ttu-id="3752d-164">Binde formatelementet som er lagt til</span><span class="sxs-lookup"><span data-stu-id="3752d-164">Bind the added format element</span></span>](#BindAddedFormatElement)
        - [<span data-ttu-id="3752d-165">Fullføre formatutformingen</span><span class="sxs-lookup"><span data-stu-id="3752d-165">Complete the format design</span></span>](#CompleteFormat2)

    - [<span data-ttu-id="3752d-166">Kjøre et format fra appen</span><span class="sxs-lookup"><span data-stu-id="3752d-166">Run a format from the application</span></span>](#RunFormatFromApp2)
    - [<span data-ttu-id="3752d-167">Kjøre et format fra ER</span><span class="sxs-lookup"><span data-stu-id="3752d-167">Run a format from ER</span></span>](#RunFormatFromER3)
    - [<span data-ttu-id="3752d-168">Konfigurere et formatmål for forhåndsvisning på skjermen</span><span class="sxs-lookup"><span data-stu-id="3752d-168">Configure a format destination for on-screen preview</span></span>](#ConfigureDestination)
    - [<span data-ttu-id="3752d-169">Kjøre et format fra appen for å forhåndsvise det som et PDF-dokument</span><span class="sxs-lookup"><span data-stu-id="3752d-169">Run a format from the application to preview it as a PDF document</span></span>](#RunFormatFromApp3)

- [<span data-ttu-id="3752d-170">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="3752d-170">Additional resources</span></span>](#References)

<span data-ttu-id="3752d-171">I dette eksemplet skal du opprette en ny ER-løsning for [Spørreskjema](../../../human-resources/hr-learning-questionnaires.md)-modulen.</span><span class="sxs-lookup"><span data-stu-id="3752d-171">In this example, you will create a new ER solution for the [Questionnaire](../../../human-resources/hr-learning-questionnaires.md) module.</span></span> <span data-ttu-id="3752d-172">Denne nye ER-løsningen lar deg utforme en rapport ved å bruke et Microsoft Excel-regneark som en mal.</span><span class="sxs-lookup"><span data-stu-id="3752d-172">This new ER solution lets you design a report by using a Microsoft Excel worksheet as a template.</span></span> <span data-ttu-id="3752d-173">Deretter kan du generere **Spørreskjema**-rapporten i Excel- eller PDF-format, i tillegg til å generere den eksisterende SQL Server Reporting Services-rapporten (SSRS).</span><span class="sxs-lookup"><span data-stu-id="3752d-173">You can then generate the **Questionnaire** report in Excel or PDF format, in addition to generating the existing SQL Server Reporting Services (SSRS) report.</span></span> <span data-ttu-id="3752d-174">Du kan også endre den nye rapporten senere på forespørsel.</span><span class="sxs-lookup"><span data-stu-id="3752d-174">You can also modify the new report later, upon request.</span></span> <span data-ttu-id="3752d-175">Ingen koding er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="3752d-175">No coding is required.</span></span>

1. <span data-ttu-id="3752d-176">Hvis du vil kjøre den eksisterende rapporten, går du til **Spørreskjema** \> **Utforming** \> **Spørreskjemaer-rapporten**.</span><span class="sxs-lookup"><span data-stu-id="3752d-176">To run the existing report, go to **Questionnaire** \> **Design** \> **Questionnaires report**.</span></span>

    ![Velge menyelementet Spørreskjemaer-rapport i Spørreskjema-modulen for å kjøre den eksisterende SSRS-rapporten](./media/er-quick-start1-application-menu-origin.png)

2. <span data-ttu-id="3752d-178">I dialogboksen **Spørreskjemaer-rapport** angir du utvalgskriterier.</span><span class="sxs-lookup"><span data-stu-id="3752d-178">In the **Questionnaires report** dialog box, specify selection criteria.</span></span> <span data-ttu-id="3752d-179">Bruk et filter slik at rapporten bare inneholder **SBCCrsExam**-spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="3752d-179">Apply a filter so that the report includes only the **SBCCrsExam** questionnaire.</span></span>

    ![Angi utvalgskriterier i dialogboksen Spørreskjemaer-rapport](./media/er-quick-start1-ssrs-report-dialog.png)

<span data-ttu-id="3752d-181">Følgende illustrasjon viser den genererte versjonen av SSRS-rapporten for **SBCCrsExam**-spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="3752d-181">The following illustration shows the generated version of the SSRS report for the **SBCCrsExam** questionnaire.</span></span>

![Generert SSRS-rapport](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a><span data-ttu-id="3752d-183">Konfigurere ER-rammeverket</span><span class="sxs-lookup"><span data-stu-id="3752d-183">Configure the ER framework</span></span>

<span data-ttu-id="3752d-184">Som en bruker i rollen som utvikler av elektronisk rapportering må du konfigurere minimumssettet av ER-parametere før du kan begynne å bruke ER-rammeverket til å utforme en ny ER-løsning.</span><span class="sxs-lookup"><span data-stu-id="3752d-184">As a user in the Electronic Reporting Developer role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design your new ER solution.</span></span>

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a><span data-ttu-id="3752d-185">Konfigurere ER-parametere</span><span class="sxs-lookup"><span data-stu-id="3752d-185">Configure ER parameters</span></span>

1. <span data-ttu-id="3752d-186">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="3752d-186">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="3752d-187">I arbeidsområdet **Elektronisk rapportering** velger du **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="3752d-187">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="3752d-188">På **Parametere for elektronisk rapportering**-siden, i **Generelt**-fanen angi **Aktiver utformingsmodus** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3752d-188">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="3752d-189">Angi følgende parametere i fanen **Vedlegg**:</span><span class="sxs-lookup"><span data-stu-id="3752d-189">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="3752d-190">Sett **Konfigurasjoner**-feltet til **Fil** for **USMF**-firmaet.</span><span class="sxs-lookup"><span data-stu-id="3752d-190">Set the **Configurations** field to **File** for the **USMF** company.</span></span>
    - <span data-ttu-id="3752d-191">Sett feltene **Jobbarkiv**, **Midlertidig**, **Grunnlinje** og **Annet** til **Fil**.</span><span class="sxs-lookup"><span data-stu-id="3752d-191">Set **Job archive**, **Temporary**, **Baseline**, and **Others** fields to **File**.</span></span>

<span data-ttu-id="3752d-192">Hvis du vil ha mer informasjon om ER-parametere, kan du se [Konfigurere ER-rammeverket](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3752d-192">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a><span data-ttu-id="3752d-193">Aktivere en ER-konfigurasjonsleverandør</span><span class="sxs-lookup"><span data-stu-id="3752d-193">Activate an ER configuration provider</span></span>

<span data-ttu-id="3752d-194">Hver ER-konfigurasjon er merket som eid av en ER-konfigurasjonsleverandør.</span><span class="sxs-lookup"><span data-stu-id="3752d-194">Every ER configuration is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="3752d-195">Derfor må du aktivere en ER-konfigurasjonsleverandør i **Elektronisk rapportering**-arbeidsområdet før du begynner å legge til eller redigere ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="3752d-195">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit any ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="3752d-196">Bare eieren av en ER-konfigurasjon kan redigere den.</span><span class="sxs-lookup"><span data-stu-id="3752d-196">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="3752d-197">Derfor, før en ER-konfigurasjon kan redigeres, må du aktivere en ER-konfigurasjonsleverandør i **Elektronisk rapportering**-arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="3752d-197">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a><span data-ttu-id="3752d-198">Se gjennom listen over ER-konfigurasjonsleverandører</span><span class="sxs-lookup"><span data-stu-id="3752d-198">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="3752d-199">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="3752d-199">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="3752d-200">I delen **Relaterte koblinger** i arbeidsområdet **Elektronisk rapportering** velger du **Konfigurasjonsleverandører**.</span><span class="sxs-lookup"><span data-stu-id="3752d-200">In the **Electronic reporting** workspace, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="3752d-201">På siden **Konfigurasjonsleverandører** har hver konfigurasjonsleverandørpost et unikt navn og en unik URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="3752d-201">On the **Configuration providers** page, each configuration provider record has a unique name and URL.</span></span> <span data-ttu-id="3752d-202">Se gjennom innholdet på denne siden.</span><span class="sxs-lookup"><span data-stu-id="3752d-202">Review the contents of this page.</span></span> <span data-ttu-id="3752d-203">Hvis det allerede finnes en post for **Litware, Inc.** (`https://www.litware.com`), hopper du over den neste fremgangsmåten og [legger til en ny ER-konfigurasjonsleverandør](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="3752d-203">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a><span data-ttu-id="3752d-204">Legg til en ny ER-konfigurasjonsleverandør</span><span class="sxs-lookup"><span data-stu-id="3752d-204">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="3752d-205">Velg **Ny** på siden **Konfigurasjonsleverandører**.</span><span class="sxs-lookup"><span data-stu-id="3752d-205">On the **Configuration providers** page, select **New**.</span></span>
2. <span data-ttu-id="3752d-206">I **Navn**-feltet angir du **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="3752d-206">In the **Name** field, enter **Litware, Inc.**</span></span>
3. <span data-ttu-id="3752d-207">I **Internett-adresse**-feltet angir du `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="3752d-207">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
4. <span data-ttu-id="3752d-208">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3752d-208">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a><span data-ttu-id="3752d-209">Aktivere en ER-konfigurasjonsleverandør</span><span class="sxs-lookup"><span data-stu-id="3752d-209">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="3752d-210">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="3752d-210">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="3752d-211">I arbeidsområdet **Elektronisk rapportering** velger du konfigurasjonsleverandøren **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="3752d-211">In the **Electronic reporting** workspace, select the **Litware, Inc.** configuration provider.</span></span>
3. <span data-ttu-id="3752d-212">Velg **Angi som aktiv**.</span><span class="sxs-lookup"><span data-stu-id="3752d-212">Select **Set active**.</span></span>

<span data-ttu-id="3752d-213">Hvis du ha mer informasjon om ER-konfigurasjonsleverandører, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="3752d-213">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a><span data-ttu-id="3752d-214">Utforme en domenespesifikk datamodell</span><span class="sxs-lookup"><span data-stu-id="3752d-214">Design a domain-specific data model</span></span>

<span data-ttu-id="3752d-215">Du må opprette en ny ER-konfigurasjon som inneholder en komponent av typen [datamodell](general-electronic-reporting.md#data-model-and-model-mapping-components) for bedriftsdomenet **Spørreskjema**.</span><span class="sxs-lookup"><span data-stu-id="3752d-215">You must create a new ER configuration that contains a [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** business domain.</span></span> <span data-ttu-id="3752d-216">Denne datamodellen vil senere bli brukt som datakilde når du utformer et ER-format for å generere **Spørreskjema**-rapporten.</span><span class="sxs-lookup"><span data-stu-id="3752d-216">This data model will later be used as a data source when you design an ER format to generate the **Questionnaire** report.</span></span>

<span data-ttu-id="3752d-217">Ved å fullføre trinnene under [Importere en ny datamodellkonfigurasjon](#ImportDataModel) kan du importere den nødvendige datamodellen fra den angitte XML-filen.</span><span class="sxs-lookup"><span data-stu-id="3752d-217">By completing the steps in the [Import a new data model configuration](#ImportDataModel) section, you can import the required data model from the provided XML file.</span></span> <span data-ttu-id="3752d-218">Du kan også fullføre trinnene i delen [Opprett en ny datamodellkonfigurasjon](#DesignDataModel) for å utforme denne datamodellen fra grunnen av.</span><span class="sxs-lookup"><span data-stu-id="3752d-218">Alternatively, you can complete the steps in the [Create a new data model configuration](#DesignDataModel) section to design this data model from scratch.</span></span>

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a><span data-ttu-id="3752d-219">Importere en ny datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3752d-219">Import a new data model configuration</span></span>

1. <span data-ttu-id="3752d-220">Last ned filen [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml), og lagre den på den lokale datamaskinen.</span><span class="sxs-lookup"><span data-stu-id="3752d-220">Download the [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="3752d-221">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="3752d-221">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="3752d-222">I arbeidsområdet **Elektronisk rapportering** velger du **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="3752d-222">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="3752d-223">I handlingsruten velger du **Kurs** \> **Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="3752d-223">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="3752d-224">Velg **Bla gjennom**, og finn og velg filen **Questionnaires model.version.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="3752d-224">Select **Browse**, and then find and select the **Questionnaires model.version.1.xml** file.</span></span>
6. <span data-ttu-id="3752d-225">Velg **OK** for å importere konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="3752d-225">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="3752d-226">For å fortsette hopper du over neste prosedyre, [Opprett en ny datamodellkonfigurasjon](#DesignDataModel).</span><span class="sxs-lookup"><span data-stu-id="3752d-226">To continue, skip the next procedure, [Create a new data model configuration](#DesignDataModel).</span></span>

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a><span data-ttu-id="3752d-227">Opprett en ny datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3752d-227">Create a new data model configuration</span></span>

1. <span data-ttu-id="3752d-228">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="3752d-228">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="3752d-229">I arbeidsområdet **Elektronisk rapportering** velger du **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="3752d-229">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="3752d-230">Velg **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="3752d-230">Select **Create configuration**.</span></span>
4. <span data-ttu-id="3752d-231">Skriv inn **Spørreskjemamodell** i **Navn**-feltet i rullegardinboksen.</span><span class="sxs-lookup"><span data-stu-id="3752d-231">In the drop-down dialog box, in the **Name** field, enter **Questionnaire model**.</span></span>
5. <span data-ttu-id="3752d-232">Velg **Opprett konfigurasjon** for å opprette konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="3752d-232">Select **Create configuration** to create the configuration.</span></span>

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a><span data-ttu-id="3752d-233">Gi navn til datamodellen</span><span class="sxs-lookup"><span data-stu-id="3752d-233">Name the data model</span></span>

1. <span data-ttu-id="3752d-234">På **Konfigurasjoner**-siden, i konfigurasjonstreet, velger du **Spørreskjemamodell**.</span><span class="sxs-lookup"><span data-stu-id="3752d-234">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
2. <span data-ttu-id="3752d-235">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="3752d-235">Select **Designer**.</span></span>
3. <span data-ttu-id="3752d-236">På siden **Datamodellutforming**, på hurtigfanen **Generelt**, i **Navn**-feltet, angir du <a name="DataModeName"></a>**Spørreskjemaer**.</span><span class="sxs-lookup"><span data-stu-id="3752d-236">On the **Data model designer** page, on the **General** FastTab, in the **Name** field, enter <a name="DataModeName"></a>**Questionnaires**.</span></span>

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a><span data-ttu-id="3752d-237">Legge til nye datamodellfelt</span><span class="sxs-lookup"><span data-stu-id="3752d-237">Add new data model fields</span></span>

1. <span data-ttu-id="3752d-238">Velg **Ny** på siden **Datamodellutforming**.</span><span class="sxs-lookup"><span data-stu-id="3752d-238">On the **Data model designer** page, select **New**.</span></span>
2. <span data-ttu-id="3752d-239">I dialogboksen for å legge til en datamodellnode gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="3752d-239">In the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="3752d-240">Velg **Modellrot** som typen for den nye noden.</span><span class="sxs-lookup"><span data-stu-id="3752d-240">Select **Model root** as the type of the new node.</span></span>
    2. <span data-ttu-id="3752d-241">I **Navn** feltet skriver du inn <a name="RootDefinitionName"></a>**Rot**.</span><span class="sxs-lookup"><span data-stu-id="3752d-241">In the **Name** field, enter <a name="RootDefinitionName"></a>**Root**.</span></span>
    3. <span data-ttu-id="3752d-242">Velg **Legg til** for å legge til den nye noden.</span><span class="sxs-lookup"><span data-stu-id="3752d-242">Select **Add** to add the new node.</span></span>

    <span data-ttu-id="3752d-243">Denne rotbeskrivelsen vil bli brukt til å angi data for **Spørreskjema**-rapporten.</span><span class="sxs-lookup"><span data-stu-id="3752d-243">This root descriptor will be used to provide data for the **Questionnaire** report.</span></span> <span data-ttu-id="3752d-244">Én enkelt datamodell kan ha flere beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="3752d-244">A single data model can have multiple descriptors.</span></span> <span data-ttu-id="3752d-245">Hver beskrivelse kan angis for ett enkelt ER-format, for å identifisere data som kreves for å generere rapporten.</span><span class="sxs-lookup"><span data-stu-id="3752d-245">Each descriptor can be specified for a single ER format, to identify data that is required to generate the report.</span></span>

3. <span data-ttu-id="3752d-246">Velg **Ny** på nytt, og deretter gjør du følgende i dialogboksen for å legge til en datamodellnode:</span><span class="sxs-lookup"><span data-stu-id="3752d-246">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="3752d-247">Velg **Underordnet for en aktiv node** som typen for den nye noden.</span><span class="sxs-lookup"><span data-stu-id="3752d-247">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="3752d-248">Angi **Bedriftsnavn** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-248">In the **Name** field, enter **CompanyName**.</span></span>
    3. <span data-ttu-id="3752d-249">Velg **Streng** i **Varetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-249">In the **Item type** field, select **String**.</span></span>
    4. <span data-ttu-id="3752d-250">Velg **Legg til** for å legge til det nye feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-250">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="3752d-251">Dette feltet er nødvendig for å overføre navnet på det gjeldende firmaet til en ER-rapport som bruker denne datamodellen som en datakilde.</span><span class="sxs-lookup"><span data-stu-id="3752d-251">This field is required to pass the name of the current company to an ER report that consumes this data model as a data source.</span></span>

4. <span data-ttu-id="3752d-252">Velg **Ny** på nytt, og deretter gjør du følgende i dialogboksen for å legge til en datamodellnode:</span><span class="sxs-lookup"><span data-stu-id="3752d-252">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="3752d-253">Velg **Underordnet for en aktiv node** som typen for den nye noden.</span><span class="sxs-lookup"><span data-stu-id="3752d-253">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="3752d-254">Angi **Spørreskjema** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-254">In the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="3752d-255">Velg **Postliste** i **Varetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-255">In the **Item type** field, select **Record list**.</span></span>
    4. <span data-ttu-id="3752d-256">Velg **Legg til** for å legge til det nye feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-256">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="3752d-257">Dette feltet brukes til å overføre listen over spørreskjemaer til en ER-rapport som bruker denne datamodellen som en datakilde.</span><span class="sxs-lookup"><span data-stu-id="3752d-257">This field will be used to pass the list of questionnaires to an ER report that consumes this data model as a data source.</span></span>

5. <span data-ttu-id="3752d-258">Velg **Spørreskjema**-noden.</span><span class="sxs-lookup"><span data-stu-id="3752d-258">Select the **Questionnaire** node.</span></span>
6. <span data-ttu-id="3752d-259">Fortsett å legge til de nødvendige feltene i den redigerbare datamodellen på samme måte helt til du har fullført den følgende datamodellstrukturen.</span><span class="sxs-lookup"><span data-stu-id="3752d-259">Continue to add the required fields of the editable data model in the same manner until you complete the following data model structure.</span></span>

    | <span data-ttu-id="3752d-260">Feltbane</span><span class="sxs-lookup"><span data-stu-id="3752d-260">Field path</span></span>                                                    | <span data-ttu-id="3752d-261">Datatype</span><span class="sxs-lookup"><span data-stu-id="3752d-261">Data type</span></span>   | <span data-ttu-id="3752d-262">Feltbetegnelse / returnert verdi</span><span class="sxs-lookup"><span data-stu-id="3752d-262">Field designation/returned value</span></span> |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | <span data-ttu-id="3752d-263">Rot</span><span class="sxs-lookup"><span data-stu-id="3752d-263">Root</span></span>                                                          |             | <span data-ttu-id="3752d-264">Referansepunktet for å be om spørreskjemadata.</span><span class="sxs-lookup"><span data-stu-id="3752d-264">The reference point to request questionnaire data.</span></span> |
    | <span data-ttu-id="3752d-265">Root\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="3752d-265">Root\\CompanyName</span></span>                                             | <span data-ttu-id="3752d-266">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-266">String</span></span>      | <span data-ttu-id="3752d-267">Navnet på gjeldende bedrift.</span><span class="sxs-lookup"><span data-stu-id="3752d-267">The name of the current company.</span></span> |
    | <span data-ttu-id="3752d-268">Root\\ExecutionContext</span><span class="sxs-lookup"><span data-stu-id="3752d-268">Root\\ExecutionContext</span></span>                                        | <span data-ttu-id="3752d-269">Registrer</span><span class="sxs-lookup"><span data-stu-id="3752d-269">Record</span></span>      | <span data-ttu-id="3752d-270">Utførelsesdetaljer for formatet.</span><span class="sxs-lookup"><span data-stu-id="3752d-270">Format execution details.</span></span> |
    | <span data-ttu-id="3752d-271">Root\\ExecutionContext\\FormatName</span><span class="sxs-lookup"><span data-stu-id="3752d-271">Root\\ExecutionContext\\FormatName</span></span>                            | <span data-ttu-id="3752d-272">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-272">String</span></span>      | <span data-ttu-id="3752d-273">Navnet på ER-formatet som kjøres.</span><span class="sxs-lookup"><span data-stu-id="3752d-273">The name of the ER format that is being run.</span></span> |
    | <span data-ttu-id="3752d-274">Root\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="3752d-274">Root\\Questionnaire</span></span>                                           | <span data-ttu-id="3752d-275">Postliste</span><span class="sxs-lookup"><span data-stu-id="3752d-275">Record list</span></span> | <span data-ttu-id="3752d-276">Listen over spørreskjemaer</span><span class="sxs-lookup"><span data-stu-id="3752d-276">The list of questionnaires</span></span> |
    | <span data-ttu-id="3752d-277">Root\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="3752d-277">Root\\Questionnaire\\Active</span></span>                                   | <span data-ttu-id="3752d-278">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-278">String</span></span>      | <span data-ttu-id="3752d-279">Status for gjeldende spørreskjema.</span><span class="sxs-lookup"><span data-stu-id="3752d-279">The status of the current questionnaire.</span></span> |
    | <span data-ttu-id="3752d-280">Root\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="3752d-280">Root\\Questionnaire\\Code</span></span>                                     | <span data-ttu-id="3752d-281">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-281">String</span></span>      | <span data-ttu-id="3752d-282">Kode for gjeldende spørreskjema.</span><span class="sxs-lookup"><span data-stu-id="3752d-282">The code of the current questionnaire.</span></span> |
    | <span data-ttu-id="3752d-283">Root\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="3752d-283">Root\\Questionnaire\\Description</span></span>                              | <span data-ttu-id="3752d-284">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-284">String</span></span>      | <span data-ttu-id="3752d-285">Beskrivelse av gjeldende spørreskjema.</span><span class="sxs-lookup"><span data-stu-id="3752d-285">The description of the current questionnaire.</span></span> |
    | <span data-ttu-id="3752d-286">Root\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="3752d-286">Root\\Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="3752d-287">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-287">String</span></span>      | <span data-ttu-id="3752d-288">Typen gjeldende spørreskjema.</span><span class="sxs-lookup"><span data-stu-id="3752d-288">The type of the current questionnaire.</span></span> |
    | <span data-ttu-id="3752d-289">Root\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="3752d-289">Root\\Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="3752d-290">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-290">String</span></span>      | <span data-ttu-id="3752d-291">Den numeriske rekkefølgen for det gjeldende spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="3752d-291">The numerical order of the current questionnaire.</span></span> |
    | <span data-ttu-id="3752d-292">Root\\Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="3752d-292">Root\\Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="3752d-293">Registrer</span><span class="sxs-lookup"><span data-stu-id="3752d-293">Record</span></span>      | <span data-ttu-id="3752d-294">Resultatparameterne for det gjeldende spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="3752d-294">The result parameters of the current questionnaire.</span></span> |
    | <span data-ttu-id="3752d-295">Root\\Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="3752d-295">Root\\Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="3752d-296">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-296">String</span></span>      | <span data-ttu-id="3752d-297">Identifikasjonskoden for den gjeldende resultatgruppen.</span><span class="sxs-lookup"><span data-stu-id="3752d-297">The identification code of the current result group.</span></span> |
    | <span data-ttu-id="3752d-298">Root\\Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="3752d-298">Root\\Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="3752d-299">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-299">String</span></span>      | <span data-ttu-id="3752d-300">Beskrivelse av gjeldende resultatgruppe.</span><span class="sxs-lookup"><span data-stu-id="3752d-300">The description of the current result group.</span></span> |
    | <span data-ttu-id="3752d-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="3752d-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="3752d-302">Kommatall</span><span class="sxs-lookup"><span data-stu-id="3752d-302">Real</span></span>        | <span data-ttu-id="3752d-303">Maksimalt antall poeng som kan oppnås.</span><span class="sxs-lookup"><span data-stu-id="3752d-303">The maximum number of points that could be earned.</span></span> |
    | <span data-ttu-id="3752d-304">Root\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="3752d-304">Root\\Questionnaire\\Question</span></span>                                 | <span data-ttu-id="3752d-305">Postliste</span><span class="sxs-lookup"><span data-stu-id="3752d-305">Record list</span></span> | <span data-ttu-id="3752d-306">Listen over spørsmål for det gjeldende spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="3752d-306">The list of questions for the current questionnaire.</span></span> |
    | <span data-ttu-id="3752d-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="3752d-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="3752d-308">Heltall</span><span class="sxs-lookup"><span data-stu-id="3752d-308">Integer</span></span>     | <span data-ttu-id="3752d-309">Sekvensnummeret for den gjeldende svarsamlingen.</span><span class="sxs-lookup"><span data-stu-id="3752d-309">The sequence number of the current answer collection.</span></span> |
    | <span data-ttu-id="3752d-310">Root\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="3752d-310">Root\\Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="3752d-311">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-311">String</span></span>      | <span data-ttu-id="3752d-312">Identifikasjonskoden for det gjeldende spørsmålet.</span><span class="sxs-lookup"><span data-stu-id="3752d-312">The identification code of the current question.</span></span> |
    | <span data-ttu-id="3752d-313">Root\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="3752d-313">Root\\Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="3752d-314">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-314">String</span></span>      | <span data-ttu-id="3752d-315">Et flagg som angir om det gjeldende spørsmålet må besvares.</span><span class="sxs-lookup"><span data-stu-id="3752d-315">A flag that indicates whether the current question must be answered.</span></span> |
    | <span data-ttu-id="3752d-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="3752d-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="3752d-317">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-317">String</span></span>      | <span data-ttu-id="3752d-318">Et flagg som angir om det gjeldende spørsmålet er primært.</span><span class="sxs-lookup"><span data-stu-id="3752d-318">A flag that indicates whether the current question is primary.</span></span> |
    | <span data-ttu-id="3752d-319">Root\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="3752d-319">Root\\Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="3752d-320">Heltall</span><span class="sxs-lookup"><span data-stu-id="3752d-320">Integer</span></span>     | <span data-ttu-id="3752d-321">Sekvensnummeret for det gjeldende spørsmålet.</span><span class="sxs-lookup"><span data-stu-id="3752d-321">The sequence number of the current question.</span></span> |
    | <span data-ttu-id="3752d-322">Root\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="3752d-322">Root\\Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="3752d-323">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-323">String</span></span>      | <span data-ttu-id="3752d-324">Teksten for det gjeldende spørsmålet.</span><span class="sxs-lookup"><span data-stu-id="3752d-324">The text of the current question.</span></span> |
    | <span data-ttu-id="3752d-325">Root\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="3752d-325">Root\\Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="3752d-326">Postliste</span><span class="sxs-lookup"><span data-stu-id="3752d-326">Record list</span></span> | <span data-ttu-id="3752d-327">Listen over svar for det gjeldende spørsmålet.</span><span class="sxs-lookup"><span data-stu-id="3752d-327">The list of answers for the current question.</span></span> |
    | <span data-ttu-id="3752d-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="3752d-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="3752d-329">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-329">String</span></span>      | <span data-ttu-id="3752d-330">Et flagg som angir om det gjeldende svaret er korrekt.</span><span class="sxs-lookup"><span data-stu-id="3752d-330">A flag that indicates whether the current answer is correct.</span></span> |
    | <span data-ttu-id="3752d-331">Root\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="3752d-331">Root\\Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="3752d-332">Kommatall</span><span class="sxs-lookup"><span data-stu-id="3752d-332">Real</span></span>        | <span data-ttu-id="3752d-333">Poengene som er opptjent når det gjeldende svaret er valgt.</span><span class="sxs-lookup"><span data-stu-id="3752d-333">The points that are earned when the current answer is selected.</span></span> |
    | <span data-ttu-id="3752d-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="3752d-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="3752d-335">Heltall</span><span class="sxs-lookup"><span data-stu-id="3752d-335">Integer</span></span>     | <span data-ttu-id="3752d-336">Sekvensnummeret for det gjeldende svaret.</span><span class="sxs-lookup"><span data-stu-id="3752d-336">The sequence number of the current answer.</span></span> |
    | <span data-ttu-id="3752d-337">Root\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="3752d-337">Root\\Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="3752d-338">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-338">String</span></span>      | <span data-ttu-id="3752d-339">Teksten for det gjeldende svaret.</span><span class="sxs-lookup"><span data-stu-id="3752d-339">The text of the current answer.</span></span> |

    <span data-ttu-id="3752d-340">Følgende illustrasjon viser den fullførte, redigerbare datamodellen på siden **Datamodellutforming**.</span><span class="sxs-lookup"><span data-stu-id="3752d-340">The following illustration shows the completed editable data model on the **Data model designer** page.</span></span>

    ![Konfigurert datamodell i ER-datamodellutforming](./media/er-quick-start1-model2.png)

7. <span data-ttu-id="3752d-342">Lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="3752d-342">Save your changes.</span></span>
8. <span data-ttu-id="3752d-343">Lukk siden **Datamodellutforming**.</span><span class="sxs-lookup"><span data-stu-id="3752d-343">Close the **Data model designer** page.</span></span>

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a><span data-ttu-id="3752d-344">Fullføre utformingen av datamodellen</span><span class="sxs-lookup"><span data-stu-id="3752d-344">Complete the design of the data model</span></span>

1. <span data-ttu-id="3752d-345">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="3752d-345">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="3752d-346">På **Konfigurasjoner**-siden, i konfigurasjonstreet, velger du **Spørreskjemamodell**.</span><span class="sxs-lookup"><span data-stu-id="3752d-346">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="3752d-347">I hurtigfanen **Versjoner** velger du konfigurasjonsversjonen med statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="3752d-347">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="3752d-348">Velg **Endre status** \> **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="3752d-348">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="3752d-349">Statusen til versjon 1 av denne konfigurasjonen endres fra **Utkast** til **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="3752d-349">The status of version 1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="3752d-350">Versjon 1 kan ikke lenger endres.</span><span class="sxs-lookup"><span data-stu-id="3752d-350">Version 1 can no longer be changed.</span></span> <span data-ttu-id="3752d-351">Denne versjonen inneholder den konfigurerte datamodellen og kan brukes som basis for andre ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="3752d-351">This version contains the configured data model and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="3752d-352">Versjon 2 av denne konfigurasjonen opprettes og har statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="3752d-352">Version 2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="3752d-353">Du kan redigere denne versjonen for å justere **Spørreskjema**-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="3752d-353">You can edit this version to adjust the **Questionnaire** data model.</span></span>

![Versjoner av den redigerbare konfigurasjonen på Konfigurasjoner-siden](./media/er-quick-start1-model-configuration.png)

<span data-ttu-id="3752d-355">Hvis du vil ha mer informasjon om versjonskontroll for ERkonfigurasjoner, kan du se [Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md#component-versioning).</span><span class="sxs-lookup"><span data-stu-id="3752d-355">For more information about versioning for ER configurations, see [Electronic reporting (ER) overview](general-electronic-reporting.md#component-versioning).</span></span>

> [!NOTE]
> <span data-ttu-id="3752d-356">Den konfigurerte datamodellen er den abstrakte representasjonen av **Spørreskjema**-bedriftsdomenet og inneholder ingen relasjoner til artefakter som er spesifikke for Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="3752d-356">The configured data model is your abstract representation of the **Questionnaire** business domain and contains no relations to artefacts that are specific to Microsoft Dynamics 365 Finance.</span></span>

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a><span data-ttu-id="3752d-357">Utforme en modelltilordning for den konfigurerte datamodellen</span><span class="sxs-lookup"><span data-stu-id="3752d-357">Design a model mapping for the configured data model</span></span>

<span data-ttu-id="3752d-358">Som en bruker med rollen som utvikler av elektronisk rapportering må du opprette en ny ER-konfigurasjon som inneholder en [modelltilordning](general-electronic-reporting.md#data-model-and-model-mapping-components)-komponent for **Spørreskjema**-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="3752d-358">As a user in the Electronic Reporting Developer role, you must create a new ER configuration that contains a [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** data model.</span></span> <span data-ttu-id="3752d-359">Fordi denne komponenten implementerer den konfigurerte datamodellen for Finance, er den Finance-spesifikk.</span><span class="sxs-lookup"><span data-stu-id="3752d-359">Because this component implements the configured data model for Finance, it's Finance-specific.</span></span> <span data-ttu-id="3752d-360">Du må konfigurere komponenten for modelltilordning for å angi appobjektene som må brukes til å fylle ut den konfigurerte datamodellen med appdata ved kjøring.</span><span class="sxs-lookup"><span data-stu-id="3752d-360">You must configure the model mapping component to specify the application objects that must be used to fill in the configured data model with application data at runtime.</span></span> <span data-ttu-id="3752d-361">For å fullføre denne oppgaven må du være oppmerksom på implementeringsdetaljene for datastrukturen i **Spørreskjema**-bedriftsdomenet i Finance.</span><span class="sxs-lookup"><span data-stu-id="3752d-361">To complete this task, you must be aware of the implementation details of the data structure of the **Questionnaire** business domain in Finance.</span></span>

<span data-ttu-id="3752d-362">Ved å fullføre trinnene under [Importere en ny modelltilordningskonfigurasjon](#ImportModelMapping) som følger, kan du importere den nødvendige modelltilordningskonfigurasjonen fra den angitte XML-filen.</span><span class="sxs-lookup"><span data-stu-id="3752d-362">By completing the steps in the [Import a new model mapping configuration](#ImportModelMapping) section that follows, you can import the required model mapping configuration from the provided XML file.</span></span> <span data-ttu-id="3752d-363">Du kan også fullføre trinnene i delen [Opprette en ny modelltilordningskonfigurasjon](#CreateModelMapping) for å utforme denne modelltilordningen fra grunnen av.</span><span class="sxs-lookup"><span data-stu-id="3752d-363">Alternatively, you can complete the steps in the [Create a new model mapping configuration](#CreateModelMapping) section to design this model mapping from scratch.</span></span>

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a><span data-ttu-id="3752d-364">Importere en ny modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3752d-364">Import a new model mapping configuration</span></span>

1. <span data-ttu-id="3752d-365">Last ned filen [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml), og lagre den på den lokale datamaskinen.</span><span class="sxs-lookup"><span data-stu-id="3752d-365">Download the [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="3752d-366">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="3752d-366">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="3752d-367">I arbeidsområdet **Elektronisk rapportering** velger du **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="3752d-367">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="3752d-368">I handlingsruten velger du **Kurs** \> **Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="3752d-368">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="3752d-369">Velg **Bla gjennom**, og finn og velg filen **Questionnaires mapping.version.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="3752d-369">Select **Browse**, and then find and select the **Questionnaires mapping.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="3752d-370">Velg **OK** for å importere konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="3752d-370">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="3752d-371">For å fortsette hopper du over neste prosedyre, [Opprette en ny modelltilordningskonfigurasjon](#CreateModelMapping).</span><span class="sxs-lookup"><span data-stu-id="3752d-371">To continue, skip the next procedure, [Create a new model mapping configuration](#CreateModelMapping).</span></span>

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a><span data-ttu-id="3752d-372">Opprette en ny modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3752d-372">Create a new model mapping configuration</span></span>

1. <span data-ttu-id="3752d-373">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="3752d-373">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="3752d-374">På **Konfigurasjoner**-siden, i konfigurasjonstreet, velger du **Spørreskjemamodell**.</span><span class="sxs-lookup"><span data-stu-id="3752d-374">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="3752d-375">Velg **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="3752d-375">Select **Create configuration**.</span></span>
4. <span data-ttu-id="3752d-376">Følg disse trinnene i rullegardinboksen:</span><span class="sxs-lookup"><span data-stu-id="3752d-376">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="3752d-377">I feltet **Ny** velger du **Modelltilordning basert på datamodellspørreskjemaer**.</span><span class="sxs-lookup"><span data-stu-id="3752d-377">In the **New** field, select **Model Mapping based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="3752d-378">I **Navn**-feltet angir du **Spørreskjematilordning**.</span><span class="sxs-lookup"><span data-stu-id="3752d-378">In the **Name** field, enter **Questionnaire mapping**.</span></span>
    3. <span data-ttu-id="3752d-379">I feltet **Definisjon av datamodell** velger du **Rot**-definisjonen.</span><span class="sxs-lookup"><span data-stu-id="3752d-379">In the **Data model definition** field, select the **Root** definition.</span></span>
    4. <span data-ttu-id="3752d-380">Velg **Opprett konfigurasjon** for å opprette konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="3752d-380">Select **Create configuration** to create the configuration.</span></span>

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a><span data-ttu-id="3752d-381">Utforme en ny modelltilordningskomponent</span><span class="sxs-lookup"><span data-stu-id="3752d-381">Design a new model mapping component</span></span>

1. <span data-ttu-id="3752d-382">På **Konfigurasjoner**-siden, i konfigurasjonstreet, velger du **Spørreskjematilordning**.</span><span class="sxs-lookup"><span data-stu-id="3752d-382">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
2. <span data-ttu-id="3752d-383">Velg **Utforming** for å åpne listen over tilordninger.</span><span class="sxs-lookup"><span data-stu-id="3752d-383">Select **Designer** to open the list of mappings.</span></span>
3. <span data-ttu-id="3752d-384">Velg tilordningen **Spørreskjematilordning** som ble automatisk lagt til for **Rot**-definisjonen</span><span class="sxs-lookup"><span data-stu-id="3752d-384">Select the **Questionnaires mapping** mapping that was automatically added for the **Root** definition</span></span>
4. <span data-ttu-id="3752d-385">Velg **Utforming** for å begynne å konfigurere den valgte tilordningen.</span><span class="sxs-lookup"><span data-stu-id="3752d-385">Select **Designer** to start to configure the selected mapping.</span></span>

<span data-ttu-id="3752d-386">Det blir automatisk lagt til en ny tilordning for **Rot**-definisjonen.</span><span class="sxs-lookup"><span data-stu-id="3752d-386">A new mapping is automatically added for the **Root** definition.</span></span> <span data-ttu-id="3752d-387">Denne tilordningen har **Til modell**-retningen.</span><span class="sxs-lookup"><span data-stu-id="3752d-387">This mapping has the **To model** direction.</span></span> <span data-ttu-id="3752d-388">Denne tilordningen kan derfor brukes til å fylle ut en datamodell med påkrevde data.</span><span class="sxs-lookup"><span data-stu-id="3752d-388">Therefore, this mapping can be used to fill in a data model with required data.</span></span>

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a><span data-ttu-id="3752d-389">Legge til datakilder for å få tilgang til apptabeller</span><span class="sxs-lookup"><span data-stu-id="3752d-389">Add data sources to access application tables</span></span>

<span data-ttu-id="3752d-390">Du må konfigurere datakilder for å få tilgang til apptabellene som inneholder spørreskjemadetaljer.</span><span class="sxs-lookup"><span data-stu-id="3752d-390">You must configure data sources to access the application tables that contain questionnaire details.</span></span>

1. <span data-ttu-id="3752d-391">På siden **Modelltilordningsutforming**, i ruten **Datakildetyper**, velger du **Dynamics 365 for Operations\\Tabellposter**.</span><span class="sxs-lookup"><span data-stu-id="3752d-391">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="3752d-392">Legg til en ny datakilde som skal brukes for å få tilgang til KMCollection-tabellen, der hver post representerer ett enkelt spørreskjema:</span><span class="sxs-lookup"><span data-stu-id="3752d-392">Add a new data source that will be used to access the KMCollection table, where every record represents a single questionnaire:</span></span>

    1. <span data-ttu-id="3752d-393">I **Datakilder**-ruten velger du **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="3752d-393">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="3752d-394">Skriv inn **Spørreskjema** i **Navn**-feltet i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="3752d-394">In dialog box, in the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="3752d-395">I **Tabell**-feltet angir du **KMCollection**.</span><span class="sxs-lookup"><span data-stu-id="3752d-395">In the **Table** field, enter **KMCollection**.</span></span>
    4. <span data-ttu-id="3752d-396">Sett alternativet **Be om spørring** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3752d-396">Set the **Ask for query** option to **Yes**.</span></span> <span data-ttu-id="3752d-397">Du kan deretter angi alternativer for [filtrering](../../fin-ops/get-started/advanced-filtering-query-options.md) for denne tabellen i dialogboksen for systemspørring ved kjøring.</span><span class="sxs-lookup"><span data-stu-id="3752d-397">You will then be able to specify [filtering](../../fin-ops/get-started/advanced-filtering-query-options.md) options for this table in the system query dialog box at runtime.</span></span>
    5. <span data-ttu-id="3752d-398">Velg **OK** for å legge til den nye datakilden.</span><span class="sxs-lookup"><span data-stu-id="3752d-398">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="3752d-399">I ruten **Datakildetyper** velger du **Dynamics 365 for Operations\\Tabellposter**.</span><span class="sxs-lookup"><span data-stu-id="3752d-399">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
4. <span data-ttu-id="3752d-400">Legg til en ny datakilde som skal brukes for å få tilgang til KMQuestion-tabellen, der hver post representerer ett enkelt spørsmål på et spørreskjema:</span><span class="sxs-lookup"><span data-stu-id="3752d-400">Add a new data source that will be used to access the KMQuestion table, where every record represents a single question in a questionnaire:</span></span>

    1. <span data-ttu-id="3752d-401">I **Datakilder**-ruten velger du **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="3752d-401">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="3752d-402">Skriv inn **Spørsmål** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-402">In the dialog box, in the **Name** field, enter **Question**.</span></span>
    3. <span data-ttu-id="3752d-403">I **Tabell**-feltet angir du **KMQuestion**.</span><span class="sxs-lookup"><span data-stu-id="3752d-403">In the **Table** field, enter **KMQuestion**.</span></span>
    4. <span data-ttu-id="3752d-404">Velg **OK** for å legge til den nye datakilden.</span><span class="sxs-lookup"><span data-stu-id="3752d-404">Select **OK** to add the new data source.</span></span>

5. <span data-ttu-id="3752d-405">I ruten **Datakildetyper** velger du **Dynamics 365 for Operations\\Tabellposter**.</span><span class="sxs-lookup"><span data-stu-id="3752d-405">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
6. <span data-ttu-id="3752d-406">Legg til et nytt datakildeforsøk som skal brukes for å få tilgang til KMAnswer-tabellen, der hver post representerer ett enkelt svar på et spørsmål på et spørreskjema:</span><span class="sxs-lookup"><span data-stu-id="3752d-406">Add a new data source try that will be used to access the KMAnswer table, where every record represents a single answer to a question in a questionnaire:</span></span>

    1. <span data-ttu-id="3752d-407">I **Datakilder**-ruten velger du **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="3752d-407">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="3752d-408">Angi **Svar** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-408">In the **Name** field, enter **Answer**.</span></span>
    3. <span data-ttu-id="3752d-409">I **Tabell**-feltet angir du **KMAnswer**.</span><span class="sxs-lookup"><span data-stu-id="3752d-409">In the **Table** field, enter **KMAnswer**.</span></span>
    4. <span data-ttu-id="3752d-410">Velg **OK** for å legge til den nye datakilden.</span><span class="sxs-lookup"><span data-stu-id="3752d-410">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="3752d-411">I ruten **Datakildetyper** velger du **Funksjoner\\Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="3752d-411">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="3752d-412">Legg til et nytt beregnet felt som skal brukes til å få tilgang til en post i KMQuestionResultGroup-tabellen fra hver post i den overordnede KMCollection-tabellen:</span><span class="sxs-lookup"><span data-stu-id="3752d-412">Add a new calculated field that will be used to access a record of the KMQuestionResultGroup table from every record of the parent KMCollection table:</span></span>

    1. <span data-ttu-id="3752d-413">I **Datakilder**-ruten velger du **Spørreskjema**.</span><span class="sxs-lookup"><span data-stu-id="3752d-413">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="3752d-414">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="3752d-414">Select **Add**.</span></span>
    3. <span data-ttu-id="3752d-415">Angi **\$ResultGroup** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-415">In the dialog box, in the **Name** field, enter **\$ResultGroup**.</span></span>
    4. <span data-ttu-id="3752d-416">Velg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="3752d-416">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="3752d-417">I [ER-formelredigeringsprogram](general-electronic-reporting-formula-designer.md), i **Formel**-feltet, angir du **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** til å bruke [banen](er-formula-language.md#Paths) til én-til-mange-relasjonen mellom tabellene KMCollection og KMQuestionResultGroup.</span><span class="sxs-lookup"><span data-stu-id="3752d-417">In the [ER formula editor](general-electronic-reporting-formula-designer.md), in the **Formula** field, enter **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** to use the [path](er-formula-language.md#Paths) of the one-to-many relation between the KMCollection and KMQuestionResultGroup tables.</span></span>
    6. <span data-ttu-id="3752d-418">Velg **Lagre**, og lukk formelredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="3752d-418">Select **Save**, and close the formula editor.</span></span>
    7. <span data-ttu-id="3752d-419">Velg **OK** for å legge til det nye beregnede feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-419">Select **OK** to add the new calculated field.</span></span>

9. <span data-ttu-id="3752d-420">I ruten **Datakildetyper** velger du **Funksjoner\\Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="3752d-420">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
10. <span data-ttu-id="3752d-421">Legg til et nytt beregnet felt som skal brukes til å få tilgang til spørsmålsposter i KMQuestion-tabellen fra hver post i den overordnede KMCollectionQuestion-tabellen:</span><span class="sxs-lookup"><span data-stu-id="3752d-421">Add a new calculated field that will be used to access question records of the KMQuestion table from every record of the parent KMCollectionQuestion table:</span></span>

    1. <span data-ttu-id="3752d-422">I **Datakilder**-ruten velger du **Spørreskjema**.</span><span class="sxs-lookup"><span data-stu-id="3752d-422">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="3752d-423">Utvid **\<Relasjoner**-noden som inneholder én-til-mange-relasjoner fra KMCollection-tabellen.</span><span class="sxs-lookup"><span data-stu-id="3752d-423">Expand the **\<Relations** node that contains one-to-many relations of the KMCollection table.</span></span>
    3. <span data-ttu-id="3752d-424">Velg den tilknyttede **KMCollectionQuestion**-tabellen, og velg deretter **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="3752d-424">Select the related **KMCollectionQuestion** table, and then select **Add**.</span></span>
    4. <span data-ttu-id="3752d-425">Skriv inn **\$Question** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-425">In the dialog box, in the **Name** field, enter **\$Question**.</span></span>
    5. <span data-ttu-id="3752d-426">Velg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="3752d-426">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="3752d-427">I formelredigeringsprogrammet, i **Formel**-feltet, angir du **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** for å returnere de aktuelle spørsmålspostene fra KMQuestion-tabellen.</span><span class="sxs-lookup"><span data-stu-id="3752d-427">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** to return the appropriate question records from the KMQuestion table.</span></span>
    7. <span data-ttu-id="3752d-428">Velg **Lagre**, og lukk formelredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="3752d-428">Select **Save**, and close the formula editor.</span></span>
    8. <span data-ttu-id="3752d-429">Velg **OK** for å legge til det nye beregnede feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-429">Select **OK** to add the new calculated field.</span></span>

11. <span data-ttu-id="3752d-430">I ruten **Datakildetyper** velger du **Funksjoner\\Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="3752d-430">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
12. <span data-ttu-id="3752d-431">Legg til et nytt beregnet felt som skal brukes til å få tilgang til svarposter i KMAnswer-tabellen fra hver post i den overordnede KMQuestion-tabellen:</span><span class="sxs-lookup"><span data-stu-id="3752d-431">Add a new calculated field that will be used to access answer records of the KMAnswer table from every record of the parent KMQuestion table:</span></span>

    1. <span data-ttu-id="3752d-432">I **Datakilder**-ruten velger du **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, og velg deretter **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="3752d-432">In the **Data sources** pane, select **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, and then select **Add**.</span></span>
    2. <span data-ttu-id="3752d-433">Skriv inn **\$Answer** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-433">In the dialog box, in the **Name** field, enter **\$Answer**.</span></span>
    3. <span data-ttu-id="3752d-434">Velg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="3752d-434">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="3752d-435">I formelredigeringsprogrammet, i **Formel**-feltet, angir du **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** for å returnere de aktuelle svarpostene fra KMAnswer-tabellen.</span><span class="sxs-lookup"><span data-stu-id="3752d-435">In the formula editor, in the **Formula** field, enter **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** to return the appropriate answer records from the KMAnswer table.</span></span>
    5. <span data-ttu-id="3752d-436">Velg **Lagre**, og lukk formelredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="3752d-436">Select **Save**, and close the formula editor.</span></span>
    6. <span data-ttu-id="3752d-437">Velg **OK** for å legge til det nye beregnede feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-437">Select **OK** to add the new calculated field.</span></span>

13. <span data-ttu-id="3752d-438">I ruten **Datakildetyper** velger du **Dynamics 365 for Operations\\Tabell**.</span><span class="sxs-lookup"><span data-stu-id="3752d-438">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table**.</span></span>
14. <span data-ttu-id="3752d-439">Legg til en ny datakilde som skal brukes til å få tilgang til metoder i CompanyInfo-tabellen.</span><span class="sxs-lookup"><span data-stu-id="3752d-439">Add a new data source that will be used to access methods of the CompanyInfo table.</span></span> <span data-ttu-id="3752d-440">Legg merke til at **find()**-metoden for denne tabellen returnerer en post som representerer et firma for gjeldende Finance-forekomst, som denne tilordningen kalles i sammenheng med.</span><span class="sxs-lookup"><span data-stu-id="3752d-440">Note that the **find()** method of this table returns a record that represents a company of the current Finance instance that this mapping is called in the context of.</span></span>

    1. <span data-ttu-id="3752d-441">I **Datakilder**-ruten velger du **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="3752d-441">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="3752d-442">Skriv inn **CompanyInfo** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-442">In the dialog box, in the **Name** field, enter **CompanyInfo**.</span></span>
    3. <span data-ttu-id="3752d-443">I **Tabell**-feltet angir du **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="3752d-443">In the **Table** field, enter **CompanyInfo**.</span></span>
    4. <span data-ttu-id="3752d-444">Velg **OK** for å legge til den nye datakilden.</span><span class="sxs-lookup"><span data-stu-id="3752d-444">Select **OK** to add the new data source.</span></span>

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a><span data-ttu-id="3752d-445">Legge til datakilder for å få tilgang til appopplistinger</span><span class="sxs-lookup"><span data-stu-id="3752d-445">Add data sources to access application enumerations</span></span>

<span data-ttu-id="3752d-446">Du må konfigurere datakilder for å få tilgang til appopplistinger og sammenligne verdiene med verdiene i felt av typen **Opplisting** i apptabellene.</span><span class="sxs-lookup"><span data-stu-id="3752d-446">You must configure data sources to access application enumerations and compare their values with values of fields of the **Enumeration** type in the application tables.</span></span> <span data-ttu-id="3752d-447">Du må bruke resultatet av sammenligningen for å fylle ut de aktuelle feltene i datamodellen.</span><span class="sxs-lookup"><span data-stu-id="3752d-447">You must use the result of the comparison to fill in appropriate fields of the data model.</span></span>

1. <span data-ttu-id="3752d-448">På siden **Modelltilordningsutforming**, i ruten **Datakildetyper**, velger du **Dynamics 365 for Operations\\Opplisting**.</span><span class="sxs-lookup"><span data-stu-id="3752d-448">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
2. <span data-ttu-id="3752d-449">Legg til en ny datakilde som skal brukes til å få tilgang til verdier i **EnumAppNoYes**-opplistingen:</span><span class="sxs-lookup"><span data-stu-id="3752d-449">Add a new data source that will be used to access values of the **EnumAppNoYes** enumeration:</span></span>

    1. <span data-ttu-id="3752d-450">I **Datakilder**-ruten velger du **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="3752d-450">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="3752d-451">Skriv inn **EnumAppNoYes** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-451">In the dialog box, in the **Name** field, enter **EnumAppNoYes**.</span></span>
    3. <span data-ttu-id="3752d-452">I **Opplisting**-feltet angir du **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="3752d-452">In the **Enumeration** field, enter **NoYes**.</span></span>
    4. <span data-ttu-id="3752d-453">Velg **OK** for å legge til den nye datakilden.</span><span class="sxs-lookup"><span data-stu-id="3752d-453">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="3752d-454">I ruten **Datakildetyper** velger du **Dynamics 365 for Operations\\Opplisting**.</span><span class="sxs-lookup"><span data-stu-id="3752d-454">In the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
4. <span data-ttu-id="3752d-455">Legg til en ny datakilde som skal brukes til å få tilgang til verdiene i **KMCollectionQuestionMode**-opplistingen:</span><span class="sxs-lookup"><span data-stu-id="3752d-455">Add a new data source that will be used to access the values of the **KMCollectionQuestionMode** enumeration:</span></span>

    1. <span data-ttu-id="3752d-456">I **Datakilder**-ruten velger du **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="3752d-456">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="3752d-457">Skriv inn **EnumAppQuestionOrder** i **Navn**-feltet i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="3752d-457">In the dialog box, in the **Name** field, enter **EnumAppQuestionOrder**.</span></span>
    3. <span data-ttu-id="3752d-458">I **Opplisting**-feltet angir du **KMCollectionQuestionMode**.</span><span class="sxs-lookup"><span data-stu-id="3752d-458">In the **Enumeration** field, enter **KMCollectionQuestionMode**.</span></span>
    4. <span data-ttu-id="3752d-459">Velg **OK** for å legge til den nye datakilden.</span><span class="sxs-lookup"><span data-stu-id="3752d-459">Select **OK** to add the new data source.</span></span>

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a><span data-ttu-id="3752d-460">Legge til ER-etiketter for å generere en rapport på et angitt språk</span><span class="sxs-lookup"><span data-stu-id="3752d-460">Add ER labels to generate a report in a specified language</span></span>

<span data-ttu-id="3752d-461">Du kan legge til ER-etiketter for å konfigurere noen av datakildene til returverdier som er avhengig av språket som er definert i konteksten til modelltilordningens kall.</span><span class="sxs-lookup"><span data-stu-id="3752d-461">You can add ER labels to configure some of your data sources to return values that depend on the language that is defined in the context of the model mapping's call.</span></span>

1. <span data-ttu-id="3752d-462">På siden **Modelltilordningsutforming**, i ruten **Datakilder**, velger du **Svar**, og deretter velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="3752d-462">On the **Model mapping designer** page, in the **Data sources** pane, select **Answer**, and then select **Edit**.</span></span>
2. <span data-ttu-id="3752d-463">Aktiver **Etikett**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-463">Activate the **Label** field.</span></span>
3. <span data-ttu-id="3752d-464">Velg **Oversett**.</span><span class="sxs-lookup"><span data-stu-id="3752d-464">Select **Translate**.</span></span>
4. <span data-ttu-id="3752d-465">Følg disse trinnene i dialogboksen **Tekstoversettelse**:</span><span class="sxs-lookup"><span data-stu-id="3752d-465">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="3752d-466">I feltet **Etikett-ID** angir du **PositiveAnswer**.</span><span class="sxs-lookup"><span data-stu-id="3752d-466">In the **Label Id** field, enter **PositiveAnswer**.</span></span>
    2. <span data-ttu-id="3752d-467">I feltet **Tekst på standardspråk** angir du **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3752d-467">In the **Text in default language** field, enter **Yes**.</span></span>
    3. <span data-ttu-id="3752d-468">Velg **Oversett**.</span><span class="sxs-lookup"><span data-stu-id="3752d-468">Select **Translate**.</span></span>
    4. <span data-ttu-id="3752d-469">I feltet **Etikett-ID** angir du **NegativeAnswer**.</span><span class="sxs-lookup"><span data-stu-id="3752d-469">In the **Label Id** field, enter **NegativeAnswer**.</span></span>
    5. <span data-ttu-id="3752d-470">I feltet **Tekst på standardspråk** angir du **Nei**.</span><span class="sxs-lookup"><span data-stu-id="3752d-470">In the **Text in default language** field, enter **No**.</span></span>
    6. <span data-ttu-id="3752d-471">Velg **Oversett**.</span><span class="sxs-lookup"><span data-stu-id="3752d-471">Select **Translate**.</span></span>

5. <span data-ttu-id="3752d-472">Lukk dialogboksen **Tekstoversettelse**.</span><span class="sxs-lookup"><span data-stu-id="3752d-472">Close the **Text translation** dialog box.</span></span>
6. <span data-ttu-id="3752d-473">Velg **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="3752d-473">Select **Cancel**.</span></span>

![Legge til ER-etiketter for den redigerbare modelltilordningen](./media/er-quick-start1-adding-labels.png)

<span data-ttu-id="3752d-475">Du har angitt ER-etiketter bare for standardspråket.</span><span class="sxs-lookup"><span data-stu-id="3752d-475">You've entered ER labels only for the default language.</span></span> <span data-ttu-id="3752d-476">Hvis du vil ha informasjon om hvordan ER-etiketter kan oversettes til andre språk, kan du se [Utforme flerspråklige rapporter](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="3752d-476">For information about how ER labels can be translated into other languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a><span data-ttu-id="3752d-477">Legge til en datakilde for å transformere resultatene av å sammenligne opplistingsverdier med en tekstverdi</span><span class="sxs-lookup"><span data-stu-id="3752d-477">Add a data source to transform the results of comparing enumeration values to a text value</span></span>

<span data-ttu-id="3752d-478">Fordi du må transformere resultatene av sammenligningen mellom opplistingsverdier og tekstverdier flere ganger for forskjellige kilder, kan det være lurt å konfigurere denne logikken som én enkelt datakilde.</span><span class="sxs-lookup"><span data-stu-id="3752d-478">Because you must transform the results of the comparison between enumeration values and text values several times for difference sources, it's a good idea to configure this logic as a single data source.</span></span> <span data-ttu-id="3752d-479">Hvis du vil at denne datakilden skal kunne brukes på nytt, må du imidlertid konfigurere den som en parameterisert datakilde.</span><span class="sxs-lookup"><span data-stu-id="3752d-479">However, to make this data source reusable, you must then configure it as the parametrized data source.</span></span> <span data-ttu-id="3752d-480">For mer informasjon, se [Støtte for parametriserte kall av ER-datakilder av felttypen Beregnet](er-calculated-field-type.md).</span><span class="sxs-lookup"><span data-stu-id="3752d-480">For more information, see [Support parameterized calls of ER data sources of the Calculated field type](er-calculated-field-type.md).</span></span>

1. <span data-ttu-id="3752d-481">På siden **Modelltilordningsutforming**, i ruten **Datakildetyper**, velger du **Generelt\\Tom container**.</span><span class="sxs-lookup"><span data-stu-id="3752d-481">On the **Model mapping designer** page, in the **Data source types** pane, select **General\\Empty container**.</span></span>
2. <span data-ttu-id="3752d-482">Legg til en ny containerdatakilde:</span><span class="sxs-lookup"><span data-stu-id="3752d-482">Add a new container data source:</span></span>

    1. <span data-ttu-id="3752d-483">I **Datakilder**-ruten velger du **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="3752d-483">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="3752d-484">Skriv inn **Hjelpeprogram** i **Navn**-feltet i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="3752d-484">In the dialog box, in the **Name** field, enter **Helper**.</span></span>
    3. <span data-ttu-id="3752d-485">Velg **OK** for å legge til den nye containerdatakilden.</span><span class="sxs-lookup"><span data-stu-id="3752d-485">Select **OK** to add the new container data source.</span></span>

3. <span data-ttu-id="3752d-486">I ruten **Datakildetyper** velger du **Funksjoner\\Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="3752d-486">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="3752d-487">Legg til en ny datakilde:</span><span class="sxs-lookup"><span data-stu-id="3752d-487">Add a new data source:</span></span>

    1. <span data-ttu-id="3752d-488">I **Datakilder**-ruten velger du **Hjelpeprogram**.</span><span class="sxs-lookup"><span data-stu-id="3752d-488">In the **Data sources** pane, select **Helper**.</span></span>
    2. <span data-ttu-id="3752d-489">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="3752d-489">Select **Add**.</span></span>
    3. <span data-ttu-id="3752d-490">Skriv inn **NoYesEnumToString** i **Navn**-feltet i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="3752d-490">In the dialog box, in the **Name** field, enter **NoYesEnumToString**.</span></span>
    4. <span data-ttu-id="3752d-491">Velg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="3752d-491">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="3752d-492">Velg **Parametere** i formelredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="3752d-492">In the formula editor, select **Parameters**.</span></span>
    6. <span data-ttu-id="3752d-493">Følg denne fremgangsmåten for å angi parametere for det konfigurerte uttrykket:</span><span class="sxs-lookup"><span data-stu-id="3752d-493">Follow these steps to specify parameters for the configured expression:</span></span>

        1. <span data-ttu-id="3752d-494">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3752d-494">Select **New**.</span></span>
        2. <span data-ttu-id="3752d-495">Skriv inn **Argument** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-495">In the dialog box, in the **Name** field, enter **Argument**.</span></span>
        3. <span data-ttu-id="3752d-496">I **Type**-feltet velger du datatypen **Boolsk**.</span><span class="sxs-lookup"><span data-stu-id="3752d-496">In the **Type** field, select the **Boolean** data type.</span></span>
        4. <span data-ttu-id="3752d-497">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3752d-497">Select **OK**.</span></span>

    7. <span data-ttu-id="3752d-498">I **Formel**-feltet angir du **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** for å returnere teksten for den aktuelle ER-etiketten, avhengig av språket i kjøringskonteksten og verdien av den angittet parameteren.</span><span class="sxs-lookup"><span data-stu-id="3752d-498">In the **Formula** field, enter **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** to return the text of the appropriate ER label, depending on the language of the execution context and value of the specified parameter.</span></span>
    8. <span data-ttu-id="3752d-499">Velg **Lagre**, og lukk formelredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="3752d-499">Select **Save**, and close the formula editor.</span></span>
    9. <span data-ttu-id="3752d-500">Velg **OK** for å legge til den nye datakilden.</span><span class="sxs-lookup"><span data-stu-id="3752d-500">Select **OK** to add the new data source.</span></span>

![Konfigurert modelltilordning i ER-modelltilordningsutforming](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a><span data-ttu-id="3752d-502">Binde datakilder til datamodellfelt</span><span class="sxs-lookup"><span data-stu-id="3752d-502">Bind data sources to data model fields</span></span>

<span data-ttu-id="3752d-503">Du må binde de konfigurerte datakildene til feltene i datamodellen for å angi hvordan datamodellen skal fylles ut med appdata ved kjøring.</span><span class="sxs-lookup"><span data-stu-id="3752d-503">You must bind the configured data sources to the fields of the data model to specify how the data model will by filled in with application data at runtime.</span></span>

1. <span data-ttu-id="3752d-504">På siden **Modelltilordningsutforming**, i ruten **Datamodell**, velger du **Bedriftsnavn**.</span><span class="sxs-lookup"><span data-stu-id="3752d-504">On the **Model mapping designer** page, in the **Data model** pane, select **CompanyName**.</span></span>
2. <span data-ttu-id="3752d-505">I **Datakilder**-ruten utvider du **CompanyInfo**, og deretter gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="3752d-505">In the **Data sources** pane, expand **CompanyInfo**, and then follow these steps:</span></span>

    1. <span data-ttu-id="3752d-506">Utvid noden **CompanyInfo.find()** som representerer **find()**-metoden i CompanyInfo-tabellen.</span><span class="sxs-lookup"><span data-stu-id="3752d-506">Expand the **CompanyInfo.find()** node that represents the **find()** method of the CompanyInfo table.</span></span>
    2. <span data-ttu-id="3752d-507">Velg **CompanyInfo.find().Name**.</span><span class="sxs-lookup"><span data-stu-id="3752d-507">Select **CompanyInfo.find().Name**.</span></span>
    3. <span data-ttu-id="3752d-508">Velg **Bind** for å fylle ut navnet på firmaet som den konfigurerte modelltilordningen kalles i, i konteksten for kjøretid.</span><span class="sxs-lookup"><span data-stu-id="3752d-508">Select **Bind** to fill in the name of the company that the configured model mapping is called in the context of at runtime.</span></span>

3. <span data-ttu-id="3752d-509">I **Datamodell**-ruten velger du **Spørreskjema**.</span><span class="sxs-lookup"><span data-stu-id="3752d-509">In the **Data model** pane, select **Questionnaire**.</span></span>
4. <span data-ttu-id="3752d-510">I **Datakilder**-ruten velger du **Spørreskjema**, og deretter velger du **Bind** for å fylle ut spørreskjemaposter.</span><span class="sxs-lookup"><span data-stu-id="3752d-510">In the **Data sources** pane, select **Questionnaire**, and then select **Bind** to fill in questionnaire records.</span></span>
5. <span data-ttu-id="3752d-511">I **Datamodell**-ruten utvider du **Spørreskjema**, og deretter gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="3752d-511">In the **Data model** pane, expand **Questionnaire**, and then follow these steps:</span></span>

    1. <span data-ttu-id="3752d-512">I **Datamodell**-ruten velger du **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="3752d-512">In the **Data model** pane, select **Active**.</span></span>
    2. <span data-ttu-id="3752d-513">I **Datamodell**-ruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="3752d-513">In the **Data model** pane, select **Edit**.</span></span>
    3. <span data-ttu-id="3752d-514">I **Formel**-feltet skriver du inn **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** for å fylle ut det tekstavhengige og språkavhengige resultatet av sammenligningen mellom opplistingsverdier.</span><span class="sxs-lookup"><span data-stu-id="3752d-514">In the **Formula** field, enter **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** to fill the text-dependent and language-dependent result of the comparison between enumeration values.</span></span>

6. <span data-ttu-id="3752d-515">Fortsett med å binde datakilder til datamodellfelt på samme måte til du oppnår følgende resultat.</span><span class="sxs-lookup"><span data-stu-id="3752d-515">Continue to bind data sources to data model fields in the same manner until you achieve the following result.</span></span>

    | <span data-ttu-id="3752d-516">Feltbane</span><span class="sxs-lookup"><span data-stu-id="3752d-516">Field path</span></span>                                              | <span data-ttu-id="3752d-517">Datatype</span><span class="sxs-lookup"><span data-stu-id="3752d-517">Data type</span></span>   | <span data-ttu-id="3752d-518">Handling</span><span class="sxs-lookup"><span data-stu-id="3752d-518">Action</span></span> | <span data-ttu-id="3752d-519">Bindingsuttrykk</span><span class="sxs-lookup"><span data-stu-id="3752d-519">Binding expression</span></span> |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | <span data-ttu-id="3752d-520">Bedriftsnavn</span><span class="sxs-lookup"><span data-stu-id="3752d-520">CompanyName</span></span>                                             | <span data-ttu-id="3752d-521">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-521">String</span></span>      | <span data-ttu-id="3752d-522">Bind</span><span class="sxs-lookup"><span data-stu-id="3752d-522">Bind</span></span>   | <span data-ttu-id="3752d-523">CompanyInfo.'find()'.Name</span><span class="sxs-lookup"><span data-stu-id="3752d-523">CompanyInfo.'find()'.Name</span></span> |
    | <span data-ttu-id="3752d-524">Spørreskjema</span><span class="sxs-lookup"><span data-stu-id="3752d-524">Questionnaire</span></span>                                           | <span data-ttu-id="3752d-525">Postliste</span><span class="sxs-lookup"><span data-stu-id="3752d-525">Record list</span></span> | <span data-ttu-id="3752d-526">Bind</span><span class="sxs-lookup"><span data-stu-id="3752d-526">Bind</span></span>   | <span data-ttu-id="3752d-527">Spørreskjema</span><span class="sxs-lookup"><span data-stu-id="3752d-527">Questionnaire</span></span> |
    | <span data-ttu-id="3752d-528">Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="3752d-528">Questionnaire\\Active</span></span>                                   | <span data-ttu-id="3752d-529">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-529">String</span></span>      | <span data-ttu-id="3752d-530">Rediger</span><span class="sxs-lookup"><span data-stu-id="3752d-530">Edit</span></span>   | <span data-ttu-id="3752d-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="3752d-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="3752d-532">Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="3752d-532">Questionnaire\\Code</span></span>                                     | <span data-ttu-id="3752d-533">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-533">String</span></span>      | <span data-ttu-id="3752d-534">Bind</span><span class="sxs-lookup"><span data-stu-id="3752d-534">Bind</span></span>   | <span data-ttu-id="3752d-535">\@.kmCollectionId</span><span class="sxs-lookup"><span data-stu-id="3752d-535">\@.kmCollectionId</span></span> |
    | <span data-ttu-id="3752d-536">Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="3752d-536">Questionnaire\\Description</span></span>                              | <span data-ttu-id="3752d-537">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-537">String</span></span>      | <span data-ttu-id="3752d-538">Bind</span><span class="sxs-lookup"><span data-stu-id="3752d-538">Bind</span></span>   | <span data-ttu-id="3752d-539">\@.Description</span><span class="sxs-lookup"><span data-stu-id="3752d-539">\@.Description</span></span> |
    | <span data-ttu-id="3752d-540">Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="3752d-540">Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="3752d-541">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-541">String</span></span>      | <span data-ttu-id="3752d-542">Bind</span><span class="sxs-lookup"><span data-stu-id="3752d-542">Bind</span></span>   | <span data-ttu-id="3752d-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span><span class="sxs-lookup"><span data-stu-id="3752d-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span></span> |
    | <span data-ttu-id="3752d-544">Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="3752d-544">Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="3752d-545">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-545">String</span></span>      | <span data-ttu-id="3752d-546">Rediger</span><span class="sxs-lookup"><span data-stu-id="3752d-546">Edit</span></span>   | <span data-ttu-id="3752d-547">CASE (\@.questionMode,</span><span class="sxs-lookup"><span data-stu-id="3752d-547">CASE (\@.questionMode,</span></span><br><span data-ttu-id="3752d-548">EnumAppQuestionOrder.Conditional, "Betinget",</span><span class="sxs-lookup"><span data-stu-id="3752d-548">EnumAppQuestionOrder.Conditional, "Conditional",</span></span><br><span data-ttu-id="3752d-549">EnumAppQuestionOrder.Random, "Tilfeldig (prosentverdi på spørreskjema)",</span><span class="sxs-lookup"><span data-stu-id="3752d-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span></span><br><span data-ttu-id="3752d-550">EnumAppQuestionOrder.RandomGroup, "Tilfeldig (prosentverdi i resultatgrupper)",</span><span class="sxs-lookup"><span data-stu-id="3752d-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span></span><br><span data-ttu-id="3752d-551">EnumAppQuestionOrder. Sequence, "Sekvensiell",</span><span class="sxs-lookup"><span data-stu-id="3752d-551">EnumAppQuestionOrder.Sequence, "Sequential",</span></span><br><span data-ttu-id="3752d-552">"")</span><span class="sxs-lookup"><span data-stu-id="3752d-552">"")</span></span> |
    | <span data-ttu-id="3752d-553">Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="3752d-553">Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="3752d-554">Registrer</span><span class="sxs-lookup"><span data-stu-id="3752d-554">Record</span></span>      |        | |
    | <span data-ttu-id="3752d-555">Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="3752d-555">Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="3752d-556">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-556">String</span></span>      | <span data-ttu-id="3752d-557">Bind</span><span class="sxs-lookup"><span data-stu-id="3752d-557">Bind</span></span>   | <span data-ttu-id="3752d-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span><span class="sxs-lookup"><span data-stu-id="3752d-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span></span> |
    | <span data-ttu-id="3752d-559">Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="3752d-559">Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="3752d-560">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-560">String</span></span>      | <span data-ttu-id="3752d-561">Bind</span><span class="sxs-lookup"><span data-stu-id="3752d-561">Bind</span></span>   | <span data-ttu-id="3752d-562">\@.'\$ResultGroup'.description</span><span class="sxs-lookup"><span data-stu-id="3752d-562">\@.'\$ResultGroup'.description</span></span> |
    | <span data-ttu-id="3752d-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="3752d-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="3752d-564">Kommatall</span><span class="sxs-lookup"><span data-stu-id="3752d-564">Real</span></span>        | <span data-ttu-id="3752d-565">Bind</span><span class="sxs-lookup"><span data-stu-id="3752d-565">Bind</span></span>   | <span data-ttu-id="3752d-566">\@.'\$ResultGroup'.maxPoint</span><span class="sxs-lookup"><span data-stu-id="3752d-566">\@.'\$ResultGroup'.maxPoint</span></span> |
    | <span data-ttu-id="3752d-567">Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="3752d-567">Questionnaire\\Question</span></span>                                 | <span data-ttu-id="3752d-568">Postliste</span><span class="sxs-lookup"><span data-stu-id="3752d-568">Record list</span></span> | <span data-ttu-id="3752d-569">Bind</span><span class="sxs-lookup"><span data-stu-id="3752d-569">Bind</span></span>   | <span data-ttu-id="3752d-570">\@.'&lt;Relations'.KMCollectionQuestion</span><span class="sxs-lookup"><span data-stu-id="3752d-570">\@.'&lt;Relations'.KMCollectionQuestion</span></span> |
    | <span data-ttu-id="3752d-571">Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="3752d-571">Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="3752d-572">Heltall</span><span class="sxs-lookup"><span data-stu-id="3752d-572">Integer</span></span>     | <span data-ttu-id="3752d-573">Bind</span><span class="sxs-lookup"><span data-stu-id="3752d-573">Bind</span></span>   | <span data-ttu-id="3752d-574">\@.answerCollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="3752d-574">\@.answerCollectionSequenceNumber</span></span> |
    | <span data-ttu-id="3752d-575">Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="3752d-575">Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="3752d-576">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-576">String</span></span>      | <span data-ttu-id="3752d-577">Bind</span><span class="sxs-lookup"><span data-stu-id="3752d-577">Bind</span></span>   | <span data-ttu-id="3752d-578">\@.kmQuestionId</span><span class="sxs-lookup"><span data-stu-id="3752d-578">\@.kmQuestionId</span></span> |
    | <span data-ttu-id="3752d-579">Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="3752d-579">Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="3752d-580">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-580">String</span></span>      | <span data-ttu-id="3752d-581">Rediger</span><span class="sxs-lookup"><span data-stu-id="3752d-581">Edit</span></span>   | <span data-ttu-id="3752d-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="3752d-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="3752d-583">Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="3752d-583">Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="3752d-584">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-584">String</span></span>      | <span data-ttu-id="3752d-585">Bind</span><span class="sxs-lookup"><span data-stu-id="3752d-585">Bind</span></span>   | <span data-ttu-id="3752d-586">\@.parentQuestionId</span><span class="sxs-lookup"><span data-stu-id="3752d-586">\@.parentQuestionId</span></span> |
    | <span data-ttu-id="3752d-587">Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="3752d-587">Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="3752d-588">Heltall</span><span class="sxs-lookup"><span data-stu-id="3752d-588">Integer</span></span>     | <span data-ttu-id="3752d-589">Bind</span><span class="sxs-lookup"><span data-stu-id="3752d-589">Bind</span></span>   | <span data-ttu-id="3752d-590">\@.SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="3752d-590">\@.SequenceNumber</span></span> |
    | <span data-ttu-id="3752d-591">Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="3752d-591">Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="3752d-592">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-592">String</span></span>      | <span data-ttu-id="3752d-593">Bind</span><span class="sxs-lookup"><span data-stu-id="3752d-593">Bind</span></span>   | <span data-ttu-id="3752d-594">\@.'\$Question'.text</span><span class="sxs-lookup"><span data-stu-id="3752d-594">\@.'\$Question'.text</span></span> |
    | <span data-ttu-id="3752d-595">Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="3752d-595">Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="3752d-596">Postliste</span><span class="sxs-lookup"><span data-stu-id="3752d-596">Record list</span></span> | <span data-ttu-id="3752d-597">Bind</span><span class="sxs-lookup"><span data-stu-id="3752d-597">Bind</span></span>   | <span data-ttu-id="3752d-598">\@.'\$Question'.'\$Answer'</span><span class="sxs-lookup"><span data-stu-id="3752d-598">\@.'\$Question'.'\$Answer'</span></span> |
    | <span data-ttu-id="3752d-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="3752d-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="3752d-600">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-600">String</span></span>      | <span data-ttu-id="3752d-601">Rediger</span><span class="sxs-lookup"><span data-stu-id="3752d-601">Edit</span></span>   | <span data-ttu-id="3752d-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="3752d-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="3752d-603">Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="3752d-603">Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="3752d-604">Kommatall</span><span class="sxs-lookup"><span data-stu-id="3752d-604">Real</span></span>        | <span data-ttu-id="3752d-605">Bind</span><span class="sxs-lookup"><span data-stu-id="3752d-605">Bind</span></span>   | <span data-ttu-id="3752d-606">\@.point</span><span class="sxs-lookup"><span data-stu-id="3752d-606">\@.point</span></span> |
    | <span data-ttu-id="3752d-607">Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="3752d-607">Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="3752d-608">Heltall</span><span class="sxs-lookup"><span data-stu-id="3752d-608">Integer</span></span>     | <span data-ttu-id="3752d-609">Bind</span><span class="sxs-lookup"><span data-stu-id="3752d-609">Bind</span></span>   | <span data-ttu-id="3752d-610">\@.sequenceNumber</span><span class="sxs-lookup"><span data-stu-id="3752d-610">\@.sequenceNumber</span></span> |
    | <span data-ttu-id="3752d-611">Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="3752d-611">Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="3752d-612">Streng</span><span class="sxs-lookup"><span data-stu-id="3752d-612">String</span></span>      | <span data-ttu-id="3752d-613">Bind</span><span class="sxs-lookup"><span data-stu-id="3752d-613">Bind</span></span>   | <span data-ttu-id="3752d-614">\@.text</span><span class="sxs-lookup"><span data-stu-id="3752d-614">\@.text</span></span> |

    <span data-ttu-id="3752d-615">Den følgende illustrasjonen viser den endelige tilstanden til den konfigurerte modelltilordningen på siden **Modelltilordningsutforming**.</span><span class="sxs-lookup"><span data-stu-id="3752d-615">The following illustration shows the final state of the configured model mapping on the **Model mapping designer** page.</span></span>

    ![Fullstendig konfigurert modelltilordning i ER-modelltilordningsutforming](./media/er-quick-start1-mapping2.png)

7. <span data-ttu-id="3752d-617">Lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="3752d-617">Save your changes.</span></span>
8. <span data-ttu-id="3752d-618">Lukk siden **Modelltilordningsutforming**.</span><span class="sxs-lookup"><span data-stu-id="3752d-618">Close the **Model mapping designer** page.</span></span>

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a><span data-ttu-id="3752d-619">Fullføre utformingen av modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="3752d-619">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="3752d-620">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="3752d-620">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="3752d-621">På **Konfigurasjoner**-siden, i konfigurasjonstreet, velger du **Spørreskjematilordning**.</span><span class="sxs-lookup"><span data-stu-id="3752d-621">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="3752d-622">I hurtigfanen **Versjoner** velger du konfigurasjonsversjonen med statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="3752d-622">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="3752d-623">Velg **Endre status** \> **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="3752d-623">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="3752d-624">Statusen til versjon 1.1 av denne konfigurasjonen endres fra **Utkast** til **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="3752d-624">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="3752d-625">Versjon 1.1 kan ikke lenger endres.</span><span class="sxs-lookup"><span data-stu-id="3752d-625">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="3752d-626">Denne versjonen inneholder den konfigurerte modelltilordningen og kan brukes som basis for andre ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="3752d-626">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="3752d-627">Versjon 1.2 av denne konfigurasjonen opprettes og har statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="3752d-627">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="3752d-628">Du kan redigere denne versjonen for å justere konfigurasjonen **Spørreskjematilordning**.</span><span class="sxs-lookup"><span data-stu-id="3752d-628">You can edit this version to adjust the **Questionnaire mapping** configuration.</span></span>

![Versjoner av den redigerbare ER-konfigurasjonen på Konfigurasjoner-siden](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> <span data-ttu-id="3752d-630">Den konfigurerte modelltilordningen er den Finance-spesifikke implementeringen av den abstrakte datamodellen som representerer bedriftsdomenet **Spørreskjema**.</span><span class="sxs-lookup"><span data-stu-id="3752d-630">The configured model mapping is your Finance-specific implementation of the abstract data model that represents the **Questionnaire** business domain.</span></span>

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a><span data-ttu-id="3752d-631">Utforme en mal for en egendefinert rapport</span><span class="sxs-lookup"><span data-stu-id="3752d-631">Design a template for a custom report</span></span>

<span data-ttu-id="3752d-632">ER-rammeverket bruker forhåndsdefinerte maler til å generere rapporter i Microsoft Office-formater (Excel-arbeidsbøker eller Word-dokumenter).</span><span class="sxs-lookup"><span data-stu-id="3752d-632">The ER framework uses predefined templates to generate reports in Microsoft Office formats (Excel workbooks or Word documents).</span></span> <span data-ttu-id="3752d-633">Mens den påkrevde rapporten genereres, fylles det ut en mal med nødvendige data i samsvar med den konfigurerte dataflyten.</span><span class="sxs-lookup"><span data-stu-id="3752d-633">While the required report is being generated, a template is filled in with required data according to the configured dataflow.</span></span> <span data-ttu-id="3752d-634">Derfor må du først utforme en mal for den egendefinerte rapporten.</span><span class="sxs-lookup"><span data-stu-id="3752d-634">Therefore, you must first design a template for your custom report.</span></span> <span data-ttu-id="3752d-635">Denne malen må utformes som en Excel-arbeidsbok, der strukturen representerer oppsettet til en egendefinert rapport.</span><span class="sxs-lookup"><span data-stu-id="3752d-635">This template must be designed as an Excel workbook, the structure of which represents the layout of a custom report.</span></span> <span data-ttu-id="3752d-636">Du må gi navn til alle Excel-elementer du planlegger å fylle ut med nødvendige data.</span><span class="sxs-lookup"><span data-stu-id="3752d-636">You must name every Excel item that you plan to fill in with required data.</span></span>

1. <span data-ttu-id="3752d-637">Last ned filen [Questionnaires report template.xlsx](https://download.microsoft.com/download/3/8/2/382c3cf0-87bb-473f-b7bb-3015b4facb74/Questionnaires_report_template.xlsx), og lagre den på den lokale datamaskinen.</span><span class="sxs-lookup"><span data-stu-id="3752d-637">Download the [Questionnaires report template.xlsx](https://download.microsoft.com/download/3/8/2/382c3cf0-87bb-473f-b7bb-3015b4facb74/Questionnaires_report_template.xlsx) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="3752d-638">Åpne filen i Excel, og gå gjennom strukturen til arbeidsboken.</span><span class="sxs-lookup"><span data-stu-id="3752d-638">Open the file in Excel, and review the structure of the workbook.</span></span>

<span data-ttu-id="3752d-639">Som den følgende illustrasjonen viser, er den nedlastede malen utformet for å skrive ut bestemte spørreskjemaer som presenterer spørsmålene i et spørreskjema sammen med riktige svar.</span><span class="sxs-lookup"><span data-stu-id="3752d-639">As the following illustration shows, the downloaded template has been designed to print specified questionnaires that present a questionnaire's questions together with appropriate answers.</span></span>

![Excel-mal for utskrift av angitte spørreskjemaer](./media/er-quick-start1-template-layout.png)

<span data-ttu-id="3752d-641">Excel-navn er lagt til denne malen for å fylle ut spørreskjemadetaljene.</span><span class="sxs-lookup"><span data-stu-id="3752d-641">Excel names have been added to this template to fill in the questionnaire details.</span></span> <span data-ttu-id="3752d-642">Du kan bruke Navnebehandling til å se gjennom Excel-navnene.</span><span class="sxs-lookup"><span data-stu-id="3752d-642">You can use Name Manager to review the Excel names.</span></span>

![Bruke Navnebehandling til å se gjennom Excel-navn i den angitte Excel-malen](./media/er-quick-start1-template-names.png)

<span data-ttu-id="3752d-644">Rapportetiketter er lagt til som fast tekst på norsk.</span><span class="sxs-lookup"><span data-stu-id="3752d-644">Report labels have been added as fixed text in the English language.</span></span> <span data-ttu-id="3752d-645">Du kan erstatte rapportetikettene med nye Excel-navn som fyller ut etikettene med språkavhengig tekst, ved å bruke [etiketter](#AddMmLabels) i ER-format, som du gjorde for språkavhengige uttrykk i den konfigurerte modelltilordningen.</span><span class="sxs-lookup"><span data-stu-id="3752d-645">You can replace the report labels with new Excel names that fill in the labels with language-dependent text by using the ER format [labels](#AddMmLabels), as you did for language-dependent expressions in the configured model mapping.</span></span> <span data-ttu-id="3752d-646">I dette tilfellet må ER-etiketter legges til i det redigerbare ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="3752d-646">In this case, ER labels must be added in the editable ER format.</span></span>

<span data-ttu-id="3752d-647">Som den følgende illustrasjonen viser, er det egendefinerte rapporthodet angitt for at Excel skal kunne utføre sideveksling.</span><span class="sxs-lookup"><span data-stu-id="3752d-647">As the following illustration shows, the custom report header has been specified to enable Excel to do paging.</span></span>

![Egendefinert rapporthode i den angitte Excel-malen](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a><span data-ttu-id="3752d-649">Utforme et format</span><span class="sxs-lookup"><span data-stu-id="3752d-649">Design a format</span></span>

<span data-ttu-id="3752d-650">Som en bruker med rollen som funksjonsrådgiver for elektronisk rapportering må du opprette en ny ER-konfigurasjon som inneholder en komponent av typen [format](general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="3752d-650">As a user in the Electronic Reporting Functional Consultant role, you must create a new ER configuration that contains a [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="3752d-651">Du må konfigurere formatkomponenten til å angi hvordan en rapportmal skal fylles ut med nødvendige data ved kjøring.</span><span class="sxs-lookup"><span data-stu-id="3752d-651">You must configure the format component to specify how a report template will be filled in with required data at runtime.</span></span>

<span data-ttu-id="3752d-652">Ved å fullføre trinnene under [Importere en konstruert formatkonfigurasjon](#FormatImport) kan du importere det nødvendige formatet fra den angitte XML-filen.</span><span class="sxs-lookup"><span data-stu-id="3752d-652">By completing the steps in the [Import a designed format configuration](#FormatImport) section, you can import the required format from the provided XML file.</span></span> <span data-ttu-id="3752d-653">Du kan også fullføre trinnene i delen [Opprette en ny formatkonfigurasjon](#FormatCreate) for å utforme dette formatet fra grunnen av.</span><span class="sxs-lookup"><span data-stu-id="3752d-653">Alternatively, you can complete the steps in the [Create a new format configuration](#FormatCreate) section to design this format from scratch.</span></span>

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a><span data-ttu-id="3752d-654">Importere en konstruert formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3752d-654">Import a designed format configuration</span></span>

1. <span data-ttu-id="3752d-655">Last ned filen [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml), og lagre den på den lokale datamaskinen.</span><span class="sxs-lookup"><span data-stu-id="3752d-655">Download the [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="3752d-656">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="3752d-656">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="3752d-657">I arbeidsområdet **Elektronisk rapportering** velger du **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="3752d-657">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="3752d-658">I handlingsruten velger du **Kurs** \> **Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="3752d-658">On the Action pane, Select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="3752d-659">Velg **Bla gjennom**, og finn og velg filen **Questionnaires format.version.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="3752d-659">Select **Browse**, and then find and select the **Questionnaires format.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="3752d-660">Velg **OK** for å importere konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="3752d-660">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="3752d-661">For å fortsette hopper du over neste prosedyre, [Opprette en ny formatkonfigurasjon](#FormatCreate).</span><span class="sxs-lookup"><span data-stu-id="3752d-661">To continue, skip the next procedure, [Create a new format configuration](#FormatCreate).</span></span>

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a><span data-ttu-id="3752d-662">Opprette en ny formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3752d-662">Create a new format configuration</span></span>
 
1. <span data-ttu-id="3752d-663">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="3752d-663">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="3752d-664">På **Konfigurasjoner**-siden, i konfigurasjonstreet, velger du **Spørreskjemamodell**.</span><span class="sxs-lookup"><span data-stu-id="3752d-664">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="3752d-665">Velg **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="3752d-665">Select **Create configuration**.</span></span>
4. <span data-ttu-id="3752d-666">Følg disse trinnene i rullegardinboksen:</span><span class="sxs-lookup"><span data-stu-id="3752d-666">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="3752d-667">I feltet **Ny** velger du **Format basert på datamodellspørreskjemaer**.</span><span class="sxs-lookup"><span data-stu-id="3752d-667">In the **New** field, select **Format based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="3752d-668">I **Navn**-feltet angir du **Spørreskjemarapport**.</span><span class="sxs-lookup"><span data-stu-id="3752d-668">In the **Name** field, enter **Questionnaire report**.</span></span>
    3. <span data-ttu-id="3752d-669">I feltet **Datamodellversjon** velger du **1**.</span><span class="sxs-lookup"><span data-stu-id="3752d-669">In the **Data model version** field, select **1**.</span></span>

        > [!NOTE]
        > - <span data-ttu-id="3752d-670">Hvis du velger en bestemt versjon av basisdatamodellen, vil strukturen i den tilsvarende versjonen av datamodellen vises som strukturen til **Modell**-datakilden i formatet som opprettes.</span><span class="sxs-lookup"><span data-stu-id="3752d-670">If you select a specific version of the base data model, the structure of the corresponding version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span>
        > - <span data-ttu-id="3752d-671">Du kan la dette feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="3752d-671">You can leave this field blank.</span></span> <span data-ttu-id="3752d-672">I så fall vises strukturen til **Utkast**-versjonen av datamodellen som strukturen til **Modell**-datakilden i formatet som er opprettet.</span><span class="sxs-lookup"><span data-stu-id="3752d-672">In that case, the structure of the **Draft** version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span> <span data-ttu-id="3752d-673">Du kan deretter justere modellen og umiddelbart se justeringene i formatet.</span><span class="sxs-lookup"><span data-stu-id="3752d-673">You can then adjust your model and immediately see those adjustments in your format.</span></span> <span data-ttu-id="3752d-674">Denne fremgangsmåten kan forbedre effektiviteten for ER-løsningsutformingen når du konfigurerer datamodellen, modelltilordningen og formatet samtidig.</span><span class="sxs-lookup"><span data-stu-id="3752d-674">This approach might improve the efficiency of ER solution design when you configure your data model, model mapping, and format simultaneously.</span></span>
        > - <span data-ttu-id="3752d-675">Hvis du velger en bestemt versjon av basisdatamodellen, kan du bytte til å bruke **Utkast**-versjonen senere, når du begynner å redigere et format.</span><span class="sxs-lookup"><span data-stu-id="3752d-675">If you select a specific version of the base data model, you can switch to using the **Draft** version later, when you start to edit a format.</span></span>

    4. <span data-ttu-id="3752d-676">I feltet **Definisjon av datamodell** velger du **Rot**-definisjonen.</span><span class="sxs-lookup"><span data-stu-id="3752d-676">In the **Data model definition** field, select the **Root** definition.</span></span>

5. <span data-ttu-id="3752d-677">Velg **Opprett konfigurasjon** for å opprette konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="3752d-677">Select **Create configuration** to create the configuration.</span></span>

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a><span data-ttu-id="3752d-678">Importere en rapportmal</span><span class="sxs-lookup"><span data-stu-id="3752d-678">Import a report template</span></span>

1. <span data-ttu-id="3752d-679">På **Konfigurasjoner**-siden, i konfigurasjonstreet, velger du **Spørreskjemarapport**.</span><span class="sxs-lookup"><span data-stu-id="3752d-679">On the **Configurations** page, in the configuration tree, select **Questionnaire report**.</span></span>
2. <span data-ttu-id="3752d-680">Velg **Utforming** for å begynne å konfigurere et egendefinert format.</span><span class="sxs-lookup"><span data-stu-id="3752d-680">Select **Designer** to start to configure a custom format.</span></span>
3. <span data-ttu-id="3752d-681">På siden **Formatutforming**, i handlingsruten, velger du **Importer** \> **Importer fra Excel**.</span><span class="sxs-lookup"><span data-stu-id="3752d-681">On the **Format designer** page, on the Action Pane, select **Import** \> **Import from Excel**.</span></span>
4. <span data-ttu-id="3752d-682">Følg disse trinnene i dialogboksen:</span><span class="sxs-lookup"><span data-stu-id="3752d-682">In the dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="3752d-683">Velg **Legg til mal**.</span><span class="sxs-lookup"><span data-stu-id="3752d-683">Select **Add template**.</span></span>
    2. <span data-ttu-id="3752d-684">Finn og velg den lokalt lagrede filen **Questionnaires report template.xslx**, og velg deretter **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="3752d-684">Find and select the locally saved **Questionnaires report template.xslx** file, and then select **Open**.</span></span>
    3. <span data-ttu-id="3752d-685">Velg **OK** for å importere malen.</span><span class="sxs-lookup"><span data-stu-id="3752d-685">Select **OK** to import the template.</span></span>

    ![Importere en rapportmal](./media/er-quick-start1-template-import.png)

<span data-ttu-id="3752d-687">Formatet **Excel\\Fil** legges automatisk til i det redigerbare formatet som et rotelement..</span><span class="sxs-lookup"><span data-stu-id="3752d-687">The **Excel\\File** format element is automatically added to the editable format as a root element.</span></span> <span data-ttu-id="3752d-688">I tillegg legges enten formatelementet **Excel\\Område** eller formatelementet **Excel\\Celle** til automatisk for hvert gjenkjente Excel-navn på den importert malen.</span><span class="sxs-lookup"><span data-stu-id="3752d-688">Additionally, either the **Excel\\Range** format element or the **Excel\\Cell** format element is automatically added for every recognized Excel name of the imported template.</span></span> <span data-ttu-id="3752d-689">Formatet **Excel\\Heode** som har det nestede **Streng**-elementet, legges til automatisk for å gjenspeile hodeinnstillingene i den importerte malen.</span><span class="sxs-lookup"><span data-stu-id="3752d-689">The **Excel\\Header** format that has the nested **String** element is automatically added to reflect the header settings of the imported template.</span></span>

![Formatstruktur som inkluderer automatisk tilføyde elementer i ER-operasjonsutforming](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a><span data-ttu-id="3752d-691">Konfigurere et format</span><span class="sxs-lookup"><span data-stu-id="3752d-691">Configure a format</span></span>

1. <span data-ttu-id="3752d-692">På siden **Formatutforming**, i formattreet, velger du **Excel**-rotelementet.</span><span class="sxs-lookup"><span data-stu-id="3752d-692">On the **Format designer** page, in the format tree, select the **Excel** root element.</span></span>
2. <span data-ttu-id="3752d-693">På **Format**-fanen til høyre på siden, i **Navn**-feltet angir du <a name="AddFormatRootElement"></a>**Rapport**.</span><span class="sxs-lookup"><span data-stu-id="3752d-693">On the **Format** tab on the right side of the page, in the **Name** field, enter <a name="AddFormatRootElement"></a>**Report**.</span></span>
3. <span data-ttu-id="3752d-694">I **Språkinnstilling**-feltet velger du **Brukerinnstilling** for å kjøre rapporten på brukerens foretrukne språk.</span><span class="sxs-lookup"><span data-stu-id="3752d-694">In the **Language preference** field, select **User preference** to run the report in the user's preferred language.</span></span>
4. <span data-ttu-id="3752d-695">I **Kulturinnstillinger**-feltet velger du **Brukerinnstilling** for å kjøre rapporten i brukerens foretrukne kultur.</span><span class="sxs-lookup"><span data-stu-id="3752d-695">In the **Culture preference** field, select **User preference** to run the report in the user's preferred culture.</span></span>

    <span data-ttu-id="3752d-696">Hvis du vil ha informasjon om hvordan du angir språk- og kulturkontekster for en ER-prosess, kan du se [Utforme flerspråklige rapporter](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="3752d-696">For information about how to specify the language and culture contexts for an ER process, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

    ![Konfigurere språk- og kulturinnstillinger for den utformede rapporten i ER-operasjonsutforming](./media/er-quick-start1-template-format-structure1.png)

5. <span data-ttu-id="3752d-698">Utvid rotnoden i formattreet, og velg deretter **ResultsGroup**.</span><span class="sxs-lookup"><span data-stu-id="3752d-698">In the format tree, expand the root node, and then select **ResultsGroup**.</span></span>
6. <span data-ttu-id="3752d-699">På **Format**-fanen i feltet **Replikeringsretning** velger du **Ingen replikering** fordi du ikke forventer å ha flere resultatgrupper for ett enkelt spørreskjema.</span><span class="sxs-lookup"><span data-stu-id="3752d-699">On the **Format** tab, in the **Replication direction** field, select **No replication**, because you don't expect to have multiple result groups for a single questionnaire.</span></span>

    ![Definere replikeringsretningen for Område-formatelementer i ER-operasjonsutforming](./media/er-quick-start1-template-format-structure2.png)

7. <span data-ttu-id="3752d-701">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3752d-701">Select **Save**.</span></span>

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a><span data-ttu-id="3752d-702">Definere databinding for en rapporttittel</span><span class="sxs-lookup"><span data-stu-id="3752d-702">Define the data binding for a report title</span></span>

<span data-ttu-id="3752d-703">Du må angi en databinding for et formatelement som brukes til å fylle ut tittelen til en generert rapport.</span><span class="sxs-lookup"><span data-stu-id="3752d-703">You must specify a data binding for a format element that is used to fill in the title of a generated report.</span></span>

1. <span data-ttu-id="3752d-704">På siden **Formatutforming**, på **Tilordning**-fanen til høyre, velger du elementet **Rapport\\ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="3752d-704">On the **Format designer** page, on the **Mapping** tab on the right, select the **Report\\ReportTitle** element.</span></span>
2. <span data-ttu-id="3752d-705">Velg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="3752d-705">Select **Edit formula**.</span></span>
3. <span data-ttu-id="3752d-706">Velg **Oversett** i formelredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="3752d-706">In the formula editor, select **Translate**.</span></span>
4. <span data-ttu-id="3752d-707">Følg disse trinnene i dialogboksen **Tekstoversettelse**:</span><span class="sxs-lookup"><span data-stu-id="3752d-707">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="3752d-708">I feltet **Etikett-ID** angir du **ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="3752d-708">In the **Label ID** field, enter **ReportTitle**.</span></span>
    2. <span data-ttu-id="3752d-709">I feltet **Tekst på standardspråk** angir du **Spørreskjemarapport**.</span><span class="sxs-lookup"><span data-stu-id="3752d-709">In the **Text in default language** field, enter **Questionnaires report**.</span></span>
    3. <span data-ttu-id="3752d-710">Velg **Oversett**, og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3752d-710">Select **Translate**, and then select **Save**.</span></span>
    4. <span data-ttu-id="3752d-711">Velg **Oversett** for å lukke dialogboksen **Tekstoversettelse**.</span><span class="sxs-lookup"><span data-stu-id="3752d-711">Select **Translate** to close the **Text translation** dialog box.</span></span>

5. <span data-ttu-id="3752d-712">Lukk formelredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="3752d-712">Close the formula editor.</span></span>

    ![Konfigurere bindingen for å fylle ut tittelen til en generert rapport](./media/er-quick-start1-add-report-title-label.png)

<span data-ttu-id="3752d-714">Du kan bruke denne metoden til å endre alle andre etiketter for gjeldende malspråk.</span><span class="sxs-lookup"><span data-stu-id="3752d-714">You can use this technique to make all other labels of the current template language-dependent.</span></span> <span data-ttu-id="3752d-715">Hvis du vil ha informasjon om hvordan de tilføyde etikettene for en enkelt ER-konfigurasjon kan oversettes til alle støttede språk, kan du se [Utforme flerspråklige rapporter](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="3752d-715">For information about how the added labels of a single ER configuration can be translated into all supported languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a><span data-ttu-id="3752d-716">Gå gjennom modelldatakilden</span><span class="sxs-lookup"><span data-stu-id="3752d-716">Review model data source</span></span>

1. <span data-ttu-id="3752d-717">På siden **Formatutforming**, på **Tilordning**-fanen, velger du <a name="ModelDSName"></a>**modell**-datakilden som representerer basisdatamodellen til dette ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="3752d-717">On the **Format designer** page, on the **Mapping** tab, select the <a name="ModelDSName"></a>**model** data source that represents the base data model of this ER format.</span></span>
2. <span data-ttu-id="3752d-718">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="3752d-718">Select **Edit**.</span></span>
3. <span data-ttu-id="3752d-719">Se gjennom informasjonen i dialogboksen **Egenskaper for datakilde**.</span><span class="sxs-lookup"><span data-stu-id="3752d-719">Review the information in the **Data source properties** dialog box.</span></span> <span data-ttu-id="3752d-720">Denne datakilden representerer versjon 1 av datamodellkomponenten **Spørreskjemaer** som ligger i ER-konfigurasjonen **Spørreskjemamodell**.</span><span class="sxs-lookup"><span data-stu-id="3752d-720">This data source represents version 1 of the **Questionnaires** data model component that resides in the **Questionnaires model** ER configuration.</span></span>

![Egenskaper for modelldatakilden i ER-operasjonsutforming](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a><span data-ttu-id="3752d-722">Binde formatelementer til datakildefelt</span><span class="sxs-lookup"><span data-stu-id="3752d-722">Bind format elements to data source fields</span></span>

<span data-ttu-id="3752d-723">Hvis du vil angi hvordan en mal skal fylles ut ved kjøring, må du binde hvert formatelement som er knyttet til et passende Excel-navn, til et enkelt felt i formatets datakilde.</span><span class="sxs-lookup"><span data-stu-id="3752d-723">To specify how a template is filled in at runtime, you must bind every format element that is associated with an appropriate Excel name to a single field of this format's data source.</span></span>

1. <span data-ttu-id="3752d-724">På siden **Formatutforming**, i formattreet, velger du formatelementet **Rapport\\CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="3752d-724">On the **Format designer** page, in the format tree, select the **Report\\CompanyName** format element.</span></span>
2. <span data-ttu-id="3752d-725">På **Tilordning**-fanen velger du datakildefeltet **model.CompanyName** for **Streng**-typen.</span><span class="sxs-lookup"><span data-stu-id="3752d-725">On the **Mapping** tab, select the **model.CompanyName** data source field of the **String** type.</span></span>
3. <span data-ttu-id="3752d-726">Velg **Bind** for å skrive inn et firmanavn i en mal.</span><span class="sxs-lookup"><span data-stu-id="3752d-726">Select **Bind** to enter a company name in a template.</span></span>
4. <span data-ttu-id="3752d-727">I formattreet velger du elementet **Rapport\\Spørreskjema**.</span><span class="sxs-lookup"><span data-stu-id="3752d-727">In the format tree, select the **Report\\Questionnaire** element.</span></span>
5. <span data-ttu-id="3752d-728">På **Tilordning**-fanen velger du datakildefeltet **model.Questionnaire** for **Postliste**-typen.</span><span class="sxs-lookup"><span data-stu-id="3752d-728">On the **Mapping** tab, select the **model.Questionnaire** data source field of the **Record list** type.</span></span>
6. <span data-ttu-id="3752d-729">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="3752d-729">Select **Bind**.</span></span>
7. <span data-ttu-id="3752d-730">Velg **Vis detaljer** for å se flere detaljer for formatelementer.</span><span class="sxs-lookup"><span data-stu-id="3752d-730">Select **Show details** to see more details for format elements.</span></span>

    <span data-ttu-id="3752d-731">Formatelementet for **Spørreskjema**-området konfigureres som vertikalt replikert.</span><span class="sxs-lookup"><span data-stu-id="3752d-731">The **Questionnaire** range format element is configured as vertically replicated.</span></span> <span data-ttu-id="3752d-732">Når det er bundet til en datakilde av typen **Postliste**, gjentas det aktuelle **Spørreskjema**-området for Excel-malen for hver post i den bundne datakilden.</span><span class="sxs-lookup"><span data-stu-id="3752d-732">When it's bound to a data source of the **Record list** type, the appropriate **Questionnaire** range of the Excel template is repeated for every record of the bound data source.</span></span>
 
    ![Binde formatelementet Spørreskjema-område til de riktige datakildene for postliste i ER-operasjonsutforming](./media/er-quick-start1-bindings1.png)

    <span data-ttu-id="3752d-734">Siden **Spørreskjema**-området i Excel-malen er definert fra rad 5 til og med rad 14, gjentas disse radene for hvert rapporterte spørreskjema.</span><span class="sxs-lookup"><span data-stu-id="3752d-734">Because the **Questionnaire** range of the Excel template is defined between rows 5 through 14, these rows are repeated for every reported questionnaire.</span></span>

    ![Rader i Excel-malen som blir gjentatt i en generert rapport for hver post i datakildene for postliste](./media/er-quick-start1-template-questionnaire-range.png)

8. <span data-ttu-id="3752d-736">Konfigurer lignende bindinger for de gjenværende formatelementene, som beskrevet i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="3752d-736">Configure similar bindings for the remaining format elements, as described in the following table.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3752d-737">I denne tabellen antar informasjonen i kolonnen "Datakildebane" at ER-funksjonen [Relativ bane](relative-path-data-bindings-er-models-format.md) er aktivert.</span><span class="sxs-lookup"><span data-stu-id="3752d-737">In this table, the information in the "Data source path" column assumes that the [relative path](relative-path-data-bindings-er-models-format.md) ER feature is turned on.</span></span>

    | <span data-ttu-id="3752d-738">Formatelementbane</span><span class="sxs-lookup"><span data-stu-id="3752d-738">Format element path</span></span>                                      | <span data-ttu-id="3752d-739">Datakildebane</span><span class="sxs-lookup"><span data-stu-id="3752d-739">Data source path</span></span> |
    |----------------------------------------------------------|------------------|
    | <span data-ttu-id="3752d-740">Excel\\ReportTitle</span><span class="sxs-lookup"><span data-stu-id="3752d-740">Excel\\ReportTitle</span></span>                                       | <span data-ttu-id="3752d-741">**\@"GER\_LABEL:ReportTitle"**</span><span class="sxs-lookup"><span data-stu-id="3752d-741">**\@"GER\_LABEL:ReportTitle"**</span></span> |
    | <span data-ttu-id="3752d-742">Excel\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="3752d-742">Excel\\CompanyName</span></span>                                       | <span data-ttu-id="3752d-743">**model.CompanyName**</span><span class="sxs-lookup"><span data-stu-id="3752d-743">**model.CompanyName**</span></span> |
    | <span data-ttu-id="3752d-744">Excel\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="3752d-744">Excel\\Questionnaire</span></span>                                     | <span data-ttu-id="3752d-745">**model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="3752d-745">**model.Questionnaire**</span></span> |
    | <span data-ttu-id="3752d-746">Excel\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="3752d-746">Excel\\Questionnaire\\Active</span></span>                             | <span data-ttu-id="3752d-747">**\@.Active**, der **\@** er **model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="3752d-747">**\@.Active**, where **\@** is **model.Questionnaire**</span></span> |
    | <span data-ttu-id="3752d-748">Excel\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="3752d-748">Excel\\Questionnaire\\Code</span></span>                               | <span data-ttu-id="3752d-749">**\@.Code**</span><span class="sxs-lookup"><span data-stu-id="3752d-749">**\@.Code**</span></span> |
    | <span data-ttu-id="3752d-750">Excel\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="3752d-750">Excel\\Questionnaire\\Description</span></span>                        | <span data-ttu-id="3752d-751">**\@.Description**</span><span class="sxs-lookup"><span data-stu-id="3752d-751">**\@.Description**</span></span> |
    | <span data-ttu-id="3752d-752">Excel\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="3752d-752">Excel\\Questionnaire\\QuestionnaireType</span></span>                  | <span data-ttu-id="3752d-753">**\@.QuestionnaireType**</span><span class="sxs-lookup"><span data-stu-id="3752d-753">**\@.QuestionnaireType**</span></span> |
    | <span data-ttu-id="3752d-754">Excel\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="3752d-754">Excel\\Questionnaire\\QuestionOrder</span></span>                      | <span data-ttu-id="3752d-755">**\@.QuestionOrder**</span><span class="sxs-lookup"><span data-stu-id="3752d-755">**\@.QuestionOrder**</span></span> |
    | <span data-ttu-id="3752d-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span><span class="sxs-lookup"><span data-stu-id="3752d-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span></span>               | <span data-ttu-id="3752d-757">**\@.ResultsGroup.Code**</span><span class="sxs-lookup"><span data-stu-id="3752d-757">**\@.ResultsGroup.Code**</span></span> |
    | <span data-ttu-id="3752d-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span><span class="sxs-lookup"><span data-stu-id="3752d-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span></span>        | <span data-ttu-id="3752d-759">**\@.ResultsGroup.Description**</span><span class="sxs-lookup"><span data-stu-id="3752d-759">**\@.ResultsGroup.Description**</span></span> |
    | <span data-ttu-id="3752d-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="3752d-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>    | <span data-ttu-id="3752d-761">**\@.ResultsGroup.MaxNumberOfPoint**</span><span class="sxs-lookup"><span data-stu-id="3752d-761">**\@.ResultsGroup.MaxNumberOfPoint**</span></span> |
    | <span data-ttu-id="3752d-762">Excel\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="3752d-762">Excel\\Questionnaire\\Question</span></span>                           | <span data-ttu-id="3752d-763">**\@.Question**</span><span class="sxs-lookup"><span data-stu-id="3752d-763">**\@.Question**</span></span> |
    | <span data-ttu-id="3752d-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="3752d-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span></span> | <span data-ttu-id="3752d-765">**\@.CollectionSequenceNumber**, der **\@** er **model.Questionnaire.Question**</span><span class="sxs-lookup"><span data-stu-id="3752d-765">**\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question**</span></span> |
    | <span data-ttu-id="3752d-766">Excel\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="3752d-766">Excel\\Questionnaire\\Question\\Id</span></span>                       | <span data-ttu-id="3752d-767">**\@.Id**</span><span class="sxs-lookup"><span data-stu-id="3752d-767">**\@.Id**</span></span> |
    | <span data-ttu-id="3752d-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="3752d-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span></span>          | <span data-ttu-id="3752d-769">**\@.MustBeCompleted**</span><span class="sxs-lookup"><span data-stu-id="3752d-769">**\@.MustBeCompleted**</span></span> |
    | <span data-ttu-id="3752d-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="3752d-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span></span>          | <span data-ttu-id="3752d-771">**\@.PrimaryQuestion**</span><span class="sxs-lookup"><span data-stu-id="3752d-771">**\@.PrimaryQuestion**</span></span> |
    | <span data-ttu-id="3752d-772">Excel\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="3752d-772">Excel\\Questionnaire\\Question\\SequenceNumber</span></span>           | <span data-ttu-id="3752d-773">**\@.SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="3752d-773">**\@.SequenceNumber**</span></span> |
    | <span data-ttu-id="3752d-774">Excel\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="3752d-774">Excel\\Questionnaire\\Question\\Text</span></span>                     | <span data-ttu-id="3752d-775">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="3752d-775">**\@.Text**</span></span> |
    | <span data-ttu-id="3752d-776">Excel\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="3752d-776">Excel\\Questionnaire\\Question\\Answer</span></span>                   | <span data-ttu-id="3752d-777">**\@.Answer**</span><span class="sxs-lookup"><span data-stu-id="3752d-777">**\@.Answer**</span></span> |
    | <span data-ttu-id="3752d-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="3752d-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>    | <span data-ttu-id="3752d-779">**\@.CorrectAnswer**, der **\@** er **model.Questionnaire.Answer**</span><span class="sxs-lookup"><span data-stu-id="3752d-779">**\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer**</span></span> |
    | <span data-ttu-id="3752d-780">Excel\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="3752d-780">Excel\\Questionnaire\\Question\\Answer\\Points</span></span>           | <span data-ttu-id="3752d-781">**\@.Points**</span><span class="sxs-lookup"><span data-stu-id="3752d-781">**\@.Points**</span></span> |
    | <span data-ttu-id="3752d-782">Excel\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="3752d-782">Excel\\Questionnaire\\Question\\Answer\\Text</span></span>             | <span data-ttu-id="3752d-783">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="3752d-783">**\@.Text**</span></span> |

9. <span data-ttu-id="3752d-784">Når du er ferdig, velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3752d-784">When you've finished, select **Save**.</span></span>

<span data-ttu-id="3752d-785">Den følgende illustrasjonen viser den endelige tilstanden til de konfigurerte databindingene på siden **Formatutforming**.</span><span class="sxs-lookup"><span data-stu-id="3752d-785">The following illustration shows the final state of the configured data bindings on the **Format designer** page.</span></span>

![Konfigurerte databindinger i ER-datamodellutforming](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> <span data-ttu-id="3752d-787">Hele samlingen av angitte datakilder og bindinger representerer en formattilordningskomponent i det konfigurerte formatet.</span><span class="sxs-lookup"><span data-stu-id="3752d-787">The whole collection of specified data sources and bindings represents a format mapping component of the configured format.</span></span> <span data-ttu-id="3752d-788">Denne formattilordningen kalles når du kjører det konfigurerte formatet for rapportgenerering.</span><span class="sxs-lookup"><span data-stu-id="3752d-788">This format mapping is called when you run the configured format for report generation.</span></span>

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a><span data-ttu-id="3752d-789">Kjøre et designet format fra ER</span><span class="sxs-lookup"><span data-stu-id="3752d-789">Run a designed format from ER</span></span>

<span data-ttu-id="3752d-790">Du kan nå kjøre et designet format for testformål fra **Konfigurasjoner**-siden.</span><span class="sxs-lookup"><span data-stu-id="3752d-790">You can now run a designed format for testing purposes from the **Configurations** page.</span></span>

1. <span data-ttu-id="3752d-791">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="3752d-791">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="3752d-792">På **Konfigurasjon**-siden, i konfigurasjonstreet i venstre rute, utvider du **Spørreskjemamodell** og velger **Spørreskjemarapport**.</span><span class="sxs-lookup"><span data-stu-id="3752d-792">On the **Configuration** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="3752d-793">Velg **Utforming** for formatversjonen som har statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="3752d-793">Select **Designer** for the format version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="3752d-794">På **Formatutforming**-siden velger du **Kjør**.</span><span class="sxs-lookup"><span data-stu-id="3752d-794">On the **Format designer** page, select **Run**.</span></span>
5. <span data-ttu-id="3752d-795">I dialogboksen **ER-parametere**, på hurtigfanen **Poster som skal inkluderes**, konfigurerer du filtreringsalternativet slik at bare **SBCCrsExam**-spørreskjemaet er inkludert.</span><span class="sxs-lookup"><span data-stu-id="3752d-795">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
6. <span data-ttu-id="3752d-796">Velg **OK** for å bekrefte filtreringsalternativet.</span><span class="sxs-lookup"><span data-stu-id="3752d-796">Select **OK** to confirm the filtering option.</span></span>
7. <span data-ttu-id="3752d-797">Velg **OK** for å kjøre rapporten.</span><span class="sxs-lookup"><span data-stu-id="3752d-797">Select **OK** to run the report.</span></span>
8. <span data-ttu-id="3752d-798">Gå gjennom den genererte rapporten.</span><span class="sxs-lookup"><span data-stu-id="3752d-798">Review the generated report.</span></span>

<span data-ttu-id="3752d-799">Som [standard](electronic-reporting-destinations.md#default-behavior) leveres en generert rapport som en Excel-fil du kan laste ned.</span><span class="sxs-lookup"><span data-stu-id="3752d-799">By [default](electronic-reporting-destinations.md#default-behavior), a generated report is delivered as an Excel file that you can download.</span></span> <span data-ttu-id="3752d-800">Illustrasjonen nedenfor viser to sider i den genererte rapporten i Excel-format.</span><span class="sxs-lookup"><span data-stu-id="3752d-800">The following illustrations show two pages of the generated report in Excel format.</span></span>

![Eksempel på en generert rapport i Excel-format, side 1](./media/er-quick-start1-report1a.png)

![Eksempel på en generert rapport i Excel-format, side 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a><span data-ttu-id="3752d-803">Justere et designet format</span><span class="sxs-lookup"><span data-stu-id="3752d-803">Tune a designed format</span></span>

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a><span data-ttu-id="3752d-804">Endre et format for å endre navnet på et generert dokument</span><span class="sxs-lookup"><span data-stu-id="3752d-804">Modify a format to change the name of a generated document</span></span>

<span data-ttu-id="3752d-805">Som standard navngis et generert dokument ved å bruke aliaset til den gjeldende brukeren.</span><span class="sxs-lookup"><span data-stu-id="3752d-805">By default, a generated document is named by using the alias of the current user.</span></span> <span data-ttu-id="3752d-806">Når du endrer formatet, kan du endre denne virkemåten slik at et generert dokument navngis basert på den egendefinerte logikken.</span><span class="sxs-lookup"><span data-stu-id="3752d-806">By modifying the format, you can change this behavior so that a generated document is named based on your custom logic.</span></span> <span data-ttu-id="3752d-807">Navnet på et generert dokument kan for eksempel være basert på gjeldende dato og klokkeslett for en økt, og på rapportens tittel.</span><span class="sxs-lookup"><span data-stu-id="3752d-807">For example, the name of a generated document can be based on the current session date and time, and on the report's title.</span></span>

1. <span data-ttu-id="3752d-808">På siden **Formatutforming** velger du rotelementet **Rapport**.</span><span class="sxs-lookup"><span data-stu-id="3752d-808">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="3752d-809">På **Tilordning**-fanen velger du **Rediger filnavn**.</span><span class="sxs-lookup"><span data-stu-id="3752d-809">On the **Mapping** tab, select **Edit file name**.</span></span>
3. <span data-ttu-id="3752d-810">I **Formel**-feltet skriver du inn **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span><span class="sxs-lookup"><span data-stu-id="3752d-810">In the **Formula** field, enter **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span></span>
4. <span data-ttu-id="3752d-811">Velg **Lagre**, og lukk formelredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="3752d-811">Select **Save**, and close the formula editor.</span></span>
5. <span data-ttu-id="3752d-812">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3752d-812">Select **Save**.</span></span>

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a><span data-ttu-id="3752d-813">Endre et format for å endre rekkefølgen på spørsmål</span><span class="sxs-lookup"><span data-stu-id="3752d-813">Modify a format to change the order of questions</span></span>

<span data-ttu-id="3752d-814">Spørsmålene er ikke riktig sortert i en generert rapport.</span><span class="sxs-lookup"><span data-stu-id="3752d-814">The questions aren't correctly ordered in a generated report.</span></span> <span data-ttu-id="3752d-815">Du kan endre rekkefølgen ved å endre formatet.</span><span class="sxs-lookup"><span data-stu-id="3752d-815">You can change the order by modifying the format.</span></span>

1. <span data-ttu-id="3752d-816">På siden **Formatutforming** velger du rotelementet **Rapport**.</span><span class="sxs-lookup"><span data-stu-id="3752d-816">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="3752d-817">På **Tilordning**-fanen i formattreet utvider du **Rapport\\Spørreskjema\\Spørsmål**.</span><span class="sxs-lookup"><span data-stu-id="3752d-817">On the **Mapping** tab, in the format tree, expand **Report\\Questionnaire\\Question**.</span></span>

    ![Spørsmål-formatelement for Område-typen i ER-operasjonsutforming](./media/er-quick-start1-bindings3.png)

3. <span data-ttu-id="3752d-819">På **Tilordning**-fanen velger du **model.Questionnaire**.</span><span class="sxs-lookup"><span data-stu-id="3752d-819">On the **Mapping** tab, select **model.Questionnaire**.</span></span>
4. <span data-ttu-id="3752d-820">Velg **Legg til** \> **Funksjoner\\Beregnet felt**, og skriv deretter inn **OrderedQuestions** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-820">Select **Add** \> **Functions\\Calculated field**, and then, in the **Name** field, enter **OrderedQuestions**.</span></span>
5. <span data-ttu-id="3752d-821">Velg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="3752d-821">Select **Edit formula**.</span></span>
6. <span data-ttu-id="3752d-822">I formularedigeringsprogrammet, i **Formel**-feltet, skriver du inn **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** for å sortere listen over spørsmål i det gjeldende spørreskjemaet etter sekvensordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="3752d-822">In the formula editor, in the **Formula** field, enter **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** to order the list of questions of the current questionnaire by the sequence order number.</span></span>
7. <span data-ttu-id="3752d-823">Velg **Lagre**, og lukk formelredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="3752d-823">Select **Save**, and close the formula editor.</span></span>
8. <span data-ttu-id="3752d-824">Velg **OK** for å fullføre registreringen av et nytt beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="3752d-824">Select **OK** to complete the entry of a new calculated field.</span></span>
9. <span data-ttu-id="3752d-825">På **Tilordning**-fanen velger du **model.Questionnaire.OrderedQuestions**.</span><span class="sxs-lookup"><span data-stu-id="3752d-825">On the **Mapping** tab, select **model.Questionnaire.OrderedQuestions**.</span></span>
10. <span data-ttu-id="3752d-826">I formattreet velger du **Excel\\Spørreskjema\\Spørsmål**.</span><span class="sxs-lookup"><span data-stu-id="3752d-826">In the format tree, select **Excel\\Questionnaire\\Question**.</span></span>
11. <span data-ttu-id="3752d-827">Velg **Bind**, og bekreft deretter at den gjeldende banen **model.Questionnaire.Questions** er erstattet av den nye banen **model.Questionnaire.OrderedQuestions** i alle bindinger av nestede elementer.</span><span class="sxs-lookup"><span data-stu-id="3752d-827">Select **Bind**, and then confirm that the current **model.Questionnaire.Questions** path is replaced by the new **model.Questionnaire.OrderedQuestions** path in all bindings of nested elements.</span></span>
12. <span data-ttu-id="3752d-828">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3752d-828">Select **Save**.</span></span>

![Binde Spørsmål-formatelementet til den konfigurerte OrderedQuestions-datakilden i ER-operasjonsutforming](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a><span data-ttu-id="3752d-830">Kjøre et endret format fra ER</span><span class="sxs-lookup"><span data-stu-id="3752d-830">Run a modified format from ER</span></span>

<span data-ttu-id="3752d-831">Du kan nå kjøre et endret format for testformål fra ER-rammeverket.</span><span class="sxs-lookup"><span data-stu-id="3752d-831">You can now run a modified format for testing purposes from the ER framework.</span></span>

1. <span data-ttu-id="3752d-832">På **Formatutforming**-siden velger du **Kjør**.</span><span class="sxs-lookup"><span data-stu-id="3752d-832">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="3752d-833">I dialogboksen **ER-parametere**, på hurtigfanen **Poster som skal inkluderes**, konfigurerer du filtreringsalternativet slik at bare **SBCCrsExam**-spørreskjemaet er inkludert.</span><span class="sxs-lookup"><span data-stu-id="3752d-833">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
3. <span data-ttu-id="3752d-834">Velg **OK** for å bekrefte filtreringsalternativet.</span><span class="sxs-lookup"><span data-stu-id="3752d-834">Select **OK** to confirm the filtering option.</span></span>
4. <span data-ttu-id="3752d-835">Velg **OK** for å kjøre rapporten.</span><span class="sxs-lookup"><span data-stu-id="3752d-835">Select **OK** to run the report.</span></span>
5. <span data-ttu-id="3752d-836">Gå gjennom den genererte rapporten.</span><span class="sxs-lookup"><span data-stu-id="3752d-836">Review the generated report.</span></span>

<span data-ttu-id="3752d-837">Den følgende illustrasjonen viser en generert rapport i Excel-format der spørsmålene er riktig sortert.</span><span class="sxs-lookup"><span data-stu-id="3752d-837">The following illustration shows a generated report in Excel format where the questions are correctly ordered.</span></span>

![Generert rapport i Excel-format som har spørsmål som er riktig sortert](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a><span data-ttu-id="3752d-839">Fullføre formatutformingen</span><span class="sxs-lookup"><span data-stu-id="3752d-839">Complete the format design</span></span>

1. <span data-ttu-id="3752d-840">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="3752d-840">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="3752d-841">På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Spørreskjemamodell** og velger **Spørreskjemarapport**.</span><span class="sxs-lookup"><span data-stu-id="3752d-841">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="3752d-842">I hurtigfanen **Versjoner** velger du konfigurasjonsversjonen med statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="3752d-842">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="3752d-843">Velg **Endre status** \> **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="3752d-843">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="3752d-844">Statusen til versjon 1.1 av denne konfigurasjonen endres fra **Utkast** til **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="3752d-844">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="3752d-845">Versjon 1.1 kan ikke lenger endres.</span><span class="sxs-lookup"><span data-stu-id="3752d-845">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="3752d-846">Denne versjonen inneholder formatet som er konfigurert, og kan brukes til å skrive ut den egendefinerte rapporten.</span><span class="sxs-lookup"><span data-stu-id="3752d-846">This version contains the configured format and can be used to print your custom report.</span></span> <span data-ttu-id="3752d-847">Versjon 1.2 av denne konfigurasjonen opprettes og har statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="3752d-847">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="3752d-848">Du kan redigere denne versjonen for å justere formatet til **Spørreskjema**-rapporten.</span><span class="sxs-lookup"><span data-stu-id="3752d-848">You can edit this version to adjust the format of your **Questionnaire** report.</span></span>

![Redigerbar ER-konfigurasjon på Konfigurasjoner-siden](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> <span data-ttu-id="3752d-850">Det konfigurerte formatet er din utforming av **Spørreskjema**-rapporten og inneholder ingen relasjoner til de Finance-spesifikke artefaktene.</span><span class="sxs-lookup"><span data-stu-id="3752d-850">The configured format is your design of the **Questionnaire** report and contains no relations to the Finance-specific artefacts.</span></span>

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a><span data-ttu-id="3752d-851">Utarbeide appartefakter for å kalle den utformede rapporten</span><span class="sxs-lookup"><span data-stu-id="3752d-851">Develop application artefacts to call the designed report</span></span>

<span data-ttu-id="3752d-852">Som en bruker i Systemansvarlig-rollen må du utvikle ny logikk slik at det konfigurerte ER-formatet kan kalles fra brukergrensesnittet (UI) i appen for å generere den egendefinerte rapporten.</span><span class="sxs-lookup"><span data-stu-id="3752d-852">As a user in the System Administrator role, you must develop new logic so that the configured ER format can be called from the application user interface (UI) to generate your custom report.</span></span> <span data-ttu-id="3752d-853">For øyeblikket tilbyr ikke ER funksjonalitet for å konfigurere denne typen logikk.</span><span class="sxs-lookup"><span data-stu-id="3752d-853">Currently, ER doesn't offer any capability for configuring this type of logic.</span></span> <span data-ttu-id="3752d-854">Derfor kreves noe utviklingsarbeid.</span><span class="sxs-lookup"><span data-stu-id="3752d-854">Therefore, some engineering work is required.</span></span> 

<span data-ttu-id="3752d-855">For å utvikle den nye logikken må du distribuere en topologi som støtter fortløpende bygging.</span><span class="sxs-lookup"><span data-stu-id="3752d-855">To develop the new logic, you must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="3752d-856">Hvis du vil ha mer informasjon, kan du se [Distribuere topologier som støtter sammenhengende automatisering av bygging og testing](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="3752d-856">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span> <span data-ttu-id="3752d-857">Du må også ha tilgang til utviklingsmiljøet for denne topologien.</span><span class="sxs-lookup"><span data-stu-id="3752d-857">You must also have access to the development environment for this topology.</span></span> <span data-ttu-id="3752d-858">Hvis du vil ha mer informasjon om det tilgjengelige API-et for ER, kan du se [API for ER-rammeverk](er-apis-app73.md).</span><span class="sxs-lookup"><span data-stu-id="3752d-858">For more information about the available ER API, see [ER framework API](er-apis-app73.md).</span></span>

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a><span data-ttu-id="3752d-859">Endre kildekode</span><span class="sxs-lookup"><span data-stu-id="3752d-859">Modify source code</span></span>

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a><span data-ttu-id="3752d-860">Legge til en datakontraktklasse</span><span class="sxs-lookup"><span data-stu-id="3752d-860">Add a data contract class</span></span>

<span data-ttu-id="3752d-861">Legg til den nye **QuestionnairesErReportContract**-klassen i Microsoft Visual Studio-prosjektet ditt, og skriv kode som spesifiserer datakontrakten som skal brukes til å kjøre det konfigurert ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="3752d-861">Add the new **QuestionnairesErReportContract** class to your Microsoft Visual Studio project, and write code that specifies the data contract that should be used to run the configured ER format.</span></span>

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a><span data-ttu-id="3752d-862">Legge til en grensesnittbyggerklasse</span><span class="sxs-lookup"><span data-stu-id="3752d-862">Add a UI builder class</span></span>

<span data-ttu-id="3752d-863">Legg til den nye **QuestionnairesErReportUIBuilder**-klassen i Visual Studio-prosjektet ditt, og skriv kode for å generere en dialogboks for kjøretid som skal brukes til å slå opp formattilordnings-ID-en for ER-formatet som må kjøres.</span><span class="sxs-lookup"><span data-stu-id="3752d-863">Add the new **QuestionnairesErReportUIBuilder** class to your Visual Studio project, and write code to generate a runtime dialog box that will be used to look up the format mapping ID of the ER format that must be run.</span></span> <span data-ttu-id="3752d-864">Den angitte koden slår bare opp ER-formater som inneholder en datakilde av typen **Datamodell** som refererer til **[Spørreskjemaer](#DataModeName)**-datamodellen ved å bruke **[Rot](#RootDefinitionName)**-definisjonen.</span><span class="sxs-lookup"><span data-stu-id="3752d-864">The provided code looks up only ER formats that contain a data source of the **Data model** type that refers to the **[Questionnaires](#DataModeName)** data model by using the **[Root](#RootDefinitionName)** definition.</span></span>

> [!NOTE]
> <span data-ttu-id="3752d-865">Du kan også bruke ER-integreringspunkter til å filtrere ER-formater.</span><span class="sxs-lookup"><span data-stu-id="3752d-865">Alternatively, you can use ER integration points to filter ER formats.</span></span> <span data-ttu-id="3752d-866">Hvis du vil ha mer informasjon, kan du se [API for å vise et formattilordningssoppslag](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span><span class="sxs-lookup"><span data-stu-id="3752d-866">For more information, see [API to show a format mapping lookup](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span></span>

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a><span data-ttu-id="3752d-867">Legge til en dataleverandørklasse</span><span class="sxs-lookup"><span data-stu-id="3752d-867">Add a data provider class</span></span>

<span data-ttu-id="3752d-868">Legg til den nye **QuestionnairesErReportDP**-klassen i Visual Studio-prosjektet ditt, og skriv kode som introduserer dataleverandøren som skal brukes til å kjøre det konfigurerte ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="3752d-868">Add the new **QuestionnairesErReportDP** class to your Visual Studio project, and write code that introduces the data provider that should used to run the configured ER format.</span></span> <span data-ttu-id="3752d-869">Den angitte koden inkluderer bare datakontrakten for denne dataleverandøren.</span><span class="sxs-lookup"><span data-stu-id="3752d-869">The provided code includes only the data contract for this data provider.</span></span>

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a><span data-ttu-id="3752d-870">Legge til en etikettfil</span><span class="sxs-lookup"><span data-stu-id="3752d-870">Add a labels file</span></span>

<span data-ttu-id="3752d-871">Legg til den nye **QuestionnairesErReportLabels\_nb-NO**-etikettfilen i Visual Studio-prosjektet ditt, og angi følgende etiketter for nye UI-ressurser:</span><span class="sxs-lookup"><span data-stu-id="3752d-871">Add the new **QuestionnairesErReportLabels\_en-US** labels file to your Visual Studio project, and specify the following labels for new UI resources:</span></span>

- <span data-ttu-id="3752d-872">**\@QuestionnairesReport**-etiketten for et nytt menyelement som inneholder følgende tekst på norsk (nb-NO): **Spørreskjemarapport (drevet av ER)**</span><span class="sxs-lookup"><span data-stu-id="3752d-872">The **\@QuestionnairesReport** label for a new menu item that contains the following text in US English (en-US): **Questionnaires report (powered by ER)**</span></span>
- <span data-ttu-id="3752d-873">**\@QuestionnairesReportBatchJobDescription**-etiketten for tittelen på en satsvis jobb hvis et valgt ER-format er planlagt for kjøring som en satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="3752d-873">The **\@QuestionnairesReportBatchJobDescription** label for a batch job title if a selected ER format is scheduled for execution as a batch job</span></span>

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a><span data-ttu-id="3752d-874">Legge til en rapporttjenesteklasse</span><span class="sxs-lookup"><span data-stu-id="3752d-874">Add a report service class</span></span>

<span data-ttu-id="3752d-875">Legg til den nye **QuestionnairesErReportService**-klassen i Visual Studio-prosjektet ditt, og skriv kode som kaller opp et ER-format, identifiserer det med en formattilordnings-ID og leverer en datakontrakt som en parameter.</span><span class="sxs-lookup"><span data-stu-id="3752d-875">Add the new **QuestionnairesErReportService** class to your Visual Studio project, and write code that calls an ER format, identifies it by a format mapping ID, and provides a data contract as a parameter.</span></span>

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

<span data-ttu-id="3752d-876">Når du må bruke et ER-format som kjører appdata, må du konfigurere en datakilde av typen **Datamodell** i formattilordningen.</span><span class="sxs-lookup"><span data-stu-id="3752d-876">When you must use an ER format that runs application data, you must configure a data source of the **Data model** type in the format mapping.</span></span> <span data-ttu-id="3752d-877">Denne datakilden refererer til en bestemt del av den angitte datamodellen ved hjelp av én enkelt rotdefinisjon.</span><span class="sxs-lookup"><span data-stu-id="3752d-877">This data source refers to a specific part of the specified data model by using a single root definition.</span></span> <span data-ttu-id="3752d-878">Når ER-formatet kjøres, kaller det denne datakilden for å få tilgang til den riktige ER-modelltilordningen som er konfigurert for en angitt modell og rotdefinisjon.</span><span class="sxs-lookup"><span data-stu-id="3752d-878">When the ER format is run, it calls this data source to access the appropriate ER model mapping that is configured for a given model and root definition.</span></span>

<span data-ttu-id="3752d-879">All informasjon du kanskje forbereder i kildekoden og lageret som en del av datakontrakten, kan sendes til det aktive ER-formatet ved å bruke en ER-modelltilordning av denne typen.</span><span class="sxs-lookup"><span data-stu-id="3752d-879">All the information that you might prepare in the source code and store as part of the data contract can be passed to the running ER format by using an ER model mapping of this type.</span></span> <span data-ttu-id="3752d-880">I ER-modelltilordningen må du konfigurere en datakilde av typen **Objekt** som refererer til **[QuestionnairesErReportContract](#DataContractClass)**-klassen.</span><span class="sxs-lookup"><span data-stu-id="3752d-880">In the ER model mapping, you must configure a data source of the **Object** type that refers to the **[QuestionnairesErReportContract](#DataContractClass)** class.</span></span> <span data-ttu-id="3752d-881">Hvis du vil identifisere en modelltilordning, må du angi en datakilde som kaller denne modelltilordningen.</span><span class="sxs-lookup"><span data-stu-id="3752d-881">To identify a model mapping, you must specify a data source that calls this model mapping.</span></span> <span data-ttu-id="3752d-882">I den angitte koden er denne datakilden angitt av **ERModelDataSourceName**-konstanten som har **[modell](#ModelDSName)**-verdien.</span><span class="sxs-lookup"><span data-stu-id="3752d-882">In the provided code, this data source specified by the **ERModelDataSourceName** constant that has the **[model](#ModelDSName)** value.</span></span> <span data-ttu-id="3752d-883">Hvis du vil identifisere hvilken datakilde som brukes til å eksponere datakontrakten i modelltilordningen, må du angi et datakildenavn.</span><span class="sxs-lookup"><span data-stu-id="3752d-883">To identify which data source is used to expose the data contract in the model mapping, you must specify a data source name.</span></span> <span data-ttu-id="3752d-884">I den angitte koden er dette navnet datakilden angitt av **ParametersDataSourceName**-konstanten som har <a name="DataContractDSName"></a>**RunTimeParameters**-verdien.</span><span class="sxs-lookup"><span data-stu-id="3752d-884">In the provided code, this name is specified by the **ParametersDataSourceName** constant that has <a name="DataContractDSName"></a>**RunTimeParameters** value.</span></span>

> [!NOTE]
> <span data-ttu-id="3752d-885">I et nytt miljø må du kanskje oppdatere ER-metadataene, slik at denne typen klasse er tilgjengelig i ER-modelltilordningsutformingen.</span><span class="sxs-lookup"><span data-stu-id="3752d-885">In a new environment, you might have to refresh the ER metadata so that this type of class is available in the ER model mapping designer.</span></span> <span data-ttu-id="3752d-886">Hvis du vil ha mer informasjon, kan du se [Konfigurere ER-rammeverket](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="3752d-886">For more information, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span></span>

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a><span data-ttu-id="3752d-887">Legge til en rapportkontrollerklasse</span><span class="sxs-lookup"><span data-stu-id="3752d-887">Add a report controller class</span></span>

<span data-ttu-id="3752d-888">Legg til den nye **QuestionnairesErReportController**-klassen i Visual Studio-prosjektet ditt, og skriv kode som kjører et ER-format i enten synkron modus eller satsvis modus, som du foretrekker, i dialogboksen som er bygd basert på logikken til den angitte **QuestionnairesErReportUIBuilder**-klassen.</span><span class="sxs-lookup"><span data-stu-id="3752d-888">Add the new **QuestionnairesErReportController** class to your Visual Studio project, and write code that runs an ER format in either synchronous mode or batch mode, as you prefer, in the dialog box that is built based on the logic of the provided **QuestionnairesErReportUIBuilder** class.</span></span>

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a><span data-ttu-id="3752d-889">Legge til et menyelement</span><span class="sxs-lookup"><span data-stu-id="3752d-889">Add a menu item</span></span>

<span data-ttu-id="3752d-890">Legg til det nye menyelementet **QuestionnairesErReport** i Visual Studio-prosjektet ditt.</span><span class="sxs-lookup"><span data-stu-id="3752d-890">Add the new **QuestionnairesErReport** menu item to your Visual Studio project.</span></span> <span data-ttu-id="3752d-891">I **Objekt**-egenskapen refererer dette menyelementet til **QuestionnairesErReportController**-klassen, og det brukes til å angi en brukertillatelse for å velge og kjøre et ER-format.</span><span class="sxs-lookup"><span data-stu-id="3752d-891">In the **Object** property, this menu item refers to the **QuestionnairesErReportController** class, and it's used to specify a user permission to select and run an ER format.</span></span> <span data-ttu-id="3752d-892">I **Etikett**-egenskapen refererer dette menyelementet til **\@QuestionnairesReport**-etiketten du opprettet tidligere, slik at riktig tekst vises i appgrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="3752d-892">In the **Label** property, this menu item refers to the **\@QuestionnairesReport** label that you created earlier, so that correct text is presented in the application UI.</span></span>

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a><span data-ttu-id="3752d-893">Legge til et menyelement i en meny</span><span class="sxs-lookup"><span data-stu-id="3752d-893">Add a menu item to a menu</span></span>

<span data-ttu-id="3752d-894">Legg til den eksisterende **KM**-menyen i Visual Studio-prosjektet ditt.</span><span class="sxs-lookup"><span data-stu-id="3752d-894">Add the existing **KM** menu to your Visual Studio project.</span></span> <span data-ttu-id="3752d-895">Du må legge til et nytt **QuestionnairesErReport**-element av typen **Utdata** på denne menyen.</span><span class="sxs-lookup"><span data-stu-id="3752d-895">You must add a new **QuestionnairesErReport** item of the **Output** type to this menu.</span></span> <span data-ttu-id="3752d-896">Dette elementet må referere til menyelementet **QuestionnairesErReport** som er beskrevet i den forrige delen.</span><span class="sxs-lookup"><span data-stu-id="3752d-896">This item must refer to the **QuestionnairesErReport** menu item that is described in the previous section.</span></span>

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a><span data-ttu-id="3752d-897">Bygge et Visual Studio-prosjekt</span><span class="sxs-lookup"><span data-stu-id="3752d-897">Build a Visual Studio project</span></span>

<span data-ttu-id="3752d-898">Bygg prosjektet for å gjøre et nytt menyelement tilgjengelig for brukere.</span><span class="sxs-lookup"><span data-stu-id="3752d-898">Build your project to make a new menu item available to users.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a><span data-ttu-id="3752d-899">Kjøre et format fra appen</span><span class="sxs-lookup"><span data-stu-id="3752d-899">Run a format from the application</span></span>

1. <span data-ttu-id="3752d-900">Gå til **Spørreskjema** \> **Utforming** \> **Spørreskjemarapport (drevet av ER)**.</span><span class="sxs-lookup"><span data-stu-id="3752d-900">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>

    ![Velge menyelementet Spørreskjemarapport (drevet av ER) i Spørreskjema-modulen for å kjøre det konfigurerte ER-formatet](./media/er-quick-start1-application-menu-modified.png)

2. <span data-ttu-id="3752d-902">I feltet **Formattilordning** i dialogboksen velger du **Spørreskjemarapport**.</span><span class="sxs-lookup"><span data-stu-id="3752d-902">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="3752d-903">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3752d-903">Select **OK**.</span></span>
4. <span data-ttu-id="3752d-904">I dialogboksen **Parametere for elektronisk rapport**, på hurtigfanen **Poster som skal inkluderes**, konfigurerer du filtreringsalternativet slik at bare **SBCCrsExam**-spørreskjemaet er inkludert.</span><span class="sxs-lookup"><span data-stu-id="3752d-904">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="3752d-905">Velg **OK** for å bekrefte filtreringsalternativet.</span><span class="sxs-lookup"><span data-stu-id="3752d-905">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="3752d-906">Velg **OK** for å kjøre rapporten.</span><span class="sxs-lookup"><span data-stu-id="3752d-906">Select **OK** to run the report.</span></span>

    ![Angi utvalgskriteriene i dialogboksen Elektronisk rapport](./media/er-quick-start1-report-run-dialog-page.png)

7. <span data-ttu-id="3752d-908">Gå gjennom den genererte rapporten.</span><span class="sxs-lookup"><span data-stu-id="3752d-908">Review the generated report.</span></span>

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a><span data-ttu-id="3752d-909">Justere en utviklet ER-løsning</span><span class="sxs-lookup"><span data-stu-id="3752d-909">Tune a designed ER solution</span></span>

<span data-ttu-id="3752d-910">Du kan endre den konfigurerte ER-løsningen slik at den bruker dataleverandørklassen du har utviklet, for å få tilgang til detaljer i det kjørende ER-formatet, og slik at den legger inn navnet på dette ER-formatet i en generert rapport.</span><span class="sxs-lookup"><span data-stu-id="3752d-910">You can modify the configured ER solution so that it uses the data provider class that you developed to access details of the running ER format, and so that it enters the name of this ER format in a generated report.</span></span>

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a><span data-ttu-id="3752d-911">Endre en modelltilordning</span><span class="sxs-lookup"><span data-stu-id="3752d-911">Modify a model mapping</span></span>

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a><span data-ttu-id="3752d-912">Legge til datakilder for å få tilgang til et datakontraktobjekt</span><span class="sxs-lookup"><span data-stu-id="3752d-912">Add data sources to access a data contract object</span></span>

1. <span data-ttu-id="3752d-913">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="3752d-913">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="3752d-914">På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Spørreskjemamodell** og velger **Spørreskjematilordning**.</span><span class="sxs-lookup"><span data-stu-id="3752d-914">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="3752d-915">Velg **Utforming** for å åpne siden **Tilordning av modell til datakilde**.</span><span class="sxs-lookup"><span data-stu-id="3752d-915">Select **Designer** to open the **Model to datasource mapping** page.</span></span>
4. <span data-ttu-id="3752d-916">Velg **Utforming** for å åpne den valgte tilordningen i modelltilordningsutformingen.</span><span class="sxs-lookup"><span data-stu-id="3752d-916">Select **Designer** to open the selected mapping in the model mapping designer.</span></span>
5. <span data-ttu-id="3752d-917">På siden **Modelltilordningsutforming**, i ruten **Datakildetyper**, velger du **Dynamics 365 for Operations\\Objekt**.</span><span class="sxs-lookup"><span data-stu-id="3752d-917">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Object**.</span></span>
6. <span data-ttu-id="3752d-918">I **Datakilder**-ruten velger du **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="3752d-918">In the **Data sources** pane, select **Add root**.</span></span>
7. <span data-ttu-id="3752d-919">I **Navn**-feltet i dialogboksen skriver du inn **[RunTimeParameters](#DataContractDSName)**, som definert i kildekoden til **QuestionnairesErReportService**-klassen.</span><span class="sxs-lookup"><span data-stu-id="3752d-919">In the dialog box, in the **Name** field, enter **[RunTimeParameters](#DataContractDSName)**, as defined in the source code of the **QuestionnairesErReportService** class.</span></span>
8. <span data-ttu-id="3752d-920">I **Klasse**-feltet skriver du inn **[QuestionnairesErReportContract](#DataContractClass)**, som ble kodet tidligere.</span><span class="sxs-lookup"><span data-stu-id="3752d-920">In the **Class** field, enter **[QuestionnairesErReportContract](#DataContractClass)**, which was coded earlier.</span></span>
9. <span data-ttu-id="3752d-921">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3752d-921">Select **OK**.</span></span>
10. <span data-ttu-id="3752d-922">Utvid **RunTimeParameters**.</span><span class="sxs-lookup"><span data-stu-id="3752d-922">Expand **RunTimeParameters**.</span></span>

<span data-ttu-id="3752d-923">Den tilføyde datakilden inneholder informasjon om post-ID-en for den kjørende ER-formattilordningen.</span><span class="sxs-lookup"><span data-stu-id="3752d-923">The added data source provides information about the record ID of the running ER format mapping.</span></span>

![Tilføyd datakilde i ER-modelltilordningsutformingen](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a><span data-ttu-id="3752d-925">Legge til en datakilde for å få tilgang til ER-formattilordningsposter</span><span class="sxs-lookup"><span data-stu-id="3752d-925">Add a data source to access ER format mapping records</span></span>

<span data-ttu-id="3752d-926">Fortsett med å redigere den valgte modelltilordningen ved å legge til en datakilde for å få tilgang til ER-formattilordningsposter.</span><span class="sxs-lookup"><span data-stu-id="3752d-926">Continue to edit the selected model mapping by adding a data source to access ER format mapping records.</span></span>

1. <span data-ttu-id="3752d-927">På siden **Modelltilordningsutforming**, i ruten **Datakildetyper**, velger du **Dynamics 365 for Operations\\Tabellposter**.</span><span class="sxs-lookup"><span data-stu-id="3752d-927">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="3752d-928">I **Datakilder**-ruten velger du **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="3752d-928">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="3752d-929">Skriv inn **ER1** i **Navn**-feltet i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="3752d-929">In the dialog box, in the **Name** field, enter **ER1**.</span></span>
4. <span data-ttu-id="3752d-930">I **Tabell**-feltet angir du **ERFormatMappingTable**.</span><span class="sxs-lookup"><span data-stu-id="3752d-930">In the **Table** field, enter **ERFormatMappingTable**.</span></span>
5. <span data-ttu-id="3752d-931">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3752d-931">Select **OK**.</span></span>

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a><span data-ttu-id="3752d-932">Legge til en datakilde for å få tilgang til en formattilordningspost for et kjørende ER-format</span><span class="sxs-lookup"><span data-stu-id="3752d-932">Add a data source to access a format mapping record of a running ER format</span></span>

<span data-ttu-id="3752d-933">Fortsett med å redigere den valgte modelltilordningen ved å legge til en datakilde for å få tilgang til formattilordningen for det kjørende ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="3752d-933">Continue to edit the selected model mapping by adding a data source to access the format mapping record of the running ER format.</span></span>

1. <span data-ttu-id="3752d-934">På siden **Modelltilordningsutforming**, i ruten **Datakildetyper**, velger du **Funksjoner\\Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="3752d-934">On the **Model mapping designer** page, in the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
2. <span data-ttu-id="3752d-935">I **Datakilder**-ruten velger du **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="3752d-935">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="3752d-936">Skriv inn **ER2** i **Navn**-feltet i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="3752d-936">In the dialog box, in the **Name** field, enter **ER2**.</span></span>
4. <span data-ttu-id="3752d-937">Velg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="3752d-937">Select **Edit formula**.</span></span>
5. <span data-ttu-id="3752d-938">I formelredigeringsprogrammet, i **Formel**-feltet, skriver du inn **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span><span class="sxs-lookup"><span data-stu-id="3752d-938">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span></span>
6. <span data-ttu-id="3752d-939">Velg **Lagre**, og lukk formelredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="3752d-939">Select **Save**, and close the formula editor.</span></span>
7. <span data-ttu-id="3752d-940">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3752d-940">Select **OK**.</span></span>

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a><span data-ttu-id="3752d-941">Angi navnet på det kjørende ER-formatet i datamodellen</span><span class="sxs-lookup"><span data-stu-id="3752d-941">Enter the name of the running ER format in the data model</span></span>

<span data-ttu-id="3752d-942">Fortsett med å redigere den valgte modelltilordningen, slik at navnet på det kjørende ER-formatet blir angitt i datamodellen.</span><span class="sxs-lookup"><span data-stu-id="3752d-942">Continue to edit the selected model mapping so that the name of the running ER format is entered in the data model.</span></span>

1. <span data-ttu-id="3752d-943">På siden **Modelltilordningsutforming**, i **Datamodell**-ruten, utvider du **ExecutionContext**, og deretter velger du **ExecutionContext\\FormatName**.</span><span class="sxs-lookup"><span data-stu-id="3752d-943">On the **Model mapping designer** page, in the **Data model** pane, expand **ExecutionContext**, and then select **ExecutionContext\\FormatName**.</span></span>
2. <span data-ttu-id="3752d-944">I **Datamodell**-ruten velger du **Rediger** for å konfigurere en databinding for feltet til den valgte datamodellen.</span><span class="sxs-lookup"><span data-stu-id="3752d-944">In the **Data model** pane, select **Edit** to configure a data binding for the selected data model's field.</span></span>
3. <span data-ttu-id="3752d-945">I formelredigeringsprogrammet, i **Formel**-feltet, skriver du inn **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span><span class="sxs-lookup"><span data-stu-id="3752d-945">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span></span>
4. <span data-ttu-id="3752d-946">Velg **Lagre**, og lukk formelredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="3752d-946">Select **Save**, and close the formula editor.</span></span>

<span data-ttu-id="3752d-947">Fordi du brukte **FormatName**-feltet, viser den konfigurerte modelltilordningen nå navnet på et ER-format som kaller opp denne modelltilordningen under utføring.</span><span class="sxs-lookup"><span data-stu-id="3752d-947">Because you used the **FormatName** field, the configured model mapping now exposes the name of an ER format that calls this model mapping during execution.</span></span>

![Binde datamodellfeltet til metoden for den tilføyde datakilden i ER-modelltilordningsutformingen](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a><span data-ttu-id="3752d-949">Fullføre utformingen av modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="3752d-949">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="3752d-950">Velg **Lagre** på siden **Modelltilordningsutforming**.</span><span class="sxs-lookup"><span data-stu-id="3752d-950">On the **Model mapping designer** page, select **Save**.</span></span>
2. <span data-ttu-id="3752d-951">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3752d-951">Close the page.</span></span>
3. <span data-ttu-id="3752d-952">Lukk siden Modelltilordninger.</span><span class="sxs-lookup"><span data-stu-id="3752d-952">Close the model mappings page.</span></span>
4. <span data-ttu-id="3752d-953">I konfigurasjonstreet på **Konfigurasjoner**-siden kontrollerer du at konfigurasjonen **Spørreskjematilordning** fortsatt er valgt.</span><span class="sxs-lookup"><span data-stu-id="3752d-953">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire mapping** configuration is still selected.</span></span> <span data-ttu-id="3752d-954">På hurtigfanen **Versjoner** velger du deretter konfigurasjonsversjonen med statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="3752d-954">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
5. <span data-ttu-id="3752d-955">Velg **Endre status** \> **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="3752d-955">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="3752d-956">Statusen til versjon 1.2 av denne konfigurasjonen endres fra **Utkast** til **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="3752d-956">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="3752d-957">Versjon 1.2 kan ikke lenger endres.</span><span class="sxs-lookup"><span data-stu-id="3752d-957">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="3752d-958">Denne versjonen inneholder den konfigurerte modelltilordningen og kan brukes som basis for andre ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="3752d-958">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="3752d-959">Versjon 1.3 av denne konfigurasjonen opprettes og har statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="3752d-959">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="3752d-960">Du kan redigere denne versjonen for å justere **Spørreskjema**-modelltilordningen.</span><span class="sxs-lookup"><span data-stu-id="3752d-960">You can edit this version to adjust the **Questionnaire** model mapping.</span></span>

### <a name="modify-a-format"></a><a name="ModifyFormat"></a><span data-ttu-id="3752d-961">Endre et format</span><span class="sxs-lookup"><span data-stu-id="3752d-961">Modify a format</span></span>

<span data-ttu-id="3752d-962">Du kan endre det konfigurerte ER-formatet slik at navnet vises i bunnteksten til en rapport som genereres når ER-formatet kjøres.</span><span class="sxs-lookup"><span data-stu-id="3752d-962">You can modify the configured ER format so that its name is shown in the footer of a report that is generated when the ER format is run.</span></span>

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a><span data-ttu-id="3752d-963">Legge til et nytt formatelement</span><span class="sxs-lookup"><span data-stu-id="3752d-963">Add a new format element</span></span>

1. <span data-ttu-id="3752d-964">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="3752d-964">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="3752d-965">På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Spørreskjemamodell** og velger **Spørreskjemarapport**.</span><span class="sxs-lookup"><span data-stu-id="3752d-965">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="3752d-966">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="3752d-966">Select **Designer**.</span></span>
4. <span data-ttu-id="3752d-967">På siden **Formatutforming** velger du rotelementet **Rapport**.</span><span class="sxs-lookup"><span data-stu-id="3752d-967">On the **Format designer** page, select the **Report** root item.</span></span>
5. <span data-ttu-id="3752d-968">Velg **Legg til** for å legge til et nytt nestet formatelement for det valgte **Rapport**-rotelementet.</span><span class="sxs-lookup"><span data-stu-id="3752d-968">Select **Add** to add a new nested format element for the selected **Report** root item.</span></span>
6. <span data-ttu-id="3752d-969">Velg **Excel\\Bunntekst**.</span><span class="sxs-lookup"><span data-stu-id="3752d-969">Select **Excel\\Footer**.</span></span>
7. <span data-ttu-id="3752d-970">Angi **Bunntekst** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3752d-970">In the **Name** field, enter **Footer**.</span></span>
8. <span data-ttu-id="3752d-971">Velg **Rapport\Bunntekst**, og velg deretter **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="3752d-971">Select **Report\Footer**, and then select **Add**.</span></span>
9. <span data-ttu-id="3752d-972">Velg **Tekst\\Streng**.</span><span class="sxs-lookup"><span data-stu-id="3752d-972">Select **Text\\String**.</span></span>

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a><span data-ttu-id="3752d-973">Binde formatelementet som er lagt til</span><span class="sxs-lookup"><span data-stu-id="3752d-973">Bind the added format element</span></span>

1. <span data-ttu-id="3752d-974">På **Formatutforming**-siden på **Tilordning**-fanen i formattreet for det aktive **Bunntekst\\Streng**-elementet velger du **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="3752d-974">On the **Format designer** page, on the **Mapping** tab, in the format tree, for the active **Footer\\String** element, select **Edit formula**.</span></span>
2. <span data-ttu-id="3752d-975">I formelredigeringsprogrammet, i **Formel**-feltet, skriver du inn **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span><span class="sxs-lookup"><span data-stu-id="3752d-975">In the formula editor, in the **Formula** field, enter **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span></span>
3. <span data-ttu-id="3752d-976">Velg **Lagre**, og lukk formelredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="3752d-976">Select **Save**, and close the formula editor.</span></span>
4. <span data-ttu-id="3752d-977">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3752d-977">Select **Save**.</span></span>

<span data-ttu-id="3752d-978">Det konfigurerte formatet er nå endret slik at navnet blir angitt i bunnteksten for en generert rapport ved hjelp av **Bunntekst\\Streng**-elementet.</span><span class="sxs-lookup"><span data-stu-id="3752d-978">The configured format has now been modified so that its name will be entered in the footer of a generated report by using the **Footer\\String** element.</span></span>

![Legge til Bunntekst-formatelementet i det konfigurerte formatet i ER-operasjonsutformingen](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a><span data-ttu-id="3752d-980">Fullføre formatutformingen</span><span class="sxs-lookup"><span data-stu-id="3752d-980">Complete the format design</span></span>

1. <span data-ttu-id="3752d-981">Lukk **Formatutforming**-siden.</span><span class="sxs-lookup"><span data-stu-id="3752d-981">Close the **Format designer** page.</span></span>
2. <span data-ttu-id="3752d-982">I konfigurasjonstreet på **Konfigurasjoner**-siden kontrollerer du at konfigurasjonen **Spørreskjemarapport** fortsatt er valgt.</span><span class="sxs-lookup"><span data-stu-id="3752d-982">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire report** configuration is still selected.</span></span> <span data-ttu-id="3752d-983">På hurtigfanen **Versjoner** velger du deretter konfigurasjonsversjonen med statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="3752d-983">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
3. <span data-ttu-id="3752d-984">Velg **Endre status** \> **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="3752d-984">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="3752d-985">Statusen til versjon 1.2 av denne konfigurasjonen endres fra **Utkast** til **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="3752d-985">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="3752d-986">Versjon 1.2 kan ikke lenger endres.</span><span class="sxs-lookup"><span data-stu-id="3752d-986">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="3752d-987">Denne versjonen inneholder det konfigurerte formatet og kan brukes som basis for andre ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="3752d-987">This version contains the configured format and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="3752d-988">Versjon 1.3 av denne konfigurasjonen opprettes og har statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="3752d-988">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="3752d-989">Du kan redigere denne versjonen for å justere **Spørreskjema**-rapporten.</span><span class="sxs-lookup"><span data-stu-id="3752d-989">You can edit this version to adjust the **Questionnaire** report.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a><span data-ttu-id="3752d-990">Kjøre et format fra appen</span><span class="sxs-lookup"><span data-stu-id="3752d-990">Run a format from the application</span></span>

1. <span data-ttu-id="3752d-991">Gå til **Spørreskjema** \> **Utforming** \> **Spørreskjemarapport (drevet av ER)**.</span><span class="sxs-lookup"><span data-stu-id="3752d-991">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="3752d-992">I feltet **Formattilordning** i dialogboksen velger du **Spørreskjemarapport**.</span><span class="sxs-lookup"><span data-stu-id="3752d-992">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="3752d-993">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3752d-993">Select **OK**.</span></span>
4. <span data-ttu-id="3752d-994">I dialogboksen **ER-parametere**, på hurtigfanen **Poster som skal inkluderes**, konfigurerer du filtreringsalternativet slik at bare **SBCCrsExam**-spørreskjemaet er inkludert.</span><span class="sxs-lookup"><span data-stu-id="3752d-994">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="3752d-995">Velg **OK** for å bekrefte filtreringsalternativet.</span><span class="sxs-lookup"><span data-stu-id="3752d-995">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="3752d-996">Velg **OK** for å kjøre rapporten.</span><span class="sxs-lookup"><span data-stu-id="3752d-996">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="3752d-997">Se gjennom den genererte rapporten i Excel-format.</span><span class="sxs-lookup"><span data-stu-id="3752d-997">Review the generated report in Excel format.</span></span>

<span data-ttu-id="3752d-998">Legg merke til at bunnteksten i den genererte rapporten inneholder navnet på ER-formatet som ble brukt til å generere den.</span><span class="sxs-lookup"><span data-stu-id="3752d-998">Notice that the footer of the generated report contains the name of the ER format that was used to generate it.</span></span>

![Generert rapport i Excel-format](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a><span data-ttu-id="3752d-1000">Kjøre et format fra ER</span><span class="sxs-lookup"><span data-stu-id="3752d-1000">Run a format from ER</span></span>

1. <span data-ttu-id="3752d-1001">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="3752d-1001">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="3752d-1002">På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Spørreskjemamodell** og velger **Spørreskjemarapport**.</span><span class="sxs-lookup"><span data-stu-id="3752d-1002">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="3752d-1003">Velg **Kjør** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3752d-1003">On the Action Pane, select **Run**.</span></span>
4. <span data-ttu-id="3752d-1004">I dialogboksen **Parametere for elektronisk rapport**, på hurtigfanen **Poster som skal inkluderes**, konfigurerer du filtreringsalternativet slik at bare **SBCCrsExam**-spørreskjemaet er inkludert.</span><span class="sxs-lookup"><span data-stu-id="3752d-1004">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="3752d-1005">Velg **OK** for å bekrefte filtreringsalternativet.</span><span class="sxs-lookup"><span data-stu-id="3752d-1005">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="3752d-1006">Velg **OK** for å kjøre rapporten.</span><span class="sxs-lookup"><span data-stu-id="3752d-1006">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="3752d-1007">Se gjennom den genererte rapporten i Excel-format.</span><span class="sxs-lookup"><span data-stu-id="3752d-1007">Review the generated report in Excel format.</span></span>

<span data-ttu-id="3752d-1008">Legg merke til at bunnteksten i den genererte rapporten ikke inneholder navnet på ER-formatet som ble brukt til å generere den, fordi datakontraktobjektet ikke ble sendt til den kjørende modelltilordningen da den ble kalt med formatet som ble kjørt fra ER.</span><span class="sxs-lookup"><span data-stu-id="3752d-1008">Notice that the footer of the generated report doesn't contain the name of ER format that was used to generate it, because the data contract object wasn't passed to the running model mapping when it was called by the ER format that was run from ER.</span></span>

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a><span data-ttu-id="3752d-1009">Konfigurere et formatmål for forhåndsvisning på skjermen</span><span class="sxs-lookup"><span data-stu-id="3752d-1009">Configure a format destination for on-screen preview</span></span>

1. <span data-ttu-id="3752d-1010">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Mål for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="3752d-1010">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting destination**.</span></span>
2. <span data-ttu-id="3752d-1011">På siden **Mål for elektronisk rapportering** legger du til en målpost for det konfigurerte ER-formatet **Spørreskjema**.</span><span class="sxs-lookup"><span data-stu-id="3752d-1011">On the **Electronic reporting destination** page, add a destination record for the configured **Questionnaire report** ER format.</span></span>
3. <span data-ttu-id="3752d-1012">På hurtigfanen **Filmål** konfigurerer du **Skjerm**-[målet](er-destination-type-screen.md) for **Rapport**-formatkomponenten som er [lagt til](#AddFormatRootElement) som rotelement for det konfigurerte ER-formatet **Spørreskjemarapport**.</span><span class="sxs-lookup"><span data-stu-id="3752d-1012">On the **File destination** FastTab, set up the **Screen** [destination](er-destination-type-screen.md) for the **Report** format component that has been [added](#AddFormatRootElement) as the root element of the configured **Questionnaire report** ER format.</span></span>
4. <span data-ttu-id="3752d-1013">På hurtigfanen **PDF-konverteringsinnstillinger** konfigurerer du målet for å konvertere en rapport til [PDF-format](electronic-reporting-destinations.md#OutputConversionToPDF) som bruker sideretningen **Liggende**.</span><span class="sxs-lookup"><span data-stu-id="3752d-1013">On the **PDF conversion settings** FastTab, configure the destination to convert a report to [PDF format](electronic-reporting-destinations.md#OutputConversionToPDF) that uses the **Landscape** page orientation.</span></span>

![Konfigurere det egendefinerte Skjerm-målet for ER-formatet på målsiden for elektronisk rapportering](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a><span data-ttu-id="3752d-1015">Kjøre et format fra appen for å forhåndsvise det som et PDF-dokument</span><span class="sxs-lookup"><span data-stu-id="3752d-1015">Run a format from the application to preview it as a PDF document</span></span>

1. <span data-ttu-id="3752d-1016">Gå til **Spørreskjema** \> **Utforming** \> **Spørreskjemarapport (drevet av ER)**.</span><span class="sxs-lookup"><span data-stu-id="3752d-1016">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="3752d-1017">I feltet **Formattilordning** i dialogboksen velger du **Spørreskjemarapport**.</span><span class="sxs-lookup"><span data-stu-id="3752d-1017">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="3752d-1018">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3752d-1018">Select **OK**.</span></span>
4. <span data-ttu-id="3752d-1019">I dialogboksen **Parametere for elektronisk rapport**, på hurtigfanen **Poster som skal inkluderes**, konfigurerer du filtreringsalternativet slik at bare **SBCCrsExam**-spørreskjemaet er inkludert.</span><span class="sxs-lookup"><span data-stu-id="3752d-1019">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="3752d-1020">Velg **OK** for å bekrefte filtreringsalternativet.</span><span class="sxs-lookup"><span data-stu-id="3752d-1020">Select **OK** to confirm the filtering option.</span></span>

    <span data-ttu-id="3752d-1021">På hurtigfanen **Mål** kan du merke deg at **Utdata**-feltet er angitt til **Skjerm**.</span><span class="sxs-lookup"><span data-stu-id="3752d-1021">On the **Destinations** FastTab, notice that the **Output** field is set to **Screen**.</span></span> <span data-ttu-id="3752d-1022">Hvis du vil endre det konfigurerte målet, velger du **Endre**.</span><span class="sxs-lookup"><span data-stu-id="3752d-1022">If you want to change the configured destination, select **Change**.</span></span>

    ![Dialogboksen for ER-rapportkjøretid, der du kan endre det konfigurerte målet](./media/er-quick-start1-run-settings.png)

6. <span data-ttu-id="3752d-1024">Velg **OK** for å kjøre rapporten.</span><span class="sxs-lookup"><span data-stu-id="3752d-1024">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="3752d-1025">Se gjennom den genererte rapporten i PDF-format.</span><span class="sxs-lookup"><span data-stu-id="3752d-1025">Review the generated report in PDF format.</span></span>

    ![Forhåndsvisning på skjermen av den genererte rapporten i PDF-format](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a><span data-ttu-id="3752d-1027">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="3752d-1027">Additional resources</span></span>

- [<span data-ttu-id="3752d-1028">Oversikt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="3752d-1028">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="3752d-1029">Formelspråk i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="3752d-1029">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="3752d-1030">Utforme flerspråklige rapporter</span><span class="sxs-lookup"><span data-stu-id="3752d-1030">Design multilingual reports</span></span>](er-design-multilingual-reports.md)
- [<span data-ttu-id="3752d-1031">API for ER-rammeverk</span><span class="sxs-lookup"><span data-stu-id="3752d-1031">ER framework API</span></span>](er-apis-app73.md)
- [<span data-ttu-id="3752d-1032">CASE-funksjonen</span><span class="sxs-lookup"><span data-stu-id="3752d-1032">CASE function</span></span>](er-functions-logical-case.md)
- [<span data-ttu-id="3752d-1033">CONCATENATE-funksjonen</span><span class="sxs-lookup"><span data-stu-id="3752d-1033">CONCATENATE function</span></span>](er-functions-text-concatenate.md)
- [<span data-ttu-id="3752d-1034">DATETIMEFORMAT-funksjonen</span><span class="sxs-lookup"><span data-stu-id="3752d-1034">DATETIMEFORMAT function</span></span>](er-functions-datetime-datetimeformat.md)
- [<span data-ttu-id="3752d-1035">FILTER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="3752d-1035">FILTER function</span></span>](er-functions-list-filter.md)
- [<span data-ttu-id="3752d-1036">FIRSTORNULL-funksjonen</span><span class="sxs-lookup"><span data-stu-id="3752d-1036">FIRSTORNULL function</span></span>](er-functions-list-firstornull.md)
- [<span data-ttu-id="3752d-1037">FORMAT-funksjonen</span><span class="sxs-lookup"><span data-stu-id="3752d-1037">FORMAT function</span></span>](er-functions-text-format.md)
- [<span data-ttu-id="3752d-1038">IF-funksjonen</span><span class="sxs-lookup"><span data-stu-id="3752d-1038">IF function</span></span>](er-functions-logical-if.md)
- [<span data-ttu-id="3752d-1039">ORDERBY-funksjonen</span><span class="sxs-lookup"><span data-stu-id="3752d-1039">ORDERBY function</span></span>](er-functions-list-orderby.md)
- [<span data-ttu-id="3752d-1040">SESSIONNOW-funksjonen</span><span class="sxs-lookup"><span data-stu-id="3752d-1040">SESSIONNOW function</span></span>](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
