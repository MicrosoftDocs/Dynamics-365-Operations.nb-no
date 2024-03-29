---
title: Konfigurer og behandle en utveksling i en returordre
description: Denne artikkelen forklarer hvordan du konfigurerer en utveksling ved en retur i Dynamics 365 Commerce.
author: josaw1
ms.date: 07/28/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: f33c674e4110b4e45ac58e499a65da2509b00046
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845799"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>Konfigurer og behandle en utveksling i en returordre

[!include [banner](includes/banner.md)]

I tidligere versjoner av Dynamics 365 Commerce ble returer mot kundeordrer behandlet ved hjelp av returordredokumentet i Headquarters. Returordredokumentet kan imidlertid brukes til å behandle bare produkter som returneres. De returnerte produktene angis med et negativt antall på returordrelinjene. Derimot angis salg med et positivt antall. Returordredokumentet støtter imidlertid ikke positive antall. På grunn av denne begrensningen støttet ikke tidligere versjoner av appen scenarier der produktutvekslinger ble utført ved hjelp av returordredokumentet.

Funksjonaliteten er imidlertid lagt til for å støtte scenarier der utvekslinger blir utført på returordrer. Commerce bruker nå salgsordredokumentet i stedet for returordredokumentet til å behandle disse transaksjonstypene.

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a>Konfigurer Commerce til å støtte utvekslinger på returordrer

> [!NOTE]
> I Commerce, versjon 10.0.20 og nyere er en ny funksjon kalt Enhetlig returbehandling i salgssted tilgjengelig. Hvis du aktiverer denne funksjonen, er ikke konfigurasjonstrinnene nedenfor nødvendige. **Behandle returer som salgsordrer** blir en permanent konfigurert innstilling, og du kan ikke endre den.

Følg denne fremgangsmåten for å konfigurere systemet til å støtte utvekslinger på returordrer (hvis du ikke har aktivert funksjonen **Enhetlig returbehandling i salgssted**.

1. Gå til **Retail og Commerce \> Hovedkvarteroppsett \> Parametere \> Commerce-parametere**. Sett alternativet **Behandle returordrer som salgsordrer** til **Ja** i hurtigfanen **Kundeordrer**.
2. Kjør jobben **Distribusjonsplan for global konfigurasjon** (**1110**).

## <a name="make-an-exchange"></a>Gjøre en utveksling

Etter at systemet er konfigurert som beskrevet i den forrige delen, vil salgsstedsbrukeren fortsatt velge en salgsordre eller salgsfaktura for å behandle en retur, som i tidligere versjoner av appen. Men etter at returvarene er lagt til handlekurven, kan brukeren legge til nye salgslinjer i handlekurven.

For disse nye salgslinjene må brukeren definere alle attributtene som kreves for å behandle en kundeordrelinje. Disse attributtene inkluderer leveringsmåten og oppfyllelseslokasjonen. Betalingen som forfaller for transaksjonen, blir en nettosum av returordrelinjene og salgsordrelinjene. Når betalingen er betalt for transaksjonen, blir returordren postert som et salgsordredokument i Headquarters, og systemet vil fakturere de returnerte linjene umiddelbart.

For å gi deg bedre oversikt over de ulike beløpene for handlekurven, er tre nye beløpsfelt lagt til i handlekurven. Du kan bruke skjermutformingen slik at disse nye feltene blir tilgjengelige i brukergrensesnittet for salgsstedet.

- **Brukt innbetaling** – Innbetalingsbeløpet som brukes for en transaksjon når brukeren utfører en kundeordrehenting. Hvis det ikke finnes overstyring av innbetaling, og en innbetaling på 10 prosent er konfigurert, vil beløpet i dette feltet være 90 prosent av totalbeløpet for kundeordren.
- **Utfør beløp** – Det totale beløpet for linjer der leveringsmåten ble satt til **Utfør** når kundeordren ble opprettet eller redigert, eller under en kundeordreutveksling. Beløpet i dette feltet inneholder avgifter og tillegg.
- **Returbeløp** – Det totale beløpet for linjer som har negative antall under kundeordreutvekslingen. Beløpet i dette feltet inneholder avgifter og tillegg.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
