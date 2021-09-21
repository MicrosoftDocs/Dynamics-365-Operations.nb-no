---
title: Enhetspriser på bestillinger beregnes ikke basert på enhetsomregningen
description: Enhetspriser på bestillinger beregnes ikke basert på enhetsomregningen
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4695f4661c3abb8ab38e3ca74b513e8529e37d20
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477195"
---
# <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Enhetspriser på bestillinger beregnes ikke basert på enhetsomregningen

## <a name="symptoms"></a>Symptomer

Når en enhet endres på en bestilling, beregnes ikke forretningsavtalepriser på nytt i henhold til enhetsomregningsdefinisjoner.

## <a name="cause"></a>Årsak

Prisene hentes alltid fra forretningsavtaler (eller andre prisinnstillinger i systemet, for eksempel salgsavtaler eller varepriser), og de angis for en enhet.

Hvis enheten endres på en ordrelinje, søker systemet etter en pris for den nye enheten og bruker denne prisen. Hvis det ikke finnes en pris for enheten, bruker ikke systemet en pris. Enhetskonverteringen kan ikke brukes til å omberegne prisen til en annen enhet. I teorien kan det hende at prisen for en boks på ti ikke er lik ti ganger prisen på en boks.

## <a name="workaround"></a>Løsning

En måte å omgå dette problemet på, er å kontrollere at det finnes forretningsavtaler for de enhetene du forventer vil bli brukt på ordrelinjer for varen.
