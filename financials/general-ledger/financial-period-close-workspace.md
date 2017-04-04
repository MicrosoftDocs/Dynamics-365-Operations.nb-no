---
title: "Arbeidsområde for regnskapsperiodeavslutning"
description: "Denne artikkelen gir en oversikt over arbeidsområdet for regnskapsperiodeavslutning og den tilknyttede konfigurasjonen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: ba0d709d123f56edb2a5287376c06c1f41181b1c
ms.lasthandoff: 03/31/2017


---

# <a name="financial-period-close-workspace"></a>Arbeidsområde for regnskapsperiodeavslutning

Denne artikkelen gir en oversikt over arbeidsområdet for regnskapsperiodeavslutning og den tilknyttede konfigurasjonen.

Arbeidsområde for regnskapsperiodeavslutning

Den **nær finansperiode** arbeidsområde kan du spore økonomiske lukking-prosesser på tvers av firmaer, områder og personer. Avhengig av visningen av den **nær finansperiode** arbeidsområde, vil du se enten for alle aktiviteter og status for en avsluttende tidsplan, eller bare oppgavene som er tilordnet til deg. 

Du må først velge en avsluttende tidsplan øverst i arbeidsområdet. Alle data som vises i arbeidsområdet er deretter filtrert etter den valgte lukking tidsplanen.

### <a name="summary-tiles"></a>Sammendrag-fliser

Flisene **Sammendrag** gir en oversikt over prosessen, og indikatorer hjelper deg med å holde avslutningsprosessen i rute. Du kan vise aktiviteter som er utløpt forfallsdato, gjenværende aktivitetene for i dag, aktiviteter som forfaller i dag, men er blokkert på grunn av avhengigheter og alle gjenstående oppgaver for prosessen. Denne informasjonen er for alle firmaer som er inkludert i den valgte lukking tidsplanen.

### <a name="tasks-and-status-section"></a>Delen Oppgaver og status

I den **aktiviteter og** -delen, status for samlede avsluttende tidsplan er inndelt i ulike måter: status etter firma, status etter område og status etter person som er ansvarlig. Du kan vise statusen for alle aktivitetene i avsluttende planlegge, bare aktiviteter som forfaller i dag, eller aktiviteter som har forfalt ved å endre filteret på toppen av listen over kort. Du kan også velge firma-filter for å vise statusen for et bestemt selskap. Hver status-kategorien gir en oppdeling av både prosentandelen som er fullført og antall oppgaver som gjenstår. Velg kortet eller **Vis detaljer** handlingen til å filtrere listen over detaljert oppgaver ved det valgte kortet. 

Den siste fanen er for detaljert aktivitets-listen. Denne listen viser full oppgavelisten kan filtreres slik at den viser bare aktivitetene som du er interessert i. Du kan filtrere listen over oppgaver på flere måter. Du kan for eksempel filtrere etter oppgave forfallsdato, tilknyttede selskap og tilknyttede området. Du kan også velge å vise eller skjule fullførte oppgaver i oppgavelisten. 

To indikatorer brukes for oppgaver:

-   Et utropstegn ikon angir at oppgaven er forfalt. Forfallsdatoen er også uthevet i rødt for aktiviteter som har forfalt.
-   En hengelås-ikon angir at aktiviteten er avhengig av andre aktiviteter som ikke er fullført ennå. En aktivitet som er blokkert av avhengigheter kan ikke merkes som fullført. Du kan angi avhengigheter for en aktivitet ved hjelp av **angir avhengighet** handling.

Navnet på aktiviteten er en hyperkobling til Microsoft Dynamics 365 for operasjoner-siden eller andre webside hvor brukeren må gå for å fullføre arbeidet. Du kan angi denne hyperkoblingen ved hjelp av **aktivitetskobling** -feltet når du redigerer eller opprette en oppgave. 

