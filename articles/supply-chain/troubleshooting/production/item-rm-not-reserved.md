---
title: Vare-RM kan ikke reserveres når en produksjonsordre frigis
description: Når du frigir en produksjonsordre, kan du få feilmeldingen "Vare-RM kan ikke reserveres fullstendig." Kontroller at hele antallet er tilgjengelig, eller reserver varer manuelt.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 528895252d661bb012f49190c15853989833064d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477227"
---
# <a name="item-rm-cant-be-fully-reserved-when-a-production-order-is-released"></a>Vare-RM kan ikke reserveres fullt ut når en produksjonsordre frigis

## <a name="symptoms"></a>Symptomer

Hvis ikke alle stykklistelinjevarer er fysisk tilgjengelige når en produksjonsordre frigis til et lager, og **Frigi til lager**-policy er satt til *Krever full reservasjon*, vil du få følgende feilmelding:

> Varen RM kan ikke reserveres fullt ut. Kontroller at hele antallet er tilgjengelig, eller reserver varene manuelt hvis Reservasjon-feltet på stykklistelinjen er angitt til Manuell eller Startet. Kan ikke frigi ordren til lager fordi noen materialer ikke kan reserveres.

## <a name="resolution"></a>Løsning

Denne virkemåten er standard og fungerer som forventet. Rett dette problemet ved å følge retningslinjene som gis i feilmeldingen: "Kontroller at hele antallet er tilgjengelig, eller reserver varene manuelt hvis Reservasjon-feltet på stykklistelinjen er angitt til Manuell eller Startet.
