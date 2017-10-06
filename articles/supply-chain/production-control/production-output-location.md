---
title: Produksjonsutleveringssted
description: "Dette emnet beskriver hierarkiet som brukes til å identifisere produksjonsutleveringsstedet."
author: johanhoffmann
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: e53c8e96579dba3b47bef0c00e55b8fa786fc55c
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---

# <a name="production-output-location"></a>Produksjonsutleveringssted

[!include[banner](../includes/banner.md)]

Dette emnet beskriver hierarkiet som brukes til å identifisere produksjonsutleveringsstedet.

Produksjonsutleveringsstedet er stedet der en ferdig vare først lagres etter at den er produsert. Dette stedet er vanligvis nær produksjonsprosessen som produserer den ferdige varen. Produksjonsutleveringsstedet brukes som et midlertidig lager for materialet før det flyttes til forsendelsesområdet, et lagringssted, et produksjonsinnleveringssted for en produksjonsprosess nedstrøms og så videre. 

Et standard produksjonsutleveringssted angis når ferdige varer rapporteres på en produksjonsordre eller partiordre. Det følgende hierarkiet brukes til å identifisere dette utleveringsstedet:

1. Bruk utleveringsstedet som er definert i produksjonsordrer eller partiordrehodet.
2. Hvis det ikke finnes noe sted der, kan du bruke utleveringsstedet som er definert på ressursen som brukes av den siste operasjonen som er definert i produksjonsruten.
3. Hvis det ikke finnes noe sted der, kan du bruke utleveringsstedet som er definert på ressursgruppen som brukes av ressursen for den siste operasjonen som er definert i produksjonsruten.
4. Hvis det ikke finnes noe sted der, kan du bruke utleveringsstedet som er definert i lageret som er definert for produksjonsordren.

Et standard produksjonsutleveringssted angis bare for produkter som er definert ved hjelp av avanserte lagerprosesser. Når denne typen vare er rapportert som fullført, opprettes lagerarbeid av typen **Plasser ferdigvarer** eller **Plasser koprodukt og biprodukt**. Denne typen arbeid bruker produksjonsutleveringsstedet som plukkested. Plasseringsstedet bestemmes av instruksjonene for stedet.
