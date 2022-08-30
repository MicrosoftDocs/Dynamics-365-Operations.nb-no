---
title: Ny tildeling av inntektsføring – scenario 4
description: Denne artikkelen går gjennom et scenario for ny tildeling der en linje fjernes fra en eksisterende, delvis fakturert salgsordre. Dette scenarioet gir samme resultat, uansett om linjen fjernes fra salgsordren eller settes til statusen Avbrutt.
author: bking
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: bking
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8ec28460319e7bfabe82261ee4ed7861c4b6eb11
ms.sourcegitcommit: 1909d18a74cef85aad020a6a7473281e451f58c7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348275"
---
# <a name="revenue-recognition-reallocation--scenario-4"></a>Ny tildeling av inntektsføring – scenario 4

[!include [banner](../includes/banner.md)]

Denne artikkelen går gjennom et scenario for ny tildeling der en linje fjernes fra en eksisterende, delvis fakturert salgsordre. Dette scenarioet gir samme resultat, uansett om linjen fjernes fra salgsordren eller settes til statusen Avbrutt.

I dette scenarioet er alternativet **Poster fakturakorrigeringer til Kunder ved ny tildeling** satt til **Nei** i fanen **Inntektsføring** på siden **Parametere for økonomimodul** (**Inntektsføring \> Oppsett \> Parametere for økonomimodul**).

[![Alternativ for å postere fakturakorreksjoner til Kunde satt til Nei.](./media/37_rev-rec-scenarios.png)](./media/37_rev-rec-scenarios.png)

Det opprettes en salgsordre for kunden US\_SI\_0003. Kunden kjøper en bærbar datamaskin (varenummer S0012), installasjonstjenester (varenummer S0001) og en støtteplan for den bærbare datamaskinen (varenummer S0008, Opprettholdt utviklingstjeneste). Inntekten for datamaskin- og installasjonstjenestene føres umiddelbart. Inntekten for støtteplanen blir periodisert og anerkjent i løpet av 12 måneder, som definert av datoområdet i kontrakten.

[![Salgsordrelinjer for den bærbare datamaskinen, installasjonstjenestene og støtteplanen.](./media/38_rev-rec-scenarios.png)](./media/38_rev-rec-scenarios.png)

Salgsordren er bekreftet. Ettersom alle tre varene er definert for inntektspristildeling, beregnes inntektsprisen når salgsordren bekreftes. Du kan vise inntekten som vil bli gjenkjent, på siden **Inntektspristildeling** (velg **Inntektspristildeling** på siden **Salgsordre** i handlingsruten i fanen **Behandle** i gruppen **Inntektsføring**). Inntekten for den bærbare datamaskinen blir postert til inntektskontoen med et beløp på USD 995,84. Inntekten for installasjonstjenestene blir også postert til inntektskontoen med et beløp på USD 314,47. Inntekten for støtteplanen blir postert til en periodisert inntektskonto med et beløp på USD 188,69. Summen av inntektsprisene må være lik summen av linjene som er satt opp til å registrere inntektspristildeling (USD 1 499,00).

[![Siden Inntektspristildeling.](./media/39_rev-rec-scenarios.png)](./media/39_rev-rec-scenarios.png)

Kunden faktureres for den bærbare datamaskinen og støtteplanen, men ikke for installasjonstjenestene. Illustrasjonen nedenfor viser regnskapsoppføringen som er postert for fakturaen.

[![Regnskapsoppføring for den fakturerte salgsordren.](./media/40_rev-rec-scenarios.png)](./media/40_rev-rec-scenarios.png)

Regnskapsoppføringen posterer USD 1 276,94 til Kunder. Ettersom denne fakturaen er en delvis faktura, vil imidlertid ikke inntekten eller den utsatte inntekten pluss avgiften være lik beløpet i Kunder. Forskjellen på USD 14,47 posteres til avsetningskontoen for delvis fakturainntekt.

Inntektsføringsplanen blir også opprettet.

[![Siden Inntektsføringsplan for den delvise fakturaen.](./media/41_rev-rec-scenarios.png)](./media/41_rev-rec-scenarios.png)

