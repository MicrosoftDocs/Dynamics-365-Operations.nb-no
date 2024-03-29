---
title: Kundebetalingsforutsigelser
description: Denne artikkelen beskriver funksjonene for betalingsprediksjoner som kan hjelpe deg med å forstå de vanlige betalingspraksisene til en kunde. Denne funksjonen kan også hjelpe til med å identifisere omstendigheter som skal føre til at du starter innkrevingsprosesser tidligere enn du ellers ville starte dem.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 5d16b42b4538a18ca3dd9d3bac25ed1af1441ace
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903167"
---
# <a name="customer-payment-predictions"></a>Kundebetalingsforutsigelser

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver funksjonene for betalingsprediksjoner som kan hjelpe deg med å forstå de vanlige betalingspraksisene til en kunde. Denne funksjonen kan også hjelpe til med å identifisere omstendigheter som skal føre til at du starter innkrevingsprosesser tidligere enn du ellers ville starte dem.

## <a name="overview"></a>Oversikt

For organisasjoner er det ofte vanskelig å forutse når kunder betaler fakturaer. Denne mangelen på innsikt kan forårsake følgende problemer:

- Mindre nøyaktige kontantstrømprognoser
- Innkrevingsprosesser som starter for sent
- Ordrer som blir frigitt til kunder som kan være på etterskudd med betalingen

Kundebetalingsprediksjoner hjelper organisasjoner med å forutse når en kundefaktura skal betales. Derfor kan de opprette strategier for innkreving som bidrar til å øke sjansene for at de vil bli betalt i tide.

## <a name="predictions"></a>Prognoser

Betalingsprediksjoner lar organisasjoner forbedre forretningsprosessene ved å hjelpe dem med å identifisere hvilke fakturaer som sannsynligvis kommer til å betales for sent. Organisasjonen kan bruke denne informasjonen til å iverksette handlinger som forbedrer sjansene for at de blir betalt i tide.

Funksjonen for prediksjoner av kundebetaling bruker en maskinlæringsmodell for å mer nøyaktig prediksjon av når en kunde betaler en utestående faktura. Denne maskinlæringsmodellen omfatter historiske fakturaer, betalinger og kundedata.

For hver åpne faktura tilordner funksjonen tre betalingssannsynligheter:

- Sannsynligheten for at betalingen blir utført i tide
- Sannsynligheten for at betalingen blir utført forsinket
- Sannsynligheten for at betalingen blir utført svært sent

Funksjonen gir også en aggregert visning av forventede betalinger.

[![Aggregert visning av betalingsprognoser.](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Hver faktura blir tildelt en sannsynlighet for betaling i tide. Fakturaer med sannsynlighet for betaling til rett tid som er mindre enn 50 %, merkes med en rød sirkel for å angi at de kan kreve oppmerksomhet fra innkrevingsagenter.

[![Liste over sannsynligheter for betaling.](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Funksjonen for kundebetalingsprediksjoner inneholder også kontekstavhengig informasjon som forklarer prediksjonen. Denne informasjonen omfatter de viktigste faktorene som påvirket prediksjonen, firmaets gjeldende forretningsrelasjon til kunden, og detaljer om kundens historiske betalingsvirkemåte.

I mange bedrifter har innkrevingsprosessen vært en reaktiv aktivitet. Innkrevingsprosessen starter med andre ord ikke før fakturaer forfaller. Med kundebetalingsprediksjoner kan organisasjoner være mer proaktive om innkrevinger. De trenger ikke lenger å vente på at en transaksjon skal forfalle før start av innkrevingsprosessen. I stedet kan de bruke betalingsprognosefunksjonen til å fastslå om proaktive innkrevinger vil forbedre sannsynligheten for at de blir betalt i tide.

## <a name="methodology"></a>Metodologi

Tidligere var det som regel vanskelig å utvikle og distribuere en kunstig intelligensløsning (AI). Prosessen har krevd et team som inkluderer datateknikere, fageksperter og teknikere som arbeider i et lengre tidsrom for å formulere, utvikle, distribuere og vedlikeholde en brukbar AI-løsning. Kundebetalingsprediksjoner gjør det enkelt å distribuere og bruke en AI-løsning i Microsoft Dynamics 365 Finance. Microsoft forhåndspakker AI-løsninger som er bygd på toppen av Microsoft AI Builder. Brukerne kan derfor distribuere AI-løsningen i ett enkelt museklikk for å dra nytte av fordelene med intelligente prediksjoner. Hvis du ikke er tilfreds med nøyaktigheten i prognosene, kan en privilegert bruker (med ett enkelt museklikk) angi utvidelsesopplevelsen for AI Builder, og deretter merke av for eller fjerne merket for feltene som brukes til å generere prognoser. Når du er klar, kan du "lære opp" modellen og publisere endringene. Den nylig opplærte modellen vil automatisk bli plukket opp for å generere prediksjoner i Dynamics 365 Finance.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
