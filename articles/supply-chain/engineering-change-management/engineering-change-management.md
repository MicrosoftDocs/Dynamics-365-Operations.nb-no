---
title: Behandle endringer i tekniske produkter
description: Dette emnet gir informasjon om behandling av teknisk endring. Behandling av tekniske endring har strukturerte prosesser for behandling av endringer i tekniske produkter, fra å foreslå, be om og foreta endringer, vurdere og godkjenne endringer, undersøke hva som er påvirket av eksisterende transaksjoner, og følge opp dem.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEcmRequestSelection,EngChgEcmRequestProducts,EngChgEcmRequestPriorityChart,EngChgEcmRequestListPage,EngChgEcmRequestFilteredPart,EngChgEcmRequestDetails,EngChgEcmReason,EngChgEcmProjTableInformation,EngChgEcmProductRoute,EngChgEcmProductRelease,EngChgEcmProductPreview, EngChgEcmWhereUsed, EngChgEcmInventTrans,EngChgEcmHeaderSelection,EngChgEcmHeaderPreviewPart,EngChgEcmHeaderFilteredPart,EngChgEcmHeaderDetails, EngChgCaseWhereUsedAnalysis, EngChgCaseValidatorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 56446e6a8abfcab83772e446dc7f01c529404b23
ms.sourcegitcommit: 05210ceefd8816b889019b2a6554855f3c5b2a6c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5954651"
---
# <a name="manage-changes-to-engineering-products"></a>Behandle endringer i tekniske produkter

[!include [banner](../includes/banner.md)]

Behandling av teknisk endring har strukturerte prosesser for behandling av endringer i tekniske produkter. Du kan bruke *prosessen for forespørsel om teknisk endring* til å foreslå og be om endringer, og deretter bruke *prosessen for ordre om teknisk endring* til å gjøre disse endringene. Brukere kan opprette forespørsler om teknisk endring eller ordrer om teknisk endring, og det er da en prosess for å gå gjennom og godkjenne dem, vurdere hvilke innvirkning de har på eksisterende transaksjoner, og følge opp dem.

## <a name="engineering-change-requests"></a>Forespørsler om teknisk endring

Med prosessen for forespørsel om teknisk endring kan du hente forespørsler om endringer fra alle relevante avdelinger i firmaet. Det spiller ingen rolle om du arbeider som en tekniker, eller i produksjon, leverandør, lager eller salgsavdeling: alle kan bruke en forespørsel om teknisk endring til å be om en endring. Denne endringen kan være en idé om et nytt produkt, et problem som du oppdaget mens du arbeidet med et eksisterende produkt, et forslag for forbedring av et eksisterende produkt eller noe annet.

Etter at noen har sendt en forespørsel om endring, behandles *gjennomgangen og godkjenningsprosessen* av en arbeidsflyt som identifiserer hvem som må godkjenne endringen (for eksempel produkteieren).

Hvis du vil definere en arbeidsflyt for ordrer om tekniske endringer eller utviklingsendringer, går du til **Behandling av teknisk endring \> Utviklingsarbeidsflyter**. Velg **Ny**, velg om arbeidsflyten skal brukes til å gjennomgå ordrer om tekniske endringer eller forespørsler om teknisk endring, og konfigurer deretter arbeidsflyten.

Hvis du vil ha mer informasjon om arbeidsflyter, kan du se [Oversikt over arbeidsflytsystem](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md). Hvis du vil ha mer informasjon om produkteiere, kan du se [Produkteiere](product-owner.md).

### <a name="create-a-new-engineering-change-request"></a>Opprett en ny forespørsel om teknisk endring

Følg en av fremgangsmåtene nedenfor for å opprette en forespørsel om teknisk endring.

- Gå til **Behandling av teknisk endring \> Felles \> Behandling av teknisk endring \> Forespørsler om teknisk endring**, og velg deretter **Ny** i handlingsruten.
- Åpne siden **Produktdetaljer** for et eksisterende utviklingsprodukt. I handlingsruten på **Tekniker**-fanen i **Behandling av teknisk endring**-gruppen velger du **Forespørsel om teknisk endring \> Ny forespørsel om teknisk endring**.

