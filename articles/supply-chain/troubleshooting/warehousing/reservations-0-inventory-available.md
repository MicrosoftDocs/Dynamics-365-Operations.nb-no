---
title: Kan ikke gjøre lagerreservasjoner fordi 0,00 er tilgjengelig
description: Du får en feilmelding om at systemet ikke kan reservere fordi bare 0,00 er tilgjengelig på lageret. Dette problemet skyldes sannsynligvis åpent arbeid.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 75d72f7ee1bdecca5a087b75b1de9907b9d244ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477231"
---
# <a name="system-cant-make-reservations-because-000-are-available-in-the-inventory"></a>Systemet kan ikke reservere fordi 0,00 er tilgjengelig på lageret

## <a name="symptoms"></a>Symptomer

Dette problemet kan oppstå hvis systemet ikke kan oppdatere et lagerantall, fordi det ikke finnes nok lagertransaksjoner som har de angitte dimensjonene. Du får følgende feilmelding:

> Fysisk lagerbeholdning område = %1, lager = %2, lagerstatus = tilgjengelig, partinummer = %3, eier = %4: %5 kan ikke reserveres fordi bare 0,00 er tilgjengelig på lageret.

## <a name="resolution"></a>Løsning

Dette problemet skyldes sannsynligvis åpent arbeid. Du må enten fullføre arbeidet eller motta uten arbeidsoppretting. Kontroller at ingen lagertransaksjoner fysisk reserverer antallet. Disse transaksjonene kan for eksempel være åpne kvalitetsordrer, lagerblokkeringsposter eller ordrer.