Du kan legge ved filer, notater, bilder og URL-adresser til en aktivitet ved hjelp av den **vedlegg** handling. Du kan for eksempel angi journalnumre som brukes som en del av en oppgave, legge til kommentarer om en bestemt aktivitet, eller legge ved en rapportfil som ble skrevet ut for en aktivitet. Et ikon vises i den **vedlegg** kolonnen for aktiviteten hvis det finnes et vedlegg. 

Den **fullføre oppgaven** alternativet må velges manuelt etter at aktiviteten er fullført. Når en aktivitet er merket som fullført, den **fullført dato** feltet oppdateres automatisk til den gjeldende dato og klokkeslett. Avhengighet indikatorer oppdateres også etter behov.

## <a name="all-financial-period-close-tasks-list-page"></a>Listeside for alle oppgaver ved regnskapsperiodeavslutning
Du kan vise alle gjeldende og forrige periode Lukk aktiviteter fra det **alle finansperiode Lukk aktiviteter** listesiden. Listesiden denne er best til historisk analyse av avslutningsprosessen, fordi den inneholder informasjon om den planlagte forfallsdato, den faktiske sluttdatoen, og personen som har fullført oppgaven. Du kan enkelt eksportere informasjonen på denne listeside til Microsoft Excel for rapportering og overvåking formål.

## <a name="financial-period-close-configuration-page"></a>Side for konfigurasjon av regnskapsperiodeavslutning
Før du kan bruke den **nær finansperiode** arbeidsområde, må du konfigurere prosessen i Microsoft Dynamics 365 for operasjoner ved hjelp av den **økonomisk periode Lukk konfigurasjon** siden. (Klikk **Økonomi**&gt;**Lukk periode**&gt;**økonomisk periode Lukk konfigurasjon**.)

### <a name="resources"></a>Ressurser

På den **ressurser** i kategorien kan du definere hvem som er involvert i de avsluttende prosessene. Alle ansatte som skal være ansvarlig for en avsluttende oppgave må først være tilordnet her. Du må også angi den ansattes visning av arbeidsområdet. Følgende alternativer er tilgjengelige:

-   **Bare tilordnede oppgaver** – Brukeren ser bare oppgavene som er tilordnet ham eller henne.
-   **Alle oppgaver og status** – Brukeren ser alle avslutningsoppgaver og statusen for hele prosessen.

Brukere som har tillatelse til å vise bare de tildelte oppgavene kan ikke legge til oppgaver i oppgavelisten, redigere oppgaver eller fjerne oppgaver fra oppgavelisten.

### <a name="task-areas"></a>Oppgaveområder

Du kan bruke oppgaveområder til å gruppere avslutningsoppgaver i logiske eierskapsområder i organisasjonen. Leverandører, Kunder eller Økonomimodul kan for eksempel brukes som oppgaveområder.

### <a name="calendars"></a>Kalendere

Opprett og Rediger økonomiske avsluttende kalendere ved hjelp av kategorien kalendere.  Dette er der du vil definere virkedager for lukking av prosesser, og vil bli brukt til planlegging av oppgaver for lukking.  Opprette en ny kalender, og angi arbeidsdager som skal brukes for aktivitetsplanlegging av.  Det er best å opprette en kalender for lang periode, for eksempel et år eller flere år, siden det kan redigeres etter oppretting.  Når du har opprettet kalenderen, klikker du Rediger-knappen for å oppdatere kalenderen for bestemte dager, for eksempel ferier.  Lukke aktiviteter planlegges på dager når verdien for kontrollen er satt til åpen.  Hvis lukke aktiviteter ikke skal planlegge på en bestemt dag, bør denne dagen har kontroll-verdien som er angitt til lukket.

### <a name="templates"></a>Maler

