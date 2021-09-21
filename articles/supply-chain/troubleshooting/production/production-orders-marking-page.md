---
title: Produksjonsordrer vises ikke på siden Merking
description: Noen produksjonsordrer vises ikke på Merking-siden. Dette emnet forklarer de tre produktkonfigurasjonene som ikke er tilgjengelige for merking.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 87507e91d3feb2557e7ba771b8e34ff7ca105749
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477146"
---
# <a name="production-orders-arent-shown-on-the-marking-page"></a>Produksjonsordrer vises ikke på siden Merking

## <a name="symptoms"></a>Symptomer

Når du arbeider med diskret produksjon, vises ikke enkelte produksjonsordrer på **Merking**-siden.

## <a name="resolution"></a>Løsning

Produkter med følgende konfigurasjoner er ikke tilgjengelige for merking. De vises derfor ikke på **Merking**-siden:

- Produktene defineres som produkter av typen *faktisk vekt*.
- De er aktivert for de avanserte lagerprosessene.
- De er konfigurert til å bli kontrollert av *Standardkostnad*-prinsippet.
