---
title: Arbeid kan ikke avbrytes på grunn av statusen
description: Arbeid kan ikke avbrytes på grunn av statusen
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
ms.openlocfilehash: f983501b490c5516525b4d5904603ed62e8799f9e6124e5672b36a12804ecb0a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755984"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a>Arbeid kan ikke avbrytes på grunn av statusen

Feilkode: WAX2190

## <a name="symptoms"></a>Symptomer

Systemet viser følgende feilmelding:

> Du kan ikke avbryte arbeidet %1 fordi det har statusen %2.

## <a name="cause"></a>Årsak

Arbeidet kan ikke avbrytes med gjeldende status.

Arbeidshodet eller arbeidslinjene har ikke den forventede **Arbeidsstatus**-verdien. Feltet **Arbeidsstatus** på arbeidshodehodet er ikke satt til *Åpen* eller *Pågår*.

## <a name="resolution"></a>Oppløsning

Følg denne fremgangsmåten for å avbryte arbeidet.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Avbryt arbeid**.
1. Angi IDen for arbeidet du vil avbryte, i **Arbeids-ID**-feltet.
1. Velg **OK**.
1. Velg **Ja** for å bekrefte at du vil avbryte arbeidet.

For mer informasjon, se [Avbryte lagerarbeid for unntaksbehandling](../../warehousing/cancel-warehouse-work.md).
