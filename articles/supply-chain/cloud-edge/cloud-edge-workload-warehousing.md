---
title: Arbeidsbelastninger for lagerstyring for sky- og kantskalaenheter
description: Dette emnet inneholder informasjon om funksjonen som gjør det mulig å kjøre valgte prosesser fra arbeidsbelastningen for lagerstyring.
author: perlynne
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers, SysWorkloadDuplicateRecord
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 081b6968575a8a057903d96de2833a98552ed123
ms.sourcegitcommit: a46f0bf9f58f559bbb2fa3d713ad86875770ed59
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/15/2021
ms.locfileid: "7813732"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Skalaenheter for sky og kant for arbeidsbelastninger for lagerstyring

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Ikke all forretningsfunksjonalitet for lagerstyring støttes fullt ut for lagre som kjører en arbeidsbelastning på en skalaenhet. Pass på at du bare bruker prosessene som dette emnet beskriver som støttet.

## <a name="warehouse-execution-on-scale-units"></a>Lagerkjøring på skalaenheter

Ved hjelp av lagerstyringsarbeidsbelastninger kan sky- og kantskaleringsenheter kjøre valgte prosesser fra lagerstyringsfunksjonene.

## <a name="prerequisites"></a>Forutsetninger

Du må ha et Dynamics 365 Supply Chain Management-senter og en skalaenhet som er distribuert med arbeidsbelastningen for lagerstyring. Hvis du vil ha mer informasjon om arkitektur og distribusjonsprosessen, kan du se [Vektenheter i en distribuert hybridtopologi](cloud-edge-landing-page.md).

## <a name="how-the-warehouse-execution-workload-works-on-scale-units"></a>Hvordan lagerkjøringsbelastninger fungerer på skalaenheter

For prosessene i arbeidsbelastningen for lagerstyring synkroniseres dataene mellom senteret og skalaenhetene.

En skalaenhet kan bare opprettholde dataene den eier. Dataeierskapskonseptet for skalaenheter bidrar til å forhindre multimaster-konflikter. Det er derfor viktig at du forstår hvilke prosessdata som eies av senteret, og hvilke som eies av skalaenhetene.

Avhengig av forretningsprosessene kan den samme dataposten endre eierskap mellom senteret og skaleringsenhetene. Det finnes et eksempel på dette scenariet i følgende del.

> [!IMPORTANT]
> Det kan opprettes data både på senteret og skalaenheten. Eksempler inkluderer **Nummerskilt** og **Partinumre**. Dedikert konflikthåndtering angis i tilfelle et scenario der den samme unike posten blir opprettet for både senteret og skaleringsenheten under samme synkroniseringssyklus. Når dette skjer, vil neste synkronisering mislykkes, og du må gå til **Systemadministrasjon > Forespørsler > Arbeidsmengdeforespørsler > Dupliserte poster**, der du kan vise og flette dataene.

## <a name="outbound-process-flow"></a>Utgående prosessflyt

Prosessen for utgående dataeierskap avhenger av om du bruker prosessen for lastplanlegging. I alle tilfeller eier senteret *kildedokumentene*, for eksempel salgsordrer og overføringsordrer, i tillegg til ordrefordelingsprosessen og de tilknyttede ordretransaksjonsdataene. Men når du bruker prosessen for lastplanlegging, vil belastningen bli opprettet på senteret og eies derfor i utgangspunktet av senteret. Som en del av *Frigi til lager*-prosessen blir eierskap av belastningsdataene overført til den dedikerte skalaenhetsdistribusjonen, som blir eier av den etterfølgende *forsendelsesbølgebehandlingen* (som arbeidstildeling, etterfyllingsarbeid og opprettelse av etterspørsel). Lagerarbeidere kan derfor bare behandle utgående salgs- og overføringsordrearbeid ved hjelp av en Warehouse Management-mobilapp som er koblet til distribusjonen som kjører den bestemte skalaenhetsarbeidsmengde.

Så snart den endelige arbeidsprosessen har plassert lageret på et endelig forsendelsessted (Rampedør), sender skaleringsenheten signaler om at kildedokumentets lagertransaksjoner skal oppdateres til *Plukket*. Før denne prosessen kjøres og blir synkronisert tilbake, blir lagerbeholdningen på skalaenhetsbelastningen fysisk reservert på lagernivå, og du kan umiddelbart behandle den utgående forsendelsesbekreftelsen uten å vente på at denne synkroniseringen skal fullføres. Den påfølgende forsendelsen av salgsfølgeseddelen og faktureringen eller overføringsordren for belastningen vil bli håndtert i forsendelsen.

