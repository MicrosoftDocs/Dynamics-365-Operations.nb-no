---
title: Konfigurasjon for Finance Insights – versjon 10.0.20 og senere
description: Dette emnet forklarer hvordan du konfigurerer systemet slik at det bruker funksjonene i Finance Insights i versjon 10.0.20 og nyere.
author: ShivamPandey-msft
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex,nofollow
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 8ff20334445fba1db435d7005c4ca9ba18f97f72
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968968"
---
# <a name="configuration-for-finance-insights---version-10020-and-later"></a>Konfigurasjon for Finance Insights – versjon 10.0.20 og senere

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Finance Insights kombinerer funksjonalitet fra Microsoft Dynamics 365 Finance med Dataverse, Azure og AI Builder for å gi organisasjonen kraftige prognoseverktøy. Dette emnet forklarer hvordan du konfigurerer Dynamics 365 Finance versjon 10.0.20 slik at systemet kan bruke funksjonene som er tilgjengelige i Finance Insights.

> [!NOTE]
> Konfigurasjonstrinnene som beskrives i dette emnet, gjelder bare for Finance versjon 10.0.20 og nyere. Hvis du vil konfigurere Finance Insights i versjon 10.0.19 og tidligere, kan du se [Konfigurasjon for Finance Insights – versjoner opptil 10.0.19](configure-for-fin-insites.md).

## <a name="deploy-finance"></a>Distribuere Finance

Følg denne fremgangsmåten for å distribuere miljøene.

