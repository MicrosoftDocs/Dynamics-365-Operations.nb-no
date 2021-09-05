---
title: Appen Lagersynlighet
description: Dette emnet beskriver hvordan du bruker Lagersynlighet-appen.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: cc09dd82547ec42041889e9a96662cd17549a3ea
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345008"
---
# <a name="inventory-visibility-app"></a>Appen Lagersynlighet

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Dette emnet beskriver hvordan du bruker Lagersynlighet-appen.

Lagersynlighet er en modelldrevet app for visualisering. Appen inneholder tre sider: **Konfigurasjon**, **Driftssynlighet** og **Lagersammendrag**. Den har følgende egenskaper:

- Det har et brukergrensesnitt for konfigurasjon av lagerbeholdning og konfigurasjon av ikke-forpliktende reservasjon.
- Den støtter spørringer av lagerbeholdning i sanntid for forskjellige dimensjonskombinasjoner.
- Den har et grensesnitt for postering av reservasjonsforespørsler.
- Den har en tilpasset visning av lagerbeholdningen for produkter sammen med alle dimensjoner.

## <a name="prerequisites"></a>Forutsetninger

Før du begynner, må du installere og konfigurere tillegget Lagersynlighet som beskrevet i [Konfigurasjon av Lagersynlighet](inventory-visibility-setup.md).

## <a name="configuration"></a><a name="configuration"></a>Konfigurasjon

**Konfigurasjon**-siden hjelper deg med konfigurasjon av lagerbeholdning og konfigurasjon av ikke-forpliktende reservasjon. Når tillegget er installert, inkluderer standardkonfigurasjonen verdien fra Microsoft Dynamics 365 Supply Chain Management (datakilden `fno`). Du kan gå gjennom standardinnstillingen. I tillegg kan du, basert på forretningskravene og lagerposteringskravene i det eksterne systemet, endre konfigurasjonen i [Dataverse](/powerapps/maker/common-data-service/data-platform-intro) for å standardisere hvordan lagerendringer kan posteres, organiseres og spørres i alle systemene.

### <a name="define-data-sources"></a>Definer datakilder

Du definerer hver *datakilde* du vil integrere med Lagersynlighet. Lagersynlighet støtter integrasjon med ulike datakilder, for eksempel POS-systemet (salgssted), Supply Chain Management og andre eksterne systemer. Som standard er Supply Chain Management definert som en standard datakilde (`fno`) i Lagersynlighet.

Følg fremgangsmåten nedenfor for å legge til en datakilde.

1. Logg deg på Power Apps-miljøet, og åpne **Lagersynlighet**.
1. Åpne **Konfigurasjon**-siden.
1. På **Datakilde**-fanen velger du **Ny datakilde** for å legge til en datakilde.

> [!NOTE]
> Når du legger til en datakilde, må du validere datakildenavnet, de fysiske målene og dimensjonstilordningene før du oppdaterer konfigurasjonen for Lagersynlighet-tjenesten. Du kan ikke endre disse innstillingene etter at du har valgt **Oppdater konfigurasjon**.

### <a name="set-up-dimension-mappings"></a>Definer dimensjonstilordninger

Lagersynlighet har en liste over basisdimensjoner som kan tilordnes fra dimensjonene til datakilden. 33 dimensjoner er tilgjengelige for tilordning.

- Hvis du bruker Supply Chain Management som én av datakildene, tilordnes 13 dimensjoner til standarddimensjonene i Supply Chain Management. 12 andre dimensjoner (`inventDimension1` til `inventDimension12`) tilordnes til egendefinerte dimensjoner i Supply Chain Management. De gjenværende åtte dimensjonene er utvidede dimensjoner som du kan tilordne til eksterne datakilder.
- Hvis du ikke bruker Supply Chain Management som en av datakildene, kan du fritt tilordne dimensjonene. Følgende tabell viser den fullstendige listen over tilgjengelige dimensjoner.

> [!NOTE]
> Hvis dimensjonen din ikke er angitt i standarddimensjonslisten, og du bruker en ekstern datakilde, anbefaler vi at du bruker `ExtendedDimension1` til `ExtendedDimension8` for å utføre tilordningen.

