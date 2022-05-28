---
title: Behandling av generell journal
description: Dette emnet beskriver funksjoner i Microsoft Dynamics 365 Finance som kan hjelpe å gjøre behandling av økonomijournaler enklere, og som også kan bidra til å sikre at riktige data blir registrert og intern kontroll ikke settes på spill.
author: kweekley
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9cfe4af0c666fb2accb6737edb2de6e0b6e7cdf1
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/06/2022
ms.locfileid: "8720034"
---
# <a name="general-journal-processing"></a>Behandling av generell journal

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjoner som kan hjelpe med å gjøre behandling av økonomijournaler enklere, og som også kan bidra til å sikre at riktige data blir registrert og intern kontroll ikke settes på spill.  

## <a name="journal-names"></a>Journalnavn

Ett av de viktigste områdene å konfigurere er journalnavn. Det er lurt å definere bestemte journalnavn for hvert formål, for eksempel konsernintern, justering av avsetning og korrigering. Du kan tilpasse hvert enkelt journalnavn for å gjøre dataregistrering enkelt og sikker for hvert formål. 

På siden **Journalnavn** kan du definere følgende elementer:

-   **Arbeidsflytgodkjenning** – Hvis du vil øke den interne kontrollen, definerer du journalarbeidsflyter som etablerer materialgrenser for gjennomgangs- og godkjenningstrinnene, basert på kriterier som total debetbeløp. Du konfigurerer arbeidsflyter for økonomijournaler på siden **Arbeidsflyter for økonomimodul**.
-   **Standardverdier** – Velg standardverdier for motkontoer, valuta og finansdimensjoner.
-   **Journalkontroll** – Du kan definere begrensninger for firma, kontotype og segmentverdier. 

**Eksempler**

Et journalnavn kan bare brukes til justeringer. I så fall kan du angi at bare **Finans**-kontotypen er gyldig på tvers av alle firmaer. 

