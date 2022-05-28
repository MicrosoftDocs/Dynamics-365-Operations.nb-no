---
title: Standardbeskrivelser for økonomimodulen
description: Standardbeskrivelser kan brukes til å oppdatere feltet Beskrivelse i bilagsposteringer til økonomimodulen.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f95dff3a77a552d5788d813b3d13dc30579be715
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695714"
---
# <a name="default-descriptions-for-the-general-ledger"></a>Standardbeskrivelser for økonomimodulen

[!include [banner](../../includes/banner.md)]

Standardbeskrivelser kan brukes til å oppdatere feltet **Beskrivelse** i bilagsposteringer til økonomimodulen. Denne funksjonaliteten er utvidet for å arbeide med Netto innkjøpspris.

Hvis du vil definere standardbeskrivelser for finansposteringer, kan du gå til **Organisasjonsstyring \> Oppsett \> Standardbeskrivelser**.

Følgende tabell viser de nye verdiene som er lagt til for feltet **Beskrivelse** på siden **Standardbeskrivelser** for å støtte Netto innkjøpspris.

| Beskrivelsestype | Notater |
|---|---|
| Importer etterkalkulering – Kostnadsforløp | Når en bestillingsfaktura posteres, behandles en kostnadsavsetning for estimerte sjøreisekostnader. Standardbeskrivelser kan angis for å legge til sjøreisenummeret i beskrivelsen. Bruk *%4* for forsendelsesnummeret. |
| Importer etterkalkulering – Varer i transittordre | Hvis du bruker behandling i transitt, posteres bestillingsfakturaen, og varene posteres til en vare i transittkonto. Standardbeskrivelser kan angis for å legge til ordrenummeret i transitt i beskrivelsen. Bruk *%4* for ordrenummeret i transitt. |
| Beholdning – lukking – justering | Når AP-fakturaen behandles for en sjøreisekostnad, behandles en lagerjustering for å estimere sjøreisekostnader. Standardbeskrivelser kan angis for å legge til sjøreisenummeret i beskrivelsen. Bruk *%4* for forsendelsesnummeret. |

Hvis du vil ha mer informasjon om hvordan du arbeider med siden **Standardbeskrivelser**, kan du se [Definere standardbeskrivelser for automatisk postering](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).
