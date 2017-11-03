---
title: Arbeidsflyt for utgifter
description: "Dette emnet forklarer hvordan du kan bruke arbeidsflytsystemet i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, for å sette opp en godkjenningsprosess for utgiftsrapporter i utgiftsstyring."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2c2e01d4da04cd24c2df1690e6e354e1c03cb50d
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="expense-workflow"></a>Arbeidsflyt for utgifter

[!include[banner](../includes/banner.md)]

Du kan bruke arbeidsflytsystemet i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, til å sette opp en godkjenningsprosess for utgiftsrapporter i utgiftsstyring. Du kan sette opp en arbeidsflyt som bruker følgende kriterier for å fastslå hvem som skal godkjenne utgiftsrapporter.

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

