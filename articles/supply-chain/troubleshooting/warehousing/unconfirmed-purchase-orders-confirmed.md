---
title: Oppdatering av produktmottaksoppgave bekrefter ikke-bekreftede ordrer
description: Når du har kjørt Oppdater produktmottak, bekrefter systemet ubekreftede ordrer som har statusen Registrert. Få mer informasjon om funksjonen som løser dette problemet.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 171a978efc6b55b92f429381e72036cb1b3296c6
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477165"
---
# <a name="unconfirmed-purchase-orders-are-confirmed-after-running-update-product-receipts"></a>Ubekreftede bestillinger bekreftes etter at du har kjørt Oppdater produkttilganger

## <a name="symptoms"></a>Symptomer

Når du har kjørt den periodiske oppgaven *Oppdater produktkvitteringer*, bekrefter systemet automatisk ubekreftede bestillinger som har lagertransaksjonsstatusen *Registrert*.

## <a name="resolution"></a>Løsning

En ny inngående lastbehandlingsfunksjon, *Overmottak for lastantall*, løser dette problemet. Hvis du aktiverer denne funksjonen, går du til arbeidsområdet [Funksjonsbehandling](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) og aktiverer følgende funksjoner i rekkefølgen de er oppført:

1. Knytt bestillingsbeholdningstransaksjoner til belastning
2. Overmottak for belastningsantall

Hvis du vil ha mer informasjon, kan du se [Poster registrerte produktantall mot bestillinger](/dynamics365/supply-chain/warehousing/inbound-load-handling).
