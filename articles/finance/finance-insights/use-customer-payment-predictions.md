---
title: Bruke kundebetalingsforutsigelser (forhåndsversjon)
description: Dette emnet leder deg gjennom forutsetningene og de brede trinnene som kreves for å bruke en prøveversjon av Finance Insights.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: e0445046d8016dfa2c02c1ff1a05bdd148f9409a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969259"
---
# <a name="use-customer-payment-predictions-preview"></a>Bruke kundebetalingsforutsigelser (forhåndsversjon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet forklarer hvordan du bruker kundebetalingsprognoser. Før du bruker denne funksjonen, må du kontrollere at du har fullført konfigurasjonstrinnene for den. Hvis du vil ha mer informasjon, se [Aktivere kundebetalingsprediksjoner](enable-cust-paymnt-prediction.md).

Du kan vise kundebetalingspredisjoner i arbeidsområdet **Behandle kundekreditt og innkrevinger** og på to nye listesider, **Betalingsprediksjoner per transaksjon** og **Betalingsprediksjoner per kunde**.

### <a name="manage-customer-credit-and-collections-workspace"></a>Arbeidsområdet Behandle kundekreditt og innkrevinger

Arbeidsområdet **Behandle kundekreditt og innkrevinger** inneholder to nye fliser, **Betalingspredisjon per transaksjon** og **Kunder med forventet høy forsinket-saldo**.

- Flisen **Betalingspresisjon per transaksjon** viser antall åpne kundetransaksjoner som har en betalingssannsynlighet som er mindre enn 50 prosent i **Til planlagt tid**-perioden. Du kan velge denne flisen for å åpne listesiden **Betalingsprediksjoner per transaksjon**.
- Flisen **Kunder med forventet høy forsinket-saldo** viser antall kunder der mer enn halvparten (50 prosent) av den totale saldoen forventes å betale forsinket og/eller svært sent. Du kan velge denne flisen for å åpne listesiden **Betalingsprediksjon per kunde**.

[![Arbeidsområdet Behandle kundekreditt og innkrevinger](./media/manage-customer-credit-collections.png)](./media/manage-customer-credit-collections.png)

### <a name="payment-predictions-per-transaction-list-page"></a>Listesiden Betalingsprediksjoner per transaksjon

På listesiden **Betalingspredisjoner per transaksjon** kan du vise sannsynligheten for betaling for åpne transaksjoner i periodene **Til planlagt tid**, **Forsinket** og **Svært sent**. For hver transaksjon i rutenettet viser kolonnen **Til planlagt tid-sannsynlighet** sannsynligheten for at fakturaen betales på eller før forfallsdatoen. Hvis sannsynligheten for at en betaling betales innen fristen er mindre enn 50 prosent, vises en rød sirkel ved siden av prosenten i kolonnen **Til planlagt tid-sannsynlighet** for å angi risikoen for sen betaling.

