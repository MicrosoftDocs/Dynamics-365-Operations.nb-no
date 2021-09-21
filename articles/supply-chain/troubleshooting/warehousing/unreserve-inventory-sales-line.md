---
title: Kan ikke reservere lager på en salgsordrelinje
description: Hvis det er åpent arbeid mot en salgslinje, og du prøver å fjerne lagerbeholdningen på linjen, får du en feilmelding. Fullfør eller slett arbeid for å frigjøre reservasjonen.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1a042065dc4cd637aff58e55cf16179b7022f6ca
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477209"
---
# <a name="cant-unreserve-inventory-on-a-sales-order-line"></a>Kan ikke reservere lager på en salgsordrelinje

## <a name="symptoms"></a>Symptomer

Hvis det er åpent arbeid mot en ordrelinje, og du prøver å fjerne lagerbeholdningen på linjen, får du følgende feilmelding:

> Kan ikke fjerne reservasjoner fordi det finnes opprettet arbeid som avhenger av reservasjonene.

## <a name="resolution"></a>Løsning

Undersøk om det finnes åpent emballasjegruppearbeid for å hente varen fra en pakkestasjon til en annen lokasjon (f.eks. *Rampedør*). Se gjennom postene på sidene **Logg over oppretting av arbeid** og **Arbeidsdetaljer** for å fastslå hva som fysisk reserverer lageret, og fullfør eller slett arbeidet for å frigjøre reservasjonen.
