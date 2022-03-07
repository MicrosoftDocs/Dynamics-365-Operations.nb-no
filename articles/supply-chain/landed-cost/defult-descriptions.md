---
title: Standardbeskrivelser for økonomimodulen
description: Standardbeskrivelser kan brukes til å oppdatere feltet Beskrivelse i bilagsposteringer til økonomimodulen.
author: sherry-zheng
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 47c5c9e71dba7a0cb7c798c167208faebeb5af6c
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500386"
---
# <a name="default-descriptions-for-the-general-ledger"></a>Standardbeskrivelser for økonomimodulen

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Standardbeskrivelser kan brukes til å oppdatere feltet **Beskrivelse** i bilagsposteringer til økonomimodulen. Denne funksjonaliteten er utvidet for å arbeide med Netto innkjøpspris.

Hvis du vil definere standardbeskrivelser for finansposteringer, kan du gå til **Organisasjonsstyring \> Oppsett \> Standardbeskrivelser**.

Følgende tabell viser de nye verdiene som er lagt til for feltet **Beskrivelse** på siden **Standardbeskrivelser** for å støtte Netto innkjøpspris.

| Beskrivelsestype | Notater |
|---|---|
| Importer etterkalkulering – Kostnadsforløp | Når en bestillingsfaktura posteres, behandles en kostnadsavsetning for estimerte sjøreisekostnader. Standardbeskrivelser kan angis for å legge til sjøreisenummeret i beskrivelsen. Bruk *%4* for forsendelsesnummeret. |
| Importer etterkalkulering – Varer i transittordre | Hvis du bruker behandling i transitt, posteres bestillingsfakturaen, og varene posteres til en vare i transittkonto. Standardbeskrivelser kan angis for å legge til ordrenummeret i transitt i beskrivelsen. Bruk *%4* for ordrenummeret i transitt. |
| Beholdning – lukking – justering | Når AP-fakturaen behandles for en sjøreisekostnad, behandles en lagerjustering for å estimere sjøreisekostnader. Standardbeskrivelser kan angis for å legge til sjøreisenummeret i beskrivelsen. Bruk *%4* for forsendelsesnummeret. |

Hvis du vil ha mer informasjon om hvordan du arbeider med siden **Standardbeskrivelser**, kan du se [Definere standardbeskrivelser for automatisk postering](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).
