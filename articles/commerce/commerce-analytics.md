---
title: Commerce-analyse (forhåndsversjon)
description: Dette emnet forklarer hvordan du installerer og bruker analysefunksjonen i Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 11/23/2021
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 8cfe2af756315b5be3eb22d99376a96166fffc52
ms.sourcegitcommit: f9fca3d55b47e615e5ef64669dab184e057ec234
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/23/2021
ms.locfileid: "7862779"
---
# <a name="commerce-analytics-preview"></a>Commerce-analyse (forhåndsversjon)

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du installerer Commerce-analyse (forhåndsversjon), den funksjonelle kapasiteten som er inkludert i Microsoft Dynamics 365 Commerce.

## <a name="commerce-analytics-preview-live-demo"></a>Commerce-analyse (forhåndsversjon), live demo

Du kan prøve ut en [live demo av Commerce-analyse (forhåndsversjon)](https://aka.ms/CommerceAnalyticsDemo).

![Sammendrag av Commerce-analyse (forhåndsversjon)](media/CommerceAnalytics_Summary.png)
![Betalinger av Commerce-analyse (forhåndsversjon) Payments](media/CommerceAnalytics_Payments.png)
![Webaktivitet for Commerce-analyse (forhåndsversjon)](media/CommerceAnalytics_WebActivity.png)


## <a name="commerce-analytics-preview-system-architecture"></a>Systemarkitekturen i Commerce-analyse (forhåndsversjon)

### <a name="key-components"></a>Nøkkelkomponenter

Commerce-analyse (forhåndsversjon) består av følgende nøkkelkomponenter:

- Interaktive Power BI rapporter som er klare til bruk
- SQL-visninger i Azure Synapse analyse
- Enhets- og ontologidata i Azure Data Lake
- Rådata i Data Lake

![Nøkkelkomponenter i systemarkitekturen til Commerce-analyse](media/CommerceAnalyticsArchitecture_v2.png)

### <a name="data-flow"></a>Dataflyt

#### <a name="step-1-data-generation"></a>Trinn 1: Datagenerering

Data kommer enten som transaksjonsdata eller virkemåtedata fra en av følgende kilder:

- En samtalesentermedarbeider bruker Commerce HQ-klienten til å behandle salgsordrer.
- En kasserer ved salgsstedet (POS) behandler salgstransaksjoner.
- Salg opprettes i tilpassede programmer ved hjelp av hodeløs handel (Commerce Scale Unit).
- En e-handelskunde blar gjennom webområdet for e-handel.
- En e-handelskunde bestiller noe på webområdet for e-handel.
- Data produseres av andre systemer, for eksempel Dynamics 365 Connected Spaces.

#### <a name="step-2-ingestion-and-pre-processing"></a>Trinn 2: Innføring og forhåndsbehandling

Transaksjonsdata går til Commerce HQ enten direkte (når det gjelder ordrer som registreres direkte i Commerce HQ-klienten) eller via Commerce Scale Unit (når det gjelder ordrer som blir registrert på salgsstedet, i e-handel, eller i egendefinerte klienter som bruker hodeløs handel).

Funksjonen Eksporter til Data Lake brukes deretter til å kopiere transaksjonsdataene til datasjøen som rådata. I datasjøen opprettes rådataene i Tabeller-mappen.

Webaktivitetsdata for e-handel sendes direkte til datasjøen. Data som produseres av andre systemer, for eksempel Dynamics 365 Connected Spaces, sendes direkte til datasjøen av disse systemene.

#### <a name="step-3-transformation-and-aggregation"></a>Trinn 3: Transformasjon og samling

Når rådata er i dataoppsamlingen, leser Commerce-analysetjenesten den, omformer den, samler dem opp og skriver den tilbake til datasjøen i form av logiske enheter (i Enheter-mappen) og akkumulerte mål (i Ontologies-mappen).

#### <a name="step-4-querying"></a>Trinn 4: Spørringer

Azure Synapse analyse brukes til å spørre på data i datasjøen via et T-SQL-grensesnitt (Transact-SQL). Dette grensesnittet inneholder SQL-visninger. SQL-visninger gjør det mulig å bruke federerte spørringer av data i datasjøen, enten direkte via en T-SQL-klient (for ad-hoc-analyse) eller via et visualiseringsverktøy, som Power BI.

#### <a name="step-5-modeling-and-serving"></a>Trinn 5: Modellering og betjening

Data som spørres av Azure Synapse analyse, går til Power BI sin semantiske modell. Avhengig av datatypen er det enten periodisk importert i minnet til Power BI eller direkte spørringer ved kjøring.

Til slutt gjengis dataene i Power BI grafikk, slik at brukere kan vise og samhandle med dem.

## <a name="commerce-analytics-preview-functional-overview"></a>Funksjonsoversikt for Commerce-analyse (forhåndsversjon)

### <a name="summary"></a>Sammendrag

Commerce-analyse-malapp inneholder følgende hovedrapportsider:

1. [Filtre på øverste nivå](#TopLevelFilters)
2. [Produkter](#ProductsPage)
3. [Kunder](#CustomersPage)
4. [Kanaler](#ChannelsPage)
5. [Salg](#SalesPage)
6. [Marger](#MarginsPage)
7. [Returer](#ReturnsPage)
8. [Rabatter](#DiscountsPage)
9. [Betalinger](#PaymentsPage)
10. [Kunder](#CustomersPage)
11. [Sammenligning](#ComparisonPage)
12. [Webaktivitet](#WebActivityPage)
13. [Webaktivitet - Filter på øverste nivå](#WebActivityTopLevelFilters)

####  <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Filtre på øverste nivå

- Datoinnstillinger

    - År
    - Kvartal
    - Måned
    - Uke
    - Dag

- Kanalinnstillinger

    - Juridisk enhet
    - Kanaltype
    - Kundetype
    - Salgstype
    - Kanal
    - Organisasjonshierarki

- Produktinnstillinger

    - Kategorihierarki
    - Kategori

####  <a name="products"></a><a name="ProductsPage"></a> Produkter

- Salg
- Marg
- Returer

####  <a name="customers"></a><a name="CustomersPage"></a> Kunder

- Salg
- Marg
- Returer

#### <a name="channels"></a><a name="ChannelsPage"></a> Kanaler

- Salg
- Marg
- Returer

### <a name="sales"></a>Salg <a name="SalesPage"></a>

- Etter leveringslokasjon
- Etter kanal/butikk/terminal
- Etter ansatt
- Etter dato
- Etter time
- Etter produktkategori

### <a name="margins"></a><a name="MarginsPage"></a> Marger

- Etter leveringslokasjon
- Biprodukt
- Etter dato

### <a name="returns"></a><a name="ReturnsPage"></a> Returer

- Retur etter beløp

    - Av filial
    - Biprodukt
    - Etter dato

- Retur etter transaksjon

    - Av filial
    - Biprodukt
    - Etter dato

### <a name="discounts"></a><a name="DiscountsPage"></a> Rabatter

- Av filial
- Biprodukt
- Etter dato
- Nedbryting

    - Juridisk enhet
    - Butikk
    - Rabattype
    - Rabattnavn
    - Produkt

### <a name="payments"></a><a name="PaymentsPage"></a> Betalinger

- Etter kanal/terminal
- Etter betalingsmåte/type
- Etter dato
- Nedbryting

    - Juridisk enhet
    - Kanaltype
    - Butikk
    - Terminal
    - Betalingsmåte

### <a name="customers"></a><a name="CustomersPage"></a> Kunder

- Levetidsverdi (LTV)

    LTV beregnes på grunnlag av det totale beløpet en kunde bruker på tvers av alle Dynamics 365 Commerce salgskanalene (inkludert salgssted, e-handel og telefonsenter).

- Recency

    Recency beregnes, basert på antall dager siden en kundes siste transaksjonsavtale med organisasjonen. For øyeblikket tar ikke recency i betraktning signaler som ikke gjelder transaksjoner, for eksempel aktivitet for e-handellesing.

- Frekvens

    Frekvens beregnes, basert på en kundes transaksjonsavtale med organisasjonen. For øyeblikket tar ikke frekvens i betraktning signaler som ikke gjelder transaksjoner, for eksempel aktivitet for e-handellesing.

- Relasjonslengde

    Relasjonslengden beregnes basert på antallet dager siden kundeposten ble opprettet i systemet.

- Transaksjonstelling

### <a name="comparison"></a><a name="ComparisonPage"></a> Sammenligning

- Produktsammenligning etter tidsperiode

    - Salgs- og salgsdifferanse
    - Margin- og margindifferanse

- Kunde etter tidsperiode

    - Salgs- og salgsdifferanse
    - Margin- og margindifferanse

### <a name="web-activity"></a><a name="WebActivityPage"></a> Webaktivitet

#### <a name="top-level-filters"></a><a name="WebActivityTopLevelFilters"></a> Filtre på øverste nivå

- Datoområde
- Kanaltype
- Kanal
- Kategorihierarki

#### <a name="acquisitions"></a>Anskaffelser

- Sidevisninger

    - Etter land eller område
    - Biprodukt
    - Etter brukers logget på-status
    - Etter dato

- E-handelsordrer
- Omregningssats

    - Etter dato

- Konverteringstrakt

    - Sidevisning etter sidetype (startside, kategoriside eller produktdetaljerside)
    - Legg til i kurv
    - Betaling
    - Kjøp

#### <a name="sessions"></a>Økter

En økt er en viktig del av en brukers besøk på webområdet for e-handel. Økten vurderes som avsluttet etter 30 minutter med inaktivitet eller 24 timer med aktiv bruk.

- Etter land eller område
- Etter opprinnelse (ekstern referanse)
- Etter brukers logget på-status
- Øktopptelling

    - Etter dato
    - Etter oppføringsside

- Ordre per økt

    - Etter dato

- Fluktfrekvens for økt

    En fluktfrekvens for økt er en økt der en bruker forlater økten umiddelbart etter å ha gått til webområdet for e-handel. Hvis du vil ha mer informasjon, kan du se [Fluktfrekvens](https://en.wikipedia.org/wiki/Bounce_rate).

- Klikk per økt

#### <a name="visitors"></a>Besøkende

En anonym besøkende på e-handelsområdet identifiseres unikt basert på den bestemte webleseren og den spesifikke enheten brukeren bruker. Commerce-analyse sporer ikke anonym anonyme besøkende på tvers av ulike nettlesere eller enheter. En anonym besøkende som bruker den samme webleseren på den samme enheten, identifiseres unikt på tvers av flere brukerøkter, helt til enten webleserens hurtigbufrede data tømmes eller en periode (vanligvis 12 måneder) passerer, avhengig av hva som skjer først.

Hvis besøkende blar gjennom e-handelsområdet når de er logget på, kan Commerce-analyse gi mer informasjon om dem. Denne informasjonen er basert på den eksisterende relasjonen som organisasjonen har med bakgrunn i innkjøpene sine fra før av i alle salgskanalene Dynamics 365 Commerce (inkludert salgssted, e-handel og telefonsenter). Tilleggsinformasjonen omfatter recency, relasjonslengde, levetidsverdi og frekvensdata.

- Margin for besøkende
- Gjennomsnittlige ordrer for besøkende
- Gjennomsnittlige salg for besøkende
- Antall besøkende på e-handelsområde

    - Etter dato
    - Etter sted

        Commerce-analyse kan for øyeblikket bare gi detaljert informasjon på lands-/områdenivå for stedsinnsikt for e-handel.

    - Etter recency

        Recency beregnes, basert på antall dager siden en kundes siste transaksjonsavtale med organisasjonen. For øyeblikket tar ikke recency i betraktning signaler som ikke gjelder transaksjoner, for eksempel aktivitet for e-handellesing.

    - Etter relasjonslengde

        Relasjonslengden beregnes basert på antallet dager siden kundeposten ble opprettet i systemet.

    - Etter levetidsverdi (LTV)

        LTV beregnes på grunnlag av det totale beløpet en kunde bruker på tvers av alle Dynamics 365 Commerce salgskanalene (inkludert salgssted, e-handel og telefonsenter).

    - Etter frekvens

        Frekvens beregnes, basert på en kundes transaksjonsavtale med organisasjonen. For øyeblikket tar ikke frekvens i betraktning signaler som ikke gjelder transaksjoner, for eksempel aktivitet for e-handellesing.

#### <a name="impressions"></a>Visninger

En visning er én enkelt visning av et visuelt produkt av en e-handelsbesøkende. For eksempel går en e-handelsbesøkende til hjemmesiden din på e-handelsområdet og viser et matprodukt i en **toppsalg**-listemodul. Deretter vises samme matprodukt i **Plukkinger for deg**-listemodulen. I dette tilfellet finnes det to produktvisninger. 

For øyeblikket spores visninger i følgende flater:

- Lister (for eksempel **Anbefalt**, **Toppsalg**, **Plukkinger for deg** og **Tendenser**)
- Handlekurvmodul
- Søkeresultatcontainer
- Container for kategorisøkeresultat

For øyeblikket telles ikke produkter som er gjengitt i en karusellmodul eller i egendefinerte visualobjekter, i visningsrelaterte mål.

Siden **Visningsrapport** inneholder følgende mål:

- Antall visninger

    - Etter sidetype og modul

        Sidetype er den generiske typen side som er definert for hver side på webområdet for e-handel. Modultype er den typen visuell e-handel-modul som produktet vises i.

        Hvis du vil vise informasjon etter modul, må du kanskje drille ned i siden og modulens visuelle effekter.

    - Biprodukt
    - Etter brukers logget på-status
    - Etter dato

- Antall visninger med klikk

    Klikk skjer når en e-handelsbesøkende velger et visuelt produkt. Vanligvis tas den besøkende deretter til produktdetaljersiden for produktet.

- Klikkfrekvens

    Klikkfrekvens beregnes som det totale antallet klikk som skal deles på totalt antall klikk.

## <a name="commerce-analytics-preview-installation"></a>Installasjon av Commerce-analyse (forhåndsversjon)

> [!NOTE]
> Commerce-analyse (forhåndsversjon) er i forhåndsversjon i USA, Canada, Storbritannia, Europa, Sør-Øst-Asia, Øst-Asia, Australia og Japan. Hvis Finance and Operations miljøet ditt finnes i noen av disse områdene, kan du aktivere denne funksjonen i miljøet ditt ved å bruke Microsoft Dynamics Lifecycle Services (LCS). Før du kan bruke denne funksjonen, kan du se [Konfigurere eksport til Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>Aktivere og konfigurere Commerce-analyse (forhåndsversjon)

Hvis du vil installere Commerce-analyse (forhåndsversjon), må du ha tillatelse til å opprette ressurser i et Azure-abonnement. Du må også ha tillatelse til å installere tilleggsprogrammet i LCS. Her er en oversikt over trinnene:

1. [Send inn inntaksskjemaet for Commerce-analyse (forhåndsversjon)](#joinPreview).
2. [Aktivere og konfigurere Eksporter til Data Lake](#enableExportToDataLake).
3. [Aktivere og konfigurere Commerce-analyse (forhåndsversjon)](#enableCommerceAnalyticsAddin).
4. [Generer en signatur for delt tilgang (SAS)-token for lagringskontoen](#getSASToken).
5. [Last ned distribusjonsskriptene for Azure Synapse visninger](#downloadSynapseDeploymentScripts).
6. [Installer og konfigurer et Azure Synapse workspace](#configureAzureSynapse).
7. [Installer Power BI malappen](#powerbi).

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a>Send inn inntaksskjemaet for Commerce-analyse (forhåndsversjon).

Send inn [inntaksskjemaet for Commerce-analyse (forhåndsversjon)](https://forms.office.com/r/vW5VLJGXZ2). Tillat opptil tre virkedager for behandling av skjemaet. Når det er behandlet, blir det sendt en bekreftelses-e-post til e-postadressen du oppgav i skjemaet.

### <a name="enable-and-configure-export-to-data-lake"></a><a name="enableExportToDataLake"></a>Aktivere og konfigurere Eksporter til Data Lake

Commerce-analyse (forhåndsversjon) er avhengig av funksjonen Eksport til Data Lake for eksport av Commerce HQ-data til Data Lake, og holder dataene oppdatert. Før du konfigurerer Commerce-analyse (forhåndsversjon), må du aktivere og konfigurere eksport til Azure Data Lake ved å følge trinnene i [Konfigurere eksport til Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

Når du konfigurerer eksport til Azure Data Lake, noterer du deg følgende informasjon fordi du må angi den senere:

- <a name="keyVault"></a>DNS-navnet (Domain Name System) til nøkkelhvelvet, og de hemmelige navnene der du lagrer program-ID- og programhemmeligheten. Hvis du vil ha mer informasjon om mål, se [Legge til hemmeligheter i nøkkelhvelvet](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).
- <a name="storageAccount"></a>Navnet på lagringskontoen for Data Lake-forekomsten. Hvis du vil ha mer informasjon, kan du se [Opprette en Data Lake Storage (Gen2)-konto i abonnementet](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription).

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a>Aktivere og konfigurere Commerce-analyse (forhåndsversjon)

Hvis du vil installere Commerce-analyse (forhåndsversjon) i LCS, må du være miljøadministrator i LCS for miljøet du planlegger å bruke.

Følg denne fremgangsmåten for å installere og konfigurere Commerce-analyse (forhåndsversjon).

1. Logg deg på [LCS](https://lcs.dynamics.com/), og gå til miljøet ditt.
2. På **Miljø**-siden i fanen **Miljøtillegg** velger du **Installer et nytt tillegg**.
3. Velg **Commerce-analyse (forhåndsversjon)** i dialogboksen.

    Hvis **Commerce-analyse (forhåndsversjon)** ikke er oppført, må du passe på at du har blitt med i Insider Program.

4. Angi følgende informasjon i dialogboksen **Konfigurer tillegg**.

    | Opplysninger | Kilde | Eksempelverdi |
    |---|---|---|
    | Azure AD leier-ID for miljøet | Logg deg på [Azure Portal](https://portal.azure.com/), og åpne **Azure Active Directory**-tjenesten. Deretter åpner du **Egenskaper**-siden og kopierer verdien i **Katalog-ID**-feltet. | 72f988bf-0000-0000-00000-2d7cd011db47 |
    | DNS-navnet for nøkkelhvelvet | Oppgi [DNS-navnet](#keyVault) til nøkkelhvelvet. Du bør ha notert deg denne verdien i den forrige delen. | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Hemmelighet som inneholder program-IDen | Angi det [hemmelige navnet som lagrer program-IDen](#keyVault). Du bør ha notert deg denne verdien i den forrige delen. | app-id |
    | Hemmelighet som inneholder programhemmeligheten | Angi det [hemmelige navnet på butikken som lagrer programhemmeligheten](#keyVault). Du bør ha notert deg denne verdien i den forrige delen. | app-secret |

5. Godta betingelsene for tilbudet ved å merke av for boksen, og velg deretter **Installer**.

    Systemet installerer og konfigurerer Commerce-analyse (forhåndsversjon)-tillegget for miljøet. Denne prosessen kan ta noen minutter. Når installasjonen er fullført, skal **Commerce-analyse (forhåndsversjon)** vises på **Miljø**-siden, og statusen bør være **Installert**.

### <a name="generate-a-sas-token-for-your-storage-account"></a><a name="getSASToken"></a>Generere et SAS-token for lagringskontoen

Et SAS-token gjør det mulig for eksterne enheter å få tilgang til lagringskontoen, og har et bestemt sett med rettigheter for en begrenset tidsperiode. Azure Synapse vil bruke SAS-tokenet til å få tilgang til underliggende data i Data Lake.

> [!NOTE]
> På grunn av en kjent begrensning i Commerce-analyse (forhåndsversjon), vil Azure Synapse forekomsten miste tilgangen til datasjøen når SAS-tokenet utløper. Når du genererer SAS-tokenet, må du derfor angi maksimal utløpsdato som organisasjonens sikkerhetsretningslinjer tillater.

Følg denne fremgangsmåten for å generere et SAS-token.

1. I Azure Portal går du til [lagringskontoen](#storageAccount) du opprettet da du konfigurerte eksport til Data Lake.
2. Velg **Delt tilgangssignatur** i venstre rute under lagringskontoen.
3. På **SAS-alternativer**-siden angir du følgende felter.

    | Felt | Verdi |
    |---|---|
    | Tillatte tjenester | Velg **Blob**. |
    | Tillatte ressurstyper | Velg **Tjeneste**, **Container** og **Objekt**. |
    | Tillatte tillatelser | Velg **Les**, **Skriv**, **Slett**, **Vis**, **Legg til** og **Opprett**. |
    | Tillatelser for Blob-versjonskontroll | Velg **Aktiverer sletting av versjoner**. |
    | Startdato og -tidspunkt for utløp | Angi start- og sluttdato og -klokkeslett for SAS-tokenet etter behov. |
    | Tillatte IP-adresser | La dette feltet stå tomt. |
    | Tillatte protokoller | Velg **Bare HTTPS**. |
    | Foretrukket rutingslag | Velg **Grunnleggende (standard)**. |
    | Signeringsnøkkel | Velg **key1** eller **key2** etter behov. |

4. Velg **Generer SAS og tilkoblingsstreng**.
5. Kopier verdien i **SAS-token**-feltet, og lim den inn i et tekstredigeringsprogram, for eksempel Notisblokk.

### <a name="download-the-deployment-scripts-for-azure-synapse-views"></a><a name="downloadSynapseDeploymentScripts"></a>Last ned distribusjonsskriptene for Azure Synapse-visninger

Hvis du vil opprette og publisere de nødvendige visningene i et Azure Synapse workspace, må du kjøre et sett med skript. Følg disse trinnene for å laste ned skriptene.

1. På GitHub går du til repositoriet [microsoft/Dynamics365Commerce.Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) (repo).
2. Last ned skriptene til den lokale datamaskinen ved å klone repo eller laste den ned som en zip-fil.

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a>Installer og konfigurer et Azure Synapse workspace

Hvis du vil installere og konfigurere et Azure Synapse workspace, gjør du følgende.

1. Installer et Azure Synapse workspace i Azure-abonnementet. Hvis du vil ha mer informasjon, kan du se [Hurtigstart: Opprette et Synapse-arbeidsområde](/azure/synapse-analytics/quickstart-create-workspace).
2. I Notisblokk eller et annet tekstredigeringsprogram åpner du **setupSynapse.sql**-skriptfilen fra mappen på den lokale datamaskinen du klonet eller lastet ned Dynamics365Commerce.Solutions repo til i den forrige delen. Skriptfilen vil være under mappen /Pipeline/CommerceAnalyticsSynapse/. I skriptet erstatter du plassholdertekst med verdier som vist i følgende tabell.

    | Plassholdertekst | Erstatningsverdi |
    |---|---|
    | placeholder_storageaccount | Navnet på [lagringskontoen](#storageAccount) du opprettet da du konfigurerte eksport til Data Lake. |
    | <a name="phContainer"></a>placeholder_container | Navnet på lagringscontaineren som ble opprettet i Data Lake-forekomsten etter at du installerte Eksporter til Data Lake-tillegget i LCS på riktig måte. Hvis du vil hente containernavnet, må du bruke Lagringsutforsker i Azure Portal til å bla gjennom lagringskontoen. |
    | placeholder_sastoken | [SAS-tokenet](#getSASToken) du genererte. Pass på at du fjerner spørsmålstegnet (**?**) fra begynnelsen av SAS-tokenverdien. |
    | <a name="phUserPwd"></a>placeholder_password | Et sterkt passord du velger. Noter dette passordet. Det blir angitt som passord for den nye **reportreadonlyuser**-kontoen som skriptet oppretter. Du bør **ikke** angi passordet for **sqladminuser**-kontoen. |

3. Kopier det oppdaterte innholdet i skriptfilen.
4. I Azure Portal går du til det nye Azure Synapse workspace. På **Oversikt**-siden velger du **Åpne Synapse Studio**.
5. I Synapse Studio velger du **Nytt \> SQL-skript**, og limer inn innholdet i skriptfilen i SQL-skriptredigeringsprogrammet.
6. Kontroller at **Bruk database**-feltet er satt til **hoved**.
7. Velg **Kjør** og vent til skriptet er ferdig med å kjøre. Vellykket utføring av skriptet oppretter databasen for Commerce-analyse, legitimasjon for tilgang til datasjøen, og en skrivebeskyttet brukerkonto som Power BI skal bruke til å koble til Azure Synapse forekomsten.
8. Åpne Windows PowerShell i admin-modus på den lokale datamaskinen, og gå til mappen /Pipeline/CommerceAnalyticsSynapse/ under mappen der du klonet eller lastet ned Dynamics365Commerce.Solutions repo til.
9. Konfigurer utførelsespolicyen i Windows PowerShell ved å kjøre følgende kommando.

    ```powershell
    Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
    ```

10. Hvis SQL Server PowerShell-modulen ikke allerede er installert, installerer du den ved å kjøre kommandoen nedenfor.

    ```powershell
    Install-Module sqlserver
    ```

    > [!NOTE]
    > Under installasjonen av modulen kan du bli bedt om å installere NuGet leverandør. I dette tilfellet velger du **Y** for å installere NuGet leverandør. Du kan også bli bedt om å bekrefte at du installerer moduler fra et ikke-klarert repositorium. I dette tilfellet velger du **Y** for å fortsette med installasjonen. Du kan eventuelt kjøre **Set-PSRepository**-cmdlet-en for å klarere **PSGallery**-repositoriet.

11. Publiser Azure Synapse visningene ved å kjøre følgende kommando.

    ```powershell
    .\PublishSynapseViews.ps1 -serverName SERVER_NAME -password PASSWORD -storageAccount STORAGE_ACCOUNT -containerName CONTAINER_NAME -datarootpath DATA_ROOT_PATH
    ```

    Når du kjører denne kommandoen, erstatter du plassholderverdiene som vist i følgende tabell.

    | Plassholderverdi | Erstatningsverdi |
    |---|---|
    | SERVER_NAME | Navnet på det Azure Synapse serverløse SQL-sluttpunktet. Du kan få denne verdien fra **Oversikt**-siden for Azure Synapse workspace i Azure Portal. |
    | PASSWORD | Passordet for **sqladminuser**-kontoen. |
    | STORAGE_ACCOUNT | Navnet på lagringskontoen for Data Lake. |
    | CONTAINER_NAME | Navnet på containeren som ble opprettet ved hjelp av funksjonen Eksporter til Data Lake. Denne containeren er den samme containeren som du angav som [placeholder_container](#phContainer)-verdien i trinn 2. |
    | DATA_ROOT_PATH | Mappenavnet under containeren som inneholder alle dataene. |

    > [!NOTE]
    > Du finner navnet på lagringskonto, containernavnet og datarotbanen ved å bruke Azure Storage-nettleseren og Data Lake-lagringskontoen i Azure Portal.

12. Vent til skriptet er ferdig med å kjøre. Vellykket kjøring av skriptet vil opprette SQL-visninger i Azure Synapse SQL-forekomsten uten server.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a>Installere Power BI malappen

Følg denne fremgangsmåten for å installere Power BI malappen for Commerce-analyse (forhåndsversjon).

1. Logg deg på [Power BI portalen](https://powerbi.microsoft.com/) ved hjelp av organisasjons-IDen.
2. Installer Power BI malappen for Commerce-analyse (forhåndsversjon) ved å gå til [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Du kan få en advarsel som angir at appen ikke er oppført på AppSource. Velg **Installer**.
3. Hvis du installerer appen på nytt for første gang, kan du gå videre til trinn 5. Hvis du har installert denne appen før, vises følgende alternativer for oppdatering av appen:

    - **Oppdater arbeidsområdet og appen**– Oppdater den eksisterende malappen, og overskriv de eksisterende appinnstillingene, for eksempel navn på appforekomst og tillatelseskonfigurasjoner.
    - **Oppdater bare innholdet i arbeidsområdet uten å oppdatere appen** – Oppdater den eksisterende malappen, men behold de eksisterende appinnstillingene. *Dette alternativet er det anbefalte alternativet for appoppdateringer.*
    - **Installer en annen kopi av appen i et nytt arbeidsområde** – Opprett et nytt arbeidsområde, og lag deretter en kopi av den eksisterende malappen i den. Det eksisterende arbeidsområdet blir stående intakt.

4. Velg ett av oppdateringsalternativene, og velg deretter **Installer**.
5. Åpne den installerte appen ved å velge **Apper** i ruten til venstre og deretter velge appen.
6. Koble appen til datakilden ved å velge **Koble til**. Hvis du har installert appen før, velger du **Koble til data**-koblingen på den gule meldingslinjen.
7. Angi følgende felt.

    | Felt | Verdi |
    |---|---|
    | Server | Angi navnet på det Azure Synapse serverløse SQL-sluttpunktet som du opprettet i forrige del. Du kan få denne verdien fra **Oversikt**-siden for Azure Synapse workspace i Azure Portal. |
    | Database | Angi **CommerceAnalytics**. |
    | Språk | Velg en verdi i listen. Dette feltet brukes for lokaliserte produkt- og kategorinavn. Verdien skiller mellom store og små bokstaver. |
    | Datoområde | Velg en verdi i listen. Data for det valgte antall måneder blir importert til Power BI datasettet. Verdien du velger, påvirker størrelsen på datasettet og tidspunktet som kreves for synkroniseringen. |

8. Velg **Neste**. Du blir bedt om å angi legitimasjon for å koble til Azure Synapse SQL-databasen. Angi feltene som vist i følgende tabell.

    | Felt | Verdi |
    |---|---|
    | Godkjenningsmetode | Velg **Grunnleggende**. |
    | Brukernavn | Angi **reportreadonlyuser**. |
    | Passord | Angi verdien du erstattet plassholderen [placeholder_password](#phUserPwd) med i setupSynapse.sql-skriptet. Dette passordet er passordet for **rapportreadonlyuser**-kontoen. |

9. Velg **Logg på og koble til**.
10. Vent til datasettet er oppdatert. Deretter velger du **Rediger app**-knappen for å åpne App-arbeidsområdet, der du kan vise oppdateringsstatusen for datasettet. I App-arbeidsområdet kan du også velge å definere automatiske oppdateringsplaner for datasettet, administrere tillatelser og gi nytt navn til appforekomsten.

### <a name="privacy"></a><a name="privacy"></a>Tilgjengelighet

Personvernet er viktig for oss. Les [personvernerklæringen](https://go.microsoft.com/fwlink/?LinkId=521839) for å finne ut mer.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
