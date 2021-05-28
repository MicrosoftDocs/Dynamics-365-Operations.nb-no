---
title: Bølgetildeling
description: Dette emnet beskriver hvordan du konfigurerer bølgetildelingstrinnet, inkludert hvordan du aktiverer parallell behandling for det.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: b01de3c9f1cbcb24abc2b5a0c91db7f0791020bf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019009"
---
# <a name="wave-allocation"></a>Bølgetildeling

[!include [banner](../includes/banner.md)]

Bølgebehandling kan være tidkrevende, og mesteparten av behandlingstiden brukes i tildelingstrinnet og i arbeidsopprettingstrinnet.

Nå er det mulig å kjøre hvert av disse trinnene parallelt, noe som kan forbedre ytelsen til bølgebehandlingen, og tillate en større produksjon av bølger i samme lager. Dette emnet forklarer hvordan du konfigurerer bølgetildelingsmetoden for å kjøre parallelt. Hvis du vil ha mer informasjon om hvordan du konfigurerer at oppretting av arbeidsprosesser skal kjøres parallelt, kan du se [Planlegge arbeidsopprettelse under bølge](configure-wave-schedule-work-creation.md).

Tidligere var det bare mulig å tildele én bølge på et lager om gangen. Denne begrensningen er fjernet og erstattet av en ny begrensning som bare låser varen og dimensjonene som er over lokasjonen i reservasjonshierarkiet. Dimensjoner over lokasjonen omfatter alltid produktdimensjoner. Hvis for eksempel en vare er konfigurert med *Farge*,kan varianter for *Rød*, *Blå* og *Gul* behandles parallelt.

Dette betyr at hvis den samme varen med de samme dimensjonene over lokasjonen tildeles med én bølge, må andre bølger vente med å få en lås på samme vare og dimensjoner. Hvis låsen ikke kan anskaffes innen rimelig tid, vil det oppstå en feil, og bølgebehandlingen vil mislykkes.

For å kunne benytte parallell behandling må bølgen kjøres satsvis.

## <a name="performance-improvements"></a>Ytelsesforbedringer

Ytelsesfordeler ved parallell behandling faller i to kategorier:

- **Forbedret gjennomstrømming** – Gjennomstrømmingen av bølger vil vanligvis forbedres selv om parallell behandling ikke er konfigurert, spesielt for scenarier der det ikke er noen overlapping av varer i bølgene.
- **Forbedring av tildelingen for en enkelt bølge** – Testing på kundedata har vist en ytelsesforbedring på nesten 50 % etter å ha byttet til parallell tildeling. Parallell behandling gjøres per varer og dimensjoner over lokasjonen, så forbedringene avhenger av hvor mange ulike varer en bølge inneholder, tilgjengelig infrastruktur og tildelingens varighet kontra varigheten til arbeidsopprettingen.

## <a name="configure-parallel-allocation"></a>Konfigurer parallell tildeling

### <a name="warehouse-management-parameters"></a>Lagerstyringsparametere

Hvis du vil bruke parallell tildelingsbehandling, kan du gå til **Lagerstyring > Oppsett > Lagerstyringsparametere**, åpne **Bølgebehandling**-fanen og foreta følgende innstillinger:

- **Satsvis gruppe for bølgebehandling** – Velg den satsvise gruppen som den første behandlingen av bølgene skal bruke. Den etterfølgende behandlingen av tildelinger kan gjøres ved hjelp av forskjellige satsvise grupper.
- **Behandle bølger satsvis** – Sett dette til *Ja* for å bruke parallell behandling.
- **Vent på lås (ms)** – Angi tiden, i millisekunder, som et tildelingstrinn skal vente på en systemressurs som er låst av et annet tildelingstrinn. Når denne tiden overskrides, behandles ikke på bølgen, og det vises en feilmelding. Vi anbefaler at du lar deg gå minst et par sekunder å tillate tildeling av én logisk enhet for å fullføre.

