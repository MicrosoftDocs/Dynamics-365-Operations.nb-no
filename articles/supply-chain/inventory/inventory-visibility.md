---
title: Tillegg for lagersynlighet
description: Dette emnet beskriver hvordan du installerer og konfigurerer tillegget for lagersynlighet for Dynamics 365 Supply Chain Management.
author: chuzheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 2976153a6a7e4b4130e8f7673ed128945aeabf65
ms.sourcegitcommit: 03c2e1717b31e4c17ee7bb9004d2ba8cf379a036
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/24/2020
ms.locfileid: "4625071"
---
# <a name="inventory-visibility-add-in"></a>Tillegg for lagersynlighet

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tillegget for lagersynlighet er en uavhengig og høyt skalerbar mikrotjeneste som aktiverer beholdningssporing i sanntid, og gir dermed en global visning av lagersynlighet.

All informasjon som er relatert til lagerbeholdningen, eksporteres til tjenesten via i SQL-integrasjon med minimal forsinkelse. Eksterne systemer får tilgang til tjenesten via RESTful-API-er for spørring om lagerbeholdningsinformasjon for gitte sett med dimensjoner, og dermed hente en liste over tilgjengelige lagerbeholdninger.

Lagersynlighet er en mikrotjeneste som er bygd på Common Data Service, som betyr at du kan utvide den ved å bygge Power Apps og bruke Power BI til å oppgi egendefinert funksjonalitet som dekker dine forretningsbehov. Det er også mulig å oppgradere indeksen for å utføre lagerspørringer.

Lagersynlighet inneholder konfigurasjonsalternativer som gjør at den kan integreres med flere tredjepartssystemer. Den støtter den standardiserte lagerdimensjonen, egendefinert utvidelse og standardisert beregnet antall som kan konfigureres.

Dette emnet beskriver hvordan du installerer og konfigurerer tillegget for lagersynlighet for Dynamics 365 Supply Chain Management, og hvordan du bruker app-programmeringsgrensesnittet (API).

## <a name="install-the-inventory-visibility-add-in"></a>Installer tillegget for lagersynlighet

Du må installere tillegget for lagersynlighet ved hjelp av Microsoft Dynamics Lifecycle Services (LCS). LCS er en samarbeidsportal som gir et miljø og et sett med jevnlig oppdaterte tjenester som hjelper deg med å administrere applivssyklusen til Dynamics 365 Finance and Operations-appene dine.

Hvis du vil ha mer informasjon, se [Lifecycle Services-ressurser](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).

### <a name="prerequisites"></a>Forutsetninger

Før du kan installere tillegget for lagersynlighet, må du gjøre følgende:

- Hent et LCS-implementeringsprosjekt med minst ett miljø som er distribuert.
- Generer betanøklene for tilbudet i LCS.
- Aktiver betanøklene for tilbudet for brukeren din i LCS.
- Kontakt produktteamet for Microsoft-lagersynlighet, og oppgi en miljø-ID der du vil distribuere tillegget for lagersynlighet.

Hvis du har spørsmål om disse forutsetningene, kan du ta kontakt med produktteamet for lagersynlighet.

### <a name="install-the-add-in"></a><a name="install-add-in"></a>Installer tillegget

Hvis du vil installere tillegget for lagersynlighet, må du gjøre følgende:

1. Logg på [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index)-portalen.
1. På hjemmesiden velger du prosjektet der miljøet er distribuert.
1. På prosjektsiden velger du miljøet du vil installere tillegget i.
1. Rull ned til du ser delen **Miljøtillegg** på miljøsiden. Hvis delen ikke er synlig, må du kontrollere at de nødvendige betanøklene er fullstendig behandlet.
1. I delen **Miljøtillegg** velger du **Installer et nytt tillegg**.
    ![Miljøsiden i LCS](media/inventory-visibility-environment.png "Miljøsiden i LCS")
1. Velg koblingen **Installer et nytt tillegg**. En liste over tilgjengelige tillegg åpnes.
1. Velg **Lagertjeneste** fra listen. (Merk at det nå er oppført som **Tillegg for lagersynlighets for Dynamics 365 Supply Chain Management**.)
1. Angi verdier for følgende felter i miljøet:

    - **App-ID for AAD**
    - **Leier-ID for AAD**

    ![Legg til i konfigurasjon-side](media/inventory-visibility-setup.png "Legg til i konfigurasjon-side")

