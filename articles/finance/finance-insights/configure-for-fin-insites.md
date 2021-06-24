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
# <a name="configuration-for-finance-insights-preview"></a>Konfigurasjon for Finance Insights (forhåndsversjon)

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Følgende fremgangsmåter for å konfigurere Finance Insights er gyldige for Microsoft Dynamics 365 Finance-versjoner opptil 10.0.19. Hvis du vil konfigurere Finance Insights i versjon 10.0.20 og nyere, kan du se [Konfigurasjon for Finance Insights (forhåndsversjon) – versjon 10.0.20 og nyere](configure-for-fin-insites-PubPrvw.md).

Finance Insights kombinerer funksjonalitet fra Microsoft Dynamics 365 Finance med Microsoft Dataverse, Azure og AI Builder for å gi organisasjonen kraftige prognoseverktøy. Dette emnet forklarer konfigurasjonstrinnene som gjør at systemet kan bruke funksjonene i Finance Insights.

## <a name="deploy-dynamics-365-finance"></a>Klargjøre Dynamics 365 Finance

Klargjør miljøene ved å følge disse trinnene.

1. Opprett eller oppdater et Dynamics 365 Finance-miljø i Microsoft Dynamics Lifecycle Services (LCS). Miljøet krever appversjon 10.0.11 / Platform update 35 eller senere.
2. Miljøet må være et miljø med høy tilgjengelighet i sandkassemodus. (Denne typen miljø kalles også et miljø på lag 2.) Hvis du vil ha mer informasjon, kan du se [Miljøplanlegging](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. Hvis du konfigurerer Finance Insights i et sandkassemiljø, må du kanskje kopiere produksjonsdata til dette miljøet for at prediksjoner skal kunne fungere. Prediksjonsmodellen bruker flere år med data til å bygge prediksjoner. Contoso-demodataene inneholder ikke nok historiske data til at prediksjonsmodellen kan læres opp tilstrekkelig. 

## <a name="configure-dataverse"></a>Konfigurer Dataverse

Bruk fremgangsmåten nedenfor til å konfigurere Dataverse for Finance Insights.

1. Åpne miljøsiden i LCS, og kontroller at **Power Platform-integrering** allerede er satt opp.
    1. Hvis det allerede er satt opp, skal Dataverse-miljønavnet som er koblet til Dynamics 365 Finance-miljøet, vises. Kopier Dataverse-miljønavnet.
    2. Hvis det ikke er definert, følger du denne fremgangsmåten:
        1. Velg **Oppsett**-knappen i Power Platform-integreringsdelen. Det kan ta opptil en time før miljøet er konfigurert.
        2. Hvis Dataverse-miljøet er konfigurert riktig, skal Dataverse-miljøetnavnet som er koblet til Dynamics 365 Finance-miljøet, vises. Kopier Dataverse-miljønavnet.
> [!NOTE]
> Når du har fullført miljøoppsettet, må du **IKKE** velge knappen **Kobling til CDS for Apps**. Dette er ikke nødvendig for Finance Insights og vil deaktivere muligheten til å fullføre de nødvendige miljøtilleggene i LCS.

2. Åpne [administrasjonssenteret for Power Platform](https://admin.powerplatform.microsoft.com/), og følg denne fremgangsmåten for å opprette et nytt Dataverse-miljø i den samme Active Directory-leieren:

    1. Åpne **Miljøer**-siden.

        [![Miljøer-siden](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)

    2. Velg Dataverse-miljøet som opprettes over, og velg deretter **Innstillinger**.
    3. Velg **Ressurser \> Alle eldre innstillinger**.
    4. Velg **Innstillinger** i det øverste navigasjonsfeltet, og velg deretter **Tilpassinger**.
    5. Velg **Utviklerressurser**.
    6. Kopier verdien for **Dataverse-organisasjons-ID**.
    7. Noter deg URL-adressen for Dataverse-organisasjonen på adresselinjen i nettleseren. URL-adressen kan for eksempel være `https://org42b2b3d3.crm.dynamics.com`.

3. Hvis du har tenkt å bruke funksjonen Kontantstrømprognoser eller Budsjettprognoser, følger du disse trinnene for å oppdatere merknadsgrensen for organisasjonen til minst 50 megabyte (MB):

    1. Åpne [Power Apps-portalen](https://make.powerapps.com).
    2. Velg miljøet du nettopp opprettet, og velg deretter **Avanserte innstillinger**.
    3. Velg **Innstillinger \> E-postkonfigurasjon**.
    4. Endre verdien i feltet **Maksimal filstørrelse** til **51 200**. (Verdien uttrykkes i kilobyte \[kB\].)
    5. Velg **OK** for å lagre endringene.

## <a name="configure-the-azure-setup"></a>Konfigurere Azure-oppsettet

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a>Angi katalog-ID-en for Dataverse og brukerens objekt-ID for Azure AD

1. Angi katalog-ID-en for Dataverse:

    1. Åpne [Azure-portalen](https://portal.azure.com).
    2. Logg på ved å bruke bruker-ID-en som ble brukt til å opprette Dataverse-miljøet.
    3. Gå til **Azure Active Directory**.
    4. Kopier verdien for **Leier-ID**.

2. Angi brukerens objekt-ID for Azure Active Directory (Azure AD):

    1. Gå til **Brukere** i [Azure-portalen](https://portal.azure.com), og søk etter brukeren etter e-postadresse.
    2. Velg brukerens navn.
    3. Kopier verdien for **Objekt-ID**.

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Bruke Azure Cloud Shell til å konfigurere Data Lake-ressurser for Finance Insights

# <a name="use-a-windows-powershell-script"></a>[Bruke et Windows PowerShell-skript](#tab/use-a-powershell-script)

Et Windows PowerShell-skript er oppgitt, slik at du lett kan konfigurere Azure-ressursene som er beskrevet i [Konfigurere eksport til Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md). Hvis du foretrekker å konfigurere manuelt, kan du hoppe over denne fremgangsmåten og fortsette med fremgangsmåten i delen [Manuell konfigurasjon](#manual-setup).

> [!NOTE]
> Følg fremgangsmåten nedenfor for å kjøre PowerShell-skriptet. Det kan hende at Azure CLI-alternativet «Prøv det» eller å kjøre skriptet på PC-en ikke fungerer.

Følg denne fremgangsmåten for å konfigurere Azure ved hjelp av Windows PowerShell-skriptet. Du må ha rettigheter til å opprette en Azure-ressursgruppe, Azure-ressurser og et Azure AD-program. Hvis du vil ha informasjon om de nødvendige tillatelsene, kan du se [Kontrollere Azure AD-tillatelser](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. I [Azure-portalen](https://portal.azure.com) går du til Azure-målabonnementet. Velg **Cloud Shell**-knappen til høyre for **Søk**-feltet.
2. Velg **PowerShell**.
3. Opprett lagringsplass hvis du blir bedt om det.
4. Gå til kategorien **Azure CLI** og velg **Kopier**.  
5. Åpne Notisblokk, og lim inn PowerShell-skriptet. Lagre filen som ConfigureDataLake.ps1.
6. Last opp Windows PowerShell-skriptet til økten ved hjelp av menyalternativet for opplasting i Cloud Shell.
7. Kjør skriptet .\ConfigureDataLake.ps1.
8. Følg instruksjonene for å kjøre skriptet.
9. Bruk informasjonen fra skriptutdataene til å installere tillegget **Eksporter til Data Lake** i LCS.
10. Bruk informasjonen fra skriptutdataene til å aktivere enhetslageret på **Datatilkoblinger**-siden i Finance (**Systemadministrasjon \> Systemparametere \> Datatilkoblinger**).

### <a name="manual-setup"></a>Manuell konfigurasjon

#### <a name="add-applications-to-the-azure-ad-tenant"></a>Legg til programmer i Azure AD-leieren

1. Gå til **Azure Active Directory** i [Azure-portalen](https://portal.azure.com).
2. Velg **Behandle \> Enterprise-programmer**.
3. Søk etter følgende programmer etter app-ID.

    | Program                              | App-ID                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP Microservices     | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    | AI Builder Authorization Service         | ad40333e-9910-4b61-b281-e3aeeb8c3ef3 |

Hvis du ikke finner noen av de ovennevnte programmene, kan du prøve følgende trinn.

1. Velg **Start**-menyen på den lokale maskinen, og søk etter **powershell**.
2. Velg og hold (eller høyreklikk på) **Windows PowerShell**, og velg deretter **Kjør som administrator**.
3. Kjør følgende kommando for å installere **AzureAD**-modulen.

    `Install-Module -Name AzureAD`

4. Hvis en NuGet-leverandør kreves for å fortsette, velger du **J** for å installere den.
5. Hvis det vises en melding om at repositoriet ikke er klarert, velger du **J** for å fortsette.
6. For hvert program som må legges til, kjører du følgende kommandoer for å legge til programmet i Azure AD. Når du blir bedt om det, logger du på som Azure AD-administrator.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Opprette Azure-ressurser

> [!NOTE]
> Kontroller at du oppretter følgende ressurser i samme Azure AD-forekomst som Dataverse-miljøet. Du kan ikke bruke ressurser fra en annen Azure AD-forekomst.

1. Opprette en ny lagringskonto:

    1. Opprett en lagringskonto i [Azure-portalen](https://portal.azure.com).
    2. I dialogboksen **Opprett lagringskonto** angir du verdier i følgende felter:

        - **Plassering** – Velg datasenteret der miljøet er plassert.
        - **Ytelse** – Vi anbefaler at du velger **Standard**.
        - **Kontotype** – Du må velge **StorageV2**.

    3. Velg **Aktiver** under funksjonen **Hierarkiske navneområder** for alternativet **Data Lake Storage Gen2** i dialogboksen **Avanserte alternativer**. Hvis du deaktiverer denne funksjonen, kan du ikke bruke data som Finance and Operations-apper skriver ved hjelp av tjenester som Power BI-dataflyter.
    4. Velg **Se gjennom og opprett**. Når distribusjonen er fullført, vises den nye ressursen i Azure-portalen.
    5. Gå til lagringskontoen du opprettet.
    6. Velg **Tilgangsnøkler** på menyen til venstre.
    7. Kopier og lagre tilkoblingsstrengen for **Nøkkel1** eller **Nøkkel2**.
    8. Kopier og lagre navnet på lagringskontoen.

2. Opprett et nytt nøkkelhvelv:

    1. Opprett et nøkkelhvelv i [Azure-portalen](https://portal.azure.com).
    2. I **Plassering**-feltet i dialogboksen **Opprett nøkkelhvelv** velger du datasenteret der miljøet er.
    3. Etter at nøkkelhvelvet er opprettet, velger du det i listen og velger deretter **Hemmeligheter**.
    4. Velg **Generer/Importer**.
    5. I feltet **Opplastingsalternativer** i dialogboksen **Opprett en hemmelighet** velger du **Manuell**.
    6. Angi et navn for hemmeligheten. Noter deg navnet, fordi du må angi det senere.
    7. I **Verdi**-feltet angir du tilkoblingsstrengen du fikk fra lagringskontoen i forrige fremgangsmåte.
    8. Velg **Aktivert**, og velg deretter **Opprett**. Hemmeligheten opprettes og legges til i Key Vault.
    9. Gå til **Oversikt over Key Vault**, og noter deg DNS-navnet.

3. Opprett og registrer et Azure AD-program:

    1. Gå til **Azure Active Directory** i [Azure-portalen](https://portal.azure.com), og velg deretter **Appregistreringer**.
    2. Velg **Ny programregistrering**, og angi verdier i følgende felter:

        - **Navn** – Angi navnet på appen.
        - **Programtype** – Velg **Web-API**.
        - **Konfigurasjon av URI for omadressering** – Angi URL-adressen til Dynamics 365-forekomsten, for eksempel `https://yourdynamicsinstance.dynamics.com/auth`.

    3. Gå til appen du nettopp opprettet, og kopier og lagre verdien for **Program-ID (klient)**. Du må angi denne verdien senere når du konfigurerer nøkkelhvelvet.
    4. Gå til **API-tillatelser**, og følg denne fremgangsmåten:

        1. Velg **Legg til en tillatelse**.
        2. Velg **Azure Key Vault**.
        3. Etter at du har valgt delegerte tillatelser, velger du **user\_impersonation**.
        4. Velg **Legg til tillatelser**.

    5. På menyen for appen velger du **Sertifikater \& hemmeligheter**, og deretter følger du denne fremgangsmåten for å opprette Key Vault-hemmeligheter:

        1. Velg **Ny klienthemmelighet**.
        2. Angi et navn i **Nøkkelbeskrivelse**-feltet.
        3. Velg en varighet, og velg deretter **Legg til**. Det genereres en hemmelighet i **Verdi**-feltet.
        4. Kopier og lagre den hemmelige verdien.

4. Opprett Key Vault-hemmeligheter:

    1. Gå til nøkkelhvelvet du opprettet tidligere, og velg **Hemmeligheter**.
    2. Følg denne fremgangsmåten for hvert hemmelige navn i følgende tabell:

        1. Velg **Generer/Importer**.
        2. I feltet **Opplastingsalternativer** i dialogboksen **Opprett en hemmelighet** velger du **Manuell**.
        3. Opprett det hemmelige navnet og verdien fra følgende tabell.
        4. Velg **Aktivert**, og velg deretter **Opprett**. Hemmeligheten opprettes og legges til i Key Vault.

        | Hemmelig navn                       | Hemmelig verdi                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | app-id                            | App-ID-en for programmet du opprettet tidligere                                      |
        | app-secret                        | Klienthemmeligheten du lagret tidligere                                                    |
        | storage-account-name              | Navnet på lagringskontoen du opprettet tidligere, for eksempel **lagringskonto1**       |
        | storage-account-connection-string | Tilkoblingsstrengen du kopierte fra siden **Tilgangsnøkler** for lagringskontoen |

5. Autoriser programmet for tilgang til nøkkelhvelvet:

    1. Åpne nøkkelhvelvet du opprettet tidligere, i [Azure-portalen](https://portal.azure.com).
    2. Velg tilgangspolicyene.
    3. Følg denne fremgangsmåten for hvert program i følgende tabell:

        1. Velg **Legg til tilgangspolicy** for å opprette en tilgangspolicy.
        2. I feltet **Hemmelige tillatelser** velger du tillatelsene fra følgende tabell.
        3. I feltet **Velg sikkerhetskontohaver** søker du etter visningsnavnet for programmet i følgende tabell.
        4. Velg **Velg**.
        5. Velg **Legg til**.
        6. Velg **Lagre**.

        | Søknad                                              | Tillatelser |
        |----------------------------------------------------------|-------------|
        | Visningsnavnet for det nye programmet du opprettet | Hent, Vis   |
        | **Microsoft Dynamics ERP Microservices**                 | Hent, Vis   |

6. Tilordne roller for tilgang til lagringskontoen:

    1. Åpne lagringskontoen du opprettet tidligere, i [Azure-portalen](https://portal.azure.com).
    2. Velg **Tilgangskontroll (IAM)**, og velg deretter **Rolletilordninger**.
    3. Velg **Legg til, Legg til rolletilordning**.
    4. Følg denne fremgangsmåten for hvert program i følgende tabell:

        1. Velg rollen fra følgende tabell.
        2. La feltet **Tilordne tilgang til** være satt til **Azure AD-bruker, -gruppe eller -tjenestekontohaver**.
        3. I **Velg**-feltet angir du programmet fra følgende tabell.
        4. Velg **Lagre**.

        | Søknad                                              | Rolle                        |
        |----------------------------------------------------------|-----------------------------|
        | Visningsnavnet for det nye programmet du opprettet | Eier                       |
        | Visningsnavnet for det nye programmet du opprettet | Bidragsyter                 |
        | Visningsnavnet for det nye programmet du opprettet | Bidragsyter for lagringskonto |
        | Visningsnavnet for det nye programmet du opprettet | Eier av Storage Blob Data     |
        | **AI Builder Authorization Service**                     | Leser for Storage Blob Data    |

# <a name="azure-cli"></a>[Azure CLI](#tab/azure-azure-cli)

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



## <a name="configure-the-data-lake"></a>Konfigurere datasjøen

Følg denne fremgangsmåten for å bruke LCS til å legge til tillegget Azure Data Lake i miljøet.

1. Logg på LCS, og velg deretter **Detaljerte opplysninger** under miljønavnet til høyre på siden.
2. I delen **Miljøtillegg** velger du **Installer et nytt tillegg**.
3. Velg tillegget **Eksporter til Data Lake**.
4. Angi følgende verdier.

    | Verdi                                                              | Beskrivelse |
    |--------------------------------------------------------------------|-------------|
    | Leier-ID-en for Azure-abonnementet der Key Vault er | Leier-ID-en der lagringskontoen, appene og nøkkelhvelvene er. Du finner denne verdien ved å åpne [Azure-portalen](https://portal.azure.com), gå til **Azure Active Directory** og kopiere verdien for **Leier-ID**. |
    | Oppgi DNS-navnet for Key Vault                             | DNS-navnet for nøkkelhvelvet, for eksempel `https://customkeyvault.vault.azure.net/`. (Denne verdien samsvarer med DNS-navnet som brukes i enhetslageret.) |
    | Angi hemmeligheten som inneholder navnet på lagringskontoen   | **storage-account-name** |
    | Hemmelig navn på app-ID-en som skal brukes til å få tilgang til Data Lake          | **app-id** |
    | Hemmelig navn som skal brukes med app-ID-en                                 | **app-secret** |

5. Godta vilkårene, og velg **Installer**.

Tillegget installeres innen noen minutter.

## <a name="configure-ai-builder"></a>Konfigurere AI Builder

1. Logg på LCS, og åpne siden **Miljødetaljer**.
2. Bla til delen **Miljøtillegg**. Du skal kunne se tilleggene som allerede er installert i dette miljøet. Hvis tillegget **Eksporter til Data Lake** ikke er blant dem, konfigurerer du dette tillegget.
3. Velg tillegget **Få innsikt**.
4. Angi følgende verdier på siden med detaljer for tillegget **Få innsikt**.

    | Verdi                                                    | beskrivelse |
    |----------------------------------------------------------|-------------|
    | URL-adresse for CDS-organisasjon                                     | URL-adressen for Dataverse kopiert fra oppføringen over. |
    | ID for CDS-organisasjon                                               | ID-en for Dataverse kopiert fra oppføringen over. |
5. Aktiver **Er dette standardmiljø for leieren din**.
    
## <a name="configure-the-entity-store"></a>Konfigurere enhetslageret

Følg denne fremgangsmåten for å konfigurere enhetslageret i Finance-miljøet ditt.

1. Gå til **Systemadministrasjon \> Oppsett \> Systemparametere \> Datatilkoblinger**.
2. Angi verdier i følgende Key Vault-felter:

    - **Program-ID (klient)** – Angi programklient-ID-en du opprettet tidligere.
    - **Programhemmelighet** – Angi hemmeligheten du lagret for programmet du opprettet tidligere.
    - **DNS-navn** – Du kan finne DNS-navnet (Domain Name System) på siden for programdetaljer for programmet du opprettet tidligere.
    - **Hemmelig navn** – Angi **storage-account-connection-string**.
3. Aktiver **Aktiver Data Lake-integrasjon**.
4. Velg **Test Azure Key Vault**, og kontroller at det ikke er noen feil.
5. Velg **Test Azure storage**, og kontroller at det ikke er noen feil.

## <a name="feedback-and-support"></a>Tilbakemelding og støtte

Send en e-postmelding til [Innsikt i kundebetaling (forhåndsversjon)](mailto:fiap@microsoft.com) hvis du er interessert i å gi tilbakemelding eller trenger støtte.

## <a name="privacy-notice"></a>Personvernerklæring

Forhåndsversjoner (1) kan ha redusert personvern og færre sikkerhetstiltak enn Dynamics 365 Finance and Operations-tjenesten, (2) er ikke inkludert i serviceavtalen (SLA) for denne tjenesten, (3) må ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) har begrenset støtte.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
