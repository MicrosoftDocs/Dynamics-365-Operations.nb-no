---
title: Lagersynlighetsreservasjoner
description: Dette emnet beskriver hvordan du definerer reserveringsfunksjonen for å opprette reserveringer, forbruke reserveringer og/eller ikke reservere angitte lagerantall ved hjelp av Lagersynlighet.
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
ms.openlocfilehash: 4a85520c0911bb7eed5842b3fd5bd706009351e5
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500361"
---
# <a name="inventory-visibility-reservations"></a>Lagersynlighetsreservasjoner

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Dette emnet beskriver hvordan du definerer reserveringsfunksjonen for å opprette reserveringer, forbruke reserveringer og/eller ikke reservere angitte lagerantall ved hjelp av Lagersynlighet.

Reserveringer markerer et lagerantall som skal brukes i fremtiden. Når du oppretter en reservasjon, forhindrer systemet at andre ordrer reserverer eller forbruker de reserverte varene til reserveringen enten blir forbrukt eller ikke reservert. Reserveringer opprettes, forbrukes og avbrytes ved hjelp av API-kall til lagersynlighetstjenesten.

Du kan eventuelt konfigurere Microsoft Dynamics 365 Supply Chain Management (og andre tredjepartssystemer) til automatisk å motpostere antallet som er reservert, ved å bruke Lagersynlighet. Motposteringsantallet slettes fra reserveringspostene i Lagersynlighet.

Når du slår på reservasjonsfunksjonen, blir Supply Chain Management automatisk klart til å motpostere reserveringer som gjøres ved hjelp av Lagersynlighet.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Aktiver og konfigurer reservasjonsfunksjonen

Følg denne fremgangsmåten for å aktivere reservasjonsfunksjonen.

