---
title: Glidende gjennomsnitt, sekvens for kostnad for tilbakefall
description: Denne artikkelen inneholder informasjon om sekvenser for kostnad for tilbakefall for glidende gjennomsnitt av beregninger i Microsoft Dynamics 365 Supply Chain Management.
author: JennySong-SH
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: ad67828e2608f4754a3dffd76c64292f6a91e95f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868021"
---
# <a name="moving-average-fallback-cost-sequence"></a>Glidende gjennomsnitt, sekvens for kostnad for tilbakefall

[!include [banner](../includes/banner.md)]

En måte du kan beregne lagerkostnadene på, er ved hjelp av et _glidende gjennomsnitt_. Opptil tre kostnadsverdier kan knyttes til hver lagervare:

- **Siste avgang** – Den siste avgangskostnaden som ble tilordnet før beholdningen ble negativ
- **Aktiv kostnad** – Den siste kostnaden som ble aktivert i en etterkalkuleringsversjon
- **Varepris** – Kostnaden som er angitt for det frigitte produktet

For å bestemme hvilke av disse kostverdiene som skal brukes ved beregning av glidende gjennomsnitt, bruker systemet en _sekvens for kostnad for tilbakefall_ for å etablere preferanserekkefølgen for verdiene. Hvis den foretrukne kostnadsverdien ikke er tilgjengelig, bruker systemet den neste foretrukne verdien, og så videre.

I tidligere versjoner av Microsoft Dynamics 365 Supply Chain Management brukte systemet en fast sekvens for kostnad for tilbakefall (_siste avgang – aktiv kostnad – varepris_). I versjon 10.0.11 er denne sekvensen fremdeles standardsekvensen. Du kan imidlertid også aktivere en funksjon som lar deg velge mellom tre tilgjengelige sekvenser for kostnad for tilbakefall. Denne funksjonen kan være spesielt nyttig for organisasjoner som regelmessig bruker negative beholdningsverdier.

Hvis du vil gjøre velgeren for tilbakefallskostnadene tilgjengelig, må du (eller en administrator) bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktivere funksjonen med navnet _Glidende gjennomsnitt, sekvens for kostnad for tilbakefall_.

Følg denne fremgangsmåten for å velge sekvensen for kostnad for tilbakefall for beregning av glidende gjennomsnitt.

1. Åpne **Parametere**-siden.
2. I fanen **Lagerregnskap**, i delen **Glidende gjennomsnitt**, setter du feltet **Sekvens for kostnad for tilbakefall** til en av følgende verdier:

    - **Siste avgang – Aktiv kostnad – varepris** – Denne sekvensen er standardsekvensen. Det er samme sekvens som brukes hvis funksjonen _Glidende gjennomsnitt, sekvens for kostnad for tilbakefall_ ikke er aktivert.
    - **Aktiv kostnad – Siste avgang**
    - **Aktiv kostnad – Varepris** – Organisasjoner kan oppleve ytelsesproblemer hvis de bruker forretningsprosesser der lageret regelmessig blir negativ, og samtidig har et høyt transaksjonsvolum. Denne innstillingen kan bidra til å redusere disse ytelsesproblemene.

![Parametere for lagerregnskap.](media/inventory-accounting-parameters.png "Parametere for lagerregnskap")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]