Diagrammet nedenfor viser den utgående flyten, og angir hvor de individuelle forretningsprosessene finner sted. (Velg diagrammet for å forstørre det.)

[![Utgående prosessflyt.](media/wes_outbound_warehouse_processes-small.png "Utgående prosessflyt")](media/wes_outbound_warehouse_processes.png)

### <a name="outbound-processing-with-load-planning"></a>Utgående behandling med lastplanlegging

Når du bruker lastplanleggingsprosessen, opprettes det belastninger og forsendelser på senteret, og eierskapet av dataene overføres til skaleringsenhetene som en del av *Frigi til lager*-prosessen, slik det illustreres i følgende figur.

![Utgående behandling med lastplanlegging.](./media/wes_outbound_processing_with_load_planning.png "Utgående behandling med lastplanlegging")

### <a name="outbound-processing-without-load-planning"></a>Utgående behandling uten lastplanlegging

Når du ikke bruker lastplanleggingsprosessen, opprettes det forsendelser på skaleringsenhetene. Belastninger opprettes også på skaleringsenhetene som en del av bølgeprosessen.

![Utgående behandling uten lastplanlegging.](./media/wes_outbound_processing_without_load_planning.png "Utgående behandling uten lastplanlegging")

## <a name="inbound-process-flow"></a>Inngående prosessflyt

Senteret eier følgende data:

- Alle kildedokumenter, for eksempel bestillinger og produksjonsordrer
- Innkommende lastbehandling
- Alle oppdateringer for kostnad og økonomi

> [!NOTE]
> Den inngående bestillingsflyten er konseptuelt forskjellig fra den utgående flyten. Du kan styre det samme lageret på skalaenheten eller i senteret, avhengig av om bestillingen er frigitt til lageret. Når du har frigitt en ordre til lageret, kan du bare arbeide med ordren mens du er logget på skalaenheten.
>
> Hvis du bruker prosessen *Frigi til lager*, opprettes [*lagerordrer*](cloud-edge-warehouse-order.md), og eierskap av den relaterte mottaksflyten tilordnes til skalaenheten. Senteret vil ikke kunne registrere innkommende mottak.

Du må logge på senteret for å bruke prosessen *Frigi til lager*. For bestillingsbehandling går du til en av følgende sider for å kjøre eller planlegge den:

- **Innkjøp og leverandører > Bestillinger > Alle bestillinger > Lager > Handlinger > Frigi til lager**
- **Lagerstyring > Frigi til lager > Automatisk frigivelse av bestillinger**

Når du bruker **Automatisk frigivelse av bestillinger**, kan du velge bestemte bestillingslinjer basert på en spørring. Et typisk scenario vil være å sette opp en gjentakende satsvis jobb som frigir alle bekreftede bestillingslinjer som forventes å ankomme neste dag.

Arbeideren kan kjøre mottaksprosessen ved å bruke en Lagerstyring-mobilapp som er knyttet til skalaenheten. Dataene registreres deretter av skalaenheten, og de rapporteres mot den inngående lagerordren. Oppretting og behandling av etterfølgende plassering vil også bli behandlet av skalaenheten.

Hvis du ikke bruker prosessen *frigivelsen til lager*, og dermed ikke bruker *lagerordrer*, kan senteret behandle lagermottak og arbeidsbehandling uavhengig av skalaenheter.

![Inngående prosessflyt.](./media/wes-inbound-ga.png "Inngående prosessflyt")

Når en arbeider gjør innkommende registrering ved hjelp av en Warehouse Management-mobilapp-mottaksprosess mot skaleringsenheten, registreres et mottak mot den relaterte lagerordren, som er lagret på skaleringsenheten. Skaleringsenhetens arbeidsmengde vil deretter signalisere senteret om å oppdatere de relaterte bestillingslinjetransaksjonene til *Registrert*. Så snart dette er fullført, kan du kjøre en produktkvittering for bestilling i senteret.

Diagrammet nedenfor viser den inngående flyten, og angir hvor de individuelle forretningsprosessene finner sted. (Velg diagrammet for å forstørre det.)

[![Innkommende prosessflyt](media/wes_inbound_warehouse_processes-small.png "Innkommende prosessflyt")](media/wes_inbound_warehouse_processes.png)

## <a name="supported-processes-and-roles"></a>Prosesser og roller som støttes