1. Godta vilkåret og betingelsen ved å merke av for **Vilkår og betingelser**.
1. Velg **Installer**. Statusen for tillegget vil vises som **Installerer**. Når du er ferdig, oppdaterer du siden for å se status endre til **Installert**.

### <a name="get-a-security-service-token"></a>Hent et token for sikkerhetstjeneste

Hvis du vil hente et token for sikkerhetstjeneste, gjør du følgende:

1. Få tak i `aadToken` og kall opp endepunktet: https://securityservice.operations365.dynamics.com/token.
1. Erstatt `client_assertion` i brødteksten med `aadToken`.
1. Erstatt konteksten i brødteksten med miljøet der du vil distribuere tillegget.
1. Erstatt omfanget i brødteksten med følgende:

    - Område for MCK – https://inventoryservice.operations365.dynamics.cn/.default  
    (Du finner Azure Active Directory-app-ID-en og leie-ID-en for MCK i `appsettings.mck.json`.)
    - Område for PROD – https://inventoryservice.operations365.dynamics.com/.default  
    (Du finner Azure Active Directory-app-ID-en og leie-ID-en for PROD i `appsettings.prod.json`.)

    Resultatet skal ligne følgende eksempel.

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{**Your_AADToken**}",
        "scope":"**https://inventoryservice.operations365.dynamics.com/.default**",
        "context": "**5dbf6cc8-255e-4de2-8a25-2101cd5649b4**",
        "context_type": "finops-env"
    }
    ```

1. Du får et `access_token` som svar. Dette er det du trenger som bærertoken for å kalle opp lagersynlighets-API-en. Her er et eksempel:

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a>Avinstallere tillegget

Velg **Avinstaller** tillegget for å avinstallere tillegget. Oppdater LCS så fjernes tillegget for lagersynlighet. Avinstallasjonsprosessen vil fjerne registreringen av tillegget, og også starte en jobb for å rydde opp i alle forretningsdataene som er lagret i tjenesten.

## <a name="inventory-visibility-add-in-public-api"></a>Offentlig API for tillegget for lagersynlighet

Den offentlige REST-API-en i tillegget for lagersynlighet viser flere spesifikke endepunkter for integrering. Det støtter tre hovedtyper for samhandling:

- Postering av beholdningsendringer i tillegget fra et eksternt system.
- Spørring etter gjeldende antall i beholdningen fra et eksternt system.
- Automatisk synkronisering med Supply Chain Management tilgjengelig.

Den automatiske synkroniseringen er ikke en del av den offentlige API-en, men blir i stedet behandlet i bakgrunnen for miljøer som har aktivert tillegget for lagersynlighet.

### <a name="authentication"></a>Godkjenning

Platformsikkerhetstoken brukes til å kalle opp tillegget for lagersynlighet, så du må generere et Azure Active Directory-token ved hjelp av Azure Active Directory-programmet.

Hvis du vil ha mer informasjon om hvordan du får tak i sikkerhetstokenet, kan du se [Installer tillegget for lagersynlighet](#install-add-in).

### <a name="configure-the-inventory-visibility-api"></a>Konfigurer API-en for lagersynlighet

Før du bruker tjenesten, må du fullføre konfigurasjonene som er beskrevet i følgende underavsnitt. Konfigurasjonen kan variere avhengig av detaljene i miljøet ditt. Den inneholder hovedsakelig fire deler:

- [Partisjonering](#partitioning)
- [Dimensjonskonfigurasjoner](#dimension-configurations)
- [Indeksering](#indexing)
- [Egendefinert mål](#custom-measurement)

#### <a name="partitioning"></a>Partisjonering

Partisjonering kan påvirke ytelsen betydelig for API-en for lagersynlighet. Det er en god idé å definere et oppsett som tillater små grupperinger av data, samtidig som du tillater meningsfulle dataspørringer samtidig.

`organizationId` (`dataAreaId` i Supply Chain Management) vil alltid være en del av partisjonen, og standard lagersynlighet er satt til partisjonering per dimensjon som *Område + sted*. Dette betyr at tjenesten alltid må spørres med disse dimensjonene som er definert i filtrene.

> [!NOTE]
> *Område* og *Sted* er to generelle standarddimensjoner i lagersynlighet. I Supply Chain Management kalles disse dimensjonene *Område* (`InventSiteId`) og *Lager* (`InventLocationId`)

### <a name="dimension-configurations"></a>Dimensjonskonfigurasjoner

Lagersynlighet inneholder en liste over generelle standarddimensjoner for å aktivere systemintegrasjon med flere kilder.

Tabellen nedenfor viser hvilke lagerdimensjoner som skal være standard dimensjonsnavn i lagersynlighet.

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

> [!NOTE]
> Dimensjonstypen som er oppført i den forrige tabellen, er bare for referanse. Du trenger ikke definere dimensjonstypen i Lagersynlighet.

Hvis det finnes en egendefinert dimensjon som må flyte til en standardverdi når det brukes av lagersynlighet, kan du konfigurere navnet **Egendefinert dimensjon** i Lagersynlighet.

Eksterne systemer har tilgang til lagersynlighet via RESTful-API-er som gir deg beholdningsinformasjon om gitte dimensjoner som det skal spørres om. Ved integreringen kan du bruke Lagersynlighet til å konfigurere den *eksterne kanaldatakilden* og kildedimensjonen til *måldimensjonene* i Lagersynlighet.

Måldimensjonene må være ett av følgende:

- Standarddimensjoner i Lagersynlighet
- Egendefinerte dimensjoner

Formålet med dimensjonskonfigurasjon er å standardisere integreringen med flere systemer for spørringen på dimensjoner og posteringshendelsen med dimensjoner.

#### <a name="indexing"></a>Indeksering

Vanligvis vil ikke lagerbeholdningsspørringen bare være på det høyeste totale nivået, men du vil kanskje se resultater som er aggregert basert på lagerdimensjonene.

Lagersynlighet gir fleksibilitet ved å la deg definere indeksene som er basert på dimensjonen eller kombinasjonen av dimensjonene.

> [!NOTE]
> For øyeblikket kan du bare konfigurere indekser til maksimalt fem. Du må nøye vurdere hvilken dimensjon eller dimensjonskombinasjon du vil bruke før implementeringen for å sikre at den oppfyller dine forretningsbehov. Hvis du for eksempel vil spørre etter produkter som følger:

- Forespør den aggregerte produktbeholdningen etter dimensjonene *Farge* og *Størrelse*.
- I noen tilfeller vil du bare spørre om produktet totalt.

Du har to indekser definert som følgende:

- `["ColorId", "SizeId"]`
- `[]`

Den tomme parentesen samles, basert på produkt-ID-en i partisjonen.

Indekseringen definerer hvordan du kan gruppere resultatene basert på `groupBy`-spørringsinnstillingen. I dette tilfellet hvis du ikke definerer noen `groupBy`-verdier, får du totaler etter `productid`. Hvis ikke hvis du definerer `groupBy` som `groupBy=ColorId&groupBy=SizeId` vil du få flere linjer returnert, basert på de ulike kombinasjonene mellom farger og størrelser i systemet.

Du kan legge spørringskriteriene i brødteksten for forespørselen.

Her er en eksempelspørring på produktet med farge- og størrelseskombinasjon.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a>Egendefinert mål

Standard målantall er koblet til Supply Chain Management, men du vil kanskje ha et antall som består av en kombinasjon av standardmålene. Hvis du vil gjøre dette, kan du ha en konfigurasjon av egendefinert antall, som vil bli lagt til i utdataene i lagerbeholdningsspørringene.

Ved hjelp av funksjonaliteten kan du bare definere et sett med mål som skal legges til, eller et sett med mål som skal trekkes fra, for å kunne lage det egendefinerte målet.

Med følgende spørringsvilkår vil du for eksempel konfigurere det egendefinerte målantallet som `MyCustomAvailableforReservation` som skal brukes av forbrukssystemet.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| Forbrukssystem | Beregnede mål | Datakilde | Modifikator | Beregningstype for modifikator |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | Tillegg |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | Tillegg |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | Subtraksjon |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | Tillegg |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | Subtraksjon |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | Tillegg |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | Tillegg |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | Subtraksjon |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | Subtraksjon |

Med dette vil spørringen på det egendefinerte målantallet returnere følgende utdata.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
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

`MyCustomAvailableforReservation`-utdataene er basert på beregningsinnstillingen i de egendefinerte målene som:  
 *100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*

### <a name="posting-on-hand-changes"></a>Postere lagerendringer

Den nøyaktige URL-adressen som hendelsen vil bli postert til, avhenger av det geografiske området. Den tar følgende form:

`https://{serviceURL}/api/environment/{environmentId}/onhand`

