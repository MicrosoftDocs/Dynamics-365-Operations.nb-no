---
title: Konfigurasjon for Finance Insights – versjoner opptil 10.0.19
description: Dette emnet forklarer konfigurasjonstrinnene som gjør at systemet kan bruke funksjonene i Finance Insights for versjoner opptil 10.0.19.
author: ShivamPandey-msft
ms.date: 06/03/2021
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
ms.openlocfilehash: 6ad06bb6d041fc060b3a99538f6d4d0af333180f
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186426"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="1e149-103">Konfigurasjon for Finance Insights (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="1e149-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="1e149-104">Følgende fremgangsmåter for å konfigurere Finance Insights er gyldige for Microsoft Dynamics 365 Finance-versjoner opptil 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="1e149-104">The following procedures for setting up Finance insights are valid for Microsoft Dynamics 365 Finance versions up to 10.0.19.</span></span> <span data-ttu-id="1e149-105">Hvis du vil konfigurere Finance Insights i versjon 10.0.20 og nyere, kan du se [Konfigurasjon for Finance Insights (forhåndsversjon) – versjon 10.0.20 og nyere](configure-for-fin-insites-PubPrvw.md).</span><span class="sxs-lookup"><span data-stu-id="1e149-105">To set up Finance insights on version 10.0.20 and later, see [Configuration for Finance Insights (preview) - versions 10.0.20 and beyond](configure-for-fin-insites-PubPrvw.md).</span></span>

