---
title: Konfigurasjon for Finance Insights for offentlig forhåndsversjon (forhåndsversjon) – versjon 10.0.20 og nyere
description: Dette emnet forklarer hvordan du konfigurerer systemet slik at det bruker funksjonene i Finance Insights for offentlig forhåndsversjon i versjon 10.0.20 og nyere.
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
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 613bd4816e2f0c4fbb56cf79779a08c6a09592bd
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222618"
---
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a><span data-ttu-id="f63da-103">Konfigurasjon for Finance Insights for offentlig forhåndsversjon (forhåndsversjon) – versjon 10.0.20 og nyere</span><span class="sxs-lookup"><span data-stu-id="f63da-103">Configuration for Finance insights for public preview (preview) - version 10.0.20 and later</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f63da-104">Finance Insights kombinerer funksjonalitet fra Microsoft Dynamics 365 Finance med Dataverse, Azure og AI Builder for å gi organisasjonen kraftige prognoseverktøy.</span><span class="sxs-lookup"><span data-stu-id="f63da-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="f63da-105">Dette emnet forklarer hvordan du konfigurerer Dynamics 365 Finance versjon 10.0.20 slik at systemet kan bruke funksjonene som er tilgjengelige i den offentlige forhåndsversjonen av Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="f63da-105">This topic explains how to configure Dynamics 365 Finance version 10.0.20 so that your system can use the capabilities that are available in Finance insights public preview.</span></span>

