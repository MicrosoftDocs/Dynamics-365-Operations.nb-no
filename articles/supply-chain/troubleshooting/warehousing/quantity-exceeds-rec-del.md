---
title: Antallet du prøver å oppdatere, overskrider det mottatte/leverte antallet.
description: Når du genererer en følgeseddel, inneholder den utgående lasten et antall som overskrider arbeidsantallet som ble plukket og reservert for salgsordren.
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
ms.openlocfilehash: 25507a482b2db7c01f56679bf3e8454249de3a6b9965f9c359a2ebe2cc8445ce
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711693"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a>Antallet du prøver å oppdatere, overskrider det mottatte/leverte antallet

Feilkode: SYS7676

## <a name="symptoms"></a>Symptomer

Når du genererer en følgeseddel, inneholder den utgående lasten et antall som overskrider arbeidsantallet som ble plukket og reservert for salgsordren.

Når du prøver å generere en følgeseddel, viser systemet følgende feilmelding:

> Antallet du prøver å oppdatere, er større enn det mottatte/leverte antallet.

Derfor kan du ikke generere følgeseddelen for belastningen.

## <a name="cause"></a>Årsak

Det plukkede arbeidsantallet samsvarer ikke med det opprettede arbeidsantallet på belastningslinjen. Dette problemet kan for eksempel oppstå hvis belastningslinjeantallet, antall for arbeid opprettet eller det plukkede antallet ikke er nøyaktig.

## <a name="resolution"></a>Løsning

Lasten eller forsendelsen er for øyeblikket i en tilstand der generering av følgeseddel mislykkes. Du kan løse dette problemet ved å fullføre én eller flere av følgende oppgaver:

- Gå gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.
- Juster lastlinjeantallet.
- Tilbakefør alle plukkregistreringer, og gjør om plukking.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Gå gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer

Bruk følgende fremgangsmåte til å g gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Velg lasten som forsendelsen ikke kan genereres for.
1. I hurtigfanen **Lastlinjer** velger du lastlinjen.
1. Legg merke til verdien i feltet **Antall for arbeid opprettet**.
1. I handlingsruten, i fanen **Laster** i gruppen **Relatert informasjon**, velger du **Arbeid**.
1. Kontroller at arbeidet er fullført på det endelige forsendelsesstedet, og at det plukkede arbeidsantallet samsvarer med det opprettede arbeidsantallet på belastningslinjen.
1. Gjenta denne fremgangsmåten for alle belastningslinjer for å være sikker på at alle kriteriene er oppfylt.

### <a name="adjust-the-load-line-quantity"></a>Juster lastlinjeantallet

Bruk fremgangsmåten nedenfor til å justere lastlinjeantallet.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Velg lasten som følgeseddelen ikke kan genereres for.
1. I handlingsruten, i fanen **Send og motta** i gruppen  **Omvendt**, velger du  **Reverser forsendelsesbekreftelse**.
1. I fanen  **Lastlinjer** velger du lastlinjen for varen som forårsaker problemet.
1. Velg **Reduser plukket antall** for å justere det plukkede antallet.
1. Angi feltet **Reduser lastlinje** for å gjenspeile justeringer på lastlinjen.

### <a name="reverse-all-pick-registrations-and-redo-picking"></a>Tilbakefør alle plukkregistreringer, og gjør om plukking

Hvis noen brukte plukkregistrering til å lukke en lastlinje uten arbeid, kan det oppstå et avvik mellom lastlinjeantallet og det plukkede antallet. I dette tilfellet må manuell plukkregistrering tilbakeføres, og plukking må deretter fullføres ved hjelp av mobilappen Warehouse Management.

Bruk fremgangsmåten nedenfor til å tilbakeføre plukkregistreringen.

1. Gå til **Kunder \> Ordrer \> Alle ordrer**.
1. Velg salgsordren du ikke kan postere en følgeseddel for lasten for.
1. I fanen **Salgsordrelinjer** velger du salgsordrelinjen som plukkregistreringen ble utført for.
1. Velg **Oppdater linje \> Plukk** for å fjerne merket for varene.
