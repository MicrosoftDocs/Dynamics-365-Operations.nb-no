---
title: Konsernintern hovedplanlegging
description: Dette emnet forklarer konsernintern hovedplanlegging
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: e28051097905503e291e0c15a50e9363b39b2daa
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548447"
---
# <a name="intercompany-master-scheduling"></a>Konsernintern hovedplanlegging

[!include [banner](../../includes/banner.md)]

Konsernintern hovedplanlegging er måten du kan beregne behov på, og generere planlagte konserninterne bestillinger på tvers av flere interne firmaer. Konsernintern hovedplanlegging utføres for det antall gjentakelser du angir. Hvis du skal få Microsoft Dynamics 365 Supply Chain Management til å utføre konsernintern hovedplanlegging, må du definere hovedplanlegging i hver av de konserninterne firmaene. Dette medfører en rekke gjentakelser der Microsoft Dynamics 365 Supply Chain Management automatisk oppretter en konsernintern bestilling, og dette fører til automatisk oppretting av en konsernintern salgsordre, som igjen fører til nye behov.

Du oppretter den konserninterne hovedplanen og den konserninterne planleggingsordren i **Hovedplanlegging**-parameterne i hver av de konserninterne firmaene.

For å kunne oveføre behovet i hele den konserninterne kjeden, må du definere parametere for å sikre at planlagte bestillinger autoriseres automatisk. Det vil si at ordrer ikke kan endres med hensyn til tid eller antall. Definer **autorisasjonshorisonten** på dekningsgruppen eller **autorisasjonshorisonten** i hovedplanen. Hvis ingen **autorisasjonshorisont** er definert, opprettes det ingen konserninterne bestillinger automatisk. Bare første utføring av hovedplanleggingen fører til planlagte bestillinger. Siden det ikke opprettes noen konsernintern bestilling, opprettes det imidlertid ingen konsernintern salgsordre, og det opprettes derfor ingen flere konserninterne bestillinger, og så videre.

Når du starter den konserninterne hovedplanleggingen, utfører Microsoft Dynamics 365 Supply Chain Management én hovedplanlegging i hvert konserninterne firma. Deretter utføres en ny hovedplanlegging i hvert konserninterne firma, og så videre, til det angitte antall iterasjoner er nådd. Maksimalt 30 iterasjoner er mulig. Jo flere iterasjoner du velger, jo lenger tid tar planleggingen.

Fordi hovedplanleggingen i firmaene styres av den konserninterne planleggingssekvensen, som er rekkefølgen programmet prioriterer hovedplanleggingen mellom hvert konserninterne firma, kan du starte den konserninterne hovedplanleggingen fra et hvilket som helst konserninternt firma. Siden den konserninterne planleggingssekvensen bestemmer rekkefølgen hovedplanleggingen utføres i firmaene, er det ikke så viktig hvor den konserninterne hovedplanleggingen starter. I hver gjentakelse utføres gjeldende firma sist.

> [!NOTE]
> Den anbefalte fremgangsmåten er å tillate at konsernintern hovedplanlegging startes fra ett Microsoft Dynamics 365 Supply Chain Management-firma.

På siden **Konsernintern hovedplanlegging** kan du starte en sekvens for hovedplanlegging, som utfører hovedplanlegging første gang med prinsippet for oppdatering av behovsberegning som du har valgt for den første gjentakelsen, for alle konserninterne firmaer. De etterfølgende gjentakelsene bruker det sekundære prinsippet du velger for den neste gjentakelsen, og dette prinsippet brukes til antall gjentakelser som er angitt, er nådd.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
