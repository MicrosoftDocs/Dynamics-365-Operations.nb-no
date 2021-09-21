---
title: Ledetekst for automatisk reservering vises med tilgjengelig lager
description: Når du bruker en vare i et lager der lagerprosessene ikke er aktivert, vises ledeteksten for automatisk reservering. Angi alle dimensjonene over lokasjonen.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a15502ce8c5bc61d37cedd746985176408a2f362
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477237"
---
# <a name="auto-reservation-prompt-for-batch-number-is-shown-even-with-available-inventory"></a>Ledetekst for automatisk reservering for partinummer vises også med tilgjengelig lager

## <a name="symptoms"></a>Symptomer

Når du bruker en vare som har et *parti-over*-reservasjonshierarki i et lager som ikke har aktivert lagerprosesser, og automatisk reservering er aktivert, vises ledeteksten for automatisk reservering for et partinummer, selv om bare ett parti er tilgjengelig for plukking.

Når du imidlertid bruker den samme varen i et lager der lagerprosessene er aktivert, vises ikke ledeteksten for automatisk reservering.

## <a name="resolution"></a>Løsning

Hvis et reserveringshierarki er definert som *parti-over* eller *serie-over*, må den refererte dimensjonen (**Partinummer** eller **Serienummer**) alltid være angitt i behovsordrer. Lagerprosesser kan kanskje fylle ut informasjonen hvis ett enkelt parti- eller serienummer er tilgjengelig. Siden lageret ikke er aktivert for lagerprosesser, må imidlertid brukeren alltid angi alle dimensjonene over **Lokasjon**.
