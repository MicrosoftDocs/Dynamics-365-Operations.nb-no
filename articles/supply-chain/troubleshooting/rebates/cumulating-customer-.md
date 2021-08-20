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
ms.openlocfilehash: fc3381dab77cf80c0fd65f3bc27c11b814e72368631bd0e2145aac0be4f4fba4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760376"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Akkumulering av kunderabatter mislykkes når varerabattgrupper brukes

KB-nummer: 4611372

## <a name="symptoms"></a>Symptomer

Når du bruker kunderabattavtaler (av *beløp*-typen) sammen med varerabattgrupper, beregnes rabatter, men akkumulering mislykkes.

## <a name="resolution"></a>Oppløsning

Systemet fungerer som tiltenkt. Varegrupper grupperer bare varer som har samme terskelbetingelse. Rabattbetingelsen (terskel) angis mot beløpet for hver vare, ikke mot det akkumulerte beløpet for en vare i varegruppen.
