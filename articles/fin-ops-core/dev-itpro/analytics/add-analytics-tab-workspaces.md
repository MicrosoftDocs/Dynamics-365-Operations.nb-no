---
title: Legge til analyse i arbeidsområder ved hjelp av Power BI Embedded
description: Dette emnet forklarer hvordan du bygger inn en Power BI-rapport i kategorien Analyse i et arbeidsområde.
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 442557a01b25e13b76074c865dfe5468bbc9fde0
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259638"
---
# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a><span data-ttu-id="5b5dd-103">Legge til analyse i arbeidsområder ved hjelp av Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="5b5dd-103">Add analytics to workspaces by using Power BI Embedded</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="5b5dd-104">Denne funksjonen støttes i Finance and Operations (versjon 7.2 og senere).</span><span class="sxs-lookup"><span data-stu-id="5b5dd-104">This feature is supported in Finance and Operations (version 7.2 and later).</span></span>

## <a name="introduction"></a><span data-ttu-id="5b5dd-105">Innledning</span><span class="sxs-lookup"><span data-stu-id="5b5dd-105">Introduction</span></span>
<span data-ttu-id="5b5dd-106">Dette emnet forklarer hvordan du bygger inn en Microsoft Power BI-rapport i kategorien **Analyse** i et arbeidsområde.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-106">This topic shows how to embed a Microsoft Power BI report on the **Analytics** tab of a workspace.</span></span> <span data-ttu-id="5b5dd-107">For eksempelet som er angitt her, vil vi utvide arbeidsområdet **Reservasjonsbehandling** i programmet Fleet Management til å bygge inn et analytisk arbeidsområde på en **Analyse**-kategori.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-107">For the example that is given here, we will extend the **Reservation management** workspace in the Fleet Management application to embed an analytical workspace on an **Analytics** tab.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5b5dd-108">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="5b5dd-108">Prerequisites</span></span>
+ <span data-ttu-id="5b5dd-109">Tilgang til et utviklermiljø som kjører plattformoppdatering 8 eller senere.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-109">Access to a developer environment that runs Platform update 8 or later.</span></span>
+ <span data-ttu-id="5b5dd-110">En analytisk rapport (.pbix-fil) som ble opprettet ved hjelp av Microsoft Power BI Desktop, og som har en datamodell som har Enhetslager-databasen som kilde.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-110">An analytical report (.pbix file) that was created by using Microsoft Power BI Desktop, and that has a data model that is sourced from the Entity store database.</span></span>

## <a name="overview"></a><span data-ttu-id="5b5dd-111">Oversikt</span><span class="sxs-lookup"><span data-stu-id="5b5dd-111">Overview</span></span>
<span data-ttu-id="5b5dd-112">Enten du utvider et eksisterende arbeidsområde for programmet eller introdusere et nytt arbeidsområde på egen hånd, kan du bruke innebygde analytiske visninger for å levere innsiktsfulle og interaktive visninger av forretningsdataene.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-112">Whether you extend an existing application workspace or introduce a new workspace of your own, you can use embedded analytical views to deliver insightful and interactive views of your business data.</span></span> <span data-ttu-id="5b5dd-113">Prosessen for å legge til en analytisk arbeidsområdet kategori har fire trinn.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-113">The process for adding an analytical workspace tab has four steps.</span></span>

1. <span data-ttu-id="5b5dd-114">Legge til en .pbix-fil som en ressurs for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-114">Add a .pbix file as a Dynamics 365 resource.</span></span>
2. <span data-ttu-id="5b5dd-115">Definer en analytisk arbeidsområdet-kategorien.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-115">Define an analytical workspace tab.</span></span>
3. <span data-ttu-id="5b5dd-116">Bygge inn ressursen .pbix i kategorien arbeidsområde.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-116">Embed the .pbix resource on the workspace tab.</span></span>
4. <span data-ttu-id="5b5dd-117">Valgfritt: Legg til filtyper hvis du vil tilpasse visningen.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-117">Optional: Add extensions to customize the view.</span></span>