1. Logg deg på Power Apps og åpne **Lagersynlighet**.
1. Åpne **Konfigurasjon**-siden.
1. På fanen **Funksjonsbehandling** aktiverer du funksjonen *OnHandReservation*.
1. Logg på Supply Chain Management.
1. Gå til arbeidsområdet **[Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og aktiver funksjonen *Integrering av lagersynlighet med motpostering av reservasjon* (krever versjon 10.0.22 eller senere).
1. Gå til **Lagerstyring \> Oppsett \> Parametere for integrering av lagersynlighet**, åpne fanen **Motpostering av reservasjon** og gjør følgende innstilling:
    - **Aktiver motpostering av reservasjon** – Sett til *Ja* for å aktivere denne funksjonaliteten.
    - **Motposteringsmodifikator for reservasjon** – Velg lagertransaksjonsstatusen som motposterer reserveringer som gjøres i lagersynligheten. Denne innstillingen bestemmer ordrebehandlingsstadiet som utløser motregninger. Fasen spores etter ordrens lagertransaksjonsstatus. Velg ett av følgende:
        - *I ordre/bestilling* – Når det gjelder statusen *I transaksjon*, sender en ordre en motposteringsforespørsel når den opprettes. Motposteringsantallet vil være antallet i den opprettede ordren.
        - *Reserver* – For statusen *Reserver bestilt transaksjon* sender en ordre en motforespørsel når den er reservert, plukket, følgeseddelpostert eller fakturert. Forespørselen utløses bare én gang, for første trinn når den nevnte prosessen inntreffer. Motposteringsantallet vil være antallet der lagertransaksjonsstatusen endres fra *I ordre/bestilling* til *Reservert av bestilt* (eller senere status) på den tilsvarende ordrelinjen.

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Bruk reservasjonsfunksjonen i Lagersynlighet

Når du kaller opp API-en for reservasjon, merker systemet reservasjonen av de angitte varene og antallene. Du må definere et reservasjonshierarki og postere forespørsler som samsvarer med dette reservasjonshierarkiet. Reservasjonene kan deretter foretas ved å kalle opp API-ene for reservasjon direkte.

### <a name="configure-the-reservation-hierarchy"></a>Konfigurer reservasjonshierarkiet

Reservasjonshierarkiet beskriver serien med dimensjoner som må angis når det opprettes reservasjoner. Det fungerer på samme måte som indekshierarkiet fungerer for lagerbeholdningsspørringer.

Reservasjonshierarkiet kan være forskjellig fra indekshierarkiet. Denne uavhengigheten lar deg implementere kategoriadministrasjon der brukere kan dele inn dimensjonene i detaljer for å angi krav til å lage mer presise reservasjoner.

Hvis du vil konfigurere et hierarki for ikke-forpliktende reservasjoner i Power Apps, åpner du **Konfigurasjon**-siden og går deretter til fanen **Hierarki for ikke-forpliktende reservasjon**, der du kan konfigurere reservasjonshierarkiet ved å legge til og/eller endre dimensjoner og deres hierarkinivåer.

Mykt reservasjonshierarki bør inneholde `SiteId` og `LocationId` som komponenter fordi de konstruerer partisjonskonfigurasjonen.

Hvis du vil ha mer informasjon om hvordan du konfigurerer reservasjoner, kan du se [Reservasjonskonfigurasjon](inventory-visibility-configuration.md#reservation-configuration).

### <a name="call-the-reservation-api"></a>Kall opp API-en for reservasjon

Reservasjoner gjøres i Lagersynlighet-tjenesten ved å sende en POSTER-forespørsel til tjenestens URL-adresse, for eksempel `/api/environment/{environment-ID}/onhand/reserve`.

For en reservasjon må forespørselsteksten inneholde en organisasjons-ID, en produkt-ID, reservert antall og dimensjoner. Forespørselen genererer en unik reservasjons-ID for hver reservasjonspost. Reservasjonsposten inneholder den unike kombinasjonen av produkt-ID-en og dimensjonene.

Når du kaller reservasjons-API, kan du styre reservasjonsvalideringen ved å angi den boolske `ifCheckAvailForReserv` parameteren i forespørselsteksten. Verdien `True` betyr at valideringen kreves, mens en verdi å `False` betyr at valideringen ikke er nødvendig. Standardverdien er `True`.

Hvis du vil avbryte en reservering eller ikke reservere angitte lagerantall, angir du antallet til en negativ verdi og angir parameteren `ifCheckAvailForReserv` til `False` for å hoppe over valideringen.

Her er et eksempel på forespørselsteksten, til referanse.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "SoftReservOrdered",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

## <a name="offset-reservations-in-supply-chain-management"></a>Motpostering av reservasjoner i Supply Chain Management

For lagertransaksjonsstatuser som har en angitt motposteringsmodifikator for reserversjon, vil transaksjonsoppdateringen motpostere den tilsvarende reservasjonsposten når alle følgende betingelser er oppfylt:

- Reservasjons-ID-en på lagertransaksjonen samsvarer med reservasjons-ID-en til reservasjonsposten i Lagersynlighet-tjenesten.
- Dimensjonene i lagertransaksjonen er identiske med dimensjonene i reservasjonsposten i Lagersynlighet-tjenesten.
- Endringer i lagertransaksjonsstatus utløser motpsoteringer for reserveringer når lagertransaksjonsstatusen viser at en ordreprosess er fullført eller hoppet over.

Motposteringsantallet følger lagerantallet som er angitt på lagertransaksjoner. Motposteringen trer ikke i kraft hvis det ikke gjenstår et reservert antall i Lagersynlighet-tjenesten.

### <a name="set-up-the-reservation-offset-modifier"></a>Definer motposteringsmodifikatoren for reservasjon

Hvis du ikke allerede har gjort det, konfigurerer du reservasjonsmodifikatoren som beskrevet i [Aktiver og konfigurer reservasjonsfunksjonen](#turn-on).

### <a name="set-up-reservation-ids"></a>Konfigurer reservasjons-ID-er

Reservasjons-ID-en markerer en reservasjonspost unikt i Lagersynlighet. I Supply Chain Management legger brukere inn reserveringer på ordrelinjer for å merke motregningen for den tilsvarende reservasjonsposten.

Følg denne fremgangsmåten for å definere reservasjons-ID-er i Supply Chain Management.

1. Åpne en salgsordre (for eksempel fra siden **Alle salgsordrer**).
1. På hurtigfanen **Salgsordrelinjer** velger du en ordrelinje.
1. På verktøylinjen på hurtigfanen **Salgsordrelinjer** velger du **Oppdater linje \> Beholdning \> Integrering av lagersynlighet**.
1. Angi de relevante reservasjons-ID-ene.

Lagerstatusendringen samsvarer med oppsettet for motregningsendringen.
