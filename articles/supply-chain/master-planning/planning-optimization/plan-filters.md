---
title: Bruke filtre på en plan
description: Dette emnet beskriver hvordan du bruker filtre på en plan når planleggingsoptimaliserings-funksjonaliteten brukes.
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 7b605f9826d2116f6f52a4b880f4fb5bd24cfdd0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813057"
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
> Du bør unngå å angi et planfilter for planen som er valgt som **gjeldende dynamiske hovedplan** på siden **Parametere for hovedplanlegging**. Hvis ikke vil funksjonaliteten for den dynamiske hovedplanen bli begrenset til de filtrerte varene. Hvis for eksempel nettobehovene er oppdatert for en vare som ikke er en del av planfilteret, vil det ikke bli generert noe resultat.

## <a name="related-resources"></a>Relaterte ressurser

[Oversikt over planleggingsoptimalisering](planning-optimization-overview.md)

[Kom i gang med planleggingsoptimalisering](get-started.md)

[Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md)

[Vise planhistorikk og planleggingslogger](plan-history-logs.md)

[Annullere en planleggingsjobb](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]