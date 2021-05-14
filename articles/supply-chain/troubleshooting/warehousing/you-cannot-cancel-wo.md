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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924407"
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
