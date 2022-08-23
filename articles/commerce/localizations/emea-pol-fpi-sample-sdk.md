---
title: Distribusjonsretningslinjer for eksempel på bilagsskriverintegrering for Sverige (eldre)
description: Denne artikkelen inneholder retningslinjer for distribusjon av eksemplet på integrering av bilagsskriver for Polen fra Microsoft Dynamics 365 Commerce Retail Software Development Kit (SDK).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 883f09f73e3b372d6896b6702e54e2e664cff4d7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286533"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>Distribusjonsretningslinjer for eksempel på bilagsskriverintegrering for Sverige (eldre)

[!include[banner](../includes/banner.md)]

Denne artikkelen inneholder retningslinjer for distribusjon av eksemplet på bilagsskriverintegrering for Polen Microsoft Dynamics 365 Commerce Retail Software Development Kit (SDK) på en virtuell utviklermaskin (VM) i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon om dette eksemplet på regnskapsintegrering, kan du se [Eksempler på bilagsskriverintegrering for Polen](emea-pol-fpi-sample.md). 

Eksempelet på regnskapsintegrering for Polen er en del av Retail SDK. Hvis du vil ha informasjon om hvordan du installerer og bruker SDK, se [Arkitektur for Retail Software Development Kit (SDK)](../dev-itpro/retail-sdk/retail-sdk-overview.md). Dette eksemplet består av utvidelser for Commerce Runtime (CRT) og maskinvarestasjon. Hvis du vil kjøre dette eksemplet, må du endre og bygge prosjektene CRT og maskinvarestasjon. Vi anbefaler at du bruker en uendret Retail SDK til å foreta endringene som er beskrevet i denne artikkelen. Vi anbefaler også at du bruker et kildekontrollsystem for eksempel Azure DevOps der ingen filer er endret ennå.

## <a name="development-environment"></a>Utviklingsmiljø

Følg denne fremgangsmåten for å definere et distribusjonsmiljø slik at du kan teste og utvide eksemplet.

### <a name="commerce-runtime-extension-components"></a>Commerce Runtime-utvidelseskomponenter

CRT-utvidelseskomponentene er inkludert i Retail SDK. Du kan fullføre følgende fremgangsmåter ved å åpne løsningen **CommerceRuntimeSamples.sln** under **RetailSdk\\SampleExtensions\\CommerceRuntime**.

1. Finn prosjektet **Runtime.Extensions.DocumentProvider.PosnetSample**, og bygg det.
2. I mappen **Extensions.DocumentProvider.PosnetSample\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll**.
3. Kopier samlingsfilen til CRT-utvidelsesmappen:

    - **Commerce Scale Unit:** Kopier filen til **\\bin\\ext**-mappen under områdplasseringen Internet Information Services (IIS) Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Kopier filen til **\\ext**-mappen under den lokale CRT-klientmeglingsplasseringen.

4. Finn utvidelseskonfigurasjonsfilen for CRT:

    - **Commerce Scale Unit:** Filen heter **commerceruntime.ext.config**, og ligger i **bin\\ext**-mappen under plasseringen av IIS Commerce Scale Unit-området.
    - **Lokal CRT i Modern POS:** Filen heter **CommerceRuntime.MPOSOffline.Ext.config** og ligger under den lokale CRT-klientmeglerplasseringen.

5. Registrer CRT-endringen i utvidelseskonfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. Start Commerce-tjenesten på nytt:

    - **Commerce Scale Unit:** Start Commerce-tjenesteområdet på nytt fra IIS Manager.
    - **Klientmegler:** Avslutt prosessen **dllhost.exe** i Oppgavebehandling, og start deretter Modern POS på nytt.

### <a name="hardware-station-extension-components"></a>Utvidelseskomponenter for maskinvarestasjon

Utvidelseskomponentene for maskinvarestasjon er inkludert i Retail SDK. Du kan fullføre følgende fremgangsmåter ved å åpne løsningen **HardwareStationSamples.sln** under **RetailSdk\\SampleExtensions\\HardwareStation**.

1. Finn prosjektet **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample** og bygg det.
2. I mappen **Extension.Posnet.ThermalFVFiscalPrinterSample\\bin\\Debug** finner du samlingsfilen **Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll**.
3. Kopier samlingsfilen til en distribuert maskinvarestasjonsmaskin:

    - **Ekstern maskinvarestasjon:** Kopier filen til **bin**-mappen under stasjonsområdeplasseringen for IIS-maskinvare. Kopier skriverdriverbibliotekene (**libposcmbth.dll**, **libcmbth\_serial.dll** og **cmbth\_pl.lng**).

4. Finn konfigurasjonsfilen for maskinvarestasjonens utvidelser. Filen kalles **HardwareConfig.Extension.config**:

    - **Ekstern maskinvarestasjon:** Filen ligger under stasjonsområdeplasseringen for IIS-maskinvare.

5. Legg til følgende linje i **sammensetningsdelen** av konfigurasjonsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. Start tjenesten maskinvarestasjon på nytt:

    - **Ekstern maskinvarestasjon:** Start maskinvarstasjonen på nytt fra IIS Manager.

## <a name="production-environment"></a>Produksjonsmiljø

