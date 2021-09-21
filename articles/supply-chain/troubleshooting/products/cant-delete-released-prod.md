---
title: Du kan ikke slette et frigitt produkt
description: Du kan bare slette et frigitt produkt og alle variantene av det hvis det frigitte produktet ikke har noen tilknyttede transaksjoner.
author: SmithaNataraj
ms.date: 06/11/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f03d45a36401314a4b02ff354fabb474568c48b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477232"
---
# <a name="you-cant-delete-a-released-product"></a>Du kan ikke slette et frigitt produkt

## <a name="symptoms"></a>Symptomer

Du kan bare slette et frigitt produkt og alle variantene av det hvis det frigitte produktet ikke har noen tilknyttede transaksjoner.

## <a name="resolution"></a>Løsning

Følg denne fremgangsmåten for å slette et frigitt produkt eller en frigitt produktstandard.

1. Lukk alle åpne transaksjoner for varene.
1. Reduser lageret til 0 (null).
1. Utfør lagerlukking.
1. Slett alle produktvarianter for produktstandarden du vil slette.
