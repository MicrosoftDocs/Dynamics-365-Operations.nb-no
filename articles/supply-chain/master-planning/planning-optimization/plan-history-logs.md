---
title: Vis planhistorikk og planleggingslogger
description: Denne artikkelen forklarer hvordan du viser historikken for planleggingsjobber.
author: t-benebo
ms.date: 06/01/2020
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
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ab469686a009364bf53cb963506fd2107075a283
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740938"
---
# <a name="view-plan-history-and-planning-logs"></a>Vis planhistorikk og planleggingslogger

[!include [banner](../../includes/banner.md)]

Denne artikkelen forklarer hvordan du viser historikken for planleggingsjobber i Microsoft Dynamics 365 Supply Chain Management.

Hvis du vil vise loggen for en plan, åpner du planen ved å gå til **Hovedplanlegging** \> **Oppsett** \> **Planer** \> **Hovedplaner** og velge **Historikk**. Loggen viser alle jobbene for den valgte planen. Listen omfatter fullførte og aktive jobber.

Systemet beholder maksimalt 60 historikkposter per hovedplan og sletter poster som er eldre enn 30 dager. Hver gang du kjører en ny hovedplanleggingsberegning, legger systemet til en ny historikkpost og rydder opp i de eldste postene etter behov.

I tillegg til å se starttid og status for jobber, kan du vise loggen for en bestemt jobb. Loggen inneholder tilleggsinformasjon og advarsler. Ikke alle jobber har en logg. Hvis du vil vise loggen for en jobb, velger du **Logg**. Loggoppføringer lagres bare i 30 dager etter avslutningsdatoen for jobben, og deretter slettes de automatisk.

Hvis alternativet for **satsvis behandling** i hurtigfanen **Kjør i bakgrunnen** ble aktivert da hovedplanleggingsbehandling ble definert, viser den satsvise jobbloggen mer informasjon om eventuelle advarsler og feil som ble generert under kjøringen av hovedplanlegging. For eksempel registreres automatisk autorisering av feil bare i loggen for den satsvise jobben. De vises ikke i logger på **Historikk**-siden.

Følg denne fremgangsmåten for å vise automatisk autorisering av feil og andre advarsler eller feil som oppstod under en hovedplanleggingskjøring.

1. Gå til **Systemadministrasjon \> Forespørsler \> Satsvise jobber**.
1. Finn og velg posten som representerer hovedplanleggingskjøringen du er interessert i. (For eksempel vil verdien av **Jobbbeskrivelse** starte med *Hovedplanlegging*.)
1. Følg ett av disse trinnene, avhengig av om du bruker det *utvidede skjemaet* eller det *eldre* (ikke-utvidede) skjemaet for **Satsvise jobber**-siden:

    - Hvis du bruker det utvidede skjemaet: Velg **Logg for satsvis jobb** i handlingsruten. På siden **Logg for satsvis jobb** velger du deretter **Logg** i handlingsruten.
    - Hvis du bruker det eldre skjemaet: Velg **Logg** i fanen **Satsvis jobb** i handlingsruten.

1. Velg **Meldingsdetaljer** for å åpne ruten **Meldingsdetaljer**, der du kan vise alle advarsler og feil som ble registrert under behandling.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
