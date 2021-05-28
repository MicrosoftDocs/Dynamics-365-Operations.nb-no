---
title: Planlagt bestilling opprettes når det finnes et innkjøp innen negative dager
description: Hvis dekningskoden er Min/maks, oppretter Planleggingsoptimalisering et bestillingsforslag når det finnes et innkjøp innen negative dager.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026785"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a>Planlagt bestilling opprettes når det finnes et innkjøp innen negative dager

KB-nummer: 4614298

## <a name="symptoms"></a>Symptomer

Hvis dekningskoden er *Min/maks*, oppretter Planleggingsoptimalisering et bestillingsforslag når det finnes et innkjøp innen negative dager.

## <a name="resolution"></a>Oppløsning

Planleggingsoptimalisering støtter ikke negative dager. Det sikrer imidlertid alltid at planlagte bestillinger ikke blir planlagt innen leveringstiden i forhold til gjeldende dato. Leveringstiden for innkjøpet er for eksempel 10 dager, og en bestilling forventes å ankomme åtte dager fra i dag. I dette tilfellet vil bestillingen brukes som forsyning for etterspørsel som er fem dager fra i dag.

Vi anbefaler derfor at du justerer leveringstiden for å dekke alle (eller nesten alle) scenariene.
