---
title: Arbeide med lokasjonsdirektiver
description: Denne artikkelen beskriver hvordan du arbeider med lokasjonsdirektiver. Lokasjonsdirektiver er brukerdefinerte regler som bidrar til å identifisere plukke- og plasseringslokasjoner for lagerbevegelse.
author: Mirzaab
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7705ea132521353cd6af7245df90aafaf23af885
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903702"
---
# <a name="work-with-location-directives"></a>Arbeide med lokasjonsdirektiver

[!include [banner](../includes/banner.md)]

Lokasjonsdirektiver er regler som bidrar til å identifisere plukke- og plasseringslokasjoner for lagerbevegelse. I en salgsordretransaksjon bestemmer for eksempel et lokasjonsdirektiv hvor varene blir plukket og hvor de plukkede varene skal plasseres. Lokasjonsdirektiver består av en topptekst og tilknyttede linjer. De opprettes for bestemte *arbeidsordretyper*.

> [!NOTE]
> Denne artikkelen gjelder funksjoner i **Lagerstyring**-modulen. Det gjelder ikke for funksjoner i modulen [Lagerstyring](../inventory/inventory-home-page.md).

Du kan bruke lokasjonsdirektiver til å utføre følgende oppgaver:

- Plasser innkommende varer.
- Plukk og plasser varer for utgående transaksjoner.
- Plukk og plasser råvarer for produksjon.
- Etterfyll lokasjoner.

## <a name="prerequisites"></a>Forutsetninger

Før du kan opprette et lokasjonsdirektiv, må du følge denne fremgangsmåten for å kontrollere at forutsetningene er på plass.

1. Kontroller at den nødvendige lisensnøkkelen er aktivert. Gå til **Systemadministrasjon \> Oppsett \> Lisenskonfigurasjon**, utvid **Hansel**-lisensnøkkelen, og velg deretter konfigurasjonsnøkkelen **Lager- og transportstyring**. Legg merke til at administratortilgang kreves for dette trinnet.
1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lagre**.
1. Opprett et lager.
1. På hurtigfanen **Lager** setter du alternativet **Bruk lagerstyringsprosesser** til *Ja*.
1. Opprett lokasjoner, lokasjonstyper, lokasjonsprofiler og lokasjonsformater. Hvis du vil ha mer informasjon, kan du se [Konfigurere lokasjoner i et WMS-aktivert lager](./tasks/configure-locations-wms-enabled-warehouse.md).
1. Opprett steder, soner og sonegrupper. Hvis du vil ha mer informasjon, kan du se [Lageroppsett](../../commerce/channels-setup-warehouse.md) og [Konfigurere lokasjoner i et WMS-aktivert lager](./tasks/configure-locations-wms-enabled-warehouse.md).

## <a name="work-order-types-for-location-directives"></a>Arbeidsordretyper for lokasjonsdirektiver

Mange av feltene som kan angis for lokasjonsdirektiver, er felles for alle arbeidsordretyper. Andre felter er imidlertid spesifikke for bestemte arbeidsordretyper.

![Arbeidsordretyper for lokasjonsdirektiver.](media/Location_Directives_Work_Order_Types.png "Arbeidsordretyper for lokasjonsdirektiver")

> [!NOTE]
> To arbeidsordretyper, *Annullert arbeid* og *Syklustelling*, brukes bare av systemet. Lokasjonsdirektiver kan ikke opprettes for disse arbeidsordretypene.

Tabellene i følgende underdeling viser en liste over felles typer og arbeidsordretypebestemte felter som er tilgjengelige når du definerer et lokasjonsdirektiv.

### <a name="fields-that-are-common-to-all-work-order-types"></a>Felter som er felles for alle arbeidsordretyper

Tabellen nedenfor viser en oversikt over feltene som er felles for alle arbeidsordretyper.

