---
title: Plukket antall er ikke tilstrekkelig under følgeseddelgenerering
description: Når du genererer en følgeseddel, inneholder den utgående lasten et plukket antall som ikke samsvarer med det opprettede arbeidsantallet på lastlinjen.
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
ms.openlocfilehash: 6febc340f140d0b3a3f08ea32a59d9eb4e6e5204
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920454"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a>Plukket antall er ikke tilstrekkelig under følgeseddelgenerering

Feilkode: SYS54073

## <a name="symptoms"></a>Symptomer

Når du genererer en følgeseddel, inneholder den utgående lasten et plukket antall som ikke samsvarer med det opprettede arbeidsantallet på lastlinjen.

Når du prøver å generere en følgeseddel, viser systemet følgende feilmelding:

> Siden %1 er plukket, er det ikke nok å oppdatere %2 når resten må være %3.

Derfor kan du ikke generere følgeseddelen for belastningen.

## <a name="cause"></a>Årsak

Følgeseddelen kan ikke genereres i gjeldende tilstand, fordi det kan hende at én av følgende betingelser finnes:

- Det relaterte arbeidet er ennå ikke plukket og flyttet til den endelige forsendelseslokasjonen.
- Det plukkede arbeidsantallet samsvarer ikke med det opprettede arbeidsantallet på belastningslinjen.
- Lastlinjeantall, antall for arbeid opprettet og plukket antall samsvarer ikke.

## <a name="resolution"></a>Løsning

Lasten eller forsendelsen er for øyeblikket i en tilstand der generering av følgeseddel mislykkes. Du kan løse dette problemet ved å fullføre én eller flere av følgende oppgaver:

- Gå gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.
- Juster lastlinjeantallet.
- Tilbakefør alle plukkregistreringer, og gjør om plukking.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Gå gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer

Bruk følgende fremgangsmåte til å g gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Velg lasten som følgeseddelen ikke kan genereres for.
1. I hurtigfanen **Lastlinjer** velger du lastlinjen.
1. Legg merke til verdien i feltet **Antall for arbeid opprettet**.
1. I handlingsruten, i fanen **Laster** i gruppen **Relatert informasjon**, velger du **Arbeid**.
1. Kontroller at arbeidet er fullført på det endelige forsendelsesstedet, og at det plukkede arbeidsantallet samsvarer med det opprettede arbeidsantallet på belastningslinjen.
1. Gjenta denne fremgangsmåten for alle belastningslinjer for å være sikker på at alle kriteriene er oppfylt.

### <a name="adjust-the-load-line-quantity"></a>Juster lastlinjeantallet

Bruk fremgangsmåten nedenfor til å justere lastlinjeantallet.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Velg lasten som følgeseddelen ikke kan genereres for.
1. I handlingsruten, i fanen **Send og motta** i gruppen **Omvendt**, velger du **Reverser forsendelsesbekreftelse**.
1. I fanen **Lastlinjer** velger du lastlinjen for varen som forårsaker problemet.
1. Velg **Reduser plukket antall** for å justere det plukkede antallet.
1. Angi feltet **Reduser lastlinje** for å gjenspeile justeringer på lastlinjen.

### <a name="reverse-all-pick-registrations-and-redo-picking"></a>Tilbakefør alle plukkregistreringer, og gjør om plukking

Problemet kan oppstå fordi noen brukte plukkregistrering til å lukke en lastlinje uten arbeid. I dette tilfellet må manuell plukkregistrering tilbakeføres, og plukking må deretter fullføres ved hjelp av mobilappen Warehouse Management.

Bruk fremgangsmåten nedenfor til å tilbakeføre plukkregistreringen.

1. Gå til **Kunder \> Ordrer \> Alle ordrer**.
1. Velg salgsordren du ikke kan postere en følgeseddel for lasten for.
1. I fanen **Salgsordrelinjer** velger du salgsordrelinjen som plukkregistreringen ble utført for.
1. Velg **Oppdater linje \> Plukk** for å fjerne merket for varene.
