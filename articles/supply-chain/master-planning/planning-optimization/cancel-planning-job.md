---
title: Avbryt en planleggingsjobb
description: Denne artikkelen beskriver hvordan du avbryter en aktiv planleggingsjobb som bruker planleggingsoptimaliserings-funksjonaliteten.
author: t-benebo
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 0474c50157295d9ecd2341b700c07f4fbf1ed51f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900948"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]