Ikke alle lagerstyringsprosesser støttes i en lagerkjøringsbelastning på en skalaenhet. Derfor anbefaler vi at du tilordner roller som samsvarer med funksjonaliteten som er tilgjengelig for hver bruker.

For å støtte denne prosessen er en eksempelrolle som heter *Lagerstyring på arbeidsbelastning* inkludert i demonstrasjonsdataene under **Systemadministrasjon \> Sikkerhet \> Sikkerhetskonfigurasjon**. Formålet med denne rollen er å gjøre det mulig for lagerledere å få tilgang til lagerkjøringsbelastningen på skalaenheten. Rollen gir tilgang til sidene som er relevante i sammenheng med en arbeidsbelastning som driftes på en skalaenhet.

Brukerroller på en skalaenhet tilordnes som en del av den opprinnelige datasynkroniseringen fra senteret til skalaenheten.

Hvis du vil endre rollene som er tilordnet til en bruker, går du til **Systemadministrasjon \> Sikkerhet \> Tilordne brukere til roller** på skalaenheten. Brukere som bare fungerer som lagerledere på skalaenheter, bør bare tilordnes rollen *Lagerlederen på arbeidsbelastning*. Denne tilnærmingen vil sikre at disse brukerne bare har tilgang til den støttede funksjonaliteten. Fjern eventuelle andre roller som er tilordnet til disse brukerne.

Brukere som fungerer som lagerledere både på senteret og skalaenheter, bør tilordnes den eksisterende rollen *Lagerarbeider*. Vær oppmerksom på at denne rollen gir lagerarbeidere tilgang til funksjoner (for eksempel behandling av overføringsordremottak) som vises i brukergrensesnittet (UI), men som ikke støttes for skalaenheter.

### <a name="supported-warehouse-execution-processes"></a>Lagerutførelsesprosesser som støttes

Følgende lagerkjøringsprosesser kan aktiveres for en lagerkjøringsbelastning på en skalaenhet:

- Valgte bølgemetoder for salgs- og overføringsordrer (validering, lastopprettelse, tildeling, behovsetterfylling, containerbruk, arbeidsoppretting og bølgeetikettutskrift)

- Behandle lagerarbeid for salgs- og overføringsordre ved hjelp av lagerappen (inkludert etterfyllingsarbeid)
- Foreta spørringer i lagerbeholdningen ved hjelp av lagerappen
- Opprette og kjøre lagerbevegelser ved hjelp av lagerappen
- Opprette og behandle syklustellingsarbeid ved hjelp av lagerappen
- Foreta lagerjusteringer ved hjelp av lagerappen
- Registrere bestillinger og utføre plasseringsarbeid ved hjelp av lagerappen

Følgende typer arbeid kan opprettes på en skalaenhet, og kan derfor behandles som en del av en lagerstyringsarbeidsmengde:

- **Lagerbevegelser** – manuell flytting og flytting etter malarbeid.
- **Syklusopptelling** – inkluderer en godkjennings-/avslagsprosess for avvik som del av opptellingsoperasjoner.
- **Bestillinger** – plasseringsarbeid via en lagerordre når bestillinger ikke er knyttet til laster.
- **Salgsordrer** – enkel plukking og lasting.
- **Utstedelse for overføring** – Enkel plukking og lasting.
- **Etterfylling** – ikke inkludert råvarer for produksjon.
- **Plasser ferdigvarer** – Etter ferdigmeldingsproduksjonsprosessen.
- **Koprodukt og plasser koprodukt** – Etter ferdigmeldingsproduksjonsprosessen.

Ingen andre typer behandling eller lagerarbeid for kildedokumenter støttes for øyeblikket på skalaenheter. For en lagerkjøringsbelastning på en skalaenhet kan du for eksempel ikke foreta et overføringsordremottak (overføringsmottak), og i stedet må dette behandles av senterforekomsten.

