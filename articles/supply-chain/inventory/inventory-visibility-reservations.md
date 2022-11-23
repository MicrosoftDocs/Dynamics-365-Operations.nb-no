---
title: Inventory Visibility-reservasjoner
description: Denne artikkelen beskriver hvordan du definerer reserveringsfunksjonen for å opprette reserveringer, forbruke reserveringer og/eller ikke reservere angitte lagerantall ved hjelp av Lagersynlighet.
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
ms.openlocfilehash: 0ae0589f8bac7ebf9b43cf0f3bc02680d324b29b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762748"
---
# <a name="inventory-visibility-reservations"></a>Inventory Visibility-reservasjoner

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver et vanlig brukstilfelle for ikke-forpliktende reserveringer, og forklarer hvordan du definerer dem i Lagersynlighet. Den inneholder informasjon om hvordan du oppretter ikke-forpliktende reserveringer, motposterer dem ved fysisk forbruk og justerer eller ikke-reserverer angitte lagerantall.

## <a name="sample-use-case-for-soft-reservation"></a>Eksempel på brukstilfelle for ikke-forpliktende reservasjon

Ikke-forpliktende reservering hjelper organisasjoner med å oppnå en enkelt kilde til sannhet om tilgjengelig beholdning, spesielt under ordreoppfyllelsesprosessen. Denne funksjonaliteten er nyttig for organisasjoner der følgende betingelser finnes:

- Organisasjonen har minst to forskjellige systemer som tar utgående ordrer direkte.
- Organisasjonen er svært streng og ønsker å hindre dobbeltbestilling av produktlager, noe som kan skje hvis flere systemer kan overbeholde den siste lagerbeholdningen. Denne situasjonen forhindres når alle ordresystemer kan foreta øyeblikkelige ikke-forpliktende reservasjon-API-kall til lagersynlighet, som gir en faktakilde om lagertilgjengelighet.

[<img src="media/inventory-visibility-soft-reservation.png" alt="Inventory Visibility soft reservation." title="Lagersynlighet, ikke-forpliktende reservasjon" width="720" />](media/inventory-visibility-soft-reservation.png)

Den forrige illustrasjonen viser hvordan ikke-forpliktende reservering fungerer, og fremhever følgende operasjoner:

