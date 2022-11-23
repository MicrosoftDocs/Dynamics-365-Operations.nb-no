---
title: Lagertildeling for Inventory Visibility
description: Denne artikkelen beskriver hvordan du konfigurerer og bruker lagertildelingsfunksjonen, slik at du kan sette av dedikert lager til side for å sikre at du kan oppfylle de mest lønnsomme kanalene eller kundene.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 449ca0616405ba589b92fba1ef078a4350d1e3b1
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762679"
---
# <a name="inventory-visibility-inventory-allocation"></a>Lagertildeling for Inventory Visibility

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>Forretningsbakgrunn og formål

Organisasjoner må ofte forhåndstilordne lagerbeholdningen til de viktigste salgskanalene, kundegruppene, regionene og kampanjehendelsene for å sikre at den forhåndstilordnede beholdningen er beskyttet mot eventuell annen bruk, og at de bare kan brukes via salgstransaksjoner som er relevante for tildelingen. Lagertilordning i Lagersynlighet er en komponent i planleggingsprosessen for salg, og gjøres før de faktiske salgsaktivitetene skjer eller en salgsordre opprettes.

Et firma med navnet Contoso produserer for eksempel en populær bedrift. Ettersom nylige avbrudd i forsyningskjeden har påvirket alle lagerbeholdningene i transitt av denne delen, har Contoso bare begrenset lagerbeholdning, og må gjøre best mulig bruk av den. Contoso driver både online- og butikksalg. I hver salgskanal har firmaet noen viktige firmapartnere (marked og store forhandlere) som krever at en bestemt del av det tilgjengelige lageret kan lagres for dem. Derfor må sykkelfirmaet være i stand til å balansere lagerdistribusjon på tvers av kanaler og også håndtere forventningene til sine VIP-partnere. Den beste måten å oppnå begge målene på, er å bruke lagerfordeling, slik at hver kanal og forhandler kan motta bestemte tilordnede antall som kan selges til kunder senere.

Lagertildeling har to grunnleggende forretningsformål:

- **Lagerbeskyttelse (ringorganisering)** – Organisasjoner vil forhåndstildele begrenset eller begrenset beholdning til prioriterte kanaler, områder, VIP-kunder og datterselskaper. Funksjonen for lagersynlighetstildeling har som mål å beskytte det tildelte lageret, slik at de andre tildelingene, reservasjonene eller andre salgsbehov ikke vil påvirke det tidligere tildelte lageret.
- **Oversalgsstyring** – Funksjonen for lagersynlighetstildeling har som mål å sette en begrensning på de tidligere tildelte antallene, slik at mottaksparten (for eksempel en kanal eller kundegruppe) ikke vil overforbruke dem når den faktiske salgstransaksjonen som er basert på en myk reservasjon, trer i kraft.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Tildelingsdefinisjon i Lagersynlighetstjeneste

### <a name="allocation-virtual-pool"></a>Virtuell pulje for tildeling

Selv om tildelingsfunksjonen i Lagersynlighet ikke setter fysiske lagerantall til side, refererer den til tilgjengelig fysisk lagerantall for å definere det første som er *tilgjengelig for å tilordne* virtuelt puljeantall. Lagertilordning i Lagersynlighet er en myk tilordning. Det gjøres før faktiske salgstransaksjoner forekommer, og er ikke avhengig av salgsordrer. Du kan for eksempel tildele aksjer til de viktigste salgskanalene eller de store firmaforhandlerne før eventuelle sluttkunder besøker salgskanalen eller detaljhandelen for å kjøpe den.

### <a name="difference-between-inventory-allocation-and-soft-reservation"></a>Differanse mellom lagertilordning og ikke-forpliktende reservering

