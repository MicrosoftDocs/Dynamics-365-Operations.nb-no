---
title: Administrere folioer
description: Dette emnet beskriver hvordan du arbeider med folioer. En folio består vanligvis av én leverandørs varer for én enhet eller et firma per forsendelse. Varene i en folio kan være i én container, eller de kan være spredt på flere containere.
author: sherry-zheng
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMFolioTable, ITMFolioTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: d414ed7ac55afbbc58b8f5542c713f56392f9bc7
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570457"
---
# <a name="manage-folios"></a>Administrere folioer

[!include [banner](../../includes/banner.md)]

En folio blir ofte fastsatt av tollbestemmelser. Den kan bestå av én leverandørs varer for én enhet eller et firma per forsendelse. Varene i en folio administreres i én beholder.

Hvis du vil åpne siden **Alle folioer**, går du til **Netto innkjøpspris \> Folioer \> Alle folioer**. Denne siden viser en liste over alle folioer. Du kan bruke knappene i handlingsruten til å opprette, slette og arbeide med folioer. Velg en hvilken som helst folio i listen for å vise detaljer om den på siden **Folioer**.

## <a name="action-pane"></a>Handlingsrute

Handlingsruten på sidene **Alle folioer** og **Folioer** inneholder knapper du kan bruke til å arbeide med en folio. Hver knapp utfører én handling. Handlingsruten inneholder også faner, der hver av dem igjen inneholder et sett med relaterte knapper. Med unntak av der det er bemerket, er alle knapper og faner som er beskrevet i følgende underdeler, tilgjengelige både i listevisningen (det vil si på siden **Alle folioer**) og i den detaljerte visningen (det vil si på siden **Folioer**).

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Knapper som vises direkte i handlingsruten

Tabellen nedenfor beskriver knappene som er tilgjengelige i handlingsruten.

| Knapp | beskrivelse |
|---|---|
| Nye | Opprette en folio. |
| Delete | Slett den åpne eller valgte folioen. |
| Sjøreisekostnader | Åpne siden **Sjøreisekostnader**, der du kan vise og legge til kostnader på folionivå for alle varene i sjøreisen. Når kostnader legges til sjøreisen manuelt, legges de automatisk til kostforespørslersiden og fordeles på hver vare i henhold til metoden som er angitt på siden **Sjøreisekostnader**. |

### <a name="buttons-on-the-manage-tab"></a>Knapper i fanen Administrer

Tabellen nedenfor beskriver knappene som er tilgjengelige i handlingsruten på siden **Administrer**.

| Knapp | beskrivelse |
|---|---|
| Poster tilgangsliste | Poster en mottaksliste for alle bestillingslinjer i folioen. Hvis det brukes flere firmaforsendelser, åpnes det en ny posteringsdialogboks for mottaksliste for hvert firma. |
| Poster mottaksseddel | Poster en produktkvittering for alle bestillingslinjer i folioen. Hvis det brukes flere sjøreiser, åpnes det en ny dialogboks for produktkvitteringspostering for hvert firma. |
| Poster faktura | Poster en faktura for alle bestillingslinjer i folioen. Hvis det brukes flere sjøreiser, åpnes det en ny dialogboks for fakturapostering for hvert firma. |
| Send overføringsordre | Poster en overføringsordre for alle overføringsordrelinjer som er relatert til gjeldende overføringsordre i den tilknyttede forsendelsen. |
| Motta overføringsordre | Poster en kvittering for overføringsordre for alle overføringsordrelinjer som er relatert til gjeldende overføringsordre i den tilknyttede forsendelsen. |
| Motta varer i transitt | Motta alle ordrelinjer som er i transit i folioen. |
| Dokumenter mottatt | Oppdater verdien for innstillingen for alternativet **Dokumenter mottatt** til *Ja*. Du kan bruke denne knappen til å låse varen og/eller innkjøpslinjen slik at den ikke kan oppdateres ytterligere. |
| Finn automatiske kostnader | Finn relevante sjøreisekostnader. Hvis disse kostnadene allerede er funnet eller oppdatert, får du følgende melding: Ikke-fakturerte kostnadslinjer finnes. Vil du overskrive dem? Legg merke til at sjøreisekostnader som er knyttet til foliioen og som er fakturert, ikke vil bli overskrevet. |
| Opprett ankomstjournal | Generer en ankomstjournal for organisasjoner ved hjelp av avanserte lagerfunksjoner. Du kan velge **Initialiser antall** (anbefales), **Opprett fra varer i transitt** og/eller **Opprett fra bestillinger**. Det siste alternativet avhenger av om behandling av varer i transitt brukes. |
| Avsett kostnader | Avsett kostnader der en kostnadstype har en finanskonto angitt for debet. Denne knappen brukes vanligvis når lageret er i transitt, eller når varene er mottatt og fakturert. |

