---
title: Offentlige API-er for lagersynlighet
description: Denne artikkelen beskriver de offentlige API-ene som leveres av Lagersynlighet.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8b0b8ca261237fbb2190f2a94cc11b816ae05af5
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762841"
---
# <a name="inventory-visibility-public-apis"></a>Offentlige API-er for lagersynlighet

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver de offentlige API-ene som leveres av Lagersynlighet.

Den offentlige REST-API-en i tillegget for lagersynlighet viser flere spesifikke endepunkter for integrering. Det støtter fire hovedtyper for samhandling:

- Postering av beholdningsendringer i tillegget fra et eksternt system
- Angi eller overstyre lagerbeholdningsantall i tillegget fra et eksternt system
- Postering av reservasjonshendelser i tillegget fra et eksternt system
- Spørring etter gjeldende antall i beholdningen fra et eksternt system

Følgende tabell viser API-ene som er tilgjengelige for øyeblikket:

| Bane | Metode | beskrivelse |
|---|---|---|
| /api/environment/{environmentId}/onhand | Poster | [Opprett én lagerendringshendelse](#create-one-onhand-change-event)|
| /api/environment/{environmentId}/onhand/bulk | Poster | [Opprett flere endringshendelser](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | Poster | [Angi/overstyre lagerbeholdninger](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | Poster | [Opprett én ikke-forpliktende reservasjonshendelse](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | Poster | [Opprett flere ikke-forpliktende reservasjonshendelser](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/unreserve | Poster | [Tilbakefør én ikke-forpliktende reservasjonshendelse](#reverse-one-reservation-event) |
| /api/environment/{environmentId}/onhand/unreserve/bulk | Poster | [Tilbakefør flere ikke-forpliktende reservasjonshendelser](#reverse-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/changeschedule | Poster | [Opprett én planlagt lagerendring](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/changeschedule/bulk | Poster | [Opprett flere lagerendringer med datoer](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/indexquery | Poster | [Spørring ved å bruke posteringsmetoden](#query-with-post-method) (anbefalt) |
| /api/environment/{environmentId}/onhand | Hent | [Spør ved å bruke hentemetoden](#query-with-get-method) |
| /api/environment/{environmentId}/onhand/exactquery | Poster | [Nøyaktig spørring ved å bruke posteringsmetoden](#exact-query-with-post-method) |
| /api/environment/{environmentId}/allocation<wbr>/allocate | Poster | [Opprett én tildelingshendelse](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/unallocate | Poster | [Opprett én ikke-tilordnet-hendelse](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/reallocate | Poster | [Opprett én hendelse for ny tildeling](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/consume | Poster | [Opprett én konsumeringshendelse](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/query | Poster | [Fordelingsresultat for spørring](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> Delen {environmentId} av banen er miljø-IDen i Microsoft Dynamics Lifecycle Services.
> 
> Bulk-API-en kan returnere maksimalt 512 poster for hver forespørsel.

Microsoft har levert en *Postman*-forespørselssamling ut av boksen. Du kan importere denne samlingen til *Postman*-programvaren ved hjelp av følgende delte kobling: <https://www.getpostman.com/collections/95a57891aff1c5f2a7c2>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a><a name = "endpoint-lcs"></a>Finn sluttpunktet i henhold til Lifecycle Services-miljøet

Mikrotjenesten Lagersynlighet distribueres i Microsoft Azure Service Fabric i flere geografiske områder og regioner. Det er for øyeblikket ikke et sentralt sluttpunkt som automatisk kan sende forespørselen til tilsvarende geografi og område. Derfor må du opprette informasjonsdeler i en URL ved hjelp av følgende mønster:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Det korte navnet på regionen kan finnes i Lifecycle Services-miljøet. Følgende tabell viser områdene som er tilgjengelige for øyeblikket.

| Azure-område        | Kortnavn for område |
| ------------------- | ----------------- |
| Australia øst      | eau               |
| Australia, sørøst | seau              |
| Midt-Canada      | cca               |
| Canada, øst         | eca               |
| Europa nord        | neu               |
| Europa vest         | weu               |
| USA øst             | eus               |
| USA vest             | wus               |
| Storbritannia sør            | suk               |
| Storbritannia vest             | wuk               |
| Japan, øst          | ejp               |
| Japan, vest          | wjp               |
| India sentralt       | cin               |
| India sør         | sin               |
| Sveits, nord   | nch               |
| Sveits, vest    | wch               |
| Frankrike, sør        | sfr               |
| Asia øst           | eas               |
| Asia, sørøst     | seas              |
| De forente arabiske emirater, nord           | nae               |
| Øst-Norge         | eno               |
| Vest-Norge         | wno               |
| Sør-Afrika, vest   | wza               |
| Sør-Afrika, nord  | nza               |

Øynummeret er der Lifecycle Services-miljøet distribueres på Service Fabric. Det er for øyeblikket ingen måte å hente denne informasjonen fra brukersiden på.

Microsoft har bygd et brukergrensesnitt i Power Apps, slik at du kan få det fullstendige sluttpunktet for mikrotjenesten. Hvis du ønsker mer informasjon, se [Finn endepunkt for tjeneste](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Godkjenning

Platformsikkerhetstokenet brukes til å kalle inn den offentlige API-en for lagersynlighet. Derfor må du generere et *Azure Active Directory-token (Azure AD)* ved hjelp av Azure AD-appen. Du må deretter bruke Azure AD-tokenet til å få *tilgangstokenet* fra sikkerhetstjenesten.

Microsoft leverer en *Postman*-tokensamling ut av boksen. Du kan importere denne samlingen til *Postman*-programvaren ved hjelp av følgende delte kobling: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Hvis du vil hente et token for sikkerhetstjeneste, gjør du følgende:

1. Logg på Azure-portalen, og bruk den til å finne `clientId`- og `clientSecret`-verdiene for Dynamics 365 Supply Chain Management-appen.
1. Hent et Azure AD-token (`aadToken`) ved å sende en HTTP-forespørsel som har følgende egenskaper:

    - **Nettadresse:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/v2.0/token`
    - **Metode:** `GET`
    - **Meldingstekst (skjemadata):**

        | Nøkkel           | Verdi                                            |
        | ------------- | -------------------------------------------------|
        | client_id     | ${aadAppId}                                      |
        | client_secret | ${aadAppSecret}                                  |
        | grant_type    | client_credentials                               |
        | scope         | 0cdb527f-a8d1-4bf8-9436-b352c68682b2/.default    |

    Du skal motta et Azure AD-token (`aadToken`) som svar. Den skal ligne følgende eksempel.

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. Former en JavaScript Object Notation-forespørsel (JSON) som ligner på følgende eksempel.

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type": "aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope": "https://inventoryservice.operations365.dynamics.com/.default",
        "context": "{$LCS_environment_id}",
        "context_type": "finops-env"
    }
    ```

    Merk følgende punkt:

    - Verdien for `client_assertion` må være Azure AD-tokenet (`aadToken`) som du mottok i forrige trinn.
    - Verdien for `context` må være Lifecycle Services-miljø-ID-en der du vil implementere tillegget.
    - Angi de andre verdiene som vist i eksemplet.

1. Hent et tilgangstoken (`access_token`) ved å sende en HTTP-forespørsel som har følgende egenskaper:

    - **URL-adresse:** `https://securityservice.operations365.dynamics.com/token`
    - **Metode:** `POST`
    - **HTTP-hode:** Inkluder API-versjonen. (Nøkkelen er `Api-Version`, og verdien er `1.0`.)
    - **Meldingstekst:** Ta med JSON-forespørselen du opprettet i forrige trinn.

    Du skal motta et tilgangstoken (`access_token`) som svar. Du må bruke dette tokenet som bærertoken for å kalle opp lagersynlighets-API-en. Her er et eksempel.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 3600
    }
    ```

> [!IMPORTANT]
> Når du bruker *Postman*-forespørselssamlingen til å kalle felles APIer for lagersynlighet, må du legge til et bærertoken for hver forespørsel. Hvis du vil finne bærertokenet, velger du kategorien **Autorisasjon** under forespørsels-URL-adressen, velger typen **Bærertoken** og kopierer tilgangstokenet som ble hentet i siste trinn. I senere deler i denne artikkelen brukes `$access_token` til å representere tokenet som ble hentet i siste trinn.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Opprett lagerendringshendelser

Det finnes to API-er for oppretting av lagerendringshendelser:

- Opprett én oppføring: `/api/environment/{environmentId}/onhand`
- Opprett flere oppføringer: `/api/environment/{environmentId}/onhand/bulk`

Tabellen nedenfor summerer betydningen av hvert felt i JSON-teksten.

| Felt-ID | Beskrivelse |
|---|---|
| `id` | En unik ID for den bestemte endringshendelsen. Hvis det forekommer en ny sending på grunn av en tjenestefeil, brukes denne ID-en til å sikre at samme hendelse ikke telles to ganger i systemet. |
| `organizationId` | Identifikatoren til organisasjonen som er koblet til hendelsen. Denne verdien tilordnes til en ID for organisasjon eller dataområde i Supply Chain Management. |
| `productId` | Identifikatoren for produktet. |
| `quantities` | Antallet som antall på lager må endres etter. Hvis for eksempel 10 nye bøker legges til på en hylle, vil denne verdien være `quantities:{ shelf:{ received: 10 }}`. Hvis tre bøker fjernes fra hyllen eller selges, vil denne verdien være `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Datakilden for dimensjonene som brukes i posteringsendringshendelsen og -spørringen. Hvis du angir datakilden, kan du bruke de egendefinerte dimensjonene fra den angitte datakilden. Lagersynlighet kan bruke dimensjonskonfigurasjonen til å tilordne de egendefinerte dimensjonene til de generelle standarddimensjonene. Hvis ingen `dimensionDataSource`-verdi er angitt, kan du bare bruke de generelle [basisdimensjonene](inventory-visibility-configuration.md#data-source-configuration-dimension) i spørringene. |
| `dimensions` | Et dynamisk nøkkel/verdi-par. Verdiene er tilordnet til noen av dimensjonene i Supply Chain Management. Du kan imidlertid også legge til egendefinerte dimensjoner (for eksempel *Kilde*) for å angi om hendelsen kommer fra Supply Chain Management eller et eksternt system. |

> [!NOTE]
> Parameterne `siteId` og `locationId` konstruerer [partisjonskonfigurasjonen](inventory-visibility-configuration.md#partition-configuration). Derfor må du angi dem i dimensjoner når du oppretter lagerendringshendelser, angir eller overstyrer lagerbeholdninger eller oppretter reservasjonshendelser.

Følgende del er eksempler som viser hvordan du bruker disse APIene.

### <a name="create-one-on-hand-change-event"></a><a name="create-one-onhand-change-event"></a>Opprett én lagerendringshendelse

Denne API-en oppretter én enkelt lagerendringshendelse.

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string, # Optional
        dimensions: {
            [key:string]: string,
        },
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
    }
```

Følgende eksempel viser eksempeltekstinnholdet. I dette eksemplet har firmaet et POS-system (salgssted) som behandler transaksjoner i butikk og dermed lagerendringer. Kunden har returnert en rød T-skjorte til butikken. For å reflektere endringer kan du postere en endringshendelse for produktet *T-skjorte*. Denne hendelsen vil øke antallet for produktet *T-skjorte* med 1.

```json
{
    "id": "Test201",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "posMachineId": "0001",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

Følgende eksempel viser eksempeltekstinnholdet uten `dimensionDataSource`. I dette tilfellet vil `dimensions` være [basisdimensjoner](inventory-visibility-configuration.md#data-source-configuration-dimension). Hvis `dimensionDataSource` er angitt, kan `dimensions` være enten datakildedimensjonene eller basisdimensjonene.

```json
{
    "id": "Test202",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Opprett flere endringshendelser

Denne API-en kan opprette endringshendelser, på samme måten som [API-en med enkelthendelser](#create-one-onhand-change-event) kan. Den eneste forskjellen er at denne API-en kan opprette flere poster samtidig. Derfor er verdiene `Path` og `Body` forskjellige. For denne API-en inneholder `Body` en matrise med poster. Maksimalt antall oppføringer er 512. Derfor kan bulk-API-en for lagerbeholdningendring støtte opptil 512 endringshendelser om gangen. 

En detaljhandelsbutikk POS-maskin behandlet for eksempel følgende to transaksjoner:

- En returordre med en rød T-skjorte
- En salgstransaksjon av tre sorte T-skjorter

I dette tilfellet kan du ta med begge lageroppdateringene i én API-samtale.

```txt
Path:
    /api/environment/{environmentId}/onhand/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
        ...
    ]
```

Følgende eksempel viser eksempeltekstinnholdet.

```json
[
    {
        "id": "Test203",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "Site1",
            "LocationId": "11",
            "posMachineId&quot;: &quot;0001"
            "colorId&quot;: &quot;red"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensions": {
            "siteId": "1",
            "locationId": "11",
            "colorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Angi/overstyre lagerbeholdninger

API-en *Angi lagerbeholdning* overstyrer de gjeldende dataene for det angitte produktet. Denne funksjonaliteten brukes vanligvis til å oppdatere lageropptelling. I løpet av den daglige lageropptellingen kan for eksempel en butikk finne ut at den faktiske lagerbeholdningen for en rød T-skjorte er 100. Derfor må det innkommende antallet i POS oppdateres til 100, uansett hva det forrige antallet var. Du kan bruke denne API-en til å overstyre den eksisterende verdien.

```txt
Path:
    /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifiedDateTimeUTC: datetime,
        },
        ...
    ]
```

Følgende eksempel viser eksempeltekstinnholdet. Virkemåten til denne API-en er forskjellig fra virkemåten til API-ene som er beskrevet i delen [Opprett lagerendringshendelser](#create-onhand-change-event) tidligere i denne artikkelen. I dette eksemplet blir antallet for produktet *T-skjorte* angitt til 1.

```json
[
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "posMachineId": "0001"
            "colorId": "red"
        },
        "quantities": {
            "pos": {
                "inbound": 100
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Opprett reservasjonshendelser

Hvis du vil bruke API-en *Reserver*, må du aktivere reservasjonsfunksjonen og fullføre reservasjonskonfigurasjonen. Hvis du vil ha mer informasjon (inkludert en dataflyt og et eksempelscenario), kan du se [Reserveringskonfigurasjon (valgfritt)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Opprett én reservasjonshendelse

En reservering kan gjøres mot ulike datakildeinnstillinger. Hvis du vil konfigurere denne reserveringstypen, må du først angi datakilden i `dimensionDataSource` parameteren. I parameteren `dimensions` kan du deretter angi dimensjoner i henhold til dimensjonsinnstillingene i måldatakilden.

Når du kaller reservasjons-API, kan du styre reservasjonsvalideringen ved å angi den boolske `ifCheckAvailForReserv` parameteren i forespørselsteksten. Verdien `True` betyr at valideringen kreves, mens en verdi å `False` betyr at valideringen ikke er nødvendig. Standardverdien er `True`.

Hvis du vil tilbakeføre en reservering eller ikke reservere angitte lagerantall, setter du antallet til en negativ verdi og setter parameteren `ifCheckAvailForReserv` til `False` for å hoppe over valideringen. Det finnes også en dedikert API for opphevelse av reservasjon som gjør det samme. Forskjellen er bare i måten de to API-ene kalles opp på. Det er enklere å tilbakeføre en bestemt reservasjonshendelse ved å bruke `reservationId` med API-en for *opphevelse av reservasjon*. Hvis du vil ha mer informasjon, kan du se delen [Oppheve reservasjon av én reservasjonshendelse](#reverse-reservation-events).

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string,
        dimensions: {
            [key:string]: string,
        },
        quantityDataSource: string, # optional
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
        modifier: string,
        quantity: number,
        ifCheckAvailForReserv: boolean,
    }
```

Følgende eksempel viser eksempeltekstinnholdet.

```json
{
    "id": "reserve-0",
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softReservOrdered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red",
        "sizeId&quot;: &quot;small"
    }
}
```

Følgende eksempel viser et vellykket svar.

```json
{
    "reservationId": "RESERVATION_ID",
    "id": "ohre~id-822-232959-524",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
``` 

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Opprett flere reservasjonshendelser

Denne API-en er en masseversjon av [API-en for enkelthendelser](#create-reservation-events).

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string,
            dimensions: {
                [key:string]: string,
            },
            quantityDataSource: string, # optional
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifier: string,
            quantity: number,
            ifCheckAvailForReserv: boolean,
        },
        ...
    ]
```

## <a name="reverse-reservation-events"></a>Tilbakefør reservasjonshendelser

API-en *Opphev reservasjon* fungerer som tilbakeføringsoperasjonen for [*Reservasjon*](#create-reservation-events)-hendelser. Det brukes til å tilbakeføre en reservasjonshendelse som er angitt av `reservationId`, eller til å redusere reserveringsantallet.

### <a name="reverse-one-reservation-event"></a><a name="reverse-one-reservation-event"></a>Tilbakefør én reservasjonshendelse

Når en reservasjon opprettes, blir en `reservationId` tatt med i svarteksten. Du må angi samme `reservationId` for å avbryte reservasjonen og ta med samme `organizationId` og `dimensions` som brukes for reservasjons-API-oppkallet. Til slutt angir du en `OffsetQty`-verdi som representerer antall varer som skal frigjøres fra forrige reservasjon. En reservasjon kan enten tilbakeføres fullstendig eller delvis, avhengig av angitt `OffsetQty`. Hvis for eksempel *100* enheter med varer er reservert, kan du angi `OffsetQty: 10` for å oppheve reservasjonen av *10* av den opprinnelige reserverte mengden.

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        reservationId: string,
        dimensions: {
            [key:string]: string,
        },
        OffsetQty: number
    }
```

Følgende kode viser et eksempel på tekstinnhold.

```json
{
    "id": "unreserve-0",
    "organizationId": "SCM_IV",
    "reservationId": "RESERVATION_ID",
    "dimensions": {
        "siteid":"iv_postman_site",
        "locationid":"iv_postman_location",
        "ColorId": "red",
        "SizeId&quot;: &quot;small"
    },
    "OffsetQty": 1
}
```

Følgende kode viser et eksempel på en vellykket svartekst.

```json
{
    "reservationId": "RESERVATION_ID",
    "totalInvalidOffsetQtyByReservId": 0,
    "id": "ohoe~id-823-11744-883",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
```

> [!NOTE]
> Når `OffsetQty` er mindre enn eller lik reservasjonsmengden i svarteksten, blir `processingStatus` "*success*" og `totalInvalidOffsetQtyByReservId` *0*.
>
> Hvis `OffsetQty` er større enn den reserverte mengden, blir `processingStatus`"*partialSuccess*" og `totalInvalidOffsetQtyByReservId` differansen mellom `OffsetQty` og den reserverte mengden.
>
>Hvis reservasjonen for eksempel har et antall på *10* og `OffsetQty` har verdien *12*, blir `totalInvalidOffsetQtyByReservId` *2*.

### <a name="reverse-multiple-reservation-events"></a><a name="reverse-multiple-reservation-events"></a>Tilbakefør flere reservasjonshendelser

Denne API-en er en masseversjon av [API-en for enkelthendelser](#reverse-one-reservation-event).

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [      
        {
            id: string,
            organizationId: string,
            reservationId: string,
            dimensions: {
                [key:string]: string,
            },
            OffsetQty: number
        }
        ...
    ]
```

## <a name="query-on-hand"></a>Spør om beholdning

Bruk API-en *Spør om beholdning* til å hente gjeldende lagerbeholdningsdata for produktene dine. Du kan bruke denne API-en hver gang du må vite beholdningen, for eksempel når du vil gå gjennom produktbeholdningsnivåene på webområdet for e-handel, eller når du vil kontrollere produkttilgjengeligheten i alle regioner eller i butikker og lagre i nærheten. API støtter for øyeblikket spørringer på opptil 5000 individuelle varer etter `productID`-verdi. Flere `siteID`- og `locationID`-verdier kan også angis i hver spørring. Maksimumsgrensen defineres av følgende ligning:

*NumOf(SiteID) \* NumOf(LocationID) <= 100*.

### <a name="query-by-using-the-post-method"></a><a name="query-with-post-method"></a>Spør ved å bruke posteringsmetoden

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            siteId: string[],
            locationId: string[],
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

I hoveddelen av denne forespørselen er `dimensionDataSource` fremdeles en valgfri parameter. Hvis den ikke er definert, behandles `filters` som *basisdimensjoner*. Det finnes fire obligatoriske felt for `filters`: `organizationId`, `productId`, `siteId` og `locationId`.

- `organizationId` skal bare inneholde én verdi, men den er likevel en matrise.
- `productId` kan inneholde én eller flere verdier. Hvis den er en tom matrise, vil alle produkter bli returnert.
- `siteId` og `locationId` brukes for partisjonering i lagersynlighet. Du kan angi mer enn én `siteId` og `locationId` verdi i en forespørsel om *lagerbeholdning*. I den gjeldende versjonen må du angi både `siteId` og `locationId` verdier.

Vi foreslår at du bruker parameteren `groupByValues` for å følge konfigurasjonen din for indeksering. Hvis du vil ha mer informasjon, kan du se [Konfigurasjon av produktindekshierarki](./inventory-visibility-configuration.md#index-configuration).

Parameteren `returnNegative` styrer om resultatene inneholder negative oppføringer.

> [!NOTE]
> Hvis du har aktivert endringsplanen for lagerbeholdning og ATP-funksjoner (available-to-promise), kan spørringen også omfatte den boolske `QueryATP`-parameteren, som styrer om resultatet av spørringen omfatter ATP-informasjon. Hvis du vil ha mer informasjon og flere eksempler, kan du se [Tidsplaner for lagerendringer i Lagersynlighet og leveringskapasitet](inventory-visibility-available-to-promise.md).

Følgende eksempel viser eksempeltekstinnholdet. Det viser at du kan spørre i lagerbeholdningen fra flere lokasjoner (lagre).

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "locationId": ["11","12","13"],
        "colorId": ["red"]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

Eksemplet nedenfor viser hvordan du spør på alle produkter på et bestemt område og sted.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "locationId": ["11"],
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Spør ved å bruke hentemetoden

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Get
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Query(Url Parameters):
    groupBy
    returnNegative
    [Filters]
```

Her er et eksempel på henting av en nettadresse. Denne hentforespørselen er nøyaktig den samme som posteringseksemplet som ble angitt tidligere.

```txt
/api/environment/{environmentId}/onhand?organizationId=SCM_IV&productId=iv_postman_product&siteId=iv_postman_site&locationId=iv_postman_location&colorId=red&groupBy=colorId,sizeId&returnNegative=true
```

## <a name="on-hand-exact-query"></a><a name="exact-query-with-post-method"></a>Nøyaktig spørringsforespørsel om beholdning

Nøyaktig spørringsforespørsel om beholdning ligner vanlige lagerbeholdningsspørringer, men de lar deg angi et tilordningshierarki mellom et område og en lokasjon. Du har for eksempel følgende to områder:

- Område 1, som er tilordnet til lokasjon A
- Område 2, som er tilordnet til lokasjon B

For en vanlig beholdningsspørring, hvis du angir `"siteId": ["1","2"]` og `"locationId": ["A","B"]`, vil lagersynlighet automatisk spørre etter resultatet for følgende områder og lokasjoner:

- Område 1, plassering A
- Område 1, plassering B
- Område 2, plassering A
- Område 2, plassering B

Som du ser, gjenkjenner ikke den vanlige lagerbeholdning at lokasjon A bare finnes i område 1, og lokasjon B finnes bare i område 2. Derfor gjør det overflødige spørringer. For å legge til rette for denne hierarkiske tilordningen, kan du bruke en nøyaktig spørring på lager og angi lokasjonstilordningene i spørringsteksten. I dette tilfellet vil du utføre spørringer og motta resultater for område 1, sted A og område 2, lokasjon B.

### <a name="exact-query-by-using-the-post-method"></a><a name="exact-query-with-post-method"></a>Nøyaktig spørring ved å bruke posteringsmetoden

```txt
Path:
    /api/environment/{environmentId}/onhand/exactquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            dimensions: string[],
            values: string[][],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

I hoveddelen av denne forespørselen er `dimensionDataSource` en valgfri parameter. Hvis den ikke er definert, behandles `dimensions` i `filters` som *basisdimensjoner*. Det finnes fire obligatoriske felt for `filters`: `organizationId`, `productId`, `dimensions` og `values`.

- `organizationId` skal bare inneholde én verdi, men den er likevel en matrise.
- `productId` kan inneholde én eller flere verdier. Hvis den er en tom matrise, vil alle produkter bli returnert.
- I matrisen `dimensions` er `siteId` og `locationId` nødvendig, men kan vises med andre elementer i hvilken som helst rekkefølge.
- `values` kan inneholde én eller flere atskilte tupler med verdier som tilsvarer `dimensions`.

`dimensions` i `filters` vil automatisk bli lagt til i `groupByValues`.

Parameteren `returnNegative` styrer om resultatene inneholder negative oppføringer.

Følgende eksempel viser eksempeltekstinnholdet.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": ["iv_postman_product"],
        "dimensions": ["siteId", "locationId", "colorId"],
        "values" : [
            ["iv_postman_site", "iv_postman_location", "red"],
            ["iv_postman_site", "iv_postman_location", "blue"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

Eksemplet nedenfor viser hvordan du spør på alle produkter i flere områder og lokasjoner.

```json
{
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": [],
        "dimensions": ["siteId", "locationId"],
        "values" : [
            ["iv_postman_site_1", "iv_postman_location_1"],
            ["iv_postman_site_2", "iv_postman_location_2"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

## <a name="available-to-promise"></a>Tilgjengelig for ordre

Du kan konfigurere Lagersynlighet slik at du kan planlegge fremtidige endringer i lagerbeholdningen og beregne ATP-antall. ATP er antallet av en vare som er tilgjengelig og kan loves til en kunde i løpet av den neste perioden. Bruk av ATP-beregningen kan øke kapasiteten for innfrielse av bestillinger betydelig. Hvis du vil ha informasjon om hvordan du aktiverer denne funksjonen, og hvordan du samhandler med Lagersynlighet via API-en etter at funksjonen er aktivert, kan du se [Tidsplaner for lagerendringer i Lagersynlighet og leveringskapasitet](inventory-visibility-available-to-promise.md#api-urls).

## <a name="allocation"></a>Tilordning

Tildelingsrelaterte API-er finnes i [lagersynlighetstilordning](inventory-visibility-allocation.md#using-allocation-api).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
