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
ms.openlocfilehash: f5f1f2c8e3e43e36d837ebf989422b0dca7819d6
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741183"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]