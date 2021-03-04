---
title: Funksjoner som er fjernet eller avskrevet i Dynamics 365 Supply Chain Management
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning i Dynamics 365 Supply Chain Management.
author: kamaybac
manager: tfehr
ms.date: 12/07/2020
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
ms.openlocfilehash: d4d2805e36f132660152370cbeee856862ad6faa
ms.sourcegitcommit: 069ed5789517b550065e5e2317658fec4027359e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/07/2020
ms.locfileid: "4689538"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Funksjoner som er fjernet eller avskrevet i Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Dette emnet vil bli oppdatert når fjernede eller avskrevne funksjoner er dokumentert for Dynamics 365 Supply Chain Management.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging.

> [!NOTE]
> Detaljert informasjon om objekter i Finance and Operations-apper finnes i [Tekniske referanserapporter](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Du kan sammenligne de ulike versjonene av disse rapportene for å lære om objekter som er endret eller fjernet i hver versjon av Finance and Operations-apper.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Fjernede eller avskrevne funksjoner i Supply Chain Management 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-støtte for Dynamics 365 er avskrevet

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Fra og med desember 2020 er Microsoft Internet Explorer 11-støtte for alle Dynamics 365-produkter avskrevet, og Internet Explorer 11 støttes ikke etter august 2021.<br><br>Dette vil påvirke kunder som bruker Dynamics 365-produkter som er utformet for bruk via et Internet Explorer 11-grensesnitt. Etter august 2021 støttes ikke Internet Explorer 11 for slike Dynamics 365-produkter. |
| **Erstattet med en annen funksjon?**   | Vi anbefaler at kundene går over til Microsoft Edge.|
| **Berørte produktområder**         | Alle Dynamics 365-produkter |
| **Distribusjonsalternativ**              | Alle|
| **Status**                         | Avskrevet. Internet Explorer 11 støttes ikke etter august 2021.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Bruk av innebygd hovedplanleggingsmotor Supply Chain Management for produksjonsscenarioer

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | For å forbedre ytelsen og redusere SQL-databasebelastningen under kjøring av hovedplanlegging, blir den innebygde Supply Chain Management-hovedplanleggingsmotoren erstattet av Planleggingsoptimalisering. Planleggingsoptimalisering gjør det mulig å utføre raske planleggingskjøringer som kan utføres selv i kontortiden. Dette gjør at planleggerne kan reagere umiddelbart på endringer i behovs- eller planleggingsparametere. |
| **Erstattet med en annen funksjon?**   | Ja, planleggingsoptimalisering erstatter den eksisterende innebygde planleggingsmotoren Supply Chain Management. |
| **Berørte produktområder**         | Supply Chain Management – Hovedplanlegging |
| **Distribusjonsalternativ**              | Bare sky. Planleggingsoptimalisering ikke med lokale distribusjoner. |
| **Status**                         | Avskrevet. Innen 1. oktober 2021 vil produksjonsscenarioer ikke lenger støttes med den innebygde Dynamics 365 Supply Chain Management-hovedplanleggingsmotoren. For produksjonsscenarioer må kunder bruke planleggingsoptimalisering for hovedplanleggingsberegninger. Hvis du vil ha mer informasjon, se [dokumentasjon for planleggingsoptimalisering](https://go.microsoft.com/fwlink/?linkid=2105830). Kunder som har lokale distribusjoner av Dynamics 365 Supply Chain Management, kan fortsette å bruke Supply Chain Management-hovedplanleggingsmotoren for produksjonsscenarioer etter oktober 2021. Det vil imidlertid ikke bli gitt flere funksjonsforbedringer. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Fjernede eller avskrevne funksjoner i Supply Chain Management 10.0.11

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Bruk av innebygd hovedplanleggingsmotor Supply Chain Management for distribusjonscenarioer

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | For å forbedre ytelsen og redusere SQL-databasebelastningen under kjøring av hovedplanlegging, blir den innebygde Supply Chain Management-hovedplanleggingsmotoren erstattet av Planleggingsoptimalisering. Planleggingsoptimalisering gjør det mulig å utføre raske planleggingskjøringer som kan utføres selv i kontortiden. Dette gjør at planleggerne kan reagere umiddelbart på endringer i behovs- eller planleggingsparametere. |
| **Erstattet med en annen funksjon?**   | Ja, planleggingsoptimalisering erstatter den eksisterende innebygde planleggingsmotoren Supply Chain Management. |
| **Berørte produktområder**         | Supply Chain Management – Hovedplanlegging |
| **Distribusjonsalternativ**              | Bare sky. Planleggingsoptimalisering ikke med lokale distribusjoner. |
| **Status**                         | Avskrevet. Innen 1. april 2021 vil distribusjonsscenarioer ikke lenger støttes med den innebygde Dynamics 365 Supply Chain Management-hovedplanleggingsmotoren. For distribusjonsscenarioer må kunder bruke planleggingsoptimalisering for hovedplanleggingsberegninger. Hvis du vil ha mer informasjon, se [dokumentasjon for planleggingsoptimalisering](https://go.microsoft.com/fwlink/?linkid=2105830). Kunder som har lokale distribusjoner av Dynamics 365 Supply Chain Management, kan fortsette å bruke Supply Chain Management-hovedplanleggingsmotoren for distribusjonscenarioer etter april 2021. Det vil imidlertid ikke bli gitt flere funksjonsforbedringer. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Tidligere kunngjøringer om fjernede eller avskrevne funksjoner

Hvis du vil lære mer om funksjoner som er fjernet eller avskrevet i tidligere versjoner, kan du se [Fjernede eller avskrevne funksjoner i tidligere versjoner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]