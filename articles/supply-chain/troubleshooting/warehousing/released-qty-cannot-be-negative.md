---
title: Kan ikke oppdatere en lastlinje fordi det frigitte antallet vil være negativt
description: Dette problemet oppstår når oppdatering eller sletting av en lastlinje vil føre til et negativt frigitt antall.
author: GalynaFedorova
ms.date: 6/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSLoadLineUnShipQty,WHSLoadTable_WHSLoadLineUnShipQty,WHSLoadPlanningWorkbench_WHSLoadLineUnShipQty,WHSShipmentDetails_WHSLoadLineUnShipQty,WHSLoadPlanningListPage_DeleteButtonLoadLine,WHSLoadTable_DeleteButtonLoadLine,WHSLoadPlanningWorkbench_DeleteButtonLoadLine,WHSShipmentDetails_DeleteButtonShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a6325a632e1f68a0a3a9cb6b6091c48da014a405e8ce9ad69ea841f5cceb216f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728465"
---
# <a name="cant-update-a-load-line-because-the-released-quantity-would-be-negative"></a>Kan ikke oppdatere en lastlinje fordi det frigitte antallet vil være negativt

Feilkode: @WAX:ReleasedQtyCannotBeNegative

## <a name="symptoms"></a>Symptomer

Dette problemet oppstår når oppdatering eller sletting av en lastlinje vil føre til et negativt frigitt antall. I dette tilfellet, når du prøver å oppdatere eller slette innlastingslinjen, viser systemet følgende feilmelding:

> Frigitt antall kan ikke være negativt for vare %1, parti %2.

Derfor kan du ikke oppdatere eller slette innlastingslinjen.

## <a name="cause"></a>Årsak

Når du har oppdatert eller slettet en innlastingslinje, oppdaterer systemet det frigitte antallet for den relaterte salgslinjen (*whsSalesLine.ReleaseQty*). Systemet evaluerer det frigitte antallet, og hvis det finner ut at det frigitte antallet på linjen vil være negativt etter oppdateringen, kan du ikke oppdatere eller slette linjen. Denne valideringen skjer hver gang du prøver å oppdatere enten belastningslinjeantallet eller måleenheten gjennom ulike handlinger, for eksempel slette en belastningslinje, slette en forsendelse, endre antallet for en belastningslinje, redusere det plukkede antallet og plukking med mangler.

Den vanligste rotårsaken til dette problemet er en endring i enhetskonverteringen som brukes for åpne belastningslinjer. Enhetsomregningen da en salgsordre ble frigitt, var for eksempel *50 Ea = 1 PL*. Før den tilknyttede belastningsforsendelsen ble ferdigstilt, ble imidlertid enhetsomregningen endret til *100 Ea = 1 PL*.

## <a name="resolution"></a>Løsning

Løsningen er å tilbakestille enhetskonverteringsendringene, oppdatere eller slette belastningslinjen og deretter implementere omregningen på nytt. Du må hindre at andre belastninger som omfatter varen som forårsaket problemet, behandles til problemet er løst. Ellers kan de nye konverteringene brukes for andre belastninger som allerede er åpne.

Du kan løse dette problemet ved å fullføre følgende oppgaver:

1. Gå gjennom enhetsomregningen som ble brukt for belastningslinjen.
2. Gå gjennom den gjeldende enhetskonverteringen for varen, og foreta justeringer som gjør at belastningslinjen kan oppdateres eller slettes.
3. Oppdater eller slett belastningslinjen, og tilbakestill enhetskonverteringsjusteringene.

### <a name="review-the-unit-conversion-that-was-used-for-the-load-line"></a>Gå gjennom enhetsomregningen som ble brukt for belastningslinjen

Bruk fremgangsmåten nedenfor til å se gjennom belastningslinjene og notere deg enhetsomregningen som ble brukt for belastningslinjen.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Velg belastningen som inkluderer belastningslinjen som ikke kan slettes eller oppdateres.
1. I handlingsruten, i fanen **Laster** i gruppen **Relatert informasjon**, velger du **Arbeid**.
1. Velg den aktuelle arbeids-ID-en i det øvre rutenettet.
1. I fanen **Generelt** nederst på siden beregner du omregningssatsen mellom verdien **Lagerarbeidsantall** og verdien **Arbeidsantall**. Noter satsen.
1. Gjenta denne fremgangsmåten for alle relevante arbeids-ID-er for å være sikker på at den samme omregningen ble brukt.

### <a name="review-the-current-unit-conversion-for-the-item-and-make-adjustments"></a>Gå gjennom den gjeldende enhetskonverteringen for varen, og foreta justeringer

Bruk følgende prosedyre til å gjennomgå produktets enhetsomregning, og juster for å sikre at enhetsimregningen justeres med lastlinjen.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Åpne det relevante produktet for å gå til siden **Detaljer om frigitt produkt**.
1. I gruppen **Oppsett** i fanen **Produkt** i handlingsruten velger du **Enhetskonverteringer**.
1. Velg omregningen mellom enhetene, og gjør justeringer ved hjelp av omregningen du fant i den forrige delen.

### <a name="update-or-delete-the-load-line-and-revert-the-unit-conversion-adjustments"></a>Oppdater eller slett belastningslinjen, og tilbakestill enhetsomregningsjusteringene

Bruk fremgangsmåten nedenfor til å behandle belastningslinjen etter behov og tilbakestille enhetsomregningene.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Åpne belastningen som inkluderer belastningslinjen som ikke kan slettes eller oppdateres.
1. I hurtigfanen **Lastlinjer** velger du lastlinjen.
1. Fortsett med de nødvendige handlingene etter behov. (Du kan for eksempel slette belastningslinjen eller endre antallet.)
1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Åpne det relevante produktet for å gå til siden **Detaljer om frigitt produkt**.
1. I gruppen **Oppsett** i fanen **Produkt** i handlingsruten velger du **Enhetskonverteringer**.
1. Velg omregningen mellom enhetene, og reverser justeringer som du gjorde i den forrige delen.
