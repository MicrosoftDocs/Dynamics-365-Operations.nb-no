---
title: Ny tildeling av inntektsføring – scenario 1
description: Denne artikkelen går gjennom et scenario for ny tildeling der to salgsordrer angis, men de blir bare bekreftet. Det samme scenarioet vil gi like resultater hvis mer enn to salgsordrer har bekreftet status.
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
ms.openlocfilehash: 92af49d9446fd9ed3310d8d0d50af902e7a7e693
ms.sourcegitcommit: 1909d18a74cef85aad020a6a7473281e451f58c7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348333"
---
# <a name="revenue-recognition-reallocation--scenario-1"></a>Ny tildeling av inntektsføring – scenario 1

[!include [banner](../includes/banner.md)]

Denne artikkelen går gjennom et scenario for ny tildeling der to salgsordrer angis, men de blir bare bekreftet. Det samme scenarioet vil gi like resultater hvis mer enn to salgsordrer har bekreftet status.

I dette scenarioet er alternativet **Poster fakturakorrigeringer til Kunder ved ny tildeling** satt til **Nei** i fanen **Inntektsføring** på siden **Parametere for økonomimodul** (**Inntektsføring \> Oppsett \> Parametere for økonomimodul**).

[![Alternativ for å postere fakturakorreksjoner til Kunde satt til Nei.](./media/06_rev-rec-scenarios.png)](./media/06_rev-rec-scenarios.png)

Det opprettes en salgsordre for kunden US\_SI\_0003. Kunden kjøper en bærbar datamaskin (varenummer S0012) og en støtteplan for den (varenummer S0008, Opprettholdt utviklingstjeneste). Inntekten for den bærbare datamaskinen gjenkjennes umiddelbart (det er ingen inntektsføringsplan). Inntekten for støtteplanen blir periodisert og anerkjent i løpet av 12 måneder, som definert av datoområdet i kontrakten.

[![Salgsordrelinjer for den bærbare datamaskinen og støtteplanen.](./media/07_rev-rec-scenarios.png)](./media/07_rev-rec-scenarios.png)

Salgsordren er bekreftet. Ettersom begge varene er definert for inntektspristildeling, beregnes inntektsprisen når salgsordren bekreftes. Du kan vise inntekten som vil bli gjenkjent, på siden **Inntektspristildeling** (velg **Inntektspristildeling** på siden **Salgsordre** i handlingsruten i fanen **Behandle** i gruppen **Inntektsføring**). Inntekten for den bærbare datamaskinen blir postert til inntektskontoen med et beløp på USD 1 008,01. Inntekten for støtteplanen blir postert til den periodiserte inntektskontoen med et beløp på USD 190,99. Summen av inntektsprisene må være lik summen av linjene som er satt opp til å registrere inntektspristildeling (USD 1 199,00).

[![Siden Inntektspristildeling.](./media/08_rev-rec-scenarios.png)](./media/08_rev-rec-scenarios.png)

Kunden valgte ikke å kjøpe installasjonstjenester (varenummer S0001) på salgsstedet, men endret senere mening. Derfor angis det en ny salgsordre for den samme kunden.

[![Salgsordrelinje for installasjonstjenester.](./media/09_rev-rec-scenarios.png)](./media/09_rev-rec-scenarios.png)

Den andre salgsordren er bekreftet. Ettersom denne salgsordren bare inneholder én linje, vil det ikke bli utført inntektspristildeling når salgsordren bekreftes. Tildeling av inntektspris skjer bare hvis det er to eller flere unike varer, og hvis disse varene er definert for inntektspristildeling.

Hvis denne nye salgsordren er den eneste endringen i kundens kontrakt, kan prosessen for ny tildeling nå kjøres. I én av de to salgsordrene velger du **Tildeling av pris på nytt med nye ordrelinjer** for å åpne siden **Tildele pris på nytt med nye ordrelinjer**. Du kan også gå til **Inntektsføring \> Periodiske oppgaver \> Tildele pris på nytt med nye ordrelinjer**. Velg de to salgsordrene og de tilsvarende salgsordrelinjene, og velg deretter **Oppdater ny tildeling**. Kolonnen **Beløp tildelt på nytt** viser den nye inntektsprisen for hver salgsordrelinje.

[![Nye inntektspriser for den nytildelte prisen med nye ordrelinjer.](./media/10_rev-rec-scenarios.png)](./media/10_rev-rec-scenarios.png)

Hvis du velger **Forventet bilag**, vises ingenting, fordi ingen fakturaer er postert.

Velg **Behandle** for å fullføre ny tildeling. Du blir bedt om å bruke en posteringsdato, selv om ingenting posteres. Når den nye tildelingen er fullført, viser siden **Inntektspristildeling** for hver salgsordre pristildelingen for alle varer på tvers av begge salgsordrene. Med andre ord vil siden **Inntektspristildeling** for hver salgsordre inneholde en vare som ikke finnes på den salgsordren, fordi den er en del av den samme kontrakten, men på en annen salgsordre.

> [!TIP]
> Hvis du vil vise en kontekst om hvorfor disse tilleggsvarene vises, kan du legge til andre kolonner i rutenettet, for eksempel **ID for ny tildeling** og **Salgsordre**.
> 
> [![Tilleggskolonner på siden Inntektspristildelinger.](./media/11_rev-rec-scenarios.png)](./media/11_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