Når den er godkjent, kan denne URL-adressen brukes sammen med HTTP `POST`-metoden til å sende lagerbeholdningshendelser til tjenesten.

En spesiell topptekst brukes til å kommunisere med Dynamics 365-tjenester via HTTP-forespørsler, og angir miljø-ID-en til Supply Chain Management-forkomten dataene er koblet til. For eksempel:

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a>Postere spørringer om lagerendringer eksempel 1

I dette eksemplet vises det et scenario der du kan definere dimensjonskonfigurasjonen i Power Apps.

Bruk følgende spørring til å konfigurere dimensjonstilordningen i Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Nå kan du angi `dimensionDataSource` og bruke egendefinerte dimensjoner i spørringene. Systemet konverterer automatisk egendefinerte dimensjoner til basisdimensjoner.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a>Postere spørringer om lagerendringer eksempel 2

Dette eksemplet viser et scenario der ingen tilordninger er definert for dimensjonskonfigurasjonen i Power Apps, slik at posteringen også bør bruke basisdimensjonene. Alle dimensjoner må være basisdimensjoner når `dimensionDataSource`-feltet er null, tomt eller mellomrom.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a>Feltegenskaper for JSON-dokument

Feltene fra JSON-spørringseksemplene som ble angitt tidligere, har egenskapene som er oppført i tabellen nedenfor.

