---
title: Antallet overskrider overleveringsprosenten under generering av følgeseddel
description: Når du genererer en følgeseddel, inneholder den utgående belastningen et antall som overskrider overleveringsprosenten.
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
ms.openlocfilehash: 00e3da7767b80e16f9351f59b109765bffc0128fe149cefafc1edda3a6cbcb96
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781351"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a>Antallet overskrider overleveringsprosenten under generering av følgeseddel

Feilkode: SYS24920

## <a name="symptoms"></a>Symptomer

Når du genererer en følgeseddel, inneholder den utgående belastningen et antall som overskrider overleveringsprosenten.

Når du prøver å generere en følgeseddel, viser systemet følgende feilmelding:

> Linjen overleveres med %1 prosent, men tillatt overlevering er bare %2 prosent.

Derfor kan du ikke generere følgeseddelen for belastningen.

## <a name="cause"></a>Årsak

Det plukkede antallet for lasten eller forsendelsen er mer enn det bestilte antallet og er ikke innenfor området for overleveringsprosenten.

## <a name="resolution"></a>Løsning

Lasten eller forsendelsen er for øyeblikket i en tilstand der generering av følgeseddel mislykkes. Du kan løse dette problemet ved å fullføre én eller flere av følgende oppgaver:

- Juster lastlinjeantallet.
- Justere overleveringsprosenten.
- Reverser og foreta justeringer.

### <a name="adjust-the-load-line-quantity"></a>Juster lastlinjeantallet

Bruk fremgangsmåten nedenfor til å justere lastlinjeantallet.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Velg lasten som følgeseddelen ikke kan genereres for.
1. I handlingsruten, i fanen **Send og motta** i gruppen  **Omvendt**, velger du  **Reverser forsendelsesbekreftelse**.
1. I fanen  **Lastlinjer** velger du lastlinjen for varen som overskrider overleveringsprosenten.
1. Velg **Reduser plukket antall** for å justere det plukkede antallet.
1. Velg  **Ordre** i kategorien **Linjedetaljer**.
1. Angi **Antall**-feltet til det plukkede antallet (det vil si til verdien til feltet **Antall for arbeid opprettet**), slik at generering av følgeseddel kan fortsette.

### <a name="adjust-the-over-delivery-percentage"></a>Justere overleveringsprosenten

Bruk fremgangsmåten nedenfor til å justere overleveringsprosenten.

1. Gå til **Kunder \> Ordrer \> Alle ordrer**.
1. Velg salgsordren du ikke kan postere en følgeseddel for lasten for.
1. I fanen  **Salgsordrelinjer** velger du salgsordrelinjen for varen som overskrider overleveringsprosenten.
1. Velg  **Levering** i kategorien **Linjedetaljer**.
1. Sett **Overlevering**-feltet til en større prosent som legger til rette for antallet som er plukket mot lastantallet, slik at generering av følgeseddel kan fortsette.

### <a name="reverse-and-make-adjustments"></a>Reversere og foreta justeringer

Tilbakefør alt som er postert for lasten (for eksempel følgeseddel, forsendelsesbekreftelse og arbeid), foreta salgsordrejusteringer, frigi ordren til lageret på nytt, og fullfør forsendelsesprosedyren.

Bruk fremgangsmåten nedenfor til å avbryte en følgeseddel.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. I handlingsruten, i fanen **Send og motta** i gruppen  **Omvendt**, velger du  **Annuller følgesedler**.

Bruk fremgangsmåten nedenfor til å tilbakeføre en forsendelsesbekreftelse.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. I handlingsruten, i fanen **Send og motta** i gruppen  **Omvendt**, velger du  **Reverser forsendelsesbekreftelse**.

Bruk fremgangsmåten nedenfor for å reversere arbeid.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. I handlingsruten velger du **Reverser arbeid** i fanen  **Laster** i gruppen  **Arbeid**.
