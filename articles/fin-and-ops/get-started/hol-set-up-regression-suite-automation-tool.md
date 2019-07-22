---
title: Opplæring i installasjon og konfigurasjon av Regression Suite Automation Tool
description: Dette emnet er en opplæring i hvordan du konfigurerer og installerer RSAT (Regression Suite Automation Tool).
author: kfend
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: ab81e95c2e31adfefd4e5c4367a61baa7c251c43
ms.sourcegitcommit: f6581bab16225a027f4fbfad25fdef45bd286489
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/27/2019
ms.locfileid: "1703835"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="6ed03-103">Opplæring i installasjon og konfigurasjon av Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="6ed03-103">Set up and install Regression suite automation tool tutorial</span></span>
<span data-ttu-id="6ed03-104">Dette emnet hjelper deg å konfigurere og komme i gang med RSAT og verktøyene som er knyttet til bruk av RSAT.</span><span class="sxs-lookup"><span data-stu-id="6ed03-104">This topic is a tutorial that helps you get setup and get started with RSAT and the tools associated with using RSAT.</span></span> 

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="6ed03-105">Bruk nettleserverktøyene til å laste ned og lagre denne siden i PDF-format.</span><span class="sxs-lookup"><span data-stu-id="6ed03-105">Use your internet browser tools to download and save this page in PDF format.</span></span> 

## <a name="key-concepts"></a><span data-ttu-id="6ed03-106">Nøkkelbegreper</span><span class="sxs-lookup"><span data-stu-id="6ed03-106">Key concepts</span></span>

- <span data-ttu-id="6ed03-107">Forstå installasjonen og den nødvendige konfigurasjonen som kreves for de ulike programmene som støtter RSAT (Regression Suite Automation Tool).</span><span class="sxs-lookup"><span data-stu-id="6ed03-107">Understand the installation and prerequisite setup that are required for the various applications that support Regression suite automation tool (RSAT).</span></span>
- <span data-ttu-id="6ed03-108">Forstå hvordan du kan bruke oppgaveopptakerfunksjonen i Microsoft Dynamics 365 for Finance and Operations, sammen med Microsoft Dynamics Lifecycle Services (LCS) og Microsoft Azure DevOps, til å opprette, konfigurere, kjøre, undersøke og rapportere testtilfeller.</span><span class="sxs-lookup"><span data-stu-id="6ed03-108">Understand how the Task recorder feature in Microsoft Dynamics 365 for Finance and Operations, together with Microsoft Dynamics Lifecycle Services (LCS) and Microsoft Azure DevOps, let you create, configure, run, investigate, and report on test cases.</span></span>
- <span data-ttu-id="6ed03-109">Gi funksjonsbrukere muligheten til å registrere forretningsoppgaver ved hjelp av oppgaveopptakeren i Finance and Operations, og konverter deretter oppgaveopptakene til en serie med automatiserte tester uten å måtte skrive kildekode.</span><span class="sxs-lookup"><span data-stu-id="6ed03-109">Empower functional users to record business tasks by using Task recorder in Finance and Operations, and then convert the task recordings into a suite of automated tests, without having to write source code.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="6ed03-110">Før du begynner</span><span class="sxs-lookup"><span data-stu-id="6ed03-110">Before you begin</span></span>

### <a name="prerequisites"></a><span data-ttu-id="6ed03-111">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="6ed03-111">Prerequisites</span></span>

- <span data-ttu-id="6ed03-112">Denne opplæringen krever et Finance and Operations-miljø som kjører Microsoft Dynamics 365 for Finance and Operations versjon 10.0 (april 2019) eller nyere.</span><span class="sxs-lookup"><span data-stu-id="6ed03-112">A Finance and Operations environment that runs Microsoft Dynamics 365 for Finance and Operations version 10.0 (April 2019) or later is required for this tutorial.</span></span> <span data-ttu-id="6ed03-113">For kunder som bruker Microsoft Dynamics 365 for Finance and Operations, støttes også Enterprise Edition 7.3, Platform update 20 (PU20) eller senere.</span><span class="sxs-lookup"><span data-stu-id="6ed03-113">For customers who are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, Platform update 20 (PU20) or later is also supported.</span></span>
- <span data-ttu-id="6ed03-114">Brukeren må ha administratorrettigheter til Finance and Operations-miljøet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-114">The user must have admin rights to the Finance and Operations environment.</span></span>
- <span data-ttu-id="6ed03-115">Du må ha tilgang til LCS for kundeleier og Azure DevOps (tidligere kalt Microsoft Visual Studio Team Services \[VSTS\]).</span><span class="sxs-lookup"><span data-stu-id="6ed03-115">You must have access to the customer tenant LCS and Azure DevOps (previously known as Microsoft Visual Studio Team Services \[VSTS\]).</span></span>
- <span data-ttu-id="6ed03-116">Brukeren som oppretter og administrerer seriene med tester, må ha en lisens for Azure DevOps Test Plans eller Test Manager.</span><span class="sxs-lookup"><span data-stu-id="6ed03-116">The user that is creating and managing tests suites must have an Azure DevOps Test Plans or Test Manager license.</span></span> <span data-ttu-id="6ed03-117">Følgende lisenser gir deg også tilgang til Test Plans:</span><span class="sxs-lookup"><span data-stu-id="6ed03-117">The following licenses will also give you access to Test Plans:</span></span>
    - <span data-ttu-id="6ed03-118">Visual Studio Enterprise-lisens</span><span class="sxs-lookup"><span data-stu-id="6ed03-118">Visual Studio Enterprise license</span></span>
    - <span data-ttu-id="6ed03-119">Visual Studio Test Professional-lisens</span><span class="sxs-lookup"><span data-stu-id="6ed03-119">Visual Studio Test Professional license</span></span>
    - <span data-ttu-id="6ed03-120">Abonnentlisens for MSDN-plattformer</span><span class="sxs-lookup"><span data-stu-id="6ed03-120">MSDN Platforms subscriber license</span></span>
- <span data-ttu-id="6ed03-121">RSAT må ha tilgang til testmiljøet via en nettleser.</span><span class="sxs-lookup"><span data-stu-id="6ed03-121">RSAT must have access to the test environment via a web browser.</span></span>
- <span data-ttu-id="6ed03-122">Hvis du vil generere og redigere testparametere, må du ha Microsoft Excel installert.</span><span class="sxs-lookup"><span data-stu-id="6ed03-122">To generate and edit test parameters, you must have Microsoft Excel installed.</span></span>

## <a name="configure-azure-devops"></a><span data-ttu-id="6ed03-123">Konfigurer Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="6ed03-123">Configure Azure DevOps</span></span>

### <a name="user-eligibility"></a><span data-ttu-id="6ed03-124">Brukerrettigheter</span><span class="sxs-lookup"><span data-stu-id="6ed03-124">User eligibility</span></span>

<span data-ttu-id="6ed03-125">Kontroller at brukeren er opprettet i Azure DevOps og har et abonnementsnivå som gir tilgang til Azure Test Plans.</span><span class="sxs-lookup"><span data-stu-id="6ed03-125">Make sure that the user is created in Azure DevOps and has a subscription level that provides access to Azure Test Plans.</span></span> <span data-ttu-id="6ed03-126">En lisens for Azure DevOps Test Plans kreves bare hvis brukeren skal opprette og administrere testtilfeller (det vil si at ikke alle RSAT-brukere trenger denne lisensen).</span><span class="sxs-lookup"><span data-stu-id="6ed03-126">An Azure DevOps Test Plans license is required only if the user will create and manage test cases (that is, not all RSAT users require this license).</span></span> <span data-ttu-id="6ed03-127">Hvis du vil ha informasjon om lisenskrav, kan du se [Lisenskrav](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).</span><span class="sxs-lookup"><span data-stu-id="6ed03-127">For information about the license requirements, see [License requirements](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).</span></span>

### <a name="create-a-new-azure-devops-project"></a><span data-ttu-id="6ed03-128">Opprette et nytt Azure DevOps-prosjekt</span><span class="sxs-lookup"><span data-stu-id="6ed03-128">Create a new Azure DevOps project</span></span>
<span data-ttu-id="6ed03-129">RSAT bruker Azure Devops til administrasjon av testtilfeller og testserier, rapportering og undersøkelse testkjøringsresultater.</span><span class="sxs-lookup"><span data-stu-id="6ed03-129">RSAT uses Azure Devops for test case and test suite management, reporting, and investigating test run results.</span></span> 

> [!NOTE]
> <span data-ttu-id="6ed03-130">Du kan bruke et eksisterende Azure DevOps-prosjekt.</span><span class="sxs-lookup"><span data-stu-id="6ed03-130">You can use an existing Azure DevOps project.</span></span> <span data-ttu-id="6ed03-131">Hvis det eksisterende Azure DevOps-prosjektet imidlertid er konfigurert slik at det har en egendefinert mal, får du feilmeldingen «Feil under VSTS-synkronisering» når du synkroniserer testtilfeller fra Forretningsprosessmodelerer (BPM) til Azure DevOps (se delen [Teste synkroniseringen fra BPM til Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops)).</span><span class="sxs-lookup"><span data-stu-id="6ed03-131">However, if your existing Azure DevOps project is set up so that it has a custom template, you will receive a "VSTS Sync Failure" error when you sync test cases from Business process modeler (BPM) to Azure DevOps (see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section).</span></span> <span data-ttu-id="6ed03-132">Hvis du har fulgt følgende anbefalte fremgangsmåter for den egendefinerte malen, kan du synkronisere testtilfellene til Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6ed03-132">If the following best practices have been followed for the custom template, you will be able to sync the test cases to Azure DevOps.</span></span> <span data-ttu-id="6ed03-133">(Disse anbefalte fremgangsmåtene vises i feilmeldingen.)</span><span class="sxs-lookup"><span data-stu-id="6ed03-133">(These best practices are listed in the error message.)</span></span>

- <span data-ttu-id="6ed03-134">Ikke slett arbeidselementtyper eller standardfelt.</span><span class="sxs-lookup"><span data-stu-id="6ed03-134">Do not delete any work item types or out-of-the-box fields.</span></span>
- <span data-ttu-id="6ed03-135">Ikke slett statusen til en arbeidselementtype.</span><span class="sxs-lookup"><span data-stu-id="6ed03-135">Do not delete any state of a work item type.</span></span>
- <span data-ttu-id="6ed03-136">Ikke legg til obligatoriske felt i en arbeidselementtype.</span><span class="sxs-lookup"><span data-stu-id="6ed03-136">Do not add any required fields to a work item type.</span></span>

![Feilmelding med en liste over anbefalte fremgangsmåter](./media/setup_rsa_tool_02.png)

