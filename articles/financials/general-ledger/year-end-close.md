---
title: "Årsavslutning"
description: "Dette emnet beskriver den nødvendige konfigurasjonen og fremgangsmåten for å kjøre årsavslutningsprosessen i økonomimodulen."
author: kweekley
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bf9d0a6ab0fcf7d6f5a31813d68f0bd452ce1019
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="year-end-close"></a>Årsavslutning

[!INCLUDE [banner](../includes/banner.md)]

Dette emnet beskriver den nødvendige konfigurasjonen og fremgangsmåten for å kjøre årsavslutningsprosessen i økonomimodulen. 

På slutten av et regnskapsår må du kjøre årsavslutningsprosessen for å overføre åpningssaldoer til det nye året. De fleste organisasjoner vil kjøre årsavslutningsprosessen flere ganger. Første gang vil være for å få saldoene flyttet inn i det nye regnskapsåret. Årsavslutningen kan deretter kjøres på nytt, som mange ganger som nødvendig, for å flytte saldoene fra justeringsposter i det nye regnskapsåret. 

Under årsavslutningsprosessen blir det opprettet to typer mulige transaksjoner. En åpningstransaksjon genereres alltid og brukes til å opprette åpningssaldoene i det nye regnskapsåret. Åpningstransaksjonen viser finanskontosaldoer for balanseregnskapet i det nye regnskapsåret, og saldoer fra finanskontosaldoer for resultat for opptjent egenkapital i det nye regnskapsåret. Avslutningstransaksjonen kan opprettes for å bringe saldoene for resultatkontoer ned til i regnskapsåret som avsluttes.

## <a name="prepare-to-run-the-year-end-close"></a>Klargjøre kjøring av årsavslutning
Før du kjører årsavslutningsprosessen, må du kontrollere innstillingene for følgende: 

På **Hovedkonto**-siden:

-   Kontroller at **Hovedkontotype** er riktig definert for hver av hovedkontoene. Hovedkontotypen brukes til å avgjøre om saldoen for hovedkontoen skal overføres som en startsaldo eller lukkes til opptjent egenkapital i åpningstransaksjonen.
-   Feltet **Åpningskonto** kan brukes til å overføre saldoen for hovedkontoen til en ny hovedkonto under årsavslutningen. Den nye hovedkontoen angis i feltet **Åpningskonto**. Vanligvis brukes dette til hovedkontoer for balanseregnskap når hovedkontoen deaktiveres og en ny hovedkonto brukes for det nye regnskapsåret.

På siden **Parametere for økonomimodul** under **Årsavslutning**:

-   Alternativet **Slett årsavslutningstransaksjoner** brukes til å angi om den systemgenererte åpningstransaksjonen fra en tidligere årsavslutning skal slettes når årsavslutningen kjøres på nytt. Hvis dette alternativet er satt til **Ja**, slettes den forrige åpningstransaksjonen og en ny åpningstransaksjon opprettes basert på gjeldende saldoer. Hvis dette alternativet er satt til **Nei**, beholdes den forrige åpningstransaksjonen og en ekstra åpningstransaksjon opprettes for å flytte saldoene fremover fra justeringstransaksjoner som er postert etter den forrige årsavslutningen.
-   Alternativet **Opprett avslutningstransaksjoner under overføring** brukes til å opprette avslutningstransaksjoner i regnskapsåret som lukkes, for å bringe saldoene i resultatkontoene til null. Hvis dette alternativet er satt til **Ja**, opprettes både åpningstransaksjonen og avslutningstransaksjonen. Hvis dette alternativet er satt til **Nei**, opprettes bare åpningstransaksjonen i det neste regnskapsåret for å overføre saldoene. Saldoene for resultatkonti beholdes på slutten av regnskapsåret.
-   Alternativet **Sett regnskapsårsstatusen til permanent lukket** brukes til å angi en permanent lukketstatus for regnskapsåret. Vær forsiktig når du bruker denne innstillingen, fordi alle perioder med permanent lukketstatus ikke kan åpnes på nytt, noe som hindrer postering av justeringer i regnskapsåret. Anbefalt fremgangsmåte er å sette dette til **Nei**.
-   Alternativet **Bilagsnummer må fylles ut** brukes til å definere om et bilagsnummer er nødvendig når du kjører årsavslutningsprosessen. Anbefalt fremgangsmåte er å kreve et bilagsnummer for enkelt å identifisere åpningstransaksjonen.

