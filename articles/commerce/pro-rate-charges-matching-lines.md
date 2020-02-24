---
title: Fordele hodegebyrer til samsvarende salgslinjer
description: Dette emnet beskriver flere funksjoner for beregning og bruk av automatiske tillegg for handelskanalordrer ved å bruke funksjonen for avanserte automatiske gebyrer.
author: hhaines
manager: annbe
ms.date: 04/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 5c03b1a1db11098058022a6916dc5bddf5518f9b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023592"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a>Fordele hodegebyrer til samsvarende salgslinjer


[!include [banner](includes/banner.md)]

Dette emnet beskriver funksjonen for å gruppere automatiske gebyrer på hodenivå og fordele dem proporsjonalt til handelslinjer. Denne funksjonen er tilgjengelig for transaksjoner som opprettes ved salgsstedet (POS) i Retail-versjon 10.0.1 og salg som er opprettet i et telefonsenter i Retail-versjon 10.0.2.

Denne funksjonen er tilgjengelig bare hvis funksjonen [avanserte automatiske tillegg](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) er aktivert ved hjelp av alternativet på **Handelsparametere**-siden. I tillegg kan utvidet beregningsmetode for automatiske gebyrer bare brukes på salgsordrer som er opprettet ved hjelp av handelskanaler (salgsstedet, et telefonsenter og e-handelsplattformen til Dynamics).

Den nye funksjonaliteten gir organisasjoner større fleksibilitet i måten automatiske gebyrer på hodenivå beregnes og brukes på salgstransaksjoner.

I versjoner av appen som er eldre enn versjon 10.0.1, beregnes automatiske gebyrer på hodenivå som har en bestemt leveringsmåte bare når det er samsvar med leveringsmåten som er definert i salgsordrehodet.

For eksempel er automatiske gebyrer på hodenivå definert for leveringsmåten **99** og leveringsmåten **11**. Det opprettes en salgsordre, og leveringsmåten **99** er definert i ordrehodet. Men noen av linjene for salg er satt opp slik at de er sendt ved hjelp av leveringsmåten **11**. I dette tilfellet er det bare gebyrer på hodenivå som er knyttet til leveringsmåten **99**, som blir tatt hensyn til og brukt på salgsordren.

I Commerce har gebyrer på hodenivå en tilleggsfunksjon som lar deg definere en [konfigurasjon av fordelt tillegg](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery) som er basert på ordreverdien. Hvis orderverdien er mellom USD 50,00 og USD 200,00, kan en organisasjon for eksempel belaste et fraktgebyr på USD 5,00. Hvis orderverdien er mellom USD 200,01 og USD 500,00, kan imidlertid fraktkostnadene være USD 4,00.

Noen organisasjoner ønsker fordelene med beregningen av fordelte tillegg som følger med gebyrer på hodenivå. I scenarioer med blandede leveringsmåter vil de også være sikre på at tilleggene som er beregnet, er basert på treff med leveringsmåten som er definert på hver salgslinje.

Du kan nå konfigurere automatiske gebyrer på hodenivå, slik at alle leveringsmåter på bestillingen medregnes når tillegg beregnes. Denne funksjonen krever en mer sammensatt beregningslogikk for å beregne gebyrer på hodenivå. Logikken grupper alle varer som leveres ved hjelp av samme beregningsmodus for levering, og den behandler den gruppen som beregningsgruppen for varene ved beregning av automatiske gebyrer på hodenivå. For varer som har samme leveringsmåte, er automatiske gebyrer beregnet basert på den totale salgsverdien for varene. På denne måten bestemmes riktig automatisk tillegg.

Etter at riktige gebyrer på hodenivå hentes fra salgslinjene som sendes ved hjelp av samme leveringsmåte, blir de beregnede kostnadene fordelt ned til salgslinjenivå. Fordi disse gebyrene er på linjenivå og ikke holdes på overskriftsnivå, lages en mer spesifikk kobling mellom varen og tilleggsverdien som ble beregnet for den. Dette kan være nyttig i delvise returscenarier der en organisasjon vil refundere bare en del av tillegget i stedet for hele tillegget når bare noen varer returneres.

## <a name="scenarios"></a>Scenarier

Følgende to eksempelscenarier viser hvordan disse gebyrene er beregnet både når den nye funksjonaliteten brukes, og når den brukes ikke.

### <a name="scenario-1"></a>Scenario 1

Dette scenariet beskriver virkemåten når alternativet **Fordel til samsvarende salgslinjer** er **Nei** i det automatiske oppsettet. (Virkemåten er lik virkemåten til gebyrer på hodenivå i appversjoner som er eldre enn versjon 10.0.1).

I dette scenarioet har organisasjonen definert gebyrer på hodenivå for relasjon for leveringsmåte **99** og relasjon for leveringsmåte **11**. Ingen automatiske tillegg som er konfigurert for leveringsmåte **21**.

![Automatiske tillegg for leveringsmåte 99 når linjesamsvarsfordeling er slått av](media/99_disabled.png)

![Automatiske tillegg for leveringsmåte 11 når linjesamsvarsfordeling er slått av](media/11_disabled.png)

Det opprettes en salgsordre i telefonsenteret, og leveringsmåten settes til **99**. Denne rekkefølgen inneholder fem elementer. To ordrelinjer er konfigurert for å bruke leveringsmåten **99**, to linjer er konfigurert til å bruke leveringsmåten **11**, og én linje er konfigurert for å bruke leveringsmåten **21**, som vist i eksempelet i tabellen nedenfor.

| Artikkel  | Linjeantall | Leveringsmåte | Pris per enhet |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | USD 10            |
| 81332 | 1             | 99            | USD 50            |
| 81333 | 2             | 11            | USD 30            |
| 81334 | 3             | 99            | USD 10            |
| 81334 | 3             | 21            | USD 5             |

