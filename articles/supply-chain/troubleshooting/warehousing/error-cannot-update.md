---
title: Det oppstår en feil når lokasjonen velges under plukklisteregistrering
description: Det oppstår en feil når lokasjonen velges under plukklisteregistrering.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ef34b4fdcc572c56319f6cbf4913d822d8857595
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474970"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a>Det oppstår en feil når lokasjonen velges under plukklisteregistrering

KB-nummer: 4613106

## <a name="symptoms"></a>Symptomer

Dette problemet oppstår når systemet er konfigurert til å reservere salgsordrer automatisk. Hvis du prøver å velge lokasjonen for en plukklisteregistreringslinje, får du følgende feilmelding når du bruker lagerstyringsreservasjonsprosesser (WMS):

> Kan ikke oppdatere antall med nye dimensjoner

Dette problemet kan oppstå fordi du ikke har nok lagerbeholdning på en angitt lokasjon.

## <a name="resolution"></a>Oppløsning

Systemet fungerer som tiltenkt.

I scenarier der du bruker reserveringsprosessen på lagernivå, anbefaler vi at du bruker den manuelle reserveringsprosessen fra plukklinjen hvis du ikke bruker lagerbeholdningen på alle lagerdimensjonsnivåer. Du kan deretter bruke funksjonen *Reserver parti* til å fordele de nedre reserveringene, for eksempel lokasjon, for alle tilgjengelige lagerantall.
