---
title: Ny tildeling av inntektsføring – scenario 2
description: Dette emnet går gjennom et scenario for ny tildeling der det angis to salgsordrer, og deretter legger kunden til en vare i kontrakten etter at den første salgsordren er fakturert. Når en ny vare legges til i en kontrakt, kan den legges til i en ny salgsordre eller til den eksisterende salgsordren.
author: kweekley
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 53e5173accb83150b2c76d93b971d8908aba2a3d
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356203"
---
# <a name="revenue-recognition-reallocation--scenario-2"></a>Ny tildeling av inntektsføring – scenario 2

[!include [banner](../includes/banner.md)]

Dette emnet går gjennom et scenario for ny tildeling der det angis to salgsordrer, og deretter legger kunden til en vare i kontrakten etter at den første salgsordren er fakturert. Når en ny vare legges til i en kontrakt, kan den legges til i en ny salgsordre eller til den eksisterende salgsordren.

I dette scenarioet er alternativet **Poster fakturakorrigeringer til Kunder ved ny tildeling** satt til **Nei** i fanen **Inntektsføring** på siden **Parametere for økonomimodul** (**Inntektsføring \> Oppsett \> Parametere for økonomimodul**).

[![Alternativ for å postere fakturakorreksjoner til Kunde satt til Nei.](./media/12_rev-rec-scenarios.png)](./media/12_rev-rec-scenarios.png)

Det opprettes en salgsordre for kunden US\_SI\_0003. Kunden kjøper installasjonstjenester (varenummeret S0001) og en støtteplan (varenummeret S0008) for en bærbar datamaskin, men har ikke valgt den bærbare datamaskinen ennå. Inntekten for installasjonstjenestene vil bli utsatt til datoen da den bærbare datamaskinen kjøpes. Inntekten for støtteplanen blir periodisert og anerkjent i løpet av 12 måneder, som definert av datoområdet i kontrakten.

[![Salgsordrelinjer for den installasjonstjenestene og støtteplanen.](./media/13_rev-rec-scenarios.png)](./media/13_rev-rec-scenarios.png)

Salgsordren er bekreftet. Ettersom begge varene er definert for inntektspristildeling, beregnes inntektsprisen når salgsordren bekreftes. Du kan vise inntekten som vil bli gjenkjent, på siden **Inntektspristildeling** (velg **Inntektspristildeling** på siden **Salgsordre** i handlingsruten i fanen **Behandle** i gruppen **Inntektsføring**). Inntekten for installasjonstjenestene blir postert til en periodiserte inntektskonto med et beløp på USD 250,00. Inntekten for støtteplanen blir også postert til den periodiserte inntektskontoen med et beløp på USD 150,00. Summen av inntektsprisene må være lik summen av linjene som er satt opp til å registrere inntektspristildeling (USD 400,00).

[![Siden Inntektspristildeling.](./media/14_rev-rec-scenarios.png)](./media/14_rev-rec-scenarios.png)

Salgsordren er fullstendig fakturert. Illustrasjonen nedenfor viser regnskapsoppføringen som er postert for fakturaen.

[![Regnskapsoppføring for den fullt fakturerte salgsordren.](./media/15_rev-rec-scenarios.png)](./media/15_rev-rec-scenarios.png)

Inntektsføringsplanen opprettes også, men ingen av inntektene føres ennå.

[![Side for inntektsføringsplan.](./media/16_rev-rec-scenarios.png)](./media/16_rev-rec-scenarios.png)

Noen dager senere velger kunden en bærbar datamaskin. En ny salgsordre angis for kunden.

[![Salgsordrelinje for den bærbare datamaskinen.](./media/17_rev-rec-scenarios.png)](./media/17_rev-rec-scenarios.png)

Den andre salgsordren er bekreftet. Ettersom denne salgsordren bare inneholder én linje, vil det ikke bli utført inntektspristildeling når salgsordren bekreftes. Tildeling av inntektspris skjer bare hvis det er to eller flere unike varer, og hvis disse varene er definert for inntektspristildeling.

Hvis denne nye salgsordren er den eneste endringen i kundens kontrakt, kan prosessen for ny tildeling nå kjøres. I én av de to salgsordrene velger du **Tildeling av pris på nytt med nye ordrelinjer** for å åpne siden **Tildele pris på nytt med nye ordrelinjer**. Du kan også gå til **Inntektsføring \> Periodiske oppgaver \> Tildele pris på nytt med nye ordrelinjer**. Velg de to salgsordrene og de tilsvarende salgsordrelinjene, og velg deretter **Oppdater ny tildeling**. Kolonnen **Beløp tildelt på nytt** viser den nye inntektsprisen for hver salgsordrelinje.

[![Nye inntektspriser for den nytildelte prisen med nye ordrelinjer.](./media/18_rev-rec-scenarios.png)](./media/18_rev-rec-scenarios.png)

