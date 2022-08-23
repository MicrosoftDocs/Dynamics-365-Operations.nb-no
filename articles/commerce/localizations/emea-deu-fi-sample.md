---
title: Eksempel på integrering av tjenesten for avgiftsmessig transaksjon for Tyskland
description: Denne artikkelen gir en oversikt over eksemplet på regnskapsintegrering for Tyskland i Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-05-29
ms.openlocfilehash: 40f2b7ece62c495e4a719121019070a9961fa915
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280313"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>Eksempel på integrering av tjenesten for avgiftsmessig transaksjon for Tyskland

[!include[banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over eksemplet på regnskapsintegrering for Tyskland i Microsoft Dynamics 365 Commerce.

For å oppfylle lokale regnskapskravene for kasser i Tyskland inneholder Microsoft Dynamics 365 Commerce-funksjonaliteten for Tyskland et eksempel på integrering av salgsstedet med en ekstern regnskapsregistreringstjeneste. Eksemplet utvider [funksjonaliteten for regnskapsintegrering](fiscal-integration-for-retail-channel.md). Den er basert på løsningen [EFR (Electronic Fiscal Register)](https://www.efsta.eu/de/fiskalloesungen/deutschland) fra [EFSTA](https://www.efsta.eu/de/), og gjør det mulig å kommunisere med EFR-tjenesten via HTTPS-protokollen. EFR-tjenesten bør være vertsbasert enten på Retail-maskinvarestasjonen eller på en separat datamaskin som kan kobles til fra maskinvarestasjonen. Eksemplet leveres i form av kildekode og er en del av Retail Software Development Kit (SDK).

Microsoft frigir ikke maskinvare, programvare eller dokumentasjon fra EFSTA. Hvis du vil ha mer informasjon om hvordan du får EFR-løsningen og bruker den, kan du kontakte [EFSTA](https://www.efsta.eu/de/kontakt/kontakt).

## <a name="scenarios"></a>Scenarier

Følgende scenarioer dekkes av eksemplet på integrering av regnskapsregistreringstjenesten for Tyskland.

### <a name="sales-operations"></a>Salgsoperasjoner

- **Registrering av kontantsalg og returer i regnskapsregistreringstjenesten:**

    Registrering av salgsoperasjoner omfatter følgende trinn:

    1. Registrering av transaksjonsstarten

        Starten på hver transaksjon er registrert i et teknisk sikkerhetselement (TSE) som er koblet til EFR-tjenesten. Som et resultat av registreringen tilordner TSE en transaksjons-ID (TID).

    2. Registrering av transaksjonsslutten

        Når en transaksjon fullføres i salgsstedet, registreres den ved hjelp av den samme TID-en som ble tilordnet ved registrering av transaksjonsstarten. I det øyeblikket sendes detaljerte transaksjonsdata til regnskapsregistreringstjenesten. Disse dataene omfatter salgslinjeinformasjon og informasjon om rabatter, betalinger og avgifter.

    3. Henting av svar fra regnskapsregistreringstjenesten

        Sikkerhetsdata mottas fra et TSE som en del av et svar, og lagres i transaksjonen i kanaldatabasen. Sikkerhetsdataene består av følgende informasjon:

        - TID
        - Dato og klokkeslett for transaksjonsstarten
        - Dato og klokkeslett for transaksjonsslutten
        - Signaturteller
        - Sjekkverdi
        - Serienummer for TSE

- **Registrering av kundeordrer i regnskapsregistreringstjenesten:** Registreringsprosessen er den samme som prosessen for kontantsalg og returer.
- **Registrering av operasjoner som omfatter gavekort og innbetalinger:** Registreringsprosessen er den samme som prosessen for kontantsalg og returer.

#### <a name="notifying-users-about-fiscal-registration-failures"></a>Varsle brukere om feil i regnskapsregistrering

Det finnes to måter regnskapsregistreringstjenesten kan varsle brukere om feil som oppstod under regnskapsregistreringen:

- Skriv ut tilleggsinformasjon fra svaret i **Infomelding**-feltet på kvitteringer.
- Vis meldinger fra regnskapstjenesten som brukermeldinger i salgsstedet.

    > [!NOTE]
    > Denne varslingsmekanismen krever at parameteren **Vis regnskapsregistreringsvarslinger** på siden **Tekniske profiler for kobling** er aktivert.

#### <a name="printing-receipts"></a>Skriv ut kvitteringer

Kvitteringsutskrift er obligatorisk i Tyskland. Alle kvitteringer må inneholde minst følgende informasjon:

- Navn og adresse for selskapet
- Informasjon om varer, inkludert priser og antall
- Informasjon om betalinger som ble mottatt
- Informasjon om avgifter, inkludert totalbeløp etter mva-sats
- Sikkerhetsdata:

    - TID
    - Dato og klokkeslett for transaksjonsstarten
    - Dato og klokkeslett for transaksjonsslutten
    - Signaturteller
    - Sjekkverdi
    - Serienummer for TSE

- Informasjonsmelding

> [!NOTE]
> En QR-kode kan også skrives ut på kvitteringer. Selv om QR-koden er valgfri, anbefaltes den på det sterkeste. Hvis du vil ha mer informasjon om hvordan du får QR-kode som en del av et svar fra regnskapsregistreringstjenesten, kan du se dokumentet EFR Guide \[DE\] som er publisert på nettstedet for [EFSTA-dokumentasjonen](https://public.efsta.net/efr/).
>
> **Informasjonsmelding**-feltet på kvitteringer viser en varsling fra regnskapsregistreringstjenesten. Hvis for eksempel en signaturenhet brytes, kan spesialtekst skrives ut på en kvittering.

#### <a name="voided-suspended-and-recalled-transactions"></a>Annullerte, suspenderte og tilbakekalte transaksjoner

- En annullert transaksjon registreres som en forespørsel om å avslutte en transaksjon i regnskapsregistreringstjenesten.
- En suspendert transaksjon registreres som en forespørsel om å avslutte en transaksjon i regnskapsregistreringstjenesten.
- Tilbakekalling av en suspendert transaksjon registreres som starten på en ny transaksjon i regnskapsregistreringstjenesten.

### <a name="non-sales-transactions-and-shift-closing"></a>Ikke-salgstransaksjoner og skiftlukking

Følgende ikke-salgstransaksjoner registreres som ikke-regnskapsoperasjoner i regnskapsregistreringstjenesten ved hjelp av **NFS**-koden:

- Deklarer startbeløp
- Flytoppføring
- Fjerning av betalingsmidler
- Deponer til safe
- Deponer til bank
- Inntektskontoer
- Utgiftskontoer

**Lukk skift**-operasjonen registreres også som en ikke-regnskapsoperasjon i regnskapsregistreringstjenesten ved hjelp av **NFS**-koden.

### <a name="data-export-and-audit"></a>Dataeksport og -revisjon

Alle transaksjoner må signeres av et TSE for å sikre integritet, ekthet og fullstendighet, og for å forhindre manipulering av registrerte data.

> [!WARNING]
> Bare en bekreftet TSE kan brukes. Hvis du vil ha informasjon om typene og modellene til TSE som støttes i EFR-løsningen, kan du se dokumentet EFR Guide \[DE\] som er publisert på nettstedet for [EFSTA-dokumentasjonen](https://public.efsta.net/efr/). Hvis du vil ha mer informasjon om hvordan du velger og skaffer et TSE, kan du kontakte [EFSTA](https://www.efsta.eu/at/kontakt).

Bestemmelser i Tyskland krever støtte for DSFinV-K-eksporten. DSFinV-K-eksporten kan utløses i EFR-løsningen. Hvis du vil ha mer informasjon om DSFinV-K-eksporten, kan du se dokumentet EFR Guide \[DE\] som er publisert på nettstedet for [EFSTA-dokumentasjonen](https://public.efsta.net/efr/).

### <a name="limitations-of-the-sample"></a>Begrensninger i eksemplet

Regnskapsregistreringstjenesten støtter bare scenarioer der merverdiavgift er inkludert i prisene. Derfor må alternativet **Priser inkludert merverdiavgift** settes til **Ja** for både butikker og kunder.

Regnskapstjenesten støtter ikke situasjoner der mer enn én mva-kode brukes på samme transaksjonslinje.

Rammeverket for regnskapsintegrering støtter ikke salgstilbud. Derfor er disse operasjonene ikke registrert i regnskapstjenesten.

## <a name="set-up-commerce-for-germany"></a>Definere Commerce for Tyskland

Denne delen beskriver innstillingene for Commerce som er spesifikke og anbefalte for Tyskland. Hvis du vil ha mer oppsettinformasjon, kan du se [Startside for Commerce](../index.md).

Hvis du vil bruke funksjonaliteten som er spesifikke for Tyskland, må du angi følgende innstillinger.

- I primæradresse for den juridiske enheten setter du feltet **Land/område** til **DEU** (Tyskland).
- Sett feltet **ISO-kode** til **DE** (Tyskland) i salgsstedsfunksjonalitetsprofilen for hver butikk som finnes i Tyskland.

Du må også angi følgende innstillinger for Tyskland. Pass på at du kjører riktige distribusjonsjobber når du har fullført oppsettet.

### <a name="set-up-vat-per-german-requirements"></a>Definere merverdiavgift i henhold til tyske krav

Du må opprette mva-koder, mva-grupper og mva-grupper for varer. Du må også definere mva-informasjon for produkter og tjenester. Hvis du vil ha mer informasjon om hvordan du definerer og bruker mva-funksjoner, kan du se [Oversikt over merverdiavgift](../../finance/general-ledger/indirect-taxes-overview.md).

På salgskvitteringer kan du skrive ut en forkortet kode for en mva-kode (for eksempel A eller B). Hvis du vil gjøre denne funksjonaliteten tilgjengelig, angir du **Kode for utskrift**-feltet på siden **Mva-koder**.

### <a name="set-up-stores"></a>Konfigurer butikker

Oppdater butikkdetaljene på **Alle butikker**-siden. Du må angi følgende parametere:

- I feltet **Mva-gruppe** angir du mva-gruppen som skal brukes for salg til standardkunden.
- Sett alternativet **Priser inkluderer mva.** til **Ja**.
- Sett **Navn**-feltet til firmanavnet. Denne endringen bidrar til å sørge for at firmanavnet vises på en salgskvittering. Du kan også legge til firmanavnet i salgskvitteringsoppsettet som frihåndstekst.
- Sett feltet **TIN (Tax Identification Number)** til firmaidentifikasjonsnummeret. Denne endringen bidrar til å sørge for at firmaets identifikasjonsnummer vises på en salgskvittering. Du kan også legge til firmaets identifikasjonsnummer i salgskvitteringsoppsettet som frihåndstekst.

### <a name="set-up-functionality-profiles"></a>Konfigurere funksjonalitetsprofiler

Konfigurer salgsstedsfunksjonalitetsprofiler. I hurtigfanen **Kvitteringsnummerering** kan du definere kvitteringsnummerering ved å opprette eller oppdatere poster for transaksjonstypene **Salg**, **Salgsordre** og **Retur**.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurere egendefinerte felt, slik at de kan brukes i kvitteringsformater for salgskvitteringer

Du kan konfigurere språkteksten og de egendefinerte feltene som skal brukes i salgsstedskvitteringsformatene. Standardfirmaet til brukeren som oppretter kvitteringsoppsettet, må være den samme juridiske enheten der språktekstoppsettet opprettes. Du kan også opprette de samme språktekstene i både brukerens standardfirma og den juridiske enheten i butikken som oppsettet er opprettet for.

På siden **Språktekst** legger du til følgende poster for etikettene for de egendefinerte feltene for kvitteringsoppsett. Vær oppmerksom på at verdiene **Språk-ID**, **Tekst-ID** og **Tekst** som vises i tabellen, bare er eksempler. Du kan endre dem slik at de oppfyller dine krav. Verdiene for **Tekst-ID** som du bruker, må imidlertid være unike, og de må være lik eller mer enn 900001.

Legg til følgende salgsstedsetiketter i **Salgssted**-delen på siden **Språktekst**.

| Språk-ID | Tekst-ID | Tekst                                  |
|-------------|---------|---------------------------------------|
| en-US       | 900001  | QR-kode                               |
| en-US       | 900002  | Transaksjons-ID                        |
| en-US       | 900003  | Utskriftskode for detaljhandelsavgift                 |
| en-US       | 900004  | Avgiftsbeløp (salg)                    |
| en-US       | 900005  | Avgiftsgrunnlag (salg)                     |
| en-US       | 900006  | Startdato/-klokkeslett for transaksjon           |
| en-US       | 900007  | Sluttdato/-klokkeslett for transaksjon             |
| en-US       | 900008  | Serienummeret for sikkerhetselementet |
| en-US       | 900009  | Signaturteller                     |
| en-US       | 900010  | Sjekkverdi                           |
| en-US       | 900011  | Informasjonsmelding                          |

På siden **Egendefinerte felt** legger du til følgende poster for de egendefinerte feltene for oppsett av mottaket. Vær oppmerksom på at verdiene **Tekst-ID for overskrift** må samsvare med verdiene **Tekst-ID** som du har angitt på siden **Språktekst**.

| Navn                            | Type    | Tekst-ID for overskrift |
|---------------------------------|---------|-----------------|
| QRCODE\_DE                      | Tilgang | 900001          |
| TRANSACTIONID\_DE               | Tilgang | 900002          |
| RETAILPRINTCODE\_DE             | Tilgang | 900003          |
| SALESTAXAMOUNT\_DE              | Tilgang | 900004          |
| SALESTAXBASIS\_DE               | Tilgang | 900005          |
| TRANSACTIONSTARTDATETIME\_DE    | Tilgang | 900006          |
| TRANSACTIONENDDATETIME\_DE      | Tilgang | 900007          |
| SECURITYELEMENTSERIALNUMBER\_DE | Tilgang | 900008          |
| SIGNCOUNTER\_DE                 | Tilgang | 900009          |
| SIGN\_DE                        | Tilgang | 900010          |
| INFOMESSAGE\_DE                 | Tilgang | 900011          |

> [!NOTE]
> Det er viktig at du angir riktige egendefinerte feltnavn, som vist i foregående tabell. Et feil egendefinert feltnavn vil forårsake manglende data i kvitteringer.

### <a name="configure-receipt-formats"></a>Konfigurere mottaksformater

For hvert nødvendig kvitteringsformat som kreves, endrer du verdien for feltet **Utskriftsatferd** til **Skriv alltid ut**.

I Utforming av kvitteringsformat legger du til de egendefinerte feltene nedenfor i de aktuelle kvitteringsdelene. Vær oppmerksom på at feltnavnene samsvarer med språktekstene som du definerte i forrige del.

- **Topptekst:** Legg til følgende felter:

    - Feltene **Butikknavn** og **Avgiftsidentifikasjonsnummer**, som brukes til å skrive ut firmanavnet og identifikasjonsnummeret på kvitteringer. Du kan også legge til firmanavnet og identifikasjonsnummeret i salgskvitteringsoppsettet som frihåndstekst.
    - **Butikkadresse**, **Dato**, **Klokkeslett 24H**, **Kvitteringsnummer** og **Registreringsnummer**.

- **Linjer:** Legg til følgende felter:

    - Feltet **Varenavn**
    - Feltet **Ant.**
    - Feltet **Totalpris med avgift**
    - Feltet **Mva-kode for detaljhandelsutskrift**, som brukes til å skrive ut den forkortede koden som tilsvarer mva-koden som gjelder for varen

- **Bunntekst:** Legg til følgende felter:

    - Betalingsfelter, slik at betalingsbeløpene for hver betalingsmåte skrives ut. Du kan for eksempel legge til feltene **Betalingsmiddel** og **Betalingsmiddelbeløp** i én linje i oppsettet.
    - Felter i feltgruppen **Nedbrytning av avgift**. Alle feltene i denne feltgruppen må skrives ut på én egen linje.

        - Feltet **Avgifts-ID**, som er et standardfelt som gjør det mulig å skrive ut et mva-sammendrag for hver mva-kode. Feltet må legges til i en ny linje.
        - Feltet **Mva-prosent**, som er et standardfelt som brukes til å skrive ut den effektive mva-satsen for mva-koden.
        - Feltet **Avgiftsgrunnlag (salg)**, som brukes til å skrive ut kvitteringens totale kontantsalgsbeløp for mva-koden. Forskuddsbetalinger og gavekort utelates.
        - Feltet **Avgiftsbeløp (salg)**, som brukes til å skrive ut kvitteringens avgiftsbeløp for kontantsalg for mva-koden.
        - Feltet **Mva-kode for detaljhandelsutskrift**, som brukes til å skrive ut den forkortede koden som tilsvarer mva-koden.

    - Felter som inneholder sikrede transaksjonsdata som returneres av regnskapsregistreringstjenesten:

        - **Transaksjons-ID**-feltet som identifiserer nummeret til kontanttransaksjonen i regnskapsregistreringstjenesten
        - Feltet **Starttidspunkt for transaksjon**
        - Feltet **Sluttidspunkt for transaksjon**
        - Feltet **Serienummeret for sikkerhetselementet**
        - Feltet **Signaturteller**
        - Feltet **Sjekkverdi**
        - Feltet **QR-kode**, som brukes til å skrive ut referansen til den registrerte kontanttransaksjonen i form av en QR-kode

        > [!NOTE]
        > Verdien **QR-kode** hentes fra svaret på regnskapsregisteret. EFR returnerer bare en QR-kode i sitt svar hvis verdien i **Attributter**-feltet i EFR-konfigurasjonen er beskrevet i EFSTA-dokumentasjonen. QR-kodeformatet i **Attributter**-feltet i EFR-konfigurasjonen må være satt til **BMP**.

    - **Informasjonsmelding**-feltet slik at varslingsmeldinger fra regnskapsregistreringstjenesten vises på kvitteringer. Hvis for eksempel en signaturenhet brytes, kan spesialtekst skrives ut på en kvittering.

Hvis du vil ha mer informasjon om hvordan du arbeider med kvitteringsformater, kan du se [Definere og utforme kvitteringsformater](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-germany"></a>Definere regnskapsintegrering for Tyskland

Eksemplet på integrering av regnskapsregistreringstjenesten for Tyskland er basert på [regnskapsintegreringsfunksjonaliteten](fiscal-integration-for-retail-channel.md) og er en del av Retail SDK. Eksemplet finnes i **src\\FiscalIntegration\\Efr**-mappen i repositoriet for [løsningen for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (for eksempel [eksemplet i release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) av en regnskapsdokumentleverandør, som er en utvidelse av Commerce Runtime (CRT) og en regnskapskobling, som er en utvidelse av Commerce-maskinvarestasjon. Hvis du vil ha mer informasjon om hvordan du bruker Retail SDK, kan du se [Retail SDK-arkitektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en kompileringskontroll for uavhengig emballasje-SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en virtuell utviklermaskin (VM) i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for eksempler på regnskapsintegrering for Tyskland (eldre)](emea-deu-fi-sample-sdk.md).
>
> Støtte for den nye uavhengige emballasje- og utvidelsesmodellen for regnskapsintegreringseksempler planlegges for senere versjoner.

Fullfør fremgangsmåten for oppsett av regnskapsintegrering slik det beskrives i [Oppsett av regnskapsintegrering for Commerce-kanaler](setting-up-fiscal-integration-for-retail-channel.md):

1. [Definer en regnskapsregistreringsprosess](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Noter deg også innstillingene for regnskapsregistreringsprosessen som er [spesifikke for dette eksemplet med integrering av regnskapsregistreringstjenesten](#set-up-the-registration-process).
1. [Angi innstillinger for feilbehandling](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

    > [!WARNING]
    > Funksjonene for feilhåndtering i regnskapsintegreringsrammeverket er kanskje ikke helt samkjørt med lokale regnskapsbestemmelser.
    >
    > - Vi anbefaler at du lar alternativet **Fortsett med feil** på siden **Regnskapsregistreringsprosess** slås av, fordi alle transaksjoner må registreres riktig, selv om det første forsøket på avgiftsregistrering ikke er vellykket.
    > - Før du aktiverer alternativet **Hopp over** eller **Merk som registrert** på siden **Regnskapsregistreringsprosess**, bør du diskutere disse endringene i regnskapsregistreringsprosessen med skattekonsulenten eller det lokale skattekontoret.

1. [Aktiver manuell kjøring av utsatt bilagsregistrering](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurere kanalkomponenter](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Definere registreringsprosessen

Hvis du vil aktivere registreringsprosessen, følger du denne fremgangsmåten for konfigurere Commerce Headquarters. Hvis du vil ha mer informasjon om regnskapsintegrering, kan du se [Definere økonomisk integrering for handelskanaler](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Last ned konfigurasjonsfiler for regnskapsdokumentleverandøren og regnskapskoblingen:

    1. Open respositoriet for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Velg riktig frigivelsesavdelingsversjon i henhold til SDK/programversjonen (for eksempel **[release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Åpne **src \> FiscalIntegration \> Efr**.
    1. Last ned konfigurasjonsfilen for regnskapsdokumentleverandør under **Konfigurasjoner \> DocumentProviders \> DocumentProviderFiscalEFRSampleGermany.xml** (for eksempel [filen for release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleGermany.xml)).
    1. Last ned konfigurasjonsfilen for regnskapskoblingen under **Konfigurasjoner \> Koblinger \> ConnectorEFRSample.xml** (for eksempel [filen for release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en utvikler-VM i LCS. Konfigurasjonsfilene for dette regnskapsintegreringseksemplet ligger i følgende mapper for Retail SDK på en utvikler-VM i LCS:
    >
    > - **Konfigurasjonsfil for regnskapsdokumentleverandør:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Konfigurasjon\\DocumentProviderFiscalEFRSampleGermany.xml
    > - **Konfigurasjonsfil for regnskapskobling:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Konfigurasjon\\ConnectorEFRSample.xml
    > 
    > Støtte for den nye uavhengige emballasje- og utvidelsesmodellen for regnskapsintegreringseksempler planlegges for senere versjoner.

1. Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> Delte handelsparametere**. På **Generelt**-fanen angir du **Aktiver regnskapsintegrering**-alternativet til **Ja**.
1. Gå til **Retail og Commerce \> Kanaloppsett \> Regnskapsintegrering \> Leverandører for regnskapsdokument**, og last inn konfigurasjonsfil for regnskapsdokumentleverandør som du lastet ned tidligere.
1. Gå til **Retail og Commerce \> Kanaloppsett \> Regnskapsintegrering \> Regnskapskoblinger**, og last inn konfigurasjonsfilen for regnskapskobling som du lastet ned tidligere.
1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Regnskapsintegrering \> Funksjonsprofiler for kobling**. Opprett en ny funksjonsprofil for kobling. Velg dokumentleverandøren og koblingen du lastet inn tidligere. Oppdater [innstillingene for datatilordning](#default-data-mapping) etter behov.
1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Regnskapsintegrering \> Tekniske profiler for kobling**. Opprett en ny teknisk profil for kobling, og velg regnskapskoblingen du lastet inn tidligere. Oppdater [koblingsinnstillingene](#fiscal-connector-settings) etter behov.
1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Regnskapsintegrering \> Grupper for regnskapskobling**. Opprett en ny gruppe for regnskapskobling for funksjonsprofilen for koblingen som du opprettet tidligere.
1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Regnskapsintegrering \> Regnskapsregistreringsprosesser**. Opprett en ny regnskapsregistreringsprosess og et trinn i regnskapsregistreringsprosessen, og velg regnskapskoblingsgruppen du opprettet tidligere.
1. Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Funksjonalitetsprofiler**. Velg en funksjonsprofil som er koblet til butikken der registreringsprosessen skal aktiveres. I hurtigfanen **Regnskapsregistreringsprosess** velger du regnskapsregistreringsprosessen du opprettet tidligere.
1. Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Maskinvareprofiler**. Velg en maskinvareprofil som er koblet til maskinvarestasjonen som bilagsskriveren skal kobles til. I hurtigganen **Eksterne regnskapsenheter** velger du den tekniske profilen for koblingen som du opprettet tidligere.
1. Åpne distribusjonsplanen (**Retail og Commerce \> IT for detaljhandel og handel \> Distribusjonsplan**), og velg jobbene **1070** og **1090** for å overføre data til kanaldatabasen.

#### <a name="default-data-mapping"></a>Standard datatilordning

Følgende standard datatilordning er inkludert i konfigurasjonen for regnskapsdokumentleverandøren som angis som en del av eksempelet på regnskapsintegrering:

- **Tilordning av betalingsmiddel** – Tilordningen av betalingsmetoder til verdier for attributtet **PayG** (betalingsgruppe) i forespørsler som sendes til regnskapstjenesten. Her er standardtilordningen:

    ```
    1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1
    ```

    Den første komponenten i hvert par representerer en betalingsmetode som er definert for butikken. Den andre komponenten representerer tilsvarende betalingsgruppe som støttes av EFR-regnskapsregistreringstjenesten. Hvis du vil ha mer informasjon om betalingsgrupper som EFR støtter for Tyskland, kan du se [EFR-referansen](https://public.efsta.net/efr/).

    Eksempeltilordningen for betalingsmetoder tilsvarer betalingsmetoder for butikk som er konfigurert i standard demodata.

    | Betalingsmåte | Navn på betalingsmåte |
    |----------------|---------------------|
    | 1              | Kontanter                |
    | 2              | Kontroll               |
    | 3              | Kort                |
    | 4              | Kundekonto    |
    | 5              | Annet               |
    | 6              | Valuta            |
    | 7              | Bilag             |
    | 8              | Gavekort           |
    | 9              | Betalingsmiddel fjern/flyt |
    | 10             | Fordelskort       |
    | 11             | Ikke-lokale sjekker    |

    Derfor må du endre eksempeltilordningen i henhold til betalingsmetodene som er konfigurert i programmet.

- **Inkluder kundedata** – Hvis denne parameteren er aktivert, vil forespørsler til regnskapstjenesten inneholde kundeinformasjon, for eksempel navn og adresser, i tilfeller der en kunde er lagt til i en transaksjon.
- **Tilordning av merverdiavgiftssatser (mva.)** – Tilordningen av mva-prosentverdier som er definert for mva-kodene til verdier av attributtet **TaxG** (mva-gruppe) i forespørsler som sendes til regnskapstjenesten. Her er standardtilordningen:

    ```
    A: 19.00; B: 7.00; C: 10.70; D: 5.50; E: 0.00
    ```

    Den første komponenten i hvert par representerer en mva-gruppe som støttes av EFR-regnskapsregistreringstjenesten. Den andre komponenten representerer den tilsvarende mva-satsen. Hvis du vil ha mer informasjon om mva-grupper som EFR støtter for Tyskland, kan du se [EFR-referansen](https://public.efsta.net/efr/).

- **Mva-gruppe for gavekort og innbetalinger** – Verdien til **TaxG**-attributtet i forespørsler som sendes til regnskapstjenesten, basert på operasjoner som omfatter gavekort eller innbetalinger. Her er standardtilordningen:

    ```
    G
    ```

- **Avgiftsgruppe for mva-fritak** – Verdien til **TaxG**-attributtet i forespørsler som sendes til regnskapstjenesten, basert på operasjoner som er unntatt avgiftsforpliktelser. Her er standardtilordningen:

    ```
    F
    ```

> [!NOTE]
> Avgiftsinnstillinger i standard datatilordning er ansvarlige for samsvarende avgiftsinnstillinger i systemet og avgiftsgruppene i EFR-tjenesten. Avgiftsgrupper kan bare skrives ut på kvitteringer hvis feltet **Kode for utskrift** er angitt på siden **Mva-koder**.

#### <a name="fiscal-connector-settings"></a>Innstillinger for regnskapskobling

Følgende innstillinger er inkludert i konfigurasjonen for regnskapskoblingen som angis som en del av eksempelet på regnskapsintegrering:

- **Endrepunktadresse** – URL-adressen til regnskapsregistreringstjenesten.
- **Tidsavbrudd** – Tiden, i millisekunder, som regnskapskoblingen vil vente på svar fra regnskapsregistreringstjenesten.
- **Vis regnskapsregistreringsmeldinger** – Dette flagget styrer om returer av avgiftsregistreringstjenesten skal vises for operatøren.

### <a name="configure-channel-components"></a>Konfigurere kanalkomponenter

> [!WARNING]
> På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en utvikler-VM i LCS. Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for eksempler på regnskapsintegrering for Tyskland (eldre)](emea-deu-fi-sample-sdk.md).
>
> Støtte for den nye uavhengige emballasje- og utvidelsesmodellen for regnskapsintegreringseksempler planlegges for senere versjoner.

#### <a name="set-up-the-development-environment"></a>Definere utviklingsmiljøet

Følg denne fremgangsmåten for å definere et distribusjonsmiljø slik at du kan teste og utvide eksemplet.

1. Klon eller last ned repositoriet for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions). Velg riktig frigivelsesavdelingsversjon i henhold til SDK/programversjonen. Hvis du vil ha mer informasjon, kan du se [Last ned eksempler og referansepakker i SDK for Retail fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Åpne EFR-løsningen på **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln**, og bygg den.
1. Installer utvidelser for Commerce Runtime:

    1. Finn installasjonsprogrammet for CRT-utvidelsen:

        - **Commerce Scale Unit:** I mappen **Efr\\ScaleUnit\\ScaleUnit.EFR.Installer\\bin\\Debug\\net461** finner du installasjonsprogrammet **scaleUnit.EFR.Installer**.
        - **Lokal CRT Modern POS:** I mappen **Efr\\ModernPOS\\ModernPOS.EFR.Installer\\bin\\Debug\\net461** finner du installeringsprogrammet **ModernPOS.EFR.Installer**.

    1. Start installeringsprogrammet for CRT-utvidelsen fra kommandolinjen:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Lokal CRT på Modern POS:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Installer utvidelser for regnskapskobling:

    Du kan installere utvidelser for regnskapskobling på [maskinvarestasjonen](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) eller i [POS-kassen](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

    1. Installer utvidelser for maskinvarestasjon:

        1. I mappen **Efr\\HardwareStation\\HardwareStation.EFR.Installer\\bin\\Debug\\net461** finner du installeringsprogrammet **HarwareStation.EFR.Installer**.
        1. Start installeringsprogrammet for utvidelsen fra kommandolinjen ved å kjøre følgende kommando.

            ```Console
            HardwareStation.EFR.Installer.exe install --verbosity 0
            ```

    1. Installer POS-utvidelser:

        1. Åpne eksempelløsningen for regnskapskobling for POS i **Dynamics365Commerce.Solutions\\FiscalIntegration\\PosFiscalConnectorSample\\Contoso.PosFiscalConnectorSample.sln**, og bygg den.
        1. Finn installasjonsprogrammet **Contoso.PosFiscalConnectorSample.StoreCommerce.Installer** i mappen **PosFiscalConnectorSample\\StoreCommerce.Installer\\bin\\Debug\\net461**.
        1. Start installeringsprogrammet for utvidelsen fra kommandolinjen ved å kjøre følgende kommando.

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Produksjonsmiljø

Følg fremgangsmåten i [Konfigurer en kompileringskontroll for et regnskapsintegreringseksempel](fiscal-integration-sample-build-pipeline.md) for å generere og frigi skyskalaenheten og selvbetjeningsdistribusjonspakker for eksemplet på regnskapsintegrering. Du finner YAML-filen for **EFR build-pipeline.yml**-malen i **Pipeline\\YAML_Files** i repositoriet for [løsningene for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-extensions"></a>Utforming av utvidelser

Eksemplet på integrering av regnskapsregistreringstjenesten for Tyskland er basert på [regnskapsintegreringsfunksjonaliteten](fiscal-integration-for-retail-channel.md) og er en del av Retail SDK. Eksemplet finnes i **src\\FiscalIntegration\\Efr**-mappen i repositoriet for [løsningen for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (for eksempel [eksemplet i release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) av en regnskapsdokumentleverandør, som er en utvidelse av CRT og en regnskapskobling, som er en utvidelse av Commerce-maskinvarestasjon. Hvis du vil ha mer informasjon om hvordan du bruker Retail SDK, kan du se [Retail SDK-arkitektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en kompileringskontroll for uavhengig emballasje-SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en utvikler-VM i LCS. Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for eksempler på regnskapsintegrering for Tyskland (eldre)](emea-deu-fi-sample-sdk.md). Støtte for den nye uavhengige emballasje- og utvidelsesmodellen for regnskapsintegreringseksempler planlegges for senere versjoner.

### <a name="crt-extension-design"></a>CRT-utvidelsesutforming

Formålet med filtypen som er en regnskapsdokumentleverandør, er å generere servicespesifikke dokumenter og håndtere svar fra regnskapsregistreringstjenesten.

#### <a name="request-handler"></a>Forespørselsbehandler

Det finnes én forespørselsbehandler for dokumentleverandøren, **DocumentProviderEFRFiscalDEU**. Denne behandleren brukes til å generere regnskapsdokumenter for regnskapsregistreringstjenesten. Den arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på koblingsdokumentleverandøren som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler:

- **GetFiscalDocumentDocumentProviderRequest** – Denne forespørselen inneholder informasjon om hvilke dokumenter som skal genereres. Det returnerer et servicespesifikk dokument som skal registreres i regnskapsregistreringstjenesten.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – Denne forespørselen returnerer svaret sammen med utvidede data.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen for regnskapsdokumentleverandør ligger under **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders\\DocumentProviderFiscalEFRSampleGermany.xml** i repositoriet for [løsningene for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er å aktivere innstillinger for dokumentleverandøren som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering.

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

Konfigurasjonsfilen for regnskapskobling ligger under **src\\FiscalIntegration\\Efr\\Configurations\\Connectors\\ConnectorEFRSample.xml** i repositoriet for [løsningene for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er å aktivere innstillinger for regnskapskoblingen som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering.

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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
