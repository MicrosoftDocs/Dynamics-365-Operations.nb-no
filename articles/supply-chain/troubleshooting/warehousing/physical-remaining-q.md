---
title: Fysisk restantall i enheten kan ikke være null
description: Når du genererer en følgeseddel, har dataene som leveres til den, et lagerantall som ikke er null, men et null salgsantall.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 187363db3030ee0741f0c7e7746295b88320162c156120112332bb78593bb673
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744660"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a>Fysisk restantall i enheten kan ikke være null

Feilkode: SYS19591

## <a name="symptoms"></a>Symptomer

Når du genererer en følgeseddel, har dataene som leveres til den, et lagerantall som ikke er null, men et null salgsantall.

Når du prøver å generere følgeseddelen, viser systemet følgende feilmelding:

> Fysisk rest i enheten %1 må være forskjellig fra null.

Derfor kan du ikke generere følgeseddelen for belastningen.

## <a name="cause"></a>Årsak

Systemet evaluerer det fysiske restantallet i lagerenheten og det fysiske restantallet i forsendelsesenheten. Hvis systemet finner ut at det fysiske restantallet i forsendelsesenheten er 0 (null), men det fysiske restantallet i lagerenheten ikke er 0, kan du ikke generere følgeseddelen. Dette problemet kan for eksempel oppstå hvis salgsenheten og lagerenheten for varen er forskjellig, og omregningen mellom enheter ikke er nøyaktig.

## <a name="resolution"></a>Løsning

Lasten eller forsendelsen er for øyeblikket i en tilstand der generering av følgeseddel mislykkes. Du kan løse dette problemet ved å fullføre én eller flere av følgende oppgaver:

- Gå gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.
- Gå gjennom belastningslinjene, og gjør justeringer for å sikre at antallet kan konverteres rent uten avrundingsproblemer.
- Gjennomgå lastlinjene, og juster for å sikre at enheten og mengden justeres med desimalpresisjonen til enheten.
- Kontroller at lagermåleenheten er mindre enn salgsmåleenheten.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Gå gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer

Bruk følgende fremgangsmåte til å g gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Velg belastningen som forsendelsen ikke kan bekreftes for.
1. I hurtigfanen **Lastlinjer** velger du lastlinjen.
1. Legg merke til verdien i feltet **Antall for arbeid opprettet**.
1. I handlingsruten, i fanen **Laster** i gruppen **Relatert informasjon**, velger du **Arbeid**.
1. Kontroller at arbeidet er fullført på det endelige forsendelsesstedet, og at det plukkede arbeidsantallet samsvarer med det opprettede arbeidsantallet på belastningslinjen.
1. Gjenta denne fremgangsmåten for alle belastningslinjer for å være sikker på at alle kriteriene er oppfylt.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a>Gå gjennom belastningslinjene, og gjør justeringer for å sikre at antallet kan konverteres rent uten avrundingsproblemer

Bruke følgende prosedyre til å gå gjennom belastningslinjene, og gjør justeringer for å sikre at antallet kan konverteres rent uten avrundingsproblemer.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Velg lasten som følgeseddelen ikke kan genereres for.
1. I handlingsruten, i fanen **Send og motta** i gruppen  **Omvendt**, velger du  **Reverser forsendelsesbekreftelse**.
1. I fanen  **Lastlinjer** velger du lastlinjen for varen som overskrider overleveringen.
1. Velg **Reduser plukket antall** for å justere det plukkede antallet.
1. Velg  **Ordre** i kategorien **Linjedetaljer**.
1. Angi **Antall**-feltet til det plukkede antallet (det vil si til verdien til feltet **Antall for arbeid opprettet**), slik at generering av følgeseddel kan fortsette.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a>Gjennomgå lastlinjene, og juster for å sikre at enheten og mengden justeres med desimalpresisjonen til enheten

Bruk følgende prosedyre til å gjennomgå lastlinjene, og juster for å sikre at enheten og mengden justeres med desimalpresisjonen til enheten.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Velg lasten som følgeseddelen ikke kan genereres for.
1. I hurtigfanen **Lastlinjer** velger du lastlinjen for varen som forårsaker problemet. Noter verdien i feltene **Antall** og **Enhet**.
1. Gå til **Organisasjonsstyring \> Enheter \> Enheter**.
1. Velg enheten som følgeseddelen ikke kan genereres for.
1. Juster verdien i feltet **Desimalpresisjon** etter behov.

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a>Kontroller at lagermåleenheten er mindre enn salgsmåleenheten

Kontroller at lagermåleenheten er mindre enn salgsmåleenheten. Vurder om du skal konfigurere måleenheten for varen på nytt etter behov.
