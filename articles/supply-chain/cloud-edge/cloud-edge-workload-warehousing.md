---
title: Arbeidsbelastninger for lagerstyring for sky- og kantskalaenheter
description: Dette emnet inneholder informasjon om funksjonen som gjør det mulig å kjøre valgte prosesser fra arbeidsbelastningen for lagerstyring.
author: perlynne
manager: tfeyr
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9b5d8c9e77fb98dfb7031a3868303970fe3bf865
ms.sourcegitcommit: 4835acc3edacf8277937723d3f85a7875bd8de83
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/11/2021
ms.locfileid: "5580971"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Skalaenheter for sky og kant for arbeidsbelastninger for lagerstyring

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Ikke all forretningsfunksjonalitet for lagerstyring støttes fullt ut for lagre som kjører en arbeidsbelastning på en skalaenhet. Pass på at du bare bruker prosessene som dette emnet beskriver som støttet.

## <a name="warehouse-execution-on-scale-units"></a>Lagerkjøring på skalaenheter

Denne funksjonen gjør det mulig for skalaenheter å kjøre valgte prosesser fra lagerstyringsfunksjonene. Skyskalaenheter kjører arbeidsbelastningene sine i skyen ved å bruke dedikert behandlingskapasitet i det valgte Microsoft Azure-området. For kantskalaenheter kan du kjøre noen arbeidsbelastninger uavhengig lokalt, også når skalaenhetene er midlertidig koblet fra skyen.

I dette emnet kalles lagerstyringskjøringer i et lager som defineres som en skalaenhet, et *lagerkjøringssystem* (*WES*).

## <a name="prerequisites"></a>Forutsetninger

Du må ha et Dynamics 365 Supply Chain Management-senter og en skalaenhet som er distribuert med arbeidsbelastningen for lagerstyring. Hvis du vil ha mer informasjon om arkitekturen og distribusjonsprosessen, kan du se [Sky- og kantskalaenheter for arbeidsbelastninger for produksjon og lagerstyring](cloud-edge-landing-page.md).

## <a name="how-the-wes-workload-works-on-scale-units"></a>Hvordan WES-arbeidsbelastninger fungerer på skalaenheter

For prosessene i arbeidsbelastningen for lagerstyring synkroniseres dataene mellom senteret og skalaenhetene.

En skalaenhet kan bare opprettholde dataene den eier. Dataeierskapskonseptet for skalaenheter bidrar til å forhindre multimaster-konflikter. Det er derfor viktig at du forstår hvilke prosesser som eies av senteret, og hvilke som eies av skalaenhetene.

Skalaenhetene eier følgende data:

- **Bølgebehandlingsdata** – Utvalgte bølgeprosessmetoder behandles som en del av bølgebehandling for skalaenhet.
- **Arbeidsbehandlingsdata** – Følgende typer behandling av arbeidsordre støttes:

  - **Lagerbevegelser** (manuell flytting og flytting etter malarbeid)
  - **Bestillinger** (plasseringsarbeid via en lagerordre når bestillinger ikke er knyttet til laster)
  - **Salgsordrer** (enkelt plukke- og lastearbeid)
  - **Overføringsordrer** (bare utgående med enkelt plukke- og lastearbeid)

- **Kvitteringsdata for lagerordre** – Disse dataene brukes bare for bestillinger som frigis manuelt til et lager.
- **Nummerskiltdata** – Nummerskilter kan opprettes på senteret og skalaenheten. Dedikert konflikthåndtering er angitt. Legg merke til at disse dataene ikke er lagerspesifikke.

## <a name="outbound-process-flow"></a>Utgående prosessflyt

Senteret eier følgende data:

- Alle kildedokumenter, for eksempel salgsordrer og overføringsordrer
- Ordretilordning og utgående lastbehandling
- Prosessene for frigivelse til lager, forsendelsesoppretting, bølgeoppretting og bølgesluttbehandling

Skalaenhetene eier den faktiske bølgebehandlingen (for eksempel arbeidsfordeling, etterfyllingsarbeid og oppretting av behovsbetinget arbeid) etter frigivelsen av bølgen. Derfor kan lagerarbeidere behandle utgående arbeid ved å bruke en lagerapp som er knyttet til skalaenheten.

![Bølgebehandlingsflyt](./media/wes-wave-processing-ga.png "Bølgebehandlingsflyt")

## <a name="inbound-process-flow"></a>Inngående prosessflyt

Senteret eier følgende data:

