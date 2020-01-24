---
title: Forbedre ytelsen til hovedplanlegging
description: Dette emnet beskriver de ulike alternativene du kan bruke til å forbedre ytelsen til hovedplanleggingen eller feilsøke problemer.
author: t-benebo
manager: AnnBe
ms.date: 12/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 7e8c1d7ee51eb6e335554a01fd050bd80f2a070d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915230"
---
# <a name="improve-master-planning-performance"></a>Forbedre ytelsen for hovedplanlegging

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

Dette emnet beskriver de ulike alternativene du kan bruke til å forbedre ytelsen til hovedplanleggingen eller feilsøke problemer. De inneholder informasjon om parametere og innstillinger, og om anbefalte konfigurasjoner og handlinger. Det inneholder også et sammendrag av alle de viktige parameterne du bør vurdere når du har langvarige hovedplanleggingsjobber.

Dette emnet er beregnet på systemansvarlige eller IT-brukere som kan feilsøke. Det er også beregnet på produksjons- eller forsyningsplanleggere, fordi det inneholder informasjon om parametere som er knyttet til krav til forretningsplanleggingskrav. 

## <a name="parameters-related-to-master-planning-performance"></a>Parametere som er knyttet til hovedplanleggingsytelse

Ulike parametere påvirker kjøretiden til hovedplanlegging og må tas hensyn til.

### <a name="number-of-threads"></a>Antall tråder

Parameteren **Antall tråder** gjør at du kan justere hovedplanleggingsprosessen slik at ytelsen forbedres for det bestemte datasettet. Den angir totalt antall tråder som skal brukes til å kjøre hovedplanlegging. Den fører til parallellisering av hovedplanleggingskjøringen, som bidrar til å redusere kjøretiden. 

Du kan angi parameteren **Antall tråder** i dialogboksen **Hovedplanleggingskjøring**. Du kan åpne denne dialogboksen ved å gå til **Hovedplanlegging \> Hovedplanlegging \> Kjør \> Hovedplanlegging** eller velge **Kjør** i arbeidsområdet **Hovedplanlegging**. Du må bruke prøve- og feilemetoden til å finne den beste verdien for denne parameteren. Du kan likevel bruke følgende formler til å beregne en første verdi:

- **Hvis industrien din er produksjon:** (Antall tråder) = (antall planlagte ordrer ÷ 1 000)
- **I andre tilfeller:** (Antall tråder) = (antall varer ÷ 1 000)

Antallet hjelpere som brukes under hovedplanleggingen, må være mindre enn eller lik maksimalt antall tråder som er tillatt på den satsvise serveren. Hvis antallet hjelpere overskrider antall tråder på den satsvise serveren, fungerer ikke de ekstra trådene.

> [!NOTE]
> Hvis du angir **0** (null) for parameteren for **Antall tråder**, øker kjøretiden for hovedplanlegging. Derfor anbefaler vi at du alltid angir en verdi som er større enn 0.

### <a name="number-of-tasks-in-helper-task-bundle"></a>Antall oppgaver i oppgavebunt for hjelper

Hvis du endrer innstillingen **Antall oppgaver i oppgavebunt** (det vil si buntstørrelsen), kan det hende at du kan redusere kjøretiden. Denne innstillingen styrer antallet varer som planlegges sammen av én hjelper.

Du kan angi parameteren **Antall oppgaver i oppgavebunt** i **Ytelse**-delen i **Generelt**-fanen på siden **Parametere for hovedplanlegging** (**Hovedplanlegging \> Oppsett \> Parametere for hovedplanlegging**). Den beste verdien for denne parameteren avhenger av dataene. Derfor anbefaler vi at du starter med verdien **1** og bruker deretter prøve- og feilemetoden til å finne den beste verdien for oppsettet ditt.

Vi anbefaler generelt at du øker antallet oppgaver når antall varer er svært stort (hundretusener). I andre tilfeller bør du redusere antall oppgaver. Ta hensyn til følgende punkt når det gjelde følgende anbefalinger:

- I detaljhandels- og distribusjonsindustrier, der det er mange uavhengige varer, bruker du mange hjelpere siden det ikke er noen avhengighet mellom varer. 
- I produksjonsindustrien, der det er mange stykklister og delte delkomponenter, bruker du færre hjelpere siden avhengigheter mellom varer kan forårsake ventetid.

