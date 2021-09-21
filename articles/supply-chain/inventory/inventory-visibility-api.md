---
title: Offentlige API-er for lagersynlighet
description: Dette emnet beskriver de offentlige API-ene som leveres av Lagersynlighet.
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
ms.openlocfilehash: 6dff54f54a495c2b4a7837f3a41f410d418cf12b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474658"
---
# <a name="inventory-visibility-public-apis"></a>Offentlige API-er for lagersynlighet

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Dette emnet beskriver de offentlige API-ene som leveres av Lagersynlighet.

Den offentlige REST-API-en i tillegget for lagersynlighet viser flere spesifikke endepunkter for integrering. Det støtter fire hovedtyper for samhandling:

- Postering av beholdningsendringer i tillegget fra et eksternt system
- Angi eller overstyre lagerbeholdningsantall i tillegget fra et eksternt system
- Postering av reservasjonshendelser i tillegget fra et eksternt system
- Spørring etter gjeldende antall i beholdningen fra et eksternt system

Følgende tabell viser API-ene som er tilgjengelige for øyeblikket:

| Bane | Metode | beskrivelse |
|---|---|---|
| /api/environment/{environmentId}/onhand | Poster | [Opprett én lagerendringshendelse](#create-one-onhand-change-event) |
| /api/environment/{environmentId}/onhand/bulk | Poster | [Opprett flere endringshendelser](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | Poster | [Angi/overstyre lagerbeholdninger](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | Poster | [Opprett én reservasjonshendelse](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | Poster | [Opprett flere reservasjonshendelser](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/indexquery | Hent | [Spør ved å bruke posteringsmetoden](#query-with-post-method) |
| /api/environment/{environmentId}/onhand/indexquery | Poster | [Spør ved å bruke hentemetoden](#query-with-get-method) |

Microsoft har levert en *Postman*-forespørselssamling ut av boksen. Du kan importere denne samlingen til *Postman*-programvaren ved hjelp av følgende delte kobling: <https://www.getpostman.com/collections/90bd57f36a789e1f8d4c>.

> [!NOTE]
> Delen {environmentId} av banen er miljø-IDen i Microsoft Dynamics Lifecycle Services (LCS).

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>Finn sluttpunktet i henhold til Lifecycle Services-miljøet

Mikrotjenesten Lagersynlighet distribueres i Microsoft Azure Service Fabric i flere geografiske områder og regioner. Det er for øyeblikket ikke et sentralt sluttpunkt som automatisk kan sende forespørselen til tilsvarende geografi og område. Derfor må du opprette informasjonsdeler i en URL ved hjelp av følgende mønster:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Det korte navnet på regionen kan finnes i Microsoft Dynamics Lifecycle Services-miljøet (LCS). Følgende tabell viser områdene som er tilgjengelige for øyeblikket.

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
| Brasil, sør        | sbr               |
| USA sentralt i sør    | scus              |

Øynummeret er der LCS-miljøet distribueres på Service Fabric. Det finnes for øyeblikket ingen måte å hente denne informasjonen fra brukersiden på.

Microsoft har bygd et brukergrensesnitt i Power Apps, slik at du kan få det fullstendige sluttpunktet for mikrotjenesten. Hvis du ønsker mer informasjon, se [Finn endepunkt for tjeneste](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Godkjenning

Platformsikkerhetstokenet brukes til å kalle inn den offentlige API-en for lagersynlighet. Derfor må du generere et _Azure Active Directory-token (Azure AD)_ ved hjelp av Azure AD-appen. Du må deretter bruke Azure AD-tokenet til å få _tilgangstokenet_ fra sikkerhetstjenesten.

Hvis du vil hente et token for sikkerhetstjeneste, gjør du følgende:

1. Logg på Azure-portalen, og bruk den til å finne `clientId`- og `clientSecret`-verdiene for Dynamics 365 Supply Chain Management-appen.
1. Hent et Azure AD-token (`aadToken`) ved å sende en HTTP-forespørsel som har følgende egenskaper:

   - **URL-adresse:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
   - **Metode:** `GET`
   - **Meldingstekst (skjemadata):**

     | Nøkkel           | Verdi                                |
     | ------------- | ------------------------------------ |
     | client_id     | ${aadAppId}                          |
     | client_secret | ${aadAppSecret}                      |
     | grant_type    | client_credentials                   |
     | resource      | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |

   Du skal motta et Azure AD-token (`aadToken`) som svar. Den skal ligne følgende eksempel.

   ```json
   {
       "token_type": "Bearer",
       "expires_in": "3599",
       "ext_expires_in": "3599",
       "expires_on": "1610466645",
       "not_before": "1610462745",
       "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
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
       "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
       "context_type": "finops-env"
   }
   ```

   Merk følgende punkt:

   - Verdien for `client_assertion` må være Azure AD-tokenet (`aadToken`) som du mottok i forrige trinn.
   - Verdien for `context` må være LCS-miljø-ID-en der du vil implementere tillegget.
   - Angi de andre verdiene som vist i eksemplet.

1. Send en HTTP-forespørsel som har følgende egenskaper:

   - **URL-adresse:** `https://securityservice.operations365.dynamics.com/token`
   - **Metode:** `POST`
   - **HTTP-hode:** Inkluder API-versjonen. (Nøkkelen er `Api-Version`, og verdien er `1.0`.)
   - **Meldingstekst:** Ta med JSON-forespørselen du opprettet i forrige trinn.

   Du skal motta et tilgangstoken (`access_token`) som svar. Du må bruke dette tokenet som bærertoken for å kalle opp lagersynlighets-API-en. Her er et eksempel:

   ```json
   {
       "access_token": "{Returned_Token}",
       "token_type": "bearer",
       "expires_in": 3600
   }
   ```

I senere deler vil du bruke `$access_token` til å representere tokenet som ble hentet i siste trinn.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Opprett lagerendringshendelser

Det finnes to API-er for oppretting av lagerendringshendelser:

- Opprett én oppføring: `/api/environment/{environmentId}/onhand`
- Opprett flere oppføringer: `/api/environment/{environmentId}/onhand/bulk`

Tabellen nedenfor summerer betydningen av hvert felt i JSON-teksten.

| Felt-ID | beskrivelse |
|---|---|
| `id` | En unik ID for den bestemte endringshendelsen. Denne ID-en brukes til å sikre at hvis kommunikasjon med tjenesten mislykkes under posteringen, vil samme hendelse ikke telles to ganger i systemet, hvis den sendes inn på nytt. |
| `organizationId` | Identifikatoren til organisasjonen som er koblet til hendelsen. Denne verdien tilordnes til en ID for organisasjon eller dataområde i Supply Chain Management. |
| `productId` | Identifikatoren for produktet. |
| `quantities` | Antallet som antall på lager må endres etter. Hvis for eksempel 10 nye bøker legges til på en hylle, vil denne verdien være `quantities:{ shelf:{ received: 10 }}`. Hvis tre bøker fjernes fra hyllen eller selges, vil denne verdien være `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Datakilden for dimensjonene som brukes i posteringsendringshendelsen og -spørringen. Hvis du angir datakilden, kan du bruke de egendefinerte dimensjonene fra den angitte datakilden. Lagersynlighet kan bruke dimensjonskonfigurasjonen til å tilordne de egendefinerte dimensjonene til de generelle standarddimensjonene. Hvis ingen `dimensionDataSource`-verdi er angitt, kan du bare bruke de generelle [basisdimensjonene](inventory-visibility-configuration.md#data-source-configuration-dimension) i spørringene. |
| `dimensions` | Et dynamisk nøkkel/verdi-par. Verdiene er tilordnet til noen av dimensjonene i Supply Chain Management. Du kan imidlertid også legge til egendefinerte dimensjoner (for eksempel _Kilde_) for å angi om hendelsen kommer fra Supply Chain Management eller et eksternt system. |

> [!NOTE]
> Parameterne `SiteId` og `LocationId` konstruerer [partisjonskonfigurasjonen](inventory-visibility-configuration.md#partition-configuration). Derfor må du angi dem i dimensjoner når du oppretter lagerendringshendelser, angir eller overstyrer lagerbeholdninger eller oppretter reservasjonshendelser.

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

Følgende eksempel viser eksempeltekstinnholdet. I dette eksemplet posterer du en endringshendelse for produktet *T-skjorte*. Denne hendelsen kommer fra POS-systemet (salgssted), og kunden har returnert en rød T-skjorte tilbake til butikken. Denne hendelsen vil øke antallet for produktet *T-skjorte* med 1.

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "PosMachineId": "0001",
        "ColorId": "Red"
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
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Opprett flere endringshendelser

Denne API-en kan opprette flere poster samtidig. De eneste forskjellene mellom denne API-en og [API-en for én hendelse](#create-one-onhand-change-event) er verdiene for `Path` og `Body`. For denne API-en inneholder `Body` en matrise med poster.

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
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "usmf",
        "productId": "Pants",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Angi/overstyre lagerbeholdninger

API-en _Angi lagerbeholdning_ overstyrer de gjeldende dataene for det angitte produktet.

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

Følgende eksempel viser eksempeltekstinnholdet. Virkemåten til denne API-en er forskjellig fra virkemåten til API-ene som er beskrevet i delen [Opprett lagerendringshendelser](#create-onhand-change-event) tidligere i dette emnet. I dette eksemplet blir antallet for produktet *T-skjorte* angitt til 1.

```json
[
    {
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
             "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId": "0001"
        },
        "quantities": {
            "pos": {
                "inbound": 1
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Opprett reservasjonshendelser

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Hvis du vil bruke API-en *Reserver*, må du åpne reservasjonsfunksjonen og fullføre reservasjonskonfigurasjonen. Hvis du vil ha mer informasjon, kan du se [Reservasjonskonfigurasjon (valgfritt)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Opprett én reservasjonshendelse

En reservering kan gjøres mot ulike datakildeinnstillinger. Hvis du vil konfigurere denne reserveringstypen, må du først angi datakilden i `dimensionDataSource` parameteren. I parameteren `dimensions` kan du deretter angi dimensjoner i henhold til dimensjonsinnstillingene i måldatakilden.

Når du kaller reservasjons-API, kan du styre reservasjonsvalideringen ved å angi den boolske `ifCheckAvailForReserv` parameteren i forespørselsteksten. Verdien `True` betyr at valideringen kreves, mens en verdi å `False` betyr at valideringen ikke er nødvendig. Standardverdien er `True`.

Hvis du vil avbryte en reservering eller ikke reservere angitte lagerantall, angir du antallet til en negativ verdi og angir parameteren `ifCheckAvailForReserv` til `False` for å hoppe over valideringen.

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
    "organizationId": "usmf",
    "productId": "T-shirt",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softreservordered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    }
}
```

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Opprett flere reservasjonshendelser

Denne API-en er en masseversjon av [API-en for enkelthendelser](#create-one-reservation-event).

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

## <a name="query-on-hand"></a>Spør om beholdning

API-en _Spør om beholdning_ brukes til å hente gjeldende lagerbeholdningsdata for produktene dine.

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

- `organizationId` bør bare inneholder én verdi, men den er fremdeles en matrise.
- `productId` kan inneholde én eller flere verdier. Hvis den er en tom matrise, vil alle produkter bli returnert.
- `siteId` og `locationId` brukes i lagersynlighet for partisjonering.

Parameteren `groupByValues` bør følge konfigurasjonen din for indeksering. Hvis du vil ha mer informasjon, kan du se [Konfigurasjon av produktindekshierarki](./inventory-visibility-configuration.md#index-configuration).

Parameteren `returnNegative` styrer om resultatene inneholder negative oppføringer.

Følgende eksempel viser eksempeltekstinnholdet.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "LocationId": ["11"],
        "ColorId": ["Red"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

Eksemplene nedenfor viser hvordan du spør på alle produkter på et bestemt område og sted.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "LocationId": ["11"],
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Spør ved å bruke hentemetoden

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
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

Her er et eksempel på henting av en URL-adresse. Denne hentforespørselen er nøyaktig den samme som posteringseksemplet som ble angitt tidligere.

```txt
/api/environment/{environmentId}/onhand/indexquery?organizationId=usmf&productId=T-shirt&SiteId=1&LocationId=11&ColorId=Red&groupBy=ColorId,SizeId&returnNegative=true
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
