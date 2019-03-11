---
title: Kundebetalingsinnsikt (forhåndsvisning)
description: Dette emnet beskriver hvordan kundebetalingsinnsikt kan bidra til å forutse når en faktura skal betales, og hjelpe organisasjoner å opprette optimaliseringsstrategier som forbedrer sannsynligheten for at betalinger skjer i tide.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "344668"
---
# <a name="customer-payment-insights-preview"></a>Kundebetalingsinnsikt (forhåndsvisning)

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> Denne funksjonen er en del av en bestemt versjon, og den er bare tilgjengelig for brukere som har valgt privat forhåndsvisning. Denne funksjonen vil inkluderes i en kommende versjon som blir generelt tilgjengelig.

# <a name="overview"></a>Oversikt

For organisasjoner er det ofte vanskelig å forutse når en kunde betaler fakturaer. Denne mangelen på innsikt kan føre til unøyaktige kontantstrømprognoser, tidkrevende innkrevingsprosesser og mulighet for at ordrer frigis til kunder som kan utgjøre en kredittrisiko. Kundebetalingsinnsikt (forhåndsvisning) bruker maskinlæring til å forutse når en faktura blir betalt. I tillegg gir den optimaliseringsstrategier som kan skreddersys for å øke sannsynligheten for at kunder betaler innen fristen.

## <a name="predictions"></a>Prognoser

Betalingsprognoser gjor det mulig for organisasjoner å forbedre forretningsprosessene sine ved å:

-   Lett å identifisere fakturaer som sannsynligvis blir betalte for seint.
-   Ta nødvendige forholdsregler for å forbedre sjansen for å få betaling i tide.

Kundebetalingsinnsikt (forhåndsvisning) bruker maskinlæring til å forutse når en faktura blir betalt. Den bruker historisk faktura, betaling og kundedata for å opprette en maskinlæringsmodell som brukes til å forutse når en faktura skal betales.

For hver åpne faktura, forutser Kundebetalingsinnsikt (forhåndsvisning) tre sannsynligheter for betaling:

-  Sannsynlighet for at betalingen blir gjort til rett tid (innen fakturaens forfallsdato).
-  Sannsynlighet for at betalingen blir gjort innen 30 dager for fakturaens forfallsdato.
-  Sannsynlighet for at betalingen blir gjort etter 30 dager for fakturaens forfallsdato.

Sannsynligheten for betalinger vises i prognosedelen.

[![Betalingsprognoser](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)

Hver faktura er også tilordnet en vinnende sannsynlighet for betaling som bruker én av de tre sannsynlige betalingscenarioene som er definert ovenfor. Scenariet med størst sannsynlighet for betaling, er det vinnende scenariet.


La oss for eksempel anta at det for en faktura er en prognose som viser en 71 prosent sannsynlighet for at fakturaen betales innen tidsfristen, 13 prosent sannsynlighet for at fakturaen betales innen 30 dager etter forfallsdatoen, og 16 prosent sannsynlighet for at fakturaen betales etter 30 dager etter forfallsdatoen. Den høyeste sannsynligheten viser at fakturaen vil bli betalt innen tidsfristen, så fakturaen merkes med sannsynlighet for betaling innen tidsfristen.

[![Betalingsprognoser](./media/payment-predict.png)](./media/payment-predict.png)

## <a name="optimization-strategies"></a>Strategier for optimalisering

I tillegg til betalingsprognoser kan Kundebetalingsinnsikt (forhåndsvisning) bruke optimaliseringsstrategier til å forbedre sjansene for å få betalt i tide. Dette gjør det mulig for organisasjoner å foreta "Hva skjer hvis"-analyse ved å tillate brukere å justere faktura- og kundeparametere, og deretter sammenligne den tilhørende innvirkningen på sannsynligheten for å motta fakturabetalinger i tide.

En organisasjon ønsker for eksempel kanskje å evaluere virkningen av å oppdatere kontantrabatten på fakturaer med sannsynlighet for å motta betalingen til rett tid. Når fakturaene er optimalisert til å bruke den nye rabatten, kan brukerne se effekten av å bruke rabatten på sannsynligheten for å motta betalinger for disse fakturaene innen tidsfristen. Hvis kostnaden av å bruke rabatten er minimal sammenlignet med fordelen med å fp betaling innen tidsfristen, kan organisasjonen velge å bruke den valgte rabatten på alle fremtidige åpne ordrer.

> [!NOTE] 
> For øyeblikket er bare rabatt tilgjengelig som optimaliseringsstrategi for Kundebetalingsinnsikt (forhåndsvisning).

[![Optimaliserte prognoser](./media/optimized-pay.png)](./media/optimized-pay.png)

## <a name="how-to-get-customer-payment-insights-preview"></a>Få tilgang til Kundebetalingsinnsikt (forhåndsvisning)

Hvis du er interessert i å prøve Kundebetalingsinnsikt (forhåndsvisning), kan du sende en e-post til [teamet for forhåndsvisning av økonomisk innsikt](mailto:fiap@microsoft.com). 

## <a name="privacy-statement"></a>Personvernerklæring

Forhåndsvisninger lagrer kundedata i USA. I tillegg (1) kan forhåndsvisninger bruke mindre personvern og færre sikkerhetstiltak enn Dynamics 365 for Finance and Operations-tjenesten, (2) er forhåndsvisninger ikke inkludert i tjenestenivåavtalen for denne tjenesten, (3) må forhåndsvisninger ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) forhåndsvisninger har begrenset støtte.
