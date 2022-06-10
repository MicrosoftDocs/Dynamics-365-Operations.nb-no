---
title: Lagertildeling for lagersynlighet
description: Dette emnet beskriver hvordan du konfigurerer og bruker lagertildelingsfunksjonen, slik at du kan sette av dedikert lager til side for å sikre at du kan oppfylle de mest lønnsomme kanalene eller kundene.
author: yufeihuang
ms.date: 05/20/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 4293ead4ccfc9ba04e8b9da437134b4e97569026
ms.sourcegitcommit: 1877696fa05d66b6f51996412cf19e3a6b2e18c6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/20/2022
ms.locfileid: "8786952"
---
# <a name="inventory-visibility-inventory-allocation"></a>Lagertildeling for lagersynlighet

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>Forretningsbakgrunn og formål

I mange tilfeller må produsenter, forhandlere og andre forretningsinnehavere av forsyningskjeden forhåndstildele beholdning for viktige salgskanaler, lokasjoner eller kunder, eller for bestemte salgshendelser. Lagertilordning er en vanlig fremgangsmåte i planleggingsprosessen for salg, og gjøres før de faktiske salgsaktivitetene skjer og en salgsordre opprettes.

Et sykkelfirma har for eksempel begrenset lagerbeholdning som er tilgjengelig for en svært populær bedrift. Dette firmaet gjør både online- og butikksalg. I hver salgskanal har firmaet noen viktige firmapartnere (marked og store forhandlere) som krever at en bestemt del av det tilgjengelige lageret kan lagres for dem. Derfor må sykkelfirmaet være i stand til å balansere lagerdistribusjon på tvers av kanaler og også håndtere forventningene til sine VIP-partnere. Den beste måten å oppnå begge målene på, er å bruke lagerfordeling, slik at hver kanal og forhandler kan motta bestemte tilordnede antall som kan selges til kunder senere.

Lagertildeling har to grunnleggende forretningsformål:

- **Lagerbeskyttelse (ringorganisering)** – Organisasjoner vil forhåndstildele begrenset eller begrenset beholdning til prioriterte kanaler, områder, VIP-kunder og datterselskaper. Funksjonen for lagersynlighetstildeling har som mål å beskytte det tildelte lageret, slik at de andre tildelingene, reservasjonene eller andre salgsbehov ikke vil påvirke det tidligere tildelte lageret.
- **Oversalgsstyring** – Funksjonen for lagersynlighetstildeling har som mål å sette en begrensning på de tidligere tildelte antallene, slik at mottaksparten (for eksempel en kanal eller kundegruppe) ikke vil overforbruke dem når den faktiske salgstransaksjonen som er basert på en myk reservasjon, trer i kraft.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Tildelingsdefinisjon i Lagersynlighetstjeneste

Selv om tildelingsfunksjonen i Lagersynlighetstjeneste ikke setter fysiske lagerantall til side, refererer den til tilgjengelig fysisk lagerantall for å definere det første som er *tilgjengelig for å tilordne* virtuelt puljeantall. Lagertilordning i Lagersynlighet er en myk tilordning. Det gjøres før faktiske salgstransaksjoner forekommer, og er ikke avhengig av salgsordrer. Du kan for eksempel tildele aksjer til de viktigste salgskanalene eller de store firmaforhandlerne før eventuelle sluttkunder besøker salgskanalen eller detaljhandelen for å kjøpe den.

