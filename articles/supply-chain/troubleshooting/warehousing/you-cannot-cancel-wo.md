---
title: Du kan ikke avbryte arbeid som er på en bruker
description: Du kan ikke avbryte arbeid som er på en bruker
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
ms.openlocfilehash: 1d7b0140d0c2724234a549ca4dfb23109012654abe0e60fcea1f98e8f17c153a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748697"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a>Du kan ikke avbryte arbeid som er på en bruker

Feilkode: WAX708

## <a name="symptoms"></a>Symptomer

Systemet viser følgende feilmelding:

> Du kan ikke avbryte arbeid som er på en bruker.

## <a name="cause"></a>Årsak

Arbeidet er låst av en bruker og kan ikke avbrytes. Hvis du vil bekrefte dette, åpner du arbeids-IDen og åpner deretter kategorien **Generelt**. Hvis arbeidet er låst, settes **Arbeidsstatus**-feltet til *Pågår*, og feltet **Sperret av** blir satt til en bruker-ID.

## <a name="resolution"></a>Oppløsning

Følg denne fremgangsmåten for å avbryte arbeidet.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Avbryt arbeid**.
1. Angi IDen for arbeidet du vil avbryte, i **Arbeids-ID**-feltet.
1. Velg **OK**.
1. Velg **Ja** for å bekrefte at du vil avbryte arbeidet.

For mer informasjon, se [Avbryte lagerarbeid for unntaksbehandling](../../warehousing/cancel-warehouse-work.md).