| Dimensjonstype | Dimensjonsnavn |
|---|---|
| Produkt | `ColorId` |
| Produkt | `SizeId` |
| Produkt | `StyleId` |
| Produkt | `ConfigId` |
| Sporing | `BatchId` |
| Sporing | `SerialId` |
| Lokasjon | `LocationId` |
| Lokasjon | `SiteId` |
| Lagerstatus | `StatusId` |
| Lagerspesifikk | `WMSLocationId` |
| Lagerspesifikk | `WMSPalletId` |
| Lagerspesifikk | `LicensePlateId` |
| Annet | `VersionId` |
| Lager (egendefinert) | `InventDimension1` til `InventDimension12` |
| Annet | `ExtendedDimension1` til `ExtendedDimension8` |

Følg fremgangsmåten nedenfor for å legge til dimensjonstilordninger.

1. Logg deg på Power Apps-miljøet, og åpne **Lagersynlighet**.
1. Åpne **Konfigurasjon**-siden.
1. På **Datakilde**-fanen i delen **Dimensjonstilordninger** velger du **Legg til** for å legge til dimensjonstilordninger.
1. I **Dimensjonsnavn**-feltet angir du kildedimensjonen.
1. I feltet **Til basisdimensjon** velger du dimensjonen i Lagersynlighet som du vil tilordne.
1. Velg **Lagre**.

![Legg til dimensjonstilordninger](media/inventory-visibility-dimension-mapping.png "Legg til dimensjonstilordninger")

Hvis datakilden for eksempel inneholder en produktfargedimensjon, kan du tilordne den til basisdimensjonen `ColorId` for å legge til en egendefinert `ProductColor`-dimensjon i `exterchannel`-datakilden. Deretter tilordnes den til `ColorId`-basisdimensjonen.

## <a name="create-a-physical-measure"></a>Opprett et fysisk mål

Når en datakilde posterer en lagerendring til Lagersynlighet, posteres denne endringen ved hjelp av *fysiske mål*. Fysiske mål er modifikatorer som gjenspeiler de summerte lagertransaksjonsstatusene. Spørringer kan være basert på de fysiske målene.

Lagersynlighet inneholder en liste over standard fysiske mål. Disse standard fysiske målene hentes fra lagertransaksjonsstatusene på siden **Beholdningsliste** i Supply Chain Management (**Lagerstyring \> Forespørsler og rapporter \> Beholdningsliste**).

| Modifikator | Navn |
|---|---|
| `PhysicalInvent` | Aktuell beholdning |
| `ReservPhysical` | Fysisk reservert |
| `AvailPhysical` | Fysisk tilgjengelig |
| `ReservOrdered` | Reservert av bestilt |
| `PostedQty` | Postert antall |
| `Deducted` | Fratrukket |
| `Picked` | Plukket |
| `Received` | Mottatt |
| `Registered` | Registrert |
| `Arrived` | Ankommet |
| `Ordered` | Bestilt |
| `OnOrder` | I ordre/bestilling |
| `QuotationReceipt` | Tilbudskvittering |
| `QuotationIssue` | Tilbud avgang |

Hvis datakilden er Supply Chain Management, trenger du ikke å opprette standard fysiske mål på nytt. For eksterne datakilder kan du imidlertid opprette nye fysiske mål ved å følge disse trinnene.

1. Logg deg på Power Apps-miljøet, og åpne **Lagersynlighet**.
1. Åpne **Konfigurasjon**-siden.
1. På **Datakilde**-fanen i delen **Fysiske mål** velger du **Legg til**, angir et navn på kildemålet og lagrer endringene.

## <a name="define-the-product-hierarchy-index"></a>Definer produkthierarkiindeksen

Når du definerer akkumulerte dimensjonsgrupper, kan du bruke Lagersynlighet til å spørre på lagerbeholdningsstatus. I Lagersynlighet kalles hver dimensjonsgruppe en *indeks*. Hver indeks tilsvarer et settnummer. Du kan bestemme hvilke dimensjoner som skal brukes til å definere indekseringen, basert på måten du vil utføre spørringer på i Lagersynlighet.

