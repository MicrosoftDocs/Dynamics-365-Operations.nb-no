---
title: Hva er nytt eller endret i Dynamics 365 Talent (9. april 2019)?
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0a4d4de6cf28e24d1265395d6440df85edf71a0d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462169"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-9-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (9. april 2019)?

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Lifecycle Services-integrasjon med "rapporter et problem"
Problemer som er logget av sluttbrukere som bruker rapporter-et-problem-funksjonen i Attract og Onboard, oppretter nå automatisk kundestøtteproblemer i kundens LCS-prosjekt. Administratorer kan deretter sortere problemene og sende dem til Microsoft når det er nødvendig. Dette er konsekvent med hvordan Core HR behandler kundestøtteproblemer for sluttbrukeren.

### <a name="relevance-search"></a>Relevanssøk
I talentsamlinger kan du nå søke i hele kandidatdatabasen etter bestemt kompetanse, navn eller utdanningsbakgrunn. Du trenger ikke lenger å angi hvilken del av kandidatprofilen du vil søke gjennom. Attract søker i hele profilen og uthever alle treff som blir funnet. Attract søker også i alle dokumenter som er tilgjengelige for en kandidat, og rangerer søkeresultatene på en intelligent måte. I tillegg kan du filtrere resultatene etter kilde eller om de er innstilt som nummer to. Hvis du vil ha mer informasjon, se [Søke etter og vise kandidatprofiler](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-talent-pools#search-and-view-candidate-profiles).

### <a name="prospect-recommendations"></a>Kandidatanbefalinger
Attract kan kickstarte rekrutteringen til en jobb så snart du aktiverer den ved å foreta intelligente kandidatanbefalinger fra organisasjonens kandidatdatabasen. Anbefalingene inkluderer kompetanse- og utdanningsinformasjonen som ble identifisert under søking etter relevante kandidater. Disse anbefalingene vises i kategorien **Jobbkandidater** under en jobb hvis du aktiverer den under jobbansettelsesprosessen. Hvis du vil ha mer informasjon, kan du se [Kandidatanbefalinger](https://docs.microsoft.com/dynamics365/unified-operations/talent/intelligent-recommendations#prospect-recommendations).

### <a name="interviewer-availability-statuses"></a>Tilgjengelighetsstatus for intervjuer
Intervjuplanleggere vil snart kunne se **Fraværende, arbeider fra et annet sted**-statuser for intervjuerne, for å planlegge tider som kan fungere bedre for intervjuerne.

### <a name="candidate-interview-experience-save-calendar-invites"></a>Kandidatintervjuerfaring: Lagre kalenderinvitasjoner
Kandidater kan nå laste ned og lagre intervjuhendelser i de personlige kalenderne ved hjelp av en ICS-fil som er knyttet til e-postmeldingen for intervjusammendraget som sendes til kandidaten.

## <a name="changes-in-onboard"></a>Endringer i Onboard

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Lifecycle Services-integrasjon (LCS) med "rapporter et problem"
Problemer som er logget av sluttbrukere som bruker rapporter-et-problem-funksjonen i Attract og Onboard, oppretter nå automatisk kundestøtteproblemer i kundens LCS-prosjekt. Administratorer kan deretter sortere problemene og sende dem til Microsoft når det er nødvendig. Dette er konsekvent med hvordan Core HR behandler kundestøtteproblemer for sluttbrukeren.

## <a name="changes-in-core-hr"></a>Endringer i Core HR
Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2225.

### <a name="percent-of-basis-variable-plans-load-incorrect-amount"></a>Prosent av grunnleggende variable planer laster inn feil beløp
Denne ukens versjon korrigerer et problem ved lasting av variabel kompensasjon når det brukes prosent av basisplaner.
 
### <a name="date-picker-on-last-day-worked-doesnt-work-correctly"></a>Datovelger for siste arbeidsdag fungerer ikke riktig
Denne endringen løser problemet: Når brukere redigerer **Sluttdato for ansettelse** og velger datoen ved hjelp av kalenderkontrollen, legges det til en dag i utvalget.

###  <a name="limit-personnel-action-types-by-the-action-taken"></a>Begrense personalhandlingstyper ved handlingen som utføres
Denne endringen begrenser handlingstypene som vises når det utføres bestemte handlinger. Når for eksempel en ny stilling forespørres, vises bare handlinger for den nye stillingen i listen over handlinger som skal velges. Tidligere viste både nye handlinger og redigeringshandlinger. 

### <a name="transferring-an-employee-with-compensation-in-a-second-legal-entity"></a>Overføring av en ansatt med kompensasjon i en annen juridisk enhet
Denne versjonen tillater at kompensasjon avsluttes i en annen juridisk enhet hvis overføringen er på tvers av firmaer.

### <a name="unable-to-select-compensation-for-a-future-employment-during-a-transfer"></a>Kan ikke velge kompensasjon for en fremtidig ansettelse under en overføring
Når du overfører en ansatt til en ny juridisk enhet, kan du nå angi kompensasjon for den nye juridiske enheten under overføringsprosessen.

### <a name="user-isnt-able-to-assign-compensation-during-position-assignment"></a>Brukeren kan ikke tildele kompensasjon under stillingstilordning
Ved tillegging av en ny stillingstilordning kan du nå definere poster for fast kompensasjon. 

## <a name="in-preview"></a>I forhåndsvisning

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Tillate angivelse av årsakskoder for permisjonstyper
Organisasjoner må kanskje ha tilleggsinformasjon om fraværsforespørsler. Du kan nå angi årsakskoder for fraværstyper og gi de ansatte mulighet til å velge en årsakskode i fraværsforespørsler.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Kreve årsakskoder for bestemte fraværstyper i forespørsler om fravær
Organisasjoner kan kreve årsakskoder for bestemte fraværstyper når ansatte sender fraværsforespørsler. Dette kan være på grunn av firmapolicy eller lovbestemte krav. Du kan nå angi hvilke permisjonstyper som krever en årsakskode, og du kan kreve at ansatte må angi en årsakskode for fraværstypen i forespørsler om fravær.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Angi transaksjonsliste for permisjon og fravær for HR
Sporing av ansattes fravær og forståelse av hvordan fravær beregnes, hjelper ikke bare HR med å svare på ansattspørsmål, men sørger også for nøyaktige fraværstildelinger for ansatte. HR har nå en ny oversikt over transaksjonene (tildelinger, avsetninger, justeringer og forespørsler), slik at det er mulig å vise årsakene bak saldoer. 

## <a name="coming-soon"></a>Kommer snart

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Forbedringer av brukergrensesnittet for kontroll av dupliserte ansatte
Med denne endringen oppdages duplikater når du angir navnefelt, og statusen viser hvor mange duplikater som ble funnet. Du kan velge den angitte lenken for å åpne en ny side for å vurdere om du vil bruke resultatet som ble funnet. For å unngå å forstyrre dataregistreringen åpnes duplikatskjemaet ikke automatisk.

###  <a name="email-support-for-alerts"></a>E-poststøtte for varsler
Med Platform update 25 for Finance and Operations kan brukere opprette varslingsregler som automatisk leverer e-postmeldinger til kontakter når de utløses av en hendelse. 
