---
title: Funksjoner som er fjernet eller avskrevet i Dynamics 365 Supply Chain Management
description: Denne artikkelen beskriver funksjoner som er fjernet eller som er planlagt for fjerning i Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 722b34e89a54715db39259549c11a78d69d2b4d3
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739877"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Funksjoner som er fjernet eller avskrevet i Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Denne artikkelen vil bli oppdatert når fjernede eller avskrevne funksjoner er dokumentert for Dynamics 365 Supply Chain Management.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging.

> [!NOTE]
> Detaljert informasjon om objekter i økonomi- og driftsapper finnes i [Tekniske referanserapporter](/dynamics/s-e/). Du kan sammenligne de ulike versjonene av disse rapportene for å lære om objekter som er endret eller fjernet i hver versjon av økonomi- og driftsapper.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10029-release"></a>Fjernede eller avskrevne funksjoner i Supply Chain Management 10.0.29

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>Lageroverføringsordrer som har avgift på overføringsprisen

| &nbsp;  | &nbsp;  |
|---|---|
| **Årsak til avskrivning/fjerning** | Funksjonen [Lageroverføringsordrer som har avgifter på overføringspris](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md) erstattes av funksjonen [Lageroverføringsordrer for India](../../finance/localizations/apac-ind-stock-transfer.md). |
| **Erstattet med en annen funksjon?**   | Ja, funksjonen [Lageroverføringsordrer som har avgifter på overføringspris](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md) erstattes av funksjonen [Lageroverføringsordrer for India](../../finance/localizations/apac-ind-stock-transfer.md). |
| **Berørte produktområder** | Supply Chain Management – lager |
| **Distribusjonsalternativ** | Skyen og lokalt |
| **Status** | <p>Blir avskrevet. Funksjonen *Lageroverføringsordrer som har avgift på overføringspris* vil ikke motta kundestøtte med feilrettinger og sikkerhetsreparasjon.</p><p>Etter april 2023 blir kunder bedt om å bruke den forbedrede funksjonaliteten *Lageroverføringsordrer for India* som standard. Etter oktober 2023 er ikke funksjonen *Lageroverføringsordrer som har avgift på overføringspris* lenger tilgjengelige, og kunder blir bedt om å flytte til den forbedrede funksjonen *Lageroverføringsordrer for India*.</p><p>Hvis du vil ha mer informasjon , kan du se [Lageroverføringsordrer for India](../../finance/localizations/apac-ind-stock-transfer.md).</p> |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10019-release"></a>Fjernede eller avskrevne funksjoner i Supply Chain Management 10.0.19

### <a name="job-card-device"></a>Jobbkortenhet

| &nbsp;  | &nbsp;  |
|---|---|
| **Årsak til avskrivning/fjerning** | [Jobbkortenheten](../production-control/config-job-card-device.md) erstattes av det nye [grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-configure.md). |
| **Erstattet med en annen funksjon?**   | Ja, [jobbkortenheten](../production-control/config-job-card-device.md) skal erstattes av det nye [grensesnittet for produksjonsutførelse](../production-control/production-floor-execution-configure.md). |
| **Berørte produktområder** | Supply Chain Management – produksjonskontroll |
| **Distribusjonsalternativ** | Skyen og lokalt |
| **Status** | Avskrevet. Jobbkortenheten vil motta støtte med feilrettinger og sikkerhetskorrigeringer, men funksjonsforbedringer vil ikke lenger være tilgjengelig. Etter april 2022 vil jobbkortenheten ikke lenger støttes, og kunder blir bedt om å flytte til det nye grensesnittet for produksjonsutførelse. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>Fjernede eller avskrevne funksjoner i Supply Chain Management 10.0.18