- Alle kildedokumenter, for eksempel bestillinger og salgsreturordrer
- Innkommende lastbehandling
- Alle oppdateringer for kostnad og økonomi

> [!NOTE]
> Den inngående bestillingsflyten er konseptuelt forskjellig fra den utgående flyten. Du kan styre det samme lageret på skalaenheten eller i senteret, avhengig av om bestillingen er frigitt til lageret eller ikke. Når du har frigitt en ordre til lageret, kan du bare arbeide med ordren mens du er logget på skalaenheten.

Hvis du bruker prosessen *Frigi til lager*, opprettes [*lagerordrer*](cloud-edge-warehouse-order.md), og eierskap av den relaterte mottaksflyten tilordnes til skalaenheten. Senteret vil ikke kunne registrere innkommende mottak.

Du må logge på senteret for å bruke prosessen *Frigi til lager*. Gå til en av følgende sider for å kjøre eller planlegge den:

- **Innkjøp og leverandører > Bestillinger > Alle bestillinger > Lager > Handlinger > Frigi til lager**
- **Lagerstyring > Frigi til lager > Automatisk frigivelse av bestillinger**

Når du bruker **Automatisk frigivelse av bestillinger**, kan du velge bestemte bestillingslinjer basert på en spørring. Et typisk scenario vil være å sette opp en gjentakende satsvis jobb som frigir alle bekreftede bestillingslinjer som forventes å ankomme neste dag.

Arbeideren kan kjøre mottaksprosessen ved å bruke en lagerapp som er knyttet til skalaenheten. Dataene registreres deretter av skalaenheten, og de rapporteres mot den inngående lagerordren. Oppretting og behandling av etterfølgende plassering vil også bli behandlet av skalaenheten.

Hvis du ikke bruker prosessen *frigivelsen til lager*, og dermed ikke bruker *lagerordrer*, kan senteret behandle lagermottak og arbeidsbehandling uavhengig av skalaenheter.

![Inngående prosessflyt](./media/wes-inbound-ga.png "Inngående prosessflyt")

## <a name="supported-processes-and-roles"></a>Prosesser og roller som støttes

Ikke alle lagerstyringsprosesser støttes i en WES-arbeidsbelastning på en skalaenhet. Derfor anbefaler vi at du tilordner roller som samsvarer med funksjonaliteten som er tilgjengelig for hver bruker.

For å støtte denne prosessen er en eksempelrolle som heter *Lagerstyring på arbeidsbelastning* inkludert i demonstrasjonsdataene under **Systemadministrasjon \> Sikkerhet \> Sikkerhetskonfigurasjon**. Formålet med denne rollen er å gjøre det mulig for lagerledere å få tilgang til WES på skalaenheten. Rollen gir tilgang til sidene som er relevante i sammenheng med en arbeidsbelastning som driftes på en skalaenhet.

Brukerroller på en skalaenhet tilordnes som en del av den opprinnelige datasynkroniseringen fra senteret til skalaenheten.

Hvis du vil endre rollene som er tilordnet til en bruker, går du til **Systemadministrasjon \> Sikkerhet \> Tilordne brukere til roller** på skalaenheten. Brukere som bare fungerer som lagerledere på skalaenheter, bør bare tilordnes rollen *Lagerlederen på arbeidsbelastning*. Denne tilnærmingen vil sikre at disse brukerne bare har tilgang til den støttede funksjonaliteten. Fjern eventuelle andre roller som er tilordnet til disse brukerne.

Brukere som fungerer som lagerledere både på senteret og skalaenheter, bør tilordnes den eksisterende rollen *Lagerarbeider*. Vær oppmerksom på at denne rollen gir lagerarbeidere tilgang til funksjoner (for eksempel behandling av overføringsordremottak) som vises i brukergrensesnittet (UI), men som ikke støttes for skalaenheter.

## <a name="supported-wes-processes"></a>Støttende WES-prosesser

Følgende lagerkjøringsprosesser kan aktiveres for en WES-arbeidsbelastning på en skalaenhet:

- Valgte bølgemetoder for salgs- og overføringsordrer (tildeling, behovsetterfylling, containerbruk, arbeidsoppretting og bølgeetikettutskrift)
- Behandle lagerarbeid for salgs- og overføringsordre ved hjelp av lagerappen (inkludert etterfyllingsarbeid)
- Foreta spørringer i lagerbeholdningen ved hjelp av lagerappen
- Opprette og kjøre lagerbevegelser ved hjelp av lagerappen
- Registrere bestillinger og utføre plasseringsarbeid ved hjelp av lagerappen

