---
title: Administrere sjøreiser
description: Denne artikkelen beskriver hvordan du arbeider med sjøreiser. En sjøreise representerer som regel et fartøy. Avhengig av praksis og fremgangsmåter kan den imidlertid representere en leverandør, en bestilling eller en annen vare som gir mening for organisasjonen.
author: Weijiesa
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMTableListPage, ITMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 43f28a7e30dbbe15bb02d26483289f25515fcfca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905870"
---
# <a name="manage-voyages"></a>Administrere sjøreiser

[!include [banner](../../includes/banner.md)]

En sjøreise representerer som regel et fartøy. Avhengig av praksis og fremgangsmåter kan den imidlertid representere en leverandør, en bestilling eller en annen vare som gir mening for organisasjonen.

Siden **Alle sjøreiser** formidler sjøreisedetaljer, informasjon om levering og etterkalkulering samt informasjon om varer, bestillinger og overføringsordrer. Hvis du vil åpne siden **Alle sjøreiser**, går du til **Netto innkjøpspris \> Sjøreiser \> Alle sjøreiser**. Denne siden viser en liste over alle sjøreiser. Du kan bruke knappene i handlingsruten til å opprette, slette og arbeide med sjøreiser. Velg en sjøreise i listen for å vise detaljene for den.

> [!NOTE]
> Forsendelsescontainere og folioer er koblet til en sjøreise. Innkjøpslinjer er koblet til en forsendelsescontainer. Hvis forsendelsescontainere og folioer er deaktivert, kan de også kobles direkte til en sjøreise. I tillegg godkjennes kostnader som angis her, til alle tilknyttede innkjøpslinjer.

## <a name="action-pane"></a>Handlingsrute

Handlingsruten på siden **Sjøreiser** inneholder knapper du kan bruke til å arbeide med en sjøreise. Hver knapp utfører én handling. Handlingsruten inneholder også faner, der hver av dem igjen inneholder et sett med relaterte knapper. Med unntak av der annet er angitt, er alle knapper og faner tilgjengelige både i listevisningen på siden **Alle sjøreiser** og i detaljert visning for én sjøreise.

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Knapper som vises direkte i handlingsruten

Tabellen nedenfor beskriver knappene som er tilgjengelige i handlingsruten.

| Knapp | beskrivelse |
|---|---|
| Nye | Opprett en sjøreise. <!-- KFM: Link to scenario --> |
| Delete | Slett den gjeldende sjøreisen. Bare sjøreiser som har statusen *Bekreftet*, kan slettes. Etter at en sjøreise forlater havnen og behandler varer i transitt, kan den ikke lenger slettes. |
| Sjøreiseredigering | Åpne siden **Redigeringsprogram for sjøreise**, der du kan legge til eller fjerne innkjøpslinjer for sjøreisen, opprette nye containere og endre detaljer om selve sjøreisen. |
| Sjøreisekostnader | Åpne siden **Sjøreisekostnader**, der du kan vise og legge til reisekostnader for alle varene i sjøreisen. Når reisekostnader legges til sjøreisen manuelt, legges de automatisk til på siden **Kostnadsforespørsel** og fordeles på hver vare i henhold til metoden som er angitt på siden **Sjøreisekostnader**. |

### <a name="buttons-on-the-voyage-tab"></a>Knapper i fanen Sjøreise

Tabellen nedenfor beskriver knappene som er tilgjengelige i handlingsruten på siden **Sjøreise**. Denne fanen er bare tilgjengelig når du arbeider i listevisningen på siden **Alle sjøreiser**.

| Knapp | beskrivelse |
|---|---|
| Fraktcontainer | Åpne en side som viser alle forsendelsescontainerne som er tilknyttet den valgte sjøreisen. Det kan være én container eller mange containere. |
| Folio | Åpne en side som viser alle folioene som er tilknyttet den valgte sjøreisen. Det kan være én folio eller mange folioer. |

### <a name="buttons-on-the-manage-tab"></a>Knapper i fanen Administrer

Tabellen nedenfor beskriver handlingene som er tilgjengelige i handlingsruten på siden **Administrer**.

