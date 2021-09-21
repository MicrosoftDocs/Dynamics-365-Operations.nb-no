---
title: Ordrestatus gjenstår. Delvis frigitt etter at den er fakturert
description: I noen tilfeller forblir statusen til en salgsordre forblir Delvis frigitt, selv etter at ordren er fakturert. Denne siden forklarer hvorfor og gir en mulig løsning.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8bfe7ecfd4beb6e77e8dd1e23ccd896d067bdb51
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477210"
---
# <a name="order-status-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Ordrestatus gjenstår. Delvis frigitt selv etter at salgsordren er fakturert

## <a name="symptoms"></a>Symptomer

En salgsordre er en leveringsordre, men én eller flere varer i den har en annen leveringsmåte. Når ordren er fakturert, har den fremdeles frigivelsesstatusen *Delvis frigitt*.

En salgsordre har for eksempel to varer: en for levering og en for plukking. Både leveringen og plukkingen er utført. Derfor er begge linjene fakturert. Frigivelsesstatusen vises imidlertid fremdeles som *Delvis frigitt*, som er villedende.

## <a name="workaround"></a>Løsning

Frigivelsesstatusen gjelder bare for ordrelinjer der varene er aktivert for lagerstyring. Derfor forblir frigivelsesstatusen *Delvis frigitt* i dette scenarioet. Microsoft har evaluert dette problemet og har funnet ut at det er en funksjonsbegrensning. En utvidelse kan legges til som en del av følgeseddelen og faktureringsprosessen for å oppdatere frigivelsesstatusen.
