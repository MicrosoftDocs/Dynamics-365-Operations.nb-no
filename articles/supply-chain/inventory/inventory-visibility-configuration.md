---
title: Konfigurer Inventory Visibility
description: Denne artikkelen beskriver hvordan du konfigurerer Lagersynlighet.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 8d8fe042d7c56b86a5a7c92cc24480f573a2ea8a
ms.sourcegitcommit: 07ed6f04dcf92a2154777333651fefe3206a817a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2022
ms.locfileid: "9423576"
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
- [Eksempel på standard konfigurasjon](#default-configuration-sample)

## <a name="prerequisites"></a>Forutsetninger

Før du begynner, må du installere og konfigurere tillegget Lagersynlighet som beskrevet i [Installere og definere lagersynlighet](inventory-visibility-setup.md).

## <a name="the-configuration-page-of-the-inventory-visibility-app"></a><a name="configuration"></a>Konfigurasjonssiden for Lagersynlighet-appen

I Power Apps hjelper **Konfigurasjon** siden i [Lagersynlighet-appen](inventory-visibility-power-platform.md) deg med konfigurasjon av lagerbeholdning og konfigurasjon av ikke-forpliktende reservasjon. Når tillegget er installert, inkluderer standardkonfigurasjonen verdien fra Microsoft Dynamics 365 Supply Chain Management (datakilden `fno`). Du kan gå gjennom standardinnstillingene. I tillegg kan du, basert på forretningskravene og lagerposteringskravene i det eksterne systemet, endre konfigurasjonen for å standardisere hvordan lagerendringer kan posteres, organiseres og spørres i alle systemene. Resten av delene i denne artikkelen forklarer hvordan du bruker hver del av **Konfigurasjon**-siden.

Når konfigurasjonen er fullført, velger du **Oppdater konfigurasjon** i appen.

## <a name="enable-inventory-visibility-features-in-power-apps-feature-management"></a><a name="feature-switch"></a>Aktivere funksjoner for Lagersynlighet i Power Apps funksjonsbehandling

Tillegget for lagersynlighet legger til flere nye funksjoner i Power Apps installasjonen. Disse funksjonene er deaktivert som standard. Hvis du vil bruke dem, åpner du **Konfigurasjon**-siden og aktiverer deretter følgende funksjoner på fanen **Funksjonsbehandling** etter behov.

| Funksjonsbehandling-navn | Beskrivelse |
|---|---|
| *OnHandReservation* | Denne funksjonen lar deg opprette reserveringer, forbruke reserveringer og/eller avreservere angitte lagerantall ved hjelp av Lagersynlighet. Hvis du vil ha mer informasjon, kan du se [Lagersynlighetsreservasjoner](inventory-visibility-reservations.md). |
| *OnHandMostSpecificBackgroundService* | Denne funksjonen gir et lagersammendrag for produkter, sammen med alle dimensjoner. Lagersammendragsdataene synkroniseres periodisk fra Lagersynlighet. Standard synkroniseringsfrekvens er én gang hvert 15. minutt og kan angis så høyt som én gang hvert 5. minutt. For mer informasjon, se [Lagersammendrag](inventory-visibility-power-platform.md#inventory-summary). |
| *OnhandChangeSchedule* | Denne valgfrie funksjonen aktiverer endringsplanen for lagerbeholdning og er tilgjengelig ATP-funksjoner (tilgjengelig for ordre). Hvis du vil ha mer informasjon, kan du se [Tidsplan for lagerendringer i Lagersynlighet og leveringskapasitet](inventory-visibility-available-to-promise.md). |
| *Tilordning* | Ved hjelp av denne valgfrie funksjonen kan lagersynlighet gi mulighet for lagerbeskyttelse (ringorganisering) og oversalgskontroll. Hvis du vil ha mer informasjon, kan du se [Lagertildeling for lagersynlighet](inventory-visibility-allocation.md). |
| *Aktiver lagervarer i lagersynlighet* | Denne valgfrie funksjonen gjør det mulig for Lagersynlighet å støtte varer som er aktivert for Warehouse Management-prosesser (WMS). Hvis du vil ha mer informasjon, kan du se [Støtte i Lagersynlighet for WMS-varer](inventory-visibility-whs-support.md). |

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Finn endepunkt for tjeneste

Hvis du ikke kjenner til det korrekte endepunktet for Lagersynlighet-tjenesten, åpner du **Konfigurasjon**-siden i Power Apps og velger deretter **Vis endepunkt for tjeneste** øverst til høyre. Siden vil vise det riktige endepunktet for tjenesten.

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Konfigurasjon av datakilde

Hver datakilde representerer et system som dataene kommer fra. Eksempler på datakildenavn inkluderer `fno` (som betyr "økonomi- og driftsapper for Dynamics 365 Finance") og `pos` (som betyr "salgssted"). Som standard er Supply Chain Management definert som en standard datakilde (`fno`) i Lagersynlighet.

> [!NOTE]
> Datakilden `fno` er reservert for Supply Chain Management. Hvis tillegget for lagersynlighet er integrert med et Supply Chain Management-miljø, anbefaler vi at du ikke sletter konfigurasjoner som er relatert til `fno` i datakilden.

Følg fremgangsmåten nedenfor for å legge til en datakilde.

1. Logg deg på Power Apps-miljøet, og åpne **Lagersynlighet**.
1. Åpne **Konfigurasjon**-siden.
1. På **Datakilde**-fanen velger du **Ny datakilde** for å legge til en datakilde.

> [!NOTE]
> Når du legger til en datakilde, må du validere datakildenavnet, de fysiske målene og dimensjonstilordningene før du oppdaterer konfigurasjonen for Lagersynlighet-tjenesten. Du kan ikke endre disse innstillingene etter at du har valgt **Oppdater konfigurasjon**.

Konfigurasjonen for datakilden omfatter følgende deler:

- Dimensjoner (dimensjonstilordning)
- Fysiske mål
- Beregnede mål

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Dimensjoner (dimensjonstilordning)

Formålet med dimensjonskonfigurasjonen er å standardisere integreringen med flere systemer for postering av hendelser og spørringer, basert på kombinasjoner av dimensjoner. Lagersynlighet har en liste over basisdimensjoner som kan tilordnes fra dimensjonene til datakilden. 33 dimensjoner er tilgjengelige for tilordning.

- Hvis du bruker Supply Chain Management som én av datakildene, tilordnes 13 dimensjoner til standarddimensjonene i Supply Chain Management. 12 andre dimensjoner (`inventDimension1` til `inventDimension12`) tilordnes til egendefinerte dimensjoner i Supply Chain Management. De gjenværende åtte dimensjonene er utvidede dimensjoner som du kan tilordne til eksterne datakilder.
- Hvis du ikke bruker Supply Chain Management som en av datakildene, kan du fritt tilordne dimensjonene. Følgende tabell viser den fullstendige listen over tilgjengelige dimensjoner.

> [!NOTE]
> Hvis dimensjonen din ikke er angitt i standarddimensjonslisten, og du bruker en ekstern datakilde, anbefaler vi at du bruker `ExtendedDimension1` til `ExtendedDimension8` for å utføre tilordningen.

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
> Lagerdimensjoner (egendefinerte) kan være reservert for Supply Chain Management. Du kan i så fall bruke de utvidede dimensjonene i stedet.

Eksterne systemer kan få tilgang til Lagersynlighet via sine RESTful-API-er. For integreringen kan du bruke Lagersynlighet til å konfigurere den _eksterne datakilden_ og tilordningen fra de _eksterne dimensjonene_ til _basisdimensjonene_. Her er et eksempel på en dimensjonstilordningstabell.

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
1. På **Datakilde**-fanen i delen **Dimensjonstilordninger** velger du **Legg til** for å legge til dimensjonstilordninger.
    ![Legg til dimensjonstilordninger](media/inventory-visibility-dimension-mapping.png "Legg til dimensjonstilordninger")

1. I **Dimensjonsnavn**-feltet angir du kildedimensjonen.
1. I feltet **Til basisdimensjon** velger du dimensjonen i Lagersynlighet som du vil tilordne.
1. Velg **Lagre**.

Hvis datakilden for eksempel inneholder en produktfargedimensjon, kan du tilordne den til basisdimensjonen `ColorId` for å legge til en egendefinert `ProductColor`-dimensjon i `exterchannel`-datakilden. Deretter tilordnes den til `ColorId`-basisdimensjonen.

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
1. På **Datakilde**-fanen i delen **Fysiske mål** velger du **Legg til**, angir et navn på kildemålet og lagrer endringene.

### <a name="calculated-measures"></a>Beregnede mål

Du kan bruke Lagersynlighet til å spørre både på fysiske lagermål og *egendefinerte beregnede mål*. Beregnede mål gir en tilpasset beregningsformel som består av en kombinasjon av fysiske mål. Med denne funksjonaliteten kan du definere et sett med fysiske mål som skal legges til, eller et sett med fysiske mål som skal trekkes fra, for å kunne lage det egendefinerte målet.

> [!IMPORTANT]
> Et beregnet mål er en sammensetning av fysiske mål. Formelen kan bare inneholde fysiske mål uten duplikater, ikke beregnede mål.

Ved hjelp av konfigurasjonen kan du definere et sett med modifikatorer som legges til eller trekkes fra for å få totalt akkumulert utdataantall.

Hvis du vil konfigurere et egendefinert beregnet mål, gjør du følgende.

1. Logg deg på Power Apps-miljøet, og åpne **Lagersynlighet**.
1. Åpne **Konfigurasjon**-siden.
1. På fanen **Beregnet mål** velger du **Nytt beregnet mål** for å legge til et beregnet mål.
1. Angi følgende felt for det nye beregnede målet:

    - **Navn på nytt beregnet mål** – Angi navnet på det beregnede målet.
    - **Datakilde** – Velg datakilden som er knyttet til den nye modifikatoren. Spørringssystemet er en datakilde.

1. Velg **Legg til** for å legge til en modifikator for det nye beregnede målet.
1. Angi følgende felter for den nye modifikatoren:

    - **Modifikator** – Velg modifikatortypen (*Addisjon* eller *Subtraksjon*).
    - **Datakilde** – Velg datakilden der målet som angir modifikatorverdien, skal finnes.
    - **Mål** – Velg navnet på målet (fra den valgte datakilden) som angir verdien for modifikatoren.

1. Gjenta trinn 5 til og med 6 til du har lagt til alle de nødvendige modifikatorene.
1. Velg **Lagre**.

Du har for eksempel følgende spørringsresultat.

```json
[
    {
        "productId": "T-shirt",
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
            "externalchannel": {
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
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `scheduled` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `reserved` | `Subtraction` |

Når denne beregningsformelen brukes, vil det nye resultatet av spørringen inneholde det tilpassede målet.

```json
[
    {
        "productId": "T-shirt",
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
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
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

Lagersynlighet gir fleksibilitet ved å la deg konfigurere _indekser_ for å forbedre ytelsen til spørringene. Disse indeksene er basert på en dimensjon eller en kombinasjon av dimensjoner. En indeks består av et *settnummer*, en *dimensjon* og et *hierarki*, som definert i følgende tabell.

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

| Element | ColorId | SizeId | StyleId | Antall |
|---|---|---|---|---|
| T-skjorte | Svart | Liten | Bred | 1 |
| T-skjorte | Svart | Liten | Vanlig | 2 |
| T-skjorte | Svart | Stor | Bred | 3 |
| T-skjorte | Svart | Stor | Vanlig | 4 |
| T-skjorte | Rød | Liten | Bred | 5 |
| T-skjorte | Rød | Liten | Vanlig | 6 |
| T-skjorte | Rød | Stor | Vanlig | 7 |

Tabellen nedenfor viser hvordan indekshierarkiet er satt opp.

| Settnummer | Dimensjon | Hierarki |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Ved hjelp av indeksen kan du utføre spørringer på lagerbeholdningen på følgende måter:

- `()` – Gruppert av alle

    - T-skjorte, 28

- `(ColorId)` – Gruppert av `ColorId`

    - T-skjorte, svart, 10
    - T-skjorte, rød, 18

- `(ColorId, SizeId)` – Gruppert etter kombinasjonen av `ColorId` og `SizeId`

    - T-skjorte, svart, liten, 3
    - T-skjorte, svart, stor, 7
    - T-skjorte, rød, liten, 11
    - T-skjorte, rød, stor, 7

- `(ColorId, SizeId, StyleId)` – Gruppert etter kombinasjonen av `ColorId`, `SizeId` og `StyleId`

    - T-skjorte, svart, liten, bred, 1
    - T-skjorte, svart, liten, vanlig, 2
    - T-skjorte, svart, stor, bred, 3
    - T-skjorte, svart, stor, vanlig, 4
    - T-skjorte, rød, liten, bred, 5
    - T-skjorte, rød, liten, vanlig, 6
    - T-skjorte, rød, stor, vanlig, 7

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Reservasjonskonfigurasjon (valgfritt)

Reservasjonskonfigurasjon er nødvendig hvis du vil bruke funksjonen for ikke-forpliktende reservasjon. Konfigurasjonen består av to grunnleggende deler:

- Tilordning av ikke-forpliktende reservasjon
- Hierarki for ikke-forpliktende reservasjon

### <a name="soft-reservation-mapping"></a>Tilordning av ikke-forpliktende reservasjon

Når du foretar en reservasjon, ønsker du kanskje å vite om lagerbeholdningen for øyeblikket er tilgjengelig for reservasjon. Valideringen er koblet til et beregnet mål som representerer en beregningsformel for en kombinasjon av fysiske mål.

Når du definerer tilordningen fra det fysiske målet til det beregnede målet, kan Lagersynlighet-tjenesten automatisk validere tilgjengelighet for reservering, basert på det fysiske målet.

Før du kan sette opp denne tilordningen, må de fysiske målene, de beregnede målene og datakildene være definert på fanene **Datakilde** og **Beregnet mål** på **Konfigurasjon**-siden i Power Apps (som beskrevet tidligere i denne artikkelen).

Følg denne fremgangsmåten for å definere tilordningen for ikke-forpliktende reservasjon.

1. Definer det fysiske målet som fungerer som mål for ikke-forpliktende reservasjon (for eksempel `SoftReservOrdered`).
1. På fanen **Beregnet mål** på **Konfigurasjon**-siden definerer du det beregnede målet *Tilgjengelig for reservasjon* (TFR) som inneholder AFR-beregningsformelen som du ønsker å tilordne til det fysiske målet. Du kan for eksempel definere `AvailableToReserve` (tilgjengelig for reservasjon), slik at det er tilordnet det tidligere definerte fysiske målet `SoftReservOrdered`. På denne måten kan du finne ut hvilke antall som har beholdningsstatusen `SoftReservOrdered`, og som er tilgjengelige for reservering. Tabellen nedenfor viser TFR-beregningsformelen.

    | Beregningstype | Datakilde | Fysisk mål |
    |---|---|---|
    | Tillegg | `fno` | `AvailPhysical` |
    | Tillegg | `pos` | `Inbound` |
    | Subtraksjon | `pos` | `Outbound` |
    | Subtraksjon | `iv` | `SoftReservOrdered` |

    Vi anbefaler at du definerer det beregnede målet slik at det inneholder det fysiske målet som reservasjonsmålet er basert på. På denne måten påvirkes det beregnede målingsantallet av reservasjonsmålingsantallet. I dette eksemplet bør derfor den `AvailableToReserve` beregnede målingen for `iv` datakilden inneholde det `SoftReservOrdered` fysiske målet fra `iv` som en komponent.

1. Åpne **Konfigurasjon**-siden.
1. På fanen **Tilordning av ikke-forpliktende reservasjon** konfigurerer du tilordningen fra det fysiske målet til det beregnede målet. For det forrige eksemplet kan du bruke følgende innstillinger til å tilordne `AvailableToReserve` til det tidligere definerte fysiske målet `SoftReservOrdered`.

    | Datakilde for fysisk mål | Fysisk mål | Tilgjengelig for datakilde for reservasjon | Tilgjengelig for beregnet mål for reservasjon |
    |---|---|---|---|
    | `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > Hvis ikke kan redigere fanen **Tilordning av ikke-forpliktende reservasjon**, må du kanskje aktivere funksjonen *OnHandReservation* på **Funksjonsbehandling**-fanen.

Når du nå reserverer i `SoftReservOrdered`, vil Lagersynlighet automatisk finne `AvailableToReserve`, og den relaterte beregningsformelen brukes til å validere reservasjonen.

Du har for eksempel følgende lagerbeholdning i Lagersynlighet.

```json
{
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservOrdered": 90
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

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservOrdered`  
= 70 + 50 – 20 – 90  
= 10

Hvis du prøver å gjøre reservasjoner på `iv.SoftReservOrdered` og antallet er mindre enn eller lik `AvailableToReserve` (10), kan du derfor gjøre reservasjonen.

> [!NOTE]
> Når du kaller reservasjons-API, kan du styre reservasjonsvalideringen ved å angi den boolske `ifCheckAvailForReserv` parameteren i forespørselsteksten. Verdien `True` betyr at valideringen kreves, mens en verdi å `False` betyr at valideringen ikke er nødvendig. Standardverdien er `True`.

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

## <a name="complete-and-update-the-configuration"></a>Fullfør og oppdater konfigurasjonen

Når du har fullført konfigurasjonen, må du aktivere alle endringene i Lagersynlighet. Du aktiverer endringer ved å velge **Oppdater konfigurasjon** øverst til høyre på **Konfigurasjon**-siden i Power Apps.

Første gang du velger **Oppdater konfigurasjon**, ber systemet deg om legitimasjon.

- **Klient-ID** – ID-en for Azure-app som du opprettet for Lagersynlighet.
- **Leier-ID** – ID-en til Azure-leieren.
- **Klienthemmelighet** – Hemmeligheten for Azure-app som du opprettet for Lagersynlighet.

Når du har logget deg på, blir konfigurasjonen oppdatert i Lagersynlighet-tjenesten.

> [!NOTE]
> Du må validere datakildenavnet, de fysiske målene og dimensjonstilordningene før du oppdaterer konfigurasjonen for Lagersynlighet-tjenesten. Du kan ikke endre disse innstillingene etter at du har valgt **Oppdater konfigurasjon**.

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

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

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
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Reservasjonshierarki

Følgende tabell viser standard reservasjonshierarki.

| Basisdimensjon | Hierarki |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |
| `BatchId` | 6 |
| `SerialId` | 7 |
| `StatusId` | 8 |
| `LicensePlateId` | 9 |
| `WMSLocationId` | 10 |
| `WMSPalletId` | 11 |
| `ConfigId` | 12 |
| `VersionId` | 13 |
| `CustomDimension1` | 14 |
| `CustomDimension2` | 15 |
| `CustomDimension3` | 16 |
| `CustomDimension4` | 17 |
| `CustomDimension5` | 18 |
| `CustomDimension6` | 19 |
| `CustomDimension7` | 20 |
| `CustomDimension8` | 21 |
| `CustomDimension9` | 22 |
| `CustomDimension10` | 23 |
| `CustomDimension11` | 24 |
| `CustomDimension12` | 25 |
| `ExtendedDimension1` | 26 |
| `ExtendedDimension2` | 27 |
| `ExtendedDimension3` | 28 |
| `ExtendedDimension4` | 29 |
| `ExtendedDimension5` | 30 |
| `ExtendedDimension6` | 31 |
| `ExtendedDimension7` | 32 |
| `ExtendedDimension8` | 33 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