Gjør følgende for å konfigurere produkthierarkiindeksen.

1. Logg deg på Power Apps-miljøet, og åpne **Lagersynlighet**.
1. Åpne **Konfigurasjon**-siden.
1. På fanen **Produkthierarkiindeks** i delen **Dimensjonstilordninger** velger du **Legg til** for å legge til dimensjonstilordninger.
1. Som standard vises det en liste over indekser. Hvis du vil endre en eksisterende indeks, velger du **Rediger** eller **Legg til** i delen for den relevante indeksen. Hvis du vil opprette et nytt indekssett, velger du **Nytt indekssett**. For hver rad i hvert indekssett velger du fra listen over basisdimensjoner i **Dimensjon**-feltet. Verdier for følgende felter genereres automatisk:

    - **Settnummer** – Dimensjoner som tilhører samme gruppe (indeks), blir gruppert sammen, og det samme settnummeret tilordnes dem.
    - **Hierarki** – Hierarkiet brukes til å definere dimensjonskombinasjonene som støttes, som det kan spørres om i en dimensjonsgruppe (indeks). Hvis du for eksempel definerer en dimensjonsgruppe som har hierarkisekvensen *Stil*, *Farge* og *Størrelse*, støtter systemet resultatet av tre spørringsgrupper. Den første gruppen er kun stil. Den andre gruppen er en kombinasjon av stil og farge. Og den tredje gruppen er en kombinasjon av stil, farge og størrelse. De andre kombinasjonene støttes ikke.