<span data-ttu-id="1e149-106">Finance Insights kombinerer funksjonalitet fra Microsoft Dynamics 365 Finance med Microsoft Dataverse, Azure og AI Builder for å gi organisasjonen kraftige prognoseverktøy.</span><span class="sxs-lookup"><span data-stu-id="1e149-106">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="1e149-107">Dette emnet forklarer konfigurasjonstrinnene som gjør at systemet kan bruke funksjonene i Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="1e149-107">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="1e149-108">Klargjøre Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="1e149-108">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="1e149-109">Klargjør miljøene ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="1e149-109">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="1e149-110">Opprett eller oppdater et Dynamics 365 Finance-miljø i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="1e149-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="1e149-111">Miljøet krever appversjon 10.0.11 / Platform update 35 eller senere.</span><span class="sxs-lookup"><span data-stu-id="1e149-111">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="1e149-112">Miljøet må være et miljø med høy tilgjengelighet i sandkassemodus.</span><span class="sxs-lookup"><span data-stu-id="1e149-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="1e149-113">(Denne typen miljø kalles også et miljø på lag 2.) Hvis du vil ha mer informasjon, kan du se [Miljøplanlegging](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="1e149-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="1e149-114">Hvis du konfigurerer Finance Insights i et sandkassemiljø, må du kanskje kopiere produksjonsdata til dette miljøet for at prediksjoner skal kunne fungere.</span><span class="sxs-lookup"><span data-stu-id="1e149-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="1e149-115">Prediksjonsmodellen bruker flere år med data til å bygge prediksjoner.</span><span class="sxs-lookup"><span data-stu-id="1e149-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="1e149-116">Contoso-demodataene inneholder ikke nok historiske data til at prediksjonsmodellen kan læres opp tilstrekkelig.</span><span class="sxs-lookup"><span data-stu-id="1e149-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="1e149-117">Konfigurer Dataverse</span><span class="sxs-lookup"><span data-stu-id="1e149-117">Configure Dataverse</span></span>

<span data-ttu-id="1e149-118">Bruk fremgangsmåten nedenfor til å konfigurere Dataverse for Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="1e149-118">Use the following steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="1e149-119">Åpne miljøsiden i LCS, og kontroller at **Power Platform-integrering** allerede er satt opp.</span><span class="sxs-lookup"><span data-stu-id="1e149-119">Open the environment page in LCS and verify that the **Power Platform Integration** section is already setup.</span></span>
    1. <span data-ttu-id="1e149-120">Hvis det allerede er satt opp, skal Dataverse-miljønavnet som er koblet til Dynamics 365 Finance-miljøet, vises.</span><span class="sxs-lookup"><span data-stu-id="1e149-120">If it is already set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="1e149-121">Kopier Dataverse-miljønavnet.</span><span class="sxs-lookup"><span data-stu-id="1e149-121">Copy the Dataverse environment name.</span></span>
    2. <span data-ttu-id="1e149-122">Hvis det ikke er definert, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="1e149-122">If it is not set up, follow these steps:</span></span>
        1. <span data-ttu-id="1e149-123">Velg **Oppsett**-knappen i Power Platform-integreringsdelen.</span><span class="sxs-lookup"><span data-stu-id="1e149-123">Select the **Setup** button in the Power Platform Integration section.</span></span> <span data-ttu-id="1e149-124">Det kan ta opptil en time før miljøet er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="1e149-124">It may take up to an hour for the environment to be set up.</span></span>
        2. <span data-ttu-id="1e149-125">Hvis Dataverse-miljøet er konfigurert riktig, skal Dataverse-miljøetnavnet som er koblet til Dynamics 365 Finance-miljøet, vises.</span><span class="sxs-lookup"><span data-stu-id="1e149-125">If the Dataverse environment is successfully set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="1e149-126">Kopier Dataverse-miljønavnet.</span><span class="sxs-lookup"><span data-stu-id="1e149-126">Copy the Dataverse environment name.</span></span>
> [!NOTE]
> <span data-ttu-id="1e149-127">Når du har fullført miljøoppsettet, må du **IKKE** velge knappen **Kobling til CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="1e149-127">After completing the environment set up, **DO NOT** select the **Link to CDS for Apps** button.</span></span> <span data-ttu-id="1e149-128">Dette er ikke nødvendig for Finance Insights og vil deaktivere muligheten til å fullføre de nødvendige miljøtilleggene i LCS.</span><span class="sxs-lookup"><span data-stu-id="1e149-128">This is not needed for Finance Insights and will disable the ability to complete the required Environment Add-ins in LCS.</span></span>

2. <span data-ttu-id="1e149-129">Åpne [administrasjonssenteret for Power Platform](https://admin.powerplatform.microsoft.com/), og følg denne fremgangsmåten for å opprette et nytt Dataverse-miljø i den samme Active Directory-leieren:</span><span class="sxs-lookup"><span data-stu-id="1e149-129">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="1e149-130">Åpne **Miljøer**-siden.</span><span class="sxs-lookup"><span data-stu-id="1e149-130">Open the **Environments** page.</span></span>

        <span data-ttu-id="1e149-131">[![Miljøer-siden](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="1e149-131">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="1e149-132">Velg Dataverse-miljøet som opprettes over, og velg deretter **Innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="1e149-132">Select the Dataverse environment created above and then select **Settings**.</span></span>
    3. <span data-ttu-id="1e149-133">Velg **Ressurser \> Alle eldre innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="1e149-133">Select **Resources \> All Legacy Settings**.</span></span>
    4. <span data-ttu-id="1e149-134">Velg **Innstillinger** i det øverste navigasjonsfeltet, og velg deretter **Tilpassinger**.</span><span class="sxs-lookup"><span data-stu-id="1e149-134">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    5. <span data-ttu-id="1e149-135">Velg **Utviklerressurser**.</span><span class="sxs-lookup"><span data-stu-id="1e149-135">Select **Developer Resources**.</span></span>
    6. <span data-ttu-id="1e149-136">Kopier verdien for **Dataverse-organisasjons-ID**.</span><span class="sxs-lookup"><span data-stu-id="1e149-136">Copy the **Dataverse organization ID** value.</span></span>
    7. <span data-ttu-id="1e149-137">Noter deg URL-adressen for Dataverse-organisasjonen på adresselinjen i nettleseren.</span><span class="sxs-lookup"><span data-stu-id="1e149-137">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="1e149-138">URL-adressen kan for eksempel være `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="1e149-138">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

3. <span data-ttu-id="1e149-139">Hvis du har tenkt å bruke funksjonen Kontantstrømprognoser eller Budsjettprognoser, følger du disse trinnene for å oppdatere merknadsgrensen for organisasjonen til minst 50 megabyte (MB):</span><span class="sxs-lookup"><span data-stu-id="1e149-139">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="1e149-140">Åpne [Power Apps-portalen](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="1e149-140">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="1e149-141">Velg miljøet du nettopp opprettet, og velg deretter **Avanserte innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="1e149-141">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="1e149-142">Velg **Innstillinger \> E-postkonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="1e149-142">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="1e149-143">Endre verdien i feltet **Maksimal filstørrelse** til **51 200**.</span><span class="sxs-lookup"><span data-stu-id="1e149-143">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="1e149-144">(Verdien uttrykkes i kilobyte \[kB\].)</span><span class="sxs-lookup"><span data-stu-id="1e149-144">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="1e149-145">Velg **OK** for å lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="1e149-145">Select **OK** to save your changes.</span></span>

## <a name="configure-the-azure-setup"></a><span data-ttu-id="1e149-146">Konfigurere Azure-oppsettet</span><span class="sxs-lookup"><span data-stu-id="1e149-146">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="1e149-147">Angi katalog-ID-en for Dataverse og brukerens objekt-ID for Azure AD</span><span class="sxs-lookup"><span data-stu-id="1e149-147">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="1e149-148">Angi katalog-ID-en for Dataverse:</span><span class="sxs-lookup"><span data-stu-id="1e149-148">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="1e149-149">Åpne [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="1e149-149">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="1e149-150">Logg på ved å bruke bruker-ID-en som ble brukt til å opprette Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="1e149-150">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="1e149-151">Gå til **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="1e149-151">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="1e149-152">Kopier verdien for **Leier-ID**.</span><span class="sxs-lookup"><span data-stu-id="1e149-152">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="1e149-153">Angi brukerens objekt-ID for Azure Active Directory (Azure AD):</span><span class="sxs-lookup"><span data-stu-id="1e149-153">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="1e149-154">Gå til **Brukere** i [Azure-portalen](https://portal.azure.com), og søk etter brukeren etter e-postadresse.</span><span class="sxs-lookup"><span data-stu-id="1e149-154">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="1e149-155">Velg brukerens navn.</span><span class="sxs-lookup"><span data-stu-id="1e149-155">Select the user's name.</span></span>
    3. <span data-ttu-id="1e149-156">Kopier verdien for **Objekt-ID**.</span><span class="sxs-lookup"><span data-stu-id="1e149-156">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="1e149-157">Bruke Azure Cloud Shell til å konfigurere Data Lake-ressurser for Finance Insights</span><span class="sxs-lookup"><span data-stu-id="1e149-157">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="1e149-158">Bruke et Windows PowerShell-skript</span><span class="sxs-lookup"><span data-stu-id="1e149-158">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="1e149-159">Et Windows PowerShell-skript er oppgitt, slik at du lett kan konfigurere Azure-ressursene som er beskrevet i [Konfigurere eksport til Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="1e149-159">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="1e149-160">Hvis du foretrekker å konfigurere manuelt, kan du hoppe over denne fremgangsmåten og fortsette med fremgangsmåten i delen [Manuell konfigurasjon](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="1e149-160">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="1e149-161">Følg fremgangsmåten nedenfor for å kjøre PowerShell-skriptet.</span><span class="sxs-lookup"><span data-stu-id="1e149-161">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="1e149-162">Det kan hende at Azure CLI-alternativet «Prøv det» eller å kjøre skriptet på PC-en ikke fungerer.</span><span class="sxs-lookup"><span data-stu-id="1e149-162">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="1e149-163">Følg denne fremgangsmåten for å konfigurere Azure ved hjelp av Windows PowerShell-skriptet.</span><span class="sxs-lookup"><span data-stu-id="1e149-163">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="1e149-164">Du må ha rettigheter til å opprette en Azure-ressursgruppe, Azure-ressurser og et Azure AD-program.</span><span class="sxs-lookup"><span data-stu-id="1e149-164">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="1e149-165">Hvis du vil ha informasjon om de nødvendige tillatelsene, kan du se [Kontrollere Azure AD-tillatelser](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="1e149-165">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="1e149-166">I [Azure-portalen](https://portal.azure.com) går du til Azure-målabonnementet.</span><span class="sxs-lookup"><span data-stu-id="1e149-166">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="1e149-167">Velg **Cloud Shell**-knappen til høyre for **Søk**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1e149-167">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="1e149-168">Velg **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="1e149-168">Select **PowerShell**.</span></span>
3. <span data-ttu-id="1e149-169">Opprett lagringsplass hvis du blir bedt om det.</span><span class="sxs-lookup"><span data-stu-id="1e149-169">Create storage if you're prompted to do so.</span></span>
4. <span data-ttu-id="1e149-170">Gå til kategorien **Azure CLI** og velg **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="1e149-170">Go to the **Azure CLI** tab and select **Copy**.</span></span>  
5. <span data-ttu-id="1e149-171">Åpne Notisblokk, og lim inn PowerShell-skriptet.</span><span class="sxs-lookup"><span data-stu-id="1e149-171">Open Notepad and paste the PowerShell script.</span></span> <span data-ttu-id="1e149-172">Lagre filen som ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="1e149-172">Save the file as ConfigureDataLake.ps1.</span></span>
6. <span data-ttu-id="1e149-173">Last opp Windows PowerShell-skriptet til økten ved hjelp av menyalternativet for opplasting i Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="1e149-173">Upload the Windows PowerShell script to the session using the menu option for upload in Cloud Shell.</span></span>
7. <span data-ttu-id="1e149-174">Kjør skriptet .\ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="1e149-174">Run the script .\ConfigureDataLake.ps1.</span></span>
8. <span data-ttu-id="1e149-175">Følg instruksjonene for å kjøre skriptet.</span><span class="sxs-lookup"><span data-stu-id="1e149-175">Follow the prompts to run the script.</span></span>
9. <span data-ttu-id="1e149-176">Bruk informasjonen fra skriptutdataene til å installere tillegget **Eksporter til Data Lake** i LCS.</span><span class="sxs-lookup"><span data-stu-id="1e149-176">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
10. <span data-ttu-id="1e149-177">Bruk informasjonen fra skriptutdataene til å aktivere enhetslageret på **Datatilkoblinger**-siden i Finance (**Systemadministrasjon \> Systemparametere \> Datatilkoblinger**).</span><span class="sxs-lookup"><span data-stu-id="1e149-177">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="1e149-178">Manuell konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="1e149-178">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="1e149-179">Legg til programmer i Azure AD-leieren</span><span class="sxs-lookup"><span data-stu-id="1e149-179">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="1e149-180">Gå til **Azure Active Directory** i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="1e149-180">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="1e149-181">Velg **Behandle \> Enterprise-programmer**.</span><span class="sxs-lookup"><span data-stu-id="1e149-181">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="1e149-182">Søk etter følgende programmer etter app-ID.</span><span class="sxs-lookup"><span data-stu-id="1e149-182">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="1e149-183">Program</span><span class="sxs-lookup"><span data-stu-id="1e149-183">Application</span></span>                              | <span data-ttu-id="1e149-184">App-ID</span><span class="sxs-lookup"><span data-stu-id="1e149-184">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="1e149-185">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="1e149-185">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="1e149-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="1e149-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="1e149-187">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="1e149-187">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="1e149-188">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="1e149-188">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="1e149-189">AI Builder Authorization Service</span><span class="sxs-lookup"><span data-stu-id="1e149-189">AI Builder Authorization Service</span></span>         | <span data-ttu-id="1e149-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="1e149-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="1e149-191">Hvis du ikke finner noen av de ovennevnte programmene, kan du prøve følgende trinn.</span><span class="sxs-lookup"><span data-stu-id="1e149-191">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="1e149-192">Velg **Start**-menyen på den lokale maskinen, og søk etter **powershell**.</span><span class="sxs-lookup"><span data-stu-id="1e149-192">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="1e149-193">Velg og hold (eller høyreklikk på) **Windows PowerShell**, og velg deretter **Kjør som administrator**.</span><span class="sxs-lookup"><span data-stu-id="1e149-193">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="1e149-194">Kjør følgende kommando for å installere **AzureAD**-modulen.</span><span class="sxs-lookup"><span data-stu-id="1e149-194">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="1e149-195">Hvis en NuGet-leverandør kreves for å fortsette, velger du **J** for å installere den.</span><span class="sxs-lookup"><span data-stu-id="1e149-195">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="1e149-196">Hvis det vises en melding om at repositoriet ikke er klarert, velger du **J** for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="1e149-196">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="1e149-197">For hvert program som må legges til, kjører du følgende kommandoer for å legge til programmet i Azure AD.</span><span class="sxs-lookup"><span data-stu-id="1e149-197">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="1e149-198">Når du blir bedt om det, logger du på som Azure AD-administrator.</span><span class="sxs-lookup"><span data-stu-id="1e149-198">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="1e149-199">Opprette Azure-ressurser</span><span class="sxs-lookup"><span data-stu-id="1e149-199">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="1e149-200">Kontroller at du oppretter følgende ressurser i samme Azure AD-forekomst som Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="1e149-200">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="1e149-201">Du kan ikke bruke ressurser fra en annen Azure AD-forekomst.</span><span class="sxs-lookup"><span data-stu-id="1e149-201">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="1e149-202">Opprette en ny lagringskonto:</span><span class="sxs-lookup"><span data-stu-id="1e149-202">Create a new storage account:</span></span>

    1. <span data-ttu-id="1e149-203">Opprett en lagringskonto i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="1e149-203">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="1e149-204">I dialogboksen **Opprett lagringskonto** angir du verdier i følgende felter:</span><span class="sxs-lookup"><span data-stu-id="1e149-204">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="1e149-205">**Plassering** – Velg datasenteret der miljøet er plassert.</span><span class="sxs-lookup"><span data-stu-id="1e149-205">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="1e149-206">**Ytelse** – Vi anbefaler at du velger **Standard**.</span><span class="sxs-lookup"><span data-stu-id="1e149-206">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="1e149-207">**Kontotype** – Du må velge **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="1e149-207">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="1e149-208">Velg **Aktiver** under funksjonen **Hierarkiske navneområder** for alternativet **Data Lake Storage Gen2** i dialogboksen **Avanserte alternativer**.</span><span class="sxs-lookup"><span data-stu-id="1e149-208">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="1e149-209">Hvis du deaktiverer denne funksjonen, kan du ikke bruke data som Finance and Operations-apper skriver ved hjelp av tjenester som Power BI-dataflyter.</span><span class="sxs-lookup"><span data-stu-id="1e149-209">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="1e149-210">Velg **Se gjennom og opprett**.</span><span class="sxs-lookup"><span data-stu-id="1e149-210">Select **Review and create**.</span></span> <span data-ttu-id="1e149-211">Når distribusjonen er fullført, vises den nye ressursen i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="1e149-211">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="1e149-212">Gå til lagringskontoen du opprettet.</span><span class="sxs-lookup"><span data-stu-id="1e149-212">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="1e149-213">Velg **Tilgangsnøkler** på menyen til venstre.</span><span class="sxs-lookup"><span data-stu-id="1e149-213">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="1e149-214">Kopier og lagre tilkoblingsstrengen for **Nøkkel1** eller **Nøkkel2**.</span><span class="sxs-lookup"><span data-stu-id="1e149-214">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="1e149-215">Kopier og lagre navnet på lagringskontoen.</span><span class="sxs-lookup"><span data-stu-id="1e149-215">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="1e149-216">Opprett et nytt nøkkelhvelv:</span><span class="sxs-lookup"><span data-stu-id="1e149-216">Create a new key vault:</span></span>

    1. <span data-ttu-id="1e149-217">Opprett et nøkkelhvelv i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="1e149-217">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="1e149-218">I **Plassering**-feltet i dialogboksen **Opprett nøkkelhvelv** velger du datasenteret der miljøet er.</span><span class="sxs-lookup"><span data-stu-id="1e149-218">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="1e149-219">Etter at nøkkelhvelvet er opprettet, velger du det i listen og velger deretter **Hemmeligheter**.</span><span class="sxs-lookup"><span data-stu-id="1e149-219">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="1e149-220">Velg **Generer/Importer**.</span><span class="sxs-lookup"><span data-stu-id="1e149-220">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="1e149-221">I feltet **Opplastingsalternativer** i dialogboksen **Opprett en hemmelighet** velger du **Manuell**.</span><span class="sxs-lookup"><span data-stu-id="1e149-221">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="1e149-222">Angi et navn for hemmeligheten.</span><span class="sxs-lookup"><span data-stu-id="1e149-222">Enter a name for the secret.</span></span> <span data-ttu-id="1e149-223">Noter deg navnet, fordi du må angi det senere.</span><span class="sxs-lookup"><span data-stu-id="1e149-223">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="1e149-224">I **Verdi**-feltet angir du tilkoblingsstrengen du fikk fra lagringskontoen i forrige fremgangsmåte.</span><span class="sxs-lookup"><span data-stu-id="1e149-224">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="1e149-225">Velg **Aktivert**, og velg deretter **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="1e149-225">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="1e149-226">Hemmeligheten opprettes og legges til i Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1e149-226">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="1e149-227">Gå til **Oversikt over Key Vault**, og noter deg DNS-navnet.</span><span class="sxs-lookup"><span data-stu-id="1e149-227">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="1e149-228">Opprett og registrer et Azure AD-program:</span><span class="sxs-lookup"><span data-stu-id="1e149-228">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="1e149-229">Gå til **Azure Active Directory** i [Azure-portalen](https://portal.azure.com), og velg deretter **Appregistreringer**.</span><span class="sxs-lookup"><span data-stu-id="1e149-229">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="1e149-230">Velg **Ny programregistrering**, og angi verdier i følgende felter:</span><span class="sxs-lookup"><span data-stu-id="1e149-230">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="1e149-231">**Navn** – Angi navnet på appen.</span><span class="sxs-lookup"><span data-stu-id="1e149-231">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="1e149-232">**Programtype** – Velg **Web-API**.</span><span class="sxs-lookup"><span data-stu-id="1e149-232">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="1e149-233">**Konfigurasjon av URI for omadressering** – Angi URL-adressen til Dynamics 365-forekomsten, for eksempel `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="1e149-233">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="1e149-234">Gå til appen du nettopp opprettet, og kopier og lagre verdien for **Program-ID (klient)**.</span><span class="sxs-lookup"><span data-stu-id="1e149-234">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="1e149-235">Du må angi denne verdien senere når du konfigurerer nøkkelhvelvet.</span><span class="sxs-lookup"><span data-stu-id="1e149-235">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="1e149-236">Gå til **API-tillatelser**, og følg denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="1e149-236">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="1e149-237">Velg **Legg til en tillatelse**.</span><span class="sxs-lookup"><span data-stu-id="1e149-237">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="1e149-238">Velg **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="1e149-238">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="1e149-239">Etter at du har valgt delegerte tillatelser, velger du **user\_impersonation**.</span><span class="sxs-lookup"><span data-stu-id="1e149-239">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="1e149-240">Velg **Legg til tillatelser**.</span><span class="sxs-lookup"><span data-stu-id="1e149-240">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="1e149-241">På menyen for appen velger du **Sertifikater \& hemmeligheter**, og deretter følger du denne fremgangsmåten for å opprette Key Vault-hemmeligheter:</span><span class="sxs-lookup"><span data-stu-id="1e149-241">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="1e149-242">Velg **Ny klienthemmelighet**.</span><span class="sxs-lookup"><span data-stu-id="1e149-242">Select **New client secret**.</span></span>
        2. <span data-ttu-id="1e149-243">Angi et navn i **Nøkkelbeskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1e149-243">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="1e149-244">Velg en varighet, og velg deretter **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="1e149-244">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="1e149-245">Det genereres en hemmelighet i **Verdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1e149-245">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="1e149-246">Kopier og lagre den hemmelige verdien.</span><span class="sxs-lookup"><span data-stu-id="1e149-246">Copy and save the secret value.</span></span>

4. <span data-ttu-id="1e149-247">Opprett Key Vault-hemmeligheter:</span><span class="sxs-lookup"><span data-stu-id="1e149-247">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="1e149-248">Gå til nøkkelhvelvet du opprettet tidligere, og velg **Hemmeligheter**.</span><span class="sxs-lookup"><span data-stu-id="1e149-248">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="1e149-249">Følg denne fremgangsmåten for hvert hemmelige navn i følgende tabell:</span><span class="sxs-lookup"><span data-stu-id="1e149-249">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="1e149-250">Velg **Generer/Importer**.</span><span class="sxs-lookup"><span data-stu-id="1e149-250">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="1e149-251">I feltet **Opplastingsalternativer** i dialogboksen **Opprett en hemmelighet** velger du **Manuell**.</span><span class="sxs-lookup"><span data-stu-id="1e149-251">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="1e149-252">Opprett det hemmelige navnet og verdien fra følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="1e149-252">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="1e149-253">Velg **Aktivert**, og velg deretter **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="1e149-253">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="1e149-254">Hemmeligheten opprettes og legges til i Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1e149-254">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="1e149-255">Hemmelig navn</span><span class="sxs-lookup"><span data-stu-id="1e149-255">Secret name</span></span>                       | <span data-ttu-id="1e149-256">Hemmelig verdi</span><span class="sxs-lookup"><span data-stu-id="1e149-256">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="1e149-257">app-id</span><span class="sxs-lookup"><span data-stu-id="1e149-257">app-id</span></span>                            | <span data-ttu-id="1e149-258">App-ID-en for programmet du opprettet tidligere</span><span class="sxs-lookup"><span data-stu-id="1e149-258">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="1e149-259">app-secret</span><span class="sxs-lookup"><span data-stu-id="1e149-259">app-secret</span></span>                        | <span data-ttu-id="1e149-260">Klienthemmeligheten du lagret tidligere</span><span class="sxs-lookup"><span data-stu-id="1e149-260">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="1e149-261">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="1e149-261">storage-account-name</span></span>              | <span data-ttu-id="1e149-262">Navnet på lagringskontoen du opprettet tidligere, for eksempel **lagringskonto1**</span><span class="sxs-lookup"><span data-stu-id="1e149-262">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="1e149-263">storage-account-connection-string</span><span class="sxs-lookup"><span data-stu-id="1e149-263">storage-account-connection-string</span></span> | <span data-ttu-id="1e149-264">Tilkoblingsstrengen du kopierte fra siden **Tilgangsnøkler** for lagringskontoen</span><span class="sxs-lookup"><span data-stu-id="1e149-264">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="1e149-265">Autoriser programmet for tilgang til nøkkelhvelvet:</span><span class="sxs-lookup"><span data-stu-id="1e149-265">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="1e149-266">Åpne nøkkelhvelvet du opprettet tidligere, i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="1e149-266">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="1e149-267">Velg tilgangspolicyene.</span><span class="sxs-lookup"><span data-stu-id="1e149-267">Select the access policies.</span></span>
    3. <span data-ttu-id="1e149-268">Følg denne fremgangsmåten for hvert program i følgende tabell:</span><span class="sxs-lookup"><span data-stu-id="1e149-268">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="1e149-269">Velg **Legg til tilgangspolicy** for å opprette en tilgangspolicy.</span><span class="sxs-lookup"><span data-stu-id="1e149-269">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="1e149-270">I feltet **Hemmelige tillatelser** velger du tillatelsene fra følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="1e149-270">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="1e149-271">I feltet **Velg sikkerhetskontohaver** søker du etter visningsnavnet for programmet i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="1e149-271">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="1e149-272">Velg **Velg**.</span><span class="sxs-lookup"><span data-stu-id="1e149-272">Select **Select**.</span></span>
        5. <span data-ttu-id="1e149-273">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="1e149-273">Select **Add**.</span></span>
        6. <span data-ttu-id="1e149-274">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="1e149-274">Select **Save**.</span></span>

        | <span data-ttu-id="1e149-275">Søknad</span><span class="sxs-lookup"><span data-stu-id="1e149-275">Application</span></span>                                              | <span data-ttu-id="1e149-276">Tillatelser</span><span class="sxs-lookup"><span data-stu-id="1e149-276">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="1e149-277">Visningsnavnet for det nye programmet du opprettet</span><span class="sxs-lookup"><span data-stu-id="1e149-277">The display name of the new application that you created</span></span> | <span data-ttu-id="1e149-278">Hent, Vis</span><span class="sxs-lookup"><span data-stu-id="1e149-278">Get, List</span></span>   |
        | <span data-ttu-id="1e149-279">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="1e149-279">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="1e149-280">Hent, Vis</span><span class="sxs-lookup"><span data-stu-id="1e149-280">Get, List</span></span>   |

6. <span data-ttu-id="1e149-281">Tilordne roller for tilgang til lagringskontoen:</span><span class="sxs-lookup"><span data-stu-id="1e149-281">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="1e149-282">Åpne lagringskontoen du opprettet tidligere, i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="1e149-282">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="1e149-283">Velg **Tilgangskontroll (IAM)**, og velg deretter **Rolletilordninger**.</span><span class="sxs-lookup"><span data-stu-id="1e149-283">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="1e149-284">Velg **Legg til, Legg til rolletilordning**.</span><span class="sxs-lookup"><span data-stu-id="1e149-284">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="1e149-285">Følg denne fremgangsmåten for hvert program i følgende tabell:</span><span class="sxs-lookup"><span data-stu-id="1e149-285">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="1e149-286">Velg rollen fra følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="1e149-286">Select the role from the following table.</span></span>
        2. <span data-ttu-id="1e149-287">La feltet **Tilordne tilgang til** være satt til **Azure AD-bruker, -gruppe eller -tjenestekontohaver**.</span><span class="sxs-lookup"><span data-stu-id="1e149-287">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="1e149-288">I **Velg**-feltet angir du programmet fra følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="1e149-288">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="1e149-289">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="1e149-289">Select **Save**.</span></span>

        | <span data-ttu-id="1e149-290">Søknad</span><span class="sxs-lookup"><span data-stu-id="1e149-290">Application</span></span>                                              | <span data-ttu-id="1e149-291">Rolle</span><span class="sxs-lookup"><span data-stu-id="1e149-291">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="1e149-292">Visningsnavnet for det nye programmet du opprettet</span><span class="sxs-lookup"><span data-stu-id="1e149-292">The display name of the new application that you created</span></span> | <span data-ttu-id="1e149-293">Eier</span><span class="sxs-lookup"><span data-stu-id="1e149-293">Owner</span></span>                       |
        | <span data-ttu-id="1e149-294">Visningsnavnet for det nye programmet du opprettet</span><span class="sxs-lookup"><span data-stu-id="1e149-294">The display name of the new application that you created</span></span> | <span data-ttu-id="1e149-295">Bidragsyter</span><span class="sxs-lookup"><span data-stu-id="1e149-295">Contributor</span></span>                 |
        | <span data-ttu-id="1e149-296">Visningsnavnet for det nye programmet du opprettet</span><span class="sxs-lookup"><span data-stu-id="1e149-296">The display name of the new application that you created</span></span> | <span data-ttu-id="1e149-297">Bidragsyter for lagringskonto</span><span class="sxs-lookup"><span data-stu-id="1e149-297">Storage Account Contributor</span></span> |
        | <span data-ttu-id="1e149-298">Visningsnavnet for det nye programmet du opprettet</span><span class="sxs-lookup"><span data-stu-id="1e149-298">The display name of the new application that you created</span></span> | <span data-ttu-id="1e149-299">Eier av Storage Blob Data</span><span class="sxs-lookup"><span data-stu-id="1e149-299">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="1e149-300">**AI Builder Authorization Service**</span><span class="sxs-lookup"><span data-stu-id="1e149-300">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="1e149-301">Leser for Storage Blob Data</span><span class="sxs-lookup"><span data-stu-id="1e149-301">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="1e149-302">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="1e149-302">Azure CLI</span></span>](#tab/azure-azure-cli)

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



## <a name="configure-the-data-lake"></a><span data-ttu-id="1e149-303">Konfigurere datasjøen</span><span class="sxs-lookup"><span data-stu-id="1e149-303">Configure the data lake</span></span>

<span data-ttu-id="1e149-304">Følg denne fremgangsmåten for å bruke LCS til å legge til tillegget Azure Data Lake i miljøet.</span><span class="sxs-lookup"><span data-stu-id="1e149-304">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="1e149-305">Logg på LCS, og velg deretter **Detaljerte opplysninger** under miljønavnet til høyre på siden.</span><span class="sxs-lookup"><span data-stu-id="1e149-305">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="1e149-306">I delen **Miljøtillegg** velger du **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="1e149-306">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="1e149-307">Velg tillegget **Eksporter til Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="1e149-307">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="1e149-308">Angi følgende verdier.</span><span class="sxs-lookup"><span data-stu-id="1e149-308">Enter the following values.</span></span>

    | <span data-ttu-id="1e149-309">Verdi</span><span class="sxs-lookup"><span data-stu-id="1e149-309">Value</span></span>                                                              | <span data-ttu-id="1e149-310">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="1e149-310">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="1e149-311">Leier-ID-en for Azure-abonnementet der Key Vault er</span><span class="sxs-lookup"><span data-stu-id="1e149-311">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="1e149-312">Leier-ID-en der lagringskontoen, appene og nøkkelhvelvene er.</span><span class="sxs-lookup"><span data-stu-id="1e149-312">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="1e149-313">Du finner denne verdien ved å åpne [Azure-portalen](https://portal.azure.com), gå til **Azure Active Directory** og kopiere verdien for **Leier-ID**.</span><span class="sxs-lookup"><span data-stu-id="1e149-313">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="1e149-314">Oppgi DNS-navnet for Key Vault</span><span class="sxs-lookup"><span data-stu-id="1e149-314">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="1e149-315">DNS-navnet for nøkkelhvelvet, for eksempel `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="1e149-315">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="1e149-316">(Denne verdien samsvarer med DNS-navnet som brukes i enhetslageret.)</span><span class="sxs-lookup"><span data-stu-id="1e149-316">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="1e149-317">Angi hemmeligheten som inneholder navnet på lagringskontoen</span><span class="sxs-lookup"><span data-stu-id="1e149-317">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="1e149-318">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="1e149-318">**storage-account-name**</span></span> |
    | <span data-ttu-id="1e149-319">Hemmelig navn på app-ID-en som skal brukes til å få tilgang til Data Lake</span><span class="sxs-lookup"><span data-stu-id="1e149-319">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="1e149-320">**app-id**</span><span class="sxs-lookup"><span data-stu-id="1e149-320">**app-id**</span></span> |
    | <span data-ttu-id="1e149-321">Hemmelig navn som skal brukes med app-ID-en</span><span class="sxs-lookup"><span data-stu-id="1e149-321">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="1e149-322">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="1e149-322">**app-secret**</span></span> |

5. <span data-ttu-id="1e149-323">Godta vilkårene, og velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="1e149-323">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="1e149-324">Tillegget installeres innen noen minutter.</span><span class="sxs-lookup"><span data-stu-id="1e149-324">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="1e149-325">Konfigurere AI Builder</span><span class="sxs-lookup"><span data-stu-id="1e149-325">Configure AI Builder</span></span>

1. <span data-ttu-id="1e149-326">Logg på LCS, og åpne siden **Miljødetaljer**.</span><span class="sxs-lookup"><span data-stu-id="1e149-326">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="1e149-327">Bla til delen **Miljøtillegg**.</span><span class="sxs-lookup"><span data-stu-id="1e149-327">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="1e149-328">Du skal kunne se tilleggene som allerede er installert i dette miljøet.</span><span class="sxs-lookup"><span data-stu-id="1e149-328">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="1e149-329">Hvis tillegget **Eksporter til Data Lake** ikke er blant dem, konfigurerer du dette tillegget.</span><span class="sxs-lookup"><span data-stu-id="1e149-329">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="1e149-330">Velg tillegget **Få innsikt**.</span><span class="sxs-lookup"><span data-stu-id="1e149-330">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="1e149-331">Angi følgende verdier på siden med detaljer for tillegget **Få innsikt**.</span><span class="sxs-lookup"><span data-stu-id="1e149-331">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="1e149-332">Verdi</span><span class="sxs-lookup"><span data-stu-id="1e149-332">Value</span></span>                                                    | <span data-ttu-id="1e149-333">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="1e149-333">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="1e149-334">URL-adresse for CDS-organisasjon</span><span class="sxs-lookup"><span data-stu-id="1e149-334">CDS Organization URL</span></span>                                     | <span data-ttu-id="1e149-335">URL-adressen for Dataverse kopiert fra oppføringen over.</span><span class="sxs-lookup"><span data-stu-id="1e149-335">The Dataverse organization URL copied from above.</span></span> |
    | <span data-ttu-id="1e149-336">ID for CDS-organisasjon</span><span class="sxs-lookup"><span data-stu-id="1e149-336">CDS Org ID</span></span>                                               | <span data-ttu-id="1e149-337">ID-en for Dataverse kopiert fra oppføringen over.</span><span class="sxs-lookup"><span data-stu-id="1e149-337">The Dataverse organization ID copied from above.</span></span> |
5. <span data-ttu-id="1e149-338">Aktiver **Er dette standardmiljø for leieren din**.</span><span class="sxs-lookup"><span data-stu-id="1e149-338">Enable **Is this the default environment for you Tenant**.</span></span>
    
## <a name="configure-the-entity-store"></a><span data-ttu-id="1e149-339">Konfigurere enhetslageret</span><span class="sxs-lookup"><span data-stu-id="1e149-339">Configure the entity store</span></span>

<span data-ttu-id="1e149-340">Følg denne fremgangsmåten for å konfigurere enhetslageret i Finance-miljøet ditt.</span><span class="sxs-lookup"><span data-stu-id="1e149-340">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="1e149-341">Gå til **Systemadministrasjon \> Oppsett \> Systemparametere \> Datatilkoblinger**.</span><span class="sxs-lookup"><span data-stu-id="1e149-341">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="1e149-342">Angi verdier i følgende Key Vault-felter:</span><span class="sxs-lookup"><span data-stu-id="1e149-342">Set the following key vault fields:</span></span>

    - <span data-ttu-id="1e149-343">**Program-ID (klient)** – Angi programklient-ID-en du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="1e149-343">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="1e149-344">**Programhemmelighet** – Angi hemmeligheten du lagret for programmet du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="1e149-344">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="1e149-345">**DNS-navn** – Du kan finne DNS-navnet (Domain Name System) på siden for programdetaljer for programmet du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="1e149-345">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="1e149-346">**Hemmelig navn** – Angi **storage-account-connection-string**.</span><span class="sxs-lookup"><span data-stu-id="1e149-346">**Secret name** – Enter **storage-account-connection-string**.</span></span>
3. <span data-ttu-id="1e149-347">Aktiver **Aktiver Data Lake-integrasjon**.</span><span class="sxs-lookup"><span data-stu-id="1e149-347">Enable **Enable Data Lake integration**.</span></span>
4. <span data-ttu-id="1e149-348">Velg **Test Azure Key Vault**, og kontroller at det ikke er noen feil.</span><span class="sxs-lookup"><span data-stu-id="1e149-348">Select **Test Azure Key Vault** and verify there are no errors.</span></span>
5. <span data-ttu-id="1e149-349">Velg **Test Azure storage**, og kontroller at det ikke er noen feil.</span><span class="sxs-lookup"><span data-stu-id="1e149-349">Select **Test Azure storage** and verify there are no errors.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="1e149-350">Tilbakemelding og støtte</span><span class="sxs-lookup"><span data-stu-id="1e149-350">Feedback and support</span></span>

<span data-ttu-id="1e149-351">Send en e-postmelding til [Innsikt i kundebetaling (forhåndsversjon)](mailto:fiap@microsoft.com) hvis du er interessert i å gi tilbakemelding eller trenger støtte.</span><span class="sxs-lookup"><span data-stu-id="1e149-351">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="1e149-352">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="1e149-352">Privacy notice</span></span>

<span data-ttu-id="1e149-353">Forhåndsversjoner (1) kan ha redusert personvern og færre sikkerhetstiltak enn Dynamics 365 Finance and Operations-tjenesten, (2) er ikke inkludert i serviceavtalen (SLA) for denne tjenesten, (3) må ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) har begrenset støtte.</span><span class="sxs-lookup"><span data-stu-id="1e149-353">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