> [!NOTE]
> Menyelementer og knapper på mobilenheter for funksjoner som ikke støttes, vises ikke i _mobilappen Lagerstyring_ når den er koblet til en skalaenhetsdistribusjon.
> 
> Når du kjører en arbeidsbelastning på en skalaenhet, kan du ikke kjøre prosesser som ikke støttes for dette bestemte lageret, i senteret. Tabellene som vises senere i dette emnet, dokumenterer funksjonene som støttes.
>
> Valgte lagerarbeidstyper kan opprettes både i senteret og på skalaenheter, men kan bare vedlikeholdes av eiersenteret eller -skalaenheten (distribusjonen som opprettet dataene).
>
> Selv når en bestemt prosess støttes av skalaenheten, må du være oppmerksom på at alle nødvendige data kanskje ikke blir synkronisert fra senteret til skalaenheten eller fra skalaenheten til senteret, som kan føre til uventet systembehandling. Eksempler på dette scenariet er:
> 
> - Hvis du bruker en spørring i et lokasjonsdirektiv som kobler sammen en datatabellpost som bare finnes i senterdistribusjonen.
> - Hvis du bruker lokasjonsstatus og/eller lokasjonsvolumetriske lastefunksjoner. Disse dataene blir ikke synkronisert mellom distribusjonene og fungerer derfor bare når lagerbeholdning for lokasjon oppdateres for en av distribusjonene.

Følgende lagerstyringsfunksjonalitet støttes ikke for øyeblikket for arbeidsbelastninger for skalaenheter:

- Inngående behandling av bestillingslinjer som er tilordnet til en last.
- Inngående behandling av bestillinger for et prosjekt.
- Administrere netto innkjøpspris, bruke reiser og spore varer i transitt.
- Inngående og utgående behandling for varer som har den aktive sporingsdimensjonen **Eier** og/eller **Serienummer**.
- Behandling av lager som har en statusverdi for blokkering.
- Endring av en lagerstatus under enhver arbeidsflyttingsprosess.
- Ordreigangsatte fleksible dimensjonsreservasjoner på lagernivå.
- Bruk av funksjonen *Status for lagerlokasjon* (dataene synkroniseres ikke mellom distribusjonene).
- Bruk av funksjonen *Nummerskiltplassering på lokasjon*.
- Bruk av *Produktfiltre* og *Produktfiltergrupper*, inkludert innstillingen **Antallet dager som kreves for at partier kan kombineres**.
- Integrasjon med kvalitetsstyring.
- Behandling med faktisk vekt-varer.
- Behandling med varer som bare er aktivert for transportstyring (TMS).
- Behandling med negativ lagerbeholdning.
- Lagerarbeidsbehandling med forsendelsesmerknader.
- Lagerarbeidsbehandling med materialhåndtering/lagerautomatisering.
- Avbildninger av produktstandarddata (for eksempel i Warehouse Management-mobilappen).
- Datadeling om produkter mellom firmaer.

> [!WARNING]
> Enkelte lagerfunksjoner blir ikke tilgjengelige for lagre som kjører arbeidsbelastninger for lagerstyring på en skalaenhet, og støttes heller ikke i senteret eller i arbeidsbelastningen for skalaenhet.
> 
> Andre funksjoner kan behandles på begge, men krever nøye bruk i enkelte scenarioer, for eksempel når lagerbeholdningen blir oppdatert for det samme lageret både i senteret og på skalaenheten på grunn av den asynkrone oppdateringsprosessen for data.
> 
> Bestemte funksjoner (for eksempel *Blokker arbeid*) som støttes både i senteret og på skalaenheter, støttes bare for eieren av. dataene.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Utgående (støttes bare for salgs- og overføringsordrer)

Følgende tabell viser hvilke utgående funksjoner som støttes, og hvor de støttes, når arbeidsbelastningen for lagerstyring brukes i sky- og kantskalaenheter.

