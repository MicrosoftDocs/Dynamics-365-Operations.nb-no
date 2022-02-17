---
title: Distribuer kantskalaenheter på egendefinert maskinvare ved hjelp av LBD
description: Dette emnet beskriver hvordan du klargjør kantskalaenheter ved hjelp av egendefinert maskinvare og distribusjon som er basert på lokale forretningsdata (LBD).
author: cabeln
ms.date: 01/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 1204b65e76c107c29a94a61c321064a87c7571fb
ms.sourcegitcommit: 948978183a1da949e35585b28b8e85a63b6c12b1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/25/2022
ms.locfileid: "8024548"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd"></a>Distribuer kantskalaenheter på egendefinert maskinvare ved hjelp av LBD

[!include [banner](../includes/banner.md)]

Kantskalaenheter spiller en viktig rolle i den distribuerte hybridtopologien for forsyningskjedeadministrasjon. I hybridtopologien kan du distribuere arbeidsmengder mellom skyen i Supply Chain Management-skysenteret og flere skalaenheter i skyen eller på kanten.

Kantskalaenheter kan distribueres ved å opprette et lokalt forretningsdatamiljø [lokalt miljø](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) og deretter konfigurere det til å fungere som en vektenhet i den distribuerte hybridtopologien for forsyningskjedeadministrasjon. Dette oppnås ved å knytte det lokale LBD-miljøet til et Supply Chain Management-miljø i skyen, som er konfigurert til å fungere som et senter.  

Dette emnet beskriver hvordan du konfigurerer et lokal LBD-miljø som en kantskalaenhet og deretter knytter det til et senter.

## <a name="infrastructure-considerations"></a>Infrastrukturhensyn

Kantskalaenheter kjøres i lokale miljøer, slik at infrastrukturkravene er ganske like. Det er imidlertid bestemte forskjeller som bør merkes:

- Kantskalaenheter bruker ikke Financial Reporting, så de trenger ikke Financial Reporting-noder.
- Produksjons- og lagerbelastningen er ikke databehandlingsintensive, så vurder derfor å beregne databehandlingskraften for AOS-noder i henhold til dette.

## <a name="deployment-overview"></a>Oversikt over distribusjon

Her er en oversikt over distribusjonstrinnene.

1. **Aktiver et LBD-spor i LBD-prosjektet i Microsoft Dynamics Lifecycle Services (LCS).**

