---
title: Ytelse for avgiftsberegning påvirker transaksjoner
description: Dette emnet inneholder feilsøkingsinformasjon som er relatert til ytelse for avgiftsberegning og innvirkningen på transaksjoner.
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: da19a83945450c2d35f95be2241b84e407860fe7808ff83934686ca2e00859bc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748960"
---
# <a name="tax-calculation-performance-affects-transactions"></a>Ytelse for avgiftsberegning påvirker transaksjoner

[!include [banner](../includes/banner.md)]

Noen ganger påvirkes en transaksjon av ytelsesproblemer som avgiftsberegningen har. Hvis du vil feilsøke dette problemet, følger du trinnene i de følgende delene etter behov.

## <a name="review-the-transaction-line-count"></a>Gå gjennom linjeantallet i transaksjonen

Bestem om transaksjonen har et stort antall linjer (for eksempel mer enn flere hundre). Hvis den ikke gjør det, kan du gå videre til den neste delen. Hvis transaksjonen har flere hundre linjer, utsetter du avgiftsberegningen. Hvis du vil ha mer informasjon, kan du se [Aktivere forsinket avgiftsberegning i journaler](enable-delayed-tax-calculation.md). 

Deretter kan du fastslå om en av følgende betingelser er oppfylt:

- Det finnes importtransaksjoner fra store filer.
- Flere økter behandler samme beregning av transaksjonsavgift samtidig.
- Transaksjonen har flere linjer, og visningene oppdateres i sanntid. Feltet **Beregnet mva-beløp i journalen** på **Økonomijournal**-siden oppdateres for eksempel i sanntid når en linjes felt endres.

   [![Feltet Beregnet mva-beløp i journalen på Journalbilag-siden.](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)

Hvis noen av disse betingelsene oppfylles, utsetter du avgiftsberegningen.

## <a name="review-the-call-stack"></a>Gå gjennom samtalestakken

Gå gjennom samtalestakken for å fastslå om avgiftsberegning kalles flere ganger. Hvis den ikke gjør det, kan du gå videre til den neste delen. Hvis samtalestakken kalles flere ganger, følger du denne fremgangsmåten for å redusere beregningstider for skatt.

1. Hvis journalen har vurdert transaksjonen, kan du utsette avgiftsberegningen. Hvis du vil ha mer informasjon, kan du se [Aktivere forsinket avgiftsberegning i journaler](enable-delayed-tax-calculation.md).
2. Hvis transaksjonen er en bestilling, og programversjonen er senere enn 10.0.15, kan du utsette avgiftsberegningen til den endelige beregningen ved å aktivere testversjoneringen for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.

## <a name="review-the-call-stack-timeline"></a>Gå gjennom tidslinjen for samtalestakken

Gå gjennom tidslinjen for samtalestakk for å finne ut om følgende problemer finnes. Hvis de gjør det, må du aktivere testversjoneringen for **TaxUncommittedDoIsolateScopeFlighting** for å løse problemet.

- Transaksjonen fører til at systemet slutter å svare til økten slutter. Transaksjonen kan derfor ikke beregne mva-resultatet. Illustrasjonen nedenfor viser meldingsboksen "Økt avsluttet" som du mottar.

    [![Melding om avsluttet økt.](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)

- **TaxUncommitted**-metodene tar mer tid enn andre metoder. I følgende illustrasjon tar for eksempel metoden **TaxUncommitted::updateTaxUncommitted()** 43,34742 sekunder, mens andre metoder 0,09 sekunder.

    [![Metodevarigheter.](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)

## <a name="customizing-and-calling-tax-calculation"></a>Tilpasse og kalle avgiftsberegning

Når du tilpasser, må du ikke kalle avgiftsberegning på metoden **insert()** eller **update()** for hver linje. Avgiftsberegning bør kalles på transaksjonsnivå.

## <a name="determine-whether-customization-exists"></a>Fastslå om det finnes tilpasning

Hvis du har fullført trinnene i de forrige delene, men ikke har funnet problemet, må du avgjøre om det finnes tilpasning. Hvis det ikke finnes noen tilpasning, oppretter du en Microsoft-tjenesteforespørsel for mer støtte.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