Du bruker en økonomisk Lukk mal til å definere alle aktiviteter som er del av en avsluttende prosess. En avsluttende oppgave er en regelmessig innsats for arbeid som er tilordnet til en person å fullføre som en del av hver prosess for lukking. I malen, en relativ forfallsdato dato må defineres for hver aktivitet i avsluttende. Den relative forfallsdatoen dato er antallet dager før eller etter den definerte periodens slutten dato som aktiviteten vil bli forfaller hver periode. En forfallstidspunktet også er tildelt hver aktivitet. Forfallstidspunktet angis ved hjelp av konteksten til din tidssone, og vil bli konvertert til tidssonen for hver bruker. 

Du kan tilordne en oppgave i malen til ett eller flere firmaer der dette gjelder. Hvis en annen person er tilordnet til å fullføre arbeidet innsatsen i hvert firma, kan det være nyttig å opprette flere aktiviteter for den samme innsatsen for arbeid. Opprett én oppgave for hvert firma. 

Den **aktivitetskobling** er knyttet til aktiviteten arbeid innsats og kan brukes til å gå direkte til den tilknyttede siden fra aktivitetskoblingen i arbeidsområdet. For eksempel en avsluttende oppgave skal kjøre valuta omvurdering for leverandører kan kobles til den tilknyttede **revaluering av utenlandsk valuta** -siden i Microsoft Dynamics 365 for operasjoner. Du kan også koble til en ekstern nettadresse. 

> [! Tips] Hvis du vil koble en bestemt Management Reporter-rapport til en økonomisk periode Lukk aktivitet, kan du bruke rapporten URL-adressen. Hvis du vil ha tilgang til URL-adressen for rapporten, åpner du rapporten i report designer, og klikk deretter **fil**&gt;**vise rapporten** å åpne rapporten i en webleser. Du kan deretter kopiere nettadressen i adresselinjen i nettleseren, og lime den inn i feltet **Nettadresse til** **oppgavekobling**. 

Du kan definere aktivitetsavhengigheter i malen. Hvis en aktivitet er satt opp, avhenger av én eller flere aktiviteter, kan aktiviteten ikke merkes som fullført før alle avhengigheter er fullført. 

Du kan opprette flere økonomiske Lukk maler. Du kan deretter bruke ulike maler til å spore de avsluttende prosessene for perioden forskjellig, for eksempel måned slutten eller slutten av året, eller spore firmaer som bruker forskjellige avsluttende prosesser. Når du oppretter en mal, kan du kopiere den til en ny mal og foreta de nødvendige endringene. Du kan tilordne bare én mal til hver avsluttende tidsplan.

### <a name="closing-schedules"></a>Lukkingstidsplaner

Du kan bruke en avsluttende plan til å tilordne en økonomisk Lukk mal til en bestemt økonomisk periode som må lukkes. Oppgaver fra malen deretter genereres automatisk for den angitte perioden, og den nye tidsplanen for lukking er lagt til i arbeidsområdet. Når du oppretter en ny plan for lukking av **sluttdato for perioden** feltet brukes til å fastslå den faktiske forfallsdatoen sluttdatoene for aktivitetene lukking, basert på den relative forfallsdatoen dato som er tilordnet i økonomiske Lukk malen. 

Tilordne kalender som er egnet for lukking planen, for å angi arbeidsdager som skal brukes ved aktivitetsplanlegging av. Hvis du ikke definerer en bestemt kalender, forfallsdatoene datoer vil bruke alle dager i uken. 

Du må også definere selskapene som skal knyttes til den avsluttende tidsplanen. Hvis malen oppgavene tilordnes til flere firmaer, opprettes separate oppgaver for hvert firma som er i avsluttende tidsplanen og tildelt aktiviteten mal. 

Etter en tidsplan for lukkingen er fullført, velger du **lukket** alternativ for den. Oppgaveloggen vil fremdeles være tilgjengelig fra den **alle finansperiode Lukk aktiviteter** listeside, men lukking-tidsplanen, fjernes fra arbeidsområdet. Etter at en lukking tidsplan er merket som **lukket**, du kan ikke legge til aktiviteter, redigere aktiviteter eller fjerne oppgaver fra den.