På siden **Regnskapskalender**:

-   Det neste regnskapsåret må finnes før du kjører årsavslutningen. Det neste regnskapsåret er nødvendig for å opprette startsaldoer i åpningsperioden.

På siden **Finanskalender**:

-   Valgfritt: Hver regnskapsperiode for regnskapsåret som lukkes, kan settes til **På vent** for å hindre at nye transaksjoner registreres. Når justeringsposter er identifisert, kan På vent-periodene åpnes på nytt for å postere justeringsposter, selv om årsavslutningsprosessen allerede er kjørt.

## <a name="define-year-end-close-templates"></a>Definere maler for årsavslutning
Når systemet er konfigurert, kan du kjøre årsavslutningsprosessen. På siden **Årsavslutning** kan en mal defineres for gruppen med juridiske enheter som årsavslutningsprosessen skal kjøres for. Malen brukes på nytt ved hver årsavslutning, men kan endres hvis organisasjonen endres. 

Definer først **gruppenavnet** for malen, og velg regnskapskalenderen. Gruppenavnet må identifisere gruppen med juridiske enheter som er inkludert.  Malen kan for eksempel være definert basert på geografi, med separate grupper opprettet for juridiske enheter for Nord-Amerika, juridiske enheter i EMEA og juridiske enheter i APAC. 

Deretter kan juridiske enheter legges til i malen. Juridiske enheter kan legges ved å velge et organisasjonshierarki eller ved å velge de juridiske enhetene. Hvis det velges et organisasjonshierarki, vil bare juridiske enheter i hierarkiet som bruker den valgte regnskapskalenderen legges til i malen. Hvis du bruker juridiske enheter for å legge til i malen, kan bare juridiske enheter med samme regnskapskalender legges til i malen. Den samme regnskapskalenderen er nødvendig fordi årsavslutningen kjøres ved å velge et regnskapsår, noe som kan variere fra kalender til kalender. 

Når de juridiske enhetene er lagt til, kan du definere hovedkontoer for opptjent egenkapital for hver juridiske enhet. Feltet **Dato for årsavslutning for i fjor** oppdateres hver gang årsavslutningen kjøres for den juridiske enheten. 

Kategorien **Finansdimensjon** brukes til å definere hvilke finansdimensjoner som skal brukes på åpningstransaksjonen. Legg merke til at innstillingene du definerer, bare gjelder for den juridiske enheten som er valgt i rutenettet **Juridiske enheter**. Du gjentar oppsettet for hver juridiske enhet i rutenettet. 

**Overfør balansedimensjoner** brukes til å definere om finansdimensjoner på transaksjoner som er postert til balansekonti, skal beholdes på åpningstransaksjonen. Anbefalt fremgangsmåte er å sette alternativet til **Ja**. **Overfør resultatdimensjoner** brukes til å definere hvilke finansdimensjoner på transaksjoner som er postert til resultatkonti, som skal overføres til hovedkontoen for opptjent egenkapital. Først må du angi finansdimensjonene som er relevante for den valgte juridiske enheten. Dette omfatter alle finansdimensjoner det er postert mot i løpet av året, selv om finansdimensjonen ikke er en del av en aktiv kontostruktur. Deretter definerer du hver dimensjon som **Lukk én** eller **Lukk alle**.  Standard er **Lukk alle**, som beholder de opprinnelige finansdimensjonsverdiene fra posterte transaksjoner, og bruker dem til å lage åpningssaldoer for kontoen for opptjent egenkapital. Separate startsaldoer for opptjent egenkapital opprettes for hver unike kombinasjon av finansdimensjonsverdier. Hvis **Lukk én** er valgt, vil alle transaksjoner som er postert med denne finansdimensjonen blir summert i en startsaldo for opptjent egenkapital for dimensjonsverdien som er angitt i feltet etter **Lukk én**. Anta for eksempel at alle transaksjonene for regnskapsåret ble postert med kontostrukturen Hovedkonto – Avdeling. For Avdeling-finansdimensjonen i malen er **Lukk én** valgt, og 100 er verdien som er angitt. Hvis totalinntekt for alle transaksjoner som er postert til avdeling 200, 300 og 400 er USD 100 000, opprettes det én startsaldo for Tilbakeholdt overskudd – 100. Hvis du velger **Lukk én** og lar finansdimensjonsverdien være tom, vil alle transaksjoner postere til tilbakeholds overskudd med denne dimensjonsverdien tom. 

