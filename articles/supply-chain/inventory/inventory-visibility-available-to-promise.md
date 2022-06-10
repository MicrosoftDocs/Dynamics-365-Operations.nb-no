---
title: Tidsplaner for lagerendringer i Lagersynlighet og leveringskapasitet
description: Dette emnet beskriver hvordan du planlegger fremtidige endringer i lagerbeholdning og beregner ATP-antall (tilgjengelig for ordre).
author: yufeihuang
ms.date: 05/11/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-04
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 7456f87bede7bd0073223fa4762f96f919799e06
ms.sourcegitcommit: 38d97efafb66de298c3f504b83a5c9b822f5a62a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/17/2022
ms.locfileid: "8763260"
---
# <a name="inventory-visibility-on-hand-change-schedules-and-available-to-promise"></a>Tidsplaner for lagerendringer i Lagersynlighet og leveringskapasitet

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer funksjonen *Tidsplan for lagerendring* for å planlegge fremtidige endringer i lagerbeholdning og beregne ATP-antall (tilgjengelig for ordre). ATP er antallet av en vare som er tilgjengelig og kan loves til en kunde i løpet av den neste perioden. Bruk av denne beregningen kan øke kapasiteten for innfrielse av bestillinger betydelig.

For mange produsenter, forhandlere eller selgere er det ikke nok bare å vite hva som er i varebeholdningen for øyeblikket. De må ha full oversikt over fremtidig tilgjengelighet. Denne fremtidige tilgjengeligheten bør vurdere fremtidig forsyning, fremtidig etterspørsel og ATP.

## <a name="enable-and-set-up-the-features"></a><a name="setup"></a>Aktiver og konfigurer funksjonene

Før du kan bruke ATP, må du definere ett eller flere beregnede mål for å beregne ATP-antallene. Du må også aktivere funksjonen og konfigurere ATP-innstillinger i Microsoft Power Apps.

### <a name="set-up-calculated-measures-for-atp-quantities"></a>Definer beregnede mål for ATP-antall

*Beregnet ATP-mål* er et forhåndsdefinert beregnet mål som vanligvis brukes til å finne lagerbeholdningen som for øyeblikket er tilgjengelig. *Forsyningsantallet* er summen av antall for de fysiske målene som har modifikatortypen *tillegg*, og *behovsmengde* er summen av antall for de fysiske målene som har typen *subtraksjon*.

Du kan legge til flere beregnede mål for å beregne flere ATP-antall. Det totale antallet distinkte fysiske mål i alle beregnede ATP-mål må imidlertid være mindre enn ni.

> [!IMPORTANT]
> Et beregnet mål er en sammensetning av fysiske mål. Formelen kan bare inneholde fysiske mål uten duplikater, ikke beregnede mål.

Du kan for eksempel sette opp følgende beregnede mål:

**On-hand-available** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) – (*ReservPhysical* + *SoftReservePhysical* + *Outbound*)

Summen av (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) representerer forsyning, og summen av (*ReservPhysical* + *SoftReservePhysical* + *Outbound*) representerer behov. Derfor kan det beregnede målet forstås på følgende måte:

**On-hand-available** = *Supply* – *Demand*

Du kan legge til et annet beregnet mål for å beregne det **disponible fysiske** ATP-antallet.

**On-hand-physical** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) – (*Outbound*)

Det finnes åtte atskilte, fysiske mål fordelt på de to ATP-beregnede målene: *PhysicalInvent*, *OnHand*, *Unrestricted*, *QualityInspection*, *Inbound*, *ReservPhysical*, *SoftReservePhysical* og *Outbound*.

