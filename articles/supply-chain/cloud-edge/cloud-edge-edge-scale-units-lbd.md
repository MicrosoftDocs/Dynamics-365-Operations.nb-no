---
title: Distribuere kantskalaenheter på egendefinert maskinvare ved hjelp av LBD (forhåndsversjon)
description: Dette emnet beskriver hvordan du klargjør kantskalaenheter ved hjelp av egendefinert maskinvare og distribusjon som er basert på lokale forretningsdata (LBD).
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0ebbdaab9d6f040497d3158db2712e102b6e9aa8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678987"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd-preview"></a>Distribuere kantskalaenheter på egendefinert maskinvare ved hjelp av LBD (forhåndsversjon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)] <!--KFM: Until 11/1/2021 -->

Kantskalaenheter spiller en viktig rolle i den distribuerte hybridtopologien for forsyningskjedeadministrasjon. I hybridtopologien kan du distribuere arbeidsmengder mellom skyen i Supply Chain Management-skysenteret og flere skalaenheter i skyen eller på kanten.

Kantskalaenheter kan distribueres ved å opprette et lokalt forretningsdatamiljø [lokalt miljø](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) og deretter konfigurere det til å fungere som en vektenhet i den distribuerte hybridtopologien for forsyningskjedeadministrasjon. Dette oppnås ved å knytte det lokale LBD-miljøet til et Supply Chain Management-miljø i skyen, som er konfigurert til å fungere som et senter.  

