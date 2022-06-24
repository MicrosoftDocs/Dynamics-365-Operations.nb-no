---
title: Konfigurere farlige materialer
description: Denne artikkelen forklarer hvordan du konfigurerer dataene som kreves for å klassifisere varer som farlige materialer. Når du oppretter en salgsordre som inkluderer en vare som er klassifisert som et farlig materiale, genererer systemet dokumentasjon for farlig materiale for den aktuelle salgsordren når den sendes.
author: t-benebo
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 95d7a4d5e61b2f0ff2a9d52b7ccfa8deec1b309d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888506"
---
# <a name="set-up-hazardous-materials"></a>Konfigurere farlige materialer

[!include [banner](../includes/banner.md)]

Hvis du vil bruke funksjonaliteten for farlig materiale, må du først konfigurere dataene som er nødvendige for å klassifisere varer som farlig materiale. Når du deretter oppretter en salgsordre som inkluderer en vare som er klassifisert som et farlig materiale, genererer systemet dokumentasjon for farlig materiale for den aktuelle salgsordren når den sendes.

## <a name="turn-on-the-hazardous-materials-feature-for-your-system"></a>Aktivere funksjonen for farlig materiale for systemet

Per Supply Chain Management versjon 10.0.21 er denne funksjonen aktivert som standard. Administratorer kan bruke siden [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere eller deaktivere den hvis det er nødvendig. Her vises funksjonen som:

- **Modul:** *Behandling av produktinformasjon*
- **Funksjonsnavn:** *Produktinformasjon og forsendelsesdokumentasjon for farlig materiale*

## <a name="hazardous-material-regulations"></a>Forskrifter for farlig materiale

For å bruke prosessene for farlige materialer må du først opprette en forskrift. Forskriftene definerer hvordan den utskrevne forsendelsesteksten blir opprettet for en vare. De definerer også de tilknyttede leveringsmåtene.

Her er noen vanlige forskrifter:

- **ADR** – Forskrifter som er knyttet til den internasjonale transporten av farlige gods på veier
- **CFR 49** – Forskrifter i USA for transport av farlig gods
- **IMDG** – Den internasjonale koden for farlige maringods (IMDG, International Marine Dangerous Goods)
- **IATA** – Forskriftene til det internasjonale lufttransportforbundet (IATA, International Air Transport Association) for farlig gods

Disse forskriftene hjelper deg med å bestemme hvilken informasjon som skal vises når du skriver ut forsendelsesteksten for en vare. Du kan definere så mange forskrifter som du må overholde.

> [!IMPORTANT]
> Funksjonaliteten for å definere informasjonskoder som er relatert til farlige materialer, gir ikke firmaet ditt samsvar med forskrifter. Det er bare et verktøy som hjelper deg med å bygge prosesser for firmaet.

Vanligvis er en forskrift for en bestemt transportmåte tilgjengelig, for eksempel sjøfrakt, veifrakt eller flyfrakt. Derfor kan du knytte hver forskrift til en leveringsmåte. Leveringsmåten vil bli brukt når bestemte dokumenter skrives ut i lagerstyring. I lagerstyring er hver forsendelse koblet til en transportør og transportørtjeneste som er definert i **Transport**-modulen. Leveringsmåten er knyttet til transportøren og transportørtjenesten. Når du kjører en rapport, brukes leveringsmåten til å finne teksten som skal skrives ut, som er knyttet til en frigitt vare.

Disse oppsettsdataene er ikke spesifikke for hver juridiske enhet (firma). Du kan derfor ha et felles sett med informasjon for farlige material informasjon som deles mellom alle juridiske enheter.

For hver forskrift kan du definere en materialliste og bruke den som en malliste som er knyttet til frigitte varer. Du kan også definere et utskriftsoppsett for hver forskrift. Ved hjelp av et utskriftsoppsett kan du definere hvordan forsendelsesteksten for en vare skal konstrueres. Utskriftsoppsettet brukes til å konstruere forsendelsesteksten for en frigitt vare.

Hvis du vil definere forskrifter for farlig materiale, kan du gå til **Behandling av produktinformasjon \> Oppsett \> Forsendelsesdokumentasjon for farlig materiale \> Forskrifter for farlig materiale**. På siden **Forskrifter for farlig materiale** kan du opprette et hvilket som helst antall forskrifter og konfigurere hver av dem ved å bruke feltene som er beskrevet i følgende underdeler.

### <a name="hazardous-material-regulation-header"></a>Overskrift for forordning for farlige materialer

Hver forskrift har en kode og en beskrivelse. Følgende tabell beskriver feltene som er tilgjengelige i overskriften.

| Felt | beskrivelse |
|---|---|
| Reguleringskode | Angi en kode for å identifisere forskriftsregistreringen for det farlige materialet. |
| beskrivelse | Angi en beskrivelse av forskriften for det farlige materialet. |

### <a name="print-setup-fasttab"></a>Hurtigfanen Utskriftsoppsett

Hver forskrift kan ha et hvilket som helst antall utskriftsoppsett. Du definerer utskriftsoppsettet i hurtigfanen **Utskriftsoppsett**. Følgende tabell beskriver feltene som er tilgjengelige for hvert utskriftsoppsett.

| Felt | beskrivelse |
|---|---|
| Rekkefølge | Definer rekkefølgen som feltene skal refereres i, i forsendelsesteksten. |
| Skriv ut felt | Velg feltet som skal tas med i forsendelsesteksten. Ikke alle feltene for det farlige materialet vil være tilgjengelig for utskrift. Bare de felles feltene som brukes til å definere forsendelsestekst i de ulike forskriftene, vil være tilgjengelige. Du bør definere det første utskriftsfeltet som et feltskilletegn som har en **Sekvens**-verdi på *0* (null), slik at det kan brukes som skilletegn mellom andre felt. Det kreves bare én referanse til feltskilletegnet.<p>Følgende verdier er tilgjengelige:</p><ul></li><li>**Feltskilletegn** – Dette utskriftsfeltet brukes som feltskilletegn for teksten. Det kreves bare ett feltskilletegn i sekvensen. Vanligvis bør du angi verdien **Sekvens** for dette utskriftsfeltet til *0* (null). Systemet vil se etter et feltskilletegn og bruke det første som blir funnet i listen. Tekstverdien som brukes i strengen, kommer fra feltet **Skriv ut**.</li><li>**Identifikasjon** – Dette utskriftsfeltet plasserer [identifikasjonskoden og/eller beskrivelsen](#identification) i utskriftsteksten.</li><li>**Klasse** – Dette utskriftsfeltet plasserer [klassekoden og/eller beskrivelsen](#classes) i utskriftsteksten.</li><li>**Inndeling** – Dette utskriftsfeltet plasserer [inndelingskoden og/eller beskrivelsen](#divisions) i utskriftsteksten.</li><li>**Emballasjegruppe** – Dette utskriftsfeltet plasserer [emballasjegruppekoden og/eller beskrivelsen](#packing-group) i utskriftsteksten.</li><li>**Tunnelkode og/eller beskrivelse** – Dette utskriftsfeltet plasserer [tunnelkoden og/eller beskrivelsen](#tunnel) i utskriftsteksten.</li><li>**Korrekt forsendelsesnavn** – Dette utskriftsfeltet plasserer [korrekt forsendelsesnavn](hazmat-items.md#hazmat-description) i utskriftsteksten.</li><li>**Teknisk navn** – Dette utskriftsfeltet plasserer [teknisk navn og/eller beskrivelse](#technical-name) i utskriftsteksten.</li><li>**Transportkategori** – Dette utskriftsfeltet plasserer [transportkategorikode og/eller beskrivelse](#transport-category) i utskriftsteksten.</li><li>**Lagring** – Dette utskriftsfeltet plasserer [lagringskoden og/eller beskrivelsen](#stowage) i utskriftsteksten.</li><li>**Fast tekst** – Dette utskriftsfeltet legger inn teksten som er definert i feltet **Fast tekst** for denne raden.</li><li>**Etikettkode og/eller beskrivelse** – Dette utskriftsfeltet plasserer [etikettkoden og/eller beskrivelsen](#label) i utskriftsteksten.</li><li>**Flypakking** – Dette utskriftsfeltet plasserer [instruksjonskoden og/eller beskrivelsen for flypakking](#packing-instruction) i utskriftsteksten.</li><li>**Begrenset antall** – Dette utskriftsfeltet kontrollerer om varen er merket som en [begrenset antall-vare](hazmat-items.md#material-management), og hvis den er det, skriver inn teksten som er definert i feltet **Fast tekst** for denne raden.</li><li>**Emballasjebeskrivelse** – Dette utskriftsfeltet plasserer [emballasjebeskrivelsen](#packing-description) i utskriftsteksten.</li></ul> |
| Skriv ut før | Skriv inn teksten som skal skrives ut før innholdet som er definert av innstillingen i feltet **Skriv ut**. |
| Skriv ut etter | Skriv inn teksten som skal skrives ut etter innholdet som er definert av innstillingen **Utskriftsfelt**. |
| Skriv ut med forrige | Merk av i denne avmerkingsboksen for å hindre at feltskilletegnet skrives ut mellom det forrige feltet og dette feltet. Bruk denne avmerkingsboksen for å skrive ut felt som enten er valgfritt eller inkludert i et annet utskriftsfelt. |
| Fast tekst | Hvis du setter feltet **Utskriftsfelt** til **Fast tekst** eller **Begrenset antall**, skriver du inn teksten som skal skrives ut. |
| Inkluder i utskrift | Velg hvilken verdi eller hvilke verdier fra det valgte utskriftsfeltet som skal skrives ut for denne raden. Du kan skrive ut koden, beskrivelsen eller både koden og beskrivelsen. |

### <a name="mode-of-delivery-fasttab"></a>Hurtigfanen Leveringsmåte

Forskriften er en delt tabell og er ikke spesifikk for hver juridiske enhet. Leveringsmåter er imidlertid spesifikke for juridiske enheter. Når du definerer en leveringsmåte, må du derfor velge relasjonen mellom forskrifter, juridisk enhet og leveringsmåte.

Følgende tabell beskriver feltene som er tilgjengelige i hurtigfanen **Leveringsmåte**.

| Felt | beskrivelse |
|---|---|
| Bedrift | Velg en juridisk enhet som skal knyttes til denne forskriften. |
| Leveringsmiddel | Velg leveringsmåten som skal knyttes til reguleringen, basert på den juridiske enheten du valgte. |

### <a name="country-fasttab"></a>Hurtigfanen Land

For referanseformål kan du føre opp landene eller regionene som reguleringen er relevant for. Når forsendelsesrapporter kjøres, brukes imidlertid bare leveringsmåten til å bestemme forskriften. Når du går gjennom en lagerforsendelse, er det ikke en direktekobling til leveringsmåten. Forsendelsen kan være knyttet til en transportør og transportørtjeneste. Når du definerer en transportørtjeneste, må du knytte den til en leveringsmåte. Denne relasjonen blir brukt på forsendelsesrapporter, for eksempel fraktbrevet, til å finne forsendelsesutskriftsteksten for en vare.

Følgende tabell beskriver feltet som er tilgjengelig i hurtigfanen **Land**.

| Felt | beskrivelse |
|---|---|
| Land/område | Velg et land/område du vil knytte forskriften til. |

## <a name="material-codes"></a><a name="hazmat-codes"></a>Materialkoder

Materialkoder oppretter innstillinger som er relatert til en bestemt farlig komponent som kan inkluderes i et frigitt produkt. Hver enkelt materialekode tilhører en bestemt forskrift for farlig materiale, og definisjonen må følge denne forskriften. Når du bruker en materialkode for et frigitt produkt ved hjelp av feltet **Materialkode**, brukes alle materialekodeinnstillingene for farlig materiale automatisk for dette produktet. Prosessen med å definere frigitte produkter er derfor raskere og mindre utsatt for feil.

Hvis du vil administrere farlige materialdefinisjoner, følger du disse trinnene.

1. Gå til **Behandling av produktinformasjon \> Oppsett \> Forsendelsesdokumentasjon for farlig materiale \> Forskrifter for farlig materiale**.
2. Velg forskriften det skal konfigureres en farlig materiale-definisjon for.
3. Velg **Farlige materialer** i fanen **Oppsett** i handlingsruten.
4. I **Materialkode**-feltet angir du en materialkode for definisjonen for farlig materiale. Du velger denne verdien når du bruker materialkoden i et frigitt produkt.

    Feltet **Reguleringskode** er skrivebeskyttet og viser forskriften du valgte i trinn 2.

5. Bruk de gjenværende feltene på denne siden til å opprette og definere hvert enkelt farlige materiale som gjelder for de valgte forskriftene. Feltene som er tilgjengelige, er et delsett av feltene for farlig materiale som er tilgjengelige for individuelle frigitte produkter. Hvis du vil ha mer informasjon, kan du se [Farlige materialer i produkter, ordrer, forsendelser og laster](hazmat-items.md).

## <a name="hazardous-material-classification-groups"></a><a name="classification-groups"></a>Klassifiseringsgrupper for farlig materiale

Hver klassifiseringsgruppe for farlig materiale definerer en gruppe feltverdier som etablerer en mal. Du kan bruke denne malen senere når du definerer informasjonen for farlig materiale for en frigitt vare.

Når du tilordner koden for en klassifiseringsgruppe for farlige materiale til en frigitt vare, kopieres informasjonen som er tilknyttet denne klassifiseringsgruppen, til de riktige feltene for varen. Derfor kan du forenkle installasjonsprosessene ved å etablere et sett med relaterte feltverdier som du ofte bruker sammen.

Disse oppsettdataene er ikke spesifikke for hver juridiske enhet. Du kan derfor ha et felles sett med informasjon for farlige material informasjon som deles mellom alle juridiske enheter.

Hvis du vil definere klassifiseringsgrupper for farlig materiale, kan du gå til **Behandling av produktinformasjon \> Oppsett \> Forsendelsesdokumentasjon for farlig materiale \> Klassifiseringsgruppe for farlig materiale**. På siden **Klassifiseringsgruppe for farlig materiale** kan du opprette et hvilket som helst antall grupper og konfigurere hver av dem ved å bruke feltene som er beskrevet i følgende tabell.

| Felt | beskrivelse |
|---|---|
| Gruppekode | Skriv inn en kode som skal brukes til å identifisere gruppen. |
| beskrivelse | Angi en beskrivelse av gruppen. |
| Klassekode | Knytt en [klassekode](#classes) for farlig materiale til gruppen. |
| Inndelingskode | Knytt en [inndelingskode](#divisions) for farlig materiale til gruppen. |
| Emballasjegruppekode | Knytt en [emballasjegruppekode](#packing-group) til gruppen. |
| Transportkategorikode | Knytt en [transportkategorikode](#transport-category) til gruppen. |
| Multiplikator | Angi multiplikatoren for farlig materiale som gjelder for den valgte klassen og inndelingen av farlige materialer, i henhold til gjeldende forskrift. Denne multiplikatoren brukes som en del av formelen som beregner total *poengsum for farlig materiale* som er inkludert i en last eller forsendelse. Hvis du vil ha mer informasjon om poeng for farlig materiale og denne multiplikatoren, se [hurtigfanen Materialstyring](hazmat-items.md#material-management). |

## <a name="hazardous-material-classes"></a><a name="classes"></a>Klasser for farlig materiale

En klasse for farlig materiale tilordnes vanligvis til listen over klasser som er oppgitt i forskriftene som du overholder. Den amerikanske forskriften CFR 49 viser for eksempel "klasse 3" som brannfarlige og lettantennelige væsker. Du kan definere klassene som er relevante for materialene du må klassifisere.

Hver klasse blir tilordnet et materialoppsett i materiallisten som er relatert til forskriften. Du vil tilordne en klasse til hver frigitt vare etter behov, for å beskrive de farlige egenskapene til et produkt.

Disse oppsettdataene er ikke spesifikke for hver juridiske enhet. Du kan derfor ha et felles sett med informasjon for farlige material informasjon som deles mellom alle juridiske enheter.

Klasser for farlig materiale fungerer sammen med inndelinger, grupper og kompatibilitetsgrupper på følgende måte:

- Når du tilordner en klasse for farlig materiale til en frigitt vare, må du også tilordne en [inndeling av farlig material](#divisions).
- Du kan bruke klasser av farlig materiale sammen med [klassifiseringsgrupper av farlig materiale](#classification-groups) til å opprette en mal med koder for å definere varer.
- Du kan bruke [kompatibilitetsgrupper for farlig materiale](#compatibility-groups) til å fastsette hvilke klasser med farlig materiale og inndelinger som kan sendes sammen.

Hvis du vil definere klasser for farlig materiale, kan du gå til **Behandling av produktinformasjon \> Oppsett \> Forsendelsesdokumentasjon for farlig materiale \> Klasser for farlig materiale**. På siden **Klasse for farlig materiale** kan du opprette et hvilket som helst antall klasser og konfigurere hver av dem ved å bruke feltene som er beskrevet i følgende tabell.

| Felt | beskrivelse |
|---|---|
| Klassekode | Skriv inn en kode som skal brukes til å identifisere denne klassen. Du definerer denne koden for varen. Den vil deretter brukes i oppslagslister når du tilordner en klasse for farlig materiale til en frigitt vare. |
| beskrivelse | Angi en beskrivelse av klassen. |

## <a name="hazardous-material-divisions"></a><a name="divisions"></a>Inndelinger av farlig materiale

En inndeling av farlig materiale er et delsett av en klasse for farlig materiale. Du må tilordne både en inndeling og en klasse til alle produkter som inneholder farlige materialer.

For klasser som ikke har noen inndelinger, oppretter du en inndeling der koden er *0*. I IATA-forskrifter har for eksempel klasse 7 for radioaktive materialer ingen underinndelinger. I dette tilfellet vil du opprette en *0*-inndeling som du kan knytte til et frigitt produkt når du tilordner klassen.

Disse oppsettdataene er ikke spesifikke for hver juridiske enhet. Du kan derfor ha et felles sett med informasjon for farlige material informasjon som deles mellom alle juridiske enheter.

Inndelinger av farlig materiale fungerer sammen med klasser, grupper og kompatibilitetsgrupper på følgende måter:

- Når du tilordner en inndeling av farlig materiale til en frigitt vare, må du også tilordne en [klasse for farlig materiale](#classes).
- Du kan bruke inndelinger av farlig materiale sammen med [klassifiseringsgrupper av farlig materiale](#classification-groups) til å opprette en mal med koder for å definere varer.
- Du kan bruke [kompatibilitetsgrupper for farlig materiale](#compatibility-groups) til å fastsette hvilke klasser med farlig materiale og inndelinger som kan sendes sammen.

Hvis du vil definere inndelinger av farlig materiale, kan du gå til **Behandling av produktinformasjon \> Oppsett \> Forsendelsesdokumentasjon for farlig materiale \> Inndeling av farlig materiale**. På siden **Inndeling av farlig materiale** kan du opprette et hvilket som helst antall inndelinger og konfigurere hver av dem ved å bruke feltene som er beskrevet i følgende tabell.

| Felt | beskrivelse |
|---|---|
| Inndeling | Angi en kode som skal brukes som referansenummer for inndelingen. |
| beskrivelse | Angi en beskrivelse av inndelingen. |
| Klasse | Slå opp og tilordne klassen som inndelingen tilhører. |

## <a name="hazardous-material-compatibility-groups"></a><a name="compatibility-groups"></a>Kompatibilitetsgrupper for farlig materiale

Kompatibilitetsgrupper for farlig materiale fastsetter hvilke klasser og inndelinger med farlig materiale som kan sendes sammen. Når operatører oppretter lagerlaster og forsendelser, kan de kjøre en kompatibilitetskontroll som vil gi en advarsel hvis lasten eller forsendelsen omfatter varer som ikke alle tilhører det samme kompatibilitetsnivået.

Disse oppsettdataene er ikke spesifikke for hver juridiske enhet. Du kan derfor ha et felles sett med informasjon for farlige material informasjon som deles mellom alle juridiske enheter.

Hvis du vil definere kompatibilitetsgrupper for farlige materialer, kan du gå til **Behandling av produktinformasjon \> Oppsett \> Forsendelsesdokumentasjon for farlig materiale \> Kompatibilitetsgruppe for farlig materiale**. På siden **Kompatibilitetsgruppe for farlig materiale** kan du opprette et hvilket som helst antall kompatibilitetsgrupper og konfigurere hver av dem ved å bruke feltene som er beskrevet i følgende underdeler.

### <a name="hazardous-material-compatibility-group-header"></a>Overskrift for kompatibilitetsgruppe for farlig materiale

Hver kompatibilitetsgruppe har en kode og en beskrivelse. Følgende tabell beskriver feltene som er tilgjengelige i overskriften.

| Felt | beskrivelse |
|---|---|
| Kompatibilitetsgruppe | Skriv inn en kode som skal brukes til å identifisere kompatibilitetsgruppen |
| beskrivelse | Angi en beskrivelse av kompatibilitetsgruppen. |

### <a name="compatibility-group-details"></a>Detaljer for kompatibilitetsgruppe

Hver kompatibilitetsgruppe fastsetter en liste over klasser og inndelinger med farlig materiale som kan sendes sammen.

| Felt | beskrivelse |
|---|---|
| Klasse | Velg en klasse for farlig materiale som er kompatibel med alle andre klasser i gruppen. |
| Inndeling | Velg en inndeling av farlig materiale som tilhører den valgte klassen. |

## <a name="hazardous-material-specification-values"></a>Spesifikasjonsverdier for farlig materiale

Microsoft Dynamics 365 Supply Chain Management tilbyr flere spesifikasjonstyper for farlig materiale. For hver type må du opprette et sentralisert sett med verdier for hvert relevante felt. Brukerne kan deretter velge mellom disse verdiene når de konfigurerer definisjoner for farlig materiale eller frigitte produkter. Supply Chain Management inneholder en samling av sider der du kan fastsette verdiene. Hver side er reservert for én type spesifikasjon. Hvis du vil ha en beskrivelse av hver tilgjengelige spesifikasjon og informasjon om hvordan du fastslår hvilke verdier som er tilgjengelige for den, kan du se underdelene nedenfor.

Et eksempel på en spesifikasjon for farlig materiale er _lagringskode_, som angir hvordan et gitt materiale kan lagres under transport. Ved å bruke informasjonen i denne delen vil du opprette en sentral samling av lagringskoder. Denne samlingen blir deretter presentert for brukere i en rullegardinliste når de angir lagringskoden for et frigitt produkt.

Disse spesifikasjonsverdiene for farlig materiale er ikke spesifikke for hver juridiske enhet, og derfor kan du ha et sett med felles verdier som deles mellom alle juridiske enheter.

Du vil bruke [materialkoder](#hazmat-codes) til å opprette fellessamlinger av innstillinger for hver spesifikasjon, slik den gjelder for en gitt forskrift. Du kan deretter bruke den riktige koden på hvert frigitte produkt etter behov. Hvis du vil ha informasjon om hvordan du bruker en kode for farlig materiale på et bestemt frigitt produkt, og hvordan du konfigurerer individuelle innstillinger for dette produktet for alle typer oppsett som beskrives her, kan du se [Farlige materialer i produkter, ordrer, forsendelser og laster](hazmat-items.md).

### <a name="hazardous-material-emergency-response"></a>Farlig materiale - nødsvar

*Beredskap for farlig materiale*-spesifikasjonen angir hva som skal gjøres hvis noe går galt mens et produkt som inneholder et bestemt farlig materiale, blir transportert.

Hvis du vil definere verdier for denne spesifikasjonen, kan du gå til **Behandling av produktinformasjon \> Oppsett \> Forsendelsesdokumentasjon for farlig materiale \> Beredskap for farlig materiale**. På siden **Beredskap for farlig materiale** kan du opprette et hvilket som helst antall verdier og konfigurere hver med en klassifiseringskode og en kort beskrivelse.

### <a name="hazardous-material-identification"></a><a name="identification"></a>Farlig materiale - identifikasjon

*Identifikasjon av farlig materiale*-spesifikasjonen identifiserer klassen eller typen av et farlig materiale. Verdien er vanligvis en kode som er basert på en FN-standard. Hver klasse identifiseres av en kode og en beskrivelse, og den kan angi grenser for transportmetoder. Hvis du for eksempel vil identifisere brannfarlige varer eller materialer, oppretter du en klasse for farlig materiale som bruker koden *FL* og beskrivelsen *Brannfarlig*. Du angir også at klassen ikke skal transporteres med fly.

Hvis du vil definere verdier for denne spesifikasjonen, kan du gå til **Behandling av produktinformasjon \> Oppsett \> Forsendelsesdokumentasjon for farlig materiale \> Identifikasjon av farlig materiale**. På siden **Identifikasjon av farlig materiale** kan du opprette et hvilket som helst antall verdier og konfigurere hver av dem ved å bruke feltene som er beskrevet i følgende tabell.

| Felt | beskrivelse |
|---|---|
| Identifikasjon | Angi en kode som skal brukes som referansenummer, som identifiserer denne klassen med farlig materiale. |
| beskrivelse | Angi en beskrivelse av denne klassen. |
| Begrens fra transport i luften | Merk av i denne avmerkingsboksen for å angi at denne klassen med farlig materiale ikke skal transporteres ved fly. |
| Begrens fra sjøtransport | Merk av i denne avmerkingsboksen for å angi at denne klassen med farlig materiale ikke skal transporteres med båt. |

### <a name="hazardous-material-label"></a><a name="label"></a>Farlig materiale - etikett

Spesifikasjonen *Farlig materiale-etikett* identifiserer etiketten for farlige varer som må brukes på relevante frigitte produkter. Selve etikettene beskriver hvordan produktet skal håndteres. Du har for eksempel et produkt som inneholder en giftig gass. I dette tilfellet angir du en etikettkode som representerer etiketten for farlig gass. Du bygger også forretningsprosessen slik at den slår opp denne verdien når du leverer produkter.

Hvis du vil definere verdier for denne spesifikasjonen, kan du gå til **Behandling av produktinformasjon \> Oppsett \> Forsendelsesdokumentasjon for farlig materiale \> Etikett for farlig materiale**. På siden **Etikett for farlig materiale** kan du opprette et hvilket som helst antall etiketter og konfigurere hver med en identifikasjonskode og en kort beskrivelse.

### <a name="hazardous-material-packing-descriptions"></a><a name="packing-description"></a>Farlig materiale - emballasjebeskrivelser

Spesifikasjonen *Emballasjebeskrivelser for farlig materiale* angir hvordan en farlig vare må pakkes. Det kan for eksempel hende at den må pakkes inn i en bestemt type ståltrommel eller en annen type spesialemballasje.

Hvis du vil definere verdier for denne spesifikasjonen, kan du gå til **Behandling av produktinformasjon \> Oppsett \> Forsendelsesdokumentasjon for farlig materiale \> Emballasjebeskrivelser for farlig materiale**. På siden **Emballasjebeskrivelse for farlig materiale** kan du opprette et hvilket som helst antall emballasjebeskrivelser og konfigurere hver med en identifikasjonskode og en kort beskrivelse.

### <a name="hazardous-material-packing-group"></a><a name="packing-group"></a>Farlig materiale - emballasjegruppe

Spesifikasjonen *Emballasjegruppe for farlig materiale* identifiserer emballasjegruppen for en farlig vare. Med emballasjegruppen kan du definere en kode og en beskrivelse for å angi hvordan farlig materiale må pakkes under transport eller forsendelse. Emballasjegruppen tilordnes til varen via siden for **vare, farlig materiale**.

Hvis du vil definere verdier for denne spesifikasjonen, kan du gå til **Behandling av produktinformasjon \> Oppsett \> Forsendelsesdokumentasjon for farlig materiale \> Empallasjegruppe for farlig materiale**. På siden **Emballasjegruppe for farlig materiale** kan du opprette et hvilket som helst antall emballasjegrupper og konfigurere hver med en identifikasjonskode og en kort beskrivelse.

### <a name="hazardous-material-packing-instruction"></a><a name="packing-instruction"></a>Farlig materiale - emballasjeinstruksjon

Spesifikasjonen *Emballasjeinstruksjon for farlig materiale* identifiserer emballasjeinstruksjoner som må følges når en gitt farlig vare er klargjort for transport med fly.

Hvis du vil definere verdier for denne spesifikasjonen, kan du gå til **Behandling av produktinformasjon \> Oppsett \> Forsendelsesdokumentasjon for farlig materiale \> Emballasjeinstruksjon for farlig materiale**. På siden **Emballasjeinstruksjon for farlig materiale** kan du opprette et hvilket som helst antall emballasjeinstruksjonsidentifikatorer og konfigurere hver med en identifikasjonskode og en kort beskrivelse.

### <a name="hazardous-material-stowage"></a><a name="stowage"></a>Farlig materiale - stuing

Spesifikasjonen *Lagring av farlig materiale* angir hvordan et produkt må lagres i en forsendelse når det transporteres med båt.

Hvis du vil definere verdier for denne spesifikasjonen, kan du gå til **Behandling av produktinformasjon \> Oppsett \> Forsendelsesdokumentasjon for farlig materiale \> Lagring av farlig materiale**. På siden **Lagring av farlig materiale** kan du opprette et hvilket som helst antall lagringsidentifikatorer og konfigurere hver med en identifikasjonskode og en kort beskrivelse.

### <a name="hazardous-material-transport-category"></a><a name="transport-category"></a>Farlig materiale - transportkategori

Spesifikasjonen *Transportkategori for farlig materiale* brukes vanligvis til å gruppere lignende farlige produkter i rapporter. Transportkategorier brukes for eksempel i rapporten **Forsendelsessammendrag**, som du kan skrive ut fra lagerforsendelsesregistreringen.

Hvis du vil definere verdier for denne spesifikasjonen, kan du gå til **Behandling av produktinformasjon \> Oppsett \> Forsendelsesdokumentasjon for farlig materiale \> Transportkategori for farlig materiale**. På siden **Transportkategori for farlig materiale** kan du opprette et hvilket som helst antall transportkategorier og konfigurere hver med et visningsnavn og en kort beskrivelse.

### <a name="hazardous-material-technical-name"></a><a name="technical-name"></a>Farlig materiale - teknisk navn

Spesifikasjonen *Teknisk navn på farlig materiale* kan brukes til å gi et vanlig brukt eller internt firmanavn som beskriver hvert materiale.

Hvis du vil definere verdier for denne spesifikasjonen, kan du gå til **Behandling av produktinformasjon \> Oppsett \> Forsendelsesdokumentasjon for farlig materiale \> Teknisk navn på farlig materiale**. På siden **Teknisk navn på farlig materiale** kan du opprette et hvilket som helst antall tekniske navn og konfigurere hvert navn med et visningsnavn og en kort beskrivelse.

### <a name="hazardous-material-tunnel"></a><a name="tunnel"></a>Farlig materiale - tunnel

Spesifikasjonen *Tunnel for farlig materiale* begrenser typene av tunneler som et farlig materiale kan transporteres gjennom ved å identifisere tunneltypene som må brukes. Tunnelkategorier etableres etter gjeldende bestemmelser for transport av farlig materiale. Denne spesifikasjonen gjelder vanligvis bare for veitransport.

Hvis du vil definere verdier for denne spesifikasjonen, kan du gå til **Behandling av produktinformasjon \> Oppsett \> Forsendelsesdokumentasjon for farlig materiale \> Tunnel for farlig materiale**. På siden **Tunnel for farlig materiale** kan du opprette et hvilket som helst antall tunnelidentifikatorer og konfigurere hver med en identifikasjonskode og en kort beskrivelse.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]