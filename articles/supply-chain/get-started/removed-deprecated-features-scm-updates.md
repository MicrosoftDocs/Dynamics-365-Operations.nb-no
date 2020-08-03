---
title: Funksjoner som er fjernet eller avskrevet i Dynamics 365 Supply Chain Management
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning i Dynamics 365 Supply Chain Management.
author: kamaybac
manager: tfehr
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 07f37488747766dcca96884e204339b425bbd201
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597122"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Funksjoner som er fjernet eller avskrevet i Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Dette emnet vil bli oppdatert når fjernede eller avskrevne funksjoner er dokumentert for Dynamics 365 Supply Chain Management.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging.

> [!NOTE]
> Detaljert informasjon om objekter i Finance and Operations-apper finnes i [Tekniske referanserapporter](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Du kan sammenligne de ulike versjonene av disse rapportene for å lære om objekter som er endret eller fjernet i hver versjon av Finance and Operations-apper.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Fjernede eller avskrevne funksjoner i Supply Chain Management 10.0.11

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Bruk av innebygd hovedplanleggingsmotor Supply Chain Management for distribusjonscenarioer

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | For å forbedre ytelsen og redusere SQL-databasebelastningen under kjøring av hovedplanlegging, blir den innebygde Supply Chain Management-hovedplanleggingsmotoren erstattet av Planleggingsoptimalisering. Planleggingsoptimalisering gjør det mulig å utføre raske planleggingskjøringer som kan utføres selv i kontortiden. Dette gjør at planleggerne kan reagere umiddelbart på endringer i behovs- eller planleggingsparametere. |
| **Erstattet med en annen funksjon?**   | Ja, planleggingsoptimalisering erstatter den eksisterende innebygde planleggingsmotoren Supply Chain Management. |
| **Berørte produktområder**         | Supply Chain Management – Hovedplanlegging |
| **Distribusjonsalternativ**              | Bare sky. Planleggingsoptimalisering ikke med lokale distribusjoner. |
| **Status**                         | Avskrevet. Fra april 2021 vil distribusjonsscenarioer ikke lenger støttes med den innebygde Dynamics 365 Supply Chain Management-hovedplanleggingsmotoren. For distribusjonsscenarioer må kunder bruke planleggingsoptimalisering for hovedplanleggingsberegninger. Hvis du vil ha mer informasjon, se [dokumentasjon for planleggingsoptimalisering](https://go.microsoft.com/fwlink/?linkid=2105830). Kunder som har lokale distribusjoner av Dynamics 365 Supply Chain Management, kan fortsette å bruke Supply Chain Management-hovedplanleggingsmotoren for distribusjonscenarioer etter april 2021. Det vil imidlertid ikke bli gitt flere funksjonsforbedringer. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Tidligere kunngjøringer om fjernede eller avskrevne funksjoner

Hvis du vil lære mer om funksjoner som er fjernet eller avskrevet i tidligere versjoner, kan du se [Fjernede eller avskrevne funksjoner i tidligere versjoner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).
