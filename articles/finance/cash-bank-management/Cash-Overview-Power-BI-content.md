---
title: Power BI-innholdet Kontantstrømoversikt
description: Dette emnet beskriver Power BI-innholdet Kontantstrømoversikt. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdet, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdet.
author: saraschi2
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 794a8b19224858a690f2b857c0d7278ed177d531
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830598"
---
# <a name="cash-overview-power-bi-content"></a>Power BI-innhold i Kontantstrømoversikt

[!include [banner](../includes/banner.md)]

Dette emnet beskriver innholdet **Kontantoversikt** Microsoft Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdet, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="overview"></a>Oversikt

Power BI-innholdet **Kontantstrømoversikt** ble opprettet for personer som er ansvarlige for kontanter i organisasjonen. Power BI-innholdet **Kontantstrømoversikt** gir oversikt over kontantstrømmen. Det gir i tillegg prognoser som kan hjelpe deg å ta bedre beslutninger og derfor forbedre tilstanden til kontantstrømmen. Du kan analysere kontanter etter juridisk enhet, valuta og bankkonto for å få en bedre forståelse av overskudd og underskudd.

## <a name="setup-needed-to-view-power-bi-content"></a>Oppsett måtte vise Power BI-innhold

Følgende oppsett må være fullført for at data skal kunne vises i Power BI-visualobjektene **Kontantstrømoversikt** og **Bank**.

1. Gå til **Systemadministrasjon > Oppsett > Systemparametere** for å angi **Systemvaluta** og **Valutakurs for system**.
2. Gå til **Økonomi > Kalendere > Regnskapskalendere** for å validere regnskapskalenderdatoer som er tilordnet den aktive tidsperioden.
3. Gå til **Økonomimodul > Oppsett > Finans** for å angi **Regnskapsvaluta** og **Type valutakurs**.
4. Definer valutakurser mellom transaksjonsvalutaer og regnskapsvaluta, regnskapsvaluta og systemvaluta samt regnskapsvaluta og bankvalutaer. Du kan gjøre dette ved å gå til **Økonomimodul > Valutaer > Valutakurser**.
5. Konfigurer og kjør kontantstrømprognoser. Hvis du vil ha mer informasjon om hvordan du definerer kontantstrømprognoser, kan du se [Kontantstrømprognose](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting). 
6. Gå til **Systemadministrasjon > Oppsett > Enhetslager** for å oppdatere den aggregerte målingen **LedgerCovLiquidityMeasurement**.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innholdet

Rapporter fra Power BI-innholdet **Kontantstrømoversikt** vises i **Kontantstrømoversikt**- og **Bank**-arbeidsområdet.

Hvis du vil vise kontantstrømmen prognoserapporter med data, må du først kjøre den prognoseberegning prosessen ved hjelp av funksjonen **Beregn kontantstrømprognoser** fra området for kontant- og bankbehandling. Dette må være fullført for hvert firma som er inkludert i prognosen.  Deretter må du oppdatere LedgerCovLiquidityMeasurement-aggregatmålinger på **Enhetslager**-siden  

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]