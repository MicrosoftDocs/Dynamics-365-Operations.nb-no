---
title: Det tar lang tid å oppdatere planlagte ordrer
description: Når du oppdaterer behovsantallet eller leveringsdatoen på en planlagt ordre, tar det vanligvis minst 30 sekunder per ordre for å lagre oppdateringen
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ccf3305cc18ea0ccf2ac3e9ca0dd507fd12a9da7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477213"
---
# <a name="planned-orders-take-a-long-time-to-update"></a>Det tar lang tid å oppdatere planlagte ordrer

## <a name="symptoms"></a>Symptomer

Når du oppdaterer behovsantallet eller leveringsdatoen på en planlagt ordre, tar det vanligvis minst 30 sekunder per ordre for å lagre oppdateringen.

## <a name="resolution"></a>Løsning

Dette er et kjent problem med den innebygde hovedplanleggingsmotoren. Det skyldes den underliggende automatiske nedbrytingen gjennom stykklistestrukturen under redigeringer. Dette problemet omtales i planleggingsoptimalisering, der en planlegger kan oppdatere og godkjenne de relevante ordrene og, når det er ønskelig, utløse en planleggingskjøring for å oppdatere planlagte ordrer for den underliggende stykklistestrukturen.

Én måte å forbedre ytelsen med den innebygde hovedplanleggingsmotoren på er å gjøre følgende:

1. Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**.
1. Velg en plan.
1. Utvid hurtigfanen **Horisont i dager**.
1. Angi **Nedbryting** til *Ja*, og sett feltet under denne innstillingen til 0 (null).

> [!NOTE]
> Dette vil begrense perioden for nedbrytinger som utføres for denne hovedplanen, til én enkelt dag.