| Hurtigfane | Felt |
|---|---|
| Lokasjonsdirektiver | Arbeidstype |
| Lokasjonsdirektiver | Site |
| Lokasjonsdirektiver | Lager |
| Lokasjonsdirektiver | Direktivkode |
| Lokasjonsdirektiver | Flere SKUer |
| Linjer | Serienummer |
| Linjer | Fra-antall |
| Linjer | Til antall |
| Linjer | Enhet |
| Linjer | Plasser antall |
| Linjer | Begrens etter enhet |
| Linjer | Avrund oppover til enhet |
| Linjer | Plasser pakkeantall |
| Linjer | Tillat deling |
| Lokasjonsdirektivhandlinger | Serienummer |
| Lokasjonsdirektivhandlinger | Navn |
| Lokasjonsdirektivhandlinger | Bruk av fast lokasjon |
| Lokasjonsdirektivhandlinger | Tillat negativ beholdning |
| Lokasjonsdirektivhandlinger | Parti aktivert |
| Lokasjonsdirektivhandlinger | Strategi |

### <a name="fields-that-are-specific-to-work-order-types"></a><a name="fields-specific-types"></a>Felter som er bestemte for arbeidsordretyper

Tabellen nedenfor viser en oversikt over feltene som er spesifikke for bestemte arbeidsordretyper.

| Hurtigfane | Felt | Arbeidsordretype |
|---|---|---|
| Lokasjonsdirektiver | Søk etter | Bestillinger |
| Lokasjonsdirektiver | Gjeldende disposisjonskode | Bestillinger |
| Lokasjonsdirektiver | Disposisjonskode | Bestillinger |
| Lokasjonsdirektiver | Gjeldende disposisjonskode | Plasser ferdigvarer |
| Lokasjonsdirektiver | Disposisjonskode | Plasser ferdigvarer |
| Lokasjonsdirektiver | Gjeldende disposisjonskode | Returordrer |
| Lokasjonsdirektiver | Disposisjonskode | Returordrer |
| Lokasjonsdirektiver | Gjeldende disposisjonskode | Kanban plassert |
| Lokasjonsdirektiver | Gjeldende disposisjonskode | Kanban-plukking |
| Linjer | Mal for umiddelbar etterfylling | Salgsordre |
| Linjer | Mal for umiddelbar etterfylling | Råvareplukking |
| Linjer | Mal for umiddelbar etterfylling | Utstedelse for overføring |
| Linjer | Mal for umiddelbar etterfylling | Kanban-plukking |

## <a name="open-the-location-directives-page"></a>Åpne siden for lokasjonsdirektiver

Hvis du åpne siden **Lokasjonsdirektiver**, går du til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.

Derfra kan du vise, opprette og redigere lokasjonsdirektiver ved hjelp av kommandoene i handlingsruten. Se resten av delene i denne artikkelen hvis du vil ha informasjon om hvordan du bruker alle feltene som er tilgjengelige på siden.

## <a name="action-pane"></a>Handlingsrute

Handlingsruten på siden **Lokasjonsdirektiver** inneholder knapper som du kan bruke til å opprette, redigere og slette direktiver (**Rediger**, **Ny** og **Slett**). Den inneholder også følgende knapper som lar deg justere rekkefølgen lokasjonsdirektivet behandles i, og konfigurere en spørring som definerer kriteriene for bruk av lokasjonsdirektivet:

- **Flytt opp** – Flytt det valgte lokasjonsdirektivet opp i sekvensen. Du kan for eksempel flytte den fra sekvensnummer 4 til sekvensnummer 3.
- **Flytt ned** – Flytt det valgte lokasjonsdirektivet ned i sekvensen. Du kan for eksempel flytte den fra sekvensnummer 4 til sekvensnummer 5.
- **Rediger spørring** – Åpne en dialogboks der du kan definere betingelsene som det valgte lokasjonsdirektivet skal behandles under. Det kan for eksempel hende at du vil at den bare skal gjelde for et bestemt lager.

## <a name="location-directives-header"></a>Topptekst for lokasjonsdirektiver

Toppteksten for lokasjonsdirektivet inneholder følgende felter for sekvensnummeret og det beskrivende navnet på lokasjonsdirektivet:

