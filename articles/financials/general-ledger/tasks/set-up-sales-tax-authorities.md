--- 
title: Definere skattemyndigheter
description: Skattemyndighetene er enheter som innsamlet merverdiavgift skal rapporteres og betales til.
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: e0d8b87e23932ce843791778f65eb77240cc28f4
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-sales-tax-authorities"></a>Definere skattemyndigheter

[!include[task guide banner](../../includes/task-guide-banner.md)]

Skattemyndighetene er enheter som innsamlet merverdiavgift skal rapporteres og betales til. Du kan betale merverdiavgift til myndigheten direkte eller via en leverandørkonto som du oppretter for skattemyndigheten. Hvis du gjør dette, kan firmaet bruke sine vanlige betalingsrutiner til å betale skattemyndigheten til rett tid. Hvis du ikke angir skattemyndigheten som en leverandør, må noen klargjøre en manuell betaling til skattemyndigheten på riktig forfallsdato. Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. Gå til Avgift > Indirekte avgifter > Merverdiavgift > Skattemyndigheter.
2. Klikk Ny.
3. Skriv inn en verdi i Skattemyndighet-feltet.
4. Skriv inn en verdi i Navn-feltet.
5. Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
7. Klikk koblingen i den valgte raden i listen.
8. Velg rapportoppsettet for ditt land/din region hvis det er aktuelt. Hvis rapportoppsettene ikke samsvarer med kravene til skattemyndighetene, kan du bruke standardoppsett.
9. Angi verdier i avrundingsformen og avrundingsfeltene for å angi hvordan det totale avgiftsbeløpet som skal betales, skal avrundes. Alle avrundingsdifferanser skal posteres til Kontoer for automatiske transaksjoner angitt i Økonomimodul.
10. Angi et tall i Avrund-feltet.
11. Klikk Lagre.

