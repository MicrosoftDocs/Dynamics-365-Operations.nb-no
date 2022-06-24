---
title: Tillegg for transportstyring
description: Denne artikkelen beskriver hvordan transportgenererte tillegg må knyttes til en tilleggskode.
author: Weijiesa
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8cc4c595d8b61cb9b6c81af4bf7f03faa1a12960
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849220"
---
# <a name="transportation-management-miscellaneous-charges"></a>Tillegg for transportstyring

[!include [banner](../includes/banner.md)]

Som med alle tillegg må transportgenererte tillegg knyttes til en tilleggskode. Ellers blir de ikke lagt tilbake i ordren som et tillegg. **Tilleggskoden** bestemmer hvordan tillegget er i forhold til ordren og ordrelinjen der den er lagt til.

Gå til **Transportstyring > Oppsett > Vurdering > Tillegg** for å definere kvalifiseringskriteriene som bestemmer når en bestemt **tilleggskode** skal brukes på et tillegg.

Du må ha minst ett oppsett for hver relevante **tilleggsmodulinnstilling** (*kunde* og *leverandør*) der **Tilleggstypen** er angitt til *Ingen*. Hvis dette mangler, blir *ikke* tillegget lagt til i ordren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]