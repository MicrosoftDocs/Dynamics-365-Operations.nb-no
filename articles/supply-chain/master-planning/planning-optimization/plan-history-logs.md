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
ms.openlocfilehash: 93e8f933524b34116987c9e0d91d226e21d98f4d
ms.sourcegitcommit: 5c9a5bfef507ed36f0f849ab56fa0aa8abb78d54
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/20/2021
ms.locfileid: "6646493"
---
# <a name="view-plan-history-and-planning-logs"></a>Vise planhistorikk og planleggingslogger

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du viser loggen for planleggingsjobber som utløses av planleggingsoptimaliserings-funksjonaliteten i Microsoft Dynamics 365 Supply Chain Management.

Hvis du vil vise loggen for en plan, åpner du planen ved å gå til **Hovedplanlegging** \> **Oppsett** \> **Planer** \> **Hovedplaner** og velge **Historikk**. Loggen viser alle jobbene for den valgte planen. Listen omfatter fullførte og aktive jobber.

Loggen for jobber for kjøringer av hovedplanlegging for planleggingsoptimalisering har bare plass til opptil 60 poster per hovedplan. Hver gang du kjører en ny hovedplanleggingsberegning, blir denne planens tidligste loggpost slettet.

I tillegg til å se starttid og status for jobber, kan du vise loggen for en bestemt jobb. Loggen inneholder tilleggsinformasjon og advarsler. Ikke alle jobber har en logg. Hvis du vil vise loggen for en jobb, velger du **Logg**. Loggoppføringer lagres bare i 30 dager etter avslutningsdatoen for jobben, og deretter slettes de automatisk.

Hvis alternativet for **satsvis behandling** i hurtigfanen **Kjør i bakgrunnen** ble aktivert da hovedplanleggingsbehandling ble definert, viser den satsvise jobbloggen mer informasjon om eventuelle advarsler og feil som ble generert under kjøringen av hovedplanlegging. For eksempel registreres automatisk autorisering av feil bare i loggen for den satsvise jobben. De vises ikke i logger på **Historikk**-siden.

Følg denne fremgangsmåten for å vise automatisk autorisering av feil og andre advarsler eller feil som oppstod under en hovedplanleggingskjøring.

1. Gå til **Systemadministrasjon \> Forespørsler \> Satsvise jobber**.
1. Finn og velg posten som representerer hovedplanleggingskjøringen du er interessert i. (For eksempel vil verdien av **Jobbbeskrivelse** starte med *Hovedplanlegging*.)
1. Følg ett av disse trinnene, avhengig av om du bruker det *utvidede skjemaet* eller det *eldre* (ikke-utvidede) skjemaet for **Satsvise jobber**-siden:

    - Hvis du bruker det utvidede skjemaet: Velg **Logg for satsvis jobb** i handlingsruten. På siden **Logg for satsvis jobb** velger du deretter **Logg** i handlingsruten.
    - Hvis du bruker det eldre skjemaet: Velg **Logg** i fanen **Satsvis jobb** i handlingsruten.

1. Velg **Meldingsdetaljer** for å åpne ruten **Meldingsdetaljer**, der du kan vise alle advarsler og feil som ble registrert under behandling.

## <a name="related-resources"></a>Relaterte ressurser

- [Oversikt over planleggingsoptimalisering](planning-optimization-overview.md)
- [Kom i gang med planleggingsoptimalisering](get-started.md)
- [Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md)
- [Bruke filtre på en plan](plan-filters.md)
- [Annullere en planleggingsjobb](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
