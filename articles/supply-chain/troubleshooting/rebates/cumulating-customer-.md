---
title: Akkumulering av kunderabatter mislykkes når varerabattgrupper brukes
description: Når du bruker kunderabattavtaler sammen med varerabattgrupper, beregnes rabatter, men akkumulering mislykkes.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026769"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Akkumulering av kunderabatter mislykkes når varerabattgrupper brukes

KB-nummer: 4611372

## <a name="symptoms"></a>Symptomer

Når du bruker kunderabattavtaler (av *beløp*-typen) sammen med varerabattgrupper, beregnes rabatter, men akkumulering mislykkes.

## <a name="resolution"></a>Oppløsning

Systemet fungerer som tiltenkt. Varegrupper grupperer bare varer som har samme terskelbetingelse. Rabattbetingelsen (terskel) angis mot beløpet for hver vare, ikke mot det akkumulerte beløpet for en vare i varegruppen.
