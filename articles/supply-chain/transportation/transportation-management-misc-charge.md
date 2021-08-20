---
title: Tillegg for transportstyring
description: Dette emnet beskriver hvordan transportgenererte tillegg må knyttes til en tilleggskode.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 6d334a1ac290ab258964df2f146d9cbe30eb766f4002c8bae856cbe5499181b3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769521"
---
# <a name="transportation-management-miscellaneous-charges"></a>Tillegg for transportstyring

[!include [banner](../includes/banner.md)]

Som med alle tillegg må transportgenererte tillegg knyttes til en tilleggskode. Ellers blir de ikke lagt tilbake i ordren som et tillegg. **Tilleggskoden** bestemmer hvordan tillegget er i forhold til ordren og ordrelinjen der den er lagt til.

Gå til **Transportstyring > Oppsett > Vurdering > Tillegg** for å definere kvalifiseringskriteriene som bestemmer når en bestemt **tilleggskode** skal brukes på et tillegg.

Du må ha minst ett oppsett for hver relevante **tilleggsmodulinnstilling** (*kunde* og *leverandør*) der **Tilleggstypen** er angitt til *Ingen*. Hvis dette mangler, blir *ikke* tillegget lagt til i ordren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]