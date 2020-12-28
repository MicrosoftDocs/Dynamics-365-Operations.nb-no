---
title: Arbeidsbelastninger for lagerstyring for sky- og kantskaleringsenheter
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4ac76ad5cd88c35ac312b8e73d942a692f35c8aa
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516846"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Arbeidsbelastninger for lagerstyring for sky- og kantskaleringsenheter

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Ikke alle forretningsfunksjoner støttes fullstendig i den offentlige forhåndsversjonen når arbeidsbelastningsskaleringsenheter brukes. Pass på at du bare bruker prosessene som dette emnet beskriver som støttet.

## <a name="warehouse-execution-on-scale-units"></a>Lagerkjøring på skaleringsenheter

Denne funksjonen gjør det mulig for skaleringsenheter å kjøre valgte prosesser fra lagerstyringsfunksjonene. Skyskaleringsenheter kjører arbeidsbelastningene sine i skyen ved å bruke dedikert behandlingskapasitet i det valgte Microsoft Azure-området. For kantskaleringsenheter kan du kjøre noen arbeidsbelastninger uavhengig lokalt, også når skaleringsenhetene er midlertidig koblet fra skyen.

I dette emnet kalles lagerstyringskjøringer i et lager som defineres som en skaleringsenhet, et *lagerkjøringssystem* (*WES*).

## <a name="prerequisites"></a>Forutsetninger

Du må ha et Dynamics 365 Supply Chain Management-senter og en skaleringsenhet som er distribuert med arbeidsbelastningen for lagerstyring. Hvis du vil ha mer informasjon om arkitekturen og distribusjonsprosessen, kan du se [Sky- og kantskalaenheter for arbeidsbelastninger for produksjon og lagerstyring](cloud-edge-landing-page.md).

## <a name="how-the-wes-workload-works-on-scale-units"></a>Hvordan WES-arbeidsbelastninger fungerer på skaleringsenheter

For prosessene i arbeidsbelastningen for lagerstyring synkroniseres dataene mellom senteret og skaleringsenhetene.

En skaleringsenhet kan bare opprettholde dataene den eier. Dataeierskapskonseptet for skaleringsenheter bidrar til å forhindre multimaster-konflikter. Det er derfor viktig at du forstår hvilke prosesser som eies av senteret, og hvilke som eies av skaleringsenhetene.

Skaleringsenhetene eier følgende data:

- **Bølgebehandlingsdata** – Utvalgte bølgeprosessmetoder behandles som en del av bølgebehandling for skaleringsenhet.
- **Arbeidsbehandlingsdata** – Følgende typer behandling av arbeidsordre støttes:

    - Lagerbevegelser (manuell flytting og flytting etter malarbeid)
    - Bestillinger (plasseringsarbeid via en lagerordre)
    - Salgsordrer (enkelt plukke- og lastearbeid)

- **Kvitteringsdata for lagerordre** – Disse dataene brukes bare for bestillinger som frigis manuelt til et lager.
- **Nummerskiltdata** – Nummerskilter kan opprettes på senteret og skaleringsenheten. Dedikert konflikthåndtering er angitt. Legg merke til at disse dataene ikke er lagerspesifikke.

## <a name="outbound-process-flow"></a>Utgående prosessflyt

Senteret eier følgende data:

- Alle kildedokumenter, for eksempel salgsordrer og overføringsordrer
- Ordretilordning og utgående lastbehandling
- Frigivelse til lager, forsendelsesoppretting og oppretting av bølgeprosesser

Skaleringsenhetene eier den faktiske bølgebehandlingen (for eksempel arbeidsfordeling, etterfyllingsarbeid og oppretting av behovsbetinget arbeid) etter frigivelsen av bølgen. Derfor kan lagerarbeidere behandle utgående arbeid ved å bruke en lagerapp som er knyttet til skaleringsenheten.

![Bølgebehandlingsflyt](./media/wes_wave_processing_flow.png "Bølgebehandlingsflyt")

## <a name="inbound-process-flow"></a>Inngående prosessflyt

Senteret eier følgende data:

- Alle kildedokumenter, for eksempel bestillinger og salgsreturordrer
- Innkommende lastbehandling

> [!NOTE]
> Den innkommende bestillingsflyten er begrepsmessig forskjellig fra den utgående flyten, der skaleringsenheten som gjør behandlingen, er avhengig av om bestillingen er frigitt til et lager.