Hvis du vil ha mer informasjon om disse og andre alternativer for bølgebehandling på siden **Lagerstyringsparametere**, kan du se [Lagerparametere for bølgebehandling](wave-warehouse-parameters.md).

## <a name="wave-process-methods"></a>Bølgebehandlingsmetoder

Slik konfigurerer du parallell behandling:

1. Gå til **Lagerstyring > Oppsett > Bølger > Bølgebehandlingsmetoder**.
1. Velg `allocateWave`-metoden i rutenettet.
1. Velg **Oppgavekonfigurasjon** i handlingsruten.
1. Siden **Oppgavekonfigurasjon av bølgeposteringsmetode** åpnes. Dette rutenettet viser hvert lager der du har konfigurert `allocateWave`-metoden. Parallell behandling brukes bare for lagre som er oppført. Bruk knappene i handlingsruten til å legge til eller fjerne lagre fra rutenettet etter behov. 
1. Gjør følgende innstillinger for hvert lager:
    - **Maksimalt antall satsvise oppgaver** – Angi antall satsvise oppgaver som skal brukes for tildelingen for det valgte lageret. Det optimale antallet satsvise oppgaver avhenger av hvilken infrastruktur som er tilgjengelig, og hvilke andre satsvise jobber som behandles på serveren. Tester som ble utført i et miljø med fire kjerner som var dedikert til bølgebehandling, viste at bruk av åtte oppgaver produserte gode resultater.
    - **Satsvis gruppe for bølgebehandling** – Bestemte satsvise grupper kan brukes for forskjellige lagre for å tillate at tildelingsprosessen kan skaleres ut per lager.

## <a name="enable-or-disable-parallelization-across-all-legal-entities"></a>Aktivere eller deaktivere parallellisering på tvers av alle juridiske enheter

Vi anbefaler at du angir at `allocateWave`-metoden skal kjøres parallelt på tvers av alle juridiske enheter, fordi dette bidrar til å forbedre ytelsen til bølgebehandlingen. Fra og med Supply Chain Management versjon 10.0.17 er funksjonen *Bølgeparallellisering for Tildel bølge-metoden* aktivert som standard for alle nye og oppdaterte installasjoner, og kan ikke slås av på nytt. Når denne funksjonen er aktivert, skjer følgende:

- `allocateWave`-metoden oppdateres slik at den inneholder en oppgavekonfigurasjonsinnstilling som lar deg bruke siden **Bølgebehandlingsmetoder** til å definere antall oppgaver som skal kjøres samtidig, tilsvarende antall parallelle prosesser. Tiden som brukes i tildelingsbølgetrinnet (som vanligvis er 30 % til 60 % av den totale behandlingstiden), reduseres med en faktor som til sammen tilsvarer antall oppgaver. Du kan også velge hvilket parti som skal tilordnes til å behandle disse oppgavene. Det er viktig å merke seg at alle juridiske enheter vil bli konfigurert til å behandle bølger satsvis. For lagre som allerede er konfigurert til å behandle bølger i satsvis behandling, og for lagre som allerede er konfigurert til å bruke `allocateWave`-metoden parallelt, beholdes den eksisterende konfigurasjonen.
- Alle nye juridiske enheter er som standard konfigurert til å behandle bølger satsvis. Alle nye lagre med alternativet **Lagerstyringsprosesser** aktivert vil ha `allocateWave`-metoden konfigurert til å kjøres parallelt som standard.
- På siden **Lagerstyringsparametere** er **Behandle bølger satsvis** satt til *Ja* og **Vent på lås (ms)** satt til 15 sekunder som standard. Dette betyr at alle bølger vil bli utført satsvis. Når en bølge kjører, får den en lås på varen og dimensjonene over stedet under tildelingstrinnet. Når en annen bølgebehandlingsoppgave prøver å oppnå samme lås for den identiske posten, blokkeres den til den nåværende prosessen er fullført. Innstillingene for **Vent på lås (ms)** etablerer den maksimale tiden systemet venter før låsen frigis.