### <a name="buttons-on-the-general-tab"></a>Knapper i fanen Generelt

Tabellen nedenfor beskriver knappene som er tilgjengelige i handlingsruten på siden **Generelt**.

| Knapp | beskrivelse |
|---|---|
| Tilgangsliste | Poster en mottaksliste for alle bestillingslinjer i folioen. Hvis det brukes flere sjøreiser, åpnes det en ny dialogboks for mottakslistepostering for hvert firma. |
| Produktkvittering | Vis produktmottaksposten, hvis den brukes. |
| Vareankomst | Vis vareankomstjournalen, hvis den brukes. |
| Forespørsel om kostnader | Åpne kostnadsforespørselssiden for å vise alle kostnadene til en sjøreise, inkludert forsendelsescontaineren, folioen og bestillingen. Du kan endre den nøyaktige visningen av siden ved hjelp av handlingen Vis. På kostnadsforespørselssiden kan du vise alle områdene, pluss vare- og kosttypekoden. Ved å fjerne disse varene kan du justere siden ved å gruppere sammen kostnader. Denne funksjonen kan være nyttig hvis du bruker størrelser og farger. Du kan endre dimensjonene som vises på siden. Siden **Kostnader** viser bare kosttypekoder der oppføringen **Dr** i fanen **Postering** er satt til *Vare*. |

## <a name="header-view"></a>Topptekstvisning

Hvis du vil åpne visningen **Topptekst**, åpner du en folio, og deretter velger du fanen **Topptekst** øverst til høyre i foliooverskriften.

### <a name="settings-on-the-general-fasttab"></a>Innstillinger i hurtigfanen Generelt

I tabellen nedenfor beskrives feltene som er tilgjengelige i hurtigfanen **Generelt** i visningen **Topptekst** for en folio.