> [!NOTE]
> <span data-ttu-id="f63da-106">Konfigurasjonstrinnene som beskrives i dette emnet, gjelder bare for Finance versjon 10.0.20 og nyere.</span><span class="sxs-lookup"><span data-stu-id="f63da-106">The configuration steps that are described in this topic apply only to Finance version 10.0.20 and later.</span></span> <span data-ttu-id="f63da-107">Hvis du vil konfigurere Finance Insights i versjon 10.0.19 og tidligere, kan du se [Konfigurasjon for Finance Insights – versjoner opptil 10.0.18](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="f63da-107">'To set up Finance insights on version 10.0.19 and earlier, see [Configuration for Finance insights - versions up to 10.0.18](configure-for-fin-insites.md).</span></span>

## <a name="deploy-finance"></a><span data-ttu-id="f63da-108">Distribuere Finance</span><span class="sxs-lookup"><span data-stu-id="f63da-108">Deploy Finance</span></span>

<span data-ttu-id="f63da-109">Følg denne fremgangsmåten for å distribuere miljøene.</span><span class="sxs-lookup"><span data-stu-id="f63da-109">Follow these steps to deploy the environments.</span></span>

1. <span data-ttu-id="f63da-110">Opprett eller oppdater et Finance-miljø i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f63da-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Finance environment.</span></span> <span data-ttu-id="f63da-111">Miljøet krever appversjon 10.0.20 eller nyere av Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="f63da-111">The environment requires app version 10.0.20 or later of Finance and Operations apps.</span></span>
2. <span data-ttu-id="f63da-112">Miljøet må være et miljø med høy tilgjengelighet i sandkassemodus.</span><span class="sxs-lookup"><span data-stu-id="f63da-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="f63da-113">(Denne typen miljø kalles også et miljø på lag 2.) Hvis du vil ha mer informasjon, kan du se [Miljøplanlegging](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="f63da-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="f63da-114">Hvis du konfigurerer Finance Insights i et sandkassemiljø, må du kanskje kopiere produksjonsdata til dette miljøet for at prediksjoner skal kunne fungere.</span><span class="sxs-lookup"><span data-stu-id="f63da-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="f63da-115">Prediksjonsmodellen bruker flere år med data til å bygge prediksjoner.</span><span class="sxs-lookup"><span data-stu-id="f63da-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="f63da-116">Contoso-demodataene inneholder ikke nok historiske data til at prediksjonsmodellen kan læres opp tilstrekkelig.</span><span class="sxs-lookup"><span data-stu-id="f63da-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="f63da-117">Konfigurer Dataverse</span><span class="sxs-lookup"><span data-stu-id="f63da-117">Configure Dataverse</span></span>

<span data-ttu-id="f63da-118">Følg fremgangsmåten nedenfor til å konfigurere Dataverse for Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="f63da-118">Follow these steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="f63da-119">Åpne miljøsiden i LCS, og kontroller at **Power Platform-integrering** allerede er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="f63da-119">In LCS, open the environment page, and verify that the **Power Platform Integration** section is already set up.</span></span>

    - <span data-ttu-id="f63da-120">Hvis den allerede er konfigurert, skal Dataverse-miljønavnet som er koblet til Finance-miljøet, vises.</span><span class="sxs-lookup"><span data-stu-id="f63da-120">If it's already set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>
    - <span data-ttu-id="f63da-121">Hvis det ikke er konfigurert, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="f63da-121">If it isn't yet set up, follow these steps:</span></span>

        1. <span data-ttu-id="f63da-122">Velg **Oppsett**-knappen i delen **Power Platform-integrering**.</span><span class="sxs-lookup"><span data-stu-id="f63da-122">In the **Power Platform Integration** section, select **Setup**.</span></span> <span data-ttu-id="f63da-123">Konfigurasjonen av miljøet kan ta opptil en time.</span><span class="sxs-lookup"><span data-stu-id="f63da-123">Setup of the environment might take up to an hour.</span></span>
        2. <span data-ttu-id="f63da-124">Hvis Dataverse-miljøet er riktig konfigurert, skal navnet på Dataverse-miljøet som er koblet til Finance-miljøet, vises.</span><span class="sxs-lookup"><span data-stu-id="f63da-124">If the Dataverse environment is successfully set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>

        > [!NOTE]
        > <span data-ttu-id="f63da-125">Etter at du har fullført miljøkonfigurasjonen, må du **ikke** velge **Kobling til CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="f63da-125">After you complete the environment setup, do **not** select **Link to CDS for Apps**.</span></span> <span data-ttu-id="f63da-126">Denne knappen kreves ikke for Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="f63da-126">This button isn't required for Finance insights.</span></span> <span data-ttu-id="f63da-127">Hvis du velger den, kan du ikke konfigurere de nødvendige miljøtilleggene i LCS.</span><span class="sxs-lookup"><span data-stu-id="f63da-127">If you select it, you won't be able to configure the required environment add-ins in LCS.</span></span>

## <a name="configure-azure"></a><span data-ttu-id="f63da-128">Konfigurere Azure</span><span class="sxs-lookup"><span data-stu-id="f63da-128">Configure Azure</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="f63da-129">Bruke Azure Cloud Shell til å konfigurere Data Lake-ressurser for Finance Insights</span><span class="sxs-lookup"><span data-stu-id="f63da-129">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="f63da-130">Bruke et Windows PowerShell-skript</span><span class="sxs-lookup"><span data-stu-id="f63da-130">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="f63da-131">Et Windows PowerShell-skript er oppgitt, slik at du lett kan konfigurere Azure-ressursene som er beskrevet i [Konfigurere eksport til Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="f63da-131">A Windows PowerShell script has been provided so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="f63da-132">Hvis du foretrekker å konfigurere manuelt, kan du hoppe over denne fremgangsmåten og i stedet fullføre fremgangsmåten i delen [Manuell konfigurasjon](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="f63da-132">If you prefer to do the setup manually, skip this procedure, and complete the procedure in the [Manual setup](#manual-setup) section instead.</span></span>

> [!NOTE]
> <span data-ttu-id="f63da-133">Bruk fremgangsmåten nedenfor til å kjøre Windows PowerShell-skriptet.</span><span class="sxs-lookup"><span data-stu-id="f63da-133">Use the following procedure to run the Windows PowerShell script.</span></span> <span data-ttu-id="f63da-134">Konfigurasjonen fungerer kanskje ikke hvis du bruker alternativet **Prøv det** i Azure CLI eller kjører skriptet på datamaskinen.</span><span class="sxs-lookup"><span data-stu-id="f63da-134">The setup might not work if you use the **Try it** option in Azure CLI or if you run the script on your computer.</span></span>

<span data-ttu-id="f63da-135">Følg denne fremgangsmåten for å bruke Windows PowerShell-skriptet til å konfigurere Azure.</span><span class="sxs-lookup"><span data-stu-id="f63da-135">Follow these steps to use the Windows PowerShell script to configure Azure.</span></span> <span data-ttu-id="f63da-136">Du må ha rettigheter til å opprette en Azure-ressursgruppe, Azure-ressurser og et Azure AD-program.</span><span class="sxs-lookup"><span data-stu-id="f63da-136">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="f63da-137">Hvis du vil ha informasjon om de nødvendige tillatelsene, kan du se [Kontrollere Azure AD-tillatelser](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="f63da-137">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="f63da-138">I [Azure-portalen](https://portal.azure.com) går du til Azure-målabonnementet.</span><span class="sxs-lookup"><span data-stu-id="f63da-138">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span>
2. <span data-ttu-id="f63da-139">Velg **Cloud Shell** til høyre for **Søk**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63da-139">Select **Cloud Shell** to the right of the **Search** field.</span></span>
3. <span data-ttu-id="f63da-140">Velg **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="f63da-140">Select **PowerShell**.</span></span>
4. <span data-ttu-id="f63da-141">Opprett lagringsplass hvis du blir bedt om å opprette det.</span><span class="sxs-lookup"><span data-stu-id="f63da-141">Create storage if you're prompted to create it.</span></span>
5. <span data-ttu-id="f63da-142">Velg **Kopier** i fanen **Azure CLI**.</span><span class="sxs-lookup"><span data-stu-id="f63da-142">On the **Azure CLI** tab, select **Copy**.</span></span>
6. <span data-ttu-id="f63da-143">Åpne en ny fil i Notisblokk, og lim inn i Windows PowerShell-skriptet.</span><span class="sxs-lookup"><span data-stu-id="f63da-143">In Notepad, open a new file, and paste in the Windows PowerShell script.</span></span>
7. <span data-ttu-id="f63da-144">Lagre filen som **ConfigureDataLake.ps1**.</span><span class="sxs-lookup"><span data-stu-id="f63da-144">Save the file as **ConfigureDataLake.ps1**.</span></span>
8. <span data-ttu-id="f63da-145">Last opp Windows PowerShell-skriptet til økten ved å bruke menyalternativet for opplasting i Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="f63da-145">Upload the Windows PowerShell script to the session by using the menu option for upload in Cloud Shell.</span></span>
9. <span data-ttu-id="f63da-146">Kjør skriptet **.\ConfigureDataLake.ps1**.</span><span class="sxs-lookup"><span data-stu-id="f63da-146">Run the **.\ConfigureDataLake.ps1** script.</span></span>
10. <span data-ttu-id="f63da-147">Følg instruksjonene for å kjøre skriptet.</span><span class="sxs-lookup"><span data-stu-id="f63da-147">Follow the prompts to run the script.</span></span>
11. <span data-ttu-id="f63da-148">Bruk informasjonen fra skriptutdataene til å installere tillegget Eksporter til Data Lake i LCS.</span><span class="sxs-lookup"><span data-stu-id="f63da-148">Use the information from the script output to install the Export to Data Lake add-in in LCS.</span></span>

### <a name="manual-setup"></a><span data-ttu-id="f63da-149">Manuell konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="f63da-149">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="f63da-150">Legg til programmer i Azure AD-leieren</span><span class="sxs-lookup"><span data-stu-id="f63da-150">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="f63da-151">Gå til **Azure Active Directory** i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="f63da-151">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="f63da-152">Velg **Behandle \> Enterprise-programmer**.</span><span class="sxs-lookup"><span data-stu-id="f63da-152">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="f63da-153">Søk etter følgende programmer etter app-ID.</span><span class="sxs-lookup"><span data-stu-id="f63da-153">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="f63da-154">Program</span><span class="sxs-lookup"><span data-stu-id="f63da-154">Application</span></span>                              | <span data-ttu-id="f63da-155">App-ID</span><span class="sxs-lookup"><span data-stu-id="f63da-155">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="f63da-156">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="f63da-156">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="f63da-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="f63da-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="f63da-158">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="f63da-158">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="f63da-159">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="f63da-159">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="f63da-160">AI Builder Authorization Service</span><span class="sxs-lookup"><span data-stu-id="f63da-160">AI Builder Authorization Service</span></span>         | <span data-ttu-id="f63da-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="f63da-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="f63da-162">Hvis du ikke finner noen av de ovennevnte programmene, kan du prøve følgende trinn.</span><span class="sxs-lookup"><span data-stu-id="f63da-162">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="f63da-163">Søk etter **powershell** på **Start**-menyen på den lokale datamaskinen.</span><span class="sxs-lookup"><span data-stu-id="f63da-163">On your local computer, on the **Start** menu, search for **powershell**.</span></span>
2. <span data-ttu-id="f63da-164">Velg og hold (eller høyreklikk på) **Windows PowerShell**, og velg deretter **Kjør som administrator**.</span><span class="sxs-lookup"><span data-stu-id="f63da-164">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="f63da-165">Kjør følgende kommando for å installere **AzureAD**-modulen.</span><span class="sxs-lookup"><span data-stu-id="f63da-165">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="f63da-166">Hvis en NuGet-leverandør kreves for å fortsette, velger du **J** for å installere den.</span><span class="sxs-lookup"><span data-stu-id="f63da-166">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="f63da-167">Hvis du får en melding om at repositoriet ikke er klarert, velger du **J** for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="f63da-167">If you receive an "Untrusted repository" message, select **Y** to continue.</span></span>
6. <span data-ttu-id="f63da-168">For hvert program som må legges til, kjører du følgende kommandoer for å legge til programmet i Azure AD.</span><span class="sxs-lookup"><span data-stu-id="f63da-168">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="f63da-169">Når du blir bedt om det, logger du på som Azure AD-administrator.</span><span class="sxs-lookup"><span data-stu-id="f63da-169">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="f63da-170">Opprette Azure-ressurser</span><span class="sxs-lookup"><span data-stu-id="f63da-170">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="f63da-171">Kontroller at du oppretter følgende ressurser i samme Azure AD-forekomst som Dataverse-miljøet er i.</span><span class="sxs-lookup"><span data-stu-id="f63da-171">Make sure that you create the following resources in the same Azure AD instance that the Dataverse environment is in.</span></span> <span data-ttu-id="f63da-172">Du kan ikke bruke ressurser fra en annen Azure AD-forekomst.</span><span class="sxs-lookup"><span data-stu-id="f63da-172">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="f63da-173">Opprett en lagringskonto:</span><span class="sxs-lookup"><span data-stu-id="f63da-173">Create a storage account:</span></span>

    1. <span data-ttu-id="f63da-174">Opprett en lagringskonto i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="f63da-174">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="f63da-175">I dialogboksen **Opprett lagringskonto** angir du verdier i følgende felter:</span><span class="sxs-lookup"><span data-stu-id="f63da-175">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="f63da-176">**Plassering** – Velg datasenteret der miljøet er plassert.</span><span class="sxs-lookup"><span data-stu-id="f63da-176">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="f63da-177">**Ytelse** – Vi anbefaler at du velger **Standard**.</span><span class="sxs-lookup"><span data-stu-id="f63da-177">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="f63da-178">**Kontotype** – Du må velge **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="f63da-178">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="f63da-179">Velg **Aktiver** under funksjonen **Hierarkiske navneområder** for alternativet **Data Lake Storage Gen2** i dialogboksen **Avanserte alternativer**.</span><span class="sxs-lookup"><span data-stu-id="f63da-179">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="f63da-180">Hvis du ikke aktiverer denne funksjonen, kan du ikke bruke data som Finance and Operations-apper skriver ved hjelp av tjenester som Power BI-dataflyter.</span><span class="sxs-lookup"><span data-stu-id="f63da-180">If you don't enable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="f63da-181">Velg **Se gjennom og opprett**.</span><span class="sxs-lookup"><span data-stu-id="f63da-181">Select **Review and create**.</span></span> <span data-ttu-id="f63da-182">Når distribusjonen er fullført, vises den nye ressursen i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="f63da-182">When the deployment is completed, the new resource is shown in the Azure portal.</span></span>
    5. <span data-ttu-id="f63da-183">Gå til lagringskontoen du opprettet.</span><span class="sxs-lookup"><span data-stu-id="f63da-183">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="f63da-184">Velg **Tilgangsnøkler** på menyen til venstre.</span><span class="sxs-lookup"><span data-stu-id="f63da-184">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="f63da-185">Kopier og lagre navnet på lagringskontoen.</span><span class="sxs-lookup"><span data-stu-id="f63da-185">Copy and save the name of the storage account.</span></span> <span data-ttu-id="f63da-186">Du må angi denne verdien senere når du konfigurerer Key Vault-hemmeligheter.</span><span class="sxs-lookup"><span data-stu-id="f63da-186">You will have to provide this value later, when you set up key vault secrets.</span></span>

2. <span data-ttu-id="f63da-187">Opprett et nøkkelhvelv:</span><span class="sxs-lookup"><span data-stu-id="f63da-187">Create a key vault:</span></span>

    1. <span data-ttu-id="f63da-188">Opprett et nøkkelhvelv i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="f63da-188">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="f63da-189">I **Plassering**-feltet i dialogboksen **Opprett nøkkelhvelv** velger du datasenteret der miljøet er.</span><span class="sxs-lookup"><span data-stu-id="f63da-189">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="f63da-190">Etter at nøkkelhvelvet er opprettet, kan du gå til **Oversikt over Key Vault** og kopiere og lagre DNS-navnet.</span><span class="sxs-lookup"><span data-stu-id="f63da-190">After key vault is created, go to **Key Vault Overview**, and copy and save the DNS name.</span></span> <span data-ttu-id="f63da-191">Du må angi denne verdien senere når du konfigurerer Data Lake-tillegget.</span><span class="sxs-lookup"><span data-stu-id="f63da-191">You will have to provide this value later, when you set up the Data Lake add-in.</span></span>

3. <span data-ttu-id="f63da-192">Opprett og registrer et Azure AD-program:</span><span class="sxs-lookup"><span data-stu-id="f63da-192">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="f63da-193">Gå til **Azure Active Directory** i [Azure-portalen](https://portal.azure.com), og velg deretter **Appregistreringer**.</span><span class="sxs-lookup"><span data-stu-id="f63da-193">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="f63da-194">Velg **Ny programregistrering**, og angi verdier i følgende felter:</span><span class="sxs-lookup"><span data-stu-id="f63da-194">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="f63da-195">**Navn** – Angi navnet på appen.</span><span class="sxs-lookup"><span data-stu-id="f63da-195">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="f63da-196">**Programtype** – Velg **Web-API**.</span><span class="sxs-lookup"><span data-stu-id="f63da-196">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="f63da-197">**Konfigurasjon av URI for omadressering** – Angi nettadressen til Dynamics 365-forekomsten, for eksempel `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="f63da-197">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="f63da-198">Gå til appen du nettopp opprettet, og kopier og lagre verdien for **Program-ID (klient)**.</span><span class="sxs-lookup"><span data-stu-id="f63da-198">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="f63da-199">Du må angi denne verdien senere når du konfigurerer Key Vault-hemmeligheter.</span><span class="sxs-lookup"><span data-stu-id="f63da-199">You will have to provide this value later, when you set up key vault secrets.</span></span>
    4. <span data-ttu-id="f63da-200">Gå til **API-tillatelser**, og følg denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="f63da-200">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="f63da-201">Velg **Legg til en tillatelse**.</span><span class="sxs-lookup"><span data-stu-id="f63da-201">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="f63da-202">Velg **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="f63da-202">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="f63da-203">Etter at du har valgt delegerte tillatelser, velger du **user\_impersonation**.</span><span class="sxs-lookup"><span data-stu-id="f63da-203">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="f63da-204">Velg **Legg til tillatelser**.</span><span class="sxs-lookup"><span data-stu-id="f63da-204">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="f63da-205">På menyen for appen velger du **Sertifikater \& hemmeligheter**, og deretter følger du denne fremgangsmåten for å opprette Key Vault-hemmeligheter:</span><span class="sxs-lookup"><span data-stu-id="f63da-205">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="f63da-206">Velg **Ny klienthemmelighet**.</span><span class="sxs-lookup"><span data-stu-id="f63da-206">Select **New client secret**.</span></span>
        2. <span data-ttu-id="f63da-207">Angi et navn i **Nøkkelbeskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63da-207">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="f63da-208">Velg en varighet, og velg deretter **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="f63da-208">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="f63da-209">Det genereres en hemmelighet i **Verdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63da-209">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="f63da-210">Kopier og lagre verdien for klienthemmelighet.</span><span class="sxs-lookup"><span data-stu-id="f63da-210">Copy and save the client secret value.</span></span> <span data-ttu-id="f63da-211">Du må angi denne verdien senere når du konfigurerer Key Vault-hemmeligheter.</span><span class="sxs-lookup"><span data-stu-id="f63da-211">You will have to provide this value later, when you set up key vault secrets.</span></span>

4. <span data-ttu-id="f63da-212">Opprett Key Vault-hemmeligheter:</span><span class="sxs-lookup"><span data-stu-id="f63da-212">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="f63da-213">Gå til nøkkelhvelvet du opprettet tidligere, og velg **Hemmeligheter**.</span><span class="sxs-lookup"><span data-stu-id="f63da-213">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="f63da-214">Følg denne fremgangsmåten for hvert hemmelige navn i følgende tabell:</span><span class="sxs-lookup"><span data-stu-id="f63da-214">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="f63da-215">Velg **Generer/Importer**.</span><span class="sxs-lookup"><span data-stu-id="f63da-215">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="f63da-216">I feltet **Opplastingsalternativer** i dialogboksen **Opprett en hemmelighet** velger du **Manuell**.</span><span class="sxs-lookup"><span data-stu-id="f63da-216">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="f63da-217">Opprett det hemmelige navnet og verdien fra tabellen.</span><span class="sxs-lookup"><span data-stu-id="f63da-217">Create the secret name and value from the table.</span></span>
        4. <span data-ttu-id="f63da-218">Velg **Aktivert**, og velg deretter **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="f63da-218">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="f63da-219">Hemmeligheten opprettes og legges til i Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f63da-219">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="f63da-220">Hemmelig navn</span><span class="sxs-lookup"><span data-stu-id="f63da-220">Secret name</span></span>                       | <span data-ttu-id="f63da-221">Hemmelig verdi</span><span class="sxs-lookup"><span data-stu-id="f63da-221">Secret value</span></span>                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | <span data-ttu-id="f63da-222">app-id</span><span class="sxs-lookup"><span data-stu-id="f63da-222">app-id</span></span>                            | <span data-ttu-id="f63da-223">App-ID-en for programmet du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="f63da-223">The app ID of the application that you created earlier.</span></span>                                      |
        | <span data-ttu-id="f63da-224">app-secret</span><span class="sxs-lookup"><span data-stu-id="f63da-224">app-secret</span></span>                        | <span data-ttu-id="f63da-225">Klienthemmeligheten du lagret tidligere.</span><span class="sxs-lookup"><span data-stu-id="f63da-225">The client secret that you saved earlier.</span></span>                                                    |
        | <span data-ttu-id="f63da-226">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="f63da-226">storage-account-name</span></span>              | <span data-ttu-id="f63da-227">Navnet på lagringskontoen du opprettet tidligere, for eksempel **storageaccount1**.</span><span class="sxs-lookup"><span data-stu-id="f63da-227">The name of the storage account that you created earlier, such as **storageaccount1**.</span></span>       |

5. <span data-ttu-id="f63da-228">Autoriser programmet for tilgang til nøkkelhvelvet:</span><span class="sxs-lookup"><span data-stu-id="f63da-228">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="f63da-229">Åpne nøkkelhvelvet du opprettet tidligere, i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="f63da-229">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="f63da-230">Velg tilgangspolicyene.</span><span class="sxs-lookup"><span data-stu-id="f63da-230">Select the access policies.</span></span>
    3. <span data-ttu-id="f63da-231">Følg denne fremgangsmåten for hvert program i følgende tabell:</span><span class="sxs-lookup"><span data-stu-id="f63da-231">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="f63da-232">Velg **Legg til tilgangspolicy** for å opprette en tilgangspolicy.</span><span class="sxs-lookup"><span data-stu-id="f63da-232">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="f63da-233">I feltet **Hemmelige tillatelser** velger du tillatelsene fra tabellen.</span><span class="sxs-lookup"><span data-stu-id="f63da-233">In the **Secret permissions** field, select the permissions from the table.</span></span>
        3. <span data-ttu-id="f63da-234">I feltet **Velg sikkerhetskontohaver** søker du etter visningsnavnet for programmet i tabellen.</span><span class="sxs-lookup"><span data-stu-id="f63da-234">In the **Select principal** field, search for the application display name from the table.</span></span>
        4. <span data-ttu-id="f63da-235">Velg **Velg**.</span><span class="sxs-lookup"><span data-stu-id="f63da-235">Select **Select**.</span></span>
        5. <span data-ttu-id="f63da-236">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="f63da-236">Select **Add**.</span></span>
        6. <span data-ttu-id="f63da-237">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f63da-237">Select **Save**.</span></span>

        | <span data-ttu-id="f63da-238">Søknad</span><span class="sxs-lookup"><span data-stu-id="f63da-238">Application</span></span>                                              | <span data-ttu-id="f63da-239">Tillatelser</span><span class="sxs-lookup"><span data-stu-id="f63da-239">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="f63da-240">Visningsnavnet for det nye programmet du opprettet</span><span class="sxs-lookup"><span data-stu-id="f63da-240">The display name of the new application that you created</span></span> | <span data-ttu-id="f63da-241">Hent, Vis</span><span class="sxs-lookup"><span data-stu-id="f63da-241">Get, List</span></span>   |
        | <span data-ttu-id="f63da-242">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="f63da-242">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="f63da-243">Hent, Vis</span><span class="sxs-lookup"><span data-stu-id="f63da-243">Get, List</span></span>   |

6. <span data-ttu-id="f63da-244">Tilordne roller for tilgang til lagringskontoen:</span><span class="sxs-lookup"><span data-stu-id="f63da-244">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="f63da-245">Åpne lagringskontoen du opprettet tidligere, i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="f63da-245">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="f63da-246">Velg **Tilgangskontroll (IAM)**, og velg deretter **Rolletilordninger**.</span><span class="sxs-lookup"><span data-stu-id="f63da-246">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="f63da-247">Velg **Legg til, Legg til rolletilordning**.</span><span class="sxs-lookup"><span data-stu-id="f63da-247">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="f63da-248">Følg denne fremgangsmåten for hvert program i følgende tabell:</span><span class="sxs-lookup"><span data-stu-id="f63da-248">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="f63da-249">Velg rollen fra tabellen.</span><span class="sxs-lookup"><span data-stu-id="f63da-249">Select the role from the table.</span></span>
        2. <span data-ttu-id="f63da-250">La feltet **Tilordne tilgang til** være satt til **Azure AD-bruker, -gruppe eller -tjenestekontohaver**.</span><span class="sxs-lookup"><span data-stu-id="f63da-250">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="f63da-251">I **Velg**-feltet angir du programmet fra tabellen.</span><span class="sxs-lookup"><span data-stu-id="f63da-251">In the **Select** field, enter the application from the table.</span></span>
        4. <span data-ttu-id="f63da-252">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f63da-252">Select **Save**.</span></span>

        | <span data-ttu-id="f63da-253">Søknad</span><span class="sxs-lookup"><span data-stu-id="f63da-253">Application</span></span>                                              | <span data-ttu-id="f63da-254">Rolle</span><span class="sxs-lookup"><span data-stu-id="f63da-254">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="f63da-255">Visningsnavnet for det nye programmet du opprettet</span><span class="sxs-lookup"><span data-stu-id="f63da-255">The display name of the new application that you created</span></span> | <span data-ttu-id="f63da-256">Eier</span><span class="sxs-lookup"><span data-stu-id="f63da-256">Owner</span></span>                       |
        | <span data-ttu-id="f63da-257">Visningsnavnet for det nye programmet du opprettet</span><span class="sxs-lookup"><span data-stu-id="f63da-257">The display name of the new application that you created</span></span> | <span data-ttu-id="f63da-258">Bidragsyter</span><span class="sxs-lookup"><span data-stu-id="f63da-258">Contributor</span></span>                 |
        | <span data-ttu-id="f63da-259">Visningsnavnet for det nye programmet du opprettet</span><span class="sxs-lookup"><span data-stu-id="f63da-259">The display name of the new application that you created</span></span> | <span data-ttu-id="f63da-260">Bidragsyter for lagringskonto</span><span class="sxs-lookup"><span data-stu-id="f63da-260">Storage Account Contributor</span></span> |
        | <span data-ttu-id="f63da-261">Visningsnavnet for det nye programmet du opprettet</span><span class="sxs-lookup"><span data-stu-id="f63da-261">The display name of the new application that you created</span></span> | <span data-ttu-id="f63da-262">Eier av Storage Blob Data</span><span class="sxs-lookup"><span data-stu-id="f63da-262">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="f63da-263">**AI Builder Authorization Service**</span><span class="sxs-lookup"><span data-stu-id="f63da-263">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="f63da-264">Leser for Storage Blob Data</span><span class="sxs-lookup"><span data-stu-id="f63da-264">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="f63da-265">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="f63da-265">Azure CLI</span></span>](#tab/azure-azure-cli)

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

## <a name="configure-the-export-to-data-lake-add-in"></a><span data-ttu-id="f63da-266">Konfigurere tillegget Eksporter til Data Lake</span><span class="sxs-lookup"><span data-stu-id="f63da-266">Configure the Export to Data Lake add-in</span></span>

<span data-ttu-id="f63da-267">Følg denne fremgangsmåten for å bruke LCS til å legge til tillegget Eksporter til Data Lake i miljøet.</span><span class="sxs-lookup"><span data-stu-id="f63da-267">Follow these steps to use LCS to add the Export to Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="f63da-268">Logg på LCS, og velg deretter **Detaljerte opplysninger** under miljønavnet til høyre på siden.</span><span class="sxs-lookup"><span data-stu-id="f63da-268">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="f63da-269">I delen **Miljøtillegg** velger du **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="f63da-269">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="f63da-270">Velg tillegget **Eksporter til Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="f63da-270">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="f63da-271">Angi følgende verdier.</span><span class="sxs-lookup"><span data-stu-id="f63da-271">Enter the following values.</span></span>

    | <span data-ttu-id="f63da-272">Verdi</span><span class="sxs-lookup"><span data-stu-id="f63da-272">Value</span></span>                                                              | <span data-ttu-id="f63da-273">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f63da-273">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="f63da-274">Leier-ID-en for Azure-abonnementet der Key Vault er</span><span class="sxs-lookup"><span data-stu-id="f63da-274">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="f63da-275">Leier-ID-en der lagringskontoen, appene og nøkkelhvelvene er.</span><span class="sxs-lookup"><span data-stu-id="f63da-275">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="f63da-276">Du henter denne verdien ved å åpne [Azure-portalen](https://portal.azure.com), gå til **Azure Active Directory** og kopiere verdien for **Leier-ID**.</span><span class="sxs-lookup"><span data-stu-id="f63da-276">To obtain this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="f63da-277">Oppgi DNS-navnet for Key Vault</span><span class="sxs-lookup"><span data-stu-id="f63da-277">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="f63da-278">DNS-navnet for nøkkelhvelvet, for eksempel `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="f63da-278">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> |
    | <span data-ttu-id="f63da-279">Angi hemmeligheten som inneholder navnet på lagringskontoen</span><span class="sxs-lookup"><span data-stu-id="f63da-279">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="f63da-280">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="f63da-280">**storage-account-name**</span></span> |
    | <span data-ttu-id="f63da-281">Hemmelig navn på app-ID-en som skal brukes til å få tilgang til Data Lake</span><span class="sxs-lookup"><span data-stu-id="f63da-281">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="f63da-282">**app-id**</span><span class="sxs-lookup"><span data-stu-id="f63da-282">**app-id**</span></span> |
    | <span data-ttu-id="f63da-283">Hemmelig navn for appklienthemmelighet</span><span class="sxs-lookup"><span data-stu-id="f63da-283">Secret name for App client secret</span></span>                                  | <span data-ttu-id="f63da-284">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="f63da-284">**app-secret**</span></span> |

5. <span data-ttu-id="f63da-285">Godta vilkårene, og velg deretter **Installer**.</span><span class="sxs-lookup"><span data-stu-id="f63da-285">Agree to the terms, and then select **Install**.</span></span>

<span data-ttu-id="f63da-286">Tillegget installeres innen noen minutter.</span><span class="sxs-lookup"><span data-stu-id="f63da-286">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-the-finance-insights-add-in"></a><span data-ttu-id="f63da-287">Konfigurere Finance Insights-tillegget</span><span class="sxs-lookup"><span data-stu-id="f63da-287">Configure the Finance insights add-in</span></span>

> [!NOTE]
> <span data-ttu-id="f63da-288">Hvis du tidligere har installert Få innsikt-tillegget, avinstallerer du det før du fullfører fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="f63da-288">If you previously installed the Get insights add-in, uninstall it before you complete the following procedure.</span></span>

<span data-ttu-id="f63da-289">Følg denne fremgangsmåten for å installere Finance Insights-tillegget.</span><span class="sxs-lookup"><span data-stu-id="f63da-289">Follow these steps to install the Finance insights add-in.</span></span>

1. <span data-ttu-id="f63da-290">Logg på LCS, og velg deretter **Detaljerte opplysninger** under miljønavnet til høyre på siden.</span><span class="sxs-lookup"><span data-stu-id="f63da-290">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="f63da-291">I delen **Miljøtillegg** velger du **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="f63da-291">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="f63da-292">Velg **Finance Insights**-tillegget.</span><span class="sxs-lookup"><span data-stu-id="f63da-292">Select the **Finance insights** add-in.</span></span>
4. <span data-ttu-id="f63da-293">Godta vilkårene, og velg deretter **Installer**.</span><span class="sxs-lookup"><span data-stu-id="f63da-293">Agree to the terms, and then select **Install**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="f63da-294">Tilbakemelding og støtte</span><span class="sxs-lookup"><span data-stu-id="f63da-294">Feedback and support</span></span>

<span data-ttu-id="f63da-295">Hvis du er interessert i å gi tilbakemelding eller vil ha kundestøtte, kan du sende en e-postmelding til [Finance Insights (forhåndsversjon)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="f63da-295">If you're interested in providing feedback, or if you require support, send an email to [Finance insights (Preview)](mailto:fiap@microsoft.com).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