Parallell tildelingsbehandling krever bølgebehandling for å kjøre satsvis. Derfor vil du redusere bølgebehandlingsytelsen hvis du slår av innstillingen **Behandle bølger satsvis**, spesielt hvis bølgebehandlingen bruker en parallell prosess, slik det er definert i oppgavekonfigurasjonen for de relevante bølgemetodene.

Om nødvendig kan du angre hver av innstillingene som er gjort som standard, når funksjonen *Bølgeparallellisering for Tildel bølge-metoden* er aktivert automatisk for forekomsten. Slik gjør du det:

- Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**. På **Bølgebehandling**-fanen bruker du de foretrukne verdiene for **Behandle bølger satsvis** og **Vent på lås (ms)**.
- Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgebehandlingsmetoder**. Velg `allocateWave`-metoden. I handlingsruten velger du **Oppgavekonfigurasjon** for å åpne en side som fører opp hvert lager, der metoden er angitt til å kjøre parallelt. Endre eller slett antall satsvise oppgaver og den tilordnede bølgegruppen for hvert oppførte lager etter behov.

## <a name="troubleshooting"></a>Feilsøking

### <a name="troubleshoot-using-the-infolog"></a>Feilsøking ved hjelp av infologgen

Fordi det satsvise rammeverket brukes, blir feil som oppstår under bølgebehandling, oppfanget som en del av infologgene for satsvise jobber. Slik leser du de satsvise jobbene som er relatert til en bølge:

1. Gå til **Lagerstyring \> Utgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Velg bølgen som du vil kontrollere.
1. I handlingsruten åpner du **Bølge**-fanen, og fra **Bølge**-gruppen velger du **Satsvise jobber**.

Bølgebehandling korrigerer seg selv, så eventuelle feil som oppdages under behandling, bør rapporteres ved hjelp av infologgen.

En typisk feil relatert til parallell behandling kan være at to bølger prøver å tildele samme vare samtidig og en ikke fullfører slik at den andre bølgen ikke kan oppnå en lås innen det angitte tidspunktet. Hvis denne situasjonen oppstår, vil loggen for satsvise jobber inneholde informasjon som angir at lås for varen ikke kan anskaffes, og i så fall må bølgen som mislyktes, behandles på nytt.

Fordi behandlingen skjer parallelt, må data opprettholdes i forskjellige tabeller for å spore behandlingsstatusen. Dette betyr at loggene for de satsvise jobbene kan inneholde feil som duplikate nøkkelfeil.

Feilene fra de satsvise oppgavene er også en del av loggen for satsvise jobber. Den viktigste informasjonen er vanligvis nederst.

I sjeldne tilfeller, for eksempel hvis SQL-tilkoblingen avsluttet, er det mulig at bølgebehandlingen kan ende i en inkonsekvent tilstand der den satsvise jobben ser ut til å kjøre, men behandlingen stoppes. Bølgen kan ikke håndtere feil som dette, så et forsøk på å rydde opp i mislykkede bølger blir gjort når neste bølge kjører. Hvis den gjeldende bølgen er inkonsekvent, kan du imidlertid utføre følgende trinn:

1. Gå til **Lagerstyring \> Utgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Velg bølgen du trenger for å rydde opp.
1. I handlingsruten åpner du **Bølge**-fanen, og i **Bølge**-gruppen velger du **Rydd bølgedata**.

### <a name="troubleshoot-using-the-wave-progress-log"></a>Feilsøking ved hjelp av fremdriftsloggen for bølgen

Hvis alternativet **Opprett bølgefremdriftslogg** er aktivert på siden **Lagerstyringsparametere**, opprettes det en loggpost hver gang tildelingen for en vare og varens dimensjoner begynner og slutter. Du bør bare aktivere denne loggen når du trenger den, for eksempel i den innledende testingen eller i forbindelse med feilsøking. Når dette alternativet er aktivert, kan du vise loggen ved å gå gjennom følgende trinn:

1. Gå til **Lagerstyring \> Utgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Velg bølgen som du vil kontrollere.
1. I handlingsruten åpner du **Bølge**-fanen, og i **Bølge**-gruppen velger du **Fremdrift**.
