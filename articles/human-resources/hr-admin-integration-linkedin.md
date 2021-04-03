---
title: Integrere med LinkedIn Talent Hub
description: Dette emnet forklarer hvordan du kan setter opp integrasjon mellom Microsoft Dynamics 365 Human Resources LinkedIn Talent Hub.
author: jaredha
manager: tfehr
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2a017d67177bcbee86abf920cf8d83f37312c5eb
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465204"
---
# <a name="integrate-with-linkedin-talent-hub"></a><span data-ttu-id="1c97f-103">Integrere med LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="1c97f-103">Integrate with LinkedIn Talent Hub</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="1c97f-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) er en is ATS-plattform (programsporingssystem).</span><span class="sxs-lookup"><span data-stu-id="1c97f-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) is an applicant tracking system (ATS) platform.</span></span> <span data-ttu-id="1c97f-105">Den gjør det mulig å finne, administrere og ansette alle ansatte på ett sted.</span><span class="sxs-lookup"><span data-stu-id="1c97f-105">It lets you source, manage, and hire employees all in one place.</span></span> <span data-ttu-id="1c97f-106">Ved å integrere Microsoft Dynamics 365 Human Resources med LinkedIn Talent Hub, kan du enkelt opprette ansattposter i Human Resources for søkere som har blitt ansatt for en stilling.</span><span class="sxs-lookup"><span data-stu-id="1c97f-106">By integrating Microsoft Dynamics 365 Human Resources with LinkedIn Talent Hub, you can easily create employee records in Human Resources for applicants who have been hired for a position.</span></span>

## <a name="setup"></a><span data-ttu-id="1c97f-107">Installasjon</span><span class="sxs-lookup"><span data-stu-id="1c97f-107">Setup</span></span>

<span data-ttu-id="1c97f-108">En systemadministrator må fullføre installasjonsoppgavene for å aktivere integrering med LinkedIn Talent Hub.</span><span class="sxs-lookup"><span data-stu-id="1c97f-108">A system administrator must complete setup tasks to enable integration with LinkedIn Talent Hub.</span></span> <span data-ttu-id="1c97f-109">I Power Apps-miljøet må du først konfigurere en bruker- og en sikkerhetsrolle for å gi LinkedIn Talent Hub de riktige tillatelsene til å skrive data i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1c97f-109">First, in the Power Apps environment, you must set up a user and security role to grant LinkedIn Talent Hub the appropriate permissions to write data into Human Resources.</span></span>

### <a name="link-your-environment-to-linkedin-talent-hub"></a><span data-ttu-id="1c97f-110">Koble miljøet til LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="1c97f-110">Link your environment to LinkedIn Talent Hub</span></span>

