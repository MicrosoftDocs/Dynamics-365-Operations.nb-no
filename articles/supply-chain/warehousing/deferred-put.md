---
title: Utsatt behandling av lagerarbeid
description: Dette emnet beskriver funksjonaliteten som gjør utsatt behandling av plasseringsoperasjoner for lagerarbeidet tilgjengelig i Microsoft Dynamics 365 for Finance and Operations.
author: josaw1
manager: AnnBe
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-6-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4905084f9bc28e55c307921280733c6acb80db86
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863592"
---
# <a name="deferred-processing-of-warehouse-work"></a>Utsatt behandling av lagerarbeid

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/pivate-preview-banner.md)]

Dette emnet beskriver funksjonaliteten som gjør utsatt behandling av plasseringsoperasjoner for lagerarbeid tilgjengelig i Microsoft Dynamics 365 for Finance and Operations.

Den utsatte behandlingsfunksjonaliteten lar lagerarbeidere fortsette å utføre annet arbeid mens plasseringsoperasjonen behandles i bakgrunnen. Utsatt behandling er nyttig når mange arbeidslinjer må behandles, og arbeideren kan la dette arbeidet behandles asynkront. Det er også nyttig når serveren kan ha ad hoc eller ikke-planlagte økninger i behandlingstiden, og den økte behandlingstiden kan påvirke brukerens produktivitet.

