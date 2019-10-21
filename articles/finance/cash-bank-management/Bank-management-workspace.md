---
title: Arbeidsområde for bank
description: Dette emnet gir informasjon om arbeidsområdet for bank. Dette arbeidsområdet viser informasjon som er knyttet til firmaets bankkontoer, og inneholder en sammendragsvisning og en Analyse-side. Sammendragsvisningen viser sammendragsfliser, bankkontoinformasjon, et saldodiagram og relatert informasjon. Analyse-siden bruker funksjonene i Microsoft Power BI til å vise bilder som er knyttet til bankkontosaldoer.
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 20847ea4651b816fc95135ca03667ae297cde5be
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188493"
---
# <a name="bank-management-workspace"></a>Arbeidsområde for bank

[!include [banner](../includes/banner.md)]

Arbeidsområdet **Bank** viser informasjon som er knyttet til firmaets bankkontoer. Arbeidsområdet inneholder en **Sammendrag**-visning og en **Analyse**-side. **Sammendrag**-visningen viser sammendragsfliser, bankkontoinformasjon, et saldodiagram og relatert informasjon. **Analyse**-siden bruker funksjonene i Microsoft Power BI til å vise bilder som er knyttet til bankkontosaldoer.

## <a name="summary-view"></a>Sammendrag-visningen

### <a name="summary"></a>Sammendrag

Flisene i **Sammendrag**-delen gir en oversikt over bankkontoene og rask tilgang til sidene du oftest må bruke. Informasjon om bankavstemming gjeler spesifikt for funksjonen Avansert bankavstemming. Informasjon tas bare med for de bankkontoene som har alternativet **Avansert bankavstemming** satt til **Ja** på **Bankkonto**-siden. Fra **Sammendrag**-delen kan du importere elektroniske bankfiler for bankkontoer på tvers av alle juridiske enheter.

### <a name="bank-accounts"></a>Bankkontoer

Hver bankkonto i den juridiske enheten representeres av et kort i **Bankkontoer**-delen. Gjeldende saldo vises, og du kan drille ned til transaksjonene som utgjør dette sammendragssaldobeløpet. **Mellomtransaksjoner**-beløpet gjør også at du kan drille ned til transaksjonene som utgjør dette sammendragsbeløpet. Mellomtransaksjoner er alle utestående transaksjoner som er postert ved hjelp av funksjonen for mellompostering, men som ikke er fjernet ennå. **Ventende saldo**-beløpet er gjeldende saldo minus de mellomposterte, eller ventende, transaksjonene.

Kortet viser også da bankkontoen sist ble avstemt. Denne informasjonen vises bare hvis Avansert bankavstemming er aktivert for bankkontoen.

### <a name="balance"></a>Beholdning

Diagrammet **Saldo** viser historisk saldoinformasjon for bankkontoen som er valgt i **Bankkontoer**-delen eller et sammendrag av historisk saldoinformasjon for alle bankkontoer i den juridiske enheten. Denne informasjonen er tilgjengelig for ulike perioder: gjeldende uke, gjeldende måned, gjeldende år, de siste fem årene og alle perioder (hele loggen for bankkontoen). 

Hvis du viser diagrammet **Saldo** for én bankkonto, vises de historiske saldoene i bankkontovalutaen. Hvis du viser diagrammet for alle bankkontoer i den juridiske enheten, vises de historiske saldoene i regnskapsvalutaen.

Informasjon om da dataene sist ble oppdatert, vises øverst i diagrammet. Du kan oppdatere dataene du trenger.

### <a name="related-information"></a>Beslektet informasjon

Fra delen **Beslektet informasjon** kan du åpne **Økonomijournal**-siden for å fullføre bankoverføringer. Du kan også raskt åpne sidene **Banktransaksjoner** og **Mellomtransaksjoner**.

## <a name="analytics-view"></a>Analyse-visningen

**Analyse**-siden inneholder viktige mål om bankkontoene i gjeldende firma. Følgende visualiseringer er tilgjengelige på siden:

-   Total banksaldo i systemvaluta
-   Saldo etter juridisk enhet
-   Dagens faktiske saldo i forhold til anslått saldo i bankkontovaluta
-   Saldo etter bankkonto
-   Saldo etter valuta

Du kan vise bankanalyse på tvers av alle firmaer fra arbeidsområdet **Kontantstrømoversikt – alle firmaer**.
