---
title: Eksempel på integrering med kontrollenheter for Sverige
description: Dette emnet gir en oversikt over eksemplet på regnskapsintegrering for Sverige i Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: ace1bd5b1a06317b6753a34779ecfa96e519a63e
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077019"
---
# <a name="control-unit-integration-sample-for-sweden"></a>Eksempel på integrering med kontrollenheter for Sverige

[!include [banner](../includes/banner.md)]

Dette emnet gir en oversikt over eksemplet på regnskapsintegrering for Sverige i Microsoft Dynamics 365 Commerce.

> [!NOTE]
> Denne funksjonaliteten for eksempel på regnskapsintegrering erstatter det tidligere [eksemplet for salgsstedsintegrering med kontrollenheter for Sverige](retail-sdk-control-unit-sample.md). Det forrige eksemplet benytter seg ikke av [regnskapsintegreringsrammeverket](./fiscal-integration-for-retail-channel.md) og blir foreldet i senere oppdateringer. Hvis du vil ha informasjon om hvordan du går over fra det tidligere eksemplet til eksemplet som tilsvarer versjon Dynamics 365 Commerce, versjon **10.0.22 og tidligere**, kan du se [Overføring fra eksempelet for tidligere integrering](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample).

Commerce-funksjonen for Sverige inneholder en eksempelintegrering av salgsstedet med spesifikke regnskapsenheter for Sverige som kalles *kontrollenheter*. Dette eksemplet utvider [funksjonaliteten for regnskapsintegrering](fiscal-integration-for-retail-channel.md). Det antas at en kontrollenhet er fysisk koblet til en maskinvarestasjon som salgsstedet er paret med. Som et eksempel bruker dette eksempelet applikasjonsprogrammeringsgrensesnittet (API) til [CleanCash Type A](https://www.retailinnovation.se/produkter)-kontrollenheten av Retail Copyright HTT AB. Versjon 1.1.4 av CleanCash API brukes.

Eksemplet leveres i form av kildekode og er en del av Retail Software Development Kit (SDK).

Microsoft frigir ikke maskinvare, programvare eller dokumentasjon fra Retail Innovation HTT AB. Hvis du vil ha mer informasjon om hvordan du får kontrollenheten og bruker den, kan du ta kontakt med [Retail Innovation HTT AB](https://www.retailinnovation.se/).

## <a name="scenarios"></a>Scenarier

Eksemplet på kontrollenhetsintegrering for Sverige inneholder følgende funksjoner:

- Salgs-, retur- og kvitteringskopier registreres automatisk i en kontrollenhet som er koblet til maskinvarestasjonen som er paret med salgsstedet.
- Kontrollkoden og produksjonsnummeret for kontrollenheten for en registrert transaksjon registreres fra kontrollenheten og lagres i transaksjonen. Disse dataene kalles også et *regnskapssvar*. Regnskapssvaret kan vises på **Butikktransaksjoner**-siden.
- Egendefinerte felter for kontrollkoden og produksjonsnummeret for kontrollenheten kan legges til i et kvitteringsoppsett. På den måten kan du skrive ut regnskapssvaret for en transaksjon på en kvittering.
- Regnskapssvaret for en transaksjon vises i kanalrapporten **Elektronisk journal  (Sverige)**.
- Flere alternativer for feilhåndtering er tilgjengelige. Her er noen eksempler:

    - Avgiftsregistrering for nye forsøk hvis det er mulig å gjøre et nytt forsøk. Du kan for eksempel gjøre et nytt forsøk på regnskapsregistrering hvis kontrollenheten ikke er koblet til, ikke er klar eller ikke svarer.
    - Utsett regnskapsregistrering.
    - Hopp over regnskapsregistrering eller merk transaksjonen som registrert, og inkluder informasjonskoder for å registrere årsaken til feilen og tilleggsinformasjon.
    - Bekreft tilgjengeligheten av kontrollenheten før en ny salgstransaksjon åpnes eller en salgstransaksjon fullføres.

### <a name="limitations-of-the-sample"></a>Begrensninger i eksemplet

Eksemplet på kontrollenhetsintegrering for Sverige støtter for øyeblikket ikke kundeordrescenarioer.

## <a name="setting-up-the-integration-with-control-units"></a>Konfigurering av integrering med kontrollenheter

Hvis du vil ha mer informasjon om oppsettet som kreves for Sverige, kan du se [Definere Commerce for Sverige](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden).

### <a name="configuring-swedenspecific-receipts"></a>Konfigurere kvitteringer spesifikke for Sverige

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurere egendefinerte felt, slik at de kan brukes i kvitteringsformater for salgskvitteringer

Du kan konfigurere språkteksten og de egendefinerte feltene som skal brukes i salgsstedskvitteringsformatene. Standardfirmaet til brukeren som oppretter kvitteringsoppsettet, må være den samme juridiske enheten der språktekstoppsettet opprettes. Du kan også opprette de samme språktekstene i både brukerens standardfirma og den juridiske enheten i butikken som oppsettet er opprettet for.

På siden **Språktekst** legger du til følgende poster for etikettene for de egendefinerte feltene for kvitteringsoppsett. Vær oppmerksom på at verdiene **Språk-ID**, **Tekst-ID** og **Tekst** som vises i tabellen, bare er eksempler. Du kan endre dem slik at de oppfyller dine krav. Verdiene for **Tekst-ID** som du bruker, må imidlertid være unike, og de må være lik eller større enn 900001.

Legg til følgende salgsstedsetiketter i **Salgssted**-delen på siden **Språktekst**.

| Språk-ID | Tekst-ID | Tekst                  |
|-------------|---------|-----------------------|
| en-US       | 900001  | Registrer kontrollkode |
| en-US       | 900002  | Register enhet       |

På siden **Egendefinerte felt** legger du til følgende poster for de egendefinerte feltene for oppsett av mottaket. Vær oppmerksom på at verdiene **Tekst-ID for overskrift** må samsvare med verdiene **Tekst-ID** som du har angitt på siden **Språktekst**.

| Navn                         | Type    | Tekst-ID for overskrift |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | Tilgang | 900001          |
| SE_FISCALREGISTERID          | Tilgang | 900002          |

> [!NOTE]
> Det er viktig at du angir riktige egendefinerte feltnavn, som vist i tabellen ovenfor. Et feil egendefinert feltnavn vil forårsake manglende data i kvitteringer.

#### <a name="configure-receipt-formats"></a>Konfigurere mottaksformater

For hvert nødvendig kvitteringsformat som kreves, endrer du verdien for feltet **Utskriftsatferd** til **Skriv alltid ut**.

I Utforming av kvitteringsformat legger du til de egendefinerte feltene i delen **Bunntekst**. Vær oppmerksom på at feltnavnene samsvarer med språktekstene som du definerte i forrige del i dette emnet.

- **Register kontrollkode** – Dette feltet skriver ut kontrollkoden.
- **Registrer enhet** – Dette feltet skriver ut produksjonsnummeret for kontrollenheten.

Hvis du vil ha mer informasjon om hvordan du arbeider med kvitteringsformater, kan du se [Kvitteringsmaler og utskrift](../receipt-templates-printing.md).

### <a name="set-up-fiscal-integration-for-sweden"></a>Definere regnskapsintegrering for Sverige

Eksemplet på integrering av kontrollenhet for Sverige er basert på [regnskapsintegreringsfunksjonaliteten](fiscal-integration-for-retail-channel.md) og er en del av Retail SDK. Eksemplet finnes i **src\\FiscalIntegration\\CleanCash**-mappen i repositoriet for [løsningen for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (for eksempel [eksemplet i release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) av en regnskapsdokumentleverandør, som er en utvidelse av Commerce Runtime (CRT) og en regnskapskobling, som er en utvidelse av Commerce-maskinvarestasjon. Hvis du vil ha mer informasjon om hvordan du bruker Retail SDK, kan du se [Retail SDK-arkitektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en kompileringskontroll for uavhengig emballasje-SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en virtuell utviklermaskin (VM) i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for eksempler på integrering av kontrollenhet for Sverige (eldre)](emea-swe-fi-sample-sdk.md).
>
> Støtte for den nye uavhengige emballasje- og utvidelsesmodellen for regnskapsintegreringseksempler planlegges for senere versjoner.

Fullfør fremgangsmåten for oppsett av regnskapsintegrering slik det beskrives i [Oppsett av regnskapsintegrering for Commerce-kanaler](setting-up-fiscal-integration-for-retail-channel.md).

1. [Definer en regnskapsregistreringsprosess](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Noter deg også innstillingene for regnskapsregistreringsprosessen som er [spesifikke for dette eksemplet med integrering av kontrollenheten](#set-up-the-registration-process).
1. [Angi innstillinger for feilbehandling](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Aktiver manuell kjøring av utsatt bilagsregistrering](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurere kanalkomponenter](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Definere registreringsprosessen

Hvis du vil aktivere registreringsprosessen, følger du denne fremgangsmåten for konfigurere Commerce Headquarters. Hvis du vil ha mer informasjon om regnskapsintegrering, kan du se [Definere økonomisk integrering for handelskanaler](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Last ned konfigurasjonsfiler for regnskapsdokumentleverandøren og regnskapskoblingen:

    1. Open respositoriet for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Velg riktig frigivelsesavdelingsversjon i henhold til SDK/programversjonen (for eksempel **[release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Åpne **src \> FiscalIntegration \> CleanCash**.
    1. Last ned leverandørkonfigurasjonsfilen for regnskapsdokument under **CommerceRuntime \> DocumentProvider.CleanCashSample \> Konfigurasjon \> DocumentProviderFiscalCleanCashSample.xml** (for eksempel [filen for release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/CommerceRuntime/DocumentProvider.CleanCashSample/Configuration/DocumentProviderFiscalCleanCashSample.xml)).
    1. Last ned konfigurasjonsfilen for regnskapskobling under **HardwareStation \> Connector.CleanCashSample \> Konfigurasjon \> ConnectorCleanCashSample.xml** (for eksempel [filen for release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml)).

    > [!WARNING]
    > På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en utvikler-VM i LCS. Konfigurasjonsfilene for dette regnskapsintegreringseksemplet ligger i følgende mapper for Retail SDK på en utvikler-VM i LCS:
    >
    > - **Konfigurasjonsfil for regnskapsdokumentleverandør:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.CleanCashSample\\Konfigurasjon\\DocumentProviderFiscalCleanCashSample.xml
    > - **Konfigurasjonsfil for regnskapskobling:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.CleanCashSample\\Konfigurasjon\\ConnectorCleanCashSample.xml
    > 
    > Støtte for den nye uavhengige emballasje- og utvidelsesmodellen for regnskapsintegreringseksempler planlegges for senere versjoner.

1. Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> Delte handelsparametere**. På **Generelt**-fanen angir du **Aktiver regnskapsintegrering**-alternativet til **Ja**.
1. Gå til **Retail og Commerce \> Kanaloppsett \> Regnskapsintegrering \> Leverandører for regnskapsdokument**, og last inn konfigurasjonsfil for regnskapsdokumentleverandør som du lastet ned tidligere.
1. Gå til **Retail og Commerce \> Kanaloppsett \> Regnskapsintegrering \> Regnskapskoblinger**, og last inn konfigurasjonsfilen for regnskapskobling som du lastet ned tidligere.
1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Regnskapsintegrering \> Funksjonsprofiler for kobling**. Opprett en ny funksjonsprofil for kobling. Velg dokumentleverandøren og koblingen du lastet inn tidligere. Oppdater [innstillingene for datatilordning](#default-data-mapping) etter behov.
1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Regnskapsintegrering \> Tekniske profiler for kobling**. Opprett en ny teknisk profil for kobling, og velg regnskapskoblingen du lastet inn tidligere. Oppdater [koblingsinnstillingene](#fiscal-connector-settings) etter behov.
6. Gå til **Detaljhandel og handel \> Kanaloppsett \> Regnskapsintegrering \> Grupper for regnskapskobling**. Opprett en ny gruppe for regnskapskobling for funksjonsprofilen for koblingen som du opprettet tidligere.
7. Gå til **Detaljhandel og handel \> Kanaloppsett \> Regnskapsintegrering \> Regnskapsregistreringsprosesser**. Opprett en ny regnskapsregistreringsprosess og et trinn i regnskapsregistreringsprosessen, og velg regnskapskoblingsgruppen du opprettet tidligere.
8. Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Funksjonalitetsprofiler**. Velg en funksjonsprofil som er koblet til butikken der registreringsprosessen skal aktiveres. I hurtigfanen **Regnskapsregistreringsprosess** velger du regnskapsregistreringsprosessen du opprettet tidligere.
9. Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Maskinvareprofiler**. Velg en maskinvareprofil som er koblet til maskinvarestasjonen som bilagsskriveren skal kobles til. I hurtigganen **Eksterne regnskapsenheter** velger du den tekniske profilen for koblingen som du opprettet tidligere.
10. Åpne distribusjonsplanen (**Retail og Commerce \> IT for detaljhandel og handel \> Distribusjonsplan**), og velg jobbene **1070** og **1090** for å overføre data til kanaldatabasen.

#### <a name="default-data-mapping"></a>Standard datatilordning

Følgende standard datatilordning er inkludert i konfigurasjonen for regnskapsdokumentleverandøren som angis som en del av eksempelet på regnskapsintegrering:

- **Kodetilordning for merverdiavgift (mva.)** – Denne tilordningen setter enhetsspesifikke merverdiavgiftskoder (mva.) til tilsvarende mva-koder. Mva-kodetilordningen må ha følgende format:

    ```
    1 : code1 ; 2 : code2
    ```

    Her er en forklaring på dette formatet:

    - *1* og *2* er enhetsspesifikke mva-koder.
    - Et semikolon (;) brukes som et skilletegn.
    - *code1* og *code2* er mva-koder som er konfigurert i Commerce Headquarters. Du må endre eksempeltilordningen i henhold til avgiftskodene som er konfigurert i programmet.

    Kontrollenheter støtter opptil fire forskjellige mva-koder. Derfor kan mva-kodetilordningen defineres på følgende måte:

    ```
    1 : code1 ; 2 : code2 ; 3 : code3 ; 4 : code4
    ```

    > [!NOTE]
    > Flere mva-koder kan tilordnes til den samme enhetsspesifikke mva-koden.

#### <a name="fiscal-connector-settings"></a>Innstillinger for regnskapskobling

Følgende innstillinger er inkludert i konfigurasjonen for regnskapskoblingen som angis som en del av eksempelet på regnskapsintegrering:

- **Tilkoblingsstreng** – Tilkoblingsinnstillingene for kontrollenheten.
- **Tidsavbrudd** – Tiden, i millisekunder, som driveren vil vente på svar fra kontrollenheten.

### <a name="configure-channel-components"></a>Konfigurere kanalkomponenter

> [!WARNING]
> På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en utvikler-VM i LCS. Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for eksempler på integrering av kontrollenhet for Sverige (eldre)](emea-swe-fi-sample-sdk.md).
>
> Støtte for den nye uavhengige emballasje- og utvidelsesmodellen for regnskapsintegreringseksempler planlegges for senere versjoner.

#### <a name="set-up-the-development-environment"></a>Definere utviklingsmiljøet

Følg denne fremgangsmåten for å definere et distribusjonsmiljø slik at du kan teste og utvide eksemplet.

1. Klon eller last ned repositoriet for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions). Velg riktig frigivelsesavdelingsversjon i henhold til SDK/programversjonen. Hvis du vil ha mer informasjon, kan du se [Last ned eksempler og referansepakker i SDK for Retail fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Åpne integreringsløsningen for kontrollenhet i **Dynamics365Commerce.Solutions\\FiscalIntegration\\CleanCash\\CleanCash.sln**, og bygg den.
1. Installer CRT-utvidelser:

    1. Finn installasjonsprogrammet for CRT-utvidelsen:

        - **Commerce Scale Unit:** I mappen **CleanCash\\ScaleUnit\\ScaleUnit.CleanCash.Installer\\bin\\Debug\\net461** finner du installasjonsprogrammet **scaleUnit.CleanCash.Installer**.
        - **Lokal CRT på Modern POS:** I mappen **CleanCash\\ModernPOS\\ModernPOS.CleanCash.Installer\\bin\\Debug\\net461** finner du installasjonsprogrammet **ModernPOS.CleanCash.Installer**.

    2. Start installeringsprogrammet for CRT-utvidelsen fra kommandolinjen:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **Lokal CRT på Modern POS:**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. Installer utvidelser for maskinvarestasjon:

    1. I mappen **CleanCash\\HardwareStation\\HardwareStation.CleanCash.Installer\\bin\\Debug\\net461** finner du installasjonsprogrammet **HardwareStation.CleanCash.Installer**.
    1. Start installeringsprogrammet for utvidelsen fra kommandolinjen:

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Produksjonsmiljø

Følg fremgangsmåten i [Konfigurer en kompileringskontroll for et regnskapsintegreringseksempel](fiscal-integration-sample-build-pipeline.md) for å generere og frigi skyskalaenheten og selvbetjeningsdistribusjonspakker for eksemplet på regnskapsintegrering. Du finner YAML-filen for **CleanCash build-pipeline.yml**-malen i **Pipeline\\YAML_Files** i repositoriet for [løsningene for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-the-extensions"></a>Utforming av utvidelsene

Eksemplet på integrering av kontrollenhet for Sverige er basert på [regnskapsintegreringsfunksjonaliteten](fiscal-integration-for-retail-channel.md) og er en del av Retail SDK. Eksemplet finnes i **src\\FiscalIntegration\\CleanCash**-mappen i repositoriet for [løsningen for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (for eksempel [eksemplet i release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) av en regnskapsdokumentleverandør, som er en utvidelse av CRT og en regnskapskobling, som er en utvidelse av Commerce-maskinvarestasjon. Hvis du vil ha mer informasjon om hvordan du bruker Retail SDK, kan du se [Retail SDK-arkitektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en kompileringskontroll for uavhengig emballasje-SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en utvikler-VM i LCS. Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for eksempler på integrering av kontrollenhet for Sverige (eldre)](emea-swe-fi-sample-sdk.md). Støtte for den nye uavhengige emballasje- og utvidelsesmodellen for regnskapsintegreringseksempler planlegges for senere versjoner.

### <a name="crt-extension-design"></a>CRT-utvidelsesutforming

Formålet med filtypen som er en regnskapsdokumentleverandør, er å generere servicespesifikke dokumenter og håndtere svar fra kontrollenheten.

#### <a name="request-handler"></a>Forespørselsbehandler

Det finnes en enkelt **DocumentProviderCleanCash**-forespørselsbehandler for dokumentleverandøren. Denne behandleren brukes til å generere regnskapsdokumenter for kontrollenheten.

Denne behandleren arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på koblingsdokumentleverandøren som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler:

- **GetFiscalDocumentDocumentProviderRequest** – Denne forespørselen inneholder informasjon om hvilke dokumenter som skal genereres. Det returnerer et servicespesifikk dokument som skal registreres i kontrollenheten.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Denne forespørselen returnerer listen over hendelser du kan abonnere på. Salgshendelser og revisjonshendelser støttes for øyeblikket.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen for regnskapsdokumentleverandør ligger under **src\\FiscalIntegration\\CleanCash\\CommerceRuntime\\DocumentProvider.CleanCashSample\\Konfigurasjon\\DocumentProviderFiscalCleanCashSample.xml** i repositoriet for [løsningene for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med denne filen er å aktivere innstillinger for dokumentleverandøren som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering.

### <a name="hardware-station-extension-design"></a>Utvidelsesutforming for maskinvarestasjon

Formålet med utvidelsen som er en regnskapskobling, er å kommunisere med kontrollenheten. Den bruker HTTP-protokollen til å sende dokumenter som CRT-utvidelsen genererer til kontrollenheten. Den håndterer også svarene som mottas fra kontrollenheten.

#### <a name="request-handler"></a>Forespørselsbehandler

Forespørselsbehandleren **CleanCashHandler** er startpunktet for behandling av forespørsler til kontrollenheten.

Behandleren arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på regnskapskoblingen som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler:

- **SubmitDocumentFiscalDeviceRequest** – Denne forespørselen sender dokumenter til kontrollenheten og returnerer et svar fra den.
- **IsReadyFiscalDeviceRequest** – Denne forespørselen brukes for en tilstandskontroll av kontrollenheten.
- **InitializeFiscalDeviceRequest** – Denne forespørselen brukes til å initialisere kontrollenheten.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen for regnskapskobling ligger under **src\\FiscalIntegration\\CleanCash\\HardwareStation\\Connector.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml** i repositoriet for [løsningene for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er å aktivere innstillinger for regnskapskoblingen som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