Forskjellen mellom lagertilordning og [ikke-forpliktet lagerreservasjons](inventory-visibility-reservations.md) er at ikke-forpliktet reservering vanligvis er koblet til faktiske salgstransaksjoner (salgsordrelinjer). Hvis du vil bruke tildelings- og ikke-forpliktet reservering sammen, anbefaler vi derfor at du gjør lagertilordningen først og deretter ikke-forpliktet reservering mot de tilordnede antallene. Hvis du vil ha mer informasjon, kan du se [Forbruke som ikke-forpliktet reservasjon](#consume-to-soft-reserved).

Ved hjelp av lagertildelingsfunksjonen kan salgsplanleggere eller nøkkelkontoledere styre og forhåndstilordne viktig beholdning på tvers av tildelingsgrupper (for eksempel kanaler, regioner og kundegrupper). Det støtter også sporing, justering og analyse av forbruk i sanntid mot tilordnede antall, slik at etterfylling eller omplassering kan utføres til riktig tid. Denne evnen til å få oversikt i sanntidssynligheten i fordeling, forbruk og fordelingssaldo, er spesielt viktig ved hendelser med hurtigsalg eller forfremmelse.

## <a name="terminology"></a>Terminologi

Følgende begreper og begreper er nyttige i diskusjoner om lagerfordeling:

- **Tildelingsgruppe** – Gruppen som eier fordelingen, for eksempel en salgskanal, kundegruppe eller ordretype.
- **Tildelingsgruppeverdi** – Verdien til hver fordelingsgruppe. *Nett* eller *butikk* kan for eksempel være verdien til salgskanalfordelingsgruppen, mens *VIP* eller *vanlig* kan være verdien til kundetildelingsgruppen.
- **Tildelingshierarki** – En måte å kombinere tildelingsgrupper på en hierarkisk måte. Du kan for eksempel definere *kanal* som hierarkinivå 1, *område* som nivå 2 og *kundegruppe* som nivå 3. Under lagertildeling må du følge fordelingshierarkisekvensen når du angir verdien til fordelingsgruppen. Det kan for eksempel hende du tildeler 200 røde sykler til *nett*-kanalen, *London*-regionen og *VIP*-kundegruppen.
- **Tilgjengelig for tildeling** – Den *virtuelle fellespuljen* som angir antallet som er tilgjengelig for ytterligere tilordning. Det er et beregnet mål som du fritt kan definere ved å bruke din egen formel. Hvis du også bruker funksjonen for ikke-forpliktende reservasjon, anbefaler vi at du bruker den samme formelen til å beregne tilgjengelig for tildeling og tilgjengelig for reservering.
- **Tildelt** – Et fysisk mål som viser den tildelte kvoten som kan forbrukes av tildelingsgruppene.
- **Forbrukt** – Et fysisk mål som angir at antall er brukt mot det opprinnelige fordelte antallet. Etter hvert som tall legges til i dette fysiske målet, reduseres det tildelte fysiske målet automatisk.

Illustrasjonen nedenfor viser forretningsarbeidsflyten for lagertildeling.

![Forretningsarbeidsflyt for lagersynlighetstilordning.](media/inventory-visibility-allocation-flow.png "Forretningsarbeidsflyt for lagersynlighetstilordning.")

## <a name="set-up-inventory-allocation"></a>Definere lagertilordning

Lagertildelingsfunksjonen består av følgende komponenter:

- Den forhåndsdefinerte, tildelingsrelaterte datakilden, fysiske mål og beregnede mål.
- Tilpassbare tildelingsgrupper som har maksimalt åtte nivåer.
- Et sett med fordelingsapplikasjonsgrensesnitt (APIer):

    - tildel
    - tildel på nytt
    - ikke-tilordnet
    - forbruk
    - spørring

Prosessen med å konfigurere fordelingsfunksjonen har to trinn:

- Definer [datakilde](inventory-visibility-configuration.md#data-source-configuration) og dens [mål](inventory-visibility-configuration.md#data-source-configuration-physical-measures).
- Angi navn og hierarki for tildelingsgruppen.

### <a name="predefined-data-source"></a>Forhåndsdefinert datakilde

Når du aktiverer fordelingsfunksjonen og kaller API for konfigurasjonsoppdatering, oppretter Lagersynlighet én forhåndsdefinert datakilde og flere innledende mål.

Datakilden kalles `@iv`.

Her er de første fysiske målene:

- `@iv`

    - `@allocated`
    - `@cumulative_allocated`
    - `@consumed`
    - `@cumulative_consumed`

Her er de første beregnede målene:

- `@iv`

    - `@iv.@available_to_allocate` = `??` – `??` – `@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Legge til andre fysiske mål i det beregnede målet som er tilgjengelig for tildeling

Hvis du vil bruke tildeling, må du definere det beregnede målet som er tilgjengelig for tildeling (`@iv`.`@available_to_allocate`). Du har for eksempel `fno`-datakilden og `onordered`-målet, `pos`-datakilden og `inbound`-målet, og du vil gjøre tildeling på lager for summen `fno.onordered` og `pos.inbound`. I dette tilfellet skal `@iv.@available_to_allocate` inneholde `pos.inbound` og `fno.onordered` i formelen. Her er et eksempel:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

### <a name="change-the-allocation-group-name"></a>Endre navnet på fordelingsgruppen

Maksimalt åtte tildelingsgruppenavn kan angis. Gruppene har et hierarki.

Du angir gruppenavnene på siden for **konfigurasjon av PowerApp for lagersynlighet**. Hvis du vil åpne denne siden, går du til Microsoft Dataverse-miljøet, åpner Lagersynlighet-appen og velger **Konfigurasjon \> Tilordning**.

Hvis du for eksempel bruker fire gruppenavn og setter dem til, \[`channel`, `customerGroup`, `region`, `orderType`\] vil disse navnene være gyldige for tildelingsrelaterte forespørsler når du kaller API for konfigurasjonsoppdatering.

### <a name="allcoation-using-tips"></a>Tildeling ved hjelp av tips

- For hvert produkt bør fordelingsfunksjonen bruke på samme dimensjonsnivå i henhold til produktindekshierarkiet du angir i [konfigurasjon for produktindekshierarkiet](inventory-visibility-configuration.md#index-configuration). Indekshierarkiet er for eksempel Område, Lokasjon, Farge, Størrelse. Hvis du tildeler noe antall for ett produkt i Område, Lokasjon, Fargenivået. Neste gang du tildeler, bør også på Område, Lokasjon, Fargenivå, hvis du bruker Område, Lokasjon, Farge, Størrelsesnivå eller Område, Lokasjonsnivå, vil ikke dataene være konsekvent.
- Endring av tildelingsgruppenavn vil ikke påvirke dataene som er lagret i tjenesten.
- Tildelingen bør skje etter at produktet har det positive beholdningsantallet.

### <a name="using-the-allocation-api"></a><a name="using-allocation-api"></a>Bruke tildelings-API

I øyeblikket åpnes fem tildelings-APIer:

- POST /api/environment/{environmentId}/allocation/allocate
- POST /api/environment/{environmentId}/allocation/unallocate
- POST /api/environment/{environmentId}/allocation/reallocate
- POST /api/environment/{environmentId}/allocation/consume
- POST /api/environment/{environmentId}/allocation/query

#### <a name="allocate"></a>Tildel

Kall API for `Allocate` for å tildele et produkt som har bestemte dimensjoner. Her er skjemaet for forespørselsteksten.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "targetGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Du vil for eksempel tildele et antall på 10 for produktet *Sykkel*, område *1*, lokasjon *11*, farge *rød*, kanale *Tilkoblet*, kundegruppen *VIP* og område *USA*. For å gjøre denne fordelingen, kan du kalle opp med følgende hovedinnhold.

```json
{
    "id": "???",
    "productId": "Bike",
    "targetGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 10,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

Antallet må alltid være mer enn 0 (null).

#### <a name="unallocate"></a>Ikke-tilordnet

Bruke API for `Unallocate` til å tilbakeføre `Allocate`-operasjonen. Negativt antall er ikke tillatt i en `Allocate`-operasjon. Teksten i `Unallocate` er identisk med teksten i `Allocate`.

#### <a name="reallocate"></a>Tildel på nytt

Bruk API til `Reallocate` for å flytte noe tildelt antall til en annen gruppekombinasjon. Her er skjemaet for forespørselsteksten.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "sourceGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "targetGroups": {
        "groupD": "string",
        "groupE": "string",
        "groupF": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Du kan for eksempel flytte to sykler som har dimensjonene \[område=1, lokasjon=11, farge=rød\] fra tildelingsgruppen \[Online, VIP, US\] til fordelingsgruppen \[Online, VIP, EU\] ved å kalle opp API for `Reallocate` og gi følgende hovedtekst.

```json
{
    "id": "???",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "targetGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "EU"
    },
    "quantity": 2,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

#### <a name="consume"></a>Forbruk

Bruk API for `Consume` til å postere forbruksantallet mot fordeling. Du kan for eksempel bruke denne API-en til å flytte tildelt antall til noen reelle mål. Her er skjemaet for forespørselsteksten.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "targetGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "physicalMeasures": {
        "datasource1": {
            "measure": "string" // Addition or Subtraction
        }
    }
}
```

Det er for eksempel åtte tildelte sykler som har dimensjonene \[område=1, lokasjon=11, farge=rød\] for tildelingsgruppen \[Online, VIP, USA\]. Følgende tilgjengelig-for-tildeling-formel brukes:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

De åtte numrene tildeles fra målet `pos.inbound`.

Tre sykler blir solgt, og de tas fra tildelingspuljen. For å registrere dette trekket, kan du kalle opp med følgende forespørselstekst.

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "targetGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "pos": {
            "inbound": "Subtraction"
        }
    }
}
```

Etter dette kallet reduseres det tildelte antallet for produktet med 3. I tillegg genererer lagersynlighet en beholdningsendringshendelse der `pos.inbound` = *-3*. Du kan også beholde verdien `pos.inbound` som den er, og bare forbruke det fordelte antallet. I dette tilfellet må du imidlertid enten opprette et nytt fysisk mål for å beholde det forbrukte antallet, eller bruke det forhåndsdefinerte målet `@iv.@consumed`.

I denne forespørselen legger du merke til at det fysiske målet du bruker i hovedteksten for ny bruk, bør bruke motsatt modifertype (Addisjon eller Subtraksjon), sammenlignet med endringstypen som brukes i det beregnede målet. Så i denne forbruksteksten har `iv.inbound` verdien `Subtraction`, ikke `Addition`.

`fno`-datakilden kan ikke brukes i den forbruksteksten, fordi vi alltid har gjort krav på at lagersynlighet ikke kan endre noen data for `fno`-datakilden. Dataflyten er enveisveis, som betyr at alle antallsendringer for datakilden `fno` må komme fra Supply Chain Management-miljøet.

#### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a>Forbruk som en myk reservasjon

API for `Consume` kan også forbruke det tildelte antallet som en myk reservering. I dette tilfellet vil operasjonen `Consume` redusere det tildelte antallet, og deretter gjøre en myk reservering for dette antallet. For å bruke denne fremgangsmåten må du også bruke [myk reservasjon](inventory-visibility-reservations.md)-funksjonen i Lagersynlighet.

Du har for eksempel angitt en myk reservasjonsmodifikator (mål) som `iv.softreserved`. Følgende formel brukes for beregnet mål for tilgjengelig til reserve:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound` – `iv.softreserved`