Senere bestemmer kunden seg for ikke å kjøpe installasjonstjenester. Derfor fjernes denne linjen fra salgsordren. Legg merke til at salgsordren ikke kan bekreftes på nytt, fordi bare fakturerte linjer blir værende på salgsordren.

[![Salgsordre etter at linjen for installasjonstjenestene er fjernet.](./media/42_rev-rec-scenarios.png)](./media/42_rev-rec-scenarios.png)

Selv om salgsordren ikke kan bekreftes, kan den tildeles på nytt. I salgsordren velger du **Tildeling av pris på nytt med nye ordrelinjer** for å åpne siden **Tildele pris på nytt med nye ordrelinjer**. Velg de to gjenværende salgsordrelinjene, og velg deretter **Oppdater ny tildeling**. Kolonnen **Beløp tildelt på nytt** viser den nye inntektsprisen for hver gjenværende salgsordrelinje.

[![Nye inntektspriser for den nytildelte prisen med nye ordrelinjer.](./media/43_rev-rec-scenarios.png)](./media/43_rev-rec-scenarios.png)

Deretter velger du **Forventet bilag** for å vise regnskapsoppføringene.

[![Regnskapsoppføringer på siden Forventet bilag.](./media/44_rev-rec-scenarios.png)](./media/44_rev-rec-scenarios.png)

På siden **Forventet bilag** tilbakefører de fem siste linjene den opprinnelige regnskapsposten fra den posterte fakturaen. De første fire linjene er de nye regnskapsoppføringene som blir postert for fakturaen. Det er viktig at du har forstått at en ny faktura ikke er presentert for kunden. Etter ny tildeling skylder kunden fortsatt USD 1 276,94, som er beløpet som må posteres til Kunder i den nye regnskapsoppføringen. Den nye inntekten eller utsatt inntekt pluss skatt er lik USD 1 276,94. Derfor trenger du ikke å postere til avsetningskontoen for delvis fakturainntekt.

Velg **Behandle** for å fullføre ny tildeling. En posteringsdato angis. Når ny tildeling er fullført, viser siden **Inntektspristildeling** den nye pristildelingen for de to gjenværende varene.

[![Ny tildeling av pris for de gjenværende varene på siden Inntekstpristildeling.](./media/45_rev-rec-scenarios.png)](./media/45_rev-rec-scenarios.png)

Inntektsføringsplanen ble også oppdatert, basert på den nye prisen for ny tildeling av inntekt. Fra salgsordren åpner du siden **Inntektsføringsplan**. Tidligere var det 13 linjer for varen S0008 (en 12-måneders plan ble tilordnet til denne varen). Nå er det 39 linjer: de 13 opprinnelige planlinjene, 13 tidsplanlinjer for tilbakeføring, og 13 linjer som er basert på den nye inntektsprisen.

[![Oppdatert inntektsføringsplan med 39 linjer for vare S0008.](./media/46_rev-rec-scenarios.png)](./media/46_rev-rec-scenarios.png)

Når du velger **Bilag**, viser fakturajournalen den opprinnelige regnskapsoppføringen. Hvis du vil vise tilbakeføringsposten og den nye regnskapsoppføringen fra salgsordren, velger du **Inntektsjusteringer** i handlingsruten og velger deretter **Bilag**.

Deretter åpner du siden **Alle kunder** (**Kunder \> Kunder \> Alle kunder**), velger kunde **US\_SI\_0003**, og velger deretter **Transaksjoner**. Siden **Kundetransaksjoner** viser bare den opprinnelige fakturaen (000008), sammen med den opprinnelige regnskapsoppføringen. Ettersom alternativer **Poster fakturakorrigeringer til Kunder** er satt til **Nei** på siden **Parametere for økonomimodul**, blir bare økonomimodulen oppdatert. Derfor vises ikke tilbakeførings- og oppdaterte regnskapsoppføringer. Legg merke til at inntektsjusteringstransaksjonene som ble opprettet i [scenario 3](rev-rec-reallocation-scenario-3.md), blir vist.

[![Opprinnelig regnskapsoppføring på siden Kundetransaksjoner.](./media/47_rev-rec-scenarios.png)](./media/47_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