| Knapp | beskrivelse |
|---|---|
| Dokumenter mottatt | Oppdater sjøreisen slik at alternativet **Dokumenter mottatt** er satt til *Ja*. Du kan bruke denne knappen til å låse varen og/eller innkjøpslinjen slik at den ikke kan oppdateres ytterligere. |
| I transitt | Oppdater feltet **Sjøreisestatus** til statusen I transitt som er fastsatt på siden **[Parametere for netto innkjøpspris](landed-cost-parameters.md)**. Det er ingen ytterligere logikk i denne prosessen. En sjøreise kan også oppdateres automatisk til statusen I transitt basert på innstillingene i [sporingskontrollsenteret](delivery-information-setup.md).
| Klar for etterkalkulering | Oppdater feltet **Sjøreisestatus** til statusen Klar for etterkalkulering som er fastsatt på siden **[Parametere for netto innkjøpspris](landed-cost-parameters.md)**. En sjøreise kan kostnadsføres når alle fakturaene er behandlet (både lagerfakturaer og kostnadsfakturaer) og varene er mottatt. Hvis de estimerte kostnadene som er knyttet til en sjøreise, ikke har blitt kostnadsført, vil det oppstå en feil når du prøver å behandle etterkalkulering av en sjøreise. |
| Kalkulert | Rydd opp i uregelmessigheter ved etterkalkulering etter at det finnes en faktura for alle bestillinger og sjøreisekostnader. Når du velger denne knappen, vises dialogboksen **Sjøreise oppdatert – kostnadsført**. Der kan du velge å postere på standard finansdato eller angi en posteringsdato, og deretter kjøre handlingen. Du kan kjøre handlingen på nytt så mange ganger du vil. Du kan også bruke dialogboksen **Sjøreise oppdatert – kostnadsført** til å opprette en plan for å kjøre handlingen som en periodisk oppgave (satsvis jobb). Det anbefales at du kjører handlingen regelmessig ved å definere den som en satsvis jobb. |
| Poster tilgangsliste | Poster en mottaksliste for alle bestillingslinjer i sjøreisen.  |
| Poster mottaksseddel | Poster en produktkvittering for alle bestillingslinjer i sjøreisen. Produktmottaksprosessen for bestillingslinjene som er knyttet til en sjøreise, vil bare bli brukt hvis varene **ikke** kommer til å gå gjennom behandling av varer i transitt. Hvis varene går gjennom behandlingen av varer i transitt, får du en feilmelding når du prøver å postere produktmottaket for en bestillingslinje.  |
| Poster faktura | Poster en faktura for alle bestillingslinjer i sjøreisen. Hvis varene på sjøreisen går gjennom behandling av varer i transitt, faktureres bestillingslinjene før mottaksprosessen er utført. Når den opprinnelige bestillingen faktureres, opprettes ordrene for varer i transitt som er knyttet til de opprinnelige bestillingslinjene. Disse ordrene kan deretter mottas av lageret.  |
| Send overføringsordre | Poster en sjøreise for overføringsordre for alle overføringsordrelinjer i sjøreisen. Når denne knappen er valgt, er bare overføringsordrer tilgjengelige for oppdatering. |
| Motta overføringsordre | Poster en kvittering for overføringsordre for alle overføringsordrelinjer i sjøreisen. |
| Motta varer i transitt | Motta alle ordrelinjer som er i transit i sjøreisen. Denne knappen er ett av tre alternativer som er tilgjengelige for mottak av varer i transitt for en sjøreise. (De to andre alternativene er knappen **Opprett ankomstjournal**, som beskrives senere i denne tabellen, og mobilappen Lagerstyring.) Dette alternativet er det enkleste alternativet, og det vil behandle varene i transitt ut av transittlageret og til det endelige destinasjonslageret. Hvis du vil ha mer kontroll over prosessen, kan du bruke ankomstjournalen eller en mobilenhet til å behandle mottak av varer. |
| Finn automatiske kostnader | Finn relevante sjøreisekostnader. Hvis disse kostnadene allerede er funnet eller oppdatert, får du følgende melding: Ikke-fakturerte kostnadslinjer finnes. Vil du overskrive dem? Eventuelle kostnader som ikke var knyttet til sjøreisen, blir funnet. Sjøreisekostnader som er knyttet til en sjøreise og som er fakturert, vil ikke bli overskrevet. |
| Opprett ankomstjournal | <p>Åpne dialogboksen **Opprett ankomstjournal** der du kan opprette en ankomstjournal som angir en lokasjon. Dialogboksen inneholder følgende alternativer:</p><ul><li>**Opprett fra varer i transitt** eller **Opprett fra overføringsordre** – Etiketten for dette alternativet endres avhengig av om du bruker varer i transittprosessen. Sett alternativet til *Ja* for å åpne en ankomstjournalside, som lar deg behandle en standard ankomstjournal for varene i transitt som er knyttet til ankomstjournalen. Hvis varen allerede er mottatt i det endelige mållageret, vil den ikke bli lagt til i ankomstjournallinjene.</li><li>**Initialiser antall** – Sett dette alternativet til *Ja* for å initialisere antallet som skal mottas, basert på antallet varer som er angitt på sjøreiselinjen. Hvis sjøreiselinjen er delvis mottatt, vil dette antallet være gjenværende antall. Det anbefales at du setter dette alternativet til *Ja*.</li><li>**Opprett fra ordrelinjer** – Sett dette alternativet til *Ja* for å bruke verdien fra ordrelinjene.</li></ul><p>Denne knappen er ett av tre alternativer som er tilgjengelige for mottak av varer for en sjøreise. (De andre alternativene er knappen **Motta varer i transitt**, som ble beskrevet tidligere i denne tabellen, og mobilappen Lagerstyring.)</p> |
| Avsett kostnader | Du kan avsette kostnader der en kostnadstype har en finanskonto angitt for debet. Denne knappen brukes vanligvis når lageret er i transitt, eller når varene er mottatt og fakturert. |
| Samle kostnader | Flytt kostnader fra forsendelsescontainernivået til sjøreisenivået. Du kan bruke denne knappen i et scenario for delt tjeneste/forsendelses der flere enheter deler en forsendelsescontainer eller kartongplass. Denne har for eksempel en forsendelsescontainer på 12 meter og en forsendelsescontainer på 6 meter, og fordelingen gjøres etter volum. I dette tilfellet kan varene/enhetene som deler eller bruker plassen i forsendelsescontaineren på 20 meter, bli gjenstand for økonomisk straff. Hvis noen organisasjoner skal kunne distribuere kostnadene riktig, kan det hende de vil overføre kostnadene til sjøreisen og distribuere dem på grunnlag av metoden for sjøreisefordelingsnivået. |
| Endre reisemal | Åpne en dialogboks der du kan endre sjøreisemalen. Når du endrer malen, slettes sjøreisekostnadene. Derfor kan det hende du må velge **Søk etter automatiske kostnader** (se beskrivelsen tidligere i denne tabellen) eller legge til kostnader manuelt på nytt. |