1. **Sett opp og distribuer et LBD-miljø med en *tom* database.**

    Bruk LCS til å distribuere LBD-miljøet med den siste topologien og en tom database. Hvis du vil ha mer informasjon, kan du se [Sette opp og distribuere et LBD-miljø med en tom database](#set-up-deploy) senere i dette emnet. Du må bruke Supply Chain Management versjon 10.0.21 eller senere i senter- og skalaenhetsmiljøer.

1. **Last opp målpakker til LBD-prosjektaktiva i LCS.**

    Klargjør program-, plattform- og tilpasningspakker som du bruker i senter- og kantskalaenheten. Hvis du vil ha mer informasjon, kan du se [Last opp målpakker til LBD-prosjektaktiva i LCS](#upload-packages)-delen senere i dette emnet.

1. **Vedlikehold LBD-miljøet med målpakkene.**

    Dette trinnet sørger for at samme build og tilpasninger distribueres i senteret og den nevnte skaleringsenheten. Hvis du vil ha mer informasjon, kan du se [Vedlikehold LBD-miljøet med målpakkene](#service-target-packages) senere i dette emnet.

1. **Fullfør skalaenhetskonfigurasjon og arbeidsmengde.**

    Hvis du vil ha mer informasjon, kan du se [Tilordne LBD-kantskalaenheten til et senter](#assign-edge-to-hub) i dette emnet.

De gjenværende delene av dette emnet gir mer informasjon om hvordan du fullfører disse trinnene.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Sett opp og distribuer et LBD-miljø med en tom database

Dette trinnet oppretter et funksjonelt LBD-miljø. Miljøet har imidlertid ikke nødvendigvis samme program- og plattformversjoner som som sentermiljøet. I tillegg mangler det fremdeles tilpasningene, og det er ennå ikke aktivert for å fungere som en vektenhet.

1. Følg instruksjonene i [Definere og distribuere lokale miljøer (Platformoppdatering 41 og nyere)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Du må bruke Supply Chain Management versjon 10.0.21 eller senere i senter- og skalaenhetsmiljøer. I tillegg må du bruke versjon 2.12.0 eller senere av infrastrukturskriptene. 

    > [!IMPORTANT]
    > Les resten av denne delen **før** du går gjennom trinnene i dette emnet.

1. Før du beskriver konfigurasjonen i infrastruktur\\ConfigTemplate.xml-filen, kan du kjøre følgende skript:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Dette skriptet vil fjerne eventuell konfigurasjon som ikke er nødvendig for å distribuere kantskalaenheter.

1. Definer en database som inneholder tomme data, som beskrevet i [Konfigurer databaser](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Bruk den tomme data.bak-filen for dette trinnet.
1. Når du har fullført trinnet [Konfigurer databaser](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb), kjører du følgende skript for å konfigurere Scale Unit Alm Orchestrator-databasen.

    > [!NOTE]
    > Ikke konfigurer Financial Reporting-databasen under trinnet [Konfigurer databaser](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb).

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EdgeScaleUnit
    ```

    Skriptet Initialize-Database.ps1 utfører følgende handlinger:

    1. Opprett en tom database med navnet **ScaleUnitAlmDb**.
    2. Tilordne brukerne til databaseroller, basert på tabellen nedenfor.

        | Bruker            | Type | Databaserolle |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | gMSA | db\_owner     |

1. Fortsett med å følge instruksjonene i [Definere og distribuere lokale miljøer (Platformoppdatering 41 og nyere)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md).
1. Når du har fullført trinnet [Konfigurer AD FS](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb), følger du denne fremgangsmåten:

    1. Opprett en ny AD FS-app (Active Directory Federation Services), som gjør det mulig for Alm Orchestration-tjenesten å kommunisere med Application Object Server (AOS).

        ```powershell
        # Host URL is your DNS record\host name for accessing the AOS
        .\Create-ADFSServerApplicationForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
        ```

    1. Opprett en ny Azure Active Directory-app (Azure AD) som gjør det mulig for Alm Orchestration-tjenesten å kommunisere med Scale Unit Management-tjenesten.

        ```powershell
        # Example .\Create-SumAADApplication.ps1 -ConfigurationFilePath ..\ConfigTemplate.xml -TenantId '6240a19e-86f1-41af-91ab-dbe29dbcfb95' -ApplicationDisplayName 'EdgeAgent-SUMCommunication-EN01'
        .\Create-SumAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                       -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                       -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
        ```

1. Fortsett med å følge instruksjonene i [Definere og distribuere lokale miljøer (Platformoppdatering 41 og nyere)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Når du må angi konfigurasjonen for den lokale agenten, må du passe på at du aktiverer Edge Scale Unit-funksjonene og angir alle nødvendige parametere.

    ![Aktivering av Edge Scale Unit-funksjoner.](media/EnableEdgeScaleUnitFeatures.png "Aktivering av Edge Scale Unit-funksjoner.")

1. Før du distribuerer miljøet fra LCS, må du konfigurere forhåndsdistribusjonsskriptet. Hvis du vil ha mer informasjon, se [Lokal agent og skript for distribusjon før og etter](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Kopier Configure-CloudAndEdge.ps1-skriptet fra **ScaleUnit**-mappen i **Infrastrukturskript** til **Skript**-mappen i delingen for agentfillagring som ble definert i miljøet. En vanlig bane er \\\\lbdiscsi01\\agent\\Scripts.
    2. Opprett skriptet **PreDeployment.ps1** som starter skriptene ved hjelp av de nødvendige parameterne. Forhåndsdistribusjonsskriptet må legges i **Skript**-mappen i agentens fillagringsdeling. Ellers kan den ikke kjøres. En vanlig bane er \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1.

        Innholdet i preDeployment.ps1-skriptet vil ligne på følgende eksempel.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        . $PSScriptRoot\Configure-CloudAndEdge.ps1 -AgentShare $agentShare -InstanceId '@A'
        ```

        > [!NOTE]
        > InstanceId-parameteren bør bare være to tegn. Det første tegnet er @ og det andre kan være en hvilken som helst stor bokstav i det engelsk alfabetet.
        >
        > - Gyldige verdier:
        >   - @D
        >   - @X
        > - Ugyldige verdier:
        >   - @a
        >   - @4
        >   - @#

1. Distribuer miljøet ved å bruke den nyeste basistopologien som er tilgjengelig.
1. Når miljøet er distribuert, følger du disse trinnene:

    1. Kjør følgende SQL-kommandoer på forretningsdatabasen (AXDB).

        ```sql
        ALTER TABLE dbo.NUMBERSEQUENCETABLE ENABLE CHANGE_TRACKING WITH (TRACK_COLUMNS_UPDATED = ON)
        delete from NumberSequenceTable
        delete from NumberSequenceReference
        delete from NumberSequenceScope
        delete from FeatureManagementMetadata
        delete from FeatureManagementState
        delete from SysFeatureStateV0
        ```

    1. Øk den samtidige maksimale satsvise økten til en verdi som er mer enn 4.

        ```sql
        Update batchserverconfig set maxbatchsessions = '<Replace with number of concurrent batch tasks you want>'
        ```

    1. Kontroller at endringssporing er aktivert på forretningsdatabasen (AXDB).

        1. Åpne SQL Server Management Studio (SSMS).
        1. Velg og hold (eller høyreklikk på) på forretningsdatabasen (AXDB), og velg deretter **Egenskaper**.
        1. I vinduet som vises, velger du **Endringssporing** og angir deretter følgende verdier:

            - **Endringssporing:** *Sann*
            - **Oppbevaringsperiode:** *7*
            - **Oppbevaringsenheter:** *Dager*
            - **Automatisk opprydding:** *Sann*

    1. Legg til ID-en for AD FS-appen du opprettet tidligere (ved hjelp av skriptet Create-ADFSServerApplicationForEdgeScaleUnits.ps1), i Azure AD-apptabellen i vektenheten. Du kan fullføre dette trinnet manuelt via brukergrensesnittet. Du kan også fullføre det via databasen ved hjelp av følgende skript.

        ```sql
        DECLARE @ALMOrchestratorId NVARCHAR(76) = '<Replace with the ADFS Application ID created in a previous step>';

        IF NOT EXISTS (SELECT TOP 1 1 FROM SysAADClientTable WHERE AADClientId = @ALMOrchestratorId)
        BEGIN
            INSERT INTO SysAADClientTable (AADClientId, UserId, Name, ModifiedBy, CreatedBy)
            VALUES (@ALMOrchestratorId, 'ScaleUnitManagement', 'Scale Unit Management', 'Admin', 'Admin');
        END
        ```

## <a name="set-up-an-azure-key-vault-and-an-azure-ad-application-to-enable-communication-between-scale-units"></a><a name="set-up-keyvault"></a>Konfigurer Azure Key Vault og en Azure AD-app for å muliggjøre kommunikasjon mellom skalaenheter

1. Når miljøet er distribuert, oppretter du en ekstra Azure AD-app for å muliggjøre klarert kommunikasjon mellom senteret og skalaenheten.

    ```powershell
    .\Create-SpokeToHubAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                          -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                          -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
    ```

1. Når du har opprettet appen, må du opprette en klienthemmelighet og lagre informasjonen i Azure Key Vault. I tillegg må du gi tilgang til Azure AD-appen som ble opprettet, slik at den kan hente frem hemmelighetene som er lagret i Key Vault. Av praktiske årsaker utfører følgende skript automatisk alle de nødvendige handlingene.

    ```powershell
    .\Create-SpokeToHubAADAppSecrets.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                         -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                         -SubscriptionName '<Any subscription within your tenant>' `
                                         -ResourceGroupName '<Any resource group within your subscription>' `
                                         -KeyVaultName '<Any key vault within your resource group>' `
                                         -Location '<Any Azure location where Azure Key Vault is available>' `
                                         -LCSEnvironmentId '<The LCS environment ID of your deployed scale unit>' `
    ```

    > [!NOTE]
    > Hvis det ikke finnes en Key Vault-forekomst som har den angitte **KeyVaultName**-verdien, oppretter skriptet automatisk en.

1. Legg til ID-en for Azure AD-appen du akkurat opprettet (da du brukte skriptet Create-SpokeToHubAADApplication.ps1), i Azure AD-apptabellen i senteret. Du kan fullføre dette trinnet manuelt via brukergrensesnittet.

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Last opp målpakker til LBD-prosjektaktiva i LCS

Dette trinnet forbereder programversjonen, plattformversjonen og tilpasningene som skal gå over til enhetsmiljøet i LBD-skalaen.

1. Last opp den samme kombinerte program-/plattformpakken som ble brukt i miljømiljøet, inn i aktivabibliotek til det lokale LCS-prosjektet.
1. Hent en kopi av den egendefinerte distribuerbare pakke som ble brukt i sentermiljøet, og last det opp til aktivabibliotek i det lokale LCS-prosjektet.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>Vedlikehold LBD-miljøet med målpakkene

Dette trinnet justerer programversjonen, plattformversjonen og tilpasningene i LBD-skalaenenhetsmiljøet med senteret.

1. Vedlikehold LBD-miljøet med den kombinerte program-/plattformpakken som du lastet opp i forrige trinn.
1. Vedlikehold LBD-miljøet med den egendefinerte distribuerbare pakken du lastet opp i forrige trinn.

    ![Bruk av oppdateringer i LCS.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Bruk av oppdateringer i LCS")

    ![Velge tilpasningspakken.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Velge tilpasningspakke")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Tilordne LBD-kantskaleringsenheten til et senter

Du konfigurerer og administrerer kantskaleringsenheten via Scale Unit Management-portalen. Hvis du vil ha mer informasjon, kan du se [Administrer skaleenheter og arbeidsmengder ved hjelp av Scale Unit Manager-portalen](./cloud-edge-landing-page.md#scale-unit-manager-portal).

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
