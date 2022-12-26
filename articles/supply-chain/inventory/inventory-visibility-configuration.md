---
title: Konfigurer Inventory Visibility
description: Denne artikkelen beskriver hvordan du konfigurerer Lagersynlighet.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 2a368535c9644e174d1a2460ac0891c9dc1b1b3f
ms.sourcegitcommit: 44f0b4ef8d74c86b5c5040be37981e32eb43e1a8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/14/2022
ms.locfileid: "9850030"
---
# <a name="configure-inventory-visibility"></a>Konfigurer Inventory Visibility

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer lagersynlighet ved hjelp av tillegget for lagersynlighet i Power Apps.

## <a name="introduction"></a><a name="introduction"></a>Innledning

Før du begynner å arbeide med Lagersynlighet, må du fullføre følgende konfigurasjon som beskrevet i denne artikkelen:

- [Konfigurasjon av datakilde](#data-source-configuration)
- [Partisjonskonfigurasjon](#partition-configuration)
- [Konfigurasjon av produktindekshierarki](#index-configuration)
- [Reservasjonskonfigurasjon (valgfritt)](#reservation-configuration)
- [Forhåndslastingskonfigurasjon for spørring (valgfritt)](#query-preload-configuration)
- [Eksempel på standard konfigurasjon](#default-configuration-sample)

## <a name="prerequisites"></a>Nødvendig programvare

Før du begynner, må du installere og konfigurere tillegget Lagersynlighet som beskrevet i [Installere og definere lagersynlighet](inventory-visibility-setup.md).

## <a name="the-configuration-page-of-the-inventory-visibility-app"></a><a name="configuration"></a>Konfigurasjonssiden for Lagersynlighet-appen

I Power Apps hjelper **Konfigurasjon** siden i [Lagersynlighet-appen](inventory-visibility-power-platform.md) deg med konfigurasjon av lagerbeholdning og konfigurasjon av ikke-forpliktende reservasjon. Når tillegget er installert, inkluderer standardkonfigurasjonen verdien fra Microsoft Dynamics 365 Supply Chain Management (datakilden `fno`). Du kan gå gjennom standardinnstillingene. I tillegg kan du, basert på forretningskravene og lagerposteringskravene i det eksterne systemet, endre konfigurasjonen for å standardisere hvordan lagerendringer kan posteres, organiseres og spørres i alle systemene. Resten av delene i artikkelen forklarer hvordan du bruker hver del av **Konfigurasjon**-siden.

Når konfigurasjonen er fullført, velger du **Oppdater konfigurasjon** i appen.

## <a name="enable-inventory-visibility-features-in-power-apps-feature-management"></a><a name="feature-switch"></a>Aktivere funksjoner for Lagersynlighet i Power Apps funksjonsbehandling

Tillegget for lagersynlighet legger til flere nye funksjoner i Power Apps installasjonen. Disse funksjonene er deaktivert som standard. Hvis du vil bruke dem, åpner du **Konfigurasjon**-siden og aktiverer deretter følgende funksjoner på fanen **Funksjonsbehandling** etter behov.

| Funksjonsbehandling-navn | Beskrivelse |
|---|---|
| *OnHandReservation* | Denne funksjonen lar deg opprette reserveringer, forbruke reserveringer og/eller avreservere angitte lagerantall ved hjelp av Lagersynlighet. Hvis du vil ha mer informasjon, kan du se [Lagersynlighetsreservasjoner](inventory-visibility-reservations.md). |
| *OnHandMostSpecificBackgroundService* | Denne funksjonen gir et lagersammendrag for produkter, sammen med alle dimensjoner. Lagersammendragsdataene synkroniseres periodisk fra Lagersynlighet. Standard synkroniseringsfrekvens er én gang hvert 15. minutt og kan angis så høyt som én gang hvert 5. minutt. For mer informasjon, se [Lagersammendrag](inventory-visibility-power-platform.md#inventory-summary). |
| *OnHandIndexQueryPreloadBackgroundService* | Denne funksjonen henter og lagrer regelmessig et sett med samledata for lagerbeholdning basert på de forhåndskonfigurerte dimensjonene. Det gir et lagersammendrag som bare omfatter de dimensjonene som er relevante for den daglige forretningen, og som er kompatible med varer som er aktivert for lagerstyringsprosesser (WMS). Hvis du vil ha mer informasjon, kan du se [Slå på og konfigurer forhåndslastede spørringer for lagerbeholdning](#query-preload-configuration) og [Forhåndslast en strømlinjeformet spørring for lagerbeholdning](inventory-visibility-power-platform.md#preload-streamlined-onhand-query). |
| *OnhandChangeSchedule* | Denne valgfrie funksjonen aktiverer endringsplanen for lagerbeholdning og er tilgjengelig ATP-funksjoner (tilgjengelig for ordre). Hvis du vil ha mer informasjon, kan du se [Tidsplan for lagerendringer i Lagersynlighet og leveringskapasitet](inventory-visibility-available-to-promise.md). |
| *Tilordning* | Ved hjelp av denne valgfrie funksjonen kan lagersynlighet gi mulighet for lagerbeskyttelse (ringorganisering) og oversalgskontroll. Hvis du vil ha mer informasjon, kan du se [Lagertildeling for lagersynlighet](inventory-visibility-allocation.md). |
| *Aktiver lagervarer i lagersynlighet* | Denne valgfrie funksjonen gjør det mulig for Lagersynlighet å støtte varer som er aktivert for Warehouse Management-prosesser (WMS). Hvis du vil ha mer informasjon, kan du se [Støtte i Lagersynlighet for WMS-varer](inventory-visibility-whs-support.md). |

> [!IMPORTANT]
> Det anbefales at du bruker enten *OnHandIndexQueryPreloadBackgroundService*-funksjonen eller *OnHandMostSpecificBackgroundService*-funksjonen, ikke begge. Hvis du aktiverer begge funksjonene, påvirker det ytelsen.

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Finn endepunkt for tjeneste

Hvis du ikke kjenner til det korrekte endepunktet for Lagersynlighet-tjenesten, åpner du **Konfigurasjon**-siden i Power Apps og velger deretter **Vis serviceordredetaljer** øverst til høyre. Siden vil vise det riktige endepunktet for tjenesten. Du kan også finne sluttpunktet i Microsoft Dynamics Lifecycle Services, som beskrevet i [Finn sluttpunktet i henhold til Lifecycle Services-miljøet](inventory-visibility-api.md#endpoint-lcs).

> [!NOTE]
> Bruk av feil sluttpunkt kan forårsake en mislykket lagersynlighetsinstallasjon og feil når Supply Chain Management synkroniseres med Lagersynlighet. Hvis du ikke er sikker på hva sluttpunktet er, bør du ta kontakt med systemadministratoren. Sluttpunkt-URLer bruker følgende format:
>
> `https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Konfigurasjon av datakilde

Hver datakilde representerer et system som dataene kommer fra. Eksempler på datakildenavn inkluderer `fno` (som tilsvarer Supply Chain Management) og `pos` (som betyr "salgssted"). Som standard er Supply Chain Management definert som en standard datakilde (`fno`) i Lagersynlighet.

> [!NOTE]
> Datakilden `fno` er reservert for Supply Chain Management. Hvis Tillegg for lagersynlighet er integrert med et Supply Chain Management-miljø, anbefaler vi at du ikke sletter konfigurasjoner som er relatert til `fno` i datakilden.

Følg fremgangsmåten nedenfor for å legge til en datakilde.

1. Logg deg på Power Apps-miljøet, og åpne **Lagersynlighet**.
1. Åpne **Konfigurasjon**-siden.
1. I fanen **Datakilde** velger du **Ny datakilde** for å legge til en datakilde (for eksempel `ecommerce` en annen meningsfull datakilde-ID).

> [!NOTE]
> Når du legger til en datakilde, må du validere datakildenavnet, de fysiske målene og dimensjonstilordningene før du oppdaterer konfigurasjonen for Lagersynlighet-tjenesten. Du kan ikke endre disse innstillingene etter at du har valgt **Oppdater konfigurasjon**.

Konfigurasjonen for datakilden omfatter følgende deler:

- Dimensjoner (dimensjonstilordning)
- Fysiske mål
- Beregnede mål

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Dimensjoner (dimensjonstilordning)

Formålet med dimensjonskonfigurasjonen er å standardisere integreringen med flere systemer for postering av hendelser og spørringer, basert på kombinasjoner av dimensjoner. Lagersynlighet har en liste over basisdimensjoner som kan tilordnes fra dimensjonene til datakilden. 33 dimensjoner er tilgjengelige for tilordning.

- Hvis du bruker Supply Chain Management som én av datakildene, tilordnes 13 dimensjoner til standarddimensjonene i Supply Chain Management som standard. De 12 andre dimensjonene (`inventDimension1` til `inventDimension12`) tilordnes også til egendefinerte dimensjoner i Supply Chain Management. De gjenværende åtte dimensjonene (`ExtendedDimension1` til `ExtendedDimension8`) er utvidede dimensjoner som du kan tilordne til eksterne datakilder.
- Hvis du ikke bruker Supply Chain Management som en av datakildene, kan du fritt tilordne dimensjonene. Følgende tabell viser den fullstendige listen over tilgjengelige dimensjoner.

> [!NOTE]
> Hvis du bruker Supply Chain Management og endrer standarddimensjonstilordninger mellom Supply Chain Management og Lagersynlighet, vil ikke den endrede dimensjonen synkronisere data. Hvis dimensjonen din ikke er angitt i standarddimensjonslisten, og du bruker en ekstern datakilde, anbefaler vi derfor at du bruker `ExtendedDimension1` til `ExtendedDimension8` for å utføre tilordningen.

| Dimensjonstype | Basisdimensjon |
|---|---|
| Produkt | `ColorId` |
| Produkt | `SizeId` |
| Produkt | `StyleId` |
| Produkt | `ConfigId` |
| Sporing | `BatchId` |
| Sporing | `SerialId` |
| Lokasjon | `LocationId` |
| Lokasjon | `SiteId` |
| Beholdningsstatus | `StatusId` |
| Lagerspesifikk | `WMSLocationId` |
| Lagerspesifikk | `WMSPalletId` |
| Lagerspesifikk | `LicensePlateId` |
| Annet | `VersionId` |
| Lager (egendefinert) | `InventDimension1` til `InventDimension12` |
| Utvidelse | `ExtendedDimension1` til `ExtendedDimension8` |
| System | `Empty` |

> [!NOTE]
> Dimensjonstypenen som er oppført i den forrige tabellen, er bare for referanse. Du trenger ikke definere dem i Lagersynlighet.
>
> Lagerdimensjonene (egendefinerte) kan være reservert for Supply Chain Management. Du kan i så fall bruke de utvidede dimensjonene i stedet.

Eksterne systemer kan få tilgang til Lagersynlighet via sine RESTful-API-er. For integreringen kan du bruke Lagersynlighet til å konfigurere den *eksterne datakilden* og tilordningen fra de *eksterne dimensjonene* til *basisdimensjonene*. Her er et eksempel på en dimensjonstilordningstabell.

| Ekstern dimensjon | Basisdimensjon |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Ved å konfigurere en dimensjonstilordning kan du sende de eksterne dimensjonene direkte til Lagersynlighet. Lagersynlighet konverterer deretter automatisk eksterne dimensjoner til basisdimensjoner.

Følg fremgangsmåten nedenfor for å legge til dimensjonstilordninger.

1. Logg deg på Power Apps-miljøet, og åpne **Lagersynlighet**.
1. Åpne **Konfigurasjon**-siden.
1. I fanen **Datakilde** velger du datakilden der du vil gjøre dimensjonstilordningen. I delen **Dimensjonstilordninger** velger du **Legg til** for å legge til dimensjonstilordninger.

    ![Legg til dimensjonstilordninger](media/inventory-visibility-dimension-mapping.png "Legg til dimensjonstilordninger")

1. I **Dimensjonsnavn**-feltet angir du kildedimensjonen.
1. I feltet **Til basisdimensjon** velger du dimensjonen i Lagersynlighet som du vil tilordne.
1. Velg **Lagre**.

Du har for eksempel allerede opprettet en datakilde med navnet `ecommerce`, og den inneholder en produktfargedimensjon. Hvis du vil gjøre tilordningen, kan du først legge til `ProductColor` til **Dimensjonsnavn**-feltet i `ecommerce`-datakilden og deretter velge `ColorId` i feltet **Til basisdimensjon**.

### <a name="physical-measures"></a><a name="data-source-configuration-physical-measures"></a>Fysiske mål

Når en datakilde posterer en lagerendring til Lagersynlighet, posteres denne endringen ved hjelp av *fysiske mål*. Fysiske mål endrer antallet og gjenspeiler lagerstatusen. Du kan definere dine egne fysiske mål basert på dine krav. Spørringer kan være basert på de fysiske målene.

Lagersynlighet gir en liste over standard fysiske mål som er koblet til Supply Chain Management (datakilden `fno`). Disse standard fysiske målene hentes fra lagertransaksjonsstatusene på siden **Beholdningsliste** i Supply Chain Management (**Lagerstyring \> Forespørsler og rapporter \> Beholdningsliste**). Følgende tabell inneholder et eksempel på fysiske mål.

| Navn på fysisk mål | beskrivelse |
|---|---|
| `NotSpecified` | Ikke angitt |
| `Arrived` | Ankommet |
| `AvailOrdered` | Tilgjengelig bestilt |
| `AvailPhysical` | Fysisk tilgjengelig |
| `Deducted` | Fratrukket |
| `OnOrder` | I bestilling |
| `Ordered` | Bestilt |
| `PhysicalInvent` | Aktuell beholdning |
| `Picked` | Plukket |
| `PostedQty` | Postert antall |
| `QuotationIssue` | Tilbud avgang |
| `QuotationReceipt` | Tilbud tilgang |
| `Received` | Mottatt |
| `Registered` | Registrert |
| `ReservOrdered` | Reservert av bestilt |
| `ReservPhysical` | Fysisk reservert |

Hvis datakilden er Supply Chain Management, trenger du ikke å opprette standard fysiske mål på nytt. For eksterne datakilder kan du imidlertid opprette nye fysiske mål ved å følge disse trinnene.

1. Logg deg på Power Apps-miljøet, og åpne **Lagersynlighet**.
1. Åpne **Konfigurasjon**-siden.
1. I kategorien **Datakilde** velger du datakilden du vil legge til fysiske mål i (for eksempel `ecommerce`-datakilden). Deretter, i delen **Fysiske målinger**, velber du **Legg til** og angir målnavnet (for eksempel `Returned` hvis du vil registrere returnerte antall i denne datakilden til Lagersynlighet). Lagre endringene.

### <a name="extended-dimensions"></a>Utvidede dimensjoner

Kunder som vil bruke eksterne datakilder i datakilden, kan ta dra nytte av utvidelsen som Dynamics 365 tilbyr, ved å opprette [klasseutvidelser](../../fin-ops-core/dev-itpro/extensibility/class-extensions.md) for `InventOnHandChangeEventDimensionSet`- og `InventInventoryDataServiceBatchJobTask`-klassene.

Pass på at du synkroniserer med databasen etter at du har opprettet tilleggene, slik at de egendefinerte feltene kan legges til i `InventSum`-tabellen. Deretter kan du se Dimensjoner-delen tidligere i denne artikkelen for å tildele egendefinerte dimensjoner til hvilken som helst av de åtte utvidede dimensjonene i `BaseDimensions` i Lager.

> [!NOTE] 
> Hvis du vil ha mer informasjon om å opprette utvidelser, kan du se [Startside for utvidbarhet](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md).

### <a name="calculated-measures"></a>Beregnede mål

Du kan bruke Lagersynlighet til å spørre både på fysiske lagermål og *egendefinerte beregnede mål*. Beregnede mål gir en tilpasset beregningsformel som består av en kombinasjon av fysiske mål. Med denne funksjonaliteten kan du definere et sett med fysiske mål som skal legges til, eller et sett med fysiske mål som skal trekkes fra, for å kunne lage det egendefinerte målet.

> [!IMPORTANT]
> Et beregnet mål er en sammensetning av fysiske mål. Formelen kan bare inneholde fysiske mål uten duplikater, ikke beregnede mål.

Ved hjelp av konfigurasjonen kan du definere et sett med kalkulerte målformler dom inkluderer modifikatorer for addisjon eller subtraksjon for å få totalt akkumulert utdataantall.

Hvis du vil konfigurere et egendefinert beregnet mål, gjør du følgende.

1. Logg deg på Power Apps-miljøet, og åpne **Lagersynlighet**.
1. Åpne **Konfigurasjon**-siden.
1. På fanen **Beregnet mål** velger du **Nytt beregnet mål** for å legge til et beregnet mål.
1. Angi følgende felt for det nye beregnede målet:

    - **Navn på nytt beregnet mål** – Angi navnet på det beregnede målet.
    - **Datakilde** – Velg datakilden som du vil inkludere det nye beregnede målet i. Spørringssystemet er en datakilde.

1. Velg **Legg til** for å legge til en modifikator for det nye beregnede målet.
1. Angi følgende felter for den nye modifikatoren:

    - **Modifikator** – Velg modifikatortypen (*Addisjon* eller *Subtraksjon*).
    - **Datakilde** – Velg datakilden der målet som angir modifikatorverdien, skal finnes.
    - **Mål** – Velg navnet på målet (fra den valgte datakilden) som angir verdien for modifikatoren.

1. Gjenta trinn 5 til 6 til du har lagt til alle de nødvendige modifikatorene og fullført formelen for de beregnede målene.
1. Velg **Lagre**.

Et motefirma opererer for eksempel på tvers av tre datakilder:

- `pos`– Tilsvarer butikkanalen.
- `fno` – Tilsvarer Supply Chain Management.
- `ecommerce` – Tilsvarer webkanalen.

Uten beregnede mål får du kanskje følgende spørringsresultat, som viser lagerantall under hvert forhåndskonfigurerte fysiske mål når du spør etter produkt D0002 (kabinett) for område 1, lager 11 og `ColorID`-dimensjonsverdi `Red`. Du har imidlertid ikke oversikt over totalen som er tilgjengelig for reservasjonsantall i hele datakildene.

```json
[
    {
        "productId": "D0002",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "ecommerce": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]
```

Deretter konfigurerer du et beregnet mål med navnet `MyCustomAvailableforReservation`, som vist i følgende tabell. Dette beregnede målet vil bli forbrukt av forbrukssystemet.

| Forbrukssystem | Beregnet mål | Datakilde | Fysisk mål | Beregningstype |
|---|---|---|---|---|
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `received` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `scheduled` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `issued` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `reserved` | `Subtraction` |

Når denne beregningsformelen brukes, vil det nye resultatet av spørringen inneholde det tilpassede målet.

```json
[
    {
        "productId": "D0002",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "ecommerce": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CrossChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

`MyCustomAvailableforReservation`-utdataene, basert på beregningsinnstillingen i de egendefinerte målene, er 100 + 50 – 10 + 80 – 20 + 90 + 30 – 60 – 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Partisjonskonfigurasjon

Partisjonskonfigurasjonen består for øyeblikket av to basisdimensjoner (`SiteId` og `LocationId`) som angir hvordan dataene skal distribueres. Operasjoner under samme partisjon kan levere høyere ytelse til lavere kostnad. Følgende tabell viser standard partisjonskonfigurasjon som tillegget for lagersynlighet gir.

| Basisdimensjon | Hierarki |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

Løsningen inkluderer denne partisjonskonfigurasjonen som standard. Derfor *trenger du ikke å omberegne manuelt*.

> [!IMPORTANT]
> Ikke tilpass standard partisjonskonfigurasjon. Hvis du sletter eller endrer den, vil du sannsynligvis forårsake en uventet feil.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Konfigurasjon av produktindekshierarki

Som oftest vil ikke spørringen om lagerbeholdning bare være på det høyeste "total"-nivået. I stedet bør du også se resultater som samles opp basert på lagerdimensjonene.

Lagersynlighet gir fleksibilitet ved å la deg konfigurere *indekser* for å forbedre ytelsen til spørringene. Disse indeksene er basert på en dimensjon eller en kombinasjon av dimensjoner. En indeks består av et *settnummer*, en *dimensjon* og et *hierarki*, som definert i følgende tabell.

| Navn | beskrivelse |
|---|---|
| Settnummer | Dimensjoner som tilhører samme sett (indeks), blir gruppert sammen, og det samme settnummeret tilordnes dem. |
| Dimensjon | Basisdimensjoner som resultatet av spørringen samles opp på. |
| Hierarki | Hierarkiet lar deg øke ytelsen til bestemte dimensjonskombinasjoner når de brukes i parametere for filter og grupperingsspørringer. Hvis du for eksempel definerer et dimensjonssett med en hierarkisekvensen `(ColorId, SizeId, StyleId)`, kan systemet raskere behandle spørringer som er knyttet til fire dimensjonskombinasjoner. Den første kombinasjonen er tom, den andre er `(ColorId)`, den tredje er `(ColorId, SizeId)` og den fjerde er `(ColorId, SizeId, StyleId)`. Hastigheten økes ikke for andre kombinasjoner. Filtre er ikke begrenset av rekkefølge, men må være i disse dimensjonene hvis du vil forbedre ytelsen deres. Hvis du vil ha mer informasjon, kan du se eksemplet nedenfor. |

Gjør følgende for å konfigurere produkthierarkiindeksen.

1. Logg deg på Power Apps-miljøet, og åpne **Lagersynlighet**.
1. Åpne **Konfigurasjon**-siden.
1. På fanen **Produkthierarkiindeks** i delen **Dimensjonstilordninger** velger du **Legg til** for å legge til dimensjonstilordninger.
1. Som standard vises det en liste over indekser. Hvis du vil endre en eksisterende indeks, velger du **Rediger** eller **Legg til** i delen for den relevante indeksen. Hvis du vil opprette et nytt indekssett, velger du **Nytt indekssett**. For hver rad i hvert indekssett velger du fra listen over basisdimensjoner i **Dimensjon**-feltet. Verdier for følgende felter genereres automatisk:

    - **Settnummer** – Dimensjoner som tilhører samme gruppe (indeks), blir gruppert sammen, og det samme settnummeret tilordnes dem.
    - **Hierarki** – Hierarkiet øker ytelsen til bestemte dimensjonskombinasjoner når de brukes i parametere for filter og grupperingsspørringer.

> [!TIP]
> Her er noen tips du kan tenke på når du definerer indekshierarkiet:
>
> - Basisdimensjoner som er definert i partisjonskonfigurasjonen, bør ikke defineres i indekskonfigurasjoner. Hvis en basisdimensjon er definert på nytt i indekskonfigurasjonen, kan du ikke utføre spørringer for denne indeksen.
> - Hvis du bare trenger å spørre etter lager som samles opp av alle dimensjonskombinasjonene, kan du definere en enkelt indeks som inneholder basisdimensjonen `Empty`.

### <a name="example"></a>Eksempel

Denne delen inneholder et eksempel som viser hvordan hierarkiet fungerer.

Følgende tabell inneholder en liste over tilgjengelig beholdning for dette eksemplet.

| Vare | ColorId | SizeId | StyleId | Antall |
|---|---|---|---|---|
| D0002 | Svart | Liten | Bred | 1 |
| D0002 | Svart | Liten | Vanlig | 2 |
| D0002 | Svart | Stor | Bred | 3 |
| D0002 | Svart | Stor | Vanlig | 4 |
| D0002 | Rød | Liten | Bred | 5 |
| D0002 | Rød | Liten | Vanlig | 6 |
| D0002 | Rød | Stor | Vanlig | 7 |

Tabellen nedenfor viser hvordan indekshierarkiet er satt opp.

| Settnummer | Dimensjon | Hierarki |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Ved hjelp av indeksen kan du utføre spørringer på lagerbeholdningen på følgende måter:

- `()` – Gruppert av alle

    - D0002, 28

- `(ColorId)` – Gruppert av `ColorId`

    - D0002, Svart, 10
    - D0002, Rød, 18

- `(ColorId, SizeId)` – Gruppert etter kombinasjonen av `ColorId` og `SizeId`

    - D0002, Svart, Liten, 3
    - D0002, Svart, Stor, 7
    - D0002, Rød, Liten, 11
    - D0002, Rød, Stor, 7

- `(ColorId, SizeId, StyleId)` – Gruppert etter kombinasjonen av `ColorId`, `SizeId` og `StyleId`

    - D0002, svart, liten, bred, 1
    - D0002, svart, liten, vanlig, 2
    - D0002, svart, stor, bred, 3
    - D0002, svart, stor, vanlig, 4
    - D0002, rød, liten, bred, 5
    - D0002, rød, liten, vanlig, 6
    - D0002, rød, stor, vanlig, 7

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Reservasjonskonfigurasjon (valgfritt)

Reservasjonskonfigurasjon er nødvendig hvis du vil bruke funksjonen for ikke-forpliktende reservasjon. Konfigurasjonen består av to grunnleggende deler:

- Tilordning av ikke-forpliktende reservasjon
- Hierarki for ikke-forpliktende reservasjon

### <a name="soft-reservation-mapping"></a>Tilordning av ikke-forpliktende reservasjon

Når du foretar en reservasjon, ønsker du kanskje å vite om lagerbeholdningen for øyeblikket er tilgjengelig for reservasjon. Valideringen er koblet til et beregnet mål som representerer en beregningsformel for en kombinasjon av fysiske mål.

Når du definerer tilordningen fra det fysiske målet til det beregnede målet, kan Lagersynlighet-tjenesten automatisk validere tilgjengelighet for reservering, basert på det fysiske målet.

Før du kan sette opp denne tilordningen, må de fysiske målene, de beregnede målene og datakildene være definert på fanene **Datakilde** og **Beregnet mål** på **Konfigurasjon**-siden i Power Apps (som beskrevet tidligere i denne artikkelen).

Følg denne fremgangsmåten for å definere tilordningen for ikke-forpliktende reservasjon.

1. Definer det fysiske målet som fungerer som mål for ikke-forpliktende reservasjon (for eksempel `SoftReservPhysical`).
1. På fanen **Beregnet mål** på **Konfigurasjon**-siden definerer du det beregnede målet *Tilgjengelig for reservasjon* (TFR) som inneholder AFR-beregningsformelen som du ønsker å tilordne til det fysiske målet. Du kan for eksempel definere `AvailableToReserve` (tilgjengelig for reservasjon), slik at det er tilordnet det tidligere definerte fysiske målet `SoftReservPhysical`. På denne måten kan du finne ut hvilke antall som har beholdningsstatusen `SoftReservPhysical`, og som er tilgjengelige for reservering. Tabellen nedenfor viser TFR-beregningsformelen.

    | Beregningstype | Datakilde | Fysisk mål |
    |---|---|---|
    | Tillegg | `fno` | `AvailPhysical` |
    | Tillegg | `pos` | `Inbound` |
    | Subtraksjon | `pos` | `Outbound` |
    | Subtraksjon | `iv` | `SoftReservPhysical` |

    Vi anbefaler at du definerer det beregnede målet slik at det inneholder det fysiske målet som reservasjonsmålet er basert på. På denne måten påvirkes det beregnede målingsantallet av reservasjonsmålingsantallet. I dette eksemplet bør derfor den `AvailableToReserve` beregnede målingen for `iv` datakilden inneholde det `SoftReservPhysical` fysiske målet fra `iv` som en komponent.

1. Åpne **Konfigurasjon**-siden.
1. På fanen **Tilordning av ikke-forpliktende reservasjon** konfigurerer du tilordningen fra det fysiske målet til det beregnede målet. For det forrige eksemplet kan du bruke følgende innstillinger til å tilordne `AvailableToReserve` til det tidligere definerte fysiske målet `SoftReservPhysical`.

    | Datakilde for fysisk mål | Fysisk mål | Tilgjengelig for datakilde for reservasjon | Tilgjengelig for beregnet mål for reservasjon |
    |---|---|---|---|
    | `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > Hvis ikke kan redigere fanen **Tilordning av ikke-forpliktende reservasjon**, må du kanskje aktivere funksjonen *OnHandReservation* på **Funksjonsbehandling**-fanen.

Når du nå reserverer i `SoftReservPhysical`, vil Lagersynlighet automatisk finne `AvailableToReserve`, og den relaterte beregningsformelen brukes til å validere reservasjonen.

Du har for eksempel følgende lagerbeholdning i Lagersynlighet.

```json
{
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservPhysical": 90
        },
        "fno": {
            "availphysical": 70.0,
        },
        "pos": {
            "inbound": 50.0,
            "outbound": 20.0
        }
    }
}
```

I dette tilfellet gjelder følgende beregning:

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservPhysical`  
= 70 + 50 – 20 – 90  
= 10

Hvis du prøver å gjøre reservasjoner på `iv.SoftReservPhysical` og antallet er mindre enn eller lik `AvailableToReserve` (10), vil den ikke-forpliktende forespørselen bli vellykket.

> [!NOTE]
> Når du kaller reservasjons-API, kan du styre reservasjonsvalideringen ved å angi den boolske `ifCheckAvailForReserv` parameteren i forespørselsteksten. `True` betyr at valideringen kreves, mens `False` betyr at valideringen ikke er nødvendig (selv om du kan ende opp med et negativt `AvailableToReserve`-antall, vil systemet likevel tillate at du gjør en ikke-forpliktende reservasjon). Standardverdien er `True`.

### <a name="soft-reservation-hierarchy"></a>Hierarki for ikke-forpliktende reservasjon

Reservasjonshierarkiet beskriver serien med dimensjoner som må angis når det opprettes reservasjoner. Det fungerer på samme måte som produktindekshierarkiet fungerer for lagerbeholdningsspørringer.

Reservasjonshierarkiet er uavhengig av produktindekshierarkiet. Denne uavhengigheten lar deg implementere kategoriadministrasjon der brukere kan dele inn dimensjonene i detaljer for å angi krav til å lage mer presise reservasjoner. Mykt reservasjonshierarki bør inneholde `SiteId` og `LocationId` som komponenter fordi de konstruerer partisjonskonfigurasjonen. Når du gjør reservasjonen, må du angi en partisjon for produktet.

Her er et eksempel på et hierarki for ikke-forpliktende reservasjon.

| Basisdimensjon | Hierarki |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

I dette eksemplet kan du reservere i følgende dimensjonssekvenser. Når du gjør reservasjonen, må du angi en partisjon for produktet. Derfor er `(SiteId, LocationId)` det grunnleggende hierarkiet du kan bruke.

- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

En gyldig dimensjonssekvens skal følge reservasjonshierarkiet, dimensjonen for dimensjon. Hierarkisekvensen `(SiteId, LocationId, SizeId)` er for eksempel ikke gyldig, fordi `ColorId` mangler.

## <a name="available-to-promise-configuration-optional"></a>Konfigurasjon av tilgjengelig for ordre (valgfritt)

Du kan konfigurere Lagersynlighet slik at du kan planlegge fremtidige endringer i lagerbeholdningen og beregne ATP-antall (tilgjengelig for ordre). ATP er antallet av en vare som er tilgjengelig og kan loves til en kunde i løpet av den neste perioden. Bruk av denne beregningen kan øke kapasiteten for innfrielse av bestillinger betydelig. Hvis du vil bruke denne funksjonen, må du aktivere den på fanen **Funksjonsbehandling** og deretter konfigurere den på fanen **ATP-innstilling**. Hvis du vil ha mer informasjon, kan du se [Tidsplaner for lagerendringer i Lagersynlighet og leveringskapasitet](inventory-visibility-available-to-promise.md).

## <a name="turn-on-and-configure-preloaded-on-hand-queries-optional"></a><a name="query-preload-configuration"></a>Slå på og konfigurer forhåndslastede lagerbeholdningsspørringer (valgfritt)

Lagersynlighet kan regelmessig hente og lagre et sett med samledata for lagerbeholdning basert på de forhåndskonfigurerte dimensjonene. Dette gir følgende fordeler:

- En renere visning som lagrer et lagersammendrag som bare omfatter de dimensjonene som er relevante for den daglige virksomheten.
- Et lagersammendrag som er kompatibelt med varer aktivert for lagerstyringsprosesser (WMS).

Se [Forhåndslast en strømlinjeformet lagerbeholdningsspørring](inventory-visibility-power-platform.md#preload-streamlined-onhand-query) for mer informasjon om hvordan du arbeider med denne funksjonen etter at du har konfigurert den.

> [!IMPORTANT]
> Det anbefales at du bruker enten *OnHandIndexQueryPreloadBackgroundService*-funksjonen eller *OnHandMostSpecificBackgroundService*-funksjonen, ikke begge. Hvis du aktiverer begge funksjonene, påvirker det ytelsen.

Gjør følgende for å konfigurere funksjonen:

1. Logg deg på PowerApp for lagersynlighet.
1. Gå til **Konfigurasjon \> Funksjonsbehandling og innstillinger**.
1. Hvis funksjonen *OnHandIndexQueryPreloadBackgroundService* allerede er aktivert, anbefaler vi at du deaktiverer den nå fordi oppryddingsprosessen kan ta svært lang tid å fullføre. Du må slå den på igjen senere i denne prosedyren.
1. Åpne fanen **Innstillinger for forhåndslasting**.
1. I delen **Trinn 1: Rydd opp i forhåndslastingslager** velger du **Rydd** for å rydde opp i databasen og gjøre den klar til å godta de nye innstillingene for gruppe.
1. I delen **Trinn 2: Konfigurer grupper etter verdier** i feltet **Grupper resultat etter** angir du en kommadelt liste over feltnavn som spørringsresultatene skal grupperes etter. Når du har data i lagringsdatabasen for forhåndslasting, kan du ikke endre denne innstillingen før du rydder i databasen, som beskrevet i forrige trinn.
1. Gå til **Konfigurasjon \> Funksjonsbehandling og innstillinger**.
1. Slå på funksjonen *OnHandIndexQueryPreloadBackgroundService*.
1. Velg **Oppdater konfigurasjon** øverst til høyre på **Konfigurasjon**-siden for å ta i bruk endringene.

## <a name="complete-and-update-the-configuration"></a>Fullfør og oppdater konfigurasjonen

Når du har fullført konfigurasjonen, må du aktivere alle endringene i Lagersynlighet. Følg denne fremgangsmåten for å gjøre endringer.

1. I Power Apps, på siden **Konfigurasjon**, velger du **Oppdater konfigurasjon** øverst til høyre. 
1. Systemet ber om påloggingslegitimasjon. Angi følgende verdier:

    - **Klient-ID** – ID-en for Azure-app som du opprettet for Lagersynlighet.
    - **Leier-ID** – ID-en til Azure-leieren.
    - **Klienthemmelighet** – Hemmeligheten for Azure-app som du opprettet for Lagersynlighet.

    Hvis du vil ha mer informasjon om denne legitimasjonen og hvordan du finner dem, kan du se [Installer og definer Lagersynlighet](inventory-visibility-setup.md).

    > [!IMPORTANT]
    > Du må validere datakildenavnet, de fysiske målene og dimensjonstilordningene før du oppdaterer konfigurasjonen. Du kan ikke endre disse innstillingene etter at du har oppdatert den.

1. Velg **Oppdater konfigurasjon** på nytt etter pålogging. Systemet bruker innstillingene dine og viser hva som er endret.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Eksempel på standard konfigurasjon

I løpet av initialiseringsstadiet definerer Lagersynlighet en standardkonfigurasjon, som er forklart her. Du kan endre denne konfigurasjonen etter behov.

### <a name="data-source-configuration"></a>Konfigurasjon av datakilde

#### <a name="configuration-of-the-iv-data-source"></a>Konfigurasjon av datakilden iv

Denne delen beskriver hvordan datakilden `iv` konfigureres.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>Fysiske mål konfigurert for datakilden "iv"

Følgende fysiske mål er konfigurert for datakilden `iv`:

- `Ordered`
- `SoftReservPhysical`
- `SoftReservOrdered`
- `ReservOrdered`
- `ReservPhysical`

##### <a name="orderedtotal-calculated-measure"></a>Beregnet mål for OrderedTotal

Det beregnede målet `OrderedTotal` konfigureres for datakilden `iv` som vist i følgende tabell.

| Beregningstype | Datakilde | Fysisk mål |
|---|---|---|
| Tillegg | `fno` | `Ordered` |
| Tillegg | `fno` | `Arrived` |
| Tillegg | `iv` | `Ordered` |

##### <a name="onhand-calculated-measure"></a>Beregnet mål OnHand

Det beregnede målet `OnHand` konfigureres for datakilden `iv` som vist i følgende tabell.

| Beregningstype | Datakilde | Fysisk mål |
|---|---|---|
| Tillegg | `fno` | `PhysicalInvent` |
| Tillegg | `iom` | `OnHand` |
| Tillegg | `erp` | `Unrestricted` |
| Tillegg | `erp` | `QualityInspection` |
| Tillegg | `pos` | `PosInbound` |
| Subtraksjon | `pos` | `PosOutbound` |

##### <a name="reservedtotal-calculated-measure"></a>Beregnet mål for ReservedTotal

Det beregnede målet `ReservedTotal` konfigureres for datakilden `iv` som vist i følgende tabell.

| Beregningstype | Datakilde | Fysisk mål |
|---|---|---|
| Tillegg | `fno` | `ReservPhysical` |
| Tillegg | `fno` | `ReservOrdered` |
| Tillegg | `iv` | `SoftReservPhysical` |
| Tillegg | `iv` | `SoftReservOrdered` |
| Tillegg | `iv` | `ReservPhysical` |
| Tillegg | `iv` | `ReservOrdered` |

##### <a name="softreserved-calculated-measure"></a>Beregnet mål for SoftReserved

Det beregnede målet `SoftReserved` konfigureres for datakilden `iv` som vist i følgende tabell.

| Beregningstype | Datakilde | Fysisk mål |
|---|---|---|
| Tillegg | `iv` | `SoftReservPhysical` |
| Tillegg | `iv` | `SoftReservOrdered` |

##### <a name="hardreserved-calculated-measure"></a>Beregnet mål for HardReserved

Det beregnede målet `HardReserved` konfigureres for datakilden `iv` som vist i følgende tabell.

| Beregningstype | Datakilde | Fysisk mål |
|---|---|---|
| Tillegg | `fno` | `ReservPhysical` |
| Tillegg | `fno` | `ReservOrdered` |
| Tillegg | `iv` | `ReservPhysical` |
| Tillegg | `iv` | `ReservOrdered` |

##### <a name="openorder-calculated-measure"></a>Beregnet mål for OpenOrder

Det beregnede målet `OpenOrder` konfigureres for datakilden `iv` som vist i følgende tabell.

| Beregningstype | Datakilde | Fysisk mål |
|---|---|---|
| Tillegg | `fno` | `OnOrder` |
| Tillegg | `iom` | `OnOrder` |

##### <a name="onhandavailable-calculated-measure"></a>Beregnet mål for OnHandAvailable

Det beregnede målet `OnHandAvailable` konfigureres for datakilden `iv` som vist i følgende tabell.

| Beregningstype | Datakilde | Fysisk mål |
|---|---|---|
| Tillegg | `fno` | `PhysicalInvent` |
| Tillegg | `iom` | `OnHand` |
| Tillegg | `erp` | `Unrestricted` |
| Tillegg | `erp` | `QualityInspection` |
| Tillegg | `pos` | `PosInbound` |
| Subtraksjon | `fno` | `ReservPhysical` |
| Subtraksjon | `iv` | `SoftReservPhysical` |
| Subtraksjon | `pos` | `PosOutbound` |

##### <a name="availabletoreserve-calculated-measure"></a>Beregnet mål for AvailableToReserve

Det beregnede målet `AvailableToReserve` konfigureres for datakilden `iv` som vist i følgende tabell.

| Beregningstype | Datakilde | Fysisk mål |
|---|---|---|
| Tillegg | `fno` | `PhysicalInvent` |
| Tillegg | `iom` | `OnHand` |
| Tillegg | `erp` | `Unrestricted` |
| Tillegg | `erp` | `QualityInspection` |
| Tillegg | `pos` | `PosInbound` |
| Tillegg | `fno` | `Ordered` |
| Tillegg | `fno` | `Arrived` |
| Tillegg | `iv` | `Ordered` |
| Subtraksjon | `fno` | `ReservPhysical` |
| Subtraksjon | `fno` | `ReservOrdered` |
| Subtraksjon | `iv` | `SoftReservPhysical` |
| Subtraksjon | `iv` | `SoftReservOrdered` |
| Subtraksjon | `iv` | `ReservPhysical` |
| Subtraksjon | `iv` | `ReservOrdered` |
| Subtraksjon | `pos` | `PosOutbound` |

##### <a name="inventorysupply-calculated-measure"></a>Beregnet mål for InventorySupply

Det beregnede målet `InventorySupply` konfigureres for datakilden `iv` som vist i følgende tabell.

| Beregningstype | Datakilde | Fysisk mål |
|---|---|---|
| Tillegg | `fno` | `Ordered` |
| Tillegg | `fno` | `Arrived` |
| Tillegg | `iv` | `Ordered` |
| Tillegg | `fno` | `PhysicalInvent` |
| Tillegg | `iom` | `OnHand` |
| Tillegg | `erp` | `Unrestricted` |
| Tillegg | `erp` | `QualityInspection` |
| Tillegg | `pos` | `PosInbound` |
| Subtraksjon | `pos` | `PosOutbound` |

##### <a name="inventorydemand-calculated-measure"></a>Beregnet mål for InventoryDemand

Det beregnede målet `InventoryDemand` konfigureres for datakilden `iv` som vist i følgende tabell.

| Beregningstype | Datakilde | Fysisk mål |
|---|---|---|
| Tillegg | `fno` | `OnOrder` |
| Tillegg | `iom` | `OnOrder` |
| Tillegg | `iv` | `SoftReservPhysical` |
| Tillegg | `iv` | `SoftReservOrdered` |
| Tillegg | `fno` | `ReservPhysical` |
| Tillegg | `fno` | `ReservOrdered` |
| Tillegg | `iv` | `ReservPhysical` |
| Tillegg | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>Konfigurasjon av datakilden "fno"

Denne delen beskriver hvordan datakilden `fno` konfigureres.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>Dimensjonstilordninger for datakilden "fno"

Dimensjonstilordningene som er oppført i tabellen nedenfor, er konfigurert for datakilden `fno`.

| Ekstern dimensjon | Basisdimensjon |
|---|---|
| `InventBatchId` | `BatchId` |
| `InventColorId` | `ColorId` |
| `InventLocationId` | `LocationId` |
| `InventSerialId` | `SerialId` |
| `InventSiteId` | `SiteId` |
| `InventSizeId` | `SizeId` |
| `InventStatusId` | `StatusId` |
| `InventStyleId` | `StyleId` |
| `LicensePlateId` | `LicensePlateId` |
| `WMSLocationId` | `WMSLocationId` |
| `WMSPalletId` | `WMSPalletId` |
| `ConfigId` | `ConfigId` |
| `InventVersionId` | `VersionId` |
| `InventDimension1` | `CustomDimension1` |
| `InventDimension2` | `CustomDimension2` |
| `InventDimension3` | `CustomDimension3` |
| `InventDimension4` | `CustomDimension4` |
| `InventDimension5` | `CustomDimension5` |
| `InventDimension6` | `CustomDimension6` |
| `InventDimension7` | `CustomDimension7` |
| `InventDimension8` | `CustomDimension8` |
| `InventDimension9` | `CustomDimension9` |
| `InventDimension10` | `CustomDimension10` |
| `InventDimension11` | `CustomDimension11` |
| `InventDimension12` | `CustomDimension12` |

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>Fysiske mål konfigurert for datakilden "fno"

Følgende fysiske mål er konfigurert for datakilden `fno`:

- `Arrived`
- `PhysicalInvent`
- `ReservPhysical`
- `onorder`
- `notspecified`
- `availordered`
- `availphysical`
- `picked`
- `postedqty`
- `quotationreceipt`
- `received`
- `ordered`
- `ReservOrdered`

#### <a name="configuration-of-the-pos-data-source"></a>Konfigurasjon av datakilden "pos"

Denne delen beskriver hvordan datakilden `pos` konfigureres.

##### <a name="physical-measures-for-the-pos-data-source"></a>Fysiske mål for datakilden "pos"

Følgende fysiske mål er konfigurert for datakilden `pos`:

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>Beregnet mål for AvailQuantity

Det beregnede målet `AvailQuantity` konfigureres for datakilden `pos` som vist i følgende tabell.

| Beregningstype | Datakilde | Fysisk mål |
|---|---|---|
| Tillegg | `fno` | `AvailPhysical` |
| Tillegg | `pos` | `PosInbound` |
| Subtraksjon | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>Konfigurasjon av datakilden "iom"

Følgende fysiske mål er konfigurert for datakilden `iom` (Intelligent Order Management):

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>Konfigurasjon av datakilden "erp"

Følgende fysiske mål er konfigurert for datakilden `erp` (Enterprise Resource Planning):

- `Unrestricted`
- `QualityInspection`

### <a name="partition-configuration"></a>Partisjonskonfigurasjon

Følgende tabell viser standard partisjonskonfigurasjon.

| Basisdimensjon | Hierarki |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

### <a name="index-configuration"></a>Indekskonfigurasjon

Følgende tabell viser standard indekskonfigurasjon.

| Settnummer | Dimensjon | Hierarki |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

### <a name="reservation-configuration"></a>Reservasjonskonfigurasjon

Denne delen beskriver standard reservasjonskonfigurasjon.

#### <a name="reservation-mapping"></a>Reservasjonstilordning

Følgende tabell viser standard reservasjonstilordning.

| Datakilde for fysisk mål | Fysisk mål | Tilgjengelig for datakilde for reservasjon | Tilgjengelig for beregnet mål for reservasjon |
|---|---|---|---|
| `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Reservasjonshierarki

Følgende tabell viser standard reservasjonshierarki.

| Basisdimensjon | Hierarki |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
