---
title: Konfigurere og behandle en utveksling i en returordre
description: Dette emnet forklarer hvordan du konfigurerer en utveksling ved en retur i Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 3331b984693c58c6ee8c49b98ed7d3a8df5b79ff
ms.openlocfilehash: 45b628376a483d3d639e5c018dd93570ed8ce7af
ms.contentlocale: nb-no
ms.lasthandoff: 12/04/2018

---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>Konfigurere og behandle en utveksling i en returordre

[!include [banner](includes/banner.md)]

I tidligere versjoner av Microsoft Dynamics 365 for Retail ble returer mot kundeordrer behandlet ved hjelp av returordredokumentet i Retail-hovedkvarteret. Returordredokumentet kan imidlertid brukes til å behandle bare produkter som returneres. De returnerte produktene angis med et negativt antall på returordrelinjene. Derimot angis salg med et positivt antall. Returordredokumentet støtter imidlertid ikke positive antall. På grunn av denne begrensningen støttet ikke tidligere versjoner av Retail scenarier der produktutvekslinger ble utført ved hjelp av returordredokumentet.

Funksjonaliteten er imidlertid lagt til for å støtte scenarier der utvekslinger blir utført på returordrer. Retail bruker nå salgsordredokumentet i stedet for returordredokumentet til å behandle disse transaksjonstypene.

## <a name="configure-retail-to-support-exchanges-on-return-orders"></a>Konfigurere Retail til å støtte utvekslinger på returordrer

Følg denne fremgangsmåten for å konfigurere systemet til å støtte utvekslinger på returordrer.

1. Gå til **Retail \> Hovedkvarteroppsett \> Parametere \> Detaljhandelsparametere**. Sett alternativet **Behandle returordrer som salgsordrer** til **Ja** i hurtigkategorien **Kundeordrer**.
2. Kjør jobben **Distribusjonsplan for global konfigurasjon** (**1110**).

## <a name="make-an-exchange"></a>Gjøre en utveksling

Etter at systemet er konfigurert som beskrevet i den forrige delen, vil salgsstedsbrukeren fortsatt velge en salgsordre eller salgsfaktura for å behandle en retur, som i tidligere versjoner av Retail. Men etter at returvarene er lagt til handlekurven, kan brukeren legge til nye salgslinjer i handlekurven.

For disse nye salgslinjene må brukeren definere alle attributtene som kreves for å behandle en kundeordrelinje. Disse attributtene inkluderer leveringsmåten og oppfyllelseslokasjonen. Betalingen som forfaller for transaksjonen, blir en nettosum av returordrelinjene og salgsordrelinjene. Når betalingen er betalt for transaksjonen, blir returordren postert som et salgsordredokument i Retail-hovedkvarteret, og systemet vil fakturere de returnerte linjene umiddelbart.

For å gi deg bedre oversikt over de ulike beløpene for handlekurven, er tre nye beløpsfelt lagt til i handlekurven. Du kan bruke skjermutformingen slik at disse nye feltene blir tilgjengelige i brukergrensesnittet for salgsstedet.

- **Brukt innbetaling** – Innbetalingsbeløpet som brukes for en transaksjon når brukeren utfører en kundeordrehenting. Hvis det ikke finnes overstyring av innbetaling, og en innbetaling på 10 prosent er konfigurert, vil beløpet i dette feltet være 90 prosent av totalbeløpet for kundeordren.
- **Utfør beløp** – Det totale beløpet for linjer der leveringsmåten ble satt til **Utfør** når kundeordren ble opprettet eller redigert, eller under en kundeordreutveksling. Beløpet i dette feltet inneholder avgifter og tillegg.
- **Returbeløp** – Det totale beløpet for linjer som har negative antall under kundeordreutvekslingen. Beløpet i dette feltet inneholder avgifter og tillegg.

