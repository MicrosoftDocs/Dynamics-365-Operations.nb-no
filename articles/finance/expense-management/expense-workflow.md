---
title: Arbeidsflyt for reiseregninger og utlegg
description: Dette emnet forklarer hvordan du kan bruke arbeidsflytsystemet i Microsoft Dynamics 365 Finance, for å sette opp en godkjenningsprosess for utgiftsrapporter i utgiftsstyring.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/21/2020
ms.locfileid: "3153979"
---
# <a name="expense-management-workflow"></a>Arbeidsflyt for reiseregninger og utlegg

[!include [banner](../includes/banner.md)]

Du kan bruke arbeidsflytsystemet, for å sette opp en godkjenningsprosess for utgiftsrapporter i utgiftsstyring. Du kan sette opp en arbeidsflyt som bruker følgende kriterier for å fastslå hvem som skal godkjenne utgiftsrapporter.

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