Følgende arbeidsordretyper støttes for øyeblikket for WES-arbeidsbelastninger på skalaenhetsdistribusjoner:

- Salgsordre
- Utstedelse for overføring
- Etterfylling
- Lagerbevegelse
- Bestillinger (koblet til lagerordrer)

Ingen andre typer behandling eller lagerarbeid for kildedokumenter støttes for øyeblikket på skalaenheter. For en WES-arbeidsbelastning på en skalaenhet kan du for eksempel ikke foreta et overføringsordremottak (overføringsmottak) eller behandle syklustellingsarbeid.

> [!NOTE]
> Menyelementer og knapper på mobilenheter for funksjoner som ikke støttes, vises ikke i _lagerappen_ når den er koblet til en skalaenhetsdistribusjon.

> [!WARNING]
> Når du kjører en arbeidsbelastning på en skalaenhet, kan du ikke kjøre prosesser som ikke støttes for dette bestemte lageret, i senteret. Tabellene som vises senere i dette emnet, dokumenterer funksjonene som støttes.
>
> Valgte lagerarbeidstyper kan opprettes både i senteret og på skalaenheter, men kan bare vedlikeholdes av eiersenteret eller -skalaenheten (distribusjonen som opprettet dataene).
>
> Selv når en bestemt prosess støttes av skalaenheten, må du være oppmerksom på at alle nødvendige data kanskje ikke blir synkronisert fra senteret til skalaenheten eller fra skalaenheten til senteret, som kan føre til uventet systembehandling. Eksempler:
> 
> - Hvis du bruker en spørring i et lokasjonsdirektiv som kobler sammen en datatabellpost som bare finnes i senterdistribusjonen.
> - Hvis du bruker lokasjonsstatus og/eller lokasjonsvolumetriske lastefunksjoner. Disse dataene blir ikke synkronisert mellom distribusjonene og fungerer derfor bare når lagerbeholdning for lokasjon oppdateres for en av distribusjonene.

Følgende lagerstyringsfunksjonalitet støttes ikke for øyeblikket for arbeidsbelastninger for skalaenheter:

- Inngående behandling av bestillingslinjer som er tilordnet til en last
- Inngående behandling av bestillinger for et prosjekt
- Inngående og utgående behandling for varer som har den aktive sporingsdimensjonen **Eier** og/eller **Serienummer**
- Behandling av lager som har en statusverdi for blokkering
- Endring av en lagerstatus under enhver arbeidsflyttingsprosess
- Ordreigangsatte fleksible dimensjonsreservasjoner på lagernivå
- Bruk av funksjonen *Status for lagerlokasjon* (dataene synkroniseres ikke mellom distribusjonene)
- Bruk av funksjonen *Nummerskiltplassering på lokasjon*
- Bruk av *Produktfiltre* og *Produktfiltergrupper*, inkludert innstillingen **Antallet dager som kreves for at partier kan kombineres**
- Integrasjon med kvalitetsstyring
- Behandling med faktisk vekt-varer
- Behandling med varer som bare er aktivert for transportstyring (TMS)
- Behandling med negativ lagerbeholdning
- Lagerarbeidsbehandling med egendefinerte arbeidstyper
- Lagerarbeidsbehandling med forsendelsesmerknader
- Lagerarbeidsbehandling med utløsing av syklustellingsterskel
- Lagerarbeidsbehandling med materialhåndtering/lagerautomatisering
- Bruk av avbildning av produktstandarddata (for eksempel i lagerappen)

> [!WARNING]
> Enkelte lagerfunksjoner blir ikke tilgjengelige for lagre som kjører arbeidsbelastninger for lagerstyring på en skalaenhet, og støttes heller ikke i senteret eller i arbeidsbelastningen for skalaenhet.
> 
> Andre funksjoner kan behandles på begge, men krever nøye bruk i enkelte scenarioer, for eksempel når lagerbeholdningen blir oppdatert for det samme lageret både i senteret og på skalaenheten på grunn av den asynkrone oppdateringsprosessen for data.
> 
> Bestemte funksjoner (for eksempel *Blokker arbeid*) som støttes både i senteret og på skalaenheter, støttes bare for eieren av dataene.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Utgående (støttes bare for salgs- og overføringsordrer)

