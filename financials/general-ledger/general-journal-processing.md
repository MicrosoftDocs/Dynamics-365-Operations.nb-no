---
title: Behandling av generell journal
description: "Denne artikkelen beskriver funksjoner i Microsoft Dynamics 365 for Operations som kan hjelpe med å gjøre behandling av generell enklere, og som også kan bidra til å sikre at riktige data blir registrert og intern kontroll ikke settes på spill."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 50cd203025be8857de943e458fc32315e494fb7a
ms.lasthandoff: 03/31/2017


---

# <a name="general-journal-processing"></a>Behandling av generell journal

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver funksjoner i Microsoft Dynamics AX som kan hjelpe med å gjøre behandling av generell enklere, og som også kan bidra til å sikre at riktige data blir registrert og intern kontroll ikke settes på spill.  

Journalnavn

Ett av de viktigste områdene å konfigurere er journalnavn. Det er lurt å definere bestemte journalnavn for hvert formål, for eksempel konsernintern, justering av avsetning og korrigering. Du kan tilpasse hvert enkelt journalnavn for å gjøre dataregistrering enkelt og sikker for hvert formål. 

På siden **Journalnavn** kan du definere følgende elementer:

-   **Arbeidsflytgodkjenning** – Hvis du vil øke den interne kontrollen, definerer du journalarbeidsflyter som etablerer materialgrenser for gjennomgangs- og godkjenningstrinnene, basert på kriterier som total debetbeløp. Du konfigurerer arbeidsflyter for økonomijournaler på siden** Arbeidsflyter for økonomimodul**.
-   **Standardverdier** – Velg standardverdier for motkontoer, valuta og finansdimensjoner.
-   **Journalkontroll** – Du kan definere begrensninger for firma, kontotype og segmentverdier. 

**Eksempler**

Et journalnavn kan bare brukes til justeringer. I så fall kan du angi at bare **Finans**-kontotypen er gyldig på tvers av alle firmaer. [![Journalkontrollkontotyper](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Et journalnavn kan bare brukes bare for et bestemt segment eller et område for hovedkontoer. [![Journalkontrollsegment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

Alternativet **Automatisk tilbakeføring** er tilgjengelig i økonomijournaler. Du har for eksempel en justering av avsetning der det faktiske dokumentet ikke har blitt behandlet ennå, som vist i illustrasjonen nedenfor.
[![Tilbakeføring for økonomijournal](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Microsoft Excel-tillegget for journaloppføring gir et ekstra nivå med automatisering og gjør dataregistrering enklere. Handlingen **Åpne linjer i Excel** er tilgjengelig på sidene **Økonomijournal** og **Journalbilag**. 

På siden **Periodiske journaler** kan du definere at gjentakelsesjournaler skal automatisere behandlingen av journalen. 

Du kan bruke bilagsmaler til enhver tid. På siden **Økonomijournaler** finnes handlingene **Lagre** og **Velg bilagsmal** på **Journalbilag**-siden, under **Funksjoner** for bilagslinjene.

## <a name="related-setup"></a>Relatert oppsett
Dette oppsettet er ikke spesifikk for økonomijournaler, men vil garantere at dataregistrering er riktig og enkel.

### <a name="main-account"></a>Hovedkonto

Hovedkontoen oppsettet gir mange muligheter til økonomijournalen behandling:

-   **DK-krav** – Bruk dette alternativet hvis en hovedkontoen er begrenset til debet- eller kredittransaksjoner. Oppsettet kontrolleres når en journal er godkjent eller postert.
-   **Standard motkonto**
-   **Suspendert** – Suspendere en hovedkonto for dataregistrering på tvers av alle firmaer eller for et bestemt firma / juridiske enheter.
-   **Ikke tillat manuell registrering** – Hindre at brukere manuelt angir en verdi for kontoen i journaler.
-   **Standard / valider valutakoder**
-   **Overstyring for juridisk enhet** – Dette oppsettet er spesifikk for definert firma / juridisk enhet:
    -   **Standard / Valider merverdiavgift**
    -   **Standarddimensjon** – **Ikke fast** eller **Fast verdi**. **Fast verdi** vil bidra til å garantere at alle posteringer for denne hovedkontoen alltid bruker en dimensjonsverdi som er definert som **Fast**.
-   **Posteringsvalidering**
    -   **Brukervalidering** – Dette alternativet styrer hvilke brukere som har tillatelse til å postere til en hovedkonto.
    -   **Validering av posteringstype** – Dette alternativet styrer hvilke posteringstyper som er tillatt for en hovedkonto.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Regnskapsstrukturer og strukturer for avanserte regler

Regnskapsstrukturer og strukturer for avanserte regler er svært viktige for å garantere at dataene som er nødvendige for økonomisk rapportering og sporing av ytelse, blir registrert under behandling av økonomijournalen og eventuell dokumentasjon. Regnskapsstrukturer og strukturer for avanserte regler lar deg tilpasse dataregistreringsopplevelsen. Du kan tillate dataregistrering bare for finansdimensjoner som er relevante i hvert tilfelle, og kan også sikre at obligatorisk og riktig data alltid registreres.

Hvis du vil ha mer informasjon, se [Planlegging: kontoplan](plan-chart-of-accounts.md). 



