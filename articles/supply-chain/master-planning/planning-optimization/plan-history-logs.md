---
title: Vise planhistorikk og planleggingslogger
description: Dette emnet forklarer hvordan du viser loggen for planleggingsjobber som utløses av planleggingsoptimaliserings-funksjonaliteten.
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187253"
---
# <a name="view-plan-history-and-planning-logs"></a>Vise planhistorikk og planleggingslogger

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du viser loggen for planleggingsjobber som utløses av planleggingsoptimaliserings-funksjonaliteten i Microsoft Dynamics 365 Supply Chain Management.

Hvis du vil vise loggen for en plan, åpner du planen ved å gå til **Hovedplanlegging** \> **Oppsett** \> **Planer** \> **Hovedplaner** og velge **Historikk**. Loggen viser alle jobbene for den valgte planen. Listen omfatter fullførte og aktive jobber.

Loggen for jobber for kjøringer av hovedplanlegging for planleggingsoptimalisering har bare plass til opptil 60 poster per hovedplan. Hver gang du kjører en ny hovedplanleggingsberegning, blir denne planens tidligste loggpost slettet.

I tillegg til å se starttid og status for jobber, kan du vise loggen for en bestemt jobb. Loggen inneholder tilleggsinformasjon og advarsler. Ikke alle jobber har en logg. Hvis du vil vise loggen for en jobb, velger du **Logg**. Loggoppføringer lagres bare i 30 dager etter avslutningsdatoen for jobben, og deretter slettes de automatisk.

## <a name="related-resources"></a>Relaterte ressurser

- [Oversikt over planleggingsoptimalisering](planning-optimization-overview.md)
- [Komme i gang med planleggingsoptimalisering](get-started.md)
- [Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md)
- [Bruke filtre på en plan](plan-filters.md)
- [Annullere en planleggingsjobb](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]