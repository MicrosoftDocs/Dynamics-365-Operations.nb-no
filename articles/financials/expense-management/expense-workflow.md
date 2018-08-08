---
title: Arbeidsflyt for utgifter
description: "Dette emnet forklarer hvordan du kan bruke arbeidsflytsystemet i Microsoft Dynamics 365 for Finance and Operations, for å sette opp en godkjenningsprosess for utgiftsrapporter i utgiftsstyring."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 6ee607f723659a5b6ecd655ba4fdfca35a4c582d
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="expense-workflow"></a>Arbeidsflyt for utgifter

[!include [banner](../includes/banner.md)]

Du kan bruke arbeidsflytsystemet i Microsoft Dynamics 365 for Finance and Operations, til å sette opp en godkjenningsprosess for utgiftsrapporter i utgiftsstyring. Du kan sette opp en arbeidsflyt som bruker følgende kriterier for å fastslå hvem som skal godkjenne utgiftsrapporter.

- Ansattes rapporteringshierarki og forhåndsdefinerte godkjenningsgrenser
- Godkjenning på flere nivåer som støtter midlertidig godkjenner og endelig godkjenner
- Finansielle dimensjoner og prosjektansvar
- Oppgave til bestemte brukere eller brukergrupper

Arbeidsflyt for godkjenninger kan opprettes for kostnadsrapporter, reiserekvisisjoner, kontantforskudd og dekning av merverdiavgift (MVA).

**Eksempel**

Følgende prosess er et eksempel på kostnadsstyringsarbeidsflyten for en kostnadsrapport.

1. En ansatt oppretter og lagrer en utgiftsrapport.
2. Den ansatte sender inn utgiftsrapporten for godkjenning. Godkjenneren er identifisert basert på reglene som ble definert når arbeidsflyten ble opprettet.
3. Godkjenner mottar et varsel om at en kostnadsrapport er klar for godkjenning. Godkjenner vurderer kostnadsrapporten og verifiserer at følgende betingelser er oppfylt:

    - Utgiftene bryter ikke med noen utgiftspolicyer. Hvis en utgift bryter med en regel, verifiserer godkjenneren at utgiftsrapporten inneholder en gyldig begrunnelse for virksomheten.
    - Elektroniske kvitteringer vedlegges utgiftsrapporten.

4. Godkjenneren godkjenner utgiftsrapporten.
5. Utgiftsrapporten er tilordnet Kredittkoordinatoren for postering.
6. Ett av følgende trinn oppstår, avhengig av om automatisk postering er konfigurert:

    - Hvis automatisk postering er konfigurert, behandles utgiftsrapporten for betaling, og statusen for utgiftsrapporten oppdateres.
    - Hvis automatisk postering ikke er konfigurert, bekrefter Kredittkoordinatoren for postering at alle opprinnelige kvitteringer er sendt inn, og at kvitteringene er justert mot utgiftene på utgiftsrapporten. Alle skattekoder som er oppgitt på utgiftsrapporten, må også bekreftes som riktige.

Etter at disse kravene er bekreftet vil utgiftsrapporten legges ut.

Etter at utgiftsrapporten er lagt ut autoriseres betaling for utgiftsrapporten, og den ansatte blir refundert.

