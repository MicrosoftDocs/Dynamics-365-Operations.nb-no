---
title: Eksempel på integrering av tjenesten for avgiftsmessig transaksjon for Østerrike
description: Denne artikkelen gir en oversikt over eksemplet på regnskapsintegrering for Østerrike i Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 08/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: f3429df2732d7d1ed6d2f0783a600c2b994c022b
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473884"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Eksempel på integrering av tjenesten for avgiftsmessig transaksjon for Østerrike

[!include [banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over eksemplet på regnskapsintegrering for Østerrike i Microsoft Dynamics 365 Commerce.

For å oppfylle lokale regnskapskravene for kasser i Østerrike inneholder Dynamics 365 Retail-funksjonaliteten for Østerrike et eksempel på integrering av salgsstedet med en ekstern regnskapsregistreringstjeneste. Eksemplet utvider [funksjonaliteten for regnskapsintegrering](fiscal-integration-for-retail-channel.md). Den er basert på løsningen [EFR (Electronic Fiscal Register)](https://www.efsta.eu/at/fiskalloesungen/oesterreich) fra [EFSTA](https://www.efsta.eu/at/), og gjør det mulig å kommunisere med EFR-tjenesten via HTTPS-protokollen. EFR-tjenesten bør være vertsbasert enten på detaljhandelsmaskinvarestasjonen eller på en separat maskin som kan kobles til fra maskinvarestasjonen. Eksemplet leveres i form av kildekode og er en del av Commerce Software Development Kit (SDK).

Microsoft frigir ikke maskinvare, programvare eller dokumentasjon fra EFSTA. Hvis du vil ha mer informasjon om hvordan du får EFR-løsningen og bruker den, kan du kontakte [EFSTA](https://www.efsta.eu/at/kontakt).

## <a name="scenarios"></a>Scenarier

Følgende scenarioer dekkes av eksemplet på integrering av regnskapsregistreringstjenesten for Østerrike:

- Registrering av kontanttransaksjoner i regnskapsregistreringstjenesten:

    - Send detaljerte transaksjonsdata til regnskapsregistreringstjenesten. Disse dataene omfatter salgslinjeinformasjon og informasjon om rabatter, betalinger og avgifter.
    - Henting av svar fra regnskapsregistreringstjenesten. Dette svaret omfatter en digital signatur og en kobling til den registrerte transaksjonen.
    - Registrer avgifter og tilordne dem til avgiftskodene for regnskapsregistreringstjenesten.
    - Skriv ut QR-koden for en registrert transaksjon på mottaket.

- Registrering av gavekortoperasjoner og kundeinnskudd som ikke-kontanttransaksjoner i regnskapsregistreringstjenesten:

    - Utsted eller legg til penger på et gavekort.
    - Registrer en innbetaling til kundekonto.
    - Registrer en innbetaling til kundeordre.

- Registrering av ikke-salgstransaksjoner og hendelser som ikke-kontanttransaksjoner i regnskapsregistreringstjenesten:

    - Åpne skift og Lukk skift
    - Startbeløp, flytoppføring og fjerning av betalingsmiddel
    - Prisoverstyring
    - Avgiftsoverstyring
    - Skriv ut kopi av kvittering
    - Åpne skuff
    - Skriv ut X-rapport
    - Skriv ut Z-rapport

- Skriv ut dagsoppgjør (X/Z-rapporter) som har spesifikke felter for Østerrike:

    - Totalt antall produkter eller tjenester som ble levert til kunder
    - Nedbryting av salg etter avgiftssats
    - Nedbryting av betalinger etter kasserer/kasseoperatør
    - Prisrabatter og returer som reduserer daglig salg
    - Nullsalg (gaver)

- Feilhåndtering, for eksempel følgende alternativer:

    - Prøv regnskapsregistrering på nytt hvis det er mulig å gjøre et nytt forsøk, for eksempel hvis regnskapsregistreringstjenesten ikke er tilgjengelig, ikke er klar eller ikke svarer.
    - Utsett regnskapsregistrering.
    - Hopp over regnskapsregistrering eller merk transaksjonen som registrert, og inkluder informasjonskoder for å registrere årsaken til feilen og tilleggsinformasjon.
    - Kontroller tilgjengeligheten av regnskapsregistreringstjenesten før en ny salgstransaksjon åpnes eller en salgstransaksjon fullføres.

### <a name="gift-cards"></a>Gavekort

Eksemplet på integrering av regnskapsregistreringstjenesten implementerer følgende regler som er relatert til gavekort:

- Utelukk salgslinjer som er relatert til *utsendelsesgavekortet*, og *Legg til gavekort*-operasjoner fra en kontanttransaksjon. I stedet for å registrere disse linjene som en del av en kontanttransaksjon, kan du registrere dem som en separat ikke-kontanttransaksjon i regnskapsregistreringstjenesten.
- Ikke skriv ut en nedbryting på avgiftsgrupper og en QR-kode på en kvittering hvis kvitteringen bare består av gavekortlinjer.
- Skriv ut totalt antall gavekort som er utstedt eller belastet på nytt i en transaksjon separat fra kontanttransaksjonsbeløpet på kvitteringen.
- Lagre beregnede justeringer av betalingslinjer i kanaldatabasen med en referanse til en tilsvarende regnskapstransaksjon.
- Betaling med gavekort regnes som en vanlig betaling.

### <a name="customer-deposits-and-customer-order-deposits"></a>Kundeinnbetalinger og kundeordreinnbetalinger

Eksemplet på integrering av regnskapsregistreringstjenesten implementerer følgende regler som er relatert til kundeinnbetaling og kundeordreinnbetaling:

- Registrer en ikke-kontanttransaksjon hvis en transaksjon er en kundeinnbetaling.
- Registrer en ikke-kontanttransaksjon hvis en transaksjon bare inneholder et innbetalingsbeløp for kundeordre eller en innbetalingsrefusjon for kundeordre.
- Trekk fra innbetalingsbeløpet for kundeordren fra betalingslinjen når det opprettes en hybridkundeordre.
- Lagre beregnede justeringer av betalingslinjer i kanaldatabasen med en referanse til en regnskapstransaksjon for en hybridkundeordre.

### <a name="limitations-of-the-sample"></a>Begrensninger i eksemplet

Regnskapsregistreringstjenesten støtter bare scenarioer der merverdiavgift er inkludert i prisen. Derfor må alternativet **Pris inkludert merverdiavgift** settes til **Ja** for både butikker og kunder.

## <a name="set-up-commerce-for-austria"></a>Definere Commerce for Østerrike

Denne delen beskriver innstillingene for Commerce som er spesifikke og anbefalte for Østerrike. Hvis du vil ha mer informasjon om oppsettet, kan du se [Commerce-startsiden](../index.md).

Hvis du vil bruke den spesifikke funksjonen for Østerrike, må du angi følgende innstillinger:

- I primæradressen for den juridiske enheten setter du feltet **Land/område** til **AUT** (Østerrike).
- Sett feltet **ISO-kode** til **AT** (Østerrike) i salgsstedsfunksjonalitetsprofilen for hver butikk som finnes i Østerrike.

Du må også angi følgende innstillinger for Østerrike. Merk at du må kjøre riktige distribusjonsjobber når du har fullført oppsettet.

### <a name="enable-features-for-austria"></a>Aktiver funksjonene for Østerrike

Du må aktivere følgende funksjoner i arbeidsområdet **Funksjonsstyring**:

- (Østerrike) Aktiver flere revisjonshendelser på salgssted
- (Østerrike) Aktiver tilleggsinformasjon i dagsoppgjør på salgssted

### <a name="set-up-vat-per-austrian-requirements"></a>Definere merverdiavgift i henhold til østerrikske krav

Du må opprette mva-koder, mva-grupper og mva-grupper for varer. Du må også definere mva-informasjon for produkter og tjenester. Hvis du vil ha mer informasjon om hvordan du definerer og bruker mva-funksjoner, kan du se [Oversikt over merverdiavgift](../../finance/general-ledger/indirect-taxes-overview.md).

På salgskvitteringer kan du skrive ut en forkortet kode for en mva-kode (for eksempel A eller B). Hvis du vil gjøre denne funksjonaliteten tilgjengelig, angir du **Utskriftskode**-feltet på siden **Mva-koder**.

### <a name="set-up-stores"></a>Konfigurer butikker

Oppdater butikkdetaljene på **Alle butikker**-siden. Du må angi følgende parametere:

- I feltet **Mva-gruppe** angir du mva-gruppen som skal brukes for salg til standardkunden.
- Sett alternativet **Priser inkluderer mva.** til **Ja**.
- Sett **Navn**-feltet til firmanavnet. Denne endringen bidrar til å garantere at firmanavnet vises på en salgskvittering. Du kan også legge til firmanavnet i salgskvitteringsoppsettet som frihåndstekst.
- Sett feltet **TIN (Tax Identification Number)** til firmaidentifikasjonsnummeret. Denne endringen bidrar til å garantere at firmaets identifikasjonsnummer vises på en salgskvittering. Du kan også legge til firmaets identifikasjonsnummer i salgskvitteringsoppsettet som frihåndstekst.

### <a name="set-up-functionality-profiles"></a>Konfigurere funksjonalitetsprofiler

Konfigurer salgsstedsfunksjonalitetsprofiler:

- I hurtigfanen **Kvitteringsnummerering** kan du definere kvitteringsnummerering ved å opprette eller oppdatere poster for transaksjonstypene **Salg**, **Salgsordre** og **Retur**.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurere egendefinerte felt, slik at de kan brukes i kvitteringsformater for salgskvitteringer

Du kan konfigurere språkteksten og de egendefinerte feltene som skal brukes i salgsstedskvitteringsformatene. Standardfirmaet til brukeren som oppretter kvitteringsoppsettet, må være den samme juridiske enheten der språktekstoppsettet opprettes. Du kan også opprette de samme språktekstene i både brukerens standardfirma og den juridiske enheten i butikken som oppsettet er opprettet for.

På siden **Språktekst** legger du til følgende poster for etikettene for de egendefinerte feltene for kvitteringsoppsett. Vær oppmerksom på at verdiene **Språk-ID**, **Tekst-ID** og **Tekst** som vises i tabellen, bare er eksempler. Du kan endre dem slik at de oppfyller dine krav. Verdiene for **Tekst-ID** som du bruker, må imidlertid være unike, og de må være lik eller mer enn 900001.

Legg til følgende salgsstedsetiketter i **Salgssted**-delen i **Språktekst** fra tabellen:

| Språk-ID | Tekst-ID | Tekst                      |
|-------------|---------|---------------------------|
| en-US       | 900001  | QR-kode                   |
| en-US       | 900002  | Fortløpende nummer         |
| en-US       | 900003  | Utskriftskode for detaljhandelsavgift     |
| en-US       | 900004  | Totalt (salg)             |
| en-US       | 900005  | Total avgift (salg)         |
| en-US       | 900006  | Sum inkludert avgift (salg) |
| en-US       | 900007  | Avgiftsbeløp (salg)        |
| en-US       | 900008  | Avgiftsgrunnlag (salg)         |

På siden **Egendefinerte felt** legger du til følgende poster for de egendefinerte feltene for oppsett av mottaket. Vær oppmerksom på at verdiene **Tekst-ID for overskrift** må samsvare med verdiene **Tekst-ID** som du har angitt på siden **Språktekst**:

| Navn                 | Type    | Tekst-ID for overskrift |
|----------------------|---------|-----------------|
| QRCODE               | Tilgang | 900001          |
| CONTINUOUSNUMBER     | Tilgang | 900002          |
| RETAILPRINTCODE      | Tilgang | 900003          |
| SALESTOTAL           | Tilgang | 900004          |
| SALESTOTALTAX        | Tilgang | 900005          |
| SALESTOTALINCLUDETAX | Tilgang | 900006          |
| SALESTAXAMOUNT       | Tilgang | 900007          |
| SALESTAXBASIS        | Tilgang | 900008          |

> [!NOTE]
> Det er viktig at du angir riktige egendefinerte feltnavn, som vist i foregående tabell. Et feil egendefinert feltnavn vil forårsake manglende data i kvitteringer.

### <a name="configure-receipt-formats"></a>Konfigurere mottaksformater

For hvert nødvendig kvitteringsformat endrer du verdien for feltet **Utskriftsatferd** til **Skriv alltid ut**.

I Utforming av kvitteringsformat legger du til de egendefinerte feltene nedenfor i de aktuelle kvitteringsdelene. Vær oppmerksom på at feltnavnene samsvarer med språktekstene som du definerte i forrige del.

- **Topptekst:** Legg til følgende felter:

    - Feltene **Butikknavn** og **Avgiftsidentifikasjonsnummer**, som brukes til å skrive ut firmanavnet og identitetsnummeret på kvitteringer. Du kan også legge til firmanavnet og identitetsnummeret i salgskvitteringsoppsettet som frihåndstekst.
    - **Butikkadresse**, **Dato**, **Klokkeslett 24H**, **Kvitteringsnummer** og **Registreringsnummer**.
    - **Fortløpende nummer**-feltene for å identifisere nummeret til kontanttransaksjonen i regnskapsregistreringstjenesten.

- **Linjer:** Legg til følgende felter:

    - **Varenavn**.
    - **Antall**.
    - **Totalpris med avgift**.
    - **Mva-kode for detaljhandelsutskrift**, som brukes til å skrive ut den forkortede koden som tilsvarer mva-koden som gjelder for varen.

- **Bunntekst:** Legg til følgende felter:

    - Betalingsfelter, slik at betalingsbeløpene for hver betalingsmåte skrives ut. Du kan for eksempel legge til feltene **Betalingsmiddel** og **Betalingsmiddelbeløp** i én linje i oppsettet.
    - **Salgstotal**-feltgruppe:

        - Feltet **Totalt (salg)**, som brukes til å skrive ut kvitteringens totale beløp for kontantsalg. Beløpet uten mva. Forskuddsbetalinger og gavekort utelates.
        - Feltet **Sum inkludert avgift (salg)**, som brukes til å skrive ut kvitteringens totale beløp for kontantsalg. Beløpet med mva. Forskuddsbetalinger og gavekort utelates.
        - Feltet **Sum inkludert avgift (salg)**, som brukes til å skrive ut kvitteringens totale avgiftsbeløp for kontantsalg. Forskuddsbetalinger og gavekort utelates.

    - **Nedbrytning av avgift**-feltgruppe. Alle feltene i denne feltgruppen må skrives ut på én egen linje.

        - Feltet **Avgifts-ID**, som er et standardfelt som gjør det mulig å skrive ut et mva-sammendrag for hver mva-kode. Feltet må legges til i en ny linje.
        - Feltet **Mva-prosent**, som er et standardfelt som brukes til å skrive ut den effektive mva-satsen for mva-koden.
        - Feltet **Avgiftsgrunnlag (salg)**, som brukes til å skrive ut kvitteringens totale kontantsalgsbeløp for mva-koden. Forskuddsbetalinger og gavekort utelates.
        - Feltet **Avgiftsbeløp (salg)**, som brukes til å skrive ut kvitteringens avgiftsbeløp for kontantsalg for mva-koden.
        - Feltet **Mva-kode for detaljhandelsutskrift**, som brukes til å skrive ut den forkortede koden som tilsvarer mva-koden.

    - Feltet **QR-kode**, som brukes til å skrive ut referansen til den registrerte kontanttransaksjonen i form av QR-kode.

        > [!NOTE]
        > Verdien **QR-kode** hentes fra svaret på regnskapsregisteret. EFR returnerer bare en QR-kode i sitt svar hvis verdien i **Attributter**-feltet i EFR-konfigurasjonen er beskrevet i EFSTA-dokumentasjonen. QR-kodeformatet i **Attributter**-feltet i EFR-konfigurasjonen må være satt til **BMP**.

Hvis du vil ha mer informasjon om hvordan du arbeider med kvitteringsformater, kan du se [Definere og utforme kvitteringsformater](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-austria"></a>Definere regnskapsintegrering for Østerrike

Eksemplet på integrering av regnskapsregistreringstjenesten for Østerrike er basert på [regnskapsintegreringsfunksjonaliteten](fiscal-integration-for-retail-channel.md) og er en del av Commerce SDK. Eksemplet ligger i mappen **src\\FiscalIntegration\\Efr** i repositoriet [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). [Eksemplet](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) består av en regnskapsdokumentleverandør, som er en utvidelse av Commerce Runtime (CRT) og en regnskapskobling, som er en utvidelse av Commerce-maskinvarestasjon. Hvis du vil ha mer informasjon om hvordan du bruker Commerce SDK, kan du se [Last ned Commerce SDK-eksempler og referansepakker fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md) og [Definer kompileringskontroll for SDK for uavhengig pakking](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Eksemplet på integrering av regnskapsregistreringstjenesten for Østerrike er tilgjengelig i Commerce SDK fra og med Commerce-versjon 10.0.29. I Commerce-versjon 10.0.28 eller tidligere må du bruke den forrige versjonen av Retail SDK på en virtuell utviklermaskin (VM) i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for eksempler på regnskapsintegrering for Østerrike (eldre)](emea-aut-fi-sample-sdk.md).

Fullfør fremgangsmåten for oppsett av regnskapsintegrering slik det beskrives i [Oppsett av regnskapsintegrering for Commerce-kanaler](setting-up-fiscal-integration-for-retail-channel.md):

1. [Definer en regnskapsregistreringsprosess](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Noter deg også innstillingene for regnskapsregistreringsprosessen som er [spesifikke for dette eksemplet med integrering av regnskapsregistreringstjenesten](#set-up-the-registration-process).
1. [Angi innstillinger for feilbehandling](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Aktiver manuell kjøring av utsatt bilagsregistrering](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurere kanalkomponenter](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Definere registreringsprosessen

Hvis du vil aktivere registreringsprosessen, følger du denne fremgangsmåten for konfigurere Commerce Headquarters. Hvis du vil ha mer informasjon om regnskapsintegrering, kan du se [Definere økonomisk integrering for handelskanaler](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Last ned konfigurasjonsfiler for regnskapsdokumentleverandøren og regnskapskoblingen:

    1. Open respositoriet for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Velg riktig frigivelsesavdelingsversjon i henhold til SDK/programversjonen.
    1. Åpne **src \> FiscalIntegration \> Efr**.
    1. Åpne **Konfigurasjoner \> DocumentProviders**, og last ned konfigurasjonsfiler for regnskapsdokumentleverandøren: 

        - DocumentProviderFiscalEFRSampleAustria.xml
        - DocumentProviderNonFiscalEFRSampleAustria.xml

    1. Last ned konfigurasjonsfilen for regnskapskoblingen under **Konfigurasjoner \> Koblinger \> ConnectorEFRSample.xml**.

    > [!NOTE]
    > I Commerce-versjon 10.0.28 eller tidligere må du bruke den forrige versjonen av Retail SDK på en utvikler-VM i LCS. Konfigurasjonsfilene for dette regnskapsintegreringseksemplet ligger i følgende mapper for Retail SDK på en utvikler-VM i LCS:
    >
    > - **Konfigurasjonsfiler for regnskapsdokumentleverandør:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Konfigurasjon
    > - **Konfigurasjonsfil for regnskapskobling:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Konfigurasjon

1. Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> Delte handelsparametere**. På **Generelt**-fanen angir du **Aktiver regnskapsintegrering**-alternativet til **Ja**.
1. Gå til **Retail og Commerce \> Kanaloppsett \> Regnskapsintegrering \> Leverandører for regnskapsdokument**, og last inn konfigurasjonsfiler for regnskapsdokumentleverandør som du lastet ned tidligere.
1. Gå til **Retail og Commerce \> Kanaloppsett \> Regnskapsintegrering \> Regnskapskoblinger**, og last inn konfigurasjonsfilen for regnskapskobling som du lastet ned tidligere.
1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Regnskapsintegrering \> Funksjonsprofiler for kobling**. Opprett to nye koblingsfunksjonsprofiler, én for hver regnskapsdokumentleverandør som du lastet inn tidligere, og velg regnskapskoblingen du lastet inn tidligere. Oppdater [innstillingene for datatilordning](#default-data-mapping) etter behov.
1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Regnskapsintegrering \> Tekniske profiler for kobling**. Opprett en ny teknisk profil for kobling, og velg regnskapskoblingen du lastet inn tidligere. Oppdater [koblingsinnstillingene](#fiscal-connector-settings) etter behov.
1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Regnskapsintegrering \> Grupper for regnskapskobling**. Opprett to nye regnskapskoblingsgrupper, én for hver koblingsfunksjonsprofil som du opprettet tidligere.
1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Regnskapsintegrering \> Regnskapsregistreringsprosesser**. Opprett en ny regnskapsregistreringsprosess og to trinn i regnskapsregistreringsprosessen, og velg regnskapskoblingsgruppene du opprettet tidligere.
1. Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Funksjonalitetsprofiler**. Velg en funksjonsprofil som er koblet til butikken der registreringsprosessen skal aktiveres. I hurtigfanen **Regnskapsregistreringsprosess** velger du regnskapsregistreringsprosessen du opprettet tidligere. Hvis du vil aktivere registrering av ikke-regnskapshendelser på salgsstedet, setter du **Revisjon**-alternativet til **Ja** på hurtigfanen **Funksjoner** under **Salgssted**.
1. Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Maskinvareprofiler**. Velg en maskinvareprofil som er koblet til maskinvarestasjonen som regnskapsregistreringstjenesten skal kobles til. I hurtigganen **Eksterne regnskapsenheter** velger du den tekniske profilen for koblingen som du opprettet tidligere.
1. Åpne distribusjonsplanen (**Retail og Commerce \> IT for detaljhandel og handel \> Distribusjonsplan**), og velg jobbene **1070** og **1090** for å overføre data til kanaldatabasen.

#### <a name="default-data-mapping"></a>Standard datatilordning

Følgende standard datatilordning er inkludert i konfigurasjonen for regnskapsdokumentleverandøren som angis som en del av eksempelet på regnskapsintegrering:

- **Tilordning av merverdiavgiftssatser (mva.)** – Tilordningen av mva-prosentverdier som er definert for mva-kodene til verdier av attributtet **TaxG** (mva-gruppe) i forespørsler som sendes til regnskapstjenesten. Her er standardtilordningen:

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    Den første komponenten i hvert par representerer en mva-gruppe som støttes av EFR-regnskapsregistreringstjenesten. Den andre komponenten representerer den tilsvarende mva-satsen. Hvis du vil ha mer informasjon om mva-grupper som EFR støtter for Østerrike, kan du se [EFR-referansen](https://public.efsta.net/efr/).

#### <a name="fiscal-connector-settings"></a>Innstillinger for regnskapskobling

Følgende innstillinger er inkludert i konfigurasjonen for regnskapskoblingen som angis som en del av eksempelet på regnskapsintegrering:

- **Endrepunktadresse** – URL-adressen til regnskapsregistreringstjenesten.
- **Tidsavbrudd for enhet** – Tiden, i millisekunder, som regnskapskoblingen vil vente på svar fra regnskapsregistreringstjenesten.
- **Vis regnskapsregistreringsmeldinger** – Dette flagget styrer om returer av avgiftsregistreringstjenesten skal vises for operatøren.

### <a name="configure-channel-components"></a>Konfigurere kanalkomponenter

> [!NOTE]
> - Eksemplet på integrering av regnskapsregistreringstjenesten for Østerrike er tilgjengelig i Commerce SDK fra og med Commerce-versjon 10.0.29. I Commerce-versjon 10.0.28 eller tidligere må du bruke den forrige versjonen av Retail SDK på en utvikler-VM i LCS. Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for eksempler på regnskapsintegrering for Østerrike (eldre)](emea-aut-fi-sample-sdk.md).
> - Commerce-eksempler som distribueres i miljøet ditt, oppdateres ikke automatisk når du bruker tjeneste- eller kvalitetsoppdateringer for Commerce-komponenter. Du må manuelt oppdatere de obligatoriske eksemplene.

#### <a name="set-up-the-development-environment"></a>Definere utviklingsmiljøet

Følg denne fremgangsmåten for å definere et distribusjonsmiljø slik at du kan teste og utvide eksemplet.

1. Klon eller last ned repositoriet for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions). Velg riktig frigivelsesavdelingsversjon i henhold til SDK/programversjonen. Hvis du vil ha mer informasjon, kan du se [Last ned eksempler og referansepakker i SDK for Commerce fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Åpne EFR-løsningen på **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln**, og bygg den.
1. Installer CRT-utvidelser:

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

## <a name="design-of-extensions"></a>Utforming utvidelser

Eksemplet på integrering av regnskapsregistreringstjenesten for Østerrike er basert på [regnskapsintegreringsfunksjonaliteten](fiscal-integration-for-retail-channel.md) og er en del av Commerce SDK. Eksemplet ligger i mappen **src\\FiscalIntegration\\Efr** i repositoriet [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) av en regnskapsdokumentleverandør, som er en utvidelse av CRT og en regnskapskobling, som er en utvidelse av Commerce-maskinvarestasjon. Hvis du vil ha mer informasjon om hvordan du bruker Commerce SDK, kan du se [Last ned Commerce SDK-eksempler og referansepakker fra GitHub og NuGet](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Definer kompileringskontroll for SDK for uavhengig pakking](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Eksemplet på integrering av regnskapsregistreringstjenesten for Østerrike er tilgjengelig i Commerce SDK fra og med Commerce-versjon 10.0.29. I Commerce-versjon 10.0.28 eller tidligere må du bruke den forrige versjonen av Retail SDK på en utvikler-VM i LCS. Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for eksempler på regnskapsintegrering for Østerrike (eldre)](emea-aut-fi-sample-sdk.md).

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime-utvidelsesutforming 

Formålet med filtypen som er en regnskapsdokumentleverandør, er å generere servicespesifikke dokumenter og håndtere svar fra regnskapsregistreringstjenesten.

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

Konfigurasjonsfilene for regnskapsdokumentleverandøren ligger i mappen **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders** i respositoriet for [løsningene for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/):

- **DocumentProviderFiscalEFRSampleAustria** – Konfigurasjonsfilen for regnskapsdokumentleverandøren for regnskapsdokumenter.
- **DocumentProviderNonFiscalEFRSampleAustria** – Konfigurasjonsfilen for regnskapsdokumentleverandøren for ikke-regnskapsdokumenter.

Formålet med disse filene er å aktivere innstillinger for dokumentleverandøren som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering.

### <a name="hardware-station-extension-design"></a>Utvidelsesutforming for maskinvarestasjon

Formålet med regnskapskoblingsutvidelsen er å kommunisere med regnskapsregistreringstjenesten. Utvidelsen for maskinvarestasjon bruker protokollene HTTP og HTTPS til å sende dokumenter som CRT-utvidelsen genererer til regnskapsregistreringstjenesten. Den håndterer også svarene som mottas fra regnskapsregistreringstjenesten.

#### <a name="request-handler"></a>Forespørselsbehandler

Forespørselsbehandleren **EFRHandler** er startpunktet for behandling av forespørsler til regnskapsregistreringstjenesten.

Behandleren arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på regnskapskoblingen som er angitt i Commerce Headquarters.

Regnskapskoblingen støtter følgende forespørsler:

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