> [!TIP]
> Hvis du har ytelsesproblemer, anbefaler vi at du reduserer innstillingen for **Antall oppgaver i oppgavebunt** til **1**. Du kan deretter bruke prøve- og feilemetoden til å finne den beste verdien for oppsettet. Ytelsesproblemer oppstår generelt når det tar lengre tid å behandle én vare enn de gjenstående varene. I dette tilfellet ser du at to etterfølgende oppgaver som har statusen **Dekning** i hovedplanleggingskjøringen, har helt forskjellige kjøretider. I ekstreme tilfeller kan denne forskjellen være hele 30 minutter. Du kan utlede hvor lang tid det tar å kjøre oppgaver, ved å se på varigheten til hver oppgave.

### <a name="use-of-cache"></a>Bruk av hurtigminne

Parameteren **Bruk av hurtigminne** gjør at du kan justere hovedplanleggingsprosessen slik at ytelsen forbedres for det bestemte datasettet. Du kan for eksempel justere den for å oppnå følgende resultater:

- Hvis det utføres mer hurtigbufring, samles mer data i dataminnet. Forventningen er at dataene brukes på nytt senere. Hvis dataene er i minnet, trenger du kanskje færre databaseforespørsler. Hvis du foretar mer hurtigbufring, øker imidlertid minnekravene.
- Hvis du foretar mindre hurtigbufring, kan det hende at de samme dataene må hentes fra databasen oftere. Application Object Server (AOS) lagrer i tillegg litt data i minnet gjennom hele prosessen.

Det er vanskelig å forutse hvilket alternativ som er best, fordi hvert tilfelle ikke bare er avhengig av dataene, men også maskinvaren. Siden mindre hurtigbufring for eksempel forårsaker ekstra belastning på databaseserveren, er det sannsynligvis ikke en god idé å bruke dette alternativet hvis databaseserveren allerede er overbelastet.

Du kan angi parameteren **Bruk av hurtigminne** i **Ytelse**-delen i **Generelt**-fanen på siden **Parametere for hovedplanlegging** (**Hovedplanlegging \> Oppsett \> Parametere for hovedplanlegging**). Hvor effektiv hurtigbufring er, avhenger av kundedataene. Hvis du for eksempel aldri har behov for hurtigbufrede data, kaster du bare bort minne hvis du lagrer dataene til slutten på planleggingsprosessen. Hvis du i dette tilfellet konfigurerer mindre hurtigbufring, kan ytelsen øke fordi AOS krever mindre minne, og serverressurser frigjøres til andre oppgaver.

> [!TIP]
> Vi anbefaler generelt at du setter parameteren **Bruk av hurtigminne** til **Maksimum**, fordi parameteren er ment som en funksjon for ytelsesforbedring. Vi anbefaler at du setter parameteren til **Minimum** hvis du kjører lokalt og har begrenset med minne (ca. 2 gigabyte \[GB\]).

### <a name="number-of-orders-in-firming-bundle"></a>Antall ordrer i autoriseringsbunt

Parameteren **Antall ordrer i autoriseringsbunt** angir det totale antallet ordrer som blir behandlet samtidig av hver tråd/bunt. Den forårsaker parallellisering av den automatiske autoriseringen.

Du kan angi parameteren **Antall ordrer i autoriseringsbunt** i **Ytelse**-delen i **Generelt**-fanen på siden **Parametere for hovedplanlegging** (**Hovedplanlegging \> Oppsett \> Parametere for hovedplanlegging**). Parallellisering av den automatiske autoriseringen er basert på ordrene som må behandles sammen. Hvis denne parameteren for eksempel settes til **50**, kommer hver tråd eller satsvis oppgave til å hente 50 ordrer om gangen og behandle dem sammen. Vi anbefaler at du bruker prøve- og feilemetoden til å finne den beste verdien. Du kan likevel bruke følgende formel til å beregne en første verdi:

(Antall ordrer per bunt) = (antall behovsvarer ÷ antall tråder)

