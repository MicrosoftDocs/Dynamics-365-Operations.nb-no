---
title: Optimalisere ytelsen med oppgaver for automatisk opprydding
description: Denne artikkelen forklarer hvordan du forbedrer ytelsen i Microsoft Dynamics 365 Human Resources ved å rydde opp i loggen for satsvise jobber.
author: twheeloc
ms.date: 08/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 10d535e54f71e7bb90c7385e09926270a446df7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902205"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Optimalisere ytelsen med oppgaver for automatisk opprydding


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Avgang**

Det kan oppstå ytelsesproblemer for Microsoft Dynamics 365 Human Resources hvis den loggen for satsvise jobber blir for stor.

**Årsak**

Satsvise jobber som kjører ofte, kan føre til uholdbar vekst i loggen for satsvise jobber. Dette kan føre til ytelsesproblemer. 

**Oppløsning**

Planlegg en automatisk oppgave som skal rydde opp i loggen for satsvise jobber. Det anbefales at du konfigurerer at oppgaven skal kjøre ukentlig, men du må kanskje kjøre oppryddingen oftere eller sjeldnere, avhengig av miljøet. Fremgangsmåten nedenfor inneholder anbefalte innstillinger, men du kan endre disse i henhold til dine behov.

1. Velg **Systemadministrasjon** i Human Resources.

2. I **Søk**-feltet angir **Opprydding av historikk for satsvis jobb**.

   ![Søk etter opprydding i logg for satsvis jobb.](media/talent-batch-history-cleanup-search-bar.png)

3. Angi **30** i **Historikkgrense (dager)**.

   ![Sett historikkgrense til 30.](media/talent-batch-history-cleanup-history-limit.png)

4. Velg **Kjør i bakgrunnen**, og velg deretter **Regelmessighet**.

   ![Angi regelmessighet.](media/talent-batch-history-cleanup-recurrence.png)

5. Under **Definer regelmessighet** angir du **Startdato** og **Starttidspunkt** som skal utføres utenom arbeidstiden eller i helgen, og deretter velger du **INGEN SLUTTDATO**. 

   ![Definere startdato og -klokkeslettet for regelmessighet.](media/talent-batch-history-cleanup-define-recurrence.png)

6. Under **MØNSTER FOR REGELMESSIGHET** velger du **Dager** og setter **GJENTA ETTER ANGITT INTERVALL** til **7**.

   ![Sette opprydding til å gjentas ukentlig.](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Velg **OK**.

8. Endre eventuelle andre parametere under **Kjør i bakgrunnen** etter behov, og velg deretter **OK.**



[!INCLUDE[footer-include](../includes/footer-banner.md)]
