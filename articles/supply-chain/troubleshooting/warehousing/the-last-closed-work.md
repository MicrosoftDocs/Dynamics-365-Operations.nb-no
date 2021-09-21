---
title: Siste lukkede arbeidslinje må være av typen Plasser
description: Siste lukkede arbeidslinje må være av typen Plasser
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 221c64c89d0e8addbf44acab8e7561e5f3a27239
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474754"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a>Siste lukkede arbeidslinje må være av typen Plasser

Feilkode: WAX1285

## <a name="symptoms"></a>Symptomer

Systemet viser følgende feilmelding:

> Siste lukkede arbeidslinje må være av typen Plasser.

## <a name="cause"></a>Årsak

Arbeidet kan ikke avbrytes med gjeldende status.

På den siste arbeidslinjen er **Arbeidsstatus**-feltet satt til *Lukket*, men **Arbeidstype**-feltet er satt til *Plasser*.

## <a name="resolution"></a>Oppløsning

Følg denne fremgangsmåten for å avbryte arbeidet.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Avbryt arbeid**.
1. Angi IDen for arbeidet du vil avbryte, i **Arbeids-ID**-feltet.
1. Velg **OK**.
1. Velg **Ja** for å bekrefte at du vil avbryte arbeidet.

For mer informasjon, se [Avbryte lagerarbeid for unntaksbehandling](../../warehousing/cancel-warehouse-work.md).
