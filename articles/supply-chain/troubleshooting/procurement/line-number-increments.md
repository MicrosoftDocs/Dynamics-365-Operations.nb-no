---
title: Uriktig linjenummer i importerte bestillinger
description: Når bestillinger importeres via databehandling, følger ikke bestillingslinjenumrene den økningen som er definert i systemparametere
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: e1cf5cf1d04824213f495ac3ebf556796c96611a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477155"
---
# <a name="imported-purchase-orders-show-incorrect-line-numbers"></a>Uriktig linjenummer i importerte bestillinger

## <a name="symptoms"></a>Symptomer

Som standard vil automatisk genererte linjenumre for bestillingslinjer som importeres via *Bestillingslinjer v2*-dataenheten, ikke bruke systemets linjenummerøkning som er angitt i systemparametere. Hvis du oppretter en bestilling manuelt og legger til linjer via bruker grensesnittet, økes linjenumrene på riktig måte. Hvis du imidlertid bruker Data Management Framework (DMF), økes de ikke riktig.

Dette problemet oppstår fordi når du importerer linjer via DMF, hvis linjenumre ikke allerede er tilordnet i den importerte enheten, bruker systemet DMFs metode for å tilordne dem. Denne metoden øker alltid linjenumrene med én.

## <a name="workaround"></a>Løsning

Kontroller at de ønskede linjenumrene allerede er angitt i linjenummerfeltene for dataenhet når du importerer bestillingslinjer. I dette tilfellet vil ikke DMF overskrive linjenumrene.