### <a name="buttons-on-the-general-tab"></a>Knapper i fanen Generelt

Tabellen nedenfor beskriver knappene som er tilgjengelige i handlingsruten på siden **Generelt**.

| Knapp | beskrivelse |
|---|---|
| Tilgangsliste | Åpne en liste over produktmottak for alle bestillingslinjer i sjøreisen.  Hvis ingen produktmottakslister er behandlet, er ikke denne knappen tilgjengelig. |
| Produktkvittering | Åpne produktmottaksposten for bestillingslinjene som er knyttet til sjøreisen, hvis den posten brukes. Hvis ingen produktmottak er postert, er ikke denne knappen tilgjengelig. Produktmottaksprosessen blir ikke brukt hvis du bruker behandling av varer i transitt. |
| Vareankomst | Åpne vareankomstjournalen, hvis den brukes. |
| Sporing | Åpne siden **Innkommende sporing**, der du kan oppdatere den forventede ankomstdatoen for varer i en forsendelsescontainer og en sjøreise, og deretter oppdatere de forventede leveringsdatoene for bestillingslinjer. |
| Forespørsel om kostnader | <p>Åpne siden **Kostnadsforespørsel**, som viser alle kostnadene for en sjøreise.</p><p>Velg **Visning** i handlingsruten for å justere visningen. Du kan vise et hvilket som helst nivå, pluss vare- og kosttypekoden.</p><p>Bare kosttypekoder som er direkte relatert til lagertransaksjoner, vises på siden **Kostnadsforespørsel**. Ved å fjerne disse kosttypekodene kan du justere siden ved å gruppere kostnader. Denne funksjonen kan være nyttig hvis du bruker størrelser og farger.</p><p>Siden **Konstnadsforespørsel** viser bare kosttypekoder der feltet **Debet** er satt til *Vare*.</p> |
| Varer i transitt-ordrer | Åpne siden **Ordrer for varer i transitt**, som viser postene for varer i transitt bare for den valgte sjøreisen. |