- Det innledende lagernivået synkroniseres med Lagersynlighet fra Microsoft Dynamics 365 Supply Chain Management.
- Ikke-forpliktende reservasjon posteres fra hver av ordrekanalene eller -systemene til Lagersynlighet. Lagersynligheten validerer lagertilgjengelighet, og forsøker å lage en ikke-forpliktende reservasjon. Hvis ikke-forpliktende reservasjon lykkes, legger Lagersynligheten til det ikke-forpliktende antallet, trekker fra det tilgjengelige for reservasjonsantallet (AFR) og svarer med en ikke-forpliktende reserverings-ID.
- På dette tidspunktet forblir det fysiske lagerantallet det samme.
- Du kan deretter synkronisere enten enkle eller aggregerte, ikke-forpliktende ordrer (ordrelinjer) til Supply Chain Management for å foreta harde reserveringer og frigi til lageret eller oppdatere det endelige lagerantallet.
- Du kan angi at systemet skal [motpostere ikke-forpliktende reserveringer](#offset-scm) når fysisk lager oppdateres i Supply Chain Management.

Ikke-forpliktende reserveringer opprettes, forbrukes og avbrytes ved hjelp av API-kall til lagersynlighetstjenesten.

> [!NOTE]
> Du kan eventuelt konfigurere Supply Chain Management (og andre tredjepartssystemer) til automatisk å motpostere antallet som er reservert, ved å bruke Lagersynlighet. Motposteringsantallet slettes fra reserveringspostene i Lagersynlighet.
>
> Som standard aktiveres motregningsfunksjonen automatisk når du aktiverer funksjonen for ikke-forpliktende reservering.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Aktiver og konfigurer reservasjonsfunksjonen

Følg denne fremgangsmåten for å aktivere reservasjonsfunksjonen.

1. Logg deg på Power Apps, og åpne **Lagersynlighet**.
1. Åpne **Konfigurasjon**-siden.
1. På fanen **Funksjonsbehandling** aktiverer du funksjonen *OnHandReservation*.
1. Logg på Supply Chain Management-miljøet.
1. Gå til arbeidsområdet **[Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og aktiver funksjonen *Integrering av lagersynlighet med motpostering av reservasjon* (krever versjon 10.0.22 eller senere).
1. Gå til **Lagerstyring \> Oppsett \> Parametere for integrering av lagersynlighet**, åpne fanen **Motpostering av reservasjon** og gjør følgende innstilling:

    - **Aktiver motpostering av reservasjon** – Sett til *Ja* for å aktivere denne funksjonaliteten.
    - **Motposteringsmodifikator for reservasjon** – Velg lagertransaksjonsstatusen som motposterer reserveringer som gjøres i lagersynligheten. Denne innstillingen bestemmer ordrebehandlingsstadiet som utløser motregninger. Fasen spores etter ordrens lagertransaksjonsstatus. Velg én av følgende verdier:

        - *I ordre/bestilling* – Ordrer som har en *I ordre/bestilling*-status, sender en motposteringsforespørsel når den opprettes. Motposteringsantallet vil være antallet i den opprettede ordren (linje).
        - *Reserver* – Ordrer som har *Reserve*-status, vil sende en motforespørsel når de enten er reservert av en ordre eller er fysisk reservert. Når du motposterer på *Reserve*-statusen, sender ordren en motforespørsel til enhver ny lagerstatus som er nærmest reservert plukket (for eksempel plukk, følgeseddelpostert eller fakturert). Dette skjer selv om du hopper over reserveringen i Supply Chain Management og fortsetter til en annen lagerstatus (for eksempel hvis du hopper fra frigivelse til lager for å plukke og pakke). Forespørselen utløses bare én gang. Hvis den er utløst ved plukking, vil den ikke duplisere motregningen når en følgeseddel posteres. Motposteringsantallet vil være det samme som antallet til lagertransaksjonsstatusen når motregningen ble utløst (med andre ord *Reservert av bestilt*/*Reservert fysisk* eller en senere status på den tilsvarende ordrelinjen).

1. Logg deg tilbake til Lagersynlighet-appen, gå til **Konfigurasjon**-siden, og deretter, på fanen **Ikke-forpliktende reservasjon** gjennomgår du standardhierarkiet for ikke-forpliktende. Legg til nye dimensjoner i hierarkiet etter behov.
1. I delen **Angi tilordning av ikke-forpliktende reservasjon** viser du standardinnstillingene. Som standard registreres det ikke-forpliktende lagerantallet mot den fysiske `softreservephysical`-målingen til datakilden `iv`. Det beregnede målet *Tilgjengelig for reservasjon* tilordnes til `availabletoreserve`. Hvis du vil oppdatere det beregnede `availabletoreserve`-målet, kan du gå til **Konfigurasjon**-siden, og deretter utvide og endre det beregnede målet i kategorien **Beregnet mål**.

Hvis du vil ha mer informasjon, kan du se [Konfigurere Lagersynlighet](inventory-visibility-configuration.md).

> [!NOTE]
> Reservasjonshierarkiet beskriver serien med dimensjoner som må angis når det opprettes reservasjoner. Det fungerer på samme måte som indekshierarkiet fungerer for lagerbeholdninger, men brukes uavhengig, slik at brukere kan angi dimensjonsdetaljer for å gjøre mer presise reserveringer.
>
> Ditt ikke-forpliktende reservasjonshierarki bør inneholde `SiteId` og `LocationId` som komponenter fordi de konstruerer partisjonskonfigurasjonen av Lagersynlighet.

Hvis du vil ha mer informasjon om hvordan du konfigurerer reservasjoner, kan du se [Reservasjonskonfigurasjon](inventory-visibility-configuration.md#reservation-configuration).

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Bruk reservasjonsfunksjonen i Lagersynlighet

Når du kaller opp API-en for reservasjon, merker systemet reservasjonen av de angitte varene og antallene.

Her er et eksempelscenario og en eksempel-API-spørringstekst. Firmaet Contoso selger produktet D0002 (Kabinett) fra webområdet for e-handel. En kunde legger inn en salgsordre for en liten, rød bestilling via webområdet. Contoso bestemmer seg for å oppfylle denne ordren ved å bruke følgende dimensjoner:

- Organisasjons-ID = usmf
- Område = 1
- Lager = 11
- Produkt = D0002
- Farge = rød
- Størrelse = liten

Contoso har allerede satt opp en API-tilkobling til Lagersynlighet fra sitt eget e-handelssystem. Når ordren mottas, utløser systemutkalling et API-kall for å lage en ikke-forpliktende reservasjon for Lagersynlighet.

### <a name="create-soft-reservations-using-the-reservation-api"></a>Opprette ikke-forpliktende reserveringer ved hjelp av reservasjons-API

Reservasjoner gjøres i Lagersynlighet-tjenesten ved å sende en POSTER-forespørsel til tjenestens URL-adresse, for eksempel `/api/environment/{environmentId}/onhand/reserve`.

For en reservasjon må forespørselsteksten inneholde en organisasjons-ID, en produkt-ID, reservert antall og dimensjoner.

Når du kaller reservasjons-API, kan du styre reservasjonsvalideringen ved å angi den boolske `ifCheckAvailForReserv` parameteren i forespørselsteksten. Verdien `True` betyr at valideringen kreves, mens en verdi å `False` betyr at valideringen ikke er nødvendig. Standardverdien er `True`.

Hvis du vil avbryte en reservering eller ikke reservere angitte lagerantall, angir du antallet til en negativ verdi og angir parameteren `ifCheckAvailForReserv` til `False` for å hoppe over valideringen.

Her er et eksempel på forespørselsteksten som refererer til salgsordren i forrige kontekst.

```json
# Url

#Replace {endpoint} with your system endpoint.
    {endpoint}/api/environment/{environmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "Testrequest-0005",
    "organizationId": "usmf",
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "softreservphysical",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

En vellykket ikke-forpliktende reservasjonsforespørsel returnerer en *ID for ikke-forpliktende reservasjons* for hver reservasjonspost. Ikke-forpliktende reservasjon-ID er ikke en unik ID for en individuell Ikke-forpliktende reservasjonspost, men en kombinasjon av produkt-IDen og dimensjonsverdiene som er knyttet til den Ikke-forpliktende reservasjonsforespørselen. Du kan registrere Ikke-forpliktende reserverings-ID på ordrelinjen når du synkroniserer de reserverte ordrene til Supply Chain Management eller et annet ERP-system for motkonto.

### <a name="offset-soft-reservations-in-supply-chain-management"></a><a name="offset-scm"></a>Motpostere ikke-forpliktende reserveringer i Supply Chain Management

Du kan motpostere ikke-forpliktende antall etter at antallet i en ordre er fysisk trukket fra i Supply Chain Management eller et annet ERP-system. Lagersynlighet gir standard ikke-forpliktende reserveringsintegrering med Supply Chain Management.

Følg denne fremgangsmåten for å motposttere en ikke-forpliktende reservasjon.

1. Logg på Supply Chain Management.
1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** i handlingsruten.
1. Opprett den eksterne salgsordren på nytt, og legg til en salgslinje som bruker nøyaktig samme produkt-ID-, organisasjon, område, lager og dimensjonsverdier.
1. På hurtigfanen **Salgsordrelinjer**, velger du salgslinjen du nettopp lag inn, og deretter, på verktøylinjen, velger du **Beholdning \> Reservasjons-ID**.
1. Følg ett av disse trinnene:

    - Kopier den ikke-forpliktende reservasjons-ID i den ikke-forpliktende forespørselssvaret, og lim den inn i **reservering-ID**-feltet.
    - La feltet **Reserverings-ID** være tomt, men merk av for **automatisk motregning av beholdningstjeneste**. Systemet vil automatisk bestemme hvilke produkter og produktdimensjoner som skal motposteres, basert på vare-IDen og dimensjonsverdiene som er angitt på den valgte linjen.

1. Velg **OK**.
1. Mens samme salgslinje fremdeles er valgt, reserverer du det bestilte antallet fysisk ved å velge **Lager \> Reservasjon** på verktøylinjen for **Salgsordrelinjer**.
1. Hvis du tidligere har satt feltet **Modifikator for reservasjonsmotkonto** til *Reservert*, utløses motregningen når ordrelinjen har statusen *Reserver fysisk* eller *Reserver bestilte*. En satsvis jobb kjøres én gang i minuttet for å synkronisere motregnede forespørsler fra Supply Chain Management til Lagersynlighet.

> [!NOTE]
> For transaksjonsstatuser som har en angitt motposteringsmodifikator for reserversjon, vil transaksjonsoppdateringen motpostere den tilsvarende reservasjonsposten når alle følgende betingelser er oppfylt:
>
> - Reservasjons-ID-en på lagertransaksjonen samsvarer med reservasjons-ID-en til reservasjonsposten i Lagersynlighet.
> - Dimensjonene i lagertransaksjonen samsvarer med dimensjonene i reservasjonsposten i Lagersynlighet.
> - Endringer i lagertransaksjonsstatus utløser motpsoteringer for reserveringer når lagertransaksjonsstatusen viser at en ordreprosess er fullført eller hoppet over.

Forskyvningsantallet følger lagerantallet som er angitt på de relevante lagertransaksjonene. En motpostering trer bare ikke i kraft hvis det reservert antallet forblir i Lagersynlighet.

### <a name="cancel-or-revert-a-soft-reservation"></a>Avbryte eller tilbakestille en ikke-forpliktende reservasjon

Hvis en opprinnelig ordrelinje avbrytes eller slettes, og du må tilbakestille den tilsvarende ikke-forpliktende reserveringen, posterer du et negativt antall som har nøyaktig samme informasjon i API-spørringsteksten.
