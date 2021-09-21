---
title: Jobber som pågår, avsluttes når du rapporterer delantall på siste jobb
description: Når du bruker prosjektkortenheten til å rapportere et delvis antall i det siste prosjektet i en produksjonsordre, avsluttes alle de forrige prosjektene som har statusen Pågår automatisk.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 11511d4ac7524facdd0d647e9bc38fe09c282be1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477242"
---
# <a name="previous-in-progress-jobs-are-ended-when-reporting-partial-quantity-on-last-job"></a>Tidligere jobber som pågår, avsluttes når du rapporterer delantall på siste jobb

## <a name="symptoms"></a>Symptomer

Når du bruker prosjektkortenheten til å rapportere et delvis antall i det siste prosjektet i en produksjonsordre, avsluttes alle de forrige prosjektene i den ordren som har statusen Pågår automatisk.

## <a name="resolution"></a>Løsning

Denne virkemåten er standard. På siden **Produksjonsordrestandarder** i fanen **Ferdigmeld** finnes det et alternativ som heter **Sluttmerk rute**. Hvis dette emnet er satt til *Ja*, posteres en rutekortjournal når en arbeider bruker prosjektkortenheten eller prosjektkortterminalen til å rapportere den siste operasjonen. Denne journalen markerer alle operasjoner som fullført, og avslutter alle produksjonsprosjektene. Når **Sluttmerk rute**-alternativet er satt til *Ja*, vurderer ikke systemet prosjektstatusen som arbeideren valgte da vedkommende sist rapporterte operasjonen. Systemet vurderer heller ikke om arbeideren rapporterer et fullstendig eller delvis antall.