Kantskalaenheter er i forhåndsvisning. Du kan derfor bruke et miljø av denne typen bare i henhold til [forhåndsversjonsbetingelsene](https://aka.ms/scmcnepreviewterms).

Dette emnet beskriver hvordan du konfigurerer et lokal LBD-miljø som en kantskalaenhet og deretter knytter det til et senter.

## <a name="deployment-overview"></a>Oversikt over distribusjon

Her er en oversikt over distribusjonstrinnene.

1. **Aktiver et LBD-spor i LBD-prosjektet i Microsoft Dynamics Lifecycle Services (LCS).**

    Under forhåndsvisning rettes LBD-kantskalaenhetene mot eksisterende LBD-kunder. En ekstra 60-dagers begrenset LBD-sandkasse blir gitt i bare bestemte kundesituasjoner.

1. **Sett opp og distribuer et LBD-miljø med en *tom* database.**

    Bruk LCS til å distribuere LBD-miljøet med den siste topologien og en tom database. Hvis du vil ha mer informasjon, kan du se [Sette opp og distribuere et LBD-miljø med en tom database](#set-up-deploy) senere i dette emnet. Du må bruke Supply Chain Management versjon 10.0.19 med platformoppdatering 43 eller høyere i senter- og skalaenhetsmiljøer.

1. **Last opp målpakker til LBD-prosjektaktiva i LCS.**

    Klargjør program-, plattform- og tilpasningspakker som du bruker i senter- og kantskalaenheten. Hvis du vil ha mer informasjon, kan du se [Last opp målpakker til LBD-prosjektaktiva i LCS](#upload-packages)-delen senere i dette emnet.

1. **Vedlikehold LBD-miljøet med målpakkene.**

    Dette trinnet sørger for at samme build og tilpasninger distribueres i senteret og den nevnte skaleringsenheten. Hvis du vil ha mer informasjon, kan du se [Vedlikehold LBD-miljøet med målpakkene](#service-target-packages) senere i dette emnet.

1. **Fullfør skalaenhetskonfigurasjon og arbeidsmengde.**

    Hvis du vil ha mer informasjon, kan du se [Tilordne LBD-kantskalaenheten til et senter](#assign-edge-to-hub) i dette emnet.

De gjenværende delene av dette emnet gir mer informasjon om hvordan du fullfører disse trinnene.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Sett opp og distribuer et LBD-miljø med en tom database

Dette trinnet oppretter et funksjonelt LBD-miljø. Miljøet har imidlertid ikke nødvendigvis samme program- og plattformversjoner som som sentermiljøet. I tillegg mangler det fremdeles tilpasningene, og det er ennå ikke aktivert for å fungere som en vektenhet.

1. Følg instruksjonene i [Definere og distribuere lokale miljøer (Platformoppdatering 41 og nyere)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Du må bruke Supply Chain Management versjon 10.0.19 med plattformoppdatering 43 eller høyere i senter- og skalaenhetsmiljøer

    > [!IMPORTANT]
    > Les resten av denne delen **før** du går gjennom trinnene i dette emnet.

1. Før du beskriver konfigurasjonen i infrastruktur\\ConfigTemplate.xml-filen, kan du kjøre følgende skript:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Dette skriptet vil fjerne eventuell konfigurasjon som ikke er nødvendig for å distribuere kantskalaenheter.

1. Definer en database som inneholder tomme data, som beskrevet i [Konfigurer databaser](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Bruk den tomme data.bak-filen for dette trinnet.
1. Konfigurere forhåndsdistribusjonsskriptet. Hvis du vil ha mer informasjon, se [Lokal agent og skript for distribusjon før og etter](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Kopier innholdet fra **ScaleUnit**-mappen i **Infrastrukturskript** til **Skript**-mappen i delingen for agentfillagring som ble definert i miljøet. En vanlig bane er \\\\lbdiscsi01\\agent\\Scripts.
    2. Opprett skriptet **PreDeployment.ps1** som starter skriptene ved hjelp av de nødvendige parameterne. Forhåndsdistribusjonsskriptet må legges i **Skript**-mappen i agentens fillagringsdeling. Ellers kan den ikke kjøres. En vanlig bane er \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1.

        Innholdet i preDeployment.ps1-skriptet vil ligne på følgende eksempel.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        & $agentShare\Scripts\Configure-CloudandEdge.ps1 -AgentShare $agentShare -InstanceId '@A' -DatabaseServer 'lbdsqla01.contoso.com' -DatabaseName 'AXDB'
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

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Last opp målpakker til LBD-prosjektaktiva i LCS

Dette trinnet forbereder programversjonen, plattformversjonen og tilpasningene som skal gå over til enhetsmiljøet i LBD-skalaen.

1. Last opp den samme kombinerte program-/plattformpakken som ble brukt i miljømiljøet, inn i aktivabibliotek til det lokale LCS-prosjektet.
1. Hent en kopi av den egendefinerte distribuerbare pakke som ble brukt i sentermiljøet, og last det opp til aktivabibliotek i det lokale LCS-prosjektet.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>Vedlikehold LBD-miljøet med målpakkene

Dette trinnet justerer programversjonen, plattformversjonen og tilpasningene i LBD-skalaenenhetsmiljøet med senteret.

1. Vedlikehold LBD-miljøet med den kombinerte program-/plattformpakken som du lastet opp i forrige trinn.
1. Vedlikehold LBD-miljøet med den egendefinerte distribuerbare pakken du lastet opp i forrige trinn.

    ![Velg Vedlikehold > Bruk oppdateringer i LCS.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Velg Vedlikehold > Bruk oppdateringer i LCS")

    ![Velge tilpasningspakken.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Velge tilpasningspakke")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Tilordne LBD-kantskaleringsenheten til et senter

Mens kantskalaenheter fremdeles er i forhåndsvisning, må du bruke [distribusjons- og konfigurasjonsverktøy for skalaenheter](https://github.com/microsoft/SCMScaleUnitDevTools), som er tilgjengelige på GitHub, til å tilordne LBD-kantskaleringsenheten til et senter. Prosessen gjør at en LBD-konfigurasjon kan fungere som en kantskalaenhet og knytter den til enheten. Prosessen ligner på konfigurasjon av et utviklingsmiljø med én boks.

1. Last ned den siste versjonen av [SCMScaleUnitDevTools](https://github.com/microsoft/SCMScaleUnitDevTools/releases) og fjern innholdet i filen.
1. Lag en kopi av `UserConfig.sample.xml`-filen og gi den navnet `UserConfig.xml`.
1. Opprett et Microsoft Azure Active Directory (Azure AD)-program i Azure AD-leieren din, som nevnt i [Retningslinjer for distribusjon for skaleringsenhet og arbeidsbelasninger](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#aad-application-registrations).
    1. Når du har opprettet det, kan du navigere til Azure AD-programskjemaer (SysAADClientTable) i senteret.
    1. Opprett en ny oppføring, og sett **Klient-ID** til IDen til programmet du opprettet. Sett **Navn** til *ScaleUnits* og **Bruker-ID** til *Admin*.

1. Opprett et AD FS-program (Active Directory Federation Service) som nevnt i [Retningslinjer for distribusjon for skaleringsenhet og arbeidsbelasninger](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#adfs-application-registrations).
    1. Når du har opprettet det, kan du navigere til Azure AD-programskjemaer (SysAADClientTable) i kantskaleringsenheten.
    1. Opprett en ny oppføring, og sett **Klient-ID** til IDen til programmet du opprettet. Sett **Bruker-ID** til *Admin*.

1. Endre `UserConfig.xml`-filen.
    1. Under delen `InterAOSAADConfiguration` angir du informasjon fra Azure AD-programmet du opprettet tidligere.
        - I elementet `AppId` angir du program-IDen til Azure-programmet.
        - I elementet `AppSecret` angir du programhemmeligheten til Azure-programmet.
        - Elementet `Authority` må inneholde URL-adressen som angir sikkerhetsmyndigheten for leietakeren.

        ```xml
        <InterAOSAADConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopty56TGUedDTVhtER-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </InterAOSAADConfiguration>
        ```

    1. I `ScaleUnitConfiguration`-delen for den første `ScaleUnitInstance` endrer du `AuthConfiguration`-delen.
        - I elementet `AppId` angir du program-IDen til Azure-programmet.
        - I elementet `AppSecret` angir du programhemmeligheten til Azure-programmet.
        - Elementet `Authority` må inneholde URL-adressen som angir sikkerhetsmyndigheten for leietakeren.

        ```xml
        <AuthConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopdz.6d3DTVOtf9Lo-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </AuthConfiguration>
        ```

    1. Angi i tillegg følgende verdier for den samme `ScaleUnitInstance`.
        - I elementet `Domain` angir du URL-adressen til senteret. For eksempel: `https://cloudhub.sandbox.operations.dynamics.com/`
        - Kontroller at verdien `EnvironmentType` er angitt i `LCSHosted`-elementet.

    1. I `ScaleUnitConfiguration`-delen for den andre `ScaleUnitInstance` endrer du `AuthConfiguration`-delen.
        - I elementet `AppId` angir du program-IDen til AD FS-programmet.
        - I elementet `AppSecret` angir du programhemmeligheten til ADFS-programmet.
        - Elementet `Authority` må inneholde URL-adressen til AD FS-forekomsten.

        ```xml
        <AuthConfiguration>
            <AppId>26b16f25-21d8-4d36-987b-62df292895aa</AppId>
            <AppSecret>iZFfObgI6lLtY9kEbBjEFV98NqI5_YZ0e5SBcWER</AppSecret>
            <Authority>https://adfs.contoso.com/adfs</Authority>
        </AuthConfiguration>
        ```

    1. Angi i tillegg følgende verdier for den samme `ScaleUnitInstance`.
        - I elementet `Domain` angir du URL-adressen til kantskaleringsenheten. For eksempel: https://ax.contoso.com/
        - Kontroller at verdi-LBD er angitt i `EnvironmentType`-elementet.
        - I `ScaleUnitId`-elementet angir du den samme verdien du angav for `InstanceId` da du konfigurerte forhåndsdistribusjonsskriptet `Configure-CloudandEdge.ps1`.

        > [!NOTE]
        > Hvis du ikke bruker standard-IDen (@A), må du oppdatere ScaleUnitId for hver ConfiguredWorkload under Arbeidsbelastninger-delen.

1. Åpne PowerShell, og naviger til mappen som inneholder `UserConfig.xml`-filen.

1. Kjør verktøyet med denne kommandoen.

    ```powershell
    .\CLI.exe
    ```

    > [!NOTE]
    > Etter hver handling må du starte verktøyet på nytt.

1. I verktøyet velger du **2. Klargjør miljøer for arbeidsmengdeinstallasjon**. Deretter kjører du følgende trinn:
    1. Velg **1. Klargjør senteret**.
    1. Velg **2. Klargjør vektenheten**.

    > [!NOTE]
    > Hvis du ikke kjører denne kommandoen fra en ren installasjon, og den mislykkes, gjør du følgende:
    >
    > - Fjern alle mappene fra `aos-storage`-mappen (unntatt `GACAssemblies`).
    > - Kjør følgende SQL-kommando på forretningsdatabasen (AXDB):
    >
    > ```sql 
    > delete from storagefoler
    > ```

1. Kjør følgende SQL-kommandoer på forretningsdatabasen (AXDB):

    ```sql
    delete from FEATUREMANAGEMENTMETADATA
    delete from FEATUREMANAGEMENTSTATE
    delete from NUMBERSEQUENCESCOPE
    ```

1. Kontroller at endringssporing er aktivert på forretningsdatabasen (AXDB)
    1. Start SQL Server Management Studio (SSMS).
    1. Høyreklikk forretningsdatabasen (AXDB), og velg egenskaper.
    1. I vinduet som åpnes, velger du **Endringssporing** og gjør følgende innstillinger:

        - **Endringssporing:** *Sann*
        - **Oppbevaringsperiode:** *7*
        - **Oppbevaringsenheter:** *Dager*
        - **Automatisk opprydding:** *Sann*

1. I verktøyet velger du **3. Installer arbeidsmengder**. Deretter kjører du følgende trinn:
    1. Velg **1. Installer i senter**.
    1. Velg **2. Installer på Scale Unit**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
