---
title: Commerce-analyse (forhåndsversjon)
description: Dette emnet forklarer hvordan du installerer og bruker analysefunksjonen i Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 02/24/2022
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 7e3721421e15bc3e5937691cdbaee51e4d3cdd17
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349749"
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
- SQL-visninger i Azure Synapse Analytics
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

Azure Synapse Analytics brukes til å spørre etter data i datasjøen via et T-SQL-grensesnitt (Transact-SQL). Dette grensesnittet inneholder SQL-visninger. SQL-visninger gjør det mulig å bruke federerte spørringer av data i datasjøen, enten direkte via en T-SQL-klient (for ad-hoc-analyse) eller via et visualiseringsverktøy, som Power BI.

#### <a name="step-5-modeling-and-serving"></a>Trinn 5: Modellering og betjening

Data som spørres av Azure Synapse Analytics, går til Power BI sin semantiske modell. Avhengig av datatypen er det enten periodisk importert i minnet til Power BI eller direkte spørringer ved kjøring.

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

#### <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Filtre på øverste nivå

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

#### <a name="products"></a><a name="ProductsPage"></a> Produkter

- Salg
- Marg
- Returer

#### <a name="customers"></a><a name="CustomersPage"></a> Kunder

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
> Commerce-analyse (forhåndsversjon) er i forhåndsversjon i USA, Canada, Storbritannia, Europa, Sør-Øst-Asia, Øst-Asia, Australia og Japan. Hvis økonomi- og driftsmiljøet ditt finnes i noen av disse områdene, kan du aktivere denne funksjonen i miljøet ditt ved å bruke Microsoft Dynamics Lifecycle Services (LCS). Før du kan bruke denne funksjonen, kan du se [Konfigurere eksport til Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>Aktivere og konfigurere Commerce-analyse (forhåndsversjon)

Hvis du vil installere Commerce-analyse (forhåndsversjon), må du ha tillatelse til å opprette ressurser i et Azure-abonnement. Du må også ha tillatelse til å installere tilleggsprogrammet i LCS. 

Følg denne fremgangsmåten for å aktivere og konfigurere Commerce-analyse (forhåndsversjon).

1. [Aktivere og konfigurere tilleggsprogrammet Eksporter til Data Lake](#enableExportToDataLake).
1. [Installer og konfigurer et Azure Synapse workspace](#configureAzureSynapse).
1. [Legg til hemmeligheter i nøkkelhvelvet](#addSecrets).
1. [Aktivere og konfigurere Commerce-analyse (forhåndsversjon)](#enableCommerceAnalyticsAddin).
1. [Installer Power BI malappen](#powerbi).

### <a name="enable-and-configure-the-export-to-data-lake-add-in"></a><a name="enableExportToDataLake"></a>Aktivere og konfigurere tilleggsprogrammet Eksporter til Data Lake

> [!IMPORTANT]
> Når du konfigurerer tilleggsprogrammet Eksport til Data Lake, fjerner du merket for **Dataendringer i sanntid** på konfigurasjonssiden i tilleggsprogrammet Eksporter til Data Lake for å sikre at dataendringer i sanntid ikke aktiveres. Funksjonen **Dataendringer i sanntid** er i forhåndsversjon og støttes for øyeblikket ikke av Commerce-analyse. Hvis du aktiverer funksjonen, kan ikke Commerce-analyse behandle dataene i datasjøen, og det vises ingen data i de fleste Power BI-rapportene dine.

Commerce-analyse (forhåndsversjon) er avhengig av funksjonen Eksporter til Data Lake for å kunne eksportere Commerce Headquarters-data til Data Lake og holde dataene oppdatert. Før du konfigurerer Commerce-analyse (forhåndsversjon), må du aktivere og konfigurere eksport til Azure Data Lake ved å følge trinnene i [Konfigurere eksport til Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

Når du konfigurerer tilleggsprogrammet Eksporter til Data Lake, noterer du deg følgende informasjon fordi du må angi den senere:

- <a name="keyVault"></a>DNS-navnet (Domain Name System) på nøkkelhvelvet du angav.
- De hemmelige navnene du har oppgitt, og som inneholder program-ID-en og programhemmeligheten. Hvis du vil ha mer informasjon om mål, se [Legge til hemmeligheter i nøkkelhvelvet](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a>Installer og konfigurer et Azure Synapse workspace

Commerce-analyse (forhåndsversjon) krever at Synapse SQL ved behov klargjøres i Azure Synapse workspace. Hvis du vil installere og konfigurere et Azure Synapse workspace, gjør du følgende.

1. Installer et Azure Synapse workspace i Azure-abonnementet. Hvis du vil ha mer informasjon, kan du se [Hurtigstart: Opprette et Synapse-arbeidsområde](/azure/synapse-analytics/quickstart-create-workspace).
1. <a name="serverlessep"></a>Etter at arbeidsområdet er klargjort, åpner du ressursoversiktssiden og noterer deg verdien for **Serverløst SQL-sluttpunkt**. Du må lagre denne verdien i nøkkelhvelvet i neste del.
1. Velg koblingen **Åpne Synapse Studio** på oversiktssiden for å åpne Azure Synapse Studio for arbeidsområdet.
1. Velg **Administrer** på venstre meny. Du må kanskje velge utvidelseskoblingen på venstre meny for å kunne se menynavnene.
1. Velg **Tilgangskontroll** under **Sikkerhetsgruppe**. 
1. Velg **Legg til**.
1. Angi alternativene som beskrevet i følgende tabell, i ruten **Legg til rolletilordning**.

    | Alternativ | Verdi |
    |--------|-------|
    | Område | Velg **Arbeidsområde**. |
    | Rolle | Velg **Synapse SQL-administrator**.|
    | Velg bruker | Søk etter navnet på programmet du [opprettet under installasjonen av tilleggsprogrammet Eksporter til Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createapplication). Velg programmet når det vises i søkeresultatene. Programmet vises nå i delen **Valgte brukere, grupper eller tjenestekontohavere**. |

1. Velg **Bruk** for å fullføre rolletilordningen. Programmet får rettigheter som Synapse SQL-administrator. Det kan derfor opprette de nødvendige visningene under konfigurasjonen av LCS-tilleggsprogrammet Commerce-analyse (forhåndsversjon).

### <a name="add-secrets-to-the-key-vault"></a><a name="addSecrets"></a>Legge til hemmeligheter i nøkkelhvelvet

Du må legge til hemmelighetene som vises i tabellen nedenfor i det samme [nøkkelhvelvet](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createkeyvault) du brukte mens du konfigurerte tilleggsprogrammet Eksporter til Data Lake. For hver hemmelighet må du angi et hemmelig navn og den angitte verdien.

| Foreslått hemmelig navn | Hemmelig verdi | Eksempel på hemmelig verdi |
|---------|---------|---------|
| synapse-sql-server | Verdien for serverløst SQL-sluttpunkt som du noterte deg mens du [konfigurerte Azure Synapse workspace](#serverlessep). | `test-ondemand.sql.azuresynapse.net` |
| <a name="roUser"></a>readonly-sql-pwd | Passordet som skal angis for den skrivebeskyttede brukeren av SQL. Power BI-rapporten bruker dette passordet til å koble til serverløs SQL. Følg organisasjonens policyer for passord når du skal angi passord. | |

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a>Aktivere og konfigurere Commerce-analyse (forhåndsversjon)

Hvis du vil installere Commerce-analyse (forhåndsversjon) i LCS, må du være miljøadministrator i LCS for miljøet du planlegger å bruke.

Følg denne fremgangsmåten for å installere og konfigurere Commerce-analyse (forhåndsversjon).

1. Logg deg på [LCS](https://lcs.dynamics.com/), og gå til miljøet ditt.
2. På **Miljø**-siden i fanen **Miljøtillegg** velger du **Installer et nytt tillegg**.
3. Velg **Commerce-analyse (forhåndsversjon)** i dialogboksen.
4. Angi følgende informasjon i dialogboksen **Konfigurer tillegg**.

    | Opplysninger | Kilde | Eksempelverdi |
    |---|---|---|
    | Leier-ID for Azure Active Directory (Azure AD) | Logg deg på [Azure Portal](https://portal.azure.com/), og åpne **Azure Active Directory**-tjenesten. Deretter åpner du **Egenskaper**-siden og kopierer verdien i **Leier-ID**-feltet. | `72f988bf-0000-0000-00000-2d7cd011db47` |
    | DNS-navnet for Azure-nøkkelhvelvet | Oppgi DNS-navnet til nøkkelhvelvet. Du skal ha notert deg denne verdien mens du [konfigurerte tilleggsprogrammet Eksporter til Data Lake](#keyVault). | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Hemmelig navn som inneholder program-ID-en | Angi det hemmelige navnet som lagrer program-IDen. Du skal ha notert deg denne verdien mens du [konfigurerte tilleggsprogrammet Eksporter til Data Lake](#keyVault). | `app-id` |
    | Hemmelig navn som inneholder programhemmeligheten | Angi det hemmelige navnet på butikken som lagrer programhemmeligheten. Du skal ha notert deg denne verdien mens du [konfigurerte tilleggsprogrammet Eksporter til Data Lake](#keyVault). | `app-secret` |
    | Hemmelig navn som inneholder det serverløse SQL-sluttpunktet for Azure Synapse | Angi det hemmelige navnet der det serverløse SQL-sluttpunktet lagres. Du skal ha opprettet hemmeligheten mens du [la til hemmeligheter i nøkkelverdien](#addSecrets). | `synapse-sql-server` |
    | Hemmelig navn som inneholder passordet som skal angis for skrivebeskyttede brukere av SQL i Azure Synapse | Angi det hemmelige navnet som lagrer passordet som skal angis for den skrivebeskyttede brukeren av serverløs SQL. Denne brukeren blir opprettet for deg og skal brukes i Power BI-rapporten til å koble til den serverløse SQL-serveren. Du skal ha opprettet hemmeligheten mens du [la til hemmeligheter i nøkkelverdien](#addSecrets). | `readonly-sql-pwd` |

1. Godta betingelsene for tilbudet ved å merke av for boksen, og velg deretter **Installer**.

    Systemet installerer og konfigurerer Commerce-analyse (forhåndsversjon)-tillegget for miljøet. Denne prosessen kan ta noen minutter. Når installasjonen er fullført, skal **Commerce-analyse (forhåndsversjon)** vises på **Miljø**-siden, og statusen bør være **Installert**.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a>Installere Power BI malappen

Følg denne fremgangsmåten for å installere Power BI malappen for Commerce-analyse (forhåndsversjon).

1. Logg deg på [Power BI portalen](https://powerbi.microsoft.com/) ved hjelp av organisasjons-IDen.
1. Installer Power BI malappen for Commerce-analyse (forhåndsversjon) ved å gå til [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Du kan alternativt gå til [AppSource-siden for Dynamics 365 Commerce-analyse](https://appsource.microsoft.com/product/power-bi/dynamics-365-commerce.dydnamics-365-commerce-analytics) og velge **Få den nå**.
1. Hvis du installerer appen på nytt for første gang, kan du gå videre til trinn 5. Hvis du har installert den før, gjelder følgende alternativer for oppdatering av appen:

    - **Oppdater arbeidsområdet og appen**– Oppdater den eksisterende malappen, og overskriv de eksisterende appinnstillingene, for eksempel navn på appforekomst og tillatelseskonfigurasjoner.
    - **Oppdater bare innholdet i arbeidsområdet uten å oppdatere appen** – Oppdater den eksisterende malappen, men behold de eksisterende appinnstillingene. *Dette alternativet er det anbefalte alternativet for appoppdateringer.*
    - **Installer en annen kopi av appen i et nytt arbeidsområde** – Opprett et nytt arbeidsområde, og lag deretter en kopi av den eksisterende malappen i den. Det eksisterende arbeidsområdet blir stående intakt.

1. Velg ett av oppdateringsalternativene, og velg deretter **Installer**.
1. Åpne den installerte appen ved å velge **Apper** i ruten til venstre og deretter velge appen.
1. Koble appen til datakilden ved å velge **Koble til**. Hvis du har installert appen før, velger du **Koble til data**-koblingen på den gule meldingslinjen.
1. Angi følgende felt.

    | Felt | Verdi |
    |---|---|
    | Server | Angi det serverløse SQL-sluttpunktet du noterte deg etter at du [opprettet Azure Synapse workspace](#serverlessep). |
    | Database | Angi **CommerceAnalytics**. |
    | Språk | Velg en verdi i listen. Dette feltet brukes for lokaliserte produkt- og kategorinavn. Verdien skiller mellom store og små bokstaver. |
    | Datoområde | Velg en verdi i listen. Data for det valgte antall måneder blir importert til Power BI datasettet. Verdien du velger, påvirker størrelsen på datasettet og tidspunktet som kreves for synkroniseringen. |

1. Velg **Neste**. Når du blir bedt om å angi legitimasjonen for tilkobling til SQL-databasen for Azure Synapse, angir du feltverdiene som vist i følgende tabell.

    | Felt | Verdi |
    |---|---|
    | Godkjenningsmetode | Velg **Grunnleggende**. |
    | Brukernavn | Angi **reportreadonlyuser**. |
    | Passord | Angi passordet du [lagret for den skrivebeskyttede brukeren av SQL i nøkkelhvelvet](#roUser). |

1. Velg **Logg på og koble til**.
1. Vent til datasettet er oppdatert. Velg deretter **Rediger app** for å åpne App-arbeidsområdet, der du kan vise oppdateringsstatusen for datasettet. I App-arbeidsområdet kan du også velge å definere automatiske oppdateringsplaner for datasettet, administrere tillatelser og gi nytt navn til appforekomsten.

### <a name="privacy"></a><a name="privacy"></a>Tilgjengelighet

Personvernet er viktig for oss. Les [personvernerklæringen](https://go.microsoft.com/fwlink/?LinkId=521839) for å finne ut mer.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
