---
title: Glidende gjennomsnitt, sekvens for kostnad for tilbakefall
description: Dette emnet inneholder informasjon om sekvenser for kostnad for tilbakefall for glidende gjennomsnitt av beregninger i Microsoft Dynamics 365 Supply Chain Management.
author: AndersGirke
manager: tfehr
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 0538701588b9c71dff4c538711606913a359de6a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434595"
---
# <a name="moving-average-fallback-cost-sequence"></a>Glidende gjennomsnitt, sekvens for kostnad for tilbakefall

En måte du kan beregne lagerkostnadene på, er ved hjelp av et _glidende gjennomsnitt_. Opptil tre kostnadsverdier kan knyttes til hver lagervare:

- **Siste avgang** – Den siste avgangskostnaden som ble tilordnet før beholdningen ble negativ
- **Aktiv kostnad** – Den siste kostnaden som ble aktivert i en etterkalkuleringsversjon
- **Varepris** – Kostnaden som er angitt for det frigitte produktet

For å bestemme hvilke av disse kostverdiene som skal brukes ved beregning av glidende gjennomsnitt, bruker systemet en _sekvens for kostnad for tilbakefall_ for å etablere preferanserekkefølgen for verdiene. Hvis den foretrukne kostnadsverdien ikke er tilgjengelig, bruker systemet den neste foretrukne verdien, og så videre.

I tidligere versjoner av Microsoft Dynamics 365 Supply Chain Management brukte systemet en fast sekvens for kostnad for tilbakefall (_siste avgang – aktiv kostnad – varepris_). I versjon 10.0.11 er denne sekvensen fremdeles standardsekvensen. Du kan imidlertid også aktivere en funksjon som lar deg velge mellom tre tilgjengelige sekvenser for kostnad for tilbakefall. Denne funksjonen kan være spesielt nyttig for organisasjoner som regelmessig bruker negative beholdningsverdier.

Hvis du vil gjøre velgeren for tilbakefallskostnadene tilgjengelig, må du (eller en administrator) bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktivere funksjonen med navnet _Glidende gjennomsnitt, sekvens for kostnad for tilbakefall_.

Følg denne fremgangsmåten for å velge sekvensen for kostnad for tilbakefall for beregning av glidende gjennomsnitt.

1. Åpne **Parametere**-siden.
2. I kategorien **Lagerregnskap**, i delen **Glidende gjennomsnitt**, setter du feltet **Sekvens for kostnad for tilbakefall** til en av følgende verdier:

    - **Siste avgang – Aktiv kostnad – varepris** – Denne sekvensen er standardsekvensen. Det er samme sekvens som brukes hvis funksjonen _Glidende gjennomsnitt, sekvens for kostnad for tilbakefall_ ikke er aktivert.
    - **Aktiv kostnad – Siste avgang**
    - **Aktiv kostnad – Varepris** – Organisasjoner kan oppleve ytelsesproblemer hvis de bruker forretningsprosesser der lageret regelmessig blir negativ, og samtidig har et høyt transaksjonsvolum. Denne innstillingen kan bidra til å redusere disse ytelsesproblemene.

![Parametere for lagerregnskap](media/inventory-accounting-parameters.png "Parametere for lagerregnskap")