Hvis du bruker prosessen *frigivelsen til lager*, opprettes lagerordrer, og eierskap av den relaterte mottaksflyten tilordnes til skaleringsenheten. Senteret vil ikke kunne registrere innkommende mottak.

Arbeideren kan kjøre mottaksprosessen ved å bruke en lagerapp som er knyttet til skaleringsenheten. Dataene registreres deretter av skaleringsenheten, og de rapporteres mot den inngående lagerordren. Oppretting og behandling av etterfølgende plassering vil også bli behandlet av skaleringsenheten.

Hvis du ikke bruker prosessen *frigivelsen til lager*, og dermed ikke bruker *lagerordrer*, kan senteret behandle lagermottak og arbeidsbehandling uavhengig av skaleringsenheter.

![Inngående prosessflyt](./media/wes_Inbound_flow.png "Inngående prosessflyt")

## <a name="supported-processes-and-roles"></a>Prosesser og roller som støttes

Ikke alle lagerstyringsprosesser støttes i en WES-arbeidsbelastning på en skaleringsenhet. Derfor anbefaler vi at du tilordner roller som samsvarer med funksjonaliteten som er tilgjengelig for hver bruker.

For å støtte denne prosessen er en eksempelrolle som heter *Lagerstyring på arbeidsbelastning* inkludert i demonstrasjonsdataene under **Systemadministrasjon \> Sikkerhet \> Sikkerhetskonfigurasjon**. Formålet med denne rollen er å gjøre det mulig for lagerledere å få tilgang til WES på skaleringsenheten. Rollen gir tilgang til sidene som er relevante i sammenheng med en arbeidsbelastning som driftes på en skaleringsenhet.

Brukerroller på en skaleringsenhet tilordnes som en del av den opprinnelige datasynkroniseringen fra senteret til skaleringsenheten.

Hvis du vil endre rollene som er tilordnet en bruker, går du til **Systemadministrasjon \> Sikkerhet \> Tilordne brukere til roller** på skaleringsenheten. Brukere som bare fungerer som lagerledere på skaleringsenheter, bør bare tilordnes rollen *Lagerlederen på arbeidsbelastning*. Denne tilnærmingen vil sikre at disse brukerne bare har tilgang til den støttede funksjonaliteten. Fjern eventuelle andre roller som er tilordnet til disse brukerne.

Brukere som fungerer som lagerledere både på senteret og skaleringsenheter, bør tilordnes den eksisterende rollen *Lagerarbeider*. Vær oppmerksom på at denne rollen gir lagerarbeidere tilgang til funksjoner (for eksempel overføringsordrebehandling) som vises i brukergrensesnittet (UI), men som ikke støttes for skaleringsenheter.

## <a name="supported-wes-processes"></a>Støttende WES-prosesser

Følgende lagerkjøringsprosesser kan aktiveres for en WES-arbeidsbelastning på en skaleringsenhet:

- Valgte bølgemetoder for salgsordrer og behovsetterfylling
- Kjøre arbeidsordrer fra salgsordrer og behovsetterfylling ved hjelp av lagerappen
- Foreta spørringer i lagerbeholdningen ved hjelp av lagerappen
- Opprette og kjøre lagerbevegelser ved hjelp av lagerappen
- Registrere bestillinger og utføre plasseringsarbeid ved hjelp av lagerappen

Følgende arbeidsordretyper støttes for øyeblikket for WES-arbeidsbelastninger på skaleringsenhetsdistribusjoner:

- Salgsordre
- Etterfylling
- Lagerbevegelse
- Bestillinger som er koblet til lagerordrer

Ingen annen behandling av kildedokumenter støttes for øyeblikket på skaleringsenheter. For en WES-arbeidsbelastning på en skaleringsenhet kan du for eksempel ikke utføre følgende handlinger:

- Frigi en overføringsordre.
- Behandle de utgående plukk- og forsendelsesoperasjonene.

> [!IMPORTANT]
> Hvis du bruker en arbeidsbelastning på en skaleringsenhet, kan du ikke kjøre prosesser som ikke støttes for det bestemte lageret på senteret.

Følgende lagerstyringsfunksjonalitet støttes ikke for øyeblikket på skaleringsenheter:

- Inngående og utgående behandling for varer som har en hvilken som helst aktiv sporingsdimensjon (for eksempel parti- eller serienummerdimensjoner)
- Behandling av lagerstatusendringer
- Behandling av lager som har en statusverdi for blokkering
- Integrasjon med kvalitetsstyring
- Integrasjon med produksjon
- Behandling av faktisk vekt-varer
- Behandling av overlevering og underlevering
- Behandling av negativ lagerbeholdning