> [!NOTE]
> <span data-ttu-id="5b5dd-118">Hvis du vil ha mer informasjon om hvordan du oppretter analyserapporter, se [Komme i gang med Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="5b5dd-118">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span></span> <span data-ttu-id="5b5dd-119">Denne siden er en god kilde for innsikt som kan hjelpe deg med å opprette overbevisende analytiske rapporteringsløsninger.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-119">This page is a great source for insights that can help you create compelling analytical reporting solutions.</span></span>

## <a name="add-a-pbix-file-as-a-resource"></a><span data-ttu-id="5b5dd-120">Legge til en .pbix-fil som en ressurs</span><span class="sxs-lookup"><span data-stu-id="5b5dd-120">Add a .pbix file as a resource</span></span>
<span data-ttu-id="5b5dd-121">Før du begynner, må du opprette eller få tak i Power BI-rapporten som du vil bygge inn i arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-121">Before you begin, you must create or obtain the Power BI report that you will embed in the workspace.</span></span> <span data-ttu-id="5b5dd-122">Hvis du vil ha mer informasjon om hvordan du oppretter analyserapporter, se [Komme i gang med Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="5b5dd-122">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span></span>

<span data-ttu-id="5b5dd-123">Følg denne fremgangsmåten for å legge til en .pbix-fil som en artefakt i et Visual Studio-prosjekt.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-123">Follow these steps to add a .pbix file as a Visual Studio project artifact.</span></span>

1. <span data-ttu-id="5b5dd-124">Opprett et nytt prosjekt i den aktuelle modellen.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-124">Create a new project in the appropriate model.</span></span>
2. <span data-ttu-id="5b5dd-125">Velg prosjektet i Solution Explorer, høyreklikk, og velg deretter **Legg til** \> **Nytt element**.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-125">In Solution Explorer, select the project, right-click, and then select **Add** \> **New Item**.</span></span>
3. <span data-ttu-id="5b5dd-126">I dialogboksen **Legg til nytt element** under **Operations-artefakter** velger du **Ressurs**-malen.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-126">In the **Add New Item** dialog box, under **Operations Artifacts**, select the **Resource** template.</span></span>
4. <span data-ttu-id="5b5dd-127">Angi et navn som skal brukes til å referere til rapporten i X++-metadataene, og klikk deretter **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-127">Enter a name that will be used to reference the report in X++ metadata, and then click **Add**.</span></span>

    ![Dialogboksen Legg til nytt element](media/analytical-workspace-add.png)

5. <span data-ttu-id="5b5dd-129">Finn .pbix-filen som inneholder definisjonen av den analytiske rapporten, og klikk deretter **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-129">Find the .pbix file that contains the definition of the analytical report, and then click **Open**.</span></span>

    ![Velge en Ressursfil-dialogboks](media/analytical-workspace-select-resource.png)

<span data-ttu-id="5b5dd-131">Nå som du har lagt til .pbix-filen som en Dynamics 365-ressurs, kan du bygge inn rapportene i arbeidsområder og legge til direkte koblinger ved å bruke menyelementer.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-131">Now that you've added the .pbix file as a Dynamics 365 resource, you can embed the reports in workspaces and add direct links by using menu items.</span></span>

## <a name="add-a-tab-control-to-an-application-workspace"></a><span data-ttu-id="5b5dd-132">Legge til en kategorikontroll i et arbeidsområde for program</span><span class="sxs-lookup"><span data-stu-id="5b5dd-132">Add a tab control to an application workspace</span></span>
<span data-ttu-id="5b5dd-133">I dette eksemplet vil vi utvide arbeidsområdet **Reservasjonsbehandling** i Fleet Management-modellen ved å legge til **Analyse**-kategorien med definisjonen av **FMClerkWorkspace**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-133">In this example, we will extend the **Reservation management** workspace in the Fleet Management model by adding the **Analytics** tab to the definition of the **FMClerkWorkspace** form.</span></span>

<span data-ttu-id="5b5dd-134">Illustrasjonen nedenfor viser hvordan **FMClerkWorkspace**-skjemaet ser ut i utformingen i Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-134">The following illustration shows what the **FMClerkWorkspace** form looks like in the designer in Microsoft Visual Studio.</span></span>

![FMClerkWorkspace-skjemaet før endringer](media/analytical-workspace-definition-before.png)

<span data-ttu-id="5b5dd-136">Følg denne fremgangsmåten for å utvide skjemadefinisjonen for den **Reservasjonsbehandling**-arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-136">Follow these steps to extend the form definition for the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="5b5dd-137">Åpne skjemautformingen for å utvide definisjonen av utformingen.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-137">Open the form designer to extend the design definition.</span></span>
2. <span data-ttu-id="5b5dd-138">I designdefinisjonen velger du det øverste elementet som heter **Design | Pattern: Workspace Operational**.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-138">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
3. <span data-ttu-id="5b5dd-139">Høyreklikk, og velg deretter **Ny** \> **Kategori** for å legge til en ny kontroll som heter **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-139">Right-click, and then select **New** \> **Tab** to add a new control that is named **FormTabControl1**.</span></span>
4. <span data-ttu-id="5b5dd-140">Velg **FormTabControl1** i skjemautformingen.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-140">In the form designer, select **FormTabControl1**.</span></span>
5. <span data-ttu-id="5b5dd-141">Høyreklikk, og velg deretter **Ny kategoriside** for å legge til en ny kategoriside.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-141">Right-click, and then select **New Tab Page** to add a new tab page.</span></span>
6. <span data-ttu-id="5b5dd-142">Endre navnet på kategorisiden til noe som gir mening, som **Arbeidsområde**.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-142">Rename the tab page to something meaningful, such as **Workspace**.</span></span>
7. <span data-ttu-id="5b5dd-143">Velg **FormTabControl1** i skjemautformingen.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-143">In the form designer, select **FormTabControl1**.</span></span>
8. <span data-ttu-id="5b5dd-144">Høyreklikk, og velg deretter **Ny kategoriside**.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-144">Right-click, and then select **New Tab Page**.</span></span>
9. <span data-ttu-id="5b5dd-145">Endre navnet på kategorisiden til noe som gir mening, som **Analyse**.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-145">Rename the tab page to something meaningful, such as **Analytics**.</span></span>
10. <span data-ttu-id="5b5dd-146">I skjemautformingen velger du **Analyse (kategoriside)**.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-146">In the form designer, select **Analytics (Tab Page)**.</span></span>
11. <span data-ttu-id="5b5dd-147">Sett egenskapen **Overskrift** til **Analyse**, og sett egenskapen **Automatisk erklæring** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-147">Set the **Caption** property to **Analytics**, and set the **Auto Declaration** property to **Yes**.</span></span>
12. <span data-ttu-id="5b5dd-148">Høyreklikk kontrollen, og velg deretter **Ny** \> **Gruppe** for å legge til en ny skjemagruppekontroll.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-148">Right-click the control, and then select **New** \> **Group** to add a new form group control.</span></span>
13. <span data-ttu-id="5b5dd-149">Endre navnet på skjemagruppen til noe som gir mening, som **powerBIReportGroup**.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-149">Rename the form group to something meaningful, such as **powerBIReportGroup**.</span></span>
14. <span data-ttu-id="5b5dd-150">I skjemautformingen velger du **PanoramaBody (kategori)**, og dra deretter kontrollen til **Arbeidsområde**-kategorien.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-150">In the form designer, select **PanoramaBody (Tab)**, and then drag the control onto the **Workspace** tab.</span></span>
15. <span data-ttu-id="5b5dd-151">I designdefinisjonen velger du det øverste elementet som heter **Design | Pattern: Workspace Operational**.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-151">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
16. <span data-ttu-id="5b5dd-152">Høyreklikk, og velg deretter **Fjern mønster**.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-152">Right-click, and then select **Remove pattern**.</span></span>
17. <span data-ttu-id="5b5dd-153">Høyreklikk på nytt, og velg deretter **Legg til mønster** \> **Arbeidsområde med kategorier**.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-153">Right-click again, and then select **Add pattern** \> **Workspace Tabbed**.</span></span>
18. <span data-ttu-id="5b5dd-154">Utfør et bygg for å bekrefte endringene.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-154">Perform a build to verify your changes.</span></span>

<span data-ttu-id="5b5dd-155">Illustrasjonen nedenfor viser hvordan utformingen ser ut etter at endringene er brukt.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-155">The following illustration shows what the design looks like after these changes are applied.</span></span>

![FMClerkWorkspace etter endringer](media/analytical-workspace-definition-after.png)

<span data-ttu-id="5b5dd-157">Nå som du har lagt til skjemakontrollene som skal brukes til å bygge inn arbeidsområderapporten, må du definere størrelsen på den overordnede kontrollen, slik at den passer for oppsettet.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-157">Now that you've added the form controls that will be used to embed the workspace report, you must define the size of the parent control so that it accommodates the layout.</span></span> <span data-ttu-id="5b5dd-158">Som standard er både **filterrutesiden** og **kategorisiden** synlig i rapporten.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-158">By default, both the **Filters Pane** page and the **Tab** page will be visible on the report.</span></span> <span data-ttu-id="5b5dd-159">Du kan imidlertid endre synligheten for disse kontrollene etter behov for rapportens målbruker.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-159">However, you can change the visibility of these controls as appropriate for the target consumer of the report.</span></span>

> [!NOTE]
> <span data-ttu-id="5b5dd-160">For innebygde arbeidsområder anbefaler vi at du bruker tilleggene for å skjule både **filtreringsruten** og **kategorisidene**, for konsekvens.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-160">For embedded workspaces, we recommend that you use extensions to hide both the **Filters Pane** and **Tab** pages, for consistency.</span></span>

<span data-ttu-id="5b5dd-161">Du har nå fullført oppgaven for å utvide programskjemadefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-161">You've now completed the task of extending the application form definition.</span></span> <span data-ttu-id="5b5dd-162">Hvis du vil ha mer informasjon om hvordan du bruker tillegg til å gjøre tilpasninger, se [Tilpasse via utvidelse og overlag](../extensibility/customization-overlayering-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="5b5dd-162">For more information about how to use extensions to do customizations, see [Customize through extension and overlayering](../extensibility/customization-overlayering-extensions.md).</span></span>

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a><span data-ttu-id="5b5dd-163">Legge til X ++-forretningslogikk for å bygge inn en visningskontroll</span><span class="sxs-lookup"><span data-stu-id="5b5dd-163">Add X++ business logic to embed a viewer control</span></span>
<span data-ttu-id="5b5dd-164">Gjør følgende for å legge til forretningslogikk som initialiserer rapportvisningskontrollen som er innebygd i arbeidsområdet **Reservasjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-164">Follow these steps to add business logic that initializes the report viewer control that is embedded in the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="5b5dd-165">Åpne **FMClerkWorkspace**-skjemautformingen for å utvide definisjonen av utformingen.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-165">Open the **FMClerkWorkspace** form designer to extend the design definition.</span></span>
2. <span data-ttu-id="5b5dd-166">Trykk F7 for å få tilgang til koden bak kodedefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-166">Press F7 to access the code behind the code definition.</span></span>
3. <span data-ttu-id="5b5dd-167">Legg til følgende X++-kode</span><span class="sxs-lookup"><span data-stu-id="5b5dd-167">Add the following X++ code.</span></span>

    ```xpp
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                // initialize the PBI report control using shared helper
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
        }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. <span data-ttu-id="5b5dd-168">Utfør et bygg for å bekrefte endringene.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-168">Perform a build to verify your changes.</span></span>

<span data-ttu-id="5b5dd-169">Du har nå fullført oppgaven med å legge til forretningslogikk for å initialisere den innebygde rapportvisningskontrollen.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-169">You've now completed the task of adding business logic to initialize the embedded report viewer control.</span></span> <span data-ttu-id="5b5dd-170">Illustrasjonen nedenfor viser hvordan arbeidsområdet ser ut etter at endringene er brukt.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-170">The following illustration shows what the workspace looks like after these changes are applied.</span></span>

![Rapport som er innebygd i arbeidsområdet](media/analytical-workspace-final.png)

> [!NOTE]
> <span data-ttu-id="5b5dd-172">Du kan få tilgang til den eksisterende operasjonelle visningen ved hjelp av arbeidsområde-kategoriene under sidetittelen.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-172">You can access the existing operational view by using the workspace tabs below the page title.</span></span>

## <a name="reference"></a><span data-ttu-id="5b5dd-173">Referanse</span><span class="sxs-lookup"><span data-stu-id="5b5dd-173">Reference</span></span>

### <a name="pbireporthelperinitializereportcontrol-method"></a><span data-ttu-id="5b5dd-174">PBIReportHelper.initializeReportControl-metoden</span><span class="sxs-lookup"><span data-stu-id="5b5dd-174">PBIReportHelper.initializeReportControl method</span></span>
<span data-ttu-id="5b5dd-175">Denne delen gir informasjon om hjelpeklassen som brukes til å bygge inn en Power BI-rapport (.pbix-ressurs) i en skjemagruppekontroll.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-175">This section provides information about the helper class that is used to embed a Power BI report (.pbix resource) in a form group control.</span></span>

#### <a name="syntax"></a><span data-ttu-id="5b5dd-176">Syntaks</span><span class="sxs-lookup"><span data-stu-id="5b5dd-176">Syntax</span></span>
```xpp
public static void initializeReportControl(
    str                 _resourceName,
    FormGroupControl    _formGroupControl,
    str                 _defaultPageName = '',
    boolean             _showFilterPane = false,
    boolean             _showNavPane = false,
    List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a><span data-ttu-id="5b5dd-177">Parametere</span><span class="sxs-lookup"><span data-stu-id="5b5dd-177">Parameters</span></span>

| <span data-ttu-id="5b5dd-178">Navn</span><span class="sxs-lookup"><span data-stu-id="5b5dd-178">Name</span></span>             | <span data-ttu-id="5b5dd-179">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5b5dd-179">Description</span></span>                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5dd-180">resourceName</span><span class="sxs-lookup"><span data-stu-id="5b5dd-180">resourceName</span></span>     | <span data-ttu-id="5b5dd-181">Navnet på .pbix-ressursen.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-181">The name of the .pbix resource.</span></span>                                                                              |
| <span data-ttu-id="5b5dd-182">formGroupControl</span><span class="sxs-lookup"><span data-stu-id="5b5dd-182">formGroupControl</span></span> | <span data-ttu-id="5b5dd-183">Skjemagruppekontrollen der Power BI-rapporten skal brukes.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-183">The form group control to apply the Power BI report control to.</span></span>                                              |
| <span data-ttu-id="5b5dd-184">defaultPageName</span><span class="sxs-lookup"><span data-stu-id="5b5dd-184">defaultPageName</span></span>  | <span data-ttu-id="5b5dd-185">Standard sidenavn.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-185">The default page name.</span></span>                                                                                       |
| <span data-ttu-id="5b5dd-186">showFilterPane</span><span class="sxs-lookup"><span data-stu-id="5b5dd-186">showFilterPane</span></span>   | <span data-ttu-id="5b5dd-187">En boolsk verdi som angir om filtreringsruten skal vises (**true**) eller skjules (**false**).</span><span class="sxs-lookup"><span data-stu-id="5b5dd-187">A Boolean value that indicates whether the filter pane should be shown (**true**) or hidden (**false**).</span></span>     |
| <span data-ttu-id="5b5dd-188">showNavPane</span><span class="sxs-lookup"><span data-stu-id="5b5dd-188">showNavPane</span></span>      | <span data-ttu-id="5b5dd-189">En boolsk verdi som angir om navigasjonsruten skal vises (**true**) eller skjules (**false**).</span><span class="sxs-lookup"><span data-stu-id="5b5dd-189">A Boolean value that indicates whether the navigation pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="5b5dd-190">defaultFilters</span><span class="sxs-lookup"><span data-stu-id="5b5dd-190">defaultFilters</span></span>   | <span data-ttu-id="5b5dd-191">Standardfiltrene for Power BI-rapporten.</span><span class="sxs-lookup"><span data-stu-id="5b5dd-191">The default filters for the Power BI report.</span></span>                                                                 |