> [!NOTE]
> Hvis du setter parameteren **Antall ordrer i autoriseringsbunt** til **0** (null), skjer det ingen parallellisering av den automatiske autoriseringen. Hele prosessen kjører i én satsvis oppgave og har en kumulativ kjøretid. Kjøretiden for hovedplanleggingen kommer derfor til å økes. Vi anbefaler derfor at du setter denne parameteren til en verdi som er større enn **0** (null).

### <a name="time-fences"></a>Horisonter

Horisonter angir hvor langt inn i fremtiden beregningene og andre behov må beregnes ved hjelp av hovedplanlegging. Jo større horisonten er, desto lengre tid tar det å kjøre hovedplanlegging. Du bør derfor angi horisontene i henhold til forretningsbehovene. Hvis du vil ha mer informasjon om horisonter, kan du se [Definere hovedplanlegging](master-planning-setup.md).

### <a name="actions"></a>Handlinger

Du kan også finne parameteren **Handlingsmelding** blant horisontene. Beregningen av handlingsmeldinger forårsaker en lengre kjøretid for hovedplanlegging. Hvis handlingsmeldinger ikke analyseres og brukes regelmessig (daglig, ukentlig og så videre), bør du vurdere å deaktivere beregningen under hovedplanleggingskjøringen. Hvis du vil deaktivere beregningen, kan du på**Hovedplanlegging**-siden (**Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**), angi **Handlingsmelding**-horisonten til **0** (null). Kontroller også at innstillingen **Handlingsmelding** er deaktivert for alle dekningsgruppene.

### <a name="futures"></a>Terminer

Beregningen av terminer forårsaker en lengre kjøretid for hovedplanlegging. Hvis du ikke planlegger stykklister, eller hvis forsinkelser ikke må overføres fra forsyning til behov under planlegging, bør du vurdere å deaktivere beregning av terminer under hovedplanlegging. Hvis du vil deaktivere beregningene, setter du horisonten **Terminer** til **0** (null) for hovedplanen du kjører. Kontroller også at innstillingen **Terminer** er deaktivert for alle dekningsgruppene.

## <a name="one-heavy-routine-at-a-time"></a>Én krevende rutine om gangen

Ikke planlegg andre satsvise jobber samtidig når du planlegger hovedplanlegging. Pass spesielt på at du ikke planlegger andre krevende rutiner, for eksempel lagerlukking, samtidig.

## <a name="review-the-session-log"></a>Se gjennom øktloggen

Systemet kan samle inn mer informasjon om oppgavene som kjøres under hovedplanlegging. Hvis du vil at systemet skal samle inn denne informasjonen, aktiverer du innstillingen **Spor behandlingstid** i dialogboksen **Hovedplanleggingskjøring**. Informasjonen som samles inn, kan hjelpe deg å finne flaskehalser i kjøringen. Når parameteren **Antall oppgaver i oppgavebunt for hjelper** for eksempel er satt til **1**, kan du identifisere varen som har den lengste kjøretiden. Du kan også sammenligne kjøretidene for de ulike trådene som har statusen **Dekning**, og sammenligne varigheten for hver oppgave.

Hvis du vil se gjennom hovedplanleggingskjøringene på systemet, følger du ett av disse trinnene.

- Velg en hovedplan i rullegardinlisten i arbeidsområdet **Hovedplanlegging**, og velg deretter **Logg** på flisen **Hovedplanlegging**. Velg en jobb, velg **Forespørsler** i hurtigfanen, og velg deretter **Varighet for prosessoppgave**.
- Ve en plan i venstre rute på **Hovedplaner**-siden , og velg deretter **Logg** i hurtigfanen. Velg en jobb, velg **Forespørsler** i hurtigfanen, og velg deretter **Varighet for prosessoppgave**.

Når du ser gjennom øktloggen, bør du vurdere følgende:

- **Oppdater** skal ikke ta lang tid (generelt skal det ta opptil 30 minutter), men er enkelttrådet.
- **Kopier plan** skal ikke ta lang tid (det skal ta omtrent ett minutt).
- **Automatisk autorisering** tar vanligvis omtrent 30 minutter. Det kan imidlertid ta opptil flere timer, avhengig av antall ordrer og kompleksiteten til varene.
- **Automatisk autorisering** skal ta mindre tid enn **Dekning**.
- **Dekning** skal ta lengst tid i forhold til resten.
- **Handling** og **Fremtidig melding** kan ta lang tid, avhengig av dataene og antallet stykklister.

