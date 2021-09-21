---
title: En leverandørrabatt blir ikke akkumulert basert på fakturaer
description: En leverandørrabatt blir ikke akkumulert basert på fakturaer
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
ms.openlocfilehash: 9d4596a7351969bf181982a24ea1dcc6f5732831
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477243"
---
# <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>En leverandørrabatt blir ikke akkumulert basert på fakturaer

## <a name="symptoms"></a>Symptomer

Hvis fakturaer som er postert, har forskjellige forfallsdatoer, blir ikke disse fakturaene gjenspeilet i leverandørrabatter som genereres fra dem.

## <a name="resolution"></a>Løsning

Forfallsdatoen tas ikke med når leverandørrabatten beregnes. Vurder å tilpasse systemet slik at forfallsdatoen og forbindelsen til fakturaen er mer synlig med hensyn til den faktiske leverandørrabatten.
