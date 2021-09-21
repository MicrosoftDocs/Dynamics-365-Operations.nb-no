---
title: Reserveringer kan ikke fjernes når en ordre annulleres
description: Du kan ikke annullere en salgsordre før arbeidet knyttet til ordren, er annullert og tilbakeført. Følg denne fremgangsmåten for å gjøre dette.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a8d947e64568246dba5eff3c21fd3920b6494b73
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477211"
---
# <a name="reservations-cannot-be-removed-when-canceling-an-order"></a>Reserveringer kan ikke fjernes når en ordre annulleres

## <a name="symptoms"></a>Symptomer

Hvis arbeid er knyttet til en salgsordre og du prøver å annullere ordren, får du følgende feilmelding:

> Kan ikke fjerne reservasjoner fordi det finnes opprettet arbeid som avhenger av reservasjonene.

Du kan ikke annullere salgsordren før arbeidet knyttet til ordren, er annullert og tilbakeført. Dette kravet gjelder selv om arbeidet som er knyttet til salgsordren, er lukket.

## <a name="resolution"></a>Løsning

Følg fremgangsmåten nedenfor for å løse problemet:

1. Avbryt arbeidet, og sett lageret tilbake på ønsket sted. Gå til den relevante belastningen for salgsordren, og velg enten **Reduser plukket kvantitet** på belastningslinjen eller **Reverser arbeid** i handlingsruten.

    Arbeidet har nå statusen *Avbrutt*, og nytt lagerflyttingsarbeid opprettes automatisk og behandles for å legge lager tilbake i lokasjonen som ble beskrevet da tilbakeføringen ble avbrutt.

2. Slett belastningen. Forsendelsen slettes også.

3. Du skal nå kunne gå til salgsordren og avbryte den.
