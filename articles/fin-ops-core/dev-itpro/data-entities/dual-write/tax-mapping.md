---
title: Integrert avgift
description: Denne artikkelen beskriver integreringen av avgiftsdata mellom Finance and Operations og Dataverse.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 29d8b2079b5d1cd70f14e096780f83a4a38d4b63
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111544"
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

