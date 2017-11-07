---
title: "Arbeidsområde for regnskapsperiodeavslutning"
description: "Denne artikkelen gir en oversikt over arbeidsområdet for regnskapsperiodeavslutning og den tilknyttede konfigurasjonen."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0bbf8f979aeb8b861164e345f9e46bb396f370ce
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="financial-period-close-workspace"></a>Arbeidsområde for regnskapsperiodeavslutning

[!include[banner](../includes/banner.md)]


Denne artikkelen gir en oversikt over arbeidsområdet for regnskapsperiodeavslutning og den tilknyttede konfigurasjonen.

Arbeidsområde for regnskapsperiodeavslutning

I arbeidsområdet **Regnskapsperiodeavslutning** kan du spore prosessene for regnskapsavslutning på tvers av firmaer, områder og personer. Avhengig av visningen av arbeidsområdet **Regnskapsperiodeavslutning** vil du se alle oppgaver og statuser for en avslutningstidsplan eller bare oppgavene som er tilordnet til deg. 

Du må først velge en avslutningstidsplan øverst i arbeidsområdet. Alle data som vises i arbeidsområdet, blir deretter filtrert etter den valgte avslutningstidsplanen.

### <a name="summary-tiles"></a>Sammendrag-fliser

**Sammendrag**-flisene gir en oversikt over prosessen, og indikatorer hjelper deg med å holde oversikt over sluttprosessen. Du kan se oppgaver som er forfalt, gjenværende oppgaver for i dag, oppgaver som forfaller i dag, men er blokkert på grunn av avhengigheter og alle gjenværende oppgaver for prosessen. Denne informasjonen er for alle firmaer som er inkludert i den valgte avslutningstidsplanen.

### <a name="tasks-and-status-section"></a>Delen Oppgaver og status

I inndelingen **Oppgaver og status** er statusen for den overordnede avslutningstidsplanen delt inn på forskjellige måter: status etter firma, status etter område og status etter person som er ansvarlig. Du kan vise statusen for alle oppgaver i avslutningstidsplanen, bare oppgaver som forfaller i dag eller oppgaver som er forfalt, ved å endre filteret øverst på kortlisten. Du kan også velge firmafilteret for å vise statusen for et bestemt firma. Hver statuskategori gir en detaljert oversikt over både prosenten som er fullført og hvor mange oppgaver som gjenstår. Klikk kortet eller handlingen **Vis detaljer om** for å filtrere den detaljerte oppgavelisten etter det valgte kortet. 

Den siste kategorien er for den detaljerte oppgavelisten. Denne listen viser hele oppgavelisten og kan filtreres slik at den viser bare viser oppgavene som du er interessert i. Du kan filtrere listen over oppgaver på flere måter. Du kan for eksempel filtrere etter forfallsdato for oppgave, tilknyttet firma og tilknyttet området. Du kan også velge å vise eller skjule fullførte oppgaver i oppgavelisten. 

To indikatorer brukes for oppgaver:

-   Et utropstegnikon angir at oppgaven er forfalt. Forfallsdatoen er også uthevet i rødt for aktiviteter som har forfalt.
-   En hengelåsikon angir at oppgaven er avhengig av andre aktiviteter som ikke er fullført ennå. En oppgave som er blokkert av avhengigheter, kan ikke merkes som fullført. Du kan angi avhengigheter for en oppgave ved hjelp av handlingen **Angi avhengighet**.

Oppgavenavnet er en hyperkobling til Microsoft Dynamics 365 for Operations-siden eller en annen nettside brukeren må gå til for å fullføre arbeidet. Du kan angi denne hyperkoblingen ved hjelp av **Oppgavekobling**-feltet når du redigerer eller oppretter en oppgave. 

Du kan knytte filer, notater, bilder og nettadresser til en oppgave ved hjelp av handlingen **Vedlegg**. Du kan for eksempel angi journalnumre som brukes som en del av en oppgave, legge til kommentarer om en bestemt oppgave eller legge ved en rapportfil som ble skrevet ut for en oppgave. Et ikon vises i **Vedlegg**-kolonnen for oppgaven hvis det finnes et vedlegg. 

