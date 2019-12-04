---
title: Inntektsføring av salgsordrer
description: Dette emnet beskriver den grunnleggende funksjonaliteten for føring av inntekt på salgsordrer og fakturaer. Inntektsføring er tilgjengelig på salgsordren og på den tilsvarende fakturaen som opprettes fra salgsordren.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 6e2eafc6785aaf9bc7421bc80c90fa4a7f98a2d4
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/31/2019
ms.locfileid: "2693026"
---
# <a name="revenue-recognition-on-sales-orders"></a>Inntektsføring av salgsordrer

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Funksjonen Inntektsføring kan ikke aktiveres via Funksjonsbehandling. For øyeblikket må du bruke konfigurasjonsnøkler for å aktivere den.

Dette emnet beskriver den grunnleggende funksjonaliteten for føring av inntekt på salgsordrer og fakturaer. Inntektsføring er tilgjengelig på en salgsordre og på den tilsvarende fakturaen som opprettes fra salgsordren. Salgsordren kan også opprettes via et Etter regning-prosjekt.

> [!NOTE]
> I illustrasjonene i dette emnet har kolonner blitt skjult eller lagt til rutenett for å bedre vise begrepene. Derfor kan det hende at sidene og dataene i illustrasjonen avviker fra det du ser i produktet.

## <a name="enter-a-sales-order"></a>Registrere en salgsordre

Følgende salgsordre er angitt og omfatter tre varer som er definert for inntektsføring.

[![Registrere en salgsordre](./media/revenue-recognition-so-basic-sales-order-header.png)](./media/revenue-recognition-so-basic-sales-order-header.png)

Det finnes to begreper for inntektsføring:

- **Fastslå inntektsprisen.** Inntektsprisen beregnes på grunnlag av oppsettet til de frigitte produktene. Inntektsprisen vises aldri for kunden, men brukes bare for regnskapsføringen av salgsordrefakturaen. Salgsordrelinjene og dokumentene som skrives som en del av salget, fortsetter å vise enhets-/listeprisen.
- **Fastslå når inntektsføring skal skje.** En inntektsplan brukes til å bestemme når inntekt skal føres.

    I dette eksemplet er den første varen, S0001 tilordnet en **1O** (en-forekomst) inntektsplan. Denne linjen representerer et scenario for milepæltype, der inntekten vil bli ført etter at installasjonen skjer i fremtiden. Derfor utsettes inntekt til installasjonen er fullført.

    Den andre varen, S0008, er en servicevare som er definert som en PCS-vare. De opprettholdte utviklingstjenestene leveres til kunden i løpet av en periode på 12 måneder. Derfor tilordnes en **12M**-inntektsplan til produktet som standard. Siden denne varen er en PCS-vare, må kontraktens start- og sluttdatoer defineres. Som standard er start- og sluttdatoen for kontrakten funnet i vare detaljer – kategorien Oppsett. I inntektsplanen defineres oppsettet for **12M**, slik at kontrakts vilkårene automatisk fylles ut som vist i følgende illustrasjon.

    [![Inntektsplaner](./media/revenue-recognition-so-basic-revenue-schedules.png)](./media/revenue-recognition-so-basic-revenue-schedules.png)

    Den tredje varen, S0012, er maskinvare, og ingen inntektsplan er tilordnet som standard. Inntekten for maskin varen føres så snart varen er fakturert.

## <a name="confirm-the-sales-order"></a>Bekrefte salgsordren

Hvis du vil vise flere detaljer om inntektsprisen og inntektsplanen, bruker du knappene i gruppen **Inntektsføring** i kategorien **Behandle** i handlingsruten i salgsordren. Ettersom salgsordren ikke er bekreftet på dette tidspunktet, er ikke knappene som brukes til inntektsføring, tilgjengelige. Disse knappene blir tilgjengelige eller ikke tilgjengelige etter hvert som salgsordren går gjennom stadiene som fører til oppfyllelse.

[![Topptekst i salgsordre](./media/revenue-recognition-so-basic-sales-order-header-02.png)](./media/revenue-recognition-so-basic-sales-order-header-02.png)

De første tre knappene gir detaljer om inntektsprisen for varene i salgsordreoppsettet for inntektsføring.

- **Tildeling av inntektspris** – denne knappen blir tilgjengelig når salgsordren er bekreftet eller fakturaen posteres. Både salgsordrebekreftelse og fakturapostering beregner inntekten for å føre prisen som vil bli ført eller utsatt på regnskapsregistreringen. Avhengig av oppsettet kan inntektsprisen som beregnes, være forskjellig fra enhetsprisen som vises til kunden.
- **Tildele pris på nytt med nye ordrelinjer** – denne knappen blir tilgjengelig når salgsordren er bekreftet eller fakturaen posteres. Den nye tildelingsprosessen brukes til å omberegne inntekten som må føres etter at en ny linje er lagt til i den gjeldende salgsordren, etter at den er fakturert eller en ny salgsordre. I begge scenariene vil tillegging av en ny vare føre til en endring i kontrakten. Derfor må inntektsprisen tildeles på nytt.
- **Oppdatere inntektspristildeling** – denne knappen blir tilgjengelig når salgsordren er bekreftet, men den blir ikke tilgjengelig etter at salgsordren er fakturert. Oppdateringen brukes til å kjøre inntektspristildelingen på nytt uten å bekrefte salgsordren. Etter at salgsordren er fakturert, kan ikke inntektsprisen omberegnes.

