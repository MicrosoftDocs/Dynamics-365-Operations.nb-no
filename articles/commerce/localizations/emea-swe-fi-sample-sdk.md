---
title: Distribusjonsretningslinjer for eksempel på kontrollenhetsintegrering for Sverige (eldre)
description: Denne artikkelen inneholder retningslinjer for distribusjon av eksemplet på kontrollenhetsintegrering for Sverige fra Retail SDK
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 05a49de43282c449c7b99072d8ac3ac4a5f2a67f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870553"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>Distribusjonsretningslinjer for eksempel på kontrollenhetsintegrering for Sverige (eldre)

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder retningslinjer for distribusjon av eksemplet på kontrollenhetsintegrering for Sverige fra SDK (Retail Software Development Kit) på en virtuell utviklermaskin (VM) i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon om dette eksemplet på regnskapsintegrering, kan du se [Eksempler på kontrollenhetsintegrering for Sverige](emea-swe-fi-sample.md). 

Eksempelet på regnskapsintegrering for Sverige er en del av Retail SDK. Hvis du vil ha informasjon om hvordan du installerer og bruker SDK, se [Arkitektur for Retail Software Development Kit (SDK)](../dev-itpro/retail-sdk/retail-sdk-overview.md). Dette eksemplet består av utvidelser for Commerce Runtime (CRT), maskinvarestasjon og salgssted. Hvis du vil kjøre dette eksemplet, må du endre og bygge CRT, maskinvarestasjon og salgsstedsprosjektene. Vi anbefaler at du bruker en uendret Retail SDK til å foreta endringene som er beskrevet i denne artikkelen. Vi anbefaler også at du bruker et kildekontrollsystem for eksempel Azure DevOps der ingen filer er endret ennå.

## <a name="development-environment"></a>Utviklingsmiljø

Følg denne fremgangsmåten for å definere et distribusjonsmiljø slik at du kan teste og utvide eksemplet.

### <a name="enable-crt-extensions"></a>Aktiver CRT-utvidelser

CRT-utvidelseskomponentene er inkludert i CRT-eksemplene. Du kan fullføre følgende fremgangsmåter ved å åpne løsningen **CommerceRuntimeSamples.sln** under **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="documentprovidercleancashsample-component"></a>DocumentProvider.CleanCashSample-komponent