Hvis du vil ha mer informasjon, kan du se [Konfigurasjon av produktindekshierarki](inventory-visibility-configuration.md#index-configuration).

### <a name="example"></a>Eksempel

Denne delen inneholder et eksempel som viser hvordan hierarkiet fungerer. Følgende tabell inneholder en liste over tilgjengelig beholdning for dette eksemplet.

| Element | Stil | Farge | Størrelse | Antall |
|---|---|---|---|---|
| I0001 | Bred | Svart | Liten | 1 |
| I0001 | Bred | Svart | Stor | 2 |
| I0001 | Bred | Rød | Liten | 3 |
| I0001 | Vanlig | Svart | Liten | 4 |
| I0001 | Vanlig | Svart | Stor | 5 |
| I0001 | Vanlig | Rød | Liten | 6 |
| I0001 | Vanlig | Rød | Stor | 7 |

Tabellen nedenfor viser hvordan indekshierarkiet er satt opp.

| Nøkkel | Settnummer | Hierarki |
|---|---|---|
| `StyleId` | 1 | 1 |
| `ColorId` | 1 | 2 |
| `SizeId` | 1 | 3 |

Basert på innstillingene ovenfor er dimensjonskombinasjonen for Lagersynlighet-spørringen *Stil*, *Farge* og *Størrelse*. Ved hjelp av hierarkioppsettet kan eksterne systemer utføre spørringer mot lagerbeholdningen på følgende måter:

- `()` – Gruppert av alle. Dette er resultatet:

    - I0001, 28

- `(StyleId)` – Gruppert etter stil. Dette er resultatet:

    - I0001, bred, 6
    - I0001, vanlig, 22

- `(StyleId, ColorId)` – Gruppert etter kombinasjonen av stil og farge. Dette er resultatet:

    - I0001, bred, svart, 3
    - I0001, bred, rød, 3
    - I0001, vanlig, svart, 9
    - I0001, vanlig, rød, 13

- `(StyleId, ColorId, SizeId)` – Gruppert etter kombinasjonen av stil, farge og størrelse. Dette er resultatet:

    - I0001, bred, svart, liten, 1
    - I0001, bred, svart, stor, 2
    - I0001, bred, rød, liten, 3
    - I0001, vanlig, svart, liten, 4
    - I0001, vanlig, svart, stor, 5
    - I0001, vanlig, rød, liten, 6
    - I0001, vanlig, rød, stor, 7

## <a name="set-up-a-custom-calculated-measure"></a>Sett opp et egendefinert beregnet mål

Du kan bruke Lagersynlighet til å spørre både på fysiske lagermål og *egendefinerte beregnede mål*.

Ved hjelp av konfigurasjonen kan du definere et sett med modifikatorer som legges til eller trekkes fra for å få totalt akkumulert utdataantall.

1. Logg deg på Power Apps-miljøet, og åpne **Lagersynlighet**.
1. Åpne **Konfigurasjon**-siden.
1. På fanen **Beregnet mål** velger du **Nytt beregnet mål** for å legge til et beregnet mål. Deretter angir du feltene som beskrevet i følgende tabell.

    | Felt | Verdi |
    |---|---|
    | Navn på nytt beregnet mål | Angi navnet på det beregnede målet. |
    | Datakilde | Spørringssystemet er en datakilde. |
    | Datakilde for modifikator | Angi datakilden for modifikatoren. |
    | Modifikator | Angi navnet på modifikatoren. |
    | Modifikatortype | Velg modifikatortypen (*Addisjon* eller *Subtraksjon*). |

Tabellen nedenfor viser et eksempel på det egendefinerte beregnede målet `MyCustomAvailableforReservation`. Hvis du vil ha mer informasjon om dette eksemplet, kan du se [Datakildekonfigurasjon](inventory-visibility-configuration.md#data-source-configuration).

| Datakilde for beregnet mål | Beregnet mål | Datakilde for modifikator | Modifikator | Modifikatortype |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `Exteexterchannelrchannel` | `reserved` | `Subtraction` |

### <a name="set-up-a-soft-reservation-mapping"></a><a name="setup-reservation-mapping"></a>Sett opp en tilordning av ikke-forpliktende reservasjon

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Før du kan redigere fanen **Tilordning av ikke-forpliktende reservasjon**, må du aktivere funksjonen *OnHandReservation* på **Funksjonsbehandling**-fanen.

Når du definerer tilordningen fra det fysiske målet til det beregnede målet, kan Lagersynlighet-tjenesten automatisk validere tilgjengelighet for reservering, basert på det fysiske målet.

Før du kan sette opp denne tilordningen, må de fysiske målene, de beregnede målene og datakildene være definert på fanene **Datakilde** og **Beregnet mål** på **Konfigurasjon**-siden i Power Apps (som beskrevet tidligere i dette emnet).

Følg denne fremgangsmåten for å definere tilordningen for ikke-forpliktende reservasjon.

1. Definer det fysiske målet som fungerer som mål for ikke-forpliktende reservasjon (for eksempel `softreservordered`).
1. På fanen **Beregnet mål** på **Konfigurasjon**-siden definerer du det beregnede målet *Tilgjengelig for reservasjon* (TFR) som inneholder AFR-beregningsformelen som du ønsker å tilordne til det fysiske målet. Du kan for eksempel definere `availforreserv` (tilgjengelig for reservasjon), slik at det er tilordnet det tidligere definerte fysiske målet `softreservordered`. På denne måten kan du finne ut hvilke antall som har beholdningsstatusen `softreservordered`, og som er tilgjengelige for reservering. Tabellen nedenfor viser TFR-beregningsformelen.

    | Modifikator | Datakilde | Måling |
    |---|---|---|
    | `Addition` | `fno` | `availphysical` |
    | `Addition` | `pos` | `inbound` |
    | `Subtraction` | `pos` | `outbound` |
    | `Subtraction` | `iv` | `softreservordered` |

1. Åpne **Konfigurasjon**-siden.
1. På fanen **Tilordning av ikke-forpliktende reservasjon** konfigurerer du tilordningen fra det fysiske målet til det beregnede målet. For det forrige eksemplet kan du bruke følgende innstillinger til å tilordne `availforreserv` til det tidligere definerte fysiske målet `softreservordered`.

    | Datakilde for fysisk mål | Fysisk mål | Tilgjengelig for datakilde for reservasjon | Tilgjengelig for beregnet mål for reservasjon |
    |---|---|---|---|
    | `iv` | `softreservordered` | `iv` | `availforreserv` |

### <a name="set-up-a-soft-reservation-hierarchy"></a><a name="setup-reservation-hierarchy"></a>Sett opp et hierarki for ikke-forpliktende reservasjon

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Før du kan redigere fanen **Hierarki for ikke-forpliktende reservasjon**, må du aktivere funksjonen *OnHandReservation* på **Funksjonsbehandling**-fanen.

Reservasjonshierarkiet beskriver serien med dimensjoner som må angis når det opprettes reservasjoner. Det fungerer på samme måte som produktindekshierarkiet fungerer for lagerbeholdningsspørringer.

Reservasjonshierarkiet kan være forskjellig fra lagerbeholdningsindekshierarkiet. Denne uavhengigheten lar deg implementere kategoriadministrasjon der brukere kan dele inn dimensjonene i detaljer for å angi krav til å lage mer presise reservasjoner.

#### <a name="example"></a>Eksempel

Følgende reservasjonshierarki defineres i systemet.

| Dimensjon | Hierarki |
|---|---|
| `ColorId` | 1 |
| `SizeId ` | 2 |
| `StyleId` | 3 |

Gitt dette reservasjonshierarkiet kan du reservere i følgende dimensjonsrekkefølger:

- `()` – Ingen dimensjon er angitt.
- `(ColorId)`
- `(ColorId, SizeId)`
- `(ColorId, SizeId, StyleId)`

Dimensjonsrekkefølgen skal følge sekvensen i reservasjonshierarkiet, dimensjonen for dimensjon. Reservasjoner som for eksempel har `(ColorId, StyleId)`, er ikke tillatt i dette eksemplet, fordi denne sekvensen ikke er definert i reservasjonshierarkiet.

### <a name="control-feature-management"></a><a name="feature-switch"></a>Styring av funksjonsbehandling

Tillegget Lagersynlighet inneholder funksjoner som *OnHandReservation* og *OnHandMostSpecificBackgroundService*. Disse funksjonene er deaktivert som standard. Hvis du vil bruke dem, åpner du **Konfigurasjon**-siden i Power Apps og aktiverer dem deretter på fanen **Funksjonsbehandling**.

### <a name="complete-and-update-the-configuration"></a>Fullfør og oppdater konfigurasjonen

Når du har fullført konfigurasjonen, må du aktivere alle endringene i Lagersynlighet. Du aktiverer endringer ved å velge **Oppdater konfigurasjon** øverst til høyre på **Konfigurasjon**-siden i Power Apps.

Første gang du velger **Oppdater konfigurasjon**, ber systemet deg om legitimasjon.

- **Klient-ID** – ID-en for Azure-app som du opprettet for Lagersynlighet.
- **Leier-ID** – ID-en til Azure-leieren.
- **Klienthemmelighet** – Hemmeligheten for Azure-app som du opprettet for Lagersynlighet.

Når du har logget deg på, blir konfigurasjonen oppdatert i Lagersynlighet-tjenesten.

> [!NOTE]
> Du må validere datakildenavnet, de fysiske målene og dimensjonstilordningene før du oppdaterer konfigurasjonen for Lagersynlighet-tjenesten. Du kan ikke endre disse innstillingene etter at du har valgt **Oppdater konfigurasjon**.

### <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Finn endepunkt for tjeneste

Hvis du ikke kjenner til det korrekte endepunktet for Lagersynlighet-tjenesten, åpner du **Konfigurasjon**-siden i Power Apps og velger deretter **Vis endepunkt for tjeneste** øverst til høyre. Siden vil vise det riktige endepunktet for tjenesten.

## <a name="operational-visibility"></a>Driftssynlighet

På siden **Driftssynlighet** vises resultatene av en lagerbeholdningsspørring i sanntid, basert på diverse dimensjonskombinasjoner. Når *OnHandReservation*-funksjonen er aktivert, kan du også postere reservasjonsforespørsler fra siden **Driftssynlighet**.

### <a name="on-hand-query"></a>Beholdningsspørring

Fanen **Beholdningsspørring** viser resultatene av en lagerbeholdningsspørring i sanntid.

Når du velger fanen **Beholdningsspørring**, ber systemet deg om legitimasjon slik at det kan hente bærertokenet som kreves for å utføre en spørring i Lagersynlighet-tjenesten. Du kan bare lime inn bærertokenet i **Bærertoken**-feltet og lukke dialogboksen. Du kan deretter postere en forespørsel om lagerbeholdning.

Hvis bærertokenet ikke er gyldig, eller hvis det er utløpt, må du lime inn et nytt i **Bærertoken**-feltet. Angi riktige verdier for **Klient-ID**, **Leier-ID** og **Klienthemmelighet**, og velg deretter **Oppdater**. Systemet får automatisk et nytt, gyldig bærertoken.

Hvis du vil postere en lagerbeholdningsspørring, angir du spørringen i forespørselsteksten. Bruk mønsteret som er beskrevet i [Spør ved å bruke posteringsmetoden](inventory-visibility-api.md#query-with-post-method).

![Innstillinger for beholdningsspørring](media/inventory-visibility-query-settings.png "Innstillinger for beholdningsspørring")

### <a name="reservation-posting"></a>Postering av reservasjon

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Bruk fanen **Postering av reservasjon** til å postere en reservasjonsforespørsel. Før du kan postere en reservasjonsforespørsel, må du aktivere funksjonen *OnHandReservation*. Hvis du vil ha mer informasjon om denne funksjonen, kan du se [Lagersynlighetsreservasjoner](inventory-visibility-reservations.md).

Hvis du vil postere en reservasjonsforespørsel, må du angi en verdi i forespørselsteksten. Bruk mønsteret som er beskrevet i [Opprett én reservasjonshendelse](inventory-visibility-api.md#create-one-reservation-event). Velg deretter **Poster**. Hvis du vil vise detaljer for forespørselssvaret, velger du **Vis detaljer**. Du kan også hente **reservationId**-verdien fra svardetaljene.

## <a name="inventory-summary"></a>Lagersammendrag

**Lagersammendrag** er en tilpasset visning for *enheten Sum av lagerbeholdning*. Det gir et lagersammendrag for produkter sammen med alle dimensjoner. Ved hjelp av det **avanserte filteret** i Dataverse kan du opprette en personlig visning som viser radene som er viktige for deg. Med de avanserte filteralternativene kan du opprette en rekke visninger, fra enkel til kompleks. I tillegg kan du legge til grupperte og nestede betingelser i filtrene.

Hvis du vil lære mer om hvordan du bruker det **avanserte filteret**, kan du se [Rediger eller opprett personlige visninger ved hjelp av avanserte rutenettfiltre](/powerapps/user/grid-filters-advanced).

Øverst i den tilpassede visningen finner du tre felter: **Standarddimensjon**, **Egendefinert dimensjon** og **Mål**. Du kan bruke disse feltene til å bestemme hvilke kolonner som skal vises.

Du kan velge kolonnehodet for å filtrere eller sortere det gjeldende resultatet.

Nederst i den tilpassede visningen vises informasjon som for eksempel "50 poster (29 valgt)" eller "50 poster". Denne informasjonen refererer til postene som er lastet inn for øyeblikket fra resultatet av det **avanserte filteret**. Teksten "29 valgt" refererer til antall poster som er valgt ved hjelp av kolonnehodefilteret for de innlastede postene.

Nederst i visningen finner du en **Last inn flere**-knapp som du kan bruke til å laste inn flere poster fra Dataverse. Standard antall poster som lastes inn, er 50. Når du velger **Last inn flere**, lastes de neste 1000 tilgjengelige postene inn i visningen. Antallet på **Last inn flere**-knappen angir postene som er lastet inn for øyeblikket, og det totale antallet poster for resultatet av det **avanserte filteret**.

![Lagersammendrag](media/inventory-visibility-onhand-list.png "Lagersammendrag")
