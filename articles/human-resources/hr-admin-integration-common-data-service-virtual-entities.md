---
title: Konfigurere virtuelle Dataverse-tabeller
description: Dette emnet beskriver hvordan du konfigurerer virtuelle tabeller for Dynamics 365 Human Resources. Generer og oppdater eksisterende virtuelle tabeller og analyser genererte og tilgjengelige tabeller.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d8780be777c9a204fcb95950f5679a5711aee298
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465828"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="93530-104">Konfigurere virtuelle Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="93530-104">Configure Dataverse virtual tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="93530-105">Dynamics 365 Human Resources er en virtuell datakilde i Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="93530-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="93530-106">Den gir fullstendige opprettings-, lese-, oppdaterings- og sletteoperasjoner (CRUD) fra Dataverse og Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="93530-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="93530-107">Dataene for virtuelle tabeller er ikke lagret i Dataverse, men i programdatabasen.</span><span class="sxs-lookup"><span data-stu-id="93530-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="93530-108">Hvis du vil aktivere CRUD-operasjoner på Human Resources-enheter fra Dataverse, må du gjøre enhetene tilgjengelige som virtuelle tabeller i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="93530-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="93530-109">Dette lar deg utføre CRUD-operasjoner fra Dataverse og Microsoft Power Platform i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="93530-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="93530-110">Operasjonene støtter også den fullstendige forretningslogikken for Human Resources for å sikre dataintegritet ved skriving av data til enhetene.</span><span class="sxs-lookup"><span data-stu-id="93530-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="93530-111">Human Resources-enheter tilsvarer Dataverse-tabeller.</span><span class="sxs-lookup"><span data-stu-id="93530-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="93530-112">Hvis du vil ha mer informasjon om Dataverse (tidligere Common Data Service) og terminologioppdateringer, kan du se [Hva er Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="93530-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="93530-113">Tilgjengelige virtuelle tabeller for Human Resources</span><span class="sxs-lookup"><span data-stu-id="93530-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="93530-114">Alle OData-enheter (Open Data Protocol) i Human Resources er tilgjengelige som virtuelle tabeller i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="93530-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="93530-115">De er også tilgjengelige i Power Platform.</span><span class="sxs-lookup"><span data-stu-id="93530-115">They're also available in Power Platform.</span></span> <span data-ttu-id="93530-116">Du kan nå bygge apper og opplevelser med data direkte fra Human Resources med fullstendig CRUD-funksjonalitet, uten å kopiere eller synkronisere data til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="93530-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="93530-117">Du kan bruke Power Apps-portaler til å bygge eksterne nettsteder som muliggjør samarbeidsscenarier for forretningsprosesser i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="93530-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="93530-118">Du kan vise listen over virtuelle tabeller som er aktivert i miljøet, og begynne å arbeide med enhetene i [Power Apps](https://make.powerapps.com), i løsningen **Dynamics 365 HR Virtual Tables**.</span><span class="sxs-lookup"><span data-stu-id="93530-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![Dynamics 365 HR Virtual Tables i Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="93530-120">Virtuelle tabeller kontra interne tabeller</span><span class="sxs-lookup"><span data-stu-id="93530-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="93530-121">Virtuelle tabeller for Human Resources er ikke det samme som de interne Dataverse-tabeller som opprettes for Human Resources.</span><span class="sxs-lookup"><span data-stu-id="93530-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="93530-122">De interne tabellene for Human Resources genereres separat og vedlikeholdes i HCM Common-løsningen i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="93530-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="93530-123">For interne tabeller lagres dataene i Dataverse og krever synkronisering med appdatabasen for Human Resources.</span><span class="sxs-lookup"><span data-stu-id="93530-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="93530-124">Hvis du vil ha en liste over de interne Dataverse-tabellene for Human Resources, kan du se [Dataverse-tabeller](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="93530-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="93530-125">Installasjon</span><span class="sxs-lookup"><span data-stu-id="93530-125">Setup</span></span>

<span data-ttu-id="93530-126">Følg disse oppsettstrinnene for å aktivere virtuelle tabeller i miljøet.</span><span class="sxs-lookup"><span data-stu-id="93530-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="93530-127">Aktiver virtuelle tabeller i Human Resources</span><span class="sxs-lookup"><span data-stu-id="93530-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="93530-128">Først må du aktivere virtuelle tabeller i arbeidsområdet **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="93530-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="93530-129">Velg **Systemadministrasjon** i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="93530-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="93530-130">Velg flisen **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="93530-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="93530-131">Velg **Støtte for virtuell tabell for i HR i Dataverse**, og velg deretter **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="93530-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="93530-132">Hvis du vil ha mer informasjon om aktivering og deaktivering av funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="93530-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="93530-133">Registrere appen i Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="93530-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="93530-134">Du må registrere Human Resources-forekomsten i Azure Portal slik at Microsoft-identitetsplattform kan tilby godkjennings- og autorisasjonstjenester for appen og brukerne.</span><span class="sxs-lookup"><span data-stu-id="93530-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="93530-135">Hvis du vil ha mer informasjon om registrering av apper i Azure, kan du se [Hurtigstart: Registrer en app i Microsoft-identitetsplattformen](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="93530-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="93530-136">Åpne [Microsoft Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="93530-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="93530-137">I listen over Azure-tjenester velger du **Appregistreringer**.</span><span class="sxs-lookup"><span data-stu-id="93530-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="93530-138">Velg **Ny registrering**.</span><span class="sxs-lookup"><span data-stu-id="93530-138">Select **New registration**.</span></span>

4. <span data-ttu-id="93530-139">I **Navn**-feltet angir du et beskrivende navn for appen.</span><span class="sxs-lookup"><span data-stu-id="93530-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="93530-140">For eksempel **Virtuelle tabeller for Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="93530-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="93530-141">I feltet **URI for omadressering** angir du URL-adressen til navneområdet til forekomsten av Human Resources.</span><span class="sxs-lookup"><span data-stu-id="93530-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="93530-142">Velg **Registrer**.</span><span class="sxs-lookup"><span data-stu-id="93530-142">Select **Register**.</span></span>

7. <span data-ttu-id="93530-143">Når registreringen er fullført, viser Azure-portalen appregistreringens **Oversikt**-rute, som inkluderer **App-ID (klient)**.</span><span class="sxs-lookup"><span data-stu-id="93530-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="93530-144">Noter **App-ID (klient)**.</span><span class="sxs-lookup"><span data-stu-id="93530-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="93530-145">Du angir denne informasjonen når du [konfigurerer datakilden for den virtuelle tabellen](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="93530-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="93530-146">I den venstre navigasjonsruten velger du **Sertifikater og hemmeligheter**.</span><span class="sxs-lookup"><span data-stu-id="93530-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="93530-147">I delen **Klienthemmeligheter** på siden, velger du **Ny klienthemmelighet**.</span><span class="sxs-lookup"><span data-stu-id="93530-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="93530-148">Angi en beskrivelse, velg en varighet og velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="93530-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="93530-149">Noter verdien for hemmeligheten.</span><span class="sxs-lookup"><span data-stu-id="93530-149">Record the secret's value.</span></span> <span data-ttu-id="93530-150">Du angir denne informasjonen når du [konfigurerer datakilden for den virtuelle tabellen](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="93530-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="93530-151">Husk å notere hemmelighetens verdi.</span><span class="sxs-lookup"><span data-stu-id="93530-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="93530-152">Hemmeligheten vises aldri på nytt når du forlater denne siden.</span><span class="sxs-lookup"><span data-stu-id="93530-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="93530-153">Installer Dynamics 365 HR Virtual Table-appen</span><span class="sxs-lookup"><span data-stu-id="93530-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="93530-154">Installer Dynamics 365 HR Virtual Table-appen i Power Apps-miljøet for å distribuere løsningspakken for den virtuelle tabellen til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="93530-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="93530-155">Åpne [Administrasjonssenter for Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="93530-155">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="93530-156">I **Miljøer**-listen velger du Power Apps-miljøet som er tilknyttet Human Resources-forekomsten.</span><span class="sxs-lookup"><span data-stu-id="93530-156">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="93530-157">I **Ressurser**-delen på siden velger du **Dynamics 365-apper**.</span><span class="sxs-lookup"><span data-stu-id="93530-157">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="93530-158">Velg handlingen **Installer app**.</span><span class="sxs-lookup"><span data-stu-id="93530-158">Select the **Install app** action.</span></span>

5. <span data-ttu-id="93530-159">Velg **Dynamics 365 HR Virtual Table**, og velg deretter **Neste**.</span><span class="sxs-lookup"><span data-stu-id="93530-159">Select **Dynamics 365 HR Virtual Table**, and select **Next**.</span></span>

6. <span data-ttu-id="93530-160">Se gjennom og merk for å godta vilkårene for bruk.</span><span class="sxs-lookup"><span data-stu-id="93530-160">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="93530-161">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="93530-161">Select **Install**.</span></span>

<span data-ttu-id="93530-162">Installasjonen tar noen minutter.</span><span class="sxs-lookup"><span data-stu-id="93530-162">The install takes a few minutes.</span></span> <span data-ttu-id="93530-163">Når den er fullført, fortsetter du til de neste trinnene.</span><span class="sxs-lookup"><span data-stu-id="93530-163">When it completes, continue to the next steps.</span></span>

![Installere Dynamics 365 HR Virtual Table-appen fra Administrasjonssenter for Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="93530-165">Konfigurere datakilden for den virtuelle tabellen</span><span class="sxs-lookup"><span data-stu-id="93530-165">Configure the virtual table data source</span></span> 

<span data-ttu-id="93530-166">Det neste trinnet er å konfigurere datakilden for den virtuelle tabellen i Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="93530-166">The next step is to configure the virtual table data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="93530-167">Åpne [Administrasjonssenter for Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="93530-167">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="93530-168">I **Miljøer**-listen velger du Power Apps-miljøet som er tilknyttet Human Resources-forekomsten.</span><span class="sxs-lookup"><span data-stu-id="93530-168">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="93530-169">Velg **URL-adresse for miljø** i **Detaljer**-delen på siden.</span><span class="sxs-lookup"><span data-stu-id="93530-169">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="93530-170">I **huben for løsningstilstand** velger du **Avansert søk**-ikonet øverst til høyre på appsiden.</span><span class="sxs-lookup"><span data-stu-id="93530-170">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="93530-171">På siden **Avansert søk** i rullegardinlisten **Søk etter**, velger du **Konfigurere virtuell datakilde for Finance and Operations**.</span><span class="sxs-lookup"><span data-stu-id="93530-171">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="93530-172">Velg **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="93530-172">Select **Results**.</span></span>

7. <span data-ttu-id="93530-173">Velg posten **Microsoft HR-datakilde**.</span><span class="sxs-lookup"><span data-stu-id="93530-173">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="93530-174">Angi den nødvendige informasjonen for konfigurasjon av datakilden:</span><span class="sxs-lookup"><span data-stu-id="93530-174">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="93530-175">**Mål-URL-adresse**: URL-adressen til Human Resources-navneområdet.</span><span class="sxs-lookup"><span data-stu-id="93530-175">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="93530-176">Formatet på mål-URL-adressen er:</span><span class="sxs-lookup"><span data-stu-id="93530-176">The format of the target URL is:</span></span>
     
     <span data-ttu-id="93530-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="93530-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="93530-178">For eksempel:</span><span class="sxs-lookup"><span data-stu-id="93530-178">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="93530-179">Pass på at du inkluderer tegnet **/** på slutten av URL-adressen for å unngå å motta en feil.</span><span class="sxs-lookup"><span data-stu-id="93530-179">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="93530-180">**Leier-ID**: Leier-ID for Azure Active Directory ( Azure AD).</span><span class="sxs-lookup"><span data-stu-id="93530-180">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="93530-181">**AAD-app-ID**: App-ID (klient) som ble opprettet for appen som er registrert i Microsoft Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="93530-181">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="93530-182">Du har mottatt denne informasjonen tidligere i trinnet [Registrere appen i Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="93530-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="93530-183">**AAD-apphemmelighet**: Klienthemmeligheten som ble opprettet for appen som er registrert i Microsoft Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="93530-183">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="93530-184">Du har mottatt denne informasjonen tidligere i trinnet [Registrere appen i Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="93530-184">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR-datakilde](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="93530-186">Velg **Lagre og lukk**.</span><span class="sxs-lookup"><span data-stu-id="93530-186">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="93530-187">Gi apptillatelser i Human Resources</span><span class="sxs-lookup"><span data-stu-id="93530-187">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="93530-188">Gi tillatelser for de to Azure AD-appene i Human Resources:</span><span class="sxs-lookup"><span data-stu-id="93530-188">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="93530-189">Appen som ble opprettet for leieren din i Microsoft Azure-portalen</span><span class="sxs-lookup"><span data-stu-id="93530-189">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="93530-190">Dynamics 365 HR Virtual Table-appen som er installert i Power Apps-miljøet</span><span class="sxs-lookup"><span data-stu-id="93530-190">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="93530-191">I Human Resources åpner du siden **Azure Active Directory-apper**.</span><span class="sxs-lookup"><span data-stu-id="93530-191">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="93530-192">Velg **Ny** for å opprette en ny appost:</span><span class="sxs-lookup"><span data-stu-id="93530-192">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="93530-193">I **Klient-ID**-feltet angir du klient-ID-en til appen du registrerte i Microsoft Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="93530-193">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="93530-194">I **Navn**-feltet angir du navnet til appen du registrerte i Microsoft Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="93530-194">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="93530-195">I **Bruker-ID**-feltet velger du bruker-ID-en til en bruker med administratortillatelser i Human Resources og Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="93530-195">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="93530-196">Velg **Ny** for å opprette enda en appost:</span><span class="sxs-lookup"><span data-stu-id="93530-196">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="93530-197">**Klient-ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="93530-197">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="93530-198">**Navn**: Dynamics 365 HR Virtual Table</span><span class="sxs-lookup"><span data-stu-id="93530-198">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="93530-199">I **Bruker-ID**-feltet velger du bruker-ID-en til en bruker med administratortillatelser i Human Resources og Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="93530-199">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="93530-200">Generere virtuelle tabeller</span><span class="sxs-lookup"><span data-stu-id="93530-200">Generate virtual tables</span></span>

<span data-ttu-id="93530-201">Når installasjonen er fullført, kan du velge de virtuelle tabeller du vil generere og aktivere i Dataverse-forekomsten.</span><span class="sxs-lookup"><span data-stu-id="93530-201">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="93530-202">I Human Resources åpner du siden **Dataverse-integrering**.</span><span class="sxs-lookup"><span data-stu-id="93530-202">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="93530-203">Velg kategorien **Virtuelle tabeller**.</span><span class="sxs-lookup"><span data-stu-id="93530-203">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="93530-204">Veksleknappen for **aktivering av virtuell tabell** vil bli satt til **Ja** automatisk når alle nødvendige oppsett er fullført.</span><span class="sxs-lookup"><span data-stu-id="93530-204">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="93530-205">Hvis veksleknappen er satt til **Nei**, går du gjennom trinnene i tidligere deler av dette dokumentet for å være sikker på at alle nødvendige oppsett er fullført.</span><span class="sxs-lookup"><span data-stu-id="93530-205">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="93530-206">Velg tabellen eller tabellene du vil generere i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="93530-206">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="93530-207">Velg **Generer/oppdater**.</span><span class="sxs-lookup"><span data-stu-id="93530-207">Select **Generate/refresh**.</span></span>

![Dataverse-integrering](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-table-generation-status"></a><span data-ttu-id="93530-209">Kontrollere status for tabellgenerering</span><span class="sxs-lookup"><span data-stu-id="93530-209">Check table generation status</span></span>

<span data-ttu-id="93530-210">Virtuelle tabeller blir generert i Dataverse gjennom en asynkron bakgrunnsprosess.</span><span class="sxs-lookup"><span data-stu-id="93530-210">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="93530-211">Oppdateringer av prosessvisningen i handlingssenteret.</span><span class="sxs-lookup"><span data-stu-id="93530-211">Updates on the process display in the action center.</span></span> <span data-ttu-id="93530-212">Detaljer om prosessen, inkludert feillogger, vises på siden for **prosessautomatiseringer**.</span><span class="sxs-lookup"><span data-stu-id="93530-212">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="93530-213">I Human Resources åpner du **Prosessautomatiseringer**-siden.</span><span class="sxs-lookup"><span data-stu-id="93530-213">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="93530-214">Velg kategorien **Bakgrunnsprosesser**.</span><span class="sxs-lookup"><span data-stu-id="93530-214">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="93530-215">Velg **Bakgrunnsprosess for asynkron operasjon for virtuell tabell**.</span><span class="sxs-lookup"><span data-stu-id="93530-215">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="93530-216">Velg **Vis de siste resultatene**.</span><span class="sxs-lookup"><span data-stu-id="93530-216">Select **View most recent results**.</span></span>

<span data-ttu-id="93530-217">Hurtigmenyen viser de siste utførelsesresultatene for prosessen.</span><span class="sxs-lookup"><span data-stu-id="93530-217">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="93530-218">Du kan vise loggen for prosessen, inkludert eventuelle feil som returneres fra Dataverse.</span><span class="sxs-lookup"><span data-stu-id="93530-218">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="93530-219">Se også</span><span class="sxs-lookup"><span data-stu-id="93530-219">See also</span></span>

[<span data-ttu-id="93530-220">Hva er Dataverse?</span><span class="sxs-lookup"><span data-stu-id="93530-220">What is Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="93530-221">Tabeller i Dataverse</span><span class="sxs-lookup"><span data-stu-id="93530-221">Tables in Dataverse</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="93530-222">Oversikt over tabellrelasjoner</span><span class="sxs-lookup"><span data-stu-id="93530-222">Table relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="93530-223">Opprette og redigere virtuelle tabeller som inneholder data fra en ekstern datakilde</span><span class="sxs-lookup"><span data-stu-id="93530-223">Create and edit virtual tables that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="93530-224">Hva er Power Apps-portaler?</span><span class="sxs-lookup"><span data-stu-id="93530-224">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="93530-225">Oversikt over oppretting av apper i Power Apps</span><span class="sxs-lookup"><span data-stu-id="93530-225">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]