| Felt | beskrivelse |
|---|---|
| Folio | Navnet på folioen. Dette navnet genereres automatisk når folioen opprettes.|
| Sjøreise | Sjøreisen som er knyttet til folioen. |
| Tollmegler | Velg tollmekleren for folioen. Tollmeklere er definert for leverandøren. De sørger for at opprettede kostnader kan fastslås automatisk. |
| HAWB/fraktbrev | Angi flyfraktseddelen eller fraktbrevet som gjelder for folioen. |
| Bedrift | Den juridiske enheten (firmaet) som er knyttet til folioen. |
| Godskontrollnummer | Dette feltet brukes av tollavdelinger i noen land eller regioner. |
| Mål | Ved hjelp av dette feltet kan det angis et mål i modulen **Netto innkjøpspris**. Mål brukes ofte av organisasjoner som ikke kjenner til det enkelte volumet eller vekten av varer, men som krever en mer nøyaktig fordeling enn alternativene Beløp eller Antall leverandører. Fraktspeditøren vil formidle vekten eller kubikkmålet, og du kan plassere den på nivå med en vare eller bestillingen. Det kan oppdateres automatisk hvis parameteren er valgt eller angitt manuelt. |
| Måleenhet | Enheten som gjelder for det angitte målet. |
| Antall kartonger | Antall kartonger i folioen. Dette feltet kan oppdateres automatisk, avhengig av parametervalget. |
| Leverandørnummer | Velg leverandøren som er knyttet til folioen. Dette feltet er bare beregnet til informasjon. Den påvirker ingen funksjonalitet. |
| Navn | Navnet på den valgte leverandørkontoen. |
| Kommentarer | Angi tilleggsinformasjon som er knyttet til folioen. |
| Beskrivelse av varer | Velg en varebeskrivelse som kan hjelpe deg med å identifisere folioen. Hvis du vil ha mer informasjon, kan du se [Beskrivelse av varer](shipping-information-setup.md#description-of-goods). |
| Verdisettingsdato | Dette feltet er knyttet til tolloppføringssiden. Modulen **Netto innkjøpspris** vil bruke tollkursen for datoen du angir her. Standardverdien er datoen på tolloppføringssiden. |
| Toll-ID | Angi toll-ID-en. Tollavdelingene i land eller regioner oppgir denne ID-en. |
| Tariffkode | Angi en tariffkode som skal knyttes til folioen. Denne koden er vanligvis obligatorisk (og definert) av landet eller regionen du sender til. |

### <a name="settings-on-the-delivery-fasttab"></a>Innstillinger i hurtigfanen Levering

I tabellen nedenfor beskrives innstillingene som er tilgjengelige i hurtigfanen **Levering** i visningen **Topptekst** for en folio.

| Felt | beskrivelse |
|---|---|
| Foliodato | Velg en dato du vil knytte til folioen. Standardverdien er opprettingsdatoen for sjøreisen. |
| Beregnet ankomst ved forsendelseshavn | Estimert ankomsttid (ETA) ved målhavnet ("til"-havn). |
| Estimert leveringsdato | Vanligvis er dette datoen da varene skal ankomme til lageret. Dette feltet brukes ikke når den estimerte leveringsdatoen beregnes. (Forventet leveringsdato for sporingskontroll brukes i stedet.) Hvis du vil angi dette feltet slik at verdien samsvarer med anslått leveringsdato for sporingskontroll, bruker du [sporingskontrollsenteret](delivery-information-setup.md#tracking-control-center). |
| Opprinnelige dokumenter mottatt | Datoen da de opprinnelige dokumentene ble mottatt. |
| Megler informert | Datoen da mekleren ble rådført. |
| Opprinnelig fraktbrev sendt | Datoen da det opprinnelige fraktbrevet ble sendt. |
| Varer frigitt | Datoen da varer ble frigitt. |
| Kundeavtale | Datoen for kundeavtalen. |
| Levert ved lager | Datoen da varer ble levert til lageret. |
| Bekreftelsesdato | Kontrolldatoen. |
| Leveringsinstruksjoner | Datoen da leveringsinstruksjonene ble mottatt. |
| Fra-havn | Havnen som sjøreisen starter fra. |
| Til-havn | Havnen der sjøreisen ankommer. Forsendelsescontaineren kan ha en annen havn, fordi skipet kan stoppe ved flere havner. |

### <a name="settings-on-the-export-fasttab"></a>Innstillinger i hurtigfanen Eksport

I tabellen nedenfor beskrives innstillingene som er tilgjengelige i hurtigfanen **Eksport** i visningen **Topptekst** for en folio.

| Felt | beskrivelse |
|---|---|
| Eksportør | Eksportøren kan lagres i folioen. I internasjonal handel kan du sende en bestilling til ett selskap, men motta varene fra et annet firma. Sporing og dokumentasjon kreves av tollmyndighetene. Navnet og adressen til eksportøren kan lagres her. |
| Navn | Navnet på den valgte eksportøren. |

## <a name="lines-view"></a>Visningen Linjer

Hvis du vil åpne visningen **Linjer**, åpner du en folio, og deretter velger du fanen **Linjer** øverst til høyre i foliooverskriften.

### <a name="information-on-the-folio-fasttab"></a>Informasjon om hurtigfanen Folio

Hurtigfanen **Folio** i visningen **Linjer** viser informasjon om folioen. Mesteparten av denne informasjonen vises også i visningen **Topptekst**, som beskrevet tidligere i dette emnet.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Informasjon og knapper i hurtigfanen Linjer

Hurtigfanen **Linjer** i visningen **Linjer** viser detaljer om alle fullstendige eller delvise bestillingslinjer som er inkludert i gjeldende folio.

Følgende tabell beskriver knappene som er tilgjengelige i hurtigfanen **Linjer** i visningen **Linjer**.

| Knapp | beskrivelse |
|---|---|
| Fjern | Fjern den valgte bestillingslinjen fra sjøreisen. |
| Lager \> Transaksjoner | Vis lagertransaksjoner for den valgte bestillingslinjen. Vær oppmerlsom på at dersom du bruker varer i transitt, vises også den opprinnelige ordren og ordrene for varer i transitt. |
| Lager \> Visningsdimensjoner | Åpne en dialogboks der du kan velge lagerdimensjonene som vises for transaksjonene du viser. |
| Forny | Oppdater informasjon som er knyttet til linjebeløpet, vekten eller volumet for den valgte bestillingslinjen. |

### <a name="information-on-the-lines-details-fasttab"></a>Informasjon i hurtigfanen Linjedetaljer

Hurtigfanen **Linjedetaljer** i visningen **Linjer** viser detaljer om bestillingslinjen som for øyeblikket er valgt i hurtigfanen **Linjer**.