Hvis du vil ha mer informasjon om beregnede mål, kan du se [Beregnede mål](inventory-visibility-configuration.md#calculated-measures).

### <a name="turn-on-the-on-hand-change-schedule-feature-and-configure-atp-settings"></a>Slå på funksjonen Tidsplan for lagerendring og konfigurer ATP-innstillinger

Følg denne fremgangsmåten for å aktivere funksjonen *Tidsplan for lagerendring* i Power Apps og konfigurere ATP-innstillingene.

1. Logg deg på Power Apps, og åpne Lagersynlighet.
1. Åpne **Konfigurasjon**-siden.
1. På fanen **Funksjonsbehandling** aktiverer du funksjonen *OnhandChangeSchedule*.
1. Velg fanen **ATP-innstillinger**.
1. Når spør Lagersynlighet, vil du få et resultat som inkluderer hvert beregnede ATP-mål som du legger til her. Velg **Legg til** for å legge til et nytt beregnet mål for ATP.
1. Angi følgende felter:

    - **Datakilde** – Velg datakilden som er knyttet til det beregnede målet.
    - **Beregnet mål** – Velg det beregnede målet som er tilknyttet den valgte datakilden, og som du vil bruke til å finne tilgjengelig beholdningsantall.
    - **Tidsplanperiode** – Angi antallet dager brukerne kan vise og sende inn planlagte endringer i lagerbeholdningen når det valgte beregnede målet brukes. Brukere som spør etter lagerinformasjon, vil få lagerbeholdningen, planlagte lagerbeholdningsendringer og ATP for hver dag i denne perioden, og begynner med gjeldende dato. Velg et heltall mellom 1 og 7.

    > [!IMPORTANT]
    > Tidsplanperioden inkluderer den gjeldende datoen. Derfor kan brukere planlegge at lagerbeholdningsendringer skal skje når som helst fra gjeldende dato (dagen når endringen sendes) til og med (tilsplanperioden – 1) dager i fremtiden.

1. Velg **Lagre**.
1. Gjenta trinn 5 til 7 til du har lagt til alle de beregnede målene du trenger for ATP.
1. Når du er ferdig med å konfigurere alle de nødvendige innstillingene, velger du **Oppdater konfigurasjon**.

Hvis du vil ha mer informasjon, kan du se [Fullfør og oppdater konfigurasjonen](inventory-visibility-configuration.md).

## <a name="how-the-on-hand-change-schedule-and-atp-calculations-work"></a>Slik fungerer tidsplanen for lagerbeholdningsendring og ATP-beregninger fungerer

En *endringsplan for lagerbeholdning* fastsetter forventede datoer og antall for planlagte endringer i lagerbeholdning. Du kan sende inn en endringsplan for lagerbeholdning til Lagersynlighet, forutsatt at datoene er innenfor perioden som er definert av innstillingen **Tidsplanperiode** (se delen [Aktiver og konfigurer funksjonene](#setup)). Brukere som spør etter lagerinformasjon, vil få lagerbeholdningen, planlagte lagerbeholdningsendringer og ATP for hver dag i denne perioden.

Planlagte endringer er i utgangspunktet ikke iverksatt, og påvirker derfor ikke den faktiske lagerbeholdningen i systemet. Hvis du vil iverksette endringene, må du sende inn *en lagerendringshendelse*, som oppdaterer det faktiske antallet som er tilgjengelig på lager. Du må deretter tilbakeføre den planlagte endringen ved å sende inn en endringsplan for lagerbeholdning for et tilsvarende negativt antall.

Du legger for eksempel inn en ordre på 10 sykler og forventer at den kommer i morgen. Derfor sender du inn en tidsplan for lagerbeholdningsendring som har et innkommende antall på 10 og er datert for i morgen. Når ordren ankommer neste dag, legger du til syklene i den fysiske lagerbeholdningen. Deretter må du iverksette endringen i systemet for å oppdatere den faktiske lagerbeholdningen. For å iverksette endringen sender du inn en beholdningendringshendelse som har et innkommende antall på 10. Deretter tilbakefører du den planlagte endringen ved å sende inn en endringsplan som har et innkommende antall på -10.

Når spør Lagersynlighet etter beholdningsantall og ATP-antall, returneres følgende informasjon for hver dag i tidsplanperioden:

- **Dato** – Datoen som resultatet gjelder for. Tidssonen er Coordinated Universal Time (UTC).
- **Antall på lager** – Det faktiske beholdningsantallet for den angitte datoen. Denne beregningen foretas i henhold til det beregnede ATP-målet som er konfigurert for Lagersynlighet.
- **Planlagt forsyning** – Summen av alle planlagte innkommende antall som ikke har blitt fysisk tilgjengelig for umiddelbart forbruk eller forsendelse per den angitte datoen.
- **Planlagt behov** – Summen av alle planlagte utgående antall som ikke er brukt eller sendt per den angitte datoen.
- **ATP-antall** – Det minste prosjekterte beholdningsantallet som er tilgjengelig fra den angitte datoen til slutten av planleggingsperioden. Dette antallet omfatter alle planlagte antallsjusteringer. Det er det maksimale antallet som kan loves på gjeldende dato for levering eller forbruk den dagen.

Hvis for eksempel gjeldende dato er 1. februar 2022 og planleggingsperioden er 7, kan brukere sende inn planlagte lagerbeholdninger som forventes å skje fra 1. februar til og med 7. februar 2022. I dette tilfellet beregnes ATP-antallet for 3. februar basert på lagerbeholdning for den dagen, og det planlagte antallet fra 3. februar til og med 7. februar.

## <a name="example"></a>Eksempel

Følgende eksempel viser hvordan en serie med endringer i planlagt antall påvirker lagerbeholdningen og ATP-antallet som lagersynsrapportene rapporterer. Det viser også hvordan du legger inn en planlagt endring, hvordan en igangsatt planendring påvirker resultatene og hva som kan skje hvis du ikke gjør noen planlagt endring.

Resultatene i dette eksemplet viser en *prosjektert lagerbeholdning*. Denne verdien inneholder alle planlagte oppdateringer til illustrasjonsformål, men vil faktisk ikke rapporteres når du spør etter lagersynlighet.

1. Følgende innstillinger er konfigurert for systemet på siden **ATP-innstilling** i Power Apps:

    - **Beregnet ATP-mål** – Du har et beregnet mål som kalles *Lagerbeholdning*. Det beregnes som *Lagerbeholdning = Forsyning – Behov*. Du velger dette målet her.
    - **Planleggingsperiode** – Du velger *7*.

1. Følgende betingelser gjelder også:

    - Gjeldende dato er 1. februar 2022.
    - Nåværende antall på lager er 20.

1. For gjeldende dato (1. februar 2022) sender du inn et planlagt behovsantall på 3 til Lagersynlighet. Derfor er det prosjekterte beholdningsantallet 17. Tabellen nedenfor viser resultatet.

    | Dato | Beholdning | Planlagt forsyning | Planlagt behov | Prosjektert lagerbeholdning | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 1. februar 2022 | 20 | | 3 | 17 | 17 |
    | 2. februar 2022 | 20 | | | 17 | 17 |
    | 3. februar 2022 | 20 | | | 17 | 17 |
    | 4. februar 2022 | 20 | | | 17 | 17 |
    | 5. februar 2022 | 20 | | | 17 | 17 |
    | 6. februar 2022 | 20 | | | 17 | 17 |
    | 7. februar 2022 | 20 | | | 17 | 17 |

1. På gjeldende dato (1. februar 2022) sender du inn et planlagt forsyningsantall på 10 for 3. februar 2022. Tabellen nedenfor viser resultatet.

    | Dato | Beholdning | Planlagt forsyning | Planlagt behov | Prosjektert lagerbeholdning | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 1. februar 2022 | 20 | | 3 | 17 | 17 |
    | 2. februar 2022 | 20 | | | 17 | 17 |
    | 3. februar 2022 | 20 | 10 | | 27 | 27 |
    | 4. februar 2022 | 20 | | | 27 | 27 |
    | 5. februar 2022 | 20 | | | 27 | 27 |
    | 6. februar 2022 | 20 | | | 27 | 27 |
    | 7. februar 2022 | 20 | | | 27 | 27 |

1. På gjeldende dato (1. februar 2022) sender du inn følgende endringer i planlagt antall:

    - Behovsantall på 15 for 4. februar 2022
    - Forsyningsantall på 1 for 5. februar 2022
    - Forsyningsantall på 3 for 6. februar 2022

    Tabellen nedenfor viser resultatet.

    | Dato | Beholdning | Planlagt forsyning | Planlagt behov | Prosjektert lagerbeholdning | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 1. februar 2022 | 20 | | 3 | 17 | 12 |
    | 2. februar 2022 | 20 | | | 17 | 12 |
    | 3. februar 2022 | 20 | 10 | | 27 | 12 |
    | 4. februar 2022 | 20 | | sept. | 12 | 12 |
    | 5. februar 2022 | 20 | 1 | | 13 | 13 |
    | 6. februar 2022 | 20 | 3 | | 16 | 16 |
    | 7. februar 2022 | 20 | | | 16 | 16 |

1. På gjeldende dato (1. februar 2022) sender du det planlagte behovsantallet på 3. Derfor må du foreta denne endringen, slik at den gjenspeiles i det faktiske lagerbeholdningsantallet. For å iverksette endringen sender du inn en beholdningendringshendelse som har et utgående antall på 3. Deretter tilbakefører du den planlagte endringen ved å sende inn en endringsplan som har et utgående antall på -3. Tabellen nedenfor viser resultatet.

    | Dato | Beholdning | Planlagt forsyning | Planlagt behov | Prosjektert lagerbeholdning | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 1. februar 2022 | 17 | | 0 | 17 | 12 |
    | 2. februar 2022 | 17 | | | 17 | 12 |
    | 3. februar 2022 | 17 | 10 | | 27 | 12 |
    | 4. februar 2022 | 17 | | sept. | 12 | 12 |
    | 5. februar 2022 | 17 | 1 | | 13 | 13 |
    | 6. februar 2022 | 17 | 3 | | 16 | 16 |
    | 7. februar 2022 | 17 | | | 16 | 16 |

1. Neste dag (2. februar 2022) forskyves tidsplanperioden fremover med én dag. Tabellen nedenfor viser resultatet.

    | Dato | Beholdning | Planlagt forsyning | Planlagt behov | Prosjektert lagerbeholdning | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2. februar 2022 | 17 | | | 17 | 12 |
    | 3. februar 2022 | 17 | 10 | | 27 | 12 |
    | 4. februar 2022 | 17 | | sept. | 12 | 12 |
    | 5. februar 2022 | 17 | 1 | | 13 | 13 |
    | 6. februar 2022 | 17 | 3 | | 16 | 16 |
    | 7. februar 2022 | 17 | | | 16 | 16 |
    | 8. februar 2022 | 17 | | | 16 | 16 |

1. Men to dager senere (4. februar 2022) er forsyningsantallet på 10 som var planlagt for 3. februar, ennå ikke ankommet. Tabellen nedenfor viser resultatet.

    | Dato | Beholdning | Planlagt forsyning | Planlagt behov | Prosjektert lagerbeholdning | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 4. februar 2022 | 17 | | sept. | 2 | 2 |
    | 5. februar 2022 | 17 | 1 | | 3 | 3 |
    | 6. februar 2022 | 17 | 3 | | 6 | 6 |
    | 7. februar 2022 | 17 | | | 6 | 6 |
    | 8. februar 2022 | 17 | | | 6 | 6 |
    | 9. februar 2022 | 17 | | | 6 | 6 |
    | 10. februar 2022 | 17 | | | 6 | 6 |

    Som du ser, påvirker ikke de planlagte (men ikke igangsatte) endringene i lagerbeholdningen det faktiske beholdningsantallet.

## <a name="submit-change-schedules-change-events-and-atp-queries-through-the-api"></a><a name="api-urls"></a>Send inn endringsplaner, endringshendelser og ATP-spørringer via API

Du kan bruke følgende URL-adresser for API (Application Programming Interface) til å sende inn tidsplaner for lagerbeholdning, endringshendelser og spørringer.

| Bane | Metode | Beskrivelse |
| --- | --- | --- |
| `/api/environment/{environmentId}/onhand/changeschedule` | `POST` | Opprett én planlagt lagerendring. |
| `/api/environment/{environmentId}/onhand/changeschedule/bulk` | `POST` | Opprett flere planlagte lagerendringer. |
| `/api/environment/{environmentId}/onhand` | `POST` | Opprett én lagerendringshendelse. |
| `/api/environment/{environmentId}/onhand/bulk` | `POST` | Opprett flere endringshendelser. |
| `/api/environment/{environmentId}/onhand/indexquery` | `POST` | Spør ved å bruke `POST`-metoden. |
| `/api/environment/{environmentId}/onhand` | `GET` | Spør ved å bruke `GET`-metoden. |

Hvis du vil ha mer informasjon, kan du se [Offentlige API-er for lagersynlighet](inventory-visibility-api.md).

### <a name="create-one-on-hand-change-schedule"></a>Opprett én endringsplan for lagerbeholdning

En endringsplan for lagerbeholdning utføres ved å sende inn en `POST`-forespørsel til den relevante URL-adressen for lagersynlighet (se delen [Send inn endringsplaner, endringshendelser og ATP-spørringer via API](#api-urls)). Du kan også sende inn masseforespørsler.

En tidsplan for lagerendring kan bare opprettes hvis den planlagte datoer er mellom gjeldende dato og slutten av gjeldende tidsplanperiode. datetime-formatet skal være *år-måned-dag* (for eksempel **2022-02-01**). Tidsformatet må bare være nøyaktig for dagen.

Denne API-en oppretter én enkelt lagerendringsplan.

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule
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
        dimensionDataSource: string, # optional
        dimensions: {
            [key:string]: string,
        },
        quantitiesByDate: {
            [datetime:datetime]: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
    }
```

Følgende eksempel viser eksempeltekstinnholdet uten `dimensionDataSource`.

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    },
    "quantitiesByDate":
    {
        "2022-02-01": // today
        {
            "pos":{
                "inbound": 10
            }
        }
    }
}
```

### <a name="create-multiple-on-hand-change-schedules"></a>Opprette flere planer for lagerendring

Denne API-en kan opprette flere poster samtidig. De eneste forskjellene mellom denne API-en og API-en for én hendelse er verdiene for `Path` og `Body`. For denne API-en inneholder `Body` en matrise med poster. Maksimalt antall oppføringer er 512. Derfor kan bulk-API-en for lagerbeholdningendring støtte opptil 512 planlagte endringer om gangen.

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule/bulk
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
            quantitiesByDate: {
                [datetime:datetime]: {
                    [dataSourceName:string]: {
                        [key:string]: number,
                    },
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
        "id": "id-bike-0001",
        "organizationId": "usmf",
        "productId": "Bike",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-01": // today
            {
                "pos":{
                    "inbound": 10
                }
            }
        }
    },
    {
        "id": "id-car-0002",
        "organizationId": "usmf",
        "productId": "Car",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-05":
            {
                "pos":{
                    "outbound": 10
                }
            }
        }
    }
]
```

### <a name="create-on-hand-change-events"></a>Opprett lagerendringshendelser

Tidsplaner for lagerendringshendelser utføres ved å sende inn en `POST`-forespørsel til den relevante URL-adressen for Lagersynlighet-tjenesten (se delen [Send inn endringsplaner, endringshendelser og ATP-spørringer via API](#api-urls)). Du kan også sende inn masseforespørsler.

> [!NOTE]
> Lagerendringshendelser er ikke unike for ATP-funksjonaliteten, men er en del av standard API for Lagersynlighet. Dette eksemplet er inkludert fordi hendelser er relevante når du arbeider med ATP. Lagerendringshendelser ligner endringer i lagerbeholdningsreservasjoner, men hendelsesmeldinger må sendes til en annen API-URL, og hendelser bruker `quantities` i stedet for `quantityByDate` i meldingsteksten. Hvis du vil ha mer informasjon om lagerendringshendelser og andre funksjoner i API-en for Lagersynlighet, kan du se [Offentlige API-er for Lagersynlighet](inventory-visibility-api.md#create-one-onhand-change-event).

Følgende eksempel viser en forespørselstekst som inneholder én enkelt lagringsendringshendelse.

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "SizeId": "Big",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 10.0
        }
    }
}
```

## <a name="query-the-scheduled-on-hand-changes-and-atp-results"></a>Spør de planlagte lagerbeholdningsendringene og ATP-resultatene

Du kan spørre planlagte lagerbeholdningsendringer og ATP-resultater ved å sende enten en `POST`-forespørsel eller en `GET`-forespørsel til den riktige URL-adressen for API-en (se delen [Send inn endringsplaner, endringshendelser og ATP-spørringer via API](#api-urls)).

I forespørselen setter du `QueryATP` til *sann* hvis du vil spørre etter planlagte lagerbeholdningsendringer og ATP-resultater.

- Hvis du sender inn forespørselen via `GET`-metoden, angir du denne parameteren i URL-adressen.
- Hvis du sender inn forespørselen via `POST`-metoden, angir du denne parameteren i forespørselsteksten.

> [!NOTE]
> Uansett om parameteren `returnNegative` er satt til *sann* eller *usann* i forespørselsteksten, vil resultatet inneholde negative verdier når du spør om planlagte lagerbeholdninger og ATP-resultater. Disse negative verdiene vil bli inkludert, fordi hvis bare behovsordrer blir planlagt, eller hvis forsyningsantallet er mindre enn behovsantallet, vil de planlagte endringene i lagerbeholdningsantallene være negative. Hvis negative verdier ikke ble tatt med, vil resultatene være forvekslingsvis. Hvis du vil ha mer informasjon om dette alternativet og hvordan det fungerer for andre typer spørringer, kan du se [Offentlige API-er for Lagersynlighet](inventory-visibility-api.md#query-with-post-method).

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

Følgende eksempel viser hvordan du oppretter en forespørselstekst som kan sendes inn til Lagersynlighet ved hjelp av `POST`-metoden.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "siteId": ["1"],
        "LocationId": ["11"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true
}
```

### <a name="get-method-example"></a>Eksempel på GET-metoden

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

Følgende eksempel viser hvordan du oppretter en forespørsels-URL som en `GET`-forespørsel.

```txt
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand?organizationId=usmf&productId=Bike&SiteId=1&LocationId=11&groupBy=ColorId,SizeId&returnNegative=true&QueryATP=true
```

Resultatet til denne `GET`-forespørselen er nøyaktig det samme som resultatet av `POST`-forespørselen i det forrige eksemplet.

### <a name="query-result-example"></a>Eksempel på spørringsresultat

Begge de forrige spørringseksemplene kan gi følgende svar. For dette eksemplet er systemet konfigurert med følgende innstillinger:

- **Beregnet ATP-mål:** *iv.onhand = pos.inbound – pos.outbound*
- **Planleggingsperiode:** *7*

Her er et eksempel på svarteksten.

```json
[
    {
        "quantitiesByDate": {
            "2022-02-02T00:00:00": {
                "pos": {
                    "outbound": 5,
                    "inbound": 0,
                },
                "iv": {
                    "onhand": -5,
                },
            },
            "2022-02-06T00:00:00": {
                "pos": {
                    "inbound": 7,
                    "outbound": 0,
                },
                "iv": {
                    "onhand": 7,
                },
            }
        },
        "atpQuantities": {
            "2022-02-01T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-02T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-03T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-04T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-05T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-06T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            },
            "2022-02-07T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            }
        },
        "productId": "Bike ",
        "dimensions": {
            "ColorId": "Red",
            "SizeId": "Big",
            "siteid": "1",
            "locationid": "11"
        },
        "quantities": {
            "pos": {
                "inbound": 10.0,
                "outbound": 0,
            },
            "iv": {
                "onhand": 10.0,
            }
        }
    }
]
```
