---
title: "Arbeidsområde for bank"
description: "Dette emnet gir informasjon om arbeidsområdet for bank. Dette arbeidsområdet viser informasjon som er knyttet til firmaets bankkontoer, og inneholder en sammendragsvisning og en Analyse-side. Sammendragsvisningen viser sammendragsfliser, bankkontoinformasjon, et saldodiagram og relatert informasjon. Analyse-siden bruker funksjonene i Microsoft Power BI til å vise bilder som er knyttet til bankkontosaldoer."
author: saraschi
manager: AnnBe
ms.date: 05/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 3abf4b151b177095b71d44e9a6c9fd8541eaa64e
ms.openlocfilehash: 759de82e9cd1c08f86c0a8eb55fa7bae5c4f740f
ms.contentlocale: nb-no
ms.lasthandoff: 06/14/2017

---
# Arbeidsområde for bank
<a id="bank-management-workspace" class="xliff"></a>

Arbeidsområdet **Bank** viser informasjon som er knyttet til firmaets bankkontoer. Arbeidsområdet inneholder en **Sammendrag**-visning og en **Analyse**-side. **Sammendrag**-visningen viser sammendragsfliser, bankkontoinformasjon, et saldodiagram og relatert informasjon. **Analyse**-siden bruker funksjonene i Microsoft Power BI til å vise bilder som er knyttet til bankkontosaldoer.

## Sammendrag-visningen
<a id="summary-view" class="xliff"></a>

### Sammendrag
<a id="summary" class="xliff"></a>

Flisene i **Sammendrag**-delen gir en oversikt over bankkontoene og rask tilgang til sidene du oftest må bruke. Informasjon om bankavstemming gjeler spesifikt for funksjonen Avansert bankavstemming. Informasjon tas bare med for de bankkontoene som har alternativet **Avansert bankavstemming** satt til **Ja** på **Bankkonto**-siden. Fra **Sammendrag**-delen kan du importere elektroniske bankfiler for bankkontoer på tvers av alle juridiske enheter.

### Bankkontoer
<a id="bank-accounts" class="xliff"></a>

Hver bankkonto i den juridiske enheten representeres av et kort i **Bankkontoer**-delen. Gjeldende saldo vises, og du kan drille ned til transaksjonene som utgjør dette sammendragssaldobeløpet. **Mellomtransaksjoner**-beløpet gjør også at du kan drille ned til transaksjonene som utgjør dette sammendragsbeløpet. Mellomtransaksjoner er alle utestående transaksjoner som er postert ved hjelp av funksjonen for mellompostering, men som ikke er fjernet ennå. **Ventende saldo**-beløpet er gjeldende saldo minus de mellomposterte, eller ventende, transaksjonene.

Kortet viser også da bankkontoen sist ble avstemt. Denne informasjonen vises bare hvis Avansert bankavstemming er aktivert for bankkontoen.

### Beholdning
<a id="balance" class="xliff"></a>

Diagrammet **Saldo** viser historisk saldoinformasjon for bankkontoen som er valgt i **Bankkontoer**-delen eller et sammendrag av historisk saldoinformasjon for alle bankkontoer i den juridiske enheten. Denne informasjonen er tilgjengelig for ulike perioder: gjeldende uke, gjeldende måned, gjeldende år, de siste fem årene og alle perioder (hele loggen for bankkontoen). 

Hvis du viser diagrammet **Saldo** for én bankkonto, vises de historiske saldoene i bankkontovalutaen. Hvis du viser diagrammet for alle bankkontoer i den juridiske enheten, vises de historiske saldoene i regnskapsvalutaen.

Informasjon om da dataene sist ble oppdatert, vises øverst i diagrammet. Du kan oppdatere dataene du trenger.

### Beslektet informasjon
<a id="related-information" class="xliff"></a>

Fra delen **Beslektet informasjon** kan du åpne **Økonomijournal**-siden for å fullføre bankoverføringer. Du kan også raskt åpne sidene **Banktransaksjoner** og **Mellomtransaksjoner**.

## Analyse-visningen
<a id="analytics-view" class="xliff"></a>

**Analyse**-siden inneholder viktige mål om bankkontoene i gjeldende firma. Følgende visualiseringer er tilgjengelige på siden:

-   Total banksaldo i systemvaluta
-   Saldo etter juridisk enhet
-   Dagens faktiske saldo i forhold til anslått saldo i bankkontovaluta
-   Saldo etter bankkonto
-   Saldo etter valuta

Du kan vise bankanalyse på tvers av alle firmaer fra arbeidsområdet **Kontantstrømoversikt – alle firmaer**.