1. Finn prosjektet **Runtime.Extensions.DocumentProvider.CleanCashSample**, og bygg det.
2. I mappen **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Commerce Scale Unit:** Kopier filen til **\\bin\\ext**-mappen under områdplasseringen Internet Information Services (IIS) Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Kopier filen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Commerce Scale Unit:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Commerce Scale Unit-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    ```

#### <a name="extension-configuration-file"></a>Konfigurasjonsfil for utvidelse

1. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Commerce Scale Unit:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Commerce Scale Unit-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

2. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

### <a name="enable-hardware-station-extensions"></a>Aktiver utvidelser for maskinvarestasjon

Utvidelseskomponentene for maskinvarestasjonen inkluderes i eksemplene for maskinvarestasjon. Du kan fullføre følgende fremgangsmåter ved å åpne løsningen **HardwareStationSamples.sln** under **RetailSdk\\SampleExtensions\\HardwareStation**.

#### <a name="cleancash-component"></a>CleanCash-komponent

1. Finn prosjektet **HardwareStation.Extension.CleanCashSample** og bygg den.
2. I mappen **Extension.CleanCashSample\\bin\\Debug** finner du samlingsfilene **Contoso.Commerce.HardwareStation.CleanCashSample.dll** og **Interop.CleanCash\_1\_1.dll**.
3. Kopier samlingsfilene til utvidelsesmappen for maskinvarestasjon:

    - **Delt maskinvarestasjon:** Kopier filene til **bin**-mappen under stasjonsområdeplasseringen for IIS-maskinvare.
    - **Dedikert maskinvarestasjon som skal opprettes i Modern POS:** Kopier filene til Modern POS-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for maskinvarestasjonens utvidelser. Filen kalles **HardwareConfig.Extension.config**.

    - **Delt maskinvarestasjon:** Filen ligger under stasjonsområdeplasseringen for IIS-maskinvare.
    - **Dedikert maskinvarestasjon som skal opprettes i Modern POS:** Filen ligger under Modern POS-klientmeglingsplasseringen.

5. Legg til følgende linje i **sammensetningsdelen** av konfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

### <a name="enable-modern-pos-extension-components"></a>Aktiver Modern POS-utvidelseskomponenter

1. Åpne løsningen **ModernPOS.sln** under **RetailSdk\\POS**, og kontroller at den kan kompileres uten feil. I tillegg må du passe på at du kan kjøre Modern POS fra Visual Studio ved hjelp av kommandoen **Kjør**.

    > [!NOTE]
    > Modern POS må ikke tilpasses. Du må aktivere Brukerkontokontroll (UAC), og du må avinstallere tidligere installerte forekomster av Modern POS etter behov.

2. Aktiver utvidelsene som må lastes inn, ved å legge til følgende linjer i **extensions.json**-filen.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
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
2. Aktiver utvidelsene som må lastes inn, ved å legge til følgende linjer i **extensions.json**-filen.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > Hvis du vil ha mer informasjon og eksempler som viser hvordan du inkluderer kildekodemapper og aktiverer tillegg som skal lastes, kan du se instruksjonene i filen readme.md i **Pos.Extensions**-prosjektet.

3. Bygg løsningen på nytt.
4. Kjør løsningen ved å bruke kommandoen **Kjør**, og følg trinnene i Retail SDK-håndboken.

## <a name="production-environment"></a>Produksjonsmiljø

Den forrige fremgangsmåten aktiverer utvidelsene som er komponenter i eksemplet på kontrollenhetsintegrering. I tillegg må du følge disse trinnene for å opprette distribuerbare pakker som inneholder Commerce-komponenter, og for å bruke disse pakkene i et produksjonsmiljø.

1. Gjør følgende endringer i konfigurasjonsfilene for pakker i mappen **RetailSdk\\Assets**:

    - I konfigurasjonsfilene **commerceruntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** legger du til følgende linjer i **sammensetningsdelen**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - I konfigurasjonsfilen **HardwareStation.Extension.config** legger du til følgende linje i **sammensetningsdelen**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. Gjør følgende endringer i pakkekonfigurasjonsfilen **Customization.settings** i **BuildTools**-mappen:

    - Legg til følgende linje for å ta med CRT-utvidelsene i pakkene som kan distribueres.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - Legg til følgende linjer for å ta med utvidelsen for maskinvarestasjon i pakkene som kan distribueres.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. Aktiver POS-utvidelsen ved å legge til følgende linjer i filen **extensions.json** under mappen **RetailSDK\\POS\\Extensions**.

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. Start MSBuild Command Prompt for Visual Studio-verktøyet, og kjør **msbuild** under Retail SDK-mappen for å opprette distribuerbare pakker.
5. Ta i bruk pakkene via LCS eller manuelt. Hvis du vil ha mer informasjon, kan du se [Opprette distribuerbare pakker](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
6. Fullfør alle de nødvendige oppsettoppgavene som beskrives under [Definer integreringen med kontrollenheter](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).

## <a name="design-of-the-extensions"></a>Utforming av utvidelsene

### <a name="crt-extension-design"></a>CRT-utvidelsesutforming

Formålet med filtypen som er en regnskapsdokumentleverandør, er å generere servicespesifikke dokumenter og håndtere svar fra kontrollenheten.

CRT-utvidelsen er **Runtime.Extensions.DocumentProvider.CleanCashSample**.

Hvis du vil ha mer informasjon om utformingen av regnskapsintegreringsløsningen, kan du se [Bilagsregistreringsprosess og regnskapsintegreringeseksempler for regnskapsenheter og -tjenester](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Forespørselsbehandler

Det finnes en enkelt **DocumentProviderCleanCash**-forespørselsbehandler for dokumentleverandøren. Denne behandleren brukes til å generere regnskapsdokumenter for kontrollenheten.

Denne behandleren arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på koblingsdokumentleverandøren som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler:

- **GetFiscalDocumentDocumentProviderRequest** – Denne forespørselen inneholder informasjon om hvilke dokumenter som skal genereres. Det returnerer et servicespesifikk dokument som skal registreres i kontrollenheten.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Denne forespørselen returnerer listen over hendelser du kan abonnere på. Salgshendelser og revisjonshendelser støttes for øyeblikket.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen **DocumentProviderFiscalCleanCashSample** ligger i **Konfigurasjon**-mappen for utvidelsesprosjektet. Formålet med denne filen er å aktivere innstillinger for dokumentleverandøren som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering. Følgende innstillinger legges til:

- Tilordning av mva-koder

### <a name="hardware-station-extension-design"></a>Utvidelsesutforming for maskinvarestasjon

Formålet med utvidelsen som er en regnskapskobling, er å kommunisere med kontrollenheten.

Utvidelsen for maskinvarestasjon er **HardwareIdent.Extension.CleanCashSample**. Den bruker HTTP-protokollen til å sende dokumenter som CRT-utvidelsen genererer til kontrollenheten. Den håndterer også svarene som mottas fra kontrollenheten.

#### <a name="request-handler"></a>Forespørselsbehandler

Forespørselsbehandleren **CleanCashHandler** er startpunktet for behandling av forespørsler til kontrollenheten.

Behandleren arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på regnskapskoblingen som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler:

- **SubmitDocumentFiscalDeviceRequest** – Denne forespørselen sender dokumenter til kontrollenheten og returnerer et svar fra den.
- **IsReadyFiscalDeviceRequest** – Denne forespørselen brukes for en tilstandskontroll av kontrollenheten.
- **InitializeFiscalDeviceRequest** – Denne forespørselen brukes til å initialisere kontrollenheten.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen ligger i **Konfigurasjon**-mappen for utvidelsesprosjektet. Formålet med filen er å aktivere innstillinger for regnskapskoblingen som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering. Følgende innstillinger legges til:

- **Tilkoblingsstreng** – Tilkoblingsinnstillingene for kontrollenheten.
- **Tidsavbrudd** – Tiden, i millisekunder, som driveren vil vente på svar fra kontrollenheten.

## <a name="migrating-from-the-earlier-integration-sample"></a>Overføring fra eksempelet for tidligere integrering

Hvis du bruker det tidligere [eksemplet for POS-integrering med kontrollenheter for Sverige](retail-sdk-control-unit-sample.md), kan det hende at du må overføre fra den til gjeldende integreringseksempel. For å ta imot endringen og motta regelmessige oppdateringer for funksjonene for Sverige i fremtiden kan det hende at du må oppgradere, gjøre små kode- og konfigurasjonsjusteringer i utvidelsene du har bygd, og bygge opp løsningene på nytt. Ingen store endringer kreves i utvidelseslogikken som du opprettet. Eksemplet på tidligere integrering og tilpasningene vil fortsette å fungere hvis det ikke er gjort endringer fra din side. Derfor kan du planlegge, forberede deg på og gjøre oppgraderingen for miljøet.

### <a name="migration-process"></a>Migreringsprosess

Overføringen fra det tidligere integreringseksemplet til det gjeldende eksemplet på kontrollenhetsintegrasjon bør baseres på konseptet med en gradvis oppdatering. Alle Commerce Headquarters- og Commerce Scale Unit-komponenter bør med andre ord allerede være oppdatert før du starter å oppdatere salgssted- og maskinvarestasjonskomponentene.

Hvis du vil ha hjelp til å forhindre situasjoner der en hendelse eller transaksjon signeres to ganger (det vil si at den er signert av både den tidligere utvidelsen og den gjeldende utvidelsen), eller der en hendelse eller transaksjon ikke kan signeres på grunn av den manglende konfigurasjonen, anbefaler vi at du deaktiverer alle salgssteds- og maskinvarestasjonsenheter som bruker den tidligere eksemplet, og oppdaterer dem deretter samtidig. Denne samtidige oppdateringen kan for eksempel utføres butikk for butikk ved å oppdatere butikkens funksjonalitetsprofil og maskinvarestasjonens maskinvareprofil.

Migreringsprosessen skal bestå av følgende trinn.

1. Oppdater Commerce Headquarters-komponentene.
1. Oppdater Commerce Scale Unit-komponentene, og aktiver utvidelsene for gjeldende eksempel.
1. Kontroller at alle frakoblede transaksjoner synkroniseres fra frakoblede MPOS-enheter.
1. Slå av alle enheter som bruker komponentene i den tidligere eksemplet.
1. Fullfør alle de nødvendige oppsettoppgavene som beskrives under [Definer integreringen med kontrollenheter](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).
1. Oppdater salgssteds- og maskinvarestasjonskomponentene, deaktiver utvidelsene som er deler av det tidligere eksemplet, og aktiver utvidelsene for gjeldende eksempel.

    > [!NOTE]
    > Avhengig av typen miljø kan du finne flere tekniske detaljer om migreringsprosessen i enten delen [Migrering i et utviklingsmiljø](#migration-in-a-development-environment) eller [Migrering i en produksjonsmiljø](#migration-in-a-production-environment) i denne artikkelen.

### <a name="migration-in-a-development-environment"></a>Migrering i et utviklingsmiljø

#### <a name="update-crt"></a>Oppdater CRT

1. Finn prosjektet **Runtime.Extensions.DocumentProvider.CleanCashSample**, og bygg det.
2. I mappen **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Commerce Scale Unit:** Kopier filen til **\\bin\\ext**-mappen under områdplasseringen IIS Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Kopier filen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Commerce Scale Unit:** Filen heter **CommerceRuntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Commerce Scale Unit-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger i **bin\\ext**-mappen under den lokale CRT-klientmeglerplasseringen.

    > [!WARNING]
    > **Ikke** rediger filene CommerceRuntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

5. Finn og fjern den tidligere CRT-utvidelsen fra konfigurasjonsfilen for utvidelse.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Ikke fullfør dette trinnet før du oppdaterer alle salgsstedsenheter som fungerer med denne CRT-forekomsten.

6. Registrer de gjeldende CRT-eksempelutvidelsene i konfigurasjonsfilen for utvidelsen ved å legge til følgende linjer.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>Oppdater maskinvarestasjon

1. Finn prosjektet **HardwareStation.Extension.CleanCashSample** og bygg den.
2. I mappen **Extension.CleanCashSample\\bin\\Debug** finner du samlingsfilene **Contoso.Commerce.HardwareStation.CleanCashSample.dll** og **Interop.CleanCash\_1\_1.dll**.
3. Kopier samlingsfilene til utvidelsesmappen for maskinvarestasjon:

    - **Delt maskinvarestasjon:** Kopier filene til **bin**-mappen under stasjonsområdeplasseringen for IIS-maskinvare.
    - **Dedikert maskinvarestasjon som skal opprettes i Modern POS:** Kopier filene til Modern POS-klientmeglingsplasseringen.

4. Finn konfigurasjonsfilen **HardwareConfig.Extension.config**:

    - **Ekstern maskinvarestasjon:** Filen ligger under stasjonsområdeplasseringen for IIS-maskinvare.
    - **Lokal maskinvarestasjon på Modern POS:** Filen ligger under Modern POS-klientmeglingsplasseringen.

    > [!WARNING]
    > **Ikke** rediger filene CommerceRuntime.config og CommerceRuntime.MPOSOffline.config. Disse filene er ikke beregnet på tilpasninger.

5. Finn og fjern den tidligere maskinvarestasjonsutvidelsen fra konfigurasjonsfilen for utvidelse.

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 og tidligere](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 og senere](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 og senere](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. Legg til følgende linje i **sammensetningsdelen** av konfigurasjonsfilen for utvidelse.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>Oppdater Modern POS

1. Åpne **CloudPOS.sln**-løsningen under **RetailSdk\\POS**.
2. Deaktiver den tidligere salgsstedsutvidelsen ved å fjerne følgende linjer fra filen **extensions.json**.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Aktiver gjeldende utvidelse for eksempelsalgssted ved å legge til følgende linjer i **extensions.json**-filen.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Oppdater skybasert salgssted

1. Åpne **ModernPOS.sln**-løsningen under **RetailSdk\\POS**.
2. Deaktiver den tidligere salgsstedsutvidelsen ved å fjerne følgende linjer fra filen **extensions.json**.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Aktiver gjeldende utvidelse for eksempelsalgssted ved å legge til følgende linjer i **extensions.json**-filen.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

### <a name="migration-in-a-production-environment"></a>Migrering i et produksjonsmiljø

#### <a name="update-crt"></a>Oppdater CRT

1. Fjern den tidligere CRT-utvidelsen fra konfigurasjonsfilene **CommerceRuntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** under mappen **RetailSdk\\Assets**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Ikke fullfør dette trinnet før du oppdaterer alle salgsstedsenheter som fungerer med denne CRT-forekomsten.

2. Aktiver gjeldende CRT-eksempelutvidelser ved å gjøre følgende endringer i konfigurasjonsfilene **CommerceRuntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** under mappen **RetailSdk\\Assets**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. I konfigurasjonsfilen for pakketilpasning for **Customization.settings** under **BuildTools**-mappen legger du til følgende linje for å inkludere gjeldende CRT-eksempelutvidelse i distribuerbare pakker.

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>Oppdater maskinvarestasjon

1. Fjern den tidligere maskinvarestasjonsutvidelsen ved å endre konfigurasjonsfilen **HardwareStation.Extension.config**.

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 og tidligere](#tab/retail-7-3)

    Fjern følgende del fra konfigurasjonsfilene **HardwareConfig.Shared.config** og **HardwareConfig.Dedicated.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 og senere](#tab/retail-7-3-1)

    Fjern følgende del fra konfigurasjonsfilen **HardwareConfig.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 og senere](#tab/retail-10-0)

    Fjern følgende del fra konfigurasjonsfilen **HardwareConfig.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

2. Aktiver det gjeldende eksempelet for maskinvarestasjonsutvidelse ved å legge til følgende linje i **sammensetningsdelen** i konfigurasjonsfilen **HardwareConfig.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

3. Gjør følgende endringer i pakkekonfigurasjonsfilen **Customization.settings** i **BuildTools**-mappen:

    - Fjern følgende linje for å ekskludere den tidligere utvidelsen for maskinvarestasjon fra pakkene som kan distribueres.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />
        ```

    - Legg til følgende linjer for å ta med det gjeldende eksemplet for utvidelsen for maskinvarestasjon i pakkene som kan distribueres.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

