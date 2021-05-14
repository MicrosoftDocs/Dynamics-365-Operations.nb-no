---
title: Arbeid gjenstår å blokkere
description: Arbeid gjenstår å blokkere
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924136"
---
# <a name="work-remains-blocked"></a>Arbeid gjenstår å blokkere

Feilkode: WHSWorkBlockingExecutingWaveReason_ErrorMessage

## <a name="symptoms"></a>Symptomer

Systemet viser følgende feilmelding:

> Arbeidet %1 er fortsatt blokkert fordi den relaterte bølgen %2 har statusen %3.

## <a name="cause"></a>Årsak

Arbeidet behandles i øyeblikket i en bølge, og blokkeringen kan ikke oppheves, som angitt ved en av følgende betingelser:

- I kategorien **Blokkeringsårsaker** er feltet **Arbeidsblokkeringsårsak** for en eller flere linjer satt til *Behandler bølge*.
- Når du velger **Bølge** i gruppen **Beslektet informasjon** i kategorien **Beslektet informasjon** i handlingsruten, er feltet **Bølgestatus** satt til *Behandling*.

## <a name="resolution"></a>Oppløsning

Velg **Bølge** i gruppen **Beslektet informasjon** i fanen **Beslektet informasjon** i handlingsruten. På **Bølger**-siden i handlingsruten i kategorien **Bølge** i **Bølge**-gruppen velger du **Rydd opp bølgedata**.

## <a name="workaround"></a>Løsning

Hvis de forrige trinnene ikke løste problemet, kan du avbryte arbeidet ved å følge disse trinnene.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Avbryt arbeid**.
1. I **Arbeids-ID**-feltet angir du IDen for arbeidet du vil avbryte, og som for øyeblikket har **Arbeidstatus**-verdien *Åpen*, *Pågår*, *Avbrutt*, *Kombinert* eller *Lukket*.
1. Velg **OK**.
1. Velg **Ja** for å bekrefte at du vil avbryte arbeidet.

For mer informasjon, se [Avbryte lagerarbeid for unntaksbehandling](../../warehousing/cancel-warehouse-work.md).
