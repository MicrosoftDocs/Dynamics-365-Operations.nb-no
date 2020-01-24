---
title: Tilpassingsanalyse av planleggingsoptimalisering
description: Dette emnet forklarer hvordan du kontrollerer gjeldende oppsett og data mot funksjonene i planleggingsoptimaliseringsfunksjonaliteten.
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a61529da63bc20fdd591afc94db960b05c284bb9
ms.sourcegitcommit: b806f0c94d703bec39680fead827733361d47045
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935881"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="planning-optimization-fit-analysis"></a>Tilpassingsanalyse av planleggingsoptimalisering

Hvis du vil se hvor kompatible gjeldende oppsett og data er med funksjonaliteten for planleggingsoptimalisering, går du til **Hovedplanlegging** \> **Oppsett** \> **Tilpassingsanalyse av planleggingsoptimalisering**, og deretter velger du **Kjør analyse**. Hvis analysen finner noen uregelmessigheter, vises de på samme side. (Det kan ta noen minutter å kjøre analysen.)

> [!NOTE]
> Hvis det blir funnet uoverensstemmelser, kan du likevel bruke planleggingsoptimalisering. Resultatene av tilpassingsanalysen viser bare steder der planleggingstjenesten ikke respekterer det gjeldende oppsettet. De viser med andre ord steder der noen prosesser kan bli ignorert, eller det er ikke sikkert at de støttes.

## <a name="analysis-results-example-1"></a>Analyseresultater: eksempel 1

- **Funksjon:** produksjon
- **Problem:** varer med stykklistenivå større enn null: 56
- **Forklaring:** tilpassingsanalysen fant 56 varer som har et oppsett for stykklister for produksjon. Fordi den gjeldende versjonen av planleggingsoptimalisering ikke støtter produksjon, genererer planleggingsoptimalisering bestillingsforslag i stedet for planlagte produksjonsordrer. Den vil også vise en advarsel som viser de berørte varene.

### <a name="analysis-results-example-2"></a>Analyseresultater: eksempel 2

- **Funksjon:** handlinger
- **Problem:** dekningsgrupper med handlingsberegning aktivert: 6
- **Forklaring:** Tilpassingsanalysen fant seks dekningsgrupper der handlingsberegning er aktivert. Fordi den gjeldende versjonen av planleggingsoptimalisering ikke støtter handlinger, blir det ikke generert noen handlinger under hovedplanleggingen.

## <a name="related-resources"></a>Relaterte ressurser

[Oversikt over planleggingsoptimalisering](planning-optimization-overview.md)

[Kom i gang med planleggingsoptimalisering](get-started.md)

[Vise planhistorikk og planleggingslogger](plan-history-logs.md)

[Bruke filtre på en plan](plan-filters.md)

[Annullere en planleggingsjobb](cancel-planning-job.md)