- **Sekvensnummer** – Dette feltet angir sekvensen som systemet prøver å bruke hvert lokasjonsdirektiv i, for den valgte arbeidsordretypen. Laveste numre brukes først. Du kan endre rekkefølgen ved å bruke knappene **Flytt opp** og **Flytt ned** i handlingsruten.
- **Navn** – Angi et beskrivende navn for lokasjonsdirektivet. Dette navnet skal være til hjelp for å identifisere den generelle bruken av direktivet. Angi for eksempel *Salgsordreplukking på lager 24*.

## <a name="location-directives-fasttab"></a>Hurtigfane for lokasjonsdirektiver

Feltene i hurtigfanen **Lokasjonsdirektiver** er spesifikke for arbeidsordretypen som er valgt i feltet **Arbeidsordretype** i listeruten.

- **Arbeidstype** – Velg hvilken type arbeid som skal utføres. Tilgjengelige verdier avhenger av typen lagertransaksjon som du har valgt i feltet **Arbeidsordretype**. Velg én av følgende verdier:

    - **Plasser** – Lokasjonsdirektivet vil prøve å finne den beste lokasjonen for å plassere eller finne beholdning som kommer inn i systemet fra mottak, produksjon eller lagerjusteringer. Det kan også brukes til å definere plasseringen på stadielokasjonen eller den endelige plasseringen på en forsendelseslokasjon.
    - **Plukk** – Lokasjonsdirektivet vil prøve å finne de beste lokasjonene for å reservere beholdning fysisk fra (opprette arbeid). Plukkingen kan fullføres (det vil si at plukklinjen kan lukkes) selv om arbeidet ikke er fullført. Brukeren kan fullføre fysisk plukking. I systemet er denne handlingen et plukketrinn. Brukeren kan deretter avbryte fra mobilenheten og fullføre arbeidet senere. Arbeidshodet lukkes imidlertid først når den endelige plasseringen er fullført.

    > [!IMPORTANT]
    > De andre verdiene i feltet **Arbeidstype** er ikke relevante for lokasjonsdirektiver. De vises bare fordi feltet ikke er filtrert slik at det samsvarer med den valgte arbeidsordretypen.

- **Område** – Dette feltet er obligatorisk fordi lokasjonsdirektivet må kunne fastslå området og lageret det er gyldig for.
- **Lager** – Dette feltet er obligatorisk fordi lokasjonsdirektivet må kunne fastslå området og lageret det er gyldig for.
- **Direktivkode** – Velg direktivkoden som skal knyttes til en arbeidsmal eller etterfyllingsmal. På siden **Direktivkode** kan du opprette nye koder som kan brukes til å koble arbeidsmaler eller etterfyllingsmaler til lokasjonsdirektiver. Direktivkoder kan også brukes til å opprette en kobling mellom en hvilken som helst linje i en arbeidsmal og et lokasjonsdirektiv (for eksempel en rampedør eller en stadieplassering).

    > [!TIP]
    > Hvis en direktivkode er angitt, søker ikke systemet etter lokasjonsdirektiver etter sekvensnummer når arbeid må genereres. Det vil i stedet søke etter direktivkode. På denne måten kan du være mer nøyaktig angående lokasjonsdirektivet som brukes for et spesifikt trinn i en arbeidsmal, for eksempel trinnet for oppsamling av materialer.