## <a name="lines-view"></a>Visningen Linjer

Hvis du vil åpne visningen **Linjer**, åpner du en sjøreise, og deretter velger du fanen **Linjer** øverst til høyre i sjøreiseoverskriften.

### <a name="information-on-the-voyage-header-fasttab"></a>Informasjon om hurtigfanen Topptekst for sjøreise

Hurtigfanen **Topptekst for sjøreise** i visningen **Linjer** for en sjøreise inneholder grunnleggende informasjon som beskriver sjøreisen. Mange av feltene som vises på denne hurtigfanen, vises også i visningen **Topptekst**, som blir beskrevet senere i denne artikkelen.

### <a name="information-on-the-voyage-lines-fasttab"></a>Informasjon om hurtigfanen Linjer for sjøreise

Hurtigfanen The **Linjer for sjøreise** i visningen **Linjer** for en sjøreise er knyttet til sjøreisedetaljer og etterkalkuleringsinformasjon som gjelder på sjøreisenivået. Her kan du se gjennom forsendelsescontainere, folioer og varer som er knyttet til sjøreisen. Prisen på og antallet av varene for sjøreisen vises også. Du kan vise en forsendelsescontainer eller folio som er oppført, ved å velge den relevante koblingen.

### <a name="information-on-the-line-details-fasttab"></a>Informasjon om hurtigfanen Linjedetaljer

Hurtigfanen **Linjedetaljer** i visningen **Linjer** for en sjøreise formidler mer informasjon om linjen som for øyeblikket er valgt i hurtigfanen **Linjer for sjøreise**. Vær oppmerksom på at denne hurtigfanen inneholder detaljer om posisjonen som hver linje innehar i containeren, og containerens deklarerte antall.

## <a name="header-view"></a>Topptekstvisning

Hvis du vil åpne visningen **Topptekst**, åpner du en sjøreise, og deretter velger du fanen **Topptekst** øverst til høyre i sjøreiseoverskriften.

### <a name="settings-on-the-general-fasttab"></a>Innstillinger i hurtigfanen Generelt

I tabellen nedenfor beskrives feltene som er tilgjengelige i hurtigfanen **Generelt** i visningen **Topptekst** for en sjøreise.

| Felt | beskrivelse |
|---|---|
| Sjøreise | Angi sjøreise- eller flight-nummeret. |
| Bestillingsreferanse | Hvis spedisjons- eller forsendelsessenteret har et referansenummer for å identifisere sjøreisen (det vil si spedisjonssenterets eller forsendelsessenterets interne referanse), angir du det her. |
| Fartøy | Angi eller velg fartøyet. Hvis fartøyet ikke er oppført som en verdi, kan du angi fartøy-ID-en som fritekst. I så fall oppdateres ikke hovedtabellen slik at du kan velge fartøy-ID-en i dette feltet senere. |
| Ekstern sjøreise-ID | Angi den offentlig tilgjengelige ID-en for en sjøreise (for eksempel flight-nummeret). |
| MAWB/fraktbrev | Angi flyfraktnummeret eller fraktbrevnummeret. Du kan angi denne verdien når du sender med fly. |
| HAWB/fraktbrev | Angi flyfraktbrevet eller fraktbrevet til forsendelsescontaineren. |
| Utleie | Merk av i denne avmerkingsboksen for å angi at containeren er en leiecontainer som må returneres. |
| beskrivelse | Angi en beskrivelse av sjøreisen for å gjøre det enklere å gjenkjenne den. |
| Sjøreisestatus | Statusen for sjøreisen. Verdiene inkluderer *Opprettet*, *I transitt*, *Dokumenter mottatt* og *Kostnadsført*. Dette feltet blir ikke beregnet basert på logikk. Det oppdateres bare via posteringshandlingen. Verdien *Kostnadsført* angir at en faktura for lageret og alle sjøreisekostnadene er mottatt. Med mindre en faktura mottas, kan ikke en sjøreise ha statusen *Kostnadsført*. |
| Bestillingsstatus | Den høyeste statusen som er nådd blant alle bestillingene som er knyttet til sjøreisen. |
| Dokumenter mottatt | En verdi som angir om firmaet har mottatt alle dokumentene som er knyttet til sjøreisen. Hvis du vil endre verdien, velger du **Dokumenter mottatt** i gruppen **Oppdatering av sjøreise** i fanen **Administrer** i handlingsruten. |
| Forsendelsesfirma | Velg forsendelsesfirmaet for denne sjøreisen. Dette feltet kan brukes til å fastslå automatiske kostnader. |
| Navn | Navnet på firmaet som er valgt i feltet **Forsendelsesfirma**. |
| Mål | Ved hjelp av dette feltet kan det angis et mål i en automatisk kostnad. Mål brukes ofte av organisasjoner som ikke kjenner til det enkelte volumet eller vekten av varene, men som krever en mer nøyaktig fordeling enn alternativene Beløp eller Antall leverandører. Fraktspeditøren vil formidle vekten eller kubikkmålet, og du kan plassere den på nivå med en vare eller bestillingen. Det kan oppdateres automatisk hvis parameteren er valgt, eller det kan angis manuelt. |
| Måleenhet | Måleenheten som gjelder for tallet i feltet **Mål**. |
| Antall paller | Angi antall paller på sjøreiselinjen. Dette feltet oppdateres automatisk hvis alternativet **Oppdater antallet kartonger automatisk** er satt til *Ja* i fanen **Generelt** på siden **Netto innkjøpspris**. |

