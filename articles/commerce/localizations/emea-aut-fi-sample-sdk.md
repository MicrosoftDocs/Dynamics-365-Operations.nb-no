---
title: Distribusjonsretningslinjer for eksempel på integrering av regnskapsregistreringstjenesten for Østerrike (eldre)
description: Dette emnet inneholder retningslinjer for distribusjon av eksemplet på regnskapsintegrering for Østerrike fra Microsoft Dynamics 365 Commerce Retail Software Development Kit (SDK).
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 65e2a64ed288fb0dcc05ec1ff2db8ed298ed3a76
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388421"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-austria-legacy"></a>Distribusjonsretningslinjer for eksempel på integrering av regnskapsregistreringstjenesten for Østerrike (eldre)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dette emnet inneholder retningslinjer for distribusjon av eksemplet på integrering av regnskapsregistreringstjenesten for Østerrike fra Microsoft Dynamics 365 Commerce Retail Software Development Kit (SDK) på en virtuell utviklermaskin (VM) i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon om dette eksemplet på regnskapsintegrering, kan du se [Eksempler på integrering av regnskapsregistreringstjenesten for Østerrike](emea-aut-fi-sample.md). 

Eksempelet på regnskapsintegrering for Østerrike er en del av Retail SDK. Hvis du vil ha informasjon om hvordan du installerer og bruker SDK, se [Arkitektur for Retail Software Development Kit (SDK)](../dev-itpro/retail-sdk/retail-sdk-overview.md). Dette eksempelet på regnskapsintegrering består av utvidelser for Commerce Runtime (CRT), maskinvarestasjon og salgssted. Hvis du vil kjøre dette eksemplet, må du endre og bygge CRT, maskinvarestasjon og salgsstedsprosjektene. Vi anbefaler at du bruker en uendret Retail SDK til å foreta endringene som er beskrevet i dette emnet. Vi anbefaler også at du bruker et kildekontrollsystem for eksempel Azure DevOps der ingen filer er endret ennå.

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
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>Aktivere utvidelser for regnskapskobling