- **Flere SKU-er** – Sett dette alternativet til *Ja* for å aktivere flere lagerenheter (SKU-er) som skal brukes på en lokasjon. Flere SKU-er må for eksempel være aktivert for rampedørplasseringen. Hvis du aktiverer flere SKU-er, blir plasseringen angitt i arbeid som forventet. Plasseringslokasjonen kan imidlertid bare håndtere en plassering for flere varer (hvis arbeid inneholder forskjellige SKU-er som må plukkes og plasseres). Det vil ikke være mulig å behandle en enkelt SKU-plassering. Hvis du setter dette alternativet til *Nei*, vil plasseringslokasjonen bare angis hvis plasseringen bare har én SKU-type.

    > [!IMPORTANT]
    > Hvis du skal kunne utføre både plasseringer med flere varer og enkelt-SKU-plasseringer, må du angi to linjer som har samme struktur og oppsett, men du må sette alternativet **Flere SKU-er** til *Ja* for en linje og *Ingen* for den andre. For plasseringsoperasjoner må du derfor ha to identiske lokasjonsdirektiver, selv om du ikke må skille mellom én eller flere SKU-er i en arbeids-ID. Hvis du ikke definerer begge disse plasseringsdirektivene, vil det komme uventede forretningsprosesslokasjoner fra lokasjonsdirektivet som er brukt. Du må bruke et lignende oppsett for lokasjonsdirektiver som har **arbeidstypen** *plukk* hvis du må behandle ordrer som omfatter flere SKU-er.

    Bruk alternativet **Flere SKU-er** for arbeidslinjer som behandler mer enn ett varenummer. (Varenummeret vil være tomt i arbeidsdetaljene, og det vil bli vist som **Flere** på behandlingssidene i mobilappen Lagerstyring.)

    I et typisk eksempelscenario er en arbeidsmal satt opp slik at den har mer enn ett plukk/plasser-par. I dette tilfellet vil du kanskje søke etter en bestemt oppsamlingslokasjon som skal brukes for linjer med **arbeidstypen** *Plasser*.

    > [!NOTE]
    > Hvis alternativet **Flere SKU-er** er satt til *Ja*, kan du ikke velge **Rediger spørring** i handlingsruten, fordi spørringen ikke kan evaluere på varenivå når det er flere varer. Hvis du vil kontrollere at det ønskede lokasjonsdirektivet er valgt, kan du bruke **Direktivkode**-feltet til å lede valget mellom lokasjonsdirektivet som er knyttet til plasseringslinjene der denne direktivkoden er tilordnet i arbeidsmalen.

    Hvis du ikke alltid arbeider med operasjoner av typen enkelt vare eller blandet vare, er det viktig at du definerer to lokasjonsdirektiver for den angitte *Plasser*-arbeidstypen: en der alternativet **Flere SKU-er** er satt til *Ja* og en der det er satt til *Nei*.

