---
title: Optimalisere ytelsen med automatiske ryddeoppgaver
description: Dette emnet beskriver hvordan du løser visse ytelsesproblemer med Microsoft Dynamics 365 Talent ved å rydde opp i loggen for satsvise jobber.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: fe536ace5c25765bd9c573f9303bd92f834765f7
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897978"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Optimalisere ytelsen med automatiske ryddeoppgaver

**Avgang**

Det kan oppstå ytelsesproblemer for Microsoft Dynamics 365 Talent hvis den loggen for satsvise jobber blir for stor.

**Årsak**

Satsvise jobber som kjører ofte, kan føre til uholdbar vekst i loggen for satsvise jobber. Dette kan føre til ytelsesproblemer. 

**Oppløsning**

Planlegg en automatisk oppgave som skal rydde opp i loggen for satsvise jobber. Vi anbefaler at du konfigurerer at oppgaven skal kjøre ukentlig, men du må kanskje kjøre oppryddingen oftere eller sjeldnere, avhengig av miljøet. Fremgangsmåten nedenfor inneholder anbefalte innstillinger, men du kan endre disse i henhold til dine behov.

1. Velg **Systemadministrasjon** i Talent.

2. I **Søk**-feltet angir **Opprydding av historikk for satsvis jobb**.

   ![Søk etter opprydding i logg for satsvis jobb](media/talent-batch-history-cleanup-search-bar.png)

3. Angi **30** i **Historikkgrense (dager)**.

   ![Sett historikkgrense til 30](media/talent-batch-history-cleanup-history-limit.png)

4. Velg **Kjør i bakgrunnen**, og velg deretter **Regelmessighet**.

   ![Angi regelmessighet](media/talent-batch-history-cleanup-recurrence.png)

5. Under **Definer regelmessighet** angir du **Startdato** og **Starttidspunkt** som skal utføres utenom arbeidstiden eller i helgen, og deretter velger du **INGEN SLUTTDATO**. 

   ![Definere startdato og -klokkeslettet for regelmessighet](media/talent-batch-history-cleanup-define-recurrence.png)

6. Under **MØNSTER FOR REGELMESSIGHET** velger du **Dager** og setter **GJENTA ETTER ANGITT INTERVALL** til **7**.

   ![Sette opprydding til å gjentas ukentlig](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Velg **OK**.

8. Endre eventuelle andre parametere under **Kjør i bakgrunnen** etter behov, og velg deretter **OK.**