[![Siden Betalingsprediksjoner per transaksjon](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Ruten **Relatert informasjon** til høyre på siden viser flere detaljer om prediksjoner:

- For transaksjonen som er valgt i rutenettet, viser hurtigfanen **Betalingsprediksjon** detaljene for betalingsprediksjonene i perioden **Til planlagt tid**, **Forsinket** og **Svært sent**. Delen for **Viktigste faktorer** viser de viktigste faktorene som påvirket prediksjonene. De viktigste faktorene er attributter for den valgte transaksjonen og/eller kunden for denne transaksjonen.
- Hurtigfanen **Customer Insights** viser gjeldende faktura-, betalings- og purrestatistikk for kunden for den valgte transaksjonen.
- Hurtigfanen **Kundehistorikk** viser kundens betalingslogg for **Til planlagt tid**, **Forsinket** og **Svært sent**.

Dataene i delen for **Viktigste faktorer** og i hurtigfanene **Kundeinnsikt** og **Kundehistorikk** bidrar til å forklare betalingsprediksjonene. Det kan bidra til å øke tiltroen til effekten av prediksjonene.

[![Grafiske indikatorer for betalingsprediksjoner på siden Relatert informasjon](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="payment-prediction-per-customer-list-page"></a>Listesiden Betalingspredisjon per kunde

Listesiden **Betalingsprediksjon per kunde** viser den totale åpne saldoen, og beløpet som forventes å bli betalt **Til planlagt tid**, **Forsinket** og **Svært sent**.

[![Listesiden Betalingspredisjoner per kunde](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

Betalingsbeløpet i hver samling beregnes som summen av det vektede gjennomsnittet av transaksjonssaldoen. Dette beløpet beregnes på grunnlag av betalingssannsynligheten i hver samling.

En kunde har for eksempel tre åpne transaksjoner som har følgende betalingssannsynligheter i hver samling.

| Transaksjon | Beløp | Sannsynlighet for betaling Til planlagt tid | Sannsynlighet for for sen betaling | Sannsynlighet for svært sen betaling |
|-------------|--------|-----------------------------|--------------------------|-------------------------------|
| T1          | 100    | 10 prosent                  | 50 prosent               | 40 prosent                    |
| A2          | 1 000  | 50 prosent                  | 30 prosent               | 20 prosent                    |
| T3          | 10,000 | 1 prosent                   | 4 prosent                | 95 prosent                    |

I dette tilfellet blir betalinger beregnet for hver samling på følgende måte.

| Samlinger   | Transaksjon T1      | Transaksjon T2         | Transaksjon T3            | Totalsum |
|-----------|---------------------|------------------------|---------------------------|-------|
| Til planlagt tid   | 100 × 10 ÷ 100 = 10 | 1000 × 50 ÷ 100 = 500 | 10.000 × 1 ÷ 100 = 100    | 610   |
| For sent      | 100 × 50 ÷ 100 = 50 | 1 000 × 30 ÷ 100 = 300 | 10 000 × 4 ÷ 100 = 400    | 750   |
| Veldig forsinket | 100 × 40 ÷ 100 = 40 | 1 000 × 20 ÷ 100 = 200 | 10 000 × 95 ÷ 100 = 9 500 | 9,740 |

Delen **Relatert informasjon** til høyre på siden viser flere detaljer om prediksjoner:

- For transaksjonen som er valgt i rutenettet, viser hurtigfanen **Betalingsprediksjoner** detaljene for betalingsprediksjonene i perioden **Til planlagt tid**, **Forsinket** og **Svært sent**. Delen for **Viktigste faktorer** viser de viktigste faktorene som påvirket betalingene. De viktigste faktorene er attributter for den valgte transaksjonen og/eller kunden for denne transaksjonen.
- Hurtigfanen **Customer Insights** viser gjeldende faktura-, betalings- og purrestatistikk for kunden for den valgte transaksjonen.
- Hurtigfanen **Kundehistorikk** viser kundens betalingslogg for **Til planlagt tid**, **Forsinket** og **Svært sent**.

Dataene i delen for **Viktigste faktorer** og i hurtigfanene **Kundeinnsikt** og **Kundehistorikk** bidrar til å forklare betalingsprediksjonene. Det kan bidra til å øke tiltroen til effekten av prediksjonene.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Forbedre nøyaktigheten av betalingspredisjoner

Du kan vise nøyaktigheten av betalingsprediksjoner ved å gå til **Kreditt og innkrevinger \> Oppsett \> Finance insights \> Parametere for økonomisk innsikt**. I kategorien **Innsikt i kundebetaling** viser delen **Prognosemodell** nøyaktigheten til forutsigelsesmodellen som en prosent.

[![Nøyaktigheten av betalingspredisjoner](./media/finance-insights-parameters-accuracy-2nd.png)](./media/finance-insights-parameters-accuracy-2nd.png)

Hvis du ikke er fornøyd med nøyaktigheten, velger du koblingen **Forbedre modellnøyaktighet** for å åpne utvidelsesopplevelsen for AI Builder. I utvidelsesopplevelsen for AI Builder kan du velge eller avbryte merkingen av felter til du har valgt feltene du tror er viktigst for å forutse sannsynligheten for betaling på en nøyaktig måte. Når du er ferdig, kan du enkelt trene opp forutsigelsesmodellen igjen og publisere endringene. Den nylig opplærte forutsigelsesmodellen vil automatisk bli plukket opp for prediksjoner i Dynamics 365 Finance.

[![Utvidelsesopplevelse for AI Builder](./media/ai-builder.png)](./media/ai-builder.png)

## <a name="release-details"></a>Frigivelsesdetaljer

Den offentlige forhåndsversjonen av Finance Insights er tilgjengelig for prøving for distribusjoner i USA, Europa og Storbritannia. Microsoft legger gradvis til støtte for flere områder.

Funksjoner i offentlige forhåndsversjoner kan og bør bare aktiveres i sandkassemiljøer på lag 2. Oppsett og modeller for kunstig intelligens som er opprettet i et sandkassemiljø, kan ikke overføres til et produksjonsmiljø. Hvis du vil ha mer informasjon, kan du se [Ekstra vilkår for bruk for Microsoft Dynamics 365-forhåndsversjoner](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).

## <a name="privacy-notice"></a>Personvernerklæring

Forhåndsversjoner (1) kan ha redusert personvern og færre sikkerhetstiltak enn Dynamics 365 Finance and Operations-tjenesten, (2) er ikke inkludert i serviceavtalen (SLA) for denne tjenesten, (3) må ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) har begrenset støtte.
