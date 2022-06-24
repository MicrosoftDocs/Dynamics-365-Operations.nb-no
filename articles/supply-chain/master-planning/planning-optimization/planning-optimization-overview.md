---
title: Oversikt over planleggingsoptimalisering
description: Denne artikkelen gir en oversikt over funksjoner i planleggingsoptimalisering.
author: t-benebo
ms.date: 10/31/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 302c92c48765d1c2faddd65c6c6a18ddfd56c71e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891009"
---
# <a name="planning-optimization-overview"></a>Oversikt over planleggingsoptimalisering

[!include [banner](../../includes/banner.md)]

Tilleggsfunksjonen for planleggingsoptimalisering for Microsoft Dynamics 365 Supply Chain Management gjør at beregningen av hovedplanlegging skjer utenfor Dynamics 365 Supply Chain Management og den tilknyttede SQL-databasen. Fordelene som er knyttet til planleggingsoptimaliserings-funksjonaliteten, omfatter forbedret ytelse og minimal virkning på SQL-database under kjøringer av hovedplanlegging. Du kan utføre raske planleggingskjøringer selv under kontortimer, slik at planleggere umiddelbart kan reagere på behovs- eller parameterendringer.

Hvis du vil bruke planleggingsoptimalisering, må du installere tillegget for planleggingsoptimalisering fra prosjektet i Microsoft Dynamics Lifecycle Services (LCS) og aktivere funksjonaliteten for planleggingsoptimalisering i Supply Chain Management. Hvis du vil ha mer informasjon, se [Kom i gang med planleggingsoptimalisering](get-started.md).

Følgende illustrasjon viser fordelen med å kjøre planleggingsoptimalisering i kontortiden.

![Fordel med å kjøre planleggingsoptimalisering i kontortiden.](media/PlanningOptimization1.png)

## <a name="improved-performance"></a>Ytelsen er forbedret

Planleggingsoptimalisering kan brukes i situasjoner som omfatter langvarige hovedplaner. Den er spesielt utformet for svært raske beregninger som involverer svært store mengder data. Fordi den er bygd som en hyperskalerbar multi-instanstjeneste, kan flere forekomster fungere sammen samtidig for å beregne planen. I tillegg fjerner planleggingstjenesten belastningen på hovedplanlegging fra systemet ditt og fungerer med en datastrøm som minimerer belastningen på serveren.

Planleggingsoptimalisering kan hjelpe deg med å oppnå følgende mål:

- Forbedre planleggingsytelsen gjennom en kortere kjøretid.
- Redusere innvirkningen på andre prosesser under kjøring av hovedplanlegging.
- Utføre ofte brukte planleggingskjøringer. (Du er ikke begrenset til daglige kjøringer.)
- Være sikker på at den fremtidige forretningsveksten ikke vil belaste planleggingssystemet.

## <a name="architecture-and-data-flow"></a>Arkitektur og dataflyt

Når planleggingsoptimaliserings-tillegget installeres fra LCS, opprettes det en sikker forbindelse til planleggingsoptimaliseringstjenesten. Tjenesten befinner seg i samme datasenterland eller -område som den tilknyttede forekomsten av Supply Chain Management. Når planleggingsoptimalisering er definert, sendes hoveddata og transaksjonsdata fra Supply Chain Management til planleggingsoptimaliseringstjenesten når hovedplanlegging kjøres.

Hvis tillegget for planleggingsoptimalisering er avinstallert, fjernes alle relaterte data i planleggingsoptimaliseringstjenesten.

### <a name="high-level-data-flow-for-regeneration-runs"></a>Dataflyt på høyt nivå for regenerering

1. Supply Chain Management-klienten sender et signal for å be om en planleggingskjøring fra planleggingsoptimalisering.
2. Planleggingsoptimalisering ber om de nødvendige dataene via den integrerte koblingen.
3. SQL-databasen sender den forespurte informasjonen om oppsett, hoved- og transaksjonsdata til planleggingsoptimalisering via koblingen. Koblingen oversetter informasjon mellom Supply Chain Management tjenesten for planleggingsoptimalisering.
4. Planleggingsoptimaliseringstjenesten inneholder planleggingsrelaterte data i minnet, og utfører de nødvendige beregningene.
5. Planleggingsresultatet sendes til Supply Chain Management-databasen via koblingen. Resultatene omfatter informasjon som for eksempel planlagte bestillinger og utligningsinformasjon. Planleggingsoptimalisering sender et signal til Supply Chain Management for å angi at planleggingsutførelsen er fullført. Den sender også eventuelle relevante meldinger og advarsler.

Følgende illustrasjon viser dataflyten.

![Dataflyt for regenerering.](media/PlanningOptimization2.png)

## <a name="related-resources"></a>Relaterte ressurser

[Komme i gang med planleggingsoptimalisering](get-started.md)

[Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md)

[Vise planhistorikk og planleggingslogger](plan-history-logs.md)

[Bruke filtre på en plan](plan-filters.md)

[Annullere en planleggingsjobb](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]