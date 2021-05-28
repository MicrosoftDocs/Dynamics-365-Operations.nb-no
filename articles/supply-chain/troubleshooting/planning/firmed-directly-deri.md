---
title: Direkte avledede autoriserte ordrer behandles av en Til vurdering-arbeidsflyt
description: Direkte avledede autoriserte ordrer behandles av en arbeidsflyt som har statuen Til vurdering.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026787"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>Direkte avledede autoriserte ordrer behandles av en Til vurdering-arbeidsflyt

KB-nummer: 4612450

## <a name="symptoms"></a>Symptomer

Direkte avledede autoriserte ordrer behandles av en arbeidsflyt som har statuen *Til vurdering*.

## <a name="resolution"></a>Oppløsning

Når endringssporing er aktivert, er statusen *Til vurdering* tilordnet til autoriserte avledede ordrer (bestillinger fra underleverandør). Hvis en bestilling er avledet (en underleverandørbestilling), blir den bare sendt til en arbeidsflyt. Hvis en bestilling er et autorisert bestillingsforslag, godkjennes det automatisk for å sikre at planleggingsmotoren ikke oppretter nye planlagte bestillinger mens bestillingen fremdeles har *Utkast*-status.