| Behandle                                                      | Hub | Lagerkjøringsbelastning på en skalaehet |
|--------------------------------------------------------------|-----|------------------------------|
| Behandling av kildedokument                                   | Ja | Nei |
| Last- og transportstyringsbehandling                | Ja, men bare lastplanleggingsprosessen. Behandling av transportstyring støttes ikke  | Nei |
| Frigi til lager                                         | Ja | Nei |
| Planlagt direkteoverføring                                        | Nei  | Nei |
| Forsendelseskonsolidering                                       | Ja, når du bruker lastplanlegging | Ja |
| Forsendelsesbølgebehandling                                     | Nei  |Ja, bortsett fra **Lastplanlegging og sortering** |
| Vedlikehold forsendelser for bølge                                  | Nei  | Ja|
| Lagerarbeidsbehandling (inkl. nummerskiltutskrift)        | Nei  | Ja, men bare for de de tidligere nevnte funksjonene som støttes |
| Gruppeplukking                                              | Nei  | Ja|
| Manuell emballasjebehandling, inkludert arbeidsbehandlingen Plukking av containerpakking | Nei <P>En del behandling kan gjøres etter at en innledende plukkeprosess er håndtert av en skalaenhet, men anbefales ikke på grunn av blokkerte operasjoner.</p>  | Nei |
| Fjern container fra gruppe                                  | Nei  | Nei |
| Utgående sorteringsbehandling                                  | Nei  | Nei |
| Utskrift av belastningsrelaterte dokumenter                           | Ja | Ja|
| Fraktbrev og ved generering av forhåndsvarsel for forsendelse                            | Nei  | Ja|
| Forsendelsesbekreftelse                                             | Nei  | Ja|
| Forsendelsesbekreftelse med Bekreft og overfør            | Nei  | Nei |
| Behandling av følgeseddel og fakturering                        | Ja | Nei |
| Plukking med mangler (salgs- og overføringsordrer)                    | Nei  | Ja, uten å fjerne reserveringer for kildedokumenter|
| Overplukking (salgs- og overføringsordrer)                     | Nei  | Ja|
| Endring av arbeidslokasjoner (salgs- og overføringsordrer)         | Nei  | Ja|
| Fullføre arbeid (salgs- og overføringsordrer)                    | Nei  | Ja|
| Skriv ut arbeidsrapport                                            | Ja | Ja|
| Bølgeetikett                                                   | Nei  | Ja|
| Oppdelt arbeid                                                   | Nei  | Ja|
| Arbeidsbehandling – styrt av Transportlasting            | Nei  | Nei |
| Reduser plukket antall                                       | Nei  | Nei |
| Tilbakefør arbeid                                                 | Nei  | Nei |
| Reverser forsendelsesbekreftelse                                | Nei  | Ja|

### <a name="inbound"></a>Innlevering

Følgende tabell viser hvilke inngående funksjoner som støttes, og hvor de støttes, når arbeidsbelastningen for lagerstyring brukes i sky- og kantskalaenheter.

| Behandle                                                          | Hub | Lagerkjøringsbelastning på en skalaehet<BR>*(Varer som er merket «Ja», gjelder bare for lagerordrer)* |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Behandling&nbsp;av&nbsp;kildedokument                             | Ja | Nei |
| Last- og transportstyringsbehandling                    | Ja | Nei |
| Mottak av varer i transitt og landingskostnad                       | Ja | Nei |
| Bekreftelse av inngående forsendelse                                    | Ja | Nei |
| Bestillingsfrigivelse til lager (lagerordrebehandling) | Ja | Nei |
| Annullering av lagerordrelinjer<p>Merk at dette bare støttes når det ikke er foretatt noen registrering mot linjen</p> | Ja | Nei |
| Motta og plassere bestillingsvarer                       | <p>Ja,&nbsp;når&nbsp;det&nbsp;ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | <p>Ja, når en bestilling ikke er en del av en <i>last</i></p> |
| Bestillingslinjen er mottatt og plassert                       | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | <p>Ja, når en bestilling ikke er en del av en <i>last</i></p></p> |
| Mottak og plassering av returordre                              | Ja | Nei |
| Mottak og plassering av kombinerte nummerskilt                       | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Ja |
| Mottak av lastvare                                              | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Mottak og plassering av nummerskilt                             | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Motta og plassere overføringsordrevare                       | Ja | Nei |
| Mottak og plassering av overføringsordrelinje                       | Ja | Nei |
| Avbryt arbeid (inngående)                                            | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | <p>Ja, men bare når det ikke er merket av for alternativet <b>Avregistrer mottak når arbeid avbrytes</b> (på siden <b>Lagerstyringsparametere</b>)</p> |
| Behandling av bestillingsproduktkvittering                        | Ja | Nei |
| Bestilling som mottas med underlevering                      | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Ja, men bare ved å utføre en annulleringsforespørsel fra senteret |
| Bestilling som mottas med overlevering                       | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Ja  |
| Mottak med oppretting av arbeidstypen *Direkteoverføring*                 | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Mottak med oppretting av arbeidstypen *Kvalitetsordre*                  | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Mottak med oppretting av arbeidstypen *Sampling av kvalitetsvare*          | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Mottak med oppretting av arbeidstypen *Kvalitet i kvalitetskontroll*       | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Mottak med oppretting av kvalitetsordre                            | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Arbeidsbehandling – styrt av *Gruppeplassering*                 | Ja | Nei |
| Arbeidsbehandling med *Plukk med mangler*                               | Ja | Nei |
| Nummerskiltlasting                                           | Ja | Ja |

### <a name="warehouse-operations-and-exception-handing"></a>Lageroperasjoner og unntaksbehandling