I forrige fremgangsmåte aktiverer utvidelsene som er komponenter i eksemplet på integrering av regnskapsregistreringstjenesten. I tillegg må du følge disse trinnene for å opprette distribuerbare pakker som inneholder Commerce-komponenter, og for å bruke disse pakkene i et produksjonsmiljø.

1. Gjør følgende endringer i konfigurasjonsfilene for pakker i mappen **RetailSdk\\Assets**:

    - I konfigurasjonsfilene **commerceruntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** legger du til følgende linje i **sammensetningsdelen**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - I konfigurasjonsfilen **HardwareStation.Extension.config** legger du til følgende linje i **sammensetningsdelen**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. Gjør følgende endringer i pakkekonfigurasjonsfilen **Customization.settings** i **BuildTools**-mappen:

    - Legg til følgende linje for å ta med CRT-utvidelsen i pakkene som kan distribueres.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - Legg til følgende linje for å ta med utvidelsen for maskinvarestasjon i pakkene som kan distribueres.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. Start MSBuild Command Prompt for Visual Studio-verktøyet, og kjør **msbuild** under Retail SDK-mappen for å opprette distribuerbare pakker.
1. Ta i bruk pakkene via LCS eller manuelt. Hvis du vil ha mer informasjon, kan du se [Opprette distribuerbare pakker](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Utforming av utvidelser

Eksemplet på integrering av bilagsskriver for Polen er basert på [regnskapsintegreringsfunksjonaliteten](fiscal-integration-for-retail-channel.md). Hvis du vil ha mer informasjon om utformingen av regnskapsintegreringsløsningen, kan du se [Oversikt over eksempelutforming av en regnskapsintegrering](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime-utvidelsesutforming

Formålet med filtypen som er en regnskapsdokumentleverandør, er å generere skriverpesifikke dokumenter og håndtere svar fra bilagsskriveren.

CRT-utvidelsen er **Runtime.Extensions.DocumentProvider.PosnetSample**. Denne utvidelsen genererer et sett med skriverspesifikke kommandoer i JSON-formatet (JavaScript Object Notation) som er definert av POSNET-spesifikasjon 19-3678.

Hvis du vil ha mer informasjon om utformingen av regnskapsintegreringsløsningen, kan du se [Bilagsregistreringsprosess og regnskapsintegreringeseksempler for regnskapsenheter og -tjenester](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Forespørselsbehandler

Forespørselsbehandleren **DocumentProviderPosnetProtocol** er startpunktet for forespørselen om å generere dokumenter fra bilagsskriveren.

Behandleren arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på koblingsdokumentleverandøren som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler:

- **GetFiscalDocumentDocumentProviderRequest** – Denne forespørselen inneholder informasjon om hvilke dokumenter som skal genereres. Det returnerer et skriverspesifikk dokument som skal registreres i bilagsskriveren.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Denne forespørselen returnerer listen over hendelser du kan abonnere på. For øyeblikket støttes følgende hendelser: salg, utskrift av X-rapport og utskrift av Z-rapport.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen ligger i **Konfigurasjon**-mappen for utvidelsesprosjektet. Formålet med filen er å aktivere innstillinger for dokumentleverandøren som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering. Følgende innstillinger legges til:

- Tilordning av mva-satser
- Tilordning av betalingsmiddeltype
- Bankinnbetalingstype

### <a name="hardware-station-extension-design"></a>Utvidelsesutforming for maskinvarestasjon

Formålet med utvidelsen som er en regnskapskobling, er å kommunisere med bilagsskriveren.

Utvidelsen for maskinvarestasjon er **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample**. Denne utvidelsen kaller funksjonene til POSNET-driveren for å sende kommandoer som CRT-utvidelsen genererer til bilagsskriveren. Den håndterer også enhetsfeil.

#### <a name="request-handler"></a>Forespørselsbehandler

Forespørselsbehandleren **FiscalPrinterHandler** er startpunktet for behandling av forespørsel til den eksterne regnskapsenheten.

Behandleren arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på regnskapskoblingen som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler:

- **SubmitDocumentFiscalDeviceRequest** – Denne forespørselen sender dokumenter til skriveren og returnerer svaret fra bilagsskriveren.
- **IsReadyFiscalDeviceRequest** – Denne forespørselen brukes for en tilstandskontroll av enheten.
- **InitializeFiscalDeviceRequest** – Denne forespørselen brukes til å initialisere skriveren.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen ligger i **Konfigurasjon**-mappen for utvidelsesprosjektet: Formålet med filen er å aktivere innstillinger for koblingen som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering. Følgende innstillinger legges til:

- **Tilkoblingsstreng** – En streng som beskriver detaljene i tilkoblingen til enheten i et format som støttes av driveren. Hvis du vil ha mer informasjon, kan du se Ett dokumentasjonen for POSNET-driveren.
- **Dato- og tidssynkronisering** – En verdi som angir om datoen og klokkeslettet for skriveren må synkroniseres med den tilkoblede maskinvarestasjonen.
- **Tidsavbrudd for enhet** – Tiden, i millisekunder, som driveren vil vente på svar fra enheten. Hvis du vil ha mer informasjon, kan du se Ett dokumentasjonen for POSNET-driveren.