I dette scenarioet evalueres hele ordren mot tabellen for automatisk tillegg for leveringsmåten **99**. Hele totalen for alle salgslinjer brukes til å finne et samsvarende nivå i konfigurasjonen for automatisk tillegg, og dette tillegget brukes på ordrehodenivå. I dette eksemplet er ordretotalen USD 165,00, og frakttillegget på USD 15,00 brukes på ordrehodet. Automatiske tillegg som er konfigurert for leveringsmåten **11**, er aldri referert til eller brukt.

I dette scenarioet, hvis en kunde returnerer noen av varene i ordren, og hvis [tilleggskoden er konfigurert slik at den blir refundert](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), blir totalt hodenivåtillegg systematisk brukt til refunderingen, selv om bare noen av varene returneres.

### <a name="scenario-2"></a>Scenario 2

I dette scenarioet defineres gebyrer på hodenivå for relasjon for leveringsmåte **99** og relasjon for leveringsmåte **11**. Men alternativet **Fordel til samsvarende salgslinjer** settes til **Ja** for disse tabellene for automatisk tillegg.

![Automatiske tillegg for leveringsmåte 99 når linjesamsvarsfordeling er slått på](media/99_enabled.png)

![Automatiske tillegg for leveringsmåte 11 når linjesamsvarsfordeling er slått på](media/11_enabled.png)

Dette scenarioet bruker den samme salgsordren som har fem linjer. Leveringsmåte på ordrehodet er satt til **99**, men leveringsmåten for hver vare i salgsordren konfigureres som vist i følgende tabell.

| Artikkel  | Linjeantall | Leveringsmåte | Pris per enhet |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | USD 10            |
| 81332 | 1             | 99            | USD 50            |
| 81333 | 2             | 11            | USD 30            |
| 81334 | 3             | 99            | USD 10            |
| 81334 | 3             | 21            | USD 5             |

Fordi automatisk tillegg-konfigurasjonen er satt til å fordele til samsvarende salgslinjer, utfører systemet følgende beregningstrinn.

1. Alle varer som har samme leveringsmåte, grupperes sammen, og systemet beregner den totale produktverdien av varene i gruppen.

    **Leveringsmodus 11**

    - Vare 81331, antall 1 = USD 10
    - Vare 81333, antall 2 = USD 60 netto (USD 30 per enhet)
    - **Total verdi av produktet for leveringsmåten 11 = USD 70**

    **Leveringsmodus 99**

    - Vare 81332, antall 1 = USD 50
    - Vare 81334, antall 3 = USD 30 netto
    - **Total verdi av produktet for leveringsmåten 99 = USD 80**

    **Leveringsmodus 21**

    - Vare 81334, antall 3 = USD 15 netto
    - **Total verdi av produktet for leveringsmåten 21 = USD 15**

2. Systemet søker etter konfigurasjonen for automatiske gebyrer på hodenivå som samsvarer med kunde- og leveringsmåteinnstillingene for hver varegruppe. Hvis konfigurasjonen blir funnet, leter systemet i den fordelte konfigurasjonen for å finne tillegget som skal brukes, basert på total produktverdi av varer i leveringsmåtegruppen.

    **Leveringsmodus 11**

    - Total produktverdi = USD 70
    - **Gebyrverdi = USD 7**

    **Leveringsmodus 99**

    - Total produktverdi = USD 80
    - **Gebyrverdi = USD 15**

    **Leveringsmodus 21**

    - Total produktverdi = USD 15
    - **Gebyrverdi = USD 0** (ingen automatiske gebyrer er konfigurert for denne kombinasjonen av kunde og leveringsmåte.)

    ![Leveringsmodus 11-gebyrer faller innenfor det merkede laget](media/step2mode11.png)

    ![Leveringsmodus 99-gebyrer faller innenfor det merkede laget](media/step2mode99.png)

3. Systemet beregner gebyrverdien som skal brukes på hver linje, basert på fordelingslogikk som vurderer den proporsjonale verdien av linjen i forhold til gruppens totale produktverdi.

    **Leveringsmodus 11**

    - Gebyrverdi = USD 7
    - Gruppeproduktverdi = USD 70
    - Linje 1-verdi = USD 10 (= 14,2857 % av gruppeverdien)
    - Linje 3-verdi = USD 60 (= 85,7143 % av gruppeverdien)
    - **Linjetillegg for linje 1 = USD 1**
    - **Linjetillegg for linje 3 = USD 6**

    **Leveringsmodus 99**

    - Gebyrverdi = USD 15
    - Gruppeproduktverdi = USD 80
    - Linje 2-verdi = USD 50 (= 62,5 % av gruppeverdien)
    - Linje 4-verdi = USD 30 (= 37,5 % av gruppeverdien)
    - **Linjetillegg for linje 2 = USD 9,38**
    - **Linjetillegg for linje 4 = USD 5,62**

    **Leveringsmodus 21**

    - Gebyrverdi = USD 0
    - Gruppeproduktverdi = USD 15
    - Linje 5-verdi = USD 15 (= 100 % av gruppeverdien)
    - **Linjetillegg for linje 5 = USD 0**

Derfor, i dette eksempelet, tilordnes varen 81334 et fraktgebyr på USD 5,62. Du kan vise disse gebyrene på siden **Vedlikehold tillegg** for salgslinjen. Illustrasjonen nedenfor viser hvordan denne siden ser ut for varen 81334.

![Fordelte tillegg på salgslinje for varen 81334](media/proratedlinecharge.png)

Når denne beregningsmåten brukes i en delvis retur-scenario, hvis tilleggskoden er refunderbar, vil bare delen av tillegget som er tilordnet til denne linjen, refunderes når varen returneres.
