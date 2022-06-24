---
title: Bruk filtre på en plan
description: Denne artikkelen beskriver hvordan du bruker filtre på en plan når planleggingsoptimaliserings-funksjonaliteten brukes.
author: t-benebo
ms.date: 01/08/2020
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
ms.openlocfilehash: c2df379be0876225bc7b0301d21f4e6660b04eb6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875311"
---
# <a name="apply-filters-to-a-plan"></a>Bruke filtre på en plan

[!include [banner](../../includes/banner.md)]

Når planleggingsoptimaliserings-funksjonaliteten brukes, kan du bruke et filter på en plan. **Planfilteret** blir alltid brukt under kjøring av en hovedplanlegging. Et **planfilter** er nyttig når du vil begrense en plan til en bestemt gruppe varer og kontrollere at ingen andre varer er inkludert som en del av den resulterende hovedplanleggingen.

Hvis det brukes et **planfilter**, og et kjøretidsfilter brukes også i kjøringen av hovedplanlegging, blir bare skjæringspunktet mellom de to filtrene tatt med i planleggingskjøringen.

Du tilgang til **planfilteret** fra **Hovedplaner** når planleggingsoptimalisering brukes.

## <a name="example-scenario"></a>Eksempelscenario

Et planfilter er definert som inkluderer varer A, B og C. Hovedplanlegging kjøres deretter for den samme planen, men forskjellige kjøretidsfiltre brukes:

- **Kjøretidsfilter som inkluderer vare D** : ingen varer er planlagt fordi det ikke er noe skjæringspunkt mellom planfilteret og kjøretidsfilteret.
- **Kjøretidsfilter som inkluderer vare A og D** : bare vare A er inkludert i planleggingskjøringen, fordi vare D ikke er del av planfilteret.
- **Kjøretidsfilter som inkluderer vare B** : bare vare B er inkludert i planleggingskjøringen, og de forrige planleggingsutdataene for vare A beholdes.
- **Kjøretidsfilter som inkluderer alle varer (tomt filter)** : varer A, B og C inkluderes i planleggingskjøringen, og de tidligere planleggingsutdataene for varer A og B blir overskrevet.

> [!NOTE]
> Hvis du definerer et planfilter for planen som er valgt som **Gjeldende dynamisk hovedplan** på siden **Parametere for hovedplanlegging**, blir funksjonaliteten for dynamisk hovedplan begrenset til de filtrerte elementene. Hvis for eksempel nettobehovene er oppdatert for en vare som ikke er en del av planfilteret, vil det ikke bli generert noe resultat.

## <a name="related-resources"></a>Relaterte ressurser

[Oversikt over planleggingsoptimalisering](planning-optimization-overview.md)

[Kom i gang med planleggingsoptimalisering](get-started.md)

[Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md)

[Vise planhistorikk og planleggingslogger](plan-history-logs.md)

[Annullere en planleggingsjobb](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
