---
title: Konfigurasjon for Finance Insights (forhåndsversjon)
description: Dette emnet forklarer konfigurasjonstrinnene som gjør at systemet kan bruke funksjonene i Finance Insights.
author: ShivamPandey-msft
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 60e4d69157d7b73bd9e47310adae320687230080
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941232"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="0c13a-103">Konfigurasjon for Finance Insights (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="0c13a-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0c13a-104">Finance Insights kombinerer funksjonalitet fra Microsoft Dynamics 365 Finance med Microsoft Dataverse, Azure og AI Builder for å gi organisasjonen kraftige prognoseverktøy.</span><span class="sxs-lookup"><span data-stu-id="0c13a-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="0c13a-105">Dette emnet forklarer konfigurasjonstrinnene som gjør at systemet kan bruke funksjonene i Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="0c13a-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="0c13a-106">Klargjøre Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="0c13a-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="0c13a-107">Klargjør miljøene ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="0c13a-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="0c13a-108">Opprett eller oppdater et Dynamics 365 Finance-miljø i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="0c13a-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="0c13a-109">Miljøet krever appversjon 10.0.11 / Platform update 35 eller senere.</span><span class="sxs-lookup"><span data-stu-id="0c13a-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="0c13a-110">Miljøet må være et miljø med høy tilgjengelighet i sandkassemodus.</span><span class="sxs-lookup"><span data-stu-id="0c13a-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="0c13a-111">(Denne typen miljø kalles også et miljø på lag 2.) Hvis du vil ha mer informasjon, kan du se [Miljøplanlegging](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="0c13a-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="0c13a-112">Hvis du bruker Contoso-demonstrasjonsdata, må du ha flere eksempeldata for å kunne bruke funksjonene for kundebetalingsprognoser, kontantstrømprognoser og budsjettprognoser.</span><span class="sxs-lookup"><span data-stu-id="0c13a-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="0c13a-113">Konfigurer Dataverse</span><span class="sxs-lookup"><span data-stu-id="0c13a-113">Configure Dataverse</span></span>

<span data-ttu-id="0c13a-114">Bruk fremgangsmåten nedenfor til å konfigurere Dataverse for Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="0c13a-114">Use the following steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="0c13a-115">Åpne miljøsiden i LCS, og kontroller at **Power Platform-integrering** allerede er satt opp.</span><span class="sxs-lookup"><span data-stu-id="0c13a-115">Open the environment page in LCS and verify that the **Power Platform Integration** section is already setup.</span></span>
    1. <span data-ttu-id="0c13a-116">Hvis det allerede er satt opp, skal Dataverse-miljønavnet som er koblet til Dynamics 365 Finance-miljøet, vises.</span><span class="sxs-lookup"><span data-stu-id="0c13a-116">If it is already set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="0c13a-117">Kopier Dataverse-miljønavnet.</span><span class="sxs-lookup"><span data-stu-id="0c13a-117">Copy the Dataverse environment name.</span></span>
    2. <span data-ttu-id="0c13a-118">Hvis det ikke er definert, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="0c13a-118">If it is not set up, follow these steps:</span></span>
        1. <span data-ttu-id="0c13a-119">Velg **Oppsett**-knappen i Power Platform-integreringsdelen.</span><span class="sxs-lookup"><span data-stu-id="0c13a-119">Select the **Setup** button in the Power Platform Integration section.</span></span> <span data-ttu-id="0c13a-120">Det kan ta opptil en time før miljøet er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="0c13a-120">It may take up to an hour for the environment to be set up.</span></span>
        2. <span data-ttu-id="0c13a-121">Hvis Dataverse-miljøet er konfigurert riktig, skal Dataverse-miljøetnavnet som er koblet til Dynamics 365 Finance-miljøet, vises.</span><span class="sxs-lookup"><span data-stu-id="0c13a-121">If the Dataverse environment is successfully set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="0c13a-122">Kopier Dataverse-miljønavnet.</span><span class="sxs-lookup"><span data-stu-id="0c13a-122">Copy the Dataverse environment name.</span></span>
> [!NOTE]
> <span data-ttu-id="0c13a-123">Når du har fullført miljøoppsettet, må du **IKKE** velge knappen **Kobling til CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-123">After completing the environment set up, **DO NOT** select the **Link to CDS for Apps** button.</span></span> <span data-ttu-id="0c13a-124">Dette er ikke nødvendig for Finance Insights og vil deaktivere muligheten til å fullføre de nødvendige miljøtilleggene i LCS.</span><span class="sxs-lookup"><span data-stu-id="0c13a-124">This is not needed for Finance Insights and will disable the ability to complete the required Environment Add-ins in LCS.</span></span>

2. <span data-ttu-id="0c13a-125">Åpne [administrasjonssenteret for Power Platform](https://admin.powerplatform.microsoft.com/), og følg denne fremgangsmåten for å opprette et nytt Dataverse-miljø i den samme Active Directory-leieren:</span><span class="sxs-lookup"><span data-stu-id="0c13a-125">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="0c13a-126">Åpne **Miljøer**-siden.</span><span class="sxs-lookup"><span data-stu-id="0c13a-126">Open the **Environments** page.</span></span>

        <span data-ttu-id="0c13a-127">[![Miljøer-siden](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="0c13a-127">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="0c13a-128">Velg Dataverse-miljøet som opprettes over, og velg deretter **Innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-128">Select the Dataverse environment created above and then select **Settings**.</span></span>
    3. <span data-ttu-id="0c13a-129">Velg **Ressurser \> Alle eldre innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-129">Select **Resources \> All Legacy Settings**.</span></span>
    4. <span data-ttu-id="0c13a-130">Velg **Innstillinger** i det øverste navigasjonsfeltet, og velg deretter **Tilpassinger**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-130">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    5. <span data-ttu-id="0c13a-131">Velg **Utviklerressurser**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-131">Select **Developer Resources**.</span></span>
    6. <span data-ttu-id="0c13a-132">Kopier verdien for **Dataverse-organisasjons-ID**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-132">Copy the **Dataverse organization ID** value.</span></span>
    7. <span data-ttu-id="0c13a-133">Noter deg URL-adressen for Dataverse-organisasjonen på adresselinjen i nettleseren.</span><span class="sxs-lookup"><span data-stu-id="0c13a-133">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="0c13a-134">URL-adressen kan for eksempel være `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="0c13a-134">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

3. <span data-ttu-id="0c13a-135">Hvis du har tenkt å bruke funksjonen Kontantstrømprognoser eller Budsjettprognoser, følger du disse trinnene for å oppdatere merknadsgrensen for organisasjonen til minst 50 megabyte (MB):</span><span class="sxs-lookup"><span data-stu-id="0c13a-135">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="0c13a-136">Åpne [Power Apps-portalen](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="0c13a-136">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="0c13a-137">Velg miljøet du nettopp opprettet, og velg deretter **Avanserte innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-137">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="0c13a-138">Velg **Innstillinger \> E-postkonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-138">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="0c13a-139">Endre verdien i feltet **Maksimal filstørrelse** til **51 200**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-139">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="0c13a-140">(Verdien uttrykkes i kilobyte \[kB\].)</span><span class="sxs-lookup"><span data-stu-id="0c13a-140">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="0c13a-141">Velg **OK** for å lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="0c13a-141">Select **OK** to save your changes.</span></span>

## <a name="configure-the-azure-setup"></a><span data-ttu-id="0c13a-142">Konfigurere Azure-oppsettet</span><span class="sxs-lookup"><span data-stu-id="0c13a-142">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="0c13a-143">Angi katalog-ID-en for Dataverse og brukerens objekt-ID for Azure AD</span><span class="sxs-lookup"><span data-stu-id="0c13a-143">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="0c13a-144">Angi katalog-ID-en for Dataverse:</span><span class="sxs-lookup"><span data-stu-id="0c13a-144">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="0c13a-145">Åpne [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="0c13a-145">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="0c13a-146">Logg på ved å bruke bruker-ID-en som ble brukt til å opprette Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="0c13a-146">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="0c13a-147">Gå til **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-147">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="0c13a-148">Kopier verdien for **Leier-ID**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-148">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="0c13a-149">Angi brukerens objekt-ID for Azure Active Directory (Azure AD):</span><span class="sxs-lookup"><span data-stu-id="0c13a-149">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="0c13a-150">Gå til **Brukere** i [Azure-portalen](https://portal.azure.com), og søk etter brukeren etter e-postadresse.</span><span class="sxs-lookup"><span data-stu-id="0c13a-150">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="0c13a-151">Velg brukerens navn.</span><span class="sxs-lookup"><span data-stu-id="0c13a-151">Select the user's name.</span></span>
    3. <span data-ttu-id="0c13a-152">Kopier verdien for **Objekt-ID**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-152">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="0c13a-153">Bruke Azure Cloud Shell til å konfigurere Data Lake-ressurser for Finance Insights</span><span class="sxs-lookup"><span data-stu-id="0c13a-153">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="0c13a-154">Bruke et Windows PowerShell-skript</span><span class="sxs-lookup"><span data-stu-id="0c13a-154">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="0c13a-155">Et Windows PowerShell-skript er oppgitt, slik at du lett kan konfigurere Azure-ressursene som er beskrevet i [Konfigurere eksport til Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="0c13a-155">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="0c13a-156">Hvis du foretrekker å konfigurere manuelt, kan du hoppe over denne fremgangsmåten og fortsette med fremgangsmåten i delen [Manuell konfigurasjon](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="0c13a-156">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="0c13a-157">Følg fremgangsmåten nedenfor for å kjøre PowerShell-skriptet.</span><span class="sxs-lookup"><span data-stu-id="0c13a-157">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="0c13a-158">Det kan hende at Azure CLI-alternativet «Prøv det» eller å kjøre skriptet på PC-en ikke fungerer.</span><span class="sxs-lookup"><span data-stu-id="0c13a-158">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="0c13a-159">Følg denne fremgangsmåten for å konfigurere Azure ved hjelp av Windows PowerShell-skriptet.</span><span class="sxs-lookup"><span data-stu-id="0c13a-159">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="0c13a-160">Du må ha rettigheter til å opprette en Azure-ressursgruppe, Azure-ressurser og et Azure AD-program.</span><span class="sxs-lookup"><span data-stu-id="0c13a-160">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="0c13a-161">Hvis du vil ha informasjon om de nødvendige tillatelsene, kan du se [Kontrollere Azure AD-tillatelser](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="0c13a-161">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="0c13a-162">I [Azure-portalen](https://portal.azure.com) går du til Azure-målabonnementet.</span><span class="sxs-lookup"><span data-stu-id="0c13a-162">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="0c13a-163">Velg **Cloud Shell**-knappen til høyre for **Søk**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0c13a-163">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="0c13a-164">Velg **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-164">Select **PowerShell**.</span></span>
3. <span data-ttu-id="0c13a-165">Opprett lagringsplass hvis du blir bedt om det.</span><span class="sxs-lookup"><span data-stu-id="0c13a-165">Create storage if you're prompted to do so.</span></span>
4. <span data-ttu-id="0c13a-166">Gå til kategorien **Azure CLI** og velg **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-166">Go to the **Azure CLI** tab and select **Copy**.</span></span>  
5. <span data-ttu-id="0c13a-167">Åpne Notisblokk, og lim inn PowerShell-skriptet.</span><span class="sxs-lookup"><span data-stu-id="0c13a-167">Open Notepad and paste the PowerShell script.</span></span> <span data-ttu-id="0c13a-168">Lagre filen som ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="0c13a-168">Save the file as ConfigureDataLake.ps1.</span></span>
6. <span data-ttu-id="0c13a-169">Last opp Windows PowerShell-skriptet til økten ved hjelp av menyalternativet for opplasting i Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="0c13a-169">Upload the Windows PowerShell script to the session using the menu option for upload in Cloud Shell.</span></span>
7. <span data-ttu-id="0c13a-170">Kjør skriptet .\ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="0c13a-170">Run the script .\ConfigureDataLake.ps1.</span></span>
8. <span data-ttu-id="0c13a-171">Følg instruksjonene for å kjøre skriptet.</span><span class="sxs-lookup"><span data-stu-id="0c13a-171">Follow the prompts to run the script.</span></span>
9. <span data-ttu-id="0c13a-172">Bruk informasjonen fra skriptutdataene til å installere tillegget **Eksporter til Data Lake** i LCS.</span><span class="sxs-lookup"><span data-stu-id="0c13a-172">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
10. <span data-ttu-id="0c13a-173">Bruk informasjonen fra skriptutdataene til å aktivere enhetslageret på **Datatilkoblinger**-siden i Finance (**Systemadministrasjon \> Systemparametere \> Datatilkoblinger**).</span><span class="sxs-lookup"><span data-stu-id="0c13a-173">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="0c13a-174">Manuell konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="0c13a-174">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="0c13a-175">Legg til programmer i Azure AD-leieren</span><span class="sxs-lookup"><span data-stu-id="0c13a-175">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="0c13a-176">Gå til **Azure Active Directory** i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="0c13a-176">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="0c13a-177">Velg **Behandle \> Enterprise-programmer**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-177">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="0c13a-178">Søk etter følgende programmer etter app-ID.</span><span class="sxs-lookup"><span data-stu-id="0c13a-178">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="0c13a-179">Program</span><span class="sxs-lookup"><span data-stu-id="0c13a-179">Application</span></span>                              | <span data-ttu-id="0c13a-180">App-ID</span><span class="sxs-lookup"><span data-stu-id="0c13a-180">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="0c13a-181">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="0c13a-181">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="0c13a-182">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="0c13a-182">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="0c13a-183">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="0c13a-183">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="0c13a-184">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="0c13a-184">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="0c13a-185">AI Builder Authorization Service</span><span class="sxs-lookup"><span data-stu-id="0c13a-185">AI Builder Authorization Service</span></span>         | <span data-ttu-id="0c13a-186">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="0c13a-186">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="0c13a-187">Hvis du ikke finner noen av de ovennevnte programmene, kan du prøve følgende trinn.</span><span class="sxs-lookup"><span data-stu-id="0c13a-187">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="0c13a-188">Velg **Start**-menyen på den lokale maskinen, og søk etter **powershell**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-188">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="0c13a-189">Velg og hold (eller høyreklikk på) **Windows PowerShell**, og velg deretter **Kjør som administrator**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-189">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="0c13a-190">Kjør følgende kommando for å installere **AzureAD**-modulen.</span><span class="sxs-lookup"><span data-stu-id="0c13a-190">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="0c13a-191">Hvis en NuGet-leverandør kreves for å fortsette, velger du **J** for å installere den.</span><span class="sxs-lookup"><span data-stu-id="0c13a-191">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="0c13a-192">Hvis det vises en melding om at repositoriet ikke er klarert, velger du **J** for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="0c13a-192">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="0c13a-193">For hvert program som må legges til, kjører du følgende kommandoer for å legge til programmet i Azure AD.</span><span class="sxs-lookup"><span data-stu-id="0c13a-193">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="0c13a-194">Når du blir bedt om det, logger du på som Azure AD-administrator.</span><span class="sxs-lookup"><span data-stu-id="0c13a-194">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="0c13a-195">Opprette Azure-ressurser</span><span class="sxs-lookup"><span data-stu-id="0c13a-195">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="0c13a-196">Kontroller at du oppretter følgende ressurser i samme Azure AD-forekomst som Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="0c13a-196">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="0c13a-197">Du kan ikke bruke ressurser fra en annen Azure AD-forekomst.</span><span class="sxs-lookup"><span data-stu-id="0c13a-197">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="0c13a-198">Opprette en ny lagringskonto:</span><span class="sxs-lookup"><span data-stu-id="0c13a-198">Create a new storage account:</span></span>

    1. <span data-ttu-id="0c13a-199">Opprett en lagringskonto i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="0c13a-199">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="0c13a-200">I dialogboksen **Opprett lagringskonto** angir du verdier i følgende felter:</span><span class="sxs-lookup"><span data-stu-id="0c13a-200">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="0c13a-201">**Plassering** – Velg datasenteret der miljøet er plassert.</span><span class="sxs-lookup"><span data-stu-id="0c13a-201">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="0c13a-202">**Ytelse** – Vi anbefaler at du velger **Standard**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-202">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="0c13a-203">**Kontotype** – Du må velge **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-203">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="0c13a-204">Velg **Aktiver** under funksjonen **Hierarkiske navneområder** for alternativet **Data Lake Storage Gen2** i dialogboksen **Avanserte alternativer**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-204">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="0c13a-205">Hvis du deaktiverer denne funksjonen, kan du ikke bruke data som Finance and Operations-apper skriver ved hjelp av tjenester som Power BI-dataflyter.</span><span class="sxs-lookup"><span data-stu-id="0c13a-205">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="0c13a-206">Velg **Se gjennom og opprett**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-206">Select **Review and create**.</span></span> <span data-ttu-id="0c13a-207">Når distribusjonen er fullført, vises den nye ressursen i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="0c13a-207">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="0c13a-208">Gå til lagringskontoen du opprettet.</span><span class="sxs-lookup"><span data-stu-id="0c13a-208">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="0c13a-209">Velg **Tilgangsnøkler** på menyen til venstre.</span><span class="sxs-lookup"><span data-stu-id="0c13a-209">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="0c13a-210">Kopier og lagre tilkoblingsstrengen for **Nøkkel1** eller **Nøkkel2**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-210">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="0c13a-211">Kopier og lagre navnet på lagringskontoen.</span><span class="sxs-lookup"><span data-stu-id="0c13a-211">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="0c13a-212">Opprett et nytt nøkkelhvelv:</span><span class="sxs-lookup"><span data-stu-id="0c13a-212">Create a new key vault:</span></span>

    1. <span data-ttu-id="0c13a-213">Opprett et nøkkelhvelv i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="0c13a-213">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="0c13a-214">I **Plassering**-feltet i dialogboksen **Opprett nøkkelhvelv** velger du datasenteret der miljøet er.</span><span class="sxs-lookup"><span data-stu-id="0c13a-214">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="0c13a-215">Etter at nøkkelhvelvet er opprettet, velger du det i listen og velger deretter **Hemmeligheter**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-215">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="0c13a-216">Velg **Generer/Importer**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-216">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="0c13a-217">I feltet **Opplastingsalternativer** i dialogboksen **Opprett en hemmelighet** velger du **Manuell**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-217">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="0c13a-218">Angi et navn for hemmeligheten.</span><span class="sxs-lookup"><span data-stu-id="0c13a-218">Enter a name for the secret.</span></span> <span data-ttu-id="0c13a-219">Noter deg navnet, fordi du må angi det senere.</span><span class="sxs-lookup"><span data-stu-id="0c13a-219">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="0c13a-220">I **Verdi**-feltet angir du tilkoblingsstrengen du fikk fra lagringskontoen i forrige fremgangsmåte.</span><span class="sxs-lookup"><span data-stu-id="0c13a-220">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="0c13a-221">Velg **Aktivert**, og velg deretter **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-221">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="0c13a-222">Hemmeligheten opprettes og legges til i Key Vault.</span><span class="sxs-lookup"><span data-stu-id="0c13a-222">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="0c13a-223">Gå til **Oversikt over Key Vault**, og noter deg DNS-navnet.</span><span class="sxs-lookup"><span data-stu-id="0c13a-223">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="0c13a-224">Opprett og registrer et Azure AD-program:</span><span class="sxs-lookup"><span data-stu-id="0c13a-224">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="0c13a-225">Gå til **Azure Active Directory** i [Azure-portalen](https://portal.azure.com), og velg deretter **Appregistreringer**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-225">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="0c13a-226">Velg **Ny programregistrering**, og angi verdier i følgende felter:</span><span class="sxs-lookup"><span data-stu-id="0c13a-226">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="0c13a-227">**Navn** – Angi navnet på appen.</span><span class="sxs-lookup"><span data-stu-id="0c13a-227">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="0c13a-228">**Programtype** – Velg **Web-API**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-228">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="0c13a-229">**Konfigurasjon av URI for omadressering** – Angi URL-adressen til Dynamics 365-forekomsten, for eksempel `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="0c13a-229">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="0c13a-230">Gå til appen du nettopp opprettet, og kopier og lagre verdien for **Program-ID (klient)**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-230">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="0c13a-231">Du må angi denne verdien senere når du konfigurerer nøkkelhvelvet.</span><span class="sxs-lookup"><span data-stu-id="0c13a-231">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="0c13a-232">Gå til **API-tillatelser**, og følg denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="0c13a-232">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="0c13a-233">Velg **Legg til en tillatelse**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-233">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="0c13a-234">Velg **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-234">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="0c13a-235">Etter at du har valgt delegerte tillatelser, velger du **user\_impersonation**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-235">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="0c13a-236">Velg **Legg til tillatelser**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-236">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="0c13a-237">På menyen for appen velger du **Sertifikater \& hemmeligheter**, og deretter følger du denne fremgangsmåten for å opprette Key Vault-hemmeligheter:</span><span class="sxs-lookup"><span data-stu-id="0c13a-237">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="0c13a-238">Velg **Ny klienthemmelighet**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-238">Select **New client secret**.</span></span>
        2. <span data-ttu-id="0c13a-239">Angi et navn i **Nøkkelbeskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0c13a-239">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="0c13a-240">Velg en varighet, og velg deretter **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-240">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="0c13a-241">Det genereres en hemmelighet i **Verdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0c13a-241">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="0c13a-242">Kopier og lagre den hemmelige verdien.</span><span class="sxs-lookup"><span data-stu-id="0c13a-242">Copy and save the secret value.</span></span>

4. <span data-ttu-id="0c13a-243">Opprett Key Vault-hemmeligheter:</span><span class="sxs-lookup"><span data-stu-id="0c13a-243">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="0c13a-244">Gå til nøkkelhvelvet du opprettet tidligere, og velg **Hemmeligheter**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-244">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="0c13a-245">Følg denne fremgangsmåten for hvert hemmelige navn i følgende tabell:</span><span class="sxs-lookup"><span data-stu-id="0c13a-245">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="0c13a-246">Velg **Generer/Importer**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-246">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="0c13a-247">I feltet **Opplastingsalternativer** i dialogboksen **Opprett en hemmelighet** velger du **Manuell**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-247">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="0c13a-248">Opprett det hemmelige navnet og verdien fra følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="0c13a-248">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="0c13a-249">Velg **Aktivert**, og velg deretter **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-249">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="0c13a-250">Hemmeligheten opprettes og legges til i Key Vault.</span><span class="sxs-lookup"><span data-stu-id="0c13a-250">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="0c13a-251">Hemmelig navn</span><span class="sxs-lookup"><span data-stu-id="0c13a-251">Secret name</span></span>                       | <span data-ttu-id="0c13a-252">Hemmelig verdi</span><span class="sxs-lookup"><span data-stu-id="0c13a-252">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="0c13a-253">app-id</span><span class="sxs-lookup"><span data-stu-id="0c13a-253">app-id</span></span>                            | <span data-ttu-id="0c13a-254">App-ID-en for programmet du opprettet tidligere</span><span class="sxs-lookup"><span data-stu-id="0c13a-254">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="0c13a-255">app-secret</span><span class="sxs-lookup"><span data-stu-id="0c13a-255">app-secret</span></span>                        | <span data-ttu-id="0c13a-256">Klienthemmeligheten du lagret tidligere</span><span class="sxs-lookup"><span data-stu-id="0c13a-256">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="0c13a-257">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="0c13a-257">storage-account-name</span></span>              | <span data-ttu-id="0c13a-258">Navnet på lagringskontoen du opprettet tidligere, for eksempel **lagringskonto1**</span><span class="sxs-lookup"><span data-stu-id="0c13a-258">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="0c13a-259">storage-account-connection-string</span><span class="sxs-lookup"><span data-stu-id="0c13a-259">storage-account-connection-string</span></span> | <span data-ttu-id="0c13a-260">Tilkoblingsstrengen du kopierte fra siden **Tilgangsnøkler** for lagringskontoen</span><span class="sxs-lookup"><span data-stu-id="0c13a-260">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="0c13a-261">Autoriser programmet for tilgang til nøkkelhvelvet:</span><span class="sxs-lookup"><span data-stu-id="0c13a-261">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="0c13a-262">Åpne nøkkelhvelvet du opprettet tidligere, i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="0c13a-262">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="0c13a-263">Velg tilgangspolicyene.</span><span class="sxs-lookup"><span data-stu-id="0c13a-263">Select the access policies.</span></span>
    3. <span data-ttu-id="0c13a-264">Følg denne fremgangsmåten for hvert program i følgende tabell:</span><span class="sxs-lookup"><span data-stu-id="0c13a-264">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="0c13a-265">Velg **Legg til tilgangspolicy** for å opprette en tilgangspolicy.</span><span class="sxs-lookup"><span data-stu-id="0c13a-265">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="0c13a-266">I feltet **Hemmelige tillatelser** velger du tillatelsene fra følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="0c13a-266">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="0c13a-267">I feltet **Velg sikkerhetskontohaver** søker du etter visningsnavnet for programmet i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="0c13a-267">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="0c13a-268">Velg **Velg**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-268">Select **Select**.</span></span>
        5. <span data-ttu-id="0c13a-269">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-269">Select **Add**.</span></span>
        6. <span data-ttu-id="0c13a-270">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-270">Select **Save**.</span></span>

        | <span data-ttu-id="0c13a-271">Søknad</span><span class="sxs-lookup"><span data-stu-id="0c13a-271">Application</span></span>                                              | <span data-ttu-id="0c13a-272">Tillatelser</span><span class="sxs-lookup"><span data-stu-id="0c13a-272">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="0c13a-273">Visningsnavnet for det nye programmet du opprettet</span><span class="sxs-lookup"><span data-stu-id="0c13a-273">The display name of the new application that you created</span></span> | <span data-ttu-id="0c13a-274">Hent, Vis</span><span class="sxs-lookup"><span data-stu-id="0c13a-274">Get, List</span></span>   |
        | <span data-ttu-id="0c13a-275">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="0c13a-275">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="0c13a-276">Hent, Vis</span><span class="sxs-lookup"><span data-stu-id="0c13a-276">Get, List</span></span>   |

6. <span data-ttu-id="0c13a-277">Tilordne roller for tilgang til lagringskontoen:</span><span class="sxs-lookup"><span data-stu-id="0c13a-277">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="0c13a-278">Åpne lagringskontoen du opprettet tidligere, i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="0c13a-278">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="0c13a-279">Velg **Tilgangskontroll (IAM)**, og velg deretter **Rolletilordninger**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-279">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="0c13a-280">Velg **Legg til, Legg til rolletilordning**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-280">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="0c13a-281">Følg denne fremgangsmåten for hvert program i følgende tabell:</span><span class="sxs-lookup"><span data-stu-id="0c13a-281">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="0c13a-282">Velg rollen fra følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="0c13a-282">Select the role from the following table.</span></span>
        2. <span data-ttu-id="0c13a-283">La feltet **Tilordne tilgang til** være satt til **Azure AD-bruker, -gruppe eller -tjenestekontohaver**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-283">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="0c13a-284">I **Velg**-feltet angir du programmet fra følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="0c13a-284">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="0c13a-285">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-285">Select **Save**.</span></span>

        | <span data-ttu-id="0c13a-286">Søknad</span><span class="sxs-lookup"><span data-stu-id="0c13a-286">Application</span></span>                                              | <span data-ttu-id="0c13a-287">Rolle</span><span class="sxs-lookup"><span data-stu-id="0c13a-287">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="0c13a-288">Visningsnavnet for det nye programmet du opprettet</span><span class="sxs-lookup"><span data-stu-id="0c13a-288">The display name of the new application that you created</span></span> | <span data-ttu-id="0c13a-289">Eier</span><span class="sxs-lookup"><span data-stu-id="0c13a-289">Owner</span></span>                       |
        | <span data-ttu-id="0c13a-290">Visningsnavnet for det nye programmet du opprettet</span><span class="sxs-lookup"><span data-stu-id="0c13a-290">The display name of the new application that you created</span></span> | <span data-ttu-id="0c13a-291">Bidragsyter</span><span class="sxs-lookup"><span data-stu-id="0c13a-291">Contributor</span></span>                 |
        | <span data-ttu-id="0c13a-292">Visningsnavnet for det nye programmet du opprettet</span><span class="sxs-lookup"><span data-stu-id="0c13a-292">The display name of the new application that you created</span></span> | <span data-ttu-id="0c13a-293">Bidragsyter for lagringskonto</span><span class="sxs-lookup"><span data-stu-id="0c13a-293">Storage Account Contributor</span></span> |
        | <span data-ttu-id="0c13a-294">Visningsnavnet for det nye programmet du opprettet</span><span class="sxs-lookup"><span data-stu-id="0c13a-294">The display name of the new application that you created</span></span> | <span data-ttu-id="0c13a-295">Eier av Storage Blob Data</span><span class="sxs-lookup"><span data-stu-id="0c13a-295">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="0c13a-296">**AI Builder Authorization Service**</span><span class="sxs-lookup"><span data-stu-id="0c13a-296">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="0c13a-297">Leser for Storage Blob Data</span><span class="sxs-lookup"><span data-stu-id="0c13a-297">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="0c13a-298">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="0c13a-298">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}

```
---



## <a name="configure-the-data-lake"></a><span data-ttu-id="0c13a-299">Konfigurere datasjøen</span><span class="sxs-lookup"><span data-stu-id="0c13a-299">Configure the data lake</span></span>

<span data-ttu-id="0c13a-300">Følg denne fremgangsmåten for å bruke LCS til å legge til tillegget Azure Data Lake i miljøet.</span><span class="sxs-lookup"><span data-stu-id="0c13a-300">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="0c13a-301">Logg på LCS, og velg deretter **Detaljerte opplysninger** under miljønavnet til høyre på siden.</span><span class="sxs-lookup"><span data-stu-id="0c13a-301">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="0c13a-302">I delen **Miljøtillegg** velger du **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-302">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="0c13a-303">Velg tillegget **Eksporter til Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-303">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="0c13a-304">Angi følgende verdier.</span><span class="sxs-lookup"><span data-stu-id="0c13a-304">Enter the following values.</span></span>

    | <span data-ttu-id="0c13a-305">Verdi</span><span class="sxs-lookup"><span data-stu-id="0c13a-305">Value</span></span>                                                              | <span data-ttu-id="0c13a-306">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0c13a-306">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="0c13a-307">Leier-ID-en for Azure-abonnementet der Key Vault er</span><span class="sxs-lookup"><span data-stu-id="0c13a-307">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="0c13a-308">Leier-ID-en der lagringskontoen, appene og nøkkelhvelvene er.</span><span class="sxs-lookup"><span data-stu-id="0c13a-308">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="0c13a-309">Du finner denne verdien ved å åpne [Azure-portalen](https://portal.azure.com), gå til **Azure Active Directory** og kopiere verdien for **Leier-ID**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-309">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="0c13a-310">Oppgi DNS-navnet for Key Vault</span><span class="sxs-lookup"><span data-stu-id="0c13a-310">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="0c13a-311">DNS-navnet for nøkkelhvelvet, for eksempel `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="0c13a-311">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="0c13a-312">(Denne verdien samsvarer med DNS-navnet som brukes i enhetslageret.)</span><span class="sxs-lookup"><span data-stu-id="0c13a-312">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="0c13a-313">Angi hemmeligheten som inneholder navnet på lagringskontoen</span><span class="sxs-lookup"><span data-stu-id="0c13a-313">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="0c13a-314">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="0c13a-314">**storage-account-name**</span></span> |
    | <span data-ttu-id="0c13a-315">Hemmelig navn på app-ID-en som skal brukes til å få tilgang til Data Lake</span><span class="sxs-lookup"><span data-stu-id="0c13a-315">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="0c13a-316">**app-id**</span><span class="sxs-lookup"><span data-stu-id="0c13a-316">**app-id**</span></span> |
    | <span data-ttu-id="0c13a-317">Hemmelig navn som skal brukes med app-ID-en</span><span class="sxs-lookup"><span data-stu-id="0c13a-317">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="0c13a-318">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="0c13a-318">**app-secret**</span></span> |

5. <span data-ttu-id="0c13a-319">Godta vilkårene, og velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-319">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="0c13a-320">Tillegget installeres innen noen minutter.</span><span class="sxs-lookup"><span data-stu-id="0c13a-320">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="0c13a-321">Konfigurere AI Builder</span><span class="sxs-lookup"><span data-stu-id="0c13a-321">Configure AI Builder</span></span>

1. <span data-ttu-id="0c13a-322">Logg på LCS, og åpne siden **Miljødetaljer**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-322">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="0c13a-323">Bla til delen **Miljøtillegg**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-323">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="0c13a-324">Du skal kunne se tilleggene som allerede er installert i dette miljøet.</span><span class="sxs-lookup"><span data-stu-id="0c13a-324">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="0c13a-325">Hvis tillegget **Eksporter til Data Lake** ikke er blant dem, konfigurerer du dette tillegget.</span><span class="sxs-lookup"><span data-stu-id="0c13a-325">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="0c13a-326">Velg tillegget **Få innsikt**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-326">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="0c13a-327">Angi følgende verdier på siden med detaljer for tillegget **Få innsikt**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-327">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="0c13a-328">Verdi</span><span class="sxs-lookup"><span data-stu-id="0c13a-328">Value</span></span>                                                    | <span data-ttu-id="0c13a-329">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0c13a-329">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="0c13a-330">URL-adresse for CDS-organisasjon</span><span class="sxs-lookup"><span data-stu-id="0c13a-330">CDS Organization URL</span></span>                                     | <span data-ttu-id="0c13a-331">URL-adressen for Dataverse kopiert fra oppføringen over.</span><span class="sxs-lookup"><span data-stu-id="0c13a-331">The Dataverse organization URL copied from above.</span></span> |
    | <span data-ttu-id="0c13a-332">ID for CDS-organisasjon</span><span class="sxs-lookup"><span data-stu-id="0c13a-332">CDS Org ID</span></span>                                               | <span data-ttu-id="0c13a-333">ID-en for Dataverse kopiert fra oppføringen over.</span><span class="sxs-lookup"><span data-stu-id="0c13a-333">The Dataverse organization ID copied from above.</span></span> |
5. <span data-ttu-id="0c13a-334">Aktiver **Er dette standardmiljø for leieren din**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-334">Enable **Is this the default environment for you Tenant**.</span></span>
    
## <a name="configure-the-entity-store"></a><span data-ttu-id="0c13a-335">Konfigurere enhetslageret</span><span class="sxs-lookup"><span data-stu-id="0c13a-335">Configure the entity store</span></span>

<span data-ttu-id="0c13a-336">Følg denne fremgangsmåten for å konfigurere enhetslageret i Finance-miljøet ditt.</span><span class="sxs-lookup"><span data-stu-id="0c13a-336">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="0c13a-337">Gå til **Systemadministrasjon \> Oppsett \> Systemparametere \> Datatilkoblinger**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-337">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="0c13a-338">Angi verdier i følgende Key Vault-felter:</span><span class="sxs-lookup"><span data-stu-id="0c13a-338">Set the following key vault fields:</span></span>

    - <span data-ttu-id="0c13a-339">**Program-ID (klient)** – Angi programklient-ID-en du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="0c13a-339">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="0c13a-340">**Programhemmelighet** – Angi hemmeligheten du lagret for programmet du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="0c13a-340">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="0c13a-341">**DNS-navn** – Du kan finne DNS-navnet (Domain Name System) på siden for programdetaljer for programmet du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="0c13a-341">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="0c13a-342">**Hemmelig navn** – Angi **storage-account-connection-string**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-342">**Secret name** – Enter **storage-account-connection-string**.</span></span>
3. <span data-ttu-id="0c13a-343">Aktiver **Aktiver Data Lake-integrasjon**.</span><span class="sxs-lookup"><span data-stu-id="0c13a-343">Enable **Enable Data Lake integration**.</span></span>
4. <span data-ttu-id="0c13a-344">Velg **Test Azure Key Vault**, og kontroller at det ikke er noen feil.</span><span class="sxs-lookup"><span data-stu-id="0c13a-344">Select **Test Azure Key Vault** and verify there are no errors.</span></span>
5. <span data-ttu-id="0c13a-345">Velg **Test Azure storage**, og kontroller at det ikke er noen feil.</span><span class="sxs-lookup"><span data-stu-id="0c13a-345">Select **Test Azure storage** and verify there are no errors.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="0c13a-346">Tilbakemelding og støtte</span><span class="sxs-lookup"><span data-stu-id="0c13a-346">Feedback and support</span></span>

<span data-ttu-id="0c13a-347">Send en e-postmelding til [Innsikt i kundebetaling (forhåndsversjon)](mailto:fiap@microsoft.com) hvis du er interessert i å gi tilbakemelding eller trenger støtte.</span><span class="sxs-lookup"><span data-stu-id="0c13a-347">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="0c13a-348">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="0c13a-348">Privacy notice</span></span>

<span data-ttu-id="0c13a-349">Forhåndsversjoner (1) kan ha redusert personvern og færre sikkerhetstiltak enn Dynamics 365 Finance and Operations-tjenesten, (2) er ikke inkludert i serviceavtalen (SLA) for denne tjenesten, (3) må ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) har begrenset støtte.</span><span class="sxs-lookup"><span data-stu-id="0c13a-349">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