Det opprettes en ny endringsforespørsel. Du kan nå angi feltene i hver hurtigfane som beskrevet i følgende underdeler.

#### <a name="general-fasttab"></a>Hurtigfanen Generelt

I **Generelt**-hurtigfanen kan du gi en grunnleggende beskrivelse av endringsforespørselen. Følgende tabell beskriver feltene på denne hurtigfanen.

| Felt | beskrivelse |
|---|---|
| Endringsforespørsel | Angi et navn for forespørselen om teknisk endring. |
| Stillingstittel | Skriv inn tekst som kort beskriver eller identifiserer endringene i forespørselen. |
| Prioritet | Velg en verdi for å angi hvor høy prioriteten til endringen er. Du kan tilpasse de tilgjengelige verdiene for firmaet etter behov. (Hvis du vil ha mer informasjon, kan du se [Opprett vanlige verdier for behandling av teknisk endring](engineering-change-management-setup.md) .) |
| Kategori | Velg en verdi for å beskrive endringstypen du ber om. Du kan tilpasse de tilgjengelige verdiene for firmaet etter behov. (Hvis du vil ha mer informasjon, kan du se [Opprett vanlige verdier for behandling av teknisk endring](engineering-change-management-setup.md) .) |
| Viktighet | Velg en verdi for å angi alvorsgraden for problemet som skal løses ved å implementere forespørselen. Du kan tilpasse de tilgjengelige verdiene for firmaet etter behov. (Hvis du vil ha mer informasjon, kan du se [Opprett vanlige verdier for behandling av teknisk endring](engineering-change-management-setup.md) .) |
| Forespørsel fra | Navnet på brukeren som opprettet forespørselen. |
| På | Datoen da forespørselen ble opprettet. |
| Status | Statusen for forespørselen. Når en forespørsel opprettes for første gang, er statusen *Opprettet*. Når forespørselen er godkjent, endres statusen til *Godkjent*. Hvis det er opprettet en tilknyttet endringsordre for forespørselen, endres statusen til *Fulgt opp*. |
| Endringsordre | Endringsordrenummeret, hvis endringsforespørselen ble fulgt opp via en endringsordre. |

#### <a name="information-fasttab"></a>Hurtigfanen Informasjon

I **Informasjon**-hurtigfanen kan du legge til mer informasjon om forespørselen.

Hvis du vil legge til en rad i rutenettet, velger du **Ny** på verktøylinjen over rutenettet, og deretter velger du ett av følgende alternativer:

- **Fil** – Last opp en fil.
- **Bilde** – Last opp en bildefil.
- **Merknad** – Angi et notat direkte i rutenettet.
- **URL** – Angi en nettadresse direkte i rutenettet.

Følgende tabell beskriver feltene på hver rad.

| Felt | beskrivelse |
|---|---|
| Opprettingsdato og -klokkeslett | Datoen og klokkeslettet da raden ble opprettet. |
| Type | Informasjonstypen som raden ble opprettet for (fil, bilde, notat eller nettadresse). |
| beskrivelse | Angi en beskrivelse for raden. |
| Begrensning | En verdi som angir om informasjonen som er lagt til, kom fra en intern eller ekstern kilde. |
| Vedlagt | En merket avmerkingsboks indikerer at raden inneholder et vedlegg (en fil eller et bilde). Hvis du vil laste ned vedlegget, merker du raden, og deretter velger du **Åpne** på verktøylinjen over rutenettet. |

#### <a name="products-fasttab"></a>Hurtigfanen Produkter

I **Produkter**-hurtigfanen kan du liste opp hvert produkt som påvirkes av endringsforespørselen. Du kan bruke knappene på verktøylinjen til å legge til produkter i rutenettet eller fjerne produkter.

Denne listen er bare beregnet til informasjon. Du kan derfor legge til så mange relaterte produkter som du anser som relevante. Hvis du oppretter en endringsforespørsel fra **Produktdetaljer**-siden for et eksisterende produkt, skal dette produktet være oppført i **Produkter**-hurtigfanen etter at du har lagret forespørselsposten.

#### <a name="source-fasttab"></a>Hurtigfanen Kilde

