---
title: Konfigurere virtuelle enheter for Common Data Service
description: Dette emnet beskriver hvordan du konfigurerer virtuelle enheter for Dynamics 365 Human Resources. Generer og oppdater eksisterende virtuelle enheter og analyser genererte og tilgjengelige enheter.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
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
ms.openlocfilehash: 2b590faeab600d04c9d5303693ec1e9ac682250d
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645607"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="ae08e-104">Konfigurere virtuelle enheter for Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ae08e-104">Configure Common Data Service virtual entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ae08e-105">Dynamics 365 Human Resources er en virtuell datakilde i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ae08e-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="ae08e-106">Den gir fullstendige opprettings-, lese-, oppdaterings- og sletteoperasjoner (CRUD) fra Common Data Service og Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="ae08e-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="ae08e-107">Dataene for virtuelle enheter er ikke lagret i Common Data Service, men i programdatabasen.</span><span class="sxs-lookup"><span data-stu-id="ae08e-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="ae08e-108">Hvis du vil aktivere CRUD-operasjoner på Human Resources-enheter fra Common Data Service, må du gjøre enhetene tilgjengelige som virtuelle enheter i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ae08e-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="ae08e-109">Dette lar deg utføre CRUD-operasjoner fra Common Data Service og Microsoft Power Platform i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ae08e-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="ae08e-110">Operasjonene støtter også den fullstendige forretningslogikken for Human Resources for å sikre dataintegritet ved skriving av data til enhetene.</span><span class="sxs-lookup"><span data-stu-id="ae08e-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="ae08e-111">Tilgjengelige virtuelle enheter for Human Resources</span><span class="sxs-lookup"><span data-stu-id="ae08e-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="ae08e-112">Alle OData-enheter (Open Data Protocol) i Human Resources er tilgjengelige som virtuelle enheter i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ae08e-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="ae08e-113">De er også tilgjengelige i Power Platform.</span><span class="sxs-lookup"><span data-stu-id="ae08e-113">They're also available in Power Platform.</span></span> <span data-ttu-id="ae08e-114">Du kan nå bygge apper og opplevelser med data direkte fra Human Resources med fullstendig CRUD-funksjonalitet, uten å kopiere eller synkronisere data til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ae08e-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="ae08e-115">Du kan bruke Power Apps-portaler til å bygge eksterne nettsteder som muliggjør samarbeidsscenarier for forretningsprosesser i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ae08e-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="ae08e-116">Du kan vise listen over virtuelle enheter som er aktivert i miljøet, og begynne å arbeide med enhetene i [Power Apps](https://make.powerapps.com), i løsningen **Dynamics 365 HR Virtual Entities**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Dynamics 365 HR Virtual Entities i Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="ae08e-118">Virtuelle enheter kontra naturlige enheter</span><span class="sxs-lookup"><span data-stu-id="ae08e-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="ae08e-119">Virtuelle enheter for Human Resources er ikke det samme som de naturlige Common Data Service-enhetene som opprettes for Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ae08e-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="ae08e-120">De naturlige enhetene for Human Resources genereres separat og vedlikeholdes i den HCM Common-løsningen i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ae08e-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="ae08e-121">For naturlige enheter lagres dataene i Common Data Service og krever synkronisering med appdatabasen for Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ae08e-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="ae08e-122">Hvis du vil ha en liste over de naturlige Common Data Service-enhetene for Human Resources, kan du se [Common Data Service-enheter](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="ae08e-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="ae08e-123">Installasjon</span><span class="sxs-lookup"><span data-stu-id="ae08e-123">Setup</span></span>

<span data-ttu-id="ae08e-124">Følg disse oppsettstrinnene for å aktivere virtuelle enheter i miljøet.</span><span class="sxs-lookup"><span data-stu-id="ae08e-124">Follow these setup steps to enable virtual entities in your environment.</span></span>

### <a name="enable-virtual-entities-in-human-resources"></a><span data-ttu-id="ae08e-125">Aktiver virtuelle enheter i Human Resources</span><span class="sxs-lookup"><span data-stu-id="ae08e-125">Enable virtual entities in Human Resources</span></span>

<span data-ttu-id="ae08e-126">Først må du aktivere virtuelle enheter i arbeidsområdet **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-126">First, you must enable virtual entities in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="ae08e-127">Velg **Systemadministrasjon** i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ae08e-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="ae08e-128">Velg flisen **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-128">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="ae08e-129">Velg **Støtte for virtuell enhet i HR/CDS** og velg deretter **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-129">Select **Virtual Entity support in HR/CDS**, and then select **Enable**.</span></span>

<span data-ttu-id="ae08e-130">Hvis du vil ha mer informasjon om aktivering og deaktivering av funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="ae08e-130">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="ae08e-131">Registrere appen i Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="ae08e-131">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="ae08e-132">Du må registrere Human Resources-forekomsten i Azure Portal slik at Microsoft-identitetsplattform kan tilby godkjennings- og autorisasjonstjenester for appen og brukerne.</span><span class="sxs-lookup"><span data-stu-id="ae08e-132">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="ae08e-133">Hvis du vil ha mer informasjon om registrering av apper i Azure, kan du se [Hurtigstart: Registrer en app i Microsoft-identitetsplattformen](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="ae08e-133">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="ae08e-134">Åpne [Microsoft Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="ae08e-134">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="ae08e-135">I listen over Azure-tjenester velger du **Appregistreringer**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-135">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="ae08e-136">Velg **Ny registrering**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-136">Select **New registration**.</span></span>

4. <span data-ttu-id="ae08e-137">I **Navn**-feltet angir du et beskrivende navn for appen.</span><span class="sxs-lookup"><span data-stu-id="ae08e-137">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="ae08e-138">For eksempel **Virtuelle enheter for Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-138">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="ae08e-139">I feltet **URI for omadressering** angir du URL-adressen til navneområdet til forekomsten av Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ae08e-139">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="ae08e-140">Velg **Registrer**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-140">Select **Register**.</span></span>

7. <span data-ttu-id="ae08e-141">Når registreringen er fullført, viser Azure-portalen appregistreringens **Oversikt**-rute, som inkluderer **App-ID (klient)**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-141">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="ae08e-142">Noter **App-ID (klient)**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-142">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="ae08e-143">Du angir denne informasjonen når du [konfigurerer datakilden for den virtuelle enheten](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="ae08e-143">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="ae08e-144">I den venstre navigasjonsruten velger du **Sertifikater og hemmeligheter**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-144">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="ae08e-145">I delen **Klienthemmeligheter** på siden, velger du **Ny klienthemmelighet**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-145">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="ae08e-146">Angi en beskrivelse, velg en varighet og velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-146">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="ae08e-147">Noter verdien for hemmeligheten.</span><span class="sxs-lookup"><span data-stu-id="ae08e-147">Record the secret's value.</span></span> <span data-ttu-id="ae08e-148">Du angir denne informasjonen når du [konfigurerer datakilden for den virtuelle enheten](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="ae08e-148">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="ae08e-149">Husk å notere hemmelighetens verdi.</span><span class="sxs-lookup"><span data-stu-id="ae08e-149">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="ae08e-150">Hemmeligheten vises aldri på nytt når du forlater denne siden.</span><span class="sxs-lookup"><span data-stu-id="ae08e-150">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="ae08e-151">Installer Dynamics 365 HR Virtual Entity-appen</span><span class="sxs-lookup"><span data-stu-id="ae08e-151">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="ae08e-152">Installer Dynamics 365 HR Virtual Entity-appen i Power Apps-miljøet for å distribuere løsningspakken for den virtuelle enheten til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ae08e-152">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="ae08e-153">Åpne [Administrasjonssenter for Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ae08e-153">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="ae08e-154">I **Miljøer**-listen velger du Power Apps-miljøet som er tilknyttet Human Resources-forekomsten.</span><span class="sxs-lookup"><span data-stu-id="ae08e-154">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="ae08e-155">I **Ressurser**-delen på siden velger du **Dynamics 365-apper**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-155">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="ae08e-156">Velg handlingen **Installer app**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-156">Select the **Install app** action.</span></span>

5. <span data-ttu-id="ae08e-157">Velg **Dynamics 365 HR Virtual Entity**, og velg deretter **Neste**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-157">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="ae08e-158">Se gjennom og merk for å godta vilkårene for bruk.</span><span class="sxs-lookup"><span data-stu-id="ae08e-158">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="ae08e-159">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-159">Select **Install**.</span></span>

<span data-ttu-id="ae08e-160">Installasjonen tar noen minutter.</span><span class="sxs-lookup"><span data-stu-id="ae08e-160">The install takes a few minutes.</span></span> <span data-ttu-id="ae08e-161">Når den er fullført, fortsetter du til de neste trinnene.</span><span class="sxs-lookup"><span data-stu-id="ae08e-161">When it completes, continue to the next steps.</span></span>

![Installere Dynamics 365 HR Virtual Entity-appen fra Administrasjonssenter for Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="ae08e-163">Konfigurere datakilden for den virtuelle enheten</span><span class="sxs-lookup"><span data-stu-id="ae08e-163">Configure the virtual entity data source</span></span> 

<span data-ttu-id="ae08e-164">Det neste trinnet er å konfigurere datakilden for den virtuelle enheten i Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="ae08e-164">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="ae08e-165">Åpne [Administrasjonssenter for Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ae08e-165">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="ae08e-166">I **Miljøer**-listen velger du Power Apps-miljøet som er tilknyttet Human Resources-forekomsten.</span><span class="sxs-lookup"><span data-stu-id="ae08e-166">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="ae08e-167">Velg **URL-adresse for miljø** i **Detaljer**-delen på siden.</span><span class="sxs-lookup"><span data-stu-id="ae08e-167">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="ae08e-168">I **huben for løsningstilstand** velger du **Avansert søk**-ikonet øverst til høyre på appsiden.</span><span class="sxs-lookup"><span data-stu-id="ae08e-168">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="ae08e-169">På siden **Avansert søk** i rullegardinlisten **Søk etter**, velger du **Konfigurere virtuell datakilde for Finance and Operations**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-169">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="ae08e-170">Velg **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-170">Select **Results**.</span></span>

7. <span data-ttu-id="ae08e-171">Velg posten **Microsoft HR-datakilde**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-171">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="ae08e-172">Angi den nødvendige informasjonen for konfigurasjon av datakilden:</span><span class="sxs-lookup"><span data-stu-id="ae08e-172">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="ae08e-173">**Mål-URL-adresse**: URL-adressen til Human Resources-navneområdet.</span><span class="sxs-lookup"><span data-stu-id="ae08e-173">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="ae08e-174">Formatet på mål-URL-adressen er:</span><span class="sxs-lookup"><span data-stu-id="ae08e-174">The format of the target URL is:</span></span>
     
     <span data-ttu-id="ae08e-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="ae08e-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="ae08e-176">For eksempel:</span><span class="sxs-lookup"><span data-stu-id="ae08e-176">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="ae08e-177">Pass på at du inkluderer tegnet **/** på slutten av URL-adressen for å unngå å motta en feil.</span><span class="sxs-lookup"><span data-stu-id="ae08e-177">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="ae08e-178">**Leier-ID**: Leier-ID for Azure Active Directory ( Azure AD).</span><span class="sxs-lookup"><span data-stu-id="ae08e-178">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="ae08e-179">**AAD-app-ID**: App-ID (klient) som ble opprettet for appen som er registrert i Microsoft Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="ae08e-179">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="ae08e-180">Du har mottatt denne informasjonen tidligere i trinnet [Registrere appen i Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="ae08e-180">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="ae08e-181">**AAD-apphemmelighet**: Klienthemmeligheten som ble opprettet for appen som er registrert i Microsoft Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="ae08e-181">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="ae08e-182">Du har mottatt denne informasjonen tidligere i trinnet [Registrere appen i Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="ae08e-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR-datakilde](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="ae08e-184">Velg **Lagre og lukk**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-184">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="ae08e-185">Gi apptillatelser i Human Resources</span><span class="sxs-lookup"><span data-stu-id="ae08e-185">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="ae08e-186">Gi tillatelser for de to Azure AD-appene i Human Resources:</span><span class="sxs-lookup"><span data-stu-id="ae08e-186">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="ae08e-187">Appen som ble opprettet for leieren din i Microsoft Azure-portalen</span><span class="sxs-lookup"><span data-stu-id="ae08e-187">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="ae08e-188">Dynamics 365 HR Virtual Entity-appen som er installert i Power Apps-miljøet</span><span class="sxs-lookup"><span data-stu-id="ae08e-188">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="ae08e-189">I Human Resources åpner du siden **Azure Active Directory-apper**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-189">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="ae08e-190">Velg **Ny** for å opprette en ny appost:</span><span class="sxs-lookup"><span data-stu-id="ae08e-190">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="ae08e-191">I **Klient-ID**-feltet angir du klient-ID-en til appen du registrerte i Microsoft Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="ae08e-191">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="ae08e-192">I **Navn**-feltet angir du navnet til appen du registrerte i Microsoft Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="ae08e-192">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="ae08e-193">I **Bruker-ID**-feltet velger du bruker-ID-en til en bruker med administratortillatelser i Human Resources og Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="ae08e-193">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="ae08e-194">Velg **Ny** for å opprette enda en appost:</span><span class="sxs-lookup"><span data-stu-id="ae08e-194">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="ae08e-195">**Klient-ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="ae08e-195">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="ae08e-196">**Navn**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="ae08e-196">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="ae08e-197">I **Bruker-ID**-feltet velger du bruker-ID-en til en bruker med administratortillatelser i Human Resources og Power Apps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="ae08e-197">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="ae08e-198">Generere virtuelle enheter</span><span class="sxs-lookup"><span data-stu-id="ae08e-198">Generate virtual entities</span></span>

<span data-ttu-id="ae08e-199">Når installasjonen er fullført, kan du velge de virtuelle enhetene du vil generere og aktivere i Common Data Service-forekomsten.</span><span class="sxs-lookup"><span data-stu-id="ae08e-199">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="ae08e-200">I Human Resources åpner du siden **Common Data Service (CDS)-integrering**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-200">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="ae08e-201">Velg kategorien **Virtuelle enheter**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-201">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="ae08e-202">Veksleknappen for **aktivering av virtuell enhet** vil bli satt til **Ja** automatisk når alle nødvendige oppsett er fullført.</span><span class="sxs-lookup"><span data-stu-id="ae08e-202">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="ae08e-203">Hvis veksleknappen er satt til **Nei**, går du gjennom trinnene i tidligere deler av dette dokumentet for å være sikker på at alle nødvendige oppsett er fullført.</span><span class="sxs-lookup"><span data-stu-id="ae08e-203">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="ae08e-204">Velg enheten eller enhetene du vil generere i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ae08e-204">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="ae08e-205">Velg **Generer/oppdater**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-205">Select **Generate/refresh**.</span></span>

![Common Data Service-integrering](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="ae08e-207">Kontrollere status for enhetsgenerering</span><span class="sxs-lookup"><span data-stu-id="ae08e-207">Check entity generation status</span></span>

<span data-ttu-id="ae08e-208">Virtuelle enheter blir generert i Common Data Service gjennom en asynkron bakgrunnsprosess.</span><span class="sxs-lookup"><span data-stu-id="ae08e-208">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="ae08e-209">Oppdateringer av prosessvisningen i handlingssenteret.</span><span class="sxs-lookup"><span data-stu-id="ae08e-209">Updates on the process display in the action center.</span></span> <span data-ttu-id="ae08e-210">Detaljer om prosessen, inkludert feillogger, vises på siden for **prosessautomatiseringer**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-210">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="ae08e-211">I Human Resources åpner du **Prosessautomatiseringer**-siden.</span><span class="sxs-lookup"><span data-stu-id="ae08e-211">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="ae08e-212">Velg kategorien **Bakgrunnsprosesser**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-212">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="ae08e-213">Velg **Bakgrunnsprosess for asynkron operasjon for virtuell enhet**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-213">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="ae08e-214">Velg **Vis de siste resultatene**.</span><span class="sxs-lookup"><span data-stu-id="ae08e-214">Select **View most recent results**.</span></span>

<span data-ttu-id="ae08e-215">Hurtigmenyen viser de siste utførelsesresultatene for prosessen.</span><span class="sxs-lookup"><span data-stu-id="ae08e-215">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="ae08e-216">Du kan vise loggen for prosessen, inkludert eventuelle feil som returneres fra Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ae08e-216">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae08e-217">Se også</span><span class="sxs-lookup"><span data-stu-id="ae08e-217">See also</span></span>

[<span data-ttu-id="ae08e-218">Hva er Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="ae08e-218">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="ae08e-219">Enhetsoversikt</span><span class="sxs-lookup"><span data-stu-id="ae08e-219">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="ae08e-220">Oversikt over enhetsrelasjoner</span><span class="sxs-lookup"><span data-stu-id="ae08e-220">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="ae08e-221">Opprette og redigere virtuelle enheter som inneholder data fra en ekstern datakilde</span><span class="sxs-lookup"><span data-stu-id="ae08e-221">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="ae08e-222">Hva er Power Apps-portaler?</span><span class="sxs-lookup"><span data-stu-id="ae08e-222">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="ae08e-223">Oversikt over oppretting av apper i Power Apps</span><span class="sxs-lookup"><span data-stu-id="ae08e-223">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
