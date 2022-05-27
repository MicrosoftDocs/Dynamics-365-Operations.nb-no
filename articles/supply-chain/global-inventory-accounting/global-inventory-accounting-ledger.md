---
title: Global lagerregnskap-finansmodul
description: Dette emnet beskriver finansmoduler for Globale lagerregnskap, som er definert av en kombinasjon av en valuta, en kalender, en konvensjon og en tilknytning til en juridisk enhet.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f5f610fa51fce18ecefbf96892b56b05208c666c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676082"
---
# <a name="global-inventory-accounting-ledger"></a>Global lagerregnskap-finansmodul

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Globalt lagerregnskap har et eget sett med finansmoduler. Hver gang en lagerrelatert transaksjon behandles for en relevant juridisk enhet, kan systemet ta hensyn til transaksjonen i et hvilket som helst antall Globalt lagerregnskap-finansmoduler, etter behov.

En finansmodul er et register av debet- og kreditoppføringer. Disse oppføringene klassifiseres ved hjelp av kostnadselementer og underregnskapskontoer. En finansmodul for Globalt lagerregnskap er definert av en kombinasjon av en valuta, en kalender, en konvensjon og en tilknytning til en juridisk enhet.

Hvis du vil konfigurere finansmoduler for Globalt lagerregnskap, kan du gå til **Globalt lagerregnskap \> Oppsett \> Globalt lagerregnskap-finanskontoer**. For hver finansmodul angir du feltene nedenfor:

- **Navn** – Angi navnet på finansmodulen.
- **Beskrivelse** – Angi en beskrivelse av finansmodulen.
- **Regnskapskalender** – Angi regnskapskalenderen for finansmodulen.
- **Valuta og valutakurstype** – Bruk feltene i denne hurtigfanen til å velge regnskapsvalutaen som finansmodulen bruker, og valutakurstypen. Valutaen du velger, kan være forskjellig fra valutaen som den juridiske enheten bruker. I Globalt lagerregnskap kan brukere definere så mange finansmoduler for kostnader som de trenger. Globalt lagerregnskap støtter lagerregnskap i flere valutaer og i flere vurderinger. Angi følgende felt:

    - **Valuta** – Velg kostnadsvalutaen som lagerrelaterte verdier vedlikeholdes i. Disse verdiene omfatter lagerverdi, solgte varers kost, lager i transitt og alle typer avvik.
    - **Valutakurstype** – Velg valutakursen som systemet skal bruke til å konvertere transaksjonsbeløpet i transaksjonsvalutaen og standardkostnaden for varene til kostnadsvalutaen.

- **Konvensjonsnavn** – Angi en konvensjon. En konvensjon er en samling policyer som fastsetter hvordan kostnader blir regnskapsføres i denne finansmodulen.
- **Juridisk enhet** – Finansmodulen vil ta hensyn til dokumentene som er postert til den valgte juridiske enheten.
- **Optimering** – Velg om lagertransaksjoner som ble opprettet før finansmodulen ble opprettet, skal behandles i henhold til valutaen og konvensjonen i finansmodulen. Velg én av følgende verdier:

    - **Aktivert** – Finansmodulen skal behandle transaksjoner som ble opprettet før finansmodulen ble opprettet.
    - **Deaktivert** – Finansmodulen skal bare behandle transaksjoner som ble opprettet etter finansmodulen ble opprettet.

    > [!IMPORTANT]
    > Du kan **ikke** gå tilbake og angi dette feltet etter at du har lagt inn nye dokumenter.

- **Status** – Systemet setter automatisk statusen for nyopprettede finanmodulen til *Klargjør*.
