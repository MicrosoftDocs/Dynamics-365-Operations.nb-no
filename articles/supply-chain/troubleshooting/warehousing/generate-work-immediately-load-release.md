---
title: Generer plukkarbeid umiddelbart når last frigis
description: Hvis arbeid må genereres umiddelbart når lasten frigis, må du konfigurere bølgemalen i henhold til dette. Denne siden går gjennom trinnene.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fdeb0b27f4d2c1a2cc9f8e0c4ba537cdce604bd2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477218"
---
# <a name="picking-work-isnt-generated-immediately-when-outbound-load-is-released"></a>Plukkarbeid genereres ikke umiddelbart når utgående last frigis

## <a name="symptoms"></a>Symptomer

Du oppretter en utgående last ved å bruke en salgs- eller overføringsordre og frigi belastningen til lageret. Du legger imidlertid merke til at det ennå ikke er generert noe plukkarbeid.

## <a name="resolution"></a>Løsning

Hvis arbeid må genereres umiddelbart når lasten frigis, må du konfigurere bølgemalen i henhold til dette. I bølgemalen angir du følgende alternativer til *Ja*:

- Automatisk oppretting av bølge
- Behandle bølge ved frigivelse til lager
- Frigi bølge automatisk