Med **Kilde**-hurtigfanen kan du spore startpunktet for endringsforespørselen. Det er nyttig hvis du for eksempel vil se om endringsforespørselen ble opprettet fra en salgsordre, hvem som opprettet den, og hvilket firma den ble opprettet i.

### <a name="evaluate-the-business-impact-of-a-change-request"></a>Evaluere betydningen av en endringsforespørsel

Når du går gjennom en forespørsel om endring, kan du søke etter avhengigheter. På denne måten kan du vurdere virkningen av den forespurte endringen på åpne transaksjoner, for eksempel salgsordrer, produksjonsordrer og lagerbeholdninger.

1. Gå til **Behandling av teknisk endring \> Felles \> Behandling av teknisk endring \> Forespørsler om teknisk endring**.
1. Åpne en eksisterende endringsforespørsel, eller velg **Ny** i handlingsruten for å opprette en ny endringsforespørsel.
1. I handlingsruten i **Endringsforespørsel**-fanen i **Forretningspåvirkning**-gruppen velger du en av følgende knapper:

    - **Søk** – Skanner alle åpne transaksjoner, og åpner deretter **Forretningspåvirkning på åpne transaksjoner**-dialogboksen, som viser alle transaksjonene som vil bli påvirket av endringen.
    - **Vis forrige søk** – Åpne dialogboksen **Forretningspåvirkning på åpne transaksjoner**, som viser resultatene av forrige søk. (Et nytt søk utføres ikke.)

1. Hvis problemet som krever en endring, er kritisk, kan du blokkere de åpne transaksjonene eller varsle den ansvarlige brukeren ved å bruke knappene på verktøylinjen i dialogboksen **Forretningspåvirkning på åpne transaksjoner**.

### <a name="create-a-change-order-from-a-change-request"></a>Opprette en endringsordre fra en endringsforespørsel

En tekniker som ser gjennom en forespørsel om teknisk endring, kan opprette en endringsordre direkte fra siden **Forespørsler om teknisk endring**. I handlingsruten i **Endringsforespørsel**-fanen i **Ordre om teknisk endring**-gruppen velger du **Kopier kobling og produkter**.

## <a name="engineering-change-orders"></a>Ordrer om teknisk endring

Ordrer om teknisk endring har strukturerte prosesser for å gjøre endringer i utviklingsprodukter. Du foreslår endringer ved å bruke en kopi av utviklingsrelevante data. De reelle hoveddataene påvirkes ikke. Hvis du vil ha mer informasjon om utviklingsrelevante data, kan du se [Utviklingsversjoner og utviklingsproduktkategorier](engineering-versions-product-category.md).

Du kan opprette en ordre om teknisk endring som er basert på en godkjent forespørsel om teknisk endring. Teknikere kan også opprette ordrer om teknisk endring fra bunnen av. Du kan inkludere flere produkter på én enkelt ordre om teknisk endring ved å følge en av disse trinnene:

- Velg produkter manuelt.
- Bruk stykklisten til å inkludere produkter som er lavere i produktstrukturen (det vil si underordnede).
- Bruk et bruksstedsøk til å inkludere produkter som er høyere i produktstrukturen (det vil si overordnede).

Når forslaget om endringer er fullført, vil gjennomgangen og godkjenningsprosessen håndteres av en arbeidsflyt. Du kan definere forskjellige arbeidsflyter basert på prioritet og alvorsgrad.

Hvis du vil definere en arbeidsflyt for ordrer om tekniske endringer eller utviklingsendringer, går du til **Behandling av teknisk endring \> Utviklingsarbeidsflyter**. Velg **Ny**, velg om arbeidsflyten skal brukes til å gjennomgå ordrer om tekniske endringer eller forespørsler om teknisk endring, og konfigurer deretter arbeidsflyten.

