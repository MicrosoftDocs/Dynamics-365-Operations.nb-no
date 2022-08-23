---
title: Eksempel på integrering av bilagsskriver for Polen
description: Denne artikkelen gir en oversikt over eksemplet på regnskapsintegrering for Polen i Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-01
ms.openlocfilehash: 1466532099820abcdf4496db80f9a34682e2ed5a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274239"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>Eksempel på integrering av bilagsskriver for Polen

[!include[banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over eksemplet på regnskapsintegrering for Polen i Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce-funksjonen for Polen omfatter en eksempelintegrering av salgsstedet med en bilagsskriver. Eksemplet utvider [integreringsfunksjonaliteten for regnskap](fiscal-integration-for-retail-channel.md) og støtter POSNET INTEGRATION 2.02-protokollen for bilagsskrivere fra [Posnet Polska S.A.](https://www.posnet.com.pl) Eksemplet aktiverer kommunikasjon med en bilagsskriver som er koblet til via en COM-port ved hjelp av en programvaredriver. Den ble implementert og testet ved hjelp av en programvareemulator som Posnet leverte for Posnet Thermal HD FV EJ-bilagsskriveren. Eksemplet leveres i form av kildekode og er en del av Retail Software Development Kit (SDK).

Microsoft frigir ikke maskinvare, programvare eller dokumentasjon fra Posnet. Hvis du vil ha mer informasjon om hvordan du får tak i bilagsskriveren og bruker den, kan du kontakte [Posnet Polska S.A.](https://www.posnet.com.pl)

## <a name="scenarios"></a>Scenarier

Følgende scenarioer dekkes av eksemplet på integrering av bilagsskriver for Polen:

- Salgsscenarioer:

    - Skriv ut en bilagskvittering for kontantsalg og returer.
    - Hent et svar fra bilagsskriveren, og lagre det i kanaldatabasen.
    - Avgifter:

        - Tilordne til bilagsskriverens avgiftskoder (avdelinger).
        - Overfør tilordnede avgiftsdata til bilagsskriveren.

    - Betalinger:

        - Tilordne til bilagsskriverens betalingsmetoder.
        - Skriv ut betalinger på en bilagskvittering.
        - Skriv ut endringsinformasjon.

    - Skriv ut linjerabatter.
    - Gavekort:

        - Utelat en utstedt / ny belastet gavekortlinje fra en bilagskvittering for et salg.
        - Skriv ut en betaling som bruker et gavekort som en vanlig betalingsmetode.

    - Skriv ut bilagskvitteringer for kundeordreoperasjoner:

        - Det skrives ikke ut en bilagskvittering for en kundeordreinnbetaling.
        - Skriv ut en bilagskvittering for utføringslinjer av en hybridkundeordre.
        - Skriv ut en bilagskvittering for plukkoperasjonen for en kundeordre.
        - Skriv ut en bilagskvittering for en returordre.

    - Skriv ut [kundeinformasjonen](emea-pol-customer-information.md) som er angitt for en salgstransaksjon ved en bilagskvittering. Et eksempel på denne informasjonen er kundens mva-nummer.

- Dagsoppgjør (X- og Z-rapporter for regnskap).
- Feilhåndtering, for eksempel følgende alternativer:

    - Prøv regnskapsregistrering på nytt hvis det er mulig, for eksempel hvis den ikke er koblet til en bilagsskriver, den ikke er klar eller ikke svarer, skriveren er tom for papir eller det er papirstopp.
    - Utsett regnskapsregistrering.
    - Hopp over regnskapsregistrering eller merk transaksjonen som registrert, og inkluder informasjonskoder for å registrere årsaken til feilen og tilleggsinformasjon.
    - Kontroller tilgjengeligheten av bilagsskriveren før en ny salgstransaksjon åpnes eller en salgstransaksjon fullføres.

### <a name="gift-cards"></a>Gavekort

Eksemplet på integrering av bilagsskriver implementerer følgende regler som er relatert til gavekort:

- Utelukk salgslinjer som er relatert til *utsendelsesgavekortet*, og *Legg til gavekort*-operasjoner fra bilagskvitteringen.
- Ikke skriv ut en bilagskvittering hvis den bare består av gavekortlinjer.
- Trekk fra totalt antall gavekort som er utstedt eller belastet på nytt i en transaksjon fra betalingslinjene på bilagskvitteringen.
- Lagre beregnede justeringer av betalingslinjer i kanaldatabasen med en referanse til en tilsvarende regnskapstransaksjon.
- Betaling med gavekort regnes som en vanlig betaling.

### <a name="customer-deposits-and-customer-order-deposits"></a>Kundeinnbetalinger og kundeordreinnbetalinger

Eksemplet på integrering av regnskapsskriver implementerer følgende regler som er relatert til kundeinnbetaling og kundeordreinnbetaling:

- Ikke skriv ut en bilagskvittering hvis en transaksjon er en kundeinnbetaling.
- Ikke skriv ut en bilagskvittering hvis en transaksjon bare inneholder et innbetalingsbeløp for kundeordre eller en innbetalingsrefusjon for kundeordre.
- Skriv ut beløpet for det tidligere betalte innbetaling på en bilagskvittering for en plukkoperasjon for kundeordre.
- Trekk fra innbetalingsbeløpet for kundeordren fra betalingslinjen når det opprettes en hybridkundeordre.
- Lagre beregnede justeringer av betalingslinjer i kanaldatabasen med en referanse til en regnskapstransaksjon for en hybridkundeordre.

### <a name="limitations-of-the-sample"></a>Begrensninger i eksemplet

- Bilagsskriveren støtter bare scenarioer der merverdiavgift er inkludert i prisen. Derfor må alternativet **Pris inkludert merverdiavgift** settes til **Ja** for både butikker og kunder.
- Daglige rapporter (regnskapsår X og regnskapsår Z) skrives ut ved hjelp av det innebygde formatet *skiftrapport*.
- Utskrift av en strekkode på bilagskvitteringer regnes som en potensiell tilpasning, fordi denne funksjonen ikke støttes i de innebygde formatene og kan bare implementeres ved å bruke den tilpassede rapporten **Super-format**.
- Bilagsskriveren støtter ikke blandede transaksjoner. Alternativet **Hindre blanding av salg og returer på én kvittering** skal settes til **Ja** i salgsstedsfunksjonalitetsprofiler.

## <a name="set-up-fiscal-integration-for-poland"></a>Definere regnskapsintegrering for Polen

Eksemplet på integrering av bilagsskriver for Polen er basert på [regnskapsintegreringsfunksjonaliteten](fiscal-integration-for-retail-channel.md) og er en del av Retail SDK. Eksemplet finnes i **src\\FiscalIntegration\\Posnet**-mappen i repositoriet for [løsningen for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (for eksempel [eksemplet i release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) av en regnskapsdokumentleverandør, som er en utvidelse av Commerce Runtime (CRT) og en regnskapskobling, som er en utvidelse av Commerce-maskinvarestasjon. Hvis du vil ha mer informasjon om hvordan du bruker Retail SDK, kan du se [Retail SDK-arkitektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en kompileringskontroll for uavhengig emballasje-SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en virtuell utviklermaskin (VM) i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for eksempler på integrering av bilagsskriver for Polen (eldre)](emea-pol-fpi-sample-sdk.md).
>
> Støtte for den nye uavhengige emballasje- og utvidelsesmodellen for regnskapsintegreringseksempler planlegges for senere versjoner.

Fullfør fremgangsmåten for oppsett av regnskapsintegrering slik det beskrives i [Oppsett av regnskapsintegrering for Commerce-kanaler](setting-up-fiscal-integration-for-retail-channel.md).

1. [Definer en regnskapsregistreringsprosess](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Noter deg også innstillingene for regnskapsregistreringsprosessen som er [spesifikke for dette eksemplet med integrering av bilagsskriveren](#set-up-the-registration-process).
1. [Angi innstillinger for feilbehandling](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Konfigurer X-/Z-regnskapsrapporter fra salgsstedet](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Aktiver manuell kjøring av utsatt bilagsregistrering](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurere kanalkomponenter](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Definere registreringsprosessen

Hvis du vil aktivere registreringsprosessen, følger du denne fremgangsmåten for konfigurere Commerce Headquarters. Hvis du vil ha mer informasjon om regnskapsintegrering, kan du se [Definere økonomisk integrering for handelskanaler](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Last ned konfigurasjonsfiler for regnskapsdokumentleverandøren og regnskapskoblingen:

    1. Open respositoriet for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Velg riktig frigivelsesavdelingsversjon i henhold til SDK/programversjonen (for eksempel **[release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Åpne **src \> FiscalIntegration \> Posnet**.
    1. Last ned leverandørkonfigurasjonsfilen for regnskapsdokument under **CommerceRuntime \> DocumentProvider.PosnetSample \> Konfigurasjon \> DocumentProviderPosnetSample.xml** (for eksempel [filen for release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/CommerceRuntime/DocumentProvider.PosnetSample/Configuration/DocumentProviderPosnetSample.xml)).
    1. Last ned konfigurasjonsfilen for regnskapskobling under **HardwareStation \> ThermalDeviceSample \> Konfigurasjon \> ConnectorPosnetThermalFVEJ.xml** (for eksempel [filen for release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/HardwareStation/ThermalDeviceSample/Configuration/ConnectorPosnetThermalFVEJ.xml)).

    > [!WARNING]
    > På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en utvikler-VM i LCS. Konfigurasjonsfilene for dette regnskapsintegreringseksemplet ligger i følgende mapper for Retail SDK på en utvikler-VM i LCS:
    >
    > - **Konfigurasjonsfil for regnskapsdokumentleverandør:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.PosnetSample\\Konfigurasjon\\DocumentProviderPosnetSample.xml
    > - **Konfigurasjonsfil for regnskapskobling:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.Posnet.ThermalDeviceSample\\Konfigurasjon\\ConnectorPosnetThermalFVEJ.xml
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

- **Tilordning av merverdiavgiftssatser (mva.)**– Tilordningen av avgiftsprosentverdier som er definert for mva-kodene til mva-satser for bilagsskriver. Her er standardtilordningen:

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    Den første komponenten i hvert par representerer et mva-satsnummer som konfigureres i bilagsskriveren. Den andre komponenten representerer den tilsvarende mva-satsen. Hvis du vil ha mer informasjon om konfigurasjonen av mva-satsen for bilagsskriver, kan du se dokumentasjonen for POSNET-driveren.

- **Tilordning av betalingsmiddeltype** – Tilordningen av betalingsmetoder som er konfigurert for butikken til betalingsformene som støttes av bilagsskriveren. Her er standardtilordningen:

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    Den første komponenten i hvert par representerer en betalingsmetode som er definert for butikken. Den andre komponenten representerer tilsvarende betalingsform som støttes av bilagsskriveren. Hvis du vil ha mer informasjon om betalingsformer som bilagsskriveren støtter, kan du se dokumentasjonen for POSNET-driveren. Du må endre eksempeltilordningen i henhold til betalingsmetodene som er konfigurert i programmet.

#### <a name="fiscal-connector-settings"></a>Innstillinger for regnskapskobling

Følgende innstillinger er inkludert i konfigurasjonen for regnskapskoblingen som angis som en del av eksempelet på regnskapsintegrering:

- **Tilkoblingsstreng** – En streng som beskriver detaljene i tilkoblingen til enheten i et format som støttes av driveren. Hvis du vil ha mer informasjon, kan du se Ett dokumentasjonen for POSNET-driveren.
- **Dato- og tidssynkronisering** – En verdi som angir om datoen og klokkeslettet for skriveren må synkroniseres med den tilkoblede maskinvarestasjonen.
- **Tidsavbrudd for enhet** – Tiden, i millisekunder, som driveren vil vente på svar fra enheten. Hvis du vil ha mer informasjon, kan du se Ett dokumentasjonen for POSNET-driveren.

### <a name="configure-channel-components"></a>Konfigurere kanalkomponenter

> [!WARNING]
> På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en utvikler-VM i LCS. Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for eksempler på integrering av bilagsskriver for Polen (eldre)](emea-pol-fpi-sample-sdk.md).
>
> Støtte for den nye uavhengige emballasje- og utvidelsesmodellen for regnskapsintegreringseksempler planlegges for senere versjoner.

#### <a name="set-up-the-development-environment"></a>Definere utviklingsmiljøet

Følg denne fremgangsmåten for å definere et distribusjonsmiljø slik at du kan teste og utvide eksemplet.

1. Klon eller last ned repositoriet for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions). Velg riktig frigivelsesavdelingsversjon i henhold til SDK/programversjonen. Hvis du vil ha mer informasjon, kan du se [Last ned eksempler og referansepakker i SDK for Retail fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Åpne integreringsløsningen for bilagsskriver i **Dynamics365Commerce.Solutions\\FiscalIntegration\\Posnet\\Posnet.sln**, og bygg den.
1. Installer CRT-utvidelser:

    1. Finn installasjonsprogrammet for CRT-utvidelsen:

        - **Commerce Scale Unit:** I mappen **Posnet\\ScaleUnit\\ScaleUnit.Posnet.Installer\\bin\\Debug\\net461** finner du installasjonsprogrammet **scaleUnit.Posnet.Installer**.
        - **Lokal CRT på Modern POS:** I mappen **Posnet\\ModernPOS\\ModernPOS.Posnet.Installer\\bin\\Debug\\net461** finner du installeringsprogrammet **ModernPOS.Posnet.Installer**.

    1. Start installeringsprogrammet for CRT-utvidelsen fra kommandolinjen:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **Lokal CRT på Modern POS:**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. Installer utvidelser for maskinvarestasjon:

    1. I mappen **Posnet\\HardwareStation\\HardwareStation.PosnetThermalFVFiscalPrinter.Installer\\bin\\Debug\\net461** finner du installasjonsprogrammet **HardwareStation.PosnetThermalFVFiscalPrinter.Installer**.
    1. Start installeringsprogrammet for utvidelsen fra kommandolinjen:

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Produksjonsmiljø

Følg fremgangsmåten i [Konfigurer en kompileringskontroll for et regnskapsintegreringseksempel](fiscal-integration-sample-build-pipeline.md) for å generere og frigi skyskalaenheten og selvbetjeningsdistribusjonspakker for eksemplet på regnskapsintegrering. Du finner YAML-filen for **Posnet build-pipeline.yml**-malen i **Pipeline\\YAML_Files** i repositoriet for [løsningene for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-extensions"></a>Utforming av utvidelser

Eksemplet på integrering av bilagsskriver for Polen er basert på [regnskapsintegreringsfunksjonaliteten](fiscal-integration-for-retail-channel.md) og er en del av Retail SDK. Eksemplet finnes i **src\\FiscalIntegration\\Posnet**-mappen i repositoriet for [løsningen for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (for eksempel [eksemplet i release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) av en regnskapsdokumentleverandør, som er en utvidelse av CRT og en regnskapskobling, som er en utvidelse av Commerce-maskinvarestasjon. Hvis du vil ha mer informasjon om hvordan du bruker Retail SDK, kan du se [Retail SDK-arkitektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en kompileringskontroll for uavhengig emballasje-SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en utvikler-VM i LCS. Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for eksempler på integrering av bilagsskriver for Polen (eldre)](emea-pol-fpi-sample-sdk.md). Støtte for den nye uavhengige emballasje- og utvidelsesmodellen for regnskapsintegreringseksempler planlegges for senere versjoner.

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime-utvidelsesutforming

Formålet med filtypen som er en regnskapsdokumentleverandør, er å generere skriverpesifikke dokumenter og håndtere svar fra bilagsskriveren. Denne utvidelsen genererer et sett med skriverspesifikke kommandoer i JSON-formatet (JavaScript Object Notation) som er definert av POSNET-spesifikasjon 19-3678.

#### <a name="request-handler"></a>Forespørselsbehandler

Forespørselsbehandleren **DocumentProviderPosnetProtocol** er startpunktet for forespørselen om å generere dokumenter fra bilagsskriveren.

Behandleren arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på koblingsdokumentleverandøren som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler:

- **GetFiscalDocumentDocumentProviderRequest** – Denne forespørselen inneholder informasjon om hvilke dokumenter som skal genereres. Det returnerer et skriverspesifikk dokument som skal registreres i bilagsskriveren.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Denne forespørselen returnerer listen over hendelser du kan abonnere på. For øyeblikket støttes følgende hendelser: salg, utskrift av X-rapport og utskrift av Z-rapport.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen for regnskapsdokumentleverandør ligger under **src\\FiscalIntegration\\Posnet\\CommerceRuntime\\DocumentProvider.PosnetSample\\Konfigurasjon\\DocumentProviderPosnetSample.xml** i repositoriet for [løsningene for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er å aktivere innstillinger for dokumentleverandøren som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering.

### <a name="hardware-station-extension-design"></a>Utvidelsesutforming for maskinvarestasjon

Formålet med utvidelsen som er en regnskapskobling, er å kommunisere med bilagsskriveren. Denne utvidelsen kaller funksjonene til POSNET-driveren for å sende kommandoer som CRT-utvidelsen genererer til bilagsskriveren. Den håndterer også enhetsfeil.

#### <a name="request-handler"></a>Forespørselsbehandler

Forespørselsbehandleren **FiscalPrinterHandler** er startpunktet for behandling av forespørsel til den eksterne regnskapsenheten.

Behandleren arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på regnskapskoblingen som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler:

- **SubmitDocumentFiscalDeviceRequest** – Denne forespørselen sender dokumenter til skriveren og returnerer svaret fra bilagsskriveren.
- **IsReadyFiscalDeviceRequest** – Denne forespørselen brukes for en tilstandskontroll av enheten.
- **InitializeFiscalDeviceRequest** – Denne forespørselen brukes til å initialisere skriveren.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen for regnskapskoblingen ligger under **src\\FiscalIntegration\\Posnet\\HardwareStation\\ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml** i repositoriet for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er å aktivere innstillinger for regnskapskoblingen som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