- **Gjeldende disposisjonskode** – Angi om disposisjonskoden til lokasjonsdirektivet må samsvare med disposisjonskoden som brukes når varen mottas, eller om lokasjonsdirektivet kan velges basert på en hvilken som helst disposisjonskode. Hvis du velger *Nøyaktig samsvar* og **Disposisjonskode**-feltet er tomt, vurderes bare tomme disposisjonskoder for dette lokasjonsdirektivet.

    > [!NOTE]
    > Dette feltet er bare tilgjengelig for valgte arbeidsordretyper der etterfyllingen er tillatt. Hvis du vil ha en fullstendig liste, kan du se [Felter som er spesifikke for arbeidsordretyper](#fields-specific-types) tidligere i denne artikkelen.

- **Søk etter** – Angi om plasseringsantallet skal være hele antallet på nummerskiltet, eller om det skal være vare etter vare. Bruk dette feltet til å sikre at alt innholdet på et nummerskilt settes inn på ett sted, og at systemet ikke foreslår at du deler innholdet inn i flere steder for **Forhåndsvarsel for forsendelse** (nummerskiltmottak), **Blandet nummerskiltmottak** og **Klyngemottaksprosesser**. (**Klyngemottaksprosessen** krever at funksjonen [Klyngeplasseringsfunksjon](putaway-clusters.md) er aktivert.) Virkemåten av lokasjonsdirektivspørringen, linjene og lokasjonsdirektivhandlingene vil variere, avhengig av verdien du velger. **Linjer**-hurtigfanen brukes bare når **Søk etter** er satt til *vare*.

    > [!NOTE]
    > Dette feltet er bare tilgjengelig for valgte arbeidsordretyper der etterfyllingen er tillatt. Hvis du vil ha en fullstendig liste, kan du se [Felter som er spesifikke for arbeidsordretyper](#fields-specific-types).

- **Disposisjonskode** – Dette feltet brukes til lokasjonsdirektiver som har arbeidsordretypen *Bestillinger*, *Plasser ferdigvarer* eller *Returordrer* og arbeidstypen *Plasser*. Bruk det til å lede flyten til å bruke et bestemt lokasjonsdirektiv, avhengig av disposisjonskoden som en arbeider som er valgt i mobilappen Lagerstyring. Du kan for eksempel sende returnerte varer til en inspeksjonslokasjon før de returneres til lager. En disposisjonskode kan knyttes til en lagerstatus. På denne måten kan det brukes til å endre lagerstatusen som en del av en mottaksprosess. Du kan for eksempel ha en disposisjonskode, *Spørsmål og svar*, som setter lagerstatusen til *Spørsmål og svar*. Du kan deretter ha et eget lokasjonsdirektiv for å flytte lageret til en karantenelokasjon.

    > [!NOTE]
    > Dette feltet er bare tilgjengelig for valgte arbeidsordretyper der etterfyllingen er tillatt. Hvis du vil ha en fullstendig liste, kan du se [Felter som er spesifikke for arbeidsordretyper](#fields-specific-types).

## <a name="lines-fasttab"></a>Hurtigfanen Linjer

Bruk hurtigfanen **Linjer** til å opprette betingelser for å bruke de relaterte handlingene som er angitt i hurtigfanen **Handlinger for lokasjonsdirektiv**. For hver linje kan du angi et minimumsantall og et maksimumsantall som handlingene skal gjelde for. Du kan også angi at handlingene skal brukes på en bestemt lagerenhet.

- **Sekvensnummer** – Angi sekvensen som hver lokasjonsdirektivlinje skal behandles i, for den valgte arbeidstypen. Du kan endre rekkefølgen etter behov ved å bruke knappene **Flytt opp** og **Flytt ned** på verktøylinjen.
- **Fra antall** – Angi starten på antallsområdet linjen gjelder for. Angi antallet i måleenheten som er valgt i **Enhet**-feltet.
- **Til antall** – Angi slutten på antallsområdet linjen gjelder for. Angi antallet i måleenheten som er valgt i **Enhet**-feltet.
- **Enhet** – Velg måleenhet for varene. Du kan angi et minimums- og maksimumsantall som direktivet skal gjelde for, og du kan angi at direktivet skal være for en bestemt lagerenhet. **Enhet**-feltet brukes *bare* for evaluering av antall. For å finne ut om lokasjonsdirektivlinjen gjelder i det hele tatt bruker systemet antallet i enheten som er angitt på linjen. Hver gang som det når en lokasjonsdirektivlinje, prøver systemet å konvertere behovsenheten til enheten som er angitt på linjen. Hvis enhetskonverteringen ikke finnes, går systemet videre til neste linje.
- **Finn antall** – Dette feltet brukes bare når det gjøres forsøk på å legge til eller finne varer i lageret. (Derfor gjelder den bare når feltet **Arbeidstype** er satt til *Plasser*.) Velg en av følgende verdier for å angi antallet som brukes til å evaluere om et antall er innenfor **Fra antall** til **Til antall**-området:

    - **Antall nummerskilter** – Bruk antallet på nummerskiltet som mottas.
    - **Antall delt opp i enheter** – Bruk antallet som er brukt i løpet av transaksjonen. Du får for eksempel et antall på 1 000 i et lager, og deler det opp i 10 nummerskilter, der hver har et antall på 100. I dette tilfellet kan du bruke et antall på 1 000 varer i stedet for nummerskiltantallet på 100.
    - **Restantall** – Bruk antallet som fortsatt må mottas på bestillingslinjen som behandles.
    - **Forventet antall** – Bruk det totale antallet av bestillingslinjen, uansett hva som allerede er mottatt.

- **Begrens etter enhet** – Med denne avmerkingsboksen kan du opprette lokasjonsdirektivlinjen som gjelder for en måleenhet eller flere måleenheter. Velg den for å begrense måleenhetene som vurderes som gyldige valgkriterier for lokasjonsdirektivlinjene. Denne funksjonaliteten fungerer bare for lokasjonsdirektiver der feltet **Arbeidstype** er satt til *Plukk*.

    Når du for eksempel reserverer antall, vil du bare reservere paller fra et bestemt sett med lokasjoner. I dette tilfellet vil linjene begrense denne rekkefølgen til paller på en slik måte at et hvilket som helst antall som er mindre enn en pall, ikke blir valgt for lokasjonsdirektivet.

    Legg merke til at avmerkingsboksen **Begrens etter enhet** ikke styrer enheten eller enhetene som brukes på arbeidslinjer. Enhetsbegrensningen gjelder bare for enhetene som gjøres tilgjengelige via enhetssekvensgruppen. En vare er for eksempel knyttet til en enhetssekvensgruppe som inkluderer både *Paller*-enheten og *Stykk*-enheten. En måleenhet er definert der 1 pall = 100 stykk, og lokasjonsdirektivet bruker funksjonen **Begrens etter enhet** bare for paller. I tillegg er det definert en arbeidsmal som begrenser opprettelsen av arbeidshodet til 50 stykk. I dette tilfellet vil det bli opprettet arbeidslinjer på 50 stykk. Følg denne fremgangsmåten for å angi måleenheten for begrensning:

    1. På **Linjer**-hurtigfanen velger du **Begrens etter enhet** på verktøylinjen. (Denne knappen blir tilgjengelig når du merker av for **Begrens etter enhet** på linjen og deretter velger **Lagre**.)
    1. På siden **Begrens etter enheter** velger du måleenheten du vil begrense, ved hjelp av prosessene plukk og plasser i **Enhet**-feltet.

- **Avrund oppover til enhet** – Dette feltet fungerer sammen med avmerkingsboksen **Begrens etter enhet**. Hvis for eksempel **Begrens etter enhet** og **Avrund oppover til enhet** er valgt på lokasjonsdirektivlinjen, skal arbeidet som er generert fra direktivet for plukking for råvarer, avrundes opp til et multiplum av en av håndteringsenhetene som er angitt på siden **Begrens etter enhet**.

    > [!NOTE]
    > Dett **Avrund oppover til enhet**-oppsettet fungerer bare for ordretypen *Plukk arbeid for råvare* og bare for lokasjonsdirektiver der feltet **Arbeidstype** er satt til *Plukk*.

- **Plasser pakkeantall** – Hvis du angir et emballasjeantall i en salgsordre, overføringsordre eller produksjonsordre, kan du bruke denne avmerkingsboksen til å begrense systemet slik at det bare kan velge lokasjoner som har minst det pakkede antallet.

    > [!NOTE]
    > Denne funksjonen fungerer bare med lokasjonsdirektiver av *plukktypen*.

- **Tillat deling** – Angi om lokasjonsdirektivet kan dele antallet som mottas, eller antallet som reserveres, på tvers av flere lagerlokasjoner, eller om hele antallet må være plassert på én enkelt lokasjon eller reservert fra én lokasjon for å opprette arbeid.
- **Mal for umiddelbar etterfylling** – Bruk dette feltet til å opprette en tilkobling til en etterfyllingsmal, slik at etterfylling starter umiddelbart hvis varer ikke er tildelt. Hvis dette feltet er tomt, starter ikke etterfylling før alle linjene i lokasjonsdirektivet er behandlet.

    > [!NOTE]
    > Dette feltet er bare tilgjengelig for valgte arbeidsordretyper der etterfyllingen er tillatt. Hvis du vil ha en fullstendig liste, kan du se [Felter som er spesifikke for arbeidsordretyper](#fields-specific-types).

## <a name="location-directive-actions-fasttab"></a>Hurtigfane Handlinger for lokasjonsdirektiv

Du kan definere flere lokasjonsdirektivhandlinger for hver linje. Et serienummer brukes igjen til å bestemme rekkefølgen som handlingene er vurdert i. På dette nivået kan du definere en spørring for å definere hvordan du finner den beste plasseringen i lageret. Du kan også bruke forhåndsdefinerte verdier for **Strategi** for å finne en optimal lokasjon.

- **Sekvensnummer** – Dette feltet viser sekvensen som handlingene blir behandlet i, for den valgte arbeidstypen. Du kan endre rekkefølgen ved å bruke knappene **Flytt opp** og **Flytt ned** på verktøylinjen.
- **Navn** – Angi navnet på lokasjonsdirektivhandlingen. Være spesifikk slik at handlingen som utføres, er tydelig i navnet.
- **Bruk av fast lokasjon** – Angi hvilke lokasjoner lokasjonsdirektivet skal vurdere. Velg én av følgende verdier:

    - **Faste og ikke-faste lokasjoner** – Lokasjonsdirektivet tar alle lokasjoner i betraktning.
    - **Bare faste lokasjoner for produktet** – Lokasjonsdirektivet tar bare faste lokasjoner for produkter i betraktning.
    - **Bare faste lokasjoner for produktvarianten** – Lokasjonsdirektivet tar bare faste lokasjoner for produktvarianter i betraktning.

- **Tillat negativt beholdning** – Velg dette for å tillate negativ beholdning på den angitte lagerlokasjonen i lokasjonsdirektiver.
- **Parti aktivert** – Velg denne avmerkingsboksen for å bruke partistrategier for varene som er partiaktivert. Det er viktig at du merker av for dette alternativet for prosesser som bruker lokasjonsdirektiver til å finne lokasjoner for å plukke partinummersporede varer fra. På denne måten inkluderes søket etter steder som inneholder partinummersporede varer. Hvis det er merket av i denne avmerkingsboksen, og **Strategi**-feltet er satt til *Ingen*, går systemet videre til den neste handlingslinjen.
- **Strategi** –Hvis du vil gjøre det lettere og raskere å angi hvilke handlinger som er knyttet til hver lokasjonsdirektivlinje, kan du velge en av følgende forhåndsdefinerte strategier:

    - **Ingen** – Ingen strategi blir brukt.
    - **Samsvar pakkeantall** – Denne strategien bekrefter om en plukklokasjon har det angitte pakkeantallet. Denne strategien er bare gyldig når feltet **Arbeidstype** er satt til *Plukk*.
    - **Konsolider** – Denne strategien konsoliderer varer på en spesifikk lokasjon når det allerede finnes like varer. Denne strategien er bare gyldig når feltet **Arbeidstype** er satt til *Plasser*. Et typisk oppsett for plassering forsøker å konsolidere på den første handlingslinjen, og deretter prøver det å plassere uten konsolidering på den andre linjen. Konsolidering av varer gjør senere plukking mer effektivt.
    - **FEFO-partireservering** – Denne strategien bruker partireserveringen første frist, først ut (FEFO). Bruk den når lagerstedet er definert ved hjelp av en utløpsdato for parti og tilordnes partireservering. Du kan bare bruke denne strategien for partiaktiverte varer. Den er bare gyldig når feltet **Arbeidstype** er satt til *Plukk*.
    - **Avrund oppover til fullstendig nummerskilt og FEFO-parti** – Denne strategien kombinerer elementene i strategiene *FEFO-partireservering* og *Avrund oppover til et fullstendig nummerskilt*. Den er bare gyldig for varer med partiaktiverte satsvise jobber og lokasjonsdirektiver som har arbeidstypen *Plukk*. Linjen må være partiaktivert for å kunne bruke strategien *FEFO-partireservering*, og strategien *Avrund oppover til et fullstendig nummerskilt* kan bare brukes til etterfylling. Hvis denne strategien konfigureres sammen med en lokasjonsbeholdningsgrense, kan det føre til at den valgte plasseringen for plassering av arbeid blir overbelastet, og at lagergrenser ignoreres.
    - **Avrund oppover til et fullstendig nummerskilt** – Denne strategien brukes til å avrunde lagerantallet oppover, slik at det tilsvarer nummerskiltantallet som er tilordnet varene som må plukkes. Du kan bare bruke denne strategien for etterfyllingslokasjonsdirektiver av typen *plukk*. Hvis denne strategien konfigureres sammen med en lokasjonsbeholdningsgrense, kan det føre til at den valgte plasseringen for plassering av arbeid blir overbelastet, og at lagergrenser ignoreres.
    - **Nummerskiltledet** – Bruk strategien når du frigir ordren til lageret for å opprette plukk- og plasseringsarbeidet. Du kan bruke denne tilnærmingen for flere nummerskilter. Denne strategien vil prøve å reservere og opprette plukkarbeid mot lokasjonene som inneholder de forespurte nummerskiltene som er knyttet til overføringsordrelinjene. Hvis disse handlingene ikke kan fullføres, men du likevel vil opprette et plukkarbeid, bør du imidlertid gå tilbake til en annen strategi for lokasjonsdirektivhandlinger. Avhengig av forretningsprosesskravene kan det også være lurt å søke etter lager i et annet område av lageret.
    - **Tom plassering med innkommende arbeid** – Bruk denne strategien til å finne tomme lokasjoner. En lokasjon anses som tom hvis den ikke har fysisk beholdning og ikke forventet innkommende arbeid. Du kan bare bruke denne strategien for lokasjonsdirektiver av arbeidstypen *Plasser*.
    - **Lokasjon med aldersfordelt FIFO** – Bruk først inn, først ut-strategien (FIFO) til å levere både partisporingsvarer og ikke-partisporingsvarer, basert på datoen da beholdningen ble registrerte på lageret. Denne funksjonen kan være spesielt nyttig for ikke-partisporingslageret, der ingen utløpsdato er tilgjengelig for sortering. FIFO-strategien finner lokasjonen som inneholder den eldste aldersfordelingsdatoen, og den tildeler plukking basert på den aldersfordelingsdatoen.
    - **Lokasjon med aldersfordelt LIFO** – Bruk sist inn, sist ut-strategien (LIFO) til å levere både partisporingsvarer og ikke-partisporingsvarer, basert på datoen da beholdningen ble registrerte på lageret. Denne funksjonen kan være spesielt nyttig for ikke-partisporingslageret, der ingen utløpsdato er tilgjengelig for sortering. LIFO-strategien finner lokasjonen som inneholder den nyeste aldersfordelingsdatoen, og den tildeler plukking basert på den aldersfordelingsdatoen.

## <a name="example-using-location-directives"></a>Eksempel: Bruke lokasjonsdirektiver

I dette eksemplet vurderes det en bestillingsprosess der lokasjonsdirektivet må finne ledig kapasitet i et lager for lagervarer som nettopp er registrert i mottakssonen. Først må du prøve å finne ledig kapasitet i lageret ved å konsolidere med eksisterende lagerbeholdning. Hvis konsolidering ikke er mulig, må du finne en ledig lokasjon.

I dette scenariet må du definere to lokasjonsdirektivhandlinger. Den første handlingen i sekvensen må bruke strategien *Konsolider* og andre må bruke strategien *Tom lokasjon uten innkommende arbeid*. Med mindre du definerer en tredje handling for å håndtere et overflytscenario er to resultater mulig når det er ikke mer kapasitet i lageret: arbeid kan opprettes selv om ingen lokasjoner defineres, eller arbeidsopprettingsprosessen kan mislykkes. Resultatet bestemmes av oppsettet på siden **Feil med lokasjonsdirektiv** der du kan bestemme om du vil velge alternativet **Stopp arbeid ved feil med lokasjonsdirektiv** for hver arbeidsordretype.

## <a name="next-step"></a>Neste trinn

Når du har opprettet lokasjonsdirektiver, kan du knytte hver direktivkode til en arbeidsmalkode for arbeidsoppretting. Hvis du vil ha mer informasjon, kan du se [Kontrollere lagerarbeid ved hjelp av arbeidsmaler og lokasjonsdirektiver](./control-warehouse-location-directives.md).

## <a name="additional-resources"></a>Tilleggsressurser

- Video: [Dyp dykk i konfigurasjon av lagerstyring](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Hjelpeartikkel: [Kontrollere lagerarbeid ved hjelp av arbeidsmaler og lokasjonsdirektiver](control-warehouse-location-directives.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]