<span data-ttu-id="6ed03-138">For denne opplæringen anbefaler vi for øvrig at du oppretter et nytt Azure DevOps-prosjekt.</span><span class="sxs-lookup"><span data-stu-id="6ed03-138">Otherwise, for this tutorial, we recommend that you create a new Azure DevOps project.</span></span> <span data-ttu-id="6ed03-139">Hvis du vil ha mer informasjon, kan du se [Problemer ved synkronisering til BPM når du bruker en egendefinert mal for Azure DevOps-prosess (VSTS)](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span><span class="sxs-lookup"><span data-stu-id="6ed03-139">For more information, see [Issues when syncing to BPM using a custom Azure DevOps (VSTS) process template](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span></span>

1. <span data-ttu-id="6ed03-140">Åpne URL-adressen til Azure DevOps (`https://dev.azure.com/<Azure DevOps Name>`).</span><span class="sxs-lookup"><span data-stu-id="6ed03-140">Open the Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).</span></span>
2. <span data-ttu-id="6ed03-141">Velg **Opprett prosjekt** i øvre høyre hjørne på Azure DevOps-siden.</span><span class="sxs-lookup"><span data-stu-id="6ed03-141">Select **Create project** in the upper-right corner of the Azure DevOps page.</span></span>

    ![Opprett prosjekt-knappen](./media/setup_rsa_tool_03.png)

3. <span data-ttu-id="6ed03-143">Fyll ut følgende felt, og velg deretter **Opprett**:</span><span class="sxs-lookup"><span data-stu-id="6ed03-143">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="6ed03-144">**Prosjektnavn**</span><span class="sxs-lookup"><span data-stu-id="6ed03-144">**Project name**</span></span>
    - <span data-ttu-id="6ed03-145">**Versjonskontroll** – Velg **Team Foundation Version Control**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-145">**Version control** – Select **Team Foundation Version Control**.</span></span> <span data-ttu-id="6ed03-146">Vær oppmerksom på at standardalternativet **Git** ikke støttes.</span><span class="sxs-lookup"><span data-stu-id="6ed03-146">Note that the default option, **Git**, isn't supported.</span></span>
    - <span data-ttu-id="6ed03-147">**Arbeidselementbehandling**</span><span class="sxs-lookup"><span data-stu-id="6ed03-147">**Work item process**</span></span>

    ![Dialogboksen Opprett nytt prosjekt](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a><span data-ttu-id="6ed03-149">Opprette et personlig tilgangstoken</span><span class="sxs-lookup"><span data-stu-id="6ed03-149">Create a personal access token</span></span>

<span data-ttu-id="6ed03-150">I denne opplæringen skal du bruke Forretningsprosessmodelerer (BPM) i LCS til å opprette et bibliotek for testtilfeller og synkronisere testtilfellene med Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6ed03-150">In this tutorial, you will use the LCS Business Process Modeler (BPM) to create a test case library and synchronize your test cases with Azure DevOps.</span></span> <span data-ttu-id="6ed03-151">Du må ha et personlig tilgangstoken for å synkronisere BPM med Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6ed03-151">You will need a personal access token to sync BPM with Azure DevOps.</span></span>

1. <span data-ttu-id="6ed03-152">Velg profilikonet i øvre høyre hjørne på siden for Azure DevOps-prosjektet, og velg deretter **Sikkerhet**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-152">Select the profile icon in the upper-right corner of the page for your Azure DevOps project, and then select **Security**.</span></span>

    ![Sikkerhet-kommandoen](./media/setup_rsa_tool_05.png)

2. <span data-ttu-id="6ed03-154">Velg **Personlige tilgangstokener** under **Sikkerhet** i venstre rute.</span><span class="sxs-lookup"><span data-stu-id="6ed03-154">In the left pane, under **Security**, select **Personal access tokens**.</span></span> <span data-ttu-id="6ed03-155">Velg deretter **Nytt token**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-155">Then select **New Token**.</span></span>

    ![Nytt token-knappen i fanen Personlige tilgangstokener i Brukerinnstillinger](./media/setup_rsa_tool_06.png)

3. <span data-ttu-id="6ed03-157">Fyll ut følgende felt, og velg deretter **Opprett**:</span><span class="sxs-lookup"><span data-stu-id="6ed03-157">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="6ed03-158">**Navn**</span><span class="sxs-lookup"><span data-stu-id="6ed03-158">**Name**</span></span>
    - <span data-ttu-id="6ed03-159">**Utløp (UTC)** – Velg **Egendefinert**, og bruk deretter datovelgeren til å velge den siste tilgjengelige datoen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-159">**Expiration (UTC)** – Select **Custom defined**, and then use the date picker to select the last available date.</span></span>
    - <span data-ttu-id="6ed03-160">**Omfang** – Velg alternativet **Full tilgang**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-160">**Scopes** – Select the **Full access** option.</span></span>

    ![Dialogboksen for å opprette et nytt personlig tilgangstoken](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > <span data-ttu-id="6ed03-162">Noter deg det personlige tilgangstokenet som opprettes.</span><span class="sxs-lookup"><span data-stu-id="6ed03-162">Make a note of the personal access token that is created.</span></span> <span data-ttu-id="6ed03-163">Du får bruk for det senere når du foretar RSAT-konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-163">You will need it later when you set up the RSAT configuration.</span></span>

    ![Personlig tilgangstoken](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a><span data-ttu-id="6ed03-165">Konfigurere LCS-prosjektet</span><span class="sxs-lookup"><span data-stu-id="6ed03-165">Configure the LCS project</span></span>

<span data-ttu-id="6ed03-166">Du trenger et LCS-prosjekt (Lifecycle Services) for hovedtestbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="6ed03-166">You need a Lifecycle Services (LCS) project for your master test library.</span></span> <span data-ttu-id="6ed03-167">Forretningsprosessmodelerer (BPM) i LCS brukes som hovedbibliotek for testtilfellene.</span><span class="sxs-lookup"><span data-stu-id="6ed03-167">The LCS Business Process Modeler (BPM) is used as the master library for your test cases.</span></span> <span data-ttu-id="6ed03-168">BPM brukes til å administrere og distribuere testbiblioteker på tvers av LCS-prosjekter.</span><span class="sxs-lookup"><span data-stu-id="6ed03-168">BPM is used to manage and distribute test libraries across LCS projects.</span></span> <span data-ttu-id="6ed03-169">En Microsoft-partner eller uavhengig programvareleverandør som for eksempel bygger testbiblioteker, gir ut testtilfeller i form av BPM-biblioteker.</span><span class="sxs-lookup"><span data-stu-id="6ed03-169">For example, a Microsoft partner or independent software vendor (ISV) building test libraries will release test cases in the form of BPM libraries.</span></span> <span data-ttu-id="6ed03-170">I BPM organiseres testtilfeller etter forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="6ed03-170">In BPM, test cases are organized by business process.</span></span> <span data-ttu-id="6ed03-171">BPM definerer ikke utføringsrekkefølgen eller -frekvensen for testomgangen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-171">BPM doesn't define the execution order or frequency of your test pass.</span></span> <span data-ttu-id="6ed03-172">Disse detaljene administreres i Azure DevOps, som beskrevet senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-172">These details are managed in Azure DevOps, as described later in this topic.</span></span>  

<span data-ttu-id="6ed03-173">For LCS-prosjektet kan du bruke en eksisterende kundeimplementering eller et eksisterende partnerprosjekt.</span><span class="sxs-lookup"><span data-stu-id="6ed03-173">For your LCS project, you can use an existing customer implementation or partner project.</span></span>

### <a name="update-the-lcs-language"></a><span data-ttu-id="6ed03-174">Oppdatere LCS-språket</span><span class="sxs-lookup"><span data-stu-id="6ed03-174">Update the LCS language</span></span>

> [!NOTE]
> <span data-ttu-id="6ed03-175">For at brukergrensesnittet (UI) skal kunne vise forretningsprosesser på riktig måte, må det foretrukne LCS-språket settes til **Engelsk (USA)**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-175">For the user interface (UI) to correctly show business processes, the LCS preferred language must be set to **English (United States)**.</span></span>

1. <span data-ttu-id="6ed03-176">Gå til LCS-implementeringsprosjektet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-176">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="6ed03-177">Velg **Innstillinger**-knappen (tannhjulsymbolet) i øvre høyre hjørne på siden, og velg deretter **Språkinnstilling**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-177">Select the **Settings** button (the gear symbol) in the upper-right corner, and then select **Language preference**.</span></span>

    ![Kommandoene på Innstillinger-menyen](./media/setup_rsa_tool_09.png)

3. <span data-ttu-id="6ed03-179">I feltet **Foretrukket språk** velger du **Engelsk (USA)** og deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-179">In the **Preferred language** field, select **English (United States)**, and then select **Save**.</span></span>

    ![Språkinnstilling-fanen i Brukerinnstillinger](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a><span data-ttu-id="6ed03-181">Konfigurere LCS for å koble til Azure DevOps-prosjektet</span><span class="sxs-lookup"><span data-stu-id="6ed03-181">Configure LCS to connect to the Azure DevOps project</span></span>

<span data-ttu-id="6ed03-182">Hvis du opprettet et nytt Azure DevOps-prosjekt tidligere, konfigurerer du LCS-prosjektet for å koble til det.</span><span class="sxs-lookup"><span data-stu-id="6ed03-182">If you created a new Azure DevOps project earlier, configure the LCS project to connect to it.</span></span> <span data-ttu-id="6ed03-183">Hvis LCS-prosjektet imidlertid allerede er koblet til Azure DevOps-prosjektet, kan du gå videre til neste del.</span><span class="sxs-lookup"><span data-stu-id="6ed03-183">Otherwise, if your LCS project is already connected to your Azure DevOps project, you can continue to the next section.</span></span>

1. <span data-ttu-id="6ed03-184">Gå til LCS-implementeringsprosjektet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-184">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="6ed03-185">Velg **Meny**-knappen, og velg deretter **Prosjektinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-185">Select the **Menu** button, and then select **Project settings**.</span></span>

    ![Prosjektinnstillinger-kommandoen](./media/setup_rsa_tool_11.png)

3. <span data-ttu-id="6ed03-187">I venstre rute velger du **Visual Studio Team Services**, og deretter velger du **Konfigurer Visual Studio Team Services**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-187">In the left pane, select **Visual Studio Team Services**, and then select **Setup Visual Studio Team Services**.</span></span>

    ![Fanen Visual Studio Team Services i Prosjektinnstillinger](./media/setup_rsa_tool_12.png)

4. <span data-ttu-id="6ed03-189">I feltet **URL-adresse til Azure DevOps-området** angir du URL-adressen til Azure DevOps-området.</span><span class="sxs-lookup"><span data-stu-id="6ed03-189">In the **Azure DevOps site URL** field, enter the URL of the Azure DevOps site.</span></span> <span data-ttu-id="6ed03-190">I feltet **Personlig tilgangstoken** angir du det personlige tilgangstokenet som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="6ed03-190">In the **Personal access token** field, enter the personal access token that was created earlier.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ed03-191">Selv om VSTS nå kalles Azure DevOps, bruker du den gamle URL-adressen til å koble LCS til Azure DevOps-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-191">Although VSTS is now known as Azure DevOps, to connect LCS to your Azure DevOps project, use the old URL.</span></span> <span data-ttu-id="6ed03-192">URL-adressen til Azure DevOps som brukes i denne opplæringen, er for eksempel `https://dev.azure.com/D365FOFastTrack/`.</span><span class="sxs-lookup"><span data-stu-id="6ed03-192">For example, the Azure DevOps URL that is used in this tutorial is `https://dev.azure.com/D365FOFastTrack/`.</span></span> <span data-ttu-id="6ed03-193">I illustrasjonen nedenfor er den imidlertid angitt som `https://D365FOFastTrack.visualstudio.com/`.</span><span class="sxs-lookup"><span data-stu-id="6ed03-193">However, in the following illustration, it's entered as `https://D365FOFastTrack.visualstudio.com/`.</span></span>

    ![Trinn 1 i Konfigurer Visual Studio Team Services](./media/setup_rsa_tool_13.png)

5. <span data-ttu-id="6ed03-195">Velg **Fortsett**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-195">Select **Continue**.</span></span>
6. <span data-ttu-id="6ed03-196">I feltet **Visual Studio Team Services-prosjektet** velger du VSTS-prosjektet på det valgte området som skal kobles til LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-196">In the **Visual Studio Team Services project** field, select the VSTS project on the selected site to link with the LCS project.</span></span> <span data-ttu-id="6ed03-197">**Prosessmal**-feltet er satt til **Fleksibel** som standard.</span><span class="sxs-lookup"><span data-stu-id="6ed03-197">The **Process template** field is set to **Agile** by default.</span></span> <span data-ttu-id="6ed03-198">Når det gjelder en egendefinert mal, ser du gjennom veiledningen for anbefalte fremgangsmåter i delen [Opprette et nytt Azure DevOps-prosjekt](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="6ed03-198">For a custom template, review the best practice guidance in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span> <span data-ttu-id="6ed03-199">Velg deretter **Fortsett**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-199">Then select **Continue**.</span></span>

    ![Trinn 2 i Konfigurer Visual Studio Team Services](./media/setup_rsa_tool_14.png)

7. <span data-ttu-id="6ed03-201">Se gjennom innstillingene, og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-201">Review your settings, and then select **Save**.</span></span>

    ![Trinn 3 i Konfigurer Visual Studio Team Services](./media/setup_rsa_tool_15.png)

8. <span data-ttu-id="6ed03-203">Velg **Autoriser** for å autorisere at LCS kan få tilgang til det konfigurerte Azure DevOps-området på vegne av deg, og for å aktivere funksjoner som kan integreres med VSTS.</span><span class="sxs-lookup"><span data-stu-id="6ed03-203">Select **Authorize** to authorize LCS to access the configured Azure DevOps site on your behalf and to turn on features that integrate with VSTS.</span></span>

    ![Autoriser-knappen](./media/setup_rsa_tool_16.png)

9. <span data-ttu-id="6ed03-205">Det vises en meldingsboks der det står «Du er i ferd med å bli omdirigert til et eksternt område for å gi Lifecycle Services tilgang til å koble til Visual Studio Team Services på dine vegne.</span><span class="sxs-lookup"><span data-stu-id="6ed03-205">A message box appears that states, "You are about to be redirected to an eternal site to authorize LCS to connect to Visual Studio Team Services on your behalf.</span></span> <span data-ttu-id="6ed03-206">Fortsette?»</span><span class="sxs-lookup"><span data-stu-id="6ed03-206">Proceed?"</span></span> <span data-ttu-id="6ed03-207">Velg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-207">Select **Yes**.</span></span>

    ![Meldingsboks](./media/setup_rsa_tool_17.png)

10. <span data-ttu-id="6ed03-209">Velg **Godta**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-209">Select **Accept**.</span></span>

    ![Autorisere tilgang](./media/setup_rsa_tool_18.png)

11. <span data-ttu-id="6ed03-211">Hvis du er autorisert som bruker, skal brukergrensesnittet sende deg tilbake til siden for LCS-prosjektinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="6ed03-211">If you're authorized as a user, the UI should you return to the LCS project settings page.</span></span>

    ![Autorisert bruker](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a><span data-ttu-id="6ed03-213">Opprett et nytt BPM-bibliotek</span><span class="sxs-lookup"><span data-stu-id="6ed03-213">Create a new BPM library</span></span>

1. <span data-ttu-id="6ed03-214">Gå til LCS-implementeringsprosjektet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-214">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="6ed03-215">Velg **Meny**-knappen, og velg deretter **Forretningsprosessmodelerer**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-215">Select the **Menu** button, and then select **Business process modeler**.</span></span>

    ![Kommandoen Forretningsprosessmodelerer](./media/setup_rsa_tool_20.png)

3. <span data-ttu-id="6ed03-217">Velg **Nytt bibliotek**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-217">Select **New library**.</span></span>

    ![Nytt bibliotek-knappen](./media/setup_rsa_tool_21.png)

4. <span data-ttu-id="6ed03-219">Skriv inn et navn i feltet **Navn på bibliotek**, og velg deretter **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-219">In the **Library name** field, enter a name, and then select **Create**.</span></span> <span data-ttu-id="6ed03-220">For denne opplæringen gir du BPM-biblioteket navnet **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-220">For this tutorial, name the BPM library **RSAT**.</span></span>

    ![Dialogboksen Opprett nytt bibliotek](./media/setup_rsa_tool_22.png)

5. <span data-ttu-id="6ed03-222">Åpne det nye BPM-biblioteket **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-222">Open the new **RSAT** BPM library.</span></span>
6. <span data-ttu-id="6ed03-223">Velg prosessen **Eksempel på kjerneforretningsprosess**, og velg deretter **Redigeringsmodus** til høyre.</span><span class="sxs-lookup"><span data-stu-id="6ed03-223">Select the **Sample Core Business Process** process, and then, on the right, select **Edit mode**.</span></span>

    ![Redigeringsmodus-knappen](./media/setup_rsa_tool_23.png)

7. <span data-ttu-id="6ed03-225">Endre verdien i **Navn**-feltet og **Beskrivelse**-feltet til **Opprett et produkt**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-225">Change the value of both the **Name** field and the **Description** field to **Create a product**.</span></span> <span data-ttu-id="6ed03-226">Velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-226">Then select **Save**.</span></span>

    ![Feltene Navn og Beskrivelse](./media/setup_rsa_tool_24.png)

## <a name="finance-and-operations-environment"></a><span data-ttu-id="6ed03-228">Finance and Operations-miljøet</span><span class="sxs-lookup"><span data-stu-id="6ed03-228">Finance and Operations environment</span></span>

### <a name="version-requirement"></a><span data-ttu-id="6ed03-229">Versjonskrav</span><span class="sxs-lookup"><span data-stu-id="6ed03-229">Version requirement</span></span>

<span data-ttu-id="6ed03-230">En Finance and Operations-test eller et sandkassemiljø som kjører versjon 10, er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="6ed03-230">A Finance and Operations test or sandbox environment that runs version 10 is required.</span></span> <span data-ttu-id="6ed03-231">For kunder som bruker versjon 7.3, støttes også Platform update 20 eller senere.</span><span class="sxs-lookup"><span data-stu-id="6ed03-231">For customers that are using version 7.3, Platform update 20 or later is also supported.</span></span>

> [!NOTE]
> <span data-ttu-id="6ed03-232">RSAT må ha tilgang til Finance and Operations-testmiljøet via en nettleser.</span><span class="sxs-lookup"><span data-stu-id="6ed03-232">RSAT must have access to your Finance and Operations test environment via a web browser.</span></span>

### <a name="user-criteria"></a><span data-ttu-id="6ed03-233">Brukerkriterier</span><span class="sxs-lookup"><span data-stu-id="6ed03-233">User criteria</span></span>

<span data-ttu-id="6ed03-234">Brukeren må ha administratorrettigheter til dette miljøet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-234">The user must have admin rights to this environment.</span></span>

### <a name="set-up-help-settings-to-connect-with-lcs"></a><span data-ttu-id="6ed03-235">Konfigurere Hjelp-innstillinger for å koble til LCS</span><span class="sxs-lookup"><span data-stu-id="6ed03-235">Set up Help settings to connect with LCS</span></span>

<span data-ttu-id="6ed03-236">Dette trinnet er nødvendig for å kunne koble til LCS, slik at oppgaveopptak kan lagres i riktig BPM-bibliotek i LCS via Finance and Operations-klienten.</span><span class="sxs-lookup"><span data-stu-id="6ed03-236">This step is required in order to connect with LCS so that task recordings can be saved to the appropriate BPM library in LCS through the Finance and Operations client.</span></span>

1. <span data-ttu-id="6ed03-237">Åpne Finance and Operations-klienten.</span><span class="sxs-lookup"><span data-stu-id="6ed03-237">Open the Finance and Operations client.</span></span>
2. <span data-ttu-id="6ed03-238">Gå til **Systemadministrasjon \> Oppsett \> Systemparametere**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-238">Go to **System Administration \> Setup \> System parameters**.</span></span>
3. <span data-ttu-id="6ed03-239">I feltet **Konfigurasjon av hjelp for Lifecycle Services** i **Hjelp**-fanen velger du det relevante LCS-prosjektet (**RSAT** for denne opplæringen).</span><span class="sxs-lookup"><span data-stu-id="6ed03-239">On the **Help** tab, in the **Lifecycle Services help configuration** field, select the relevant LCS project (**RSAT** for this tutorial).</span></span>

    ![Feltet Konfigurasjon av hjelp for Lifecycle Services i Hjelp-fanen](./media/setup_rsa_tool_25.png)

    <span data-ttu-id="6ed03-241">BPM-biblioteker fylles ut i det riktige LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-241">BPM libraries are filled in under the appropriate LCS project.</span></span>

4. <span data-ttu-id="6ed03-242">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-242">Select **Save**.</span></span>
5. <span data-ttu-id="6ed03-243">Du må kanskje oppdatere nettleseren for å kunne se det oppdaterte innholdet i Hjelp.</span><span class="sxs-lookup"><span data-stu-id="6ed03-243">You might have to refresh the browser to see the updated Help content.</span></span>

    ![Varsling om oppdatering av nettleseren](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a><span data-ttu-id="6ed03-245">Oppgaveopptak</span><span class="sxs-lookup"><span data-stu-id="6ed03-245">Task recordings</span></span>

> [!NOTE]
> <span data-ttu-id="6ed03-246">Kontroller at alle oppgaveopptakene starter på hovedinstrumentbordet for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6ed03-246">Make sure that all your task recordings start on the main dashboard of Finance and Operations.</span></span> <span data-ttu-id="6ed03-247">Hold individuelle opptak korte, og fokuser på én forretningsoppgave, for eksempel opprettelse av en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="6ed03-247">Keep individual recordings short, and focus on one business task, such as creating a sales order.</span></span>

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a><span data-ttu-id="6ed03-248">Opprette et oppgaveopptak og lagre det i BPM-biblioteket</span><span class="sxs-lookup"><span data-stu-id="6ed03-248">Create a task recording and save it to the BPM library</span></span>

<span data-ttu-id="6ed03-249">Opprett et tilsvarende oppgaveopptak du kan knytte til den enkle forretningsprosessen som ble opprettet i det nye BPM-biblioteket.</span><span class="sxs-lookup"><span data-stu-id="6ed03-249">Create a corresponding task recording that you can attach to the simple business process that was created in the new BPM library.</span></span>

1. <span data-ttu-id="6ed03-250">Åpne Finance and Operations-klienten.</span><span class="sxs-lookup"><span data-stu-id="6ed03-250">Open the Finance and Operations client.</span></span>
2. <span data-ttu-id="6ed03-251">Velg **Innstillinger**-knappen (tannhjulsymbolet) på hovedinstrumentbordet, og velg deretter **Oppgaveopptaker**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-251">On the main dashboard, select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>

    ![Kommandoene på Innstillinger-menyen](./media/setup_rsa_tool_27.png)

3. <span data-ttu-id="6ed03-253">Velg **Opprett opptak**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-253">Select **Create recording**.</span></span>

    ![Opprett opptak-knappen](./media/setup_rsa_tool_28.png)

4. <span data-ttu-id="6ed03-255">Fyll ut feltene **Navn på opptak** og **Beskrivelse av opptak**, og velg deretter **Start**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-255">Fill in the **Recording name** and **Recording description** fields, and then select **Start**.</span></span>

    ![Feltene Navn på opptak og Beskrivelse av opptak](./media/setup_rsa_tool_29.png)

5. <span data-ttu-id="6ed03-257">Ta opp trinnene for å opprette et produkt.</span><span class="sxs-lookup"><span data-stu-id="6ed03-257">Record the steps for creating a product.</span></span> <span data-ttu-id="6ed03-258">Når du er ferdig, velger du **Stopp** for å stoppe opptaket.</span><span class="sxs-lookup"><span data-stu-id="6ed03-258">When you've finished, select **Stop** to stop recording.</span></span>

    ![Trinn for å opprette et produkt](./media/setup_rsa_tool_30.png)

6. <span data-ttu-id="6ed03-260">Velg **Lagre i Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-260">Select **Save to Lifecycle Services**.</span></span>

    ![Lagringsalternativer](./media/setup_rsa_tool_31.png)

    <span data-ttu-id="6ed03-262">Bibliotekinformasjon lastes inn fra LCS.</span><span class="sxs-lookup"><span data-stu-id="6ed03-262">Library information is loaded from LCS.</span></span>

    ![Fremdriftsindikator](./media/setup_rsa_tool_32.png)

7. <span data-ttu-id="6ed03-264">Velg BPM-biblioteket som oppgaveopptaket skal knyttes til.</span><span class="sxs-lookup"><span data-stu-id="6ed03-264">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="6ed03-265">For denne opplæringen velger du BPM-biblioteket **RSAT** som ble opprettet tidligere, og forretningsprosessen **Opprett et produkt** under det.</span><span class="sxs-lookup"><span data-stu-id="6ed03-265">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Create a product** business process under it.</span></span> <span data-ttu-id="6ed03-266">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-266">Then select **OK**.</span></span>

    ![Knytte oppgaveopptaket til et BPM-bibliotek og en forretningsprosess](./media/setup_rsa_tool_33.png)

    <span data-ttu-id="6ed03-268">Meldingen «Lagring i Lifecycle Services er utført» vises.</span><span class="sxs-lookup"><span data-stu-id="6ed03-268">A "Saving to Lifecycle Services was successful" message appears.</span></span>

    ![Melding om vellykket lagring i LCS](./media/setup_rsa_tool_34.png)

8. <span data-ttu-id="6ed03-270">Hvis du vil lagre oppgaveopptaket lokalt og deretter laste det opp til BPM via LCS, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="6ed03-270">If you want to save the task recording locally and then upload it to BPM through LCS, follow these steps:</span></span>

    1. <span data-ttu-id="6ed03-271">Når opptaket er fullført, velger du **Lagre på denne PC-en**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-271">After the recording is completed, select **Save to this PC**.</span></span>

        ![Lagringsalternativer](./media/setup_rsa_tool_35.png)

    2. <span data-ttu-id="6ed03-273">I nettleserens varslingsfelt velger du **Lagre** eller **Lagre som** for å lagre filen på den lokale datamaskinen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-273">In the browser's Notification bar, select **Save** or **Save As** to save the file on your local computer.</span></span>

        ![Varslingsfelt](./media/setup_rsa_tool_36.png)

    3. <span data-ttu-id="6ed03-275">Gå til BPM-biblioteket **RSAT**, og velg forretningsprosessen du vil lagre oppgaveopptaket mot.</span><span class="sxs-lookup"><span data-stu-id="6ed03-275">Go to the **RSAT** BPM library, and select the business process to save the task recording against.</span></span>
    4. <span data-ttu-id="6ed03-276">Velg **Last opp** i **Oversikt**-fanen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-276">On the **Overview** tab, select **Upload**.</span></span>

        ![Last opp-knappen](./media/setup_rsa_tool_37.png)

    5. <span data-ttu-id="6ed03-278">Velg **Bla gjennom**, og velg AXTR-filen du lagret tidligere.</span><span class="sxs-lookup"><span data-stu-id="6ed03-278">Select **Browse**, and select the .axtr file that you saved earlier.</span></span> <span data-ttu-id="6ed03-279">Velg deretter **Last opp**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-279">Then select **Upload**.</span></span>

        ![Velge AXTR-filen som skal lastes opp](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a><span data-ttu-id="6ed03-281">Teste synkroniseringen fra BPM til Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="6ed03-281">Test the synchronization from BPM to Azure DevOps</span></span>

<span data-ttu-id="6ed03-282">Nå som et oppgaveopptak er knyttet til forretningsprosessen, må du validere at forretningsprosessen og det tilknyttede oppgaveopptaket kan synkroniseres til Azure DevOps som (henholdsvis) en funksjon og et testtilfelle, ved å bruke VSTS-synkroniseringsfunksjonen i LCS.</span><span class="sxs-lookup"><span data-stu-id="6ed03-282">Now that a task recording is attached to the business process, you must validate that the business process and the associated task recording can be synced to Azure DevOps as a feature and a test case (respectively) by using the VSTS sync feature in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="6ed03-283">Den tilsvarende arbeidselementtypen som opprettes i Azure DevOps, varierer avhengig av prosessmalen du valgte da du konfigurerte LCS-prosjektet med Azure DevOps, som beskrevet i delen [Opprette et nytt Azure DevOps-prosjekt](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="6ed03-283">The corresponding work item type that is created in Azure DevOps will vary, depending on the process template that you selected when you configured the LCS project with Azure DevOps, as described in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span>

1. <span data-ttu-id="6ed03-284">Gå til BPM-biblioteket, og åpne **RSAT**-biblioteket du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="6ed03-284">Go to the BPM library, and open the **RSAT** library that you created earlier.</span></span>
2. <span data-ttu-id="6ed03-285">Velg ellipseknappen (**...**), og velg **VSTS-synkronisering**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-285">Select the ellipsis button (**...**), and select **VSTS sync**.</span></span>

    ![Kommandoen VSTS-synkronisering på ellipsemenyen](./media/setup_rsa_tool_39.png)

    <span data-ttu-id="6ed03-287">Etter at VSTS-synkronisering er fullført, vises det en **Behov**-fane på venstre side som omfatter det tilsvarende Azure DevOps-arbeidselementet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-287">After VSTS sync is completed, a **Requirements** tab appears on the left side and includes the corresponding Azure DevOps work item.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ed03-288">Arbeidselementet som opprettes i Azure DevOps, har navnet på BPM-biblioteket som tittelprefiks.</span><span class="sxs-lookup"><span data-stu-id="6ed03-288">The work item that is created in Azure DevOps will have the BPM library name as the title prefix.</span></span>

    ![Behov-fanen](./media/setup_rsa_tool_40.png)

3. <span data-ttu-id="6ed03-290">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="6ed03-290">Refresh the page.</span></span>
4. <span data-ttu-id="6ed03-291">Velg ellipseknappen (**...**). Det vises et ekstra alternativ, **Synkroniser testtilfeller**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-291">Select the ellipsis button (**...**). You will see an additional option, **Sync test cases**.</span></span> <span data-ttu-id="6ed03-292">Velg dette alternativet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-292">Select this option.</span></span>

    ![Kommandoen Synkroniser testtilfeller på ellipsemenyen](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > <span data-ttu-id="6ed03-294">Hvis alternativet **Synkroniser testtilfeller** ikke er tilgjengelig etter at du har oppdatert siden, går du til hovedsiden for BPM og velger **Synkroniser testtilfeller** for hele biblioteket.</span><span class="sxs-lookup"><span data-stu-id="6ed03-294">If the **Sync test cases** option isn't available after you refresh the page, go to main page for BPM, and select **Sync test cases** for the whole library itself.</span></span> <span data-ttu-id="6ed03-295">På denne måten fremtvinger du en synkronisering for hele biblioteket.</span><span class="sxs-lookup"><span data-stu-id="6ed03-295">In this way, you effectively force a synchronization for the whole library.</span></span>
    > 
    > ![Velge Synkroniser testtilfeller for hele biblioteket](./media/setup_rsa_tool_42.png)

    <span data-ttu-id="6ed03-297">Etter at Synkroniser testtilfeller er fullført, blir det opprettet et nytt testtilfelle i **Behov**-fanen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-297">After Sync test cases is completed, a new test case is created on the **Requirements** tab.</span></span>

    ![Nytt testtilfelle i Behov-fanen](./media/setup_rsa_tool_43.png)

5. <span data-ttu-id="6ed03-299">Gå til Azure DevOps-prosjektet, og velg **Tavler \> Arbeidselementer**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-299">Go to your Azure DevOps project, and select **Boards \> Work Items**.</span></span>

    ![Kommandoen Arbeidselementer under Tavler](./media/setup_rsa_tool_44.png)

6. <span data-ttu-id="6ed03-301">Valider at arbeidselementet og testtilfellet du opprettet ved hjelp av BPM-synkronisering, finnes.</span><span class="sxs-lookup"><span data-stu-id="6ed03-301">Validate that the work item and test case that you created through BPM synchronization exist.</span></span>

    ![Arbeidselement og testtilfelle](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a><span data-ttu-id="6ed03-303">Installere og konfigurere RSAT</span><span class="sxs-lookup"><span data-stu-id="6ed03-303">Install and Configure RSAT</span></span>

<span data-ttu-id="6ed03-304">Du kan installere RSAT på alle datamaskiner som kjører Windows 10 og kan koble til Finance and Operations-miljøet via en nettleser (Internet Explorer eller Google Chrome).</span><span class="sxs-lookup"><span data-stu-id="6ed03-304">RSAT can be installed on any computer that runs Windows 10 and that can connect to the Finance and Operations environment via a web browser (Internet Explorer or Google Chrome).</span></span>

> [!NOTE]
> <span data-ttu-id="6ed03-305">Før du installerer en ny versjon av verktøyet, anbefaler vi at du avinstallerer den forrige versjonen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-305">Before you install a new version of the tool, we recommend that you uninstall the previous version.</span></span>

### <a name="install-an-authentication-certificate"></a><span data-ttu-id="6ed03-306">Installere et godkjenningssertifikat</span><span class="sxs-lookup"><span data-stu-id="6ed03-306">Install an authentication certificate</span></span>

<span data-ttu-id="6ed03-307">Hvis du vil aktivere godkjenning, må du generere og installere et sertifikat på samme datamaskin som RSAT kjører på.</span><span class="sxs-lookup"><span data-stu-id="6ed03-307">To enable authentication, you must generate and install a certificate on the same computer that RSAT is running on.</span></span>

#### <a name="generate-a-certificate"></a><span data-ttu-id="6ed03-308">Generere et sertifikat</span><span class="sxs-lookup"><span data-stu-id="6ed03-308">Generate a certificate</span></span>

1. <span data-ttu-id="6ed03-309">Hvis du vil generere en sertifikatfil, åpner du et Microsoft Windows PowerShell-vindu som administrator og kjører følgende kommando:</span><span class="sxs-lookup"><span data-stu-id="6ed03-309">To generate a certificate file, open a Microsoft Windows PowerShell window as an admin, and run the following command.</span></span>

    ```
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. <span data-ttu-id="6ed03-310">Åpne sertifikatbehandling ved å skrive inn **certlm.msc** i dialogboksen **Kjør**, og bekreft at sertifikatet **D365 Automated testing certificate** er opprettet under **Personlig \> Sertifikater**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-310">Open certificate manager by entering **certlm.msc** in the **Run** dialog box, and confirm that the **D365 Automated testing certificate** certificate is created under **Personal \> Certificates**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ed03-311">Pass på at du skriver inn **certlm.msc**msc, ikke **certmgr.msc**, fordi sertifikatene er lagret på den lokale datamaskinen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-311">Be sure to enter **certlm.msc**, not **certmgr.msc**, because the certificates are stored on the local computer.</span></span>

    ![Sertifikatet D365 Automated testing certificate](./media/setup_rsa_tool_46.png)

3. <span data-ttu-id="6ed03-313">Høyreklikk på sertifikatet, og velg deretter **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-313">Right-click the certificate, and then select **Copy**.</span></span>
4. <span data-ttu-id="6ed03-314">Gå til **Klarerte rotsertifiseringsinstanser \> Sertifikater**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-314">Go to **Trusted Root Certification Authorities \> Certificates**.</span></span>

    ![Sertifikater-mappen under mappen Klarerte rotsertifiseringsinstanser](./media/setup_rsa_tool_47.png)

5. <span data-ttu-id="6ed03-316">Velg **Lim inn** på **Handling**-menyen for å kopiere sertifikatet til plasseringen **Klarerte rotsertifiseringsinstanser**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-316">On the **Action** menu, select **Paste** to copy the certificate to the **Trusted Root Certification Authorities** location.</span></span>

    ![Kommandoen Lim inn på Handling-menyen](./media/setup_rsa_tool_48.png)

6. <span data-ttu-id="6ed03-318">Hvis du vil hente avtrykket for det installerte sertifikatet, men uten mellomrom eller spesialtegn, åpner du et Windows PowerShell-vindu som administrator og kjører følgende kommandoer:</span><span class="sxs-lookup"><span data-stu-id="6ed03-318">To get the thumbprint of the installed certificate, but without spaces or special characters, open a Windows PowerShell window as an admin, and run the following commands.</span></span>

    ```
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > <span data-ttu-id="6ed03-319">Lagre avtrykket, fordi du trenger det senere når du skal oppdatere WIF-filene for AOS (Application Object Server) og foreta RSAT-konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-319">Save the thumbprint, because you will need it later when you update the .wif files for Application Object Server (AOS) and set up the RSAT configuration.</span></span>

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a><span data-ttu-id="6ed03-320">Konfigurere AOS-datamaskinen slik at den klarerer tilkoblingen</span><span class="sxs-lookup"><span data-stu-id="6ed03-320">Configure the AOS computer to trust the connection</span></span>

> [!NOTE]
> <span data-ttu-id="6ed03-321">Hvis Finance and Operations-miljøet er et miljø på Lag 2 eller høyere, må sertifikatavtrykket oppdateres i filen wif.config for **alle** AOS-datamaskiner for miljøet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-321">If the Finance and Operations environment is a Tier 2+ environment, the certificate thumbprint must be updated in the wif.config file for **all** AOS computers for the environment.</span></span>

1. <span data-ttu-id="6ed03-322">Opprett en RDP-tilkobling (Remote Desktop Protocol) til AOS-datamaskinen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-322">Establish a Remote Desktop Protocol (RDP) connection to the AOS computer.</span></span> <span data-ttu-id="6ed03-323">Påloggingsdetaljer er tilgjengelige på siden for miljødetaljer i LCS.</span><span class="sxs-lookup"><span data-stu-id="6ed03-323">Sign-in details are available on the environment details page in LCS.</span></span>
2. <span data-ttu-id="6ed03-324">Åpne Microsoft Internet Information Services (IIS), og finn **AOSService** i listen over områder.</span><span class="sxs-lookup"><span data-stu-id="6ed03-324">Open Microsoft Internet Information Services (IIS), and find **AOSService** in the list of sites.</span></span>

    ![AOSService i listen over områder](./media/setup_rsa_tool_49.png)

3. <span data-ttu-id="6ed03-326">Høyreklikk på **Utforsk** for å åpne mappen **\<Stasjon\>: \\AosService\\WebRoot**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-326">Right-click **Explore** to open the **\<Drive\>: \\AosService\\WebRoot** folder.</span></span> <span data-ttu-id="6ed03-327">Finn filen **wif.config**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-327">Find the **wif.config** file.</span></span>

    ![Filen wif.config i WebRoot-mappen](./media/setup_rsa_tool_50.png)

4. <span data-ttu-id="6ed03-329">Oppdater filen **wif.config** ved å legge til en ny instansoppføring for navnet på sertifikatet og instansen, som vist i eksemplet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="6ed03-329">Update the **wif.config** file by adding a new authority entry for your certificate and authority name, as shown in the following example.</span></span>

    ```
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > <span data-ttu-id="6ed03-330">Hvis flere brukere bruker samme program i Finance and Operations, må hver bruker generere separate avtrykk, og hvert av disse avtrykkene må legges til i **\<keys\>**-delen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-330">If multiple users are using the same Finance and Operations application, each user must generate separate thumbprints, and each of those thumbprints must be added in the **\<keys\>** section.</span></span>

5. <span data-ttu-id="6ed03-331">Hvis det er flere enn én AOS-datamaskin, gjentar du trinn 3 til og med 4 for hver ekstra datamaskin.</span><span class="sxs-lookup"><span data-stu-id="6ed03-331">If there is more than one AOS computer, repeat steps 3 through 4 for each additional computer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ed03-332">I motsetning til eldre Lag 2-miljøer distribueres nye Lag 2-miljøer med to AOS-forekomster.</span><span class="sxs-lookup"><span data-stu-id="6ed03-332">Unlike older Tier 2 environments, new Tier 2 environments are deployed with two AOS instances.</span></span>

6. <span data-ttu-id="6ed03-333">Kjør **iisreset** på alle AOS-datamaskinene.</span><span class="sxs-lookup"><span data-stu-id="6ed03-333">Run **iisreset** on all the AOS computers.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ed03-334">Hvis du ikke har administratorrettigheter til å kjøre **iisreset** på en Lag 1-datamaskin, velger du Vedlikehold > Start tjenester på nytt på siden Miljødetaljer i LCS.</span><span class="sxs-lookup"><span data-stu-id="6ed03-334">If you don't have admin rights to run **iisreset** on a Tier 1 computer, on the Environment details page in LCS, select Maintain > Restart services.</span></span>

#### <a name="tier-2-environment"></a><span data-ttu-id="6ed03-335">Miljø på Lag 2 eller høyere</span><span class="sxs-lookup"><span data-stu-id="6ed03-335">Tier 2+ environment</span></span>

<span data-ttu-id="6ed03-336">Hvis et Finance and Operations-miljø på Lag 2 eller høyere (sandkasse for standard aksepttest eller høyere), bekrefter eller angir du følgende registerinnstilling på datamaskinen der RSAT er installert.</span><span class="sxs-lookup"><span data-stu-id="6ed03-336">If a Tier 2+ (Standard Acceptance Test sandbox or higher) Finance and Operations environment is used, verify or set the following registry setting on the computer where RSAT is installed.</span></span> <span data-ttu-id="6ed03-337">Dette trinnet er nødvendig fordi det gjør at du unngår godkjenningsfeil eller RSAT-tilkoblingsfeil.</span><span class="sxs-lookup"><span data-stu-id="6ed03-337">This step is required because it helps you avoid authentication or RSAT connection errors.</span></span>

```
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a><span data-ttu-id="6ed03-338">Installere RSAT</span><span class="sxs-lookup"><span data-stu-id="6ed03-338">Install RSAT</span></span>

1. <span data-ttu-id="6ed03-339">Gå til <https://www.microsoft.com/download/details.aspx?id=57357>, og velg **Download**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-339">Go to <https://www.microsoft.com/download/details.aspx?id=57357>, and select **Download**.</span></span>
2. <span data-ttu-id="6ed03-340">Merk av for alle filene, og velg deretter **Next**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-340">Select all the files, and then select **Next**.</span></span>

    ![Merke av for alle filene](./media/setup_rsa_tool_51.png)

3. <span data-ttu-id="6ed03-342">Dobbeltklikk på MSI-pakken for å kjøre installasjonsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-342">Double-click the .msi package to run the installer.</span></span> <span data-ttu-id="6ed03-343">Når installasjonen er fullført, velger du **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-343">Then, when the installation is completed, select **Finish**.</span></span>

    ![Installasjonsprogramfilen for RSAT](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a><span data-ttu-id="6ed03-345">Installere Selenium og nettleserdrivere</span><span class="sxs-lookup"><span data-stu-id="6ed03-345">Install Selenium and browser drivers</span></span>

<span data-ttu-id="6ed03-346">I eldre versjoner av RSAT måtte du installere Selenium og nettleserdrivere.</span><span class="sxs-lookup"><span data-stu-id="6ed03-346">In older versions of RSAT, you had to install Selenium and browser drivers.</span></span> <span data-ttu-id="6ed03-347">Du trenger ikke lenger å installere disse driverne, fordi de nå installeres automatisk.</span><span class="sxs-lookup"><span data-stu-id="6ed03-347">You no longer have to install these drivers because they are automatically installed.</span></span>

1. <span data-ttu-id="6ed03-348">Første gang du åpner RSAT, blir du bedt om å laste ned og installere Selenium automatisk.</span><span class="sxs-lookup"><span data-stu-id="6ed03-348">The first time that you open RSAT, you're prompted to automatically download and install Selenium.</span></span> <span data-ttu-id="6ed03-349">Hvis du vil ha mer informasjon, kan du se delen [Konfigurere RSAT](#configure-rsat).</span><span class="sxs-lookup"><span data-stu-id="6ed03-349">For more information, see the [Configure RSAT](#configure-rsat) section.</span></span>
2. <span data-ttu-id="6ed03-350">Før du kan kjøre et testtilfelle, blir du bedt om å laste ned og installere nettleserdriveren som svarer til standardnettleseren som er valgt i RSAT-konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-350">Before you can run a test case, you're prompted to automatically download and install the browser driver that corresponds to the default browser that is selected in the RSAT configuration.</span></span> <span data-ttu-id="6ed03-351">Hvis du vil ha mer informasjon, kan du se delen [Laste inn og kjøre testtilfeller](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="6ed03-351">For more information, see the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

## <a name="get-started-with-rsat"></a><span data-ttu-id="6ed03-352">Komme i gang med RSAT</span><span class="sxs-lookup"><span data-stu-id="6ed03-352">Get started with RSAT</span></span>

### <a name="create-a-test-plan-and-test-suites"></a><span data-ttu-id="6ed03-353">Opprette en testplan og testserier</span><span class="sxs-lookup"><span data-stu-id="6ed03-353">Create a test plan and test suites</span></span>

1. <span data-ttu-id="6ed03-354">Gå til Azure DevOps-prosjektet, og velg **Testplaner**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-354">Go to the Azure DevOps project, and select **Test Plans**.</span></span>

    ![Kommandoen Testplaner](./media/setup_rsa_tool_53.png)

2. <span data-ttu-id="6ed03-356">Velg **Ny testplan**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-356">Select **New Test Plan**.</span></span>

    ![Knappen Ny testplan](./media/setup_rsa_tool_54.png)

3. <span data-ttu-id="6ed03-358">Fyll ut **Navn**-feltet, og velg deretter **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-358">Fill in the **Name** field, and then select **Create**.</span></span> <span data-ttu-id="6ed03-359">For denne opplæringen gir du testplanen navnet **RSAT-testplan**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-359">For this tutorial, name the test plan **RSAT Test Plan**.</span></span>

    ![Dialogboksen Ny testplan](./media/setup_rsa_tool_55.png)

4. <span data-ttu-id="6ed03-361">Velg plusstegnet (**+**), og velg deretter **Statisk serie** for å opprette en statisk serie under den nye testplanen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-361">Select the plus sign (**+**), and then select **Static suite** to create a static suite under the new test plan.</span></span> <span data-ttu-id="6ed03-362">Gi den nye testserien navnet **T01 – Produser for lager**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-362">Name the new test suite **T01 – Make to Stock**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ed03-363">Du kan også opprette en spørringsbasert serie hvis du vil at de nye testtilfellene fra BPM skal hentes inn i RSAT-testserien automatisk.</span><span class="sxs-lookup"><span data-stu-id="6ed03-363">You can also create a query-based suite, if you want the new test cases from BPM to be automatically pulled into the RSAT test suite.</span></span>

    ![Opprette en statisk serie](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a><span data-ttu-id="6ed03-365">Knytte testtilfeller til testserier</span><span class="sxs-lookup"><span data-stu-id="6ed03-365">Attach test cases to test suites</span></span>

1. <span data-ttu-id="6ed03-366">Velg **Legg til eksisterende** på høyre side for å legge til eksisterende testtilfeller i testserien.</span><span class="sxs-lookup"><span data-stu-id="6ed03-366">Select **Add existing** on the right side to add existing test cases to the test suite.</span></span>

    ![Knappen Legg til eksisterende](./media/setup_rsa_tool_57.png)

2. <span data-ttu-id="6ed03-368">Velg **Kjør spørring** på siden **Legg til testtilfeller i serie**, og velg deretter testtilfellet som skal legges til i testserien.</span><span class="sxs-lookup"><span data-stu-id="6ed03-368">On the **Add test cases to suite** page, select **Run query**, and then select the test case to add to the test suite.</span></span> <span data-ttu-id="6ed03-369">For denne opplæringen velger du testtilfellet **Opprett et nytt produkt**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-369">For this tutorial, select the **Create a new product** test case.</span></span> <span data-ttu-id="6ed03-370">Deretter velger du **Legg til testtilfeller** i nedre høyre hjørne på siden (denne knappen vises ikke i illustrasjonen nedenfor).</span><span class="sxs-lookup"><span data-stu-id="6ed03-370">Then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Kjør spørring-knappen](./media/setup_rsa_tool_58.png)

    <span data-ttu-id="6ed03-372">Testtilfellet legges til i testserien **T01 – Produser for lager**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-372">The test case is added to the **T01-Make to Stock** test suite.</span></span>

    ![Testtilfelle lagt til testserien](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a><span data-ttu-id="6ed03-374">Konfigurer RSAT</span><span class="sxs-lookup"><span data-stu-id="6ed03-374">Configure RSAT</span></span>

1. <span data-ttu-id="6ed03-375">Åpne RSAT.</span><span class="sxs-lookup"><span data-stu-id="6ed03-375">Open RSAT.</span></span>

    ![RSAT-ikon](./media/setup_rsa_tool_60.png)

2. <span data-ttu-id="6ed03-377">Du får en advarsel om at Regression Suite Automation Tool krever Selenium, og blir spurt om du vil automatisk laste det ned og installere det nå.</span><span class="sxs-lookup"><span data-stu-id="6ed03-377">You receive a warning message that states, "The Regression Suite Automation Tool requires Selenium, do you want to automatically download and install it now?"</span></span> <span data-ttu-id="6ed03-378">Velg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-378">Select **Yes**.</span></span>

    ![Advarselsmelding](./media/setup_rsa_tool_61.png)

3. <span data-ttu-id="6ed03-380">Velg **Innstillinger**-knappen (tannhjulsymbolet) i øvre høyre hjørne, og fyll deretter ut følgende felt i dialogboksen som vises:</span><span class="sxs-lookup"><span data-stu-id="6ed03-380">Select the **Settings** button (the gear symbol) in the upper-right corner, and then, in the dialog box that appears, fill in the following fields:</span></span>

    - <span data-ttu-id="6ed03-381">**URL-adresse til Azure DevOps** – Skriv inn URL-adressen til Azure DevOps-prosjektet, for eksempel `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span><span class="sxs-lookup"><span data-stu-id="6ed03-381">**Azure DevOps Url** – Enter the URL of your Azure DevOps project, such as `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>
    - <span data-ttu-id="6ed03-382">**Tilgangstoken** – Angi tilgangstokenet som gjør at verktøyet kan koble til Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6ed03-382">**Access Token** – Enter the access token that lets the tool connect to Azure DevOps.</span></span> <span data-ttu-id="6ed03-383">Bruk det personlige tilgangstokenet du opprettet tidligere i denne opplæringen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-383">Use the personal access token that you created earlier in this tutorial.</span></span> <span data-ttu-id="6ed03-384">Hvis du vil ha mer informasjon, kan du se [Godkjenne tilgang med personlige tilgangstokener](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span><span class="sxs-lookup"><span data-stu-id="6ed03-384">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span>
    - <span data-ttu-id="6ed03-385">**Prosjektnavn** – Velg navnet på Azure DevOps-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-385">**Project Name** – Select the name of your Azure DevOps project.</span></span>
    - <span data-ttu-id="6ed03-386">**Testplan** – Velg Azure DevOps-testplanen som inneholder testtilfellene.</span><span class="sxs-lookup"><span data-stu-id="6ed03-386">**Test Plan** – Select the Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="6ed03-387">Hvis du vil ha mer informasjon, kan du se [Opprette testplaner og testserier](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span><span class="sxs-lookup"><span data-stu-id="6ed03-387">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> <span data-ttu-id="6ed03-388">Etter at du har valgt en testplan, velger du **Test tilkobling** for å teste tilkoblingen til Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6ed03-388">After you select a test plan, select **Test Connection** to test your connection to Azure DevOps.</span></span>
    - <span data-ttu-id="6ed03-389">**Vertsnavn** – Angi vertsnavnet på Finance and Operations-testmiljøet, for eksempel **\<myaos\>.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-389">**Hostname** – Enter the host name of the Finance and Operations test environment, such as **\<myaos\>.cloudax.dynamics.com**.</span></span> <span data-ttu-id="6ed03-390">Ikke ta med prefikset **https://** eller **http://**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-390">Don't include the **https://** or **http://** prefix.</span></span>
    - <span data-ttu-id="6ed03-391">**SOAP-vertsnavn** – Angi SOAP-vertsnavnet for Finance and Operations-testmiljøet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-391">**SOAP Hostname** – Enter the SOAP host name of the Finance and Operations test environment.</span></span> <span data-ttu-id="6ed03-392">SOAP-vertsnavnet er vanligvis det samme som vertsnavnet, men det har suffikset **SOAP**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-392">Typically, the SOAP host name is the same as the host name, but it has a **soap** suffix.</span></span> <span data-ttu-id="6ed03-393">Her er et eksempel: **\<myaos\>soap.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-393">Here is an example: **\<myaos\>soap.cloudax.dynamics.com**.</span></span> <span data-ttu-id="6ed03-394">Ikke ta med prefikset **https://** eller **http://**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-394">Don't include the **https://** or **http://** prefix.</span></span>

        > [!NOTE]
        > <span data-ttu-id="6ed03-395">Du kan finne vertsnavnet og SOAP-vertsnavnet ved å åpne IIS-behandling, høyreklikke på **Områder \> AOSService** og deretter velge **Rediger bindinger**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-395">To find the host name and SOAP host name, open IIS Manager, right-click **Sites \> AOSService**, and then select **Edit bindings**.</span></span> <span data-ttu-id="6ed03-396">Verdiene i **Vertsnavn**-kolonnen gir deg vertsnavnet og SOAP-vertsnavnet (SOAP-vertsnavnet har suffikset **soap** i URL-adressen).</span><span class="sxs-lookup"><span data-stu-id="6ed03-396">The values in the **Host Name** column give you the host name and SOAP host name (the SOAP host name has the suffix **soap** in the URL).</span></span>

        ![Vertsnavn og SOAP-vertsnavn i Vertsnavn-kolonnen](./media/setup_rsa_tool_63.png)

    - <span data-ttu-id="6ed03-398">**Navn på administratorbruker** – Angi e-postadressen for administratorbruker i Finance and Operations-testmiljøet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-398">**Admin user name** – Enter the email address of an admin user in the Finance and Operations test environment.</span></span>
    - <span data-ttu-id="6ed03-399">**Avtrykk** – Angi avtrykket for godkjenningssertifikatet, som beskrevet tidligere i denne opplæringen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-399">**Thumbprint** – Enter the thumbprint of the authentication certificate, as described earlier in this tutorial.</span></span>
    - <span data-ttu-id="6ed03-400">**Arbeidskatalog** – Angi mappeplasseringen for lagring av testautomatiseringsfiler, for eksempel Excel-testdatafiler.</span><span class="sxs-lookup"><span data-stu-id="6ed03-400">**Working directory** – Specify the folder location for storing test automation files, such as Excel test data files.</span></span> <span data-ttu-id="6ed03-401">Du kan for eksempel skrive inn eller velge **C:\\Temp\\RegressionTool**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-401">For example, enter or select **C:\\Temp\\RegressionTool**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="6ed03-402">Hvis navnet på mappen har mellomrom, mislykkes kjøringen fordi mappen ikke blir funnet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-402">If the name of the folder has spaces, execution will fail because the folder can't be found.</span></span> <span data-ttu-id="6ed03-403">Dette er et kjent problem og skal være løst i den nyeste versjonen av verktøyet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-403">This issue is a known issue and should be fixed in the latest version of the tool.</span></span>

    - <span data-ttu-id="6ed03-404">**Standardnettleser** – Velg **Internet Explorer** eller **Google Chrome**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-404">**Default browser** – Select either **Internet Explorer** or **Google Chrome**.</span></span> <span data-ttu-id="6ed03-405">Kontroller at de riktige nettleserdriverne er installert.</span><span class="sxs-lookup"><span data-stu-id="6ed03-405">Make sure that the appropriate browser drivers have been installed.</span></span>
    - <span data-ttu-id="6ed03-406">**Tidsavbrudd for testkjøring** – Angi tidsavbruddsperioden for testkjøringer i minutter.</span><span class="sxs-lookup"><span data-stu-id="6ed03-406">**Test run timeout** – Specify the time-out period, in minutes, for test runs.</span></span> <span data-ttu-id="6ed03-407">Når tidsavbruddsperioden har utløpt, lukkes alle aktive vinduer, og ventende testtilfeller mislykkes.</span><span class="sxs-lookup"><span data-stu-id="6ed03-407">When the time-out period elapses, all active windows are closed, and pending test cases fail.</span></span>
    - <span data-ttu-id="6ed03-408">**Tidsavbrudd for testhandling** – Dette feltet styrer tidsavbruddsperioden i minutter for serverforespørsler i Finance and Operation-miljøet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-408">**Test action timeout** – This field controls the time-out period, in minutes, for Finance and Operation environment server requests.</span></span> <span data-ttu-id="6ed03-409">Standardverdien (2 minutter) skal vanligvis være nok.</span><span class="sxs-lookup"><span data-stu-id="6ed03-409">Usually, the default value (2 minutes) should be enough.</span></span> <span data-ttu-id="6ed03-410">Det kan imidlertid være aktuelt å øke verdien for tregere miljøer hvis det oppstår feil i forbindelse med tidsavbrudd.</span><span class="sxs-lookup"><span data-stu-id="6ed03-410">However, for slower environments, you might want to increase the value if errors that are related to time-outs occur.</span></span>
    - <span data-ttu-id="6ed03-411">**Firmanavn** – Angi firmanavnet som skal brukes som standard Finance and Operations-firma når det opprettes Excel-parameterfiler.</span><span class="sxs-lookup"><span data-stu-id="6ed03-411">**Company name** – Enter the company name to use as your default Finance and Operations company when Excel parameter files are created.</span></span> <span data-ttu-id="6ed03-412">Du kan endre firmaet senere ved å redigere Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-412">You can change the company later by editing the Excel parameter file.</span></span>

    ![Dialogboksen Innstillinger](./media/setup_rsa_tool_62.png)

4. <span data-ttu-id="6ed03-414">Velg **Bruk** for å bruke og lagre innstillingene.</span><span class="sxs-lookup"><span data-stu-id="6ed03-414">Select **Apply** to apply and save your settings.</span></span>

    <span data-ttu-id="6ed03-415">Hvis du vil lagre de gjeldende innstillingene i en konfigurasjonsfil på datamaskinen, velger du **Lagre som**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-415">To save your current settings to a configuration file on your computer, select **Save as**.</span></span> <span data-ttu-id="6ed03-416">Du kan gjenopprette innstillingene fra en konfigurasjonsfil på datamaskinen ved å velge **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-416">To restore your settings from a configuration file on your computer, select **Open**.</span></span>

5. <span data-ttu-id="6ed03-417">Velg **Lukk** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-417">Select **Close** to close the dialog box.</span></span>

### <a name="load-and-run-test-cases"></a><span data-ttu-id="6ed03-418">Laste inn og kjøre testtilfeller</span><span class="sxs-lookup"><span data-stu-id="6ed03-418">Load and run test cases</span></span>

1. <span data-ttu-id="6ed03-419">Velg **Last inn** for å laste inn **RSAT-testplan** fra Azure DevOps-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-419">Select **Load** to load the **RSAT Test Plan** test plan from the Azure DevOps project.</span></span>

    ![Last inn-knappen](./media/setup_rsa_tool_64.png)

2. <span data-ttu-id="6ed03-421">Velg testtilfellet **Opprett et nytt produkt** fra testserien, og velg deretter **Ny \> Generer testkjøring og parameterfiler**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-421">Select the **Create a new product** test case from the test suite, and then select **New \> Generate Test Execution and Parameter files**.</span></span>

    ![Kommandoen Generer testkjøring og parameterfiler på Ny-menyen](./media/setup_rsa_tool_65.png)

    <span data-ttu-id="6ed03-423">Excel-parameterfilen opprettes i den lokale mappen du angav i RSAT-konfigurasjonen (for eksempel **C:\\Temp\\RegressionTool**).</span><span class="sxs-lookup"><span data-stu-id="6ed03-423">The Excel parameter file is created in the local folder that you specified in the RSAT configuration (for example, **C:\\Temp\\RegressionTool**).</span></span>

    ![Excel-parameterfil opprettet](./media/setup_rsa_tool_66.png)

3. <span data-ttu-id="6ed03-425">Hvis du vil lagre parameterfilene, velger du **Last opp**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-425">If you want to save the parameter files, select **Upload**.</span></span> <span data-ttu-id="6ed03-426">Testautomatiseringsfiler for alle valgte testtilfeller lastes opp til Azure DevOps for fremtidig bruk.</span><span class="sxs-lookup"><span data-stu-id="6ed03-426">Test automation files of all selected test cases are uploaded to Azure DevOps for future use.</span></span> <span data-ttu-id="6ed03-427">(Disse filene omfatter Excel-testparameterfiler.)</span><span class="sxs-lookup"><span data-stu-id="6ed03-427">(These files include Excel test parameter files.)</span></span>

    <span data-ttu-id="6ed03-428">På denne måten kan du velge **Last inn** for å laste inn parameterfilene (og automatiseringsfilene) fra testtilfellet direkte fra Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6ed03-428">In this way, you can select **Load** to load the parameter files (and automation files) from the test case directly from Azure DevOps.</span></span> <span data-ttu-id="6ed03-429">Du trenger ikke å generere parameterfilene på nytt.</span><span class="sxs-lookup"><span data-stu-id="6ed03-429">You don't have to regenerate the parameter files.</span></span> <span data-ttu-id="6ed03-430">Denne metoden blir viktig senere, når du ønsker å beholde endringene i parameterfilen og ikke vil at de skal bli overskrevet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-430">This approach will become important later, when you want to keep the modifications in the parameter file and don't want them to be overwritten.</span></span>

4. <span data-ttu-id="6ed03-431">Du kan kontrollere at automatiseringsfilene og parameterfilene er lagret i Azure DevOps, ved å gå til Azure DevOps-prosjektet, velge **Tavler \> Arbeidselementer** og velge testtilfellet **Opprett et nytt produkt**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-431">To verify that the automation files and parameter files are saved to Azure DevOps, go to the Azure DevOps project, select **Boards \> Work Items**, and select the **Create a new product** test case.</span></span> <span data-ttu-id="6ed03-432">Følgende fire filer skal vises i **Vedlegg**-fanen:</span><span class="sxs-lookup"><span data-stu-id="6ed03-432">On the **Attachments** tab, you should see four files:</span></span>

    - <span data-ttu-id="6ed03-433">**CS** – C\#-automatiseringsfil</span><span class="sxs-lookup"><span data-stu-id="6ed03-433">**.cs** – C\# automation file</span></span>
    - <span data-ttu-id="6ed03-434">**DLL** – Kompilert automatiseringsfil som en samling</span><span class="sxs-lookup"><span data-stu-id="6ed03-434">**.dll** – Compiled automation file as an assembly</span></span>
    - <span data-ttu-id="6ed03-435">**XLSX** – Excel-parameterfil</span><span class="sxs-lookup"><span data-stu-id="6ed03-435">**.xlsx** – Excel parameter file</span></span>
    - <span data-ttu-id="6ed03-436">**XML** – Opptaksfil</span><span class="sxs-lookup"><span data-stu-id="6ed03-436">**.xml** – Recording file</span></span>

    ![Filer i Vedlegg-fanen](./media/setup_rsa_tool_67.png)

5. <span data-ttu-id="6ed03-438">Velg testtilfellet som skal kjøres, og velg deretter **Kjør**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-438">Select the test case to run, and then select **Run**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ed03-439">Hvis du bruker Internet Explorer, må du kontrollere at skrivebordsoppløsningen er satt til **100 %** i **Skjerminnstillinger \> Skala og oppsett** i Windows før du kjører testtilfeller.</span><span class="sxs-lookup"><span data-stu-id="6ed03-439">Before you run test cases, if you're using Internet Explorer as the browser, make sure that your desktop resolution is set to **100%** at **Windows Display settings \> Scale and layout**.</span></span> <span data-ttu-id="6ed03-440">Hvis du ikke kan endre denne innstillingen på en virtuell maskin (VM), må du endre den på klienten (den bærbare datamaskinen) som du prøver å få tilgang til VM-en fra.</span><span class="sxs-lookup"><span data-stu-id="6ed03-440">If you can't change this setting on a virtual machine (VM), change it on the client (laptop) that you're trying to access the VM from.</span></span> <span data-ttu-id="6ed03-441">Innstillingene for oppløsning arves deretter av skjerminnstillingene for VM-en.</span><span class="sxs-lookup"><span data-stu-id="6ed03-441">The resolution settings will then be inherited by the VM display settings.</span></span>

    ![Skrivebordsoppløsningen satt til 100 %](./media/setup_rsa_tool_68.png)

6. <span data-ttu-id="6ed03-443">Hvis nettleserdriverne ikke er installert på systemet, får du en advarsel om at denne operasjonen krever driveren for \<nettlesernavn\>.</span><span class="sxs-lookup"><span data-stu-id="6ed03-443">If the browser drivers aren't installed in the system, you receive a warning message that states, "This operation requires the \<browser name\> driver.</span></span> <span data-ttu-id="6ed03-444">Deretter blir du spurt om du vil laste den ned og installere den automatisk nå.</span><span class="sxs-lookup"><span data-stu-id="6ed03-444">Do you want to automatically downloads and install it now?"</span></span> <span data-ttu-id="6ed03-445">Velg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-445">Select **Yes**.</span></span>

    ![Advarsel for Internet Explorer](./media/setup_rsa_tool_69.png)

    ![Advarsel for Chrome](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > <span data-ttu-id="6ed03-448">Hvis du bruker Chrome og får en feilmelding om at økten ikke ble opprettet fordi du bruker feil Chrome-versjon, laster du ned den nyeste Chrome-driveren fra <http://chromedriver.chromium.org/downloads> til mappen **C:\\Programfiler (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-448">If you're using Chrome as the browser and receive an error message that states that the session wasn't created because the Chrome version isn't correct, download the latest Chrome driver from <http://chromedriver.chromium.org/downloads> to the **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** folder.</span></span>

    ![Feilmelding for Chrome](./media/setup_rsa_tool_71.png)

    <span data-ttu-id="6ed03-450">Testtilfellet kjøres, og **Resultat**-feltet oppdateres.</span><span class="sxs-lookup"><span data-stu-id="6ed03-450">The test case is run, and the **Result** field is updated.</span></span>

    ![Fremdriftsindikator](./media/setup_rsa_tool_72.png)

    <span data-ttu-id="6ed03-452">Hvis du har fulgt denne opplæringen slik den er skrevet, mislykkes testtilfellet **Opprett et nytt produkt** fordi oppgaveopptaket for opprettelsen av et produkt lagret produktnavnet som en hardkodet verdi.</span><span class="sxs-lookup"><span data-stu-id="6ed03-452">If you've followed this tutorial as it's written, the **Create a new product** test case will fail, because the task recording for creating a product saved the product name as a hard-coded value.</span></span> <span data-ttu-id="6ed03-453">Hvis du kjører det samme testtilfellet på nytt, skal du få en feilmelding fordi produktet allerede finnes.</span><span class="sxs-lookup"><span data-stu-id="6ed03-453">If you rerun the same test case, you should receive an error message, because the product already exists.</span></span>

    ![Resultat-felt satt til Mislyktes](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a><span data-ttu-id="6ed03-455">Vise testresultatene</span><span class="sxs-lookup"><span data-stu-id="6ed03-455">View the test results</span></span>

1. <span data-ttu-id="6ed03-456">Dobbeltklikk på det mislykkede testtilfellet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-456">Double-click the failed test case.</span></span>

    <span data-ttu-id="6ed03-457">Du får en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="6ed03-457">You receive an error message.</span></span>

    ![Feilmelding](./media/setup_rsa_tool_73.png)

2. <span data-ttu-id="6ed03-459">Velg **Detaljer** for å vise hele feilmeldingen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-459">Select **Details** to view the whole error message.</span></span>

    ![Hele feilmeldingen](./media/setup_rsa_tool_74.png)

3. <span data-ttu-id="6ed03-461">Hvis du vil vise en detaljert versjon av feilmeldingen i Azure DevOps, velger du **Åpne i Azure DevOps**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-461">To view a detailed version of the error message in Azure DevOps, select **Open in Azure DevOps**.</span></span> <span data-ttu-id="6ed03-462">I Azure DevOps kan du vise statusen for testtilfellet og den detaljerte feilmeldingen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-462">In Azure DevOps, you can view the status of the test case and the detailed error message.</span></span>

    ![Detaljert feilmelding i Azure DevOps](./media/setup_rsa_tool_75.png)

4. <span data-ttu-id="6ed03-464">Hvis du vil vise testresultatene direkte i Azure DevOps-prosjektet, kan du gå til **Testplaner \> Testplaner \> Kjøringer**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-464">To view the test results directly in the Azure DevOps project, go to **Test Plans \> Test Plans \> Runs**.</span></span> <span data-ttu-id="6ed03-465">Dobbeltklikk på testkjøringen du vil vise flere detaljer om.</span><span class="sxs-lookup"><span data-stu-id="6ed03-465">Double-click the test run that you want to see more details for.</span></span>

    ![Liste over testkjøringer i Azure DevOps](./media/setup_rsa_tool_76.png)

5. <span data-ttu-id="6ed03-467">Fanen **Kjøringssammendrag** angir at testtilfellet mislyktes, men den faktiske feilmeldingen vises ikke.</span><span class="sxs-lookup"><span data-stu-id="6ed03-467">The **Run summary** tab indicates that the test case failed, but it doesn't provide the actual error message.</span></span> <span data-ttu-id="6ed03-468">Hvis du vil vise den detaljerte feilmeldingen, velger du **Testresultater**-fanen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-468">To view the detailed error message, select the **Test results** tab.</span></span>

    ![Fanen Kjøringssammendrag](./media/setup_rsa_tool_77.png)

    <span data-ttu-id="6ed03-470">**Testresultater**-fanen inneholder informasjon om testtilfellet sammen med resultatet og feilmeldingen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-470">The **Test results** tab provides the test case information, together with the outcome and the error message.</span></span>

    ![Testresultater-fanen](./media/setup_rsa_tool_78.png)

6. <span data-ttu-id="6ed03-472">Dobbeltklikk på den aktuelle posten for å vise den detaljerte feilmeldingen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-472">Double-click the relevant record to view the detailed error message.</span></span>

    ![Detaljert feilmelding](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > <span data-ttu-id="6ed03-474">Alle feilmeldinger også tilgjengelige lokalt i **C:\\Brukere\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-474">All error messages are also available locally in **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span></span>

7. <span data-ttu-id="6ed03-475">Du kan også eksportere resultatene av testkjøringen fra testplannivået ved å velge **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-475">You can also export the test run results from the test plan level by selecting **Export**.</span></span>

    ![Eksportere en testplan](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a><span data-ttu-id="6ed03-477">Endre Excel-parameterfilen</span><span class="sxs-lookup"><span data-stu-id="6ed03-477">Modify the Excel parameter file</span></span>

1. <span data-ttu-id="6ed03-478">Åpne RSAT.</span><span class="sxs-lookup"><span data-stu-id="6ed03-478">Open RSAT.</span></span>
2. <span data-ttu-id="6ed03-479">Velg testtilfellet, og velg deretter **Rediger** for å åpne Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-479">Select the test case, and then select **Edit** to open the Excel parameter file.</span></span>

    <span data-ttu-id="6ed03-480">I arket **EcoResProductCreate** legger du merke til at verdien i **Produktnummer**-feltet er hardkodet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-480">On the **EcoResProductCreate** sheet, notice that the value of the **Product number** field is hard-coded.</span></span> <span data-ttu-id="6ed03-481">Du må oppdatere dette feltet til et nytt produktnummer før du kjører testtilfellet på nytt.</span><span class="sxs-lookup"><span data-stu-id="6ed03-481">You must update this field to a new product number before you run the test case again.</span></span>

3. <span data-ttu-id="6ed03-482">Hvis du vil generere et unikt produktnummer for hver kjøring uten å måtte åpne Excel-parameterfilen på nytt og oppdatere produktnummeret manuelt hver gang, bruker du følgende Excel-formel.</span><span class="sxs-lookup"><span data-stu-id="6ed03-482">To generate a unique product number for each run without having to reopen the Excel parameter file and manually update the product number every time, use the following Excel formula.</span></span>

    ```
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > <span data-ttu-id="6ed03-483">I tillegg til **Generelt**-fanen inneholder Excel-parameterfilen en datafane for hver Finance and Operations-skjemaside testtilfellet går til.</span><span class="sxs-lookup"><span data-stu-id="6ed03-483">In addition to the **General** tab, the Excel parameter file contains a data tab for every Finance and Operations form page the test case visits.</span></span>

    ![Produktnummer-feltet](./media/setup_rsa_tool_81.png)

4. <span data-ttu-id="6ed03-485">Velg **Lagre**, og lukk deretter Excel-arbeidsboken.</span><span class="sxs-lookup"><span data-stu-id="6ed03-485">Select **Save**, and then close the Excel workbook.</span></span>
5. <span data-ttu-id="6ed03-486">Velg **Last opp** for å lagre Excel-parameterfilen i Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6ed03-486">Select **Upload** to save the Excel parameter file to Azure DevOps.</span></span>

    ![Melding om vellykket opplasting](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > <span data-ttu-id="6ed03-488">Hvis du vil kjøre testtilfeller i en bestemt brukerkontekst, angir du brukerens e-post-ID i **Testbruker**-feltet i **Generelt**-fanen i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-488">To run test cases in a specific user context, enter the user's email ID in the **Test User** field on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="6ed03-489">I den nyeste versjonen av RSAT er oppsettet av feltene i Excel-parameterfilen oppdatert, men konseptet er uendret.</span><span class="sxs-lookup"><span data-stu-id="6ed03-489">In the latest version of RSAT, the layout of the fields in the Excel parameter file has been updated, but the concept remains the same.</span></span>
    >
    > ![Testbruker-feltet](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a><span data-ttu-id="6ed03-491">Validere resultatene</span><span class="sxs-lookup"><span data-stu-id="6ed03-491">Validate the results</span></span>

- <span data-ttu-id="6ed03-492">Velg **Kjør** for å kjøre testtilfellet på nytt, og kontroller at testtilfellet har bestått.</span><span class="sxs-lookup"><span data-stu-id="6ed03-492">Select **Run** to rerun the test case, and verify that the test case has passed.</span></span> <span data-ttu-id="6ed03-493">Du kan vise testresultatene som beskrevet i delen [Vise testresultatene](#view-the-test-results).</span><span class="sxs-lookup"><span data-stu-id="6ed03-493">You can view the test results as described in the [View the test results](#view-the-test-results) section.</span></span>

    ![Resultat-feltet satt til Bestått](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a><span data-ttu-id="6ed03-495">Kjeding av testtilfeller</span><span class="sxs-lookup"><span data-stu-id="6ed03-495">Chaining of test cases</span></span>

<span data-ttu-id="6ed03-496">En nøkkelfunksjon i RSAT er kjeding av testtilfeller (det vil si funksjonen som gjør at en test kan sende verdier til andre tester).</span><span class="sxs-lookup"><span data-stu-id="6ed03-496">One key feature of RSAT is the chaining of test cases (that is, the capability of a test to pass values to other tests).</span></span> <span data-ttu-id="6ed03-497">Testtilfeller kjøres i henhold til den definerte rekkefølgen i Azure DevOps-testplanen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-497">Test cases are run according to their defined order in the Azure DevOps test plan.</span></span> <span data-ttu-id="6ed03-498">(Denne rekkefølgen kan også oppdateres i selve testverktøyet.) Hvis du vil sende variabler fra ett testtilfelle til et annet, er det derfor svært viktig at testene er i riktig rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="6ed03-498">(This order can also be updated in the test tool itself.) Therefore, if you want to pass variables from one test case to another, it's very important that the tests be in the correct order.</span></span>

<span data-ttu-id="6ed03-499">I denne delen skal du opprette en lagret variabel i det første testtilfellet, opprette et andre testtilfelle og sende den lagrede variabelen fra det første til det andre testtilfellet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-499">In this section, you will create a saved variable in the first test case, create a second test case, and pass the saved variable from the first test case to the second test case.</span></span> <span data-ttu-id="6ed03-500">Du skal deretter kjøre testtilfellen som et kjedet testtilfelle i RSAT.</span><span class="sxs-lookup"><span data-stu-id="6ed03-500">You will then run the test cases as a chained test case in RSAT.</span></span>

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a><span data-ttu-id="6ed03-501">Endre et eksisterende oppgaveopptak for å opprette en lagret variabel</span><span class="sxs-lookup"><span data-stu-id="6ed03-501">Modify an existing task recording to create a saved variable</span></span>

1. <span data-ttu-id="6ed03-502">Åpne Finance and Operations-klienten.</span><span class="sxs-lookup"><span data-stu-id="6ed03-502">Open the Finance and Operations client.</span></span>
2. <span data-ttu-id="6ed03-503">Velg **Innstillinger**-knappen (tannhjulsymbolet), og velg deretter **Oppgaveopptaker**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-503">Select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>
3. <span data-ttu-id="6ed03-504">Velg **Rediger opptak**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-504">Select **Edit Recording**.</span></span>

    ![Rediger opptak-knappen](./media/setup_rsa_tool_85.png)

4. <span data-ttu-id="6ed03-506">Velg **Åpne fra Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-506">Select **Open from Lifecycle Services**.</span></span>

    ![Knappen Åpne fra Lifecycle Services](./media/setup_rsa_tool_86.png)

5. <span data-ttu-id="6ed03-508">Velg **Velg Lifecycle Services-biblioteket**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-508">Select **Select the Lifecycle Services library**.</span></span>

    ![Knappen Velg Lifecycle Services-biblioteket](./media/setup_rsa_tool_87.png)

    <span data-ttu-id="6ed03-510">BPM-biblioteker lastes inn fra LCS.</span><span class="sxs-lookup"><span data-stu-id="6ed03-510">BPM libraries are loaded from LCS.</span></span>

    ![Fremdriftsindikator](./media/setup_rsa_tool_88.png)

6. <span data-ttu-id="6ed03-512">Etter at BPM-bibliotekene er lastet inn fra LCS, velger du BPM-biblioteket **RSAT** og forretningsprosessen **Opprett et nytt produkt** som oppgaveopptaket var knyttet til.</span><span class="sxs-lookup"><span data-stu-id="6ed03-512">After the BPM libraries are loaded from LCS, select the **RSAT** BPM library and the **Create a new product** business process that the task recording was associated with.</span></span> <span data-ttu-id="6ed03-513">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-513">Then select **OK**.</span></span>

    ![Velge et BPM-bibliotek og en forretningsprosess](./media/setup_rsa_tool_89.png)

7. <span data-ttu-id="6ed03-515">Navnet på det aktuelle oppgaveopptaket angis i feltet **Navn på opptak**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-515">The name of the appropriate task recording is entered in the **Recording name** field.</span></span> <span data-ttu-id="6ed03-516">Velg **Start**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-516">Select **Start**.</span></span>

    ![Navnet på oppgaveopptaket i feltet Navn på opptak](./media/setup_rsa_tool_90.png)

8. <span data-ttu-id="6ed03-518">Gå til **Behandling av produktinformasjon \> Produkter**, og velg **Ny** for å åpne siden der det opprinnelige oppgaveopptaket, **Opprett et produkt**, ble tatt opp.</span><span class="sxs-lookup"><span data-stu-id="6ed03-518">Go to **Product information management \> Products**, and select **New** to open the page where the original task recording, **Create a product**, was recorded.</span></span>
9. <span data-ttu-id="6ed03-519">Velg **Sett inn trinn**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-519">Select **Insert step**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ed03-520">Det nye trinnet settes inn **etter** trinnet du valgte i ruten.</span><span class="sxs-lookup"><span data-stu-id="6ed03-520">The new step is inserted **after** the step that you selected in the pane.</span></span>

    ![Knappen Sett inn trinn](./media/setup_rsa_tool_91.png)

10. <span data-ttu-id="6ed03-522">Høyreklikk på **Produktnummer**-feltet, og velg deretter **Oppgaveopptaker \> Kopier**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-522">Right-click the **Product number** field, and then select **Task recorder \> Copy**.</span></span>

    ![Kopier-kommandoen](./media/setup_rsa_tool_92.png)

11. <span data-ttu-id="6ed03-524">Det legges til et nytt trinn i ruten.</span><span class="sxs-lookup"><span data-stu-id="6ed03-524">A new step is added in the pane.</span></span> <span data-ttu-id="6ed03-525">Noter verdien i **Produktnummer**-feltet siden du får behov for det senere.</span><span class="sxs-lookup"><span data-stu-id="6ed03-525">Make a note of the value in the **Product number** field, because you will need it later.</span></span>

    ![Nytt trinn lagt til](./media/setup_rsa_tool_93.png)

12. <span data-ttu-id="6ed03-527">Velg **Redigeringen er fullført**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-527">Select **Done editing**.</span></span>
13. <span data-ttu-id="6ed03-528">Velg **Lagre i Lifecycle Services**, og knytt det nye oppgaveopptaket til det samme BPM-biblioteket og den samme forretningsprosessen som det opprinnelige oppgaveopptaket var knyttet til.</span><span class="sxs-lookup"><span data-stu-id="6ed03-528">Select **Save to Lifecycle Services**, and associate the new task recording with the same BPM library and business process that the original task recording was associated with.</span></span> <span data-ttu-id="6ed03-529">Hvis du vil ha mer informasjon, kan du se delen [Opprette et oppgaveopptak og lagre det i BPM-biblioteket](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="6ed03-529">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>
14. <span data-ttu-id="6ed03-530">Gå til BPM-biblioteket, og velg **Synkroniser testtilfeller** for å skrive over oppgaveopptaket som er knyttet til testtilfellet i Azure DevOps, slik det er beskrevet i delen [Teste synkroniseringen fra BPM til Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="6ed03-530">Go to the BPM library, and select **Sync testcases** to overwrite the task recording that is attached to the test case in Azure DevOps, as described in the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>
15. <span data-ttu-id="6ed03-531">Åpne RSAT, og velg **Last inn** for å laste inn alle testtilfellene i testserien på nytt.</span><span class="sxs-lookup"><span data-stu-id="6ed03-531">Open RSAT, and select **Load** to reload all the test cases in the test suite.</span></span> <span data-ttu-id="6ed03-532">Du må generere automatiserings- og parameterfilene for det aktuelle testtilfellet på nytt ved å velge testtilfellet og deretter **Ny \> Generer testkjøring og parameterfiler**, slik det er beskrevet i delen [Laste inn og kjøre testtilfeller](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="6ed03-532">You must regenerate the automation and parameter files for the appropriate test case by selecting the test case and then selecting **New \> Generate Test Execution and Parameter files**, as described in the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ed03-533">Hvis du lot Excel-parameterfilen være åpen, mislykkes ny generering.</span><span class="sxs-lookup"><span data-stu-id="6ed03-533">If the Excel parameter file was left open, regeneration will fail.</span></span> <span data-ttu-id="6ed03-534">Derfor må du kontrollere at Excel-parameterfilen for testtilfellet lukkes før du genererer den nye Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-534">Therefore, make sure that the Excel parameter file for the test case is closed before you generate the new Excel parameter file.</span></span>

16. <span data-ttu-id="6ed03-535">Velg **Rediger** for å åpne den nye Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-535">Select **Edit** to open the new Excel parameter file.</span></span> <span data-ttu-id="6ed03-536">En ny **Lagret variabel**-oppføring vises på linje 9.</span><span class="sxs-lookup"><span data-stu-id="6ed03-536">You will see a new **Saved variable** entry on line 9.</span></span> <span data-ttu-id="6ed03-537">Denne variabelen, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, lagres i XML-filen for oppgaveopptaket og kan brukes i senere tester.</span><span class="sxs-lookup"><span data-stu-id="6ed03-537">This variable, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, is saved in the task recording's XML file and can be used in subsequent tests.</span></span>

    ![Lagret variabel-oppføringen](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a><span data-ttu-id="6ed03-539">Opprette et nytt testtilfelle</span><span class="sxs-lookup"><span data-stu-id="6ed03-539">Create a new test case</span></span>

1. <span data-ttu-id="6ed03-540">Gå til BPM-biblioteket **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-540">Go to the **RSAT** BPM library.</span></span>
2. <span data-ttu-id="6ed03-541">Velg prosessen **Eksempel på støtteforretningsprosess**, og velg deretter **Redigeringsmodus** til høyre.</span><span class="sxs-lookup"><span data-stu-id="6ed03-541">Select the **Sample Support Business Process** process, and then, on the right, select **Edit mode**.</span></span>
3. <span data-ttu-id="6ed03-542">Endre verdien i **Navn**-feltet og **Beskrivelse**-feltet til **Frigi produkt**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-542">Change the value of both the **Name** field and the **Description** field to **Release a product**.</span></span> <span data-ttu-id="6ed03-543">Velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-543">Then select **Save**.</span></span>

    ![Navnet og beskrivelsen er endret til Frigi produkt](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a><span data-ttu-id="6ed03-545">Opprette et nytt oppgaveopptak som har en valideringsfunksjon</span><span class="sxs-lookup"><span data-stu-id="6ed03-545">Create a new task recording that has a Validate function</span></span>

- <span data-ttu-id="6ed03-546">Opprett et oppgaveopptak for å frigi produktet som ble opprettet tidligere, til den juridiske enheten USRT.</span><span class="sxs-lookup"><span data-stu-id="6ed03-546">Create a task recording to release the product that was created earlier to the USRT legal entity.</span></span> <span data-ttu-id="6ed03-547">Hvis du vil ha mer informasjon, kan du se delen [Opprette et oppgaveopptak og lagre det i BPM-biblioteket](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="6ed03-547">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ed03-548">Når det gjelder kjedede testtilfeller, anbefaler vi alltid at du finner eller filtrerer for posten du trenger, ved å *skrive inn verdien for feltet manuelt*.</span><span class="sxs-lookup"><span data-stu-id="6ed03-548">For chained test cases, we always recommend that you find or filter for the record that you require by *manually typing the value of the field*.</span></span> <span data-ttu-id="6ed03-549">På den måten kan verktøyet fastsette posten som handlingen må utføres mot, i det etterfølgende testtilfellet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-549">In that way, the tool can determine the record that the action must be taken against in the subsequent test case.</span></span>

    ![Nytt oppgaveopptak som har en valideringsfunksjon](./media/setup_rsa_tool_96.png)

    <span data-ttu-id="6ed03-551">Som den foregående illustrasjonen viser, validerer du verdien i **Produktnummer**-feltet etter at produktet er funnet ved hjelp av hurtigfilteret, men før du velger **Frigi produkter**, for å kontrollere at produkt-ID-en er produkt-ID-en som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="6ed03-551">As the preceding illustration shows, after the product is found by using the Quick Filter, but before you select **Release products**, you validate the value of the **Product number** field to make sure that the product ID is the product ID that was created earlier.</span></span> <span data-ttu-id="6ed03-552">Du kan validere verdien ved å høyreklikke på **Produktnummer**-feltet og deretter velge **Oppgaveopptaker \> Valider \> Gjeldende verdi**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-552">To validate the value, right-click the **Product number** field, and then select **Task recorder \> Validate \> Current Value**.</span></span>

    ![Validere gjeldende verdi](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a><span data-ttu-id="6ed03-554">Lagre oppgaveopptaket i BPM</span><span class="sxs-lookup"><span data-stu-id="6ed03-554">Save the task recording to BPM</span></span>

1. <span data-ttu-id="6ed03-555">Etter at oppgaveopptaket er fullført, velger du **Lagre i Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-555">After the task recording is completed, select **Save to Lifecycle Services**.</span></span>

    ![Lagringsalternativer](./media/setup_rsa_tool_98.png)

2. <span data-ttu-id="6ed03-557">Bibliotekinformasjon lastes inn fra LCS.</span><span class="sxs-lookup"><span data-stu-id="6ed03-557">Library information is loaded from LCS.</span></span>

    ![Fremdriftsindikator](./media/setup_rsa_tool_99.png)

3. <span data-ttu-id="6ed03-559">Velg BPM-biblioteket som oppgaveopptaket skal knyttes til.</span><span class="sxs-lookup"><span data-stu-id="6ed03-559">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="6ed03-560">For denne opplæringen velger du BPM-biblioteket **RSAT** som ble opprettet tidligere, og forretningsprosessen **Frigi produkt** under det.</span><span class="sxs-lookup"><span data-stu-id="6ed03-560">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Release a product** business process under it.</span></span> <span data-ttu-id="6ed03-561">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-561">Then select **OK**.</span></span>

#### <a name="sync-bpm-to-azure-devops"></a><span data-ttu-id="6ed03-562">Synkronisere BPM med Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="6ed03-562">Sync BPM to Azure DevOps</span></span>

1. <span data-ttu-id="6ed03-563">Gå til BPM-biblioteket, og åpne **RSAT**-biblioteket.</span><span class="sxs-lookup"><span data-stu-id="6ed03-563">Go to the BPM library, and open the **RSAT** library.</span></span>
2. <span data-ttu-id="6ed03-564">Velg **VSTS-synkronisering** og deretter **Synkroniser testtilfeller**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-564">Select **VSTS sync** and then **Sync test cases**.</span></span> <span data-ttu-id="6ed03-565">Hvis du vil ha mer informasjon, kan du se delen [Teste synkroniseringen fra BPM til Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="6ed03-565">For more information, see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>

    <span data-ttu-id="6ed03-566">Etter at synkroniseringen er fullført, vises det nye arbeidselementet og det tilsvarende testtilfellet for forretningsprosessen **Frigi produkt** i Azure DevOps i **Tavler \> Arbeidselementer**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-566">After the synchronization is completed, the new work item and the corresponding test case for the **Release a product** business process appear in Azure DevOps at **Boards \> Work Items**.</span></span>

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a><span data-ttu-id="6ed03-567">Legge til det nye testtilfellet i den eksisterende testserien</span><span class="sxs-lookup"><span data-stu-id="6ed03-567">Add the new test case to the existing test suite</span></span>

1. <span data-ttu-id="6ed03-568">Gå til **Testplaner \> Testplaner**, og velg planen **RSAT-testplan**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-568">Go to **Test plans \> Test plans**, and select the **RSAT Test Plan** plan.</span></span>
2. <span data-ttu-id="6ed03-569">Velg **Legg til eksisterende**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-569">Select **Add existing**.</span></span>
3. <span data-ttu-id="6ed03-570">Velg **Kjør spørring** på siden **Legg til testtilfeller i serie**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-570">On the **Add test cases to suite** page, select **Run query**.</span></span>
4. <span data-ttu-id="6ed03-571">Velg det nye testtilfellet som ble opprettet for **Frigi produkt**, og velg deretter **Legg til testtilfeller** i nedre høyre hjørne på siden (denne knappen vises ikke i illustrasjonen nedenfor).</span><span class="sxs-lookup"><span data-stu-id="6ed03-571">Select the new test case that was created for **Release a product**, and then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Siden Legg til testtilfeller i serie](./media/setup_rsa_tool_100.png)

    <span data-ttu-id="6ed03-573">Testserien har nå to testtilfeller.</span><span class="sxs-lookup"><span data-stu-id="6ed03-573">The test suite now has two test cases.</span></span>

    ![To testtilfeller i testserien](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a><span data-ttu-id="6ed03-575">Laste inn testtilfeller i RSAT</span><span class="sxs-lookup"><span data-stu-id="6ed03-575">Load test cases into RSAT</span></span>

1. <span data-ttu-id="6ed03-576">Åpne RSAT, og velg **Last inn**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-576">Open RSAT, and select **Load**.</span></span>
2. <span data-ttu-id="6ed03-577">Testtilfellene lastes inn, og du får en advarsel om at denne handlingen skriver over Excel-testdatafiler, og at lokale endringer går tapt.</span><span class="sxs-lookup"><span data-stu-id="6ed03-577">The test cases are loaded, and you receive a warning that states, "This action will overwrite Excel test data files, local changes will be lost.</span></span> <span data-ttu-id="6ed03-578">Du blir også spurt om du vil fortsette.</span><span class="sxs-lookup"><span data-stu-id="6ed03-578">Do you want to proceed?"</span></span> <span data-ttu-id="6ed03-579">Velg **Ja** for å oppdatere Excel-parameterfiler i det lokale systemet, men ikke Excel-parameterfilene som ble lastet opp til Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6ed03-579">Select **Yes** to update the Excel parameter files in the local system but not the Excel parameter files that were uploaded to Azure DevOps.</span></span>

    ![Advarselsmelding](./media/setup_rsa_tool_102.png)

    <span data-ttu-id="6ed03-581">Begge testtilfellene lastes inn, sammen med Excel-parameterfilen for det første testtilfellet.</span><span class="sxs-lookup"><span data-stu-id="6ed03-581">Both the test cases are loaded, together with the Excel parameter file for the first test case.</span></span> <span data-ttu-id="6ed03-582">Siden du valgte **Last opp** i den siste kjøringen, hentes parameterfilene fra Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6ed03-582">Because you selected **Upload** in the last run, the parameter files are pulled from Azure DevOps.</span></span>

    ![Testtilfeller lastet inn](./media/setup_rsa_tool_103.png)

3. <span data-ttu-id="6ed03-584">Velg bare det andre testtilfellet, og velg deretter **Ny \> Generer testkjøring og parameterfiler**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-584">Select only the second test case, and then select **New \> Generate test execution and parameter files**.</span></span>

#### <a name="edit-the-excel-parameter-file"></a><span data-ttu-id="6ed03-585">Redigere Excel-parameterfilen</span><span class="sxs-lookup"><span data-stu-id="6ed03-585">Edit the Excel parameter file</span></span>

1. <span data-ttu-id="6ed03-586">Velg bare det andre testtilfellet, og velg deretter **Rediger** for å åpne den tilsvarende Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-586">Select only the second test case, and then select **Edit** to open the corresponding Excel parameter file.</span></span>
2. <span data-ttu-id="6ed03-587">Kopier den lagrede variabelen **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** (se delen [Endre et eksisterende oppgaveopptak for å opprette en lagret variabel](#modify-an-existing-task-recording-to-create-a-saved-variable)) fra det første testtilfellet til alle feltene der produktnummeret brukes.</span><span class="sxs-lookup"><span data-stu-id="6ed03-587">Copy the **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** saved variable (see the [Modify an existing task recording to create a saved variable](#modify-an-existing-task-recording-to-create-a-saved-variable) section) from the first test case into all the fields where the product number is used.</span></span> <span data-ttu-id="6ed03-588">I dette tilfellet kopierer du variabelen til feltene **Produktnummer** og **Valider produktnummer** i arket **EcoResProductListPage**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-588">In this case, you copy the variable into the **Product number** and **Validate Product number** fields on the **EcoResProductListPage** sheet.</span></span>

    ![Feltene Produktnummer og Valider produktnummer](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > <span data-ttu-id="6ed03-590">Variabler kan bare sendes mellom tester i den samme testkjøringen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-590">Variables can be passed between tests only during the same test run.</span></span> <span data-ttu-id="6ed03-591">Navnene på variablene må samsvare nøyaktig.</span><span class="sxs-lookup"><span data-stu-id="6ed03-591">The names of the variables must match exactly.</span></span>

3. <span data-ttu-id="6ed03-592">Velg **Lagre**, og lukk deretter Excel-arbeidsboken.</span><span class="sxs-lookup"><span data-stu-id="6ed03-592">Select **Save**, and then close the Excel workbook.</span></span>
4. <span data-ttu-id="6ed03-593">Velg **Last opp** for å lagre endringene du har gjort i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="6ed03-593">Select **Upload** to save the changes that you made to the Excel parameter file.</span></span>

#### <a name="run-the-chained-test-cases"></a><span data-ttu-id="6ed03-594">Kjøre kjedede testtilfeller</span><span class="sxs-lookup"><span data-stu-id="6ed03-594">Run the chained test cases</span></span>

1. <span data-ttu-id="6ed03-595">Velg begge testtilfellene, og velg deretter **Kjør**.</span><span class="sxs-lookup"><span data-stu-id="6ed03-595">Select both the test cases, and then select **Run**.</span></span>
2. <span data-ttu-id="6ed03-596">Kontroller at begge testtilfellene har bestått.</span><span class="sxs-lookup"><span data-stu-id="6ed03-596">Verify that both test cases have passed.</span></span>

    ![Resultat-feltet satt til Bestått for begge testtilfeller](./media/setup_rsa_tool_105.png)