Hvis du vil bruke dette oppsettet med fordelingsfunksjonen, legger du `@iv.@allocated` til `iv.available_to_reserve` i produksjon av følgende formel:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound` – `iv.softreserved` – `@iv.@allocated`

Oppdater deretter `@iv.@available_to_allocate` til samme verdi.

Når du vil bruke et antall på 3 og reservere dette antallet direkte, kan du gjøre et kall som har forespørselsteksten nedenfor.

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "targetGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "iv": {
            "softreserved": "Addition"
        }
    }
}
```

I denne forespørselen legger du merke til at `iv.softreserved` har verdien `Addition`, ikke `Subtraction`.

#### <a name="query"></a>Forespørsel

Bruk API for `Query` til å hente tildelingsrelatert informasjon for noen produkter. Du kan bruke dimensjonsfiltre og tilordningsgruppefiltre til å begrense resultatene. Dimensjonene må samsvare ut fra det du vil hente, for eksempel \[område=1, lokasjon=11\] vil ha ikke-relaterte resultater sammenlignet med \[område=1, lokasjon=11, farge=rød\].

```json
{
    "productId": "string",
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "groups": {
        "additionalProp1": "string",
        "additionalProp2": "string",
        "additionalProp3": "string"
    },
}
```

Bruk for eksempel feltet \[område=1, lokasjon=11, farge=rød\] og tomme gruppefelt til å hente alle tildelingsposter:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

Bruk \[område=1, lokasjon=11, farge=rød\] og gruppene \[kanal=Online, customerGroup=VIP, område=USA\] for å få tildelingsposter for denne gruppen:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```