Alternativet **Oppgave fullført** må velges manuelt etter at oppgaven er fullført. Når en oppgave er merket som fullført, oppdateres feltet **Fullføringsdato** automatisk til gjeldende dato og klokkeslett. Avhengighetsindikatorer oppdateres også etter behov.

## <a name="all-financial-period-close-tasks-list-page"></a>Listeside for alle oppgaver ved regnskapsperiodeavslutning
Du kan vise alle gjeldende og forrige periodes avslutningsoppgaver fra listesiden **Alle oppgaver ved regnskapsperiodeavslutning**. Denne listesiden bør brukes for historiske analyse av avslutningsprosessen, fordi den inneholder informasjon om den planlagte forfallsdato, den faktiske sluttdatoen og personen som fullførte oppgaven. Du kan enkelt eksportere informasjonen på denne listesiden til Microsoft Excel for rapportering og revisjon.

## <a name="financial-period-close-configuration-page"></a>Side for konfigurasjon av regnskapsperiodeavslutning
Før du kan bruke arbeidsområdet **Regnskapsperiodeavslutning**, må du konfigurere prosessen i Microsoft Dynamics 365 for Finance and Operations ved hjelp av siden **Konfigurasjon av regnskapsperiodeavslutning**. (Klikk **Økonomimodul** &gt; **Periodeavslutning** &gt; **Konfigurasjon av regnskapsperiodeavslutning**.)

### <a name="resources"></a>Ressurser

I kategorien **Ressurser** definerer du personene som er involvert i avslutningsprosessene. Alle ansatte som skal være ansvarlige for en avslutningsoppgave, må først tilordnes her. Du må også angi den ansattes visning av arbeidsområdet. Følgende alternativer er tilgjengelige:

-   **Bare tilordnede oppgaver** – Brukeren ser bare oppgavene som er tilordnet ham eller henne.
-   **Alle oppgaver og status** – Brukeren ser alle avslutningsoppgaver og statusen for hele prosessen.

Brukere som har tillatelse til å vise bare de tildelte oppgavene kan ikke legge til oppgaver i oppgavelisten, redigere oppgaver eller fjerne oppgaver fra oppgavelisten.

### <a name="task-areas"></a>Oppgaveområder

Du kan bruke oppgaveområder til å gruppere avslutningsoppgaver i logiske eierskapsområder i organisasjonen. Leverandører, Kunder eller Økonomimodul kan for eksempel brukes som oppgaveområder.

### <a name="calendars"></a>Kalendere

Opprett og rediger finansielle avslutningstidsplaner ved hjelp av kategorien Kalendere. Her definerer du arbeidsdager for avsluttende prosesser, og den vil brukes til å planlegge avslutningsoppgaver.  Opprett en ny kalender, og angi virkedagene som skal brukes for oppgaveplanlegging.  Det er best å opprette en kalender for lengre tidsrom, for eksempel ett eller flere år, siden dette kan redigeres etter oppretting.  Når du har opprettet kalenderen, klikker du Rediger-knappen for å oppdatere kalenderen for bestemte dager, for eksempel ferier.  Avslutningsoppgaver planlegges på dager Kontrollverdi er satt til Åpen.  Hvis du avslutningsoppgaver ikke skal planlegges på en bestemt dag, må Kontrollverdi være satt Lukket.

### <a name="templates"></a>Maler

Du kan bruke en mal for regnskapsavslutning til å definere alle oppgaver som er en del av en avslutningsprosess. En avslutningsoppgave er en gjentakende arbeidsinnsats som er tilordnet til en person for fullføring som en del av hver avslutningsprosess. I malen må det være definert en relativ forfallsdato for hver avslutningsoppgave. Den relative forfallsdatoen er antall dager før eller etter den definerte periodesluttdatoen som oppgaven forfaller på for hver periode. Et forfallstidspunkt tilordnes også til hver oppgave. Forfallstidspunktet angis ved hjelp av konteksten til din tidssone, og konverteres til tidssonen for hver bruker. 

