---
title: Funksjonshullene mellom rapporter om lagerverdi/aldersfordelinger og deres lagringsversjoner
description: Funksjonshullene mellom rapporter om lagerverdi/aldersfordelinger og deres lagringsversjoner
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f74389648034bf036ce48ac84b3421a8a340f105
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686660"
---
# <a name="functional-gaps-between-inventory-valueaging-reports-and-their-storage-versions"></a>Funksjonshullene mellom rapporter om lagerverdi/aldersfordelinger og deres lagringsversjoner

Funksjonene [Lagring av rapport for aldersfordeling for lager](/dynamics365/supply-chain/cost-management/inventory-aging-report-storage) og [Rapport for oppbevaring av lagerverdi](/dynamics365/supply-chain/cost-management/inventory-value-report-storage) gjør det mulig for Supply Chain Management å vise store mengder lagertransaksjoner. I hvert tilfelle lagres rapportresultatene for lesing og eksport, i motsetning til ikke-lagerversjoner av disse rapportene. Det finnes imidlertid en del funksjonalitet som finnes i ikke-lagerversjoner av disse rapportene, som ikke finnes i lagerversjonene. Underdelene nedenfor gir en oversikt over forskjellene og løsninger.

## <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Lagerrapporter inkluderer ikke delsummer, selv om de er aktivert i rapportoppsettet

Delsummer kan forårsake problemer når resultatet eksporteres, spesielt hvis brukerne endrer postrekkefølgen.

Hvis du vil kontrollere delsummene, kan du eksportere resultatet til Microsoft Excel. Hvis du vil kontrollere delsummer i Supply Chain Management, kan du også bruke [Funksjonsbehandling](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) til å aktivere funksjonene *Ny rutenettetkontroll* og *Gruppering i rutenett*, som gir en mye mer fleksibel måte å se delsummen på for alle grupper etter kolonne. Hvis du vil ha mer informasjon, se [Rutenettfunksjoner](/dynamics365/fin-ops-core/fin-ops/get-started/grid-capabilities).

## <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Rapport for oppbevaring av lagerverdi støtter ikke finanskontoinformasjon

Du kan kjøre råbalansen for å hente saldoen for lagerkontoene og sammenligne dem med **rapporten for oppbevaring av lagerverdi**.