| Felt-ID | beskrivelse |
|---|---|
| `id` | En unik ID for den bestemte endringshendelsen. Denne ID-en brukes til å sikre at hvis kommunikasjon med tjenesten mislykkes under posteringen, vil sendingen av hendelsen ikke resultere i at samme hendelse telles to ganger i systemet. |
| `organizationId` | Identifikatoren til organisasjonen som er koblet til hendelsen. Dette tilordner til ID-er til Supply Chain Management-organisasjoner eller dataområder. |
| `productId` | Identifikatoren til produktet det gjelder. |
| `quantity` | Antallet som lagerbeholdningen må endres med. Hvis for eksempel ti nye bagels er lagt til i en hylle, vil denne verdien være 10. Hvis tre bagels deretter ble fjernet fra hyllen eller solgt, ville denne verdien være –3. |
| `dimensionDataSource` | Datakilden for dimensjonene som brukes i posteringsendringshendelsen og -spørringen. Hvis du angir datakilden, kan du bruke de egendefinerte dimensjonene fra den angitte datakilden. Med dimensjonskonfigurasjonen kan Lagersynlighet tilordne de egendefinerte dimensjonene til de generelle standarddimensjonene. Hvis `dimensionDataSource` ikke er angitt, kan du bare bruke de generelle standarddimensjonene i spørringene.   |
| `dimensions` | En dynamisk samling med nøkkel/verdi-par. Disse vil tilordnes noen av dimensjonene i Supply Chain Management, men du kan også legge til egendefinerte dimensjoner (som *Kilde*) som kan angi om hendelsen kommer fra Supply Chain Management eller et eksternt system. |

### <a name="querying-current-on-hand"></a>Spørring om aktuell lagerbeholdning

Endepunktet for spørringer av gjeldende lagerbeholdning vil ha en lignende URL-adresse:

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

Det blir spurt med HTTP `POST`-metoden.

#### <a name="current-on-hand-query-example-1"></a>Gjeldende beholdningsspørring, eksempel 1

I dette eksemplet vises det et scenario der du allerede har fullført dimensjonskonfigurasjonen i Power Apps.

Bruk følgende spørring til å konfigurere dimensjonstilordningen i Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Nå kan du angi `dimensionDataSource` og bruke egendefinerte dimensjoner i spørringene. Systemet konverterer automatisk egendefinerte dimensjoner til basisdimensjoner. Du kan angi `DimensionDataSource` i `filters` og angi egendefinerte dimensjoner i både `filters` og `groupByValues`. Systemet konverterer automatisk egendefinerte dimensjoner til basisdimensjoner.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a>Gjeldende beholdningsspørring, eksempel 2

Dette eksemplet viser et scenario der ingen tilordninger er definert for dimensjonskonfigurasjonen i Power Apps, slik at posteringen også bør bruke basisdimensjonene. Alle dimensjoner må være basisdimensjoner når `dimensionDataSource`-feltet, under `filters`, er null, tomt eller mellomrom.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a>Eksempel på returresultat

Spørringene som vises i eksemplene ovenfor, kan returnere et resultat som dette.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
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

Legg merke til at antall-feltene er strukturert som en ordliste for mål og tilknyttede verdier.
