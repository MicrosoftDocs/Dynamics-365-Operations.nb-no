---
title: Ikke nok arbeid funnet for klynge etter konfigurasjon av profil
description: Hvis du konfigurerer en klyngeprofil, kan du få en feilmelding som sier at det ikke er nok arbeid å finne. Rediger profilen og sett Aktiver stillinger til Nei.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 139fd72e571c8ef83af2fd0e497cf334b6ef0ea4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477166"
---
# <a name="not-enough-work-found-for-cluster-when-using-system-directed-cluster-picking"></a>Ikke nok arbeid som blir funnet for klynge ved bruk av klyngeplukking med system

## <a name="symptoms"></a>Symptomer

Når du bruker prosessen *Systemkontrollert gruppeplukking*, hvis du konfigurerer en gruppeprofil der for eksempel 10 stillinger kan plukkes, fungerer prosessen som planlagt når det er nok arbeid til å plukke til 10 stillinger. Hvis det imidlertid bare er åtte stillinger som skal plukkes, får du følgende feilmelding:

> Finner ikke nok arbeid for gruppen.

## <a name="resolution"></a>Løsning

Du kan løse dette problemet ved å redigere gruppeprofilen og sette **Aktiver stillinger**-alternativet til *Nei*.