1. Opprett eller oppdater et Finance-miljø i Microsoft Dynamics Lifecycle Services (LCS). Miljøet krever appversjon 10.0.20 eller nyere av Finance and Operations-apper.
2. Miljøet må være et miljø med høy tilgjengelighet i sandkassemodus. (Denne typen miljø kalles også et miljø på lag 2.) Hvis du vil ha mer informasjon, kan du se [Miljøplanlegging](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. Hvis du konfigurerer Finance Insights i et sandkassemiljø, må du kanskje kopiere produksjonsdata til dette miljøet for at prediksjoner skal kunne fungere. Prediksjonsmodellen bruker flere år med data til å bygge prediksjoner. Contoso-demodataene inneholder ikke nok historiske data til at prediksjonsmodellen kan læres opp tilstrekkelig. 

## <a name="configure-dataverse"></a>Konfigurer Dataverse

Følg fremgangsmåten nedenfor til å konfigurere Dataverse for Finance Insights.

1. Åpne miljøsiden i LCS, og kontroller at **Power Platform-integrering** allerede er konfigurert.

    - Hvis den allerede er konfigurert, skal Dataverse-miljønavnet som er koblet til Finance-miljøet, vises.
    - Hvis det ikke er konfigurert, følger du denne fremgangsmåten:

        1. Velg **Oppsett**-knappen i delen **Power Platform-integrering**. Konfigurasjonen av miljøet kan ta opptil en time.
        2. Hvis Dataverse-miljøet er riktig konfigurert, skal navnet på Dataverse-miljøet som er koblet til Finance-miljøet, vises.

        > [!NOTE]
        > Etter at du har fullført miljøkonfigurasjonen, må du **ikke** velge **Kobling til CDS for Apps**. Denne knappen kreves ikke for Finance Insights. Hvis du velger den, kan du ikke konfigurere de nødvendige miljøtilleggene i LCS.

## <a name="configure-azure"></a>Konfigurere Azure

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Bruke Azure Cloud Shell til å konfigurere Data Lake-ressurser for Finance Insights

# <a name="use-a-windows-powershell-script"></a>[Bruke et Windows PowerShell-skript](#tab/use-a-powershell-script)

Et Windows PowerShell-skript er oppgitt, slik at du lett kan konfigurere Azure-ressursene som er beskrevet i [Konfigurere eksport til Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md). Hvis du foretrekker å konfigurere manuelt, kan du hoppe over denne fremgangsmåten og i stedet fullføre fremgangsmåten i delen [Manuell konfigurasjon](#manual-setup).

> [!NOTE]
> Bruk fremgangsmåten nedenfor til å kjøre Windows PowerShell-skriptet. Konfigurasjonen fungerer kanskje ikke hvis du bruker alternativet **Prøv det** i Azure CLI eller kjører skriptet på datamaskinen.

Følg denne fremgangsmåten for å bruke Windows PowerShell-skriptet til å konfigurere Azure. Du må ha rettigheter til å opprette en Azure-ressursgruppe, Azure-ressurser og et Azure AD-program. Hvis du vil ha informasjon om de nødvendige tillatelsene, kan du se [Kontrollere Azure AD-tillatelser](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. I [Azure-portalen](https://portal.azure.com) går du til Azure-målabonnementet.
2. Velg **Cloud Shell** til høyre for **Søk**-feltet.
3. Velg **PowerShell**.
4. Opprett lagringsplass hvis du blir bedt om å opprette det.
5. Velg **Kopier** i fanen **Azure CLI**.
6. Åpne en ny fil i Notisblokk, og lim inn i Windows PowerShell-skriptet.
7. Lagre filen som **ConfigureDataLake.ps1**.
8. Last opp Windows PowerShell-skriptet til økten ved å bruke menyalternativet for opplasting i Cloud Shell.
9. Kjør skriptet **.\ConfigureDataLake.ps1**.
10. Følg instruksjonene for å kjøre skriptet.
11. Bruk informasjonen fra skriptutdataene til å installere tillegget Eksporter til Data Lake i LCS.

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

1. Søk etter **powershell** på **Start**-menyen på den lokale datamaskinen.
2. Velg og hold (eller høyreklikk på) **Windows PowerShell**, og velg deretter **Kjør som administrator**.
3. Kjør følgende kommando for å installere **AzureAD**-modulen.

    `Install-Module -Name AzureAD`

4. Hvis en NuGet-leverandør kreves for å fortsette, velger du **J** for å installere den.
5. Hvis du får en melding om at repositoriet ikke er klarert, velger du **J** for å fortsette.
6. For hvert program som må legges til, kjører du følgende kommandoer for å legge til programmet i Azure AD. Når du blir bedt om det, logger du på som Azure AD-administrator.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Opprette Azure-ressurser

> [!NOTE]
> Kontroller at du oppretter følgende ressurser i samme Azure AD-forekomst som Dataverse-miljøet er i. Du kan ikke bruke ressurser fra en annen Azure AD-forekomst.

1. Opprett en lagringskonto:

    1. Opprett en lagringskonto i [Azure-portalen](https://portal.azure.com).
    2. I dialogboksen **Opprett lagringskonto** angir du verdier i følgende felter:

        - **Plassering** – Velg datasenteret der miljøet er plassert.
        - **Ytelse** – Vi anbefaler at du velger **Standard**.
        - **Kontotype** – Du må velge **StorageV2**.

    3. Velg **Aktiver** under funksjonen **Hierarkiske navneområder** for alternativet **Data Lake Storage Gen2** i dialogboksen **Avanserte alternativer**. Hvis du ikke aktiverer denne funksjonen, kan du ikke bruke data som Finance and Operations-apper skriver ved hjelp av tjenester som Power BI-dataflyter.
    4. Velg **Se gjennom og opprett**. Når distribusjonen er fullført, vises den nye ressursen i Azure-portalen.
    5. Gå til lagringskontoen du opprettet.
    6. Velg **Tilgangsnøkler** på menyen til venstre.
    7. Kopier og lagre navnet på lagringskontoen. Du må angi denne verdien senere når du konfigurerer Key Vault-hemmeligheter.

2. Opprett et nøkkelhvelv:

    1. Opprett et nøkkelhvelv i [Azure-portalen](https://portal.azure.com).
    2. I **Plassering**-feltet i dialogboksen **Opprett nøkkelhvelv** velger du datasenteret der miljøet er.
    3. Etter at nøkkelhvelvet er opprettet, kan du gå til **Oversikt over Key Vault** og kopiere og lagre DNS-navnet. Du må angi denne verdien senere når du konfigurerer Data Lake-tillegget.

3. Opprett og registrer et Azure AD-program:

    1. Gå til **Azure Active Directory** i [Azure-portalen](https://portal.azure.com), og velg deretter **Appregistreringer**.
    2. Velg **Ny programregistrering**, og angi verdier i følgende felter:

        - **Navn** – Angi navnet på appen.
        - **Programtype** – Velg **Web-API**.
        - **Konfigurasjon av URI for omadressering** – Angi nettadressen til Dynamics 365-forekomsten, for eksempel `https://yourdynamicsinstance.dynamics.com/auth`.

    3. Gå til appen du nettopp opprettet, og kopier og lagre verdien for **Program-ID (klient)**. Du må angi denne verdien senere når du konfigurerer Key Vault-hemmeligheter.
    4. Gå til **API-tillatelser**, og følg denne fremgangsmåten:

        1. Velg **Legg til en tillatelse**.
        2. Velg **Azure Key Vault**.
        3. Etter at du har valgt delegerte tillatelser, velger du **user\_impersonation**.
        4. Velg **Legg til tillatelser**.

    5. På menyen for appen velger du **Sertifikater \& hemmeligheter**, og deretter følger du denne fremgangsmåten for å opprette Key Vault-hemmeligheter:

        1. Velg **Ny klienthemmelighet**.
        2. Angi et navn i **Nøkkelbeskrivelse**-feltet.
        3. Velg en varighet, og velg deretter **Legg til**. Det genereres en hemmelighet i **Verdi**-feltet.
        4. Kopier og lagre verdien for klienthemmelighet. Du må angi denne verdien senere når du konfigurerer Key Vault-hemmeligheter.

4. Opprett Key Vault-hemmeligheter:

    1. Gå til nøkkelhvelvet du opprettet tidligere, og velg **Hemmeligheter**.
    2. Følg denne fremgangsmåten for hvert hemmelige navn i følgende tabell:

        1. Velg **Generer/Importer**.
        2. I feltet **Opplastingsalternativer** i dialogboksen **Opprett en hemmelighet** velger du **Manuell**.
        3. Opprett det hemmelige navnet og verdien fra tabellen.
        4. Velg **Aktivert**, og velg deretter **Opprett**. Hemmeligheten opprettes og legges til i Key Vault.

        | Hemmelig navn                       | Hemmelig verdi                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | app-id                            | App-ID-en for programmet du opprettet tidligere.                                      |
        | app-secret                        | Klienthemmeligheten du lagret tidligere.                                                    |
        | storage-account-name              | Navnet på lagringskontoen du opprettet tidligere, for eksempel **storageaccount1**.       |

5. Autoriser programmet for tilgang til nøkkelhvelvet:

    1. Åpne nøkkelhvelvet du opprettet tidligere, i [Azure-portalen](https://portal.azure.com).
    2. Velg tilgangspolicyene.
    3. Følg denne fremgangsmåten for hvert program i følgende tabell:

        1. Velg **Legg til tilgangspolicy** for å opprette en tilgangspolicy.
        2. I feltet **Hemmelige tillatelser** velger du tillatelsene fra tabellen.
        3. I feltet **Velg sikkerhetskontohaver** søker du etter visningsnavnet for programmet i tabellen.
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

        1. Velg rollen fra tabellen.
        2. La feltet **Tilordne tilgang til** være satt til **Azure AD-bruker, -gruppe eller -tjenestekontohaver**.
        3. I **Velg**-feltet angir du programmet fra tabellen.
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

## <a name="configure-the-export-to-data-lake-add-in"></a>Konfigurere tillegget Eksporter til Data Lake

Følg denne fremgangsmåten for å bruke LCS til å legge til tillegget Eksporter til Data Lake i miljøet.

1. Logg på LCS, og velg deretter **Detaljerte opplysninger** under miljønavnet til høyre på siden.
2. I delen **Miljøtillegg** velger du **Installer et nytt tillegg**.
3. Velg tillegget **Eksporter til Data Lake**.
4. Angi følgende verdier.

    | Verdi                                                              | Beskrivelse |
    |--------------------------------------------------------------------|-------------|
    | Leier-ID-en for Azure-abonnementet der Key Vault er | Leier-ID-en der lagringskontoen, appene og nøkkelhvelvene er. Du henter denne verdien ved å åpne [Azure-portalen](https://portal.azure.com), gå til **Azure Active Directory** og kopiere verdien for **Leier-ID**. |
    | Oppgi DNS-navnet for Key Vault                             | DNS-navnet for nøkkelhvelvet, for eksempel `https://customkeyvault.vault.azure.net/`. |
    | Angi hemmeligheten som inneholder navnet på lagringskontoen   | **storage-account-name** |
    | Hemmelig navn på app-ID-en som skal brukes til å få tilgang til Data Lake          | **app-id** |
    | Hemmelig navn for appklienthemmelighet                                  | **app-secret** |

5. Godta vilkårene, og velg deretter **Installer**.

Tillegget installeres innen noen minutter.

## <a name="configure-the-finance-insights-add-in"></a>Konfigurere Finance Insights-tillegget

> [!NOTE]
> Hvis du tidligere har installert Få innsikt-tillegget, avinstallerer du det før du fullfører fremgangsmåten nedenfor.

Følg denne fremgangsmåten for å installere Finance Insights-tillegget.

1. Logg på LCS, og velg deretter **Detaljerte opplysninger** under miljønavnet til høyre på siden.
2. I delen **Miljøtillegg** velger du **Installer et nytt tillegg**.
3. Velg **Finance Insights**-tillegget.
4. Godta vilkårene, og velg deretter **Installer**.

Det kan ta flere minutter å installere tillegget.

## <a name="feedback-and-support"></a>Tilbakemelding og støtte

Hvis du er interessert i å gi tilbakemelding eller vil ha kundestøtte, kan du sende en e-postmelding til [Finance Insights](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