### <a name="settings-on-the-delivery-fasttab"></a>Innstillinger i hurtigfanen Levering

I tabellen nedenfor beskrives feltene som er tilgjengelige i hurtigfanen **Levering** i visningen **Topptekst** for en sjøreise.

| Felt | beskrivelse |
|---|---|
| Opprettingsdato og -klokkeslett | Datoen og klokkeslettet da sjøreiseposten ble opprettet. |
| Dato for ab fabrikk | Dette feltet velger den tidligste datoen for fabrikkutskipning blant bestillingene som er koblet til sjøreisen. Fabrikkutskipningsdatoen er tilgjengelig på bestillingshodet, og den oppdateres ved hjelp av sporingskontrollfunksjonen. |
| Forsendelsesdato | Den anslåtte datoen da flyet eller fartøyet forlater opprinnelsesstedet. |
| Avreisedato | Avgangsdatoen er vanligvis datoen da flyet eller fartøyet faktisk forlater havnen i utlandet. Forsendelsesdatoen og avgangsdatoen trenger ikke samsvare. Feltet **Avgangsdato** er bare til informasjon. Det vil ikke bli brukt til å estimere den forventede leveringsdatoen. Sporingskontrollfunksjonen brukes til å estimere den forventede leveringsdatoen, og dette feltet kan settes opp slik at det automatisk fylles ut av sporingskontrollfunksjonen. |
| Til butikk-dato | Dette feltet velger den tidligste datoen da varene fra bestillingene som er koblet til forretningsforbindelsen, vil være tilgjengelige for salg. |
| Estimert leveringsdato | Den estimerte leveringsdatoen er vanligvis datoen da varene skal ankomme lageret. Dette feltet er bare beregnet til informasjon. Det brukes ikke til hovedplanlegging for varer. Den forventede leveringsdatoen på bestillingslinjen brukes til hovedplanlegging for varer på en sjøreise, og den oppdateres ved hjelp av sporingskontrollfunksjonen. Dette feltet kan settes opp slik at det fylles ut av sporingskontrollfunksjonen. |
| Faktisk leveringsdato | Den tidligste leveringsdatoen, basert på varene som er koblet til sjøreisen. |
| Beregnet ankomst ved forsendelseshavn | Angi datoen da du forventer at sjøreisen ankommer forsendelseshavnen, basert på informasjonen som ble oppgitt av transportøren. |
| Opprinnelige dokumenter mottatt | Angi datoen da de opprinnelige dokumentene ble mottatt. |
| Megler informert | Angi datoen da mekleren ble rådført. |
| Opprinnelig fraktbrev sendt | Angi datoen da det opprinnelige fraktbrevet ble sendt. |
| Varer frigitt | Angi datoen da varene ble frigitt fra tollen. |
| Kundeavtale | Angi kundeavtaledatoen, som er datoen da du forventer at kunden skal ta eierskap av varene. |
| Levert ved lager | Angi datoen da varene ble levert til lageret. |
| Bekreftelsesdato | Angi verifiseringsdatoen. |
| Leveringsinstruksjoner | Angi datoen da leveringsinstruksjonene ble mottatt. |
| Leveringsmiddel | Dette feltet formidler informasjon om metoden som brukes til å levere sjøreisen og kostnadsvalget for automatiske kostnader som er knyttet til den leveringsmåten. |
| Fra-havn | Forsendelseshavnen som sjøreisen starter fra. |
| Til-havn | Forsendelseshavnen der sjøreisen ankommer. Forsendelsescontainerne kan ha ulike havner, fordi skipet kanskje stopper ved flere havner. Hvis du kontrollerer "til"-havnen på forsendelsescontainernivå, formidler du nøyaktige havndetaljer for hver forsendelsescontainer i en sjøreise. Den automatiske kostnaden som er knyttet til frakten, fastslås på grunnlag av kombinasjonen av forsendelsescontainertypen, til-havnen og fra-havnen. |
| Lokal videresender | Dette feltet er bare beregnet til informasjon. Den lokale speditøren bør kunne velges fra leverandørtabellen. |
| Dato for lokal transport | Datoen som den lokale transporten er bestilt for. Dette feltet kan hjelpe lageret med planlegging. |
| Klokkeslett for lokal transport | Tidspunktet som den lokale transporten er bestilt for. Dette feltet kan hjelpe lageret med planlegging. |
| Reisemal | Reisemalen som er angitt for sjøreisen. Reisemalen brukes til å angi til-havnen og fra-havnen til forsendelsescontaineren og sjøreisen. Disse verdiene hjelper i sin tur deg med å identifisere de automatiske kostnadene som er knyttet til sjøreisen. |

