---
title: Innsikt i kundebetaling (forhåndsvisning)
description: Dette emnet beskriver funksjonene for betalingsinnsikt som hjelper deg med å forstå de vanlige betalingspraksisene til en kunde. Funksjonen kan også hjelpe til med å identifisere omstendigheter som fører til at du starter innkrevingsprosesser tidligere enn du ellers ville starte dem.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f151942555ac503338f0fd44aa8779e3c2970fb1
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644639"
---
# <a name="customer-payment-insights-preview"></a>Innsikt i kundebetaling (forhåndsvisning)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet beskriver funksjonene for betalingsinnsikt som hjelper deg med å forstå de vanlige betalingspraksisene til en kunde. Funksjonen kan også hjelpe til med å identifisere omstendigheter som fører til at du starter innkrevingsprosesser tidligere enn du ellers ville starte dem. 

## <a name="overview"></a>Oversikt

Det kan være vanskelig å forutse når kunder betaler fakturaer. Denne mangelen på innsikt fører til mindre nøyaktige kontantstrømprognoser, innkrevingsprosesser som starter for sent, og ordrer som blir frigitt til kunder som ikke har utført betalingen. Kundebetalingsinnsikt (forhåndsversjon) hjelper organisasjoner med å forutse når en kundefaktura skal betales. Denne informasjonen kan hjelpe organisasjoner med å opprette strategier for innsamling som forbedrer sannsynligheten for betaling i tide. 

## <a name="predictions"></a>Prognoser

Betalingsprognoser gjør det mulig for organisasjoner å forbedre forretnings prosessene ved å hjelpe dem til enkelt å identifisere fakturaene som sannsynligvis betales for sent, og for å få riktige tiltak som forbedrer sjansen til å få betalt i tide.

Ved bruk av en maskinlæringsmodell, som benytter historiske fakturaer, betalinger og kundedata, kan kundebetalingsinnsikt (forhåndsvisning) mer nøyaktige forutsi når en kunde vil betale en utestående faktura.

For hver åpne faktura kan Kundebetalingsinnsikt (forhåndsvisning) predikere tre sannsynligheter for betaling:

-   Sannsynlighet for at betalingen utføres i tide 
-   Sannsynlighet for at betalingen utføres sent
-   Sannsynlighet for at betalingen utføres veldig sent

For å hjelpe organisasjoner med å forstå det totale betalingsbeløpet de kan forvente fra en kunde i én av de tre periodene, til rett tid, for sent og veldig sent, gir Kundebetalingsinnsikt (forhåndsvisning) også en samlet visning av forventede betalinger.

[![Aggregert visning av betalingsprognoser](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Hver faktura blir også tildelt en sannsynlighet for betaling i tide. Hvis sannsynlighet for betaling til rett tid er mindre enn 50 %, blir fakturaene merket med en rød sirkel for å angi at disse fakturaene kan måtte innkreves. 

[![Liste over sannsynligheter for betaling](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Innsikt i kundebetaling (forhåndsvisning) inneholder også kontekstavhengig informasjon som forklarer de viktigste faktorene som påvirket prognosene, den gjeldende forretningsstatusen til kunden og detaljer om den historiske kundebetalingsatferden. I mange bedrifter har innkrevingsprosessen vært en reaktiv aktivitet, innkrevingsprosessen starter ikke før fakturaer forfaller. 

Med Innsikt i kundebetaling (forhåndsvisning) kan organisasjoner bli mer proaktive om innkrevinger. De trenger ikke lenger å vente på at transaksjonene skal forfalle før start av innkrevingsprosessen. I stedet kan de bruke betalingsprognosefunksjonen til å fastslå om proaktive innkrevinger vil forbedre sannsynligheten for å bli betalt i tide. Betalingsforutsigelse gir også virksomheter informasjonen som kreves for å kunne starte innkrevingsprosessen tidlig.

## <a name="methodology"></a>Metodologi

Utvikling og distribusjon av en AI-løsning er vanskelig. Det krever en gruppe med datateknikere, fageksperter og teknikere som arbeider i lenge på et lengre tidsrom for å formulere, utvikle, distribuere og vedlikeholde en brukbar AI-løsning. Vi gjør det enkelt å distribuere og bruke AI-løsninger i Finance. Vi forhåndspakker AI-løsninger i Finance som er bygd på toppen av Microsoft AI Builder. En sluttbruker kan med et enkelt klikk på en knapp distribuere AI-løsningen og begynne å utnytte fordelene med intelligente prognoser. Hvis en organisasjon ikke er tilfreds med nøyaktigheten i prognosene, kan en privilegert bruker med ett enkelt klikk angi utvidelsesopplevelsen for AI Builder, og deretter merke av for eller fjerne merket for feltene som brukes til å generere prognoser. Når de er klare, kan de kalibrere og publisere endringene, og den nyutformede modellen blir automatisk plukket opp for prognoser i Finance.

## <a name="how-to-get-customer-payment-insights-preview"></a>Få tilgang til Kundebetalingsinnsikt (forhåndsvisning)

Hvis du er interessert i å prøve Kundebetalingsinnsikt (forhåndsvisning), kan du sende en e-post til [Innsikt i kundebetaling (forhåndsvisning)](mailto:fiap@microsoft.com).

## <a name="privacy-notice"></a>Personvernerklæring

Forhåndsvisninger (1) kan bruke mindre personvern og færre sikkerhetstiltak enn Dynamics 365 Finance and Operations-tjenesten, (2) er ikke inkludert i tjenestenivåavtalen for denne tjenesten, (3) må ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) har begrenset støtte.


