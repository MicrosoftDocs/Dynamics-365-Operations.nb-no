---
title: Plukkarbeid blokkert på grunn av uferdig etterfyllingsarbeid
description: Plukkarbeid kan bli blokkert på grunn av avhengig etterfyllingsarbeid. Fullfør etterfyllingsarbeidet, og behandle deretter plukkarbeidet.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 53b50d1e3e2d7bb64e78514affe80076ddcb9052
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477246"
---
# <a name="picking-work-cant-be-unblocked-because-of-unfinished-replenishment-work"></a>Blokkering av plukkarbeid kan ikke oppheves på grunn av uferdig etterfyllingsarbeid

## <a name="symptoms"></a>Symptomer

Ved bruk av etterfylling av bølgebehov kan plukkingsarbeid blokkeres på grunn av avhengig etterfyllingsarbeid. Hvis en plukklokasjon må etterfylles for å opofylle kildeordrebehovet, vil systemet opprette både etter fyllingsarbeidet og plukkarbeidet. Den blokkerer imidlertid plukkingsarbeidet til etterfyllingsarbeidet er fullført og du får følgende feilmelding:

> Kan ikke oppheve blokkeringen av arbeidet %1 fordi det har etterfyllingsarbeid som ikke er fullført.

## <a name="resolution"></a>Løsning

Denne virkemåten er med hensikt, fordi plukklokasjonen ikke har nok lager hvis ikke etterfyllingsarbeidet er fullført. Fullfør etterfyllingsarbeidet, og behandle deretter plukkarbeidet.
