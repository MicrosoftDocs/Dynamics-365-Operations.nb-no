---
title: Avbryt en hovedplanleggingsjobb
description: Denne artikkelen beskriver hvordan du avbryter en aktiv planleggingsjobb som bruker innebygd planleggingfunksjonalitet.
author: t-benebo
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6a9667be9921fdde7e1ca5de68c7f51d48905ac8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860790"
---
# <a name="cancel-a-master-planning-job"></a>Avbryte en hovedplanleggingsjobb

[!include [banner](../includes/banner.md)]

I Microsoft Dynamics 365 Supply Chain Management finnes det flere alternativer for å avbryte en hovedplanleggingjobb. Det kan for eksempel hende at du vil avbryte en hovedplanleggingsjobb hvis den ble startet ved en feiltakelse eller kjører lenger tid enn forventet, og du vil avslutte den. Den beste måten å avbryte en planleggingsjobb på, er fra siden **Uferdige planleggingsprosesser**. Alternative valg fra sidene **satsvise jobber** og **satsvise jobber utvidet** bør bare brukes hvis avbrytelse av hovedplanleggingsjobben fra siden **Uferdige planleggingsprosesser** ikke ble fullført i løpet av få minutter.

## <a name="preferred-cancel-option"></a>Foretrukket avbruddsalternativ
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a>Avbryte hovedplanleggingsjobb fra siden **Uferdige planleggingsprosesser**
1. Gå til **Hovedplanlegging > Forespørsler og rapporter > Hovedplanlegging > Uferdige planleggingsprosesser**.
2. Velg linjen med reparasjonen planleggingsprosessen du ønsker å avbryte.
3. Klikk på **Avbryt**.

## <a name="additional-cancel-options"></a>Flere avbruddsalternativer
Disse bør bare brukes hvis avbrytelse av hovedplanleggingsjobben fra siden **Uferdige planleggingsprosesser** ikke ble fullført i løpet av få minutter.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Slette hovedplanleggingsjobb fra siden **satsvise jobber**
1. Gå til **Systemadministrasjon > Forespørsler > Satsvise jobber**.
2. Velg linjen med planleggingsjobben du ønsker å slette.
3. Klikk på **Slett**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Avbryte oppgave for hovedplanleggingsjobb fra siden **satsvise jobber utvidet**
1. Gå til **Systemadministrasjon > Forespørsler > Satsvise jobber**.
2. Hvis jobb-IDen ikke vises i listen, klikker du **Bytt til utvidet skjema**, ellers fortsetter du med neste trinn.
3. Åpne den satsvise jobben. Klikk på **Jobb-IDen** for den satsvise jobben med aktiviteter som du vil avslutte.
4. I **satsvise oppgaver** velger du aktivitetene som skal avsluttes.
5. Klikk på **Endre status**, velg **Avbryt**, og klikk deretter **OK**.
6. Klikk på **Avbryt** i hurtigfanen **Satsvise oppgaver**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]