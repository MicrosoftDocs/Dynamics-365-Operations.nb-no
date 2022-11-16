---
title: Avbryt en jobb som ble opprettet med den avskrevne hovedplanleggingsmotoren
description: Denne artikkelen beskriver hvordan du avbryter en aktiv planleggingsjobb som bruker den avskrevne hovedplanleggingsmotoren.
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
ms.openlocfilehash: 7b71a43f407050dccb7550db7c4b6a98a596d589
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740884"
---
# <a name="cancel-a-job-that-was-created-using-the-deprecated-master-planning-engine"></a>Avbryt en jobb som ble opprettet med den avskrevne hovedplanleggingsmotoren

[!include [banner](../includes/banner.md)]

Det finnes flere alternativer for å avbryte en jobb som ble opprettet med den avskrevne hovedplanleggingsmotoren. Det kan for eksempel hende at du vil avbryte en hovedplanleggingsjobb hvis den ble startet ved en feiltakelse eller kjører lenger tid enn forventet, og du vil avslutte den.

Den beste måten å avbryte en planleggingsjobb på, er fra siden **Uferdige planleggingsprosesser**. Alternative valg fra sidene **satsvise jobber** og **satsvise jobber utvidet** bør bare brukes hvis avbrytelse av hovedplanleggingsjobben fra siden **Uferdige planleggingsprosesser** ikke ble fullført i løpet av få minutter.

## <a name="preferred-cancel-option"></a>Foretrukket avbruddsalternativ

### <a name="cancel-master-planning-job-from-the-unfinished-planning-processes-page"></a>Avbryt hovedplanleggingsjobben fra siden Uferdige planleggingsprosesser

1. Gå til **Hovedplanlegging > Forespørsler og rapporter > Hovedplanlegging > Uferdige planleggingsprosesser**.
2. Velg linjen med reparasjonen planleggingsprosessen du ønsker å avbryte.
3. Velg **Avbryt**.

## <a name="additional-cancel-options"></a>Flere avbruddsalternativer

Disse bør bare brukes hvis avbrytelse av hovedplanleggingsjobben fra siden **Uferdige planleggingsprosesser** ikke ble fullført i løpet av få minutter.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Slette hovedplanleggingsjobb fra siden **satsvise jobber**

1. Gå til **Systemadministrasjon > Forespørsler > Satsvise jobber**.
2. Velg linjen med planleggingsjobben du ønsker å slette.
3. Velg **Slett**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Avbryte oppgave for hovedplanleggingsjobb fra siden **satsvise jobber utvidet**

1. Gå til **Systemadministrasjon > Forespørsler > Satsvise jobber**.
2. Hvis jobb-IDen ikke vises i listen, klikker du **Bytt til utvidet skjema**, ellers fortsetter du med neste trinn.
3. Åpne den satsvise jobben. Velg **Jobb-ID** for den satsvise jobben med aktiviteter du vil avslutte.
4. I **satsvise oppgaver** velger du aktivitetene som skal avsluttes.
5. Velg **Endre status**, velg **Avbryt**, og klikk deretter på **OK**.
6. Klikk på **Avbryt** i hurtigfanen **Satsvise oppgaver**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]