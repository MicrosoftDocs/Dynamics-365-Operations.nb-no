---
title: Antallet overskrider underleveringsprosenten under generering av følgeseddel
description: Når du genererer en følgeseddel, inneholder den utgående belastningen et antall som overskrider underleveringsprosenten.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7cdc22eeabda6cf9f08484d698e5096f66af4a12
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920704"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a>Antallet overskrider underleveringsprosenten under generering av følgeseddel

Feilkode: SYS24921

## <a name="symptoms"></a>Symptomer

Når du genererer en følgeseddel, inneholder den utgående belastningen et antall som overskrider underleveringsprosenten.

Når du prøver å generere en følgeseddel, viser systemet følgende feilmelding:

> Linjen underleveres med %1 prosent, men tillatt underlevering er bare %2 prosent.

Derfor kan du ikke generere følgeseddelen for belastningen.

## <a name="cause"></a>Årsak

Det plukkede antallet for lasten eller forsendelsen er mindre enn det bestilte antallet og er ikke innenfor området for underleveringsprosenten.

## <a name="resolution"></a>Løsning

Lasten eller forsendelsen er for øyeblikket i en tilstand der generering av følgeseddel mislykkes. Du kan løse dette problemet ved å fullføre én eller flere av følgende oppgaver:

- Juster underleveringsprosenten.
- Reverser og foreta justeringer.

### <a name="adjust-the-under-delivery-percentage"></a>Justere underleveringsprosenten

Bruk fremgangsmåten nedenfor til å justere underleveringsprosenten.

1. Gå til **Kunder \> Ordrer \> Alle ordrer**.
1. Velg salgsordren du ikke kan postere en følgeseddel for lasten for.
1. I fanen **Salgsordrelinjer** velger du salgsordrelinjen for varen som overskrider underleveringsprosenten.
1. Velg **Levering** i fanen **Linjedetaljer**.
1. Sett **Underlevering**-feltet til en større prosent som legger til rette for antallet som er plukket mot lastantallet, slik at generering av følgeseddel kan fortsette.

### <a name="reverse-and-make-adjustments"></a>Reversere og foreta justeringer

Tilbakefør alt som er postert for lasten (for eksempel følgeseddel, forsendelsesbekreftelse og arbeid), foreta salgsordrejusteringer, frigi ordren til lageret på nytt, og fullfør forsendelsesprosedyren.

Bruk fremgangsmåten nedenfor til å avbryte en følgeseddel.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. I handlingsruten, i fanen **Send og motta** i gruppen **Omvendt**, velger du **Annuller følgesedler**.

Bruk fremgangsmåten nedenfor til å tilbakeføre en forsendelsesbekreftelse.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. I handlingsruten, i fanen **Send og motta** i gruppen **Omvendt**, velger du **Reverser forsendelsesbekreftelse**.

Bruk fremgangsmåten nedenfor for å reversere arbeid.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. I handlingsruten velger du **Reverser arbeid** i fanen **Laster** i gruppen **Arbeid**.