Du kan tilordne en oppgave i malen til ett eller flere firmaer der denne oppgaven gjelder. Hvis en annen person er tilordnet for å fullføre arbeidsinnsatsen i hvert firma, kan det være nyttig å opprette flere oppgaver for den samme arbeidsinnsatsen. Opprett én oppgave for hvert firma. 

Menyelementet **Oppgavekobling** er tilknyttet arbeidsinnsatsen for oppgaven og kan brukes til å gå direkte til den tilknyttede siden fra oppgavekoblingen i arbeidsområdet. En avslutningsoppgave som for eksempel skal kjøre prosessen for revaluering av valuta for leverandører, kan kobles til den tilknyttede siden **Revaluering av utenlandsk valuta** i Enterprise-utgaven av Microsoft Dynamics 365 for Finance and Operations. Du kan også koble til en ekstern nettadresse. 

> Tips: Hvis du vil koble en spesifikk Management Reporter-rapport til en oppgave ved regnskapsperiodeavslutning, kan du bruke nettadressen for rapporten. Hvis du vil ha tilgang til nettadressen for rapporten, åpner du rapporten i rapportutformingen, og deretter klikker du **Fil** &gt; **Vis rapport** for å åpne rapporten i en nettleser. Du kan deretter kopiere nettadressen i adresselinjen i nettleseren, og lime den inn i feltet **Nettadresse til** **oppgavekobling**. 

Du kan definere oppgaveavhengigheter i malen. Hvis en oppgave er definert til å være avhengig av én eller flere oppgaver, kan den ikke merkes som fullført før alle avhengigheter er fullført. 

Du kan opprette flere maler for regnskapsavslutning. Du kan deretter bruke de forskjellige malene til å spore avslutningsprosessene for forskjellige periodetyper, for eksempel månedsavslutning eller årsavslutning, eller til å spore firmaer som bruker de forskjellige avslutningsprosesser. Når én mal er opprettet, kan du kopiere den til en ny mal og gjøre de nødvendige endringene. Bare én mal kan tilordnes hver avslutningstidsplan.

### <a name="closing-schedules"></a>Lukkingstidsplaner

Du kan bruke en avslutningstidsplan til å tilordne en mal for regnskapsavslutning til en bestemt regnskapsperiode som skal avsluttes. Oppgavene fra malen genereres deretter automatisk for den angitte perioden, og den nye avslutningstidsplanen blir lagt til arbeidsområdet. Når du oppretter en ny avslutningstidsplan, brukes feltet **Periodens sluttdato** til å fastsette de faktiske forfallsdatoene for avslutningsoppgavene, basert på den relative forfallsdatoen som er tilordnet i malen for regnskapsavslutning. 

Tilordne den aktuelle kalenderen til avslutningstidsplanen for å angi virkedager som skal brukes ved oppgaveplanleggingen. Hvis du ikke definerer en bestemt kalender, bruker forfallsdatoene for oppgavene alle ukedagene. 

Du må også definere firmaene som skal knyttes til avslutningstidsplanen. Hvis maloppgaver tilordnes til flere firmaer, blir det opprettet separate oppgaver for hvert firma som er i avslutningstidsplanen, og de blir tildelt maloppgaven. 

Når en avslutningstidsplan er fullført, velger du alternativet **Lukket** for den. Oppgaveloggen vil fortsatt være tilgjengelig fra listesiden **Alle oppgaver ved regnskapsperiodeavslutning**, men avslutningstidsplanen vil bli fjernet fra arbeidsområdet. Når en avslutningstidsplan er merket som **Lukket**, kan du ikke legge til oppgaver i den, redigerer oppgaver eller fjerne oppgaver fra den.




