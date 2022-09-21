---
title: Distribusjonsretningslinjer for eksempel på bilagsskriverintegrering for Italia (eldre)
description: Denne artikkelen inneholder retningslinjer for distribusjon av eksemplet på integrering av bilagsskriver for Italia fra Microsoft Dynamics 365 Commerce Retail Software Development Kit (SDK).
author: EvgenyPopovMBS
ms.date: 08/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 275759ffec470c6188f734968f4b18b641a49212
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474160"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>Distribusjonsretningslinjer for eksempel på bilagsskriverintegrering for Italia (eldre)

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Du bør bare følge retningslinjene i denne artikkelen hvis du bruker Microsoft Dynamics 365 Commerce, versjon 10.0.28 eller tidligere. Som i Commerce, versjon 10.0.29 er eksemplet på integrering av bilagsskriveren for Italia tilgjengelig i Commerce Software Development Kit (SDK). Hvis du vil ha mer informasjon, kan du se [Konfigurer kanalkomponenter](./emea-ita-fpi-sample.md#configure-channel-components).

Denne artikkelen inneholder retningslinjer for distribusjon av eksemplet på bilagsskriverintegrering for Italia fra Dynamics 365 Commerce Retail SDK på en virtuell utviklermaskin (VM) i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon om dette eksemplet på regnskapsintegrering, kan du se [Eksempler på bilagsskriverintegrering for Italia](emea-ita-fpi-sample.md). 

Eksempelet på regnskapsintegrering for Italia er en del av Retail SDK. Hvis du vil ha informasjon om hvordan du installerer og bruker SDK, se [Arkitektur for Retail Software Development Kit (SDK)](../dev-itpro/retail-sdk/retail-sdk-overview.md). Dette eksemplet består av utvidelser for Commerce Runtime (CRT) og maskinvarestasjon. Hvis du vil kjøre dette eksemplet, må du endre og bygge prosjektene CRT og maskinvarestasjon. Vi anbefaler at du bruker en uendret Retail SDK til å foreta endringene som er beskrevet i denne artikkelen. Vi anbefaler også at du bruker et kildekontrollsystem for eksempel Azure DevOps der ingen filer er endret ennå.

## <a name="development-environment"></a>Utviklingsmiljø

Følg denne fremgangsmåten for å definere et distribusjonsmiljø slik at du kan teste og utvide eksemplet.

### <a name="commerce-runtime-extension-components"></a>Commerce Runtime-utvidelseskomponenter

CRT-utvidelseskomponentene er inkludert i Retail SDK. Du kan fullføre følgende fremgangsmåter ved å åpne løsningen **CommerceRuntimeSamples.sln** under **RetailSdk\\SampleExtensions\\CommerceRuntime**.

1. Finn prosjektet **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample**, og bygg det.
2. I mappen **Extensions.DocumentProvider.EpsonFP90IIISample\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Commerce Scale Unit:** Kopier filen til **\\bin\\ext**-mappen under områdplasseringen Internet Information Services (IIS) Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Kopier filen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Commerce Scale Unit:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Commerce Scale Unit-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Start Commerce Scale Unit på nytt:

    - **Commerce Scale Unit:** Start Commerce Scale Unit-området på nytt fra IIS Manager.
    - **Klientmegler:** Avslutt prosessen **dllhost.exe** i Oppgavebehandling, og start deretter Modern POS på nytt.

### <a name="hardware-station-extension-components"></a>Utvidelseskomponenter for maskinvarestasjon

Utvidelseskomponentene for maskinvarestasjon er inkludert i Retail SDK. Du kan fullføre følgende fremgangsmåter ved å åpne løsningen **HardwareStationSamples.sln** under **RetailSdk\\SampleExtensions\\HardwareStation**.

1. Finn prosjektet **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample**, og bygg det.
2. I mappen **Extensions.EpsonFP90IIIFiscalDeviceSample\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll**.
3. Kopier samlingsfilen til en distribuert maskinvarestasjonsmaskin:

    - **Ekstern maskinvarestasjon:** Kopier filen til **bin**-mappen under stasjonsområdeplasseringen for IIS-maskinvare.
    - **Lokal maskinvarestasjon:** Kopier filen til Modern POS-klientmeglingsplasseringen.

4. Finn konfigurasjonsfilen for maskinvarestasjonens utvidelser. Filen kalles **HardwareConfig.Extension.config**:

    - **Ekstern maskinvarestasjon:** Filen ligger under stasjonsområdeplasseringen for IIS-maskinvare.
    - **Lokal maskinvarestasjon:** Filen ligger under Modern POS-klientmeglingsplasseringen.

5. Legg til følgende del i **sammensetningsdelen** av konfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. Start tjenesten maskinvarestasjon på nytt:

    - **Ekstern maskinvarestasjon:** Start maskinvarstasjonen på nytt fra IIS Manager.
    - **Lokal maskinvarestasjon:** Avslutt prosessen **dllhost.exe** i Oppgavebehandling, og start deretter Modern POS på nytt.

## <a name="production-environment"></a>Produksjonsmiljø

For å opprette distribuerbare pakker som inneholder Commerce-komponenter, og for å bruke disse pakkene i et produksjonsmiljø, følger du denne fremgangsmåten.

1. Fullfør fremgangsmåten som beskrives i delen [Utviklingsmiljø](#development-environment) tidligere i denne artikkelen.
2. Gjør følgende endringer i konfigurasjonsfilene for pakker i mappen **RetailSdk\\Assets**:

    1. I konfigurasjonsfilene **commerceruntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** legger du til følgende linje i **sammensetningsdelen**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    1. I konfigurasjonsfilen **HardwareStation.Extension.config** legger du til følgende linje i **sammensetningsdelen**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. Gjør følgende endringer i pakkekonfigurasjonsfilen **Customization.settings** i **BuildTools**-mappen:

    1. Legg til følgende linje for å ta med CRT-utvidelsen i pakkene som kan distribueres.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    1. Legg til følgende linje for å ta med utvidelsen for maskinvarestasjon i pakkene som kan distribueres.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. Gjør følgende endringer i filen **Sdk.ModernPos.Shared.csproj** i mappen **Packages\_SharedPackagingProjectComponents** for å ta med ressursfilene for Italia i pakker som kan distribueres:

    1. Legg til en **ItemGroup**-del som inneholder noder som peker mot ressursfilene for de ønskede oversettelsene. Pass på at du angir riktige navneområder og eksempelnavn. Følgende eksempel legger til ressursnoder for de nasjonale innstillingene **it** og **it-CH**.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. I delen **Target Name="CopyPackageFiles"** legger du til én linje for hver nasjonale innstilling, som vist i eksemplet nedenfor.

        ```xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it-CH" SkipUnchangedFiles="true" />
        ```

5. Gjør følgende endringer i filen **Sdk.RetailServerSetup.proj** i mappen **Packages\_SharedPackagingProjectComponents** for å ta med ressursfilene for Italia i pakker som kan distribueres:

    1. Legg til en **ItemGroup**-del som inneholder noder som peker mot ressursfilene for de ønskede oversettelsene. Pass på at du angir riktige navneområder og eksempelnavn. Følgende eksempel legger til ressursnoder for de nasjonale innstillingene **it** og **it-CH**.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. I delen **Target Name="CopyPackageFiles"** legger du til én linje for hver nasjonale innstilling, som vist i eksemplet nedenfor.

        ``` xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it-CH" SkipUnchangedFiles="true" />
        ```

6. Start MSBuild Command Prompt for Visual Studio-verktøyet, og kjør deretter **msbuild** under Retail SDK-mappen for å opprette distribuerbare pakker.
7. Ta i bruk pakkene via LCS eller manuelt. Hvis du vil ha mer informasjon, kan du se [Opprette distribuerbare pakker](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Utforming av utvidelser

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime-utvidelsesutforming

Formålet med filtypen som er en regnskapsdokumentleverandør, er å generere skriverpesifikke dokumenter og håndtere svar fra bilagsskriveren.

CRT-utvidelsen er **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample**.

Hvis du vil ha mer informasjon om utformingen av regnskapsintegreringsløsningen, kan du se [Bilagsregistreringsprosess og regnskapsintegreringeseksempler for regnskapsenheter og -tjenester](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Forespørselsbehandler

Forespørselsbehandleren **DocumentProviderEpsonFP90III** er startpunktet for forespørselen om å generere dokumenter fra bilagsskriveren.

Behandleren arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på koblingsdokumentleverandøren som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler:

- **GetFiscalDocumentDocumentProviderRequest** – Denne forespørselen inneholder informasjon om hvilke dokumenter som skal genereres. Det returnerer et skriverspesifikk dokument som skal registreres i bilagsskriveren.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Denne forespørselen returnerer listen over hendelser du kan abonnere på. For øyeblikket støttes følgende hendelser: salg, utskrift av X-rapport og utskrift av Z-rapport.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen ligger i **Konfigurasjon**-mappen for utvidelsesprosjektet: Formålet med filen er å aktivere innstillinger for dokumentleverandøren som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering. Følgende innstillinger legges til:

- Tilordning av mva-koder
- Tilordning av mva-satser
- Tilordning av betalingsmiddeltype
- Strekkodetype for kvitteringsnummer
- Bankinnbetalingstype

### <a name="hardware-station-extension-design"></a>Utvidelsesutforming for maskinvarestasjon

Formålet med utvidelsen som er en regnskapskobling, er å kommunisere med bilagsskriveren.

Utvidelsen for maskinvarestasjon er **HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample**. Denne utvidelsen bruker HTTP-protokollen til å sende dokumenter som CRT-utvidelsen genererer til bilagsskriveren. Den håndterer også svarene som mottas fra bilagsskriveren.

#### <a name="request-handler"></a>Forespørselsbehandler

Forespørselsbehandleren **EpsonFP90IIISample** er startpunktet for behandling av forespørsler til den eksterne regnskapsenheten.

Behandleren arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på regnskapskoblingen som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler:

- **SubmitDocumentFiscalDeviceRequest** – Denne forespørselen sender dokumenter til skriveren og returnerer svaret fra bilagsskriveren.
- **IsReadyFiscalDeviceRequest** – Denne forespørselen brukes for en tilstandskontroll av enheten.
- **InitializeFiscalDeviceRequest** – Denne forespørselen brukes til å initialisere skriveren.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen ligger i **Konfigurasjon**-mappen for utvidelsesprosjektet: Formålet med filen er å aktivere innstillinger for koblingen som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering. Følgende innstillinger legges til:

- **Sluttpunktadresse** – URL-adressen til skriveren.
- **Dato- og tidssynkronisering** – En verdi som angir om datoen og klokkeslettet for skriveren må synkroniseres med den tilkoblede maskinvarestasjonen.
