---
title: Optimalisere ytelsen med oppgaver for automatisk opprydding
description: Denne artikkelen beskriver hvordan du løser visse ytelsesproblemer med Microsoft Dynamics 365 Human Resources ved å rydde opp i loggen for satsvise jobber.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 97f6e310d3a69c870fe8ef03bd7a10cc7ab652e5
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113707"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Optimalisere ytelsen med automatiske ryddeoppgaver

**Avgang**

Det kan oppstå ytelsesproblemer for Microsoft Dynamics 365 Human Resources hvis den loggen for satsvise jobber blir for stor.

**Årsak**

Satsvise jobber som kjører ofte, kan føre til uholdbar vekst i loggen for satsvise jobber. Dette kan føre til ytelsesproblemer. 

**Oppløsning**

Planlegg en automatisk oppgave som skal rydde opp i loggen for satsvise jobber. Vi anbefaler at du konfigurerer at oppgaven skal kjøre ukentlig, men du må kanskje kjøre oppryddingen oftere eller sjeldnere, avhengig av miljøet. Fremgangsmåten nedenfor inneholder anbefalte innstillinger, men du kan endre disse i henhold til dine behov.

1. Velg **Systemadministrasjon** i Human Resources.

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

