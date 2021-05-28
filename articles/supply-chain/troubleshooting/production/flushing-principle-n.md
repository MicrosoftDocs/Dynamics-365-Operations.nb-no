---
title: Trekkprinsippinnstillinger på stykklistelinjer overholdes ikke
description: Trekkprinsippinnstillinger på stykklistelinjer overholdes ikke.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026781"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a>Trekkprinsippinnstillinger på stykklistelinjer overholdes ikke

KB-nummer: 4612725

## <a name="symptoms"></a>Symptomer

Dette problemet oppstår når feltet **Automatisk stykklisteforbruk** i kategorien **Automatisk oppdatering** på siden **Parametere for produksjonskontroll** er angitt til *Trekkprinsipp*. Denne innstillingen angir at alle stykklistelinjer automatisk skal forbrukes når en bestilling mottas. Hvis **Trekkprinsipp**-feltet på stykklistelinjer er uttrykkelig angitt til *Manuell*, kan du forvente at stykklistelinjene ikke forbrukes automatisk. Når dette problemet oppstår, blir imidlertid stykklistelinjer der **Trekkprinsipp**-feltet er satt til *Manuell*, automatisk forbrukt.

## <a name="resolution"></a>Oppløsning

Hvis du har dette problemet, kan det hende at produksjonskontrollparameterne er satt opp til å overstyre **Trekkprinsipp**-innstillinger på stykklistelinjer. Kontroller verdien i feltet **Automatisk stykklisteforbruk** på siden **Produksjonskontrollparametere** i kategorien **Automatisk oppdatering**. Hvis den er satt til *Alltid*, vil systemet ignorere innstillingen for **Trekkprinsipp** på alle stykklistelinjer, og linjene tømmes alltid. Hvis du vil at systemet skal overholde **Trekkprinsipp**-innstillingen på stykklistelinjer, endrer du verdien i feltet **Automatisk stykklisteforbruk** til *Trekkprinsipp*.
