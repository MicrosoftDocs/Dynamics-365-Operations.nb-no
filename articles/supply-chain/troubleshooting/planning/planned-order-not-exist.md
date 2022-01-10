---
title: Systemet finner ikke en planlagt bestilling under operasjoner på flere bestillinger
description: Feilmeldingen Planlagt bestilling finnes ikke når du utfører operasjoner på flere planlagte bestillinger, og minst to ordrer tilhører samme vare-ID.
author: t-benebo
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo_ReqTransPoMarkChangeType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0ece4a331b63b86e896c5b337a58185ed3ea1049
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920809"
---
# <a name="the-system-cant-find-a-planned-order-during-operations-on-multiple-orders"></a>Systemet finner ikke en planlagt bestilling under operasjoner på flere bestillinger

Feilkode: SYS24774

## <a name="symptoms"></a>Symptomer

Du mottar følgende feilmelding når du prøver å utføre en operasjon på flere planlagte bestillinger samtidig, og minst to av bestillingene tilhører samme vare-ID. Feilen kan for eksempel oppstå når bestillingene blir autorisert eller ordretypen endres.

> Planlagt bestilling %1 finnes ikke.

## <a name="cause"></a>Årsak

Når systemet autoriserer eller endrer ordretypen, må det vurdere eksisterende planlagte bestillinger på nytt for varen, for å sikre at den planlagte forsyningen samsvarer med behovet og den eksisterende forsyningen. Som en del av denne prosessen oppretter systemet planlagte bestillinger på nytt for varen. Den andre planlagte bestillingen som systemet forventer å behandle, finnes ikke lenger.

## <a name="workaround"></a>Løsning

Godkjenn ordrene før du behandler dem. På denne måten slettes ikke bestillingene når systemet behandler den første bestillingen for varen.
