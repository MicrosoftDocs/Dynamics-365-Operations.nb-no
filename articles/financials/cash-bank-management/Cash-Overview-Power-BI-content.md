---
title: "Power BI-innholdet Kontantstrømoversikt"
description: "Dette emnet beskriver Power BI-innholdet Kontantstrømoversikt. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdet, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: saraschi2
manager: AnnBe
ms.date: 06/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: fdcd3083f475967ec2e5f94dad850a1bf98c864a
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="cash-overview-power-bi-content"></a>Power BI-innholdet Kontantstrømoversikt

[!include[banner](../includes/banner.md)]

Dette emnet beskriver Microsoft Power BI-innholdet **Kontantstrømoversikt**. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdet, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="overview"></a>Oversikt

Power BI-innholdet **Kontantstrømoversikt** ble opprettet for personer som er ansvarlige for kontanter i organisasjonen. Power BI-innholdet **Kontantstrømoversikt** gir oversikt over kontantstrømmen. Det gir i tillegg prognoser som kan hjelpe deg å ta bedre beslutninger og derfor forbedre tilstanden til kontantstrømmen. Du kan analysere kontanter etter juridisk enhet, valuta og bankkonto for å få en bedre forståelse av overskudd og underskudd.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innhold

Hvis du bruker Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017), vil rapporter fra **Kontantstrømoversikt** Power Bi-innholdet vises i arbeidsområdene **Kontantstrømoversikt** og **Bankbehandling**.

Hvis du vil vise kontantstrømmen prognoserapporter med data, må du først kjøre den prognoseberegning prosessen ved hjelp av funksjonen **Beregn kontantstrømprognoser** fra området for kontant- og bankbehandling.  Dette må være fullført for hvert firma som er inkludert i prognosen.  Deretter må du oppdatere LedgerCovLiquidityMeasurement-aggregatmålinger på **Enhetslager**-siden  

For demonstrasjonsformål kan du legge til kontantstrøm prognostedemodataene ved hjelp av siden **Generer data** fra modulen Demodata.  Dette skriptet vil sette inn data i kontantstrømmens prognosetabeller for å raskt fylle ut informasjonen som kreves for rapporter.  Denne modulen er bare tilgjengelig hvis du har Demodatapakkemodellen distribuert i miljøet. 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter som er inkludert i Power BI-innholdet
Tabellen nedenfor viser detaljer om mål som finnes på hver rapportside i Power BI-innholdet **Kontantstrømoversikt**.

| Rapporter                                | Innhold |
|---------------------------------------|----------|
| Kontantstrømoversikt – alle firmaer         | <ul><li>Innflyt og utflyt i systemvaluta</li><li>Anslåtte valutasaldoer</li><li>Total banksaldo i systemvaluta</li><li>Saldo etter juridisk enhet</li><li>Dagens faktiske saldo i forhold til anslått saldo i bankkontovaluta</li></ul> |
| Kontantstrømoversikt – gjeldende firma       | <ul><li>Innflyt og utflyt i regnskapsvaluta</li><li>Anslåtte valutasaldoer</li><li>Total banksaldo i regnskapsvaluta</li><li>Dagens faktiske saldo i forhold til anslått saldo i bankkontovaluta</li></ul> |
| Kontantstrømprognose – alle firmaer    | <ul><li>Innflyt og utflyt i systemvaluta</li><li>Sammendrag av daglig prognose</li><li>Prognosedetaljer</li></ul> |
| Kontantstrømprognose – valutafirma | <ul><li>Innflyt og utflyt i regnskapsvaluta</li><li>Daglig sammendrag av prognose</li><li>Prognosedetaljer</li></ul> |
| Valutaprognose                     | <ul><li>Anslåtte valutasaldoer</li><li>Daglig sammendrag av valuta</li><li>Prognosedetaljer</li></ul> |
| Banksaldoer                         | <ul><li>Total banksaldo i systemvaluta</li><li>Saldo etter juridisk enhet</li><li>Dagens faktiske saldo i forhold til anslått saldo i bankkontovaluta</li><li>Saldo etter bankkonto</li><li>Saldo etter valuta</li></ul> |

## <a name="extending-the-power-bi-content"></a>Utvide Power BI-innholdet
Du kan gi personer som ikke logger på Dynamics 365, gode analyser ved å bruke innholdspakkene som er tilgjengelige i Lifecycle Services (LCS). Disse innholdspakkene kan endres slik at de inneholder andre rapporter eller visuelle hjelpemidler, og deretter publiseres på Power BI.com-leieren for analyse. 

Du kan finne Power BI-innholdet **Kontantstrømoversikt** i det delte aktivabiblioteket i LCS. Hvis du vil ha mer informasjon om hvordan du laster ned innholdet og implementerer det i organisasjonen, kan du se [Power BI-innhold i LCS fra Microsoft og partnerne](../../dev-itpro/analytics/power-bi-content-microsoft-partners.md). Hvis du vil se en demo som viser hvordan du implementerer Power BI-innholdet, kan du se [Power BI-innhold fra Microsoft og partnerne i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter

Tabellen nedenfor viser enhetene som Power BI-innholdet **Kontantstrømoversikt** er basert på.

| Enhet                                                                          | Innhold |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Company                                          | Selskaper til å filtrere rapporter etter |
| LedgerCovLiquidityMeasurement\_Date                                             | Datoer å filtrere rapporter etter |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | Faktisk banksaldo i forhold til sist anslåtte banksaldo |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | Detaljer om anslått transaksjon |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | Summering av kontant innflyt, utflyt og saldo ved hjelp av regnskapsvalutaen for hvert firma |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | Summering av kontant innflyt, utflyt og saldo ved hjelp av systemvalutaen for alle firmaer |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | Summering av netto transaksjonsbeløp og saldo for valutaer ved hjelp av transaksjonsvalutaen |

Disse enhetene ble brukt til å opprette beregnede mål i datamodellen. Disse beregnede målene brukes deretter til å beregne diagrammene og rapportene som brukes i Power BI-innholdet **Kontantstrømoversikt**. Hvis du vil ha med flere beregninger i rapportene og instrumentbordet, kan du laste ned og endre filen Power BI-filen fra LCS. Denne filen er standarddatamodellen som ble brukt til å opprette innholdet. Når du har gjort endringene, kan du opprette innhold og instrumentbord for organisasjonen som inneholder informasjonen du har lagt til.