### <a name="outbound-supported-only-for-sales-orders-and-demand-replenishment"></a>Utgående (støttes bare for salgsordrer og behovsetterfylling)

Følgende tabell viser hvilke utgående funksjoner som støttes, og hvor de støttes, når arbeidsbelastningen for lagerstyring brukes i sky- og kantskaleringsenheter.

> [!WARNING]
> Siden bare salgsordrebehandling støttes, kan ikke utgående lagerstyringsbehandling brukes for overføringsordrer.
>
> Noen lagerfunksjoner er ikke tilgjengelige på lagre som kjører arbeidsbelastningen for lagerstyring i en skaleringsenhet.

| Behandle                                                      | Hub | WES-arbeidsbelastning på en skaleringsenhet |
|--------------------------------------------------------------|-----|------------------------------|
| Behandling av kildedokument                                   | Ja | Nei |
| Last- og transportstyringsbehandling                | Ja | Nei |
| Frigi til lager                                         | Ja | Nei |
| Forsendelseskonsolidering                                       | Nei  | Nei |
| Direkteoverføringsarbeid (plukkarbeid)                                 | Nei  | Nei |
| Forsendelsesbølgebehandling                                     | Nei, men fullføring av bølgestatusen håndteres i senteret |<p>Ja, men følgende funksjoner støttes ikke:</p><ul><li>Opprettelse av parallellarbeid</li><li>Lastplanlegging og sortering</li><li>Containerbruk</li><li>Bølgeetikettutskrift</li></li></ul><p><b>Obs!</b> Tilgang til senteret kreves for å fullføre bølgestatusen som en del av bølgebehandlingen.</p> |
| Lagerarbeidsbehandling (inkl. nummerskiltutskrift)     | Nei  | <p>Ja, men bare for følgende funksjoner:</p><ul><li>Salgsplukking (uten bruk av aktive sporingsdimensjoner)</li><li>Salgslasting (uten bruk av aktive sporingsdimensjoner)</li></ul> |
| Gruppeplukking                                              | Nei  | Nei |
| Emballasjebehandling                                           | Nei  | Nei |
| Utgående sorteringsbehandling                                  | Nei  | Nei |
| Utskrift av belastningsrelaterte dokumenter                           | Ja | Nei |
| Fraktbrev og ved generering av forhåndsvarsel for forsendelse                            | Ja | Nei |
| Sendingsbekreftelse og følgeseddelbehandling                | Ja | Nei |
| Plukking med mangler (salgsordrer)                                 | Nei  | Nei |
| Arbeidsannullering                                            | Nei  | Nei |
| Endring av arbeidslokasjoner (salgsordrer)                      | Nei  | Nei |
| Fullføre arbeid (salgsordrer)                                 | Nei  | Nei |
| Blokker og opphev blokkering av arbeid                                       | Nei  | Nei |
| Endre bruker                                                  | Nei  | Nei |
| Skriv ut arbeidsrapport                                            | Nei  | Nei |
| Bølgeetikett                                                   | Nei  | Nei |
| Tilbakefør arbeid                                                 | Nei  | Nei |

### <a name="inbound"></a>Innlevering

Følgende tabell viser hvilke inngående funksjoner som støttes, og hvor de støttes, når arbeidsbelastningen for lagerstyring brukes i sky- og kantskaleringsenheter.

| Behandle                                                          | Hub | WES-arbeidsbelastning på en skaleringsenhet |
|------------------------------------------------------------------|-----|------------------------------|
| Behandling&nbsp;av&nbsp;kildedokument                                       | Ja | Nei |
| Last- og transportstyringsbehandling                    | Ja | Nei |
| Forsendelsesbekreftelse                                            | Ja | Nei |
| Bestillingsfrigivelse til lager (lagerordrebehandling) | Ja | Nei |
| Motta og plassere bestillingsvarer                        | <p>Ja,&nbsp;når&nbsp;det&nbsp;ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | <p>Ja, når det er en lagerordre, og når en bestilling ikke er en del av en <i>belastning</i>. To menyelementer for mobilenheter må imidlertid brukes, en for mottak (<i>bestillingsvaremottak</i>) og en annen, med <b>Bruk eksisterende arbeid</b>-alternativet aktivert for å behandle plasseringen.</p><p>Nei, når det ikke er en lagerordre.</p> |
| Bestillingslinjen er mottatt og plassert                        | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Mottak og plassering av returordre                               | Ja | Nei |
| Mottak og plassering av kombinerte nummerskilt                        | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Mottak av lastvare                                              | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Mottak og plassering av nummerskilt                              | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |
| Motta og plassere overføringsordrevare                        | Ja | Nei |
| Mottak og plassering av overføringsordrelinje                        | Ja | Nei |
| Arbeidsannullering                                                | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | <p>Ja, men alternativet <b>Avregistrer mottak ved annullerings av arbeid</b> (på siden <b>Lagerstyringsparametere</b>) støttes ikke.</p> |
| Behandling av bestillingsproduktkvittering                        | Ja | Nei |
| Oppretting av direkteoverføringsarbeid som en del av mottaket                 | <p>Ja, når det ikke er en lagerordre</p><p>Nei, når det er en lagerordre</p> | Nei |

