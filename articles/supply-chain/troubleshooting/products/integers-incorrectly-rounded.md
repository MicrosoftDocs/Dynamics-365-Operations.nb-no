---
title: Heltall avrundet feil i beregning av produktkonfigurasjonsmodeller
description: Heltallsresultater avrundes ikke alltid riktig når produktkonfigurasjonsmodeller beregnes. Løs problemet med et ekstra desimalattributt og beregning.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b17145d7d17cb784fe11b3fbf65ddf5aa5530f27
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477219"
---
# <a name="integers-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Heltall avrundet feil når produktkonfigurasjonsmodeller beregnes

## <a name="symptoms"></a>Symptomer

Dette problemet kan oppstå når du utfører følgende serie med handlinger:

1. Definer følgende attributter i en produksjonskonfigurasjonsmodell:

    - Inndata (heltall)
    - Prosent (desimal)
    - Resultat (heltall)

2. Opprett en beregning som har følgende uttrykk:

    *Resultat* = *inndata* × *prosent* ÷ 100

I dette tilfellet blir ikke heltallsresultatet alltid avrundet riktig. Hvis inndataene for eksempel er 1 000 og prosenten er 2,40, forventer du at heltallsresultatet blir 24, fordi 2,40 prosent av 1 000 er 24 (eller 24,00 i desimalskjema). Resultatet vises i stedet som 23. Når prosenten er 2,39, avrundes imidlertid beregningen til 24 i stedet for 23. Når prosenten er 2,50, avrundes beregningen til 25 som forventet.

## <a name="cause"></a>Årsak

Dette problemet oppstår på grunn av måten som Microsoft Solver Foundation internt representerer tall ved hjelp av brøker. I det foregående eksemplet representeres resultatet av beregningen der prosenten er 2,40 som 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375. Når .NET sender denne verdien som et heltall, returnerer den 23.

## <a name="resolution"></a>Løsning

Denne virkemåten vil ikke bli endret fordi andre scenarioer er avhengige av den. I det foregående eksemplet kan du løse problemet ved å introdusere et ekstra desimalattributt og beregninger.

Du kan for eksempel definere følgende attributter i en produksjonskonfigurasjonsmodell:

- Inndata (heltall)
- Prosent (desimal)
- ResultDecimal (desimal)
- ResultInteger (heltall)

Du kan deretter legge til følgende beregninger:

- *ResultDecimal* = *inndata* × *prosent* ÷ 100
- *ResultInteger* = *ResultDecimal*