#### <a name="update-modern-pos"></a>Oppdater Modern POS

1. Åpne **CloudPOS.sln**-løsningen under **RetailSdk\\POS**.
2. Deaktiver den tidligere salgsstedsutvidelsen:

    - Legg til **FiscalRegisterSample**-mappen i ekskluderingslisten i **tsconfig.json**-filen.
    - Fjern følgende linjer fra **extensions.json** under mappen **RetailSDK\\POS\\Extensions**.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Aktiver gjeldende salgstedseksempelutvidelse ved å legge til følgende linjer i filen **extensions.json** under mappen **RetailSDK\\POS\\Extensions**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Oppdater skybasert salgssted

1. Åpne **ModernPOS.sln**-løsningen under **RetailSdk\\POS**.
2. Deaktiver den tidligere salgsstedsutvidelsen:

    - Legg til **FiscalRegisterSample**-mappen i ekskluderingslisten i **tsconfig.json**-filen.
    - Fjern følgende linjer fra **extensions.json** under mappen **RetailSDK\\POS\\Extensions**.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Aktiver gjeldende salgstedseksempelutvidelse ved å legge til følgende linjer i filen **extensions.json** under mappen **RetailSDK\\POS\\Extensions**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="create-deployable-packages"></a>Opprette distribuerbare pakker

Kjør **msbuild** for hele Retail SDK for å opprette distribuerbare pakker. Ta i bruk pakkene via LCS eller manuelt. Hvis du vil ha mer informasjon, kan du se [Retail SDK-pakking](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
