---
title: Eksempel på integrering av bilagsskriver for Italia
description: Dette emnet gir en oversikt over eksemplet på regnskapsintegrering for Italia i Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.openlocfilehash: 592cecff5b6179e7afd1bacb25beda277dfb8fa3
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944640"
---
# <a name="fiscal-printer-integration-sample-for-italy"></a>Eksempel på integrering av bilagsskriver for Italia

[!include[banner](../includes/banner.md)]

Dette emnet gir en oversikt over eksemplet på regnskapsintegrering for Italia i Microsoft Dynamics 365 Commerce.

Commerce-funksjonen for Italia omfatter en eksempelintegrering av salgsstedet med en bilagsskriver. Eksemplet utvider [funksjonaliteten for regnskapsintegrering](fiscal-integration-for-retail-channel.md) slik at den fungerer med [Epson FP-90III Series](https://www.epson.it/products/sd/pos-printer/epson-fp-90iii-series)-skrivere fra Epson, og det gjør det mulig å kommunisere med en bilagsskriver i nettservermodus via EpsonFPMate-nettjenesten ved hjelp av Fiscal ePOS-Print-API-en. Eksemplet støtter bare modusen Registratore Telematico (RT). Eksemplet leveres i form av kildekode og er en del av Retail Software Development Kit (SDK).

Microsoft frigir ikke maskinvare, programvare eller dokumentasjon fra Epson. Hvis du vil ha mer informasjon om hvordan du får tak i bilagsskriveren og bruker den, kan du kontakte [Epson Italia S.p.A](https://www.epson.it).

## <a name="scenarios"></a>Scenarier

Følgende scenarioer dekkes av eksemplet på integrering av bilagsskriver for Italia:

- Salgsscenarioer:

    - Skriv ut en bilagskvittering for kontantsalg og returer.
    - Hent et svar fra bilagsskriveren, og lagre det i kanaldatabasen.
    - Avgifter:

        - Tilordne til bilagsskriverens avgiftskoder (avdelinger).
        - Overfør tilordnede avgiftsdata til bilagsskriveren.
        - Skriv ut avgifter på en bilagskvittering.

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

    - Skriv ut en strekkode for kvitteringsnummeret på en regnskapskvittering.
    - Skriv ut [kundeinformasjonen](emea-ita-customer-information.md) som er angitt for en salgstransaksjon ved en bilagskvittering. Et eksempel på denne informasjonen er kundens lotterikode. 

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
- Daglige rapporter (regnskapsår X og regnskapsår Z) skrives ut ved hjelp av formatet som er innebygd i bilagsskriverens innhold.
- Bilagsskriveren støtter ikke blandede transaksjoner. Alternativet **Hindre blanding av salg og returer på én kvittering** skal settes til **Ja** i salgsstedsfunksjonalitetsprofiler.
- Eksemplet støtter bare integrering med en bilagsskriver som fungerer i modusen Registratore Telematico (RT)).

## <a name="set-up-fiscal-integration-for-italy"></a>Definere regnskapsintegrering for Italia

Eksemplet på integrering av bilagsskriver for Italia er basert på [regnskapsintegreringsfunksjonaliteten](fiscal-integration-for-retail-channel.md) og er en del av Retail SDK. Eksemplet finnes i **src\\FiscalIntegration\\EpsonFP90IIISample**-mappen i repositoriet for [løsningen for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (for eksempel [eksemplet i release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) av en regnskapsdokumentleverandør, som er en utvidelse av Commerce Runtime (CRT) og en regnskapskobling, som er en utvidelse av Commerce-maskinvarestasjon. Hvis du vil ha mer informasjon om hvordan du bruker Retail SDK, kan du se [Retail SDK-arkitektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en kompileringskontroll for uavhengig emballasje-SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en virtuell utviklermaskin (VM) i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for eksempler på integrering av bilagsskriver for Italia (eldre)](emea-ita-fpi-sample-sdk.md).
>
> Støtte for den nye uavhengige emballasje- og utvidelsesmodellen for regnskapsintegreringseksempler planlegges for senere versjoner.

Fullfør fremgangsmåten for oppsett av regnskapsintegrering slik det beskrives i [Oppsett av regnskapsintegrering for Commerce-kanaler](setting-up-fiscal-integration-for-retail-channel.md).

1. [Definer en regnskapsregistreringsprosess](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Noter deg også innstillingene for regnskapsregistreringsprosessen som er [spesifikke for dette eksemplet med integrering av bilagsskriveren](#set-up-the-registration-process).
1. [Konfigurere bilagstekster for rabatter](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).
1. [Angi innstillinger for feilbehandling](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Konfigurer X-/Z-regnskapsrapporter fra salgsstedet](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Aktiver manuell kjøring av utsatt bilagsregistrering](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Definer funksjonaliteten for administrasjon av kundeinformasjon i salgssted](emea-ita-customer-information.md#setup).
1. [Konfigurere kanalkomponenter](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Definere registreringsprosessen

Hvis du vil aktivere registreringsprosessen, følger du denne fremgangsmåten for konfigurere Commerce Headquarters. Hvis du vil ha mer informasjon om regnskapsintegrering, kan du se [Definere økonomisk integrering for handelskanaler](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Last ned konfigurasjonsfiler for regnskapsdokumentleverandøren og regnskapskoblingen:

    1. Open respositoriet for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Velg riktig frigivelsesavdelingsversjon i henhold til SDK/programversjonen (for eksempel **[release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Åpne **src \> FiscalIntegration \> EpsonFP90IIISample**.
    1. Last ned leverandørkonfigurasjonsfilen for regnskapsdokument under **CommerceRuntime \> DocumentProvider.EpsonFP90IIISample \> Konfigurasjon \> DocumentProviderEpsonFP90IIISample.xml** (for eksempel [filen for release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/CommerceRuntime/DocumentProvider.EpsonFP90IIISample/Configuration/DocumentProviderEpsonFP90IIISample.xml)).
    1. Last ned konfigurasjonsfilen for regnskapskobling under **HardwareStation \> EpsonFP90IIIFiscalDeviceSample \> Konfigurasjon \> ConnectorEpsonFP90IIISample.xml** (for eksempel [filen for release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/HardwareStation/EpsonFP90IIIFiscalDeviceSample/Configuration/ConnectorEpsonFP90IIISample.xml).

    > [!WARNING]
    > På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en utvikler-VM i LCS. Konfigurasjonsfilene for dette regnskapsintegreringseksemplet ligger i følgende mapper for Retail SDK på en utvikler-VM i LCS:
    >
    > - **Konfigurasjonsfil for regnskapsdokumentleverandør:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.EpsonFP90IIISample\\Konfigurasjon\\DocumentProviderEpsonFP90IIISample.xml
    > - **Konfigurasjonsfil for regnskapskobling:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EpsonFP90IIIFiscalDeviceSample\\Konfigurasjon\\ConnectorEpsonFP90IIISample.xml
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

- **Tilordning av betalingsmiddeltype** – Tilordningen av betalingsmetoder som er konfigurert for butikken til betalingstypene som bilagsskriveren støtter. Følgende eksempel viser standardtilordning.

    ```JSON
    {"PaymentMethods": [
        {"StorePaymentMethod":"1", "PrinterPaymentType":"0", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"3", "PrinterPaymentType":"2", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"4", "PrinterPaymentType":"2", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"6", "PrinterPaymentType":"0", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"8", "PrinterPaymentType":"6", "PrinterPaymentIndex":"01"}
        ],
        "DepositPaymentMethod": {"PrinterPaymentType":"2", "PrinterPaymentIndex":"00"}}
    ```

    Her er en forklaring på attributtene i denne tilordningen:

    - **StorePaymentMethod** er en betalingsmetode som er definert for butikken i **Retail og Commerce \> Kanaloppsettet \> Betalingsmetoder \> Betalingsmetoder**.
    - **PrinterPaymentType** og **PrinterPaymentIndex** er den tilsvarende betalingstypen og indeksen som er definert i dokumentasjonen for Epson-bilagsskriveren.
    - **DepositPaymentMethod** brukes til å angi en skrivers betalingstype og indeks for den delen av hentebeløpet for kundeordre som er utlignet med kundeordreinnbetalingen.

    Følgende tabell viser hvordan eksempeltilordningen for betalingsmetoder tilsvarer betalingsmetoder for butikk som er konfigurert i standard demodata.

    | Betalingsmåte | Navn på betalingsmåte |
    |----------------|---------------------|
    | 1              | Kontanter                |
    | 3              | Kort                |
    | 4              | Kundekonto    |
    | 6              | Valuta            |
    | 8              | Gavekort           |

    Du må endre eksempeltilordningen i henhold til betalingsmetodene som er konfigurert i programmet.

- **Strekkodetype for kvitteringsnummer** – Typen strekkode som brukes til å vise et kvitteringsnummer på en bilagskvittering. Standardtilordning er **CODE128**.
- **Skriv ut regnskapsdata i kvitteringshodet** – Hvis denne parameteren er aktivert, blir butikkinformasjon skrevet ut på bilagskvitteringen. Denne informasjonen inkluderer butikkens navn, adresse og avgiftsidentifikasjonsnummer, og kassererens navn.
- **Avdelingstilordning for bilagsskriver** – Tilordningen av avdelinger for bilagsskriveren til merverdiavgiftssatser (mva.), mva-fritakstyper og produkttyper. Følgende eksempel viser standardtilordning.

    ```JSON
    {"Departments": [
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"01"},
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"02"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"03"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"04"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"05"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"06"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"07"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"08"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"09"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"10"},
        {"VATRate":"0000", "VATExemptNature":"NS", "ProductType":"0", "DepartmentNumber":"99"}]}
    ```

    Her er en forklaring på attributtene i denne tilordningen:

    - **VATRate** er en mva-sats som støttes, som konfigureres som en mva-kode. Verdien i tilordningen har to desimalplasser, men ingen desimalskilletegn. **2200** representerer for eksempel 22 prosent, og **1000** representerer 10 prosent.
    - **VATExemptNature** gjelder bare i tilfeller der mva-satsen er 0 (null), inkludert tilfeller der det ikke er avgift. **VATExemptNature** støttes for øyeblikket bare for gavekort, og verdien i tilordningen bør samsvare med verdien i egenskapen **VATExemptNatureForGiftCard** i XML-konfigurasjonsfilen.
    - **ProductType** er produkttypen. En verdi på **0** representerer varer, og en verdi på **1** representerer tjenester.
    - **DepartmentNumber** er nummeret på avdelingen som er konfigurert i skriveren, og som tilsvarer de tre foregående attributtene.

    Du må endre eksempeltilordningen i henhold til mva-satsene som er konfigurert i programmet, og tilsvarende avdelinger som er konfigurert i bilagsskriveren.

- **Mva-fritakstype for gavekort** – Mva-fritaktype som skal brukes når et gavekort utstedes eller fylles på. Verdien må tilsvare en del av oppføringen i avdelingstilordningen for bilagsskriver. Standardtilordning er **NS**.
- **Aktiver gratisvarer** – Hvis denne parameteren er aktivert, aktiveres den spesielle *omaggio*-rabattjusteringstypen for varer som har en 100 prosent-rabatt.
- **Informasjonskode for returopprinnelse** – Informasjonskoden som brukes til å registrere opprinnelsen til en returtransaksjon hvis det ikke finnes noe opprinnelig salgsmottak. Denne parameteren brukes sammen med **Informasjonskoden for opprinnelig salgsdato** og parametere for **tilordning av returopprinnelse** til å generere en riktig melding i bilagskvitteringen om opprinnelsen til en returtransaksjon hvis det ikke finnes noen opprinnelig salgstransaksjon. 

    Denne informasjonskoden må konfigureres slik at brukeren kan velge eller angi et av de mulige opprinnelsene til returer i butikkene dine. Den kan for eksempel konfigureres som en liste over delkoder (for eksempel **Retur fra område** eller **Retur fra kiosk**). Parameteren **Tilordning av returopprinnelse** brukes deretter til å oversette verdien til informasjonskoden til en kommando for bilagsskriveren.

    Informasjonskoden som er valgt for **Informasjonskode for returopprinnelse**, må konfigureres som en obligatorisk informasjonskode som avlyses én gang per salgstransaksjon. Den bør tilordnes som informasjonskoden **Returprodukt** i salgsstedsfunksjonalitetsprofilen, slik at den avlyses når operasjonen **Returprodukt** kjøres.

    Det er ikke angitt noen standardverdi for denne tilordningen. Du må velge en informasjonskode som er konfigurert i programmet.

- **Informasjonskode for opprinnelig salgsdato** – Informasjonskoden som brukes til å registrere opprinnelig salgsdato for en returtransaksjon hvis det ikke finnes noe opprinnelig salgsmottak. Denne parameteren brukes sammen med **Informasjonskoden for returopprinnelse** og parametere for **tilordning av returopprinnelse** til å generere en riktig melding i bilagskvitteringen om opprinnelsen til en returtransaksjon hvis det ikke finnes noen opprinnelig salgstransaksjon.

    Informasjonskoden må konfigureres slik at feltet **Inndatatype** settes til **Dato**. Den bør konfigureres som en obligatorisk informasjonskode som avlyses én gang per salgstransaksjon. Den bør også tilordnes som **Tilknyttet informasjonskode** for informasjonskoden som er valgt for parameteren **Informasjonskode for returopprinnelse**, slik at de to informasjonskodene avlyses etter hverandre.

    Det er ikke angitt noen standardverdi for denne tilordningen. Du må velge en informasjonskode som er konfigurert i programmet.

- **Tilordning av returopprinnelse** – Tilordning av returopprinnelser som brukes til å skrive ut opprinnelsen til en returtransaksjon hvis det ikke finnes noe opprinnelig salgsmottak. Denne parameteren brukes sammen med parameterne **Informasjonskoden for returopprinnelse** og **Informasjonskode for opprinnelig salgsdato** til å generere en riktig melding i bilagskvitteringen om opprinnelsen til en returtransaksjon hvis det ikke finnes noen opprinnelig salgstransaksjon. Følgende eksempel viser standardtilordning.

    ```JSON
    {"ReturnOrigins": [
        {"ReturnOrigin":"1", "PrinterReturnOrigin":"POS"},
        {"ReturnOrigin":"2", "PrinterReturnOrigin":"ND"}
        ],
        "PrinterReturnOriginWithoutFiscalData":"POS"}
    ```

    Her er en forklaring på attributtene i denne tilordningen:

    - **ReturnOrigin** er et av de mulige opprinnelsene til returer i butikkene. Verdien må samsvare med en verdi av parameteren **Informasjonskode for returopprinnelse**.
    - **PrinterReturnOrigin** er et av returopprinnelsene som bilagsskriveren godtar (**POS**, **VR** eller **ND**).
    - **PrinterReturnOriginWithoutFiscalData** er returopprinnelsen som bilagsskriveren godtar, og som tilsvarer en returtransaksjon som er koblet til en opprinnelig salgstransaksjon som ikke har koblede regnskapsdata, fordi den ikke er registrert via en bilagsskriver. I dette tilfellet identifiseres den opprinnelige salgsdatoen som datoen for den opprinnelige salgstransaksjonen.

Følgende standard datatilordninger er foreldet og beholdes bare for bakoverkompatibilitet:

- Tilordning av merverdiavgiftskoder (mva.)
- Bankinnbetalingstype

#### <a name="fiscal-connector-settings"></a>Innstillinger for regnskapskobling

Følgende innstillinger er inkludert i konfigurasjonen for regnskapskoblingen som angis som en del av eksempelet på regnskapsintegrering:

- **Sluttpunktadresse** – URL-adressen til skriveren.
- **Dato- og tidssynkronisering** – En verdi som angir om datoen og klokkeslettet for skriveren må synkroniseres med den tilkoblede maskinvarestasjonen.

### <a name="configure-channel-components"></a>Konfigurere kanalkomponenter

> [!WARNING]
> På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en utvikler-VM i LCS. Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for eksempler på integrering av bilagsskriver for Italia (eldre)](emea-ita-fpi-sample-sdk.md).
>
> Støtte for den nye uavhengige emballasje- og utvidelsesmodellen for regnskapsintegreringseksempler planlegges for senere versjoner.

#### <a name="set-up-the-development-environment"></a>Definere utviklingsmiljøet

Følg denne fremgangsmåten for å definere et distribusjonsmiljø slik at du kan teste og utvide eksemplet.

1. Klon eller last ned repositoriet for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions). Velg riktig frigivelsesavdelingsversjon i henhold til SDK/programversjonen. Hvis du vil ha mer informasjon, kan du se [Last ned eksempler og referansepakker i SDK for Retail fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Åpne integreringsløsningen for bilagsskriver i **Dynamics365Commerce.Solutions\\FiscalIntegration\\EpsonFP90IIISample\\EpsonFP90IIISample.sln**, og bygg den.
1. Installer CRT-utvidelser:

    1. Finn installasjonsprogrammet for CRT-utvidelsen:

        - **Commerce Scale Unit:** I mappen **EpsonFP90IIISample\\ScaleUnit\\ScaleUnit.EpsonFP90III.Installer\\bin\\Debug\\net461** finner du installasjonsprogrammet **ScaleUnit.EpsonFP90III.Installer**.
        - **Lokal CRT Modern POS:** I mappen **EpsonFP90IIISample\\ModernPOS\\ModernPOS.EpsonFP90III.Installer\\bin\\Debug\\net461** finner du installeringsprogrammet **ModernPOS.EpsonFP90III.Installer**.

    1. Start installeringsprogrammet for CRT-utvidelsen fra kommandolinjen:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EpsonFP90III.Installer.exe install --verbosity 0
            ```

        - **Lokal CRT på Modern POS:**

            ```Console
            ModernPOS.EpsonFP90III.Installer.exe install --verbosity 0
            ```

1. Installer utvidelser for maskinvarestasjon:

    1. I mappen **EpsonFP90IIISample\\HardwareStation\\HardwareStation.EpsonFP90III.Installer\\bin\\Debug\\net461** finner du installasjonsprogrammet **HardwareStation.EpsonFP90III.Installer**.
    1. Start installeringsprogrammet for utvidelsen fra kommandolinjen:

        ```Console
        HardwareStation.EpsonFP90III.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Produksjonsmiljø

Følg fremgangsmåten i [Konfigurer en kompileringskontroll for et regnskapsintegreringseksempel](fiscal-integration-sample-build-pipeline.md) for å generere og frigi skyskalaenheten og selvbetjeningsdistribusjonspakker for eksemplet på regnskapsintegrering. Du finner YAML-filen for **EpsonFP90III build-pipeline.yml**-malen i **Pipeline\\YAML_Files** i repositoriet for [løsningene for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-extensions"></a>Utforming av utvidelser

Eksemplet på integrering av bilagsskriver for Italia er basert på [regnskapsintegreringsfunksjonaliteten](fiscal-integration-for-retail-channel.md) og er en del av Retail SDK. Eksemplet finnes i **src\\FiscalIntegration\\EpsonFP90IIISample**-mappen i repositoriet for [løsningen for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (for eksempel [eksemplet i release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) av en regnskapsdokumentleverandør, som er en utvidelse av CRT og en regnskapskobling, som er en utvidelse av Commerce-maskinvarestasjon. Hvis du vil ha mer informasjon om hvordan du bruker Retail SDK, kan du se [Retail SDK-arkitektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en kompileringskontroll for uavhengig emballasje-SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en utvikler-VM i LCS. Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for eksempler på integrering av bilagsskriver for Italia (eldre)](emea-ita-fpi-sample-sdk.md). Støtte for den nye uavhengige emballasje- og utvidelsesmodellen for regnskapsintegreringseksempler planlegges for senere versjoner.

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime-utvidelsesutforming

Formålet med filtypen som er en regnskapsdokumentleverandør, er å generere skriverpesifikke dokumenter og håndtere svar fra bilagsskriveren.

#### <a name="request-handler"></a>Forespørselsbehandler

Forespørselsbehandleren **DocumentProviderEpsonFP90III** er startpunktet for forespørselen om å generere dokumenter fra bilagsskriveren.

Behandleren arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på koblingsdokumentleverandøren som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler:

- **GetFiscalDocumentDocumentProviderRequest** – Denne forespørselen inneholder informasjon om hvilke dokumenter som skal genereres. Det returnerer et skriverspesifikk dokument som skal registreres i bilagsskriveren.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Denne forespørselen returnerer listen over hendelser du kan abonnere på. For øyeblikket støttes følgende hendelser: salg, utskrift av X-rapport og utskrift av Z-rapport.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen for regnskapsdokumentleverandør ligger under **src\\FiscalIntegration\\EpsonFP90IIISample\\CommerceRuntime\\DocumentProvider.EpsonFP90IIISample\\Konfigurasjon\\DocumentProviderEpsonFP90IIISample.xml** i repositoriet for [løsningene for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er å aktivere innstillinger for dokumentleverandøren som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering.

### <a name="hardware-station-extension-design"></a>Utvidelsesutforming for maskinvarestasjon

Formålet med utvidelsen som er en regnskapskobling, er å kommunisere med bilagsskriveren. Denne utvidelsen bruker HTTP-protokollen til å sende dokumenter som CRT-utvidelsen genererer til bilagsskriveren. Den håndterer også svarene som mottas fra bilagsskriveren.

#### <a name="request-handler"></a>Forespørselsbehandler

Forespørselsbehandleren **EpsonFP90IIISample** er startpunktet for behandling av forespørsel til den eksterne regnskapsenheten.

Behandleren arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på regnskapskoblingen som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler:

- **SubmitDocumentFiscalDeviceRequest** – Denne forespørselen sender dokumenter til skriveren og returnerer svaret fra bilagsskriveren.
- **IsReadyFiscalDeviceRequest** – Denne forespørselen brukes for en tilstandskontroll av enheten.
- **InitializeFiscalDeviceRequest** – Denne forespørselen brukes til å initialisere skriveren.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen for regnskapskobling ligger under **src\\FiscalIntegration\\EpsonFP90IIISample\\HardwareStation\\EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml** i repositoriet for [løsningene for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er å aktivere innstillinger for koblingen som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
