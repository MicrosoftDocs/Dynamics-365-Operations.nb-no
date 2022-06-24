---
title: Produksjonsutleveringssted
description: Denne artikkelen beskriver hierarkiet som brukes til å identifisere produksjonsutleveringsstedet.
author: johanhoffmann
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5bfabae39d3bcb8f7fdd71ac5c93fcdbaeb9d946
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893301"
---
# <a name="production-output-location"></a>Produksjonsutleveringssted

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hierarkiet som brukes til å identifisere produksjonsutleveringsstedet.

Produksjonsutleveringsstedet er stedet der en ferdig vare først lagres etter at den er produsert. Dette stedet er vanligvis nær produksjonsprosessen som produserer den ferdige varen. Produksjonsutleveringsstedet brukes som et midlertidig lager for materialet før det flyttes til forsendelsesområdet, et lagringssted, et produksjonsinnleveringssted for en produksjonsprosess nedstrøms og så videre. 

Et standard produksjonsutleveringssted angis når ferdige varer rapporteres på en produksjonsordre eller partiordre. Det følgende hierarkiet brukes til å identifisere dette utleveringsstedet:

1. Bruk utleveringsstedet som er definert i produksjonsordrer eller partiordrehodet.
2. Hvis det ikke finnes noe sted der, kan du bruke utleveringsstedet som er definert på ressursen som brukes av den siste operasjonen som er definert i produksjonsruten.
3. Hvis det ikke finnes noe sted der, kan du bruke utleveringsstedet som er definert på ressursgruppen som brukes av ressursen for den siste operasjonen som er definert i produksjonsruten.
4. Hvis det ikke finnes noe sted der, kan du bruke utleveringsstedet som er definert i lageret som er definert for produksjonsordren.

Et standard produksjonsutleveringssted angis bare for produkter som er definert ved hjelp av avanserte lagerprosesser. Når denne typen vare er rapportert som fullført, opprettes lagerarbeid av typen **Plasser ferdigvarer** eller **Plasser koprodukt og biprodukt**. Denne typen arbeid bruker produksjonsutleveringsstedet som plukkested. Plasseringsstedet bestemmes av instruksjonene for stedet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]