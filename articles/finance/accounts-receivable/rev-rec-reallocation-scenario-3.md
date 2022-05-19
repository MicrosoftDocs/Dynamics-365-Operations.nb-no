---
title: Ny tildeling av inntektsføring – scenario 3
description: Dette emnet går gjennom et scenario for ny tildeling der en ny linje legges til i en eksisterende, fakturert salgsordre. Når en ny vare legges til i en kontrakt, kan den legges til i en ny salgsordre eller til den eksisterende salgsordren.
author: kweekley
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3b3b41b09cc9f4c56fdb04f6a2c4156bc1637699
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726584"
---
# <a name="revenue-recognition-reallocation--scenario-3"></a>Ny tildeling av inntektsføring – scenario 3

[!include [banner](../includes/banner.md)]

Dette emnet går gjennom et scenario for ny tildeling der en ny linje legges til i en eksisterende, fakturert salgsordre. Når en ny vare legges til i en kontrakt, kan den legges til i en ny salgsordre eller til den eksisterende salgsordren. Dette scenarioet viser også hva som skjer når Kunder oppdateres på grunn av ny tildeling.

I dette scenarioet er alternativet **Poster fakturakorrigeringer til Kunder ved ny tildeling** satt til **Ja** i fanen **Inntektsføring** på siden **Parametere for økonomimodul** (**Inntektsføring \> Oppsett \> Parametere for økonomimodul**).

[![Alternativ for å postere fakturakorreksjoner til Kunde satt til Ja.](./media/25_rev-rec-scenarios.png)](./media/25_rev-rec-scenarios.png)

Det opprettes en salgsordre for kunden US\_SI\_0003. Kunden kjøper en bærbar datamaskin (varenummer S0012) og en støtteplan for den (varenummer S0008, Opprettholdt utviklingstjeneste). Inntekten for den bærbare datamaskinen føres umiddelbart. Inntekten for støtteplanen blir periodisert og anerkjent i løpet av 12 måneder, som definert av datoområdet i kontrakten.

[![Salgsordrelinjer for den bærbare datamaskinen og støtteplanen.](./media/26_rev-rec-scenarios.png)](./media/26_rev-rec-scenarios.png)

Salgsordren er bekreftet. Ettersom begge varene er definert for inntektspristildeling, beregnes inntektsprisen når salgsordren bekreftes. Du kan vise inntekten som vil bli gjenkjent, på siden **Inntektspristildeling** (velg **Inntektspristildeling** på siden **Salgsordre** i handlingsruten i fanen **Behandle** i gruppen **Inntektsføring**). Inntekten for den bærbare datamaskinen blir postert til inntektskontoen med et beløp på USD 1 008,01. Inntekten for støtteplanen blir postert til den periodiserte inntektskontoen med et beløp på USD 190,99. Summen av inntektsprisene må være lik summen av linjene som er satt opp til å registrere inntektspristildeling (USD 1 199,00).

[![Siden Inntektspristildeling.](./media/27_rev-rec-scenarios.png)](./media/27_rev-rec-scenarios.png)

Salgsordren er fullstendig fakturert. Illustrasjonen nedenfor viser regnskapsoppføringen som er postert for fakturaen.

[![Regnskapsoppføring for den fullt fakturerte salgsordren.](./media/28_rev-rec-scenarios.png)](./media/28_rev-rec-scenarios.png)

Inntektsføringsplanen blir også opprettet. Etter at tiden er over, har to av månedene ført inntekt for støtteplanen.

[![Siden Inntektsføringsplan etter at to måneder er gått.](./media/29_rev-rec-scenarios.png)](./media/29_rev-rec-scenarios.png)

På dette tidspunktet bestemmer kunden seg for å legge til installasjonstjenester (varenummer S0001). Denne varen legges til i den eksisterende salgsordren. Kunden blir bedt om å bekrefte at vedkommende vil endre den fullt fakturerte salgsordren, og velger **Ja**.

[![Salgsordre etter at linjen for installasjonstjenestene er lagt til.](./media/30_rev-rec-scenarios.png)](./media/30_rev-rec-scenarios.png)

Hvis denne nye varen er den eneste endringen i kundens kontrakt, kan prosessen for ny tildeling nå kjøres. I salgsordren velger du **Tildeling av pris på nytt med nye ordrelinjer** for å åpne siden **Tildele pris på nytt med nye ordrelinjer**. Velg alle salgsordrelinjene for denne salgsordren, og velg deretter **Oppdater ny tildeling**. Kolonnen **Beløp tildelt på nytt** viser den nye inntektsprisen for hver salgsordrelinje.