[Ikke-forpliktende reserveringer](inventory-visibility-reservations.md) er vanligvis koblet til faktiske salgstransaksjoner (salgsordrelinjer). Både tildeling og ikke-forpliktende reservering kan brukes uavhengig, men hvis du vil bruke dem sammen, bør myk reservering utføres etter fordeling. Vi anbefaler derfor at du gjør lagertilordningen først og deretter ikke-forpliktet reservering mot de tilordnede antallene for å oppnå forbruk nesten i sanntid mot tildeling. Hvis du vil ha mer informasjon, kan du se [Forbruke som ikke-forpliktet reservasjon](#consume-to-soft-reserved).

Ved hjelp av lagertildelingsfunksjonen kan salgsplanleggere eller nøkkelkontoledere styre og forhåndstilordne viktig beholdning på tvers av tildelingsgrupper (for eksempel kanaler, regioner og kundegrupper). Det støtter også sporing, justering og analyse av forbruk i sanntid mot tilordnede antall, slik at etterfylling eller omplassering kan utføres til riktig tid. Denne evnen til å få oversikt i sanntidssynligheten i fordeling, forbruk og fordelingssaldo, er spesielt viktig ved hendelser med hurtigsalg eller forfremmelse.

## <a name="terminology"></a>Terminologi

Følgende begreper og begreper er nyttige i diskusjoner om lagerfordeling:

- **Tildelingsgruppe** – Gruppen som eier fordelingen, for eksempel en salgskanal, kundegruppe eller ordretype.
- **Tildelingsgruppeverdi** – Verdien til hver fordelingsgruppe. *Nett* eller *butikk* kan for eksempel være verdien til salgskanalfordelingsgruppen, mens *VIP* eller *vanlig* kan være verdien til kundetildelingsgruppen.
- **Tildelingshierarki** – En måte å kombinere tildelingsgrupper på en hierarkisk måte. Du kan for eksempel definere *kanal* som hierarkinivå 1, *område* som nivå 2 og *kundegruppe* som nivå 3. Under lagertildeling må du følge fordelingshierarkisekvensen når du angir verdien til fordelingsgruppen. Det kan for eksempel hende du tildeler 200 røde sykler til *nett*-kanalen, *London*-regionen og *VIP*-kundegruppen.
- **Tilgjengelig for tildeling** – Den *virtuelle fellespuljen* som angir antallet som er tilgjengelig for ytterligere tilordning. Det er et beregnet mål som du fritt kan definere ved å bruke din egen formel. Hvis du også bruker funksjonen for ikke-forpliktende reservasjon, anbefaler vi at du bruker den samme formelen til å beregne tilgjengelig for tildeling og tilgjengelig for reservering.
- **Tildelt** – Et fysisk mål som viser den tildelte kvoten som kan forbrukes av tildelingsgruppene. Trekkes fra samtidig som det forbrukte antallet legges til.
- **Forbrukt** – Et fysisk mål som angir at antall er brukt mot det opprinnelige fordelte antallet. Etter hvert som tall legges til i dette fysiske målet, reduseres det tildelte fysiske målet automatisk.

Illustrasjonen nedenfor viser forretningsarbeidsflyten for lagertildeling.

![Forretningsarbeidsflyt for lagersynlighetstilordning.](media/inventory-visibility-allocation-flow.png "Forretningsarbeidsflyt for lagersynlighetstilordning.")

Illustrasjonen nedenfor viser tildelingshierarkiet og tildelingsgruppene. Den *virtuelle fellespuljen* som vises her, er det tilgjengelige antallet for tildeling.

[<img src="media/inventory-visibility-allocation-hierarchy.png" alt="Inventory Visibility allocation hierarchy." title="Lagersynlighet-tildelingshierarki" width="720" />](media/inventory-visibility-allocation-hierarchy.png)

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

Prosessen med å konfigurere fordelingsfunksjonen har tre trinn:

- Aktiver funksjonen i Lagersynlighet-appen ved å gå til **Konfigurasjon \> Funksjonsbehandling og -innstillinger \> Tildeling**.
- Definer [datakilde](inventory-visibility-configuration.md#data-source-configuration) og dens [mål](inventory-visibility-configuration.md#data-source-configuration-physical-measures).
- Angi navn og hierarki for tildelingsgruppen.

### <a name="predefined-data-source"></a>Forhåndsdefinert datakilde

Når du aktiverer fordelingsfunksjonen og kaller API for konfigurasjonsoppdatering, oppretter Lagersynlighet én forhåndsdefinert datakilde og flere innledende mål.

Datakilden kalles `@iv`. Den inneholder et sett med standard fysiske mål. Du kan vise dem fra Lagersynlighet-appen ved å gå til **Konfigurasjon \> Datakilde**. Du skal se **Datakilde – @IV**. Utvid `@iv`-datakilden for å vise listen over opprinnelige fysiske mål:

- `@iv`

    - `@allocated`
    - `@cumulative_allocated`
    - `@consumed`
    - `@cumulative_consumed`

Velg kategorien **Beregnede målinger** for å vise det opprinnelige beregnede målet, som har navnet `@iv.@available_to_allocate`:

- `@iv`

    - `@iv.@available_to_allocate` = `??` – `??` – `@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Legge til andre fysiske mål i det beregnede målet som er tilgjengelig for tildeling

Hvis du vil bruke tildeling, må du definere formelen korrekt for det tilgjengelig-for-tildeling-beregnede målingen(`@iv.@available_to_allocate`). Du har for eksempel `fno`-datakilden og `onordered`-målet, `pos`-datakilden og `inbound`-målet, og du vil gjøre tildeling på lagerbeholdningen for summen `fno.onordered` og `pos.inbound`. I dette tilfellet skal `@iv.@available_to_allocate` inneholde `pos.inbound` og `fno.onordered` i formelen. Her er et eksempel:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

> [!NOTE]
> Datakilden `@iv` er en forhåndsdefinert datakilde, og de fysiske målene som er definert i `@iv` med prefiks `@`, er forhåndsdefinerte mål. Disse målene er en forhåndsdefinert konfigurasjon for fordelingsfunksjonen, så ikke endre eller slett dem, ellers vil du sannsynligvis oppleve uventede feil når du bruker fordelingsfunksjonen.
>
> Du kan legge til nye fysiske mål i det forhåndsdefinerte beregnede målet `@iv.@available_to_allocate`, men du må ikke endre navnet.

### <a name="manage-allocation-groups"></a>Behandle tildelingsgrupper

Maksimalt åtte tildelingsgruppenavn kan angis. Gruppene har et hierarki. Følg denne fremgangsmåten for å vise og oppdatere tildelingsgrupper.

1. Logg deg på Power Apps-miljøet, og åpne **Lagersynlighet**.
1. Åpne **Konfigurasjon**-siden, og velg deretter **Rediger konfigurasjon** i kategorien **Tildeling**. Som standard er det et tildelingshierarki som har fire lag: `Channel` (topplag), `customerGroup` (andre lag),`Region` (tredje lag) og `OrderType` (fjerde lag).
1. Du kan fjerne en eksisterende fordelingsgruppe ved å velge **X** ved siden av den. Du kan også legge til nye tildelingsgrupper i hierarkiet ved å angi navnet på hver nye gruppe direkte i feltet.

    > [!IMPORTANT]
    > Vær forsiktig når du sletter eller endrer tilordningshierarkitilordningen. Hvis du vil ha retningslinjer, kan du se [Tips for bruk av tildeling](#allocation-tips).

1. Når du er ferdig med å konfigurere innstillingene for fordelingsgruppen og hierarkiet, lagrer du endringene og velger deretter **Oppdater konfigurasjon** øverst til høyre. Verdiene til de konfigurerte tildelingsgruppene blir oppdatert når du oppretter en tilordning ved hjelp av enten brukergrensesnittet eller API POST (/api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/allocate). Du finner begge fremgangsmåtene senere i denne artikkelen.

Hvis du bruker fire gruppenavn og setter dem til \[`channel`, `customerGroup`, `region`, `orderType`\], vil disse navnene være gyldige for tildelingsrelaterte forespørsler når du kaller API for konfigurasjonsoppdatering.

### <a name="tips-for-using-allocation"></a><a name="allocation-tips"></a>Tips for bruk av tildeling

- For hvert produkt bør fordelingsfunksjonen bruke på samme *dimensjonsnivå* i henhold til produktindekshierarkiet du angir i [konfigurasjonen for produktindekshierarkiet](inventory-visibility-configuration.md#index-configuration). La oss for eksempel anta at indekshierarkiet er \[`Site`, `Location`, `Color`, `Size`\]. Hvis du tildeler et antall for ett produkt på dimensjonsnivået \[`Site`, `Location`, `Color`\], bør du også tildele på samme nivå, \[`Site`, `Location`, `Color`\], neste gang du ønsker å tildele dette produktet. Hvis du bruker nivået \[`Site`, `Location`, `Color`, `Size`\] eller \[`Site`, `Location`\], vil dataene være inkonsekvente.
- **Endre tildelingsgrupper og hierarkiet:** Hvis det allerede finnes tildelingsdata i systemet, vil sletting av eksisterende tildelingsgrupper eller et skift i hierarkiet for tildelingsgrupper ødelegge den eksisterende tilordningen mellom tildelingsgruppene. Husk derfor å rydde opp i alle de gamle dataene manuelt før du oppdaterer den nye konfigurasjonen. Fordi tillegget av nye tildelingsgrupper i det laveste hierarkiet ikke påvirker eksisterende tilordninger, behøver du imidlertid ikke å rydde opp i dataene.
- Tildelingen vil bare lykkes hvis produktet har et positivt `available_to_allocate`-antall.
- Hvis du vil tildele produkter fra en gruppe på et høyt *tildelingsnivå* til en undergruppe, bruker du API-en `Reallocate`. Hvis du for eksempel har et hierarki for tildelingsgrupper, \[`channel`, `customerGroup`, `region`, `orderType`\], og du ønsker å tildele noen produkter fra tildelingsgruppen \[Online, VIP\] til tildelingsundergruppen \[Online, VIP, EU\], bruker du API-en `Reallocate` til å flytte antallet. Hvis du bruker API-en `Allocate`, vil den tildele antallet fra det virtuelle fellesutvalget.
- Hvis du vil vise generell produkttilgjengelighet (fellespuljen), bruker du [Spør om beholdning](inventory-visibility-api.md#query-on-hand)-APIen for å be om lagerbeløpet som er *tilgjengelig for tildeling*. Du kan deretter foreta fordelingsavgjørelser basert på denne informasjonen.

## <a name="use-the-allocation-api"></a><a name="using-allocation-api"></a>Bruke tildelings-API

I øyeblikket åpnes fem tildelings-APIer:

- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/allocate** – Denne API-en brukes til å opprette den innledende tilordningen.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/unallocate** – Denne API-en brukes til å reversere eller fjerne de tildelte antallene.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/reallocate** – Denne API-en brukes til å flytte det tilordnede antallet fra en eksisterende tildeling til andre tildelingsgrupper.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/consume** – Denne API-en brukes til å trekkefra (bruke) det tildelte antallet.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/query** – Denne API-en brukes til å kontrollere eksisterende tildelingsposter mot tildelingsgruppene og hierarkiet.

### <a name="allocate"></a>Tildel

Kall API for `Allocate` for å tildele et produkt som har bestemte dimensjoner. Her er skjemaet for forespørselsteksten.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
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
    "id": "test101",
    "productId": "Bike",
    "groups": {
        "channel": "Web",
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

### <a name="unallocate"></a>Ikke-tilordnet

Bruke API for `Unallocate` til å tilbakeføre `Allocate`-operasjonen. Negativt antall er ikke tillatt i en `Allocate`-operasjon. Teksten i `Unallocate` er identisk med teksten i `Allocate`.

### <a name="reallocate"></a>Tildel på nytt

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
    "groups": {
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
    "id": "test102",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "groups": {
        "channel": "Web",
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

### <a name="consume"></a>Forbruk

Bruk API for `Consume` til å postere forbruksantallet mot fordeling. Du kan for eksempel bruke denne API-en til å flytte tildelt antall til noen reelle mål. Her er skjemaet for forespørselsteksten.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
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
    "id": "test103",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
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

I denne forespørselen legger du merke til at det fysiske målet du bruker i hovedteksten for forbruksforespørselen, bør bruke motsatt modifikatortype (Addisjon eller Subtraksjon), sammenlignet med modifikatortypen som brukes i det beregnede målet. Så i denne forbruksteksten har `iv.inbound` verdien `Subtraction`, ikke `Addition`.

`fno`-datakilden kan ikke brukes i forbruksteksten, fordi vi alltid har gjort krav på at lagersynlighet ikke kan endre noen data for `fno`-datakilden. Dataflyten er enveisveis, som betyr at alle antallsendringer for datakilden `fno` må komme fra Supply Chain Management-miljøet.

### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a>Forbruk som en myk reservasjon

API for `Consume` kan også forbruke det tildelte antallet som en myk reservering. I dette tilfellet vil operasjonen `Consume` redusere det tildelte antallet, og deretter gjøre en myk reservering for dette antallet. For å bruke denne fremgangsmåten må du også bruke [myk reservasjon](inventory-visibility-reservations.md)-funksjonen i Lagersynlighet.

Du har for eksempel angitt en ikke-forpliktende fysisk mål til `iv.softreserved`. Følgende formel brukes for beregnet mål for tilgjengelig til reserve:

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
    "groups": {
        "channel": "Web",
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

### <a name="query"></a>Forespørsel

Bruk API-en `Query` til å hente tildelingsrelatert informasjon for noen produkter. Du kan bruke dimensjonsfiltre og tilordningsgruppefiltre til å begrense resultatene. Dimensjonene må samsvare ut fra det du vil hente, for eksempel \[område=1, lokasjon=11\] vil ha ikke-relaterte resultater sammenlignet med \[område=1, lokasjon=11, farge=rød\].

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
        "channel": "Web",
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
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

## <a name="use-the-allocation-user-interface"></a>Bruke brukergrensesnittet for tildeling

Du kan manuelt styre tildelinger via brukergrensesnittet ved å åpne Lagersynlighet-appen og gå til **Driftssynlighet \> Tildeling**. Derfra kan du utføre alle handlingene som er beskrevet i følgende underseksjoner.

### <a name="create-an-allocation"></a>Opprette en tildeling

Følg denne fremgangsmåten for å opprette en tildeling fra siden **Tildeling** i Lagersynlighet-appen.

1. Velg **Tildel**.
1. Angi verdier for basisfelt, dimensjoner og målfordelingsgrupper. (Når du velger samledatakilden i **Dimensjondelen**-delen, bruker du først rullegardinlisten til å angi dimensjonene (for eksempel `siteId`). Deretter angir du dimensjonsverdier i feltene som vises.)
1. Velg **Send**.

### <a name="consume-an-allocation"></a>Bruke en tildeling

Velg **Forbruk** for å forbruke en tildeling. For å sikre at du bruker innenfor den riktige tildelingsgruppen og hierarkiet, angir du de samme settene med organisasjons- og dimensjonsdetaljer som du angav da du opprettet tildelingen.

### <a name="reallocate-an-allocation"></a>Tildele en tildeling på nytt

Velg **Tildel på nytt** å flytte eksisterende tildelt antall fra et sett med tildelingsgrupper til et annet.

### <a name="query-existing-allocations"></a>Spør på eksisterende tildelinger

Velg **Spørring**, og angi deretter produkt-, organisasjons-, dimensjons- og tildelingsgruppeverdier for å hente spørringsresultater for eksisterende tildelinger.
