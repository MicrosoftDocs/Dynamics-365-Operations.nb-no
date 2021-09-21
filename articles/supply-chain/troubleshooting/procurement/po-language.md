---
title: Bestillinger reflekterer ikke språkinnstillingene til den juridiske enheten
description: Produktnavnet på en bestilling vises på systemspråket i stedet for språket som er angitt for den juridiske enheten der bestillingen ble opprettet
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
ms.openlocfilehash: 4deec493b5480dc570ac82876243bc31a2ae87aa
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477189"
---
# <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Bestillinger reflekterer ikke språkinnstillingene til den juridiske enheten


## <a name="symptoms"></a>Symptomer

Produktnavnet på en bestilling vises på systemspråket i stedet for språket som er angitt for den juridiske enheten der bestillingen ble opprettet.

## <a name="reproduce-the-issue"></a>Reprodusere problemet

Følgende prosedyre viser én måte å reprodusere problemet på.

1. Sett systemspråket til *EN-US* (amerikansk engelsk).
1. Kontroller at det finnes et produkt der språkene *EN-US* og *DE* (tysk) blir vedlikeholdt for oversettelser av produktnavnet.
1. Endre språket for en juridisk enhet til *DE*.
1. I den juridiske enheten der *DE* er angitt som språk, oppretter du en bestilling som inkluderer produktet.
1. Legg merke til at produktnavnet fremdeles vises på amerikansk engelsk (systemspråket).

## <a name="resolution"></a>Løsning

Denne virkemåten er standard. I bestillinger vises produktet alltid på systemspråket. Bestillingsspråket brukes når det opprettes en bekreftelsesjournal.
