---
title: Eksempel på integrering av regnskapsregistreringstjenesten for Tsjekkia
description: Denne artikkelen gir en oversikt over eksemplet for regnskapsintegrering for Tsjekkia i Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-4-1
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: d255b03242a4cb7a72cef1e8e6fab901ecf953e6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910504"
---
# <a name="fiscal-registration-service-integration-sample-for-the-czech-republic"></a>Eksempel på integrering av regnskapsregistreringstjenesten for Tsjekkia

[!include[banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over eksemplet for regnskapsintegrering for Tsjekkia i Microsoft Dynamics 365 Commerce.

For å oppfylle lokale regnskapskravene for kasser i Tsjekkia inneholder Dynamics 365 Commerce-funksjonaliteten for Tsjekkia et eksempel på salgsstedsintegrering med en ekstern regnskapsregistreringstjeneste. Eksemplet utvider [funksjonaliteten for regnskapsintegrering](fiscal-integration-for-retail-channel.md). Den er basert på løsningen [EFR (Electronic Fiscal Register)](https://efsta.org/sicherheitsloesungen/) fra [EFSTA](https://efsta.org/), og gjør det mulig å kommunisere med EFR-tjenesten via HTTPS-protokollen. EFR-tjenesten sørger for elektronisk registrering av salg (EET – Elektronická evidence tržeb) det vil si den elektroniske overføringen av salgsdataene til skattemyndighetenes nettjeneste.

EFR-tjenesten bør være vertsbasert enten på Commerce-maskinstasjonen eller på en separat maskin som kan kobles til fra maskinvarestasjonen. Eksemplet leveres i form av kildekode og er en del av Retail Software Development Kit (SDK).

Microsoft frigir ikke maskinvare, programvare eller dokumentasjon fra EFSTA. Hvis du vil ha mer informasjon om hvordan du får EFR-løsningen og bruker den, kan du kontakte [EFSTA](https://efsta.org/kontakt/).

## <a name="scenarios"></a>Scenarier

Følgende scenarioer dekkes av eksemplet på integrering av regnskapsregistreringstjenesten for Tsjekkia:

- Registrering av kontanttransaksjoner i regnskapsregistreringstjenesten.

    - Send detaljerte transaksjonsdata til regnskapsregistreringstjenesten. Disse dataene omfatter salgslinjeinformasjon og informasjon om rabatter, betalinger og avgifter. Regnskapsregistreringstjenesten sender ytterligere dataene til skattemyndighetenes nettjeneste, og mottar en bekreftelse fra den som inkluderer regnskapsidentifikasjonskoden for transaksjonen.
    - Henting av svar fra regnskapsregistreringstjenesten. Dette svaret inneholder regnskapsdata som regnskapsidentifikasjonskoden og sikkerhetskoden for transaksjonen osv.
    - Skriv ut regnskapsdata for en registrert transaksjon på mottaket.

- Registrering av gavekortoperasjoner og kundeinnskudd i regnskapsregistreringstjenesten.

    - Utsted eller legg til penger på et gavekort.
    - Registrer en innbetaling til kundekonto.
    - Opprett en kundeordre, og registrer en innbetaling for ordren.
    - Rediger en kundeordre, og overstyr innbetalingen for ordren.
    - Avbryt en kundeordre, og refunder innbetalingen for ordren.

- Feilhåndtering, for eksempel følgende alternativer.

    - Prøv regnskapsregistrering på nytt hvis det er mulig å gjøre et nytt forsøk, for eksempel hvis regnskapsregistreringstjenesten ikke er tilgjengelig, ikke er klar eller ikke svarer.
    - Utsett regnskapsregistrering.
    - Hopp over regnskapsregistrering eller merk transaksjonen som registrert, og inkluder informasjonskoder for å registrere årsaken til feilen og tilleggsinformasjon.
    - Kontroller tilgjengeligheten av regnskapsregistreringstjenesten før en ny salgstransaksjon åpnes eller en salgstransaksjon fullføres.

### <a name="gift-cards"></a>Gavekort

Eksemplet på integrering av regnskapsregistreringstjenesten implementerer følgende regler som er relatert til gavekort.

- Salgslinjer som er knyttet til handlingene *Utsted gavekort* eller *Legg til gavekort* i en salgstransaksjon, merkes med et spesielt attributt når transaksjonen registreres i regnskapsregistreringstjenesten.
- En betaling med gavekort regnes som en vanlig betaling, og merkes med et spesielt attributt når transaksjonen registreres i regnskapsregistreringstjenesten.

### <a name="customer-account-deposits-and-customer-order-deposits"></a>Innbetalinger på kundekonto og kundeordreinnbetalinger

Eksemplet på integrering av regnskapsregistreringstjenesten implementerer følgende regler som er relatert til kundekontoinnbetaling og kundeordreinnbetaling.

- En transaksjon som er relatert til en kundekontoinnbetaling eller en kundeordreinnbetaling, registreres i regnskapsregistreringstjenesten som en enkeltlinjetransaksjon og merkes med et spesielt attributt. Mva-gruppen for innbetaling er angitt i denne linjen.
- Når det opprettes en hybridkundeordre, det vil si en kundeordre som inneholder produkter som kan utføres av butikken av kunden, i tillegg til produkter som skal plukkes eller sendes senere, inneholder transaksjonen som er registrert i regnskapsregistreringstjenesten, linjer for produktene som utføres, i tillegg til en linje for ordreinnbetalingen.
- En betaling fra en kundekonto regnes som en vanlig betaling, og merkes med et spesielt attributt når transaksjonen registreres i regnskapsregistreringstjenesten.
- Innbetalingsbeløpet for kundeordre som brukes på en plukkoperasjon for kundeordre, regnes som en vanlig betaling, og merkes med et spesielt attributt når transaksjonen registreres i regnskapsregistreringstjenesten.

### <a name="offline-registration"></a>Frakoblet registrering

Hvis avgiftsregistreringstjenesten ikke overfører transaksjonsdata til skattemyndighetenes regnskapsnettjeneste (for eksempel på grunn av tidsavbruddet), og det mottas en bekreftelse fra nettjenesten (det vil si regnskapsidentifikasjonskoden til transaksjonen), genererer den en lokal signatur for transaksjonen, og inkluderer den og en spesiell feilkode i svaret. Regnskapsregistreringstjenesten sender transaksjoner på nytt i opprinnelig rekkefølge i bakgrunnen så snart nettverkstilkoblingen er gjenopprettet.

### <a name="limitations-of-the-sample"></a>Begrensninger i eksemplet

Regnskapsregistreringstjenesten støtter bare scenarioer der merverdiavgift er inkludert i prisen. Derfor må alternativet **Pris inkludert merverdiavgift** settes til **Ja** for både butikker og kunder.

## <a name="set-up-commerce-for-the-czech-republic"></a>Konfigurer Commerce for Tsjekkia

Denne delen beskriver innstillingene for Commerce som er spesifikke og anbefalte for Tsjekkia. Hvis du vil ha mer informasjon, kan du se [Startside for Commerce](../index.md).

Hvis du vil bruke den spesifikke funksjonen for Tsjekkia, må du angi følgende innstillinger.

- I primæradressen for den juridiske enheten setter du feltet **Land/område** til **CZE** (Tsjekkia).
- I salgsstedsfunksjonalitetsprofilen for hver butikk som ligger i Tsjekkia, setter du feltet **ISO-kode** til **CZ** (Tsjekkia).

Du må også angi følgende innstillinger for Tsjekkia. Merk at du må kjøre riktige distribusjonsjobber når du har fullført oppsettet.

### <a name="set-up-vat-per-czech-republic-requirements"></a>Definer merverdiavgift i henhold til kravene for Tsjekkia


Du må opprette mva-koder, mva-grupper og mva-grupper for varer. Du må også definere mva-informasjon for produkter og tjenester. Hvis du vil ha mer informasjon om hvordan du definerer og bruker mva-funksjoner, kan du se [Oversikt over merverdiavgift](../../finance/general-ledger/indirect-taxes-overview.md).

### <a name="set-up-stores"></a>Konfigurer butikker

Oppdater butikkdetaljene på **Alle butikker**-siden. Du må angi følgende parametere.

- I feltet **Mva-gruppe** angir du mva-gruppen som skal brukes for salg til standardkunden.
- Sett alternativet **Priser inkluderer mva.** til **Ja**.
- Sett **Navn**-feltet til firmanavnet. Denne endringen bidrar til å garantere at firmanavnet vises på en salgskvittering. Du kan også legge til firmanavnet i salgskvitteringsoppsettet som frihåndstekst.
- Sett feltet **TIN (Tax Identification Number)** til firmaidentifikasjonsnummeret. Denne endringen bidrar til å garantere at firmaets identifikasjonsnummer vises på en salgskvittering. Du kan også legge til firmaets identifikasjonsnummer i salgskvitteringsoppsettet som frihåndstekst.

### <a name="set-up-functionality-profiles"></a>Konfigurere funksjonalitetsprofiler

Konfigurer salgsstedsfunksjonalitetsprofiler.

- I hurtigfanen **Kvitteringsnummerering** kan du definere kvitteringsnummerering ved å opprette eller oppdatere poster for transaksjonstypene **Salg**, **Salgsordre** og **Retur**.

### <a name="set-up-registration-numbers"></a>Definer registreringsnumre

1. Gå til **Organisasjonsstyring \> Global adressebok \> Registreringstyper \> Registreringstyper**. Opprett en ny registreringstype. Angi feltet **Land/område** til **CZE** (Tsjekkia), og gjør det begrenset til organisasjon.
2. Gå til **Organisasjonsstyring \> Global adressebok \> Registreringstyper \> Registreringskategorier**. Opprett en ny registreringskategori. Velg registreringstypen fra forrige trinn, og angi **Registreringskategori** til **ID for forretningslokale**.
3. Gå til **Organisasjonsstyring \> Organisasjoner \> Driftsenheter**. For hver butikk som finnes i Tsjekkia, velger du enheten som er knyttet til butikken. Utvid **Flere alternativer**-rullegardinlisten på i hurtigfanen **Adresse**, og velg deretter **Avansert**. 
4. På den åpne **Administrer adresser**-siden må du angi følgende innstilling.

    - I hurtigfanen **Adresse** setter du feltet **Land/område** til **CZE**.
    - Opprett et nytt passord på hurtigfanen **Registrerings-ID**. Velg registreringstypen opprettet tidligere, og angi registreringsnummeret.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurere egendefinerte felt, slik at de kan brukes i kvitteringsformater for salgskvitteringer

Du kan konfigurere språkteksten og de egendefinerte feltene som skal brukes i salgsstedskvitteringsformatene. Standardfirmaet til brukeren som oppretter kvitteringsoppsettet, må være den samme juridiske enheten der språktekstoppsettet opprettes. Du kan også opprette de samme språktekstene i både brukerens standardfirma og den juridiske enheten i butikken som oppsettet er opprettet for.

På siden **Språktekst** legger du til følgende poster for etikettene for de egendefinerte feltene for kvitteringsoppsett. Vær oppmerksom på at verdiene **Språk-ID**, **Tekst-ID** og **Tekst** som vises i tabellen, bare er eksempler. Du kan endre dem slik at de oppfyller dine krav. Verdiene for **Tekst-ID** som du bruker, må imidlertid være unike, og de må være lik eller mer enn 900001.

Legg til følgende salgsstedsetiketter i **Salgssted**-delen i **Språktekst** fra tabellen:

| Språk-ID | Tekst-ID | Tekst                   |
|-------------|---------|------------------------|
| en-US       | 900001  | ID provozovny/pokladny |
| en-US       | 900002  | BKP                    |
| en-US       | 900003  | PKP                    |
| en-US       | 900004  | FIK                    |
| en-US       | 900005  | Info                   |
| en-US       | 900006  | Serienummer        |

På siden **Egendefinerte felt** legger du til følgende poster for de egendefinerte feltene for oppsett av mottaket. Vær oppmerksom på at verdiene **Tekst-ID for overskrift** må samsvare med verdiene **Tekst-ID** som du har angitt på siden **Språktekst**:

| Navn                 | Type    | Tekst-ID for overskrift |
|----------------------|---------|-----------------|
| TLT                  | Tilgang | 900001          |
| SEC                  | Tilgang | 900002          |
| SIGN                 | Tilgang | 900003          |
| FISCAL               | Tilgang | 900004          |
| INFO                 | Tilgang | 900005          |
| CONTINUOUSNUMBER     | Tilgang | 900006          |

> [!NOTE]
> Det er viktig at du angir riktige egendefinerte feltnavn, som vist i foregående tabell. Et feil egendefinert feltnavn vil forårsake manglende data i kvitteringer.

### <a name="configure-receipt-formats"></a>Konfigurere mottaksformater

For hvert nødvendig kvitteringsformat endrer du verdien for feltet **Utskriftsatferd** til **Skriv alltid ut**.

I Utforming av kvitteringsformat legger du til de egendefinerte feltene nedenfor i de aktuelle kvitteringsdelene. Vær oppmerksom på at feltnavnene samsvarer med språktekstene som du definerte i forrige del.

- **Topptekst:** Legg til følgende felter.

    - **Butikknavn** og **Avgiftsidentifikasjonsnummer**: Disse feltene brukes til å skrive ut firmanavnet og identitetsnummeret på kvitteringer. Du kan også legge til firmanavnet og identitetsnummeret i salgskvitteringsoppsettet som frihåndstekst.
    - **Butikkadresse**, **Dato**, **Klokkeslett 24H**, **Kvitteringsnummer** og **Registreringsnummer**.
    - **Serienummer**: Dette feltet identifiserer nummeret til kontanttransaksjonen i regnskapsregistreringstjenesten.

- **Linjer:** Legg til følgende felter.

    - **Varenavn**
    - **Antall**
    - **Totalpris med avgift**

- **Bunntekst:** Legg til følgende felter.

    - Betalingsfelter, slik at betalingsbeløpene for hver betalingsmåte skrives ut. Du kan for eksempel legge til feltene **Betalingsmiddel** og **Betalingsmiddelbeløp** i én linje i oppsettet.
    - **ID provozfaktura/pokladny**: Dette feltet skriver ut identifikatorene til forretningslokalene og kassen.
    - **BKP**: Dette feltet skriver ut avgiftsbetalerens sikkerhetskode som er tilordnet av regnskapsregistreringstjenesten.
    - **FIK**: Dette feltet skriver ut regnskapsidentifikasjonskoden for transaksjonen som tilordnes av nettjenesten til skattemyndighetene i tilfelle vellykket nettregistrering.
    - **PKP**: Dette feltet skriver ut avgiftsbetalerens signaturkode som genereres av regnskapsregistreringstjenesten ved frakoblet registrering.
    - **Info**: Dette feltet skriver ut tilleggsinformasjonen fra regnskapsregistreringstjenesten.

Hvis du vil ha mer informasjon om hvordan du arbeider med kvitteringsformater, kan du se [Definere og utforme kvitteringsformater](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-the-czech-republic"></a>Definer regnskapsintegrering for Tsjekkia

Eksemplet på integrering av regnskapsregistreringstjenesten for Tsjekkia er basert på [regnskapsintegreringsfunksjonaliteten](fiscal-integration-for-retail-channel.md) og er en del av Retail SDK. Eksemplet finnes i **src\\FiscalIntegration\\Efr**-mappen i repositoriet for [løsningen for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (for eksempel [eksemplet i release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) av en regnskapsdokumentleverandør, som er en utvidelse av Commerce Runtime (CRT) og en regnskapskobling, som er en utvidelse av Commerce-maskinvarestasjon. Hvis du vil ha mer informasjon om hvordan du bruker Retail SDK, kan du se [Retail SDK-arkitektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en kompileringskontroll for uavhengig emballasje-SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en virtuell utviklermaskin (VM) i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for eksempel på regnskapsintegrering for Tsjekkia (eldre)](emea-cze-fi-sample-sdk.md).
>
> Støtte for den nye uavhengige emballasje- og utvidelsesmodellen for regnskapsintegreringseksempler planlegges for senere versjoner.

Fullfør fremgangsmåten for oppsett av regnskapsintegrering slik det beskrives i [Oppsett av regnskapsintegrering for Commerce-kanaler](setting-up-fiscal-integration-for-retail-channel.md):

1. [Definer en regnskapsregistreringsprosess](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Noter deg også innstillingene for regnskapsregistreringsprosessen som er [spesifikke for dette eksemplet med integrering av regnskapsregistreringstjenesten](#set-up-the-registration-process).
1. [Angi innstillinger for feilbehandling](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Aktiver manuell kjøring av utsatt bilagsregistrering](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurere kanalkomponenter](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Definere registreringsprosessen

Hvis du vil aktivere registreringsprosessen, følger du denne fremgangsmåten for konfigurere Commerce Headquarters. Hvis du vil ha mer informasjon om regnskapsintegrering, kan du se [Definere økonomisk integrering for handelskanaler](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Last ned konfigurasjonsfiler for regnskapsdokumentleverandøren og regnskapskoblingen:

    1. Open respositoriet for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Velg riktig frigivelsesavdelingsversjon i henhold til SDK/programversjonen (for eksempel **[release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Åpne **src \> FiscalIntegration \> Efr**.
    1. Last ned konfigurasjonsfilen for regnskapsdokumentleverandør under **Konfigurasjoner \> DocumentProviders \> DocumentProviderFiscalEFRSampleCzech.xml** (for eksempel [filen for release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleCzech.xml)).
    1. Last ned konfigurasjonsfilen for regnskapskoblingen under **Konfigurasjoner \> Koblinger \> ConnectorEFRSample.xml** (for eksempel [filen for release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en utvikler-VM i LCS. Konfigurasjonsfilene for dette regnskapsintegreringseksemplet ligger i følgende mapper for Retail SDK på en utvikler-VM i LCS:
    >
    > - **Konfigurasjonsfil for regnskapsdokumentleverandør:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Konfigurasjon\\DocumentProviderFiscalEFRSampleCzech.xml
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

- **Tilordning av merverdiavgiftssatser (mva.)** – Tilordningen av mva-prosentverdier som er definert for mva-kodene til verdier av attributtet **TaxG** (mva-gruppe) i forespørsler som sendes til regnskapstjenesten. Her er standardtilordningen:

    ```
    A: 21.00; B: 15.00; C: 10.00; Z: 0.00
    ```

    Den første komponenten i hvert par representerer en mva-gruppe som støttes av EFR-regnskapsregistreringstjenesten. Den andre komponenten representerer den tilsvarende mva-satsen. Hvis du vil ha mer informasjon om mva-grupper som EFR støtter for Tsjekkia, kan du se [EFR-referansen](https://public.efsta.net/efr/).

- **Standard mva-gruppetilordning** – Alle mva-beløp som ikke kan tilordnes en av de forhåndsbestemte mva-gruppene, tilskrives standard mva-gruppe (standardvaluta). Her er standardtilordningen:

    ```
    A
    ```

- **Tilordning av mva-gruppe for innbetaling** – Innbetalingsbeløp for kunde og innbetalingsbeløp for kundeordre tilskrives mva-gruppen for innbetaling. Her er standardtilordningen:

    ```
    Z
    ```

#### <a name="fiscal-connector-settings"></a>Innstillinger for regnskapskobling

Følgende innstillinger er inkludert i konfigurasjonen for regnskapskoblingen som angis som en del av eksempelet på regnskapsintegrering:

- **Endrepunktadresse** – URL-adressen til regnskapsregistreringstjenesten.
- **Tidsavbrudd** – Tiden, i millisekunder, som regnskapskoblingen vil vente på svar fra regnskapsregistreringstjenesten.

### <a name="configure-channel-components"></a>Konfigurere kanalkomponenter

> [!WARNING]
> På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en utvikler-VM i LCS. Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for eksempel på regnskapsintegrering for Tsjekkia (eldre)](emea-cze-fi-sample-sdk.md).
>
> Støtte for den nye uavhengige emballasje- og utvidelsesmodellen for regnskapsintegreringseksempler planlegges for senere versjoner.

#### <a name="set-up-the-development-environment"></a>Definere utviklingsmiljøet

Følg denne fremgangsmåten for å definere et distribusjonsmiljø slik at du kan teste og utvide eksemplet.

1. Klon eller last ned repositoriet for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions). Velg riktig frigivelsesavdelingsversjon i henhold til SDK/programversjonen. Hvis du vil ha mer informasjon, kan du se [Last ned eksempler og referansepakker i SDK for Retail fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
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

## <a name="design-of-extensions"></a>Utforming av utvidelser

Eksemplet på integrering av regnskapsregistreringstjenesten for Tsjekkia er basert på [regnskapsintegreringsfunksjonaliteten](fiscal-integration-for-retail-channel.md) og er en del av Retail SDK. Eksemplet finnes i **src\\FiscalIntegration\\Efr**-mappen i repositoriet for [løsningen for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (for eksempel [eksemplet i release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) av en regnskapsdokumentleverandør, som er en utvidelse av CRT og en regnskapskobling, som er en utvidelse av Commerce-maskinvarestasjon. Hvis du vil ha mer informasjon om hvordan du bruker Retail SDK, kan du se [Retail SDK-arkitektur](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en kompileringskontroll for uavhengig emballasje-SDK](../dev-itpro/build-pipeline.md).

> [!WARNING]
> På grunn av begrensninger i den [nye uavhengige emballasje- og linjemodellen](../dev-itpro/build-pipeline.md), kan den for øyeblikket ikke brukes for dette eksemplet på regnskapsintegrering. Du må bruke den forrige versjonen av Retail SDK på en utvikler-VM i LCS. Hvis du vil ha mer informasjon, kan du se [Distribusjonsretningslinjer for eksempel på regnskapsintegrering for Tsjekkia (eldre)](emea-cze-fi-sample-sdk.md). Støtte for den nye uavhengige emballasje- og utvidelsesmodellen for regnskapsintegreringseksempler planlegges for senere versjoner.

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime-utvidelsesutforming

Formålet med filtypen som er en regnskapsdokumentleverandør, er å generere servicespesifikke dokumenter og håndtere svar fra regnskapsregistreringstjenesten.

#### <a name="request-handler"></a>Forespørselsbehandler

Det finnes en enkelt **DocumentProviderEFRFiscalCZE**-forespørselsbehandler for dokumentleverandør, som brukes til å generere regnskapsdokumenter for regnskapsregistreringstjenesten.

Denne behandleren arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på koblingsdokumentleverandøren som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler.

- **GetFiscalDocumentDocumentProviderRequest** – Denne forespørselen inneholder informasjon om hvilke dokumenter som skal genereres. Det returnerer et servicespesifikk dokument som skal registreres i regnskapsregistreringstjenesten.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Denne forespørselen returnerer listen over hendelser du kan abonnere på. For øyeblikket støttes følgende hendelser: salg, kundekontoinnbetalinger og innbetalinger for kundeordre.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Denne forespørselen returnerer svaret fra regnskapsregistreringstjenesten. Dette svaret serialiseres til å utgjøre en streng, slik at den er klar til å lagres.

#### <a name="configuration"></a>Konfigurasjon

Konfigurasjonsfilen for regnskapsdokumentleverandør ligger under **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders\\DocumentProviderFiscalEFRSampleCzech.xml** i repositoriet for [løsningene for Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er å aktivere innstillinger for dokumentleverandøren som skal konfigureres fra Commerce Headquarters. Filformatet samkjøres med kravene for konfigurasjon av regnskapsintegrering.

### <a name="hardware-station-extension-design"></a>Utvidelsesutforming for maskinvarestasjon

Formålet med utvidelsen som er en regnskapskobling, er å kommunisere med regnskapsregistreringstjenesten. Utvidelsen for maskinvarestasjon bruker HTTP-protokollen til å sende dokumenter som CRT-utvidelsen genererer til regnskapsregistreringstjenesten. Den håndterer også svarene som mottas fra regnskapsregistreringstjenesten.

#### <a name="request-handler"></a>Forespørselsbehandler

Forespørselsbehandleren **EFRHandler** er startpunktet for behandling av forespørsler til regnskapsregistreringstjenesten.

Behandleren arves fra **INamedRequestHandler**-grensesnittet. **HandlerName**-metoden er ansvarlig for å returnere navnet på behandleren. Behandlernavnet må samsvare med navnet på regnskapskoblingen som er angitt i Commerce Headquarters.

Koblingen støtter følgende forespørsler.

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
