---
title: Salgsordrer kan ikke frigis med utgående lageroperasjoner
description: Det er flere årsaker til at du kan få en feilmelding om at en salgsordre ikke kan frigis. Denne siden beskriver hvorfor og hvordan du kan løse problemet.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fca5ee1bc97545ea4de56d940fdedd320a6cfe84
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477215"
---
# <a name="sales-order-could-not-be-released-with-outbound-warehouse-operations"></a>Salgsordrer kan ikke frigis med utgående lageroperasjoner

## <a name="symptoms"></a>Symptomer

Du kan få følgende feilmelding når du arbeider med utgående lageroperasjoner:

> Kan ikke frigi salgsordren.

## <a name="cause"></a>Årsak

Dette problemet kan oppstå av flere årsaker. Ordren er for eksempel på vent for kredittbehandling, og ingen forsendelser kan opprettes før en gyldig postadresse angis for alle salgslinjer som er tilknyttet en ordre. Det finnes også en ordresperre som må løses før ordren kan frigis til lageret. Denne sperringen kan være ordrespesifikk, eller den kan være på kundekontoen.

## <a name="resolution"></a>Løsning

Legg til eller oppdater adressen på salgsordren og ordrelinjene, og frigi deretter ordren til lageret. Ordrer kan bare frigis til lageret hvis de har en gyldig leveringsadresse (per adresseformatoppsettet i modulen **Organisasjonsstyring**).

Undersøk ordresperringen og løs problemene. Fjern deretter sperringen fra ordren eller kunden, og frigi ordren til lageret.