Årsavslutningsprosessen overholder ikke kontostrukturer. Dette er fordi kontostrukturer kan endres i løpet av et regnskapsår, og det er ikke alltid mulig å identifisere den relevante kontostrukturen på grunn av disse endringene.  Når åpningstransaksjoner opprettes, vil saldoene overføres fremover med finansdimensjoner som er definert i årsavslutningsmalen. Startsaldopostene kan ikke lenger inneholde finansdimensjoner i gjeldende kontostruktur og segmentkombinasjoner som er ikke lenger er gyldig i gjeldende kontostruktur. Hvis organisasjonen vil utelate en finansdimensjon for startsaldoen for tilbakeholdt overskudd, må finansdimensjonen settes til **Lukk én** dimensjonsverdien må være tom.

## <a name="run-the-year-end-close-process"></a>Kjøre årsavslutningsprosessen
Når malene for årsavslutning er opprettet, startes årsavslutningsprosessen ved å velge **Kjør regnskapsår** i handlingsruten. Velg alle eller et delsett med juridiske enheter fra malen som årsavslutningen skal kjøres for. Når du kjører i årsavslutningen for første gang i et regnskapsår, velger du sannsynligvis alle juridiske enheter for å opprette startsaldoer for dem. Hvis du kjører årsavslutningen på nytt, kan du velge å kjøre prosessen for bare juridiske enheter som det ble postert justeringsposter for. 

Velg regnskapsåret som du vil kjøre årsavslutningen mot. Hvis det finnes mer enn én avslutningsperiode for den siste perioden i regnskapsåret, er feltet **Periodenavn** tilgjengelig, slik at du kan velge avslutningsperiode for postering av avslutningstransaksjonen, hvis det er definert i oppsettet å opprette avslutningstransaksjonen. 

Angi et bilagsnummer som kan være nødvendig, avhengig av oppsettet i økonomiparametere. Det samme bilagsnummeret brukes for alle juridiske enheter som er valgt for årsavslutningsprosessen. Bilagsnummeret genereres ikke med en nummerserie. Anbefalt fremgangsmåte er å angi et bilagsnummer selv om det ikke er påkrevd. Angivelse av et bilagsnummer gjør det enklere å finne åpningstransaksjonen i det nye regnskapsåret. Hvis det ikke angis et bilagsnummer, er bilaget tomt for åpningstransaksjonen. 

Hvis du vil tilbakeføre en årsavslutning for et foregående år for det valgte regnskapsåret, setter du **Angre forrige avslutning** til **Ja**. Årsavslutningen tilbakeføres, men prosessen kan kjøres på nytt når som helst. Hvis du tilbakefører en årsavslutning, er ikke **Dato for årsavslutning for i fjor** tilgjengelig. 

Standardinnstillingen for årsavslutningsprosessen er å kjøre i satsvis modus. Anbefalt fremgangsmåte er å kjøre prosessen i satsvis modus, slik at brukeren kan å gå tilbake til andre aktiviteter. Når årsavslutningsprosessen er fullført, oppdateres **Dato for årsavslutning for i fjor** med datoen for økten.

Hvis du vil ha mer informasjon, kan du se [Lukke økonomimodulen ved periodeslutt](close-general-ledger-at-period-end.md) og [Avslutte regnskapsåret](tasks/close-fiscal-year.md).