Deretter velger du **Forventet bilag** for å vise regnskapsoppføringene som bare blir postert til økonomimodulen. Ettersom alternativet **Poster fakturakorreksjoner til Kunder** er satt til **Nei** på siden **Parametere for økonomimodul**, vil ingenting bli endret i Kunder når ny tildeling behandles.

[![Regnskapsoppføringer på siden Forventet bilag.](./media/19_rev-rec-scenarios.png)](./media/19_rev-rec-scenarios.png)

På siden **Forventet bilag** tilbakefører de tre siste linjene den opprinnelige regnskapsposten fra den posterte fakturaen. De første fire linjene utgjør den nye regnskapsoppføringen som er postert for fakturaen. Det er viktig at du har forstått at en ny faktura ikke er presentert for kunden. Etter ny tildeling skylder kunden fortsatt USD 426,00, som er beløpet som må posteres til Kunder i den nye regnskapsoppføringen. Motpostering av avgifter og utsatt inntekt er lik USD 188,69 + USD 314,48 + USD 26,00 = USD 529,17. Det utsatte inntektsbeløpet er endret på grunn av den nye tildelingen. Forskjellen på USD 103,17 posteres til en avsetningskonto for delvis fakturainntekt. Denne saldoen slettes når fakturaen posteres for den andre salgsordren som ble inkludert i ny tildeling.

Velg **Behandle** for å fullføre ny tildeling. Du blir bedt om å bruke en posteringsdato, selv om ingenting posteres. Når den nye tildelingen er fullført, viser siden **Inntektspristildeling** for hver salgsordre pristildelingen for alle varer på tvers av begge salgsordrene. Med andre ord vil siden **Inntektspristildeling** for hver salgsordre inneholde en vare som ikke finnes på den salgsordren, fordi den er en del av den samme kontrakten, men på en annen salgsordre.

> [!TIP]
> Hvis du vil vise en kontekst om hvorfor disse tilleggsvarene vises, kan du legge til andre kolonner i rutenettet, for eksempel **ID for ny tildeling** og **Salgsordre**.
> 
> [![Tilleggskolonner på siden Inntektspristildelinger.](./media/20_rev-rec-scenarios.png)](./media/20_rev-rec-scenarios.png)

I salgsordren 00036 ble også inntektsføringsplanen oppdatert, basert på den nye prisen for ny tildeling av inntekt. Fra denne salgsordren åpner du siden **Inntektsføringsplan**. Tidligere var det 13 linjer for varen S0008 (en 12-måneders plan ble tilordnet til denne varen). Nå er det 39 linjer: de 13 opprinnelige planlinjene, 13 tidsplanlinjer for tilbakeføring, og 13 linjer som er basert på den nye inntektsprisen.

[![Oppdatert inntektsføringsplan med 39 linjer for vare S0008.](./media/21_rev-rec-scenarios.png)](./media/21_rev-rec-scenarios.png)

På samme måte fantes det tidligere to linjer for vare S0001, men nå er det seks.

[![Oppdatert inntektsføringsplan med seks linjer for vare S0001.](./media/22_rev-rec-scenarios.png)](./media/22_rev-rec-scenarios.png)

Når du velger **Bilag** i salgsordre 000036, viser fakturajournalen den opprinnelige regnskapsoppføringen. Hvis du vil vise tilbakeføringsposten og den nye regnskapsoppføringen fra salgsordren, velger du **Inntektsjusteringer** i handlingsruten og velger deretter **Bilag**.

[![Salgsordre 000036.](./media/23_rev-rec-scenarios.png)](./media/23_rev-rec-scenarios.png)

Deretter åpner du siden **Alle kunder** (**Kunder \> Kunder \> Alle kunder**), velger kunde **US\_SI\_0003**, og velger deretter **Transaksjoner**. Den åpne fakturaen fra salgsordren 000036 vises. Hvis du velger bilaget, vil du se den opprinnelige regnskapsoppføringen, og ikke den nye regnskapsoppføringen fra den nye tildelingen. Tilbakeføringsoppføringen og den nye regnskapsoppføringen kan ikke vises fra Kunder.

Den andre salgsordren er nå fakturert. Totalfakturaen som presenteres for kunden, er på USD 1 099,00 + USD 71,44 = USD 1 170,44. Illustrasjonen nedenfor viser regnskapsoppføringen som er postert.

[![Bilagstransaksjonssiden med regnskapsoppføringen som er postert.](./media/24_rev-rec-scenarios.png)](./media/24_rev-rec-scenarios.png)

Ettersom summen av inntekten og salget er mer enn USD 1 170,44, posteres differansen for USD 130,17. Dette beløpet fjerner saldoen fra avsetningskontoen for delvis fakturainntekt. Denne saldoen posteres i den nye regnskapsoppføringen etter ny tildeling.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]