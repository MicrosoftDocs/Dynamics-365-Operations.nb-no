---
title: Desimalrunding av det fysiske oppdateringsantallet er feil
description: Når du genererer en følgeseddel, inneholder den utgående lasten et antall som ikke samsvarer med desimalpresisjonen som er angitt i enheten.
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
ms.openlocfilehash: a9e0475aab452daa9e1a6f012e17a59e611010da
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920479"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a>Desimalrunding av det fysiske oppdateringsantallet er feil

Feilkode: SYS19589

## <a name="symptoms"></a>Symptomer

Når du genererer en følgeseddel, inneholder den utgående lasten et antall som ikke samsvarer med desimalpresisjonen som er angitt i enheten.

Når du prøver å generere en følgeseddel, viser systemet følgende feilmelding:

> Desimalavrunding av det fysiske oppdateringsantallet i enheten %1 er feil.

Derfor kan du ikke generere følgeseddelen for belastningen.

## <a name="cause"></a>Årsak

Systemet evaluerer om desimalavrundingen av forsendelsesantallet tilsvarer desimalpresisjonen som er definert for forsendelsesenheten. Når systemet runder av forsendelsesantallet til det angitte antallet desimaler, og det blir funnet ut at det avrundede forsendelsesantallet ikke samsvarer med det faktiske forsendelsesantallet, kan du ikke generere følgeseddelen. Dette problemet kan for eksempel oppstå hvis salgsantallet er 1,75 kilogram (kg), men desimalpresisjonen er satt til *1*.

## <a name="resolution"></a>Løsning

Lasten eller forsendelsen er for øyeblikket i en tilstand der generering av følgeseddel mislykkes. Du kan løse dette problemet ved å fullføre én eller flere av følgende oppgaver:

- Gå gjennom lastlinjene, og gjør justeringer for å sikre at antallet kan konverteres rent uten desimalnumre og andre avrundingsproblemer.
- Gjennomgå lastlinjene, og juster for å sikre at enheten og mengden justeres med desimalpresisjonen til enheten.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a>Gå gjennom lastlinjene, og gjør justeringer for å sikre at antallet kan konverteres rent uten desimalnumre og andre avrundingsproblemer

Bruk følgende prosedyre til å gå gjennom lastlinjene, og gjør justeringer for å sikre at antallet kan konverteres rent uten desimalnumre og andre avrundingsproblemer.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Velg lasten som følgeseddelen ikke kan genereres for.
1. I handlingsruten, i fanen **Send og motta** i gruppen **Omvendt**, velger du **Reverser forsendelsesbekreftelse**.
1. I fanen **Lastlinjer** velger du lastlinjen for varen som forårsaker problemet.
1. Velg **Reduser plukket antall** for å justere det plukkede antallet.
1. Velg **Ordre** i fanen **Linjedetaljer**.
1. Angi **Antall**-feltet til det plukkede antallet (det vil si til verdien til feltet **Antall for arbeid opprettet**), slik at generering av følgeseddel kan fortsette.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a>Gjennomgå lastlinjene, og juster for å sikre at enheten og mengden justeres med desimalpresisjonen til enheten

Bruk følgende prosedyre til å gjennomgå lastlinjene, og juster for å sikre at enheten og mengden justeres med desimalpresisjonen til enheten.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Velg lasten som følgeseddelen ikke kan genereres for.
1. I hurtigfanen **Lastlinjer** velger du lastlinjen for varen som forårsaker problemet. Noter verdien i feltene **Antall** og **Enhet**.
1. Gå til **Organisasjonsstyring \> Enheter \> Enheter**.
1. Velg enheten som følgeseddelen ikke kan genereres for.
1. Juster verdien i feltet **Desimalpresisjon** etter behov.