[![Journalkontrollkontotyper.](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Et journalnavn kan bare brukes bare for et bestemt segment eller et område for hovedkontoer. 

[![Journalkontrollsegment.](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

Alternativet **Automatisk tilbakeføring** er tilgjengelig i økonomijournaler. Du har for eksempel en justering av avsetning der det faktiske dokumentet ikke har blitt behandlet ennå, som vist i illustrasjonen nedenfor.
[![Tilbakeføring for økonomijournal.](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Microsoft Excel-tillegget for journaloppføring gir et ekstra nivå med automatisering og gjør dataregistrering enklere. Handlingen **Åpne linjer i Excel** er tilgjengelig på sidene **Økonomijournal** og **Journalbilag**. 

På siden **Periodiske journaler** kan du definere at gjentakelsesjournaler skal automatisere behandlingen av journalen. 

Du kan bruke bilagsmaler til enhver tid. På siden **Økonomijournaler** finnes handlingene **Lagre** og **Velg bilagsmal** på **Journalbilag**-siden, under **Funksjoner** for bilagslinjene.

## <a name="related-setup"></a>Relatert oppsett
Dette oppsettet er ikke spesifikk for økonomijournaler, men vil sørge for at dataregistrering er riktig og enkel.

### <a name="main-account"></a>Hovedkonto

Hovedkontoen oppsettet gir mange muligheter til økonomijournalen behandling:

-   **DK-krav** – Bruk dette alternativet hvis en hovedkontoen er begrenset til debet- eller kredittransaksjoner. Oppsettet kontrolleres når en journal er godkjent eller postert.

-   **Standard motkonto**
-   **Suspendert** – Suspendere en hovedkonto for dataregistrering på tvers av alle firmaer eller for et bestemt firma / en juridisk enhet.
-   **Ikke tillat manuell registrering** – Hindre at brukere manuelt angir en verdi for kontoen i journaler.
-   **Standard / valider valutakoder**
-   **Overstyring for juridisk enhet** – Dette oppsettet er spesifikk for definert firma / juridisk enhet:
    -   **Standard / Valider merverdiavgift**
    -   **Standarddimensjon** – **Ikke fast** eller **Fast verdi**. **Fast verdi** vil bidra til å sørge for at alle posteringer for denne hovedkontoen alltid bruker en dimensjonsverdi som er definert som **Fast**.
-   **Posteringsvalidering**
    -   **Brukervalidering** – Dette alternativet styrer hvilke brukere som har tillatelse til å postere til en hovedkonto.
    -   **Validering av posteringstype** – Dette alternativet styrer hvilke posteringstyper som er tillatt for en hovedkonto.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Regnskapsstrukturer og strukturer for avanserte regler

Regnskapsstrukturer og strukturer for avanserte regler er svært viktige for å sørge for at dataene som er nødvendige for økonomisk rapportering og sporing av ytelse, blir registrert under behandling av økonomijournalen og eventuell dokumentasjon. Regnskapsstrukturer og strukturer for avanserte regler lar deg tilpasse dataregistreringsopplevelsen. Du kan tillate dataregistrering bare for finansdimensjoner som er relevante i hvert tilfelle, og kan også sikre at obligatoriske og nøyaktige data alltid registreres.

Hvis du vil ha mer informasjon, kan du se følgende emner:
- [Planlegge kontoplanen](plan-chart-of-accounts.md) 
- [Opprette avanserte regler for journaler](tasks/create-advanced-rules-journals.md)
- [Opprette en journaloppføring ved hjelp av en mal](tasks/create-journal-entry-template.md)
- [Opprette og validere journaler](tasks/create-validate-journals.md)
- [Postere periodiske journaler](tasks/post-periodic-journals.md)
- [Behandle finansfordelingsjournal](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a>Simuler postering
Du finner **Simuler postering** på **Valider**-menyen for de fleste journaler. Når du validerer en journal ved hjelp av **Valider**-funksjonen, tester systemet journalen for bestemte feiltilstander. Hvis du bruker funksjonen **Simuler postering**, vil systemet kjøre alle de samme prosessene som kjøres under postering, uten faktisk å postere journalen. Du kan deretter se gjennom posteringsmeldingene som vises, korrigere eventuelle feil du finner, og deretter åpne **Poster**-menyen for å postere journalen. 

**Simuler postering** er ikke tilgjengelig for partiprosessering. Det finnes imidlertid tilgjengelig kode for å simulere postering i parti, og utviklere kan utvide koden for å legge til denne funksjonaliteten.  

## <a name="journal-unlock"></a>Lås opp journal
En knapp er tilgjengelig på Journal-siden for å låse opp en journal som har statusen "Sperret av systemet" satt til Ja. Denne opplåsingen kan utføres av en systemadministrator som har analysert alle satsvise jobber og bekreftet at denne journalen ikke lenger behandles av en satsvis jobb. Denne knappen aktiveres av funksjonen **Logg opp journal** på siden **Funksjonsbehandling**. 

## <a name="workflow-recall"></a>Tilbakekall arbeidsflyt 
Muligheten til å tilbakekalle en journal i en arbeidsflyt som har statusen uopprettelig, aktiveres ved hjelp av **Arbeidsflyt**-knappen i en journal og på siden **Arbeidsflytlogg**. Dette aktiveres av funksjonen kalt **Tilbakestille arbeidsflytstatusen for journaler** på siden **Funksjonsbehandling**.

## <a name="delete-journal-lines"></a>Slett journallinjer
Muligheten til å slette alle journallinjer raskt aktiveres i en journal under **Funksjoner** > **Slett journallinjer**. Hvis du vil aktivere denne funksjonen, velger du **Slett ytelsesoptimaliseringer for journal** under **Funksjonsbehandling**. Denne funksjonen påvirker utvidelsene i tabellen **LedgerJournalTrans**, og **Slett**-metoden for den, siden linjesettet fjernes uten at **Slett**-metoden for hver linje kalles opp. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
