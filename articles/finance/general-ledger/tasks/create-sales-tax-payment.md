---
title: Opprette en mva-betaling
description: Jobbprosedyren Utlign og poster merverdiavgift utligner mva-saldoer på mva-kontoene og forskyver dem til mva-oppgjørskontoen for en gitt periode.
author: twheeloc
ms.date: 01/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c388a8f98cd4581abe2ec13d8922e232321e4039
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735938"
---
# <a name="create-a-sales-tax-payment"></a>Opprette en mva-betaling

[!include [banner](../../includes/banner.md)]

Jobbprosedyren Utlign og poster merverdiavgift utligner mva-saldoer på mva-kontoene og forskyver dem til mva-oppgjørskontoen for en gitt periode.

1. Gå til **Avgift > Deklareringer > Merverdiavgift > Utlign og poster merverdiavgift**.
2. Velg rullegardinknappen i **Utligningsperiode**-feltet for å åpne oppslaget.
3. Klikk på koblingen i den valgte raden i listen.
4. Angi en dato i **Fra dato**-feltet. Hvis du ikke velger alternativet **Ta med rettelser** på siden **Parametere for økonomimodul**, kan utligningen behandles for forskjellige versjoner. **Original** er den første utligningen for et periodeintervall og kan bare behandles én gang for et periodeintervall. De nyeste rettelsene utligner mva-transaksjoner som er postert etter at den opprinnelige versjonen er opprettet.
5. Angi en dato i feltet **Transaksjonsdato**.
6. Velg **OK**. Rapporten for **Mva-betalinger** skrives ut, slik at du kan gå gjennom de utlignede mva-transaksjonene i perioden.

Fra og med Finance versjon 10.0.24 kan du utelate rapporten **Mva-betalinger** som genereres like etter at den periodiske prosedyren **Utlign og poster merverdiavgift** er implementert under funksjonen **Generering av separat mva-betalingsrapport fra mva-utligning** i arbeidsområdet **Funksjonsbehandling**.

Når funksjonen er aktivert, blir det ikke skrevet ut en mva-betalingsrapport når utligningsprosessen er fullført. Du får i stedet følgende melding: «Mva-utligningen og posteringen er fullført. Bilaget ‘xxxx, m/d/åååå’ er postert.»

Du kan fortsatt kjøre mva-betalingsrapporten manuelt ved å gå til **Avgift** > **Forespørsler og rapporter** > **Merverdiavgiftforespørsler** > **Mva-betalinger**.

## <a name="performance-consideration"></a>Ytelseshensyn

Det kan ta lang tid å fullføre mva-betalingen. Hovedfaktorene som påvirker ytelsen til fremgangsmåten, er antall fakturaer i utligningsperioden og antall oppføringer som må posteres i utligningsbilaget for merverdiavgift. For å hjelpe til med å forbedre ytelsen kan du velge å hoppe over noe funksjonalitet som ikke kreves i prosessen.

### <a name="enable-the-sales-tax-payment-performance-improvement-feature"></a>Aktivere funksjonen for ytelsesforbedring av mva-betaling

Funksjonen for **ytelsesforbedring for mva-betaling** kan hjelpe deg med å forbedre ytelsen til betalingsprosedyren for mva ved å aggregere, på én linje, regnskapsvalutabeløpet og rapporteringsvalutabeløpet på bilagslinjene for mva-betaling som har samme hovedkonto, finansdimensjon og valuta.

1. Gå til **Systemadministrasjon** \> **Arbeidsområder** \> **Funksjonsbehandling**.
2. I kategorien **Alle** søker du etter og velger funksjonen for **ytelsesforbedring av mva-betaling**.
3. Velg **Aktiver**.

### <a name="prevent-generation-of-offset-tax-transactions"></a>Hindre generering av transaksjoner for motregningsavgift

Som standard posterer mva-betalingsbilaget motregnet merverdiavgift mot hver mva-transaksjon som utlignes i fremgangsmåten for mva-betaling. Disse motposterte mva-transaksjonene er inkludert i rapporten for **mva/finans-avstemming**. De viser utestående saldo på mva-transaksjoner som ikke er utlignet i løpet av perioden.

Motposteringene for mva-transaksjoner kan imidlertid øke belastningen for betalingsprosedyren for mva. Derfor kan en testversjon med navnet **TaxReportGenOffsetTaxTransPerRecordSetFlighting** aktiveres ved behov. Denne testversjonen kan hjelpe deg med å forbedre ytelsen til generering av motposterte mva-transaksjoner for land og områder, unntatt Thailand, Polen, Ungarn, Litausen, Malaysia, India, Italia, Russland, Tsjekkia, Estland og Latvia.

> [!NOTE]
> Hvis det er tilpassede felt i mva-transaksjonstabellen, kan ikke testversjonen aktiveres.

Siden rapporten for **mva/finans-avstemming** vanligvis bare brukes til interne kontrollformål og ikke kreves i mange avgiftsregimer, kan du velge å ikke generere motpostering av mva-transaksjoner på mva-betalingsbilaget.

1. Gå til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Mva-utligningsperioder**.
2. Velg en utligningsperiode.
3. I hurtigfanen **Generelt** angir du alternativet **Hindre generering av transaksjoner for motregningsavgift** til **Ja**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