Følgende tabell viser hvilke utgående funksjoner som støttes, og hvor de støttes, når arbeidsbelastningen for lagerstyring brukes i sky- og kantskalaenheter.

| Behandle                                                      | Hub | WES-arbeidsbelastning på en skalaenhet |
|--------------------------------------------------------------|-----|------------------------------|
| Behandling av kildedokument                                   | Ja | Nei |
| Last- og transportstyringsbehandling                | Ja | Nei |
| Frigi til lager                                         | Ja | Nei |
| Planlagt direkteoverføring                                        | Nei  | Nei |
| Forsendelseskonsolidering                                       | Ja | Nei |
| Forsendelsesbølgebehandling                                     | Ja, men bare initialisering og sluttbehandling av bølgen håndteres i senteret. Dette betyr at utgående behandling av overførings- og slagsordrer bare kan håndteres av skalaenheten.|<p>Nei, initialisering og sluttbehandling blir håndtert av senteret, og **Lastplanlegging og sortering** støttes ikke<p><b>Obs!</b> Tilgang til senteret kreves for å fullføre bølgestatusen som en del av bølgebehandlingen.</p> |
| Vedlikehold forsendelser for bølge                                  | Ja | Nei |
| Lagerarbeidsbehandling (inkl. nummerskiltutskrift)        | Nei  | <p>Ja, men bare for de ovennevnte funksjonene som støttes. |
| Gruppeplukking                                              | Nei  | Ja|
| Manuell emballasjebehandling, inkludert arbeidsbehandlingen Plukking av containerpakking                                           | Nei <P>En del behandling kan gjøres etter at en innledende plukkeprosess er håndtert av en skalaenhet, men anbefales ikke på grunn av blokkerte operasjoner.</p>  | Nei  |
| Fjern container fra gruppe                        | Nei  | Nei                           |
| Utgående sorteringsbehandling                                  | Nei  | Nei |
| Utskrift av belastningsrelaterte dokumenter                           | Ja | Nei |
| Fraktbrev og ved generering av forhåndsvarsel for forsendelse                            | Ja | Nei |
| Forsendelsesbekreftelse                    | Ja  | Nei |
| Forsendelsesbekreftelse med Bekreft og overfør                    | Nei  | Nei |
| Behandling av følgeseddel og fakturering                | Ja | Nei |
| Plukking med mangler (salgs- og overføringsordrer)                    | Nei  | Nei |
| Overplukking (salgs- og overføringsordrer)                     | Nei  | Nei |
| Endring av arbeidslokasjoner (salgs- og overføringsordrer)         | Nei  | Ja|
| Fullføre arbeid (salgs- og overføringsordrer)                    | Nei  | Ja|
| Skriv ut arbeidsrapport                                            | Ja | Nei |
| Bølgeetikett                                                   | Nei  | Ja|
| Oppdelt arbeid                                                   | Nei  | Ja|
| Arbeidsbehandling – styrt av Transportlasting            | Nei  | Nei |
| Reduser plukket antall                                       | Nei  | Nei |
| Tilbakefør arbeid                                                 | Nei  | Nei |
| Reverser forsendelsesbekreftelse                                | Ja | Nei |

### <a name="inbound"></a>Innlevering

Følgende tabell viser hvilke inngående funksjoner som støttes, og hvor de støttes, når arbeidsbelastningen for lagerstyring brukes i sky- og kantskalaenheter.