### <a name="settings-on-the-other-fasttab"></a>Innstillinger i hurtigfanen Annet

I tabellen nedenfor beskrives feltene som er tilgjengelige i hurtigfanen **Annet** i visningen **Topptekst** for en sjøreise.

| Felt | beskrivelse |
|---|---|
| Kommentarer | Angi tilleggsinformasjon som er knyttet til sjøreisen. |
| Verdisettingsdato | Velg den tidligste datoen for fabrikkutskipning for bestillingene som er koblet til sjøreisen. |
| Ventende sjøreise | Du kan bruke dette til å angi om forsendelsen eller sjøreisen har startet. Den er bare til informasjon.  |
| Gi nytt navn til forsendelsescontainere | Antall containere som ennå ikke er mottatt, for sjøreiser som har mer enn én container. |

## <a name="voyage-update-periodic-tasks"></a>Oppdaterer periodiske oppgaver for sjøreise

Modulen **Netto innkjøpspris** inkluderer flere sjøreiserelaterte periodiske oppgaver som kan masseoppdatere flere aspekter av sjøreisen. Hvis du vil kjøre eller planlegge disse periodiske oppgavene, kan du gå til **Netto innkjøpspris \> Periodiske oppgaver \> Sjøreiseoppdateringer**, og deretter velger du én av følgende oppgavetyper:

- **Mottatte dokumenter** – Med denne oppgaven kan du sette **Dokumenter mottatt** til *Ja* for flere sjøreiser samtidig. Bruk innstillingene for **Filter** til å definere settet med sjøreiser du vil oppdatere.
- **I transitt** – Med denne oppgaven kan du sette feltet **Sjøreisestatus** til statusen I transitt som er etablert på siden **[Parametere for netto innkjøpspris](landed-cost-parameters.md)** for flere sjøreiser samtidig. Bruk innstillingene for **Filter** til å definere settet med sjøreiser du vil oppdatere.
- **Klar til etterkalkulering** – Med denne oppgaven kan du sette feltet **Sjøreisestatus** til statusen Klar til etterkalkulering som er etablert på siden **[Parametere for netto innkjøpspris](landed-cost-parameters.md)** for flere sjøreiser samtidig. Du vil vanligvis sette opp denne oppgaven til å kjøre med jevne mellomrom.
- **Etterkalkulert** – Med denne oppgaven kan du sette feltet **Sjøreisestatus** til statusen Etterkalkulert som er etablert på siden **[Parametere for netto innkjøpspris](landed-cost-parameters.md)** for flere sjøreiser samtidig, forutsatt at de er kostnadsført, men ikke har blitt oppdatert i sjøreisen. Du vil vanligvis sette opp denne oppgaven til å kjøre med jevne mellomrom.
