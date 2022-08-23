---
title: Integrert avgift
description: Denne artikkelen beskriver integreringen av avgiftsdata mellom Finance and Operations og Dataverse.
author: josaw
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8f148b710e2294edf1e402b9b8b22cb24e60a1f2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288802"
---
# <a name="integrated-tax"></a>Integrert avgift

[!include [banner](../../includes/banner.md)]



Avgiftsoppsettsdata definerer oppsettet for både indirekte avgifter (mva, merverdiavgift, salgsskatt) og kildeskatt. Den beskriver avgiftsberegningsregelen, mva-satsen, avgiftsregnskapet, utligningen og andre begreper.

## <a name="templates"></a>Maler

Avgiftsdata inkluderer en samling tabelltilordninger som fungerer sammen under datasamhandling, som vist i følgende tabell.

| Finance and Operations-apper | Kundeengasjementsapper | Beskrivelse |
|-----------------------------|-----------------------------------|-------------|
[Varens mva-gruppe](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Skattemyndigheter](mapping-reference.md#193) | msdyn_taxauthorities | |
[Enhet for mva-fritakskoder for CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Mva-grupper](mapping-reference.md#195) | msdyn_taxgroups | |
[Finansposteringsgrupper for mva V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Kildeskattkoder](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Kildeskattgrupper](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