| Behandle                                                          | Hub | WES-arbeidsbelastning på en skalaenhet<BR>*(Varer som er merket «Ja», gjelder bare for lagerordrer)*</p> |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Behandling&nbsp;av&nbsp;kildedokument                                       | Ja | Nei |
| Last- og transportstyringsbehandling                    | Ja | Nei |
| Bekreftelse av inngående forsendelse                                            | Ja | Nei |
| Bestillingsfrigivelse til lager (lagerordrebehandling) | Ja | Nei |
| Annullering av lagerordrelinjer<p>Merk at dette bare støttes når det ikke er foretatt noen registrering mot linjen</p>          | Ja | Nei |
| Motta og plassere bestillingsvarer                       | <p>Ja,&nbsp;når&nbsp;det&nbsp;ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | <p>Ja, når en bestilling ikke er en del av en <i>last</i></p> |
| Bestillingslinjen er mottatt og plassert                        | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | <p>Ja, når en bestilling ikke er en del av en <i>last</i></p></p> |
| Mottak og plassering av returordre                               | Ja | Nei |
| Mottak og plassering av kombinerte nummerskilt                        | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Mottak av lastvare                                             | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Mottak og plassering av nummerskilt                              | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Motta og plassere overføringsordrevare                        | Ja | Nei |
| Mottak og plassering av overføringsordrelinje                        | Ja | Nei |
| Avbryt arbeid (inngående)                                              | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | <p>Ja, men bare når det ikke er merket av for alternativet <b>Avregistrer mottak når arbeid avbrytes</b> (på siden <b>Lagerstyringsparametere</b>)</p> |
| Behandling av bestillingsproduktkvittering                          | Ja | Nei |
| Bestilling som mottas med underlevering                        | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Ja, men bare ved å utføre en annulleringsforespørsel fra senteret |
| Bestilling som mottas med overlevering                        | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Ja  |
| Mottak med oppretting av arbeidstypen *Direkteoverføring*                   | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Mottak med oppretting av arbeidstypen *Kvalitetsordre*                  | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Mottak med oppretting av arbeidstypen *Sampling av kvalitetsvare*          | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Mottak med oppretting av arbeidstypen *Kvalitet i kvalitetskontroll*       | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Mottak med oppretting av kvalitetsordre                            | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Arbeidsbehandling – styrt av *Gruppeplassering*                             | Ja | Nei |
| Arbeidsbehandling med *Plukk med mangler*                                           | Ja | Nei |
| Nummerskiltlasting                                           | Ja | Nei |

### <a name="warehouse-operations-and-exception-handing"></a>Lageroperasjoner og unntaksbehandling

Følgende tabell viser hvilke funksjoner for lageroperatsjoner og unntaksbehandling som støttes, og hvor de støttes, når arbeidsbelastningen for lagerstyring brukes i sky- og kantskalaenheter.

| Behandle                                            | Hub | WES-arbeidsbelastning på en skalaenhet |
|----------------------------------------------------|-----|------------------------------|
| Nummerskiltforespørsel                              | Ja | Ja                          |
| Vareforespørsel                                       | Ja | Ja                          |
| Lokasjonsforespørsel                                   | Ja | Ja                          |
| Endre lager                                   | Ja | Ja                          |
| Bevegelse                                           | Ja | Ja                          |
| Flytting etter mal                               | Ja | Ja                          |
| Lageroverføring                                 | Ja | Nei                           |
| Opprett overføringsordre fra lagerapp           | Ja | Nei                           |
| Justering (inn/ut)                                | Ja | Nei                           |
| Endring av beholdningsstatus                            | Ja | Nei                           |
| Syklustelling og behandling av tellingsavvik | Ja | Nei                           |
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

Produksjonsscenarioer med lagerstyring støttes for øyeblikket ikke i arbeidsbelastninger for skalaenhet, som angitt i følgende tabell.

| Behandle | Hub | WES-arbeidsbelastning på en skalaenhet |
|---------|-----|------------------------------|
| <p>Alle lagerstyringsprosessene som er knyttet til produksjon. Her er noen eksempler:</p><li>Frigi til lager</li><li>Produksjonsbølgebehandling</li><li>Råvareplukking</li><li>RAF og plassering av ferdigvarer</li><li>Plasser koprodukt og biprodukt</li><li>Kanban plassert</li><li>Kanban-plukking</li><li>Start produksjonsordre</li><li>Produksjonssvinn</li><li>Siste produksjonspall</li><li>Registrer materialforbruk</li><li>Tøm Kanban</li></ul> | Ja | Nei |

## <a name="maintaining-scale-units-for-wes"></a>Vedlikeholde skalaenheter for WES

Flere satsvise jobber kjøres både på senteret og skalaenheter.

Ved senterdistribusjonen kan du vedlikeholde de satsvise jobbene manuelt. Du kan administrere følgende satsvise jobber under **Lagerstyring \> Periodiske oppgaver \> Back-office-arbeidsbelastningsbehandling**:

- Behandle oppdateringshendelser for arbeidsstatus
- Skalaenhet til sentermeldingsprosessor
- Registrer kildeordremottak
- Fullfør lagerordrer
- Behandle svar om oppdatering av antall for lagerordrelinjer

I arbeidsbelastningen på skalaenheter kan du administrere følgende satsvise jobber under **Lagerstyring \> Periodiske oppgaver \> Arbeidsbelastningsbehandling**:

- Behandle bølgetabellposter
- Lagersenter til meldingsprosessor for skalaenhet
- Behandle forespørsler om oppdatering av antall for lagerordrelinjer


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