De to siste knappene gir detaljer om inntektsplanen for de varene i salgsordren som har en inntektsplan.

- **Forventet inntektsføringsplan** – denne knappen blir tilgjengelig når salgsordren er bekreftet, men den blir ikke tilgjengelig etter at salgsordren er fakturert. Den åpner en side som viser den forventede inntektsplanen. Den endelige tidsplanen kan endres, fordi den forventede tidsplanen bruker den ønskede forsendelsesdatoen, mens den endelige planen bruker den faktiske forsendelsesdatoen.
- **Inntektsføringsplan** – denne knappen blir tilgjengelig når salgsordren er fakturert. Den endelige inntektsføringsplanen blir ikke opprettet når det skjer en bekreftelse eller det opprettes en følgeseddel. Den opprettes bare når salgsordren faktureres.

I eksemplet nedenfor ble inntektspristildeling utført når salgsordren ble bekreftet. Vær oppmerksom på at selv om inntektsprisene tildeles på en annen måte, må totalbeløpet i feltet **Inntekt som skal føres** fremdeles være identisk med summen for salgsordrelinjene som er fakturert til kunden. Summen av salgsordrelinjene, ekskl. mva., er for eksempel USD 1499. Derfor må summen av verdiene for **Inntekt som skal føres** også være USD 1499.

[![Inntektspristildeling](./media/revenue-recognition-so-basic-revenue-price-allocation.png)](./media/revenue-recognition-so-basic-revenue-price-allocation.png)

Den forventede inntektsføringsplanen blir også opprettet. Inntektsplanen bruker verdien for **Inntekt som skal føres** som beløpet som skal utsettes. Vare S0001 utsetter USD 321,21 i stedet for USD 300, og vare S0008en utsetter USD 160,61 i stedet for USD 100. Vare S0012 vises ikke i den forventede tidsplanen fordi inntekten ikke er utsatt. Når postering skjer, posterer var S0012 USD 1017,18 direkte til inntektsfinanskontoen.

[![Forventet inntektsføringsplan](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)

## <a name="create-the-packing-slip"></a>Opprette følgeseddelen

Deretter kan følgeseddelen opprettes for salgsordren. Ingen inntekt føres når følgeseddelen posteres. Hvis salgsordren ikke ble bekreftet, utløses ikke postering av følgeseddelen at inntektspris blir beregnet. Det utløser heller ikke opprettingen av den forventede eller endelige inntektsføringsplanen. Hvis varemodellgruppen er definert til å utsette inntekter på følgeseddelen, fortsetter den å postere ved hjelp av de gjeldende finanskontoene for posteringsprofil, og ikke de nye utsatte inntektskontoene som brukes i fakturaposteringen.

## <a name="create-the-invoice"></a>Opprette fakturaen

Det siste trinnet er å fakturere salgsordren. Hvis du ser på fakturaens bilag, vil du se at inntekten for varer S0001 og S0008 ble utsatt (USD 321,21 + 160,61 = 481,82), og det gjenstående beløpet for vare S0012 ble postert til inntekt (1 017,18). Disse verdiene blir til sammen USD 1499, som samsvarer med summen av salgsordrelinjene.

[![Bilagstransaksjoner](./media/revenue-recognition-so-voucher-transactions.png)](./media/revenue-recognition-so-voucher-transactions.png)

Etter at fakturaen er opprettet, blir knappene **Inntektspristildeling**, **Tildele pris på nytt med nye ordrelinjer** og **Inntektsføringsplan** for inntektsføring tilgjengelige, men knappene **Oppdatere inntektspristildeling** og **Forventet inntektsføringsplan** er utilgjengelige.

[![Tilgjengelighet for knapp for tilgjengelig inntektsføring](./media/revenue-recognition-so-basic-after-invoice-buttons.png)](./media/revenue-recognition-so-basic-after-invoice-buttons.png)

Knappen **Inntektspristildeling** er fremdeles tilgjengelig, og dermed kan du vise beregningen av inntektspris. Hvis ingenting er endret på salgsordren etter at det ble bekreftet, vil posteringen av fakturaen ikke endre det beregnede beløpet i feltet **Inntekt som skal føres**.

Den forventede inntektsføringsplanen blir fjernet og erstattet med den endelige inntektsføringsplanen. Detaljene for inntektsplanen beholdes for hver salgsordrelinje, og brukes til å frigi den utsatte inntekten til den faktiske inntekten, fordi kontraktsforpliktelser er oppfylt.

[![Tidsplan for endelig inntektsføring](./media/revenue-recognition-so-revenue-recognition-schedule.png)](./media/revenue-recognition-so-revenue-recognition-schedule.png)