### <a name="warehouse-operations-and-exception-handing"></a>Lageroperasjoner og unntaksbehandling

Følgende tabell viser hvilke funksjoner for lageroperatsjoner og unntaksbehandling som støttes, og hvor de støttes, når arbeidsbelastningen for lagerstyring brukes i sky- og kantskaleringsenheter.

| Behandle                                            | Hub | WES-arbeidsbelastning på en skaleringsenhet |
|----------------------------------------------------|-----|------------------------------|
| Nummerskiltforespørsel                              | Ja | Ja                          |
| Vareforespørsel                                       | Ja | Ja                          |
| Lokasjonsforespørsel                                   | Ja | Ja                          |
| Endre lager                                   | Ja | Ja                          |
| Bevegelse                                           | Nei  | Ja                          |
| Flytting etter mal                               | Nei  | Ja                          |
| Justering (inn/ut)                                | Ja | Nei                           |
| Syklustelling og behandling av tellingsavvik | Ja | Nei                           |
| Skrive ut etikett på nytt (nummerskilteutskrift)             | Ja | Nei                           |
| Nummerskilt-build                                | Ja | Nei                           |
| Nummerskilt – bryt                                | Ja | Nei                           |
| Sjåførinnsjekking                                    | Ja | Nei                           |
| Sjåførutsjekking                                   | Ja | Nei                           |
| Endre partidisposisjonskode                      | Ja | Nei                           |
| Vis liste over åpent arbeid                             | Ja | Nei                           |
| Konsolider skiltnummer                         | Nei  | Nei                           |
| Fjern container fra gruppe                        | Nei  | Nei                           |
| Avbryt arbeid                                        | Nei  | Nei                           |
| Behandling av minimums-/maksimumsetterfylling                   | Nei  | Nei                           |
| Behandling av sporingsetterfylling                  | Nei  | Nei                           |

### <a name="production"></a>Produksjon

Lagerstyringsintegrering for produksjonsscenarioer støttes for øyeblikket ikke, som angitt i følgende tabell.

| Behandle | Hub | WES-arbeidsbelastning på en skaleringsenhet |
|---------|-----|------------------------------|
| <p>Alle lagerstyringsprosessene som er knyttet til produksjon. Her er noen eksempler:</p><li>Frigi til lager</li><li>Produksjonsbølgebehandling</li><li>Råvareplukking</li><li>Plasser ferdigvarer</li><li>Plasser koprodukt og biprodukt</li><li>Kanban plassert</li><li>Kanban-plukking</li><li>Start produksjonsordre</li><li>Produksjonssvinn</li><li>Siste produksjonspall</li><li>Registrer materialforbruk</li><li>Tøm Kanban</li></ul> | Nei | Nei |

## <a name="maintaining-scale-units-for-wes"></a>Vedlikeholde skaleringsenheter for WES

Flere satsvise jobber kjøres både på senteret og skaleringsenheter.

Ved senterdistribusjonen kan du vedlikeholde de satsvise jobbene manuelt. Du kan administrere følgende tre jobber under **Lagerstyring \> Periodiske oppgaver \> Back-office-arbeidsbelastningsbehandling**:

- Behandle oppdateringshendelser for arbeidsstatus
- Behandle overføringshendelser for kontroll av bølgeutførelse
- Registrer kildeordremottak

På arbeidsbelastningen på skaleringsenheter kan du administrere følgende to jobber under **Lagerstyring \> Periodiske oppgaver \> Arbeidsbelastningsbehandling**:

- Behandle bølgetabellposter
- Behandle overføringshendelser for kontroll av bølgeutførelse