1. <span data-ttu-id="1c97f-111">Åpne [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span><span class="sxs-lookup"><span data-stu-id="1c97f-111">Open [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span></span>

2. <span data-ttu-id="1c97f-112">Velg **Produktinnstillinger** på brukerrullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="1c97f-112">On the user drop-down menu, select **Product Settings**.</span></span>

3. <span data-ttu-id="1c97f-113">I den venstre navigasjonsruten i delen **Avansert** velger du **Integreringer**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-113">In the left navigation pane, in the **Advanced** section, select **Integrations**.</span></span>

4. <span data-ttu-id="1c97f-114">Velg **Autorisere** for Microsoft Dynamics 365 Human Resources-integreringen.</span><span class="sxs-lookup"><span data-stu-id="1c97f-114">Select **Authorize** for the Microsoft Dynamics 365 Human Resources integration.</span></span>

5. <span data-ttu-id="1c97f-115">På **Dynamics 365 Human Resources**-siden velger du miljøet du vil koble LinkedIn Talent Hub til, og deretter velger du **Kobling**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-115">On the **Dynamics 365 Human Resources** page, select the environment to link LinkedIn Talent Hub to, and then select **Link**.</span></span>

    ![LinkedIn Talent Hub-pålasting](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > <span data-ttu-id="1c97f-117">Du kan bare koble til miljøer der brukerkontoen har administratortilgang til både Human Resources-miljøet og det tilknyttede Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="1c97f-117">You can link only to environments where your user account has administrator access to both the Human Resources environment and the associated Power Apps environment.</span></span> <span data-ttu-id="1c97f-118">Hvis det ikke vises noen miljøer Human Resources-koblingssiden, må du kontrollere at du har lisensierte Human Resources-miljøer på leieren, og at brukeren du logget deg på koblingssiden som har administratortilgang til både Human Resources-administrasjonsmiljøet og Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="1c97f-118">If no environments are listed on the Human Resources link page, make sure that you have licensed Human Resources environments on the tenant, and that the user that you signed in to the link page as has administrator permissions to both the Human Resources environment and the Power Apps environment.</span></span>

### <a name="create-a-power-apps-security-role"></a><span data-ttu-id="1c97f-119">Opprette en Power Apps-sikkerhetsrolle</span><span class="sxs-lookup"><span data-stu-id="1c97f-119">Create a Power Apps security role</span></span>

1. <span data-ttu-id="1c97f-120">Åpne [Administrasjonssenter for Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="1c97f-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="1c97f-121">I **Miljøer**-listen velger du miljøet som er knyttet til Human Resources-miljøet du vil koble forekomsten av LinkedIn Talent Hub til.</span><span class="sxs-lookup"><span data-stu-id="1c97f-121">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="1c97f-122">Velg **Innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-122">Select **Settings**.</span></span>

4. <span data-ttu-id="1c97f-123">Utvid noden **Brukere + tillatelser**, og velg **Sikkerhetsroller**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-123">Expand the **Users + Permissions** node, and select **Security Roles**.</span></span>

5. <span data-ttu-id="1c97f-124">På verktøylinjen på **Sikkerhetsroller**-siden velger du **Ny rolle**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-124">On the **Security Roles** page, on the toolbar, select **New role**.</span></span>

6. <span data-ttu-id="1c97f-125">I kategorien **Detaljer** angir du et navn på rollen, for eksempel **LinkedIn Talent Hub HRIS-integrering**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-125">On the **Details** tab, enter a name for the role, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>

7. <span data-ttu-id="1c97f-126">I kategorien **Tilpassing** velger du **Lese**-tilgang på organisasjonsnivå for følgende enheter:</span><span class="sxs-lookup"><span data-stu-id="1c97f-126">On the **Customization** tab, select organization-level **Read** permission for the following entities:</span></span>

    - <span data-ttu-id="1c97f-127">Entity</span><span class="sxs-lookup"><span data-stu-id="1c97f-127">Entity</span></span>
    - <span data-ttu-id="1c97f-128">Felt</span><span class="sxs-lookup"><span data-stu-id="1c97f-128">Field</span></span>
    - <span data-ttu-id="1c97f-129">Relasjon</span><span class="sxs-lookup"><span data-stu-id="1c97f-129">Relationship</span></span>

8. <span data-ttu-id="1c97f-130">Lagre og lukk sikkerhetsrollen.</span><span class="sxs-lookup"><span data-stu-id="1c97f-130">Save and close the security role.</span></span>

### <a name="create-a-power-apps-application-user"></a><span data-ttu-id="1c97f-131">Opprette en Power Apps-programbruker</span><span class="sxs-lookup"><span data-stu-id="1c97f-131">Create a Power Apps application user</span></span>

<span data-ttu-id="1c97f-132">Det må opprettes en programbruker for LinkedIn Talent Hub-adapteren for å gi tillatelse til at adapteren kan skrive kandidatposter til Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="1c97f-132">An application user must be created for the LinkedIn Talent Hub adapter to grant permissions to the adapter to write candidate records into the Power Apps environment.</span></span>

1. <span data-ttu-id="1c97f-133">Åpne [Administrasjonssenter for Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="1c97f-133">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="1c97f-134">I **Miljøer**-listen velger du miljøet som er knyttet til Human Resources-miljøet du vil koble forekomsten av LinkedIn Talent Hub til.</span><span class="sxs-lookup"><span data-stu-id="1c97f-134">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="1c97f-135">Velg **Innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-135">Select **Settings**.</span></span>

4. <span data-ttu-id="1c97f-136">Utvid noden **Brukere + tillatelser**, og velg **Brukere**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-136">Expand the **Users + Permissions** node, and select **Users**.</span></span>

5. <span data-ttu-id="1c97f-137">Velg **Behandle brukere i Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-137">Select **Manage users in Dynamics 365**.</span></span>

6. <span data-ttu-id="1c97f-138">Bruk rullegardinmenyen over listen til å endre visningen fra standardvisningen **Aktiverte brukere** til **Programbrukere**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-138">Use the drop-down menu above the list to change the view from the default **Enabled Users** view to **Application Users**.</span></span>

    ![Programbrukere-visningen](./media/hr-admin-integration-power-apps-application-users.jpg)

7. <span data-ttu-id="1c97f-140">Klikk **Ny** på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="1c97f-140">On the toolbar, select **New**.</span></span>

8. <span data-ttu-id="1c97f-141">Følg denne fremgangsmåten på siden **Ny bruker**:</span><span class="sxs-lookup"><span data-stu-id="1c97f-141">On the **New user** page, follow these steps:</span></span>

    1. <span data-ttu-id="1c97f-142">Endre verdien for feltet **Brukertype** til **Programbruker**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-142">Change the value of the **User type** field to **Application User**.</span></span>
    2. <span data-ttu-id="1c97f-143">Sett **Brukernavn**-feltet til **Dynamics365 HR LinkedIn HRIS-integrering**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-143">Set the **User Name** field to **Dynamics365 HR LinkedIn HRIS Integration**.</span></span>
    3. <span data-ttu-id="1c97f-144">Angi **Program-ID**-feltet til **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-144">Set the **Application ID** field to **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    4. <span data-ttu-id="1c97f-145">Angi en verdi i feltene **Navn**, **Etternavn** og **Primær e-post**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-145">Enter any value in the **First Name**, **Last Name**, and **Primary Email** fields.</span></span>
    5. <span data-ttu-id="1c97f-146">Velg **Lagre \& lukk** på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="1c97f-146">On the toolbar, select **Save \& Close**.</span></span>

### <a name="assign-a-security-role-to-the-new-user"></a><span data-ttu-id="1c97f-147">Tilordne en sikkerhetsrolle til den nye brukeren</span><span class="sxs-lookup"><span data-stu-id="1c97f-147">Assign a security role to the new user</span></span>

<span data-ttu-id="1c97f-148">Når du har lagret og lukket den nye programbrukeren i den forrige delen, kommer du tilbake til **Brukerliste**-siden.</span><span class="sxs-lookup"><span data-stu-id="1c97f-148">After you save and close the new application user in the previous section, you're returned to the **Users list** page.</span></span>

1. <span data-ttu-id="1c97f-149">På **Brukerlisten**-siden endrer du visningen til **Programbrukere**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-149">On the **Users list** page, change the view to **Application Users**.</span></span>

2. <span data-ttu-id="1c97f-150">Velg programbrukeren du opprettet i den forrige delen.</span><span class="sxs-lookup"><span data-stu-id="1c97f-150">Select the application user that you created in the previous section.</span></span>

3. <span data-ttu-id="1c97f-151">Velg **Administrer roller** på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="1c97f-151">On the toolbar, select **Manage Roles**.</span></span>

4. <span data-ttu-id="1c97f-152">Velg sikkerhetsrollen du opprettet tidligere for integreringen.</span><span class="sxs-lookup"><span data-stu-id="1c97f-152">Select the security role that you created earlier for the integration.</span></span>

5. <span data-ttu-id="1c97f-153">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-153">Select **OK**.</span></span>

### <a name="add-an-azure-active-directory-app-in-human-resources"></a><span data-ttu-id="1c97f-154">Legge til en Azure Active Directory-app i Human Resources</span><span class="sxs-lookup"><span data-stu-id="1c97f-154">Add an Azure Active Directory app in Human Resources</span></span>

1. <span data-ttu-id="1c97f-155">I Dynamics 365 Human Resources åpner du siden **Azure Active Directory-programmer**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-155">In Dynamics 365 Human Resources, open the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="1c97f-156">Legg til en ny post i listen, og angi følgende felt:</span><span class="sxs-lookup"><span data-stu-id="1c97f-156">Add a new record to the list, and set the following fields:</span></span>

    - <span data-ttu-id="1c97f-157">**Klient-ID**: Angi **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-157">**Client ID**: Enter **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    - <span data-ttu-id="1c97f-158">**Navn**: Skriv inn navnet på Power Apps-sikkerhetsrollen du opprettet tidligere, for eksempel **LinkedIn Talent Hub HRIS-integrering**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-158">**Name**: Enter the name of the Power Apps security role that you created earlier, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>
    - <span data-ttu-id="1c97f-159">**Bruker-ID**: Velg en bruker som har tillatelse til å skrive data i Personaladministrasjon.</span><span class="sxs-lookup"><span data-stu-id="1c97f-159">**User ID**: Select a user who has permissions to write data in Personnel Management.</span></span>

### <a name="create-the-table-in-dataverse"></a><span data-ttu-id="1c97f-160">Opprette tabellen i Dataverse</span><span class="sxs-lookup"><span data-stu-id="1c97f-160">Create the table in Dataverse</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c97f-161">Integreringen med LinkedIn Talent Hub er avhengig av virtuelle tabeller i Dataverse for Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1c97f-161">The integration with LinkedIn Talent Hub depends on virtual tables in Dataverse for Human Resources.</span></span> <span data-ttu-id="1c97f-162">Som en forutsetning for dette trinnet i oppsettet, må du konfigurere virtuelle tabeller.</span><span class="sxs-lookup"><span data-stu-id="1c97f-162">As a prerequisite for this step in the setup, you must configure virtual tables.</span></span> <span data-ttu-id="1c97f-163">Hvis du vil ha informasjon om hvordan du konfigurerer virtuelle tabeller, se [Konfigurere virtuelle tabeller for Dataverse](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="1c97f-163">For information about how to configure virtual tables, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

1. <span data-ttu-id="1c97f-164">I Human Resources åpner du siden **Dataverse-integrering**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-164">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="1c97f-165">Velg kategorien **Virtuelle tabeller**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-165">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="1c97f-166">Filtrer enhetslisten etter enhetsetikett for å finne **LinkedIn-eksporterte kandidater**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-166">Filter the entity list by entity label to find **LinkedIn exported candidate**.</span></span>

4. <span data-ttu-id="1c97f-167">Velg enheten, og velg deretter **Generer/oppdater**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-167">Select the entity, and then select **Generate/refresh**.</span></span>

## <a name="exporting-candidate-records"></a><span data-ttu-id="1c97f-168">Eksportere kandidatposter</span><span class="sxs-lookup"><span data-stu-id="1c97f-168">Exporting candidate records</span></span>

<span data-ttu-id="1c97f-169">Når oppsettet er fullført, kan rekrutteringspersoner og personaleksperter bruke funksjonen **Eksporter til HRIS** i LinkedIn Talent Hub til å eksportere kandidatposter for ansatte fra LinkedIn Talent Hub til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1c97f-169">After the setup is completed, recruiters and human resources (HR) professionals can use the **Export to HRIS** function in LinkedIn Talent Hub to export hired candidate records from LinkedIn Talent Hub to Human Resources.</span></span>

### <a name="export-records-from-linkedin-talent-hub"></a><span data-ttu-id="1c97f-170">Eksportere poster fra LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="1c97f-170">Export records from LinkedIn Talent Hub</span></span>

<span data-ttu-id="1c97f-171">Når en kandidat har gått gjennom rekrutteringsprosessen og har blitt ansatt, kan du eksportere kandidatposten fra LinkedIn Talent Hub til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1c97f-171">After a candidate has moved through the recruiting process and has been hired, you can export the candidate record from LinkedIn Talent Hub to Human Resources.</span></span>

1. <span data-ttu-id="1c97f-172">I LinkedIn Talent Hub åpner du prosjektet som du ansatte den nye medarbeideren for.</span><span class="sxs-lookup"><span data-stu-id="1c97f-172">In LinkedIn Talent Hub, open the project that you hired the new employee for.</span></span>

2. <span data-ttu-id="1c97f-173">Velg en kandidatpost.</span><span class="sxs-lookup"><span data-stu-id="1c97f-173">Select a candidate record.</span></span>

3. <span data-ttu-id="1c97f-174">Velg **Endre stadium**, og velg deretter **Ansatt**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-174">Select **Change stage**, and then select **Hired**.</span></span>

4. <span data-ttu-id="1c97f-175">På ellipsemenyen (**...**) for kandidaten velger du **Eksporter til HRIS**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-175">On the ellipsis menu (**...**) for the candidate, select **Export to HRIS**.</span></span>

5. <span data-ttu-id="1c97f-176">Skriv inn informasjonen som må eksporteres, i ruten **Eksporter til HRIS**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-176">In the **Export to HRIS** pane, enter the information that must be exported:</span></span>

    - <span data-ttu-id="1c97f-177">I feltet **HRIS-leverandør** velger du **Microsoft Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="1c97f-177">In the **HRIS provider** field, select **Microsoft Dynamics 365 Human Resources**.</span></span>
    - <span data-ttu-id="1c97f-178">Velg en verdi for den nyansatte i **Startdato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1c97f-178">In the **Start date** field, select a value for the new employee.</span></span>
    - <span data-ttu-id="1c97f-179">I **Stilling**-feltet angir du en stillingstittel for den nye ansattes stilling.</span><span class="sxs-lookup"><span data-stu-id="1c97f-179">In the **Job title** field, enter a job title for the new employee's job.</span></span>
    - <span data-ttu-id="1c97f-180">Angi lokasjonen der den ansatte skal være basert, i **Lokasjon**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1c97f-180">In the **Location** field, enter the location where the employee will be based.</span></span>
    - <span data-ttu-id="1c97f-181">Angi eller kontroller den ansattes e-postadresse.</span><span class="sxs-lookup"><span data-stu-id="1c97f-181">Enter or verify the employee's email address.</span></span>

![Eksporter til HRIS-ruten i LinkedIn Talent Hub](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a><span data-ttu-id="1c97f-183">Fullføre pålasting i Human Resources</span><span class="sxs-lookup"><span data-stu-id="1c97f-183">Complete onboarding in Human Resources</span></span>

<span data-ttu-id="1c97f-184">Kandidatposter som eksporteres fra LinkedIn Talent Hub til Personal, vises i delen **Kandidater som skal ansette** på **Personaladministrasjon**-siden.</span><span class="sxs-lookup"><span data-stu-id="1c97f-184">Candidate records that are exported from LinkedIn Talent Hub to Human Resources appear in the **Candidates to hire** section of the **Personnel management** page.</span></span>

1. <span data-ttu-id="1c97f-185">I Human Resources åpner du **Personaladministrasjon**-siden.</span><span class="sxs-lookup"><span data-stu-id="1c97f-185">In Human Resources, open the **Personnel management** page.</span></span>

2. <span data-ttu-id="1c97f-186">I delen **Kandidater som skal ansettes** velger du **Ansett** for den valgte kandidaten.</span><span class="sxs-lookup"><span data-stu-id="1c97f-186">In the **Candidates to hire** section, select **Hire** for the selected candidate.</span></span>

3. <span data-ttu-id="1c97f-187">I dialogboksen **Ansett en ny arbeider** kontrollerer du posten og legger til eventuell nødvendig informasjon.</span><span class="sxs-lookup"><span data-stu-id="1c97f-187">In the **Hire new worker** dialog box, review the record, and add any required information.</span></span> <span data-ttu-id="1c97f-188">Du kan også velge stillingsnummeret som kandidaten er ansatt for.</span><span class="sxs-lookup"><span data-stu-id="1c97f-188">You can also select the position number that the candidate has been hired for.</span></span>

<span data-ttu-id="1c97f-189">Når den nødvendige informasjonen er angitt, kan du fortsette med standardprosessene for å opprette ansattposter og sette pålaste ansatte.</span><span class="sxs-lookup"><span data-stu-id="1c97f-189">After the required information has been entered, you can continue with your standard processes for creating employee records and onboarding employees.</span></span>

<span data-ttu-id="1c97f-190">Følgende detaljer blir importert og inkludert i den nye ansattposten:</span><span class="sxs-lookup"><span data-stu-id="1c97f-190">The following details are imported and included on the new employee record:</span></span>

- <span data-ttu-id="1c97f-191">Fornavn</span><span class="sxs-lookup"><span data-stu-id="1c97f-191">First name</span></span>
- <span data-ttu-id="1c97f-192">Etternavn</span><span class="sxs-lookup"><span data-stu-id="1c97f-192">Last name</span></span>
- <span data-ttu-id="1c97f-193">Startdato for ansettelse</span><span class="sxs-lookup"><span data-stu-id="1c97f-193">Employment start date</span></span>
- <span data-ttu-id="1c97f-194">E-postadresse</span><span class="sxs-lookup"><span data-stu-id="1c97f-194">Email address</span></span>
- <span data-ttu-id="1c97f-195">Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="1c97f-195">Phone number</span></span>

## <a name="see-also"></a><span data-ttu-id="1c97f-196">Se også</span><span class="sxs-lookup"><span data-stu-id="1c97f-196">See also</span></span>

[<span data-ttu-id="1c97f-197">Konfigurere virtuelle Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="1c97f-197">Configure Dataverse virtual tables</span></span>](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="1c97f-198">Hva er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="1c97f-198">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]