### <a name="supply-chain-management--warehousing-the-warehouse-app"></a><a name="wma"></a>Supply Chain Management - Warehousing (lagerappen)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Fra april 2021 er *Supply Chain Management - Warehousing* (lagerappen) avskrivet, og den støttes ikke etter april 2022. Den erstattes nå av *mobilappen Lagerstyring*, som ble lansert sammen med versjon 10.0.17 av Supply Chain Management. Den nye appen er en fullstendig erstatning, men bruker samme underliggende rammeverk, noe som gjør det enkelt å migrere. Om nødvendig kan de to appene brukes side ved side for å hjelpe brukerne med å justere gradvis når de lærer å bruke den nye appen.<br><br>For mer informasjon om den nye mobilappen Lagerstyring kan du se [Mobilappen Lagerstyring](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) og [Installere og koble til mobilappen Lagerstyring](../warehousing/install-configure-warehouse-management-app.md). |
| **Erstattet med en annen funksjon?**   | Ja, erstattet av den nye mobilappen Lagerstyring. |
| **Berørte produktområder**         | Supply Chain Management - Warehouse-app |
| **Distribusjonsalternativ**              | Skyen og lokalt |
| **Status**                         | Avskrevet. Lagerappen vil motta støtte med feilrettinger og sikkerhetskorrigeringer, men funksjonsforbedringer vil ikke lenger være tilgjengelig. Etter april 2022 vil den gamle lagerappen ikke lenger støttes, og kunder blir bedt om å flytte til den nye mobilappen Lagerstyring. Den gamle lagerappen fjernes deretter fra Microsoft Store og Google Play-butikk.  |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Fjernede eller avskrevne funksjoner i Supply Chain Management 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-støtte for Dynamics 365 er avskrevet

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Fra og med desember 2020 er Microsoft Internet Explorer 11-støtte for alle Dynamics 365-produkter avskrevet, og Internet Explorer 11 støttes ikke etter august 2021.<br><br>Dette vil påvirke kunder som bruker Dynamics 365-produkter som er utformet for bruk via et Internet Explorer 11-grensesnitt. Etter august 2021 støttes ikke Internet Explorer 11 for slike Dynamics 365-produkter. |
| **Erstattet med en annen funksjon?**   | Vi anbefaler at kundene går over til Microsoft Edge.|
| **Berørte produktområder**         | Alle Dynamics 365-produkter |
| **Distribusjonsalternativ**              | Alle|
| **Status**                         | Avskrevet. Internet Explorer 11 støttes ikke etter august 2021.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Bruk av innebygd hovedplanleggingsmotor Supply Chain Management for produksjonsscenarioer

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | For å forbedre ytelsen og redusere SQL-databasebelastningen under kjøring av hovedplanlegging, blir den innebygde Supply Chain Management-hovedplanleggingsmotoren erstattet av Planleggingsoptimalisering. Planleggingsoptimalisering gjør det mulig å utføre raske planleggingskjøringer som kan utføres selv i kontortiden. Dette gjør at planleggerne kan reagere umiddelbart på endringer i behovs- eller planleggingsparametere. |
| **Erstattet med en annen funksjon?**   | Ja, planleggingsoptimalisering erstatter den eksisterende innebygde planleggingsmotoren Supply Chain Management. |
| **Berørte produktområder**         | Supply Chain Management – Hovedplanlegging |
| **Distribusjonsalternativ**              | Bare sky. Planleggingsoptimalisering ikke med lokale distribusjoner. |
| **Status**                         | Avskrevet. Innen 1. april 2022 vil produksjonsscenarioer ikke lenger støttes for den innebygde hovedplanleggingsmotoren i Supply Chain Management. Per denne datoen vil Microsoft stoppe all aktiv utvikling på produksjonsscenarioer for den innebygde planleggingsmotoren, ikke frigi nye funksjoner og bare frigi kritiske reparasjoner. Etter denne datoen må alle firmaer som trenger støtte for produksjonsscenarioer, bruke Planleggingsoptimalisering for hovedplanleggingsberegningene. Planleggingsoptimalisering forventes å gi full støtte for produksjonsscenarioer i oktober 2022. Hvis du vil ha mer informasjon, kan du se [Oversikt over avskrevet hovedplanlegging](../master-planning/deprecated-master-planning-overview.md).<br><br>Firmaer som har lokale distribusjoner av Supply Chain Management, kan fortsette å bruke den innebygde hovedplanleggingsmotoren for produksjonsscenarioer etter april 2022. Det vil imidlertid ikke bli gitt flere funksjonsforbedringer. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Fjernede eller avskrevne funksjoner i Supply Chain Management 10.0.11

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Bruk av innebygd hovedplanleggingsmotor Supply Chain Management for distribusjonscenarioer

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | For å forbedre ytelsen og redusere SQL-databasebelastningen under kjøring av hovedplanlegging, blir den innebygde Supply Chain Management-hovedplanleggingsmotoren erstattet av Planleggingsoptimalisering. Planleggingsoptimalisering gjør det mulig å utføre raske planleggingskjøringer som kan utføres selv i kontortiden. Dette gjør at planleggerne kan reagere umiddelbart på endringer i behovs- eller planleggingsparametere. |
| **Erstattet med en annen funksjon?**   | Ja, planleggingsoptimalisering erstatter den eksisterende innebygde planleggingsmotoren Supply Chain Management. |
| **Berørte produktområder**         | Supply Chain Management – Hovedplanlegging |
| **Distribusjonsalternativ**              | Bare sky. Planleggingsoptimalisering ikke med lokale distribusjoner. |
| **Status**                         | Avskrevet. Innen 1. april 2021 vil distribusjonsscenarioer ikke lenger støttes med den innebygde Dynamics 365 Supply Chain Management-hovedplanleggingsmotoren. For distribusjonsscenarioer må kunder bruke planleggingsoptimalisering for hovedplanleggingsberegninger. Hvis du vil ha mer informasjon, kan du se [Oversikt over avskrevet hovedplanlegging](../master-planning/deprecated-master-planning-overview.md). Kunder som har lokale distribusjoner av Dynamics 365 Supply Chain Management, kan fortsette å bruke Supply Chain Management-hovedplanleggingsmotoren for distribusjonscenarioer etter april 2021. Det vil imidlertid ikke bli gitt flere funksjonsforbedringer. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Tidligere kunngjøringer om fjernede eller avskrevne funksjoner

Hvis du vil lære mer om funksjoner som er fjernet eller avskrevet i tidligere versjoner, kan du se [Fjernede eller avskrevne funksjoner i tidligere versjoner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