Bakgrunnsbehandling oppnås ved å bruke SysOperation-rammeverket. For mer informasjon, se [Oversikt over SysOperation-rammeverket](https://docs.microsoft.com/dynamicsax-2012/developer/sysoperation-framework-overview).

## <a name="configuring-the-work-processing-policies"></a>Konfigurere policyer for arbeidsbehandling

Hvis du vil bruke utsatt behandling, må du konfigurere og bruke en policy for arbeidsbehandling.

Policyer konfigureres på siden **Arbeidsbehandlingspolicyer**. Følgende tabell beskriver feltene på denne siden.

| Felt                           | Beskrivelse |
|---------------------------------|-------------|
| Navn på arbeidsbehandlingspolicy     | Navnet på arbeidsbehandlingspolicyen. |
| Arbeidsordretype                 | Arbeidsordretypen som policyen gjelder for. |
| Operasjon                       | Operasjonen som behandles ved hjelp av policyen. |
| Arbeidsbehandlingsmetode          | Metoden som brukes til å behandle arbeidslinjen. Hvis metoden er satt til **Umiddelbar**, ligner virkemåten når ingen arbeidsbehandlingspolicyer brukes til å behandle linjen. Hvis metoden er satt til **Utsatt**, brukes utsatt behandling som bruker det satsvise rammeverket. |
| Terskel for utsatt behandling   | Verdien **0** (null) angir at det finnes ikke noen terskel. I dette tilfellet brukes utsatt behandling hvis den kan brukes. Hvis den spesifikke terskelberegningen er under terskelen, brukes den umiddelbare metoden. Ellers brukes den utsatte metoden hvis den kan brukes. For salgs- og overføringsrelatert arbeid beregnes terskelen som antall tilknyttede kildelastlinjer som behandles for arbeidet. For etterfyllingsarbeid beregnes terskelen som antall arbeidslinjer som etterfylles av arbeidet. Ved å angi en terskel på, for eksempel **5** for salg, vil mindre arbeid som har færre enn fem første kildelastlinjer, ikke bruke utsatt behandling, men større arbeide vil bruke den. Terskelen har bare en effekt hvis metoden for arbeidsbehandling er satt til **Utsatt**. |
| Satsvis gruppe for utsatt behandling |Den satsvise gruppen som brukes for behandling. |

## <a name="assigning-the-work-creation-policy"></a>Tilordne policyen for arbeidsopprettelse

Policyen for arbeidsopprettelse kan tilordnes i lagerstyringsparameterne. Det kan også tildeles på nivå med individuelle lagre. Hvis policyen er tilordnet et lager, brukes den bare på arbeid som er opprettet for dette lageret. Hvis ingen policy er tilordnet på lagernivå, brukes policyen fra lagerstyringsparameterne.

## <a name="viewing-the-deferred-put-processing-tasks"></a>Vise behandling av utsatte plasseringsoppgaver

Du kan vise utsatte plasseringsoppgaver på siden **Utsatte plasseringsoppgaver**.

Som standard vises **fullførte** oppgaver.

| Felt            | Beskrivelse |
|------------------|-------------|
| Status           | Statusen for oppgaven. |
| Status for satsvis jobb | Statusen til den relaterte satsvise jobben. Hvis den satsvise jobben er behandlet, inneholder loggen for den selve loggen og informasjonen fra den satsvise jobben. |

Her er en forklaring av de mulige statusene:

- **Venter** – den relaterte satsvise jobben venter på behandling på den satsvise serveren.
- **Mislyktes** – behandlingen mislyktes. Aktiviteten kan behandlesp på nytt ved hjelp av handlingen **Behandle utsatt plassering**, eller den kan avbrytes ved hjelp av handlingen **Avbryt utsatt plassering**.
- **Fullført** – jobben ble fullført.

## <a name="impact-on-closed-work-dates"></a>Innvirkning på lukkede arbeidsdatoer

Når utsatt plasseringsbehandling brukes, er den lukkede arbeidsdatoen angitt som opprettet dato/klokkeslett for de utsatte plasseringsoppgavene. Den lukkede arbeidsdatoen brukes fordi dette er det beste estimatet for når plasseringsoperasjonen ble fullført.

## <a name="reprocessing-a-failed-task"></a>Bearbeiding av en mislykket oppgave

Du kan behandle en mislykket oppgave på nytt ved å velge den på siden og deretter velge **Behandle utsatt plassering**. Bearbeiding tilsvarer en situasjon hvor brukeren fullfører plasseringen fra den mobile enheten som om den var innstilt for umiddelbar behandling.

## <a name="canceling-failed-tasks"></a>Avbryte mislykkede oppgaver

Bare mislykkede oppgaver kan avbrytes. Når du avbryter en oppgave, kan du tilordne den til en ny bruker. Oppgaven kan også forbli tilordnet til brukeren som behandlet arbeidet. Avbrudd tilsvarer en situasjon der arbeidet bringes tilbake til den mobile enheten som om den siste plukketrinnet var nettopp fullført, og arbeidet må settes bort. Brukeren vil imidlertid kunne fastslå at arbeidet er "annerledes", fordi det bare vil ha et plasseringstrinn, og plasseringen vil tilsvare plasseringen som den første brukeren som behandlet arbeidet, hadde som en endelig plassering.

Når en oppgave avbrytes, blokkeres ikke lenger arbeidet av blokkeringsårsakenen til den utsatte plasseringsbehandlingen. Den kan bearbeides ved hjelp av mobilenheten.

Oppgaveoppføringen slettes når aktiviteten ble avbrutt.

## <a name="configuring-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Konfigurere menyen på mobilenheten for å hoppe over den utsatte behandlingspolicyen

Du kan konfigurere menyelementet for mobilenheten slik at den utsatte behandlingspolicyen ikke brukes. Arbeidet blir deretter behandlet som det er når ingen utsatt behandlingspolicy er brukt. Denne funksjonen lar en leder bruke et bestemt menyelement der utsatt plassering ikke brukes. Hvis du vil konfigurere dette, kan du angi feltet **Policy for utsatt plasseringsbehandling** til **Overstyr innstilinger og behandle plassering synkront**. 

## <a name="restrictions-when-the-deferred-put-processing-isnt-applied"></a>Begrensninger når utsatt plasseringsbehandling ikke brukes

Det er flere scenarioer der utsatt plasseringsbehandling ikke brukes, selv om policyen er konfigurert. Her er noen eksempler:

- Manuell arbeidsfullføring brukes.
- Arbeidet er fullført ved hjelp av autofullføring.
- Revisjonsmaler brukes.
- Arbeidet bruker containere.

## <a name="monitoring-the-deferred-processing-tasks-from-the-outbound-work-monitoring-workspace"></a>Overvåke utsatte behandlingsoppgaver fra arbeidsområdet for overvåking av utgående arbeid

Arbeidsområdet **Overvåking av utgående arbeid** har to fliser som hjelper deg med å overvåke utsatte plasseringsoppgaver:

- **Mislykkede utsatte plasseringsoppgaver** – denne flisen viser antall mislykkede oppgaver. Hvis det finnes mislykkede oppgaver, må lagerlederen enten behandle dem på nytt eller avbryte dem, fordi de ikke blir behandles automatisk.
- **Ventende utsatte plasseringsoppgaver** -denne flisen viser antall oppgaver som har vært i **Venter**-status i mer enn 10 minutter. Hvis flisen viser et tall, kan det tyde på at det oppstod et problem under den satsvise behandlingen. Du kan behandle **ventende** oppgaver manuelt. Hvis den satsvise jobben for en oppgave behandles senere, vil den bare mislykkes fordi den allerede er behandlet. Det blir ingen innvirkning.

## <a name="deleting-completed-tasks"></a>Slette fullførte oppgaver

Du kan slette utsatte plasseringsoppgaver som er fullført, ved å merke dem og slette dem på siden.
