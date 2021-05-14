---
title: Arbeid kan ikke avbrytes fordi det er blokkert
description: Arbeid kan ikke avbrytes fordi det er blokkert
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924285"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a>Arbeid kan ikke avbrytes fordi det er blokkert

Feilkode: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage

## <a name="symptoms"></a>Symptomer

Systemet viser følgende feilmelding:

> Arbeid %1 kan ikke avbrytes fordi det er sperret av årsakstypen %2. Blokkeringen av arbeid må oppheves før det kan avbrytes.

## <a name="cause"></a>Årsak

Arbeidet er blokkert og kan ikke avbrytes.

På **Arbeid**-siden i kategorien **Generelt** er alternativet **Blokkert** satt til *Ja*. Denne innstillingen angir at arbeidet er sperret. Kategorien **Blokkeringsårsaker** viser hvorfor arbeidet ble blokkert.

## <a name="resolution"></a>Oppløsning

Hvis du vil fjerne blokkeringen av arbeidet, velger du kategorien **Blokkeringsårsaker**, og deretter følger du ett av disse trinnene:

- Hvis feltet **Arbeidsblokkeringsårsak** er satt til *Udefinert årsak*: I handlingsruten i kategorien **Arbeid**, i **Arbeid**-gruppen, velger du **Opphev blokkering av arbeid**.
- Hvis feltet **Arbeidsblokkeringsårsak** er satt til *Behandler bølge*: I handlingsruten i kategorien **Relatert informasjon**, i gruppen **Relatert informasjon**, velger du **Bølge**. På **Bølger**-siden i handlingsruten i kategorien **Bølge** i **Bølge**-gruppen velger du **Rydd opp bølgedata**.

## <a name="workaround"></a>Løsning

Hvis de forrige trinnene ikke løste problemet, kan du avbryte arbeidet ved å følge disse trinnene.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Avbryt arbeid**.
1. I **Arbeids-ID**-feltet angir du IDen for arbeidet du vil avbryte, og som for øyeblikket har **Arbeidstatus**-verdien *Åpen*, *Pågår*, *Avbrutt*, *Kombinert* eller *Lukket*.
1. Velg **OK**.
1. Velg **Ja** for å bekrefte at du vil avbryte arbeidet.

For mer informasjon, se [Avbryte lagerarbeid for unntaksbehandling](../../warehousing/cancel-warehouse-work.md).