[![Nye inntektspriser for den nytildelte prisen med nye ordrelinjer.](./media/31_rev-rec-scenarios.png)](./media/31_rev-rec-scenarios.png)

Deretter velger du **Forventet bilag** for å vise regnskapsoppføringene. Ettersom alternativet **Poster fakturakorrigeringer til Kunder** er satt til **Ja** på siden **Parametere for økonomimodul**, blir disse regnskapsoppføringene postert til økonomimodulen via kredittdokumentet, og en ny faktura blir opprettet i Kunder.

[![Regnskapsoppføringer på siden Forventet bilag.](./media/32_rev-rec-scenarios.png)](./media/32_rev-rec-scenarios.png)

På siden **Forventet bilag** tilbakefører de fire siste linjene den opprinnelige regnskapsposten fra den posterte fakturaen. De første fem linjene er de nye regnskapsoppføringene som blir postert for fakturaen. Det er viktig at du har forstått at en ny faktura ikke er presentert for kunden. Etter ny tildeling skylder kunden fortsatt USD 1 276,94, som er beløpet som må posteres til Kunder i den nye regnskapsoppføringen. Motpostering av avgifter og inntekt eller utsatt inntekt er lik USD 995,83 + USD 188,69 + USD 77,94 = USD 1 262,46. Inntekten eller det utsatte inntektsbeløpet er endret på grunn av den nye tildelingen. Forskjellen på USD 14,48 posteres til en avsetningskonto for delvis fakturainntekt. Denne saldoen slettes når fakturaen posteres for den nye varen som ble lagt til i salgsordren.

Velg **Behandle** for å fullføre ny tildeling. En posteringsdato angis. Når ny tildeling er fullført, viser siden **Inntektspristildeling** den nye pristildelingen for alle tre varer.

[![Ny tildeling av pris for alle de tre varene på siden Inntekstpristildeling.](./media/33_rev-rec-scenarios.png)](./media/33_rev-rec-scenarios.png)

Inntektsføringsplanen ble også oppdatert, basert på den nye prisen for ny tildeling av inntekt. Fra salgsordren åpner du siden **Inntektsføringsplan**. Tidligere var det 13 linjer for varen S0008 (en 12-måneders plan ble tilordnet til denne varen). Nå er det 39 linjer: de 13 opprinnelige planlinjene, 13 tidsplanlinjer for tilbakeføring, og 13 linjer som er basert på den nye inntektsprisen.

[![Oppdatert inntektsføringsplan med 39 linjer for vare S0008.](./media/34_rev-rec-scenarios.png)](./media/34_rev-rec-scenarios.png)

Når du velger **Bilag**, viser fakturajournalen den opprinnelige regnskapsoppføringen. Hvis du vil vise tilbakeføringsposten og den nye regnskapsoppføringen fra salgsordren, velger du **Inntektsjusteringer** i handlingsruten og velger deretter **Bilag**.

Deretter åpner du siden **Alle kunder** (**Kunder \> Kunder \> Alle kunder**), velger kunde **US\_SI\_0003**, og velger deretter **Transaksjoner**. Siden **Kundetransaksjoner** viser den opprinnelige fakturaen (000006), tilbakeføringsdokumentet (000006-1) og den nye fakturaen (000006-2). Den opprinnelige fakturaen og tilbakeføringsdokumentet utlignes mot hverandre og har en saldo på 0 (null). Vis bilaget for hvert dokument for å se virkningen i økonomimodulen.

[![Opprinnelig faktura, tilbakeføringsdokument og den nye fakturaen på siden Kundetransaksjoner.](./media/35_rev-rec-scenarios.png)](./media/35_rev-rec-scenarios.png)

Salgsordren faktureres på nytt for varen som ble lagt til. Totalfakturaen som presenteres for kunden, er på USD 300,00 + USD 19,50 = USD 319,50. Illustrasjonen nedenfor viser regnskapsoppføringen som er postert.

[![Bilagstransaksjonssiden med regnskapsoppføringen som er postert.](./media/36_rev-rec-scenarios.png)](./media/36_rev-rec-scenarios.png)

Ettersom summen av inntekten og salget er mer enn USD 319,50, posteres differansen for USD 14,48. Dette beløpet fjerner saldoen fra avsetningskontoen for delvis fakturainntekt. Denne saldoen ble oppdatert i den nye regnskapsoppføringen som ble postert etter den nye tildelingen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
