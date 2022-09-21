---
title: Distribusjonsretningslinjer for eksempel på integrering av regnskapsregistreringstjenesten for Tsjekkia (eldre)
description: Denne artikkelen inneholder retningslinjer for distribusjon av eksemplet på integrering av bilagsskriver for Tsjekkia fra Microsoft Dynamics 365 Commerce Retail Software Development Kit (SDK).
author: EvgenyPopovMBS
ms.date: 08/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 7406a6443f851fcfa9757deed57c108ba7b6e069
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473911"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-the-czech-republic-legacy"></a>Distribusjonsretningslinjer for eksempel på integrering av regnskapsregistreringstjenesten for Tsjekkia (eldre)

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Du må bare følge retningslinjene i denne artikkelen hvis du bruker Microsoft Dynamics 365 Commerce, versjon 10.0.28 eller tidligere. Som i Commerce, versjon 10.0.29 er eksemplet på integrering av regnskapsregistreringstjenesten for Den tsjekkiske republikk tilgjengelig i Commerce Software Development Kit (SDK). Hvis du vil ha mer informasjon, kan du se [Konfigurer kanalkomponenter](./emea-cze-fi-sample.md#configure-channel-components).

Denne artikkelen inneholder retningslinjer for distribusjon av eksemplet på integrering av regnskapsregistreringstjenesten for Tsjekkia fra Dynamics 365 Commerce Retail SDK på en virtuell utviklermaskin (VM) i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon om dette eksemplet på regnskapsintegrering, kan du se [Eksempler på integrering av regnskapsregistreringstjenesten for Tsjekkia](emea-cze-fi-sample.md). 

Eksempelet på regnskapsintegrering for Tsjekkia er en del av Retail SDK. Hvis du vil ha informasjon om hvordan du installerer og bruker SDK, se [Arkitektur for Retail Software Development Kit (SDK)](../dev-itpro/retail-sdk/retail-sdk-overview.md). Dette eksemplet består av utvidelser for Commerce Runtime (CRT) og maskinvarestasjon. Hvis du vil kjøre dette eksemplet, må du endre og bygge prosjektene CRT og maskinvarestasjon. Vi anbefaler at du bruker en uendret Retail SDK til å foreta endringene som er beskrevet i denne artikkelen. Vi anbefaler også at du bruker et kildekontrollsystem for eksempel Azure DevOps der ingen filer er endret ennå.

## <a name="development-environment"></a>Utviklingsmiljø

Følg denne fremgangsmåten for å definere et distribusjonsmiljø slik at du kan teste og utvide eksemplet.

### <a name="enable-commerce-runtime-extensions"></a>Aktiver utvidelser for Commerce Runtime

CRT-utvidelseskomponentene er inkludert i CRT-eksemplene. Du kan fullføre følgende fremgangsmåter ved å åpne løsningen **CommerceRuntimeSamples.sln** under **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample-komponent

1. Finn prosjektet **Runtime.Extensions.DocumentProvider.EFRSample**, og bygg det.
2. I mappen **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Commerce Scale Unit:** Kopier filen til **\\bin\\ext**-mappen under områdplasseringen Internet Information Services (IIS) Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Kopier filen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Commerce Scale Unit:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Commerce Scale Unit-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR-komponenten

1. Finn prosjektet **Runtime.Extensions.DocumentProvider.DataModelEFR**, og bygg det.
2. I mappen **Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Commerce Scale Unit:** Kopier filen til **\\bin\\ext**-mappen under områdplasseringen IIS Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Kopier filen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Commerce Scale Unit:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Commerce Scale Unit-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Konfigurasjonsfil for utvidelse

1. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Commerce Scale Unit:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Commerce Scale Unit-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

2. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>Aktivere utvidelser for regnskapskobling

Du kan aktivere utvidelser for regnskapskobling på [maskinvarestasjonen](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) eller i [POS-kassen](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

### <a name="enable-hardware-station-extensions"></a>Aktiver utvidelser for maskinvarestasjon

Utvidelseskomponentene for maskinvarestasjonen inkluderes i eksemplene for maskinvarestasjon. Du kan fullføre følgende fremgangsmåter ved å åpne løsningen **HardwareStationSamples.sln** under **RetailSdk\\SampleExtensions\\HardwareStation**.

#### <a name="efrsample-component"></a>EFRSample-komponent

1. Finn prosjektet **HardwareStation.Extension.EFRSample** og bygg den.
2. Finn følgende samlingsfiler i mappen **Extension.EFRSample\\bin\\Debug**:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. Kopier samlingsfilene til utvidelsesmappen for maskinvarestasjon:

    - **Delt maskinvarestasjon:** Kopier filene til **bin**-mappen under stasjonsområdeplasseringen for IIS-maskinvare.
    - **Dedikert maskinvarestasjon som skal opprettes i Modern POS:** Kopier filene til Modern POS-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for maskinvarestasjonens utvidelser. Filen kalles **HardwareConfig.Extension.config**.

    - **Delt maskinvarestasjon:** Filen ligger under stasjonsområdeplasseringen for IIS-maskinvare.
    - **Dedikert maskinvarestasjon som skal opprettes i Modern POS:** Filen ligger under Modern POS-klientmeglingsplasseringen.

5. Legg til følgende linje i **sammensetningsdelen** av konfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

#### <a name="enable-pos-extensions"></a>Aktivere POS-utvidelser

Eksemplet på POS-utvidelse ligger i mappen **src\\FiscalIntegration\\PosFiscalConnectorSample** i repositoriet [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/).

Følg denne fremgangsmåten for å bruke eksemplet på POS-utvidelse i den gamle SDK-en.

1. Kopier mappen **Pos.Extension** til POS-mappen **Extensions** i den gamle SDK-en (for eksempel `C:\RetailSDK\src\POS\Extensions`).
1. Gi kopien av mappen **Pos.Extension** navnet **PosFiscalConnector**.
1. Fjern følgende mapper og filer fra mappen **PosFiscalConnector**:

    - bin
    - DataService
    - devDependencies
    - Biblioteker
    - obj
    - Contoso.PosFiscalConnectorSample.Pos.csproj
    - RetailServerEdmxModel.g.xml
    - tsconfig.json

1. Åpne løsningen **CloudPos.sln** eller **ModernPos.sln**.
1. Ta med mappen **PosFiscalConnector**-mappen i prosjektet **Pos.Extensions**.
1. Åpne filen **extensions.json**, og legg til utvidelsen **PosFiscalConnector**.
1. Bygg SDK-en.

### <a name="production-environment"></a>Produksjonsmiljø

Den forrige fremgangsmåten aktiverer utvidelsene som er komponenter i eksemplet på integrering av regnskapsregistreringstjenesten. I tillegg må du følge disse trinnene for å opprette distribuerbare pakker som inneholder Commerce-komponenter, og for å bruke disse pakkene i et produksjonsmiljø.

1. Gjør følgende endringer i konfigurasjonsfilene for pakker i mappen **RetailSdk\\Assets**.

    - I konfigurasjonsfilene **commerceruntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** legger du til følgende linjer i **sammensetningsdelen**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
        ```

    - I konfigurasjonsfilen **HardwareStation.Extension.config** legger du til følgende linje i **sammensetningsdelen**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        ```

2. Gjør følgende endringer i pakkekonfigurasjonsfilen **Customization.settings** i **BuildTools**-mappen.

    - Legg til følgende linjer for å ta med CRT-utvidelsene i pakkene som kan distribueres.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Legg til følgende linje for å ta med utvidelsen for maskinvarestasjon i pakkene som kan distribueres.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample" />
        ```

3. Start MSBuild Command Prompt for Visual Studio-verktøyet, og kjør **msbuild** under Retail SDK-mappen for å opprette distribuerbare pakker.
4. Ta i bruk pakkene via LCS eller manuelt. Hvis du vil ha mer informasjon, kan du se [Opprette distribuerbare pakker](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Fullfør alle de nødvendige oppsettoppgavene som er beskrevet i [Definer Commerce for Tsjekkia](emea-cze-fi-sample.md#set-up-commerce-for-the-czech-republic).

## <a name="design-of-extensions"></a>Utforming av utvidelser

Eksemplet på integrering av regnskapsregistreringstjenesten for Tsjekkia er basert på [regnskapsintegreringsfunksjonaliteten](fiscal-integration-for-retail-channel.md). Hvis du vil ha mer informasjon om utformingen av regnskapsintegreringsløsningen, kan du se [Oversikt over eksempelutforming av en regnskapsintegrering](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime-utvidelsesutforming

Formålet med filtypen som er en regnskapsdokumentleverandør, er å generere servicespesifikke dokumenter og håndtere svar fra regnskapsregistreringstjenesten.

CRT-utvidelsen er **Runtime.Extensions.DocumentProvider.EFRSample**.

#### <a name="request-handler"></a>Forespørselsbehandler

Det finnes en enkelt **DocumentProviderEFRFiscalCZE**-forespørselsbehandler for dokumentleverandøren. Den brukes til å generere regnskapsdokumenter for regnskapsregistreringstjenesten.

Denne behandleren arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på koblingsdokumentleverandøren som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler:

- **GetFiscalDocumentDocumentProviderRequest** – Denne forespørselen inneholder informasjon om hvilke dokumenter som skal genereres. Det returnerer et servicespesifikk dokument som skal registreres i regnskapsregistreringstjenesten.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Denne forespørselen returnerer listen over hendelser du kan abonnere på. For øyeblikket støttes følgende hendelser: salg, kundekontoinnbetalinger og innbetalinger for kundeordre.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Denne forespørselen returnerer svaret fra regnskapsregistreringstjenesten. Dette svaret serialiseres til å utgjøre en streng, slik at den er klar til å lagres.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen **DocumentProviderFiscalEFRSampleCzech** ligger i **Konfigurasjon**-mappen for utvidelsesprosjektet. Formålet med denne filen er å aktivere innstillinger for dokumentleverandøren som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering. Følgende innstillinger legges til:

- Tilordning av mva-satser
- Standard mva-gruppe
- Mva-gruppe for innbetaling

### <a name="hardware-station-extension-design"></a>Utvidelsesutforming for maskinvarestasjon

Formålet med utvidelsen som er en regnskapskobling, er å kommunisere med regnskapsregistreringstjenesten.

Utvidelsen for maskinvarestasjon kalles **HardwareStation.Extension.EFRSample**. Den bruker HTTP- eller HTTPS-protokollen til å sende dokumenter som CRT-utvidelsen genererer til regnskapsregistreringstjenesten. Den håndterer også svarene som mottas fra regnskapsregistreringstjenesten.

#### <a name="request-handler"></a>Forespørselsbehandler

Forespørselsbehandleren **EFRHandler** er startpunktet for behandling av forespørsler til regnskapsregistreringstjenesten.

Behandleren arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på regnskapskoblingen som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler:

- **SubmitDocumentFiscalDeviceRequest** – Denne forespørselen sender dokumenter til regnskapsregistreringstjenesten og returnerer et svar fra den.
- **IsReadyFiscalDeviceRequest** – Denne forespørselen brukes for en tilstandskontroll av regnskapsregistreringstjenesten.
- **InitializeFiscalDeviceRequest** – Denne forespørselen brukes til å initialisere regnskapsregistreringstjenesten.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen ligger i **Konfigurasjon**-mappen for utvidelsesprosjektet: Formålet med filen er å aktivere innstillinger for regnskapskoblingen som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering. Følgende innstillinger legges til:

- **Endrepunktadresse** – URL-adressen til regnskapsregistreringstjenesten.
- **Tidsavbrudd** – Tiden, i millisekunder, som koblingen vil vente på svar fra regnskapsregistreringstjenesten.

### <a name="pos-fiscal-connector-extension-design"></a>Utforming av regnskapskoblingsutvidelsen for POS

Formålet med regnskapskoblingsutvidelsen for POS, er å kommunisere med regnskapsregistreringstjenesten fra POS. Den bruker HTTPS-protokollen til kommunikasjon.

#### <a name="fiscal-connector-factory"></a>Regnskapskoblingsfabrikk

Regnskapskoblingsfabrikken tilordner koblingsnavnet til implementeringen av regnskapskoblingen og er i filen **Pos.Extension\\Connectors\\FiscalConnectorFactory.ts**. Koblingsnavnet må samsvare med navnet på regnskapskoblingen som er angitt i Commerce Headquarters.

#### <a name="efr-fiscal-connector"></a>Regnskapskobling for EFR

Regnskapskoblingen for EFR er i filen **Pos.Extension\\Connectors\\Efr\\EfrFiscalConnector.ts**. Det implementerer grensesnittet for **IFiscalConnector** som støtter følgende forespørsler:

- **FiscalRegisterSubmitDocumentClientRequest** – Denne forespørselen sender dokumenter til regnskapsregistreringstjenesten og returnerer et svar fra den.
- **FiscalRegisterIsReadyClientRequest** – Denne forespørselen brukes for en tilstandskontroll av regnskapsregistreringstjenesten.
- **FiscalRegisterInitializeClientRequest** – Denne forespørselen brukes til å initialisere regnskapsregistreringstjenesten.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen ligger i mappen **src\\FiscalIntegration\\Efr\\Configurations\\Connectors** i repositoriet [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er å aktivere innstillinger for regnskapskoblingen som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering. Følgende innstillinger legges til:

- **Endrepunktadresse** – URL-adressen til regnskapsregistreringstjenesten.
- **Tidsavbrudd** – Tiden, i millisekunder, som koblingen vil vente på svar fra regnskapsregistreringstjenesten.