Hvis du vil ha mer informasjon om arbeidsflyter, kan du se [Oversikt over arbeidsflytsystem](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

Her er noen vanlige interessenter som kan godkjenne en ordre om teknisk endring:

- **Produkteiere** – Hvis du vil ha mer informasjon om produkteiere, kan du se [Produkteiere](product-owner.md).
- **Ansvarlig teamleder** – **Tekniker**-feltet i **Topptekst**-visningen for ordre om teknisk endring viser teknikeren som opprettet ordren om tekniske endring. Hvis teknikeren tilhører en gruppe som er definert i systemet, viser feltet **Ansvarlig** lederen for teamet.
- **Økonomiavdeling** – Økonomiavdelingen kan måtte se gjennom saker der endringen omfatter høye kostnader.

Du kan velge om ordren om teknisk endring skal behandles direkte etter at den er godkjent, som en del av arbeidsflyten, eller om behandlingen skal utføres senere, som et manuelt trinn. Under behandling av en ordre om teknisk endring blir tekniske data på det faktiske produktet oppdatert.

Mens du ser gjennom en forespørsel om endring, i handlingsruten, i **Endringsforespørsel**-fanen i **Forretningspåvirkning**-gruppen, velger du **Søk** for å vurdere påvirkningen av forslått endring på åpne transaksjoner, for eksempel salgsordrer, produksjonsordrer og lagerbeholdning. Resultatene vises i dialogboksen **Forretningspåvirkning på åpne transaksjoner**, der du kan velge berørte transaksjoner og deretter bruke kommandoene på verktøylinjen til å vise mer informasjon, varsle den ansvarlige brukeren eller blokkere transaksjonen.

### <a name="engineering-change-orders-in-engineering-or-operational-companies"></a>Ordrer om teknisk endring i tekniske firmaer eller driftsfirmaer

Som beskrevet i [Tekniske firmaer og dataeierskapsregler](engineering-org-data-ownership-rules.md), varierer produkt dataene du kan redigere, avhengig av hvilken type juridisk enhet du arbeider i (et teknisk firma kontra et driftsfirma). Dataeierskapsregler brukes også for odrer om teknisk endring. Avhengig av den juridiske enheten der du oppretter en ordre om teknisk endring, kan du derfor foreta ulike typer endringer. Her er noen eksempler:

- Når det gjelder ordrer om teknisk endring i et *teknisk firma*, kan du gjøre grunnleggende endringer i de tekniske dataene. Du kan for eksempel opprette nye versjoner av et produkt, endre produktets struktur via stykklisten og endre tekniske attributtverdier. For hvert produkt som påvirkes, velger du en av følgende verdier i **Påvirkning**-feltet:

    - **Ingen** – Oppdater den eksisterende produktversjonen (oppdatering i versjon).
    - **Ny versjon** – Opprett en ny versjon som er basert på den valgte produktversjonen.
    - **Nytt produkt** – Opprett helt nytt produkt som er basert på den valgte produktversjonen.
    - **Ny variant** – Opprett en ny variant som er basert på den valgte produktversjonen. Informasjonen om stykklisten og ruten kopieres.

- Når det gjelder ordrer om teknisk endring i et *driftsfirma*, kan du endre logistikkdataene for produktet. Du kan for eksempel supplere den eksisterende stykklisten med innstillinger for leverandører, legge til lokale ruter eller lokale stykklister, og til og med supplere en stykkliste ved å legge til nye stykklistelinjer for lokale emballasjer, smørevæsker eller instruksjoner på det lokale språket. Suppleringer som brukere gjør i driftsfirmaet, beholdes når nye oppdateringer sendes fra det tekniske firmaet. Hvis du vil ha mer informasjon, kan du se [Tekniske firmaer og dataeierskapsregler](engineering-org-data-ownership-rules.md).

    Når ordrer om teknisk endring behandles i det tekniske firmaet, blir produktene opprettet eller oppdatert bare i det tekniske firmaet. Hvis produktets hoveddata også skal oppdateres, må du derfor også frigi produktene til driftsfirmaene.

- Du kan frigi produkter direkte fra ordrer om teknisk endring. Åpne endringsordren og, i handlingsruten, i **Endringsordre**-fanen i **Produktfrigivelser**-gruppen, velger du **Frigi produktstruktur**. Prosessen fungerer på samme måte som den fungerer når du frigir produkter fra siden **Frigitte produkter**. Hvis du vil ha mer informasjon, kan du se [Frigi produktstrukturer](release-product-structure.md).
- Du kan få produkter som automatisk er frigitt fra ordrer om teknisk endring, basert på følgende faktorer:

    - Nye frigivelser til firmaer der produkter ble frigitt tidligere. Velg **Søk** for å skanne alle tidligere versjoner, og velg deretter **Vis** for å vise resultatene. **Visning**-siden viser de forrige produktversjonene, og du kan velge hvilke produkter du vil frigi på nytt. Deretter lukker du **Visning**-siden og velger **Behandle** for å frigi de valgte produktene på nytt.
    - Frigi innstillinger automatisk i frigi-kontrollen for teknisk produktkategori. Du kan utføre denne frigivelsen som en del av arbeidsflyten. Når blokken **samle frigivelsesforslag** brukes, vil frigivelsesforslaget bli fylt ut med nypubliserte forslag (se det forrige listeelementet), og produkter vil bli frigitt til firmaer hvis det er merket av for **Automatisk frigivelse** i frigi-kontrollen i teknisk produktkategori. Du kan velge **Vis** for å vise resultatene, som beskrevet i det forrige listeelementet. Produktene vil også bli frigitt når blokken **behandle frigivelsesforslag** brukes. Hvis du velger bare å samle inn frigivelsesforslaget som en del av arbeidsflyten, kan du starte frigivelsen manuelt ved å velge **Behandle**, som beskrevet i det forrige listeelementet.

## <a name="follow-up-on-an-engineering-change-request-via-an-engineering-change-order"></a>Følg opp en forespørsel om teknisk endring ved hjelp av en ordre om teknisk endring

Så snart en forepørsel om teknisk endring er godkjent, kan du følge den opp via en ordre om teknisk endring. Du kan kombinere flere forespørsler om teknisk endring til én enkelt ordre om teknisk endring. Én enkelt ordre om teknisk endring kan til og med inkludere flere produkter. (Vanligvis bruker du denne fremgangsmåten når den samme endringen må brukes for flere produkter.) Du kan imidlertid ikke opprette flere ordrer om teknisk endring fra én enkelt forespørsel om teknisk endring.

Hvis du vil følge opp en endringsforespørsel via en endringsordre, åpner du endringsforespørselen, og deretter, i handlingsruten, i **Endringsordre**-fanen, i **Ordre om teknisk endring**-gruppen, velger du **Kopier kobling og produkter**. Du kan deretter velge en eksisterende ordre om teknisk endring som du vil koble endringsforespørselen til, eller du kan opprette en ny ordre om teknisk endring for den bestemte forespørselen.

## <a name="engineering-change-order-report"></a>Rapport for ordre om teknisk endring

Rapporter for ordre om teknisk endring beskriver endringene som ble gjort i en ordre om teknisk endring. De er nyttige både under og etter gjennomgangen og godkjenningsprosessen.

Hvis du vil vise en rapport for ordre om teknisk endring, åpner du den relevante endringsrekkefølgen, og deretter, i handlingsruten, i **Endringsforepørsel**-fanen, i **Vis**-gruppen, velger **Rapport for ordre om teknisk endring**.

## <a name="fields-on-an-engineering-change-order"></a>Felter i en ordre om teknisk endring

De fleste feltene på ordrer om teknisk endring er de samme som feltene for frigitte produkter, tekniske versjoner, dokumenter, stykklister (linjer) og ruter (operasjoner). Feltene i følgende tabell er imidlertid unike for endringsordrer.

| Felt | beskrivelse |
|---|---|
| Årsaker til teknisk endring | Velg årsaken til å endre det berørte produktet. |
| Endringsbeskrivelse | Angi en beskrivelse av endringen. |
| Nødvendig spesialverktøy | Angi om spesialverktøy kreves for å ta i bruk endringen. |
| Disposisjon om teknisk materiale | Velg en materialdisposisjonskode for eventuelt avfall som produseres når endringen brukes. |
| Kundegodkjenning kreves | Angi om det kreves godkjenning av kunden før endringen kan brukes. |
| Mottatt kundegodkjenning | Angi status for kundens godkjenning. |
| Helse, miljø og sikkerhet | Angi om regler for helse, miljø og sikkerhet gjelder for endringen. Hvis de gjør det, kan du deretter velge gjeldende regler. |

Du kan bruke knappen **Behold/kopier endringsinformasjon** til å kopiere endringsinformasjon mellom berørte produkter.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
