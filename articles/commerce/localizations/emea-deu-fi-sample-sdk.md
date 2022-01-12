---
title: Distribusjonsretningslinjer for eksempel på integrering av regnskapsregistreringstjenesten for Tyskland (eldre)
description: Dette emnet inneholder retningslinjer for distribusjon av eksemplet på regnskapsintegrering for Tyskland fra Microsoft Dynamics 365 Commerce Retail Software Development Kit (SDK).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 51107731090b77e75a0e5a8c91b052d494b452e4
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944921"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-germany-legacy"></a>Distribusjonsretningslinjer for eksempel på integrering av regnskapsregistreringstjenesten for Tyskland (eldre)

[!include [banner](../includes/banner.md)]

Dette emnet inneholder retningslinjer for distribusjon av eksemplet på integrering av regnskapsregistreringstjenesten for Tyskland fra Microsoft Dynamics 365 Commerce Retail Software Development Kit (SDK) på en virtuell utviklermaskin (VM) i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon om dette eksemplet på regnskapsintegrering, kan du se [Eksempler på integrering av regnskapsregistreringstjenesten for Tyskland](emea-deu-fi-sample.md). 

Eksempelet på regnskapsintegrering for Tyskland er en del av Retail SDK. Hvis du vil ha informasjon om hvordan du installerer og bruker SDK, se [Arkitektur for Retail Software Development Kit (SDK)](../dev-itpro/retail-sdk/retail-sdk-overview.md). Dette eksemplet består av utvidelser for Commerce Runtime (CRT) og maskinvarestasjon. Hvis du vil kjøre dette eksemplet, må du endre og bygge prosjektene CRT og maskinvarestasjon. Vi anbefaler at du bruker en uendret Retail SDK til å foreta endringene som er beskrevet i dette emnet. Vi anbefaler også at du bruker et kildekontrollsystem for eksempel Azure DevOps der ingen filer er endret ennå.

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
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
    ```

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

### <a name="production-environment"></a>Produksjonsmiljø

I forrige fremgangsmåte aktiverer utvidelsene som er komponenter i eksemplet på integrering av regnskapsregistreringstjenesten. I tillegg må du følge disse trinnene for å opprette distribuerbare pakker som inneholder Commerce-komponenter, og for å bruke disse pakkene i et produksjonsmiljø.

1. Gjør følgende endringer i konfigurasjonsfilene for pakker i mappen **RetailSdk\\Assets**:

    - I konfigurasjonsfilene **commerceruntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** legger du til følgende linjer i **sammensetningsdelen**.

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

    - I konfigurasjonsfilen **HardwareStation.Extension.config** legger du til følgende linjer i **sammensetningsdelen**.

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

    - Legg til følgende linjer for å ta med utvidelsene for maskinvarestasjon i pakkene som kan distribueres.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Start MSBuild Command Prompt for Visual Studio-verktøyet, og kjør **msbuild** under Retail SDK-mappen for å opprette distribuerbare pakker.
4. Ta i bruk pakkene via LCS eller manuelt. Hvis du vil ha mer informasjon, kan du se [Opprette distribuerbare pakker](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Fullfør alle de nødvendige oppsettoppgavene som er beskrevet i [Definer Commerce for Tyskland](emea-deu-fi-sample.md#set-up-commerce-for-germany).

## <a name="design-of-extensions"></a>Utforming av utvidelser

Eksemplet på integrering av regnskapsregistreringstjenesten for Tyskland er basert på [regnskapsintegreringsfunksjonaliteten](fiscal-integration-for-retail-channel.md). Hvis du vil ha mer informasjon om utformingen av regnskapsintegreringsløsningen, kan du se [Oversikt over eksempelutforming av en regnskapsintegrering](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime-utvidelsesutforming

Formålet med filtypen som er en regnskapsdokumentleverandør, er å generere servicespesifikke dokumenter og håndtere svar fra regnskapsregistreringstjenesten.

CRT-utvidelsen er **Runtime.Extensions.DocumentProvider.EFRSample**. Hvis du vil ha mer informasjon om utformingen for regnskapsintegreringsløsningen, kan du se [Oversikt over regnskapsintegrering for handelskanaler](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

#### <a name="request-handler"></a>Forespørselsbehandler

Det finnes én forespørselsbehandler for dokumentleverandøren, **DocumentProviderEFRFiscalDEU**. Denne behandleren brukes til å generere regnskapsdokumenter for regnskapsregistreringstjenesten. Den arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på koblingsdokumentleverandøren som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler:

- **GetFiscalDocumentDocumentProviderRequest** – Denne forespørselen inneholder informasjon om hvilke dokumenter som skal genereres. Det returnerer et servicespesifikk dokument som skal registreres i regnskapsregistreringstjenesten.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – Denne forespørselen returnerer svaret sammen med utvidede data.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen **DocumentProviderFiscalEFRSampleGermany** ligger i **Konfigurasjon**-mappen for utvidelsesprosjektet. Formålet med denne filen er å aktivere innstillinger for dokumentleverandøren som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering.

Følgende innstillinger legges til:

- **Tilordning av mva-satser** – Tilordningen av mva-prosentverdier som er definert for mva-kodene til verdier av attributtet **TaxG** (mva-gruppe) i forespørsler som sendes til regnskapstjenesten.
- **Mva-gruppe for gavekort og innbetalinger** – Verdien til **TaxG**-attributtet i forespørsler som sendes til regnskapstjenesten, basert på operasjoner som omfatter gavekort eller innbetalinger.
- **Tilordning av betalingsmiddel** – Tilordningen av betalingsmetoder til verdier for attributtet **PayG** (betalingsgruppe) i forespørsler som sendes til regnskapstjenesten.
- **Avgiftsgruppe for mva-fritak** – Verdien til **TaxG**-attributtet i forespørsler som sendes til regnskapstjenesten, basert på operasjoner som er unntatt avgiftsforpliktelser.
- **Inkluder kundedata** – Hvis denne parameteren er aktivert, vil forespørsler til regnskapstjenesten inneholde kundeinformasjon, for eksempel navn og adresser, i tilfeller der en kunde er lagt til i en transaksjon.

### <a name="hardware-station-extension-design"></a>Utvidelsesutforming for maskinvarestasjon

Formålet med utvidelsen som er en regnskapskobling, er å kommunisere med regnskapsregistreringstjenesten.

Utvidelsen for maskinvarestasjon er **HardwareIdent.Extension.EFRSample**. Den bruker HTTP-protokollen til å sende dokumenter som CRT-utvidelsen genererer til regnskapsregistreringstjenesten. Den håndterer også svarene som mottas fra regnskapsregistreringstjenesten.

#### <a name="request-handler"></a>Forespørselsbehandler

Forespørselsbehandleren **EFRHandler** er startpunktet for behandling av forespørsler til regnskapsregistreringstjenesten. Denne behandleren arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på regnskapskoblingen som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler:

- **SubmitDocumentFiscalDeviceRequest** – Denne forespørselen sender dokumenter til regnskapsregistreringstjenesten og returnerer et svar fra den.
- **IsReadyFiscalDeviceRequest** – Denne forespørselen brukes for en tilstandskontroll av regnskapsregistreringstjenesten.
- **InitializeFiscalDeviceRequest** – Denne forespørselen brukes til å initialisere regnskapsregistreringstjenesten.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen ligger i **Konfigurasjon**-mappen for utvidelsesprosjektet: Formålet med filen er å aktivere innstillinger for regnskapskoblingen som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering.

Følgende innstillinger legges til:

- **Endrepunktadresse** – URL-adressen til regnskapsregistreringstjenesten.
- **Tidsavbrudd** – Tiden, i millisekunder (ms), som driveren vil vente på svar fra regnskapsregistreringstjenesten.
- **Vis regnskapsregistreringsmeldinger** – Hvis denne parameteren er aktivert, vises meldinger fra regnskapstjenesten som brukermeldinger i salgsstedet.
