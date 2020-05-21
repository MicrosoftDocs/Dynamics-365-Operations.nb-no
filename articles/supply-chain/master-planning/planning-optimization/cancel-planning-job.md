---
title: Annullere en planleggingsjobb
description: Dette emnet beskriver hvordan du avbryter en aktiv planleggingsjobb som bruker planleggingsoptimaliserings-funksjonaliteten.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4b65d344cd764740cc1485969c2fc4c2052e55e2
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323468"
---
# <a name="cancel-a-planning-job"></a>Avbryte en planleggingsjobb

[!include [banner](../../includes/banner.md)]

I Microsoft Dynamics 365 Supply Chain Management kan du avbryte en aktiv planleggingsjobb som bruker planleggingsoptimaliserings-funksjonaliteten. Når du velger **Avbryt** i dialogboksen når en planleggingsoptimaliseringsjobb utløses direkte fra brukergrensesnittet (ikke i bakgrunnen), vil ikke dette avbryte planleggingsoptimaliseringsjobben. Selv om du får en advarsel som "operasjonen er avbrutt", må du likevel bruke følgende fremgangsmåte for å avbryte en planleggingsjobb med planleggingsoptimalisering.


Hvis du vil avbryte en aktiv planleggingsjobb, følger du disse trinnene. 

> [!NOTE]
> Bare aktive jobber kan avbrytes.

1. Gå til **Hovedplanlegging \> Oppsett \> Planer**.
2. Velg en passende plan for planleggingskjøringen.
3. Velg **Logg**.
4. Velg planleggingsjobben som skal avbrytes.
5. Velg **Avbryt**.

Jobbstatusen blir **Avbryter** til planleggingsoptimaliserings-tjenesten bekrefter at jobben er avbrutt. Da vil statusen bli endret til **Avbrutt**.

> [!NOTE]
> Hvis du vil vise statusendringer, må du oppdatere siden ved å velge **Oppdater**-knappen.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over planleggingsoptimalisering](planning-optimization-overview.md)

[Komme i gang med planleggingsoptimalisering](get-started.md)

[Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md)

[Vise planhistorikk og planleggingslogger](plan-history-logs.md)

[Bruke filtre på en plan](plan-filters.md)