Du kan aktivere utvidelser for regnskapskobling på [maskinvarestasjonen](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) eller i [POS-kassen](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

#### <a name="enable-hardware-station-extensions"></a>Aktiver utvidelser for maskinvarestasjon

Utvidelseskomponentene for maskinvarestasjonen inkluderes i eksemplene for maskinvarestasjon. Du kan fullføre følgende fremgangsmåter ved å åpne løsningen **HardwareStationSamples.sln** under **RetailSdk\\SampleExtensions\\HardwareStation**.

##### <a name="efrsample-component"></a>EFRSample-komponent

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

### <a name="enable-modern-pos-extension-components"></a>Aktiver Modern POS-utvidelseskomponenter

1. Åpne løsningen **ModernPOS.sln** under **RetailSdk\\POS**, og kontroller at den kan kompileres uten feil. I tillegg må du passe på at du kan kjøre Modern POS fra Visual Studio ved hjelp av kommandoen **Kjør**.

    > [!NOTE]
    > Modern POS må ikke tilpasses. Du må aktivere Brukerkontokontroll (UAC), og du må avinstallere tidligere installerte forekomster av Modern POS etter behov.

2. Aktiver utvidelsene som skal lastes inn, ved å legge til følgende linjer i **extensions.json**-filen.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Hvis du vil ha mer informasjon og eksempler som viser hvordan du inkluderer kildekodemapper og aktiverer tillegg som skal lastes, kan du se instruksjonene i filen readme.md i **Pos.Extensions**-prosjektet.

3. Bygg løsningen på nytt.
4. Kjør Modern POS i feilsøkingen, og test funksjonaliteten.

### <a name="enable-cloud-pos-extension-components"></a>Aktiver Cloud POS-utvidelseskomponenter

1. Åpne løsningen **CloudPOS.sln** under **RetailSdk\\POS**, og kontroller at den kan kompileres uten feil.
2. Aktiver utvidelsene som skal lastes inn, ved å legge til følgende linjer i **extensions.json**-filen.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Hvis du vil ha mer informasjon og eksempler som viser hvordan du inkluderer kildekodemapper og aktiverer tillegg som skal lastes, kan du se instruksjonene i filen readme.md i **Pos.Extensions**-prosjektet.

3. Bygg løsningen på nytt.
4. Kjør løsningen ved å bruke kommandoen **Kjør**, og følg trinnene i Retail SDK-håndboken.

## <a name="production-environment"></a>Produksjonsmiljø

Den forrige fremgangsmåten aktiverer utvidelsene som er komponenter i eksemplet på integrering av regnskapsregistreringstjenesten. I tillegg må du følge disse trinnene for å opprette distribuerbare pakker som inneholder Commerce-komponenter, og for å bruke disse pakkene i et produksjonsmiljø.

1. Gjør følgende endringer i konfigurasjonsfilene for pakker i mappen **RetailSdk\\Assets**:

    - I konfigurasjonsfilene **commerceruntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** legger du til følgende linjer i **sammensetningsdelen**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
        ```

    - I konfigurasjonsfilen **HardwareStation.Extension.config** legger du til følgende linje i **sammensetningsdelen**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. Gjør følgende endringer i pakkekonfigurasjonsfilen **Customization.settings** i **BuildTools**-mappen:

    - Legg til følgende linjer for å ta med CRT-utvidelsene i pakkene som kan distribueres.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Legg til følgende linje for å ta med utvidelsen for maskinvarestasjon i pakkene som kan distribueres.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Start MSBuild Command Prompt for Visual Studio-verktøyet, og kjør **msbuild** under Retail SDK-mappen for å opprette distribuerbare pakker.
4. Ta i bruk pakkene via LCS eller manuelt. Hvis du vil ha mer informasjon, kan du se [Opprette distribuerbare pakker](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Fullfør alle de nødvendige oppsettoppgavene som er beskrevet i [Definer Commerce for Østerrike](emea-aut-fi-sample.md#set-up-commerce-for-austria).

## <a name="design-of-extensions"></a>Utforming av utvidelser

Eksemplet på integrering av regnskapsregistreringstjenesten for Østerrike er basert på [regnskapsintegreringsfunksjonaliteten](fiscal-integration-for-retail-channel.md). Hvis du vil ha mer informasjon om utformingen av regnskapsintegreringsløsningen, kan du se [Oversikt over eksempelutforming av en regnskapsintegrering](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime-utvidelsesutforming

Formålet med filtypen som er en regnskapsdokumentleverandør, er å generere servicespesifikke dokumenter og håndtere svar fra regnskapsregistreringstjenesten.

CRT-utvidelsen er **Runtime.Extensions.DocumentProvider.EFRSample**.

#### <a name="request-handler"></a>Forespørselsbehandler

Det finnes to forespørselsbehandlere for dokumentleverandører:

- **DocumentProviderEFRFiscalAUT** – Denne behandleren brukes til å generere regnskapsdokumenter for regnskapsregistreringstjenesten.
- **DocumentProviderEFRNonFiscalAUT** – Denne behandleren brukes til å generere ikke-regnskapsdokumenter for regnskapsregistreringstjenesten.

Disse behandlerne arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på koblingsdokumentleverandøren som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler:

- **GetFiscalDocumentDocumentProviderRequest** – Denne forespørselen inneholder informasjon om hvilke dokumenter som skal genereres. Det returnerer et servicespesifikk dokument som skal registreres i regnskapsregistreringstjenesten.
- **GetNonFiscalDocumentDocumentProviderRequest** – Denne forespørselen inneholder informasjon om hvilke ikke-regnskapsdokumenter som skal genereres. Det returnerer et servicespesifikk dokument som skal registreres i regnskapsregistreringstjenesten.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Denne forespørselen returnerer listen over hendelser du kan abonnere på. For øyeblikket støttes følgende hendelser: salg, utskrift av X-rapport, utskrift av Z-rapport, innbetalinger på kundekonto, innbetalinger på kundeordre, revisjonshendelser og ikke-salgstransaksjoner.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Denne forespørselen returnerer svaret fra regnskapsregistreringstjenesten. Dette svaret serialiseres til å utgjøre en streng, slik at den er klar til å lagres.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilene ligger i **Konfigurasjon**-mappen for utvidelsesprosjektet:

- **DocumentProviderFiscalEFRSampleAustria** – for regnskapsdokumenter.
- **DocumentProviderNonFiscalEFRSampleAustria** – for ikke-regnskapsdokumenter.

Formålet med disse filene er å aktivere innstillinger for dokumentleverandøren som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering. Følgende innstilling legges til:

- Tilordning av mva-satser

### <a name="hardware-station-extension-design"></a>Utvidelsesutforming for maskinvarestasjon

Formålet med regnskapskoblingsutvidelsen er å kommunisere med regnskapsregistreringstjenesten. Utvidelsen for maskinvarestasjon kalles **HardwareStation.Extension.EFRSample**. Den bruker HTTP- eller HTTPS-protokollen til å sende dokumenter som CRT-utvidelsen genererer til regnskapsregistreringstjenesten. Den håndterer også svarene som mottas fra regnskapsregistreringstjenesten.

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
- **Tidsavbrudd** – Tiden, i millisekunder, som driveren vil vente på svar fra regnskapsregistreringstjenesten.

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
