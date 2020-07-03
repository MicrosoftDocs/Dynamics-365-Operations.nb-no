---
title: Funksjoner som er fjernet eller avskrevet i Dynamics 365 Commerce
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning fra Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 64241ef1c25359c7b3b305c4e8f2b24de7e8f5e4
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443924"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Funksjoner som er fjernet eller avskrevet i Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning fra Dynamics 365 Commerce.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging. 

> [!NOTE]
> Detaljert informasjon om objekter i Finance and Operations-apper finnes i [Tekniske referanserapporter](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Du kan sammenligne de ulike versjonene av disse rapportene for å lære om objekter som er endret eller fjernet i hver versjon av Finance and Operations-apper.

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Fjernede eller avskrevne funksjoner i Commerce 10.0.11
### <a name="data-action-hooks"></a>Datahandlingsbindinger
|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Funksjonen for datahandlingsbindinger er avskrevet på grunn av ytelsesproblemer. |
| **Erstattet med en annen funksjon?**   | Det anbefales å i stedet bruke [overstyringer for datahandling](../e-commerce-extensibility/data-action-overrides.md) til å endre forretningslogikken i datahandlingslaget.|
| **Berørte produktområder**         | Datahandlinger for utvidelsesmuligheter for e-handel |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Fra og med versjon 10.0.11 |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Fjernede eller avskrevne funksjoner i Commerce 10.0.10
### <a name="pos-operation-803---picking-and-receiving"></a>POS-operasjon 803 - Plukk og mottak
|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Plukk- og mottaksoperasjoner avskrives på grunn av ny utforming av den nye operasjonen. |
| **Erstattet med en annen funksjon?**   | Ja. Den er erstattet av to nye POS-operasjoner: innkommende operasjon (804) og utgående operasjon (805).|
| **Berørte produktområder**         | Salgsstedsapplikasjon |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Etter utgivelse 10.0.10 vil ikke plukk- og mottaksoperasjonen lenger motta nye funksjonsoppdateringer. Bare kritiske feilrettinger vil bli utført for denne operasjonen i fremtidige versjoner. Alle kunder oppfordres til å flytte til nye [innkommende operasjoner](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) og [utgående operasjoner](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), som vil fortsette å være en del av vårt langsiktig produktveikart. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Fjernede eller avskrevne funksjoner i Commerce 10.0.7
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>API-er for Commerce GetProductAvailabilities og GetAvailableInventoryNearby
|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Nye optimaliserte API-er er opprettet for å erstatte API-ene GetProductAvailabilities og GetAvailableInventoryNearby. |
| **Erstattet med en annen funksjon?**   | Ja: Den erstattes av APIene GetEstimatedAvailability og GetEstimatedProductWarehouseAvailability. |
| **Berørte produktområder**         | SDK for e-handelsprogram |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Etter versjon 10.0.7 vil det ikke lenger gjøres tekniske investeringer for GetProductAvailabilities og GetAvailableInventoryNearby. Organisasjoner som bruker disse APIene i sine e-handelsdistribusjoner, bør konvertere dem til de nye GetEstimatedAvailability og GetEstimatedProductWarehouseAvailability-APIene og aktivere [funksjonen for beregning av optimalisert produkttilgjengelighet](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Tidligere kunngjøringer om fjernede eller avskrevne funksjoner
Hvis du vil lære mer om funksjoner som er fjernet eller avskrevet i tidligere versjoner, kan du se [Fjernede eller avskrevne funksjoner i tidligere versjoner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).