Følgende tabell viser hvilke funksjoner for lageroperatsjoner og unntaksbehandling som støttes, og hvor de støttes, når arbeidsbelastningen for lagerstyring brukes i sky- og kantskalaenheter.

| Behandle                                            | Hub | Lagerkjøringsbelastning på en skalaehet |
|----------------------------------------------------|-----|------------------------------|
| Nummerskiltforespørsel                              | Ja | Ja                          |
| Vareforespørsel                                       | Ja | Ja                          |
| Lokasjonsforespørsel                                   | Ja | Ja                          |
| Endre lager                                   | Ja | Ja                          |
| Bevegelse                                           | Ja | Ja                          |
| Flytting etter mal                               | Ja | Ja                          |
| Lageroverføring                                 | Ja | Nei                           |
| Opprett overføringsordre fra lagerapp           | Ja | Nei                           |
| Justering (inn/ut)                                | Ja | Ja, men ikke for justeringsscenariet der lagerreservering må fjernes ved hjelp av innstillingen **Fjern reserveringer** i lagerjusteringstypene</p>                           |
| Endring av beholdningsstatus                            | Ja | Nei                           |
| Syklustelling og behandling av tellingsavvik | Ja | Ja                           |
| Skrive ut etikett på nytt (nummerskilteutskrift)             | Ja | Ja                          |
| Nummerskilt-build                                | Ja | Nei                           |
| Nummerskilt – bryt                                | Ja | Nei                           |
| Pakk til nestede nummerskilt                                | Ja | Nei                           |
| Sjåførinnsjekking                                    | Ja | Nei                           |
| Sjåførutsjekking                                   | Ja | Nei                           |
| Endre partidisposisjonskode                      | Ja | Ja                          |
| Vis liste over åpent arbeid                             | Ja | Ja                          |
| Konsolider skiltnummer                         | Ja | Nei                           |
| Behandling av minimums-/maksimumsetterfylling og etterfylling av soneterskel| Ja <p>Det anbefales at du ikke tar med de samme lokasjonene som en del av spørringene</p>| Ja                          |
| Behandling av sporingsetterfylling                  | Ja  | Ja<p>Merk at oppsettet må utføres på skalaenheten</p>                           |
| Blokker og opphev blokkering av arbeid                             | Ja | Ja                          |
| Endre bruker                                        | Ja | Ja                          |
| Endre arbeidspulje i arbeid                           | Ja | Ja                          |
| Avbryt arbeid                                        | Ja | Ja                          |

### <a name="production"></a>Produksjon

Tabellen nedenfor oppsummerer hvilke produksjonsscenarioer med lagerstyring som støttes for øyeblikket i arbeidsbelastninger for skalaenhet.

| Behandle | Hub | Lagerkjøringsbelastning på en skalaehet |
|---------|-----|------------------------------|
| Ferdigmeld og Plasser ferdigvarer | Ja | Ja |
| Plasser koprodukt og biprodukt | Ja | Ja |
| Start produksjonsordre | Ja | Ja |
| <p>Alle andre lagerstyringsprosesser som er knyttet til produksjon, inkludert følgende:</p><li>Frigi til lager</li><li>Produksjonsbølgebehandling</li><li>Råvareplukking</li><li>Kanban plassert</li><li>Kanban-plukking</li><li>Produksjonssvinn</li><li>Siste produksjonspall</li><li>Registrer materialforbruk</li><li>Tøm Kanban</li></ul> | Ja | Nei |
| Etterfylling av råvarer | Nei | Nei |

## <a name="maintaining-scale-units-for-warehouse-execution"></a>Vedlikeholde skalaenheter for lagerkjøring

Flere satsvise jobber kjøres både på senteret og skalaenheter.

Ved senterdistribusjonen kan du vedlikeholde de satsvise jobbene manuelt. Du kan administrere følgende satsvise jobber under **Lagerstyring \> Periodiske oppgaver \> Back-office-arbeidsbelastningsbehandling**:

- Skalaenhet til sentermeldingsprosessor
- Registrer kildeordremottak
- Fullfør lagerordrer

I arbeidsbelastningen på skalaenheter kan du administrere følgende satsvise jobber under **Lagerstyring \> Periodiske oppgaver \> Arbeidsbelastningsbehandling**:

- Behandle bølgetabellposter
- Lagersenter til meldingsprosessor for skalaenhet
- Behandle forespørsler om oppdatering av antall for lagerordrelinjer

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