## <a name="filtering-of-items"></a>Filtrering av varer

Filtre som brukes i dialogboksen **Hovedplanleggingskjøring**, påvirker varigheten til hovedplanleggingskjøringen. Gå til **Hovedplanlegging \> Hovedplanlegging \> Kjør \> Hovedplanlegging**, eller velg **Kjør** i arbeidsområdet **Hovedplanlegging**. Hvis du vil utelate varer fra kjøringen, anbefaler vi at du filtrerer etter livssyklustilstanden for varen (ikke etter varenumre). Når du filtrerer etter livssyklustilstanden, tar oppdateringsprosessen mindre tid enn når du filtrerer etter varenumre.

## <a name="automatically-filter-by-items-with-direct-demand"></a>Filtrer automatisk etter varer med direkte behov

Hvis du vil forbedre kjøretiden for hovedplanlegging, kan du velge å bare inkludere varer med direkte behov. Dette filteret kan bare brukes for en fullstendig hovedplanleggingskjøring uten andre filtre som brukes i **Poster som skal inkluderes**-feltet. En hovedplanlegging som kjøres med filtre, ignorerer innstillingen **Filtrer automatisk etter varer med direkte behov**.

Feltet **Filtrer automatisk etter varer med direkte behov** finnes på siden **Parametere for hovedplanlegging**, og kan brukes med både forhåndsbehandlings- og etterbehandlingsinnstillinger.

### <a name="pre-processing"></a>Forhåndsbehandling
Parameterne **Forhåndsbehandling: Filtrer automatisk etter varer med direkte behov** sikrer at forhåndsbehandlingsfasen av hovedplanlegging bare inneholder varer som oppfyller minst én av følgende betingelser:
  - Varen har en forventet kvittering eller avgang, for eksempel en bestilling, salgsordre, tilbud, overføringsordre eller produksjonsordre. 
  - Varen har varedekning med sikkerhetslager (minimum lagerbeholdning).
  - Prognosebehov etter i dag finnes for varen.
  - Prognoseforsyning etter i dag finnes for varen.
  - Varen inkluderer alle kontinuitetslinjer fra telefonsentermodulen som ennå ikke er opprettet.

> [!NOTE]
> En vare som har fysisk tilgjengelig lagerbeholdning, vil ikke vise en behovstransaksjon fordi det ikke er behov for varen.

### <a name="post-processing"></a>Etterbehandling
Alternativet **Etterbehandling: Filtrer automatisk etter varer med direkte behov** er bare tilgjengelig hvis du angir **Krav angående stykklisteversjon** i dekningsgruppene. Hvis ikke trenger du ikke aktivere parameteren. 

Før dekningstrinnet starter, er det et trinn før dekning der varer med dekningsinnstillingen **Krav angående stykklisteversjon** er aktivert, vil bli behandles på nytt. Dette gjøres for å sikre at varer fra den nødvendige stykklisteversjonen planlegges. Varer som anses å ha behov under forhåndsbehandling, har ikke lenger behov, og bør derfor utelates fra planleggingskjøringen.

## <a name="performance-checklist-summary"></a>Sammendrag av sjekkliste for ytelse

- **Antall tråder** – Sett til en verdi som er større enn **0** (null).
- **Antall oppgaver i oppgavebunt for hjelper** – Sett til en verdi som er større enn **0** (null). (Bruk formlene som ble vist tidligere i dette emnet.)
- **Bruk av hurtigminne** Sett til **Maksimum** med mindre systemet har lite minne.
- **Antall ordrer i autoriseringsbunt** – Sett til en verdi som er større enn **0** (null). (Bruk formelen som ble vist tidligere i dette emnet.)
- **Horisonter** – Juster etter forretningsbehovene dine.
- **Handlinger og terminer** – Deaktiver handlinger og terminer hvis du ikke bruker dem.
- **Én krevende rutine om gangen** – Ikke kjør hovedplanlegging sammen med en annen krevende rutine.
- **Se gjennom øktloggen.**
- **Filtrering av varer** – Bruk livssyklustilstanden til å utelate varer fra hovedplanleggingskjøringen. (Ikke bruk varenumrene.)
