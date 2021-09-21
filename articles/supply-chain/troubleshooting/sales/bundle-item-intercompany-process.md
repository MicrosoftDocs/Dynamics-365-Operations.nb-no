---
title: Buntvare støttes ikke i en konsernintern prosess
description: Buntvaren er ikke er tilgjengelig for innkjøp. Salgsordren kjøper bare komponentene for buntvaren, ikke selve buntvaren.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 21adc7d071837b762157364f6f8ed370c69c7fd3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477202"
---
# <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>En buntvare støttes ikke i en konsernintern prosess

## <a name="symptoms"></a>Symptomer

Buntvaren er ikke tilgjengelig for bestillingen fordi hvis du undersøker salgsordrelinjene for buntvaren, vil du se at antallet er *0* (null), og at statusen er *Avbrutt*.

## <a name="resolution"></a>Løsning

Denne virkemåten er standard. Salgsordren kjøper bare komponentene til buntvaren. Selve buntvaren kjøpes ikke. Hvis du må kjøpe en bunt, bør du vurdere om du må merke den som buntvare, fordi denne funksjonaliteten er utformet for scenarioer med inntektsføring. Hvis du vil ha mer informasjon om buntvarer, se [Bunter](/dynamics365/finance/accounts-receivable/revenue-recognition-setup).
