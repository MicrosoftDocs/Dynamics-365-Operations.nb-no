---
title: Definere skattemyndigheter
description: Skattemyndighetene er enheter som innsamlet merverdiavgift skal rapporteres og betales til.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 63b1b023181e1ead16571102c524a61edfdabdca
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446320"
---
# <a name="set-up-sales-tax-authorities"></a>Definere skattemyndigheter

[!include [banner](../../includes/banner.md)]

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

